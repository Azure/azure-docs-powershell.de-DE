---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTrigger.md
ms.openlocfilehash: 171cb897d1e385056d391468cf31f3b361c39202
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922595"
---
# <span data-ttu-id="e3463-101">Remove-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="e3463-101">Remove-AzSynapseTrigger</span></span>

## <span data-ttu-id="e3463-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3463-102">SYNOPSIS</span></span>
<span data-ttu-id="e3463-103">Entfernt einen Trigger aus einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="e3463-103">Removes a trigger from a workspace.</span></span>

## <span data-ttu-id="e3463-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e3463-104">SYNTAX</span></span>

### <span data-ttu-id="e3463-105">RemoveByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="e3463-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3463-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="e3463-106">RemoveByObject</span></span>
```
Remove-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3463-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="e3463-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3463-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e3463-108">DESCRIPTION</span></span>
<span data-ttu-id="e3463-109">Das **Cmdlet Remove-AzSynapseTrigger** entfernt einen Trigger aus einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="e3463-109">The **Remove-AzSynapseTrigger** cmdlet removes a trigger from a workspace.</span></span>

## <span data-ttu-id="e3463-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e3463-110">EXAMPLES</span></span>

### <span data-ttu-id="e3463-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e3463-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="e3463-112">Entfernen Sie einen Trigger namens ContosoTrigger aus dem Arbeitsbereich ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="e3463-112">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="e3463-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e3463-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="e3463-114">Entfernen Sie einen Trigger namens ContosoTrigger aus dem Arbeitsbereich ContosoWorkspace über die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="e3463-114">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="e3463-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e3463-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTrigger
```

<span data-ttu-id="e3463-116">Entfernen Sie einen Trigger namens ContosoTrigger aus dem Arbeitsbereich ContosoWorkspace über die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="e3463-116">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="e3463-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e3463-117">PARAMETERS</span></span>

### <span data-ttu-id="e3463-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3463-118">-AsJob</span></span>
<span data-ttu-id="e3463-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e3463-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e3463-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3463-120">-DefaultProfile</span></span>
<span data-ttu-id="e3463-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e3463-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3463-122">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="e3463-122">-Force</span></span>
<span data-ttu-id="e3463-123">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="e3463-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e3463-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3463-124">-InputObject</span></span>
<span data-ttu-id="e3463-125">Das Triggerobjekt.</span><span class="sxs-lookup"><span data-stu-id="e3463-125">The trigger object.</span></span>

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

### <span data-ttu-id="e3463-126">-Name</span><span class="sxs-lookup"><span data-stu-id="e3463-126">-Name</span></span>
<span data-ttu-id="e3463-127">Der Triggername.</span><span class="sxs-lookup"><span data-stu-id="e3463-127">The trigger name.</span></span>

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

### <span data-ttu-id="e3463-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3463-128">-PassThru</span></span>
<span data-ttu-id="e3463-129">Dieses Cmdlet gibt standardmäßig kein -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="e3463-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e3463-130">Wenn dieser Schalter angegeben ist, gibt er "true" zurück, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="e3463-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="e3463-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e3463-131">-WorkspaceName</span></span>
<span data-ttu-id="e3463-132">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="e3463-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e3463-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e3463-133">-WorkspaceObject</span></span>
<span data-ttu-id="e3463-134">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="e3463-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e3463-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e3463-135">-Confirm</span></span>
<span data-ttu-id="e3463-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e3463-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3463-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3463-137">-WhatIf</span></span>
<span data-ttu-id="e3463-138">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e3463-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e3463-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e3463-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3463-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3463-140">CommonParameters</span></span>
<span data-ttu-id="e3463-141">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3463-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3463-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3463-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3463-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e3463-143">INPUTS</span></span>

### <span data-ttu-id="e3463-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e3463-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e3463-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="e3463-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="e3463-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e3463-146">OUTPUTS</span></span>

### <span data-ttu-id="e3463-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e3463-147">System.Boolean</span></span>

## <span data-ttu-id="e3463-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e3463-148">NOTES</span></span>

## <span data-ttu-id="e3463-149">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e3463-149">RELATED LINKS</span></span>
