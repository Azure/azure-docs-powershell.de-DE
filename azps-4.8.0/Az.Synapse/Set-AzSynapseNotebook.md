---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
ms.openlocfilehash: da4907200bef198afa1d57b51069c6379d28c8f1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173360"
---
# <span data-ttu-id="212bd-101">Set-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="212bd-101">Set-AzSynapseNotebook</span></span>

## <span data-ttu-id="212bd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="212bd-102">SYNOPSIS</span></span>
<span data-ttu-id="212bd-103">Erstellt oder aktualisiert ein Notizbuch in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="212bd-103">Creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="212bd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="212bd-104">SYNTAX</span></span>

### <span data-ttu-id="212bd-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="212bd-105">SetByName (Default)</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="212bd-106">SetByNameAndSparkPool</span><span class="sxs-lookup"><span data-stu-id="212bd-106">SetByNameAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -SparkPoolName <String> [-ExecutorSize <String>]
 -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="212bd-107">SetByObject</span><span class="sxs-lookup"><span data-stu-id="212bd-107">SetByObject</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="212bd-108">SetByObjectAndSparkPool</span><span class="sxs-lookup"><span data-stu-id="212bd-108">SetByObjectAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -SparkPoolName <String>
 [-ExecutorSize <String>] -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="212bd-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="212bd-109">DESCRIPTION</span></span>
<span data-ttu-id="212bd-110">Das Cmdlet " **Satz-AzSynapseNotebook** " erstellt oder aktualisiert ein Notizbuch in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="212bd-110">The **Set-AzSynapseNotebook** cmdlet creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="212bd-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="212bd-111">EXAMPLES</span></span>

### <span data-ttu-id="212bd-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="212bd-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb"

    WorkspaceName : ContosoWorkspace
    Properties    : Microsoft.Azure.Commands.Synapse.Models.PSNotebook
    Name          : notebook
```

<span data-ttu-id="212bd-113">Dieser Befehl erstellt oder aktualisiert ein Notizbuch aus Notizbuch-Datei Notizbuch. ipynb im Arbeitsbereich mit dem Namen ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="212bd-113">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="212bd-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="212bd-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseNotebook -DefinitionFile "C:\\samples\\notebook.ipynb"
```

<span data-ttu-id="212bd-115">Dieser Befehl erstellt oder aktualisiert ein Notizbuch aus Notizbuch-Datei Notizbuch. ipynb im Arbeitsbereich mit dem Namen ContosoWorkspace through Pipeline.</span><span class="sxs-lookup"><span data-stu-id="212bd-115">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="212bd-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="212bd-116">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb" -SparkPoolName ContosoSparkPool -ExecutorCount 2
```

<span data-ttu-id="212bd-117">Dieser Befehl erstellt oder aktualisiert ein Notizbuch aus Notizbuch-Datei Notizbuch. ipynb, das an ContosoSparkPool angefügt wird und 2 Executors im Arbeitsbereich mit dem Namen ContosoWorkspace verwendet.</span><span class="sxs-lookup"><span data-stu-id="212bd-117">This command creates or updates a notebook from notebook file notebook.ipynb which attaches to ContosoSparkPool and uses 2 executors in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="212bd-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="212bd-118">PARAMETERS</span></span>

### <span data-ttu-id="212bd-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="212bd-119">-AsJob</span></span>
<span data-ttu-id="212bd-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="212bd-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="212bd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="212bd-121">-DefaultProfile</span></span>
<span data-ttu-id="212bd-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="212bd-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="212bd-123">-Definitions-Nr.</span><span class="sxs-lookup"><span data-stu-id="212bd-123">-DefinitionFile</span></span>
<span data-ttu-id="212bd-124">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="212bd-124">The JSON file path.</span></span>

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

### <span data-ttu-id="212bd-125">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="212bd-125">-ExecutorCount</span></span>
<span data-ttu-id="212bd-126">Die Anzahl der Executors, die im angegebenen Spark-Pool für den Auftrag zugewiesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="212bd-126">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="212bd-127">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="212bd-127">-ExecutorSize</span></span>
<span data-ttu-id="212bd-128">Die Anzahl des Kerns und des Arbeitsspeichers, der für Executors verwendet werden soll, die im angegebenen Spark Pool für den Auftrag reserviert sind.</span><span class="sxs-lookup"><span data-stu-id="212bd-128">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="212bd-129">-Name</span><span class="sxs-lookup"><span data-stu-id="212bd-129">-Name</span></span>
<span data-ttu-id="212bd-130">Der Name des Notizbuchs.</span><span class="sxs-lookup"><span data-stu-id="212bd-130">The notebook name.</span></span>

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

### <span data-ttu-id="212bd-131">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="212bd-131">-SparkPoolName</span></span>
<span data-ttu-id="212bd-132">Name des Synapsen-Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="212bd-132">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="212bd-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="212bd-133">-WorkspaceName</span></span>
<span data-ttu-id="212bd-134">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="212bd-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="212bd-135">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="212bd-135">-WorkspaceObject</span></span>
<span data-ttu-id="212bd-136">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="212bd-136">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="212bd-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="212bd-137">-Confirm</span></span>
<span data-ttu-id="212bd-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="212bd-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="212bd-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="212bd-139">-WhatIf</span></span>
<span data-ttu-id="212bd-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="212bd-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="212bd-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="212bd-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="212bd-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="212bd-142">CommonParameters</span></span>
<span data-ttu-id="212bd-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="212bd-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="212bd-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="212bd-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="212bd-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="212bd-145">INPUTS</span></span>

### <span data-ttu-id="212bd-146">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="212bd-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="212bd-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="212bd-147">OUTPUTS</span></span>

### <span data-ttu-id="212bd-148">Microsoft. Azure. Commands. Synapse. Models. PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="212bd-148">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="212bd-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="212bd-149">NOTES</span></span>

## <span data-ttu-id="212bd-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="212bd-150">RELATED LINKS</span></span>
