---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapseintegrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
ms.openlocfilehash: 59630bd0ffcf5bebfc68f647cff444466727a990
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359314"
---
# <span data-ttu-id="6a3ea-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="6a3ea-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="6a3ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a3ea-102">SYNOPSIS</span></span>
<span data-ttu-id="6a3ea-103">Aktualisiert die selbst gehostete Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="6a3ea-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="6a3ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6a3ea-104">SYNTAX</span></span>

### <span data-ttu-id="6a3ea-105">InvokeByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6a3ea-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a3ea-106">InvokeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a3ea-106">InvokeByParentObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a3ea-107">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a3ea-107">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a3ea-108">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a3ea-108">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a3ea-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6a3ea-109">DESCRIPTION</span></span>
<span data-ttu-id="6a3ea-110">Das **Cmdlet Invoke-AzSynapseIntegrationRuntimeUpgrade** aktualisiert die selbst gehostete Integrationslaufzeit, wenn die neue Version verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="6a3ea-110">The **Invoke-AzSynapseIntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="6a3ea-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6a3ea-111">EXAMPLES</span></span>

### <span data-ttu-id="6a3ea-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6a3ea-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapseIntegrationRuntimeUpgrade -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="6a3ea-113">Das Cmdlet aktualisiert die selbst gehostete Integrationslaufzeit namens "test-selfhost-ir" im ContosoWorkspace-Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="6a3ea-113">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="6a3ea-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a3ea-114">PARAMETERS</span></span>

### <span data-ttu-id="6a3ea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a3ea-115">-DefaultProfile</span></span>
<span data-ttu-id="6a3ea-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6a3ea-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a3ea-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a3ea-117">-InputObject</span></span>
<span data-ttu-id="6a3ea-118">Das Integrations-Runtime-Objekt.</span><span class="sxs-lookup"><span data-stu-id="6a3ea-118">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: InvokeByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a3ea-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6a3ea-119">-Name</span></span>
<span data-ttu-id="6a3ea-120">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="6a3ea-120">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet, InvokeByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a3ea-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a3ea-121">-ResourceGroupName</span></span>
<span data-ttu-id="6a3ea-122">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="6a3ea-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a3ea-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a3ea-123">-ResourceId</span></span>
<span data-ttu-id="6a3ea-124">Ressourcenbezeichner der Synapse-Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="6a3ea-124">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a3ea-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6a3ea-125">-WorkspaceName</span></span>
<span data-ttu-id="6a3ea-126">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="6a3ea-126">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a3ea-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6a3ea-127">-WorkspaceObject</span></span>
<span data-ttu-id="6a3ea-128">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="6a3ea-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: InvokeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a3ea-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a3ea-129">-Confirm</span></span>
<span data-ttu-id="6a3ea-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6a3ea-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a3ea-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6a3ea-131">-WhatIf</span></span>
<span data-ttu-id="6a3ea-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6a3ea-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a3ea-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6a3ea-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a3ea-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a3ea-134">CommonParameters</span></span>
<span data-ttu-id="6a3ea-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a3ea-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a3ea-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a3ea-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a3ea-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6a3ea-137">INPUTS</span></span>

### <span data-ttu-id="6a3ea-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6a3ea-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="6a3ea-139">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6a3ea-139">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="6a3ea-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6a3ea-140">OUTPUTS</span></span>

### <span data-ttu-id="6a3ea-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="6a3ea-141">System.Void</span></span>

## <span data-ttu-id="6a3ea-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6a3ea-142">NOTES</span></span>

## <span data-ttu-id="6a3ea-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6a3ea-143">RELATED LINKS</span></span>
