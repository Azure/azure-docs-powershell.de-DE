---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 37E41DA2-B65B-4AA2-B6AB-F93CCA881C72
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightdefaultstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
ms.openlocfilehash: 06a783d0faf32dc2a3a35b448b1316ef50ba3326
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167420"
---
# <span data-ttu-id="dceda-101">Set-AzHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="dceda-101">Set-AzHDInsightDefaultStorage</span></span>

## <span data-ttu-id="dceda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dceda-102">SYNOPSIS</span></span>
<span data-ttu-id="dceda-103">Legt die Standardeinstellung für das Speicherkonto in einem Clusterkonfigurationsobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="dceda-103">Sets the default Storage account setting in a cluster configuration object.</span></span>

## <span data-ttu-id="dceda-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dceda-104">SYNTAX</span></span>

```
Set-AzHDInsightDefaultStorage [-Config] <AzureHDInsightConfig> [-StorageAccountResourceId] <String>
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dceda-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dceda-105">DESCRIPTION</span></span>
<span data-ttu-id="dceda-106">Das **Cmdlet "Set-AzHDInsightDefaultStorage"** legt die Standardeinstellung für das Speicherkonto im Konfigurationsobjekt des Azure-HDInsight-Cluster fest, das vom cmdlet New-AzHDInsightClusterConfig erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="dceda-106">The **Set-AzHDInsightDefaultStorage** cmdlet sets the default Storage account setting in the Azure HDInsight cluster configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="dceda-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dceda-107">EXAMPLES</span></span>

### <span data-ttu-id="dceda-108">Beispiel 1: Festlegen des Standardspeicherkontos für das Clusterkonfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="dceda-108">Example 1: Set the default storage account for the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageaccountname"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\>$storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Set-AzHDInsightDefaultStorage `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $key2 `
                -StorageContainer $storageContainer `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location
```

<span data-ttu-id="dceda-109">Mit diesem Befehl wird das Standardspeicherkonto für ein Clusterkonfigurationsobjekt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dceda-109">This command sets the default Storage account for a cluster configuration object.</span></span>

## <span data-ttu-id="dceda-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dceda-110">PARAMETERS</span></span>

### <span data-ttu-id="dceda-111">-Config</span><span class="sxs-lookup"><span data-stu-id="dceda-111">-Config</span></span>
<span data-ttu-id="dceda-112">Gibt das Konfigurationsobjekt für den HDInsight-Cluster an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="dceda-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="dceda-113">Dieses Objekt wird vom **Cmdlet "New-AzHDInsightClusterConfig"** erstellt.</span><span class="sxs-lookup"><span data-stu-id="dceda-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="dceda-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dceda-114">-DefaultProfile</span></span>
<span data-ttu-id="dceda-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="dceda-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dceda-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="dceda-116">-StorageAccountKey</span></span>
<span data-ttu-id="dceda-117">Gibt den Kontoschlüssel für das Azure Storage-Standardkonto an, das vom Cluster "HDInsight" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dceda-117">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dceda-118">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="dceda-118">-StorageAccountResourceId</span></span>
<span data-ttu-id="dceda-119">Der Name des Speicherkontos für das Speicherkonto, das dem neuen Cluster hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="dceda-119">The storage account name for the storage account to be added to the new cluster.</span></span>

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

### <span data-ttu-id="dceda-120">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="dceda-120">-StorageAccountType</span></span>
<span data-ttu-id="dceda-121">Ruft den Typ des Standardspeicherkontos ab oder legt diesen Typ fest.</span><span class="sxs-lookup"><span data-stu-id="dceda-121">Gets or sets the type of the default storage account.</span></span> <span data-ttu-id="dceda-122">Standardeinstellungen von AzureStorage</span><span class="sxs-lookup"><span data-stu-id="dceda-122">Defaults to AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore, AzureDataLakeStorageGen2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dceda-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dceda-123">CommonParameters</span></span>
<span data-ttu-id="dceda-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dceda-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dceda-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dceda-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dceda-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dceda-126">INPUTS</span></span>

### <span data-ttu-id="dceda-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="dceda-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="dceda-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dceda-128">OUTPUTS</span></span>

### <span data-ttu-id="dceda-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="dceda-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="dceda-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dceda-130">NOTES</span></span>

## <span data-ttu-id="dceda-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dceda-131">RELATED LINKS</span></span>
