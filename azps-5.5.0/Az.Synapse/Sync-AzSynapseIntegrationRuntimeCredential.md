---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/sync-azsynapseintegrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
ms.openlocfilehash: feb9d74cf49dfa8ae5455b303ee78f443a08e942
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173529"
---
# <span data-ttu-id="c6640-101">Sync-AzSynapseIntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="c6640-101">Sync-AzSynapseIntegrationRuntimeCredential</span></span>

## <span data-ttu-id="c6640-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6640-102">SYNOPSIS</span></span>
<span data-ttu-id="c6640-103">Synchronisiert Anmeldeinformationen zwischen Integrations-Runtime-Knoten.</span><span class="sxs-lookup"><span data-stu-id="c6640-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="c6640-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6640-104">SYNTAX</span></span>

### <span data-ttu-id="c6640-105">StopByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c6640-105">StopByNameParameterSet (Default)</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6640-106">StopByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6640-106">StopByParentObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -IntegrationRuntimeName <String>
 -WorkspaceObject <PSSynapseWorkspace> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6640-107">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6640-107">StopByResourceIdParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -ResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6640-108">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6640-108">StopByInputObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6640-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6640-109">DESCRIPTION</span></span>
<span data-ttu-id="c6640-110">Das **Cmdlet Sync-AzSynapseIntegrationRuntimeCredential** synchronisiert lokale Anmeldeinformationen zwischen Integrations-Runtime-Knoten, wodurch die Identischheit der Anmeldeinformationen in allen Knoten erzwingt wird.</span><span class="sxs-lookup"><span data-stu-id="c6640-110">The **Sync-AzSynapseIntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="c6640-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c6640-111">EXAMPLES</span></span>

### <span data-ttu-id="c6640-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c6640-112">Example 1</span></span>
```powershell
PS C:\> Sync-AzSynapseIntegrationRuntimeCredential -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir'
```

<span data-ttu-id="c6640-113">Synchronisiert Anmeldeinformationen zwischen Integrations-Runtime-Knoten.</span><span class="sxs-lookup"><span data-stu-id="c6640-113">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="c6640-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6640-114">PARAMETERS</span></span>

### <span data-ttu-id="c6640-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6640-115">-DefaultProfile</span></span>
<span data-ttu-id="c6640-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6640-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6640-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c6640-117">-Force</span></span>
<span data-ttu-id="c6640-118">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="c6640-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c6640-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6640-119">-InputObject</span></span>
<span data-ttu-id="c6640-120">Das Integrations-Runtime-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c6640-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: StopByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6640-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="c6640-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="c6640-122">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="c6640-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet, StopByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6640-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6640-123">-ResourceGroupName</span></span>
<span data-ttu-id="c6640-124">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="c6640-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6640-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6640-125">-ResourceId</span></span>
<span data-ttu-id="c6640-126">Ressourcenbezeichner der Laufzeit der Synapse-Integration.</span><span class="sxs-lookup"><span data-stu-id="c6640-126">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6640-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c6640-127">-WorkspaceName</span></span>
<span data-ttu-id="c6640-128">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="c6640-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6640-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c6640-129">-WorkspaceObject</span></span>
<span data-ttu-id="c6640-130">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="c6640-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StopByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6640-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6640-131">-Confirm</span></span>
<span data-ttu-id="c6640-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c6640-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6640-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c6640-133">-WhatIf</span></span>
<span data-ttu-id="c6640-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c6640-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6640-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c6640-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6640-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6640-136">CommonParameters</span></span>
<span data-ttu-id="c6640-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6640-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6640-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6640-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6640-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c6640-139">INPUTS</span></span>

### <span data-ttu-id="c6640-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c6640-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="c6640-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c6640-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="c6640-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c6640-142">OUTPUTS</span></span>

### <span data-ttu-id="c6640-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="c6640-143">System.Void</span></span>

## <span data-ttu-id="c6640-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c6640-144">NOTES</span></span>

## <span data-ttu-id="c6640-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c6640-145">RELATED LINKS</span></span>
