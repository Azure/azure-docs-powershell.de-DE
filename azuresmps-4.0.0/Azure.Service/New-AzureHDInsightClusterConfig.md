---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: FF8AA7DE-1E0F-4F5B-95F6-7820AAF789F2
online version: ''
schema: 2.0.0
ms.openlocfilehash: c36931af0b6927ef4fee26b9f8ade7db77d17db2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006126"
---
# <span data-ttu-id="07d7d-101">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="07d7d-101">New-AzureHDInsightClusterConfig</span></span>

## <span data-ttu-id="07d7d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="07d7d-102">SYNOPSIS</span></span>
<span data-ttu-id="07d7d-103">Erstellt eine nicht persistente HDInsight-Cluster Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="07d7d-103">Creates a non-persisted HDInsight cluster configuration.</span></span>

## <span data-ttu-id="07d7d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="07d7d-104">SYNTAX</span></span>

```
New-AzureHDInsightClusterConfig -ClusterSizeInNodes <Int32> [-HeadNodeVMSize <String>]
 [-ClusterType <ClusterType>] [-VirtualNetworkId <String>] [-SubnetName <String>] [-DataNodeVMSize <String>]
 [-ZookeeperNodeVMSize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="07d7d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07d7d-105">DESCRIPTION</span></span>
<span data-ttu-id="07d7d-106">Diese Version von Azure PowerShell-HDInsight ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="07d7d-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="07d7d-107">Diese Cmdlets werden vom 1. Januar 2017 entfernt.</span><span class="sxs-lookup"><span data-stu-id="07d7d-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="07d7d-108">Verwenden Sie bitte die neuere Version von Azure PowerShell-HDInsight.</span><span class="sxs-lookup"><span data-stu-id="07d7d-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="07d7d-109">Informationen zum Verwenden des neuen HDInsight zum Erstellen eines Clusters finden Sie unter [Erstellen von Linux-basierten Clustern in HDInsight mithilfe von Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="07d7d-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="07d7d-110">Informationen zum Übermitteln von Aufträgen mithilfe von Azure PowerShell und anderen Ansätzen finden Sie unter über [Mitteln von Hadoop-Aufträgen in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="07d7d-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="07d7d-111">Referenzinformationen zu Azure PowerShell-HDInsight finden Sie unter [Azure HDInsight-Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="07d7d-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="07d7d-112">Das Cmdlet **New-AzureHDInsightClusterConfig** erstellt eine nicht persistente Azure HDInsight-Cluster Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="07d7d-112">The **New-AzureHDInsightClusterConfig** cmdlet creates a non-persisted Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="07d7d-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="07d7d-113">EXAMPLES</span></span>

### <span data-ttu-id="07d7d-114">Beispiel 1: Erstellen einer Cluster Konfiguration</span><span class="sxs-lookup"><span data-stu-id="07d7d-114">Example 1: Create a cluster configuration</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $Key1 = Get-AzureStorageKey -StorageAccountName "MyBlobStorage" | %{ $_.Primary }
PS C:\> $Key2 = Get-AzureStorageKey -StorageAccountName "MySecondBlobStorage" | %{ $_.Primary }
PS C:\> $Creds = Get-Credential
PS C:\> $OozieCreds = Get-Credential
PS C:\> $HiveCreds = Get-Credential
PS C:\> New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
    | Set-AzureHDInsightDefaultStorage -StorageAccountName MyBlobStorage.blob.core.windows.net -StorageAccountKey $Key1 -StorageContainerName "MyContainer" 
    | Add-AzureHDInsightStorage -StorageAccountName "MySecondBlobStorage.blob.core.windows.net" -StorageAccountKey $Key2 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.widows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubID -Credential $Creds
```

<span data-ttu-id="07d7d-115">Der erste Befehl verwendet das Cmdlet " **Get-AzureSubscription** ", um die aktuelle Abonnement-ID abzurufen, und speichert Sie dann in der $SubId-Variablen.</span><span class="sxs-lookup"><span data-stu-id="07d7d-115">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="07d7d-116">Der zweite und der dritte Befehl verwenden das Cmdlet " **Get-AzureStorageKey** ", um die primären Speicherschlüssel für MyBlobStorage und MySecondBlobStorage abzurufen, und speichern Sie dann die Schlüssel in den Variablen $Key 1 und $Key 2.</span><span class="sxs-lookup"><span data-stu-id="07d7d-116">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="07d7d-117">Der vierte, fünfte und sechste Befehl verwenden Sie das Cmdlet **Get-Credential** , um Anmeldeinformationen für das aktuelle Abonnement sowie für Oozie und Hive abzurufen, und speichern Sie dann die Anmeldeinformationen in Variablen.</span><span class="sxs-lookup"><span data-stu-id="07d7d-117">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="07d7d-118">Der endgültige Befehl führt eine Abfolge von Vorgängen mithilfe dieser Cmdlets aus:</span><span class="sxs-lookup"><span data-stu-id="07d7d-118">The final command performs a sequence of operations by using these cmdlets:</span></span> 

