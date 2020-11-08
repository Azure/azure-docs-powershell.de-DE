---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 7D73D37B-17EE-4FF8-9A21-D2014D5417D6
online version: ''
schema: 2.0.0
ms.openlocfilehash: fa779907648ca8e8e1288394d562c86b6102d9ca
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006682"
---
# <span data-ttu-id="f104f-101">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f104f-101">Remove-AzureHDInsightCluster</span></span>

## <span data-ttu-id="f104f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f104f-102">SYNOPSIS</span></span>
<span data-ttu-id="f104f-103">Löscht einen HDInsight-Cluster aus einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f104f-103">Deletes an HDInsight cluster from a subscription.</span></span>

## <span data-ttu-id="f104f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f104f-104">SYNTAX</span></span>

```
Remove-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Name <String> [-Subscription <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="f104f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f104f-105">DESCRIPTION</span></span>
<span data-ttu-id="f104f-106">Diese Version von Azure PowerShell-HDInsight ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="f104f-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="f104f-107">Diese Cmdlets werden vom 1. Januar 2017 entfernt.</span><span class="sxs-lookup"><span data-stu-id="f104f-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="f104f-108">Verwenden Sie bitte die neuere Version von Azure PowerShell-HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f104f-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="f104f-109">Informationen zum Verwenden des neuen HDInsight zum Erstellen eines Clusters finden Sie unter [Erstellen von Linux-basierten Clustern in HDInsight mithilfe von Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="f104f-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="f104f-110">Informationen zum Übermitteln von Aufträgen mithilfe von Azure PowerShell und anderen Ansätzen finden Sie unter über [Mitteln von Hadoop-Aufträgen in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="f104f-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="f104f-111">Referenzinformationen zu Azure PowerShell-HDInsight finden Sie unter [Azure HDInsight-Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f104f-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="f104f-112">Das Cmdlet **Remove-AzureHDInsightCluster** löscht den angegebenen HDInsight-Dienst Cluster aus einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f104f-112">The **Remove-AzureHDInsightCluster** cmdlet deletes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="f104f-113">Dieser Vorgang löscht auch alle Daten, die im Hadoop Distributed File System (HDFS) auf dem Cluster gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="f104f-113">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="f104f-114">Im zugeordneten Azure Storage-Konto gespeicherte Daten werden nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f104f-114">Data stored in the associated Azure Storage account is not deleted.</span></span>

## <span data-ttu-id="f104f-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f104f-115">EXAMPLES</span></span>

### <span data-ttu-id="f104f-116">Beispiel 1: Entfernen eines Clusters</span><span class="sxs-lookup"><span data-stu-id="f104f-116">Example 1: Remove a cluster</span></span>
```
PS C:\>Remove-AzureHDInsightCluster -Name "HDICluster"
```

<span data-ttu-id="f104f-117">Dieser Befehl löscht den HDInsight-Cluster mit dem Namen HDICluster.</span><span class="sxs-lookup"><span data-stu-id="f104f-117">This command deletes the HDInsight cluster named HDICluster.</span></span>

## <span data-ttu-id="f104f-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="f104f-118">PARAMETERS</span></span>

### <span data-ttu-id="f104f-119">-Zertifikat</span><span class="sxs-lookup"><span data-stu-id="f104f-119">-Certificate</span></span>
<span data-ttu-id="f104f-120">Gibt das Verwaltungszertifikat für ein Azure-Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="f104f-120">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="f104f-121">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="f104f-121">-Endpoint</span></span>
<span data-ttu-id="f104f-122">Gibt den Endpunkt an, mit dem eine Verbindung mit Azure hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f104f-122">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="f104f-123">Wenn Sie diesen Parameter nicht angeben, verwendet dieses Cmdlet den Standardendpunkt.</span><span class="sxs-lookup"><span data-stu-id="f104f-123">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="f104f-124">-HostedService</span><span class="sxs-lookup"><span data-stu-id="f104f-124">-HostedService</span></span>
<span data-ttu-id="f104f-125">Gibt den Namespace eines HDInsight-Diensts an, wenn Sie den Standardnamespace nicht verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="f104f-125">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

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

### <span data-ttu-id="f104f-126">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="f104f-126">-IgnoreSslErrors</span></span>
<span data-ttu-id="f104f-127">Gibt an, ob SSL-Fehler (Secure Sockets Layer) ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="f104f-127">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="f104f-128">-Name</span><span class="sxs-lookup"><span data-stu-id="f104f-128">-Name</span></span>
<span data-ttu-id="f104f-129">Gibt den Namen des zu entfernenden HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="f104f-129">Specifies the name of the HDInsight cluster to remove.</span></span>

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

### <span data-ttu-id="f104f-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="f104f-130">-Profile</span></span>
<span data-ttu-id="f104f-131">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="f104f-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f104f-132">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="f104f-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f104f-133">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="f104f-133">-Subscription</span></span>
<span data-ttu-id="f104f-134">Gibt das Abonnementkonto an, das den zu entfernenden HDInsight-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="f104f-134">Specifies the subscription account that contains the HDInsight cluster to remove.</span></span>

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

### <span data-ttu-id="f104f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f104f-135">CommonParameters</span></span>
<span data-ttu-id="f104f-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f104f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f104f-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f104f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f104f-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f104f-138">INPUTS</span></span>

## <span data-ttu-id="f104f-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f104f-139">OUTPUTS</span></span>

## <span data-ttu-id="f104f-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="f104f-140">NOTES</span></span>

## <span data-ttu-id="f104f-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f104f-141">RELATED LINKS</span></span>

[<span data-ttu-id="f104f-142">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f104f-142">Get-AzureHDInsightCluster</span></span>](./Get-AzureHDInsightCluster.md)

[<span data-ttu-id="f104f-143">Neu – AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f104f-143">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="f104f-144">Verwenden von-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f104f-144">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


