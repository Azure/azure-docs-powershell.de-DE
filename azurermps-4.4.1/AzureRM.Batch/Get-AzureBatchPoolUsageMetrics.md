---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4B373447-3078-4C1F-932E-8337AB170DEB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolUsageMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolUsageMetrics.md
ms.openlocfilehash: 4f985859cb26372a6ffc68b8521d08033fdc6670
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505666"
---
# <span data-ttu-id="442d9-101">Get-AzureBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="442d9-101">Get-AzureBatchPoolUsageMetrics</span></span>

## <span data-ttu-id="442d9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="442d9-102">SYNOPSIS</span></span>
<span data-ttu-id="442d9-103">Ruft Metriken für die Poolnutzung für ein Stapelverarbeitungs Konto ab.</span><span class="sxs-lookup"><span data-stu-id="442d9-103">Gets pool usage metrics for a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="442d9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="442d9-104">SYNTAX</span></span>

```
Get-AzureBatchPoolUsageMetrics [-StartTime <DateTime>] [-EndTime <DateTime>] [-Filter <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="442d9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="442d9-105">DESCRIPTION</span></span>
<span data-ttu-id="442d9-106">Das Cmdlet " **Get-AzureBatchPoolUsageMetrics** " Ruft die Nutzungs Metrik ab, die für das angegebene Konto über einzelne Zeitintervalle aggregiert werden.</span><span class="sxs-lookup"><span data-stu-id="442d9-106">The **Get-AzureBatchPoolUsageMetrics** cmdlet gets the usage metrics, aggregated by pool across individual time intervals, for the specified account.</span></span>
<span data-ttu-id="442d9-107">Sie können die Statistiken für einen bestimmten Pool und einen Zeitbereich abrufen.</span><span class="sxs-lookup"><span data-stu-id="442d9-107">You can get the statistics for a specific pool and for a time range.</span></span>

## <span data-ttu-id="442d9-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="442d9-108">EXAMPLES</span></span>

### <span data-ttu-id="442d9-109">Beispiel 1: Abrufen von Pool Nutzungs Metriken für einen Zeitbereich</span><span class="sxs-lookup"><span data-stu-id="442d9-109">Example 1: Get pool usage metrics for a time range</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $StartTime = Get-Date -Date "2016-05-16 00:00:00Z"
PS C:\> $EndTime = Get-Date -Date "2016-05-16 01:00:00Z"
PS C:\> Get-AzureBatchPoolUsageMetrics -StartTime $StartTime -EndTime $EndTime -BatchContext $context
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

<span data-ttu-id="442d9-110">Der erste Befehl erstellt einen Objektverweis auf die Kontoschlüssel für das Batch Konto mit dem Namen ContosoBatchAccount mithilfe von **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="442d9-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="442d9-111">Der Befehl speichert diesen Objektverweis in der $Context Variablen.</span><span class="sxs-lookup"><span data-stu-id="442d9-111">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="442d9-112">Die nächsten beiden Befehle erstellen **DateTime** -Objekte mithilfe des Get-Date-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="442d9-112">The next two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="442d9-113">Die Befehle speichern diese Werte im $StartTime und $EndTime Variablen, die mit dem letzten Befehl verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="442d9-113">The commands store these values in the $StartTime and $EndTime variables for use with the final command.</span></span>

<span data-ttu-id="442d9-114">Der endgültige Befehl gibt alle vom Pool aggregierten Metriken für die Poolnutzung über das Zeitintervall zwischen den angegebenen Anfangs-und Endzeitpunkten zurück.</span><span class="sxs-lookup"><span data-stu-id="442d9-114">The final command returns all of the pool usage metrics, aggregated by pool, across time interval between the specified start and end times.</span></span>

### <span data-ttu-id="442d9-115">Beispiel 2: Abrufen von Metriken zur Poolnutzung mithilfe eines Filters</span><span class="sxs-lookup"><span data-stu-id="442d9-115">Example 2: Get pool usage metrics by using a filter</span></span>
```
PS C:\>Get-AzureBatchPoolUsageMetrics -Filter "poolId eq 'ContosoPool'" -BatchContext $Context
DataEgressGiB      : 9.0496614575386E-06
DataIngressGiB     : 2.60043889284134E-05
EndTime            : 5/16/2016 5:30:00 PM
PoolId             : MyPool
StartTime          : 5/16/2016 5:00:00 PM
TotalCoreHours     : 12
VirtualMachineSize : standard_d4
```

<span data-ttu-id="442d9-116">Dieser Befehl gibt die Verwendungs Metriken für den Pool mit dem Namen ContosoPool zurück.</span><span class="sxs-lookup"><span data-stu-id="442d9-116">This command returns the usage metrics for pool named ContosoPool.</span></span>
<span data-ttu-id="442d9-117">Der Befehl gibt eine Filterzeichenfolge an, um diesen Pool anzugeben, und verwendet denselben $context Wert wie im vorherigen Beispiel.</span><span class="sxs-lookup"><span data-stu-id="442d9-117">The command specifies a filter string to specify that pool, and uses the same $Context value as the previous example.</span></span>

## <span data-ttu-id="442d9-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="442d9-118">PARAMETERS</span></span>

### <span data-ttu-id="442d9-119">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="442d9-119">-BatchContext</span></span>
<span data-ttu-id="442d9-120">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="442d9-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="442d9-121">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="442d9-121">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="442d9-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="442d9-122">-EndTime</span></span>
<span data-ttu-id="442d9-123">Gibt das Ende eines Zeitbereichs an, für den dieses Cmdlet Nutzungs Metriken erhält.</span><span class="sxs-lookup"><span data-stu-id="442d9-123">Specifies the end of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="442d9-124">Geben Sie mindestens zwei Stunden zuvor eine Uhrzeit an.</span><span class="sxs-lookup"><span data-stu-id="442d9-124">Specify a time at least two hours earlier.</span></span>
<span data-ttu-id="442d9-125">Wenn Sie keine Endzeit angeben, verwendet dieses Cmdlet das letzte Aggregations Intervall, das derzeit verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="442d9-125">If you do not specify an end time, this cmdlet uses the last aggregation interval currently available.</span></span>

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

### <span data-ttu-id="442d9-126">-Filter</span><span class="sxs-lookup"><span data-stu-id="442d9-126">-Filter</span></span>
<span data-ttu-id="442d9-127">Gibt eine OData-Filterklausel an, die zum Filtern der Metriken verwendet werden soll, die dieses Cmdlet retruns.</span><span class="sxs-lookup"><span data-stu-id="442d9-127">Specifies an OData filter clause to use to filter the metrics that this cmdlet retruns.</span></span>
<span data-ttu-id="442d9-128">Die einzige gültige Eigenschaft ist **Pool** -Nr mit einem Zeichenfolgenwert.</span><span class="sxs-lookup"><span data-stu-id="442d9-128">The only valid property is **poolId** with a string value.</span></span>
<span data-ttu-id="442d9-129">Mögliche Vorgänge sind die folgenden: EQ, ge, gt, Le, lt, StartsWith.</span><span class="sxs-lookup"><span data-stu-id="442d9-129">Possible operations are the following: eq, ge, gt, le, lt, startswith.</span></span>

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

### <span data-ttu-id="442d9-130">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="442d9-130">-StartTime</span></span>
<span data-ttu-id="442d9-131">Gibt den Anfang eines Zeitbereichs an, für den dieses Cmdlet Nutzungs Metriken erhält.</span><span class="sxs-lookup"><span data-stu-id="442d9-131">Specifies the start of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="442d9-132">Geben Sie eine Uhrzeit an, die mindestens zweieinhalb Stunden früher ist.</span><span class="sxs-lookup"><span data-stu-id="442d9-132">Specify a time at least two and a half hours earlier.</span></span>
<span data-ttu-id="442d9-133">Wenn Sie keine Startzeit angeben, verwendet dieses Cmdlet das letzte Aggregations Intervall, das derzeit verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="442d9-133">If you do not specify a start time, this cmdlet uses the last aggregation interval currently available.</span></span>

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

### <span data-ttu-id="442d9-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="442d9-134">-DefaultProfile</span></span>
<span data-ttu-id="442d9-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="442d9-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="442d9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="442d9-136">CommonParameters</span></span>
<span data-ttu-id="442d9-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="442d9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="442d9-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="442d9-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="442d9-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="442d9-139">INPUTS</span></span>

### <span data-ttu-id="442d9-140">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="442d9-140">BatchAccountContext</span></span>
<span data-ttu-id="442d9-141">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="442d9-141">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="442d9-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="442d9-142">OUTPUTS</span></span>

### <span data-ttu-id="442d9-143">PSPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="442d9-143">PSPoolUsageMetrics</span></span>

## <span data-ttu-id="442d9-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="442d9-144">NOTES</span></span>

## <span data-ttu-id="442d9-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="442d9-145">RELATED LINKS</span></span>

[<span data-ttu-id="442d9-146">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="442d9-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="442d9-147">Get-AzureBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="442d9-147">Get-AzureBatchPoolStatistics</span></span>](./Get-AzureBatchPoolStatistics.md)

[<span data-ttu-id="442d9-148">Get-AzureBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="442d9-148">Get-AzureBatchJobStatistics</span></span>](./Get-AzureBatchJobStatistics.md)


