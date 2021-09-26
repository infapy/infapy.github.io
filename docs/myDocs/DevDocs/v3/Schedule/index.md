# Schedule

Use this resource to request details of the schedules in the organization. You can also use this resource to create, update, or delete schedules.
You can use the following request methods:
* To get schedule details, use a GET request.
* To create a schedule, use a POST request.
* To update a schedule, use a PATCH request.
* To delete a schedule, use a DELETE request.

>    To leverage full scheduling capabilities, use this resource instead of the version 2 schedule resource.

## Function: getAllSchedules()

getAllSchedules() returns details for all Schedules in the Org.

>       Returns:
>            List of dict: <Schedule Details in dict Format>


### Example:


```python
import infapy

# create infa handler
infaHandler = infapy.connect(profile="spani")
v3=infaHandler.v3()

# Perform getAllSchedules()
Schedule=v3.schedule()
print(Schedule.getAllSchedules())
```

    {'count': 3, 'schedules': [{'id': '9dMjYg78QCpewd7iS939IzD0000000000002', 'createTime': '2020-08-05T13:56:00.000Z', 'updateTime': '2020-11-04T12:46:58.000Z', 'createdBy': None, 'updatedBy': None, 'name': 'MI_FILE_LISTENER_14738', 'rangeStartTime': None, 'rangeEndTime': None, 'status': 'enabled', 'frequency': 1, 'description': 'This schedule is used as File Listener trigger and must not be modified or used for other purpose', 'mon': False, 'tue': False, 'wed': False, 'thu': False, 'fri': False, 'sat': False, 'sun': False, 'weekDay': False, 'dayOfMonth': 0, 'weekOfMonth': None, 'dayOfWeek': None, 'scheduleFederatedId': '8o3SVtzcC4ocMmQhnP7mCv', 'startTime': '2020-08-05T07:00:00.000Z', 'endTime': '2020-08-06T06:55:00.000Z', 'interval': 'Daily'}, {'id': '9dMjYg78QCpewd7iS939IzD0000000000005', 'createTime': '2021-01-06T12:00:03.000Z', 'updateTime': '2021-01-07T09:59:58.000Z', 'createdBy': None, 'updatedBy': None, 'name': 'MI_FILE_LISTENER_16901', 'rangeStartTime': None, 'rangeEndTime': None, 'status': 'enabled', 'frequency': 1, 'description': 'This schedule is used as File Listener trigger and must not be modified or used for other purpose', 'mon': False, 'tue': False, 'wed': False, 'thu': False, 'fri': False, 'sat': False, 'sun': False, 'weekDay': False, 'dayOfMonth': 0, 'weekOfMonth': None, 'dayOfWeek': None, 'scheduleFederatedId': '8eFSBGozSpbdyd4qzVV5E9', 'startTime': '2021-01-05T18:30:00.000Z', 'endTime': None, 'interval': 'Daily'}, {'id': '9dMjYg78QCpewd7iS939IzD0000000000007', 'createTime': '2021-04-05T14:35:55.000Z', 'updateTime': '2021-04-05T14:35:55.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'name': 'TASKFLOW_CMD_ISSUE', 'rangeStartTime': None, 'rangeEndTime': None, 'status': 'enabled', 'frequency': 15, 'description': None, 'mon': True, 'tue': True, 'wed': True, 'thu': True, 'fri': True, 'sat': True, 'sun': True, 'weekDay': False, 'dayOfMonth': 0, 'weekOfMonth': None, 'dayOfWeek': None, 'scheduleFederatedId': '9GROQi3ZyIufwF9yzLtx0I', 'startTime': '2021-04-05T15:00:20.000Z', 'endTime': None, 'interval': 'Minutely'}]}
    

## Function: getScheduleById()

getScheduleById() returns details for the schedule as specified by the Id.

>       Args:
>            id (string): Schedule Id.
>
>        Returns:
>            dict: <Schedule Details in dict Format>


### Example:


```python
import infapy

# create infa handler
infaHandler = infapy.connect(profile="spani")
v3=infaHandler.v3()

# Perform getScheduleById()
Schedule=v3.schedule()
print(Schedule.getScheduleById("9dMjYg78QCpewd7iS939IzD0000000000002"))
```

    {'id': '9dMjYg78QCpewd7iS939IzD0000000000002', 'createTime': '2020-08-05T13:56:00.000Z', 'updateTime': '2020-11-04T12:46:58.000Z', 'createdBy': None, 'updatedBy': None, 'name': 'MI_FILE_LISTENER_14738', 'rangeStartTime': None, 'rangeEndTime': None, 'status': 'enabled', 'frequency': 1, 'description': 'This schedule is used as File Listener trigger and must not be modified or used for other purpose', 'mon': False, 'tue': False, 'wed': False, 'thu': False, 'fri': False, 'sat': False, 'sun': False, 'weekDay': False, 'dayOfMonth': 0, 'weekOfMonth': None, 'dayOfWeek': None, 'scheduleFederatedId': '8o3SVtzcC4ocMmQhnP7mCv', 'startTime': '2020-08-05T07:00:00.000Z', 'endTime': '2020-08-06T06:55:00.000Z', 'interval': 'Daily'}
    

## Function: getSchedulesWithQuery()

getScheduleWithQuery() returns details for the schedules as specified by the filter query provided.

>       Args:
>            query (string): Filter Query to filter out Schedules.
>
>        Returns:
>            list of dict: <Schedule Details in dict Format>

You can use the following query parameters in the URI:
    
| Parameter | Type | Description |
| :-------- | :--- | :---------- |
| status | Boolean | Status of the schedule.<br>You can use the following operators: <ul id="GUID-C2F65D9E-CD14-4848-B0FD-D93B9533902A_UL_A37B26E2911343638944A7EC9FE25E48" class="ul"><div  style="display: inline;"><li id="GUID-C2F65D9E-CD14-4848-B0FD-D93B9533902A_LI_F30F80B3E95D4C8882A754DA7B08C6EC" class="li"><div  style="display: inline;">==</div></li><li id="GUID-C2F65D9E-CD14-4848-B0FD-D93B9533902A_LI_4B201B9A565A4AECA48194D85C28DA42" class="li"><div  style="display: inline;">!=	</div></li></div></ul> |
| id | String | Schedule ID.<br>Use the == operator. |
    | scheduleFederatedId | String | 	Federated schedule ID.<br>Use the == operator. |
    | name | String | Schedule name.<br>Use the == operator.<br><br>If the schedule name includes a space, replace the space with %20 |
    | updateTime | Date | Last time the schedule was updated, in UTC format.<br>You can use the following operators: <ul><li>&lt;</li><li>&lt;=</li><li>==</li><li>=&gt;</li><li>&gt;</li><li>!=</li></ul> |
    | updatedBy | String | User who updated the schedule.<br>Use the == operator. |
    | createdBy | String | User who created the schedule.<br>Use the == operator. |
    | interval | String | Interval or repeat frequency at which the schedule runs. You can use the following values:<ul><li>None</li><li>Minutely</li><li>Hourly</li><li>Daily</li><li>Weekly</li><li>Biweekly</li><li>Monthly</li></ul>You can use the following operators:<ul><li>==</li><li>!=</li></ul>|

### Example:


```python
import infapy

# create infa handler
infaHandler = infapy.connect(profile="spani")
v3=infaHandler.v3()

# Perform getSchedulesWithQuery()
Schedule=v3.schedule()
print(Schedule.getSchedulesWithQuery("status=='enabled' and createdBy=='admin021651'"))
```

    {'count': 1, 'schedules': [{'id': '9dMjYg78QCpewd7iS939IzD0000000000007', 'createTime': '2021-04-05T14:35:55.000Z', 'updateTime': '2021-04-05T14:35:55.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'name': 'TASKFLOW_CMD_ISSUE', 'rangeStartTime': None, 'rangeEndTime': None, 'status': 'enabled', 'frequency': 15, 'description': None, 'mon': True, 'tue': True, 'wed': True, 'thu': True, 'fri': True, 'sat': True, 'sun': True, 'weekDay': False, 'dayOfMonth': 0, 'weekOfMonth': None, 'dayOfWeek': None, 'scheduleFederatedId': '9GROQi3ZyIufwF9yzLtx0I', 'startTime': '2021-04-05T15:00:20.000Z', 'endTime': None, 'interval': 'Minutely'}]}
    

## Function: createSchedule()

createSchedule() creates a Schedule based on the information provided in the Body. For configuration of body, please refer to: 
            https://docs.informatica.com/integration-cloud/cloud-platform/current-version/rest-api-reference/platform-rest-api-version-3-resources/schedule.html
            
>       Args:
>            body (dict): JSON body for POST request.
>
>        Returns:
>            dict: <Status of Create Schedule Request in dict Format>


### Example:


```python
import infapy

# create infa handler
infaHandler = infapy.connect(profile="spani")
v3=infaHandler.v3()

#create JSON body
createBody= {
    "name": "TEST_SCHEDULE_API",
    "status": "enabled",
    "frequency": 15,
    "dayOfMonth": 0,
    "scheduleFederatedId": "9GROQi3ZyIufwF9yzLtx0I",
    "startTime": "2021-04-05T15:00:20.000Z",
    "interval": "Minutely"
}

# Perform createSchedule()
Schedule=v3.schedule()
print(Schedule.createSchedule(createBody))
```

    {'id': '9dMjYg78QCpewd7iS939IzD000000000000A', 'createTime': '2021-09-26T12:37:01.000Z', 'updateTime': '2021-09-26T12:37:01.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'name': 'TEST_SCHEDULE_API', 'rangeStartTime': None, 'rangeEndTime': None, 'status': 'enabled', 'frequency': 15, 'description': None, 'mon': False, 'tue': False, 'wed': False, 'thu': False, 'fri': False, 'sat': False, 'sun': False, 'weekDay': False, 'dayOfMonth': 0, 'weekOfMonth': None, 'dayOfWeek': None, 'scheduleFederatedId': '9GROQi3ZyIufwF9yzLtx0I', 'startTime': '2021-04-05T15:00:20.000Z', 'endTime': None, 'interval': 'Minutely'}
    

## Function: updateSchedule()

updateSchedule() updates a Schedule with specified Id based on the information provided in the Body. For configuration of body, please refer to: 
            https://docs.informatica.com/integration-cloud/cloud-platform/current-version/rest-api-reference/platform-rest-api-version-3-resources/schedule.html

>       Args:
>            body (dict): JSON body for POST request.
>            id (string): Schedule Id.
>
>        Returns:
>            dict: <Status of Update Schedule Request in dict Format>


### Example:


```python
import infapy

# create infa handler
infaHandler = infapy.connect(profile="spani")
v3=infaHandler.v3()

#create JSON body
updateBody={
    "schedules":[
        {
    "id": "9dMjYg78QCpewd7iS939IzD000000000000A",
    "name": "TEST_SCHEDULE_API_V2",
    "status": "disabled",
    "frequency": 15,
    "description": "V2 API",
    "scheduleFederatedId": "9GROQi3ZyIufwF9yzLtx0I"
}
    ]
}

# Perform updateSchedule()
Schedule=v3.schedule()
print(Schedule.updateSchedule(updateBody,"9dMjYg78QCpewd7iS939IzD000000000000A"))
```

    {'id': '9dMjYg78QCpewd7iS939IzD000000000000A', 'createTime': '2021-09-26T12:37:01.000Z', 'updateTime': '2021-09-26T12:39:34.742Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'name': 'TEST_SCHEDULE_API_V2', 'rangeStartTime': None, 'rangeEndTime': None, 'status': 'disabled', 'frequency': 15, 'description': 'V2 API', 'mon': False, 'tue': False, 'wed': False, 'thu': False, 'fri': False, 'sat': False, 'sun': False, 'weekDay': False, 'dayOfMonth': 0, 'weekOfMonth': None, 'dayOfWeek': None, 'scheduleFederatedId': '9GROQi3ZyIufwF9yzLtx0I', 'startTime': '2021-04-05T15:00:20.000Z', 'endTime': None, 'interval': 'Minutely'}
    

## Function: deleteSchedule()

deleteSchedule() deletes Schedule as specified by the Id.

>       Args:
>            id (string): Schedule Id.
>
>        Returns:
>            dict: <Status of Delete Schedule Request in dict Format>


### Example:


```python
import infapy

# create infa handler
infaHandler = infapy.connect(profile="spani")
v3=infaHandler.v3()

# Perform deleteSchedule()
Schedule=v3.schedule()
print(Schedule.deleteSchedule("9dMjYg78QCpewd7iS939IzD000000000000A"))
```

    {'Status': 'Schedule 9dMjYg78QCpewd7iS939IzD000000000000A has been deleted.'}
    
