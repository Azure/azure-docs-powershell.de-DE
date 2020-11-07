---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6E967F9C-949E-4485-9B57-FC4F523D5DC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzRouteConfig.md
ms.openlocfilehash: 58adfcb04fef8822624669f8a723de5a524ae3aa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843584"
---
# <span data-ttu-id="9b879-101">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="9b879-101">Set-AzRouteConfig</span></span>

## <span data-ttu-id="9b879-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9b879-102">SYNOPSIS</span></span>
<span data-ttu-id="9b879-103">Legt den Zielstatus für eine Route fest.</span><span class="sxs-lookup"><span data-stu-id="9b879-103">Sets the goal state for a route.</span></span>

## <span data-ttu-id="9b879-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b879-104">SYNTAX</span></span>

```
Set-AzRouteConfig -RouteTable <PSRouteTable> [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b879-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9b879-105">DESCRIPTION</span></span>
<span data-ttu-id="9b879-106">Das Cmdlet " **Set-AzRouteConfig** " legt den Zielstatus für eine Azure-Route fest.</span><span class="sxs-lookup"><span data-stu-id="9b879-106">The **Set-AzRouteConfig** cmdlet sets the goal state for an Azure route.</span></span>

## <span data-ttu-id="9b879-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9b879-107">EXAMPLES</span></span>

### <span data-ttu-id="9b879-108">Beispiel 1: Ändern einer Route</span><span class="sxs-lookup"><span data-stu-id="9b879-108">Example 1: Modify a route</span></span>
```
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

<span data-ttu-id="9b879-109">Dieser Befehl ruft die Routingtabelle mit dem Namen RouteTable01 mithilfe des Get-AzRouteTable-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="9b879-109">This command gets the route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="9b879-110">Der Befehl übergibt diese Tabelle mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b879-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9b879-111">Das aktuelle Cmdlet ändert die Route mit dem Namen Route02 und übergibt dann das Ergebnis an das Cmdlet " **setAzRouteTable** ", das die Tabelle so aktualisiert, dass die Änderungen wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9b879-111">The current cmdlet modifies the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="9b879-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b879-112">PARAMETERS</span></span>

### <span data-ttu-id="9b879-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9b879-113">-AddressPrefix</span></span>
<span data-ttu-id="9b879-114">Gibt das Ziel im CIDR-Format (klassenlos InterDomain Routing) an, auf das die Route angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="9b879-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="9b879-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b879-115">-DefaultProfile</span></span>
<span data-ttu-id="9b879-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9b879-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b879-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9b879-117">-Name</span></span>
<span data-ttu-id="9b879-118">Gibt den Namen der Route an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="9b879-118">Specifies the name of the route that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9b879-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="9b879-119">-NextHopIpAddress</span></span>
<span data-ttu-id="9b879-120">Gibt die IP-Adresse einer virtuellen Appliance an, die Sie Ihrem virtuellen Azure-Netzwerk hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9b879-120">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="9b879-121">Diese Route leitet Pakete an diese Adresse weiter.</span><span class="sxs-lookup"><span data-stu-id="9b879-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="9b879-122">Geben Sie diesen Parameter nur an, wenn Sie einen Wert von VirtualAppliance für den *NextHopType* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="9b879-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="9b879-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="9b879-123">-NextHopType</span></span>
<span data-ttu-id="9b879-124">Gibt an, wie Pakete von dieser Route weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="9b879-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="9b879-125">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9b879-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9b879-126">Internet.</span><span class="sxs-lookup"><span data-stu-id="9b879-126">Internet.</span></span>
<span data-ttu-id="9b879-127">Das standardmäßige Internet Gateway, das von Azure bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="9b879-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="9b879-128">Keine.</span><span class="sxs-lookup"><span data-stu-id="9b879-128">None.</span></span>
<span data-ttu-id="9b879-129">Wenn Sie diesen Wert angeben, leitet die Route keine Pakete weiter.</span><span class="sxs-lookup"><span data-stu-id="9b879-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="9b879-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="9b879-130">VirtualAppliance.</span></span>
<span data-ttu-id="9b879-131">Eine virtuelle Appliance, die Sie Ihrem virtuellen Azure-Netzwerk hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9b879-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="9b879-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="9b879-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="9b879-133">Ein Azureserver-zu-Server-virtuelles privates Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="9b879-133">An Azureserver-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="9b879-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="9b879-134">VnetLocal.</span></span>
<span data-ttu-id="9b879-135">Lokales virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="9b879-135">The local virtual network.</span></span>
<span data-ttu-id="9b879-136">Wenn Sie über zwei Subnetze (10.1.0.0/16 und 10.2.0.0/16) im gleichen virtuellen Netzwerk verfügen, wählen Sie den Wert VnetLocal für jedes Subnetz aus, um es an das andere Subnetz weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="9b879-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="9b879-137">-Routel</span><span class="sxs-lookup"><span data-stu-id="9b879-137">-RouteTable</span></span>
<span data-ttu-id="9b879-138">Gibt die Routentabelle an, der diese Route zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9b879-138">Specifies the route table with which this route is associated.</span></span>

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

### <span data-ttu-id="9b879-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9b879-139">-Confirm</span></span>
<span data-ttu-id="9b879-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9b879-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b879-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b879-141">-WhatIf</span></span>
<span data-ttu-id="9b879-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9b879-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b879-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b879-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b879-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b879-144">CommonParameters</span></span>
<span data-ttu-id="9b879-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b879-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b879-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b879-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b879-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9b879-147">INPUTS</span></span>

### <span data-ttu-id="9b879-148">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="9b879-148">PSRouteTable</span></span>
<span data-ttu-id="9b879-149">Der Parameter "routeable" akzeptiert den Wert vom Typ "PSRouteTable" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="9b879-149">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="9b879-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9b879-150">OUTPUTS</span></span>

### <span data-ttu-id="9b879-151">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="9b879-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="9b879-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="9b879-152">NOTES</span></span>

## <span data-ttu-id="9b879-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9b879-153">RELATED LINKS</span></span>

[<span data-ttu-id="9b879-154">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="9b879-154">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="9b879-155">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="9b879-155">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="9b879-156">Neu – AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="9b879-156">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="9b879-157">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="9b879-157">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)


