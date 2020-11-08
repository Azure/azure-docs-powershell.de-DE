---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
ms.openlocfilehash: 419c7bc71def03bc2db004e378d80ea9c31f5183
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176146"
---
# <span data-ttu-id="02571-101">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="02571-101">Update-AzVpnGateway</span></span>

## <span data-ttu-id="02571-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="02571-102">SYNOPSIS</span></span>
<span data-ttu-id="02571-103">Aktualisiert ein skalierbares VPN-Gateway.</span><span class="sxs-lookup"><span data-stu-id="02571-103">Updates a scalable VPN gateway.</span></span>

## <span data-ttu-id="02571-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="02571-104">SYNTAX</span></span>

### <span data-ttu-id="02571-105">ByVpnGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="02571-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02571-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="02571-106">ByVpnGatewayObject</span></span>
```
Update-AzVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02571-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="02571-107">ByVpnGatewayResourceId</span></span>
```
Update-AzVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02571-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="02571-108">DESCRIPTION</span></span>
<span data-ttu-id="02571-109">Das Cmdlet **Update-AzVpnGateway** aktualisiert ein skalierbares VPN-Gateway.</span><span class="sxs-lookup"><span data-stu-id="02571-109">The **Update-AzVpnGateway** cmdlet updates a scalable VPN gateway.</span></span>  
<span data-ttu-id="02571-110">Bei einem Azure VPN-Gateway handelt es sich um eine Software definierte Konnektivität für Standort-zu-Standort-Verbindungen innerhalb des VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="02571-110">An Azure VPN gateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="02571-111">Dieses Gateway ändert die Größe und skaliert basierend auf der vom Benutzer angegebenen Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="02571-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="02571-112">Eine Verbindung kann über eine Verzweigung/Website, die als VPN-Website bezeichnet wird, zum skalierbaren Gateway eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="02571-112">A connection can be set up from a branch/site known as VPN site to the scalable gateway.</span></span> <span data-ttu-id="02571-113">Jede Verbindung besteht aus zwei Active-Active Tunneln</span><span class="sxs-lookup"><span data-stu-id="02571-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="02571-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="02571-114">EXAMPLES</span></span>

### <span data-ttu-id="02571-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="02571-115">Example 1</span></span>

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

<span data-ttu-id="02571-116">Das obige wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtuelles Drehkreuz in West US in der Ressourcengruppe "testRG" in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="02571-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="02571-117">Anschließend wird ein VPN-Gateway im virtuellen Hub mit 2 Skalierungseinheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="02571-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="02571-118">Nachdem das Gateway erstellt wurde, wird Update-AzVpnGateway verwendet, um das Gateway auf 3 Skaleneinheiten zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="02571-118">After the gateway has been created, it uses  Update-AzVpnGateway to upgrade the gateway to 3 scale units.</span></span>

### <span data-ttu-id="02571-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="02571-119">Example 2</span></span>

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

<span data-ttu-id="02571-120">Das obige wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtuelles Drehkreuz in West US in der Ressourcengruppe "testRG" in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="02571-120">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="02571-121">Anschließend wird ein VPN-Gateway im virtuellen Hub mit 2 Skalierungseinheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="02571-121">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="02571-122">Nachdem das Gateway erstellt wurde, verwendet es Set-AzVpnGateway, um BgpPeeringAddress zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="02571-122">After the gateway has been created, it uses Set-AzVpnGateway to update BgpPeeringAddress.</span></span>

## <span data-ttu-id="02571-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="02571-123">PARAMETERS</span></span>

### <span data-ttu-id="02571-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02571-124">-AsJob</span></span>
<span data-ttu-id="02571-125">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="02571-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02571-126">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="02571-126">-BgpPeeringAddress</span></span>
<span data-ttu-id="02571-127">Die BGP-Peering Adressen für dieses VpnGateway bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="02571-127">The BGP peering addresses for this VpnGateway bgpsettings.</span></span>

```yaml
Type: PSIpConfigurationBgpPeeringAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02571-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="02571-128">-Confirm</span></span>
<span data-ttu-id="02571-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="02571-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02571-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02571-130">-DefaultProfile</span></span>
<span data-ttu-id="02571-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="02571-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02571-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="02571-132">-InputObject</span></span>
<span data-ttu-id="02571-133">Das zu ändernde VPN-Gateway-Objekt</span><span class="sxs-lookup"><span data-stu-id="02571-133">The vpn gateway object to be modified</span></span>

```yaml
Type: PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02571-134">-Name</span><span class="sxs-lookup"><span data-stu-id="02571-134">-Name</span></span>
<span data-ttu-id="02571-135">Der Name des VPN-Gateways.</span><span class="sxs-lookup"><span data-stu-id="02571-135">The vpn gateway name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02571-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02571-136">-ResourceGroupName</span></span>
<span data-ttu-id="02571-137">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="02571-137">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02571-138">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="02571-138">-ResourceId</span></span>
<span data-ttu-id="02571-139">Die Azure-Ressourcen-ID des zu ändernden VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="02571-139">The Azure resource ID of the VpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02571-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="02571-140">-Tag</span></span>
<span data-ttu-id="02571-141">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="02571-141">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02571-142">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="02571-142">-VpnConnection</span></span>
<span data-ttu-id="02571-143">Die Liste der VpnConnections, die dieser VpnGateway haben muss.</span><span class="sxs-lookup"><span data-stu-id="02571-143">The list of VpnConnections that this VpnGateway needs to have.</span></span>

```yaml
Type: PSVpnConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02571-144">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="02571-144">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="02571-145">Die Skalierungseinheit für diesen VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="02571-145">The scale unit for this VpnGateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02571-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02571-146">-WhatIf</span></span>
<span data-ttu-id="02571-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="02571-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02571-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="02571-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02571-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02571-149">CommonParameters</span></span>
<span data-ttu-id="02571-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02571-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02571-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02571-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02571-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="02571-152">INPUTS</span></span>

### <span data-ttu-id="02571-153">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="02571-153">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="02571-154">System. String</span><span class="sxs-lookup"><span data-stu-id="02571-154">System.String</span></span>

## <span data-ttu-id="02571-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="02571-155">OUTPUTS</span></span>

### <span data-ttu-id="02571-156">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="02571-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="02571-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="02571-157">NOTES</span></span>

## <span data-ttu-id="02571-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="02571-158">RELATED LINKS</span></span>
[<span data-ttu-id="02571-159">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="02571-159">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="02571-160">Neu – AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="02571-160">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="02571-161">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="02571-161">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)