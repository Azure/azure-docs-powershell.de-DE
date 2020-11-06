---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FD27C755-9AAF-42DA-8425-1661C92B6C68
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Stop-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Stop-AzureRmHDInsightJob.md
ms.openlocfilehash: 674c8f1cb5fdf8d8c76da36a7bb6d8df06e29c8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504969"
---
# <span data-ttu-id="2c230-101">Stop-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2c230-101">Stop-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="2c230-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2c230-102">SYNOPSIS</span></span>
<span data-ttu-id="2c230-103">Beendet einen angegebenen ausgeführten Auftrag in einem Cluster.</span><span class="sxs-lookup"><span data-stu-id="2c230-103">Stops a specified running job on a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c230-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c230-104">SYNTAX</span></span>

```
Stop-AzureRmHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c230-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2c230-105">DESCRIPTION</span></span>
<span data-ttu-id="2c230-106">Das Cmdlet **Stop-AzureRmHDInsightJob** beendet einen angegebenen ausgeführten Auftrag in einem Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="2c230-106">The **Stop-AzureRmHDInsightJob** cmdlet stops a specified running job on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="2c230-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2c230-107">EXAMPLES</span></span>

### <span data-ttu-id="2c230-108">Beispiel 1: Beenden eines Auftrags auf dem angegebenen Cluster</span><span class="sxs-lookup"><span data-stu-id="2c230-108">Example 1: Stop a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential
PS C:\> Stop-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
            -JobId $jobId
```

<span data-ttu-id="2c230-109">Mit diesem Befehl wird ein Auftrag auf dem Cluster "Your-Hadoop-001" beendet.</span><span class="sxs-lookup"><span data-stu-id="2c230-109">This command stops a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="2c230-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c230-110">PARAMETERS</span></span>

### <span data-ttu-id="2c230-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="2c230-111">-ClusterName</span></span>
<span data-ttu-id="2c230-112">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="2c230-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="2c230-113">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="2c230-113">-HttpCredential</span></span>
<span data-ttu-id="2c230-114">Gibt die Anmeldeinformationen für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="2c230-114">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="2c230-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="2c230-115">-JobId</span></span>
<span data-ttu-id="2c230-116">Gibt die Auftrags-ID des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="2c230-116">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="2c230-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c230-117">-ResourceGroupName</span></span>
<span data-ttu-id="2c230-118">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2c230-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2c230-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c230-119">-DefaultProfile</span></span>
<span data-ttu-id="2c230-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2c230-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c230-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c230-121">CommonParameters</span></span>
<span data-ttu-id="2c230-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c230-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c230-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c230-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c230-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2c230-124">INPUTS</span></span>

### <span data-ttu-id="2c230-125">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2c230-125">String</span></span>
<span data-ttu-id="2c230-126">Der Parameter "JobID" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="2c230-126">Parameter 'JobId' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="2c230-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2c230-127">OUTPUTS</span></span>

### <span data-ttu-id="2c230-128">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2c230-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="2c230-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="2c230-129">NOTES</span></span>

## <span data-ttu-id="2c230-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2c230-130">RELATED LINKS</span></span>

[<span data-ttu-id="2c230-131">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2c230-131">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="2c230-132">Anfang-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2c230-132">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="2c230-133">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2c230-133">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


