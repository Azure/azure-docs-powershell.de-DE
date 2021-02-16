---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A40AB6AB-D3CB-4A6C-B614-0B22085759DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightclusteridentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
ms.openlocfilehash: 6d3924f3613d01e515e58e1b35c3640b0447ca06
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175372"
---
# <span data-ttu-id="93f69-101">Add-AzHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="93f69-101">Add-AzHDInsightClusterIdentity</span></span>

## <span data-ttu-id="93f69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93f69-102">SYNOPSIS</span></span>
<span data-ttu-id="93f69-103">Fügt einem Clusterkonfigurationsobjekt eine Clusteridentität hinzu.</span><span class="sxs-lookup"><span data-stu-id="93f69-103">Adds a cluster identity to a cluster configuration object.</span></span>

## <span data-ttu-id="93f69-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93f69-104">SYNTAX</span></span>

### <span data-ttu-id="93f69-105">CertificateFilePath (Standard)</span><span class="sxs-lookup"><span data-stu-id="93f69-105">CertificateFilePath (Default)</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [[-ApplicationId] <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93f69-106">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="93f69-106">CertificateFileContents</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFileContents] <Byte[]> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [[-ApplicationId] <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93f69-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="93f69-107">DESCRIPTION</span></span>
<span data-ttu-id="93f69-108">Das **Cmdlet "Add-AzHDInsightClusterIdentity"** fügt dem Azure HDInsight-Konfigurationsobjekt, das vom cmdlet New-AzHDInsightClusterConfig erstellt wurde, eine Clusteridentität hinzu.</span><span class="sxs-lookup"><span data-stu-id="93f69-108">The **Add-AzHDInsightClusterIdentity** cmdlet adds a cluster identity to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="93f69-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="93f69-109">EXAMPLES</span></span>

### <span data-ttu-id="93f69-110">Beispiel 1: Hinzufügen von Clusteridentitätsinformationen zum Clusterkonfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="93f69-110">Example 1: Add Cluster Identity info to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value 
PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Cluster Identity values
PS C:\> $tenantId = (Get-AzContext).Tenant.TenantId
PS C:\> $objectId = "<Azure AD Service Principal Object ID>"
PS C:\> $applicationId = "<Azure AD Service Principal Application ID>"
PS C:\> $certificateFilePath = "<Path to Azure AD Service Principal Certificate>"
PS C:\> $certificatePassword = "<Password for Azure AD Service Principal Certificate>"

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightClusterIdentity `
                -AadTenantId $tenantId `
                -ObjectId $objectId `
                -Application $applicationId
                -CertificateFilePath $certificateFilePath `
                -CertificatePassword $certificatePassword `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Linux `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageAccountContainer
```

<span data-ttu-id="93f69-111">Mit diesem Befehl werden dem Cluster Informationen zur Clusteridentität mit dem Namen "Ihr-Hadoop-001" hinzufügt, sodass der Cluster auf Azure Data Lake Store zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="93f69-111">This command adds Cluster Identity info to the cluster named your-hadoop-001, allowing the cluster to access Azure Data Lake Store.</span></span>

## <span data-ttu-id="93f69-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93f69-112">PARAMETERS</span></span>

### <span data-ttu-id="93f69-113">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="93f69-113">-AadTenantId</span></span>
<span data-ttu-id="93f69-114">Gibt die Azure AD-Mandanten-ID an, die beim Zugriff auf Azure Data Lake Store verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="93f69-114">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="93f69-115">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="93f69-115">-ApplicationId</span></span>
<span data-ttu-id="93f69-116">Die Dienstprinzipalanwendungs-ID für den Zugriff auf Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="93f69-116">The Service Principal Application Id for accessing Azure Data Lake.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f69-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="93f69-117">-CertificateFileContents</span></span>
<span data-ttu-id="93f69-118">Gibt den Dateiinhalt des Zertifikats an, das beim Zugriff auf Azure Data Lake Store verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="93f69-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="93f69-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="93f69-119">-CertificateFilePath</span></span>
<span data-ttu-id="93f69-120">Gibt den Dateipfad des Zertifikats an, das zur Authentifizierung als Dienstprinzipal verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="93f69-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="93f69-121">Der Cluster verwendet dies beim Zugriff auf Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="93f69-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="93f69-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="93f69-122">-CertificatePassword</span></span>
<span data-ttu-id="93f69-123">Gibt das Kennwort für das Zertifikat an, das zur Authentifizierung als Dienstprinzipal verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="93f69-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="93f69-124">Der Cluster verwendet dies beim Zugriff auf Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="93f69-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="93f69-125">-Config</span><span class="sxs-lookup"><span data-stu-id="93f69-125">-Config</span></span>
<span data-ttu-id="93f69-126">Gibt das Konfigurationsobjekt für den HDInsight-Cluster an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="93f69-126">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="93f69-127">Dieses Objekt wird vom New-AzHDInsightClusterConfig erstellt.</span><span class="sxs-lookup"><span data-stu-id="93f69-127">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="93f69-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93f69-128">-DefaultProfile</span></span>
<span data-ttu-id="93f69-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="93f69-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93f69-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="93f69-130">-ObjectId</span></span>
<span data-ttu-id="93f69-131">Gibt die Azure AD-Objekt-ID (GUID) des Azure AD-Dienstprinzipal an, der den Cluster darstellt.</span><span class="sxs-lookup"><span data-stu-id="93f69-131">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="93f69-132">Der Cluster verwendet dies beim Zugriff auf Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="93f69-132">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="93f69-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93f69-133">CommonParameters</span></span>
<span data-ttu-id="93f69-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93f69-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93f69-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93f69-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93f69-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="93f69-136">INPUTS</span></span>

### <span data-ttu-id="93f69-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="93f69-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

### <span data-ttu-id="93f69-138">System.Guid</span><span class="sxs-lookup"><span data-stu-id="93f69-138">System.Guid</span></span>

## <span data-ttu-id="93f69-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="93f69-139">OUTPUTS</span></span>

### <span data-ttu-id="93f69-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="93f69-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="93f69-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="93f69-141">NOTES</span></span>

## <span data-ttu-id="93f69-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="93f69-142">RELATED LINKS</span></span>

[<span data-ttu-id="93f69-143">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="93f69-143">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


