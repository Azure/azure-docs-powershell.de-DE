---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueue.md
ms.openlocfilehash: 077d8139817c3998e27300d8c86c809b4da9e630
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482630"
---
# Get-AzureStorageQueue

## Synopsis
Listet Speicher Warteschlangen auf.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### QueueName (Standard)
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### QueuePrefix
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

### -Name
Gibt einen Namen an.
Wenn kein Name angegeben wird, ruft das Cmdlet eine Liste aller Warteschlangen ab.
Wenn ein vollständiger oder partieller Name angegeben wird, ruft das Cmdlet alle Warteschlangen ab, die dem Namensmuster entsprechen.

```yaml
Type: System.String
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
Type: System.String
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

### System. String

### Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext

## Ausgaben

### Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageQueue

## Notizen

## Verwandte Links

[Neu – AzureStorageQueue](./New-AzureStorageQueue.md)

[Remove-AzureStorageQueue](./Remove-AzureStorageQueue.md)


