---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
ms.openlocfilehash: 0852cbbce26e1f95bfb75975418fae30038316ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939187"
---
# <span data-ttu-id="79877-101">Set-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="79877-101">Set-AzSynapseTrigger</span></span>

## <span data-ttu-id="79877-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79877-102">SYNOPSIS</span></span>
<span data-ttu-id="79877-103">Erstellt einen Trigger in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="79877-103">Creates a trigger in a workspace.</span></span>

## <span data-ttu-id="79877-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79877-104">SYNTAX</span></span>

### <span data-ttu-id="79877-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="79877-105">SetByName (Default)</span></span>
```
Set-AzSynapseTrigger -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79877-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="79877-106">SetByObject</span></span>
```
Set-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79877-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79877-107">DESCRIPTION</span></span>
<span data-ttu-id="79877-108">Das **Set-AzSynapseTrigger-Cmdlet** erstellt einen Trigger in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="79877-108">The **Set-AzSynapseTrigger** cmdlet creates a trigger in a workspace.</span></span> <span data-ttu-id="79877-109">Trigger werden im Zustand "Beendet" erstellt, d. h., sie beginnen nicht sofort mit dem Aufrufen von Pipelines, auf die sie verweisen.</span><span class="sxs-lookup"><span data-stu-id="79877-109">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="79877-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="79877-110">EXAMPLES</span></span>

### <span data-ttu-id="79877-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="79877-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="79877-112">Erstellen Sie im Arbeitsbereich ContosoWorkspace einen neuen Trigger namens ContosoTrigger.</span><span class="sxs-lookup"><span data-stu-id="79877-112">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span> <span data-ttu-id="79877-113">Der Trigger wird im Zustand "Beendet" erstellt, was bedeutet, dass er nicht sofort gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="79877-113">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="79877-114">Ein Trigger kann mit dem `Start-AzDataFactoryV2Trigger` Cmdlet gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="79877-114">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

### <span data-ttu-id="79877-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="79877-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseTrigger -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="79877-116">Erstellen Sie einen neuen Trigger namens ContosoTrigger im Arbeitsbereich ContosoWorkspace über die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="79877-116">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span> <span data-ttu-id="79877-117">Der Trigger wird im Zustand "Beendet" erstellt, was bedeutet, dass er nicht sofort gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="79877-117">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="79877-118">Ein Trigger kann mit dem `Start-AzDataFactoryV2Trigger` Cmdlet gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="79877-118">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="79877-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="79877-119">PARAMETERS</span></span>

### <span data-ttu-id="79877-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79877-120">-AsJob</span></span>
<span data-ttu-id="79877-121">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="79877-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="79877-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79877-122">-DefaultProfile</span></span>
<span data-ttu-id="79877-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="79877-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79877-124">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="79877-124">-DefinitionFile</span></span>
<span data-ttu-id="79877-125">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="79877-125">The JSON file path.</span></span>

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

### <span data-ttu-id="79877-126">-Name</span><span class="sxs-lookup"><span data-stu-id="79877-126">-Name</span></span>
<span data-ttu-id="79877-127">Der Triggername.</span><span class="sxs-lookup"><span data-stu-id="79877-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79877-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="79877-128">-WorkspaceName</span></span>
<span data-ttu-id="79877-129">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="79877-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="79877-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="79877-130">-WorkspaceObject</span></span>
<span data-ttu-id="79877-131">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="79877-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="79877-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="79877-132">-Confirm</span></span>
<span data-ttu-id="79877-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="79877-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79877-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79877-134">-WhatIf</span></span>
<span data-ttu-id="79877-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="79877-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79877-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="79877-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79877-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79877-137">CommonParameters</span></span>
<span data-ttu-id="79877-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79877-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79877-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79877-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79877-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="79877-140">INPUTS</span></span>

### <span data-ttu-id="79877-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="79877-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="79877-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="79877-142">OUTPUTS</span></span>

### <span data-ttu-id="79877-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="79877-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="79877-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="79877-144">NOTES</span></span>

## <span data-ttu-id="79877-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="79877-145">RELATED LINKS</span></span>
