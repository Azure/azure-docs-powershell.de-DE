---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/add-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
ms.openlocfilehash: ca5501115b7c75b2e3c1baca368ebaac841e0ae1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166733"
---
# <span data-ttu-id="1cc9e-101">Add-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="1cc9e-101">Add-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="1cc9e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1cc9e-102">SYNOPSIS</span></span>
<span data-ttu-id="1cc9e-103">Abonnieren Sie den Ereignisauslöser für externe Dienstereignisse.</span><span class="sxs-lookup"><span data-stu-id="1cc9e-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="1cc9e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1cc9e-104">SYNTAX</span></span>

### <span data-ttu-id="1cc9e-105">AddByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="1cc9e-105">AddByName (Default)</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cc9e-106">AddByObject</span><span class="sxs-lookup"><span data-stu-id="1cc9e-106">AddByObject</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cc9e-107">AddByInputObject</span><span class="sxs-lookup"><span data-stu-id="1cc9e-107">AddByInputObject</span></span>
```
Add-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cc9e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1cc9e-108">DESCRIPTION</span></span>
<span data-ttu-id="1cc9e-109">Das Cmdlet **Add-AzSynapseTriggerSubscription** abonniert den Ereignistrigger für die angegebenen externen Dienstereignisse aus dem Trigger-Definition.</span><span class="sxs-lookup"><span data-stu-id="1cc9e-109">The **Add-AzSynapseTriggerSubscription** cmdlet subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="1cc9e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1cc9e-110">EXAMPLES</span></span>

### <span data-ttu-id="1cc9e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1cc9e-111">Example 1</span></span>
```powershell
PS C:\> Add-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="1cc9e-112">Dieser Befehl abonniert Trigger namens ContosoTrigger zu den angegebenen Ereignissen aus dem Trigger-Definition.</span><span class="sxs-lookup"><span data-stu-id="1cc9e-112">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="1cc9e-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1cc9e-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Add-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="1cc9e-114">Dieser Befehl abonniert Trigger namens ContosoTrigger zu den angegebenen Ereignissen aus dem Trigger Definition through Pipeline.</span><span class="sxs-lookup"><span data-stu-id="1cc9e-114">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="1cc9e-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="1cc9e-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Add-AzSynapseTriggerSubscription
```

<span data-ttu-id="1cc9e-116">Dieser Befehl abonniert Trigger namens ContosoTrigger zu den angegebenen Ereignissen aus dem Trigger Definition through Pipeline.</span><span class="sxs-lookup"><span data-stu-id="1cc9e-116">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="1cc9e-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="1cc9e-117">PARAMETERS</span></span>

### <span data-ttu-id="1cc9e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1cc9e-118">-AsJob</span></span>
<span data-ttu-id="1cc9e-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1cc9e-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1cc9e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cc9e-120">-DefaultProfile</span></span>
<span data-ttu-id="1cc9e-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1cc9e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cc9e-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1cc9e-122">-InputObject</span></span>
<span data-ttu-id="1cc9e-123">Das Trigger-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1cc9e-123">The trigger object.</span></span>

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

### <span data-ttu-id="1cc9e-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1cc9e-124">-Name</span></span>
<span data-ttu-id="1cc9e-125">Der Name des Triggers.</span><span class="sxs-lookup"><span data-stu-id="1cc9e-125">The trigger name.</span></span>

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

### <span data-ttu-id="1cc9e-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1cc9e-126">-WorkspaceName</span></span>
<span data-ttu-id="1cc9e-127">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="1cc9e-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1cc9e-128">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="1cc9e-128">-WorkspaceObject</span></span>
<span data-ttu-id="1cc9e-129">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="1cc9e-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1cc9e-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1cc9e-130">-Confirm</span></span>
<span data-ttu-id="1cc9e-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1cc9e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cc9e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cc9e-132">-WhatIf</span></span>
<span data-ttu-id="1cc9e-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1cc9e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cc9e-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1cc9e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cc9e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cc9e-135">CommonParameters</span></span>
<span data-ttu-id="1cc9e-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cc9e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cc9e-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1cc9e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cc9e-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1cc9e-138">INPUTS</span></span>

### <span data-ttu-id="1cc9e-139">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1cc9e-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="1cc9e-140">Microsoft. Azure. Commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="1cc9e-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="1cc9e-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1cc9e-141">OUTPUTS</span></span>

### <span data-ttu-id="1cc9e-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="1cc9e-142">System.Object</span></span>
## <span data-ttu-id="1cc9e-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="1cc9e-143">NOTES</span></span>

## <span data-ttu-id="1cc9e-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1cc9e-144">RELATED LINKS</span></span>
