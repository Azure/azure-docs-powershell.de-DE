---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 35f2bc63366a86501650af1808274a3a0403e77f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460744"
---
# <span data-ttu-id="30878-101">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="30878-101">New-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="30878-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30878-102">SYNOPSIS</span></span>
<span data-ttu-id="30878-103">Erstellt eine Datenmaskregel für eine Datenbank.</span><span class="sxs-lookup"><span data-stu-id="30878-103">Creates a data masking rule for a database.</span></span>

## <span data-ttu-id="30878-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="30878-104">SYNTAX</span></span>

```
New-AzSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>] [-ReplacementString <String>]
 [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru] -SchemaName <String>
 -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="30878-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="30878-105">DESCRIPTION</span></span>
<span data-ttu-id="30878-106">Das **Cmdlet "New-AzSqlDatabaseDataMaskingRule"** erstellt eine Datenmaskierungsregel für eine Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="30878-106">The **New-AzSqlDatabaseDataMaskingRule** cmdlet creates a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="30878-107">Verwenden Sie zum Verwenden des Cmdlets die Parameter *"ResourceGroupName",* *"ServerName"* und *"DatabaseName",* um die Regel zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="30878-107">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the rule.</span></span>
<span data-ttu-id="30878-108">Geben Sie *"TableName"* und *"ColumnName"* an, um das Ziel der Regel und den *Parameter "MaskingFunction"* anzugeben, um zu definieren, wie die Daten maskiert werden.</span><span class="sxs-lookup"><span data-stu-id="30878-108">Provide the *TableName* and *ColumnName* to specify the target of the rule and the *MaskingFunction* parameter to define how the data is masked.</span></span>
<span data-ttu-id="30878-109">Wenn *"MaskingFunction"* den Wert "Number" oder "Text" hat, können Sie die Parameter *"NumberFrom"* und *"NumberTo"* für die Zahlenformatierung oder die Parameter *"PrefixSize",* *"ReplacementString"* und *"SuffixSize"* für die Textformatierung angeben.</span><span class="sxs-lookup"><span data-stu-id="30878-109">If *MaskingFunction* has a value of Number or Text, you can specify the *NumberFrom* and *NumberTo* parameters, for number masking, or the *PrefixSize*, *ReplacementString*, and *SuffixSize* for text masking.</span></span>
<span data-ttu-id="30878-110">Wenn der Befehl erfolgreich ist und der *Parameter "PassThru"* verwendet wird, gibt das Cmdlet zusätzlich zu den Regelbezeichnern ein Objekt zurück, das die Eigenschaften der Datenmaskierungsregel beschreibt.</span><span class="sxs-lookup"><span data-stu-id="30878-110">If the command succeeds and the *PassThru* parameter is used, the cmdlet returns an object describing the data masking rule properties in addition to the rule identifiers.</span></span>
<span data-ttu-id="30878-111">Regelbezeichner umfassen, sind aber nicht beschränkt auf, *ResourceGroupName,* *ServerName,* *DatabaseName* und *RuleID.*</span><span class="sxs-lookup"><span data-stu-id="30878-111">Rule identifiers include, but are not limited to, *ResourceGroupName*, *ServerName*, *DatabaseName*, and *RuleID*.</span></span>
<span data-ttu-id="30878-112">Dieses Cmdlet wird auch vom Dienst SQL Server Stretch Database in Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="30878-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="30878-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="30878-113">EXAMPLES</span></span>

### <span data-ttu-id="30878-114">Beispiel 1: Erstellen einer Datenmaskregel für eine Zahlenspalte in einer Datenbank</span><span class="sxs-lookup"><span data-stu-id="30878-114">Example 1: Create a data masking rule for a number column in a database</span></span>
```
PS C:\>New-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"  -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

