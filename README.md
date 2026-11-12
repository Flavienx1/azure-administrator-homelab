# Azure Administrator Homelab

I am building a hands-on administration portfolio as I move from IT Support (L1/L2) toward Azure Administrator, Cloud Engineer and DevOps Engineer roles. I earned Microsoft Azure Fundamentals (AZ-900). This repository records the configurations, validation results and troubleshooting decisions from my lab.

## Environment

- Local lab: VirtualBox, Windows Server 2022, Active Directory Domain Services (AD DS), DNS, DHCP, Group Policy, SMB and a Windows 11 client.
- Cloud lab: Microsoft Entra ID is the current area of study. Azure infrastructure and hybrid integration are scheduled in later modules.

See the [architecture diagram](architecture/README.md) for the reported local topology and its verification limits.

## Module progress

| Module | Status | Objective |
| --- | --- | --- |
| [On-premises Active Directory](00-On-Premises-Active-Directory/README.md) | In progress | Document the Windows domain and verify its current baseline. |
| [Microsoft Entra ID](01-Microsoft-Entra-ID/README.md) | In progress | Manage identities, access and authentication in a cloud tenant. |
| [Azure governance and RBAC](02-Azure-Governance-RBAC/README.md) | Planned | Organize resources and validate least-privilege access. |
| [Azure networking](03-Azure-Networking/README.md) | Planned | Build private connectivity and diagnose traffic flows. |
| [Azure compute](04-Azure-Compute/README.md) | Planned | Deploy and operate virtual machines with documented availability choices. |
| [Azure storage](05-Azure-Storage/README.md) | Planned | Manage data access, redundancy and lifecycle. |
| [Monitoring and security](06-Monitoring-Security/README.md) | Planned | Collect telemetry, investigate events and review security recommendations. |
| [Backup and disaster recovery](07-Backup-Disaster-Recovery/README.md) | Planned | Prove data recoverability with a measured restore. |
| [Hybrid identity](08-Hybrid-Identity/README.md) | Planned | Connect a verified local directory to a test tenant and validate synchronization. |

**Planned** indicates an exercise on the roadmap. **In progress** indicates work or documentation has started. **Validated** requires a recorded result and supporting evidence for the exercise. A module can contain exercises at different stages.

## Technical skills demonstrated

- Interpreting historical domain controller connectivity and DNS diagnostics.
- Distinguishing basic reachability from AD service discovery and identifying a resolver that could not answer the domain's locator query.

See the [DNS diagnostic case](troubleshooting/dns-domain-controller-discovery.md) for the evidence and outstanding verification.

## Progress log

| Date | Milestone |
| --- | --- |
| 2026-11-12 | Established the portfolio structure, documented the reported local lab and historical DNS diagnosis, and recorded the start of Microsoft Entra ID work. |

## Project resources

[Architecture](architecture/README.md) · [Troubleshooting](troubleshooting/README.md) · [Screenshots](screenshots/README.md) · [Scripts](scripts/README.md) · [Exercise template](exercise-template.md)
