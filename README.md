# Cyberd Triage
home Lab (Cybersecurity)
Dt1ger Triage Tool for Windows
=============================

Author: Demar Powell
Version: 1.0
Date: April 2025

Overview:
---------
This is a Windows desktop application designed to assist with rapid cyber triage. It allows analysts or first responders to quickly collect and view vital system information including:

✔️ Active network connections  
✔️ Access to KAPE (Kroll Artifact Parser & Extractor)  
✔️ Memory dump trigger (via DumpIt or other tools)  
✔️ Viewing of recent Windows Event Logs

The tool is styled with a Jamaican-inspired theme (black, yellow, and green) for clarity and aesthetics.

---

How to Use:
-----------
1. **Launch the App:**
   Double-click the `triage_app.exe` located in the `dist` folder or extracted ZIP package.

2. **Available Buttons:**

   - `Scan Network`: Lists all current network connections (like netstat).
   - `Run KAPE`: Opens the KAPE graphical interface. Make sure `kape.exe` is available at the path specified in the app (see Requirements).
   - `Dump Memory`: Runs a memory dump tool like DumpIt. Ensure it's available at the default path.
   - `View Event Logs`: Retrieves the last 20 Windows System Event Logs using `wevtutil`.

---

Requirements:
-------------
- **Windows 10/11**
- Python is NOT required for end users. This `.exe` is fully packaged.
- The following tools must be available on the system:
  - `kape.exe` at:
    `C:\Users\Demar's PC\Downloads\kape\KAPE\kape.exe`
  - `DumpIt.exe` (or similar) at:
    `C:\tools\DumpIt.exe`

(You may edit the Python source to use different paths if needed.)

---

How to Customize:
-----------------
To change the paths for KAPE or DumpIt:
1. Open the original `triage_app.py` file in any text editor.
2. Update the paths in the `run_kape()` and `dump_memory()` functions.
3. Rebuild the `.exe` using:
   `python -m PyInstaller --onefile --windowed triage_app.py`

---
![image](https://github.com/user-attachments/assets/9832a566-2b05-4510-be66-7c808475a611)

Disclaimer:
-----------
This tool is provided for internal, educational, and lawful incident response usage only. Ensure you have appropriate permissions before deploying memory dumps or event log access.

---

