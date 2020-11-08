---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 544db2f0e23cb510c81fb64898b6bcf856e760e5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174091"
---
# <span data-ttu-id="b2565-101">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="b2565-101">Set-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="b2565-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b2565-102">SYNOPSIS</span></span>
<span data-ttu-id="b2565-103">Legt die Eigenschaften einer Daten Maskierungs Regel für eine Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="b2565-103">Sets the properties of a data masking rule for a database.</span></span>

## <span data-ttu-id="b2565-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2565-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b2565-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2565-105">DESCRIPTION</span></span>
<span data-ttu-id="b2565-106">Das Cmdlet " **Set-AzSqlDatabaseDataMaskingRule** " legt eine Daten Maskierungs Regel für eine Azure SQL-Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="b2565-106">The **Set-AzSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="b2565-107">Um das Cmdlet zu verwenden, geben Sie die *ResourceGroupName* -, *Servername* -, *DatabaseName* -und *Rules* -Parameter an, um die Regel zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b2565-107">To use the cmdlet, provide the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="b2565-108">Sie können einen der Parameter von Schema *Name* , *TableSchema* und *ColumnName* angeben, um die Regel erneut zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="b2565-108">You can provide any of the parameters of *SchemaName* , *TableName* , and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="b2565-109">Geben Sie den *MaskingFunction* -Parameter an, um zu ändern, wie die Daten maskiert werden.</span><span class="sxs-lookup"><span data-stu-id="b2565-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>
<span data-ttu-id="b2565-110">Wenn Sie einen Wert von Zahl oder Text für *MaskingFunction* angeben, können Sie die *NumberFrom* -und *NumberTo* -Parameter für die Zahlen Maskierung oder die *PrefixSize* -, *Ersatz* -und *SuffixSize* -Parameter für die Text Maskierung angeben.</span><span class="sxs-lookup"><span data-stu-id="b2565-110">If you specify a value of Number or Text for *MaskingFunction* , you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize* , *ReplacementString* , and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="b2565-111">Wenn der Befehl erfolgreich ausgeführt wird und Sie den *passthru* -Parameter angeben, gibt das Cmdlet ein Objekt zurück, das die Eigenschaften der Daten Maskierungs Regel und die Regelbezeichner beschreibt.</span><span class="sxs-lookup"><span data-stu-id="b2565-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="b2565-112">Regelbezeichner sind: **ResourceGroupName** , **Servername** , **DatabaseName** und **rule** -ID.</span><span class="sxs-lookup"><span data-stu-id="b2565-112">Rule identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , **DatabaseName** , and **RuleId**.</span></span>
<span data-ttu-id="b2565-113">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b2565-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="b2565-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b2565-114">EXAMPLES</span></span>

### <span data-ttu-id="b2565-115">Beispiel 1: Ändern des Bereichs einer Daten Maskierungs Regel in einer Datenbank</span><span class="sxs-lookup"><span data-stu-id="b2565-115">Example 1: Change the range of a data masking rule in a database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="b2565-116">Mit diesem Befehl wird eine Daten Maskierungs Regel geändert, die die ID Rule17.</span><span class="sxs-lookup"><span data-stu-id="b2565-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="b2565-117">Diese Regel wird in der Datenbank mit dem Namen Database01 auf dem Server Server01 ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2565-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="b2565-118">Mit diesem Befehl werden die Begrenzungen für das Intervall geändert, in dem eine Zufallszahl als maskierter Wert generiert wird.</span><span class="sxs-lookup"><span data-stu-id="b2565-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="b2565-119">Der neue Bereich liegt zwischen 23 und 42.</span><span class="sxs-lookup"><span data-stu-id="b2565-119">The new range is between 23 and 42.</span></span>

### <span data-ttu-id="b2565-120">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b2565-120">Example 2</span></span>

