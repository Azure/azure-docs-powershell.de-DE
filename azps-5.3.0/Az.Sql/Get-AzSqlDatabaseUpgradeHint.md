---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
ms.openlocfilehash: b5f94aeb66749fa9bc89a89febb0bc5597241d58
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458275"
---
# <span data-ttu-id="513bd-101">Get-AzSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="513bd-101">Get-AzSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="513bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="513bd-102">SYNOPSIS</span></span>
<span data-ttu-id="513bd-103">Ruft Preisstufenhinweise für eine Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="513bd-103">Gets pricing tier hints for a database.</span></span>

## <span data-ttu-id="513bd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="513bd-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="513bd-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="513bd-105">DESCRIPTION</span></span>
<span data-ttu-id="513bd-106">Das **Cmdlet "Get-AzSqlDatabaseUpgradeHint"** ruft Preisstufenhinweise für das Upgrade einer Azure SQL ab.</span><span class="sxs-lookup"><span data-stu-id="513bd-106">The **Get-AzSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="513bd-107">Datenbanken, die sich noch auf den Preisstufen "Web" und "Business" befinden, erhalten den Hinweis, auf die neuen Preisstufen Basic, Standard oder Premium zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="513bd-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>
<span data-ttu-id="513bd-108">Dieses Cmdlet wird auch vom Dienst SQL Server Stretch Database in Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="513bd-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="513bd-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="513bd-109">EXAMPLES</span></span>

### <span data-ttu-id="513bd-110">Beispiel 1: Erhalten von Empfehlungen für alle Datenbanken auf einem Server</span><span class="sxs-lookup"><span data-stu-id="513bd-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="513bd-111">Dieser Befehl gibt Upgradehinweise für alle Datenbanken auf dem Server "Server01" zurück.</span><span class="sxs-lookup"><span data-stu-id="513bd-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="513bd-112">Beispiel 2: Erhalten von Empfehlungen für eine bestimmte Datenbank</span><span class="sxs-lookup"><span data-stu-id="513bd-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="513bd-113">Dieser Befehl gibt Upgradehinweise für eine bestimmte Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="513bd-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="513bd-114">Beispiel 3: Empfehlung für alle Datenbanken erhalten, die sich nicht in einem Datenbankpool befinden</span><span class="sxs-lookup"><span data-stu-id="513bd-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="513bd-115">Dieser Befehl gibt Upgradehinweise für alle Datenbanken zurück, die sich nicht in einem Datenbankpool mit Datenbanken befinden.</span><span class="sxs-lookup"><span data-stu-id="513bd-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

### <span data-ttu-id="513bd-116">Beispiel 4: Erhalten von Empfehlungen für alle Datenbanken auf einem Server mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="513bd-116">Example 4: Get recommendations for all databases on a server using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="513bd-117">Dieser Befehl gibt Upgradehinweise für alle Datenbanken auf dem Server "Server01" zurück, die mit "Datenbank" beginnen.</span><span class="sxs-lookup"><span data-stu-id="513bd-117">This command returns upgrade hints for all databases on the server named Server01 that start with "Database".</span></span>

## <span data-ttu-id="513bd-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="513bd-118">PARAMETERS</span></span>

### <span data-ttu-id="513bd-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="513bd-119">-DatabaseName</span></span>
<span data-ttu-id="513bd-120">Gibt den Namen der SQL an, für die dieses Cmdlet einen Upgradehinweis erhält.</span><span class="sxs-lookup"><span data-stu-id="513bd-120">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="513bd-121">Wenn Sie keine Datenbank angeben, erhält dieses Cmdlet Hinweise für alle Datenbanken auf dem logischen Server.</span><span class="sxs-lookup"><span data-stu-id="513bd-121">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

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

### <span data-ttu-id="513bd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="513bd-122">-DefaultProfile</span></span>
<span data-ttu-id="513bd-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="513bd-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="513bd-124">-ExcludeElasticPoolCandidates</span><span class="sxs-lookup"><span data-stu-id="513bd-124">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="513bd-125">Gibt an, ob Datenbanken in Datenbankdatenbanken von den zurückgegebenen Empfehlungen ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="513bd-125">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

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

### <span data-ttu-id="513bd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="513bd-126">-ResourceGroupName</span></span>
<span data-ttu-id="513bd-127">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="513bd-127">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="513bd-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="513bd-128">-ServerName</span></span>
<span data-ttu-id="513bd-129">Gibt den Namen des Servers an, der die Datenbank hostet, für die dieses Cmdlet einen Upgradehinweis erhält.</span><span class="sxs-lookup"><span data-stu-id="513bd-129">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="513bd-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="513bd-130">-Confirm</span></span>
<span data-ttu-id="513bd-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="513bd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="513bd-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="513bd-132">-WhatIf</span></span>
<span data-ttu-id="513bd-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="513bd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="513bd-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="513bd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="513bd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="513bd-135">CommonParameters</span></span>
<span data-ttu-id="513bd-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="513bd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="513bd-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="513bd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="513bd-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="513bd-138">INPUTS</span></span>

### <span data-ttu-id="513bd-139">System.String</span><span class="sxs-lookup"><span data-stu-id="513bd-139">System.String</span></span>

### <span data-ttu-id="513bd-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="513bd-140">System.Boolean</span></span>

## <span data-ttu-id="513bd-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="513bd-141">OUTPUTS</span></span>

### <span data-ttu-id="513bd-142">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span><span class="sxs-lookup"><span data-stu-id="513bd-142">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span></span>

## <span data-ttu-id="513bd-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="513bd-143">NOTES</span></span>

## <span data-ttu-id="513bd-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="513bd-144">RELATED LINKS</span></span>

[<span data-ttu-id="513bd-145">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="513bd-145">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="513bd-146">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="513bd-146">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)


