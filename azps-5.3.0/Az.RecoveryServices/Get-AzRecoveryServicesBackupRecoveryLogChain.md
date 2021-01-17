---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: ba82e1ddf8385f74b271feb9119280d48fc1b859
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472095"
---
# Get-AzRecoveryServicesBackupRecoveryLogChain

## SYNOPSIS
Dieser Befehl listet die Start- und Endpunkte der nicht aufgebrochenen Protokollkette des angegebenen Sicherungselements auf. Damit können Sie feststellen, ob der Zeitpunkt, zu dem der Benutzer die DB wiederherstellen möchte, gültig ist oder nicht.

## SYNTAX

### NoFilterParameterSet (Standard)
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### DateTimeFilter
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzRecoveryServicesBackupRecoveryLogChain"** ruft die Wiederherstellungspunkte für den Zeitraum für ein gesichertes Azure Backup-Element ab.
Nachdem ein Element gesichert wurde, hat ein **AzRecoveryServicesBackupRecoveryLogChain-Objekt** einen oder mehrere Wiederherstellungszeitbereiche.

## BEISPIELE

### Beispiel 1
```powershell
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

Der erste Befehl ruft das Datum von vor sieben Tagen ab und speichert es dann in der $StartDate Variable.
Der zweite Befehl ruft das aktuelle Datum ab und speichert es dann in der $EndDate Variable.
Der dritte Befehl ruft Sicherungscontainer für AzureWorkload ab und speichert sie in der $Container Variable.
Der vierte Befehl ruft das Sicherungselement ab und gibt es dann über das Cmdlet "Pipedlet" als Sicherungselementobjekt aus.
Der letzte Befehl ruft ein Array von Wiederherstellungspunktzeitbereichen für das Element in $BackupItem ab und speichert sie dann in $RP Variable.

### Beispiel 2

Dieser Befehl listet die Start- und Endpunkte der nicht aufgebrochenen Protokollkette des angegebenen Sicherungselements auf. (automatisch generiert)

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupRecoveryLogChain -Item $Item -VaultId $vault.ID
```

## PARAMETERS

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -EndDate
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
Geschütztes Elementobjekt, für das ein Wiederherstellungspunkt abgerufen werden muss

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

### -VaultId
ARM-ID des Wiederherstellungsdienste-Tresors.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
System.String

## AUSGABEN

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
