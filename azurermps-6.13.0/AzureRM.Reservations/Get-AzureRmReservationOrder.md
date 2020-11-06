---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
ms.openlocfilehash: 12e76c3412f54ba840528f9ff1a40acd388cd109
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480153"
---
# <span data-ttu-id="df7ff-101">Get-AzureRmReservationOrder</span><span class="sxs-lookup"><span data-stu-id="df7ff-101">Get-AzureRmReservationOrder</span></span>

## <span data-ttu-id="df7ff-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="df7ff-102">SYNOPSIS</span></span>
<span data-ttu-id="df7ff-103">Erhalten `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="df7ff-103">Get `ReservationOrder`</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df7ff-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="df7ff-104">SYNTAX</span></span>

```
Get-AzureRmReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df7ff-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="df7ff-105">DESCRIPTION</span></span>
<span data-ttu-id="df7ff-106">Liste aller `ReservationOrder` s, auf die der Benutzer im aktuellen Mandanten zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="df7ff-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="df7ff-107">Wenn der ReservationOrderId-Parameter festzulegen ist, rufen Sie diesen bestimmten ReservationOrder.</span><span class="sxs-lookup"><span data-stu-id="df7ff-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="df7ff-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="df7ff-108">EXAMPLES</span></span>

### <span data-ttu-id="df7ff-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="df7ff-109">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationOrder
```

<span data-ttu-id="df7ff-110">Listen Sie alle auf `ReservationOrder` , auf die der Benutzer im aktuellen Mandanten zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="df7ff-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="df7ff-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="df7ff-111">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="df7ff-112">Abrufen `ReservationOrder` mit dem angegebenen ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="df7ff-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="df7ff-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="df7ff-113">PARAMETERS</span></span>

### <span data-ttu-id="df7ff-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df7ff-114">-DefaultProfile</span></span>
<span data-ttu-id="df7ff-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="df7ff-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df7ff-116">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="df7ff-116">-ReservationOrderId</span></span>
<span data-ttu-id="df7ff-117">Die ID des spezifischen ReservationOrder, das der Benutzer anzeigen möchte</span><span class="sxs-lookup"><span data-stu-id="df7ff-117">Id of the specific ReservationOrder that user wants to see</span></span>

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

### <span data-ttu-id="df7ff-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df7ff-118">CommonParameters</span></span>
<span data-ttu-id="df7ff-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df7ff-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df7ff-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df7ff-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df7ff-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="df7ff-121">INPUTS</span></span>

### <span data-ttu-id="df7ff-122">Keine</span><span class="sxs-lookup"><span data-stu-id="df7ff-122">None</span></span>

## <span data-ttu-id="df7ff-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="df7ff-123">OUTPUTS</span></span>

### <span data-ttu-id="df7ff-124">Microsoft. Azure. Commands. reservations. Models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="df7ff-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

### <span data-ttu-id="df7ff-125">Microsoft. Azure. Commands. reservations. Models. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="df7ff-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="df7ff-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="df7ff-126">NOTES</span></span>

## <span data-ttu-id="df7ff-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="df7ff-127">RELATED LINKS</span></span>
