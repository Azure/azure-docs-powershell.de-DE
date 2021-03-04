---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
ms.openlocfilehash: b70c30b7652c331571030917057339a9d2d7de3e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924344"
---
# <span data-ttu-id="040db-101">Remove-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="040db-101">Remove-AzSynapseDataset</span></span>

## <span data-ttu-id="040db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="040db-102">SYNOPSIS</span></span>
<span data-ttu-id="040db-103">Entfernt ein Dataset aus dem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="040db-103">Removes a dataset from workspace.</span></span>

## <span data-ttu-id="040db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="040db-104">SYNTAX</span></span>

### <span data-ttu-id="040db-105">RemoveByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="040db-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataset -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="040db-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="040db-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="040db-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="040db-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataset -InputObject <PSDatasetResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="040db-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="040db-108">DESCRIPTION</span></span>
<span data-ttu-id="040db-109">Das **Cmdlet Remove-AzSynapseDataset** entfernt ein Dataset aus dem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="040db-109">The **Remove-AzSynapseDataset** cmdlet removes a dataset from workspace.</span></span>

## <span data-ttu-id="040db-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="040db-110">EXAMPLES</span></span>

### <span data-ttu-id="040db-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="040db-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="040db-112">Mit diesem Befehl wird das Dataset mit dem Namen ContosoDataset aus dem Arbeitsbereich namens ContosoWorkspace entfernt.</span><span class="sxs-lookup"><span data-stu-id="040db-112">This command removes the dataset named ContosoDataset from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="040db-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="040db-113">PARAMETERS</span></span>

### <span data-ttu-id="040db-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="040db-114">-AsJob</span></span>
<span data-ttu-id="040db-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="040db-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="040db-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="040db-116">-DefaultProfile</span></span>
<span data-ttu-id="040db-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="040db-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="040db-118">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="040db-118">-Force</span></span>
<span data-ttu-id="040db-119">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="040db-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="040db-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="040db-120">-InputObject</span></span>
<span data-ttu-id="040db-121">Das Datasetobjekt.</span><span class="sxs-lookup"><span data-stu-id="040db-121">The dataset object.</span></span>

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

### <span data-ttu-id="040db-122">-Name</span><span class="sxs-lookup"><span data-stu-id="040db-122">-Name</span></span>
<span data-ttu-id="040db-123">Der Name des Datasets.</span><span class="sxs-lookup"><span data-stu-id="040db-123">The dataset name.</span></span>

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

### <span data-ttu-id="040db-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="040db-124">-PassThru</span></span>
<span data-ttu-id="040db-125">Dieses Cmdlet gibt standardmäßig kein -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="040db-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="040db-126">Wenn dieser Schalter angegeben ist, gibt er "true" zurück, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="040db-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="040db-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="040db-127">-WorkspaceName</span></span>
<span data-ttu-id="040db-128">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="040db-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="040db-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="040db-129">-WorkspaceObject</span></span>
<span data-ttu-id="040db-130">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="040db-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="040db-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="040db-131">-Confirm</span></span>
<span data-ttu-id="040db-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="040db-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="040db-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="040db-133">-WhatIf</span></span>
<span data-ttu-id="040db-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="040db-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="040db-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="040db-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="040db-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="040db-136">CommonParameters</span></span>
<span data-ttu-id="040db-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="040db-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="040db-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="040db-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="040db-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="040db-139">INPUTS</span></span>

### <span data-ttu-id="040db-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="040db-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="040db-141">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="040db-141">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="040db-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="040db-142">OUTPUTS</span></span>

### <span data-ttu-id="040db-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="040db-143">System.Boolean</span></span>

## <span data-ttu-id="040db-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="040db-144">NOTES</span></span>

## <span data-ttu-id="040db-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="040db-145">RELATED LINKS</span></span>
