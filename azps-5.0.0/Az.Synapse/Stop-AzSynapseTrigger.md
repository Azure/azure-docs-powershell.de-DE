---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
ms.openlocfilehash: 4e35814be14c2be3b5ba0fd1ca5960d297590dca
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176805"
---
# <span data-ttu-id="71399-101">Stop-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="71399-101">Stop-AzSynapseTrigger</span></span>

## <span data-ttu-id="71399-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="71399-102">SYNOPSIS</span></span>
<span data-ttu-id="71399-103">Beendet einen Trigger in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="71399-103">Stops a trigger in a workspace.</span></span>

## <span data-ttu-id="71399-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="71399-104">SYNTAX</span></span>

### <span data-ttu-id="71399-105">StopByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="71399-105">StopByName (Default)</span></span>
```
Stop-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71399-106">StopByObject</span><span class="sxs-lookup"><span data-stu-id="71399-106">StopByObject</span></span>
```
Stop-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71399-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="71399-107">StopByInputObject</span></span>
```
Stop-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71399-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71399-108">DESCRIPTION</span></span>
<span data-ttu-id="71399-109">Das Cmdlet " **Stop-AzSynapseTrigger** " beendet einen Trigger in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="71399-109">The **Stop-AzSynapseTrigger** cmdlet stops a trigger in a workspace.</span></span> <span data-ttu-id="71399-110">Wenn sich der Trigger im Zustand "Started" befindet, beendet das Cmdlet den Trigger und ruft keine Pipelines mehr auf.</span><span class="sxs-lookup"><span data-stu-id="71399-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="71399-111">Wenn sich der Trigger bereits im Zustand "beendet" befindet, hat dieses Cmdlet keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="71399-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="71399-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="71399-112">EXAMPLES</span></span>

### <span data-ttu-id="71399-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="71399-113">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="71399-114">Beendet einen Trigger namens ContosoTrigger im Arbeitsbereich ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="71399-114">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="71399-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="71399-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="71399-116">Beendet einen Trigger mit dem Namen ContosoTrigger im Arbeitsbereich ContosoWorkspace durch Pipeline.</span><span class="sxs-lookup"><span data-stu-id="71399-116">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="71399-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="71399-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Stop-AzSynapseTrigger
```

<span data-ttu-id="71399-118">Beenden eines Triggers mit dem Namen ContosoTrigger im Arbeitsbereich ContosoWorkspace through-Pipeline.</span><span class="sxs-lookup"><span data-stu-id="71399-118">Stop a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="71399-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="71399-119">PARAMETERS</span></span>

### <span data-ttu-id="71399-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71399-120">-AsJob</span></span>
<span data-ttu-id="71399-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="71399-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71399-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71399-122">-DefaultProfile</span></span>
<span data-ttu-id="71399-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="71399-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71399-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="71399-124">-InputObject</span></span>
<span data-ttu-id="71399-125">Das Trigger-Objekt.</span><span class="sxs-lookup"><span data-stu-id="71399-125">The trigger object.</span></span>

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

### <span data-ttu-id="71399-126">-Name</span><span class="sxs-lookup"><span data-stu-id="71399-126">-Name</span></span>
<span data-ttu-id="71399-127">Der Name des Triggers.</span><span class="sxs-lookup"><span data-stu-id="71399-127">The trigger name.</span></span>

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

### <span data-ttu-id="71399-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71399-128">-PassThru</span></span>
<span data-ttu-id="71399-129">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="71399-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="71399-130">Wenn dieser Schalter angegeben wird, wird true zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="71399-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="71399-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="71399-131">-WorkspaceName</span></span>
<span data-ttu-id="71399-132">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="71399-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="71399-133">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="71399-133">-WorkspaceObject</span></span>
<span data-ttu-id="71399-134">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="71399-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="71399-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="71399-135">-Confirm</span></span>
<span data-ttu-id="71399-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="71399-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71399-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71399-137">-WhatIf</span></span>
<span data-ttu-id="71399-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="71399-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71399-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="71399-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71399-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71399-140">CommonParameters</span></span>
<span data-ttu-id="71399-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71399-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71399-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71399-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71399-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="71399-143">INPUTS</span></span>

### <span data-ttu-id="71399-144">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="71399-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="71399-145">Microsoft. Azure. Commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="71399-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="71399-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="71399-146">OUTPUTS</span></span>

### <span data-ttu-id="71399-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="71399-147">System.Boolean</span></span>

## <span data-ttu-id="71399-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="71399-148">NOTES</span></span>

## <span data-ttu-id="71399-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="71399-149">RELATED LINKS</span></span>
