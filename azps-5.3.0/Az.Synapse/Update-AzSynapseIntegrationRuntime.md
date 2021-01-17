---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 31647da87319ca6be90962f34d128f5e2c922d47
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469248"
---
# <span data-ttu-id="63939-101">Update-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="63939-101">Update-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="63939-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63939-102">SYNOPSIS</span></span>
<span data-ttu-id="63939-103">Aktualisiert eine Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="63939-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="63939-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="63939-104">SYNTAX</span></span>

### <span data-ttu-id="63939-105">UpdateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="63939-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63939-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="63939-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63939-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="63939-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -ResourceId <String> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63939-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="63939-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="63939-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="63939-109">DESCRIPTION</span></span>
<span data-ttu-id="63939-110">Das **Cmdlet "Update-AzSynapseIntegrationRuntime"** aktualisiert Integrationslaufzeiteigenschaften.</span><span class="sxs-lookup"><span data-stu-id="63939-110">The **Update-AzSynapseIntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="63939-111">Derzeit unterstützt das Cmdlet nur das Aktualisieren von "AutoUpdate" und "AutoUpdateDelayOffset" für selbst gehostete Integrationslaufzeiten.</span><span class="sxs-lookup"><span data-stu-id="63939-111">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="63939-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="63939-112">EXAMPLES</span></span>

### <span data-ttu-id="63939-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="63939-113">Example 1</span></span>
```powershell
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -AutoUpdate Off -AutoUpdateDelayOffset $ts
```

<span data-ttu-id="63939-114">Das Cmdlet aktualisiert die selbst gehostete Integrationslaufzeit mit dem Namen "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="63939-114">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="63939-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63939-115">PARAMETERS</span></span>

### <span data-ttu-id="63939-116">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="63939-116">-AutoUpdate</span></span>
<span data-ttu-id="63939-117">Aktivieren oder deaktivieren Sie die automatische Aktualisierung der selbst gehosteten Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="63939-117">Enable or disable the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: On, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63939-118">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="63939-118">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="63939-119">Die Tageszeit für die automatische Aktualisierung der selbst gehosteten Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="63939-119">The time of the day for the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63939-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63939-120">-DefaultProfile</span></span>
<span data-ttu-id="63939-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="63939-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63939-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63939-122">-InputObject</span></span>
<span data-ttu-id="63939-123">Das Integrations-Runtime-Objekt.</span><span class="sxs-lookup"><span data-stu-id="63939-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="63939-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="63939-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="63939-125">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="63939-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="63939-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63939-126">-ResourceGroupName</span></span>
<span data-ttu-id="63939-127">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="63939-127">Resource group name.</span></span>

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

### <span data-ttu-id="63939-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63939-128">-ResourceId</span></span>
<span data-ttu-id="63939-129">Ressourcenbezeichner der Synapse-Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="63939-129">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="63939-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="63939-130">-WorkspaceName</span></span>
<span data-ttu-id="63939-131">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="63939-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="63939-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="63939-132">-WorkspaceObject</span></span>
<span data-ttu-id="63939-133">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="63939-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="63939-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63939-134">-Confirm</span></span>
<span data-ttu-id="63939-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="63939-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63939-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="63939-136">-WhatIf</span></span>
<span data-ttu-id="63939-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="63939-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63939-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="63939-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63939-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63939-139">CommonParameters</span></span>
<span data-ttu-id="63939-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63939-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63939-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63939-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63939-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="63939-142">INPUTS</span></span>

### <span data-ttu-id="63939-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="63939-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="63939-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="63939-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="63939-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="63939-145">OUTPUTS</span></span>

### <span data-ttu-id="63939-146">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="63939-146">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="63939-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="63939-147">NOTES</span></span>

## <span data-ttu-id="63939-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="63939-148">RELATED LINKS</span></span>
