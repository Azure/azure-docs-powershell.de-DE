---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: cee0318367ad764a9cc9e37995f092462cd157a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495921"
---
# <span data-ttu-id="50bb3-101">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="50bb3-101">New-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="50bb3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="50bb3-102">SYNOPSIS</span></span>
<span data-ttu-id="50bb3-103">Erstellt einen Azure Express-Routen Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="50bb3-103">Creates an Azure express route circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50bb3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="50bb3-104">SYNTAX</span></span>

### <span data-ttu-id="50bb3-105">Serviceprovider</span><span class="sxs-lookup"><span data-stu-id="50bb3-105">ServiceProvider</span></span>
```
New-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] [-ServiceProviderName <String>] [-PeeringLocation <String>]
 [-BandwidthInMbps <Int32>]
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50bb3-106">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="50bb3-106">ExpressRoutePort</span></span>
```
New-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] [-ExpressRoutePort <PSExpressRoutePort>] [-BandwidthInGbps <Double>]
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50bb3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="50bb3-107">DESCRIPTION</span></span>
<span data-ttu-id="50bb3-108">Das Cmdlet **New-AzureRmExpressRouteCircuit** erstellt einen Azure Express-Routen Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="50bb3-108">The **New-AzureRmExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="50bb3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="50bb3-109">EXAMPLES</span></span>

### <span data-ttu-id="50bb3-110">Beispiel 1: Erstellen eines neuen Express Route-Schaltkreises</span><span class="sxs-lookup"><span data-stu-id="50bb3-110">Example 1: Create a new ExpressRoute circuit</span></span>
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

### <span data-ttu-id="50bb3-111">Beispiel 2: Erstellen eines neuen Express Route-Schaltkreises auf ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="50bb3-111">Example 2: Create a new ExpressRoute circuit on ExpressRoutePort</span></span>
```
$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ExpressRoutePort=$PSExpressRoutePort
    BandwidthInGbps=10.0
}
New-AzureRmExpressRouteCircuit @parameters
```

## <span data-ttu-id="50bb3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="50bb3-112">PARAMETERS</span></span>

### <span data-ttu-id="50bb3-113">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="50bb3-113">-AllowClassicOperations</span></span>
<span data-ttu-id="50bb3-114">Die Verwendung dieses Parameters ermöglicht Ihnen, die klassischen Azure PowerShell-Cmdlets zum Verwalten des Schaltkreises zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="50bb3-114">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

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

### <span data-ttu-id="50bb3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50bb3-115">-AsJob</span></span>
<span data-ttu-id="50bb3-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="50bb3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="50bb3-117">– Autorisierung</span><span class="sxs-lookup"><span data-stu-id="50bb3-117">-Authorization</span></span>
<span data-ttu-id="50bb3-118">Eine Liste mit Schaltkreis Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="50bb3-118">A list of circuit authorizations.</span></span>

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

### <span data-ttu-id="50bb3-119">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="50bb3-119">-BandwidthInGbps</span></span>
<span data-ttu-id="50bb3-120">Die Bandbreite des Schaltkreises, wenn der Schaltkreis für eine ExpressRoutePort-Ressource bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="50bb3-120">The bandwidth of the circuit when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: Double
Parameter Sets: ExpressRoutePort
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50bb3-121">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="50bb3-121">-BandwidthInMbps</span></span>
<span data-ttu-id="50bb3-122">Die Bandbreite des Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="50bb3-122">The bandwidth of the circuit.</span></span> <span data-ttu-id="50bb3-123">Hierbei muss es sich um einen Wert handeln, der vom Dienstanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="50bb3-123">This must be a value that is supported by the service provider.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ServiceProvider
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50bb3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50bb3-124">-DefaultProfile</span></span>
<span data-ttu-id="50bb3-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="50bb3-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50bb3-126">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="50bb3-126">-ExpressRoutePort</span></span>
<span data-ttu-id="50bb3-127">Der Verweis auf die ExpressRoutePort-Ressource, wenn der Schaltkreis für eine ExpressRoutePort-Ressource bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="50bb3-127">The reference to the ExpressRoutePort resource when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: PSExpressRoutePort
Parameter Sets: ExpressRoutePort
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50bb3-128">-Force</span><span class="sxs-lookup"><span data-stu-id="50bb3-128">-Force</span></span>
<span data-ttu-id="50bb3-129">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="50bb3-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="50bb3-130">-Standort</span><span class="sxs-lookup"><span data-stu-id="50bb3-130">-Location</span></span>
<span data-ttu-id="50bb3-131">Die Position des Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="50bb3-131">The location of the circuit.</span></span>

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

