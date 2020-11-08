---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionreservationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationDetail.md
ms.openlocfilehash: 2a49cb88fc25643cd26e7ed75d226b8abf6ee50f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167287"
---
# <span data-ttu-id="56804-101">Get-AzConsumptionReservationDetail</span><span class="sxs-lookup"><span data-stu-id="56804-101">Get-AzConsumptionReservationDetail</span></span>

## <span data-ttu-id="56804-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="56804-102">SYNOPSIS</span></span>
<span data-ttu-id="56804-103">Hier erhalten Sie Reservierungsdetails für den bereitgestellten Datumsbereich.</span><span class="sxs-lookup"><span data-stu-id="56804-103">Get reservations details for provided date range.</span></span>

## <span data-ttu-id="56804-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="56804-104">SYNTAX</span></span>

```
Get-AzConsumptionReservationDetail -StartDate <DateTime> -EndDate <DateTime> -ReservationOrderId <String>
 [-ReservationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56804-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56804-105">DESCRIPTION</span></span>
<span data-ttu-id="56804-106">Das Cmdlet " **Get-AzConsumptionReservationDetail** " ruft Reservierungsdetails für den bereitgestellten Datumsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="56804-106">The **Get-AzConsumptionReservationDetail** cmdlet gets reservations details for provided date range.</span></span>

## <span data-ttu-id="56804-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="56804-107">EXAMPLES</span></span>

### <span data-ttu-id="56804-108">Beispiel 1: Abrufen von Reservierungsdetails mit der Reservierungs Auftrags-ID für den bereitgestellten Datumsbereich</span><span class="sxs-lookup"><span data-stu-id="56804-108">Example 1: Get reservation details with reservation order Id for provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationDetail -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -StartDate 2017-10-01 -EndDate 2017-12-07
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640providers/Microsoft.Consumption/reservationDetails/20171007
InstanceId:  subscriptions/a98d6dc5-eb8f-46cf-8938-f1fb08f03706/resourcegroups/testrg/providers/microsoft.compute/virtualmachines/std2swindows
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171007
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
TotalReservedQuantity:  1
Type:  Microsoft.Consumption/reservationDetails
UsageDate:  10/7/2017 12:00:00 AM
UsedHour:  24
```

### <span data-ttu-id="56804-109">Beispiel 2: Abrufen von Reservierungsdetails mit der Reservierungs Auftrags-ID und der Reservierungs-ID für den bereitgestellten Datumsbereich</span><span class="sxs-lookup"><span data-stu-id="56804-109">Example 2: Get reservation details with reservation order Id and reservation Id for provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationDetail -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640 -StartDate 2017-10-01 -EndDate 2017-12-07
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640providers/Microsoft.Consumption/reservationDetails/20171007
InstanceId:  subscriptions/a98d6dc5-eb8f-46cf-8938-f1fb08f03706/resourcegroups/testrg/providers/microsoft.compute/virtualmachines/std2swindows
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171007
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
TotalReservedQuantity:  1
Type:  Microsoft.Consumption/reservationDetails
UsageDate:  10/7/2017 12:00:00 AM
UsedHour:  24
```

## <span data-ttu-id="56804-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="56804-110">PARAMETERS</span></span>

### <span data-ttu-id="56804-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56804-111">-DefaultProfile</span></span>
<span data-ttu-id="56804-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="56804-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56804-113">-Enddate</span><span class="sxs-lookup"><span data-stu-id="56804-113">-EndDate</span></span>
<span data-ttu-id="56804-114">Die Enddaten (yyyy-mm-tt in UTC) des Reservierungsdetails.</span><span class="sxs-lookup"><span data-stu-id="56804-114">The end data (YYYY-MM-DD in UTC) of the reservation detail.</span></span>

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

### <span data-ttu-id="56804-115">-Reservierungs-Nr.</span><span class="sxs-lookup"><span data-stu-id="56804-115">-ReservationId</span></span>
<span data-ttu-id="56804-116">Der Bezeichner einer Reservierung innerhalb einer Reservierungs Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="56804-116">The identifier of a reservation within a reservation order.</span></span>

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

### <span data-ttu-id="56804-117">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="56804-117">-ReservationOrderId</span></span>
<span data-ttu-id="56804-118">Der Bezeichner eines Reservierungs Kaufs.</span><span class="sxs-lookup"><span data-stu-id="56804-118">The identifier of a reservation purchase.</span></span>

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

### <span data-ttu-id="56804-119">-StartDate</span><span class="sxs-lookup"><span data-stu-id="56804-119">-StartDate</span></span>
<span data-ttu-id="56804-120">Die Startdaten (yyyy-mm-tt in UTC) des Reservierungsdetails.</span><span class="sxs-lookup"><span data-stu-id="56804-120">The start data (YYYY-MM-DD in UTC) of the reservation detail.</span></span>

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

### <span data-ttu-id="56804-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56804-121">CommonParameters</span></span>
<span data-ttu-id="56804-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56804-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56804-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56804-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56804-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="56804-124">INPUTS</span></span>

### <span data-ttu-id="56804-125">Keine</span><span class="sxs-lookup"><span data-stu-id="56804-125">None</span></span>

## <span data-ttu-id="56804-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="56804-126">OUTPUTS</span></span>

### <span data-ttu-id="56804-127">Microsoft. Azure. Commands. Verbrauch. Models. PSReservationDetail</span><span class="sxs-lookup"><span data-stu-id="56804-127">Microsoft.Azure.Commands.Consumption.Models.PSReservationDetail</span></span>

## <span data-ttu-id="56804-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="56804-128">NOTES</span></span>

## <span data-ttu-id="56804-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="56804-129">RELATED LINKS</span></span>
