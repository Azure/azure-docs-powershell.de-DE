---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 66857c9d12bb23ffdccb893b8fae8bfc7c6e0f4f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009281"
---
# <span data-ttu-id="396c9-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="396c9-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="396c9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="396c9-102">SYNOPSIS</span></span>
<span data-ttu-id="396c9-103">Erstellt ein nicht persistentes Cluster Konfigurationsobjekt, das eine Azure HDInsight-Cluster Konfiguration beschreibt.</span><span class="sxs-lookup"><span data-stu-id="396c9-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="396c9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="396c9-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-MinSupportedTlsVersion <String>]
 [-AssignedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-PublicNetworkAccessType <String>]
 [-OutboundPublicNetworkAccessType <String>] [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="396c9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="396c9-105">DESCRIPTION</span></span>
<span data-ttu-id="396c9-106">Das Cmdlet **New-AzHDInsightClusterConfig** erstellt ein nicht beibehaltenes Objekt, das eine Azure HDInsight-Cluster Konfiguration beschreibt.</span><span class="sxs-lookup"><span data-stu-id="396c9-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="396c9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="396c9-107">EXAMPLES</span></span>

### <span data-ttu-id="396c9-108">Beispiel 1: Erstellen eines Cluster Konfigurationsobjekts</span><span class="sxs-lookup"><span data-stu-id="396c9-108">Example 1: Create a cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
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
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="396c9-109">Mit diesem Befehl wird ein Cluster Konfigurationsobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="396c9-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="396c9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="396c9-110">PARAMETERS</span></span>

### <span data-ttu-id="396c9-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="396c9-111">-AadTenantId</span></span>
<span data-ttu-id="396c9-112">Gibt die Azure AD-Mandanten-ID an, die beim Zugriff auf den Azure Data Lake Store verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="396c9-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="396c9-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="396c9-113">-ApplicationId</span></span>
<span data-ttu-id="396c9-114">Ruft die Dienstprinzipal-Anwendungs-ID für den Zugriff auf Azure Data Lake ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="396c9-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="396c9-115">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="396c9-115">-AssignedIdentity</span></span>
<span data-ttu-id="396c9-116">Ruft die zugewiesene Identität ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="396c9-116">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="396c9-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="396c9-117">-CertificateFileContents</span></span>
<span data-ttu-id="396c9-118">Gibt den Dateiinhalt des Zertifikats an, das beim Zugriff auf den Azure Data Lake Store verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="396c9-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="396c9-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="396c9-119">-CertificateFilePath</span></span>
<span data-ttu-id="396c9-120">Gibt den Dateipfad zu dem Zertifikat an, das zur Authentifizierung als Dienstprinzipal verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="396c9-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="396c9-121">Der Cluster verwendet diesen beim Zugriff auf den Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="396c9-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="396c9-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="396c9-122">-CertificatePassword</span></span>
<span data-ttu-id="396c9-123">Gibt das Kennwort für das Zertifikat an, das für die Authentifizierung als Dienstprinzipal verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="396c9-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="396c9-124">Der Cluster verwendet diesen beim Zugriff auf den Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="396c9-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="396c9-125">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="396c9-125">-ClusterTier</span></span>
<span data-ttu-id="396c9-126">Gibt die HDInsight-Clusterebene an.</span><span class="sxs-lookup"><span data-stu-id="396c9-126">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="396c9-127">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="396c9-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="396c9-128">Standard</span><span class="sxs-lookup"><span data-stu-id="396c9-128">Standard</span></span>
- <span data-ttu-id="396c9-129">Premium der Standardwert ist Standard.</span><span class="sxs-lookup"><span data-stu-id="396c9-129">Premium The default value is Standard.</span></span>
<span data-ttu-id="396c9-130">Die Premium-Stufe kann nur mit Linux-Clustern verwendet werden und ermöglicht die Verwendung einiger neuer Funktionen.</span><span class="sxs-lookup"><span data-stu-id="396c9-130">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="396c9-131">-Clustertyp</span><span class="sxs-lookup"><span data-stu-id="396c9-131">-ClusterType</span></span>
<span data-ttu-id="396c9-132">Gibt den Typ des zu erstellende Clusters an.</span><span class="sxs-lookup"><span data-stu-id="396c9-132">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="396c9-133">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="396c9-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="396c9-134">Hadoop</span><span class="sxs-lookup"><span data-stu-id="396c9-134">Hadoop</span></span>
- <span data-ttu-id="396c9-135">HBase</span><span class="sxs-lookup"><span data-stu-id="396c9-135">HBase</span></span>
- <span data-ttu-id="396c9-136">Sturm</span><span class="sxs-lookup"><span data-stu-id="396c9-136">Storm</span></span>
- <span data-ttu-id="396c9-137">Funken</span><span class="sxs-lookup"><span data-stu-id="396c9-137">Spark</span></span>
- <span data-ttu-id="396c9-138">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="396c9-138">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="396c9-139">Kafka</span><span class="sxs-lookup"><span data-stu-id="396c9-139">Kafka</span></span>
- <span data-ttu-id="396c9-140">RServer</span><span class="sxs-lookup"><span data-stu-id="396c9-140">RServer</span></span>

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

### <span data-ttu-id="396c9-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="396c9-141">-DefaultProfile</span></span>
<span data-ttu-id="396c9-142">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="396c9-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="396c9-143">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="396c9-143">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="396c9-144">Gibt den Kontoschlüssel für das standardmäßige Azure Storage-Konto an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="396c9-144">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="396c9-145">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="396c9-145">-DefaultStorageAccountName</span></span>
<span data-ttu-id="396c9-146">Gibt den Namen des Standardspeicher Kontos an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="396c9-146">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="396c9-147">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="396c9-147">-DefaultStorageAccountType</span></span>
<span data-ttu-id="396c9-148">Gibt den Typ des Standardspeicher Kontos an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="396c9-148">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="396c9-149">Mögliche Werte sind AzureStorage und AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="396c9-149">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: AzureStorage
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="396c9-150">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="396c9-150">-EdgeNodeSize</span></span>
<span data-ttu-id="396c9-151">Gibt die Größe des virtuellen Computers für den Edge-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="396c9-151">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="396c9-152">Verwenden Sie Get-AzVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="396c9-152">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="396c9-153">Dieser Parameter ist nur für RServer-Cluster gültig.</span><span class="sxs-lookup"><span data-stu-id="396c9-153">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="396c9-154">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="396c9-154">-EncryptionAlgorithm</span></span>
<span data-ttu-id="396c9-155">Ruft den Verschlüsselungsalgorithmus ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="396c9-155">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="396c9-156">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="396c9-156">-EncryptionAtHost</span></span>
<span data-ttu-id="396c9-157">Ruft das Flag ab, das angibt, ob die Verschlüsselung beim Host aktiviert werden soll, oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="396c9-157">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="396c9-158">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="396c9-158">-EncryptionInTransit</span></span>
<span data-ttu-id="396c9-159">Ruft das Flag ab, das angibt, ob die Verschlüsselung bei der Übertragung aktiviert werden soll, oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="396c9-159">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="396c9-160">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="396c9-160">-EncryptionKeyName</span></span>
<span data-ttu-id="396c9-161">Ruft den Namen des Verschlüsselungsschlüssels ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="396c9-161">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="396c9-162">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="396c9-162">-EncryptionKeyVersion</span></span>
<span data-ttu-id="396c9-163">Ruft die Version des Verschlüsselungsschlüssels ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="396c9-163">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="396c9-164">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="396c9-164">-EncryptionVaultUri</span></span>
<span data-ttu-id="396c9-165">Ruft den Verschlüsselungs Tresor-URI ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="396c9-165">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="396c9-166">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="396c9-166">-HeadNodeSize</span></span>
<span data-ttu-id="396c9-167">Gibt die Größe des virtuellen Computers für den Head-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="396c9-167">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="396c9-168">Verwenden Sie Get-AzVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="396c9-168">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="396c9-169">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="396c9-169">-HiveMetastore</span></span>
<span data-ttu-id="396c9-170">Gibt den metastore an, in dem die Struktur Metadaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="396c9-170">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="396c9-171">Sie können das Add-AzHDInsightMetastore-Cmdlet auch verwenden.</span><span class="sxs-lookup"><span data-stu-id="396c9-171">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="396c9-172">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="396c9-172">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="396c9-173">Ruft die minimal unterstützte TLS-Version ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="396c9-173">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="396c9-174">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="396c9-174">-ObjectId</span></span>
<span data-ttu-id="396c9-175">Gibt die Azure AD-Objekt-ID (eine GUID) des Azure AD-Dienst Prinzipals an, der den Cluster darstellt.</span><span class="sxs-lookup"><span data-stu-id="396c9-175">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="396c9-176">Der Cluster verwendet diesen beim Zugriff auf den Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="396c9-176">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="396c9-177">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="396c9-177">-OozieMetastore</span></span>
<span data-ttu-id="396c9-178">Gibt den metastore an, in dem Oozie-Metadaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="396c9-178">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="396c9-179">Alternativ können Sie das Cmdlet **Add-AzHDInsightMetastore** verwenden.</span><span class="sxs-lookup"><span data-stu-id="396c9-179">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="396c9-180">-OutboundPublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="396c9-180">-OutboundPublicNetworkAccessType</span></span>
<span data-ttu-id="396c9-181">Ruft den ausgehenden Zugriffstyp für das öffentliche Netzwerk ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="396c9-181">Gets or sets the outbound access type to the public network.</span></span>

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

### <span data-ttu-id="396c9-182">-PublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="396c9-182">-PublicNetworkAccessType</span></span>
<span data-ttu-id="396c9-183">Ruft den Zugriffstyp für öffentliche Netzwerke ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="396c9-183">Gets or sets the public network access type.</span></span>

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

### <span data-ttu-id="396c9-184">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="396c9-184">-WorkerNodeSize</span></span>
<span data-ttu-id="396c9-185">Gibt die Größe des virtuellen Computers für den Worker-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="396c9-185">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="396c9-186">Verwenden Sie Get-AzVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="396c9-186">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="396c9-187">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="396c9-187">-ZookeeperNodeSize</span></span>
<span data-ttu-id="396c9-188">Gibt die Größe des virtuellen Computers für den zoowärter-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="396c9-188">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="396c9-189">Verwenden Sie Get-AzVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="396c9-189">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="396c9-190">Dieser Parameter ist nur für HBAs oder Storm-Cluster gültig.</span><span class="sxs-lookup"><span data-stu-id="396c9-190">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="396c9-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="396c9-191">CommonParameters</span></span>
<span data-ttu-id="396c9-192">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="396c9-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="396c9-193">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="396c9-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="396c9-194">Eingaben</span><span class="sxs-lookup"><span data-stu-id="396c9-194">INPUTS</span></span>

### <span data-ttu-id="396c9-195">Keine</span><span class="sxs-lookup"><span data-stu-id="396c9-195">None</span></span>

## <span data-ttu-id="396c9-196">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="396c9-196">OUTPUTS</span></span>

### <span data-ttu-id="396c9-197">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="396c9-197">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="396c9-198">Notizen</span><span class="sxs-lookup"><span data-stu-id="396c9-198">NOTES</span></span>

## <span data-ttu-id="396c9-199">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="396c9-199">RELATED LINKS</span></span>

[<span data-ttu-id="396c9-200">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="396c9-200">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


