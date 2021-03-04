---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
ms.openlocfilehash: 9018dab5f09bbab6a3fb1197ee8aabd09141e664
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949952"
---
# <span data-ttu-id="c0e98-101">Get-AzSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="c0e98-101">Get-AzSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="c0e98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0e98-102">SYNOPSIS</span></span>
<span data-ttu-id="c0e98-103">Ruft Preisstufenhinweise für eine Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="c0e98-103">Gets pricing tier hints for a database.</span></span>

## <span data-ttu-id="c0e98-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c0e98-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0e98-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c0e98-105">DESCRIPTION</span></span>
<span data-ttu-id="c0e98-106">Das **Get-AzSqlDatabaseUpgradeHint-Cmdlet** erhält Preisstufenhinweise zum Upgrade einer Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="c0e98-106">The **Get-AzSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="c0e98-107">Datenbanken, die sich noch in web- und business-Preisstufen befinden, erhalten den Hinweis zum Upgrade auf die neuen Tarife Basic, Standard oder Premium.</span><span class="sxs-lookup"><span data-stu-id="c0e98-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>
<span data-ttu-id="c0e98-108">Dieses Cmdlet wird auch vom SQL Server Stretch Database Service in Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c0e98-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="c0e98-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c0e98-109">EXAMPLES</span></span>

### <span data-ttu-id="c0e98-110">Beispiel 1: Erhalten von Empfehlungen für alle Datenbanken auf einem Server</span><span class="sxs-lookup"><span data-stu-id="c0e98-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="c0e98-111">Dieser Befehl gibt Upgradehinweise für alle Datenbanken auf dem Server mit dem Namen Server01 zurück.</span><span class="sxs-lookup"><span data-stu-id="c0e98-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="c0e98-112">Beispiel 2: Erhalten von Empfehlungen für eine bestimmte Datenbank</span><span class="sxs-lookup"><span data-stu-id="c0e98-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="c0e98-113">Dieser Befehl gibt Upgradehinweise für eine bestimmte Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="c0e98-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="c0e98-114">Beispiel 3: Empfehlung für alle Datenbanken erhalten, die sich nicht in einem pool für flexible Datenbanken befinden</span><span class="sxs-lookup"><span data-stu-id="c0e98-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="c0e98-115">Dieser Befehl gibt Upgradehinweise für alle Datenbanken zurück, die sich nicht in einem pool für flexible Datenbanken befinden.</span><span class="sxs-lookup"><span data-stu-id="c0e98-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

### <span data-ttu-id="c0e98-116">Beispiel 4: Erhalten von Empfehlungen für alle Datenbanken auf einem Server mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="c0e98-116">Example 4: Get recommendations for all databases on a server using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="c0e98-117">Dieser Befehl gibt Upgradehinweise für alle Datenbanken auf dem Server mit dem Namen Server01 zurück, die mit "Datenbank" beginnen.</span><span class="sxs-lookup"><span data-stu-id="c0e98-117">This command returns upgrade hints for all databases on the server named Server01 that start with "Database".</span></span>

## <span data-ttu-id="c0e98-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c0e98-118">PARAMETERS</span></span>

### <span data-ttu-id="c0e98-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c0e98-119">-DatabaseName</span></span>
<span data-ttu-id="c0e98-120">Gibt den Namen der SQL an, für die dieses Cmdlet einen Upgradehinweis erhält.</span><span class="sxs-lookup"><span data-stu-id="c0e98-120">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="c0e98-121">Wenn Sie keine Datenbank angeben, ruft dieses Cmdlet Hinweise für alle Datenbanken auf dem logischen Server ab.</span><span class="sxs-lookup"><span data-stu-id="c0e98-121">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

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

### <span data-ttu-id="c0e98-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0e98-122">-DefaultProfile</span></span>
<span data-ttu-id="c0e98-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c0e98-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0e98-124">-ExcludeElasticPoolCandidates</span><span class="sxs-lookup"><span data-stu-id="c0e98-124">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="c0e98-125">Gibt an, ob Datenbanken in flexiblen Datenbankpools von den zurückgegebenen Empfehlungen ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="c0e98-125">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0e98-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0e98-126">-ResourceGroupName</span></span>
<span data-ttu-id="c0e98-127">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="c0e98-127">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="c0e98-128">-Servername</span><span class="sxs-lookup"><span data-stu-id="c0e98-128">-ServerName</span></span>
<span data-ttu-id="c0e98-129">Gibt den Namen des Servers an, der die Datenbank hostet, für die dieses Cmdlet einen Upgradehinweis erhält.</span><span class="sxs-lookup"><span data-stu-id="c0e98-129">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="c0e98-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c0e98-130">-Confirm</span></span>
<span data-ttu-id="c0e98-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c0e98-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0e98-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0e98-132">-WhatIf</span></span>
<span data-ttu-id="c0e98-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c0e98-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0e98-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0e98-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0e98-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0e98-135">CommonParameters</span></span>
<span data-ttu-id="c0e98-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0e98-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0e98-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0e98-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0e98-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c0e98-138">INPUTS</span></span>

### <span data-ttu-id="c0e98-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c0e98-139">System.String</span></span>

### <span data-ttu-id="c0e98-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c0e98-140">System.Boolean</span></span>

## <span data-ttu-id="c0e98-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c0e98-141">OUTPUTS</span></span>

### <span data-ttu-id="c0e98-142">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span><span class="sxs-lookup"><span data-stu-id="c0e98-142">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span></span>

## <span data-ttu-id="c0e98-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c0e98-143">NOTES</span></span>

## <span data-ttu-id="c0e98-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c0e98-144">RELATED LINKS</span></span>

[<span data-ttu-id="c0e98-145">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="c0e98-145">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="c0e98-146">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="c0e98-146">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)


