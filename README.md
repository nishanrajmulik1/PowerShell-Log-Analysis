# PowerShell Log Analysis – Windows Event Viewer Monitoring

This project explores security monitoring using PowerShell by enabling logging, simulating attacks, and retrieving logs.

## 📌 Key Features
- Enables **PowerShell Module Logging, Script Block Logging, and Transcription**.
- Simulates an **attack reconnaissance** with `Get-LocalUser` to list system accounts.
- Detects suspicious activity using **Windows Event Viewer (Event ID 4104)**.
- Retrieves logs using PowerShell commands like `Get-WinEvent`.

## 🛠 Tools & Technologies
- PowerShell
- Windows Event Viewer
- Sysmon (Optional for deeper logging)
- Security Monitoring & Threat Hunting

## 🚀 How to Use

1. **Enable PowerShell Logging**:  
   - Open **Group Policy Editor** by running:  
     ```
     gpedit.msc
     ```
   - Navigate to:  
     ```
     Computer Configuration > Administrative Templates > Windows Components > Windows PowerShell
     ```
   - Enable:
     - **Module Logging**
     - **Script Block Logging**
     - **Transcription**

2. **Simulate a Suspicious Activity**  
   Run the following PowerShell command:
   ```powershell
   Get-LocalUser | Select-Object Name, Enabled
   
3. Detect Logs using Event Viewer or PowerShell
   Retrieve logs from Event ID 4104:
   ```powershell
   Get-WinEvent -LogName "Microsoft-Windows-PowerShell/Operational" | Where-Object {$_.Id -eq 4104}

4. Analyze the retrieved logs.
   - Open Event Viewer (eventvwr.msc)
   - Navigate to:
   ```
   Applications and Services Logs > Microsoft > Windows > PowerShell > Operational
   ```
   - Filter by Event ID 4104
