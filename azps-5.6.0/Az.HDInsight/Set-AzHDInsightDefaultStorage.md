---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 37E41DA2-B65B-4AA2-B6AB-F93CCA881C72
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/set-azhdinsightdefaultstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
ms.openlocfilehash: 9873ba2e4fa4f54c4aa77822af076bb5426ac198
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944153"
---
# <span data-ttu-id="00b55-101">Set-AzHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="00b55-101">Set-AzHDInsightDefaultStorage</span></span>

## <span data-ttu-id="00b55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00b55-102">SYNOPSIS</span></span>
<span data-ttu-id="00b55-103">Legt die Standardeinstellung für das Speicherkonto in einem Clusterkonfigurationsobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="00b55-103">Sets the default Storage account setting in a cluster configuration object.</span></span>

## <span data-ttu-id="00b55-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="00b55-104">SYNTAX</span></span>

```
Set-AzHDInsightDefaultStorage [-Config] <AzureHDInsightConfig> [-StorageAccountResourceId] <String>
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="00b55-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="00b55-105">DESCRIPTION</span></span>
<span data-ttu-id="00b55-106">Das **Cmdlet Set-AzHDInsightDefaultStorage** legt die Standardeinstellung speicherkonto im Azure HDInsight-Clusterkonfigurationsobjekt fest, das vom cmdlet New-AzHDInsightClusterConfig erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="00b55-106">The **Set-AzHDInsightDefaultStorage** cmdlet sets the default Storage account setting in the Azure HDInsight cluster configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="00b55-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="00b55-107">EXAMPLES</span></span>

### <span data-ttu-id="00b55-108">Beispiel 1: Festlegen des Standardspeicherkontos für das Clusterkonfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="00b55-108">Example 1: Set the default storage account for the cluster configuration object</span></span>
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

<span data-ttu-id="00b55-109">Mit diesem Befehl wird das Standardspeicherkonto für ein Clusterkonfigurationsobjekt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="00b55-109">This command sets the default Storage account for a cluster configuration object.</span></span>

## <span data-ttu-id="00b55-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="00b55-110">PARAMETERS</span></span>

### <span data-ttu-id="00b55-111">-Config</span><span class="sxs-lookup"><span data-stu-id="00b55-111">-Config</span></span>
<span data-ttu-id="00b55-112">Gibt das HDInsight-Clusterkonfigurationsobjekt an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="00b55-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="00b55-113">Dieses Objekt wird vom **Cmdlet New-AzHDInsightClusterConfig** erstellt.</span><span class="sxs-lookup"><span data-stu-id="00b55-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="00b55-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00b55-114">-DefaultProfile</span></span>
<span data-ttu-id="00b55-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="00b55-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00b55-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="00b55-116">-StorageAccountKey</span></span>
<span data-ttu-id="00b55-117">Gibt den Kontoschlüssel für das Standardmäßige Azure Storage-Konto an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="00b55-117">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="00b55-118">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="00b55-118">-StorageAccountResourceId</span></span>
<span data-ttu-id="00b55-119">Der Speicherkontoname für das Speicherkonto, das dem neuen Cluster hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="00b55-119">The storage account name for the storage account to be added to the new cluster.</span></span>

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

### <span data-ttu-id="00b55-120">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="00b55-120">-StorageAccountType</span></span>
<span data-ttu-id="00b55-121">Ruft den Typ des Standardspeicherkontos ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="00b55-121">Gets or sets the type of the default storage account.</span></span> <span data-ttu-id="00b55-122">Standardwerte für AzureStorage</span><span class="sxs-lookup"><span data-stu-id="00b55-122">Defaults to AzureStorage</span></span>

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

### <span data-ttu-id="00b55-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00b55-123">CommonParameters</span></span>
<span data-ttu-id="00b55-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00b55-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00b55-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00b55-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00b55-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="00b55-126">INPUTS</span></span>

### <span data-ttu-id="00b55-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="00b55-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="00b55-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="00b55-128">OUTPUTS</span></span>

### <span data-ttu-id="00b55-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="00b55-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="00b55-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="00b55-130">NOTES</span></span>

## <span data-ttu-id="00b55-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="00b55-131">RELATED LINKS</span></span>
