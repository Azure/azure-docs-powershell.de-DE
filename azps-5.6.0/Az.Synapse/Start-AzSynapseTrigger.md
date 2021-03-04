---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/start-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
ms.openlocfilehash: 39801db0d1cd400fa88868b87098260c9148daa3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939163"
---
# <span data-ttu-id="b024c-101">Start-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="b024c-101">Start-AzSynapseTrigger</span></span>

## <span data-ttu-id="b024c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b024c-102">SYNOPSIS</span></span>
<span data-ttu-id="b024c-103">Startet einen Trigger in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="b024c-103">Starts a trigger in a workspace.</span></span>

## <span data-ttu-id="b024c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b024c-104">SYNTAX</span></span>

### <span data-ttu-id="b024c-105">StartByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b024c-105">StartByName (Default)</span></span>
```
Start-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b024c-106">StartByObject</span><span class="sxs-lookup"><span data-stu-id="b024c-106">StartByObject</span></span>
```
Start-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b024c-107">StartByInputObject</span><span class="sxs-lookup"><span data-stu-id="b024c-107">StartByInputObject</span></span>
```
Start-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b024c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b024c-108">DESCRIPTION</span></span>
<span data-ttu-id="b024c-109">Das **Cmdlet Start-AzSynapseTrigger** startet einen Trigger in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="b024c-109">The **Start-AzSynapseTrigger** cmdlet starts a trigger in a workspace.</span></span> <span data-ttu-id="b024c-110">Wenn sich der Trigger im Zustand "Beendet" befindet, startet das Cmdlet den Trigger und ruft schließlich Pipelines basierend auf seiner Definition auf.</span><span class="sxs-lookup"><span data-stu-id="b024c-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="b024c-111">Wenn sich der Trigger bereits im Zustand "Gestartet" befindet, hat dieses Cmdlet keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="b024c-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="b024c-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b024c-112">EXAMPLES</span></span>

### <span data-ttu-id="b024c-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b024c-113">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="b024c-114">Startet einen Trigger namens ContosoTrigger im Arbeitsbereich ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="b024c-114">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="b024c-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b024c-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Start-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="b024c-116">Startet einen Trigger namens ContosoTrigger im Arbeitsbereich ContosoWorkspace über die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b024c-116">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="b024c-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="b024c-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Start-AzSynapseTrigger
```

<span data-ttu-id="b024c-118">Startet einen Trigger namens ContosoTrigger im Arbeitsbereich ContosoWorkspace über die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b024c-118">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="b024c-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b024c-119">PARAMETERS</span></span>

### <span data-ttu-id="b024c-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b024c-120">-AsJob</span></span>
<span data-ttu-id="b024c-121">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b024c-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b024c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b024c-122">-DefaultProfile</span></span>
<span data-ttu-id="b024c-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b024c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b024c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b024c-124">-InputObject</span></span>
<span data-ttu-id="b024c-125">Das Triggerobjekt.</span><span class="sxs-lookup"><span data-stu-id="b024c-125">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: StartByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b024c-126">-Name</span><span class="sxs-lookup"><span data-stu-id="b024c-126">-Name</span></span>
<span data-ttu-id="b024c-127">Der Triggername.</span><span class="sxs-lookup"><span data-stu-id="b024c-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: StartByName, StartByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b024c-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b024c-128">-PassThru</span></span>
<span data-ttu-id="b024c-129">Dieses Cmdlet gibt standardmäßig kein -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="b024c-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="b024c-130">Wenn dieser Schalter angegeben ist, gibt er "true" zurück, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="b024c-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="b024c-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b024c-131">-WorkspaceName</span></span>
<span data-ttu-id="b024c-132">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="b024c-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b024c-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b024c-133">-WorkspaceObject</span></span>
<span data-ttu-id="b024c-134">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="b024c-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StartByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b024c-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b024c-135">-Confirm</span></span>
<span data-ttu-id="b024c-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b024c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b024c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b024c-137">-WhatIf</span></span>
<span data-ttu-id="b024c-138">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b024c-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b024c-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b024c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b024c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b024c-140">CommonParameters</span></span>
<span data-ttu-id="b024c-141">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b024c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b024c-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b024c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b024c-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b024c-143">INPUTS</span></span>

### <span data-ttu-id="b024c-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b024c-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="b024c-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="b024c-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="b024c-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b024c-146">OUTPUTS</span></span>

### <span data-ttu-id="b024c-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b024c-147">System.Boolean</span></span>

## <span data-ttu-id="b024c-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b024c-148">NOTES</span></span>

## <span data-ttu-id="b024c-149">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b024c-149">RELATED LINKS</span></span>
