---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
ms.openlocfilehash: 479b89296ae52221f714992791ed73cd14bf2fe0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151748"
---
# <span data-ttu-id="f2b0b-101">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f2b0b-101">New-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="f2b0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2b0b-102">SYNOPSIS</span></span>
<span data-ttu-id="f2b0b-103">Erstellt einen Azure Express-Routen-Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="f2b0b-103">Creates an Azure express route circuit.</span></span>

## <span data-ttu-id="f2b0b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f2b0b-104">SYNTAX</span></span>

### <span data-ttu-id="f2b0b-105">ServiceProvider (Standard)</span><span class="sxs-lookup"><span data-stu-id="f2b0b-105">ServiceProvider (Default)</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String> -BandwidthInMbps <Int32>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2b0b-106">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f2b0b-106">ExpressRoutePort</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ExpressRoutePort <PSExpressRoutePort> -BandwidthInGbps <Double>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2b0b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2b0b-107">DESCRIPTION</span></span>
<span data-ttu-id="f2b0b-108">Das **Cmdlet "New-AzExpressRouteCircuit"** erstellt einen Azure Express-Routen-Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="f2b0b-108">The **New-AzExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="f2b0b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f2b0b-109">EXAMPLES</span></span>

### <span data-ttu-id="f2b0b-110">Beispiel 1: Erstellen eines neuen "ExpressRoute"-Schaltkreises</span><span class="sxs-lookup"><span data-stu-id="f2b0b-110">Example 1: Create a new ExpressRoute circuit</span></span>
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

### <span data-ttu-id="f2b0b-111">Beispiel 2: Erstellen eines neuen "ExpressRoute"-Schaltkreises auf ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f2b0b-111">Example 2: Create a new ExpressRoute circuit on ExpressRoutePort</span></span>
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

## <span data-ttu-id="f2b0b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2b0b-112">PARAMETERS</span></span>

### <span data-ttu-id="f2b0b-113">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="f2b0b-113">-AllowClassicOperations</span></span>
<span data-ttu-id="f2b0b-114">Die Verwendung dieses Parameters ermöglicht ihnen die Verwendung der klassischen Azure PowerShell-Cmdlets zum Verwalten des Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="f2b0b-114">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

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

### <span data-ttu-id="f2b0b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2b0b-115">-AsJob</span></span>
<span data-ttu-id="f2b0b-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f2b0b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f2b0b-117">-Authorization</span><span class="sxs-lookup"><span data-stu-id="f2b0b-117">-Authorization</span></span>
<span data-ttu-id="f2b0b-118">Eine Liste der Schaltkreisautorisierungen.</span><span class="sxs-lookup"><span data-stu-id="f2b0b-118">A list of circuit authorizations.</span></span>

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

### <span data-ttu-id="f2b0b-119">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="f2b0b-119">-BandwidthInGbps</span></span>
<span data-ttu-id="f2b0b-120">Die Bandbreite des Schaltkreises, wenn der Schaltkreis für eine ExpressRoutePort-Ressource bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f2b0b-120">The bandwidth of the circuit when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="f2b0b-121">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="f2b0b-121">-BandwidthInMbps</span></span>
<span data-ttu-id="f2b0b-122">Die Bandbreite des Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="f2b0b-122">The bandwidth of the circuit.</span></span> <span data-ttu-id="f2b0b-123">Dies muss ein Wert sein, der vom Dienstanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="f2b0b-123">This must be a value that is supported by the service provider.</span></span>

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

### <span data-ttu-id="f2b0b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2b0b-124">-DefaultProfile</span></span>
<span data-ttu-id="f2b0b-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f2b0b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2b0b-126">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f2b0b-126">-ExpressRoutePort</span></span>
<span data-ttu-id="f2b0b-127">Der Verweis auf die ExpressRoutePort-Ressource, wenn der Schaltkreis für eine ExpressRoutePort-Ressource bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f2b0b-127">The reference to the ExpressRoutePort resource when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="f2b0b-128">-Force</span><span class="sxs-lookup"><span data-stu-id="f2b0b-128">-Force</span></span>
<span data-ttu-id="f2b0b-129">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="f2b0b-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f2b0b-130">-Location</span><span class="sxs-lookup"><span data-stu-id="f2b0b-130">-Location</span></span>
<span data-ttu-id="f2b0b-131">Die Position des Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="f2b0b-131">The location of the circuit.</span></span>

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

### <span data-ttu-id="f2b0b-132">-Name</span><span class="sxs-lookup"><span data-stu-id="f2b0b-132">-Name</span></span>
<span data-ttu-id="f2b0b-133">Der Name des zu erstellende ExpressRoute-Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="f2b0b-133">The name of the ExpressRoute circuit being created.</span></span>

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

