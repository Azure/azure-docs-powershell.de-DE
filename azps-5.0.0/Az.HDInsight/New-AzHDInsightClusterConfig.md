---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 1124136a580d0079690c60e31fe8de8649e3cafb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178047"
---
# <span data-ttu-id="e4147-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="e4147-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="e4147-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e4147-102">SYNOPSIS</span></span>
<span data-ttu-id="e4147-103">Erstellt ein nicht persistentes Cluster Konfigurationsobjekt, das eine Azure HDInsight-Cluster Konfiguration beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e4147-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="e4147-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4147-104">SYNTAX</span></span>

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

## <span data-ttu-id="e4147-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e4147-105">DESCRIPTION</span></span>
<span data-ttu-id="e4147-106">Das Cmdlet **New-AzHDInsightClusterConfig** erstellt ein nicht beibehaltenes Objekt, das eine Azure HDInsight-Cluster Konfiguration beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e4147-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="e4147-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e4147-107">EXAMPLES</span></span>

### <span data-ttu-id="e4147-108">Beispiel 1: Erstellen eines Cluster Konfigurationsobjekts</span><span class="sxs-lookup"><span data-stu-id="e4147-108">Example 1: Create a cluster configuration object</span></span>
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

<span data-ttu-id="e4147-109">Mit diesem Befehl wird ein Cluster Konfigurationsobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="e4147-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="e4147-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4147-110">PARAMETERS</span></span>

### <span data-ttu-id="e4147-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="e4147-111">-AadTenantId</span></span>
<span data-ttu-id="e4147-112">Gibt die Azure AD-Mandanten-ID an, die beim Zugriff auf den Azure Data Lake Store verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e4147-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="e4147-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e4147-113">-ApplicationId</span></span>
<span data-ttu-id="e4147-114">Ruft die Dienstprinzipal-Anwendungs-ID für den Zugriff auf Azure Data Lake ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="e4147-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="e4147-115">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e4147-115">-AssignedIdentity</span></span>
<span data-ttu-id="e4147-116">Ruft die zugewiesene Identität ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="e4147-116">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="e4147-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="e4147-117">-CertificateFileContents</span></span>
<span data-ttu-id="e4147-118">Gibt den Dateiinhalt des Zertifikats an, das beim Zugriff auf den Azure Data Lake Store verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e4147-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="e4147-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="e4147-119">-CertificateFilePath</span></span>
<span data-ttu-id="e4147-120">Gibt den Dateipfad zu dem Zertifikat an, das zur Authentifizierung als Dienstprinzipal verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e4147-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="e4147-121">Der Cluster verwendet diesen beim Zugriff auf den Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e4147-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="e4147-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="e4147-122">-CertificatePassword</span></span>
<span data-ttu-id="e4147-123">Gibt das Kennwort für das Zertifikat an, das für die Authentifizierung als Dienstprinzipal verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e4147-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="e4147-124">Der Cluster verwendet diesen beim Zugriff auf den Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e4147-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="e4147-125">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="e4147-125">-ClusterTier</span></span>
<span data-ttu-id="e4147-126">Gibt die HDInsight-Clusterebene an.</span><span class="sxs-lookup"><span data-stu-id="e4147-126">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="e4147-127">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e4147-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e4147-128">Standard</span><span class="sxs-lookup"><span data-stu-id="e4147-128">Standard</span></span>
- <span data-ttu-id="e4147-129">Premium der Standardwert ist Standard.</span><span class="sxs-lookup"><span data-stu-id="e4147-129">Premium The default value is Standard.</span></span>
<span data-ttu-id="e4147-130">Die Premium-Stufe kann nur mit Linux-Clustern verwendet werden und ermöglicht die Verwendung einiger neuer Funktionen.</span><span class="sxs-lookup"><span data-stu-id="e4147-130">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="e4147-131">-Clustertyp</span><span class="sxs-lookup"><span data-stu-id="e4147-131">-ClusterType</span></span>
<span data-ttu-id="e4147-132">Gibt den Typ des zu erstellende Clusters an.</span><span class="sxs-lookup"><span data-stu-id="e4147-132">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="e4147-133">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e4147-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e4147-134">Hadoop</span><span class="sxs-lookup"><span data-stu-id="e4147-134">Hadoop</span></span>
- <span data-ttu-id="e4147-135">HBase</span><span class="sxs-lookup"><span data-stu-id="e4147-135">HBase</span></span>
- <span data-ttu-id="e4147-136">Sturm</span><span class="sxs-lookup"><span data-stu-id="e4147-136">Storm</span></span>
- <span data-ttu-id="e4147-137">Funken</span><span class="sxs-lookup"><span data-stu-id="e4147-137">Spark</span></span>
- <span data-ttu-id="e4147-138">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="e4147-138">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="e4147-139">Kafka</span><span class="sxs-lookup"><span data-stu-id="e4147-139">Kafka</span></span>
- <span data-ttu-id="e4147-140">RServer</span><span class="sxs-lookup"><span data-stu-id="e4147-140">RServer</span></span>

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

