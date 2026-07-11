---
title: "Week 12 Worklog"
date: 2026-07-10
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---
{{% notice warning %}} 
⚠️ **Note:** The following information is for reference purposes only. Please **do not copy verbatim** for your own report, including this warning.
{{% /notice %}}


### Week 12 Objectives:

* Verify the whole system after AWS deployment, from the access layer to the processing and data layers.
* Build test scenarios for main functions, idempotency, concurrency, rate limiting, and fault tolerance.
* Run load tests to observe latency, throughput, error rate, and resource usage of ECS, RDS, and Redis.
* Tune operational parameters, complete project documentation, and clean up AWS resources after testing.

### Tasks to be carried out this week:
| Date | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 07/03/2026 | - Check system status after deployment<br>&emsp; + Verify API Gateway, VPC Link, Internal ALB, target groups, and ECS tasks<br>&emsp; + Review service startup logs in CloudWatch<br>&emsp; + Confirm that services connect to RDS PostgreSQL and ElastiCache Redis | 07/03/2026 | 07/03/2026 | AWS Console, CloudWatch Logs |
| 07/04/2026 | - Test the main business flows<br>&emsp; + Send account creation requests and check initial balance<br>&emsp; + Send payment creation requests through API Gateway<br>&emsp; + Query payment and transaction status to verify processed data | 07/04/2026 | 07/04/2026 | API test scenarios |
| 07/05/2026 | - Test idempotency and data consistency<br>&emsp; + Repeat payment requests with the same idempotencyKey<br>&emsp; + Check transactionId in Account Service to ensure no repeated debit occurs<br>&emsp; + Try a different payload with the same key to confirm invalid requests are rejected | 07/05/2026 | 07/05/2026 | Payment Service, Account Service |
| 07/06/2026 | - Test concurrency and rate limiting<br>&emsp; + Send many parallel requests to the payment creation API<br>&emsp; + Observe Redis lock and state machine behavior in duplicate-processing prevention<br>&emsp; + Check user-based request limits and responses when thresholds are exceeded | 07/06/2026 | 07/06/2026 | Redis, API Gateway |
| 07/07/2026 | - Test failure scenarios and recovery behavior<br>&emsp; + Simulate slow or unstable Account Service responses<br>&emsp; + Observe retry, circuit breaker, and how payments keep their status while waiting for resolution<br>&emsp; + Review logs to identify failure causes and trace request flow | 07/07/2026 | 07/07/2026 | Resilience4j, CloudWatch |
| 07/08/2026 | - Run load tests and monitor resources<br>&emsp; + Gradually increase request volume to measure latency, throughput, and error rate<br>&emsp; + Monitor CPU, memory, ECS task count, database connections, and Redis metrics<br>&emsp; + Record bottlenecks or unsuitable configuration during the load test | 07/08/2026 | 07/08/2026 | CloudWatch, load testing tool |
| 07/09/2026 | - Tune, summarize results, and clean up resources<br>&emsp; + Adjust timeout, retry, rate limit, CPU/memory, and scaling policy based on test results<br>&emsp; + Update architecture diagram, worklog, test report, and project summary<br>&emsp; + Review, stop, or delete unused AWS resources to avoid additional cost | 07/09/2026 | 07/09/2026 | Test report, project documentation |

### Week 12 Achievements:

* Verified the deployed AWS system through the end-to-end flow. Requests move from API Gateway through VPC Link to the Internal ALB and are then routed to the correct ECS Service inside private subnets.

* Confirmed that the main services run on ECS Fargate and send centralized logs to CloudWatch. Logs help inspect service startup, connection errors, request handling errors, and health check status.

* Verified connectivity to RDS PostgreSQL and ElastiCache Redis in the deployed environment. Services can store and query business data while using Redis for fast-response functions.

* Executed the main payment system flows, including account creation, balance lookup, payment creation, and transaction query. Processed data is recorded correctly in the related components.

* Confirmed that idempotency works when requests are repeated. Payment Service does not create a new transaction when the idempotencyKey and payload match the earlier request.

* Verified duplicate-debit prevention in Account Service. When a transactionId has already been processed with valid data, repeated requests do not change the balance again.

* Detected and handled cases where a request reuses a key but changes the payload. The system rejects these requests to avoid confusing different transactions and protect data consistency.

* Evaluated the system's concurrent processing behavior. Redis lock, the state machine, and conditional updates reduce the risk of multiple requests processing the same payment.

* Verified user-based rate limiting at API Gateway. When request volume exceeds the allowed threshold, the system returns a throttling response instead of passing all traffic to downstream services.

* Observed retry and circuit breaker behavior when dependent services respond slowly or fail temporarily. This prevents repeated calls from growing uncontrollably and reduces the risk of incorrect payment status decisions.

* Ran basic load tests and monitored latency, throughput, error rate, CPU, memory, database connections, Redis metrics, and running task count.

* Based on test results, tuned operational settings such as timeout, retry, rate limit, container resources, and scaling policies to improve stability under higher load.

* Completed final documentation including the AWS architecture diagram, deployment flow, test scenarios, test results, bilingual worklog, and project summary.

* Reviewed AWS resources after testing and stopped or deleted resources that were no longer needed. This helped reduce additional cost and built a more careful habit of cloud resource management.