---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
ms.openlocfilehash: 479b89296ae52221f714992791ed73cd14bf2fe0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178746"
---
# <span data-ttu-id="6fa40-101">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6fa40-101">New-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="6fa40-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6fa40-102">SYNOPSIS</span></span>
<span data-ttu-id="6fa40-103">Erstellt einen Azure Express-Routen Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="6fa40-103">Creates an Azure express route circuit.</span></span>

## <span data-ttu-id="6fa40-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fa40-104">SYNTAX</span></span>

### <span data-ttu-id="6fa40-105">Serviceprovider (Standard)</span><span class="sxs-lookup"><span data-stu-id="6fa40-105">ServiceProvider (Default)</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String> -BandwidthInMbps <Int32>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fa40-106">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="6fa40-106">ExpressRoutePort</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ExpressRoutePort <PSExpressRoutePort> -BandwidthInGbps <Double>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fa40-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6fa40-107">DESCRIPTION</span></span>
<span data-ttu-id="6fa40-108">Das Cmdlet **New-AzExpressRouteCircuit** erstellt einen Azure Express-Routen Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="6fa40-108">The **New-AzExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="6fa40-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6fa40-109">EXAMPLES</span></span>

### <span data-ttu-id="6fa40-110">Beispiel 1: Erstellen eines neuen Express Route-Schaltkreises</span><span class="sxs-lookup"><span data-stu-id="6fa40-110">Example 1: Create a new ExpressRoute circuit</span></span>
```powershell
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

### <span data-ttu-id="6fa40-111">Beispiel 2: Erstellen eines neuen Express Route-Schaltkreises auf ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="6fa40-111">Example 2: Create a new ExpressRoute circuit on ExpressRoutePort</span></span>
```powershell
$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ExpressRoutePort=$PSExpressRoutePort
    BandwidthInGbps=10.0
}
New-AzExpressRouteCircuit @parameters
```

## <span data-ttu-id="6fa40-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6fa40-112">PARAMETERS</span></span>

### <span data-ttu-id="6fa40-113">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="6fa40-113">-AllowClassicOperations</span></span>
<span data-ttu-id="6fa40-114">Die Verwendung dieses Parameters ermöglicht Ihnen, die klassischen Azure PowerShell-Cmdlets zum Verwalten des Schaltkreises zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6fa40-114">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fa40-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6fa40-115">-AsJob</span></span>
<span data-ttu-id="6fa40-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6fa40-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fa40-117">– Autorisierung</span><span class="sxs-lookup"><span data-stu-id="6fa40-117">-Authorization</span></span>
<span data-ttu-id="6fa40-118">Eine Liste mit Schaltkreis Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="6fa40-118">A list of circuit authorizations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fa40-119">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="6fa40-119">-BandwidthInGbps</span></span>
<span data-ttu-id="6fa40-120">Die Bandbreite des Schaltkreises, wenn der Schaltkreis für eine ExpressRoutePort-Ressource bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6fa40-120">The bandwidth of the circuit when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: System.Double
Parameter Sets: ExpressRoutePort
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fa40-121">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="6fa40-121">-BandwidthInMbps</span></span>
<span data-ttu-id="6fa40-122">Die Bandbreite des Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="6fa40-122">The bandwidth of the circuit.</span></span> <span data-ttu-id="6fa40-123">Hierbei muss es sich um einen Wert handeln, der vom Dienstanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="6fa40-123">This must be a value that is supported by the service provider.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ServiceProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fa40-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fa40-124">-DefaultProfile</span></span>
<span data-ttu-id="6fa40-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6fa40-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fa40-126">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="6fa40-126">-ExpressRoutePort</span></span>
<span data-ttu-id="6fa40-127">Der Verweis auf die ExpressRoutePort-Ressource, wenn der Schaltkreis für eine ExpressRoutePort-Ressource bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6fa40-127">The reference to the ExpressRoutePort resource when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: ExpressRoutePort
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fa40-128">-Force</span><span class="sxs-lookup"><span data-stu-id="6fa40-128">-Force</span></span>
<span data-ttu-id="6fa40-129">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="6fa40-129">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fa40-130">-Standort</span><span class="sxs-lookup"><span data-stu-id="6fa40-130">-Location</span></span>
<span data-ttu-id="6fa40-131">Die Position des Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="6fa40-131">The location of the circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fa40-132">-Name</span><span class="sxs-lookup"><span data-stu-id="6fa40-132">-Name</span></span>
<span data-ttu-id="6fa40-133">Der Name des Express Route-Schaltkreises, der erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="6fa40-133">The name of the ExpressRoute circuit being created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fa40-134">-Peering</span><span class="sxs-lookup"><span data-stu-id="6fa40-134">-Peering</span></span>
<span data-ttu-id="6fa40-135">Eine Liste der Peer Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="6fa40-135">A list peer configurations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPeering[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fa40-136">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="6fa40-136">-PeeringLocation</span></span>
<span data-ttu-id="6fa40-137">Der Name des Peering-Standorts, der vom Dienstanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="6fa40-137">The name of the peering location supported by the service provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fa40-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fa40-138">-ResourceGroupName</span></span>
<span data-ttu-id="6fa40-139">Die Ressourcengruppe, die den Schaltkreis enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="6fa40-139">The resource group that will contain the circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fa40-140">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="6fa40-140">-ServiceProviderName</span></span>
<span data-ttu-id="6fa40-141">Der Name des Circuit Service Providers.</span><span class="sxs-lookup"><span data-stu-id="6fa40-141">The name of the circuit service provider.</span></span> <span data-ttu-id="6fa40-142">Dieser muss mit einem vom Get-AzExpressRouteServiceProvider-Cmdlet aufgelisteten Namen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="6fa40-142">This must match a name listed by the Get-AzExpressRouteServiceProvider cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fa40-143">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="6fa40-143">-SkuFamily</span></span>
<span data-ttu-id="6fa40-144">SKU-Familie bestimmt den Abrechnungstyp.</span><span class="sxs-lookup"><span data-stu-id="6fa40-144">SKU family determines the billing type.</span></span> <span data-ttu-id="6fa40-145">Mögliche Werte für diesen Parameter sind: `MeteredData` oder `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="6fa40-145">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="6fa40-146">Beachten Sie, dass Sie den Abrechnungstyp von MeteredData in UnlimitedData ändern können, der Typ aber nicht von UnlimitedData in MeteredData geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="6fa40-146">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MeteredData, UnlimitedData

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fa40-147">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="6fa40-147">-SkuTier</span></span>
<span data-ttu-id="6fa40-148">Die Dienstebene für den Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="6fa40-148">The tier of service for the circuit.</span></span> <span data-ttu-id="6fa40-149">Mögliche Werte für diesen Parameter sind: `Standard` `Premium` oder `Local` .</span><span class="sxs-lookup"><span data-stu-id="6fa40-149">Possible values for this parameter are: `Standard`, `Premium` or `Local`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium, Local

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fa40-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="6fa40-150">-Tag</span></span>
<span data-ttu-id="6fa40-151">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="6fa40-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6fa40-152">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="6fa40-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fa40-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6fa40-153">-Confirm</span></span>
<span data-ttu-id="6fa40-154">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6fa40-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fa40-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fa40-155">-WhatIf</span></span>
<span data-ttu-id="6fa40-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6fa40-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fa40-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6fa40-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fa40-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fa40-158">CommonParameters</span></span>
<span data-ttu-id="6fa40-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fa40-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fa40-160">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fa40-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fa40-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6fa40-161">INPUTS</span></span>

