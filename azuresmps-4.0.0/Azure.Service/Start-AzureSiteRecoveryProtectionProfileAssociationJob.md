---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: CB5E1419-C4C7-4524-ACCC-13C9D9CCA621
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4955bfa121d6742903dd2ca99721186c7c860004
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006054"
---
# Start-AzureSiteRecoveryProtectionProfileAssociationJob

## Synopsis
Startet einen Standort Wiederherstellungs-Replikationsrichtlinien Zuordnungs Auftrag.

## Syntax

### EnterpriseToAzure (Standard)
```
Start-AzureSiteRecoveryProtectionProfileAssociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### EnterpriseToEnterprise
```
Start-AzureSiteRecoveryProtectionProfileAssociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Start-AzureSiteRecoveryProtectionProfileAssociationJob** initiiert einen Zuordnungs Auftrag, um eine Replikationsrichtlinie einem Azure Site Recovery Protection-Container zuzuordnen.

## Beispiele

### Beispiel 1: Zuweisen eines Schutz Profils
```
PS C:\> $ProtectionContainer01 = Get-AzureSiteRecoveryProtectionContainer -Id "5ba2ea95-856d-4033-9ca3-91e3e2c080b9"
PS C:\> $ProtectionProfile = New-AzureSiteRecoveryProtectionProfileObject -ReplicationProvider "HyperVReplica" -AllowReplicaDeletion -ApplicationConsistentSnapshotFrequencyInHours 1 -CompressionEnabled -RecoveryPoints 2 -ReplicationFrequencyInSeconds 30 -ReplicationMethod "Online" -ReplicationPort 8085 -ReplicationStartTime 1
PS C:\> $ProtectionContainer02 = Get-AzureSiteRecoveryProtectionContainer -Id "cf011f2a-aa19-443c-9f60-357f6b8afb77"
PS C:\> Start-AzureSiteRecoveryProtectionProfileAssociationJob -PrimaryProtectionContainer $ProtectionContainer01 -ProtectionProfile $ProtectionProfile -RecoveryProtectionContainer $ProtectionContainer02
Name             : MyProtectionProfile
ID               : 51978b0f-9241-4153-9171-2e19344f0805
ClientRequestId  : bb6f3200-b7c6-4c6f-bcbc-a70bb9946f03-2015-01-27 22:55:55Z-P
State            : InProgress
StateDescription : InProgress
StartTime        : 1/27/2015 10:56:01 PM
EndTime          : 
AllowedActions   : 
Tasks            : {Adding the protection group, Configuring Windows Server 2012 R2 Hyper-V hosts for Azure}
Errors           : {}
```

Der erste Befehl ruft einen Schutzcontainer mit dem Cmdlet **Get-AzureSiteRecoveryProtectionContainer** ab und speichert diesen Container dann in der Variablen $ProtectionContainer 01.

Der zweite Befehl erstellt ein Schutzprofil mithilfe des Cmdlets **New-AzureSiteRecoveryProtectionProfileObject** und speichert dieses Schutzprofil in der $ProtectionProfile Variablen.

Der dritte Befehl ruft einen Schutzcontainer ab und speichert ihn dann in der Variablen $ProtectionContainer 02.

Der endgültige Befehl ordnet das in $ProtectionProfile gespeicherte Schutzprofil dem Container zu, der in $ProtectionContainer 01 als primärer Schutzcontainer gespeichert ist.
Der Befehl ordnet den in $ProtectionContainer 02 gespeicherten Container als Wiederherstellungs Schutzcontainer zu.

## Parameter

### -PrimaryProtectionContainer
Gibt den primären Schutzcontainer an, auf dem die Schutzprofil Einstellungen angewendet werden sollen.

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
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

### -ProtectionProfile
Gibt die Schutzprofil Einstellungen an, die auf die Schutzcontainer angewendet werden sollen.
Verwenden Sie das New-AzureSiteRecoveryProtectionProfileObject-Cmdlet, um ein **ASRProtectionProfile** -Objekt zu erhalten.

```yaml
Type: ASRProtectionProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RecoveryProtectionContainer
Gibt den Wiederherstellungs Schutzcontainer an, auf dem die Schutzprofil Einstellungen angewendet werden sollen.

```yaml
Type: ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
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

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureSiteRecoveryProtectionContainer](./Get-AzureSiteRecoveryProtectionContainer.md)

[Neu – AzureSiteRecoveryProtectionProfileObject](./New-AzureSiteRecoveryProtectionProfileObject.md)

[Anfang-AzureSiteRecoveryProtectionProfileDissociationJob](./Start-AzureSiteRecoveryProtectionProfileDissociationJob.md)


