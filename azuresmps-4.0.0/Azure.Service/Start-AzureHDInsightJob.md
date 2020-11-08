---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 60A5ACF7-2637-4BDC-BF41-80E81B23F4CD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0308c3ff5bee358a82d74d452784f42c69bc7c32
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005630"
---
# <span data-ttu-id="82037-101">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="82037-101">Start-AzureHDInsightJob</span></span>

## <span data-ttu-id="82037-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="82037-102">SYNOPSIS</span></span>
<span data-ttu-id="82037-103">Startet einen HDInsight-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="82037-103">Starts an HDInsight job.</span></span>

## <span data-ttu-id="82037-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="82037-104">SYNTAX</span></span>

### <span data-ttu-id="82037-105">Starten von Tabelle Jobdetails auf einem HDInsight-Cluster (Standard)</span><span class="sxs-lookup"><span data-stu-id="82037-105">Start jobDetails on an HDInsight Cluster (Default)</span></span>
```
Start-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>]
 -JobDefinition <AzureHDInsightJobDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="82037-106">Starten von Tabelle Jobdetails auf einem HDInsight-Cluster (mit bestimmten Anmeldeinformationen für Abonnements)</span><span class="sxs-lookup"><span data-stu-id="82037-106">Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Start-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobDefinition <AzureHDInsightJobDefinition>
 [-Subscription <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="82037-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="82037-107">DESCRIPTION</span></span>
<span data-ttu-id="82037-108">Diese Version von Azure PowerShell-HDInsight ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="82037-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="82037-109">Diese Cmdlets werden vom 1. Januar 2017 entfernt.</span><span class="sxs-lookup"><span data-stu-id="82037-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="82037-110">Verwenden Sie bitte die neuere Version von Azure PowerShell-HDInsight.</span><span class="sxs-lookup"><span data-stu-id="82037-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="82037-111">Informationen zum Verwenden des neuen HDInsight zum Erstellen eines Clusters finden Sie unter [Erstellen von Linux-basierten Clustern in HDInsight mithilfe von Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="82037-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="82037-112">Informationen zum Übermitteln von Aufträgen mithilfe von Azure PowerShell und anderen Ansätzen finden Sie unter über [Mitteln von Hadoop-Aufträgen in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="82037-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="82037-113">Referenzinformationen zu Azure PowerShell-HDInsight finden Sie unter [Azure HDInsight-Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="82037-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="82037-114">Mit dem Cmdlet **Start-AzureHDInsightJob** wird ein definierter Azure HDInsight-Auftrag in einem angegebenen Cluster gestartet.</span><span class="sxs-lookup"><span data-stu-id="82037-114">The **Start-AzureHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="82037-115">Der zu startende Job kann ein MapReduce-Job, ein Streaming-Job, ein Hive-Job oder ein Pig-Job sein.</span><span class="sxs-lookup"><span data-stu-id="82037-115">The job to start can be a MapReduce job, a streaming job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="82037-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="82037-116">EXAMPLES</span></span>

### <span data-ttu-id="82037-117">Beispiel 1: Starten eines HDInsight-Auftrags</span><span class="sxs-lookup"><span data-stu-id="82037-117">Example 1: Start an HDInsight job</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "Cluster01" 
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:\> $WordCountJob | Start-AzureHDInsightJob -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

<span data-ttu-id="82037-118">Der erste Befehl ruft die aktuelle Abonnement-ID ab und speichert Sie dann in der $SubId-Variablen.</span><span class="sxs-lookup"><span data-stu-id="82037-118">The first command gets the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="82037-119">Der zweite Befehl weist den Namen Cluster01 der $Clustername Variablen zu.</span><span class="sxs-lookup"><span data-stu-id="82037-119">The second command assigns the name Cluster01 to the $ClusterName variable.</span></span>

<span data-ttu-id="82037-120">Der dritte Befehl verwendet das Cmdlet **New-AzureHDInsightMapReduceJobDefinition** , um eine MapReduce-Auftragsdefinition zu erstellen, und speichert Sie dann in der $WordCountJob-Variablen.</span><span class="sxs-lookup"><span data-stu-id="82037-120">The third command uses the **New-AzureHDInsightMapReduceJobDefinition** cmdlet to create a MapReduce job definition, and then stores it in the $WordCountJob variable.</span></span>

<span data-ttu-id="82037-121">Der endgültige Befehl verwendet den Pipelineoperator, um den $WordCountJob an das Cmdlet **Start-AzureHDInsightJob** zu übergeben, um den Auftrag zu starten.</span><span class="sxs-lookup"><span data-stu-id="82037-121">The final command uses the pipeline operator to pass the $WordCountJob to the **Start-AzureHDInsightJob** cmdlet to start the job.</span></span>
<span data-ttu-id="82037-122">Nachdem der Auftrag gestartet wurde, wird er an das **Wait-AzureHDInsightJob-** Cmdlet übergeben, das auf den Abschluss des Auftrags wartet, bevor er an das Cmdlet **Get-AzureHDInsightJobOutput** übergeben wird, um die Ausgabe des Auftrags zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="82037-122">After the job starts, it is passed to the **Wait-AzureHDInsightJob** cmdlet, which waits for the job to complete before passing it to the **Get-AzureHDInsightJobOutput** cmdlet to get the job output.</span></span>

## <span data-ttu-id="82037-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="82037-123">PARAMETERS</span></span>

### <span data-ttu-id="82037-124">-Zertifikat</span><span class="sxs-lookup"><span data-stu-id="82037-124">-Certificate</span></span>
<span data-ttu-id="82037-125">Gibt das Verwaltungszertifikat für ein Azure-Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="82037-125">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82037-126">-Cluster</span><span class="sxs-lookup"><span data-stu-id="82037-126">-Cluster</span></span>
<span data-ttu-id="82037-127">Gibt einen Cluster an.</span><span class="sxs-lookup"><span data-stu-id="82037-127">Specifies a cluster.</span></span>
<span data-ttu-id="82037-128">Mit diesem Cmdlet wird ein Auftrag auf dem Cluster gestartet, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="82037-128">This cmdlet starts a job on the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82037-129">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="82037-129">-Credential</span></span>
<span data-ttu-id="82037-130">Gibt Cluster Anmeldeinformationen für direkten HTTP-Zugriff auf einen Cluster an.</span><span class="sxs-lookup"><span data-stu-id="82037-130">Specifies cluster credentials for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="82037-131">Sie können diesen Parameter anstelle des *Subscription* -Parameters angeben, um den Zugriff auf einen Cluster zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="82037-131">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: Start jobDetails on an HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82037-132">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="82037-132">-Endpoint</span></span>
<span data-ttu-id="82037-133">Gibt den Endpunkt an, mit dem eine Verbindung mit Azure hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="82037-133">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="82037-134">Wenn Sie diesen Parameter nicht angeben, verwendet dieses Cmdlet den Standardendpunkt.</span><span class="sxs-lookup"><span data-stu-id="82037-134">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82037-135">-HostedService</span><span class="sxs-lookup"><span data-stu-id="82037-135">-HostedService</span></span>
<span data-ttu-id="82037-136">Gibt den Namespace eines HDInsight-Diensts an, wenn Sie den Standardnamespace nicht verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="82037-136">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82037-137">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="82037-137">-IgnoreSslErrors</span></span>
<span data-ttu-id="82037-138">Gibt an, ob SSL-Fehler (Secure Sockets Layer) ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="82037-138">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82037-139">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="82037-139">-JobDefinition</span></span>
<span data-ttu-id="82037-140">Gibt den Endpunkt an, der beim Herstellen einer Verbindung mit Microsoft Azure verwendet werden soll, wenn sich der Endpunkt vom Standardwert unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="82037-140">Specifies the endpoint to use when connecting to Microsoft Azure if the endpoint is different from the default.</span></span>

```yaml
Type: AzureHDInsightJobDefinition
Parameter Sets: (All)
Aliases: jobDetails

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82037-141">-Profil</span><span class="sxs-lookup"><span data-stu-id="82037-141">-Profile</span></span>
<span data-ttu-id="82037-142">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="82037-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="82037-143">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="82037-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="82037-144">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="82037-144">-Subscription</span></span>
<span data-ttu-id="82037-145">Gibt ein Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="82037-145">Specifies a subscription.</span></span>
<span data-ttu-id="82037-146">Mit diesem Cmdlet wird ein Auftrag für das Abonnement gestartet, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="82037-146">This cmdlet starts a job for the subscription that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82037-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82037-147">CommonParameters</span></span>
<span data-ttu-id="82037-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82037-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82037-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82037-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82037-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="82037-150">INPUTS</span></span>

## <span data-ttu-id="82037-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="82037-151">OUTPUTS</span></span>

## <span data-ttu-id="82037-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="82037-152">NOTES</span></span>

## <span data-ttu-id="82037-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="82037-153">RELATED LINKS</span></span>

[<span data-ttu-id="82037-154">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="82037-154">Get-AzureHDInsightJob</span></span>](./Get-AzureHDInsightJob.md)

[<span data-ttu-id="82037-155">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="82037-155">Get-AzureHDInsightJobOutput</span></span>](./Get-AzureHDInsightJobOutput.md)

[<span data-ttu-id="82037-156">Neu – AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="82037-156">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="82037-157">Stopp-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="82037-157">Stop-AzureHDInsightJob</span></span>](./Stop-AzureHDInsightJob.md)

[<span data-ttu-id="82037-158">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="82037-158">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


