# Lab Architecture

## Overview

The SIEM Lab is designed to simulate a basic enterprise security monitoring environment using Wazuh. The lab consists of virtual machines representing a monitored endpoint and a centralized SIEM server. Security events generated on the endpoint are collected, analyzed, and visualized through the Wazuh platform.

The objective of this architecture is to understand the complete lifecycle of security monitoring, from log generation on an endpoint to alert generation and analysis within a SIEM.

---

# Lab Components

## Ubuntu Server

The Ubuntu Server hosts the complete Wazuh platform, including the Wazuh Manager, Wazuh Indexer, and Wazuh Dashboard. It acts as the central server responsible for collecting logs, processing security events, generating alerts, and providing visualization through the web dashboard.

### Responsibilities

* Host the Wazuh Platform
* Receive logs from monitored endpoints
* Analyze security events
* Apply detection rules
* Generate security alerts
* Provide centralized monitoring

---

## Windows 11 Endpoint

The Windows virtual machine represents a monitored endpoint within the environment. It generates operating system events and security logs that are forwarded to the Wazuh Server using the Wazuh Agent. Microsoft Sysmon is also deployed to provide enhanced endpoint telemetry.

### Responsibilities

* Generate Windows Event Logs
* Generate Sysmon Events
* Forward logs using the Wazuh Agent
* Simulate endpoint activity

---

## Kali Linux (Future Expansion)

Kali Linux will be introduced during the later stages of the project to simulate attacker behavior. It will be used to perform controlled security assessments and generate security events that can be detected by Wazuh.

### Planned Activities

* Network Scanning
* Port Enumeration
* Authentication Testing
* Web Application Testing
* Attack Simulation

---

# Architecture Diagram

```text
                 Kali Linux
              (Attack Machine)
                      │
                      ▼
            Windows 11 Endpoint
      (Wazuh Agent + Microsoft Sysmon)
                      │
                      ▼
               Ubuntu Server
        (Wazuh Manager + Indexer +
             Wazuh Dashboard)
```

---

# Data Flow

The security monitoring process follows the workflow below:

1. User or system activity generates security events on the Windows endpoint.
2. Windows Event Logs and Sysmon record these activities.
3. The Wazuh Agent collects the generated events.
4. Events are securely forwarded to the Wazuh Manager.
5. The Wazuh Manager processes the events using predefined rules.
6. Processed events are indexed by the Wazuh Indexer.
7. The Wazuh Dashboard displays alerts, logs, and monitoring information for analysis.

---

# Communication Flow

```text
Windows Event Logs
        │
        ▼
Microsoft Sysmon
        │
        ▼
Wazuh Agent
        │
        ▼
Wazuh Manager
        │
        ▼
Wazuh Indexer
        │
        ▼
Wazuh Dashboard
```

---

# Objectives of the Lab Architecture

* Understand the architecture of a centralized SIEM deployment.
* Learn how endpoint logs are collected and processed.
* Observe the flow of security events from endpoint to dashboard.
* Develop practical experience with enterprise security monitoring.
* Build a foundation for future SOC and Detection Engineering projects.

---

# Conclusion

This lab architecture provides a simplified representation of an enterprise SIEM environment. By combining a centralized Wazuh server with monitored Windows endpoints, the lab enables practical learning of log collection, event processing, alert generation, and security monitoring. Additional systems, attack simulations, and detection techniques will be incorporated as the project progresses.

