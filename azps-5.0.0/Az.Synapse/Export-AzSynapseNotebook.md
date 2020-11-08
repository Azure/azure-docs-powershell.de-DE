---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/export-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
ms.openlocfilehash: d61038add8ded9f697bfef551e00aec24c8aaf3e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176370"
---
# <span data-ttu-id="e0cf4-101">Export-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="e0cf4-101">Export-AzSynapseNotebook</span></span>

## <span data-ttu-id="e0cf4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e0cf4-102">SYNOPSIS</span></span>
<span data-ttu-id="e0cf4-103">Exportiert Notbooks.</span><span class="sxs-lookup"><span data-stu-id="e0cf4-103">Exports notbooks.</span></span>

## <span data-ttu-id="e0cf4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0cf4-104">SYNTAX</span></span>

### <span data-ttu-id="e0cf4-105">ExportByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="e0cf4-105">ExportByName (Default)</span></span>
```
Export-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0cf4-106">ExportByObject</span><span class="sxs-lookup"><span data-stu-id="e0cf4-106">ExportByObject</span></span>
```
Export-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0cf4-107">ExportByInputObject</span><span class="sxs-lookup"><span data-stu-id="e0cf4-107">ExportByInputObject</span></span>
```
Export-AzSynapseNotebook -InputObject <PSNotebookResource> -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0cf4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e0cf4-108">DESCRIPTION</span></span>
<span data-ttu-id="e0cf4-109">Das Cmdlet **Export-AzSynapseNotebook** exportiert ein Azure Synapse-Notizbuch in eine Notizbuch-Datei (. ipynb).</span><span class="sxs-lookup"><span data-stu-id="e0cf4-109">The **Export-AzSynapseNotebook** cmdlet exports an Azure Synapse notebook to a notebook (.ipynb) file.</span></span> <span data-ttu-id="e0cf4-110">Der Name des Notizbuchs wird zum Namen der exportierten Datei.</span><span class="sxs-lookup"><span data-stu-id="e0cf4-110">The name of the notebook becomes the name of the exported file.</span></span> <span data-ttu-id="e0cf4-111">Wenn Sie den Namen eines Notizbuchs angeben, wird dieses Notizbuch vom Cmdlet exportiert.</span><span class="sxs-lookup"><span data-stu-id="e0cf4-111">If you specify the name of a notebook, the cmdlet exports that notebook.</span></span> <span data-ttu-id="e0cf4-112">Wenn Sie keinen Namen angeben, werden alle Notizbücher im Arbeitsbereich vom Cmdlet exportiert.</span><span class="sxs-lookup"><span data-stu-id="e0cf4-112">If you do not specify a name, the cmdlet export all notebooks in the workspace.</span></span>

## <span data-ttu-id="e0cf4-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e0cf4-113">EXAMPLES</span></span>

### <span data-ttu-id="e0cf4-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e0cf4-114">Example 1</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -OutputFolder "C:\Notebook"
```

<span data-ttu-id="e0cf4-115">Exportiert alle Notizbücher im Arbeitsbereich ContosoWorkspace in den Ordner "C:\Notebook".</span><span class="sxs-lookup"><span data-stu-id="e0cf4-115">Exports all notebooks in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="e0cf4-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e0cf4-116">Example 2</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="e0cf4-117">Exportiert ein einzelnes Notizbuch namens ContosoNotebook im Arbeitsbereich ContosoWorkspace in den Ordner "C:\Notebook".</span><span class="sxs-lookup"><span data-stu-id="e0cf4-117">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="e0cf4-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e0cf4-118">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Export-AzSynapseNotebook -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="e0cf4-119">Exportiert ein einzelnes Notizbuch mit dem Namen ContosoNotebook im Arbeitsbereich ContosoWorkspace in den Ordner "C:\Notebook" bis zur Pipeline.</span><span class="sxs-lookup"><span data-stu-id="e0cf4-119">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

### <span data-ttu-id="e0cf4-120">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="e0cf4-120">Example 4</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Export-AzSynapseNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="e0cf4-121">Exportiert ein einzelnes Notizbuch mit dem Namen ContosoNotebook im Arbeitsbereich ContosoWorkspace in den Ordner "C:\Notebook" bis zur Pipeline.</span><span class="sxs-lookup"><span data-stu-id="e0cf4-121">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

## <span data-ttu-id="e0cf4-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0cf4-122">PARAMETERS</span></span>

### <span data-ttu-id="e0cf4-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0cf4-123">-AsJob</span></span>
<span data-ttu-id="e0cf4-124">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e0cf4-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e0cf4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0cf4-125">-DefaultProfile</span></span>
<span data-ttu-id="e0cf4-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e0cf4-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0cf4-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e0cf4-127">-InputObject</span></span>
<span data-ttu-id="e0cf4-128">Das Notizbuch-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e0cf4-128">The notebook object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource
Parameter Sets: ExportByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0cf4-129">-Name</span><span class="sxs-lookup"><span data-stu-id="e0cf4-129">-Name</span></span>
<span data-ttu-id="e0cf4-130">Der Name des Notizbuchs.</span><span class="sxs-lookup"><span data-stu-id="e0cf4-130">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByName, ExportByObject
Aliases: NotebookName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0cf4-131">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="e0cf4-131">-OutputFolder</span></span>
<span data-ttu-id="e0cf4-132">Der Ordner, in dem das Notizbuch gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e0cf4-132">The folder where the notebook should be placed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0cf4-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e0cf4-133">-WorkspaceName</span></span>
<span data-ttu-id="e0cf4-134">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="e0cf4-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0cf4-135">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="e0cf4-135">-WorkspaceObject</span></span>
<span data-ttu-id="e0cf4-136">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="e0cf4-136">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ExportByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0cf4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0cf4-137">CommonParameters</span></span>
<span data-ttu-id="e0cf4-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0cf4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0cf4-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0cf4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0cf4-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e0cf4-140">INPUTS</span></span>

### <span data-ttu-id="e0cf4-141">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e0cf4-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e0cf4-142">Microsoft. Azure. Commands. Synapse. Models. PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="e0cf4-142">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="e0cf4-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e0cf4-143">OUTPUTS</span></span>

### <span data-ttu-id="e0cf4-144">System. IO. FileInfo</span><span class="sxs-lookup"><span data-stu-id="e0cf4-144">System.IO.FileInfo</span></span>

## <span data-ttu-id="e0cf4-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="e0cf4-145">NOTES</span></span>

## <span data-ttu-id="e0cf4-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e0cf4-146">RELATED LINKS</span></span>
