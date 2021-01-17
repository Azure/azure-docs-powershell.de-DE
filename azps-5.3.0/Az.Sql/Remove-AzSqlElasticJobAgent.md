---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
ms.openlocfilehash: 1352ef72ffc6fd757b4019e217ecb439495ebb44
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460632"
---
# <span data-ttu-id="b2f40-101">Remove-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="b2f40-101">Remove-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="b2f40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2f40-102">SYNOPSIS</span></span>
<span data-ttu-id="b2f40-103">Entfernt den Jobauftragsmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="b2f40-103">Removes the elastic job agent</span></span>

## <span data-ttu-id="b2f40-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2f40-104">SYNTAX</span></span>

### <span data-ttu-id="b2f40-105">DefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b2f40-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2f40-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="b2f40-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2f40-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b2f40-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2f40-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b2f40-108">DESCRIPTION</span></span>
<span data-ttu-id="b2f40-109">Mit Remove-AzSqlElasticJobAgent cmdlet wird ein Agent für einen Arbeitsauftrag entfernt.</span><span class="sxs-lookup"><span data-stu-id="b2f40-109">The Remove-AzSqlElasticJobAgent cmdlet removes an Elastic Job agent</span></span>

## <span data-ttu-id="b2f40-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b2f40-110">EXAMPLES</span></span>

### <span data-ttu-id="b2f40-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b2f40-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="b2f40-112">Entfernt einen Mitarbeiter für einen Job im Job</span><span class="sxs-lookup"><span data-stu-id="b2f40-112">Removes an Elastic Job agent</span></span>

## <span data-ttu-id="b2f40-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2f40-113">PARAMETERS</span></span>

### <span data-ttu-id="b2f40-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2f40-114">-DefaultProfile</span></span>
<span data-ttu-id="b2f40-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b2f40-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2f40-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b2f40-116">-Force</span></span>
<span data-ttu-id="b2f40-117">Bestätigungsmeldung zum Ausführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="b2f40-117">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2f40-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2f40-118">-InputObject</span></span>
<span data-ttu-id="b2f40-119">Das Agentobjekt</span><span class="sxs-lookup"><span data-stu-id="b2f40-119">The agent object</span></span>

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

### <span data-ttu-id="b2f40-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b2f40-120">-Name</span></span>
<span data-ttu-id="b2f40-121">Der Agentname</span><span class="sxs-lookup"><span data-stu-id="b2f40-121">The agent name</span></span>

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

### <span data-ttu-id="b2f40-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2f40-122">-ResourceGroupName</span></span>
<span data-ttu-id="b2f40-123">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="b2f40-123">The resource group name</span></span>

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

### <span data-ttu-id="b2f40-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2f40-124">-ResourceId</span></span>
<span data-ttu-id="b2f40-125">Die Agentressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="b2f40-125">The agent resource id</span></span>

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

### <span data-ttu-id="b2f40-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b2f40-126">-ServerName</span></span>
<span data-ttu-id="b2f40-127">Der Servername</span><span class="sxs-lookup"><span data-stu-id="b2f40-127">The server name</span></span>

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

### <span data-ttu-id="b2f40-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2f40-128">-Confirm</span></span>
<span data-ttu-id="b2f40-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b2f40-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2f40-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b2f40-130">-WhatIf</span></span>
<span data-ttu-id="b2f40-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b2f40-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2f40-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2f40-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2f40-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2f40-133">CommonParameters</span></span>
<span data-ttu-id="b2f40-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2f40-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2f40-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2f40-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2f40-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b2f40-136">INPUTS</span></span>

### <span data-ttu-id="b2f40-137">Microsoft.Azure.Commands.Sql.AgentJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="b2f40-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="b2f40-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b2f40-138">OUTPUTS</span></span>

### <span data-ttu-id="b2f40-139">Microsoft.Azure.Commands.Sql.AgentJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="b2f40-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="b2f40-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b2f40-140">NOTES</span></span>

## <span data-ttu-id="b2f40-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b2f40-141">RELATED LINKS</span></span>
