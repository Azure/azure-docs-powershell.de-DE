---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 95CCEB79-EAC4-4F56-B289-5401F976E5F5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92b2c005f855ccf99e8bae4d8db8445ba7e63dad
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006468"
---
# <span data-ttu-id="6f230-101">Grant-AzureHDInsightRdpAccess</span><span class="sxs-lookup"><span data-stu-id="6f230-101">Grant-AzureHDInsightRdpAccess</span></span>

## <span data-ttu-id="6f230-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6f230-102">SYNOPSIS</span></span>
<span data-ttu-id="6f230-103">Gewährt RDP-Zugriff auf einen HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="6f230-103">Grants RDP access to an HDInsight cluster.</span></span>

## <span data-ttu-id="6f230-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f230-104">SYNTAX</span></span>

```
Grant-AzureHDInsightRdpAccess [-Certificate <X509Certificate2>] [-HostedService <String>]
 -RdpCredential <PSCredential> -RdpAccessExpiry <DateTime> [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>]
 -Location <String> -Name <String> [-Subscription <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6f230-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6f230-105">DESCRIPTION</span></span>
<span data-ttu-id="6f230-106">Diese Version von Azure PowerShell-HDInsight ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="6f230-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="6f230-107">Diese Cmdlets werden vom 1. Januar 2017 entfernt.</span><span class="sxs-lookup"><span data-stu-id="6f230-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="6f230-108">Verwenden Sie bitte die neuere Version von Azure PowerShell-HDInsight.</span><span class="sxs-lookup"><span data-stu-id="6f230-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="6f230-109">Informationen zum Verwenden des neuen HDInsight zum Erstellen eines Clusters finden Sie unter [Erstellen von Linux-basierten Clustern in HDInsight mithilfe von Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="6f230-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="6f230-110">Informationen zum Übermitteln von Aufträgen mithilfe von Azure PowerShell und anderen Ansätzen finden Sie unter über [Mitteln von Hadoop-Aufträgen in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="6f230-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="6f230-111">Referenzinformationen zu Azure PowerShell-HDInsight finden Sie unter [Azure HDInsight-Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="6f230-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="6f230-112">Das Cmdlet **Grant-AzureHDInsightRdpAccess** gewährt Remote Desktop Protokoll (RDP) Zugriff auf einen Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="6f230-112">The **Grant-AzureHDInsightRdpAccess** cmdlet grants Remote Desktop Protocol (RDP) access to an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="6f230-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6f230-113">EXAMPLES</span></span>

## <span data-ttu-id="6f230-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f230-114">PARAMETERS</span></span>

### <span data-ttu-id="6f230-115">-Zertifikat</span><span class="sxs-lookup"><span data-stu-id="6f230-115">-Certificate</span></span>
<span data-ttu-id="6f230-116">Gibt das Verwaltungszertifikat für ein Azure-Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="6f230-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="6f230-117">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="6f230-117">-Endpoint</span></span>
<span data-ttu-id="6f230-118">Gibt den Endpunkt an, mit dem eine Verbindung mit Azure hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6f230-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="6f230-119">Wenn Sie diesen Parameter nicht angeben, verwendet dieses Cmdlet den Standardendpunkt.</span><span class="sxs-lookup"><span data-stu-id="6f230-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="6f230-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="6f230-120">-HostedService</span></span>
<span data-ttu-id="6f230-121">Gibt den Namespace eines HDInsight-Diensts an.</span><span class="sxs-lookup"><span data-stu-id="6f230-121">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="6f230-122">Wenn Sie diesen Parameter nicht angeben, verwendet dieses Cmdlet den Standardnamespace.</span><span class="sxs-lookup"><span data-stu-id="6f230-122">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="6f230-123">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="6f230-123">-IgnoreSslErrors</span></span>
<span data-ttu-id="6f230-124">Gibt an, ob SSL-Fehler (Secure Sockets Layer) ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="6f230-124">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="6f230-125">-Standort</span><span class="sxs-lookup"><span data-stu-id="6f230-125">-Location</span></span>
<span data-ttu-id="6f230-126">Gibt den Azure-Bereich an, in dem sich ein Cluster befindet.</span><span class="sxs-lookup"><span data-stu-id="6f230-126">Specifies the Azure region in which a cluster is located.</span></span>

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

### <span data-ttu-id="6f230-127">-Name</span><span class="sxs-lookup"><span data-stu-id="6f230-127">-Name</span></span>
<span data-ttu-id="6f230-128">Gibt den Namen eines Azure HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="6f230-128">Specifies the name of an Azure HDInsight cluster.</span></span>

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

### <span data-ttu-id="6f230-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="6f230-129">-Profile</span></span>
<span data-ttu-id="6f230-130">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="6f230-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6f230-131">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="6f230-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6f230-132">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="6f230-132">-RdpAccessExpiry</span></span>
<span data-ttu-id="6f230-133">Gibt den Ablauf als **DateTime** -Objekt für den Zugriff auf einen Cluster mit Remote Desktop Protokoll (RDP) an.</span><span class="sxs-lookup"><span data-stu-id="6f230-133">Specifies the expiration, as a **DateTime** object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f230-134">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="6f230-134">-RdpCredential</span></span>
<span data-ttu-id="6f230-135">Gibt die Anmeldeinformationen für den RDP-Zugriff auf einen Cluster an.</span><span class="sxs-lookup"><span data-stu-id="6f230-135">Specifies the credentials for RDP access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f230-136">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="6f230-136">-Subscription</span></span>
<span data-ttu-id="6f230-137">Gibt das Abonnement an, das den HDInsight-Cluster enthält, dem Sie den Zugriff gewähren möchten.</span><span class="sxs-lookup"><span data-stu-id="6f230-137">Specifies the subscription that contains the HDInsight cluster to which to grant access.</span></span>

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

### <span data-ttu-id="6f230-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f230-138">CommonParameters</span></span>
<span data-ttu-id="6f230-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f230-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f230-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f230-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f230-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6f230-141">INPUTS</span></span>

## <span data-ttu-id="6f230-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6f230-142">OUTPUTS</span></span>

## <span data-ttu-id="6f230-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="6f230-143">NOTES</span></span>

## <span data-ttu-id="6f230-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6f230-144">RELATED LINKS</span></span>

[<span data-ttu-id="6f230-145">REVOKE-AzureHdinsightRdpAccess</span><span class="sxs-lookup"><span data-stu-id="6f230-145">Revoke-AzureHdinsightRdpAccess</span></span>](./Revoke-AzureHdinsightRdpAccess.md)


