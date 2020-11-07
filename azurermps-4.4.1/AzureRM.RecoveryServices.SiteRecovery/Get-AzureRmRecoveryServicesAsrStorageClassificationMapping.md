---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 5b15fdea68cc57d6f389fe43e81fb3f710736953
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663865"
---
# Get-AzureRmRecoveryServicesAsrStorageClassificationMapping

## Synopsis
Ruft ASR-Speicher Klassifikations Zuordnungen ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ByObject (Standard)
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [<CommonParameters>]
```

### ByObjectWithName
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmRecoveryServicesAsrStorageClassificationMapping** " Ruft die Details einer ASR-Speicher Klassifikations Zuordnung ab.

## Beispiele

### Beispiel 1
```
PS C:\> $StorageClassificationMappings = Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

Listet alle Speicher Klassifikations Zuordnungen auf, die der angegebenen speicherklassifizierung entsprechen.

## Parameter

### -Name
Gibt den Namen der abzurufenden Speicher Klassifikations Zuordnung an.

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageClassification
Gibt ein ASR-Speicher Klassifikations Objekt an. Das Cmdlet ruft ASR-Speicher Klassifikations Zuordnungen ab, die der angegebenen speicherklassifizierung entsprechen. 

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]

## Notizen

## Verwandte Links

[Neu – AzureRmRecoveryServicesAsrStorageClassificationMapping](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
