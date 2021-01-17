---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/split-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
ms.openlocfilehash: b879b5b47c752a331f0c2d70a6d37e57b113d816
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377976"
---
# <span data-ttu-id="09c7e-101">Split-AzReservation</span><span class="sxs-lookup"><span data-stu-id="09c7e-101">Split-AzReservation</span></span>

## <span data-ttu-id="09c7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09c7e-102">SYNOPSIS</span></span>
<span data-ttu-id="09c7e-103">Teilen `Reservation` eines</span><span class="sxs-lookup"><span data-stu-id="09c7e-103">Split a `Reservation`.</span></span>

## <span data-ttu-id="09c7e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09c7e-104">SYNTAX</span></span>

### <span data-ttu-id="09c7e-105">Befehlszeile (Standard)</span><span class="sxs-lookup"><span data-stu-id="09c7e-105">CommandLine (Default)</span></span>
```
Split-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -Quantity <Int32[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09c7e-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="09c7e-106">PipeObject</span></span>
```
Split-AzReservation -Quantity <Int32[]> -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09c7e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="09c7e-107">DESCRIPTION</span></span>
<span data-ttu-id="09c7e-108">Teilen Sie eine `Reservation` in zwei s mit einer `Reservation` bestimmten Mengenverteilung auf.</span><span class="sxs-lookup"><span data-stu-id="09c7e-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="09c7e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="09c7e-109">EXAMPLES</span></span>

### <span data-ttu-id="09c7e-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="09c7e-110">Example 1</span></span>
```
PS C:\> Split-AzReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="09c7e-111">Aufteilen der `Reservation` angegebenen `Reservation` Daten in zwei s mit den entsprechenden Mengen</span><span class="sxs-lookup"><span data-stu-id="09c7e-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="09c7e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09c7e-112">PARAMETERS</span></span>

### <span data-ttu-id="09c7e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09c7e-113">-DefaultProfile</span></span>
<span data-ttu-id="09c7e-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="09c7e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09c7e-115">-Quantity</span><span class="sxs-lookup"><span data-stu-id="09c7e-115">-Quantity</span></span>
<span data-ttu-id="09c7e-116">Durch Kommas getrennte ganze Zahlen für das Feld "Anzahl" der beiden `Reservation` Werte</span><span class="sxs-lookup"><span data-stu-id="09c7e-116">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

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

### <span data-ttu-id="09c7e-117">-Reservierung</span><span class="sxs-lookup"><span data-stu-id="09c7e-117">-Reservation</span></span>
<span data-ttu-id="09c7e-118">Objektparameter "Pipe" für `Reservation`</span><span class="sxs-lookup"><span data-stu-id="09c7e-118">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="09c7e-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="09c7e-119">-ReservationId</span></span>
<span data-ttu-id="09c7e-120">ID der zu `Reservation` teilende</span><span class="sxs-lookup"><span data-stu-id="09c7e-120">Id of the `Reservation` to split</span></span>

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

### <span data-ttu-id="09c7e-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="09c7e-121">-ReservationOrderId</span></span>
<span data-ttu-id="09c7e-122">ID der `ReservationOrder` Id, die den `Reservation` Benutzer enthält, der geteilt werden soll</span><span class="sxs-lookup"><span data-stu-id="09c7e-122">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

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

### <span data-ttu-id="09c7e-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09c7e-123">-Confirm</span></span>
<span data-ttu-id="09c7e-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="09c7e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09c7e-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="09c7e-125">-WhatIf</span></span>
<span data-ttu-id="09c7e-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="09c7e-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="09c7e-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="09c7e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09c7e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09c7e-128">CommonParameters</span></span>
<span data-ttu-id="09c7e-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09c7e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09c7e-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09c7e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09c7e-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="09c7e-131">INPUTS</span></span>

### <span data-ttu-id="09c7e-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="09c7e-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="09c7e-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="09c7e-133">OUTPUTS</span></span>

### <span data-ttu-id="09c7e-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="09c7e-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="09c7e-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="09c7e-135">NOTES</span></span>

## <span data-ttu-id="09c7e-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="09c7e-136">RELATED LINKS</span></span>
