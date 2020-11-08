---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
ms.openlocfilehash: f28abbca41c68ce08e516fb52f69b7de8c54e67a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178132"
---
# <span data-ttu-id="4ed96-101">Remove-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="4ed96-101">Remove-AzSynapsePipeline</span></span>

## <span data-ttu-id="4ed96-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4ed96-102">SYNOPSIS</span></span>
<span data-ttu-id="4ed96-103">Entfernt eine Pipeline aus dem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="4ed96-103">Removes a pipeline from workspace.</span></span>

## <span data-ttu-id="4ed96-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ed96-104">SYNTAX</span></span>

### <span data-ttu-id="4ed96-105">RemoveByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="4ed96-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapsePipeline -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ed96-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="4ed96-106">RemoveByObject</span></span>
```
Remove-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ed96-107">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="4ed96-107">NewByInputObject</span></span>
```
Remove-AzSynapsePipeline -Name <String> -InputObject <PSPipelineResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ed96-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4ed96-108">DESCRIPTION</span></span>
<span data-ttu-id="4ed96-109">Das Cmdlet " **Remove-AzSynapsePipeline** " entfernt eine Pipeline aus dem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="4ed96-109">The **Remove-AzSynapsePipeline** cmdlet removes a pipeline from workspace.</span></span>

## <span data-ttu-id="4ed96-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4ed96-110">EXAMPLES</span></span>

### <span data-ttu-id="4ed96-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4ed96-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="4ed96-112">Dieses Cmdlet entfernt die Pipeline mit dem Namen ContosoPipeline aus dem Arbeitsbereich mit dem Namen ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="4ed96-112">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="4ed96-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4ed96-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="4ed96-114">Dieses Cmdlet entfernt die Pipeline mit dem Namen ContosoPipeline aus dem Arbeitsbereich mit dem Namen ContosoWorkspace through Pipeline.</span><span class="sxs-lookup"><span data-stu-id="4ed96-114">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="4ed96-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="4ed96-115">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Remove-AzSynapsePipeline
```

<span data-ttu-id="4ed96-116">Dieses Cmdlet entfernt die Pipeline mit dem Namen ContosoPipeline aus dem Arbeitsbereich mit dem Namen ContosoWorkspace through Pipeline.</span><span class="sxs-lookup"><span data-stu-id="4ed96-116">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="4ed96-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ed96-117">PARAMETERS</span></span>

### <span data-ttu-id="4ed96-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ed96-118">-AsJob</span></span>
<span data-ttu-id="4ed96-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4ed96-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4ed96-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ed96-120">-DefaultProfile</span></span>
<span data-ttu-id="4ed96-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4ed96-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ed96-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4ed96-122">-InputObject</span></span>
<span data-ttu-id="4ed96-123">Das Pipeline-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4ed96-123">The pipeline object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource
Parameter Sets: NewByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ed96-124">-Name</span><span class="sxs-lookup"><span data-stu-id="4ed96-124">-Name</span></span>
<span data-ttu-id="4ed96-125">Der Name der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="4ed96-125">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ed96-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ed96-126">-PassThru</span></span>
<span data-ttu-id="4ed96-127">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="4ed96-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="4ed96-128">Wenn dieser Schalter angegeben wird, wird true zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="4ed96-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="4ed96-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4ed96-129">-WorkspaceName</span></span>
<span data-ttu-id="4ed96-130">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="4ed96-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4ed96-131">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="4ed96-131">-WorkspaceObject</span></span>
<span data-ttu-id="4ed96-132">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="4ed96-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4ed96-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4ed96-133">-Confirm</span></span>
<span data-ttu-id="4ed96-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4ed96-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ed96-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ed96-135">-WhatIf</span></span>
<span data-ttu-id="4ed96-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4ed96-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ed96-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4ed96-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ed96-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ed96-138">CommonParameters</span></span>
<span data-ttu-id="4ed96-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ed96-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ed96-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ed96-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ed96-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4ed96-141">INPUTS</span></span>

### <span data-ttu-id="4ed96-142">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4ed96-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="4ed96-143">Microsoft. Azure. Commands. Synapse. Models. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="4ed96-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="4ed96-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4ed96-144">OUTPUTS</span></span>

### <span data-ttu-id="4ed96-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4ed96-145">System.Boolean</span></span>

## <span data-ttu-id="4ed96-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="4ed96-146">NOTES</span></span>

## <span data-ttu-id="4ed96-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4ed96-147">RELATED LINKS</span></span>
