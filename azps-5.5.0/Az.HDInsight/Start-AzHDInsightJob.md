---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/start-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
ms.openlocfilehash: ad2060a399b5781e18c9d8b7fc1c8a37b5d467b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175361"
---
# <span data-ttu-id="99c52-101">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="99c52-101">Start-AzHDInsightJob</span></span>

## <span data-ttu-id="99c52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99c52-102">SYNOPSIS</span></span>
<span data-ttu-id="99c52-103">Startet einen definierten Azure -HDInsight-Auftrag für einen angegebenen Cluster.</span><span class="sxs-lookup"><span data-stu-id="99c52-103">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

## <span data-ttu-id="99c52-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99c52-104">SYNTAX</span></span>

```
Start-AzHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="99c52-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="99c52-105">DESCRIPTION</span></span>
<span data-ttu-id="99c52-106">Das **Cmdlet "Start-AzHDInsightJob"** startet einen definierten Azure -HDInsight-Auftrag in einem angegebenen Cluster.</span><span class="sxs-lookup"><span data-stu-id="99c52-106">The **Start-AzHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="99c52-107">Dies kann ein MapReduce-Auftrag, ein Streaming-MapReduce-Auftrag, eine Struktur oder ein Job im Job sein.</span><span class="sxs-lookup"><span data-stu-id="99c52-107">This can be a MapReduce job, a Streaming MapReduce job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="99c52-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="99c52-108">EXAMPLES</span></span>

### <span data-ttu-id="99c52-109">Beispiel 1: Starten eines Auftrags für den angegebenen Cluster</span><span class="sxs-lookup"><span data-stu-id="99c52-109">Example 1: Start a job on the specified cluster</span></span>
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

<span data-ttu-id="99c52-110">Mit diesem Befehl wird ein Auftrag für den Cluster namens "Ihr-Hadoop-001" gestartet.</span><span class="sxs-lookup"><span data-stu-id="99c52-110">This command starts a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="99c52-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99c52-111">PARAMETERS</span></span>

### <span data-ttu-id="99c52-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="99c52-112">-ClusterName</span></span>
<span data-ttu-id="99c52-113">Gibt den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="99c52-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="99c52-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99c52-114">-DefaultProfile</span></span>
<span data-ttu-id="99c52-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="99c52-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99c52-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="99c52-116">-HttpCredential</span></span>
<span data-ttu-id="99c52-117">Gibt die Anmeldeinformationen für den Cluster (Cluster Login, HTTP) für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="99c52-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="99c52-118">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="99c52-118">-JobDefinition</span></span>
<span data-ttu-id="99c52-119">Gibt die Aufgabe an, die im Azure -HDInsight-Cluster gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="99c52-119">Specifies the job to start on the Azure HDInsight cluster.</span></span>

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

### <span data-ttu-id="99c52-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99c52-120">-ResourceGroupName</span></span>
<span data-ttu-id="99c52-121">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="99c52-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="99c52-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99c52-122">CommonParameters</span></span>
<span data-ttu-id="99c52-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99c52-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99c52-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="99c52-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99c52-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="99c52-125">INPUTS</span></span>

### <span data-ttu-id="99c52-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition</span><span class="sxs-lookup"><span data-stu-id="99c52-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition</span></span>

## <span data-ttu-id="99c52-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="99c52-127">OUTPUTS</span></span>

### <span data-ttu-id="99c52-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="99c52-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="99c52-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="99c52-129">NOTES</span></span>

## <span data-ttu-id="99c52-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="99c52-130">RELATED LINKS</span></span>

[<span data-ttu-id="99c52-131">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="99c52-131">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="99c52-132">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="99c52-132">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="99c52-133">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="99c52-133">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="99c52-134">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="99c52-134">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


