# Active Directory Security Engineering Project

## Overview

This project demonstrates enterprise-level Active Directory (AD) security hardening and role-based access control (RBAC) implementation using Windows Server.

The objective was to simulate a real-world corporate environment and enforce identity security, least privilege access, and centralized endpoint control using Group Policy Objects (GPOs).


## Environment

- Windows Server (Domain Controller: DC01)
- Windows 11 Client (CLIENT-01)
- Active Directory Domain Services (AD DS)
- Group Policy Management
- Organizational Units (OUs)
- Security Groups



## Key Security Implementations

- Structured OU design for policy segmentation
- Password complexity & account lockout enforcement
- Least privilege enforcement using Restricted Groups
- Delegation of password reset permissions
- Endpoint configuration hardening via GPO



## Security Objectives

- Reduce privilege escalation risk
- Enforce centralized identity control
- Implement enterprise-style RBAC
- Validate policy enforcement through testing


## Project Structure

- ou-design.md → OU architecture explanation
- gpo-settings.md → Security policy configurations
- restricted-groups.md → Local admin control enforcement

## Skills Demonstrated

- Active Directory Administration
- Role-Based Access Control (RBAC)
- Group Policy Hardening
- Privilege Escalation Prevention
- Identity & Access Management
- Security Validation Testing
