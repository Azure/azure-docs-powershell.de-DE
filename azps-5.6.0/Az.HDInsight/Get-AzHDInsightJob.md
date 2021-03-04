---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: AFE90092-8B25-4897-8D3A-3E732CC5CBA6
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJob.md
ms.openlocfilehash: 87a5b306619bd3d16b9a7c4e76256f2d0e74d568
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942768"
---
# <span data-ttu-id="f7504-101">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f7504-101">Get-AzHDInsightJob</span></span>

## <span data-ttu-id="f7504-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7504-102">SYNOPSIS</span></span>
<span data-ttu-id="f7504-103">Ruft die Liste der Aufträge aus einem Cluster ab und listet sie in umgekehrter chronologischer Reihenfolge auf oder ruft einen bestimmten Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="f7504-103">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

## <span data-ttu-id="f7504-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7504-104">SYNTAX</span></span>

```
Get-AzHDInsightJob [-ClusterName] <String> [-HttpCredential] <PSCredential> [[-JobId] <String>]
 [-NumOfJobs <Int32>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7504-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f7504-105">DESCRIPTION</span></span>
<span data-ttu-id="f7504-106">Das **Get-AzHDInsightJob-Cmdlet** ruft die letzten Aufträge für einen angegebenen Azure HDInsight-Cluster in umgekehrter chronologischer Reihenfolge ab, mit dem neuesten Auftrag ganz oben in der Liste.</span><span class="sxs-lookup"><span data-stu-id="f7504-106">The **Get-AzHDInsightJob** cmdlet gets recent jobs for a specified Azure HDInsight cluster in reverse chronological order, with the most recent job at the top of the list.</span></span>
<span data-ttu-id="f7504-107">Erhalten Sie einen bestimmten Auftrag, indem Sie den *Parameter "JobId"* angeben.</span><span class="sxs-lookup"><span data-stu-id="f7504-107">Get a specific job by providing the *JobId* parameter.</span></span>

## <span data-ttu-id="f7504-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f7504-108">EXAMPLES</span></span>

### <span data-ttu-id="f7504-109">Beispiel 1: Herunterladen der letzten Aufträge für einen angegebenen Azure HDInsight-Cluster</span><span class="sxs-lookup"><span data-stu-id="f7504-109">Example 1: Get recent jobs for a specified Azure HDInsight cluster</span></span>
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

<span data-ttu-id="f7504-110">Dieser Befehl ruft alle aktuellen Aufträge für den Cluster mit dem Namen "your-hadoop-001" ab.</span><span class="sxs-lookup"><span data-stu-id="f7504-110">This command gets all recent jobs for the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="f7504-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f7504-111">PARAMETERS</span></span>

### <span data-ttu-id="f7504-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f7504-112">-ClusterName</span></span>
<span data-ttu-id="f7504-113">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="f7504-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="f7504-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7504-114">-DefaultProfile</span></span>
<span data-ttu-id="f7504-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f7504-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7504-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="f7504-116">-HttpCredential</span></span>
<span data-ttu-id="f7504-117">Gibt die Anmeldeinformationen für den Cluster (Cluster Login, HTTP) für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="f7504-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="f7504-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="f7504-118">-JobId</span></span>
<span data-ttu-id="f7504-119">Gibt die Auftrags-ID des zu erhaltenden Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="f7504-119">Specifies the job ID of the job to get.</span></span>

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

### <span data-ttu-id="f7504-120">-NumOfJobs</span><span class="sxs-lookup"><span data-stu-id="f7504-120">-NumOfJobs</span></span>
<span data-ttu-id="f7504-121">Gibt die Anzahl der abzurufenden Aufträge an.</span><span class="sxs-lookup"><span data-stu-id="f7504-121">Specifies the number of jobs to retrieve.</span></span>

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

### <span data-ttu-id="f7504-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7504-122">-ResourceGroupName</span></span>
<span data-ttu-id="f7504-123">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="f7504-123">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f7504-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7504-124">CommonParameters</span></span>
<span data-ttu-id="f7504-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7504-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7504-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7504-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7504-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f7504-127">INPUTS</span></span>

### <span data-ttu-id="f7504-128">Keine</span><span class="sxs-lookup"><span data-stu-id="f7504-128">None</span></span>

## <span data-ttu-id="f7504-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f7504-129">OUTPUTS</span></span>

### <span data-ttu-id="f7504-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f7504-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="f7504-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f7504-131">NOTES</span></span>

## <span data-ttu-id="f7504-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f7504-132">RELATED LINKS</span></span>

[<span data-ttu-id="f7504-133">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f7504-133">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="f7504-134">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f7504-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="f7504-135">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f7504-135">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="f7504-136">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f7504-136">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


