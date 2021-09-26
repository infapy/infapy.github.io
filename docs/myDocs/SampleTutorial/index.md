# A Sample Tutorial

The goal of this tutorial is to help you get started with infapy. infapy is a very simple, yet powerful tool to automate business specific use cases with python. 

You can do a lot with our library of which some examples include, triggerring a mapping task with job (v2), monitoring the jobs using (ActivityMonitor), performing auto code migration (with v3 export, import) etc.

In this tutorial, we walk you through the 1,2 and 3 steps required to get started.

## Creating the config files

We follow a profile based approach to connect to informatica cloud and use a strong encrypted key so passwords are not stored in clear text.

##### Creating the configuration files:

In Linux the default path is: ~/.infa/
In Windows the default path is: C:\Users\yourUserName\\.infa\

Create two files in this location
- credentials
- config

In the credentials file, store the credentails with a profile Name, like below:
>    [default]<br>
>    region = us<br>
>
>    [myProfile]<br>
>    region = us<br>
>    
>    [dev]<br>
>    region = us<br>

In the config file, store the infa_access_key_id and the infa_secret_access_key with the profile Name, like below.
>    [default]<br>
>    infa_access_key_id = value<br>
>    infa_secret_access_key = value<br>
>
>
>    [myProfile]<br>
>    infa_access_key_id = value<br>
>    infa_secret_access_key = value<br>
>    
>    [dev]<br>
>    infa_access_key_id = value<br>
>    infa_secret_access_key = value<br>

Follow the getting started guide for steps to use the encrypt function to get the above access key values


## Connecting to Informatica Cloud


```python
import infapy
infaHandler = infapy.connect(profile="DEV")

# if you are using the default profile
infaHandler = infapy.connect()
```

## Enabling Logging with Infapy

We support two types of loggers, 

- One is a file logger which logs all activities to a file called infapy.log in the current working directory where the script is running.
- The second is stream logger. Useful when you are working with python in the shell / command prompt so the logs are streamed.


We support 4 levels of logging:
>    - DEBUG
>    - INFO
>    - WARN
>    - ERROR
    
Please note that enabling DEBUG logging will output the entire wire trace to the log files.

### Enabling File Logger

>    Use this function to enable file logging<br>
>
>    Args:<br>
>        name (str, optional): Name of your logger. Defaults to "infapy".<br>
>        filepath (type, optional): The location where you want to create the file. Defaults to current working directory.<br>
>        level (type, optional): DEBUG/WARN/INFO/ERROR. Default is at INFO<br>
>        formatString (type, optional): If you want to change the formating of the logger<br>


```python
# Add the below code at the start of every script
# ideally the name of the logger is the name of your script
# so if your script is prodExport.py
# name of logger is prodExport

import infapy
infapy.setFileLogger(name="test",level="DEBUG")
infaHandler = infapy.connect(profile="DEV")
```

### Enabling Stream Logger:

>    Use this function to enable file logging<br>
>
>    Args:<br>
>        name (str, optional): Name of your logger. Defaults to "infapy".<br>
>        level (type, optional): DEBUG/WARN/INFO/ERROR. Default is at INFO<br>
>        formatString (type, optional): If you want to change the formating of the logger<br>


```python
# Add the below code at the start of every script
# ideally the name of the logger is the name of your script
# so if your script is prodExport.py
# name of logger is prodExport

import infapy
infapy.setStreamLogger(name="test",level="INFO")
infaHandler = infapy.connect(profile="DEV")
```

    2021-09-26 23:42:56,267  test  INFO: New instance of infapy started from hostname: INWPF23T242-AAD
    2021-09-26 23:42:56,276  test  INFO: Host OS: Windows
    2021-09-26 23:42:56,277  test  INFO: INFAPY Root Path: C:\Users\ppradeep\.infa
    

## Creating the informatica handlers


```python
infaHandler = infapy.connect(profile="DEV")

# Create v3 handle
v3 = infaHandler.v3()

# Create v2 handle
v2 = infaHandler.v2()

```

    2021-09-26 23:44:30,582  test  INFO: Created the v3 object to access the iics v3 apis
    2021-09-26 23:44:30,583  test  INFO: created a v3 handler object successfully
    2021-09-26 23:44:30,584  test  INFO: v3BaseURL: https://na1.dm-us.informaticacloud.com/saas
    2021-09-26 23:44:30,592  test  INFO: Created the v2 object to access the iics v2 apis
    2021-09-26 23:44:30,592  test  INFO: created a v2 class object successfully
    2021-09-26 23:44:30,593  test  INFO: v2BaseURL: https://na1.dm-us.informaticacloud.com/saas
    

You are now ready to follow along the tutorials to get started. I suggest you review the Business Scenarios next and then proceed with the documentaion.
