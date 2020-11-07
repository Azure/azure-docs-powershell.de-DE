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
# <span data-ttu-id="30a22-101">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="30a22-101">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="30a22-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="30a22-102">SYNOPSIS</span></span>
<span data-ttu-id="30a22-103">Legt die Eigenschaften einer Daten Maskierungs Regel für eine Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="30a22-103">Sets the properties of a data masking rule for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30a22-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="30a22-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="30a22-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="30a22-105">DESCRIPTION</span></span>
<span data-ttu-id="30a22-106">Das Cmdlet " **Set-AzureRmSqlDatabaseDataMaskingRule** " legt eine Daten Maskierungs Regel für eine Azure SQL-Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="30a22-106">The **Set-AzureRmSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="30a22-107">Um das Cmdlet zu verwenden, geben Sie die *ResourceGroupName* -, *Servername* -, *DatabaseName* -und *Rules* -Parameter an, um die Regel zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="30a22-107">To use the cmdlet, provide the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="30a22-108">Sie können einen der Parameter von Schema *Name* , *TableSchema* und *ColumnName* angeben, um die Regel erneut zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="30a22-108">You can provide any of the parameters of *SchemaName* , *TableName* , and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="30a22-109">Geben Sie den *MaskingFunction* -Parameter an, um zu ändern, wie die Daten maskiert werden.</span><span class="sxs-lookup"><span data-stu-id="30a22-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>

<span data-ttu-id="30a22-110">Wenn Sie einen Wert von Zahl oder Text für *MaskingFunction* angeben, können Sie die *NumberFrom* -und *NumberTo* -Parameter für die Zahlen Maskierung oder die *PrefixSize* -, *Ersatz* -und *SuffixSize* -Parameter für die Text Maskierung angeben.</span><span class="sxs-lookup"><span data-stu-id="30a22-110">If you specify a value of Number or Text for *MaskingFunction* , you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize* , *ReplacementString* , and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="30a22-111">Wenn der Befehl erfolgreich ausgeführt wird und Sie den *passthru* -Parameter angeben, gibt das Cmdlet ein Objekt zurück, das die Eigenschaften der Daten Maskierungs Regel und die Regelbezeichner beschreibt.</span><span class="sxs-lookup"><span data-stu-id="30a22-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="30a22-112">Regelbezeichner sind: **ResourceGroupName** , **Servername** , **DatabaseName** und **rule** -ID.</span><span class="sxs-lookup"><span data-stu-id="30a22-112">Rule identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , **DatabaseName** , and **RuleId**.</span></span>

<span data-ttu-id="30a22-113">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="30a22-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="30a22-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="30a22-114">EXAMPLES</span></span>

### <span data-ttu-id="30a22-115">Beispiel 1: Ändern des Bereichs einer Daten Maskierungs Regel in einer Datenbank</span><span class="sxs-lookup"><span data-stu-id="30a22-115">Example 1: Change the range of a data masking rule in a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="30a22-116">Mit diesem Befehl wird eine Daten Maskierungs Regel geändert, die die ID Rule17.</span><span class="sxs-lookup"><span data-stu-id="30a22-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="30a22-117">Diese Regel wird in der Datenbank mit dem Namen Database01 auf dem Server Server01 ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="30a22-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="30a22-118">Mit diesem Befehl werden die Begrenzungen für das Intervall geändert, in dem eine Zufallszahl als maskierter Wert generiert wird.</span><span class="sxs-lookup"><span data-stu-id="30a22-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="30a22-119">Der neue Bereich liegt zwischen 23 und 42.</span><span class="sxs-lookup"><span data-stu-id="30a22-119">The new range is between 23 and 42.</span></span>

## <span data-ttu-id="30a22-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="30a22-120">PARAMETERS</span></span>

### <span data-ttu-id="30a22-121">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="30a22-121">-ColumnName</span></span>
<span data-ttu-id="30a22-122">Gibt den Namen der Spalte an, auf die die Maskierungs Regel ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="30a22-122">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="30a22-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="30a22-123">-DatabaseName</span></span>
<span data-ttu-id="30a22-124">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="30a22-124">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="30a22-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30a22-125">-DefaultProfile</span></span>
<span data-ttu-id="30a22-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="30a22-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30a22-127">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="30a22-127">-MaskingFunction</span></span>
<span data-ttu-id="30a22-128">Gibt die Maskierungsfunktion an, die von der Regel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="30a22-128">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="30a22-129">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="30a22-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="30a22-130">Standard</span><span class="sxs-lookup"><span data-stu-id="30a22-130">Default</span></span>
- <span data-ttu-id="30a22-131">Nomasking</span><span class="sxs-lookup"><span data-stu-id="30a22-131">NoMasking</span></span>
- <span data-ttu-id="30a22-132">Text</span><span class="sxs-lookup"><span data-stu-id="30a22-132">Text</span></span>
- <span data-ttu-id="30a22-133">Anzahl</span><span class="sxs-lookup"><span data-stu-id="30a22-133">Number</span></span>
- <span data-ttu-id="30a22-134">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="30a22-134">SocialSecurityNumber</span></span>
- <span data-ttu-id="30a22-135">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="30a22-135">CreditCardNumber</span></span>
- <span data-ttu-id="30a22-136">E-Mail</span><span class="sxs-lookup"><span data-stu-id="30a22-136">Email</span></span>

