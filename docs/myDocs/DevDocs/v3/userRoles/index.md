# User Roles

Use this resource to get the details for roles in your organization. You can also use this resource to create and delete custom roles.


```python
import infapy

infapy.setFileLogger(name="test",level="DEBUG")
infaHandler = infapy.connect(profile="DEV")
v3 = infaHandler.v3()
userRoles = v3.userRoles()
```

## Function: getAllUserRoles()

>        Method for fetching all the user roles in IICS
>
>        Returns:
>            list of dict: List of all user roles in IICS

### Example for getAllUserRoles


```python
getAllUserRoles = userRoles.getAllUserRoles()
# Printing only the first 3 roles for example
for i in range(3):
    print(getAllUserRoles[i])
    print()
    
```

    {'id': '9gedBDoYQoQibNMohf5KCh', 'orgId': '52ZSTB0IDK6dXxaEQLUaQu', 'createdBy': 'System built-in user', 'updatedBy': 'ops-post-deploy-user', 'createTime': '2017-12-05T21:02:36.000Z', 'updateTime': '2021-09-15T04:42:29.000Z', 'roleName': 'Admin', 'description': 'Role for performing administrative tasks for an organization. Has full access to all licensed services.', 'displayName': 'Admin', 'displayDescription': 'Role for performing administrative tasks for an organization. Has full access to all licensed services.', 'systemRole': True, 'status': 'Enabled'}
    
    {'id': '5RZKlypdE5QiAIIAngXSS8', 'orgId': '52ZSTB0IDK6dXxaEQLUaQu', 'createdBy': 'ops-post-deploy-user', 'updatedBy': 'ops-post-deploy-user', 'createTime': '2018-02-11T04:16:57.000Z', 'updateTime': '2018-10-13T15:00:28.000Z', 'roleName': 'Business Manager', 'description': 'Role used for business managers', 'displayName': 'Application Integration Business Manager', 'displayDescription': 'Role used for business managers', 'systemRole': True, 'status': 'Enabled'}
    
    {'id': '8hQVJFGyyQkep1g2AeEewB', 'orgId': '52ZSTB0IDK6dXxaEQLUaQu', 'createdBy': 'ops-post-deploy-user', 'updatedBy': 'ops-post-deploy-user', 'createTime': '2018-02-11T04:16:57.000Z', 'updateTime': '2018-10-13T15:00:28.000Z', 'roleName': 'Data Viewer', 'description': 'Role used for granting access for data', 'displayName': 'Application Integration Data Viewer', 'displayDescription': 'Role used for granting access for data', 'systemRole': True, 'status': 'Enabled'}
    
    

## Function: createNewUserRole()

>        You can use this method to create a new user role
>
>        Args:
>            userRoleJson (dict): please read the documentation
>
>        Raises:
>            InvalidArgumentsError: if invalid args are passed
>
>        Returns:
>            dict: user role created response


```python
response = userRoles.createNewUserRole(name="myTestRole",description="my test roles",privileges=["9Yz7DzpQAKThluCEpbUqmX"])
print(response)
```

    {'id': '3FPb258AcWZkDxO6v25dGx', 'orgId': 'fg1dzqDZ1K3lbHp8uq5vQB', 'createdBy': 'prashanth-p', 'updatedBy': 'prashanth-p', 'createTime': '2021-09-26T12:25:20.394Z', 'updateTime': '2021-09-26T12:25:20.400Z', 'roleName': 'myTestRole', 'description': 'my test roles', 'displayName': 'myTestRole', 'displayDescription': 'my test roles', 'systemRole': False, 'status': 'Enabled'}
    

## Function: getUserRoleByName

>        Method for fetching the user role details
>        by name in IICS
>
>        Args:
>            userRoleName (string): name of the userrole
>
>        Returns:
>            dict: userrole Details


```python
response = v3.userRoles().getUserRoleByName(userRoleName="myTestRole")
print(response)

```

    [{'id': '3FPb258AcWZkDxO6v25dGx', 'orgId': 'fg1dzqDZ1K3lbHp8uq5vQB', 'createdBy': 'prashanth-p', 'updatedBy': 'prashanth-p', 'createTime': '2021-09-26T12:25:20.000Z', 'updateTime': '2021-09-26T12:25:20.000Z', 'roleName': 'myTestRole', 'description': 'my test roles', 'displayName': 'myTestRole', 'displayDescription': 'my test roles', 'systemRole': False, 'status': 'Enabled', 'privileges': [{'id': '9Yz7DzpQAKThluCEpbUqmX', 'name': 'create.datawiz.task', 'description': None, 'service': 'DI', 'status': 'Enabled'}]}]
    

## Function: deleteUserrole()

>        The function deletes the user role in informatica cloud
>
>        Args:
>            userRoleID (string): User role ID


```python
# You can get the role id from the get commands as in above example
response = v3.userRoles().deleteUserrole(userRoleID="3FPb258AcWZkDxO6v25dGx")
print(response)
```

    <Response [204]>
    
