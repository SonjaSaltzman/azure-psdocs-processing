---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
ms.assetid: 22B63259-799B-4F25-A06B-7A818D295870
online version:
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Reset-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Reset-AzureRmServerManagementGatewayProfile.md
gitcommit: https://github.com/Azure/azure-powershell/blob/8810c0614b76be8d014616888a4ae7733a452af9
updated_at: 05/12/2017 03:05 AM
ms.date: 05/12/2017
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: erickson-doug
open_to_public_contributors: true
ms.service: server-management
---

# Reset-AzureRmServerManagementGatewayProfile

## SYNOPSIS
Resets the profile of a Server Management gateway.

## SYNTAX

### ByName
```
Reset-AzureRmServerManagementGatewayProfile [-ResourceGroupName] <String> [-GatewayName] <String>
 [<CommonParameters>]
```

### ByObject
```
Reset-AzureRmServerManagementGatewayProfile [-Gateway] <Gateway> [<CommonParameters>]
```

## DESCRIPTION
The **Reset-AzureRmServerManagementGatewayProfile** cmdlet resets the profile for an Azure Server Management Gateway.

You will need to use the Save-AzureRmServerManagementGatewayProfile cmdlet to download the profile and then the Install-AzureRmServerManagementGatewayProfile cmdlet to save it after you reset the profile.

## EXAMPLES

### 1:
```

```

## PARAMETERS

### -Gateway
Specifies the gateway for which the cmdlet resets the profile for.

May be specified instead of ResourceGoupName and GatewayName

```yaml
Type: Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -GatewayName
Specifies the name of the gateway for which the cmdlet resets the profile.

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifies the name of the resource group that the gateway belongs to.

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Install-AzureRmServerManagementGatewayProfile](./Install-AzureRmServerManagementGatewayProfile.md)

[Save-AzureRmServerManagementGatewayProfile](./Save-AzureRmServerManagementGatewayProfile.md)


