# Oracle Principal Core Infrastructure Engineer — AI infrastructure research

## Scope and evidence

The supplied attachment is the resume `_dev_Oracle_PrincipalCoreInfrastructureEngineer_346040.docx`. The message did not include a separate job-description URL, and the exact requisition 346040 was not available from Oracle's searchable careers pages during research. The role analysis below combines the resume's GPU/server/networking experience with Oracle's current official AI infrastructure and core infrastructure materials. A live official Core Infrastructure posting is used as a role-family comparator; details unique to requisition 346040 should be checked against its original job page if available.

## Company and technical context

Oracle Cloud Infrastructure (OCI) is investing in GPU infrastructure for distributed AI, machine learning, and HPC workloads. Oracle's AI Infrastructure page describes GPU bare-metal instances and RDMA cluster networking as building blocks for AI training and inference. Oracle documentation explains that these clusters connect GPU/HPC nodes using high-bandwidth, low-latency networking, including RDMA over converged Ethernet (RoCE), and discusses shared storage and parallel filesystems for multi-node workloads. This architecture makes host diagnostics, fabric validation, telemetry, data-path efficiency, recovery, and operational readiness important alongside application code.

Oracle's current Core Infrastructure posting family emphasizes scalable distributed/data-plane services, availability and durability requirements, high-throughput retrieval/storage/processing, in-service updates, failover, and resilience to partitions using load shedding, throttling, rate limits, retries, and timeouts. For GPU environments, the work naturally spans software services, Linux and GPU hosts, cluster networking, and operations: a healthy control/data plane must identify unhealthy capacity and help restore it without destabilizing workloads that are already running.

## Resume evidence

| Role need | Evidence in this resume |
| --- | --- |
| Large production estate | 1,000+ Linux servers; 1,200+ servers in the Sprouts AI service footprint |
| SLO and service ownership | 99.99% availability at 25K+ requests/sec; 45% lower MTTR |
| High-throughput data paths | 3.2x throughput and 48% lower p99 latency; profiling and zero-copy I/O |
| Distributed failure handling | 4x surges and network partitions without cascading failures; replication, failover, retries, timeouts, and quorum state |
| GPU/HPC infrastructure | 35% less GPU-node downtime across 300+ servers; automated hardware health checks and BMC/IPMI management |
| High-speed networking | InfiniBand and RoCE validation; Linux, TCP/IP, operating systems, memory, concurrency, and I/O tuning |
| Safe operations | Fleet-wide patches/rollbacks; Terraform and Ansible; canary automation; CI/CD; security controls and compliance docs |
| Data reliability | 2B+ events/day under 5 seconds lag with zero data loss; partitioned Kafka replication and idempotent writes |
| Fault diagnosis and learning | OpenTelemetry, Grafana, proactive alerting, fault injection, brownout tests, root-cause analysis, and recovery runbooks |
| Technical leadership | Mentored six engineers and drove incident response, operational readiness, and production quality |

## Preparation themes

- Explain how you measured availability and throughput, including the SLO boundary, request mix, load-test shape, and measurement window.
- Walk through a GPU/server health-check flow: BMC/IPMI inputs, host and device signals, fabric validation, triage, quarantine or repair, and safe return to service. Clearly separate implemented experience from proposed extensions.
- Discuss InfiniBand/RoCE/RDMA failure modes and how you would distinguish host, NIC, fabric, congestion, storage, and application bottlenecks using evidence.
- Describe the 3.2x throughput / 48% p99 result: baseline, profiling evidence, zero-copy changes, correctness checks, and regression protections.
- Detail how the system behaves during 4x demand or network partitions: shedding, throttling, rate limits, retries, timeouts, state ownership, and SLO protection.
- Present a node/zone recovery drill, including detection, quorum behavior, data consistency, runbook execution, and recovery time measurement.
- Explain fleet-safe patching: canary size, health gates, rollout state, rollback trigger, blast-radius limits, and how you prevent partial rollouts from lingering.
- Show how telemetry, fault injection, and brownout tests changed operations, including the 45% MTTR reduction and 90% pre-release regression detection.

## Authoritative sources

- [Oracle — AI Infrastructure](https://www.oracle.com/ai-infrastructure/)
- [Oracle Cloud Infrastructure — Deploy a Bare Metal GPU Cluster for AI Workloads](https://docs.oracle.com/en/solutions/deploy-bare-metal-gpu-cluster-for-ai/index.html)
- [Oracle Cloud Infrastructure — High Performance Computing](https://docs.oracle.com/en-us/iaas/Content/Compute/References/high-performance-compute.htm)
- [Oracle Careers — Principal Software Engineer, Core Infrastructure (role-family comparator)](https://careers.oracle.com/en/sites/jobsearch/job/345544/)
- [Oracle Cloud Infrastructure — High Availability](https://docs.oracle.com/en-us/iaas/Content/cloud-adoption-framework/high-availability.htm)
- [Oracle Cloud Infrastructure — Monitoring and Observability](https://docs.oracle.com/en-us/iaas/Content/cloud-adoption-framework/monitoring-and-observability.htm)
