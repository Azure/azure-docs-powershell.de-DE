---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
ms.openlocfilehash: 1e60ca2ce1a845fa460e14a4e99b921fa4c085ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480149"
---
# <span data-ttu-id="df1c0-101">Get-AzureRmReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="df1c0-101">Get-AzureRmReservationOrderId</span></span>

## <span data-ttu-id="df1c0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="df1c0-102">SYNOPSIS</span></span>
<span data-ttu-id="df1c0-103">Abrufen einer Liste der gültigen `ReservationOrder` IDs</span><span class="sxs-lookup"><span data-stu-id="df1c0-103">Get list of applicable `ReservationOrder` Ids.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df1c0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="df1c0-104">SYNTAX</span></span>

```
Get-AzureRmReservationOrderId [-SubscriptionId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df1c0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="df1c0-105">DESCRIPTION</span></span>
<span data-ttu-id="df1c0-106">Abrufen von IDs des anwendbaren `ReservationOrder` s, die auf dieses Abonnement angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="df1c0-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="df1c0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="df1c0-107">EXAMPLES</span></span>

### <span data-ttu-id="df1c0-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="df1c0-108">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationOrderId
```

<span data-ttu-id="df1c0-109">Abrufen `ReservationOrder` des Standardabonnements</span><span class="sxs-lookup"><span data-stu-id="df1c0-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="df1c0-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="df1c0-110">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="df1c0-111">Abrufen `ReservationOrder` des angegebenen Abonnements</span><span class="sxs-lookup"><span data-stu-id="df1c0-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="df1c0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="df1c0-112">PARAMETERS</span></span>

### <span data-ttu-id="df1c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df1c0-113">-DefaultProfile</span></span>
<span data-ttu-id="df1c0-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="df1c0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df1c0-115">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="df1c0-115">-SubscriptionId</span></span>
<span data-ttu-id="df1c0-116">Die ID des Abonnements zum Abrufen des angewendeten `ReservationOrder` s</span><span class="sxs-lookup"><span data-stu-id="df1c0-116">Id of the subscription to get the applied `ReservationOrder`s</span></span>

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

### <span data-ttu-id="df1c0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df1c0-117">CommonParameters</span></span>
<span data-ttu-id="df1c0-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df1c0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df1c0-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df1c0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df1c0-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="df1c0-120">INPUTS</span></span>

### <span data-ttu-id="df1c0-121">Keine</span><span class="sxs-lookup"><span data-stu-id="df1c0-121">None</span></span>

## <span data-ttu-id="df1c0-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="df1c0-122">OUTPUTS</span></span>

### <span data-ttu-id="df1c0-123">Microsoft. Azure. Management. reservations. Models. AppliedReservations</span><span class="sxs-lookup"><span data-stu-id="df1c0-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span></span>

## <span data-ttu-id="df1c0-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="df1c0-124">NOTES</span></span>

## <span data-ttu-id="df1c0-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="df1c0-125">RELATED LINKS</span></span>
