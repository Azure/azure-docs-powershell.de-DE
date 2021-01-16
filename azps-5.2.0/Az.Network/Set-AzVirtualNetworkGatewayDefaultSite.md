---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: a4be0aed365517e1ae3ae11155f82ea097db309a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293621"
---
# <span data-ttu-id="ef547-101">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="ef547-101">Set-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="ef547-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef547-102">SYNOPSIS</span></span>
<span data-ttu-id="ef547-103">Legt die Standardwebsite für ein virtuelles Netzwerkgateway fest.</span><span class="sxs-lookup"><span data-stu-id="ef547-103">Sets the default site for a virtual network gateway.</span></span>

## <span data-ttu-id="ef547-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef547-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef547-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef547-105">DESCRIPTION</span></span>
<span data-ttu-id="ef547-106">Das **Cmdlet "Set-AzVirtualNetworkGatewayDefaultSite"** weist einem virtuellen Netzwerkgateway eine Standardwebsite für erzwungenes Tunneln zu.</span><span class="sxs-lookup"><span data-stu-id="ef547-106">The **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet assigns a forced tunneling default site to a virtual network gateway.</span></span>
<span data-ttu-id="ef547-107">Erzwungenes Tunneln bietet Ihnen die Möglichkeit, internetgebundenen Datenverkehr von virtuellen #A0 an Ihr lokales Netzwerk umzuleiten. auf diese Weise können Sie den Datenverkehr prüfen und überwachen, bevor Sie ihn freigeben.</span><span class="sxs-lookup"><span data-stu-id="ef547-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="ef547-108">Erzwungenes Tunneln wird mithilfe eines VPN (Virtual Private Network)-Tunnels durchgeführt. dieser Tunnel erfordert eine Standardwebsite, also ein lokales Gateway, an das der internetgebundene Azure-Datenverkehr umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="ef547-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="ef547-109">**Set-AzVirtualNetworkGatewayDefaultSite** bietet eine Möglichkeit, die einem Gateway zugewiesene Standardwebsite zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ef547-109">**Set-AzVirtualNetworkGatewayDefaultSite** provides a way to change the default site assigned to a gateway.</span></span>

## <span data-ttu-id="ef547-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ef547-110">EXAMPLES</span></span>

### <span data-ttu-id="ef547-111">Beispiel 1: Zuweisen einer Standardwebsite zu einem virtuellen Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="ef547-111">Example 1: Assign a default site to a virtual network gateway</span></span>
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

<span data-ttu-id="ef547-112">In diesem Beispiel wird eine Standardwebsite einem virtuellen Netzwerkgateway namens "ContosoVirtualGateway" zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="ef547-112">This example assigns a default site to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="ef547-113">Der erste Befehl erstellt einen Objektverweis auf ein lokales Gateway namens "ContosoLocalGateway".</span><span class="sxs-lookup"><span data-stu-id="ef547-113">The first command creates an object reference to a local gateway named ContosoLocalGateway.</span></span>
<span data-ttu-id="ef547-114">Dieser Objektverweis, der in der Variablen namens $LocalGateway gespeichert wird, stellt das Gateway dar, das als Standardwebsite konfiguriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ef547-114">This object reference that is stored in the variable named $LocalGateway represents the gateway to be configured as the default site .</span></span>
<span data-ttu-id="ef547-115">Der zweite Befehl erstellt dann einen Objektverweis auf das virtuelle Netzwerkgateway und speichert das Ergebnis in der Variablen namens $VirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="ef547-115">The second command then creates an object reference to the virtual network gateway and stores the result in the variable named $VirtualGateway.</span></span>
<span data-ttu-id="ef547-116">Der dritte Befehl verwendet das **Cmdlet "Set-AzVirtualNetworkGatewayDefaultSite",** um "ContosoVirtualGateway" die Standardwebsite zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="ef547-116">The third command uses the **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet to assign the default site to ContosoVirtualGateway.</span></span>

## <span data-ttu-id="ef547-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef547-117">PARAMETERS</span></span>

### <span data-ttu-id="ef547-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef547-118">-DefaultProfile</span></span>
<span data-ttu-id="ef547-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef547-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef547-120">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="ef547-120">-GatewayDefaultSite</span></span>
<span data-ttu-id="ef547-121">Gibt einen Objektverweis auf das lokale Netzwerkgateway an, das als Standardwebsite für das angegebene virtuelle Netzwerk zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ef547-121">Specifies an object reference to the local network gateway to be assigned as the default site for the specified virtual network.</span></span>
<span data-ttu-id="ef547-122">Sie können das cmdlet Get-AzLocalNetworkGateway erstellen, um einen Objektverweis auf ein lokales Gateway zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ef547-122">You can use the Get-AzLocalNetworkGateway cmdlet to create an object reference to a local gateway.</span></span>

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

### <span data-ttu-id="ef547-123">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ef547-123">-VirtualNetworkGateway</span></span>
<span data-ttu-id="ef547-124">Gibt einen Objektverweis auf das virtuelle Netzwerkgateway an, dem die Standardwebsite zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ef547-124">Specifies an object reference to the virtual network gateway where the default site will be assigned.</span></span>
<span data-ttu-id="ef547-125">Sie können einen Objektverweis auf ein virtuelles Netzwerkgateway erstellen, indem Sie **das Get-AzVirtualNetworkGateway verwenden** und den Namen des Gateways angeben.</span><span class="sxs-lookup"><span data-stu-id="ef547-125">You can create an object reference to a virtual network gateway by using the **Get-AzVirtualNetworkGateway** and specifying the name of the gateway.</span></span>
<span data-ttu-id="ef547-126">Die variable $VirtualGateway kann dann als Parameterwert für den *Parameter VirtualNetworkGateway verwendet* werden:</span><span class="sxs-lookup"><span data-stu-id="ef547-126">The variable $VirtualGateway can then be used as the parameter value for the *VirtualNetworkGateway* parameter:</span></span>

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

### <span data-ttu-id="ef547-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef547-127">CommonParameters</span></span>
<span data-ttu-id="ef547-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef547-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef547-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef547-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef547-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ef547-130">INPUTS</span></span>

### <span data-ttu-id="ef547-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ef547-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="ef547-132">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ef547-132">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="ef547-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ef547-133">OUTPUTS</span></span>

### <span data-ttu-id="ef547-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ef547-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="ef547-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ef547-135">NOTES</span></span>

## <span data-ttu-id="ef547-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ef547-136">RELATED LINKS</span></span>

[<span data-ttu-id="ef547-137">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ef547-137">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="ef547-138">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ef547-138">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="ef547-139">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="ef547-139">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


