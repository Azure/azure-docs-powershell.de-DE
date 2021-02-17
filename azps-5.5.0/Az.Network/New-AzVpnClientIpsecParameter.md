---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
ms.openlocfilehash: f57c3d4711fe0c05e79f0d7dbeca897475f78421
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154233"
---
# <span data-ttu-id="4fb43-101">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="4fb43-101">New-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="4fb43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fb43-102">SYNOPSIS</span></span>
<span data-ttu-id="4fb43-103">Mit diesem Befehl können die Benutzer das Vpn ipsec-Parameterobjekt erstellen, das einen oder alle Werte wie "IpsecEncryption", "IpsecIntegrity", "IkeEncryption", "IkeIntegrity", "DhGroup", "PfsGroup" anfordert, die für das vorhandene VPN-Gateway festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4fb43-103">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="4fb43-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4fb43-104">SYNTAX</span></span>

```
New-AzVpnClientIpsecParameter [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fb43-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4fb43-105">DESCRIPTION</span></span>
<span data-ttu-id="4fb43-106">Mit diesem Befehl können die Benutzer das Vpn ipsec-Parameterobjekt erstellen, das einen oder alle Werte wie "IpsecEncryption", "IpsecIntegrity", "IkeEncryption", "IkeIntegrity", "DhGroup", "PfsGroup" anfordert, die für das vorhandene VPN-Gateway festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4fb43-106">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="4fb43-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4fb43-107">EXAMPLES</span></span>

### <span data-ttu-id="4fb43-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4fb43-108">Example 1</span></span>
```
PS C:\> $vpnclientipsecparams1 = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName $rname -ResourceGroupName $rgname -VpnClientIPsecParameter $vpnclientipsecparams1
```

<span data-ttu-id="4fb43-109">New-AzVpnClientIpsecParameter cmdlet wird verwendet, um das Vpn-IPSec-Parameterobjekt zu erstellen, in dem die übergebenen Werte eines oder aller Parameter verwendet werden, die der Benutzer für ein vorhandenes virtuelles Netzwerkgateway in ResourceGroup festlegen kann.</span><span class="sxs-lookup"><span data-stu-id="4fb43-109">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="4fb43-110">Dieses erstellte "VpnClientIPsecParameters"-Objekt wird an den Befehl Set-AzVpnClientIpsecParameter übergeben, um die angegebene benutzerdefinierte Vpn -Ipsec-Richtlinie für das virtuelle Netzwerkgateway wie im obigen Beispiel gezeigt zu festlegen.</span><span class="sxs-lookup"><span data-stu-id="4fb43-110">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="4fb43-111">Dieser Befehl gibt das Objekt "VpnClientIPsecParameters" zurück, das die festgelegten Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="4fb43-111">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="4fb43-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4fb43-112">PARAMETERS</span></span>

### <span data-ttu-id="4fb43-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fb43-113">-DefaultProfile</span></span>
<span data-ttu-id="4fb43-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4fb43-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fb43-115">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="4fb43-115">-DhGroup</span></span>
<span data-ttu-id="4fb43-116">Die VpnClient -DH-Gruppen, die in IKE Phase 1 für den anfänglichen SA verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="4fb43-116">The VpnClient DH Groups used in IKE Phase 1 for initial SA.</span></span>

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

### <span data-ttu-id="4fb43-117">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="4fb43-117">-IkeEncryption</span></span>
<span data-ttu-id="4fb43-118">Der VpnClient-IKE-Verschlüsselungsalgorithmus (IKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="4fb43-118">The VpnClient IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="4fb43-119">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="4fb43-119">-IkeIntegrity</span></span>
<span data-ttu-id="4fb43-120">Der VpnClient-IKE-Integritätsalgorithmus (IKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="4fb43-120">The VpnClient IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="4fb43-121">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="4fb43-121">-IpsecEncryption</span></span>
<span data-ttu-id="4fb43-122">Der VpnClient-IPSec-Verschlüsselungsalgorithmus (IKE Phase 1)</span><span class="sxs-lookup"><span data-stu-id="4fb43-122">The VpnClient IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="4fb43-123">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="4fb43-123">-IpsecIntegrity</span></span>
<span data-ttu-id="4fb43-124">Der VpnClient-IPSec-Integritätsalgorithmus (IKE Phase 1)</span><span class="sxs-lookup"><span data-stu-id="4fb43-124">The VpnClient IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="4fb43-125">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="4fb43-125">-PfsGroup</span></span>
<span data-ttu-id="4fb43-126">Die vpnClient-PFS-Gruppen, die in IKE Phase 2 für das neue untergeordnete SA verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4fb43-126">The VpnClient PFS Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="4fb43-127">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="4fb43-127">-SADataSize</span></span>
<span data-ttu-id="4fb43-128">Die Nutzlastgröße der VPNClient IPSec Security Association (auch als Schnellmodus oder Phase 2 SA bezeichnet) in KB</span><span class="sxs-lookup"><span data-stu-id="4fb43-128">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="4fb43-129">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="4fb43-129">-SALifeTime</span></span>
<span data-ttu-id="4fb43-130">Die Lebensdauer der VPNClient IPSec Security Association (auch als Schnellmodus oder Phase 2 SA bezeichnet) in Sekunden</span><span class="sxs-lookup"><span data-stu-id="4fb43-130">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="4fb43-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fb43-131">CommonParameters</span></span>
<span data-ttu-id="4fb43-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fb43-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fb43-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fb43-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fb43-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4fb43-134">INPUTS</span></span>

### <span data-ttu-id="4fb43-135">Keine</span><span class="sxs-lookup"><span data-stu-id="4fb43-135">None</span></span>

## <span data-ttu-id="4fb43-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4fb43-136">OUTPUTS</span></span>

### <span data-ttu-id="4fb43-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="4fb43-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="4fb43-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4fb43-138">NOTES</span></span>

## <span data-ttu-id="4fb43-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4fb43-139">RELATED LINKS</span></span>

[<span data-ttu-id="4fb43-140">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="4fb43-140">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="4fb43-141">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="4fb43-141">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="4fb43-142">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="4fb43-142">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
