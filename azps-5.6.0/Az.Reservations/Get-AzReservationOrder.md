---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/get-azreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
ms.openlocfilehash: 1878237544cc1b44b5e47814f455638c168e2412
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943690"
---
# <span data-ttu-id="dc6d5-101">Get-AzReservationOrder</span><span class="sxs-lookup"><span data-stu-id="dc6d5-101">Get-AzReservationOrder</span></span>

## <span data-ttu-id="dc6d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc6d5-102">SYNOPSIS</span></span>
<span data-ttu-id="dc6d5-103">Erhalten `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="dc6d5-103">Get `ReservationOrder`</span></span>

## <span data-ttu-id="dc6d5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc6d5-104">SYNTAX</span></span>

```
Get-AzReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc6d5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc6d5-105">DESCRIPTION</span></span>
<span data-ttu-id="dc6d5-106">Liste aller Benutzer, auf die `ReservationOrder` der Benutzer im aktuellen Mandanten zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="dc6d5-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="dc6d5-107">Wenn der Parameter ReservationOrderId festgelegt ist, erhalten Sie diese spezielle Reservierungsanordnung.</span><span class="sxs-lookup"><span data-stu-id="dc6d5-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="dc6d5-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dc6d5-108">EXAMPLES</span></span>

### <span data-ttu-id="dc6d5-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dc6d5-109">Example 1</span></span>
```
PS C:\> Get-AzReservationOrder
```

<span data-ttu-id="dc6d5-110">Auflisten `ReservationOrder` aller Zugriffe des Benutzers im aktuellen Mandanten</span><span class="sxs-lookup"><span data-stu-id="dc6d5-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="dc6d5-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="dc6d5-111">Example 2</span></span>
```
PS C:\> Get-AzReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="dc6d5-112">Mit `ReservationOrder` der angegebenen ReservationOrderId erhalten</span><span class="sxs-lookup"><span data-stu-id="dc6d5-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="dc6d5-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="dc6d5-113">PARAMETERS</span></span>

### <span data-ttu-id="dc6d5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc6d5-114">-DefaultProfile</span></span>
<span data-ttu-id="dc6d5-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dc6d5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc6d5-116">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="dc6d5-116">-ReservationOrderId</span></span>
<span data-ttu-id="dc6d5-117">ID der speziellen ReservationOrder, die der Benutzer sehen möchte</span><span class="sxs-lookup"><span data-stu-id="dc6d5-117">Id of the specific ReservationOrder that user wants to see</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc6d5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc6d5-118">CommonParameters</span></span>
<span data-ttu-id="dc6d5-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc6d5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc6d5-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc6d5-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc6d5-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dc6d5-121">INPUTS</span></span>

### <span data-ttu-id="dc6d5-122">Keine</span><span class="sxs-lookup"><span data-stu-id="dc6d5-122">None</span></span>

## <span data-ttu-id="dc6d5-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dc6d5-123">OUTPUTS</span></span>

### <span data-ttu-id="dc6d5-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="dc6d5-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

### <span data-ttu-id="dc6d5-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="dc6d5-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="dc6d5-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="dc6d5-126">NOTES</span></span>

## <span data-ttu-id="dc6d5-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="dc6d5-127">RELATED LINKS</span></span>
