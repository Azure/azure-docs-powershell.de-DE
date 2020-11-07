---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnConnection.md
ms.openlocfilehash: 85b6472cd6dd99210e188f6fc9b66ba4b00e3198
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821680"
---
# <span data-ttu-id="64959-101">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="64959-101">Get-AzVpnConnection</span></span>

## <span data-ttu-id="64959-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="64959-102">SYNOPSIS</span></span>
<span data-ttu-id="64959-103">Ruft eine VPN-Verbindung nach Namen ab oder listet alle VPN-Verbindungen auf, die mit einem VpnGateway verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="64959-103">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

## <span data-ttu-id="64959-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="64959-104">SYNTAX</span></span>

### <span data-ttu-id="64959-105">ByVpnGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="64959-105">ByVpnGatewayName (Default)</span></span>
```
Get-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64959-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="64959-106">ByVpnGatewayObject</span></span>
```
Get-AzVpnConnection -ParentObject <PSVpnGateway> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="64959-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="64959-107">ByVpnGatewayResourceId</span></span>
```
Get-AzVpnConnection -ParentResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="64959-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="64959-108">DESCRIPTION</span></span>
<span data-ttu-id="64959-109">Ruft eine VPN-Verbindung nach Namen ab oder listet alle VPN-Verbindungen auf, die mit einem VpnGateway verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="64959-109">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

## <span data-ttu-id="64959-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="64959-110">EXAMPLES</span></span>

### <span data-ttu-id="64959-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="64959-111">Example 1</span></span>

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

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Get-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="64959-112">Das obige wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtuellen Hub und einen VpnSite in West US in "testRG"-Ressourcengruppe in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="64959-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="64959-113">Anschließend wird ein VPN-Gateway im virtuellen Hub mit 2 Skalierungseinheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="64959-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="64959-114">Nachdem das Gateway erstellt wurde, wird es mit dem VpnSite mit dem Befehl New-AzVpnConnection verbunden.</span><span class="sxs-lookup"><span data-stu-id="64959-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="64959-115">Anschließend wird die Verbindung mit dem Verbindungsnamen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="64959-115">Then it gets the connection using the connection name.</span></span>

### <span data-ttu-id="64959-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="64959-116">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnConnection -ResourceGroupName ps9361 -ParentResourceName testvpngw -Name test*

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection1

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection2
```

<span data-ttu-id="64959-117">Dieses Cmdlet ruft alle Verbindungen ab, die mit "Test" beginnen.</span><span class="sxs-lookup"><span data-stu-id="64959-117">This cmdlet gets all connections that start with "test".</span></span>

## <span data-ttu-id="64959-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="64959-118">PARAMETERS</span></span>

### <span data-ttu-id="64959-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64959-119">-DefaultProfile</span></span>
<span data-ttu-id="64959-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="64959-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64959-121">-Name</span><span class="sxs-lookup"><span data-stu-id="64959-121">-Name</span></span>
<span data-ttu-id="64959-122">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="64959-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64959-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="64959-123">-ParentObject</span></span>
<span data-ttu-id="64959-124">Der übergeordnete VpnGateway für diese Verbindung.</span><span class="sxs-lookup"><span data-stu-id="64959-124">The parent VpnGateway for this connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64959-125">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="64959-125">-ParentResourceId</span></span>
<span data-ttu-id="64959-126">Die Ressourcen-ID des übergeordneten VpnGateway für diese Verbindung.</span><span class="sxs-lookup"><span data-stu-id="64959-126">The resource id of the parent VpnGateway for this connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64959-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="64959-127">-ParentResourceName</span></span>
<span data-ttu-id="64959-128">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="64959-128">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64959-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64959-129">-ResourceGroupName</span></span>
<span data-ttu-id="64959-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="64959-130">The resource group name.</span></span>

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

### <span data-ttu-id="64959-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64959-131">CommonParameters</span></span>
<span data-ttu-id="64959-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64959-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64959-133">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64959-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64959-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="64959-134">INPUTS</span></span>

### <span data-ttu-id="64959-135">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="64959-135">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="64959-136">System. String</span><span class="sxs-lookup"><span data-stu-id="64959-136">System.String</span></span>

## <span data-ttu-id="64959-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="64959-137">OUTPUTS</span></span>

### <span data-ttu-id="64959-138">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="64959-138">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="64959-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="64959-139">NOTES</span></span>

## <span data-ttu-id="64959-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="64959-140">RELATED LINKS</span></span>

[<span data-ttu-id="64959-141">Neu – AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="64959-141">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="64959-142">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="64959-142">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="64959-143">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="64959-143">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
