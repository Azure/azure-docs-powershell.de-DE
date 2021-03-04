---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C2AF43D-18BF-4036-A355-FC27E406B18A
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/add-azhdinsightstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
ms.openlocfilehash: 47e40395d9422610bcf6fbd341141ba6e9eb3a97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938099"
---
# <span data-ttu-id="afbd9-101">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="afbd9-101">Add-AzHDInsightStorage</span></span>

## <span data-ttu-id="afbd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afbd9-102">SYNOPSIS</span></span>
<span data-ttu-id="afbd9-103">Fügt einem Clusterkonfigurationsobjekt einen Azure Storage-Schlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="afbd9-103">Adds an Azure Storage key to a cluster configuration object.</span></span>

## <span data-ttu-id="afbd9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="afbd9-104">SYNTAX</span></span>

```
Add-AzHDInsightStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="afbd9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="afbd9-105">DESCRIPTION</span></span>
<span data-ttu-id="afbd9-106">Das **Add-AzHDInsightStorage-Cmdlet** fügt dem Azure HDInsight-Konfigurationsobjekt, das vom New-AzHDInsightClusterConfig erstellt wurde, einen Azure Storage-Kontoeintrag hinzu.</span><span class="sxs-lookup"><span data-stu-id="afbd9-106">The **Add-AzHDInsightStorage** cmdlet adds an Azure Storage account entry to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="afbd9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="afbd9-107">EXAMPLES</span></span>

### <span data-ttu-id="afbd9-108">Beispiel 1: Hinzufügen eines Azure-Speicherschlüssels zum Clusterkonfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="afbd9-108">Example 1: Add an Azure storage key to the cluster configuration object</span></span>
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

# Second storage account info
PS C:\> $secondStorageAccountResourceGroupName = "Group"
PS C:\> $secondStorageAccountName = "yourstorageacct002"
PS C:\> $secondStorageAccountKey = Get-AzStorageAccountKey `
PS C:\> -ResourceGroupName $secondStorageAccountResourceGroupName `
            -Name $secondStorageAccountName | %{ $_.Key1 }

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

<span data-ttu-id="afbd9-109">Mit diesem Befehl wird der HDInsight-Konfiguration mit dem Namen your-hadoop-001 ein Blobspeicherkontoeintrag hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="afbd9-109">This command adds an blob storage account entry to the HDInsight configuration named your-hadoop-001.</span></span>

## <span data-ttu-id="afbd9-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="afbd9-110">PARAMETERS</span></span>

### <span data-ttu-id="afbd9-111">-Config</span><span class="sxs-lookup"><span data-stu-id="afbd9-111">-Config</span></span>
<span data-ttu-id="afbd9-112">Gibt das HDInsight-Clusterkonfigurationsobjekt an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="afbd9-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="afbd9-113">Dieses Objekt wird vom **Cmdlet New-AzHDInsightClusterConfig** erstellt.</span><span class="sxs-lookup"><span data-stu-id="afbd9-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="afbd9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afbd9-114">-DefaultProfile</span></span>
<span data-ttu-id="afbd9-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="afbd9-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="afbd9-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="afbd9-116">-StorageAccountKey</span></span>
<span data-ttu-id="afbd9-117">Gibt den Speicherkontoschlüssel für das Speicherkonto an, das dem neuen Cluster hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="afbd9-117">Specifies the storage account key for the storage account to be added to the new cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afbd9-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="afbd9-118">-StorageAccountName</span></span>
<span data-ttu-id="afbd9-119">Gibt den Namen des Speicherkontos für das Speicherkonto an, das dem Cluster hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="afbd9-119">Specifies the storage account name for the storage account to be added to the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afbd9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afbd9-120">CommonParameters</span></span>
<span data-ttu-id="afbd9-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afbd9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afbd9-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="afbd9-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afbd9-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="afbd9-123">INPUTS</span></span>

### <span data-ttu-id="afbd9-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="afbd9-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="afbd9-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="afbd9-125">OUTPUTS</span></span>

### <span data-ttu-id="afbd9-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="afbd9-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="afbd9-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="afbd9-127">NOTES</span></span>

## <span data-ttu-id="afbd9-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="afbd9-128">RELATED LINKS</span></span>

[<span data-ttu-id="afbd9-129">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="afbd9-129">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


