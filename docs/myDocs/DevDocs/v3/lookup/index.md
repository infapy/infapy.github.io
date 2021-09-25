# Lookup

Use the lookup resource to look up an object's ID, name, path, or type attributes.
lookup api is used to fetch the object ID.

>        Args:
>            id ([str], required if path and object not provided): [description]. object id.
>            path ([str], required if id not provided): [description]. ProjectFolder/SubFolder/mt_test
>            objectType ([str], required if id not provided): [description]. Type of object, ex: MTT
>
>        Raises:
>            InvalidArgumentsError: if required arguments are not passed
>
>        Returns:
>            json: lookup of objects in iics v3.lookup()

For More Information on support values for object types, read the product documentation: https://docs.informatica.com/integration-cloud/cloud-platform/current-version/rest-api-reference/platform-rest-api-version-3-resources/lookup.html

## Example: Lookup Connection Details


```python
import infapy

# create infa handler
infaHandler = infapy.connect()
v3 = infaHandler.v3()

# Perform Lookup
# path = connectionName
lookup = v3.lookup(path="__ff",objectType="connection")
print(lookup)
```

    {'objects': [{'id': '848Au1yuOzAcdxJMgPkdqy', 'path': '__ff', 'type': 'Connection', 'description': None, 'updatedBy': 'prashanth-p', 'updateTime': '2021-08-12T14:40:54Z'}]}
    

## Example: Lookup Runtime Environment


```python
import infapy

# create infa handler
infaHandler = infapy.connect()
v3 = infaHandler.v3()

# Perform Lookup
# path = agentName
lookup = v3.lookup(path="prashanth-sbx",objectType="agent")
print(lookup)
```

    {'objects': [{'id': '6tSb1EPg2b4jbkpUuV2p6z', 'path': 'prashanth-sbx', 'type': 'AGENT', 'description': None, 'updatedBy': 'prashanth-p', 'updateTime': '2021-03-22T11:13:35Z'}]}
    

## Example: Lookup Mapping task id


```python
import infapy

# create infa handler
infaHandler = infapy.connect()
v3 = infaHandler.v3()

# Perform Lookup
# path = <projectFolder>/<subFolder>/<taskName>
lookup = v3.lookup(path="Prashanth/TEST/mt_scheduled_job_test",objectType="MTT")
print(lookup)
```

    {'objects': [{'id': 'kuBb7spW60ghLWgeRX6isa', 'path': 'Prashanth/TEST/mt_scheduled_job_test', 'type': 'MTT', 'description': '', 'updatedBy': 'prashanth-p', 'updateTime': '2021-03-30T12:31:04Z'}]}
    
