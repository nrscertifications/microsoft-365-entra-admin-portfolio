# Microsoft 365 & Entra ID Administration Portfolio

## Project Overview

This repository documents a hands-on Microsoft 365 and Microsoft Entra ID administration environment focused on tenant readiness, user administration, external collaboration, group management, licensing review, service health, backup readiness, and Microsoft Graph PowerShell administration.

I configured the work in a dedicated non-production Microsoft 365 tenant using fictional users, test contacts, sample guest users, and lab-only objects. The repository is organized by administrative workflow instead of course section, so the evidence can be reviewed as a practical IT Support, Service Desk, Technical Support, or junior systems administration portfolio.

The goal of this project was to understand how the Microsoft 365 admin center, Microsoft Entra admin center, Azure portal, and Microsoft Graph PowerShell connect across tenant setup, identity objects, licensing, collaboration, operational support views, and command-line administration.

> **Data and lab context note:** Screenshots use fictional users, test objects, and sample external collaboration targets created only for this Microsoft 365 / Entra ID lab. User names and lab email addresses are intentionally visible where they help show workflow verification. Temporary password values shown in command examples or portal output were redacted before publishing. No production customer data, private user data, or live business records are included.

---

## Core Technical Skills & Tools

* **Microsoft 365 Administration:** Tenant navigation, active user management, contacts, groups, licensing, service health, and service access review
* **Tenant & Domain Readiness:** Tenant overview validation, custom domain workflow review, primary domain awareness, and admin portal navigation
* **Microsoft Entra ID:** Member users, guest users, external collaboration, group objects, identity properties, and portal validation
* **Azure Portal:** Tenant and directory administration, resource group review, and Log Analytics workspace exposure
* **Microsoft Graph PowerShell:** Module installation, delegated authentication, Graph scopes, user retrieval, test user creation, group creation, subscribed SKU review, license assignment, CSV-based bulk provisioning, and cleanup validation
* **User Lifecycle Administration:** Manual provisioning, bulk provisioning, profile properties, account state review, license review, and cross-portal verification
* **External Collaboration:** B2B guest invitation workflow, external contacts, address book visibility concepts, and Outlook web access validation
* **Group Administration:** Microsoft 365 groups, owners, members, group properties, Entra group validation, and dynamic membership exposure
* **Role-Based Access & Delegated Administration:** Microsoft Entra role assignment, Microsoft 365 admin role management, administrative units, scoped User Administrator delegation, Purview role groups, Defender/Purview permission surfaces, and PIM eligible assignment workflows
* **Operational Readiness:** Service health, network insights, software update visibility, and Microsoft 365 Backup readiness review
* **Documentation & Version Control:** Markdown documentation, screenshot evidence mapping, Git/GitHub portfolio structure, and technical portfolio publishing

---

## Functional Architecture & Evidence

### 1. Tenant Foundation & Domain Readiness

I established the tenant foundation used for the rest of the administrative work. This included tenant overview validation, admin portal navigation, custom domain workflow review, and resource-backed service visibility through Azure.

This provided the base layer for user identities, email addressing, licensing, collaboration, service health, and backup readiness.

![Tenant creation confirmation](screenshots/01-tenant-foundation/03-tenant-create-successful-04.png)

![Custom domain verification](screenshots/02-domain-readiness/03-custom-domain-azure03-verified.png)

### 2. Identity & User Lifecycle Administration

I created internal member users from multiple admin portals and verified that the same user objects appeared across Microsoft 365 admin center, Azure portal, and Microsoft Entra admin center.

This helped confirm the difference between the portal used to complete an admin task and the underlying identity object stored in Microsoft Entra ID.

![Microsoft 365 admin user creation](screenshots/03-user-provisioning/19-m365-admin-user-create-01.png)

![User visible in Entra users list](screenshots/03-user-provisioning/15-m365-admin-user-create-azure-portal-confirmation-07.png)

### 3. Bulk User Provisioning

