---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
ms.openlocfilehash: 3db5c7bf9665498236c3d0dacf05107926ed45eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659685"
---
# <span data-ttu-id="b0784-101">Get-AzReservationOrder</span><span class="sxs-lookup"><span data-stu-id="b0784-101">Get-AzReservationOrder</span></span>

## <span data-ttu-id="b0784-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b0784-102">SYNOPSIS</span></span>
<span data-ttu-id="b0784-103">Erhalten `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="b0784-103">Get `ReservationOrder`</span></span>

## <span data-ttu-id="b0784-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0784-104">SYNTAX</span></span>

```
Get-AzReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0784-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0784-105">DESCRIPTION</span></span>
<span data-ttu-id="b0784-106">Liste aller `ReservationOrder` s, auf die der Benutzer im aktuellen Mandanten zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="b0784-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="b0784-107">Wenn der ReservationOrderId-Parameter festzulegen ist, rufen Sie diesen bestimmten ReservationOrder.</span><span class="sxs-lookup"><span data-stu-id="b0784-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="b0784-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b0784-108">EXAMPLES</span></span>

### <span data-ttu-id="b0784-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b0784-109">Example 1</span></span>
```
PS C:\> Get-AzReservationOrder
```

<span data-ttu-id="b0784-110">Listen Sie alle auf `ReservationOrder` , auf die der Benutzer im aktuellen Mandanten zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="b0784-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="b0784-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b0784-111">Example 2</span></span>
```
PS C:\> Get-AzReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="b0784-112">Abrufen `ReservationOrder` mit dem angegebenen ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="b0784-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="b0784-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0784-113">PARAMETERS</span></span>

### <span data-ttu-id="b0784-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0784-114">-DefaultProfile</span></span>
<span data-ttu-id="b0784-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b0784-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0784-116">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="b0784-116">-ReservationOrderId</span></span>
<span data-ttu-id="b0784-117">Die ID des spezifischen ReservationOrder, das der Benutzer anzeigen möchte</span><span class="sxs-lookup"><span data-stu-id="b0784-117">Id of the specific ReservationOrder that user wants to see</span></span>

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

### <span data-ttu-id="b0784-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0784-118">CommonParameters</span></span>
<span data-ttu-id="b0784-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0784-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0784-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0784-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0784-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b0784-121">INPUTS</span></span>

### <span data-ttu-id="b0784-122">Keine</span><span class="sxs-lookup"><span data-stu-id="b0784-122">None</span></span>

## <span data-ttu-id="b0784-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b0784-123">OUTPUTS</span></span>

### <span data-ttu-id="b0784-124">Microsoft. Azure. Commands. reservations. Models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="b0784-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

### <span data-ttu-id="b0784-125">Microsoft. Azure. Commands. reservations. Models. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="b0784-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="b0784-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="b0784-126">NOTES</span></span>

## <span data-ttu-id="b0784-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b0784-127">RELATED LINKS</span></span>
