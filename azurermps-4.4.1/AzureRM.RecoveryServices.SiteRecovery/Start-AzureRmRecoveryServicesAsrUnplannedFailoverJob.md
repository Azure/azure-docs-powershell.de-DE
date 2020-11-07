---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: 0d619084f62f4cad9b5bd7a9295987681994e53e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663858"
---
# Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob

## Synopsis
Startet einen ungeplanten Failover-Vorgang.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ByRPIObject (Standard)
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByRPObject
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob** wird das ungeplante Failover eines geschützten Elements oder Wiederherstellungsplans für die Azure Site Recovery-Replikation gestartet.
Mithilfe des Get-AzureRmRecoveryServicesAsrJob-Cmdlets können Sie überprüfen, ob der Auftrag erfolgreich ist.

## Beispiele

### Beispiel 1
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

Startet den ungeplanten Failover-Vorgang für den angegebenen Wiederherstellungsplan unter Verwendung der angegebenen Parameter und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.

## Parameter

### -DataEncryptionPrimaryCertFile
Gibt die primäre Zertifikatsdatei an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataEncryptionSecondaryCertFile
Gibt die sekundäre Zertifikatsdatei an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Richtung
Gibt die Richtung des Failovers an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- PrimaryToRecovery
- RecoveryToPrimary

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PerformSourceSideAction
Gibt an, dass alle im Wiederherstellungsplan angegebenen Quellwebsite Vorgänge als Teil des Failovers ausgeführt werden müssen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: PerformSourceSideActions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryPlan
Gibt ein ASR-Wiederherstellungsplan Objekt an, das dem Wiederherstellungsplan entspricht, für den der Failovervorgang durchgeführt werden soll.

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ReplicationProtectedItem
Gibt das Objekt der ASR-Replikations geschützten Elemente an, das dem Replikations geschützten Element entspricht, für das der Failovervorgang durchgeführt werden soll.

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan
Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem

## Ausgaben

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob

## Notizen

## Verwandte Links

[Get-AzureRmRecoveryServicesAsrJob](./Get-AzureRmRecoveryServicesAsrJob.md)


