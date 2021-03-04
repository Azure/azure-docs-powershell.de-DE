---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: ddf0f6687550e544aa22efbce772c0751a7b810e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945838"
---
# <span data-ttu-id="f3287-101">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="f3287-101">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="f3287-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3287-102">SYNOPSIS</span></span>
<span data-ttu-id="f3287-103">Entfernt die Standardwebsite aus einem Gateway für virtuelle Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="f3287-103">Removes the default site from a virtual network gateway.</span></span>

## <span data-ttu-id="f3287-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f3287-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3287-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f3287-105">DESCRIPTION</span></span>
<span data-ttu-id="f3287-106">Das **Cmdlet Remove-AzVirtualNetworkGatewayDefaultSite** entfernt die Standardwebsite für erzwungenes Tunneln aus einem Gateway für virtuelle Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="f3287-106">The **Remove-AzVirtualNetworkGatewayDefaultSite** cmdlet removes the forced tunneling default site from a virtual network gateway.</span></span>
<span data-ttu-id="f3287-107">Erzwungenes Tunneln bietet Ihnen die Möglichkeit, internetgebundenen Datenverkehr von virtuellen #A0 an Ihr lokales Netzwerk umzuleiten. Auf diese Weise können Sie den Datenverkehr prüfen und überwachen, bevor Sie ihn freigeben.</span><span class="sxs-lookup"><span data-stu-id="f3287-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="f3287-108">Erzwungenes Tunneln wird mithilfe eines VPN-Tunnels (Virtual Private Network) ausgeführt. Für diesen Tunnel ist eine Standardwebsite erforderlich, ein lokales Gateway, auf dem der internetgebundene Azure-Datenverkehr umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="f3287-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="f3287-109">**Remove-AzVirtualNetworkGatewayDefaultSite** entfernt die Standardwebsite, die einem Gateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="f3287-109">**Remove-AzVirtualNetworkGatewayDefaultSite** removes the default site assigned to a gateway.</span></span>
<span data-ttu-id="f3287-110">Wenn Sie dies tun, müssen Sie Set-AzVirtualNetworkGatewayDefaultSite verwenden, um eine neue Standardwebsite zuzuordnen, bevor das Gateway für erzwungenes Tunneln verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f3287-110">If you do this you will need to use Set-AzVirtualNetworkGatewayDefaultSite to assign a new default site before the gateway can be used for forced tunneling.</span></span>

## <span data-ttu-id="f3287-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f3287-111">EXAMPLES</span></span>

### <span data-ttu-id="f3287-112">Beispiel 1: Entfernen der Standardwebsite, die einem Gateway für virtuelle Netzwerke zugewiesen ist</span><span class="sxs-lookup"><span data-stu-id="f3287-112">Example 1: Remove the default site assigned to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway $Gateway
```

<span data-ttu-id="f3287-113">In diesem Beispiel wird die Standardwebsite entfernt, die derzeit einem Virtuellen Netzwerkgateway namens ContosoVirtualGateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="f3287-113">This example removes the default site currently assigned to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="f3287-114">Der erste Befehl verwendet **Get-AzVirtualNetworkGateway,** um einen Objektverweis auf das Gateway zu erstellen. Dieser Objektverweis wird in einer Variablen mit dem Namen $Gateway.</span><span class="sxs-lookup"><span data-stu-id="f3287-114">The first command uses **Get-AzVirtualNetworkGateway** to create an object reference to the gateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="f3287-115">Der zweite Befehl verwendet dann **Remove-AzVirtualNetworkGatewayDefaultSite,** um die diesem Gateway zugewiesene Standardwebsite zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="f3287-115">The second command then uses **Remove-AzVirtualNetworkGatewayDefaultSite** to remove the default site assigned to that gateway.</span></span>

## <span data-ttu-id="f3287-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f3287-116">PARAMETERS</span></span>

### <span data-ttu-id="f3287-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3287-117">-DefaultProfile</span></span>
<span data-ttu-id="f3287-118">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3287-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3287-119">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f3287-119">-VirtualNetworkGateway</span></span>
<span data-ttu-id="f3287-120">Gibt einen Objektverweis auf das Gateway für virtuelle Netzwerke an, das die zu entfernende Standardwebsite enthält.</span><span class="sxs-lookup"><span data-stu-id="f3287-120">Specifies an object reference to the virtual network gateway containing the default site to be removed.</span></span>
<span data-ttu-id="f3287-121">Sie können einen Objektverweis auf ein virtuelles Netzwerkgateway erstellen, indem Sie Get-AzVirtualNetworkGateway und den Namen des Gateways angeben.</span><span class="sxs-lookup"><span data-stu-id="f3287-121">You can create an object reference to a virtual network gateway by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="f3287-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3287-122">CommonParameters</span></span>
<span data-ttu-id="f3287-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3287-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3287-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3287-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3287-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f3287-125">INPUTS</span></span>

### <span data-ttu-id="f3287-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f3287-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="f3287-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f3287-127">OUTPUTS</span></span>

### <span data-ttu-id="f3287-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f3287-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="f3287-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f3287-129">NOTES</span></span>

## <span data-ttu-id="f3287-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f3287-130">RELATED LINKS</span></span>

[<span data-ttu-id="f3287-131">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f3287-131">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="f3287-132">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="f3287-132">Set-AzVirtualNetworkGatewayDefaultSite</span></span>](./Set-AzVirtualNetworkGatewayDefaultSite.md)


