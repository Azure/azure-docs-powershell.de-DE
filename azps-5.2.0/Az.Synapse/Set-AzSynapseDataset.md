---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
ms.openlocfilehash: d2471320a27b1af96dba6b5e2b552a01ff5b50e3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98301600"
---
# <span data-ttu-id="b8b00-101">Set-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="b8b00-101">Set-AzSynapseDataset</span></span>

## <span data-ttu-id="b8b00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8b00-102">SYNOPSIS</span></span>
<span data-ttu-id="b8b00-103">Erstellt oder aktualisiert ein Dataset im Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="b8b00-103">Creates or updates a dataset in workspace.</span></span>

## <span data-ttu-id="b8b00-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8b00-104">SYNTAX</span></span>

### <span data-ttu-id="b8b00-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b8b00-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataset -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8b00-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="b8b00-106">SetByObject</span></span>
```
Set-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8b00-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b8b00-107">DESCRIPTION</span></span>
<span data-ttu-id="b8b00-108">Das **Cmdlet "Set-AzSynapseDataset"** erstellt ein Dataset oder aktualisiert ein vorhandenes Dataset im Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="b8b00-108">The **Set-AzSynapseDataset** cmdlet creates a dataset or updates an existing dataset in workspace.</span></span>

## <span data-ttu-id="b8b00-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b8b00-109">EXAMPLES</span></span>

### <span data-ttu-id="b8b00-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b8b00-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset -DefinitionFile "C:\\samples\\Dataset.json"
```

<span data-ttu-id="b8b00-111">Mit diesem Befehl wird ein Dataset namens "ContosoDataset" im Arbeitsbereich "ContosoWorkspace" erstellt.</span><span class="sxs-lookup"><span data-stu-id="b8b00-111">This command creates a dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="b8b00-112">Der Befehl basiert auf Informationen im Dataset, Dataset.jsdateibasiert sind.</span><span class="sxs-lookup"><span data-stu-id="b8b00-112">The command bases the dataset on information in the Dataset.json file.</span></span>

## <span data-ttu-id="b8b00-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8b00-113">PARAMETERS</span></span>

### <span data-ttu-id="b8b00-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8b00-114">-AsJob</span></span>
<span data-ttu-id="b8b00-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b8b00-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b8b00-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8b00-116">-DefaultProfile</span></span>
<span data-ttu-id="b8b00-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8b00-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8b00-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="b8b00-118">-DefinitionFile</span></span>
<span data-ttu-id="b8b00-119">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="b8b00-119">The JSON file path.</span></span>

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

### <span data-ttu-id="b8b00-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b8b00-120">-Name</span></span>
<span data-ttu-id="b8b00-121">Der Datasetname.</span><span class="sxs-lookup"><span data-stu-id="b8b00-121">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b00-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b8b00-122">-WorkspaceName</span></span>
<span data-ttu-id="b8b00-123">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="b8b00-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b8b00-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b8b00-124">-WorkspaceObject</span></span>
<span data-ttu-id="b8b00-125">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="b8b00-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b8b00-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8b00-126">-Confirm</span></span>
<span data-ttu-id="b8b00-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b8b00-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8b00-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b8b00-128">-WhatIf</span></span>
<span data-ttu-id="b8b00-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b8b00-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8b00-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b8b00-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8b00-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8b00-131">CommonParameters</span></span>
<span data-ttu-id="b8b00-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8b00-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8b00-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8b00-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8b00-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b8b00-134">INPUTS</span></span>

### <span data-ttu-id="b8b00-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b8b00-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b8b00-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b8b00-136">OUTPUTS</span></span>

### <span data-ttu-id="b8b00-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="b8b00-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="b8b00-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b8b00-138">NOTES</span></span>

## <span data-ttu-id="b8b00-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b8b00-139">RELATED LINKS</span></span>
