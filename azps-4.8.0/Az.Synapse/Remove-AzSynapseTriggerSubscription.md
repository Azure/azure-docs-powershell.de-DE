---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
ms.openlocfilehash: 69e7c17d28c94ce00f054a0e5b71eadc4d8ade76
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167191"
---
# <span data-ttu-id="0d150-101">Remove-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="0d150-101">Remove-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="0d150-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0d150-102">SYNOPSIS</span></span>
<span data-ttu-id="0d150-103">Kündigen Sie den Ereignisauslöser für externe Dienstereignisse.</span><span class="sxs-lookup"><span data-stu-id="0d150-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="0d150-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d150-104">SYNTAX</span></span>

### <span data-ttu-id="0d150-105">RemoveByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="0d150-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d150-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="0d150-106">RemoveByObject</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d150-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="0d150-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d150-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d150-108">DESCRIPTION</span></span>
<span data-ttu-id="0d150-109">Mit dem Cmdlet **Remove-AzSynapseTriggerSubscription** wird der Event-Trigger für die angegebenen externen Dienstereignisse vom Trigger-Definition abgemeldet.</span><span class="sxs-lookup"><span data-stu-id="0d150-109">The **Remove-AzSynapseTriggerSubscription** cmdlet unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="0d150-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d150-110">EXAMPLES</span></span>

### <span data-ttu-id="0d150-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0d150-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="0d150-112">Mit diesem Befehl wird der Subscribe-Trigger "ContosoTrigger" zu den angegebenen Ereignissen aus dem Trigger-Definition abgemeldet.</span><span class="sxs-lookup"><span data-stu-id="0d150-112">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="0d150-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0d150-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="0d150-114">Mit diesem Befehl wird der ContosoTrigger-Trigger für die angegebenen Ereignisse vom Trigger Definition through-Pipeline abgemeldet.</span><span class="sxs-lookup"><span data-stu-id="0d150-114">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="0d150-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="0d150-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTriggerSubscription
```

<span data-ttu-id="0d150-116">Mit diesem Befehl wird der ContosoTrigger-Trigger für die angegebenen Ereignisse vom Trigger Definition through-Pipeline abgemeldet.</span><span class="sxs-lookup"><span data-stu-id="0d150-116">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="0d150-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d150-117">PARAMETERS</span></span>

### <span data-ttu-id="0d150-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d150-118">-AsJob</span></span>
<span data-ttu-id="0d150-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0d150-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0d150-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d150-120">-DefaultProfile</span></span>
<span data-ttu-id="0d150-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0d150-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d150-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0d150-122">-InputObject</span></span>
<span data-ttu-id="0d150-123">Das Trigger-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0d150-123">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d150-124">-Name</span><span class="sxs-lookup"><span data-stu-id="0d150-124">-Name</span></span>
<span data-ttu-id="0d150-125">Der Name des Triggers.</span><span class="sxs-lookup"><span data-stu-id="0d150-125">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d150-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d150-126">-PassThru</span></span>
<span data-ttu-id="0d150-127">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="0d150-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="0d150-128">Wenn dieser Schalter angegeben wird, wird true zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="0d150-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="0d150-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0d150-129">-WorkspaceName</span></span>
<span data-ttu-id="0d150-130">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="0d150-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d150-131">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="0d150-131">-WorkspaceObject</span></span>
<span data-ttu-id="0d150-132">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="0d150-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d150-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0d150-133">-Confirm</span></span>
<span data-ttu-id="0d150-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0d150-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d150-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d150-135">-WhatIf</span></span>
<span data-ttu-id="0d150-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0d150-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d150-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0d150-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d150-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d150-138">CommonParameters</span></span>
<span data-ttu-id="0d150-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d150-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d150-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d150-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d150-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0d150-141">INPUTS</span></span>

### <span data-ttu-id="0d150-142">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0d150-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="0d150-143">Microsoft. Azure. Commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="0d150-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="0d150-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0d150-144">OUTPUTS</span></span>

### <span data-ttu-id="0d150-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0d150-145">System.Boolean</span></span>

## <span data-ttu-id="0d150-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="0d150-146">NOTES</span></span>

## <span data-ttu-id="0d150-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0d150-147">RELATED LINKS</span></span>
