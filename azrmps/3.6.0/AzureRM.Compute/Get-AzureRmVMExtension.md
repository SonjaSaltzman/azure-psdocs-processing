---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version:
schema: 2.0.0
updated_at: 03/11/2017 15:03 PM
ms.date: 03/11/2017
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/marchrelease/azureps-cmdlets-docs/ResourceManager/AzureRM.Compute/v2.7.0/Get-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell/blob/marchrelease/azureps-cmdlets-docs/ResourceManager/AzureRM.Compute/v2.7.0/Get-AzureRmVMExtension.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/bc71000aa3c7f754b95442dcc415a7324626a15c
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
open_to_public_contributors: false
---

# Get-AzureRmVMExtension

## SYNOPSIS
Gets properties of Virtual Machine Extensions installed on a virtual machine.

## SYNTAX

```
Get-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureRmVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.
Specify the name of an extension for which to get properties.
To get only the instance view of an extension, specify the Status parameter.

## EXAMPLES

### Example 1: Get properties of an extension
```
PS C:\>Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"
```

This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.

### Example 2: Get instance view of an extension
```
PS C:\>Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status
```

This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.

## PARAMETERS

### -Name
Specifies the name of an extension.
This cmdlet gets properties for the extension that this parameter specifies.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifies the name of a resource group.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Status
Indicates that this cmdlet gets only the instance view of an extension.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Specifies the name of a virtual machine.
This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 2
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

[Remove-AzureRmVMExtension](./Remove-AzureRmVMExtension.md)

[Set-AzureRmVMExtension](./Set-AzureRmVMExtension.md)

