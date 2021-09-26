# MTTask

Use MTTask resource to request the details of a mapping task. You can also create, update, or delete a mapping task.

## Function: getAllMTTasks()

getAllMTTasks() returns details for all Mapping tasks in the Org.

>        Returns:
>            List of dict: <Mapping Task Details in dict Format>
   

### Example:


```python
import infapy

# create infa handler
infaHandler = infapy.connect(profile="spani")
v2=infaHandler.v2()

# Perform getAllMTTasks()
MTTask=v2.mttask()
print(MTTask.getAllMTTasks())
```

    [{'@type': 'mtTask', 'id': '0119Y40Z000000000002', 'orgId': '0119Y4', 'name': 'aaaa', 'description': '', 'createTime': '2020-07-31T09:32:23.000Z', 'updateTime': '2020-08-03T13:20:53.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000002L', 'orgId': '0119Y4', 'name': 'ER-6941', 'description': '', 'createTime': '2021-09-23T10:47:49.000Z', 'updateTime': '2021-09-23T11:27:45.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000001W', 'orgId': '0119Y4', 'name': 'MappingTask1', 'description': '', 'createTime': '2021-08-26T11:45:45.000Z', 'updateTime': '2021-08-26T11:45:45.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000002J', 'orgId': '0119Y4', 'name': 'MappingTask2', 'description': '', 'createTime': '2021-09-23T06:26:37.000Z', 'updateTime': '2021-09-23T06:45:50.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000000J', 'orgId': '0119Y4', 'name': 'MappingTask3', 'description': '', 'createTime': '2020-11-02T08:12:16.000Z', 'updateTime': '2020-11-02T08:22:01.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000000K', 'orgId': '0119Y4', 'name': 'MappingTask4', 'description': '', 'createTime': '2020-11-02T08:22:38.000Z', 'updateTime': '2020-11-02T08:42:55.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000000M', 'orgId': '0119Y4', 'name': 'MappingTask5', 'description': '', 'createTime': '2020-11-09T15:30:52.000Z', 'updateTime': '2020-11-09T15:30:52.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000000R', 'orgId': '0119Y4', 'name': 'MappingTask6', 'description': '', 'createTime': '2020-12-04T06:16:08.000Z', 'updateTime': '2020-12-08T10:34:37.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000002K', 'orgId': '0119Y4', 'name': 'MappingTask7', 'description': '', 'createTime': '2021-09-23T06:27:56.000Z', 'updateTime': '2021-09-23T06:47:39.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000000G', 'orgId': '0119Y4', 'name': 'MappingTaskBuilder', 'description': '', 'createTime': '2020-11-02T05:05:41.000Z', 'updateTime': '2020-11-02T06:38:08.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000002B', 'orgId': '0119Y4', 'name': 'MC_RUNSTATUS_123', 'description': '', 'createTime': '2021-09-17T01:41:01.000Z', 'updateTime': '2021-09-21T02:22:00.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z000000000025', 'orgId': '0119Y4', 'name': 'MC_UC4_IHUB_IOSD_JOB_RUN_STATUS_UPD', 'description': '', 'createTime': '2021-09-16T10:30:24.000Z', 'updateTime': '2021-09-21T00:36:56.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z000000000011', 'orgId': '0119Y4', 'name': 'mct_Parametrized_task', 'description': '', 'createTime': '2021-01-06T07:26:03.000Z', 'updateTime': '2021-08-09T05:33:22.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000001B', 'orgId': '0119Y4', 'name': 'MT IU', 'description': '', 'createTime': '2021-03-11T07:06:35.000Z', 'updateTime': '2021-09-24T06:45:30.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z000000000017', 'orgId': '0119Y4', 'name': 'mt_completeness_parm', 'description': '', 'createTime': '2021-02-22T09:38:03.000Z', 'updateTime': '2021-02-22T09:38:03.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000001I', 'orgId': '0119Y4', 'name': 'mt_QSR_iHUB_AsignaFecha_UnlockingKeyring', 'description': '', 'createTime': '2021-04-05T07:53:03.000Z', 'updateTime': '2021-04-05T07:53:03.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000001D', 'orgId': '0119Y4', 'name': 'MT_SAP_EM', 'description': '', 'createTime': '2021-03-17T09:10:21.000Z', 'updateTime': '2021-03-17T12:08:52.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z000000000018', 'orgId': '0119Y4', 'name': 'mt_uniqueness_parm', 'description': '', 'createTime': '2021-02-22T09:38:04.000Z', 'updateTime': '2021-02-22T09:38:04.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z000000000019', 'orgId': '0119Y4', 'name': 'mt_validity_expression_parm', 'description': '', 'createTime': '2021-02-22T09:38:04.000Z', 'updateTime': '2021-02-22T09:38:04.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000001S', 'orgId': '0119Y4', 'name': 'MT_Warning', 'description': '', 'createTime': '2021-08-12T12:14:41.000Z', 'updateTime': '2021-09-23T03:11:27.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000000Z', 'orgId': '0119Y4', 'name': 'MT-failure', 'description': '', 'createTime': '2020-12-23T04:47:11.000Z', 'updateTime': '2021-07-07T07:54:53.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000000W', 'orgId': '0119Y4', 'name': 'MT-GOLDMAN2', 'description': '', 'createTime': '2020-12-21T07:14:15.000Z', 'updateTime': '2020-12-21T07:37:12.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z000000000020', 'orgId': '0119Y4', 'name': 'MT-lead_to_ff', 'description': '', 'createTime': '2021-09-07T08:48:46.000Z', 'updateTime': '2021-09-09T02:07:23.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000001K', 'orgId': '0119Y4', 'name': 'MT-midstream-inputnum', 'description': '', 'createTime': '2021-07-02T09:51:08.000Z', 'updateTime': '2021-07-02T09:51:08.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z000000000021', 'orgId': '0119Y4', 'name': 'MT-Redshiftv2-identity', 'description': '', 'createTime': '2021-09-08T10:40:07.000Z', 'updateTime': '2021-09-16T11:27:58.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z000000000022', 'orgId': '0119Y4', 'name': 'MT-Redshiftv2-identity-mapped', 'description': '', 'createTime': '2021-09-08T10:47:28.000Z', 'updateTime': '2021-09-08T10:48:28.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000001C', 'orgId': '0119Y4', 'name': 'MT-rest-ASIS', 'description': '', 'createTime': '2021-03-12T08:05:50.000Z', 'updateTime': '2021-03-12T08:25:22.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000000T', 'orgId': '0119Y4', 'name': 'MTT_editAPI', 'description': '', 'createTime': '2020-12-11T07:38:31.000Z', 'updateTime': '2020-12-14T10:26:02.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000001E', 'orgId': '0119Y4', 'name': 'MTT_SAP_EM_ASIS', 'description': '', 'createTime': '2021-03-17T12:26:11.000Z', 'updateTime': '2021-03-30T11:21:53.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000001M', 'orgId': '0119Y4', 'name': 'mtt-error-03116800', 'description': '', 'createTime': '2021-07-07T07:51:09.000Z', 'updateTime': '2021-07-07T07:58:50.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000001Q', 'orgId': '0119Y4', 'name': 'mtt-error-03143927', 'description': '', 'createTime': '2021-07-30T06:51:33.000Z', 'updateTime': '2021-08-09T05:33:22.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000000U', 'orgId': '0119Y4', 'name': 'mtt-ff-to-ff', 'description': '', 'createTime': '2020-12-15T07:02:15.000Z', 'updateTime': '2021-07-07T07:48:12.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000001H', 'orgId': '0119Y4', 'name': 'MTT-FullParam', 'description': '', 'createTime': '2021-03-22T09:34:21.000Z', 'updateTime': '2021-07-13T06:42:15.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000001T', 'orgId': '0119Y4', 'name': 'MTT-java-decrypt', 'description': '', 'createTime': '2021-08-17T09:29:19.000Z', 'updateTime': '2021-08-26T11:43:44.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000000Y', 'orgId': '0119Y4', 'name': 'MTT-NEWline', 'description': '', 'createTime': '2020-12-21T09:28:49.000Z', 'updateTime': '2020-12-22T09:53:14.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000001P', 'orgId': '0119Y4', 'name': 'mtt-safe-03143927', 'description': '', 'createTime': '2021-07-30T06:38:13.000Z', 'updateTime': '2021-08-09T05:33:22.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000001L', 'orgId': '0119Y4', 'name': 'mtt-success-03116800', 'description': '', 'createTime': '2021-07-07T07:48:52.000Z', 'updateTime': '2021-07-07T07:50:17.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000002E', 'orgId': '0119Y4', 'name': 'RR_03190675', 'description': '', 'createTime': '2021-09-20T04:17:58.000Z', 'updateTime': '2021-09-23T06:45:50.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000002H', 'orgId': '0119Y4', 'name': 'RR_03190675', 'description': '', 'createTime': '2021-09-21T14:48:01.000Z', 'updateTime': '2021-09-23T06:51:10.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000000H', 'orgId': '0119Y4', 'name': 'SampleMappingTask', 'description': '', 'createTime': '2020-11-02T05:21:01.000Z', 'updateTime': '2021-01-07T05:03:36.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000000S', 'orgId': '0119Y4', 'name': 'sp_mtt_shared', 'description': '', 'createTime': '2020-12-04T07:31:54.000Z', 'updateTime': '2020-12-14T10:24:30.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z000000000008', 'orgId': '0119Y4', 'name': 'sp-mt-decode', 'description': '', 'createTime': '2020-09-04T11:58:44.000Z', 'updateTime': '2020-09-04T12:01:25.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z000000000005', 'orgId': '0119Y4', 'name': 'sp-mt-demo', 'description': '', 'createTime': '2020-09-01T11:51:28.000Z', 'updateTime': '2020-09-01T11:51:28.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z000000000007', 'orgId': '0119Y4', 'name': 'sp-mt-encode', 'description': '', 'createTime': '2020-09-04T11:50:05.000Z', 'updateTime': '2020-09-04T11:51:53.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000000O', 'orgId': '0119Y4', 'name': 'sp-mtt-rest-token', 'description': '', 'createTime': '2020-11-12T10:33:38.000Z', 'updateTime': '2020-11-12T10:39:12.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000000L', 'orgId': '0119Y4', 'name': 'sp-mtt-restry', 'description': '', 'createTime': '2020-11-09T14:21:29.000Z', 'updateTime': '2021-01-25T12:00:30.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}, {'@type': 'mtTask', 'id': '0119Y40Z00000000000N', 'orgId': '0119Y4', 'name': 'sp-mtt-wsc', 'description': '', 'createTime': '2020-11-12T08:14:33.000Z', 'updateTime': '2020-11-12T08:46:21.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'maxLogs': 10, 'verbose': False, 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}]
    

