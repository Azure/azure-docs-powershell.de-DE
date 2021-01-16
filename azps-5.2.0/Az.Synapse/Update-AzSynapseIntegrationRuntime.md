---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 31647da87319ca6be90962f34d128f5e2c922d47
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293590"
---
# <span data-ttu-id="ab1f1-101">Update-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ab1f1-101">Update-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="ab1f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab1f1-102">SYNOPSIS</span></span>
<span data-ttu-id="ab1f1-103">Aktualisiert eine Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="ab1f1-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="ab1f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab1f1-104">SYNTAX</span></span>

### <span data-ttu-id="ab1f1-105">UpdateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ab1f1-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab1f1-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab1f1-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab1f1-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab1f1-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -ResourceId <String> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ab1f1-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab1f1-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ab1f1-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ab1f1-109">DESCRIPTION</span></span>
<span data-ttu-id="ab1f1-110">Das **Cmdlet "Update-AzSynapseIntegrationRuntime"** aktualisiert Integrationslaufzeiteigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ab1f1-110">The **Update-AzSynapseIntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="ab1f1-111">Derzeit unterstützt das Cmdlet nur das Aktualisieren von "AutoUpdate" und "AutoUpdateDelayOffset" für selbst gehostete Integrationslaufzeiten.</span><span class="sxs-lookup"><span data-stu-id="ab1f1-111">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="ab1f1-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ab1f1-112">EXAMPLES</span></span>

### <span data-ttu-id="ab1f1-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ab1f1-113">Example 1</span></span>
```powershell
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -AutoUpdate Off -AutoUpdateDelayOffset $ts
```

<span data-ttu-id="ab1f1-114">Das Cmdlet aktualisiert die selbst gehostete Integrationslaufzeit mit dem Namen "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="ab1f1-114">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="ab1f1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab1f1-115">PARAMETERS</span></span>

### <span data-ttu-id="ab1f1-116">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="ab1f1-116">-AutoUpdate</span></span>
<span data-ttu-id="ab1f1-117">Aktivieren oder deaktivieren Sie die automatische Aktualisierung der selbst gehosteten Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="ab1f1-117">Enable or disable the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="ab1f1-118">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="ab1f1-118">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="ab1f1-119">Die Tageszeit für die automatische Aktualisierung der selbst gehosteten Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="ab1f1-119">The time of the day for the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="ab1f1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab1f1-120">-DefaultProfile</span></span>
<span data-ttu-id="ab1f1-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab1f1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab1f1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab1f1-122">-InputObject</span></span>
<span data-ttu-id="ab1f1-123">Das Integrations-Runtime-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ab1f1-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="ab1f1-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="ab1f1-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="ab1f1-125">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="ab1f1-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="ab1f1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab1f1-126">-ResourceGroupName</span></span>
<span data-ttu-id="ab1f1-127">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="ab1f1-127">Resource group name.</span></span>

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

### <span data-ttu-id="ab1f1-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab1f1-128">-ResourceId</span></span>
<span data-ttu-id="ab1f1-129">Ressourcenbezeichner der Laufzeit der Synapse-Integration.</span><span class="sxs-lookup"><span data-stu-id="ab1f1-129">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="ab1f1-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ab1f1-130">-WorkspaceName</span></span>
<span data-ttu-id="ab1f1-131">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="ab1f1-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ab1f1-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ab1f1-132">-WorkspaceObject</span></span>
<span data-ttu-id="ab1f1-133">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="ab1f1-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ab1f1-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ab1f1-134">-Confirm</span></span>
<span data-ttu-id="ab1f1-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ab1f1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab1f1-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ab1f1-136">-WhatIf</span></span>
<span data-ttu-id="ab1f1-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ab1f1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab1f1-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ab1f1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab1f1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab1f1-139">CommonParameters</span></span>
<span data-ttu-id="ab1f1-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab1f1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab1f1-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ab1f1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab1f1-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ab1f1-142">INPUTS</span></span>

### <span data-ttu-id="ab1f1-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ab1f1-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ab1f1-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ab1f1-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="ab1f1-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ab1f1-145">OUTPUTS</span></span>

### <span data-ttu-id="ab1f1-146">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="ab1f1-146">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="ab1f1-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ab1f1-147">NOTES</span></span>

## <span data-ttu-id="ab1f1-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ab1f1-148">RELATED LINKS</span></span>
