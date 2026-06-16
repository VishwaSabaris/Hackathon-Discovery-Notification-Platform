# Hackathon Discovery & Notification Platform

A Python-based automation platform that discovers hackathon opportunities from online platforms, stores structured data in Excel, and sends automated email notifications using n8n Email Node.

This project helps students stay updated with hackathons without manually searching multiple websites.

---

## Demo

### Current Status

- Devpost hackathon scraping completed
- Unstop hackathon scraping completed
- Hackathon data stored in Excel
- Automated workflow execution using Python scripts
- Email notification delivery handled through n8n Email Node
- Queue-based worker logic included for automation flow

---

## Key Features

- Scrapes hackathon details from Devpost and Unstop
- Extracts structured information such as title, deadline, platform, and application link
- Stores collected hackathon data in Excel format
- Supports automated workflow execution through worker scripts
- Sends email notifications using n8n Email Node
- Designed to reduce manual hackathon searching for students
- Modular code structure for adding more platforms in the future

---

## Architecture Diagram

![Architecture](docs/architecture.png)

---

## Workflow Diagram

![Workflow](docs/workflow.png)

---

## Project Overview

Students often miss hackathon opportunities because details are spread across multiple platforms. This project automates the discovery and notification process.

The system scrapes hackathon listings from platforms such as Devpost and Unstop, processes the collected data, stores it in an Excel file, and uses n8n to send automated email notifications.

---

## Problem Statement

Manually searching for hackathons across different platforms is time-consuming and inefficient. Students may miss deadlines because there is no centralized notification system.

This project solves the problem by creating an automated pipeline that:

1. Collects hackathon details from online platforms
2. Converts unstructured web data into structured Excel data
3. Sends automated email notifications through n8n
4. Helps students discover opportunities faster

---

## Tech Stack

### Programming Language

- Python

### Web Scraping

- Playwright
- Requests / Browser Automation Logic

### Data Storage

- Excel

### Automation

- n8n
- n8n Email Node
- Worker-based processing

### Tools

- Git
- GitHub
- VS Code
- Linux

---

## Project Structure

```text
E-mail-Automation/
│
├── devpost.py
├── unstop.py
├── excel_writer.py
├── run_all.py
├── worker.py
│
├── docs/
│   ├── architecture.png
│   └── workflow.png
│
├── requirements.txt
├── LICENSE
├── .gitignore
└── README.md
```

---

## How It Works

1. `devpost.py` scrapes hackathon details from Devpost.
2. `unstop.py` scrapes hackathon details from Unstop.
3. Extracted data is cleaned and converted into a structured format.
4. `excel_writer.py` stores the final hackathon data in an Excel file.
5. `worker.py` supports automated processing logic.
6. n8n reads or receives the processed hackathon data.
7. n8n Email Node sends automated email notifications to students.

---

## Data Fields

The Excel file can contain fields such as:

| Field | Description |
|---|---|
| Title | Name of the hackathon |
| Platform | Source platform such as Devpost or Unstop |
| Deadline | Last date to apply |
| Apply Link | Registration or application URL |
| Date Added | Date when the opportunity was collected |
| Status | Notification or processing status |

---

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/VishwaSabaris/E-mail-Automation.git
cd E-mail-Automation
```

### 2. Create Virtual Environment

```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
playwright install
```

---

## Usage

Run the complete automation pipeline:

```bash
python run_all.py
```

Run individual scrapers:

```bash
python devpost.py
python unstop.py
```

The generated Excel file can then be used in the n8n workflow to send email notifications.

---

## n8n Email Workflow

The email notification part is handled using n8n Email Node.

### Workflow Logic

```text
Excel Hackathon Data
      ↓
n8n Workflow
      ↓
Read / Process Hackathon Records
      ↓
Email Node
      ↓
Send Notification to Students
```

---

## Future Improvements

- Google Sheets integration
- Duplicate hackathon detection
- Deadline-based filtering
- Email personalization
- Web dashboard for viewing opportunities
- Database storage using SQLite or PostgreSQL
- Scheduled scraping using cron or GitHub Actions
- Multi-platform support beyond Devpost and Unstop
- Deployment on cloud server

---

## Learning Outcomes

Through this project, I gained practical experience in:

- Web scraping
- Browser automation
- Data extraction and cleaning
- Excel automation
- Workflow automation using n8n
- Email automation
- Python scripting
- Modular project design

---

## Author

**Vishwa Sabaris V**

B.E. Computer Science and Engineering (Artificial Intelligence & Machine Learning)

Kalaignar Karunanidhi Institute of Technology (KIT), Coimbatore
