---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 69e59580d5ada03400420788169bba18d2f30444
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502862"
---
# <span data-ttu-id="3585b-101">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="3585b-101">New-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="3585b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3585b-102">SYNOPSIS</span></span>
<span data-ttu-id="3585b-103">Erstellt eine Daten Maskierungs Regel für eine Datenbank.</span><span class="sxs-lookup"><span data-stu-id="3585b-103">Creates a data masking rule for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3585b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3585b-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3585b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3585b-105">DESCRIPTION</span></span>
<span data-ttu-id="3585b-106">Das Cmdlet **New-AzureRmSqlDatabaseDataMaskingRule** erstellt eine Daten Maskierungs Regel für eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="3585b-106">The **New-AzureRmSqlDatabaseDataMaskingRule** cmdlet creates a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="3585b-107">Um das Cmdlet zu verwenden, verwenden Sie die *ResourceGroupName* -, *Servername* -, *DatabaseName* -und *Rules* -Parameter, um die Regel zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="3585b-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="3585b-108">Geben Sie den *Namen* und *ColumnName* an, um das Ziel der Regel und den *MaskingFunction* -Parameter anzugeben, um zu definieren, wie die Daten maskiert werden.</span><span class="sxs-lookup"><span data-stu-id="3585b-108">Provide the *TableName* and *ColumnName* to specify the target of the rule and the *MaskingFunction* parameter to define how the data is masked.</span></span>
<span data-ttu-id="3585b-109">Wenn *MaskingFunction* den Wert "Zahl" oder "Text" aufweist, können Sie die *NumberFrom* -und *NumberTo* -Parameter für die Maskierung von Zahlen oder die *PrefixSize* -, *Ersatz* -und *SuffixSize* für die Text Maskierung angeben.</span><span class="sxs-lookup"><span data-stu-id="3585b-109">If *MaskingFunction* has a value of Number or Text, you can specify the *NumberFrom* and *NumberTo* parameters, for number masking, or the *PrefixSize* , *ReplacementString* , and *SuffixSize* for text masking.</span></span>
<span data-ttu-id="3585b-110">Wenn der Befehl erfolgreich ausgeführt wird und der *passthru* -Parameter verwendet wird, gibt das Cmdlet zusätzlich zu den Regel Bezeichnern ein Objekt zurück, das die Eigenschaften der Daten Maskierungs Regel beschreibt.</span><span class="sxs-lookup"><span data-stu-id="3585b-110">If the command succeeds and the *PassThru* parameter is used, the cmdlet returns an object describing the data masking rule properties in addition to the rule identifiers.</span></span>
<span data-ttu-id="3585b-111">Regelbezeichner sind: *ResourceGroupName* , *Servername* , *DatabaseName* und *rule* -ID.</span><span class="sxs-lookup"><span data-stu-id="3585b-111">Rule identifiers include, but are not limited to, *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleID*.</span></span>
<span data-ttu-id="3585b-112">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3585b-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="3585b-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3585b-113">EXAMPLES</span></span>

