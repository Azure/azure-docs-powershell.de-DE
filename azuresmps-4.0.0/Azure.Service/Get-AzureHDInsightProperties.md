---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 325DE85D-B9CB-4584-8C61-DA417736ABBF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 55992408c1376c9456157387456b114c292b44c2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006557"
---
# <span data-ttu-id="b2f37-101">Get-AzureHDInsightProperties</span><span class="sxs-lookup"><span data-stu-id="b2f37-101">Get-AzureHDInsightProperties</span></span>

## <span data-ttu-id="b2f37-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b2f37-102">SYNOPSIS</span></span>
<span data-ttu-id="b2f37-103">Ruft Eigenschaften ab, die für einen HDInsight-Dienst spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="b2f37-103">Gets properties specific to an HDInsight service.</span></span>

## <span data-ttu-id="b2f37-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2f37-104">SYNTAX</span></span>

```
Get-AzureHDInsightProperties [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] [-Locations] [-Subscription <String>] [-Versions] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2f37-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2f37-105">DESCRIPTION</span></span>
<span data-ttu-id="b2f37-106">Diese Version von Azure PowerShell-HDInsight ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="b2f37-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="b2f37-107">Diese Cmdlets werden vom 1. Januar 2017 entfernt.</span><span class="sxs-lookup"><span data-stu-id="b2f37-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="b2f37-108">Verwenden Sie bitte die neuere Version von Azure PowerShell-HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b2f37-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="b2f37-109">Informationen zum Verwenden des neuen HDInsight zum Erstellen eines Clusters finden Sie unter [Erstellen von Linux-basierten Clustern in HDInsight mithilfe von Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="b2f37-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="b2f37-110">Informationen zum Übermitteln von Aufträgen mithilfe von Azure PowerShell und anderen Ansätzen finden Sie unter über [Mitteln von Hadoop-Aufträgen in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="b2f37-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="b2f37-111">Referenzinformationen zu Azure PowerShell-HDInsight finden Sie unter [Azure HDInsight-Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b2f37-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="b2f37-112">Das Cmdlet " **Get-AzureHDInsightProperties** " Ruft Eigenschaften ab, die für einen Azure HDInsight-Dienst spezifisch sind, beispielsweise eine Liste der verfügbaren Azure-Bereiche, HDInsight-Cluster Versionen und verfügbarer Rechenkapazität.</span><span class="sxs-lookup"><span data-stu-id="b2f37-112">The **Get-AzureHDInsightProperties** cmdlet gets properties specific to an Azure HDInsight service, such as a list of available Azure regions, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="b2f37-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b2f37-113">EXAMPLES</span></span>

### <span data-ttu-id="b2f37-114">Beispiel 1: Abrufen von HDInsight-Eigenschaften für ein Abonnement</span><span class="sxs-lookup"><span data-stu-id="b2f37-114">Example 1: Get HDInsight properties for a subscription</span></span>
```
PS C:\>$SubName = Get-AzureSubscription -Current | %{ $_.SubscriptionName }
PS C:\> Get-AzureHDInsightProperties -Subscription $SubName
```

<span data-ttu-id="b2f37-115">Der erste Befehl ruft den Namen des aktuellen Azure-Abonnements ab und speichert ihn dann in der $SubName-Variablen.</span><span class="sxs-lookup"><span data-stu-id="b2f37-115">The first command gets the name of the current Azure subscription, and then stores it in the $SubName variable.</span></span>

<span data-ttu-id="b2f37-116">Der zweite Befehl ruft die HDInsight-Eigenschaften für das Abonnement in $SubName ab.</span><span class="sxs-lookup"><span data-stu-id="b2f37-116">The second command gets the HDInsight properties for the subscription in $SubName.</span></span>

## <span data-ttu-id="b2f37-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2f37-117">PARAMETERS</span></span>

### <span data-ttu-id="b2f37-118">-Zertifikat</span><span class="sxs-lookup"><span data-stu-id="b2f37-118">-Certificate</span></span>
<span data-ttu-id="b2f37-119">Gibt das Verwaltungszertifikat für ein Azure-Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="b2f37-119">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="b2f37-120">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="b2f37-120">-Endpoint</span></span>
<span data-ttu-id="b2f37-121">Gibt den Endpunkt an, mit dem eine Verbindung mit Azure hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2f37-121">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="b2f37-122">Wenn Sie diesen Parameter nicht angeben, verwendet dieses Cmdlet den Standardendpunkt.</span><span class="sxs-lookup"><span data-stu-id="b2f37-122">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="b2f37-123">-HostedService</span><span class="sxs-lookup"><span data-stu-id="b2f37-123">-HostedService</span></span>
<span data-ttu-id="b2f37-124">Gibt den Namespace eines HDInsight-Diensts an.</span><span class="sxs-lookup"><span data-stu-id="b2f37-124">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="b2f37-125">Wenn Sie diesen Parameter nicht angeben, verwendet dieses Cmdlet den Standardnamespace.</span><span class="sxs-lookup"><span data-stu-id="b2f37-125">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="b2f37-126">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="b2f37-126">-IgnoreSslErrors</span></span>
<span data-ttu-id="b2f37-127">Gibt an, ob SSL-Fehler (Secure Sockets Layer) ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="b2f37-127">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="b2f37-128">-Standorte</span><span class="sxs-lookup"><span data-stu-id="b2f37-128">-Locations</span></span>
<span data-ttu-id="b2f37-129">Gibt an, dass dieses Cmdlet die Liste der Azure-Bereiche abruft, in denen der HDInsight-Dienst verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b2f37-129">Indicates that this cmdlet gets the list of Azure regions where the HDInsight service is available.</span></span>

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

### <span data-ttu-id="b2f37-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="b2f37-130">-Profile</span></span>
<span data-ttu-id="b2f37-131">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="b2f37-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b2f37-132">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="b2f37-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b2f37-133">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="b2f37-133">-Subscription</span></span>
<span data-ttu-id="b2f37-134">Gibt das Abonnement an, das die HDInsight-Eigenschaften enthält, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b2f37-134">Specifies the subscription that contains the HDInsight properties to get.</span></span>

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

### <span data-ttu-id="b2f37-135">-Versionen</span><span class="sxs-lookup"><span data-stu-id="b2f37-135">-Versions</span></span>
<span data-ttu-id="b2f37-136">Gibt an, dass dieses Cmdlet die Liste der HDInsight-Cluster Versionen abruft, die im Dienst für ein Abonnement zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="b2f37-136">Indicates that this cmdlet gets the list of HDInsight cluster versions that are available in the service for a subscription.</span></span>

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

### <span data-ttu-id="b2f37-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2f37-137">CommonParameters</span></span>
<span data-ttu-id="b2f37-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2f37-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2f37-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2f37-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2f37-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b2f37-140">INPUTS</span></span>

## <span data-ttu-id="b2f37-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b2f37-141">OUTPUTS</span></span>

## <span data-ttu-id="b2f37-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="b2f37-142">NOTES</span></span>

## <span data-ttu-id="b2f37-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b2f37-143">RELATED LINKS</span></span>

