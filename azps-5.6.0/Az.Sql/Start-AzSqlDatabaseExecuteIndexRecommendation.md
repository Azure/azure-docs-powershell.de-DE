---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/powershell/module/az.sql/start-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: 74beb667ec01af4661c2f56daa6a3159d960622a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930763"
---
# Start-AzSqlDatabaseExecuteIndexRecommendation

## SYNOPSIS
Startet den Workflow, der einen empfohlenen Indexvorgang ausgeführt.

## SYNTAX

```
Start-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Start-AzSqlDatabaseExecuteIndexRecommendation** startet den Workflow, der einen empfohlenen Indexvorgang für eine Azure SQL ausführt.

## BEISPIELE

### Beispiel 1: Ausführen einer Indexempfehlung
```
PS C:\>Start-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

Mit diesem Befehl wird eine Indexempfehlung ausgeführt.

## PARAMETER

### -DatabaseName
Gibt den Namen der Datenbank an, für die dieses Cmdlet den Workflow startet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IndexRecommendationName
Gibt den Namen der Indexempfehlung an, die von diesem Cmdlet ausgeführt wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Servername
Gibt den Server an, der die Datenbank hostet, für die dieses Cmdlet einen Workflow startet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Sql.Model.IndexRecommendation

## NOTIZEN

## VERWANDTE LINKS

[Get-AzSqlDatabaseIndexRecommendation](./Get-AzSqlDatabaseIndexRecommendation.md)

[Stop-AzSqlDatabaseExecuteIndexRecommendation](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)

[SQL Datenbankdokumentation](https://docs.microsoft.com/azure/sql-database/)


