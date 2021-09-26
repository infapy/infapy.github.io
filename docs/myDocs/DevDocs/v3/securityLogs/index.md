# GetSecurityLogs

Use this resource to receive security log entries. Security logs include information about events such as login actions and creating, updating, and deleting users, user groups, and roles. To use this resource, you must be logged in with an administrator role.


```python
import infapy

infapy.setFileLogger(name="test",level="DEBUG")
infaHandler = infapy.connect(profile="DEV")

v3 = infaHandler.v3()
securityLogs = v3.getSecurityLogs()
```

## Function: getSecurityLogsForLastOneDay()

>        getSecurityLogsForLastOneDay
>
>        Returns:
>            list of dict: The response of the security logs in the last one day


```python
lastOneDayLogs = securityLogs.getSecurityLogsForLastOneDay()
print(lastOneDayLogs)
```

   
    

## Function: getSecurityLogsByCustomQuery()

>        getSecurityLogsByCustomQuery
>
>        Args:
>            query (String): Pass the query string
>
>        Returns:
>            list of dict: The response of the security logs in json

To build the Query. Review the product docs
https://docs.informatica.com/integration-cloud/cloud-platform/current-version/rest-api-reference/platform-rest-api-version-3-resources/securitylog.html


```python
query = "entryTime>=\"2021-09-25T08:00:00.000Z\";entryTime<=\"2021-09-26T17:00:00.000Z\""
print(query)

response = securityLogs.getSecurityLogsByCustomQuery(query=query)
print(response)
```

    
