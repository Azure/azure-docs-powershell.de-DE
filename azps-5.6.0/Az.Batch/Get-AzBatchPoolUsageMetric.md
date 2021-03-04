---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B373447-3078-4C1F-932E-8337AB170DEB
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchpoolusagemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
ms.openlocfilehash: 7d23774085bb467ca091aa500cf67ee43fa2aa46
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933240"
---
# <span data-ttu-id="af077-101">Get-AzBatchPoolUsageMetric</span><span class="sxs-lookup"><span data-stu-id="af077-101">Get-AzBatchPoolUsageMetric</span></span>

## <span data-ttu-id="af077-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af077-102">SYNOPSIS</span></span>
<span data-ttu-id="af077-103">Ruft Poolnutzungsmetriken für ein Batchkonto ab.</span><span class="sxs-lookup"><span data-stu-id="af077-103">Gets pool usage metrics for a Batch account.</span></span>

## <span data-ttu-id="af077-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af077-104">SYNTAX</span></span>

```
Get-AzBatchPoolUsageMetric [-StartTime <DateTime>] [-EndTime <DateTime>] [-Filter <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af077-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="af077-105">DESCRIPTION</span></span>
<span data-ttu-id="af077-106">Das **Get-AzBatchPoolUsageMetric-Cmdlet** ruft die Nach Pool aggregierten Nutzungsmetriken für das angegebene Konto über einzelne Zeitintervalle ab.</span><span class="sxs-lookup"><span data-stu-id="af077-106">The **Get-AzBatchPoolUsageMetric** cmdlet gets the usage metrics, aggregated by pool across individual time intervals, for the specified account.</span></span>
<span data-ttu-id="af077-107">Sie können die Statistiken für einen bestimmten Pool und einen Zeitraum erhalten.</span><span class="sxs-lookup"><span data-stu-id="af077-107">You can get the statistics for a specific pool and for a time range.</span></span>

## <span data-ttu-id="af077-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="af077-108">EXAMPLES</span></span>

### <span data-ttu-id="af077-109">Beispiel 1: Get pool usage metrics for a time range</span><span class="sxs-lookup"><span data-stu-id="af077-109">Example 1: Get pool usage metrics for a time range</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $StartTime = Get-Date -Date "2016-05-16 00:00:00Z"
PS C:\> $EndTime = Get-Date -Date "2016-05-16 01:00:00Z"
PS C:\> Get-AzBatchPoolUsageMetric -StartTime $StartTime -EndTime $EndTime -BatchContext $context
DataEgressGiB      : 6.68875873088837E-06
DataIngressGiB     : 1.9485130906105E-05
EndTime            : 5/16/2016 12:30:00 AM
PoolId             : testpool1
StartTime          : 5/16/2016 12:00:00 AM
TotalCoreHours     : 8
VirtualMachineSize : standard_d4

DataEgressGiB      : 5.61587512493134E-06
DataIngressGiB     : 1.76150351762772E-05
EndTime            : 5/16/2016 12:30:00 AM
PoolId             : testpool2
StartTime          : 5/16/2016 12:00:00 AM
TotalCoreHours     : 12
VirtualMachineSize : standard_d4

DataEgressGiB      : 7.36676156520844E-06
DataIngressGiB     : 2.10804864764214E-05
EndTime            : 5/16/2016 1:00:00 AM
PoolId             : testpool1
StartTime          : 5/16/2016 12:30:00 AM
TotalCoreHours     : 7.99999999955555
VirtualMachineSize : standard_d4

DataEgressGiB      : 5.80586493015289E-06
DataIngressGiB     : 1.80602073669434E-05
EndTime            : 5/16/2016 1:00:00 AM
PoolId             : testpool2
StartTime          : 5/16/2016 12:30:00 AM
TotalCoreHours     : 11.9999999993333
VirtualMachineSize : standard_d4
```

<span data-ttu-id="af077-110">Mit dem ersten Befehl wird mithilfe von **Get-AzBatchAccountKey** ein Objektverweis auf die Kontoschlüssel für das Batchkonto namens ContosoBatchAccount erstellt.</span><span class="sxs-lookup"><span data-stu-id="af077-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="af077-111">Der Befehl speichert diesen Objektverweis in der $Context-Variable.</span><span class="sxs-lookup"><span data-stu-id="af077-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="af077-112">Mit den nächsten beiden Befehlen werden **DateTime-Objekte** mithilfe des Get-Date erstellt.</span><span class="sxs-lookup"><span data-stu-id="af077-112">The next two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="af077-113">Die Befehle speichern diese Werte in den $StartTime und $EndTime für die Verwendung mit dem endgültigen Befehl.</span><span class="sxs-lookup"><span data-stu-id="af077-113">The commands store these values in the $StartTime and $EndTime variables for use with the final command.</span></span>
<span data-ttu-id="af077-114">Der letzte Befehl gibt alle Nach Pool zusammengefassten Poolnutzungsmetriken über das Zeitintervall zwischen den angegebenen Start- und Endzeiten zurück.</span><span class="sxs-lookup"><span data-stu-id="af077-114">The final command returns all of the pool usage metrics, aggregated by pool, across time interval between the specified start and end times.</span></span>

### <span data-ttu-id="af077-115">Beispiel 2: Erfassen von Poolnutzungsmetriken mithilfe eines Filters</span><span class="sxs-lookup"><span data-stu-id="af077-115">Example 2: Get pool usage metrics by using a filter</span></span>
```
PS C:\>Get-AzBatchPoolUsageMetric -Filter "poolId eq 'ContosoPool'" -BatchContext $Context
DataEgressGiB      : 9.0496614575386E-06
DataIngressGiB     : 2.60043889284134E-05
EndTime            : 5/16/2016 5:30:00 PM
PoolId             : MyPool
StartTime          : 5/16/2016 5:00:00 PM
TotalCoreHours     : 12
VirtualMachineSize : standard_d4
```

