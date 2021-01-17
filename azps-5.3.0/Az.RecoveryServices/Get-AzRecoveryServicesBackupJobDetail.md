---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: 7ebbb3cf53c422a3a4d5c73f156cd3890eaa41e5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460908"
---
# Get-AzRecoveryServicesBackupJobDetail

## SYNOPSIS

Ruft Details für einen Sicherungsauftrag ab.

## SYNTAX

### JobFilterSet (Standard)
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### IdFilterSet
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG

Das **Cmdlet "Get-AzRecoveryServicesBackupJobDetail"** ruft Details zum Azure -Sicherungsauftrag für einen angegebenen Auftrag ab.
Legen Sie den Tresorkontext mithilfe des Parameters "-VaultId" ein.

Warnung: **Der Alias "Get-AzRecoveryServicesBackupJobDetails"** wird in einer zukünftigen Änderungsversion entfernt.

## BEISPIELE

### Beispiel 1: Erhalten von Sicherungsauftragsdetails für fehlgeschlagene Aufträge

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status Failed -VaultId $vault.ID
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0] -VaultId $vault.ID
PS C:\> $JobDetails.ErrorDetails
```

Der erste Befehl ruft den relevanten Tresor ab. Der zweite Befehl ruft ein Array mit fehlgeschlagenen Aufträgen im Tresor ab und speichert sie dann im $Jobs Array.
Der dritte Befehl ruft die Auftragsdetails für den ersten fehlgeschlagenen Auftrag in $Jobs ab und speichert sie dann in der $JobDetails Variable.
Der letzte Befehl zeigt Fehlerdetails für die fehlgeschlagenen Aufträge an.

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

### -Job

Gibt den zu erhaltenden Auftrag an.
Verwenden Sie das Cmdlet **"Get-AzRecoveryServicesBackupJob",** um ein **"BackupJob"-Objekt** zu erhalten.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: JobFilterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId

Gibt die ID eines Sicherungsauftrags an.
Die ID ist die "JobId"-Eigenschaft eines **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase-Objekts.**

```yaml
Type: System.String
Parameter Sets: IdFilterSet
Aliases:

Required: True
Position: 2
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

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzRecoveryServicesBackupJob](./Get-AzRecoveryServicesBackupJob.md)
