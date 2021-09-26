# Users

Use this resource to request Informatica Intelligent Cloud Services user details, create users, and delete users. 


```python
import infapy
infapy.setFileLogger(name="test",level="DEBUG")
infaHandler = infapy.connect(profile="DEV")

v3 = infaHandler.v3()
users = v3.users()
```

## Function: getAllUsers()

>        getAllUsers can be used to fetch all the user details in you iics org
>
>        Returns:
>            infaUserData: <list of dict>


```python
allusers = users.getAllUsers()
# printing only 1 user for example
print(allusers[4])
```

    {'id': '0Kk2nHoX9eUgdzgu9HRYCS', 'orgId': 'fg1dzqDZ1K3lbHp8uq5vQB', 'createdBy': 'prashanth-p', 'updatedBy': 'prashanth-p', 'createTime': '2021-08-05T13:13:09.000Z', 'updateTime': '2021-08-05T13:13:09.000Z', 'userName': 'reshma-r', 'firstName': 'Reshma', 'lastName': 'Tangdu', 'description': '', 'title': 'Software Engineer', 'phone': '1234567890', 'email': 'xyz@informatica.com', 'state': 'Provisioned', 'timeZoneId': 'America/Los_Angeles', 'maxLoginAttempts': '10', 'authentication': 'Native', 'forcePasswordChange': False, 'lastLoginTime': None, 'lastLoginMode': 'None', 'roles': [{'id': 'aKOABsXIRP6eI0aEE32bg8', 'roleName': 'Data Preview', 'description': 'Role to preview data', 'displayName': 'Data Integration Data Previewer', 'displayDescription': 'Role to preview data'}, {'id': 'lObMwXOTigHi5XBJTU1Z8Q', 'roleName': 'Deployer', 'description': 'Role used by deployer', 'displayName': 'Deployer', 'displayDescription': 'Role used by deployer'}, {'id': '9dKyXtuAcJIdKsKZGohq49', 'roleName': 'Data Integration Task Executor', 'description': 'Role to run Data Integration tasks', 'displayName': 'Data Integration Task Executor', 'displayDescription': 'Role to run Data Integration tasks'}, {'id': '9aTuLGRQgHyjpftpLFj7Qg', 'roleName': 'Designer', 'description': 'Role for creating assets, tasks, and processes. Can configure connections, schedules, and runtime environments. Has access to the Application Integration Console.', 'displayName': 'Designer', 'displayDescription': 'Role for creating assets, tasks, and processes. Can configure connections, schedules, and runtime environments. Has access to the Application Integration Console.'}, {'id': '9gedBDoYQoQibNMohf5KCh', 'roleName': 'Admin', 'description': 'Role for performing administrative tasks for an organization. Has full access to all licensed services.', 'displayName': 'Admin', 'displayDescription': 'Role for performing administrative tasks for an organization. Has full access to all licensed services.'}], 'groups': []}
    

## Function: getUserByID()

>        We can use this method to get the user details of a particular user
>
>        Args:
>            id (string): you can use the user id to get the details
>
>        Returns:
>            json: infaUserDetails


```python
myUser = users.getUserByID(id="0Kk2nHoX9eUgdzgu9HRYCS")
print(myUser)
```

    [{'id': '0Kk2nHoX9eUgdzgu9HRYCS', 'orgId': 'fg1dzqDZ1K3lbHp8uq5vQB', 'createdBy': 'prashanth-p', 'updatedBy': 'prashanth-p', 'createTime': '2021-08-05T13:13:09.000Z', 'updateTime': '2021-08-05T13:13:09.000Z', 'userName': 'reshma-r', 'firstName': 'Reshma', 'lastName': 'Tangdu', 'description': '', 'title': 'Software Engineer', 'phone': '1234567890', 'email': 'xyz@informatica.com', 'state': 'Provisioned', 'timeZoneId': 'America/Los_Angeles', 'maxLoginAttempts': '10', 'authentication': 'Native', 'forcePasswordChange': False, 'lastLoginTime': None, 'lastLoginMode': 'None', 'roles': [{'id': 'aKOABsXIRP6eI0aEE32bg8', 'roleName': 'Data Preview', 'description': 'Role to preview data', 'displayName': 'Data Integration Data Previewer', 'displayDescription': 'Role to preview data'}, {'id': 'lObMwXOTigHi5XBJTU1Z8Q', 'roleName': 'Deployer', 'description': 'Role used by deployer', 'displayName': 'Deployer', 'displayDescription': 'Role used by deployer'}, {'id': '9dKyXtuAcJIdKsKZGohq49', 'roleName': 'Data Integration Task Executor', 'description': 'Role to run Data Integration tasks', 'displayName': 'Data Integration Task Executor', 'displayDescription': 'Role to run Data Integration tasks'}, {'id': '9aTuLGRQgHyjpftpLFj7Qg', 'roleName': 'Designer', 'description': 'Role for creating assets, tasks, and processes. Can configure connections, schedules, and runtime environments. Has access to the Application Integration Console.', 'displayName': 'Designer', 'displayDescription': 'Role for creating assets, tasks, and processes. Can configure connections, schedules, and runtime environments. Has access to the Application Integration Console.'}, {'id': '9gedBDoYQoQibNMohf5KCh', 'roleName': 'Admin', 'description': 'Role for performing administrative tasks for an organization. Has full access to all licensed services.', 'displayName': 'Admin', 'displayDescription': 'Role for performing administrative tasks for an organization. Has full access to all licensed services.'}], 'groups': []}]
    

