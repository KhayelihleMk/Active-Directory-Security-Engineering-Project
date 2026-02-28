# Group Policy Security Hardening

This project implemented multiple layered security controls using Group Policy Objects (GPOs) to simulate enterprise endpoint hardening.

---

# 1. Domain Password & Lockout Policy

Configured via Default Domain Policy.

## Settings Implemented

- Password complexity: Enabled
- Minimum password length: 8+ characters
- Account lockout threshold: Configured
- Account lockout duration: Configured
- Reset lockout counter after: Configured

## Security Objective

- Mitigate brute-force attacks
- Enforce strong authentication standards
- Reduce credential compromise risk

---

# 2. Staff Endpoint Restrictions (User-Level Hardening)

Applied to the Staff OU.

## Policies Implemented

### Control Panel Restriction
- Prohibit access to Control Panel and PC Settings

###  Command Prompt Restriction
- Prevent access to Command Prompt (cmd.exe)
- Prevent batch file execution

## Security Objective

- Prevent system configuration tampering
- Reduce insider misuse
- Limit privilege abuse opportunities



# 3. Local Administrator Access Control (Least Privilege)

Applied to the Workstations OU.

## Restricted Groups Configuration

Computer Configuration → Policies → Windows Settings → Security Settings → Restricted Groups

Configured the **Administrators** local group to contain only:

- Domain Admins
- Authorized IT Security Group

## Security Objective

- Prevent unauthorized local admin escalation
- Stop users from adding themselves to Administrators
- Reduce lateral movement risk in case of compromise



# 4. Delegated Password Reset Permissions

Configured via Delegation of Control Wizard on Staff OU.

## Delegated To:
- IT Security Group

## Permissions Granted:
- Reset user passwords
- Force password change at next logon

## Security Objective

- Implement RBAC
- Avoid granting Domain Admin rights unnecessarily
- Support operational separation of duties



# Validation & Testing

The following tests were performed:

- Logged in as Staff user → Confirmed Control Panel blocked
- Attempted to open CMD → Access denied
- Executed gpupdate /force → Policies applied successfully
- Ran net localgroup administrators on CLIENT-01 → Verified restricted membership
- Reset password using delegated IT account → Successful



# Security Architecture Summary

This implementation demonstrates:

- Identity hardening
- Role-based access control (RBAC)
- Endpoint configuration lockdown
- Centralized privilege governance
- Enterprise-style AD segmentation
