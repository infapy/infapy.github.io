# Server Time

## Function: getServerTime()

getServerTime() returns all the activity logs from IICS in dict format

>        Returns:
>            List of dict: <Local Time of the IICS Server>

### Example


```python
import infapy

# create infa handler
infaHandler = infapy.connect(profile="jefjames")
v2=infaHandler.v2()

# Get the Server Time
serverTime = v2.getServerTime()
print(serverTime)
```

    {'@type': 'serverTime', 'time': '2021-09-26T15:43:19.308Z'}
    
