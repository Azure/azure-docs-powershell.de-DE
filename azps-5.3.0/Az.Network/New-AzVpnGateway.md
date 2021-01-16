---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
ms.openlocfilehash: fa7374264e46e65dcddacb9f35e5822f18294147
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385369"
---
# <span data-ttu-id="305bb-101">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="305bb-101">New-AzVpnGateway</span></span>

## <span data-ttu-id="305bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="305bb-102">SYNOPSIS</span></span>
<span data-ttu-id="305bb-103">Erstellt ein skalierbares VPN-Gateway.</span><span class="sxs-lookup"><span data-stu-id="305bb-103">Creates a Scalable VPN Gateway.</span></span>

## <span data-ttu-id="305bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="305bb-104">SYNTAX</span></span>

### <span data-ttu-id="305bb-105">ByVirtualHubName (Standard)</span><span class="sxs-lookup"><span data-stu-id="305bb-105">ByVirtualHubName (Default)</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="305bb-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="305bb-106">ByVirtualHubObject</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="305bb-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="305bb-107">ByVirtualHubResourceId</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="305bb-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="305bb-108">DESCRIPTION</span></span>

<span data-ttu-id="305bb-109">New-AzVpnGateway erstellt ein skalierbares VPN-Gateway.</span><span class="sxs-lookup"><span data-stu-id="305bb-109">New-AzVpnGateway creates a scalable VPN Gateway.</span></span> <span data-ttu-id="305bb-110">Dabei handelt es sich um softwaredefinierte Konnektivität für Website-zu-Website-Verbindungen innerhalb von VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="305bb-110">This is software defined connectivity for site to site connections inside the VirtualHub.</span></span> 

<span data-ttu-id="305bb-111">Die Größe dieses Gateways wird basierend auf der in diesem cmdlet oder Set-AzVpnGateway Festgelegten Skalierungseinheit geändert und skaliert.</span><span class="sxs-lookup"><span data-stu-id="305bb-111">This gateway resizes and scales based on the scale unit specified in this or the Set-AzVpnGateway cmdlet.</span></span> 

<span data-ttu-id="305bb-112">Eine Verbindung wird von einer Verzweigung/Website, die als VPNSite bezeichnet wird, zum skalierbaren Gateway eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="305bb-112">A connection is set up from a branch/Site known as VPNSite to the scalable gateway.</span></span> <span data-ttu-id="305bb-113">Jede Verbindung besteht aus 2 Active-Active Tunneln.</span><span class="sxs-lookup"><span data-stu-id="305bb-113">Each connection comprises of 2 Active-Active tunnels.</span></span>

<span data-ttu-id="305bb-114">Das VpnGateway befindet sich an demselben Speicherort wie der VirtualHub, auf den verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="305bb-114">The VpnGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="305bb-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="305bb-115">EXAMPLES</span></span>

### <span data-ttu-id="305bb-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="305bb-116">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="305bb-117">Im vorstehenden Beispiel wird eine Ressourcengruppe, ein virtuelles WAN, ein virtuelles Netzwerk und ein virtueller Hub in der West-US-Region in der Ressourcengruppe "testRG" in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="305bb-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="305bb-118">Anschließend wird im virtuellen Hub ein VPN-Gateway mit 2 Skalierungseinheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="305bb-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="305bb-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="305bb-119">PARAMETERS</span></span>

### <span data-ttu-id="305bb-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="305bb-120">-AsJob</span></span>
<span data-ttu-id="305bb-121">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="305bb-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="305bb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="305bb-122">-DefaultProfile</span></span>
<span data-ttu-id="305bb-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="305bb-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="305bb-124">-Name</span><span class="sxs-lookup"><span data-stu-id="305bb-124">-Name</span></span>
<span data-ttu-id="305bb-125">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="305bb-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="305bb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="305bb-126">-ResourceGroupName</span></span>
<span data-ttu-id="305bb-127">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="305bb-127">The resource name.</span></span>

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

### <span data-ttu-id="305bb-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="305bb-128">-Tag</span></span>
<span data-ttu-id="305bb-129">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="305bb-129">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="305bb-130">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="305bb-130">-VirtualHub</span></span>
<span data-ttu-id="305bb-131">Der VirtualHub, dem dieses VpnGateway zugeordnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="305bb-131">The VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="305bb-132">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="305bb-132">-VirtualHubId</span></span>
<span data-ttu-id="305bb-133">Die ID des VirtualHub, dem dieses VpnGateway zugeordnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="305bb-133">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="305bb-134">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="305bb-134">-VirtualHubName</span></span>
<span data-ttu-id="305bb-135">Die ID des VirtualHub, dem dieses VpnGateway zugeordnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="305bb-135">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="305bb-136">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="305bb-136">-VpnConnection</span></span>
<span data-ttu-id="305bb-137">Die Liste der VpnConnections, die dieses VpnGateway haben muss.</span><span class="sxs-lookup"><span data-stu-id="305bb-137">The list of VpnConnections that this VpnGateway needs to have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="305bb-138">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="305bb-138">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="305bb-139">Die Skalierungseinheit für dieses VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="305bb-139">The scale unit for this VpnGateway.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="305bb-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="305bb-140">-Confirm</span></span>
<span data-ttu-id="305bb-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="305bb-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="305bb-142">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="305bb-142">-WhatIf</span></span>
<span data-ttu-id="305bb-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="305bb-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="305bb-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="305bb-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="305bb-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="305bb-145">CommonParameters</span></span>
<span data-ttu-id="305bb-146">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="305bb-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="305bb-147">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="305bb-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="305bb-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="305bb-148">INPUTS</span></span>

### <span data-ttu-id="305bb-149">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="305bb-149">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="305bb-150">System.String</span><span class="sxs-lookup"><span data-stu-id="305bb-150">System.String</span></span>

## <span data-ttu-id="305bb-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="305bb-151">OUTPUTS</span></span>

### <span data-ttu-id="305bb-152">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="305bb-152">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="305bb-153">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="305bb-153">NOTES</span></span>

## <span data-ttu-id="305bb-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="305bb-154">RELATED LINKS</span></span>

[<span data-ttu-id="305bb-155">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="305bb-155">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="305bb-156">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="305bb-156">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="305bb-157">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="305bb-157">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
