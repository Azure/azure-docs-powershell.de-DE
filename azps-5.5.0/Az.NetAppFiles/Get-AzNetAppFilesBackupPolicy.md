---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 754149172b3154975580a0802426f9a2f20c0f62
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154508"
---
# Get-AzNetAppFilesBackupPolicy

## SYNOPSIS
Ruft Details zu einer Azure NetApp Files (ANF)-Sicherungsrichtlinie ab.

## SYNTAX

### ByFieldsParameterSet (Standard)
```
Get-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByResourceIdParameterSet
```
Get-AzNetAppFilesBackupPolicy [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByParentObjectParameterSet
```
Get-AzNetAppFilesBackupPolicy [-Name <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzNetAppFilesBackupPolicy"** ruft Details einer ANF-Sicherungsrichtlinie ab.

## BEISPIELE

### Beispiel 1
```powershell
PS C:\> Get-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyBackupPolicy"
```

Dieser Befehl ruft die Sicherungsrichtlinie mit dem Namen "MyBackupPolicy" für das Konto "MyAnfAccount" ab.

## PARAMETERS

### -AccountName
Der Name des ANF-Kontos

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AccountObject
Das Kontoobjekt mit der zurückzukehrenden Sicherungsrichtlinie

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Der Name der ANF-Sicherungsrichtlinie

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupPolicyName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Die Ressourcengruppe des ANF-Kontos

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Die Ressourcen-ID der ANF-Sicherungsrichtlinie

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

### Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount

## AUSGABEN

### Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
