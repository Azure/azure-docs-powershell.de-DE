---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6E967F9C-949E-4485-9B57-FC4F523D5DC9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteConfig.md
ms.openlocfilehash: a86e5346078bd1a8c9be924cdeac3b94fab907dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481822"
---
# <span data-ttu-id="93d2f-101">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="93d2f-101">Set-AzureRmRouteConfig</span></span>

## <span data-ttu-id="93d2f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="93d2f-102">SYNOPSIS</span></span>
<span data-ttu-id="93d2f-103">Legt den Zielstatus für eine Route fest.</span><span class="sxs-lookup"><span data-stu-id="93d2f-103">Sets the goal state for a route.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93d2f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="93d2f-104">SYNTAX</span></span>

```
Set-AzureRmRouteConfig -Name <String> -RouteTable <PSRouteTable> [-AddressPrefix <String>]
 -NextHopType <String> [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="93d2f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="93d2f-105">DESCRIPTION</span></span>
<span data-ttu-id="93d2f-106">Das Cmdlet " **Set-AzureRmRouteConfig** " legt den Zielstatus für eine Azure-Route fest.</span><span class="sxs-lookup"><span data-stu-id="93d2f-106">The **Set-AzureRmRouteConfig** cmdlet sets the goal state for an Azure route.</span></span>

## <span data-ttu-id="93d2f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="93d2f-107">EXAMPLES</span></span>

### <span data-ttu-id="93d2f-108">Beispiel 1: Ändern einer Route</span><span class="sxs-lookup"><span data-stu-id="93d2f-108">Example 1: Modify a route</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Set-AzureRmRouteConfig -Name "Route02" -AddressPrefix 10.4.0.0/16 -NextHopType VnetLocal | Set-AzureRmRouteTable
Name              : Routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"58c2922e-9efe-4554-a457-956ef44bc718"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"58c2922e-9efe-4554-a457-956ef44bc718\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/Routetable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route02",
                        "Etag": "W/\"58c2922e-9efe-4554-a457-956ef44bc718\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route02",
                        "AddressPrefix": "10.4.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="93d2f-109">Dieser Befehl ruft die Routingtabelle mit dem Namen RouteTable01 mithilfe des Get-AzureRmRouteTable-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="93d2f-109">This command gets the route table named RouteTable01 by using the Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="93d2f-110">Der Befehl übergibt diese Tabelle mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93d2f-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="93d2f-111">Das aktuelle Cmdlet ändert die Route mit dem Namen Route02 und übergibt dann das Ergebnis an das Cmdlet " **setAzureRmRouteTable** ", das die Tabelle so aktualisiert, dass die Änderungen wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="93d2f-111">The current cmdlet modifies the route named Route02, and then passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="93d2f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="93d2f-112">PARAMETERS</span></span>

### <span data-ttu-id="93d2f-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="93d2f-113">-AddressPrefix</span></span>
<span data-ttu-id="93d2f-114">Gibt das Ziel im CIDR-Format (klassenlos InterDomain Routing) an, auf das die Route angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="93d2f-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="93d2f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="93d2f-115">-Name</span></span>
<span data-ttu-id="93d2f-116">Gibt den Namen der Route an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="93d2f-116">Specifies the name of the route that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="93d2f-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="93d2f-117">-NextHopIpAddress</span></span>
<span data-ttu-id="93d2f-118">Gibt die IP-Adresse einer virtuellen Appliance an, die Sie Ihrem virtuellen Azure-Netzwerk hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="93d2f-118">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="93d2f-119">Diese Route leitet Pakete an diese Adresse weiter.</span><span class="sxs-lookup"><span data-stu-id="93d2f-119">This route forwards packets to that address.</span></span>
<span data-ttu-id="93d2f-120">Geben Sie diesen Parameter nur an, wenn Sie einen Wert von VirtualAppliance für den *NextHopType* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="93d2f-120">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="93d2f-121">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="93d2f-121">-NextHopType</span></span>
<span data-ttu-id="93d2f-122">Gibt an, wie Pakete von dieser Route weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="93d2f-122">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="93d2f-123">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="93d2f-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="93d2f-124">Internet.</span><span class="sxs-lookup"><span data-stu-id="93d2f-124">Internet.</span></span>
<span data-ttu-id="93d2f-125">Das standardmäßige Internet Gateway, das von Azure bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="93d2f-125">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="93d2f-126">Keine.</span><span class="sxs-lookup"><span data-stu-id="93d2f-126">None.</span></span>
<span data-ttu-id="93d2f-127">Wenn Sie diesen Wert angeben, leitet die Route keine Pakete weiter.</span><span class="sxs-lookup"><span data-stu-id="93d2f-127">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="93d2f-128">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="93d2f-128">VirtualAppliance.</span></span>
<span data-ttu-id="93d2f-129">Eine virtuelle Appliance, die Sie Ihrem virtuellen Azure-Netzwerk hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="93d2f-129">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="93d2f-130">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="93d2f-130">VirtualNetworkGateway.</span></span>
<span data-ttu-id="93d2f-131">Ein Azureserver-zu-Server-virtuelles privates Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="93d2f-131">An Azureserver-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="93d2f-132">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="93d2f-132">VnetLocal.</span></span>
<span data-ttu-id="93d2f-133">Lokales virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="93d2f-133">The local virtual network.</span></span>
<span data-ttu-id="93d2f-134">Wenn Sie über zwei Subnetze (10.1.0.0/16 und 10.2.0.0/16) im gleichen virtuellen Netzwerk verfügen, wählen Sie den Wert VnetLocal für jedes Subnetz aus, um es an das andere Subnetz weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="93d2f-134">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="93d2f-135">-Routel</span><span class="sxs-lookup"><span data-stu-id="93d2f-135">-RouteTable</span></span>
<span data-ttu-id="93d2f-136">Gibt die Routentabelle an, der diese Route zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="93d2f-136">Specifies the route table with which this route is associated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93d2f-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93d2f-137">-DefaultProfile</span></span>
<span data-ttu-id="93d2f-138">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="93d2f-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93d2f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93d2f-139">CommonParameters</span></span>
<span data-ttu-id="93d2f-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93d2f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93d2f-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93d2f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93d2f-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="93d2f-142">INPUTS</span></span>

### <span data-ttu-id="93d2f-143">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="93d2f-143">PSRouteTable</span></span>
<span data-ttu-id="93d2f-144">Der Parameter "routeable" akzeptiert den Wert vom Typ "PSRouteTable" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="93d2f-144">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="93d2f-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="93d2f-145">OUTPUTS</span></span>

### <span data-ttu-id="93d2f-146">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="93d2f-146">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="93d2f-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="93d2f-147">NOTES</span></span>

## <span data-ttu-id="93d2f-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="93d2f-148">RELATED LINKS</span></span>

[<span data-ttu-id="93d2f-149">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="93d2f-149">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="93d2f-150">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="93d2f-150">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="93d2f-151">Neu – AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="93d2f-151">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="93d2f-152">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="93d2f-152">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)


