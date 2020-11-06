---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
ms.openlocfilehash: 2e778f84eabf7e5dc4dd325d2a17361064c5d99f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505514"
---
# <span data-ttu-id="00dc2-101">New-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="00dc2-101">New-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="00dc2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="00dc2-102">SYNOPSIS</span></span>
<span data-ttu-id="00dc2-103">Erstellt einen Azure HDInsight-Cluster in der angegebenen Ressourcengruppe für das aktuelle Abonnement.</span><span class="sxs-lookup"><span data-stu-id="00dc2-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00dc2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="00dc2-104">SYNTAX</span></span>

### <span data-ttu-id="00dc2-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="00dc2-105">Default (Default)</span></span>
```
New-AzureRmHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [-DefaultStorageAccountType <StorageType>]
 [-Config <AzureHDInsightConfig>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-DefaultStorageContainer <String>] [-DefaultStorageRootPath <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>]
 [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificatePassword <String>] [-AadTenantId <Guid>]
 [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DisksPerWorkerNode <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00dc2-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="00dc2-106">CertificateFilePath</span></span>
```
New-AzureRmHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [-DefaultStorageAccountType <StorageType>]
 [-Config <AzureHDInsightConfig>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-DefaultStorageContainer <String>] [-DefaultStorageRootPath <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>]
 [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00dc2-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="00dc2-107">CertificateFileContents</span></span>
```
New-AzureRmHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [-DefaultStorageAccountType <StorageType>]
 [-Config <AzureHDInsightConfig>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-DefaultStorageContainer <String>] [-DefaultStorageRootPath <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>]
 [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00dc2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="00dc2-108">DESCRIPTION</span></span>
<span data-ttu-id="00dc2-109">Das New-AzureHDInsightCluster erstellt einen Azure HDInsight-Cluster mithilfe der angegebenen Parameter oder mithilfe eines mit dem New-AzureRmHDInsightClusterConfig-Cmdlet erstellten Konfigurationsobjekts.</span><span class="sxs-lookup"><span data-stu-id="00dc2-109">The New-AzureHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="00dc2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="00dc2-110">EXAMPLES</span></span>

### <span data-ttu-id="00dc2-111">--------------------------Beispiel 1: Erstellen eines Azure HDInsight-Clusters--------------------------</span><span class="sxs-lookup"><span data-stu-id="00dc2-111">--------------------------  Example 1: Create an Azure HDInsight cluster  --------------------------</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzureStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        #   New-AzureRMResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzureRmHDInsightCluster `
            -ClusterType Hadoop `
            -OSType Windows `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="00dc2-112">Dieser Befehl erstellt einen Cluster im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="00dc2-112">This command creates a cluster in the current subscription.</span></span>

## <span data-ttu-id="00dc2-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="00dc2-113">PARAMETERS</span></span>

### <span data-ttu-id="00dc2-114">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="00dc2-114">-AadTenantId</span></span>
<span data-ttu-id="00dc2-115">Gibt die Azure AD-Mandanten-ID an, die beim Zugriff auf den Azure Data Lake Store verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="00dc2-115">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00dc2-116">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="00dc2-116">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="00dc2-117">Gibt die zusätzlichen Azure-Speicherkonten für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="00dc2-117">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="00dc2-118">Sie können das Add-AzureRmHDInsightStorage-Cmdlet auch verwenden.</span><span class="sxs-lookup"><span data-stu-id="00dc2-118">You can alternatively use the Add-AzureRmHDInsightStorage cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00dc2-119">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="00dc2-119">-CertificateFileContents</span></span>
<span data-ttu-id="00dc2-120">Gibt den Dateiinhalt des Zertifikats an, das beim Zugriff auf den Azure Data Lake Store verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="00dc2-120">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Byte[]
Parameter Sets: CertificateFileContents
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00dc2-121">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="00dc2-121">-CertificateFilePath</span></span>
<span data-ttu-id="00dc2-122">Gibt den Dateipfad zu dem Zertifikat an, das zur Authentifizierung als Dienstprinzipal verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="00dc2-122">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="00dc2-123">Der Cluster verwendet diesen beim Zugriff auf den Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="00dc2-123">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: String
Parameter Sets: CertificateFilePath
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00dc2-124">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="00dc2-124">-CertificatePassword</span></span>
<span data-ttu-id="00dc2-125">Gibt das Kennwort für das Zertifikat an, das für die Authentifizierung als Dienstprinzipal verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="00dc2-125">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="00dc2-126">Der Cluster verwendet diesen beim Zugriff auf den Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="00dc2-126">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="00dc2-127">-Clustername</span><span class="sxs-lookup"><span data-stu-id="00dc2-127">-ClusterName</span></span>
<span data-ttu-id="00dc2-128">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="00dc2-128">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00dc2-129">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="00dc2-129">-ClusterSizeInNodes</span></span>
<span data-ttu-id="00dc2-130">Gibt die Anzahl der Arbeits Knoten für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="00dc2-130">Specifies the number of Worker nodes for the cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00dc2-131">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="00dc2-131">-ClusterTier</span></span>
<span data-ttu-id="00dc2-132">Gibt die HDInsight-Clusterebene an.</span><span class="sxs-lookup"><span data-stu-id="00dc2-132">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="00dc2-133">Standardmäßig ist dies Standard.</span><span class="sxs-lookup"><span data-stu-id="00dc2-133">By default, this is Standard.</span></span>
<span data-ttu-id="00dc2-134">Die Premium-Stufe kann nur mit Linux-Clustern verwendet werden und ermöglicht die Verwendung einiger neuer Funktionen.</span><span class="sxs-lookup"><span data-stu-id="00dc2-134">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

```yaml
Type: Tier
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00dc2-135">-Clustertyp</span><span class="sxs-lookup"><span data-stu-id="00dc2-135">-ClusterType</span></span>
<span data-ttu-id="00dc2-136">Gibt den Typ des zu erstellende Clusters an.</span><span class="sxs-lookup"><span data-stu-id="00dc2-136">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="00dc2-137">Folgende Optionen stehen zur Auswahl: Hadoop, HBAs, Storm, Spark</span><span class="sxs-lookup"><span data-stu-id="00dc2-137">Options are: Hadoop, HBase, Storm, Spark</span></span>

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

### <span data-ttu-id="00dc2-138">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="00dc2-138">-ComponentVersion</span></span>
```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00dc2-139">-Config</span><span class="sxs-lookup"><span data-stu-id="00dc2-139">-Config</span></span>
<span data-ttu-id="00dc2-140">Gibt das Clusterobjekt an, das zum Erstellen des Clusters verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="00dc2-140">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="00dc2-141">Dieses Objekt kann mithilfe des New-AzureRmHDInsightClusterConfig-Cmdlets erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="00dc2-141">This object can be created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00dc2-142">-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="00dc2-142">-Configurations</span></span>
<span data-ttu-id="00dc2-143">Gibt die Konfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="00dc2-143">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="00dc2-144">Sie können das Add-AzureRmHDInsightConfigValues-Cmdlet auch verwenden.</span><span class="sxs-lookup"><span data-stu-id="00dc2-144">You can alternatively use the Add-AzureRmHDInsightConfigValues cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00dc2-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00dc2-145">-DefaultProfile</span></span>
<span data-ttu-id="00dc2-146">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="00dc2-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00dc2-147">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="00dc2-147">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="00dc2-148">Gibt den Kontoschlüssel für das standardmäßige Azure Storage-Konto an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="00dc2-148">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="00dc2-149">Sie können das Set-AzureRmHDInsightDefaultStorage-Cmdlet auch verwenden.</span><span class="sxs-lookup"><span data-stu-id="00dc2-149">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00dc2-150">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="00dc2-150">-DefaultStorageAccountName</span></span>
<span data-ttu-id="00dc2-151">Gibt den Namen des standardmäßigen Azure-speicherkontos an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="00dc2-151">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="00dc2-152">Sie können das Set-AzureRmHDInsightDefaultStorage-Cmdlet auch verwenden.</span><span class="sxs-lookup"><span data-stu-id="00dc2-152">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00dc2-153">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="00dc2-153">-DefaultStorageAccountType</span></span>
<span data-ttu-id="00dc2-154">Gibt den Typ des Standardspeicher Kontos an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="00dc2-154">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="00dc2-155">Mögliche Werte sind AzureStorage und AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="00dc2-155">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="00dc2-156">Standardmäßig AzureStorage, wenn nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="00dc2-156">Defaults to AzureStorage if not specified.</span></span>

```yaml
Type: StorageType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: AzureStorage
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00dc2-157">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="00dc2-157">-DefaultStorageContainer</span></span>
<span data-ttu-id="00dc2-158">Gibt den Namen des Standardcontainers im standardmäßigen Azure Storage-Konto an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="00dc2-158">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="00dc2-159">Sie können das Set-AzureRmHDInsightDefaultStorage-Cmdlet auch verwenden.</span><span class="sxs-lookup"><span data-stu-id="00dc2-159">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="00dc2-160">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="00dc2-160">-DefaultStorageRootPath</span></span>
<span data-ttu-id="00dc2-161">Gibt den Pfadpräfix im Data Lake Store-Konto an, das vom HDInsight-Cluster als Standarddateisystem verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="00dc2-161">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

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

### <span data-ttu-id="00dc2-162">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="00dc2-162">-DisksPerWorkerNode</span></span>
<span data-ttu-id="00dc2-163">Gibt die Anzahl der Datenträger für die Worker-Knoten Rolle im Cluster an.</span><span class="sxs-lookup"><span data-stu-id="00dc2-163">Specifies the number of disks for worker node role in the cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00dc2-164">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="00dc2-164">-EdgeNodeSize</span></span>
<span data-ttu-id="00dc2-165">Gibt die Größe des virtuellen Computers für den Edge-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="00dc2-165">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="00dc2-166">Verwenden Sie Get-AzureRmVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="00dc2-166">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="00dc2-167">Dieser Parameter ist nur für RServer-Cluster gültig.</span><span class="sxs-lookup"><span data-stu-id="00dc2-167">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="00dc2-168">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="00dc2-168">-HeadNodeSize</span></span>
<span data-ttu-id="00dc2-169">Gibt die Größe des virtuellen Computers für den Head-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="00dc2-169">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="00dc2-170">Verwenden Sie Get-AzureRmVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="00dc2-170">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="00dc2-171">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="00dc2-171">-HiveMetastore</span></span>
<span data-ttu-id="00dc2-172">Gibt die SQL-Datenbank zum Speichern von Struktur Metadaten an.</span><span class="sxs-lookup"><span data-stu-id="00dc2-172">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="00dc2-173">Sie können das Add-AzureRmHDInsightMetastore-Cmdlet auch verwenden.</span><span class="sxs-lookup"><span data-stu-id="00dc2-173">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

```yaml
Type: AzureHDInsightMetastore
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00dc2-174">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="00dc2-174">-HttpCredential</span></span>
<span data-ttu-id="00dc2-175">Gibt die Anmeldeinformationen für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="00dc2-175">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00dc2-176">-Standort</span><span class="sxs-lookup"><span data-stu-id="00dc2-176">-Location</span></span>
<span data-ttu-id="00dc2-177">Gibt den Speicherort des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="00dc2-177">Specifies the location for the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00dc2-178">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="00dc2-178">-ObjectId</span></span>
<span data-ttu-id="00dc2-179">Gibt die Azure AD-Objekt-ID (eine GUID) des Azure AD-Dienst Prinzipals an, der den Cluster darstellt.</span><span class="sxs-lookup"><span data-stu-id="00dc2-179">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="00dc2-180">Der Cluster verwendet diesen beim Zugriff auf den Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="00dc2-180">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00dc2-181">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="00dc2-181">-OozieMetastore</span></span>
<span data-ttu-id="00dc2-182">Gibt die SQL-Datenbank an, in der Oozie-Metadaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="00dc2-182">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="00dc2-183">Sie können das Add-AzureRmHDInsightMetastore-Cmdlet auch verwenden.</span><span class="sxs-lookup"><span data-stu-id="00dc2-183">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

```yaml
Type: AzureHDInsightMetastore
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00dc2-184">-OSType</span><span class="sxs-lookup"><span data-stu-id="00dc2-184">-OSType</span></span>
<span data-ttu-id="00dc2-185">Gibt das Betriebssystem für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="00dc2-185">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="00dc2-186">Optionen sind: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="00dc2-186">Options are: Windows, Linux</span></span>

```yaml
Type: OSType
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00dc2-187">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="00dc2-187">-RdpAccessExpiry</span></span>
<span data-ttu-id="00dc2-188">Gibt den Ablauf als DateTime-Objekt für den Zugriff auf einen Cluster mit Remote Desktop Protokoll (RDP) an.</span><span class="sxs-lookup"><span data-stu-id="00dc2-188">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="00dc2-189">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="00dc2-189">-RdpCredential</span></span>
<span data-ttu-id="00dc2-190">Gibt die Remote Desktop (RDP)-Anmeldeinformationen für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="00dc2-190">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="00dc2-191">Dies gilt nur für Windows-Cluster.</span><span class="sxs-lookup"><span data-stu-id="00dc2-191">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="00dc2-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00dc2-192">-ResourceGroupName</span></span>
<span data-ttu-id="00dc2-193">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="00dc2-193">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00dc2-194">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="00dc2-194">-ScriptActions</span></span>
<span data-ttu-id="00dc2-195">Gibt die Skriptaktionen an, die am Ende der Clustererstellung auf dem Cluster ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="00dc2-195">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="00dc2-196">Alternativ können Sie Add-AzureRmHDInsightScriptAction verwenden.</span><span class="sxs-lookup"><span data-stu-id="00dc2-196">You can alternatively use Add-AzureRmHDInsightScriptAction.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]
Parameter Sets: (All)
Aliases: 
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00dc2-197">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="00dc2-197">-SecurityProfile</span></span>
<span data-ttu-id="00dc2-198">Gibt die sicherheitsbezogenen Eigenschaften an, die zum Erstellen eines sicheren Clusters verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00dc2-198">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="00dc2-199">Sie können das Add-AzureRmHDInsightSecurityProfile-Cmdlet auch verwenden.</span><span class="sxs-lookup"><span data-stu-id="00dc2-199">You can alternatively use the Add-AzureRmHDInsightSecurityProfile cmdlet.</span></span>

