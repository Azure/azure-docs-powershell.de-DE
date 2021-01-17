---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 544db2f0e23cb510c81fb64898b6bcf856e760e5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458395"
---
# <span data-ttu-id="0a0f2-101">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="0a0f2-101">Set-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="0a0f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a0f2-102">SYNOPSIS</span></span>
<span data-ttu-id="0a0f2-103">Legt die Eigenschaften einer Datenmaskregel für eine Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-103">Sets the properties of a data masking rule for a database.</span></span>

## <span data-ttu-id="0a0f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0a0f2-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0a0f2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0a0f2-105">DESCRIPTION</span></span>
<span data-ttu-id="0a0f2-106">Das **Cmdlet "Set-AzSqlDatabaseDataMaskingRule"** legt eine Datenmaskierungsregel für eine Azure SQL fest.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-106">The **Set-AzSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="0a0f2-107">Um das Cmdlet zu verwenden, geben Sie die Parameter *"ResourceGroupName",* *"ServerName",* *"DatabaseName"* und *"RuleId"* zum Identifizieren der Regel an.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-107">To use the cmdlet, provide the *ResourceGroupName*, *ServerName*, *DatabaseName*, and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="0a0f2-108">Sie können beliebige Parameter von *SchemaName,* *TableName* und *ColumnName* angeben, um die Regel neu zu definieren.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-108">You can provide any of the parameters of *SchemaName*, *TableName*, and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="0a0f2-109">Geben Sie den *Parameter "MaskingFunction"* an, um die Maskierung der Daten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>
<span data-ttu-id="0a0f2-110">Wenn Sie den Wert "Number" oder "Text" für *"MaskingFunction"* angeben, können Sie die *Parameter "NumberFrom"* und *"NumberTo"* für die Zahlenformatierung oder die Parameter *"PrefixSize",* *"ReplacementString"* und *"SuffixSize"* für die Textformatierung angeben.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-110">If you specify a value of Number or Text for *MaskingFunction*, you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize*, *ReplacementString*, and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="0a0f2-111">Wenn der Befehl erfolgreich ist und Sie den Parameter *"PassThru"* angeben, gibt das Cmdlet ein Objekt zurück, das die Eigenschaften der Datenmaskierungsregel und die Regelbezeichner beschreibt.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="0a0f2-112">Regelbezeichner umfassen, sind aber nicht beschränkt auf: **ResourceGroupName,** **ServerName,** **DatabaseName** und **RuleId.**</span><span class="sxs-lookup"><span data-stu-id="0a0f2-112">Rule identifiers include, but are not limited to, **ResourceGroupName**, **ServerName**, **DatabaseName**, and **RuleId**.</span></span>
<span data-ttu-id="0a0f2-113">Dieses Cmdlet wird auch vom Dienst SQL Server Stretch Database in Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="0a0f2-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0a0f2-114">EXAMPLES</span></span>

### <span data-ttu-id="0a0f2-115">Beispiel 1: Ändern des Bereichs einer Datenmaskierungsregel in einer Datenbank</span><span class="sxs-lookup"><span data-stu-id="0a0f2-115">Example 1: Change the range of a data masking rule in a database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="0a0f2-116">Mit diesem Befehl wird eine Datenmaskregel geändert, die die ID Rule17 enthält.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="0a0f2-117">Diese Regel gilt in der Datenbank mit dem Namen "Database01" auf Server Server01.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="0a0f2-118">Mit diesem Befehl werden die Grenzen für das Intervall geändert, in dem eine Zufallszahl als maskierter Wert generiert wird.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="0a0f2-119">Der neue Bereich liegt zwischen 23 und 42.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-119">The new range is between 23 and 42.</span></span>

### <span data-ttu-id="0a0f2-120">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0a0f2-120">Example 2</span></span>

