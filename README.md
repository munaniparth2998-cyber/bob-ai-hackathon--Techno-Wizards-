# Threat Correlation & Forecasting Assistant

> An explainable security alert analysis solution that converts scattered alerts into prioritized attack stories for SOC analysts.

---

## 👥 Team

| Field | Value |
| --- | --- |
| **Team Name** | Techno Wizards |
| **Track** | AI |
| **Team Lead** | Parth Munani — 26dce053@charusat.edu.in |
| **Members** | Pari Desai, Prinsi Babariya, Kartik Jha |

---

## 🎯 Problem Statement

Security Operations Centers (SOCs) receive thousands of security alerts every day, making it difficult for analysts to identify which alerts are connected to a larger attack.

Related alerts are often viewed as separate events, so analysts must manually examine IP addresses, timestamps, and event sequences to understand the complete attack story and prioritize high-risk activity.

---

## 💡 Solution

Threat Correlation & Forecasting Assistant converts scattered security alerts into a prioritized and explainable attack story.

The system preprocesses alerts, correlates related events using source IP and time proximity, maps suspicious activity to MITRE ATT&CK techniques, calculates an explainable risk score, forecasts plausible next techniques using documented ATT&CK relationships, and generates a BLUF (Bottom Line Up Front) report.

---

## ✨ Key Features

- **Alert Correlation:** Groups related alerts using the same source IP and a deterministic time window.
- **MITRE ATT&CK Mapping:** Provides standardized context for observed attacker techniques.
- **Explainable Risk Scoring:** Uses technique-weighted scores so analysts can understand why activity is considered high or medium risk.
- **Knowledge-Based Forecasting:** Identifies plausible next techniques using the observed attack sequence and documented MITRE ATT&CK relationships.
- **BLUF Report:** Summarizes important findings and recommended actions for faster analyst decision-making.

---

## 🛠️ Tech Stack

| Category | Technologies |
| --- | --- |
| **Languages** | Python, JavaScript, HTML, CSS |
| **Frameworks** | None |
| **IBM Technologies** | None |
| **Databases** | None |
| **Other** | Git, GitHub, MITRE ATT&CK |

---

## 📁 Repository Structure

├── src/                  # Source code and project data
├── docs/                 # Project documentation
│   ├── problem-statement.md
│   ├── solution-overview.md
│   ├── architecture.md
│   └── setup-guide.md
├── demo/                 # Demo artifacts
│   ├── screenshots/
│   ├── demo-video-link.txt
│   └── live-demo-url.txt
├── presentation/         # Slide deck
└── submission.yaml       # Submission metadata

---

## ⚡ How to Run

For complete setup instructions, see `docs/setup-guide.md`.

1. Open `src/index.html` in a modern web browser to view the dashboard.
2. Open a terminal and move into the `src` directory.
3. Run the alert-processing script:

python correlate_alerts.py

If your system uses Python 3 as `python3`, run:

python3 correlate_alerts.py

The project uses the provided `alerts.csv` sample dataset for the analysis workflow.

---

## 🖥️ Demo

| Artifact | Location |
| --- | --- |
| 📹 **Demo Video** | `demo/demo-video-link.txt` |
| 🌐 **Live Demo** | `demo/live-demo-url.txt` |
| 🖼️ **Screenshots** | `demo/screenshots/` |
| 📊 **Presentation** | `presentation/` |

---

## ⚠️ Known Limitations

- Forecasting is knowledge-based and uses documented MITRE ATT&CK relationships; it is not a machine-learning prediction model.
- Risk scoring is project-defined and inspired by structured CVSS-like principles; it is not official CVSS scoring.
- The current implementation uses a sample alert dataset and deterministic correlation rules.
- A live production deployment is not currently provided.

---

## 🏅 What We're Most Proud Of

We are most proud of turning fragmented security alerts into a clear and explainable attack story.

The solution combines alert correlation, MITRE ATT&CK context, explainable risk scoring, knowledge-based forecasting, and BLUF reporting in one workflow. This helps SOC analysts move from large volumes of scattered alerts toward prioritized and actionable security findings.
