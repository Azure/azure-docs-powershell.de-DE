---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 848A6972-AB29-46FB-8E03-FF2ADB113A0E
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: ab6bdaac71e13cfe62c054c5dbc01686760505ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926352"
---
# <span data-ttu-id="8f4b9-101">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="8f4b9-101">Get-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="8f4b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f4b9-102">SYNOPSIS</span></span>
<span data-ttu-id="8f4b9-103">Ruft die Datenformatierungsregeln aus einer Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="8f4b9-103">Gets the data masking rules from a database.</span></span>

## <span data-ttu-id="8f4b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f4b9-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingRule [-SchemaName <String>] [-TableName <String>] [-ColumnName <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f4b9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f4b9-105">DESCRIPTION</span></span>
<span data-ttu-id="8f4b9-106">Das **Get-AzSqlDatabaseDataMaskingRule-Cmdlet** ruft entweder eine bestimmte Datenformatierungsregel oder alle Datenformatierungsregeln für eine Azure SQL ab.</span><span class="sxs-lookup"><span data-stu-id="8f4b9-106">The **Get-AzSqlDatabaseDataMaskingRule** cmdlet gets either a specific data masking rule or all of the data masking rules for an Azure SQL database.</span></span>
<span data-ttu-id="8f4b9-107">Um das Cmdlet zu verwenden, verwenden Sie die *Parameter ResourceGroupName,* *ServerName* und *DatabaseName,* um die Datenbank zu identifizieren, und geben Sie mit dem Parameter *RuleId* an, welche Regel dieses Cmdlet zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="8f4b9-107">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database, and the *RuleId* parameter to specify which rule this cmdlet returns.</span></span>
<span data-ttu-id="8f4b9-108">Wenn Sie RuleId nicht *bereitstellen,* werden alle Datenformatierungsregeln für diese Azure SQL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8f4b9-108">If you do not provide *RuleId*, all the data masking rules for that Azure SQL database are returned.</span></span>
<span data-ttu-id="8f4b9-109">Dieses Cmdlet wird auch vom SQL Server Stretch Database Service in Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8f4b9-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="8f4b9-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8f4b9-110">EXAMPLES</span></span>

### <span data-ttu-id="8f4b9-111">Beispiel 1: Alle Datenformatierungsregeln aus einer Datenbank erhalten</span><span class="sxs-lookup"><span data-stu-id="8f4b9-111">Example 1: Get all data masking rules from a database</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table1
ColumnName        : column1
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :

DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table2
ColumnName        : column2
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :
```

### <span data-ttu-id="8f4b9-112">Beispiel 2: Die Datenformatierungsregel wird in Schema "dbo", Tabelle "Tabelle1" und Spalte "Spalte1" definiert.</span><span class="sxs-lookup"><span data-stu-id="8f4b9-112">Example 2: Get the data masking rule defined on schema "dbo", table "table1" and column "column1".</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table1
ColumnName        : column1
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :
```

## <span data-ttu-id="8f4b9-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8f4b9-113">PARAMETERS</span></span>

### <span data-ttu-id="8f4b9-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="8f4b9-114">-ColumnName</span></span>
<span data-ttu-id="8f4b9-115">Gibt den Namen der Spalte an, die auf die Maskierungsregel ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="8f4b9-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="8f4b9-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8f4b9-116">-DatabaseName</span></span>
<span data-ttu-id="8f4b9-117">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="8f4b9-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="8f4b9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f4b9-118">-DefaultProfile</span></span>
<span data-ttu-id="8f4b9-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="8f4b9-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f4b9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f4b9-120">-ResourceGroupName</span></span>
<span data-ttu-id="8f4b9-121">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="8f4b9-121">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="8f4b9-122">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="8f4b9-122">-SchemaName</span></span>
<span data-ttu-id="8f4b9-123">Gibt den Namen eines Schemas an.</span><span class="sxs-lookup"><span data-stu-id="8f4b9-123">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="8f4b9-124">-Servername</span><span class="sxs-lookup"><span data-stu-id="8f4b9-124">-ServerName</span></span>
<span data-ttu-id="8f4b9-125">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="8f4b9-125">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="8f4b9-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="8f4b9-126">-TableName</span></span>
<span data-ttu-id="8f4b9-127">Gibt den Namen einer Azure-SQL an.</span><span class="sxs-lookup"><span data-stu-id="8f4b9-127">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="8f4b9-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8f4b9-128">-Confirm</span></span>
<span data-ttu-id="8f4b9-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8f4b9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f4b9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f4b9-130">-WhatIf</span></span>
<span data-ttu-id="8f4b9-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8f4b9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f4b9-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8f4b9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f4b9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f4b9-133">CommonParameters</span></span>
<span data-ttu-id="8f4b9-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f4b9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f4b9-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f4b9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f4b9-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8f4b9-136">INPUTS</span></span>

### <span data-ttu-id="8f4b9-137">System.String</span><span class="sxs-lookup"><span data-stu-id="8f4b9-137">System.String</span></span>

## <span data-ttu-id="8f4b9-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8f4b9-138">OUTPUTS</span></span>

### <span data-ttu-id="8f4b9-139">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="8f4b9-139">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="8f4b9-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8f4b9-140">NOTES</span></span>

## <span data-ttu-id="8f4b9-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8f4b9-141">RELATED LINKS</span></span>

[<span data-ttu-id="8f4b9-142">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="8f4b9-142">Get-AzSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="8f4b9-143">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="8f4b9-143">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="8f4b9-144">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="8f4b9-144">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="8f4b9-145">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="8f4b9-145">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="8f4b9-146">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="8f4b9-146">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)


