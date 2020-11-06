---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 0c611edc0ef8cb117e556a19e22f93d1f8db96ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499758"
---
# <span data-ttu-id="8f59f-101">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8f59f-101">New-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="8f59f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8f59f-102">SYNOPSIS</span></span>
<span data-ttu-id="8f59f-103">Erstellt einen Azure Express-Routen Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="8f59f-103">Creates an Azure express route circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f59f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f59f-104">SYNTAX</span></span>

```
New-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String>
 -BandwidthInMbps <Int32>
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f59f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8f59f-105">DESCRIPTION</span></span>
<span data-ttu-id="8f59f-106">Das Cmdlet **New-AzureRmExpressRouteCircuit** erstellt einen Azure Express-Routen Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="8f59f-106">The **New-AzureRmExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="8f59f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8f59f-107">EXAMPLES</span></span>

### <span data-ttu-id="8f59f-108">Beispiel 1: Erstellen eines neuen Express Route-Schaltkreises</span><span class="sxs-lookup"><span data-stu-id="8f59f-108">Example 1: Create a new ExpressRoute circuit</span></span>
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
New-AzureRmExpressRouteCircuit @parameters
```

## <span data-ttu-id="8f59f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f59f-109">PARAMETERS</span></span>

### <span data-ttu-id="8f59f-110">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="8f59f-110">-AllowClassicOperations</span></span>
<span data-ttu-id="8f59f-111">Die Verwendung dieses Parameters ermöglicht Ihnen, die klassischen Azure PowerShell-Cmdlets zum Verwalten des Schaltkreises zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8f59f-111">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

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

### <span data-ttu-id="8f59f-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f59f-112">-AsJob</span></span>
<span data-ttu-id="8f59f-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8f59f-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8f59f-114">– Autorisierung</span><span class="sxs-lookup"><span data-stu-id="8f59f-114">-Authorization</span></span>
<span data-ttu-id="8f59f-115">Eine Liste mit Schaltkreis Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="8f59f-115">A list of circuit authorizations.</span></span>

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

### <span data-ttu-id="8f59f-116">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="8f59f-116">-BandwidthInMbps</span></span>
<span data-ttu-id="8f59f-117">Die Bandbreite des Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="8f59f-117">The bandwidth of the circuit.</span></span> <span data-ttu-id="8f59f-118">Hierbei muss es sich um einen Wert handeln, der vom Dienstanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="8f59f-118">This must be a value that is supported by the service provider.</span></span>

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

### <span data-ttu-id="8f59f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f59f-119">-DefaultProfile</span></span>
<span data-ttu-id="8f59f-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8f59f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f59f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="8f59f-121">-Force</span></span>
<span data-ttu-id="8f59f-122">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="8f59f-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8f59f-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="8f59f-123">-Location</span></span>
<span data-ttu-id="8f59f-124">Die Position des Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="8f59f-124">The location of the circuit.</span></span>

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

### <span data-ttu-id="8f59f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="8f59f-125">-Name</span></span>
<span data-ttu-id="8f59f-126">Der Name des Express Route-Schaltkreises, der erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8f59f-126">The name of the ExpressRoute circuit being created.</span></span>

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

### <span data-ttu-id="8f59f-127">-Peering</span><span class="sxs-lookup"><span data-stu-id="8f59f-127">-Peering</span></span>
<span data-ttu-id="8f59f-128">Eine Liste der Peer Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="8f59f-128">A list peer configurations.</span></span>

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

### <span data-ttu-id="8f59f-129">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="8f59f-129">-PeeringLocation</span></span>
<span data-ttu-id="8f59f-130">Der Name des Peering-Standorts, der vom Dienstanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="8f59f-130">The name of the peering location supported by the service provider.</span></span>

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

### <span data-ttu-id="8f59f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f59f-131">-ResourceGroupName</span></span>
<span data-ttu-id="8f59f-132">Die Ressourcengruppe, die den Schaltkreis enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="8f59f-132">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="8f59f-133">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="8f59f-133">-ServiceProviderName</span></span>
<span data-ttu-id="8f59f-134">Der Name des Circuit Service Providers.</span><span class="sxs-lookup"><span data-stu-id="8f59f-134">The name of the circuit service provider.</span></span> <span data-ttu-id="8f59f-135">Dieser muss mit einem vom Get-AzureRmExpressRouteServiceProvider-Cmdlet aufgelisteten Namen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="8f59f-135">This must match a name listed by the Get-AzureRmExpressRouteServiceProvider cmdlet.</span></span>

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

### <span data-ttu-id="8f59f-136">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="8f59f-136">-SkuFamily</span></span>
<span data-ttu-id="8f59f-137">SKU-Familie bestimmt den Abrechnungstyp.</span><span class="sxs-lookup"><span data-stu-id="8f59f-137">SKU family determines the billing type.</span></span> <span data-ttu-id="8f59f-138">Mögliche Werte für diesen Parameter sind: `MeteredData` oder `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="8f59f-138">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="8f59f-139">Beachten Sie, dass Sie den Abrechnungstyp von MeteredData in UnlimitedData ändern können, der Typ aber nicht von UnlimitedData in MeteredData geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="8f59f-139">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

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

### <span data-ttu-id="8f59f-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="8f59f-140">-SkuTier</span></span>
<span data-ttu-id="8f59f-141">Die Dienstebene für den Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="8f59f-141">The tier of service for the circuit.</span></span> <span data-ttu-id="8f59f-142">Mögliche Werte für diesen Parameter sind: `Standard` oder `Premium` .</span><span class="sxs-lookup"><span data-stu-id="8f59f-142">Possible values for this parameter are: `Standard` or `Premium`.</span></span>

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

### <span data-ttu-id="8f59f-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="8f59f-143">-Tag</span></span>
<span data-ttu-id="8f59f-144">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="8f59f-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8f59f-145">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8f59f-145">For example:</span></span>

<span data-ttu-id="8f59f-146">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="8f59f-146">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8f59f-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8f59f-147">-Confirm</span></span>
<span data-ttu-id="8f59f-148">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8f59f-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f59f-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f59f-149">-WhatIf</span></span>
<span data-ttu-id="8f59f-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8f59f-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f59f-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8f59f-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f59f-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f59f-152">CommonParameters</span></span>
<span data-ttu-id="8f59f-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f59f-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f59f-154">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f59f-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f59f-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8f59f-155">INPUTS</span></span>

### <span data-ttu-id="8f59f-156">Keine</span><span class="sxs-lookup"><span data-stu-id="8f59f-156">None</span></span>
<span data-ttu-id="8f59f-157">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="8f59f-157">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8f59f-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8f59f-158">OUTPUTS</span></span>

### <span data-ttu-id="8f59f-159">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8f59f-159">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="8f59f-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="8f59f-160">NOTES</span></span>

## <span data-ttu-id="8f59f-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8f59f-161">RELATED LINKS</span></span>

[<span data-ttu-id="8f59f-162">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8f59f-162">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="8f59f-163">Verschieben-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8f59f-163">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="8f59f-164">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8f59f-164">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="8f59f-165">Satz-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8f59f-165">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
