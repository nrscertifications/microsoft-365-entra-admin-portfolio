# Microsoft 365 & Entra ID Administration Portfolio

## Project Overview

This repository documents hands-on Microsoft 365, Microsoft Entra ID, Windows Server AD DS, and hybrid identity administration in a dedicated non-production environment. The work covers tenant and domain readiness, identity administration, external collaboration, group management, licensing and service access, operational visibility, Microsoft 365 Backup readiness, Microsoft Graph PowerShell, delegated administration, directory synchronization, and identity health monitoring.

I configured the work in a dedicated non-production Microsoft 365 tenant using fictional users, test contacts, sample guest users, and lab-only objects. The repository is organized by administrative workflow, so the evidence can be reviewed as a practical IT Support, Service Desk, Technical Support, or junior systems administration portfolio.

The project connects work across the Microsoft 365 admin center, Microsoft Entra admin center, Azure portal, Windows Server Active Directory Domain Services, Microsoft Graph PowerShell, Microsoft Entra Connect Sync, Microsoft Entra Cloud Sync, and workload-specific admin centers. The documentation shows what was configured, what was verified, and where a result remained a review or troubleshooting step rather than being presented as completed production work.

> **Data and lab context note:** Screenshots use fictional users, test objects, and sample external collaboration targets created only for this Microsoft 365 / Entra ID environment. User names and lab email addresses remain visible when they help verify the workflow. Temporary passwords, public IP information, and values that could expose access were removed or cropped before publishing. No production customer data, private user records, or live business information are included.

---

## Core Technical Skills & Tools

* **Microsoft 365 Administration:** Tenant navigation, active user management, contacts, groups, licensing, service health, service access review, backup policy readiness, and admin center workflow validation.
* **Tenant & Domain Readiness:** Tenant overview validation, custom domain workflow review, primary domain awareness, and admin portal navigation.
* **Microsoft Entra ID:** Member users, guest users, external collaboration, group objects, identity properties, administrative roles, administrative units, scoped delegation, synchronized identities, and portal validation.
* **Hybrid Identity:** IDFix directory cleanup, Microsoft Entra Connect Sync, Microsoft Entra Cloud Sync, Password Hash Synchronization, OU and distinguished-name scoping, sync verification, and Connect Health troubleshooting.
* **Windows Server & Active Directory:** AD DS and DNS role installation, forest promotion, OU and user preparation, directory attribute review, and domain-controller validation.
* **Azure Portal:** Virtual machine deployment, resource configuration, tenant and directory administration, and Log Analytics workspace exposure.
* **Microsoft Graph PowerShell:** Module installation, delegated authentication, Graph scopes, user retrieval, test user creation, group creation, subscribed SKU review, license assignment, CSV-based bulk provisioning, and cleanup validation.
* **User Lifecycle Administration:** Manual provisioning, bulk provisioning, profile properties, account state validation, license review, and cross-portal verification.
* **External Collaboration:** B2B guest invitation workflow, external contacts, address book visibility concepts, and Outlook web access validation.
* **Group Administration:** Microsoft 365 group creation, owners, members, group properties, Entra group validation, and dynamic membership exposure.
* **Role-Based Access & Delegated Administration:** Microsoft Entra role assignment, Microsoft 365 admin role management, administrative units, scoped User Administrator delegation, Purview role groups, Defender/Purview permission surfaces, and PIM-style eligible assignment workflows.
* **Operational Readiness:** Service health, network insights, software update visibility, Connect Health, Log Analytics exposure, and Microsoft 365 Backup policy readiness for Exchange, OneDrive, and SharePoint.
* **Documentation & Version Control:** Markdown documentation, screenshot-to-claim mapping, Git/GitHub portfolio structure, and evidence-based technical writing.

---

## Functional Architecture & Evidence

### 1. Tenant Foundation & Domain Readiness

I established the tenant foundation used for the rest of the administrative work. This included tenant overview validation, admin portal navigation, custom domain workflow review, and resource-backed service visibility through Azure.

This provided the base layer for user identities, email addressing, licensing, collaboration, service health, backup readiness, and administrative workflow validation.

![Tenant creation confirmation](screenshots/01-tenant-foundation/03-tenant-create-successful-04.png)

![Custom domain verification](screenshots/02-domain-readiness/03-custom-domain-azure03-verified.png)

### 2. Identity & User Lifecycle Administration

I created internal member users from multiple admin portals and validated that the same user objects appeared across Microsoft 365 admin center, Azure portal, and Microsoft Entra admin center.

This helped confirm the difference between the portal used to complete an admin task and the underlying identity object stored in Microsoft Entra ID.

![Microsoft 365 admin user creation](screenshots/03-user-provisioning/19-m365-admin-user-create-01.png)

![User visible in Entra users list](screenshots/03-user-provisioning/15-m365-admin-user-create-azure-portal-confirmation-07.png)

### 3. Bulk User Provisioning

I completed the bulk user creation workflow, including CSV-based account creation, generated results validation, and post-creation verification in the active users list.

This workflow is relevant to onboarding scenarios where multiple accounts need to be created consistently before licenses, groups, and access are finalized.