<span data-ttu-id="b2565-121">Legt die Eigenschaften einer Daten Maskierungs Regel für eine Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="b2565-121">Sets the properties of a data masking rule for a database.</span></span> <span data-ttu-id="b2565-122">automatisch</span><span class="sxs-lookup"><span data-stu-id="b2565-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlDatabaseDataMaskingRule -ColumnName 'column1' -DatabaseName $params.databaseName -MaskingFunction NoMasking -NumberFrom 5 -NumberTo 14 -PrefixSize <UInt32> -ReplacementString <String> -ResourceGroupName $params.rgname -SchemaName 'dbo' -ServerName $params.serverName -SuffixSize <UInt32> -TableName 'table1'
```

## <span data-ttu-id="b2565-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2565-123">PARAMETERS</span></span>

### <span data-ttu-id="b2565-124">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="b2565-124">-ColumnName</span></span>
<span data-ttu-id="b2565-125">Gibt den Namen der Spalte an, auf die die Maskierungs Regel ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="b2565-125">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="b2565-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b2565-126">-DatabaseName</span></span>
<span data-ttu-id="b2565-127">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="b2565-127">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="b2565-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2565-128">-DefaultProfile</span></span>
<span data-ttu-id="b2565-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b2565-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2565-130">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="b2565-130">-MaskingFunction</span></span>
<span data-ttu-id="b2565-131">Gibt die Maskierungsfunktion an, die von der Regel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b2565-131">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="b2565-132">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b2565-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b2565-133">Standard</span><span class="sxs-lookup"><span data-stu-id="b2565-133">Default</span></span>
- <span data-ttu-id="b2565-134">Nomasking</span><span class="sxs-lookup"><span data-stu-id="b2565-134">NoMasking</span></span>
- <span data-ttu-id="b2565-135">Text</span><span class="sxs-lookup"><span data-stu-id="b2565-135">Text</span></span>
- <span data-ttu-id="b2565-136">Anzahl</span><span class="sxs-lookup"><span data-stu-id="b2565-136">Number</span></span>
- <span data-ttu-id="b2565-137">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="b2565-137">SocialSecurityNumber</span></span>
- <span data-ttu-id="b2565-138">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="b2565-138">CreditCardNumber</span></span>
- <span data-ttu-id="b2565-139">E-Mail der Standardwert ist Standard.</span><span class="sxs-lookup"><span data-stu-id="b2565-139">Email The default value is Default.</span></span>

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

### <span data-ttu-id="b2565-140">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="b2565-140">-NumberFrom</span></span>
<span data-ttu-id="b2565-141">Gibt die untere Grenze des Intervalls an, aus dem ein Zufallswert ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="b2565-141">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="b2565-142">Geben Sie diesen Parameter nur an, wenn Sie für den *MaskingFunction* -Parameter den Wert Zahl angeben.</span><span class="sxs-lookup"><span data-stu-id="b2565-142">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="b2565-143">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="b2565-143">The default value is 0.</span></span>

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

### <span data-ttu-id="b2565-144">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="b2565-144">-NumberTo</span></span>
<span data-ttu-id="b2565-145">Gibt die Obergrenze des Intervalls an, aus dem ein Zufallswert ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="b2565-145">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="b2565-146">Geben Sie diesen Parameter nur an, wenn Sie für den *MaskingFunction* -Parameter den Wert Zahl angeben.</span><span class="sxs-lookup"><span data-stu-id="b2565-146">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="b2565-147">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="b2565-147">The default value is 0.</span></span>

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

### <span data-ttu-id="b2565-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2565-148">-PassThru</span></span>
<span data-ttu-id="b2565-149">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="b2565-149">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b2565-150">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="b2565-150">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b2565-151">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="b2565-151">-PrefixSize</span></span>
<span data-ttu-id="b2565-152">Gibt die Anzahl der Zeichen am Anfang des Texts an, die nicht maskiert sind.</span><span class="sxs-lookup"><span data-stu-id="b2565-152">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="b2565-153">Geben Sie diesen Parameter nur an, wenn Sie einen Wert von Text für den *MaskingFunction* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="b2565-153">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="b2565-154">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="b2565-154">The default value is 0.</span></span>

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

### <span data-ttu-id="b2565-155">-Ersatz-Nr.</span><span class="sxs-lookup"><span data-stu-id="b2565-155">-ReplacementString</span></span>
<span data-ttu-id="b2565-156">Gibt die Anzahl der Zeichen am Ende des Texts an, die nicht maskiert sind.</span><span class="sxs-lookup"><span data-stu-id="b2565-156">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="b2565-157">Geben Sie diesen Parameter nur an, wenn Sie einen Wert von Text für den *MaskingFunction* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="b2565-157">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="b2565-158">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="b2565-158">The default value is 0.</span></span>

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

### <span data-ttu-id="b2565-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2565-159">-ResourceGroupName</span></span>
<span data-ttu-id="b2565-160">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="b2565-160">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="b2565-161">-Schemaname</span><span class="sxs-lookup"><span data-stu-id="b2565-161">-SchemaName</span></span>
<span data-ttu-id="b2565-162">Gibt den Namen eines Schemas an.</span><span class="sxs-lookup"><span data-stu-id="b2565-162">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="b2565-163">-Servername</span><span class="sxs-lookup"><span data-stu-id="b2565-163">-ServerName</span></span>
<span data-ttu-id="b2565-164">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="b2565-164">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="b2565-165">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="b2565-165">-SuffixSize</span></span>
<span data-ttu-id="b2565-166">Gibt die Anzahl der Zeichen am Ende des Texts an, die nicht maskiert sind.</span><span class="sxs-lookup"><span data-stu-id="b2565-166">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="b2565-167">Geben Sie diesen Parameter nur an, wenn Sie einen Wert von Text für den *MaskingFunction* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="b2565-167">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="b2565-168">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="b2565-168">The default value is 0.</span></span>

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

### <span data-ttu-id="b2565-169">-Tabellenname</span><span class="sxs-lookup"><span data-stu-id="b2565-169">-TableName</span></span>
<span data-ttu-id="b2565-170">Gibt den Namen der Datenbanktabelle an, die die maskierte Spalte enthält.</span><span class="sxs-lookup"><span data-stu-id="b2565-170">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="b2565-171">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b2565-171">-Confirm</span></span>
<span data-ttu-id="b2565-172">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b2565-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2565-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2565-173">-WhatIf</span></span>
<span data-ttu-id="b2565-174">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b2565-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2565-175">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2565-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2565-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2565-176">CommonParameters</span></span>
<span data-ttu-id="b2565-177">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2565-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2565-178">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2565-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2565-179">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b2565-179">INPUTS</span></span>

### <span data-ttu-id="b2565-180">System. String</span><span class="sxs-lookup"><span data-stu-id="b2565-180">System.String</span></span>

### <span data-ttu-id="b2565-181">System. Nullable ' 1 [[System. UInt32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b2565-181">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b2565-182">System. Nullable ' 1 [[System. Double, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b2565-182">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="b2565-183">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b2565-183">OUTPUTS</span></span>

### <span data-ttu-id="b2565-184">Microsoft. Azure. Commands. SQL. datamasking. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="b2565-184">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="b2565-185">Notizen</span><span class="sxs-lookup"><span data-stu-id="b2565-185">NOTES</span></span>

## <span data-ttu-id="b2565-186">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b2565-186">RELATED LINKS</span></span>

[<span data-ttu-id="b2565-187">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="b2565-187">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="b2565-188">Neu – AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="b2565-188">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="b2565-189">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="b2565-189">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="b2565-190">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="b2565-190">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


