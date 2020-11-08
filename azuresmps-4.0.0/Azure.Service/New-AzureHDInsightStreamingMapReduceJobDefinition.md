---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 824F6302-6285-4AEC-A63C-E2519DE4C7CC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2597d66e87de682bbf5702085612f7338d75deac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006215"
---
# <span data-ttu-id="2e05e-101">New-AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="2e05e-101">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="2e05e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2e05e-102">SYNOPSIS</span></span>
<span data-ttu-id="2e05e-103">Definiert einen neuen Streaming-MapReduce-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="2e05e-103">Defines a new streaming MapReduce job.</span></span>

## <span data-ttu-id="2e05e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e05e-104">SYNTAX</span></span>

```
New-AzureHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-CmdEnv <String[]>]
 [-Combiner <String>] [-Defines <Hashtable>] [-Files <String[]>] [-InputPath <String>] [-JobName <String>]
 [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2e05e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2e05e-105">DESCRIPTION</span></span>
<span data-ttu-id="2e05e-106">Diese Version von Azure PowerShell-HDInsight ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="2e05e-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="2e05e-107">Diese Cmdlets werden vom 1. Januar 2017 entfernt.</span><span class="sxs-lookup"><span data-stu-id="2e05e-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="2e05e-108">Verwenden Sie bitte die neuere Version von Azure PowerShell-HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2e05e-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="2e05e-109">Informationen zum Verwenden des neuen HDInsight zum Erstellen eines Clusters finden Sie unter [Erstellen von Linux-basierten Clustern in HDInsight mithilfe von Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="2e05e-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="2e05e-110">Informationen zum Übermitteln von Aufträgen mithilfe von Azure PowerShell und anderen Ansätzen finden Sie unter über [Mitteln von Hadoop-Aufträgen in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="2e05e-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="2e05e-111">Referenzinformationen zu Azure PowerShell-HDInsight finden Sie unter [Azure HDInsight-Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2e05e-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="2e05e-112">Das Cmdlet **New-AzureHDInsightStreamingMapReduceJobDefinition** definiert ein neues Auftrags Definitionsobjekt, das die Parameter eines Hadoop-Streaming-Auftrags darstellt.</span><span class="sxs-lookup"><span data-stu-id="2e05e-112">The **New-AzureHDInsightStreamingMapReduceJobDefinition** cmdlet defines a new job definition object that represents the parameters of a Hadoop streaming job.</span></span>

## <span data-ttu-id="2e05e-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2e05e-113">EXAMPLES</span></span>

### <span data-ttu-id="2e05e-114">Beispiel 1: Erstellen einer Streaming-MapReduce-Auftragsdefinition</span><span class="sxs-lookup"><span data-stu-id="2e05e-114">Example 1: Create a streaming MapReduce job definition</span></span>
```
PS C:\>$StreamingWordCount = New-AzureHDInsightStreamingMapReduceJobDefinition -Files "/Example/Apps/WordCount.exe", "/Example/Apps/Cat.exe" -InputPath "/Example/Data/Gutenberg/Davinci.txt" -OutputPath "/Example/Data/StreamingOutput/WordCount.txt" -Mapper "Cat.exe" -Reducer "WordCount.exe"
```

<span data-ttu-id="2e05e-115">Dieser Befehl erstellt die angegebene Streaming MapReduce-Auftragsdefinition und speichert Sie dann in der $StreamingWordCount-Variablen.</span><span class="sxs-lookup"><span data-stu-id="2e05e-115">This command creates the specified streaming MapReduce job definition, and then stores it in the $StreamingWordCount variable.</span></span>

## <span data-ttu-id="2e05e-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e05e-116">PARAMETERS</span></span>

### <span data-ttu-id="2e05e-117">-Argumente</span><span class="sxs-lookup"><span data-stu-id="2e05e-117">-Arguments</span></span>
<span data-ttu-id="2e05e-118">Gibt ein Array von Argumenten für einen Hadoop-Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="2e05e-118">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="2e05e-119">Die Argumente werden als Befehlszeilenargumente an jede Aufgabe übergeben.</span><span class="sxs-lookup"><span data-stu-id="2e05e-119">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Args

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e05e-120">-CmdEnv</span><span class="sxs-lookup"><span data-stu-id="2e05e-120">-CmdEnv</span></span>
<span data-ttu-id="2e05e-121">Gibt ein Array mit Befehlszeilen Umgebungsvariablen an, die festgelegt werden sollen, wenn ein Auftrag auf Datenknoten ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2e05e-121">Specifies an array of command-line environment variables to set when a job runs on data nodes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e05e-122">-Combiner</span><span class="sxs-lookup"><span data-stu-id="2e05e-122">-Combiner</span></span>
<span data-ttu-id="2e05e-123">Gibt einen Combiner-Dateinamen an.</span><span class="sxs-lookup"><span data-stu-id="2e05e-123">Specifies a Combiner file name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e05e-124">– Definiert</span><span class="sxs-lookup"><span data-stu-id="2e05e-124">-Defines</span></span>
<span data-ttu-id="2e05e-125">Gibt Hadoop-Konfigurationswerte an, die beim Ausführen des Auftrags festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2e05e-125">Specifies Hadoop configuration values to set when the job runs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Params

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e05e-126">-Dateien</span><span class="sxs-lookup"><span data-stu-id="2e05e-126">-Files</span></span>
<span data-ttu-id="2e05e-127">Gibt ein Array von Dateien an, die für einen Auftrag erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="2e05e-127">Specifies an array of files that are required for a job.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e05e-128">-InputPath</span><span class="sxs-lookup"><span data-stu-id="2e05e-128">-InputPath</span></span>
<span data-ttu-id="2e05e-129">Gibt den WASB-Pfad zu den Eingabedateien an.</span><span class="sxs-lookup"><span data-stu-id="2e05e-129">Specifies the WASB path to the input files.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Input

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e05e-130">-Jobname</span><span class="sxs-lookup"><span data-stu-id="2e05e-130">-JobName</span></span>
<span data-ttu-id="2e05e-131">Gibt den Namen der neuen MapReduce-Auftragsdefinition an.</span><span class="sxs-lookup"><span data-stu-id="2e05e-131">Specifies the name of the new MapReduce job definition.</span></span>
<span data-ttu-id="2e05e-132">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="2e05e-132">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e05e-133">-Mapper</span><span class="sxs-lookup"><span data-stu-id="2e05e-133">-Mapper</span></span>
<span data-ttu-id="2e05e-134">Gibt einen Mapper-Dateinamen an.</span><span class="sxs-lookup"><span data-stu-id="2e05e-134">Specifies a Mapper file name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e05e-135">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="2e05e-135">-OutputPath</span></span>
<span data-ttu-id="2e05e-136">Gibt den WASB-Pfad für die Auftragsausgabe an.</span><span class="sxs-lookup"><span data-stu-id="2e05e-136">Specifies the WASB path for the job output.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Output

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e05e-137">-Profil</span><span class="sxs-lookup"><span data-stu-id="2e05e-137">-Profile</span></span>
<span data-ttu-id="2e05e-138">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="2e05e-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2e05e-139">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="2e05e-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e05e-140">-Reduzierstück</span><span class="sxs-lookup"><span data-stu-id="2e05e-140">-Reducer</span></span>
<span data-ttu-id="2e05e-141">Gibt einen Reduzierer-Dateinamen an.</span><span class="sxs-lookup"><span data-stu-id="2e05e-141">Specifies a Reducer file name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e05e-142">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="2e05e-142">-StatusFolder</span></span>
<span data-ttu-id="2e05e-143">Gibt den Ordner an, der die Standardausgaben und Fehlerausgaben für den Auftrag enthält, einschließlich des Exit-Codes und der Aufgaben Protokolle.</span><span class="sxs-lookup"><span data-stu-id="2e05e-143">Specifies the folder that contains the standard outputs and error outputs for the job, including its exit code and task logs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e05e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e05e-144">CommonParameters</span></span>
<span data-ttu-id="2e05e-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e05e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e05e-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e05e-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e05e-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2e05e-147">INPUTS</span></span>

## <span data-ttu-id="2e05e-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2e05e-148">OUTPUTS</span></span>

## <span data-ttu-id="2e05e-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="2e05e-149">NOTES</span></span>

## <span data-ttu-id="2e05e-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2e05e-150">RELATED LINKS</span></span>

[<span data-ttu-id="2e05e-151">Neu – AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="2e05e-151">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="2e05e-152">Neu – AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="2e05e-152">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="2e05e-153">Neu – AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="2e05e-153">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="2e05e-154">Neu – AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="2e05e-154">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)


