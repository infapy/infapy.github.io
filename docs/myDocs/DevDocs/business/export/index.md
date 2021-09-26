# Export

Use this resource with the import resource to migrate objects from one organization to another.

## Prerequisite - Identify the object ids

The first step in performing the migration is to identify the object id of the object you are trying to migrate. In this example, we will be using a test mapping task which we will be migrating.

### Example code to identify the object id of the mapping task we are trying to migrate


```python
import infapy

infapy.setFileLogger(name="test",level="DEBUG")
infaHandler = infapy.connect(profile="DEV")

v3 = infaHandler.v3()
mappingTaskDetails = v3.lookup(path="infapy/mt_infapy_test",objectType="MTT")
print("Mapping Task Details: " + str(mappingTaskDetails))
mappingTaskID = mappingTaskDetails["objects"][0]["id"]
print("Mapping Task ID: " + str(mappingTaskID))

```

    Mapping Task Details: {'objects': [{'id': '1QcjcQ9hXwwcqW1P93354V', 'path': 'infapy/mt_infapy_test', 'type': 'MTT', 'description': '', 'updatedBy': 'prashanth-p', 'updateTime': '2021-09-26T08:41:04Z'}]}
    Mapping Task ID: 1QcjcQ9hXwwcqW1P93354V
    

## Function: startExport()

>        Used to export an object in IICS
>        This function initiates the export operation
>
>        Args:
>            name (String): Name of your export job
>            id (String): This is the object id which you want to export
>            use the lookup function or object function to get the object id
>
>            includeDependencies (bool, optional): If you want to include dependencies. Defaults to True.
>
>        Returns:
>            json: confirmation or failure response from export operation

### Example Code to start the export operation


```python
# name is just an identifier for your export operation
exportObj = v3.exportObject()
response = exportObj.startExport(name="MyTestJobFromPython",ObjectId="1QcjcQ9hXwwcqW1P93354V")
print(response)
exportID = response["id"]
print("Export Name: MyTestJobFromPython")
print("Export ID " + exportID)
```

    {'id': '9SczgYW6zyufJkDB6Uaduz', 'createTime': '2021-09-26T09:06:38.898Z', 'updateTime': '2021-09-26T09:06:38.898Z', 'name': 'MyTestJobFromPython', 'startTime': '2021-09-26T09:06:38.803Z', 'endTime': None, 'status': {'state': 'IN_PROGRESS', 'message': 'In Progress'}, 'objects': None}
    Export Name: MyTestJobFromPython
    Export ID 9SczgYW6zyufJkDB6Uaduz
    

## Function: getStatusOfExportByExportID()

>        use this method to get the status of the export
>        if it is a success or a failure
>
>        Args:
>            exportID (exportID): provide the export id you recieved
>            from startExport Method used before this
>
>        Returns:
>            json: Export operation status

### Example code to get the status of export


```python
# exportObj variable is defined above
# use the export id from the above code

response = exportObj.getStatusOfExportByExportID(exportID="9SczgYW6zyufJkDB6Uaduz")
print(response)
```

    {'id': '9SczgYW6zyufJkDB6Uaduz', 'createTime': '2021-09-26T09:06:39.000Z', 'updateTime': '2021-09-26T09:06:40.000Z', 'name': 'MyTestJobFromPython', 'startTime': '2021-09-26T09:06:39.000Z', 'endTime': '2021-09-26T09:06:40.000Z', 'status': {'state': 'SUCCESSFUL', 'message': 'Export completed successfully'}, 'objects': [{'id': '1QcjcQ9hXwwcqW1P93354V', 'name': 'mt_infapy_test', 'path': '/infapy', 'type': 'MTT', 'description': '', 'status': {'state': 'SUCCESSFUL', 'message': None}}, {'id': '3vVj4xdOpKsgAqwRSyhQM3', 'name': 'm_infapy_test', 'path': '/infapy', 'type': 'DTEMPLATE', 'description': '', 'status': {'state': 'SUCCESSFUL', 'message': None}}, {'id': '848Au1yuOzAcdxJMgPkdqy', 'name': '__ff', 'path': None, 'type': 'Connection', 'description': None, 'status': {'state': 'SUCCESSFUL', 'message': None}}, {'id': '95OeUg6sjYVhH6zxQUB76k', 'name': 'prashanth-sbx', 'path': None, 'type': 'AgentGroup', 'description': None, 'status': {'state': 'SUCCESSFUL', 'message': None}}, {'id': 'aeOwF2U4Uauf5fdiFwaLCz', 'name': 'infapy', 'path': '/', 'type': 'Project', 'description': '', 'status': {'state': 'SUCCESSFUL', 'message': None}}]}
    