<span data-ttu-id="0a0f2-121">Legt die Eigenschaften einer Datenmaskregel für eine Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-121">Sets the properties of a data masking rule for a database.</span></span> <span data-ttu-id="0a0f2-122">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="0a0f2-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlDatabaseDataMaskingRule -ColumnName 'column1' -DatabaseName $params.databaseName -MaskingFunction NoMasking -NumberFrom 5 -NumberTo 14 -PrefixSize <UInt32> -ReplacementString <String> -ResourceGroupName $params.rgname -SchemaName 'dbo' -ServerName $params.serverName -SuffixSize <UInt32> -TableName 'table1'
```

## <span data-ttu-id="0a0f2-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a0f2-123">PARAMETERS</span></span>

### <span data-ttu-id="0a0f2-124">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="0a0f2-124">-ColumnName</span></span>
<span data-ttu-id="0a0f2-125">Gibt den Namen der Spalte an, auf die die Maskierungsregel ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-125">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="0a0f2-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0a0f2-126">-DatabaseName</span></span>
<span data-ttu-id="0a0f2-127">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-127">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="0a0f2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a0f2-128">-DefaultProfile</span></span>
<span data-ttu-id="0a0f2-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0a0f2-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a0f2-130">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="0a0f2-130">-MaskingFunction</span></span>
<span data-ttu-id="0a0f2-131">Gibt die von der Regel verwendeten Maskierungsfunktion an.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-131">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="0a0f2-132">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="0a0f2-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0a0f2-133">Standard</span><span class="sxs-lookup"><span data-stu-id="0a0f2-133">Default</span></span>
- <span data-ttu-id="0a0f2-134">NoMasking</span><span class="sxs-lookup"><span data-stu-id="0a0f2-134">NoMasking</span></span>
- <span data-ttu-id="0a0f2-135">Text</span><span class="sxs-lookup"><span data-stu-id="0a0f2-135">Text</span></span>
- <span data-ttu-id="0a0f2-136">Zahl</span><span class="sxs-lookup"><span data-stu-id="0a0f2-136">Number</span></span>
- <span data-ttu-id="0a0f2-137">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="0a0f2-137">SocialSecurityNumber</span></span>
- <span data-ttu-id="0a0f2-138">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="0a0f2-138">CreditCardNumber</span></span>
- <span data-ttu-id="0a0f2-139">E-Mail Der Standardwert ist "Standard".</span><span class="sxs-lookup"><span data-stu-id="0a0f2-139">Email The default value is Default.</span></span>

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

### <span data-ttu-id="0a0f2-140">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="0a0f2-140">-NumberFrom</span></span>
<span data-ttu-id="0a0f2-141">Gibt die untere gebundene Zahl des Intervalls an, aus dem ein Zufallswert ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-141">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="0a0f2-142">Geben Sie diesen Parameter nur an, wenn Sie für den Parameter *"MaskingFunction"* den Wert "Number" angeben.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-142">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="0a0f2-143">Der Standardwert ist "0".</span><span class="sxs-lookup"><span data-stu-id="0a0f2-143">The default value is 0.</span></span>

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

### <span data-ttu-id="0a0f2-144">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="0a0f2-144">-NumberTo</span></span>
<span data-ttu-id="0a0f2-145">Gibt die obere gebundene Zahl des Intervalls an, aus dem ein Zufallswert ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-145">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="0a0f2-146">Geben Sie diesen Parameter nur an, wenn Sie für den Parameter *"MaskingFunction"* den Wert "Number" angeben.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-146">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="0a0f2-147">Der Standardwert ist "0".</span><span class="sxs-lookup"><span data-stu-id="0a0f2-147">The default value is 0.</span></span>

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

### <span data-ttu-id="0a0f2-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a0f2-148">-PassThru</span></span>
<span data-ttu-id="0a0f2-149">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-149">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0a0f2-150">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-150">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0a0f2-151">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="0a0f2-151">-PrefixSize</span></span>
<span data-ttu-id="0a0f2-152">Gibt die Anzahl von Zeichen am Anfang des Texts an, die nicht maskiert sind.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-152">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="0a0f2-153">Geben Sie diesen Parameter nur an, wenn Sie für den Parameter *"MaskingFunction"* den Wert "Text" angeben.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-153">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="0a0f2-154">Der Standardwert ist "0".</span><span class="sxs-lookup"><span data-stu-id="0a0f2-154">The default value is 0.</span></span>

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

### <span data-ttu-id="0a0f2-155">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="0a0f2-155">-ReplacementString</span></span>
<span data-ttu-id="0a0f2-156">Gibt die Anzahl von Zeichen am Ende des Texts an, die nicht maskiert sind.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-156">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="0a0f2-157">Geben Sie diesen Parameter nur an, wenn Sie für den Parameter *"MaskingFunction"* den Wert "Text" angeben.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-157">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="0a0f2-158">Der Standardwert ist "0".</span><span class="sxs-lookup"><span data-stu-id="0a0f2-158">The default value is 0.</span></span>

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

### <span data-ttu-id="0a0f2-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a0f2-159">-ResourceGroupName</span></span>
<span data-ttu-id="0a0f2-160">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-160">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="0a0f2-161">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="0a0f2-161">-SchemaName</span></span>
<span data-ttu-id="0a0f2-162">Gibt den Namen eines Schemas an.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-162">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="0a0f2-163">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0a0f2-163">-ServerName</span></span>
<span data-ttu-id="0a0f2-164">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-164">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="0a0f2-165">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="0a0f2-165">-SuffixSize</span></span>
<span data-ttu-id="0a0f2-166">Gibt die Anzahl von Zeichen am Ende des Texts an, die nicht maskiert sind.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-166">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="0a0f2-167">Geben Sie diesen Parameter nur an, wenn Sie für den Parameter *"MaskingFunction"* den Wert "Text" angeben.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-167">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="0a0f2-168">Der Standardwert ist "0".</span><span class="sxs-lookup"><span data-stu-id="0a0f2-168">The default value is 0.</span></span>

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

### <span data-ttu-id="0a0f2-169">-TableName</span><span class="sxs-lookup"><span data-stu-id="0a0f2-169">-TableName</span></span>
<span data-ttu-id="0a0f2-170">Gibt den Namen der Datenbanktabelle an, die die maskierte Spalte enthält.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-170">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="0a0f2-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a0f2-171">-Confirm</span></span>
<span data-ttu-id="0a0f2-172">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a0f2-173">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0a0f2-173">-WhatIf</span></span>
<span data-ttu-id="0a0f2-174">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a0f2-175">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a0f2-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a0f2-176">CommonParameters</span></span>
<span data-ttu-id="0a0f2-177">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a0f2-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a0f2-178">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a0f2-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a0f2-179">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0a0f2-179">INPUTS</span></span>

### <span data-ttu-id="0a0f2-180">System.String</span><span class="sxs-lookup"><span data-stu-id="0a0f2-180">System.String</span></span>

### <span data-ttu-id="0a0f2-181">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0a0f2-181">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0a0f2-182">System.Nullable'1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0a0f2-182">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="0a0f2-183">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0a0f2-183">OUTPUTS</span></span>

### <span data-ttu-id="0a0f2-184">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="0a0f2-184">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="0a0f2-185">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0a0f2-185">NOTES</span></span>

## <span data-ttu-id="0a0f2-186">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0a0f2-186">RELATED LINKS</span></span>

[<span data-ttu-id="0a0f2-187">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="0a0f2-187">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="0a0f2-188">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="0a0f2-188">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="0a0f2-189">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="0a0f2-189">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="0a0f2-190">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="0a0f2-190">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


