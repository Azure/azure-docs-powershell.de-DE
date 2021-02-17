---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B373447-3078-4C1F-932E-8337AB170DEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolusagemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
ms.openlocfilehash: 1700e20318a502f32386638f94a9c5c86c271d7d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171503"
---
# <span data-ttu-id="551e9-101">Get-AzBatchPoolUsageMetric</span><span class="sxs-lookup"><span data-stu-id="551e9-101">Get-AzBatchPoolUsageMetric</span></span>

## <span data-ttu-id="551e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="551e9-102">SYNOPSIS</span></span>
<span data-ttu-id="551e9-103">Ruft Poolnutzungsmetriken für ein Batchkonto ab.</span><span class="sxs-lookup"><span data-stu-id="551e9-103">Gets pool usage metrics for a Batch account.</span></span>

## <span data-ttu-id="551e9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="551e9-104">SYNTAX</span></span>

```
Get-AzBatchPoolUsageMetric [-StartTime <DateTime>] [-EndTime <DateTime>] [-Filter <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="551e9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="551e9-105">DESCRIPTION</span></span>
<span data-ttu-id="551e9-106">Das **Cmdlet "Get-AzBatchPoolUsageMetric"** ruft die nach Pool über einzelne Zeitintervalle zusammengefassten Nutzungsmetriken für das angegebene Konto ab.</span><span class="sxs-lookup"><span data-stu-id="551e9-106">The **Get-AzBatchPoolUsageMetric** cmdlet gets the usage metrics, aggregated by pool across individual time intervals, for the specified account.</span></span>
<span data-ttu-id="551e9-107">Sie können die Statistiken für einen bestimmten Pool und einen Zeitraum erhalten.</span><span class="sxs-lookup"><span data-stu-id="551e9-107">You can get the statistics for a specific pool and for a time range.</span></span>

## <span data-ttu-id="551e9-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="551e9-108">EXAMPLES</span></span>

### <span data-ttu-id="551e9-109">Beispiel 1: Erhalten von Poolnutzungsmetriken für einen Zeitraum</span><span class="sxs-lookup"><span data-stu-id="551e9-109">Example 1: Get pool usage metrics for a time range</span></span>
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

<span data-ttu-id="551e9-110">Der erste Befehl erstellt mithilfe von **"Get-AzBatchAccountKey"** einen Objektverweis auf die Kontoschlüssel für das Batchkonto namens "ContosoBatchAccount".</span><span class="sxs-lookup"><span data-stu-id="551e9-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="551e9-111">Der Befehl speichert diesen Objektverweis in der $Context Variable.</span><span class="sxs-lookup"><span data-stu-id="551e9-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="551e9-112">Die nächsten beiden Befehle erstellen **"DateTime"-Objekte** mithilfe des Get-Date-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="551e9-112">The next two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="551e9-113">Die Befehle speichern diese Werte in den $StartTime und $EndTime für die Verwendung mit dem endgültigen Befehl.</span><span class="sxs-lookup"><span data-stu-id="551e9-113">The commands store these values in the $StartTime and $EndTime variables for use with the final command.</span></span>
<span data-ttu-id="551e9-114">Der letzte Befehl gibt alle Nach Poolnutzungsmetriken aggregiert über das Zeitintervall zwischen der angegebenen Start- und Endzeit zurück.</span><span class="sxs-lookup"><span data-stu-id="551e9-114">The final command returns all of the pool usage metrics, aggregated by pool, across time interval between the specified start and end times.</span></span>

### <span data-ttu-id="551e9-115">Beispiel 2: Erhalten von Poolnutzungsmetriken mithilfe eines Filters</span><span class="sxs-lookup"><span data-stu-id="551e9-115">Example 2: Get pool usage metrics by using a filter</span></span>
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

<span data-ttu-id="551e9-116">Dieser Befehl gibt die Verwendungsmetriken für den Pool "ContosoPool" zurück.</span><span class="sxs-lookup"><span data-stu-id="551e9-116">This command returns the usage metrics for pool named ContosoPool.</span></span>
<span data-ttu-id="551e9-117">Der Befehl gibt eine Filterzeichenfolge an, um diesen Pool anzugeben, und verwendet denselben $Context Wert wie im vorherigen Beispiel.</span><span class="sxs-lookup"><span data-stu-id="551e9-117">The command specifies a filter string to specify that pool, and uses the same $Context value as the previous example.</span></span>

## <span data-ttu-id="551e9-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="551e9-118">PARAMETERS</span></span>

### <span data-ttu-id="551e9-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="551e9-119">-BatchContext</span></span>
<span data-ttu-id="551e9-120">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="551e9-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="551e9-121">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="551e9-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="551e9-122">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="551e9-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="551e9-123">Bei der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="551e9-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="551e9-124">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="551e9-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="551e9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="551e9-125">-DefaultProfile</span></span>
<span data-ttu-id="551e9-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="551e9-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="551e9-127">-EndTime</span><span class="sxs-lookup"><span data-stu-id="551e9-127">-EndTime</span></span>
<span data-ttu-id="551e9-128">Gibt das Ende eines Zeitbereichs an, für den dieses Cmdlet Nutzungsmetriken erhält.</span><span class="sxs-lookup"><span data-stu-id="551e9-128">Specifies the end of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="551e9-129">Geben Sie eine Uhrzeit an, die mindestens zwei Stunden früher war.</span><span class="sxs-lookup"><span data-stu-id="551e9-129">Specify a time at least two hours earlier.</span></span>
<span data-ttu-id="551e9-130">Wenn Sie keine Endzeit angeben, verwendet dieses Cmdlet das zurzeit verfügbare letzte Aggregationsintervall.</span><span class="sxs-lookup"><span data-stu-id="551e9-130">If you do not specify an end time, this cmdlet uses the last aggregation interval currently available.</span></span>

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

### <span data-ttu-id="551e9-131">-Filter</span><span class="sxs-lookup"><span data-stu-id="551e9-131">-Filter</span></span>
<span data-ttu-id="551e9-132">Gibt eine OData-Filterklausel an, die zum Filtern der von diesem Cmdlet zurückgegebenen Metriken verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="551e9-132">Specifies an OData filter clause to use to filter the metrics that this cmdlet returns.</span></span>
<span data-ttu-id="551e9-133">Die einzige gültige Eigenschaft ist **"poolId"** mit einem Zeichenfolgenwert.</span><span class="sxs-lookup"><span data-stu-id="551e9-133">The only valid property is **poolId** with a string value.</span></span>
<span data-ttu-id="551e9-134">Mögliche Vorgänge sind: eq, ge, gt, le, lt, startswith.</span><span class="sxs-lookup"><span data-stu-id="551e9-134">Possible operations are the following: eq, ge, gt, le, lt, startswith.</span></span>

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

### <span data-ttu-id="551e9-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="551e9-135">-StartTime</span></span>
<span data-ttu-id="551e9-136">Gibt den Anfang eines Zeitbereichs an, für den dieses Cmdlet Nutzungsmetriken erhält.</span><span class="sxs-lookup"><span data-stu-id="551e9-136">Specifies the start of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="551e9-137">Geben Sie eine Uhrzeit an, die mindestens zwei,5 Stunden früher war.</span><span class="sxs-lookup"><span data-stu-id="551e9-137">Specify a time at least two and a half hours earlier.</span></span>
<span data-ttu-id="551e9-138">Wenn Sie keine Startzeit angeben, verwendet dieses Cmdlet das zurzeit verfügbare letzte Aggregationsintervall.</span><span class="sxs-lookup"><span data-stu-id="551e9-138">If you do not specify a start time, this cmdlet uses the last aggregation interval currently available.</span></span>

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

### <span data-ttu-id="551e9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="551e9-139">CommonParameters</span></span>
<span data-ttu-id="551e9-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="551e9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="551e9-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="551e9-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="551e9-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="551e9-142">INPUTS</span></span>

### <span data-ttu-id="551e9-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="551e9-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="551e9-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="551e9-144">OUTPUTS</span></span>

### <span data-ttu-id="551e9-145">Microsoft.Azure.Commands.Batch. Models.PSPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="551e9-145">Microsoft.Azure.Commands.Batch.Models.PSPoolUsageMetrics</span></span>

## <span data-ttu-id="551e9-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="551e9-146">NOTES</span></span>

## <span data-ttu-id="551e9-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="551e9-147">RELATED LINKS</span></span>

[<span data-ttu-id="551e9-148">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="551e9-148">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="551e9-149">Get-AzBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="551e9-149">Get-AzBatchPoolStatistics</span></span>](./Get-AzBatchPoolStatistic.md)

[<span data-ttu-id="551e9-150">Get-AzBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="551e9-150">Get-AzBatchJobStatistics</span></span>](./Get-AzBatchJobStatistic.md)
