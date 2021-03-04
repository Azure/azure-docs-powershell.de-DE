---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/get-azreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
ms.openlocfilehash: 9783d1ff8d3a42d3ad6627abcaae792f966b7828
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943685"
---
# <span data-ttu-id="359c9-101">Get-AzReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="359c9-101">Get-AzReservationOrderId</span></span>

## <span data-ttu-id="359c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="359c9-102">SYNOPSIS</span></span>
<span data-ttu-id="359c9-103">Hier finden Sie eine Liste der `ReservationOrder` anwendbaren Ids.</span><span class="sxs-lookup"><span data-stu-id="359c9-103">Get list of applicable `ReservationOrder` Ids.</span></span>

## <span data-ttu-id="359c9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="359c9-104">SYNTAX</span></span>

```
Get-AzReservationOrderId [-SubscriptionId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="359c9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="359c9-105">DESCRIPTION</span></span>
<span data-ttu-id="359c9-106">Holen Sie sich ids der `ReservationOrder` anwendbaren s, die auf dieses Abonnement angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="359c9-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="359c9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="359c9-107">EXAMPLES</span></span>

### <span data-ttu-id="359c9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="359c9-108">Example 1</span></span>
```
PS C:\> Get-AzReservationOrderId
```

<span data-ttu-id="359c9-109">Für `ReservationOrder` Standardabonnement angewendet</span><span class="sxs-lookup"><span data-stu-id="359c9-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="359c9-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="359c9-110">Example 2</span></span>
```
PS C:\> Get-AzReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="359c9-111">Für `ReservationOrder` angegebenes Abonnement angewendet werden</span><span class="sxs-lookup"><span data-stu-id="359c9-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="359c9-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="359c9-112">PARAMETERS</span></span>

### <span data-ttu-id="359c9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="359c9-113">-DefaultProfile</span></span>
<span data-ttu-id="359c9-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="359c9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="359c9-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="359c9-115">-SubscriptionId</span></span>
<span data-ttu-id="359c9-116">ID des Abonnements, um die angewendeten s zu `ReservationOrder` erhalten</span><span class="sxs-lookup"><span data-stu-id="359c9-116">Id of the subscription to get the applied `ReservationOrder`s</span></span>

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

### <span data-ttu-id="359c9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="359c9-117">CommonParameters</span></span>
<span data-ttu-id="359c9-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="359c9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="359c9-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="359c9-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="359c9-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="359c9-120">INPUTS</span></span>

### <span data-ttu-id="359c9-121">Keine</span><span class="sxs-lookup"><span data-stu-id="359c9-121">None</span></span>

## <span data-ttu-id="359c9-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="359c9-122">OUTPUTS</span></span>

### <span data-ttu-id="359c9-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span><span class="sxs-lookup"><span data-stu-id="359c9-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span></span>

## <span data-ttu-id="359c9-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="359c9-124">NOTES</span></span>

## <span data-ttu-id="359c9-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="359c9-125">RELATED LINKS</span></span>
