---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BBF12B16-C5FD-4AE2-B5D7-AFDC29CEE4D3
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/unregister-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 8a2c2e671d29bb2a547d6fa57c946bb2793765d0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931720"
---
# Unregister-AzRecoveryServicesBackupManagementServer

## SYNOPSIS
Die Registrierung eines SCDPM-Servers oder Sicherungsservers aus dem Tresor wird aufgehoben.

## SYNTAX

```
Unregister-AzRecoveryServicesBackupManagementServer [-AzureRmBackupManagementServer] <BackupEngineBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Unregister-AzRecoveryServicesBackupManagementServer"** registriert einen System Center Data Protection Manager (SCDPM)-Server oder einen Azure Backup-Server aus dem Tresor.
Mit diesem Cmdlet werden Verweise auf die Server entfernt, die nicht aus dem Tresor registriert sind.
Bevor Sie die Registrierung eines Containers aufheben können, müssen Sie alle geschützten Daten löschen, die diesem Container zugeordnet sind.
Legen Sie den Tresorkontext mithilfe des cmdlets Set-AzRecoveryServicesVaultContext, bevor Sie das aktuelle Cmdlet verwenden.

## BEISPIELE

### Beispiel 1: Aufheben der Registrierung eines SCDPM-Servers aus dem Tresor
```powershell
PS C:\>$BMS = Get-AzRecoveryServicesBackupManagementServer -Name "dpmserver01.contoso.com"
PS C:\> Unregister-AzRecoveryServicesBackupManagementServer -AzBackupManagementServer $BMS
```

Der erste Befehl ruft den Sicherungsverwaltungsserver dpmserver01.contoso.com ab und speichert ihn dann in der $BMS Variablen.
Mit dem zweiten Befehl wird die Registrierung des SCDPM-Servers aus dem Tresor aufgehoben.

### Beispiel 2

Die Registrierung eines SCDPM-Servers oder Sicherungsservers aus dem Tresor wird aufgehoben. (automatisch generiert)

```powershell <!-- Aladdin Generated Example --> 
Unregister-AzRecoveryServicesBackupManagementServer -AzureRmBackupManagementServer <BackupEngineBase> -VaultId $vault.ID
```

## PARAMETER

### -AzureRmBackupManagementServer
Der Sicherungscontainer der Wiederherstellungsdienste.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -PassThru
Geben Sie den Sicherungsverwaltungsserver zurück, der gelöscht werden soll.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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

### -Bestätigen
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird. 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

[Get-AzRecoveryServicesBackupManagementServer](./Get-AzRecoveryServicesBackupManagementServer.md)


