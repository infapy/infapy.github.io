# Register

## Function: registerSubOrg()

registerSubOrg() can be used register a new sub org

>        Args:
>            subOrgRegInfoInJson (dict): Details for Sub-org Registeration in json format
>
>        Returns:
>            List of dict: <Sub Org Details in dict Format>

### Example


```python
import infapy

#Create infa handler
infaHandler = infapy.connect(profile="jefjames")
v2=infaHandler.v2()

#Call registerSubOrg()
data = {'@type' : 'registration','user' : {'@type' : 'user','name' : 'jjtest','emails' : 'email@company.com','firstName' : 'firstName','lastName' : 'lastName','title' : 'jobTitle','phone' : '(0)1234 567 890','timezone' : 'null','forceChangePassword' : 'false'},'org' : {'@type' : 'org','offerCode' : 'PPC30daytrial', 'campaignCode' : 'PPC','name' : 'testorg','address1' : '1 Main St','city' : 'Mycity','state' : 'CA','zipcode' : '90210','country' : 'US','employees' : '5001_'},'registrationCode' : 'ics-standard', 'sendEmail' : 'true'}
response = v2.org().registerSubOrg(data)
print(response)
```

This function returns the details for the newly created Sub-org
