---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 1d6199042cec106d81ba91ccb7ccb854741d319d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663866"
---
# Get-AzureRmRecoveryServicesAsrServicesProvider

## Synopsis
Ruft die Details der ASR-Wiederherstellungsdienste-Anbieter ab, die für den Recovery Services Vault registriert sind.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Standard (Standard)
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [<CommonParameters>]
```

### ByName
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric> [<CommonParameters>]
```

### ByFriendlyName
```
Get-AzureRmRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric> [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmRecoveryServicesAsrServicesProvider** " Ruft Informationen zu den Azure Site Recovery-Anbietern im Tresor ab.

## Beispiele

### Beispiel 1
```
PS C:\> $RSPs = Get-AzureRmRecoveryServicesAsrFabric | Get-AzureRmRecoveryServicesAsrServicesProvider
```

Auflisten aller für den Wiederherstellungsdienste-Tresor registrierten ASR-Replikationsdienst Anbieter, die dem angegebenen Fabric entsprechen.

## Parameter

### -Stoff
Gibt das ASR-Fabric-Objekt an.

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -FriendlyName
Gibt den Anzeigenamen des Dienstanbieters für ASR-Wiederherstellungsdienste an, für den Details abgerufen werden sollen.

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen des Dienstanbieters für ASR-Wiederherstellungsdienste an, für den Details abgerufen werden sollen.

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric

## Ausgaben

### System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]

## Notizen

## Verwandte Links

[Remove-AzureRmRecoveryServicesAsrServicesProvider](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)

[Update-AzureRmRecoveryServicesAsrServicesProvider](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)
