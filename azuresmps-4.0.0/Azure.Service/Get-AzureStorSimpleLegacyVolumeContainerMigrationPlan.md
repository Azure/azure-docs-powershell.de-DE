---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: E4F6D096-E265-49CF-AA73-E9C807F8383B
online version: ''
schema: 2.0.0
ms.openlocfilehash: b0207d4b7eddfe56a8e4e86aac6899d19c10f44e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005762"
---
# Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan

## Synopsis
Ruft Migrationspläne für Legacy Container ab.

## Syntax

```
Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan [-LegacyConfigId <String>]
 [-LegacyContainerNames <String[]>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureStorSimpleLEgacyVolumeContainerMigrationPlan** " ruft Migrationspläne für Legacy Container ab.
Geben Sie einen Migrationsplan anhand seiner Legacy-Konfigurations-ID an.
Wenn die Erstellung des Migrationsplans noch nicht abgeschlossen ist, ruft dieses Cmdlet den Status des Migrationsplans ab.
Wenn der Migrationsplan abgeschlossen ist, gibt dieses Cmdlet den tatsächlichen Migrationsplan für den Satz von Legacy Containern zurück.
Wenn Sie den *LegacyConfigId* -Parameter nicht angeben, gibt dieses Cmdlet eine Liste mit Konfigurations-IDs zurück.

## Beispiele

### Beispiel 1: Abrufen des Status eines Plans
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "f16463bd-94a9-4c3c-91c2-7a3ba7120087" -LegacyContainerNames "OneSDKAzureCloud"
VERBOSE: 2015-04-08 13:48:05 ClientRequestId: 51e413fd-c2c9-4108-88cd-a0e792eab80a_PS
VERBOSE: 2015-04-08 13:48:05 ClientRequestId: 4c6398ef-35a0-4d1c-931e-d9d45599a97a_PS
VERBOSE: 2015-04-08 13:48:17 ClientRequestId: ef7a7e35-6dff-46cd-9df3-cb5fa25d149e_PS
VERBOSE: Request Id : fd7e502f273885468f633a44567bcb3f, HttpResponse OK
VERBOSE: List of volume containers: 


LegacyConfigId                    : f16463bd-94a9-4c3c-91c2-7a3ba7120087
DeviceName                        : ARUNKM-N4
MigrationTimeEstimationCompleted  : CloudConfigurationName        : OneSDKAzureCloud
                                    EstimatedTimeForLatestBackup  : 15Minutes
                                    EstimatedTimeForAllBackups    : 15Minutes
                                    These estimates are assuming 20 MBps bandwidth. Refer to migration guide to re-calculate for lower bandwidths. 



MigrationTimeEstimationInProgress : None
MigrationTimeEstimationFailed     : None
MigrationTimeEstimationNotStarted : None
```

Mit diesem Befehl wird der Status des Migrationsplans abgerufen.
Der Status umfasst angenommene Bandbreite, geschätzte Zeit und verwandte Informationen.

### Beispiel 2: Abrufen der IDs vorhandener Pläne
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
VERBOSE: 2015-04-08 13:46:51 ClientRequestId: 813da56c-0cfc-4325-80db-08ef32bdde1e_PS
VERBOSE: 2015-04-08 13:46:51 ClientRequestId: 9e7cf244-1894-490a-be02-749834a99318_PS
VERBOSE: List of LegacyConfig Ids on the resource: 

LegacyConfigId                                              DeviceName
--------------                                              ----------
1e1f10a0-3dff-4249-b847-4930061cd87a                        ARUNKM-N4
26d4096d-49b6-4102-b188-0446ece73c8b                        ARUNKM-N4
```

Dieser Befehl ruft alle Konfigurations-IDs von Migrationsplänen ab.

## Parameter

### -LegacyConfigId
Gibt die eindeutige ID der Konfiguration der Legacy-Appliance an.

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

### -LegacyContainerNames
Gibt ein Array von Volumen Containernamen an, für die dieses Cmdlet einen Migrationsplan erhält.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Gibt ein Azure-Profil an.

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

### Keine

## Ausgaben

### MigrationPlanMsg
Dieses Cmdlet gibt ein **MigrationPlanMsg** -Objekt zurück, das den Status des Migrationsplan Auftrags enthält, die Bandbreite in Megabit pro Sekunde und die geschätzte Zeit in Minuten angenommen hat.

## Notizen

## Verwandte Links

[Anfang-AzureStorSimpleLegacyVolumeContainerMigrationPlan](./Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


