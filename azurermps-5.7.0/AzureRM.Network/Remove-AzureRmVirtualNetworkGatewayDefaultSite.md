---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 6ea456ca5e8d06c1ff732664127ca2e7a62abb2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503058"
---
# <span data-ttu-id="283c4-101">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="283c4-101">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="283c4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="283c4-102">SYNOPSIS</span></span>
<span data-ttu-id="283c4-103">Entfernt die Standardwebsite aus einem virtuellen Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="283c4-103">Removes the default site from a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="283c4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="283c4-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="283c4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="283c4-105">DESCRIPTION</span></span>
<span data-ttu-id="283c4-106">Das Cmdlet **Remove-AzureRmVirtualNetworkGatewayDefaultSite** entfernt die erzwungene Tunneling-Standardwebsite von einem virtuellen Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="283c4-106">The **Remove-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet removes the forced tunneling default site from a virtual network gateway.</span></span>
<span data-ttu-id="283c4-107">Erzwungener Tunneling bietet Ihnen eine Möglichkeit, den Internet gebundenen Datenverkehr von Azure Virtual Machines zu Ihrem lokalen Netzwerk umzuleiten. auf diese Weise können Sie den Datenverkehr prüfen und überwachen, bevor Sie ihn freigeben.</span><span class="sxs-lookup"><span data-stu-id="283c4-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="283c4-108">Erzwungener Tunneling wird mithilfe eines VPN-Tunnels (virtuelles privates Netzwerk) durchgeführt. Dieser Tunnel erfordert eine Standardwebsite, ein lokales Gateway, in dem der gesamte Azure Internet gebundene Datenverkehr umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="283c4-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>

<span data-ttu-id="283c4-109">**Remove-AzureRmVirtualNetworkGatewayDefaultSite** entfernt die Standardwebsite, die einem Gateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="283c4-109">**Remove-AzureRmVirtualNetworkGatewayDefaultSite** removes the default site assigned to a gateway.</span></span>
<span data-ttu-id="283c4-110">In diesem Fall müssen Sie Set-AzureRmVirtualNetworkGatewayDefaultSite verwenden, um eine neue Standardwebsite zuzuweisen, bevor das Gateway für erzwungenen Tunneln verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="283c4-110">If you do this you will need to use Set-AzureRmVirtualNetworkGatewayDefaultSite to assign a new default site before the gateway can be used for forced tunneling.</span></span>

## <span data-ttu-id="283c4-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="283c4-111">EXAMPLES</span></span>

### <span data-ttu-id="283c4-112">Beispiel 1: Entfernen der Standardwebsite, die einem virtuellen Netzwerkgateway zugewiesen ist</span><span class="sxs-lookup"><span data-stu-id="283c4-112">Example 1: Remove the default site assigned to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworknGateway $Gateway
```

<span data-ttu-id="283c4-113">In diesem Beispiel wird die Standardwebsite entfernt, die derzeit einem virtuellen Netzwerkgateway mit dem Namen ContosoVirtualGateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="283c4-113">This example removes the default site currently assigned to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="283c4-114">Der erste Befehl verwendet " **Get-AzureRmVirtualNetworkGateway** ", um einen Objektverweis auf das Gateway zu erstellen. dieser Objektverweis wird in einer Variablen mit dem Namen $Gateway gespeichert.</span><span class="sxs-lookup"><span data-stu-id="283c4-114">The first command uses **Get-AzureRmVirtualNetworkGateway** to create an object reference to the gateway; this object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="283c4-115">Der zweite Befehl verwendet dann **Remove-AzureRmVirtualNetworkGatewayDefaultSite** , um die dem Gateway zugewiesene Standardwebsite zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="283c4-115">The second command then uses **Remove-AzureRmVirtualNetworkGatewayDefaultSite** to remove the default site assigned to that gateway.</span></span>

## <span data-ttu-id="283c4-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="283c4-116">PARAMETERS</span></span>

### <span data-ttu-id="283c4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="283c4-117">-DefaultProfile</span></span>
<span data-ttu-id="283c4-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="283c4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="283c4-119">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="283c4-119">-VirtualNetworkGateway</span></span>
<span data-ttu-id="283c4-120">Gibt einen Objektverweis auf das virtuelle Netzwerkgateway an, das die zu entfernende Standardwebsite enthält.</span><span class="sxs-lookup"><span data-stu-id="283c4-120">Specifies an object reference to the virtual network gateway containing the default site to be removed.</span></span>
<span data-ttu-id="283c4-121">Sie können einen Objektverweis auf ein virtuelles Netzwerkgateway erstellen, indem Sie den Get-AzureRmVirtualNetworkGateway verwenden und den Namen des Gateways angeben.</span><span class="sxs-lookup"><span data-stu-id="283c4-121">You can create an object reference to a virtual network gateway by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="283c4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="283c4-122">CommonParameters</span></span>
<span data-ttu-id="283c4-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="283c4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="283c4-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="283c4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="283c4-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="283c4-125">INPUTS</span></span>

###  
<span data-ttu-id="283c4-126">Dieses Cmdlet akzeptiert Pipelineinstanzen des **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="283c4-126">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="283c4-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="283c4-127">OUTPUTS</span></span>

###  
<span data-ttu-id="283c4-128">Dieses Cmdlet ändert vorhandene Instanzen des **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="283c4-128">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="283c4-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="283c4-129">NOTES</span></span>

## <span data-ttu-id="283c4-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="283c4-130">RELATED LINKS</span></span>

[<span data-ttu-id="283c4-131">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="283c4-131">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="283c4-132">Satz-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="283c4-132">Set-AzureRmVirtualNetworkGatewayDefaultSite</span></span>](./Set-AzureRmVirtualNetworkGatewayDefaultSite.md)


