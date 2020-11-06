---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
ms.openlocfilehash: 3149e2fa0ef748d11583919161555805d54f5efc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505730"
---
# <span data-ttu-id="97b7f-101">Get-AzureRmReservationHistory</span><span class="sxs-lookup"><span data-stu-id="97b7f-101">Get-AzureRmReservationHistory</span></span>

## <span data-ttu-id="97b7f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="97b7f-102">SYNOPSIS</span></span>
<span data-ttu-id="97b7f-103">Abrufen des `Reservation` Versionsverlaufs</span><span class="sxs-lookup"><span data-stu-id="97b7f-103">Get `Reservation` revision history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97b7f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="97b7f-104">SYNTAX</span></span>

### <span data-ttu-id="97b7f-105">CommandLine (Standard)</span><span class="sxs-lookup"><span data-stu-id="97b7f-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservationHistory -ReservationOrderId <Guid> -ReservationId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97b7f-106">Pipeobject</span><span class="sxs-lookup"><span data-stu-id="97b7f-106">PipeObject</span></span>
```
Get-AzureRmReservationHistory -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="97b7f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="97b7f-107">DESCRIPTION</span></span>
<span data-ttu-id="97b7f-108">Liste aller Überarbeitungen für die `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="97b7f-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="97b7f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="97b7f-109">EXAMPLES</span></span>

### <span data-ttu-id="97b7f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="97b7f-110">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="97b7f-111">Abrufen des Versionsverlaufs der jeweiligen Reservierung</span><span class="sxs-lookup"><span data-stu-id="97b7f-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="97b7f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="97b7f-112">PARAMETERS</span></span>

### <span data-ttu-id="97b7f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97b7f-113">-DefaultProfile</span></span>
<span data-ttu-id="97b7f-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="97b7f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97b7f-115">-Reservation</span><span class="sxs-lookup"><span data-stu-id="97b7f-115">-Reservation</span></span>
<span data-ttu-id="97b7f-116">Pipe-Objektparameter für `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="97b7f-116">Pipe object parameter for `Reservation`s</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97b7f-117">-Reservierungs-Nr.</span><span class="sxs-lookup"><span data-stu-id="97b7f-117">-ReservationId</span></span>
<span data-ttu-id="97b7f-118">Reservierungs-Nr. des `Reservation` Verlaufs, der angezeigt werden soll</span><span class="sxs-lookup"><span data-stu-id="97b7f-118">ReservationId of the `Reservation` of which history is to be shown</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97b7f-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="97b7f-119">-ReservationOrderId</span></span>
<span data-ttu-id="97b7f-120">ReservationOrderId für das `ReservationOrder` , das die `Reservation`</span><span class="sxs-lookup"><span data-stu-id="97b7f-120">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97b7f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97b7f-121">CommonParameters</span></span>
<span data-ttu-id="97b7f-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97b7f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97b7f-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97b7f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97b7f-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="97b7f-124">INPUTS</span></span>

### <span data-ttu-id="97b7f-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="97b7f-125">System.Guid</span></span>

### <span data-ttu-id="97b7f-126">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="97b7f-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>
<span data-ttu-id="97b7f-127">Parameter: Reservierung (ByValue)</span><span class="sxs-lookup"><span data-stu-id="97b7f-127">Parameters: Reservation (ByValue)</span></span>

## <span data-ttu-id="97b7f-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="97b7f-128">OUTPUTS</span></span>

### <span data-ttu-id="97b7f-129">Microsoft. Azure. Commands. reservations. Models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="97b7f-129">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="97b7f-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="97b7f-130">NOTES</span></span>

## <span data-ttu-id="97b7f-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="97b7f-131">RELATED LINKS</span></span>
