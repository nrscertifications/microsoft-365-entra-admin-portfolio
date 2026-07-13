# Hybrid Identity Synchronization & Health Monitoring

## Administrative Objective

Build and verify hybrid identity synchronization between Windows Server Active Directory Domain Services and Microsoft Entra ID using both Microsoft Entra Connect Sync and Microsoft Entra Cloud Sync.

The work used two separate lab forests so each synchronization method could be configured and reviewed independently:

| Server | Hosting | Active Directory forest | Synchronization method |
|---|---|---|---|
| `NYC-DC1` | Hyper-V | `ad.narindersharmalabs.xyz` | Microsoft Entra Connect Sync |
| `NYC-DC-CLOUD-SYNC` | Azure virtual machine | `narindersharmalabs.org` | Microsoft Entra Cloud Sync provisioning agent |

The two forests are separate environments. RDP and Hyper-V were only management paths to the servers; they were not synchronization targets.

---

## Work Completed

* Created a controlled UPN formatting issue in a fictional AD DS account and used IDFix to detect, correct, and verify the attribute.
* Prepared an OU, fictional users, a security group, and user attributes for a limited Connect Sync scope.
* Installed Microsoft Entra Connect Sync with custom settings and connected the `ad.narindersharmalabs.xyz` forest.
* Limited synchronization to the `Entra Connect Sync` OU.
* Selected Password Hash Synchronization, Seamless Single Sign-On, password writeback, and group writeback options during configuration.
* Verified synchronized users and Connect Sync status in Microsoft Entra.
* Deployed an Azure Windows Server virtual machine and promoted it as a domain controller for `narindersharmalabs.org`.
* Installed and registered the Microsoft Entra Cloud Sync provisioning agent.
* Scoped Cloud Sync to the `Entra Cloud Sync` OU by using its distinguished name.
* Enabled the Cloud Sync configuration and verified a synchronized user in Microsoft Entra.
* Reviewed Connect Health, sync error views, service state, scheduler state, connectivity, and Cloud Sync audit logs.
* Investigated a stale-health-data alert without presenting the still-active portal alert as resolved.

---

## Evidence Walkthrough

### 1. Cleaned a directory attribute before synchronization

I created a controlled UPN issue in a fictional account so the directory-readiness workflow included a real correction rather than only a clean-state review. IDFix detected the `userPrincipalName` character error. I staged the corrected value, applied the edit, and confirmed that the remediation completed. I then confirmed the corrected UPN in Active Directory Users and Computers.

![IDFix detected a userPrincipalName error](../screenshots/11-hybrid-identity-synchronization/01-directory-readiness-idfix/02-idfix-directory-error-detected.png)

![IDFix correction staged](../screenshots/11-hybrid-identity-synchronization/01-directory-readiness-idfix/04-idfix-correction-staged.png)

![IDFix remediation complete](../screenshots/11-hybrid-identity-synchronization/01-directory-readiness-idfix/05-idfix-remediation-complete.png)

![Corrected UPN verified in Active Directory](../screenshots/11-hybrid-identity-synchronization/01-directory-readiness-idfix/06-ad-user-upn-correction-verified.png)

### 2. Prepared a controlled Connect Sync scope

The `Entra Connect Sync` OU was used to isolate the objects intended for the synchronization workflow. I created fictional users, added meaningful account attributes, and created a security group before starting the connector installation.

![Users prepared in the synchronization OU](../screenshots/11-hybrid-identity-synchronization/01-directory-readiness-idfix/09-sync-scope-users-created.png)

![Users and group verified in the synchronization OU](../screenshots/11-hybrid-identity-synchronization/01-directory-readiness-idfix/11-sync-scope-users-and-group-verified.png)

### 3. Configured Microsoft Entra Connect Sync

I used the custom installation path so the sign-in method, forest connection, OU filtering, and optional features could be reviewed directly. Password Hash Synchronization and Seamless SSO were selected, and the `ad.narindersharmalabs.xyz` forest was added after correcting the domain credential format that caused the first connection error.

![Password Hash Synchronization and Seamless SSO selected](../screenshots/11-hybrid-identity-synchronization/02-entra-connect-sync/05-password-hash-sync-and-seamless-sso-selected.png)

![Initial directory credential error](../screenshots/11-hybrid-identity-synchronization/02-entra-connect-sync/07-directory-credential-error-detected.png)

![Active Directory forest connection confirmed](../screenshots/11-hybrid-identity-synchronization/02-entra-connect-sync/08-ad-forest-connection-confirmed.png)

The scope was limited to the prepared OU rather than synchronizing the full directory. I reviewed the user matching and source-anchor defaults, then selected password hash synchronization, password writeback, and group writeback options. The screenshots prove those options were selected during setup; they are not presented as separate end-to-end writeback tests.

![OU filter limited to the prepared synchronization scope](../screenshots/11-hybrid-identity-synchronization/02-entra-connect-sync/09-ou-filter-limited-to-sync-scope.png)

