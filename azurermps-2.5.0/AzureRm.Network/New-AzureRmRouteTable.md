---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutetable
schema: 2.0.0
ms.openlocfilehash: 9ba23a33e82e003413172240264ef8485b12d4e0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850372"
---
# <span data-ttu-id="f872e-101">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="f872e-101">New-AzureRmRouteTable</span></span>

## <span data-ttu-id="f872e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f872e-102">SYNOPSIS</span></span>
<span data-ttu-id="f872e-103">Erstellt eine Routentabelle.</span><span class="sxs-lookup"><span data-stu-id="f872e-103">Creates a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f872e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f872e-104">SYNTAX</span></span>

```
New-AzureRmRouteTable -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Route <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f872e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f872e-105">DESCRIPTION</span></span>
<span data-ttu-id="f872e-106">Das Cmdlet **New-AzureRmRouteTable** erstellt eine Azure Route-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="f872e-106">The **New-AzureRmRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="f872e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f872e-107">EXAMPLES</span></span>

### <span data-ttu-id="f872e-108">Beispiel 1: Erstellen einer Arbeitsplan Tabelle, die eine Route enthält</span><span class="sxs-lookup"><span data-stu-id="f872e-108">Example 1: Create a route table that contains a route</span></span>
```
PS C:\>$Route = New-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> New-AzureRmRouteTable -Name "RouteTable01" -ResourceGroupName "ResourceGroup11" -Location "EASTUS" -Route $Route
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

<span data-ttu-id="f872e-109">Der erste Befehl erstellt eine Route mit dem Namen Route07 mithilfe des New-AzureRmRouteConfig-Cmdlets und speichert Sie dann in der $Route-Variablen.</span><span class="sxs-lookup"><span data-stu-id="f872e-109">The first command creates a route named Route07 by using the New-AzureRmRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="f872e-110">Diese Route leitet Pakete an das lokale virtuelle Netzwerk weiter.</span><span class="sxs-lookup"><span data-stu-id="f872e-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="f872e-111">Mit dem zweiten Befehl wird eine Routentabelle mit dem Namen RouteTable01 erstellt, und die in $Route gespeicherte Route wird der neuen Tabelle hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f872e-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="f872e-112">Der Befehl gibt die Ressourcengruppe an, zu der die Tabelle gehört, und den Speicherort für die Tabelle.</span><span class="sxs-lookup"><span data-stu-id="f872e-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="f872e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f872e-113">PARAMETERS</span></span>

### <span data-ttu-id="f872e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f872e-114">-AsJob</span></span>
<span data-ttu-id="f872e-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f872e-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f872e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f872e-116">-DefaultProfile</span></span>
<span data-ttu-id="f872e-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f872e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f872e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f872e-118">-Force</span></span>
<span data-ttu-id="f872e-119">Gibt an, dass dieses Cmdlet eine Route-Tabelle erstellt, auch wenn bereits eine Route-Tabelle mit dem gleichen Namen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f872e-119">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f872e-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="f872e-120">-Location</span></span>
<span data-ttu-id="f872e-121">Gibt den Azure-Bereich an, in dem dieses Cmdlet eine Routentabelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="f872e-121">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="f872e-122">Weitere Informationen finden Sie unter [Azure-Bereiche](https://azure.microsoft.com/en-us/regions/).</span><span class="sxs-lookup"><span data-stu-id="f872e-122">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions/).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f872e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f872e-123">-Name</span></span>
<span data-ttu-id="f872e-124">Gibt einen Namen für die Route-Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="f872e-124">Specifies a name for the route table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f872e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f872e-125">-ResourceGroupName</span></span>
<span data-ttu-id="f872e-126">Gibt den Namen der Ressourcengruppe an, in der mit diesem Cmdlet eine Routentabelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f872e-126">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f872e-127">-Route</span><span class="sxs-lookup"><span data-stu-id="f872e-127">-Route</span></span>
<span data-ttu-id="f872e-128">Gibt ein Array von **Route** -Objekten an, die der Route-Tabelle zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f872e-128">Specifies an array of **Route** objects to associate with the route table.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f872e-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="f872e-129">-Tag</span></span>
<span data-ttu-id="f872e-130">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="f872e-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f872e-131">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="f872e-131">For example:</span></span>

<span data-ttu-id="f872e-132">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="f872e-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f872e-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f872e-133">-Confirm</span></span>
<span data-ttu-id="f872e-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f872e-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f872e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f872e-135">-WhatIf</span></span>
<span data-ttu-id="f872e-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f872e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f872e-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f872e-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f872e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f872e-138">CommonParameters</span></span>
<span data-ttu-id="f872e-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f872e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f872e-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f872e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f872e-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f872e-141">INPUTS</span></span>

## <span data-ttu-id="f872e-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f872e-142">OUTPUTS</span></span>

### <span data-ttu-id="f872e-143">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="f872e-143">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="f872e-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="f872e-144">NOTES</span></span>

## <span data-ttu-id="f872e-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f872e-145">RELATED LINKS</span></span>

[<span data-ttu-id="f872e-146">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="f872e-146">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="f872e-147">Neu – AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f872e-147">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="f872e-148">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="f872e-148">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="f872e-149">Satz-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="f872e-149">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)
