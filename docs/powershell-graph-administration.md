# PowerShell & Microsoft Graph Administration

This work combines PowerShell administration fundamentals with Microsoft Graph PowerShell workflows for Microsoft 365 and Microsoft Entra.

## Environment

- Windows PowerShell
- Microsoft Graph PowerShell SDK
- Microsoft 365 E5 lab tenant
- Microsoft 365 and Microsoft Entra admin centers
- CSV input for bulk user provisioning

## Work Completed

- Practiced command discovery, event-log formatting, service review, and output handling.
- Installed Microsoft Graph PowerShell and completed delegated tenant authentication.
- Retrieved users and created lab users and groups.
- Reviewed subscribed SKUs and assigned a license.
- Created users from CSV, verified the accounts, and removed the test users after validation.

## Phase 1 — PowerShell Administration Fundamentals

I used command discovery, formatted event-log output, reviewed services with parameters, and redirected process information to a file.

<p align="center">
  <a href="../screenshots/09-powershell-admin-tooling/02-powershell-get-command-by-noun.png"><img src="../screenshots/09-powershell-admin-tooling/02-powershell-get-command-by-noun.png" alt="PowerShell command discovery" width="49%"></a>
  <a href="../screenshots/09-powershell-admin-tooling/06-powershell-output-process-view-processes-file.png"><img src="../screenshots/09-powershell-admin-tooling/06-powershell-output-process-view-processes-file.png" alt="PowerShell output file" width="49%"></a>
</p>

_Left: Get-Command used to locate commands by noun. Right: Process output redirected and reviewed from a file._

## Phase 2 — Microsoft Graph Setup and Connection

I installed the Microsoft Graph PowerShell module and connected to the tenant through delegated authentication.

<p align="center">
  <a href="../screenshots/09-powershell-admin-tooling/12-graph-module-installation-complete.png"><img src="../screenshots/09-powershell-admin-tooling/12-graph-module-installation-complete.png" alt="Graph module installation complete" width="49%"></a>
  <a href="../screenshots/09-powershell-admin-tooling/14-graph-sign-in-successful.png"><img src="../screenshots/09-powershell-admin-tooling/14-graph-sign-in-successful.png" alt="Graph tenant connection" width="49%"></a>
</p>

_Left: The Microsoft Graph module installation completed in PowerShell. Right: The delegated Microsoft Graph connection completed successfully._

## Phase 3 — User, Group, and Licensing Administration

I created and verified a lab user, created a Microsoft 365 group, reviewed subscribed SKUs, and completed a license assignment.

<p align="center">
  <a href="../screenshots/09-powershell-admin-tooling/16-graph-create-user-command-password-redacted.png"><img src="../screenshots/09-powershell-admin-tooling/16-graph-create-user-command-password-redacted.png" alt="Graph user creation" width="49%"></a>
  <a href="../screenshots/09-powershell-admin-tooling/17-graph-created-user-admin-center-verification.png"><img src="../screenshots/09-powershell-admin-tooling/17-graph-created-user-admin-center-verification.png" alt="Graph-created user verified" width="49%"></a>
</p>

_Left: The user creation command with the temporary password redacted. Right: The Graph-created user visible in the admin center._
<p align="center">
  <a href="../screenshots/09-powershell-admin-tooling/18-graph-create-group-command.png"><img src="../screenshots/09-powershell-admin-tooling/18-graph-create-group-command.png" alt="Graph group creation" width="49%"></a>
  <a href="../screenshots/09-powershell-admin-tooling/20-graph-license-review-assignment.png"><img src="../screenshots/09-powershell-admin-tooling/20-graph-license-review-assignment.png" alt="Graph license assignment" width="49%"></a>
</p>

_Left: A Microsoft 365 group created through Microsoft Graph PowerShell. Right: Subscribed SKU review and license assignment through Microsoft Graph._

## Phase 4 — CSV Bulk Provisioning and Cleanup

I created lab users from CSV input, verified the results in the admin center, and removed the test accounts when the workflow was complete.

<p align="center">
  <a href="../screenshots/09-powershell-admin-tooling/22-graph-bulk-user-import-command-password-redacted.png"><img src="../screenshots/09-powershell-admin-tooling/22-graph-bulk-user-import-command-password-redacted.png" alt="Graph bulk user import" width="49%"></a>
  <a href="../screenshots/09-powershell-admin-tooling/23-graph-bulk-users-created-admin-center-verification.png"><img src="../screenshots/09-powershell-admin-tooling/23-graph-bulk-users-created-admin-center-verification.png" alt="Graph bulk users verified" width="49%"></a>
</p>

_Left: The CSV import and user creation command with the password value redacted. Right: The bulk-created users visible in the admin center._
<p align="center">
  <a href="../screenshots/09-powershell-admin-tooling/25-graph-bulk-users-removed-admin-center-verification.png"><img src="../screenshots/09-powershell-admin-tooling/25-graph-bulk-users-removed-admin-center-verification.png" alt="Graph bulk users removed" width="78%"></a>
</p>

_The admin center after removal of the bulk-created test users._

## Troubleshooting Notes

- Tenant sign-in required the correct Microsoft 365 administrator account and password state.
- Write operations required the appropriate Microsoft Graph permission scopes.
- The bulk input had to be saved as CSV so `Import-Csv` could read the headers.
- A failed creation attempt was traced by checking the columns passed to `New-MgUser`.

## Skills Demonstrated

- PowerShell command discovery and output handling
- Microsoft Graph PowerShell installation and delegated authentication
- User and group administration
- Subscribed SKU review and license assignment
- CSV-based bulk user provisioning
- Cross-portal verification and test-account cleanup

## Result

Microsoft Graph PowerShell was used for user, group, licensing, bulk provisioning, verification, troubleshooting, and cleanup workflows in the lab tenant.

The complete screenshot sequence is available in [`screenshots/09-powershell-admin-tooling`](../screenshots/09-powershell-admin-tooling).
