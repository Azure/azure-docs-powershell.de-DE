---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/split-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
ms.openlocfilehash: b879b5b47c752a331f0c2d70a6d37e57b113d816
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996559"
---
# <span data-ttu-id="6d9a9-101">Split-AzReservation</span><span class="sxs-lookup"><span data-stu-id="6d9a9-101">Split-AzReservation</span></span>

## <span data-ttu-id="6d9a9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6d9a9-102">SYNOPSIS</span></span>
<span data-ttu-id="6d9a9-103">Split a `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="6d9a9-103">Split a `Reservation`.</span></span>

## <span data-ttu-id="6d9a9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d9a9-104">SYNTAX</span></span>

### <span data-ttu-id="6d9a9-105">CommandLine (Standard)</span><span class="sxs-lookup"><span data-stu-id="6d9a9-105">CommandLine (Default)</span></span>
```
Split-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -Quantity <Int32[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d9a9-106">Pipeobject</span><span class="sxs-lookup"><span data-stu-id="6d9a9-106">PipeObject</span></span>
```
Split-AzReservation -Quantity <Int32[]> -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d9a9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6d9a9-107">DESCRIPTION</span></span>
<span data-ttu-id="6d9a9-108">Teilen Sie eine `Reservation` in zwei `Reservation` s mit der angegebenen Mengenverteilung.</span><span class="sxs-lookup"><span data-stu-id="6d9a9-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="6d9a9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6d9a9-109">EXAMPLES</span></span>

### <span data-ttu-id="6d9a9-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6d9a9-110">Example 1</span></span>
```
PS C:\> Split-AzReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="6d9a9-111">Teilen des angegebenen `Reservation` in zwei `Reservation` s mit den entsprechenden Mengen</span><span class="sxs-lookup"><span data-stu-id="6d9a9-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="6d9a9-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d9a9-112">PARAMETERS</span></span>

### <span data-ttu-id="6d9a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d9a9-113">-DefaultProfile</span></span>
<span data-ttu-id="6d9a9-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6d9a9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d9a9-115">-Quantity</span><span class="sxs-lookup"><span data-stu-id="6d9a9-115">-Quantity</span></span>
<span data-ttu-id="6d9a9-116">Durch Kommas getrennte ganze Zahlen für das Feld "Menge" der beiden `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="6d9a9-116">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d9a9-117">-Reservation</span><span class="sxs-lookup"><span data-stu-id="6d9a9-117">-Reservation</span></span>
<span data-ttu-id="6d9a9-118">Pipe-Objektparameter für `Reservation`</span><span class="sxs-lookup"><span data-stu-id="6d9a9-118">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="6d9a9-119">-Reservierungs-Nr.</span><span class="sxs-lookup"><span data-stu-id="6d9a9-119">-ReservationId</span></span>
<span data-ttu-id="6d9a9-120">ID der `Reservation` to-Teilung</span><span class="sxs-lookup"><span data-stu-id="6d9a9-120">Id of the `Reservation` to split</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d9a9-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="6d9a9-121">-ReservationOrderId</span></span>
<span data-ttu-id="6d9a9-122">Die ID des `ReservationOrder` Benutzers, der den `Reservation` Benutzer teilen möchte</span><span class="sxs-lookup"><span data-stu-id="6d9a9-122">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d9a9-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6d9a9-123">-Confirm</span></span>
<span data-ttu-id="6d9a9-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6d9a9-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d9a9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d9a9-125">-WhatIf</span></span>
<span data-ttu-id="6d9a9-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6d9a9-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6d9a9-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6d9a9-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d9a9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d9a9-128">CommonParameters</span></span>
<span data-ttu-id="6d9a9-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d9a9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d9a9-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d9a9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d9a9-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6d9a9-131">INPUTS</span></span>

### <span data-ttu-id="6d9a9-132">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="6d9a9-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="6d9a9-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6d9a9-133">OUTPUTS</span></span>

### <span data-ttu-id="6d9a9-134">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="6d9a9-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="6d9a9-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="6d9a9-135">NOTES</span></span>

## <span data-ttu-id="6d9a9-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6d9a9-136">RELATED LINKS</span></span>
