# bicep_deployment
Template repo for deployment of Azure resources with bicep


## Powershell deployment
* Start by running `Connect-AzAccount -TenantId <Tenant id> -Subscription <Subscription id>` 
* To set default resource group run `Set-AzDefault -ResourceGroupName [sandbox resource group name]` 
* Deploy based on main file by running `New-AzResourceGroupDeployment -TemplateFile main.bicep`

Note that it is possible to use the `-WhatIf` parameter for deployment, which lists the changes that would be deployed to. To do a WhatIf followed by a chioce to deploy changes or not, use `-Confirm` instead of `-WhatIf`. Additionally, the mode can be set to _Incremental_ or _Complete_ using the parameter input `-Mode`.

Please use the command `Get-Help <command>` to get info about a powershell command.



## Resources:
The fundamentals of this repo have been build with [this](https://learn.microsoft.com/en-us/training/paths/fundamentals-bicep/) learning path as a starting point