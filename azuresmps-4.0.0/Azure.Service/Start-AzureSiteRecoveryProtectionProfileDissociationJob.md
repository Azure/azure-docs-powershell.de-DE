---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 185506BC-6155-4517-BCBD-BCDE7450C7A8
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8017c2947a8d046226a63b5ed07b3714c35b22c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006616"
---
# Start-AzureSiteRecoveryProtectionProfileDissociationJob

## Synopsis
Startet einen Dissoziation-Auftrag für eine Replikationsrichtlinie, die einem Schutzcontainer für die Standortwiederherstellung zugeordnet ist.

## Syntax

### EnterpriseToAzure (Standard)
```
Start-AzureSiteRecoveryProtectionProfileDissociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### EnterpriseToEnterprise
```
Start-AzureSiteRecoveryProtectionProfileDissociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Start-AzureSiteRecoveryProtectionProfileDissociationJob** initiiert einen Dissoziation-Auftrag in der Replikationsrichtlinie, die einem Azure Site Recovery Protection-Container zugeordnet ist.

## Beispiele

### Beispiel 1: Trennen eines Schutz Profils
```
PS C:\> $ProtectionContainer01 = Get-AzureSiteRecoveryProtectionContainer -Id "5ba2ea95-856d-4033-9ca3-91e3e2c080b9"
PS C:\> $ProtectionContainer02 = Get-AzureSiteRecoveryProtectionContainer -Id "cf011f2a-aa19-443c-9f60-357f6b8afb77"
PS C:\> Start-AzureSiteRecoveryProtectionProfileDissociationJob -PrimaryProtectionContainer $ProtectionContainer01 -ProtectionProfile $ProtectionContainer01.AvailableProtectionProfiles[0] -RecoveryProtectionContainer $ProtectionContainer02
Name             : MyProtectionProfile
ID               : 51978b0f-9241-4153-9171-2e19344f0805
ClientRequestId  : bb6f3200-b7c6-4c6f-bcbc-a70bb9946f03-2015-01-30 02:55:55Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : 
Tasks            : {}
Errors           : {}
```

Der erste Befehl ruft einen Schutzcontainer mit dem Cmdlet **Get-AzureSiteRecoveryProtectionContainer** ab und speichert diesen Container dann in der Variablen $ProtectionContainer 01.

Der zweite Befehl ruft einen Schutzcontainer ab und speichert ihn dann in der Variablen $ProtectionContainer 02.

Der endgültige Befehl distanziert sich vom Schutzprofil des in $ProtectionContainer 01 gespeicherten Containers als primärer Schutzcontainer.
Der Befehl distanziert den in $ProtectionContainer 02 gespeicherten Container als Wiederherstellungs Schutzcontainer.

## Parameter

### -PrimaryProtectionContainer
Gibt einen primären Schutzcontainer an.

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
Gibt die Schutzprofil Einstellungen an, mit denen die Zuordnung zu den Schutz Containern aufgehoben werden soll.
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
Gibt einen Wiederherstellungs Schutzcontainer an.

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

[Anfang-AzureSiteRecoveryProtectionProfileAssociationJob](./Start-AzureSiteRecoveryProtectionProfileAssociationJob.md)


