---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionreservationsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationSummary.md
ms.openlocfilehash: a76254f1aeb369e6f93ed8edccfd6f74ff79ceb0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295625"
---
# <span data-ttu-id="4b57d-101">Get-AzConsumptionReservationSummary</span><span class="sxs-lookup"><span data-stu-id="4b57d-101">Get-AzConsumptionReservationSummary</span></span>

## <span data-ttu-id="4b57d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b57d-102">SYNOPSIS</span></span>
<span data-ttu-id="4b57d-103">Erhalten Sie Zusammenfassungen der Reservierungen für tages- oder monatsige Körner.</span><span class="sxs-lookup"><span data-stu-id="4b57d-103">Get reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="4b57d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b57d-104">SYNTAX</span></span>

```
Get-AzConsumptionReservationSummary -Grain <String> -ReservationOrderId <String> [-ReservationId <String>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b57d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b57d-105">DESCRIPTION</span></span>
<span data-ttu-id="4b57d-106">Das **Cmdlet "Get-AzConsumptionReservationSummary"** ruft Reservierungszusammenfassungen für tägliche oder monatliche Körner ab.</span><span class="sxs-lookup"><span data-stu-id="4b57d-106">The **Get-AzConsumptionReservationSummary** cmdlet gets reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="4b57d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4b57d-107">EXAMPLES</span></span>

### <span data-ttu-id="4b57d-108">Beispiel 1: Erhalten von Reservierungszusammenfassungen mit Der Reservierungsauftrags-ID für monatliches Körnern</span><span class="sxs-lookup"><span data-stu-id="4b57d-108">Example 1: Get reservation summaries with reservation order Id for monthly grain</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain monthly -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20170901
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20170901
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  288
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  9/1/2017 12:00:00 AM
UsedHour:  288
```

### <span data-ttu-id="4b57d-109">Beispiel 2: Erhalten von Reservierungszusammenfassungen mit Reservierungsauftrags-ID und Reservierungs-ID für monatsweises Körner</span><span class="sxs-lookup"><span data-stu-id="4b57d-109">Example 2: Get reservation summaries with reservation order Id and reservation Id for monthly grain</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain monthly -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20170901
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20170901
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  288
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  9/1/2017 12:00:00 AM
UsedHour:  288
```

### <span data-ttu-id="4b57d-110">Beispiel 3: Erhalten von Reservierungszusammenfassungen mit Der Reservierungsauftrags-ID für den täglichen Datumsbereich</span><span class="sxs-lookup"><span data-stu-id="4b57d-110">Example 3: Get reservation summaries with reservation order Id for daily grain provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain daily -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -StartDate 2017-10-01 -EndDate 2017-12-07
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20171101
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171101
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  11/1/2017 12:00:00 AM
UsedHour:  24
```

### <span data-ttu-id="4b57d-111">Beispiel 4: Erhalten von Reservierungszusammenfassungen mit Reservierungsauftrags-ID und Reservierungs-ID für den täglich bereitgestellten Datumsbereich</span><span class="sxs-lookup"><span data-stu-id="4b57d-111">Example 4: Get reservation summaries with reservation order Id and reservation Id for daily grain provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain daily -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640 -StartDate 2017-10-01 -EndDate 2017-12-07
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20171101
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171101
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  11/1/2017 12:00:00 AM
UsedHour:  24
```

## <span data-ttu-id="4b57d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b57d-112">PARAMETERS</span></span>

### <span data-ttu-id="4b57d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b57d-113">-DefaultProfile</span></span>
<span data-ttu-id="4b57d-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4b57d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b57d-115">-EndDate</span><span class="sxs-lookup"><span data-stu-id="4b57d-115">-EndDate</span></span>
<span data-ttu-id="4b57d-116">Die Enddaten (JJJJ-MM-DD in UTC) der Reservierungszusammenfassung, nur für tägliches Körner erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4b57d-116">The end data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

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

### <span data-ttu-id="4b57d-117">-Grain</span><span class="sxs-lookup"><span data-stu-id="4b57d-117">-Grain</span></span>
<span data-ttu-id="4b57d-118">Das Zeitmask der Reservierungszusammenfassung kann täglich oder monatlich sein.</span><span class="sxs-lookup"><span data-stu-id="4b57d-118">The time grain of the reservation summary, can be daily or monthly.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: daily, monthly

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b57d-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="4b57d-119">-ReservationId</span></span>
<span data-ttu-id="4b57d-120">Der Bezeichner einer Reservierung innerhalb eines Reservierungsauftrags.</span><span class="sxs-lookup"><span data-stu-id="4b57d-120">The identifier of a reservation within a reservation order.</span></span>

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

### <span data-ttu-id="4b57d-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="4b57d-121">-ReservationOrderId</span></span>
<span data-ttu-id="4b57d-122">Der Bezeichner eines Reservierungskaufs.</span><span class="sxs-lookup"><span data-stu-id="4b57d-122">The identifier of a reservation purchase.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b57d-123">-StartDate</span><span class="sxs-lookup"><span data-stu-id="4b57d-123">-StartDate</span></span>
<span data-ttu-id="4b57d-124">Die Startdaten (JJJJ-MM-DD in UTC) der Reservierungszusammenfassung, nur für tägliches Körner erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4b57d-124">The start data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

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

### <span data-ttu-id="4b57d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b57d-125">CommonParameters</span></span>
<span data-ttu-id="4b57d-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b57d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b57d-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b57d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b57d-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4b57d-128">INPUTS</span></span>

### <span data-ttu-id="4b57d-129">Keine</span><span class="sxs-lookup"><span data-stu-id="4b57d-129">None</span></span>

## <span data-ttu-id="4b57d-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4b57d-130">OUTPUTS</span></span>

### <span data-ttu-id="4b57d-131">Microsoft.Azure.Commands.Consumption.Models.PSReservationSummary</span><span class="sxs-lookup"><span data-stu-id="4b57d-131">Microsoft.Azure.Commands.Consumption.Models.PSReservationSummary</span></span>

## <span data-ttu-id="4b57d-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4b57d-132">NOTES</span></span>

## <span data-ttu-id="4b57d-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4b57d-133">RELATED LINKS</span></span>
