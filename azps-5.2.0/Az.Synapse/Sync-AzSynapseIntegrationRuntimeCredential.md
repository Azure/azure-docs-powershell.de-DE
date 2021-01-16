---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/sync-azsynapseintegrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
ms.openlocfilehash: feb9d74cf49dfa8ae5455b303ee78f443a08e942
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357116"
---
# <span data-ttu-id="776d6-101">Sync-AzSynapseIntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="776d6-101">Sync-AzSynapseIntegrationRuntimeCredential</span></span>

## <span data-ttu-id="776d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="776d6-102">SYNOPSIS</span></span>
<span data-ttu-id="776d6-103">Synchronisiert Anmeldeinformationen zwischen Integrationslaufzeitknoten.</span><span class="sxs-lookup"><span data-stu-id="776d6-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="776d6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="776d6-104">SYNTAX</span></span>

### <span data-ttu-id="776d6-105">StopByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="776d6-105">StopByNameParameterSet (Default)</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="776d6-106">StopByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="776d6-106">StopByParentObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -IntegrationRuntimeName <String>
 -WorkspaceObject <PSSynapseWorkspace> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="776d6-107">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="776d6-107">StopByResourceIdParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -ResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="776d6-108">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="776d6-108">StopByInputObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="776d6-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="776d6-109">DESCRIPTION</span></span>
<span data-ttu-id="776d6-110">Das **Cmdlet "Sync-AzSynapseIntegrationRuntimeCredential"** synchronisiert lokale Anmeldeinformationen zwischen Integrations-Runtime-Knoten, wodurch die Identischheit der Anmeldeinformationen in allen Knoten erzwingt wird.</span><span class="sxs-lookup"><span data-stu-id="776d6-110">The **Sync-AzSynapseIntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="776d6-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="776d6-111">EXAMPLES</span></span>

### <span data-ttu-id="776d6-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="776d6-112">Example 1</span></span>
```powershell
PS C:\> Sync-AzSynapseIntegrationRuntimeCredential -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir'
```

<span data-ttu-id="776d6-113">Synchronisiert Anmeldeinformationen zwischen Integrations-Runtime-Knoten.</span><span class="sxs-lookup"><span data-stu-id="776d6-113">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="776d6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="776d6-114">PARAMETERS</span></span>

### <span data-ttu-id="776d6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="776d6-115">-DefaultProfile</span></span>
<span data-ttu-id="776d6-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="776d6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="776d6-117">-Force</span><span class="sxs-lookup"><span data-stu-id="776d6-117">-Force</span></span>
<span data-ttu-id="776d6-118">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="776d6-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="776d6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="776d6-119">-InputObject</span></span>
<span data-ttu-id="776d6-120">Das Integrations-Runtime-Objekt.</span><span class="sxs-lookup"><span data-stu-id="776d6-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="776d6-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="776d6-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="776d6-122">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="776d6-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="776d6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="776d6-123">-ResourceGroupName</span></span>
<span data-ttu-id="776d6-124">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="776d6-124">Resource group name.</span></span>

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

### <span data-ttu-id="776d6-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="776d6-125">-ResourceId</span></span>
<span data-ttu-id="776d6-126">Ressourcenbezeichner der Synapse-Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="776d6-126">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="776d6-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="776d6-127">-WorkspaceName</span></span>
<span data-ttu-id="776d6-128">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="776d6-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="776d6-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="776d6-129">-WorkspaceObject</span></span>
<span data-ttu-id="776d6-130">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="776d6-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="776d6-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="776d6-131">-Confirm</span></span>
<span data-ttu-id="776d6-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="776d6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="776d6-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="776d6-133">-WhatIf</span></span>
<span data-ttu-id="776d6-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="776d6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="776d6-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="776d6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="776d6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="776d6-136">CommonParameters</span></span>
<span data-ttu-id="776d6-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="776d6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="776d6-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="776d6-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="776d6-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="776d6-139">INPUTS</span></span>

### <span data-ttu-id="776d6-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="776d6-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="776d6-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="776d6-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="776d6-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="776d6-142">OUTPUTS</span></span>

### <span data-ttu-id="776d6-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="776d6-143">System.Void</span></span>

## <span data-ttu-id="776d6-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="776d6-144">NOTES</span></span>

## <span data-ttu-id="776d6-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="776d6-145">RELATED LINKS</span></span>
