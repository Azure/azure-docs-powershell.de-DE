---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
ms.openlocfilehash: fc8f24cb124194bc2d2acd5ab5f19a4484571079
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007682"
---
# <span data-ttu-id="271b7-101">Invoke-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="271b7-101">Invoke-AzSynapsePipeline</span></span>

## <span data-ttu-id="271b7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="271b7-102">SYNOPSIS</span></span>
<span data-ttu-id="271b7-103">Ruft eine Pipeline auf, um einen Testlauf zu starten.</span><span class="sxs-lookup"><span data-stu-id="271b7-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="271b7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="271b7-104">SYNTAX</span></span>

### <span data-ttu-id="271b7-105">NewByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="271b7-105">NewByName (Default)</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceName <String> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="271b7-106">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="271b7-106">NewByInputObject</span></span>
```
Invoke-AzSynapsePipeline -InputObject <PSPipelineResource> [-Parameter <Hashtable>] [-ParameterFile <String>]
 [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="271b7-107">NewByObject</span><span class="sxs-lookup"><span data-stu-id="271b7-107">NewByObject</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="271b7-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="271b7-108">DESCRIPTION</span></span>
<span data-ttu-id="271b7-109">Der Befehl **Invoke-AzSynapsePipeline** startet eine Ausführung für die angegebene Pipeline und gibt eine ID für diesen Testlauf zurück.</span><span class="sxs-lookup"><span data-stu-id="271b7-109">The **Invoke-AzSynapsePipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="271b7-110">Diese GUID kann an **Get-AzSynapsePipelineRun** oder **Get-AzSynapseActivityRun** übergeben werden, um weitere Details zu diesem Testlauf abzurufen.</span><span class="sxs-lookup"><span data-stu-id="271b7-110">This GUID can be passed to **Get-AzSynapsePipelineRun** or **Get-AzSynapseActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="271b7-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="271b7-111">EXAMPLES</span></span>

### <span data-ttu-id="271b7-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="271b7-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapsePipeline -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline
```

<span data-ttu-id="271b7-113">Mit diesem Befehl wird im Arbeitsbereich ContosoWorkspace ein Run für Pipeline mit dem Namen ContosoPipeline gestartet.</span><span class="sxs-lookup"><span data-stu-id="271b7-113">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="271b7-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="271b7-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Invoke-AzSynapsePipeline -PipelineName ContosoPipeline
```

<span data-ttu-id="271b7-115">Mit diesem Befehl wird im Arbeitsbereich ContosoWorkspace through-Pipeline ein Run für Pipeline mit dem Namen ContosoPipeline gestartet.</span><span class="sxs-lookup"><span data-stu-id="271b7-115">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="271b7-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="271b7-116">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Invoke-AzSynapsePipeline
```

<span data-ttu-id="271b7-117">Mit diesem Befehl wird im Arbeitsbereich ContosoWorkspace through-Pipeline ein Run für Pipeline mit dem Namen ContosoPipeline gestartet.</span><span class="sxs-lookup"><span data-stu-id="271b7-117">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="271b7-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="271b7-118">PARAMETERS</span></span>

### <span data-ttu-id="271b7-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="271b7-119">-AsJob</span></span>
<span data-ttu-id="271b7-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="271b7-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="271b7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="271b7-121">-DefaultProfile</span></span>
<span data-ttu-id="271b7-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="271b7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="271b7-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="271b7-123">-InputObject</span></span>
<span data-ttu-id="271b7-124">Die Informationen zur Pipeline werden ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="271b7-124">The information about the pipeline run.</span></span>

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

### <span data-ttu-id="271b7-125">-Isrecovery</span><span class="sxs-lookup"><span data-stu-id="271b7-125">-IsRecovery</span></span>
<span data-ttu-id="271b7-126">Flag für den Wiederherstellungsmodus.</span><span class="sxs-lookup"><span data-stu-id="271b7-126">Recovery mode flag.</span></span>
<span data-ttu-id="271b7-127">Wenn der Wiederherstellungsmodus auf "true" festgelegt ist, wird die angegebene referenzierte Pipeline ausgeführt und der neue Run unter derselben Gruppen-Nr gruppiert.</span><span class="sxs-lookup"><span data-stu-id="271b7-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

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

### <span data-ttu-id="271b7-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="271b7-128">-Parameter</span></span>
<span data-ttu-id="271b7-129">Parameter für Pipelineausführung.</span><span class="sxs-lookup"><span data-stu-id="271b7-129">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="271b7-130">-Parameterdatei</span><span class="sxs-lookup"><span data-stu-id="271b7-130">-ParameterFile</span></span>
<span data-ttu-id="271b7-131">Der Name der Datei mit Parametern für die Pipelineausführung.</span><span class="sxs-lookup"><span data-stu-id="271b7-131">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="271b7-132">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="271b7-132">-PipelineName</span></span>
<span data-ttu-id="271b7-133">Der Name der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="271b7-133">The pipeline name.</span></span>

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

### <span data-ttu-id="271b7-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="271b7-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="271b7-135">Die Pipeline Lauf-ID für die erneute Ausführung.</span><span class="sxs-lookup"><span data-stu-id="271b7-135">The pipeline run ID for rerun.</span></span>
<span data-ttu-id="271b7-136">Wenn die Run-ID angegeben ist, werden die Parameter des angegebenen Laufs zum Erstellen eines neuen Laufs verwendet.</span><span class="sxs-lookup"><span data-stu-id="271b7-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

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

### <span data-ttu-id="271b7-137">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="271b7-137">-StartActivityName</span></span>
<span data-ttu-id="271b7-138">Im Wiederherstellungsmodus wird die erneute Ausführung von dieser Aktivität gestartet.</span><span class="sxs-lookup"><span data-stu-id="271b7-138">In recovery mode, the rerun will start from this activity.</span></span>
<span data-ttu-id="271b7-139">Wenn nicht angegeben, werden alle Aktivitäten ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="271b7-139">If not specified, all activities will run.</span></span>

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

### <span data-ttu-id="271b7-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="271b7-140">-WorkspaceName</span></span>
<span data-ttu-id="271b7-141">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="271b7-141">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="271b7-142">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="271b7-142">-WorkspaceObject</span></span>
<span data-ttu-id="271b7-143">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="271b7-143">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="271b7-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="271b7-144">-Confirm</span></span>
<span data-ttu-id="271b7-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="271b7-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="271b7-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="271b7-146">-WhatIf</span></span>
<span data-ttu-id="271b7-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="271b7-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="271b7-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="271b7-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="271b7-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="271b7-149">CommonParameters</span></span>
<span data-ttu-id="271b7-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="271b7-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="271b7-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="271b7-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="271b7-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="271b7-152">INPUTS</span></span>

### <span data-ttu-id="271b7-153">Microsoft. Azure. Commands. Synapse. Models. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="271b7-153">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

### <span data-ttu-id="271b7-154">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="271b7-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="271b7-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="271b7-155">OUTPUTS</span></span>

### <span data-ttu-id="271b7-156">Microsoft. Azure. Commands. Synapse. Models. PSCreateRunResponse</span><span class="sxs-lookup"><span data-stu-id="271b7-156">Microsoft.Azure.Commands.Synapse.Models.PSCreateRunResponse</span></span>

## <span data-ttu-id="271b7-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="271b7-157">NOTES</span></span>

## <span data-ttu-id="271b7-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="271b7-158">RELATED LINKS</span></span>
