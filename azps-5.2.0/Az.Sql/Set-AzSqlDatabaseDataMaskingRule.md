---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 544db2f0e23cb510c81fb64898b6bcf856e760e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98300739"
---
# Set-AzSqlDatabaseDataMaskingRule

## SYNOPSIS
Legt die Eigenschaften einer Datenmaskregel für eine Datenbank fest.

## SYNTAX

```
Set-AzSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Set-AzSqlDatabaseDataMaskingRule"** legt eine Datenmaskierungsregel für eine Azure SQL fest.
Um das Cmdlet zu verwenden, geben Sie die Parameter *"ResourceGroupName",* *"ServerName",* *"DatabaseName"* und *"RuleId"* zum Identifizieren der Regel an.
Sie können beliebige Parameter von *SchemaName,* *TableName* und *ColumnName* angeben, um die Regel neu zu definieren.
Geben Sie den *Parameter "MaskingFunction"* an, um die Maskierung der Daten zu ändern.
Wenn Sie den Wert "Number" oder "Text" für *"MaskingFunction"* angeben, können Sie die *Parameter "NumberFrom"* und *"NumberTo"* für die Zahlenformatierung oder die Parameter *"PrefixSize",* *"ReplacementString"* und *"SuffixSize"* für die Textformatierung angeben.
Wenn der Befehl erfolgreich ist und Sie den Parameter *"PassThru"* angeben, gibt das Cmdlet ein Objekt zurück, das die Eigenschaften der Datenmaskierungsregel und die Regelbezeichner beschreibt.
Regelbezeichner umfassen, sind aber nicht beschränkt auf: **ResourceGroupName,** **ServerName,** **DatabaseName** und **RuleId.**
Dieses Cmdlet wird auch vom Dienst SQL Server Stretch Database in Azure unterstützt.

## BEISPIELE

### Beispiel 1: Ändern des Bereichs einer Datenmaskierungsregel in einer Datenbank
```powershell
PS C:\>Set-AzSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

Mit diesem Befehl wird eine Datenmaskregel geändert, die die ID Rule17 enthält.
Diese Regel gilt in der Datenbank mit dem Namen "Database01" auf Server Server01.
Mit diesem Befehl werden die Grenzen für das Intervall geändert, in dem eine Zufallszahl als maskierter Wert generiert wird.
Der neue Bereich liegt zwischen 23 und 42.

### Beispiel 2

Legt die Eigenschaften einer Datenmaskregel für eine Datenbank fest. (automatisch generiert)

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlDatabaseDataMaskingRule -ColumnName 'column1' -DatabaseName $params.databaseName -MaskingFunction NoMasking -NumberFrom 5 -NumberTo 14 -PrefixSize <UInt32> -ReplacementString <String> -ResourceGroupName $params.rgname -SchemaName 'dbo' -ServerName $params.serverName -SuffixSize <UInt32> -TableName 'table1'
```

## PARAMETERS

### -ColumnName
Gibt den Namen der Spalte an, auf die die Maskierungsregel ausgerichtet ist.

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

### -MaskingFunction
Gibt die von der Regel verwendeten Maskierungsfunktion an.
Die zulässigen Werte für diesen Parameter sind:
- Standard
- NoMasking
- Text
- Zahl
- SocialSecurityNumber
- CreditCardNumber
- E-Mail Der Standardwert ist "Standard".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NumberFrom
Gibt die untere gebundene Zahl des Intervalls an, aus dem ein Zufallswert ausgewählt wird.
Geben Sie diesen Parameter nur an, wenn Sie für den Parameter *"MaskingFunction"* den Wert "Number" angeben.
Der Standardwert ist "0".

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NumberTo
Gibt die obere gebundene Zahl des Intervalls an, aus dem ein Zufallswert ausgewählt wird.
Geben Sie diesen Parameter nur an, wenn Sie für den Parameter *"MaskingFunction"* den Wert "Number" angeben.
Der Standardwert ist "0".

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.
Standardmäßig generiert dieses Cmdlet keine Ausgabe.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrefixSize
Gibt die Anzahl von Zeichen am Anfang des Texts an, die nicht maskiert sind.
Geben Sie diesen Parameter nur an, wenn Sie für den Parameter *"MaskingFunction"* den Wert "Text" angeben.
Der Standardwert ist "0".

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ReplacementString
Gibt die Anzahl von Zeichen am Ende des Texts an, die nicht maskiert sind.
Geben Sie diesen Parameter nur an, wenn Sie für den Parameter *"MaskingFunction"* den Wert "Text" angeben.
Der Standardwert ist "0".

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

### -SchemaName
Gibt den Namen eines Schemas an.

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

### -ServerName
Gibt den Namen des Servers an, der die Datenbank hostet.

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

### -SuffixSize
Gibt die Anzahl von Zeichen am Ende des Texts an, die nicht maskiert sind.
Geben Sie diesen Parameter nur an, wenn Sie für den Parameter *"MaskingFunction"* den Wert "Text" angeben.
Der Standardwert ist "0".

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TableName
Gibt den Namen der Datenbanktabelle an, die die maskierte Spalte enthält.

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

### -Confirm
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

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

### -Waswenn
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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

### System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Nullable'1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## AUSGABEN

### Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzSqlDatabaseDataMaskingRule](./Get-AzSqlDatabaseDataMaskingRule.md)

[New-AzSqlDatabaseDataMaskingRule](./New-AzSqlDatabaseDataMaskingRule.md)

[Remove-AzSqlDatabaseDataMaskingRule](./Remove-AzSqlDatabaseDataMaskingRule.md)

[SQL Datenbankdokumentation](https://docs.microsoft.com/azure/sql-database/)


