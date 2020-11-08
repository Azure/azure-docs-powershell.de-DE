---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/merge-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
ms.openlocfilehash: fc0b04049184334c59a38226e031342fc29207b2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996013"
---
# <span data-ttu-id="46013-101">Merge-AzReservation</span><span class="sxs-lookup"><span data-stu-id="46013-101">Merge-AzReservation</span></span>

## <span data-ttu-id="46013-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46013-102">SYNOPSIS</span></span>
<span data-ttu-id="46013-103">Verbindet zwei `Reservation` s.</span><span class="sxs-lookup"><span data-stu-id="46013-103">Merges two `Reservation`s.</span></span>

## <span data-ttu-id="46013-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="46013-104">SYNTAX</span></span>

### <span data-ttu-id="46013-105">CommandLine (Standard)</span><span class="sxs-lookup"><span data-stu-id="46013-105">CommandLine (Default)</span></span>
```
Merge-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46013-106">Pipeobject</span><span class="sxs-lookup"><span data-stu-id="46013-106">PipeObject</span></span>
```
Merge-AzReservation -Reservation <PSReservation[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46013-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46013-107">DESCRIPTION</span></span>
<span data-ttu-id="46013-108">Zusammenführen der angegebenen `Reservation` s in eine neue `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="46013-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="46013-109">Die beiden `Reservation` s, die zusammengeführt werden, müssen die gleichen Eigenschaften aufweisen.</span><span class="sxs-lookup"><span data-stu-id="46013-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="46013-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46013-110">EXAMPLES</span></span>

### <span data-ttu-id="46013-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="46013-111">Example 1</span></span>
```
PS C:\> Merge-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="46013-112">Zusammenführen der beiden angegebenen `Reservation` s in einem `Reservation`</span><span class="sxs-lookup"><span data-stu-id="46013-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="46013-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="46013-113">PARAMETERS</span></span>

### <span data-ttu-id="46013-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46013-114">-DefaultProfile</span></span>
<span data-ttu-id="46013-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="46013-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46013-116">-Reservation</span><span class="sxs-lookup"><span data-stu-id="46013-116">-Reservation</span></span>
<span data-ttu-id="46013-117">Durch Kommas getrennte Zeichenfolgen von zwei ReservationIds, die zusammengeführt werden sollen</span><span class="sxs-lookup"><span data-stu-id="46013-117">Comma-separated strings of two ReservationIds to merge</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation[]
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46013-118">-Reservierungs-Nr.</span><span class="sxs-lookup"><span data-stu-id="46013-118">-ReservationId</span></span>
<span data-ttu-id="46013-119">ReservationOrderId für die `ReservationOrder` , die die beiden `Reservation` s enthält</span><span class="sxs-lookup"><span data-stu-id="46013-119">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

```yaml
Type: System.Guid[]
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46013-120">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="46013-120">-ReservationOrderId</span></span>
<span data-ttu-id="46013-121">{{Fill ReservationOrderId Description}}</span><span class="sxs-lookup"><span data-stu-id="46013-121">{{Fill ReservationOrderId Description}}</span></span>

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

### <span data-ttu-id="46013-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="46013-122">-Confirm</span></span>
<span data-ttu-id="46013-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46013-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46013-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46013-124">-WhatIf</span></span>
<span data-ttu-id="46013-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46013-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46013-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46013-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46013-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46013-127">CommonParameters</span></span>
<span data-ttu-id="46013-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46013-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46013-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46013-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46013-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46013-130">INPUTS</span></span>

### <span data-ttu-id="46013-131">Keine</span><span class="sxs-lookup"><span data-stu-id="46013-131">None</span></span>

## <span data-ttu-id="46013-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46013-132">OUTPUTS</span></span>

### <span data-ttu-id="46013-133">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="46013-133">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="46013-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="46013-134">NOTES</span></span>

## <span data-ttu-id="46013-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46013-135">RELATED LINKS</span></span>
