---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/wait-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
ms.openlocfilehash: b603be88ffa89f730cfaaa2f67738cdadc2d4d25
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651022"
---
# <span data-ttu-id="10606-101">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="10606-101">Wait-AzHDInsightJob</span></span>

## <span data-ttu-id="10606-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="10606-102">SYNOPSIS</span></span>
<span data-ttu-id="10606-103">Wartet auf den Abschluss oder Fehler eines angegebenen Auftrags.</span><span class="sxs-lookup"><span data-stu-id="10606-103">Waits for the completion or failure of a specified job.</span></span>

## <span data-ttu-id="10606-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="10606-104">SYNTAX</span></span>

```
Wait-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10606-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10606-105">DESCRIPTION</span></span>
<span data-ttu-id="10606-106">Das Cmdlet **Wait-AzHDInsightJob** wartet auf den Abschluss oder Fehler eines Azure HDInsight-Auftrags.</span><span class="sxs-lookup"><span data-stu-id="10606-106">The **Wait-AzHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="10606-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="10606-107">EXAMPLES</span></span>

### <span data-ttu-id="10606-108">Beispiel 1: warten auf den Abschluss oder Fehler eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="10606-108">Example 1: Wait for the completion or failure of a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Wait-AzHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="10606-109">Dieser Befehl wartet auf den Abschluss oder Fehler eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="10606-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="10606-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="10606-110">PARAMETERS</span></span>

### <span data-ttu-id="10606-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="10606-111">-ClusterName</span></span>
<span data-ttu-id="10606-112">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="10606-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="10606-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10606-113">-DefaultProfile</span></span>
<span data-ttu-id="10606-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="10606-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10606-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="10606-115">-HttpCredential</span></span>
<span data-ttu-id="10606-116">Gibt die Anmeldeinformationen für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="10606-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="10606-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="10606-117">-JobId</span></span>
<span data-ttu-id="10606-118">Gibt die Auftrags-ID des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="10606-118">Specifies the job ID of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10606-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10606-119">-ResourceGroupName</span></span>
<span data-ttu-id="10606-120">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="10606-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="10606-121">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="10606-121">-TimeoutInSeconds</span></span>
<span data-ttu-id="10606-122">Die Gesamtwartezeit für den Abschluss des Auftrags in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="10606-122">The total time to wait for job completion, in seconds.</span></span>

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

### <span data-ttu-id="10606-123">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="10606-123">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="10606-124">Die Wartezeit zwischen Auftragsstatus Prüfungen in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="10606-124">The time to wait between job status checks, in seconds.</span></span>

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

### <span data-ttu-id="10606-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10606-125">CommonParameters</span></span>
<span data-ttu-id="10606-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10606-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10606-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10606-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10606-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="10606-128">INPUTS</span></span>

### <span data-ttu-id="10606-129">System. String</span><span class="sxs-lookup"><span data-stu-id="10606-129">System.String</span></span>

## <span data-ttu-id="10606-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="10606-130">OUTPUTS</span></span>

### <span data-ttu-id="10606-131">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="10606-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="10606-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="10606-132">NOTES</span></span>

## <span data-ttu-id="10606-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="10606-133">RELATED LINKS</span></span>

[<span data-ttu-id="10606-134">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="10606-134">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="10606-135">Anfang-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="10606-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="10606-136">Stopp-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="10606-136">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)


