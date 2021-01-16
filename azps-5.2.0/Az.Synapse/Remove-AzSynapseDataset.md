---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
ms.openlocfilehash: 68da67d2a29b6f05ed50adc9eb8aef343a7e973b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368960"
---
# <span data-ttu-id="c77cc-101">Remove-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="c77cc-101">Remove-AzSynapseDataset</span></span>

## <span data-ttu-id="c77cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c77cc-102">SYNOPSIS</span></span>
<span data-ttu-id="c77cc-103">Entfernt ein Dataset aus dem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="c77cc-103">Removes a dataset from workspace.</span></span>

## <span data-ttu-id="c77cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c77cc-104">SYNTAX</span></span>

### <span data-ttu-id="c77cc-105">RemoveByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c77cc-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataset -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c77cc-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="c77cc-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c77cc-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="c77cc-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataset -InputObject <PSDatasetResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c77cc-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c77cc-108">DESCRIPTION</span></span>
<span data-ttu-id="c77cc-109">Das **Cmdlet "Remove-AzSynapseDataset"** entfernt ein Dataset aus dem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="c77cc-109">The **Remove-AzSynapseDataset** cmdlet removes a dataset from workspace.</span></span>

## <span data-ttu-id="c77cc-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c77cc-110">EXAMPLES</span></span>

### <span data-ttu-id="c77cc-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c77cc-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="c77cc-112">Mit diesem Befehl wird das Dataset mit dem Namen "ContosoDataset" aus dem Arbeitsbereich "ContosoWorkspace" entfernt.</span><span class="sxs-lookup"><span data-stu-id="c77cc-112">This command removes the dataset named ContosoDataset from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="c77cc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c77cc-113">PARAMETERS</span></span>

### <span data-ttu-id="c77cc-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c77cc-114">-AsJob</span></span>
<span data-ttu-id="c77cc-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c77cc-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c77cc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c77cc-116">-DefaultProfile</span></span>
<span data-ttu-id="c77cc-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c77cc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c77cc-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c77cc-118">-Force</span></span>
<span data-ttu-id="c77cc-119">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="c77cc-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c77cc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c77cc-120">-InputObject</span></span>
<span data-ttu-id="c77cc-121">Das Datasetobjekt.</span><span class="sxs-lookup"><span data-stu-id="c77cc-121">The dataset object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c77cc-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c77cc-122">-Name</span></span>
<span data-ttu-id="c77cc-123">Der Datasetname.</span><span class="sxs-lookup"><span data-stu-id="c77cc-123">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: DatasetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c77cc-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c77cc-124">-PassThru</span></span>
<span data-ttu-id="c77cc-125">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="c77cc-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="c77cc-126">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="c77cc-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="c77cc-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c77cc-127">-WorkspaceName</span></span>
<span data-ttu-id="c77cc-128">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="c77cc-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c77cc-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c77cc-129">-WorkspaceObject</span></span>
<span data-ttu-id="c77cc-130">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="c77cc-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c77cc-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c77cc-131">-Confirm</span></span>
<span data-ttu-id="c77cc-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c77cc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c77cc-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c77cc-133">-WhatIf</span></span>
<span data-ttu-id="c77cc-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c77cc-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c77cc-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c77cc-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c77cc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c77cc-136">CommonParameters</span></span>
<span data-ttu-id="c77cc-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c77cc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c77cc-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c77cc-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c77cc-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c77cc-139">INPUTS</span></span>

### <span data-ttu-id="c77cc-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c77cc-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="c77cc-141">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="c77cc-141">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="c77cc-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c77cc-142">OUTPUTS</span></span>

### <span data-ttu-id="c77cc-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c77cc-143">System.Boolean</span></span>

## <span data-ttu-id="c77cc-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c77cc-144">NOTES</span></span>

## <span data-ttu-id="c77cc-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c77cc-145">RELATED LINKS</span></span>
