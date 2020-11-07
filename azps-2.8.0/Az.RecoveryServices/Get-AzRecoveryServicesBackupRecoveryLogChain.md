---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: d06cae4fc13151d8b1c5c2b0fb4dd7803606fe49
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824328"
---
# Get-AzRecoveryServicesBackupRecoveryLogChain

## Synopsis
Dieser Befehl listet die Anfangs-und Endpunkte der unbeschädigten Protokollkette des angegebenen sicherungselements auf. Verwenden Sie diese Option, um zu ermitteln, ob der Zeitpunkt, zu dem der Benutzer die Datenbank wiederherstellen möchte, gültig ist.

## Syntax

### Nofilterset (Standard)
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### DateTimeFilter
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Get-AzRecoveryServicesBackupRecoveryLogChain werden** die Zeitbereich-Wiederherstellungspunkte rechtzeitig für ein gesichertes Azure-Sicherungselement abgerufen.
Nachdem ein Element gesichert wurde, verfügt ein **AzRecoveryServicesBackupRecoveryLogChain** -Objekt über einen oder mehrere Wiederherstellungszeit Bereiche.

## Beispiele

### Beispiel 1
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

Der erste Befehl ruft das Datum vor sieben Tagen ab und speichert es dann in der $StartDate-Variablen.
Der zweite Befehl ruft das heutige Datum ab und speichert es dann in der $EndDate Variablen.
Der dritte Befehl ruft AzureWorkload-Sicherungs Container ab und speichert Sie in der $Containers-Variablen.
Der vierte Befehl ruft das Sicherungselement ab und speichert es dann in der $BackupItem Variablen.
Der letzte Befehl ruft ein Array von Wiederherstellungspunkt-Zeitbereichen für das Element in $BackupItem ab und speichert Sie dann in der $RP-Variablen.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enddate
Endzeit des Zeitbereichs, für den der Wiederherstellungspunkt abgerufen werden muss

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Item
Geschütztes Element Objekt, für das der Wiederherstellungspunkt abgerufen werden muss

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StartDate
Startzeit des Zeitbereichs, für den der Wiederherstellungspunkt abgerufen werden muss

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tresor
Arm-ID des Speichers für Wiederherstellungsdienste

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ItemBase
System. String

## Ausgaben

### Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. RecoveryPointBase

## Notizen

## Verwandte Links