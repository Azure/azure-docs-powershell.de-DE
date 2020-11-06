---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 3ba13fb1ee18f5dcc35b81ff70ebd7c5a61d1e4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477506"
---
# Get-AzureStorageTable

## Synopsis
Listet die Speichertabellen auf.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Tabellenname (Standard)
```
Get-AzureStorageTable [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### TablePrefix
```
Get-AzureStorageTable -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureStorageTable** " listet die Speichertabellen auf, die dem Speicherkonto in Azure zugeordnet sind.

## Beispiele

### Beispiel 1: Auflisten aller Azure-Speichertabellen
```
PS C:\>Get-AzureStorageTable
```

Dieser Befehl ruft alle Speichertabellen für ein Speicherkonto ab.

### Beispiel 2: Auflisten von Azure-Speichertabellen mit einem Platzhalterzeichen
```
PS C:\>Get-AzureStorageTable -Name table*
```

Dieser Befehl verwendet ein Platzhalterzeichen, um Speichertabellen abzurufen, deren Name mit Tabelle beginnt.

### Beispiel 3: Auflisten von Azure-Speichertabellen mit dem Tabellennamen Präfix
```
PS C:\>Get-AzureStorageTable -Prefix "table"
```

Dieser Befehl verwendet den *prefix* -Parameter, um Speichertabellen abzurufen, deren Name mit Tabelle beginnt.

## Parameter

### -Context
Gibt den Speicherkontext an.
Sie können das New-AzureStorageContext-Cmdlet verwenden, um es zu erstellen.

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
Gibt den Tabellennamen an.
Wenn der Tabellenname leer ist, listet das Cmdlet alle Tabellen auf.
Andernfalls werden alle Tabellen aufgelistet, die dem angegebenen Namen oder dem Muster des regulären namens entsprechen.

```yaml
Type: String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### -Prefix
Gibt ein Präfix an, das für den Namen der Tabelle oder der Tabellen verwendet wird, die Sie abrufen möchten.
Sie können damit alle Tabellen suchen, die mit der gleichen Zeichenfolge beginnen, beispielsweise Table.

```yaml
Type: String
Parameter Sets: TablePrefix
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

### IStorageContext

Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.

### Zeichenfolge

Der Parameter "Name" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.

## Ausgaben

### Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageTable

## Notizen

## Verwandte Links

[Neu – AzureStorageTable](./New-AzureStorageTable.md)

[Remove-AzureStorageTable](./Remove-AzureStorageTable.md)


