# **Project Structure**

attendance_logs/          # Input folder for log files (.log, .csv)
attendance_reports/       # Output folder for generated reports
process_attendance.py     # Main script
README.md                # This file



1. Create venv
2. Run pip install -r [requirements.txt](requirements.txt)
3. Run python [process_attendance.py](process_attendance.py)

# **Search by Employee Code**

### Search by Employee Code

    python3 process_attendance.py --search employee 10015

### Search by Date

    python3 process_attendance.py --search date 1757510258
    or
    python3 process_attendance.py --search date 2025-09-10

### Search by Employee and Date

    python3 process_attendance.py --search employee_and_date 10015 1757510258 
    or
    python3 process_attendance.py --search employee_and_date 10015 2025-09-10 

### Search by Date Range

    python3 process_attendance.py --search date_range 10015 1757510258 1857510258
    or
    python3 process_attendance.py --search date_range 10015 2025-09-09 2025-09-10

