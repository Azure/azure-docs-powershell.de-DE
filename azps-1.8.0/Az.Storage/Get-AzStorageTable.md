---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
ms.openlocfilehash: 5c575ace97687ca6906a73e8e79d93343f369f45
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658849"
---
# Get-AzStorageTable

## Synopsis
Listet die Speichertabellen auf.

## Syntax

### Tabellenname (Standard)
```
Get-AzStorageTable [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### TablePrefix
```
Get-AzStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzStorageTable** " listet die Speichertabellen auf, die dem Speicherkonto in Azure zugeordnet sind.

## Beispiele

### Beispiel 1: Auflisten aller Azure-Speichertabellen
```
PS C:\>Get-AzStorageTable
```

Dieser Befehl ruft alle Speichertabellen für ein Speicherkonto ab.

### Beispiel 2: Auflisten von Azure-Speichertabellen mit einem Platzhalterzeichen
```
PS C:\>Get-AzStorageTable -Name table*
```

Dieser Befehl verwendet ein Platzhalterzeichen, um Speichertabellen abzurufen, deren Name mit Tabelle beginnt.

### Beispiel 3: Auflisten von Azure-Speichertabellen mit dem Tabellennamen Präfix
```
PS C:\>Get-AzStorageTable -Prefix "table"
```

Dieser Befehl verwendet den *prefix* -Parameter, um Speichertabellen abzurufen, deren Name mit Tabelle beginnt.

## Parameter

### -Context
Gibt den Speicherkontext an.
Sie können das New-AzStorageContext-Cmdlet verwenden, um es zu erstellen.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Tabellennamen an.
Wenn der Tabellenname leer ist, listet das Cmdlet alle Tabellen auf.
Andernfalls werden alle Tabellen aufgelistet, die dem angegebenen Namen oder dem Muster des regulären namens entsprechen.

```yaml
Type: System.String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Prefix
Gibt ein Präfix an, das für den Namen der Tabelle oder der Tabellen verwendet wird, die Sie abrufen möchten.
Sie können damit alle Tabellen suchen, die mit der gleichen Zeichenfolge beginnen, beispielsweise Table.

```yaml
Type: System.String
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

### System. String

### Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext

## Ausgaben

### Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageTable

## Notizen

## Verwandte Links

[Neu – AzStorageTable](./New-AzStorageTable.md)

[Remove-AzStorageTable](./Remove-AzStorageTable.md)


