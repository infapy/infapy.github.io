# User Groups

Use the userGroups resource along with the users and roles resources to manage user privileges for Informatica Intelligent Cloud Services tasks and assets. Users and groups can perform tasks and access assets based on the roles that you assign to them.


```python
import infapy

infapy.setFileLogger(name="test",level="DEBUG")
infaHandler = infapy.connect(profile="DEV")
v3 = infaHandler.v3()
userGroups = v3.userGroups()
```

## Function: getAllUserGroups()

>        Method for fetching all the user groups in IICS
>
>        Returns:
>            list of dict: List of all user groups in IICS

### Example for getAllUserGroups


```python
getAllUserGroups = userGroups.getAllUserGroups()
# Printing only the first 3 roles for example
for i in range(3):
    print(getAllUserGroups[i])
    print()
    
```

    {'id': '3T4BuFAenI7enCWZBCjRKn', 'orgId': 'fg1dzqDZ1K3lbHp8uq5vQB', 'createdBy': 'prashanth-p', 'updatedBy': 'prashanth-p', 'createTime': '2021-09-07T18:03:12.000Z', 'updateTime': '2021-09-07T18:03:12.000Z', 'userGroupName': '32f9e987-b422-42cf-bf00-dbd01243920b;32f9e987-b422-42cf-bf00-dbd01243920b;32f9e987-b422-42cf-bf00-dbd01243920b;32f9e987-b422-42cf-bf00-dbd01243920b32f9e987-b422-42cf-bf00-dbd01243920b', 'description': None, 'roles': [{'id': '5RZKlypdE5QiAIIAngXSS8', 'roleName': 'Business Manager', 'description': 'Role used for business managers', 'displayName': 'Application Integration Business Manager', 'displayDescription': 'Role used for business managers'}], 'users': []}
    
    {'id': '2yD1ZOHwo50beZglCQLcU1', 'orgId': 'fg1dzqDZ1K3lbHp8uq5vQB', 'createdBy': 'prashanth-p', 'updatedBy': 'prashanth-p', 'createTime': '2021-09-07T18:08:14.000Z', 'updateTime': '2021-09-07T18:08:14.000Z', 'userGroupName': '32f9e987-b422-42cf-bf00-dbd01243920b;32f9e987-b422-42cf-bf00-dbd01243920b;32f9e987-b422-42cf-bf00-dbd01243920b;32f9e987-b422-42cf-bf00-dbd01243920b32f9e987-b422-42cf-bf00-dbd01243920b;32f9e987-b422-42cf-bf00-dbd01243920b;', 'description': None, 'roles': [{'id': '5RZKlypdE5QiAIIAngXSS8', 'roleName': 'Business Manager', 'description': 'Role used for business managers', 'displayName': 'Application Integration Business Manager', 'displayDescription': 'Role used for business managers'}], 'users': []}
    
    {'id': 'huoQp9M4jaVgIwIIgI8Q81', 'orgId': 'fg1dzqDZ1K3lbHp8uq5vQB', 'createdBy': 'prashanth-p', 'updatedBy': 'prashanth-p', 'createTime': '2021-09-15T19:31:06.000Z', 'updateTime': '2021-09-15T19:31:06.000Z', 'userGroupName': '32f9e987-b422-42cf-bf00-dbd01243920b;32f9e987-b422-42cf-bf00-dbd01243920b;32f9e987-b422-42cf-bf00-dbd01243920b;32f9e987-b422-42cf-bf00-dbd01243920b32f9e987-b422-42cf-bf00-dbd01243920b;32f9e987-b422-42cf-bf00-dbd01243920b;32f9e987-b422-42cf-bf00-dbd', 'description': None, 'roles': [{'id': '5RZKlypdE5QiAIIAngXSS8', 'roleName': 'Business Manager', 'description': 'Role used for business managers', 'displayName': 'Application Integration Business Manager', 'displayDescription': 'Role used for business managers'}], 'users': []}
    
    

## Function: createNewUserGroup()

