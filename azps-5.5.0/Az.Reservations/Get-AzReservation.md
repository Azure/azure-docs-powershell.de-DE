---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
ms.openlocfilehash: 2970abdcce0be707e5b6ef407adee5261a0620de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174492"
---
# <span data-ttu-id="7f97f-101">Get-AzReservation</span><span class="sxs-lookup"><span data-stu-id="7f97f-101">Get-AzReservation</span></span>

## <span data-ttu-id="7f97f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f97f-102">SYNOPSIS</span></span>
<span data-ttu-id="7f97f-103">Erhalten `Reservation` von S in einer bestimmten Reservierungsreihenfolge</span><span class="sxs-lookup"><span data-stu-id="7f97f-103">Get `Reservation`s in a given reservation Order</span></span>

## <span data-ttu-id="7f97f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f97f-104">SYNTAX</span></span>

### <span data-ttu-id="7f97f-105">Befehlszeile (Standard)</span><span class="sxs-lookup"><span data-stu-id="7f97f-105">CommandLine (Default)</span></span>
```
Get-AzReservation -ReservationOrderId <Guid> [-ReservationId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7f97f-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="7f97f-106">PipeObject</span></span>
```
Get-AzReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7f97f-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="7f97f-107">PagePipeObject</span></span>
```
Get-AzReservation [-ReservationOrderPage <PSReservationOrderPage>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f97f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7f97f-108">DESCRIPTION</span></span>
<span data-ttu-id="7f97f-109">Liste `Reservation` in einer einzelnen `ReservationOrder` Liste</span><span class="sxs-lookup"><span data-stu-id="7f97f-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="7f97f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7f97f-110">EXAMPLES</span></span>

### <span data-ttu-id="7f97f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7f97f-111">Example 1</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="7f97f-112">Listen `Reservation` innerhalb der angegebenen `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="7f97f-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="7f97f-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7f97f-113">Example 2</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="7f97f-114">Hier erhalten Sie `Reservation` spezifische Details.</span><span class="sxs-lookup"><span data-stu-id="7f97f-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="7f97f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f97f-115">PARAMETERS</span></span>

### <span data-ttu-id="7f97f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f97f-116">-DefaultProfile</span></span>
<span data-ttu-id="7f97f-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7f97f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f97f-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="7f97f-118">-ReservationId</span></span>
<span data-ttu-id="7f97f-119">ID des zu `Reservation` betrachtende</span><span class="sxs-lookup"><span data-stu-id="7f97f-119">Id of the `Reservation` to look at</span></span>

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

### <span data-ttu-id="7f97f-120">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="7f97f-120">-ReservationOrder</span></span>
<span data-ttu-id="7f97f-121">Objektparameter 'Pipe' für `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="7f97f-121">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="7f97f-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="7f97f-122">-ReservationOrderId</span></span>
<span data-ttu-id="7f97f-123">DIE ID der `ReservationOrder` Id, die den `Reservation` enthält.</span><span class="sxs-lookup"><span data-stu-id="7f97f-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="7f97f-124">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7f97f-124">Required.</span></span>

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

### <span data-ttu-id="7f97f-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="7f97f-125">-ReservationOrderPage</span></span>
<span data-ttu-id="7f97f-126">Objektparameter 'Pipe' für `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="7f97f-126">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="7f97f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f97f-127">CommonParameters</span></span>
<span data-ttu-id="7f97f-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f97f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f97f-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f97f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f97f-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7f97f-130">INPUTS</span></span>

### <span data-ttu-id="7f97f-131">System.Guid</span><span class="sxs-lookup"><span data-stu-id="7f97f-131">System.Guid</span></span>

### <span data-ttu-id="7f97f-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="7f97f-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

### <span data-ttu-id="7f97f-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="7f97f-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="7f97f-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7f97f-134">OUTPUTS</span></span>

### <span data-ttu-id="7f97f-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="7f97f-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="7f97f-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="7f97f-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="7f97f-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7f97f-137">NOTES</span></span>

## <span data-ttu-id="7f97f-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7f97f-138">RELATED LINKS</span></span>
