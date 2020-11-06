---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: A40AB6AB-D3CB-4A6C-B614-0B22085759DA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightclusteridentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightClusterIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightClusterIdentity.md
ms.openlocfilehash: d02dce12425015ed12e082f0bb3ba52c5b9b77c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476041"
---
# <span data-ttu-id="c36bc-101">Add-AzureRmHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="c36bc-101">Add-AzureRmHDInsightClusterIdentity</span></span>

## <span data-ttu-id="c36bc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c36bc-102">SYNOPSIS</span></span>
<span data-ttu-id="c36bc-103">Fügt einem Cluster Konfigurationsobjekt eine Clusteridentität hinzu.</span><span class="sxs-lookup"><span data-stu-id="c36bc-103">Adds a cluster identity to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c36bc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c36bc-104">SYNTAX</span></span>

### <span data-ttu-id="c36bc-105">CertificateFilePath (Standard)</span><span class="sxs-lookup"><span data-stu-id="c36bc-105">CertificateFilePath (Default)</span></span>
```
Add-AzureRmHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c36bc-106">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="c36bc-106">CertificateFileContents</span></span>
```
Add-AzureRmHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFileContents] <Byte[]> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c36bc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c36bc-107">DESCRIPTION</span></span>
<span data-ttu-id="c36bc-108">Das Cmdlet **Add-AzureRmHDInsightClusterIdentity** fügt dem Azure HDInsight-Konfigurationsobjekt, das vom New-AzureRmHDInsightClusterConfig-Cmdlet erstellt wird, eine Clusteridentität hinzu.</span><span class="sxs-lookup"><span data-stu-id="c36bc-108">The **Add-AzureRmHDInsightClusterIdentity** cmdlet adds a cluster identity to the Azure HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="c36bc-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c36bc-109">EXAMPLES</span></span>

### <span data-ttu-id="c36bc-110">Beispiel 1: Hinzufügen von Cluster Identitätsinformationen zum Cluster Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="c36bc-110">Example 1: Add Cluster Identity info to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value 
PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Cluster Identity values
PS C:\> $tenantId = (Get-AzureRmContext).Tenant.TenantId
PS C:\> $objectId = "<Azure AD Service Principal Object ID>"
PS C:\> $certificateFilePath = "<Path to Azure AD Service Principal Certificate>"
PS C:\> $certificatePassword = "<Password for Azure AD Service Principal Certificate>"

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightClusterIdentity `
                -AadTenantId $tenantId `
                -ObjectId $objectId `
                -CertificateFilePath $certificateFilePath `
                -CertificatePassword $certificatePassword `
            | New-AzureRmHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageAccountContainer
```

<span data-ttu-id="c36bc-111">Dieser Befehl fügt dem Cluster mit dem Namen "Your-Hadoop-001" Cluster-Identitätsinformationen hinzu, sodass der Cluster auf Azure Data Lake Store zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="c36bc-111">This command adds Cluster Identity info to the cluster named your-hadoop-001, allowing the cluster to access Azure Data Lake Store.</span></span>

## <span data-ttu-id="c36bc-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c36bc-112">PARAMETERS</span></span>

### <span data-ttu-id="c36bc-113">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="c36bc-113">-AadTenantId</span></span>
<span data-ttu-id="c36bc-114">Gibt die Azure AD-Mandanten-ID an, die beim Zugriff auf den Azure Data Lake Store verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c36bc-114">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c36bc-115">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="c36bc-115">-CertificateFileContents</span></span>
<span data-ttu-id="c36bc-116">Gibt den Dateiinhalt des Zertifikats an, das beim Zugriff auf den Azure Data Lake Store verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c36bc-116">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: CertificateFileContents
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c36bc-117">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="c36bc-117">-CertificateFilePath</span></span>
<span data-ttu-id="c36bc-118">Gibt den Dateipfad zu dem Zertifikat an, das zur Authentifizierung als Dienstprinzipal verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c36bc-118">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="c36bc-119">Der Cluster verwendet diesen beim Zugriff auf den Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c36bc-119">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: CertificateFilePath
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c36bc-120">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="c36bc-120">-CertificatePassword</span></span>
<span data-ttu-id="c36bc-121">Gibt das Kennwort für das Zertifikat an, das für die Authentifizierung als Dienstprinzipal verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c36bc-121">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="c36bc-122">Der Cluster verwendet diesen beim Zugriff auf den Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c36bc-122">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c36bc-123">-Config</span><span class="sxs-lookup"><span data-stu-id="c36bc-123">-Config</span></span>
<span data-ttu-id="c36bc-124">Gibt das HDInsight-Cluster Konfigurationsobjekt an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="c36bc-124">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="c36bc-125">Dieses Objekt wird vom New-AzureRmHDInsightClusterConfig-Cmdlet erstellt.</span><span class="sxs-lookup"><span data-stu-id="c36bc-125">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c36bc-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c36bc-126">-DefaultProfile</span></span>
<span data-ttu-id="c36bc-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c36bc-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c36bc-128">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="c36bc-128">-ObjectId</span></span>
<span data-ttu-id="c36bc-129">Gibt die Azure AD-Objekt-ID (eine GUID) des Azure AD-Dienst Prinzipals an, der den Cluster darstellt.</span><span class="sxs-lookup"><span data-stu-id="c36bc-129">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="c36bc-130">Der Cluster verwendet diesen beim Zugriff auf den Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c36bc-130">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c36bc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c36bc-131">CommonParameters</span></span>
<span data-ttu-id="c36bc-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c36bc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c36bc-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c36bc-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c36bc-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c36bc-134">INPUTS</span></span>

### <span data-ttu-id="c36bc-135">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="c36bc-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
<span data-ttu-id="c36bc-136">Parameter: config (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c36bc-136">Parameters: Config (ByValue)</span></span>

### <span data-ttu-id="c36bc-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c36bc-137">System.Guid</span></span>
<span data-ttu-id="c36bc-138">Parameter: ObjectID (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c36bc-138">Parameters: ObjectId (ByValue)</span></span>

## <span data-ttu-id="c36bc-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c36bc-139">OUTPUTS</span></span>

### <span data-ttu-id="c36bc-140">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="c36bc-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="c36bc-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="c36bc-141">NOTES</span></span>

## <span data-ttu-id="c36bc-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c36bc-142">RELATED LINKS</span></span>

[<span data-ttu-id="c36bc-143">Neu – AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="c36bc-143">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


