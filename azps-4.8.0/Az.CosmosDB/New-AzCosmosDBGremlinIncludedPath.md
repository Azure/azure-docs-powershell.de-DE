---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
ms.openlocfilehash: 779589d3789e9b6baa1864f22366fb40b1c41c3c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009948"
---
# New-AzCosmosDBGremlinIncludedPath

## Synopsis
Erstellt ein neues Objekt vom Typ PSIncludedPath. Sie kann als Parameterwert für "AzCosmosDBGremlinGraph" übergeben werden.

## Syntax

```
New-AzCosmosDBGremlinIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Objekt, das dem IncludedPath der Gremlin-API entspricht.

## Beispiele

### Beispiel 1
```powershell
PS C:\> $index1 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
New-AzCosmosDBGremlinIncludedPath -Path "/*" -Index $index1
Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Index
Liste der Indizes für diesen Pfad

```yaml
Type: PSIndexes[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Der Pfad, auf den das Indizierungs Verhalten angewendet werden soll.
Index Pfade beginnen in der Regel mit "root" und enden mit Platzhalter (/Pfad/*).

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Keine

## Ausgaben

### Microsoft. Azure. Commands. CosmosDB. Models. PSIncludedPath

## Notizen

## Verwandte Links
