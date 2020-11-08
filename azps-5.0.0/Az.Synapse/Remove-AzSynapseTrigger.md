---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTrigger.md
ms.openlocfilehash: 0882789e230c012fe9f23dcdbeeb5378e9b91781
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177341"
---
# <span data-ttu-id="20df0-101">Remove-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="20df0-101">Remove-AzSynapseTrigger</span></span>

## <span data-ttu-id="20df0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="20df0-102">SYNOPSIS</span></span>
<span data-ttu-id="20df0-103">Entfernt einen Trigger aus einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="20df0-103">Removes a trigger from a workspace.</span></span>

## <span data-ttu-id="20df0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="20df0-104">SYNTAX</span></span>

### <span data-ttu-id="20df0-105">RemoveByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="20df0-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20df0-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="20df0-106">RemoveByObject</span></span>
```
Remove-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20df0-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="20df0-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20df0-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20df0-108">DESCRIPTION</span></span>
<span data-ttu-id="20df0-109">Mit dem Cmdlet **Remove-AzSynapseTrigger** wird ein Trigger aus einem Arbeitsbereich entfernt.</span><span class="sxs-lookup"><span data-stu-id="20df0-109">The **Remove-AzSynapseTrigger** cmdlet removes a trigger from a workspace.</span></span>

## <span data-ttu-id="20df0-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="20df0-110">EXAMPLES</span></span>

### <span data-ttu-id="20df0-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="20df0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="20df0-112">Entfernen Sie einen Trigger namens ContosoTrigger aus dem Arbeitsbereich ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="20df0-112">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="20df0-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="20df0-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="20df0-114">Entfernen Sie einen Trigger namens ContosoTrigger aus dem Arbeitsbereich ContosoWorkspace durch Pipeline.</span><span class="sxs-lookup"><span data-stu-id="20df0-114">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="20df0-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="20df0-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTrigger
```

<span data-ttu-id="20df0-116">Entfernen Sie einen Trigger namens ContosoTrigger aus dem Arbeitsbereich ContosoWorkspace durch Pipeline.</span><span class="sxs-lookup"><span data-stu-id="20df0-116">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="20df0-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="20df0-117">PARAMETERS</span></span>

### <span data-ttu-id="20df0-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20df0-118">-AsJob</span></span>
<span data-ttu-id="20df0-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="20df0-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="20df0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20df0-120">-DefaultProfile</span></span>
<span data-ttu-id="20df0-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="20df0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20df0-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="20df0-122">-InputObject</span></span>
<span data-ttu-id="20df0-123">Das Trigger-Objekt.</span><span class="sxs-lookup"><span data-stu-id="20df0-123">The trigger object.</span></span>

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

### <span data-ttu-id="20df0-124">-Name</span><span class="sxs-lookup"><span data-stu-id="20df0-124">-Name</span></span>
<span data-ttu-id="20df0-125">Der Name des Triggers.</span><span class="sxs-lookup"><span data-stu-id="20df0-125">The trigger name.</span></span>

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

### <span data-ttu-id="20df0-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20df0-126">-PassThru</span></span>
<span data-ttu-id="20df0-127">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="20df0-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="20df0-128">Wenn dieser Schalter angegeben wird, wird true zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="20df0-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="20df0-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="20df0-129">-WorkspaceName</span></span>
<span data-ttu-id="20df0-130">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="20df0-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="20df0-131">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="20df0-131">-WorkspaceObject</span></span>
<span data-ttu-id="20df0-132">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="20df0-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="20df0-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="20df0-133">-Confirm</span></span>
<span data-ttu-id="20df0-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="20df0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20df0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20df0-135">-WhatIf</span></span>
<span data-ttu-id="20df0-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="20df0-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20df0-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="20df0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20df0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20df0-138">CommonParameters</span></span>
<span data-ttu-id="20df0-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20df0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20df0-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20df0-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20df0-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="20df0-141">INPUTS</span></span>

### <span data-ttu-id="20df0-142">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="20df0-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="20df0-143">Microsoft. Azure. Commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="20df0-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="20df0-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="20df0-144">OUTPUTS</span></span>

### <span data-ttu-id="20df0-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="20df0-145">System.Boolean</span></span>

## <span data-ttu-id="20df0-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="20df0-146">NOTES</span></span>

## <span data-ttu-id="20df0-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="20df0-147">RELATED LINKS</span></span>
