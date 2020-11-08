---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 16146A0D-4605-489A-8259-A37BEAC98306
online version: ''
schema: 2.0.0
ms.openlocfilehash: 664c9af9373120f293153a1bbdc65d1a82637631
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006221"
---
# Update-AzureSiteRecoveryProtectionEntity

## Synopsis
Aktualisiert die Eigenschaften einer Schutz Entität in Azure Site Recovery.

## Syntax

```
Update-AzureSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Update-AzureSiteRecoveryProtectionEntity** aktualisiert die Eigenschaften einer Schutz Entität in Azure Site Recovery, wie etwa Besitzerinformationen des virtuellen Computers.
Dieses Cmdlet wird nur für Virtual Machine Monitor (VMM) für VMM-geschützte Schutz Entitäten unterstützt.

## Beispiele

### Beispiel 1: Aktualisieren einer Schutz Entität
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container
PS C:\> Update-AzureSiteRecoveryProtectionEntity -ProtectionEntity $ProtectionEntity
           Name             : 
           ID               : 680ffe0f-6236-465e-8c94-81242fa67e6d
           ClientRequestId  : 2c47e6ce-1460-4187-8a0f-b9073735fa38-2014-12-30 06:44:40Z-P
           State            : NotStarted
           StateDescription : NotStarted
           StartTime        : 
           EndTime          : 
           AllowedActions   : {}
           Tasks            : {}
           Errors           : {}
```

Der erste Befehl ruft einen geschützten Container mit dem Cmdlet **Get-AzureSiteRecoveryProtectionContainer** ab und speichert dieses Objekt dann in der $Container Variablen.

Der zweite Befehl ruft den geschützten virtuellen Computer ab, der dem in $Container gespeicherten Container mit dem Cmdlet **Get-AzureSiteRecoveryProtectionEntity** zugeordnet ist, und speichert ihn dann in der Variablen $ProtectionEntity.

Der endgültige Befehl aktualisiert die Schutz Entität in $ProtectionEntity.

## Parameter

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

### -ProtectionEntity
Gibt eine zu aktualisierende Schutz Entität an.
Verwenden Sie das Cmdlet **Get-AzureSiteRecoveryProtectionEntity** , um ein **ASRProtectionEntity** -Objekt abzurufen.

```yaml
Type: ASRProtectionEntity
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WaitForCompletion
Gibt an, dass dieses Cmdlet wartet, bis der Vorgang abgeschlossen ist, bevor es die Steuerung an die Windows PowerShell-Konsole zurückgibt.

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

[Satz-AzureSiteRecoveryProtectionEntity](./Set-AzureSiteRecoveryProtectionEntity.md)


