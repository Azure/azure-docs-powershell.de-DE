---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
ms.openlocfilehash: 289e601ab80e4842b493cd6852839bec544bcc36
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302874"
---
# <span data-ttu-id="5f25f-101">Set-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="5f25f-101">Set-AzSynapseTrigger</span></span>

## <span data-ttu-id="5f25f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5f25f-102">SYNOPSIS</span></span>
<span data-ttu-id="5f25f-103">Erstellt einen Trigger in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="5f25f-103">Creates a trigger in a workspace.</span></span>

## <span data-ttu-id="5f25f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f25f-104">SYNTAX</span></span>

### <span data-ttu-id="5f25f-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="5f25f-105">SetByName (Default)</span></span>
```
Set-AzSynapseTrigger -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f25f-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="5f25f-106">SetByObject</span></span>
```
Set-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f25f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f25f-107">DESCRIPTION</span></span>
<span data-ttu-id="5f25f-108">Das Cmdlet " **Satz-AzSynapseTrigger** " erstellt einen Trigger in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="5f25f-108">The **Set-AzSynapseTrigger** cmdlet creates a trigger in a workspace.</span></span> <span data-ttu-id="5f25f-109">Trigger werden im Zustand "stopped" erstellt, was bedeutet, dass Sie nicht sofort mit dem Aufruf von Pipelines beginnen, auf die Sie verweisen.</span><span class="sxs-lookup"><span data-stu-id="5f25f-109">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="5f25f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5f25f-110">EXAMPLES</span></span>

### <span data-ttu-id="5f25f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5f25f-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="5f25f-112">Erstellen Sie einen neuen Trigger namens ContosoTrigger im Arbeitsbereich ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="5f25f-112">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span> <span data-ttu-id="5f25f-113">Der Trigger wird im Zustand "stopped" erstellt, was bedeutet, dass er nicht sofort gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="5f25f-113">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="5f25f-114">Ein Trigger kann mit dem Cmdlet gestartet werden `Start-AzDataFactoryV2Trigger` .</span><span class="sxs-lookup"><span data-stu-id="5f25f-114">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

### <span data-ttu-id="5f25f-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5f25f-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseTrigger -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="5f25f-116">Erstellen Sie einen neuen Trigger namens ContosoTrigger im Arbeitsbereich ContosoWorkspace through-Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5f25f-116">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span> <span data-ttu-id="5f25f-117">Der Trigger wird im Zustand "stopped" erstellt, was bedeutet, dass er nicht sofort gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="5f25f-117">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="5f25f-118">Ein Trigger kann mit dem Cmdlet gestartet werden `Start-AzDataFactoryV2Trigger` .</span><span class="sxs-lookup"><span data-stu-id="5f25f-118">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="5f25f-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f25f-119">PARAMETERS</span></span>

### <span data-ttu-id="5f25f-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5f25f-120">-AsJob</span></span>
<span data-ttu-id="5f25f-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5f25f-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5f25f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f25f-122">-DefaultProfile</span></span>
<span data-ttu-id="5f25f-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5f25f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f25f-124">-Definitions-Nr.</span><span class="sxs-lookup"><span data-stu-id="5f25f-124">-DefinitionFile</span></span>
<span data-ttu-id="5f25f-125">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="5f25f-125">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f25f-126">-Name</span><span class="sxs-lookup"><span data-stu-id="5f25f-126">-Name</span></span>
<span data-ttu-id="5f25f-127">Der Name des Triggers.</span><span class="sxs-lookup"><span data-stu-id="5f25f-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f25f-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5f25f-128">-WorkspaceName</span></span>
<span data-ttu-id="5f25f-129">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="5f25f-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f25f-130">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="5f25f-130">-WorkspaceObject</span></span>
<span data-ttu-id="5f25f-131">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="5f25f-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f25f-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5f25f-132">-Confirm</span></span>
<span data-ttu-id="5f25f-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5f25f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f25f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f25f-134">-WhatIf</span></span>
<span data-ttu-id="5f25f-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f25f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f25f-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5f25f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f25f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f25f-137">CommonParameters</span></span>
<span data-ttu-id="5f25f-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f25f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f25f-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f25f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f25f-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5f25f-140">INPUTS</span></span>

### <span data-ttu-id="5f25f-141">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5f25f-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="5f25f-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5f25f-142">OUTPUTS</span></span>

### <span data-ttu-id="5f25f-143">Microsoft. Azure. Commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="5f25f-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="5f25f-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="5f25f-144">NOTES</span></span>

## <span data-ttu-id="5f25f-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5f25f-145">RELATED LINKS</span></span>
