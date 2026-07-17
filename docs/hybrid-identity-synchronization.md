# Hybrid Identity Synchronization & Health Monitoring

This work uses two separate Active Directory lab forests to document Microsoft Entra Connect Sync and Microsoft Entra Cloud Sync.

## Lab Layout

| Server | Hosting | Active Directory forest | Synchronization method |
|---|---|---|---|
| `NYC-DC1` | Hyper-V | `ad.narindersharmalabs.xyz` | Microsoft Entra Connect Sync |
| `NYC-DC-CLOUD-SY` | Azure virtual machine | `narindersharmalabs.org` | Microsoft Entra Cloud Sync provisioning agent |

## Work Completed

- Used IDFix to detect and correct a UPN formatting issue.
- Prepared OUs, users, a group, and account attributes for synchronization.
- Configured Microsoft Entra Connect Sync with Password Hash Synchronization and limited OU scope.
- Verified synchronized identities and Connect Sync status.
- Deployed a separate Azure Windows Server domain controller for Cloud Sync.
- Installed and registered the Cloud Sync provisioning agent.
- Scoped Cloud Sync by distinguished name and verified a synchronized user.
- Investigated Connect Health telemetry through service, scheduler, connectivity, and audit-log checks.

## Phase 1 — Directory Readiness and IDFix

I used IDFix to locate and correct a controlled UPN formatting issue, then verified the updated value in Active Directory Users and Computers.

<p align="center">
  <a href="../screenshots/11-hybrid-identity-synchronization/01-directory-readiness-idfix/02-idfix-directory-error-detected.png"><img src="../screenshots/11-hybrid-identity-synchronization/01-directory-readiness-idfix/02-idfix-directory-error-detected.png" alt="IDFix error detected" width="49%"></a>
  <a href="../screenshots/11-hybrid-identity-synchronization/01-directory-readiness-idfix/06-ad-user-upn-correction-verified.png"><img src="../screenshots/11-hybrid-identity-synchronization/01-directory-readiness-idfix/06-ad-user-upn-correction-verified.png" alt="UPN verified in Active Directory" width="49%"></a>
</p>

_Left: IDFix identified the invalid userPrincipalName value. Right: The corrected UPN verified in Active Directory Users and Computers._

## Phase 2 — Connect Sync Configuration

I selected Password Hash Synchronization and Seamless SSO, corrected the forest credential format, limited synchronization to the prepared OU, and completed the Connect Sync configuration.

<p align="center">
  <a href="../screenshots/11-hybrid-identity-synchronization/02-entra-connect-sync/09-ou-filter-limited-to-sync-scope.png"><img src="../screenshots/11-hybrid-identity-synchronization/02-entra-connect-sync/09-ou-filter-limited-to-sync-scope.png" alt="Connect Sync OU filter" width="49%"></a>
  <a href="../screenshots/11-hybrid-identity-synchronization/02-entra-connect-sync/17-connect-sync-configuration-complete.png"><img src="../screenshots/11-hybrid-identity-synchronization/02-entra-connect-sync/17-connect-sync-configuration-complete.png" alt="Connect Sync complete" width="49%"></a>
</p>

_Left: Synchronization limited to the prepared OU. Right: The Microsoft Entra Connect Sync configuration completed._

## Phase 3 — Connect Sync Verification

I compared a synchronized identity with its on-premises account and confirmed Connect Sync and Password Hash Sync status in Microsoft Entra.

<p align="center">
  <a href="../screenshots/11-hybrid-identity-synchronization/02-entra-connect-sync/19-synced-user-phil-walker-verified.png"><img src="../screenshots/11-hybrid-identity-synchronization/02-entra-connect-sync/19-synced-user-phil-walker-verified.png" alt="Synchronized user verified" width="49%"></a>
  <a href="../screenshots/11-hybrid-identity-synchronization/02-entra-connect-sync/21-connect-sync-status-and-password-hash-sync-enabled.png"><img src="../screenshots/11-hybrid-identity-synchronization/02-entra-connect-sync/21-connect-sync-status-and-password-hash-sync-enabled.png" alt="Connect Sync status" width="49%"></a>
</p>

_Left: The on-premises and Entra identity values reviewed together. Right: Microsoft Entra Connect Sync and Password Hash Sync shown as enabled._

## Phase 4 — Cloud Sync Infrastructure

I deployed the Azure Windows Server virtual machine, installed AD DS and DNS, created the separate forest, and prepared the Cloud Sync OU and lab users.

<p align="center">
  <a href="../screenshots/11-hybrid-identity-synchronization/03-cloud-sync-infrastructure/05-azure-vm-deployment-complete.png"><img src="../screenshots/11-hybrid-identity-synchronization/03-cloud-sync-infrastructure/05-azure-vm-deployment-complete.png" alt="Azure VM deployed" width="49%"></a>
  <a href="../screenshots/11-hybrid-identity-synchronization/03-cloud-sync-infrastructure/12-cloud-sync-ou-and-users-created.png"><img src="../screenshots/11-hybrid-identity-synchronization/03-cloud-sync-infrastructure/12-cloud-sync-ou-and-users-created.png" alt="Cloud Sync OU prepared" width="49%"></a>