![Synchronization and writeback options selected](../screenshots/11-hybrid-identity-synchronization/02-entra-connect-sync/13-sync-writeback-features-selected.png)

![Connect Sync configuration reviewed before execution](../screenshots/11-hybrid-identity-synchronization/02-entra-connect-sync/16-connect-sync-configuration-review.png)

![Connect Sync configuration completed](../screenshots/11-hybrid-identity-synchronization/02-entra-connect-sync/17-connect-sync-configuration-complete.png)

The completion screen also displayed follow-up warnings, including the Active Directory Recycle Bin recommendation and Seamless SSO Group Policy follow-up. Those items were retained in the evidence instead of being hidden or described as completed work.

### 4. Verified Connect Sync results

I compared an on-premises user and its Microsoft Entra representation, then checked the Connect Sync status page. The portal showed synchronization enabled, a recent synchronization time, and Password Hash Sync enabled.

![Synchronized user and attributes compared across AD DS and Entra](../screenshots/11-hybrid-identity-synchronization/02-entra-connect-sync/19-synced-user-phil-walker-verified.png)

![Connect Sync and Password Hash Sync status](../screenshots/11-hybrid-identity-synchronization/02-entra-connect-sync/21-connect-sync-status-and-password-hash-sync-enabled.png)

### 5. Built the separate Cloud Sync directory environment

For the Cloud Sync path, I created an Azure Windows Server 2022 virtual machine, reviewed its deployment settings, and completed Azure validation before deployment.

![Azure virtual machine basics](../screenshots/11-hybrid-identity-synchronization/03-cloud-sync-infrastructure/01-azure-virtual-machine-basics-configured.png)

![Azure virtual machine validation passed](../screenshots/11-hybrid-identity-synchronization/03-cloud-sync-infrastructure/04-azure-vm-validation-passed.png)

![Azure virtual machine deployment completed](../screenshots/11-hybrid-identity-synchronization/03-cloud-sync-infrastructure/05-azure-vm-deployment-complete.png)

I installed AD DS and DNS, configured the new `narindersharmalabs.org` forest, and confirmed the prerequisite check before promotion. After restart, Server Manager showed the AD DS and DNS roles, the server properties showed the new domain, and Active Directory Users and Computers showed the Cloud Sync OU with two fictional users.

![New Active Directory forest selected](../screenshots/11-hybrid-identity-synchronization/03-cloud-sync-infrastructure/08-new-ad-forest-deployment-selected.png)

![AD DS prerequisite checks passed](../screenshots/11-hybrid-identity-synchronization/03-cloud-sync-infrastructure/09-ad-ds-prerequisites-passed.png)

![AD DS and DNS roles installed](../screenshots/11-hybrid-identity-synchronization/03-cloud-sync-infrastructure/10-ad-ds-and-dns-roles-installed.png)

![Cloud server domain verified](../screenshots/11-hybrid-identity-synchronization/03-cloud-sync-infrastructure/11-cloud-server-domain-verified.png)

![Cloud Sync OU and fictional users created](../screenshots/11-hybrid-identity-synchronization/03-cloud-sync-infrastructure/12-cloud-sync-ou-and-users-created.png)

### 6. Installed and registered the Cloud Sync provisioning agent

I downloaded the provisioning agent, selected the Active Directory domain option, connected `narindersharmalabs.org`, and registered the agent with Microsoft Entra. The configuration summary showed the generated gMSA and the lab tenant account used for registration.

![Provisioning agent set to connect Active Directory](../screenshots/11-hybrid-identity-synchronization/04-cloud-sync-configuration/02-provisioning-agent-ad-domain-option.png)

![Active Directory domain connected to the provisioning agent](../screenshots/11-hybrid-identity-synchronization/04-cloud-sync-configuration/03-provisioning-agent-active-directory-connected.png)

![Provisioning agent configuration complete](../screenshots/11-hybrid-identity-synchronization/04-cloud-sync-configuration/05-provisioning-agent-configuration-complete.png)

### 7. Scoped and enabled Cloud Sync

The new configuration selected the `narindersharmalabs.org` domain and enabled Password Hash Synchronization. I collected the `Entra Cloud Sync` OU distinguished name from ADUC Attribute Editor and used it as the selected-OU scoping filter in Microsoft Entra.

![Cloud Sync domain and Password Hash Sync selected](../screenshots/11-hybrid-identity-synchronization/04-cloud-sync-configuration/07-cloud-sync-domain-and-password-hash-sync.png)

![OU distinguished name collected from Active Directory](../screenshots/11-hybrid-identity-synchronization/04-cloud-sync-configuration/09-sync-scope-distinguished-name-collected.png)

![OU scoping filter saved](../screenshots/11-hybrid-identity-synchronization/04-cloud-sync-configuration/11-organizational-unit-scope-filter-saved.png)

![Cloud Sync configuration reviewed before enablement](../screenshots/11-hybrid-identity-synchronization/04-cloud-sync-configuration/12-cloud-sync-review-and-enable.png)

