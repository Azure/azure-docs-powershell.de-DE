---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
ms.openlocfilehash: fc8f24cb124194bc2d2acd5ab5f19a4484571079
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383674"
---
# <span data-ttu-id="f5da6-101">Invoke-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="f5da6-101">Invoke-AzSynapsePipeline</span></span>

## <span data-ttu-id="f5da6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5da6-102">SYNOPSIS</span></span>
<span data-ttu-id="f5da6-103">Ruft eine Pipeline auf, um eine Ausführung dafür zu starten.</span><span class="sxs-lookup"><span data-stu-id="f5da6-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="f5da6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f5da6-104">SYNTAX</span></span>

### <span data-ttu-id="f5da6-105">NewByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="f5da6-105">NewByName (Default)</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceName <String> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5da6-106">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="f5da6-106">NewByInputObject</span></span>
```
Invoke-AzSynapsePipeline -InputObject <PSPipelineResource> [-Parameter <Hashtable>] [-ParameterFile <String>]
 [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5da6-107">NewByObject</span><span class="sxs-lookup"><span data-stu-id="f5da6-107">NewByObject</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5da6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f5da6-108">DESCRIPTION</span></span>
<span data-ttu-id="f5da6-109">Der **Befehl "Invoke-AzSynapsePipeline"** startet eine Ausführung für die angegebene Pipeline und gibt eine ID für diese Ausführung zurück.</span><span class="sxs-lookup"><span data-stu-id="f5da6-109">The **Invoke-AzSynapsePipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="f5da6-110">Diese GUID kann an **"Get-AzSynapsePipelineRun"** oder **"Get-AzSynapseActivityRun"** übergeben werden, um weitere Details zu dieser Ausführung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f5da6-110">This GUID can be passed to **Get-AzSynapsePipelineRun** or **Get-AzSynapseActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="f5da6-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f5da6-111">EXAMPLES</span></span>

### <span data-ttu-id="f5da6-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f5da6-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapsePipeline -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline
```

<span data-ttu-id="f5da6-113">Dieser Befehl startet eine Ausführung für die Pipeline namens "ContosoPipeline" im Arbeitsbereich "ContosoWorkspace".</span><span class="sxs-lookup"><span data-stu-id="f5da6-113">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="f5da6-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f5da6-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Invoke-AzSynapsePipeline -PipelineName ContosoPipeline
```

<span data-ttu-id="f5da6-115">Mit diesem Befehl wird eine Ausführung für die Pipeline namens "ContosoPipeline" im Arbeitsbereich "ContosoWorkspace" über die Pipeline gestartet.</span><span class="sxs-lookup"><span data-stu-id="f5da6-115">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="f5da6-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="f5da6-116">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Invoke-AzSynapsePipeline
```

<span data-ttu-id="f5da6-117">Mit diesem Befehl wird eine Ausführung für die Pipeline namens "ContosoPipeline" im Arbeitsbereich "ContosoWorkspace" über die Pipeline gestartet.</span><span class="sxs-lookup"><span data-stu-id="f5da6-117">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="f5da6-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5da6-118">PARAMETERS</span></span>

### <span data-ttu-id="f5da6-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5da6-119">-AsJob</span></span>
<span data-ttu-id="f5da6-120">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f5da6-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f5da6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5da6-121">-DefaultProfile</span></span>
<span data-ttu-id="f5da6-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f5da6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5da6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5da6-123">-InputObject</span></span>
<span data-ttu-id="f5da6-124">Die Informationen zur Ausführung der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="f5da6-124">The information about the pipeline run.</span></span>

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

### <span data-ttu-id="f5da6-125">-IsRecovery</span><span class="sxs-lookup"><span data-stu-id="f5da6-125">-IsRecovery</span></span>
<span data-ttu-id="f5da6-126">Kennzeichen für den Wiederherstellungsmodus.</span><span class="sxs-lookup"><span data-stu-id="f5da6-126">Recovery mode flag.</span></span>
<span data-ttu-id="f5da6-127">Wenn der Wiederherstellungsmodus auf "true" festgelegt ist, werden die angegebene Pipeline, auf die verwiesen wird, und die neue Ausführung unter derselben groupId gruppieren.</span><span class="sxs-lookup"><span data-stu-id="f5da6-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

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

### <span data-ttu-id="f5da6-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="f5da6-128">-Parameter</span></span>
<span data-ttu-id="f5da6-129">Parameter für die Ausführung der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="f5da6-129">Parameters for pipeline run.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5da6-130">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="f5da6-130">-ParameterFile</span></span>
<span data-ttu-id="f5da6-131">Der Name der Datei mit Parametern für die Ausführung der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="f5da6-131">The name of the file with parameters for pipeline run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5da6-132">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="f5da6-132">-PipelineName</span></span>
<span data-ttu-id="f5da6-133">Der Pipelinename.</span><span class="sxs-lookup"><span data-stu-id="f5da6-133">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByName, NewByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5da6-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="f5da6-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="f5da6-135">Die Pipeline-Ausführungs-ID für die erneute Ausführung.</span><span class="sxs-lookup"><span data-stu-id="f5da6-135">The pipeline run ID for rerun.</span></span>
<span data-ttu-id="f5da6-136">Wenn "Run ID" angegeben wird, werden die Parameter der angegebenen Ausführung verwendet, um eine neue Ausführung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f5da6-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5da6-137">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="f5da6-137">-StartActivityName</span></span>
<span data-ttu-id="f5da6-138">Im Wiederherstellungsmodus beginnt der erneute Ausführen mit dieser Aktivität.</span><span class="sxs-lookup"><span data-stu-id="f5da6-138">In recovery mode, the rerun will start from this activity.</span></span>
<span data-ttu-id="f5da6-139">Wenn nicht angegeben, werden alle Aktivitäten ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f5da6-139">If not specified, all activities will run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5da6-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f5da6-140">-WorkspaceName</span></span>
<span data-ttu-id="f5da6-141">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="f5da6-141">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5da6-142">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f5da6-142">-WorkspaceObject</span></span>
<span data-ttu-id="f5da6-143">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f5da6-143">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: NewByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5da6-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f5da6-144">-Confirm</span></span>
<span data-ttu-id="f5da6-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f5da6-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5da6-146">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f5da6-146">-WhatIf</span></span>
<span data-ttu-id="f5da6-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f5da6-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5da6-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f5da6-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5da6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5da6-149">CommonParameters</span></span>
<span data-ttu-id="f5da6-150">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5da6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5da6-151">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5da6-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5da6-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f5da6-152">INPUTS</span></span>

### <span data-ttu-id="f5da6-153">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="f5da6-153">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

### <span data-ttu-id="f5da6-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f5da6-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f5da6-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f5da6-155">OUTPUTS</span></span>

### <span data-ttu-id="f5da6-156">Microsoft.Azure.Commands.Synapse.Models.PSCreateRunResponse</span><span class="sxs-lookup"><span data-stu-id="f5da6-156">Microsoft.Azure.Commands.Synapse.Models.PSCreateRunResponse</span></span>

## <span data-ttu-id="f5da6-157">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f5da6-157">NOTES</span></span>

## <span data-ttu-id="f5da6-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f5da6-158">RELATED LINKS</span></span>
