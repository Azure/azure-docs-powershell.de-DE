---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: AFE90092-8B25-4897-8D3A-3E732CC5CBA6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJob.md
ms.openlocfilehash: 1fb2ee80a6dafb005509265e6012380eebf5abd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496146"
---
# <span data-ttu-id="75617-101">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="75617-101">Get-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="75617-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="75617-102">SYNOPSIS</span></span>
<span data-ttu-id="75617-103">Ruft die Liste der Aufträge aus einem Cluster ab und listet sie in umgekehrter chronologischer Reihenfolge auf oder Ruft einen bestimmten Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="75617-103">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75617-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="75617-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightJob [-ClusterName] <String> [-HttpCredential] <PSCredential> [[-JobId] <String>]
 [-NumOfJobs <Int32>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75617-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75617-105">DESCRIPTION</span></span>
<span data-ttu-id="75617-106">Das Cmdlet " **Get-AzureRmHDInsightJob** " Ruft aktuelle Aufträge für einen angegebenen Azure HDInsight-Cluster in umgekehrter chronologischer Reihenfolge ab, wobei der letzte Auftrag oben in der Liste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="75617-106">The **Get-AzureRmHDInsightJob** cmdlet gets recent jobs for a specified Azure HDInsight cluster in reverse chronological order, with the most recent job at the top of the list.</span></span>
<span data-ttu-id="75617-107">Rufen Sie einen bestimmten Job ab, indem Sie den *JobID* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="75617-107">Get a specific job by providing the *JobId* parameter.</span></span>

## <span data-ttu-id="75617-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75617-108">EXAMPLES</span></span>

### <span data-ttu-id="75617-109">Beispiel 1: Abrufen von letzten Aufträgen für einen angegebenen Azure HDInsight-Cluster</span><span class="sxs-lookup"><span data-stu-id="75617-109">Example 1: Get recent jobs for a specified Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="75617-110">Dieser Befehl ruft alle letzten Aufträge für den Cluster mit dem Namen "Your-Hadoop-001" ab.</span><span class="sxs-lookup"><span data-stu-id="75617-110">This command gets all recent jobs for the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="75617-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="75617-111">PARAMETERS</span></span>

### <span data-ttu-id="75617-112">-Clustername</span><span class="sxs-lookup"><span data-stu-id="75617-112">-ClusterName</span></span>
<span data-ttu-id="75617-113">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="75617-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="75617-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75617-114">-DefaultProfile</span></span>
<span data-ttu-id="75617-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="75617-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75617-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="75617-116">-HttpCredential</span></span>
<span data-ttu-id="75617-117">Gibt die Anmeldeinformationen für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="75617-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="75617-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="75617-118">-JobId</span></span>
<span data-ttu-id="75617-119">Gibt die Auftrags-ID des abzurufenden Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="75617-119">Specifies the job ID of the job to get.</span></span>

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

### <span data-ttu-id="75617-120">-NumOfJobs</span><span class="sxs-lookup"><span data-stu-id="75617-120">-NumOfJobs</span></span>
<span data-ttu-id="75617-121">Gibt die Anzahl von Aufträgen an, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="75617-121">Specifies the number of jobs to retrieve.</span></span>

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

### <span data-ttu-id="75617-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75617-122">-ResourceGroupName</span></span>
<span data-ttu-id="75617-123">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="75617-123">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="75617-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75617-124">CommonParameters</span></span>
<span data-ttu-id="75617-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75617-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75617-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75617-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75617-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="75617-127">INPUTS</span></span>

### <span data-ttu-id="75617-128">Keine</span><span class="sxs-lookup"><span data-stu-id="75617-128">None</span></span>

## <span data-ttu-id="75617-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="75617-129">OUTPUTS</span></span>

### <span data-ttu-id="75617-130">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="75617-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="75617-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="75617-131">NOTES</span></span>

## <span data-ttu-id="75617-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="75617-132">RELATED LINKS</span></span>

[<span data-ttu-id="75617-133">Neu – AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="75617-133">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="75617-134">Anfang-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="75617-134">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="75617-135">Stopp-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="75617-135">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)

[<span data-ttu-id="75617-136">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="75617-136">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


