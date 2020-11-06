---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
ms.openlocfilehash: 651fdef0599a9a62de5d4bdfac8fc5e9105bb4dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500361"
---
# New-AzureRmStorageAccountKey

## Synopsis
Generiert einen Speicherschlüssel für ein Azure Storage-Konto erneut.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
New-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmStorageAccountKey** generiert einen Speicherschlüssel für ein Azure Storage-Konto erneut.

## Beispiele

### Beispiel 1: Erneutes Generieren eines Speicher Schlüssels
```
PS C:\>New-AzureRmStorageAccountKey -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -KeyName "key1"
```

Mit diesem Befehl wird ein Speicherschlüssel für das angegebene Speicherkonto neu generiert.

## Parameter

### -KeyName
Gibt an, welche Taste neu generiert werden soll.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- key1
- key2

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen des speicherkontos an, für das ein Speicherschlüssel neu generiert werden soll.

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

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, die das Speicherkonto enthält.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
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

[Get-AzureRmStorageAccountKey](./Get-AzureRmStorageAccountKey.md)
