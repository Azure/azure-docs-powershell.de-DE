---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
ms.openlocfilehash: c931bff1ba95ee1be185b5fe4dfdc2256d2cafec
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368512"
---
# <span data-ttu-id="19659-101">New-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="19659-101">New-AzSynapseSparkPool</span></span>

## <span data-ttu-id="19659-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19659-102">SYNOPSIS</span></span>
<span data-ttu-id="19659-103">Erstellt einen Synapse Analytics Spark-Pool.</span><span class="sxs-lookup"><span data-stu-id="19659-103">Creates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="19659-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="19659-104">SYNTAX</span></span>

### <span data-ttu-id="19659-105">CreateByNameAndEnableAutoScaleParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="19659-105">CreateByNameAndEnableAutoScaleParameterSet (Default)</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19659-106">CreateByNameAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="19659-106">CreateByNameAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19659-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="19659-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19659-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="19659-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19659-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="19659-109">DESCRIPTION</span></span>
<span data-ttu-id="19659-110">Das **Cmdlet "New-AzSynapseSparkPool"** erstellt einen Azure Synapse Analytics Spark-Pool.</span><span class="sxs-lookup"><span data-stu-id="19659-110">The **New-AzSynapseSparkPool** cmdlet creates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="19659-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="19659-111">EXAMPLES</span></span>

### <span data-ttu-id="19659-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="19659-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="19659-113">Mit diesem Befehl wird ein Azure Synapse Analytics Spark-Pool erstellt.</span><span class="sxs-lookup"><span data-stu-id="19659-113">This command creates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="19659-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="19659-114">Example 2</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="19659-115">Mit diesem Befehl wird ein Azure Synapse Analytics Spark-Pool mit aktivierter automatischer Skalierung erstellt.</span><span class="sxs-lookup"><span data-stu-id="19659-115">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled.</span></span>

### <span data-ttu-id="19659-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="19659-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="19659-117">Mit diesem Befehl wird über die Pipeline ein Azure Synapse Analytics Spark-Pool erstellt.</span><span class="sxs-lookup"><span data-stu-id="19659-117">This command creates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="19659-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="19659-118">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="19659-119">Mit diesem Befehl wird ein Azure Synapse Analytics Spark-Pool mit aktivierter automatischer Skalierung über die Pipeline erstellt.</span><span class="sxs-lookup"><span data-stu-id="19659-119">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled through pipeline.</span></span>

## <span data-ttu-id="19659-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19659-120">PARAMETERS</span></span>

### <span data-ttu-id="19659-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19659-121">-AsJob</span></span>
<span data-ttu-id="19659-122">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="19659-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="19659-123">-AutoPauseDelayInMinute</span><span class="sxs-lookup"><span data-stu-id="19659-123">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="19659-124">Anzahl der Minuten im Leerlauf.</span><span class="sxs-lookup"><span data-stu-id="19659-124">Number of minutes idle.</span></span> <span data-ttu-id="19659-125">Dieser Parameter muss angegeben werden, wenn "Automatisches Anhalten" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="19659-125">This parameter must be specified when Auto-pause is enabled.</span></span>

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

### <span data-ttu-id="19659-126">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="19659-126">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="19659-127">Die maximale Anzahl von Knoten, die im angegebenen Sparkpool zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="19659-127">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="19659-128">Dieser Parameter muss angegeben werden, wenn die automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="19659-128">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="19659-129">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="19659-129">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="19659-130">Die minimale Anzahl von Knoten, die im angegebenen Sparkpool zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="19659-130">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="19659-131">Dieser Parameter muss angegeben werden, wenn die automatische Skalierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="19659-131">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="19659-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19659-132">-DefaultProfile</span></span>
<span data-ttu-id="19659-133">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="19659-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19659-134">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="19659-134">-EnableAutoPause</span></span>
<span data-ttu-id="19659-135">Gibt an, ob das automatische Anhalten aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="19659-135">Indicates whether Auto-pause should be enabled.</span></span>

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

### <span data-ttu-id="19659-136">-LibraryRequirementsFilePath</span><span class="sxs-lookup"><span data-stu-id="19659-136">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="19659-137">Umgebungskonfigurationsdatei ("PIP-Fixierung" Ausgabe).</span><span class="sxs-lookup"><span data-stu-id="19659-137">Environment configuration file ("PIP freeze" output).</span></span>

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

### <span data-ttu-id="19659-138">-Name</span><span class="sxs-lookup"><span data-stu-id="19659-138">-Name</span></span>
<span data-ttu-id="19659-139">Name des Synapse Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="19659-139">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="19659-140">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="19659-140">-NodeCount</span></span>
<span data-ttu-id="19659-141">Die Anzahl der Knoten, die im angegebenen Sparkpool zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="19659-141">Number of nodes to be allocated in the specified Spark pool.</span></span>

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

### <span data-ttu-id="19659-142">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="19659-142">-NodeSize</span></span>
<span data-ttu-id="19659-143">Die Anzahl des Kerns und des Arbeitsspeichers, der für Knoten verwendet werden soll, die im angegebenen Sparkpool zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="19659-143">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="19659-144">Dieser Parameter muss angegeben werden, wenn die automatische Skalierung deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="19659-144">This parameter must be specified when Auto-scale is disabled</span></span>

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

### <span data-ttu-id="19659-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19659-145">-ResourceGroupName</span></span>
<span data-ttu-id="19659-146">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="19659-146">Resource group name.</span></span>

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

### <span data-ttu-id="19659-147">-SparkVersion</span><span class="sxs-lookup"><span data-stu-id="19659-147">-SparkVersion</span></span>
<span data-ttu-id="19659-148">Apache Spark-Version.</span><span class="sxs-lookup"><span data-stu-id="19659-148">Apache Spark version.</span></span>
<span data-ttu-id="19659-149">Zulässige Werte: 2,4</span><span class="sxs-lookup"><span data-stu-id="19659-149">Allowed values: 2.4</span></span>

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

### <span data-ttu-id="19659-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="19659-150">-Tag</span></span>
<span data-ttu-id="19659-151">Ein Zeichenfolgenverzeichnis mit Tags, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="19659-151">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="19659-152">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="19659-152">-WorkspaceName</span></span>
<span data-ttu-id="19659-153">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="19659-153">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="19659-154">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="19659-154">-WorkspaceObject</span></span>
<span data-ttu-id="19659-155">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="19659-155">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="19659-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19659-156">-Confirm</span></span>
<span data-ttu-id="19659-157">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="19659-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19659-158">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="19659-158">-WhatIf</span></span>
<span data-ttu-id="19659-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="19659-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19659-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="19659-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19659-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19659-161">CommonParameters</span></span>
<span data-ttu-id="19659-162">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19659-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19659-163">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19659-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19659-164">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="19659-164">INPUTS</span></span>

### <span data-ttu-id="19659-165">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="19659-165">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="19659-166">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="19659-166">OUTPUTS</span></span>

### <span data-ttu-id="19659-167">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="19659-167">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="19659-168">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="19659-168">NOTES</span></span>

## <span data-ttu-id="19659-169">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="19659-169">RELATED LINKS</span></span>
