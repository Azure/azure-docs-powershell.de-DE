---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/remove-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightCluster.md
ms.openlocfilehash: 1029871a2125668c732f7ff541582f06dbd790c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663261"
---
# <span data-ttu-id="e8faa-101">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e8faa-101">Remove-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="e8faa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e8faa-102">SYNOPSIS</span></span>
<span data-ttu-id="e8faa-103">Entfernt den angegebenen HDInsight-Cluster aus dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e8faa-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8faa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8faa-104">SYNTAX</span></span>

```
Remove-AzureRmHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8faa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e8faa-105">DESCRIPTION</span></span>
<span data-ttu-id="e8faa-106">Das Cmdlet **Remove-AzureRmHDInsightCluster** entfernt den angegebenen HDInsight-Dienst Cluster aus einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e8faa-106">The **Remove-AzureRmHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="e8faa-107">Dieser Vorgang löscht auch alle Daten, die im Hadoop Distributed File System (HDFS) auf dem Cluster gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="e8faa-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="e8faa-108">Im zugeordneten Azure Storage-Konto gespeicherte Daten werden nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e8faa-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="e8faa-109">In externen metastores gespeicherte Daten werden nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e8faa-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="e8faa-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e8faa-110">EXAMPLES</span></span>

### <span data-ttu-id="e8faa-111">Beispiel 1: Löschen eines Azure HDInsight-Clusters</span><span class="sxs-lookup"><span data-stu-id="e8faa-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzureRmHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="e8faa-112">Mit diesem Befehl wird der Cluster "Your-Hadoop-001" entfernt.</span><span class="sxs-lookup"><span data-stu-id="e8faa-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="e8faa-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8faa-113">PARAMETERS</span></span>

### <span data-ttu-id="e8faa-114">-Clustername</span><span class="sxs-lookup"><span data-stu-id="e8faa-114">-ClusterName</span></span>
<span data-ttu-id="e8faa-115">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="e8faa-115">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8faa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8faa-116">-DefaultProfile</span></span>
<span data-ttu-id="e8faa-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e8faa-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8faa-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8faa-118">-ResourceGroupName</span></span>
<span data-ttu-id="e8faa-119">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="e8faa-119">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8faa-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8faa-120">CommonParameters</span></span>
<span data-ttu-id="e8faa-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8faa-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8faa-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8faa-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8faa-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e8faa-123">INPUTS</span></span>

### <span data-ttu-id="e8faa-124">Keine</span><span class="sxs-lookup"><span data-stu-id="e8faa-124">None</span></span>
<span data-ttu-id="e8faa-125">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="e8faa-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e8faa-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e8faa-126">OUTPUTS</span></span>

### <span data-ttu-id="e8faa-127">Microsoft. Azure. Management. HDInsight. Models. ClusterGetResponse</span><span class="sxs-lookup"><span data-stu-id="e8faa-127">Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse</span></span>

## <span data-ttu-id="e8faa-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="e8faa-128">NOTES</span></span>

## <span data-ttu-id="e8faa-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e8faa-129">RELATED LINKS</span></span>

[<span data-ttu-id="e8faa-130">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e8faa-130">Get-AzureRmHDInsightCluster</span></span>](./Get-AzureRmHDInsightCluster.md)

[<span data-ttu-id="e8faa-131">Verwenden von-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e8faa-131">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


