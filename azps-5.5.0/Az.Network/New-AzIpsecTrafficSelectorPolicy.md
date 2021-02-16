---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipsectrafficselectorpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
ms.openlocfilehash: f335272bce6591c617d8111dd1d0d81af50ec255
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160889"
---
# <span data-ttu-id="67705-101">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="67705-101">New-AzIpsecTrafficSelectorPolicy</span></span>

## <span data-ttu-id="67705-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67705-102">SYNOPSIS</span></span>
<span data-ttu-id="67705-103">Erstellt eine Richtlinie für die Datenverkehrsauswahl.</span><span class="sxs-lookup"><span data-stu-id="67705-103">Creates a traffic selector policy.</span></span>

## <span data-ttu-id="67705-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="67705-104">SYNTAX</span></span>

```
New-AzIpsecTrafficSelectorPolicy -LocalAddressRange <String[]> -RemoteAddressRange <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67705-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="67705-105">DESCRIPTION</span></span>
<span data-ttu-id="67705-106">Das New-AzTrafficSelectorPolicy erstellt einen Richtlinienvorschlag für die Datenverkehrsauswahl, der in einer Virtuellen Netzwerkgatewayverbindung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="67705-106">The New-AzTrafficSelectorPolicy cmdlet creates a traffic selector policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="67705-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="67705-107">EXAMPLES</span></span>

### <span data-ttu-id="67705-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="67705-108">Example 1</span></span>
```powershell
$trafficSelectorPolicy = New-AzIpsecTrafficSelectorPolicy -LocalAddressRange ("10.10.10.0/24", "20.20.20.0/24") -RemoteAddressRange ("30.30.30.0/24", "40.40.40.0/24")
New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -TrafficSelectorPolicies ($trafficSelectorPolicy)
```

<span data-ttu-id="67705-109">Erstellt eine Instanz einer Datenverkehrsauswahlrichtlinie und fügt sie als Parameter hinzu, wenn eine virtuelle Netzwerkgatewayverbindung mit einem IKEv2-Protokoll erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="67705-109">Creates an instance of a traffic selector policy and adds it as a parameter when creating a virtual network gateway connection with an IKEv2 protocol.</span></span>

## <span data-ttu-id="67705-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67705-110">PARAMETERS</span></span>

### <span data-ttu-id="67705-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67705-111">-DefaultProfile</span></span>
<span data-ttu-id="67705-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="67705-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67705-113">-LocalAddressRange</span><span class="sxs-lookup"><span data-stu-id="67705-113">-LocalAddressRange</span></span>
<span data-ttu-id="67705-114">Eine Sammlung von CIDR-Adressbereichen</span><span class="sxs-lookup"><span data-stu-id="67705-114">A collection of CIDR address ranges</span></span>

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

### <span data-ttu-id="67705-115">-RemoteAddressRange</span><span class="sxs-lookup"><span data-stu-id="67705-115">-RemoteAddressRange</span></span>
<span data-ttu-id="67705-116">Eine Sammlung von CIDR-Adressbereichen</span><span class="sxs-lookup"><span data-stu-id="67705-116">A collection of CIDR address ranges</span></span>

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

### <span data-ttu-id="67705-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67705-117">CommonParameters</span></span>
<span data-ttu-id="67705-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67705-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67705-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67705-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67705-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="67705-120">INPUTS</span></span>

### <span data-ttu-id="67705-121">System.String[]</span><span class="sxs-lookup"><span data-stu-id="67705-121">System.String[]</span></span>

## <span data-ttu-id="67705-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="67705-122">OUTPUTS</span></span>

### <span data-ttu-id="67705-123">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="67705-123">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy</span></span>

## <span data-ttu-id="67705-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="67705-124">NOTES</span></span>

## <span data-ttu-id="67705-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="67705-125">RELATED LINKS</span></span>
