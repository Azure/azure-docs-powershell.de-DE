---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightClusterConfig.md
ms.openlocfilehash: e4588f3799052cf9f397f846b635be4f525df930
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496114"
---
# <span data-ttu-id="8c1bd-101">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="8c1bd-101">New-AzureRmHDInsightClusterConfig</span></span>

## <span data-ttu-id="8c1bd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8c1bd-102">SYNOPSIS</span></span>
<span data-ttu-id="8c1bd-103">Erstellt ein nicht persistentes Cluster Konfigurationsobjekt, das eine Azure HDInsight-Cluster Konfiguration beschreibt.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c1bd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c1bd-104">SYNTAX</span></span>

```
New-AzureRmHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8c1bd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8c1bd-105">DESCRIPTION</span></span>
<span data-ttu-id="8c1bd-106">Das Cmdlet **New-AzureRmHDInsightClusterConfig** erstellt ein nicht beibehaltenes Objekt, das eine Azure HDInsight-Cluster Konfiguration beschreibt.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-106">The **New-AzureRmHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="8c1bd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8c1bd-107">EXAMPLES</span></span>

### <span data-ttu-id="8c1bd-108">Beispiel 1: Erstellen eines Cluster Konfigurationsobjekts</span><span class="sxs-lookup"><span data-stu-id="8c1bd-108">Example 1: Create a cluster configuration object</span></span>
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

<span data-ttu-id="8c1bd-109">Mit diesem Befehl wird ein Cluster Konfigurationsobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="8c1bd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c1bd-110">PARAMETERS</span></span>

### <span data-ttu-id="8c1bd-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="8c1bd-111">-AadTenantId</span></span>
<span data-ttu-id="8c1bd-112">Gibt die Azure AD-Mandanten-ID an, die beim Zugriff auf den Azure Data Lake Store verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="8c1bd-113">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="8c1bd-113">-CertificateFileContents</span></span>
<span data-ttu-id="8c1bd-114">Gibt den Dateiinhalt des Zertifikats an, das beim Zugriff auf den Azure Data Lake Store verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-114">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="8c1bd-115">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="8c1bd-115">-CertificateFilePath</span></span>
<span data-ttu-id="8c1bd-116">Gibt den Dateipfad zu dem Zertifikat an, das zur Authentifizierung als Dienstprinzipal verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-116">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="8c1bd-117">Der Cluster verwendet diesen beim Zugriff auf den Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-117">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="8c1bd-118">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="8c1bd-118">-CertificatePassword</span></span>
<span data-ttu-id="8c1bd-119">Gibt das Kennwort für das Zertifikat an, das für die Authentifizierung als Dienstprinzipal verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-119">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="8c1bd-120">Der Cluster verwendet diesen beim Zugriff auf den Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-120">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="8c1bd-121">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="8c1bd-121">-ClusterTier</span></span>
<span data-ttu-id="8c1bd-122">Gibt die HDInsight-Clusterebene an.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-122">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="8c1bd-123">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8c1bd-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8c1bd-124">Standard</span><span class="sxs-lookup"><span data-stu-id="8c1bd-124">Standard</span></span>
- <span data-ttu-id="8c1bd-125">Premium der Standardwert ist Standard.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-125">Premium The default value is Standard.</span></span>
<span data-ttu-id="8c1bd-126">Die Premium-Stufe kann nur mit Linux-Clustern verwendet werden und ermöglicht die Verwendung einiger neuer Funktionen.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-126">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="8c1bd-127">-Clustertyp</span><span class="sxs-lookup"><span data-stu-id="8c1bd-127">-ClusterType</span></span>
<span data-ttu-id="8c1bd-128">Gibt den Typ des zu erstellende Clusters an.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-128">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="8c1bd-129">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8c1bd-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8c1bd-130">Hadoop</span><span class="sxs-lookup"><span data-stu-id="8c1bd-130">Hadoop</span></span>
- <span data-ttu-id="8c1bd-131">HBase</span><span class="sxs-lookup"><span data-stu-id="8c1bd-131">HBase</span></span>
- <span data-ttu-id="8c1bd-132">Sturm</span><span class="sxs-lookup"><span data-stu-id="8c1bd-132">Storm</span></span>
- <span data-ttu-id="8c1bd-133">Funken</span><span class="sxs-lookup"><span data-stu-id="8c1bd-133">Spark</span></span>

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

### <span data-ttu-id="8c1bd-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c1bd-134">-DefaultProfile</span></span>
<span data-ttu-id="8c1bd-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8c1bd-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c1bd-136">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="8c1bd-136">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="8c1bd-137">Gibt den Kontoschlüssel für das standardmäßige Azure Storage-Konto an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-137">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="8c1bd-138">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8c1bd-138">-DefaultStorageAccountName</span></span>
<span data-ttu-id="8c1bd-139">Gibt den Namen des Standardspeicher Kontos an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-139">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="8c1bd-140">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="8c1bd-140">-DefaultStorageAccountType</span></span>
<span data-ttu-id="8c1bd-141">Gibt den Typ des Standardspeicher Kontos an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-141">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="8c1bd-142">Mögliche Werte sind AzureStorage und AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-142">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

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

### <span data-ttu-id="8c1bd-143">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="8c1bd-143">-EdgeNodeSize</span></span>
<span data-ttu-id="8c1bd-144">Gibt die Größe des virtuellen Computers für den Edge-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-144">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="8c1bd-145">Verwenden Sie Get-AzureRmVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-145">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="8c1bd-146">Dieser Parameter ist nur für RServer-Cluster gültig.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-146">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="8c1bd-147">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="8c1bd-147">-HeadNodeSize</span></span>
<span data-ttu-id="8c1bd-148">Gibt die Größe des virtuellen Computers für den Head-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-148">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="8c1bd-149">Verwenden Sie Get-AzureRMVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-149">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="8c1bd-150">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="8c1bd-150">-HiveMetastore</span></span>
<span data-ttu-id="8c1bd-151">Gibt den metastore an, in dem die Struktur Metadaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-151">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="8c1bd-152">Sie können das Add-AzureRmHDInsightMetastore-Cmdlet auch verwenden.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-152">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="8c1bd-153">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="8c1bd-153">-ObjectId</span></span>
<span data-ttu-id="8c1bd-154">Gibt die Azure AD-Objekt-ID (eine GUID) des Azure AD-Dienst Prinzipals an, der den Cluster darstellt.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-154">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="8c1bd-155">Der Cluster verwendet diesen beim Zugriff auf den Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-155">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="8c1bd-156">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="8c1bd-156">-OozieMetastore</span></span>
<span data-ttu-id="8c1bd-157">Gibt den metastore an, in dem Oozie-Metadaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-157">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="8c1bd-158">Alternativ können Sie das Cmdlet **Add-AzureRmHDInsightMetastore** verwenden.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-158">You can alternatively use the **Add-AzureRmHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="8c1bd-159">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="8c1bd-159">-WorkerNodeSize</span></span>
<span data-ttu-id="8c1bd-160">Gibt die Größe des virtuellen Computers für den Worker-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-160">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="8c1bd-161">Verwenden Sie Get-AzureRMVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-161">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="8c1bd-162">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="8c1bd-162">-ZookeeperNodeSize</span></span>
<span data-ttu-id="8c1bd-163">Gibt die Größe des virtuellen Computers für den zoowärter-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-163">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="8c1bd-164">Verwenden Sie Get-AzureRMVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-164">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="8c1bd-165">Dieser Parameter ist nur für HBAs oder Storm-Cluster gültig.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-165">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="8c1bd-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c1bd-166">CommonParameters</span></span>
<span data-ttu-id="8c1bd-167">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c1bd-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c1bd-168">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c1bd-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c1bd-169">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8c1bd-169">INPUTS</span></span>

### <span data-ttu-id="8c1bd-170">Keine</span><span class="sxs-lookup"><span data-stu-id="8c1bd-170">None</span></span>

## <span data-ttu-id="8c1bd-171">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8c1bd-171">OUTPUTS</span></span>

### <span data-ttu-id="8c1bd-172">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="8c1bd-172">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="8c1bd-173">Notizen</span><span class="sxs-lookup"><span data-stu-id="8c1bd-173">NOTES</span></span>

## <span data-ttu-id="8c1bd-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8c1bd-174">RELATED LINKS</span></span>

[<span data-ttu-id="8c1bd-175">Add-AzureRmHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="8c1bd-175">Add-AzureRmHDInsightStorage</span></span>](./Add-AzureRmHDInsightStorage.md)


