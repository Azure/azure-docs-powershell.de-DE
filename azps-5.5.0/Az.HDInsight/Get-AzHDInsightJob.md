---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: AFE90092-8B25-4897-8D3A-3E732CC5CBA6
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJob.md
ms.openlocfilehash: dc7f69ef29d7e5396ad57346380decc672f83db5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153113"
---
# <span data-ttu-id="597cb-101">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="597cb-101">Get-AzHDInsightJob</span></span>

## <span data-ttu-id="597cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="597cb-102">SYNOPSIS</span></span>
<span data-ttu-id="597cb-103">Ruft die Liste der Aufträge aus einem Cluster ab und listet sie in umgekehrter chronologischer Reihenfolge auf oder ruft einen bestimmten Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="597cb-103">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

## <span data-ttu-id="597cb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="597cb-104">SYNTAX</span></span>

```
Get-AzHDInsightJob [-ClusterName] <String> [-HttpCredential] <PSCredential> [[-JobId] <String>]
 [-NumOfJobs <Int32>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="597cb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="597cb-105">DESCRIPTION</span></span>
<span data-ttu-id="597cb-106">Das **Cmdlet "Get-AzHDInsightJob"** ruft die letzten Aufträge für einen angegebenen Azure -HDInsight-Cluster in umgekehrter chronologischer Reihenfolge ab, mit dem letzten Auftrag ganz oben in der Liste.</span><span class="sxs-lookup"><span data-stu-id="597cb-106">The **Get-AzHDInsightJob** cmdlet gets recent jobs for a specified Azure HDInsight cluster in reverse chronological order, with the most recent job at the top of the list.</span></span>
<span data-ttu-id="597cb-107">Erhalten Sie einen bestimmten Auftrag, indem Sie den *Parameter "JobId"* angeben.</span><span class="sxs-lookup"><span data-stu-id="597cb-107">Get a specific job by providing the *JobId* parameter.</span></span>

## <span data-ttu-id="597cb-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="597cb-108">EXAMPLES</span></span>

### <span data-ttu-id="597cb-109">Beispiel 1: Aktuelle Aufträge für einen bestimmten Azure -HDInsight-Cluster erhalten</span><span class="sxs-lookup"><span data-stu-id="597cb-109">Example 1: Get recent jobs for a specified Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="597cb-110">Dieser Befehl ruft alle zuletzt verwendeten Aufträge für den Cluster namens "Ihr-Hadoop-001" ab.</span><span class="sxs-lookup"><span data-stu-id="597cb-110">This command gets all recent jobs for the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="597cb-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="597cb-111">PARAMETERS</span></span>

### <span data-ttu-id="597cb-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="597cb-112">-ClusterName</span></span>
<span data-ttu-id="597cb-113">Gibt den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="597cb-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="597cb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="597cb-114">-DefaultProfile</span></span>
<span data-ttu-id="597cb-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="597cb-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="597cb-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="597cb-116">-HttpCredential</span></span>
<span data-ttu-id="597cb-117">Gibt die Anmeldeinformationen für den Cluster (Cluster Login, HTTP) für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="597cb-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597cb-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="597cb-118">-JobId</span></span>
<span data-ttu-id="597cb-119">Gibt die Auftrags-ID des zu erhaltenden Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="597cb-119">Specifies the job ID of the job to get.</span></span>

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

### <span data-ttu-id="597cb-120">-NumOfJobs</span><span class="sxs-lookup"><span data-stu-id="597cb-120">-NumOfJobs</span></span>
<span data-ttu-id="597cb-121">Gibt die Anzahl der abzurufenden Aufträge an.</span><span class="sxs-lookup"><span data-stu-id="597cb-121">Specifies the number of jobs to retrieve.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597cb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="597cb-122">-ResourceGroupName</span></span>
<span data-ttu-id="597cb-123">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="597cb-123">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="597cb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="597cb-124">CommonParameters</span></span>
<span data-ttu-id="597cb-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="597cb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="597cb-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="597cb-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="597cb-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="597cb-127">INPUTS</span></span>

### <span data-ttu-id="597cb-128">Keine</span><span class="sxs-lookup"><span data-stu-id="597cb-128">None</span></span>

## <span data-ttu-id="597cb-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="597cb-129">OUTPUTS</span></span>

### <span data-ttu-id="597cb-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="597cb-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="597cb-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="597cb-131">NOTES</span></span>

## <span data-ttu-id="597cb-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="597cb-132">RELATED LINKS</span></span>

[<span data-ttu-id="597cb-133">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="597cb-133">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="597cb-134">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="597cb-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="597cb-135">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="597cb-135">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="597cb-136">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="597cb-136">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


