---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 0B194605-F6B2-4FBC-ABF8-E49876EC7CFD
online version: ''
schema: 2.0.0
ms.openlocfilehash: b215cfa95c20a2e8d13cfefa9e2ef0b3794a6727
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005846"
---
# <span data-ttu-id="2822e-101">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="2822e-101">Get-AzureHDInsightJobOutput</span></span>

## <span data-ttu-id="2822e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2822e-102">SYNOPSIS</span></span>
<span data-ttu-id="2822e-103">Ruft die Protokollausgabe für einen Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="2822e-103">Gets the log output for a job.</span></span>

## <span data-ttu-id="2822e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2822e-104">SYNTAX</span></span>

```
Get-AzureHDInsightJobOutput [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-DownloadTaskLogs] [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobId <String> [-StandardError]
 [-StandardOutput] [-Subscription <String>] [-TaskLogsDirectory <String>] [-TaskSummary]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2822e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2822e-105">DESCRIPTION</span></span>
<span data-ttu-id="2822e-106">Diese Version von Azure PowerShell-HDInsight ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="2822e-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="2822e-107">Diese Cmdlets werden vom 1. Januar 2017 entfernt.</span><span class="sxs-lookup"><span data-stu-id="2822e-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="2822e-108">Verwenden Sie bitte die neuere Version von Azure PowerShell-HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2822e-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="2822e-109">Informationen zum Verwenden des neuen HDInsight zum Erstellen eines Clusters finden Sie unter Erstellen von Linux-basierten Clustern in [HDInsight mithilfe von Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span><span class="sxs-lookup"><span data-stu-id="2822e-109">For information about how to use the new HDInsight to create a cluster, see Create Linux-based clusters in [HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="2822e-110">Informationen zum Übermitteln von Aufträgen mithilfe von Azure PowerShell und anderen Ansätzen finden Sie unter über [Mitteln von Hadoop-Aufträgen in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span><span class="sxs-lookup"><span data-stu-id="2822e-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="2822e-111">Referenzinformationen zu Azure PowerShell-HDInsight finden Sie unter [Azure HDInsight-Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span><span class="sxs-lookup"><span data-stu-id="2822e-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="2822e-112">Das Cmdlet " **Get-AzureHDInsightJobOutput** " Ruft die Protokollausgabe für einen Auftrag aus dem Speicherkonto ab, das einem Cluster zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2822e-112">The **Get-AzureHDInsightJobOutput** cmdlet gets the log output for a job from the storage account associated with a cluster.</span></span>
<span data-ttu-id="2822e-113">Sie können verschiedene Arten von Auftragsprotokollen abrufen, darunter Standardausgabe, Standardfehler, Vorgangsprotokolle und eine Zusammenfassung der Vorgangsprotokolle.</span><span class="sxs-lookup"><span data-stu-id="2822e-113">You can get various types of job logs including standard output, standard error, task logs, and a summary of the task logs.</span></span>

## <span data-ttu-id="2822e-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2822e-114">EXAMPLES</span></span>

### <span data-ttu-id="2822e-115">Beispiel 1: Abrufen der Auftragsausgabe</span><span class="sxs-lookup"><span data-stu-id="2822e-115">Example 1: Get job output</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "MyCluster"
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" $WordCountJob
    | Start-AzureHDInsightJob -Subscription $SubId -Cluster $ClusterName
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -StandardError
```

<span data-ttu-id="2822e-116">Der erste Befehl ruft die ID des aktuellen Abonnements ab und speichert ihn dann in der $SubId-Variablen.</span><span class="sxs-lookup"><span data-stu-id="2822e-116">The first command gets the ID of the current subscription, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="2822e-117">Der zweite Befehl speichert den Namen mycluster in der $Clustername-Variablen.</span><span class="sxs-lookup"><span data-stu-id="2822e-117">The second command stores the name MyCluster in the $Clustername variable.</span></span>

<span data-ttu-id="2822e-118">Der dritte Befehl erstellt eine MapReduce-Auftragsdefinition und speichert Sie dann in der $WordCountJob-Variablen.</span><span class="sxs-lookup"><span data-stu-id="2822e-118">The third command creates a MapReduce job definition, and then stores it in the $WordCountJob variable.</span></span>
<span data-ttu-id="2822e-119">Der Befehl übergibt den Auftrag in $WordCountJob an das Cmdlet **Start-AzureHDInsightJob** , um den Auftrag zu starten.</span><span class="sxs-lookup"><span data-stu-id="2822e-119">The command passes the job in $WordCountJob to the **Start-AzureHDInsightJob** cmdlet to start the job.</span></span>
<span data-ttu-id="2822e-120">Es übergibt auch $WordCountJob an das **Wait-AzureHDInsightJob-** Cmdlet, um auf den Abschluss des Auftrags zu warten, und dann wird **Get-AzureHDInsightJobOutput** verwendet, um die Ausgabe des Auftrags abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2822e-120">It also passes $WordCountJob to the **Wait-AzureHDInsightJob** cmdlet to wait for the job to finish, and then it uses **Get-AzureHDInsightJobOutput** to get the job output.</span></span>