I reviewed the bulk user creation workflow, including CSV-based account creation, generated results, and post-creation verification in the active users list.

This workflow is relevant to onboarding scenarios where multiple accounts need to be created consistently before licenses, groups, and access are finalized.

![Bulk user provisioning workflow](screenshots/03-user-provisioning/01-bulk-user-provisioning-01.png)

![Bulk user provisioning completed with temporary passwords redacted](screenshots/03-user-provisioning/13-bulk-user-provisioning-completed-redacted-passwords.png)

### 4. External Collaboration & Address Book Management

I created external contacts for address book visibility and reviewed the guest invitation workflow through Microsoft Entra B2B collaboration.

This workflow separates two common support scenarios: external contacts used for discoverability and communication, and guest users that become tenant-visible collaboration identities after invitation.

![External contact creation](screenshots/04-external-collaboration-contacts/02-external-contact-create-01.png)

![External guest invitation review](screenshots/04-external-collaboration-contacts/07-external-guest-invitation-04.png)

### 5. Group-Based Collaboration Management

I created and reviewed Microsoft 365 group configuration, including group properties, owners, members, and Entra-side object validation.

This demonstrates how group objects support collaboration, membership management, and access-related administration in Microsoft 365 environments.

![Microsoft 365 group creation](screenshots/05-group-collaboration/01-groups-m365-group-create-01.png)

![Group owners validation](screenshots/05-group-collaboration/10-groups-add-365-group-owners-010.png)

### 6. Licensing & Service Access Review

I reviewed license inventory, user assignment views, and service access settings from the admin center.

The focus was administrative review: checking available products, where license assignments are viewed, how licensing affects service access, and why license state matters during account troubleshooting.

![License inventory review](screenshots/06-licensing-service-access/01-license-inventory-review-01.png)

### 7. Operational Visibility & Backup Readiness

I reviewed admin views for service health, network insights, software update visibility, Log Analytics exposure, and Microsoft 365 Backup readiness for Exchange, OneDrive, and SharePoint.

These views support service desk triage by helping separate local device issues from tenant-level service issues, network readiness problems, service access issues, or backup-readiness gaps.

![Network insights location configuration](screenshots/07-service-health-network-insights/01-network-insights-location-complete.png)

![Backup policy readiness](screenshots/08-operational-resilience-backup/01-exchange-backup-policy-01.png)

### 8. PowerShell & Microsoft Graph Administration Track

I documented command-line administration separately from the portal-based work because PowerShell and Microsoft Graph support repeatable provisioning, reporting, validation, and cleanup workflows.

This track includes Microsoft Graph PowerShell module setup, delegated tenant authentication, user retrieval, test user creation, Microsoft 365 group creation, subscribed SKU review, license assignment, CSV-based bulk user provisioning, and cleanup of test accounts after verification.

![Microsoft Graph sign-in successful](screenshots/09-powershell-admin-tooling/14-graph-sign-in-successful.png)

![Microsoft Graph bulk user import command with temporary password redacted](screenshots/09-powershell-admin-tooling/22-graph-bulk-user-import-command-password-redacted.png)

![Microsoft Graph license review and assignment](screenshots/09-powershell-admin-tooling/20-graph-license-review-assignment.png)

### 9. Role-Based Access & Delegated Administration

I administered role-based access workflows across Microsoft 365 admin center, Microsoft Entra admin center, Defender XDR, Microsoft Purview, administrative units, and Privileged Identity Management concepts in a non-production tenant.

This work covered hands-on role assignment, administrative unit creation, scoped User Administrator delegation, Purview role group workflows, and PIM-style eligible assignment configuration for temporary administrative access.

![Microsoft 365 role assignment completed](screenshots/10-role-based-access-delegation/12-m365-admin-center-role-assignment-complete.png)

![Administrative unit scoped role assignment confirmation](screenshots/10-role-based-access-delegation/22-administrative-unit-scoped-role-confirmation.png)

