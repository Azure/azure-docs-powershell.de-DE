---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: bfc14e0fba2b384766495dde9e3ef11fafd4653c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947136"
---
# <span data-ttu-id="e8a52-101">New-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="e8a52-101">New-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="e8a52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8a52-102">SYNOPSIS</span></span>
<span data-ttu-id="e8a52-103">Erstellt ein nicht persistiertes Objekt, das die Konfiguration der automatischen Skalierung eines Azure HDInsight-Clusters beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e8a52-103">Creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="e8a52-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e8a52-104">SYNTAX</span></span>

### <span data-ttu-id="e8a52-105">LoadAutoscaleParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e8a52-105">LoadAutoscaleParameterSet (Default)</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount <Int32> -MaxWorkerNodeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8a52-106">ScheduleAutoscaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8a52-106">ScheduleAutoscaleParameterSet</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -TimeZone <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8a52-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e8a52-107">DESCRIPTION</span></span>
<span data-ttu-id="e8a52-108">Das Cmdlet **New-AzHDInsightClusterAutoscaleConfiguration** erstellt ein nicht persistiertes Objekt, das die Konfiguration der automatischen Skalierung eines Azure HDInsight-Clusters beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e8a52-108">The cmdlet **New-AzHDInsightClusterAutoscaleConfiguration** creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="e8a52-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e8a52-109">EXAMPLES</span></span>

### <span data-ttu-id="e8a52-110">Beispiel 1: Erstellen eines Objekts, das die Konfiguration der ladebasierten automatischen Skalierung beschreibt</span><span class="sxs-lookup"><span data-stu-id="e8a52-110">Example 1: Create an object which describes Load-based autoscale configuration</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5
```

<span data-ttu-id="e8a52-111">Mit diesem Befehl wird ein -Objekt erstellt, das die Konfiguration der ladebasierten automatischen Skalierung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e8a52-111">This command creates an object which describes Load-based autoscale configuration.</span></span>

### <span data-ttu-id="e8a52-112">Beispiel 2: Erstellen eines Objekts, das die Konfiguration der zeitplanbasierten automatischen Skalierung beschreibt</span><span class="sxs-lookup"><span data-stu-id="e8a52-112">Example 2: Create an object which describes Schedule-based autoscale configuration</span></span>
```powershell
# Create an autoscale condition firstly
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Day Monday -Time 09:00 -WorkerNodeCount 5
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -TimeZone ([System.TimeZoneInfo]::Local).Id `
        -Condition $condition
```

<span data-ttu-id="e8a52-113">Mit diesem Befehl wird ein -Objekt erstellt, das die zeitplanbasierte Konfiguration der automatischen Skalierung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e8a52-113">This command creates an object which describes Schedule-based autoscale configuration.</span></span>

## <span data-ttu-id="e8a52-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e8a52-114">PARAMETERS</span></span>

### <span data-ttu-id="e8a52-115">-Bedingung</span><span class="sxs-lookup"><span data-stu-id="e8a52-115">-Condition</span></span>
<span data-ttu-id="e8a52-116">Ruft die Bedingung der zeitplanbasierten automatischen Skalierung ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="e8a52-116">Gets or sets the condition of schedule-based autoscale.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]
Parameter Sets: ScheduleAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8a52-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8a52-117">-DefaultProfile</span></span>
<span data-ttu-id="e8a52-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e8a52-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8a52-119">-MaxWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="e8a52-119">-MaxWorkerNodeCount</span></span>
<span data-ttu-id="e8a52-120">Ruft die maximale Workernodeanzahl der ladebasierten automatischen Skalierung ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="e8a52-120">Gets or sets the maximal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8a52-121">-MinWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="e8a52-121">-MinWorkerNodeCount</span></span>
<span data-ttu-id="e8a52-122">Ruft die minimale Workernodeanzahl der ladebasierten automatischen Skalierung ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="e8a52-122">Gets or sets the minimal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8a52-123">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="e8a52-123">-TimeZone</span></span>
<span data-ttu-id="e8a52-124">Ruft die Zeitzone der zeitplanbasierten automatischen Skalierung ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="e8a52-124">Gets or sets the time zone of schedule-based autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduleAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8a52-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8a52-125">CommonParameters</span></span>
<span data-ttu-id="e8a52-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8a52-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8a52-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8a52-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8a52-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e8a52-128">INPUTS</span></span>

### <span data-ttu-id="e8a52-129">Keine</span><span class="sxs-lookup"><span data-stu-id="e8a52-129">None</span></span>

## <span data-ttu-id="e8a52-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e8a52-130">OUTPUTS</span></span>

### <span data-ttu-id="e8a52-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="e8a52-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="e8a52-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e8a52-132">NOTES</span></span>

## <span data-ttu-id="e8a52-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e8a52-133">RELATED LINKS</span></span>

<span data-ttu-id="e8a52-134">[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e8a52-134">[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
