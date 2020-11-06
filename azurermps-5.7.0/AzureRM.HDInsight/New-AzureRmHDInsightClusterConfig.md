---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightClusterConfig.md
ms.openlocfilehash: 1f6a6d05bff2c012ca3b32abd16dca01cbe1707b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481222"
---
# <span data-ttu-id="22909-101">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="22909-101">New-AzureRmHDInsightClusterConfig</span></span>

## <span data-ttu-id="22909-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="22909-102">SYNOPSIS</span></span>
<span data-ttu-id="22909-103">Erstellt ein nicht persistentes Cluster Konfigurationsobjekt, das eine Azure HDInsight-Cluster Konfiguration beschreibt.</span><span class="sxs-lookup"><span data-stu-id="22909-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22909-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="22909-104">SYNTAX</span></span>

```
New-AzureRmHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22909-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22909-105">DESCRIPTION</span></span>
<span data-ttu-id="22909-106">Das Cmdlet **New-AzureRmHDInsightClusterConfig** erstellt ein nicht beibehaltenes Objekt, das eine Azure HDInsight-Cluster Konfiguration beschreibt.</span><span class="sxs-lookup"><span data-stu-id="22909-106">The **New-AzureRmHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="22909-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="22909-107">EXAMPLES</span></span>

### <span data-ttu-id="22909-108">Beispiel 1: Erstellen eines Cluster Konfigurationsobjekts</span><span class="sxs-lookup"><span data-stu-id="22909-108">Example 1: Create a cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
            | New-AzureRmHDInsightCluster `
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

<span data-ttu-id="22909-109">Mit diesem Befehl wird ein Cluster Konfigurationsobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="22909-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="22909-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="22909-110">PARAMETERS</span></span>

