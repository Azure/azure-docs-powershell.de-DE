---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
ms.openlocfilehash: 31cccc3c2bde38593bcc1b54d86940f07716a0db
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846812"
---
# <span data-ttu-id="5a7a7-101">Get-AzReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="5a7a7-101">Get-AzReservationOrderId</span></span>

## <span data-ttu-id="5a7a7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5a7a7-102">SYNOPSIS</span></span>
<span data-ttu-id="5a7a7-103">Abrufen einer Liste der gültigen `ReservationOrder` IDs</span><span class="sxs-lookup"><span data-stu-id="5a7a7-103">Get list of applicable `ReservationOrder` Ids.</span></span>

## <span data-ttu-id="5a7a7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a7a7-104">SYNTAX</span></span>

```
Get-AzReservationOrderId [-SubscriptionId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a7a7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a7a7-105">DESCRIPTION</span></span>
<span data-ttu-id="5a7a7-106">Abrufen von IDs des anwendbaren `ReservationOrder` s, die auf dieses Abonnement angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="5a7a7-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="5a7a7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5a7a7-107">EXAMPLES</span></span>

### <span data-ttu-id="5a7a7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5a7a7-108">Example 1</span></span>
```
PS C:\> Get-AzReservationOrderId
```

<span data-ttu-id="5a7a7-109">Abrufen `ReservationOrder` des Standardabonnements</span><span class="sxs-lookup"><span data-stu-id="5a7a7-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="5a7a7-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5a7a7-110">Example 2</span></span>
```
PS C:\> Get-AzReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="5a7a7-111">Abrufen `ReservationOrder` des angegebenen Abonnements</span><span class="sxs-lookup"><span data-stu-id="5a7a7-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="5a7a7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a7a7-112">PARAMETERS</span></span>

### <span data-ttu-id="5a7a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a7a7-113">-DefaultProfile</span></span>
<span data-ttu-id="5a7a7-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5a7a7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a7a7-115">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="5a7a7-115">-SubscriptionId</span></span>
<span data-ttu-id="5a7a7-116">Die ID des Abonnements zum Abrufen des angewendeten `ReservationOrder` s</span><span class="sxs-lookup"><span data-stu-id="5a7a7-116">Id of the subscription to get the applied `ReservationOrder`s</span></span>

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

### <span data-ttu-id="5a7a7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a7a7-117">CommonParameters</span></span>
<span data-ttu-id="5a7a7-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a7a7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a7a7-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a7a7-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a7a7-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5a7a7-120">INPUTS</span></span>

### <span data-ttu-id="5a7a7-121">Keine</span><span class="sxs-lookup"><span data-stu-id="5a7a7-121">None</span></span>

## <span data-ttu-id="5a7a7-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5a7a7-122">OUTPUTS</span></span>

### <span data-ttu-id="5a7a7-123">Microsoft. Azure. Management. reservations. Models. AppliedReservations</span><span class="sxs-lookup"><span data-stu-id="5a7a7-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span></span>

## <span data-ttu-id="5a7a7-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="5a7a7-124">NOTES</span></span>

## <span data-ttu-id="5a7a7-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5a7a7-125">RELATED LINKS</span></span>
