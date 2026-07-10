---
title: "Blog 2"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 3.2. </b> "
---
{{% notice warning %}}
⚠️ **Note:**All content below is provided for guidance and reference purposes only. Please rewrite it in your own words and do not copy any passage verbatim, including this notice, into your official report.
{{% /notice %}}

<div class="workshop-big-title">
OPTIMIZING DISASTER RECOVERY FOR STATEFUL SERVICES ON AMAZON EKS WITH VELERO
</div>

Ensuring high availability and data security is always a critical requirement for systems running on Kubernetes. Accidentally deleting a namespace in a production environment or encountering errors during a cluster upgrade may require the operations team to manually rebuild all resources, which can consume a significant amount of time and effort.

The disaster recovery solution using the open-source Velero tool automates the process of packaging logical resource configurations and storing them in Amazon S3. At the same time, it creates snapshots of the physical storage volumes used by stateful applications through Amazon EBS Snapshots. This article provides a detailed overview of the architecture, operational workflow, and important technical considerations identified during the practical implementation of the solution on Amazon EKS.

## 1. Core advantages of the solution

The deployment architecture focuses on optimizing the system in two important areas: preserving data integrity and strengthening infrastructure security.

- **Security through EKS Pod Identity:** Instead of using static credentials or granting excessive `cluster-admin` permissions, the solution uses EKS Pod Identity to provide temporary AWS permissions. Combined with a custom ClusterRole, Velero is only allowed to interact with the required `apiGroups` according to the principle of least privilege.
- **Synchronized backup of two components:** Velero simultaneously backs up logical configuration resources such as Deployments, PVCs, and Secrets by compressing and uploading them to Amazon S3, while the actual application data stored on gp3 volumes is preserved using Amazon EBS Snapshots.
- **Flexible cross-Namespace recovery:** The `namespaceMapping` feature allows the entire application and its historical data to be quickly restored from an existing snapshot into a new and independent namespace without affecting the original environment.

## 2. System operational workflow

The solution's data-processing workflow is divided into two independent stages through Kubernetes Custom Resources:

- **During backup:** The Velero controller receives the backup request and scans the Kubernetes API to collect all resource definitions in the specified namespace. These resources are compressed and uploaded to an S3 Bucket. For persistent storage volumes, the system also calls AWS APIs to create Amazon EBS Snapshots, preserving the state of the data at the time of backup.
- **During recovery:** When restoring the application to a new namespace, Velero reads the configuration data stored in Amazon S3 and retrieves the snapshot information created during the previous backup. AWS then creates a new gp3 volume from the snapshot. The volume is automatically attached to a Worker Node, allowing the application to continue accessing and writing historical data without interruption.

<div class="image-holder large">
Backup Restore
</div>

## 3. Technology selection and storage scope

<table class="work-table">
  <thead>
    <tr>
      <th>System component</th>
      <th>Technology used</th>
      <th>Role in the architecture</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Control Plane Backup</td>
      <td>Amazon S3</td>
      <td>Centrally stores logical Kubernetes resource definitions in compressed .tar.gz files.</td>
    </tr>
    <tr>
      <td>Data Plane Backup</td>
      <td>Amazon EBS Snapshots</td>
      <td>Stores the actual data of stateful applications using block-level snapshots.</td>
    </tr>
    <tr>
      <td>Identity & Access</td>
      <td>EKS Pod Identity</td>
      <td>Manages identity and grants temporary IAM permissions to Velero Pods.</td>
    </tr>
    <tr>
      <td>Orchestration</td>
      <td>Velero Server & Helm</td>
      <td>Manages the lifecycle of backup and restore operations within the Kubernetes cluster.</td>
    </tr>
  </tbody>
</table>

## 4. Technical considerations for practical deployment

During the implementation and configuration process, several environment-specific issues required direct adjustments to the infrastructure.

### Windows CMD environment considerations

Because the original documentation is mainly designed for Linux environments, environment variable syntax must be converted to the `%VARIABLE%` format when commands are executed in Windows CMD. In addition, commands used to generate YAML manifest files from the terminal should be enclosed within parentheses or executed through PowerShell to prevent errors caused by special characters.

<div class="image-holder medium">
EKS Pod Identity Association
</div>

### Pods stuck in the Pending state

This issue may occur because the sample AWS deployment manifest contains node-selection settings designed for EKS Auto Mode. If the actual cluster uses a standard Managed Node Group, the Pod may not be scheduled on any available Worker Node. Removing the node-selection configuration from the deployment file allows the Pod to transition to the Running state and attach the persistent volume successfully.

<div class="image-holder medium">
Velero Backup Completed
</div>

## 5. Conclusion

The combination of Velero and Amazon EKS through the EKS Pod Identity authentication mechanism provides a comprehensive disaster recovery solution for stateful applications in cloud environments. This approach not only satisfies strict enterprise security requirements but also significantly reduces the operational workload when the system encounters accidental deletion, cluster failures, or other major incidents.

**Original article:** https://aws.amazon.com/blogs/containers/back-up-and-restore-your-amazon-eks-cluster-resources-using-velero/
