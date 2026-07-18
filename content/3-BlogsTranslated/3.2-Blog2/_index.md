---
title: "Blog 2"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 3.2. </b> "
---

# Optimizing the Disaster Recovery Process for Stateful Services on Amazon EKS Using Velero

Ensuring high availability and data safety is always a critical challenge for systems running on Kubernetes. When a namespace is accidentally deleted in a production environment or when a cluster upgrade fails, manually rebuilding all resources consumes a great deal of time and effort from the operations team.

The disaster recovery backup and restore solution using the open-source Velero tool helps automate the packaging of logical configurations to Amazon S3, while also taking physical disk snapshots of stateful applications in the form of Amazon EBS Snapshots. This article summarizes the architecture, workflow, and important technical notes learned from the practical deployment of this solution on an Amazon EKS system.

---

## 1. Core advantages of the solution

The deployment architecture focuses on optimizing the system based on two important aspects: maintaining data integrity and strengthening infrastructure security standards.

- **Security through EKS Pod Identity:** Instead of using static credentials such as long-term AWS Access Keys or overusing the system’s default `cluster-admin` privileges, the solution establishes a short-term authorization mechanism through EKS Pod Identity. Combined with a custom `ClusterRole`, Velero is only allowed to interact minimally with the necessary apiGroups according to the Least Privilege principle.
- **Synchronized backup of two components:** Unlike common solutions that only store soft configurations, Velero processes both logical configuration files in parallel, such as Deployments, PVCs, and Secrets compressed and pushed to Amazon S3, and actual data stored on gp3 disks, which is frozen and converted into Amazon EBS Snapshots.
- **Flexible cross-namespace restoration:** The `namespaceMapping` feature allows the entire application to be quickly restored and historical data from an old snapshot to be pulled into a new independent namespace (`myrestore`) without affecting the original environment.

---

## 2. System workflow

The data processing flow of the solution is clearly divided into two independent phases through Kubernetes Custom Resources:

- **When backing up:** The Velero controller receives the request, scans the Kubernetes API to collect all resource definitions in the specified namespace, and pushes the compressed file to the S3 Bucket. For persistent physical disk volumes, the system simultaneously calls the AWS API to trigger the physical disk snapshot process (EBS Snapshot) in order to freeze the data state at the time of backup.
- **When restoring:** When restoring to a new namespace, AWS automatically analyzes the configuration data stored on S3, reads the old snapshot information from the previous backup process, and creates a completely new `gp3` disk. This new disk is automatically mounted to the Worker Node so the application can continue writing data to the historical file without interruption.

---

![Backup restore](/images/104.png)

## 3. Technology selection and storage scope

| System component | Technology used | Role in the architecture |
| :--- | :--- | :--- |
| **Control Plane Backup** | Amazon S3 | Centrally stores logical resource definition files in `.tar.gz` format |
| **Data Plane Backup** | Amazon EBS Snapshots | Stores the actual stateful application data using the block storage mechanism |
| **Identity & Access** | EKS Pod Identity | Manages identity and grants short-term permissions to Pods through IAM Role |
| **Orchestration** | Velero Server & Helm | Manages the lifecycle of backup and restore processes for resources in the cluster |

---

## 4. Technical notes for practical deployment

During the process of configuring the solution, several environment-specific issues occurred and needed to be adjusted directly on the infrastructure:

### Windows CMD environment characteristics

Since the original documentation was fully optimized for the Linux environment, when executing commands on Windows CMD, all environment variable syntax must be converted to the `%VARIABLE%` format. In addition, the process of generating YAML manifest configuration files from the terminal needs to be wrapped in opening and closing command blocks or use implicit PowerShell commands to avoid special character formatting errors.

![EKS Pod Identity Association](/images/101.png)

### Pod stuck in Pending status error (FailedScheduling)

This error occurs because the sample AWS deployment file uses a node selection configuration by default (`nodeSelector` bound to EKS Auto Mode). If the actual infrastructure is running a normal Standard Node Group cluster, the Pod cannot be scheduled. Proactively removing this node filtering configuration line from the deployment file helps the application quickly move to the `Running` state and mount the disk smoothly.

---

![Velero Backup Completed](/images/100.png)

## 5. Conclusion

The combination of Velero and Amazon EKS through the Pod Identity authentication mechanism provides a comprehensive disaster recovery solution for stateful applications in the cloud environment. This approach not only satisfies strict enterprise security standards but also significantly reduces the operational burden for the Operations team when the system faces major incidents.

Original article: https://aws.amazon.com/blogs/containers/back-up-and-restore-your-amazon-eks-cluster-resources-using-velero/