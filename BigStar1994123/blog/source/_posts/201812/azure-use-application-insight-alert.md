---
title: Azure 使用 Application Insights Alert 功能
tags:
  - 工作
  - Azure 
  - Application Insights
category:
  - 工作日誌
  - 2018
  - 12月
date: 2018-12-19 19:04:38
---
[看這裡](https://edwardkuo.imas.tw/paper/2017/01/31/Devops/Teams/MicrosoftTeamsAI/)  
https://www.rickvanrousselt.com/send-your-application-insights-alert-data-to-microsoft-teams/  
https://blog.poychang.net/how-to-query-and-analytics-application-insights-log/  
https://docs.microsoft.com/en-us/azure/kusto/query/iiffunction

```
union (traces),(exceptions)
| where (tostring(customDimensions[‘StatusCode’]) == ‘500’) and (timestamp > ago(4h))
| top 101 by timestamp desc
```