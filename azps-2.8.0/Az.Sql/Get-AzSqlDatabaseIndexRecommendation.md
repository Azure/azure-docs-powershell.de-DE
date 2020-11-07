---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 10656EA5-EA5F-4394-951F-BC64BE3BF6F9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
ms.openlocfilehash: 009dcceb07b676e61eaa923e8b7ddecfbda3cfda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825659"
---
# Get-AzSqlDatabaseIndexRecommendation

## Synopsis
Ruft die empfohlenen Indexvorgänge für einen Server oder eine Datenbank ab.

## Syntax

```
Get-AzSqlDatabaseIndexRecommendation -ServerName <String> [-DatabaseName <String>] [-TableName <String>]
 [-IndexRecommendationName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzSqlDatabaseIndexRecommendation** " Ruft die empfohlenen Indexvorgänge für einen Azure SQL-Datenbankserver oder eine Datenbank ab.

## Beispiele

### Beispiel 1: Abrufen von Indexempfehlungen für alle Datenbanken auf dem Server
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

Dieser Befehl gibt Indexempfehlungen für alle Datenbanken auf dem Server Server01 zurück.

### Beispiel 2: Abrufen von Indexempfehlungen für eine bestimmte Datenbank
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

Dieser Befehl gibt Indexempfehlungen für eine bestimmte Datenbank zurück.

### Beispiel 3: Abrufen einer einzelnen Indexempfehlung nach Name
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

Dieser Befehl gibt eine Empfehlung für einen einzelnen Index nach Namen zurück.

## Parameter

### -DatabaseName
Gibt den Namen der Datenbank an, für die dieses Cmdlet Indexempfehlungen erhält.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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
Gibt den Namen der Indexempfehlung an, die dieses Cmdlet erhält.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, für die der Server zugewiesen ist.
Dieses Cmdlet ruft Indexempfehlungen für eine von diesem Server gehostete Datenbank ab.

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
Gibt den Server an, der die Datenbank hostet, für die dieses Cmdlet Indexempfehlungen erhält.

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

### -Tabellenname
Gibt den Namen einer Azure SQL-Tabelle an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. SQL. Model. IndexRecommendation

## Notizen

## Verwandte Links

[Anfang-AzSqlDatabaseExecuteIndexRecommendation](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[Stopp-AzSqlDatabaseExecuteIndexRecommendation](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)
