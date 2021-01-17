---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 848A6972-AB29-46FB-8E03-FF2ADB113A0E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 8813d405ebc8fadafa037afb884240dcdbb95383
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375065"
---
# <span data-ttu-id="3b849-101">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="3b849-101">Get-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="3b849-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b849-102">SYNOPSIS</span></span>
<span data-ttu-id="3b849-103">Ruft die Datenmaskierungsregeln aus einer Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="3b849-103">Gets the data masking rules from a database.</span></span>

## <span data-ttu-id="3b849-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3b849-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingRule [-SchemaName <String>] [-TableName <String>] [-ColumnName <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b849-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3b849-105">DESCRIPTION</span></span>
<span data-ttu-id="3b849-106">Das **Cmdlet "Get-AzSqlDatabaseDataMaskingRule"** ruft entweder eine bestimmte Datenmaskierungsregel oder alle Datenmaskierungsregeln für eine Azure SQL ab.</span><span class="sxs-lookup"><span data-stu-id="3b849-106">The **Get-AzSqlDatabaseDataMaskingRule** cmdlet gets either a specific data masking rule or all of the data masking rules for an Azure SQL database.</span></span>
<span data-ttu-id="3b849-107">Um das Cmdlet zu verwenden, verwenden Sie die Parameter *"ResourceGroupName",* *"ServerName"* und *"DatabaseName",* um die Datenbank zu identifizieren, und den Parameter *"RuleId",* um anzugeben, welche Regel dieses Cmdlet zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="3b849-107">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database, and the *RuleId* parameter to specify which rule this cmdlet returns.</span></span>
<span data-ttu-id="3b849-108">Wenn Sie *"RuleId" nicht bereitstellen,* werden alle Datenmaskierungsregeln für diese Azure SQL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3b849-108">If you do not provide *RuleId*, all the data masking rules for that Azure SQL database are returned.</span></span>
<span data-ttu-id="3b849-109">Dieses Cmdlet wird auch vom Dienst SQL Server Stretch Database in Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3b849-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="3b849-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3b849-110">EXAMPLES</span></span>

### <span data-ttu-id="3b849-111">Beispiel 1: Alle Datenmaskierungsregeln aus einer Datenbank erhalten</span><span class="sxs-lookup"><span data-stu-id="3b849-111">Example 1: Get all data masking rules from a database</span></span>
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

### <span data-ttu-id="3b849-112">Beispiel 2: Die Datenmaskregel wird für das Schema "dbo", die Tabelle "Tabelle1" und die Spalte "Spalte1" definiert.</span><span class="sxs-lookup"><span data-stu-id="3b849-112">Example 2: Get the data masking rule defined on schema "dbo", table "table1" and column "column1".</span></span>
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

## <span data-ttu-id="3b849-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b849-113">PARAMETERS</span></span>

### <span data-ttu-id="3b849-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="3b849-114">-ColumnName</span></span>
<span data-ttu-id="3b849-115">Gibt den Namen der Spalte an, auf die die Maskierungsregel ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="3b849-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="3b849-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3b849-116">-DatabaseName</span></span>
<span data-ttu-id="3b849-117">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="3b849-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="3b849-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b849-118">-DefaultProfile</span></span>
<span data-ttu-id="3b849-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="3b849-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b849-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b849-120">-ResourceGroupName</span></span>
<span data-ttu-id="3b849-121">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="3b849-121">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="3b849-122">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="3b849-122">-SchemaName</span></span>
<span data-ttu-id="3b849-123">Gibt den Namen eines Schemas an.</span><span class="sxs-lookup"><span data-stu-id="3b849-123">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="3b849-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3b849-124">-ServerName</span></span>
<span data-ttu-id="3b849-125">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="3b849-125">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="3b849-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="3b849-126">-TableName</span></span>
<span data-ttu-id="3b849-127">Gibt den Namen einer Azure SQL an.</span><span class="sxs-lookup"><span data-stu-id="3b849-127">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="3b849-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b849-128">-Confirm</span></span>
<span data-ttu-id="3b849-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3b849-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b849-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3b849-130">-WhatIf</span></span>
<span data-ttu-id="3b849-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3b849-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b849-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3b849-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b849-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b849-133">CommonParameters</span></span>
<span data-ttu-id="3b849-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b849-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b849-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b849-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b849-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3b849-136">INPUTS</span></span>

### <span data-ttu-id="3b849-137">System.String</span><span class="sxs-lookup"><span data-stu-id="3b849-137">System.String</span></span>

## <span data-ttu-id="3b849-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3b849-138">OUTPUTS</span></span>

### <span data-ttu-id="3b849-139">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="3b849-139">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="3b849-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3b849-140">NOTES</span></span>

## <span data-ttu-id="3b849-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3b849-141">RELATED LINKS</span></span>

[<span data-ttu-id="3b849-142">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="3b849-142">Get-AzSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="3b849-143">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="3b849-143">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="3b849-144">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="3b849-144">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="3b849-145">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="3b849-145">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="3b849-146">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="3b849-146">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)


