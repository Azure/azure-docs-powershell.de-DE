---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C868DFA4-8A9D-4108-B88B-ACD7F100A63C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteConfig.md
ms.openlocfilehash: 326baa91b8da8f9bae67cf47dcc69246549d7c06
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175094"
---
# <span data-ttu-id="ddb55-101">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="ddb55-101">Add-AzRouteConfig</span></span>

## <span data-ttu-id="ddb55-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ddb55-102">SYNOPSIS</span></span>
<span data-ttu-id="ddb55-103">Fügt eine Route zu einer Routentabelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="ddb55-103">Adds a route to a route table.</span></span>

## <span data-ttu-id="ddb55-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ddb55-104">SYNTAX</span></span>

```
Add-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ddb55-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ddb55-105">DESCRIPTION</span></span>
<span data-ttu-id="ddb55-106">Mit dem Cmdlet **Add-AzRouteConfig** wird eine Route zu einer Azure Route-Tabelle hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ddb55-106">The **Add-AzRouteConfig** cmdlet adds a route to an Azure route table.</span></span>

## <span data-ttu-id="ddb55-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ddb55-107">EXAMPLES</span></span>

### <span data-ttu-id="ddb55-108">Beispiel 1: Hinzufügen einer Route zu einer Routentabelle</span><span class="sxs-lookup"><span data-stu-id="ddb55-108">Example 1: Add a route to a route table</span></span>
```powershell
PS C:\>$RouteTable = Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
PS C:\> Add-AzRouteConfig -Name "Route13" -AddressPrefix 10.3.0.0/16 -NextHopType "VnetLocal" -RouteTable $RouteTable
```

<span data-ttu-id="ddb55-109">Der erste Befehl ruft mithilfe des Get-AzRouteTable-Cmdlets eine Routingtabelle mit dem Namen RouteTable01 ab.</span><span class="sxs-lookup"><span data-stu-id="ddb55-109">The first command gets a route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="ddb55-110">Der Befehl speichert die Tabelle in der $RouteTable-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ddb55-110">The command stores the table in the $RouteTable variable.</span></span>
<span data-ttu-id="ddb55-111">Mit dem zweiten Befehl wird eine Route mit dem Namen Route13 zu der in $RouteTable gespeicherten Routentabelle hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ddb55-111">The second command adds a route named Route13 to the route table stored in $RouteTable.</span></span>
<span data-ttu-id="ddb55-112">Diese Route leitet Pakete an das lokale virtuelle Netzwerk weiter.</span><span class="sxs-lookup"><span data-stu-id="ddb55-112">This route forwards packets to the local virtual network.</span></span>

### <span data-ttu-id="ddb55-113">Beispiel 2: Hinzufügen einer Route zu einer Routentabelle mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="ddb55-113">Example 2: Add a route to a route table by using the pipeline</span></span>
```powershell
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

<span data-ttu-id="ddb55-114">Dieser Befehl ruft die Routingtabelle mit dem Namen RouteTable01 mithilfe von **Get-AzRouteTable**.</span><span class="sxs-lookup"><span data-stu-id="ddb55-114">This command gets the route table named RouteTable01 by using **Get-AzRouteTable**.</span></span>
<span data-ttu-id="ddb55-115">Der Befehl übergibt diese Tabelle mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddb55-115">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ddb55-116">Das aktuelle Cmdlet fügt die Route mit dem Namen "Route02" hinzu und übergibt dann das Ergebnis an das Cmdlet "AzRouteTable", das die Tabelle so aktualisiert, dass die Änderungen wieder **gegeben** werden.</span><span class="sxs-lookup"><span data-stu-id="ddb55-116">The current cmdlet adds the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="ddb55-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="ddb55-117">PARAMETERS</span></span>

### <span data-ttu-id="ddb55-118">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ddb55-118">-AddressPrefix</span></span>
<span data-ttu-id="ddb55-119">Gibt das Ziel im CIDR-Format (klassenlos InterDomain Routing) an, auf das die Route angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="ddb55-119">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddb55-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddb55-120">-DefaultProfile</span></span>
<span data-ttu-id="ddb55-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ddb55-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddb55-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ddb55-122">-Name</span></span>
<span data-ttu-id="ddb55-123">Gibt den Namen der Route an, die der Route-Tabelle hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ddb55-123">Specifies a name of the route to add to the route table.</span></span>

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

