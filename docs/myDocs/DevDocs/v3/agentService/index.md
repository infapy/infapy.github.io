# Agent Service

Use the AgentService function to update the status of IICS agent services

## Function: updateAgentService()

updateAgentService() updates the status of agent services

>        Args:
>            serviceName (string): Name of the agent service to update
>            serviceAction (string): Action to be performed
>            agentId (string)): Id of the agent to be updated
>
>        Returns:
>            List of dict: <Status message of the aent service update>

### Example


```python
import infapy

#Create infa handler
infaHandler = infapy.connect(profile="jefjames")
v3=infaHandler.v3()

#Call updateAgentService()
sName = "OI Data Collector"
sAction = "start"
agentId = "jGbv2pNa8qukzzKDNZsCI6"
response=v3.AgentService().updateAgentService(sName,sAction,agentId)
print(response)
```

    {'serviceState': 'NEED_RUNNING', 'message': 'Successfully initiated START action. Note that only the latest version of the service  will be started. Send a GET request to  /v2/agent/details API to check the updated status of the service.'}
    
