---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/resize-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 0a3dea2b706f7efcdc76b48175df225e2974728c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850596"
---
# <span data-ttu-id="0cf28-101">Resize-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0cf28-101">Resize-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="0cf28-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0cf28-102">SYNOPSIS</span></span>
<span data-ttu-id="0cf28-103">Ändert die Größe eines vorhandenen virtuellen Netzwerkgateways.</span><span class="sxs-lookup"><span data-stu-id="0cf28-103">Resizes an existing virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0cf28-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0cf28-104">SYNTAX</span></span>

```
Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cf28-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0cf28-105">DESCRIPTION</span></span>
<span data-ttu-id="0cf28-106">Mit dem Cmdlet **size-AzureRmVirtualNetworkGateway** können Sie die Lagerhaltungs Einheit (SKU) für ein virtuelles Netzwerkgateway ändern.</span><span class="sxs-lookup"><span data-stu-id="0cf28-106">The **Resize-AzureRmVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="0cf28-107">SKUs ermitteln die Funktionen eines Gateways, beispielsweise den Durchsatz und die maximal zulässige Anzahl von IP-Tunneln.</span><span class="sxs-lookup"><span data-stu-id="0cf28-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="0cf28-108">Azure unterstützt Basis-, Standard-, Hochleistungs-, VpnGw1-, VpnGw2-und VpnGw3-SKUs (manchmal auch als kleine, mittlere und große SKUs bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="0cf28-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2 and VpnGw3 SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="0cf28-109">Ausführliche Informationen zu den Funktionen der einzelnen SKU-Typen finden Sie unter https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .</span><span class="sxs-lookup"><span data-stu-id="0cf28-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>

<span data-ttu-id="0cf28-110">Beachten Sie, dass sich die SKUs in der Preis-und Leistungsfähigkeit unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="0cf28-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="0cf28-111">Weitere Informationen finden Sie unter https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .</span><span class="sxs-lookup"><span data-stu-id="0cf28-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="0cf28-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0cf28-112">EXAMPLES</span></span>

### <span data-ttu-id="0cf28-113">Beispiel 1: Ändern der Größe eines virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="0cf28-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="0cf28-114">In diesem Beispiel wird die Größe eines virtuellen Netzwerkgateways mit dem Namen ContosoVirtualGateway geändert.</span><span class="sxs-lookup"><span data-stu-id="0cf28-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="0cf28-115">Der erste Befehl erstellt einen Objektverweis auf ContosoVirtualGateway; dieser Objektverweis wird in einer Variablen mit dem Namen $Gateway gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0cf28-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="0cf28-116">Der zweite Befehl verwendet dann das Cmdlet **size-AzureRmVirtualNetworkGateway** , um die *GatewaySku* -Eigenschaft auf Basic zu setzen.</span><span class="sxs-lookup"><span data-stu-id="0cf28-116">The second command then uses the **Resize-AzureRmVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="0cf28-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="0cf28-117">PARAMETERS</span></span>

### <span data-ttu-id="0cf28-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cf28-118">-DefaultProfile</span></span>
<span data-ttu-id="0cf28-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0cf28-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cf28-120">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="0cf28-120">-GatewaySku</span></span>
<span data-ttu-id="0cf28-121">Gibt den neuen Typ der Gateway-SKU an.</span><span class="sxs-lookup"><span data-stu-id="0cf28-121">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="0cf28-122">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0cf28-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0cf28-123">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="0cf28-123">Basic</span></span>
- <span data-ttu-id="0cf28-124">Standard</span><span class="sxs-lookup"><span data-stu-id="0cf28-124">Standard</span></span>
- <span data-ttu-id="0cf28-125">Höchstleistung</span><span class="sxs-lookup"><span data-stu-id="0cf28-125">High Performance</span></span>
- <span data-ttu-id="0cf28-126">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="0cf28-126">VpnGw1</span></span>
- <span data-ttu-id="0cf28-127">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="0cf28-127">VpnGw2</span></span>
- <span data-ttu-id="0cf28-128">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="0cf28-128">VpnGw3</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cf28-129">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0cf28-129">-VirtualNetworkGateway</span></span>
<span data-ttu-id="0cf28-130">Gibt einen Objektverweis auf das virtuelle Netzwerkgateway an, dessen Größe geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0cf28-130">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="0cf28-131">Sie können diesen Objektverweis mithilfe der Get-AzureRmVirtualNetworkGateway erstellen und den Namen des Gateways angeben.</span><span class="sxs-lookup"><span data-stu-id="0cf28-131">You can create this object reference by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0cf28-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cf28-132">CommonParameters</span></span>
<span data-ttu-id="0cf28-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cf28-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cf28-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cf28-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cf28-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0cf28-135">INPUTS</span></span>

###  
<span data-ttu-id="0cf28-136">Dieses Cmdlet akzeptiert Pipelineinstanzen des **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="0cf28-136">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="0cf28-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0cf28-137">OUTPUTS</span></span>

###  
<span data-ttu-id="0cf28-138">Dieses Cmdlet ändert vorhandene Instanzen des **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="0cf28-138">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="0cf28-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="0cf28-139">NOTES</span></span>
<span data-ttu-id="0cf28-140">Sie können die Größe nicht von Basic/Standard/Performance-SKUs auf die neue VpnGw1/VpnGw2/VpnGw3-SKUs ändern.</span><span class="sxs-lookup"><span data-stu-id="0cf28-140">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="0cf28-141">Anweisungen hierzu finden Sie unter https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways .</span><span class="sxs-lookup"><span data-stu-id="0cf28-141">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="0cf28-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0cf28-142">RELATED LINKS</span></span>

[<span data-ttu-id="0cf28-143">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="0cf28-143">Get-AzureRmVpnClientPackage</span></span>](./Get-AzureRmVpnClientPackage.md)

[<span data-ttu-id="0cf28-144">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0cf28-144">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="0cf28-145">Satz-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="0cf28-145">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


