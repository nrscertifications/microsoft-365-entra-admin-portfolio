# User Lifecycle Administration

## Administrative Objective

Provision and validate internal Microsoft 365 users through multiple administrative portals and a CSV-based bulk user workflow.

## Work Completed

* Created internal member users from Microsoft 365 and Entra administration surfaces.
* Reviewed account basics, profile details, password options, account state, user type, and license options.
* Verified created user objects across Microsoft 365, Azure, and Microsoft Entra views.
* Completed and verified CSV-based bulk user provisioning.
* Redacted temporary password output before publishing.

## Evidence Walkthrough

### Microsoft 365 user creation and cross-portal verification

I created an internal user through the Microsoft 365 admin center, reviewed license options, completed the account workflow, and verified the same identity from Azure and Microsoft Entra administration views.

![Microsoft 365 user creation basics](../screenshots/03-user-provisioning/19-m365-admin-user-create-01.png)

![License assignment options during user creation](../screenshots/03-user-provisioning/20-m365-admin-user-create-02.png)

![User creation confirmation](../screenshots/03-user-provisioning/17-m365-admin-user-create-successful-creation-05.png)

![User visible in Azure portal user view](../screenshots/03-user-provisioning/15-m365-admin-user-create-azure-portal-confirmation-07.png)

![User visible in Entra admin center](../screenshots/03-user-provisioning/16-m365-admin-user-create-entra-id-portal-confirmation-07.png)

### Azure and Entra user creation

I also completed the user creation workflow from the Azure and Entra administration surface and confirmed the account was created successfully.

![Azure portal user creation start](../screenshots/03-user-provisioning/24-azure-portal-user-create-01.png)

![Azure portal user creation completed](../screenshots/03-user-provisioning/23-azure-portal-user-create-successful-creation-05.png)

### CSV-based bulk provisioning

I used the Microsoft 365 bulk user workflow to create multiple accounts from structured input, handled the generated temporary password output as sensitive, and verified the new users in the active users list.

![Bulk user provisioning start](../screenshots/03-user-provisioning/01-bulk-user-provisioning-01.png)

![Bulk user provisioning setup](../screenshots/03-user-provisioning/05-bulk-user-provisioning-05.png)

![Bulk user provisioning completed with temporary passwords redacted](../screenshots/03-user-provisioning/13-bulk-user-provisioning-completed-redacted-passwords.png)

![Bulk user provisioning admin center verification](../screenshots/03-user-provisioning/14-bulk-user-provisioning-13-admin-center-verification.png)

## Skills Demonstrated

* Microsoft 365 and Entra user provisioning
* User property and account-state review
* License-option review during account creation
* Cross-portal identity verification
* CSV-based bulk user creation
* Secure handling of temporary credentials

## Support Relevance

User creation affects sign-in, email, licensing, groups, and downstream access. Verifying the identity across portals helps confirm that the account exists and is available for the next administration step.

## Outcome

Internal users were created and verified through Microsoft 365, Azure, and Microsoft Entra administration workflows. The bulk provisioning process was completed and validated with temporary credentials protected in the published evidence.
