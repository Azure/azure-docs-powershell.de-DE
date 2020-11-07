---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
ms.openlocfilehash: 15faf94ae7e0afac7200423dcd36d8edf2964c21
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846815"
---
# <span data-ttu-id="76aba-101">Get-AzReservationOrder</span><span class="sxs-lookup"><span data-stu-id="76aba-101">Get-AzReservationOrder</span></span>

## <span data-ttu-id="76aba-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="76aba-102">SYNOPSIS</span></span>
<span data-ttu-id="76aba-103">Erhalten `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="76aba-103">Get `ReservationOrder`</span></span>

## <span data-ttu-id="76aba-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="76aba-104">SYNTAX</span></span>

```
Get-AzReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="76aba-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="76aba-105">DESCRIPTION</span></span>
<span data-ttu-id="76aba-106">Liste aller `ReservationOrder` s, auf die der Benutzer im aktuellen Mandanten zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="76aba-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="76aba-107">Wenn der ReservationOrderId-Parameter festzulegen ist, rufen Sie diesen bestimmten ReservationOrder.</span><span class="sxs-lookup"><span data-stu-id="76aba-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="76aba-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="76aba-108">EXAMPLES</span></span>

### <span data-ttu-id="76aba-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="76aba-109">Example 1</span></span>
```
PS C:\> Get-AzReservationOrder
```

<span data-ttu-id="76aba-110">Listen Sie alle auf `ReservationOrder` , auf die der Benutzer im aktuellen Mandanten zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="76aba-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="76aba-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="76aba-111">Example 2</span></span>
```
PS C:\> Get-AzReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="76aba-112">Abrufen `ReservationOrder` mit dem angegebenen ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="76aba-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="76aba-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="76aba-113">PARAMETERS</span></span>

### <span data-ttu-id="76aba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76aba-114">-DefaultProfile</span></span>
<span data-ttu-id="76aba-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="76aba-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76aba-116">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="76aba-116">-ReservationOrderId</span></span>
<span data-ttu-id="76aba-117">Die ID des spezifischen ReservationOrder, das der Benutzer anzeigen möchte</span><span class="sxs-lookup"><span data-stu-id="76aba-117">Id of the specific ReservationOrder that user wants to see</span></span>

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

### <span data-ttu-id="76aba-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76aba-118">CommonParameters</span></span>
<span data-ttu-id="76aba-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76aba-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76aba-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76aba-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76aba-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="76aba-121">INPUTS</span></span>

### <span data-ttu-id="76aba-122">Keine</span><span class="sxs-lookup"><span data-stu-id="76aba-122">None</span></span>

## <span data-ttu-id="76aba-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="76aba-123">OUTPUTS</span></span>

### <span data-ttu-id="76aba-124">Microsoft. Azure. Commands. reservations. Models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="76aba-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

### <span data-ttu-id="76aba-125">Microsoft. Azure. Commands. reservations. Models. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="76aba-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="76aba-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="76aba-126">NOTES</span></span>

## <span data-ttu-id="76aba-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="76aba-127">RELATED LINKS</span></span>
