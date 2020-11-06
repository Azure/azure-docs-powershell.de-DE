---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 2605B232-10CA-4426-9917-7C9719C15166
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/enable-azurermbackupcontainerreregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
ms.openlocfilehash: 6ae660eae9e597d92e162529ff244431d4720418
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480586"
---
# Enable-AzureRmBackupContainerReregistration

## Synopsis
Registrieren Sie einen Server erneut, um eine Verbindung mit einem sicherungstresor herzustellen.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Enable-AzureRmBackupContainerReregistration [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **enable-AzureRmBackupContainerReregistration** wird ein Server erneut registriert, um eine Verbindung mit einem Azure Backup Vault herzustellen und die Backup-Wiederherstellungspunkt Kette fortzusetzen.
Wenn Sie einen Server zerstören, verbleiben alle seine Cloud-Sicherungspunkte im Sicherungsspeicher.
Wenn Sie einen Ersatzserver erstellen und ihm denselben vollqualifizierten Domänennamen zuweisen, können Sie den Server wieder mit demselben Tresor verbinden.
Mit diesem Cmdlet kann die Sicherung Backups erstellen und dem vorhandenen Satz neue Sicherungspunkte hinzufügen.
Das neue, das der Server in der Sicherungskette fortsetzt.

## Beispiele

## Parameter

### -Container
Gibt den Container an, der von diesem Cmdlet erneut registriert wird.
Verwenden Sie zum Abrufen eines **AzureRmBackupContainer** das Get-AzureRmBackupContainer-Cmdlet.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupContainer
Parameter: Container (ByValue)

## Ausgaben

### System. void

## Notizen

## Verwandte Links

[Get-AzureRmBackupContainer](./Get-AzureRmBackupContainer.md)

[Registrieren-AzureRmBackupContainer](./Register-AzureRmBackupContainer.md)


