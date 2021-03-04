---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 50fb3af805adf4e42ab0b6bf1824b09473d98239
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938520"
---
# Get-AzRecoveryServicesBackupManagementServer

## SYNOPSIS
Ruft SCDPM- und Azure Backup-Verwaltungsserver ab.

## SYNTAX

```
Get-AzRecoveryServicesBackupManagementServer [[-Name] <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Get-AzRecoveryServicesBackupManagementServer-Cmdlet** ruft eine Liste der Sicherungsverwaltungsserver ab, die in einem Tresor registriert sind.
Es gibt zwei Arten von Sicherungsverwaltungsservern: System Center Data Protection Manager (SCDPM) und Azure Backup-Verwaltungsserver.
Sicherungsverwaltungsserver werden separat installiert, um die Sicherungs orchestrierung zu verwalten.
Legen Sie den Tresorkontext mithilfe des cmdlets Set-AzRecoveryServicesVaultContext, bevor Sie das aktuelle Cmdlet verwenden.

## BEISPIELE

### Beispiel 1: Alle Sicherungsverwaltungsserver erhalten
```
PS C:\>Get-AzRecoveryServicesBackupManagementServer
```

Dieser Befehl ruft alle beim Tresor registrierten Sicherungsverwaltungsserver ab.

## PARAMETER

### -DefaultProfile
Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -Name
Gibt den Namen des Sicherungsverwaltungsservers an, den Sie erhalten möchten.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase

## NOTIZEN

## VERWANDTE LINKS

[Aufheben der Registrierung-AzRecoveryServicesBackupManagementServer](./Unregister-AzRecoveryServicesBackupManagementServer.md)


