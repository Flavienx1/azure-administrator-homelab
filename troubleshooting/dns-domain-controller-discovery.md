# Domain controller DNS diagnostics

**Status:** In progress

## Technical objective and environment

Investigate a DNS diagnostic failure on the Windows Server 2022 domain controller in the VirtualBox Active Directory lab. This case concerns the domain configuration that existed when the diagnostics were captured.

## Diagnostic procedure

The historical diagnostic used the Windows domain controller diagnostics tool (`dcdiag`). Its output included the connectivity and DNS tests. The [current validation checklist](../00-On-Premises-Active-Directory/evidence-checklist.md) gives the targeted commands to reproduce those checks on the current lab.

## Diagnosis

The domain controller passed the connectivity test. The enterprise DNS test failed. Its output showed that the external resolver could not resolve an AD LDAP service record. The internal resolver returned AD-related records in the diagnostic excerpt. Clients use these service records to locate domain controllers, so resolver selection matters even when basic network connectivity succeeds.

## Corrective action and validation

The lab owner later reported that the domain DNS test passed. The exact resolver change and full passing output are pending confirmation. The [evidence checklist](../00-On-Premises-Active-Directory/evidence-checklist.md) describes how to retest the current configuration.

## Evidence and skills

Historical diagnostic output supports the initial failure and the distinction between network connectivity and AD DNS resolution. The later pass is a reported result. A sanitized screenshot or output excerpt for the follow-up run remains to be collected.

[Incident index](README.md)
