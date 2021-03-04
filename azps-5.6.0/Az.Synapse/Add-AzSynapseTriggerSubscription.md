---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/add-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
ms.openlocfilehash: d9ff2e46b7b4ccf7b3d2fafd1aa8142efd0675b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933304"
---
# <span data-ttu-id="ab042-101">Add-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="ab042-101">Add-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="ab042-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab042-102">SYNOPSIS</span></span>
<span data-ttu-id="ab042-103">Abonnieren Sie den Ereignistrigger für externe Dienstereignisse.</span><span class="sxs-lookup"><span data-stu-id="ab042-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="ab042-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab042-104">SYNTAX</span></span>

### <span data-ttu-id="ab042-105">AddByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="ab042-105">AddByName (Default)</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab042-106">AddByObject</span><span class="sxs-lookup"><span data-stu-id="ab042-106">AddByObject</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab042-107">AddByInputObject</span><span class="sxs-lookup"><span data-stu-id="ab042-107">AddByInputObject</span></span>
```
Add-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab042-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ab042-108">DESCRIPTION</span></span>
<span data-ttu-id="ab042-109">Das **Add-AzSynapseTriggerSubscription-Cmdlet** abonniert den Ereignistrigger für die angegebenen externen Dienstereignisse aus der Triggerdefintion.</span><span class="sxs-lookup"><span data-stu-id="ab042-109">The **Add-AzSynapseTriggerSubscription** cmdlet subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="ab042-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ab042-110">EXAMPLES</span></span>

### <span data-ttu-id="ab042-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ab042-111">Example 1</span></span>
```powershell
PS C:\> Add-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="ab042-112">Dieser Befehl abonniert den Trigger "ContosoTrigger" für die angegebenen Ereignisse aus der Triggerdefintion.</span><span class="sxs-lookup"><span data-stu-id="ab042-112">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="ab042-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ab042-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Add-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="ab042-114">Dieser Befehl abonniert den Trigger "ContosoTrigger" für die angegebenen Ereignisse aus der Triggerdefintion über die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ab042-114">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="ab042-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ab042-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Add-AzSynapseTriggerSubscription
```

<span data-ttu-id="ab042-116">Dieser Befehl abonniert den Trigger "ContosoTrigger" für die angegebenen Ereignisse aus der Triggerdefintion über die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ab042-116">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="ab042-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ab042-117">PARAMETERS</span></span>

### <span data-ttu-id="ab042-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab042-118">-AsJob</span></span>
<span data-ttu-id="ab042-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ab042-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ab042-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab042-120">-DefaultProfile</span></span>
<span data-ttu-id="ab042-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab042-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab042-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab042-122">-InputObject</span></span>
<span data-ttu-id="ab042-123">Das Triggerobjekt.</span><span class="sxs-lookup"><span data-stu-id="ab042-123">The trigger object.</span></span>

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

### <span data-ttu-id="ab042-124">-Name</span><span class="sxs-lookup"><span data-stu-id="ab042-124">-Name</span></span>
<span data-ttu-id="ab042-125">Der Triggername.</span><span class="sxs-lookup"><span data-stu-id="ab042-125">The trigger name.</span></span>

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

### <span data-ttu-id="ab042-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ab042-126">-WorkspaceName</span></span>
<span data-ttu-id="ab042-127">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="ab042-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ab042-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ab042-128">-WorkspaceObject</span></span>
<span data-ttu-id="ab042-129">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="ab042-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ab042-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ab042-130">-Confirm</span></span>
<span data-ttu-id="ab042-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ab042-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab042-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab042-132">-WhatIf</span></span>
<span data-ttu-id="ab042-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ab042-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab042-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ab042-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab042-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab042-135">CommonParameters</span></span>
<span data-ttu-id="ab042-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab042-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab042-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab042-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab042-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ab042-138">INPUTS</span></span>

### <span data-ttu-id="ab042-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ab042-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ab042-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="ab042-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="ab042-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ab042-141">OUTPUTS</span></span>

### <span data-ttu-id="ab042-142">System.Object</span><span class="sxs-lookup"><span data-stu-id="ab042-142">System.Object</span></span>
## <span data-ttu-id="ab042-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ab042-143">NOTES</span></span>

## <span data-ttu-id="ab042-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ab042-144">RELATED LINKS</span></span>
