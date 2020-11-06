---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C868DFA4-8A9D-4108-B88B-ACD7F100A63C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteConfig.md
ms.openlocfilehash: 7b28c50cfc53fee03d5715697a88e9356ea7664b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501758"
---
# <span data-ttu-id="fce0d-101">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="fce0d-101">Add-AzureRmRouteConfig</span></span>

## <span data-ttu-id="fce0d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fce0d-102">SYNOPSIS</span></span>
<span data-ttu-id="fce0d-103">Fügt eine Route zu einer Routentabelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="fce0d-103">Adds a route to a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fce0d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fce0d-104">SYNTAX</span></span>

```
Add-AzureRmRouteConfig -Name <String> -RouteTable <PSRouteTable> [-AddressPrefix <String>]
 -NextHopType <String> [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fce0d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fce0d-105">DESCRIPTION</span></span>
<span data-ttu-id="fce0d-106">Mit dem Cmdlet **Add-AzureRmRouteConfig** wird eine Route zu einer Azure Route-Tabelle hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fce0d-106">The **Add-AzureRmRouteConfig** cmdlet adds a route to an Azure route table.</span></span>

## <span data-ttu-id="fce0d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fce0d-107">EXAMPLES</span></span>

### <span data-ttu-id="fce0d-108">Beispiel 1: Hinzufügen einer Route zu einer Routentabelle</span><span class="sxs-lookup"><span data-stu-id="fce0d-108">Example 1: Add a route to a route table</span></span>
```
PS C:\>$RouteTable = Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
PS C:\> Add-AzureRmRouteConfig -Name "Route13" -AddressPrefix 10.3.0.0/16 -NextHopType "VnetLocal" -RouteTable $RouteTable
```

<span data-ttu-id="fce0d-109">Der erste Befehl ruft mithilfe des Get-AzureRmRouteTable-Cmdlets eine Routingtabelle mit dem Namen RouteTable01 ab.</span><span class="sxs-lookup"><span data-stu-id="fce0d-109">The first command gets a route table named RouteTable01 by using the Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="fce0d-110">Der Befehl speichert die Tabelle in der $RouteTable-Variablen.</span><span class="sxs-lookup"><span data-stu-id="fce0d-110">The command stores the table in the $RouteTable variable.</span></span>

<span data-ttu-id="fce0d-111">Mit dem zweiten Befehl wird eine Route mit dem Namen Route13 zu der in $RouteTable gespeicherten Routentabelle hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fce0d-111">The second command adds a route named Route13 to the route table stored in $RouteTable.</span></span>
<span data-ttu-id="fce0d-112">Diese Route leitet Pakete an das lokale virtuelle Netzwerk weiter.</span><span class="sxs-lookup"><span data-stu-id="fce0d-112">This route forwards packets to the local virtual network.</span></span>

### <span data-ttu-id="fce0d-113">Beispiel 2: Hinzufügen einer Route zu einer Routentabelle mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="fce0d-113">Example 2: Add a route to a route table by using the pipeline</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzureRmRouteConfig -Name "Route02" -AddressPrefix 10.2.0.0/16 -NextHopType VnetLocal | Set-AzureRmRouteTable
Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable01
Etag              : W/"f13e1bc8-d41f-44d0-882d-b8b5a1134f59"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route02",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route02",
                        "AddressPrefix": "10.2.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route13",
                        "Etag": null, 
                        "Id": null, 
                        "AddressPrefix": "10.3.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": null
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="fce0d-114">Dieser Befehl ruft die Routingtabelle mit dem Namen RouteTable01 mithilfe von **Get-AzureRmRouteTable**.</span><span class="sxs-lookup"><span data-stu-id="fce0d-114">This command gets the route table named RouteTable01 by using **Get-AzureRmRouteTable**.</span></span>
<span data-ttu-id="fce0d-115">Der Befehl übergibt diese Tabelle mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fce0d-115">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fce0d-116">Das aktuelle Cmdlet fügt die Route mit dem Namen "Route02" hinzu und übergibt dann das Ergebnis an das Cmdlet "AzureRmRouteTable", das die Tabelle so aktualisiert, dass die Änderungen wieder **gegeben** werden.</span><span class="sxs-lookup"><span data-stu-id="fce0d-116">The current cmdlet adds the route named Route02, and then passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="fce0d-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="fce0d-117">PARAMETERS</span></span>

### <span data-ttu-id="fce0d-118">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="fce0d-118">-AddressPrefix</span></span>
<span data-ttu-id="fce0d-119">Gibt das Ziel im CIDR-Format (klassenlos InterDomain Routing) an, auf das die Route angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="fce0d-119">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="fce0d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="fce0d-120">-Name</span></span>
<span data-ttu-id="fce0d-121">Gibt den Namen der Route an, die der Route-Tabelle hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fce0d-121">Specifies a name of the route to add to the route table.</span></span>

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

### <span data-ttu-id="fce0d-122">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="fce0d-122">-NextHopIpAddress</span></span>
<span data-ttu-id="fce0d-123">Gibt die IP-Adresse einer virtuellen Appliance an, die Sie Ihrem virtuellen Azure-Netzwerk hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="fce0d-123">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="fce0d-124">Diese Route leitet Pakete an diese Adresse weiter.</span><span class="sxs-lookup"><span data-stu-id="fce0d-124">This route forwards packets to that address.</span></span>
<span data-ttu-id="fce0d-125">Geben Sie diesen Parameter nur an, wenn Sie einen Wert von VirtualAppliance für den *NextHopType* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="fce0d-125">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="fce0d-126">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="fce0d-126">-NextHopType</span></span>
<span data-ttu-id="fce0d-127">Gibt an, wie Pakete von dieser Route weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="fce0d-127">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="fce0d-128">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="fce0d-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fce0d-129">Internet.</span><span class="sxs-lookup"><span data-stu-id="fce0d-129">Internet.</span></span>
<span data-ttu-id="fce0d-130">Das standardmäßige Internet Gateway, das von Azure bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="fce0d-130">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="fce0d-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="fce0d-131">None.</span></span>
<span data-ttu-id="fce0d-132">Wenn Sie diesen Wert angeben, leitet die Route keine Pakete weiter.</span><span class="sxs-lookup"><span data-stu-id="fce0d-132">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="fce0d-133">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="fce0d-133">VirtualAppliance.</span></span>
<span data-ttu-id="fce0d-134">Eine virtuelle Appliance, die Sie Ihrem virtuellen Azure-Netzwerk hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="fce0d-134">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="fce0d-135">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="fce0d-135">VirtualNetworkGateway.</span></span>
<span data-ttu-id="fce0d-136">Ein Azure Server-zu-Server-virtuelles privates Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="fce0d-136">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="fce0d-137">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="fce0d-137">VnetLocal.</span></span>
<span data-ttu-id="fce0d-138">Lokales virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="fce0d-138">The local virtual network.</span></span>
<span data-ttu-id="fce0d-139">Wenn Sie über zwei Subnetze (10.1.0.0/16 und 10.2.0.0/16) im gleichen virtuellen Netzwerk verfügen, wählen Sie den Wert VnetLocal für jedes Subnetz aus, um es an das andere Subnetz weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="fce0d-139">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="fce0d-140">-Routel</span><span class="sxs-lookup"><span data-stu-id="fce0d-140">-RouteTable</span></span>
<span data-ttu-id="fce0d-141">Gibt die Routingtabelle an, der das Cmdlet eine Route hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="fce0d-141">Specifies the route table to which this cmdlet adds a route.</span></span>

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

### <span data-ttu-id="fce0d-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fce0d-142">-DefaultProfile</span></span>
<span data-ttu-id="fce0d-143">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fce0d-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fce0d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fce0d-144">CommonParameters</span></span>
<span data-ttu-id="fce0d-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fce0d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fce0d-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fce0d-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fce0d-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fce0d-147">INPUTS</span></span>

### <span data-ttu-id="fce0d-148">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="fce0d-148">PSRouteTable</span></span>
<span data-ttu-id="fce0d-149">Der Parameter "routeable" akzeptiert den Wert vom Typ "PSRouteTable" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="fce0d-149">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="fce0d-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fce0d-150">OUTPUTS</span></span>

### <span data-ttu-id="fce0d-151">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="fce0d-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="fce0d-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="fce0d-152">NOTES</span></span>

## <span data-ttu-id="fce0d-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fce0d-153">RELATED LINKS</span></span>

[<span data-ttu-id="fce0d-154">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="fce0d-154">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="fce0d-155">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="fce0d-155">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="fce0d-156">Neu – AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="fce0d-156">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="fce0d-157">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="fce0d-157">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="fce0d-158">Satz-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="fce0d-158">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)

[<span data-ttu-id="fce0d-159">Satz-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="fce0d-159">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