<span data-ttu-id="30878-115">Mit diesem Befehl wird eine Datenmaskregel für die Spalte "Column01" in der Tabelle namens "Table01" im Schema "Schema01" erstellt.</span><span class="sxs-lookup"><span data-stu-id="30878-115">This command creates a data masking rule for the column named Column01 in the table named Table01 in the schema named Schema01.</span></span>
<span data-ttu-id="30878-116">Die Datenbank namens "Datenbank01" enthält alle diese Elemente.</span><span class="sxs-lookup"><span data-stu-id="30878-116">The database named Database01 contains all these items.</span></span>
<span data-ttu-id="30878-117">Bei der Regel handelt es sich um eine Zahlenformatregel, bei der eine Zufallszahl zwischen 5 und 14 als Maskenwert verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="30878-117">The rule is a number masking rule that uses a random number between 5 and 14 as the mask value.</span></span>

## <span data-ttu-id="30878-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30878-118">PARAMETERS</span></span>

### <span data-ttu-id="30878-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="30878-119">-ColumnName</span></span>
<span data-ttu-id="30878-120">Gibt den Namen der Spalte an, auf die die Maskierungsregel ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="30878-120">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="30878-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="30878-121">-DatabaseName</span></span>
<span data-ttu-id="30878-122">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="30878-122">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="30878-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30878-123">-DefaultProfile</span></span>
<span data-ttu-id="30878-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="30878-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30878-125">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="30878-125">-MaskingFunction</span></span>
<span data-ttu-id="30878-126">Gibt die von der Regel verwendeten Maskierungsfunktion an.</span><span class="sxs-lookup"><span data-stu-id="30878-126">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="30878-127">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="30878-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="30878-128">Standard</span><span class="sxs-lookup"><span data-stu-id="30878-128">Default</span></span>
- <span data-ttu-id="30878-129">NoMasking</span><span class="sxs-lookup"><span data-stu-id="30878-129">NoMasking</span></span>
- <span data-ttu-id="30878-130">Text</span><span class="sxs-lookup"><span data-stu-id="30878-130">Text</span></span>
- <span data-ttu-id="30878-131">Zahl</span><span class="sxs-lookup"><span data-stu-id="30878-131">Number</span></span>
- <span data-ttu-id="30878-132">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="30878-132">SocialSecurityNumber</span></span>
- <span data-ttu-id="30878-133">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="30878-133">CreditCardNumber</span></span>
- <span data-ttu-id="30878-134">E-Mail Der Standardwert ist "Standard".</span><span class="sxs-lookup"><span data-stu-id="30878-134">Email The default value is Default.</span></span>

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

### <span data-ttu-id="30878-135">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="30878-135">-NumberFrom</span></span>
<span data-ttu-id="30878-136">Gibt die untere gebundene Zahl des Intervalls an, aus dem ein Zufallswert ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="30878-136">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="30878-137">Geben Sie diesen Parameter nur an, wenn Sie für den Parameter *"MaskingFunction"* den Wert "Number" angeben.</span><span class="sxs-lookup"><span data-stu-id="30878-137">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="30878-138">Der Standardwert ist "0".</span><span class="sxs-lookup"><span data-stu-id="30878-138">The default value is 0.</span></span>

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

### <span data-ttu-id="30878-139">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="30878-139">-NumberTo</span></span>
<span data-ttu-id="30878-140">Gibt die obere gebundene Zahl des Intervalls an, aus dem ein Zufallswert ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="30878-140">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="30878-141">Geben Sie diesen Parameter nur an, wenn Sie für den Parameter *"MaskingFunction"* den Wert "Number" angeben.</span><span class="sxs-lookup"><span data-stu-id="30878-141">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="30878-142">Der Standardwert ist "0".</span><span class="sxs-lookup"><span data-stu-id="30878-142">The default value is 0.</span></span>

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