- <span data-ttu-id="07d7d-119">**New-AzureHDInsightClusterConfig** zum Erstellen einer HDInsight-Cluster Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="07d7d-119">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="07d7d-120">**Legen Sie AzureHDInsightDefaultStorage** , um das Standardspeicher Konto für die Konfiguration auf MyBlobStorage.BLOB.Core.Windows.net zu legen.</span><span class="sxs-lookup"><span data-stu-id="07d7d-120">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="07d7d-121">**Add-AzureHDInsightStorage** , um der Konfiguration ein zweites Speicherkonto mit dem Namen MySecondBlobStorage.BLOB.Core.Windows.net hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="07d7d-121">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="07d7d-122">**Add-AzureHDInsightMetastore** , um der Konfiguration einen metastore für Oozie und einen metastore für Hive hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="07d7d-122">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="07d7d-123">**New-AzureHDInsightCluster** zum Erstellen eines HDInsight-Clusters mit der neuen Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="07d7d-123">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="07d7d-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="07d7d-124">PARAMETERS</span></span>

### <span data-ttu-id="07d7d-125">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="07d7d-125">-ClusterSizeInNodes</span></span>
<span data-ttu-id="07d7d-126">Gibt die Anzahl der Datenknoten an, die für einen Cluster erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="07d7d-126">Specifies the number of data nodes to create for a cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Nodes, Size

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07d7d-127">-Clustertyp</span><span class="sxs-lookup"><span data-stu-id="07d7d-127">-ClusterType</span></span>
<span data-ttu-id="07d7d-128">Gibt den Typ des zu erstellende Clusters an.</span><span class="sxs-lookup"><span data-stu-id="07d7d-128">Specifies the type of cluster to create.</span></span>

```yaml
Type: ClusterType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07d7d-129">-DataNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="07d7d-129">-DataNodeVMSize</span></span>
<span data-ttu-id="07d7d-130">Gibt die Größe des virtuellen Computers für den Datenknoten an.</span><span class="sxs-lookup"><span data-stu-id="07d7d-130">Specifies the size of the virtual machine for the data node.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07d7d-131">-HeadNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="07d7d-131">-HeadNodeVMSize</span></span>
<span data-ttu-id="07d7d-132">Gibt die Größe des virtuellen Computers des Head-Knotens für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="07d7d-132">Specifies the virtual machine size of the head node for the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07d7d-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="07d7d-133">-Profile</span></span>
<span data-ttu-id="07d7d-134">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="07d7d-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="07d7d-135">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="07d7d-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="07d7d-136">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="07d7d-136">-SubnetName</span></span>
<span data-ttu-id="07d7d-137">Gibt den Namen eines Subnetzes an.</span><span class="sxs-lookup"><span data-stu-id="07d7d-137">Specifies the name of a subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07d7d-138">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="07d7d-138">-VirtualNetworkId</span></span>
<span data-ttu-id="07d7d-139">Gibt die ID des virtuellen Netzwerks an, in das der Cluster bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="07d7d-139">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07d7d-140">-ZookeeperNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="07d7d-140">-ZookeeperNodeVMSize</span></span>
<span data-ttu-id="07d7d-141">Gibt die Größe des virtuellen Computers für den zoowärter-Knoten für einen HBAs oder Storm-Cluster an.</span><span class="sxs-lookup"><span data-stu-id="07d7d-141">Specifies the size of the virtual machine for the ZooKeeper node for an HBase or Storm cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07d7d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07d7d-142">CommonParameters</span></span>
<span data-ttu-id="07d7d-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07d7d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07d7d-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07d7d-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07d7d-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="07d7d-145">INPUTS</span></span>

## <span data-ttu-id="07d7d-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="07d7d-146">OUTPUTS</span></span>

## <span data-ttu-id="07d7d-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="07d7d-147">NOTES</span></span>

## <span data-ttu-id="07d7d-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="07d7d-148">RELATED LINKS</span></span>

[<span data-ttu-id="07d7d-149">Add-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="07d7d-149">Add-AzureHDInsightMetastore</span></span>](./Add-AzureHDInsightMetastore.md)

[<span data-ttu-id="07d7d-150">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="07d7d-150">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="07d7d-151">Neu – AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="07d7d-151">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="07d7d-152">Satz-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="07d7d-152">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)


