# Org

Use the Org Functions to get and update the details of Orgs and Sub-orgs

## Function: getOrgDetails()

getOrgDetails() returns the details of the IICS Organization currently logged into

>        Returns:
>            List of dict: <Organization Details in dict Format>

### Example


```python
import infapy

# create infa handler
infaHandler = infapy.connect(profile="jefjames")
v2=infaHandler.v2()

# Call getOrgDetails()
orgDetails = v2.org().getOrgDetails()
print(orgDetails)
```

    [{'@type': 'org', 'id': '000QML', 'orgId': '000QML', 'name': 'Infa NA2', 'description': '', 'createTime': '2018-05-07T13:30:29.000Z', 'updateTime': '2021-05-23T14:20:54.000Z', 'createdBy': 'OrgMigUser_1525714228777', 'updatedBy': 'infa_nishita', 'address1': '200 seaport', 'address2': '', 'address3': '', 'employees': '501_1000', 'city': 'redwood City', 'country': 'IN', 'state': 'CA', 'zipcode': '94063', 'successEmails': '', 'warningEmails': '', 'errorEmails': '', 'campaignCode': '1-627033281', 'spiUrl': 'https://paku.rt.informaticacloud.com/activevos', 'devOrg': False, 'timezone': 'IST', 'maxLogRows': 100, 'minPasswordLength': 4, 'minPasswordCharMix': 1, 'passwordReuseInDays': 0, 'passwordExpirationInDays': 0, 'subOrgLimit': 50, 'restApiSessionLimit': 500, 'parentOrgId': '52ZSTB0IDK6dXxaEQLUaQu', 'subOrgs': [{'@type': 'subOrg', 'id': '012BZ4', 'name': 'Cloud Intern 2021'}, {'@type': 'subOrg', 'id': '0106LX', 'name': 'Infa-IIDIQ-POD2-suborg-1'}], 'twoFactorAuthentication': False, 'orgUUID': '80bTjaasFejbEkQynNFnyT', 'ipAddressRanges': []}]
    

## Function: getSubOrgDetailsById()

getSubOrgDetailsById() returns the details of the Sub Organization with the Id passed to the function

>        Args:
>            subId (string): Sub Organization Id
>
>        Returns:
>            List of dict: <Sub Organization Details in dict Format>

### Example


```python
import infapy

# create infa handler
infaHandler = infapy.connect(profile="jefjames")
v2=infaHandler.v2()

# Call getSubOrgDetailsById()
subOrgId = orgDetails[0]["subOrgs"][0]["id"]
subOrgDetails = v2.org().getSubOrgDetailsById(subOrgId)
print(subOrgDetails)
```

    {'@type': 'org', 'id': '012BZ4', 'orgId': '012BZ4', 'name': 'Cloud Intern 2021', 'description': '', 'createTime': '2020-09-17T02:46:07.000Z', 'updateTime': '2020-09-17T02:46:07.000Z', 'createdBy': 'kkararia@informatica.com', 'updatedBy': 'kkararia@informatica.com', 'address1': '', 'address2': '', 'address3': '', 'employees': '0_10', 'city': '', 'country': 'US', 'state': '', 'zipcode': '', 'successEmails': '', 'warningEmails': '', 'errorEmails': '', 'spiUrl': 'https://paku.rt.informaticacloud.com/activevos', 'devOrg': False, 'timezone': 'America/Los_Angeles', 'maxLogRows': 100, 'minPasswordLength': 9, 'minPasswordCharMix': 3, 'passwordReuseInDays': 90, 'passwordExpirationInDays': 180, 'subOrgLimit': 0, 'restApiSessionLimit': 0, 'parentOrgId': '80bTjaasFejbEkQynNFnyT', 'subOrgs': [], 'twoFactorAuthentication': False, 'orgUUID': '2XMVRXUwIQmfd3zQWD9Xmd', 'ipAddressRanges': []}
    

## Function: getSubOrgDetailsByName()

getSubOrgDetailsByName() returns the details of the Sub Organization with the name passed to the function

>        Args:
>            subName (string): Sub Organization Name
>
>        Returns:
>            List of dict: <Sub Organization Details in dict Format>

### Example


```python
import infapy

#Create infa handler
infaHandler = infapy.connect(profile="jefjames")
v2=infaHandler.v2()

#Call getSubOrgDetailsByName()
subOrgName = orgDetails[0]["subOrgs"][0]["name"]
subOrgDetails= v2.org().getSubOrgDetailsByName(subOrgName)
print(subOrgDetails)
```

    {'@type': 'org', 'id': '012BZ4', 'orgId': '012BZ4', 'name': 'Cloud Intern 2021', 'description': '', 'createTime': '2020-09-17T02:46:07.000Z', 'updateTime': '2020-09-17T02:46:07.000Z', 'createdBy': 'kkararia@informatica.com', 'updatedBy': 'kkararia@informatica.com', 'address1': '', 'address2': '', 'address3': '', 'employees': '0_10', 'city': '', 'country': 'US', 'state': '', 'zipcode': '', 'successEmails': '', 'warningEmails': '', 'errorEmails': '', 'spiUrl': 'https://paku.rt.informaticacloud.com/activevos', 'devOrg': False, 'timezone': 'America/Los_Angeles', 'maxLogRows': 100, 'minPasswordLength': 9, 'minPasswordCharMix': 3, 'passwordReuseInDays': 90, 'passwordExpirationInDays': 180, 'subOrgLimit': 0, 'restApiSessionLimit': 0, 'parentOrgId': '80bTjaasFejbEkQynNFnyT', 'subOrgs': [], 'twoFactorAuthentication': False, 'orgUUID': '2XMVRXUwIQmfd3zQWD9Xmd', 'ipAddressRanges': []}
    
