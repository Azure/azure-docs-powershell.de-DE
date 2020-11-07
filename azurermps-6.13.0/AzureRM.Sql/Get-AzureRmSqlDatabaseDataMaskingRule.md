---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 848A6972-AB29-46FB-8E03-FF2ADB113A0E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: c5cf2d8611238706bb9725101a320c79eb099570
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664001"
---
# Get-AzureRmSqlDatabaseDataMaskingRule

## Synopsis
Ruft die Regeln für die Daten Maskierung aus einer Datenbank ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmSqlDatabaseDataMaskingRule [-SchemaName <String>] [-TableName <String>] [-ColumnName <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmSqlDatabaseDataMaskingRule** " erhält entweder eine bestimmte Daten Maskierungs Regel oder alle Daten Maskierungs Regeln für eine Azure SQL-Datenbank.
Um das Cmdlet zu verwenden, verwenden Sie die *ResourceGroupName* -, *Servername* -und *DatabaseName* -Parameter, um die Datenbank zu identifizieren, und den Parameter " *rulecode* ", um anzugeben, welche Regel dieses Cmdlet zurückgibt.
Wenn Sie keine Regel- *Nr* angeben, werden alle Daten Maskierungs Regeln für diese Azure SQL-Datenbank zurückgegeben.
Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.

## Beispiele

### Beispiel 1: Abrufen aller Regeln für die Daten Maskierung aus einer Datenbank
```
PS C:\>Get-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table1
ColumnName        : column1
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :

DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table2
ColumnName        : column2
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :
```

### Beispiel 2: Abrufen der für das Schema "dbo" definierten Daten Maskierungs Regel, Tabelle "Tabelle1" und Spalte "Spalte1"
```
PS C:\>Get-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table1
ColumnName        : column1
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :
```

## Parameter

### -ColumnName
Gibt den Namen der Spalte an, auf die die Maskierungs Regel ausgerichtet ist.

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

### -DatabaseName
Gibt den Namen der Datenbank an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.

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

### -Schemaname
Gibt den Namen eines Schemas an.

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

### -Servername
Gibt den Namen des Servers an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. SQL. datamasking. Model. DatabaseDataMaskingRuleModel

## Notizen

## Verwandte Links

[Get-AzureRmSqlDatabaseDataMaskingPolicy](./Get-AzureRmSqlDatabaseDataMaskingPolicy.md)

[Neu – AzureRmSqlDatabaseDataMaskingRule](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[Remove-AzureRmSqlDatabaseDataMaskingRule](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[Satz-AzureRmSqlDatabaseDataMaskingPolicy](./Set-AzureRmSqlDatabaseDataMaskingPolicy.md)

[Satz-AzureRmSqlDatabaseDataMaskingRule](./Set-AzureRmSqlDatabaseDataMaskingRule.md)


