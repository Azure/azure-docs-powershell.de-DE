---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: EE2ADA86-B2A3-4F6F-96EF-BB61D6DC550F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 338bef67e771bf211c063bf054e13e3844497850
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005970"
---
# <span data-ttu-id="ea0af-101">Stop-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ea0af-101">Stop-AzureHDInsightJob</span></span>

## <span data-ttu-id="ea0af-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ea0af-102">SYNOPSIS</span></span>
<span data-ttu-id="ea0af-103">Beendet einen HDInsight-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="ea0af-103">Stops an HDInsight job.</span></span>

## <span data-ttu-id="ea0af-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea0af-104">SYNTAX</span></span>

### <span data-ttu-id="ea0af-105">Starten von Tabelle Jobdetails auf einem HDInsight-Cluster (Standard)</span><span class="sxs-lookup"><span data-stu-id="ea0af-105">Start jobDetails on an HDInsight Cluster (Default)</span></span>
```
Stop-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>] -JobId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ea0af-106">Starten von Tabelle Jobdetails auf einem HDInsight-Cluster (mit bestimmten Anmeldeinformationen für Abonnements)</span><span class="sxs-lookup"><span data-stu-id="ea0af-106">Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Stop-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobId <String> [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ea0af-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ea0af-107">DESCRIPTION</span></span>
<span data-ttu-id="ea0af-108">Diese Version von Azure PowerShell-HDInsight ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="ea0af-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="ea0af-109">Diese Cmdlets werden vom 1. Januar 2017 entfernt.</span><span class="sxs-lookup"><span data-stu-id="ea0af-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="ea0af-110">Verwenden Sie bitte die neuere Version von Azure PowerShell-HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ea0af-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="ea0af-111">Informationen zum Verwenden des neuen HDInsight zum Erstellen eines Clusters finden Sie unter [Erstellen von Linux-basierten Clustern in HDInsight mithilfe von Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="ea0af-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="ea0af-112">Informationen zum Übermitteln von Aufträgen mithilfe von Azure PowerShell und anderen Ansätzen finden Sie unter über [Mitteln von Hadoop-Aufträgen in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="ea0af-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="ea0af-113">Referenzinformationen zu Azure PowerShell-HDInsight finden Sie unter [Azure HDInsight-Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ea0af-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="ea0af-114">Das Cmdlet **Stop-AzureHDInsightJob** beendet einen Azure HDInsight-Auftrag auf dem angegebenen Cluster.</span><span class="sxs-lookup"><span data-stu-id="ea0af-114">The **Stop-AzureHDInsightJob** cmdlet stops an Azure HDInsight job on the specified cluster.</span></span>

## <span data-ttu-id="ea0af-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ea0af-115">EXAMPLES</span></span>

## <span data-ttu-id="ea0af-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea0af-116">PARAMETERS</span></span>

### <span data-ttu-id="ea0af-117">-Zertifikat</span><span class="sxs-lookup"><span data-stu-id="ea0af-117">-Certificate</span></span>
<span data-ttu-id="ea0af-118">Gibt das Verwaltungszertifikat für ein Azure-Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="ea0af-118">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="ea0af-119">-Cluster</span><span class="sxs-lookup"><span data-stu-id="ea0af-119">-Cluster</span></span>
<span data-ttu-id="ea0af-120">Gibt einen Cluster an.</span><span class="sxs-lookup"><span data-stu-id="ea0af-120">Specifies a cluster.</span></span>
<span data-ttu-id="ea0af-121">Dieses Cmdlet beendet einen Auftrag, der auf dem Cluster ausgeführt wird, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ea0af-121">This cmdlet stops a job that runs on the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea0af-122">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="ea0af-122">-Credential</span></span>
<span data-ttu-id="ea0af-123">Gibt die für den direkten HTTP-Zugriff auf einen Cluster zu verwendenden Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="ea0af-123">Specifies the credentials to use for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="ea0af-124">Sie können diesen Parameter anstelle des *Subscription* -Parameters angeben, um den Zugriff auf einen Cluster zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="ea0af-124">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

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

### <span data-ttu-id="ea0af-125">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="ea0af-125">-Endpoint</span></span>
<span data-ttu-id="ea0af-126">Gibt den Endpunkt an, mit dem eine Verbindung mit Azure hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ea0af-126">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="ea0af-127">Wenn Sie diesen Parameter nicht angeben, verwendet dieses Cmdlet den Standardendpunkt.</span><span class="sxs-lookup"><span data-stu-id="ea0af-127">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="ea0af-128">-HostedService</span><span class="sxs-lookup"><span data-stu-id="ea0af-128">-HostedService</span></span>
<span data-ttu-id="ea0af-129">Gibt den Namespace eines HDInsight-Diensts an, wenn Sie den Standardnamespace nicht verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="ea0af-129">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

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

### <span data-ttu-id="ea0af-130">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="ea0af-130">-IgnoreSslErrors</span></span>
<span data-ttu-id="ea0af-131">Gibt an, ob SSL-Fehler (Secure Sockets Layer) ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="ea0af-131">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="ea0af-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="ea0af-132">-JobId</span></span>
<span data-ttu-id="ea0af-133">Gibt die ID des HDInsight-Auftrags an, der beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ea0af-133">Specifies the ID of the HDInsight job to stop.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea0af-134">-Profil</span><span class="sxs-lookup"><span data-stu-id="ea0af-134">-Profile</span></span>
<span data-ttu-id="ea0af-135">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="ea0af-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ea0af-136">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="ea0af-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ea0af-137">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="ea0af-137">-Subscription</span></span>
<span data-ttu-id="ea0af-138">Gibt ein Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="ea0af-138">Specifies a subscription.</span></span>
<span data-ttu-id="ea0af-139">Dieses Cmdlet beendet einen Auftrag für das Abonnement, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ea0af-139">This cmdlet stops a job for the subscription that this parameter specifies.</span></span>

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

### <span data-ttu-id="ea0af-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea0af-140">CommonParameters</span></span>
<span data-ttu-id="ea0af-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea0af-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea0af-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea0af-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea0af-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ea0af-143">INPUTS</span></span>

## <span data-ttu-id="ea0af-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ea0af-144">OUTPUTS</span></span>

## <span data-ttu-id="ea0af-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="ea0af-145">NOTES</span></span>

## <span data-ttu-id="ea0af-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ea0af-146">RELATED LINKS</span></span>

[<span data-ttu-id="ea0af-147">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ea0af-147">Get-AzureHDInsightJob</span></span>](./Get-AzureHDInsightJob.md)

[<span data-ttu-id="ea0af-148">Anfang-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ea0af-148">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="ea0af-149">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ea0af-149">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