### <span data-ttu-id="30878-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30878-143">-PassThru</span></span>
<span data-ttu-id="30878-144">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="30878-144">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="30878-145">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="30878-145">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="30878-146">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="30878-146">-PrefixSize</span></span>
<span data-ttu-id="30878-147">Gibt die Anzahl von Zeichen am Anfang des Texts an, die nicht maskiert sind.</span><span class="sxs-lookup"><span data-stu-id="30878-147">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="30878-148">Geben Sie diesen Parameter nur an, wenn Sie für den Parameter *"MaskingFunction"* den Wert "Text" angeben.</span><span class="sxs-lookup"><span data-stu-id="30878-148">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="30878-149">Der Standardwert ist "0".</span><span class="sxs-lookup"><span data-stu-id="30878-149">The default value is 0.</span></span>

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

### <span data-ttu-id="30878-150">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="30878-150">-ReplacementString</span></span>
<span data-ttu-id="30878-151">Gibt die Anzahl von Zeichen am Ende des Texts an, die nicht maskiert sind.</span><span class="sxs-lookup"><span data-stu-id="30878-151">Specifies the number of characters in the end of the text that are not masked.</span></span>
<span data-ttu-id="30878-152">Geben Sie diesen Parameter nur an, wenn Sie für den Parameter *"MaskingFunction"* den Wert "Text" angeben.</span><span class="sxs-lookup"><span data-stu-id="30878-152">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="30878-153">Der Standardwert ist eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="30878-153">The default value is an empty string.</span></span>

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

### <span data-ttu-id="30878-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30878-154">-ResourceGroupName</span></span>
<span data-ttu-id="30878-155">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="30878-155">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="30878-156">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="30878-156">-SchemaName</span></span>
<span data-ttu-id="30878-157">Gibt den Namen eines Schemas an.</span><span class="sxs-lookup"><span data-stu-id="30878-157">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="30878-158">-ServerName</span><span class="sxs-lookup"><span data-stu-id="30878-158">-ServerName</span></span>
<span data-ttu-id="30878-159">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="30878-159">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="30878-160">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="30878-160">-SuffixSize</span></span>
<span data-ttu-id="30878-161">Gibt die Anzahl von Zeichen am Ende des Texts an, die nicht maskiert sind.</span><span class="sxs-lookup"><span data-stu-id="30878-161">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="30878-162">Geben Sie diesen Parameter nur an, wenn Sie für den Parameter *"MaskingFunction"* den Wert "Text" angeben.</span><span class="sxs-lookup"><span data-stu-id="30878-162">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="30878-163">Der Standardwert ist "0".</span><span class="sxs-lookup"><span data-stu-id="30878-163">The default value is 0.</span></span>

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

### <span data-ttu-id="30878-164">-TableName</span><span class="sxs-lookup"><span data-stu-id="30878-164">-TableName</span></span>
<span data-ttu-id="30878-165">Gibt den Namen der Datenbanktabelle an, die die maskierte Spalte enthält.</span><span class="sxs-lookup"><span data-stu-id="30878-165">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="30878-166">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30878-166">-Confirm</span></span>
<span data-ttu-id="30878-167">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="30878-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30878-168">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="30878-168">-WhatIf</span></span>
<span data-ttu-id="30878-169">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="30878-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30878-170">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="30878-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30878-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30878-171">CommonParameters</span></span>
<span data-ttu-id="30878-172">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30878-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30878-173">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30878-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30878-174">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="30878-174">INPUTS</span></span>

### <span data-ttu-id="30878-175">System.String</span><span class="sxs-lookup"><span data-stu-id="30878-175">System.String</span></span>

### <span data-ttu-id="30878-176">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="30878-176">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="30878-177">System.Nullable'1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="30878-177">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="30878-178">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="30878-178">OUTPUTS</span></span>

### <span data-ttu-id="30878-179">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="30878-179">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="30878-180">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="30878-180">NOTES</span></span>

## <span data-ttu-id="30878-181">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="30878-181">RELATED LINKS</span></span>

[<span data-ttu-id="30878-182">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="30878-182">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="30878-183">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="30878-183">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="30878-184">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="30878-184">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="30878-185">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="30878-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


