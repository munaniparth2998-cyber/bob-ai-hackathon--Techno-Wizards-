## Components

| Component | Responsibility |
|---|---|
| Alert Input | Receives security alert data |
| Preprocessing | Cleans data, removes duplicates, handles timestamps and sorts alerts |
| Correlation Engine | Groups related alerts using source IP and time proximity |
| MITRE ATT&CK Mapping | Maps suspicious activities to MITRE ATT&CK techniques |
| Risk Scoring | Calculates an explainable technique-weighted risk score |
| Forecasting | Identifies plausible next techniques using documented ATT&CK relationships |
| BLUF Report | Presents important findings and recommended actions |

## End-to-End Data Flow

1. Security alerts are provided as input.
2. Alerts are cleaned, validated and sorted.
3. Duplicate alerts and timestamp issues are handled.
4. Related alerts are correlated using the same source IP and a deterministic time window.
5. Correlated activity is mapped to MITRE ATT&CK techniques.
6. A technique-weighted risk score is calculated.
7. MITRE ATT&CK relationships are used to identify plausible next techniques.
8. The final findings and recommended actions are presented through the dashboard and BLUF report.

## Security and Explainability

The system uses deterministic rules and documented MITRE ATT&CK knowledge so that the correlation, risk score and forecast can be explained to the analyst.

Forecasting is knowledge-based and does not claim machine-learning prediction or fabricated confidence percentages.

## Scalability

The solution separates preprocessing, correlation, MITRE mapping, risk scoring, forecasting and reporting into different stages. This modular structure makes the system easier to extend with additional alert sources, techniques and analysis rules.
