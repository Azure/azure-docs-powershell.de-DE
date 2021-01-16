---
external help file: Microsoft.Azure.PowerShell.Cmdlets.UsageAggregates.dll-Help.xml
Module Name: Az.Billing
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-usageaggregates
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
ms.openlocfilehash: 858966f5fb20f001dc21363875362673884fcc90
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295618"
---
# <span data-ttu-id="ab862-101">Get-UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="ab862-101">Get-UsageAggregates</span></span>

## <span data-ttu-id="ab862-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab862-102">SYNOPSIS</span></span>
<span data-ttu-id="ab862-103">Ruft die gemeldeten Nutzungsdetails für das Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="ab862-103">Gets the reported Azure subscription usage details.</span></span>

## <span data-ttu-id="ab862-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab862-104">SYNTAX</span></span>

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab862-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ab862-105">DESCRIPTION</span></span>
<span data-ttu-id="ab862-106">Das **Cmdlet "Get-UsageAggregates"** ruft nach den folgenden Eigenschaften aggregierte Nutzungsdaten für das Azure-Abonnement ab:</span><span class="sxs-lookup"><span data-stu-id="ab862-106">The **Get-UsageAggregates** cmdlet gets aggregated Azure subscription usage data by the following properties:</span></span> 
- <span data-ttu-id="ab862-107">Start- und Endzeit, zu der die Nutzung gemeldet wurde.</span><span class="sxs-lookup"><span data-stu-id="ab862-107">Start and end times of when the usage was reported.</span></span>
- <span data-ttu-id="ab862-108">Aggregationsgenauigkeit, entweder täglich oder stündlich.</span><span class="sxs-lookup"><span data-stu-id="ab862-108">Aggregation precision, either daily or hourly.</span></span>
- <span data-ttu-id="ab862-109">Detailinformationen auf Instanzenebene für mehrere Instanzen derselben Ressource.</span><span class="sxs-lookup"><span data-stu-id="ab862-109">Instance level detail for multiple instances of the same resource.</span></span>
<span data-ttu-id="ab862-110">Um konsistente Ergebnisse zu erzielen, basieren die zurückgegebenen Daten darauf, wann die Nutzungsdetails von der Azure-Ressource gemeldet wurden.</span><span class="sxs-lookup"><span data-stu-id="ab862-110">For consistent results, the returned data is based on when the usage details were reported by the Azure resource.</span></span>
<span data-ttu-id="ab862-111">Weitere Informationen finden Sie in der Rest-API-Referenz zur Azure-Abrechnung https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) (in der Microsoft Developer Network-Bibliothek).</span><span class="sxs-lookup"><span data-stu-id="ab862-111">For more information, see Azure Billing REST API Referencehttps://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c (https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) in the Microsoft Developer Network library.</span></span>

## <span data-ttu-id="ab862-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ab862-112">EXAMPLES</span></span>

### <span data-ttu-id="ab862-113">Beispiel 1: Abrufen von Abonnementdaten</span><span class="sxs-lookup"><span data-stu-id="ab862-113">Example 1: Retrieve subscription data</span></span>
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

<span data-ttu-id="ab862-114">Mit diesem Befehl werden die gemeldeten Nutzungsdaten für das Abonnement zwischen dem 02.05.2015 und dem 05.05.2015 abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ab862-114">This command retrieves the reported usage data for the subscription between 5/2/2015 and 5/5/2015.</span></span>

## <span data-ttu-id="ab862-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab862-115">PARAMETERS</span></span>

### <span data-ttu-id="ab862-116">-AggregationSfunktionen</span><span class="sxs-lookup"><span data-stu-id="ab862-116">-AggregationGranularity</span></span>
<span data-ttu-id="ab862-117">Gibt die Aggregationsgenauigkeit der Daten an.</span><span class="sxs-lookup"><span data-stu-id="ab862-117">Specifies the aggregation precision of the data.</span></span>
<span data-ttu-id="ab862-118">Gültige Werte sind: Täglich und stündlich.</span><span class="sxs-lookup"><span data-stu-id="ab862-118">Valid values are: Daily and Hourly.</span></span>
<span data-ttu-id="ab862-119">Der Standardwert ist "Täglich".</span><span class="sxs-lookup"><span data-stu-id="ab862-119">The default value is Daily.</span></span>

