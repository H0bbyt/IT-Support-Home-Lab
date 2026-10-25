# Windows 11 Enterprise — CLIENT01 Configuration

## 1. Overview

Windows 11 Enterprise was deployed as a domain-joined workstation in the home lab. The virtual machine, named CLIENT01, simulates an employee computer in a small business environment.

The primary objective was to install Windows 11, configure network connectivity, integrate the workstation with the `monster.test` Active Directory domain, and prepare it for IT Support and security administration exercises.

## 2. Virtual Machine Configuration

| Component | Configuration |
|---|---|
| Virtual Machine | CLIENT01 |
| Operating System | Windows 11 Enterprise Evaluation |
| Hypervisor | VMware Workstation |
| Virtual CPUs | 2 |
| RAM | 4 GB |
| Virtual Disk | 64 GB |
| Network | NAT (VMnet8) |
| Firmware | UEFI |

## 3. Operating System Installation

CLIENT01 was created in VMware Workstation using the Windows 11 Enterprise Evaluation installation ISO.

After installation, a local administrator account was configured for workstation management.

## 4. VMware Snapshot

A snapshot named **Clean Windows 11 Installation** was created after the operating system installation completed.

The snapshot provides a recovery point for future configuration changes and security exercises.

## 5. Network Configuration

CLIENT01 was connected to VMware's NAT network, VMnet8, alongside the Windows Server 2025 domain controller.

The command `nslookup monster.test` successfully resolved the domain to CLIENT01 IP address.

## 6. Active Directory Domain Integration

CLIENT01 was joined to the `monster.test` domain through Windows System Properties using `sysdm.cpl`.

Domain administrator credentials were supplied to authorize the join. Windows displayed a successful domain welcome message, and the workstation was restarted to complete the process.

Domain membership and domain controller discovery were subsequently verified using `systeminfo` and `nltest`.

## 7. Domain Authentication Testing

A test employee account, `MONSTER\jsmith`, was used to sign in to CLIENT01.

The user successfully completed the initial password-change process and signed in to Windows.

The `whoami` command confirmed the authenticated identity as `monster\jsmith`.

A subsequent Help Desk password-reset exercise was also completed successfully. The account password was reset through Active Directory Users and Computers, and the user regained access to CLIENT01.

## 8. Troubleshooting and Lessons Learned

This deployment provided practical experience troubleshooting UEFI boot problems, managing virtual installation media, using Windows recovery tools, configuring DNS, and joining a workstation to Active Directory.

The process reinforced the importance of verifying operating system installation, network connectivity, and domain name resolution before attempting domain authentication.

## 9. Current Status and Next Steps

CLIENT01 is installed, domain-joined, and capable of authenticating Active Directory users.

Future exercises will include Group Policy application, account lockout troubleshooting, security group permissions, and Windows endpoint administration.