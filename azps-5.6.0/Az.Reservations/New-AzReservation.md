---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/new-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
ms.openlocfilehash: 37be462c2af2c33987e6acd0118c3169b1e062d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943661"
---
# <span data-ttu-id="55a86-101">New-AzReservation</span><span class="sxs-lookup"><span data-stu-id="55a86-101">New-AzReservation</span></span>

## <span data-ttu-id="55a86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55a86-102">SYNOPSIS</span></span>
<span data-ttu-id="55a86-103">Kaufen einer Reservierung</span><span class="sxs-lookup"><span data-stu-id="55a86-103">Purchase a reservation</span></span>

## <span data-ttu-id="55a86-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55a86-104">SYNTAX</span></span>

```
New-AzReservation -ReservationOrderId <String> -ReservedResourceType <String> -Sku <String>
 [-Location <String>] -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32>
 -DisplayName <String> -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>]
 [-InstanceFlexibility <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="55a86-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55a86-105">DESCRIPTION</span></span>
<span data-ttu-id="55a86-106">Erwerben einer Reservierungsinstanz und Nutzen</span><span class="sxs-lookup"><span data-stu-id="55a86-106">Purchase a reservation Instance and get benefit</span></span>

## <span data-ttu-id="55a86-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="55a86-107">EXAMPLES</span></span>

### <span data-ttu-id="55a86-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="55a86-108">Example 1</span></span>
```powershell
PS C:\> New-AzReservation -ReservationOrderId "112382d9-9af7-4fd5-b136-b71f0a69a1d0" -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="55a86-109">Nach der Berechnung des Preises könnte der Kunde die von RI zur Verfügung stellende Purcahse durch Berechnen des Preises</span><span class="sxs-lookup"><span data-stu-id="55a86-109">After calculate price, customer could purcahse that RI provide by calculatePrice</span></span>

## <span data-ttu-id="55a86-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="55a86-110">PARAMETERS</span></span>

### <span data-ttu-id="55a86-111">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="55a86-111">-AppliedScope</span></span>
<span data-ttu-id="55a86-112">Abonnement, für das der Vorteil angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="55a86-112">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="55a86-113">Erforderlich, wenn --applied-scope-type single ist.</span><span class="sxs-lookup"><span data-stu-id="55a86-113">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="55a86-114">Geben Sie nicht an, ob --applied-scope-type freigegeben ist.</span><span class="sxs-lookup"><span data-stu-id="55a86-114">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="55a86-115">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="55a86-115">-AppliedScopeType</span></span>
<span data-ttu-id="55a86-116">Typ des angewendeten Bereichs zum Aktualisieren der Reservierung mit "Single" oder "Shared"</span><span class="sxs-lookup"><span data-stu-id="55a86-116">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="55a86-117">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="55a86-117">-BillingPlan</span></span>
<span data-ttu-id="55a86-118">Die für diese SKU verfügbaren Abrechnungsplanoptionen.</span><span class="sxs-lookup"><span data-stu-id="55a86-118">The billing plan options available for this SKU.</span></span> <span data-ttu-id="55a86-119">"Monatlich" oder "Vorab"</span><span class="sxs-lookup"><span data-stu-id="55a86-119">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="55a86-120">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="55a86-120">-BillingScopeId</span></span>
<span data-ttu-id="55a86-121">Abonnement, das für den Kauf der Reservierung in Rechnung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="55a86-121">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="55a86-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55a86-122">-DefaultProfile</span></span>
<span data-ttu-id="55a86-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="55a86-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55a86-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="55a86-124">-DisplayName</span></span>
<span data-ttu-id="55a86-125">Anzeigename für den Benutzer, um die Reservierung ganz einfach zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="55a86-125">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="55a86-126">-InstanzFlexibilität</span><span class="sxs-lookup"><span data-stu-id="55a86-126">-InstanceFlexibility</span></span>
<span data-ttu-id="55a86-127">{{ Fill InstanceFlexibility Description }}</span><span class="sxs-lookup"><span data-stu-id="55a86-127">{{ Fill InstanceFlexibility Description }}</span></span>

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

### <span data-ttu-id="55a86-128">-Location</span><span class="sxs-lookup"><span data-stu-id="55a86-128">-Location</span></span>
<span data-ttu-id="55a86-129">Speicherort, an dem die SKU verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="55a86-129">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="55a86-130">-Quantity</span><span class="sxs-lookup"><span data-stu-id="55a86-130">-Quantity</span></span>
<span data-ttu-id="55a86-131">Menge des Produkts zur Berechnung von Preis oder Einkauf.</span><span class="sxs-lookup"><span data-stu-id="55a86-131">Quantity of product for calculating price or purchasing.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55a86-132">-Verlängern</span><span class="sxs-lookup"><span data-stu-id="55a86-132">-Renew</span></span>
<span data-ttu-id="55a86-133">Wenn Sie diesen Wert auf "true" festlegen, wird automatisch eine neue Reservierung zum Ablaufdatum kauft.</span><span class="sxs-lookup"><span data-stu-id="55a86-133">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55a86-134">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="55a86-134">-ReservationOrderId</span></span>
<span data-ttu-id="55a86-135">Id des zu kaufenden Reservierungsauftrags, generieren Sie per az reservations reservation-order calculate.</span><span class="sxs-lookup"><span data-stu-id="55a86-135">Id of reservation order to purchase, generate by az reservations reservation-order calculate.</span></span>

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

### <span data-ttu-id="55a86-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="55a86-136">-ReservedResourceType</span></span>
<span data-ttu-id="55a86-137">Typ der Ressource, für die der Skus bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="55a86-137">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="55a86-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="55a86-138">-Sku</span></span>
<span data-ttu-id="55a86-139">Sku-Name</span><span class="sxs-lookup"><span data-stu-id="55a86-139">Sku name</span></span>

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

### <span data-ttu-id="55a86-140">-Ausdruck</span><span class="sxs-lookup"><span data-stu-id="55a86-140">-Term</span></span>
<span data-ttu-id="55a86-141">Verfügbare Reservierungsbedingungen für diese Ressource.</span><span class="sxs-lookup"><span data-stu-id="55a86-141">Available reservation terms for this resource.</span></span>


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

### <span data-ttu-id="55a86-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="55a86-142">-Confirm</span></span>
<span data-ttu-id="55a86-143">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="55a86-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55a86-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55a86-144">-WhatIf</span></span>
<span data-ttu-id="55a86-145">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="55a86-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55a86-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="55a86-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55a86-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55a86-147">CommonParameters</span></span>
<span data-ttu-id="55a86-148">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55a86-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55a86-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55a86-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55a86-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="55a86-150">INPUTS</span></span>

### <span data-ttu-id="55a86-151">Keine</span><span class="sxs-lookup"><span data-stu-id="55a86-151">None</span></span>

## <span data-ttu-id="55a86-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="55a86-152">OUTPUTS</span></span>

### <span data-ttu-id="55a86-153">Microsoft.Azure.Management.Reservations.Models.ReservationOrderResponse</span><span class="sxs-lookup"><span data-stu-id="55a86-153">Microsoft.Azure.Management.Reservations.Models.ReservationOrderResponse</span></span>

## <span data-ttu-id="55a86-154">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="55a86-154">NOTES</span></span>

## <span data-ttu-id="55a86-155">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="55a86-155">RELATED LINKS</span></span>
