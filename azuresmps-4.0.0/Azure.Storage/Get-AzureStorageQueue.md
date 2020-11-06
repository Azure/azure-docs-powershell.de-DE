---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 11a8ffe26a65bf2ecabab7807d8e54bc23b629fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475674"
---
# Get-AzureStorageQueue

## Synopsis
Listet Speicher Warteschlangen auf.

## Syntax

### QueueName (Standard)
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### QueuePrefix
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureStorageQueue** " listet Speicher Warteschlangen auf, die einem Azure-Speicherkonto zugeordnet sind.

## Beispiele

### Beispiel 1: Auflisten aller Azure-Speicher Warteschlangen
```
PS C:\>Get-AzureStorageQueue
```

Dieser Befehl ruft eine Liste aller Speicher Warteschlangen für das aktuelle Speicherkonto ab.

### Beispiel 2: Auflisten von Azure-Speicher Warteschlangen mit einem Platzhalterzeichen
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

Dieser Befehl verwendet ein Platzhalterzeichen, um eine Liste der Speicher Warteschlangen abzurufen, deren Name mit Queue beginnt.

### Beispiel 3: Auflisten von Azure-Speicher Warteschlangen mithilfe des Warteschlangennamen Präfix
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

In diesem Beispiel wird der *prefix* -Parameter verwendet, um eine Liste der Speicher Warteschlangen abzurufen, deren Name mit Queue beginnt.

## Parameter

### -Context
Gibt den Azure-Speicherkontext an.
Sie können Sie mithilfe des Cmdlets **New-AzureStorageContext** erstellen.

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
Gibt einen Namen an.
Wenn kein Name angegeben wird, ruft das Cmdlet eine Liste aller Warteschlangen ab.
Wenn ein vollständiger oder partieller Name angegeben wird, ruft das Cmdlet alle Warteschlangen ab, die dem Namensmuster entsprechen.

```yaml
Type: String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Prefix
Gibt ein Präfix an, das für den Namen der Warteschlangen verwendet wird, die Sie abrufen möchten.

```yaml
Type: String
Parameter Sets: QueuePrefix
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

## Ausgaben

## Notizen

## Verwandte Links

[Neu – AzureStorageQueue](./New-AzureStorageQueue.md)

[Remove-AzureStorageQueue](./Remove-AzureStorageQueue.md)


