---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/start-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
ms.openlocfilehash: 6eab5c80fa8c21d5b592f0e194a5aba50c4d3002
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008292"
---
# <span data-ttu-id="52a8c-101">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="52a8c-101">Start-AzHDInsightJob</span></span>

## <span data-ttu-id="52a8c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="52a8c-102">SYNOPSIS</span></span>
<span data-ttu-id="52a8c-103">Startet einen definierten Azure HDInsight-Auftrag in einem angegebenen Cluster.</span><span class="sxs-lookup"><span data-stu-id="52a8c-103">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

## <span data-ttu-id="52a8c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="52a8c-104">SYNTAX</span></span>

```
Start-AzHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="52a8c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="52a8c-105">DESCRIPTION</span></span>
<span data-ttu-id="52a8c-106">Mit dem Cmdlet **Start-AzHDInsightJob** wird ein definierter Azure HDInsight-Auftrag in einem angegebenen Cluster gestartet.</span><span class="sxs-lookup"><span data-stu-id="52a8c-106">The **Start-AzHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="52a8c-107">Dies kann ein MapReduce-Auftrag, ein Streaming-MapReduce-Auftrag, ein Hive-Job oder ein Pig-Job sein.</span><span class="sxs-lookup"><span data-stu-id="52a8c-107">This can be a MapReduce job, a Streaming MapReduce job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="52a8c-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="52a8c-108">EXAMPLES</span></span>

### <span data-ttu-id="52a8c-109">Beispiel 1: Starten eines Auftrags auf dem angegebenen Cluster</span><span class="sxs-lookup"><span data-stu-id="52a8c-109">Example 1: Start a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="52a8c-110">Mit diesem Befehl wird ein Auftrag auf dem Cluster "Your-Hadoop-001" gestartet.</span><span class="sxs-lookup"><span data-stu-id="52a8c-110">This command starts a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="52a8c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="52a8c-111">PARAMETERS</span></span>

### <span data-ttu-id="52a8c-112">-Clustername</span><span class="sxs-lookup"><span data-stu-id="52a8c-112">-ClusterName</span></span>
<span data-ttu-id="52a8c-113">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="52a8c-113">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52a8c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52a8c-114">-DefaultProfile</span></span>
<span data-ttu-id="52a8c-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="52a8c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52a8c-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="52a8c-116">-HttpCredential</span></span>
<span data-ttu-id="52a8c-117">Gibt die Anmeldeinformationen für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="52a8c-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52a8c-118">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="52a8c-118">-JobDefinition</span></span>
<span data-ttu-id="52a8c-119">Gibt den Auftrag an, der im Azure HDInsight-Cluster gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="52a8c-119">Specifies the job to start on the Azure HDInsight cluster.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52a8c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52a8c-120">-ResourceGroupName</span></span>
<span data-ttu-id="52a8c-121">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="52a8c-121">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52a8c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52a8c-122">CommonParameters</span></span>
<span data-ttu-id="52a8c-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52a8c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52a8c-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52a8c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52a8c-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="52a8c-125">INPUTS</span></span>

### <span data-ttu-id="52a8c-126">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJobDefinition</span><span class="sxs-lookup"><span data-stu-id="52a8c-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition</span></span>

## <span data-ttu-id="52a8c-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="52a8c-127">OUTPUTS</span></span>

### <span data-ttu-id="52a8c-128">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="52a8c-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="52a8c-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="52a8c-129">NOTES</span></span>

## <span data-ttu-id="52a8c-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="52a8c-130">RELATED LINKS</span></span>

[<span data-ttu-id="52a8c-131">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="52a8c-131">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="52a8c-132">Neu – AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="52a8c-132">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="52a8c-133">Stopp-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="52a8c-133">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="52a8c-134">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="52a8c-134">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