## Function: getMTTaskById()

getMTTaskById() returns details for the Mapping Task specified by the Id.

>        Args:
>            id (string): Mapping Task Id.
>
>        Returns:
>            dict: <Mapping Task Details in dict Format>

### Example:


```python
import infapy

# create infa handler
infaHandler = infapy.connect(profile="spani")
v2=infaHandler.v2()

# Perform getMTTaskById()
MTTask=v2.mttask()
print(MTTask.getMTTaskById("0119Y40Z00000000001S"))
```

    {'@type': 'mtTask', 'id': '0119Y40Z00000000001S', 'orgId': '0119Y4', 'name': 'MT_Warning', 'description': '', 'createTime': '2021-08-12T12:14:41.000Z', 'updateTime': '2021-09-23T03:11:27.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'agentId': '0119Y40800000000000A', 'runtimeEnvironmentId': '0119Y425000000000003', 'maxLogs': 10, 'verbose': False, 'lastRunTime': 1632656141000, 'mappingId': '0119Y41700000000001D', 'shortDescription': '', 'sessionProperties': {'Allow Temporary Sequence for Pushdown': 'NO', 'Allow Temporary View for Pushdown': 'NO', 'Error Log Type': 'Flat File', 'Pushdown Optimization': 'None'}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'paramFileType': 'PARAM_FILE_LOCAL', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [{'@type': 'mtTaskParameter', 'id': 361609753, 'name': '$Source$', 'type': 'EXTENDED_SOURCE', 'label': 'Source', 'uiProperties': {'connectionParameterized': 'false', 'isMsrcFilterParameterized': 'false', 'isMsrcSortParameterized': 'false', 'objectParameterized': 'false', 'visible': 'false'}, 'sourceConnectionId': '0119Y40B000000000004', 'newFlatFile': False, 'newObject': False, 'showBusinessNames': False, 'naturalOrder': True, 'truncateTarget': False, 'bulkApiDBTarget': False, 'srcFFAttrs': {'@type': 'flatFileAttrs', 'id': 44960395, 'delimiter': ',', 'textQualifier': '"', 'escapeChar': '', 'headerLineNo': 1, 'firstDataRow': 2}, 'customFuncCfg': {'@type': 'customFuncConfig', 'id': -1, 'connections': [], 'inputMap': [], 'outputFields': []}, 'tgtFieldRefs': {}, 'targetUpdateColumns': [], 'extendedObject': {'@type': 'extendedObject', 'object': {'@type': 'mObject', 'name': 'src_failedtgtrows.txt', 'label': 'src_failedtgtrows.txt', 'metadataUpdated': False, 'relations': [], 'children': []}, 'objects': [{'@type': 'mObject', 'name': 'src_failedtgtrows.txt', 'label': 'src_failedtgtrows.txt', 'metadataUpdated': False, 'relations': [], 'children': []}], 'filters': [], 'sortFields': []}, 'runtimeAttrs': {}, 'isRESTModernSource': True, 'isFileList': False, 'handleSpecialChars': False, 'frsAsset': False, 'dynamicFileName': False, 'currentlyProcessedFileName': False, 'tgtObjectAttributes': {}, 'runtimeParameterData': {'@type': 'mtTaskRuntimeParameterData', 'isConnectionRuntimeParameter': False, 'isObjectRuntimeParameter': False}, 'overriddenFields': []}, {'@type': 'mtTaskParameter', 'id': 361609756, 'name': '$Target$', 'type': 'TARGET', 'label': 'Target', 'uiProperties': {'connectionParameterized': 'false', 'objectParameterized': 'false', 'visible': 'false', 'defaultTargetUpdateColumns': '', 'supportApplyDDLChanges': 'false'}, 'targetConnectionId': '0119Y40B000000000002', 'targetObject': 'MULTIPK', 'targetObjectLabel': 'MULTIPK', 'newFlatFile': False, 'newObject': False, 'showBusinessNames': False, 'naturalOrder': True, 'truncateTarget': False, 'bulkApiDBTarget': False, 'operationType': 'Insert', 'customFuncCfg': {'@type': 'customFuncConfig', 'id': -1, 'connections': [], 'inputMap': [], 'outputFields': []}, 'tgtFieldRefs': {}, 'targetUpdateColumns': [], 'extendedObject': {'@type': 'extendedObject', 'filters': [], 'sortFields': []}, 'runtimeAttrs': {}, 'isRESTModernSource': True, 'isFileList': False, 'handleSpecialChars': False, 'frsAsset': False, 'dynamicFileName': False, 'currentlyProcessedFileName': False, 'objectName': 'MULTIPK', 'objectLabel': 'MULTIPK', 'tgtObjectAttributes': {}, 'runtimeParameterData': {'@type': 'mtTaskRuntimeParameterData', 'isConnectionRuntimeParameter': False, 'isObjectRuntimeParameter': False}, 'overriddenFields': []}], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}
    

## Function: getMTTaskByName()

getMTTaskByName() returns details for the Mapping Task specified by the Name.

>        Args:
>            name (string): Mapping Task Name.
>
>        Returns:
>            dict: <Mapping Task Details in dict Format>

### Example:


```python
import infapy

# create infa handler
infaHandler = infapy.connect(profile="spani")
v2=infaHandler.v2()

# Perform getMTTaskByName()
MTTask=v2.mttask()
print(MTTask.getMTTaskByName("MT IU"))
```

    {'@type': 'mtTask', 'id': '0119Y40Z00000000001B', 'orgId': '0119Y4', 'name': 'MT IU', 'description': '', 'createTime': '2021-03-11T07:06:35.000Z', 'updateTime': '2021-09-24T06:45:30.000Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'agentId': '0119Y408000000000006', 'runtimeEnvironmentId': '0119Y42500000000000E', 'maxLogs': 10, 'verbose': True, 'lastRunTime': 1616080675000, 'mappingId': '0119Y417000000000011', 'shortDescription': '', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'paramFileType': 'PARAM_FILE_LOCAL', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [{'@type': 'mtTaskParameter', 'id': 362429266, 'name': '$Source$', 'type': 'EXTENDED_SOURCE', 'label': 'Source', 'uiProperties': {'connectionParameterized': 'false', 'isMsrcFilterParameterized': 'false', 'isMsrcSortParameterized': 'false', 'objectParameterized': 'false', 'visible': 'false'}, 'sourceConnectionId': '0119Y40B000000000004', 'newFlatFile': False, 'newObject': False, 'showBusinessNames': False, 'naturalOrder': True, 'truncateTarget': False, 'bulkApiDBTarget': False, 'srcFFAttrs': {'@type': 'flatFileAttrs', 'id': 45053350, 'delimiter': ',', 'textQualifier': '"', 'escapeChar': '', 'headerLineNo': 1, 'firstDataRow': 2}, 'customFuncCfg': {'@type': 'customFuncConfig', 'id': -1, 'connections': [], 'inputMap': [], 'outputFields': []}, 'tgtFieldRefs': {}, 'targetUpdateColumns': [], 'extendedObject': {'@type': 'extendedObject', 'object': {'@type': 'mObject', 'name': 'src_HS.csv', 'label': 'src_HS.csv', 'metadataUpdated': False, 'relations': [], 'children': []}, 'objects': [{'@type': 'mObject', 'name': 'src_HS.csv', 'label': 'src_HS.csv', 'metadataUpdated': False, 'relations': [], 'children': []}], 'filters': [], 'sortFields': []}, 'runtimeAttrs': {}, 'isRESTModernSource': True, 'isFileList': False, 'handleSpecialChars': False, 'frsAsset': False, 'dynamicFileName': False, 'currentlyProcessedFileName': False, 'fetchMode': 'ORIGINAL', 'tgtObjectAttributes': {}, 'runtimeParameterData': {'@type': 'mtTaskRuntimeParameterData', 'isConnectionRuntimeParameter': False, 'isObjectRuntimeParameter': False}, 'overriddenFields': []}, {'@type': 'mtTaskParameter', 'id': 362429269, 'name': '$Target$', 'type': 'TARGET', 'label': 'Target', 'uiProperties': {'connectionParameterized': 'false', 'objectParameterized': 'false', 'visible': 'false', 'defaultTargetUpdateColumns': '', 'supportApplyDDLChanges': 'true'}, 'targetConnectionId': '0119Y40B000000000004', 'targetObject': "'T_IU_'||Reg_Extract(op_xml, '((.|\\n)*)(<provider-id>)([^<]*)((.|\\n)*)', 4) ||'_'||  To_Char(SYSDATE,'YYYYMMDD')  ||'.xml'", 'targetObjectLabel': "'T_IU_'||Reg_Extract(op_xml, '((.|\\n)*)(<provider-id>)([^<]*)((.|\\n)*)', 4) ||'_'||  To_Char(SYSDATE,'YYYYMMDD')  ||'.xml'", 'newFlatFile': False, 'newObject': True, 'showBusinessNames': False, 'naturalOrder': True, 'newObjectName': "'T_IU_'||Reg_Extract(op_xml, '((.|\\n)*)(<provider-id>)([^<]*)((.|\\n)*)', 4) ||'_'||  To_Char(SYSDATE,'YYYYMMDD')  ||'.xml'", 'truncateTarget': False, 'bulkApiDBTarget': False, 'operationType': 'Insert', 'tgtFFAttrs': {'@type': 'flatFileAttrs', 'id': 45053353, 'delimiter': ',', 'textQualifier': 'none', 'escapeChar': '', 'headerLineNo': 1}, 'customFuncCfg': {'@type': 'customFuncConfig', 'id': -1, 'connections': [], 'inputMap': [], 'outputFields': []}, 'tgtFieldRefs': {}, 'targetUpdateColumns': [], 'extendedObject': {'@type': 'extendedObject', 'filters': [], 'sortFields': []}, 'runtimeAttrs': {}, 'isRESTModernSource': True, 'isFileList': False, 'handleSpecialChars': False, 'frsAsset': False, 'dynamicFileName': False, 'currentlyProcessedFileName': False, 'objectName': "'T_IU_'||Reg_Extract(op_xml, '((.|\\n)*)(<provider-id>)([^<]*)((.|\\n)*)', 4) ||'_'||  To_Char(SYSDATE,'YYYYMMDD')  ||'.xml'", 'objectLabel': "'T_IU_'||Reg_Extract(op_xml, '((.|\\n)*)(<provider-id>)([^<]*)((.|\\n)*)', 4) ||'_'||  To_Char(SYSDATE,'YYYYMMDD')  ||'.xml'", 'fetchMode': 'ORIGINAL', 'tgtObjectAttributes': {}, 'runtimeParameterData': {'@type': 'mtTaskRuntimeParameterData', 'isConnectionRuntimeParameter': False, 'isObjectRuntimeParameter': False}, 'overriddenFields': []}, {'@type': 'mtTaskParameter', 'id': 362429272, 'name': '$HierarchyBuilder$', 'type': 'HSCHEMA', 'label': 'HierarchyBuilder', 'uiProperties': {'visible': 'false'}, 'newFlatFile': False, 'newObject': False, 'showBusinessNames': True, 'naturalOrder': True, 'truncateTarget': False, 'bulkApiDBTarget': False, 'customFuncCfg': {'@type': 'customFuncConfig', 'id': -1, 'connections': [], 'inputMap': [], 'outputFields': []}, 'tgtFieldRefs': {}, 'targetUpdateColumns': [], 'runtimeAttrs': {}, 'isRESTModernSource': True, 'isFileList': False, 'handleSpecialChars': False, 'frsAsset': False, 'dynamicFileName': False, 'currentlyProcessedFileName': False, 'fetchMode': 'ORIGINAL', 'tgtObjectAttributes': {}, 'runtimeParameterData': {'@type': 'mtTaskRuntimeParameterData', 'isConnectionRuntimeParameter': False, 'isObjectRuntimeParameter': False}, 'overriddenFields': []}], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}
    

## Function: createMTTask()

createMTTask() creates a Mapping Task based on the information provided in the Body. For configuration of body, please refer to: 
            https://docs.informatica.com/integration-cloud/cloud-platform/current-version/rest-api-reference/data-integration-rest-api/mttask.html

>        Args:
>            body (dict): JSON body for POST request.
>
>        Returns:
>            dict: <Details of Create Mapping Task Request in dict Format>

### Example:


```python
import infapy

# create infa handler
infaHandler = infapy.connect(profile="spani")
v2=infaHandler.v2()

#create JSON body
createJSON={
    "@type":"mtTask",
    "name": "MT_IU_v2",
    "containerId": "9wKUcCBrrb1kTpMB2G94UM",
    "description": "IN DEFAULA FOLDER",
    "runtimeEnvironmentId": "0119Y425000000000003",
    "mappingId": "0119Y417000000000011",
    "sessionProperties": {},
    "enableCrossSchemaPushdown": True,
    "enableParallelRun": False,
    "autoTunedApplied": False,
    "autoTunedAppliedType": "NONE",
    "paramFileType": "PARAM_FILE_LOCAL",
    "schemaMode": "async",
    "parameterFileEncoding": "UTF-8",
    "serverlessProperties": {},
    "parameters": [
        {
            "@type": "mtTaskParameter",
            "id": 362430283,
            "name": "$Source$",
            "type": "EXTENDED_SOURCE",
            "label": "Source",
            "uiProperties": {
                "connectionParameterized": "False",
                "isMsrcFilterParameterized": "False",
                "isMsrcSortParameterized": "False",
                "objectParameterized": "False",
                "visible": "False"
            },
            "sourceConnectionId": "0119Y40B000000000004",
            "newFlatFile": False,
            "newObject": False,
            "showBusinessNames": False,
            "naturalOrder": True,
            "truncateTarget": False,
            "bulkApiDBTarget": False,
            "srcFFAttrs": {
                "@type": "flatFileAttrs",
                "id": 45053425,
                "delimiter": ",",
                "textQualifier": "\"",
                "escapeChar": "",
                "headerLineNo": 1,
                "firstDataRow": 2
            },
            "customFuncCfg": {
                "@type": "customFuncConfig",
                "id": -1,
                "connections": [],
                "inputMap": [],
                "outputFields": []
            },
            "tgtFieldRefs": {},
            "targetUpdateColumns": [],
            "extendedObject": {
                "@type": "extendedObject",
                "object": {
                    "@type": "mObject",
                    "name": "src_HS.csv",
                    "label": "src_HS.csv",
                    "metadataUpdated": False,
                    "relations": [],
                    "children": []
                },
                "objects": [
                    {
                        "@type": "mObject",
                        "name": "src_HS.csv",
                        "label": "src_HS.csv",
                        "metadataUpdated": False,
                        "relations": [],
                        "children": []
                    }
                ],
                "filters": [],
                "sortFields": []
            },
            "runtimeAttrs": {},
            "isRESTModernSource": True,
            "isFileList": False,
            "handleSpecialChars": False,
            "frsAsset": False,
            "dynamicFileName": False,
            "currentlyProcessedFileName": False,
            "tgtObjectAttributes": {},
            "runtimeParameterData": {
                "@type": "mtTaskRuntimeParameterData",
                "isConnectionRuntimeParameter": False,
                "isObjectRuntimeParameter": False
            },
            "overriddenFields": []
        },
        {
            "@type": "mtTaskParameter",
            "id": 362430286,
            "name": "$Target$",
            "type": "TARGET",
            "label": "Target",
            "uiProperties": {
                "connectionParameterized": "False",
                "objectParameterized": "False",
                "visible": "False",
                "defaultTargetUpdateColumns": "",
                "supportApplyDDLChanges": "True"
            },
            "targetConnectionId": "0119Y40B000000000004",
            "targetObject": "'T_IU_'||Reg_Extract(op_xml, '((.|\\n)*)(<provider-id>)([^<]*)((.|\\n)*)', 4) ||'_'||  To_Char(SYSDATE,'YYYYMMDD')  ||'.xml'",
            "targetObjectLabel": "'T_IU_'||Reg_Extract(op_xml, '((.|\\n)*)(<provider-id>)([^<]*)((.|\\n)*)', 4) ||'_'||  To_Char(SYSDATE,'YYYYMMDD')  ||'.xml'",
            "newFlatFile": False,
            "newObject": True,
            "showBusinessNames": False,
            "naturalOrder": True,
            "newObjectName": "'T_IU_'||Reg_Extract(op_xml, '((.|\\n)*)(<provider-id>)([^<]*)((.|\\n)*)', 4) ||'_'||  To_Char(SYSDATE,'YYYYMMDD')  ||'.xml'",
            "truncateTarget": False,
            "bulkApiDBTarget": False,
            "operationType": "Insert",
            "tgtFFAttrs": {
                "@type": "flatFileAttrs",
                "id": 45053428,
                "delimiter": ",",
                "textQualifier": "none",
                "escapeChar": "",
                "headerLineNo": 1
            },
            "customFuncCfg": {
                "@type": "customFuncConfig",
                "id": -1,
                "connections": [],
                "inputMap": [],
                "outputFields": []
            },
            "tgtFieldRefs": {},
            "targetUpdateColumns": [],
            "extendedObject": {
                "@type": "extendedObject",
                "filters": [],
                "sortFields": []
            },
            "runtimeAttrs": {},
            "isRESTModernSource": True,
            "isFileList": False,
            "handleSpecialChars": False,
            "frsAsset": False,
            "dynamicFileName": False,
            "currentlyProcessedFileName": False,
            "objectName": "'T_IU_'||Reg_Extract(op_xml, '((.|\\n)*)(<provider-id>)([^<]*)((.|\\n)*)', 4) ||'_'||  To_Char(SYSDATE,'YYYYMMDD')  ||'.xml'",
            "objectLabel": "'T_IU_'||Reg_Extract(op_xml, '((.|\\n)*)(<provider-id>)([^<]*)((.|\\n)*)', 4) ||'_'||  To_Char(SYSDATE,'YYYYMMDD')  ||'.xml'",
            "tgtObjectAttributes": {},
            "runtimeParameterData": {
                "@type": "mtTaskRuntimeParameterData",
                "isConnectionRuntimeParameter": False,
                "isObjectRuntimeParameter": False
            },
            "overriddenFields": []
        },
        {
            "@type": "mtTaskParameter",
            "id": 362430289,
            "name": "$HierarchyBuilder$",
            "type": "HSCHEMA",
            "label": "HierarchyBuilder",
            "uiProperties": {
                "visible": "False"
            },
            "newFlatFile": False,
            "newObject": False,
            "showBusinessNames": True,
            "naturalOrder": True,
            "truncateTarget": False,
            "bulkApiDBTarget": False,
            "customFuncCfg": {
                "@type": "customFuncConfig",
                "id": -1,
                "connections": [],
                "inputMap": [],
                "outputFields": []
            },
            "tgtFieldRefs": {},
            "targetUpdateColumns": [],
            "runtimeAttrs": {},
            "isRESTModernSource": True,
            "isFileList": False,
            "handleSpecialChars": False,
            "frsAsset": False,
            "dynamicFileName": False,
            "currentlyProcessedFileName": False,
            "tgtObjectAttributes": {},
            "runtimeParameterData": {
                "@type": "mtTaskRuntimeParameterData",
                "isConnectionRuntimeParameter": False,
                "isObjectRuntimeParameter": False
            },
            "overriddenFields": []
        }
    ],
    "sequences": [],
    "inOutParameters": [],
    "connRuntimeAttrs": []
}

# Perform createMTTask()
MTTask=v2.mttask()
print(MTTask.createMTTask(createJSON))
```

    {'@type': 'mtTask', 'id': '0119Y40Z00000000002Q', 'orgId': '0119Y4', 'name': 'MT_IU_v2', 'description': 'IN DEFAULA FOLDER', 'createTime': '2021-09-26T07:56:36.628Z', 'updateTime': '2021-09-26T07:56:36.628Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'agentId': '0119Y40800000000000A', 'runtimeEnvironmentId': '0119Y425000000000003', 'maxLogs': 10, 'verbose': False, 'mappingId': '0119Y417000000000011', 'shortDescription': 'IN DEFAULA FOLDER', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'paramFileType': 'PARAM_FILE_LOCAL', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [{'@type': 'mtTaskParameter', 'id': 362949169, 'name': '$Source$', 'type': 'EXTENDED_SOURCE', 'label': 'Source', 'uiProperties': {}, 'sourceConnectionId': '0119Y40B000000000004', 'newFlatFile': False, 'newObject': False, 'showBusinessNames': False, 'naturalOrder': True, 'truncateTarget': False, 'bulkApiDBTarget': False, 'srcFFAttrs': {'@type': 'flatFileAttrs', 'id': 45116533, 'delimiter': ',', 'textQualifier': '"', 'escapeChar': '', 'headerLineNo': 1, 'firstDataRow': 2}, 'customFuncCfg': {'@type': 'customFuncConfig', 'id': -1, 'connections': [], 'inputMap': [], 'outputFields': []}, 'tgtFieldRefs': {}, 'targetUpdateColumns': [], 'extendedObject': {'@type': 'extendedObject', 'object': {'@type': 'mObject', 'name': 'src_HS.csv', 'label': 'src_HS.csv', 'metadataUpdated': False, 'relations': [], 'children': []}, 'objects': [{'@type': 'mObject', 'name': 'src_HS.csv', 'label': 'src_HS.csv', 'metadataUpdated': False, 'relations': [], 'children': []}], 'filters': [], 'sortFields': []}, 'runtimeAttrs': {}, 'isRESTModernSource': True, 'isFileList': False, 'handleSpecialChars': False, 'frsAsset': False, 'dynamicFileName': False, 'currentlyProcessedFileName': False, 'fetchMode': 'ORIGINAL', 'tgtObjectAttributes': {}, 'runtimeParameterData': {'@type': 'mtTaskRuntimeParameterData', 'isConnectionRuntimeParameter': False, 'isObjectRuntimeParameter': False}, 'overriddenFields': []}, {'@type': 'mtTaskParameter', 'id': 362949172, 'name': '$Target$', 'type': 'TARGET', 'label': 'Target', 'uiProperties': {}, 'targetConnectionId': '0119Y40B000000000004', 'targetObject': "'T_IU_'||Reg_Extract(op_xml, '((.|\\n)*)(<provider-id>)([^<]*)((.|\\n)*)', 4) ||'_'||  To_Char(SYSDATE,'YYYYMMDD')  ||'.xml'", 'targetObjectLabel': "'T_IU_'||Reg_Extract(op_xml, '((.|\\n)*)(<provider-id>)([^<]*)((.|\\n)*)', 4) ||'_'||  To_Char(SYSDATE,'YYYYMMDD')  ||'.xml'", 'newFlatFile': False, 'newObject': True, 'showBusinessNames': False, 'naturalOrder': True, 'newObjectName': "'T_IU_'||Reg_Extract(op_xml, '((.|\\n)*)(<provider-id>)([^<]*)((.|\\n)*)', 4) ||'_'||  To_Char(SYSDATE,'YYYYMMDD')  ||'.xml'", 'truncateTarget': False, 'bulkApiDBTarget': False, 'operationType': 'Insert', 'tgtFFAttrs': {'@type': 'flatFileAttrs', 'id': 45116536, 'delimiter': ',', 'textQualifier': 'none', 'escapeChar': '', 'headerLineNo': 1}, 'customFuncCfg': {'@type': 'customFuncConfig', 'id': -1, 'connections': [], 'inputMap': [], 'outputFields': []}, 'tgtFieldRefs': {}, 'targetUpdateColumns': [], 'extendedObject': {'@type': 'extendedObject', 'filters': [], 'sortFields': []}, 'runtimeAttrs': {}, 'isRESTModernSource': True, 'isFileList': False, 'handleSpecialChars': False, 'frsAsset': False, 'dynamicFileName': False, 'currentlyProcessedFileName': False, 'objectName': "'T_IU_'||Reg_Extract(op_xml, '((.|\\n)*)(<provider-id>)([^<]*)((.|\\n)*)', 4) ||'_'||  To_Char(SYSDATE,'YYYYMMDD')  ||'.xml'", 'objectLabel': "'T_IU_'||Reg_Extract(op_xml, '((.|\\n)*)(<provider-id>)([^<]*)((.|\\n)*)', 4) ||'_'||  To_Char(SYSDATE,'YYYYMMDD')  ||'.xml'", 'fetchMode': 'ORIGINAL', 'tgtObjectAttributes': {}, 'runtimeParameterData': {'@type': 'mtTaskRuntimeParameterData', 'isConnectionRuntimeParameter': False, 'isObjectRuntimeParameter': False}, 'overriddenFields': []}, {'@type': 'mtTaskParameter', 'id': 362949175, 'name': '$HierarchyBuilder$', 'type': 'HSCHEMA', 'label': 'HierarchyBuilder', 'uiProperties': {}, 'newFlatFile': False, 'newObject': False, 'showBusinessNames': True, 'naturalOrder': True, 'truncateTarget': False, 'bulkApiDBTarget': False, 'customFuncCfg': {'@type': 'customFuncConfig', 'id': -1, 'connections': [], 'inputMap': [], 'outputFields': []}, 'tgtFieldRefs': {}, 'targetUpdateColumns': [], 'runtimeAttrs': {}, 'isRESTModernSource': True, 'isFileList': False, 'handleSpecialChars': False, 'frsAsset': False, 'dynamicFileName': False, 'currentlyProcessedFileName': False, 'fetchMode': 'ORIGINAL', 'tgtObjectAttributes': {}, 'runtimeParameterData': {'@type': 'mtTaskRuntimeParameterData', 'isConnectionRuntimeParameter': False, 'isObjectRuntimeParameter': False}, 'overriddenFields': []}], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}
    

## Function: updateMTTaskFull()

updateMTTaskFull() updates an existing Mapping Task with specified ID based on the information provided in the Body, with Partial Mode Disabled. For configuration of body, please refer to: 
            https://docs.informatica.com/integration-cloud/cloud-platform/current-version/rest-api-reference/data-integration-rest-api/mttask.html

>        Args:
>            body (dict): JSON body for POST request.
>
>        Returns:
>            dict: <Details of Update Mapping Task Request in dict Format>

### Example:


```python
import infapy

# create infa handler
infaHandler = infapy.connect(profile="spani")
v2=infaHandler.v2()

#create JSON body
updateFullJSON={
    "@type":"mtTask",
    "name": "MT_IU_v3",
    "containerId": "9wKUcCBrrb1kTpMB2G94UM",
    "description": "NEW_DESCRIPTION",
    "runtimeEnvironmentId": "0119Y425000000000003",
    "mappingId": "0119Y417000000000011",
    "sessionProperties": {},
    "enableCrossSchemaPushdown": True,
    "enableParallelRun": False,
    "autoTunedApplied": False,
    "autoTunedAppliedType": "NONE",
    "paramFileType": "PARAM_FILE_LOCAL",
    "schemaMode": "async",
    "parameterFileEncoding": "UTF-8",
    "serverlessProperties": {},
    "parameters": [
        {
            "@type": "mtTaskParameter",
            "id": 362430283,
            "name": "$Source$",
            "type": "EXTENDED_SOURCE",
            "label": "Source",
            "uiProperties": {
                "connectionParameterized": "False",
                "isMsrcFilterParameterized": "False",
                "isMsrcSortParameterized": "False",
                "objectParameterized": "False",
                "visible": "False"
            },
            "sourceConnectionId": "0119Y40B000000000004",
            "newFlatFile": False,
            "newObject": False,
            "showBusinessNames": False,
            "naturalOrder": True,
            "truncateTarget": False,
            "bulkApiDBTarget": False,
            "srcFFAttrs": {
                "@type": "flatFileAttrs",
                "id": 45053425,
                "delimiter": ",",
                "textQualifier": "\"",
                "escapeChar": "",
                "headerLineNo": 1,
                "firstDataRow": 2
            },
            "customFuncCfg": {
                "@type": "customFuncConfig",
                "id": -1,
                "connections": [],
                "inputMap": [],
                "outputFields": []
            },
            "tgtFieldRefs": {},
            "targetUpdateColumns": [],
            "extendedObject": {
                "@type": "extendedObject",
                "object": {
                    "@type": "mObject",
                    "name": "src_HS.csv",
                    "label": "src_HS.csv",
                    "metadataUpdated": False,
                    "relations": [],
                    "children": []
                },
                "objects": [
                    {
                        "@type": "mObject",
                        "name": "src_HS.csv",
                        "label": "src_HS.csv",
                        "metadataUpdated": False,
                        "relations": [],
                        "children": []
                    }
                ],
                "filters": [],
                "sortFields": []
            },
            "runtimeAttrs": {},
            "isRESTModernSource": True,
            "isFileList": False,
            "handleSpecialChars": False,
            "frsAsset": False,
            "dynamicFileName": False,
            "currentlyProcessedFileName": False,
            "tgtObjectAttributes": {},
            "runtimeParameterData": {
                "@type": "mtTaskRuntimeParameterData",
                "isConnectionRuntimeParameter": False,
                "isObjectRuntimeParameter": False
            },
            "overriddenFields": []
        },
        {
            "@type": "mtTaskParameter",
            "id": 362430286,
            "name": "$Target$",
            "type": "TARGET",
            "label": "Target",
            "uiProperties": {
                "connectionParameterized": "False",
                "objectParameterized": "False",
                "visible": "False",
                "defaultTargetUpdateColumns": "",
                "supportApplyDDLChanges": "True"
            },
            "targetConnectionId": "0119Y40B000000000004",
            "targetObject": "'T_IU_'||Reg_Extract(op_xml, '((.|\\n)*)(<provider-id>)([^<]*)((.|\\n)*)', 4) ||'_'||  To_Char(SYSDATE,'YYYYMMDD')  ||'.xml'",
            "targetObjectLabel": "'T_IU_'||Reg_Extract(op_xml, '((.|\\n)*)(<provider-id>)([^<]*)((.|\\n)*)', 4) ||'_'||  To_Char(SYSDATE,'YYYYMMDD')  ||'.xml'",
            "newFlatFile": False,
            "newObject": True,
            "showBusinessNames": False,
            "naturalOrder": True,
            "newObjectName": "'T_IU_'||Reg_Extract(op_xml, '((.|\\n)*)(<provider-id>)([^<]*)((.|\\n)*)', 4) ||'_'||  To_Char(SYSDATE,'YYYYMMDD')  ||'.xml'",
            "truncateTarget": False,
            "bulkApiDBTarget": False,
            "operationType": "Insert",
            "tgtFFAttrs": {
                "@type": "flatFileAttrs",
                "id": 45053428,
                "delimiter": ",",
                "textQualifier": "none",
                "escapeChar": "",
                "headerLineNo": 1
            },
            "customFuncCfg": {
                "@type": "customFuncConfig",
                "id": -1,
                "connections": [],
                "inputMap": [],
                "outputFields": []
            },
            "tgtFieldRefs": {},
            "targetUpdateColumns": [],
            "extendedObject": {
                "@type": "extendedObject",
                "filters": [],
                "sortFields": []
            },
            "runtimeAttrs": {},
            "isRESTModernSource": True,
            "isFileList": False,
            "handleSpecialChars": False,
            "frsAsset": False,
            "dynamicFileName": False,
            "currentlyProcessedFileName": False,
            "objectName": "'T_IU_'||Reg_Extract(op_xml, '((.|\\n)*)(<provider-id>)([^<]*)((.|\\n)*)', 4) ||'_'||  To_Char(SYSDATE,'YYYYMMDD')  ||'.xml'",
            "objectLabel": "'T_IU_'||Reg_Extract(op_xml, '((.|\\n)*)(<provider-id>)([^<]*)((.|\\n)*)', 4) ||'_'||  To_Char(SYSDATE,'YYYYMMDD')  ||'.xml'",
            "tgtObjectAttributes": {},
            "runtimeParameterData": {
                "@type": "mtTaskRuntimeParameterData",
                "isConnectionRuntimeParameter": False,
                "isObjectRuntimeParameter": False
            },
            "overriddenFields": []
        },
        {
            "@type": "mtTaskParameter",
            "id": 362430289,
            "name": "$HierarchyBuilder$",
            "type": "HSCHEMA",
            "label": "HierarchyBuilder",
            "uiProperties": {
                "visible": "False"
            },
            "newFlatFile": False,
            "newObject": False,
            "showBusinessNames": True,
            "naturalOrder": True,
            "truncateTarget": False,
            "bulkApiDBTarget": False,
            "customFuncCfg": {
                "@type": "customFuncConfig",
                "id": -1,
                "connections": [],
                "inputMap": [],
                "outputFields": []
            },
            "tgtFieldRefs": {},
            "targetUpdateColumns": [],
            "runtimeAttrs": {},
            "isRESTModernSource": True,
            "isFileList": False,
            "handleSpecialChars": False,
            "frsAsset": False,
            "dynamicFileName": False,
            "currentlyProcessedFileName": False,
            "tgtObjectAttributes": {},
            "runtimeParameterData": {
                "@type": "mtTaskRuntimeParameterData",
                "isConnectionRuntimeParameter": False,
                "isObjectRuntimeParameter": False
            },
            "overriddenFields": []
        }
    ],
    "sequences": [],
    "inOutParameters": [],
    "connRuntimeAttrs": []
}

# Perform updateMTTaskFull()
MTTask=v2.mttask()
print(MTTask.updateMTTaskFull(updateFullJSON,"0119Y40Z00000000002Q"))
```

    {'@type': 'mtTask', 'id': '0119Y40Z00000000002Q', 'orgId': '0119Y4', 'name': 'MT_IU_v3', 'description': 'NEW_DESCRIPTION', 'createTime': '2021-09-26T07:56:37.000Z', 'updateTime': '2021-09-26T07:59:14.713Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'agentId': '0119Y40800000000000A', 'runtimeEnvironmentId': '0119Y425000000000003', 'maxLogs': 10, 'verbose': False, 'mappingId': '0119Y417000000000011', 'shortDescription': 'NEW_DESCRIPTION', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'paramFileType': 'PARAM_FILE_LOCAL', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [{'@type': 'mtTaskParameter', 'id': 362949262, 'name': '$Source$', 'type': 'EXTENDED_SOURCE', 'label': 'Source', 'uiProperties': {}, 'sourceConnectionId': '0119Y40B000000000004', 'newFlatFile': False, 'newObject': False, 'showBusinessNames': False, 'naturalOrder': True, 'truncateTarget': False, 'bulkApiDBTarget': False, 'srcFFAttrs': {'@type': 'flatFileAttrs', 'id': 45116539, 'delimiter': ',', 'textQualifier': '"', 'escapeChar': '', 'headerLineNo': 1, 'firstDataRow': 2}, 'customFuncCfg': {'@type': 'customFuncConfig', 'id': -1, 'connections': [], 'inputMap': [], 'outputFields': []}, 'tgtFieldRefs': {}, 'targetUpdateColumns': [], 'extendedObject': {'@type': 'extendedObject', 'object': {'@type': 'mObject', 'name': 'src_HS.csv', 'label': 'src_HS.csv', 'metadataUpdated': False, 'relations': [], 'children': []}, 'objects': [{'@type': 'mObject', 'name': 'src_HS.csv', 'label': 'src_HS.csv', 'metadataUpdated': False, 'relations': [], 'children': []}], 'filters': [], 'sortFields': []}, 'runtimeAttrs': {}, 'isRESTModernSource': True, 'isFileList': False, 'handleSpecialChars': False, 'frsAsset': False, 'dynamicFileName': False, 'currentlyProcessedFileName': False, 'fetchMode': 'ORIGINAL', 'tgtObjectAttributes': {}, 'runtimeParameterData': {'@type': 'mtTaskRuntimeParameterData', 'isConnectionRuntimeParameter': False, 'isObjectRuntimeParameter': False}, 'overriddenFields': []}, {'@type': 'mtTaskParameter', 'id': 362949265, 'name': '$Target$', 'type': 'TARGET', 'label': 'Target', 'uiProperties': {}, 'targetConnectionId': '0119Y40B000000000004', 'targetObject': "'T_IU_'||Reg_Extract(op_xml, '((.|\\n)*)(<provider-id>)([^<]*)((.|\\n)*)', 4) ||'_'||  To_Char(SYSDATE,'YYYYMMDD')  ||'.xml'", 'targetObjectLabel': "'T_IU_'||Reg_Extract(op_xml, '((.|\\n)*)(<provider-id>)([^<]*)((.|\\n)*)', 4) ||'_'||  To_Char(SYSDATE,'YYYYMMDD')  ||'.xml'", 'newFlatFile': False, 'newObject': True, 'showBusinessNames': False, 'naturalOrder': True, 'newObjectName': "'T_IU_'||Reg_Extract(op_xml, '((.|\\n)*)(<provider-id>)([^<]*)((.|\\n)*)', 4) ||'_'||  To_Char(SYSDATE,'YYYYMMDD')  ||'.xml'", 'truncateTarget': False, 'bulkApiDBTarget': False, 'operationType': 'Insert', 'tgtFFAttrs': {'@type': 'flatFileAttrs', 'id': 45116542, 'delimiter': ',', 'textQualifier': 'none', 'escapeChar': '', 'headerLineNo': 1}, 'customFuncCfg': {'@type': 'customFuncConfig', 'id': -1, 'connections': [], 'inputMap': [], 'outputFields': []}, 'tgtFieldRefs': {}, 'targetUpdateColumns': [], 'extendedObject': {'@type': 'extendedObject', 'filters': [], 'sortFields': []}, 'runtimeAttrs': {}, 'isRESTModernSource': True, 'isFileList': False, 'handleSpecialChars': False, 'frsAsset': False, 'dynamicFileName': False, 'currentlyProcessedFileName': False, 'objectName': "'T_IU_'||Reg_Extract(op_xml, '((.|\\n)*)(<provider-id>)([^<]*)((.|\\n)*)', 4) ||'_'||  To_Char(SYSDATE,'YYYYMMDD')  ||'.xml'", 'objectLabel': "'T_IU_'||Reg_Extract(op_xml, '((.|\\n)*)(<provider-id>)([^<]*)((.|\\n)*)', 4) ||'_'||  To_Char(SYSDATE,'YYYYMMDD')  ||'.xml'", 'fetchMode': 'ORIGINAL', 'tgtObjectAttributes': {}, 'runtimeParameterData': {'@type': 'mtTaskRuntimeParameterData', 'isConnectionRuntimeParameter': False, 'isObjectRuntimeParameter': False}, 'overriddenFields': []}, {'@type': 'mtTaskParameter', 'id': 362949268, 'name': '$HierarchyBuilder$', 'type': 'HSCHEMA', 'label': 'HierarchyBuilder', 'uiProperties': {}, 'newFlatFile': False, 'newObject': False, 'showBusinessNames': True, 'naturalOrder': True, 'truncateTarget': False, 'bulkApiDBTarget': False, 'customFuncCfg': {'@type': 'customFuncConfig', 'id': -1, 'connections': [], 'inputMap': [], 'outputFields': []}, 'tgtFieldRefs': {}, 'targetUpdateColumns': [], 'runtimeAttrs': {}, 'isRESTModernSource': True, 'isFileList': False, 'handleSpecialChars': False, 'frsAsset': False, 'dynamicFileName': False, 'currentlyProcessedFileName': False, 'fetchMode': 'ORIGINAL', 'tgtObjectAttributes': {}, 'runtimeParameterData': {'@type': 'mtTaskRuntimeParameterData', 'isConnectionRuntimeParameter': False, 'isObjectRuntimeParameter': False}, 'overriddenFields': []}], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}
    

## Function: updateMTTaskPartial()

updateMTTaskPartial() updates an existing Mapping Task with specified ID based on the information provided in the Body, with Partial Mode Enabled. For configuration of body, please refer to: 
            https://docs.informatica.com/integration-cloud/cloud-platform/current-version/rest-api-reference/data-integration-rest-api/mttask.html

>        Args:
>            body (dict): JSON body for POST request.
>
>        Returns:
>            dict: <Details of Partial Update Mapping Task Request in dict Format>

### Example:


```python
import infapy

# create infa handler
infaHandler = infapy.connect(profile="spani")
v2=infaHandler.v2()

# create JSON body
updatePartialJSON={
    "@type":"mtTask",
    "description": "NEW DESCRIPTION V2"
}

# Perform updateMTTaskPartial()
MTTask=v2.mttask()
print(MTTask.updateMTTaskPartial(updatePartialJSON,"0119Y40Z00000000002Q"))
```

    {'@type': 'mtTask', 'id': '0119Y40Z00000000002Q', 'orgId': '0119Y4', 'name': 'MT_IU_v3', 'description': 'NEW DESCRIPTION V2', 'createTime': '2021-09-26T07:56:37.000Z', 'updateTime': '2021-09-26T08:02:29.295Z', 'createdBy': 'admin021651', 'updatedBy': 'admin021651', 'agentId': '0119Y40800000000000A', 'runtimeEnvironmentId': '0119Y425000000000003', 'maxLogs': 10, 'verbose': False, 'mappingId': '0119Y417000000000011', 'shortDescription': 'NEW DESCRIPTION V2', 'sessionProperties': {}, 'enableCrossSchemaPushdown': True, 'enableParallelRun': False, 'autoTunedApplied': False, 'autoTunedAppliedType': 'NONE', 'paramFileType': 'PARAM_FILE_LOCAL', 'schemaMode': 'async', 'parameterFileEncoding': 'UTF-8', 'serverlessProperties': {}, 'parameters': [{'@type': 'mtTaskParameter', 'id': 362949397, 'name': '$Source$', 'type': 'EXTENDED_SOURCE', 'label': 'Source', 'uiProperties': {}, 'sourceConnectionId': '0119Y40B000000000004', 'newFlatFile': False, 'newObject': False, 'showBusinessNames': False, 'naturalOrder': True, 'truncateTarget': False, 'bulkApiDBTarget': False, 'srcFFAttrs': {'@type': 'flatFileAttrs', 'id': 45116572, 'delimiter': ',', 'textQualifier': '"', 'escapeChar': '', 'headerLineNo': 1, 'firstDataRow': 2}, 'customFuncCfg': {'@type': 'customFuncConfig', 'id': -1, 'connections': [], 'inputMap': [], 'outputFields': []}, 'tgtFieldRefs': {}, 'targetUpdateColumns': [], 'extendedObject': {'@type': 'extendedObject', 'object': {'@type': 'mObject', 'name': 'src_HS.csv', 'label': 'src_HS.csv', 'metadataUpdated': False, 'relations': [], 'children': []}, 'objects': [{'@type': 'mObject', 'name': 'src_HS.csv', 'label': 'src_HS.csv', 'metadataUpdated': False, 'relations': [], 'children': []}], 'filters': [], 'sortFields': []}, 'runtimeAttrs': {}, 'isRESTModernSource': True, 'isFileList': False, 'handleSpecialChars': False, 'frsAsset': False, 'dynamicFileName': False, 'currentlyProcessedFileName': False, 'fetchMode': 'ORIGINAL', 'tgtObjectAttributes': {}, 'runtimeParameterData': {'@type': 'mtTaskRuntimeParameterData', 'isConnectionRuntimeParameter': False, 'isObjectRuntimeParameter': False}, 'overriddenFields': []}, {'@type': 'mtTaskParameter', 'id': 362949400, 'name': '$Target$', 'type': 'TARGET', 'label': 'Target', 'uiProperties': {}, 'targetConnectionId': '0119Y40B000000000004', 'targetObject': "'T_IU_'||Reg_Extract(op_xml, '((.|\\n)*)(<provider-id>)([^<]*)((.|\\n)*)', 4) ||'_'||  To_Char(SYSDATE,'YYYYMMDD')  ||'.xml'", 'targetObjectLabel': "'T_IU_'||Reg_Extract(op_xml, '((.|\\n)*)(<provider-id>)([^<]*)((.|\\n)*)', 4) ||'_'||  To_Char(SYSDATE,'YYYYMMDD')  ||'.xml'", 'newFlatFile': False, 'newObject': True, 'showBusinessNames': False, 'naturalOrder': True, 'newObjectName': "'T_IU_'||Reg_Extract(op_xml, '((.|\\n)*)(<provider-id>)([^<]*)((.|\\n)*)', 4) ||'_'||  To_Char(SYSDATE,'YYYYMMDD')  ||'.xml'", 'truncateTarget': False, 'bulkApiDBTarget': False, 'operationType': 'Insert', 'tgtFFAttrs': {'@type': 'flatFileAttrs', 'id': 45116575, 'delimiter': ',', 'textQualifier': 'none', 'escapeChar': '', 'headerLineNo': 1}, 'customFuncCfg': {'@type': 'customFuncConfig', 'id': -1, 'connections': [], 'inputMap': [], 'outputFields': []}, 'tgtFieldRefs': {}, 'targetUpdateColumns': [], 'extendedObject': {'@type': 'extendedObject', 'filters': [], 'sortFields': []}, 'runtimeAttrs': {}, 'isRESTModernSource': True, 'isFileList': False, 'handleSpecialChars': False, 'frsAsset': False, 'dynamicFileName': False, 'currentlyProcessedFileName': False, 'objectName': "'T_IU_'||Reg_Extract(op_xml, '((.|\\n)*)(<provider-id>)([^<]*)((.|\\n)*)', 4) ||'_'||  To_Char(SYSDATE,'YYYYMMDD')  ||'.xml'", 'objectLabel': "'T_IU_'||Reg_Extract(op_xml, '((.|\\n)*)(<provider-id>)([^<]*)((.|\\n)*)', 4) ||'_'||  To_Char(SYSDATE,'YYYYMMDD')  ||'.xml'", 'fetchMode': 'ORIGINAL', 'tgtObjectAttributes': {}, 'runtimeParameterData': {'@type': 'mtTaskRuntimeParameterData', 'isConnectionRuntimeParameter': False, 'isObjectRuntimeParameter': False}, 'overriddenFields': []}, {'@type': 'mtTaskParameter', 'id': 362949403, 'name': '$HierarchyBuilder$', 'type': 'HSCHEMA', 'label': 'HierarchyBuilder', 'uiProperties': {}, 'newFlatFile': False, 'newObject': False, 'showBusinessNames': True, 'naturalOrder': True, 'truncateTarget': False, 'bulkApiDBTarget': False, 'customFuncCfg': {'@type': 'customFuncConfig', 'id': -1, 'connections': [], 'inputMap': [], 'outputFields': []}, 'tgtFieldRefs': {}, 'targetUpdateColumns': [], 'runtimeAttrs': {}, 'isRESTModernSource': True, 'isFileList': False, 'handleSpecialChars': False, 'frsAsset': False, 'dynamicFileName': False, 'currentlyProcessedFileName': False, 'fetchMode': 'ORIGINAL', 'tgtObjectAttributes': {}, 'runtimeParameterData': {'@type': 'mtTaskRuntimeParameterData', 'isConnectionRuntimeParameter': False, 'isObjectRuntimeParameter': False}, 'overriddenFields': []}], 'sequences': [], 'inOutParameters': [], 'connRuntimeAttrs': []}
    

## Function: deleteMTTask()

deleteMTTask() deletes the Mapping Task specified by the Id.

>        Args:
>            id (string): Mapping Task Id.
>
>        Returns:
>            dict: <Details of Delete Mapping Task Request in dict Format>

### Example:


```python
import infapy

# create infa handler
infaHandler = infapy.connect(profile="spani")
v2=infaHandler.v2()

# Perform getAllMTTasks()
MTTask=v2.mttask()
print(MTTask.deleteMTTask("0119Y40Z00000000002Q"))
```

    {'Status': 'Mapping Task 0119Y40Z00000000002Q has been deleted.'}
    
