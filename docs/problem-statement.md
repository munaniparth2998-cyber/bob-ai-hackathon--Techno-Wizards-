# Problem Statement

## Background

Security Operations Centers (SOCs) receive thousands of security alerts every day. The large volume of alerts makes it difficult for analysts to quickly identify the alerts that are part of a larger attack.

## Core Problem

The main challenge is that related security alerts are often viewed as separate and independent events. Attackers may move through multiple stages, while SOC logs provide only fragmented snapshots of their activity.

This makes it difficult for analysts to understand the complete attack story, identify multi-stage campaigns, and decide which incidents require immediate attention.

## Who Is Affected

SOC analysts and security teams are directly affected by this problem. They need to manually examine alert sources, IP addresses, timestamps, and event sequences to determine whether multiple alerts are connected.

## Limitations of the Traditional Approach

When alerts are handled individually:

- Important signals can be hidden by large amounts of background alert noise.
- Analysts must manually correlate IP addresses and timestamps.
- Relationships between multiple attack stages can be difficult to recognize.
- Prioritising active and high-risk attack chains takes additional time.
- Multi-stage attacks may progress while analysts are still investigating individual alerts.

## Why This Problem Matters

Fast and accurate alert triage is important because security teams need to understand attacker progression and respond before an attack advances further.

The project sample evaluation demonstrates the scale of the alert-correlation challenge, with 203 raw alerts being reduced to 184 correlated groups and 5 identified attack chains.

## Project Goal

The goal of the Threat Correlation & Forecasting Assistant is to transform scattered security alerts into a prioritised and explainable threat story.

The system aims to reduce manual correlation effort by grouping related alerts, providing MITRE ATT&CK context, calculating an explainable risk score, identifying plausible next techniques, and presenting actionable findings to SOC analysts.
