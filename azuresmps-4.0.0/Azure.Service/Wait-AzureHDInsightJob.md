---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 2EA36090-1A45-4F77-9222-9C0E9C07656C
online version: ''
schema: 2.0.0
ms.openlocfilehash: ea1247fd2b91f173b8125ad61c0bf2b57f408d18
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006038"
---
# <span data-ttu-id="4f55f-101">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="4f55f-101">Wait-AzureHDInsightJob</span></span>

## <span data-ttu-id="4f55f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4f55f-102">SYNOPSIS</span></span>
<span data-ttu-id="4f55f-103">Erwartet den Abschluss oder Fehler eines HDInsight-Auftrags und zeigt den Status des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="4f55f-103">Awaits the completion or failure of an HDInsight job and displays the progress of the job.</span></span>

## <span data-ttu-id="4f55f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f55f-104">SYNTAX</span></span>

### <span data-ttu-id="4f55f-105">Abrufen des Tabelle Jobdetails-Verlaufs eines HDInsight-Clusters (Standard)</span><span class="sxs-lookup"><span data-stu-id="4f55f-105">Get jobDetails History of a HDInsight Cluster (Default)</span></span>
```
Wait-AzureHDInsightJob [-Credential <PSCredential>] [-WaitTimeoutInSeconds <Double>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4f55f-106">Abrufen des Tabelle Jobdetails-Verlaufs eines HDInsight-Clusters (mit bestimmten Anmeldeinformationen für Abonnements)</span><span class="sxs-lookup"><span data-stu-id="4f55f-106">Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Wait-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Job <AzureHDInsightJob> -Subscription <String> [-WaitTimeoutInSeconds <Double>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4f55f-107">Warten des Auftrags mit JobID in einem HDInsight-Cluster</span><span class="sxs-lookup"><span data-stu-id="4f55f-107">Wait Job with JobId on an HDInsight Cluster</span></span>
```
Wait-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>] -JobId <String>
 [-WaitTimeoutInSeconds <Double>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4f55f-108">Job mit Job auf einem HDInsight-Cluster warten</span><span class="sxs-lookup"><span data-stu-id="4f55f-108">Wait Job with Job on an HDInsight Cluster</span></span>
```
Wait-AzureHDInsightJob [-Credential <PSCredential>] -Job <AzureHDInsightJob> [-WaitTimeoutInSeconds <Double>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4f55f-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4f55f-109">DESCRIPTION</span></span>
<span data-ttu-id="4f55f-110">Diese Version von Azure PowerShell-HDInsight ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="4f55f-110">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="4f55f-111">Diese Cmdlets werden vom 1. Januar 2017 entfernt.</span><span class="sxs-lookup"><span data-stu-id="4f55f-111">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="4f55f-112">Verwenden Sie bitte die neuere Version von Azure PowerShell-HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4f55f-112">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="4f55f-113">Informationen zum Verwenden des neuen HDInsight zum Erstellen eines Clusters finden Sie unter [Erstellen von Linux-basierten Clustern in HDInsight mithilfe von Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="4f55f-113">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="4f55f-114">Informationen zum Übermitteln von Aufträgen mithilfe von Azure PowerShell und anderen Ansätzen finden Sie unter über [Mitteln von Hadoop-Aufträgen in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="4f55f-114">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="4f55f-115">Referenzinformationen zu Azure PowerShell-HDInsight finden Sie unter [Azure HDInsight-Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4f55f-115">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="4f55f-116">Das Cmdlet **Wait-AzureHDInsightJob** wartet auf den Abschluss oder Fehler eines Azure HDInsight-Auftrags und zeigt den Fortschritt des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="4f55f-116">The **Wait-AzureHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job and displays the progress of the job.</span></span>

## <span data-ttu-id="4f55f-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4f55f-117">EXAMPLES</span></span>

### <span data-ttu-id="4f55f-118">Beispiel 1: Ausführen eines Auftrags und abwarten des Abschlusses</span><span class="sxs-lookup"><span data-stu-id="4f55f-118">Example 1: Run a job and wait for it to complete</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:>\ $ClusterName = "MyCluster"
PS C:>\ $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:>\ $WordCountJob | Start-AzureHDInsightJob -Subscription $SubId -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

<span data-ttu-id="4f55f-119">Der erste Befehl ruft die aktuelle Azure-Abonnement-ID ab und speichert Sie dann in der $SubId-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4f55f-119">The first command gets the current Azure subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="4f55f-120">Der zweite Befehl ruft den angegebenen Cluster ab und speichert ihn dann in der $Clustername-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4f55f-120">The second command gets the specified cluster, and then stores it in the $ClusterName variable.</span></span>

<span data-ttu-id="4f55f-121">Der dritte Befehl verwendet das Cmdlet **New-AzureHDInsightMapReduceJobDefinition** , um eine MapReduce-Auftragsdefinition zu erstellen, und speichert Sie dann in der $WordCountJob-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4f55f-121">The third command uses the **New-AzureHDInsightMapReduceJobDefinition** cmdlet to create a MapReduce job definition, and then stores it in the $WordCountJob variable.</span></span>

<span data-ttu-id="4f55f-122">Der vierte Befehl verwendet mehrere Cmdlets in der folgenden Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="4f55f-122">The fourth command uses several cmdlets in sequence:</span></span> 

- <span data-ttu-id="4f55f-123">Er verwendet den Pipelineoperator, um $WordCountJob an das **Start-AzureHDInsightJob-** Cmdlet zu übergeben, um den Auftrag zu starten.</span><span class="sxs-lookup"><span data-stu-id="4f55f-123">It uses the pipeline operator to pass $WordCountJob to the **Start-AzureHDInsightJob** cmdlet to start the job.</span></span> 
- <span data-ttu-id="4f55f-124">Der Auftrag wird an das **Wait-AzureHDInsightJob-** Cmdlet übergeben, um 3600 Sekunden für den Abschluss des Auftrags zu warten.</span><span class="sxs-lookup"><span data-stu-id="4f55f-124">The job is passed to the **Wait-AzureHDInsightJob** cmdlet to wait 3600 seconds for the job to complete.</span></span> 
- <span data-ttu-id="4f55f-125">Wenn der Auftrag abgeschlossen ist, verwendet der Befehl das Cmdlet " **Get-AzureHDInsightJobOutput** ", um die Ausgabe des Auftrags abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4f55f-125">If the job completes, the command uses the **Get-AzureHDInsightJobOutput** cmdlet to get the job output.</span></span>

## <span data-ttu-id="4f55f-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f55f-126">PARAMETERS</span></span>

### <span data-ttu-id="4f55f-127">-Zertifikat</span><span class="sxs-lookup"><span data-stu-id="4f55f-127">-Certificate</span></span>
<span data-ttu-id="4f55f-128">Gibt das Verwaltungszertifikat für ein Azure-Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="4f55f-128">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f55f-129">-Cluster</span><span class="sxs-lookup"><span data-stu-id="4f55f-129">-Cluster</span></span>
<span data-ttu-id="4f55f-130">Gibt einen Cluster an.</span><span class="sxs-lookup"><span data-stu-id="4f55f-130">Specifies a cluster.</span></span>
<span data-ttu-id="4f55f-131">Dieses Cmdlet wartet auf einen Auftrag im Cluster, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="4f55f-131">This cmdlet waits for a job on the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Wait Job with JobId on an HDInsight Cluster
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f55f-132">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="4f55f-132">-Credential</span></span>
<span data-ttu-id="4f55f-133">Gibt die für den direkten HTTP-Zugriff auf einen Cluster zu verwendenden Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="4f55f-133">Specifies the credentials to use for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="4f55f-134">Sie können diesen Parameter anstelle des *Subscription* -Parameters angeben, um den Zugriff auf einen Cluster zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="4f55f-134">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: Get jobDetails History of a HDInsight Cluster, Wait Job with JobId on an HDInsight Cluster, Wait Job with Job on an HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f55f-135">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="4f55f-135">-Endpoint</span></span>
<span data-ttu-id="4f55f-136">Gibt den Endpunkt an, mit dem eine Verbindung mit Azure hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f55f-136">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="4f55f-137">Wenn Sie diesen Parameter nicht angeben, verwendet dieses Cmdlet den Standardendpunkt.</span><span class="sxs-lookup"><span data-stu-id="4f55f-137">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f55f-138">-HostedService</span><span class="sxs-lookup"><span data-stu-id="4f55f-138">-HostedService</span></span>
<span data-ttu-id="4f55f-139">Gibt den Namespace eines HDInsight-Diensts an.</span><span class="sxs-lookup"><span data-stu-id="4f55f-139">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="4f55f-140">Wenn Sie diesen Parameter nicht angeben, wird der Standardnamespace verwendet.</span><span class="sxs-lookup"><span data-stu-id="4f55f-140">If you do not specify this parameter, the default namespace is used.</span></span>

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f55f-141">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="4f55f-141">-IgnoreSslErrors</span></span>
<span data-ttu-id="4f55f-142">Gibt an, ob SSL-Fehler (Secure Sockets Layer) ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="4f55f-142">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f55f-143">-Job</span><span class="sxs-lookup"><span data-stu-id="4f55f-143">-Job</span></span>
<span data-ttu-id="4f55f-144">Gibt einen Azure HDInsight-Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="4f55f-144">Specifies an Azure HDInsight job.</span></span>

```yaml
Type: AzureHDInsightJob
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential), Wait Job with Job on an HDInsight Cluster
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f55f-145">-JobId</span><span class="sxs-lookup"><span data-stu-id="4f55f-145">-JobId</span></span>
<span data-ttu-id="4f55f-146">Gibt die ID des Auftrags an, auf den gewartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f55f-146">Specifies the ID of the job to wait for.</span></span>

