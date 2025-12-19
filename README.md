# AttendanceLog-Parser

![Python Version](https://img.shields.io/badge/python-3.8%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)

A streamlined CLI engine for processing raw attendance logs and CSV data. Built for speed and auditability, **AttendanceLog-Parser** allows you to parse, search, and report on attendance records without the overhead of a database management system.

## 📂 Project Structure

```text
.
├── attendance_logs/          # Input: Place raw .log or .csv files here
├── attendance_reports/       # Output: Generated report files
├── process_attendance.py     # Main processing and search script
├── requirements.txt          # Project dependencies (if any)
└── README.md                 # Project documentation
```

## 🚀 Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/karimullahchowdhury12/AttendanceLog-Parser.git
cd AttendanceLog-Parser
```

### 2. Environment Configuration
```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
```
### 3. Install Dependencies 
Note: Skip this if using only standard libraries.
```bash
pip install -r requirements.txt
```
## 💻 Usage
### 1. Generate Reports
To process all files within the `attendance_logs/` directory and generate a summary in `attendance_reports/`:
```bash
python process_attendance.py
```
### 2. Search Functionality
Query the logs directly via the CLI using the `--search` flag.

| Query Type | Command Example |
| :--- | :--- |
| **Employee ID** | `python process_attendance.py --search employee 10015` |
| **Date (ISO)** | `python process_attendance.py --search date 2025-09-10` |
| **Unix Timestamp** | `python process_attendance.py --search date 1757510258` |
| **Employee + Date** | `python process_attendance.py --search employee_and_date 10015 2025-09-10` |
| **Date Range** | `python process_attendance.py --search date_range 10015 2025-09-09 2025-09-10` |

## 🛠 Technical Specifications

* **Parsing Logic:** Optimized for low-memory consumption using line-by-line stream processing.
* **Time Handling:** Native support for **Unix Epoch** and **ISO 8601** formatting.
* **Extensibility:** The parser can be easily modified in `process_attendance.py` to support custom log delimiters.

