---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: D57C32D1-EB4F-495E-A11B-3B4066E8C552
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
ms.openlocfilehash: 82e86d27c5ef628e6cd6122fa024ac72788e79db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500946"
---
# Set-AzureRmBackupVault

## Synopsis
Ändert den Speichertyp eines Sicherungs Depots.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Set-AzureRmBackupVault [[-Storage] <AzureBackupVaultStorageType>] [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureRmBackupVault** " ändert den Speichertyp eines Azure Backup Vaults.
Sie können andere Eigenschaften eines Tresors nicht ändern.

## Beispiele

### Beispiel 1: Ändern des Speichers für einen vorhandenen Tresor
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Set-AzureRmBackupVault -Storage LocallyRedundant
```

Dieser Befehl ruft das Azure Backup Vault mit dem Namen Vault03 mit dem Cmdlet **Get-AzureRmBackupVault** .
Der Befehl übergibt diesen Tresor mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Das aktuelle Cmdlet ändert den Speichertyp in LocallyRedundant.

## Parameter

### -Speicher
Gibt den Speichertyp für die Sicherungsdaten an.
Die zulässigen Werte für diesen Parameter sind: LocallyRedundant und georedundant.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases: 
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vault
Gibt ein Sicherungs Depot an, das von diesem Cmdlet geändert wird.
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

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### AzureRmBackupVault

## Ausgaben

### Keine

## Notizen
* Wenn Sie den ersten Server oder virtuellen Computer für einen Tresor registrieren, ist der Speichertyp gesperrt. Anschließend können Sie den Speichertyp nicht ändern.

## Verwandte Links

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Neu – AzureRmBackupVault](./New-AzureRmBackupVault.md)

[Remove-AzureRmBackupVault](./Remove-AzureRmBackupVault.md)


