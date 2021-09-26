# Task

Use Task resource to request a list of tasks of a specified type. You can use this resource to retrieve the name and ID for a task.<br><br>
Do not use this resource to obtain a task ID to run a job. Instead, use the lookup resource. The lookup resource returns the federated task ID which is required to run a task that is not located in the Default folder.<br><br>
Do not use this resource for a file ingestion task. Instead, use the file ingestion job resource.

## Function: getTaskListByType()

getTaskListByType() returns list of tasks from IICS based on the task type specified.

>        Args:
>            type (string): Type of tasks.
>
>        Returns:
>            List of dict: <List of tasks in dict Format>
   
Valid Values for type argument:
* DMASK. Masking task.
* DRS. Replication task.
* DSS. Synchronization task.
* MTT. Mapping task.
* PCS. PowerCenter task.

### Example:


```python
import infapy

# create infa handler
infaHandler = infapy.connect(profile="spani")
v2=infaHandler.v2()

# Perform getTaskListByType()
TaskList=v2.taskList()
print(TaskList.getTaskListByType("DSS"))
```

    [{'@type': 'baseTask', 'id': '0119Y40I000000000002', 'orgId': '0119Y4', 'name': 'aaaaabbbbbcccccdddddeeeeefffffggggghhhhhiiiiijjjjjkkkkklllllmmmmmnnnnnooooopppppqqqqqrrrrrssssstttttuuuuuvvvvvwwwwwxxxxxyyyyyyzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzaaaaaaa', 'description': '', 'createTime': '2020-07-31T10:05:16.000Z', 'updateTime': '2020-07-31T10:08:35.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651'}, {'@type': 'baseTask', 'id': '0119Y40I000000000003', 'orgId': '0119Y4', 'name': 'sp-dss-rep1', 'description': '', 'createTime': '2020-09-21T08:39:12.000Z', 'updateTime': '2020-09-21T08:58:03.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651'}, {'@type': 'baseTask', 'id': '0119Y40I000000000004', 'orgId': '0119Y4', 'name': 'sp-dss-rep2', 'description': '', 'createTime': '2020-09-21T08:46:01.000Z', 'updateTime': '2020-09-21T09:15:13.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651'}, {'@type': 'baseTask', 'id': '0119Y40I000000000005', 'orgId': '0119Y4', 'name': 'Synchronization Task1', 'description': '', 'createTime': '2020-10-26T08:23:42.000Z', 'updateTime': '2020-10-26T08:24:05.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651'}]
    