![PIM eligible assignment confirmation](screenshots/10-role-based-access-delegation/31-pim-eligible-assignment-confirmation.png)

---

## Configuration Walkthrough & Evidence Map

Evidence is organized by operational workstream:

| Workstream | Evidence Folder | Documentation |
|---|---|---|
| Tenant Foundation | [`screenshots/01-tenant-foundation`](screenshots/01-tenant-foundation) | [`docs/tenant-foundation-domain-readiness.md`](docs/tenant-foundation-domain-readiness.md) |
| Domain Readiness | [`screenshots/02-domain-readiness`](screenshots/02-domain-readiness) | [`docs/tenant-foundation-domain-readiness.md`](docs/tenant-foundation-domain-readiness.md) |
| User Provisioning | [`screenshots/03-user-provisioning`](screenshots/03-user-provisioning) | [`docs/user-lifecycle-administration.md`](docs/user-lifecycle-administration.md) |
| External Collaboration & Contacts | [`screenshots/04-external-collaboration-contacts`](screenshots/04-external-collaboration-contacts) | [`docs/external-collaboration-contacts.md`](docs/external-collaboration-contacts.md) |
| Group Collaboration | [`screenshots/05-group-collaboration`](screenshots/05-group-collaboration) | [`docs/group-collaboration-management.md`](docs/group-collaboration-management.md) |
| Licensing & Service Access | [`screenshots/06-licensing-service-access`](screenshots/06-licensing-service-access) | [`docs/licensing-service-access-review.md`](docs/licensing-service-access-review.md) |
| Service Health & Network Insights | [`screenshots/07-service-health-network-insights`](screenshots/07-service-health-network-insights) | [`docs/service-health-backup-readiness.md`](docs/service-health-backup-readiness.md) |
| Backup Readiness | [`screenshots/08-operational-resilience-backup`](screenshots/08-operational-resilience-backup) | [`docs/service-health-backup-readiness.md`](docs/service-health-backup-readiness.md) |
| PowerShell Admin Tooling | [`screenshots/09-powershell-admin-tooling`](screenshots/09-powershell-admin-tooling) | [`docs/powershell-graph-administration.md`](docs/powershell-graph-administration.md) |
| Role-Based Access & Delegation | [`screenshots/10-role-based-access-delegation`](screenshots/10-role-based-access-delegation) | [`docs/role-based-access-delegated-administration.md`](docs/role-based-access-delegated-administration.md) |

> Screenshot note: The full screenshot archive supporting these workstreams is available in the [`screenshots/`](screenshots/) directory.

---

## Core Competencies Demonstrated

* Built and validated a non-production Microsoft 365 tenant for administration practice.
* Created and reviewed member users across Microsoft 365 admin center, Azure portal, and Microsoft Entra admin center.
* Practiced manual and bulk user provisioning workflows, including post-creation verification.
* Used Microsoft Graph PowerShell to connect to a tenant, retrieve users, create users, create groups, review licensing, assign licenses, bulk-provision users from CSV, and clean up test accounts.
* Separated internal users, guest users, and external contacts based on how each object is used in Microsoft 365 and Entra ID.
* Created and reviewed Microsoft 365 group settings, owners, members, and Entra-side group properties.
* Reviewed license inventory and service access views for troubleshooting and access-readiness awareness.
* Reviewed operational admin views related to service health, network insights, software update visibility, and backup readiness.
* Organized screenshots, evidence notes, and markdown documentation into a structured public GitHub portfolio.

---

## Intended Role Alignment

This portfolio is aligned with entry-level and junior IT operations roles where Microsoft 365, Entra ID, user support, ticket triage, documentation, and escalation awareness are important:

* IT Support Technician
* Service Desk Analyst
* Help Desk Analyst
* Technical Support Analyst
* Desktop Support Technician
* Junior Systems Support Technician

---

## Notes

This is a non-production learning and portfolio environment. The focus is on administrative workflow understanding, safe lab documentation, and support-oriented troubleshooting awareness rather than production tenant ownership.
