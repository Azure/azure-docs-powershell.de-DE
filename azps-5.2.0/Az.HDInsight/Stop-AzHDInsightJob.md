---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FD27C755-9AAF-42DA-8425-1661C92B6C68
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/stop-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Stop-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Stop-AzHDInsightJob.md
ms.openlocfilehash: d5e38cf3edb89801b630735dee1ce0dbd1d62d41
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98289654"
---
# <span data-ttu-id="5680e-101">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="5680e-101">Stop-AzHDInsightJob</span></span>

## <span data-ttu-id="5680e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5680e-102">SYNOPSIS</span></span>
<span data-ttu-id="5680e-103">Beendet einen angegebenen ausgeführten Auftrag für einen Cluster.</span><span class="sxs-lookup"><span data-stu-id="5680e-103">Stops a specified running job on a cluster.</span></span>

## <span data-ttu-id="5680e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5680e-104">SYNTAX</span></span>

```
Stop-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5680e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5680e-105">DESCRIPTION</span></span>
<span data-ttu-id="5680e-106">Das **Cmdlet "Stop-AzHDInsightJob"** beendet einen angegebenen laufenden Auftrag in einem Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="5680e-106">The **Stop-AzHDInsightJob** cmdlet stops a specified running job on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="5680e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5680e-107">EXAMPLES</span></span>

### <span data-ttu-id="5680e-108">Beispiel 1: Beenden eines Auftrags für den angegebenen Cluster</span><span class="sxs-lookup"><span data-stu-id="5680e-108">Example 1: Stop a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential
PS C:\> Stop-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
            -JobId $jobId
```

<span data-ttu-id="5680e-109">Mit diesem Befehl wird ein Auftrag für den Cluster namens "Ihr-Hadoop-001" beendet.</span><span class="sxs-lookup"><span data-stu-id="5680e-109">This command stops a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="5680e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5680e-110">PARAMETERS</span></span>

### <span data-ttu-id="5680e-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5680e-111">-ClusterName</span></span>
<span data-ttu-id="5680e-112">Gibt den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="5680e-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="5680e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5680e-113">-DefaultProfile</span></span>
<span data-ttu-id="5680e-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="5680e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5680e-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="5680e-115">-HttpCredential</span></span>
<span data-ttu-id="5680e-116">Gibt die Anmeldeinformationen für den Cluster (Cluster Login, HTTP) für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="5680e-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="5680e-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="5680e-117">-JobId</span></span>
<span data-ttu-id="5680e-118">Gibt die Auftrags-ID des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="5680e-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="5680e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5680e-119">-ResourceGroupName</span></span>
<span data-ttu-id="5680e-120">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="5680e-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5680e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5680e-121">CommonParameters</span></span>
<span data-ttu-id="5680e-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5680e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5680e-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5680e-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5680e-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5680e-124">INPUTS</span></span>

### <span data-ttu-id="5680e-125">System.String</span><span class="sxs-lookup"><span data-stu-id="5680e-125">System.String</span></span>

## <span data-ttu-id="5680e-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5680e-126">OUTPUTS</span></span>

### <span data-ttu-id="5680e-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="5680e-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="5680e-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5680e-128">NOTES</span></span>

## <span data-ttu-id="5680e-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5680e-129">RELATED LINKS</span></span>

[<span data-ttu-id="5680e-130">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="5680e-130">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="5680e-131">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="5680e-131">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="5680e-132">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="5680e-132">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


