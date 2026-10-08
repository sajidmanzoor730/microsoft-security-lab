# Microsoft Security Investigation Lab

Hands-on Microsoft security investigation lab focused on endpoint alert triage, Microsoft Sentinel, and KQL-based security analysis.

> **Scope:** Personal hands-on lab/project work using Microsoft 365 E5 trial capabilities. This repository does **not** represent production Microsoft security employment experience.

## What I Practiced

| Area | Experience |
|---|---|
| Microsoft Defender for Endpoint | Hands-on alert investigation |
| Microsoft Sentinel | Hands-on KQL investigation |
| KQL | 5+ queries written/tested |
| Defender for Cloud | Explored |
| Defender for Office 365 | Explored |
| Security Operations | Alert triage, prioritization, investigation workflow |

## Investigation Work

During the lab, I investigated **10+ Microsoft Defender for Endpoint alerts** involving malware/phishing scenarios.

The investigation focused on:

- Reviewing alert context and severity
- Examining affected devices and activity
- Understanding alert evidence and investigation context
- Prioritizing alerts for further investigation
- Using Microsoft security tooling to understand an end-to-end investigation workflow

## Microsoft Sentinel — KQL

I wrote and tested **5+ KQL queries** in Microsoft Sentinel to practice filtering, summarization, and investigation workflows.

### Alert severity analysis

```kql
SecurityAlert
| where TimeGenerated > ago(7d)
| summarize AlertCount = count() by AlertSeverity
| order by AlertCount desc
```

### High-severity alert review

```kql
SecurityAlert
| where TimeGenerated > ago(7d)
| where AlertSeverity == "High"
| project TimeGenerated, AlertSeverity, AlertName, ProviderName
| order by TimeGenerated desc
```

### Entity-level alert analysis

```kql
SecurityAlert
| where TimeGenerated > ago(7d)
| summarize AlertCount = count() by CompromisedEntity
| order by AlertCount desc
```

## Skills Demonstrated

- Microsoft Defender for Endpoint
- Microsoft Sentinel
- KQL
- Security alert triage
- Incident investigation
- Alert prioritization
- Technical troubleshooting
- Root-cause thinking
- Operational analytics
- Power BI
- SQL
- Python / Pandas
- Excel

## Related Analytics Work

My security investigation learning is complemented by my operations analytics projects, where I work with real project datasets and build KPI-focused analysis.

### Helpdesk KPI Dashboard

A separate analytics project using **3,672 raw ticket rows → 3,600 unique tickets**, with analysis covering SLA, CSAT, repeat tickets, MTTR, data quality, SQL-based deduplication, Power BI, Python/Pandas, and Streamlit.

Repository: https://github.com/sajidmanzoor730/helpdesk-kpi-dashboard

## What I Learned

This lab strengthened my understanding of:

1. How security alerts are surfaced and prioritized
2. How endpoint investigation fits into security operations
3. How KQL can be used to filter and summarize security telemetry
4. How structured investigation supports escalation handling
5. How security operations data can be translated into actionable analysis

## Technology Stack

**Microsoft Security:** Defender for Endpoint, Microsoft Sentinel, Defender for Cloud, Defender for Office 365  
**Querying:** KQL, SQL  
**Analytics:** Power BI, Python, Pandas, Excel  
**Operations:** Incident Management, Escalation Triage, RCA, SLA/MTTR Analysis

## Important Note

All Microsoft Security work in this repository is **hands-on lab/project experience**, completed for learning and portfolio development. It should not be interpreted as professional production experience with Microsoft security products.

---

**Sajid Manzoor**  
Data Analytics | Technical Operations | Microsoft Security  
GitHub: https://github.com/sajidmanzoor730
