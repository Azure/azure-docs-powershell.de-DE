---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
ms.openlocfilehash: 23bd6186f31199ab9387df5ee78ce3fdbe89032e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162809"
---
# <span data-ttu-id="ef37c-101">Remove-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="ef37c-101">Remove-AzSynapseNotebook</span></span>

## <span data-ttu-id="ef37c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef37c-102">SYNOPSIS</span></span>
<span data-ttu-id="ef37c-103">Entfernt ein Notizbuch aus einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="ef37c-103">Removes a notebook from a workspace.</span></span>

## <span data-ttu-id="ef37c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef37c-104">SYNTAX</span></span>

### <span data-ttu-id="ef37c-105">RemoveByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="ef37c-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseNotebook -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef37c-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="ef37c-106">RemoveByObject</span></span>
```
Remove-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef37c-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="ef37c-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseNotebook -InputObject <PSNotebookResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef37c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef37c-108">DESCRIPTION</span></span>
<span data-ttu-id="ef37c-109">Das **Cmdlet "Remove-AzSynapseNotebook"** entfernt ein Notizbuch aus einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="ef37c-109">The **Remove-AzSynapseNotebook** cmdlet removes a notebook from a workspace.</span></span>

## <span data-ttu-id="ef37c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ef37c-110">EXAMPLES</span></span>

### <span data-ttu-id="ef37c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ef37c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="ef37c-112">Entfernen Sie ein Notizbuch namens "ContosoNotebook" aus dem Arbeitsbereich "ContosoWorkspace".</span><span class="sxs-lookup"><span data-stu-id="ef37c-112">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="ef37c-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ef37c-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="ef37c-114">Entfernen Sie über die Pipeline ein Notizbuch namens "ContosoNotebook" aus dem Arbeitsbereich "ContosoWorkspace".</span><span class="sxs-lookup"><span data-stu-id="ef37c-114">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="ef37c-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ef37c-115">Example 3</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Remove-AzSynapseNotebook
```

<span data-ttu-id="ef37c-116">Entfernen Sie über die Pipeline ein Notizbuch namens "ContosoNotebook" aus dem Arbeitsbereich "ContosoWorkspace".</span><span class="sxs-lookup"><span data-stu-id="ef37c-116">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="ef37c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef37c-117">PARAMETERS</span></span>

### <span data-ttu-id="ef37c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef37c-118">-AsJob</span></span>
<span data-ttu-id="ef37c-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ef37c-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ef37c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef37c-120">-DefaultProfile</span></span>
<span data-ttu-id="ef37c-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef37c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef37c-122">-Force</span><span class="sxs-lookup"><span data-stu-id="ef37c-122">-Force</span></span>
<span data-ttu-id="ef37c-123">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="ef37c-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ef37c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef37c-124">-InputObject</span></span>
<span data-ttu-id="ef37c-125">Das Notizbuchobjekt.</span><span class="sxs-lookup"><span data-stu-id="ef37c-125">The notebook object.</span></span>

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

### <span data-ttu-id="ef37c-126">-Name</span><span class="sxs-lookup"><span data-stu-id="ef37c-126">-Name</span></span>
<span data-ttu-id="ef37c-127">Der Notizbuchname.</span><span class="sxs-lookup"><span data-stu-id="ef37c-127">The notebook name.</span></span>

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

### <span data-ttu-id="ef37c-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef37c-128">-PassThru</span></span>
<span data-ttu-id="ef37c-129">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="ef37c-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="ef37c-130">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="ef37c-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="ef37c-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ef37c-131">-WorkspaceName</span></span>
<span data-ttu-id="ef37c-132">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="ef37c-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ef37c-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ef37c-133">-WorkspaceObject</span></span>
<span data-ttu-id="ef37c-134">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="ef37c-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ef37c-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef37c-135">-Confirm</span></span>
<span data-ttu-id="ef37c-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ef37c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef37c-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ef37c-137">-WhatIf</span></span>
<span data-ttu-id="ef37c-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ef37c-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef37c-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ef37c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef37c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef37c-140">CommonParameters</span></span>
<span data-ttu-id="ef37c-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef37c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef37c-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef37c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef37c-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ef37c-143">INPUTS</span></span>

### <span data-ttu-id="ef37c-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ef37c-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ef37c-145">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="ef37c-145">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="ef37c-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ef37c-146">OUTPUTS</span></span>

### <span data-ttu-id="ef37c-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ef37c-147">System.Boolean</span></span>

## <span data-ttu-id="ef37c-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ef37c-148">NOTES</span></span>

## <span data-ttu-id="ef37c-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ef37c-149">RELATED LINKS</span></span>
