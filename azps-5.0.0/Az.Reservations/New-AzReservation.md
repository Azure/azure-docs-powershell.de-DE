---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/new-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
ms.openlocfilehash: 60de1572afda000c8c1a99f53df1344b9b0fbfda
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176120"
---
# <span data-ttu-id="3bfbc-101">New-AzReservation</span><span class="sxs-lookup"><span data-stu-id="3bfbc-101">New-AzReservation</span></span>

## <span data-ttu-id="3bfbc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3bfbc-102">SYNOPSIS</span></span>
<span data-ttu-id="3bfbc-103">Eine Reservierung kaufen</span><span class="sxs-lookup"><span data-stu-id="3bfbc-103">Purchase a reservation</span></span>

## <span data-ttu-id="3bfbc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3bfbc-104">SYNTAX</span></span>

```
New-AzReservation -ReservationOrderId <String> -ReservedResourceType <String> -Sku <String>
 [-Location <String>] -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32>
 -DisplayName <String> -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>]
 [-InstanceFlexibility <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3bfbc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3bfbc-105">DESCRIPTION</span></span>
<span data-ttu-id="3bfbc-106">Erwerben einer Reservierungs Instanz und erhalten von Benefit</span><span class="sxs-lookup"><span data-stu-id="3bfbc-106">Purchase a reservation Instance and get benefit</span></span>

## <span data-ttu-id="3bfbc-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3bfbc-107">EXAMPLES</span></span>

### <span data-ttu-id="3bfbc-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3bfbc-108">Example 1</span></span>
```powershell
PS C:\> New-AzReservation -ReservationOrderId "112382d9-9af7-4fd5-b136-b71f0a69a1d0" -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="3bfbc-109">Nach dem Preis berechnen kann der Kunde purcahse, dass RI von calculatePrice bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="3bfbc-109">After calculate price, customer could purcahse that RI provide by calculatePrice</span></span>

## <span data-ttu-id="3bfbc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3bfbc-110">PARAMETERS</span></span>

### <span data-ttu-id="3bfbc-111">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="3bfbc-111">-AppliedScope</span></span>
<span data-ttu-id="3bfbc-112">Abonnement, auf das der Vorteil angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="3bfbc-112">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="3bfbc-113">Erforderlich, wenn--Applied-Scope-Type Single ist.</span><span class="sxs-lookup"><span data-stu-id="3bfbc-113">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="3bfbc-114">Geben Sie nicht an, ob--Applied-Scope-Type freigegeben ist.</span><span class="sxs-lookup"><span data-stu-id="3bfbc-114">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="3bfbc-115">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="3bfbc-115">-AppliedScopeType</span></span>
<span data-ttu-id="3bfbc-116">Typ des angewendeten Bereichs zum Aktualisieren der Reservierung mit "einzeln" oder "freigegeben"</span><span class="sxs-lookup"><span data-stu-id="3bfbc-116">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="3bfbc-117">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="3bfbc-117">-BillingPlan</span></span>
<span data-ttu-id="3bfbc-118">Die für diese SKU verfügbaren Optionen für den Fakturierungsplan.</span><span class="sxs-lookup"><span data-stu-id="3bfbc-118">The billing plan options available for this SKU.</span></span> <span data-ttu-id="3bfbc-119">"Monatlich" oder "im voraus"</span><span class="sxs-lookup"><span data-stu-id="3bfbc-119">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="3bfbc-120">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="3bfbc-120">-BillingScopeId</span></span>
<span data-ttu-id="3bfbc-121">Das Abonnement wird für den Kauf einer Reservierung in Rechnung gestellt.</span><span class="sxs-lookup"><span data-stu-id="3bfbc-121">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="3bfbc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bfbc-122">-DefaultProfile</span></span>
<span data-ttu-id="3bfbc-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3bfbc-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bfbc-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3bfbc-124">-DisplayName</span></span>
<span data-ttu-id="3bfbc-125">Anzeigename für den Benutzer, um die Reservierung einfach zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="3bfbc-125">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="3bfbc-126">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="3bfbc-126">-InstanceFlexibility</span></span>
<span data-ttu-id="3bfbc-127">{{Fill InstanceFlexibility Description}}</span><span class="sxs-lookup"><span data-stu-id="3bfbc-127">{{ Fill InstanceFlexibility Description }}</span></span>

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

