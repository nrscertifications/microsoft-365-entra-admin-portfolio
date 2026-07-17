# Hybrid Identity Synchronization & Health Monitoring

## Administrative Objective

Configure and verify hybrid identity synchronization between Windows Server Active Directory Domain Services and Microsoft Entra ID using Microsoft Entra Connect Sync and Microsoft Entra Cloud Sync.

The work used two separate lab forests:

| Server | Hosting | Active Directory forest | Synchronization method |
|---|---|---|---|
| `NYC-DC1` | Hyper-V | `ad.narindersharmalabs.xyz` | Microsoft Entra Connect Sync |
| `NYC-DC-CLOUD-SYNC` | Azure virtual machine | `narindersharmalabs.org` | Microsoft Entra Cloud Sync provisioning agent |

RDP and Hyper-V were used to manage the servers. The synchronization paths connected the Active Directory forests to Microsoft Entra ID.

## Work Completed

* Used IDFix to detect and correct a UPN formatting issue.
* Prepared OUs, fictional users, a security group, and account attributes for synchronization.
* Configured Microsoft Entra Connect Sync with a limited OU scope and Password Hash Synchronization.
* Verified synchronized users and Connect Sync status in Microsoft Entra.
* Deployed a separate Azure Windows Server domain controller for Cloud Sync.
* Installed and registered the Cloud Sync provisioning agent and gMSA.
* Scoped Cloud Sync by distinguished name and verified a synchronized user.
* Investigated Connect Health telemetry through services, scheduler, connectivity, and audit-log checks.

## Evidence Walkthrough

### Directory readiness and IDFix remediation

I created a controlled UPN formatting issue, used IDFix to identify and correct it, and verified the updated value in Active Directory Users and Computers.

![IDFix detected a userPrincipalName error](../screenshots/11-hybrid-identity-synchronization/01-directory-readiness-idfix/02-idfix-directory-error-detected.png)

![IDFix correction staged](../screenshots/11-hybrid-identity-synchronization/01-directory-readiness-idfix/04-idfix-correction-staged.png)

![IDFix remediation complete](../screenshots/11-hybrid-identity-synchronization/01-directory-readiness-idfix/05-idfix-remediation-complete.png)

![Corrected UPN verified in Active Directory](../screenshots/11-hybrid-identity-synchronization/01-directory-readiness-idfix/06-ad-user-upn-correction-verified.png)

### Connect Sync scope preparation

The `Entra Connect Sync` OU contained the fictional users and security group used for the controlled synchronization scope.

![Users prepared in the synchronization OU](../screenshots/11-hybrid-identity-synchronization/01-directory-readiness-idfix/09-sync-scope-users-created.png)

![Users and group verified in the synchronization OU](../screenshots/11-hybrid-identity-synchronization/01-directory-readiness-idfix/11-sync-scope-users-and-group-verified.png)

### Microsoft Entra Connect Sync configuration

I used the custom setup path, selected Password Hash Synchronization and Seamless SSO, corrected the AD credential format, connected the forest, limited synchronization to the prepared OU, reviewed matching settings, selected the required features, and completed the configuration.

![Password Hash Synchronization and Seamless SSO selected](../screenshots/11-hybrid-identity-synchronization/02-entra-connect-sync/05-password-hash-sync-and-seamless-sso-selected.png)

![Initial directory credential error](../screenshots/11-hybrid-identity-synchronization/02-entra-connect-sync/07-directory-credential-error-detected.png)

![Active Directory forest connection confirmed](../screenshots/11-hybrid-identity-synchronization/02-entra-connect-sync/08-ad-forest-connection-confirmed.png)

![OU filter limited to the prepared synchronization scope](../screenshots/11-hybrid-identity-synchronization/02-entra-connect-sync/09-ou-filter-limited-to-sync-scope.png)

![Synchronization and writeback options selected](../screenshots/11-hybrid-identity-synchronization/02-entra-connect-sync/13-sync-writeback-features-selected.png)

