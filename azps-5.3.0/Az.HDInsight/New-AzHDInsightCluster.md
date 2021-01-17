---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: f4592a371e528c7779e07251bf79677dac47e6df
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458515"
---
# <span data-ttu-id="f7dcd-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f7dcd-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="f7dcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7dcd-102">SYNOPSIS</span></span>
<span data-ttu-id="f7dcd-103">Erstellt einen Azure -HDInsight-Cluster in der angegebenen Ressourcengruppe für das aktuelle Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="f7dcd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7dcd-104">SYNTAX</span></span>

### <span data-ttu-id="f7dcd-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="f7dcd-105">Default (Default)</span></span>
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
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7dcd-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="f7dcd-106">CertificateFilePath</span></span>
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
 [-PrivateLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7dcd-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="f7dcd-107">CertificateFileContents</span></span>
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
 [-PrivateLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7dcd-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f7dcd-108">DESCRIPTION</span></span>
<span data-ttu-id="f7dcd-109">Die New-AzHDInsightCluster erstellt einen Azure HDInsight-Cluster mithilfe der angegebenen Parameter oder mithilfe eines Konfigurationsobjekts, das mit dem cmdlet New-AzHDInsightClusterConfig erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="f7dcd-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f7dcd-110">EXAMPLES</span></span>

### <span data-ttu-id="f7dcd-111">Beispiel 1: Erstellen eines Azure -HDInsight-Cluster</span><span class="sxs-lookup"><span data-stu-id="f7dcd-111">Example 1: Create an Azure HDInsight cluster</span></span>
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

<span data-ttu-id="f7dcd-112">Mit diesem Befehl wird im aktuellen Abonnement ein Cluster erstellt.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-112">This command creates a cluster in the current subscription.</span></span>

### <span data-ttu-id="f7dcd-113">Beispiel 2: Erstellen eines Clusters mit vom Kunden verwalteter Schlüsseldatenträgerverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="f7dcd-113">Example 2: Create cluster with customer-managed key disk encryption</span></span>
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

### <span data-ttu-id="f7dcd-114">Beispiel 3: Erstellen eines Azure HDInsight-Cluster, der Verschlüsselung bei der Übertragung ermöglicht</span><span class="sxs-lookup"><span data-stu-id="f7dcd-114">Example 3: Create an Azure HDInsight cluster which enables encryption in transit</span></span>
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

### <span data-ttu-id="f7dcd-115">Beispiel 4: Erstellen eines Azure -HDInsight-Cluster mit funktion "Ausgehende und private Weiterleitung"</span><span class="sxs-lookup"><span data-stu-id="f7dcd-115">Example 4: Create an Azure HDInsight cluster with relay outbound and private link feature</span></span>
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
            -ResourceProviderConnection Outbound -PrivateLink Enabled `
```

### <span data-ttu-id="f7dcd-116">Beispiel 5: Erstellen eines Azure -HDInsight-Cluster, der Verschlüsselung auf dem Host ermöglicht</span><span class="sxs-lookup"><span data-stu-id="f7dcd-116">Example 5: Create an Azure HDInsight cluster which enables encryption at host</span></span>
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

### <span data-ttu-id="f7dcd-117">Beispiel 6: Erstellen eines Azure HDInsight-Cluster, der die Automatische Skalierung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-117">Example 6: Create an Azure HDInsight cluster which enables autoscale.</span></span>
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

### <span data-ttu-id="f7dcd-118">Beispiel 7: Erstellen eines Azure -HDInsight-Cluster mit Kafka Rest Proxy.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-118">Example 7: Create an Azure HDInsight cluster with Kafka Rest Proxy.</span></span>
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

### <span data-ttu-id="f7dcd-119">Beispiel 8: Erstellen eines Azure -HDInsight-Cluster mit Azure Data Lake Gen2-Speicher.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-119">Example 8: Create an Azure HDInsight cluster with Azure Data Lake Gen2 storage.</span></span>
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

### <span data-ttu-id="f7dcd-120">Beispiel 9: Erstellen eines Azure -HDInsight-Cluster mit Enterprise Security Package (ESP) und Aktivieren des HDInsight-ID-Brokers.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-120">Example 9: Create an Azure HDInsight cluster with Enterprise Security Package(ESP) and Enable HDInsight ID Broker.</span></span>
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

## <span data-ttu-id="f7dcd-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7dcd-121">PARAMETERS</span></span>

### <span data-ttu-id="f7dcd-122">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="f7dcd-122">-AadTenantId</span></span>
<span data-ttu-id="f7dcd-123">Gibt die Azure AD-Mandanten-ID an, die beim Zugriff auf Azure Data Lake Store verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-123">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f7dcd-124">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="f7dcd-124">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="f7dcd-125">Gibt die zusätzlichen Azure Storage-Konten für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-125">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="f7dcd-126">Alternativ können Sie das Add-AzHDInsightStorage verwenden.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-126">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="f7dcd-127">-DeserariDatabase</span><span class="sxs-lookup"><span data-stu-id="f7dcd-127">-AmbariDatabase</span></span>
<span data-ttu-id="f7dcd-128">Ruft die Datenbank für "aria" ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-128">Gets or sets the database for ambari.</span></span>

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

### <span data-ttu-id="f7dcd-129">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f7dcd-129">-ApplicationId</span></span>
<span data-ttu-id="f7dcd-130">Ruft die Dienstprinzipalanwendungs-ID für den Zugriff auf Azure Data Lake ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-130">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="f7dcd-131">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="f7dcd-131">-AssignedIdentity</span></span>
<span data-ttu-id="f7dcd-132">Ruft die zugewiesene Identität ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-132">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="f7dcd-133">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7dcd-133">-AutoscaleConfiguration</span></span>
<span data-ttu-id="f7dcd-134">Ruft die Konfiguration der automatischen Skala ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-134">Gets or sets the autoscale configuration</span></span>

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

### <span data-ttu-id="f7dcd-135">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="f7dcd-135">-CertificateFileContents</span></span>
<span data-ttu-id="f7dcd-136">Gibt den Dateiinhalt des Zertifikats an, das beim Zugriff auf Azure Data Lake Store verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-136">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f7dcd-137">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="f7dcd-137">-CertificateFilePath</span></span>
<span data-ttu-id="f7dcd-138">Gibt den Dateipfad des Zertifikats an, das zur Authentifizierung als Dienstprinzipal verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-138">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="f7dcd-139">Der Cluster verwendet dies beim Zugriff auf Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-139">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f7dcd-140">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="f7dcd-140">-CertificatePassword</span></span>
<span data-ttu-id="f7dcd-141">Gibt das Kennwort für das Zertifikat an, das zur Authentifizierung als Dienstprinzipal verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-141">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="f7dcd-142">Der Cluster verwendet dies beim Zugriff auf Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-142">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f7dcd-143">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f7dcd-143">-ClusterName</span></span>
<span data-ttu-id="f7dcd-144">Gibt den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-144">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="f7dcd-145">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="f7dcd-145">-ClusterSizeInNodes</span></span>
<span data-ttu-id="f7dcd-146">Gibt die Anzahl der Workerknoten für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-146">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="f7dcd-147">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="f7dcd-147">-ClusterTier</span></span>
<span data-ttu-id="f7dcd-148">Gibt die Clusterebene "HDInsight" an.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-148">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="f7dcd-149">Standardmäßig ist dies Standard.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-149">By default, this is Standard.</span></span>
<span data-ttu-id="f7dcd-150">Das Premium-Tier kann nur mit Linux-Clustern verwendet werden, und es ermöglicht die Verwendung einiger neuer Features.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-150">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="f7dcd-151">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="f7dcd-151">-ClusterType</span></span>
<span data-ttu-id="f7dcd-152">Gibt den Typ des zu erstellenden Clusters an.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-152">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="f7dcd-153">Optionen sind: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka und RServer</span><span class="sxs-lookup"><span data-stu-id="f7dcd-153">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

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

### <span data-ttu-id="f7dcd-154">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="f7dcd-154">-ComponentVersion</span></span>
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

### <span data-ttu-id="f7dcd-155">-Config</span><span class="sxs-lookup"><span data-stu-id="f7dcd-155">-Config</span></span>
<span data-ttu-id="f7dcd-156">Gibt das Clusterobjekt an, das zum Erstellen des Clusters verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-156">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="f7dcd-157">Dieses Objekt kann mithilfe des cmdlets New-AzHDInsightClusterConfig erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-157">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="f7dcd-158">-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="f7dcd-158">-Configurations</span></span>
<span data-ttu-id="f7dcd-159">Gibt die Konfigurationen dieses Cluster "HDInsight" an.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-159">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="f7dcd-160">Alternativ können Sie das Add-AzHDInsightConfigValues verwenden.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-160">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="f7dcd-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7dcd-161">-DefaultProfile</span></span>
<span data-ttu-id="f7dcd-162">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f7dcd-162">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7dcd-163">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="f7dcd-163">-DisksPerWorkerNode</span></span>
<span data-ttu-id="f7dcd-164">Gibt die Anzahl der Datenträger für die Rolle des Workerknotens im Cluster an.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-164">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="f7dcd-165">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="f7dcd-165">-EdgeNodeSize</span></span>
<span data-ttu-id="f7dcd-166">Gibt die Größe des virtuellen Computers für den Edgeknoten an.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-166">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="f7dcd-167">Verwenden Get-AzVMSize für akzeptable Größen für virtuelle Computer, und lesen Sie die Preisseite von HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-167">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="f7dcd-168">Dieser Parameter ist nur für RServer-Cluster gültig.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-168">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="f7dcd-169">-EnableIDBroker</span><span class="sxs-lookup"><span data-stu-id="f7dcd-169">-EnableIDBroker</span></span>
<span data-ttu-id="f7dcd-170">Aktiviert das Feature "HDInsight-Identitätsbroker".</span><span class="sxs-lookup"><span data-stu-id="f7dcd-170">Enables HDInsight Identity Broker feature.</span></span>

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

### <span data-ttu-id="f7dcd-171">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="f7dcd-171">-EncryptionAlgorithm</span></span>
<span data-ttu-id="f7dcd-172">Ruft den Verschlüsselungsalgorithmus ab oder legt den Algorithmus fest.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-172">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="f7dcd-173">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="f7dcd-173">-EncryptionAtHost</span></span>
<span data-ttu-id="f7dcd-174">Ruft das Kennzeichen ab oder legt es fest, das angibt, ob die Verschlüsselung auf dem Host aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-174">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="f7dcd-175">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="f7dcd-175">-EncryptionInTransit</span></span>
<span data-ttu-id="f7dcd-176">Ruft das Kennzeichen ab oder legt es fest, das angibt, ob die Verschlüsselung bei der Übertragung aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-176">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="f7dcd-177">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="f7dcd-177">-EncryptionKeyName</span></span>
<span data-ttu-id="f7dcd-178">Ruft den Namen des Verschlüsselungsschlüssels ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-178">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="f7dcd-179">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="f7dcd-179">-EncryptionKeyVersion</span></span>
<span data-ttu-id="f7dcd-180">Ruft die Verschlüsselungsschlüsselversion ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-180">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="f7dcd-181">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="f7dcd-181">-EncryptionVaultUri</span></span>
<span data-ttu-id="f7dcd-182">Ruft den Verschlüsselungstresor-URI ab oder legt den URI fest.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-182">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="f7dcd-183">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="f7dcd-183">-HeadNodeSize</span></span>
<span data-ttu-id="f7dcd-184">Gibt die Größe des virtuellen Computers für den Head-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-184">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="f7dcd-185">Verwenden Get-AzVMSize für akzeptable Größen für virtuelle Computer, und lesen Sie die Preisseite von HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-185">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="f7dcd-186">-StruktureMetastore</span><span class="sxs-lookup"><span data-stu-id="f7dcd-186">-HiveMetastore</span></span>
<span data-ttu-id="f7dcd-187">Gibt die SQL Datenbank an, in der Strukturmetadaten gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-187">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="f7dcd-188">Alternativ können Sie das Add-AzHDInsightMetastore verwenden.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-188">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="f7dcd-189">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="f7dcd-189">-HttpCredential</span></span>
<span data-ttu-id="f7dcd-190">Gibt die Anmeldeinformationen für den Cluster (Cluster Login, HTTP) für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-190">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="f7dcd-191">-KafkaClientGroupId</span><span class="sxs-lookup"><span data-stu-id="f7dcd-191">-KafkaClientGroupId</span></span>
<span data-ttu-id="f7dcd-192">Ruft die Clientgruppen-ID für Kafka Rest Proxy Access ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-192">Gets or sets the client group id for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="f7dcd-193">-KafkaClientGroupName</span><span class="sxs-lookup"><span data-stu-id="f7dcd-193">-KafkaClientGroupName</span></span>
<span data-ttu-id="f7dcd-194">Ruft den Clientgruppennamen für Kafka Rest Proxy Access ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-194">Gets or sets the client group name for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="f7dcd-195">-KafkaManagementNodeSize</span><span class="sxs-lookup"><span data-stu-id="f7dcd-195">-KafkaManagementNodeSize</span></span>
<span data-ttu-id="f7dcd-196">Ruft die Größe des Verwaltungsknotens für Kafka ab oder legt die Größe fest.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-196">Gets or sets the size of the Kafka Management Node.</span></span>

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

### <span data-ttu-id="f7dcd-197">-Location</span><span class="sxs-lookup"><span data-stu-id="f7dcd-197">-Location</span></span>
<span data-ttu-id="f7dcd-198">Gibt die Position für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-198">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="f7dcd-199">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="f7dcd-199">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="f7dcd-200">Ruft die minimale unterstützte Version von TLS ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-200">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="f7dcd-201">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f7dcd-201">-ObjectId</span></span>
<span data-ttu-id="f7dcd-202">Gibt die Azure AD-Objekt-ID (GUID) des Azure AD-Dienstprinzipal an, der den Cluster darstellt.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-202">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="f7dcd-203">Der Cluster verwendet dies beim Zugriff auf Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-203">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f7dcd-204">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="f7dcd-204">-OozieMetastore</span></span>
<span data-ttu-id="f7dcd-205">Gibt die SQL Datenbank an, in der die Metadaten von Oozie gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-205">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="f7dcd-206">Alternativ können Sie das Add-AzHDInsightMetastore verwenden.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-206">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="f7dcd-207">-OSType</span><span class="sxs-lookup"><span data-stu-id="f7dcd-207">-OSType</span></span>
<span data-ttu-id="f7dcd-208">Gibt das Betriebssystem für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-208">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="f7dcd-209">Optionen sind: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="f7dcd-209">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="f7dcd-210">-PrivateLink</span><span class="sxs-lookup"><span data-stu-id="f7dcd-210">-PrivateLink</span></span>
<span data-ttu-id="f7dcd-211">Ruft den privaten Linktyp ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-211">Gets or sets the private link type.</span></span>

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

### <span data-ttu-id="f7dcd-212">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="f7dcd-212">-RdpAccessExpiry</span></span>
<span data-ttu-id="f7dcd-213">Gibt den Ablauf (als DateTime-Objekt) für den Remotedesktopprotokoll(RDP)-Zugriff auf einen Cluster an.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-213">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="f7dcd-214">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="f7dcd-214">-RdpCredential</span></span>
<span data-ttu-id="f7dcd-215">Gibt die Remotedesktopanmeldeinformationen für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-215">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="f7dcd-216">Dies gilt nur für Windows-Cluster.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-216">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="f7dcd-217">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7dcd-217">-ResourceGroupName</span></span>
<span data-ttu-id="f7dcd-218">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-218">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f7dcd-219">-ResourceProviderConnection</span><span class="sxs-lookup"><span data-stu-id="f7dcd-219">-ResourceProviderConnection</span></span>
<span data-ttu-id="f7dcd-220">Ruft den Verbindungstyp des Ressourcenanbieters ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-220">Gets or sets the resource provider connection type.</span></span>

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

### <span data-ttu-id="f7dcd-221">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="f7dcd-221">-ScriptActions</span></span>
<span data-ttu-id="f7dcd-222">Gibt die Skriptaktionen an, die am Ende der Clustererstellung für den Cluster ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-222">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="f7dcd-223">Alternativ können Sie Add-AzHDInsightScriptAction verwenden.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-223">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="f7dcd-224">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="f7dcd-224">-SecurityProfile</span></span>
<span data-ttu-id="f7dcd-225">Gibt die sicherheitsbezogenen Eigenschaften an, die zum Erstellen eines sicheren Cluster verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-225">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="f7dcd-226">Alternativ können Sie das Add-AzHDInsightSecurityProfile verwenden.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-226">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="f7dcd-227">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="f7dcd-227">-SshCredential</span></span>
<span data-ttu-id="f7dcd-228">Gibt die SSH-Anmeldeinformationen an, die für SSH-Verbindungen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-228">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="f7dcd-229">Dies gilt nur für Linux-Cluster.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-229">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="f7dcd-230">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="f7dcd-230">-SshPublicKey</span></span>
<span data-ttu-id="f7dcd-231">Gibt den öffentlichen Schlüssel an, der für SSH-Verbindungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-231">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="f7dcd-232">Dies gilt nur für Linux-Cluster.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-232">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="f7dcd-233">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f7dcd-233">-StorageAccountKey</span></span>
<span data-ttu-id="f7dcd-234">Ruft den Zugriffsschlüssel für das Speicherkonto ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-234">Gets or sets the Storage Account Access Key for the Storage Account.</span></span>

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

### <span data-ttu-id="f7dcd-235">-StorageAccountManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="f7dcd-235">-StorageAccountManagedIdentity</span></span>
<span data-ttu-id="f7dcd-236">Ruft die verwaltete Identität des Speicherkontos ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-236">Gets or sets the storage account managed identity.</span></span>

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

### <span data-ttu-id="f7dcd-237">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="f7dcd-237">-StorageAccountResourceId</span></span>
<span data-ttu-id="f7dcd-238">Ruft die Speicherressourcen-ID für das Speicherkonto ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-238">Gets or sets the Storage Resource Id for the Storage Account.</span></span>

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

### <span data-ttu-id="f7dcd-239">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="f7dcd-239">-StorageAccountType</span></span>
<span data-ttu-id="f7dcd-240">Ruft den Typ des Speicherkontos ab oder legt diesen Typ fest.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-240">Gets or sets the type of the storage account.</span></span>

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

### <span data-ttu-id="f7dcd-241">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="f7dcd-241">-StorageContainer</span></span>
<span data-ttu-id="f7dcd-242">Ruft den Namen des StorageContainers für das standardmäßige Azure -Speicherkonto ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-242">Gets or sets the StorageContainer name for the default Azure Storage Account</span></span>

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

### <span data-ttu-id="f7dcd-243">-StorageFileSystem</span><span class="sxs-lookup"><span data-stu-id="f7dcd-243">-StorageFileSystem</span></span>
<span data-ttu-id="f7dcd-244">Ruft das Dateisystem für das standardmäßige Azure Data Lake Storage Gen2-Konto ab oder legt es fest.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-244">Gets or sets the file system for the default Azure Data Lake Storage Gen2 account.</span></span>

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

### <span data-ttu-id="f7dcd-245">-StorageRootPath</span><span class="sxs-lookup"><span data-stu-id="f7dcd-245">-StorageRootPath</span></span>
<span data-ttu-id="f7dcd-246">Ruft den Pfad zur Stammgruppe des Clusters im standardmäßigen Data Lake Store Account ab oder legt den Pfad fest.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-246">Gets or sets the path to the root of the cluster in the default Data Lake Store Account.</span></span>

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

### <span data-ttu-id="f7dcd-247">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="f7dcd-247">-SubnetName</span></span>
<span data-ttu-id="f7dcd-248">Ruft den Subnetznamen für diesen Cluster "HDInsight" ab oder legt diesen namen fest.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-248">Gets or sets the subnet name for this HDInsight cluster.</span></span>

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

### <span data-ttu-id="f7dcd-249">-Version</span><span class="sxs-lookup"><span data-stu-id="f7dcd-249">-Version</span></span>
<span data-ttu-id="f7dcd-250">Gibt die HDI-Version des Cluster "HDInsight" an.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-250">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="f7dcd-251">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="f7dcd-251">-VirtualNetworkId</span></span>
<span data-ttu-id="f7dcd-252">Gibt die ID des virtuellen Netzwerks an, in dem der Cluster bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-252">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="f7dcd-253">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="f7dcd-253">-WorkerNodeSize</span></span>
<span data-ttu-id="f7dcd-254">Gibt die Größe des virtuellen Computers für den Workerknoten an.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-254">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="f7dcd-255">Verwenden Get-AzVMSize für akzeptable Größen für virtuelle Computer, und lesen Sie die Preisseite von HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-255">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="f7dcd-256">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="f7dcd-256">-ZookeeperNodeSize</span></span>
<span data-ttu-id="f7dcd-257">Gibt die Größe des virtuellen Computers für den Knoten "Zookeeper" an.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-257">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="f7dcd-258">Verwenden Get-AzVMSize für akzeptable Größen für virtuelle Computer, und lesen Sie die Preisseite von HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-258">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="f7dcd-259">Dieser Parameter ist nur für HBase- oder Storm-Cluster gültig.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-259">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="f7dcd-260">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7dcd-260">CommonParameters</span></span>
<span data-ttu-id="f7dcd-261">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-261">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7dcd-262">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7dcd-262">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7dcd-263">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f7dcd-263">INPUTS</span></span>

### <span data-ttu-id="f7dcd-264">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="f7dcd-264">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="f7dcd-265">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f7dcd-265">OUTPUTS</span></span>

### <span data-ttu-id="f7dcd-266">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f7dcd-266">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="f7dcd-267">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f7dcd-267">NOTES</span></span>
<span data-ttu-id="f7dcd-268">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span><span class="sxs-lookup"><span data-stu-id="f7dcd-268">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="f7dcd-269">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f7dcd-269">RELATED LINKS</span></span>

[<span data-ttu-id="f7dcd-270">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="f7dcd-270">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

