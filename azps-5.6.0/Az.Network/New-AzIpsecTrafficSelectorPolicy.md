---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azipsectrafficselectorpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
ms.openlocfilehash: 6980ccc3e3ad9c69755253183da1d83f522973da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947776"
---
# <span data-ttu-id="b31af-101">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="b31af-101">New-AzIpsecTrafficSelectorPolicy</span></span>

## <span data-ttu-id="b31af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b31af-102">SYNOPSIS</span></span>
<span data-ttu-id="b31af-103">Erstellt eine Datenverkehrsauswahlrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="b31af-103">Creates a traffic selector policy.</span></span>

## <span data-ttu-id="b31af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b31af-104">SYNTAX</span></span>

```
New-AzIpsecTrafficSelectorPolicy -LocalAddressRange <String[]> -RemoteAddressRange <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b31af-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b31af-105">DESCRIPTION</span></span>
<span data-ttu-id="b31af-106">Das New-AzTrafficSelectorPolicy-Cmdlet erstellt einen Vorschlag für eine Datenverkehrsauswahlrichtlinie, der in einer Gatewayverbindung für virtuelle Netzwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b31af-106">The New-AzTrafficSelectorPolicy cmdlet creates a traffic selector policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="b31af-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b31af-107">EXAMPLES</span></span>

### <span data-ttu-id="b31af-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b31af-108">Example 1</span></span>
```powershell
$trafficSelectorPolicy = New-AzIpsecTrafficSelectorPolicy -LocalAddressRange ("10.10.10.0/24", "20.20.20.0/24") -RemoteAddressRange ("30.30.30.0/24", "40.40.40.0/24")
New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -TrafficSelectorPolicies ($trafficSelectorPolicy)
```

<span data-ttu-id="b31af-109">Erstellt eine Instanz einer Datenverkehrsauswahlrichtlinie und fügt sie als Parameter beim Erstellen einer Gatewayverbindung für virtuelle Netzwerke mit einem IKEv2-Protokoll hinzu.</span><span class="sxs-lookup"><span data-stu-id="b31af-109">Creates an instance of a traffic selector policy and adds it as a parameter when creating a virtual network gateway connection with an IKEv2 protocol.</span></span>

## <span data-ttu-id="b31af-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b31af-110">PARAMETERS</span></span>

### <span data-ttu-id="b31af-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b31af-111">-DefaultProfile</span></span>
<span data-ttu-id="b31af-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b31af-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b31af-113">-LocalAddressRange</span><span class="sxs-lookup"><span data-stu-id="b31af-113">-LocalAddressRange</span></span>
<span data-ttu-id="b31af-114">Eine Sammlung von CIDR-Adressbereichen</span><span class="sxs-lookup"><span data-stu-id="b31af-114">A collection of CIDR address ranges</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b31af-115">-RemoteAddressRange</span><span class="sxs-lookup"><span data-stu-id="b31af-115">-RemoteAddressRange</span></span>
<span data-ttu-id="b31af-116">Eine Sammlung von CIDR-Adressbereichen</span><span class="sxs-lookup"><span data-stu-id="b31af-116">A collection of CIDR address ranges</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b31af-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b31af-117">CommonParameters</span></span>
<span data-ttu-id="b31af-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b31af-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b31af-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b31af-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b31af-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b31af-120">INPUTS</span></span>

### <span data-ttu-id="b31af-121">System.String[]</span><span class="sxs-lookup"><span data-stu-id="b31af-121">System.String[]</span></span>

## <span data-ttu-id="b31af-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b31af-122">OUTPUTS</span></span>

### <span data-ttu-id="b31af-123">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="b31af-123">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy</span></span>

## <span data-ttu-id="b31af-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b31af-124">NOTES</span></span>

## <span data-ttu-id="b31af-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b31af-125">RELATED LINKS</span></span>
