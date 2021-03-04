---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/update-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
ms.openlocfilehash: b93dd1462bb019b12fe761e0bdd6cc4172c01b89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943654"
---
# <span data-ttu-id="a06df-101">Update-AzReservation</span><span class="sxs-lookup"><span data-stu-id="a06df-101">Update-AzReservation</span></span>

## <span data-ttu-id="a06df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a06df-102">SYNOPSIS</span></span>
<span data-ttu-id="a06df-103">Aktualisieren eines `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="a06df-103">Update a `Reservation`.</span></span>

## <span data-ttu-id="a06df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a06df-104">SYNTAX</span></span>

### <span data-ttu-id="a06df-105">Befehlszeile (Standard)</span><span class="sxs-lookup"><span data-stu-id="a06df-105">CommandLine (Default)</span></span>
```
Update-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -AppliedScopeType <String>
 [-AppliedScope <String>] [-InstanceFlexibility <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a06df-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="a06df-106">PipeObject</span></span>
```
Update-AzReservation -AppliedScopeType <String> [-AppliedScope <String>] [-InstanceFlexibility <String>]
 -Reservation <PSReservation> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a06df-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a06df-107">DESCRIPTION</span></span>
<span data-ttu-id="a06df-108">Aktualisiert die angewendeten Bereiche der `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="a06df-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="a06df-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a06df-109">EXAMPLES</span></span>

### <span data-ttu-id="a06df-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a06df-110">Example 1</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff" -InstanceFlexibility "On"
```

<span data-ttu-id="a06df-111">Aktualisiert den AppliedScopeType des angegebenen `Reservation` auf Single und InstanceFlexibility auf Ein.</span><span class="sxs-lookup"><span data-stu-id="a06df-111">Updates the AppliedScopeType of the specified `Reservation` to Single and InstanceFlexibility to On.</span></span>

### <span data-ttu-id="a06df-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a06df-112">Example 2</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared" -InstanceFlexibility "Off"
```

<span data-ttu-id="a06df-113">Aktualisiert den AppliedScopeType des angegebenen `Reservation` auf Freigegeben und InstanzFlexibility auf Aus.</span><span class="sxs-lookup"><span data-stu-id="a06df-113">Updates the AppliedScopeType of the specified `Reservation` to Shared and InstanceFlexibility to Off.</span></span>

## <span data-ttu-id="a06df-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a06df-114">PARAMETERS</span></span>

### <span data-ttu-id="a06df-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="a06df-115">-AppliedScope</span></span>
<span data-ttu-id="a06df-116">SubscriptionId für `Reservation` diese Anwendung</span><span class="sxs-lookup"><span data-stu-id="a06df-116">SubscriptionId for this `Reservation` to be applied</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a06df-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="a06df-117">-AppliedScopeType</span></span>
<span data-ttu-id="a06df-118">Typ des angewendeten Bereichs</span><span class="sxs-lookup"><span data-stu-id="a06df-118">Type of the Applied Scope</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a06df-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a06df-119">-DefaultProfile</span></span>
<span data-ttu-id="a06df-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a06df-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a06df-121">-InstanzFlexibilität</span><span class="sxs-lookup"><span data-stu-id="a06df-121">-InstanceFlexibility</span></span>
<span data-ttu-id="a06df-122">Wenn vorhanden, aktualisiert der Wert "InstanzFlexibility" der `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="a06df-122">If present, updates the InstanceFlexibility value of the `Reservation`.</span></span> <span data-ttu-id="a06df-123">Wenn nicht angegeben, bleibt der vorhandene Wert unverändert.</span><span class="sxs-lookup"><span data-stu-id="a06df-123">If not specified, the existing value remains unchanged.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a06df-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a06df-124">-Name</span></span>
<span data-ttu-id="a06df-125">Name der Reservierung</span><span class="sxs-lookup"><span data-stu-id="a06df-125">Name of Reservation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a06df-126">-Reservierung</span><span class="sxs-lookup"><span data-stu-id="a06df-126">-Reservation</span></span>
<span data-ttu-id="a06df-127">Parameter des Pipeobjekts für `Reservation`</span><span class="sxs-lookup"><span data-stu-id="a06df-127">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="a06df-128">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="a06df-128">-ReservationId</span></span>
<span data-ttu-id="a06df-129">ID des `Reservation` zu aktualisieren</span><span class="sxs-lookup"><span data-stu-id="a06df-129">Id of the `Reservation` to update</span></span>

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

### <span data-ttu-id="a06df-130">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="a06df-130">-ReservationOrderId</span></span>
<span data-ttu-id="a06df-131">ID des `ReservationOrder` zu aktualisieren</span><span class="sxs-lookup"><span data-stu-id="a06df-131">Id of the `ReservationOrder` to update</span></span>

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

### <span data-ttu-id="a06df-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a06df-132">-Confirm</span></span>
<span data-ttu-id="a06df-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a06df-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a06df-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a06df-134">-WhatIf</span></span>
<span data-ttu-id="a06df-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a06df-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a06df-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a06df-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a06df-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a06df-137">CommonParameters</span></span>
<span data-ttu-id="a06df-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a06df-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a06df-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a06df-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a06df-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a06df-140">INPUTS</span></span>

### <span data-ttu-id="a06df-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="a06df-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="a06df-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a06df-142">OUTPUTS</span></span>

### <span data-ttu-id="a06df-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="a06df-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="a06df-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a06df-144">NOTES</span></span>

## <span data-ttu-id="a06df-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a06df-145">RELATED LINKS</span></span>
