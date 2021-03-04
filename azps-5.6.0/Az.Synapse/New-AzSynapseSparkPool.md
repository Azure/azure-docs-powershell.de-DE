---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/new-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
ms.openlocfilehash: c41c6afdda39843afa985a53eb572b64f8bcfe19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930648"
---
# <span data-ttu-id="b101c-101">New-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="b101c-101">New-AzSynapseSparkPool</span></span>

## <span data-ttu-id="b101c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b101c-102">SYNOPSIS</span></span>
<span data-ttu-id="b101c-103">Erstellt einen Synapse Analytics Spark-Pool.</span><span class="sxs-lookup"><span data-stu-id="b101c-103">Creates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="b101c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b101c-104">SYNTAX</span></span>

### <span data-ttu-id="b101c-105">CreateByNameAndEnableAutoScaleParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b101c-105">CreateByNameAndEnableAutoScaleParameterSet (Default)</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b101c-106">CreateByNameAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="b101c-106">CreateByNameAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b101c-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="b101c-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b101c-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="b101c-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b101c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b101c-109">DESCRIPTION</span></span>
<span data-ttu-id="b101c-110">Das **Cmdlet New-AzSynapseSparkPool** erstellt einen Azure Synapse Analytics Spark-Pool.</span><span class="sxs-lookup"><span data-stu-id="b101c-110">The **New-AzSynapseSparkPool** cmdlet creates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="b101c-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b101c-111">EXAMPLES</span></span>

### <span data-ttu-id="b101c-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b101c-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="b101c-113">Mit diesem Befehl wird ein Azure Synapse Analytics Spark-Pool erstellt.</span><span class="sxs-lookup"><span data-stu-id="b101c-113">This command creates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="b101c-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b101c-114">Example 2</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="b101c-115">Mit diesem Befehl wird ein Azure Synapse Analytics Spark-Pool mit aktivierter automatischer Skalierung erstellt.</span><span class="sxs-lookup"><span data-stu-id="b101c-115">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled.</span></span>

### <span data-ttu-id="b101c-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="b101c-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="b101c-117">Mit diesem Befehl wird über die Pipeline ein Azure Synapse Analytics Spark-Pool erstellt.</span><span class="sxs-lookup"><span data-stu-id="b101c-117">This command creates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="b101c-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="b101c-118">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="b101c-119">Mit diesem Befehl wird ein Azure Synapse Analytics Spark-Pool mit aktivierter automatischer Skalierung über die Pipeline erstellt.</span><span class="sxs-lookup"><span data-stu-id="b101c-119">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled through pipeline.</span></span>

## <span data-ttu-id="b101c-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b101c-120">PARAMETERS</span></span>

### <span data-ttu-id="b101c-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b101c-121">-AsJob</span></span>
<span data-ttu-id="b101c-122">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b101c-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b101c-123">-AutoPauseDelayInMinute</span><span class="sxs-lookup"><span data-stu-id="b101c-123">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="b101c-124">Anzahl der Minuten im Leerlauf.</span><span class="sxs-lookup"><span data-stu-id="b101c-124">Number of minutes idle.</span></span> <span data-ttu-id="b101c-125">Dieser Parameter muss angegeben werden, wenn die automatische Pause aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b101c-125">This parameter must be specified when Auto-pause is enabled.</span></span>

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

### <span data-ttu-id="b101c-126">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="b101c-126">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="b101c-127">Maximale Anzahl von Knoten, die im angegebenen Spark-Pool zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b101c-127">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="b101c-128">Dieser Parameter muss angegeben werden, wenn die automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b101c-128">This parameter must be specified when Auto-scale is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByParentObjectAndEnableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b101c-129">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="b101c-129">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="b101c-130">Mindestanzahl von Knoten, die im angegebenen Spark-Pool zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b101c-130">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="b101c-131">Dieser Parameter muss angegeben werden, wenn die automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b101c-131">This parameter must be specified when Auto-scale is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByParentObjectAndEnableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b101c-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b101c-132">-DefaultProfile</span></span>
<span data-ttu-id="b101c-133">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b101c-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b101c-134">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="b101c-134">-EnableAutoPause</span></span>
<span data-ttu-id="b101c-135">Gibt an, ob die automatische Pause aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b101c-135">Indicates whether Auto-pause should be enabled.</span></span>

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

