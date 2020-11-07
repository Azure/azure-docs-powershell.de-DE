---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Wait-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Wait-AzureRmHDInsightJob.md
ms.openlocfilehash: 6e19594cfcd79c6be82373af6245ea2154296b48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665382"
---
# <span data-ttu-id="35b65-101">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="35b65-101">Wait-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="35b65-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="35b65-102">SYNOPSIS</span></span>
<span data-ttu-id="35b65-103">Wartet auf den Abschluss oder Fehler eines angegebenen Auftrags.</span><span class="sxs-lookup"><span data-stu-id="35b65-103">Waits for the completion or failure of a specified job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35b65-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="35b65-104">SYNTAX</span></span>

```
Wait-AzureRmHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35b65-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="35b65-105">DESCRIPTION</span></span>
<span data-ttu-id="35b65-106">Das Cmdlet **Wait-AzureRmHDInsightJob** wartet auf den Abschluss oder Fehler eines Azure HDInsight-Auftrags.</span><span class="sxs-lookup"><span data-stu-id="35b65-106">The **Wait-AzureRmHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="35b65-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="35b65-107">EXAMPLES</span></span>

### <span data-ttu-id="35b65-108">Beispiel 1: warten auf den Abschluss oder Fehler eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="35b65-108">Example 1: Wait for the completion or failure of a job</span></span>
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

<span data-ttu-id="35b65-109">Dieser Befehl wartet auf den Abschluss oder Fehler eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="35b65-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="35b65-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="35b65-110">PARAMETERS</span></span>

### <span data-ttu-id="35b65-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="35b65-111">-ClusterName</span></span>
<span data-ttu-id="35b65-112">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="35b65-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="35b65-113">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="35b65-113">-HttpCredential</span></span>
<span data-ttu-id="35b65-114">Gibt die Anmeldeinformationen für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="35b65-114">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="35b65-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="35b65-115">-JobId</span></span>
<span data-ttu-id="35b65-116">Gibt die Auftrags-ID des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="35b65-116">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="35b65-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35b65-117">-ResourceGroupName</span></span>
<span data-ttu-id="35b65-118">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="35b65-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="35b65-119">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="35b65-119">-TimeoutInSeconds</span></span>
<span data-ttu-id="35b65-120">Die Gesamtwartezeit für den Abschluss des Auftrags in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="35b65-120">The total time to wait for job completion, in seconds.</span></span>

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

### <span data-ttu-id="35b65-121">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="35b65-121">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="35b65-122">Die Wartezeit zwischen Auftragsstatus Prüfungen in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="35b65-122">The time to wait between job status checks, in seconds.</span></span>

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

### <span data-ttu-id="35b65-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35b65-123">-DefaultProfile</span></span>
<span data-ttu-id="35b65-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="35b65-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35b65-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35b65-125">CommonParameters</span></span>
<span data-ttu-id="35b65-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35b65-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35b65-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35b65-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35b65-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="35b65-128">INPUTS</span></span>

### <span data-ttu-id="35b65-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="35b65-129">String</span></span>
<span data-ttu-id="35b65-130">Der Parameter "JobID" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="35b65-130">Parameter 'JobId' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="35b65-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="35b65-131">OUTPUTS</span></span>

### <span data-ttu-id="35b65-132">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="35b65-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="35b65-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="35b65-133">NOTES</span></span>

## <span data-ttu-id="35b65-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="35b65-134">RELATED LINKS</span></span>

[<span data-ttu-id="35b65-135">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="35b65-135">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="35b65-136">Anfang-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="35b65-136">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="35b65-137">Stopp-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="35b65-137">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)