![Connect Sync configuration reviewed before execution](../screenshots/11-hybrid-identity-synchronization/02-entra-connect-sync/16-connect-sync-configuration-review.png)

![Connect Sync configuration completed](../screenshots/11-hybrid-identity-synchronization/02-entra-connect-sync/17-connect-sync-configuration-complete.png)

### Connect Sync verification

I compared the on-premises and Microsoft Entra identity details and confirmed that Connect Sync and Password Hash Sync were enabled.

![Synchronized user and attributes compared across AD DS and Entra](../screenshots/11-hybrid-identity-synchronization/02-entra-connect-sync/19-synced-user-phil-walker-verified.png)

![Connect Sync and Password Hash Sync status](../screenshots/11-hybrid-identity-synchronization/02-entra-connect-sync/21-connect-sync-status-and-password-hash-sync-enabled.png)

### Cloud Sync infrastructure

I deployed the Azure Windows Server virtual machine, installed AD DS and DNS, created the `narindersharmalabs.org` forest, and prepared the Cloud Sync OU and fictional users.

![Azure virtual machine basics](../screenshots/11-hybrid-identity-synchronization/03-cloud-sync-infrastructure/01-azure-virtual-machine-basics-configured.png)

![Azure virtual machine validation passed](../screenshots/11-hybrid-identity-synchronization/03-cloud-sync-infrastructure/04-azure-vm-validation-passed.png)

![Azure virtual machine deployment completed](../screenshots/11-hybrid-identity-synchronization/03-cloud-sync-infrastructure/05-azure-vm-deployment-complete.png)

![New Active Directory forest selected](../screenshots/11-hybrid-identity-synchronization/03-cloud-sync-infrastructure/08-new-ad-forest-deployment-selected.png)

![AD DS prerequisite checks passed](../screenshots/11-hybrid-identity-synchronization/03-cloud-sync-infrastructure/09-ad-ds-prerequisites-passed.png)

![AD DS and DNS roles installed](../screenshots/11-hybrid-identity-synchronization/03-cloud-sync-infrastructure/10-ad-ds-and-dns-roles-installed.png)

![Cloud server domain verified](../screenshots/11-hybrid-identity-synchronization/03-cloud-sync-infrastructure/11-cloud-server-domain-verified.png)

![Cloud Sync OU and fictional users created](../screenshots/11-hybrid-identity-synchronization/03-cloud-sync-infrastructure/12-cloud-sync-ou-and-users-created.png)

### Cloud Sync provisioning agent and configuration

I connected the Active Directory domain, registered the provisioning agent, selected Password Hash Synchronization, collected the OU distinguished name, applied the scoping filter, and enabled the configuration.

![Provisioning agent set to connect Active Directory](../screenshots/11-hybrid-identity-synchronization/04-cloud-sync-configuration/02-provisioning-agent-ad-domain-option.png)

![Active Directory domain connected to the provisioning agent](../screenshots/11-hybrid-identity-synchronization/04-cloud-sync-configuration/03-provisioning-agent-active-directory-connected.png)

![Provisioning agent configuration complete](../screenshots/11-hybrid-identity-synchronization/04-cloud-sync-configuration/05-provisioning-agent-configuration-complete.png)

![Cloud Sync domain and Password Hash Sync selected](../screenshots/11-hybrid-identity-synchronization/04-cloud-sync-configuration/07-cloud-sync-domain-and-password-hash-sync.png)

![OU distinguished name collected from Active Directory](../screenshots/11-hybrid-identity-synchronization/04-cloud-sync-configuration/09-sync-scope-distinguished-name-collected.png)

![OU scoping filter saved](../screenshots/11-hybrid-identity-synchronization/04-cloud-sync-configuration/11-organizational-unit-scope-filter-saved.png)

![Cloud Sync configuration reviewed before enablement](../screenshots/11-hybrid-identity-synchronization/04-cloud-sync-configuration/12-cloud-sync-review-and-enable.png)

