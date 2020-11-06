---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 698DCD00-13C0-4C36-A74B-35215D608339
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/remove-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
ms.openlocfilehash: 4b8098889cbec7bd313ffb2ed70c5384a7e24ef0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501545"
---
# Remove-AzureRmBackupVault

## Synopsis
Löscht einen Sicherungsspeicher.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Remove-AzureRmBackupVault [-Force] [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Remove-AzureRmBackupVault** wird ein Azure Backup Vault gelöscht.

Bevor Sie ein Sicherungs Depot löschen können, muss es leer sein.
Verwenden Sie das Cmdlet " **Remove-AzureRmBackupContainer** ", um die Backup-Daten des virtuellen Computers Infrastructure as a Service (IaaS) aus dem Tresor zu entfernen.
Verwenden Sie das Cmdlet **delete-registeredserver** , um andere registrierte Server und Sicherungsdaten zu entfernen.

## Beispiele

### Beispiel 1: Löschen eines Azure-Sicherungsspeichers
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Remove-AzureRmBackupVault
```

Dieser Befehl ruft das Azure Backup Vault mit dem Namen Vault03 mit dem Cmdlet **Get-AzureRmBackupVault** .
Der Befehl übergibt diesen Tresor mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Das aktuelle Cmdlet entfernt den Tresor.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vault
Gibt einen sicherungstresor an, den dieses Cmdlet entfernt.
Verwenden Sie zum Abrufen eines **AzureRmBackupVault** das Get-AzureRmBackupVault-Cmdlet.

```yaml
Type: AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### AzureRMBackupVault

## Ausgaben

### Keine

## Notizen
* Keine

## Verwandte Links

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Neu – AzureRmBackupVault](./New-AzureRmBackupVault.md)

[Satz-AzureRmBackupVault](./Set-AzureRmBackupVault.md)


