---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
ms.openlocfilehash: 7556a2d23d4c4969c3037d6b49dbd482bcdea207
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924672"
---
# <span data-ttu-id="f4d90-101">New-AzVpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="f4d90-101">New-AzVpnClientIpsecPolicy</span></span>

## <span data-ttu-id="f4d90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4d90-102">SYNOPSIS</span></span>
<span data-ttu-id="f4d90-103">Mit diesem Befehl können die Benutzer das Vpn ipsec-Richtlinienobjekt erstellen, das einen oder alle Werte wie IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup für das VPN-Gateway anfordert.</span><span class="sxs-lookup"><span data-stu-id="f4d90-103">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="f4d90-104">Mit diesem Befehl können Ausgabeobjekt verwendet werden, um die VPN-IPSec-Richtlinie für das neue /vorhandene Gateway zu legen.</span><span class="sxs-lookup"><span data-stu-id="f4d90-104">This command let output object is used to set vpn ipsec policy for both new / existing gateway.</span></span>

## <span data-ttu-id="f4d90-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4d90-105">SYNTAX</span></span>

```
New-AzVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4d90-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f4d90-106">DESCRIPTION</span></span>
<span data-ttu-id="f4d90-107">Mit diesem Befehl können die Benutzer das Vpn ipsec-Richtlinienobjekt erstellen, das einen oder alle Werte wie IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup für das VPN-Gateway anfordert.</span><span class="sxs-lookup"><span data-stu-id="f4d90-107">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="f4d90-108">Mit diesem Befehl können Ausgabeobjekt verwendet werden, um die VPN-IPSec-Richtlinie für das neue /vorhandene Gateway zu legen.</span><span class="sxs-lookup"><span data-stu-id="f4d90-108">This command let output object is used to set vpn ipsec policy for both new / existing gateway.</span></span>

## <span data-ttu-id="f4d90-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f4d90-109">EXAMPLES</span></span>

### <span data-ttu-id="f4d90-110">Beispiel 1: Definieren des Vpn-Ipsec-Richtlinienobjekts:</span><span class="sxs-lookup"><span data-stu-id="f4d90-110">Example 1: Define vpn ipsec policy object:</span></span>
```powershell
PS C:\>$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

<span data-ttu-id="f4d90-111">Dieses Cmdlet wird verwendet, um das vpn ipsec-Richtlinienobjekt mit den übergebenen Werten eines oder aller Parameter zu erstellen, die der Benutzer an param:VpnClientIpsecPolicy of PS übergeben kann: New-AzVirtualNetworkGateway (New VPN Gateway creation) / Set-AzVirtualNetworkGateway (existing VPN Gateway update) in ResourceGroup :</span><span class="sxs-lookup"><span data-stu-id="f4d90-111">This cmdlet is used to create the vpn ipsec policy object using the passed one or all parameters' values which user can pass to param:VpnClientIpsecPolicy of PS command let: New-AzVirtualNetworkGateway (New VPN Gateway creation) / Set-AzVirtualNetworkGateway (existing VPN Gateway update) in ResourceGroup :</span></span>

### <span data-ttu-id="f4d90-112">Beispiel 2: Erstellen eines neuen virtuellen Netzwerkgateways mit dem Festlegen einer benutzerdefinierten Vpn-IPSec-Richtlinie:</span><span class="sxs-lookup"><span data-stu-id="f4d90-112">Example 2: Create new virtual network gateway with setting vpn custom ipsec policy:</span></span>
```powershell
PS C:\> $vnetGateway = New-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="f4d90-113">Dieses Cmdlet gibt das Objekt des virtuellen Netzwerkgateways nach der Erstellung zurück.</span><span class="sxs-lookup"><span data-stu-id="f4d90-113">This cmdlet returns virtual network gateway object after creation.</span></span> 

### <span data-ttu-id="f4d90-114">Beispiel 3: Festlegen der benutzerdefinierten Vpn-IPSec-Richtlinie für vorhandenes Gateway für virtuelle Netzwerke:</span><span class="sxs-lookup"><span data-stu-id="f4d90-114">Example 3: Set vpn custom ipsec policy on existing virtual network gateway:</span></span>
```powershell
PS C:\> $vnetGateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="f4d90-115">Dieses Cmdlet gibt virtuelles Netzwerkgatewayobjekt zurück, nachdem eine benutzerdefinierte Vpn-IPSec-Richtlinie konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="f4d90-115">This cmdlet returns virtual network gateway object after setting vpn custom ipsec policy.</span></span>

