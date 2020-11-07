---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermrouteconfig
schema: 2.0.0
ms.openlocfilehash: ab528e837f6f2e45db5e68430d973e0d8f019850
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850379"
---
# <span data-ttu-id="52172-101">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="52172-101">New-AzureRmRouteConfig</span></span>

## <span data-ttu-id="52172-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="52172-102">SYNOPSIS</span></span>
<span data-ttu-id="52172-103">Erstellt eine Route für eine Routentabelle.</span><span class="sxs-lookup"><span data-stu-id="52172-103">Creates a route for a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52172-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="52172-104">SYNTAX</span></span>

```
New-AzureRmRouteConfig [-AddressPrefix <String>] [-NextHopType <String>] [-NextHopIpAddress <String>]
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52172-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="52172-105">DESCRIPTION</span></span>
<span data-ttu-id="52172-106">Das Cmdlet **New-AzureRmRouteConfig** erstellt eine Route für eine Azure Route-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="52172-106">The **New-AzureRmRouteConfig** cmdlet creates a route for an Azure route table.</span></span>

## <span data-ttu-id="52172-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="52172-107">EXAMPLES</span></span>

### <span data-ttu-id="52172-108">Beispiel 1: Erstellen einer Route</span><span class="sxs-lookup"><span data-stu-id="52172-108">Example 1: Create a route</span></span>
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

<span data-ttu-id="52172-109">Der erste Befehl erstellt eine Route mit dem Namen Route07 und speichert Sie dann in der $Route-Variablen.</span><span class="sxs-lookup"><span data-stu-id="52172-109">The first command creates a route named Route07, and then stores it in the $Route variable.</span></span>
<span data-ttu-id="52172-110">Diese Route leitet Pakete an das lokale virtuelle Netzwerk weiter.</span><span class="sxs-lookup"><span data-stu-id="52172-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="52172-111">Mit dem zweiten Befehl werden die Eigenschaften der Route angezeigt.</span><span class="sxs-lookup"><span data-stu-id="52172-111">The second command displays the properties of the route.</span></span>

## <span data-ttu-id="52172-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="52172-112">PARAMETERS</span></span>

### <span data-ttu-id="52172-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="52172-113">-AddressPrefix</span></span>
<span data-ttu-id="52172-114">Gibt das Ziel im CIDR-Format (klassenlos InterDomain Routing) an, auf das die Route angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="52172-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52172-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52172-115">-DefaultProfile</span></span>
<span data-ttu-id="52172-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="52172-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52172-117">-Name</span><span class="sxs-lookup"><span data-stu-id="52172-117">-Name</span></span>
<span data-ttu-id="52172-118">Gibt einen Namen für die Route an.</span><span class="sxs-lookup"><span data-stu-id="52172-118">Specifies a name for the route.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52172-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="52172-119">-NextHopIpAddress</span></span>
<span data-ttu-id="52172-120">Gibt die IP-Adresse einer virtuellen Appliance an, die Sie Ihrem Azurevirtual-Netzwerk hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="52172-120">Specifies the IP address of a virtual appliance that you add to your Azurevirtual network.</span></span>
<span data-ttu-id="52172-121">Diese Route leitet Pakete an diese Adresse weiter.</span><span class="sxs-lookup"><span data-stu-id="52172-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="52172-122">Geben Sie diesen Parameter nur an, wenn Sie einen Wert von VirtualAppliance für den *NextHopType* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="52172-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52172-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="52172-123">-NextHopType</span></span>
<span data-ttu-id="52172-124">Gibt an, wie Pakete von dieser Route weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="52172-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="52172-125">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="52172-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="52172-126">Internet.</span><span class="sxs-lookup"><span data-stu-id="52172-126">Internet.</span></span>
<span data-ttu-id="52172-127">Das standardmäßige Internet Gateway, das von Azure bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="52172-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="52172-128">Keine.</span><span class="sxs-lookup"><span data-stu-id="52172-128">None.</span></span>
<span data-ttu-id="52172-129">Wenn Sie diesen Wert angeben, leitet die Route keine Pakete weiter.</span><span class="sxs-lookup"><span data-stu-id="52172-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="52172-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="52172-130">VirtualAppliance.</span></span>
<span data-ttu-id="52172-131">Eine virtuelle Appliance, die Sie Ihrem virtuellen Azure-Netzwerk hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="52172-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="52172-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="52172-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="52172-133">Ein Azure Server-zu-Server-virtuelles privates Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="52172-133">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="52172-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="52172-134">VnetLocal.</span></span>
<span data-ttu-id="52172-135">Lokales virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="52172-135">The local virtual network.</span></span>
<span data-ttu-id="52172-136">Wenn Sie über zwei Subnetze (10.1.0.0/16 und 10.2.0.0/16) im gleichen virtuellen Netzwerk verfügen, wählen Sie den Wert VnetLocal für jedes Subnetz aus, um es an das andere Subnetz weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="52172-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52172-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="52172-137">-Confirm</span></span>
<span data-ttu-id="52172-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="52172-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52172-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52172-139">-WhatIf</span></span>
<span data-ttu-id="52172-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="52172-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52172-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="52172-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52172-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52172-142">CommonParameters</span></span>
<span data-ttu-id="52172-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52172-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52172-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52172-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52172-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="52172-145">INPUTS</span></span>

## <span data-ttu-id="52172-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="52172-146">OUTPUTS</span></span>

### <span data-ttu-id="52172-147">Microsoft. Azure. Commands. Network. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="52172-147">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="52172-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="52172-148">NOTES</span></span>

## <span data-ttu-id="52172-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="52172-149">RELATED LINKS</span></span>

[<span data-ttu-id="52172-150">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="52172-150">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="52172-151">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="52172-151">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="52172-152">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="52172-152">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="52172-153">Satz-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="52172-153">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


