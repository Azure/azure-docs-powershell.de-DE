---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteTable.md
ms.openlocfilehash: e7e0b58dfd4ac925110c5f666bc7c360cc222983
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009102"
---
# <span data-ttu-id="0e3fb-101">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="0e3fb-101">New-AzRouteTable</span></span>

## <span data-ttu-id="0e3fb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0e3fb-102">SYNOPSIS</span></span>
<span data-ttu-id="0e3fb-103">Erstellt eine Routentabelle.</span><span class="sxs-lookup"><span data-stu-id="0e3fb-103">Creates a route table.</span></span>

## <span data-ttu-id="0e3fb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e3fb-104">SYNTAX</span></span>

```
New-AzRouteTable -ResourceGroupName <String> -Name <String> [-DisableBgpRoutePropagation] -Location <String>
 [-Tag <Hashtable>] [-Route <PSRoute[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e3fb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e3fb-105">DESCRIPTION</span></span>
<span data-ttu-id="0e3fb-106">Das Cmdlet **New-AzRouteTable** erstellt eine Azure Route-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="0e3fb-106">The **New-AzRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="0e3fb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0e3fb-107">EXAMPLES</span></span>

### <span data-ttu-id="0e3fb-108">Beispiel 1: Erstellen einer Arbeitsplan Tabelle, die eine Route enthält</span><span class="sxs-lookup"><span data-stu-id="0e3fb-108">Example 1: Create a route table that contains a route</span></span>
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

<span data-ttu-id="0e3fb-109">Der erste Befehl erstellt eine Route mit dem Namen Route07 mithilfe des New-AzRouteConfig-Cmdlets und speichert Sie dann in der $Route-Variablen.</span><span class="sxs-lookup"><span data-stu-id="0e3fb-109">The first command creates a route named Route07 by using the New-AzRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="0e3fb-110">Diese Route leitet Pakete an das lokale virtuelle Netzwerk weiter.</span><span class="sxs-lookup"><span data-stu-id="0e3fb-110">This route forwards packets to the local virtual network.</span></span>
<span data-ttu-id="0e3fb-111">Mit dem zweiten Befehl wird eine Routentabelle mit dem Namen RouteTable01 erstellt, und die in $Route gespeicherte Route wird der neuen Tabelle hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0e3fb-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="0e3fb-112">Der Befehl gibt die Ressourcengruppe an, zu der die Tabelle gehört, und den Speicherort für die Tabelle.</span><span class="sxs-lookup"><span data-stu-id="0e3fb-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="0e3fb-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e3fb-113">PARAMETERS</span></span>

### <span data-ttu-id="0e3fb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e3fb-114">-AsJob</span></span>
<span data-ttu-id="0e3fb-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0e3fb-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0e3fb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e3fb-116">-DefaultProfile</span></span>
<span data-ttu-id="0e3fb-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0e3fb-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e3fb-118">-DisableBgpRoutePropagation</span><span class="sxs-lookup"><span data-stu-id="0e3fb-118">-DisableBgpRoutePropagation</span></span>
<span data-ttu-id="0e3fb-119">Deaktivieren Sie die Automatische Propagierung der BGP-Route.</span><span class="sxs-lookup"><span data-stu-id="0e3fb-119">Disable BGP Route auto propagation.</span></span>

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

### <span data-ttu-id="0e3fb-120">-Force</span><span class="sxs-lookup"><span data-stu-id="0e3fb-120">-Force</span></span>
<span data-ttu-id="0e3fb-121">Gibt an, dass dieses Cmdlet eine Route-Tabelle erstellt, auch wenn bereits eine Route-Tabelle mit dem gleichen Namen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0e3fb-121">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

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

### <span data-ttu-id="0e3fb-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="0e3fb-122">-Location</span></span>
<span data-ttu-id="0e3fb-123">Gibt den Azure-Bereich an, in dem dieses Cmdlet eine Routentabelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="0e3fb-123">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="0e3fb-124">Weitere Informationen finden Sie unter [Azure-Bereiche](http://azure.microsoft.com/en-us/regions/).</span><span class="sxs-lookup"><span data-stu-id="0e3fb-124">For more information, see [Azure Regions](http://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="0e3fb-125">-Name</span><span class="sxs-lookup"><span data-stu-id="0e3fb-125">-Name</span></span>
<span data-ttu-id="0e3fb-126">Gibt einen Namen für die Route-Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="0e3fb-126">Specifies a name for the route table.</span></span>

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

### <span data-ttu-id="0e3fb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e3fb-127">-ResourceGroupName</span></span>
<span data-ttu-id="0e3fb-128">Gibt den Namen der Ressourcengruppe an, in der mit diesem Cmdlet eine Routentabelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0e3fb-128">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

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

### <span data-ttu-id="0e3fb-129">-Route</span><span class="sxs-lookup"><span data-stu-id="0e3fb-129">-Route</span></span>
<span data-ttu-id="0e3fb-130">Gibt ein Array von **Route** -Objekten an, die der Route-Tabelle zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0e3fb-130">Specifies an array of **Route** objects to associate with the route table.</span></span>

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

### <span data-ttu-id="0e3fb-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="0e3fb-131">-Tag</span></span>
<span data-ttu-id="0e3fb-132">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="0e3fb-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0e3fb-133">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="0e3fb-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0e3fb-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0e3fb-134">-Confirm</span></span>
<span data-ttu-id="0e3fb-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0e3fb-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e3fb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e3fb-136">-WhatIf</span></span>
<span data-ttu-id="0e3fb-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0e3fb-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e3fb-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0e3fb-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e3fb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e3fb-139">CommonParameters</span></span>
<span data-ttu-id="0e3fb-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e3fb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e3fb-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e3fb-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e3fb-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0e3fb-142">INPUTS</span></span>

### <span data-ttu-id="0e3fb-143">System. String</span><span class="sxs-lookup"><span data-stu-id="0e3fb-143">System.String</span></span>

### <span data-ttu-id="0e3fb-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0e3fb-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0e3fb-145">Microsoft. Azure. Commands. Network. Models. PSRoute []</span><span class="sxs-lookup"><span data-stu-id="0e3fb-145">Microsoft.Azure.Commands.Network.Models.PSRoute[]</span></span>

## <span data-ttu-id="0e3fb-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0e3fb-146">OUTPUTS</span></span>

### <span data-ttu-id="0e3fb-147">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="0e3fb-147">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="0e3fb-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="0e3fb-148">NOTES</span></span>

## <span data-ttu-id="0e3fb-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0e3fb-149">RELATED LINKS</span></span>

[<span data-ttu-id="0e3fb-150">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="0e3fb-150">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="0e3fb-151">Neu – AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="0e3fb-151">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="0e3fb-152">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="0e3fb-152">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="0e3fb-153">Satz-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="0e3fb-153">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)