### <span data-ttu-id="f4d90-116">Beispiel 4: Holen Sie sich das Gateway für virtuelles Netzwerk, um zu sehen, ob die benutzerdefinierte Vpn-Richtlinie richtig festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="f4d90-116">Example 4: Get virtual network gateway to see if vpn custom policy is set correctly:</span></span>
```powershell
PS C:\> $gateway = Get-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

<span data-ttu-id="f4d90-117">Dieses Cmdlet gibt virtuelles Netzwerkgatewayobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="f4d90-117">This cmdlet returns virtual network gateway object.</span></span>

## <span data-ttu-id="f4d90-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f4d90-118">PARAMETERS</span></span>

### <span data-ttu-id="f4d90-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4d90-119">-DefaultProfile</span></span>
<span data-ttu-id="f4d90-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f4d90-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4d90-121">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="f4d90-121">-DhGroup</span></span>
<span data-ttu-id="f4d90-122">Die vpnClient-DH-Gruppen, die in IKE Phase 1 für die erste SA verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f4d90-122">The VpnClient DH Groups used in IKE Phase 1 for initial SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DHGroup24, ECP384, ECP256, DHGroup14, DHGroup2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4d90-123">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="f4d90-123">-IkeEncryption</span></span>
<span data-ttu-id="f4d90-124">VpnClient-IKE-Verschlüsselungsalgorithmus (IKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="f4d90-124">The VpnClient IKE encryption algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4d90-125">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="f4d90-125">-IkeIntegrity</span></span>
<span data-ttu-id="f4d90-126">Der VpnClient-IKE-Integritätsalgorithmus (IKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="f4d90-126">The VpnClient IKE integrity algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SHA384, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4d90-127">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="f4d90-127">-IpsecEncryption</span></span>
<span data-ttu-id="f4d90-128">VpnClient-IPSec-Verschlüsselungsalgorithmus (IKE Phase 1)</span><span class="sxs-lookup"><span data-stu-id="f4d90-128">The VpnClient IPSec encryption algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4d90-129">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="f4d90-129">-IpsecIntegrity</span></span>
<span data-ttu-id="f4d90-130">Der VpnClient-IPSec-Integritätsalgorithmus (IKE Phase 1)</span><span class="sxs-lookup"><span data-stu-id="f4d90-130">The VpnClient IPSec integrity algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4d90-131">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="f4d90-131">-PfsGroup</span></span>
<span data-ttu-id="f4d90-132">Die vpnClient-PFS-Gruppen, die in IKE Phase 2 für neue untergeordnete SA verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f4d90-132">The VpnClient PFS Groups used in IKE Phase 2 for new child SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PFS24, PFSMM, ECP384, ECP256, PFS14, PFS2, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4d90-133">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="f4d90-133">-SADataSize</span></span>
<span data-ttu-id="f4d90-134">Die Nutzlastgröße der VpnClient IPSec Security Association (auch als Schnellmodus oder Phase 2 SA bezeichnet) in KB</span><span class="sxs-lookup"><span data-stu-id="f4d90-134">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4d90-135">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="f4d90-135">-SALifeTime</span></span>
<span data-ttu-id="f4d90-136">Die Lebensdauer der VpnClient IPSec Security Association (auch als Schnellmodus oder Phase 2 SA bezeichnet) in Sekunden</span><span class="sxs-lookup"><span data-stu-id="f4d90-136">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4d90-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4d90-137">CommonParameters</span></span>
<span data-ttu-id="f4d90-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4d90-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4d90-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4d90-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4d90-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f4d90-140">INPUTS</span></span>

### <span data-ttu-id="f4d90-141">Keine</span><span class="sxs-lookup"><span data-stu-id="f4d90-141">None</span></span>

## <span data-ttu-id="f4d90-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f4d90-142">OUTPUTS</span></span>

### <span data-ttu-id="f4d90-143">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="f4d90-143">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="f4d90-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f4d90-144">NOTES</span></span>

## <span data-ttu-id="f4d90-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f4d90-145">RELATED LINKS</span></span>