### <span data-ttu-id="b101c-136">-LibraryRequirementsFilePath</span><span class="sxs-lookup"><span data-stu-id="b101c-136">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="b101c-137">Umgebungskonfigurationsdatei ("PIP freeze"-Ausgabe).</span><span class="sxs-lookup"><span data-stu-id="b101c-137">Environment configuration file ("PIP freeze" output).</span></span>

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

### <span data-ttu-id="b101c-138">-Name</span><span class="sxs-lookup"><span data-stu-id="b101c-138">-Name</span></span>
<span data-ttu-id="b101c-139">Name des Synapse Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="b101c-139">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SparkPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b101c-140">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="b101c-140">-NodeCount</span></span>
<span data-ttu-id="b101c-141">Die Anzahl der Knoten, die im angegebenen Spark-Pool zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b101c-141">Number of nodes to be allocated in the specified Spark pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByNameAndDisableAutoScaleParameterSet, CreateByParentObjectAndDisableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b101c-142">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="b101c-142">-NodeSize</span></span>
<span data-ttu-id="b101c-143">Anzahl des Kerns und des Arbeitsspeichers, der für Knoten verwendet werden soll, die im angegebenen Spark-Pool zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b101c-143">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="b101c-144">Dieser Parameter muss angegeben werden, wenn die automatische Skalierung deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b101c-144">This parameter must be specified when Auto-scale is disabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b101c-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b101c-145">-ResourceGroupName</span></span>
<span data-ttu-id="b101c-146">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b101c-146">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByNameAndDisableAutoScaleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b101c-147">-SparkVersion</span><span class="sxs-lookup"><span data-stu-id="b101c-147">-SparkVersion</span></span>
<span data-ttu-id="b101c-148">Apache Spark-Version.</span><span class="sxs-lookup"><span data-stu-id="b101c-148">Apache Spark version.</span></span>
<span data-ttu-id="b101c-149">Zulässige Werte: 2,4</span><span class="sxs-lookup"><span data-stu-id="b101c-149">Allowed values: 2.4</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b101c-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="b101c-150">-Tag</span></span>
<span data-ttu-id="b101c-151">Eine Zeichenfolge, ein Zeichenfolgenwörterbuch mit Tags, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b101c-151">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="b101c-152">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b101c-152">-WorkspaceName</span></span>
<span data-ttu-id="b101c-153">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="b101c-153">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByNameAndDisableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b101c-154">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b101c-154">-WorkspaceObject</span></span>
<span data-ttu-id="b101c-155">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="b101c-155">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectAndEnableAutoScaleParameterSet, CreateByParentObjectAndDisableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b101c-156">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b101c-156">-Confirm</span></span>
<span data-ttu-id="b101c-157">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b101c-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b101c-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b101c-158">-WhatIf</span></span>
<span data-ttu-id="b101c-159">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b101c-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b101c-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b101c-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b101c-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b101c-161">CommonParameters</span></span>
<span data-ttu-id="b101c-162">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b101c-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b101c-163">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b101c-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b101c-164">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b101c-164">INPUTS</span></span>

### <span data-ttu-id="b101c-165">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b101c-165">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b101c-166">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b101c-166">OUTPUTS</span></span>

### <span data-ttu-id="b101c-167">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="b101c-167">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="b101c-168">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b101c-168">NOTES</span></span>

## <span data-ttu-id="b101c-169">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b101c-169">RELATED LINKS</span></span>