```yaml
Type: String
Parameter Sets: Wait Job with JobId on an HDInsight Cluster
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f55f-147">-Profil</span><span class="sxs-lookup"><span data-stu-id="4f55f-147">-Profile</span></span>
<span data-ttu-id="4f55f-148">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="4f55f-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4f55f-149">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="4f55f-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4f55f-150">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="4f55f-150">-Subscription</span></span>
<span data-ttu-id="4f55f-151">Gibt ein Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="4f55f-151">Specifies a subscription.</span></span>
<span data-ttu-id="4f55f-152">Dieses Cmdlet wartet auf einen Auftrag für das Abonnement, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="4f55f-152">This cmdlet waits for a job for the subscription that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f55f-153">-WaitTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="4f55f-153">-WaitTimeoutInSeconds</span></span>
<span data-ttu-id="4f55f-154">Gibt das Timeout in Sekunden für den Wait-Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="4f55f-154">Specifies the time-out, in seconds, for the wait operation.</span></span>
<span data-ttu-id="4f55f-155">Wenn das Timeout abläuft, bevor der Auftrag abgeschlossen ist, wird das Cmdlet nicht mehr ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f55f-155">If the time-out expires before the job completes, the cmdlet ceases to run.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f55f-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f55f-156">CommonParameters</span></span>
<span data-ttu-id="4f55f-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f55f-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f55f-158">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f55f-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f55f-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4f55f-159">INPUTS</span></span>

## <span data-ttu-id="4f55f-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4f55f-160">OUTPUTS</span></span>

## <span data-ttu-id="4f55f-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="4f55f-161">NOTES</span></span>

## <span data-ttu-id="4f55f-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4f55f-162">RELATED LINKS</span></span>

[<span data-ttu-id="4f55f-163">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="4f55f-163">Get-AzureHDInsightJob</span></span>](./Get-AzureHDInsightJob.md)

[<span data-ttu-id="4f55f-164">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="4f55f-164">Get-AzureHDInsightJobOutput</span></span>](./Get-AzureHDInsightJobOutput.md)

[<span data-ttu-id="4f55f-165">Anfang-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="4f55f-165">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="4f55f-166">Stopp-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="4f55f-166">Stop-AzureHDInsightJob</span></span>](./Stop-AzureHDInsightJob.md)


