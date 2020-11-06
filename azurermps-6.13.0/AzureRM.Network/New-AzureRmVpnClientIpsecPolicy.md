---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecPolicy.md
ms.openlocfilehash: 98ea39141614c800b7b71d2f0c75519762bb87b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504329"
---
# <span data-ttu-id="71cac-101">New-AzureRmVpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="71cac-101">New-AzureRmVpnClientIpsecPolicy</span></span>

## <span data-ttu-id="71cac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="71cac-102">SYNOPSIS</span></span>
<span data-ttu-id="71cac-103">Mit diesem Befehl können die Benutzer das VPN-IPSec-Richtlinienobjekt erstellen, das einen oder alle Werte angibt, wie IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup und PfsGroup, die auf dem VPN-Gateway festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="71cac-103">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="71cac-104">Dieser Befehl Let Output-Objekt wird verwendet, um die VPN-IPSec-Richtlinie für das neue/exisitng-Gateway einzurichten.</span><span class="sxs-lookup"><span data-stu-id="71cac-104">This command let output object is used to set vpn ipsec policy for both new / exisitng gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71cac-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="71cac-105">SYNTAX</span></span>

```
New-AzureRmVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71cac-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71cac-106">DESCRIPTION</span></span>
<span data-ttu-id="71cac-107">Mit diesem Befehl können die Benutzer das VPN-IPSec-Richtlinienobjekt erstellen, das einen oder alle Werte angibt, wie IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup und PfsGroup, die auf dem VPN-Gateway festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="71cac-107">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="71cac-108">Dieser Befehl Let Output-Objekt wird verwendet, um die VPN-IPSec-Richtlinie für das neue/exisitng-Gateway einzurichten.</span><span class="sxs-lookup"><span data-stu-id="71cac-108">This command let output object is used to set vpn ipsec policy for both new / exisitng gateway.</span></span>

## <span data-ttu-id="71cac-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="71cac-109">EXAMPLES</span></span>

### <span data-ttu-id="71cac-110">Definieren Sie das VPN-IPSec-Richtlinienobjekt:</span><span class="sxs-lookup"><span data-stu-id="71cac-110">Define vpn ipsec policy object:</span></span>
```
PS C:\>$vpnclientipsecpolicy = New-AzureRmVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

<span data-ttu-id="71cac-111">Dieses Cmdlet wird verwendet, um das VPN-IPSec-Richtlinienobjekt zu erstellen, wobei die Werte für einen oder alle Parameter übergeben werden, die der Benutzer an param: VpnClientIpsecPolicy des PS-Befehls Let: New-AzureRmVirtualNetworkGateway (neue VPN-Gateway-Erstellung)/Set-AzureRmVirtualNetworkGateway (vorhandenes VPN-Gateway-Update) in ResourceGroup übergeben kann:</span><span class="sxs-lookup"><span data-stu-id="71cac-111">This cmdlet is used to create the vpn ipsec policy object using the passed one or all parameters' values which user can pass to param:VpnClientIpsecPolicy of PS command let: New-AzureRmVirtualNetworkGateway (New VPN Gateway creation) / Set-AzureRmVirtualNetworkGateway (existing VPN Gateway update) in ResourceGroup :</span></span>

### <span data-ttu-id="71cac-112">Erstellen eines neuen virtuellen Netzwerkgateways mit dem Festlegen einer benutzerdefinierten VPN-IPSec-Richtlinie:</span><span class="sxs-lookup"><span data-stu-id="71cac-112">Create new virtual network gateway with setting vpn custom ipsec policy:</span></span>
```
PS C:\> $vnetGateway = New-AzureRmVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="71cac-113">Dieses Cmdlet gibt nach der Erstellung ein virtuelles Netzwerkgateway-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="71cac-113">This cmdlet returns virtual network gateway object after creation.</span></span> 

### <span data-ttu-id="71cac-114">Festlegen einer benutzerdefinierten VPN-IPSec-Richtlinie auf einem vorhandenen virtuellen Netzwerkgateway:</span><span class="sxs-lookup"><span data-stu-id="71cac-114">Set vpn custom ipsec policy on existing virtual network gateway:</span></span>
```
PS C:\> $vnetGateway = Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="71cac-115">Dieses Cmdlet gibt nach dem Festlegen einer benutzerdefinierten VPN-IPSec-Richtlinie virtuelles Netzwerkgateway-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="71cac-115">This cmdlet returns virtual network gateway object after setting vpn custom ipsec policy.</span></span>

