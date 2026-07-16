# Screenshot Publishing Notes

The screenshots in this repository use fictional lab users, test contacts, sample guest users, and lab-only configuration objects.

## Kept Visible

- Fictional user names and lab email addresses
- Fictional group and organizational-unit names
- Lab tenant and domain references
- Administrative role names and policy settings
- Authentication-method and password-protection configuration values
- Weak example values used only to demonstrate the custom banned-password control
- Portal warnings, error states, and incomplete conditions that are relevant to the workflow
- Commands and results needed to understand the evidence

## Redacted or Excluded

- Temporary passwords
- Tokens, secrets, private keys, recovery codes, and connection strings
- Real personal information
- Values that could provide access to an active environment
- Duplicate, transitional, or navigation-only screenshots that do not add distinct employer-facing evidence
- Screens that could imply a completed result when no supporting outcome was captured

## Authentication Evidence Notes

Security questions remain visible because the portal itself shows the retirement notice and the screenshots document the control as a legacy setting. SMS policy screenshots show method availability and are not described as MFA enforcement.

Password-writeback screenshots show the tenant settings that were selected and saved. They are not presented as a successful end-to-end reset or writeback test.

Windows Server Active Directory password protection is documented in **Audit** mode because that is the state shown in the evidence. The repository does not describe it as Enforced mode.

## Reasoning

Leaving fictional users and useful configuration values visible makes the evidence easier to review. Redacting only genuine secrets avoids weakening the screenshots or covering the labels, commands, and results that an employer needs to understand the workflow.
