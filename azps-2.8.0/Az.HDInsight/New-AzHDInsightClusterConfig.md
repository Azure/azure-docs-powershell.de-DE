---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: fad988977cf5fe24e440d654206e0f1a212be6b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651051"
---
# <span data-ttu-id="0d799-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="0d799-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="0d799-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0d799-102">SYNOPSIS</span></span>
<span data-ttu-id="0d799-103">Erstellt ein nicht persistentes Cluster Konfigurationsobjekt, das eine Azure HDInsight-Cluster Konfiguration beschreibt.</span><span class="sxs-lookup"><span data-stu-id="0d799-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="0d799-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d799-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0d799-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d799-105">DESCRIPTION</span></span>
<span data-ttu-id="0d799-106">Das Cmdlet **New-AzHDInsightClusterConfig** erstellt ein nicht beibehaltenes Objekt, das eine Azure HDInsight-Cluster Konfiguration beschreibt.</span><span class="sxs-lookup"><span data-stu-id="0d799-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="0d799-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d799-107">EXAMPLES</span></span>

### <span data-ttu-id="0d799-108">Beispiel 1: Erstellen eines Cluster Konfigurationsobjekts</span><span class="sxs-lookup"><span data-stu-id="0d799-108">Example 1: Create a cluster configuration object</span></span>
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

<span data-ttu-id="0d799-109">Mit diesem Befehl wird ein Cluster Konfigurationsobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="0d799-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="0d799-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d799-110">PARAMETERS</span></span>

### <span data-ttu-id="0d799-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="0d799-111">-AadTenantId</span></span>
<span data-ttu-id="0d799-112">Gibt die Azure AD-Mandanten-ID an, die beim Zugriff auf den Azure Data Lake Store verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0d799-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="0d799-113">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="0d799-113">-CertificateFileContents</span></span>
<span data-ttu-id="0d799-114">Gibt den Dateiinhalt des Zertifikats an, das beim Zugriff auf den Azure Data Lake Store verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0d799-114">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="0d799-115">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="0d799-115">-CertificateFilePath</span></span>
<span data-ttu-id="0d799-116">Gibt den Dateipfad zu dem Zertifikat an, das zur Authentifizierung als Dienstprinzipal verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0d799-116">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="0d799-117">Der Cluster verwendet diesen beim Zugriff auf den Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0d799-117">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="0d799-118">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="0d799-118">-CertificatePassword</span></span>
<span data-ttu-id="0d799-119">Gibt das Kennwort für das Zertifikat an, das für die Authentifizierung als Dienstprinzipal verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0d799-119">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="0d799-120">Der Cluster verwendet diesen beim Zugriff auf den Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0d799-120">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="0d799-121">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="0d799-121">-ClusterTier</span></span>
<span data-ttu-id="0d799-122">Gibt die HDInsight-Clusterebene an.</span><span class="sxs-lookup"><span data-stu-id="0d799-122">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="0d799-123">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0d799-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0d799-124">Standard</span><span class="sxs-lookup"><span data-stu-id="0d799-124">Standard</span></span>
- <span data-ttu-id="0d799-125">Premium der Standardwert ist Standard.</span><span class="sxs-lookup"><span data-stu-id="0d799-125">Premium The default value is Standard.</span></span>
<span data-ttu-id="0d799-126">Die Premium-Stufe kann nur mit Linux-Clustern verwendet werden und ermöglicht die Verwendung einiger neuer Funktionen.</span><span class="sxs-lookup"><span data-stu-id="0d799-126">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="0d799-127">-Clustertyp</span><span class="sxs-lookup"><span data-stu-id="0d799-127">-ClusterType</span></span>
<span data-ttu-id="0d799-128">Gibt den Typ des zu erstellende Clusters an.</span><span class="sxs-lookup"><span data-stu-id="0d799-128">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="0d799-129">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0d799-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0d799-130">Hadoop</span><span class="sxs-lookup"><span data-stu-id="0d799-130">Hadoop</span></span>
- <span data-ttu-id="0d799-131">HBase</span><span class="sxs-lookup"><span data-stu-id="0d799-131">HBase</span></span>
- <span data-ttu-id="0d799-132">Sturm</span><span class="sxs-lookup"><span data-stu-id="0d799-132">Storm</span></span>
- <span data-ttu-id="0d799-133">Funken</span><span class="sxs-lookup"><span data-stu-id="0d799-133">Spark</span></span>

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

