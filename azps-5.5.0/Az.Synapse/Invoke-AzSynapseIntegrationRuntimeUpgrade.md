---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapseintegrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
ms.openlocfilehash: 59630bd0ffcf5bebfc68f647cff444466727a990
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174961"
---
# <span data-ttu-id="731e5-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="731e5-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="731e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="731e5-102">SYNOPSIS</span></span>
<span data-ttu-id="731e5-103">Aktualisiert die selbst gehostete Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="731e5-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="731e5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="731e5-104">SYNTAX</span></span>

### <span data-ttu-id="731e5-105">InvokeByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="731e5-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="731e5-106">InvokeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="731e5-106">InvokeByParentObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="731e5-107">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="731e5-107">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="731e5-108">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="731e5-108">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="731e5-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="731e5-109">DESCRIPTION</span></span>
<span data-ttu-id="731e5-110">Das **Cmdlet Invoke-AzSynapseIntegrationRuntimeUpgrade** aktualisiert die selbst gehostete Integrationslaufzeit, wenn die neue Version verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="731e5-110">The **Invoke-AzSynapseIntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="731e5-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="731e5-111">EXAMPLES</span></span>

### <span data-ttu-id="731e5-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="731e5-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapseIntegrationRuntimeUpgrade -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="731e5-113">Das Cmdlet aktualisiert die selbst gehostete Integrationslaufzeit namens "test-selfhost-ir" im ContosoWorkspace-Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="731e5-113">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="731e5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="731e5-114">PARAMETERS</span></span>

### <span data-ttu-id="731e5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="731e5-115">-DefaultProfile</span></span>
<span data-ttu-id="731e5-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="731e5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="731e5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="731e5-117">-InputObject</span></span>
<span data-ttu-id="731e5-118">Das Integrations-Runtime-Objekt.</span><span class="sxs-lookup"><span data-stu-id="731e5-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="731e5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="731e5-119">-Name</span></span>
<span data-ttu-id="731e5-120">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="731e5-120">The integration runtime name.</span></span>

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

### <span data-ttu-id="731e5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="731e5-121">-ResourceGroupName</span></span>
<span data-ttu-id="731e5-122">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="731e5-122">Resource group name.</span></span>

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

### <span data-ttu-id="731e5-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="731e5-123">-ResourceId</span></span>
<span data-ttu-id="731e5-124">Ressourcenbezeichner der Laufzeit der Synapse-Integration.</span><span class="sxs-lookup"><span data-stu-id="731e5-124">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="731e5-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="731e5-125">-WorkspaceName</span></span>
<span data-ttu-id="731e5-126">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="731e5-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="731e5-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="731e5-127">-WorkspaceObject</span></span>
<span data-ttu-id="731e5-128">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="731e5-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="731e5-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="731e5-129">-Confirm</span></span>
<span data-ttu-id="731e5-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="731e5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="731e5-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="731e5-131">-WhatIf</span></span>
<span data-ttu-id="731e5-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="731e5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="731e5-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="731e5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="731e5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="731e5-134">CommonParameters</span></span>
<span data-ttu-id="731e5-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="731e5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="731e5-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="731e5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="731e5-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="731e5-137">INPUTS</span></span>

### <span data-ttu-id="731e5-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="731e5-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="731e5-139">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="731e5-139">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="731e5-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="731e5-140">OUTPUTS</span></span>

### <span data-ttu-id="731e5-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="731e5-141">System.Void</span></span>

## <span data-ttu-id="731e5-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="731e5-142">NOTES</span></span>

## <span data-ttu-id="731e5-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="731e5-143">RELATED LINKS</span></span>