### <span data-ttu-id="71cac-116">Abrufen des virtuellen Netzwerkgateways, um zu sehen, ob die benutzerdefinierte VPN-Richtlinie richtig festgesetzt ist:</span><span class="sxs-lookup"><span data-stu-id="71cac-116">Get virtual network gateway to see if vpn custom policy is set correctly:</span></span>
```
PS C:\> $gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

<span data-ttu-id="71cac-117">Dieses Cmdlet gibt virtuelles Netzwerkgateway-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="71cac-117">This cmdlet returns virtual network gateway object.</span></span>

## <span data-ttu-id="71cac-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="71cac-118">PARAMETERS</span></span>

### <span data-ttu-id="71cac-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71cac-119">-DefaultProfile</span></span>
<span data-ttu-id="71cac-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="71cac-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71cac-121">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="71cac-121">-DhGroup</span></span>
<span data-ttu-id="71cac-122">Die vpnclient-DH-Gruppen, die in der IKE-Phase 1 für Initial SA verwendet werden</span><span class="sxs-lookup"><span data-stu-id="71cac-122">The Vpnclient DH Groups used in IKE Phase 1 for initial SA</span></span>

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

### <span data-ttu-id="71cac-123">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="71cac-123">-IkeEncryption</span></span>
<span data-ttu-id="71cac-124">Der vpnclient-IKE-Verschlüsselungsalgorithmus (IKE-Phase 2)</span><span class="sxs-lookup"><span data-stu-id="71cac-124">The Vpnclient IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="71cac-125">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="71cac-125">-IkeIntegrity</span></span>
<span data-ttu-id="71cac-126">Der vpnclient-IKE-Integritätsalgorithmus (IKE-Phase 2)</span><span class="sxs-lookup"><span data-stu-id="71cac-126">The Vpnclient IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="71cac-127">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="71cac-127">-IpsecEncryption</span></span>
<span data-ttu-id="71cac-128">Der vpnclient IPSec-Verschlüsselungsalgorithmus (IKE-Phase 1)</span><span class="sxs-lookup"><span data-stu-id="71cac-128">The Vpnclient IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="71cac-129">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="71cac-129">-IpsecIntegrity</span></span>
<span data-ttu-id="71cac-130">Der vpnclient-IPSec-Integritätsalgorithmus (IKE-Phase 1)</span><span class="sxs-lookup"><span data-stu-id="71cac-130">The Vpnclient IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="71cac-131">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="71cac-131">-PfsGroup</span></span>
<span data-ttu-id="71cac-132">Die vpnclient-PFS-Gruppen, die in IKE Phase 2 für neue untergeordnete SA verwendet werden</span><span class="sxs-lookup"><span data-stu-id="71cac-132">The Vpnclient PFS Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="71cac-133">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="71cac-133">-SADataSize</span></span>
<span data-ttu-id="71cac-134">Die vpnclient IPSec-Sicherheitszuordnung (auch als Schnellmodus oder Phase 2 SA bezeichnet) Nutzlast-Größe in KB</span><span class="sxs-lookup"><span data-stu-id="71cac-134">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="71cac-135">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="71cac-135">-SALifeTime</span></span>
<span data-ttu-id="71cac-136">Die vpnclient IPSec-Sicherheitszuordnung (auch als Schnellmodus oder Phase 2 SA bezeichnet) Lebensdauer in Sekunden</span><span class="sxs-lookup"><span data-stu-id="71cac-136">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="71cac-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71cac-137">CommonParameters</span></span>
<span data-ttu-id="71cac-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71cac-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71cac-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71cac-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71cac-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="71cac-140">INPUTS</span></span>

### <span data-ttu-id="71cac-141">Keine</span><span class="sxs-lookup"><span data-stu-id="71cac-141">None</span></span>

## <span data-ttu-id="71cac-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="71cac-142">OUTPUTS</span></span>

### <span data-ttu-id="71cac-143">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="71cac-143">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="71cac-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="71cac-144">NOTES</span></span>

## <span data-ttu-id="71cac-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="71cac-145">RELATED LINKS</span></span>
