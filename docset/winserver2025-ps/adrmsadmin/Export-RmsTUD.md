---
description: Use this topic to help manage Windows and Windows Server technologies with Windows PowerShell.
external help file: Microsoft.RightsManagementServices.Admin.dll-Help.xml
Module Name: ADRMSAdmin
ms.date: 12/20/2016
online version: https://learn.microsoft.com/powershell/module/adrmsadmin/export-rmstud?view=windowsserver2025-ps&wt.mc_id=ps-gethelp
schema: 2.0.0
title: Export-RmsTUD
---

# Export-RmsTUD

## SYNOPSIS
Exports a TUD.

## SYNTAX

```
Export-RmsTUD [-SavedFile] <String[]> [-Force] [-Path] <String[]> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Export-RmsTUD** cmdlet exports the internal enterprise trusted user domain (TUD) in Active Directory Rights Management Services (AD RMS) to a file.

To perform the export, set the *SavedFilePath* parameter to the export file path, and then set the *Path* parameter to the AD RMS provider subpath `<PSDrive>:\TrustPolicy\TrustedUserDomain\<TUD_ID>` where `<PSDrive>` is the provider drive ID and `<TUD_ID>` is the ID of the internal TUD.

## EXAMPLES

### Example 1: Export a TUD by ID
```
PS C:\> Export-RmsTuD -Path ".\100" -SavedFile "c:\temp\test.xml"
```

This command exports the TUD with the ID of 100 to the file c:\temp\test.xml.

## PARAMETERS

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

### -Force
Overrides restrictions that prevent the command from succeeding if the restrictions do not compromise security.
For example, *Force* overrides the read-only attribute or creates directories to complete a file path, but it does not attempt to change file permissions.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Path
Specifies a provider drive and path or relative path on the current drive.
Use a dot (.) to specify the current location.
This parameter does not accept wildcards and has no default value.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SavedFile
Specifies the full path and filename of the file that receives the exported content.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Using Windows PowerShell with AD RMS](https://go.microsoft.com/fwlink/?LinkId=136806)

[Export-RmsTPD](./Export-RmsTPD.md)

[Import-RmsTPD](./Import-RmsTPD.md)

[Import-RmsTUD](./Import-RmsTUD.md)

