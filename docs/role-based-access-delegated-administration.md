# Role-Based Access & Delegated Administration

This work covers direct role assignments, workload-specific permission surfaces, Microsoft Purview role groups, administrative-unit scope, and eligible access through Privileged Identity Management.

## Work Completed

- Reviewed role descriptions and permissions before assignment.
- Completed role assignments in Microsoft Entra and the Microsoft 365 admin center.
- Reviewed Exchange, Intune, and Defender permission surfaces.
- Completed a Microsoft Purview role-group assignment.
- Created administrative units, added members, and assigned User Administrator with administrative-unit scope.
- Configured and confirmed an eligible PIM assignment.

## Phase 1 — Microsoft Entra Role Assignment

I reviewed the selected role permissions, assigned the lab user, and confirmed the completed Microsoft Entra role assignment.

<p align="center">
  <a href="../screenshots/10-role-based-access-delegation/03-entra-role-permissions-validation.png"><img src="../screenshots/10-role-based-access-delegation/03-entra-role-permissions-validation.png" alt="Entra role permissions" width="49%"></a>
  <a href="../screenshots/10-role-based-access-delegation/09-entra-role-assignment-success.png"><img src="../screenshots/10-role-based-access-delegation/09-entra-role-assignment-success.png" alt="Entra role assignment complete" width="49%"></a>
</p>

_Left: The permissions included with the selected administrative role. Right: The completed Microsoft Entra role assignment._

## Phase 2 — Microsoft 365 and Workload Permission Surfaces

I completed a role assignment in the Microsoft 365 admin center and reviewed where workload-specific permissions are administered.

<p align="center">
  <a href="../screenshots/10-role-based-access-delegation/12-m365-admin-center-role-assignment-complete.png"><img src="../screenshots/10-role-based-access-delegation/12-m365-admin-center-role-assignment-complete.png" alt="Microsoft 365 role assignment complete" width="49%"></a>
  <a href="../screenshots/10-role-based-access-delegation/15-defender-xdr-permission-surface-validation.png"><img src="../screenshots/10-role-based-access-delegation/15-defender-xdr-permission-surface-validation.png" alt="Defender XDR permissions" width="49%"></a>
</p>

_Left: The completed SharePoint Administrator assignment. Right: The Defender XDR permission-management overview._

## Phase 3 — Microsoft Purview Role Groups

I added the lab member to the selected Microsoft Purview role group and confirmed the assignment.

<p align="center">
  <a href="../screenshots/10-role-based-access-delegation/18-purview-role-group-assignment-workflow.png"><img src="../screenshots/10-role-based-access-delegation/18-purview-role-group-assignment-workflow.png" alt="Purview role-group assignment" width="49%"></a>
  <a href="../screenshots/10-role-based-access-delegation/19-purview-role-group-assignment-confirmation.png"><img src="../screenshots/10-role-based-access-delegation/19-purview-role-group-assignment-confirmation.png" alt="Purview role-group confirmation" width="49%"></a>
</p>

_Left: The member-selection workflow for the Compliance Administrator role group. Right: The completed role-group membership shown in Microsoft Purview._

## Phase 4 — Administrative Units and Scoped Delegation

I created the New York administrative unit with restricted management, added the lab users, and assigned User Administrator with scope limited to that unit.

<p align="center">
  <a href="../screenshots/10-role-based-access-delegation/22-administrative-unit-restricted-management-confirmation.png"><img src="../screenshots/10-role-based-access-delegation/22-administrative-unit-restricted-management-confirmation.png" alt="Restricted administrative unit" width="49%"></a>
  <a href="../screenshots/10-role-based-access-delegation/25-administrative-unit-scope-check.png"><img src="../screenshots/10-role-based-access-delegation/25-administrative-unit-scope-check.png" alt="Scoped User Administrator assignment" width="49%"></a>
</p>

_Left: The New York administrative unit with restricted management enabled. Right: The User Administrator role assignment limited to the New York administrative unit._

## Phase 5 — Privileged Identity Management Eligible Access

I configured an eligible role assignment with a defined schedule and confirmed the assignment in Microsoft Entra.

<p align="center">
  <a href="../screenshots/10-role-based-access-delegation/30-pim-eligible-assignment-configuration.png"><img src="../screenshots/10-role-based-access-delegation/30-pim-eligible-assignment-configuration.png" alt="PIM eligible assignment configuration" width="49%"></a>
  <a href="../screenshots/10-role-based-access-delegation/31-pim-eligible-assignment-confirmation.png"><img src="../screenshots/10-role-based-access-delegation/31-pim-eligible-assignment-confirmation.png" alt="PIM eligible assignment confirmed" width="49%"></a>
</p>

_Left: The eligible assignment type and schedule settings. Right: The resulting eligible assignment in Microsoft Entra._

## Skills Demonstrated

- Microsoft Entra and Microsoft 365 role assignment
- Workload-specific permission navigation
- Microsoft Purview role-group administration
- Administrative-unit creation and membership management
- Scoped User Administrator delegation
- Privileged Identity Management eligible assignments
- Cross-portal access administration

## Result

Administrative access was assigned and reviewed across the Microsoft 365 permission surfaces. Administrative units limited User Administrator scope, and PIM was used to configure eligible access.

The complete screenshot sequence is available in [`screenshots/10-role-based-access-delegation`](../screenshots/10-role-based-access-delegation).
