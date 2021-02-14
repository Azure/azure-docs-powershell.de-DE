---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 1124136a580d0079690c60e31fe8de8649e3cafb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167500"
---
# <span data-ttu-id="46b3e-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="46b3e-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="46b3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46b3e-102">SYNOPSIS</span></span>
<span data-ttu-id="46b3e-103">Erstellt ein nicht beibehaltenes Clusterkonfigurationsobjekt, das eine Konfiguration des Azure -HDInsight-Cluster beschreibt.</span><span class="sxs-lookup"><span data-stu-id="46b3e-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="46b3e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46b3e-104">SYNTAX</span></span>

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

## <span data-ttu-id="46b3e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46b3e-105">DESCRIPTION</span></span>
<span data-ttu-id="46b3e-106">Das **Cmdlet "New-AzHDInsightClusterConfig"** erstellt ein nicht beibehaltenes Objekt, das eine Konfiguration des Azure -HDInsight-Cluster beschreibt.</span><span class="sxs-lookup"><span data-stu-id="46b3e-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="46b3e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="46b3e-107">EXAMPLES</span></span>

### <span data-ttu-id="46b3e-108">Beispiel 1: Erstellen eines Clusterkonfigurationsobjekts</span><span class="sxs-lookup"><span data-stu-id="46b3e-108">Example 1: Create a cluster configuration object</span></span>
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

<span data-ttu-id="46b3e-109">Mit diesem Befehl wird ein Clusterkonfigurationsobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="46b3e-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="46b3e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46b3e-110">PARAMETERS</span></span>

### <span data-ttu-id="46b3e-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="46b3e-111">-AadTenantId</span></span>
<span data-ttu-id="46b3e-112">Gibt die Azure AD-Mandanten-ID an, die beim Zugriff auf Azure Data Lake Store verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="46b3e-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="46b3e-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="46b3e-113">-ApplicationId</span></span>
<span data-ttu-id="46b3e-114">Ruft die Dienstprinzipalanwendungs-ID für den Zugriff auf Azure Data Lake ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="46b3e-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="46b3e-115">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="46b3e-115">-AssignedIdentity</span></span>
<span data-ttu-id="46b3e-116">Ruft die zugewiesene Identität ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="46b3e-116">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="46b3e-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="46b3e-117">-CertificateFileContents</span></span>
<span data-ttu-id="46b3e-118">Gibt den Dateiinhalt des Zertifikats an, das beim Zugriff auf Azure Data Lake Store verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="46b3e-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="46b3e-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="46b3e-119">-CertificateFilePath</span></span>
<span data-ttu-id="46b3e-120">Gibt den Dateipfad des Zertifikats an, das zur Authentifizierung als Dienstprinzipal verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="46b3e-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="46b3e-121">Der Cluster verwendet dies beim Zugriff auf Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="46b3e-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="46b3e-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="46b3e-122">-CertificatePassword</span></span>
<span data-ttu-id="46b3e-123">Gibt das Kennwort für das Zertifikat an, das zur Authentifizierung als Dienstprinzipal verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="46b3e-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="46b3e-124">Der Cluster verwendet dies beim Zugriff auf Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="46b3e-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="46b3e-125">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="46b3e-125">-ClusterTier</span></span>
<span data-ttu-id="46b3e-126">Gibt die Clusterebene "HDInsight" an.</span><span class="sxs-lookup"><span data-stu-id="46b3e-126">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="46b3e-127">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="46b3e-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="46b3e-128">Standard</span><span class="sxs-lookup"><span data-stu-id="46b3e-128">Standard</span></span>
- <span data-ttu-id="46b3e-129">Premium Der Standardwert ist "Standard".</span><span class="sxs-lookup"><span data-stu-id="46b3e-129">Premium The default value is Standard.</span></span>
<span data-ttu-id="46b3e-130">Das Premium-Tier kann nur mit Linux-Clustern verwendet werden, und es ermöglicht die Verwendung einiger neuer Features.</span><span class="sxs-lookup"><span data-stu-id="46b3e-130">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="46b3e-131">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="46b3e-131">-ClusterType</span></span>
<span data-ttu-id="46b3e-132">Gibt den Typ des zu erstellenden Clusters an.</span><span class="sxs-lookup"><span data-stu-id="46b3e-132">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="46b3e-133">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="46b3e-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="46b3e-134">Hadoop</span><span class="sxs-lookup"><span data-stu-id="46b3e-134">Hadoop</span></span>
- <span data-ttu-id="46b3e-135">HBase</span><span class="sxs-lookup"><span data-stu-id="46b3e-135">HBase</span></span>
- <span data-ttu-id="46b3e-136">Regen</span><span class="sxs-lookup"><span data-stu-id="46b3e-136">Storm</span></span>
- <span data-ttu-id="46b3e-137">Spark</span><span class="sxs-lookup"><span data-stu-id="46b3e-137">Spark</span></span>
- <span data-ttu-id="46b3e-138">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="46b3e-138">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="46b3e-139">Kafka</span><span class="sxs-lookup"><span data-stu-id="46b3e-139">Kafka</span></span>
- <span data-ttu-id="46b3e-140">RServer</span><span class="sxs-lookup"><span data-stu-id="46b3e-140">RServer</span></span>

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