### Cloud Sync verification

The configuration showed healthy and enabled with an active agent, and a user from the scoped OU appeared in Microsoft Entra with on-premises synchronization enabled.

![Cloud Sync configuration healthy and enabled](../screenshots/11-hybrid-identity-synchronization/04-cloud-sync-configuration/13-cloud-sync-configuration-healthy.png)

![Cloud-synchronized user verified in Microsoft Entra](../screenshots/11-hybrid-identity-synchronization/04-cloud-sync-configuration/14-cloud-synced-user-verified-in-entra.png)

### Connect Health investigation

Connect Health showed zero object-level sync errors and later reported stale health data for `NYC-DC1`. I checked the alert details, confirmed the sync and health services, reviewed the scheduler, tested Microsoft endpoint connectivity, and confirmed a successful Event Hub diagnostic upload. The separate Cloud Sync configuration and audit log remained healthy during the review.

![Connect Health sync errors at zero](../screenshots/11-hybrid-identity-synchronization/05-connect-health-troubleshooting/02-connect-health-sync-errors-zero.png)

![Stale health data alert history](../screenshots/11-hybrid-identity-synchronization/05-connect-health-troubleshooting/05-stale-health-data-alert-history.png)

![Stale health data alert details](../screenshots/11-hybrid-identity-synchronization/05-connect-health-troubleshooting/06-stale-health-data-alert-details.png)

![Sync services, scheduler, and health connectivity verified](../screenshots/11-hybrid-identity-synchronization/05-connect-health-troubleshooting/08-sync-services-scheduler-and-connectivity-verified.png)

![Sync and health services running](../screenshots/11-hybrid-identity-synchronization/05-connect-health-troubleshooting/09-sync-services-running-in-task-manager.png)

![Cloud Sync remained healthy during the investigation](../screenshots/11-hybrid-identity-synchronization/05-connect-health-troubleshooting/10-cloud-sync-configuration-remained-healthy.png)

![Cloud Sync audit log showed a successful synchronization event](../screenshots/11-hybrid-identity-synchronization/05-connect-health-troubleshooting/11-cloud-sync-audit-log-success.png)

## Troubleshooting Record

| Issue | Checks completed | Result |
|---|---|---|
| Connect Sync could not validate the first AD forest credentials | Confirmed the AD DNS root and NetBIOS name, then used the correct domain account format | The forest connection completed and the installer continued to OU filtering |
| Connect Health reported stale service data | Checked services, scheduler status, Microsoft endpoint connectivity, Event Hub upload, Cloud Sync health, and audit logs | The local services and outbound health connectivity tested successfully while the portal alert remained available for follow-up |
| Connect Sync and Cloud Sync used separate forests | Reviewed each forest, agent, configuration, synchronized user, and health surface separately | Each synchronization method was documented as its own workflow |

## Skills Demonstrated

* IDFix directory readiness and UPN remediation
* Windows Server AD DS and DNS deployment
* Active Directory OU, user, group, and attribute preparation
* Microsoft Entra Connect Sync custom installation
* Microsoft Entra Cloud Sync provisioning-agent installation
* Password Hash Synchronization
* OU and distinguished-name synchronization scoping
* Cross-directory identity verification
* Microsoft Entra Connect Health review
* PowerShell service, scheduler, and connectivity checks
* Cloud Sync audit-log review

## Support Relevance

Hybrid identity support can involve missing users, incorrect attributes, OU scoping, agent health, password synchronization, or stale monitoring data. This workflow shows the checks used across AD DS, the synchronization servers, Microsoft Entra, Connect Health, and provisioning audit logs.

## Outcome

Microsoft Entra Connect Sync and Microsoft Entra Cloud Sync were configured and verified in separate lab forests. The health investigation confirmed running services, an enabled scheduler, successful endpoint connectivity, and a successful Cloud Sync audit event.
