# Homelab — IT & Cybersecurity Home Lab

## Project Overview

Monster Hacker by 35 is a hands-on IT infrastructure and cybersecurity project designed to develop practical skills in technical support, system administration, networking, Active Directory, and ethical hacking.

The project simulates a small business IT environment using VMware Workstation, Windows Server 2025, Windows 11 Enterprise, and Kali Linux.

The initial phase focuses on building and administering a functional Windows domain environment while practicing common Help Desk responsibilities. Future phases will expand into Windows security, network analysis, automation, and authorized penetration testing.

## Lab Environment

| Virtual Machine | Operating System | Role |
|---|---|---|
| DC01 | Windows Server 2025 | Active Directory Domain Services and DNS |
| CLIENT01 | Windows 11 Enterprise | Domain-joined workstation |
| Kali Linux | Kali Linux | Security testing workstation |

**Domain:** `monster.test`  
**Virtual Network:** VMware NAT (VMnet8)  

## Virtual Machine Configurations

Detailed installation and configuration documentation is available below.

- [Kali Linux](VM-Configurations/Kali-Linux.md)
- [Windows Server 2025](VM-Configurations/Windows-Server-2025.md)
- [Windows 11 Enterprise](VM-Configurations/Windows-11-Enterprise.md)

## IT Support Labs

Hands-on exercises simulate real-world Help Desk and Windows administration responsibilities.

- [Active Directory User Management](IT-Support-Labs/Active-Directory-User-Management.md)

Completed exercises include employee account creation, domain authentication testing, and password-reset troubleshooting.

## Security Labs

Security exercises will be added as the project progresses. Future activities will include Active Directory enumeration, vulnerability assessment, Windows security testing, and penetration-testing practice within the authorized lab environment.

## Skills Developed

This project provides hands-on experience with VMware virtualization, Windows deployment, Active Directory Domain Services, DNS configuration, network troubleshooting, domain authentication, user account provisioning, password management, and technical documentation.

## Project Roadmap

The next phase will focus on account lockout troubleshooting, security groups, Group Policy, Windows administration, and basic PowerShell automation.

Later phases will introduce Active Directory security assessment techniques, Python scripting, and ethical hacking exercises.

## Documentation Approach

Each lab session is documented separately to capture objectives, configuration changes, troubleshooting, results, and lessons learned. Detailed technical documentation is organized by virtual machine and lab activity, allowing the repository to serve as both a learning record and a professional portfolio.
