# ActivityMonitor

Use ActivityMonitor resource to request log information for running jobs from the Monitor service. To request log information for completed jobs, use the ActivityLog resource.

## Function: getActivityMonitorLog()

getActivityMonitorLog() returns activity logs for running jobs in IICS.

>        Args:
>            details (str, optional): Returns log information for tasks, linear taskflows, and child objects 
>                                     if set to true. Defaults to "false", since it is IICS default.
>
>        Returns:
>            List of dict: <Activity Monitor Log in dict Format>

### Example:


```python
import infapy

# create infa handler
infaHandler = infapy.connect(profile="spani")
v2=infaHandler.v2()

# Perform getActivityMonitorLog()
ActivityMonitor=v2.getActivityMonitor()
print(ActivityMonitor.getActivityMonitorLog())
```

    [{'@type': 'activityMonitoryEntry', 'id': '0119Y40E000000000Q3D', 'type': 'MTT', 'taskId': '0119Y40Z00000000001S', 'taskName': 'MT_Warning', 'objectName': '', 'runId': 20, 'startTime': '2021-09-26T02:37:42.000Z', 'executionState': 'RUNNING', 'failedSourceRows': 0, 'successSourceRows': 0, 'failedTargetRows': 0, 'successTargetRows': 0, 'entries': [], 'agentId': '0119Y40800000000000A', 'startedBy': 'admin021651', 'runContextType': 'ICS_UI', 'runtimeEnvironmentId': '0119Y425000000000003'}]
    
