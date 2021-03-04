---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/submit-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
ms.openlocfilehash: 0555d9ba860d9a8c4c036fa9171d1fadc7a167eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948259"
---
# <span data-ttu-id="c0675-101">Submit-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="c0675-101">Submit-AzSynapseSparkJob</span></span>

## <span data-ttu-id="c0675-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0675-102">SYNOPSIS</span></span>
<span data-ttu-id="c0675-103">Sendet einen Synapse Analytics Spark-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="c0675-103">Submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="c0675-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c0675-104">SYNTAX</span></span>

### <span data-ttu-id="c0675-105">RunSparkJobParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c0675-105">RunSparkJobParameterSetName (Default)</span></span>
```
Submit-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0675-106">RunSparkJobByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0675-106">RunSparkJobByParentObjectParameterSet</span></span>
```
Submit-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0675-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c0675-107">DESCRIPTION</span></span>
<span data-ttu-id="c0675-108">Das **Cmdlet Submit-AzSynapseSparkJob** sendet einen Synapse Analytics Spark-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="c0675-108">The **Submit-AzSynapseSparkJob** cmdlet submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="c0675-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c0675-109">EXAMPLES</span></span>

### <span data-ttu-id="c0675-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c0675-110">Example 1</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language Spark -Name WordCount_Java -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/wordcount.jar -MainClassName WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="c0675-111">Mit diesem Befehl wird ein Synapse Analytics Spark-Auftrag übermittelt.</span><span class="sxs-lookup"><span data-stu-id="c0675-111">This command submits a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="c0675-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c0675-112">Example 2</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language SparkDotNet -Name WordCount_Dotnet -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/wordcount.zip -MainExecutableFile WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/result -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="c0675-113">Mit diesem Befehl wird ein Synapse Analytics Spark .NET-Auftrag übermittelt.</span><span class="sxs-lookup"><span data-stu-id="c0675-113">This command submits a Synapse Analytics Spark .NET job.</span></span>

### <span data-ttu-id="c0675-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c0675-114">Example 3</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language PySpark -Name WordCount_Python -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/wordcount.py -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="c0675-115">Mit diesem Befehl wird ein PySpark-Auftrag von Synapse Analytics übermittelt.</span><span class="sxs-lookup"><span data-stu-id="c0675-115">This command submits a Synapse Analytics PySpark job.</span></span>

## <span data-ttu-id="c0675-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c0675-116">PARAMETERS</span></span>

### <span data-ttu-id="c0675-117">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="c0675-117">-CommandLineArgument</span></span>
<span data-ttu-id="c0675-118">Optionale Argumente für den Auftrag.</span><span class="sxs-lookup"><span data-stu-id="c0675-118">Optional arguments to the job.</span></span> <span data-ttu-id="c0675-119">z. B. "--iteration 10000 --timeout 20s"</span><span class="sxs-lookup"><span data-stu-id="c0675-119">e.g. "--iteration 10000 --timeout 20s"</span></span>

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

### <span data-ttu-id="c0675-120">-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="c0675-120">-Configuration</span></span>
<span data-ttu-id="c0675-121">Spark-Konfigurationseigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c0675-121">Spark configuration properties.</span></span>

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

