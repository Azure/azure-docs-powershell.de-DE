---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: A8953045-3836-4C5A-96F8-461CB1DB6BBD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 58958a6bedd29cd55535fe879fab813a430ff20b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006122"
---
# <span data-ttu-id="70105-101">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="70105-101">New-AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="70105-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="70105-102">SYNOPSIS</span></span>
<span data-ttu-id="70105-103">Definiert einen neuen MapReduce-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="70105-103">Defines a new MapReduce job.</span></span>

## <span data-ttu-id="70105-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="70105-104">SYNTAX</span></span>

```
New-AzureHDInsightMapReduceJobDefinition [-Arguments <String[]>] -ClassName <String> [-Defines <Hashtable>]
 [-Files <String[]>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="70105-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="70105-105">DESCRIPTION</span></span>
<span data-ttu-id="70105-106">Diese Version von Azure PowerShell-HDInsight ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="70105-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="70105-107">Diese Cmdlets werden vom 1. Januar 2017 entfernt.</span><span class="sxs-lookup"><span data-stu-id="70105-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="70105-108">Verwenden Sie bitte die neuere Version von Azure PowerShell-HDInsight.</span><span class="sxs-lookup"><span data-stu-id="70105-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="70105-109">Informationen zum Verwenden des neuen HDInsight zum Erstellen eines Clusters finden Sie unter [Erstellen von Linux-basierten Clustern in HDInsight mithilfe von Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="70105-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="70105-110">Informationen zum Übermitteln von Aufträgen mithilfe von Azure PowerShell und anderen Ansätzen finden Sie unter über [Mitteln von Hadoop-Aufträgen in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="70105-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="70105-111">Referenzinformationen zu Azure PowerShell-HDInsight finden Sie unter [Azure HDInsight-Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="70105-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="70105-112">Das Cmdlet **New-AzureHDInsightMapReduceJobDefinition** definiert einen neuen MapReduce-Auftrag, der auf einem Azure HDInsight-Cluster ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="70105-112">The **New-AzureHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job to run on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="70105-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="70105-113">EXAMPLES</span></span>

### <span data-ttu-id="70105-114">Beispiel 1: Definieren eines MapReduce-Auftrags, Ausführen des Auftrags und Abrufen der Ausgabe</span><span class="sxs-lookup"><span data-stu-id="70105-114">Example 1: Define a MapReduce job, run the job, and get the output</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "MyCluster" 
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "WordCount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:\> $WordCountJob | Start-AzureHDInsightJob -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

<span data-ttu-id="70105-115">Der erste Befehl ruft die ID des aktuellen Abonnements ab und speichert ihn dann in der $SubId-Variablen.</span><span class="sxs-lookup"><span data-stu-id="70105-115">The first command gets the ID of the current subscription, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="70105-116">Der zweite Befehl weist den Namen mycluster der $Clustername-Variablen zu.</span><span class="sxs-lookup"><span data-stu-id="70105-116">The second command assigns the name MyCluster to the $Clustername variable.</span></span>

<span data-ttu-id="70105-117">Der dritte Befehl verwendet das Cmdlet **New-AzureHDInsightMapReduceJobDefinition** , um eine MapReduce-Auftragsdefinition zu erstellen und diese dann in der $WordCountJob-Variable zu speichern.</span><span class="sxs-lookup"><span data-stu-id="70105-117">The third command uses the **New-AzureHDInsightMapReduceJobDefinition** cmdlet to create a MapReduce job definition, and then store it in the $WordCountJob variable.</span></span>

<span data-ttu-id="70105-118">Der vierte Befehl führt eine Abfolge von Vorgängen mithilfe dieser Cmdlets aus:</span><span class="sxs-lookup"><span data-stu-id="70105-118">The fourth command performs a sequence of operations by using these cmdlets:</span></span> 

- <span data-ttu-id="70105-119">**Start-AzureHDInsightJob** , um den Auftrag auf $Clustername zu starten.</span><span class="sxs-lookup"><span data-stu-id="70105-119">**Start-AzureHDInsightJob** to start the job on $ClusterName.</span></span> 
- <span data-ttu-id="70105-120">**Warten** Sie, bis der Vorgang abgeschlossen ist, und zeigen Sie den Fortschritt in Richtung AzureHDInsightJob an.</span><span class="sxs-lookup"><span data-stu-id="70105-120">**Wait-AzureHDInsightJob** to wait for the job to finish and to display the progress toward completion.</span></span>
- <span data-ttu-id="70105-121">**Get-AzureHDInsightJobOutput** , um die Ausgabe des Auftrags zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="70105-121">**Get-AzureHDInsightJobOutput** to get the job output.</span></span>

## <span data-ttu-id="70105-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="70105-122">PARAMETERS</span></span>

### <span data-ttu-id="70105-123">-Argumente</span><span class="sxs-lookup"><span data-stu-id="70105-123">-Arguments</span></span>
<span data-ttu-id="70105-124">Gibt ein Array von Argumenten für einen Hadoop-Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="70105-124">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="70105-125">Die Argumente werden als Befehlszeilenargumente an jede Aufgabe übergeben.</span><span class="sxs-lookup"><span data-stu-id="70105-125">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="70105-126">-ClassName</span><span class="sxs-lookup"><span data-stu-id="70105-126">-ClassName</span></span>
<span data-ttu-id="70105-127">Gibt den Namen der Auftragsklasse in der Java-Archivdatei (jar) an.</span><span class="sxs-lookup"><span data-stu-id="70105-127">Specifies the name of the job class in the Java Archive (JAR) file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Class

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70105-128">– Definiert</span><span class="sxs-lookup"><span data-stu-id="70105-128">-Defines</span></span>
<span data-ttu-id="70105-129">Gibt Hadoop-Konfigurationswerte an, die beim Ausführen des Auftrags festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="70105-129">Specifies Hadoop configuration values to set when the job runs.</span></span>

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

### <span data-ttu-id="70105-130">-Dateien</span><span class="sxs-lookup"><span data-stu-id="70105-130">-Files</span></span>
<span data-ttu-id="70105-131">Gibt ein Array von WASB-Dateien an, die für einen Auftrag erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="70105-131">Specifies an array of WASB files that are required for a job.</span></span>

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

### <span data-ttu-id="70105-132">-JarFile</span><span class="sxs-lookup"><span data-stu-id="70105-132">-JarFile</span></span>
<span data-ttu-id="70105-133">Gibt den vollqualifizierten Namen einer JAR-Datei an, die den Code und die Abhängigkeiten eines MapReduce-Auftrags enthält.</span><span class="sxs-lookup"><span data-stu-id="70105-133">Specifies the fully qualified name of a JAR file that contains the code and dependencies of a MapReduce job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Jar

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70105-134">-Jobname</span><span class="sxs-lookup"><span data-stu-id="70105-134">-JobName</span></span>
<span data-ttu-id="70105-135">Gibt den Namen eines MapReduce-Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="70105-135">Specifies the name of a MapReduce job.</span></span>
<span data-ttu-id="70105-136">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="70105-136">This parameter is optional.</span></span>
<span data-ttu-id="70105-137">Wenn Sie diesen Parameter nicht angeben, wird der Wert des *className* -Parameters verwendet.</span><span class="sxs-lookup"><span data-stu-id="70105-137">If you do not specify this parameter, the value of the *ClassName* parameter is used.</span></span>

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

### <span data-ttu-id="70105-138">-Libjar</span><span class="sxs-lookup"><span data-stu-id="70105-138">-LibJars</span></span>
<span data-ttu-id="70105-139">Gibt ein Array von LibJar-verweisen des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="70105-139">Specifies an array of LibJar references of the job.</span></span>

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

### <span data-ttu-id="70105-140">-Profil</span><span class="sxs-lookup"><span data-stu-id="70105-140">-Profile</span></span>
<span data-ttu-id="70105-141">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="70105-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="70105-142">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="70105-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="70105-143">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="70105-143">-StatusFolder</span></span>
<span data-ttu-id="70105-144">Gibt den Speicherort des Ordners an, der Standardausgaben und Fehlerausgaben für einen Auftrag enthält, einschließlich des Exit-Codes und der Aufgaben Protokolle.</span><span class="sxs-lookup"><span data-stu-id="70105-144">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="70105-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70105-145">CommonParameters</span></span>
<span data-ttu-id="70105-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70105-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70105-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70105-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70105-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="70105-148">INPUTS</span></span>

## <span data-ttu-id="70105-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="70105-149">OUTPUTS</span></span>

## <span data-ttu-id="70105-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="70105-150">NOTES</span></span>

## <span data-ttu-id="70105-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="70105-151">RELATED LINKS</span></span>

[<span data-ttu-id="70105-152">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="70105-152">Get-AzureHDInsightJobOutput</span></span>](./Get-AzureHDInsightJobOutput.md)

[<span data-ttu-id="70105-153">Neu – AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="70105-153">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="70105-154">Neu – AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="70105-154">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="70105-155">Neu – AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="70105-155">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)

[<span data-ttu-id="70105-156">Anfang-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="70105-156">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="70105-157">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="70105-157">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


