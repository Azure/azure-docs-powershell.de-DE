---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76876cb76e65c913401d62fc7f08b3cb8b5626c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475318"
---
# New-AzureStorageQueue

## Synopsis
Erstellt eine Speicherwarteschlange.

## Syntax

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureStorageQueue** erstellt eine Speicherwarteschlange in Azure.

## Beispiele

### Beispiel 1: Erstellen einer Azure Storage-Warteschlange
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

In diesem Beispiel wird eine Speicherwarteschlange mit dem Namen "queueabc" erstellt.

### Beispiel 2: Erstellen mehrerer Azure Storage-Warteschlangen
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

In diesem Beispiel werden mehrere Speicher Warteschlangen erstellt.
Sie verwendet die Split-Methode der .net-Zeichenfolgenklasse und übergibt dann die Namen in der Pipeline.

## Parameter

### -Context
Gibt den Azure-Speicherkontext an.
Sie können es mithilfe des New-AzureStorageContext-Cmdlets erstellen.

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Name
Gibt einen Namen für die Warteschlange an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureStorageQueue](./Get-AzureStorageQueue.md)

[Remove-AzureStorageQueue](./Remove-AzureStorageQueue.md)


