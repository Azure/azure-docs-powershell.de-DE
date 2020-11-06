---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/wait-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Wait-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Wait-AzureRmHDInsightJob.md
ms.openlocfilehash: de7df9417e617f88c61e75c64dd42f32b83fc66b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497465"
---
# <span data-ttu-id="8e5c0-101">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="8e5c0-101">Wait-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="8e5c0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8e5c0-102">SYNOPSIS</span></span>
<span data-ttu-id="8e5c0-103">Wartet auf den Abschluss oder Fehler eines angegebenen Auftrags.</span><span class="sxs-lookup"><span data-stu-id="8e5c0-103">Waits for the completion or failure of a specified job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e5c0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e5c0-104">SYNTAX</span></span>

```
Wait-AzureRmHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e5c0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e5c0-105">DESCRIPTION</span></span>
<span data-ttu-id="8e5c0-106">Das Cmdlet **Wait-AzureRmHDInsightJob** wartet auf den Abschluss oder Fehler eines Azure HDInsight-Auftrags.</span><span class="sxs-lookup"><span data-stu-id="8e5c0-106">The **Wait-AzureRmHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="8e5c0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8e5c0-107">EXAMPLES</span></span>

### <span data-ttu-id="8e5c0-108">Beispiel 1: warten auf den Abschluss oder Fehler eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="8e5c0-108">Example 1: Wait for the completion or failure of a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Wait-AzureRmHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="8e5c0-109">Dieser Befehl wartet auf den Abschluss oder Fehler eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="8e5c0-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="8e5c0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e5c0-110">PARAMETERS</span></span>

### <span data-ttu-id="8e5c0-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="8e5c0-111">-ClusterName</span></span>
<span data-ttu-id="8e5c0-112">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="8e5c0-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="8e5c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e5c0-113">-DefaultProfile</span></span>
<span data-ttu-id="8e5c0-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8e5c0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e5c0-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="8e5c0-115">-HttpCredential</span></span>
<span data-ttu-id="8e5c0-116">Gibt die Anmeldeinformationen für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="8e5c0-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="8e5c0-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="8e5c0-117">-JobId</span></span>
<span data-ttu-id="8e5c0-118">Gibt die Auftrags-ID des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="8e5c0-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="8e5c0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e5c0-119">-ResourceGroupName</span></span>
<span data-ttu-id="8e5c0-120">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="8e5c0-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="8e5c0-121">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="8e5c0-121">-TimeoutInSeconds</span></span>
<span data-ttu-id="8e5c0-122">Die Gesamtwartezeit für den Abschluss des Auftrags in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="8e5c0-122">The total time to wait for job completion, in seconds.</span></span>

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

### <span data-ttu-id="8e5c0-123">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="8e5c0-123">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="8e5c0-124">Die Wartezeit zwischen Auftragsstatus Prüfungen in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="8e5c0-124">The time to wait between job status checks, in seconds.</span></span>

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

### <span data-ttu-id="8e5c0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e5c0-125">CommonParameters</span></span>
<span data-ttu-id="8e5c0-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e5c0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e5c0-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e5c0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e5c0-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8e5c0-128">INPUTS</span></span>

### <span data-ttu-id="8e5c0-129">System. String</span><span class="sxs-lookup"><span data-stu-id="8e5c0-129">System.String</span></span>
<span data-ttu-id="8e5c0-130">Parameter: JobID (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8e5c0-130">Parameters: JobId (ByValue)</span></span>

## <span data-ttu-id="8e5c0-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8e5c0-131">OUTPUTS</span></span>

### <span data-ttu-id="8e5c0-132">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="8e5c0-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="8e5c0-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="8e5c0-133">NOTES</span></span>

## <span data-ttu-id="8e5c0-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8e5c0-134">RELATED LINKS</span></span>

[<span data-ttu-id="8e5c0-135">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="8e5c0-135">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="8e5c0-136">Anfang-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="8e5c0-136">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="8e5c0-137">Stopp-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="8e5c0-137">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)


