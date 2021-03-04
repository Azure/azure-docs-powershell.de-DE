---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 07b1b36222f0d1a31d4a4a7374957336246f0073
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948267"
---
# <span data-ttu-id="f48f0-101">Remove-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="f48f0-101">Remove-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="f48f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f48f0-102">SYNOPSIS</span></span>
<span data-ttu-id="f48f0-103">Entfernen Sie einen Knoten mit dem angegebenen Namen in einer Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="f48f0-103">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="f48f0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f48f0-104">SYNTAX</span></span>

### <span data-ttu-id="f48f0-105">RemoveByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f48f0-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f48f0-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f48f0-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f48f0-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f48f0-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -ResourceId <String> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f48f0-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f48f0-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f48f0-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f48f0-109">DESCRIPTION</span></span>
<span data-ttu-id="f48f0-110">Das **Cmdlet Remove-AzSynapseIntegrationRuntimeNode** entfernt einen Knoten in einer Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="f48f0-110">The **Remove-AzSynapseIntegrationRuntimeNode** cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="f48f0-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f48f0-111">EXAMPLES</span></span>

### <span data-ttu-id="f48f0-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f48f0-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="f48f0-113">Entfernen Sie einen Knoten mit dem angegebenen Namen in einer Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="f48f0-113">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="f48f0-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f48f0-114">PARAMETERS</span></span>

### <span data-ttu-id="f48f0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f48f0-115">-DefaultProfile</span></span>
<span data-ttu-id="f48f0-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f48f0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f48f0-117">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="f48f0-117">-Force</span></span>
<span data-ttu-id="f48f0-118">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="f48f0-118">Don't ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f48f0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f48f0-119">-InputObject</span></span>
<span data-ttu-id="f48f0-120">Das Integrations-Runtime-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f48f0-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f48f0-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="f48f0-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="f48f0-122">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="f48f0-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f48f0-123">-NodeName</span><span class="sxs-lookup"><span data-stu-id="f48f0-123">-NodeName</span></span>
<span data-ttu-id="f48f0-124">Der Name des Integrations-Runtime-Knotens.</span><span class="sxs-lookup"><span data-stu-id="f48f0-124">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f48f0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f48f0-125">-ResourceGroupName</span></span>
<span data-ttu-id="f48f0-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f48f0-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f48f0-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f48f0-127">-ResourceId</span></span>
<span data-ttu-id="f48f0-128">Ressourcenbezeichner der Synapse-Integrations-Runtime.</span><span class="sxs-lookup"><span data-stu-id="f48f0-128">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f48f0-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f48f0-129">-WorkspaceName</span></span>
<span data-ttu-id="f48f0-130">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="f48f0-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f48f0-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f48f0-131">-WorkspaceObject</span></span>
<span data-ttu-id="f48f0-132">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f48f0-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f48f0-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f48f0-133">-Confirm</span></span>
<span data-ttu-id="f48f0-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f48f0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f48f0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f48f0-135">-WhatIf</span></span>
<span data-ttu-id="f48f0-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f48f0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f48f0-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f48f0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f48f0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f48f0-138">CommonParameters</span></span>
<span data-ttu-id="f48f0-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f48f0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f48f0-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f48f0-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f48f0-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f48f0-141">INPUTS</span></span>

### <span data-ttu-id="f48f0-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f48f0-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="f48f0-143">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f48f0-143">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="f48f0-144">System.String</span><span class="sxs-lookup"><span data-stu-id="f48f0-144">System.String</span></span>

## <span data-ttu-id="f48f0-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f48f0-145">OUTPUTS</span></span>

### <span data-ttu-id="f48f0-146">System.Void</span><span class="sxs-lookup"><span data-stu-id="f48f0-146">System.Void</span></span>

## <span data-ttu-id="f48f0-147">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f48f0-147">NOTES</span></span>

## <span data-ttu-id="f48f0-148">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f48f0-148">RELATED LINKS</span></span>
