---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
ms.openlocfilehash: d7eab73fbe6bed4a51df7c5056a0dc52787de845
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659692"
---
# <span data-ttu-id="d4004-101">Get-AzReservation</span><span class="sxs-lookup"><span data-stu-id="d4004-101">Get-AzReservation</span></span>

## <span data-ttu-id="d4004-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d4004-102">SYNOPSIS</span></span>
<span data-ttu-id="d4004-103">Abrufen `Reservation` von s in einer bestimmten Reservierungs Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="d4004-103">Get `Reservation`s in a given reservation Order</span></span>

## <span data-ttu-id="d4004-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4004-104">SYNTAX</span></span>

### <span data-ttu-id="d4004-105">CommandLine (Standard)</span><span class="sxs-lookup"><span data-stu-id="d4004-105">CommandLine (Default)</span></span>
```
Get-AzReservation -ReservationOrderId <Guid> [-ReservationId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d4004-106">Pipeobject</span><span class="sxs-lookup"><span data-stu-id="d4004-106">PipeObject</span></span>
```
Get-AzReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d4004-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="d4004-107">PagePipeObject</span></span>
```
Get-AzReservation [-ReservationOrderPage <PSReservationOrderPage>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d4004-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4004-108">DESCRIPTION</span></span>
<span data-ttu-id="d4004-109">Liste `Reservation` s innerhalb einer einzelnen `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="d4004-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="d4004-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4004-110">EXAMPLES</span></span>

### <span data-ttu-id="d4004-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d4004-111">Example 1</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="d4004-112">Liste `Reservation` s innerhalb der angegebenen `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="d4004-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="d4004-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d4004-113">Example 2</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="d4004-114">Abrufen spezifischer `Reservation` Details.</span><span class="sxs-lookup"><span data-stu-id="d4004-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="d4004-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4004-115">PARAMETERS</span></span>

### <span data-ttu-id="d4004-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4004-116">-DefaultProfile</span></span>
<span data-ttu-id="d4004-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d4004-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4004-118">-Reservierungs-Nr.</span><span class="sxs-lookup"><span data-stu-id="d4004-118">-ReservationId</span></span>
<span data-ttu-id="d4004-119">Die ID des `Reservation` anzusehenden</span><span class="sxs-lookup"><span data-stu-id="d4004-119">Id of the `Reservation` to look at</span></span>

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

### <span data-ttu-id="d4004-120">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="d4004-120">-ReservationOrder</span></span>
<span data-ttu-id="d4004-121">Pipe-Objektparameter für `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="d4004-121">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="d4004-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="d4004-122">-ReservationOrderId</span></span>
<span data-ttu-id="d4004-123">Die ID des `ReservationOrder` , die das enthält `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="d4004-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="d4004-124">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d4004-124">Required.</span></span>

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

### <span data-ttu-id="d4004-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="d4004-125">-ReservationOrderPage</span></span>
<span data-ttu-id="d4004-126">Pipe-Objektparameter für `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="d4004-126">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="d4004-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4004-127">CommonParameters</span></span>
<span data-ttu-id="d4004-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4004-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4004-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4004-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4004-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d4004-130">INPUTS</span></span>

### <span data-ttu-id="d4004-131">System. GUID</span><span class="sxs-lookup"><span data-stu-id="d4004-131">System.Guid</span></span>

### <span data-ttu-id="d4004-132">Microsoft. Azure. Commands. reservations. Models. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="d4004-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

### <span data-ttu-id="d4004-133">Microsoft. Azure. Commands. reservations. Models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="d4004-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="d4004-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d4004-134">OUTPUTS</span></span>

### <span data-ttu-id="d4004-135">Microsoft. Azure. Commands. reservations. Models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="d4004-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="d4004-136">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="d4004-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="d4004-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="d4004-137">NOTES</span></span>

## <span data-ttu-id="d4004-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d4004-138">RELATED LINKS</span></span>
