---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 8e35347813849badfa50100cc4cac418e2d66332
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932336"
---
# <span data-ttu-id="94236-101">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="94236-101">Set-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="94236-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94236-102">SYNOPSIS</span></span>
<span data-ttu-id="94236-103">Legt die Standardwebsite für ein Virtuelles Netzwerkgateway fest.</span><span class="sxs-lookup"><span data-stu-id="94236-103">Sets the default site for a virtual network gateway.</span></span>

## <span data-ttu-id="94236-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="94236-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94236-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="94236-105">DESCRIPTION</span></span>
<span data-ttu-id="94236-106">Das **Cmdlet Set-AzVirtualNetworkGatewayDefaultSite** weist einem Gateway des virtuellen Netzwerks eine Standardwebsite für erzwungenes Tunneln zu.</span><span class="sxs-lookup"><span data-stu-id="94236-106">The **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet assigns a forced tunneling default site to a virtual network gateway.</span></span>
<span data-ttu-id="94236-107">Erzwungenes Tunneln bietet Ihnen die Möglichkeit, internetgebundenen Datenverkehr von virtuellen #A0 an Ihr lokales Netzwerk umzuleiten. Auf diese Weise können Sie den Datenverkehr prüfen und überwachen, bevor Sie ihn freigeben.</span><span class="sxs-lookup"><span data-stu-id="94236-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="94236-108">Erzwungenes Tunneln wird mithilfe eines VPN-Tunnels (Virtual Private Network) ausgeführt. Für diesen Tunnel ist eine Standardwebsite erforderlich, ein lokales Gateway, auf dem der internetgebundene Azure-Datenverkehr umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="94236-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="94236-109">**Set-AzVirtualNetworkGatewayDefaultSite** bietet eine Möglichkeit zum Ändern der Standardwebsite, die einem Gateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="94236-109">**Set-AzVirtualNetworkGatewayDefaultSite** provides a way to change the default site assigned to a gateway.</span></span>

## <span data-ttu-id="94236-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="94236-110">EXAMPLES</span></span>

### <span data-ttu-id="94236-111">Beispiel 1: Zuweisen einer Standardwebsite zu einem Gateway für virtuelle Netzwerke</span><span class="sxs-lookup"><span data-stu-id="94236-111">Example 1: Assign a default site to a virtual network gateway</span></span>
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

<span data-ttu-id="94236-112">In diesem Beispiel wird einem Virtuellen Netzwerkgateway namens ContosoVirtualGateway eine Standardwebsite zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="94236-112">This example assigns a default site to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="94236-113">Mit dem ersten Befehl wird ein Objektverweis auf ein lokales Gateway namens ContosoLocalGateway erstellt.</span><span class="sxs-lookup"><span data-stu-id="94236-113">The first command creates an object reference to a local gateway named ContosoLocalGateway.</span></span>
<span data-ttu-id="94236-114">Dieser Objektverweis, der in der Variablen namens $LocalGateway ist, stellt das Gateway dar, das als Standardwebsite konfiguriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="94236-114">This object reference that is stored in the variable named $LocalGateway represents the gateway to be configured as the default site .</span></span>
<span data-ttu-id="94236-115">Der zweite Befehl erstellt dann einen Objektverweis auf das Virtuelle Netzwerkgateway und speichert das Ergebnis in der Variablen namens $VirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="94236-115">The second command then creates an object reference to the virtual network gateway and stores the result in the variable named $VirtualGateway.</span></span>
<span data-ttu-id="94236-116">Der dritte Befehl verwendet das **Cmdlet Set-AzVirtualNetworkGatewayDefaultSite,** um contosoVirtualGateway die Standardwebsite zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="94236-116">The third command uses the **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet to assign the default site to ContosoVirtualGateway.</span></span>

## <span data-ttu-id="94236-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="94236-117">PARAMETERS</span></span>

### <span data-ttu-id="94236-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94236-118">-DefaultProfile</span></span>
<span data-ttu-id="94236-119">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="94236-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94236-120">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="94236-120">-GatewayDefaultSite</span></span>
<span data-ttu-id="94236-121">Gibt einen Objektverweis auf das lokale Netzwerkgateway an, das als Standardwebsite für das angegebene virtuelle Netzwerk zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="94236-121">Specifies an object reference to the local network gateway to be assigned as the default site for the specified virtual network.</span></span>
<span data-ttu-id="94236-122">Sie können das cmdlet Get-AzLocalNetworkGateway verwenden, um einen Objektverweis auf ein lokales Gateway zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="94236-122">You can use the Get-AzLocalNetworkGateway cmdlet to create an object reference to a local gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94236-123">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="94236-123">-VirtualNetworkGateway</span></span>
<span data-ttu-id="94236-124">Gibt einen Objektverweis auf das Virtuelle Netzwerkgateway an, dem die Standardwebsite zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="94236-124">Specifies an object reference to the virtual network gateway where the default site will be assigned.</span></span>
<span data-ttu-id="94236-125">Sie können einen Objektverweis auf ein virtuelles Netzwerkgateway erstellen, indem Sie **das Get-AzVirtualNetworkGateway** verwenden und den Namen des Gateways angeben.</span><span class="sxs-lookup"><span data-stu-id="94236-125">You can create an object reference to a virtual network gateway by using the **Get-AzVirtualNetworkGateway** and specifying the name of the gateway.</span></span>
<span data-ttu-id="94236-126">Die Variable $VirtualGateway kann dann als Parameterwert für den *VirtualNetworkGateway-Parameter verwendet* werden:</span><span class="sxs-lookup"><span data-stu-id="94236-126">The variable $VirtualGateway can then be used as the parameter value for the *VirtualNetworkGateway* parameter:</span></span>

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

### <span data-ttu-id="94236-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94236-127">CommonParameters</span></span>
<span data-ttu-id="94236-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94236-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94236-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94236-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94236-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="94236-130">INPUTS</span></span>

### <span data-ttu-id="94236-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="94236-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="94236-132">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="94236-132">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="94236-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="94236-133">OUTPUTS</span></span>

### <span data-ttu-id="94236-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="94236-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="94236-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="94236-135">NOTES</span></span>

## <span data-ttu-id="94236-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="94236-136">RELATED LINKS</span></span>

[<span data-ttu-id="94236-137">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="94236-137">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="94236-138">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="94236-138">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="94236-139">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="94236-139">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


