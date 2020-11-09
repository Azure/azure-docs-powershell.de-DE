---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azradiusserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
ms.openlocfilehash: 0f92f09d3caf481f845c96942fd038a82c1078ee
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301918"
---
# <span data-ttu-id="fefa8-101">New-AzRadiusServer</span><span class="sxs-lookup"><span data-stu-id="fefa8-101">New-AzRadiusServer</span></span>

## <span data-ttu-id="fefa8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fefa8-102">SYNOPSIS</span></span>
<span data-ttu-id="fefa8-103">Erstellt eine externe RADIUS-Serverkonfiguration</span><span class="sxs-lookup"><span data-stu-id="fefa8-103">Creates an external radius server configuration</span></span>

## <span data-ttu-id="fefa8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fefa8-104">SYNTAX</span></span>

```
New-AzRadiusServer -RadiusServerAddress <String> -RadiusServerSecret <SecureString>
 [-RadiusServerScore <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fefa8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fefa8-105">DESCRIPTION</span></span>
<span data-ttu-id="fefa8-106">Das New-AzRadiusServer-Cmdlet erstellt eine externe RADIUS-Serverkonfiguration, die im virtuellen Netzwerkgateway und in der VPN-Serverkonfiguration verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fefa8-106">The New-AzRadiusServer cmdlet creates an external radius server configuration to be used in virtual network gateway and VPN server configuration.</span></span>

## <span data-ttu-id="fefa8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fefa8-107">EXAMPLES</span></span>

### <span data-ttu-id="fefa8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fefa8-108">Example 1</span></span>
```powershell
PS C:\> $radiusServer1 = New-AzRadiusServer -RadiusServerAddress 10.1.0.1 -RadiusServerSecret $radiuspd -RadiusServerScore 30
PS C:\> $radiusServer2 = New-AzRadiusServer -RadiusServerAddress 10.1.0.2 -RadiusServerSecret $radiuspd -RadiusServerScore 1
PS C:\> New-AzVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku VpnGw1 -VpnClientAddressPool 201.169.0.0/16 -VpnClientProtocol "IkeV2" -RadiusServerList $radiusServers
```

<span data-ttu-id="fefa8-109">Erstellen mehrerer externer RADIUS-Serverkonfigurationen, die für die Konfiguration von P2S auf einem neuen virtuellen Netzwerkgateway verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fefa8-109">Creating multiple external radius server configurations to be used for configuring P2S on a new virtual network gateway.</span></span>

## <span data-ttu-id="fefa8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fefa8-110">PARAMETERS</span></span>

### <span data-ttu-id="fefa8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fefa8-111">-DefaultProfile</span></span>
<span data-ttu-id="fefa8-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fefa8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fefa8-113">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="fefa8-113">-RadiusServerAddress</span></span>
<span data-ttu-id="fefa8-114">Externe RADIUS-Serveradresse</span><span class="sxs-lookup"><span data-stu-id="fefa8-114">External radius server address</span></span>

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

### <span data-ttu-id="fefa8-115">-RadiusServerScore</span><span class="sxs-lookup"><span data-stu-id="fefa8-115">-RadiusServerScore</span></span>
<span data-ttu-id="fefa8-116">Externer RADIUS-Server-Score</span><span class="sxs-lookup"><span data-stu-id="fefa8-116">External radius server score</span></span>

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

### <span data-ttu-id="fefa8-117">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="fefa8-117">-RadiusServerSecret</span></span>
<span data-ttu-id="fefa8-118">Externer RADIUS-Server-Schlüssel</span><span class="sxs-lookup"><span data-stu-id="fefa8-118">External radius server secret</span></span>

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

### <span data-ttu-id="fefa8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fefa8-119">CommonParameters</span></span>
<span data-ttu-id="fefa8-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fefa8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fefa8-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fefa8-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fefa8-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fefa8-122">INPUTS</span></span>

### <span data-ttu-id="fefa8-123">System. String</span><span class="sxs-lookup"><span data-stu-id="fefa8-123">System.String</span></span>

### <span data-ttu-id="fefa8-124">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="fefa8-124">System.Security.SecureString</span></span>

### <span data-ttu-id="fefa8-125">System. Int32</span><span class="sxs-lookup"><span data-stu-id="fefa8-125">System.Int32</span></span>

## <span data-ttu-id="fefa8-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fefa8-126">OUTPUTS</span></span>

### <span data-ttu-id="fefa8-127">Microsoft. Azure. Commands. Network. Models. PSRadiusServer</span><span class="sxs-lookup"><span data-stu-id="fefa8-127">Microsoft.Azure.Commands.Network.Models.PSRadiusServer</span></span>

## <span data-ttu-id="fefa8-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="fefa8-128">NOTES</span></span>

## <span data-ttu-id="fefa8-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fefa8-129">RELATED LINKS</span></span>
