```kusto
VMProcess
| where Computer == "name-of-virtual-machine"
| order by TimeGenerated
| project TimeGenerated, ExecutableName, FirstPid, StartTime, CommandLine

InsightsMetrics
|where Computer == "name-of-virtual-machine" and Namespace =="Processor" | order by TimeGenerated
```
![image](https://github.com/expertcloudconsultant/azure-log-analytics/assets/69172523/0152cb26-3f7e-4c2b-9001-ac8f00a0e570)
