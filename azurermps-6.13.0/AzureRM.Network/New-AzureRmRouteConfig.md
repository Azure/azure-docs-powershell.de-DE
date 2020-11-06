---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteConfig.md
ms.openlocfilehash: ba5a389bd726822c24931fecb631f6c70cf7ce48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495886"
---
# <span data-ttu-id="30d09-101">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="30d09-101">New-AzureRmRouteConfig</span></span>

## <span data-ttu-id="30d09-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="30d09-102">SYNOPSIS</span></span>
<span data-ttu-id="30d09-103">Erstellt eine Route für eine Routentabelle.</span><span class="sxs-lookup"><span data-stu-id="30d09-103">Creates a route for a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30d09-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="30d09-104">SYNTAX</span></span>

```
New-AzureRmRouteConfig [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="30d09-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="30d09-105">DESCRIPTION</span></span>
<span data-ttu-id="30d09-106">Das Cmdlet **New-AzureRmRouteConfig** erstellt eine Route für eine Azure Route-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="30d09-106">The **New-AzureRmRouteConfig** cmdlet creates a route for an Azure route table.</span></span>

## <span data-ttu-id="30d09-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="30d09-107">EXAMPLES</span></span>

### <span data-ttu-id="30d09-108">Beispiel 1: Erstellen einer Route</span><span class="sxs-lookup"><span data-stu-id="30d09-108">Example 1: Create a route</span></span>
```
PS C:\>$Route = New-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> $Route
Name              : Route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="30d09-109">Der erste Befehl erstellt eine Route mit dem Namen Route07 und speichert Sie dann in der $Route-Variablen.</span><span class="sxs-lookup"><span data-stu-id="30d09-109">The first command creates a route named Route07, and then stores it in the $Route variable.</span></span>
<span data-ttu-id="30d09-110">Diese Route leitet Pakete an das lokale virtuelle Netzwerk weiter.</span><span class="sxs-lookup"><span data-stu-id="30d09-110">This route forwards packets to the local virtual network.</span></span>
<span data-ttu-id="30d09-111">Mit dem zweiten Befehl werden die Eigenschaften der Route angezeigt.</span><span class="sxs-lookup"><span data-stu-id="30d09-111">The second command displays the properties of the route.</span></span>

## <span data-ttu-id="30d09-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="30d09-112">PARAMETERS</span></span>

### <span data-ttu-id="30d09-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="30d09-113">-AddressPrefix</span></span>
<span data-ttu-id="30d09-114">Gibt das Ziel im CIDR-Format (klassenlos InterDomain Routing) an, auf das die Route angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="30d09-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="30d09-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30d09-115">-DefaultProfile</span></span>
<span data-ttu-id="30d09-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="30d09-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30d09-117">-Name</span><span class="sxs-lookup"><span data-stu-id="30d09-117">-Name</span></span>
<span data-ttu-id="30d09-118">Gibt einen Namen für die Route an.</span><span class="sxs-lookup"><span data-stu-id="30d09-118">Specifies a name for the route.</span></span>

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

### <span data-ttu-id="30d09-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="30d09-119">-NextHopIpAddress</span></span>
<span data-ttu-id="30d09-120">Gibt die IP-Adresse einer virtuellen Appliance an, die Sie Ihrem Azurevirtual-Netzwerk hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="30d09-120">Specifies the IP address of a virtual appliance that you add to your Azurevirtual network.</span></span>
<span data-ttu-id="30d09-121">Diese Route leitet Pakete an diese Adresse weiter.</span><span class="sxs-lookup"><span data-stu-id="30d09-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="30d09-122">Geben Sie diesen Parameter nur an, wenn Sie einen Wert von VirtualAppliance für den *NextHopType* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="30d09-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="30d09-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="30d09-123">-NextHopType</span></span>
<span data-ttu-id="30d09-124">Gibt an, wie Pakete von dieser Route weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="30d09-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="30d09-125">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="30d09-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="30d09-126">Internet.</span><span class="sxs-lookup"><span data-stu-id="30d09-126">Internet.</span></span>
<span data-ttu-id="30d09-127">Das standardmäßige Internet Gateway, das von Azure bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="30d09-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="30d09-128">Keine.</span><span class="sxs-lookup"><span data-stu-id="30d09-128">None.</span></span>
<span data-ttu-id="30d09-129">Wenn Sie diesen Wert angeben, leitet die Route keine Pakete weiter.</span><span class="sxs-lookup"><span data-stu-id="30d09-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="30d09-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="30d09-130">VirtualAppliance.</span></span>
<span data-ttu-id="30d09-131">Eine virtuelle Appliance, die Sie Ihrem virtuellen Azure-Netzwerk hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="30d09-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="30d09-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="30d09-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="30d09-133">Ein Azure Server-zu-Server-virtuelles privates Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="30d09-133">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="30d09-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="30d09-134">VnetLocal.</span></span>
<span data-ttu-id="30d09-135">Lokales virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="30d09-135">The local virtual network.</span></span>
<span data-ttu-id="30d09-136">Wenn Sie über zwei Subnetze (10.1.0.0/16 und 10.2.0.0/16) im gleichen virtuellen Netzwerk verfügen, wählen Sie den Wert VnetLocal für jedes Subnetz aus, um es an das andere Subnetz weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="30d09-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="30d09-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="30d09-137">-Confirm</span></span>
<span data-ttu-id="30d09-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="30d09-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30d09-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30d09-139">-WhatIf</span></span>
<span data-ttu-id="30d09-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="30d09-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30d09-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="30d09-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30d09-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30d09-142">CommonParameters</span></span>
<span data-ttu-id="30d09-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30d09-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30d09-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30d09-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30d09-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="30d09-145">INPUTS</span></span>

### <span data-ttu-id="30d09-146">System. String</span><span class="sxs-lookup"><span data-stu-id="30d09-146">System.String</span></span>

## <span data-ttu-id="30d09-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="30d09-147">OUTPUTS</span></span>

### <span data-ttu-id="30d09-148">Microsoft. Azure. Commands. Network. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="30d09-148">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="30d09-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="30d09-149">NOTES</span></span>

## <span data-ttu-id="30d09-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="30d09-150">RELATED LINKS</span></span>

[<span data-ttu-id="30d09-151">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="30d09-151">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="30d09-152">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="30d09-152">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="30d09-153">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="30d09-153">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="30d09-154">Satz-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="30d09-154">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


