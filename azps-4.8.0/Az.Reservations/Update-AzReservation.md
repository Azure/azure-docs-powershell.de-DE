---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/update-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
ms.openlocfilehash: 4d4228ebcdf007485e35b45b93ea738c828c9c4d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165013"
---
# <span data-ttu-id="662b6-101">Update-AzReservation</span><span class="sxs-lookup"><span data-stu-id="662b6-101">Update-AzReservation</span></span>

## <span data-ttu-id="662b6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="662b6-102">SYNOPSIS</span></span>
<span data-ttu-id="662b6-103">Aktualisieren Sie eine `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="662b6-103">Update a `Reservation`.</span></span>

## <span data-ttu-id="662b6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="662b6-104">SYNTAX</span></span>

### <span data-ttu-id="662b6-105">CommandLine (Standard)</span><span class="sxs-lookup"><span data-stu-id="662b6-105">CommandLine (Default)</span></span>
```
Update-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -AppliedScopeType <String>
 [-AppliedScope <String>] [-InstanceFlexibility <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="662b6-106">Pipeobject</span><span class="sxs-lookup"><span data-stu-id="662b6-106">PipeObject</span></span>
```
Update-AzReservation -AppliedScopeType <String> [-AppliedScope <String>] [-InstanceFlexibility <String>]
 -Reservation <PSReservation> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="662b6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="662b6-107">DESCRIPTION</span></span>
<span data-ttu-id="662b6-108">Aktualisiert die angewendeten Bereiche von `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="662b6-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="662b6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="662b6-109">EXAMPLES</span></span>

### <span data-ttu-id="662b6-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="662b6-110">Example 1</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff" -InstanceFlexibility "On"
```

<span data-ttu-id="662b6-111">Aktualisiert die AppliedScopeType des angegebenen `Reservation` in Single und InstanceFlexibility auf ein.</span><span class="sxs-lookup"><span data-stu-id="662b6-111">Updates the AppliedScopeType of the specified `Reservation` to Single and InstanceFlexibility to On.</span></span>

### <span data-ttu-id="662b6-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="662b6-112">Example 2</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared" -InstanceFlexibility "Off"
```

<span data-ttu-id="662b6-113">Aktualisiert die AppliedScopeType des angegebenen `Reservation` freigegebenen und InstanceFlexibility auf aus.</span><span class="sxs-lookup"><span data-stu-id="662b6-113">Updates the AppliedScopeType of the specified `Reservation` to Shared and InstanceFlexibility to Off.</span></span>

## <span data-ttu-id="662b6-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="662b6-114">PARAMETERS</span></span>

### <span data-ttu-id="662b6-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="662b6-115">-AppliedScope</span></span>
<span data-ttu-id="662b6-116">Abonnement-Nr für diese `Reservation` Anwendung</span><span class="sxs-lookup"><span data-stu-id="662b6-116">SubscriptionId for this `Reservation` to be applied</span></span>

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

### <span data-ttu-id="662b6-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="662b6-117">-AppliedScopeType</span></span>
<span data-ttu-id="662b6-118">Typ des angewendeten Bereichs</span><span class="sxs-lookup"><span data-stu-id="662b6-118">Type of the Applied Scope</span></span>

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

### <span data-ttu-id="662b6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="662b6-119">-DefaultProfile</span></span>
<span data-ttu-id="662b6-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="662b6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="662b6-121">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="662b6-121">-InstanceFlexibility</span></span>
<span data-ttu-id="662b6-122">Wenn vorhanden, wird der InstanceFlexibility-Wert der `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="662b6-122">If present, updates the InstanceFlexibility value of the `Reservation`.</span></span> <span data-ttu-id="662b6-123">Wenn nicht angegeben, bleibt der vorhandene Wert unverändert.</span><span class="sxs-lookup"><span data-stu-id="662b6-123">If not specified, the existing value remains unchanged.</span></span>

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

### <span data-ttu-id="662b6-124">-Name</span><span class="sxs-lookup"><span data-stu-id="662b6-124">-Name</span></span>
<span data-ttu-id="662b6-125">Name der Reservierung</span><span class="sxs-lookup"><span data-stu-id="662b6-125">Name of Reservation</span></span>

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

### <span data-ttu-id="662b6-126">-Reservation</span><span class="sxs-lookup"><span data-stu-id="662b6-126">-Reservation</span></span>
<span data-ttu-id="662b6-127">Pipe-Objektparameter für `Reservation`</span><span class="sxs-lookup"><span data-stu-id="662b6-127">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="662b6-128">-Reservierungs-Nr.</span><span class="sxs-lookup"><span data-stu-id="662b6-128">-ReservationId</span></span>
<span data-ttu-id="662b6-129">Die ID des `Reservation` zu aktualisierendes</span><span class="sxs-lookup"><span data-stu-id="662b6-129">Id of the `Reservation` to update</span></span>

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

### <span data-ttu-id="662b6-130">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="662b6-130">-ReservationOrderId</span></span>
<span data-ttu-id="662b6-131">Die ID des `ReservationOrder` zu aktualisierendes</span><span class="sxs-lookup"><span data-stu-id="662b6-131">Id of the `ReservationOrder` to update</span></span>

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

### <span data-ttu-id="662b6-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="662b6-132">-Confirm</span></span>
<span data-ttu-id="662b6-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="662b6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="662b6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="662b6-134">-WhatIf</span></span>
<span data-ttu-id="662b6-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="662b6-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="662b6-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="662b6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="662b6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="662b6-137">CommonParameters</span></span>
<span data-ttu-id="662b6-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="662b6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="662b6-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="662b6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="662b6-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="662b6-140">INPUTS</span></span>

### <span data-ttu-id="662b6-141">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="662b6-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="662b6-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="662b6-142">OUTPUTS</span></span>

### <span data-ttu-id="662b6-143">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="662b6-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="662b6-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="662b6-144">NOTES</span></span>

## <span data-ttu-id="662b6-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="662b6-145">RELATED LINKS</span></span>
