# How to Install VMware Workstation Pro 17

![alt text](<Active Directory & User Management/images/VMware17Pro-1171461506.png>)

## Guide: Installing and Setting up VMware
In this guide, you will learn how to install VMware on your computer, create two virtual machines, and connect them on the same NAT network.

## What is VMware?
VMware Workstation Pro is a free virtualisation platform available on Windows and Linux operating systems. VMware was brought by Broadcom in 2023 and made available as a free product for personal use in May 2024.

### VMware vs. VirtualBox
VMware Workstation Pro offers superior performance, better hardware compatibility, and more reliable snapshot functionality compared to VirtualBox. Whilst VirtualBox remains a solid choice for basic virtualisation, VMware is often preferred by professionals and power users who require more robust features and stability.


## Prerequiste Considerations

- **System Requirements:** Ensure your CPU supports hardware virtualisation (Intel VT-x or AMD-V) and that it's enabled in BIOS/UEFI.
- **Available Resources:** Minimum 4GB RAM recommended (8GB+ preferred), with at least 50GB free storage space per virtual machine.
- **Operating System:** Windows 10/11 64-bit or a compatible Linux distribution with kernel 3.10 or later.
- **Account Registration:** A Broadcom account is required to download VMware Workstation Pro.


## Getting Started

### Part 1: Installing VMware

1. **Download VMware:**

- Register and login to the <a href="https://support.broadcom.com">Broadcom Support Portal</a>.
- After successful login, access <a href="https://support.broadcom.com/group/ecx/productdownloads?subfamily=VMware%20Workstation%20Pro&freeDownloads=true">VMware Workstation Pro</a> downloads.
- Expand "VMware Workstation Pro 17.0 for Windows".
- Select the most recent stable version to download under the release column.

2. **Install VMware:**

- Locate the downloaded installer file (typically in your Downloads folder) and double-click to run it.
- Follow the setup wizard instructions, accepting the licence agreement and choosing your installation preferences.
- When prompted, select "Use VMware Workstation 17 for Personal Use" to activate the free licence.
- Complete the installation and restart your computer if prompted.
- Open the VMware Workstation Pro application. You should see the following:

![alt text](<Active Directory & User Management/images/image.png>)

---

### Part 2: Navigating VMware Interface

1. **Adding Virtual Machines:**

- **Method 1: Create a New Virtual Machine**
    - Click "Create a New Virtual Machine" on the home screen or select File → New Virtual Machine.
    - Choose "Typical" for a guided setup or "Custom" for advanced configuration options.
    - Select your installation media (ISO file, physical disc, or install later) and follow the wizard to configure RAM, storage, and network settings.

- **Method 2: Open a Preconfigured Virtual Machine**
    - Click "Open a Virtual Machine" on the home screen or select File → Open.
    - Navigate to the location of your existing .vmx file (VMware configuration file).
    - Select the file and click "Open" to add it to your VMware library.

---

### Part 3: Creating Two Virtual Machines on NAT Network

1. **Create Your First Virtual Machine:**

- Follow Method 1 from Part 2 to create a new VM with your chosen operating system.
- During network configuration, ensure "Network Adapter" is set to "NAT" (this is usually the default).
- Complete the VM creation and install your guest operating system.


2. **Create Your Second Virtual Machine:**

- Repeat the process to create a second VM, again ensuring the network adapter is set to "NAT".
- Both VMs will now be on the same virtual NAT network and can communicate with each other.

3. **Verify Network Connectivity:**

- Power on both virtual machines.
- In each VM, open a terminal or command prompt and use `ipconfig` (Windows) or `ip a` (Linux) to check the assigned IP addresses.
- Test connectivity by pinging one VM from the other using the command `ping [IP_ADDRESS]`.

---

## Troubleshooting

- **Installation Wizard Won't Open or Shows Errors:** If the VMware installer fails to launch or displays errors, the downloaded file may be corrupted. Verify the file integrity by comparing hashes:

    1. Locate the correct SHA256 hash on the Broadcom download page (displayed next to the file).
    2. Open PowerShell or Command Prompt as administrator.
    3. Navigate to your Downloads folder: `cd Downloads`
    4. Run the command: `certutil -hashfile [filename].exe SHA256` (replace [filename] with your actual file name).
    5. Compare the output hash with the one from Broadcom's website - they should match exactly.
    6. If the hashes don't match, delete the file and re-download it from the official portal.

- **Virtualisation Not Available:** Enable Intel VT-x or AMD-V in your BIOS/UEFI settings. Restart your computer, enter BIOS setup (usually by pressing F2, F10, or Del during boot), and locate virtualisation settings under CPU or Advanced options.
- **Slow Performance:** If your virtual machine feels slow, navigate to VM Settings → Display and increase Video Memory to 128 MB. Also consider allocating more RAM to the VM if your host system has sufficient resources.
- **Network Connection Issues:** If VMs cannot communicate, verify both are using NAT network adapter. Check firewall settings in the guest operating systems aren't blocking ICMP (ping) requests.

<br>

---

*If you have a different problem, read the <a href="https://techdocs.broadcom.com/us/en/vmware-cis/desktop-hypervisors/workstation-pro/17-0.html">**official documentation**</a> provided by Broadcom.*