</p>

_Left: The Azure Windows Server virtual machine deployment completed. Right: The Cloud Sync OU and lab users created in Active Directory._

## Phase 5 — Cloud Sync Agent and Configuration

I installed and registered the provisioning agent, selected Password Hash Synchronization, saved the OU distinguished-name scope, and enabled the configuration.

<p align="center">
  <a href="../screenshots/11-hybrid-identity-synchronization/04-cloud-sync-configuration/05-provisioning-agent-configuration-complete.png"><img src="../screenshots/11-hybrid-identity-synchronization/04-cloud-sync-configuration/05-provisioning-agent-configuration-complete.png" alt="Provisioning agent complete" width="49%"></a>
  <a href="../screenshots/11-hybrid-identity-synchronization/04-cloud-sync-configuration/11-organizational-unit-scope-filter-saved.png"><img src="../screenshots/11-hybrid-identity-synchronization/04-cloud-sync-configuration/11-organizational-unit-scope-filter-saved.png" alt="Cloud Sync OU scope saved" width="49%"></a>
</p>

_Left: The provisioning agent installation and registration completed. Right: The distinguished-name scope filter saved for the Cloud Sync OU._
<p align="center">
  <a href="../screenshots/11-hybrid-identity-synchronization/04-cloud-sync-configuration/13-cloud-sync-configuration-healthy.png"><img src="../screenshots/11-hybrid-identity-synchronization/04-cloud-sync-configuration/13-cloud-sync-configuration-healthy.png" alt="Cloud Sync healthy" width="78%"></a>
</p>

_The enabled Cloud Sync configuration with a healthy agent._

## Phase 6 — Cloud Sync Identity Verification

I confirmed that a user from the scoped OU appeared in Microsoft Entra with on-premises synchronization enabled.

<p align="center">
  <a href="../screenshots/11-hybrid-identity-synchronization/04-cloud-sync-configuration/14-cloud-synced-user-verified-in-entra.png"><img src="../screenshots/11-hybrid-identity-synchronization/04-cloud-sync-configuration/14-cloud-synced-user-verified-in-entra.png" alt="Cloud-synchronized user verified" width="78%"></a>
</p>

_The Cloud Sync user shown in Microsoft Entra with on-premises synchronization enabled._

## Phase 7 — Connect Health Investigation

Connect Health reported stale service data for `NYC-DC1`. I reviewed the alert, checked the synchronization and health services, confirmed the scheduler and Microsoft endpoint connectivity, and reviewed the Cloud Sync audit log during the investigation.

<p align="center">
  <a href="../screenshots/11-hybrid-identity-synchronization/05-connect-health-troubleshooting/06-stale-health-data-alert-details.png"><img src="../screenshots/11-hybrid-identity-synchronization/05-connect-health-troubleshooting/06-stale-health-data-alert-details.png" alt="Stale health data alert" width="49%"></a>
  <a href="../screenshots/11-hybrid-identity-synchronization/05-connect-health-troubleshooting/08-sync-services-scheduler-and-connectivity-verified.png"><img src="../screenshots/11-hybrid-identity-synchronization/05-connect-health-troubleshooting/08-sync-services-scheduler-and-connectivity-verified.png" alt="Connect Health checks" width="49%"></a>
</p>

_Left: The Connect Health stale-data alert details for NYC-DC1. Right: Services, scheduler status, endpoint connectivity, and diagnostic upload checks._
<p align="center">
  <a href="../screenshots/11-hybrid-identity-synchronization/05-connect-health-troubleshooting/11-cloud-sync-audit-log-success.png"><img src="../screenshots/11-hybrid-identity-synchronization/05-connect-health-troubleshooting/11-cloud-sync-audit-log-success.png" alt="Cloud Sync audit success" width="78%"></a>
</p>

_A successful Cloud Sync provisioning event in the audit log._

## Troubleshooting Record

| Issue | Checks completed | Result |
|---|---|---|
| Connect Sync rejected the first forest credentials | Confirmed the AD DNS root and NetBIOS name, then corrected the domain-account format | The forest connected and the installer continued to OU filtering |
| Connect Health displayed stale service data | Checked services, scheduler status, Microsoft endpoint connectivity, diagnostic upload, Cloud Sync health, and audit logs | Local services and outbound checks completed successfully while the portal alert remained visible |

## Skills Demonstrated

- IDFix UPN detection and remediation
- Windows Server AD DS and DNS deployment
- Microsoft Entra Connect Sync and Microsoft Entra Cloud Sync
- Password Hash Synchronization
- OU and distinguished-name scoping
- Synchronized identity verification
- Microsoft Entra Connect Health review
- PowerShell service, scheduler, and connectivity checks
- Cloud Sync audit-log review

## Result

Microsoft Entra Connect Sync and Microsoft Entra Cloud Sync were configured in separate lab forests, synchronized identities were verified, and Connect Health troubleshooting was documented through portal, service, scheduler, connectivity, and audit-log checks.

The complete screenshot sequence is available in [`screenshots/11-hybrid-identity-synchronization`](../screenshots/11-hybrid-identity-synchronization).
