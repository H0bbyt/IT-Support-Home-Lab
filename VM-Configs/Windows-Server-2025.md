# Windows Server 2025 — Domain Controller Configuration

## 1. Overview

Windows Server 2025 was deployed in VMware Workstation Pro to serve as the primary domain controller for the Active Directory home lab. The server, named DC01, provides Active Directory Domain Services (AD DS) and DNS for the `monster.test` domain.

The environment simulates a small business network in which centralized authentication, user management, and Windows workstation administration can be practiced.

## 2. Virtual Machine Configuration

| Component | Configuration |
|---|---|
| Virtual Machine | DC01 |
| Operating System | Windows Server 2025 Evaluation |
| Hypervisor | VMware Workstation |
| Virtual CPUs | 2 |
| RAM | 4 GB |
| Virtual Disk | 80 GB |
| Network | NAT (VMnet8) |

## 3. Network Configuration

DC01 was configured with a static IPv4 address to provide a consistent location for Active Directory and DNS services.

The static address ensures that domain-joined clients can consistently locate the domain controller.

## 4. Active Directory Deployment

The Active Directory Domain Services and DNS Server roles were installed using Windows Server Manager.

DC01 was promoted to the first domain controller in a new forest named `monster.test`, with the NetBIOS domain name `MONSTER`.

## 5. Organizational Unit Structure

The following organizational units were created to simulate a small company's departmental structure.

```text
monster.test
└── Employees
    ├── IT
    ├── HR
    └── Sales
```

These organizational units provide a foundation for organizing employee accounts and applying department-specific administrative settings.

## 6. Domain User Accounts

Three test employee accounts were created in Active Directory.

| Employee | Username | Department |
|---|---|---|
| John Smith | `jsmith` | IT |
| Sarah Johnson | `sjohnson` | HR |
| Michael Brown | `mbrown` | Sales |

The accounts are used for domain authentication testing and simulated Help Desk/IT support scenarios.

## 7. Validation

The domain controller was verified through Windows Server Manager and Active Directory Users and Computers.

CLIENT01 successfully resolved `monster.test` to the configure IP address, joined the domain, and authenticated using the `MONSTER\jsmith` account.

These tests confirmed that the domain controller was providing the essential services required for a functioning Active Directory environment.

## 8. Troubleshooting and Lessons Learned

The initial domain controller promotion failure demonstrated the importance of account security requirements during Active Directory deployment.

Configuring a static IP address and using the domain controller as the DNS server also reinforced the relationship between DNS and domain authentication.

## 9. Current Status and Next Steps

DC01 is operational as the domain controller and DNS server for `monster.test`.

Future work will include Group Policy configuration, account lockout testing, security group management, permissions, and Active Directory security assessments.