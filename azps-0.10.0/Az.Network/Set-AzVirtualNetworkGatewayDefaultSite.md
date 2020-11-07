---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 560053ca6b5e49ffcef8dbb6ee4b0ba32f3ed276
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843567"
---
# <span data-ttu-id="47ab2-101">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="47ab2-101">Set-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="47ab2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="47ab2-102">SYNOPSIS</span></span>
<span data-ttu-id="47ab2-103">Legt die Standardwebsite für ein virtuelles Netzwerkgateway fest.</span><span class="sxs-lookup"><span data-stu-id="47ab2-103">Sets the default site for a virtual network gateway.</span></span>

## <span data-ttu-id="47ab2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="47ab2-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47ab2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47ab2-105">DESCRIPTION</span></span>
<span data-ttu-id="47ab2-106">Das Cmdlet " **festlegen-AzVirtualNetworkGatewayDefaultSite** " weist einem virtuellen Netzwerkgateway eine erzwungene Tunneling-Standardwebsite zu.</span><span class="sxs-lookup"><span data-stu-id="47ab2-106">The **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet assigns a forced tunneling default site to a virtual network gateway.</span></span>
<span data-ttu-id="47ab2-107">Erzwungener Tunneling bietet Ihnen eine Möglichkeit, den Internet gebundenen Datenverkehr von Azure Virtual Machines zu Ihrem lokalen Netzwerk umzuleiten. auf diese Weise können Sie den Datenverkehr prüfen und überwachen, bevor Sie ihn freigeben.</span><span class="sxs-lookup"><span data-stu-id="47ab2-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="47ab2-108">Erzwungener Tunneling wird mithilfe eines VPN-Tunnels (virtuelles privates Netzwerk) durchgeführt. Dieser Tunnel erfordert eine Standardwebsite, ein lokales Gateway, in dem der gesamte Azure Internet gebundene Datenverkehr umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="47ab2-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="47ab2-109">" **AzVirtualNetworkGatewayDefaultSite** " bietet eine Möglichkeit zum Ändern der Standardwebsite, die einem Gateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="47ab2-109">**Set-AzVirtualNetworkGatewayDefaultSite** provides a way to change the default site assigned to a gateway.</span></span>

## <span data-ttu-id="47ab2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="47ab2-110">EXAMPLES</span></span>

### <span data-ttu-id="47ab2-111">Beispiel 1: Zuweisen einer Standardwebsite zu einem virtuellen Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="47ab2-111">Example 1: Assign a default site to a virtual network gateway</span></span>
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

<span data-ttu-id="47ab2-112">In diesem Beispiel wird einem virtuellen Netzwerkgateway mit dem Namen ContosoVirtualGateway eine Standardwebsite zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="47ab2-112">This example assigns a default site to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="47ab2-113">Der erste Befehl erstellt einen Objektverweis auf ein lokales Gateway mit dem Namen ContosoLocalGateway.</span><span class="sxs-lookup"><span data-stu-id="47ab2-113">The first command creates an object reference to a local gateway named ContosoLocalGateway.</span></span>
<span data-ttu-id="47ab2-114">Dieser Objektverweis, der in der Variablen mit dem Namen $LocalGateway gespeichert ist, stellt das Gateway dar, das als Standardwebsite konfiguriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="47ab2-114">This object reference that is stored in the variable named $LocalGateway represents the gateway to be configured as the default site</span></span>

<span data-ttu-id="47ab2-115">.</span><span class="sxs-lookup"><span data-stu-id="47ab2-115">.</span></span>
<span data-ttu-id="47ab2-116">Der zweite Befehl erstellt dann einen Objektverweis auf das virtuelle Netzwerkgateway und speichert das Ergebnis in der Variablen mit dem Namen $VirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="47ab2-116">The second command then creates an object reference to the virtual network gateway and stores the result in the variable named $VirtualGateway.</span></span>

<span data-ttu-id="47ab2-117">Der dritte Befehl verwendet das Cmdlet " **Satz-AzVirtualNetworkGatewayDefaultSite** ", um die Standardwebsite ContosoVirtualGateway zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="47ab2-117">The third command uses the **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet to assign the default site to ContosoVirtualGateway.</span></span>

## <span data-ttu-id="47ab2-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="47ab2-118">PARAMETERS</span></span>

### <span data-ttu-id="47ab2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47ab2-119">-DefaultProfile</span></span>
<span data-ttu-id="47ab2-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="47ab2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47ab2-121">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="47ab2-121">-GatewayDefaultSite</span></span>
<span data-ttu-id="47ab2-122">Gibt einen Objektverweis auf das lokale Netzwerkgateway an, der als Standardwebsite für das angegebene virtuelle Netzwerk zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="47ab2-122">Specifies an object reference to the local network gateway to be assigned as the default site for the specified virtual network.</span></span>
<span data-ttu-id="47ab2-123">Sie können das Get-AzLocalNetworkGateway-Cmdlet verwenden, um einen Objektverweis auf ein lokales Gateway zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="47ab2-123">You can use the Get-AzLocalNetworkGateway cmdlet to create an object reference to a local gateway.</span></span>

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

### <span data-ttu-id="47ab2-124">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="47ab2-124">-VirtualNetworkGateway</span></span>
<span data-ttu-id="47ab2-125">Gibt einen Objektverweis auf das virtuelle Netzwerkgateway an, dem die Standardwebsite zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="47ab2-125">Specifies an object reference to the virtual network gateway where the default site will be assigned.</span></span>
<span data-ttu-id="47ab2-126">Sie können einen Objektverweis auf ein virtuelles Netzwerkgateway erstellen, indem Sie den **Get-AzVirtualNetworkGateway** verwenden und den Namen des Gateways angeben.</span><span class="sxs-lookup"><span data-stu-id="47ab2-126">You can create an object reference to a virtual network gateway by using the **Get-AzVirtualNetworkGateway** and specifying the name of the gateway.</span></span>

<span data-ttu-id="47ab2-127">Die Variable $VirtualGateway kann dann als Parameterwert für den *VirtualNetworkGateway* -Parameter verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="47ab2-127">The variable $VirtualGateway can then be used as the parameter value for the *VirtualNetworkGateway* parameter:</span></span>

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

### <span data-ttu-id="47ab2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47ab2-128">CommonParameters</span></span>
<span data-ttu-id="47ab2-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47ab2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47ab2-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47ab2-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47ab2-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="47ab2-131">INPUTS</span></span>

###  
<span data-ttu-id="47ab2-132">Dieses Cmdlet akzeptiert Pipelineinstanzen des **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="47ab2-132">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="47ab2-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="47ab2-133">OUTPUTS</span></span>

###  
<span data-ttu-id="47ab2-134">Dieses Cmdlet ändert vorhandene Instanzen des **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="47ab2-134">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="47ab2-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="47ab2-135">NOTES</span></span>

## <span data-ttu-id="47ab2-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="47ab2-136">RELATED LINKS</span></span>

[<span data-ttu-id="47ab2-137">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="47ab2-137">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="47ab2-138">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="47ab2-138">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="47ab2-139">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="47ab2-139">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


