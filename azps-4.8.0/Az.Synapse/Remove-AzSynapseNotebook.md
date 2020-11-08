---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
ms.openlocfilehash: 22570fa8d236675a8ad2acd712e1ff66c1bc5049
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010116"
---
# <span data-ttu-id="b729b-101">Remove-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="b729b-101">Remove-AzSynapseNotebook</span></span>

## <span data-ttu-id="b729b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b729b-102">SYNOPSIS</span></span>
<span data-ttu-id="b729b-103">Entfernt ein Notizbuch aus einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="b729b-103">Removes a notebook from a workspace.</span></span>

## <span data-ttu-id="b729b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b729b-104">SYNTAX</span></span>

### <span data-ttu-id="b729b-105">RemoveByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b729b-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseNotebook -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b729b-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="b729b-106">RemoveByObject</span></span>
```
Remove-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b729b-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="b729b-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseNotebook -InputObject <PSNotebookResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b729b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b729b-108">DESCRIPTION</span></span>
<span data-ttu-id="b729b-109">Mit dem Cmdlet **Remove-AzSynapseNotebook** wird ein Notizbuch aus einem Arbeitsbereich entfernt.</span><span class="sxs-lookup"><span data-stu-id="b729b-109">The **Remove-AzSynapseNotebook** cmdlet removes a notebook from a workspace.</span></span>

## <span data-ttu-id="b729b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b729b-110">EXAMPLES</span></span>

### <span data-ttu-id="b729b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b729b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="b729b-112">Entfernen Sie ein Notizbuch namens ContosoNotebook aus dem Arbeitsbereich ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="b729b-112">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="b729b-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b729b-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="b729b-114">Entfernen Sie ein Notizbuch namens ContosoNotebook aus dem Arbeitsbereich ContosoWorkspace through-Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b729b-114">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="b729b-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="b729b-115">Example 3</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Remove-AzSynapseNotebook
```

<span data-ttu-id="b729b-116">Entfernen Sie ein Notizbuch namens ContosoNotebook aus dem Arbeitsbereich ContosoWorkspace through-Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b729b-116">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="b729b-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="b729b-117">PARAMETERS</span></span>

### <span data-ttu-id="b729b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b729b-118">-AsJob</span></span>
<span data-ttu-id="b729b-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b729b-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b729b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b729b-120">-DefaultProfile</span></span>
<span data-ttu-id="b729b-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b729b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b729b-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b729b-122">-InputObject</span></span>
<span data-ttu-id="b729b-123">Das Notizbuch-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b729b-123">The notebook object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b729b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="b729b-124">-Name</span></span>
<span data-ttu-id="b729b-125">Der Name des Notizbuchs.</span><span class="sxs-lookup"><span data-stu-id="b729b-125">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: NotebookName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b729b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b729b-126">-PassThru</span></span>
<span data-ttu-id="b729b-127">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="b729b-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="b729b-128">Wenn dieser Schalter angegeben wird, wird true zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="b729b-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="b729b-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b729b-129">-WorkspaceName</span></span>
<span data-ttu-id="b729b-130">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="b729b-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b729b-131">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="b729b-131">-WorkspaceObject</span></span>
<span data-ttu-id="b729b-132">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="b729b-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b729b-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b729b-133">-Confirm</span></span>
<span data-ttu-id="b729b-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b729b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b729b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b729b-135">-WhatIf</span></span>
<span data-ttu-id="b729b-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b729b-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b729b-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b729b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b729b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b729b-138">CommonParameters</span></span>
<span data-ttu-id="b729b-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b729b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b729b-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b729b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b729b-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b729b-141">INPUTS</span></span>

### <span data-ttu-id="b729b-142">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b729b-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="b729b-143">Microsoft. Azure. Commands. Synapse. Models. PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="b729b-143">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="b729b-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b729b-144">OUTPUTS</span></span>

### <span data-ttu-id="b729b-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b729b-145">System.Boolean</span></span>

## <span data-ttu-id="b729b-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="b729b-146">NOTES</span></span>

## <span data-ttu-id="b729b-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b729b-147">RELATED LINKS</span></span>
