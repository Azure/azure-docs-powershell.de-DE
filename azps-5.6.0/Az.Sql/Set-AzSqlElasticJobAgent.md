---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/set-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
ms.openlocfilehash: c65c7a74d4b2edfcddf8b4e08ee3e538c32d31df
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935931"
---
# <span data-ttu-id="170d7-101">Set-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="170d7-101">Set-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="170d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="170d7-102">SYNOPSIS</span></span>
<span data-ttu-id="170d7-103">Aktualisiert einen flexiblen Job-Agent</span><span class="sxs-lookup"><span data-stu-id="170d7-103">Updates an elastic job agent</span></span>

## <span data-ttu-id="170d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="170d7-104">SYNTAX</span></span>

### <span data-ttu-id="170d7-105">DefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="170d7-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="170d7-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="170d7-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="170d7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="170d7-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="170d7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="170d7-108">DESCRIPTION</span></span>
<span data-ttu-id="170d7-109">Das Set-AzSqlElasticJobAgent-Cmdlet aktualisiert einen Mitarbeiter für den flexiblen Auftrag</span><span class="sxs-lookup"><span data-stu-id="170d7-109">The Set-AzSqlElasticJobAgent cmdlet updates an Elastic Job agents</span></span>

## <span data-ttu-id="170d7-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="170d7-110">EXAMPLES</span></span>

### <span data-ttu-id="170d7-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="170d7-111">Example 1</span></span>
```
PS C:\> Set-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent -Tag @{ Octopus = "Agent" }

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="170d7-112">Aktualisiert einen Mitarbeiter für einen flexiblen Auftrag</span><span class="sxs-lookup"><span data-stu-id="170d7-112">Updates an Elastic Job agent</span></span>

## <span data-ttu-id="170d7-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="170d7-113">PARAMETERS</span></span>

### <span data-ttu-id="170d7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="170d7-114">-DefaultProfile</span></span>
<span data-ttu-id="170d7-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="170d7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="170d7-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="170d7-116">-InputObject</span></span>
<span data-ttu-id="170d7-117">Das Agenteingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="170d7-117">The agent input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="170d7-118">-Name</span><span class="sxs-lookup"><span data-stu-id="170d7-118">-Name</span></span>
<span data-ttu-id="170d7-119">Der Agentname</span><span class="sxs-lookup"><span data-stu-id="170d7-119">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: AgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="170d7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="170d7-120">-ResourceGroupName</span></span>
<span data-ttu-id="170d7-121">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="170d7-121">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="170d7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="170d7-122">-ResourceId</span></span>
<span data-ttu-id="170d7-123">Die Agentressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="170d7-123">The agent resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170d7-124">-Servername</span><span class="sxs-lookup"><span data-stu-id="170d7-124">-ServerName</span></span>
<span data-ttu-id="170d7-125">Der Servername</span><span class="sxs-lookup"><span data-stu-id="170d7-125">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="170d7-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="170d7-126">-Tag</span></span>
<span data-ttu-id="170d7-127">Die Tags, die dem Azure SQL-Datenbank-Agent zugeordnet werden sollen</span><span class="sxs-lookup"><span data-stu-id="170d7-127">The tags to associate with the Azure SQL Database Agent</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="170d7-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="170d7-128">-Confirm</span></span>
<span data-ttu-id="170d7-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="170d7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="170d7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="170d7-130">-WhatIf</span></span>
<span data-ttu-id="170d7-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="170d7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="170d7-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="170d7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="170d7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="170d7-133">CommonParameters</span></span>
<span data-ttu-id="170d7-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="170d7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="170d7-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="170d7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="170d7-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="170d7-136">INPUTS</span></span>

### <span data-ttu-id="170d7-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="170d7-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="170d7-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="170d7-138">OUTPUTS</span></span>

### <span data-ttu-id="170d7-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="170d7-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="170d7-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="170d7-140">NOTES</span></span>

## <span data-ttu-id="170d7-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="170d7-141">RELATED LINKS</span></span>
