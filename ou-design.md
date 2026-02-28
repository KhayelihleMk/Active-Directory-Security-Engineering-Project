# Organizational Unit (OU) Design

## Objective

To implement logical separation of users and devices in order to apply targeted security policies.



## OU Structure

- IT
- Staff
- Workstations



## Design Rationale

### Staff OU
Contains standard domain users. GPOs applied:
- Control Panel restrictions
- Password policy enforcement

### IT OU
Contains administrative users with delegated privileges.
Used for:
- Password reset delegation
- Controlled elevated access

### Workstations OU
Contains domain-joined endpoints.
Used to:
- Enforce local administrator restrictions
- Apply device-level hardening policies



## Security Benefit

This structure ensures:

- Role-based policy targeting
- Reduced attack surface
- Easier privilege management
- Enterprise scalability
