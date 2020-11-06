---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/start-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Start-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Start-AzureRmHDInsightJob.md
ms.openlocfilehash: 8c3e0f01472469be856d69c1a87f8eb5185f2012
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504570"
---
# <span data-ttu-id="b756c-101">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b756c-101">Start-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="b756c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b756c-102">SYNOPSIS</span></span>
<span data-ttu-id="b756c-103">Startet einen definierten Azure HDInsight-Auftrag in einem angegebenen Cluster.</span><span class="sxs-lookup"><span data-stu-id="b756c-103">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b756c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b756c-104">SYNTAX</span></span>

```
Start-AzureRmHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b756c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b756c-105">DESCRIPTION</span></span>
<span data-ttu-id="b756c-106">Mit dem Cmdlet **Start-AzureRMHDInsightJob** wird ein definierter Azure HDInsight-Auftrag in einem angegebenen Cluster gestartet.</span><span class="sxs-lookup"><span data-stu-id="b756c-106">The **Start-AzureRMHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="b756c-107">Dies kann ein MapReduce-Auftrag, ein Streaming-MapReduce-Auftrag, ein Hive-Job oder ein Pig-Job sein.</span><span class="sxs-lookup"><span data-stu-id="b756c-107">This can be a MapReduce job, a Streaming MapReduce job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="b756c-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b756c-108">EXAMPLES</span></span>

### <span data-ttu-id="b756c-109">Beispiel 1: Starten eines Auftrags auf dem angegebenen Cluster</span><span class="sxs-lookup"><span data-stu-id="b756c-109">Example 1: Start a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="b756c-110">Mit diesem Befehl wird ein Auftrag auf dem Cluster "Your-Hadoop-001" gestartet.</span><span class="sxs-lookup"><span data-stu-id="b756c-110">This command starts a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="b756c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b756c-111">PARAMETERS</span></span>

### <span data-ttu-id="b756c-112">-Clustername</span><span class="sxs-lookup"><span data-stu-id="b756c-112">-ClusterName</span></span>
<span data-ttu-id="b756c-113">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="b756c-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="b756c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b756c-114">-DefaultProfile</span></span>
<span data-ttu-id="b756c-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b756c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b756c-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="b756c-116">-HttpCredential</span></span>
<span data-ttu-id="b756c-117">Gibt die Anmeldeinformationen für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="b756c-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b756c-118">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="b756c-118">-JobDefinition</span></span>
<span data-ttu-id="b756c-119">Gibt den Auftrag an, der im Azure HDInsight-Cluster gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b756c-119">Specifies the job to start on the Azure HDInsight cluster.</span></span>

```yaml
Type: AzureHDInsightJobDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b756c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b756c-120">-ResourceGroupName</span></span>
<span data-ttu-id="b756c-121">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b756c-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b756c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b756c-122">CommonParameters</span></span>
<span data-ttu-id="b756c-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b756c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b756c-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b756c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b756c-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b756c-125">INPUTS</span></span>

### <span data-ttu-id="b756c-126">AzureHDInsightJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b756c-126">AzureHDInsightJobDefinition</span></span>
<span data-ttu-id="b756c-127">Der Parameter "JobDefinition" akzeptiert den Wert vom Typ "AzureHDInsightJobDefinition" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b756c-127">Parameter 'JobDefinition' accepts value of type 'AzureHDInsightJobDefinition' from the pipeline</span></span>

## <span data-ttu-id="b756c-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b756c-128">OUTPUTS</span></span>

### <span data-ttu-id="b756c-129">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b756c-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="b756c-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="b756c-130">NOTES</span></span>

## <span data-ttu-id="b756c-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b756c-131">RELATED LINKS</span></span>

[<span data-ttu-id="b756c-132">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b756c-132">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="b756c-133">Neu – AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b756c-133">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="b756c-134">Stopp-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b756c-134">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)

[<span data-ttu-id="b756c-135">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b756c-135">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