### <span data-ttu-id="46b3e-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46b3e-141">-DefaultProfile</span></span>
<span data-ttu-id="46b3e-142">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="46b3e-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46b3e-143">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="46b3e-143">-EdgeNodeSize</span></span>
<span data-ttu-id="46b3e-144">Gibt die Größe des virtuellen Computers für den Edgeknoten an.</span><span class="sxs-lookup"><span data-stu-id="46b3e-144">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="46b3e-145">Verwenden Get-AzVMSize für akzeptable Größen für virtuelle Computer, und sehen Sie sich die Preisseite von HDInsight an.</span><span class="sxs-lookup"><span data-stu-id="46b3e-145">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="46b3e-146">Dieser Parameter ist nur für RServer-Cluster gültig.</span><span class="sxs-lookup"><span data-stu-id="46b3e-146">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="46b3e-147">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="46b3e-147">-EncryptionAlgorithm</span></span>
<span data-ttu-id="46b3e-148">Ruft den Verschlüsselungsalgorithmus ab oder legt den Algorithmus fest.</span><span class="sxs-lookup"><span data-stu-id="46b3e-148">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="46b3e-149">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="46b3e-149">-EncryptionAtHost</span></span>
<span data-ttu-id="46b3e-150">Ruft das Kennzeichen ab oder legt es fest, das angibt, ob die Verschlüsselung auf dem Host aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="46b3e-150">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="46b3e-151">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="46b3e-151">-EncryptionInTransit</span></span>
<span data-ttu-id="46b3e-152">Ruft das Kennzeichen ab oder legt es fest, das angibt, ob die Verschlüsselung bei der Übertragung aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="46b3e-152">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="46b3e-153">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="46b3e-153">-EncryptionKeyName</span></span>
<span data-ttu-id="46b3e-154">Ruft den Namen des Verschlüsselungsschlüssels ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="46b3e-154">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="46b3e-155">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="46b3e-155">-EncryptionKeyVersion</span></span>
<span data-ttu-id="46b3e-156">Ruft die Verschlüsselungsschlüsselversion ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="46b3e-156">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="46b3e-157">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="46b3e-157">-EncryptionVaultUri</span></span>
<span data-ttu-id="46b3e-158">Ruft den Verschlüsselungstresor-URI ab oder legt den URI fest.</span><span class="sxs-lookup"><span data-stu-id="46b3e-158">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="46b3e-159">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="46b3e-159">-HeadNodeSize</span></span>
<span data-ttu-id="46b3e-160">Gibt die Größe des virtuellen Computers für den Head-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="46b3e-160">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="46b3e-161">Verwenden Get-AzVMSize für akzeptable Größen für virtuelle Computer, und sehen Sie sich die Preisseite von HDInsight an.</span><span class="sxs-lookup"><span data-stu-id="46b3e-161">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="46b3e-162">-StruktureMetastore</span><span class="sxs-lookup"><span data-stu-id="46b3e-162">-HiveMetastore</span></span>
<span data-ttu-id="46b3e-163">Gibt den Metastore an, in dem Strukturmetadaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="46b3e-163">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="46b3e-164">Alternativ können Sie das Add-AzHDInsightMetastore verwenden.</span><span class="sxs-lookup"><span data-stu-id="46b3e-164">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="46b3e-165">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="46b3e-165">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="46b3e-166">Ruft die minimale unterstützte Version von TLS ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="46b3e-166">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="46b3e-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="46b3e-167">-ObjectId</span></span>
<span data-ttu-id="46b3e-168">Gibt die Azure AD-Objekt-ID (GUID) des Azure AD-Dienstprinzipal an, der den Cluster darstellt.</span><span class="sxs-lookup"><span data-stu-id="46b3e-168">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="46b3e-169">Der Cluster verwendet dies beim Zugriff auf Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="46b3e-169">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="46b3e-170">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="46b3e-170">-OozieMetastore</span></span>
<span data-ttu-id="46b3e-171">Gibt den Metastore an, in dem die Metadaten von Oozie gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="46b3e-171">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="46b3e-172">Alternativ können Sie das **Cmdlet "Add-AzHDInsightMetastore"** verwenden.</span><span class="sxs-lookup"><span data-stu-id="46b3e-172">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="46b3e-173">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="46b3e-173">-StorageAccountKey</span></span>
<span data-ttu-id="46b3e-174">Ruft den Zugriffsschlüssel für das Speicherkonto ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="46b3e-174">Gets or sets the storage account access key.</span></span>

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

