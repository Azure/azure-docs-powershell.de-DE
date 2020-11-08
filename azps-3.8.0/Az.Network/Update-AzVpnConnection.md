---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
ms.openlocfilehash: a35f9b776bcd0f7fcb206103cd20475fb18bd608
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004717"
---
# <span data-ttu-id="58620-101">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="58620-101">Update-AzVpnConnection</span></span>

## <span data-ttu-id="58620-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="58620-102">SYNOPSIS</span></span>
<span data-ttu-id="58620-103">Aktualisiert eine VPN-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="58620-103">Updates a VPN connection.</span></span>

## <span data-ttu-id="58620-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="58620-104">SYNTAX</span></span>

### <span data-ttu-id="58620-105">ByVpnConnectionName (Standard)</span><span class="sxs-lookup"><span data-stu-id="58620-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58620-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="58620-106">ByVpnConnectionResourceId</span></span>
```
Update-AzVpnConnection -ResourceId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>]
 [-EnableInternetSecurity <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="58620-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="58620-107">ByVpnConnectionObject</span></span>
```
Update-AzVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>]
 [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58620-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="58620-108">DESCRIPTION</span></span>
<span data-ttu-id="58620-109">Das Cmdlet **Update-AzVpnConnection** aktualisiert eine VPN-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="58620-109">The **Update-AzVpnConnection** cmdlet updates a VPN connection.</span></span>  
<span data-ttu-id="58620-110">Die VPN-Verbindung erstellt eine IPSec-Verbindung, die ein VPN-Gateway mit einem Remote-Kunden Zweig verbindet, der in Azure als VPN-Website dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="58620-110">VPN connection creates an IPsec connection that connects a VPN gateway to a remote customer branch represented in Azure as a VPN site.</span></span>

## <span data-ttu-id="58620-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="58620-111">EXAMPLES</span></span>

### <span data-ttu-id="58620-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="58620-112">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> $vpnConnection = New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $ipsecPolicy = New-AzIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> Update-AzVpnConnection -InputObject $vpnConnection -IpSecPolicy $ipsecPolicy

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy}
ConnectionBandwidth       : 20
EnableBgp                 : False
UseLocalAzureIpAddress    : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="58620-113">Das obige wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtuellen Hub und einen VpnSite in West US in "testRG"-Ressourcengruppe in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="58620-113">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="58620-114">Anschließend wird ein VPN-Gateway im virtuellen Hub mit 2 Skalierungseinheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="58620-114">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="58620-115">Nachdem das Gateway erstellt wurde, wird es mit dem VpnSite mit dem Befehl New-AzVpnConnection verbunden.</span><span class="sxs-lookup"><span data-stu-id="58620-115">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="58620-116">Die Verbindung wird dann mit dem Befehl Set-AzVpnConnection auf einen neuen IpSecPolicy aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="58620-116">The connection is then updated to have a new IpSecPolicy by using the Set-AzVpnConnection command.</span></span>

### <span data-ttu-id="58620-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="58620-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> $vpnConnection = New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $Secure_String_Pwd = Read-Host -AsSecureString
PS C:\> Update-AzVpnConnection -InputObject $vpnConnection -SharedKey $Secure_String_Pwd

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy}
ConnectionBandwidth       : 20
EnableBgp                 : False
UseLocalAzureIpAddress    : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="58620-118">Das obige wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtuellen Hub und einen VpnSite in West US in "testRG"-Ressourcengruppe in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="58620-118">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="58620-119">Anschließend wird ein VPN-Gateway im virtuellen Hub mit 2 Skalierungseinheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="58620-119">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="58620-120">Nachdem das Gateway erstellt wurde, wird es mit dem VpnSite mit dem Befehl New-AzVpnConnection verbunden.</span><span class="sxs-lookup"><span data-stu-id="58620-120">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="58620-121">Die Verbindung wird dann aktualisiert, um einen neuen freigegebenen Schlüssel mithilfe des Secure String-Konstrukts zu haben.</span><span class="sxs-lookup"><span data-stu-id="58620-121">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="58620-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="58620-122">PARAMETERS</span></span>