### <span data-ttu-id="3bfbc-128">-Standort</span><span class="sxs-lookup"><span data-stu-id="3bfbc-128">-Location</span></span>
<span data-ttu-id="3bfbc-129">Der Speicherort, an dem die SKU verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3bfbc-129">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="3bfbc-130">-Quantity</span><span class="sxs-lookup"><span data-stu-id="3bfbc-130">-Quantity</span></span>
<span data-ttu-id="3bfbc-131">Die Menge des Produkts zur Berechnung des Preises oder des Kaufs.</span><span class="sxs-lookup"><span data-stu-id="3bfbc-131">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="3bfbc-132">– Verlängern</span><span class="sxs-lookup"><span data-stu-id="3bfbc-132">-Renew</span></span>
<span data-ttu-id="3bfbc-133">Wenn diese Einstellung auf "true" festgelegt ist, wird automatisch eine neue Reservierung für das Ablaufdatum gekauft.</span><span class="sxs-lookup"><span data-stu-id="3bfbc-133">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="3bfbc-134">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="3bfbc-134">-ReservationOrderId</span></span>
<span data-ttu-id="3bfbc-135">Die ID der Reservierungs Reihenfolge für den Kauf, die durch AZ-Reservierungs Reservierung generiert wird-Bestellung berechnen.</span><span class="sxs-lookup"><span data-stu-id="3bfbc-135">Id of reservation order to purchase, generate by az reservations reservation-order calculate.</span></span>

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

### <span data-ttu-id="3bfbc-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="3bfbc-136">-ReservedResourceType</span></span>
<span data-ttu-id="3bfbc-137">Der Typ der Ressource, für die die SKUs bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3bfbc-137">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="3bfbc-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="3bfbc-138">-Sku</span></span>
<span data-ttu-id="3bfbc-139">SKU-Name</span><span class="sxs-lookup"><span data-stu-id="3bfbc-139">Sku name</span></span>

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

### <span data-ttu-id="3bfbc-140">-Term</span><span class="sxs-lookup"><span data-stu-id="3bfbc-140">-Term</span></span>
<span data-ttu-id="3bfbc-141">Die verfügbaren Reservierungsbestimmungen für diese Ressource.</span><span class="sxs-lookup"><span data-stu-id="3bfbc-141">Available reservation terms for this resource.</span></span>


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

### <span data-ttu-id="3bfbc-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3bfbc-142">-Confirm</span></span>
<span data-ttu-id="3bfbc-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3bfbc-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bfbc-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bfbc-144">-WhatIf</span></span>
<span data-ttu-id="3bfbc-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3bfbc-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3bfbc-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3bfbc-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bfbc-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bfbc-147">CommonParameters</span></span>
<span data-ttu-id="3bfbc-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bfbc-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bfbc-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3bfbc-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bfbc-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3bfbc-150">INPUTS</span></span>

### <span data-ttu-id="3bfbc-151">Keine</span><span class="sxs-lookup"><span data-stu-id="3bfbc-151">None</span></span>

## <span data-ttu-id="3bfbc-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3bfbc-152">OUTPUTS</span></span>

### <span data-ttu-id="3bfbc-153">Microsoft. Azure. Management. reservations. Models. ReservationOrderResponse</span><span class="sxs-lookup"><span data-stu-id="3bfbc-153">Microsoft.Azure.Management.Reservations.Models.ReservationOrderResponse</span></span>

## <span data-ttu-id="3bfbc-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="3bfbc-154">NOTES</span></span>

## <span data-ttu-id="3bfbc-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3bfbc-155">RELATED LINKS</span></span>
