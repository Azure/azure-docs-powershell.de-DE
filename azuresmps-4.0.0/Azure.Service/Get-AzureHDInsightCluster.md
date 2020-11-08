---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3B39F43D-E74A-441D-91BC-26C324C1EDF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d0ea12e873604360114b02bb89d9bde12c9e70e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005850"
---
# <span data-ttu-id="e542a-101">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e542a-101">Get-AzureHDInsightCluster</span></span>

## <span data-ttu-id="e542a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e542a-102">SYNOPSIS</span></span>
<span data-ttu-id="e542a-103">Ruft einen HDInsight-Cluster ab.</span><span class="sxs-lookup"><span data-stu-id="e542a-103">Gets an HDInsight cluster.</span></span>

## <span data-ttu-id="e542a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e542a-104">SYNTAX</span></span>

```
Get-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] [-Name <String>] [-Subscription <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e542a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e542a-105">DESCRIPTION</span></span>
<span data-ttu-id="e542a-106">Diese Version von Azure PowerShell-HDInsight ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="e542a-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="e542a-107">Diese Cmdlets werden vom 1. Januar 2017 entfernt.</span><span class="sxs-lookup"><span data-stu-id="e542a-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="e542a-108">Verwenden Sie bitte die neuere Version von Azure PowerShell-HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e542a-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="e542a-109">Informationen zum Verwenden des neuen HDInsight zum Erstellen eines Clusters finden Sie unter [Erstellen von Linux-basierten Clustern in HDInsight mithilfe von Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="e542a-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="e542a-110">Informationen zum Übermitteln von Aufträgen mithilfe von Azure PowerShell und anderen Ansätzen finden Sie unter über [Mitteln von Hadoop-Aufträgen in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="e542a-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="e542a-111">Referenzinformationen zu Azure PowerShell-HDInsight finden Sie unter [Azure HDInsight-Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e542a-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="e542a-112">Das Cmdlet " **Get-AzureHDInsightCluster** " Ruft die Azure HDInsight-Dienst Cluster für das aktuelle Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="e542a-112">The **Get-AzureHDInsightCluster** cmdlet gets the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="e542a-113">Sie können den Parameter *Name* verwenden, um einen bestimmten Cluster abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e542a-113">You can use the *Name* parameter to get a specific cluster.</span></span>

## <span data-ttu-id="e542a-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e542a-114">EXAMPLES</span></span>

### <span data-ttu-id="e542a-115">Beispiel 1: Abrufen der Cluster in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="e542a-115">Example 1: Get the clusters in a subscription</span></span>
```
PS C:\> Get-AzureHDInsightCluster
```

<span data-ttu-id="e542a-116">Dieser Befehl ruft Informationen zu den HDInsight-Clustern im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="e542a-116">This command gets information about the HDInsight clusters in the current subscription.</span></span>

## <span data-ttu-id="e542a-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="e542a-117">PARAMETERS</span></span>

### <span data-ttu-id="e542a-118">-Zertifikat</span><span class="sxs-lookup"><span data-stu-id="e542a-118">-Certificate</span></span>
<span data-ttu-id="e542a-119">Gibt das Verwaltungszertifikat für ein Azure-Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="e542a-119">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="e542a-120">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="e542a-120">-Endpoint</span></span>
<span data-ttu-id="e542a-121">Gibt den Endpunkt an, mit dem eine Verbindung mit Azure hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e542a-121">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="e542a-122">Wenn Sie diesen Parameter nicht angeben, verwendet dieses Cmdlet den Standardendpunkt.</span><span class="sxs-lookup"><span data-stu-id="e542a-122">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="e542a-123">-HostedService</span><span class="sxs-lookup"><span data-stu-id="e542a-123">-HostedService</span></span>
<span data-ttu-id="e542a-124">Gibt den Namespace eines HDInsight-Diensts an.</span><span class="sxs-lookup"><span data-stu-id="e542a-124">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="e542a-125">Wenn Sie diesen Parameter nicht angeben, verwendet dieses Cmdlet den Standardnamespace.</span><span class="sxs-lookup"><span data-stu-id="e542a-125">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="e542a-126">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="e542a-126">-IgnoreSslErrors</span></span>
<span data-ttu-id="e542a-127">Gibt an, ob SSL-Fehler (Secure Sockets Layer) ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="e542a-127">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="e542a-128">-Name</span><span class="sxs-lookup"><span data-stu-id="e542a-128">-Name</span></span>
<span data-ttu-id="e542a-129">Gibt den Namen eines HDInsight-Clusters an, der abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e542a-129">Specifies the name of an HDInsight cluster to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName, DnsName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e542a-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="e542a-130">-Profile</span></span>
<span data-ttu-id="e542a-131">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="e542a-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e542a-132">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="e542a-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e542a-133">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="e542a-133">-Subscription</span></span>
<span data-ttu-id="e542a-134">Gibt das Abonnement an, das den abzurufenden HDInsight-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="e542a-134">Specifies the subscription that contains the HDInsight cluster to get.</span></span>

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

### <span data-ttu-id="e542a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e542a-135">CommonParameters</span></span>
<span data-ttu-id="e542a-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e542a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e542a-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e542a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e542a-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e542a-138">INPUTS</span></span>

## <span data-ttu-id="e542a-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e542a-139">OUTPUTS</span></span>

## <span data-ttu-id="e542a-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="e542a-140">NOTES</span></span>

## <span data-ttu-id="e542a-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e542a-141">RELATED LINKS</span></span>

[<span data-ttu-id="e542a-142">Neu – AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e542a-142">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="e542a-143">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e542a-143">Remove-AzureHDInsightCluster</span></span>](./Remove-AzureHDInsightCluster.md)

[<span data-ttu-id="e542a-144">Verwenden von-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e542a-144">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


