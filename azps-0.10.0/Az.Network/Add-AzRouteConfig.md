---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C868DFA4-8A9D-4108-B88B-ACD7F100A63C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzRouteConfig.md
ms.openlocfilehash: 1afd855be89f83e9591bbd180b1357e1b03952eb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841803"
---
# <span data-ttu-id="deb01-101">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="deb01-101">Add-AzRouteConfig</span></span>

## <span data-ttu-id="deb01-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="deb01-102">SYNOPSIS</span></span>
<span data-ttu-id="deb01-103">Fügt eine Route zu einer Routentabelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="deb01-103">Adds a route to a route table.</span></span>

## <span data-ttu-id="deb01-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="deb01-104">SYNTAX</span></span>

```
Add-AzRouteConfig -RouteTable <PSRouteTable> [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="deb01-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="deb01-105">DESCRIPTION</span></span>
<span data-ttu-id="deb01-106">Mit dem Cmdlet **Add-AzRouteConfig** wird eine Route zu einer Azure Route-Tabelle hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="deb01-106">The **Add-AzRouteConfig** cmdlet adds a route to an Azure route table.</span></span>

## <span data-ttu-id="deb01-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="deb01-107">EXAMPLES</span></span>

### <span data-ttu-id="deb01-108">Beispiel 1: Hinzufügen einer Route zu einer Routentabelle</span><span class="sxs-lookup"><span data-stu-id="deb01-108">Example 1: Add a route to a route table</span></span>
```
PS C:\>$RouteTable = Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
PS C:\> Add-AzRouteConfig -Name "Route13" -AddressPrefix 10.3.0.0/16 -NextHopType "VnetLocal" -RouteTable $RouteTable
```

<span data-ttu-id="deb01-109">Der erste Befehl ruft mithilfe des Get-AzRouteTable-Cmdlets eine Routingtabelle mit dem Namen RouteTable01 ab.</span><span class="sxs-lookup"><span data-stu-id="deb01-109">The first command gets a route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="deb01-110">Der Befehl speichert die Tabelle in der $RouteTable-Variablen.</span><span class="sxs-lookup"><span data-stu-id="deb01-110">The command stores the table in the $RouteTable variable.</span></span>

<span data-ttu-id="deb01-111">Mit dem zweiten Befehl wird eine Route mit dem Namen Route13 zu der in $RouteTable gespeicherten Routentabelle hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="deb01-111">The second command adds a route named Route13 to the route table stored in $RouteTable.</span></span>
<span data-ttu-id="deb01-112">Diese Route leitet Pakete an das lokale virtuelle Netzwerk weiter.</span><span class="sxs-lookup"><span data-stu-id="deb01-112">This route forwards packets to the local virtual network.</span></span>

### <span data-ttu-id="deb01-113">Beispiel 2: Hinzufügen einer Route zu einer Routentabelle mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="deb01-113">Example 2: Add a route to a route table by using the pipeline</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzRouteConfig -Name "Route02" -AddressPrefix 10.2.0.0/16 -NextHopType VnetLocal | Set-AzRouteTable
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

<span data-ttu-id="deb01-114">Dieser Befehl ruft die Routingtabelle mit dem Namen RouteTable01 mithilfe von **Get-AzRouteTable**.</span><span class="sxs-lookup"><span data-stu-id="deb01-114">This command gets the route table named RouteTable01 by using **Get-AzRouteTable**.</span></span>
<span data-ttu-id="deb01-115">Der Befehl übergibt diese Tabelle mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="deb01-115">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="deb01-116">Das aktuelle Cmdlet fügt die Route mit dem Namen "Route02" hinzu und übergibt dann das Ergebnis an das Cmdlet "AzRouteTable", das die Tabelle so aktualisiert, dass die Änderungen wieder **gegeben** werden.</span><span class="sxs-lookup"><span data-stu-id="deb01-116">The current cmdlet adds the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="deb01-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="deb01-117">PARAMETERS</span></span>

### <span data-ttu-id="deb01-118">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="deb01-118">-AddressPrefix</span></span>
<span data-ttu-id="deb01-119">Gibt das Ziel im CIDR-Format (klassenlos InterDomain Routing) an, auf das die Route angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="deb01-119">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="deb01-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deb01-120">-DefaultProfile</span></span>
<span data-ttu-id="deb01-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="deb01-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="deb01-122">-Name</span><span class="sxs-lookup"><span data-stu-id="deb01-122">-Name</span></span>
<span data-ttu-id="deb01-123">Gibt den Namen der Route an, die der Route-Tabelle hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="deb01-123">Specifies a name of the route to add to the route table.</span></span>

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

### <span data-ttu-id="deb01-124">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="deb01-124">-NextHopIpAddress</span></span>
<span data-ttu-id="deb01-125">Gibt die IP-Adresse einer virtuellen Appliance an, die Sie Ihrem virtuellen Azure-Netzwerk hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="deb01-125">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="deb01-126">Diese Route leitet Pakete an diese Adresse weiter.</span><span class="sxs-lookup"><span data-stu-id="deb01-126">This route forwards packets to that address.</span></span>
<span data-ttu-id="deb01-127">Geben Sie diesen Parameter nur an, wenn Sie einen Wert von VirtualAppliance für den *NextHopType* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="deb01-127">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="deb01-128">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="deb01-128">-NextHopType</span></span>
<span data-ttu-id="deb01-129">Gibt an, wie Pakete von dieser Route weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="deb01-129">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="deb01-130">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="deb01-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="deb01-131">Internet.</span><span class="sxs-lookup"><span data-stu-id="deb01-131">Internet.</span></span>
<span data-ttu-id="deb01-132">Das standardmäßige Internet Gateway, das von Azure bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="deb01-132">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="deb01-133">Keine.</span><span class="sxs-lookup"><span data-stu-id="deb01-133">None.</span></span>
<span data-ttu-id="deb01-134">Wenn Sie diesen Wert angeben, leitet die Route keine Pakete weiter.</span><span class="sxs-lookup"><span data-stu-id="deb01-134">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="deb01-135">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="deb01-135">VirtualAppliance.</span></span>
<span data-ttu-id="deb01-136">Eine virtuelle Appliance, die Sie Ihrem virtuellen Azure-Netzwerk hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="deb01-136">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="deb01-137">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="deb01-137">VirtualNetworkGateway.</span></span>
<span data-ttu-id="deb01-138">Ein Azure Server-zu-Server-virtuelles privates Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="deb01-138">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="deb01-139">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="deb01-139">VnetLocal.</span></span>
<span data-ttu-id="deb01-140">Lokales virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="deb01-140">The local virtual network.</span></span>
<span data-ttu-id="deb01-141">Wenn Sie über zwei Subnetze (10.1.0.0/16 und 10.2.0.0/16) im gleichen virtuellen Netzwerk verfügen, wählen Sie den Wert VnetLocal für jedes Subnetz aus, um es an das andere Subnetz weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="deb01-141">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="deb01-142">-Routel</span><span class="sxs-lookup"><span data-stu-id="deb01-142">-RouteTable</span></span>
<span data-ttu-id="deb01-143">Gibt die Routingtabelle an, der das Cmdlet eine Route hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="deb01-143">Specifies the route table to which this cmdlet adds a route.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="deb01-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="deb01-144">-Confirm</span></span>
<span data-ttu-id="deb01-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="deb01-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="deb01-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="deb01-146">-WhatIf</span></span>
<span data-ttu-id="deb01-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="deb01-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="deb01-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="deb01-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="deb01-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deb01-149">CommonParameters</span></span>
<span data-ttu-id="deb01-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="deb01-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deb01-151">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="deb01-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deb01-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="deb01-152">INPUTS</span></span>

### <span data-ttu-id="deb01-153">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="deb01-153">PSRouteTable</span></span>
<span data-ttu-id="deb01-154">Der Parameter "routeable" akzeptiert den Wert vom Typ "PSRouteTable" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="deb01-154">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="deb01-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="deb01-155">OUTPUTS</span></span>

### <span data-ttu-id="deb01-156">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="deb01-156">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="deb01-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="deb01-157">NOTES</span></span>

## <span data-ttu-id="deb01-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="deb01-158">RELATED LINKS</span></span>

[<span data-ttu-id="deb01-159">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="deb01-159">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="deb01-160">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="deb01-160">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="deb01-161">Neu – AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="deb01-161">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="deb01-162">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="deb01-162">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="deb01-163">Satz-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="deb01-163">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)

[<span data-ttu-id="deb01-164">Satz-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="deb01-164">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


