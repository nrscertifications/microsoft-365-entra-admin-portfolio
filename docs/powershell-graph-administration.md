# PowerShell & Microsoft Graph Administration

## Administrative Objective

Use PowerShell and Microsoft Graph PowerShell for repeatable Microsoft 365 and Microsoft Entra administration, verification, and cleanup.

## Environment

* Microsoft 365 E5 trial tenant
* Microsoft Entra user and group objects
* Microsoft Graph PowerShell SDK
* Windows PowerShell
* Microsoft 365 and Microsoft Entra admin centers
* CSV input for bulk user provisioning

## Work Completed

* Practiced PowerShell command discovery, event, process, service, variable, output, and execution-policy workflows.
* Installed and connected Microsoft Graph PowerShell with delegated permissions.
* Retrieved users and created test users and groups.
* Reviewed subscribed SKUs and assigned a license.
* Created users from CSV and verified the results.
* Removed the bulk-created test accounts after validation.
* Redacted temporary passwords before publishing.

## Evidence Walkthrough

### PowerShell administration fundamentals

I practiced command discovery, formatted administrative output, reviewed processes and services, redirected output to a file, checked execution policy, and used variables before moving into Microsoft Graph administration.

![PowerShell Get-Command by noun](../screenshots/09-powershell-admin-tooling/02-powershell-get-command-by-noun.png)

![PowerShell event log formatted output](../screenshots/09-powershell-admin-tooling/03-powershell-get-eventlog-format-as-list.png)

![PowerShell Get-Process](../screenshots/09-powershell-admin-tooling/04-powershell-get-process.png)

![PowerShell Get-Service with parameter](../screenshots/09-powershell-admin-tooling/05-powershell-get-service-with-parameter-with-service.png)

![PowerShell output process view to file](../screenshots/09-powershell-admin-tooling/06-powershell-output-process-view-processes-file.png)

![PowerShell execution policy awareness](../screenshots/09-powershell-admin-tooling/07-powershell-set-executionpolicies-bypassing-restricting.png)

![PowerShell variable calculations](../screenshots/09-powershell-admin-tooling/09-powershell-variable-calculations.png)

### Microsoft Graph setup and tenant connection

I installed the Microsoft Graph PowerShell module, started delegated tenant sign-in, and confirmed the connected session before running directory commands.

![Microsoft Graph module installation validation](../screenshots/09-powershell-admin-tooling/11-graph-module-installation-review.png)

![Microsoft Graph module installation complete](../screenshots/09-powershell-admin-tooling/12-graph-module-installation-complete.png)

![Microsoft Graph admin sign-in prompt](../screenshots/09-powershell-admin-tooling/13-graph-admin-sign-in-prompt.png)

![Microsoft Graph sign-in successful](../screenshots/09-powershell-admin-tooling/14-graph-sign-in-successful.png)

### User, group, and licensing administration

I retrieved tenant users, created and verified a test user, created and verified a Microsoft 365 group, and completed a license review and assignment workflow.

![Microsoft Graph user list review](../screenshots/09-powershell-admin-tooling/15-graph-user-list-review.png)

![Microsoft Graph create user command with temporary password redacted](../screenshots/09-powershell-admin-tooling/16-graph-create-user-command-password-redacted.png)

![Created user verified in Microsoft 365 admin center](../screenshots/09-powershell-admin-tooling/17-graph-created-user-admin-center-verification.png)

![Microsoft Graph create group command](../screenshots/09-powershell-admin-tooling/18-graph-create-group-command.png)

![Microsoft Graph group verified in admin portal](../screenshots/09-powershell-admin-tooling/19-graph-group-admin-center-verification.png)

![Microsoft Graph license review and assignment](../screenshots/09-powershell-admin-tooling/20-graph-license-review-assignment.png)

### CSV bulk provisioning and cleanup

I prepared a CSV, created multiple users through Microsoft Graph PowerShell, verified the accounts in the admin center, and removed the test users after the workflow was complete.

![CSV review for bulk user provisioning](../screenshots/09-powershell-admin-tooling/21-graph-bulk-user-csv-review.png)

![Microsoft Graph bulk user import command with temporary password redacted](../screenshots/09-powershell-admin-tooling/22-graph-bulk-user-import-command-password-redacted.png)

![Bulk-created users verified in admin portal](../screenshots/09-powershell-admin-tooling/23-graph-bulk-users-created-admin-center-verification.png)

![CSV-based bulk user removal command](../screenshots/09-powershell-admin-tooling/24-graph-bulk-user-removal-command.png)

![Bulk-created users removed after verification](../screenshots/09-powershell-admin-tooling/25-graph-bulk-users-removed-admin-center-verification.png)

![Microsoft Graph user review and cleanup command](../screenshots/09-powershell-admin-tooling/26-graph-user-review-and-cleanup-command.png)

## Troubleshooting Notes

* Tenant sign-in required the correct Microsoft 365 administrator account and password state.
* Write operations required the appropriate Microsoft Graph permission scopes.
* The bulk input needed to be saved as CSV so `Import-Csv` could read the headers.
* A failed creation attempt was traced by checking the columns passed to `New-MgUser`.

## Skills Demonstrated

* PowerShell command discovery and output handling
* Microsoft Graph PowerShell installation and delegated authentication
* User and group administration
* Subscribed SKU review and license assignment
* CSV-based bulk user provisioning
* Cross-portal verification and test-account cleanup

## Support Relevance

PowerShell and Microsoft Graph support repeatable provisioning, reporting, licensing checks, validation, and cleanup. The workflow connects command-line administration with verification in the Microsoft 365 admin centers.

## Outcome

Microsoft Graph PowerShell was used for user, group, licensing, bulk provisioning, verification, troubleshooting, and cleanup workflows in the lab tenant.
