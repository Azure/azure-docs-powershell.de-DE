---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
ms.openlocfilehash: 443f7c161cf2e3e44b2e080ef5adbc27665833bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476617"
---
# <span data-ttu-id="d8df4-101">Get-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="d8df4-101">Get-AzureRmReservation</span></span>

## <span data-ttu-id="d8df4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d8df4-102">SYNOPSIS</span></span>
<span data-ttu-id="d8df4-103">Abrufen `Reservation` von s in einer bestimmten Reservierungs Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="d8df4-103">Get `Reservation`s in a given reservation Order</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8df4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8df4-104">SYNTAX</span></span>

### <span data-ttu-id="d8df4-105">CommandLine (Standard)</span><span class="sxs-lookup"><span data-stu-id="d8df4-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservation -ReservationOrderId <String> [-ReservationId <String>] [<CommonParameters>]
```

### <span data-ttu-id="d8df4-106">Pipeobject</span><span class="sxs-lookup"><span data-stu-id="d8df4-106">PipeObject</span></span>
```
Get-AzureRmReservation [-ReservationOrder <PSReservationOrder>]
 [-ReservationOrderPage <PSReservationOrderPage>] [<CommonParameters>]
```

## <span data-ttu-id="d8df4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d8df4-107">DESCRIPTION</span></span>
<span data-ttu-id="d8df4-108">Liste `Reservation` s innerhalb einer einzelnen `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="d8df4-108">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="d8df4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d8df4-109">EXAMPLES</span></span>

### <span data-ttu-id="d8df4-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d8df4-110">Example 1</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="d8df4-111">Liste `Reservation` s innerhalb der angegebenen `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="d8df4-111">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="d8df4-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d8df4-112">Example 2</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="d8df4-113">Abrufen spezifischer `Reservation` Details.</span><span class="sxs-lookup"><span data-stu-id="d8df4-113">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="d8df4-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8df4-114">PARAMETERS</span></span>

### <span data-ttu-id="d8df4-115">-Reservierungs-Nr.</span><span class="sxs-lookup"><span data-stu-id="d8df4-115">-ReservationId</span></span>
<span data-ttu-id="d8df4-116">Die ID des `Reservation` anzusehenden</span><span class="sxs-lookup"><span data-stu-id="d8df4-116">Id of the `Reservation` to look at</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8df4-117">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="d8df4-117">-ReservationOrder</span></span>
<span data-ttu-id="d8df4-118">Pipe-Objektparameter für `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="d8df4-118">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: PSReservationOrder
Parameter Sets: PipeObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8df4-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="d8df4-119">-ReservationOrderId</span></span>
<span data-ttu-id="d8df4-120">Die ID des `ReservationOrder` , die das enthält `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="d8df4-120">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="d8df4-121">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d8df4-121">Required.</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8df4-122">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="d8df4-122">-ReservationOrderPage</span></span>
<span data-ttu-id="d8df4-123">Pipe-Objektparameter für `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="d8df4-123">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: PSReservationOrderPage
Parameter Sets: PipeObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8df4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8df4-124">CommonParameters</span></span>
<span data-ttu-id="d8df4-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8df4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8df4-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8df4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8df4-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d8df4-127">INPUTS</span></span>

### <span data-ttu-id="d8df4-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d8df4-128">System.String</span></span>
<span data-ttu-id="d8df4-129">Microsoft. Azure. Commands. reservations. Models. PSReservationOrder Microsoft. Azure. Commands. reservations. Models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="d8df4-129">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="d8df4-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d8df4-130">OUTPUTS</span></span>

### <span data-ttu-id="d8df4-131">Microsoft. Azure. Commands. reservations. Models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="d8df4-131">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>
<span data-ttu-id="d8df4-132">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="d8df4-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="d8df4-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="d8df4-133">NOTES</span></span>

## <span data-ttu-id="d8df4-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d8df4-134">RELATED LINKS</span></span>

