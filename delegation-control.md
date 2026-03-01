# Delegation of Control – Staff OU

## Objective

Implement Role-Based Access Control (RBAC) by delegating limited administrative privileges to the **IT-Security** group without granting Domain Admin rights.



## Configuration Steps

1. Created security group:  
   - `IT`  

2. Added members:  
   - `ITAdmin`  
   - `SecurityEngineer`  

3. Right-clicked **Staff OU** → Selected **Delegate Control**  

4. Added **IT-Security** group and selected permissions:  
   - Reset user passwords and force password change at next logon  



## Security Validation

Delegation was verified by:  

- Reviewing **Staff OU → Properties → Security → Advanced**  
- Confirming **IT-Security** group has:  
  - Reset password  
  - Write `pwdLastSet` permissions  



## Security Hardening Result

- IT staff can manage only **Staff OU users**  
- No Domain Admin privileges granted  
- `ITAdmin` denied interactive logon on Domain Controller  
- Demonstrates **Principle of Least Privilege**



## Enterprise Security Concepts Demonstrated

- **Role-Based Access Control (RBAC)**  
- **OU-level permission scoping**  
- **Privilege separation**  
- **Domain Controller logon restriction**
