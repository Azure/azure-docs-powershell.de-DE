---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/split-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
ms.openlocfilehash: 9ea53203bc07cca5ca5a8b7909f9fbab558e3c5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943649"
---
# <span data-ttu-id="ce02e-101">Split-AzReservation</span><span class="sxs-lookup"><span data-stu-id="ce02e-101">Split-AzReservation</span></span>

## <span data-ttu-id="ce02e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce02e-102">SYNOPSIS</span></span>
<span data-ttu-id="ce02e-103">Teilen Sie ein `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="ce02e-103">Split a `Reservation`.</span></span>

## <span data-ttu-id="ce02e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce02e-104">SYNTAX</span></span>

### <span data-ttu-id="ce02e-105">Befehlszeile (Standard)</span><span class="sxs-lookup"><span data-stu-id="ce02e-105">CommandLine (Default)</span></span>
```
Split-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -Quantity <Int32[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce02e-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="ce02e-106">PipeObject</span></span>
```
Split-AzReservation -Quantity <Int32[]> -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce02e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ce02e-107">DESCRIPTION</span></span>
<span data-ttu-id="ce02e-108">Teilen Sie `Reservation` ein in zwei s mit einer `Reservation` angegebenen Mengenverteilung auf.</span><span class="sxs-lookup"><span data-stu-id="ce02e-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="ce02e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ce02e-109">EXAMPLES</span></span>

### <span data-ttu-id="ce02e-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ce02e-110">Example 1</span></span>
```
PS C:\> Split-AzReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="ce02e-111">Aufteilen der `Reservation` angegebenen in `Reservation` zwei s mit den entsprechenden Mengen</span><span class="sxs-lookup"><span data-stu-id="ce02e-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="ce02e-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ce02e-112">PARAMETERS</span></span>

### <span data-ttu-id="ce02e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce02e-113">-DefaultProfile</span></span>
<span data-ttu-id="ce02e-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ce02e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce02e-115">-Quantity</span><span class="sxs-lookup"><span data-stu-id="ce02e-115">-Quantity</span></span>
<span data-ttu-id="ce02e-116">Durch Kommas getrennte ganze Zahlen für das Mengenfeld der beiden `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="ce02e-116">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

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

### <span data-ttu-id="ce02e-117">-Reservierung</span><span class="sxs-lookup"><span data-stu-id="ce02e-117">-Reservation</span></span>
<span data-ttu-id="ce02e-118">Parameter des Pipeobjekts für `Reservation`</span><span class="sxs-lookup"><span data-stu-id="ce02e-118">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="ce02e-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="ce02e-119">-ReservationId</span></span>
<span data-ttu-id="ce02e-120">ID des `Reservation` zu teilen</span><span class="sxs-lookup"><span data-stu-id="ce02e-120">Id of the `Reservation` to split</span></span>

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

### <span data-ttu-id="ce02e-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="ce02e-121">-ReservationOrderId</span></span>
<span data-ttu-id="ce02e-122">ID des `ReservationOrder` -Kontos, das den `Reservation` Benutzer enthält, der geteilt werden soll</span><span class="sxs-lookup"><span data-stu-id="ce02e-122">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

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

### <span data-ttu-id="ce02e-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ce02e-123">-Confirm</span></span>
<span data-ttu-id="ce02e-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ce02e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce02e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce02e-125">-WhatIf</span></span>
<span data-ttu-id="ce02e-126">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ce02e-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ce02e-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ce02e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce02e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce02e-128">CommonParameters</span></span>
<span data-ttu-id="ce02e-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce02e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce02e-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce02e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce02e-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ce02e-131">INPUTS</span></span>

### <span data-ttu-id="ce02e-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="ce02e-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="ce02e-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ce02e-133">OUTPUTS</span></span>

### <span data-ttu-id="ce02e-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="ce02e-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="ce02e-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ce02e-135">NOTES</span></span>

## <span data-ttu-id="ce02e-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ce02e-136">RELATED LINKS</span></span>
