---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/update-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Update-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Update-AzureRmReservation.md
ms.openlocfilehash: 64e2ec58c6ed31e54a4adf0ee983aa9ae485715d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482138"
---
# <span data-ttu-id="aea37-101">Update-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="aea37-101">Update-AzureRmReservation</span></span>

## <span data-ttu-id="aea37-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aea37-102">SYNOPSIS</span></span>
<span data-ttu-id="aea37-103">Aktualisieren Sie eine `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="aea37-103">Update a `Reservation`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aea37-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aea37-104">SYNTAX</span></span>

### <span data-ttu-id="aea37-105">CommandLine (Standard)</span><span class="sxs-lookup"><span data-stu-id="aea37-105">CommandLine (Default)</span></span>
```
Update-AzureRmReservation -ReservationOrderId <Guid> -ReservationId <Guid> -AppliedScopeType <String>
 [-AppliedScope <String>] [-InstanceFlexibility <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aea37-106">Pipeobject</span><span class="sxs-lookup"><span data-stu-id="aea37-106">PipeObject</span></span>
```
Update-AzureRmReservation -AppliedScopeType <String> [-AppliedScope <String>] [-InstanceFlexibility <String>]
 -Reservation <PSReservation> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aea37-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aea37-107">DESCRIPTION</span></span>
<span data-ttu-id="aea37-108">Aktualisiert die angewendeten Bereiche von `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="aea37-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="aea37-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aea37-109">EXAMPLES</span></span>

### <span data-ttu-id="aea37-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="aea37-110">Example 1</span></span>
```
PS C:\> Update-AzureRmReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff" -InstanceFlexibility "On"
```

<span data-ttu-id="aea37-111">Aktualisiert die AppliedScopeType des angegebenen `Reservation` in Single und InstanceFlexibility auf ein.</span><span class="sxs-lookup"><span data-stu-id="aea37-111">Updates the AppliedScopeType of the specified `Reservation` to Single and InstanceFlexibility to On.</span></span>

### <span data-ttu-id="aea37-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="aea37-112">Example 2</span></span>
```
PS C:\> Update-AzureRmReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared" -InstanceFlexibility "Off"
```

<span data-ttu-id="aea37-113">Aktualisiert die AppliedScopeType des angegebenen `Reservation` freigegebenen und InstanceFlexibility auf aus.</span><span class="sxs-lookup"><span data-stu-id="aea37-113">Updates the AppliedScopeType of the specified `Reservation` to Shared and InstanceFlexibility to Off.</span></span>

## <span data-ttu-id="aea37-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="aea37-114">PARAMETERS</span></span>

### <span data-ttu-id="aea37-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="aea37-115">-AppliedScope</span></span>
<span data-ttu-id="aea37-116">Abonnement-Nr für diese `Reservation` Anwendung</span><span class="sxs-lookup"><span data-stu-id="aea37-116">SubscriptionId for this `Reservation` to be applied</span></span>

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

### <span data-ttu-id="aea37-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="aea37-117">-AppliedScopeType</span></span>
<span data-ttu-id="aea37-118">Typ des angewendeten Bereichs</span><span class="sxs-lookup"><span data-stu-id="aea37-118">Type of the Applied Scope</span></span>

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

### <span data-ttu-id="aea37-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aea37-119">-DefaultProfile</span></span>
<span data-ttu-id="aea37-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aea37-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aea37-121">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="aea37-121">-InstanceFlexibility</span></span>
<span data-ttu-id="aea37-122">Wenn vorhanden, wird der InstanceFlexibility-Wert der `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="aea37-122">If present, updates the InstanceFlexibility value of the `Reservation`.</span></span> <span data-ttu-id="aea37-123">Wenn nicht angegeben, bleibt der vorhandene Wert unverändert.</span><span class="sxs-lookup"><span data-stu-id="aea37-123">If not specified, the existing value remains unchanged.</span></span>

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

### <span data-ttu-id="aea37-124">-Name</span><span class="sxs-lookup"><span data-stu-id="aea37-124">-Name</span></span>
<span data-ttu-id="aea37-125">Name der Reservierung</span><span class="sxs-lookup"><span data-stu-id="aea37-125">Name of Reservation</span></span>

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

### <span data-ttu-id="aea37-126">-Reservation</span><span class="sxs-lookup"><span data-stu-id="aea37-126">-Reservation</span></span>
<span data-ttu-id="aea37-127">Pipe-Objektparameter für `Reservation`</span><span class="sxs-lookup"><span data-stu-id="aea37-127">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="aea37-128">-Reservierungs-Nr.</span><span class="sxs-lookup"><span data-stu-id="aea37-128">-ReservationId</span></span>
<span data-ttu-id="aea37-129">Die ID des `Reservation` zu aktualisierendes</span><span class="sxs-lookup"><span data-stu-id="aea37-129">Id of the `Reservation` to update</span></span>

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

### <span data-ttu-id="aea37-130">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="aea37-130">-ReservationOrderId</span></span>
<span data-ttu-id="aea37-131">Die ID des `ReservationOrder` zu aktualisierendes</span><span class="sxs-lookup"><span data-stu-id="aea37-131">Id of the `ReservationOrder` to update</span></span>

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

### <span data-ttu-id="aea37-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="aea37-132">-Confirm</span></span>
<span data-ttu-id="aea37-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aea37-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aea37-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aea37-134">-WhatIf</span></span>
<span data-ttu-id="aea37-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aea37-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aea37-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aea37-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aea37-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aea37-137">CommonParameters</span></span>
<span data-ttu-id="aea37-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aea37-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aea37-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aea37-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aea37-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aea37-140">INPUTS</span></span>

### <span data-ttu-id="aea37-141">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="aea37-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>
<span data-ttu-id="aea37-142">Parameter: Reservierung (ByValue)</span><span class="sxs-lookup"><span data-stu-id="aea37-142">Parameters: Reservation (ByValue)</span></span>

## <span data-ttu-id="aea37-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aea37-143">OUTPUTS</span></span>

### <span data-ttu-id="aea37-144">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="aea37-144">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="aea37-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="aea37-145">NOTES</span></span>

## <span data-ttu-id="aea37-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aea37-146">RELATED LINKS</span></span>
