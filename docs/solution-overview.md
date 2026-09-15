# Solution Overview

## Overview

Threat Correlation & Forecasting Assistant converts scattered security alerts into a prioritized and explainable attack story for SOC analysts.

The system processes raw alerts, cleans and validates the data, correlates related alerts, maps suspicious activity to MITRE ATT&CK techniques, calculates an explainable risk score, forecasts plausible next techniques, and produces an actionable BLUF (Bottom Line Up Front) report.

## How the Solution Works

The solution follows a deterministic processing pipeline:

Raw Alerts → Preprocessing → Correlation → MITRE ATT&CK → Risk Score → Forecast → BLUF Report

### 1. Alert Preprocessing

The system cleans and validates incoming alert data. Duplicate alerts are removed, corrupt timestamps are handled, and events are ordered chronologically.

### 2. Alert Correlation

Related alerts are grouped using the same source IP and a close time window. The core rule is:

Same Source IP + Close Time Window = Related Activity

This converts fragmented alerts into a coherent attack timeline.

### 3. MITRE ATT&CK Mapping

Suspicious activities are mapped to standardized MITRE ATT&CK techniques. This provides a common framework for understanding attacker behavior.

### 4. Explainable Risk Scoring

The system assigns technique-weighted point scores to the observed attack chain. Higher-impact techniques contribute higher scores, making the reason for the overall risk level transparent to analysts.

The risk score is project-defined and is inspired by structured CVSS-like principles; it is not official CVSS.

### 5. Knowledge-Based Forecasting

The system uses the observed chronological attack chain and documented MITRE ATT&CK relationships to identify plausible next techniques.

This is knowledge-based forecasting, not machine-learning prediction. The system does not create fabricated confidence percentages.

### 6. BLUF Report

Finally, the system produces a Bottom Line Up Front report containing the important findings and recommended action so that analysts can quickly understand and respond to the threat.

## What Makes the Solution Different

Instead of treating alerts as isolated events, the solution combines correlation, MITRE ATT&CK context, explainable risk scoring, and knowledge-based forecasting into one workflow.

The approach is deterministic and transparent, allowing analysts to understand why alerts were grouped, why a risk score was assigned, and why a particular next technique was considered plausible.

## User Experience

The user provides security alert data through the application. The system processes the alerts and presents the resulting attack chains, MITRE techniques, risk scores, forecasted activity, and recommended actions through the dashboard and final report.

The goal is to help SOC analysts move from scattered alerts to a prioritized threat story with less manual investigation.
