---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
online version:
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
gitcommit: https://github.com/Azure/azure-powershell/blob/41f4a7b63c9651a305b985d28fcd40e60968957c
updated_at: 05/10/2017 19:05 PM
ms.date: 05/10/2017
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: erickson-doug
open_to_public_contributors: true
---

# Test-AzureRmContainerRegistryNameAvailability

## SYNOPSIS
Checks the availability of a container registry name.

## SYNTAX

```
Test-AzureRmContainerRegistryNameAvailability [-Name] <String> [<CommonParameters>]
```

## DESCRIPTION
The **Test-AzureRmContainerRegistryNameAvailability** cmdlet checks whether a container registry name is valid and available to use.

## EXAMPLES

### Example 1: Check the availability of a container registry name
```
PS C:\>Test-AzureRmContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

This command checks the availability of the container registry name `SomeRegistryName`.

## PARAMETERS

### -Name
Container Registry Name.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

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

### Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus

## NOTES

## RELATED LINKS

[New-AzureRmContainerRegistry](./New-AzureRmContainerRegistry.md)
