# On-premises Active Directory Lab

**Status:** In progress

## Technical objective

Build and validate a Windows domain lab that supports domain discovery, client enrollment, group-based access, and policy application. Establish a verified baseline for later hybrid identity exercises.

## Architecture and prerequisites

The reported environment uses VirtualBox, a Windows Server 2022 VM used as the lab server, and a Windows 11 client VM. The server has acted as an AD DS domain controller and DNS server. DHCP, Group Policy, and security groups are part of the reported lab scope.

See the [architecture diagram](../architecture/README.md). Confirm the current domain name, network mode, DHCP configuration and client membership before recording the baseline.

The client needs a Windows edition that supports AD domain join, network reachability to the controller, and a resolver that can answer queries for the AD zone.

## Concepts

AD DS provides domain identities and authentication. DNS SRV records let a client locate a domain controller. DHCP supplies IP configuration, including the DNS resolver when configured. Security groups let administrators assign access by role. Group Policy applies settings according to scope and filtering.

## Configuration performed

Historical diagnostic output identifies the server as a domain controller and shows AD-related DNS records on the internal DNS service. The exact promotion workflow and settings are pending confirmation. The lab owner reports that a Windows 11 VM was set up and that the domain configuration was updated after the historical diagnostics. The current domain name and Windows 11 membership need fresh checks.

The historical work included Windows domain-controller diagnostics. See the [DNS troubleshooting case](../troubleshooting/dns-domain-controller-discovery.md) for the observed failure and follow-up. The [evidence checklist](evidence-checklist.md) contains commands proposed for the next validation pass.

## Screenshots and evidence

Historical diagnostic excerpts were reviewed. The checklist identifies screenshots and command output to collect for the current configuration.

## Validation and results

| Check | Observed result | Evidence |
| --- | --- | --- |
| Historical domain-controller connectivity | Pass | Historical diagnostic excerpt, `Connectivity` test |
| Historical enterprise DNS test | Initial failure. A subsequent pass was reported by the lab owner. | Historical output and follow-up report |
| Current domain and client membership | Pending | Server identity, client domain membership, and secure channel |
| Current DHCP, Group Policy, and group-based access | Pending | Lease, resultant policy, and access tests |

## Incidents and resolution

See [Domain controller DNS diagnostics](../troubleshooting/dns-domain-controller-discovery.md).

## Skills demonstrated

Historical evidence documents interpretation of domain-controller diagnostics and identification of a resolver that could not answer AD service-record queries.

## Planned exercises

- Verify the current AD DS and DNS baseline from both server and client.
- Confirm the Windows 11 domain join, secure channel and domain-user sign-in.
- Validate a DHCP lease, Group Policy application and group-based SMB access.
- Record the outcomes of the previously practised DNS, DHCP, SMB and RDP diagnostics where evidence is available.

[Portfolio home](../README.md)
