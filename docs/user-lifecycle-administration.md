# User Lifecycle Administration

## Administrative Objective

Provision and validate internal Microsoft 365 users using multiple administrative portals while keeping a clear distinction between account creation, license assignment, role assignment, account state, and post-creation verification.

## Work Completed

* Created internal member users from the Microsoft 365 admin center.
* Created users from Azure / Entra administration surfaces.
* Validated account basics, profile details, password options, account enabled state, and user type.
* Checked product license assignment options during account creation.
* Verified user objects in active users and Entra user listings.
* Completed a bulk user provisioning workflow using the Microsoft 365 admin center.

## Support Relevance

User lifecycle administration is a common service desk and IT support responsibility. Correct account creation affects sign-in, email access, Microsoft 365 app access, licensing, security defaults, and downstream group membership.

## Evidence

![Microsoft 365 user creation basics](../screenshots/03-user-provisioning/19-m365-admin-user-create-01.png)

![License assignment review during user creation](../screenshots/03-user-provisioning/20-m365-admin-user-create-02.png)

![User creation confirmation](../screenshots/03-user-provisioning/17-m365-admin-user-create-successful-creation-05.png)

![Active users verification](../screenshots/03-user-provisioning/14-bulk-user-provisioning-13-admin-center-verification.png)

![Bulk user provisioning result with temporary passwords redacted](../screenshots/03-user-provisioning/13-bulk-user-provisioning-completed-redacted-passwords.png)

## Controls Observed

* Standard users were not granted administrative roles by default.
* License assignment was reviewed separately from identity creation.
* Post-creation verification was performed rather than assuming successful creation after submission.
* Bulk provisioning output was handled as sensitive because temporary credentials are generated during the workflow.

## Outcome

Internal users were created and verified across Microsoft 365 and Entra ID views. Bulk provisioning was completed and documented with public-safe screenshot evidence.
