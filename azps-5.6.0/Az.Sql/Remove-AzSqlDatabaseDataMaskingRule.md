---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4695AFEA-D244-4FCB-AF36-D8CDEBFB392C
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 2529057f7a2963c28175e18bacbc1aa3894a3eea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923315"
---
# <span data-ttu-id="c6110-101">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="c6110-101">Remove-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="c6110-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6110-102">SYNOPSIS</span></span>
<span data-ttu-id="c6110-103">Entfernt eine Datenformatierungsregel aus einer Datenbank.</span><span class="sxs-lookup"><span data-stu-id="c6110-103">Removes a data masking rule from a database.</span></span>

## <span data-ttu-id="c6110-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6110-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseDataMaskingRule [-PassThru] [-Force] -SchemaName <String> -TableName <String>
 -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6110-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6110-105">DESCRIPTION</span></span>
<span data-ttu-id="c6110-106">Das **Cmdlet Remove-AzSqlDatabaseDataMaskingRule** entfernt eine bestimmte Datenformatierungsregel aus einer Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="c6110-106">The **Remove-AzSqlDatabaseDataMaskingRule** cmdlet removes a specific data masking rule from an Azure SQL database.</span></span>
<span data-ttu-id="c6110-107">Sie können eine Datenformatierungsregel entfernen, indem Sie die Parameter *ResourceGroupName,* *ServerName,* *DatabaseName* und *RuleId* verwenden, um die Regel zu identifizieren, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="c6110-107">You can remove a data masking rule by using the *ResourceGroupName*, *ServerName*, *DatabaseName*, and *RuleId* parameters to identify the rule that this cmdlet removes.</span></span>
<span data-ttu-id="c6110-108">Dieses Cmdlet wird auch vom SQL Server Stretch Database Service in Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c6110-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="c6110-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c6110-109">EXAMPLES</span></span>

### <span data-ttu-id="c6110-110">Beispiel 1: Entfernen einer Regel zum Maskieren von Datenbankdaten</span><span class="sxs-lookup"><span data-stu-id="c6110-110">Example 1: Remove a database data masking rule</span></span>
```
PS C:\>Remove-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
```

<span data-ttu-id="c6110-111">Mit diesem Befehl wird der Regelname Rule01 entfernt, der für die Datenbankdatenbank01 definiert ist.</span><span class="sxs-lookup"><span data-stu-id="c6110-111">This command removes rule name Rule01 defined for the database Database01.</span></span>
<span data-ttu-id="c6110-112">Die Datenbank befindet sich auf Server01 und ist der Ressourcengruppe ResourceGroup01 zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="c6110-112">The database is located on Server01 and assigned to resource group ResourceGroup01.</span></span>

## <span data-ttu-id="c6110-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c6110-113">PARAMETERS</span></span>

### <span data-ttu-id="c6110-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="c6110-114">-ColumnName</span></span>
<span data-ttu-id="c6110-115">Gibt den Namen der Spalte an, die auf die Maskierungsregel ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="c6110-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="c6110-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c6110-116">-DatabaseName</span></span>
<span data-ttu-id="c6110-117">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="c6110-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="c6110-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6110-118">-DefaultProfile</span></span>
<span data-ttu-id="c6110-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c6110-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c6110-120">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="c6110-120">-Force</span></span>
<span data-ttu-id="c6110-121">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="c6110-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c6110-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6110-122">-PassThru</span></span>
<span data-ttu-id="c6110-123">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="c6110-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c6110-124">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="c6110-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c6110-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6110-125">-ResourceGroupName</span></span>
<span data-ttu-id="c6110-126">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="c6110-126">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="c6110-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="c6110-127">-SchemaName</span></span>
<span data-ttu-id="c6110-128">Gibt den Namen eines Schemas an.</span><span class="sxs-lookup"><span data-stu-id="c6110-128">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="c6110-129">-Servername</span><span class="sxs-lookup"><span data-stu-id="c6110-129">-ServerName</span></span>
<span data-ttu-id="c6110-130">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="c6110-130">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="c6110-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="c6110-131">-TableName</span></span>
<span data-ttu-id="c6110-132">Gibt den Namen einer Azure-SQL an.</span><span class="sxs-lookup"><span data-stu-id="c6110-132">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="c6110-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c6110-133">-Confirm</span></span>
<span data-ttu-id="c6110-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c6110-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6110-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6110-135">-WhatIf</span></span>
<span data-ttu-id="c6110-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c6110-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6110-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c6110-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6110-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6110-138">CommonParameters</span></span>
<span data-ttu-id="c6110-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6110-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6110-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6110-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6110-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c6110-141">INPUTS</span></span>

### <span data-ttu-id="c6110-142">System.String</span><span class="sxs-lookup"><span data-stu-id="c6110-142">System.String</span></span>

## <span data-ttu-id="c6110-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c6110-143">OUTPUTS</span></span>

### <span data-ttu-id="c6110-144">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="c6110-144">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="c6110-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c6110-145">NOTES</span></span>

## <span data-ttu-id="c6110-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c6110-146">RELATED LINKS</span></span>

[<span data-ttu-id="c6110-147">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="c6110-147">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="c6110-148">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="c6110-148">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="c6110-149">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="c6110-149">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="c6110-150">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="c6110-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


