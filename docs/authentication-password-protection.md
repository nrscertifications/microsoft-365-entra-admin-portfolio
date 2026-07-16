# Authentication Methods, Self-Service Password Reset & Password Protection

## Administrative Objective

Configure and review Microsoft Entra authentication methods, self-service password reset, password writeback, tenant password-expiration settings, smart lockout, custom banned passwords, Windows Server Active Directory password protection, and authentication reporting in a non-production tenant.

The work is documented as a support and administration workflow. A saved policy proves that the setting was configured in the portal; it does not automatically prove that an end user completed a password reset, that password writeback succeeded end to end, or that every user was registered for the method.

---

## Work Completed

- Enabled self-service password reset for all users in the lab tenant.
- Reviewed the security-question settings available for SSPR and the portal notice that security questions are retiring in March 2027.
- Configured the lab security-question policy with one authentication method required, five questions required for registration, three questions required for reset, ten predefined questions, and one custom question.
- Enabled the SMS authentication method for all users and confirmed that the policy saved.
- Enabled password writeback settings for synchronized users through Microsoft Entra Connect Sync and Microsoft Entra Cloud Sync.
- Reviewed the tenant-wide password-expiration control in Microsoft 365 admin center and saved a 60-day lab value while retaining the portal recommendation for non-expiring passwords in the evidence.
- Configured smart lockout with a threshold of 10 failed sign-ins and a 60-second lockout duration.
- Enabled a custom banned-password list using weak lab examples.
- Enabled password protection for Windows Server Active Directory in **Audit** mode.
- Reviewed authentication capability, registered-method, user-registration, and registration/reset-event reporting.

---

## Evidence Walkthrough

### 1. Enabled self-service password reset

I changed the SSPR scope from a limited selection to **All** users and saved the policy.

![SSPR enabled for all users](../screenshots/12-authentication-password-protection/01-self-service-password-reset/01-sspr-enabled-for-all-users.png)

![SSPR policy saved](../screenshots/12-authentication-password-protection/01-self-service-password-reset/02-sspr-policy-save-confirmation.png)

This confirms the tenant policy scope and save result. It does not show an end-user password-reset test.

### 2. Reviewed the SSPR security-question settings

The authentication-method page showed one method required for reset, five questions required for registration, and three questions required for reset. The same screen displayed Microsoft's notice that security questions are retiring in March 2027.

![Security-question requirements and retirement notice](../screenshots/12-authentication-password-protection/01-self-service-password-reset/03-security-question-settings-and-retirement-notice.png)

I reviewed the predefined list, added one custom question, and confirmed the combined selection.

![Predefined security questions selected](../screenshots/12-authentication-password-protection/01-self-service-password-reset/04-predefined-security-questions-selected.png)

![Custom security question added](../screenshots/12-authentication-password-protection/01-self-service-password-reset/05-custom-security-question-added.png)

![Predefined and custom questions reviewed](../screenshots/12-authentication-password-protection/01-self-service-password-reset/06-security-question-selection-reviewed.png)

The final policy showed 11 selected questions and saved successfully.

![Security-question policy saved](../screenshots/12-authentication-password-protection/01-self-service-password-reset/07-security-question-policy-save-confirmation.png)

These screenshots document the legacy security-question controls exposed in the tenant. The portfolio does not present security questions as the preferred long-term authentication method.

### 3. Enabled the SMS authentication method

The authentication-method policy initially showed SMS as disabled.

![SMS method initially disabled](../screenshots/12-authentication-password-protection/02-authentication-methods-and-writeback/01-sms-method-initially-disabled.png)

I enabled SMS and targeted the method to all users, then confirmed that the policy saved and the method list showed SMS as enabled.

![SMS method enabled for all users](../screenshots/12-authentication-password-protection/02-authentication-methods-and-writeback/02-sms-method-enabled-for-all-users.png)

![SMS method policy saved](../screenshots/12-authentication-password-protection/02-authentication-methods-and-writeback/03-sms-method-policy-save-confirmation.png)

This makes SMS available as an authentication method. It does not enforce MFA by itself and does not prove that every user registered a phone number.

### 4. Configured password writeback settings

Under Password reset > On-premises integration, I enabled password writeback for synchronized users and selected the Cloud Sync writeback option.

![Password writeback options selected](../screenshots/12-authentication-password-protection/02-authentication-methods-and-writeback/04-password-writeback-options-selected.png)

The settings saved successfully. The same screen still showed an error for the Cloud Sync provisioning agent, so the evidence is presented as a tenant-setting change rather than a successful end-to-end Cloud Sync password-writeback test.

![Password writeback settings saved with Cloud Sync agent error visible](../screenshots/12-authentication-password-protection/02-authentication-methods-and-writeback/05-password-writeback-settings-saved-with-cloud-sync-agent-error.png)

The option to unlock an account without resetting the password remained disabled.

### 5. Reviewed tenant password-expiration settings

In Microsoft 365 admin center, I set the tenant-wide password-expiration value to 60 days and saved it.

![Password expiration set to 60 days](../screenshots/12-authentication-password-protection/03-password-protection/01-password-expiration-set-to-60-days.png)

