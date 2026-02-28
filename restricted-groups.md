# Restricted Groups – Local Administrator Control

## Objective

To enforce least privilege by centrally managing local Administrator group membership across domain-joined systems.



## Configuration

Using Group Policy:

Computer Configuration → Policies → Windows Settings → Security Settings → Restricted Groups

Configured:
- Administrators group
- Members allowed:
  - Domain Admins
  - IT Security Group



## Validation

On CLIENT-01:

Command executed:
net localgroup administrators

Result:
Only approved groups were present.



## Security Impact

- Prevents unauthorized local admin additions
- Reduces lateral movement risk
- Enforces enterprise-level RBAC
