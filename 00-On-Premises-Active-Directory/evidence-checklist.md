# Active Directory validation and evidence checklist

The following checks are proposed for the current lab. Record the date, machine, and observed result for each check. Use a sanitized lab domain in published examples and redact account names, host network details, and unrelated information from screenshots and outputs.

| Area | Check to run | Evidence to capture |
| --- | --- | --- |
| Domain controller | On the server, run `hostname`, `Get-ADDomain \| Select-Object DNSRoot,NetBIOSName`, and `Get-WindowsFeature AD-Domain-Services,DNS,DHCP`. | Sanitized domain identity and installed role output. |
| AD DNS and reachability | On the server, run `dcdiag /test:dns`. On the client, check `ipconfig /all` and query the current AD locator record with `Resolve-DnsName -Type SRV "_ldap._tcp.dc._msdcs.<current-ad-domain>"`, replacing the placeholder. | Server test summary and client-side SRV answer. Confirm the VirtualBox adapter mode separately. |
| DHCP | If the lab server supplies DHCP, compare its scope options and client lease with `ipconfig /all` on the Windows 11 client. | Sanitized scope, DNS option, and client lease. |
| Windows 11 join | On the client, run `Get-CimInstance Win32_ComputerSystem \| Select-Object Domain,PartOfDomain`. Once joined, run `Test-ComputerSecureChannel` in an elevated PowerShell session and test a domain-user sign-in. | Domain membership, secure-channel result, and redacted sign-in evidence. |
| Group Policy | Record a policy setting and its linked OU. Run `gpresult /r` in the relevant user session and verify the intended setting. | GPO link, applied policy, and observed setting. |
| Security groups | Choose a test group and protected resource. Compare access for one test identity in the group and one outside it, after refreshing the relevant sessions. | Sanitized membership, permission assignment, and allowed and denied access results. |
| Historical DNS incident | Confirm the resolver change applied at the time if recorded. | Sanitized before-and-after output if available. |
| Configuration history | Confirm which installation and configuration steps were performed for server roles, the domain, DHCP, GPOs, security groups, and the client VM. | Original notes or screenshots. Record dates where known. |

## Screenshot set to collect

1. VirtualBox network settings for both VMs, with host interface details masked.
2. Server roles and sanitized domain identity, plus the AD DNS zone or client-side SRV query.
3. DHCP scope and lease, if DHCP runs on the lab server.
4. Windows 11 domain membership and secure-channel result.
5. One GPO link and its observed effect on the client.
6. SMB share and NTFS permissions with allowed and denied test results.

Use the [publication checklist](../screenshots/README.md) before adding screenshots.

[Active Directory lab](README.md)
