---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleschedulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
ms.openlocfilehash: 4f046344942e244d6bd220034f7cbe85c48681ef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292024"
---
# <span data-ttu-id="4a470-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span><span class="sxs-lookup"><span data-stu-id="4a470-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span></span>

## <span data-ttu-id="4a470-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a470-102">SYNOPSIS</span></span>
<span data-ttu-id="4a470-103">Erstellt eine terminplanbasierte Autoskalen-Bedingung.</span><span class="sxs-lookup"><span data-stu-id="4a470-103">Creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="4a470-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a470-104">SYNTAX</span></span>

```
New-AzHDInsightClusterAutoscaleScheduleCondition -Time <DateTime> -WorkerNodeCount <Int32>
 -Day <AzureHDInsightDaysOfWeek[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a470-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a470-105">DESCRIPTION</span></span>
<span data-ttu-id="4a470-106">Das **Cmdlet "New-AzHDInsightClusterAutoscaleScheduleCondition"** erstellt eine zeitplanbasierte Autoskalierungsbedingung.</span><span class="sxs-lookup"><span data-stu-id="4a470-106">The **New-AzHDInsightClusterAutoscaleScheduleCondition** cmdlet creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="4a470-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4a470-107">EXAMPLES</span></span>

### <span data-ttu-id="4a470-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4a470-108">Example 1</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
```

<span data-ttu-id="4a470-109">Dieser Befehl erstellt eine Bedingung, in der jeden Montag, Mittwoch um 09:00 Uhr, die Automatische Skalierung des Clusters auf 5 Workerknoten ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4a470-109">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

### <span data-ttu-id="4a470-110">Beispiel 2: Aktivieren der zeitplanbasierten Autoskala eines Clusters mit Autoskalen-Bedingung.</span><span class="sxs-lookup"><span data-stu-id="4a470-110">Example 2: Enable Schedule-based autoscale of a cluster with autoscale condition.</span></span>
```powershell
# create a autoscale condition
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday

# Set the cluster autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition
```

<span data-ttu-id="4a470-111">Dieser Befehl erstellt eine Bedingung, in der jeden Montag, Mittwoch um 09:00 Uhr, die Automatische Skalierung des Clusters auf 5 Workerknoten ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4a470-111">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

## <span data-ttu-id="4a470-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a470-112">PARAMETERS</span></span>

### <span data-ttu-id="4a470-113">-Day</span><span class="sxs-lookup"><span data-stu-id="4a470-113">-Day</span></span>
<span data-ttu-id="4a470-114">Ruft die Tage des Zeitplans für die Automatische Skalierung ab oder legt diese Bedingung fest.</span><span class="sxs-lookup"><span data-stu-id="4a470-114">Gets or sets the days of Autoscale schedule condition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightDaysOfWeek[]
Parameter Sets: (All)
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a470-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a470-115">-DefaultProfile</span></span>
<span data-ttu-id="4a470-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a470-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a470-117">-Time</span><span class="sxs-lookup"><span data-stu-id="4a470-117">-Time</span></span>
<span data-ttu-id="4a470-118">Ruft die Zeit der Zeitplanbedingung für die Automatische Skalierung ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="4a470-118">Gets or sets the time of Autoscale schedule condition.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a470-119">-WorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="4a470-119">-WorkerNodeCount</span></span>
<span data-ttu-id="4a470-120">Ruft die Zeitplan-Workernode-Anzahl der Zeitplanbedingung für die Automatische Skalierung ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="4a470-120">Gets or sets the schedule workernode count of Autoscale schedule condition.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a470-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a470-121">CommonParameters</span></span>
<span data-ttu-id="4a470-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a470-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a470-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a470-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a470-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4a470-124">INPUTS</span></span>

### <span data-ttu-id="4a470-125">Keine</span><span class="sxs-lookup"><span data-stu-id="4a470-125">None</span></span>

## <span data-ttu-id="4a470-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4a470-126">OUTPUTS</span></span>

### <span data-ttu-id="4a470-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition</span><span class="sxs-lookup"><span data-stu-id="4a470-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition</span></span>

## <span data-ttu-id="4a470-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4a470-128">NOTES</span></span>

## <span data-ttu-id="4a470-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4a470-129">RELATED LINKS</span></span>

<span data-ttu-id="4a470-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4a470-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
