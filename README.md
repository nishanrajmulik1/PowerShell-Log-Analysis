# 🧪 PowerShell Log Analysis

## 📌 Project Overview

**PowerShell-Log-Analysis** is a blue team project focused on detecting and analyzing suspicious PowerShell activity within Windows environments. This project uses native Windows Event Logs, parsed and monitored using PowerShell scripts, to identify behaviors related to reconnaissance, execution, and lateral movement.

The goal of this project is to simulate real-world attacks, capture PowerShell-based IOCs (Indicators of Compromise), and build a strong understanding of how attackers use PowerShell during exploitation phases.

---

## 🛠️ Tools & Technologies

- 💻 **PowerShell** (scripted log parsing & automation)
- 📂 **Windows Event Viewer / Logs**
- 🧠 **MITRE ATT&CK Framework**
- 📊 **Event IDs Monitored**: 4104, 4688, 7045, 400, 403
- 🔍 **Log Sources**: PowerShell Operational Logs, Security Logs

---

## 🔍 Key Detection Use Cases

| Event ID | Description | MITRE Technique |
|----------|-------------|------------------|
| 4104     | PowerShell script block logging | T1059.001 (PowerShell) |
| 4688     | New process creation | T1059 / T1047 |
| 7045     | Service installation | T1543.003 |
| 400/403  | PowerShell engine start/stop | Execution tracking |

---

## 📁 Project Structure

```bash
PowerShell-Log-Analysis/
├── logs/
│   └── sample_logs.evtx
├── scripts/
│   └── parse-ps-logs.ps1
│   └── detect-obfuscation.ps1
├── IOC-list/
│   └── suspicious-commands.txt
├── screenshots/
│   └── detection_output.png
└── README.md
---

## ✅ What I Learned

- How attackers use PowerShell for stealthy execution
- The importance of script block logging for detection
- Writing detection logic in PowerShell based on event IDs and attacker behaviour
- Mapping logs to MITRE ATT&CK techniques for threat classification

---

## 📸 Screenshots

![Detection Output](screenshots/detection_output.png)

