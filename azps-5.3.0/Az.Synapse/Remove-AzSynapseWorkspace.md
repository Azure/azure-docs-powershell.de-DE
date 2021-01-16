---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
ms.openlocfilehash: fbdca80b33dd15e34a958cb63a41377b400d03ce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470307"
---
# <span data-ttu-id="4338b-101">Remove-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4338b-101">Remove-AzSynapseWorkspace</span></span>

## <span data-ttu-id="4338b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4338b-102">SYNOPSIS</span></span>
<span data-ttu-id="4338b-103">Löscht einen Synapse Analytics-Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="4338b-103">Deletes a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="4338b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4338b-104">SYNTAX</span></span>

### <span data-ttu-id="4338b-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4338b-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseWorkspace [-ResourceGroupName <String>] -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4338b-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4338b-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4338b-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4338b-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseWorkspace -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4338b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4338b-108">DESCRIPTION</span></span>
<span data-ttu-id="4338b-109">Das **Cmdlet "Remove-AzSynapseWorkspace"** löscht einen Azure Synapse Analytics-Arbeitsbereich endgültig.</span><span class="sxs-lookup"><span data-stu-id="4338b-109">The **Remove-AzSynapseWorkspace** cmdlet permanently deletes an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="4338b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4338b-110">EXAMPLES</span></span>

### <span data-ttu-id="4338b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4338b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="4338b-112">Mit diesem Befehl wird ein Azure Synapse Analytics-Arbeitsbereich gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4338b-112">This command deletes an Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="4338b-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4338b-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseWorkspace
```

<span data-ttu-id="4338b-114">Mit diesem Befehl wird ein Azure Synapse Analytics-Arbeitsbereich über die Pipeline gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4338b-114">This command deletes an Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="4338b-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="4338b-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="4338b-116">Mit diesem Befehl wird ein Azure Synapse Analytics-Arbeitsbereich über die Pipeline mit der angegebenen Ressourcen-ID gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4338b-116">This command deletes an Azure Synapse Analytics workspace through pipeline with the specified resource ID.</span></span>

## <span data-ttu-id="4338b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4338b-117">PARAMETERS</span></span>

### <span data-ttu-id="4338b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4338b-118">-AsJob</span></span>
<span data-ttu-id="4338b-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4338b-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4338b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4338b-120">-DefaultProfile</span></span>
<span data-ttu-id="4338b-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4338b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4338b-122">-Force</span><span class="sxs-lookup"><span data-stu-id="4338b-122">-Force</span></span>
<span data-ttu-id="4338b-123">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="4338b-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4338b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4338b-124">-InputObject</span></span>
<span data-ttu-id="4338b-125">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="4338b-125">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4338b-126">-Name</span><span class="sxs-lookup"><span data-stu-id="4338b-126">-Name</span></span>
<span data-ttu-id="4338b-127">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="4338b-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4338b-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4338b-128">-PassThru</span></span>
<span data-ttu-id="4338b-129">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="4338b-129">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="4338b-130">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="4338b-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="4338b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4338b-131">-ResourceGroupName</span></span>
<span data-ttu-id="4338b-132">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="4338b-132">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4338b-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4338b-133">-ResourceId</span></span>
<span data-ttu-id="4338b-134">Ressourcenbezeichner des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="4338b-134">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4338b-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4338b-135">-Confirm</span></span>
<span data-ttu-id="4338b-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4338b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4338b-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4338b-137">-WhatIf</span></span>
<span data-ttu-id="4338b-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4338b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4338b-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4338b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4338b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4338b-140">CommonParameters</span></span>
<span data-ttu-id="4338b-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4338b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4338b-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4338b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4338b-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4338b-143">INPUTS</span></span>

### <span data-ttu-id="4338b-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4338b-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="4338b-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4338b-145">OUTPUTS</span></span>

### <span data-ttu-id="4338b-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4338b-146">System.Boolean</span></span>

## <span data-ttu-id="4338b-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4338b-147">NOTES</span></span>

## <span data-ttu-id="4338b-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4338b-148">RELATED LINKS</span></span>
