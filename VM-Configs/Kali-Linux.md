# Kali Linux — Virtual Machine Configuration

## 1. Overview

Kali Linux was deployed as part of the home lab to provide a dedicated environment for learning ethical hacking, network analysis, vulnerability assessment, and penetration testing. The virtual machine runs on VMware Workstation alongside a Windows Server 2025 domain controller and a Windows 11 Enterprise workstation.

The purpose of this machine is to support authorized security testing within the isolated home lab while developing practical Linux administration and cybersecurity skills.

## 2. Virtual Machine Configuration

| Component | Configuration |
|---|---|
| Hypervisor | VMware Workstation |
| Operating System | Kali Linux |
| Virtual CPUs | 2 |
| RAM | 4 GB |
| Virtual Disk | Approximately 60 GB |
| Network Adapter | VMware virtual network |
| VM Name | Kali Linux |

## 3. Installation and Initial Setup

The Kali Linux virtual machine was created in VMware Workstation Pro with two virtual CPUs, 4 GB of RAM, and approximately 60 GB of virtual disk storage. The operating system was installed and configured for use as the primary security testing workstation in the home lab.

After installation, system packages were updated to bring the operating system up to date. VMware integration tools were also installed to improve usability and compatibility between the guest operating system and the host computer.

## 4. Networking

Kali Linux is intended to communicate with the Windows Server 2025 domain controller and Windows 11 workstation through the VMware virtual network.

The final network adapter configuration and Kali IP address will be verified and documented before beginning Active Directory security testing.

## 5. Tools and Capabilities

Kali Linux provides a platform for practicing network reconnaissance, Linux administration, security analysis, and penetration-testing techniques. Specific tools and commands will be documented as they are used during future lab sessions.

## 6. Troubleshooting and Lessons Learned

This deployment provided practical experience creating a Linux virtual machine, allocating hardware resources, installing an operating system, performing package updates, and configuring VMware guest integration.

## 7. Current Status

Kali Linux has been installed, updated, and prepared for future security exercises. Network connectivity to the Active Directory lab and individual security tools will be verified during upcoming sessions.

## 8. Next Steps

The next stage will involve verifying Kali Linux network connectivity, identifying the Windows domain controller and workstation from the authorized lab network, and documenting the initial security testing environment.