![Bulk user provisioning workflow](screenshots/03-user-provisioning/01-bulk-user-provisioning-01.png)

![Bulk user provisioning completed with temporary passwords redacted](screenshots/03-user-provisioning/13-bulk-user-provisioning-completed-redacted-passwords.png)

### 4. External Collaboration & Address Book Management

I created external contacts for address book visibility and completed the guest invitation workflow through Microsoft Entra B2B collaboration.

This workflow separates two common support scenarios: external contacts used for discoverability and communication, and guest users that become tenant-visible collaboration identities after invitation.

![External contact creation](screenshots/04-external-collaboration-contacts/02-external-contact-create-01.png)

![External guest invitation workflow](screenshots/04-external-collaboration-contacts/07-external-guest-invitation-04.png)

### 5. Group-Based Collaboration Management

I created, configured, and validated Microsoft 365 group settings, including group properties, owners, members, and Entra-side object validation.

This demonstrates how group objects support collaboration, membership management, and access-related administration in Microsoft 365 environments.

![Microsoft 365 group creation](screenshots/05-group-collaboration/01-groups-m365-group-create-01.png)

![Group owners validation](screenshots/05-group-collaboration/10-groups-add-365-group-owners-010.png)

### 6. Licensing & Service Access Review

I reviewed license inventory, user assignment views, and service access settings from the Microsoft 365 admin center.

The focus was administrative validation: checking available products, where license assignments are viewed, how licensing affects service access, and why license state matters during account troubleshooting.

![License inventory review](screenshots/06-licensing-service-access/01-license-inventory-review-01.png)

### 7. Operational Visibility & Backup Readiness

I reviewed Microsoft 365 operational visibility areas used for service desk and administrator triage, including service health, network connectivity insights, software update visibility, and Log Analytics exposure.

I also configured and validated Microsoft 365 Backup policy readiness workflows for Exchange, OneDrive, and SharePoint, including workload-level backup policy screens and backup readiness confirmation.

These workflows support service desk triage by helping separate local device issues from tenant-level service issues, network readiness problems, service access issues, monitoring gaps, or backup-readiness issues.

![Network insights location configuration](screenshots/07-service-health-network-insights/01-network-insights-location-complete.png)

![Backup policy readiness](screenshots/08-operational-resilience-backup/03-all-backup-policies-completed.png)

### 8. PowerShell & Microsoft Graph Administration Track

I built and documented a command-line administration track separately from the portal-based workflows because PowerShell and Microsoft Graph support repeatable provisioning, reporting, validation, licensing, and cleanup tasks.

This track includes Microsoft Graph PowerShell module setup, delegated tenant authentication, user retrieval, test user creation, Microsoft 365 group creation, subscribed SKU review, license assignment, CSV-based bulk user provisioning, and cleanup of test accounts after verification.

![Microsoft Graph sign-in successful](screenshots/09-powershell-admin-tooling/14-graph-sign-in-successful.png)

![Microsoft Graph bulk user import command with temporary password redacted](screenshots/09-powershell-admin-tooling/22-graph-bulk-user-import-command-password-redacted.png)

![Microsoft Graph license review and assignment](screenshots/09-powershell-admin-tooling/20-graph-license-review-assignment.png)

### 9. Role-Based Access & Delegated Administration

I administered role-based access workflows across Microsoft 365 admin center, Microsoft Entra admin center, Defender XDR, Microsoft Purview, administrative units, and Privileged Identity Management concepts in a non-production tenant.

This work covered hands-on role assignment, administrative unit creation, scoped User Administrator delegation, Purview role group workflows, and PIM-style eligible assignment configuration for temporary administrative access.

![Microsoft 365 role assignment completed](screenshots/10-role-based-access-delegation/12-m365-admin-center-role-assignment-complete.png)

![Administrative unit scoped User Administrator assignment](screenshots/10-role-based-access-delegation/25-administrative-unit-scope-check.png)

![PIM eligible assignment confirmation](screenshots/10-role-based-access-delegation/31-pim-eligible-assignment-confirmation.png)

### 10. Hybrid Identity Synchronization & Health Monitoring

I prepared Active Directory objects for synchronization, used IDFix to correct a directory attribute issue, and configured two separate synchronization paths: Microsoft Entra Connect Sync for the `ad.narindersharmalabs.xyz` forest and Microsoft Entra Cloud Sync for the `narindersharmalabs.org` forest.

The work included synchronization scoping, Password Hash Synchronization, user verification in Microsoft Entra, provisioning-agent setup, Connect Health review, and a stale-health-data investigation. The troubleshooting evidence confirms that the local services, scheduler, Microsoft endpoint connectivity, and Event Hub diagnostic upload were working. It does not claim that the portal alert had already cleared when the screenshots were captured.

![Microsoft Entra Connect Sync configuration complete](screenshots/11-hybrid-identity-synchronization/02-entra-connect-sync/17-connect-sync-configuration-complete.png)

![Microsoft Entra Cloud Sync configuration healthy](screenshots/11-hybrid-identity-synchronization/04-cloud-sync-configuration/13-cloud-sync-configuration-healthy.png)

