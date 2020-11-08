---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
ms.openlocfilehash: 28a4742b2e744fb41bca9402a8c48b830554e231
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008770"
---
# <span data-ttu-id="f679b-101">Get-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="f679b-101">Get-AzSynapseNotebook</span></span>

## <span data-ttu-id="f679b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f679b-102">SYNOPSIS</span></span>
<span data-ttu-id="f679b-103">Ruft Informationen zu Notizbüchern in einem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="f679b-103">Gets information about notebooks in a workspace.</span></span>

## <span data-ttu-id="f679b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f679b-104">SYNTAX</span></span>

### <span data-ttu-id="f679b-105">GetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="f679b-105">GetByName (Default)</span></span>
```
Get-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f679b-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="f679b-106">GetByObject</span></span>
```
Get-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f679b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f679b-107">DESCRIPTION</span></span>
<span data-ttu-id="f679b-108">Das Cmdlet " **Get-AzSynapseNotebook** " Ruft Informationen zu Notizbüchern in einem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="f679b-108">The **Get-AzSynapseNotebook** cmdlet gets information about notebooks in a workspace.</span></span> <span data-ttu-id="f679b-109">Wenn Sie den Namen eines Notizbuchs angeben, erhält das Cmdlet Informationen zu diesem Notizbuch.</span><span class="sxs-lookup"><span data-stu-id="f679b-109">If you specify the name of a notebook, the cmdlet gets information about that notebook.</span></span> <span data-ttu-id="f679b-110">Wenn Sie keinen Namen angeben, ruft das Cmdlet Informationen zu allen Notizbüchern im Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="f679b-110">If you do not specify a name, the cmdlet gets information about all notebooks in the workspace.</span></span>

## <span data-ttu-id="f679b-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f679b-111">EXAMPLES</span></span>

### <span data-ttu-id="f679b-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f679b-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace | Format-Table

WorkspaceName    Properties                                         Name
-------------    ----------                                         --
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook1
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook2
```

<span data-ttu-id="f679b-113">Ruft eine Liste aller Notizbücher im Arbeitsbereich ContosoWorkspace ab.</span><span class="sxs-lookup"><span data-stu-id="f679b-113">Gets a list of all notebooks in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="f679b-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f679b-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="f679b-115">Ruft ein einzelnes Notizbuch mit dem Namen ContosoNotebook im Arbeitsbereich ContosoWorkspace ab.</span><span class="sxs-lookup"><span data-stu-id="f679b-115">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="f679b-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="f679b-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="f679b-117">Ruft ein einzelnes Notizbuch mit dem Namen ContosoNotebook im Arbeitsbereich ContosoWorkspace through-Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="f679b-117">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="f679b-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="f679b-118">PARAMETERS</span></span>

### <span data-ttu-id="f679b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f679b-119">-DefaultProfile</span></span>
<span data-ttu-id="f679b-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f679b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f679b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f679b-121">-Name</span></span>
<span data-ttu-id="f679b-122">Der Name des Notizbuchs.</span><span class="sxs-lookup"><span data-stu-id="f679b-122">The notebook name.</span></span>

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

### <span data-ttu-id="f679b-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f679b-123">-WorkspaceName</span></span>
<span data-ttu-id="f679b-124">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="f679b-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f679b-125">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="f679b-125">-WorkspaceObject</span></span>
<span data-ttu-id="f679b-126">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="f679b-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f679b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f679b-127">CommonParameters</span></span>
<span data-ttu-id="f679b-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f679b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f679b-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f679b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f679b-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f679b-130">INPUTS</span></span>

### <span data-ttu-id="f679b-131">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f679b-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f679b-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f679b-132">OUTPUTS</span></span>

### <span data-ttu-id="f679b-133">Microsoft. Azure. Commands. Synapse. Models. PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="f679b-133">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="f679b-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="f679b-134">NOTES</span></span>

## <span data-ttu-id="f679b-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f679b-135">RELATED LINKS</span></span>
