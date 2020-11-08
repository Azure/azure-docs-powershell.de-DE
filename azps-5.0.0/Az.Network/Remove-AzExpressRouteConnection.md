---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
ms.openlocfilehash: 324999280df465a6fad621b6c4892e02cdd6e106
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178724"
---
# <span data-ttu-id="6ae06-101">Remove-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="6ae06-101">Remove-AzExpressRouteConnection</span></span>

## <span data-ttu-id="6ae06-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6ae06-102">SYNOPSIS</span></span>
<span data-ttu-id="6ae06-103">Entfernt eine ExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="6ae06-103">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="6ae06-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ae06-104">SYNTAX</span></span>

### <span data-ttu-id="6ae06-105">ByExpressRouteConnectionName (Standard)</span><span class="sxs-lookup"><span data-stu-id="6ae06-105">ByExpressRouteConnectionName (Default)</span></span>
```
Remove-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ae06-106">ByExpressRouteConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="6ae06-106">ByExpressRouteConnectionResourceId</span></span>
```
Remove-AzExpressRouteConnection -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ae06-107">ByExpressRouteConnectionObject</span><span class="sxs-lookup"><span data-stu-id="6ae06-107">ByExpressRouteConnectionObject</span></span>
```
Remove-AzExpressRouteConnection -InputObject <PSExpressRouteConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ae06-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6ae06-108">DESCRIPTION</span></span>
<span data-ttu-id="6ae06-109">Entfernt eine ExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="6ae06-109">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="6ae06-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6ae06-110">EXAMPLES</span></span>

### <span data-ttu-id="6ae06-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6ae06-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> $ExpressRouteGateway = Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"
PS C:\> $ExpressRouteCircuit = New-AzExpressRouteCircuit -ResourceGroupName "testRG" -Name "testExpressRouteCircuit" -Location "West Central US" -SkuTier Premium -SkuFamily MeteredData -ServiceProviderName "Equinix" -PeeringLocation "Silicon Valley" -BandwidthInMbps 200
PS C:\> Add-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ExpressRouteCircuit -PeeringType AzurePrivatePeering -PeerASN 100 -PrimaryPeerAddressPrefix "123.0.0.0/30" -SecondaryPeerAddressPrefix "123.0.0.4/30" -VlanId 300
PS C:\> $ExpressRouteCircuit = Set-AzExpressRouteCircuit -ExpressRouteCircuit $ExpressRouteCircuit
PS C:\> $ExpressRouteCircuitPeeringId = $ExpressRouteCircuit.Peerings[0].Id
PS C:\> New-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" -ExpressRouteCircuitPeeringId $ExpressRouteCircuitPeeringId -RoutingWeight 20
PS C:\> Remove-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection"
```

