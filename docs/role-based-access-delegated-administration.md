# Role-Based Access & Delegated Administration

## Administrative Objective
Administer Microsoft 365 and Microsoft Entra role-based access workflows used to assign administrative permissions, scope responsibilities, and support least-privilege operations in a non-production tenant.

This section documents hands-on role administration across Microsoft Entra admin center, Microsoft 365 admin center, Microsoft Defender XDR, Microsoft Purview, administrative units, and Privileged Identity Management concepts. The workflow focuses on how roles are selected, assigned, scoped, validated, and removed when access needs to be controlled across Microsoft 365 services.

## Work Completed

* Validated Microsoft Entra role categories, role descriptions, permission details, and role settings before assignment.
* Compared support and operations roles including Helpdesk Administrator, Global Reader, Exchange Administrator, Intune Administrator, Teams Administrator, SharePoint Administrator, and Identity Governance Administrator.
* Assigned an administrative role to a lab user and confirmed the completed role assignment in Microsoft Entra.
* Administered Microsoft 365 admin center role assignment workflows and compared Microsoft 365 role behavior with Microsoft Entra role management.
* Checked workload-specific role and permission surfaces across Exchange admin center, Intune admin center, Microsoft Defender XDR, and Microsoft Purview.
* Managed Microsoft Purview role group workflows, including role group assignment, confirmation, validation, and removal.
* Created administrative units to support scoped delegation.
* Assigned a scoped User Administrator role through an administrative unit.
* Added lab users to an administrative unit and verified membership through both Microsoft 365 admin center and Microsoft Entra admin center.
* Confirmed administrative unit scope behavior, membership visibility, and dynamic membership query exposure.
* Worked through Privileged Identity Management views for eligible roles, active roles, pending requests, expired roles, approval views, and role assignment management.
* Configured and validated a PIM-style eligible assignment workflow for temporary administrative access.

## Support Relevance
Role management is a core part of secure Microsoft 365 administration. Support and junior administration teams need to understand what an assigned role allows, where the role is managed, whether the assignment is tenant-wide or scoped, and how temporary access can be controlled.

This workflow is relevant to service desk and support scenarios where a technician, administrator, or delegated support user requires limited administrative access for a defined support task without receiving unnecessary tenant-wide permissions.

Administrative units are especially relevant for scoped delegation because they allow administrative responsibility to be limited to a defined subset of users instead of the full organization.

## Workflow Evidence

### Role inventory and permission validation

![Microsoft Entra roles and administrators catalog](../screenshots/10-role-based-access-delegation/01-entra-roles-and-administrators-overview.png)

![Microsoft Entra role description validation](../screenshots/10-role-based-access-delegation/02-entra-role-description-validation.png)

![Microsoft Entra role permissions validation](../screenshots/10-role-based-access-delegation/03-entra-role-permissions-validation.png)

![Helpdesk Administrator role validation](../screenshots/10-role-based-access-delegation/05-helpdesk-administrator-role-validation.png)

### Role assignment administration

![Microsoft Entra role assignment workflow start](../screenshots/10-role-based-access-delegation/07-entra-role-assignment-start.png)

![Microsoft Entra role assignment member selection](../screenshots/10-role-based-access-delegation/08-entra-role-assignment-member-selection.png)

![Microsoft Entra role assignment completed](../screenshots/10-role-based-access-delegation/09-entra-role-assignment-success.png)

### Microsoft 365 admin center role administration

![Microsoft 365 admin center role management overview](../screenshots/10-role-based-access-delegation/10-m365-admin-center-role-management-overview.png)

![Microsoft 365 admin center role assignment workflow](../screenshots/10-role-based-access-delegation/11-m365-admin-center-assign-role.png)

![Microsoft 365 admin center role assignment completed](../screenshots/10-role-based-access-delegation/12-m365-admin-center-role-assignment-complete.png)

### Workload permission surfaces and role groups

![Exchange admin center role surface](../screenshots/10-role-based-access-delegation/13-exchange-admin-center-role-view.png)

![Intune admin center role surface](../screenshots/10-role-based-access-delegation/14-intune-admin-center-role-view.png)

![Defender XDR permission surface validation](../screenshots/10-role-based-access-delegation/15-defender-xdr-permission-surface-validation.png)

![Defender email and collaboration role validation](../screenshots/10-role-based-access-delegation/16-defender-email-collaboration-role-validation.png)

![Microsoft Purview role group management](../screenshots/10-role-based-access-delegation/17-purview-role-groups-management.png)

![Microsoft Purview role group assignment workflow](../screenshots/10-role-based-access-delegation/18-purview-role-group-assignment-workflow.png)

![Microsoft Purview role group assignment confirmation](../screenshots/10-role-based-access-delegation/19-purview-role-group-assignment-confirmation.png)

### Administrative units and scoped delegation

![Administrative units management overview](../screenshots/10-role-based-access-delegation/20-administrative-units-overview.png)

![Administrative unit scoped role assignment selection](../screenshots/10-role-based-access-delegation/21-administrative-unit-role-assignment-selection.png)

![Administrative unit scoped role assignment confirmation](../screenshots/10-role-based-access-delegation/22-administrative-unit-scoped-role-confirmation.png)

![Administrative unit member confirmation](../screenshots/10-role-based-access-delegation/23-administrative-unit-member-confirmation.png)

![Administrative unit user membership verified in Microsoft Entra](../screenshots/10-role-based-access-delegation/24-administrative-unit-entra-user-confirmation.png)

![Administrative unit scope validation](../screenshots/10-role-based-access-delegation/25-administrative-unit-scope-check.png)

![Administrative unit dynamic membership query exposure](../screenshots/10-role-based-access-delegation/26-administrative-unit-dynamic-membership-query.png)

### Privileged Identity Management and eligible access

![Privileged Identity Management access overview](../screenshots/10-role-based-access-delegation/27-pim-access-management-overview.png)

![PIM eligible roles validation](../screenshots/10-role-based-access-delegation/28-pim-eligible-roles-validation.png)

![PIM role assignment management](../screenshots/10-role-based-access-delegation/29-pim-role-assignment-management.png)

![PIM eligible assignment configuration](../screenshots/10-role-based-access-delegation/30-pim-eligible-assignment-configuration.png)

![PIM eligible assignment confirmation](../screenshots/10-role-based-access-delegation/31-pim-eligible-assignment-confirmation.png)

## Skills Demonstrated

* Microsoft Entra role assignment and validation
* Microsoft 365 admin center role administration
* Administrative unit creation and membership management
* Scoped User Administrator delegation
* Microsoft Purview role group assignment and removal
* Defender XDR / Purview / Intune permission awareness
* Least-privilege access control
* Privileged Identity Management workflow awareness
* Cross-portal validation
* Screenshot-based technical documentation

## Outcome
Role-based access was administered across Microsoft 365, Microsoft Entra, Defender XDR, and Microsoft Purview surfaces. Administrative units were used to demonstrate scoped delegation, and Privileged Identity Management was used to document eligible and temporary administrative access concepts.

This strengthens the portfolio beyond basic user and group administration by showing practical exposure to least privilege, scoped administration, workload-specific role management, and just-in-time access workflows.
