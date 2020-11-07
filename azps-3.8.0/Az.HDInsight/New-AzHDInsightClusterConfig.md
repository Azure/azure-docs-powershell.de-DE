---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 38dc23c2bebe3c608833e55bcb4ffb2d687f9041
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847544"
---
# <span data-ttu-id="795f0-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="795f0-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="795f0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="795f0-102">SYNOPSIS</span></span>
<span data-ttu-id="795f0-103">Erstellt ein nicht persistentes Cluster Konfigurationsobjekt, das eine Azure HDInsight-Cluster Konfiguration beschreibt.</span><span class="sxs-lookup"><span data-stu-id="795f0-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="795f0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="795f0-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [[-DefaultStorageAccountType] <StorageType>] [[-OozieMetastore] <AzureHDInsightMetastore>]
 [[-HiveMetastore] <AzureHDInsightMetastore>] [[-HeadNodeSize] <String>] [[-WorkerNodeSize] <String>]
 [[-EdgeNodeSize] <String>] [[-ZookeeperNodeSize] <String>] [[-ClusterType] <String>] [[-ClusterTier] <Tier>]
 [[-ObjectId] <Guid>] [[-ApplicationId] <Guid>] [[-CertificateFileContents] <Byte[]>]
 [[-CertificateFilePath] <String>] [[-CertificatePassword] <String>] [[-AadTenantId] <Guid>]
 [[-MinSupportedTlsVersion] <String>] [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="795f0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="795f0-105">DESCRIPTION</span></span>
<span data-ttu-id="795f0-106">Das Cmdlet **New-AzHDInsightClusterConfig** erstellt ein nicht beibehaltenes Objekt, das eine Azure HDInsight-Cluster Konfiguration beschreibt.</span><span class="sxs-lookup"><span data-stu-id="795f0-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="795f0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="795f0-107">EXAMPLES</span></span>

### <span data-ttu-id="795f0-108">Beispiel 1: Erstellen eines Cluster Konfigurationsobjekts</span><span class="sxs-lookup"><span data-stu-id="795f0-108">Example 1: Create a cluster configuration object</span></span>
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

<span data-ttu-id="795f0-109">Mit diesem Befehl wird ein Cluster Konfigurationsobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="795f0-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="795f0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="795f0-110">PARAMETERS</span></span>

### <span data-ttu-id="795f0-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="795f0-111">-AadTenantId</span></span>
<span data-ttu-id="795f0-112">Gibt die Azure AD-Mandanten-ID an, die beim Zugriff auf den Azure Data Lake Store verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="795f0-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="795f0-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="795f0-113">-ApplicationId</span></span>
<span data-ttu-id="795f0-114">Ruft die Dienstprinzipal-Anwendungs-ID für den Zugriff auf Azure Data Lake ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="795f0-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="795f0-115">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="795f0-115">-CertificateFileContents</span></span>
<span data-ttu-id="795f0-116">Gibt den Dateiinhalt des Zertifikats an, das beim Zugriff auf den Azure Data Lake Store verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="795f0-116">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="795f0-117">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="795f0-117">-CertificateFilePath</span></span>
<span data-ttu-id="795f0-118">Gibt den Dateipfad zu dem Zertifikat an, das zur Authentifizierung als Dienstprinzipal verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="795f0-118">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="795f0-119">Der Cluster verwendet diesen beim Zugriff auf den Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="795f0-119">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="795f0-120">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="795f0-120">-CertificatePassword</span></span>
<span data-ttu-id="795f0-121">Gibt das Kennwort für das Zertifikat an, das für die Authentifizierung als Dienstprinzipal verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="795f0-121">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="795f0-122">Der Cluster verwendet diesen beim Zugriff auf den Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="795f0-122">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="795f0-123">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="795f0-123">-ClusterTier</span></span>
<span data-ttu-id="795f0-124">Gibt die HDInsight-Clusterebene an.</span><span class="sxs-lookup"><span data-stu-id="795f0-124">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="795f0-125">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="795f0-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="795f0-126">Standard</span><span class="sxs-lookup"><span data-stu-id="795f0-126">Standard</span></span>
- <span data-ttu-id="795f0-127">Premium der Standardwert ist Standard.</span><span class="sxs-lookup"><span data-stu-id="795f0-127">Premium The default value is Standard.</span></span>
<span data-ttu-id="795f0-128">Die Premium-Stufe kann nur mit Linux-Clustern verwendet werden und ermöglicht die Verwendung einiger neuer Funktionen.</span><span class="sxs-lookup"><span data-stu-id="795f0-128">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="795f0-129">-Clustertyp</span><span class="sxs-lookup"><span data-stu-id="795f0-129">-ClusterType</span></span>
<span data-ttu-id="795f0-130">Gibt den Typ des zu erstellende Clusters an.</span><span class="sxs-lookup"><span data-stu-id="795f0-130">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="795f0-131">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="795f0-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="795f0-132">Hadoop</span><span class="sxs-lookup"><span data-stu-id="795f0-132">Hadoop</span></span>
- <span data-ttu-id="795f0-133">HBase</span><span class="sxs-lookup"><span data-stu-id="795f0-133">HBase</span></span>
- <span data-ttu-id="795f0-134">Sturm</span><span class="sxs-lookup"><span data-stu-id="795f0-134">Storm</span></span>
- <span data-ttu-id="795f0-135">Funken</span><span class="sxs-lookup"><span data-stu-id="795f0-135">Spark</span></span>
- <span data-ttu-id="795f0-136">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="795f0-136">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="795f0-137">Kafka</span><span class="sxs-lookup"><span data-stu-id="795f0-137">Kafka</span></span>
- <span data-ttu-id="795f0-138">RServer</span><span class="sxs-lookup"><span data-stu-id="795f0-138">RServer</span></span>

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

### <span data-ttu-id="795f0-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="795f0-139">-DefaultProfile</span></span>
<span data-ttu-id="795f0-140">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="795f0-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="795f0-141">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="795f0-141">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="795f0-142">Gibt den Kontoschlüssel für das standardmäßige Azure Storage-Konto an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="795f0-142">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="795f0-143">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="795f0-143">-DefaultStorageAccountName</span></span>
<span data-ttu-id="795f0-144">Gibt den Namen des Standardspeicher Kontos an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="795f0-144">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="795f0-145">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="795f0-145">-DefaultStorageAccountType</span></span>
<span data-ttu-id="795f0-146">Gibt den Typ des Standardspeicher Kontos an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="795f0-146">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="795f0-147">Mögliche Werte sind AzureStorage und AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="795f0-147">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

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

### <span data-ttu-id="795f0-148">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="795f0-148">-EdgeNodeSize</span></span>
<span data-ttu-id="795f0-149">Gibt die Größe des virtuellen Computers für den Edge-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="795f0-149">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="795f0-150">Verwenden Sie Get-AzVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="795f0-150">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="795f0-151">Dieser Parameter ist nur für RServer-Cluster gültig.</span><span class="sxs-lookup"><span data-stu-id="795f0-151">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="795f0-152">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="795f0-152">-HeadNodeSize</span></span>
<span data-ttu-id="795f0-153">Gibt die Größe des virtuellen Computers für den Head-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="795f0-153">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="795f0-154">Verwenden Sie Get-AzVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="795f0-154">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="795f0-155">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="795f0-155">-HiveMetastore</span></span>
<span data-ttu-id="795f0-156">Gibt den metastore an, in dem die Struktur Metadaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="795f0-156">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="795f0-157">Sie können das Add-AzHDInsightMetastore-Cmdlet auch verwenden.</span><span class="sxs-lookup"><span data-stu-id="795f0-157">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="795f0-158">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="795f0-158">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="795f0-159">Ruft die minimal unterstützte TLS-Version ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="795f0-159">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="795f0-160">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="795f0-160">-ObjectId</span></span>
<span data-ttu-id="795f0-161">Gibt die Azure AD-Objekt-ID (eine GUID) des Azure AD-Dienst Prinzipals an, der den Cluster darstellt.</span><span class="sxs-lookup"><span data-stu-id="795f0-161">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="795f0-162">Der Cluster verwendet diesen beim Zugriff auf den Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="795f0-162">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="795f0-163">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="795f0-163">-OozieMetastore</span></span>
<span data-ttu-id="795f0-164">Gibt den metastore an, in dem Oozie-Metadaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="795f0-164">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="795f0-165">Alternativ können Sie das Cmdlet **Add-AzHDInsightMetastore** verwenden.</span><span class="sxs-lookup"><span data-stu-id="795f0-165">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="795f0-166">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="795f0-166">-WorkerNodeSize</span></span>
<span data-ttu-id="795f0-167">Gibt die Größe des virtuellen Computers für den Worker-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="795f0-167">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="795f0-168">Verwenden Sie Get-AzVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="795f0-168">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="795f0-169">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="795f0-169">-ZookeeperNodeSize</span></span>
<span data-ttu-id="795f0-170">Gibt die Größe des virtuellen Computers für den zoowärter-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="795f0-170">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="795f0-171">Verwenden Sie Get-AzVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="795f0-171">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="795f0-172">Dieser Parameter ist nur für HBAs oder Storm-Cluster gültig.</span><span class="sxs-lookup"><span data-stu-id="795f0-172">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="795f0-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="795f0-173">CommonParameters</span></span>
<span data-ttu-id="795f0-174">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="795f0-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="795f0-175">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="795f0-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="795f0-176">Eingaben</span><span class="sxs-lookup"><span data-stu-id="795f0-176">INPUTS</span></span>

### <span data-ttu-id="795f0-177">Keine</span><span class="sxs-lookup"><span data-stu-id="795f0-177">None</span></span>

## <span data-ttu-id="795f0-178">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="795f0-178">OUTPUTS</span></span>

### <span data-ttu-id="795f0-179">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="795f0-179">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="795f0-180">Notizen</span><span class="sxs-lookup"><span data-stu-id="795f0-180">NOTES</span></span>

## <span data-ttu-id="795f0-181">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="795f0-181">RELATED LINKS</span></span>

[<span data-ttu-id="795f0-182">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="795f0-182">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


