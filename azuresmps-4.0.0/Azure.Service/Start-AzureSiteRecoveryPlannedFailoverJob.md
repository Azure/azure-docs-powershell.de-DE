---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2575F5C4-A276-49CE-AB0C-726F359DA6F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7f71138e47c851097fe36ca294784fc571b6369f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005957"
---
# Start-AzureSiteRecoveryPlannedFailoverJob

## Synopsis
Startet einen geplanten Failover-Vorgang für eine Websitewiederherstellung.

## Syntax

### ByRPId (Standard)
```
Start-AzureSiteRecoveryPlannedFailoverJob -RPId <String> -Direction <String> [-WaitForCompletion]
 [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByPEId
```
Start-AzureSiteRecoveryPlannedFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByRPObject
```
Start-AzureSiteRecoveryPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByPEObject
```
Start-AzureSiteRecoveryPlannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Start-AzureSiteRecoveryPlannedFailoverJob** startet ein Geplantes Failover für eine Azure Site Recovery Protection-Entität oder einen Wiederherstellungsplan.
Mit dem Cmdlet **Get-AzureSiteRecoveryJob** können Sie überprüfen, ob der Auftrag erfolgreich ist.

## Beispiele

### Beispiel 1: Starten eines geplanten Failover-Auftrags
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
PS C:\> Start-AzureSiteRecoveryPlannedFailoverJob -Direction PrimaryToRecovery -ProtectionEntity $Protected -Optimize ForDowntime
ID               : c38eecdc-731c-405b-a61c-08db99aae2fe
ClientRequestId  : 32ace403-0916-4967-83a1-529176bd6e88-2014-49-06 15:49:24Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : {}
Name             : 
Tasks            : {}
Errors           : {}
```

Der erste Befehl ruft alle geschützten Container im aktuellen Azure Site Recovery Vault mit dem Cmdlet **Get-AzureSiteRecoveryProtectionContainer** ab und speichert die Ergebnisse dann in der $Container Variablen.
In diesem Beispiel ist ein einzelner Container vorhanden.

Der zweite Befehl ruft die geschützten virtuellen Computer ab, die zu dem in $Container gespeicherten Container gehören, indem Sie das Cmdlet " **Get-AzureSiteRecoveryProtectionEntity** " verwenden.
Der Befehl speichert die Ergebnisse in der $protected-Variablen.

Der endgültige Befehl startet den Failover-Auftrag in Richtung PrimaryToRecovery für die geschützten virtuellen Computer, die in $Protected gespeichert sind.

## Parameter

### -Richtung
Gibt die Richtung des Failovers an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- PrimaryToRecovery
- RecoveryToPrimary

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Optimieren
Gibt an, was optimiert werden soll.
Dieser Parameter gilt für Failover von einer Azure-Website zu einer lokalen Website, für die eine signifikante Datensynchronisierung erforderlich ist.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- ForDowntime
- ForSynchronization

Wenn **ForDowntime** angegeben wird, bedeutet dies, dass Daten vor dem Failover synchronisiert werden, um die Ausfallzeit zu minimieren.
Die Synchronisierung wird ausgeführt, ohne den virtuellen Computer herunterzufahren.
Nach Abschluss der Synchronisierung wird der Auftrag angehalten.
Setzen Sie den Auftrag fort, um einen zusätzlichen Synchronisierungsvorgang auszuführen, der den virtuellen Computer herunterfährt.

Wenn **ForSynchronization** angegeben wird, bedeutet dies, dass Daten während des Failovers nur synchronisiert werden, damit die Datensynchronisierung minimiert wird.
Da diese Einstellung aktiviert ist, wird der virtuelle Computer sofort heruntergefahren.
Die Synchronisierung beginnt nach dem Herunterfahren, um den Failovervorgang abzuschließen.

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

### -ProtectionContainerId
Gibt die ID des geschützten Containers an, für den der Auftrag gestartet werden soll.

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectionEntity
Gibt das Entitätsobjekt für den Standort Wiederherstellungs Schutz an.

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ProtectionEntityId
Gibt ein **ASRProtectionEntity** -Objekt an, für das der Auftrag gestartet werden soll.
Verwenden Sie das Cmdlet **Get-AzureSiteRecoveryProtectionEntity** , um ein **ASRProtectionEntity** -Objekt abzurufen.

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryPlan
Gibt ein Wiederherstellungsplan-Objekt an.

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

### -RPId
Gibt die ID eines Wiederherstellungsplans an, für den der Auftrag gestartet werden soll.

```yaml
Type: String
Parameter Sets: ByRPId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitForCompletion
Gibt an, dass das Cmdlet wartet, bis der Vorgang abgeschlossen ist, bevor es die Steuerung an die Windows PowerShell-Konsole zurückgibt.

```yaml
Type: SwitchParameter
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

[Get-AzureSiteRecoveryProtectionContainer](./Get-AzureSiteRecoveryProtectionContainer.md)

[Get-AzureSiteRecoveryProtectionEntity](./Get-AzureSiteRecoveryProtectionEntity.md)


