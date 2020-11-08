---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3EDD612F-AC5D-4D4D-BB14-2FB8DE5EDCCE
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4652cb1b30717b5ea11d596646dc43e2a5ec4a0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006129"
---
# <span data-ttu-id="bdf4b-101">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="bdf4b-101">New-AzureHDInsightCluster</span></span>

## <span data-ttu-id="bdf4b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bdf4b-102">SYNOPSIS</span></span>
<span data-ttu-id="bdf4b-103">Erstellt einen HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-103">Creates an HDInsight cluster.</span></span>

## <span data-ttu-id="bdf4b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdf4b-104">SYNTAX</span></span>

### <span data-ttu-id="bdf4b-105">Cluster nach config (mit bestimmten Anmeldeinformationen für Abonnements) (Standard)</span><span class="sxs-lookup"><span data-stu-id="bdf4b-105">Cluster By Config (with Specific Subscription Credential) (Default)</span></span>
```
New-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>]
 -Config <AzureHDInsightConfig> -Credential <PSCredential> [-EndPoint <Uri>] [-IgnoreSslErrors <Boolean>]
 -Location <String> -Name <String> [-Subscription <String>] [-Version <String>] [-OSType <OSType>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bdf4b-106">Cluster nach Name (mit bestimmten Anmeldeinformationen für Abonnements)</span><span class="sxs-lookup"><span data-stu-id="bdf4b-106">Cluster By Name (with Specific Subscription Credential)</span></span>
```
New-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>]
 -ClusterSizeInNodes <Int32> -Credential <PSCredential> -DefaultStorageAccountKey <String>
 -DefaultStorageAccountName <String> -DefaultStorageContainerName <String> [-EndPoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Location <String> -Name <String> [-Subscription <String>] [-Version <String>]
 [-HeadNodeVMSize <String>] [-ClusterType <ClusterType>] [-VirtualNetworkId <String>] [-SubnetName <String>]
 [-DataNodeVMSize <String>] [-ZookeeperNodeVMSize <String>] [-OSType <OSType>] [-SshCredential <PSCredential>]
 [-SshPublicKey <String>] [-RdpCredential <PSCredential>] [-RdpAccessExpiry <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bdf4b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bdf4b-107">DESCRIPTION</span></span>
<span data-ttu-id="bdf4b-108">Diese Version von Azure PowerShell-HDInsight ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="bdf4b-109">Diese Cmdlets werden vom 1. Januar 2017 entfernt.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="bdf4b-110">Verwenden Sie bitte die neuere Version von Azure PowerShell-HDInsight.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="bdf4b-111">Informationen zum Verwenden des neuen HDInsight zum Erstellen eines Clusters finden Sie unter [Erstellen von Linux-basierten Clustern in HDInsight mithilfe von Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="bdf4b-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="bdf4b-112">Informationen zum Übermitteln von Aufträgen mithilfe von Azure PowerShell und anderen Ansätzen finden Sie unter über [Mitteln von Hadoop-Aufträgen in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="bdf4b-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="bdf4b-113">Referenzinformationen zu Azure PowerShell-HDInsight finden Sie unter [Azure HDInsight-Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="bdf4b-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="bdf4b-114">Mit dem Cmdlet **New-AzureHDInsightCluster** wird ein Azure HDInsight-Cluster mithilfe der angegebenen Parameter oder mithilfe eines Konfigurationsobjekts erstellt, das mit dem Cmdlet **New-AzureHDInsightClusterConfig** erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-114">The **New-AzureHDInsightCluster** cmdlet creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the **New-AzureHDInsightClusterConfig** cmdlet.</span></span>

## <span data-ttu-id="bdf4b-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bdf4b-115">EXAMPLES</span></span>

### <span data-ttu-id="bdf4b-116">Beispiel 1: Erstellen eines HDInsight-Clusters</span><span class="sxs-lookup"><span data-stu-id="bdf4b-116">Example 1: Create an HDInsight cluster</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $Key1 = Get-AzureStorageKey -StorageAccountName "MyBlobStorage" | %{ $_.Primary }
PS C:\> $Key2 = Get-AzureStorageKey -StorageAccountName "MySecondBlobStorage" | %{ $_.Primary }
PS C:\> $Creds = Get-Credential
PS C:\> $OozieCreds = Get-Credential
PS C:\> $HiveCreds = Get-Credential 
PS C:\> New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
    | Set-AzureHDInsightDefaultStorage -StorageAccountName "MyBlobStorage.blob.core.windows.net" -StorageAccountKey $Key1 -StorageContainerName "MyContainer" 
    | Add-AzureHDInsightStorage -StorageAccountName "MySecondBlobStorage.blob.core.windows.net" -StorageAccountKey $Key2 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds
```

<span data-ttu-id="bdf4b-117">In diesem Beispiel wird ein HDInsight-Cluster für das aktuelle Abonnement erstellt.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-117">This example creates an HDInsight cluster for the current subscription.</span></span>

<span data-ttu-id="bdf4b-118">Der erste Befehl verwendet das Cmdlet " **Get-AzureSubscription** ", um die aktuelle Abonnement-ID abzurufen, und speichert Sie dann in der $SubId-Variablen.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-118">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="bdf4b-119">Der zweite und der dritte Befehl verwenden das Cmdlet " **Get-AzureStorageKey** ", um die primären Speicherschlüssel für MyBlobStorage und MySecondBlobStorage abzurufen, und speichern Sie dann die Schlüssel in den Variablen $Key 1 und $Key 2.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-119">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="bdf4b-120">Der vierte, fünfte und sechste Befehl verwenden Sie das Cmdlet **Get-Credential** , um Anmeldeinformationen für das aktuelle Abonnement sowie für Oozie und Hive abzurufen, und speichern Sie dann die Anmeldeinformationen in Variablen.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-120">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="bdf4b-121">Der endgültige Befehl führt eine Abfolge von Vorgängen mithilfe dieser Cmdlets aus:</span><span class="sxs-lookup"><span data-stu-id="bdf4b-121">The final command performs a sequence of operations by using these cmdlets:</span></span>

- <span data-ttu-id="bdf4b-122">**New-AzureHDInsightClusterConfig** zum Erstellen einer HDInsight-Cluster Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-122">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="bdf4b-123">**Legen Sie AzureHDInsightDefaultStorage** , um das Standardspeicher Konto für die Konfiguration auf MyBlobStorage.BLOB.Core.Windows.net zu legen.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-123">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="bdf4b-124">**Add-AzureHDInsightStorage** , um der Konfiguration ein zweites Speicherkonto mit dem Namen MySecondBlobStorage.BLOB.Core.Windows.net hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-124">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="bdf4b-125">**Add-AzureHDInsightMetastore** , um der Konfiguration einen metastore für Oozie und einen metastore für Hive hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-125">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="bdf4b-126">**New-AzureHDInsightCluster** zum Erstellen eines HDInsight-Clusters mit der neuen Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-126">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="bdf4b-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="bdf4b-127">PARAMETERS</span></span>

### <span data-ttu-id="bdf4b-128">-Zertifikat</span><span class="sxs-lookup"><span data-stu-id="bdf4b-128">-Certificate</span></span>
<span data-ttu-id="bdf4b-129">Gibt das Verwaltungszertifikat für ein Azure-Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-129">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="bdf4b-130">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="bdf4b-130">-ClusterSizeInNodes</span></span>
<span data-ttu-id="bdf4b-131">Gibt die Anzahl der Datenknoten an, die für einen Cluster erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-131">Specifies the number of data nodes to create for a cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: Nodes, Size

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf4b-132">-Clustertyp</span><span class="sxs-lookup"><span data-stu-id="bdf4b-132">-ClusterType</span></span>
<span data-ttu-id="bdf4b-133">Gibt den Typ des zu erstellende Clusters an.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-133">Specifies the type of cluster to create.</span></span>

```yaml
Type: ClusterType
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf4b-134">-Config</span><span class="sxs-lookup"><span data-stu-id="bdf4b-134">-Config</span></span>
<span data-ttu-id="bdf4b-135">Gibt ein Configuration-Objekt an, das mit dem Cmdlet **New-AzureHDInsightClusterConfig** erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-135">Specifies a configuration object that is created by using the **New-AzureHDInsightClusterConfig** cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: Cluster By Config (with Specific Subscription Credential)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdf4b-136">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="bdf4b-136">-Credential</span></span>
<span data-ttu-id="bdf4b-137">Gibt die Benutzeranmeldeinformationen an, die HDInsight für das Standardkonto verwenden soll, das für den Remotezugriff auf einen Hadoop-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-137">Specifies the user credentials for HDInsight to use for the default account that is used to remotely access a Hadoop cluster.</span></span>
<span data-ttu-id="bdf4b-138">Diese Anmeldeinformationen unterscheiden sich von den Abonnement Anmeldeinformationen des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-138">These credentials are distinct from the subscription credentials of the user.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: Cred

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf4b-139">-DataNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="bdf4b-139">-DataNodeVMSize</span></span>
<span data-ttu-id="bdf4b-140">Gibt die Größe des virtuellen Computers für den Datenknoten an.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-140">Specifies the size of the virtual machine for the data node.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf4b-141">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="bdf4b-141">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="bdf4b-142">Gibt den Kontoschlüssel für das Standardspeicher Konto an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-142">Specifies the account key for the default storage account that the HDInsight cluster uses.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf4b-143">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bdf4b-143">-DefaultStorageAccountName</span></span>
<span data-ttu-id="bdf4b-144">Gibt den Namen des Standardspeicher Kontos an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-144">Specifies the name of the default storage account that the HDInsight cluster uses.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf4b-145">-DefaultStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="bdf4b-145">-DefaultStorageContainerName</span></span>
<span data-ttu-id="bdf4b-146">Gibt den Namen des Standardcontainers im standardmäßigen Azure Storage-Konto an, das ein HDInsight-Cluster verwendet.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-146">Specifies the name of the default container in the default Azure storage account that an HDInsight cluster uses.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf4b-147">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="bdf4b-147">-EndPoint</span></span>
<span data-ttu-id="bdf4b-148">Gibt den Endpunkt an, mit dem eine Verbindung mit Azure hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-148">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="bdf4b-149">Wenn Sie diesen Parameter nicht angeben, verwendet dieses Cmdlet den Standardendpunkt.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-149">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="bdf4b-150">-HeadNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="bdf4b-150">-HeadNodeVMSize</span></span>
<span data-ttu-id="bdf4b-151">Gibt die Größe des virtuellen Computers für den Head-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-151">Specifies the size of the virtual machine for the head node.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf4b-152">-HostedService</span><span class="sxs-lookup"><span data-stu-id="bdf4b-152">-HostedService</span></span>
<span data-ttu-id="bdf4b-153">Gibt den Namespace eines HDInsight-Diensts an.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-153">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="bdf4b-154">Wenn Sie diesen Parameter nicht angeben, verwendet dieses Cmdlet den Standardnamespace.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-154">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="bdf4b-155">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="bdf4b-155">-IgnoreSslErrors</span></span>
<span data-ttu-id="bdf4b-156">Gibt an, ob SSL-Fehler (Secure Sockets Layer) ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-156">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="bdf4b-157">-Standort</span><span class="sxs-lookup"><span data-stu-id="bdf4b-157">-Location</span></span>
<span data-ttu-id="bdf4b-158">Gibt den Bereich an, in dem ein HDInsight-Cluster erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-158">Specifies the region in which to create an HDInsight cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Loc

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf4b-159">-Name</span><span class="sxs-lookup"><span data-stu-id="bdf4b-159">-Name</span></span>
<span data-ttu-id="bdf4b-160">Gibt den Namen des Azure HDInsight-Clusters an, den Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-160">Specifies the name of the Azure HDInsight cluster to create.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Config (with Specific Subscription Credential)
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

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf4b-161">-OSType</span><span class="sxs-lookup"><span data-stu-id="bdf4b-161">-OSType</span></span>
<span data-ttu-id="bdf4b-162">Gibt das Betriebssystem für einen Cluster an.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-162">Specifies the operating system for a cluster.</span></span>

```yaml
Type: OSType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf4b-163">-Profil</span><span class="sxs-lookup"><span data-stu-id="bdf4b-163">-Profile</span></span>
<span data-ttu-id="bdf4b-164">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-164">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bdf4b-165">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-165">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bdf4b-166">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="bdf4b-166">-RdpAccessExpiry</span></span>
<span data-ttu-id="bdf4b-167">Gibt den Ablauf als **DateTime** -Objekt für den Zugriff auf einen Cluster mit Remote Desktop Protokoll (RDP) an.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-167">Specifies the expiration, as a **DateTime** object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf4b-168">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="bdf4b-168">-RdpCredential</span></span>
<span data-ttu-id="bdf4b-169">Gibt die Anmeldeinformationen für den RDP-Zugriff auf einen Cluster an.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-169">Specifies the credentials for RDP access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf4b-170">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="bdf4b-170">-SshCredential</span></span>
<span data-ttu-id="bdf4b-171">Gibt den Benutzernamen und das Kennwort für Secure Shell (SSH) für den HDInsight-Cluster an.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-171">Specifies the Secure Shell (SSH) user name and password for the HDInsight cluster.</span></span>
<span data-ttu-id="bdf4b-172">Dieser Parameter ist nur für Linux-Cluster gültig.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-172">This parameter is valid only for Linux clusters.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf4b-173">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="bdf4b-173">-SshPublicKey</span></span>
<span data-ttu-id="bdf4b-174">Gibt den öffentlichen SSH-Schlüssel für einen HDInsight-Cluster an.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-174">Specifies the SSH public key for an HDInsight cluster.</span></span>
<span data-ttu-id="bdf4b-175">Dieser Parameter ist nur für Linux-Cluster gültig.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-175">This parameter is valid only for Linux clusters.</span></span>

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

### <span data-ttu-id="bdf4b-176">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="bdf4b-176">-SubnetName</span></span>
<span data-ttu-id="bdf4b-177">Gibt den Namen eines Subnetzes an.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-177">Specifies the name of a subnet.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf4b-178">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="bdf4b-178">-Subscription</span></span>
<span data-ttu-id="bdf4b-179">Gibt das Azure-Abonnement an, in dem ein HDInsight-Cluster erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-179">Specifies the Azure subscription in which to create an HDInsight cluster.</span></span>

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

### <span data-ttu-id="bdf4b-180">-Version</span><span class="sxs-lookup"><span data-stu-id="bdf4b-180">-Version</span></span>
<span data-ttu-id="bdf4b-181">Gibt die HDInsight-Clusterversion an, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-181">Specifies the HDInsight cluster version to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Ver

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf4b-182">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="bdf4b-182">-VirtualNetworkId</span></span>
<span data-ttu-id="bdf4b-183">Gibt die ID des virtuellen Netzwerks an, in das der Cluster bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-183">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf4b-184">-ZookeeperNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="bdf4b-184">-ZookeeperNodeVMSize</span></span>
<span data-ttu-id="bdf4b-185">Gibt die Größe des virtuellen Computers für den zoowärter-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-185">Specifies the size of the virtual machine for the ZooKeeper node.</span></span>
<span data-ttu-id="bdf4b-186">Dieser Parameter ist nur für HBAs oder Storm-Cluster gültig.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-186">This parameter is valid only for HBase or Storm clusters.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf4b-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdf4b-187">CommonParameters</span></span>
<span data-ttu-id="bdf4b-188">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdf4b-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdf4b-189">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdf4b-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdf4b-190">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bdf4b-190">INPUTS</span></span>

## <span data-ttu-id="bdf4b-191">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bdf4b-191">OUTPUTS</span></span>

## <span data-ttu-id="bdf4b-192">Notizen</span><span class="sxs-lookup"><span data-stu-id="bdf4b-192">NOTES</span></span>

## <span data-ttu-id="bdf4b-193">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bdf4b-193">RELATED LINKS</span></span>

[<span data-ttu-id="bdf4b-194">Add-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="bdf4b-194">Add-AzureHDInsightMetastore</span></span>](./Add-AzureHDInsightMetastore.md)

[<span data-ttu-id="bdf4b-195">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="bdf4b-195">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="bdf4b-196">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="bdf4b-196">Get-AzureHDInsightCluster</span></span>](./Get-AzureHDInsightCluster.md)

[<span data-ttu-id="bdf4b-197">Neu – AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="bdf4b-197">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="bdf4b-198">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="bdf4b-198">Remove-AzureHDInsightCluster</span></span>](./Remove-AzureHDInsightCluster.md)

[<span data-ttu-id="bdf4b-199">Satz-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="bdf4b-199">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)

[<span data-ttu-id="bdf4b-200">Verwenden von-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="bdf4b-200">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


