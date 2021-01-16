---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSparkPool.md
ms.openlocfilehash: 1ed539f6064d6f99aff632a43cee5f200d735b6d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470259"
---
# <span data-ttu-id="2fe17-101">Update-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="2fe17-101">Update-AzSynapseSparkPool</span></span>

## <span data-ttu-id="2fe17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fe17-102">SYNOPSIS</span></span>
<span data-ttu-id="2fe17-103">Aktualisiert einen Synapse Analytics Spark-Pool.</span><span class="sxs-lookup"><span data-stu-id="2fe17-103">Updates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="2fe17-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2fe17-104">SYNTAX</span></span>

### <span data-ttu-id="2fe17-105">SetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2fe17-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-EnableAutoScale <Boolean>] [-AutoScaleMinNodeCount <Int32>]
 [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>] [-AutoPauseDelayInMinute <Int32>]
 [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>] [-LibraryRequirementsFilePath <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fe17-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fe17-106">SetByParentObjectParameterSet</span></span>
```
Update-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-EnableAutoScale <Boolean>] [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>]
 [-EnableAutoPause <Boolean>] [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>]
 [-SparkVersion <String>] [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fe17-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fe17-107">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseSparkPool -InputObject <PSSynapseSparkPool> [-Tag <Hashtable>] [-EnableAutoScale <Boolean>]
 [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>]
 [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>]
 [-LibraryRequirementsFilePath <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fe17-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fe17-108">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseSparkPool -ResourceId <String> [-Tag <Hashtable>] [-EnableAutoScale <Boolean>]
 [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>]
 [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>]
 [-LibraryRequirementsFilePath <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fe17-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2fe17-109">DESCRIPTION</span></span>
<span data-ttu-id="2fe17-110">Das **Cmdlet "Update-AzSynapseSparkPool"** aktualisiert einen Azure Synapse Analytics Spark-Pool.</span><span class="sxs-lookup"><span data-stu-id="2fe17-110">The **Update-AzSynapseSparkPool** cmdlet updates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="2fe17-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2fe17-111">EXAMPLES</span></span>

### <span data-ttu-id="2fe17-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2fe17-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -Tag @{"key" = "value"} -NodeCount 5 -NodeSize Medium
```

<span data-ttu-id="2fe17-113">Mit diesem Befehl wird ein Azure Synapse Analytics Spark-Pool aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2fe17-113">This command updates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="2fe17-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2fe17-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
$pool | Update-AzSynapseSparkPool -Tag @{"key" = "value1"}
```

<span data-ttu-id="2fe17-115">Mit diesem Befehl wird ein Azure Synapse Analytics Spark-Pool über die Pipeline aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2fe17-115">This command updates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="2fe17-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="2fe17-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSparkPool -Name ContosoSparkPool -Tag @{"key" = "value2"}
```

<span data-ttu-id="2fe17-117">Mit diesem Befehl wird ein Azure Synapse Analytics Spark-Pool über die Pipeline aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2fe17-117">This command updates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="2fe17-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="2fe17-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool -Tag @{"key" = "value3"}
```

<span data-ttu-id="2fe17-119">Mit diesem Befehl wird ein Azure Synapse Analytics Spark-Pool mit Ressourcen-ID aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2fe17-119">This command updates an Azure Synapse Analytics Spark pool with resource ID.</span></span>

### <span data-ttu-id="2fe17-120">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="2fe17-120">Example 5</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoScale $true -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 7
```

<span data-ttu-id="2fe17-121">Dieser Befehl aktiviert die automatische Skalierung für einen Azure Synapse Analytics Spark-Pool.</span><span class="sxs-lookup"><span data-stu-id="2fe17-121">This command enables auto-scale for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="2fe17-122">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="2fe17-122">Example 6</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoScale $false
```

<span data-ttu-id="2fe17-123">Mit diesem Befehl wird die automatische Skalierung für einen Azure Synapse Analytics Spark-Pool deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="2fe17-123">This command disables auto-scale for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="2fe17-124">Beispiel 7</span><span class="sxs-lookup"><span data-stu-id="2fe17-124">Example 7</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoPause $true -AutoPauseDelayInMinute 15
```

<span data-ttu-id="2fe17-125">Dieser Befehl ermöglicht das automatische Anhalten für einen Azure Synapse Analytics Spark-Pool.</span><span class="sxs-lookup"><span data-stu-id="2fe17-125">This command enables auto-pause for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="2fe17-126">Beispiel 8</span><span class="sxs-lookup"><span data-stu-id="2fe17-126">Example 8</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoPause $false
```

<span data-ttu-id="2fe17-127">Mit diesem Befehl wird das automatische Anhalten für einen Azure Synapse Analytics Spark-Pool deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="2fe17-127">This command disables auto-pause for an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="2fe17-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2fe17-128">PARAMETERS</span></span>

### <span data-ttu-id="2fe17-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2fe17-129">-AsJob</span></span>
<span data-ttu-id="2fe17-130">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2fe17-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2fe17-131">-AutoPauseDelayInMinute</span><span class="sxs-lookup"><span data-stu-id="2fe17-131">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="2fe17-132">Anzahl der Minuten im Leerlauf.</span><span class="sxs-lookup"><span data-stu-id="2fe17-132">Number of minutes idle.</span></span> <span data-ttu-id="2fe17-133">Dieser Parameter muss angegeben werden, wenn "Automatisches Anhalten" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2fe17-133">This parameter must be specified when Auto-pause is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe17-134">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="2fe17-134">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="2fe17-135">Die maximale Anzahl von Knoten, die im angegebenen Sparkpool zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2fe17-135">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="2fe17-136">Dieser Parameter muss angegeben werden, wenn die automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2fe17-136">This parameter must be specified when Auto-scale is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe17-137">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="2fe17-137">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="2fe17-138">Die minimale Anzahl von Knoten, die im angegebenen Sparkpool zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2fe17-138">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="2fe17-139">Dieser Parameter muss angegeben werden, wenn die automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2fe17-139">This parameter must be specified when Auto-scale is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe17-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fe17-140">-DefaultProfile</span></span>
<span data-ttu-id="2fe17-141">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2fe17-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fe17-142">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="2fe17-142">-EnableAutoPause</span></span>
<span data-ttu-id="2fe17-143">Gibt an, ob das automatische Anhalten aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2fe17-143">Indicates whether Auto-pause should be enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe17-144">-EnableAutoScale</span><span class="sxs-lookup"><span data-stu-id="2fe17-144">-EnableAutoScale</span></span>
<span data-ttu-id="2fe17-145">Gibt an, ob die automatische Skalierung aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2fe17-145">Indicates whether Auto-scale should be enabled</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe17-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2fe17-146">-InputObject</span></span>
<span data-ttu-id="2fe17-147">Sparkpooleingabeobjekt, das normalerweise über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="2fe17-147">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2fe17-148">-LibraryRequirementsFilePath</span><span class="sxs-lookup"><span data-stu-id="2fe17-148">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="2fe17-149">Umgebungskonfigurationsdatei ("PIP-Fixierung" Ausgabe).</span><span class="sxs-lookup"><span data-stu-id="2fe17-149">Environment configuration file ("PIP freeze" output).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe17-150">-Name</span><span class="sxs-lookup"><span data-stu-id="2fe17-150">-Name</span></span>
<span data-ttu-id="2fe17-151">Name des Synapse Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="2fe17-151">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases: SparkPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe17-152">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="2fe17-152">-NodeCount</span></span>
<span data-ttu-id="2fe17-153">Die Anzahl der Knoten, die im angegebenen Sparkpool zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2fe17-153">Number of nodes to be allocated in the specified Spark pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe17-154">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="2fe17-154">-NodeSize</span></span>
<span data-ttu-id="2fe17-155">Die Anzahl des Kerns und des Arbeitsspeichers, der für Knoten verwendet werden soll, die im angegebenen Sparkpool zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="2fe17-155">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="2fe17-156">Dieser Parameter muss angegeben werden, wenn die automatische Skalierung deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2fe17-156">This parameter must be specified when Auto-scale is disabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe17-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fe17-157">-ResourceGroupName</span></span>
<span data-ttu-id="2fe17-158">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="2fe17-158">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe17-159">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2fe17-159">-ResourceId</span></span>
<span data-ttu-id="2fe17-160">Ressourcenbezeichner des Synapse Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="2fe17-160">Resource identifier of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe17-161">-SparkVersion</span><span class="sxs-lookup"><span data-stu-id="2fe17-161">-SparkVersion</span></span>
<span data-ttu-id="2fe17-162">Apache Spark-Version.</span><span class="sxs-lookup"><span data-stu-id="2fe17-162">Apache Spark version.</span></span>
<span data-ttu-id="2fe17-163">Zulässige Werte: 2,4</span><span class="sxs-lookup"><span data-stu-id="2fe17-163">Allowed values: 2.4</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe17-164">-Tag</span><span class="sxs-lookup"><span data-stu-id="2fe17-164">-Tag</span></span>
<span data-ttu-id="2fe17-165">Ein Zeichenfolgenverzeichnis mit Tags, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="2fe17-165">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe17-166">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2fe17-166">-WorkspaceName</span></span>
<span data-ttu-id="2fe17-167">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="2fe17-167">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe17-168">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2fe17-168">-WorkspaceObject</span></span>
<span data-ttu-id="2fe17-169">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="2fe17-169">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2fe17-170">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2fe17-170">-Confirm</span></span>
<span data-ttu-id="2fe17-171">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2fe17-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fe17-172">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2fe17-172">-WhatIf</span></span>
<span data-ttu-id="2fe17-173">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2fe17-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fe17-174">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2fe17-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fe17-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fe17-175">CommonParameters</span></span>
<span data-ttu-id="2fe17-176">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fe17-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fe17-177">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2fe17-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fe17-178">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2fe17-178">INPUTS</span></span>

### <span data-ttu-id="2fe17-179">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2fe17-179">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="2fe17-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="2fe17-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="2fe17-181">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2fe17-181">OUTPUTS</span></span>

### <span data-ttu-id="2fe17-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="2fe17-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="2fe17-183">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2fe17-183">NOTES</span></span>

## <span data-ttu-id="2fe17-184">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2fe17-184">RELATED LINKS</span></span>
