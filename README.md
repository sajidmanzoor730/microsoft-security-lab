# Microsoft Security Investigation Lab

Microsoft security investigation work focused on endpoint alert triage, Microsoft Sentinel, KQL-based investigation, and security operations analysis.

![Microsoft Security Investigation Workflow](docs/investigation-workflow.svg)

## Defender for Endpoint

![Defender for Endpoint Lab Analysis](docs/defender-lab-summary.svg)

I investigated **10+ Microsoft Defender for Endpoint alerts** involving malware and phishing scenarios.

Key investigation areas:
- Alert severity and context
- Affected devices and activity
- Alert evidence
- Investigation prioritization
- Structured escalation workflow

## Microsoft Sentinel & KQL

![Microsoft Sentinel KQL Analysis](docs/sentinel-kql-summary.svg)

I wrote and tested **5+ KQL queries** covering filtering, aggregation, severity analysis, and entity-level investigation.

### Alert severity analysis

```kql
SecurityAlert
| where TimeGenerated > ago(7d)
| summarize AlertCount = count() by AlertSeverity
| order by AlertCount desc
```

### High-severity investigation

```kql
SecurityAlert
| where TimeGenerated > ago(7d)
| where AlertSeverity == "High"
| project TimeGenerated, AlertSeverity, AlertName, ProviderName
| order by TimeGenerated desc
```

### Entity-level investigation

```kql
SecurityAlert
| where TimeGenerated > ago(7d)
| summarize AlertCount = count() by CompromisedEntity
| order by AlertCount desc
```

## Security & Analytics Skills

**Microsoft Security:** Defender for Endpoint, Microsoft Sentinel, Defender for Cloud, Defender for Office 365  
**Security Analytics:** Alert Triage, Incident Investigation, Prioritization, Evidence Review, RCA Thinking  
**Querying:** KQL, SQL  
**Analytics:** Power BI, Python, Pandas, Excel  
**Operations:** Escalation Management, SLA/MTTR Analysis, Technical Troubleshooting

## Related Analytics Project

### Helpdesk KPI Dashboard

**3,672 raw ticket rows → 3,600 unique tickets**

Analysis includes SLA adherence, CSAT, repeat tickets, MTTR, data quality, SQL-based deduplication, Power BI, Python/Pandas, and Streamlit.

Repository: https://github.com/sajidmanzoor730/helpdesk-kpi-dashboard

## Investigation Workflow

**Alert → Triage → Investigate → Query → Analyze → Prioritize → Operational Outcome**

This project demonstrates the combination of technical troubleshooting, security investigation, KQL analysis, and operational reporting.

---

**Sajid Manzoor**  
Data Analytics | Technical Operations | Microsoft Security  
GitHub: https://github.com/sajidmanzoor730
