# IT-Support-Home-Lab

# Project Overview
This project documents hands-on experience building and managing a virtual IT environment using VMware Workstation Pro, Windows Server 2025, Active Directory, DNS, and Kali Linux.

# Lab Enviroment

I built my IT Support and Cybersecurity Home Lab using an Acer Nitro 5 laptop running Windows 11 with 16GB of RAM. I used VMware Workstation Pro to create and manage virtual machines, including Kali Linux and Windows Server 2025. The Windows Server virtual machine was configured as a domain controller named **DC01**, hosting an Active Directory domain called monster.test. To establish consistent network connectivity, I configured the domain controller with a static IP address on a VMware NAT network.

# Lab Deployment

I successfully installed and configured Kali Linux and Windows Server 2025 within VMware Workstation. I began by setting up the virtual machines, allocating hardware resources, and updating Kali Linux to prepare it for future cybersecurity exercises.

Next, I configured Windows Server 2025 by renaming the server to DC01 and assigning it a static IPv4 address. I installed Active Directory Domain Services (AD DS) and DNS to establish my first Windows domain, `monster.test`.

During the domain controller promotion process, I encountered a prerequisite validation error caused by the local Administrator account having a blank password. I investigated the error, identified the cause, configured a strong Administrator password, and completed the domain controller setup.

After confirming that the Active Directory and DNS services were running, I used Active Directory Users and Computers (ADUC) to create an organizational structure consisting of an Employees Organizational Unit (OU) with three departmental OUs: IT, Human Resources (HR), and Sales.

**Outcome:** By the end of Day 1, I had established a functional virtualized Active Directory environment for practicing Windows Server administration, user account management, Group Policy, network troubleshooting, and common IT Help Desk responsibilities. This project represents the foundation of my hands-on IT Support and cybersecurity portfolio.
