---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C868DFA4-8A9D-4108-B88B-ACD7F100A63C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteConfig.md
ms.openlocfilehash: 326baa91b8da8f9bae67cf47dcc69246549d7c06
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467444"
---
# <span data-ttu-id="46c2e-101">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="46c2e-101">Add-AzRouteConfig</span></span>

## <span data-ttu-id="46c2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46c2e-102">SYNOPSIS</span></span>
<span data-ttu-id="46c2e-103">Fügt einer Routentabelle eine Route hinzu.</span><span class="sxs-lookup"><span data-stu-id="46c2e-103">Adds a route to a route table.</span></span>

## <span data-ttu-id="46c2e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46c2e-104">SYNTAX</span></span>

```
Add-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="46c2e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46c2e-105">DESCRIPTION</span></span>
<span data-ttu-id="46c2e-106">Das **Cmdlet "Add-AzRouteConfig"** fügt einer Azure-Routentabelle eine Route hinzu.</span><span class="sxs-lookup"><span data-stu-id="46c2e-106">The **Add-AzRouteConfig** cmdlet adds a route to an Azure route table.</span></span>

## <span data-ttu-id="46c2e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="46c2e-107">EXAMPLES</span></span>

### <span data-ttu-id="46c2e-108">Beispiel 1: Hinzufügen einer Route zu einer Routentabelle</span><span class="sxs-lookup"><span data-stu-id="46c2e-108">Example 1: Add a route to a route table</span></span>
```powershell
PS C:\>$RouteTable = Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
PS C:\> Add-AzRouteConfig -Name "Route13" -AddressPrefix 10.3.0.0/16 -NextHopType "VnetLocal" -RouteTable $RouteTable
```

<span data-ttu-id="46c2e-109">Der erste Befehl ruft eine Routentabelle namens "RouteTable01" mithilfe des cmdlets Get-AzRouteTable ab.</span><span class="sxs-lookup"><span data-stu-id="46c2e-109">The first command gets a route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="46c2e-110">Der Befehl speichert die Tabelle in der $RouteTable Variable.</span><span class="sxs-lookup"><span data-stu-id="46c2e-110">The command stores the table in the $RouteTable variable.</span></span>
<span data-ttu-id="46c2e-111">Der zweite Befehl fügt der in der Tabelle "Route13" gespeicherten Route den Namen "Route13" $RouteTable.</span><span class="sxs-lookup"><span data-stu-id="46c2e-111">The second command adds a route named Route13 to the route table stored in $RouteTable.</span></span>
<span data-ttu-id="46c2e-112">Mit dieser Route werden Pakete an das lokale virtuelle Netzwerk weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="46c2e-112">This route forwards packets to the local virtual network.</span></span>

### <span data-ttu-id="46c2e-113">Beispiel 2: Hinzufügen einer Route zu einer Routentabelle mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="46c2e-113">Example 2: Add a route to a route table by using the pipeline</span></span>
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

<span data-ttu-id="46c2e-114">Dieser Befehl ruft die Routentabelle mit dem Namen "RouteTable01" mit **"Get-AzRouteTable" ab.**</span><span class="sxs-lookup"><span data-stu-id="46c2e-114">This command gets the route table named RouteTable01 by using **Get-AzRouteTable**.</span></span>
<span data-ttu-id="46c2e-115">Der Befehl übergibt diese Tabelle mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46c2e-115">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="46c2e-116">Das aktuelle Cmdlet fügt die Route "Route02" hinzu und übergibt das Ergebnis an das **Set-AzRouteTable-Cmdlet,** das die Tabelle entsprechend Ihren Änderungen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="46c2e-116">The current cmdlet adds the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="46c2e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46c2e-117">PARAMETERS</span></span>

### <span data-ttu-id="46c2e-118">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="46c2e-118">-AddressPrefix</span></span>
<span data-ttu-id="46c2e-119">Gibt das Ziel im klassenloses domänenübergreifendes Routing (CIDR) an, auf das die Route angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="46c2e-119">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="46c2e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46c2e-120">-DefaultProfile</span></span>
<span data-ttu-id="46c2e-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="46c2e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46c2e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="46c2e-122">-Name</span></span>
<span data-ttu-id="46c2e-123">Gibt einen Namen der Route an, die der Routentabelle hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="46c2e-123">Specifies a name of the route to add to the route table.</span></span>

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

### <span data-ttu-id="46c2e-124">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="46c2e-124">-NextHopIpAddress</span></span>
<span data-ttu-id="46c2e-125">Gibt die IP-Adresse eines virtuellen Geräts an, das Sie Ihrem virtuellen Azure-Netzwerk hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="46c2e-125">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="46c2e-126">Dadurch werden Pakete an diese Adresse weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="46c2e-126">This route forwards packets to that address.</span></span>
<span data-ttu-id="46c2e-127">Geben Sie diesen Parameter nur an, wenn Sie einen Wert von "VirtualAppliance" für den Parameter *"NextHopType"* angeben.</span><span class="sxs-lookup"><span data-stu-id="46c2e-127">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="46c2e-128">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="46c2e-128">-NextHopType</span></span>
<span data-ttu-id="46c2e-129">Gibt an, wie Pakete durch diese Route weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="46c2e-129">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="46c2e-130">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="46c2e-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="46c2e-131">Internet" aus.</span><span class="sxs-lookup"><span data-stu-id="46c2e-131">Internet.</span></span>
<span data-ttu-id="46c2e-132">Das von Azure bereitgestellte Standard-Internetgateway.</span><span class="sxs-lookup"><span data-stu-id="46c2e-132">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="46c2e-133">"Keine".</span><span class="sxs-lookup"><span data-stu-id="46c2e-133">None.</span></span>
<span data-ttu-id="46c2e-134">Wenn Sie diesen Wert angeben, werden von der Route keine Pakete weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="46c2e-134">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="46c2e-135">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="46c2e-135">VirtualAppliance.</span></span>
<span data-ttu-id="46c2e-136">Ein virtuelles Gerät, das Sie Ihrem virtuellen Azure-Netzwerk hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="46c2e-136">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="46c2e-137">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="46c2e-137">VirtualNetworkGateway.</span></span>
<span data-ttu-id="46c2e-138">Ein virtuelles Azure Server-zu-Server-Gateway für private Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="46c2e-138">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="46c2e-139">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="46c2e-139">VnetLocal.</span></span>
<span data-ttu-id="46c2e-140">Das lokale virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="46c2e-140">The local virtual network.</span></span>
<span data-ttu-id="46c2e-141">Wenn Sie über zwei Subnetze verfügen, 10.1.0.0/16 und 10.2.0.0/16 im gleichen virtuellen Netzwerk, wählen Sie einen Wert von VnetLocal für jedes Subnetz aus, das an das andere Subnetz weitergeleitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="46c2e-141">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="46c2e-142">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="46c2e-142">-RouteTable</span></span>
<span data-ttu-id="46c2e-143">Gibt die Routentabelle an, der dieses Cmdlet eine Route hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="46c2e-143">Specifies the route table to which this cmdlet adds a route.</span></span>

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

### <span data-ttu-id="46c2e-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46c2e-144">-Confirm</span></span>
<span data-ttu-id="46c2e-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46c2e-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46c2e-146">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="46c2e-146">-WhatIf</span></span>
<span data-ttu-id="46c2e-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46c2e-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46c2e-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46c2e-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46c2e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46c2e-149">CommonParameters</span></span>
<span data-ttu-id="46c2e-150">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46c2e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46c2e-151">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46c2e-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46c2e-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="46c2e-152">INPUTS</span></span>

### <span data-ttu-id="46c2e-153">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="46c2e-153">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="46c2e-154">System.String</span><span class="sxs-lookup"><span data-stu-id="46c2e-154">System.String</span></span>

## <span data-ttu-id="46c2e-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="46c2e-155">OUTPUTS</span></span>

### <span data-ttu-id="46c2e-156">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="46c2e-156">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="46c2e-157">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="46c2e-157">NOTES</span></span>

## <span data-ttu-id="46c2e-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="46c2e-158">RELATED LINKS</span></span>

[<span data-ttu-id="46c2e-159">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="46c2e-159">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="46c2e-160">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="46c2e-160">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="46c2e-161">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="46c2e-161">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="46c2e-162">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="46c2e-162">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="46c2e-163">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="46c2e-163">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)

[<span data-ttu-id="46c2e-164">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="46c2e-164">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


