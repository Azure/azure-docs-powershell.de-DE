---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: c8cf8074d6b077ed67f46f747c80439b41f9abca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824344"
---
# Get-AzRecoveryServicesBackupJobDetail

## Synopsis

Ruft Details für einen Backup-Auftrag ab.

## Syntax

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

## Beschreibung

Das Cmdlet " **Get-AzRecoveryServicesBackupJobDetail** " ruft Azure Backup-Auftragsdetails für einen angegebenen Auftrag ab.
Setzen Sie den Vault-Kontext mithilfe des-Vault-Parameters.

Warnung: **Get-AzRecoveryServicesBackupJobDetails-** Alias wird in einer zukünftigen Version von Breaking Change entfernt.

## Beispiele

### Beispiel 1: Abrufen von Backup-Auftragsdetails für fehlerhafte Aufträge

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status Failed -VaultId $vault.ID
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0] -VaultId $vault.ID
PS C:\> $JobDetails.ErrorDetails
```

Der erste Befehl ruft ein Array von fehlgeschlagenen Aufträgen im Tresor ab und speichert diese dann im $Jobs-Array.
Der zweite Befehl ruft die Auftragsdetails für die fehlgeschlagenen Aufträge in $Jobs ab und speichert Sie dann in der $JobDetails Variablen.
Der letzte Befehl zeigt Fehlerdetails für die fehlerhaften Aufträge an.

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

### -Job

Gibt den abzurufenden Auftrag an.
Verwenden Sie das Cmdlet **Get-AzRecoveryServicesBackupJob** , um ein **BackupJob** -Objekt abzurufen.

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

Gibt die ID eines Backup-Auftrags an.
Die ID ist die JobId-Eigenschaft eines **Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase** -Objekts.

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

### -CommonParameters

Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase

## Notizen

## Verwandte Links

[Get-AzRecoveryServicesBackupJob](./Get-AzRecoveryServicesBackupJob.md)
