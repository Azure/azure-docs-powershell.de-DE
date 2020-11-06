---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C868DFA4-8A9D-4108-B88B-ACD7F100A63C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteConfig.md
ms.openlocfilehash: ecd5df4728e963e8bcf4614a6acb554fdbf17788
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499793"
---
# <span data-ttu-id="634eb-101">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="634eb-101">Add-AzureRmRouteConfig</span></span>

## <span data-ttu-id="634eb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="634eb-102">SYNOPSIS</span></span>
<span data-ttu-id="634eb-103">Fügt eine Route zu einer Routentabelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="634eb-103">Adds a route to a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="634eb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="634eb-104">SYNTAX</span></span>

```
Add-AzureRmRouteConfig -RouteTable <PSRouteTable> [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="634eb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="634eb-105">DESCRIPTION</span></span>
<span data-ttu-id="634eb-106">Mit dem Cmdlet **Add-AzureRmRouteConfig** wird eine Route zu einer Azure Route-Tabelle hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="634eb-106">The **Add-AzureRmRouteConfig** cmdlet adds a route to an Azure route table.</span></span>

## <span data-ttu-id="634eb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="634eb-107">EXAMPLES</span></span>

### <span data-ttu-id="634eb-108">Beispiel 1: Hinzufügen einer Route zu einer Routentabelle</span><span class="sxs-lookup"><span data-stu-id="634eb-108">Example 1: Add a route to a route table</span></span>
```
PS C:\>$RouteTable = Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
PS C:\> Add-AzureRmRouteConfig -Name "Route13" -AddressPrefix 10.3.0.0/16 -NextHopType "VnetLocal" -RouteTable $RouteTable
```

<span data-ttu-id="634eb-109">Der erste Befehl ruft mithilfe des Get-AzureRmRouteTable-Cmdlets eine Routingtabelle mit dem Namen RouteTable01 ab.</span><span class="sxs-lookup"><span data-stu-id="634eb-109">The first command gets a route table named RouteTable01 by using the Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="634eb-110">Der Befehl speichert die Tabelle in der $RouteTable-Variablen.</span><span class="sxs-lookup"><span data-stu-id="634eb-110">The command stores the table in the $RouteTable variable.</span></span>

<span data-ttu-id="634eb-111">Mit dem zweiten Befehl wird eine Route mit dem Namen Route13 zu der in $RouteTable gespeicherten Routentabelle hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="634eb-111">The second command adds a route named Route13 to the route table stored in $RouteTable.</span></span>
<span data-ttu-id="634eb-112">Diese Route leitet Pakete an das lokale virtuelle Netzwerk weiter.</span><span class="sxs-lookup"><span data-stu-id="634eb-112">This route forwards packets to the local virtual network.</span></span>

### <span data-ttu-id="634eb-113">Beispiel 2: Hinzufügen einer Route zu einer Routentabelle mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="634eb-113">Example 2: Add a route to a route table by using the pipeline</span></span>
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

<span data-ttu-id="634eb-114">Dieser Befehl ruft die Routingtabelle mit dem Namen RouteTable01 mithilfe von **Get-AzureRmRouteTable**.</span><span class="sxs-lookup"><span data-stu-id="634eb-114">This command gets the route table named RouteTable01 by using **Get-AzureRmRouteTable**.</span></span>
<span data-ttu-id="634eb-115">Der Befehl übergibt diese Tabelle mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="634eb-115">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="634eb-116">Das aktuelle Cmdlet fügt die Route mit dem Namen "Route02" hinzu und übergibt dann das Ergebnis an das Cmdlet "AzureRmRouteTable", das die Tabelle so aktualisiert, dass die Änderungen wieder **gegeben** werden.</span><span class="sxs-lookup"><span data-stu-id="634eb-116">The current cmdlet adds the route named Route02, and then passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="634eb-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="634eb-117">PARAMETERS</span></span>

### <span data-ttu-id="634eb-118">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="634eb-118">-AddressPrefix</span></span>
<span data-ttu-id="634eb-119">Gibt das Ziel im CIDR-Format (klassenlos InterDomain Routing) an, auf das die Route angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="634eb-119">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="634eb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="634eb-120">-DefaultProfile</span></span>
<span data-ttu-id="634eb-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="634eb-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="634eb-122">-Name</span><span class="sxs-lookup"><span data-stu-id="634eb-122">-Name</span></span>
<span data-ttu-id="634eb-123">Gibt den Namen der Route an, die der Route-Tabelle hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="634eb-123">Specifies a name of the route to add to the route table.</span></span>

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

### <span data-ttu-id="634eb-124">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="634eb-124">-NextHopIpAddress</span></span>
<span data-ttu-id="634eb-125">Gibt die IP-Adresse einer virtuellen Appliance an, die Sie Ihrem virtuellen Azure-Netzwerk hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="634eb-125">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="634eb-126">Diese Route leitet Pakete an diese Adresse weiter.</span><span class="sxs-lookup"><span data-stu-id="634eb-126">This route forwards packets to that address.</span></span>
<span data-ttu-id="634eb-127">Geben Sie diesen Parameter nur an, wenn Sie einen Wert von VirtualAppliance für den *NextHopType* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="634eb-127">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="634eb-128">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="634eb-128">-NextHopType</span></span>
<span data-ttu-id="634eb-129">Gibt an, wie Pakete von dieser Route weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="634eb-129">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="634eb-130">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="634eb-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="634eb-131">Internet.</span><span class="sxs-lookup"><span data-stu-id="634eb-131">Internet.</span></span>
<span data-ttu-id="634eb-132">Das standardmäßige Internet Gateway, das von Azure bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="634eb-132">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="634eb-133">Keine.</span><span class="sxs-lookup"><span data-stu-id="634eb-133">None.</span></span>
<span data-ttu-id="634eb-134">Wenn Sie diesen Wert angeben, leitet die Route keine Pakete weiter.</span><span class="sxs-lookup"><span data-stu-id="634eb-134">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="634eb-135">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="634eb-135">VirtualAppliance.</span></span>
<span data-ttu-id="634eb-136">Eine virtuelle Appliance, die Sie Ihrem virtuellen Azure-Netzwerk hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="634eb-136">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="634eb-137">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="634eb-137">VirtualNetworkGateway.</span></span>
<span data-ttu-id="634eb-138">Ein Azure Server-zu-Server-virtuelles privates Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="634eb-138">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="634eb-139">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="634eb-139">VnetLocal.</span></span>
<span data-ttu-id="634eb-140">Lokales virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="634eb-140">The local virtual network.</span></span>
<span data-ttu-id="634eb-141">Wenn Sie über zwei Subnetze (10.1.0.0/16 und 10.2.0.0/16) im gleichen virtuellen Netzwerk verfügen, wählen Sie den Wert VnetLocal für jedes Subnetz aus, um es an das andere Subnetz weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="634eb-141">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="634eb-142">-Routel</span><span class="sxs-lookup"><span data-stu-id="634eb-142">-RouteTable</span></span>
<span data-ttu-id="634eb-143">Gibt die Routingtabelle an, der das Cmdlet eine Route hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="634eb-143">Specifies the route table to which this cmdlet adds a route.</span></span>

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

### <span data-ttu-id="634eb-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="634eb-144">-Confirm</span></span>
<span data-ttu-id="634eb-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="634eb-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="634eb-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="634eb-146">-WhatIf</span></span>
<span data-ttu-id="634eb-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="634eb-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="634eb-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="634eb-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="634eb-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="634eb-149">CommonParameters</span></span>
<span data-ttu-id="634eb-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="634eb-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="634eb-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="634eb-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="634eb-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="634eb-152">INPUTS</span></span>

### <span data-ttu-id="634eb-153">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="634eb-153">PSRouteTable</span></span>
<span data-ttu-id="634eb-154">Der Parameter "routeable" akzeptiert den Wert vom Typ "PSRouteTable" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="634eb-154">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="634eb-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="634eb-155">OUTPUTS</span></span>

### <span data-ttu-id="634eb-156">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="634eb-156">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="634eb-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="634eb-157">NOTES</span></span>

## <span data-ttu-id="634eb-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="634eb-158">RELATED LINKS</span></span>

[<span data-ttu-id="634eb-159">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="634eb-159">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="634eb-160">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="634eb-160">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="634eb-161">Neu – AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="634eb-161">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="634eb-162">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="634eb-162">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="634eb-163">Satz-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="634eb-163">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)

[<span data-ttu-id="634eb-164">Satz-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="634eb-164">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


