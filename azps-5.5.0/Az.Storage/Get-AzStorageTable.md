---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
ms.openlocfilehash: d501faaebcc5e381dc2a7270c8b55b148e2812b4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163025"
---
# Get-AzStorageTable

## SYNOPSIS
Listet die Speichertabellen auf.

## SYNTAX

### TableName (Standard)
```
Get-AzStorageTable [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### TablePrefix
```
Get-AzStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzStorageTable"** listet die Speichertabellen auf, die dem Speicherkonto in Azure zugeordnet sind.

## BEISPIELE

### Beispiel 1: Auflisten aller Azure Storage-Tabellen
```
PS C:\>Get-AzStorageTable
```

Dieser Befehl ruft alle Speichertabellen für ein Speicherkonto ab.

### Beispiel 2: Auflisten von Azure Storage-Tabellen mit einem Platzhalterzeichen
```
PS C:\>Get-AzStorageTable -Name table*
```

Dieser Befehl verwendet ein Platzhalterzeichen, um Speichertabellen zu erhalten, deren Name mit der Tabelle beginnt.

### Beispiel 3: Auflisten von Azure Storage-Tabellen mit dem Tabellennamenpräfix
```
PS C:\>Get-AzStorageTable -Prefix "table"
```

Dieser Befehl verwendet den *Präfixparameter,* um Speichertabellen zu erhalten, deren Name mit der Tabelle beginnt.

## PARAMETERS

### -Context
Gibt den Speicherkontext an.
Zum Erstellen können Sie das cmdlet New-AzStorageContext erstellen.

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
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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
Wenn der Tabellenname leer ist, werden im Cmdlet alle Tabellen aufgeführt.
Andernfalls werden alle Tabellen aufgeführt, die dem angegebenen Namen oder dem normalen Namensmuster entsprechen.

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
Gibt ein Präfix an, das im Namen der Tabelle oder Tabellen verwendet wird, die Sie erhalten möchten.
Auf diese Weise können Sie nach allen Tabellen suchen, die mit derselben Zeichenfolge beginnen, z. B. "Tabelle".

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## AUSGABEN

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[New-AzStorageTable](./New-AzStorageTable.md)

[Remove-AzStorageTable](./Remove-AzStorageTable.md)


