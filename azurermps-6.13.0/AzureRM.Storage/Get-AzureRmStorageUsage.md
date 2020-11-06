---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
ms.openlocfilehash: c63573da3c12eb54329d05f49615057d0595b77c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498162"
---
# Get-AzureRmStorageUsage

## Synopsis
Ruft die Speicherressourcen Verwendung des aktuellen Abonnements ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmStorageUsage [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmStorageUsage** " Ruft die Ressourcenverwendung für den Azure-Speicher für das aktuelle Abonnement ab.

## Beispiele

### Beispiel 1: Abrufen der Speicherressourcen Verwendung
```
PS C:\>Get-AzureRmStorageUsage
```

Dieser Befehl ruft die Speicherressourcen Verwendung des aktuellen Abonnements ab.
 

### Beispiel 2: Abrufen der Speicherressourcen Verwendung des angegebenen Speicherorts
```
PS C:\>Get-AzureRmStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

Mit diesem Befehl wird die Speicherressourcen Verwendung des angegebenen Speicherorts unter dem aktuellen Abonnement abgerufen.

## Parameter

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

### -Standort
Geben Sie an, dass die Speicherressourcen Verwendung am angegebenen Speicherort abgerufen werden soll.
Wenn diese nicht angegeben ist, wird die Verwendung von Speicherressourcen an allen Speicherorten unter dem Abonnement abgerufen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### Microsoft. Azure. Commands. Management. Storage. Models. PSU

## Notizen

## Verwandte Links

[Azure Storage Manager-Cmdlets](./AzureRM.Storage.md)


