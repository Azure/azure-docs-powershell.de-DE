---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: bd42d7cec30b7d42dcb1cdb3657f6681bf2cb6b0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843723"
---
# <span data-ttu-id="f94ce-101">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f94ce-101">Resize-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="f94ce-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f94ce-102">SYNOPSIS</span></span>
<span data-ttu-id="f94ce-103">Ändert die Größe eines vorhandenen virtuellen Netzwerkgateways.</span><span class="sxs-lookup"><span data-stu-id="f94ce-103">Resizes an existing virtual network gateway.</span></span>

## <span data-ttu-id="f94ce-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f94ce-104">SYNTAX</span></span>

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f94ce-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f94ce-105">DESCRIPTION</span></span>
<span data-ttu-id="f94ce-106">Mit dem Cmdlet **size-AzVirtualNetworkGateway** können Sie die Lagerhaltungs Einheit (SKU) für ein virtuelles Netzwerkgateway ändern.</span><span class="sxs-lookup"><span data-stu-id="f94ce-106">The **Resize-AzVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="f94ce-107">SKUs ermitteln die Funktionen eines Gateways, beispielsweise den Durchsatz und die maximal zulässige Anzahl von IP-Tunneln.</span><span class="sxs-lookup"><span data-stu-id="f94ce-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="f94ce-108">Azure unterstützt Basis-, Standard-, Hochleistungs-, VpnGw1-, VpnGw2-und VpnGw3-SKUs (manchmal auch als kleine, mittlere und große SKUs bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="f94ce-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2 and VpnGw3 SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="f94ce-109">Ausführliche Informationen zu den Funktionen der einzelnen SKU-Typen finden Sie unter https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .</span><span class="sxs-lookup"><span data-stu-id="f94ce-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>

<span data-ttu-id="f94ce-110">Beachten Sie, dass sich die SKUs in der Preis-und Leistungsfähigkeit unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="f94ce-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="f94ce-111">Weitere Informationen finden Sie unter https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .</span><span class="sxs-lookup"><span data-stu-id="f94ce-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="f94ce-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f94ce-112">EXAMPLES</span></span>

### <span data-ttu-id="f94ce-113">Beispiel 1: Ändern der Größe eines virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="f94ce-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="f94ce-114">In diesem Beispiel wird die Größe eines virtuellen Netzwerkgateways mit dem Namen ContosoVirtualGateway geändert.</span><span class="sxs-lookup"><span data-stu-id="f94ce-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="f94ce-115">Der erste Befehl erstellt einen Objektverweis auf ContosoVirtualGateway; dieser Objektverweis wird in einer Variablen mit dem Namen $Gateway gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f94ce-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="f94ce-116">Der zweite Befehl verwendet dann das Cmdlet **size-AzVirtualNetworkGateway** , um die *GatewaySku* -Eigenschaft auf Basic zu setzen.</span><span class="sxs-lookup"><span data-stu-id="f94ce-116">The second command then uses the **Resize-AzVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="f94ce-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="f94ce-117">PARAMETERS</span></span>

### <span data-ttu-id="f94ce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f94ce-118">-DefaultProfile</span></span>
<span data-ttu-id="f94ce-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f94ce-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f94ce-120">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="f94ce-120">-GatewaySku</span></span>
<span data-ttu-id="f94ce-121">Gibt den neuen Typ der Gateway-SKU an.</span><span class="sxs-lookup"><span data-stu-id="f94ce-121">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="f94ce-122">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f94ce-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f94ce-123">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="f94ce-123">Basic</span></span>
- <span data-ttu-id="f94ce-124">Standard</span><span class="sxs-lookup"><span data-stu-id="f94ce-124">Standard</span></span>
- <span data-ttu-id="f94ce-125">Höchstleistung</span><span class="sxs-lookup"><span data-stu-id="f94ce-125">High Performance</span></span>
- <span data-ttu-id="f94ce-126">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="f94ce-126">VpnGw1</span></span>
- <span data-ttu-id="f94ce-127">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="f94ce-127">VpnGw2</span></span>
- <span data-ttu-id="f94ce-128">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="f94ce-128">VpnGw3</span></span>

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

### <span data-ttu-id="f94ce-129">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f94ce-129">-VirtualNetworkGateway</span></span>
<span data-ttu-id="f94ce-130">Gibt einen Objektverweis auf das virtuelle Netzwerkgateway an, dessen Größe geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f94ce-130">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="f94ce-131">Sie können diesen Objektverweis mithilfe der Get-AzVirtualNetworkGateway erstellen und den Namen des Gateways angeben.</span><span class="sxs-lookup"><span data-stu-id="f94ce-131">You can create this object reference by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="f94ce-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f94ce-132">CommonParameters</span></span>
<span data-ttu-id="f94ce-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f94ce-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f94ce-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f94ce-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f94ce-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f94ce-135">INPUTS</span></span>

###  
<span data-ttu-id="f94ce-136">Dieses Cmdlet akzeptiert Pipelineinstanzen des **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="f94ce-136">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="f94ce-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f94ce-137">OUTPUTS</span></span>

###  
<span data-ttu-id="f94ce-138">Dieses Cmdlet ändert vorhandene Instanzen des **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="f94ce-138">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="f94ce-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="f94ce-139">NOTES</span></span>
<span data-ttu-id="f94ce-140">Sie können die Größe nicht von Basic/Standard/Performance-SKUs auf die neue VpnGw1/VpnGw2/VpnGw3-SKUs ändern.</span><span class="sxs-lookup"><span data-stu-id="f94ce-140">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="f94ce-141">Anweisungen hierzu finden Sie unter https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways .</span><span class="sxs-lookup"><span data-stu-id="f94ce-141">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="f94ce-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f94ce-142">RELATED LINKS</span></span>

[<span data-ttu-id="f94ce-143">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="f94ce-143">Get-AzVpnClientPackage</span></span>](./Get-AzVpnClientPackage.md)

[<span data-ttu-id="f94ce-144">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f94ce-144">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="f94ce-145">Satz-AzVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="f94ce-145">Set-AzVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)


