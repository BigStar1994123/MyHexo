---
title: Azure 使用 Application Insights Alert 功能
tags:
  - Azure 
  - Application Insights
category:
  - Azure
date: 2018-12-19 19:04:38
---
[看這裡](https://edwardkuo.imas.tw/paper/2017/01/31/Devops/Teams/MicrosoftTeamsAI/)  

https://www.rickvanrousselt.com/send-your-application-insights-alert-data-to-microsoft-teams/  

https://blog.poychang.net/how-to-query-and-analytics-application-insights-log/  

https://docs.microsoft.com/en-us/azure/kusto/query/iiffunction  

```SQL
union (traces),(exceptions)
| where (tostring(customDimensions[‘StatusCode’]) == ‘500’) and (timestamp > ago(4h))
| top 101 by timestamp desc
```
