---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
ms.openlocfilehash: d04c665bce4c37425564e4eb65ff46da3b39fa8a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918344"
---
# <span data-ttu-id="b3767-101">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="b3767-101">Update-AzVpnGateway</span></span>

## <span data-ttu-id="b3767-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3767-102">SYNOPSIS</span></span>
<span data-ttu-id="b3767-103">Aktualisiert ein skalierbares VPN-Gateway.</span><span class="sxs-lookup"><span data-stu-id="b3767-103">Updates a scalable VPN gateway.</span></span>

## <span data-ttu-id="b3767-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b3767-104">SYNTAX</span></span>

### <span data-ttu-id="b3767-105">ByVpnGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b3767-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3767-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="b3767-106">ByVpnGatewayObject</span></span>
```
Update-AzVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3767-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="b3767-107">ByVpnGatewayResourceId</span></span>
```
Update-AzVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3767-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b3767-108">DESCRIPTION</span></span>
<span data-ttu-id="b3767-109">Das **Update-AzVpnGateway-Cmdlet** aktualisiert ein skalierbares VPN-Gateway.</span><span class="sxs-lookup"><span data-stu-id="b3767-109">The **Update-AzVpnGateway** cmdlet updates a scalable VPN gateway.</span></span>  
<span data-ttu-id="b3767-110">Ein Azure VPN-Gateway ist eine softwaredefinierte Konnektivität für Website-zu-Website-Verbindungen innerhalb des VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="b3767-110">An Azure VPN gateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="b3767-111">Die Größe und Skalierung dieses Gateways wird basierend auf der vom Benutzer angegebenen Skalierungseinheit angepasst.</span><span class="sxs-lookup"><span data-stu-id="b3767-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="b3767-112">Eine Verbindung kann von einer als VPN-Website bezeichneten Verzweigung/Website zum skalierbaren Gateway eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="b3767-112">A connection can be set up from a branch/site known as VPN site to the scalable gateway.</span></span> <span data-ttu-id="b3767-113">Jede Verbindung besteht aus 2 Active-Active Tunneln</span><span class="sxs-lookup"><span data-stu-id="b3767-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="b3767-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b3767-114">EXAMPLES</span></span>

### <span data-ttu-id="b3767-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b3767-115">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Update-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VpnGatewayScaleUnit 3

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 3
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="b3767-116">Mit dem vorstehenden Beispiel wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtueller Hub in West USA in der Ressourcengruppe "testRG" in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="b3767-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="b3767-117">Anschließend wird im virtuellen Hub ein VPN-Gateway mit zwei Skalierungseinheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="b3767-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="b3767-118">Nachdem das Gateway erstellt wurde, verwendet es Update-AzVpnGateway, um das Gateway auf 3 Skalierungseinheiten zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b3767-118">After the gateway has been created, it uses  Update-AzVpnGateway to upgrade the gateway to 3 scale units.</span></span>

### <span data-ttu-id="b3767-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b3767-119">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\>$ipconfigurationId1 = 'Instance0'
PS C:\>$addresslist1 = @('169.254.21.5')
PS C:\>$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
PS C:\>$ipconfigurationId2 = 'Instance1'
PS C:\>$addresslist2 = @('169.254.21.10')
PS C:\>$gw1ipconfBgp2 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId2 -CustomAddress $addresslist2
PS C:\>$gw = Get-AzVpnGateway -ResourceGroupName testRg -Name testgw
PS C:\> Update-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -BgpPeeringAddress @($gw1ipconfBgp1,$gw1ipconfBgp2)

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 3
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="b3767-120">Mit dem vorstehenden Beispiel wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtueller Hub in West USA in der Ressourcengruppe "testRG" in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="b3767-120">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="b3767-121">Anschließend wird im virtuellen Hub ein VPN-Gateway mit zwei Skalierungseinheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="b3767-121">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="b3767-122">Nachdem das Gateway erstellt wurde, verwendet es Set-AzVpnGateway zum Aktualisieren von BgpPeeringAddress.</span><span class="sxs-lookup"><span data-stu-id="b3767-122">After the gateway has been created, it uses Set-AzVpnGateway to update BgpPeeringAddress.</span></span>

## <span data-ttu-id="b3767-123">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b3767-123">PARAMETERS</span></span>

### <span data-ttu-id="b3767-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3767-124">-AsJob</span></span>
<span data-ttu-id="b3767-125">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b3767-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b3767-126">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="b3767-126">-BgpPeeringAddress</span></span>
<span data-ttu-id="b3767-127">Die BGP-Peeringadressen für dieses VpnGateway-bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="b3767-127">The BGP peering addresses for this VpnGateway bgpsettings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3767-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3767-128">-DefaultProfile</span></span>
<span data-ttu-id="b3767-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b3767-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3767-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3767-130">-InputObject</span></span>
<span data-ttu-id="b3767-131">Das zu ändernde Vpngatewayobjekt</span><span class="sxs-lookup"><span data-stu-id="b3767-131">The vpn gateway object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3767-132">-Name</span><span class="sxs-lookup"><span data-stu-id="b3767-132">-Name</span></span>
<span data-ttu-id="b3767-133">Der Name des VPN-Gateways.</span><span class="sxs-lookup"><span data-stu-id="b3767-133">The vpn gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3767-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3767-134">-ResourceGroupName</span></span>
<span data-ttu-id="b3767-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b3767-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3767-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3767-136">-ResourceId</span></span>
<span data-ttu-id="b3767-137">Die Azure-Ressourcen-ID des vpnGateways, das geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b3767-137">The Azure resource ID of the VpnGateway to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3767-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="b3767-138">-Tag</span></span>
<span data-ttu-id="b3767-139">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="b3767-139">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b3767-140">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="b3767-140">-VpnConnection</span></span>
<span data-ttu-id="b3767-141">Die Liste der VpnConnections, die dieses VpnGateway haben muss.</span><span class="sxs-lookup"><span data-stu-id="b3767-141">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="b3767-142">-VpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="b3767-142">-VpnGatewayNatRule</span></span>
<span data-ttu-id="b3767-143">Die Liste der VpnGatewayNatRules, die diesem VpnGateway zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b3767-143">The list of VpnGatewayNatRules that are associated with this VpnGateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3767-144">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="b3767-144">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="b3767-145">Die Skalierungseinheit für dieses VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="b3767-145">The scale unit for this VpnGateway.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3767-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b3767-146">-Confirm</span></span>
<span data-ttu-id="b3767-147">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b3767-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3767-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3767-148">-WhatIf</span></span>
<span data-ttu-id="b3767-149">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b3767-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3767-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b3767-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3767-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3767-151">CommonParameters</span></span>
<span data-ttu-id="b3767-152">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3767-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3767-153">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3767-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3767-154">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b3767-154">INPUTS</span></span>

### <span data-ttu-id="b3767-155">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="b3767-155">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="b3767-156">System.String</span><span class="sxs-lookup"><span data-stu-id="b3767-156">System.String</span></span>

## <span data-ttu-id="b3767-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b3767-157">OUTPUTS</span></span>

### <span data-ttu-id="b3767-158">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="b3767-158">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="b3767-159">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b3767-159">NOTES</span></span>

## <span data-ttu-id="b3767-160">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b3767-160">RELATED LINKS</span></span>

[<span data-ttu-id="b3767-161">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="b3767-161">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="b3767-162">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="b3767-162">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="b3767-163">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="b3767-163">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)