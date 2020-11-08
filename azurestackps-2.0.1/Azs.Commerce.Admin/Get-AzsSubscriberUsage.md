---
external help file: ''
Module Name: Azs.Commerce.Admin
online version: https://docs.microsoft.com/powershell/module/azs.commerce.admin/get-azssubscriberusage
schema: 2.0.0
ms.openlocfilehash: 9eed3f6f2a4d07bd48136c50ec173f801b30c928
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005550"
---
# <span data-ttu-id="647bc-101">Get-AzsSubscriberUsage</span><span class="sxs-lookup"><span data-stu-id="647bc-101">Get-AzsSubscriberUsage</span></span>

## <span data-ttu-id="647bc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="647bc-102">SYNOPSIS</span></span>
<span data-ttu-id="647bc-103">Ruft eine Sammlung von SubscriberUsageAggregates ab, die von Benutzern UsageAggregates werden.</span><span class="sxs-lookup"><span data-stu-id="647bc-103">Gets a collection of SubscriberUsageAggregates, which are UsageAggregates from users.</span></span>

## <span data-ttu-id="647bc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="647bc-104">SYNTAX</span></span>

```
Get-AzsSubscriberUsage -ReportedEndTime <DateTime> -ReportedStartTime <DateTime> [-SubscriptionId <String[]>]
 [-AggregationGranularity <String>] [-ContinuationToken <String>] [-SubscriberId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="647bc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="647bc-105">DESCRIPTION</span></span>
<span data-ttu-id="647bc-106">Ruft eine Sammlung von SubscriberUsageAggregates ab, die von Benutzern UsageAggregates werden.</span><span class="sxs-lookup"><span data-stu-id="647bc-106">Gets a collection of SubscriberUsageAggregates, which are UsageAggregates from users.</span></span>

## <span data-ttu-id="647bc-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="647bc-107">EXAMPLES</span></span>

### <span data-ttu-id="647bc-108">Beispiel 1: Abrufen von Nutzungsdaten, die nach Tag aggregiert werden</span><span class="sxs-lookup"><span data-stu-id="647bc-108">Example 1: Get usage data aggregated by day</span></span>
```powershell
Get-AzsSubscriberUsage -ReportedStartTime "2019-12-30T00:00:00Z" -ReportedEndTime "2019-12-31T00:00:00Z" -AggregationGranularity Daily
```

<span data-ttu-id="647bc-109">Rufen Sie die Nutzungsdaten für den gesamten Tag des 30. Dezember 2019 (in UTC) für alle Mandanten ab, die vom Tag aggregiert werden.</span><span class="sxs-lookup"><span data-stu-id="647bc-109">Get the usage data for the entire day of 30th Dec 2019 (in UTC) for all tenants under provider aggregated by the day.</span></span>
<span data-ttu-id="647bc-110">ReportedStartTime und ReportedEndTime müssen auf Tage gerundet werden.</span><span class="sxs-lookup"><span data-stu-id="647bc-110">ReportedStartTime and ReportedEndTime must be rounded to days.</span></span>
<span data-ttu-id="647bc-111">Wenn Sie als Dienstadministrator aufgerufen wird, werden alle Verwendungsdaten für jeden Mandanten effektiv angezeigt.</span><span class="sxs-lookup"><span data-stu-id="647bc-111">If called as the service administrator, this effectively shows all usage data for every tenant.</span></span>

### <span data-ttu-id="647bc-112">Beispiel 2: Abrufen von Nutzungsdaten, die stundenweise aggregiert sind</span><span class="sxs-lookup"><span data-stu-id="647bc-112">Example 2: Get usage data aggregated by the hour</span></span>
```powershell
Get-AzsSubscriberUsage -ReportedStartTime "2019-12-30T00:00:00Z" -ReportedEndTime "2019-12-30T02:00:00Z" -AggregationGranularity Hourly
```

<span data-ttu-id="647bc-113">Besorgen Sie sich die Nutzungsdaten zwischen 12.00-02.00 Uhr am 30. Dezember 2019 (in UTC), aggregiert nach Stunden.</span><span class="sxs-lookup"><span data-stu-id="647bc-113">Get the usage data between  12am - 2am on 30th Dec 2019 (in UTC) aggregated by the hour.</span></span>
<span data-ttu-id="647bc-114">ReportedStartTime und ReportedEndTime müssen auf Stunden gerundet werden.</span><span class="sxs-lookup"><span data-stu-id="647bc-114">ReportedStartTime and ReportedEndTime must be rounded to hours.</span></span>
<span data-ttu-id="647bc-115">Wenn Sie als Dienstadministrator aufgerufen werden, werden auch alle Verwendungsdaten für jeden Mandanten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="647bc-115">Likewise, if called as the service administrator, this effectively shows all usage data for every tenant.</span></span>

## <span data-ttu-id="647bc-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="647bc-116">PARAMETERS</span></span>

### <span data-ttu-id="647bc-117">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="647bc-117">-AggregationGranularity</span></span>
<span data-ttu-id="647bc-118">Die Aggregations Granularität.</span><span class="sxs-lookup"><span data-stu-id="647bc-118">The aggregation granularity.</span></span>

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

### <span data-ttu-id="647bc-119">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="647bc-119">-ContinuationToken</span></span>
<span data-ttu-id="647bc-120">Das Fortsetzungstoken.</span><span class="sxs-lookup"><span data-stu-id="647bc-120">The continuation token.</span></span>

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

### <span data-ttu-id="647bc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="647bc-121">-DefaultProfile</span></span>
<span data-ttu-id="647bc-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="647bc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="647bc-123">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="647bc-123">-ReportedEndTime</span></span>
<span data-ttu-id="647bc-124">Die gemeldete Endzeit (exklusiv).</span><span class="sxs-lookup"><span data-stu-id="647bc-124">The reported end time (exclusive).</span></span>

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

### <span data-ttu-id="647bc-125">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="647bc-125">-ReportedStartTime</span></span>
<span data-ttu-id="647bc-126">Die gemeldete Startzeit (inklusive).</span><span class="sxs-lookup"><span data-stu-id="647bc-126">The reported start time (inclusive).</span></span>

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

### <span data-ttu-id="647bc-127">-Abonnenten-Nr</span><span class="sxs-lookup"><span data-stu-id="647bc-127">-SubscriberId</span></span>
<span data-ttu-id="647bc-128">Die Mandanten-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="647bc-128">The tenant subscription identifier.</span></span>

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

### <span data-ttu-id="647bc-129">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="647bc-129">-SubscriptionId</span></span>
<span data-ttu-id="647bc-130">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="647bc-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="647bc-131">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="647bc-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="647bc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="647bc-132">CommonParameters</span></span>
<span data-ttu-id="647bc-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="647bc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="647bc-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="647bc-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="647bc-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="647bc-135">INPUTS</span></span>

## <span data-ttu-id="647bc-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="647bc-136">OUTPUTS</span></span>

### <span data-ttu-id="647bc-137">Microsoft. Azure. PowerShell. Cmdlets. Commerce. Models. Api20150601Preview. IUsageAggregate</span><span class="sxs-lookup"><span data-stu-id="647bc-137">Microsoft.Azure.PowerShell.Cmdlets.Commerce.Models.Api20150601Preview.IUsageAggregate</span></span>



## <span data-ttu-id="647bc-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="647bc-138">NOTES</span></span>

## <span data-ttu-id="647bc-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="647bc-139">RELATED LINKS</span></span>