>        You can use this method to create a new user group
>
>        Args:
>            userGroupJson (dict): please read the documentation
>
>        Raises:
>            InvalidArgumentsError: if invalid args are passed
>
>        Returns:
>            dict: user group created response


```python
# v3 = infaHandler.v2()
user = v3.users()
userDetails = user.getAllUsers()
for eachUser in userDetails:
    if eachUser["userName"] in ["prashanth-p","reshma-r"]:
        print("User ID of User " + eachUser["userName"] + ": " + eachUser["id"])

adminRole = v3.userRoles().getUserRoleByName(userRoleName="admin")
print("Role ID of Admin Role: " + adminRole[0]["id"])


groupJsonBody = {
    "name" : "user_group_1",
    "roles" : ["9gedBDoYQoQibNMohf5KCh"],
    "users" : ["42szaouMf0bg0yycPME0Up","0Kk2nHoX9eUgdzgu9HRYCS"]
}

newGroup = userGroups.createNewUserGroup(userGroupJson=groupJsonBody)
print(newGroup)
```

    User ID of User prashanth-p: 42szaouMf0bg0yycPME0Up
    User ID of User reshma-r: 0Kk2nHoX9eUgdzgu9HRYCS
    Role ID of Admin Role: 9gedBDoYQoQibNMohf5KCh
    {'id': '93jD796cGQNcB8ZEbfwdO9', 'orgId': 'fg1dzqDZ1K3lbHp8uq5vQB', 'createdBy': 'prashanth-p', 'updatedBy': 'prashanth-p', 'createTime': '2021-09-26T13:22:02.171Z', 'updateTime': '2021-09-26T13:22:02.180Z', 'userGroupName': 'user_group_1', 'description': None, 'roles': [{'id': '9gedBDoYQoQibNMohf5KCh', 'roleName': 'Admin', 'description': 'Role for performing administrative tasks for an organization. Has full access to all licensed services.', 'displayName': 'Admin', 'displayDescription': 'Role for performing administrative tasks for an organization. Has full access to all licensed services.'}], 'users': [{'id': '0Kk2nHoX9eUgdzgu9HRYCS', 'userName': 'reshma-r', 'description': ''}, {'id': '42szaouMf0bg0yycPME0Up', 'userName': 'prashanth-p', 'description': ''}]}
    

## Function: getUserGroupByName

>        Method for fetching the user group details
>        by name in IICS
>
>        Args:
>            userGroupName (string): name of the usergroup
>
>        Returns:
>            dict: userGroup Details


```python
response = userGroups.getUserGroupByName(userGroupName="user_group_1")
print(response)

```

    [{'id': '93jD796cGQNcB8ZEbfwdO9', 'orgId': 'fg1dzqDZ1K3lbHp8uq5vQB', 'createdBy': 'prashanth-p', 'updatedBy': 'prashanth-p', 'createTime': '2021-09-26T13:22:02.000Z', 'updateTime': '2021-09-26T13:22:02.000Z', 'userGroupName': 'user_group_1', 'description': None, 'roles': [{'id': '9gedBDoYQoQibNMohf5KCh', 'roleName': 'Admin', 'description': 'Role for performing administrative tasks for an organization. Has full access to all licensed services.', 'displayName': 'Admin', 'displayDescription': 'Role for performing administrative tasks for an organization. Has full access to all licensed services.'}], 'users': [{'id': '0Kk2nHoX9eUgdzgu9HRYCS', 'userName': 'reshma-r', 'description': ''}, {'id': '42szaouMf0bg0yycPME0Up', 'userName': 'prashanth-p', 'description': ''}]}]
    

## Function: deleteUserrole()

>        The function deletes the user role in informatica cloud
>
>        Args:
>            userRoleID (string): User role ID


```python
# You can get the role id from the get commands as in above example
response = userGroups.deleteUserGroup(userGroupID="93jD796cGQNcB8ZEbfwdO9")
print(response)
```

    <Response [204]>
    
