---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionreservationsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationSummary.md
ms.openlocfilehash: 3b59aaf537c544a53a1e1cccbb09c1964f6662fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652363"
---
# <span data-ttu-id="e514c-101">Get-AzConsumptionReservationSummary</span><span class="sxs-lookup"><span data-stu-id="e514c-101">Get-AzConsumptionReservationSummary</span></span>

## <span data-ttu-id="e514c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e514c-102">SYNOPSIS</span></span>
<span data-ttu-id="e514c-103">Erhalten Sie Reservierungs Zusammenfassungen für tägliche oder monatliche Körnungen.</span><span class="sxs-lookup"><span data-stu-id="e514c-103">Get reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="e514c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e514c-104">SYNTAX</span></span>

```
Get-AzConsumptionReservationSummary -Grain <String> -ReservationOrderId <String> [-ReservationId <String>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e514c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e514c-105">DESCRIPTION</span></span>
<span data-ttu-id="e514c-106">Das Cmdlet " **Get-AzConsumptionReservationSummary** " erhält Reservierungs Zusammenfassungen für das tägliche oder monatliche Korn.</span><span class="sxs-lookup"><span data-stu-id="e514c-106">The **Get-AzConsumptionReservationSummary** cmdlet gets reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="e514c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e514c-107">EXAMPLES</span></span>

### <span data-ttu-id="e514c-108">Beispiel 1: Abrufen von Reservierungs Zusammenfassungen mit der Reservierungs Auftrags-ID für monatliches Getreide</span><span class="sxs-lookup"><span data-stu-id="e514c-108">Example 1: Get reservation summaries with reservation order Id for monthly grain</span></span>
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

### <span data-ttu-id="e514c-109">Beispiel 2: Abrufen von Reservierungs Zusammenfassungen mit der Reservierungs Auftrags-ID und der Reservierungs-ID für monatliches Getreide</span><span class="sxs-lookup"><span data-stu-id="e514c-109">Example 2: Get reservation summaries with reservation order Id and reservation Id for monthly grain</span></span>
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

### <span data-ttu-id="e514c-110">Beispiel 3: Abrufen von Reservierungs Zusammenfassungen mit der Reservierungs Auftrags-ID für das tägliche Korn, vorausgesetzt, Datumsbereich</span><span class="sxs-lookup"><span data-stu-id="e514c-110">Example 3: Get reservation summaries with reservation order Id for daily grain provided date range</span></span>
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

### <span data-ttu-id="e514c-111">Beispiel 4: Abrufen von Reservierungs Zusammenfassungen mit der Reservierungs Auftrags-ID und der Reservierungs-ID für das tägliche Getreide bereitgestellte Datumsbereich</span><span class="sxs-lookup"><span data-stu-id="e514c-111">Example 4: Get reservation summaries with reservation order Id and reservation Id for daily grain provided date range</span></span>
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

## <span data-ttu-id="e514c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e514c-112">PARAMETERS</span></span>

### <span data-ttu-id="e514c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e514c-113">-DefaultProfile</span></span>
<span data-ttu-id="e514c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e514c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e514c-115">-Enddate</span><span class="sxs-lookup"><span data-stu-id="e514c-115">-EndDate</span></span>
<span data-ttu-id="e514c-116">Die Enddaten (yyyy-mm-tt in UTC) der Reservierungs Zusammenfassung, die nur für das tägliche Korn erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="e514c-116">The end data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

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

### <span data-ttu-id="e514c-117">-Grain</span><span class="sxs-lookup"><span data-stu-id="e514c-117">-Grain</span></span>
<span data-ttu-id="e514c-118">Das Zeit Korn der Reservierungs Zusammenfassung kann täglich oder monatlich sein.</span><span class="sxs-lookup"><span data-stu-id="e514c-118">The time grain of the reservation summary, can be daily or monthly.</span></span>

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

### <span data-ttu-id="e514c-119">-Reservierungs-Nr.</span><span class="sxs-lookup"><span data-stu-id="e514c-119">-ReservationId</span></span>
<span data-ttu-id="e514c-120">Der Bezeichner einer Reservierung innerhalb einer Reservierungs Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="e514c-120">The identifier of a reservation within a reservation order.</span></span>

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

### <span data-ttu-id="e514c-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="e514c-121">-ReservationOrderId</span></span>
<span data-ttu-id="e514c-122">Der Bezeichner eines Reservierungs Kaufs.</span><span class="sxs-lookup"><span data-stu-id="e514c-122">The identifier of a reservation purchase.</span></span>

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

### <span data-ttu-id="e514c-123">-StartDate</span><span class="sxs-lookup"><span data-stu-id="e514c-123">-StartDate</span></span>
<span data-ttu-id="e514c-124">Die Startdaten (yyyy-mm-tt in UTC) der Reservierungs Zusammenfassung, die nur für das tägliche Korn erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="e514c-124">The start data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

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

### <span data-ttu-id="e514c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e514c-125">CommonParameters</span></span>
<span data-ttu-id="e514c-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e514c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e514c-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e514c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e514c-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e514c-128">INPUTS</span></span>

### <span data-ttu-id="e514c-129">Keine</span><span class="sxs-lookup"><span data-stu-id="e514c-129">None</span></span>

## <span data-ttu-id="e514c-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e514c-130">OUTPUTS</span></span>

### <span data-ttu-id="e514c-131">Microsoft. Azure. Commands. Verbrauch. Models. PSReservationSummary</span><span class="sxs-lookup"><span data-stu-id="e514c-131">Microsoft.Azure.Commands.Consumption.Models.PSReservationSummary</span></span>

## <span data-ttu-id="e514c-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="e514c-132">NOTES</span></span>

## <span data-ttu-id="e514c-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e514c-133">RELATED LINKS</span></span>
