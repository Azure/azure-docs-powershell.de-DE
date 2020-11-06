---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 0c05800bc72af7b6158b2adeaccc92255d7ae4af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481102"
---
# <span data-ttu-id="7fe72-101">Set-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="7fe72-101">Set-AzureRmVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="7fe72-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7fe72-102">SYNOPSIS</span></span>
<span data-ttu-id="7fe72-103">Legt die Standardwebsite für ein virtuelles Netzwerkgateway fest.</span><span class="sxs-lookup"><span data-stu-id="7fe72-103">Sets the default site for a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fe72-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7fe72-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fe72-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7fe72-105">DESCRIPTION</span></span>
<span data-ttu-id="7fe72-106">Das Cmdlet " **festlegen-AzureRmVirtualNetworkGatewayDefaultSite** " weist einem virtuellen Netzwerkgateway eine erzwungene Tunneling-Standardwebsite zu.</span><span class="sxs-lookup"><span data-stu-id="7fe72-106">The **Set-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet assigns a forced tunneling default site to a virtual network gateway.</span></span>
<span data-ttu-id="7fe72-107">Erzwungener Tunneling bietet Ihnen eine Möglichkeit, den Internet gebundenen Datenverkehr von Azure Virtual Machines zu Ihrem lokalen Netzwerk umzuleiten. auf diese Weise können Sie den Datenverkehr prüfen und überwachen, bevor Sie ihn freigeben.</span><span class="sxs-lookup"><span data-stu-id="7fe72-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="7fe72-108">Erzwungener Tunneling wird mithilfe eines VPN-Tunnels (virtuelles privates Netzwerk) durchgeführt. Dieser Tunnel erfordert eine Standardwebsite, ein lokales Gateway, in dem der gesamte Azure Internet gebundene Datenverkehr umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="7fe72-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="7fe72-109">" **AzureRmVirtualNetworkGatewayDefaultSite** " bietet eine Möglichkeit zum Ändern der Standardwebsite, die einem Gateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7fe72-109">**Set-AzureRmVirtualNetworkGatewayDefaultSite** provides a way to change the default site assigned to a gateway.</span></span>

## <span data-ttu-id="7fe72-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7fe72-110">EXAMPLES</span></span>

### <span data-ttu-id="7fe72-111">Beispiel 1: Zuweisen einer Standardwebsite zu einem virtuellen Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="7fe72-111">Example 1: Assign a default site to a virtual network gateway</span></span>
```
PS C:\>$LocalGateway = Get-AzureRmLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

<span data-ttu-id="7fe72-112">In diesem Beispiel wird einem virtuellen Netzwerkgateway mit dem Namen ContosoVirtualGateway eine Standardwebsite zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="7fe72-112">This example assigns a default site to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="7fe72-113">Der erste Befehl erstellt einen Objektverweis auf ein lokales Gateway mit dem Namen ContosoLocalGateway.</span><span class="sxs-lookup"><span data-stu-id="7fe72-113">The first command creates an object reference to a local gateway named ContosoLocalGateway.</span></span>
<span data-ttu-id="7fe72-114">Dieser Objektverweis, der in der Variablen mit dem Namen $LocalGateway gespeichert ist, stellt das Gateway dar, das als Standardwebsite konfiguriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7fe72-114">This object reference that is stored in the variable named $LocalGateway represents the gateway to be configured as the default site</span></span>

<span data-ttu-id="7fe72-115">.</span><span class="sxs-lookup"><span data-stu-id="7fe72-115">.</span></span>
<span data-ttu-id="7fe72-116">Der zweite Befehl erstellt dann einen Objektverweis auf das virtuelle Netzwerkgateway und speichert das Ergebnis in der Variablen mit dem Namen $VirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="7fe72-116">The second command then creates an object reference to the virtual network gateway and stores the result in the variable named $VirtualGateway.</span></span>

<span data-ttu-id="7fe72-117">Der dritte Befehl verwendet das Cmdlet " **Satz-AzureRmVirtualNetworkGatewayDefaultSite** ", um die Standardwebsite ContosoVirtualGateway zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="7fe72-117">The third command uses the **Set-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet to assign the default site to ContosoVirtualGateway.</span></span>

## <span data-ttu-id="7fe72-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="7fe72-118">PARAMETERS</span></span>

### <span data-ttu-id="7fe72-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fe72-119">-DefaultProfile</span></span>
<span data-ttu-id="7fe72-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7fe72-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fe72-121">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="7fe72-121">-GatewayDefaultSite</span></span>
<span data-ttu-id="7fe72-122">Gibt einen Objektverweis auf das lokale Netzwerkgateway an, der als Standardwebsite für das angegebene virtuelle Netzwerk zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7fe72-122">Specifies an object reference to the local network gateway to be assigned as the default site for the specified virtual network.</span></span>
<span data-ttu-id="7fe72-123">Sie können das Get-AzureRmLocalNetworkGateway-Cmdlet verwenden, um einen Objektverweis auf ein lokales Gateway zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7fe72-123">You can use the Get-AzureRmLocalNetworkGateway cmdlet to create an object reference to a local gateway.</span></span>

```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fe72-124">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7fe72-124">-VirtualNetworkGateway</span></span>
<span data-ttu-id="7fe72-125">Gibt einen Objektverweis auf das virtuelle Netzwerkgateway an, dem die Standardwebsite zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7fe72-125">Specifies an object reference to the virtual network gateway where the default site will be assigned.</span></span>
<span data-ttu-id="7fe72-126">Sie können einen Objektverweis auf ein virtuelles Netzwerkgateway erstellen, indem Sie den **Get-AzureRmVirtualNetworkGateway** verwenden und den Namen des Gateways angeben.</span><span class="sxs-lookup"><span data-stu-id="7fe72-126">You can create an object reference to a virtual network gateway by using the **Get-AzureRmVirtualNetworkGateway** and specifying the name of the gateway.</span></span>

<span data-ttu-id="7fe72-127">Die Variable $VirtualGateway kann dann als Parameterwert für den *VirtualNetworkGateway* -Parameter verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="7fe72-127">The variable $VirtualGateway can then be used as the parameter value for the *VirtualNetworkGateway* parameter:</span></span>

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

### <span data-ttu-id="7fe72-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fe72-128">CommonParameters</span></span>
<span data-ttu-id="7fe72-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fe72-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fe72-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fe72-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fe72-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7fe72-131">INPUTS</span></span>

###  
<span data-ttu-id="7fe72-132">Dieses Cmdlet akzeptiert Pipelineinstanzen des **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="7fe72-132">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="7fe72-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7fe72-133">OUTPUTS</span></span>

###  
<span data-ttu-id="7fe72-134">Dieses Cmdlet ändert vorhandene Instanzen des **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="7fe72-134">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="7fe72-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="7fe72-135">NOTES</span></span>

## <span data-ttu-id="7fe72-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7fe72-136">RELATED LINKS</span></span>

[<span data-ttu-id="7fe72-137">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7fe72-137">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="7fe72-138">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7fe72-138">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="7fe72-139">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="7fe72-139">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span></span>](./Remove-AzureRmVirtualNetworkGatewayDefaultSite.md)


