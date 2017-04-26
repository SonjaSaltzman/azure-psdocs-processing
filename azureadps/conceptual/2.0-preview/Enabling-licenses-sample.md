---
content_git_url: https://github.com/Azure/azure-docs-powershell-azuread/blob/master/Azure%20AD%20Cmdlets/docs-conceptual/Enabling-licenses-sample.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-azuread/blob/master/Azure%20AD%20Cmdlets/docs-conceptual/Enabling-licenses-sample.md
gitcommit: https://github.com/Azure/azure-docs-powershell-azuread/blob/4e89d3f85116c4fe05240aba6cdb46e2191b130e
---
# Assigning licenses to a user

This example shows how to assign a license to a user. 

```powershell
#The user that will get a license
$UserToLicense = Get-AzureADUser -ObjectId "<UPN of the user for which you want to assign a license>"
 
#Define the plans that will be enabled (Exchange Online, Skype for Business and Office 365 ProPlus )
$EnabledPlans = 'O365_BUSINESS_PREMIUM'
#Get the LicenseSKU and create the Disabled ServicePlans object
$LicenseSku = Get-AzureADSubscribedSku | Where-Object {$_.SkuPartNumber -eq 'O365_BUSINESS_PREMIUM'} 
#Loop through all the individual plans and disable all plans except the one in $EnabledPlans
$DisabledPlans = $LicenseSku.ServicePlans | ForEach-Object -Process { 
  $_ | Where-Object -FilterScript {$_.ServicePlanName -notin $EnabledPlans }
}
 
#Create the AssignedLicense object with the License and DisabledPlans earlier created
$License = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicense
$License.SkuId = $LicenseSku.SkuId
$License.DisabledPlans = $DisabledPlans.ServicePlanId
 
#Create the AssignedLicenses Object 
$AssignedLicenses = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicenses
$AssignedLicenses.AddLicenses = $License
$AssignedLicenses.RemoveLicenses = @()

#Assign the license to the user
Set-AzureADUserLicense -ObjectId $UserToLicense.ObjectId -AssignedLicenses $AssignedLicenses

```