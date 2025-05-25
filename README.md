<p align="center">
  <a href="https://github.com/Samuel-Cavada" target="_blank">
    <img src="https://img.shields.io/badge/Back_to_Main_Page-000000?style=for-the-badge&logo=github&logoColor=white" alt="Back to Main Page"/>
  </a>
</p>

<h1 align="center">Disable Windows Firewall on a Virtual Machine</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Azure-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white" alt="Cloud Platform" />
  <img src="https://img.shields.io/badge/OS-Windows%2010-0078D6?style=for-the-badge&logo=windows&logoColor=white" alt="OS" />
  <img src="https://img.shields.io/badge/Tool-Built%20in%20Firewall-00B388?style=for-the-badge" alt="Tool" />
  <img src="https://img.shields.io/badge/Focus-System%20Hardening-orange?style=for-the-badge" alt="Focus Area" />
</p>

---

## Project Objective
> Demonstrate how to disable the Windows Firewall in a secure lab environment for the purpose of enabling full access during vulnerability assessments or remote system administration testing.

---

## Tools & Technologies
- **Platform:** Azure
- **OS:** Windows 10
- **Tools:** Windows Defender Firewall (`wf.msc`)
- **Languages/Scripts:** N/A (GUI walkthrough)

---

## Skills Gained / Focus Areas
- Navigated Windows Firewall GUI
- Disabled firewall across all network profiles
- Prepared environment for full-scope vulnerability scanning

---

## Environment Setup
> Virtual machine provisioned on Microsoft Azure and accessed via RDP. Windows Defender Firewall must be disabled manually from the GUI for this lab.

---

## Walkthrough
1. [Step 1: Log in to the VM](#step-1-log-in-to-the-vm)
2. [Step 2: Open Firewall Settings](#step-2-open-firewall-settings)
3. [Step 3: Disable Windows Firewall](#step-3-disable-windows-firewall)

---

## 🚨 Danger Notice

**Disabling the Windows Firewall poses a significant security risk if done outside of a controlled lab environment. Proceed with caution.**

---

### Step 1: Log in to the VM
Access the VM remotely using Remote Desktop Protocol (RDP).

<p align="center">
  <img src="https://raw.githubusercontent.com/Samuel-Cavada/Windows-Vulnerability-Scanning-Authenticated-vs.-Unauthenticated/main/assets/images/Windows-Vulnerability-Scanning-Authenticated-vs.-Unauthenticated%2022.jpg" alt="RDP Login Screenshot">
</p>

---

### Step 2: Open Firewall Settings
Access the Windows Defender Firewall with Advanced Security interface.

- Press `Win`, type `wf.msc`, and press Enter.
- This opens the firewall console.
- Click on Windows Defender Firewall Properties from the right panel.

---

### Step 3: Disable Windows Firewall
Disable the firewall on all network profiles (Domain, Private, Public) to allow unrestricted inbound and outbound communication.

- In the Domain Profile tab:
  - Set Firewall state to Off.
- Repeat for Private Profile and Public Profile tabs.
- Click Apply and then OK on each tab.

<p align="center">
  <img src="https://raw.githubusercontent.com/Samuel-Cavada/Windows-Vulnerability-Scanning-Authenticated-vs.-Unauthenticated/main/assets/images/Windows-Vulnerability-Scanning-Authenticated-vs.-Unauthenticated%201.jpg" alt="Firewall Settings Screenshot">
</p>

---

## Outcomes and Lessons Learned
- Technical Insight: Learned how to disable the firewall using GUI controls on Windows 10.
- Configuration Skills: Adjusted firewall states across network profiles.
- Troubleshooting: Confirmed open network ports via scanning after firewall was disabled.
- Takeaway: Essential for enabling full-access authenticated scans in secure lab environments.

---

## References
- [Microsoft Docs: Windows Defender Firewall](https://learn.microsoft.com/en-us/windows/security/threat-protection/windows-firewall/windows-firewall-with-advanced-security)
- [How to Access `wf.msc`](https://learn.microsoft.com/en-us/windows/security/threat-protection/windows-firewall/create-an-inbound-port-rule)
