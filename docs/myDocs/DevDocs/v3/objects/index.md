# Objects

Use the objects resource to get a list of an organization's assets. You might use this resource to find assets to export.


```python
import infapy
infapy.setFileLogger(name="test",level="DEBUG")
infaHandler = infapy.connect(profile="QA")

v3 = infaHandler.v3()
obj = v3.objects()
```

## Function: getObjectID()

>        get the object IDs of objects in IICS
>
>        Args:
>            q ([type], optional): [description]. Defaults to None.
>            limit (int, optional): [description]. Defaults to 200.
>            skip ([type], optional): [description]. Defaults to None.
>       
>       To build the query, read the docs:
>           https://docs.informatica.com/integration-cloud/cloud-platform/current-version/rest-api-reference/platform-rest-api-version-3-resources/objects/finding-assets.html


```python
queryString="type=='MTT'"
myObjects = obj.getObjectID(q=queryString)
print(myObjects)
```

    {'count': 1, 'objects': [{'id': '4JzMQBmn5YWbX1CCECivWK', 'path': 'infapy/mt_infapy_test', 'type': 'MTT', 'description': '', 'updatedBy': 'prash1234', 'updateTime': '2021-09-26T11:09:48Z', 'tags': [], 'sourceControl': None, 'customAttributes': None}]}
    

## Function: getObjectDependency()

>        Get object dependency of objects in IICS
>
>        Args:
>            objectID (str): string object id
>            refType (str, optional): uses or usedBy. Defaults to "uses".
>            limit (int, optional): Max 50. Defaults to 50.
>            skip ([type], optional): Number of elements to skip from the beginning. Defaults to 0.
>
>        Returns:
>            list of dict: dependency list in json


```python
myObjectsDependencies = obj.getObjectDependency(objectID="4JzMQBmn5YWbX1CCECivWK")
print(myObjectsDependencies)
```

    {'count': 3, '@id': '4JzMQBmn5YWbX1CCECivWK', 'references': [{'id': '9YGTW8zLVaAb6O15bcjbyk', 'appContextId': '01AU220B000000000002', 'path': 'FF', 'documentType': 'SAAS_CONNECTION', 'description': None, 'lastUpdatedTime': '2021-09-25T07:12:53Z'}, {'id': 'lI0qCBPFUyKfSYNPSZNLMT', 'appContextId': '01AU2217000000000005', 'path': 'infapy/m_infapy_test', 'documentType': 'MAPPING', 'description': '', 'lastUpdatedTime': '2021-09-26T11:09:47Z'}, {'id': 'iwvniZZPdG6cltC3Uzcf2i', 'appContextId': '01AU2225000000000002', 'path': 'prashanth-redhat-sbx', 'documentType': 'SAAS_RUNTIME_ENVIRONMENT', 'description': None, 'lastUpdatedTime': '2021-09-25T07:03:24Z'}]}
    