### <span data-ttu-id="46b3e-175">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="46b3e-175">-StorageAccountResourceId</span></span>
<span data-ttu-id="46b3e-176">Ruft die Ressourcen-ID des Speicherkontos ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="46b3e-176">Gets or sets the storage account resource id.</span></span>

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

### <span data-ttu-id="46b3e-177">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="46b3e-177">-StorageAccountType</span></span>
<span data-ttu-id="46b3e-178">Ruft den Typ des Standardspeicherkontos ab oder legt diesen Typ fest.</span><span class="sxs-lookup"><span data-stu-id="46b3e-178">Gets or sets the type of the default storage account.</span></span>

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

### <span data-ttu-id="46b3e-179">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="46b3e-179">-WorkerNodeSize</span></span>
<span data-ttu-id="46b3e-180">Gibt die Größe des virtuellen Computers für den Workerknoten an.</span><span class="sxs-lookup"><span data-stu-id="46b3e-180">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="46b3e-181">Verwenden Get-AzVMSize für akzeptable Größen für virtuelle Computer, und sehen Sie sich die Preisseite von HDInsight an.</span><span class="sxs-lookup"><span data-stu-id="46b3e-181">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="46b3e-182">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="46b3e-182">-ZookeeperNodeSize</span></span>
<span data-ttu-id="46b3e-183">Gibt die Größe des virtuellen Computers für den Knoten "Zookeeper" an.</span><span class="sxs-lookup"><span data-stu-id="46b3e-183">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="46b3e-184">Verwenden Get-AzVMSize für akzeptable Größen für virtuelle Computer, und sehen Sie sich die Preisseite von HDInsight an.</span><span class="sxs-lookup"><span data-stu-id="46b3e-184">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="46b3e-185">Dieser Parameter ist nur für HBase- oder Storm-Cluster gültig.</span><span class="sxs-lookup"><span data-stu-id="46b3e-185">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="46b3e-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46b3e-186">CommonParameters</span></span>
<span data-ttu-id="46b3e-187">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46b3e-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46b3e-188">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46b3e-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46b3e-189">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="46b3e-189">INPUTS</span></span>

### <span data-ttu-id="46b3e-190">Keine</span><span class="sxs-lookup"><span data-stu-id="46b3e-190">None</span></span>

## <span data-ttu-id="46b3e-191">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="46b3e-191">OUTPUTS</span></span>

### <span data-ttu-id="46b3e-192">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="46b3e-192">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="46b3e-193">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="46b3e-193">NOTES</span></span>

## <span data-ttu-id="46b3e-194">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="46b3e-194">RELATED LINKS</span></span>

[<span data-ttu-id="46b3e-195">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="46b3e-195">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


