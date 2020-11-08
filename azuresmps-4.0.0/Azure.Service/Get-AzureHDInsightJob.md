---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3E3C9626-7AED-4B15-93D0-0B79AD17A834
online version: ''
schema: 2.0.0
ms.openlocfilehash: de4b768dbc6c97e84bccd4c8e0ef42f6f81a5b31
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006556"
---
# <span data-ttu-id="732e5-101">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="732e5-101">Get-AzureHDInsightJob</span></span>

## <span data-ttu-id="732e5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="732e5-102">SYNOPSIS</span></span>
<span data-ttu-id="732e5-103">Ruft HDInsight-Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="732e5-103">Gets HDInsight jobs.</span></span>

## <span data-ttu-id="732e5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="732e5-104">SYNTAX</span></span>

### <span data-ttu-id="732e5-105">Abrufen des Tabelle Jobdetails-Verlaufs eines HDInsight-Clusters (Standard)</span><span class="sxs-lookup"><span data-stu-id="732e5-105">Get jobDetails History of a HDInsight Cluster (Default)</span></span>
```
Get-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>] [-IgnoreSslErrors <Boolean>]
 [-JobId <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="732e5-106">Abrufen des Tabelle Jobdetails-Verlaufs eines HDInsight-Clusters (mit bestimmten Anmeldeinformationen für Abonnements)</span><span class="sxs-lookup"><span data-stu-id="732e5-106">Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Get-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] [-JobId <String>] [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="732e5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="732e5-107">DESCRIPTION</span></span>
<span data-ttu-id="732e5-108">Diese Version von Azure PowerShell-HDInsight ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="732e5-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="732e5-109">Diese Cmdlets werden vom 1. Januar 2017 entfernt.</span><span class="sxs-lookup"><span data-stu-id="732e5-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="732e5-110">Verwenden Sie bitte die neuere Version von Azure PowerShell-HDInsight.</span><span class="sxs-lookup"><span data-stu-id="732e5-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="732e5-111">Informationen zum Verwenden des neuen HDInsight zum Erstellen eines Clusters finden Sie unter [Erstellen von Linux-basierten Clustern in HDInsight mithilfe von Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="732e5-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="732e5-112">Informationen zum Übermitteln von Aufträgen mithilfe von Azure PowerShell und anderen Ansätzen finden Sie unter über [Mitteln von Hadoop-Aufträgen in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="732e5-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="732e5-113">Referenzinformationen zu Azure PowerShell-HDInsight finden Sie unter [Azure HDInsight-Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="732e5-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="732e5-114">Das Cmdlet " **Get-AzureHDInsightJob** " Ruft aktuelle Azure HDInsight-Aufträge für einen angegebenen Cluster ab und zeigt diese in umgekehrter chronologischer Reihenfolge an.</span><span class="sxs-lookup"><span data-stu-id="732e5-114">The **Get-AzureHDInsightJob** cmdlet gets recent Azure HDInsight jobs for a specified cluster and displays them in reverse chronological order.</span></span>

## <span data-ttu-id="732e5-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="732e5-115">EXAMPLES</span></span>

## <span data-ttu-id="732e5-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="732e5-116">PARAMETERS</span></span>

### <span data-ttu-id="732e5-117">-Zertifikat</span><span class="sxs-lookup"><span data-stu-id="732e5-117">-Certificate</span></span>
<span data-ttu-id="732e5-118">Gibt das Verwaltungszertifikat für ein Azure-Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="732e5-118">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="732e5-119">-Cluster</span><span class="sxs-lookup"><span data-stu-id="732e5-119">-Cluster</span></span>
<span data-ttu-id="732e5-120">Gibt einen Cluster an.</span><span class="sxs-lookup"><span data-stu-id="732e5-120">Specifies a cluster.</span></span>
<span data-ttu-id="732e5-121">Dieses Cmdlet ruft HDInsight-Aufträge ab, die auf dem Cluster ausgeführt werden, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="732e5-121">This cmdlet gets HDInsight jobs that run on the cluster that this parameter specifies.</span></span>

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

### <span data-ttu-id="732e5-122">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="732e5-122">-Credential</span></span>
<span data-ttu-id="732e5-123">Gibt die für den direkten HTTP-Zugriff auf einen Cluster zu verwendenden Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="732e5-123">Specifies the credentials to use for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="732e5-124">Sie können diesen Parameter anstelle des *Subscription* -Parameters angeben, um den Zugriff auf einen Cluster zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="732e5-124">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: Get jobDetails History of a HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="732e5-125">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="732e5-125">-Endpoint</span></span>
<span data-ttu-id="732e5-126">Gibt den Endpunkt an, mit dem eine Verbindung mit Azure hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="732e5-126">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="732e5-127">Wenn Sie diesen Parameter nicht angeben, verwendet dieses Cmdlet den Standardendpunkt.</span><span class="sxs-lookup"><span data-stu-id="732e5-127">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="732e5-128">-HostedService</span><span class="sxs-lookup"><span data-stu-id="732e5-128">-HostedService</span></span>
<span data-ttu-id="732e5-129">Gibt den Namespace eines HDInsight-Diensts an, wenn Sie den Standardnamespace nicht verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="732e5-129">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

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

### <span data-ttu-id="732e5-130">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="732e5-130">-IgnoreSslErrors</span></span>
<span data-ttu-id="732e5-131">Gibt an, ob SSL-Fehler (Secure Sockets Layer) ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="732e5-131">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="732e5-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="732e5-132">-JobId</span></span>
<span data-ttu-id="732e5-133">Gibt die ID des abzurufenden Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="732e5-133">Specifies the ID of a job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="732e5-134">-Profil</span><span class="sxs-lookup"><span data-stu-id="732e5-134">-Profile</span></span>
<span data-ttu-id="732e5-135">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="732e5-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="732e5-136">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="732e5-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="732e5-137">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="732e5-137">-Subscription</span></span>
<span data-ttu-id="732e5-138">Gibt das Abonnement an, das die HDInsight-Aufträge enthält, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="732e5-138">Specifies the subscription that contains the HDInsight jobs to get.</span></span>

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="732e5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="732e5-139">CommonParameters</span></span>
<span data-ttu-id="732e5-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="732e5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="732e5-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="732e5-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="732e5-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="732e5-142">INPUTS</span></span>

## <span data-ttu-id="732e5-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="732e5-143">OUTPUTS</span></span>

## <span data-ttu-id="732e5-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="732e5-144">NOTES</span></span>

## <span data-ttu-id="732e5-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="732e5-145">RELATED LINKS</span></span>

[<span data-ttu-id="732e5-146">Anfang-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="732e5-146">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="732e5-147">Stopp-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="732e5-147">Stop-AzureHDInsightJob</span></span>](./Stop-AzureHDInsightJob.md)

[<span data-ttu-id="732e5-148">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="732e5-148">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


