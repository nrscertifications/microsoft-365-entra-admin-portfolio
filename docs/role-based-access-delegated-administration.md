# Role-Based Access & Delegated Administration

## Administrative Objective

Administer Microsoft 365 and Microsoft Entra role-based access, scoped delegation, workload-specific permission surfaces, and temporary eligible access workflows.

## Work Completed

* Reviewed Microsoft Entra role descriptions, permissions, settings, and support-focused role options.
* Completed administrative role assignments in Microsoft Entra and Microsoft 365 admin center.
* Reviewed role and permission surfaces in Exchange, Intune, Defender XDR, and Microsoft Purview.
* Completed a Microsoft Purview role group assignment workflow.
* Created administrative units, added members, and assigned a scoped User Administrator role.
* Reviewed dynamic administrative unit membership options.
* Configured and confirmed a PIM-style eligible role assignment.

## Evidence Walkthrough

### Role review and direct assignment

I reviewed the Entra role catalog, description, permissions, and settings before comparing Helpdesk Administrator and Intune Administrator. I then selected a lab user and completed the role assignment.

![Microsoft Entra roles and administrators catalog](../screenshots/10-role-based-access-delegation/01-entra-roles-and-administrators-overview.png)

![Microsoft Entra role description validation](../screenshots/10-role-based-access-delegation/02-entra-role-description-validation.png)

![Microsoft Entra role permissions validation](../screenshots/10-role-based-access-delegation/03-entra-role-permissions-validation.png)

![Microsoft Entra role settings validation](../screenshots/10-role-based-access-delegation/04-entra-role-settings-validation.png)

![Helpdesk Administrator role validation](../screenshots/10-role-based-access-delegation/05-helpdesk-administrator-role-validation.png)

![Intune Administrator role validation](../screenshots/10-role-based-access-delegation/06-intune-administrator-role-validation.png)

![Microsoft Entra role assignment workflow start](../screenshots/10-role-based-access-delegation/07-entra-role-assignment-start.png)

![Microsoft Entra role assignment member selection](../screenshots/10-role-based-access-delegation/08-entra-role-assignment-member-selection.png)

![Microsoft Entra role assignment completed](../screenshots/10-role-based-access-delegation/09-entra-role-assignment-success.png)

### Microsoft 365 and workload-specific role surfaces

I reviewed Microsoft 365 admin center role management, completed a role assignment, and compared the role and permission locations used by Exchange, Intune, Defender XDR, and Defender email and collaboration administration.

![Microsoft 365 admin center role management overview](../screenshots/10-role-based-access-delegation/10-m365-admin-center-role-management-overview.png)

![Microsoft 365 admin center role assignment workflow](../screenshots/10-role-based-access-delegation/11-m365-admin-center-assign-role.png)

![Microsoft 365 admin center role assignment completed](../screenshots/10-role-based-access-delegation/12-m365-admin-center-role-assignment-complete.png)

![Exchange admin center role surface](../screenshots/10-role-based-access-delegation/13-exchange-admin-center-role-view.png)

![Intune admin center role surface](../screenshots/10-role-based-access-delegation/14-intune-admin-center-role-view.png)

![Defender XDR permission surface validation](../screenshots/10-role-based-access-delegation/15-defender-xdr-permission-surface-validation.png)

![Defender email and collaboration role validation](../screenshots/10-role-based-access-delegation/16-defender-email-collaboration-role-validation.png)

### Microsoft Purview role groups

I opened Purview role group management, completed the role group assignment workflow, and confirmed the assignment result.

![Microsoft Purview role group management](../screenshots/10-role-based-access-delegation/17-purview-role-groups-management.png)

![Microsoft Purview role group assignment workflow](../screenshots/10-role-based-access-delegation/18-purview-role-group-assignment-workflow.png)

![Microsoft Purview role group assignment confirmation](../screenshots/10-role-based-access-delegation/19-purview-role-group-assignment-confirmation.png)

### Administrative units and scoped delegation

I created administrative units, selected a scoped role assignment, confirmed restricted management and membership, verified the units in Microsoft Entra, and confirmed that the delegated User Administrator assignment was limited to the New York administrative unit.

![Administrative units management overview](../screenshots/10-role-based-access-delegation/20-administrative-units-overview.png)

![Administrative unit scoped role assignment selection](../screenshots/10-role-based-access-delegation/21-administrative-unit-role-assignment-selection.png)

![Administrative unit restricted management confirmation](../screenshots/10-role-based-access-delegation/22-administrative-unit-restricted-management-confirmation.png)

![Administrative unit member confirmation](../screenshots/10-role-based-access-delegation/23-administrative-unit-member-confirmation.png)

![Administrative unit visibility in Microsoft Entra admin center](../screenshots/10-role-based-access-delegation/24-administrative-unit-entra-list-confirmation.png)

![Administrative unit scoped User Administrator assignment](../screenshots/10-role-based-access-delegation/25-administrative-unit-scope-check.png)

![Administrative unit dynamic membership options](../screenshots/10-role-based-access-delegation/26-administrative-unit-dynamic-membership-options.png)

### Privileged Identity Management eligible access

I reviewed PIM access and eligible-role views, opened role assignment management, configured an eligible assignment, and confirmed the resulting temporary-access workflow.

![Privileged Identity Management access overview](../screenshots/10-role-based-access-delegation/27-pim-access-management-overview.png)

![PIM eligible roles validation](../screenshots/10-role-based-access-delegation/28-pim-eligible-roles-validation.png)

![PIM role assignment management](../screenshots/10-role-based-access-delegation/29-pim-role-assignment-management.png)

![PIM eligible assignment configuration](../screenshots/10-role-based-access-delegation/30-pim-eligible-assignment-configuration.png)

![PIM eligible assignment confirmation](../screenshots/10-role-based-access-delegation/31-pim-eligible-assignment-confirmation.png)

## Skills Demonstrated

* Microsoft Entra role review, assignment, and validation
* Microsoft 365 admin center role administration
* Workload-specific role and permission navigation
* Microsoft Purview role group administration
* Administrative unit creation and membership management
* Scoped User Administrator delegation
* PIM-style eligible assignment configuration
* Least-privilege and cross-portal access administration

## Support Relevance

Role management determines what support staff can administer and whether access applies across the tenant or only to a defined scope. Administrative units and eligible assignments provide practical ways to limit permissions while still supporting user and service administration.

## Outcome

Role-based access was reviewed and administered across Microsoft Entra, Microsoft 365, Defender, Intune, Exchange, and Purview. Administrative units provided scoped delegation, and the PIM workflow documented eligible access for temporary administrative responsibilities.