### <span data-ttu-id="ddb55-124">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="ddb55-124">-NextHopIpAddress</span></span>
<span data-ttu-id="ddb55-125">Gibt die IP-Adresse einer virtuellen Appliance an, die Sie Ihrem virtuellen Azure-Netzwerk hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ddb55-125">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="ddb55-126">Diese Route leitet Pakete an diese Adresse weiter.</span><span class="sxs-lookup"><span data-stu-id="ddb55-126">This route forwards packets to that address.</span></span>
<span data-ttu-id="ddb55-127">Geben Sie diesen Parameter nur an, wenn Sie einen Wert von VirtualAppliance für den *NextHopType* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="ddb55-127">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddb55-128">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="ddb55-128">-NextHopType</span></span>
<span data-ttu-id="ddb55-129">Gibt an, wie Pakete von dieser Route weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="ddb55-129">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="ddb55-130">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ddb55-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ddb55-131">Internet.</span><span class="sxs-lookup"><span data-stu-id="ddb55-131">Internet.</span></span>
<span data-ttu-id="ddb55-132">Das standardmäßige Internet Gateway, das von Azure bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="ddb55-132">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="ddb55-133">Keine.</span><span class="sxs-lookup"><span data-stu-id="ddb55-133">None.</span></span>
<span data-ttu-id="ddb55-134">Wenn Sie diesen Wert angeben, leitet die Route keine Pakete weiter.</span><span class="sxs-lookup"><span data-stu-id="ddb55-134">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="ddb55-135">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="ddb55-135">VirtualAppliance.</span></span>
<span data-ttu-id="ddb55-136">Eine virtuelle Appliance, die Sie Ihrem virtuellen Azure-Netzwerk hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ddb55-136">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="ddb55-137">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="ddb55-137">VirtualNetworkGateway.</span></span>
<span data-ttu-id="ddb55-138">Ein Azure Server-zu-Server-virtuelles privates Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="ddb55-138">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="ddb55-139">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="ddb55-139">VnetLocal.</span></span>
<span data-ttu-id="ddb55-140">Lokales virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="ddb55-140">The local virtual network.</span></span>
<span data-ttu-id="ddb55-141">Wenn Sie über zwei Subnetze (10.1.0.0/16 und 10.2.0.0/16) im gleichen virtuellen Netzwerk verfügen, wählen Sie den Wert VnetLocal für jedes Subnetz aus, um es an das andere Subnetz weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="ddb55-141">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddb55-142">-Routel</span><span class="sxs-lookup"><span data-stu-id="ddb55-142">-RouteTable</span></span>
<span data-ttu-id="ddb55-143">Gibt die Routingtabelle an, der das Cmdlet eine Route hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="ddb55-143">Specifies the route table to which this cmdlet adds a route.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ddb55-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ddb55-144">-Confirm</span></span>
<span data-ttu-id="ddb55-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ddb55-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddb55-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddb55-146">-WhatIf</span></span>
<span data-ttu-id="ddb55-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ddb55-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ddb55-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ddb55-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddb55-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddb55-149">CommonParameters</span></span>
<span data-ttu-id="ddb55-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddb55-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddb55-151">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddb55-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddb55-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ddb55-152">INPUTS</span></span>

### <span data-ttu-id="ddb55-153">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="ddb55-153">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="ddb55-154">System. String</span><span class="sxs-lookup"><span data-stu-id="ddb55-154">System.String</span></span>

## <span data-ttu-id="ddb55-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ddb55-155">OUTPUTS</span></span>

### <span data-ttu-id="ddb55-156">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="ddb55-156">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="ddb55-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="ddb55-157">NOTES</span></span>

## <span data-ttu-id="ddb55-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ddb55-158">RELATED LINKS</span></span>

[<span data-ttu-id="ddb55-159">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="ddb55-159">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="ddb55-160">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="ddb55-160">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="ddb55-161">Neu – AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="ddb55-161">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="ddb55-162">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="ddb55-162">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="ddb55-163">Satz-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="ddb55-163">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)

[<span data-ttu-id="ddb55-164">Satz-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="ddb55-164">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


