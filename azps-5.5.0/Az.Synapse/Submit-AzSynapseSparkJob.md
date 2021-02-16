---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/submit-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
ms.openlocfilehash: c8e710db383aae6698278ac4fb5ad7eb4344641b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174889"
---
# <span data-ttu-id="7f314-101">Submit-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="7f314-101">Submit-AzSynapseSparkJob</span></span>

## <span data-ttu-id="7f314-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f314-102">SYNOPSIS</span></span>
<span data-ttu-id="7f314-103">Übermittelt einen Synapse Analytics Spark-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="7f314-103">Submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="7f314-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f314-104">SYNTAX</span></span>

### <span data-ttu-id="7f314-105">RunSparkJobParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7f314-105">RunSparkJobParameterSetName (Default)</span></span>
```
Submit-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f314-106">RunSparkJobByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f314-106">RunSparkJobByParentObjectParameterSet</span></span>
```
Submit-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f314-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7f314-107">DESCRIPTION</span></span>
<span data-ttu-id="7f314-108">Das **Cmdlet "Submit-AzSynapseSparkJob"** übermittelt einen Synapse Analytics Spark-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="7f314-108">The **Submit-AzSynapseSparkJob** cmdlet submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="7f314-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7f314-109">EXAMPLES</span></span>

### <span data-ttu-id="7f314-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7f314-110">Example 1</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language Spark -Name WordCount_Java -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/wordcount.jar -MainClassName WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="7f314-111">Dieser Befehl übermittelt einen Synapse Analytics Spark-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="7f314-111">This command submits a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="7f314-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7f314-112">Example 2</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language SparkDotNet -Name WordCount_Dotnet -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/wordcount.zip -MainExecutableFile WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/result -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="7f314-113">Dieser Befehl übermittelt einen Synapse Analytics Spark.NET-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="7f314-113">This command submits a Synapse Analytics Spark .NET job.</span></span>

### <span data-ttu-id="7f314-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="7f314-114">Example 3</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language PySpark -Name WordCount_Python -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/wordcount.py -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="7f314-115">Dieser Befehl übermittelt einen Synapse Analytics PySpark-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="7f314-115">This command submits a Synapse Analytics PySpark job.</span></span>

## <span data-ttu-id="7f314-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f314-116">PARAMETERS</span></span>

### <span data-ttu-id="7f314-117">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="7f314-117">-CommandLineArgument</span></span>
<span data-ttu-id="7f314-118">Optionale Argumente für den Auftrag.</span><span class="sxs-lookup"><span data-stu-id="7f314-118">Optional arguments to the job.</span></span> <span data-ttu-id="7f314-119">z. B. "--Iteration 10000 --timeout 20s"</span><span class="sxs-lookup"><span data-stu-id="7f314-119">e.g. "--iteration 10000 --timeout 20s"</span></span>

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

### <span data-ttu-id="7f314-120">-Configuration</span><span class="sxs-lookup"><span data-stu-id="7f314-120">-Configuration</span></span>
<span data-ttu-id="7f314-121">Sparkkonfigurationseigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7f314-121">Spark configuration properties.</span></span>

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

### <span data-ttu-id="7f314-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f314-122">-DefaultProfile</span></span>
<span data-ttu-id="7f314-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7f314-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f314-124">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="7f314-124">-ExecutorCount</span></span>
<span data-ttu-id="7f314-125">Die Anzahl der Ausführungsgeber, die im angegebenen Sparkpool für den Auftrag zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7f314-125">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="7f314-126">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="7f314-126">-ExecutorSize</span></span>
<span data-ttu-id="7f314-127">Die Anzahl des Kerns und des Arbeitsspeichers, der für die Ausführungsgeber verwendet werden soll, die im angegebenen Sparkpool für den Auftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7f314-127">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="7f314-128">-Language</span><span class="sxs-lookup"><span data-stu-id="7f314-128">-Language</span></span>
<span data-ttu-id="7f314-129">Die Sprache des zu übermittelnden Auftrags.</span><span class="sxs-lookup"><span data-stu-id="7f314-129">Language of the job to submit.</span></span>

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