```yaml
Type: Microsoft.Azure.Commerce.UsageAggregates.Models.AggregationGranularity
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Hourly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab862-120">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="ab862-120">-ContinuationToken</span></span>
<span data-ttu-id="ab862-121">Gibt das Fortsetzungstoken an, das im vorherigen Aufruf aus dem Antworttext abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="ab862-121">Specifies the continuation token that was retrieved from the response body in the previous call.</span></span>
<span data-ttu-id="ab862-122">Bei einem großen Ergebnissatz werden Antworten mithilfe von Fortsetzungstoken paged angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ab862-122">For a large result set, responses are paged by using continuation tokens.</span></span>
<span data-ttu-id="ab862-123">Das Fortsetzungstoken dient als Lesezeichen für den Fortschritt.</span><span class="sxs-lookup"><span data-stu-id="ab862-123">The continuation token serves as a bookmark for progress.</span></span>
<span data-ttu-id="ab862-124">Wenn Sie diesen Parameter nicht angeben, werden die Daten vom Anfang des in *ReportedStartTime* angegebenen Tages oder der angegebenen Stunde abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ab862-124">If you do not specify this parameter, the data is retrieved from the beginning of the day or hour specified in *ReportedStartTime*.</span></span>
<span data-ttu-id="ab862-125">Es wird empfohlen, dass Sie den nächsten Link in der Antwort auf die Seite mit den Daten befolgen.</span><span class="sxs-lookup"><span data-stu-id="ab862-125">We recommend that you follow the next link in the response to page though the data.</span></span>

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

### <span data-ttu-id="ab862-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab862-126">-DefaultProfile</span></span>
<span data-ttu-id="ab862-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab862-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab862-128">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="ab862-128">-ReportedEndTime</span></span>
<span data-ttu-id="ab862-129">Gibt die gemeldete Endzeit für die Aufzeichnung der Ressourcennutzung im Azure-Abrechnungssystem an.</span><span class="sxs-lookup"><span data-stu-id="ab862-129">Specifies the reported end time for when resource usage was recorded in the Azure billing system.</span></span>
<span data-ttu-id="ab862-130">Azure ist ein verteiltes System, das sich über mehrere Rechenzentren auf der ganzen Welt erstreckt. Daher gibt es eine Verzögerung zwischen dem tatsächlichen Verbrauch der Ressource, d. h. der Zeit für die Ressourcennutzung und dem Zeitpunkt, zu dem das Verwendungsereignis das Abrechnungssystem erreicht hat. Dies ist die gemeldete Zeit für die Ressourcennutzung.</span><span class="sxs-lookup"><span data-stu-id="ab862-130">Azure is a distributed system, spanning multiple datacenters around the world, so there is a delay between when the resource was actually consumed, which is the resource usage time, and when the usage event reached the billing system, which is the resource usage reported time.</span></span>
<span data-ttu-id="ab862-131">Um alle Nutzungsereignisse für ein Abonnement zu erhalten, die für einen Zeitraum gemeldet werden, fragen Sie nach der gemeldeten Uhrzeit ab.</span><span class="sxs-lookup"><span data-stu-id="ab862-131">In order to get all usage events for a subscription that are reported for a time period, you query by reported time.</span></span>
<span data-ttu-id="ab862-132">Obwohl Sie nach der gemeldeten Zeit abfragen, aggregiert das Cmdlet die Antwortdaten nach der Ressourcennutzungszeit.</span><span class="sxs-lookup"><span data-stu-id="ab862-132">Even though you query by reported time, the cmdlet aggregates the response data by the resource usage time.</span></span>
<span data-ttu-id="ab862-133">Die Ressourcennutzungsdaten sind das nützliche Pivot zum Analysieren der Daten.</span><span class="sxs-lookup"><span data-stu-id="ab862-133">The resource usage data is the useful pivot for analyzing the data.</span></span>

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

### <span data-ttu-id="ab862-134">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="ab862-134">-ReportedStartTime</span></span>
<span data-ttu-id="ab862-135">Gibt die gemeldete Startzeit für die Aufzeichnung der Ressourcennutzung im Abrechnungssystem von Azure an.</span><span class="sxs-lookup"><span data-stu-id="ab862-135">Specifies the reported start time for when resource usage was recorded in the Azure billing system.</span></span>

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

### <span data-ttu-id="ab862-136">-ShowDetails</span><span class="sxs-lookup"><span data-stu-id="ab862-136">-ShowDetails</span></span>
<span data-ttu-id="ab862-137">Gibt an, ob dieses Cmdlet Details auf Instanzebene mit den Nutzungsdaten zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="ab862-137">Indicates whether this cmdlet returns instance-level details with the usage data.</span></span>
<span data-ttu-id="ab862-138">Der Standardwert ist $True.</span><span class="sxs-lookup"><span data-stu-id="ab862-138">The default value is $True.</span></span>
<span data-ttu-id="ab862-139">Wenn $False, aggregiert der Dienst die Ergebnisse auf serverseitig und gibt daher weniger Aggregatgruppen zurück.</span><span class="sxs-lookup"><span data-stu-id="ab862-139">If $False, the service aggregates the results on the server side, and therefore returns fewer aggregate groups.</span></span>
<span data-ttu-id="ab862-140">Wenn Sie beispielsweise drei Websites ausführen, erhalten Sie standardmäßig drei Positionen für die Nutzung der Website.</span><span class="sxs-lookup"><span data-stu-id="ab862-140">For example, if you are running three websites, by default you will get three line items for website consumption.</span></span>
<span data-ttu-id="ab862-141">Wenn der Wert jedoch $False, werden alle Daten für dieselbe **subscriptionId,** **meterId,** **usageStartTime** und **usageEndTime** in einer einzelnen Position reduziert.</span><span class="sxs-lookup"><span data-stu-id="ab862-141">However, when the value is $False, all the data for the same **subscriptionId**, **meterId**, **usageStartTime**, and **usageEndTime** is collapsed into a single line item.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab862-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab862-142">CommonParameters</span></span>
<span data-ttu-id="ab862-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab862-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab862-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab862-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab862-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ab862-145">INPUTS</span></span>

### <span data-ttu-id="ab862-146">Keine</span><span class="sxs-lookup"><span data-stu-id="ab862-146">None</span></span>

## <span data-ttu-id="ab862-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ab862-147">OUTPUTS</span></span>

### <span data-ttu-id="ab862-148">Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse</span><span class="sxs-lookup"><span data-stu-id="ab862-148">Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse</span></span>

## <span data-ttu-id="ab862-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ab862-149">NOTES</span></span>

## <span data-ttu-id="ab862-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ab862-150">RELATED LINKS</span></span>
