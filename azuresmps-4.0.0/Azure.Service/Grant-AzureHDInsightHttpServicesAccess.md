---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: E3D22B03-2997-4F2C-895E-AE0993FD7C92
online version: ''
schema: 2.0.0
ms.openlocfilehash: bfd3e1f2bb5d057dec8a7bee5929ba5c67c8d53d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006704"
---
# <span data-ttu-id="6decb-101">Grant-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6decb-101">Grant-AzureHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="6decb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6decb-102">SYNOPSIS</span></span>
<span data-ttu-id="6decb-103">Gewährt HTTP-Zugriff auf einen Cluster.</span><span class="sxs-lookup"><span data-stu-id="6decb-103">Grants HTTP access to a cluster.</span></span>

## <span data-ttu-id="6decb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6decb-104">SYNTAX</span></span>

```
Grant-AzureHDInsightHttpServicesAccess [-Certificate <X509Certificate2>] [-HostedService <String>]
 -Credential <PSCredential> [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -Location <String> -Name <String>
 [-Subscription <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6decb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6decb-105">DESCRIPTION</span></span>
<span data-ttu-id="6decb-106">Diese Version von Azure PowerShell-HDInsight ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="6decb-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="6decb-107">Diese Cmdlets werden vom 1. Januar 2017 entfernt.</span><span class="sxs-lookup"><span data-stu-id="6decb-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="6decb-108">Verwenden Sie bitte die neuere Version von Azure PowerShell-HDInsight.</span><span class="sxs-lookup"><span data-stu-id="6decb-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="6decb-109">Informationen zum Verwenden des neuen HDInsight zum Erstellen eines Clusters finden Sie unter [Erstellen von Linux-basierten Clustern in HDInsight mithilfe von Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="6decb-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="6decb-110">Informationen zum Übermitteln von Aufträgen mithilfe von Azure PowerShell und anderen Ansätzen finden Sie unter über [Mitteln von Hadoop-Aufträgen in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="6decb-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="6decb-111">Referenzinformationen zu Azure PowerShell-HDInsight finden Sie unter [Azure HDInsight-Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="6decb-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="6decb-112">Das Cmdlet **Grant-AzureHDInsightHttpServicesAccess** gewährt HTTP-Zugriff auf einen Azure HDInsight-Cluster mithilfe von ODBC, Ambari, Oozie und Webdiensten.</span><span class="sxs-lookup"><span data-stu-id="6decb-112">The **Grant-AzureHDInsightHttpServicesAccess** cmdlet grants HTTP access to an Azure HDInsight cluster using ODBC, Ambari, Oozie, and web services.</span></span>

## <span data-ttu-id="6decb-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6decb-113">EXAMPLES</span></span>

## <span data-ttu-id="6decb-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="6decb-114">PARAMETERS</span></span>

### <span data-ttu-id="6decb-115">-Zertifikat</span><span class="sxs-lookup"><span data-stu-id="6decb-115">-Certificate</span></span>
<span data-ttu-id="6decb-116">Gibt das Verwaltungszertifikat für ein Azure-Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="6decb-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="6decb-117">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="6decb-117">-Credential</span></span>
<span data-ttu-id="6decb-118">Gibt einen Benutzernamen und ein Kennwort für den HTTP-Zugriff an.</span><span class="sxs-lookup"><span data-stu-id="6decb-118">Specifies a user name and password for HTTP access.</span></span>

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

### <span data-ttu-id="6decb-119">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="6decb-119">-Endpoint</span></span>
<span data-ttu-id="6decb-120">Gibt den Endpunkt an, mit dem eine Verbindung mit Azure hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6decb-120">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="6decb-121">Wenn Sie diesen Parameter nicht angeben, verwendet dieses Cmdlet den Standardendpunkt.</span><span class="sxs-lookup"><span data-stu-id="6decb-121">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="6decb-122">-HostedService</span><span class="sxs-lookup"><span data-stu-id="6decb-122">-HostedService</span></span>
<span data-ttu-id="6decb-123">Gibt den Namespace eines HDInsight-Diensts an.</span><span class="sxs-lookup"><span data-stu-id="6decb-123">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="6decb-124">Wenn Sie diesen Parameter nicht angeben, verwendet dieses Cmdlet den Standardnamespace.</span><span class="sxs-lookup"><span data-stu-id="6decb-124">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="6decb-125">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="6decb-125">-IgnoreSslErrors</span></span>
<span data-ttu-id="6decb-126">Gibt an, ob SSL-Fehler (Secure Sockets Layer) ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="6decb-126">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="6decb-127">-Standort</span><span class="sxs-lookup"><span data-stu-id="6decb-127">-Location</span></span>
<span data-ttu-id="6decb-128">Gibt den Azure-Bereich an, in dem sich ein Cluster befindet.</span><span class="sxs-lookup"><span data-stu-id="6decb-128">Specifies the Azure region in which a cluster is located.</span></span>

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

### <span data-ttu-id="6decb-129">-Name</span><span class="sxs-lookup"><span data-stu-id="6decb-129">-Name</span></span>
<span data-ttu-id="6decb-130">Gibt den Namen eines Clusters an.</span><span class="sxs-lookup"><span data-stu-id="6decb-130">Specifies the name of a cluster.</span></span>
<span data-ttu-id="6decb-131">Dieses Cmdlet gewährt HTTP-Zugriff auf den Cluster, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="6decb-131">This cmdlet grants HTTP access to the cluster that this parameter specifies.</span></span>

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

### <span data-ttu-id="6decb-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="6decb-132">-Profile</span></span>
<span data-ttu-id="6decb-133">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="6decb-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6decb-134">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="6decb-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6decb-135">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="6decb-135">-Subscription</span></span>
<span data-ttu-id="6decb-136">Gibt das Abonnement an, das den HDInsight-Cluster enthält, dem Sie den Zugriff gewähren möchten.</span><span class="sxs-lookup"><span data-stu-id="6decb-136">Specifies the subscription that contains the HDInsight cluster to which to grant access.</span></span>

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

### <span data-ttu-id="6decb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6decb-137">CommonParameters</span></span>
<span data-ttu-id="6decb-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6decb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6decb-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6decb-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6decb-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6decb-140">INPUTS</span></span>

## <span data-ttu-id="6decb-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6decb-141">OUTPUTS</span></span>

## <span data-ttu-id="6decb-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="6decb-142">NOTES</span></span>

## <span data-ttu-id="6decb-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6decb-143">RELATED LINKS</span></span>

[<span data-ttu-id="6decb-144">REVOKE-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6decb-144">Revoke-AzureHDInsightHttpServicesAccess</span></span>](./Revoke-AzureHDInsightHttpServicesAccess.md)


