---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
ms.openlocfilehash: f907afbc573d558a08d514c019cbcbe3fa999bf6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383115"
---
# <span data-ttu-id="770d8-101">Stop-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="770d8-101">Stop-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="770d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="770d8-102">SYNOPSIS</span></span>
<span data-ttu-id="770d8-103">Beendet die Ausführung einer Pipeline in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="770d8-103">Stops a pipeline run in a workspace.</span></span>

## <span data-ttu-id="770d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="770d8-104">SYNTAX</span></span>

### <span data-ttu-id="770d8-105">RemoveByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="770d8-105">RemoveByName (Default)</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="770d8-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="770d8-106">RemoveByObject</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="770d8-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="770d8-107">RemoveByInputObject</span></span>
```
Stop-AzSynapsePipelineRun -InputObject <PSPipelineRun> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="770d8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="770d8-108">DESCRIPTION</span></span>
<span data-ttu-id="770d8-109">Das **Cmdlet "Stop-AzSynapsePipelineRun"** beendet die Ausführung einer Pipeline in einem Arbeitsbereich, der mit der Pipelinelauf-ID angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="770d8-109">The **Stop-AzSynapsePipelineRun** cmdlet stops a pipeline run in a workspace specified with the pipeline run ID.</span></span>

## <span data-ttu-id="770d8-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="770d8-110">EXAMPLES</span></span>

### <span data-ttu-id="770d8-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="770d8-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="770d8-112">Dieser Befehl beendet die Ausführung der Pipeline mit id b9730a13-aa12-4926-a8b3-8e3a974ab0bd im Arbeitsbereich ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="770d8-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="770d8-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="770d8-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapsePipelineRun -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="770d8-114">Dieser Befehl beendet die Ausführung der Pipeline mit id b9730a13-aa12-4926-a8b3-8e3a974ab0bd im Arbeitsbereich ContosoWorkspace über die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="770d8-114">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="770d8-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="770d8-115">Example 3</span></span>
```powershell
PS C:\> $pipelineRun = Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
PS C:\> $pipelineRun | Stop-AzSynapsePipelineRun
```

<span data-ttu-id="770d8-116">Dieser Befehl beendet die Ausführung der Pipeline mit id b9730a13-aa12-4926-a8b3-8e3a974ab0bd im Arbeitsbereich ContosoWorkspace über die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="770d8-116">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="770d8-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="770d8-117">PARAMETERS</span></span>

### <span data-ttu-id="770d8-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="770d8-118">-AsJob</span></span>
<span data-ttu-id="770d8-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="770d8-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="770d8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="770d8-120">-DefaultProfile</span></span>
<span data-ttu-id="770d8-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="770d8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="770d8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="770d8-122">-InputObject</span></span>
<span data-ttu-id="770d8-123">Die Informationen zur Ausführung der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="770d8-123">The information about the pipeline run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="770d8-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="770d8-124">-PassThru</span></span>
<span data-ttu-id="770d8-125">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="770d8-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="770d8-126">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="770d8-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="770d8-127">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="770d8-127">-PipelineRunId</span></span>
<span data-ttu-id="770d8-128">Der Pipeline-Ausführungsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="770d8-128">The pipeline run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770d8-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="770d8-129">-WorkspaceName</span></span>
<span data-ttu-id="770d8-130">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="770d8-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="770d8-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="770d8-131">-WorkspaceObject</span></span>
<span data-ttu-id="770d8-132">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="770d8-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="770d8-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="770d8-133">-Confirm</span></span>
<span data-ttu-id="770d8-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="770d8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="770d8-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="770d8-135">-WhatIf</span></span>
<span data-ttu-id="770d8-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="770d8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="770d8-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="770d8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="770d8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="770d8-138">CommonParameters</span></span>
<span data-ttu-id="770d8-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="770d8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="770d8-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="770d8-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="770d8-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="770d8-141">INPUTS</span></span>

### <span data-ttu-id="770d8-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="770d8-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="770d8-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="770d8-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="770d8-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="770d8-144">OUTPUTS</span></span>

### <span data-ttu-id="770d8-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="770d8-145">System.Boolean</span></span>

## <span data-ttu-id="770d8-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="770d8-146">NOTES</span></span>

## <span data-ttu-id="770d8-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="770d8-147">RELATED LINKS</span></span>