## Function: createNewUser()

>        create a new user by passing the user profile as a dict
>
>        Args:
>            userProfileInJson (dict): user profile in json
>
>        Raises:
>            InvalidUserDetailsProvided: if invalid json is provided
>
>        Returns:
>            json: confirmation of user created


```python
roles = v3.userRoles().getUserRoleByName(userRoleName="Admin")
devRoles = v3.userRoles().getUserRoleByName(userRoleName="Designer")
groups = v3.userGroups().getUserGroupByName(userGroupName="user_group_1")
print(roles[0]["id"])
print(devRoles[0]["id"])
print(groups[0]["id"])
```

    9gedBDoYQoQibNMohf5KCh
    9aTuLGRQgHyjpftpLFj7Qg
    04QPIavnjLOjUuXBaWX6aE
    


```python
userProfile = {
    "name" : "pprad1234",
    "firstName" : "Prashanth",
    "lastName" : "Pradeep",
    "email" : "pasds@informatica.com",
    "authentication" : 0,
    "roles" : ["9gedBDoYQoQibNMohf5KCh", "9aTuLGRQgHyjpftpLFj7Qg"],
    "groups" : ["04QPIavnjLOjUuXBaWX6aE"]
}

response = users.createNewUser(userProfileInJson=userProfile)
print(response)
```

    {'id': '27WKlN7CiCYhYPGwiBTeMJ', 'orgId': 'fg1dzqDZ1K3lbHp8uq5vQB', 'createdBy': 'prashanth-p', 'updatedBy': 'prashanth-p', 'createTime': '2021-09-26T14:14:18.424Z', 'updateTime': '2021-09-26T14:14:18.471Z', 'userName': 'pprad1234', 'firstName': 'Prashanth', 'lastName': 'Pradeep', 'description': None, 'title': None, 'phone': None, 'email': 'xyz@informatica.com', 'state': 'Provisioned', 'timeZoneId': 'America/Los_Angeles', 'maxLoginAttempts': '10', 'authentication': 'Native', 'forcePasswordChange': False, 'lastLoginTime': None, 'lastLoginMode': 'None', 'roles': [{'id': '9aTuLGRQgHyjpftpLFj7Qg', 'roleName': 'Designer', 'description': 'Role for creating assets, tasks, and processes. Can configure connections, schedules, and runtime environments. Has access to the Application Integration Console.', 'displayName': 'Designer', 'displayDescription': 'Role for creating assets, tasks, and processes. Can configure connections, schedules, and runtime environments. Has access to the Application Integration Console.'}, {'id': '9gedBDoYQoQibNMohf5KCh', 'roleName': 'Admin', 'description': 'Role for performing administrative tasks for an organization. Has full access to all licensed services.', 'displayName': 'Admin', 'displayDescription': 'Role for performing administrative tasks for an organization. Has full access to all licensed services.'}], 'groups': [{'id': '04QPIavnjLOjUuXBaWX6aE', 'userGroupName': 'user_group_1', 'description': None}]}
    

## Function: deleteUser()


```python
response = users.deleteUser(userID="27WKlN7CiCYhYPGwiBTeMJ")
```
