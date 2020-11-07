---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteConfig.md
ms.openlocfilehash: 07b7d0decd196fba9cbf0a813af4d252d01dfc8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660489"
---
# <span data-ttu-id="c1864-101">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c1864-101">New-AzRouteConfig</span></span>

## <span data-ttu-id="c1864-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c1864-102">SYNOPSIS</span></span>
<span data-ttu-id="c1864-103">Erstellt eine Route für eine Routentabelle.</span><span class="sxs-lookup"><span data-stu-id="c1864-103">Creates a route for a route table.</span></span>

## <span data-ttu-id="c1864-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1864-104">SYNTAX</span></span>

```
New-AzRouteConfig [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1864-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c1864-105">DESCRIPTION</span></span>
<span data-ttu-id="c1864-106">Das Cmdlet **New-AzRouteConfig** erstellt eine Route für eine Azure Route-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c1864-106">The **New-AzRouteConfig** cmdlet creates a route for an Azure route table.</span></span>

## <span data-ttu-id="c1864-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c1864-107">EXAMPLES</span></span>

### <span data-ttu-id="c1864-108">Beispiel 1: Erstellen einer Route</span><span class="sxs-lookup"><span data-stu-id="c1864-108">Example 1: Create a route</span></span>
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

<span data-ttu-id="c1864-109">Der erste Befehl erstellt eine Route mit dem Namen Route07 und speichert Sie dann in der $Route-Variablen.</span><span class="sxs-lookup"><span data-stu-id="c1864-109">The first command creates a route named Route07, and then stores it in the $Route variable.</span></span>
<span data-ttu-id="c1864-110">Diese Route leitet Pakete an das lokale virtuelle Netzwerk weiter.</span><span class="sxs-lookup"><span data-stu-id="c1864-110">This route forwards packets to the local virtual network.</span></span>
<span data-ttu-id="c1864-111">Mit dem zweiten Befehl werden die Eigenschaften der Route angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c1864-111">The second command displays the properties of the route.</span></span>

## <span data-ttu-id="c1864-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1864-112">PARAMETERS</span></span>

### <span data-ttu-id="c1864-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c1864-113">-AddressPrefix</span></span>
<span data-ttu-id="c1864-114">Gibt das Ziel im CIDR-Format (klassenlos InterDomain Routing) an, auf das die Route angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c1864-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="c1864-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1864-115">-DefaultProfile</span></span>
<span data-ttu-id="c1864-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c1864-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1864-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c1864-117">-Name</span></span>
<span data-ttu-id="c1864-118">Gibt einen Namen für die Route an.</span><span class="sxs-lookup"><span data-stu-id="c1864-118">Specifies a name for the route.</span></span>

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

### <span data-ttu-id="c1864-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="c1864-119">-NextHopIpAddress</span></span>
<span data-ttu-id="c1864-120">Gibt die IP-Adresse einer virtuellen Appliance an, die Sie Ihrem Azurevirtual-Netzwerk hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c1864-120">Specifies the IP address of a virtual appliance that you add to your Azurevirtual network.</span></span>
<span data-ttu-id="c1864-121">Diese Route leitet Pakete an diese Adresse weiter.</span><span class="sxs-lookup"><span data-stu-id="c1864-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="c1864-122">Geben Sie diesen Parameter nur an, wenn Sie einen Wert von VirtualAppliance für den *NextHopType* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="c1864-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="c1864-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="c1864-123">-NextHopType</span></span>
<span data-ttu-id="c1864-124">Gibt an, wie Pakete von dieser Route weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="c1864-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="c1864-125">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c1864-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c1864-126">Internet.</span><span class="sxs-lookup"><span data-stu-id="c1864-126">Internet.</span></span>
<span data-ttu-id="c1864-127">Das standardmäßige Internet Gateway, das von Azure bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c1864-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="c1864-128">Keine.</span><span class="sxs-lookup"><span data-stu-id="c1864-128">None.</span></span>
<span data-ttu-id="c1864-129">Wenn Sie diesen Wert angeben, leitet die Route keine Pakete weiter.</span><span class="sxs-lookup"><span data-stu-id="c1864-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="c1864-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="c1864-130">VirtualAppliance.</span></span>
<span data-ttu-id="c1864-131">Eine virtuelle Appliance, die Sie Ihrem virtuellen Azure-Netzwerk hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c1864-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="c1864-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="c1864-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="c1864-133">Ein Azure Server-zu-Server-virtuelles privates Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="c1864-133">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="c1864-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="c1864-134">VnetLocal.</span></span>
<span data-ttu-id="c1864-135">Lokales virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="c1864-135">The local virtual network.</span></span>
<span data-ttu-id="c1864-136">Wenn Sie über zwei Subnetze (10.1.0.0/16 und 10.2.0.0/16) im gleichen virtuellen Netzwerk verfügen, wählen Sie den Wert VnetLocal für jedes Subnetz aus, um es an das andere Subnetz weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="c1864-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="c1864-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c1864-137">-Confirm</span></span>
<span data-ttu-id="c1864-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c1864-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1864-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1864-139">-WhatIf</span></span>
<span data-ttu-id="c1864-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c1864-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c1864-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c1864-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1864-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1864-142">CommonParameters</span></span>
<span data-ttu-id="c1864-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1864-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1864-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1864-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1864-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c1864-145">INPUTS</span></span>

### <span data-ttu-id="c1864-146">System. String</span><span class="sxs-lookup"><span data-stu-id="c1864-146">System.String</span></span>

## <span data-ttu-id="c1864-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c1864-147">OUTPUTS</span></span>

### <span data-ttu-id="c1864-148">Microsoft. Azure. Commands. Network. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="c1864-148">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="c1864-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="c1864-149">NOTES</span></span>

## <span data-ttu-id="c1864-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c1864-150">RELATED LINKS</span></span>

[<span data-ttu-id="c1864-151">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c1864-151">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="c1864-152">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c1864-152">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="c1864-153">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c1864-153">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="c1864-154">Satz-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c1864-154">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


