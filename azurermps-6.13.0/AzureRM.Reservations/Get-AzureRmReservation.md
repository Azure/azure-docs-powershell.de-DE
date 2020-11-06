---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
ms.openlocfilehash: 1003dcf38815be8daba8b0e218dbca430a89f9e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477729"
---
# <span data-ttu-id="f4be2-101">Get-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="f4be2-101">Get-AzureRmReservation</span></span>

## <span data-ttu-id="f4be2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f4be2-102">SYNOPSIS</span></span>
<span data-ttu-id="f4be2-103">Abrufen `Reservation` von s in einer bestimmten Reservierungs Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="f4be2-103">Get `Reservation`s in a given reservation Order</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4be2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4be2-104">SYNTAX</span></span>

### <span data-ttu-id="f4be2-105">CommandLine (Standard)</span><span class="sxs-lookup"><span data-stu-id="f4be2-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservation -ReservationOrderId <Guid> [-ReservationId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4be2-106">Pipeobject</span><span class="sxs-lookup"><span data-stu-id="f4be2-106">PipeObject</span></span>
```
Get-AzureRmReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f4be2-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="f4be2-107">PagePipeObject</span></span>
```
Get-AzureRmReservation [-ReservationOrderPage <PSReservationOrderPage>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4be2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4be2-108">DESCRIPTION</span></span>
<span data-ttu-id="f4be2-109">Liste `Reservation` s innerhalb einer einzelnen `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="f4be2-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="f4be2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f4be2-110">EXAMPLES</span></span>

### <span data-ttu-id="f4be2-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f4be2-111">Example 1</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="f4be2-112">Liste `Reservation` s innerhalb der angegebenen `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="f4be2-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="f4be2-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f4be2-113">Example 2</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="f4be2-114">Abrufen spezifischer `Reservation` Details.</span><span class="sxs-lookup"><span data-stu-id="f4be2-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="f4be2-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4be2-115">PARAMETERS</span></span>

### <span data-ttu-id="f4be2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4be2-116">-DefaultProfile</span></span>
<span data-ttu-id="f4be2-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f4be2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4be2-118">-Reservierungs-Nr.</span><span class="sxs-lookup"><span data-stu-id="f4be2-118">-ReservationId</span></span>
<span data-ttu-id="f4be2-119">Die ID des `Reservation` anzusehenden</span><span class="sxs-lookup"><span data-stu-id="f4be2-119">Id of the `Reservation` to look at</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4be2-120">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="f4be2-120">-ReservationOrder</span></span>
<span data-ttu-id="f4be2-121">Pipe-Objektparameter für `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="f4be2-121">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder
Parameter Sets: PipeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4be2-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="f4be2-122">-ReservationOrderId</span></span>
<span data-ttu-id="f4be2-123">Die ID des `ReservationOrder` , die das enthält `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="f4be2-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="f4be2-124">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f4be2-124">Required.</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4be2-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="f4be2-125">-ReservationOrderPage</span></span>
<span data-ttu-id="f4be2-126">Pipe-Objektparameter für `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="f4be2-126">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage
Parameter Sets: PagePipeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4be2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4be2-127">CommonParameters</span></span>
<span data-ttu-id="f4be2-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4be2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4be2-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4be2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4be2-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f4be2-130">INPUTS</span></span>

### <span data-ttu-id="f4be2-131">System. GUID</span><span class="sxs-lookup"><span data-stu-id="f4be2-131">System.Guid</span></span>

### <span data-ttu-id="f4be2-132">Microsoft. Azure. Commands. reservations. Models. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="f4be2-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>
<span data-ttu-id="f4be2-133">Parameter: ReservationOrder (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f4be2-133">Parameters: ReservationOrder (ByValue)</span></span>

### <span data-ttu-id="f4be2-134">Microsoft. Azure. Commands. reservations. Models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="f4be2-134">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>
<span data-ttu-id="f4be2-135">Parameter: ReservationOrderPage (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f4be2-135">Parameters: ReservationOrderPage (ByValue)</span></span>

## <span data-ttu-id="f4be2-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f4be2-136">OUTPUTS</span></span>

### <span data-ttu-id="f4be2-137">Microsoft. Azure. Commands. reservations. Models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="f4be2-137">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="f4be2-138">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="f4be2-138">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="f4be2-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="f4be2-139">NOTES</span></span>

## <span data-ttu-id="f4be2-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f4be2-140">RELATED LINKS</span></span>
