---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
ms.assetid: 78CD47B3-1953-4DE5-A255-A1E408C87929
online version:
schema: 2.0.0
updated_at: 05/01/2017 21:05 PM
ms.date: 05/01/2017
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.DataLakeStore/v2.1.0/Remove-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.DataLakeStore/v2.1.0/Remove-AzureRmDataLakeStoreItemAclEntry.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/0589fbf53d27e39e0cf445261d29c64fb0859d62
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: erickson-doug
open_to_public_contributors: true
ms.service: data-lake-store
---

# Remove-AzureRmDataLakeStoreItemAclEntry

## SYNOPSIS
Removes an entry from the ACL of a file or folder in Data Lake Store.

## SYNTAX

### Remove ACL Entries using ACL object (Default)
```
Remove-AzureRmDataLakeStoreItemAclEntry -Account <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAcl> [-Force] [<CommonParameters>]
```

### Remove specific ACE
```
Remove-AzureRmDataLakeStoreItemAclEntry -Account <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Default] [-Force] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-AzureRmDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.

## EXAMPLES

### Example 1: Remove a user entry
```
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

This command removes the user ACE for Patti Fuller from the ContosoADL account.

## PARAMETERS

### -AceType
Specifies the type of ACE to remove.
The acceptable values for this parameter are:

- User
- Group
- Mask
- Other

```yaml
Type: AceType
Parameter Sets: Remove specific ACE
Aliases: 
Accepted values: User, Group, Mask, Other

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Acl
Specifies the ACL object that contains the entries to be removed.

```yaml
Type: DataLakeStoreItemAcl
Parameter Sets: Remove ACL Entries using ACL object
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Default
Indicates that this operation removes the default ACE from the specified ACL.

```yaml
Type: SwitchParameter
Parameter Sets: Remove specific ACE
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Forces the command to run without asking for user confirmation.```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Id
Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.

```yaml
Type: Guid
Parameter Sets: Remove specific ACE
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Account
Specifies the name of the Data Lake Store account.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
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

[Set-AzureRmDataLakeStoreItemAclEntry](./Set-AzureRmDataLakeStoreItemAclEntry.md)


