---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
ms.openlocfilehash: 31cccc3c2bde38593bcc1b54d86940f07716a0db
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370080"
---
# <span data-ttu-id="0e52e-101">Get-AzReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="0e52e-101">Get-AzReservationOrderId</span></span>

## <span data-ttu-id="0e52e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e52e-102">SYNOPSIS</span></span>
<span data-ttu-id="0e52e-103">Hier finden Sie eine Liste der `ReservationOrder` anwendbaren IDs.</span><span class="sxs-lookup"><span data-stu-id="0e52e-103">Get list of applicable `ReservationOrder` Ids.</span></span>

## <span data-ttu-id="0e52e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0e52e-104">SYNTAX</span></span>

```
Get-AzReservationOrderId [-SubscriptionId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0e52e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0e52e-105">DESCRIPTION</span></span>
<span data-ttu-id="0e52e-106">Erhalten Sie ids of applicable `ReservationOrder` s, die auf dieses Abonnement angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="0e52e-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="0e52e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0e52e-107">EXAMPLES</span></span>

### <span data-ttu-id="0e52e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0e52e-108">Example 1</span></span>
```
PS C:\> Get-AzReservationOrderId
```

<span data-ttu-id="0e52e-109">Angewendet für `ReservationOrder` Standardabonnement</span><span class="sxs-lookup"><span data-stu-id="0e52e-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="0e52e-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0e52e-110">Example 2</span></span>
```
PS C:\> Get-AzReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="0e52e-111">Für `ReservationOrder` angegebenes Abonnement angewendet werden</span><span class="sxs-lookup"><span data-stu-id="0e52e-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="0e52e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e52e-112">PARAMETERS</span></span>

### <span data-ttu-id="0e52e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e52e-113">-DefaultProfile</span></span>
<span data-ttu-id="0e52e-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0e52e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e52e-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0e52e-115">-SubscriptionId</span></span>
<span data-ttu-id="0e52e-116">ID des Abonnements, um die angewendeten S `ReservationOrder` zu erhalten</span><span class="sxs-lookup"><span data-stu-id="0e52e-116">Id of the subscription to get the applied `ReservationOrder`s</span></span>

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

### <span data-ttu-id="0e52e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e52e-117">CommonParameters</span></span>
<span data-ttu-id="0e52e-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e52e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e52e-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e52e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e52e-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0e52e-120">INPUTS</span></span>

### <span data-ttu-id="0e52e-121">Keine</span><span class="sxs-lookup"><span data-stu-id="0e52e-121">None</span></span>

## <span data-ttu-id="0e52e-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0e52e-122">OUTPUTS</span></span>

### <span data-ttu-id="0e52e-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span><span class="sxs-lookup"><span data-stu-id="0e52e-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span></span>

## <span data-ttu-id="0e52e-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0e52e-124">NOTES</span></span>

## <span data-ttu-id="0e52e-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0e52e-125">RELATED LINKS</span></span>
