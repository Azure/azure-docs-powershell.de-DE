---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 4192350397a9ba23e57b77b017ff7409afac7a39
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009543"
---
# <span data-ttu-id="c3cd6-101">Update-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="c3cd6-101">Update-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="c3cd6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c3cd6-102">SYNOPSIS</span></span>
<span data-ttu-id="c3cd6-103">Aktualisiert den Self-Hosted Integration Runtime-Knoten.</span><span class="sxs-lookup"><span data-stu-id="c3cd6-103">Updates self-hosted integration runtime node.</span></span>

## <span data-ttu-id="c3cd6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3cd6-104">SYNTAX</span></span>

### <span data-ttu-id="c3cd6-105">UpdateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c3cd6-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3cd6-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3cd6-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3cd6-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3cd6-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3cd6-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3cd6-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String>
 -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c3cd6-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3cd6-109">DESCRIPTION</span></span>
<span data-ttu-id="c3cd6-110">Das Cmdlet **Update-AzSynapseIntegrationRuntimeNode** aktualisiert Eigenschaften des selbst gehosteten Integrationslauf Zeit Knotens in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="c3cd6-110">The **Update-AzSynapseIntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a workspace.</span></span> <span data-ttu-id="c3cd6-111">Derzeit wird nur die Aktualisierung von "ConcurrentJobsLimit" unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c3cd6-111">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="c3cd6-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c3cd6-112">EXAMPLES</span></span>

### <span data-ttu-id="c3cd6-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c3cd6-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -ConcurrentJobsLimit 3
```

<span data-ttu-id="c3cd6-114">Das Cmdlet aktualisiert "ConcurrentJobsLimit" auf "3" für den Knoten "Node_1" in der selbst gehosteten Integrationslaufzeit "Test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="c3cd6-114">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="c3cd6-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3cd6-115">PARAMETERS</span></span>

### <span data-ttu-id="c3cd6-116">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="c3cd6-116">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="c3cd6-117">Die Anzahl von gleichzeitigen Aufträgen, die auf dem Integrationslauf Zeit Knoten ausgeführt werden dürfen.</span><span class="sxs-lookup"><span data-stu-id="c3cd6-117">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="c3cd6-118">Werte zwischen 1 und maxConcurrentJobs sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="c3cd6-118">Values between 1 and maxConcurrentJobs are allowed.</span></span>

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

### <span data-ttu-id="c3cd6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3cd6-119">-DefaultProfile</span></span>
<span data-ttu-id="c3cd6-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c3cd6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3cd6-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c3cd6-121">-InputObject</span></span>
<span data-ttu-id="c3cd6-122">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="c3cd6-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="c3cd6-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="c3cd6-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="c3cd6-124">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="c3cd6-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="c3cd6-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c3cd6-125">-Name</span></span>
<span data-ttu-id="c3cd6-126">Der Knotenname der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="c3cd6-126">The integration runtime node name.</span></span>

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

### <span data-ttu-id="c3cd6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3cd6-127">-ResourceGroupName</span></span>
<span data-ttu-id="c3cd6-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c3cd6-128">Resource group name.</span></span>

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

### <span data-ttu-id="c3cd6-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c3cd6-129">-ResourceId</span></span>
<span data-ttu-id="c3cd6-130">Ressourcenbezeichner der Synapse-Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="c3cd6-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="c3cd6-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c3cd6-131">-WorkspaceName</span></span>
<span data-ttu-id="c3cd6-132">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="c3cd6-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c3cd6-133">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="c3cd6-133">-WorkspaceObject</span></span>
<span data-ttu-id="c3cd6-134">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="c3cd6-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c3cd6-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c3cd6-135">-Confirm</span></span>
<span data-ttu-id="c3cd6-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3cd6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3cd6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3cd6-137">-WhatIf</span></span>
<span data-ttu-id="c3cd6-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3cd6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3cd6-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3cd6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3cd6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3cd6-140">CommonParameters</span></span>
<span data-ttu-id="c3cd6-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3cd6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3cd6-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3cd6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3cd6-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c3cd6-143">INPUTS</span></span>

### <span data-ttu-id="c3cd6-144">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c3cd6-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="c3cd6-145">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c3cd6-145">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="c3cd6-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c3cd6-146">OUTPUTS</span></span>

### <span data-ttu-id="c3cd6-147">Microsoft. Azure. Commands. Synapse. Models. PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="c3cd6-147">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="c3cd6-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="c3cd6-148">NOTES</span></span>

## <span data-ttu-id="c3cd6-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c3cd6-149">RELATED LINKS</span></span>
