# Architecture

## System Architecture

The Threat Correlation & Forecasting Assistant follows a sequential security-analysis pipeline:

```text
Raw Security Alerts
        ↓
Alert Preprocessing
        ↓
Alert Correlation
        ↓
MITRE ATT&CK Mapping
        ↓
Technique-Weighted Risk Score
        ↓
Knowledge-Based Forecast
        ↓
BLUF Security Report
