# Enterprise Security Monitoring: Hands-On Splunk SIEM Analytics Lab

## 📌 Project Overview
This project demonstrates the deployment, configuration, and practical utilization of **Splunk Enterprise** as a central Security Information and Event Management (SIEM) platform. The core goal of this lab was to ingest multiple enterprise log sources, build optimized Search Processing Language (SPL) queries to detect malicious behavior, and construct a functional SOC Dashboard for real-time security monitoring.

Through this lab, I mastered log parsing, data normalization, advanced threat hunting, and security reporting within a simulated enterprise infrastructure.

---

## 🛠️ Tech Stack & Architecture
* **SIEM Platform:** Splunk Enterprise (Indexer, Search Head, and Forwarder setup)
* **Log Sources Ingested:** * Windows Event Logs (Security, System, Application)
  * Microsoft Sysmon (System Monitor)
  * Linux Auditd & Syslog
* **Framework Alignment:** MITRE ATT&CK Framework

---

## 🚀 Key Milestones & Capabilities Implemented

### 1. Data Ingestion & Field Extraction
* Configured a Splunk Universal Forwarder to safely ship Windows Event Logs and Linux Syslogs into the Splunk Indexer.
* Handled source-typing (`sourcetype=WinEventLog`) and created custom field extractions to cleanly isolate user accounts, process IDs, and source IP addresses.

### 2. Advanced Threat Hunting with SPL (Search Processing Language)
Developed high-fidelity, optimized SPL search queries to hunt for active cyber threats, including:
* **Brute Force Detection:** Identifying a high frequency of failed login events (Event ID 4625) followed by a single successful login (Event ID 4624) from the same IP.
* **Living off the Land (LotL):** Monitoring suspicious usage of native binaries like `powershell.exe`, `cmd.exe`, and `certutil.exe` downloading external scripts.
* **Account Creation Auditing:** Tracking unauthorized local user or group creations (Event IDs 4720/4732).

### 3. SOC Dashboard Engineering
* Created a functional **Live Security Operations Dashboard** utilizing XML and Splunk visualization tools.
* **Visual Panels Created:**
  * Top Target Users (Most failed authentication attempts)
  * Real-time PowerShell Activity Monitor
  * Geographic mapping of inbound firewall connections

---

## 🧠 Core Competencies Developed
* **SPL Query Optimization:** Writing clean, fast, and resource-efficient search terms.
* **Security Analytics:** Turning raw, unorganized system logs into actionable security intelligence.
* **Incident Triage Workflow:** Filtering out benign administrative noise to prioritize critical alerts.
