---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 5c2d7c8aa81cb45b6b49898c95b27256aa504b73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924331"
---
# <span data-ttu-id="91ffc-101">Update-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="91ffc-101">Update-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="91ffc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91ffc-102">SYNOPSIS</span></span>
<span data-ttu-id="91ffc-103">Aktualisiert den selbst gehosteten Integrations-Runtime-Knoten.</span><span class="sxs-lookup"><span data-stu-id="91ffc-103">Updates self-hosted integration runtime node.</span></span>

## <span data-ttu-id="91ffc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91ffc-104">SYNTAX</span></span>

### <span data-ttu-id="91ffc-105">UpdateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="91ffc-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91ffc-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="91ffc-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91ffc-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="91ffc-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91ffc-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="91ffc-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String>
 -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="91ffc-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="91ffc-109">DESCRIPTION</span></span>
<span data-ttu-id="91ffc-110">Das **Cmdlet Update-AzSynapseIntegrationRuntimeNode** aktualisiert die Eigenschaften des selbst gehosteten Integrations-Runtime-Knotens in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="91ffc-110">The **Update-AzSynapseIntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a workspace.</span></span> <span data-ttu-id="91ffc-111">Derzeit wird nur das Aktualisieren von "ConcurrentJobsLimit" unterstützt.</span><span class="sxs-lookup"><span data-stu-id="91ffc-111">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="91ffc-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="91ffc-112">EXAMPLES</span></span>

### <span data-ttu-id="91ffc-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="91ffc-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -ConcurrentJobsLimit 3
```

<span data-ttu-id="91ffc-114">Das Cmdlet aktualisiert "ConcurrentJobsLimit" auf 3 für Knoten "Node_1" in der selbst gehosteten Integrations-Runtime "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="91ffc-114">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="91ffc-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="91ffc-115">PARAMETERS</span></span>

### <span data-ttu-id="91ffc-116">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="91ffc-116">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="91ffc-117">Die Anzahl der gleichzeitigen Aufträge, die auf dem Integrations-Runtime-Knoten ausgeführt werden dürfen.</span><span class="sxs-lookup"><span data-stu-id="91ffc-117">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="91ffc-118">Werte zwischen 1 und maxConcurrentJobs sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="91ffc-118">Values between 1 and maxConcurrentJobs are allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ffc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91ffc-119">-DefaultProfile</span></span>
<span data-ttu-id="91ffc-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="91ffc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91ffc-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91ffc-121">-InputObject</span></span>
<span data-ttu-id="91ffc-122">Das Integrations-Runtime-Objekt.</span><span class="sxs-lookup"><span data-stu-id="91ffc-122">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91ffc-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="91ffc-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="91ffc-124">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="91ffc-124">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ffc-125">-Name</span><span class="sxs-lookup"><span data-stu-id="91ffc-125">-Name</span></span>
<span data-ttu-id="91ffc-126">Der Name des Integrations-Runtime-Knotens.</span><span class="sxs-lookup"><span data-stu-id="91ffc-126">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ffc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91ffc-127">-ResourceGroupName</span></span>
<span data-ttu-id="91ffc-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="91ffc-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ffc-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91ffc-129">-ResourceId</span></span>
<span data-ttu-id="91ffc-130">Ressourcenbezeichner der Synapse-Integrations-Runtime.</span><span class="sxs-lookup"><span data-stu-id="91ffc-130">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ffc-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="91ffc-131">-WorkspaceName</span></span>
<span data-ttu-id="91ffc-132">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="91ffc-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ffc-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="91ffc-133">-WorkspaceObject</span></span>
<span data-ttu-id="91ffc-134">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="91ffc-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91ffc-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="91ffc-135">-Confirm</span></span>
<span data-ttu-id="91ffc-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="91ffc-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ffc-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91ffc-137">-WhatIf</span></span>
<span data-ttu-id="91ffc-138">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="91ffc-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91ffc-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="91ffc-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ffc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91ffc-140">CommonParameters</span></span>
<span data-ttu-id="91ffc-141">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91ffc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91ffc-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91ffc-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91ffc-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="91ffc-143">INPUTS</span></span>

### <span data-ttu-id="91ffc-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="91ffc-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="91ffc-145">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="91ffc-145">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="91ffc-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="91ffc-146">OUTPUTS</span></span>

### <span data-ttu-id="91ffc-147">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="91ffc-147">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="91ffc-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="91ffc-148">NOTES</span></span>

## <span data-ttu-id="91ffc-149">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="91ffc-149">RELATED LINKS</span></span>