### <span data-ttu-id="50bb3-132">-Name</span><span class="sxs-lookup"><span data-stu-id="50bb3-132">-Name</span></span>
<span data-ttu-id="50bb3-133">Der Name des Express Route-Schaltkreises, der erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="50bb3-133">The name of the ExpressRoute circuit being created.</span></span>

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

### <span data-ttu-id="50bb3-134">-Peering</span><span class="sxs-lookup"><span data-stu-id="50bb3-134">-Peering</span></span>
<span data-ttu-id="50bb3-135">Eine Liste der Peer Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="50bb3-135">A list peer configurations.</span></span>

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

### <span data-ttu-id="50bb3-136">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="50bb3-136">-PeeringLocation</span></span>
<span data-ttu-id="50bb3-137">Der Name des Peering-Standorts, der vom Dienstanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="50bb3-137">The name of the peering location supported by the service provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50bb3-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50bb3-138">-ResourceGroupName</span></span>
<span data-ttu-id="50bb3-139">Die Ressourcengruppe, die den Schaltkreis enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="50bb3-139">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="50bb3-140">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="50bb3-140">-ServiceProviderName</span></span>
<span data-ttu-id="50bb3-141">Der Name des Circuit Service Providers.</span><span class="sxs-lookup"><span data-stu-id="50bb3-141">The name of the circuit service provider.</span></span> <span data-ttu-id="50bb3-142">Dieser muss mit einem vom Get-AzureRmExpressRouteServiceProvider-Cmdlet aufgelisteten Namen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="50bb3-142">This must match a name listed by the Get-AzureRmExpressRouteServiceProvider cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50bb3-143">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="50bb3-143">-SkuFamily</span></span>
<span data-ttu-id="50bb3-144">SKU-Familie bestimmt den Abrechnungstyp.</span><span class="sxs-lookup"><span data-stu-id="50bb3-144">SKU family determines the billing type.</span></span> <span data-ttu-id="50bb3-145">Mögliche Werte für diesen Parameter sind: `MeteredData` oder `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="50bb3-145">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="50bb3-146">Beachten Sie, dass Sie den Abrechnungstyp von MeteredData in UnlimitedData ändern können, der Typ aber nicht von UnlimitedData in MeteredData geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="50bb3-146">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

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

### <span data-ttu-id="50bb3-147">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="50bb3-147">-SkuTier</span></span>
<span data-ttu-id="50bb3-148">Die Dienstebene für den Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="50bb3-148">The tier of service for the circuit.</span></span> <span data-ttu-id="50bb3-149">Mögliche Werte für diesen Parameter sind: `Standard` oder `Premium` .</span><span class="sxs-lookup"><span data-stu-id="50bb3-149">Possible values for this parameter are: `Standard` or `Premium`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50bb3-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="50bb3-150">-Tag</span></span>
<span data-ttu-id="50bb3-151">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="50bb3-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="50bb3-152">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="50bb3-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="50bb3-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="50bb3-153">-Confirm</span></span>
<span data-ttu-id="50bb3-154">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="50bb3-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50bb3-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50bb3-155">-WhatIf</span></span>
<span data-ttu-id="50bb3-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="50bb3-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50bb3-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="50bb3-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50bb3-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50bb3-158">CommonParameters</span></span>
<span data-ttu-id="50bb3-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50bb3-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50bb3-160">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50bb3-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50bb3-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="50bb3-161">INPUTS</span></span>

### <span data-ttu-id="50bb3-162">System. String</span><span class="sxs-lookup"><span data-stu-id="50bb3-162">System.String</span></span>

### <span data-ttu-id="50bb3-163">System. Int32</span><span class="sxs-lookup"><span data-stu-id="50bb3-163">System.Int32</span></span>

### <span data-ttu-id="50bb3-164">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSPeering, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="50bb3-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPeering, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="50bb3-165">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="50bb3-165">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="50bb3-166">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="50bb3-166">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="50bb3-167">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="50bb3-167">System.Collections.Hashtable</span></span>

## <span data-ttu-id="50bb3-168">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="50bb3-168">OUTPUTS</span></span>

### <span data-ttu-id="50bb3-169">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="50bb3-169">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="50bb3-170">Notizen</span><span class="sxs-lookup"><span data-stu-id="50bb3-170">NOTES</span></span>

## <span data-ttu-id="50bb3-171">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="50bb3-171">RELATED LINKS</span></span>

[<span data-ttu-id="50bb3-172">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="50bb3-172">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="50bb3-173">Verschieben-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="50bb3-173">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="50bb3-174">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="50bb3-174">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="50bb3-175">Satz-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="50bb3-175">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
