---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azradiusserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
ms.openlocfilehash: 0f92f09d3caf481f845c96942fd038a82c1078ee
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459888"
---
# <span data-ttu-id="9d959-101">New-AzRadiusServer</span><span class="sxs-lookup"><span data-stu-id="9d959-101">New-AzRadiusServer</span></span>

## <span data-ttu-id="9d959-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d959-102">SYNOPSIS</span></span>
<span data-ttu-id="9d959-103">Erstellt eine Konfiguration des externen Radiusservers</span><span class="sxs-lookup"><span data-stu-id="9d959-103">Creates an external radius server configuration</span></span>

## <span data-ttu-id="9d959-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d959-104">SYNTAX</span></span>

```
New-AzRadiusServer -RadiusServerAddress <String> -RadiusServerSecret <SecureString>
 [-RadiusServerScore <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d959-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9d959-105">DESCRIPTION</span></span>
<span data-ttu-id="9d959-106">Das New-AzRadiusServer erstellt eine Konfiguration des externen Radiusservers, die in der Konfiguration des virtuellen Netzwerkgateways und des VPN-Servers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9d959-106">The New-AzRadiusServer cmdlet creates an external radius server configuration to be used in virtual network gateway and VPN server configuration.</span></span>

## <span data-ttu-id="9d959-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9d959-107">EXAMPLES</span></span>

### <span data-ttu-id="9d959-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9d959-108">Example 1</span></span>
```powershell
PS C:\> $radiusServer1 = New-AzRadiusServer -RadiusServerAddress 10.1.0.1 -RadiusServerSecret $radiuspd -RadiusServerScore 30
PS C:\> $radiusServer2 = New-AzRadiusServer -RadiusServerAddress 10.1.0.2 -RadiusServerSecret $radiuspd -RadiusServerScore 1
PS C:\> New-AzVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku VpnGw1 -VpnClientAddressPool 201.169.0.0/16 -VpnClientProtocol "IkeV2" -RadiusServerList $radiusServers
```

<span data-ttu-id="9d959-109">Erstellen mehrerer Konfigurationen des externen Radiusservers zur Konfiguration von P2S auf einem neuen virtuellen Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="9d959-109">Creating multiple external radius server configurations to be used for configuring P2S on a new virtual network gateway.</span></span>

## <span data-ttu-id="9d959-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d959-110">PARAMETERS</span></span>

### <span data-ttu-id="9d959-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d959-111">-DefaultProfile</span></span>
<span data-ttu-id="9d959-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9d959-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d959-113">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="9d959-113">-RadiusServerAddress</span></span>
<span data-ttu-id="9d959-114">Serveradresse des externen Radius</span><span class="sxs-lookup"><span data-stu-id="9d959-114">External radius server address</span></span>

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

### <span data-ttu-id="9d959-115">-RadiusServerScore</span><span class="sxs-lookup"><span data-stu-id="9d959-115">-RadiusServerScore</span></span>
<span data-ttu-id="9d959-116">Bewertung des externen Radiusservers</span><span class="sxs-lookup"><span data-stu-id="9d959-116">External radius server score</span></span>

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

### <span data-ttu-id="9d959-117">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="9d959-117">-RadiusServerSecret</span></span>
<span data-ttu-id="9d959-118">Externer Servergeheimnis des Radius</span><span class="sxs-lookup"><span data-stu-id="9d959-118">External radius server secret</span></span>

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

### <span data-ttu-id="9d959-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d959-119">CommonParameters</span></span>
<span data-ttu-id="9d959-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d959-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d959-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d959-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d959-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9d959-122">INPUTS</span></span>

### <span data-ttu-id="9d959-123">System.String</span><span class="sxs-lookup"><span data-stu-id="9d959-123">System.String</span></span>

### <span data-ttu-id="9d959-124">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="9d959-124">System.Security.SecureString</span></span>

### <span data-ttu-id="9d959-125">System.Int32</span><span class="sxs-lookup"><span data-stu-id="9d959-125">System.Int32</span></span>

## <span data-ttu-id="9d959-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9d959-126">OUTPUTS</span></span>

### <span data-ttu-id="9d959-127">Microsoft.Azure.Commands.Network.Models.PSRadiusServer</span><span class="sxs-lookup"><span data-stu-id="9d959-127">Microsoft.Azure.Commands.Network.Models.PSRadiusServer</span></span>

## <span data-ttu-id="9d959-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9d959-128">NOTES</span></span>

## <span data-ttu-id="9d959-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9d959-129">RELATED LINKS</span></span>