### <span data-ttu-id="c0675-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0675-122">-DefaultProfile</span></span>
<span data-ttu-id="c0675-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c0675-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0675-124">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="c0675-124">-ExecutorCount</span></span>
<span data-ttu-id="c0675-125">Die Anzahl der executors, die im angegebenen Spark-Pool für den Auftrag zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c0675-125">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="c0675-126">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="c0675-126">-ExecutorSize</span></span>
<span data-ttu-id="c0675-127">Anzahl des Kerns und des Arbeitsspeichers, der für Executoren verwendet werden soll, die im angegebenen Spark-Pool für den Auftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c0675-127">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="c0675-128">-Sprache</span><span class="sxs-lookup"><span data-stu-id="c0675-128">-Language</span></span>
<span data-ttu-id="c0675-129">Sprache des zu übermittelnden Auftrags.</span><span class="sxs-lookup"><span data-stu-id="c0675-129">Language of the job to submit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0675-130">-MainClassName</span><span class="sxs-lookup"><span data-stu-id="c0675-130">-MainClassName</span></span>
<span data-ttu-id="c0675-131">Der vollqualifizierte Bezeichner oder die Hauptklasse, die sich in der Hauptdefinitionsdatei befindet.</span><span class="sxs-lookup"><span data-stu-id="c0675-131">The fully-qualified identifier or the main class that is in the main definition file.</span></span>
<span data-ttu-id="c0675-132">Erforderlich für Spark- und .NET Spark-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="c0675-132">Required for Spark and .NET Spark job.</span></span>
<span data-ttu-id="c0675-133">z. B. "org.apache.spark.examples.SparkPi"</span><span class="sxs-lookup"><span data-stu-id="c0675-133">e.g. "org.apache.spark.examples.SparkPi"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MainExecutableFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0675-134">-MainDefinitionFile</span><span class="sxs-lookup"><span data-stu-id="c0675-134">-MainDefinitionFile</span></span>
<span data-ttu-id="c0675-135">Die Hauptdatei, die für den Auftrag verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c0675-135">The main file used for the job.</span></span>
<span data-ttu-id="c0675-136">z. B. " abfss://filesystem@account.dfs.core.windows.net/mySpark.jar "</span><span class="sxs-lookup"><span data-stu-id="c0675-136">e.g. "abfss://filesystem@account.dfs.core.windows.net/mySpark.jar"</span></span>

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

### <span data-ttu-id="c0675-137">-Name</span><span class="sxs-lookup"><span data-stu-id="c0675-137">-Name</span></span>
<span data-ttu-id="c0675-138">Name des Spark-Auftrags.</span><span class="sxs-lookup"><span data-stu-id="c0675-138">Name of Spark job.</span></span>

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

### <span data-ttu-id="c0675-139">-ReferenceFile</span><span class="sxs-lookup"><span data-stu-id="c0675-139">-ReferenceFile</span></span>
<span data-ttu-id="c0675-140">Zusätzliche Dateien, die als Referenz in der Hauptdefinitionsdatei verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c0675-140">Additional files used for reference in the main definition file.</span></span> <span data-ttu-id="c0675-141">Durch Kommas getrennte Speicher-URI-Liste.</span><span class="sxs-lookup"><span data-stu-id="c0675-141">Comma-separated storage URI list.</span></span> <span data-ttu-id="c0675-142">z. B. " abfss://filesystem@account.dfs.core.windows.net/file1.txt , abfss://filesystem@account.dfs.core.windows.net/result/ "</span><span class="sxs-lookup"><span data-stu-id="c0675-142">e.g. "abfss://filesystem@account.dfs.core.windows.net/file1.txt,abfss://filesystem@account.dfs.core.windows.net/result/"</span></span>

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

### <span data-ttu-id="c0675-143">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="c0675-143">-SparkPoolName</span></span>
<span data-ttu-id="c0675-144">Name des Synapse Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="c0675-144">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkJobParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0675-145">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="c0675-145">-SparkPoolObject</span></span>
<span data-ttu-id="c0675-146">Spark pool input object, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="c0675-146">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: RunSparkJobByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0675-147">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c0675-147">-WorkspaceName</span></span>
<span data-ttu-id="c0675-148">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="c0675-148">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkJobParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0675-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c0675-149">-Confirm</span></span>
<span data-ttu-id="c0675-150">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c0675-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0675-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0675-151">-WhatIf</span></span>
<span data-ttu-id="c0675-152">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c0675-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0675-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0675-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0675-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0675-154">CommonParameters</span></span>
<span data-ttu-id="c0675-155">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0675-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0675-156">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0675-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0675-157">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c0675-157">INPUTS</span></span>

### <span data-ttu-id="c0675-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="c0675-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="c0675-159">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c0675-159">OUTPUTS</span></span>

### <span data-ttu-id="c0675-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="c0675-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="c0675-161">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c0675-161">NOTES</span></span>

## <span data-ttu-id="c0675-162">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c0675-162">RELATED LINKS</span></span>