### <span data-ttu-id="0d799-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d799-134">-DefaultProfile</span></span>
<span data-ttu-id="0d799-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="0d799-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d799-136">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="0d799-136">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="0d799-137">Gibt den Kontoschlüssel für das standardmäßige Azure Storage-Konto an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0d799-137">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="0d799-138">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0d799-138">-DefaultStorageAccountName</span></span>
<span data-ttu-id="0d799-139">Gibt den Namen des Standardspeicher Kontos an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0d799-139">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="0d799-140">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="0d799-140">-DefaultStorageAccountType</span></span>
<span data-ttu-id="0d799-141">Gibt den Typ des Standardspeicher Kontos an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0d799-141">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="0d799-142">Mögliche Werte sind AzureStorage und AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="0d799-142">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

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

### <span data-ttu-id="0d799-143">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="0d799-143">-EdgeNodeSize</span></span>
<span data-ttu-id="0d799-144">Gibt die Größe des virtuellen Computers für den Edge-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="0d799-144">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="0d799-145">Verwenden Sie Get-AzVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="0d799-145">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="0d799-146">Dieser Parameter ist nur für RServer-Cluster gültig.</span><span class="sxs-lookup"><span data-stu-id="0d799-146">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="0d799-147">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="0d799-147">-HeadNodeSize</span></span>
<span data-ttu-id="0d799-148">Gibt die Größe des virtuellen Computers für den Head-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="0d799-148">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="0d799-149">Verwenden Sie Get-AzVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="0d799-149">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="0d799-150">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="0d799-150">-HiveMetastore</span></span>
<span data-ttu-id="0d799-151">Gibt den metastore an, in dem die Struktur Metadaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="0d799-151">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="0d799-152">Sie können das Add-AzHDInsightMetastore-Cmdlet auch verwenden.</span><span class="sxs-lookup"><span data-stu-id="0d799-152">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="0d799-153">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="0d799-153">-ObjectId</span></span>
<span data-ttu-id="0d799-154">Gibt die Azure AD-Objekt-ID (eine GUID) des Azure AD-Dienst Prinzipals an, der den Cluster darstellt.</span><span class="sxs-lookup"><span data-stu-id="0d799-154">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="0d799-155">Der Cluster verwendet diesen beim Zugriff auf den Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0d799-155">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="0d799-156">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="0d799-156">-OozieMetastore</span></span>
<span data-ttu-id="0d799-157">Gibt den metastore an, in dem Oozie-Metadaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="0d799-157">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="0d799-158">Alternativ können Sie das Cmdlet **Add-AzHDInsightMetastore** verwenden.</span><span class="sxs-lookup"><span data-stu-id="0d799-158">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="0d799-159">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="0d799-159">-WorkerNodeSize</span></span>
<span data-ttu-id="0d799-160">Gibt die Größe des virtuellen Computers für den Worker-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="0d799-160">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="0d799-161">Verwenden Sie Get-AzVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="0d799-161">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="0d799-162">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="0d799-162">-ZookeeperNodeSize</span></span>
<span data-ttu-id="0d799-163">Gibt die Größe des virtuellen Computers für den zoowärter-Knoten an.</span><span class="sxs-lookup"><span data-stu-id="0d799-163">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="0d799-164">Verwenden Sie Get-AzVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.</span><span class="sxs-lookup"><span data-stu-id="0d799-164">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="0d799-165">Dieser Parameter ist nur für HBAs oder Storm-Cluster gültig.</span><span class="sxs-lookup"><span data-stu-id="0d799-165">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="0d799-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d799-166">CommonParameters</span></span>
<span data-ttu-id="0d799-167">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d799-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d799-168">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d799-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d799-169">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0d799-169">INPUTS</span></span>

### <span data-ttu-id="0d799-170">Keine</span><span class="sxs-lookup"><span data-stu-id="0d799-170">None</span></span>

## <span data-ttu-id="0d799-171">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0d799-171">OUTPUTS</span></span>

### <span data-ttu-id="0d799-172">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="0d799-172">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="0d799-173">Notizen</span><span class="sxs-lookup"><span data-stu-id="0d799-173">NOTES</span></span>

## <span data-ttu-id="0d799-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0d799-174">RELATED LINKS</span></span>

[<span data-ttu-id="0d799-175">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="0d799-175">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


