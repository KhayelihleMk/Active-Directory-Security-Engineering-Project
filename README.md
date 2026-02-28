# Active Directory Security Engineering Project

## Project Overview

This project demonstrates comprehensive Active Directory (AD) security engineering, including OU design, Group Policy Objects (GPOs), password and lockout policies, delegation, and restricted groups. The goal was to simulate enterprise-level AD management and hardening practices in a lab environment while applying security best practices.

The project highlights hands-on experience with AD administration, security enforcement, and SOC-relevant security controls.



## Objectives

- Design and implement Organizational Unit (OU) hierarchy for logical and secure management  
- Configure Group Policy Objects (GPOs) to enforce password, lockout, and security settings  
- Implement restricted groups to limit local administrator privileges  
- Delegate administrative permissions securely  
- Validate security policies and test enforcement across lab domain controllers and client machines  



## Lab Setup

- Domain Controller (Windows Server VM)  
- Client Workstation (Windows 11 VM)  
- Active Directory Users and Computers configured with custom OUs  
- GPOs linked to OUs for policy enforcement  
- Restricted groups applied to critical computers  



## Testing / Validation

- OU structure verified via Active Directory Users and Computers  
- GPOs tested by logging into client machines and confirming policy enforcement  
- Restricted groups validated by attempting unauthorized privilege escalation  
- All configurations documented and screenshots captured for portfolio demonstration  



## Technologies Used

- Windows Server (Domain Controller)  
- Windows Clients  
- Active Directory Users and Computers (ADUC)  
- Group Policy Management Console (GPMC)  
- Restricted Groups configuration  



## Skills Demonstrated

- Active Directory security engineering  
- OU design and delegation strategy  
- GPO creation and enforcement  
- Restricted group management  
- Policy testing and validation  
- Hands-on SOC/security operations practices  



## Screenshots

### OU Structure
![OU Structure](screenshots/ou-structure.png)

### GPO Policy Settings
![GPO Settings](screenshots/gpo-policy.png)

### Restricted Groups Configuration
![Restricted Groups](screenshots/restricted-group-settings.png)



## Notes

- This project was completed in a lab environment for learning and portfolio purposes.  
- Security policies and thresholds were applied according to best practice guidelines for AD security.  
- All configurations can be adapted for production environments with proper change management.
