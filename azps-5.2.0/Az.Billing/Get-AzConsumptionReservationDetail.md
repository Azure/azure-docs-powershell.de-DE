---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionreservationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationDetail.md
ms.openlocfilehash: 2a49cb88fc25643cd26e7ed75d226b8abf6ee50f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295630"
---
# <span data-ttu-id="46ffe-101">Get-AzConsumptionReservationDetail</span><span class="sxs-lookup"><span data-stu-id="46ffe-101">Get-AzConsumptionReservationDetail</span></span>

## <span data-ttu-id="46ffe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46ffe-102">SYNOPSIS</span></span>
<span data-ttu-id="46ffe-103">Erhalten Sie Reservierungsdetails für den angegebenen Datumsbereich.</span><span class="sxs-lookup"><span data-stu-id="46ffe-103">Get reservations details for provided date range.</span></span>

## <span data-ttu-id="46ffe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46ffe-104">SYNTAX</span></span>

```
Get-AzConsumptionReservationDetail -StartDate <DateTime> -EndDate <DateTime> -ReservationOrderId <String>
 [-ReservationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46ffe-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46ffe-105">DESCRIPTION</span></span>
<span data-ttu-id="46ffe-106">Das **Cmdlet "Get-AzConsumptionReservationDetail"** ruft Reservierungsdetails für den angegebenen Datumsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="46ffe-106">The **Get-AzConsumptionReservationDetail** cmdlet gets reservations details for provided date range.</span></span>

## <span data-ttu-id="46ffe-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="46ffe-107">EXAMPLES</span></span>

### <span data-ttu-id="46ffe-108">Beispiel 1: Erhalten von Reservierungsdetails mit Reservierungsauftrags-ID für den angegebenen Datumsbereich</span><span class="sxs-lookup"><span data-stu-id="46ffe-108">Example 1: Get reservation details with reservation order Id for provided date range</span></span>
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

### <span data-ttu-id="46ffe-109">Beispiel 2: Erhalten von Reservierungsdetails mit Reservierungsauftrags-ID und Reservierungs-ID für den angegebenen Datumsbereich</span><span class="sxs-lookup"><span data-stu-id="46ffe-109">Example 2: Get reservation details with reservation order Id and reservation Id for provided date range</span></span>
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

## <span data-ttu-id="46ffe-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46ffe-110">PARAMETERS</span></span>

### <span data-ttu-id="46ffe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46ffe-111">-DefaultProfile</span></span>
<span data-ttu-id="46ffe-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="46ffe-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46ffe-113">-EndDate</span><span class="sxs-lookup"><span data-stu-id="46ffe-113">-EndDate</span></span>
<span data-ttu-id="46ffe-114">Die Enddaten (JJJJ-MM-DD in UTC) der Reservierungsdetails.</span><span class="sxs-lookup"><span data-stu-id="46ffe-114">The end data (YYYY-MM-DD in UTC) of the reservation detail.</span></span>

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

### <span data-ttu-id="46ffe-115">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="46ffe-115">-ReservationId</span></span>
<span data-ttu-id="46ffe-116">Der Bezeichner einer Reservierung innerhalb eines Reservierungsauftrags.</span><span class="sxs-lookup"><span data-stu-id="46ffe-116">The identifier of a reservation within a reservation order.</span></span>

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

### <span data-ttu-id="46ffe-117">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="46ffe-117">-ReservationOrderId</span></span>
<span data-ttu-id="46ffe-118">Der Bezeichner eines Reservierungskaufs.</span><span class="sxs-lookup"><span data-stu-id="46ffe-118">The identifier of a reservation purchase.</span></span>

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

### <span data-ttu-id="46ffe-119">-StartDate</span><span class="sxs-lookup"><span data-stu-id="46ffe-119">-StartDate</span></span>
<span data-ttu-id="46ffe-120">Die Startdaten (JJJJ-MM-DD in UTC) der Reservierungsdetails.</span><span class="sxs-lookup"><span data-stu-id="46ffe-120">The start data (YYYY-MM-DD in UTC) of the reservation detail.</span></span>

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

### <span data-ttu-id="46ffe-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46ffe-121">CommonParameters</span></span>
<span data-ttu-id="46ffe-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46ffe-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46ffe-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46ffe-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46ffe-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="46ffe-124">INPUTS</span></span>

### <span data-ttu-id="46ffe-125">Keine</span><span class="sxs-lookup"><span data-stu-id="46ffe-125">None</span></span>

## <span data-ttu-id="46ffe-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="46ffe-126">OUTPUTS</span></span>

### <span data-ttu-id="46ffe-127">Microsoft.Azure.Commands.Consumption.Models.PSReservationDetail</span><span class="sxs-lookup"><span data-stu-id="46ffe-127">Microsoft.Azure.Commands.Consumption.Models.PSReservationDetail</span></span>

## <span data-ttu-id="46ffe-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="46ffe-128">NOTES</span></span>

## <span data-ttu-id="46ffe-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="46ffe-129">RELATED LINKS</span></span>
