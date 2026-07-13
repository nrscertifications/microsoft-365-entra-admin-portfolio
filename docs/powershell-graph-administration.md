# PowerShell & Microsoft Graph Administration

## Administrative Objective

Build and document a command-line administration track for Microsoft 365 and Microsoft Entra ID using PowerShell and Microsoft Graph PowerShell.

This section demonstrates repeatable administration workflows for command discovery, user review, user creation, group creation, license review, license assignment, CSV-based bulk provisioning, verification, and cleanup.

---

## Environment

* Microsoft 365 E5 trial tenant
* Microsoft Entra ID user and group objects
* Microsoft Graph PowerShell SDK
* Windows PowerShell
* Microsoft 365 admin center
* Microsoft Entra admin center
* CSV input for bulk user provisioning

---

## Work Completed

* Practiced PowerShell command discovery, process review, service review, formatting, variables, output handling, and execution policy awareness.
* Installed and validated Microsoft Graph PowerShell module usage.
* Connected to the Microsoft 365 tenant using delegated Microsoft Graph permissions.
* Retrieved existing tenant users from PowerShell.
* Created a test user through Microsoft Graph PowerShell.
* Verified the created user in the Microsoft 365 admin center.
* Created a Microsoft 365 group through Microsoft Graph PowerShell.
* Verified the group in the admin portal.
* Reviewed subscribed SKUs and consumed license units.
* Assigned a license to a test user through PowerShell.
* Created a CSV file for bulk user provisioning.
* Imported users from CSV using Microsoft Graph PowerShell.
* Verified bulk-created users in the admin center.
* Removed bulk-created test users through PowerShell after validation.
* Redacted temporary password values before publishing screenshots.

---

## Evidence Walkthrough

### 1. Practiced command discovery with PowerShell

PowerShell command discovery was practiced to understand how cmdlets can be found by noun and used for administration tasks.

![PowerShell Get-Command by noun](../screenshots/09-powershell-admin-tooling/02-powershell-get-command-by-noun.png)

### 2. Retrieved and formatted event log output

Event log output was retrieved and formatted for structured review of administrative results.

![PowerShell event log formatted output](../screenshots/09-powershell-admin-tooling/03-powershell-get-eventlog-format-as-list.png)

### 3. Retrieved process information

Process information was retrieved from PowerShell to review basic system activity.

![PowerShell Get-Process](../screenshots/09-powershell-admin-tooling/04-powershell-get-process.png)

### 4. Retrieved service information with parameters

Service information was retrieved with PowerShell parameters for a targeted system service review.

![PowerShell Get-Service with parameter](../screenshots/09-powershell-admin-tooling/05-powershell-get-service-with-parameter-with-service.png)

### 5. Exported process output to a file

Process output was redirected to a file to demonstrate command output handling and documentation-friendly evidence capture.

![PowerShell output process view to file](../screenshots/09-powershell-admin-tooling/06-powershell-output-process-view-processes-file.png)

### 6. Checked execution policy behavior

Execution policy behavior was reviewed to understand script execution controls in a PowerShell environment.

![PowerShell execution policy awareness](../screenshots/09-powershell-admin-tooling/07-powershell-set-executionpolicies-bypassing-restricting.png)

### 7. Practiced variables and calculation output

Variables and calculation output were practiced to build command-line familiarity before moving into Microsoft Graph administration.

![PowerShell variable calculations](../screenshots/09-powershell-admin-tooling/09-powershell-variable-calculations.png)

### 8. Installed and validated Microsoft Graph PowerShell

The Microsoft Graph PowerShell module was installed and validated for tenant administration work.

![Microsoft Graph module installation validation](../screenshots/09-powershell-admin-tooling/11-graph-module-installation-review.png)

### 9. Confirmed Microsoft Graph module installation

The module installation completed successfully before connecting to the tenant.

![Microsoft Graph module installation complete](../screenshots/09-powershell-admin-tooling/12-graph-module-installation-complete.png)

### 10. Started Microsoft Graph tenant sign-in

The tenant sign-in prompt was started for delegated Microsoft Graph authentication.

![Microsoft Graph admin sign-in prompt](../screenshots/09-powershell-admin-tooling/13-graph-admin-sign-in-prompt.png)

### 11. Confirmed successful Microsoft Graph sign-in

Microsoft Graph authentication completed successfully, confirming the command-line session was connected to the tenant.

![Microsoft Graph sign-in successful](../screenshots/09-powershell-admin-tooling/14-graph-sign-in-successful.png)

### 12. Retrieved tenant users through Microsoft Graph PowerShell

Existing tenant users were retrieved through Microsoft Graph PowerShell to confirm read access and command output.

