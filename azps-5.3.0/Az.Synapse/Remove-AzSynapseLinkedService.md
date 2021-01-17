---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
ms.openlocfilehash: c70cc0f8659a04e8a10a4fbd2b776d22fca6a616
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383478"
---
# <span data-ttu-id="a28d7-101">Remove-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="a28d7-101">Remove-AzSynapseLinkedService</span></span>

## <span data-ttu-id="a28d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a28d7-102">SYNOPSIS</span></span>
<span data-ttu-id="a28d7-103">Entfernt einen verknüpften Dienst aus dem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="a28d7-103">Removes a linked service from workspace.</span></span>

## <span data-ttu-id="a28d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a28d7-104">SYNTAX</span></span>

### <span data-ttu-id="a28d7-105">RemoveByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a28d7-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a28d7-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="a28d7-106">RemoveByObject</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a28d7-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="a28d7-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseLinkedService -InputObject <PSLinkedServiceResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a28d7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a28d7-108">DESCRIPTION</span></span>
<span data-ttu-id="a28d7-109">Das **Cmdlet "Remove-AzSynapseLinkedService"** entfernt einen verknüpften Dienst aus dem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="a28d7-109">The **Remove-AzSynapseLinkedService** cmdlet removes a linked service from workspace.</span></span>

## <span data-ttu-id="a28d7-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a28d7-110">EXAMPLES</span></span>

### <span data-ttu-id="a28d7-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a28d7-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="a28d7-112">Mit diesem Befehl wird der verknüpfte Dienst "ContosoLinkedService" aus dem Arbeitsbereich "ContosoWorkspace" entfernt.</span><span class="sxs-lookup"><span data-stu-id="a28d7-112">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="a28d7-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a28d7-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="a28d7-114">Mit diesem Befehl wird der verknüpfte Dienst "ContosoLinkedService" über die Pipeline aus dem Arbeitsbereich "ContosoWorkspace" entfernt.</span><span class="sxs-lookup"><span data-stu-id="a28d7-114">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="a28d7-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a28d7-115">Example 3</span></span>
```powershell
PS C:\> $linkedService = Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
PS C:\> $linkedService | Remove-AzSynapseLinkedService
```

<span data-ttu-id="a28d7-116">Mit diesem Befehl wird der verknüpfte Dienst "ContosoLinkedService" über die Pipeline aus dem Arbeitsbereich "ContosoWorkspace" entfernt.</span><span class="sxs-lookup"><span data-stu-id="a28d7-116">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="a28d7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a28d7-117">PARAMETERS</span></span>

### <span data-ttu-id="a28d7-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a28d7-118">-AsJob</span></span>
<span data-ttu-id="a28d7-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a28d7-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a28d7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a28d7-120">-DefaultProfile</span></span>
<span data-ttu-id="a28d7-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a28d7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a28d7-122">-Force</span><span class="sxs-lookup"><span data-stu-id="a28d7-122">-Force</span></span>
<span data-ttu-id="a28d7-123">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="a28d7-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a28d7-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a28d7-124">-InputObject</span></span>
<span data-ttu-id="a28d7-125">Das verknüpfte Dienstobjekt.</span><span class="sxs-lookup"><span data-stu-id="a28d7-125">The linked service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a28d7-126">-Name</span><span class="sxs-lookup"><span data-stu-id="a28d7-126">-Name</span></span>
<span data-ttu-id="a28d7-127">Der Name des verknüpften Diensts.</span><span class="sxs-lookup"><span data-stu-id="a28d7-127">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: LinkedServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a28d7-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a28d7-128">-PassThru</span></span>
<span data-ttu-id="a28d7-129">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="a28d7-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a28d7-130">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="a28d7-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a28d7-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a28d7-131">-WorkspaceName</span></span>
<span data-ttu-id="a28d7-132">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="a28d7-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a28d7-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a28d7-133">-WorkspaceObject</span></span>
<span data-ttu-id="a28d7-134">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a28d7-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a28d7-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a28d7-135">-Confirm</span></span>
<span data-ttu-id="a28d7-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a28d7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a28d7-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a28d7-137">-WhatIf</span></span>
<span data-ttu-id="a28d7-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a28d7-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a28d7-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a28d7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a28d7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a28d7-140">CommonParameters</span></span>
<span data-ttu-id="a28d7-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a28d7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a28d7-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a28d7-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a28d7-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a28d7-143">INPUTS</span></span>

### <span data-ttu-id="a28d7-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a28d7-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a28d7-145">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="a28d7-145">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="a28d7-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a28d7-146">OUTPUTS</span></span>

### <span data-ttu-id="a28d7-147">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="a28d7-147">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="a28d7-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a28d7-148">NOTES</span></span>

## <span data-ttu-id="a28d7-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a28d7-149">RELATED LINKS</span></span>
