---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2C2AF43D-18BF-4036-A355-FC27E406B18A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightStorage.md
ms.openlocfilehash: f70403f70e116a0e6addc569942f927aca0dcf0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500038"
---
# <span data-ttu-id="e6409-101">Add-AzureRmHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="e6409-101">Add-AzureRmHDInsightStorage</span></span>

## <span data-ttu-id="e6409-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e6409-102">SYNOPSIS</span></span>
<span data-ttu-id="e6409-103">Fügt einen Azure-Speicherschlüssel zu einem Cluster-Konfigurationsobjekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="e6409-103">Adds an Azure Storage key to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6409-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6409-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6409-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e6409-105">DESCRIPTION</span></span>
<span data-ttu-id="e6409-106">Das Cmdlet **Add-AzureRmHDInsightStorage** fügt dem Azure HDInsight-Konfigurationsobjekt, das vom Cmdlet New-AzureRmHDInsightClusterConfig erstellt wurde, einen Azure-Speicherkonto Eintrag hinzu.</span><span class="sxs-lookup"><span data-stu-id="e6409-106">The **Add-AzureRmHDInsightStorage** cmdlet adds an Azure Storage account entry to the Azure HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="e6409-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e6409-107">EXAMPLES</span></span>

### <span data-ttu-id="e6409-108">Beispiel 1: Hinzufügen eines Azure Storage-Schlüssels zum Cluster-Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="e6409-108">Example 1: Add an Azure storage key to the cluster configuration object</span></span>
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

# Second storage account info
PS C:\> $secondStorageAccountResourceGroupName = "Group"
PS C:\> $secondStorageAccountName = "yourstorageacct002"
PS C:\> $secondStorageAccountKey = Get-AzureRmStorageAccountKey `
PS C:\> -ResourceGroupName $secondStorageAccountResourceGroupName `
            -Name $secondStorageAccountName | %{ $_.Key1 }

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

<span data-ttu-id="e6409-109">Mit diesem Befehl wird der HDInsight-Konfiguration mit dem Namen "Your-Hadoop-001" ein BLOB-Speicherkonto Eintrag hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e6409-109">This command adds an blob storage account entry to the HDInsight configuration named your-hadoop-001.</span></span>

## <span data-ttu-id="e6409-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6409-110">PARAMETERS</span></span>

### <span data-ttu-id="e6409-111">-Config</span><span class="sxs-lookup"><span data-stu-id="e6409-111">-Config</span></span>
<span data-ttu-id="e6409-112">Gibt das HDInsight-Cluster Konfigurationsobjekt an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="e6409-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="e6409-113">Dieses Objekt wird vom Cmdlet **New-AzureRmHDInsightClusterConfig** erstellt.</span><span class="sxs-lookup"><span data-stu-id="e6409-113">This object is created by the **New-AzureRmHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="e6409-114">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e6409-114">-StorageAccountKey</span></span>
<span data-ttu-id="e6409-115">Gibt den speicherkontoschlüssel für das Speicherkonto an, das dem neuen Cluster hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e6409-115">Specifies the storage account key for the storage account to be added to the new cluster.</span></span>

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

### <span data-ttu-id="e6409-116">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e6409-116">-StorageAccountName</span></span>
<span data-ttu-id="e6409-117">Gibt den Namen des speicherkontos für das Speicherkonto an, das dem Cluster hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e6409-117">Specifies the storage account name for the storage account to be added to the cluster.</span></span>

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

### <span data-ttu-id="e6409-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6409-118">-DefaultProfile</span></span>
<span data-ttu-id="e6409-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e6409-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6409-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6409-120">CommonParameters</span></span>
<span data-ttu-id="e6409-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6409-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6409-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6409-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6409-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e6409-123">INPUTS</span></span>

### <span data-ttu-id="e6409-124">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="e6409-124">AzureHDInsightConfig</span></span>
<span data-ttu-id="e6409-125">Der Parameter "config" akzeptiert den Wert vom Typ "AzureHDInsightConfig" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="e6409-125">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="e6409-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e6409-126">OUTPUTS</span></span>

### <span data-ttu-id="e6409-127">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="e6409-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="e6409-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="e6409-128">NOTES</span></span>

## <span data-ttu-id="e6409-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e6409-129">RELATED LINKS</span></span>

[<span data-ttu-id="e6409-130">Neu – AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="e6409-130">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


