---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 6818F49E-0A51-4D99-BC3D-5A90F1F30C33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 78caed4ac43f21a1afe21a8901bdcd77ba29e482
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005682"
---
# <span data-ttu-id="4f24e-101">Revoke-AzureHDInsightRdpAccess</span><span class="sxs-lookup"><span data-stu-id="4f24e-101">Revoke-AzureHDInsightRdpAccess</span></span>

## <span data-ttu-id="4f24e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4f24e-102">SYNOPSIS</span></span>
<span data-ttu-id="4f24e-103">Deaktiviert den RDP-Zugriff auf einen HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="4f24e-103">Disables RDP access to an HDInsight cluster.</span></span>

## <span data-ttu-id="4f24e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f24e-104">SYNTAX</span></span>

```
Revoke-AzureHDInsightRdpAccess [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Location <String> -Name <String> [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4f24e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4f24e-105">DESCRIPTION</span></span>
<span data-ttu-id="4f24e-106">Diese Version von Azure PowerShell-HDInsight ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="4f24e-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="4f24e-107">Diese Cmdlets werden vom 1. Januar 2017 entfernt.</span><span class="sxs-lookup"><span data-stu-id="4f24e-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="4f24e-108">Verwenden Sie bitte die neuere Version von Azure PowerShell-HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4f24e-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="4f24e-109">Informationen zum Verwenden des neuen HDInsight zum Erstellen eines Clusters finden Sie unter [Erstellen von Linux-basierten Clustern in HDInsight mithilfe von Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="4f24e-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="4f24e-110">Informationen zum Übermitteln von Aufträgen mithilfe von Azure PowerShell und anderen Ansätzen finden Sie unter über [Mitteln von Hadoop-Aufträgen in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="4f24e-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="4f24e-111">Referenzinformationen zu Azure PowerShell-HDInsight finden Sie unter [Azure HDInsight-Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4f24e-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="4f24e-112">Das **REVOKE-AzureHDInsightRdpAccess-** Cmdlet deaktiviert den Remote Desktop Protokoll-Zugriff (RDP) auf einen Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="4f24e-112">The **Revoke-AzureHDInsightRdpAccess** cmdlet disables Remote Desktop Protocol (RDP) access to an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="4f24e-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4f24e-113">EXAMPLES</span></span>

## <span data-ttu-id="4f24e-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f24e-114">PARAMETERS</span></span>

### <span data-ttu-id="4f24e-115">-Zertifikat</span><span class="sxs-lookup"><span data-stu-id="4f24e-115">-Certificate</span></span>
<span data-ttu-id="4f24e-116">Gibt das Verwaltungszertifikat für ein Azure-Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="4f24e-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="4f24e-117">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="4f24e-117">-Endpoint</span></span>
<span data-ttu-id="4f24e-118">Gibt den Endpunkt an, mit dem eine Verbindung mit Azure hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f24e-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="4f24e-119">Wenn Sie diesen Parameter nicht angeben, verwendet dieses Cmdlet den Standardendpunkt.</span><span class="sxs-lookup"><span data-stu-id="4f24e-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="4f24e-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="4f24e-120">-HostedService</span></span>
<span data-ttu-id="4f24e-121">Gibt den Namespace eines HDInsight-Diensts an.</span><span class="sxs-lookup"><span data-stu-id="4f24e-121">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="4f24e-122">Wenn Sie diesen Parameter nicht angeben, verwendet dieses Cmdlet den Standardnamespace.</span><span class="sxs-lookup"><span data-stu-id="4f24e-122">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="4f24e-123">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="4f24e-123">-IgnoreSslErrors</span></span>
<span data-ttu-id="4f24e-124">Gibt an, ob SSL-Fehler (Secure Sockets Layer) ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="4f24e-124">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="4f24e-125">-Standort</span><span class="sxs-lookup"><span data-stu-id="4f24e-125">-Location</span></span>
<span data-ttu-id="4f24e-126">Gibt den Azure-Bereich an, in dem sich ein Cluster befindet.</span><span class="sxs-lookup"><span data-stu-id="4f24e-126">Specifies the Azure region in which a cluster is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f24e-127">-Name</span><span class="sxs-lookup"><span data-stu-id="4f24e-127">-Name</span></span>
<span data-ttu-id="4f24e-128">Gibt den Namen eines Azure HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="4f24e-128">Specifies the name of an Azure HDInsight cluster.</span></span>

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

### <span data-ttu-id="4f24e-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="4f24e-129">-Profile</span></span>
<span data-ttu-id="4f24e-130">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="4f24e-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4f24e-131">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="4f24e-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4f24e-132">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="4f24e-132">-Subscription</span></span>
<span data-ttu-id="4f24e-133">Gibt ein Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="4f24e-133">Specifies a subscription.</span></span>
<span data-ttu-id="4f24e-134">Mit diesem Cmdlet wird der Zugriff auf das Remote Desktop Protokoll (RDP) für das Abonnement, das dieser Parameter angibt, aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="4f24e-134">This cmdlet revokes Remote Desktop Protocol (RDP) access for the subscription that this parameter specifies.</span></span>

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

### <span data-ttu-id="4f24e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f24e-135">CommonParameters</span></span>
<span data-ttu-id="4f24e-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f24e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f24e-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f24e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f24e-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4f24e-138">INPUTS</span></span>

## <span data-ttu-id="4f24e-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4f24e-139">OUTPUTS</span></span>

## <span data-ttu-id="4f24e-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="4f24e-140">NOTES</span></span>

## <span data-ttu-id="4f24e-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4f24e-141">RELATED LINKS</span></span>

[<span data-ttu-id="4f24e-142">Grant-AzureHdinsightRdpAccess</span><span class="sxs-lookup"><span data-stu-id="4f24e-142">Grant-AzureHdinsightRdpAccess</span></span>](./Grant-AzureHdinsightRdpAccess.md)


