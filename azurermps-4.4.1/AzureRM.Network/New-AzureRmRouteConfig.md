---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteConfig.md
ms.openlocfilehash: bb51d5bfb1ccc81aa10c7aecc4d7a255fc0f60d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481885"
---
# <span data-ttu-id="6098b-101">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="6098b-101">New-AzureRmRouteConfig</span></span>

## <span data-ttu-id="6098b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6098b-102">SYNOPSIS</span></span>
<span data-ttu-id="6098b-103">Erstellt eine Route für eine Routentabelle.</span><span class="sxs-lookup"><span data-stu-id="6098b-103">Creates a route for a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6098b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6098b-104">SYNTAX</span></span>

```
New-AzureRmRouteConfig -Name <String> [-AddressPrefix <String>] -NextHopType <String>
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6098b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6098b-105">DESCRIPTION</span></span>
<span data-ttu-id="6098b-106">Das Cmdlet **New-AzureRmRouteConfig** erstellt eine Route für eine Azure Route-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6098b-106">The **New-AzureRmRouteConfig** cmdlet creates a route for an Azure route table.</span></span>

## <span data-ttu-id="6098b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6098b-107">EXAMPLES</span></span>

### <span data-ttu-id="6098b-108">Beispiel 1: Erstellen einer Route</span><span class="sxs-lookup"><span data-stu-id="6098b-108">Example 1: Create a route</span></span>
```
PS C:\>$Route = New-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> $Route
Name              : Route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="6098b-109">Der erste Befehl erstellt eine Route mit dem Namen Route07 und speichert Sie dann in der $Route-Variablen.</span><span class="sxs-lookup"><span data-stu-id="6098b-109">The first command creates a route named Route07, and then stores it in the $Route variable.</span></span>
<span data-ttu-id="6098b-110">Diese Route leitet Pakete an das lokale virtuelle Netzwerk weiter.</span><span class="sxs-lookup"><span data-stu-id="6098b-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="6098b-111">Mit dem zweiten Befehl werden die Eigenschaften der Route angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6098b-111">The second command displays the properties of the route.</span></span>

## <span data-ttu-id="6098b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6098b-112">PARAMETERS</span></span>

### <span data-ttu-id="6098b-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="6098b-113">-AddressPrefix</span></span>
<span data-ttu-id="6098b-114">Gibt das Ziel im CIDR-Format (klassenlos InterDomain Routing) an, auf das die Route angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="6098b-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6098b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="6098b-115">-Name</span></span>
<span data-ttu-id="6098b-116">Gibt einen Namen für die Route an.</span><span class="sxs-lookup"><span data-stu-id="6098b-116">Specifies a name for the route.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6098b-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="6098b-117">-NextHopIpAddress</span></span>
<span data-ttu-id="6098b-118">Gibt die IP-Adresse einer virtuellen Appliance an, die Sie Ihrem Azurevirtual-Netzwerk hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6098b-118">Specifies the IP address of a virtual appliance that you add to your Azurevirtual network.</span></span>
<span data-ttu-id="6098b-119">Diese Route leitet Pakete an diese Adresse weiter.</span><span class="sxs-lookup"><span data-stu-id="6098b-119">This route forwards packets to that address.</span></span>
<span data-ttu-id="6098b-120">Geben Sie diesen Parameter nur an, wenn Sie einen Wert von VirtualAppliance für den *NextHopType* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="6098b-120">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6098b-121">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="6098b-121">-NextHopType</span></span>
<span data-ttu-id="6098b-122">Gibt an, wie Pakete von dieser Route weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="6098b-122">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="6098b-123">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6098b-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6098b-124">Internet.</span><span class="sxs-lookup"><span data-stu-id="6098b-124">Internet.</span></span>
<span data-ttu-id="6098b-125">Das standardmäßige Internet Gateway, das von Azure bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6098b-125">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="6098b-126">Keine.</span><span class="sxs-lookup"><span data-stu-id="6098b-126">None.</span></span>
<span data-ttu-id="6098b-127">Wenn Sie diesen Wert angeben, leitet die Route keine Pakete weiter.</span><span class="sxs-lookup"><span data-stu-id="6098b-127">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="6098b-128">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="6098b-128">VirtualAppliance.</span></span>
<span data-ttu-id="6098b-129">Eine virtuelle Appliance, die Sie Ihrem virtuellen Azure-Netzwerk hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6098b-129">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="6098b-130">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="6098b-130">VirtualNetworkGateway.</span></span>
<span data-ttu-id="6098b-131">Ein Azure Server-zu-Server-virtuelles privates Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="6098b-131">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="6098b-132">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="6098b-132">VnetLocal.</span></span>
<span data-ttu-id="6098b-133">Lokales virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="6098b-133">The local virtual network.</span></span>
<span data-ttu-id="6098b-134">Wenn Sie über zwei Subnetze (10.1.0.0/16 und 10.2.0.0/16) im gleichen virtuellen Netzwerk verfügen, wählen Sie den Wert VnetLocal für jedes Subnetz aus, um es an das andere Subnetz weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="6098b-134">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Internet, None, VirtualAppliance, VirtualNetworkGateway, VnetLocal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6098b-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6098b-135">-DefaultProfile</span></span>
<span data-ttu-id="6098b-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6098b-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6098b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6098b-137">CommonParameters</span></span>
<span data-ttu-id="6098b-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6098b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6098b-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6098b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6098b-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6098b-140">INPUTS</span></span>

## <span data-ttu-id="6098b-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6098b-141">OUTPUTS</span></span>

### <span data-ttu-id="6098b-142">Microsoft. Azure. Commands. Network. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="6098b-142">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="6098b-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="6098b-143">NOTES</span></span>

## <span data-ttu-id="6098b-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6098b-144">RELATED LINKS</span></span>

[<span data-ttu-id="6098b-145">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="6098b-145">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="6098b-146">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="6098b-146">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="6098b-147">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="6098b-147">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="6098b-148">Satz-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="6098b-148">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


