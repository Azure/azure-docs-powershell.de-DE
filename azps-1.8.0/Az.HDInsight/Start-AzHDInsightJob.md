---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/start-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
ms.openlocfilehash: 54fb8305b14272fb34b6329cf057372da7c42a88
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819852"
---
# <span data-ttu-id="11078-101">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="11078-101">Start-AzHDInsightJob</span></span>

## <span data-ttu-id="11078-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="11078-102">SYNOPSIS</span></span>
<span data-ttu-id="11078-103">Startet einen definierten Azure HDInsight-Auftrag in einem angegebenen Cluster.</span><span class="sxs-lookup"><span data-stu-id="11078-103">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

## <span data-ttu-id="11078-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="11078-104">SYNTAX</span></span>

```
Start-AzHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="11078-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="11078-105">DESCRIPTION</span></span>
<span data-ttu-id="11078-106">Mit dem Cmdlet **Start-AzHDInsightJob** wird ein definierter Azure HDInsight-Auftrag in einem angegebenen Cluster gestartet.</span><span class="sxs-lookup"><span data-stu-id="11078-106">The **Start-AzHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="11078-107">Dies kann ein MapReduce-Auftrag, ein Streaming-MapReduce-Auftrag, ein Hive-Job oder ein Pig-Job sein.</span><span class="sxs-lookup"><span data-stu-id="11078-107">This can be a MapReduce job, a Streaming MapReduce job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="11078-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="11078-108">EXAMPLES</span></span>

### <span data-ttu-id="11078-109">Beispiel 1: Starten eines Auftrags auf dem angegebenen Cluster</span><span class="sxs-lookup"><span data-stu-id="11078-109">Example 1: Start a job on the specified cluster</span></span>
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

<span data-ttu-id="11078-110">Mit diesem Befehl wird ein Auftrag auf dem Cluster "Your-Hadoop-001" gestartet.</span><span class="sxs-lookup"><span data-stu-id="11078-110">This command starts a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="11078-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="11078-111">PARAMETERS</span></span>

### <span data-ttu-id="11078-112">-Clustername</span><span class="sxs-lookup"><span data-stu-id="11078-112">-ClusterName</span></span>
<span data-ttu-id="11078-113">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="11078-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="11078-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11078-114">-DefaultProfile</span></span>
<span data-ttu-id="11078-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="11078-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11078-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="11078-116">-HttpCredential</span></span>
<span data-ttu-id="11078-117">Gibt die Anmeldeinformationen für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="11078-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="11078-118">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="11078-118">-JobDefinition</span></span>
<span data-ttu-id="11078-119">Gibt den Auftrag an, der im Azure HDInsight-Cluster gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="11078-119">Specifies the job to start on the Azure HDInsight cluster.</span></span>

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

### <span data-ttu-id="11078-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11078-120">-ResourceGroupName</span></span>
<span data-ttu-id="11078-121">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="11078-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="11078-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11078-122">CommonParameters</span></span>
<span data-ttu-id="11078-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11078-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11078-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11078-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11078-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="11078-125">INPUTS</span></span>

### <span data-ttu-id="11078-126">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJobDefinition</span><span class="sxs-lookup"><span data-stu-id="11078-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition</span></span>

## <span data-ttu-id="11078-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="11078-127">OUTPUTS</span></span>

### <span data-ttu-id="11078-128">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="11078-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="11078-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="11078-129">NOTES</span></span>

## <span data-ttu-id="11078-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="11078-130">RELATED LINKS</span></span>

[<span data-ttu-id="11078-131">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="11078-131">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="11078-132">Neu – AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="11078-132">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="11078-133">Stopp-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="11078-133">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="11078-134">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="11078-134">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


