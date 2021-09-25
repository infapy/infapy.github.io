# Hello World Infapy


```python
import infapy
```

 ## Enabling File Logging


```python
infapy.setFileLogger(name="test",level="DEBUG")
```

## Creating Infa Handler


```python
infaHandler = infapy.connect(profile="jefjames")
v2=infaHandler.v2()
```

## Method: getAllRuntimeEnvironments()
### _getAllRuntimeEnvironments returns the details of All the Runtime Environments_


```python
runEnvId = "000QML2500000000002Z"
runEnvDetails = v2.getRuntimeEnvironment().getRuntimeEnvironmentById(runEnvId)
```


```python
print("Runtime Environment Details:")
print(runEnvDetails)
```

    Runtime Environment Details:
    {'@type': 'runtimeEnvironment', 'id': '000QML2500000000002Z', 'orgId': '000QML', 'name': 'infoca-dev-mesa', 'createTime': '2020-11-18T03:33:00.000Z', 'updateTime': '2020-11-18T03:33:00.000Z', 'createdBy': 'repro_user', 'updatedBy': 'repro_user', 'agents': [], 'isShared': False, 'federatedId': 'hgIuSJzoxMTlXWmdvs3RWr', 'createTimeUTC': '2020-11-18T08:33:00.000Z', 'updateTimeUTC': '2020-11-18T08:33:00.000Z', 'serverlessConfig': {'cloudProviderConfig': {'cloudConfig': []}}}
    
