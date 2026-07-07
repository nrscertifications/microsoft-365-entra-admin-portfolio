# User Lifecycle Administration

## Administrative Objective

Provision and validate internal Microsoft 365 users using multiple administrative portals while keeping a clear distinction between account creation, license assignment, role assignment, account state, and post-creation verification.

This section demonstrates user lifecycle administration from both portal-based and bulk-provisioning perspectives.

---

## Work Completed

* Created internal member users from the Microsoft 365 admin center.
* Created users from Azure / Microsoft Entra administrative surfaces.
* Checked account basics, profile details, password options, account enabled state, and user type during provisioning.
* Checked license assignment options during user creation without presenting the work as purchasing or billing administration.
* Verified created user objects in Microsoft 365 active users and Microsoft Entra user listings.
* Completed a CSV-based bulk user provisioning workflow in the Microsoft 365 admin center.
* Verified bulk-created users after provisioning.
* Treated temporary password output as sensitive and used redacted evidence where required.

---

## Evidence Walkthrough

### 1. Created a user from the Microsoft 365 admin center

A new internal user was created through the Microsoft 365 admin center to demonstrate standard user provisioning from the primary admin portal.

![Microsoft 365 user creation basics](../screenshots/03-user-provisioning/19-m365-admin-user-create-01.png)

### 2. Checked license assignment options during user creation

License assignment options were checked during account creation to understand where service access can be assigned or deferred.

![License assignment options during user creation](../screenshots/03-user-provisioning/20-m365-admin-user-create-02.png)

### 3. Completed the Microsoft 365 user creation workflow

The user creation workflow was completed and the account was created successfully.

![User creation confirmation](../screenshots/03-user-provisioning/17-m365-admin-user-create-successful-creation-05.png)

### 4. Validated the created user from the Azure portal view

The created user was checked from the Azure portal / Entra-related view to confirm the identity object was visible outside the Microsoft 365 admin center.

![User visible in Azure portal user view](../screenshots/03-user-provisioning/15-m365-admin-user-create-azure-portal-confirmation-07.png)

### 5. Validated the created user from Microsoft Entra admin center

The same user object was confirmed from the Microsoft Entra admin center, showing that portal-based creation still results in an Entra identity object.

![User visible in Entra admin center](../screenshots/03-user-provisioning/16-m365-admin-user-create-entra-id-portal-confirmation-07.png)

### 6. Created a user through the Azure / Entra user workflow

A user creation workflow was also completed from the Azure / Entra administrative surface to compare portal behavior.

![Azure portal user creation start](../screenshots/03-user-provisioning/24-azure-portal-user-create-01.png)

### 7. Completed Azure / Entra user creation

The Azure / Entra user creation workflow completed successfully, confirming another valid path for user provisioning.

![Azure portal user creation completed](../screenshots/03-user-provisioning/23-azure-portal-user-create-successful-creation-05.png)

### 8. Started CSV-based bulk user provisioning

The Microsoft 365 bulk user provisioning workflow was started to demonstrate account creation for multiple users using structured input.

![Bulk user provisioning start](../screenshots/03-user-provisioning/01-bulk-user-provisioning-01.png)

### 9. Continued bulk user provisioning setup

The bulk user provisioning workflow was continued through the Microsoft 365 admin center upload and setup screens.

![Bulk user provisioning setup](../screenshots/03-user-provisioning/05-bulk-user-provisioning-05.png)

### 10. Completed bulk user provisioning with temporary passwords redacted

The bulk user provisioning workflow completed and generated account output. Temporary passwords were redacted before publishing.

![Bulk user provisioning completed with temporary passwords redacted](../screenshots/03-user-provisioning/13-bulk-user-provisioning-completed-redacted-passwords.png)

### 11. Verified bulk-created users in the active users list

The bulk-created accounts were verified in the Microsoft 365 active users list instead of assuming the upload completed correctly.

![Bulk user provisioning admin center verification](../screenshots/03-user-provisioning/14-bulk-user-provisioning-13-admin-center-verification.png)

---

## Controls Observed

* Standard users were not granted administrative roles by default.
* License assignment was treated separately from identity creation.
* Account creation was followed by verification in Microsoft 365 and Entra views.
* Bulk provisioning output was handled as sensitive because temporary credentials can be generated during the workflow.
* Screenshots were organized to show creation, validation, and verification rather than only final results.

---

## Support Relevance

User lifecycle administration is a common service desk, IT support, and junior administrator responsibility.

Correct user creation affects sign-in, mailbox access, Microsoft 365 app access, licensing, security defaults, group membership, and downstream collaboration access. Verifying the user object across portals helps avoid confusion when an account appears in one admin surface but must be supported from another.

---

## Outcome

Internal users were created and verified across Microsoft 365, Azure, and Microsoft Entra administrative views.

Manual provisioning and CSV-based bulk provisioning were completed and documented with public-safe screenshot evidence. This demonstrates practical exposure to account creation, post-creation validation, and basic onboarding workflow discipline.