<span data-ttu-id="30a22-137">Der Standardwert ist default.</span><span class="sxs-lookup"><span data-stu-id="30a22-137">The default value is Default.</span></span>

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

### <span data-ttu-id="30a22-138">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="30a22-138">-NumberFrom</span></span>
<span data-ttu-id="30a22-139">Gibt die untere Grenze des Intervalls an, aus dem ein Zufallswert ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="30a22-139">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="30a22-140">Geben Sie diesen Parameter nur an, wenn Sie für den *MaskingFunction* -Parameter den Wert Zahl angeben.</span><span class="sxs-lookup"><span data-stu-id="30a22-140">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="30a22-141">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="30a22-141">The default value is 0.</span></span>

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

### <span data-ttu-id="30a22-142">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="30a22-142">-NumberTo</span></span>
<span data-ttu-id="30a22-143">Gibt die Obergrenze des Intervalls an, aus dem ein Zufallswert ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="30a22-143">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="30a22-144">Geben Sie diesen Parameter nur an, wenn Sie für den *MaskingFunction* -Parameter den Wert Zahl angeben.</span><span class="sxs-lookup"><span data-stu-id="30a22-144">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="30a22-145">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="30a22-145">The default value is 0.</span></span>

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

### <span data-ttu-id="30a22-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30a22-146">-PassThru</span></span>
<span data-ttu-id="30a22-147">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="30a22-147">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="30a22-148">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="30a22-148">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="30a22-149">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="30a22-149">-PrefixSize</span></span>
<span data-ttu-id="30a22-150">Gibt die Anzahl der Zeichen am Anfang des Texts an, die nicht maskiert sind.</span><span class="sxs-lookup"><span data-stu-id="30a22-150">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="30a22-151">Geben Sie diesen Parameter nur an, wenn Sie einen Wert von Text für den *MaskingFunction* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="30a22-151">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="30a22-152">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="30a22-152">The default value is 0.</span></span>

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

### <span data-ttu-id="30a22-153">-Ersatz-Nr.</span><span class="sxs-lookup"><span data-stu-id="30a22-153">-ReplacementString</span></span>
<span data-ttu-id="30a22-154">Gibt die Anzahl der Zeichen am Ende des Texts an, die nicht maskiert sind.</span><span class="sxs-lookup"><span data-stu-id="30a22-154">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="30a22-155">Geben Sie diesen Parameter nur an, wenn Sie einen Wert von Text für den *MaskingFunction* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="30a22-155">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="30a22-156">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="30a22-156">The default value is 0.</span></span>

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

### <span data-ttu-id="30a22-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30a22-157">-ResourceGroupName</span></span>
<span data-ttu-id="30a22-158">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="30a22-158">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="30a22-159">-Schemaname</span><span class="sxs-lookup"><span data-stu-id="30a22-159">-SchemaName</span></span>
<span data-ttu-id="30a22-160">Gibt den Namen eines Schemas an.</span><span class="sxs-lookup"><span data-stu-id="30a22-160">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="30a22-161">-Servername</span><span class="sxs-lookup"><span data-stu-id="30a22-161">-ServerName</span></span>
<span data-ttu-id="30a22-162">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="30a22-162">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="30a22-163">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="30a22-163">-SuffixSize</span></span>
<span data-ttu-id="30a22-164">Gibt die Anzahl der Zeichen am Ende des Texts an, die nicht maskiert sind.</span><span class="sxs-lookup"><span data-stu-id="30a22-164">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="30a22-165">Geben Sie diesen Parameter nur an, wenn Sie einen Wert von Text für den *MaskingFunction* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="30a22-165">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="30a22-166">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="30a22-166">The default value is 0.</span></span>

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

### <span data-ttu-id="30a22-167">-Tabellenname</span><span class="sxs-lookup"><span data-stu-id="30a22-167">-TableName</span></span>
<span data-ttu-id="30a22-168">Gibt den Namen der Datenbanktabelle an, die die maskierte Spalte enthält.</span><span class="sxs-lookup"><span data-stu-id="30a22-168">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="30a22-169">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="30a22-169">-Confirm</span></span>
<span data-ttu-id="30a22-170">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="30a22-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30a22-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30a22-171">-WhatIf</span></span>
<span data-ttu-id="30a22-172">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="30a22-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30a22-173">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="30a22-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30a22-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30a22-174">CommonParameters</span></span>
<span data-ttu-id="30a22-175">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30a22-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30a22-176">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30a22-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30a22-177">Eingaben</span><span class="sxs-lookup"><span data-stu-id="30a22-177">INPUTS</span></span>

###  
<span data-ttu-id="30a22-178">Keine</span><span class="sxs-lookup"><span data-stu-id="30a22-178">None</span></span>

## <span data-ttu-id="30a22-179">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="30a22-179">OUTPUTS</span></span>

### <span data-ttu-id="30a22-180">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="30a22-180">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="30a22-181">Notizen</span><span class="sxs-lookup"><span data-stu-id="30a22-181">NOTES</span></span>

## <span data-ttu-id="30a22-182">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="30a22-182">RELATED LINKS</span></span>

[<span data-ttu-id="30a22-183">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="30a22-183">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="30a22-184">Neu – AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="30a22-184">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="30a22-185">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="30a22-185">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="30a22-186">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="30a22-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


