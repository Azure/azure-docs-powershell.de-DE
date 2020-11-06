---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
ms.openlocfilehash: 75ff92efe1a37e55396da7dc6d644408952ed179
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500433"
---
# <span data-ttu-id="c4702-101">Get-AzureRmReservationHistory</span><span class="sxs-lookup"><span data-stu-id="c4702-101">Get-AzureRmReservationHistory</span></span>

## <span data-ttu-id="c4702-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c4702-102">SYNOPSIS</span></span>
<span data-ttu-id="c4702-103">Abrufen des `Reservation` Versionsverlaufs</span><span class="sxs-lookup"><span data-stu-id="c4702-103">Get `Reservation` revision history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4702-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4702-104">SYNTAX</span></span>

### <span data-ttu-id="c4702-105">CommandLine (Standard)</span><span class="sxs-lookup"><span data-stu-id="c4702-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservationHistory -ReservationOrderId <String> -ReservationId <String> [<CommonParameters>]
```

### <span data-ttu-id="c4702-106">Pipeobject</span><span class="sxs-lookup"><span data-stu-id="c4702-106">PipeObject</span></span>
```
Get-AzureRmReservationHistory -Reservation <PSReservation> [<CommonParameters>]
```

## <span data-ttu-id="c4702-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4702-107">DESCRIPTION</span></span>
<span data-ttu-id="c4702-108">Liste aller Überarbeitungen für die `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="c4702-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="c4702-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4702-109">EXAMPLES</span></span>

### <span data-ttu-id="c4702-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c4702-110">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="c4702-111">Abrufen des Versionsverlaufs der jeweiligen Reservierung</span><span class="sxs-lookup"><span data-stu-id="c4702-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="c4702-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4702-112">PARAMETERS</span></span>

### <span data-ttu-id="c4702-113">-Reservation</span><span class="sxs-lookup"><span data-stu-id="c4702-113">-Reservation</span></span>
<span data-ttu-id="c4702-114">Pipe-Objektparameter für `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="c4702-114">Pipe object parameter for `Reservation`s</span></span>

```yaml
Type: PSReservation
Parameter Sets: PipeObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4702-115">-Reservierungs-Nr.</span><span class="sxs-lookup"><span data-stu-id="c4702-115">-ReservationId</span></span>
<span data-ttu-id="c4702-116">Reservierungs-Nr. des `Reservation` Verlaufs, der angezeigt werden soll</span><span class="sxs-lookup"><span data-stu-id="c4702-116">ReservationId of the `Reservation` of which history is to be shown</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4702-117">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="c4702-117">-ReservationOrderId</span></span>
<span data-ttu-id="c4702-118">ReservationOrderId für das `ReservationOrder` , das die `Reservation`</span><span class="sxs-lookup"><span data-stu-id="c4702-118">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4702-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4702-119">CommonParameters</span></span>
<span data-ttu-id="c4702-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4702-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4702-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4702-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4702-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c4702-122">INPUTS</span></span>

### <span data-ttu-id="c4702-123">System. String</span><span class="sxs-lookup"><span data-stu-id="c4702-123">System.String</span></span>
<span data-ttu-id="c4702-124">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="c4702-124">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="c4702-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c4702-125">OUTPUTS</span></span>

### <span data-ttu-id="c4702-126">Microsoft. Azure. Commands. reservations. Models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="c4702-126">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="c4702-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="c4702-127">NOTES</span></span>

## <span data-ttu-id="c4702-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c4702-128">RELATED LINKS</span></span>

