---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: b42b93bbecef5ec56495be632788bd1373ae9db1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175563"
---
# <span data-ttu-id="34d61-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="34d61-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="34d61-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="34d61-102">SYNOPSIS</span></span>
<span data-ttu-id="34d61-103">Erstellt einen Azure HDInsight-Cluster in der angegebenen Ressourcengruppe für das aktuelle Abonnement.</span><span class="sxs-lookup"><span data-stu-id="34d61-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="34d61-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="34d61-104">SYNTAX</span></span>

### <span data-ttu-id="34d61-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="34d61-105">Default (Default)</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
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
 [-KafkaClientGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34d61-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="34d61-106">CertificateFilePath</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
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
 [-KafkaClientGroupId <String>] [-KafkaClientGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="34d61-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="34d61-107">CertificateFileContents</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
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
 [-KafkaClientGroupId <String>] [-KafkaClientGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="34d61-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34d61-108">DESCRIPTION</span></span>
<span data-ttu-id="34d61-109">Das New-AzHDInsightCluster erstellt einen Azure HDInsight-Cluster mithilfe der angegebenen Parameter oder mithilfe eines mit dem New-AzHDInsightClusterConfig-Cmdlet erstellten Konfigurationsobjekts.</span><span class="sxs-lookup"><span data-stu-id="34d61-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="34d61-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="34d61-110">EXAMPLES</span></span>

### <span data-ttu-id="34d61-111">Beispiel 1: Erstellen eines Azure HDInsight-Clusters</span><span class="sxs-lookup"><span data-stu-id="34d61-111">Example 1: Create an Azure HDInsight cluster</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
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

<span data-ttu-id="34d61-112">Dieser Befehl erstellt einen Cluster im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="34d61-112">This command creates a cluster in the current subscription.</span></span>

### <span data-ttu-id="34d61-113">Beispiel 2: Erstellen eines Clusters mit vom Kunden verwalteten Schlüsseldaten Träger Verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="34d61-113">Example 2: Create cluster with customer-managed key disk encryption</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
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

### <span data-ttu-id="34d61-114">Beispiel 3: Erstellen eines Azure HDInsight-Clusters, der die Verschlüsselung bei der Übertragung ermöglicht</span><span class="sxs-lookup"><span data-stu-id="34d61-114">Example 3: Create an Azure HDInsight cluster which enables encryption in transit</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
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

### <span data-ttu-id="34d61-115">Beispiel 4: Erstellen eines Azure HDInsight-Clusters mit Feature für private Links</span><span class="sxs-lookup"><span data-stu-id="34d61-115">Example 4: Create an Azure HDInsight cluster with private link feature</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
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
            -PublicNetworkAccessType OutboundOnly -OutboundPublicNetworkAccessType PublicLoadBalancer `
```

### <span data-ttu-id="34d61-116">Beispiel 5: Erstellen eines Azure HDInsight-Clusters, der die Verschlüsselung am Host ermöglicht</span><span class="sxs-lookup"><span data-stu-id="34d61-116">Example 5: Create an Azure HDInsight cluster which enables encryption at host</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
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

### <span data-ttu-id="34d61-117">Beispiel 6: Erstellen eines Azure HDInsight-Clusters, der die autoskala aktiviert.</span><span class="sxs-lookup"><span data-stu-id="34d61-117">Example 6: Create an Azure HDInsight cluster which enables autoscale.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
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

### <span data-ttu-id="34d61-118">Beispiel 7: Erstellen eines Azure HDInsight-Clusters mit Kafka-Ruhe Proxy</span><span class="sxs-lookup"><span data-stu-id="34d61-118">Example 7: Create an Azure HDInsight cluster with Kafka Rest Proxy.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
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

### <span data-ttu-id="34d61-119">Beispiel 8: Erstellen eines Azure HDInsight-Clusters mit Azure Data Lake Gen2-Speicher.</span><span class="sxs-lookup"><span data-stu-id="34d61-119">Example 8: Create an Azure HDInsight cluster with Azure Data Lake Gen2 storage.</span></span>
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

### <span data-ttu-id="34d61-120">Beispiel 9: Erstellen eines Azure HDInsight-Clusters mit ESP (Enterprise Security Package) und Aktivieren des HDInsight-ID-Brokers.</span><span class="sxs-lookup"><span data-stu-id="34d61-120">Example 9: Create an Azure HDInsight cluster with Enterprise Security Package(ESP) and Enable HDInsight ID Broker.</span></span>
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

## <span data-ttu-id="34d61-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="34d61-121">PARAMETERS</span></span>

### <span data-ttu-id="34d61-122">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="34d61-122">-AadTenantId</span></span>
<span data-ttu-id="34d61-123">Gibt die Azure AD-Mandanten-ID an, die beim Zugriff auf den Azure Data Lake Store verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="34d61-123">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="34d61-124">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="34d61-124">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="34d61-125">Gibt die zusätzlichen Azure-Speicherkonten für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="34d61-125">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="34d61-126">Sie können das Add-AzHDInsightStorage-Cmdlet auch verwenden.</span><span class="sxs-lookup"><span data-stu-id="34d61-126">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="34d61-127">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="34d61-127">-ApplicationId</span></span>
<span data-ttu-id="34d61-128">Ruft die Dienstprinzipal-Anwendungs-ID für den Zugriff auf Azure Data Lake ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="34d61-128">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="34d61-129">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="34d61-129">-AssignedIdentity</span></span>
<span data-ttu-id="34d61-130">Ruft die zugewiesene Identität ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="34d61-130">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="34d61-131">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="34d61-131">-AutoscaleConfiguration</span></span>
<span data-ttu-id="34d61-132">Ruft die Konfiguration des AutoScale ab oder legt diese fest</span><span class="sxs-lookup"><span data-stu-id="34d61-132">Gets or sets the autoscale configuration</span></span>

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

### <span data-ttu-id="34d61-133">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="34d61-133">-CertificateFileContents</span></span>
<span data-ttu-id="34d61-134">Gibt den Dateiinhalt des Zertifikats an, das beim Zugriff auf den Azure Data Lake Store verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="34d61-134">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="34d61-135">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="34d61-135">-CertificateFilePath</span></span>
<span data-ttu-id="34d61-136">Gibt den Dateipfad zu dem Zertifikat an, das zur Authentifizierung als Dienstprinzipal verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="34d61-136">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="34d61-137">Der Cluster verwendet diesen beim Zugriff auf den Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="34d61-137">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="34d61-138">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="34d61-138">-CertificatePassword</span></span>
<span data-ttu-id="34d61-139">Gibt das Kennwort für das Zertifikat an, das für die Authentifizierung als Dienstprinzipal verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="34d61-139">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="34d61-140">Der Cluster verwendet diesen beim Zugriff auf den Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="34d61-140">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="34d61-141">-Clustername</span><span class="sxs-lookup"><span data-stu-id="34d61-141">-ClusterName</span></span>
<span data-ttu-id="34d61-142">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="34d61-142">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="34d61-143">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="34d61-143">-ClusterSizeInNodes</span></span>
<span data-ttu-id="34d61-144">Gibt die Anzahl der Arbeits Knoten für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="34d61-144">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="34d61-145">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="34d61-145">-ClusterTier</span></span>
<span data-ttu-id="34d61-146">Gibt die HDInsight-Clusterebene an.</span><span class="sxs-lookup"><span data-stu-id="34d61-146">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="34d61-147">Standardmäßig ist dies Standard.</span><span class="sxs-lookup"><span data-stu-id="34d61-147">By default, this is Standard.</span></span>
<span data-ttu-id="34d61-148">Die Premium-Stufe kann nur mit Linux-Clustern verwendet werden und ermöglicht die Verwendung einiger neuer Funktionen.</span><span class="sxs-lookup"><span data-stu-id="34d61-148">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="34d61-149">-Clustertyp</span><span class="sxs-lookup"><span data-stu-id="34d61-149">-ClusterType</span></span>
<span data-ttu-id="34d61-150">Gibt den Typ des zu erstellende Clusters an.</span><span class="sxs-lookup"><span data-stu-id="34d61-150">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="34d61-151">Folgende Optionen stehen zur Auswahl: Hadoop, HBAs, Storm, Spark, INTERACTIVEHIVE, Kafka und RServer</span><span class="sxs-lookup"><span data-stu-id="34d61-151">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

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

### <span data-ttu-id="34d61-152">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="34d61-152">-ComponentVersion</span></span>
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

### <span data-ttu-id="34d61-153">-Config</span><span class="sxs-lookup"><span data-stu-id="34d61-153">-Config</span></span>
<span data-ttu-id="34d61-154">Gibt das Clusterobjekt an, das zum Erstellen des Clusters verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="34d61-154">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="34d61-155">Dieses Objekt kann mithilfe des New-AzHDInsightClusterConfig-Cmdlets erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="34d61-155">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="34d61-156">-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="34d61-156">-Configurations</span></span>
<span data-ttu-id="34d61-157">Gibt die Konfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="34d61-157">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="34d61-158">Sie können das Add-AzHDInsightConfigValues-Cmdlet auch verwenden.</span><span class="sxs-lookup"><span data-stu-id="34d61-158">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="34d61-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34d61-159">-DefaultProfile</span></span>
<span data-ttu-id="34d61-160">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="34d61-160">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34d61-161">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="34d61-161">-DisksPerWorkerNode</span></span>
<span data-ttu-id="34d61-162">Gibt die Anzahl der Datenträger für die Worker-Knoten Rolle im Cluster an.</span><span class="sxs-lookup"><span data-stu-id="34d61-162">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="34d61-163">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="34d61-163">-EdgeNodeSize</span></span>
<span data-ttu-id="34d61-164">Gibt die Größe des virtuellen Computers für den Edge-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="34d61-164">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="34d61-165">Verwenden Sie Get-AzVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="34d61-165">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="34d61-166">Dieser Parameter ist nur für RServer-Cluster gültig.</span><span class="sxs-lookup"><span data-stu-id="34d61-166">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="34d61-167">-EnableIDBroker</span><span class="sxs-lookup"><span data-stu-id="34d61-167">-EnableIDBroker</span></span>
<span data-ttu-id="34d61-168">Aktiviert HDInsight Identity Broker-Feature.</span><span class="sxs-lookup"><span data-stu-id="34d61-168">Enables HDInsight Identity Broker feature.</span></span>

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

### <span data-ttu-id="34d61-169">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="34d61-169">-EncryptionAlgorithm</span></span>
<span data-ttu-id="34d61-170">Ruft den Verschlüsselungsalgorithmus ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="34d61-170">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="34d61-171">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="34d61-171">-EncryptionAtHost</span></span>
<span data-ttu-id="34d61-172">Ruft das Flag ab, das angibt, ob die Verschlüsselung beim Host aktiviert werden soll, oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="34d61-172">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="34d61-173">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="34d61-173">-EncryptionInTransit</span></span>
<span data-ttu-id="34d61-174">Ruft das Flag ab, das angibt, ob die Verschlüsselung bei der Übertragung aktiviert werden soll, oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="34d61-174">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="34d61-175">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="34d61-175">-EncryptionKeyName</span></span>
<span data-ttu-id="34d61-176">Ruft den Namen des Verschlüsselungsschlüssels ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="34d61-176">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="34d61-177">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="34d61-177">-EncryptionKeyVersion</span></span>
<span data-ttu-id="34d61-178">Ruft die Version des Verschlüsselungsschlüssels ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="34d61-178">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="34d61-179">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="34d61-179">-EncryptionVaultUri</span></span>
<span data-ttu-id="34d61-180">Ruft den Verschlüsselungs Tresor-URI ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="34d61-180">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="34d61-181">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="34d61-181">-HeadNodeSize</span></span>
<span data-ttu-id="34d61-182">Gibt die Größe des virtuellen Computers für den Head-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="34d61-182">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="34d61-183">Verwenden Sie Get-AzVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="34d61-183">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="34d61-184">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="34d61-184">-HiveMetastore</span></span>
<span data-ttu-id="34d61-185">Gibt die SQL-Datenbank zum Speichern von Struktur Metadaten an.</span><span class="sxs-lookup"><span data-stu-id="34d61-185">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="34d61-186">Sie können das Add-AzHDInsightMetastore-Cmdlet auch verwenden.</span><span class="sxs-lookup"><span data-stu-id="34d61-186">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="34d61-187">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="34d61-187">-HttpCredential</span></span>
<span data-ttu-id="34d61-188">Gibt die Anmeldeinformationen für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="34d61-188">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="34d61-189">-KafkaClientGroupId</span><span class="sxs-lookup"><span data-stu-id="34d61-189">-KafkaClientGroupId</span></span>
<span data-ttu-id="34d61-190">Ruft die Clientgruppen-ID für den Kafka-Ruhe Proxy Zugriff ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="34d61-190">Gets or sets the client group id for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="34d61-191">-KafkaClientGroupName</span><span class="sxs-lookup"><span data-stu-id="34d61-191">-KafkaClientGroupName</span></span>
<span data-ttu-id="34d61-192">Ruft den Namen der Clientgruppe für den Zugriff auf Kafka-Ruhe Proxy ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="34d61-192">Gets or sets the client group name for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="34d61-193">-KafkaManagementNodeSize</span><span class="sxs-lookup"><span data-stu-id="34d61-193">-KafkaManagementNodeSize</span></span>
<span data-ttu-id="34d61-194">Ruft die Größe des Kafka-Verwaltungs Knotens ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="34d61-194">Gets or sets the size of the Kafka Management Node.</span></span>

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

### <span data-ttu-id="34d61-195">-Standort</span><span class="sxs-lookup"><span data-stu-id="34d61-195">-Location</span></span>
<span data-ttu-id="34d61-196">Gibt den Speicherort des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="34d61-196">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="34d61-197">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="34d61-197">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="34d61-198">Ruft die minimal unterstützte TLS-Version ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="34d61-198">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="34d61-199">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="34d61-199">-ObjectId</span></span>
<span data-ttu-id="34d61-200">Gibt die Azure AD-Objekt-ID (eine GUID) des Azure AD-Dienst Prinzipals an, der den Cluster darstellt.</span><span class="sxs-lookup"><span data-stu-id="34d61-200">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="34d61-201">Der Cluster verwendet diesen beim Zugriff auf den Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="34d61-201">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="34d61-202">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="34d61-202">-OozieMetastore</span></span>
<span data-ttu-id="34d61-203">Gibt die SQL-Datenbank an, in der Oozie-Metadaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="34d61-203">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="34d61-204">Sie können das Add-AzHDInsightMetastore-Cmdlet auch verwenden.</span><span class="sxs-lookup"><span data-stu-id="34d61-204">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="34d61-205">-OSType</span><span class="sxs-lookup"><span data-stu-id="34d61-205">-OSType</span></span>
<span data-ttu-id="34d61-206">Gibt das Betriebssystem für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="34d61-206">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="34d61-207">Optionen sind: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="34d61-207">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="34d61-208">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="34d61-208">-RdpAccessExpiry</span></span>
<span data-ttu-id="34d61-209">Gibt den Ablauf als DateTime-Objekt für den Zugriff auf einen Cluster mit Remote Desktop Protokoll (RDP) an.</span><span class="sxs-lookup"><span data-stu-id="34d61-209">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="34d61-210">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="34d61-210">-RdpCredential</span></span>
<span data-ttu-id="34d61-211">Gibt die Remote Desktop (RDP)-Anmeldeinformationen für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="34d61-211">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="34d61-212">Dies gilt nur für Windows-Cluster.</span><span class="sxs-lookup"><span data-stu-id="34d61-212">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="34d61-213">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34d61-213">-ResourceGroupName</span></span>
<span data-ttu-id="34d61-214">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="34d61-214">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="34d61-215">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="34d61-215">-ScriptActions</span></span>
<span data-ttu-id="34d61-216">Gibt die Skriptaktionen an, die am Ende der Clustererstellung auf dem Cluster ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="34d61-216">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="34d61-217">Alternativ können Sie Add-AzHDInsightScriptAction verwenden.</span><span class="sxs-lookup"><span data-stu-id="34d61-217">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="34d61-218">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="34d61-218">-SecurityProfile</span></span>
<span data-ttu-id="34d61-219">Gibt die sicherheitsbezogenen Eigenschaften an, die zum Erstellen eines sicheren Clusters verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="34d61-219">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="34d61-220">Sie können das Add-AzHDInsightSecurityProfile-Cmdlet auch verwenden.</span><span class="sxs-lookup"><span data-stu-id="34d61-220">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="34d61-221">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="34d61-221">-SshCredential</span></span>
<span data-ttu-id="34d61-222">Gibt die für SSH-Verbindungen zu verwendenden SSH-Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="34d61-222">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="34d61-223">Dies gilt nur für Linux-Cluster.</span><span class="sxs-lookup"><span data-stu-id="34d61-223">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="34d61-224">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="34d61-224">-SshPublicKey</span></span>
<span data-ttu-id="34d61-225">Gibt den öffentlichen Schlüssel an, der für SSH-Verbindungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="34d61-225">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="34d61-226">Dies gilt nur für Linux-Cluster.</span><span class="sxs-lookup"><span data-stu-id="34d61-226">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="34d61-227">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="34d61-227">-StorageAccountKey</span></span>
<span data-ttu-id="34d61-228">Ruft den Zugriffsschlüssel für das Speicherkonto für das Speicherkonto ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="34d61-228">Gets or sets the Storage Account Access Key for the Storage Account.</span></span>

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

### <span data-ttu-id="34d61-229">-StorageAccountManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="34d61-229">-StorageAccountManagedIdentity</span></span>
<span data-ttu-id="34d61-230">Ruft die verwaltete Identität des speicherkontos ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="34d61-230">Gets or sets the storage account managed identity.</span></span>

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

### <span data-ttu-id="34d61-231">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="34d61-231">-StorageAccountResourceId</span></span>
<span data-ttu-id="34d61-232">Ruft die Speicherressourcen-ID für das Speicherkonto ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="34d61-232">Gets or sets the Storage Resource Id for the Storage Account.</span></span>

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

### <span data-ttu-id="34d61-233">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="34d61-233">-StorageAccountType</span></span>
<span data-ttu-id="34d61-234">Ruft den Typ des speicherkontos ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="34d61-234">Gets or sets the type of the storage account.</span></span>

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

### <span data-ttu-id="34d61-235">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="34d61-235">-StorageContainer</span></span>
<span data-ttu-id="34d61-236">Ruft den StorageContainer-Namen für das standardmäßige Azure Storage-Konto ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="34d61-236">Gets or sets the StorageContainer name for the default Azure Storage Account</span></span>

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

### <span data-ttu-id="34d61-237">-StorageFileSystem</span><span class="sxs-lookup"><span data-stu-id="34d61-237">-StorageFileSystem</span></span>
<span data-ttu-id="34d61-238">Ruft das Dateisystem für das standardmäßige Azure Data Lake-Speicher Gen2-Konto ab oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="34d61-238">Gets or sets the file system for the default Azure Data Lake Storage Gen2 account.</span></span>

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

### <span data-ttu-id="34d61-239">-StorageRootPath</span><span class="sxs-lookup"><span data-stu-id="34d61-239">-StorageRootPath</span></span>
<span data-ttu-id="34d61-240">Ruft den Pfad zum Stamm des Clusters im standardmäßigen Data Lake Store-Konto ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="34d61-240">Gets or sets the path to the root of the cluster in the default Data Lake Store Account.</span></span>

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

### <span data-ttu-id="34d61-241">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="34d61-241">-SubnetName</span></span>
<span data-ttu-id="34d61-242">Ruft den Namen des Subnets für diesen HDInsight-Cluster ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="34d61-242">Gets or sets the subnet name for this HDInsight cluster.</span></span>

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

### <span data-ttu-id="34d61-243">-Version</span><span class="sxs-lookup"><span data-stu-id="34d61-243">-Version</span></span>
<span data-ttu-id="34d61-244">Gibt die HDI-Version des HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="34d61-244">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="34d61-245">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="34d61-245">-VirtualNetworkId</span></span>
<span data-ttu-id="34d61-246">Gibt die ID des virtuellen Netzwerks an, in das der Cluster bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="34d61-246">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="34d61-247">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="34d61-247">-WorkerNodeSize</span></span>
<span data-ttu-id="34d61-248">Gibt die Größe des virtuellen Computers für den Worker-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="34d61-248">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="34d61-249">Verwenden Sie Get-AzVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="34d61-249">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="34d61-250">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="34d61-250">-ZookeeperNodeSize</span></span>
<span data-ttu-id="34d61-251">Gibt die Größe des virtuellen Computers für den zoowärter-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="34d61-251">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="34d61-252">Verwenden Sie Get-AzVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="34d61-252">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="34d61-253">Dieser Parameter ist nur für HBAs oder Storm-Cluster gültig.</span><span class="sxs-lookup"><span data-stu-id="34d61-253">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="34d61-254">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34d61-254">CommonParameters</span></span>
<span data-ttu-id="34d61-255">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34d61-255">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34d61-256">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34d61-256">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34d61-257">Eingaben</span><span class="sxs-lookup"><span data-stu-id="34d61-257">INPUTS</span></span>

### <span data-ttu-id="34d61-258">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="34d61-258">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="34d61-259">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="34d61-259">OUTPUTS</span></span>

### <span data-ttu-id="34d61-260">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="34d61-260">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="34d61-261">Notizen</span><span class="sxs-lookup"><span data-stu-id="34d61-261">NOTES</span></span>
<span data-ttu-id="34d61-262">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Hadoop, hdinsight, HD, Insight</span><span class="sxs-lookup"><span data-stu-id="34d61-262">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="34d61-263">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="34d61-263">RELATED LINKS</span></span>

[<span data-ttu-id="34d61-264">Neu – AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="34d61-264">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

