---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
ms.openlocfilehash: da4907200bef198afa1d57b51069c6379d28c8f1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297034"
---
# <span data-ttu-id="4a555-101">Set-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="4a555-101">Set-AzSynapseNotebook</span></span>

## <span data-ttu-id="4a555-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a555-102">SYNOPSIS</span></span>
<span data-ttu-id="4a555-103">Erstellt oder aktualisiert ein Notizbuch in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="4a555-103">Creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="4a555-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a555-104">SYNTAX</span></span>

### <span data-ttu-id="4a555-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="4a555-105">SetByName (Default)</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a555-106">SetByNameAndSparkPool</span><span class="sxs-lookup"><span data-stu-id="4a555-106">SetByNameAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -SparkPoolName <String> [-ExecutorSize <String>]
 -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a555-107">SetByObject</span><span class="sxs-lookup"><span data-stu-id="4a555-107">SetByObject</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a555-108">SetByObjectAndSparkPool</span><span class="sxs-lookup"><span data-stu-id="4a555-108">SetByObjectAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -SparkPoolName <String>
 [-ExecutorSize <String>] -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a555-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a555-109">DESCRIPTION</span></span>
<span data-ttu-id="4a555-110">Das **Cmdlet "Set-AzSynapseNotebook"** erstellt oder aktualisiert ein Notizbuch in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="4a555-110">The **Set-AzSynapseNotebook** cmdlet creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="4a555-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4a555-111">EXAMPLES</span></span>

### <span data-ttu-id="4a555-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4a555-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb"

    WorkspaceName : ContosoWorkspace
    Properties    : Microsoft.Azure.Commands.Synapse.Models.PSNotebook
    Name          : notebook
```

<span data-ttu-id="4a555-113">Mit diesem Befehl wird ein Notizbuch aus der Datei "notebook.ipynb" im Arbeitsbereich "ContosoWorkspace" erstellt oder aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="4a555-113">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="4a555-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4a555-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseNotebook -DefinitionFile "C:\\samples\\notebook.ipynb"
```

<span data-ttu-id="4a555-115">Mit diesem Befehl wird ein Notizbuch aus der Datei "notebook.ipynb" im Arbeitsbereich "ContosoWorkspace" über die Pipeline erstellt oder aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="4a555-115">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="4a555-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="4a555-116">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb" -SparkPoolName ContosoSparkPool -ExecutorCount 2
```

<span data-ttu-id="4a555-117">Mit diesem Befehl wird ein Notizbuch aus der Datei "notebook.ipynb" erstellt oder aktualisiert, das an "ContosoSparkPool" anfügen und zwei Ausführungsgeber im Arbeitsbereich "ContosoWorkspace" verwendet.</span><span class="sxs-lookup"><span data-stu-id="4a555-117">This command creates or updates a notebook from notebook file notebook.ipynb which attaches to ContosoSparkPool and uses 2 executors in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="4a555-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a555-118">PARAMETERS</span></span>

### <span data-ttu-id="4a555-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a555-119">-AsJob</span></span>
<span data-ttu-id="4a555-120">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4a555-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4a555-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a555-121">-DefaultProfile</span></span>
<span data-ttu-id="4a555-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a555-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a555-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="4a555-123">-DefinitionFile</span></span>
<span data-ttu-id="4a555-124">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="4a555-124">The JSON file path.</span></span>

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

### <span data-ttu-id="4a555-125">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="4a555-125">-ExecutorCount</span></span>
<span data-ttu-id="4a555-126">Die Anzahl der Ausführungsgeber, die im angegebenen Sparkpool für den Auftrag zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4a555-126">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="4a555-127">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="4a555-127">-ExecutorSize</span></span>
<span data-ttu-id="4a555-128">Die Anzahl des Kerns und des Arbeitsspeichers, der für die Ausführungsgeber verwendet werden soll, die im angegebenen Sparkpool für den Auftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="4a555-128">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="4a555-129">-Name</span><span class="sxs-lookup"><span data-stu-id="4a555-129">-Name</span></span>
<span data-ttu-id="4a555-130">Der Notizbuchname.</span><span class="sxs-lookup"><span data-stu-id="4a555-130">The notebook name.</span></span>

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

### <span data-ttu-id="4a555-131">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="4a555-131">-SparkPoolName</span></span>
<span data-ttu-id="4a555-132">Name des Synapse Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="4a555-132">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="4a555-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4a555-133">-WorkspaceName</span></span>
<span data-ttu-id="4a555-134">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="4a555-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4a555-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4a555-135">-WorkspaceObject</span></span>
<span data-ttu-id="4a555-136">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="4a555-136">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4a555-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a555-137">-Confirm</span></span>
<span data-ttu-id="4a555-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4a555-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a555-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4a555-139">-WhatIf</span></span>
<span data-ttu-id="4a555-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4a555-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a555-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4a555-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a555-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a555-142">CommonParameters</span></span>
<span data-ttu-id="4a555-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a555-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a555-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a555-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a555-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4a555-145">INPUTS</span></span>

### <span data-ttu-id="4a555-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4a555-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="4a555-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4a555-147">OUTPUTS</span></span>

### <span data-ttu-id="4a555-148">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="4a555-148">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="4a555-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4a555-149">NOTES</span></span>

## <span data-ttu-id="4a555-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4a555-150">RELATED LINKS</span></span>
