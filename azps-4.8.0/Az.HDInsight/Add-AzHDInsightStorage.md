---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C2AF43D-18BF-4036-A355-FC27E406B18A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
ms.openlocfilehash: 43850e035a59674b06502db1486de0d90fe6e4ba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94172972"
---
# <span data-ttu-id="ce660-101">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="ce660-101">Add-AzHDInsightStorage</span></span>

## <span data-ttu-id="ce660-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ce660-102">SYNOPSIS</span></span>
<span data-ttu-id="ce660-103">Fügt einen Azure-Speicherschlüssel zu einem Cluster-Konfigurationsobjekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="ce660-103">Adds an Azure Storage key to a cluster configuration object.</span></span>

## <span data-ttu-id="ce660-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce660-104">SYNTAX</span></span>

```
Add-AzHDInsightStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce660-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce660-105">DESCRIPTION</span></span>
<span data-ttu-id="ce660-106">Das Cmdlet **Add-AzHDInsightStorage** fügt dem Azure HDInsight-Konfigurationsobjekt, das vom Cmdlet New-AzHDInsightClusterConfig erstellt wurde, einen Azure-Speicherkonto Eintrag hinzu.</span><span class="sxs-lookup"><span data-stu-id="ce660-106">The **Add-AzHDInsightStorage** cmdlet adds an Azure Storage account entry to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="ce660-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ce660-107">EXAMPLES</span></span>

### <span data-ttu-id="ce660-108">Beispiel 1: Hinzufügen eines Azure Storage-Schlüssels zum Cluster-Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="ce660-108">Example 1: Add an Azure storage key to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
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
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="ce660-109">Mit diesem Befehl wird der HDInsight-Konfiguration mit dem Namen "Your-Hadoop-001" ein BLOB-Speicherkonto Eintrag hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ce660-109">This command adds an blob storage account entry to the HDInsight configuration named your-hadoop-001.</span></span>

## <span data-ttu-id="ce660-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce660-110">PARAMETERS</span></span>

### <span data-ttu-id="ce660-111">-Config</span><span class="sxs-lookup"><span data-stu-id="ce660-111">-Config</span></span>
<span data-ttu-id="ce660-112">Gibt das HDInsight-Cluster Konfigurationsobjekt an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="ce660-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="ce660-113">Dieses Objekt wird vom Cmdlet **New-AzHDInsightClusterConfig** erstellt.</span><span class="sxs-lookup"><span data-stu-id="ce660-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="ce660-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce660-114">-DefaultProfile</span></span>
<span data-ttu-id="ce660-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ce660-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce660-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ce660-116">-StorageAccountKey</span></span>
<span data-ttu-id="ce660-117">Gibt den speicherkontoschlüssel für das Speicherkonto an, das dem neuen Cluster hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ce660-117">Specifies the storage account key for the storage account to be added to the new cluster.</span></span>

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

### <span data-ttu-id="ce660-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ce660-118">-StorageAccountName</span></span>
<span data-ttu-id="ce660-119">Gibt den Namen des speicherkontos für das Speicherkonto an, das dem Cluster hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ce660-119">Specifies the storage account name for the storage account to be added to the cluster.</span></span>

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

### <span data-ttu-id="ce660-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce660-120">CommonParameters</span></span>
<span data-ttu-id="ce660-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce660-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce660-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce660-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce660-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ce660-123">INPUTS</span></span>

### <span data-ttu-id="ce660-124">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="ce660-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="ce660-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ce660-125">OUTPUTS</span></span>

### <span data-ttu-id="ce660-126">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="ce660-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="ce660-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="ce660-127">NOTES</span></span>

## <span data-ttu-id="ce660-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ce660-128">RELATED LINKS</span></span>

[<span data-ttu-id="ce660-129">Neu – AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="ce660-129">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


