---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
ms.openlocfilehash: 2bce821f55b5f8ff39f56fa8a6960cb1f99b47d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178111"
---
# <span data-ttu-id="7bd33-101">Set-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="7bd33-101">Set-AzSynapsePipeline</span></span>

## <span data-ttu-id="7bd33-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7bd33-102">SYNOPSIS</span></span>
<span data-ttu-id="7bd33-103">Erstellt eine Pipeline im Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="7bd33-103">Creates a pipeline in workspace.</span></span>

## <span data-ttu-id="7bd33-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7bd33-104">SYNTAX</span></span>

### <span data-ttu-id="7bd33-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7bd33-105">SetByName (Default)</span></span>
```
Set-AzSynapsePipeline -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bd33-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="7bd33-106">SetByObject</span></span>
```
Set-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bd33-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7bd33-107">DESCRIPTION</span></span>
<span data-ttu-id="7bd33-108">Das Cmdlet " **Satz-AzSynapsePipeline** " erstellt eine Pipeline im Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="7bd33-108">The **Set-AzSynapsePipeline** cmdlet creates a pipeline in workspace.</span></span>

## <span data-ttu-id="7bd33-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7bd33-109">EXAMPLES</span></span>

### <span data-ttu-id="7bd33-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7bd33-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="7bd33-111">Dieser Befehl erstellt eine Pipeline mit dem Namen ContosoPipeline im Arbeitsbereich mit dem Namen ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="7bd33-111">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="7bd33-112">Der Befehl basiert auf Informationen in der pipeline.jsfür die Datei.</span><span class="sxs-lookup"><span data-stu-id="7bd33-112">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="7bd33-113">Diese Datei enthält Informationen zu Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="7bd33-113">This file includes information about activities.</span></span>

### <span data-ttu-id="7bd33-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7bd33-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapsePipeline -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="7bd33-115">Dieser Befehl erstellt eine Pipeline mit dem Namen ContosoPipeline im Arbeitsbereich mit dem Namen ContosoWorkspace through Pipeline.</span><span class="sxs-lookup"><span data-stu-id="7bd33-115">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>
<span data-ttu-id="7bd33-116">Der Befehl basiert auf Informationen in der pipeline.jsfür die Datei.</span><span class="sxs-lookup"><span data-stu-id="7bd33-116">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="7bd33-117">Diese Datei enthält Informationen zu Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="7bd33-117">This file includes information about activities.</span></span>

## <span data-ttu-id="7bd33-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="7bd33-118">PARAMETERS</span></span>

### <span data-ttu-id="7bd33-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7bd33-119">-AsJob</span></span>
<span data-ttu-id="7bd33-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7bd33-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7bd33-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bd33-121">-DefaultProfile</span></span>
<span data-ttu-id="7bd33-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7bd33-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bd33-123">-Definitions-Nr.</span><span class="sxs-lookup"><span data-stu-id="7bd33-123">-DefinitionFile</span></span>
<span data-ttu-id="7bd33-124">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="7bd33-124">The JSON file path.</span></span>

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

### <span data-ttu-id="7bd33-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7bd33-125">-Name</span></span>
<span data-ttu-id="7bd33-126">Der Name der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="7bd33-126">The pipeline name.</span></span>

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

### <span data-ttu-id="7bd33-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7bd33-127">-WorkspaceName</span></span>
<span data-ttu-id="7bd33-128">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="7bd33-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7bd33-129">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="7bd33-129">-WorkspaceObject</span></span>
<span data-ttu-id="7bd33-130">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="7bd33-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="7bd33-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7bd33-131">-Confirm</span></span>
<span data-ttu-id="7bd33-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7bd33-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bd33-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bd33-133">-WhatIf</span></span>
<span data-ttu-id="7bd33-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7bd33-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bd33-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7bd33-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bd33-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bd33-136">CommonParameters</span></span>
<span data-ttu-id="7bd33-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bd33-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bd33-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7bd33-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bd33-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7bd33-139">INPUTS</span></span>

### <span data-ttu-id="7bd33-140">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7bd33-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="7bd33-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7bd33-141">OUTPUTS</span></span>

### <span data-ttu-id="7bd33-142">Microsoft. Azure. Commands. Synapse. Models. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="7bd33-142">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="7bd33-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="7bd33-143">NOTES</span></span>

## <span data-ttu-id="7bd33-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7bd33-144">RELATED LINKS</span></span>
