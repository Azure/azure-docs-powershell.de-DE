---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
ms.openlocfilehash: 2bce821f55b5f8ff39f56fa8a6960cb1f99b47d0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307275"
---
# <span data-ttu-id="db518-101">Set-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="db518-101">Set-AzSynapsePipeline</span></span>

## <span data-ttu-id="db518-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db518-102">SYNOPSIS</span></span>
<span data-ttu-id="db518-103">Erstellt eine Pipeline im Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="db518-103">Creates a pipeline in workspace.</span></span>

## <span data-ttu-id="db518-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db518-104">SYNTAX</span></span>

### <span data-ttu-id="db518-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="db518-105">SetByName (Default)</span></span>
```
Set-AzSynapsePipeline -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db518-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="db518-106">SetByObject</span></span>
```
Set-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db518-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="db518-107">DESCRIPTION</span></span>
<span data-ttu-id="db518-108">Das **Cmdlet "Set-AzSynapsePipeline"** erstellt eine Pipeline im Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="db518-108">The **Set-AzSynapsePipeline** cmdlet creates a pipeline in workspace.</span></span>

## <span data-ttu-id="db518-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="db518-109">EXAMPLES</span></span>

### <span data-ttu-id="db518-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="db518-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="db518-111">Mit diesem Befehl wird eine Pipeline namens "ContosoPipeline" im Arbeitsbereich "ContosoWorkspace" erstellt.</span><span class="sxs-lookup"><span data-stu-id="db518-111">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="db518-112">Der Befehl basiert auf Der Pipeline basiert auf Informationen in pipeline.jsDatei.</span><span class="sxs-lookup"><span data-stu-id="db518-112">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="db518-113">Diese Datei enthält Informationen zu Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="db518-113">This file includes information about activities.</span></span>

### <span data-ttu-id="db518-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="db518-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapsePipeline -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="db518-115">Mit diesem Befehl wird eine Pipeline namens "ContosoPipeline" im Arbeitsbereich namens "ContosoWorkspace" über die Pipeline erstellt.</span><span class="sxs-lookup"><span data-stu-id="db518-115">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>
<span data-ttu-id="db518-116">Der Befehl basiert auf Informationen in der pipeline.jsDatei.</span><span class="sxs-lookup"><span data-stu-id="db518-116">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="db518-117">Diese Datei enthält Informationen zu Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="db518-117">This file includes information about activities.</span></span>

## <span data-ttu-id="db518-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db518-118">PARAMETERS</span></span>

### <span data-ttu-id="db518-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db518-119">-AsJob</span></span>
<span data-ttu-id="db518-120">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="db518-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db518-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db518-121">-DefaultProfile</span></span>
<span data-ttu-id="db518-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="db518-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db518-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="db518-123">-DefinitionFile</span></span>
<span data-ttu-id="db518-124">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="db518-124">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db518-125">-Name</span><span class="sxs-lookup"><span data-stu-id="db518-125">-Name</span></span>
<span data-ttu-id="db518-126">Der Pipelinename.</span><span class="sxs-lookup"><span data-stu-id="db518-126">The pipeline name.</span></span>

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

### <span data-ttu-id="db518-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="db518-127">-WorkspaceName</span></span>
<span data-ttu-id="db518-128">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="db518-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db518-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="db518-129">-WorkspaceObject</span></span>
<span data-ttu-id="db518-130">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="db518-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db518-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db518-131">-Confirm</span></span>
<span data-ttu-id="db518-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="db518-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db518-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="db518-133">-WhatIf</span></span>
<span data-ttu-id="db518-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="db518-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db518-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="db518-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db518-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db518-136">CommonParameters</span></span>
<span data-ttu-id="db518-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db518-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db518-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db518-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db518-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="db518-139">INPUTS</span></span>

### <span data-ttu-id="db518-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="db518-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="db518-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="db518-141">OUTPUTS</span></span>

### <span data-ttu-id="db518-142">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="db518-142">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="db518-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="db518-143">NOTES</span></span>

## <span data-ttu-id="db518-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="db518-144">RELATED LINKS</span></span>
