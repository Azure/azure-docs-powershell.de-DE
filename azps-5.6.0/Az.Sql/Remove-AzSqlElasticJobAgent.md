---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/remove-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
ms.openlocfilehash: 3c6a92a205aef19b1e4cef4842de4cf0414c2397
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921560"
---
# <span data-ttu-id="311f9-101">Remove-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="311f9-101">Remove-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="311f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="311f9-102">SYNOPSIS</span></span>
<span data-ttu-id="311f9-103">Entfernt den flexiblen Job-Agent</span><span class="sxs-lookup"><span data-stu-id="311f9-103">Removes the elastic job agent</span></span>

## <span data-ttu-id="311f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="311f9-104">SYNTAX</span></span>

### <span data-ttu-id="311f9-105">DefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="311f9-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="311f9-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="311f9-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="311f9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="311f9-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="311f9-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="311f9-108">DESCRIPTION</span></span>
<span data-ttu-id="311f9-109">Das Remove-AzSqlElasticJobAgent cmdlet entfernt einen Mitarbeiter für den flexiblen Auftrag</span><span class="sxs-lookup"><span data-stu-id="311f9-109">The Remove-AzSqlElasticJobAgent cmdlet removes an Elastic Job agent</span></span>

## <span data-ttu-id="311f9-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="311f9-110">EXAMPLES</span></span>

### <span data-ttu-id="311f9-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="311f9-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="311f9-112">Entfernt einen Mitarbeiter für einen flexiblen Auftrag</span><span class="sxs-lookup"><span data-stu-id="311f9-112">Removes an Elastic Job agent</span></span>

## <span data-ttu-id="311f9-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="311f9-113">PARAMETERS</span></span>

### <span data-ttu-id="311f9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="311f9-114">-DefaultProfile</span></span>
<span data-ttu-id="311f9-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="311f9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="311f9-116">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="311f9-116">-Force</span></span>
<span data-ttu-id="311f9-117">Bestätigungsmeldung überspringen zum Ausführen der Aktion</span><span class="sxs-lookup"><span data-stu-id="311f9-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="311f9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="311f9-118">-InputObject</span></span>
<span data-ttu-id="311f9-119">Das Agentobjekt</span><span class="sxs-lookup"><span data-stu-id="311f9-119">The agent object</span></span>

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

### <span data-ttu-id="311f9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="311f9-120">-Name</span></span>
<span data-ttu-id="311f9-121">Der Agentname</span><span class="sxs-lookup"><span data-stu-id="311f9-121">The agent name</span></span>

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

### <span data-ttu-id="311f9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="311f9-122">-ResourceGroupName</span></span>
<span data-ttu-id="311f9-123">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="311f9-123">The resource group name</span></span>

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

### <span data-ttu-id="311f9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="311f9-124">-ResourceId</span></span>
<span data-ttu-id="311f9-125">Die Agentressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="311f9-125">The agent resource id</span></span>

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

### <span data-ttu-id="311f9-126">-Servername</span><span class="sxs-lookup"><span data-stu-id="311f9-126">-ServerName</span></span>
<span data-ttu-id="311f9-127">Der Servername</span><span class="sxs-lookup"><span data-stu-id="311f9-127">The server name</span></span>

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

### <span data-ttu-id="311f9-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="311f9-128">-Confirm</span></span>
<span data-ttu-id="311f9-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="311f9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="311f9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="311f9-130">-WhatIf</span></span>
<span data-ttu-id="311f9-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="311f9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="311f9-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="311f9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="311f9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="311f9-133">CommonParameters</span></span>
<span data-ttu-id="311f9-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="311f9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="311f9-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="311f9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="311f9-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="311f9-136">INPUTS</span></span>

### <span data-ttu-id="311f9-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="311f9-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="311f9-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="311f9-138">OUTPUTS</span></span>

### <span data-ttu-id="311f9-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="311f9-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="311f9-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="311f9-140">NOTES</span></span>

## <span data-ttu-id="311f9-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="311f9-141">RELATED LINKS</span></span>
