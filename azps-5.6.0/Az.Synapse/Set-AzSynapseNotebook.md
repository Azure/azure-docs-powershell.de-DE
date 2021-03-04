---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
ms.openlocfilehash: 9b960c3b671ecada8f4f24e1b5a8897de7004440
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946378"
---
# <span data-ttu-id="941d7-101">Set-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="941d7-101">Set-AzSynapseNotebook</span></span>

## <span data-ttu-id="941d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="941d7-102">SYNOPSIS</span></span>
<span data-ttu-id="941d7-103">Erstellt oder aktualisiert ein Notizbuch in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="941d7-103">Creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="941d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="941d7-104">SYNTAX</span></span>

### <span data-ttu-id="941d7-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="941d7-105">SetByName (Default)</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="941d7-106">SetByNameAndSparkPool</span><span class="sxs-lookup"><span data-stu-id="941d7-106">SetByNameAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -SparkPoolName <String> [-ExecutorSize <String>]
 -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="941d7-107">SetByObject</span><span class="sxs-lookup"><span data-stu-id="941d7-107">SetByObject</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="941d7-108">SetByObjectAndSparkPool</span><span class="sxs-lookup"><span data-stu-id="941d7-108">SetByObjectAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -SparkPoolName <String>
 [-ExecutorSize <String>] -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="941d7-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="941d7-109">DESCRIPTION</span></span>
<span data-ttu-id="941d7-110">Das **Cmdlet Set-AzSynapseNotebook** erstellt oder aktualisiert ein Notizbuch in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="941d7-110">The **Set-AzSynapseNotebook** cmdlet creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="941d7-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="941d7-111">EXAMPLES</span></span>

### <span data-ttu-id="941d7-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="941d7-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb"

    WorkspaceName : ContosoWorkspace
    Properties    : Microsoft.Azure.Commands.Synapse.Models.PSNotebook
    Name          : notebook
```

<span data-ttu-id="941d7-113">Mit diesem Befehl wird ein Notizbuch aus notizbuchdatei"notebook.ipynb" im Arbeitsbereich "ContosoWorkspace" erstellt oder aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="941d7-113">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="941d7-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="941d7-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseNotebook -DefinitionFile "C:\\samples\\notebook.ipynb"
```

<span data-ttu-id="941d7-115">Mit diesem Befehl wird ein Notizbuch aus notizbuchdatei notebook.ipynb im Arbeitsbereich namens ContosoWorkspace über die Pipeline erstellt oder aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="941d7-115">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="941d7-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="941d7-116">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb" -SparkPoolName ContosoSparkPool -ExecutorCount 2
```

<span data-ttu-id="941d7-117">Mit diesem Befehl wird ein Notizbuch aus notizbuchdatei notebook.ipynb erstellt oder aktualisiert, das an ContosoSparkPool anfügen und zwei Executoren im Arbeitsbereich namens ContosoWorkspace verwendet.</span><span class="sxs-lookup"><span data-stu-id="941d7-117">This command creates or updates a notebook from notebook file notebook.ipynb which attaches to ContosoSparkPool and uses 2 executors in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="941d7-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="941d7-118">PARAMETERS</span></span>

### <span data-ttu-id="941d7-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="941d7-119">-AsJob</span></span>
<span data-ttu-id="941d7-120">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="941d7-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="941d7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="941d7-121">-DefaultProfile</span></span>
<span data-ttu-id="941d7-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="941d7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="941d7-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="941d7-123">-DefinitionFile</span></span>
<span data-ttu-id="941d7-124">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="941d7-124">The JSON file path.</span></span>

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

### <span data-ttu-id="941d7-125">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="941d7-125">-ExecutorCount</span></span>
<span data-ttu-id="941d7-126">Die Anzahl der executors, die im angegebenen Spark-Pool für den Auftrag zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="941d7-126">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByNameAndSparkPool, SetByObjectAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="941d7-127">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="941d7-127">-ExecutorSize</span></span>
<span data-ttu-id="941d7-128">Anzahl des Kerns und des Arbeitsspeichers, der für Executoren verwendet werden soll, die im angegebenen Spark-Pool für den Auftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="941d7-128">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndSparkPool, SetByObjectAndSparkPool
Aliases:
Accepted values: Small, Medium, Large

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="941d7-129">-Name</span><span class="sxs-lookup"><span data-stu-id="941d7-129">-Name</span></span>
<span data-ttu-id="941d7-130">Der Name des Notizbuchs.</span><span class="sxs-lookup"><span data-stu-id="941d7-130">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NotebookName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="941d7-131">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="941d7-131">-SparkPoolName</span></span>
<span data-ttu-id="941d7-132">Name des Synapse Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="941d7-132">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndSparkPool, SetByObjectAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="941d7-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="941d7-133">-WorkspaceName</span></span>
<span data-ttu-id="941d7-134">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="941d7-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="941d7-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="941d7-135">-WorkspaceObject</span></span>
<span data-ttu-id="941d7-136">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="941d7-136">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject, SetByObjectAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="941d7-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="941d7-137">-Confirm</span></span>
<span data-ttu-id="941d7-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="941d7-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="941d7-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="941d7-139">-WhatIf</span></span>
<span data-ttu-id="941d7-140">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="941d7-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="941d7-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="941d7-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="941d7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="941d7-142">CommonParameters</span></span>
<span data-ttu-id="941d7-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="941d7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="941d7-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="941d7-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="941d7-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="941d7-145">INPUTS</span></span>

### <span data-ttu-id="941d7-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="941d7-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="941d7-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="941d7-147">OUTPUTS</span></span>

### <span data-ttu-id="941d7-148">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="941d7-148">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="941d7-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="941d7-149">NOTES</span></span>

## <span data-ttu-id="941d7-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="941d7-150">RELATED LINKS</span></span>
