---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/get-azreservationquote
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
ms.openlocfilehash: 3a06de95cedd0ea38fa38b2fb8784e553ae6f4d7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943684"
---
# <span data-ttu-id="b76a6-101">Get-AzReservationQuote</span><span class="sxs-lookup"><span data-stu-id="b76a6-101">Get-AzReservationQuote</span></span>

## <span data-ttu-id="b76a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b76a6-102">SYNOPSIS</span></span>
<span data-ttu-id="b76a6-103">Erhalten Sie ein Angebot für die Reservierung.</span><span class="sxs-lookup"><span data-stu-id="b76a6-103">Get a quote for the reservation.</span></span> <span data-ttu-id="b76a6-104">Dies wird an `New-AzReservation` den Kauf übergeben.</span><span class="sxs-lookup"><span data-stu-id="b76a6-104">This is passed to `New-AzReservation` to purchase.</span></span>

## <span data-ttu-id="b76a6-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b76a6-105">SYNTAX</span></span>

```
Get-AzReservationQuote -ReservedResourceType <String> -Sku <String> [-Location <String>]
 -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32> -DisplayName <String>
 -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>] [-InstanceFlexibility <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b76a6-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b76a6-106">DESCRIPTION</span></span>
<span data-ttu-id="b76a6-107">Berechnen sie den Preis für die Bestellung einer Reservierung.</span><span class="sxs-lookup"><span data-stu-id="b76a6-107">Calculate price for placing a reservation order.</span></span>

## <span data-ttu-id="b76a6-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b76a6-108">EXAMPLES</span></span>

### <span data-ttu-id="b76a6-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b76a6-109">Example 1</span></span>
```powershell
PS C:\> Get-AzReservationQuote -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="b76a6-110">Nach dem Herunterladen des Katalogs kann der Kunde das unterschiedliche Produkt je nach Standort erhalten.</span><span class="sxs-lookup"><span data-stu-id="b76a6-110">After get catalog, customer can get the differe product based on location.</span></span> <span data-ttu-id="b76a6-111">Überprüfen Sie anhand dieser Informationen den Preis ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="b76a6-111">By using those infomation, check the price properly</span></span>

## <span data-ttu-id="b76a6-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b76a6-112">PARAMETERS</span></span>

### <span data-ttu-id="b76a6-113">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="b76a6-113">-AppliedScope</span></span>
<span data-ttu-id="b76a6-114">Abonnement, für das der Vorteil angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="b76a6-114">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="b76a6-115">Erforderlich, wenn --applied-scope-type single ist.</span><span class="sxs-lookup"><span data-stu-id="b76a6-115">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="b76a6-116">Geben Sie nicht an, ob --applied-scope-type freigegeben ist.</span><span class="sxs-lookup"><span data-stu-id="b76a6-116">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="b76a6-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="b76a6-117">-AppliedScopeType</span></span>
<span data-ttu-id="b76a6-118">Typ des angewendeten Bereichs zum Aktualisieren der Reservierung mit "Single" oder "Shared"</span><span class="sxs-lookup"><span data-stu-id="b76a6-118">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="b76a6-119">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="b76a6-119">-BillingPlan</span></span>
<span data-ttu-id="b76a6-120">Die für diese SKU verfügbaren Abrechnungsplanoptionen.</span><span class="sxs-lookup"><span data-stu-id="b76a6-120">The billing plan options available for this SKU.</span></span> <span data-ttu-id="b76a6-121">"Monatlich" oder "Vorab"</span><span class="sxs-lookup"><span data-stu-id="b76a6-121">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="b76a6-122">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="b76a6-122">-BillingScopeId</span></span>
<span data-ttu-id="b76a6-123">Abonnement, das für den Kauf der Reservierung in Rechnung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="b76a6-123">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="b76a6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b76a6-124">-DefaultProfile</span></span>
<span data-ttu-id="b76a6-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b76a6-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b76a6-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b76a6-126">-DisplayName</span></span>
<span data-ttu-id="b76a6-127">Anzeigename für den Benutzer, um die Reservierung ganz einfach zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b76a6-127">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="b76a6-128">-InstanzFlexibilität</span><span class="sxs-lookup"><span data-stu-id="b76a6-128">-InstanceFlexibility</span></span>
<span data-ttu-id="b76a6-129">Typ der Instanzflexibilität zum Aktualisieren der Reservierung mit.</span><span class="sxs-lookup"><span data-stu-id="b76a6-129">Type of the Instance Flexibility to update the reservation with.</span></span>

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

### <span data-ttu-id="b76a6-130">-Location</span><span class="sxs-lookup"><span data-stu-id="b76a6-130">-Location</span></span>
<span data-ttu-id="b76a6-131">Speicherort, an dem die SKU verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b76a6-131">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="b76a6-132">-Quantity</span><span class="sxs-lookup"><span data-stu-id="b76a6-132">-Quantity</span></span>
<span data-ttu-id="b76a6-133">Menge des Produkts zur Berechnung von Preis oder Einkauf.</span><span class="sxs-lookup"><span data-stu-id="b76a6-133">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="b76a6-134">-Verlängern</span><span class="sxs-lookup"><span data-stu-id="b76a6-134">-Renew</span></span>
<span data-ttu-id="b76a6-135">Wenn Sie diesen Wert auf "true" festlegen, wird automatisch eine neue Reservierung zum Ablaufdatum kauft.</span><span class="sxs-lookup"><span data-stu-id="b76a6-135">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="b76a6-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="b76a6-136">-ReservedResourceType</span></span>
<span data-ttu-id="b76a6-137">Typ der Ressource, für die der Skus bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b76a6-137">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="b76a6-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="b76a6-138">-Sku</span></span>
<span data-ttu-id="b76a6-139">Sku-Name, Sku-Liste mithilfe des Befehls az reservierungskatalog anzeigen</span><span class="sxs-lookup"><span data-stu-id="b76a6-139">Sku name, get the sku list by using command az reservations catalog show</span></span>

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

### <span data-ttu-id="b76a6-140">-Ausdruck</span><span class="sxs-lookup"><span data-stu-id="b76a6-140">-Term</span></span>
<span data-ttu-id="b76a6-141">Verfügbare Reservierungsbedingungen für diese Ressource.</span><span class="sxs-lookup"><span data-stu-id="b76a6-141">Available reservation terms for this resource.</span></span>

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

### <span data-ttu-id="b76a6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b76a6-142">CommonParameters</span></span>
<span data-ttu-id="b76a6-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b76a6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b76a6-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b76a6-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b76a6-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b76a6-145">INPUTS</span></span>

### <span data-ttu-id="b76a6-146">Keine</span><span class="sxs-lookup"><span data-stu-id="b76a6-146">None</span></span>

## <span data-ttu-id="b76a6-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b76a6-147">OUTPUTS</span></span>

### <span data-ttu-id="b76a6-148">Microsoft.Azure.Management.Reservations.Models.CalculatePriceResponse</span><span class="sxs-lookup"><span data-stu-id="b76a6-148">Microsoft.Azure.Management.Reservations.Models.CalculatePriceResponse</span></span>

## <span data-ttu-id="b76a6-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b76a6-149">NOTES</span></span>

## <span data-ttu-id="b76a6-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b76a6-150">RELATED LINKS</span></span>
