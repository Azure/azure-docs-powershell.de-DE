---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 302b781ee6af68cb960ab01668147edc56e04284
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501666"
---
# Update-AzureRmRecoveryServicesAsrPolicy

## Synopsis
Aktualisiert eine Azure Site Recovery-Replikationsrichtlinie.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Update-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Update-AzureRmRecoveryServicesAsrPolicy** aktualisiert die angegebene Azure Site Recovery-Replikationsrichtlinie.

## Beispiele

### Beispiel 1
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

Startet den Update-Replikationsrichtlinien Vorgang mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.

## Parameter

### -ApplicationConsistentSnapshotFrequencyInHours
Gibt die Häufigkeit (in Stunden) an, mit der anwendungskonsistente Wiederherstellungspunkte erstellt werden.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Authentifizierung
Gibt den verwendeten Authentifizierungstyp an.
Gültige Werte sind:

- Zertifikat
-  Kerberos

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Komprimierung
Gibt an, ob die Komprimierung aktiviert werden soll.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Verschlüsselung
Gibt an, ob die Verschlüsselung aktiviert oder deaktiviert werden soll.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inputobject
Eingabeobjekt für das Cmdlet: gibt das ASR-Replikationsrichtlinien Objekt an, das der zu aktualisierden Replikationsrichtlinie entspricht.

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NumberOfRecoveryPointsToRetain
Gibt die zu speichernden Nummern Wiederherstellungspunkte an.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryAzureStorageAccountId
Gibt die Azure-Speicherkonto-ID des Replikations Ziels an. Wird als Zielspeicher Konto für die Replikation verwendet, wenn keine Alternative bereitgestellt wird, während die Replikation mithilfe des New-AzureRmRecoveryServicesASRReplicationProtectedItem-Cmdlets aktiviert wird.

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

### -ReplicaDeletion
Gibt an, ob der virtuelle replikatcomputer beim Deaktivieren der Replikation von einer VMM-verwalteten Website zu einem anderen gelöscht werden soll.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationFrequencyInSeconds
Gibt das Replikations Häufigkeitsintervall in Sekunden an.
Gültige Werte sind:

- 30
- 300
- 900

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationMethod
Gibt die Replikationsmethode an.
Gültige Werte sind:

- Online
- Offline

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationPort
Gibt den Port an, der für die Replikation verwendet wird.

```yaml
Type: UInt16
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationStartTime
Gibt die Startzeit der Replikation an.
Sie darf nicht später als 24 Stunden nach dem Start des Auftrags erfolgen.

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
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

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy

## Ausgaben

### System. Object

## Notizen

## Verwandte Links

