

Automated Report Generator

 Overview
The **Automated Report Generator** is a Python-based GUI application built using Tkinter. It automates the process of parsing incident reports from text files, deduplicates incidents, and generates an Excel report based on a provided template.

This tool is designed for operational teams managing fault updates, streamlining their reporting process by reducing manual effort.

---

Features
- Incident Parsing: Extracts incidents and details from structured text files.
- Deduplication: Eliminates duplicate incident entries based on ticket number and start time.
- Custom Excel Reports: Generates Excel reports based on a predefined template.
- User-Friendly GUI: Simple interface for selecting input files, templates, and output folders.
- SLA Compliance Check: Automatically evaluates SLA compliance for each incident.

---

 Requirements
- Python Version: Python 3.7 or higher
- Dependencies: 
  - `tkinter` (for GUI)
  - `openpyxl` (for Excel file handling)
  - `re` (for regular expressions)
  - `datetime` (for date and time handling)

Install dependencies via:
```bash
pip install openpyxl
```

---

Installation
1. Clone or download this repository to your local machine.
2. Ensure Python 3.7+ is installed.
3. Install the required dependencies using `pip`.
4. Run the application using:
   ```bash
   python app.py
   ```

---

Usage
1. Launch the application.
2. Use the Browse buttons to:
   - Select a chat file (text format) containing fault updates.
   - Choose an Excel template file.
   - Specify the output folder for the generated report.
3. Click **Generate Report** to process the files and create an Excel report.
4. The generated report will be saved in the specified output folder as `Automated_Report.xlsx`.

---

File Formats
Input Text File
The chat file should follow this format:
```
*EBU Fault Update*
*HH:MM DD/MM/YYYY*
*1. Incident Description
Ticket #INC-XXXXXXXX-XXXXXXXX
Start Time: HH:MM DD/MM/YYYY
End Time: HH:MM DD/MM/YYYY
RFO: Reason
Status: Resolved*
```

 Excel Template
Ensure the template is structured with specific columns corresponding to:
- Ticket Number
- Outage Description
- SLA Compliance
- etc.

---

Example
Input:
Chat File:
```
*EBU Fault Update*
*12:30 01/01/2025*
*1. Network outage in area XYZ
Ticket #INC-12345678-12345678
Start Time: 10:00 01/01/2025
End Time: 12:00 01/01/2025
RFO: Power failure
Status: Resolved*
```
Template File:
Predefined Excel file with headers matching the script’s column mappings.

Output:
Generated Excel report with rows populated based on incidents parsed.

---

## Customization
You can modify:
- Regex Patterns: For parsing different text formats.
- Column Mappings: To align with custom Excel templates.
- SLA Rules: For compliance evaluation.

---

Troubleshooting
- Error Messages: Displayed via the GUI for file-related or parsing issues.
- Log Files: Extend the script to add logging for debugging.

---

 License
This project is licensed under the MIT License. You are free to use, modify, and distribute this software.

---

 Contact
For questions or issues, please contact:
Mweemba Mathews Mizinga   
mweemba1401@gmail.com

--- 