### <span data-ttu-id="6fa40-162">System. String</span><span class="sxs-lookup"><span data-stu-id="6fa40-162">System.String</span></span>

### <span data-ttu-id="6fa40-163">System. Int32</span><span class="sxs-lookup"><span data-stu-id="6fa40-163">System.Int32</span></span>

### <span data-ttu-id="6fa40-164">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="6fa40-164">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="6fa40-165">System. Double</span><span class="sxs-lookup"><span data-stu-id="6fa40-165">System.Double</span></span>

### <span data-ttu-id="6fa40-166">Microsoft. Azure. Commands. Network. Models. PSPeering []</span><span class="sxs-lookup"><span data-stu-id="6fa40-166">Microsoft.Azure.Commands.Network.Models.PSPeering[]</span></span>

### <span data-ttu-id="6fa40-167">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization []</span><span class="sxs-lookup"><span data-stu-id="6fa40-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]</span></span>

### <span data-ttu-id="6fa40-168">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6fa40-168">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6fa40-169">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6fa40-169">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6fa40-170">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6fa40-170">OUTPUTS</span></span>

### <span data-ttu-id="6fa40-171">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6fa40-171">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="6fa40-172">Notizen</span><span class="sxs-lookup"><span data-stu-id="6fa40-172">NOTES</span></span>

## <span data-ttu-id="6fa40-173">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6fa40-173">RELATED LINKS</span></span>

[<span data-ttu-id="6fa40-174">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6fa40-174">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="6fa40-175">Verschieben-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6fa40-175">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="6fa40-176">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6fa40-176">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="6fa40-177">Satz-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6fa40-177">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
