---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/start-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseSparkSession.md
ms.openlocfilehash: e7e873638e38ed8c0c561fce5c4cd425be7bafbb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939176"
---
# <span data-ttu-id="a9af7-101">Start-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="a9af7-101">Start-AzSynapseSparkSession</span></span>

## <span data-ttu-id="a9af7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9af7-102">SYNOPSIS</span></span>
<span data-ttu-id="a9af7-103">Startet eine Synapse Analytics Spark-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="a9af7-103">Starts a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="a9af7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9af7-104">SYNTAX</span></span>

### <span data-ttu-id="a9af7-105">CreateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a9af7-105">CreateByNameParameterSet (Default)</span></span>
```
Start-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-Language <String>] -Name <String>
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9af7-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9af7-106">CreateByParentObjectParameterSet</span></span>
```
Start-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-Language <String>] -Name <String>
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9af7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a9af7-107">DESCRIPTION</span></span>
<span data-ttu-id="a9af7-108">Das **Cmdlet Start-AzSynapseSparkSession** startet eine Synapse Analytics Spark-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="a9af7-108">The **Start-AzSynapseSparkSession** cmdlet starts a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="a9af7-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a9af7-109">EXAMPLES</span></span>

### <span data-ttu-id="a9af7-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a9af7-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
```

<span data-ttu-id="a9af7-111">Mit diesem Befehl wird eine Azure Synapse Analytics Spark-Sitzung gestartet.</span><span class="sxs-lookup"><span data-stu-id="a9af7-111">This command starts an Azure Synapse Analytics Spark session.</span></span>

### <span data-ttu-id="a9af7-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a9af7-112">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Start-AzSynapseSparkSession -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
```

<span data-ttu-id="a9af7-113">Mit diesem Befehl wird eine Azure Synapse Analytics Spark-Sitzung über eine Pipeline gestartet.</span><span class="sxs-lookup"><span data-stu-id="a9af7-113">This command starts an Azure Synapse Analytics Spark session through pipeline.</span></span>

## <span data-ttu-id="a9af7-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a9af7-114">PARAMETERS</span></span>

### <span data-ttu-id="a9af7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9af7-115">-AsJob</span></span>
<span data-ttu-id="a9af7-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a9af7-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a9af7-117">-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="a9af7-117">-Configuration</span></span>
<span data-ttu-id="a9af7-118">Spark-Konfigurationseigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a9af7-118">Spark configuration properties.</span></span>

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

### <span data-ttu-id="a9af7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9af7-119">-DefaultProfile</span></span>
<span data-ttu-id="a9af7-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a9af7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9af7-121">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="a9af7-121">-ExecutorCount</span></span>
<span data-ttu-id="a9af7-122">Die Anzahl der executors, die im angegebenen Spark-Pool für den Auftrag zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a9af7-122">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9af7-123">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="a9af7-123">-ExecutorSize</span></span>
<span data-ttu-id="a9af7-124">Anzahl des Kerns und des Arbeitsspeichers, der für Executoren verwendet werden soll, die im angegebenen Spark-Pool für den Auftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a9af7-124">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="a9af7-125">-Sprache</span><span class="sxs-lookup"><span data-stu-id="a9af7-125">-Language</span></span>
<span data-ttu-id="a9af7-126">Sprache des Ausführungscodes.</span><span class="sxs-lookup"><span data-stu-id="a9af7-126">Language of the execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp, SQL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9af7-127">-Name</span><span class="sxs-lookup"><span data-stu-id="a9af7-127">-Name</span></span>
<span data-ttu-id="a9af7-128">Name der Spark-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="a9af7-128">Name of Spark session.</span></span>

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

### <span data-ttu-id="a9af7-129">-ReferenceFile</span><span class="sxs-lookup"><span data-stu-id="a9af7-129">-ReferenceFile</span></span>
<span data-ttu-id="a9af7-130">Zusätzliche Dateien, die als Referenz in der Hauptdefinitionsdatei verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a9af7-130">Additional files used for reference in the main definition file.</span></span> <span data-ttu-id="a9af7-131">Durch Kommas getrennte Speicher-URI-Liste.</span><span class="sxs-lookup"><span data-stu-id="a9af7-131">Comma-separated storage URI list.</span></span> <span data-ttu-id="a9af7-132">z. B. " abfss://filesystem@account.dfs.core.windows.net/file1.txt , abfss://filesystem@account.dfs.core.windows.net/result/ "</span><span class="sxs-lookup"><span data-stu-id="a9af7-132">e.g. "abfss://filesystem@account.dfs.core.windows.net/file1.txt,abfss://filesystem@account.dfs.core.windows.net/result/"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9af7-133">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="a9af7-133">-SparkPoolName</span></span>
<span data-ttu-id="a9af7-134">Name des Synapse Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="a9af7-134">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9af7-135">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="a9af7-135">-SparkPoolObject</span></span>
<span data-ttu-id="a9af7-136">Spark pool input object, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="a9af7-136">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9af7-137">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a9af7-137">-WorkspaceName</span></span>
<span data-ttu-id="a9af7-138">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="a9af7-138">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9af7-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a9af7-139">-Confirm</span></span>
<span data-ttu-id="a9af7-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a9af7-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9af7-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9af7-141">-WhatIf</span></span>
<span data-ttu-id="a9af7-142">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a9af7-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9af7-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a9af7-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9af7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9af7-144">CommonParameters</span></span>
<span data-ttu-id="a9af7-145">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9af7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9af7-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9af7-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9af7-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a9af7-147">INPUTS</span></span>

### <span data-ttu-id="a9af7-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="a9af7-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="a9af7-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a9af7-149">OUTPUTS</span></span>

### <span data-ttu-id="a9af7-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="a9af7-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="a9af7-151">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a9af7-151">NOTES</span></span>

## <span data-ttu-id="a9af7-152">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a9af7-152">RELATED LINKS</span></span>
