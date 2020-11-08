---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 771B7CB2-88F6-4FC5-9DB0-E623D231E51A
online version: ''
schema: 2.0.0
ms.openlocfilehash: bdbf7778ca2d7498d7f33586f7e9e50e0955c521
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006168"
---
# <span data-ttu-id="22813-101">Set-AzureHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="22813-101">Set-AzureHDInsightClusterSize</span></span>

## <span data-ttu-id="22813-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="22813-102">SYNOPSIS</span></span>
<span data-ttu-id="22813-103">Legt die Anzahl der Datenknoten für einen HDInsight-Cluster fest.</span><span class="sxs-lookup"><span data-stu-id="22813-103">Sets the number of data nodes for an HDInsight cluster.</span></span>

## <span data-ttu-id="22813-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="22813-104">SYNTAX</span></span>

### <span data-ttu-id="22813-105">Setzen Sie die Clustergröße in Knoten mit dem Namen.</span><span class="sxs-lookup"><span data-stu-id="22813-105">Set cluster size in nodes with name.</span></span>
```
Set-AzureHDInsightClusterSize -ClusterSizeInNodes <Int32> -Name <String> [-Force] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="22813-106">Setzen Sie die Clustergröße in Knoten mit Cluster aus Pipeline.</span><span class="sxs-lookup"><span data-stu-id="22813-106">Set cluster size in nodes with cluster from pipeline.</span></span>
```
Set-AzureHDInsightClusterSize -ClusterSizeInNodes <Int32> [-Force] -Cluster <AzureHDInsightCluster>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="22813-107">Cluster nach Name (mit bestimmten Anmeldeinformationen für Abonnements)</span><span class="sxs-lookup"><span data-stu-id="22813-107">Cluster By Name (with Specific Subscription Credential)</span></span>
```
Set-AzureHDInsightClusterSize [-Certificate <X509Certificate2>] [-Subscription <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="22813-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22813-108">DESCRIPTION</span></span>
<span data-ttu-id="22813-109">Diese Version von Azure PowerShell-HDInsight ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="22813-109">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="22813-110">Diese Cmdlets werden vom 1. Januar 2017 entfernt.</span><span class="sxs-lookup"><span data-stu-id="22813-110">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="22813-111">Verwenden Sie bitte die neuere Version von Azure PowerShell-HDInsight.</span><span class="sxs-lookup"><span data-stu-id="22813-111">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="22813-112">Informationen zum Verwenden des neuen HDInsight zum Erstellen eines Clusters finden Sie unter [Erstellen von Linux-basierten Clustern in HDInsight mithilfe von Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="22813-112">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="22813-113">Informationen zum Übermitteln von Aufträgen mithilfe von Azure PowerShell und anderen Ansätzen finden Sie unter über [Mitteln von Hadoop-Aufträgen in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="22813-113">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="22813-114">Referenzinformationen zu Azure PowerShell-HDInsight finden Sie unter [Azure HDInsight-Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="22813-114">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="22813-115">Das Cmdlet " **Set-AzureHDInsightClusterSize** " legt die Anzahl der Datenknoten für einen Azure HDInsight-Cluster fest.</span><span class="sxs-lookup"><span data-stu-id="22813-115">The **Set-AzureHDInsightClusterSize** cmdlet sets the number of data nodes for an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="22813-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="22813-116">EXAMPLES</span></span>

## <span data-ttu-id="22813-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="22813-117">PARAMETERS</span></span>

### <span data-ttu-id="22813-118">-Zertifikat</span><span class="sxs-lookup"><span data-stu-id="22813-118">-Certificate</span></span>
<span data-ttu-id="22813-119">Gibt das Verwaltungszertifikat für ein Azure-Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="22813-119">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22813-120">-Cluster</span><span class="sxs-lookup"><span data-stu-id="22813-120">-Cluster</span></span>
<span data-ttu-id="22813-121">Gibt den Cluster an, dessen Größe geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="22813-121">Specifies the cluster to resize.</span></span>

```yaml
Type: AzureHDInsightCluster
Parameter Sets: Set cluster size in nodes with cluster from pipeline.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22813-122">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="22813-122">-ClusterSizeInNodes</span></span>
<span data-ttu-id="22813-123">Gibt die Anzahl der Datenknoten an, die für einen Cluster erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="22813-123">Specifies the number of data nodes to create for a cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Set cluster size in nodes with name.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Int32
Parameter Sets: Set cluster size in nodes with cluster from pipeline.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22813-124">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="22813-124">-Endpoint</span></span>
<span data-ttu-id="22813-125">Gibt den Endpunkt an, mit dem eine Verbindung mit Azure hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="22813-125">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="22813-126">Wenn Sie diesen Parameter nicht angeben, verwendet dieses Cmdlet den Standardendpunkt.</span><span class="sxs-lookup"><span data-stu-id="22813-126">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22813-127">-Force</span><span class="sxs-lookup"><span data-stu-id="22813-127">-Force</span></span>
<span data-ttu-id="22813-128">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="22813-128">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Set cluster size in nodes with name., Set cluster size in nodes with cluster from pipeline.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22813-129">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="22813-129">-IgnoreSslErrors</span></span>
<span data-ttu-id="22813-130">Gibt an, ob SSL-Fehler (Secure Sockets Layer) ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="22813-130">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22813-131">-Name</span><span class="sxs-lookup"><span data-stu-id="22813-131">-Name</span></span>
<span data-ttu-id="22813-132">Gibt den Namen des HDInsight-Clusters an, dessen Größe geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="22813-132">Specifies the name of the HDInsight cluster to resize.</span></span>

```yaml
Type: String
Parameter Sets: Set cluster size in nodes with name.
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: ClusterName, DnsName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22813-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="22813-133">-Profile</span></span>
<span data-ttu-id="22813-134">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="22813-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="22813-135">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="22813-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="22813-136">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="22813-136">-Subscription</span></span>
<span data-ttu-id="22813-137">Gibt ein Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="22813-137">Specifies a subscription.</span></span>
<span data-ttu-id="22813-138">Mit diesem Cmdlet wird die Clustergröße für das Abonnement festgelegt, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="22813-138">This cmdlet sets the cluster size for the subscription that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22813-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22813-139">CommonParameters</span></span>
<span data-ttu-id="22813-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22813-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22813-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22813-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22813-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="22813-142">INPUTS</span></span>

## <span data-ttu-id="22813-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="22813-143">OUTPUTS</span></span>

## <span data-ttu-id="22813-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="22813-144">NOTES</span></span>

## <span data-ttu-id="22813-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="22813-145">RELATED LINKS</span></span>

