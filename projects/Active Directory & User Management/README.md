# Active Directory & User Management

## Summary
This project demonstrates the implementation of Active Directory Domain Services (AD DS) in a controlled lab environment. Using Windows Server 2022 as the domain controller and a Windows 10 host machine, I configure a small business network infrastructure with organised user management, group policies, and security controls.


## Objectives
- Set up and configure a Windows Server 2022 domain controller with Active Directory Domain Services.
- Create and manage organisational units (OUs), user accounts, and security groups.
- Implement basic Group Policy Objects (GPOs) for security and user management.
- Join a Windows 10 host to the domain and verify domain functionality.
- Remote onto the Active Directory server from the Windows 10 host using SSH.


## Environment

### Tools Used:
- **Windows Server 2022** — Domain Controller
- **Windows 10 Enterprise** — Host machine
- **Active Directory Domain Services** — Promote server to Domain Controller
- **PowerShell** — Automation and management
- **SSH** — Remote administration
- **VMware Workstation 17 Pro** — *(<a href="https://github.com/Luka-Babetzki/cybersecurity-portfolio/blob/main/How%20to%20Install%20VMware.md">How to Install VMware</a>)*

### VM Configurations:

| Domain Controller   | Host Machine          |
|---------------------|-----------------------|
| Windows Server 2022 | Windows 10 Enterprise |
| 4GB RAM             | 2GB RAM               |
| 2 CPU cores         | 2 CPU cores           |
| 60GB Storage        | 50GB Storage          |
| NAT Network         | NAT Network           |

### Network Topology:

![alt text](image.png)


## Getting Started

### I. Promote Server to Domain Controller
1. Install Windows Server 2022
2. Configure static IP addressing
3. Install AD DS role
4. Promote server to domain controller
5. Configure DNS settings

### II. Configure Active Directory
1. Design OU hierarchy
2. Create departmental OUs
3. Configure user templates
4. Set up security groups

### III. Implement Group Policy
1. Create GPOs for security baseline
2. Configure password policies
3. Implement access controls
4. Set up folder redirection

### IV. Configure Windows Host
1. Join Windows 10 host to domain
2. Test user login
3. Verify group policy application
4. Document connectivity issues
5. Backup and recovery procedures

### V. Remote Administration
1. Demonstrate remote access from host to server


<!--

## Challenges & Solutions

### Challenge 1: ...

**Challenge Faced:** [What you were attempting to achieve and what went wrong or proved difficult]

**Solution Implemented:** [Detail the approach taken to resolve the challenge. Include specific tools, techniques, or methodologies used. Explain why this solution was chosen over alternatives if relevant]

**Skills Developed:**

- [Specific technical skill or knowledge gained]
- [Specific technical skill or knowledge gained]
- [Relevant soft skill or methodology learned]

---

### Challenge 2: ...

**Challenge Faced:** [What you were attempting to achieve and what went wrong or proved difficult]

**Solution Implemented:** [Detail the approach taken to resolve the challenge. Include specific tools, techniques, or methodologies used. Explain why this solution was chosen over alternatives if relevant.]

**Skills Developed:** 

- [Specific technical skill or knowledge gained]
- [Specific technical skill or knowledge gained]
- [Relevant soft skill or methodology learned]

-->


## Results & Impact
- Vulnerabilities discovered
- Security gaps identified
- Attack paths documented
