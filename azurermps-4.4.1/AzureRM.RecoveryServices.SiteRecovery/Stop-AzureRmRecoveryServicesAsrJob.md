---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: e639e6fc42e440b5088a34ee29e21d324ed7d235
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663856"
---
# Stop-AzureRmRecoveryServicesAsrJob

## Synopsis
Beendet einen Azure Site Recovery-Auftrag.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ByObject (Standard)
```
Stop-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Stop-AzureRmRecoveryServicesAsrJob -Name <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Stop-AzureRmRecoveryServicesAsrJob** beendet den angegebenen Azure Site Recovery-Auftrag.

## Beispiele

### Beispiel 1
```
PS C:\> $currentJob = Stop-AzureRmRecoveryServicesAsrJob -Job $Job
```

Versucht, den angegebenen Auftrag zu beenden und gibt ein aktualisiertes ASR-Auftragsobjekt zurück.

## Parameter

### -Inputobject
Eingabeobjekt: Geben Sie das ASR-Auftragsobjekt an, das dem zu beendenden ASR-Auftrag entspricht.

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: Job

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Geben Sie den ASR-Auftrag an, der vom ASR-Auftragsnamen angehalten werden soll.

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

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob

## Ausgaben

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob

## Notizen

## Verwandte Links

[Get-AzureRmRecoveryServicesAsrJob](./Get-AzureRmRecoveryServicesAsrJob.md)

[Neustart-AzureRmRecoveryServicesAsrJob](./Restart-AzureRmRecoveryServicesAsrJob.md)

[Lebenslauf-AzureRmRecoveryServicesAsrJob](./Resume-AzureRmRecoveryServicesAsrJob.md)
