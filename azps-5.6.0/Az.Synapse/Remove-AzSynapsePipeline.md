---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
ms.openlocfilehash: b7bd7866ec6c6ff41a6ef7474b71cfc880e28f49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933515"
---
# <span data-ttu-id="fea3d-101">Remove-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="fea3d-101">Remove-AzSynapsePipeline</span></span>

## <span data-ttu-id="fea3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fea3d-102">SYNOPSIS</span></span>
<span data-ttu-id="fea3d-103">Entfernt eine Pipeline aus dem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="fea3d-103">Removes a pipeline from workspace.</span></span>

## <span data-ttu-id="fea3d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fea3d-104">SYNTAX</span></span>

### <span data-ttu-id="fea3d-105">RemoveByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="fea3d-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapsePipeline -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fea3d-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="fea3d-106">RemoveByObject</span></span>
```
Remove-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fea3d-107">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="fea3d-107">NewByInputObject</span></span>
```
Remove-AzSynapsePipeline -Name <String> -InputObject <PSPipelineResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fea3d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fea3d-108">DESCRIPTION</span></span>
<span data-ttu-id="fea3d-109">Das **Cmdlet Remove-AzSynapsePipeline** entfernt eine Pipeline aus dem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="fea3d-109">The **Remove-AzSynapsePipeline** cmdlet removes a pipeline from workspace.</span></span>

## <span data-ttu-id="fea3d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fea3d-110">EXAMPLES</span></span>

### <span data-ttu-id="fea3d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fea3d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="fea3d-112">Dieses Cmdlet entfernt die Pipeline namens ContosoPipeline aus dem Arbeitsbereich namens ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="fea3d-112">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="fea3d-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fea3d-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="fea3d-114">Dieses Cmdlet entfernt die Pipeline namens ContosoPipeline aus dem Arbeitsbereich namens ContosoWorkspace über die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="fea3d-114">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="fea3d-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="fea3d-115">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Remove-AzSynapsePipeline
```

<span data-ttu-id="fea3d-116">Dieses Cmdlet entfernt die Pipeline namens ContosoPipeline aus dem Arbeitsbereich namens ContosoWorkspace über die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="fea3d-116">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="fea3d-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fea3d-117">PARAMETERS</span></span>

### <span data-ttu-id="fea3d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fea3d-118">-AsJob</span></span>
<span data-ttu-id="fea3d-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="fea3d-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fea3d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fea3d-120">-DefaultProfile</span></span>
<span data-ttu-id="fea3d-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fea3d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fea3d-122">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="fea3d-122">-Force</span></span>
<span data-ttu-id="fea3d-123">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="fea3d-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="fea3d-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fea3d-124">-InputObject</span></span>
<span data-ttu-id="fea3d-125">Das Pipelineobjekt.</span><span class="sxs-lookup"><span data-stu-id="fea3d-125">The pipeline object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource
Parameter Sets: NewByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fea3d-126">-Name</span><span class="sxs-lookup"><span data-stu-id="fea3d-126">-Name</span></span>
<span data-ttu-id="fea3d-127">Der Name der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="fea3d-127">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fea3d-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fea3d-128">-PassThru</span></span>
<span data-ttu-id="fea3d-129">Dieses Cmdlet gibt standardmäßig kein -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="fea3d-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="fea3d-130">Wenn dieser Schalter angegeben ist, gibt er "true" zurück, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="fea3d-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="fea3d-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fea3d-131">-WorkspaceName</span></span>
<span data-ttu-id="fea3d-132">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="fea3d-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fea3d-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="fea3d-133">-WorkspaceObject</span></span>
<span data-ttu-id="fea3d-134">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="fea3d-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fea3d-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fea3d-135">-Confirm</span></span>
<span data-ttu-id="fea3d-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fea3d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fea3d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fea3d-137">-WhatIf</span></span>
<span data-ttu-id="fea3d-138">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fea3d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fea3d-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fea3d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fea3d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fea3d-140">CommonParameters</span></span>
<span data-ttu-id="fea3d-141">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fea3d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fea3d-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fea3d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fea3d-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fea3d-143">INPUTS</span></span>

### <span data-ttu-id="fea3d-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="fea3d-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="fea3d-145">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="fea3d-145">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="fea3d-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fea3d-146">OUTPUTS</span></span>

### <span data-ttu-id="fea3d-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fea3d-147">System.Boolean</span></span>

## <span data-ttu-id="fea3d-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fea3d-148">NOTES</span></span>

## <span data-ttu-id="fea3d-149">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fea3d-149">RELATED LINKS</span></span>
