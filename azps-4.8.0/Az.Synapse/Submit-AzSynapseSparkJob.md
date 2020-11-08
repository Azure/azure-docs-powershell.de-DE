---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/submit-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
ms.openlocfilehash: c8e710db383aae6698278ac4fb5ad7eb4344641b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165421"
---
# <span data-ttu-id="0ebeb-101">Submit-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="0ebeb-101">Submit-AzSynapseSparkJob</span></span>

## <span data-ttu-id="0ebeb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0ebeb-102">SYNOPSIS</span></span>
<span data-ttu-id="0ebeb-103">Sendet einen Synapse Analytics Spark-Job.</span><span class="sxs-lookup"><span data-stu-id="0ebeb-103">Submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="0ebeb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ebeb-104">SYNTAX</span></span>

### <span data-ttu-id="0ebeb-105">RunSparkJobParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="0ebeb-105">RunSparkJobParameterSetName (Default)</span></span>
```
Submit-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ebeb-106">RunSparkJobByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ebeb-106">RunSparkJobByParentObjectParameterSet</span></span>
```
Submit-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ebeb-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ebeb-107">DESCRIPTION</span></span>
<span data-ttu-id="0ebeb-108">Das Cmdlet **Submit-AzSynapseSparkJob** sendet einen Synapse Analytics Spark-Job.</span><span class="sxs-lookup"><span data-stu-id="0ebeb-108">The **Submit-AzSynapseSparkJob** cmdlet submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="0ebeb-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0ebeb-109">EXAMPLES</span></span>

### <span data-ttu-id="0ebeb-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0ebeb-110">Example 1</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language Spark -Name WordCount_Java -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/wordcount.jar -MainClassName WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="0ebeb-111">Dieser Befehl sendet einen Synapse Analytics Spark-Job.</span><span class="sxs-lookup"><span data-stu-id="0ebeb-111">This command submits a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="0ebeb-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0ebeb-112">Example 2</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language SparkDotNet -Name WordCount_Dotnet -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/wordcount.zip -MainExecutableFile WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/result -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="0ebeb-113">Mit diesem Befehl wird ein Synapse Analytics Spark .net-Auftrag übermittelt.</span><span class="sxs-lookup"><span data-stu-id="0ebeb-113">This command submits a Synapse Analytics Spark .NET job.</span></span>

### <span data-ttu-id="0ebeb-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="0ebeb-114">Example 3</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language PySpark -Name WordCount_Python -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/wordcount.py -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="0ebeb-115">Dieser Befehl übermittelt einen Synapse Analytics-Job.</span><span class="sxs-lookup"><span data-stu-id="0ebeb-115">This command submits a Synapse Analytics PySpark job.</span></span>

## <span data-ttu-id="0ebeb-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ebeb-116">PARAMETERS</span></span>

### <span data-ttu-id="0ebeb-117">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="0ebeb-117">-CommandLineArgument</span></span>
<span data-ttu-id="0ebeb-118">Optionale Argumente für den Auftrag.</span><span class="sxs-lookup"><span data-stu-id="0ebeb-118">Optional arguments to the job.</span></span> <span data-ttu-id="0ebeb-119">beispielsweise "--Iteration 10000--Timeout 20er"</span><span class="sxs-lookup"><span data-stu-id="0ebeb-119">e.g. "--iteration 10000 --timeout 20s"</span></span>

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

### <span data-ttu-id="0ebeb-120">-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="0ebeb-120">-Configuration</span></span>
<span data-ttu-id="0ebeb-121">Spark-Konfigurationseigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0ebeb-121">Spark configuration properties.</span></span>

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

### <span data-ttu-id="0ebeb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ebeb-122">-DefaultProfile</span></span>
<span data-ttu-id="0ebeb-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0ebeb-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ebeb-124">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="0ebeb-124">-ExecutorCount</span></span>
<span data-ttu-id="0ebeb-125">Die Anzahl der Executors, die im angegebenen Spark-Pool für den Auftrag zugewiesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0ebeb-125">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="0ebeb-126">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="0ebeb-126">-ExecutorSize</span></span>
<span data-ttu-id="0ebeb-127">Die Anzahl des Kerns und des Arbeitsspeichers, der für Executors verwendet werden soll, die im angegebenen Spark Pool für den Auftrag reserviert sind.</span><span class="sxs-lookup"><span data-stu-id="0ebeb-127">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="0ebeb-128">– Sprache</span><span class="sxs-lookup"><span data-stu-id="0ebeb-128">-Language</span></span>
<span data-ttu-id="0ebeb-129">Die Sprache des zu übermittelnden Auftrags.</span><span class="sxs-lookup"><span data-stu-id="0ebeb-129">Language of the job to submit.</span></span>

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

