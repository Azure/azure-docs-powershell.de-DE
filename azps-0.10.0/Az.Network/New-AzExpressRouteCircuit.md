---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzExpressRouteCircuit.md
ms.openlocfilehash: d03b52c477686f3aa724057771285eaf9d522a56
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841363"
---
# <span data-ttu-id="28b0f-101">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="28b0f-101">New-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="28b0f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="28b0f-102">SYNOPSIS</span></span>
<span data-ttu-id="28b0f-103">Erstellt einen Azure Express-Routen Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="28b0f-103">Creates an Azure express route circuit.</span></span>

## <span data-ttu-id="28b0f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="28b0f-104">SYNTAX</span></span>

```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String>
 -BandwidthInMbps <Int32>
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28b0f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="28b0f-105">DESCRIPTION</span></span>
<span data-ttu-id="28b0f-106">Das Cmdlet **New-AzExpressRouteCircuit** erstellt einen Azure Express-Routen Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="28b0f-106">The **New-AzExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="28b0f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="28b0f-107">EXAMPLES</span></span>

### <span data-ttu-id="28b0f-108">Beispiel 1: Erstellen eines neuen Express Route-Schaltkreises</span><span class="sxs-lookup"><span data-stu-id="28b0f-108">Example 1: Create a new ExpressRoute circuit</span></span>
```
$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ServiceProviderName='Equinix'
    PeeringLocation='Silicon Valley'
    BandwidthInMbps=200
}
New-AzExpressRouteCircuit @parameters
```

## <span data-ttu-id="28b0f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="28b0f-109">PARAMETERS</span></span>

### <span data-ttu-id="28b0f-110">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="28b0f-110">-AllowClassicOperations</span></span>
<span data-ttu-id="28b0f-111">Die Verwendung dieses Parameters ermöglicht Ihnen, die klassischen Azure PowerShell-Cmdlets zum Verwalten des Schaltkreises zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="28b0f-111">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b0f-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28b0f-112">-AsJob</span></span>
<span data-ttu-id="28b0f-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="28b0f-113">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b0f-114">– Autorisierung</span><span class="sxs-lookup"><span data-stu-id="28b0f-114">-Authorization</span></span>
<span data-ttu-id="28b0f-115">Eine Liste mit Schaltkreis Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="28b0f-115">A list of circuit authorizations.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b0f-116">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="28b0f-116">-BandwidthInMbps</span></span>
<span data-ttu-id="28b0f-117">Die Bandbreite des Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="28b0f-117">The bandwidth of the circuit.</span></span> <span data-ttu-id="28b0f-118">Hierbei muss es sich um einen Wert handeln, der vom Dienstanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="28b0f-118">This must be a value that is supported by the service provider.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b0f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28b0f-119">-DefaultProfile</span></span>
<span data-ttu-id="28b0f-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="28b0f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28b0f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="28b0f-121">-Force</span></span>
<span data-ttu-id="28b0f-122">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="28b0f-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b0f-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="28b0f-123">-Location</span></span>
<span data-ttu-id="28b0f-124">Die Position des Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="28b0f-124">The location of the circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b0f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="28b0f-125">-Name</span></span>
<span data-ttu-id="28b0f-126">Der Name des Express Route-Schaltkreises, der erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="28b0f-126">The name of the ExpressRoute circuit being created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b0f-127">-Peering</span><span class="sxs-lookup"><span data-stu-id="28b0f-127">-Peering</span></span>
<span data-ttu-id="28b0f-128">Eine Liste der Peer Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="28b0f-128">A list peer configurations.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b0f-129">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="28b0f-129">-PeeringLocation</span></span>
<span data-ttu-id="28b0f-130">Der Name des Peering-Standorts, der vom Dienstanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="28b0f-130">The name of the peering location supported by the service provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b0f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28b0f-131">-ResourceGroupName</span></span>
<span data-ttu-id="28b0f-132">Die Ressourcengruppe, die den Schaltkreis enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="28b0f-132">The resource group that will contain the circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b0f-133">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="28b0f-133">-ServiceProviderName</span></span>
<span data-ttu-id="28b0f-134">Der Name des Circuit Service Providers.</span><span class="sxs-lookup"><span data-stu-id="28b0f-134">The name of the circuit service provider.</span></span> <span data-ttu-id="28b0f-135">Dieser muss mit einem vom Get-AzExpressRouteServiceProvider-Cmdlet aufgelisteten Namen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="28b0f-135">This must match a name listed by the Get-AzExpressRouteServiceProvider cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b0f-136">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="28b0f-136">-SkuFamily</span></span>
<span data-ttu-id="28b0f-137">SKU-Familie bestimmt den Abrechnungstyp.</span><span class="sxs-lookup"><span data-stu-id="28b0f-137">SKU family determines the billing type.</span></span> <span data-ttu-id="28b0f-138">Mögliche Werte für diesen Parameter sind: `MeteredData` oder `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="28b0f-138">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="28b0f-139">Beachten Sie, dass Sie den Abrechnungstyp von MeteredData in UnlimitedData ändern können, der Typ aber nicht von UnlimitedData in MeteredData geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="28b0f-139">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: MeteredData, UnlimitedData

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b0f-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="28b0f-140">-SkuTier</span></span>
<span data-ttu-id="28b0f-141">Die Dienstebene für den Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="28b0f-141">The tier of service for the circuit.</span></span> <span data-ttu-id="28b0f-142">Mögliche Werte für diesen Parameter sind: `Standard` oder `Premium` .</span><span class="sxs-lookup"><span data-stu-id="28b0f-142">Possible values for this parameter are: `Standard` or `Premium`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b0f-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="28b0f-143">-Tag</span></span>
<span data-ttu-id="28b0f-144">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="28b0f-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="28b0f-145">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="28b0f-145">For example:</span></span>

<span data-ttu-id="28b0f-146">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="28b0f-146">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b0f-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="28b0f-147">-Confirm</span></span>
<span data-ttu-id="28b0f-148">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="28b0f-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b0f-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28b0f-149">-WhatIf</span></span>
<span data-ttu-id="28b0f-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="28b0f-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28b0f-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="28b0f-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b0f-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28b0f-152">CommonParameters</span></span>
<span data-ttu-id="28b0f-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28b0f-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28b0f-154">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28b0f-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28b0f-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="28b0f-155">INPUTS</span></span>

## <span data-ttu-id="28b0f-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="28b0f-156">OUTPUTS</span></span>

### <span data-ttu-id="28b0f-157">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="28b0f-157">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="28b0f-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="28b0f-158">NOTES</span></span>

## <span data-ttu-id="28b0f-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="28b0f-159">RELATED LINKS</span></span>

[<span data-ttu-id="28b0f-160">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="28b0f-160">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="28b0f-161">Verschieben-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="28b0f-161">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="28b0f-162">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="28b0f-162">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="28b0f-163">Satz-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="28b0f-163">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
