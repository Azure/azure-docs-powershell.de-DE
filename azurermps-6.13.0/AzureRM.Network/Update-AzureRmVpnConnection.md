---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/update-azurermvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnConnection.md
ms.openlocfilehash: 08b1e18fcd15dfb2667d0aec2410e7e0d7ea7b99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495849"
---
# <span data-ttu-id="ce097-101">Update-AzureRmVpnConnection</span><span class="sxs-lookup"><span data-stu-id="ce097-101">Update-AzureRmVpnConnection</span></span>

## <span data-ttu-id="ce097-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ce097-102">SYNOPSIS</span></span>
<span data-ttu-id="ce097-103">Aktualisiert ein VpnConnection-Objekt in einem Zielzustand.</span><span class="sxs-lookup"><span data-stu-id="ce097-103">Updates a VpnConnection object to a goal state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce097-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce097-104">SYNTAX</span></span>

### <span data-ttu-id="ce097-105">ByVpnConnectionName (Standard)</span><span class="sxs-lookup"><span data-stu-id="ce097-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzureRmVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ce097-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="ce097-106">ByVpnConnectionResourceId</span></span>
```
Update-AzureRmVpnConnection -ResourceId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce097-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="ce097-107">ByVpnConnectionObject</span></span>
```
Update-AzureRmVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce097-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce097-108">DESCRIPTION</span></span>
<span data-ttu-id="ce097-109">Erstellt eine IPSec-Verbindung, die einen VpnGateway mit einer Remote-Kunden Verzweigung verbindet, die in RM als VpnSite dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="ce097-109">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="ce097-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ce097-110">EXAMPLES</span></span>

### <span data-ttu-id="ce097-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ce097-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> $vpnConnection = New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $ipsecPolicy = New-AzureRmIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> Update-AzureRmVpnConnection -InputObject $vpnConnection -IpSecPolicy $ipsecPolicy

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

<span data-ttu-id="ce097-112">Das obige wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtuellen Hub und einen VpnSite in West US in "testRG"-Ressourcengruppe in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="ce097-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="ce097-113">Anschließend wird ein VPN-Gateway im virtuellen Hub mit 2 Skalierungseinheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="ce097-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="ce097-114">Nachdem das Gateway erstellt wurde, wird es mit dem VpnSite mit dem Befehl New-AzureRmVpnConnection verbunden.</span><span class="sxs-lookup"><span data-stu-id="ce097-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="ce097-115">Die Verbindung wird dann mit dem Befehl Set-AzureRmVpnConnection auf einen neuen IpSecPolicy aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ce097-115">The connection is then updated to have a new IpSecPolicy by using the Set-AzureRmVpnConnection command.</span></span>

### <span data-ttu-id="ce097-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ce097-116">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> $vpnConnection = New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $Secure_String_Pwd = Read-Host -AsSecureString
PS C:\> Update-AzureRmVpnConnection -InputObject $vpnConnection -SharedKey $Secure_String_Pwd

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

<span data-ttu-id="ce097-117">Das obige wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtuellen Hub und einen VpnSite in West US in "testRG"-Ressourcengruppe in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="ce097-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="ce097-118">Anschließend wird ein VPN-Gateway im virtuellen Hub mit 2 Skalierungseinheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="ce097-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="ce097-119">Nachdem das Gateway erstellt wurde, wird es mit dem VpnSite mit dem Befehl New-AzureRmVpnConnection verbunden.</span><span class="sxs-lookup"><span data-stu-id="ce097-119">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="ce097-120">Die Verbindung wird dann aktualisiert, um einen neuen freigegebenen Schlüssel mithilfe des Secure String-Konstrukts zu haben.</span><span class="sxs-lookup"><span data-stu-id="ce097-120">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="ce097-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce097-121">PARAMETERS</span></span>

### <span data-ttu-id="ce097-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce097-122">-AsJob</span></span>
<span data-ttu-id="ce097-123">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ce097-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ce097-124">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="ce097-124">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="ce097-125">Die Bandbreite, die von dieser Verbindung in Mbit/s verarbeitet werden muss.</span><span class="sxs-lookup"><span data-stu-id="ce097-125">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="ce097-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce097-126">-DefaultProfile</span></span>
<span data-ttu-id="ce097-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ce097-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce097-128">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="ce097-128">-EnableBgp</span></span>
<span data-ttu-id="ce097-129">Aktivieren von BGP für diese Verbindung</span><span class="sxs-lookup"><span data-stu-id="ce097-129">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="ce097-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ce097-130">-InputObject</span></span>
<span data-ttu-id="ce097-131">Das zu Aktualisier VpnConenction-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ce097-131">The VpnConenction object to update.</span></span>

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

### <span data-ttu-id="ce097-132">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="ce097-132">-IpSecPolicy</span></span>
<span data-ttu-id="ce097-133">Die Bandbreite, die von dieser Verbindung in Mbit/s verarbeitet werden muss.</span><span class="sxs-lookup"><span data-stu-id="ce097-133">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="ce097-134">-Name</span><span class="sxs-lookup"><span data-stu-id="ce097-134">-Name</span></span>
<span data-ttu-id="ce097-135">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="ce097-135">The resource name.</span></span>

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

### <span data-ttu-id="ce097-136">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="ce097-136">-ParentResourceName</span></span>
<span data-ttu-id="ce097-137">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="ce097-137">The parent resource name.</span></span>

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

### <span data-ttu-id="ce097-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce097-138">-ResourceGroupName</span></span>
<span data-ttu-id="ce097-139">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ce097-139">The resource group name.</span></span>

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

### <span data-ttu-id="ce097-140">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ce097-140">-ResourceId</span></span>
<span data-ttu-id="ce097-141">Die Ressourcen-ID des zu löschenden VpnConenction-Objekts.</span><span class="sxs-lookup"><span data-stu-id="ce097-141">The resource id of the VpnConenction object to delete.</span></span>

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

### <span data-ttu-id="ce097-142">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="ce097-142">-SharedKey</span></span>
<span data-ttu-id="ce097-143">Der freigegebene Schlüssel, der zum Einrichten dieser Verbindung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="ce097-143">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="ce097-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ce097-144">-Confirm</span></span>
<span data-ttu-id="ce097-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ce097-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce097-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce097-146">-WhatIf</span></span>
<span data-ttu-id="ce097-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ce097-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce097-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ce097-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce097-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce097-149">CommonParameters</span></span>
<span data-ttu-id="ce097-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce097-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce097-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce097-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce097-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ce097-152">INPUTS</span></span>

### <span data-ttu-id="ce097-153">System. String</span><span class="sxs-lookup"><span data-stu-id="ce097-153">System.String</span></span>

### <span data-ttu-id="ce097-154">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="ce097-154">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="ce097-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ce097-155">OUTPUTS</span></span>

### <span data-ttu-id="ce097-156">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="ce097-156">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="ce097-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="ce097-157">NOTES</span></span>

## <span data-ttu-id="ce097-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ce097-158">RELATED LINKS</span></span>