## <span data-ttu-id="2822e-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="2822e-121">PARAMETERS</span></span>

### <span data-ttu-id="2822e-122">-Zertifikat</span><span class="sxs-lookup"><span data-stu-id="2822e-122">-Certificate</span></span>
<span data-ttu-id="2822e-123">Gibt das Verwaltungszertifikat für ein Azure-Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="2822e-123">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: (All)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2822e-124">-Cluster</span><span class="sxs-lookup"><span data-stu-id="2822e-124">-Cluster</span></span>
<span data-ttu-id="2822e-125">Gibt einen Cluster an.</span><span class="sxs-lookup"><span data-stu-id="2822e-125">Specifies a cluster.</span></span>
<span data-ttu-id="2822e-126">Dieses Cmdlet ruft Auftragsprotokolle aus dem Cluster ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="2822e-126">This cmdlet gets job logs from the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2822e-127">-DownloadTaskLogs</span><span class="sxs-lookup"><span data-stu-id="2822e-127">-DownloadTaskLogs</span></span>
<span data-ttu-id="2822e-128">Gibt an, dass dieses Cmdlet die Vorgangsprotokolle für einen Auftrag abruft.</span><span class="sxs-lookup"><span data-stu-id="2822e-128">Indicates that this cmdlet gets the task logs for a job.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2822e-129">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="2822e-129">-Endpoint</span></span>
<span data-ttu-id="2822e-130">Gibt den Endpunkt an, mit dem eine Verbindung mit Azure hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2822e-130">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="2822e-131">Wenn Sie diesen Parameter nicht angeben, verwendet dieses Cmdlet den Standardendpunkt.</span><span class="sxs-lookup"><span data-stu-id="2822e-131">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2822e-132">-HostedService</span><span class="sxs-lookup"><span data-stu-id="2822e-132">-HostedService</span></span>
<span data-ttu-id="2822e-133">Gibt den Namespace eines HDInsight-Diensts an, wenn Sie den Standardnamespace nicht verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="2822e-133">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2822e-134">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="2822e-134">-IgnoreSslErrors</span></span>
<span data-ttu-id="2822e-135">Gibt an, ob SSL-Fehler (Secure Sockets Layer) ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="2822e-135">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2822e-136">-JobId</span><span class="sxs-lookup"><span data-stu-id="2822e-136">-JobId</span></span>
<span data-ttu-id="2822e-137">Gibt die ID des abzurufenden Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="2822e-137">Specifies the ID of the job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2822e-138">-Profil</span><span class="sxs-lookup"><span data-stu-id="2822e-138">-Profile</span></span>
<span data-ttu-id="2822e-139">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="2822e-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2822e-140">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="2822e-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2822e-141">-StandardError</span><span class="sxs-lookup"><span data-stu-id="2822e-141">-StandardError</span></span>
<span data-ttu-id="2822e-142">Gibt an, dass dieses Cmdlet die StdErr-Ausgabe eines Auftrags abruft.</span><span class="sxs-lookup"><span data-stu-id="2822e-142">Indicates that this cmdlet gets the StdErr output of a job.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2822e-143">-StandardOutput</span><span class="sxs-lookup"><span data-stu-id="2822e-143">-StandardOutput</span></span>
<span data-ttu-id="2822e-144">Gibt an, dass dieses Cmdlet die SdtOut-Ausgabe eines Auftrags abruft.</span><span class="sxs-lookup"><span data-stu-id="2822e-144">Indicates that this cmdlet gets the SdtOut output of a job.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2822e-145">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="2822e-145">-Subscription</span></span>
<span data-ttu-id="2822e-146">Gibt das Abonnement an, das den abzurufenden HDInsight-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="2822e-146">Specifies the subscription that contains the HDInsight cluster to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2822e-147">-TaskLogsDirectory</span><span class="sxs-lookup"><span data-stu-id="2822e-147">-TaskLogsDirectory</span></span>
<span data-ttu-id="2822e-148">Gibt einen lokalen Ordner an, in dem Aufgaben Protokolle gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="2822e-148">Specifies a local folder in which to store tasks logs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: LogsDir

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2822e-149">-TaskSummary</span><span class="sxs-lookup"><span data-stu-id="2822e-149">-TaskSummary</span></span>
<span data-ttu-id="2822e-150">Gibt an, dass diese Cmdlets die Zusammenfassung des Vorgangs Protokolls abrufen.</span><span class="sxs-lookup"><span data-stu-id="2822e-150">Indicates that this cmdlets gets the task log summary.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2822e-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2822e-151">CommonParameters</span></span>
<span data-ttu-id="2822e-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2822e-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2822e-153">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2822e-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2822e-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2822e-154">INPUTS</span></span>

## <span data-ttu-id="2822e-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2822e-155">OUTPUTS</span></span>

## <span data-ttu-id="2822e-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="2822e-156">NOTES</span></span>

## <span data-ttu-id="2822e-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2822e-157">RELATED LINKS</span></span>

[<span data-ttu-id="2822e-158">Neu – AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="2822e-158">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="2822e-159">Anfang-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2822e-159">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="2822e-160">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2822e-160">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)
