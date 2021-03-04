---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: 94b982eb2add8341b861732bef5e63d88e67a937
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947144"
---
# <span data-ttu-id="e4642-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e4642-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="e4642-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4642-102">SYNOPSIS</span></span>
<span data-ttu-id="e4642-103">Erstellt einen Azure HDInsight-Cluster in der angegebenen Ressourcengruppe für das aktuelle Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e4642-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="e4642-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4642-104">SYNTAX</span></span>

### <span data-ttu-id="e4642-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="e4642-105">Default (Default)</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
 [-AmbariDatabase <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-StorageContainer <String>] [-StorageRootPath <String>] [-StorageFileSystem <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>]
 [-KafkaManagementNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificatePassword <String>]
 [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DisksPerWorkerNode <Int32>]
 [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>] [-StorageAccountManagedIdentity <String>]
 [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>]
 [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-EnableIDBroker] [-KafkaClientGroupId <String>]
 [-KafkaClientGroupName <String>] [-ResourceProviderConnection <String>] [-PrivateLink <String>]
 [-EnableComputeIsolation] [-ComputeIsolationHostSku <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e4642-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="e4642-106">CertificateFilePath</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
 [-AmbariDatabase <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-StorageContainer <String>] [-StorageRootPath <String>] [-StorageFileSystem <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>]
 [-KafkaManagementNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-StorageAccountManagedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>]
 [-EncryptionAtHost <Boolean>] [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-EnableIDBroker]
 [-KafkaClientGroupId <String>] [-KafkaClientGroupName <String>] [-ResourceProviderConnection <String>]
 [-PrivateLink <String>] [-EnableComputeIsolation] [-ComputeIsolationHostSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4642-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="e4642-107">CertificateFileContents</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
 [-AmbariDatabase <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-StorageContainer <String>] [-StorageRootPath <String>] [-StorageFileSystem <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>]
 [-KafkaManagementNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-StorageAccountManagedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>]
 [-EncryptionAtHost <Boolean>] [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-EnableIDBroker]
 [-KafkaClientGroupId <String>] [-KafkaClientGroupName <String>] [-ResourceProviderConnection <String>]
 [-PrivateLink <String>] [-EnableComputeIsolation] [-ComputeIsolationHostSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4642-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4642-108">DESCRIPTION</span></span>
<span data-ttu-id="e4642-109">Die New-AzHDInsightCluster erstellt einen Azure HDInsight-Cluster mithilfe der angegebenen Parameter oder mithilfe eines Konfigurationsobjekts, das mithilfe des New-AzHDInsightClusterConfig erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e4642-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="e4642-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e4642-110">EXAMPLES</span></span>

### <span data-ttu-id="e4642-111">Beispiel 1: Erstellen eines Azure HDInsight-Clusters</span><span class="sxs-lookup"><span data-stu-id="e4642-111">Example 1: Create an Azure HDInsight cluster</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
```

<span data-ttu-id="e4642-112">Mit diesem Befehl wird ein Cluster im aktuellen Abonnement erstellt.</span><span class="sxs-lookup"><span data-stu-id="e4642-112">This command creates a cluster in the current subscription.</span></span>

### <span data-ttu-id="e4642-113">Beispiel 2: Erstellen eines Clusters mit vom Kunden verwalteter Schlüsseldatenträgerverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="e4642-113">Example 2: Create cluster with customer-managed key disk encryption</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-cmk-cluster"
        $clusterCreds = Get-Credential

        # Customer-managed Key info
        $assignedIdentity = "your-ami-resource-id"
        $encryptionKeyName = "new-key"
        $encryptionVaultUri = "https://MyKeyVault.vault.azure.net"
        $encryptionKeyVersion = "00000000000000000000000000000000"

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Spark `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AssignedIdentity $assignedIdentity `
            -EncryptionKeyName $encryptionKeyName `
            -EncryptionVaultUri $encryptionVaultUri `
            -EncryptionKeyVersion $encryptionKeyVersion
```

### <span data-ttu-id="e4642-114">Beispiel 3: Erstellen eines Azure HDInsight-Clusters, der die Verschlüsselung bei der Übertragung ermöglicht</span><span class="sxs-lookup"><span data-stu-id="e4642-114">Example 3: Create an Azure HDInsight cluster which enables encryption in transit</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}}
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionInTransit $true `
```

### <span data-ttu-id="e4642-115">Beispiel 4: Erstellen eines Azure HDInsight-Clusters mit relay outbound and private link feature</span><span class="sxs-lookup"><span data-stu-id="e4642-115">Example 4: Create an Azure HDInsight cluster with relay outbound and private link feature</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Virtual network info
        $virtualNetworkId="yourvnetresourceid"
        $subnetName="yoursubnetname"

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -VirtualNetworkId $virtualNetworkId -SubnetName $subnetName `
            -ResourceProviderConnection Outbound -PrivateLink Enabled `
```

### <span data-ttu-id="e4642-116">Beispiel 5: Erstellen eines Azure HDInsight-Clusters, der die Verschlüsselung beim Host ermöglicht</span><span class="sxs-lookup"><span data-stu-id="e4642-116">Example 5: Create an Azure HDInsight cluster which enables encryption at host</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionAtHost $true `
```

### <span data-ttu-id="e4642-117">Beispiel 6: Erstellen Sie einen Azure HDInsight-Cluster, der die automatische Skalierung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="e4642-117">Example 6: Create an Azure HDInsight cluster which enables autoscale.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create autoscale configuration
        $autoscaleConfiguration=New-AzHDInsightClusterAutoscaleConfiguration `
            -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AutoscaleConfiguration $autoscaleConfiguration
```

### <span data-ttu-id="e4642-118">Beispiel 7: Erstellen eines Azure HDInsight-Clusters mit Kafka RestProxy.</span><span class="sxs-lookup"><span data-stu-id="e4642-118">Example 7: Create an Azure HDInsight cluster with Kafka Rest Proxy.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Kafka Rest Proxy configuration info
        $kafkaClientGroupName = "yourclientgroupname"
        $kafkaClientGroupId = "yourclientgroupid"
        $kafkaManagementNodeSize = "Standard_D4_v2"
        $disksPerWorkerNode = 2

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Kafka `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -KafkaClientGroupId  $kafkaClientGroupId -KafkaClientGroupName $kafkaClientGroupName `
            -KafkaManagementNodeSize $kafkaManagementNodeSize -DisksPerWorkerNode $disksPerWorkerNode
```

### <span data-ttu-id="e4642-119">Beispiel 8: Erstellen sie einen Azure HDInsight-Cluster mit Azure Data Lake Gen2-Speicher.</span><span class="sxs-lookup"><span data-stu-id="e4642-119">Example 8: Create an Azure HDInsight cluster with Azure Data Lake Gen2 storage.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageManagedIdentity = "yourstorageusermanagedidentity"
        $storageFileSystem = "filesystem01"
        $storageAccountType=AzureDataLakeStorageGen2

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 3 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountManagedIdentity $storageManagedIdentity `
            -StorageFileSystem $storageFileSystem `
            -StorageAccountType $storageAccountType `
            -SshCredential $clusterCreds
```

### <span data-ttu-id="e4642-120">Beispiel 9: Erstellen sie einen Azure HDInsight-Cluster mit Enterprise Security Package(ESP) und Aktivieren des HDInsight-ID-Brokers.</span><span class="sxs-lookup"><span data-stu-id="e4642-120">Example 9: Create an Azure HDInsight cluster with Enterprise Security Package(ESP) and Enable HDInsight ID Broker.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountKey = "yourstorageaccountaccesskey"
        $storageContainer = "yourcontainer01"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # ESP configuration
        $domainResourceId = "your Azure AD Domin Service resource id"
        $domainUser = "yourdomainuser"
        $domainPassword = "yourdoaminpasswd"
        $domainPassword = ConvertTo-SecureString $domainPassword -AsPlainText -Force
        $domainCredential = New-Object System.Management.Automation.PSCredential($domainUser, $domainPassword)
        $clusterUserGroupDns = "dominusergroup"
        $ldapUrls = "ldaps://{your domain name}:636"

        $clusterTier = Premium
        $vnetId = "yourvnetid"
        $subnetName = "yoursubnetname"
        $assignedIdentity = "your user managed assigned identity resourcee id"

        #Create security profile
        $config= New-AzHDInsightClusterConfig|Add-AzHDInsightSecurityProfile -DomainResourceId $domainResourceId -DomainUserCredential $domainCredential -LdapsUrls $ldapUrls -ClusterUsersGroupDNs $clusterUserGroupDns

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusteTier $clusterTier `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 3 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -VirtualNetworkId $vnetId -SubnetName $subnetName `
            -AssignedIdentity $assignedIdentity `
            -SecurityProfile $config.SecurityProfile -EnableIDBroker
```

### <span data-ttu-id="e4642-121">Beispiel 10: Erstellen sie einen Azure HDInsight-Cluster, der die Computeisolation ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="e4642-121">Example 10: Create an Azure HDInsight cluster which enables compute isolation.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential
        $workerNodeSize="Standard_E16S_V3" # here is just an example
        $headNodeSize="Standard_E8S_V3"
        $zookeeperNodeSize="Standard_E2S_V3"

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -WorkerNodeSize $workerNodeSize `
            -HeadNodeSize $headNodeSize `
            -ZookeeperNodeSize $zookeeperNodeSize `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EnableComputeIsolation `
```

## <span data-ttu-id="e4642-122">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e4642-122">PARAMETERS</span></span>

### <span data-ttu-id="e4642-123">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="e4642-123">-AadTenantId</span></span>
<span data-ttu-id="e4642-124">Gibt die Azure AD-Mandanten-ID an, die beim Zugriff auf Azure Data Lake Store verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e4642-124">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-125">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="e4642-125">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="e4642-126">Gibt die zusätzlichen Azure Storage-Konten für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="e4642-126">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="e4642-127">Alternativ können Sie das cmdlet Add-AzHDInsightStorage verwenden.</span><span class="sxs-lookup"><span data-stu-id="e4642-127">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="e4642-128">-AmbariDatabase</span><span class="sxs-lookup"><span data-stu-id="e4642-128">-AmbariDatabase</span></span>
<span data-ttu-id="e4642-129">Ruft die Datenbank für "ambari" ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="e4642-129">Gets or sets the database for ambari.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-130">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e4642-130">-ApplicationId</span></span>
<span data-ttu-id="e4642-131">Ruft die Dienstprinzipalanwendungs-ID für den Zugriff auf Azure Data Lake ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="e4642-131">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-132">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e4642-132">-AssignedIdentity</span></span>
<span data-ttu-id="e4642-133">Ruft die zugewiesene Identität ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="e4642-133">Gets or sets the assigned identity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-134">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4642-134">-AutoscaleConfiguration</span></span>
<span data-ttu-id="e4642-135">Ruft die Konfiguration der automatischen Skalierung ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="e4642-135">Gets or sets the autoscale configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-136">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="e4642-136">-CertificateFileContents</span></span>
<span data-ttu-id="e4642-137">Gibt den Dateiinhalt des Zertifikats an, das beim Zugriff auf Azure Data Lake Store verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e4642-137">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: CertificateFileContents
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-138">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="e4642-138">-CertificateFilePath</span></span>
<span data-ttu-id="e4642-139">Gibt den Dateipfad zu dem Zertifikat an, das zum Authentifizieren als Dienstprinzipal verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e4642-139">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="e4642-140">Der Cluster verwendet dies beim Zugriff auf Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e4642-140">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: CertificateFilePath
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-141">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="e4642-141">-CertificatePassword</span></span>
<span data-ttu-id="e4642-142">Gibt das Kennwort für das Zertifikat an, das zum Authentifizieren als Dienstprinzipal verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e4642-142">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="e4642-143">Der Cluster verwendet dies beim Zugriff auf Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e4642-143">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-144">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e4642-144">-ClusterName</span></span>
<span data-ttu-id="e4642-145">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="e4642-145">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-146">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="e4642-146">-ClusterSizeInNodes</span></span>
<span data-ttu-id="e4642-147">Gibt die Anzahl der Workerknoten für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="e4642-147">Specifies the number of Worker nodes for the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-148">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="e4642-148">-ClusterTier</span></span>
<span data-ttu-id="e4642-149">Gibt die HDInsight-Clusterebene an.</span><span class="sxs-lookup"><span data-stu-id="e4642-149">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="e4642-150">Standardmäßig ist dies Standard.</span><span class="sxs-lookup"><span data-stu-id="e4642-150">By default, this is Standard.</span></span>
<span data-ttu-id="e4642-151">Die Premiumebene kann nur mit Linux-Clustern verwendet werden, und sie ermöglicht die Verwendung einiger neuer Features.</span><span class="sxs-lookup"><span data-stu-id="e4642-151">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.Tier
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-152">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="e4642-152">-ClusterType</span></span>
<span data-ttu-id="e4642-153">Gibt den Typ des zu erstellenden Clusters an.</span><span class="sxs-lookup"><span data-stu-id="e4642-153">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="e4642-154">Optionen sind: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka und RServer</span><span class="sxs-lookup"><span data-stu-id="e4642-154">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-155">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="e4642-155">-ComponentVersion</span></span>
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

### <span data-ttu-id="e4642-156">-ComputeIsolationHostSku</span><span class="sxs-lookup"><span data-stu-id="e4642-156">-ComputeIsolationHostSku</span></span>
<span data-ttu-id="e4642-157">Ruft die dedizierte Host-Sku für die Computeisolation ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="e4642-157">Gets or sets the dedicated host sku for compute isolation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-158">-Config</span><span class="sxs-lookup"><span data-stu-id="e4642-158">-Config</span></span>
<span data-ttu-id="e4642-159">Gibt das Clusterobjekt an, das zum Erstellen des Clusters verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e4642-159">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="e4642-160">Dieses Objekt kann mithilfe des cmdlets New-AzHDInsightClusterConfig werden.</span><span class="sxs-lookup"><span data-stu-id="e4642-160">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-161">-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="e4642-161">-Configurations</span></span>
<span data-ttu-id="e4642-162">Gibt die Konfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="e4642-162">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="e4642-163">Alternativ können Sie das cmdlet Add-AzHDInsightConfigValues verwenden.</span><span class="sxs-lookup"><span data-stu-id="e4642-163">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="e4642-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4642-164">-DefaultProfile</span></span>
<span data-ttu-id="e4642-165">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e4642-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-166">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="e4642-166">-DisksPerWorkerNode</span></span>
<span data-ttu-id="e4642-167">Gibt die Anzahl der Datenträger für die Rolle des Workerknotens im Cluster an.</span><span class="sxs-lookup"><span data-stu-id="e4642-167">Specifies the number of disks for worker node role in the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-168">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="e4642-168">-EdgeNodeSize</span></span>
<span data-ttu-id="e4642-169">Gibt die Größe des virtuellen Computers für den Edgeknoten an.</span><span class="sxs-lookup"><span data-stu-id="e4642-169">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="e4642-170">Verwenden Get-AzVMSize für akzeptable VM-Größen, und lesen Sie die Preisseite von HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e4642-170">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="e4642-171">Dieser Parameter ist nur für RServer-Cluster gültig.</span><span class="sxs-lookup"><span data-stu-id="e4642-171">This parameter is valid only for RServer clusters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-172">-EnableComputeIsolation</span><span class="sxs-lookup"><span data-stu-id="e4642-172">-EnableComputeIsolation</span></span>
<span data-ttu-id="e4642-173">Aktiviert die HDInsight-Computeisolationsfunktion.</span><span class="sxs-lookup"><span data-stu-id="e4642-173">Enables HDInsight compute isolation feature.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-174">-EnableIDBroker</span><span class="sxs-lookup"><span data-stu-id="e4642-174">-EnableIDBroker</span></span>
<span data-ttu-id="e4642-175">Aktiviert das Feature HDInsight Identity Broker.</span><span class="sxs-lookup"><span data-stu-id="e4642-175">Enables HDInsight Identity Broker feature.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-176">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="e4642-176">-EncryptionAlgorithm</span></span>
<span data-ttu-id="e4642-177">Ruft den Verschlüsselungsalgorithmus ab oder legt den Verschlüsselungsalgorithmus fest.</span><span class="sxs-lookup"><span data-stu-id="e4642-177">Gets or sets the encryption algorithm.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA-OAEP-256, RSA1_5

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-178">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="e4642-178">-EncryptionAtHost</span></span>
<span data-ttu-id="e4642-179">Ruft das -Kennzeichen ab oder legt es fest, das angibt, ob die Verschlüsselung auf dem Host aktiviert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="e4642-179">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-180">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="e4642-180">-EncryptionInTransit</span></span>
<span data-ttu-id="e4642-181">Ruft das -Kennzeichen ab oder legt es fest, das angibt, ob die Verschlüsselung bei der Übertragung aktiviert werden soll oder nicht.</span><span class="sxs-lookup"><span data-stu-id="e4642-181">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-182">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="e4642-182">-EncryptionKeyName</span></span>
<span data-ttu-id="e4642-183">Ruft den Namen des Verschlüsselungsschlüssels ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="e4642-183">Gets or sets the encryption key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-184">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="e4642-184">-EncryptionKeyVersion</span></span>
<span data-ttu-id="e4642-185">Ruft die Verschlüsselungsschlüsselversion ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="e4642-185">Gets or sets the encryption key version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-186">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="e4642-186">-EncryptionVaultUri</span></span>
<span data-ttu-id="e4642-187">Ruft den Verschlüsselungstresor-URI ab oder legt den -URI fest.</span><span class="sxs-lookup"><span data-stu-id="e4642-187">Gets or sets the encryption vault uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-188">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="e4642-188">-HeadNodeSize</span></span>
<span data-ttu-id="e4642-189">Gibt die Größe des virtuellen Computers für den Knoten Head an.</span><span class="sxs-lookup"><span data-stu-id="e4642-189">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="e4642-190">Verwenden Get-AzVMSize für akzeptable VM-Größen, und lesen Sie die Preisseite von HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e4642-190">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-191">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="e4642-191">-HiveMetastore</span></span>
<span data-ttu-id="e4642-192">Gibt die SQL-Datenbank zum Speichern von Hive-Metadaten an.</span><span class="sxs-lookup"><span data-stu-id="e4642-192">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="e4642-193">Alternativ können Sie das cmdlet Add-AzHDInsightMetastore verwenden.</span><span class="sxs-lookup"><span data-stu-id="e4642-193">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-194">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="e4642-194">-HttpCredential</span></span>
<span data-ttu-id="e4642-195">Gibt die Anmeldeinformationen für den Cluster (Cluster Login, HTTP) für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="e4642-195">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-196">-KafkaClientGroupId</span><span class="sxs-lookup"><span data-stu-id="e4642-196">-KafkaClientGroupId</span></span>
<span data-ttu-id="e4642-197">Ruft die Clientgruppen-ID für kafka Restproxyzugriff ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="e4642-197">Gets or sets the client group id for Kafka Rest Proxy access.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-198">-KafkaClientGroupName</span><span class="sxs-lookup"><span data-stu-id="e4642-198">-KafkaClientGroupName</span></span>
<span data-ttu-id="e4642-199">Ruft den Namen der Clientgruppe für kafka RestProxyzugriff ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="e4642-199">Gets or sets the client group name for Kafka Rest Proxy access.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-200">-KafkaManagementNodeSize</span><span class="sxs-lookup"><span data-stu-id="e4642-200">-KafkaManagementNodeSize</span></span>
<span data-ttu-id="e4642-201">Ruft die Größe des Kafka-Verwaltungsknotens ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="e4642-201">Gets or sets the size of the Kafka Management Node.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-202">-Location</span><span class="sxs-lookup"><span data-stu-id="e4642-202">-Location</span></span>
<span data-ttu-id="e4642-203">Gibt den Speicherort für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="e4642-203">Specifies the location for the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-204">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="e4642-204">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="e4642-205">Ruft die minimal unterstützte TLS-Version ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="e4642-205">Gets or sets the minimal supported TLS version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-206">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e4642-206">-ObjectId</span></span>
<span data-ttu-id="e4642-207">Gibt die Azure AD-Objekt-ID (GUID) des Azure AD-Dienstprinzipals an, der den Cluster darstellt.</span><span class="sxs-lookup"><span data-stu-id="e4642-207">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="e4642-208">Der Cluster verwendet dies beim Zugriff auf Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e4642-208">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-209">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="e4642-209">-OozieMetastore</span></span>
<span data-ttu-id="e4642-210">Gibt die datenbank SQL an, um Oozie-Metadaten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="e4642-210">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="e4642-211">Alternativ können Sie das cmdlet Add-AzHDInsightMetastore verwenden.</span><span class="sxs-lookup"><span data-stu-id="e4642-211">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-212">-OSType</span><span class="sxs-lookup"><span data-stu-id="e4642-212">-OSType</span></span>
<span data-ttu-id="e4642-213">Gibt das Betriebssystem für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="e4642-213">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="e4642-214">Optionen sind: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="e4642-214">Options are: Windows, Linux</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.OSType
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-215">-PrivateLink</span><span class="sxs-lookup"><span data-stu-id="e4642-215">-PrivateLink</span></span>
<span data-ttu-id="e4642-216">Ruft den privaten Linktyp ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="e4642-216">Gets or sets the private link type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-217">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="e4642-217">-RdpAccessExpiry</span></span>
<span data-ttu-id="e4642-218">Gibt den Ablauf als DateTime-Objekt für den Remotedesktopprotokollzugriff (RDP) auf einen Cluster an.</span><span class="sxs-lookup"><span data-stu-id="e4642-218">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-219">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="e4642-219">-RdpCredential</span></span>
<span data-ttu-id="e4642-220">Gibt die Remotedesktopanmeldeinformationen für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="e4642-220">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="e4642-221">Dies gilt nur für Windows-Cluster.</span><span class="sxs-lookup"><span data-stu-id="e4642-221">This is only for Windows clusters.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-222">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4642-222">-ResourceGroupName</span></span>
<span data-ttu-id="e4642-223">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="e4642-223">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-224">-ResourceProviderConnection</span><span class="sxs-lookup"><span data-stu-id="e4642-224">-ResourceProviderConnection</span></span>
<span data-ttu-id="e4642-225">Ruft den Verbindungstyp des Ressourcenanbieters ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="e4642-225">Gets or sets the resource provider connection type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-226">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="e4642-226">-ScriptActions</span></span>
<span data-ttu-id="e4642-227">Gibt die Skriptaktionen an, die am Ende der Clustererstellung für den Cluster ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e4642-227">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="e4642-228">Alternativ können Sie Add-AzHDInsightScriptAction verwenden.</span><span class="sxs-lookup"><span data-stu-id="e4642-228">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="e4642-229">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="e4642-229">-SecurityProfile</span></span>
<span data-ttu-id="e4642-230">Gibt die sicherheitsbezogenen Eigenschaften an, die zum Erstellen eines sicheren Clusters verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e4642-230">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="e4642-231">Alternativ können Sie das cmdlet Add-AzHDInsightSecurityProfile verwenden.</span><span class="sxs-lookup"><span data-stu-id="e4642-231">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-232">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="e4642-232">-SshCredential</span></span>
<span data-ttu-id="e4642-233">Gibt die SSH-Anmeldeinformationen an, die für SSH-Verbindungen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e4642-233">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="e4642-234">Dies gilt nur für Linux-Cluster.</span><span class="sxs-lookup"><span data-stu-id="e4642-234">This is only for Linux clusters.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-235">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="e4642-235">-SshPublicKey</span></span>
<span data-ttu-id="e4642-236">Gibt den öffentlichen Schlüssel an, der für SSH-Verbindungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e4642-236">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="e4642-237">Dies gilt nur für Linux-Cluster.</span><span class="sxs-lookup"><span data-stu-id="e4642-237">This is only for Linux clusters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-238">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e4642-238">-StorageAccountKey</span></span>
<span data-ttu-id="e4642-239">Ruft den Speicherkontozugriffsschlüssel für das Speicherkonto ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="e4642-239">Gets or sets the Storage Account Access Key for the Storage Account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-240">-StorageAccountManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="e4642-240">-StorageAccountManagedIdentity</span></span>
<span data-ttu-id="e4642-241">Ruft die verwaltete Identität des Speicherkontos ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="e4642-241">Gets or sets the storage account managed identity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-242">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="e4642-242">-StorageAccountResourceId</span></span>
<span data-ttu-id="e4642-243">Ruft die Speicherressourcen-ID für das Speicherkonto ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="e4642-243">Gets or sets the Storage Resource Id for the Storage Account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-244">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="e4642-244">-StorageAccountType</span></span>
<span data-ttu-id="e4642-245">Ruft den Typ des Speicherkontos ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="e4642-245">Gets or sets the type of the storage account.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore, AzureDataLakeStorageGen2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-246">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="e4642-246">-StorageContainer</span></span>
<span data-ttu-id="e4642-247">Ruft den StorageContainer-Namen für das standardmäßige Azure Storage-Konto ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="e4642-247">Gets or sets the StorageContainer name for the default Azure Storage Account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-248">-StorageFileSystem</span><span class="sxs-lookup"><span data-stu-id="e4642-248">-StorageFileSystem</span></span>
<span data-ttu-id="e4642-249">Ruft das Dateisystem für das Standardmäßige Azure Data Lake Storage Gen2-Konto ab oder legt es fest.</span><span class="sxs-lookup"><span data-stu-id="e4642-249">Gets or sets the file system for the default Azure Data Lake Storage Gen2 account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-250">-StorageRootPath</span><span class="sxs-lookup"><span data-stu-id="e4642-250">-StorageRootPath</span></span>
<span data-ttu-id="e4642-251">Ruft den Pfad zum Stamm des Clusters im Standardmäßigen Data Lake Store-Konto ab oder legt den Pfad fest.</span><span class="sxs-lookup"><span data-stu-id="e4642-251">Gets or sets the path to the root of the cluster in the default Data Lake Store Account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-252">-Subnetzname</span><span class="sxs-lookup"><span data-stu-id="e4642-252">-SubnetName</span></span>
<span data-ttu-id="e4642-253">Ruft den Subnetznamen für diesen HDInsight-Cluster ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="e4642-253">Gets or sets the subnet name for this HDInsight cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-254">-Version</span><span class="sxs-lookup"><span data-stu-id="e4642-254">-Version</span></span>
<span data-ttu-id="e4642-255">Gibt die HDI-Version des HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="e4642-255">Specifies the HDI version of the HDInsight cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-256">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="e4642-256">-VirtualNetworkId</span></span>
<span data-ttu-id="e4642-257">Gibt die ID des virtuellen Netzwerks an, in dem der Cluster bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e4642-257">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-258">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="e4642-258">-WorkerNodeSize</span></span>
<span data-ttu-id="e4642-259">Gibt die Größe des virtuellen Computers für den Workerknoten an.</span><span class="sxs-lookup"><span data-stu-id="e4642-259">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="e4642-260">Verwenden Get-AzVMSize für akzeptable VM-Größen, und lesen Sie die Preisseite von HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e4642-260">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-261">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="e4642-261">-ZookeeperNodeSize</span></span>
<span data-ttu-id="e4642-262">Gibt die Größe des virtuellen Computers für den Knoten Zookeeper an.</span><span class="sxs-lookup"><span data-stu-id="e4642-262">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="e4642-263">Verwenden Get-AzVMSize für akzeptable VM-Größen, und lesen Sie die Preisseite von HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e4642-263">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="e4642-264">Dieser Parameter ist nur für HBase- oder Storm-Cluster gültig.</span><span class="sxs-lookup"><span data-stu-id="e4642-264">This parameter is valid only for HBase or Storm clusters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4642-265">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4642-265">CommonParameters</span></span>
<span data-ttu-id="e4642-266">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4642-266">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4642-267">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4642-267">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4642-268">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e4642-268">INPUTS</span></span>

### <span data-ttu-id="e4642-269">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="e4642-269">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="e4642-270">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e4642-270">OUTPUTS</span></span>

### <span data-ttu-id="e4642-271">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e4642-271">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="e4642-272">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e4642-272">NOTES</span></span>
<span data-ttu-id="e4642-273">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span><span class="sxs-lookup"><span data-stu-id="e4642-273">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="e4642-274">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e4642-274">RELATED LINKS</span></span>

[<span data-ttu-id="e4642-275">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="e4642-275">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

