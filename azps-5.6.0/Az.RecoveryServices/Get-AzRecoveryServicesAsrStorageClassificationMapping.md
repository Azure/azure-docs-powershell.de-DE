---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: c5dea86066fd2b7bc6bd3b2bd3eb7ac94f401895
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924520"
---
# Get-AzRecoveryServicesAsrStorageClassificationMapping

## SYNOPSIS
Ruft ASR-Speicherklassifizierungszuordnungen ab.

## SYNTAX

### ByObject (Standard)
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObjectWithName
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Get-AzRecoveryServicesAsrStorageClassificationMapping-Cmdlet** ruft die Details einer ASR-Speicherklassifizierungszuordnung ab.

## BEISPIELE

### Beispiel 1
```
PS C:\> $StorageClassificationMappings = Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

Listen Sie alle Speicherklassifizierungszuordnungen auf, die der angegebenen Speicherklassifizierung entspricht.

## PARAMETER

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
Gibt den Namen der zu erhaltenden Speicherklassifizierungszuordnung an.

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageClassification
Gibt ein ASR-Speicherklassifizierungsobjekt an. Das Cmdlet ruft ASR-Speicherklassifizierungszuordnungen ab, die der angegebenen Speicherklassifizierung entsprechend sind. 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification

## AUSGABEN

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping

## NOTIZEN

## VERWANDTE LINKS

[New-AzRecoveryServicesAsrStorageClassificationMapping](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)

[Remove-AzRecoveryServicesAsrStorageClassificationMapping](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
