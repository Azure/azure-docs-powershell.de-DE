---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 8FF1362B-C7AB-4769-A88B-D1B6E214A006
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf8275b8dfec4263c5ab7a8022dcb65edccb1171
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006613"
---
# Stop-AzureSiteRecoveryJob

## Synopsis
Beendet einen Wiederherstellungsauftrag für die Website.

## Syntax

### ByObject (Standard)
```
Stop-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ById
```
Stop-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Stop-AzureSiteRecoveryJob** " beendet einen Azure Site Recovery-Auftrag.

## Beispiele

### Beispiel 1: Beenden aller Aufträge
```
PS C:\>$Jobs = Get-AzureSiteRecoveryJob 
PS C:\> Stop-AzureSiteRecoveryJob -Job $Jobs
```

Der erste Befehl ruft die Azure Site Recovery-Aufträge für das aktuelle Azure Site Recovery Vault mit dem Cmdlet **Get-AzureSiteRecoveryJob** ab und speichert die Ergebnisse dann in der $Jobs-Variablen.

Mit dem zweiten Befehl werden die von $Jobs angegebenen Aufträge angehalten.

## Parameter

### -ID
Gibt die ID des Auftrags an, der beendet werden soll.

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Job
Gibt den Auftrag an, der beendet werden soll.

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest.
Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureSiteRecoveryJob](./Get-AzureSiteRecoveryJob.md)

[Neustart-AzureSiteRecoveryJob](./Restart-AzureSiteRecoveryJob.md)

[Lebenslauf-AzureSiteRecoveryJob](./Resume-AzureSiteRecoveryJob.md)


