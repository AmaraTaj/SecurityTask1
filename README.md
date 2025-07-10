# SecurityTask1
Sysmon configuration and setup for endpoint security and user activity monitoring.
# Sysmon Endpoint Security & Monitoring

🎯 Objective
Protect Internee.pk devices and servers from malware and unauthorized access.

✅ What was implemented

**Sysmon installation**
**File integrity monitoring** (Event ID 11)
**User process activity monitoring** (Event ID 1)
**Network connection monitoring** (Event ID 3)

🛠 Configuration

The `sysmonconfig.xml` file in this repository contains:

- `<ProcessCreate onmatch="include"/>` – to log every process created
- `<NetworkConnect onmatch="include"/>` – to log all outbound connections
- `<FileCreate>` – to log file creation in `C:\impprtant data\`

🗂 Contents

- `sysmonconfig.xml` – Sysmon configuration file
- `SysmonLogs.evtx` – Example logs exported from Event Viewer
🚀 How to Use

1. Install Sysmon:
   ```powershell
   sysmon64.exe -accepteula -i "path\to\sysmonconfig.xml"

