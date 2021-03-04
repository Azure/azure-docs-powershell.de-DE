---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azradiusserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
ms.openlocfilehash: d739741333f0c50da237fc29d96ac2dd02435280
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921720"
---
# <span data-ttu-id="a16f3-101">New-AzRadiusServer</span><span class="sxs-lookup"><span data-stu-id="a16f3-101">New-AzRadiusServer</span></span>

## <span data-ttu-id="a16f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a16f3-102">SYNOPSIS</span></span>
<span data-ttu-id="a16f3-103">Erstellt eine Serverkonfiguration für externen Radius</span><span class="sxs-lookup"><span data-stu-id="a16f3-103">Creates an external radius server configuration</span></span>

## <span data-ttu-id="a16f3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a16f3-104">SYNTAX</span></span>

```
New-AzRadiusServer -RadiusServerAddress <String> -RadiusServerSecret <SecureString>
 [-RadiusServerScore <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a16f3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a16f3-105">DESCRIPTION</span></span>
<span data-ttu-id="a16f3-106">Das New-AzRadiusServer-Cmdlet erstellt eine Konfiguration des externen Radiusservers, die in der Konfiguration des Gateways für virtuelle Netzwerke und des VPN-Servers verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a16f3-106">The New-AzRadiusServer cmdlet creates an external radius server configuration to be used in virtual network gateway and VPN server configuration.</span></span>

## <span data-ttu-id="a16f3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a16f3-107">EXAMPLES</span></span>

### <span data-ttu-id="a16f3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a16f3-108">Example 1</span></span>
```powershell
PS C:\> $radiusServer1 = New-AzRadiusServer -RadiusServerAddress 10.1.0.1 -RadiusServerSecret $radiuspd -RadiusServerScore 30
PS C:\> $radiusServer2 = New-AzRadiusServer -RadiusServerAddress 10.1.0.2 -RadiusServerSecret $radiuspd -RadiusServerScore 1
PS C:\> New-AzVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku VpnGw1 -VpnClientAddressPool 201.169.0.0/16 -VpnClientProtocol "IkeV2" -RadiusServerList $radiusServers
```

<span data-ttu-id="a16f3-109">Erstellen mehrerer Konfigurationen für externe Radiusserver, die zum Konfigurieren von P2S auf einem neuen Gateway für virtuelle Netzwerke verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a16f3-109">Creating multiple external radius server configurations to be used for configuring P2S on a new virtual network gateway.</span></span>

## <span data-ttu-id="a16f3-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a16f3-110">PARAMETERS</span></span>

### <span data-ttu-id="a16f3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a16f3-111">-DefaultProfile</span></span>
<span data-ttu-id="a16f3-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a16f3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a16f3-113">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="a16f3-113">-RadiusServerAddress</span></span>
<span data-ttu-id="a16f3-114">Serveradresse für externen Radius</span><span class="sxs-lookup"><span data-stu-id="a16f3-114">External radius server address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a16f3-115">-RadiusServerScore</span><span class="sxs-lookup"><span data-stu-id="a16f3-115">-RadiusServerScore</span></span>
<span data-ttu-id="a16f3-116">Externes Radius-Serverergebnis</span><span class="sxs-lookup"><span data-stu-id="a16f3-116">External radius server score</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a16f3-117">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="a16f3-117">-RadiusServerSecret</span></span>
<span data-ttu-id="a16f3-118">Geheimer Server für externen Radius</span><span class="sxs-lookup"><span data-stu-id="a16f3-118">External radius server secret</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a16f3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a16f3-119">CommonParameters</span></span>
<span data-ttu-id="a16f3-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a16f3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a16f3-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a16f3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a16f3-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a16f3-122">INPUTS</span></span>

### <span data-ttu-id="a16f3-123">System.String</span><span class="sxs-lookup"><span data-stu-id="a16f3-123">System.String</span></span>

### <span data-ttu-id="a16f3-124">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="a16f3-124">System.Security.SecureString</span></span>

### <span data-ttu-id="a16f3-125">System.Int32</span><span class="sxs-lookup"><span data-stu-id="a16f3-125">System.Int32</span></span>

## <span data-ttu-id="a16f3-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a16f3-126">OUTPUTS</span></span>

### <span data-ttu-id="a16f3-127">Microsoft.Azure.Commands.Network.Models.PSRadiusServer</span><span class="sxs-lookup"><span data-stu-id="a16f3-127">Microsoft.Azure.Commands.Network.Models.PSRadiusServer</span></span>

## <span data-ttu-id="a16f3-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a16f3-128">NOTES</span></span>

## <span data-ttu-id="a16f3-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a16f3-129">RELATED LINKS</span></span>
