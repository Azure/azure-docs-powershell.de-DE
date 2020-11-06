---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: DD150A2C-27D5-4119-9B43-FAB82F9F7D5B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/enable-azurermbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupProtection.md
ms.openlocfilehash: c66eda488b0b7876317b02db279202a88bbcc3d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498473"
---
# Enable-AzureRmBackupProtection

## Synopsis
Ordnet einem Element eine Azure Backup Protection-Richtlinie zu.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Enable-AzureRmBackupProtection -Policy <AzureRMBackupProtectionPolicy>
 [-Item] <AzureRMBackupContainerContextObject> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **enable-AzureRmBackupProtection** ordnet einem Element eine Azure Backup Protection-Richtlinie zu.
Um eine Schutzrichtlinie zu aktivieren, müssen Sie zunächst über ein vorhandenes Sicherungselement und eine vorhandene Richtlinie verfügen.
Beide müssen dem gleichen sicherungstresor angehören.
Der Sicherungszeitplan führt die vollständige anfangs Kopie für das Element und die inkrementelle Kopie für die nachfolgenden Sicherungen durch.

## Beispiele

### Beispiel 1: Aktivieren des Schutzes auf einem virtuellen Azure-Computer
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Policy = Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DefaultPolicy"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered | Get-AzureRmBackupItem | Enable-AzureRmBackupProtection -Policy $Policy
WorkloadName    Operation        Status          StartTime              EndTime
------------    ---------        ------          ---------              -------
co03-vm         ConfigureBackup  Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
```

Der erste Befehl ruft den Tresor mit dem Namen Vault03 mit dem Cmdlet **Get-AzureRmBackupVault** ab.
Der Befehl speichert das Objekt in der $Vault Variablen.
Der zweite Befehl ruft die Sicherungsschutz Richtlinie mit dem Namen DefaultPolicy für den Tresor in $Vault ab.
Der Befehl speichert das Objekt in der $Policy Variablen.
Der endgültige Befehl verwendet den Pipelineoperator, um Werte von einem Cmdlet an das nächste zu übergeben.
Mithilfe des Get-AzureRmBackupContainer-Cmdlets wird ein Container abgerufen.
Der Befehl ruft das Sicherungselement aus diesem Container mithilfe des Get-AzureRmBackupItem-Cmdlets ab.
Das aktuelle Cmdlet aktiviert die in $Policy gespeicherte Richtlinie für das Element, das der Befehl an dieses Cmdlet übergibt.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Item
Gibt das Sicherungselement an, für das dieses Cmdlet den Schutz aktiviert.
Verwenden Sie zum Abrufen eines **AzureRmBackupItem** das Get-AzureRmBackupItem-Cmdlet.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainerContextObject
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### – Richtlinien
Gibt eine Schutzrichtlinie an, die mit diesem Cmdlet einem Element zugeordnet ist.
Verwenden Sie das Get-AzureRmBackupProtectionPolicy-Cmdlet, um ein **AzureRmBackupProtectionPolicy** -Objekt zu erhalten.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
Parameter Sets: (All)
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

### Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupContainerContextObject
Parameter: Item (ByValue)

## Ausgaben

### Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupJob

## Notizen

## Verwandte Links

[Backup-AzureRmBackupItem](./Backup-AzureRmBackupItem.md)

[Get-AzureRmBackupItem](./Get-AzureRmBackupItem.md)

[Get-AzureRmBackupProtectionPolicy](./Get-AzureRmBackupProtectionPolicy.md)


