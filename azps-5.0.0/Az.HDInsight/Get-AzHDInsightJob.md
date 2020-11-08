---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: AFE90092-8B25-4897-8D3A-3E732CC5CBA6
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJob.md
ms.openlocfilehash: b2ba2144eccd3069453daa1ada15527539400c22
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175575"
---
# <span data-ttu-id="6e859-101">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="6e859-101">Get-AzHDInsightJob</span></span>

## <span data-ttu-id="6e859-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6e859-102">SYNOPSIS</span></span>
<span data-ttu-id="6e859-103">Ruft die Liste der Aufträge aus einem Cluster ab und listet sie in umgekehrter chronologischer Reihenfolge auf oder Ruft einen bestimmten Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="6e859-103">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

## <span data-ttu-id="6e859-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e859-104">SYNTAX</span></span>

```
Get-AzHDInsightJob [-ClusterName] <String> [-HttpCredential] <PSCredential> [[-JobId] <String>]
 [-NumOfJobs <Int32>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6e859-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6e859-105">DESCRIPTION</span></span>
<span data-ttu-id="6e859-106">Das Cmdlet " **Get-AzHDInsightJob** " Ruft aktuelle Aufträge für einen angegebenen Azure HDInsight-Cluster in umgekehrter chronologischer Reihenfolge ab, wobei der letzte Auftrag oben in der Liste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6e859-106">The **Get-AzHDInsightJob** cmdlet gets recent jobs for a specified Azure HDInsight cluster in reverse chronological order, with the most recent job at the top of the list.</span></span>
<span data-ttu-id="6e859-107">Rufen Sie einen bestimmten Job ab, indem Sie den *JobID* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="6e859-107">Get a specific job by providing the *JobId* parameter.</span></span>

## <span data-ttu-id="6e859-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6e859-108">EXAMPLES</span></span>

### <span data-ttu-id="6e859-109">Beispiel 1: Abrufen von letzten Aufträgen für einen angegebenen Azure HDInsight-Cluster</span><span class="sxs-lookup"><span data-stu-id="6e859-109">Example 1: Get recent jobs for a specified Azure HDInsight cluster</span></span>
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

<span data-ttu-id="6e859-110">Dieser Befehl ruft alle letzten Aufträge für den Cluster mit dem Namen "Your-Hadoop-001" ab.</span><span class="sxs-lookup"><span data-stu-id="6e859-110">This command gets all recent jobs for the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="6e859-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e859-111">PARAMETERS</span></span>

### <span data-ttu-id="6e859-112">-Clustername</span><span class="sxs-lookup"><span data-stu-id="6e859-112">-ClusterName</span></span>
<span data-ttu-id="6e859-113">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="6e859-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="6e859-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e859-114">-DefaultProfile</span></span>
<span data-ttu-id="6e859-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6e859-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e859-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="6e859-116">-HttpCredential</span></span>
<span data-ttu-id="6e859-117">Gibt die Anmeldeinformationen für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="6e859-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="6e859-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="6e859-118">-JobId</span></span>
<span data-ttu-id="6e859-119">Gibt die Auftrags-ID des abzurufenden Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="6e859-119">Specifies the job ID of the job to get.</span></span>

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

### <span data-ttu-id="6e859-120">-NumOfJobs</span><span class="sxs-lookup"><span data-stu-id="6e859-120">-NumOfJobs</span></span>
<span data-ttu-id="6e859-121">Gibt die Anzahl von Aufträgen an, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6e859-121">Specifies the number of jobs to retrieve.</span></span>

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

### <span data-ttu-id="6e859-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e859-122">-ResourceGroupName</span></span>
<span data-ttu-id="6e859-123">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="6e859-123">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="6e859-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e859-124">CommonParameters</span></span>
<span data-ttu-id="6e859-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e859-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e859-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e859-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e859-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6e859-127">INPUTS</span></span>

### <span data-ttu-id="6e859-128">Keine</span><span class="sxs-lookup"><span data-stu-id="6e859-128">None</span></span>

## <span data-ttu-id="6e859-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6e859-129">OUTPUTS</span></span>

### <span data-ttu-id="6e859-130">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="6e859-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="6e859-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="6e859-131">NOTES</span></span>

## <span data-ttu-id="6e859-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6e859-132">RELATED LINKS</span></span>

[<span data-ttu-id="6e859-133">Neu – AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="6e859-133">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="6e859-134">Anfang-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="6e859-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="6e859-135">Stopp-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="6e859-135">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="6e859-136">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="6e859-136">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


