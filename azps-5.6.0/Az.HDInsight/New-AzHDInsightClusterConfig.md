---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: b5ae1de58a7c3862379e73e852d7b367063c3629
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947128"
---
# <span data-ttu-id="eebfa-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="eebfa-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="eebfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eebfa-102">SYNOPSIS</span></span>
<span data-ttu-id="eebfa-103">Erstellt ein nicht persistiertes Clusterkonfigurationsobjekt, das eine Azure HDInsight-Clusterkonfiguration beschreibt.</span><span class="sxs-lookup"><span data-stu-id="eebfa-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="eebfa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eebfa-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [-StorageAccountResourceId <String>] [-StorageAccountKey <String>]
 [-StorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-MinSupportedTlsVersion <String>]
 [-AssignedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>]
 [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eebfa-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eebfa-105">DESCRIPTION</span></span>
<span data-ttu-id="eebfa-106">Das **Cmdlet New-AzHDInsightClusterConfig** erstellt ein nicht persistiertes Objekt, das eine Azure HDInsight-Clusterkonfiguration beschreibt.</span><span class="sxs-lookup"><span data-stu-id="eebfa-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="eebfa-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="eebfa-107">EXAMPLES</span></span>

### <span data-ttu-id="eebfa-108">Beispiel 1: Erstellen eines Clusterkonfigurationsobjekts</span><span class="sxs-lookup"><span data-stu-id="eebfa-108">Example 1: Create a cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageaccountname"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer
```

<span data-ttu-id="eebfa-109">Mit diesem Befehl wird ein Clusterkonfigurationsobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="eebfa-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="eebfa-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="eebfa-110">PARAMETERS</span></span>

### <span data-ttu-id="eebfa-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="eebfa-111">-AadTenantId</span></span>
<span data-ttu-id="eebfa-112">Gibt die Azure AD-Mandanten-ID an, die beim Zugriff auf Azure Data Lake Store verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="eebfa-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="eebfa-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="eebfa-113">-ApplicationId</span></span>
<span data-ttu-id="eebfa-114">Ruft die Dienstprinzipalanwendungs-ID für den Zugriff auf Azure Data Lake ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="eebfa-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="eebfa-115">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="eebfa-115">-AssignedIdentity</span></span>
<span data-ttu-id="eebfa-116">Ruft die zugewiesene Identität ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="eebfa-116">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="eebfa-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="eebfa-117">-CertificateFileContents</span></span>
<span data-ttu-id="eebfa-118">Gibt den Dateiinhalt des Zertifikats an, das beim Zugriff auf Azure Data Lake Store verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="eebfa-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eebfa-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="eebfa-119">-CertificateFilePath</span></span>
<span data-ttu-id="eebfa-120">Gibt den Dateipfad zu dem Zertifikat an, das zum Authentifizieren als Dienstprinzipal verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="eebfa-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="eebfa-121">Der Cluster verwendet dies beim Zugriff auf Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="eebfa-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="eebfa-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="eebfa-122">-CertificatePassword</span></span>
<span data-ttu-id="eebfa-123">Gibt das Kennwort für das Zertifikat an, das zum Authentifizieren als Dienstprinzipal verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="eebfa-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="eebfa-124">Der Cluster verwendet dies beim Zugriff auf Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="eebfa-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="eebfa-125">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="eebfa-125">-ClusterTier</span></span>
<span data-ttu-id="eebfa-126">Gibt die HDInsight-Clusterebene an.</span><span class="sxs-lookup"><span data-stu-id="eebfa-126">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="eebfa-127">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="eebfa-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="eebfa-128">Standard</span><span class="sxs-lookup"><span data-stu-id="eebfa-128">Standard</span></span>
- <span data-ttu-id="eebfa-129">Premium Der Standardwert ist Standard.</span><span class="sxs-lookup"><span data-stu-id="eebfa-129">Premium The default value is Standard.</span></span>
<span data-ttu-id="eebfa-130">Die Premiumebene kann nur mit Linux-Clustern verwendet werden, und sie ermöglicht die Verwendung einiger neuer Features.</span><span class="sxs-lookup"><span data-stu-id="eebfa-130">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="eebfa-131">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="eebfa-131">-ClusterType</span></span>
<span data-ttu-id="eebfa-132">Gibt den Typ des zu erstellenden Clusters an.</span><span class="sxs-lookup"><span data-stu-id="eebfa-132">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="eebfa-133">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="eebfa-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="eebfa-134">Hadoop</span><span class="sxs-lookup"><span data-stu-id="eebfa-134">Hadoop</span></span>
- <span data-ttu-id="eebfa-135">HBase</span><span class="sxs-lookup"><span data-stu-id="eebfa-135">HBase</span></span>
- <span data-ttu-id="eebfa-136">Storm</span><span class="sxs-lookup"><span data-stu-id="eebfa-136">Storm</span></span>
- <span data-ttu-id="eebfa-137">Spark</span><span class="sxs-lookup"><span data-stu-id="eebfa-137">Spark</span></span>
- <span data-ttu-id="eebfa-138">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="eebfa-138">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="eebfa-139">Kafka</span><span class="sxs-lookup"><span data-stu-id="eebfa-139">Kafka</span></span>
- <span data-ttu-id="eebfa-140">RServer</span><span class="sxs-lookup"><span data-stu-id="eebfa-140">RServer</span></span>

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

### <span data-ttu-id="eebfa-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eebfa-141">-DefaultProfile</span></span>
<span data-ttu-id="eebfa-142">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="eebfa-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eebfa-143">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="eebfa-143">-EdgeNodeSize</span></span>
<span data-ttu-id="eebfa-144">Gibt die Größe des virtuellen Computers für den Edgeknoten an.</span><span class="sxs-lookup"><span data-stu-id="eebfa-144">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="eebfa-145">Verwenden Get-AzVMSize für akzeptable VM-Größen, und lesen Sie die Preisseite von HDInsight.</span><span class="sxs-lookup"><span data-stu-id="eebfa-145">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="eebfa-146">Dieser Parameter ist nur für RServer-Cluster gültig.</span><span class="sxs-lookup"><span data-stu-id="eebfa-146">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="eebfa-147">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="eebfa-147">-EncryptionAlgorithm</span></span>
<span data-ttu-id="eebfa-148">Ruft den Verschlüsselungsalgorithmus ab oder legt den Verschlüsselungsalgorithmus fest.</span><span class="sxs-lookup"><span data-stu-id="eebfa-148">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="eebfa-149">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="eebfa-149">-EncryptionAtHost</span></span>
<span data-ttu-id="eebfa-150">Ruft das -Kennzeichen ab oder legt es fest, das angibt, ob die Verschlüsselung auf dem Host aktiviert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="eebfa-150">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="eebfa-151">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="eebfa-151">-EncryptionInTransit</span></span>
<span data-ttu-id="eebfa-152">Ruft das -Kennzeichen ab oder legt es fest, das angibt, ob die Verschlüsselung bei der Übertragung aktiviert werden soll oder nicht.</span><span class="sxs-lookup"><span data-stu-id="eebfa-152">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="eebfa-153">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="eebfa-153">-EncryptionKeyName</span></span>
<span data-ttu-id="eebfa-154">Ruft den Namen des Verschlüsselungsschlüssels ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="eebfa-154">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="eebfa-155">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="eebfa-155">-EncryptionKeyVersion</span></span>
<span data-ttu-id="eebfa-156">Ruft die Verschlüsselungsschlüsselversion ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="eebfa-156">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="eebfa-157">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="eebfa-157">-EncryptionVaultUri</span></span>
<span data-ttu-id="eebfa-158">Ruft den Verschlüsselungstresor-URI ab oder legt den -URI fest.</span><span class="sxs-lookup"><span data-stu-id="eebfa-158">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="eebfa-159">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="eebfa-159">-HeadNodeSize</span></span>
<span data-ttu-id="eebfa-160">Gibt die Größe des virtuellen Computers für den Knoten Head an.</span><span class="sxs-lookup"><span data-stu-id="eebfa-160">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="eebfa-161">Verwenden Get-AzVMSize für akzeptable VM-Größen, und lesen Sie die Preisseite von HDInsight.</span><span class="sxs-lookup"><span data-stu-id="eebfa-161">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="eebfa-162">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="eebfa-162">-HiveMetastore</span></span>
<span data-ttu-id="eebfa-163">Gibt den Metastore zum Speichern von Hive-Metadaten an.</span><span class="sxs-lookup"><span data-stu-id="eebfa-163">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="eebfa-164">Alternativ können Sie das cmdlet Add-AzHDInsightMetastore verwenden.</span><span class="sxs-lookup"><span data-stu-id="eebfa-164">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="eebfa-165">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="eebfa-165">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="eebfa-166">Ruft die minimal unterstützte TLS-Version ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="eebfa-166">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="eebfa-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="eebfa-167">-ObjectId</span></span>
<span data-ttu-id="eebfa-168">Gibt die Azure AD-Objekt-ID (GUID) des Azure AD-Dienstprinzipals an, der den Cluster darstellt.</span><span class="sxs-lookup"><span data-stu-id="eebfa-168">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="eebfa-169">Der Cluster verwendet dies beim Zugriff auf Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="eebfa-169">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="eebfa-170">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="eebfa-170">-OozieMetastore</span></span>
<span data-ttu-id="eebfa-171">Gibt den Metastore zum Speichern von Oozie-Metadaten an.</span><span class="sxs-lookup"><span data-stu-id="eebfa-171">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="eebfa-172">Alternativ können Sie das **Cmdlet Add-AzHDInsightMetastore** verwenden.</span><span class="sxs-lookup"><span data-stu-id="eebfa-172">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="eebfa-173">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="eebfa-173">-StorageAccountKey</span></span>
<span data-ttu-id="eebfa-174">Ruft den Zugriffsschlüssel für das Speicherkonto ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="eebfa-174">Gets or sets the storage account access key.</span></span>

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

### <span data-ttu-id="eebfa-175">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="eebfa-175">-StorageAccountResourceId</span></span>
<span data-ttu-id="eebfa-176">Ruft die Ressourcen-ID des Speicherkontos ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="eebfa-176">Gets or sets the storage account resource id.</span></span>

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

### <span data-ttu-id="eebfa-177">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="eebfa-177">-StorageAccountType</span></span>
<span data-ttu-id="eebfa-178">Ruft den Typ des Standardspeicherkontos ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="eebfa-178">Gets or sets the type of the default storage account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore, AzureDataLakeStorageGen2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eebfa-179">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="eebfa-179">-WorkerNodeSize</span></span>
<span data-ttu-id="eebfa-180">Gibt die Größe des virtuellen Computers für den Workerknoten an.</span><span class="sxs-lookup"><span data-stu-id="eebfa-180">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="eebfa-181">Verwenden Get-AzVMSize für akzeptable VM-Größen, und lesen Sie die Preisseite von HDInsight.</span><span class="sxs-lookup"><span data-stu-id="eebfa-181">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="eebfa-182">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="eebfa-182">-ZookeeperNodeSize</span></span>
<span data-ttu-id="eebfa-183">Gibt die Größe des virtuellen Computers für den Knoten Zookeeper an.</span><span class="sxs-lookup"><span data-stu-id="eebfa-183">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="eebfa-184">Verwenden Get-AzVMSize für akzeptable VM-Größen, und lesen Sie die Preisseite von HDInsight.</span><span class="sxs-lookup"><span data-stu-id="eebfa-184">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="eebfa-185">Dieser Parameter ist nur für HBase- oder Storm-Cluster gültig.</span><span class="sxs-lookup"><span data-stu-id="eebfa-185">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="eebfa-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eebfa-186">CommonParameters</span></span>
<span data-ttu-id="eebfa-187">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eebfa-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eebfa-188">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eebfa-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eebfa-189">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="eebfa-189">INPUTS</span></span>

### <span data-ttu-id="eebfa-190">Keine</span><span class="sxs-lookup"><span data-stu-id="eebfa-190">None</span></span>

## <span data-ttu-id="eebfa-191">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="eebfa-191">OUTPUTS</span></span>

### <span data-ttu-id="eebfa-192">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="eebfa-192">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="eebfa-193">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="eebfa-193">NOTES</span></span>

## <span data-ttu-id="eebfa-194">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="eebfa-194">RELATED LINKS</span></span>

[<span data-ttu-id="eebfa-195">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="eebfa-195">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


