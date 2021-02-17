---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: 31ec0453b0ce64c27d1bb37d4bf6c0f100a8c760
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405141"
---
# <span data-ttu-id="f535b-101">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f535b-101">Resize-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="f535b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f535b-102">SYNOPSIS</span></span>
<span data-ttu-id="f535b-103">Ändert die Größe eines vorhandenen virtuellen Netzwerkgateways.</span><span class="sxs-lookup"><span data-stu-id="f535b-103">Resizes an existing virtual network gateway.</span></span>

## <span data-ttu-id="f535b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f535b-104">SYNTAX</span></span>

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f535b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f535b-105">DESCRIPTION</span></span>
<span data-ttu-id="f535b-106">Mit **dem Cmdlet Resize-AzVirtualNetworkGateway** können Sie die SKU (Stock-Keeping Unit) für ein virtuelles Netzwerkgateway ändern.</span><span class="sxs-lookup"><span data-stu-id="f535b-106">The **Resize-AzVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="f535b-107">SKUs bestimmen die Funktionen eines Gateways, z. B. Durchsatz und die maximale Anzahl zulässiger IP-Tunnel.</span><span class="sxs-lookup"><span data-stu-id="f535b-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="f535b-108">Azure unterstützt Basic, Standard, High-Performance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKUs (manchmal auch als kleine, mittlere und große SKUs bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="f535b-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="f535b-109">Ausführliche Informationen zu den Funktionen der einzelnen SKU-Typen finden Sie unter https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .</span><span class="sxs-lookup"><span data-stu-id="f535b-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>
<span data-ttu-id="f535b-110">Bedenken Sie, dass skUs in der Preisgestaltung sowie in den Funktionen unterschiedlich sind.</span><span class="sxs-lookup"><span data-stu-id="f535b-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="f535b-111">Weitere Informationen finden Sie unter https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .</span><span class="sxs-lookup"><span data-stu-id="f535b-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="f535b-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f535b-112">EXAMPLES</span></span>

### <span data-ttu-id="f535b-113">Beispiel 1: Ändern der Größe eines virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="f535b-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="f535b-114">In diesem Beispiel wird die Größe eines virtuellen Netzwerkgateways namens "ContosoVirtualGateway" geändert.</span><span class="sxs-lookup"><span data-stu-id="f535b-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="f535b-115">Der erste Befehl erstellt einen Objektverweis auf ContosoVirtualGateway. objektverweis wird in einer Variablen mit dem Namen $Gateway.</span><span class="sxs-lookup"><span data-stu-id="f535b-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="f535b-116">Der zweite Befehl verwendet dann das **Cmdlet Resize-AzVirtualNetworkGateway,** um die *Eigenschaft "GatewaySku"* auf "Basic" zu setzen.</span><span class="sxs-lookup"><span data-stu-id="f535b-116">The second command then uses the **Resize-AzVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="f535b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f535b-117">PARAMETERS</span></span>

### <span data-ttu-id="f535b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f535b-118">-DefaultProfile</span></span>
<span data-ttu-id="f535b-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f535b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f535b-120">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="f535b-120">-GatewaySku</span></span>
<span data-ttu-id="f535b-121">Gibt den neuen Typ der Gateway-SKU an.</span><span class="sxs-lookup"><span data-stu-id="f535b-121">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="f535b-122">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="f535b-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f535b-123">Standard</span><span class="sxs-lookup"><span data-stu-id="f535b-123">Basic</span></span>
- <span data-ttu-id="f535b-124">Standard</span><span class="sxs-lookup"><span data-stu-id="f535b-124">Standard</span></span>
- <span data-ttu-id="f535b-125">Hohe Leistung</span><span class="sxs-lookup"><span data-stu-id="f535b-125">High Performance</span></span>
- <span data-ttu-id="f535b-126">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="f535b-126">VpnGw1</span></span>
- <span data-ttu-id="f535b-127">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="f535b-127">VpnGw2</span></span>
- <span data-ttu-id="f535b-128">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="f535b-128">VpnGw3</span></span>
- <span data-ttu-id="f535b-129">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="f535b-129">VpnGw1AZ</span></span> 
- <span data-ttu-id="f535b-130">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="f535b-130">VpnGw2AZ</span></span> 
- <span data-ttu-id="f535b-131">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="f535b-131">VpnGw3AZ</span></span> 
- <span data-ttu-id="f535b-132">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="f535b-132">ErGw1AZ</span></span> 
- <span data-ttu-id="f535b-133">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="f535b-133">ErGw2AZ</span></span> 
- <span data-ttu-id="f535b-134">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="f535b-134">ErGw3AZ</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f535b-135">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f535b-135">-VirtualNetworkGateway</span></span>
<span data-ttu-id="f535b-136">Gibt einen Objektverweis auf das virtuelle Netzwerkgateway an, dessen Größe geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f535b-136">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="f535b-137">Sie können diesen Objektverweis erstellen, indem Sie Get-AzVirtualNetworkGateway und den Namen des Gateways angeben.</span><span class="sxs-lookup"><span data-stu-id="f535b-137">You can create this object reference by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="f535b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f535b-138">CommonParameters</span></span>
<span data-ttu-id="f535b-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f535b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f535b-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f535b-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f535b-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f535b-141">INPUTS</span></span>

### <span data-ttu-id="f535b-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f535b-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="f535b-143">System.String</span><span class="sxs-lookup"><span data-stu-id="f535b-143">System.String</span></span>

## <span data-ttu-id="f535b-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f535b-144">OUTPUTS</span></span>

### <span data-ttu-id="f535b-145">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f535b-145">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="f535b-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f535b-146">NOTES</span></span>
<span data-ttu-id="f535b-147">Sie können die Größe nicht von Basic/Standard/HighPerformance-SKUs auf die neuen VPNGw1/VpnGw2/VpnGw3-SKUs ändern.</span><span class="sxs-lookup"><span data-stu-id="f535b-147">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="f535b-148">Eine weitere Größenänderung ist von/zu VpnGw1AZ/VpnGw2AZ/VpnGw3AZ oder ErGw1AZ/ErGw2AZ/ErGw3AZ nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="f535b-148">Further resize is not allowed from/to VpnGw1AZ/VpnGw2AZ/VpnGw3AZ or ErGw1AZ/ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="f535b-149">Die Größenänderung ist nur in der SKU-Serie zulässig, z. B. kann die Größe von VpnGw1AZ in VpnGw2AZ/VpnGw3AZ und von ErGw1AZ in/von ErGw2AZ/ErGw3AZ geändert werden.</span><span class="sxs-lookup"><span data-stu-id="f535b-149">Resize is allowed only within the SKU 'series' e.g VpnGw1AZ can be resized to/from VpnGw2AZ/VpnGw3AZ and ErGw1AZ can be resized to/from ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="f535b-150">Anweisungen https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways finden Sie hier.</span><span class="sxs-lookup"><span data-stu-id="f535b-150">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="f535b-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f535b-151">RELATED LINKS</span></span>

[<span data-ttu-id="f535b-152">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f535b-152">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="f535b-153">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f535b-153">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="f535b-154">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f535b-154">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="f535b-155">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f535b-155">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="f535b-156">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f535b-156">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)

[<span data-ttu-id="f535b-157">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="f535b-157">Get-AzVpnClientPackage</span></span>](./Get-AzVpnClientPackage.md)

