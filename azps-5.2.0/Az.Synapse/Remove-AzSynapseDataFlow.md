---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
ms.openlocfilehash: 2d0bec0c86f51771e971ca2c6b5a22c32f8ee687
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297883"
---
# <span data-ttu-id="a16f6-101">Remove-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="a16f6-101">Remove-AzSynapseDataFlow</span></span>

## <span data-ttu-id="a16f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a16f6-102">SYNOPSIS</span></span>
<span data-ttu-id="a16f6-103">Entfernt einen Datenfluss aus dem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="a16f6-103">Removes a data flow from workspace.</span></span>

## <span data-ttu-id="a16f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a16f6-104">SYNTAX</span></span>

### <span data-ttu-id="a16f6-105">RemoveByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a16f6-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a16f6-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="a16f6-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a16f6-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="a16f6-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataFlow -InputObject <PSDataFlowResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a16f6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a16f6-108">DESCRIPTION</span></span>
<span data-ttu-id="a16f6-109">Das **Cmdlet "Remove-AzSynapseDataFlow"** entfernt einen Datenfluss aus dem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="a16f6-109">The **Remove-AzSynapseDataFlow** cmdlet removes a data flow from workspace.</span></span>

## <span data-ttu-id="a16f6-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a16f6-110">EXAMPLES</span></span>

### <span data-ttu-id="a16f6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a16f6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="a16f6-112">Mit diesem Befehl wird der Datenfluss mit dem Namen "ContosoDataFlow" aus dem Arbeitsbereich "ContosoWorkspace" entfernt.</span><span class="sxs-lookup"><span data-stu-id="a16f6-112">This command removes the data flow named ContosoDataFlow from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="a16f6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a16f6-113">PARAMETERS</span></span>

### <span data-ttu-id="a16f6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a16f6-114">-AsJob</span></span>
<span data-ttu-id="a16f6-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a16f6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a16f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a16f6-116">-DefaultProfile</span></span>
<span data-ttu-id="a16f6-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a16f6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a16f6-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a16f6-118">-Force</span></span>
<span data-ttu-id="a16f6-119">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="a16f6-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a16f6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a16f6-120">-InputObject</span></span>
<span data-ttu-id="a16f6-121">Das Datenflussobjekt.</span><span class="sxs-lookup"><span data-stu-id="a16f6-121">The data flow object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a16f6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a16f6-122">-Name</span></span>
<span data-ttu-id="a16f6-123">Der Datenflussname.</span><span class="sxs-lookup"><span data-stu-id="a16f6-123">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: DataFlowName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16f6-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a16f6-124">-PassThru</span></span>
<span data-ttu-id="a16f6-125">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="a16f6-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a16f6-126">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="a16f6-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a16f6-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a16f6-127">-WorkspaceName</span></span>
<span data-ttu-id="a16f6-128">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="a16f6-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a16f6-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a16f6-129">-WorkspaceObject</span></span>
<span data-ttu-id="a16f6-130">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a16f6-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a16f6-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a16f6-131">-Confirm</span></span>
<span data-ttu-id="a16f6-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a16f6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a16f6-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a16f6-133">-WhatIf</span></span>
<span data-ttu-id="a16f6-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a16f6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a16f6-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a16f6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a16f6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a16f6-136">CommonParameters</span></span>
<span data-ttu-id="a16f6-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a16f6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a16f6-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a16f6-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a16f6-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a16f6-139">INPUTS</span></span>

### <span data-ttu-id="a16f6-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a16f6-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a16f6-141">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="a16f6-141">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="a16f6-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a16f6-142">OUTPUTS</span></span>

### <span data-ttu-id="a16f6-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a16f6-143">System.Boolean</span></span>

## <span data-ttu-id="a16f6-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a16f6-144">NOTES</span></span>

## <span data-ttu-id="a16f6-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a16f6-145">RELATED LINKS</span></span>