![Microsoft Graph user list review](../screenshots/09-powershell-admin-tooling/15-graph-user-list-review.png)

### 13. Created a test user through Microsoft Graph PowerShell

A test user was created from the command line using Microsoft Graph PowerShell. Temporary password values were redacted before publishing.

![Microsoft Graph create user command with temporary password redacted](../screenshots/09-powershell-admin-tooling/16-graph-create-user-command-password-redacted.png)

### 14. Verified the created user in Microsoft 365 admin center

The Graph-created user was verified from the Microsoft 365 admin center to confirm cross-portal validation.

![Created user verified in Microsoft 365 admin center](../screenshots/09-powershell-admin-tooling/17-graph-created-user-admin-center-verification.png)

### 15. Created a Microsoft 365 group through Microsoft Graph PowerShell

A Microsoft 365 group was created using Microsoft Graph PowerShell to demonstrate command-line group administration.

![Microsoft Graph create group command](../screenshots/09-powershell-admin-tooling/18-graph-create-group-command.png)

### 16. Verified the Graph-created group in the admin portal

The group created from PowerShell was verified in the Microsoft 365 admin portal.

![Microsoft Graph group verified in admin portal](../screenshots/09-powershell-admin-tooling/19-graph-group-admin-center-verification.png)

### 17. Reviewed licensing and assigned a license through PowerShell

Subscribed SKUs and consumed license units were reviewed, and a license assignment workflow was completed through PowerShell.

![Microsoft Graph license review and assignment](../screenshots/09-powershell-admin-tooling/20-graph-license-review-assignment.png)

### 18. Prepared a CSV file for bulk user provisioning

A CSV input file was prepared with user attributes for repeatable bulk provisioning.

![CSV review for bulk user provisioning](../screenshots/09-powershell-admin-tooling/21-graph-bulk-user-csv-review.png)

### 19. Imported users from CSV through Microsoft Graph PowerShell

The CSV file was imported through PowerShell to create multiple users with consistent attributes. Temporary password values were redacted before publishing.

![Microsoft Graph bulk user import command with temporary password redacted](../screenshots/09-powershell-admin-tooling/22-graph-bulk-user-import-command-password-redacted.png)

### 20. Verified bulk-created users in the admin portal

Bulk-created users were verified in the Microsoft 365 admin center after the import completed.

![Bulk-created users verified in admin portal](../screenshots/09-powershell-admin-tooling/23-graph-bulk-users-created-admin-center-verification.png)

### 21. Removed bulk-created test users through PowerShell

The bulk-created test users were removed through PowerShell after validation to close the lab workflow cleanly.

![CSV-based bulk user removal command](../screenshots/09-powershell-admin-tooling/24-graph-bulk-user-removal-command.png)

### 22. Verified bulk-created users were removed

The active user list was checked to confirm that bulk-created test accounts were removed after the cleanup workflow.

![Bulk-created users removed after verification](../screenshots/09-powershell-admin-tooling/25-graph-bulk-users-removed-admin-center-verification.png)

### 23. Reviewed final cleanup command output

Final command output was reviewed after cleanup to confirm the PowerShell workflow ended cleanly.

![Microsoft Graph user review and cleanup command](../screenshots/09-powershell-admin-tooling/26-graph-user-review-and-cleanup-command.png)

---

## Troubleshooting Notes

During the lab, realistic setup and execution issues were encountered and resolved:

* Tenant sign-in required the correct Microsoft 365 admin account and password reset before Graph authentication succeeded.
* Permission scopes needed to support write operations, not only read-only organization review.
* CSV input needed to be saved as a `.csv` file, not an Excel workbook, so `Import-Csv` could parse the headers correctly.
* A failed bulk user creation attempt was traced by checking the exact input columns being passed into `New-MgUser`.

---

## Security and Publishing Notes

* Temporary password values were redacted before publishing screenshots.
* No production customer data or live business records are included.
* Users, groups, and email addresses shown are lab-created objects for portfolio documentation.
* Test objects were removed after the workflow was validated.

---

## Support Relevance

PowerShell and Microsoft Graph are useful in support and junior administration work because they support repeatable provisioning, reporting, validation, licensing checks, and cleanup tasks.

This workflow connects portal-based Microsoft 365 administration with command-line administration while still showing verification in the graphical admin centers.

---

## Outcome

Microsoft Graph PowerShell was used to complete user, group, licensing, bulk provisioning, verification, and cleanup workflows in a controlled Microsoft 365 / Entra ID lab tenant.

The work demonstrates command-line administration awareness, repeatable provisioning concepts, license troubleshooting awareness, and verification discipline suitable for IT Support, Service Desk, Technical Support, and junior systems administration roles.
