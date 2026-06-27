# SOC Home Lab

## Overview

This repository documents my journey of building a Security Operations Center (SOC) Home Lab to gain practical experience in enterprise security monitoring, threat detection, log analysis, and incident response. The project is focused on understanding how Security Operations Centers monitor systems, detect malicious activities, investigate security alerts, and respond to cyber threats using industry-standard tools and methodologies.

The purpose of this repository is to apply theoretical cybersecurity concepts in a practical environment while developing hands-on skills in Security Information and Event Management (SIEM), Windows event logging, detection engineering, and security operations.

---

## Objectives

The primary objectives of this project are:

* Build a functional SOC Home Lab using open-source security tools.
* Learn the architecture and workflow of a Security Operations Center.
* Configure and manage Wazuh for security monitoring.
* Understand Windows Event Logs and Sysmon event generation.
* Simulate common cyber attacks in a controlled environment.
* Analyze security logs and investigate generated alerts.
* Study Detection Engineering concepts and rule creation.
* Understand MITRE ATT&CK techniques and their practical implementation.
* Document every stage of the lab with proper technical notes and observations.

---

## Technologies Used

This project will include practical implementation and documentation of the following technologies:

* Wazuh SIEM
* Sysmon
* Windows 11
* Ubuntu Server
* Kali Linux
* VirtualBox
* Nmap
* Wireshark
* Sigma Rules
* MITRE ATT&CK Framework
* Git and GitHub

---

## Repository Structure

```text
SOC-Home-Lab/
│
├── Architecture/
├── Wazuh/
├── Sysmon/
├── Detection_Rules/
├── Attack_Simulations/
├── Alert_Analysis/
├── Sigma/
├── Resources/
├── Screenshots/
└── README.md
```

---

## Project Scope

Throughout this project, I will document the complete process of building a SOC Home Lab, beginning with the installation and configuration of the required infrastructure. The repository will include practical attack simulations, security monitoring, alert analysis, investigation procedures, and incident documentation.

Each topic will include detailed explanations, practical demonstrations, screenshots, observations, and learning outcomes to create a comprehensive reference for future learning.

---

## Topics Covered

The repository will cover the following areas:

* Security Operations Center (SOC)
* Security Information and Event Management (SIEM)
* Wazuh Installation and Configuration
* Windows Event Logging
* Sysmon Configuration
* Log Analysis
* Detection Engineering
* Attack Simulation
* Security Monitoring
* Alert Investigation
* Incident Response
* MITRE ATT&CK Mapping
* Sigma Rules

---

## Learning Goals

By completing this project, I aim to strengthen my understanding of enterprise security operations and develop practical skills in monitoring, detecting, and investigating security events. The project will also improve my knowledge of security logging, detection methodologies, and incident response processes while providing hands-on experience with commonly used SOC tools.

---

## Future Enhancements

As I continue learning, I plan to expand this repository by including additional attack simulations, custom detection rules, automation using Python, threat intelligence integration, and more advanced security monitoring techniques.

---

## References

The learning resources used throughout this project include official documentation, industry standards, practical cybersecurity platforms, and community resources such as:

* Wazuh Documentation
* Microsoft Learn
* Sysmon Documentation
* MITRE ATT&CK Framework
* Sigma HQ
* OWASP
* TryHackMe
* Hack The Box

---

## Repo fileflow

SOC-Home-Lab/
│
├── README.md
├── LICENSE
│
├── 01_Introduction/
│   ├── SOC_Overview.md
│   ├── SIEM_Basics.md
│   ├── SOC_Workflow.md
│   └── MITRE_ATTACK_Overview.md
│
├── 02_Lab_Setup/
│   ├── Lab_Architecture.md
│   ├── VirtualBox_Setup.md
│   ├── Windows_VM.md
│   ├── Ubuntu_Server.md
│   ├── Kali_Linux.md
│   └── Network_Configuration.md
│
├── 03_Wazuh/
│   ├── Installation.md
│   ├── Agent_Configuration.md
│   ├── Dashboard_Configuration.md
│   ├── Rule_Management.md
│   └── Troubleshooting.md
│
├── 04_Sysmon/
│   ├── Installation.md
│   ├── Configuration.md
│   ├── Event_ID_Reference.md
│   └── Sysmon_vs_Windows_Logs.md
│
├── 05_Attack_Simulations/
│   ├── Nmap_Scan.md
│   ├── Failed_Login.md
│   ├── Brute_Force.md
│   ├── Reverse_Shell.md
│   ├── PowerShell_Execution.md
│   ├── Suspicious_Process.md
│   └── Web_Attack.md
│
├── 06_Detection_Engineering/
│   ├── Detection_Engineering_Basics.md
│   ├── Sigma_Rules.md
│   ├── Custom_Detection_Rules.md
│   └── MITRE_Mapping.md
│
├── 07_Alert_Analysis/
│   ├── Alert_Investigation.md
│   ├── Incident_Report_Template.md
│   ├── IOC_Analysis.md
│   └── False_Positives.md
│
├── 08_Threat_Hunting/
│   ├── Threat_Hunting_Basics.md
│   ├── Windows_Event_Log_Analysis.md
│   ├── Log_Analysis.md
│   └── Hunting_Scenarios.md
│
├── 09_Automation/
│   ├── Python_Automation.md
│   ├── Log_Parsing.md
│   └── Alert_Automation.md
│
├── 10_CheatSheets/
│   ├── Wazuh_Commands.md
│   ├── Sysmon_Event_IDs.md
│   ├── Windows_Event_IDs.md
│   ├── Sigma_Syntax.md
│   └── MITRE_ATT&CK_CheatSheet.md
│
├── Screenshots/
│   ├── Wazuh/
│   ├── Sysmon/
│   ├── Dashboards/
│   ├── Alerts/
│   └── Attack_Simulations/
│
└── Resources/
    ├── References.md
    ├── Useful_Links.md
    └── Learning_Roadmap.md

## License

This project is licensed under the MIT License.