### <span data-ttu-id="58620-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58620-123">-AsJob</span></span>
<span data-ttu-id="58620-124">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="58620-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="58620-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="58620-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="58620-126">Die Bandbreite, die von dieser Verbindung in Mbit/s verarbeitet werden muss.</span><span class="sxs-lookup"><span data-stu-id="58620-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="58620-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58620-127">-DefaultProfile</span></span>
<span data-ttu-id="58620-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="58620-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58620-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="58620-129">-EnableBgp</span></span>
<span data-ttu-id="58620-130">Aktivieren von BGP für diese Verbindung</span><span class="sxs-lookup"><span data-stu-id="58620-130">Enable BGP for this connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58620-131">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="58620-131">-EnableInternetSecurity</span></span>
<span data-ttu-id="58620-132">Aktivieren der Internetsicherheit für diese Verbindung</span><span class="sxs-lookup"><span data-stu-id="58620-132">Enable internet security for this connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58620-133">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="58620-133">-InputObject</span></span>
<span data-ttu-id="58620-134">Das zu Aktualisier VpnConnection-Objekt.</span><span class="sxs-lookup"><span data-stu-id="58620-134">The VpnConnection object to update.</span></span>

```yaml
Type: PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58620-135">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="58620-135">-IpSecPolicy</span></span>
<span data-ttu-id="58620-136">Die Bandbreite, die von dieser Verbindung in Mbit/s verarbeitet werden muss.</span><span class="sxs-lookup"><span data-stu-id="58620-136">The bandwidth that needs to be handled by this connection in mbps.</span></span>

```yaml
Type: PSIpsecPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58620-137">-Name</span><span class="sxs-lookup"><span data-stu-id="58620-137">-Name</span></span>
<span data-ttu-id="58620-138">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="58620-138">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58620-139">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="58620-139">-ParentResourceName</span></span>
<span data-ttu-id="58620-140">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="58620-140">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58620-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58620-141">-ResourceGroupName</span></span>
<span data-ttu-id="58620-142">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="58620-142">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58620-143">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="58620-143">-ResourceId</span></span>
<span data-ttu-id="58620-144">Die Ressourcen-ID des zu löschenden VpnConnection-Objekts.</span><span class="sxs-lookup"><span data-stu-id="58620-144">The resource id of the VpnConnection object to delete.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionResourceId
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58620-145">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="58620-145">-SharedKey</span></span>
<span data-ttu-id="58620-146">Der freigegebene Schlüssel, der zum Einrichten dieser Verbindung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="58620-146">The shared key required to set this connection up.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58620-147">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="58620-147">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="58620-148">Verwenden Sie die lokale Azure-IP-Adresse als Quelladresse, während Sie die Verbindung initiieren.</span><span class="sxs-lookup"><span data-stu-id="58620-148">Use local azure ip address as source address while initiating connection.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58620-149">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="58620-149">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="58620-150">Verwenden Sie für diese Verbindung richtlinienbasierte Datenverkehrs Auswahl.</span><span class="sxs-lookup"><span data-stu-id="58620-150">Use policy based traffic selectors for this connection.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58620-151">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="58620-151">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="58620-152">Die Liste der VpnSiteLinkConnections, die dieser VpnConnection haben muss.</span><span class="sxs-lookup"><span data-stu-id="58620-152">The list of VpnSiteLinkConnections that this VpnConnection needs to have.</span></span>

```yaml
Type: PSVpnSiteLinkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58620-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="58620-153">-Confirm</span></span>
<span data-ttu-id="58620-154">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="58620-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58620-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58620-155">-WhatIf</span></span>
<span data-ttu-id="58620-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="58620-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58620-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="58620-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58620-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58620-158">CommonParameters</span></span>
<span data-ttu-id="58620-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58620-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58620-160">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58620-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58620-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="58620-161">INPUTS</span></span>

### <span data-ttu-id="58620-162">System. String</span><span class="sxs-lookup"><span data-stu-id="58620-162">System.String</span></span>

### <span data-ttu-id="58620-163">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="58620-163">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="58620-164">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="58620-164">OUTPUTS</span></span>

### <span data-ttu-id="58620-165">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="58620-165">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="58620-166">Notizen</span><span class="sxs-lookup"><span data-stu-id="58620-166">NOTES</span></span>

## <span data-ttu-id="58620-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="58620-167">RELATED LINKS</span></span>

[<span data-ttu-id="58620-168">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="58620-168">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="58620-169">Neu – AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="58620-169">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="58620-170">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="58620-170">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)
