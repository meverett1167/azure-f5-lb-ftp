# azure-f5-lb
## Summary
Deploys a demo app protected by HA pair of F5 behind Azure ALB

## Requirements
- 2x eval keys for BIG-IP
- AS3 declaration for BIG-IP configuration, or, use default value of https://raw.githubusercontent.com/mikeoleary/azure-f5-lb/master/declaration.json

## Deploy
  [![Deploy to Azure](http://azuredeploy.net/deploybutton.png)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fmikeoleary%2Fazure-f5-lb%2Fmaster%2Fazuredeploy.json)
  
## Verify
### Verify F5 config
When the Azure deployment completes, the output will contain multiple URL's. Use these to inspect the configuration of the BIG-IP devices using the UI over HTTPS, or console over SSH. 
### Verify application
There is also a URL for the app that is deployed and protected by BIG-IP. Visit this URL and inspect your IP headers and other information about your connection. It may take a few mins (approx 5 mins) after the Azure deployment has completed for the application to be up and running, and reachable via the URL provided in the outputs.
