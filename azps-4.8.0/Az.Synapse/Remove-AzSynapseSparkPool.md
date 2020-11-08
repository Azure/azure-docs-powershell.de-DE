---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
ms.openlocfilehash: d9e3160d5ba0620ff881c940bf8383a7046136a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010337"
---
# <span data-ttu-id="1fba3-101">Remove-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="1fba3-101">Remove-AzSynapseSparkPool</span></span>

## <span data-ttu-id="1fba3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1fba3-102">SYNOPSIS</span></span>
<span data-ttu-id="1fba3-103">Löscht einen Synapse Analytics Spark Pool.</span><span class="sxs-lookup"><span data-stu-id="1fba3-103">Deletes a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="1fba3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1fba3-104">SYNTAX</span></span>

### <span data-ttu-id="1fba3-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1fba3-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fba3-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fba3-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fba3-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fba3-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -InputObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fba3-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fba3-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSparkPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fba3-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1fba3-109">DESCRIPTION</span></span>
<span data-ttu-id="1fba3-110">Mit dem Cmdlet **Remove-AzSynapseSparkPool** wird ein Azure Synapse Analytics-Spark-Pool endgültig gelöscht.</span><span class="sxs-lookup"><span data-stu-id="1fba3-110">The **Remove-AzSynapseSparkPool** cmdlet permanently deletes an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="1fba3-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1fba3-111">EXAMPLES</span></span>

### <span data-ttu-id="1fba3-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1fba3-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="1fba3-113">Mit diesem Befehl wird ein Azure Synapse Analytics-Spark-Pool gelöscht.</span><span class="sxs-lookup"><span data-stu-id="1fba3-113">This command deletes an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="1fba3-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1fba3-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Remove-AzSynapseSparkPool
```

<span data-ttu-id="1fba3-115">Mit diesem Befehl wird ein Azure Synapse Analytics-Spark-Pool durch Pipeline gelöscht.</span><span class="sxs-lookup"><span data-stu-id="1fba3-115">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="1fba3-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="1fba3-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSparkPool -Name ContosoSparkPool
```

<span data-ttu-id="1fba3-117">Mit diesem Befehl wird ein Azure Synapse Analytics-Spark-Pool durch Pipeline gelöscht.</span><span class="sxs-lookup"><span data-stu-id="1fba3-117">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="1fba3-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="1fba3-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool
```

<span data-ttu-id="1fba3-119">Mit diesem Befehl wird ein Azure Synapse Analytics-Spark-Pool mit einer Ressourcen-ID gelöscht.</span><span class="sxs-lookup"><span data-stu-id="1fba3-119">This command deletes an Azure Synapse Analytics Spark pool with a resource ID.</span></span>

## <span data-ttu-id="1fba3-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="1fba3-120">PARAMETERS</span></span>

### <span data-ttu-id="1fba3-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1fba3-121">-AsJob</span></span>
<span data-ttu-id="1fba3-122">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1fba3-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1fba3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fba3-123">-DefaultProfile</span></span>
<span data-ttu-id="1fba3-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1fba3-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fba3-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1fba3-125">-InputObject</span></span>
<span data-ttu-id="1fba3-126">Spark Pool-Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="1fba3-126">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1fba3-127">-Name</span><span class="sxs-lookup"><span data-stu-id="1fba3-127">-Name</span></span>
<span data-ttu-id="1fba3-128">Name des Synapsen-Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="1fba3-128">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="1fba3-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1fba3-129">-PassThru</span></span>
<span data-ttu-id="1fba3-130">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="1fba3-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="1fba3-131">Wenn dieser Schalter angegeben wird, wird true zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="1fba3-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="1fba3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fba3-132">-ResourceGroupName</span></span>
<span data-ttu-id="1fba3-133">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1fba3-133">Resource group name.</span></span>

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

### <span data-ttu-id="1fba3-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1fba3-134">-ResourceId</span></span>
<span data-ttu-id="1fba3-135">Ressourcen-ID des Synapse-Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="1fba3-135">Resource identifier of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="1fba3-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1fba3-136">-WorkspaceName</span></span>
<span data-ttu-id="1fba3-137">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="1fba3-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1fba3-138">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="1fba3-138">-WorkspaceObject</span></span>
<span data-ttu-id="1fba3-139">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="1fba3-139">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1fba3-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1fba3-140">-Confirm</span></span>
<span data-ttu-id="1fba3-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1fba3-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fba3-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fba3-142">-WhatIf</span></span>
<span data-ttu-id="1fba3-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1fba3-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fba3-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1fba3-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fba3-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fba3-145">CommonParameters</span></span>
<span data-ttu-id="1fba3-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fba3-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fba3-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1fba3-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fba3-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1fba3-148">INPUTS</span></span>

### <span data-ttu-id="1fba3-149">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1fba3-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="1fba3-150">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="1fba3-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="1fba3-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1fba3-151">OUTPUTS</span></span>

### <span data-ttu-id="1fba3-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1fba3-152">System.Boolean</span></span>

## <span data-ttu-id="1fba3-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="1fba3-153">NOTES</span></span>

## <span data-ttu-id="1fba3-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1fba3-154">RELATED LINKS</span></span>
