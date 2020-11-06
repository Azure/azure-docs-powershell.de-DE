---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/update-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Update-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Update-AzureRmReservation.md
ms.openlocfilehash: 76abdc2f7a7099529af87f69af8e37319685aea7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482754"
---
# <span data-ttu-id="5288c-101">Update-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="5288c-101">Update-AzureRmReservation</span></span>

## <span data-ttu-id="5288c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5288c-102">SYNOPSIS</span></span>
<span data-ttu-id="5288c-103">Aktualisieren Sie eine `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="5288c-103">Update a `Reservation`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5288c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5288c-104">SYNTAX</span></span>

### <span data-ttu-id="5288c-105">CommandLine (Standard)</span><span class="sxs-lookup"><span data-stu-id="5288c-105">CommandLine (Default)</span></span>
```
Update-AzureRmReservation -ReservationOrderId <String> -ReservationId <String> -AppliedScopeType <String>
 [-AppliedScope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5288c-106">Pipeobject</span><span class="sxs-lookup"><span data-stu-id="5288c-106">PipeObject</span></span>
```
Update-AzureRmReservation -AppliedScopeType <String> [-AppliedScope <String>] -Reservation <PSReservation>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5288c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5288c-107">DESCRIPTION</span></span>
<span data-ttu-id="5288c-108">Aktualisiert die angewendeten Bereiche von `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="5288c-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="5288c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5288c-109">EXAMPLES</span></span>

### <span data-ttu-id="5288c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5288c-110">Example 1</span></span>
```
PS C:\> Update-AzureRmReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="5288c-111">Aktualisiert die AppliedScopeType der angegebenen Reservierung in Single</span><span class="sxs-lookup"><span data-stu-id="5288c-111">Updates the AppliedScopeType of the specified reservation to Single</span></span>

### <span data-ttu-id="5288c-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5288c-112">Example 2</span></span>
```
PS C:\> Update-AzureRmReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared"
```

<span data-ttu-id="5288c-113">Aktualisiert die AppliedScopeType der angegebenen Reservierung für Shared</span><span class="sxs-lookup"><span data-stu-id="5288c-113">Updates the AppliedScopeType of the specified reservation to Shared</span></span>

## <span data-ttu-id="5288c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="5288c-114">PARAMETERS</span></span>

### <span data-ttu-id="5288c-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="5288c-115">-AppliedScope</span></span>
<span data-ttu-id="5288c-116">Abonnement-Nr für diese `Reservation` Anwendung</span><span class="sxs-lookup"><span data-stu-id="5288c-116">SubscriptionId for this `Reservation` to be applied</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5288c-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="5288c-117">-AppliedScopeType</span></span>
<span data-ttu-id="5288c-118">Der Typ der `Reservation` zu aktualisierende</span><span class="sxs-lookup"><span data-stu-id="5288c-118">Type of the `Reservation` to be updated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Single, Shared

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5288c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5288c-119">-DefaultProfile</span></span>
<span data-ttu-id="5288c-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5288c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5288c-121">-Reservation</span><span class="sxs-lookup"><span data-stu-id="5288c-121">-Reservation</span></span>
<span data-ttu-id="5288c-122">Pipe-Objektparameter für `Reservation`</span><span class="sxs-lookup"><span data-stu-id="5288c-122">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="5288c-123">-Reservierungs-Nr.</span><span class="sxs-lookup"><span data-stu-id="5288c-123">-ReservationId</span></span>
<span data-ttu-id="5288c-124">Die ID des `Reservation` zu aktualisierendes</span><span class="sxs-lookup"><span data-stu-id="5288c-124">Id of the `Reservation` to update</span></span>

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

### <span data-ttu-id="5288c-125">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="5288c-125">-ReservationOrderId</span></span>
<span data-ttu-id="5288c-126">Die ID des `ReservationOrder` zu aktualisierendes</span><span class="sxs-lookup"><span data-stu-id="5288c-126">Id of the `ReservationOrder` to update</span></span>

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

### <span data-ttu-id="5288c-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5288c-127">-Confirm</span></span>
<span data-ttu-id="5288c-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5288c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5288c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5288c-129">-WhatIf</span></span>
<span data-ttu-id="5288c-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5288c-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5288c-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5288c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5288c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5288c-132">CommonParameters</span></span>
<span data-ttu-id="5288c-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5288c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5288c-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5288c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5288c-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5288c-135">INPUTS</span></span>

### <span data-ttu-id="5288c-136">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="5288c-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="5288c-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5288c-137">OUTPUTS</span></span>

### <span data-ttu-id="5288c-138">Microsoft. Azure. Commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="5288c-138">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="5288c-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="5288c-139">NOTES</span></span>

## <span data-ttu-id="5288c-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5288c-140">RELATED LINKS</span></span>