<span data-ttu-id="af077-116">Dieser Befehl gibt die Verwendungsmetriken für den Pool mit dem Namen ContosoPool zurück.</span><span class="sxs-lookup"><span data-stu-id="af077-116">This command returns the usage metrics for pool named ContosoPool.</span></span>
<span data-ttu-id="af077-117">Der Befehl gibt eine Filterzeichenfolge an, um diesen Pool anzugeben, und verwendet den $Context wert wie im vorherigen Beispiel.</span><span class="sxs-lookup"><span data-stu-id="af077-117">The command specifies a filter string to specify that pool, and uses the same $Context value as the previous example.</span></span>

## <span data-ttu-id="af077-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="af077-118">PARAMETERS</span></span>

### <span data-ttu-id="af077-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="af077-119">-BatchContext</span></span>
<span data-ttu-id="af077-120">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="af077-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="af077-121">Wenn Sie das Get-AzBatchAccount verwenden, um Ihren BatchAccountContext zu erhalten, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="af077-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="af077-122">Wenn Sie stattdessen die Authentifizierung für freigegebene Schlüssel verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="af077-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="af077-123">Bei Verwendung der Authentifizierung mit gemeinsam genutzten Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="af077-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="af077-124">Um den zu verwendende Schlüssel zu ändern, legen Sie die BatchAccountContext.KeyInUse-Eigenschaft ein.</span><span class="sxs-lookup"><span data-stu-id="af077-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af077-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af077-125">-DefaultProfile</span></span>
<span data-ttu-id="af077-126">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="af077-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af077-127">-EndTime</span><span class="sxs-lookup"><span data-stu-id="af077-127">-EndTime</span></span>
<span data-ttu-id="af077-128">Gibt das Ende eines Zeitbereichs an, für den dieses Cmdlet Nutzungsmetriken erhält.</span><span class="sxs-lookup"><span data-stu-id="af077-128">Specifies the end of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="af077-129">Geben Sie eine Uhrzeit mindestens zwei Stunden früher an.</span><span class="sxs-lookup"><span data-stu-id="af077-129">Specify a time at least two hours earlier.</span></span>
<span data-ttu-id="af077-130">Wenn Sie keine Endzeit angeben, verwendet dieses Cmdlet das letzte aktuell verfügbare Aggregationsintervall.</span><span class="sxs-lookup"><span data-stu-id="af077-130">If you do not specify an end time, this cmdlet uses the last aggregation interval currently available.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af077-131">-Filter</span><span class="sxs-lookup"><span data-stu-id="af077-131">-Filter</span></span>
<span data-ttu-id="af077-132">Gibt eine OData-Filterklausel an, mit der die von diesem Cmdlet zurückgegebenen Metriken gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="af077-132">Specifies an OData filter clause to use to filter the metrics that this cmdlet returns.</span></span>
<span data-ttu-id="af077-133">Die einzige gültige Eigenschaft ist **poolId** mit einem Zeichenfolgenwert.</span><span class="sxs-lookup"><span data-stu-id="af077-133">The only valid property is **poolId** with a string value.</span></span>
<span data-ttu-id="af077-134">Mögliche Vorgänge sind die folgenden: eq, ge, gt, le, lt, startswith.</span><span class="sxs-lookup"><span data-stu-id="af077-134">Possible operations are the following: eq, ge, gt, le, lt, startswith.</span></span>

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

### <span data-ttu-id="af077-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="af077-135">-StartTime</span></span>
<span data-ttu-id="af077-136">Gibt den Anfang eines Zeitbereichs an, für den dieses Cmdlet Nutzungsmetriken erhält.</span><span class="sxs-lookup"><span data-stu-id="af077-136">Specifies the start of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="af077-137">Geben Sie eine Zeit von mindestens zweieinhalb Stunden früher an.</span><span class="sxs-lookup"><span data-stu-id="af077-137">Specify a time at least two and a half hours earlier.</span></span>
<span data-ttu-id="af077-138">Wenn Sie keine Startzeit angeben, verwendet dieses Cmdlet das letzte aktuell verfügbare Aggregationsintervall.</span><span class="sxs-lookup"><span data-stu-id="af077-138">If you do not specify a start time, this cmdlet uses the last aggregation interval currently available.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af077-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af077-139">CommonParameters</span></span>
<span data-ttu-id="af077-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af077-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af077-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af077-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af077-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="af077-142">INPUTS</span></span>

### <span data-ttu-id="af077-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="af077-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="af077-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="af077-144">OUTPUTS</span></span>

### <span data-ttu-id="af077-145">Microsoft.Azure.Commands.Batch. Models.PSPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="af077-145">Microsoft.Azure.Commands.Batch.Models.PSPoolUsageMetrics</span></span>

## <span data-ttu-id="af077-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="af077-146">NOTES</span></span>

## <span data-ttu-id="af077-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="af077-147">RELATED LINKS</span></span>

[<span data-ttu-id="af077-148">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="af077-148">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="af077-149">Get-AzBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="af077-149">Get-AzBatchPoolStatistics</span></span>](./Get-AzBatchPoolStatistic.md)

[<span data-ttu-id="af077-150">Get-AzBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="af077-150">Get-AzBatchJobStatistics</span></span>](./Get-AzBatchJobStatistic.md)