### <span data-ttu-id="0ebeb-130">-MainClassName</span><span class="sxs-lookup"><span data-stu-id="0ebeb-130">-MainClassName</span></span>
<span data-ttu-id="0ebeb-131">Der vollqualifizierte Bezeichner oder die Hauptklasse, die sich in der Haupt Definitionsdatei befindet.</span><span class="sxs-lookup"><span data-stu-id="0ebeb-131">The fully-qualified identifier or the main class that is in the main definition file.</span></span>
<span data-ttu-id="0ebeb-132">Erforderlich für Spark und .net Spark Job.</span><span class="sxs-lookup"><span data-stu-id="0ebeb-132">Required for Spark and .NET Spark job.</span></span>
<span data-ttu-id="0ebeb-133">beispielsweise "org. Apache. Spark. examples. SparkPi"</span><span class="sxs-lookup"><span data-stu-id="0ebeb-133">e.g. "org.apache.spark.examples.SparkPi"</span></span>

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

### <span data-ttu-id="0ebeb-134">-MainDefinitionFile</span><span class="sxs-lookup"><span data-stu-id="0ebeb-134">-MainDefinitionFile</span></span>
<span data-ttu-id="0ebeb-135">Die Hauptdatei für den Auftrag.</span><span class="sxs-lookup"><span data-stu-id="0ebeb-135">The main file used for the job.</span></span>
<span data-ttu-id="0ebeb-136">beispielsweise " abfss://filesystem@account.dfs.core.windows.net/mySpark.jar "</span><span class="sxs-lookup"><span data-stu-id="0ebeb-136">e.g. "abfss://filesystem@account.dfs.core.windows.net/mySpark.jar"</span></span>

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

### <span data-ttu-id="0ebeb-137">-Name</span><span class="sxs-lookup"><span data-stu-id="0ebeb-137">-Name</span></span>
<span data-ttu-id="0ebeb-138">Name des Spark-Auftrags.</span><span class="sxs-lookup"><span data-stu-id="0ebeb-138">Name of Spark job.</span></span>

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

### <span data-ttu-id="0ebeb-139">-Referenzdatei</span><span class="sxs-lookup"><span data-stu-id="0ebeb-139">-ReferenceFile</span></span>
<span data-ttu-id="0ebeb-140">Zusätzliche Dateien, die als Referenz in der Haupt Definitionsdatei verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0ebeb-140">Additional files used for reference in the main definition file.</span></span> <span data-ttu-id="0ebeb-141">Durch Kommas getrennte Speicher-URI-Liste.</span><span class="sxs-lookup"><span data-stu-id="0ebeb-141">Comma-separated storage URI list.</span></span> <span data-ttu-id="0ebeb-142">beispielsweise " abfss://filesystem@account.dfs.core.windows.net/file1.txt , abfss://filesystem@account.dfs.core.windows.net/result/ "</span><span class="sxs-lookup"><span data-stu-id="0ebeb-142">e.g. "abfss://filesystem@account.dfs.core.windows.net/file1.txt,abfss://filesystem@account.dfs.core.windows.net/result/"</span></span>

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

### <span data-ttu-id="0ebeb-143">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="0ebeb-143">-SparkPoolName</span></span>
<span data-ttu-id="0ebeb-144">Name des Synapsen-Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="0ebeb-144">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="0ebeb-145">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="0ebeb-145">-SparkPoolObject</span></span>
<span data-ttu-id="0ebeb-146">Spark Pool-Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="0ebeb-146">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0ebeb-147">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0ebeb-147">-WorkspaceName</span></span>
<span data-ttu-id="0ebeb-148">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="0ebeb-148">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="0ebeb-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0ebeb-149">-Confirm</span></span>
<span data-ttu-id="0ebeb-150">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0ebeb-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ebeb-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ebeb-151">-WhatIf</span></span>
<span data-ttu-id="0ebeb-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0ebeb-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ebeb-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0ebeb-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ebeb-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ebeb-154">CommonParameters</span></span>
<span data-ttu-id="0ebeb-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ebeb-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ebeb-156">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ebeb-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ebeb-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0ebeb-157">INPUTS</span></span>

### <span data-ttu-id="0ebeb-158">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="0ebeb-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="0ebeb-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0ebeb-159">OUTPUTS</span></span>

### <span data-ttu-id="0ebeb-160">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="0ebeb-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="0ebeb-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="0ebeb-161">NOTES</span></span>

## <span data-ttu-id="0ebeb-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0ebeb-162">RELATED LINKS</span></span>
