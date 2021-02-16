---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
ms.openlocfilehash: 747658224703a09f98f232deb865adf4bb084682
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162801"
---
# <span data-ttu-id="2e659-101">Remove-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="2e659-101">Remove-AzSynapsePipeline</span></span>

## <span data-ttu-id="2e659-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e659-102">SYNOPSIS</span></span>
<span data-ttu-id="2e659-103">Entfernt eine Pipeline aus dem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="2e659-103">Removes a pipeline from workspace.</span></span>

## <span data-ttu-id="2e659-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e659-104">SYNTAX</span></span>

### <span data-ttu-id="2e659-105">RemoveByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="2e659-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapsePipeline -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e659-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="2e659-106">RemoveByObject</span></span>
```
Remove-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e659-107">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="2e659-107">NewByInputObject</span></span>
```
Remove-AzSynapsePipeline -Name <String> -InputObject <PSPipelineResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e659-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2e659-108">DESCRIPTION</span></span>
<span data-ttu-id="2e659-109">Das **Cmdlet "Remove-AzSynapsePipeline"** entfernt eine Pipeline aus dem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="2e659-109">The **Remove-AzSynapsePipeline** cmdlet removes a pipeline from workspace.</span></span>

## <span data-ttu-id="2e659-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2e659-110">EXAMPLES</span></span>

### <span data-ttu-id="2e659-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2e659-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="2e659-112">Mit diesem Cmdlet wird die Pipeline mit dem Namen "ContosoPipeline" aus dem Arbeitsbereich "ContosoWorkspace" entfernt.</span><span class="sxs-lookup"><span data-stu-id="2e659-112">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="2e659-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2e659-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="2e659-114">Mit diesem Cmdlet wird die Pipeline namens "ContosoPipeline" über die Pipeline aus dem Arbeitsbereich "ContosoWorkspace" entfernt.</span><span class="sxs-lookup"><span data-stu-id="2e659-114">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="2e659-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="2e659-115">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Remove-AzSynapsePipeline
```

<span data-ttu-id="2e659-116">Mit diesem Cmdlet wird die Pipeline namens "ContosoPipeline" über die Pipeline aus dem Arbeitsbereich "ContosoWorkspace" entfernt.</span><span class="sxs-lookup"><span data-stu-id="2e659-116">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="2e659-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e659-117">PARAMETERS</span></span>

### <span data-ttu-id="2e659-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e659-118">-AsJob</span></span>
<span data-ttu-id="2e659-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2e659-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2e659-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e659-120">-DefaultProfile</span></span>
<span data-ttu-id="2e659-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2e659-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e659-122">-Force</span><span class="sxs-lookup"><span data-stu-id="2e659-122">-Force</span></span>
<span data-ttu-id="2e659-123">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="2e659-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2e659-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e659-124">-InputObject</span></span>
<span data-ttu-id="2e659-125">Das Pipelineobjekt.</span><span class="sxs-lookup"><span data-stu-id="2e659-125">The pipeline object.</span></span>

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

### <span data-ttu-id="2e659-126">-Name</span><span class="sxs-lookup"><span data-stu-id="2e659-126">-Name</span></span>
<span data-ttu-id="2e659-127">Der Pipelinename.</span><span class="sxs-lookup"><span data-stu-id="2e659-127">The pipeline name.</span></span>

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

### <span data-ttu-id="2e659-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e659-128">-PassThru</span></span>
<span data-ttu-id="2e659-129">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="2e659-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="2e659-130">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="2e659-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="2e659-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2e659-131">-WorkspaceName</span></span>
<span data-ttu-id="2e659-132">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="2e659-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="2e659-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2e659-133">-WorkspaceObject</span></span>
<span data-ttu-id="2e659-134">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="2e659-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2e659-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e659-135">-Confirm</span></span>
<span data-ttu-id="2e659-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2e659-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e659-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2e659-137">-WhatIf</span></span>
<span data-ttu-id="2e659-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2e659-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e659-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2e659-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e659-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e659-140">CommonParameters</span></span>
<span data-ttu-id="2e659-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e659-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e659-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e659-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e659-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2e659-143">INPUTS</span></span>

### <span data-ttu-id="2e659-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2e659-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="2e659-145">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="2e659-145">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="2e659-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2e659-146">OUTPUTS</span></span>

### <span data-ttu-id="2e659-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2e659-147">System.Boolean</span></span>

## <span data-ttu-id="2e659-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2e659-148">NOTES</span></span>

## <span data-ttu-id="2e659-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2e659-149">RELATED LINKS</span></span>
