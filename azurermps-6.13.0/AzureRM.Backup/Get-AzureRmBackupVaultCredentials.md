---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9882F1A5-6FFB-4DAF-8ED5-B14596BC939D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupvaultcredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
ms.openlocfilehash: 6ee9e3062108049e517dbea09573af7905dd54d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663679"
---
# Get-AzureRmBackupVaultCredentials

## Synopsis
Lädt die Vault-Anmeldeinformationsdatei für einen Sicherungsspeicher herunter.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmBackupVaultCredentials [-TargetLocation] <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmBackupVaultCredentials** " downloadet die Vault-Anmeldeinformationsdatei für ein Azure Backup Vault.
Bei der Sicherung wird eine Vault-Anmeldeinformationsdatei verwendet, um einen Server mit dem Azure Backup Vault zu verbinden und zu registrieren.
Sie müssen einen Server registrieren, bevor Sicherungsdaten an den Tresor gesendet werden können.

## Beispiele

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

### -Zielstandort
Gibt den Zielpfad an, in dem dieses Cmdlet die Vault-Anmeldeinformationsdatei speichert.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vault
Gibt den sicherungstresor an, für den dieses Cmdlet eine Vault-Anmeldeinformationsdatei erhält.
Verwenden Sie das Get-AzureRmBackupVault-Cmdlet, um ein **AzureRmBackupVault** -Objekt zu erhalten.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupVault
Parameter: Vault (ByValue)

## Ausgaben

### System. String
Dieses Cmdlet gibt den Namen der Vault-Anmeldeinformationsdatei zurück.

## Notizen

## Verwandte Links

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)