<span data-ttu-id="6ae06-112">Das obige wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtuelles Drehkreuz in West US in der Ressourcengruppe "testRG" in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="6ae06-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="6ae06-113">Anschließend wird ein Express Route-Gateway im virtuellen Hub mit zwei Skaleneinheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="6ae06-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="6ae06-114">Nachdem das Gateway erstellt wurde, wird es mit dem ExpressRouteSite mit dem Befehl New-AzExpressRouteConnection verbunden.</span><span class="sxs-lookup"><span data-stu-id="6ae06-114">Once the gateway has been created, it is connected to the ExpressRouteSite using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="6ae06-115">Anschließend wird die Verbindung mit dem Verbindungsnamen entfernt.</span><span class="sxs-lookup"><span data-stu-id="6ae06-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="6ae06-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6ae06-116">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> $ExpressRouteGateway = Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"
PS C:\> $ExpressRouteCircuit = New-AzExpressRouteCircuit -ResourceGroupName "testRG" -Name "testExpressRouteCircuit" -Location "West Central US" -SkuTier Premium -SkuFamily MeteredData -ServiceProviderName "Equinix" -PeeringLocation "Silicon Valley" -BandwidthInMbps 200
PS C:\> Add-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ExpressRouteCircuit -PeeringType AzurePrivatePeering -PeerASN 100 -PrimaryPeerAddressPrefix "123.0.0.0/30" -SecondaryPeerAddressPrefix "123.0.0.4/30" -VlanId 300
PS C:\> $ExpressRouteCircuit = Set-AzExpressRouteCircuit -ExpressRouteCircuit $ExpressRouteCircuit
PS C:\> $ExpressRouteCircuitPeeringId = $ExpressRouteCircuit.Peerings[0].Id
PS C:\> New-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" -ExpressRouteCircuitPeeringId $ExpressRouteCircuitPeeringId -RoutingWeight 20
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" | Remove-AzExpressRouteConnection
```

<span data-ttu-id="6ae06-117">Identisch mit Beispiel 1, aber jetzt wird die Verbindung mit dem piped-Objekt aus Get-AzExpressRouteConnection entfernt.</span><span class="sxs-lookup"><span data-stu-id="6ae06-117">Same as example 1, but it now removes the connection using the piped object from Get-AzExpressRouteConnection.</span></span>

## <span data-ttu-id="6ae06-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ae06-118">PARAMETERS</span></span>

### <span data-ttu-id="6ae06-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ae06-119">-DefaultProfile</span></span>
<span data-ttu-id="6ae06-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6ae06-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ae06-121">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="6ae06-121">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="6ae06-122">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="6ae06-122">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ae06-123">-Force</span><span class="sxs-lookup"><span data-stu-id="6ae06-123">-Force</span></span>
<span data-ttu-id="6ae06-124">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="6ae06-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="6ae06-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6ae06-125">-InputObject</span></span>
<span data-ttu-id="6ae06-126">Das zu Aktualisier ExpressRouteConnection-Objekt.</span><span class="sxs-lookup"><span data-stu-id="6ae06-126">The ExpressRouteConnection object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection
Parameter Sets: ByExpressRouteConnectionObject
Aliases: ExpressRouteConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ae06-127">-Name</span><span class="sxs-lookup"><span data-stu-id="6ae06-127">-Name</span></span>
<span data-ttu-id="6ae06-128">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="6ae06-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ae06-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ae06-129">-PassThru</span></span>
<span data-ttu-id="6ae06-130">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="6ae06-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6ae06-131">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="6ae06-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6ae06-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ae06-132">-ResourceGroupName</span></span>
<span data-ttu-id="6ae06-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6ae06-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ae06-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="6ae06-134">-ResourceId</span></span>
<span data-ttu-id="6ae06-135">Die Ressourcen-ID des zu löschenden ExpressRouteConnection-Objekts.</span><span class="sxs-lookup"><span data-stu-id="6ae06-135">The resource id of the ExpressRouteConnection object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionResourceId
Aliases: ExpressRouteConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ae06-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6ae06-136">-Confirm</span></span>
<span data-ttu-id="6ae06-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6ae06-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ae06-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ae06-138">-WhatIf</span></span>
<span data-ttu-id="6ae06-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6ae06-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ae06-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6ae06-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ae06-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ae06-141">CommonParameters</span></span>
<span data-ttu-id="6ae06-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ae06-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ae06-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ae06-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ae06-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6ae06-144">INPUTS</span></span>

### <span data-ttu-id="6ae06-145">System. String</span><span class="sxs-lookup"><span data-stu-id="6ae06-145">System.String</span></span>

### <span data-ttu-id="6ae06-146">Microsoft. Azure. Commands. Network. Models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="6ae06-146">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="6ae06-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6ae06-147">OUTPUTS</span></span>

### <span data-ttu-id="6ae06-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6ae06-148">System.Boolean</span></span>

## <span data-ttu-id="6ae06-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="6ae06-149">NOTES</span></span>

## <span data-ttu-id="6ae06-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6ae06-150">RELATED LINKS</span></span>
