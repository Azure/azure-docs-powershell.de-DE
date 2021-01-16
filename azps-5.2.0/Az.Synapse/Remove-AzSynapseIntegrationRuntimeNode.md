---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: cb2c632b47e512d31a5349be9b6091a9981f5459
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362885"
---
# <span data-ttu-id="a496e-101">Remove-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="a496e-101">Remove-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="a496e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a496e-102">SYNOPSIS</span></span>
<span data-ttu-id="a496e-103">Entfernen Sie einen Knoten mit dem angegebenen Namen in einer Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="a496e-103">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="a496e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a496e-104">SYNTAX</span></span>

### <span data-ttu-id="a496e-105">RemoveByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a496e-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a496e-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a496e-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a496e-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a496e-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -ResourceId <String> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a496e-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a496e-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a496e-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a496e-109">DESCRIPTION</span></span>
<span data-ttu-id="a496e-110">Das **Cmdlet "Remove-AzSynapseIntegrationRuntimeNode"** entfernt einen Knoten in einer Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="a496e-110">The **Remove-AzSynapseIntegrationRuntimeNode** cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="a496e-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a496e-111">EXAMPLES</span></span>

### <span data-ttu-id="a496e-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a496e-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="a496e-113">Entfernen Sie einen Knoten mit dem angegebenen Namen in einer Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="a496e-113">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="a496e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a496e-114">PARAMETERS</span></span>

### <span data-ttu-id="a496e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a496e-115">-DefaultProfile</span></span>
<span data-ttu-id="a496e-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a496e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a496e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a496e-117">-Force</span></span>
<span data-ttu-id="a496e-118">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="a496e-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="a496e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a496e-119">-InputObject</span></span>
<span data-ttu-id="a496e-120">Das Integrations-Runtime-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a496e-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="a496e-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="a496e-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="a496e-122">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="a496e-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="a496e-123">-NodeName</span><span class="sxs-lookup"><span data-stu-id="a496e-123">-NodeName</span></span>
<span data-ttu-id="a496e-124">Der Name des Integrations-Runtime-Knotens.</span><span class="sxs-lookup"><span data-stu-id="a496e-124">The integration runtime node name.</span></span>

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

### <span data-ttu-id="a496e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a496e-125">-ResourceGroupName</span></span>
<span data-ttu-id="a496e-126">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="a496e-126">Resource group name.</span></span>

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

### <span data-ttu-id="a496e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a496e-127">-ResourceId</span></span>
<span data-ttu-id="a496e-128">Ressourcenbezeichner der Laufzeit der Synapse-Integration.</span><span class="sxs-lookup"><span data-stu-id="a496e-128">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="a496e-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a496e-129">-WorkspaceName</span></span>
<span data-ttu-id="a496e-130">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="a496e-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a496e-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a496e-131">-WorkspaceObject</span></span>
<span data-ttu-id="a496e-132">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a496e-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a496e-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a496e-133">-Confirm</span></span>
<span data-ttu-id="a496e-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a496e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a496e-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a496e-135">-WhatIf</span></span>
<span data-ttu-id="a496e-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a496e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a496e-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a496e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a496e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a496e-138">CommonParameters</span></span>
<span data-ttu-id="a496e-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a496e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a496e-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a496e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a496e-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a496e-141">INPUTS</span></span>

### <span data-ttu-id="a496e-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a496e-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a496e-143">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a496e-143">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="a496e-144">System.String</span><span class="sxs-lookup"><span data-stu-id="a496e-144">System.String</span></span>

## <span data-ttu-id="a496e-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a496e-145">OUTPUTS</span></span>

### <span data-ttu-id="a496e-146">System.Void</span><span class="sxs-lookup"><span data-stu-id="a496e-146">System.Void</span></span>

## <span data-ttu-id="a496e-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a496e-147">NOTES</span></span>

## <span data-ttu-id="a496e-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a496e-148">RELATED LINKS</span></span>