### <span data-ttu-id="f2b0b-134">-Peering</span><span class="sxs-lookup"><span data-stu-id="f2b0b-134">-Peering</span></span>
<span data-ttu-id="f2b0b-135">Eine Listen-Peer-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f2b0b-135">A list peer configurations.</span></span>

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

### <span data-ttu-id="f2b0b-136">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="f2b0b-136">-PeeringLocation</span></span>
<span data-ttu-id="f2b0b-137">Der Name des vom Dienstanbieter unterstützten Peeringstandorts.</span><span class="sxs-lookup"><span data-stu-id="f2b0b-137">The name of the peering location supported by the service provider.</span></span>

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

### <span data-ttu-id="f2b0b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2b0b-138">-ResourceGroupName</span></span>
<span data-ttu-id="f2b0b-139">Die Ressourcengruppe, die den Schaltkreis enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="f2b0b-139">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="f2b0b-140">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="f2b0b-140">-ServiceProviderName</span></span>
<span data-ttu-id="f2b0b-141">Der Name des Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="f2b0b-141">The name of the circuit service provider.</span></span> <span data-ttu-id="f2b0b-142">Dies muss mit einem Namen übereinstimmen, der im cmdlet Get-AzExpressRouteServiceProvider wird.</span><span class="sxs-lookup"><span data-stu-id="f2b0b-142">This must match a name listed by the Get-AzExpressRouteServiceProvider cmdlet.</span></span>

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

### <span data-ttu-id="f2b0b-143">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="f2b0b-143">-SkuFamily</span></span>
<span data-ttu-id="f2b0b-144">Die SKU-Familie bestimmt den Abrechnungstyp.</span><span class="sxs-lookup"><span data-stu-id="f2b0b-144">SKU family determines the billing type.</span></span> <span data-ttu-id="f2b0b-145">Mögliche Werte für diesen Parameter sind: `MeteredData` oder `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="f2b0b-145">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="f2b0b-146">Beachten Sie, dass Sie den Abrechnungstyp von "MeteredData" in "UnlimitedData" ändern können, nicht jedoch den Typ von "UnlimitedData" in "MeteredData".</span><span class="sxs-lookup"><span data-stu-id="f2b0b-146">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

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

### <span data-ttu-id="f2b0b-147">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="f2b0b-147">-SkuTier</span></span>
<span data-ttu-id="f2b0b-148">Die Dienststufe für den Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="f2b0b-148">The tier of service for the circuit.</span></span> <span data-ttu-id="f2b0b-149">Mögliche Werte für diesen Parameter sind: `Standard` oder `Premium` `Local` .</span><span class="sxs-lookup"><span data-stu-id="f2b0b-149">Possible values for this parameter are: `Standard`, `Premium` or `Local`.</span></span>

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

### <span data-ttu-id="f2b0b-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="f2b0b-150">-Tag</span></span>
<span data-ttu-id="f2b0b-151">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="f2b0b-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f2b0b-152">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="f2b0b-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f2b0b-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2b0b-153">-Confirm</span></span>
<span data-ttu-id="f2b0b-154">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f2b0b-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2b0b-155">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f2b0b-155">-WhatIf</span></span>
<span data-ttu-id="f2b0b-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f2b0b-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2b0b-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f2b0b-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2b0b-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2b0b-158">CommonParameters</span></span>
<span data-ttu-id="f2b0b-159">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2b0b-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2b0b-160">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2b0b-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2b0b-161">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f2b0b-161">INPUTS</span></span>

### <span data-ttu-id="f2b0b-162">System.String</span><span class="sxs-lookup"><span data-stu-id="f2b0b-162">System.String</span></span>

### <span data-ttu-id="f2b0b-163">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f2b0b-163">System.Int32</span></span>

### <span data-ttu-id="f2b0b-164">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f2b0b-164">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="f2b0b-165">System.Double</span><span class="sxs-lookup"><span data-stu-id="f2b0b-165">System.Double</span></span>

### <span data-ttu-id="f2b0b-166">Microsoft.Azure.Commands.Network.Models.PSPeering[]</span><span class="sxs-lookup"><span data-stu-id="f2b0b-166">Microsoft.Azure.Commands.Network.Models.PSPeering[]</span></span>

### <span data-ttu-id="f2b0b-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]</span><span class="sxs-lookup"><span data-stu-id="f2b0b-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]</span></span>

### <span data-ttu-id="f2b0b-168">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f2b0b-168">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f2b0b-169">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f2b0b-169">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f2b0b-170">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f2b0b-170">OUTPUTS</span></span>

### <span data-ttu-id="f2b0b-171">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f2b0b-171">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="f2b0b-172">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f2b0b-172">NOTES</span></span>

## <span data-ttu-id="f2b0b-173">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f2b0b-173">RELATED LINKS</span></span>

[<span data-ttu-id="f2b0b-174">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f2b0b-174">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="f2b0b-175">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f2b0b-175">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="f2b0b-176">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f2b0b-176">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="f2b0b-177">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f2b0b-177">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