## Function: getExportLogsByExportID()

>        use this method to get the export
>        logs
>
>        Args:
>            exportID (exportID): provide the export id you recieved
>            from startExport Method used before this
>
>        Returns:
>            string text: Export logs in text

### Example code to get exportLogsByExportID()


```python
# exportObj variable is defined above
# use the export id from the above code

response = exportObj.getExportLogsByExportID(exportID="9SczgYW6zyufJkDB6Uaduz")
print(response)
```

    > OIE_002 INFO 2021-09-26T09:06:39.017Z Starting export operation.
    Execution Client: API
    Job Name: MyTestJobFromPython
    Organization: GCS IICS
    RequestId: 9SczgYW6zyufJkDB6Uaduz
    User: prashanth-p
    > OIE_004 INFO 2021-09-26T09:06:39.139Z Successfully exported object [/Explore/infapy] of type [Project] id [aeOwF2U4Uauf5fdiFwaLCz]
    > OIE_004 INFO 2021-09-26T09:06:39.139Z Successfully exported object [/SYS/_SYSTEM_PROJECT] of type [Project] id [hrRCl2TfTa1jvmKBfGC4Il]
    > OIE_004 INFO 2021-09-26T09:06:39.237Z Successfully exported object [/SYS/_SYSTEM_FOLDER] of type [Folder] id [cfvpgEOpQmhlh1qOwkFkkc]
    > OIE_004 INFO 2021-09-26T09:06:39.463Z Successfully exported object [/SYS/prashanth-sbx] of type [AgentGroup] id [95OeUg6sjYVhH6zxQUB76k]
    > OIE_004 INFO 2021-09-26T09:06:39.592Z Successfully exported object [/SYS/__ff] of type [Connection] id [848Au1yuOzAcdxJMgPkdqy]
    > OIE_004 INFO 2021-09-26T09:06:39.721Z Successfully exported object [/Explore/infapy/m_infapy_test] of type [DTEMPLATE] id [3vVj4xdOpKsgAqwRSyhQM3]
    > OIE_004 INFO 2021-09-26T09:06:39.943Z Successfully exported object [/Explore/infapy/mt_infapy_test] of type [MTT] id [1QcjcQ9hXwwcqW1P93354V]
    > OIE_003 INFO 2021-09-26T09:06:39.943Z Finished export operation.
    Job Name: MyTestJobFromPython
    Start Time: 9/26/21 9:06 AM
    End Time: 9/26/21 9:06 AM
    Started by: prashanth-p
    Start Method: API
    Source Organization: GCS IICS
    Status: SUCCESSFUL
    
    

## Function: getExportZipFileByExportID()

This is the final step in the export operation. After the above export was successful. We now need to download the package to our local computer / server, so the package can then be imported to QA or higher environments.

>        Use this method to download the export object as a zip file
>        1. startExport()
>        2. getStatusOfExportByExportID()
>        3. getExportZipFileByExportID()
>        4. getExportLogsByExportID()
>
>        Args:
>            exportID (String): You recieve this id when you startExport()
>            filePath (String, optional): Path to download the object. Defaults to os.getcwd().
>            fileName (str, optional): exportObjectName.zip. Defaults to "infapyExportDownloaded.zip".
>
>        Returns:
>            zipfile: downloaded to filepath/filename


```python
# exportObj variable is defined above
# use the export id from the above code
# By default the zip file - "infapyExportDownloaded.zip" will get downloaded to your current working directory

response = exportObj.getExportZipFileByExportID(exportID="9SczgYW6zyufJkDB6Uaduz")
```
