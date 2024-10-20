# Heart Rate Monitoring System

## Project Overview

This project is part of an effort to improve patient monitoring and data management in hospitals. It involves the development of a system for **recording heart rate data**, **archiving logs**, and **backing them up to a remote server**. The system consists of three key scripts:

- **Heart Rate Monitoring Script**: `heart_rate_monitor.sh`
- **Log Archival Script**: `archive_log.sh`
- **Remote Backup Script**: `backup_archives.sh`

Each script performs a specific function to ensure efficient monitoring, archiving, and secure remote storage of heart rate data.

---

## Prerequisites and Setup

To use this system, ensure the following prerequisites are met:

- A Unix/Linux environment with Bash installed (pre-installed by default).
- Git installed for version control.

### Setup Instructions

1. Clone the repository and navigate to the project directory:
   ```bash
   git clone https://github.com/DphenomenalALU/hospital_monitoring_group26.git
   cd hospital_monitoring_group26
   ```

---

## Task 1: Heart Rate Monitoring

The **heart_rate_monitor.sh** script records heart rate data from a specified device and logs it into a file.

### Usage Instructions

To start recording heart rate data:

1. Run the script:
   ```bash
   ./heart_rate_monitor.sh
   ```
2. When prompted, enter the name of the recording device (e.g., "Monitor_A", "Monitor_B").
3. The script will run in the background, and its Process ID (PID) will be displayed.

### Viewing Logs

You can monitor the output log in real-time using the `tail` command:
```bash
tail -f heart_rate_log.txt
```

---

## Task 2: Log Archival

The **archive_log.sh** script renames the heart rate log file with a timestamp, creating a backup version of the log for later reference.

### Usage Instructions

To archive the log file:

1. Run the script:
   ```bash
   ./archive_log.sh
   ```
2. The original `heart_rate_log.txt` will be renamed to `heart_rate_log.txt_YYYYMMDD_HHMMSS`, where the timestamp reflects the moment of archival.

---

## Task 3: Remote Backup

The **backup_archives.sh** script automates the process of moving archived log files to a designated local directory and securely transferring them to a remote server.

### Setup SSH Access

Before running the script, update the SSH credentials (remote host and username) in the **backup_archives.sh** script to match your remote server.

### Usage Instructions

To back up the archived logs:

1. Run the script:
   ```bash
   ./backup_archives.sh
   ```
2. Enter your remote server password when prompted.
3. The archived files will be moved to the `archived_logs_group26` directory locally and securely copied to your remote server's `/home/` directory.

### Verifying Backup

To confirm successful backup, check the home directory of your remote server for the `archived_logs_group26` folder and its contents.

---

## Group Session Attendance

Throughout the development of this project, the group met regularly to discuss and implement the tasks. Below is a summary of attendance for the group meetings:

| **Session**                 | **Date (2024)** | **Present**                                          | **Absent** |
|-----------------------------|-----------------|-----------------------------------------------------|------------|
| Task Introduction & Delegation         | Thursday, Oct 17         | Ibrahim, Victor, Chelsea, Alexis | Delphin       |
| Final Testing & Documentation| Sunday, Oct 20      | Ibrahim, Victor, Chelsea  | Delphin, Alexis       |

---

## Contributors

This project was developed collaboratively by a dedicated team of students:

- **Ibrahim Opeyemi Salami**  
  Email: [i.salami@alustudent.com](mailto:i.salami@alustudent.com)  

- **Victor Akin Oladiran**  
  Email: [v.akinoladi@alustudent.com](mailto:v.akinoladi@alustudent.com)  

- **Chelsea Omondi**  
  Email: [c.omondi@alustudent.com](mailto:c.omondi@alustudent.com)  

- **Alexis-Gerald Okwa**  
  Email: [a.okwa@alustudent.com](mailto:a.okwa@alustudent.com)  

---

Thank you for using our **Heart Rate Monitoring System**! If you have any questions or feedback, feel free to contact any of the contributors listed above.

---