### <span data-ttu-id="e4147-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4147-141">-DefaultProfile</span></span>
<span data-ttu-id="e4147-142">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e4147-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4147-143">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="e4147-143">-EdgeNodeSize</span></span>
<span data-ttu-id="e4147-144">Gibt die Größe des virtuellen Computers für den Edge-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="e4147-144">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="e4147-145">Verwenden Sie Get-AzVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="e4147-145">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="e4147-146">Dieser Parameter ist nur für RServer-Cluster gültig.</span><span class="sxs-lookup"><span data-stu-id="e4147-146">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="e4147-147">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="e4147-147">-EncryptionAlgorithm</span></span>
<span data-ttu-id="e4147-148">Ruft den Verschlüsselungsalgorithmus ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="e4147-148">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="e4147-149">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="e4147-149">-EncryptionAtHost</span></span>
<span data-ttu-id="e4147-150">Ruft das Flag ab, das angibt, ob die Verschlüsselung beim Host aktiviert werden soll, oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="e4147-150">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="e4147-151">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="e4147-151">-EncryptionInTransit</span></span>
<span data-ttu-id="e4147-152">Ruft das Flag ab, das angibt, ob die Verschlüsselung bei der Übertragung aktiviert werden soll, oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="e4147-152">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="e4147-153">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="e4147-153">-EncryptionKeyName</span></span>
<span data-ttu-id="e4147-154">Ruft den Namen des Verschlüsselungsschlüssels ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="e4147-154">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="e4147-155">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="e4147-155">-EncryptionKeyVersion</span></span>
<span data-ttu-id="e4147-156">Ruft die Version des Verschlüsselungsschlüssels ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="e4147-156">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="e4147-157">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="e4147-157">-EncryptionVaultUri</span></span>
<span data-ttu-id="e4147-158">Ruft den Verschlüsselungs Tresor-URI ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="e4147-158">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="e4147-159">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="e4147-159">-HeadNodeSize</span></span>
<span data-ttu-id="e4147-160">Gibt die Größe des virtuellen Computers für den Head-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="e4147-160">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="e4147-161">Verwenden Sie Get-AzVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="e4147-161">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="e4147-162">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="e4147-162">-HiveMetastore</span></span>
<span data-ttu-id="e4147-163">Gibt den metastore an, in dem die Struktur Metadaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="e4147-163">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="e4147-164">Sie können das Add-AzHDInsightMetastore-Cmdlet auch verwenden.</span><span class="sxs-lookup"><span data-stu-id="e4147-164">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="e4147-165">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="e4147-165">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="e4147-166">Ruft die minimal unterstützte TLS-Version ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="e4147-166">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="e4147-167">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="e4147-167">-ObjectId</span></span>
<span data-ttu-id="e4147-168">Gibt die Azure AD-Objekt-ID (eine GUID) des Azure AD-Dienst Prinzipals an, der den Cluster darstellt.</span><span class="sxs-lookup"><span data-stu-id="e4147-168">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="e4147-169">Der Cluster verwendet diesen beim Zugriff auf den Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e4147-169">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="e4147-170">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="e4147-170">-OozieMetastore</span></span>
<span data-ttu-id="e4147-171">Gibt den metastore an, in dem Oozie-Metadaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="e4147-171">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="e4147-172">Alternativ können Sie das Cmdlet **Add-AzHDInsightMetastore** verwenden.</span><span class="sxs-lookup"><span data-stu-id="e4147-172">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="e4147-173">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e4147-173">-StorageAccountKey</span></span>
<span data-ttu-id="e4147-174">Ruft die Zugriffstaste für das Speicherkonto ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="e4147-174">Gets or sets the storage account access key.</span></span>

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

### <span data-ttu-id="e4147-175">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="e4147-175">-StorageAccountResourceId</span></span>
<span data-ttu-id="e4147-176">Ruft die Ressourcen-ID des speicherkontos ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="e4147-176">Gets or sets the storage account resource id.</span></span>

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

### <span data-ttu-id="e4147-177">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="e4147-177">-StorageAccountType</span></span>
<span data-ttu-id="e4147-178">Ruft den Typ des Standardspeicher Kontos ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="e4147-178">Gets or sets the type of the default storage account.</span></span>

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

### <span data-ttu-id="e4147-179">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="e4147-179">-WorkerNodeSize</span></span>
<span data-ttu-id="e4147-180">Gibt die Größe des virtuellen Computers für den Worker-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="e4147-180">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="e4147-181">Verwenden Sie Get-AzVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="e4147-181">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="e4147-182">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="e4147-182">-ZookeeperNodeSize</span></span>
<span data-ttu-id="e4147-183">Gibt die Größe des virtuellen Computers für den zoowärter-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="e4147-183">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="e4147-184">Verwenden Sie Get-AzVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="e4147-184">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="e4147-185">Dieser Parameter ist nur für HBAs oder Storm-Cluster gültig.</span><span class="sxs-lookup"><span data-stu-id="e4147-185">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="e4147-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4147-186">CommonParameters</span></span>
<span data-ttu-id="e4147-187">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4147-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4147-188">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4147-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4147-189">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e4147-189">INPUTS</span></span>

### <span data-ttu-id="e4147-190">Keine</span><span class="sxs-lookup"><span data-stu-id="e4147-190">None</span></span>

## <span data-ttu-id="e4147-191">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e4147-191">OUTPUTS</span></span>

### <span data-ttu-id="e4147-192">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="e4147-192">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="e4147-193">Notizen</span><span class="sxs-lookup"><span data-stu-id="e4147-193">NOTES</span></span>

## <span data-ttu-id="e4147-194">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e4147-194">RELATED LINKS</span></span>

[<span data-ttu-id="e4147-195">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="e4147-195">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


