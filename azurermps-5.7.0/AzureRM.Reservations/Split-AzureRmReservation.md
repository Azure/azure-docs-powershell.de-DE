---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/split-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
ms.openlocfilehash: 89c19f2c61604f3c38ba8cc9679f956d68df3179
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482766"
---
# <span data-ttu-id="469c0-101">Split-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="469c0-101">Split-AzureRmReservation</span></span>

## <span data-ttu-id="469c0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="469c0-102">SYNOPSIS</span></span>
<span data-ttu-id="469c0-103">Split a `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="469c0-103">Split a `Reservation`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="469c0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="469c0-104">SYNTAX</span></span>

### <span data-ttu-id="469c0-105">CommandLine (Standard)</span><span class="sxs-lookup"><span data-stu-id="469c0-105">CommandLine (Default)</span></span>
```
Split-AzureRmReservation -ReservationOrderId <String> -ReservationId <String> -Quantity <Nullable`1[]>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="469c0-106">Pipeobject</span><span class="sxs-lookup"><span data-stu-id="469c0-106">PipeObject</span></span>
```
Split-AzureRmReservation -Quantity <Nullable`1[]> -Reservation <PSReservation> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="469c0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="469c0-107">DESCRIPTION</span></span>
<span data-ttu-id="469c0-108">Teilen Sie eine `Reservation` in zwei `Reservation` s mit der angegebenen Mengenverteilung.</span><span class="sxs-lookup"><span data-stu-id="469c0-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="469c0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="469c0-109">EXAMPLES</span></span>

### <span data-ttu-id="469c0-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="469c0-110">Example 1</span></span>
```
PS C:\> Split-AzureRmReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="469c0-111">Teilen des angegebenen `Reservation` in zwei `Reservation` s mit den entsprechenden Mengen</span><span class="sxs-lookup"><span data-stu-id="469c0-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="469c0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="469c0-112">PARAMETERS</span></span>

### <span data-ttu-id="469c0-113">-Quantity</span><span class="sxs-lookup"><span data-stu-id="469c0-113">-Quantity</span></span>
<span data-ttu-id="469c0-114">Durch Kommas getrennte ganze Zahlen für das Feld "Menge" der beiden `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="469c0-114">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

```yaml
Type: Nullable`1[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="469c0-115">-Reservation</span><span class="sxs-lookup"><span data-stu-id="469c0-115">-Reservation</span></span>
<span data-ttu-id="469c0-116">Pipe-Objektparameter für `Reservation`</span><span class="sxs-lookup"><span data-stu-id="469c0-116">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="469c0-117">-Reservierungs-Nr.</span><span class="sxs-lookup"><span data-stu-id="469c0-117">-ReservationId</span></span>
<span data-ttu-id="469c0-118">ID der `Reservation` to-Teilung</span><span class="sxs-lookup"><span data-stu-id="469c0-118">Id of the `Reservation` to split</span></span>

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

### <span data-ttu-id="469c0-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="469c0-119">-ReservationOrderId</span></span>
<span data-ttu-id="469c0-120">Die ID des `ReservationOrder` Benutzers, der den `Reservation` Benutzer teilen möchte</span><span class="sxs-lookup"><span data-stu-id="469c0-120">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

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

### <span data-ttu-id="469c0-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="469c0-121">-Confirm</span></span>
<span data-ttu-id="469c0-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="469c0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="469c0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="469c0-123">-WhatIf</span></span>
<span data-ttu-id="469c0-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="469c0-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="469c0-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="469c0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="469c0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="469c0-126">CommonParameters</span></span>
<span data-ttu-id="469c0-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="469c0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="469c0-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="469c0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="469c0-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="469c0-129">INPUTS</span></span>

### <span data-ttu-id="469c0-130">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="469c0-130">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="469c0-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="469c0-131">OUTPUTS</span></span>

### <span data-ttu-id="469c0-132">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. reservations. Models. PSReservation, Microsoft. Azure. Commands. Reservations, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="469c0-132">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Reservations.Models.PSReservation, Microsoft.Azure.Commands.Reservations, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="469c0-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="469c0-133">NOTES</span></span>

## <span data-ttu-id="469c0-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="469c0-134">RELATED LINKS</span></span>

