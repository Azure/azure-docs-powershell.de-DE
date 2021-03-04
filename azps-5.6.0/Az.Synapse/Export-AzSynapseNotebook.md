---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/export-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
ms.openlocfilehash: 110d72f0a73a6a710e014a08c64cadf3b8be7d0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933547"
---
# <span data-ttu-id="8c52e-101">Export-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="8c52e-101">Export-AzSynapseNotebook</span></span>

## <span data-ttu-id="8c52e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c52e-102">SYNOPSIS</span></span>
<span data-ttu-id="8c52e-103">Exportiert Notbooks.</span><span class="sxs-lookup"><span data-stu-id="8c52e-103">Exports notbooks.</span></span>

## <span data-ttu-id="8c52e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c52e-104">SYNTAX</span></span>

### <span data-ttu-id="8c52e-105">ExportByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="8c52e-105">ExportByName (Default)</span></span>
```
Export-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c52e-106">ExportByObject</span><span class="sxs-lookup"><span data-stu-id="8c52e-106">ExportByObject</span></span>
```
Export-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c52e-107">ExportByInputObject</span><span class="sxs-lookup"><span data-stu-id="8c52e-107">ExportByInputObject</span></span>
```
Export-AzSynapseNotebook -InputObject <PSNotebookResource> -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c52e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8c52e-108">DESCRIPTION</span></span>
<span data-ttu-id="8c52e-109">Das **Cmdlet Export-AzSynapseNotebook** exportiert ein Azure Synapse-Notizbuch in eine Notizbuchdatei (IPYNB).</span><span class="sxs-lookup"><span data-stu-id="8c52e-109">The **Export-AzSynapseNotebook** cmdlet exports an Azure Synapse notebook to a notebook (.ipynb) file.</span></span> <span data-ttu-id="8c52e-110">Der Name des Notizbuchs wird zum Namen der exportierten Datei.</span><span class="sxs-lookup"><span data-stu-id="8c52e-110">The name of the notebook becomes the name of the exported file.</span></span> <span data-ttu-id="8c52e-111">Wenn Sie den Namen eines Notizbuchs angeben, exportiert das Cmdlet dieses Notizbuch.</span><span class="sxs-lookup"><span data-stu-id="8c52e-111">If you specify the name of a notebook, the cmdlet exports that notebook.</span></span> <span data-ttu-id="8c52e-112">Wenn Sie keinen Namen angeben, exportiert das Cmdlet alle Notizbücher im Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="8c52e-112">If you do not specify a name, the cmdlet export all notebooks in the workspace.</span></span>

## <span data-ttu-id="8c52e-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8c52e-113">EXAMPLES</span></span>

### <span data-ttu-id="8c52e-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8c52e-114">Example 1</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -OutputFolder "C:\Notebook"
```

<span data-ttu-id="8c52e-115">Exportiert alle Notizbücher im Arbeitsbereich ContosoWorkspace in den Ordner "C:\Notizbuch".</span><span class="sxs-lookup"><span data-stu-id="8c52e-115">Exports all notebooks in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="8c52e-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8c52e-116">Example 2</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="8c52e-117">Exportiert ein einzelnes Notizbuch namens ContosoNotebook im Arbeitsbereich ContosoWorkspace in den Ordner "C:\Notizbuch".</span><span class="sxs-lookup"><span data-stu-id="8c52e-117">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="8c52e-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="8c52e-118">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Export-AzSynapseNotebook -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="8c52e-119">Exportiert ein einzelnes Notizbuch namens ContosoNotebook im Arbeitsbereich ContosoWorkspace über die Pipeline in den Ordner "C:\Notizbuch".</span><span class="sxs-lookup"><span data-stu-id="8c52e-119">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

### <span data-ttu-id="8c52e-120">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="8c52e-120">Example 4</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Export-AzSynapseNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="8c52e-121">Exportiert ein einzelnes Notizbuch namens ContosoNotebook im Arbeitsbereich ContosoWorkspace über die Pipeline in den Ordner "C:\Notizbuch".</span><span class="sxs-lookup"><span data-stu-id="8c52e-121">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

## <span data-ttu-id="8c52e-122">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8c52e-122">PARAMETERS</span></span>

### <span data-ttu-id="8c52e-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c52e-123">-AsJob</span></span>
<span data-ttu-id="8c52e-124">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8c52e-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8c52e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c52e-125">-DefaultProfile</span></span>
<span data-ttu-id="8c52e-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8c52e-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c52e-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c52e-127">-InputObject</span></span>
<span data-ttu-id="8c52e-128">Das Notizbuchobjekt.</span><span class="sxs-lookup"><span data-stu-id="8c52e-128">The notebook object.</span></span>

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

### <span data-ttu-id="8c52e-129">-Name</span><span class="sxs-lookup"><span data-stu-id="8c52e-129">-Name</span></span>
<span data-ttu-id="8c52e-130">Der Name des Notizbuchs.</span><span class="sxs-lookup"><span data-stu-id="8c52e-130">The notebook name.</span></span>

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

### <span data-ttu-id="8c52e-131">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="8c52e-131">-OutputFolder</span></span>
<span data-ttu-id="8c52e-132">Der Ordner, in dem das Notizbuch platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8c52e-132">The folder where the notebook should be placed.</span></span>

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

### <span data-ttu-id="8c52e-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8c52e-133">-WorkspaceName</span></span>
<span data-ttu-id="8c52e-134">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="8c52e-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8c52e-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8c52e-135">-WorkspaceObject</span></span>
<span data-ttu-id="8c52e-136">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="8c52e-136">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8c52e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c52e-137">CommonParameters</span></span>
<span data-ttu-id="8c52e-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c52e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c52e-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c52e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c52e-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8c52e-140">INPUTS</span></span>

### <span data-ttu-id="8c52e-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8c52e-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="8c52e-142">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="8c52e-142">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="8c52e-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8c52e-143">OUTPUTS</span></span>

### <span data-ttu-id="8c52e-144">System.IO.FileInfo</span><span class="sxs-lookup"><span data-stu-id="8c52e-144">System.IO.FileInfo</span></span>

## <span data-ttu-id="8c52e-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8c52e-145">NOTES</span></span>

## <span data-ttu-id="8c52e-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8c52e-146">RELATED LINKS</span></span>
