---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 9516d132f2c6b26c162dcbb8abc742e69dccfc14
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660312"
---
# <span data-ttu-id="c36a1-101">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="c36a1-101">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="c36a1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c36a1-102">SYNOPSIS</span></span>
<span data-ttu-id="c36a1-103">Entfernt die Standardwebsite aus einem virtuellen Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="c36a1-103">Removes the default site from a virtual network gateway.</span></span>

## <span data-ttu-id="c36a1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c36a1-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c36a1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c36a1-105">DESCRIPTION</span></span>
<span data-ttu-id="c36a1-106">Das Cmdlet **Remove-AzVirtualNetworkGatewayDefaultSite** entfernt die erzwungene Tunneling-Standardwebsite von einem virtuellen Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="c36a1-106">The **Remove-AzVirtualNetworkGatewayDefaultSite** cmdlet removes the forced tunneling default site from a virtual network gateway.</span></span>
<span data-ttu-id="c36a1-107">Erzwungener Tunneling bietet Ihnen eine Möglichkeit, den Internet gebundenen Datenverkehr von Azure Virtual Machines zu Ihrem lokalen Netzwerk umzuleiten. auf diese Weise können Sie den Datenverkehr prüfen und überwachen, bevor Sie ihn freigeben.</span><span class="sxs-lookup"><span data-stu-id="c36a1-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="c36a1-108">Erzwungener Tunneling wird mithilfe eines VPN-Tunnels (virtuelles privates Netzwerk) durchgeführt. Dieser Tunnel erfordert eine Standardwebsite, ein lokales Gateway, in dem der gesamte Azure Internet gebundene Datenverkehr umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="c36a1-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="c36a1-109">**Remove-AzVirtualNetworkGatewayDefaultSite** entfernt die Standardwebsite, die einem Gateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="c36a1-109">**Remove-AzVirtualNetworkGatewayDefaultSite** removes the default site assigned to a gateway.</span></span>
<span data-ttu-id="c36a1-110">In diesem Fall müssen Sie Set-AzVirtualNetworkGatewayDefaultSite verwenden, um eine neue Standardwebsite zuzuweisen, bevor das Gateway für erzwungenen Tunneln verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c36a1-110">If you do this you will need to use Set-AzVirtualNetworkGatewayDefaultSite to assign a new default site before the gateway can be used for forced tunneling.</span></span>

## <span data-ttu-id="c36a1-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c36a1-111">EXAMPLES</span></span>

### <span data-ttu-id="c36a1-112">Beispiel 1: Entfernen der Standardwebsite, die einem virtuellen Netzwerkgateway zugewiesen ist</span><span class="sxs-lookup"><span data-stu-id="c36a1-112">Example 1: Remove the default site assigned to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway $Gateway
```

<span data-ttu-id="c36a1-113">In diesem Beispiel wird die Standardwebsite entfernt, die derzeit einem virtuellen Netzwerkgateway mit dem Namen ContosoVirtualGateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="c36a1-113">This example removes the default site currently assigned to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="c36a1-114">Der erste Befehl verwendet " **Get-AzVirtualNetworkGateway** ", um einen Objektverweis auf das Gateway zu erstellen. dieser Objektverweis wird in einer Variablen mit dem Namen $Gateway gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c36a1-114">The first command uses **Get-AzVirtualNetworkGateway** to create an object reference to the gateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="c36a1-115">Der zweite Befehl verwendet dann **Remove-AzVirtualNetworkGatewayDefaultSite** , um die dem Gateway zugewiesene Standardwebsite zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="c36a1-115">The second command then uses **Remove-AzVirtualNetworkGatewayDefaultSite** to remove the default site assigned to that gateway.</span></span>

## <span data-ttu-id="c36a1-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="c36a1-116">PARAMETERS</span></span>

### <span data-ttu-id="c36a1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c36a1-117">-DefaultProfile</span></span>
<span data-ttu-id="c36a1-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c36a1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c36a1-119">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c36a1-119">-VirtualNetworkGateway</span></span>
<span data-ttu-id="c36a1-120">Gibt einen Objektverweis auf das virtuelle Netzwerkgateway an, das die zu entfernende Standardwebsite enthält.</span><span class="sxs-lookup"><span data-stu-id="c36a1-120">Specifies an object reference to the virtual network gateway containing the default site to be removed.</span></span>
<span data-ttu-id="c36a1-121">Sie können einen Objektverweis auf ein virtuelles Netzwerkgateway erstellen, indem Sie den Get-AzVirtualNetworkGateway verwenden und den Namen des Gateways angeben.</span><span class="sxs-lookup"><span data-stu-id="c36a1-121">You can create an object reference to a virtual network gateway by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c36a1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c36a1-122">CommonParameters</span></span>
<span data-ttu-id="c36a1-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c36a1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c36a1-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c36a1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c36a1-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c36a1-125">INPUTS</span></span>

### <span data-ttu-id="c36a1-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c36a1-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="c36a1-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c36a1-127">OUTPUTS</span></span>

### <span data-ttu-id="c36a1-128">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c36a1-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="c36a1-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="c36a1-129">NOTES</span></span>

## <span data-ttu-id="c36a1-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c36a1-130">RELATED LINKS</span></span>

[<span data-ttu-id="c36a1-131">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c36a1-131">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="c36a1-132">Satz-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="c36a1-132">Set-AzVirtualNetworkGatewayDefaultSite</span></span>](./Set-AzVirtualNetworkGatewayDefaultSite.md)


