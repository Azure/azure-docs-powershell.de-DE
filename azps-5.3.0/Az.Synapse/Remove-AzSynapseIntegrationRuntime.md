---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 57b6c6619a45e515c7aff2e30edc346ff39af9ac
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383492"
---
# <span data-ttu-id="ff6b3-101">Remove-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ff6b3-101">Remove-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="ff6b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff6b3-102">SYNOPSIS</span></span>
<span data-ttu-id="ff6b3-103">Entfernt eine Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="ff6b3-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="ff6b3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff6b3-104">SYNTAX</span></span>

### <span data-ttu-id="ff6b3-105">RemoveByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ff6b3-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff6b3-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff6b3-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff6b3-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff6b3-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -ResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff6b3-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff6b3-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff6b3-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ff6b3-109">DESCRIPTION</span></span>
<span data-ttu-id="ff6b3-110">Das **Cmdlet "Remove-AzSynapseIntegrationRuntime"** entfernt eine Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="ff6b3-110">The **Remove-AzSynapseIntegrationRuntime** cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="ff6b3-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ff6b3-111">EXAMPLES</span></span>

### <span data-ttu-id="ff6b3-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ff6b3-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="ff6b3-113">Mit diesem Befehl wird die Integrationslaufzeit mit dem Namen "test-reserved-ir" aus dem Arbeitsbereich "ContosoWorkspace" entfernt.</span><span class="sxs-lookup"><span data-stu-id="ff6b3-113">This command removes the integration runtime named 'test-reserved-ir' from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="ff6b3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff6b3-114">PARAMETERS</span></span>

### <span data-ttu-id="ff6b3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff6b3-115">-DefaultProfile</span></span>
<span data-ttu-id="ff6b3-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ff6b3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff6b3-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ff6b3-117">-Force</span></span>
<span data-ttu-id="ff6b3-118">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="ff6b3-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="ff6b3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff6b3-119">-InputObject</span></span>
<span data-ttu-id="ff6b3-120">Das Integrations-Runtime-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ff6b3-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="ff6b3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ff6b3-121">-Name</span></span>
<span data-ttu-id="ff6b3-122">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="ff6b3-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff6b3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff6b3-123">-ResourceGroupName</span></span>
<span data-ttu-id="ff6b3-124">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="ff6b3-124">Resource group name.</span></span>

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

### <span data-ttu-id="ff6b3-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff6b3-125">-ResourceId</span></span>
<span data-ttu-id="ff6b3-126">Ressourcenbezeichner der Synapse-Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="ff6b3-126">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="ff6b3-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ff6b3-127">-WorkspaceName</span></span>
<span data-ttu-id="ff6b3-128">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="ff6b3-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ff6b3-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ff6b3-129">-WorkspaceObject</span></span>
<span data-ttu-id="ff6b3-130">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="ff6b3-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ff6b3-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff6b3-131">-Confirm</span></span>
<span data-ttu-id="ff6b3-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ff6b3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff6b3-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ff6b3-133">-WhatIf</span></span>
<span data-ttu-id="ff6b3-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ff6b3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff6b3-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ff6b3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff6b3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff6b3-136">CommonParameters</span></span>
<span data-ttu-id="ff6b3-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff6b3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff6b3-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff6b3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff6b3-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ff6b3-139">INPUTS</span></span>

### <span data-ttu-id="ff6b3-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ff6b3-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ff6b3-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ff6b3-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="ff6b3-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ff6b3-142">OUTPUTS</span></span>

### <span data-ttu-id="ff6b3-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="ff6b3-143">System.Void</span></span>

## <span data-ttu-id="ff6b3-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ff6b3-144">NOTES</span></span>

## <span data-ttu-id="ff6b3-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ff6b3-145">RELATED LINKS</span></span>
