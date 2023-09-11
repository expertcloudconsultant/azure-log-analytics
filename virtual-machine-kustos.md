```kusto
VMProcess
| where Computer == "name-of-virtual-machine"
| order by TimeGenerated
| project TimeGenerated, ExecutableName, FirstPid, StartTime, CommandLine

InsightsMetrics
|where Computer == "name-of-virtual-machine" and Namespace =="Processor" | order by TimeGenerated
```
