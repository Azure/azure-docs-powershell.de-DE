---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 35f2bc63366a86501650af1808274a3a0403e77f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178679"
---
# New-AzSqlDatabaseDataMaskingRule

## Synopsis
Erstellt eine Daten Maskierungs Regel für eine Datenbank.

## Syntax

```
New-AzSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>] [-ReplacementString <String>]
 [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru] -SchemaName <String>
 -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzSqlDatabaseDataMaskingRule** erstellt eine Daten Maskierungs Regel für eine Azure SQL-Datenbank.
Um das Cmdlet zu verwenden, verwenden Sie die Parameter *ResourceGroupName* , *Servername* und *DatabaseName* , um die Regel zu identifizieren.
Geben Sie den *Namen* und *ColumnName* an, um das Ziel der Regel und den *MaskingFunction* -Parameter anzugeben, um zu definieren, wie die Daten maskiert werden.
Wenn *MaskingFunction* den Wert "Zahl" oder "Text" aufweist, können Sie die *NumberFrom* -und *NumberTo* -Parameter für die Maskierung von Zahlen oder die *PrefixSize* -, *Ersatz* -und *SuffixSize* für die Text Maskierung angeben.
Wenn der Befehl erfolgreich ausgeführt wird und der *passthru* -Parameter verwendet wird, gibt das Cmdlet zusätzlich zu den Regel Bezeichnern ein Objekt zurück, das die Eigenschaften der Daten Maskierungs Regel beschreibt.
Regelbezeichner sind: *ResourceGroupName* , *Servername* , *DatabaseName* und *rule* -ID.
Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.

## Beispiele

### Beispiel 1: Erstellen einer Daten Maskierungs Regel für eine Zahlenspalte in einer Datenbank
```
PS C:\>New-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"  -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

Dieser Befehl erstellt eine Daten Maskierungs Regel für die Spalte mit dem Namen Column01 in der Tabelle mit dem Namen Table01 im Schema mit dem Namen Schema01.
Die Datenbank mit dem Namen database01 enthält alle diese Elemente.
Bei der Regel handelt es sich um eine Zahlen Maskierungs Regel, die eine Zufallszahl zwischen 5 und 14 als Maskenwert verwendet.

## Parameter

### -ColumnName
Gibt den Namen der Spalte an, auf die die Maskierungs Regel ausgerichtet ist.

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

### -MaskingFunction
Gibt die Maskierungsfunktion an, die von der Regel verwendet wird.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- Standard
- Nomasking
- Text
- Anzahl
- SocialSecurityNumber
- CreditCardNumber
- E-Mail der Standardwert ist Standard.

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
Gibt die untere Grenze des Intervalls an, aus dem ein Zufallswert ausgewählt wird.
Geben Sie diesen Parameter nur an, wenn Sie für den *MaskingFunction* -Parameter den Wert Zahl angeben.
Der Standardwert ist 0.

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
Gibt die Obergrenze des Intervalls an, aus dem ein Zufallswert ausgewählt wird.
Geben Sie diesen Parameter nur an, wenn Sie für den *MaskingFunction* -Parameter den Wert Zahl angeben.
Der Standardwert ist 0.

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
Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.

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
Gibt die Anzahl der Zeichen am Anfang des Texts an, die nicht maskiert sind.
Geben Sie diesen Parameter nur an, wenn Sie einen Wert von Text für den *MaskingFunction* -Parameter angeben.
Der Standardwert ist 0.

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

### -Ersatz-Nr.
Gibt die Anzahl der Zeichen am Ende des Texts an, die nicht maskiert sind.
Geben Sie diesen Parameter nur an, wenn Sie einen Wert von Text für den *MaskingFunction* -Parameter angeben.
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

### -Schemaname
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

### -Servername
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
Gibt die Anzahl der Zeichen am Ende des Texts an, die nicht maskiert sind.
Geben Sie diesen Parameter nur an, wenn Sie einen Wert von Text für den *MaskingFunction* -Parameter angeben.
Der Standardwert ist 0.

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

### -Tabellenname
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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

### System. Nullable ' 1 [[System. UInt32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]

### System. Nullable ' 1 [[System. Double, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]

## Ausgaben

### Microsoft. Azure. Commands. SQL. datamasking. Model. DatabaseDataMaskingRuleModel

## Notizen

## Verwandte Links

[Get-AzSqlDatabaseDataMaskingRule](./Get-AzSqlDatabaseDataMaskingRule.md)

[Remove-AzSqlDatabaseDataMaskingRule](./Remove-AzSqlDatabaseDataMaskingRule.md)

[Satz-AzSqlDatabaseDataMaskingRule](./Set-AzSqlDatabaseDataMaskingRule.md)

[SQL-Datenbank-Dokumentation](https://docs.microsoft.com/azure/sql-database/)


