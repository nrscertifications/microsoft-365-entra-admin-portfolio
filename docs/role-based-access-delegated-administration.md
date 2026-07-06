# Role-Based Access & Delegated Administration

## Administrative Objective
Review Microsoft 365 and Microsoft Entra role administration workflows used to control administrative access, scope responsibilities, and support least-privilege operations in a non-production tenant.

This section focuses on how admin permissions are reviewed and assigned across Microsoft 365 admin center, Microsoft Entra admin center, Microsoft Defender XDR, Microsoft Purview, administrative units, and Privileged Identity Management.

## Work Completed

* Reviewed Microsoft Entra role categories, role descriptions, permission details, and role settings.
* Reviewed common admin roles used in support and operations, including Helpdesk Administrator, Global Reader, Exchange Administrator, Intune Administrator, Teams Administrator, SharePoint Administrator, and Identity Governance Administrator.
* Assigned an administrative role to a lab user and validated the role assignment workflow.
* Reviewed Microsoft 365 admin center role assignment behavior and compared it with Entra role management.
* Reviewed role and permission areas across Microsoft Defender XDR and Microsoft Purview.
* Reviewed Microsoft Purview role groups, role group assignment, confirmation, and removal workflow.
* Created and reviewed administrative units for scoped delegation.
* Assigned a scoped User Administrator role through an administrative unit.
* Added lab users to an administrative unit and verified membership through Microsoft 365 admin center and Microsoft Entra admin center.
* Reviewed administrative unit scope behavior and dynamic membership query exposure.
* Reviewed Privileged Identity Management views for eligible roles, active roles, pending requests, expired roles, approval views, and role assignment management.
* Configured and validated a PIM-style eligible assignment workflow for temporary role access.

## Support Relevance
Role management is a core part of secure Microsoft 365 administration. Support and junior administration teams need to understand what an assigned role allows, where the role is managed, whether the assignment is tenant-wide or scoped, and how temporary access can be controlled.

This workflow is relevant to service desk and support scenarios where a user needs limited administrative rights for a defined support task, a team needs scoped access to a subset of users, or an administrator needs to confirm whether a role assignment is active, eligible, pending, expired, or limited by administrative unit scope.

## Workflow Evidence

### Microsoft Entra role review

![Entra roles and administrators overview](../screenshots/10-role-based-access-delegation/01-entra-roles-and-administrators-overview.png)

![Entra role description review](../screenshots/10-role-based-access-delegation/02-entra-role-description-review.png)

![Entra role permissions review](../screenshots/10-role-based-access-delegation/03-entra-role-permissions-review.png)

![Helpdesk Administrator role review](../screenshots/10-role-based-access-delegation/05-helpdesk-administrator-role-review.png)

### Role assignment workflow

![Entra role assignment start](../screenshots/10-role-based-access-delegation/07-entra-role-assignment-start.png)

![Entra role assignment member selection](../screenshots/10-role-based-access-delegation/08-entra-role-assignment-member-selection.png)

![Entra role assignment success](../screenshots/10-role-based-access-delegation/09-entra-role-assignment-success.png)

### Microsoft 365 admin center role review

![Microsoft 365 admin center role overview](../screenshots/10-role-based-access-delegation/10-m365-admin-center-role-overview.png)

![Microsoft 365 admin center assign role](../screenshots/10-role-based-access-delegation/11-m365-admin-center-assign-role.png)

![Microsoft 365 admin center role assignment complete](../screenshots/10-role-based-access-delegation/12-m365-admin-center-role-assignment-complete.png)

### Defender XDR and Purview role groups

![Defender XDR permissions review](../screenshots/10-role-based-access-delegation/15-defender-xdr-permissions-review.png)

![Defender email and collaboration role review](../screenshots/10-role-based-access-delegation/16-defender-email-collaboration-role-review.png)

![Purview role groups review](../screenshots/10-role-based-access-delegation/17-purview-role-groups-review.png)

![Purview role group assignment confirmation](../screenshots/10-role-based-access-delegation/19-purview-role-group-assignment-confirmation.png)

### Administrative units and scoped delegation

![Administrative units overview](../screenshots/10-role-based-access-delegation/20-administrative-units-overview.png)

![Administrative unit role assignment selection](../screenshots/10-role-based-access-delegation/21-administrative-unit-role-assignment-selection.png)

![Administrative unit scoped role confirmation](../screenshots/10-role-based-access-delegation/22-administrative-unit-scoped-role-confirmation.png)

![Administrative unit member confirmation](../screenshots/10-role-based-access-delegation/23-administrative-unit-member-confirmation.png)

![Administrative unit Entra user confirmation](../screenshots/10-role-based-access-delegation/24-administrative-unit-entra-user-confirmation.png)

![Administrative unit scope check](../screenshots/10-role-based-access-delegation/25-administrative-unit-scope-check.png)

![Administrative unit dynamic membership query](../screenshots/10-role-based-access-delegation/26-administrative-unit-dynamic-membership-query.png)

### Privileged Identity Management

![PIM overview](../screenshots/10-role-based-access-delegation/27-pim-overview.png)

![PIM eligible roles review](../screenshots/10-role-based-access-delegation/28-pim-eligible-roles-review.png)

![PIM managed role assignment review](../screenshots/10-role-based-access-delegation/29-pim-managed-role-assignment-review.png)

![PIM eligible assignment configuration](../screenshots/10-role-based-access-delegation/30-pim-eligible-assignment-configuration.png)

![PIM eligible assignment confirmation](../screenshots/10-role-based-access-delegation/31-pim-eligible-assignment-confirmation.png)

## Outcome
Role-based access workflows were reviewed across Microsoft 365, Microsoft Entra, Defender XDR, and Microsoft Purview. Administrative units were used to demonstrate scoped delegation, and Privileged Identity Management was reviewed as a controlled access model for eligible and temporary administrative access.

This strengthens the portfolio beyond basic user and group administration by showing awareness of least privilege, scoped administration, portal-specific role management, and just-in-time access concepts.
