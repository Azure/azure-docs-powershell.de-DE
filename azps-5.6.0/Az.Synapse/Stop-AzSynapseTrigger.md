---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/stop-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
ms.openlocfilehash: 94773a882a4bb2d29712fff6796d34cff6254df1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939136"
---
# <span data-ttu-id="5b208-101">Stop-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="5b208-101">Stop-AzSynapseTrigger</span></span>

## <span data-ttu-id="5b208-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b208-102">SYNOPSIS</span></span>
<span data-ttu-id="5b208-103">Beendet einen Trigger in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="5b208-103">Stops a trigger in a workspace.</span></span>

## <span data-ttu-id="5b208-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5b208-104">SYNTAX</span></span>

### <span data-ttu-id="5b208-105">StopByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="5b208-105">StopByName (Default)</span></span>
```
Stop-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b208-106">StopByObject</span><span class="sxs-lookup"><span data-stu-id="5b208-106">StopByObject</span></span>
```
Stop-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b208-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="5b208-107">StopByInputObject</span></span>
```
Stop-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b208-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5b208-108">DESCRIPTION</span></span>
<span data-ttu-id="5b208-109">Das **Cmdlet Stop-AzSynapseTrigger** beendet einen Trigger in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="5b208-109">The **Stop-AzSynapseTrigger** cmdlet stops a trigger in a workspace.</span></span> <span data-ttu-id="5b208-110">Wenn sich der Trigger im Zustand "Gestartet" befindet, beendet das Cmdlet den Trigger und ruft keine Pipelines mehr auf.</span><span class="sxs-lookup"><span data-stu-id="5b208-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="5b208-111">Wenn sich der Trigger bereits im Zustand "Beendet" befindet, hat dieses Cmdlet keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="5b208-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="5b208-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5b208-112">EXAMPLES</span></span>

### <span data-ttu-id="5b208-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5b208-113">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="5b208-114">Beendet einen Trigger namens ContosoTrigger im Arbeitsbereich ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="5b208-114">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="5b208-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5b208-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="5b208-116">Beendet einen Trigger namens ContosoTrigger im Arbeitsbereich ContosoWorkspace über die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5b208-116">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="5b208-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="5b208-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Stop-AzSynapseTrigger
```

<span data-ttu-id="5b208-118">Beenden Sie einen Trigger namens ContosoTrigger im Arbeitsbereich ContosoWorkspace über die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5b208-118">Stop a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="5b208-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5b208-119">PARAMETERS</span></span>

### <span data-ttu-id="5b208-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b208-120">-AsJob</span></span>
<span data-ttu-id="5b208-121">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5b208-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5b208-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b208-122">-DefaultProfile</span></span>
<span data-ttu-id="5b208-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5b208-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b208-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b208-124">-InputObject</span></span>
<span data-ttu-id="5b208-125">Das Triggerobjekt.</span><span class="sxs-lookup"><span data-stu-id="5b208-125">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b208-126">-Name</span><span class="sxs-lookup"><span data-stu-id="5b208-126">-Name</span></span>
<span data-ttu-id="5b208-127">Der Triggername.</span><span class="sxs-lookup"><span data-stu-id="5b208-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByName, StopByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b208-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b208-128">-PassThru</span></span>
<span data-ttu-id="5b208-129">Dieses Cmdlet gibt standardmäßig kein -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="5b208-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="5b208-130">Wenn dieser Schalter angegeben ist, gibt er "true" zurück, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="5b208-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="5b208-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5b208-131">-WorkspaceName</span></span>
<span data-ttu-id="5b208-132">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="5b208-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b208-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5b208-133">-WorkspaceObject</span></span>
<span data-ttu-id="5b208-134">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="5b208-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StopByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b208-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5b208-135">-Confirm</span></span>
<span data-ttu-id="5b208-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5b208-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b208-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b208-137">-WhatIf</span></span>
<span data-ttu-id="5b208-138">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5b208-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5b208-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5b208-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b208-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b208-140">CommonParameters</span></span>
<span data-ttu-id="5b208-141">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b208-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b208-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b208-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b208-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5b208-143">INPUTS</span></span>

### <span data-ttu-id="5b208-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5b208-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="5b208-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="5b208-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="5b208-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5b208-146">OUTPUTS</span></span>

### <span data-ttu-id="5b208-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5b208-147">System.Boolean</span></span>

## <span data-ttu-id="5b208-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5b208-148">NOTES</span></span>

## <span data-ttu-id="5b208-149">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5b208-149">RELATED LINKS</span></span>