### <span data-ttu-id="3585b-114">Beispiel 1: Erstellen einer Daten Maskierungs Regel für eine Zahlenspalte in einer Datenbank</span><span class="sxs-lookup"><span data-stu-id="3585b-114">Example 1: Create a data masking rule for a number column in a database</span></span>
```
PS C:\>New-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RuleId "Rule01" -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

<span data-ttu-id="3585b-115">Dieser Befehl erstellt eine Daten Maskierungs Regel für die Spalte mit dem Namen Column01 in der Tabelle mit dem Namen Table01 im Schema mit dem Namen Schema01.</span><span class="sxs-lookup"><span data-stu-id="3585b-115">This command creates a data masking rule for the column named Column01 in the table named Table01 in the schema named Schema01.</span></span>
<span data-ttu-id="3585b-116">Die Datenbank mit dem Namen database01 enthält alle diese Elemente.</span><span class="sxs-lookup"><span data-stu-id="3585b-116">The database named Database01 contains all these items.</span></span>
<span data-ttu-id="3585b-117">Bei der Regel handelt es sich um eine Zahlen Maskierungs Regel, die eine Zufallszahl zwischen 5 und 14 als Maskenwert verwendet.</span><span class="sxs-lookup"><span data-stu-id="3585b-117">The rule is a number masking rule that uses a random number between 5 and 14 as the mask value.</span></span>
<span data-ttu-id="3585b-118">Die Regel hat den Namen Rule01.</span><span class="sxs-lookup"><span data-stu-id="3585b-118">The rule is named Rule01.</span></span>

## <span data-ttu-id="3585b-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="3585b-119">PARAMETERS</span></span>

### <span data-ttu-id="3585b-120">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="3585b-120">-ColumnName</span></span>
<span data-ttu-id="3585b-121">Gibt den Namen der Spalte an, auf die die Maskierungs Regel ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="3585b-121">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="3585b-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3585b-122">-DatabaseName</span></span>
<span data-ttu-id="3585b-123">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="3585b-123">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="3585b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3585b-124">-DefaultProfile</span></span>
<span data-ttu-id="3585b-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3585b-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3585b-126">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="3585b-126">-MaskingFunction</span></span>
<span data-ttu-id="3585b-127">Gibt die Maskierungsfunktion an, die von der Regel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3585b-127">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="3585b-128">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3585b-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3585b-129">Standard</span><span class="sxs-lookup"><span data-stu-id="3585b-129">Default</span></span>
- <span data-ttu-id="3585b-130">Nomasking</span><span class="sxs-lookup"><span data-stu-id="3585b-130">NoMasking</span></span>
- <span data-ttu-id="3585b-131">Text</span><span class="sxs-lookup"><span data-stu-id="3585b-131">Text</span></span>
- <span data-ttu-id="3585b-132">Anzahl</span><span class="sxs-lookup"><span data-stu-id="3585b-132">Number</span></span>
- <span data-ttu-id="3585b-133">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="3585b-133">SocialSecurityNumber</span></span>
- <span data-ttu-id="3585b-134">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="3585b-134">CreditCardNumber</span></span>
- <span data-ttu-id="3585b-135">E-Mail der Standardwert ist Standard.</span><span class="sxs-lookup"><span data-stu-id="3585b-135">Email The default value is Default.</span></span>

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

### <span data-ttu-id="3585b-136">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="3585b-136">-NumberFrom</span></span>
<span data-ttu-id="3585b-137">Gibt die untere Grenze des Intervalls an, aus dem ein Zufallswert ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="3585b-137">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="3585b-138">Geben Sie diesen Parameter nur an, wenn Sie für den *MaskingFunction* -Parameter den Wert Zahl angeben.</span><span class="sxs-lookup"><span data-stu-id="3585b-138">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="3585b-139">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="3585b-139">The default value is 0.</span></span>

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

### <span data-ttu-id="3585b-140">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="3585b-140">-NumberTo</span></span>
<span data-ttu-id="3585b-141">Gibt die Obergrenze des Intervalls an, aus dem ein Zufallswert ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="3585b-141">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="3585b-142">Geben Sie diesen Parameter nur an, wenn Sie für den *MaskingFunction* -Parameter den Wert Zahl angeben.</span><span class="sxs-lookup"><span data-stu-id="3585b-142">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="3585b-143">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="3585b-143">The default value is 0.</span></span>

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

### <span data-ttu-id="3585b-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3585b-144">-PassThru</span></span>
<span data-ttu-id="3585b-145">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="3585b-145">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3585b-146">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="3585b-146">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3585b-147">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="3585b-147">-PrefixSize</span></span>
<span data-ttu-id="3585b-148">Gibt die Anzahl der Zeichen am Anfang des Texts an, die nicht maskiert sind.</span><span class="sxs-lookup"><span data-stu-id="3585b-148">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="3585b-149">Geben Sie diesen Parameter nur an, wenn Sie einen Wert von Text für den *MaskingFunction* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="3585b-149">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="3585b-150">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="3585b-150">The default value is 0.</span></span>

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

### <span data-ttu-id="3585b-151">-Ersatz-Nr.</span><span class="sxs-lookup"><span data-stu-id="3585b-151">-ReplacementString</span></span>
<span data-ttu-id="3585b-152">Gibt die Anzahl der Zeichen am Ende des Texts an, die nicht maskiert sind.</span><span class="sxs-lookup"><span data-stu-id="3585b-152">Specifies the number of characters in the end of the text that are not masked.</span></span>
<span data-ttu-id="3585b-153">Geben Sie diesen Parameter nur an, wenn Sie einen Wert von Text für den *MaskingFunction* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="3585b-153">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="3585b-154">Der Standardwert ist eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="3585b-154">The default value is an empty string.</span></span>

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

### <span data-ttu-id="3585b-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3585b-155">-ResourceGroupName</span></span>
<span data-ttu-id="3585b-156">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="3585b-156">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="3585b-157">-Schemaname</span><span class="sxs-lookup"><span data-stu-id="3585b-157">-SchemaName</span></span>
<span data-ttu-id="3585b-158">Gibt den Namen eines Schemas an.</span><span class="sxs-lookup"><span data-stu-id="3585b-158">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="3585b-159">-Servername</span><span class="sxs-lookup"><span data-stu-id="3585b-159">-ServerName</span></span>
<span data-ttu-id="3585b-160">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="3585b-160">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="3585b-161">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="3585b-161">-SuffixSize</span></span>
<span data-ttu-id="3585b-162">Gibt die Anzahl der Zeichen am Ende des Texts an, die nicht maskiert sind.</span><span class="sxs-lookup"><span data-stu-id="3585b-162">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="3585b-163">Geben Sie diesen Parameter nur an, wenn Sie einen Wert von Text für den *MaskingFunction* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="3585b-163">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="3585b-164">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="3585b-164">The default value is 0.</span></span>

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

### <span data-ttu-id="3585b-165">-Tabellenname</span><span class="sxs-lookup"><span data-stu-id="3585b-165">-TableName</span></span>
<span data-ttu-id="3585b-166">Gibt den Namen der Datenbanktabelle an, die die maskierte Spalte enthält.</span><span class="sxs-lookup"><span data-stu-id="3585b-166">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="3585b-167">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3585b-167">-Confirm</span></span>
<span data-ttu-id="3585b-168">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3585b-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3585b-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3585b-169">-WhatIf</span></span>
<span data-ttu-id="3585b-170">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3585b-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3585b-171">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3585b-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3585b-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3585b-172">CommonParameters</span></span>
<span data-ttu-id="3585b-173">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3585b-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3585b-174">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3585b-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3585b-175">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3585b-175">INPUTS</span></span>

### <span data-ttu-id="3585b-176">System. String</span><span class="sxs-lookup"><span data-stu-id="3585b-176">System.String</span></span>

### <span data-ttu-id="3585b-177">System. Nullable ' 1 [[System. UInt32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="3585b-177">System.Nullable\`1[[System.UInt32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="3585b-178">System. Nullable ' 1 [[System. Double, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="3585b-178">System.Nullable\`1[[System.Double, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="3585b-179">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3585b-179">OUTPUTS</span></span>

### <span data-ttu-id="3585b-180">Microsoft. Azure. Commands. SQL. datamasking. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="3585b-180">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="3585b-181">Notizen</span><span class="sxs-lookup"><span data-stu-id="3585b-181">NOTES</span></span>

## <span data-ttu-id="3585b-182">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3585b-182">RELATED LINKS</span></span>

[<span data-ttu-id="3585b-183">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="3585b-183">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="3585b-184">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="3585b-184">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="3585b-185">Satz-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="3585b-185">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="3585b-186">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="3585b-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


