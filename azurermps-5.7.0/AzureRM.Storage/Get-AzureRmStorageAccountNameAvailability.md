---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
ms.openlocfilehash: 8590c9566cf84648dc8668d3fb49ac19b8d4787d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662343"
---
# Get-AzureRmStorageAccountNameAvailability

## Synopsis
Überprüft die Verfügbarkeit eines Speicherkonto namens.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmStorageAccountNameAvailability [-Name] <String> [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmStorageAccountNameAvailability** " überprüft, ob der Name eines Azure-speicherkontos gültig und für die Verwendung verfügbar ist.

## Beispiele

### Beispiel 1: Überprüfen der Verfügbarkeit eines Speicherkonto namens
```
PS C:\>Get-AzureRmStorageAccountNameAvailability -Name 'ContosoStorage03'
```

Dieser Befehl überprüft die Verfügbarkeit des Namens ContosoStorage03.

## Parameter

### -Name
Gibt den Namen des speicherkontos an, das von diesem Cmdlet überprüft wird.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

## Notizen

## Verwandte Links

[Azure Storage Manager-Cmdlets](./AzureRM.Storage.md)
