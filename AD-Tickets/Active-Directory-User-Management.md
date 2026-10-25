# Active Directory User Management — IT Support Lab

## 1. Overview

This lab focused on performing common IT Support and Help Desk tasks in a Windows Active Directory environment. The exercises were completed using a Windows Server 2025 domain controller and a Windows 11 Enterprise workstation joined to the `monster.test` domain.

The objective was to gain hands-on experience with user account provisioning, domain authentication, password management, and basic account troubleshooting.

## 2. Lab Environment

| Component | Configuration |
|---|---|
| Domain controller | DC01 — Windows Server 2025 |
| Client workstation | CLIENT01 — Windows 11 Enterprise |
| Active Directory domain | `monster.test` |
| Network | VMware NAT (VMnet8) |

## 3. Active Directory User Provisioning

Three fictional employee accounts were created using Active Directory Users and Computers (ADUC). Each account was placed in its corresponding departmental organizational unit.

| Employee | Username | Organizational Unit |
|---|---|---|
| John Smith | `jsmith` | Employees/IT |
| Sarah Johnson | `sjohnson` | Employees/HR |
| Michael Brown | `mbrown` | Employees/Sales |

Temporary passwords were assigned, and users were configured to change their passwords at their next sign-in.

This exercise demonstrated how IT administrators provision new employees and organize accounts within a centralized directory.

## 4. Domain Authentication Testing

CLIENT01 was used to test domain authentication with the `MONSTER\jsmith` account.

The user successfully signed in using domain credentials, changed the temporary password, and accessed the Windows desktop.

The authenticated identity was verified using:

```cmd
whoami
```

The command returned:

```text
monster\jsmith
```

This confirmed that CLIENT01 could authenticate an Active Directory user through DC01.

## 5. Password Reset Simulation

A simulated Help Desk ticket was performed in which John Smith reported forgetting his password.

Using Active Directory Users and Computers on DC01, the account password was reset and the option requiring a password change at next logon was enabled.

The user subsequently signed in to CLIENT01 using the temporary password and completed the password-change process.

This exercise demonstrated a standard Help Desk password recovery workflow.

## 6. Troubleshooting and Lessons Learned

These exercises reinforced the relationship between Active Directory user accounts, domain-joined workstations, DNS services, and centralized authentication.

They also demonstrated the importance of account verification, password security, and accurate technical documentation when supporting employees.

## 7. Outcome and Next Steps

User provisioning, domain authentication, and password-reset testing were completed successfully.

Future exercises will include account lockout troubleshooting, security group administration, Group Policy configuration, and additional Windows Help Desk scenarios.