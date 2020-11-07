---
external help file: Microsoft.Azure.Commands.UsageAggregates.dll-Help.xml
Module Name: AzureRM
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.usageaggregates/get-usageaggregates
schema: 2.0.0
ms.openlocfilehash: 70dda4d40f517d3d7bd7a3a8d64584e74f80310a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848636"
---
# <span data-ttu-id="12771-101">Get-UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="12771-101">Get-UsageAggregates</span></span>

## <span data-ttu-id="12771-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="12771-102">SYNOPSIS</span></span>
<span data-ttu-id="12771-103">Ruft die gemeldeten Azure-Abonnement Nutzungsdetails ab.</span><span class="sxs-lookup"><span data-stu-id="12771-103">Gets the reported Azure subscription usage details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12771-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="12771-104">SYNTAX</span></span>

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12771-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12771-105">DESCRIPTION</span></span>
<span data-ttu-id="12771-106">Das Cmdlet " **Get-UsageAggregates** " ruft aggregierte Azure-Abonnement Nutzungsdaten mit den folgenden Eigenschaften ab:</span><span class="sxs-lookup"><span data-stu-id="12771-106">The **Get-UsageAggregates** cmdlet gets aggregated Azure subscription usage data by the following properties:</span></span> 

- <span data-ttu-id="12771-107">Anfangs-und Endzeiten für den Zeitpunkt, zu dem die Verwendung gemeldet wurde.</span><span class="sxs-lookup"><span data-stu-id="12771-107">Start and end times of when the usage was reported.</span></span>

- <span data-ttu-id="12771-108">Aggregations Genauigkeit, entweder täglich oder stündlich.</span><span class="sxs-lookup"><span data-stu-id="12771-108">Aggregation precision, either daily or hourly.</span></span>

- <span data-ttu-id="12771-109">Details der Instanzebene für mehrere Instanzen der gleichen Ressource.</span><span class="sxs-lookup"><span data-stu-id="12771-109">Instance level detail for multiple instances of the same resource.</span></span>

<span data-ttu-id="12771-110">Für konsistente Ergebnisse basieren die zurückgegebenen Daten auf dem Zeitpunkt, zu dem die Nutzungsdetails von der Azure-Ressource gemeldet wurden.</span><span class="sxs-lookup"><span data-stu-id="12771-110">For consistent results, the returned data is based on when the usage details were reported by the Azure resource.</span></span>

<span data-ttu-id="12771-111">Weitere Informationen finden Sie unter Referenz zu Azure Billing-Ruhe-API https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c ( https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) in der Microsoft Developer Network Library.</span><span class="sxs-lookup"><span data-stu-id="12771-111">For more information, see Azure Billing REST API Referencehttps://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c (https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) in the Microsoft Developer Network library.</span></span>

## <span data-ttu-id="12771-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="12771-112">EXAMPLES</span></span>

### <span data-ttu-id="12771-113">Beispiel 1: Abrufen von Abonnementdaten</span><span class="sxs-lookup"><span data-stu-id="12771-113">Example 1: Retrieve subscription data</span></span>
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

<span data-ttu-id="12771-114">Dieser Befehl ruft die gemeldeten Nutzungsdaten für das Abonnement zwischen 5/2/2015 und 5/5/2015 ab.</span><span class="sxs-lookup"><span data-stu-id="12771-114">This command retrieves the reported usage data for the subscription between 5/2/2015 and 5/5/2015.</span></span>

## <span data-ttu-id="12771-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="12771-115">PARAMETERS</span></span>

### <span data-ttu-id="12771-116">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="12771-116">-AggregationGranularity</span></span>
<span data-ttu-id="12771-117">Gibt die Aggregations Genauigkeit der Daten an.</span><span class="sxs-lookup"><span data-stu-id="12771-117">Specifies the aggregation precision of the data.</span></span>
<span data-ttu-id="12771-118">Gültige Werte sind: täglich und stündlich.</span><span class="sxs-lookup"><span data-stu-id="12771-118">Valid values are: Daily and Hourly.</span></span>

<span data-ttu-id="12771-119">Der Standardwert ist Daily.</span><span class="sxs-lookup"><span data-stu-id="12771-119">The default value is Daily.</span></span>