![Connect Sync services, scheduler, and health connectivity verified](screenshots/11-hybrid-identity-synchronization/05-connect-health-troubleshooting/08-sync-services-scheduler-and-connectivity-verified.png)

---

## Configuration Walkthrough & Evidence Map

Evidence is organized by operational workstream:

| Workstream | Evidence Folder | Documentation |
|---|---|---|
| Tenant Foundation & Domain Readiness | [`screenshots/01-tenant-foundation`](screenshots/01-tenant-foundation)<br>[`screenshots/02-domain-readiness`](screenshots/02-domain-readiness) | [`docs/tenant-foundation-domain-readiness.md`](docs/tenant-foundation-domain-readiness.md) |
| User Provisioning | [`screenshots/03-user-provisioning`](screenshots/03-user-provisioning) | [`docs/user-lifecycle-administration.md`](docs/user-lifecycle-administration.md) |
| External Collaboration & Contacts | [`screenshots/04-external-collaboration-contacts`](screenshots/04-external-collaboration-contacts) | [`docs/external-collaboration-contacts.md`](docs/external-collaboration-contacts.md) |
| Group Collaboration | [`screenshots/05-group-collaboration`](screenshots/05-group-collaboration) | [`docs/group-collaboration-management.md`](docs/group-collaboration-management.md) |
| Licensing & Service Access | [`screenshots/06-licensing-service-access`](screenshots/06-licensing-service-access) | [`docs/licensing-service-access-review.md`](docs/licensing-service-access-review.md) |
| Service Health & Network Insights | [`screenshots/07-service-health-network-insights`](screenshots/07-service-health-network-insights) | [`docs/service-health-backup-readiness.md`](docs/service-health-backup-readiness.md) |
| Backup Readiness | [`screenshots/08-operational-resilience-backup`](screenshots/08-operational-resilience-backup) | [`docs/service-health-backup-readiness.md`](docs/service-health-backup-readiness.md) |
| PowerShell Admin Tooling | [`screenshots/09-powershell-admin-tooling`](screenshots/09-powershell-admin-tooling) | [`docs/powershell-graph-administration.md`](docs/powershell-graph-administration.md) |
| Role-Based Access & Delegation | [`screenshots/10-role-based-access-delegation`](screenshots/10-role-based-access-delegation) | [`docs/role-based-access-delegated-administration.md`](docs/role-based-access-delegated-administration.md) |
| Hybrid Identity Synchronization | [`screenshots/11-hybrid-identity-synchronization`](screenshots/11-hybrid-identity-synchronization) | [`docs/hybrid-identity-synchronization.md`](docs/hybrid-identity-synchronization.md) |

> Screenshot note: The full screenshot archive supporting these workstreams is available in the [`screenshots/`](screenshots/) directory. The [`evidence index`](docs/evidence-index.md) lists every published file by workstream.

---

## Core Competencies Demonstrated

* Built and validated a non-production Microsoft 365 tenant for hands-on administration.
* Created and validated member users across Microsoft 365 admin center, Azure portal, and Microsoft Entra admin center.
* Completed manual and bulk user provisioning workflows, including CSV-based account creation and post-creation verification.
* Created external contacts and completed Microsoft Entra B2B guest invitation workflows for external collaboration scenarios.
* Created, configured, and validated Microsoft 365 group settings, owners, members, and Entra-side group properties.
* Reviewed license inventory and service access views for troubleshooting and access-readiness awareness.
* Reviewed service health, network insights, software update visibility, and Log Analytics exposure for operational triage awareness.
* Configured and validated Microsoft 365 Backup policy readiness workflows for Exchange, OneDrive, and SharePoint.
* Used Microsoft Graph PowerShell to connect to a tenant, retrieve users, create users, create groups, review licensing, assign licenses, bulk-provision users from CSV, and clean up test accounts.
* Administered role-based access workflows, including Microsoft Entra role assignment, Microsoft 365 admin role management, administrative units, scoped User Administrator delegation, Purview role groups, and PIM-style eligible assignment configuration.
* Prepared Windows Server AD DS objects for synchronization and corrected an invalid UPN attribute with IDFix.
* Configured and verified Microsoft Entra Connect Sync and Microsoft Entra Cloud Sync in separate lab forests.
* Investigated Connect Health telemetry by checking services, the sync scheduler, outbound connectivity, and Cloud Sync audit results.
* Organized screenshots, evidence notes, and Markdown documentation into a structured public GitHub portfolio.

---

## Intended Role Alignment

This portfolio is aligned with entry-level and junior IT operations roles where Microsoft 365, Entra ID, user support, ticket triage, documentation, access administration, and escalation awareness are important:

* IT Support Technician
* Service Desk Analyst
* Help Desk Analyst
* Technical Support Analyst
* Desktop Support Technician
* Junior Systems Support Technician
* Junior Systems Administrator
* Junior Microsoft 365 Administrator

---

## Notes

This is a non-production portfolio environment. The focus is hands-on administration, safe documentation, least-privilege awareness, and support-oriented troubleshooting rather than production tenant ownership.
