---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
ms.openlocfilehash: 5161dfcb843310ad372739438e63adb6c81f1935
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660128"
---
# <span data-ttu-id="fca73-101">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="fca73-101">Update-AzVpnConnection</span></span>

## <span data-ttu-id="fca73-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fca73-102">SYNOPSIS</span></span>
<span data-ttu-id="fca73-103">Aktualisiert eine VPN-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="fca73-103">Updates a VPN connection.</span></span>

## <span data-ttu-id="fca73-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fca73-104">SYNTAX</span></span>

### <span data-ttu-id="fca73-105">ByVpnConnectionName (Standard)</span><span class="sxs-lookup"><span data-stu-id="fca73-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fca73-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="fca73-106">ByVpnConnectionResourceId</span></span>
```
Update-AzVpnConnection -ResourceId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fca73-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="fca73-107">ByVpnConnectionObject</span></span>
```
Update-AzVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fca73-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fca73-108">DESCRIPTION</span></span>
<span data-ttu-id="fca73-109">Das Cmdlet **Update-AzVpnConnection** aktualisiert eine VPN-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="fca73-109">The **Update-AzVpnConnection** cmdlet updates a VPN connection.</span></span>  
<span data-ttu-id="fca73-110">Die VPN-Verbindung erstellt eine IPSec-Verbindung, die ein VPN-Gateway mit einem Remote-Kunden Zweig verbindet, der in Azure als VPN-Website dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="fca73-110">VPN connection creates an IPsec connection that connects a VPN gateway to a remote customer branch represented in Azure as a VPN site.</span></span>

## <span data-ttu-id="fca73-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fca73-111">EXAMPLES</span></span>

### <span data-ttu-id="fca73-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fca73-112">Example 1</span></span>

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
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="fca73-113">Das obige wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtuellen Hub und einen VpnSite in West US in "testRG"-Ressourcengruppe in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="fca73-113">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="fca73-114">Anschließend wird ein VPN-Gateway im virtuellen Hub mit 2 Skalierungseinheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="fca73-114">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="fca73-115">Nachdem das Gateway erstellt wurde, wird es mit dem VpnSite mit dem Befehl New-AzVpnConnection verbunden.</span><span class="sxs-lookup"><span data-stu-id="fca73-115">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="fca73-116">Die Verbindung wird dann mit dem Befehl Set-AzVpnConnection auf einen neuen IpSecPolicy aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="fca73-116">The connection is then updated to have a new IpSecPolicy by using the Set-AzVpnConnection command.</span></span>

### <span data-ttu-id="fca73-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fca73-117">Example 2</span></span>

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
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="fca73-118">Das obige wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtuellen Hub und einen VpnSite in West US in "testRG"-Ressourcengruppe in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="fca73-118">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="fca73-119">Anschließend wird ein VPN-Gateway im virtuellen Hub mit 2 Skalierungseinheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="fca73-119">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="fca73-120">Nachdem das Gateway erstellt wurde, wird es mit dem VpnSite mit dem Befehl New-AzVpnConnection verbunden.</span><span class="sxs-lookup"><span data-stu-id="fca73-120">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="fca73-121">Die Verbindung wird dann aktualisiert, um einen neuen freigegebenen Schlüssel mithilfe des Secure String-Konstrukts zu haben.</span><span class="sxs-lookup"><span data-stu-id="fca73-121">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="fca73-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="fca73-122">PARAMETERS</span></span>

### <span data-ttu-id="fca73-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fca73-123">-AsJob</span></span>
<span data-ttu-id="fca73-124">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="fca73-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fca73-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="fca73-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="fca73-126">Die Bandbreite, die von dieser Verbindung in Mbit/s verarbeitet werden muss.</span><span class="sxs-lookup"><span data-stu-id="fca73-126">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="fca73-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fca73-127">-DefaultProfile</span></span>
<span data-ttu-id="fca73-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fca73-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fca73-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="fca73-129">-EnableBgp</span></span>
<span data-ttu-id="fca73-130">Aktivieren von BGP für diese Verbindung</span><span class="sxs-lookup"><span data-stu-id="fca73-130">Enable BGP for this connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fca73-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fca73-131">-InputObject</span></span>
<span data-ttu-id="fca73-132">Das zu Aktualisier VpnConenction-Objekt.</span><span class="sxs-lookup"><span data-stu-id="fca73-132">The VpnConenction object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fca73-133">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="fca73-133">-IpSecPolicy</span></span>
<span data-ttu-id="fca73-134">Die Bandbreite, die von dieser Verbindung in Mbit/s verarbeitet werden muss.</span><span class="sxs-lookup"><span data-stu-id="fca73-134">The bandwith that needs to be handled by this connection in mbps.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fca73-135">-Name</span><span class="sxs-lookup"><span data-stu-id="fca73-135">-Name</span></span>
<span data-ttu-id="fca73-136">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="fca73-136">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fca73-137">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="fca73-137">-ParentResourceName</span></span>
<span data-ttu-id="fca73-138">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="fca73-138">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fca73-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fca73-139">-ResourceGroupName</span></span>
<span data-ttu-id="fca73-140">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fca73-140">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fca73-141">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="fca73-141">-ResourceId</span></span>
<span data-ttu-id="fca73-142">Die Ressourcen-ID des zu löschenden VpnConenction-Objekts.</span><span class="sxs-lookup"><span data-stu-id="fca73-142">The resource id of the VpnConenction object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fca73-143">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="fca73-143">-SharedKey</span></span>
<span data-ttu-id="fca73-144">Der freigegebene Schlüssel, der zum Einrichten dieser Verbindung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="fca73-144">The shared key required to set this connection up.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fca73-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fca73-145">-Confirm</span></span>
<span data-ttu-id="fca73-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fca73-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fca73-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fca73-147">-WhatIf</span></span>
<span data-ttu-id="fca73-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fca73-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fca73-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fca73-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fca73-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fca73-150">CommonParameters</span></span>
<span data-ttu-id="fca73-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fca73-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fca73-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fca73-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fca73-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fca73-153">INPUTS</span></span>

### <span data-ttu-id="fca73-154">System. String</span><span class="sxs-lookup"><span data-stu-id="fca73-154">System.String</span></span>

### <span data-ttu-id="fca73-155">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="fca73-155">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="fca73-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fca73-156">OUTPUTS</span></span>

### <span data-ttu-id="fca73-157">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="fca73-157">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="fca73-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="fca73-158">NOTES</span></span>

## <span data-ttu-id="fca73-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fca73-159">RELATED LINKS</span></span>

[<span data-ttu-id="fca73-160">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="fca73-160">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="fca73-161">Neu – AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="fca73-161">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="fca73-162">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="fca73-162">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)
