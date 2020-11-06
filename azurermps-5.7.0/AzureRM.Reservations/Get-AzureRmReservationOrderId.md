---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
ms.openlocfilehash: ce6132c7c9b782969b78094de4a055415f3f30ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482762"
---
# <span data-ttu-id="f821a-101">Get-AzureRmReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="f821a-101">Get-AzureRmReservationOrderId</span></span>

## <span data-ttu-id="f821a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f821a-102">SYNOPSIS</span></span>
<span data-ttu-id="f821a-103">Abrufen einer Liste der gültigen `ReservationOrder` IDs</span><span class="sxs-lookup"><span data-stu-id="f821a-103">Get list of applicable `ReservationOrder` Ids.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f821a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f821a-104">SYNTAX</span></span>

```
Get-AzureRmReservationOrderId [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="f821a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f821a-105">DESCRIPTION</span></span>
<span data-ttu-id="f821a-106">Abrufen von IDs des anwendbaren `ReservationOrder` s, die auf dieses Abonnement angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="f821a-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="f821a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f821a-107">EXAMPLES</span></span>

### <span data-ttu-id="f821a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f821a-108">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationOrderId
```

<span data-ttu-id="f821a-109">Abrufen `ReservationOrder` des Standardabonnements</span><span class="sxs-lookup"><span data-stu-id="f821a-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="f821a-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f821a-110">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="f821a-111">Abrufen `ReservationOrder` des angegebenen Abonnements</span><span class="sxs-lookup"><span data-stu-id="f821a-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="f821a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f821a-112">PARAMETERS</span></span>

### <span data-ttu-id="f821a-113">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="f821a-113">-SubscriptionId</span></span>
<span data-ttu-id="f821a-114">Die ID des Abonnements zum Abrufen des angewendeten `ReservationOrder` s</span><span class="sxs-lookup"><span data-stu-id="f821a-114">Id of the subscription to get the applied `ReservationOrder`s</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f821a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f821a-115">CommonParameters</span></span>
<span data-ttu-id="f821a-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f821a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f821a-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f821a-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f821a-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f821a-118">INPUTS</span></span>

### <span data-ttu-id="f821a-119">Keine</span><span class="sxs-lookup"><span data-stu-id="f821a-119">None</span></span>

## <span data-ttu-id="f821a-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f821a-120">OUTPUTS</span></span>

### <span data-ttu-id="f821a-121">Microsoft. Azure. Commands. reservations. Models. PSAppliedReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="f821a-121">Microsoft.Azure.Commands.Reservations.Models.PSAppliedReservationOrderId</span></span>

## <span data-ttu-id="f821a-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="f821a-122">NOTES</span></span>

## <span data-ttu-id="f821a-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f821a-123">RELATED LINKS</span></span>

