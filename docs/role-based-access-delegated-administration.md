# Role-Based Access & Delegated Administration

## Administrative Objective

Administer Microsoft 365 and Microsoft Entra role-based access workflows used to assign administrative permissions, scope responsibilities, and support least-privilege operations in a non-production tenant.

This section documents hands-on role administration across Microsoft Entra admin center, Microsoft 365 admin center, Microsoft Defender XDR, Microsoft Purview, administrative units, and Privileged Identity Management concepts.

The workflow focuses on how roles are selected, assigned, scoped, validated, and removed when access needs to be controlled across Microsoft 365 services.

---

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
* Confirmed administrative unit scope behavior, membership visibility, and dynamic membership option exposure.
* Worked through Privileged Identity Management views for eligible roles, active roles, pending requests, expired roles, approval views, and role assignment management.
* Configured and validated a PIM-style eligible assignment workflow for temporary administrative access.

---

## Evidence Walkthrough

### 1. Reviewed Microsoft Entra role catalog

The Microsoft Entra roles and administrators catalog was reviewed to identify where administrative roles are selected and managed.

![Microsoft Entra roles and administrators catalog](../screenshots/10-role-based-access-delegation/01-entra-roles-and-administrators-overview.png)

### 2. Validated role description before assignment

Role description details were checked before assignment to understand the purpose and scope of the selected role.

![Microsoft Entra role description validation](../screenshots/10-role-based-access-delegation/02-entra-role-description-validation.png)

### 3. Validated role permissions

Role permissions were checked before assignment to understand what the selected administrative role allows.

![Microsoft Entra role permissions validation](../screenshots/10-role-based-access-delegation/03-entra-role-permissions-validation.png)

### 4. Checked role settings

Role settings were checked to understand assignment behavior and role configuration before completing administrative changes.

![Microsoft Entra role settings validation](../screenshots/10-role-based-access-delegation/04-entra-role-settings-validation.png)

### 5. Validated Helpdesk Administrator role behavior

The Helpdesk Administrator role was reviewed as a common support role relevant to password reset and user support workflows.

![Helpdesk Administrator role validation](../screenshots/10-role-based-access-delegation/05-helpdesk-administrator-role-validation.png)

### 6. Validated Intune Administrator role behavior

The Intune Administrator role was checked to compare endpoint-management administration scope against other Microsoft 365 support roles.

![Intune Administrator role validation](../screenshots/10-role-based-access-delegation/06-intune-administrator-role-validation.png)

### 7. Started Microsoft Entra role assignment

A Microsoft Entra role assignment workflow was started to demonstrate hands-on role assignment.

![Microsoft Entra role assignment workflow start](../screenshots/10-role-based-access-delegation/07-entra-role-assignment-start.png)

### 8. Selected member for role assignment

A lab user was selected as the member for the role assignment workflow.

![Microsoft Entra role assignment member selection](../screenshots/10-role-based-access-delegation/08-entra-role-assignment-member-selection.png)

### 9. Confirmed Microsoft Entra role assignment

The role assignment completed successfully and was confirmed in Microsoft Entra.

![Microsoft Entra role assignment completed](../screenshots/10-role-based-access-delegation/09-entra-role-assignment-success.png)

### 10. Reviewed Microsoft 365 admin center role management

Microsoft 365 admin center role management was reviewed to compare how roles appear outside the Entra admin center.

![Microsoft 365 admin center role management overview](../screenshots/10-role-based-access-delegation/10-m365-admin-center-role-management-overview.png)

### 11. Started Microsoft 365 admin center role assignment

A role assignment workflow was started from the Microsoft 365 admin center.

![Microsoft 365 admin center role assignment workflow](../screenshots/10-role-based-access-delegation/11-m365-admin-center-assign-role.png)

### 12. Confirmed Microsoft 365 admin center role assignment

The Microsoft 365 admin center role assignment workflow completed successfully.

![Microsoft 365 admin center role assignment completed](../screenshots/10-role-based-access-delegation/12-m365-admin-center-role-assignment-complete.png)

### 13. Checked Exchange admin center role surface

The Exchange admin center role surface was checked to understand workload-specific role management exposure.

![Exchange admin center role surface](../screenshots/10-role-based-access-delegation/13-exchange-admin-center-role-view.png)

### 14. Checked Intune admin center role surface

The Intune admin center role surface was checked to understand endpoint-management permission exposure.

![Intune admin center role surface](../screenshots/10-role-based-access-delegation/14-intune-admin-center-role-view.png)

### 15. Validated Defender XDR permission surface

The Defender XDR permission surface was checked to understand how security-related permissions appear in workload-specific admin centers.

![Defender XDR permission surface validation](../screenshots/10-role-based-access-delegation/15-defender-xdr-permission-surface-validation.png)

### 16. Checked Defender email and collaboration role view

The Defender email and collaboration role view was checked as part of workload-specific role awareness.

![Defender email and collaboration role validation](../screenshots/10-role-based-access-delegation/16-defender-email-collaboration-role-validation.png)

### 17. Opened Microsoft Purview role group management

Microsoft Purview role group management was opened to review Purview-specific role group administration.

