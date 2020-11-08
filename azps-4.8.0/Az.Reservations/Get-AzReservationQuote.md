---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationquote
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
ms.openlocfilehash: 844e67f7491825fe0484a60d55cb254988cfb5c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167404"
---
# <span data-ttu-id="8a659-101">Get-AzReservationQuote</span><span class="sxs-lookup"><span data-stu-id="8a659-101">Get-AzReservationQuote</span></span>

## <span data-ttu-id="8a659-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8a659-102">SYNOPSIS</span></span>
<span data-ttu-id="8a659-103">{{Füllen Sie die Zusammenfassung aus}}</span><span class="sxs-lookup"><span data-stu-id="8a659-103">{{ Fill in the Synopsis }}</span></span>

## <span data-ttu-id="8a659-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a659-104">SYNTAX</span></span>

```
Get-AzReservationQuote -ReservedResourceType <String> -Sku <String> [-Location <String>]
 -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32> -DisplayName <String>
 -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>] [-InstanceFlexibility <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a659-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a659-105">DESCRIPTION</span></span>
<span data-ttu-id="8a659-106">Berechnen Sie den Preis für das Platzieren einer Reservierungs Bestellung.</span><span class="sxs-lookup"><span data-stu-id="8a659-106">Calculate price for placing a reservation order.</span></span>

## <span data-ttu-id="8a659-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8a659-107">EXAMPLES</span></span>

### <span data-ttu-id="8a659-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8a659-108">Example 1</span></span>
```powershell
PS C:\> Get-AzReservationQuote -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="8a659-109">Nach dem Abrufen des Katalogs kann der Kunde das unterschiedliche Produkt auf der Grundlage des Standorts erhalten.</span><span class="sxs-lookup"><span data-stu-id="8a659-109">After get catalog, customer can get the differe product based on location.</span></span> <span data-ttu-id="8a659-110">Wenn Sie diese Informationen verwenden, überprüfen Sie den Preis richtig.</span><span class="sxs-lookup"><span data-stu-id="8a659-110">By using those infomation, check the price properly</span></span>

## <span data-ttu-id="8a659-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a659-111">PARAMETERS</span></span>

### <span data-ttu-id="8a659-112">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="8a659-112">-AppliedScope</span></span>
<span data-ttu-id="8a659-113">Abonnement, auf das der Vorteil angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="8a659-113">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="8a659-114">Erforderlich, wenn--Applied-Scope-Type Single ist.</span><span class="sxs-lookup"><span data-stu-id="8a659-114">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="8a659-115">Geben Sie nicht an, ob--Applied-Scope-Type freigegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8a659-115">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="8a659-116">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="8a659-116">-AppliedScopeType</span></span>
<span data-ttu-id="8a659-117">Typ des angewendeten Bereichs zum Aktualisieren der Reservierung mit "einzeln" oder "freigegeben"</span><span class="sxs-lookup"><span data-stu-id="8a659-117">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="8a659-118">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="8a659-118">-BillingPlan</span></span>
<span data-ttu-id="8a659-119">Die für diese SKU verfügbaren Optionen für den Fakturierungsplan.</span><span class="sxs-lookup"><span data-stu-id="8a659-119">The billing plan options available for this SKU.</span></span> <span data-ttu-id="8a659-120">"Monatlich" oder "im voraus"</span><span class="sxs-lookup"><span data-stu-id="8a659-120">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="8a659-121">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="8a659-121">-BillingScopeId</span></span>
<span data-ttu-id="8a659-122">Das Abonnement wird für den Kauf einer Reservierung in Rechnung gestellt.</span><span class="sxs-lookup"><span data-stu-id="8a659-122">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="8a659-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a659-123">-DefaultProfile</span></span>
<span data-ttu-id="8a659-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8a659-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a659-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8a659-125">-DisplayName</span></span>
<span data-ttu-id="8a659-126">Anzeigename für den Benutzer, um die Reservierung einfach zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8a659-126">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="8a659-127">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="8a659-127">-InstanceFlexibility</span></span>
<span data-ttu-id="8a659-128">Der Typ der Instanz Flexibilität, mit der die Reservierung aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8a659-128">Type of the Instance Flexibility to update the reservation with.</span></span>

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

### <span data-ttu-id="8a659-129">-Standort</span><span class="sxs-lookup"><span data-stu-id="8a659-129">-Location</span></span>
<span data-ttu-id="8a659-130">Der Speicherort, an dem die SKU verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="8a659-130">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="8a659-131">-Quantity</span><span class="sxs-lookup"><span data-stu-id="8a659-131">-Quantity</span></span>
<span data-ttu-id="8a659-132">Die Menge des Produkts zur Berechnung des Preises oder des Kaufs.</span><span class="sxs-lookup"><span data-stu-id="8a659-132">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="8a659-133">– Verlängern</span><span class="sxs-lookup"><span data-stu-id="8a659-133">-Renew</span></span>
<span data-ttu-id="8a659-134">Wenn diese Einstellung auf "true" festgelegt ist, wird automatisch eine neue Reservierung für das Ablaufdatum gekauft.</span><span class="sxs-lookup"><span data-stu-id="8a659-134">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="8a659-135">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="8a659-135">-ReservedResourceType</span></span>
<span data-ttu-id="8a659-136">Der Typ der Ressource, für die die SKUs bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8a659-136">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="8a659-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="8a659-137">-Sku</span></span>
<span data-ttu-id="8a659-138">SKU-Name, Abrufen der SKU-Liste mithilfe des Befehls AZ-Reservierungs Katalog anzeigen</span><span class="sxs-lookup"><span data-stu-id="8a659-138">Sku name, get the sku list by using command az reservations catalog show</span></span>

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

### <span data-ttu-id="8a659-139">-Term</span><span class="sxs-lookup"><span data-stu-id="8a659-139">-Term</span></span>
<span data-ttu-id="8a659-140">Die verfügbaren Reservierungsbestimmungen für diese Ressource.</span><span class="sxs-lookup"><span data-stu-id="8a659-140">Available reservation terms for this resource.</span></span>

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

### <span data-ttu-id="8a659-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a659-141">CommonParameters</span></span>
<span data-ttu-id="8a659-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a659-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a659-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a659-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a659-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8a659-144">INPUTS</span></span>

### <span data-ttu-id="8a659-145">Keine</span><span class="sxs-lookup"><span data-stu-id="8a659-145">None</span></span>

## <span data-ttu-id="8a659-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8a659-146">OUTPUTS</span></span>

### <span data-ttu-id="8a659-147">Microsoft. Azure. Management. reservations. Models. CalculatePriceResponse</span><span class="sxs-lookup"><span data-stu-id="8a659-147">Microsoft.Azure.Management.Reservations.Models.CalculatePriceResponse</span></span>

## <span data-ttu-id="8a659-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="8a659-148">NOTES</span></span>

## <span data-ttu-id="8a659-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8a659-149">RELATED LINKS</span></span>
