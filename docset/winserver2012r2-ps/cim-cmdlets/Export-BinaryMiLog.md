---
external help file: Microsoft.Management.Infrastructure.CimCmdlets.dll-Help.xml
Module Name: CimCmdlets
online version: 
schema: 2.0.0
title: Export-BinaryMiLog
description: 
keywords: powershell, cmdlet
author: brianlic
manager: alanth
ms.date: 2017-10-29
ms.topic: reference
ms.prod: powershell
ms.technology: powershell
ms.assetid: 0812F28F-D7B4-4325-A84E-2F274CD4D3E1
---

# Export-BinaryMiLog

## SYNOPSIS
Creates a binary encoded representation of an object or objects and stores it in a file.

## SYNTAX

```
Export-BinaryMiLog [-InputObject <CimInstance>] [-Path] <String> [<CommonParameters>]
```

## DESCRIPTION
The **Export-BinaryMILog** cmdlet creates an binary-based representation of an object or objects and stores it in a file.
You can then use the Import-BinaryMILog cmdlet to re-create the saved object based on the contents of that file.

This cmdlet is similar to Import-CliXML, except that Export-BinaryMILog stores the resulting object in a binary encoded file.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
PS C:\> Get-CimInstance Win32_Process | Export-BinaryMiLog -Path Processes.bmil
```

Description

-----------

This example exports CimInstances to a binary MI log file specified by the -Path parameter.
See the example for Import-BinaryMILog to see how to recreate the CimInstances by importing this file.

## PARAMETERS

### -InputObject
Specifies the input to this cmdlet.
You can use this parameter, or you can pipe the input to this cmdlet.

```yaml
Type: CimInstance
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Path
Specifies the path to the file where the binary representation of the object will be stored.

The Path parameter supports wild cards and relative paths. 
The cmdlet generates an error if the path resolves to more than one file.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
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

[Import-BinaryMILog](./Import-BinaryMiLog.md)

