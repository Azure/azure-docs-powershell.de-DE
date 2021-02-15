---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/update-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
ms.openlocfilehash: 4d4228ebcdf007485e35b45b93ea738c828c9c4d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143657"
---
# <span data-ttu-id="72c12-101">Update-AzReservation</span><span class="sxs-lookup"><span data-stu-id="72c12-101">Update-AzReservation</span></span>

## <span data-ttu-id="72c12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72c12-102">SYNOPSIS</span></span>
<span data-ttu-id="72c12-103">Aktualisieren sie eine `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="72c12-103">Update a `Reservation`.</span></span>

## <span data-ttu-id="72c12-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72c12-104">SYNTAX</span></span>

### <span data-ttu-id="72c12-105">Befehlszeile (Standard)</span><span class="sxs-lookup"><span data-stu-id="72c12-105">CommandLine (Default)</span></span>
```
Update-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -AppliedScopeType <String>
 [-AppliedScope <String>] [-InstanceFlexibility <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72c12-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="72c12-106">PipeObject</span></span>
```
Update-AzReservation -AppliedScopeType <String> [-AppliedScope <String>] [-InstanceFlexibility <String>]
 -Reservation <PSReservation> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="72c12-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="72c12-107">DESCRIPTION</span></span>
<span data-ttu-id="72c12-108">Aktualisiert die angewendeten Bereiche der `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="72c12-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="72c12-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="72c12-109">EXAMPLES</span></span>

### <span data-ttu-id="72c12-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="72c12-110">Example 1</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff" -InstanceFlexibility "On"
```

<span data-ttu-id="72c12-111">Aktualisiert den AppliedScopeType des angegebenen `Reservation` Werts auf "Single" und "InstanceFlexibility" auf "On".</span><span class="sxs-lookup"><span data-stu-id="72c12-111">Updates the AppliedScopeType of the specified `Reservation` to Single and InstanceFlexibility to On.</span></span>

### <span data-ttu-id="72c12-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="72c12-112">Example 2</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared" -InstanceFlexibility "Off"
```

<span data-ttu-id="72c12-113">Aktualisiert den AppliedScopeType des angegebenen `Reservation` Werts auf "Shared" und "InstanceFlexibility" auf "Off".</span><span class="sxs-lookup"><span data-stu-id="72c12-113">Updates the AppliedScopeType of the specified `Reservation` to Shared and InstanceFlexibility to Off.</span></span>

## <span data-ttu-id="72c12-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72c12-114">PARAMETERS</span></span>

### <span data-ttu-id="72c12-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="72c12-115">-AppliedScope</span></span>
<span data-ttu-id="72c12-116">SubscriptionId für diese `Reservation` Anwendung</span><span class="sxs-lookup"><span data-stu-id="72c12-116">SubscriptionId for this `Reservation` to be applied</span></span>

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

### <span data-ttu-id="72c12-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="72c12-117">-AppliedScopeType</span></span>
<span data-ttu-id="72c12-118">Typ des angewendeten Bereichs</span><span class="sxs-lookup"><span data-stu-id="72c12-118">Type of the Applied Scope</span></span>

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

### <span data-ttu-id="72c12-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72c12-119">-DefaultProfile</span></span>
<span data-ttu-id="72c12-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="72c12-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72c12-121">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="72c12-121">-InstanceFlexibility</span></span>
<span data-ttu-id="72c12-122">Wenn vorhanden, wird der Wert "InstanceFlexibility" der " `Reservation` aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="72c12-122">If present, updates the InstanceFlexibility value of the `Reservation`.</span></span> <span data-ttu-id="72c12-123">Wenn dieser Wert nicht angegeben wird, bleibt der vorhandene Wert unverändert.</span><span class="sxs-lookup"><span data-stu-id="72c12-123">If not specified, the existing value remains unchanged.</span></span>

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

### <span data-ttu-id="72c12-124">-Name</span><span class="sxs-lookup"><span data-stu-id="72c12-124">-Name</span></span>
<span data-ttu-id="72c12-125">Name der Reservierung</span><span class="sxs-lookup"><span data-stu-id="72c12-125">Name of Reservation</span></span>

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

### <span data-ttu-id="72c12-126">-Reservierung</span><span class="sxs-lookup"><span data-stu-id="72c12-126">-Reservation</span></span>
<span data-ttu-id="72c12-127">Objektparameter 'Pipe' für `Reservation`</span><span class="sxs-lookup"><span data-stu-id="72c12-127">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="72c12-128">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="72c12-128">-ReservationId</span></span>
<span data-ttu-id="72c12-129">ID der zu `Reservation` aktualisierende Datei</span><span class="sxs-lookup"><span data-stu-id="72c12-129">Id of the `Reservation` to update</span></span>

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

### <span data-ttu-id="72c12-130">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="72c12-130">-ReservationOrderId</span></span>
<span data-ttu-id="72c12-131">ID der zu `ReservationOrder` aktualisierende Datei</span><span class="sxs-lookup"><span data-stu-id="72c12-131">Id of the `ReservationOrder` to update</span></span>

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

### <span data-ttu-id="72c12-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="72c12-132">-Confirm</span></span>
<span data-ttu-id="72c12-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="72c12-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72c12-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="72c12-134">-WhatIf</span></span>
<span data-ttu-id="72c12-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="72c12-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72c12-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="72c12-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72c12-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72c12-137">CommonParameters</span></span>
<span data-ttu-id="72c12-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72c12-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72c12-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72c12-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72c12-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="72c12-140">INPUTS</span></span>

### <span data-ttu-id="72c12-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="72c12-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="72c12-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="72c12-142">OUTPUTS</span></span>

### <span data-ttu-id="72c12-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="72c12-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="72c12-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="72c12-144">NOTES</span></span>

## <span data-ttu-id="72c12-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="72c12-145">RELATED LINKS</span></span>
