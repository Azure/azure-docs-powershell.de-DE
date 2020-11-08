---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 0BF58D9C-814E-4276-823F-D566DC99391C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 773af58d0ae9b4ca940240875b5cf9a8d3a0ffe7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006043"
---
# <span data-ttu-id="c4ab8-101">Use-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c4ab8-101">Use-AzureHDInsightCluster</span></span>

## <span data-ttu-id="c4ab8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c4ab8-102">SYNOPSIS</span></span>
<span data-ttu-id="c4ab8-103">Wählt einen HDInsight-Cluster für das Invoke-AzureHDInsightHiveJob-Cmdlet aus, das zum Übermitteln von Aufträgen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-103">Selects an HDInsight cluster for the Invoke-AzureHDInsightHiveJob cmdlet to use to submit jobs.</span></span>

## <span data-ttu-id="c4ab8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4ab8-104">SYNTAX</span></span>

```
Use-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Name <String> [-Subscription <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4ab8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4ab8-105">DESCRIPTION</span></span>
<span data-ttu-id="c4ab8-106">Diese Version von Azure PowerShell-HDInsight ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="c4ab8-107">Diese Cmdlets werden vom 1. Januar 2017 entfernt.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="c4ab8-108">Verwenden Sie bitte die neuere Version von Azure PowerShell-HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="c4ab8-109">Informationen zum Verwenden des neuen HDInsight zum Erstellen eines Clusters finden Sie unter [Erstellen von Linux-basierten Clustern in HDInsight mithilfe von Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="c4ab8-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="c4ab8-110">Informationen zum Übermitteln von Aufträgen mithilfe von Azure PowerShell und anderen Ansätzen finden Sie unter über [Mitteln von Hadoop-Aufträgen in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="c4ab8-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="c4ab8-111">Referenzinformationen zu Azure PowerShell-HDInsight finden Sie unter [Azure HDInsight-Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c4ab8-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="c4ab8-112">Das Cmdlet **use-AzureHDInsightCluster** wählt den Azure HDInsight-Cluster für das **Invoke-AzureHDInsightHiveJob-** Cmdlet aus, das zum Übermitteln von Aufträgen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-112">The **Use-AzureHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the **Invoke-AzureHDInsightHiveJob** cmdlet to use to submit jobs.</span></span>

## <span data-ttu-id="c4ab8-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4ab8-113">EXAMPLES</span></span>

## <span data-ttu-id="c4ab8-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4ab8-114">PARAMETERS</span></span>

### <span data-ttu-id="c4ab8-115">-Zertifikat</span><span class="sxs-lookup"><span data-stu-id="c4ab8-115">-Certificate</span></span>
<span data-ttu-id="c4ab8-116">Gibt das Verwaltungszertifikat für ein Azure-Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="c4ab8-117">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="c4ab8-117">-Endpoint</span></span>
<span data-ttu-id="c4ab8-118">Gibt den Endpunkt an, mit dem eine Verbindung mit Azure hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="c4ab8-119">Wenn Sie diesen Parameter nicht angeben, verwendet dieses Cmdlet den Standardendpunkt.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="c4ab8-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="c4ab8-120">-HostedService</span></span>
<span data-ttu-id="c4ab8-121">Gibt den Namespace eines HDInsight-Diensts an.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-121">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="c4ab8-122">Wenn Sie diesen Parameter nicht angeben, wird der Standardnamespace verwendet.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-122">If you do not specify this parameter, the default namespace is used.</span></span>

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

### <span data-ttu-id="c4ab8-123">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="c4ab8-123">-IgnoreSslErrors</span></span>
<span data-ttu-id="c4ab8-124">Gibt an, ob SSL-Fehler (Secure Sockets Layer) ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-124">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="c4ab8-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c4ab8-125">-Name</span></span>
<span data-ttu-id="c4ab8-126">Gibt den Namen des Clusters an, der vom Cmdlet **Invoke-AzureHDInsightHiveJob** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-126">Specifies the name of the cluster that is used by the **Invoke-AzureHDInsightHiveJob** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4ab8-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="c4ab8-127">-Profile</span></span>
<span data-ttu-id="c4ab8-128">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c4ab8-129">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c4ab8-130">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="c4ab8-130">-Subscription</span></span>
<span data-ttu-id="c4ab8-131">Gibt das Abonnement an, das die zu verwendenden HDInsight-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-131">Specifies the subscription that contains the HDInsight clusters to use.</span></span>

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

### <span data-ttu-id="c4ab8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4ab8-132">CommonParameters</span></span>
<span data-ttu-id="c4ab8-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4ab8-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4ab8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4ab8-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c4ab8-135">INPUTS</span></span>

## <span data-ttu-id="c4ab8-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c4ab8-136">OUTPUTS</span></span>

## <span data-ttu-id="c4ab8-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="c4ab8-137">NOTES</span></span>

## <span data-ttu-id="c4ab8-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c4ab8-138">RELATED LINKS</span></span>

[<span data-ttu-id="c4ab8-139">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c4ab8-139">Get-AzureHDInsightCluster</span></span>](./Get-AzureHDInsightCluster.md)

[<span data-ttu-id="c4ab8-140">Neu – AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c4ab8-140">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="c4ab8-141">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c4ab8-141">Remove-AzureHDInsightCluster</span></span>](./Remove-AzureHDInsightCluster.md)


