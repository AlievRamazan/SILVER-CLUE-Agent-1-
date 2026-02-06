# SILVER CLUE 🕵️‍♂️🤖

> **Private AI Employees for Your Business.**  
> Automate routine financial processes with secure, modular AI assistants deployed on your own server.

![Status](https://img.shields.io/badge/Status-MVP%20Prototype-success)
![Python](https://img.shields.io/badge/Built%20With-Python%20%7C%20Tkinter%20%7C%20Pandas-blue)
![Privacy](https://img.shields.io/badge/Data-Local%20%26%20Private-green)

## 📖 Overview

**SILVER CLUE** is a modular automation platform designed to save small businesses money and time by replacing routine operational tasks. 

This repository contains the source code for the **Check Reader** and **Accountant** modules—a desktop application that automates the extraction of data from payment receipts and manages client debt tracking without requiring data to leave your local environment.

**Why Silver Clue?**
*   **Privacy First:** Unlike public AI (ChatGPT), this solution runs locally. Your financial data never leaves your machine.
*   **Routine Automation:** Automates data entry from PDF receipts into structured Excel reports.
*   **Financial Health:** Tracks client debts, payments, and discounts automatically.

## 🚀 Features (Implemented in MVP)

Based on the provided Python prototype, the current application supports:

### 1. 📄 Intelligent Receipt Analysis (`Check Reader` Module)
*   **Pattern Matching Engine:** Uses Regex-based learning patterns to parse receipts (specifically optimized for **Sberbank** transfers).
*   **Data Extraction:** Automatically extracts:
    *   Sender/Receiver Name (FIO)
    *   Transaction Amount
    *   Date & Time
    *   Phone Numbers & Account Fragments
*   **Batch Processing:** Analyze multiple PDF files simultaneously.
*   **Duplicate Protection:** Uses MD5 file hashing to prevent processing the same receipt twice.

### 2. 💰 Financial Management (`Accountant` Module)
*   **Client Database:** Local SQLite database storing client profiles and transaction history.
*   **Debt Tracking:** Automatically calculates total debt vs. paid amount.
*   **Manual Entry:** UI for adding manual payments (cash) or applying discounts.
*   **Smart Matching:** Auto-creates new client profiles if the receipt name doesn't exist in the database.

### 3. 📊 Reporting
*   **Beautiful Excel Export:** Generates formatted `.xlsx` reports using `openpyxl`.
    *   *Clients Sheet:* Debt summary, payment counts.
    *   *History Sheet:* Detailed transaction logs with color-coding for manual vs. auto entries.

## 🛠️ Technical Stack

The project is built entirely in **Python** to ensure modularity and ease of deployment.

*   **GUI:** `tkinter` (Native desktop interface).
*   **Data Processing:** `pandas` (Data manipulation), `re` (Regular expressions).
*   **Database:** `sqlite3` (Serverless, local file storage for zero-setup deployment).
*   **File Handling:** `PyPDF2` (PDF text extraction), `openpyxl` (Excel generation).

## 📦 Installation & Usage

### Prerequisites
*   Python 3.8+
*   Pip (Python Package Manager)

### Setup

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/silver-clue.git
    cd silver-clue
    ```

2.  **Install dependencies:**
    ```bash
    pip install pandas openpyxl PyPDF2
    ```
    *(Note: `tkinter` and `sqlite3` are included in standard Python installations).*

3.  **Run the Application:**
    ```bash
    python main.py
    ```

### How to Use
1.  **Analyze Receipts:** Click "Analyze Receipts" and select PDF files from your computer. The system will parse them and populate the database.
2.  **Manage Clients:** View client debts, edit details, or apply discounts via the "Manage Clients" dashboard.
3.  **Export:** Click "Export to Excel" to get a full financial report.

## 🤖 Module Roadmap

The Silver Clue vision includes a library of interchangeable modules. This repository currently implements the **Finance Core**.

| Module | Status | Description |
| :--- | :--- | :--- |
| **📄 Check Reader** | ✅ **Active** | OCR/Regex parsing of receipt data. |
| **💳 Accountant** | ✅ **Active** | Ledger management, debt calculation, Excel export. |
| **📊 Financial Analyst** | 🚧 Planned | P&L reports and cashflow forecasting. |
| **💬 Client Bot** | 🚧 Planned | 24/7 Telegram/WhatsApp support bot. |
| **🚚 Logistics** | 🚧 Planned | Route optimization and SDEK integration. |

## 💰 Business Value

*   **Target Audience:** Small businesses in Retail, Services, and Logistics.
*   **ROI:** Saves ~67% of employee time spent on data entry.
*   **Cost Efficiency:** Replaces the need for manual bookkeeping for routine transactions.


---
*© 2025 SILVER CLUE. All rights reserved.*
