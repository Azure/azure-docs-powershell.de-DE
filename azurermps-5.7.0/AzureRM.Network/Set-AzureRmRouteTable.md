---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE2A30A-6DF8-4C4C-8348-C3C1CD4D0146
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteTable.md
ms.openlocfilehash: 6848b00d090b8d365b0c26fb3948a4eec3ad047d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505438"
---
# <span data-ttu-id="c8343-101">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="c8343-101">Set-AzureRmRouteTable</span></span>

## <span data-ttu-id="c8343-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c8343-102">SYNOPSIS</span></span>
<span data-ttu-id="c8343-103">Legt den Zielstatus für eine Routentabelle fest.</span><span class="sxs-lookup"><span data-stu-id="c8343-103">Sets the goal state for a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8343-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8343-104">SYNTAX</span></span>

```
Set-AzureRmRouteTable -RouteTable <PSRouteTable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8343-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8343-105">DESCRIPTION</span></span>
<span data-ttu-id="c8343-106">Das Cmdlet " **Set-AzureRmRouteTable** " legt den Zielstatus für eine Azure Route-Tabelle fest.</span><span class="sxs-lookup"><span data-stu-id="c8343-106">The **Set-AzureRmRouteTable** cmdlet sets the goal state for an Azure route table.</span></span>

## <span data-ttu-id="c8343-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c8343-107">EXAMPLES</span></span>

### <span data-ttu-id="c8343-108">Beispiel 1: Hinzufügen einer Route und anschließendes setzen des Zielzustands der Route-Tabelle</span><span class="sxs-lookup"><span data-stu-id="c8343-108">Example 1: Add a route and then set the goal state of the route table</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.2.0.0/16 -NextHopType "VnetLocal" | Set-AzureRmRouteTable
Name              : RouteTable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"f13e1bc8-d41f-44d0-882d-b8b5a1134f59"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/RouteTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "Route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/RouteTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.2.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "Route13",
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

<span data-ttu-id="c8343-109">Dieser Befehl ruft die Routingtabelle mit dem Namen RouteTable01 mithilfe Get-AzureRmRouteTable-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="c8343-109">This command gets the route table named RouteTable01 by using Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="c8343-110">Der Befehl übergibt diese Tabelle mithilfe des Pipelineoperators an das Add-AzureRmRouteConfig-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8343-110">The command passes that table to the Add-AzureRmRouteConfig cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c8343-111">**Add-AzureRmRouteConfig** fügt die Route mit dem Namen Route07 hinzu und übergibt dann das Ergebnis an das aktuelle Cmdlet, das die Tabelle so aktualisiert, dass Sie Ihre Änderungen widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="c8343-111">**Add-AzureRmRouteConfig** adds the route named Route07, and then passes the result to the current cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="c8343-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8343-112">PARAMETERS</span></span>

### <span data-ttu-id="c8343-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8343-113">-AsJob</span></span>
<span data-ttu-id="c8343-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c8343-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c8343-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8343-115">-DefaultProfile</span></span>
<span data-ttu-id="c8343-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c8343-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8343-117">-Routel</span><span class="sxs-lookup"><span data-stu-id="c8343-117">-RouteTable</span></span>
<span data-ttu-id="c8343-118">Gibt ein Routingtabellen Objekt an, das den Zielzustand darstellt, in den dieses Cmdlet die Route-Tabelle festlegt.</span><span class="sxs-lookup"><span data-stu-id="c8343-118">Specifies a route table object that represents the goal state to which this cmdlet sets the route table.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8343-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c8343-119">-Confirm</span></span>
<span data-ttu-id="c8343-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c8343-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8343-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8343-121">-WhatIf</span></span>
<span data-ttu-id="c8343-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c8343-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8343-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c8343-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8343-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8343-124">CommonParameters</span></span>
<span data-ttu-id="c8343-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8343-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8343-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8343-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8343-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c8343-127">INPUTS</span></span>

### <span data-ttu-id="c8343-128">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="c8343-128">PSRouteTable</span></span>
<span data-ttu-id="c8343-129">Der Parameter "routeable" akzeptiert den Wert vom Typ "PSRouteTable" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c8343-129">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="c8343-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c8343-130">OUTPUTS</span></span>

### <span data-ttu-id="c8343-131">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="c8343-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="c8343-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="c8343-132">NOTES</span></span>

## <span data-ttu-id="c8343-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c8343-133">RELATED LINKS</span></span>

[<span data-ttu-id="c8343-134">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c8343-134">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="c8343-135">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="c8343-135">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="c8343-136">Neu – AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="c8343-136">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="c8343-137">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="c8343-137">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)