```yaml
Type: AzureHDInsightSecurityProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00dc2-200">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="00dc2-200">-SshCredential</span></span>
<span data-ttu-id="00dc2-201">Gibt die für SSH-Verbindungen zu verwendenden SSH-Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="00dc2-201">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="00dc2-202">Dies gilt nur für Linux-Cluster.</span><span class="sxs-lookup"><span data-stu-id="00dc2-202">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="00dc2-203">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="00dc2-203">-SshPublicKey</span></span>
<span data-ttu-id="00dc2-204">Gibt den öffentlichen Schlüssel an, der für SSH-Verbindungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="00dc2-204">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="00dc2-205">Dies gilt nur für Linux-Cluster.</span><span class="sxs-lookup"><span data-stu-id="00dc2-205">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="00dc2-206">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="00dc2-206">-SubnetName</span></span>
<span data-ttu-id="00dc2-207">Gibt den Namen eines Subnetzes im ausgewählten virtuellen Netzwerk für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="00dc2-207">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

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

### <span data-ttu-id="00dc2-208">-Version</span><span class="sxs-lookup"><span data-stu-id="00dc2-208">-Version</span></span>
<span data-ttu-id="00dc2-209">Gibt die HDI-Version des HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="00dc2-209">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="00dc2-210">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="00dc2-210">-VirtualNetworkId</span></span>
<span data-ttu-id="00dc2-211">Gibt die ID des virtuellen Netzwerks an, in das der Cluster bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="00dc2-211">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="00dc2-212">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="00dc2-212">-WorkerNodeSize</span></span>
<span data-ttu-id="00dc2-213">Gibt die Größe des virtuellen Computers für den Worker-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="00dc2-213">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="00dc2-214">Verwenden Sie Get-AzureRmVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="00dc2-214">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="00dc2-215">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="00dc2-215">-ZookeeperNodeSize</span></span>
<span data-ttu-id="00dc2-216">Gibt die Größe des virtuellen Computers für den zoowärter-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="00dc2-216">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="00dc2-217">Verwenden Sie Get-AzureRmVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="00dc2-217">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="00dc2-218">Dieser Parameter ist nur für HBAs oder Storm-Cluster gültig.</span><span class="sxs-lookup"><span data-stu-id="00dc2-218">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="00dc2-219">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00dc2-219">CommonParameters</span></span>
<span data-ttu-id="00dc2-220">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00dc2-220">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00dc2-221">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00dc2-221">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00dc2-222">Eingaben</span><span class="sxs-lookup"><span data-stu-id="00dc2-222">INPUTS</span></span>

### <span data-ttu-id="00dc2-223">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="00dc2-223">AzureHDInsightConfig</span></span>
<span data-ttu-id="00dc2-224">Der Parameter "config" akzeptiert den Wert vom Typ "AzureHDInsightConfig" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="00dc2-224">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="00dc2-225">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="00dc2-225">OUTPUTS</span></span>

### <span data-ttu-id="00dc2-226">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="00dc2-226">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="00dc2-227">Notizen</span><span class="sxs-lookup"><span data-stu-id="00dc2-227">NOTES</span></span>
<span data-ttu-id="00dc2-228">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Hadoop, hdinsight, HD, Insight</span><span class="sxs-lookup"><span data-stu-id="00dc2-228">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="00dc2-229">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="00dc2-229">RELATED LINKS</span></span>

[<span data-ttu-id="00dc2-230">Neu – AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="00dc2-230">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)

