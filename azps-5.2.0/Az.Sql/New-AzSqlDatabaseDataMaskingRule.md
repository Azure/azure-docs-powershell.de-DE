---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 35f2bc63366a86501650af1808274a3a0403e77f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360630"
---
# New-AzSqlDatabaseDataMaskingRule

## SYNOPSIS
Erstellt eine Datenmaskregel für eine Datenbank.

## SYNTAX

```
New-AzSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>] [-ReplacementString <String>]
 [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru] -SchemaName <String>
 -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "New-AzSqlDatabaseDataMaskingRule"** erstellt eine Datenmaskierungsregel für eine Azure SQL Datenbank.
Verwenden Sie zum Verwenden des Cmdlets die Parameter *"ResourceGroupName",* *"ServerName"* und *"DatabaseName",* um die Regel zu identifizieren.
Geben Sie *"TableName"* und *"ColumnName"* an, um das Ziel der Regel und den *Parameter "MaskingFunction"* anzugeben, um zu definieren, wie die Daten maskiert werden.
Wenn *"MaskingFunction"* den Wert "Number" oder "Text" hat, können Sie die Parameter *"NumberFrom"* und *"NumberTo"* für die Zahlenformatierung oder die Parameter *"PrefixSize",* *"ReplacementString"* und *"SuffixSize"* für die Textformatierung angeben.
Wenn der Befehl erfolgreich ist und der *Parameter "PassThru"* verwendet wird, gibt das Cmdlet zusätzlich zu den Regelbezeichnern ein Objekt zurück, das die Eigenschaften der Datenmaskierungsregel beschreibt.
Regelbezeichner umfassen, sind aber nicht beschränkt auf, *ResourceGroupName,* *ServerName,* *DatabaseName* und *RuleID.*
Dieses Cmdlet wird auch vom Dienst SQL Server Stretch Database in Azure unterstützt.

## BEISPIELE

### Beispiel 1: Erstellen einer Datenmaskregel für eine Zahlenspalte in einer Datenbank
```
PS C:\>New-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"  -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

Mit diesem Befehl wird eine Datenmaskregel für die Spalte "Column01" in der Tabelle namens "Table01" im Schema "Schema01" erstellt.
Die Datenbank namens "Datenbank01" enthält alle diese Elemente.
Bei der Regel handelt es sich um eine Zahlenformatregel, bei der eine Zufallszahl zwischen 5 und 14 als Maskenwert verwendet wird.

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

Required: True
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
Der Standardwert ist eine leere Zeichenfolge.

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

[Remove-AzSqlDatabaseDataMaskingRule](./Remove-AzSqlDatabaseDataMaskingRule.md)

[Set-AzSqlDatabaseDataMaskingRule](./Set-AzSqlDatabaseDataMaskingRule.md)

[SQL Datenbankdokumentation](https://docs.microsoft.com/azure/sql-database/)


