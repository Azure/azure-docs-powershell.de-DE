---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: dd29dd7e58a233d62e3af5260971d56300a43230
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662545"
---
# Set-AzureRmSqlDatabaseDataMaskingRule

## Synopsis
Legt die Eigenschaften einer Daten Maskierungs Regel für eine Datenbank fest.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Set-AzureRmSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Set-AzureRmSqlDatabaseDataMaskingRule** " legt eine Daten Maskierungs Regel für eine Azure SQL-Datenbank fest.
Um das Cmdlet zu verwenden, geben Sie die *ResourceGroupName* -, *Servername* -, *DatabaseName* -und *Rules* -Parameter an, um die Regel zu identifizieren.
Sie können einen der Parameter von Schema *Name* , *TableSchema* und *ColumnName* angeben, um die Regel erneut zu erreichen.
Geben Sie den *MaskingFunction* -Parameter an, um zu ändern, wie die Daten maskiert werden.

Wenn Sie einen Wert von Zahl oder Text für *MaskingFunction* angeben, können Sie die *NumberFrom* -und *NumberTo* -Parameter für die Zahlen Maskierung oder die *PrefixSize* -, *Ersatz* -und *SuffixSize* -Parameter für die Text Maskierung angeben.
Wenn der Befehl erfolgreich ausgeführt wird und Sie den *passthru* -Parameter angeben, gibt das Cmdlet ein Objekt zurück, das die Eigenschaften der Daten Maskierungs Regel und die Regelbezeichner beschreibt.
Regelbezeichner sind: **ResourceGroupName** , **Servername** , **DatabaseName** und **rule** -ID.

Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.

## Beispiele

### Beispiel 1: Ändern des Bereichs einer Daten Maskierungs Regel in einer Datenbank
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

Mit diesem Befehl wird eine Daten Maskierungs Regel geändert, die die ID Rule17.
Diese Regel wird in der Datenbank mit dem Namen Database01 auf dem Server Server01 ausgeführt.
Mit diesem Befehl werden die Begrenzungen für das Intervall geändert, in dem eine Zufallszahl als maskierter Wert generiert wird.
Der neue Bereich liegt zwischen 23 und 42.

## Parameter

### -ColumnName
Gibt den Namen der Spalte an, auf die die Maskierungs Regel ausgerichtet ist.

```yaml
Type: String
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
Type: String
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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
- E-Mail

Der Standardwert ist default.

```yaml
Type: String
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
Gibt die untere Grenze des Intervalls an, aus dem ein Zufallswert ausgewählt wird.
Geben Sie diesen Parameter nur an, wenn Sie für den *MaskingFunction* -Parameter den Wert Zahl angeben.
Der Standardwert ist 0.

```yaml
Type: Double
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
Type: Double
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
Type: SwitchParameter
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
Type: UInt32
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
Der Standardwert ist 0.

```yaml
Type: String
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
Type: String
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
Type: String
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
Type: String
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
Type: UInt32
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
Type: String
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
Type: SwitchParameter
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
Type: SwitchParameter
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

###  
Keine

## Ausgaben

### Microsoft. Azure. Commands. SQL. Security. Model. DatabaseDataMaskingRuleModel

## Notizen

## Verwandte Links

[Get-AzureRmSqlDatabaseDataMaskingRule](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[Neu – AzureRmSqlDatabaseDataMaskingRule](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[Remove-AzureRmSqlDatabaseDataMaskingRule](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[SQL-Datenbank-Dokumentation](https://docs.microsoft.com/azure/sql-database/)


