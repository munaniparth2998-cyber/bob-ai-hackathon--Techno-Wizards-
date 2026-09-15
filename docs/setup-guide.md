# Setup Guide

> This file provides the setup and execution instructions for the Threat Correlation & Forecasting Assistant.

## Prerequisites

Before you begin, ensure you have the following installed:

- Python 3
- A modern web browser such as Google Chrome, Microsoft Edge, or Firefox
- Git (if cloning the repository locally)

The current project does not require Node.js, Docker, PostgreSQL, or an IBM Cloud account for the implemented workflow.

## Environment Variables

The current project does not require environment variables or API keys.

The `.env.example` file is kept in the project as part of the submission structure, but no real credentials are required for the current implementation.

Do not add passwords, API keys, tokens, or other secrets to the repository.

## Installation

### 1. Clone the repository

git clone https://github.com/[your-repository].git
cd [your-repository]

### 2. Project Structure

The main project files are located inside the `src/` directory:

src/
├── index.html
├── correlate_alerts.py
├── alerts.csv
├── final_report.txt
├── .env.example
└── README.md

### 3. Python Setup

Make sure Python 3 is installed.

No additional Python package installation is required for the current project unless required by the local implementation.

## Running the Application

### Web Dashboard

Open the following file from the `src/` directory in a modern web browser:

src/index.html

The dashboard provides the user interface for viewing the threat correlation and forecasting results.

### Alert Processing

Open a terminal and move into the source directory:

cd src

Run the alert-processing script:

python correlate_alerts.py

If your system uses `python3`, run:

python3 correlate_alerts.py

The script processes the provided alert data and performs the implemented correlation and analysis workflow.

## Input Data

The project uses the following sample alert dataset:

src/alerts.csv

The alert-processing workflow handles the available alert data and supports:

- Alert preprocessing
- Duplicate handling
- Timestamp handling
- Chronological ordering
- Alert correlation
- MITRE ATT&CK mapping
- Risk scoring
- Knowledge-based forecasting
- Final reporting

## Running Tests

No separate automated test suite is currently provided with the project.

For basic verification, run the Python processing script:

python correlate_alerts.py

and confirm that it completes without errors.

## Quick Demo

For a quick demonstration:

### 1. Open the dashboard

Open `src/index.html` in a modern web browser.

### 2. Process the sample alerts

Open a terminal, move into the `src` directory, and run:

python correlate_alerts.py

### 3. Review the results

Review the generated analysis and report, including:

- Correlated alert activity
- Attack chains
- MITRE ATT&CK techniques
- Risk information
- Forecasted next techniques
- Recommended actions

The project sample evaluation demonstrates the correlation workflow using the provided alert dataset.

## Troubleshooting

| Issue | Solution |
|---|---|
| `python` command is not recognised | Install Python 3 or try using `python3`. |
| Dashboard does not open | Make sure `src/index.html` exists and open it using a modern web browser. |
| Python script does not run | Make sure Python 3 is installed and run the command from the `src` directory. |
| `alerts.csv` cannot be found | Make sure `alerts.csv` is present inside the `src` directory. |
| Changes are not visible in the dashboard | Refresh the browser and make sure you are opening the latest `src/index.html` file. |
| Required project files are missing | Verify that the repository contains the complete `src/` directory and its project files. |

## Expected Result

After successful setup, the Threat Correlation & Forecasting Assistant should provide:

1. A web dashboard for viewing the project results.
2. Alert preprocessing and correlation functionality.
3. MITRE ATT&CK technique context.
4. Explainable risk scoring.
5. Knowledge-based forecasting of plausible next techniques.
6. A final BLUF report with important findings and recommended actions.
