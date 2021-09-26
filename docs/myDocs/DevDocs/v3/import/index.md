# Import

Use this resource with the export resource to migrate objects from one organization to another.

# Prerequisite - Need to get the source and target object ids

When we are performing an import operation, we need to map the source connection with the target connection, similartly map the source runtime environment with the target runtime env. As a first step, we need to get the object ids of the source dependant objects and the target dependant objects.


```python
# First fetching source depenant object ids
import infapy

infapy.setFileLogger(name="DEV Logger",level="DEBUG")
devInfaHandler = infapy.connect(profile="DEV")
v3 = devInfaHandler.v3()

# Get the connection object id
lookupObj = v3.lookup(path="__ff",objectType="connection")
print(lookupObj)
srcConnectionID = lookupObj["objects"][0]["id"]
print("srcConnection ID: " + srcConnectionID)

# Get the agent group object details
lookupObj = v3.lookup(path="prashanth-sbx",objectType="agentgroup")
print(lookupObj)
srcRuntimeID = lookupObj["objects"][0]["id"]
print("srcRuntime ID: " + srcRuntimeID)

```

    {'objects': [{'id': '848Au1yuOzAcdxJMgPkdqy', 'path': '__ff', 'type': 'Connection', 'description': None, 'updatedBy': 'prashanth-p', 'updateTime': '2021-08-12T14:40:54Z'}]}
    srcConnection ID: 848Au1yuOzAcdxJMgPkdqy
    {'objects': [{'id': '95OeUg6sjYVhH6zxQUB76k', 'path': 'prashanth-sbx', 'type': 'AgentGroup', 'description': None, 'updatedBy': 'prashanth-p', 'updateTime': '2021-02-15T07:50:30Z'}]}
    srcRuntime ID: 95OeUg6sjYVhH6zxQUB76k
    


```python
# First fetching target depenant object ids
import infapy

infapy.setFileLogger(name="QA Logger",level="DEBUG")
qaInfaHandler = infapy.connect(profile="QA")
v3 = qaInfaHandler.v3()

# Get the connection object id
lookupObj = v3.lookup(path="FF",objectType="connection")
print(lookupObj)
tgtConnectionID = lookupObj["objects"][0]["id"]
print("tgtConnection ID: " + tgtConnectionID)

# Get the agent group object details
lookupObj = v3.lookup(path="prashanth-redhat-sbx",objectType="agentgroup")
print(lookupObj)
tgtRuntimeID = lookupObj["objects"][0]["id"]
print("tgtRuntime ID: " + tgtRuntimeID)
```

    {'objects': [{'id': '9YGTW8zLVaAb6O15bcjbyk', 'path': 'FF', 'type': 'Connection', 'description': None, 'updatedBy': 'prash1234', 'updateTime': '2021-09-25T07:12:53Z'}]}
    tgtConnection ID: 9YGTW8zLVaAb6O15bcjbyk
    {'objects': [{'id': 'iwvniZZPdG6cltC3Uzcf2i', 'path': 'prashanth-redhat-sbx', 'type': 'AgentGroup', 'description': None, 'updatedBy': 'prash1234', 'updateTime': '2021-09-25T07:03:24Z'}]}
    tgtRuntime ID: iwvniZZPdG6cltC3Uzcf2i
    

## Function: uploadZipToGetJobID()

>        Use this function to import the zip file to fetch the job id
>        This function initiates the process 
>
>        Args:
>            filePath (str, optional): Defaults to os.getcwd().
>            fileName (str, optional): Defaults to "infapyExportDownloaded.zip".
>
>        Raises:
>            InvalidArgumentsError: if invalid arguments are provided
>
>        Returns:
>            json: response after the upload zip has been initiated


```python
v3 = qaInfaHandler.v3()
importObj = v3.importObject()

response = importObj.uploadZipToGetJobID()
print(response)
print()

importJobID = response["jobId"]
print("Import Job ID: " + importJobID)
```

    {'jobId': '8bSlx81r2GSlX417G9XNsq', 'jobStatus': {'state': 'NOT_STARTED', 'message': None}, 'checksumValid': True}
    
    Import Job ID: 8bSlx81r2GSlX417G9XNsq
    

## Function: startImportByJobID()

>        This function initiates the job once the
>        zip is uploaded
>
>        Args:
>            jobID (str): From response of uploadZipToGetJobID
>            importBody (dict): Read the docs for understanding the import body
>
>        Raises:
>            InvalidArgumentsError: if invalid body sent
>
>        Returns:
>            json: import job success response


```python
jsonObject = {
    "name" : "ImportNameFromScript",
    "importSpecification" : {
        "defaultConflictResolution" : "OVERWRITE",
        "objectSpecification" : [
        {
            "sourceObjectId" : "848Au1yuOzAcdxJMgPkdqy",
            "targetObjectId" : "9YGTW8zLVaAb6O15bcjbyk"
        },
        {
            "sourceObjectId" : "95OeUg6sjYVhH6zxQUB76k",
            "targetObjectId" : "iwvniZZPdG6cltC3Uzcf2i"
        }]
    }
}

# using importObj created above
response = importObj.startImportByJobID(jobID="8bSlx81r2GSlX417G9XNsq",importBody=jsonObject)
print(response)
```

    {'id': '8bSlx81r2GSlX417G9XNsq', 'createTime': '2021-09-26T11:08:30.000Z', 'updateTime': '2021-09-26T11:09:46.183Z', 'name': 'ImportNameFromScript', 'startTime': '2021-09-26T11:09:46.079Z', 'endTime': None, 'status': {'state': 'IN_PROGRESS', 'message': 'In Progress'}, 'objects': None, 'sourceOrgId': 'fg1dzqDZ1K3lbHp8uq5vQB', 'checksumValid': True}
    

