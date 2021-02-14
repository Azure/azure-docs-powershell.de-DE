---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/add-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
ms.openlocfilehash: ca5501115b7c75b2e3c1baca368ebaac841e0ae1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150041"
---
# <span data-ttu-id="8633a-101">Add-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="8633a-101">Add-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="8633a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8633a-102">SYNOPSIS</span></span>
<span data-ttu-id="8633a-103">Abonnieren Sie den Ereignistrigger für Ereignisse externer Dienste.</span><span class="sxs-lookup"><span data-stu-id="8633a-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="8633a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8633a-104">SYNTAX</span></span>

### <span data-ttu-id="8633a-105">AddByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="8633a-105">AddByName (Default)</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8633a-106">AddByObject</span><span class="sxs-lookup"><span data-stu-id="8633a-106">AddByObject</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8633a-107">AddByInputObject</span><span class="sxs-lookup"><span data-stu-id="8633a-107">AddByInputObject</span></span>
```
Add-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8633a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8633a-108">DESCRIPTION</span></span>
<span data-ttu-id="8633a-109">Das **Cmdlet "Add-AzSynapseTriggerSubscription"** abonniert den Ereignistrigger für die angegebenen externen Dienstereignisse aus der Triggerdefinierung.</span><span class="sxs-lookup"><span data-stu-id="8633a-109">The **Add-AzSynapseTriggerSubscription** cmdlet subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="8633a-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8633a-110">EXAMPLES</span></span>

### <span data-ttu-id="8633a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8633a-111">Example 1</span></span>
```powershell
PS C:\> Add-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="8633a-112">Dieser Befehl abonniert den Trigger "ContosoTrigger" für die angegebenen Ereignisse aus der Triggerdefinierung.</span><span class="sxs-lookup"><span data-stu-id="8633a-112">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="8633a-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8633a-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Add-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="8633a-114">Dieser Befehl abonniert den Trigger "ContosoTrigger" für die angegebenen Ereignisse von der Definierung des Triggers über die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="8633a-114">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="8633a-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="8633a-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Add-AzSynapseTriggerSubscription
```

<span data-ttu-id="8633a-116">Dieser Befehl abonniert den Trigger "ContosoTrigger" für die angegebenen Ereignisse von der Definierung des Triggers über die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="8633a-116">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="8633a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8633a-117">PARAMETERS</span></span>

### <span data-ttu-id="8633a-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8633a-118">-AsJob</span></span>
<span data-ttu-id="8633a-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8633a-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8633a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8633a-120">-DefaultProfile</span></span>
<span data-ttu-id="8633a-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8633a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8633a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8633a-122">-InputObject</span></span>
<span data-ttu-id="8633a-123">Das Triggerobjekt.</span><span class="sxs-lookup"><span data-stu-id="8633a-123">The trigger object.</span></span>

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

### <span data-ttu-id="8633a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="8633a-124">-Name</span></span>
<span data-ttu-id="8633a-125">Der Auslösername.</span><span class="sxs-lookup"><span data-stu-id="8633a-125">The trigger name.</span></span>

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

### <span data-ttu-id="8633a-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8633a-126">-WorkspaceName</span></span>
<span data-ttu-id="8633a-127">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="8633a-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8633a-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8633a-128">-WorkspaceObject</span></span>
<span data-ttu-id="8633a-129">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="8633a-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8633a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8633a-130">-Confirm</span></span>
<span data-ttu-id="8633a-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8633a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8633a-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8633a-132">-WhatIf</span></span>
<span data-ttu-id="8633a-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8633a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8633a-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8633a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8633a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8633a-135">CommonParameters</span></span>
<span data-ttu-id="8633a-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8633a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8633a-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8633a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8633a-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8633a-138">INPUTS</span></span>

### <span data-ttu-id="8633a-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8633a-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="8633a-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="8633a-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="8633a-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8633a-141">OUTPUTS</span></span>

### <span data-ttu-id="8633a-142">System.Object</span><span class="sxs-lookup"><span data-stu-id="8633a-142">System.Object</span></span>
## <span data-ttu-id="8633a-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8633a-143">NOTES</span></span>

## <span data-ttu-id="8633a-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8633a-144">RELATED LINKS</span></span>
