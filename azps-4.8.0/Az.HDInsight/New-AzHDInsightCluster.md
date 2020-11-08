---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: 9008cb1dba2c39a2c552b2395f4115ca50a17fdf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009286"
---
# <span data-ttu-id="4604e-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="4604e-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="4604e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4604e-102">SYNOPSIS</span></span>
<span data-ttu-id="4604e-103">Erstellt einen Azure HDInsight-Cluster in der angegebenen Ressourcengruppe für das aktuelle Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4604e-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="4604e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4604e-104">SYNTAX</span></span>

### <span data-ttu-id="4604e-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="4604e-105">Default (Default)</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
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
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificatePassword <String>]
 [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DisksPerWorkerNode <Int32>]
 [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>] [-EncryptionAlgorithm <String>]
 [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>]
 [-PublicNetworkAccessType <String>] [-OutboundPublicNetworkAccessType <String>]
 [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4604e-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="4604e-106">CertificateFilePath</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
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
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>]
 [-EncryptionVaultUri <String>] [-PublicNetworkAccessType <String>] [-OutboundPublicNetworkAccessType <String>]
 [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4604e-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="4604e-107">CertificateFileContents</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
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
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>]
 [-EncryptionVaultUri <String>] [-PublicNetworkAccessType <String>] [-OutboundPublicNetworkAccessType <String>]
 [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4604e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4604e-108">DESCRIPTION</span></span>
<span data-ttu-id="4604e-109">Das New-AzHDInsightCluster erstellt einen Azure HDInsight-Cluster mithilfe der angegebenen Parameter oder mithilfe eines mit dem New-AzHDInsightClusterConfig-Cmdlet erstellten Konfigurationsobjekts.</span><span class="sxs-lookup"><span data-stu-id="4604e-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="4604e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4604e-110">EXAMPLES</span></span>

### <span data-ttu-id="4604e-111">Beispiel 1: Erstellen eines Azure HDInsight-Clusters</span><span class="sxs-lookup"><span data-stu-id="4604e-111">Example 1: Create an Azure HDInsight cluster</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
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
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
```

<span data-ttu-id="4604e-112">Dieser Befehl erstellt einen Cluster im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4604e-112">This command creates a cluster in the current subscription.</span></span>

### <span data-ttu-id="4604e-113">Beispiel 2: Erstellen eines Clusters mit vom Kunden verwalteten Schlüsseldaten Träger Verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="4604e-113">Example 2: Create cluster with customer-managed key disk encryption</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
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
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AssignedIdentity $assignedIdentity `
            -EncryptionKeyName $encryptionKeyName `
            -EncryptionVaultUri $encryptionVaultUri `
            -EncryptionKeyVersion $encryptionKeyVersion
```

### <span data-ttu-id="4604e-114">Beispiel 3: Erstellen eines Azure HDInsight-Clusters, der die Verschlüsselung bei der Übertragung ermöglicht</span><span class="sxs-lookup"><span data-stu-id="4604e-114">Example 3: Create an Azure HDInsight cluster which enables encryption in transit</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
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
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionInTransit $true `
```

### <span data-ttu-id="4604e-115">Beispiel 4: Erstellen eines Azure HDInsight-Clusters mit Feature für private Links</span><span class="sxs-lookup"><span data-stu-id="4604e-115">Example 4: Create an Azure HDInsight cluster with private link feature</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
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
        $subnetName="yoursubnetresourceid"

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -VirtualNetworkId $virtualNetworkId -SubnetName $subnetName `
            -PublicNetworkAccessType OutboundOnly -OutboundPublicNetworkAccessType PublicLoadBalancer `
```

### <span data-ttu-id="4604e-116">Beispiel 5: Erstellen eines Azure HDInsight-Clusters, der die Verschlüsselung am Host ermöglicht</span><span class="sxs-lookup"><span data-stu-id="4604e-116">Example 5: Create an Azure HDInsight cluster which enables encryption at host</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
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
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionAtHost $true `
```

### <span data-ttu-id="4604e-117">Beispiel 6: Erstellen eines Azure HDInsight-Clusters, der die autoskala aktiviert.</span><span class="sxs-lookup"><span data-stu-id="4604e-117">Example 6: Create an Azure HDInsight cluster which enables autoscale.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
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
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AutoscaleConfiguration $autoscaleConfiguration
```

## <span data-ttu-id="4604e-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="4604e-118">PARAMETERS</span></span>

### <span data-ttu-id="4604e-119">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="4604e-119">-AadTenantId</span></span>
<span data-ttu-id="4604e-120">Gibt die Azure AD-Mandanten-ID an, die beim Zugriff auf den Azure Data Lake Store verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4604e-120">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="4604e-121">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="4604e-121">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="4604e-122">Gibt die zusätzlichen Azure-Speicherkonten für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="4604e-122">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="4604e-123">Sie können das Add-AzHDInsightStorage-Cmdlet auch verwenden.</span><span class="sxs-lookup"><span data-stu-id="4604e-123">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="4604e-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="4604e-124">-ApplicationId</span></span>
<span data-ttu-id="4604e-125">Ruft die Dienstprinzipal-Anwendungs-ID für den Zugriff auf Azure Data Lake ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="4604e-125">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="4604e-126">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="4604e-126">-AssignedIdentity</span></span>
<span data-ttu-id="4604e-127">Ruft die zugewiesene Identität ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="4604e-127">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="4604e-128">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="4604e-128">-AutoscaleConfiguration</span></span>
<span data-ttu-id="4604e-129">Ruft die Konfiguration des AutoScale ab oder legt diese fest</span><span class="sxs-lookup"><span data-stu-id="4604e-129">Gets or sets the autoscale configuration</span></span>

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

### <span data-ttu-id="4604e-130">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="4604e-130">-CertificateFileContents</span></span>
<span data-ttu-id="4604e-131">Gibt den Dateiinhalt des Zertifikats an, das beim Zugriff auf den Azure Data Lake Store verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4604e-131">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="4604e-132">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="4604e-132">-CertificateFilePath</span></span>
<span data-ttu-id="4604e-133">Gibt den Dateipfad zu dem Zertifikat an, das zur Authentifizierung als Dienstprinzipal verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4604e-133">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="4604e-134">Der Cluster verwendet diesen beim Zugriff auf den Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4604e-134">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="4604e-135">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="4604e-135">-CertificatePassword</span></span>
<span data-ttu-id="4604e-136">Gibt das Kennwort für das Zertifikat an, das für die Authentifizierung als Dienstprinzipal verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4604e-136">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="4604e-137">Der Cluster verwendet diesen beim Zugriff auf den Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4604e-137">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="4604e-138">-Clustername</span><span class="sxs-lookup"><span data-stu-id="4604e-138">-ClusterName</span></span>
<span data-ttu-id="4604e-139">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="4604e-139">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="4604e-140">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="4604e-140">-ClusterSizeInNodes</span></span>
<span data-ttu-id="4604e-141">Gibt die Anzahl der Arbeits Knoten für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="4604e-141">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="4604e-142">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="4604e-142">-ClusterTier</span></span>
<span data-ttu-id="4604e-143">Gibt die HDInsight-Clusterebene an.</span><span class="sxs-lookup"><span data-stu-id="4604e-143">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="4604e-144">Standardmäßig ist dies Standard.</span><span class="sxs-lookup"><span data-stu-id="4604e-144">By default, this is Standard.</span></span>
<span data-ttu-id="4604e-145">Die Premium-Stufe kann nur mit Linux-Clustern verwendet werden und ermöglicht die Verwendung einiger neuer Funktionen.</span><span class="sxs-lookup"><span data-stu-id="4604e-145">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="4604e-146">-Clustertyp</span><span class="sxs-lookup"><span data-stu-id="4604e-146">-ClusterType</span></span>
<span data-ttu-id="4604e-147">Gibt den Typ des zu erstellende Clusters an.</span><span class="sxs-lookup"><span data-stu-id="4604e-147">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="4604e-148">Folgende Optionen stehen zur Auswahl: Hadoop, HBAs, Storm, Spark, INTERACTIVEHIVE, Kafka und RServer</span><span class="sxs-lookup"><span data-stu-id="4604e-148">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

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

### <span data-ttu-id="4604e-149">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="4604e-149">-ComponentVersion</span></span>
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

### <span data-ttu-id="4604e-150">-Config</span><span class="sxs-lookup"><span data-stu-id="4604e-150">-Config</span></span>
<span data-ttu-id="4604e-151">Gibt das Clusterobjekt an, das zum Erstellen des Clusters verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4604e-151">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="4604e-152">Dieses Objekt kann mithilfe des New-AzHDInsightClusterConfig-Cmdlets erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4604e-152">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="4604e-153">-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="4604e-153">-Configurations</span></span>
<span data-ttu-id="4604e-154">Gibt die Konfigurationen dieses HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="4604e-154">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="4604e-155">Sie können das Add-AzHDInsightConfigValues-Cmdlet auch verwenden.</span><span class="sxs-lookup"><span data-stu-id="4604e-155">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="4604e-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4604e-156">-DefaultProfile</span></span>
<span data-ttu-id="4604e-157">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="4604e-157">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4604e-158">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="4604e-158">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="4604e-159">Gibt den Kontoschlüssel für das standardmäßige Azure Storage-Konto an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4604e-159">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="4604e-160">Sie können das Set-AzHDInsightDefaultStorage-Cmdlet auch verwenden.</span><span class="sxs-lookup"><span data-stu-id="4604e-160">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="4604e-161">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4604e-161">-DefaultStorageAccountName</span></span>
<span data-ttu-id="4604e-162">Gibt den Namen des standardmäßigen Azure-speicherkontos an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4604e-162">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="4604e-163">Sie können das Set-AzHDInsightDefaultStorage-Cmdlet auch verwenden.</span><span class="sxs-lookup"><span data-stu-id="4604e-163">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="4604e-164">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="4604e-164">-DefaultStorageAccountType</span></span>
<span data-ttu-id="4604e-165">Gibt den Typ des Standardspeicher Kontos an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4604e-165">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="4604e-166">Mögliche Werte sind AzureStorage und AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="4604e-166">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="4604e-167">Standardmäßig AzureStorage, wenn nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="4604e-167">Defaults to AzureStorage if not specified.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: AzureStorage
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4604e-168">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="4604e-168">-DefaultStorageContainer</span></span>
<span data-ttu-id="4604e-169">Gibt den Namen des Standardcontainers im standardmäßigen Azure Storage-Konto an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4604e-169">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="4604e-170">Sie können das Set-AzHDInsightDefaultStorage-Cmdlet auch verwenden.</span><span class="sxs-lookup"><span data-stu-id="4604e-170">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="4604e-171">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="4604e-171">-DefaultStorageRootPath</span></span>
<span data-ttu-id="4604e-172">Gibt den Pfadpräfix im Data Lake Store-Konto an, das vom HDInsight-Cluster als Standarddateisystem verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4604e-172">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

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

### <span data-ttu-id="4604e-173">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="4604e-173">-DisksPerWorkerNode</span></span>
<span data-ttu-id="4604e-174">Gibt die Anzahl der Datenträger für die Worker-Knoten Rolle im Cluster an.</span><span class="sxs-lookup"><span data-stu-id="4604e-174">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="4604e-175">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="4604e-175">-EdgeNodeSize</span></span>
<span data-ttu-id="4604e-176">Gibt die Größe des virtuellen Computers für den Edge-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="4604e-176">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="4604e-177">Verwenden Sie Get-AzVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="4604e-177">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="4604e-178">Dieser Parameter ist nur für RServer-Cluster gültig.</span><span class="sxs-lookup"><span data-stu-id="4604e-178">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="4604e-179">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="4604e-179">-EncryptionAlgorithm</span></span>
<span data-ttu-id="4604e-180">Ruft den Verschlüsselungsalgorithmus ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="4604e-180">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="4604e-181">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="4604e-181">-EncryptionAtHost</span></span>
<span data-ttu-id="4604e-182">Ruft das Flag ab, das angibt, ob die Verschlüsselung beim Host aktiviert werden soll, oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="4604e-182">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="4604e-183">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="4604e-183">-EncryptionInTransit</span></span>
<span data-ttu-id="4604e-184">Ruft das Flag ab, das angibt, ob die Verschlüsselung bei der Übertragung aktiviert werden soll, oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="4604e-184">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="4604e-185">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="4604e-185">-EncryptionKeyName</span></span>
<span data-ttu-id="4604e-186">Ruft den Namen des Verschlüsselungsschlüssels ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="4604e-186">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="4604e-187">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="4604e-187">-EncryptionKeyVersion</span></span>
<span data-ttu-id="4604e-188">Ruft die Version des Verschlüsselungsschlüssels ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="4604e-188">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="4604e-189">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="4604e-189">-EncryptionVaultUri</span></span>
<span data-ttu-id="4604e-190">Ruft den Verschlüsselungs Tresor-URI ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="4604e-190">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="4604e-191">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="4604e-191">-HeadNodeSize</span></span>
<span data-ttu-id="4604e-192">Gibt die Größe des virtuellen Computers für den Head-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="4604e-192">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="4604e-193">Verwenden Sie Get-AzVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="4604e-193">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="4604e-194">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="4604e-194">-HiveMetastore</span></span>
<span data-ttu-id="4604e-195">Gibt die SQL-Datenbank zum Speichern von Struktur Metadaten an.</span><span class="sxs-lookup"><span data-stu-id="4604e-195">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="4604e-196">Sie können das Add-AzHDInsightMetastore-Cmdlet auch verwenden.</span><span class="sxs-lookup"><span data-stu-id="4604e-196">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="4604e-197">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="4604e-197">-HttpCredential</span></span>
<span data-ttu-id="4604e-198">Gibt die Anmeldeinformationen für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="4604e-198">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="4604e-199">-Standort</span><span class="sxs-lookup"><span data-stu-id="4604e-199">-Location</span></span>
<span data-ttu-id="4604e-200">Gibt den Speicherort des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="4604e-200">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="4604e-201">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="4604e-201">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="4604e-202">Ruft die minimal unterstützte TLS-Version ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="4604e-202">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="4604e-203">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="4604e-203">-ObjectId</span></span>
<span data-ttu-id="4604e-204">Gibt die Azure AD-Objekt-ID (eine GUID) des Azure AD-Dienst Prinzipals an, der den Cluster darstellt.</span><span class="sxs-lookup"><span data-stu-id="4604e-204">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="4604e-205">Der Cluster verwendet diesen beim Zugriff auf den Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4604e-205">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="4604e-206">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="4604e-206">-OozieMetastore</span></span>
<span data-ttu-id="4604e-207">Gibt die SQL-Datenbank an, in der Oozie-Metadaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="4604e-207">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="4604e-208">Sie können das Add-AzHDInsightMetastore-Cmdlet auch verwenden.</span><span class="sxs-lookup"><span data-stu-id="4604e-208">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="4604e-209">-OSType</span><span class="sxs-lookup"><span data-stu-id="4604e-209">-OSType</span></span>
<span data-ttu-id="4604e-210">Gibt das Betriebssystem für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="4604e-210">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="4604e-211">Optionen sind: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="4604e-211">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="4604e-212">-OutboundPublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="4604e-212">-OutboundPublicNetworkAccessType</span></span>
<span data-ttu-id="4604e-213">Ruft den ausgehenden Zugriffstyp für das öffentliche Netzwerk ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="4604e-213">Gets or sets the outbound access type to the public network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PublicLoadBalancer, UDR

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4604e-214">-PublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="4604e-214">-PublicNetworkAccessType</span></span>
<span data-ttu-id="4604e-215">Ruft den Zugriffstyp für öffentliche Netzwerke ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="4604e-215">Gets or sets the public network access type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: InboundAndOutbound, OutboundOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4604e-216">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="4604e-216">-RdpAccessExpiry</span></span>
<span data-ttu-id="4604e-217">Gibt den Ablauf als DateTime-Objekt für den Zugriff auf einen Cluster mit Remote Desktop Protokoll (RDP) an.</span><span class="sxs-lookup"><span data-stu-id="4604e-217">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="4604e-218">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="4604e-218">-RdpCredential</span></span>
<span data-ttu-id="4604e-219">Gibt die Remote Desktop (RDP)-Anmeldeinformationen für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="4604e-219">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="4604e-220">Dies gilt nur für Windows-Cluster.</span><span class="sxs-lookup"><span data-stu-id="4604e-220">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="4604e-221">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4604e-221">-ResourceGroupName</span></span>
<span data-ttu-id="4604e-222">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4604e-222">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="4604e-223">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="4604e-223">-ScriptActions</span></span>
<span data-ttu-id="4604e-224">Gibt die Skriptaktionen an, die am Ende der Clustererstellung auf dem Cluster ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4604e-224">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="4604e-225">Alternativ können Sie Add-AzHDInsightScriptAction verwenden.</span><span class="sxs-lookup"><span data-stu-id="4604e-225">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="4604e-226">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="4604e-226">-SecurityProfile</span></span>
<span data-ttu-id="4604e-227">Gibt die sicherheitsbezogenen Eigenschaften an, die zum Erstellen eines sicheren Clusters verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4604e-227">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="4604e-228">Sie können das Add-AzHDInsightSecurityProfile-Cmdlet auch verwenden.</span><span class="sxs-lookup"><span data-stu-id="4604e-228">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="4604e-229">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="4604e-229">-SshCredential</span></span>
<span data-ttu-id="4604e-230">Gibt die für SSH-Verbindungen zu verwendenden SSH-Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="4604e-230">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="4604e-231">Dies gilt nur für Linux-Cluster.</span><span class="sxs-lookup"><span data-stu-id="4604e-231">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="4604e-232">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="4604e-232">-SshPublicKey</span></span>
<span data-ttu-id="4604e-233">Gibt den öffentlichen Schlüssel an, der für SSH-Verbindungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4604e-233">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="4604e-234">Dies gilt nur für Linux-Cluster.</span><span class="sxs-lookup"><span data-stu-id="4604e-234">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="4604e-235">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="4604e-235">-SubnetName</span></span>
<span data-ttu-id="4604e-236">Gibt den Namen eines Subnetzes im ausgewählten virtuellen Netzwerk für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="4604e-236">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

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

### <span data-ttu-id="4604e-237">-Version</span><span class="sxs-lookup"><span data-stu-id="4604e-237">-Version</span></span>
<span data-ttu-id="4604e-238">Gibt die HDI-Version des HDInsight-Clusters an.</span><span class="sxs-lookup"><span data-stu-id="4604e-238">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="4604e-239">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="4604e-239">-VirtualNetworkId</span></span>
<span data-ttu-id="4604e-240">Gibt die ID des virtuellen Netzwerks an, in das der Cluster bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4604e-240">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="4604e-241">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="4604e-241">-WorkerNodeSize</span></span>
<span data-ttu-id="4604e-242">Gibt die Größe des virtuellen Computers für den Worker-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="4604e-242">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="4604e-243">Verwenden Sie Get-AzVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="4604e-243">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="4604e-244">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="4604e-244">-ZookeeperNodeSize</span></span>
<span data-ttu-id="4604e-245">Gibt die Größe des virtuellen Computers für den zoowärter-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="4604e-245">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="4604e-246">Verwenden Sie Get-AzVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="4604e-246">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="4604e-247">Dieser Parameter ist nur für HBAs oder Storm-Cluster gültig.</span><span class="sxs-lookup"><span data-stu-id="4604e-247">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="4604e-248">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4604e-248">CommonParameters</span></span>
<span data-ttu-id="4604e-249">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4604e-249">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4604e-250">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4604e-250">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4604e-251">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4604e-251">INPUTS</span></span>

### <span data-ttu-id="4604e-252">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="4604e-252">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="4604e-253">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4604e-253">OUTPUTS</span></span>

### <span data-ttu-id="4604e-254">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="4604e-254">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="4604e-255">Notizen</span><span class="sxs-lookup"><span data-stu-id="4604e-255">NOTES</span></span>
<span data-ttu-id="4604e-256">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Hadoop, hdinsight, HD, Insight</span><span class="sxs-lookup"><span data-stu-id="4604e-256">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="4604e-257">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4604e-257">RELATED LINKS</span></span>

[<span data-ttu-id="4604e-258">Neu – AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="4604e-258">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

