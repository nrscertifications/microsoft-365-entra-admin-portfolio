# PowerShell & Microsoft Graph Administration

## Overview

This document captures the command-line administration portion of the Microsoft 365 / Entra ID portfolio. The goal was to move beyond portal-only administration and practice repeatable Microsoft Graph PowerShell workflows for user review, user creation, group creation, license review, license assignment, CSV-based bulk provisioning, and cleanup.

The work was completed in a non-production Microsoft 365 tenant using fictional users and lab-only objects. Temporary password values visible in command examples were redacted before publishing. User names, lab email addresses, and verification results are intentionally visible because they show the workflow clearly for employer review.

## Environment

* Microsoft 365 E5 trial tenant
* Microsoft Entra ID user and group objects
* Microsoft Graph PowerShell SDK
* Windows PowerShell
* Microsoft 365 admin center
* Microsoft Entra admin center
* CSV input for bulk user provisioning

## Scope of Work

* Installed and reviewed Microsoft Graph PowerShell module usage.
* Connected to the Microsoft 365 tenant using delegated Microsoft Graph permissions.
* Reviewed existing tenant users from PowerShell.
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

## Workflow Summary

### 1. Microsoft Graph PowerShell setup

I reviewed the Microsoft Graph PowerShell module installation process and confirmed that the module was available for tenant administration work.

![Microsoft Graph module installation review](../screenshots/09-powershell-admin-tooling/11-graph-module-installation-review.png)

![Microsoft Graph module installation complete](../screenshots/09-powershell-admin-tooling/12-graph-module-installation-complete.png)

### 2. Tenant authentication and permission scopes

I connected to the tenant with Microsoft Graph PowerShell using delegated permissions. This required tenant sign-in and Graph scopes for organization, group, and user administration.

![Microsoft Graph admin sign-in prompt](../screenshots/09-powershell-admin-tooling/13-graph-admin-sign-in-prompt.png)

![Microsoft Graph sign-in successful](../screenshots/09-powershell-admin-tooling/14-graph-sign-in-successful.png)

### 3. User review and single-user creation

After connecting, I reviewed existing users and created a test user through PowerShell. The user was then verified in the Microsoft 365 admin center.

![Microsoft Graph user list review](../screenshots/09-powershell-admin-tooling/15-graph-user-list-review.png)

![Microsoft Graph create user command with temporary password redacted](../screenshots/09-powershell-admin-tooling/16-graph-create-user-command-password-redacted.png)

![Created user verified in Microsoft 365 admin center](../screenshots/09-powershell-admin-tooling/17-graph-created-user-admin-center-verification.png)

### 4. Group creation and portal validation

I created a Microsoft 365 group through Microsoft Graph PowerShell and validated the object in the admin portal. This demonstrated how command-line object creation can be confirmed through the graphical admin interface.

![Microsoft Graph create group command](../screenshots/09-powershell-admin-tooling/18-graph-create-group-command.png)

![Microsoft Graph group verified in admin portal](../screenshots/09-powershell-admin-tooling/19-graph-group-admin-center-verification.png)

### 5. License review and assignment

I reviewed subscribed SKUs, checked consumed units, and assigned a license to a test user through PowerShell. This workflow is relevant to account provisioning and access troubleshooting because license state directly affects available Microsoft 365 services.

![Microsoft Graph license review and assignment](../screenshots/09-powershell-admin-tooling/20-graph-license-review-assignment.png)

### 6. CSV-based bulk user provisioning

I created a CSV input file with display names, mail nicknames, and user principal names. The CSV was imported through PowerShell to create multiple users with consistent attributes.

![CSV review for bulk user provisioning](../screenshots/09-powershell-admin-tooling/21-graph-bulk-user-csv-review.png)

![Microsoft Graph bulk user import command with temporary password redacted](../screenshots/09-powershell-admin-tooling/22-graph-bulk-user-import-command-password-redacted.png)

![Bulk-created users verified in admin portal](../screenshots/09-powershell-admin-tooling/23-graph-bulk-users-created-admin-center-verification.png)

### 7. Cleanup and verification

After validating the bulk-created users, I removed the test accounts through PowerShell and verified that the objects were no longer visible in the active user list. This closed the lab workflow cleanly and demonstrated cleanup discipline.

![CSV-based bulk user removal command](../screenshots/09-powershell-admin-tooling/24-graph-bulk-user-removal-command.png)

![Bulk-created users removed after verification](../screenshots/09-powershell-admin-tooling/25-graph-bulk-users-removed-admin-center-verification.png)

![Microsoft Graph user review and cleanup command](../screenshots/09-powershell-admin-tooling/26-graph-user-review-and-cleanup-command.png)

## Troubleshooting Notes

During the lab, I ran into realistic setup and execution issues:

* Tenant sign-in required the correct Microsoft 365 admin account and password reset before Graph authentication succeeded.
* The permission scope needed to support write operations, not just read-only organization review.
* CSV input needed to be saved as a CSV file, not an Excel workbook, so `Import-Csv` could parse the headers correctly.
* A failed bulk user creation attempt was traced by checking the exact input columns being passed into `New-MgUser`.

## Security and Publishing Notes

* Temporary password values were redacted before publishing screenshots.
* No production customer data or live business records are included.
* The users, groups, and email addresses shown are lab-created objects for portfolio documentation.
* Test objects were removed after the workflow was validated.

## Outcome

Microsoft Graph PowerShell was used to complete user, group, licensing, bulk provisioning, and cleanup workflows in a controlled Microsoft 365 / Entra ID lab tenant. The work demonstrates command-line administration awareness, repeatable provisioning concepts, license troubleshooting awareness, and verification discipline suitable for IT Support, Service Desk, Technical Support, and junior systems administration roles.
