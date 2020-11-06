---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/merge-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Merge-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Merge-AzureRmReservation.md
ms.openlocfilehash: 1f5b0c6a743c9ed26864144cf8df21917bc2ac45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482765"
---
# <span data-ttu-id="8e9cb-101">Merge-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="8e9cb-101">Merge-AzureRmReservation</span></span>

## <span data-ttu-id="8e9cb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8e9cb-102">SYNOPSIS</span></span>
<span data-ttu-id="8e9cb-103">Verbindet zwei `Reservation` s.</span><span class="sxs-lookup"><span data-stu-id="8e9cb-103">Merges two `Reservation`s.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e9cb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e9cb-104">SYNTAX</span></span>

### <span data-ttu-id="8e9cb-105">CommandLine (Standard)</span><span class="sxs-lookup"><span data-stu-id="8e9cb-105">CommandLine (Default)</span></span>
```
Merge-AzureRmReservation -ReservationOrderId <String> -ReservationId <String[]> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e9cb-106">Pipeobject</span><span class="sxs-lookup"><span data-stu-id="8e9cb-106">PipeObject</span></span>
```
Merge-AzureRmReservation -Reservation <PSReservation[]> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e9cb-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e9cb-107">DESCRIPTION</span></span>
<span data-ttu-id="8e9cb-108">Zusammenführen der angegebenen `Reservation` s in eine neue `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="8e9cb-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="8e9cb-109">Die beiden `Reservation` s, die zusammengeführt werden, müssen die gleichen Eigenschaften aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8e9cb-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="8e9cb-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8e9cb-110">EXAMPLES</span></span>

### <span data-ttu-id="8e9cb-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8e9cb-111">Example 1</span></span>
```
PS C:\> Merge-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="8e9cb-112">Zusammenführen der beiden angegebenen `Reservation` s in einem `Reservation`</span><span class="sxs-lookup"><span data-stu-id="8e9cb-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="8e9cb-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e9cb-113">PARAMETERS</span></span>

### <span data-ttu-id="8e9cb-114">-Reservation</span><span class="sxs-lookup"><span data-stu-id="8e9cb-114">-Reservation</span></span>
<span data-ttu-id="8e9cb-115">Durch Kommas getrennte Zeichenfolgen von zwei ReservationIds, die zusammengeführt werden sollen</span><span class="sxs-lookup"><span data-stu-id="8e9cb-115">Comma-separated strings of two ReservationIds to merge</span></span>

```yaml
Type: PSReservation[]
Parameter Sets: PipeObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e9cb-116">-Reservierungs-Nr.</span><span class="sxs-lookup"><span data-stu-id="8e9cb-116">-ReservationId</span></span>
<span data-ttu-id="8e9cb-117">ReservationOrderId für die `ReservationOrder` , die die beiden `Reservation` s enthält</span><span class="sxs-lookup"><span data-stu-id="8e9cb-117">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

```yaml
Type: String[]
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e9cb-118">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="8e9cb-118">-ReservationOrderId</span></span>
<span data-ttu-id="8e9cb-119">{{Fill ReservationOrderId Description}}</span><span class="sxs-lookup"><span data-stu-id="8e9cb-119">{{Fill ReservationOrderId Description}}</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e9cb-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8e9cb-120">-Confirm</span></span>
<span data-ttu-id="8e9cb-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8e9cb-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e9cb-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e9cb-122">-WhatIf</span></span>
<span data-ttu-id="8e9cb-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8e9cb-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e9cb-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8e9cb-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e9cb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e9cb-125">CommonParameters</span></span>
<span data-ttu-id="8e9cb-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e9cb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e9cb-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e9cb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e9cb-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8e9cb-128">INPUTS</span></span>

### <span data-ttu-id="8e9cb-129">Microsoft. Azure. Commands. reservations. Models. PSReservation []</span><span class="sxs-lookup"><span data-stu-id="8e9cb-129">Microsoft.Azure.Commands.Reservations.Models.PSReservation[]</span></span>

## <span data-ttu-id="8e9cb-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8e9cb-130">OUTPUTS</span></span>

### <span data-ttu-id="8e9cb-131">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. reservations. Models. PSReservation, Microsoft. Azure. Commands. Reservations, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="8e9cb-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Reservations.Models.PSReservation, Microsoft.Azure.Commands.Reservations, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8e9cb-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="8e9cb-132">NOTES</span></span>

## <span data-ttu-id="8e9cb-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8e9cb-133">RELATED LINKS</span></span>

