# Group Policy Security Configuration

## 1. Password Policy

Configured via Default Domain Policy:

- Password complexity: Enabled
- Minimum length: 8+ characters
- Maximum age: Configured
- Account lockout threshold: Configured

### Security Purpose

Prevents brute-force and weak credential attacks.



## 2. Control Panel Restriction

Applied to Staff OU:

- Prohibit access to Control Panel and PC Settings

### Security Purpose

Prevents users from modifying system configuration and reducing endpoint security posture.



## Testing Validation

- gpupdate /force executed on CLIENT-01
- Attempted Control Panel access blocked successfully
