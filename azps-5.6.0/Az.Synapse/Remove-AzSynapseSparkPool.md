---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
ms.openlocfilehash: 22b006d096d1ab2457d53a97a6265bf950c4658e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924339"
---
# <span data-ttu-id="90f8e-101">Remove-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="90f8e-101">Remove-AzSynapseSparkPool</span></span>

## <span data-ttu-id="90f8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90f8e-102">SYNOPSIS</span></span>
<span data-ttu-id="90f8e-103">Löscht einen Synapse Analytics Spark-Pool.</span><span class="sxs-lookup"><span data-stu-id="90f8e-103">Deletes a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="90f8e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="90f8e-104">SYNTAX</span></span>

### <span data-ttu-id="90f8e-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="90f8e-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90f8e-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="90f8e-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90f8e-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="90f8e-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -InputObject <PSSynapseSparkPool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90f8e-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="90f8e-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSparkPool -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90f8e-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="90f8e-109">DESCRIPTION</span></span>
<span data-ttu-id="90f8e-110">Das **Cmdlet Remove-AzSynapseSparkPool** löscht einen Azure Synapse Analytics Spark-Pool endgültig.</span><span class="sxs-lookup"><span data-stu-id="90f8e-110">The **Remove-AzSynapseSparkPool** cmdlet permanently deletes an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="90f8e-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="90f8e-111">EXAMPLES</span></span>

### <span data-ttu-id="90f8e-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="90f8e-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="90f8e-113">Mit diesem Befehl wird ein Azure Synapse Analytics Spark-Pool gelöscht.</span><span class="sxs-lookup"><span data-stu-id="90f8e-113">This command deletes an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="90f8e-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="90f8e-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Remove-AzSynapseSparkPool
```

<span data-ttu-id="90f8e-115">Mit diesem Befehl wird ein Azure Synapse Analytics Spark-Pool über eine Pipeline gelöscht.</span><span class="sxs-lookup"><span data-stu-id="90f8e-115">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="90f8e-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="90f8e-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSparkPool -Name ContosoSparkPool
```

<span data-ttu-id="90f8e-117">Mit diesem Befehl wird ein Azure Synapse Analytics Spark-Pool über eine Pipeline gelöscht.</span><span class="sxs-lookup"><span data-stu-id="90f8e-117">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="90f8e-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="90f8e-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool
```

<span data-ttu-id="90f8e-119">Mit diesem Befehl wird ein Azure Synapse Analytics Spark-Pool mit einer Ressourcen-ID gelöscht.</span><span class="sxs-lookup"><span data-stu-id="90f8e-119">This command deletes an Azure Synapse Analytics Spark pool with a resource ID.</span></span>

## <span data-ttu-id="90f8e-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="90f8e-120">PARAMETERS</span></span>

### <span data-ttu-id="90f8e-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90f8e-121">-AsJob</span></span>
<span data-ttu-id="90f8e-122">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="90f8e-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="90f8e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90f8e-123">-DefaultProfile</span></span>
<span data-ttu-id="90f8e-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="90f8e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90f8e-125">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="90f8e-125">-Force</span></span>
<span data-ttu-id="90f8e-126">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="90f8e-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="90f8e-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90f8e-127">-InputObject</span></span>
<span data-ttu-id="90f8e-128">Spark pool input object, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="90f8e-128">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90f8e-129">-Name</span><span class="sxs-lookup"><span data-stu-id="90f8e-129">-Name</span></span>
<span data-ttu-id="90f8e-130">Name des Synapse Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="90f8e-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases: SparkPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90f8e-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90f8e-131">-PassThru</span></span>
<span data-ttu-id="90f8e-132">Dieses Cmdlet gibt standardmäßig kein -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="90f8e-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="90f8e-133">Wenn dieser Schalter angegeben ist, gibt er "true" zurück, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="90f8e-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="90f8e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90f8e-134">-ResourceGroupName</span></span>
<span data-ttu-id="90f8e-135">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="90f8e-135">Resource group name.</span></span>

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

### <span data-ttu-id="90f8e-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90f8e-136">-ResourceId</span></span>
<span data-ttu-id="90f8e-137">Ressourcenbezeichner des Synapse Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="90f8e-137">Resource identifier of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="90f8e-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="90f8e-138">-WorkspaceName</span></span>
<span data-ttu-id="90f8e-139">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="90f8e-139">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90f8e-140">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="90f8e-140">-WorkspaceObject</span></span>
<span data-ttu-id="90f8e-141">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="90f8e-141">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90f8e-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="90f8e-142">-Confirm</span></span>
<span data-ttu-id="90f8e-143">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="90f8e-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90f8e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90f8e-144">-WhatIf</span></span>
<span data-ttu-id="90f8e-145">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="90f8e-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90f8e-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="90f8e-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90f8e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90f8e-147">CommonParameters</span></span>
<span data-ttu-id="90f8e-148">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90f8e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90f8e-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90f8e-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90f8e-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="90f8e-150">INPUTS</span></span>

### <span data-ttu-id="90f8e-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="90f8e-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="90f8e-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="90f8e-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="90f8e-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="90f8e-153">OUTPUTS</span></span>

### <span data-ttu-id="90f8e-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="90f8e-154">System.Boolean</span></span>

## <span data-ttu-id="90f8e-155">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="90f8e-155">NOTES</span></span>

## <span data-ttu-id="90f8e-156">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="90f8e-156">RELATED LINKS</span></span>
