# Authentication Methods, Self-Service Password Reset & Password Protection

This work covers Microsoft Entra self-service password reset, authentication-method policy settings, password writeback, password protection, and authentication reporting.

## Work Completed

- Enabled self-service password reset for all users in the lab tenant.
- Configured the available security-question controls and added a custom question.
- Enabled SMS as an authentication method for all users.
- Selected and saved password-writeback options.
- Set the tenant password-expiration value to 60 days for the lab.
- Configured smart lockout with a 10-attempt threshold and 60-second duration.
- Enabled a custom banned-password list.
- Set Windows Server Active Directory password protection to Audit mode.
- Reviewed authentication capability, method registration, user registration, and registration and reset event reports.

## Phase 1 — Self-Service Password Reset and Security Questions

I enabled SSPR for all users and saved the policy. I then reviewed the security-question controls exposed in the tenant, added a custom question, and saved the configuration.

<p align="center">
  <a href="../screenshots/12-authentication-password-protection/01-self-service-password-reset/02-sspr-policy-save-confirmation.png"><img src="../screenshots/12-authentication-password-protection/01-self-service-password-reset/02-sspr-policy-save-confirmation.png" alt="SSPR policy saved" width="49%"></a>
  <a href="../screenshots/12-authentication-password-protection/01-self-service-password-reset/03-security-question-settings-and-retirement-notice.png"><img src="../screenshots/12-authentication-password-protection/01-self-service-password-reset/03-security-question-settings-and-retirement-notice.png" alt="Security-question controls" width="49%"></a>
</p>

_Left: Self-service password reset enabled for all users and saved. Right: The legacy security-question controls exposed in the tenant._
<p align="center">
  <a href="../screenshots/12-authentication-password-protection/01-self-service-password-reset/05-custom-security-question-added.png"><img src="../screenshots/12-authentication-password-protection/01-self-service-password-reset/05-custom-security-question-added.png" alt="Custom security question" width="49%"></a>
  <a href="../screenshots/12-authentication-password-protection/01-self-service-password-reset/07-security-question-policy-save-confirmation.png"><img src="../screenshots/12-authentication-password-protection/01-self-service-password-reset/07-security-question-policy-save-confirmation.png" alt="Security-question policy saved" width="49%"></a>
</p>

_Left: A custom security question added to the available list. Right: The security-question policy save confirmation._

## Phase 2 — SMS Authentication and Password Writeback

I enabled SMS for all users and saved the authentication-method policy. In the password-reset integration settings, I selected both password-writeback options and saved the configuration. The Cloud Sync provisioning-agent status is visible on the saved settings screen.

<p align="center">
  <a href="../screenshots/12-authentication-password-protection/02-authentication-methods-and-writeback/03-sms-method-policy-save-confirmation.png"><img src="../screenshots/12-authentication-password-protection/02-authentication-methods-and-writeback/03-sms-method-policy-save-confirmation.png" alt="SMS policy saved" width="49%"></a>
  <a href="../screenshots/12-authentication-password-protection/02-authentication-methods-and-writeback/05-password-writeback-settings-saved-with-cloud-sync-agent-error.png"><img src="../screenshots/12-authentication-password-protection/02-authentication-methods-and-writeback/05-password-writeback-settings-saved-with-cloud-sync-agent-error.png" alt="Password writeback settings saved" width="49%"></a>
</p>

_Left: The SMS authentication-method policy save confirmation. Right: Both password-writeback options saved with the provisioning-agent status visible._

## Phase 3 — Password Expiration and Smart Lockout

I set the tenant password-expiration value to 60 days and configured smart lockout with a threshold of 10 attempts and a 60-second duration.

<p align="center">
  <a href="../screenshots/12-authentication-password-protection/03-password-protection/02-password-expiration-policy-save-confirmation.png"><img src="../screenshots/12-authentication-password-protection/03-password-protection/02-password-expiration-policy-save-confirmation.png" alt="Password expiration saved" width="49%"></a>
  <a href="../screenshots/12-authentication-password-protection/03-password-protection/04-smart-lockout-duration-set-to-60-seconds.png"><img src="../screenshots/12-authentication-password-protection/03-password-protection/04-smart-lockout-duration-set-to-60-seconds.png" alt="Smart lockout settings" width="49%"></a>
</p>

_Left: The tenant password-expiration policy save confirmation. Right: The smart-lockout threshold and 60-second duration in the policy view._

## Phase 4 — Custom Banned Passwords and Windows Server AD Protection

I enabled the custom banned-password list and set Windows Server Active Directory password protection to Audit mode.

<p align="center">
  <a href="../screenshots/12-authentication-password-protection/03-password-protection/05-custom-banned-password-list-enabled.png"><img src="../screenshots/12-authentication-password-protection/03-password-protection/05-custom-banned-password-list-enabled.png" alt="Custom banned passwords" width="49%"></a>
  <a href="../screenshots/12-authentication-password-protection/03-password-protection/06-on-premises-password-protection-audit-mode.png"><img src="../screenshots/12-authentication-password-protection/03-password-protection/06-on-premises-password-protection-audit-mode.png" alt="Windows Server AD protection in Audit mode" width="49%"></a>
</p>

_Left: The custom banned-password list enabled with lab example values. Right: Windows Server Active Directory password protection set to Audit mode._

## Phase 5 — Authentication Monitoring and Reporting

I reviewed the tenant capability summary, authentication method registration, user-level registration details, and the registration and reset event report.

<p align="center">
  <a href="../screenshots/12-authentication-password-protection/04-monitoring-and-reporting/01-authentication-registration-capability-overview.png"><img src="../screenshots/12-authentication-password-protection/04-monitoring-and-reporting/01-authentication-registration-capability-overview.png" alt="Authentication capability overview" width="49%"></a>
  <a href="../screenshots/12-authentication-password-protection/04-monitoring-and-reporting/03-user-registration-details.png"><img src="../screenshots/12-authentication-password-protection/04-monitoring-and-reporting/03-user-registration-details.png" alt="User registration details" width="49%"></a>
</p>

_Left: The tenant capability and registration summary. Right: The user-level authentication registration report._
<p align="center">
  <a href="../screenshots/12-authentication-password-protection/04-monitoring-and-reporting/04-registration-and-reset-events-review.png"><img src="../screenshots/12-authentication-password-protection/04-monitoring-and-reporting/04-registration-and-reset-events-review.png" alt="Registration and reset events" width="78%"></a>
</p>

_The registration and reset event report view._

## Skills Demonstrated

- Microsoft Entra self-service password reset administration
- Security-question control configuration
- Authentication-method policy configuration
- SMS authentication-method targeting
- Password-writeback settings
- Tenant password-expiration configuration
- Microsoft Entra smart lockout
- Custom banned-password controls
- Windows Server Active Directory password protection in Audit mode
- Authentication registration and event reporting

## Result

The lab tenant was configured with SSPR, security-question controls, SMS availability, password-writeback settings, password expiration, smart lockout, custom banned passwords, and Windows Server Active Directory password protection in Audit mode. Authentication registration and event reports were reviewed from the same administration area.

The complete screenshot sequence is available in [`screenshots/12-authentication-password-protection`](../screenshots/12-authentication-password-protection).