![Microsoft Purview role group management](../screenshots/10-role-based-access-delegation/17-purview-role-groups-management.png)

### 18. Assigned a Microsoft Purview role group

A Microsoft Purview role group assignment workflow was completed to demonstrate role group administration.

![Microsoft Purview role group assignment workflow](../screenshots/10-role-based-access-delegation/18-purview-role-group-assignment-workflow.png)

### 19. Confirmed Microsoft Purview role group assignment

The Purview role group assignment was confirmed after the workflow completed.

![Microsoft Purview role group assignment confirmation](../screenshots/10-role-based-access-delegation/19-purview-role-group-assignment-confirmation.png)

### 20. Opened administrative units management

Administrative units management was opened to demonstrate scoped delegation concepts.

![Administrative units management overview](../screenshots/10-role-based-access-delegation/20-administrative-units-overview.png)

### 21. Selected scoped role assignment for administrative unit

A scoped role assignment was selected through the administrative unit workflow.

![Administrative unit scoped role assignment selection](../screenshots/10-role-based-access-delegation/21-administrative-unit-role-assignment-selection.png)

### 22. Confirmed administrative unit restricted management

The administrative unit list confirmed the New York administrative unit was created with restricted management enabled and assigned membership.

![Administrative unit restricted management confirmation](../screenshots/10-role-based-access-delegation/22-administrative-unit-restricted-management-confirmation.png)

### 23. Confirmed administrative unit membership

Administrative unit membership was confirmed after lab users were added to the unit.

![Administrative unit member confirmation](../screenshots/10-role-based-access-delegation/23-administrative-unit-member-confirmation.png)

### 24. Verified administrative unit visibility in Microsoft Entra admin center

The administrative unit list was checked from the Microsoft Entra admin center to confirm the scoped administrative units were visible from the Entra role management surface.

![Administrative unit visibility in Microsoft Entra admin center](../screenshots/10-role-based-access-delegation/24-administrative-unit-entra-list-confirmation.png)

### 25. Confirmed scoped User Administrator assignment

The User Administrator assignment view confirmed that the delegated admin account was assigned with scope limited to the New York administrative unit.

![Administrative unit scoped User Administrator assignment](../screenshots/10-role-based-access-delegation/25-administrative-unit-scope-check.png)

### 26. Reviewed dynamic membership options

The administrative unit membership type options were checked to identify assigned membership, dynamic user membership, and dynamic device membership paths.

![Administrative unit dynamic membership options](../screenshots/10-role-based-access-delegation/26-administrative-unit-dynamic-membership-options.png)

### 27. Opened Privileged Identity Management access management

Privileged Identity Management was opened to review eligible and temporary administrative access concepts.

![Privileged Identity Management access overview](../screenshots/10-role-based-access-delegation/27-pim-access-management-overview.png)

### 28. Checked PIM eligible roles view

The PIM eligible roles view was checked to understand how eligible administrative access is displayed.

![PIM eligible roles validation](../screenshots/10-role-based-access-delegation/28-pim-eligible-roles-validation.png)

### 29. Opened PIM role assignment management

PIM role assignment management was opened to understand where role assignments are managed.

![PIM role assignment management](../screenshots/10-role-based-access-delegation/29-pim-role-assignment-management.png)

### 30. Configured PIM-style eligible assignment

A PIM-style eligible assignment workflow was configured for temporary administrative access.

![PIM eligible assignment configuration](../screenshots/10-role-based-access-delegation/30-pim-eligible-assignment-configuration.png)

### 31. Confirmed PIM-style eligible assignment

The eligible assignment workflow was confirmed after configuration.

![PIM eligible assignment confirmation](../screenshots/10-role-based-access-delegation/31-pim-eligible-assignment-confirmation.png)

---

## Skills Demonstrated

* Microsoft Entra role assignment and validation
* Microsoft 365 admin center role administration
* Administrative unit creation and membership management
* Scoped User Administrator delegation
* Microsoft Purview role group assignment and validation
* Defender XDR / Purview / Intune permission awareness
* Least-privilege access control
* Privileged Identity Management workflow awareness
* Cross-portal validation
* Screenshot-based technical documentation

---

## Support Relevance

Role management is a core part of secure Microsoft 365 administration.

Support and junior administration teams need to understand what an assigned role allows, where the role is managed, whether the assignment is tenant-wide or scoped, and how temporary access can be controlled.

This workflow is relevant to service desk and support scenarios where a technician, administrator, or delegated support user requires limited administrative access for a defined support task without receiving unnecessary tenant-wide permissions.

Administrative units are especially relevant for scoped delegation because they allow administrative responsibility to be limited to a defined subset of users instead of the full organization.

---

## Outcome

Role-based access was administered across Microsoft 365, Microsoft Entra, Defender XDR, and Microsoft Purview surfaces.

Administrative units were used to demonstrate scoped delegation, and Privileged Identity Management was used to document eligible and temporary administrative access concepts.

This strengthens the portfolio beyond basic user and group administration by showing practical exposure to least privilege, scoped administration, workload-specific role management, and just-in-time access workflows.