![Password expiration policy saved](../screenshots/12-authentication-password-protection/03-password-protection/02-password-expiration-policy-save-confirmation.png)

The portal also displayed its recommendation to set passwords to never expire. The 60-day value is documented as the lab configuration selected during this workflow, not as a general security recommendation.

### 6. Configured Microsoft Entra password protection

The smart-lockout settings were reviewed at:

- **Lockout threshold:** 10 failed sign-ins
- **Lockout duration:** 60 seconds

![Smart lockout threshold set to 10](../screenshots/12-authentication-password-protection/03-password-protection/03-smart-lockout-threshold-set-to-10.png)

![Smart lockout duration set to 60 seconds](../screenshots/12-authentication-password-protection/03-password-protection/04-smart-lockout-duration-set-to-60-seconds.png)

I enabled the custom banned-password list and entered weak lab examples so the control could be reviewed visibly.

![Custom banned-password list enabled](../screenshots/12-authentication-password-protection/03-password-protection/05-custom-banned-password-list-enabled.png)

Password protection for Windows Server Active Directory was enabled in **Audit** mode. In this mode, attempts involving banned passwords are logged rather than blocked.

![On-premises password protection enabled in Audit mode](../screenshots/12-authentication-password-protection/03-password-protection/06-on-premises-password-protection-audit-mode.png)

The completed configuration saved successfully.

![Password protection policy saved](../screenshots/12-authentication-password-protection/03-password-protection/07-password-protection-policy-save-confirmation.png)

The evidence does not present the on-premises policy as Enforced mode and does not include a password-change test against the banned-password list.

### 7. Reviewed authentication monitoring and reporting

The authentication activity page showed the tenant's current registration state:

- 1 of 22 users capable of multifactor authentication
- 0 of 22 users capable of passwordless authentication
- 1 of 22 users capable of self-service password reset

![Authentication registration capability overview](../screenshots/12-authentication-password-protection/04-monitoring-and-reporting/01-authentication-registration-capability-overview.png)

The registered-method chart showed two method registrations across Microsoft Authenticator and software token.

![Users registered by authentication method](../screenshots/12-authentication-password-protection/04-monitoring-and-reporting/02-users-registered-by-authentication-method.png)

The user-registration detail view provided user-level MFA, passwordless, SSPR, default-method, and registered-method columns.

![User registration details](../screenshots/12-authentication-password-protection/04-monitoring-and-reporting/03-user-registration-details.png)

The registration and reset event page returned no results for the selected period.

![Registration and reset events reviewed](../screenshots/12-authentication-password-protection/04-monitoring-and-reporting/04-registration-and-reset-events-review.png)

The reporting evidence records the tenant's current state. It does not claim that the policy changes automatically made all users MFA-capable, passwordless-capable, or SSPR-capable.

---

## Evidence Boundaries

| Configuration or observation | What the evidence proves | What it does not prove |
|---|---|---|
| SSPR set to All and saved | The tenant SSPR scope was configured and saved | A user completed a self-service reset |
| SMS enabled for All users | SMS was made available as an authentication method | MFA was enforced or every user registered SMS |
| Password writeback settings saved | The portal accepted the writeback configuration | A password was written back successfully to either forest |
| Cloud Sync agent showed an error | The agent was not healthy on the captured screen | That Connect Sync was also failing |
| Password expiration set to 60 days | The tenant-wide lab value was saved | That 60-day expiration is Microsoft's preferred practice |
| Windows Server AD protection set to Audit | Banned-password attempts would be logged for review | Banned passwords were actively blocked |
| Registration reports reviewed | The current user capability and method-registration state was visible | All tenant users were registered or protected by the methods |

---

## Skills Demonstrated

- Microsoft Entra self-service password reset administration
- Authentication-method policy configuration
- SMS authentication-method targeting
- Security-question policy review and retirement-awareness documentation
- Microsoft Entra Connect password-writeback setting review
- Microsoft 365 tenant password-expiration control review
- Microsoft Entra smart-lockout configuration
- Custom banned-password policy configuration
- Windows Server Active Directory password-protection Audit mode
- Authentication-method registration and capability reporting
- Evidence-based documentation that separates saved settings from end-to-end validation

---

## Support Relevance

Authentication issues often arrive as ordinary support requests: a user cannot reset a password, a registered method is missing, an account locks repeatedly, a synchronized password does not appear on-premises, or a policy is enabled but the user is not registered.

This work shows where those conditions are reviewed across Microsoft Entra authentication-method policies, SSPR settings, Microsoft 365 password controls, on-premises integration, password protection, and registration reporting.

The scope is appropriate for IT support and junior administration work. It demonstrates how to check policy scope, save results, method availability, agent health, reporting state, and the difference between a configured control and a verified user outcome.

---

## Outcome

The non-production tenant was configured with SSPR for all users, a reviewed legacy security-question policy, SMS method availability, password-writeback settings, a 60-day lab password-expiration value, smart-lockout controls, a custom banned-password list, and Windows Server AD password protection in Audit mode.

Authentication reports were reviewed to confirm the tenant's actual registration state. The documentation does not claim an end-user password reset, successful password writeback event, enforced on-premises banned-password blocking, or full-user registration where the screenshots do not show those results.
