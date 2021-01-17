---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
ms.openlocfilehash: 1352ef72ffc6fd757b4019e217ecb439495ebb44
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306872"
---
# <span data-ttu-id="5acd3-101">Remove-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="5acd3-101">Remove-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="5acd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5acd3-102">SYNOPSIS</span></span>
<span data-ttu-id="5acd3-103">Entfernt den Jobcentermitarbeiter</span><span class="sxs-lookup"><span data-stu-id="5acd3-103">Removes the elastic job agent</span></span>

## <span data-ttu-id="5acd3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5acd3-104">SYNTAX</span></span>

### <span data-ttu-id="5acd3-105">DefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5acd3-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5acd3-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="5acd3-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5acd3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5acd3-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5acd3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5acd3-108">DESCRIPTION</span></span>
<span data-ttu-id="5acd3-109">Mit Remove-AzSqlElasticJobAgent cmdlet wird ein Agent für einen Job im Job entfernt.</span><span class="sxs-lookup"><span data-stu-id="5acd3-109">The Remove-AzSqlElasticJobAgent cmdlet removes an Elastic Job agent</span></span>

## <span data-ttu-id="5acd3-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5acd3-110">EXAMPLES</span></span>

### <span data-ttu-id="5acd3-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5acd3-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="5acd3-112">Entfernt einen Jobcentermitarbeiter</span><span class="sxs-lookup"><span data-stu-id="5acd3-112">Removes an Elastic Job agent</span></span>

## <span data-ttu-id="5acd3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5acd3-113">PARAMETERS</span></span>

### <span data-ttu-id="5acd3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5acd3-114">-DefaultProfile</span></span>
<span data-ttu-id="5acd3-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5acd3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5acd3-116">-Force</span><span class="sxs-lookup"><span data-stu-id="5acd3-116">-Force</span></span>
<span data-ttu-id="5acd3-117">Bestätigungsmeldung zum Ausführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="5acd3-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="5acd3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5acd3-118">-InputObject</span></span>
<span data-ttu-id="5acd3-119">Das Agentobjekt</span><span class="sxs-lookup"><span data-stu-id="5acd3-119">The agent object</span></span>

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

### <span data-ttu-id="5acd3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5acd3-120">-Name</span></span>
<span data-ttu-id="5acd3-121">Der Agentname</span><span class="sxs-lookup"><span data-stu-id="5acd3-121">The agent name</span></span>

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

### <span data-ttu-id="5acd3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5acd3-122">-ResourceGroupName</span></span>
<span data-ttu-id="5acd3-123">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="5acd3-123">The resource group name</span></span>

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

### <span data-ttu-id="5acd3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5acd3-124">-ResourceId</span></span>
<span data-ttu-id="5acd3-125">Die Agentressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="5acd3-125">The agent resource id</span></span>

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

### <span data-ttu-id="5acd3-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5acd3-126">-ServerName</span></span>
<span data-ttu-id="5acd3-127">Der Servername</span><span class="sxs-lookup"><span data-stu-id="5acd3-127">The server name</span></span>

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

### <span data-ttu-id="5acd3-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5acd3-128">-Confirm</span></span>
<span data-ttu-id="5acd3-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5acd3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5acd3-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5acd3-130">-WhatIf</span></span>
<span data-ttu-id="5acd3-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5acd3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5acd3-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5acd3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5acd3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5acd3-133">CommonParameters</span></span>
<span data-ttu-id="5acd3-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5acd3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5acd3-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5acd3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5acd3-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5acd3-136">INPUTS</span></span>

### <span data-ttu-id="5acd3-137">Microsoft.Azure.Commands.Sql.AgentJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="5acd3-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="5acd3-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5acd3-138">OUTPUTS</span></span>

### <span data-ttu-id="5acd3-139">Microsoft.Azure.Commands.Sql.AgentJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="5acd3-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="5acd3-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5acd3-140">NOTES</span></span>

## <span data-ttu-id="5acd3-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5acd3-141">RELATED LINKS</span></span>
