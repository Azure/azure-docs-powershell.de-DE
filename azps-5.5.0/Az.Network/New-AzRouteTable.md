---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteTable.md
ms.openlocfilehash: e7e0b58dfd4ac925110c5f666bc7c360cc222983
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146852"
---
# <span data-ttu-id="1651a-101">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="1651a-101">New-AzRouteTable</span></span>

## <span data-ttu-id="1651a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1651a-102">SYNOPSIS</span></span>
<span data-ttu-id="1651a-103">Erstellt eine Routentabelle.</span><span class="sxs-lookup"><span data-stu-id="1651a-103">Creates a route table.</span></span>

## <span data-ttu-id="1651a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1651a-104">SYNTAX</span></span>

```
New-AzRouteTable -ResourceGroupName <String> -Name <String> [-DisableBgpRoutePropagation] -Location <String>
 [-Tag <Hashtable>] [-Route <PSRoute[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1651a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1651a-105">DESCRIPTION</span></span>
<span data-ttu-id="1651a-106">Das **Cmdlet "New-AzRouteTable"** erstellt eine Azure-Routentabelle.</span><span class="sxs-lookup"><span data-stu-id="1651a-106">The **New-AzRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="1651a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1651a-107">EXAMPLES</span></span>

### <span data-ttu-id="1651a-108">Beispiel 1: Erstellen einer Routentabelle, die eine Route enthält</span><span class="sxs-lookup"><span data-stu-id="1651a-108">Example 1: Create a route table that contains a route</span></span>
```
PS C:\>$Route = New-AzRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> New-AzRouteTable -Name "RouteTable01" -ResourceGroupName "ResourceGroup11" -Location "EASTUS" -Route $Route
Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/myroutetable
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              :
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null,
                        "ProvisioningState": "Succeeded"
                      }
                    ]
Subnets           : []
```

<span data-ttu-id="1651a-109">Der erste Befehl erstellt mithilfe des cmdlets "route07New-AzRouteConfig eine Route mit dem Namen "Route07" und speichert sie dann in $Route Variable.</span><span class="sxs-lookup"><span data-stu-id="1651a-109">The first command creates a route named Route07 by using the New-AzRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="1651a-110">Mit dieser Route werden Pakete an das lokale virtuelle Netzwerk weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="1651a-110">This route forwards packets to the local virtual network.</span></span>
<span data-ttu-id="1651a-111">Der zweite Befehl erstellt eine Routentabelle namens "RouteTable01" und fügt die in der Tabelle $Route gespeicherte Route der neuen Tabelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="1651a-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="1651a-112">Der Befehl gibt die Ressourcengruppe an, zu der die Tabelle gehört, und den Speicherort für die Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1651a-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="1651a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1651a-113">PARAMETERS</span></span>

### <span data-ttu-id="1651a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1651a-114">-AsJob</span></span>
<span data-ttu-id="1651a-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1651a-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1651a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1651a-116">-DefaultProfile</span></span>
<span data-ttu-id="1651a-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1651a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1651a-118">-DisableBgpRoutePropagation</span><span class="sxs-lookup"><span data-stu-id="1651a-118">-DisableBgpRoutePropagation</span></span>
<span data-ttu-id="1651a-119">Deaktivieren Sie die automatische Verteilung der BGP-Route.</span><span class="sxs-lookup"><span data-stu-id="1651a-119">Disable BGP Route auto propagation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1651a-120">-Force</span><span class="sxs-lookup"><span data-stu-id="1651a-120">-Force</span></span>
<span data-ttu-id="1651a-121">Gibt an, dass mit diesem Cmdlet eine Routentabelle erstellt wird, auch wenn bereits eine Routentabelle mit demselben Namen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1651a-121">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1651a-122">-Location</span><span class="sxs-lookup"><span data-stu-id="1651a-122">-Location</span></span>
<span data-ttu-id="1651a-123">Gibt die Azure-Region an, in der dieses Cmdlet eine Routentabelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="1651a-123">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="1651a-124">Weitere Informationen finden Sie unter ["Azure-Regionen".](http://azure.microsoft.com/en-us/regions/)</span><span class="sxs-lookup"><span data-stu-id="1651a-124">For more information, see [Azure Regions](http://azure.microsoft.com/en-us/regions/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1651a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="1651a-125">-Name</span></span>
<span data-ttu-id="1651a-126">Gibt einen Namen für die Routentabelle an.</span><span class="sxs-lookup"><span data-stu-id="1651a-126">Specifies a name for the route table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1651a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1651a-127">-ResourceGroupName</span></span>
<span data-ttu-id="1651a-128">Gibt den Namen der Ressourcengruppe an, in der dieses Cmdlet eine Routentabelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="1651a-128">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1651a-129">-Route</span><span class="sxs-lookup"><span data-stu-id="1651a-129">-Route</span></span>
<span data-ttu-id="1651a-130">Gibt ein Array von **Route-Objekten** an, die der Routentabelle zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="1651a-130">Specifies an array of **Route** objects to associate with the route table.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRoute[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1651a-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="1651a-131">-Tag</span></span>
<span data-ttu-id="1651a-132">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="1651a-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1651a-133">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="1651a-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1651a-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1651a-134">-Confirm</span></span>
<span data-ttu-id="1651a-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1651a-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1651a-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1651a-136">-WhatIf</span></span>
<span data-ttu-id="1651a-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1651a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1651a-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1651a-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1651a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1651a-139">CommonParameters</span></span>
<span data-ttu-id="1651a-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1651a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1651a-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1651a-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1651a-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1651a-142">INPUTS</span></span>

### <span data-ttu-id="1651a-143">System.String</span><span class="sxs-lookup"><span data-stu-id="1651a-143">System.String</span></span>

### <span data-ttu-id="1651a-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1651a-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1651a-145">Microsoft.Azure.Commands.Network.Models.PSRoute[]</span><span class="sxs-lookup"><span data-stu-id="1651a-145">Microsoft.Azure.Commands.Network.Models.PSRoute[]</span></span>

## <span data-ttu-id="1651a-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1651a-146">OUTPUTS</span></span>

### <span data-ttu-id="1651a-147">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="1651a-147">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="1651a-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1651a-148">NOTES</span></span>

## <span data-ttu-id="1651a-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1651a-149">RELATED LINKS</span></span>

[<span data-ttu-id="1651a-150">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="1651a-150">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="1651a-151">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1651a-151">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="1651a-152">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="1651a-152">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="1651a-153">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="1651a-153">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)
