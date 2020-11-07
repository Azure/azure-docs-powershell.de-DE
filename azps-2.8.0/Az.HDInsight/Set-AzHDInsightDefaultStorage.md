---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 37E41DA2-B65B-4AA2-B6AB-F93CCA881C72
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightdefaultstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
ms.openlocfilehash: 6815e697376f51d70782885485541debb209ecf7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651029"
---
# <span data-ttu-id="03e8c-101">Set-AzHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="03e8c-101">Set-AzHDInsightDefaultStorage</span></span>

## <span data-ttu-id="03e8c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="03e8c-102">SYNOPSIS</span></span>
<span data-ttu-id="03e8c-103">Legt die Standardeinstellung für das Speicherkonto in einem Cluster Konfigurationsobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="03e8c-103">Sets the default Storage account setting in a cluster configuration object.</span></span>

## <span data-ttu-id="03e8c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="03e8c-104">SYNTAX</span></span>

```
Set-AzHDInsightDefaultStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="03e8c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="03e8c-105">DESCRIPTION</span></span>
<span data-ttu-id="03e8c-106">Das Cmdlet " **Set-AzHDInsightDefaultStorage** " legt die Standardeinstellung für das Speicherkonto im Azure HDInsight-Cluster Konfigurationsobjekt fest, das vom Cmdlet "New-AzHDInsightClusterConfig" erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="03e8c-106">The **Set-AzHDInsightDefaultStorage** cmdlet sets the default Storage account setting in the Azure HDInsight cluster configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="03e8c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="03e8c-107">EXAMPLES</span></span>

### <span data-ttu-id="03e8c-108">Beispiel 1: Festlegen des Standardspeicher Kontos für das Cluster Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="03e8c-108">Example 1: Set the default storage account for the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
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
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
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

<span data-ttu-id="03e8c-109">Dieser Befehl legt das Standardspeicher Konto für ein Cluster Konfigurationsobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="03e8c-109">This command sets the default Storage account for a cluster configuration object.</span></span>

## <span data-ttu-id="03e8c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="03e8c-110">PARAMETERS</span></span>

### <span data-ttu-id="03e8c-111">-Config</span><span class="sxs-lookup"><span data-stu-id="03e8c-111">-Config</span></span>
<span data-ttu-id="03e8c-112">Gibt das HDInsight-Cluster Konfigurationsobjekt an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="03e8c-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="03e8c-113">Dieses Objekt wird vom Cmdlet **New-AzHDInsightClusterConfig** erstellt.</span><span class="sxs-lookup"><span data-stu-id="03e8c-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="03e8c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03e8c-114">-DefaultProfile</span></span>
<span data-ttu-id="03e8c-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="03e8c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03e8c-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="03e8c-116">-StorageAccountKey</span></span>
<span data-ttu-id="03e8c-117">Gibt den Kontoschlüssel für das standardmäßige Azure Storage-Konto an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="03e8c-117">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="03e8c-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="03e8c-118">-StorageAccountName</span></span>
<span data-ttu-id="03e8c-119">Gibt den Namen des Standardspeicher Kontos an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="03e8c-119">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="03e8c-120">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="03e8c-120">-StorageAccountType</span></span>
<span data-ttu-id="03e8c-121">Ruft den Typ des Standardspeicher Kontos ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="03e8c-121">Gets or sets the type of the default storage account.</span></span> <span data-ttu-id="03e8c-122">Standardmäßig AzureStorage</span><span class="sxs-lookup"><span data-stu-id="03e8c-122">Defaults to AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03e8c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03e8c-123">CommonParameters</span></span>
<span data-ttu-id="03e8c-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03e8c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03e8c-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03e8c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03e8c-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="03e8c-126">INPUTS</span></span>

### <span data-ttu-id="03e8c-127">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="03e8c-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="03e8c-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="03e8c-128">OUTPUTS</span></span>

### <span data-ttu-id="03e8c-129">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="03e8c-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="03e8c-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="03e8c-130">NOTES</span></span>

## <span data-ttu-id="03e8c-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="03e8c-131">RELATED LINKS</span></span>
