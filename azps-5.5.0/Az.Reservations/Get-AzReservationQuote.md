---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationquote
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
ms.openlocfilehash: 073a059063198e91a1bbcc67814c01c1b786e7c9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143681"
---
# <span data-ttu-id="dbd54-101">Get-AzReservationQuote</span><span class="sxs-lookup"><span data-stu-id="dbd54-101">Get-AzReservationQuote</span></span>

## <span data-ttu-id="dbd54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbd54-102">SYNOPSIS</span></span>
<span data-ttu-id="dbd54-103">Hier erhalten Sie ein Angebot für die Reservierung.</span><span class="sxs-lookup"><span data-stu-id="dbd54-103">Get a quote for the reservation.</span></span> <span data-ttu-id="dbd54-104">Diese wird an `New-AzReservation` den Kauf übergeben.</span><span class="sxs-lookup"><span data-stu-id="dbd54-104">This is passed to `New-AzReservation` to purchase.</span></span>

## <span data-ttu-id="dbd54-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dbd54-105">SYNTAX</span></span>

```
Get-AzReservationQuote -ReservedResourceType <String> -Sku <String> [-Location <String>]
 -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32> -DisplayName <String>
 -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>] [-InstanceFlexibility <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbd54-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dbd54-106">DESCRIPTION</span></span>
<span data-ttu-id="dbd54-107">Berechnen des Preises für einen Reservierungsauftrag</span><span class="sxs-lookup"><span data-stu-id="dbd54-107">Calculate price for placing a reservation order.</span></span>

## <span data-ttu-id="dbd54-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dbd54-108">EXAMPLES</span></span>

### <span data-ttu-id="dbd54-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dbd54-109">Example 1</span></span>
```powershell
PS C:\> Get-AzReservationQuote -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="dbd54-110">Nach dem Erhalten des Katalogs kann der Kunde das andere Produkt basierend auf dem Standort erhalten.</span><span class="sxs-lookup"><span data-stu-id="dbd54-110">After get catalog, customer can get the differe product based on location.</span></span> <span data-ttu-id="dbd54-111">Anhand dieser Informationen können Sie den Preis ordnungsgemäß überprüfen.</span><span class="sxs-lookup"><span data-stu-id="dbd54-111">By using those infomation, check the price properly</span></span>

## <span data-ttu-id="dbd54-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbd54-112">PARAMETERS</span></span>

### <span data-ttu-id="dbd54-113">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="dbd54-113">-AppliedScope</span></span>
<span data-ttu-id="dbd54-114">Abonnement, für das der Vorteil angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="dbd54-114">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="dbd54-115">Erforderlich, wenn "-applied-scope-type" "Single" ist.</span><span class="sxs-lookup"><span data-stu-id="dbd54-115">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="dbd54-116">Geben Sie nicht an, ob "-applied-scope-type" freigegeben ist.</span><span class="sxs-lookup"><span data-stu-id="dbd54-116">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="dbd54-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="dbd54-117">-AppliedScopeType</span></span>
<span data-ttu-id="dbd54-118">Typ des angewendeten Bereichs, um die Reservierung mit "Single" oder "Shared" zu aktualisieren</span><span class="sxs-lookup"><span data-stu-id="dbd54-118">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="dbd54-119">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="dbd54-119">-BillingPlan</span></span>
<span data-ttu-id="dbd54-120">Die für diese SKU verfügbaren Abrechnungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="dbd54-120">The billing plan options available for this SKU.</span></span> <span data-ttu-id="dbd54-121">"Monatlich" oder "Im Voraus"</span><span class="sxs-lookup"><span data-stu-id="dbd54-121">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="dbd54-122">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="dbd54-122">-BillingScopeId</span></span>
<span data-ttu-id="dbd54-123">Abonnement, das für den Kauf der Reservierung in Rechnung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="dbd54-123">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="dbd54-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbd54-124">-DefaultProfile</span></span>
<span data-ttu-id="dbd54-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dbd54-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbd54-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="dbd54-126">-DisplayName</span></span>
<span data-ttu-id="dbd54-127">Anzeigename für den Benutzer, um die Reservierung einfach zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="dbd54-127">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="dbd54-128">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="dbd54-128">-InstanceFlexibility</span></span>
<span data-ttu-id="dbd54-129">Typ der Instanzflexibilität, mit der die Reservierung aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="dbd54-129">Type of the Instance Flexibility to update the reservation with.</span></span>

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

### <span data-ttu-id="dbd54-130">-Location</span><span class="sxs-lookup"><span data-stu-id="dbd54-130">-Location</span></span>
<span data-ttu-id="dbd54-131">Speicherort, an dem die SKU verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="dbd54-131">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="dbd54-132">-Quantity</span><span class="sxs-lookup"><span data-stu-id="dbd54-132">-Quantity</span></span>
<span data-ttu-id="dbd54-133">Menge des Produkts zur Berechnung des Preises oder Kaufs.</span><span class="sxs-lookup"><span data-stu-id="dbd54-133">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="dbd54-134">-Verlängern</span><span class="sxs-lookup"><span data-stu-id="dbd54-134">-Renew</span></span>
<span data-ttu-id="dbd54-135">Wenn Sie dies auf "true" festlegen, wird am Ablaufdatum automatisch eine neue Reservierung kauft.</span><span class="sxs-lookup"><span data-stu-id="dbd54-135">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="dbd54-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="dbd54-136">-ReservedResourceType</span></span>
<span data-ttu-id="dbd54-137">Der Typ der Ressource, für die die SKU bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dbd54-137">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="dbd54-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="dbd54-138">-Sku</span></span>
<span data-ttu-id="dbd54-139">SKU-Name, Anzeigen der SKU-Liste mithilfe des Befehls az reservations catalog show</span><span class="sxs-lookup"><span data-stu-id="dbd54-139">Sku name, get the sku list by using command az reservations catalog show</span></span>

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

### <span data-ttu-id="dbd54-140">-Term</span><span class="sxs-lookup"><span data-stu-id="dbd54-140">-Term</span></span>
<span data-ttu-id="dbd54-141">Verfügbare Reservierungsbedingungen für diese Ressource.</span><span class="sxs-lookup"><span data-stu-id="dbd54-141">Available reservation terms for this resource.</span></span>

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

### <span data-ttu-id="dbd54-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbd54-142">CommonParameters</span></span>
<span data-ttu-id="dbd54-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbd54-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbd54-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dbd54-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbd54-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dbd54-145">INPUTS</span></span>

### <span data-ttu-id="dbd54-146">Keine</span><span class="sxs-lookup"><span data-stu-id="dbd54-146">None</span></span>

## <span data-ttu-id="dbd54-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dbd54-147">OUTPUTS</span></span>

### <span data-ttu-id="dbd54-148">Microsoft.Azure.Management.Reservations.Models.CalculatePriceResponse</span><span class="sxs-lookup"><span data-stu-id="dbd54-148">Microsoft.Azure.Management.Reservations.Models.CalculatePriceResponse</span></span>

## <span data-ttu-id="dbd54-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dbd54-149">NOTES</span></span>

## <span data-ttu-id="dbd54-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dbd54-150">RELATED LINKS</span></span>