### <span data-ttu-id="7f314-130">-MainClassName</span><span class="sxs-lookup"><span data-stu-id="7f314-130">-MainClassName</span></span>
<span data-ttu-id="7f314-131">Der vollqualifizierte Bezeichner oder die Hauptklasse, die in der Hauptdefinitionsdatei enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="7f314-131">The fully-qualified identifier or the main class that is in the main definition file.</span></span>
<span data-ttu-id="7f314-132">Erforderlich für den Auftrag "Spark" und ".NET Spark".</span><span class="sxs-lookup"><span data-stu-id="7f314-132">Required for Spark and .NET Spark job.</span></span>
<span data-ttu-id="7f314-133">z. B. "org.apache.spark.examples.SparkPi"</span><span class="sxs-lookup"><span data-stu-id="7f314-133">e.g. "org.apache.spark.examples.SparkPi"</span></span>

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

### <span data-ttu-id="7f314-134">-MainDefinitionFile</span><span class="sxs-lookup"><span data-stu-id="7f314-134">-MainDefinitionFile</span></span>
<span data-ttu-id="7f314-135">Die für den Auftrag verwendete Hauptdatei.</span><span class="sxs-lookup"><span data-stu-id="7f314-135">The main file used for the job.</span></span>
<span data-ttu-id="7f314-136">z. B. " abfss://filesystem@account.dfs.core.windows.net/mySpark.jar "</span><span class="sxs-lookup"><span data-stu-id="7f314-136">e.g. "abfss://filesystem@account.dfs.core.windows.net/mySpark.jar"</span></span>

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

### <span data-ttu-id="7f314-137">-Name</span><span class="sxs-lookup"><span data-stu-id="7f314-137">-Name</span></span>
<span data-ttu-id="7f314-138">Name des Sparkauftrags.</span><span class="sxs-lookup"><span data-stu-id="7f314-138">Name of Spark job.</span></span>

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

### <span data-ttu-id="7f314-139">-ReferenceFile</span><span class="sxs-lookup"><span data-stu-id="7f314-139">-ReferenceFile</span></span>
<span data-ttu-id="7f314-140">Zusätzliche Dateien, die in der Hauptdefinitionsdatei als Referenz verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7f314-140">Additional files used for reference in the main definition file.</span></span> <span data-ttu-id="7f314-141">Durch Kommas getrennte Speicher-URI-Liste.</span><span class="sxs-lookup"><span data-stu-id="7f314-141">Comma-separated storage URI list.</span></span> <span data-ttu-id="7f314-142">z. B. " abfss://filesystem@account.dfs.core.windows.net/file1.txt , abfss://filesystem@account.dfs.core.windows.net/result/ "</span><span class="sxs-lookup"><span data-stu-id="7f314-142">e.g. "abfss://filesystem@account.dfs.core.windows.net/file1.txt,abfss://filesystem@account.dfs.core.windows.net/result/"</span></span>

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

### <span data-ttu-id="7f314-143">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="7f314-143">-SparkPoolName</span></span>
<span data-ttu-id="7f314-144">Name des Synapse Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="7f314-144">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="7f314-145">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="7f314-145">-SparkPoolObject</span></span>
<span data-ttu-id="7f314-146">Sparkpooleingabeobjekt, das normalerweise über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="7f314-146">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="7f314-147">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7f314-147">-WorkspaceName</span></span>
<span data-ttu-id="7f314-148">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="7f314-148">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7f314-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7f314-149">-Confirm</span></span>
<span data-ttu-id="7f314-150">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7f314-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f314-151">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7f314-151">-WhatIf</span></span>
<span data-ttu-id="7f314-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7f314-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7f314-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7f314-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f314-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f314-154">CommonParameters</span></span>
<span data-ttu-id="7f314-155">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f314-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f314-156">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f314-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f314-157">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7f314-157">INPUTS</span></span>

### <span data-ttu-id="7f314-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="7f314-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="7f314-159">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7f314-159">OUTPUTS</span></span>

### <span data-ttu-id="7f314-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="7f314-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="7f314-161">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7f314-161">NOTES</span></span>

## <span data-ttu-id="7f314-162">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7f314-162">RELATED LINKS</span></span>
