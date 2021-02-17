---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6E967F9C-949E-4485-9B57-FC4F523D5DC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
ms.openlocfilehash: ca7335abfd8fe2dc9591dcb7d96fb6ca71dda4fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158868"
---
# <span data-ttu-id="4a22c-101">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4a22c-101">Set-AzRouteConfig</span></span>

## <span data-ttu-id="4a22c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a22c-102">SYNOPSIS</span></span>
<span data-ttu-id="4a22c-103">Aktualisiert eine Routenkonfiguration für eine Routentabelle.</span><span class="sxs-lookup"><span data-stu-id="4a22c-103">Updates a route configuration for a route table.</span></span>

## <span data-ttu-id="4a22c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a22c-104">SYNTAX</span></span>

```
Set-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4a22c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a22c-105">DESCRIPTION</span></span>
<span data-ttu-id="4a22c-106">Das **Cmdlet Set-AzRouteConfig** aktualisiert eine Routenkonfiguration für eine Routentabelle.</span><span class="sxs-lookup"><span data-stu-id="4a22c-106">The **Set-AzRouteConfig** cmdlet updates a route configuration for a route table.</span></span>

## <span data-ttu-id="4a22c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4a22c-107">EXAMPLES</span></span>

### <span data-ttu-id="4a22c-108">Beispiel 1: Ändern einer Route</span><span class="sxs-lookup"><span data-stu-id="4a22c-108">Example 1: Modify a route</span></span>
```powershell
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Set-AzRouteConfig -Name "Route02" -AddressPrefix 10.4.0.0/16 -NextHopType VnetLocal | Set-AzRouteTable
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

<span data-ttu-id="4a22c-109">Dieser Befehl ruft die Routentabelle mit dem Namen "RouteTable01" mithilfe des cmdlets Get-AzRouteTable ab.</span><span class="sxs-lookup"><span data-stu-id="4a22c-109">This command gets the route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="4a22c-110">Der Befehl übergibt diese Tabelle mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a22c-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4a22c-111">Das aktuelle Cmdlet ändert die Route namens "Route02" und übergibt das Ergebnis dann an das **Set-AzRouteTable-Cmdlet,** das die Tabelle entsprechend Ihren Änderungen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="4a22c-111">The current cmdlet modifies the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="4a22c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a22c-112">PARAMETERS</span></span>

### <span data-ttu-id="4a22c-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4a22c-113">-AddressPrefix</span></span>
<span data-ttu-id="4a22c-114">Gibt das Ziel im klassenloses domänenübergreifendes Routing (CIDR) an, auf das die Route angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="4a22c-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="4a22c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a22c-115">-DefaultProfile</span></span>
<span data-ttu-id="4a22c-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a22c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a22c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4a22c-117">-Name</span></span>
<span data-ttu-id="4a22c-118">Gibt den Namen der Route an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="4a22c-118">Specifies the name of the route that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4a22c-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="4a22c-119">-NextHopIpAddress</span></span>
<span data-ttu-id="4a22c-120">Gibt die IP-Adresse eines virtuellen Geräts an, das Sie Ihrem virtuellen Azure-Netzwerk hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4a22c-120">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="4a22c-121">Dadurch werden Pakete an diese Adresse weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="4a22c-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="4a22c-122">Geben Sie diesen Parameter nur an, wenn Sie einen Wert von "VirtualAppliance" für den Parameter *"NextHopType"* angeben.</span><span class="sxs-lookup"><span data-stu-id="4a22c-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="4a22c-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="4a22c-123">-NextHopType</span></span>
<span data-ttu-id="4a22c-124">Gibt an, wie Pakete durch diese Route weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="4a22c-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="4a22c-125">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="4a22c-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4a22c-126">Internet" aus.</span><span class="sxs-lookup"><span data-stu-id="4a22c-126">Internet.</span></span>
<span data-ttu-id="4a22c-127">Das von Azure bereitgestellte Standard-Internetgateway.</span><span class="sxs-lookup"><span data-stu-id="4a22c-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="4a22c-128">"Keine".</span><span class="sxs-lookup"><span data-stu-id="4a22c-128">None.</span></span>
<span data-ttu-id="4a22c-129">Wenn Sie diesen Wert angeben, werden von der Route keine Pakete weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="4a22c-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="4a22c-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="4a22c-130">VirtualAppliance.</span></span>
<span data-ttu-id="4a22c-131">Ein virtuelles Gerät, das Sie Ihrem virtuellen Azure-Netzwerk hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4a22c-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="4a22c-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="4a22c-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="4a22c-133">Ein Gateway für virtuelles privates Netzwerk von Azureserver zu Server.</span><span class="sxs-lookup"><span data-stu-id="4a22c-133">An Azureserver-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="4a22c-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="4a22c-134">VnetLocal.</span></span>
<span data-ttu-id="4a22c-135">Das lokale virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="4a22c-135">The local virtual network.</span></span>
<span data-ttu-id="4a22c-136">Wenn Sie über zwei Subnetze verfügen, 10.1.0.0/16 und 10.2.0.0/16 im gleichen virtuellen Netzwerk, wählen Sie einen Wert von "VnetLocal" für jedes Subnetz aus, das an das andere Subnetz weitergeleitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a22c-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="4a22c-137">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="4a22c-137">-RouteTable</span></span>
<span data-ttu-id="4a22c-138">Gibt die Routentabelle an, der diese Route zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4a22c-138">Specifies the route table with which this route is associated.</span></span>

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

### <span data-ttu-id="4a22c-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a22c-139">-Confirm</span></span>
<span data-ttu-id="4a22c-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4a22c-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a22c-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4a22c-141">-WhatIf</span></span>
<span data-ttu-id="4a22c-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4a22c-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4a22c-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4a22c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a22c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a22c-144">CommonParameters</span></span>
<span data-ttu-id="4a22c-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a22c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a22c-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a22c-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a22c-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4a22c-147">INPUTS</span></span>

### <span data-ttu-id="4a22c-148">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="4a22c-148">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="4a22c-149">System.String</span><span class="sxs-lookup"><span data-stu-id="4a22c-149">System.String</span></span>

## <span data-ttu-id="4a22c-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4a22c-150">OUTPUTS</span></span>

### <span data-ttu-id="4a22c-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="4a22c-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="4a22c-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4a22c-152">NOTES</span></span>

## <span data-ttu-id="4a22c-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4a22c-153">RELATED LINKS</span></span>

[<span data-ttu-id="4a22c-154">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4a22c-154">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="4a22c-155">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4a22c-155">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="4a22c-156">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4a22c-156">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="4a22c-157">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4a22c-157">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)


