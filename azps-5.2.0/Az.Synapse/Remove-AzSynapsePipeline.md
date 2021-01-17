---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
ms.openlocfilehash: 747658224703a09f98f232deb865adf4bb084682
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364999"
---
# <span data-ttu-id="cf3e5-101">Remove-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="cf3e5-101">Remove-AzSynapsePipeline</span></span>

## <span data-ttu-id="cf3e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf3e5-102">SYNOPSIS</span></span>
<span data-ttu-id="cf3e5-103">Entfernt eine Pipeline aus dem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="cf3e5-103">Removes a pipeline from workspace.</span></span>

## <span data-ttu-id="cf3e5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf3e5-104">SYNTAX</span></span>

### <span data-ttu-id="cf3e5-105">RemoveByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="cf3e5-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapsePipeline -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf3e5-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="cf3e5-106">RemoveByObject</span></span>
```
Remove-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf3e5-107">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="cf3e5-107">NewByInputObject</span></span>
```
Remove-AzSynapsePipeline -Name <String> -InputObject <PSPipelineResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf3e5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cf3e5-108">DESCRIPTION</span></span>
<span data-ttu-id="cf3e5-109">Das **Cmdlet "Remove-AzSynapsePipeline"** entfernt eine Pipeline aus dem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="cf3e5-109">The **Remove-AzSynapsePipeline** cmdlet removes a pipeline from workspace.</span></span>

## <span data-ttu-id="cf3e5-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cf3e5-110">EXAMPLES</span></span>

### <span data-ttu-id="cf3e5-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cf3e5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="cf3e5-112">Mit diesem Cmdlet wird die Pipeline namens "ContosoPipeline" aus dem Arbeitsbereich "ContosoWorkspace" entfernt.</span><span class="sxs-lookup"><span data-stu-id="cf3e5-112">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="cf3e5-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="cf3e5-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="cf3e5-114">Mit diesem Cmdlet wird die Pipeline namens "ContosoPipeline" über die Pipeline aus dem Arbeitsbereich "ContosoWorkspace" entfernt.</span><span class="sxs-lookup"><span data-stu-id="cf3e5-114">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="cf3e5-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="cf3e5-115">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Remove-AzSynapsePipeline
```

<span data-ttu-id="cf3e5-116">Mit diesem Cmdlet wird die Pipeline namens "ContosoPipeline" über die Pipeline aus dem Arbeitsbereich "ContosoWorkspace" entfernt.</span><span class="sxs-lookup"><span data-stu-id="cf3e5-116">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="cf3e5-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf3e5-117">PARAMETERS</span></span>

### <span data-ttu-id="cf3e5-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf3e5-118">-AsJob</span></span>
<span data-ttu-id="cf3e5-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="cf3e5-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cf3e5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf3e5-120">-DefaultProfile</span></span>
<span data-ttu-id="cf3e5-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cf3e5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf3e5-122">-Force</span><span class="sxs-lookup"><span data-stu-id="cf3e5-122">-Force</span></span>
<span data-ttu-id="cf3e5-123">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="cf3e5-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cf3e5-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf3e5-124">-InputObject</span></span>
<span data-ttu-id="cf3e5-125">Das Pipelineobjekt.</span><span class="sxs-lookup"><span data-stu-id="cf3e5-125">The pipeline object.</span></span>

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

### <span data-ttu-id="cf3e5-126">-Name</span><span class="sxs-lookup"><span data-stu-id="cf3e5-126">-Name</span></span>
<span data-ttu-id="cf3e5-127">Der Pipelinename.</span><span class="sxs-lookup"><span data-stu-id="cf3e5-127">The pipeline name.</span></span>

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

### <span data-ttu-id="cf3e5-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf3e5-128">-PassThru</span></span>
<span data-ttu-id="cf3e5-129">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="cf3e5-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="cf3e5-130">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="cf3e5-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="cf3e5-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cf3e5-131">-WorkspaceName</span></span>
<span data-ttu-id="cf3e5-132">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="cf3e5-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="cf3e5-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="cf3e5-133">-WorkspaceObject</span></span>
<span data-ttu-id="cf3e5-134">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="cf3e5-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="cf3e5-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf3e5-135">-Confirm</span></span>
<span data-ttu-id="cf3e5-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cf3e5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf3e5-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="cf3e5-137">-WhatIf</span></span>
<span data-ttu-id="cf3e5-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cf3e5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf3e5-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cf3e5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf3e5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf3e5-140">CommonParameters</span></span>
<span data-ttu-id="cf3e5-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf3e5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf3e5-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf3e5-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf3e5-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cf3e5-143">INPUTS</span></span>

### <span data-ttu-id="cf3e5-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cf3e5-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="cf3e5-145">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="cf3e5-145">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="cf3e5-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cf3e5-146">OUTPUTS</span></span>

### <span data-ttu-id="cf3e5-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cf3e5-147">System.Boolean</span></span>

## <span data-ttu-id="cf3e5-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cf3e5-148">NOTES</span></span>

## <span data-ttu-id="cf3e5-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cf3e5-149">RELATED LINKS</span></span>
