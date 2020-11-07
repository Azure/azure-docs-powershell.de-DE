---
external help file: Azs.Commerce.Admin-help.xml
Module Name: Azs.Commerce.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 12b98727cdb8e6d31fb1aaf1a2215b79a6b982e5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825800"
---
# <span data-ttu-id="3b3a9-101">Get-AzsSubscriberUsage</span><span class="sxs-lookup"><span data-stu-id="3b3a9-101">Get-AzsSubscriberUsage</span></span>

## <span data-ttu-id="3b3a9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3b3a9-102">SYNOPSIS</span></span>
<span data-ttu-id="3b3a9-103">Abrufen von Nutzungsdaten aus der angegebenen Zeitspanne.</span><span class="sxs-lookup"><span data-stu-id="3b3a9-103">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="3b3a9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b3a9-104">SYNTAX</span></span>

```
Get-AzsSubscriberUsage [[-SubscriberId] <String>] [-ReportedStartTime] <DateTime>
 [[-AggregationGranularity] <String>] [[-Skip] <Int32>] [-ReportedEndTime] <DateTime>
 [[-ContinuationToken] <String>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="3b3a9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b3a9-105">DESCRIPTION</span></span>
<span data-ttu-id="3b3a9-106">Abrufen von Nutzungsdaten aus der angegebenen Zeitspanne.</span><span class="sxs-lookup"><span data-stu-id="3b3a9-106">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="3b3a9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3b3a9-107">EXAMPLES</span></span>

### <span data-ttu-id="3b3a9-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3b3a9-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriberUsage -ReportedStartTime "2017-09-06T00:00:00Z" -ReportedEndTime "2017-09-07T00:00:00Z"
```

<span data-ttu-id="3b3a9-109">Abrufen von Nutzungsdaten aus den letzten 24 Stunden.</span><span class="sxs-lookup"><span data-stu-id="3b3a9-109">Get usage data from the last 24 hours.</span></span>

## <span data-ttu-id="3b3a9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b3a9-110">PARAMETERS</span></span>

### <span data-ttu-id="3b3a9-111">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="3b3a9-111">-AggregationGranularity</span></span>
<span data-ttu-id="3b3a9-112">Die Aggregations Granularität.</span><span class="sxs-lookup"><span data-stu-id="3b3a9-112">The aggregation granularity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3a9-113">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="3b3a9-113">-ContinuationToken</span></span>
<span data-ttu-id="3b3a9-114">Das Fortsetzungstoken.</span><span class="sxs-lookup"><span data-stu-id="3b3a9-114">The continuation token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3a9-115">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="3b3a9-115">-ReportedEndTime</span></span>
<span data-ttu-id="3b3a9-116">Die gemeldete Endzeit (exklusiv).</span><span class="sxs-lookup"><span data-stu-id="3b3a9-116">The reported end time (exclusive).</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3a9-117">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="3b3a9-117">-ReportedStartTime</span></span>
<span data-ttu-id="3b3a9-118">Die gemeldete Startzeit (inklusive).</span><span class="sxs-lookup"><span data-stu-id="3b3a9-118">The reported start time (inclusive).</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3a9-119">-Skip</span><span class="sxs-lookup"><span data-stu-id="3b3a9-119">-Skip</span></span>
<span data-ttu-id="3b3a9-120">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="3b3a9-120">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3a9-121">-Abonnenten-Nr</span><span class="sxs-lookup"><span data-stu-id="3b3a9-121">-SubscriberId</span></span>
<span data-ttu-id="3b3a9-122">Die Mandanten-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="3b3a9-122">The tenant subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3a9-123">-Top</span><span class="sxs-lookup"><span data-stu-id="3b3a9-123">-Top</span></span>
<span data-ttu-id="3b3a9-124">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="3b3a9-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="3b3a9-125">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="3b3a9-125">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3a9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b3a9-126">CommonParameters</span></span>
<span data-ttu-id="3b3a9-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b3a9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b3a9-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b3a9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b3a9-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3b3a9-129">INPUTS</span></span>

## <span data-ttu-id="3b3a9-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3b3a9-130">OUTPUTS</span></span>

### <span data-ttu-id="3b3a9-131">Microsoft. AzureStack. Management. Commerce. admin. Models. UsageAggregate</span><span class="sxs-lookup"><span data-stu-id="3b3a9-131">Microsoft.AzureStack.Management.Commerce.Admin.Models.UsageAggregate</span></span>

## <span data-ttu-id="3b3a9-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="3b3a9-132">NOTES</span></span>

## <span data-ttu-id="3b3a9-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3b3a9-133">RELATED LINKS</span></span>