## Function: getStatusOfImportByImportID()

>        use this method to get the status of the import
>        if it is a success or a failure
>
>        Args:
>            importID (importID): provide the import id you recieved
>            from uploadZipToGetJobID Method used before this
>
>        Returns:
>            json: import operation status


```python
response = importObj.getStatusOfImportByImportID(importID="8bSlx81r2GSlX417G9XNsq")
print(response)
```

    {'id': '8bSlx81r2GSlX417G9XNsq', 'createTime': '2021-09-26T11:08:30.000Z', 'updateTime': '2021-09-26T11:09:49.000Z', 'name': 'ImportNameFromScript', 'startTime': '2021-09-26T11:09:46.000Z', 'endTime': '2021-09-26T11:09:49.000Z', 'status': {'state': 'SUCCESSFUL', 'message': 'Import completed successfully'}, 'objects': [{'sourceObject': {'id': '1QcjcQ9hXwwcqW1P93354V', 'name': 'mt_infapy_test', 'path': '/infapy', 'type': 'MTT', 'description': ''}, 'targetObject': {'id': None, 'name': 'mt_infapy_test', 'path': '/infapy', 'type': 'MTT', 'description': None, 'status': None}, 'status': {'state': 'SUCCESSFUL', 'message': 'Create object'}}, {'sourceObject': {'id': '3vVj4xdOpKsgAqwRSyhQM3', 'name': 'm_infapy_test', 'path': '/infapy', 'type': 'DTEMPLATE', 'description': ''}, 'targetObject': {'id': None, 'name': 'm_infapy_test', 'path': '/infapy', 'type': 'DTEMPLATE', 'description': None, 'status': None}, 'status': {'state': 'SUCCESSFUL', 'message': 'Create object'}}, {'sourceObject': {'id': '848Au1yuOzAcdxJMgPkdqy', 'name': '__ff', 'path': None, 'type': 'Connection', 'description': None}, 'targetObject': {'id': None, 'name': 'FF', 'path': None, 'type': 'Connection', 'description': None, 'status': None}, 'status': {'state': 'SUCCESSFUL', 'message': 'Reuse existing object'}}, {'sourceObject': {'id': '95OeUg6sjYVhH6zxQUB76k', 'name': 'prashanth-sbx', 'path': None, 'type': 'AgentGroup', 'description': None}, 'targetObject': {'id': None, 'name': 'prashanth-redhat-sbx', 'path': None, 'type': 'AgentGroup', 'description': None, 'status': None}, 'status': {'state': 'SUCCESSFUL', 'message': 'Reuse existing object'}}, {'sourceObject': {'id': 'aeOwF2U4Uauf5fdiFwaLCz', 'name': 'infapy', 'path': '/', 'type': 'Project', 'description': ''}, 'targetObject': {'id': None, 'name': 'infapy', 'path': '/', 'type': 'Project', 'description': None, 'status': None}, 'status': {'state': 'SUCCESSFUL', 'message': 'Create object'}}], 'sourceOrgId': 'fg1dzqDZ1K3lbHp8uq5vQB', 'checksumValid': True}
    

## Function: getImportLogsByImportID()

>        use this method to get the import
>        logs
>
>        Args:
>            importID (importID): provide the import id you recieved
>            from uploadZipToGetJobID Method used before this
>
>        Returns:
>            string text: import logs in text


```python
response = importObj.getImportLogsByImportID(importID="8bSlx81r2GSlX417G9XNsq")
print(response)
```

    > OIE_002 INFO 2021-09-26T11:09:46.194Z Starting import operation.
    Execution Client: API
    Job Name: ImportNameFromScript
    Organization: Informatica
    RequestId: 8bSlx81r2GSlX417G9XNsq
    User: prash1234
    > OIE_006 INFO 2021-09-26T11:09:46.499Z Successfully imported object [/Explore/infapy] of type [Project] id [aeOwF2U4Uauf5fdiFwaLCz] to [/Explore/infapy]
    > OIE_006 INFO 2021-09-26T11:09:47.473Z Successfully imported object [/Explore/infapy/m_infapy_test] of type [DTEMPLATE] id [3vVj4xdOpKsgAqwRSyhQM3] to [/Explore/infapy/m_infapy_test]
    > OIE_006 INFO 2021-09-26T11:09:48.569Z Successfully imported object [/Explore/infapy/mt_infapy_test] of type [MTT] id [1QcjcQ9hXwwcqW1P93354V] to [/Explore/infapy/mt_infapy_test]
    > OIE_003 INFO 2021-09-26T11:09:48.569Z Finished import operation.
    Job Name: ImportNameFromScript
    Start Time: 9/26/21 11:09 AM
    End Time: 9/26/21 11:09 AM
    Started by: prash1234
    Start Method: API
    Source Organization: GCS IICS
    Status: SUCCESSFUL
    
    