```yaml
Type: AggregationGranularity
Parameter Sets: (All)
Aliases: 
Accepted values: Daily, Hourly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12771-120">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="12771-120">-ContinuationToken</span></span>
<span data-ttu-id="12771-121">Gibt das Fortsetzungstoken an, das im vorherigen Aufruf aus dem Antworttext abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="12771-121">Specifies the continuation token that was retrieved from the response body in the previous call.</span></span>
<span data-ttu-id="12771-122">Bei einem umfangreichen Resultset werden Antworten mithilfe von Fortsetzungstoken ausgelagert.</span><span class="sxs-lookup"><span data-stu-id="12771-122">For a large result set, responses are paged by using continuation tokens.</span></span>
<span data-ttu-id="12771-123">Das Fortsetzungstoken dient als Textmarke für den Fortschritt.</span><span class="sxs-lookup"><span data-stu-id="12771-123">The continuation token serves as a bookmark for progress.</span></span>
<span data-ttu-id="12771-124">Wenn Sie diesen Parameter nicht angeben, werden die Daten aus dem Anfang des in *ReportedStartTime* angegebenen Tages oder der Stunde abgerufen.</span><span class="sxs-lookup"><span data-stu-id="12771-124">If you do not specify this parameter, the data is retrieved from the beginning of the day or hour specified in *ReportedStartTime*.</span></span>
<span data-ttu-id="12771-125">Wir empfehlen, dass Sie dem nächsten Link auf der Seite Antwort auf die Daten folgen.</span><span class="sxs-lookup"><span data-stu-id="12771-125">We recommend that you follow the next link in the response to page though the data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12771-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12771-126">-DefaultProfile</span></span>
<span data-ttu-id="12771-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="12771-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12771-128">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="12771-128">-ReportedEndTime</span></span>
<span data-ttu-id="12771-129">Gibt die gemeldete Endzeit für den Zeitpunkt an, zu dem die Ressourcenverwendung im Azure-Abrechnungssystem aufgezeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="12771-129">Specifies the reported end time for when resource usage was recorded in the Azure billing system.</span></span>

<span data-ttu-id="12771-130">Azure ist ein verteiltes System, das mehrere Rechenzentren in der ganzen Welt umfasst, sodass eine Verzögerung zwischen dem Zeitpunkt der tatsächlichen Nutzung der Ressource, der Ressourcen Nutzungszeit und dem Erreichen des Abrechnungssystems, dem Zeitpunkt, zu dem die Ressourcenverwendung gemeldet wurde, besteht.</span><span class="sxs-lookup"><span data-stu-id="12771-130">Azure is a distributed system, spanning multiple datacenters around the world, so there is a delay between when the resource was actually consumed, which is the resource usage time, and when the usage event reached the billing system, which is the resource usage reported time.</span></span>
<span data-ttu-id="12771-131">Um alle nutzungsereignisse für ein Abonnement abzurufen, die für einen Zeitraum gemeldet werden, können Sie nach gemeldeter Zeit Abfragen.</span><span class="sxs-lookup"><span data-stu-id="12771-131">In order to get all usage events for a subscription that are reported for a time period, you query by reported time.</span></span>
<span data-ttu-id="12771-132">Obwohl Sie nach der angegebenen Zeit Abfragen, aggregiert das Cmdlet die Antwortdaten nach der Ressourcen Nutzungszeit.</span><span class="sxs-lookup"><span data-stu-id="12771-132">Even though you query by reported time, the cmdlet aggregates the response data by the resource usage time.</span></span>
<span data-ttu-id="12771-133">Die Ressourcen Nutzungsdaten sind der hilfreiche Drehpunkt für die Datenanalyse.</span><span class="sxs-lookup"><span data-stu-id="12771-133">The resource usage data is the useful pivot for analyzing the data.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12771-134">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="12771-134">-ReportedStartTime</span></span>
<span data-ttu-id="12771-135">Gibt die gemeldete Startzeit für den Zeitpunkt an, zu dem die Ressourcenverwendung im Azure-Abrechnungssystem aufgezeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="12771-135">Specifies the reported start time for when resource usage was recorded in the Azure billing system.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12771-136">-Show Details</span><span class="sxs-lookup"><span data-stu-id="12771-136">-ShowDetails</span></span>
<span data-ttu-id="12771-137">Gibt an, ob dieses Cmdlet Details auf Instanzebene mit den Nutzungsdaten zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="12771-137">Indicates whether this cmdlet returns instance-level details with the usage data.</span></span>

<span data-ttu-id="12771-138">Der Standardwert ist $true.</span><span class="sxs-lookup"><span data-stu-id="12771-138">The default value is $True.</span></span>

<span data-ttu-id="12771-139">Wenn $false, aggregiert der Dienst die Ergebnisse auf der Serverseite und gibt daher weniger Aggregat Gruppen zurück.</span><span class="sxs-lookup"><span data-stu-id="12771-139">If $False, the service aggregates the results on the server side, and therefore returns fewer aggregate groups.</span></span>
<span data-ttu-id="12771-140">Wenn Sie beispielsweise drei Websites ausführen, erhalten Sie standardmäßig drei Einzelposten für die Websitenutzung.</span><span class="sxs-lookup"><span data-stu-id="12771-140">For example, if you are running three websites, by default you will get three line items for website consumption.</span></span>
<span data-ttu-id="12771-141">Wenn der Wert jedoch $false ist, werden alle Daten für die gleiche **Abonnement** -, **Mess** -, **usageStartTime** und **usageEndTime** in einer einzelnen Zeile reduziert.</span><span class="sxs-lookup"><span data-stu-id="12771-141">However, when the value is $False, all the data for the same **subscriptionId** , **meterId** , **usageStartTime** , and **usageEndTime** is collapsed into a single line item.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12771-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12771-142">CommonParameters</span></span>
<span data-ttu-id="12771-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12771-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12771-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12771-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12771-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="12771-145">INPUTS</span></span>

### <span data-ttu-id="12771-146">Keine</span><span class="sxs-lookup"><span data-stu-id="12771-146">None</span></span>
<span data-ttu-id="12771-147">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="12771-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="12771-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="12771-148">OUTPUTS</span></span>

### <span data-ttu-id="12771-149">Microsoft. Azure. Commerce. UsageAggregates. Models. UsageAggregationGetResponse</span><span class="sxs-lookup"><span data-stu-id="12771-149">Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse</span></span>

## <span data-ttu-id="12771-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="12771-150">NOTES</span></span>

## <span data-ttu-id="12771-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="12771-151">RELATED LINKS</span></span>

