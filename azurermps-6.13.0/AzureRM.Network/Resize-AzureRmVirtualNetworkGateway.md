---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/resize-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 0a8a5c4084813bac74ea907575d2bd26c3d8c5f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503481"
---
# <span data-ttu-id="ac9f6-101">Resize-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ac9f6-101">Resize-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="ac9f6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ac9f6-102">SYNOPSIS</span></span>
<span data-ttu-id="ac9f6-103">Ändert die Größe eines vorhandenen virtuellen Netzwerkgateways.</span><span class="sxs-lookup"><span data-stu-id="ac9f6-103">Resizes an existing virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac9f6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac9f6-104">SYNTAX</span></span>

```
Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac9f6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ac9f6-105">DESCRIPTION</span></span>
<span data-ttu-id="ac9f6-106">Mit dem Cmdlet **size-AzureRmVirtualNetworkGateway** können Sie die Lagerhaltungs Einheit (SKU) für ein virtuelles Netzwerkgateway ändern.</span><span class="sxs-lookup"><span data-stu-id="ac9f6-106">The **Resize-AzureRmVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="ac9f6-107">SKUs ermitteln die Funktionen eines Gateways, beispielsweise den Durchsatz und die maximal zulässige Anzahl von IP-Tunneln.</span><span class="sxs-lookup"><span data-stu-id="ac9f6-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="ac9f6-108">Azure unterstützt Basis-, Standard-, Hochleistungs-, VpnGw1-, VpnGw2-, VpnGw3-, VpnGw1AZ-, VpnGw2AZ-, VpnGw3AZ-, ErGw1AZ-, ErGw2AZ-SKUs (manchmal auch als kleine, mittlere und große SKUs bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="ac9f6-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="ac9f6-109">Ausführliche Informationen zu den Funktionen der einzelnen SKU-Typen finden Sie unter https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .</span><span class="sxs-lookup"><span data-stu-id="ac9f6-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>
<span data-ttu-id="ac9f6-110">Beachten Sie, dass sich die SKUs in der Preis-und Leistungsfähigkeit unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="ac9f6-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="ac9f6-111">Weitere Informationen finden Sie unter https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .</span><span class="sxs-lookup"><span data-stu-id="ac9f6-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="ac9f6-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ac9f6-112">EXAMPLES</span></span>

### <span data-ttu-id="ac9f6-113">Beispiel 1: Ändern der Größe eines virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="ac9f6-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="ac9f6-114">In diesem Beispiel wird die Größe eines virtuellen Netzwerkgateways mit dem Namen ContosoVirtualGateway geändert.</span><span class="sxs-lookup"><span data-stu-id="ac9f6-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="ac9f6-115">Der erste Befehl erstellt einen Objektverweis auf ContosoVirtualGateway; dieser Objektverweis wird in einer Variablen mit dem Namen $Gateway gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ac9f6-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="ac9f6-116">Der zweite Befehl verwendet dann das Cmdlet **size-AzureRmVirtualNetworkGateway** , um die *GatewaySku* -Eigenschaft auf Basic zu setzen.</span><span class="sxs-lookup"><span data-stu-id="ac9f6-116">The second command then uses the **Resize-AzureRmVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="ac9f6-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac9f6-117">PARAMETERS</span></span>

### <span data-ttu-id="ac9f6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac9f6-118">-DefaultProfile</span></span>
<span data-ttu-id="ac9f6-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ac9f6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac9f6-120">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="ac9f6-120">-GatewaySku</span></span>
<span data-ttu-id="ac9f6-121">Gibt den neuen Typ der Gateway-SKU an.</span><span class="sxs-lookup"><span data-stu-id="ac9f6-121">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="ac9f6-122">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ac9f6-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ac9f6-123">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="ac9f6-123">Basic</span></span>
- <span data-ttu-id="ac9f6-124">Standard</span><span class="sxs-lookup"><span data-stu-id="ac9f6-124">Standard</span></span>
- <span data-ttu-id="ac9f6-125">Höchstleistung</span><span class="sxs-lookup"><span data-stu-id="ac9f6-125">High Performance</span></span>
- <span data-ttu-id="ac9f6-126">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="ac9f6-126">VpnGw1</span></span>
- <span data-ttu-id="ac9f6-127">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="ac9f6-127">VpnGw2</span></span>
- <span data-ttu-id="ac9f6-128">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="ac9f6-128">VpnGw3</span></span>
- <span data-ttu-id="ac9f6-129">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="ac9f6-129">VpnGw1AZ</span></span> 
- <span data-ttu-id="ac9f6-130">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="ac9f6-130">VpnGw2AZ</span></span> 
- <span data-ttu-id="ac9f6-131">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="ac9f6-131">VpnGw3AZ</span></span> 
- <span data-ttu-id="ac9f6-132">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="ac9f6-132">ErGw1AZ</span></span> 
- <span data-ttu-id="ac9f6-133">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="ac9f6-133">ErGw2AZ</span></span> 
- <span data-ttu-id="ac9f6-134">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="ac9f6-134">ErGw3AZ</span></span> 

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

### <span data-ttu-id="ac9f6-135">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ac9f6-135">-VirtualNetworkGateway</span></span>
<span data-ttu-id="ac9f6-136">Gibt einen Objektverweis auf das virtuelle Netzwerkgateway an, dessen Größe geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ac9f6-136">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="ac9f6-137">Sie können diesen Objektverweis mithilfe der Get-AzureRmVirtualNetworkGateway erstellen und den Namen des Gateways angeben.</span><span class="sxs-lookup"><span data-stu-id="ac9f6-137">You can create this object reference by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="ac9f6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac9f6-138">CommonParameters</span></span>
<span data-ttu-id="ac9f6-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac9f6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac9f6-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac9f6-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac9f6-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ac9f6-141">INPUTS</span></span>

### <span data-ttu-id="ac9f6-142">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ac9f6-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="ac9f6-143">Parameter: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ac9f6-143">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="ac9f6-144">System. String</span><span class="sxs-lookup"><span data-stu-id="ac9f6-144">System.String</span></span>

## <span data-ttu-id="ac9f6-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ac9f6-145">OUTPUTS</span></span>

### <span data-ttu-id="ac9f6-146">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ac9f6-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="ac9f6-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="ac9f6-147">NOTES</span></span>
<span data-ttu-id="ac9f6-148">Sie können die Größe nicht von Basic/Standard/Performance-SKUs auf die neue VpnGw1/VpnGw2/VpnGw3-SKUs ändern.</span><span class="sxs-lookup"><span data-stu-id="ac9f6-148">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="ac9f6-149">Eine weitere Größenänderung ist von/zu VpnGw1AZ/VpnGw2AZ/VpnGw3AZ oder ErGw1AZ/ErGw2AZ/ErGw3AZ nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="ac9f6-149">Further resize is not allowed from/to VpnGw1AZ/VpnGw2AZ/VpnGw3AZ or ErGw1AZ/ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="ac9f6-150">Die Größe ist nur innerhalb der SKU-Serie zulässig, z. b. VpnGw1AZ kann in/aus VpnGw2AZ/VpnGw3AZ geändert werden, und ErGw1AZ kann in/aus ErGw2AZ/ErGw3AZ geändert werden.</span><span class="sxs-lookup"><span data-stu-id="ac9f6-150">Resize is allowed only within the SKU 'series' e.g VpnGw1AZ can be resized to/from VpnGw2AZ/VpnGw3AZ and ErGw1AZ can be resized to/from ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="ac9f6-151">Anweisungen hierzu finden Sie unter https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways .</span><span class="sxs-lookup"><span data-stu-id="ac9f6-151">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="ac9f6-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ac9f6-152">RELATED LINKS</span></span>

[<span data-ttu-id="ac9f6-153">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="ac9f6-153">Get-AzureRmVpnClientPackage</span></span>](./Get-AzureRmVpnClientPackage.md)

[<span data-ttu-id="ac9f6-154">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ac9f6-154">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="ac9f6-155">Satz-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="ac9f6-155">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


