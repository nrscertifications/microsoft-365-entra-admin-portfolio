# Authentication Methods, Self-Service Password Reset & Password Protection

## Administrative Objective

Configure and review Microsoft Entra self-service password reset, authentication methods, password writeback, tenant password settings, smart lockout, custom banned passwords, Windows Server Active Directory password protection, and authentication reporting.

## Work Completed

* Enabled self-service password reset for all users in the lab tenant.
* Configured the available security-question policy and custom question.
* Enabled the SMS authentication method for all users.
* Saved password-writeback settings for synchronized users.
* Reviewed and saved a 60-day tenant password-expiration value.
* Configured smart lockout with a threshold of 10 attempts and a 60-second duration.
* Enabled a custom banned-password list.
* Set Windows Server Active Directory password protection to Audit mode.
* Reviewed authentication capability, registered methods, user registration, and registration and reset event reporting.

## Evidence Walkthrough

### Self-service password reset and security questions

I enabled SSPR for all users and saved the policy. I then reviewed the security-question requirements, selected the predefined questions, added one custom question, and confirmed the saved configuration. The portal retirement notice remains visible in the screenshots.

![SSPR enabled for all users](../screenshots/12-authentication-password-protection/01-self-service-password-reset/01-sspr-enabled-for-all-users.png)

![SSPR policy saved](../screenshots/12-authentication-password-protection/01-self-service-password-reset/02-sspr-policy-save-confirmation.png)

![Security-question requirements and retirement notice](../screenshots/12-authentication-password-protection/01-self-service-password-reset/03-security-question-settings-and-retirement-notice.png)

![Predefined security questions selected](../screenshots/12-authentication-password-protection/01-self-service-password-reset/04-predefined-security-questions-selected.png)

![Custom security question added](../screenshots/12-authentication-password-protection/01-self-service-password-reset/05-custom-security-question-added.png)

![Predefined and custom questions reviewed](../screenshots/12-authentication-password-protection/01-self-service-password-reset/06-security-question-selection-reviewed.png)

![Security-question policy saved](../screenshots/12-authentication-password-protection/01-self-service-password-reset/07-security-question-policy-save-confirmation.png)

### SMS authentication method and password writeback

I enabled SMS for all users and confirmed the policy save. SMS became available as an authentication method. I also selected and saved the on-premises password-writeback options. The Cloud Sync provisioning-agent status remains visible on the saved settings screen for troubleshooting context.

![SMS method initially disabled](../screenshots/12-authentication-password-protection/02-authentication-methods-and-writeback/01-sms-method-initially-disabled.png)

![SMS method enabled for all users](../screenshots/12-authentication-password-protection/02-authentication-methods-and-writeback/02-sms-method-enabled-for-all-users.png)

![SMS method policy saved](../screenshots/12-authentication-password-protection/02-authentication-methods-and-writeback/03-sms-method-policy-save-confirmation.png)

![Password writeback options selected](../screenshots/12-authentication-password-protection/02-authentication-methods-and-writeback/04-password-writeback-options-selected.png)

![Password writeback settings saved with Cloud Sync agent status visible](../screenshots/12-authentication-password-protection/02-authentication-methods-and-writeback/05-password-writeback-settings-saved-with-cloud-sync-agent-error.png)

### Tenant password settings and smart lockout

I reviewed the tenant password-expiration control, saved a 60-day lab value, and configured smart lockout with a 10-attempt threshold and 60-second duration.

![Password expiration set to 60 days](../screenshots/12-authentication-password-protection/03-password-protection/01-password-expiration-set-to-60-days.png)

![Password expiration policy saved](../screenshots/12-authentication-password-protection/03-password-protection/02-password-expiration-policy-save-confirmation.png)

![Smart lockout threshold set to 10](../screenshots/12-authentication-password-protection/03-password-protection/03-smart-lockout-threshold-set-to-10.png)

![Smart lockout duration set to 60 seconds](../screenshots/12-authentication-password-protection/03-password-protection/04-smart-lockout-duration-set-to-60-seconds.png)

### Custom banned passwords and Windows Server AD protection

I enabled a custom banned-password list and set Windows Server Active Directory password protection to Audit mode. Audit mode records banned-password activity for review while the policy is evaluated.

![Custom banned-password list enabled](../screenshots/12-authentication-password-protection/03-password-protection/05-custom-banned-password-list-enabled.png)

![On-premises password protection enabled in Audit mode](../screenshots/12-authentication-password-protection/03-password-protection/06-on-premises-password-protection-audit-mode.png)

![Password protection policy saved](../screenshots/12-authentication-password-protection/03-password-protection/07-password-protection-policy-save-confirmation.png)

### Authentication monitoring and reporting

I reviewed the tenant's authentication capability overview, method-registration chart, user-level registration details, and registration and reset event report.

The capability overview showed 1 of 22 users capable of multifactor authentication, 0 of 22 capable of passwordless authentication, and 1 of 22 capable of self-service password reset. The registered-method chart showed two registrations across Microsoft Authenticator and software token.

![Authentication registration capability overview](../screenshots/12-authentication-password-protection/04-monitoring-and-reporting/01-authentication-registration-capability-overview.png)

![Users registered by authentication method](../screenshots/12-authentication-password-protection/04-monitoring-and-reporting/02-users-registered-by-authentication-method.png)

![User registration details](../screenshots/12-authentication-password-protection/04-monitoring-and-reporting/03-user-registration-details.png)

![Registration and reset events reviewed](../screenshots/12-authentication-password-protection/04-monitoring-and-reporting/04-registration-and-reset-events-review.png)

## Skills Demonstrated

* Microsoft Entra self-service password reset administration
* Authentication-method policy configuration
* SMS authentication-method targeting
* Security-question policy configuration
* Password-writeback setting administration
* Microsoft 365 tenant password-expiration review
* Microsoft Entra smart-lockout configuration
* Custom banned-password policy configuration
* Windows Server Active Directory password protection in Audit mode
* Authentication-method registration and capability reporting

## Support Relevance

Authentication requests can involve password reset scope, method availability, account lockout, synchronized password settings, password protection, or missing registration details. This work shows where those settings and reports are reviewed across Microsoft Entra and Microsoft 365 administration.

## Outcome

The lab tenant was configured with SSPR for all users, security-question settings, SMS method availability, password-writeback options, a 60-day password-expiration value, smart-lockout controls, a custom banned-password list, and Windows Server AD password protection in Audit mode. Authentication registration and event reports were also reviewed.
