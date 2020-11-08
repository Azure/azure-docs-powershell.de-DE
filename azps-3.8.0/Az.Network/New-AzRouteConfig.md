---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteConfig.md
ms.openlocfilehash: 83f6f44af262719c9ed9fb5cae818bc6b70d5c2b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003457"
---
# <span data-ttu-id="27563-101">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="27563-101">New-AzRouteConfig</span></span>

## <span data-ttu-id="27563-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="27563-102">SYNOPSIS</span></span>
<span data-ttu-id="27563-103">Erstellt eine Route für eine Routentabelle.</span><span class="sxs-lookup"><span data-stu-id="27563-103">Creates a route for a route table.</span></span>

## <span data-ttu-id="27563-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="27563-104">SYNTAX</span></span>

```
New-AzRouteConfig [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="27563-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="27563-105">DESCRIPTION</span></span>
<span data-ttu-id="27563-106">Das Cmdlet **New-AzRouteConfig** erstellt eine Route für eine Azure Route-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="27563-106">The **New-AzRouteConfig** cmdlet creates a route for an Azure route table.</span></span>

## <span data-ttu-id="27563-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="27563-107">EXAMPLES</span></span>

### <span data-ttu-id="27563-108">Beispiel 1: Erstellen einer Route</span><span class="sxs-lookup"><span data-stu-id="27563-108">Example 1: Create a route</span></span>
```
PS C:\>$Route = New-AzRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> $Route
Name              : Route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="27563-109">Der erste Befehl erstellt eine Route mit dem Namen Route07 und speichert Sie dann in der $Route-Variablen.</span><span class="sxs-lookup"><span data-stu-id="27563-109">The first command creates a route named Route07, and then stores it in the $Route variable.</span></span>
<span data-ttu-id="27563-110">Diese Route leitet Pakete an das lokale virtuelle Netzwerk weiter.</span><span class="sxs-lookup"><span data-stu-id="27563-110">This route forwards packets to the local virtual network.</span></span>
<span data-ttu-id="27563-111">Mit dem zweiten Befehl werden die Eigenschaften der Route angezeigt.</span><span class="sxs-lookup"><span data-stu-id="27563-111">The second command displays the properties of the route.</span></span>

## <span data-ttu-id="27563-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="27563-112">PARAMETERS</span></span>

### <span data-ttu-id="27563-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="27563-113">-AddressPrefix</span></span>
<span data-ttu-id="27563-114">Gibt das Ziel im CIDR-Format (klassenlos InterDomain Routing) an, auf das die Route angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="27563-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="27563-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27563-115">-DefaultProfile</span></span>
<span data-ttu-id="27563-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="27563-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27563-117">-Name</span><span class="sxs-lookup"><span data-stu-id="27563-117">-Name</span></span>
<span data-ttu-id="27563-118">Gibt einen Namen für die Route an.</span><span class="sxs-lookup"><span data-stu-id="27563-118">Specifies a name for the route.</span></span>

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

### <span data-ttu-id="27563-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="27563-119">-NextHopIpAddress</span></span>
<span data-ttu-id="27563-120">Gibt die IP-Adresse einer virtuellen Appliance an, die Sie Ihrem Azurevirtual-Netzwerk hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="27563-120">Specifies the IP address of a virtual appliance that you add to your Azurevirtual network.</span></span>
<span data-ttu-id="27563-121">Diese Route leitet Pakete an diese Adresse weiter.</span><span class="sxs-lookup"><span data-stu-id="27563-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="27563-122">Geben Sie diesen Parameter nur an, wenn Sie einen Wert von VirtualAppliance für den *NextHopType* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="27563-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="27563-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="27563-123">-NextHopType</span></span>
<span data-ttu-id="27563-124">Gibt an, wie Pakete von dieser Route weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="27563-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="27563-125">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="27563-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="27563-126">Internet.</span><span class="sxs-lookup"><span data-stu-id="27563-126">Internet.</span></span>
<span data-ttu-id="27563-127">Das standardmäßige Internet Gateway, das von Azure bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="27563-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="27563-128">Keine.</span><span class="sxs-lookup"><span data-stu-id="27563-128">None.</span></span>
<span data-ttu-id="27563-129">Wenn Sie diesen Wert angeben, leitet die Route keine Pakete weiter.</span><span class="sxs-lookup"><span data-stu-id="27563-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="27563-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="27563-130">VirtualAppliance.</span></span>
<span data-ttu-id="27563-131">Eine virtuelle Appliance, die Sie Ihrem virtuellen Azure-Netzwerk hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="27563-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="27563-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="27563-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="27563-133">Ein Azure Server-zu-Server-virtuelles privates Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="27563-133">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="27563-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="27563-134">VnetLocal.</span></span>
<span data-ttu-id="27563-135">Lokales virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="27563-135">The local virtual network.</span></span>
<span data-ttu-id="27563-136">Wenn Sie über zwei Subnetze (10.1.0.0/16 und 10.2.0.0/16) im gleichen virtuellen Netzwerk verfügen, wählen Sie den Wert VnetLocal für jedes Subnetz aus, um es an das andere Subnetz weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="27563-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="27563-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="27563-137">-Confirm</span></span>
<span data-ttu-id="27563-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="27563-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27563-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27563-139">-WhatIf</span></span>
<span data-ttu-id="27563-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="27563-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27563-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="27563-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27563-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27563-142">CommonParameters</span></span>
<span data-ttu-id="27563-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27563-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27563-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27563-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27563-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="27563-145">INPUTS</span></span>

### <span data-ttu-id="27563-146">System. String</span><span class="sxs-lookup"><span data-stu-id="27563-146">System.String</span></span>

## <span data-ttu-id="27563-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="27563-147">OUTPUTS</span></span>

### <span data-ttu-id="27563-148">Microsoft. Azure. Commands. Network. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="27563-148">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="27563-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="27563-149">NOTES</span></span>

## <span data-ttu-id="27563-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="27563-150">RELATED LINKS</span></span>

[<span data-ttu-id="27563-151">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="27563-151">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="27563-152">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="27563-152">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="27563-153">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="27563-153">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="27563-154">Satz-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="27563-154">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


