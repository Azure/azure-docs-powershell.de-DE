---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/start-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
ms.openlocfilehash: d2488a99bba1813c192df5ef8561d83c06f2f6e7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167187"
---
# <span data-ttu-id="34095-101">Start-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="34095-101">Start-AzSynapseTrigger</span></span>

## <span data-ttu-id="34095-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="34095-102">SYNOPSIS</span></span>
<span data-ttu-id="34095-103">Startet einen Trigger in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="34095-103">Starts a trigger in a workspace.</span></span>

## <span data-ttu-id="34095-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="34095-104">SYNTAX</span></span>

### <span data-ttu-id="34095-105">StartByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="34095-105">StartByName (Default)</span></span>
```
Start-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34095-106">StartByObject</span><span class="sxs-lookup"><span data-stu-id="34095-106">StartByObject</span></span>
```
Start-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34095-107">StartByInputObject</span><span class="sxs-lookup"><span data-stu-id="34095-107">StartByInputObject</span></span>
```
Start-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34095-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34095-108">DESCRIPTION</span></span>
<span data-ttu-id="34095-109">Mit dem Cmdlet **Start-AzSynapseTrigger** wird ein Trigger in einem Arbeitsbereich gestartet.</span><span class="sxs-lookup"><span data-stu-id="34095-109">The **Start-AzSynapseTrigger** cmdlet starts a trigger in a workspace.</span></span> <span data-ttu-id="34095-110">Wenn sich der Trigger im Zustand "stopped" befindet, startet das Cmdlet den Trigger und ruft schließlich Pipelines basierend auf seiner Definition auf.</span><span class="sxs-lookup"><span data-stu-id="34095-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="34095-111">Wenn sich der Trigger bereits im Zustand "Started" befindet, hat dieses Cmdlet keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="34095-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="34095-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="34095-112">EXAMPLES</span></span>

### <span data-ttu-id="34095-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="34095-113">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="34095-114">Startet einen Trigger namens ContosoTrigger im Arbeitsbereich ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="34095-114">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="34095-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="34095-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Start-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="34095-116">Startet einen Trigger namens ContosoTrigger im Arbeitsbereich ContosoWorkspace through-Pipeline.</span><span class="sxs-lookup"><span data-stu-id="34095-116">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="34095-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="34095-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Start-AzSynapseTrigger
```

<span data-ttu-id="34095-118">Startet einen Trigger namens ContosoTrigger im Arbeitsbereich ContosoWorkspace through-Pipeline.</span><span class="sxs-lookup"><span data-stu-id="34095-118">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="34095-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="34095-119">PARAMETERS</span></span>

### <span data-ttu-id="34095-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="34095-120">-AsJob</span></span>
<span data-ttu-id="34095-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="34095-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="34095-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34095-122">-DefaultProfile</span></span>
<span data-ttu-id="34095-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="34095-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34095-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="34095-124">-InputObject</span></span>
<span data-ttu-id="34095-125">Das Trigger-Objekt.</span><span class="sxs-lookup"><span data-stu-id="34095-125">The trigger object.</span></span>

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

### <span data-ttu-id="34095-126">-Name</span><span class="sxs-lookup"><span data-stu-id="34095-126">-Name</span></span>
<span data-ttu-id="34095-127">Der Name des Triggers.</span><span class="sxs-lookup"><span data-stu-id="34095-127">The trigger name.</span></span>

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

### <span data-ttu-id="34095-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34095-128">-PassThru</span></span>
<span data-ttu-id="34095-129">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="34095-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="34095-130">Wenn dieser Schalter angegeben wird, wird true zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="34095-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="34095-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="34095-131">-WorkspaceName</span></span>
<span data-ttu-id="34095-132">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="34095-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="34095-133">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="34095-133">-WorkspaceObject</span></span>
<span data-ttu-id="34095-134">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="34095-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="34095-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="34095-135">-Confirm</span></span>
<span data-ttu-id="34095-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="34095-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34095-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34095-137">-WhatIf</span></span>
<span data-ttu-id="34095-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="34095-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="34095-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="34095-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34095-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34095-140">CommonParameters</span></span>
<span data-ttu-id="34095-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34095-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34095-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34095-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34095-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="34095-143">INPUTS</span></span>

### <span data-ttu-id="34095-144">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="34095-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="34095-145">Microsoft. Azure. Commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="34095-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="34095-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="34095-146">OUTPUTS</span></span>

### <span data-ttu-id="34095-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="34095-147">System.Boolean</span></span>

## <span data-ttu-id="34095-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="34095-148">NOTES</span></span>

## <span data-ttu-id="34095-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="34095-149">RELATED LINKS</span></span>
