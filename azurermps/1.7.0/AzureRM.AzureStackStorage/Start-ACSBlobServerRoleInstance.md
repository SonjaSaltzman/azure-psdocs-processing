---
external help file: Microsoft.AzureStack.Commands.StorageAdmin.dll-Help.xml
ms.assetid: 500963CA-7D06-432D-BFFD-906000DAE19A
online version:
schema: 2.0.0
updated_at: 05/01/2017 21:05 PM
ms.date: 05/01/2017
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.AzureStackStorage/v0.9.9.1/Start-ACSBlobServerRoleInstance.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.AzureStackStorage/v0.9.9.1/Start-ACSBlobServerRoleInstance.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/0589fbf53d27e39e0cf445261d29c64fb0859d62
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: erickson-doug
open_to_public_contributors: true
ms.service: azure-stack
---

# Start-ACSBlobServerRoleInstance

## SYNOPSIS
Starts the ACS blob service instance on a specific physical node.

## SYNTAX

```
Start-ACSBlobServerRoleInstance [-FarmName] <String> [-InstanceId] <String> [[-SubscriptionId] <String>]
 [[-Token] <String>] [[-AdminUri] <Uri>] [-ResourceGroupName] <String> [-SkipCertificateValidation] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Start-ACSBlobServerRoleInstance** cmdlet starts the Azure Consistent Storage (ACS) blob service instance on a specific physical node.

## EXAMPLES

### Example 1: Start the ACS blob service instance on a specific physical node
```
PS C:\>$Global:AdminUri = "https://srp.yourdomainFQDN:30020"
PS C:\> $SubscriptId = "SubID"
PS C:\> $Token = "Token"
PS C:\> $ResourceGroup = "System" 
PS C:\> $Farm = Get-ACSFarm -SubscriptionId $SubscriptId -Token $Token -AdminUri $AdminUri -SkipCertificateValidation -ResourceGroupName $ResourceGroup
PS C:\> Start-ACSBlobServerRoleInstance -SubscriptionId $SubscriptId -Token $Token -AdminUri $AdminUri -ResourceGroupName $ResourceGroup -SkipCertificateValidation -FarmName $Farm.Name -InstanceId "0123456789"
```

The first command gets the specified ACS Farm and stores the result in the variable named $Farm.
The final command starts the ACS blob service instance on the physical node named 0123456789.

## PARAMETERS

### -AdminUri
Specifies the location of the Resource Manager endpoint.
If you configured your environment by using the Set-AzureRMEnvironment cmdlet, you do not have to specify this parameter.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FarmName
Specifies the name of the ACS farm.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InstanceId
Specifies the instance ID of a specific role instance.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifies the name of the resource group for which this cmdlet gets the ACS farm.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkipCertificateValidation
Indicates that this cmdlet skips certificate validation.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Specifies the service administrator subscription ID.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Token
Specifies the service administrator token.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.AzureStack.Commands.StorageAdmin.FarmResponse,Microsoft.AzureStack.Commands.StorageAdmin.AccountContainerRoleInstanceResponse,
Output from Get-ACSFarm and Get-ACSRoleInstance can be piped to this cmdlet's input.

## OUTPUTS

## NOTES

## RELATED LINKS

[Stop-ACSBlobServerRoleInstance](./Stop-ACSBlobServerRoleInstance.md)

[Get-ACSRoleInstance](./Get-ACSRoleInstance.md)

[Get-ACSFarm](./Get-ACSFarm.md)