### <span data-ttu-id="22909-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="22909-111">-AadTenantId</span></span>
<span data-ttu-id="22909-112">Gibt die Azure AD-Mandanten-ID an, die beim Zugriff auf den Azure Data Lake Store verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="22909-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="22909-113">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="22909-113">-CertificateFileContents</span></span>
<span data-ttu-id="22909-114">Gibt den Dateiinhalt des Zertifikats an, das beim Zugriff auf den Azure Data Lake Store verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="22909-114">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Byte[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22909-115">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="22909-115">-CertificateFilePath</span></span>
<span data-ttu-id="22909-116">Gibt den Dateipfad zu dem Zertifikat an, das zur Authentifizierung als Dienstprinzipal verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="22909-116">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="22909-117">Der Cluster verwendet diesen beim Zugriff auf den Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="22909-117">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="22909-118">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="22909-118">-CertificatePassword</span></span>
<span data-ttu-id="22909-119">Gibt das Kennwort für das Zertifikat an, das für die Authentifizierung als Dienstprinzipal verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="22909-119">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="22909-120">Der Cluster verwendet diesen beim Zugriff auf den Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="22909-120">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="22909-121">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="22909-121">-ClusterTier</span></span>
<span data-ttu-id="22909-122">Gibt die HDInsight-Clusterebene an.</span><span class="sxs-lookup"><span data-stu-id="22909-122">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="22909-123">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="22909-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="22909-124">Standard</span><span class="sxs-lookup"><span data-stu-id="22909-124">Standard</span></span>
- <span data-ttu-id="22909-125">Premium</span><span class="sxs-lookup"><span data-stu-id="22909-125">Premium</span></span>

<span data-ttu-id="22909-126">Der Standardwert ist Standard.</span><span class="sxs-lookup"><span data-stu-id="22909-126">The default value is Standard.</span></span>
<span data-ttu-id="22909-127">Die Premium-Stufe kann nur mit Linux-Clustern verwendet werden und ermöglicht die Verwendung einiger neuer Funktionen.</span><span class="sxs-lookup"><span data-stu-id="22909-127">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="22909-128">-Clustertyp</span><span class="sxs-lookup"><span data-stu-id="22909-128">-ClusterType</span></span>
<span data-ttu-id="22909-129">Gibt den Typ des zu erstellende Clusters an.</span><span class="sxs-lookup"><span data-stu-id="22909-129">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="22909-130">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="22909-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="22909-131">Hadoop</span><span class="sxs-lookup"><span data-stu-id="22909-131">Hadoop</span></span>
- <span data-ttu-id="22909-132">HBase</span><span class="sxs-lookup"><span data-stu-id="22909-132">HBase</span></span>
- <span data-ttu-id="22909-133">Sturm</span><span class="sxs-lookup"><span data-stu-id="22909-133">Storm</span></span>
- <span data-ttu-id="22909-134">Funken</span><span class="sxs-lookup"><span data-stu-id="22909-134">Spark</span></span>

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

### <span data-ttu-id="22909-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22909-135">-DefaultProfile</span></span>
<span data-ttu-id="22909-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="22909-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22909-137">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="22909-137">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="22909-138">Gibt den Kontoschlüssel für das standardmäßige Azure Storage-Konto an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="22909-138">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="22909-139">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="22909-139">-DefaultStorageAccountName</span></span>
<span data-ttu-id="22909-140">Gibt den Namen des Standardspeicher Kontos an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="22909-140">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="22909-141">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="22909-141">-DefaultStorageAccountType</span></span>
<span data-ttu-id="22909-142">Gibt den Typ des Standardspeicher Kontos an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="22909-142">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="22909-143">Mögliche Werte sind AzureStorage und AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="22909-143">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

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

### <span data-ttu-id="22909-144">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="22909-144">-EdgeNodeSize</span></span>
<span data-ttu-id="22909-145">Gibt die Größe des virtuellen Computers für den Edge-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="22909-145">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="22909-146">Verwenden Sie Get-AzureRmVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="22909-146">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="22909-147">Dieser Parameter ist nur für RServer-Cluster gültig.</span><span class="sxs-lookup"><span data-stu-id="22909-147">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="22909-148">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="22909-148">-HeadNodeSize</span></span>
<span data-ttu-id="22909-149">Gibt die Größe des virtuellen Computers für den Head-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="22909-149">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="22909-150">Verwenden Sie Get-AzureRMVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="22909-150">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="22909-151">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="22909-151">-HiveMetastore</span></span>
<span data-ttu-id="22909-152">Gibt den metastore an, in dem die Struktur Metadaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="22909-152">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="22909-153">Sie können das Add-AzureRmHDInsightMetastore-Cmdlet auch verwenden.</span><span class="sxs-lookup"><span data-stu-id="22909-153">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="22909-154">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="22909-154">-ObjectId</span></span>
<span data-ttu-id="22909-155">Gibt die Azure AD-Objekt-ID (eine GUID) des Azure AD-Dienst Prinzipals an, der den Cluster darstellt.</span><span class="sxs-lookup"><span data-stu-id="22909-155">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="22909-156">Der Cluster verwendet diesen beim Zugriff auf den Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="22909-156">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="22909-157">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="22909-157">-OozieMetastore</span></span>
<span data-ttu-id="22909-158">Gibt den metastore an, in dem Oozie-Metadaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="22909-158">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="22909-159">Alternativ können Sie das Cmdlet **Add-AzureRmHDInsightMetastore** verwenden.</span><span class="sxs-lookup"><span data-stu-id="22909-159">You can alternatively use the **Add-AzureRmHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="22909-160">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="22909-160">-WorkerNodeSize</span></span>
<span data-ttu-id="22909-161">Gibt die Größe des virtuellen Computers für den Worker-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="22909-161">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="22909-162">Verwenden Sie Get-AzureRMVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="22909-162">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="22909-163">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="22909-163">-ZookeeperNodeSize</span></span>
<span data-ttu-id="22909-164">Gibt die Größe des virtuellen Computers für den zoowärter-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="22909-164">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="22909-165">Verwenden Sie Get-AzureRMVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="22909-165">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="22909-166">Dieser Parameter ist nur für HBAs oder Storm-Cluster gültig.</span><span class="sxs-lookup"><span data-stu-id="22909-166">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="22909-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22909-167">CommonParameters</span></span>
<span data-ttu-id="22909-168">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22909-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22909-169">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22909-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22909-170">Eingaben</span><span class="sxs-lookup"><span data-stu-id="22909-170">INPUTS</span></span>

### <span data-ttu-id="22909-171">Keine</span><span class="sxs-lookup"><span data-stu-id="22909-171">None</span></span>
<span data-ttu-id="22909-172">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="22909-172">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="22909-173">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="22909-173">OUTPUTS</span></span>

### <span data-ttu-id="22909-174">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="22909-174">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="22909-175">Notizen</span><span class="sxs-lookup"><span data-stu-id="22909-175">NOTES</span></span>

## <span data-ttu-id="22909-176">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="22909-176">RELATED LINKS</span></span>

[<span data-ttu-id="22909-177">Add-AzureRmHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="22909-177">Add-AzureRmHDInsightStorage</span></span>](./Add-AzureRmHDInsightStorage.md)