After enablement, the configuration showed `Healthy`, `Enabled`, and one active agent. A fictional user from the selected OU then appeared in Microsoft Entra with on-premises synchronization enabled.

![Cloud Sync configuration healthy and enabled](../screenshots/11-hybrid-identity-synchronization/04-cloud-sync-configuration/13-cloud-sync-configuration-healthy.png)

![Cloud-synchronized user verified in Microsoft Entra](../screenshots/11-hybrid-identity-synchronization/04-cloud-sync-configuration/14-cloud-synced-user-verified-in-entra.png)

### 8. Reviewed synchronization health and investigated stale telemetry

Connect Health initially showed zero object-level sync errors. A later service-health view showed an active `Health service data is not up to date` error for `NYC-DC1`, while the last export remained successful and the sync error count remained at zero. I treated this as a telemetry problem to investigate rather than assuming directory synchronization had failed.

![Connect Health sync errors at zero](../screenshots/11-hybrid-identity-synchronization/05-connect-health-troubleshooting/02-connect-health-sync-errors-zero.png)

![Stale health data alert history](../screenshots/11-hybrid-identity-synchronization/05-connect-health-troubleshooting/05-stale-health-data-alert-history.png)

![Stale health data alert details](../screenshots/11-hybrid-identity-synchronization/05-connect-health-troubleshooting/06-stale-health-data-alert-details.png)

On `NYC-DC1`, PowerShell confirmed that the Azure AD Sync service, Connect Agent Updater, and Microsoft Entra Connect Health Agent were running. The scheduler was enabled, endpoint tests succeeded, and the Event Hub diagnostic upload completed successfully. Task Manager provided a second service-state check.

![Sync services, scheduler, and health connectivity verified](../screenshots/11-hybrid-identity-synchronization/05-connect-health-troubleshooting/08-sync-services-scheduler-and-connectivity-verified.png)

![Sync and health services running](../screenshots/11-hybrid-identity-synchronization/05-connect-health-troubleshooting/09-sync-services-running-in-task-manager.png)

The separate Cloud Sync configuration remained healthy, and its audit log showed a successful synchronization event. The Connect Health alert was still active when captured, so this section documents the checks completed and does not claim that the portal had already marked the alert resolved.

![Cloud Sync remained healthy during the investigation](../screenshots/11-hybrid-identity-synchronization/05-connect-health-troubleshooting/10-cloud-sync-configuration-remained-healthy.png)

![Cloud Sync audit log showed a successful synchronization event](../screenshots/11-hybrid-identity-synchronization/05-connect-health-troubleshooting/11-cloud-sync-audit-log-success.png)

---

## Troubleshooting Record

| Issue | Checks performed | Evidence-based result |
|---|---|---|
| Connect Sync could not validate the first AD forest credentials | Confirmed the actual AD DNS root and NetBIOS name, then used the correct domain account format | The forest was added and the installer moved to OU filtering |
| Connect Health reported stale service data | Checked Connect Sync and health services, scheduler status, Microsoft endpoint connectivity, and Event Hub upload | Local services and outbound health connectivity tested successfully; portal alert was still active in the captured evidence |
| Need to separate Connect Sync and Cloud Sync results | Reviewed each forest, agent, configuration, user result, and health surface independently | Connect Sync and Cloud Sync were documented as separate synchronization paths rather than one combined environment |

---

## Skills Demonstrated

* IDFix directory readiness and UPN remediation
* Windows Server AD DS and DNS deployment
* Active Directory OU, user, group, and attribute preparation
* Microsoft Entra Connect Sync custom installation
* Microsoft Entra Cloud Sync provisioning-agent installation
* Password Hash Synchronization configuration
* OU and distinguished-name synchronization scoping
* Cross-directory user verification
* Microsoft Entra Connect Health review
* PowerShell service, scheduler, and connectivity checks
* Cloud Sync audit-log review
* Evidence-based troubleshooting and technical documentation

---

## Support Relevance

Hybrid identity incidents often look like ordinary account problems: a user is missing from Microsoft 365, a password change has not appeared in the cloud, an attribute is malformed, a synchronization scope excludes an OU, or a health alert suggests that monitoring data is stale. This work shows where those issues are checked across AD DS, the synchronization server, Microsoft Entra, Connect Health, and provisioning audit logs.

The scope is appropriate for IT support and junior administration work. It demonstrates the ability to follow a controlled setup, recognize an error, check the supporting services, and document the boundary between what was verified and what still required time or follow-up.

---

## Outcome

Two separate hybrid identity synchronization methods were configured in non-production lab forests. Connect Sync synchronized selected AD DS users to Microsoft Entra, and Cloud Sync synchronized a user from a distinguished-name-scoped OU through the provisioning agent. Health checks and troubleshooting confirmed running services, an enabled scheduler, successful outbound health connectivity, and a successful Cloud Sync audit event.

The evidence does not present the environment as a production design, a high-availability deployment, or a fully resolved Connect Health incident. It documents the configuration and verification that were actually completed.

