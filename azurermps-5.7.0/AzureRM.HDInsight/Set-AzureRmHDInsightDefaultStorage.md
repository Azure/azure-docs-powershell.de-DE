---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 37E41DA2-B65B-4AA2-B6AB-F93CCA881C72
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/set-azurermhdinsightdefaultstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightDefaultStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightDefaultStorage.md
ms.openlocfilehash: 43418937c379ba1ac93b5a2c733028e31eef7318
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663066"
---
# <span data-ttu-id="b1daf-101">Set-AzureRmHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="b1daf-101">Set-AzureRmHDInsightDefaultStorage</span></span>

## <span data-ttu-id="b1daf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b1daf-102">SYNOPSIS</span></span>
<span data-ttu-id="b1daf-103">Legt die Standardeinstellung für das Speicherkonto in einem Cluster Konfigurationsobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="b1daf-103">Sets the default Storage account setting in a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1daf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1daf-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightDefaultStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b1daf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1daf-105">DESCRIPTION</span></span>
<span data-ttu-id="b1daf-106">Das Cmdlet " **Set-AzureRmHDInsightDefaultStorage** " legt die Standardeinstellung für das Speicherkonto im Azure HDInsight-Cluster Konfigurationsobjekt fest, das vom Cmdlet "New-AzureRmHDInsightClusterConfig" erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b1daf-106">The **Set-AzureRmHDInsightDefaultStorage** cmdlet sets the default Storage account setting in the Azure HDInsight cluster configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="b1daf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b1daf-107">EXAMPLES</span></span>

### <span data-ttu-id="b1daf-108">Beispiel 1: Festlegen des Standardspeicher Kontos für das Cluster Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="b1daf-108">Example 1: Set the default storage account for the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\>$storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRMResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Set-AzureRmHDInsightDefaultStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
                -StorageContainer $storageContainer `
            | New-AzureRmHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location
```

<span data-ttu-id="b1daf-109">Dieser Befehl legt das Standardspeicher Konto für ein Cluster Konfigurationsobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="b1daf-109">This command sets the default Storage account for a cluster configuration object.</span></span>

## <span data-ttu-id="b1daf-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1daf-110">PARAMETERS</span></span>

### <span data-ttu-id="b1daf-111">-Config</span><span class="sxs-lookup"><span data-stu-id="b1daf-111">-Config</span></span>
<span data-ttu-id="b1daf-112">Gibt das HDInsight-Cluster Konfigurationsobjekt an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="b1daf-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="b1daf-113">Dieses Objekt wird vom Cmdlet **New-AzureRmHDInsightClusterConfig** erstellt.</span><span class="sxs-lookup"><span data-stu-id="b1daf-113">This object is created by the **New-AzureRmHDInsightClusterConfig** cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1daf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1daf-114">-DefaultProfile</span></span>
<span data-ttu-id="b1daf-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b1daf-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1daf-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="b1daf-116">-StorageAccountKey</span></span>
<span data-ttu-id="b1daf-117">Gibt den Kontoschlüssel für das standardmäßige Azure Storage-Konto an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b1daf-117">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1daf-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b1daf-118">-StorageAccountName</span></span>
<span data-ttu-id="b1daf-119">Gibt den Namen des Standardspeicher Kontos an, das vom HDInsight-Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b1daf-119">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1daf-120">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="b1daf-120">-StorageAccountType</span></span>
<span data-ttu-id="b1daf-121">Ruft den Typ des Standardspeicher Kontos ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="b1daf-121">Gets or sets the type of the default storage account.</span></span> <span data-ttu-id="b1daf-122">Standardmäßig AzureStorage</span><span class="sxs-lookup"><span data-stu-id="b1daf-122">Defaults to AzureStorage</span></span>

```yaml
Type: StorageType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1daf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1daf-123">CommonParameters</span></span>
<span data-ttu-id="b1daf-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1daf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1daf-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1daf-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1daf-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b1daf-126">INPUTS</span></span>

### <span data-ttu-id="b1daf-127">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="b1daf-127">AzureHDInsightConfig</span></span>
<span data-ttu-id="b1daf-128">Der Parameter "config" akzeptiert den Wert vom Typ "AzureHDInsightConfig" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b1daf-128">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="b1daf-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b1daf-129">OUTPUTS</span></span>

### <span data-ttu-id="b1daf-130">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="b1daf-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="b1daf-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="b1daf-131">NOTES</span></span>

## <span data-ttu-id="b1daf-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b1daf-132">RELATED LINKS</span></span>

