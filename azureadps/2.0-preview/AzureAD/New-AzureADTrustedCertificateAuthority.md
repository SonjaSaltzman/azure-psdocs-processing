---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.Custom.dll-Help.xml
ms.assetid: C19B638B-9511-4828-B5AD-D177ECF9D5C0
online version:
schema: 2.0.0
updated_at: 04/25/2017 20:04 PM
ms.date: 04/25/2017
content_git_url: https://github.com/Azure/azure-docs-powershell-azuread/blob/master/Azure%20AD%20Cmdlets/AzureAD/v2preview/New-AzureADTrustedCertificateAuthority.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-azuread/blob/master/Azure%20AD%20Cmdlets/AzureAD/v2preview/New-AzureADTrustedCertificateAuthority.md
gitcommit: https://github.com/Azure/azure-docs-powershell-azuread/blob/c5cc449ee6e2b805fc85a9e05130b06b10899f67
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: carolz
ms.service: active-directory
---

# New-AzureADTrustedCertificateAuthority

## SYNOPSIS
Creates a trusted certificate authority.

## SYNTAX

```
New-AzureADTrustedCertificateAuthority -CertificateAuthorityInformation <CertificateAuthorityInformation>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The **New-AzureADTrustedCertificateAuthority** cmdlet creates a trusted certificate authority in Azure Active Directory (AD).

## EXAMPLES

## PARAMETERS

### -CertificateAuthorityInformation
```yaml
Type: CertificateAuthorityInformation
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -InformationAction
Specifies how this cmdlet responds to an information event. The acceptable values for this parameter are:

- Continue
- Ignore
- Inquire
- SilentlyContinue
- Stop
- Suspend

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Specifies an information variable.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADTrustedCertificateAuthority](./Get-AzureADTrustedCertificateAuthority.md)

[Remove-AzureADTrustedCertificateAuthority](./Remove-AzureADTrustedCertificateAuthority.md)

[Set-AzureADTrustedCertificateAuthority](./Set-AzureADTrustedCertificateAuthority.md)


