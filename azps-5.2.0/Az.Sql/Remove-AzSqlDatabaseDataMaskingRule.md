---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4695AFEA-D244-4FCB-AF36-D8CDEBFB392C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 02a6090a98a80300f886e8bbbd8e2622aa7981d4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98289342"
---
# <span data-ttu-id="e653a-101">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="e653a-101">Remove-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="e653a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e653a-102">SYNOPSIS</span></span>
<span data-ttu-id="e653a-103">Entfernt eine Datenmaskregel aus einer Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e653a-103">Removes a data masking rule from a database.</span></span>

## <span data-ttu-id="e653a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e653a-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseDataMaskingRule [-PassThru] [-Force] -SchemaName <String> -TableName <String>
 -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e653a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e653a-105">DESCRIPTION</span></span>
<span data-ttu-id="e653a-106">Das **Cmdlet "Remove-AzSqlDatabaseDataMaskingRule"** entfernt eine bestimmte Datenmaskierungsregel aus einer Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e653a-106">The **Remove-AzSqlDatabaseDataMaskingRule** cmdlet removes a specific data masking rule from an Azure SQL database.</span></span>
<span data-ttu-id="e653a-107">Sie können eine Datenmaskregel entfernen, indem Sie die Parameter *"ResourceGroupName",* *"ServerName",* *"DatabaseName"* und *"RuleId"* verwenden, um die Regel zu identifizieren, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="e653a-107">You can remove a data masking rule by using the *ResourceGroupName*, *ServerName*, *DatabaseName*, and *RuleId* parameters to identify the rule that this cmdlet removes.</span></span>
<span data-ttu-id="e653a-108">Dieses Cmdlet wird auch vom Dienst SQL Server Stretch Database in Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e653a-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="e653a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e653a-109">EXAMPLES</span></span>

### <span data-ttu-id="e653a-110">Beispiel 1: Entfernen einer Regel zum Maskieren von Datenbankdaten</span><span class="sxs-lookup"><span data-stu-id="e653a-110">Example 1: Remove a database data masking rule</span></span>
```
PS C:\>Remove-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
```

<span data-ttu-id="e653a-111">Mit diesem Befehl wird "Regelname Regel01" entfernt, der für die Datenbankdatenbank01 definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e653a-111">This command removes rule name Rule01 defined for the database Database01.</span></span>
<span data-ttu-id="e653a-112">Die Datenbank befindet sich auf Server01 und ist der Ressourcengruppe "ResourceGroup01" zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="e653a-112">The database is located on Server01 and assigned to resource group ResourceGroup01.</span></span>

## <span data-ttu-id="e653a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e653a-113">PARAMETERS</span></span>

### <span data-ttu-id="e653a-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="e653a-114">-ColumnName</span></span>
<span data-ttu-id="e653a-115">Gibt den Namen der Spalte an, auf die die Maskierungsregel ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="e653a-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="e653a-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e653a-116">-DatabaseName</span></span>
<span data-ttu-id="e653a-117">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="e653a-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="e653a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e653a-118">-DefaultProfile</span></span>
<span data-ttu-id="e653a-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e653a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e653a-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e653a-120">-Force</span></span>
<span data-ttu-id="e653a-121">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="e653a-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e653a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e653a-122">-PassThru</span></span>
<span data-ttu-id="e653a-123">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="e653a-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e653a-124">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="e653a-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e653a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e653a-125">-ResourceGroupName</span></span>
<span data-ttu-id="e653a-126">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="e653a-126">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="e653a-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="e653a-127">-SchemaName</span></span>
<span data-ttu-id="e653a-128">Gibt den Namen eines Schemas an.</span><span class="sxs-lookup"><span data-stu-id="e653a-128">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="e653a-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e653a-129">-ServerName</span></span>
<span data-ttu-id="e653a-130">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="e653a-130">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="e653a-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="e653a-131">-TableName</span></span>
<span data-ttu-id="e653a-132">Gibt den Namen einer Azure SQL an.</span><span class="sxs-lookup"><span data-stu-id="e653a-132">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="e653a-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e653a-133">-Confirm</span></span>
<span data-ttu-id="e653a-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e653a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e653a-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e653a-135">-WhatIf</span></span>
<span data-ttu-id="e653a-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e653a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e653a-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e653a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e653a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e653a-138">CommonParameters</span></span>
<span data-ttu-id="e653a-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e653a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e653a-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e653a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e653a-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e653a-141">INPUTS</span></span>

### <span data-ttu-id="e653a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="e653a-142">System.String</span></span>

## <span data-ttu-id="e653a-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e653a-143">OUTPUTS</span></span>

### <span data-ttu-id="e653a-144">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="e653a-144">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="e653a-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e653a-145">NOTES</span></span>

## <span data-ttu-id="e653a-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e653a-146">RELATED LINKS</span></span>

[<span data-ttu-id="e653a-147">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="e653a-147">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="e653a-148">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="e653a-148">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="e653a-149">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="e653a-149">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="e653a-150">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="e653a-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


