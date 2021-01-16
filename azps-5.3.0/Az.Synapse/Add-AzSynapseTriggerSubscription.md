---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/add-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
ms.openlocfilehash: ca5501115b7c75b2e3c1baca368ebaac841e0ae1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384165"
---
# <span data-ttu-id="c2f07-101">Add-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="c2f07-101">Add-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="c2f07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2f07-102">SYNOPSIS</span></span>
<span data-ttu-id="c2f07-103">Abonnieren Sie den Ereignistrigger für Ereignisse externer Dienste.</span><span class="sxs-lookup"><span data-stu-id="c2f07-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="c2f07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c2f07-104">SYNTAX</span></span>

### <span data-ttu-id="c2f07-105">AddByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c2f07-105">AddByName (Default)</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2f07-106">AddByObject</span><span class="sxs-lookup"><span data-stu-id="c2f07-106">AddByObject</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2f07-107">AddByInputObject</span><span class="sxs-lookup"><span data-stu-id="c2f07-107">AddByInputObject</span></span>
```
Add-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2f07-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c2f07-108">DESCRIPTION</span></span>
<span data-ttu-id="c2f07-109">Das **Cmdlet "Add-AzSynapseTriggerSubscription"** abonniert den Ereignistrigger für die angegebenen externen Dienstereignisse aus der Triggerdefinierung.</span><span class="sxs-lookup"><span data-stu-id="c2f07-109">The **Add-AzSynapseTriggerSubscription** cmdlet subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="c2f07-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c2f07-110">EXAMPLES</span></span>

### <span data-ttu-id="c2f07-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c2f07-111">Example 1</span></span>
```powershell
PS C:\> Add-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="c2f07-112">Dieser Befehl abonniert den Trigger "ContosoTrigger" für die angegebenen Ereignisse aus der Triggerdefinierung.</span><span class="sxs-lookup"><span data-stu-id="c2f07-112">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="c2f07-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c2f07-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Add-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="c2f07-114">Dieser Befehl abonniert den Trigger "ContosoTrigger" für die angegebenen Ereignisse von der Definierung des Triggers über die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c2f07-114">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="c2f07-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c2f07-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Add-AzSynapseTriggerSubscription
```

<span data-ttu-id="c2f07-116">Dieser Befehl abonniert den Trigger "ContosoTrigger" für die angegebenen Ereignisse von der Definierung des Triggers über die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c2f07-116">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="c2f07-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2f07-117">PARAMETERS</span></span>

### <span data-ttu-id="c2f07-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2f07-118">-AsJob</span></span>
<span data-ttu-id="c2f07-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c2f07-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c2f07-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2f07-120">-DefaultProfile</span></span>
<span data-ttu-id="c2f07-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2f07-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2f07-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2f07-122">-InputObject</span></span>
<span data-ttu-id="c2f07-123">Das Triggerobjekt.</span><span class="sxs-lookup"><span data-stu-id="c2f07-123">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: AddByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2f07-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c2f07-124">-Name</span></span>
<span data-ttu-id="c2f07-125">Der Auslösername.</span><span class="sxs-lookup"><span data-stu-id="c2f07-125">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: AddByName, AddByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2f07-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c2f07-126">-WorkspaceName</span></span>
<span data-ttu-id="c2f07-127">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="c2f07-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: AddByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2f07-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c2f07-128">-WorkspaceObject</span></span>
<span data-ttu-id="c2f07-129">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="c2f07-129">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: AddByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2f07-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2f07-130">-Confirm</span></span>
<span data-ttu-id="c2f07-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c2f07-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2f07-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c2f07-132">-WhatIf</span></span>
<span data-ttu-id="c2f07-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c2f07-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2f07-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2f07-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2f07-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2f07-135">CommonParameters</span></span>
<span data-ttu-id="c2f07-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2f07-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2f07-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2f07-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2f07-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c2f07-138">INPUTS</span></span>

### <span data-ttu-id="c2f07-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c2f07-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="c2f07-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="c2f07-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="c2f07-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c2f07-141">OUTPUTS</span></span>

### <span data-ttu-id="c2f07-142">System.Object</span><span class="sxs-lookup"><span data-stu-id="c2f07-142">System.Object</span></span>
## <span data-ttu-id="c2f07-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c2f07-143">NOTES</span></span>

## <span data-ttu-id="c2f07-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c2f07-144">RELATED LINKS</span></span>
