---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/merge-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
ms.openlocfilehash: fc0b04049184334c59a38226e031342fc29207b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143676"
---
# <span data-ttu-id="d37e1-101">Merge-AzReservation</span><span class="sxs-lookup"><span data-stu-id="d37e1-101">Merge-AzReservation</span></span>

## <span data-ttu-id="d37e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d37e1-102">SYNOPSIS</span></span>
<span data-ttu-id="d37e1-103">Führt zwei `Reservation` Zellen zusammen.</span><span class="sxs-lookup"><span data-stu-id="d37e1-103">Merges two `Reservation`s.</span></span>

## <span data-ttu-id="d37e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d37e1-104">SYNTAX</span></span>

### <span data-ttu-id="d37e1-105">Befehlszeile (Standard)</span><span class="sxs-lookup"><span data-stu-id="d37e1-105">CommandLine (Default)</span></span>
```
Merge-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d37e1-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="d37e1-106">PipeObject</span></span>
```
Merge-AzReservation -Reservation <PSReservation[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d37e1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d37e1-107">DESCRIPTION</span></span>
<span data-ttu-id="d37e1-108">Führen Sie die `Reservation` angegebenen S in einem neuen `Reservation` zusammen.</span><span class="sxs-lookup"><span data-stu-id="d37e1-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="d37e1-109">Die beiden `Reservation` zusammengeführten Daten müssen über die gleichen Eigenschaften verfügen.</span><span class="sxs-lookup"><span data-stu-id="d37e1-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="d37e1-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d37e1-110">EXAMPLES</span></span>

### <span data-ttu-id="d37e1-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d37e1-111">Example 1</span></span>
```
PS C:\> Merge-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="d37e1-112">Zusammenführen der beiden `Reservation` angegebenen Daten in einem `Reservation`</span><span class="sxs-lookup"><span data-stu-id="d37e1-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="d37e1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d37e1-113">PARAMETERS</span></span>

### <span data-ttu-id="d37e1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d37e1-114">-DefaultProfile</span></span>
<span data-ttu-id="d37e1-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d37e1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d37e1-116">-Reservierung</span><span class="sxs-lookup"><span data-stu-id="d37e1-116">-Reservation</span></span>
<span data-ttu-id="d37e1-117">Durch Kommas getrennte Zeichenfolgen von zwei zu zusammenführenden Reservierungs-Ids</span><span class="sxs-lookup"><span data-stu-id="d37e1-117">Comma-separated strings of two ReservationIds to merge</span></span>

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

### <span data-ttu-id="d37e1-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="d37e1-118">-ReservationId</span></span>
<span data-ttu-id="d37e1-119">ReservationOrderId für `ReservationOrder` das, das die beiden `Reservation` Elemente enthält</span><span class="sxs-lookup"><span data-stu-id="d37e1-119">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

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

### <span data-ttu-id="d37e1-120">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="d37e1-120">-ReservationOrderId</span></span>
<span data-ttu-id="d37e1-121">{{Fill ReservationOrderId Description}}</span><span class="sxs-lookup"><span data-stu-id="d37e1-121">{{Fill ReservationOrderId Description}}</span></span>

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

### <span data-ttu-id="d37e1-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d37e1-122">-Confirm</span></span>
<span data-ttu-id="d37e1-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d37e1-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d37e1-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d37e1-124">-WhatIf</span></span>
<span data-ttu-id="d37e1-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d37e1-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d37e1-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d37e1-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d37e1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d37e1-127">CommonParameters</span></span>
<span data-ttu-id="d37e1-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d37e1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d37e1-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d37e1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d37e1-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d37e1-130">INPUTS</span></span>

### <span data-ttu-id="d37e1-131">Keine</span><span class="sxs-lookup"><span data-stu-id="d37e1-131">None</span></span>

## <span data-ttu-id="d37e1-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d37e1-132">OUTPUTS</span></span>

### <span data-ttu-id="d37e1-133">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="d37e1-133">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="d37e1-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d37e1-134">NOTES</span></span>

## <span data-ttu-id="d37e1-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d37e1-135">RELATED LINKS</span></span>
