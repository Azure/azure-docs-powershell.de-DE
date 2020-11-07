---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
ms.openlocfilehash: c969d24a894165e23628b91cda640f676ec3f3d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825087"
---
# <span data-ttu-id="19dd5-101">Get-AzReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="19dd5-101">Get-AzReservationOrderId</span></span>

## <span data-ttu-id="19dd5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="19dd5-102">SYNOPSIS</span></span>
<span data-ttu-id="19dd5-103">Abrufen einer Liste der gültigen `ReservationOrder` IDs</span><span class="sxs-lookup"><span data-stu-id="19dd5-103">Get list of applicable `ReservationOrder` Ids.</span></span>

## <span data-ttu-id="19dd5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="19dd5-104">SYNTAX</span></span>

```
Get-AzReservationOrderId [-SubscriptionId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="19dd5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="19dd5-105">DESCRIPTION</span></span>
<span data-ttu-id="19dd5-106">Abrufen von IDs des anwendbaren `ReservationOrder` s, die auf dieses Abonnement angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="19dd5-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="19dd5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="19dd5-107">EXAMPLES</span></span>

### <span data-ttu-id="19dd5-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="19dd5-108">Example 1</span></span>
```
PS C:\> Get-AzReservationOrderId
```

<span data-ttu-id="19dd5-109">Abrufen `ReservationOrder` des Standardabonnements</span><span class="sxs-lookup"><span data-stu-id="19dd5-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="19dd5-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="19dd5-110">Example 2</span></span>
```
PS C:\> Get-AzReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="19dd5-111">Abrufen `ReservationOrder` des angegebenen Abonnements</span><span class="sxs-lookup"><span data-stu-id="19dd5-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="19dd5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="19dd5-112">PARAMETERS</span></span>

### <span data-ttu-id="19dd5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19dd5-113">-DefaultProfile</span></span>
<span data-ttu-id="19dd5-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="19dd5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19dd5-115">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="19dd5-115">-SubscriptionId</span></span>
<span data-ttu-id="19dd5-116">Die ID des Abonnements zum Abrufen des angewendeten `ReservationOrder` s</span><span class="sxs-lookup"><span data-stu-id="19dd5-116">Id of the subscription to get the applied `ReservationOrder`s</span></span>

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

### <span data-ttu-id="19dd5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19dd5-117">CommonParameters</span></span>
<span data-ttu-id="19dd5-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19dd5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19dd5-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19dd5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19dd5-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="19dd5-120">INPUTS</span></span>

### <span data-ttu-id="19dd5-121">Keine</span><span class="sxs-lookup"><span data-stu-id="19dd5-121">None</span></span>

## <span data-ttu-id="19dd5-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="19dd5-122">OUTPUTS</span></span>

### <span data-ttu-id="19dd5-123">Microsoft. Azure. Management. reservations. Models. AppliedReservations</span><span class="sxs-lookup"><span data-stu-id="19dd5-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span></span>

## <span data-ttu-id="19dd5-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="19dd5-124">NOTES</span></span>

## <span data-ttu-id="19dd5-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="19dd5-125">RELATED LINKS</span></span>
