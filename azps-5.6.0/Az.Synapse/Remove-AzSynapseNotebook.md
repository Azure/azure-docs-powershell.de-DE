---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
ms.openlocfilehash: 6203143eb2d386b627d0208730987709b1dd68c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934587"
---
# <span data-ttu-id="4e320-101">Remove-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="4e320-101">Remove-AzSynapseNotebook</span></span>

## <span data-ttu-id="4e320-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e320-102">SYNOPSIS</span></span>
<span data-ttu-id="4e320-103">Entfernt ein Notizbuch aus einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="4e320-103">Removes a notebook from a workspace.</span></span>

## <span data-ttu-id="4e320-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4e320-104">SYNTAX</span></span>

### <span data-ttu-id="4e320-105">RemoveByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="4e320-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseNotebook -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e320-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="4e320-106">RemoveByObject</span></span>
```
Remove-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e320-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="4e320-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseNotebook -InputObject <PSNotebookResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e320-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4e320-108">DESCRIPTION</span></span>
<span data-ttu-id="4e320-109">Das **Cmdlet Remove-AzSynapseNotebook** entfernt ein Notizbuch aus einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="4e320-109">The **Remove-AzSynapseNotebook** cmdlet removes a notebook from a workspace.</span></span>

## <span data-ttu-id="4e320-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4e320-110">EXAMPLES</span></span>

### <span data-ttu-id="4e320-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4e320-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="4e320-112">Entfernen Sie ein Notizbuch namens ContosoNotebook aus dem Arbeitsbereich ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="4e320-112">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="4e320-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4e320-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="4e320-114">Entfernen Sie ein Notizbuch namens ContosoNotebook über die Pipeline aus dem Arbeitsbereich ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="4e320-114">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="4e320-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="4e320-115">Example 3</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Remove-AzSynapseNotebook
```

<span data-ttu-id="4e320-116">Entfernen Sie ein Notizbuch namens ContosoNotebook über die Pipeline aus dem Arbeitsbereich ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="4e320-116">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="4e320-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4e320-117">PARAMETERS</span></span>

### <span data-ttu-id="4e320-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e320-118">-AsJob</span></span>
<span data-ttu-id="4e320-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4e320-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4e320-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e320-120">-DefaultProfile</span></span>
<span data-ttu-id="4e320-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4e320-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e320-122">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="4e320-122">-Force</span></span>
<span data-ttu-id="4e320-123">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="4e320-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4e320-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e320-124">-InputObject</span></span>
<span data-ttu-id="4e320-125">Das Notizbuchobjekt.</span><span class="sxs-lookup"><span data-stu-id="4e320-125">The notebook object.</span></span>

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

### <span data-ttu-id="4e320-126">-Name</span><span class="sxs-lookup"><span data-stu-id="4e320-126">-Name</span></span>
<span data-ttu-id="4e320-127">Der Name des Notizbuchs.</span><span class="sxs-lookup"><span data-stu-id="4e320-127">The notebook name.</span></span>

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

### <span data-ttu-id="4e320-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e320-128">-PassThru</span></span>
<span data-ttu-id="4e320-129">Dieses Cmdlet gibt standardmäßig kein -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="4e320-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="4e320-130">Wenn dieser Schalter angegeben ist, gibt er "true" zurück, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="4e320-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="4e320-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4e320-131">-WorkspaceName</span></span>
<span data-ttu-id="4e320-132">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="4e320-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4e320-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4e320-133">-WorkspaceObject</span></span>
<span data-ttu-id="4e320-134">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="4e320-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4e320-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4e320-135">-Confirm</span></span>
<span data-ttu-id="4e320-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4e320-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e320-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e320-137">-WhatIf</span></span>
<span data-ttu-id="4e320-138">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4e320-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e320-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4e320-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e320-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e320-140">CommonParameters</span></span>
<span data-ttu-id="4e320-141">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e320-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e320-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e320-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e320-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4e320-143">INPUTS</span></span>

### <span data-ttu-id="4e320-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4e320-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="4e320-145">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="4e320-145">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="4e320-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4e320-146">OUTPUTS</span></span>

### <span data-ttu-id="4e320-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4e320-147">System.Boolean</span></span>

## <span data-ttu-id="4e320-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4e320-148">NOTES</span></span>

## <span data-ttu-id="4e320-149">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4e320-149">RELATED LINKS</span></span>
