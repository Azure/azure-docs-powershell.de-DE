---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE2A30A-6DF8-4C4C-8348-C3C1CD4D0146
online version: https://docs.microsoft.com/powershell/module/az.network/set-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteTable.md
ms.openlocfilehash: 6bd40f09089b9030e50d30e7155d13b85b7978a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947771"
---
# <span data-ttu-id="f3ddd-101">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="f3ddd-101">Set-AzRouteTable</span></span>

## <span data-ttu-id="f3ddd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3ddd-102">SYNOPSIS</span></span>
<span data-ttu-id="f3ddd-103">Aktualisiert eine Routentabelle.</span><span class="sxs-lookup"><span data-stu-id="f3ddd-103">Updates a route table.</span></span>

## <span data-ttu-id="f3ddd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f3ddd-104">SYNTAX</span></span>

```
Set-AzRouteTable -RouteTable <PSRouteTable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3ddd-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f3ddd-105">DESCRIPTION</span></span>
<span data-ttu-id="f3ddd-106">Das **Cmdlet Set-AzRouteTable** aktualisiert eine Routentabelle.</span><span class="sxs-lookup"><span data-stu-id="f3ddd-106">The **Set-AzRouteTable** cmdlet updates a route table.</span></span>

## <span data-ttu-id="f3ddd-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f3ddd-107">EXAMPLES</span></span>

### <span data-ttu-id="f3ddd-108">Beispiel 1: Aktualisieren einer Routentabelle durch Hinzufügen einer Routenkonfiguration</span><span class="sxs-lookup"><span data-stu-id="f3ddd-108">Example 1: Update a route table by adding route configuration to it</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzRouteConfig -Name "Route07" -AddressPrefix 10.2.0.0/16 -NextHopType "VnetLocal" | Set-AzRouteTable
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

<span data-ttu-id="f3ddd-109">Dieser Befehl ruft die Routentabelle mit dem Namen RouteTable01 ab, indem Get-AzRouteTable cmdlet verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f3ddd-109">This command gets the route table named RouteTable01 by using Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="f3ddd-110">Der Befehl übergibt diese Tabelle mithilfe des Pipelineoperators an Add-AzRouteConfig-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3ddd-110">The command passes that table to the Add-AzRouteConfig cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f3ddd-111">**Add-AzRouteConfig** fügt die Route mit dem Namen Route07 hinzu und übergibt das Ergebnis dann an das aktuelle Cmdlet, das die Tabelle aktualisiert, um Ihre Änderungen widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="f3ddd-111">**Add-AzRouteConfig** adds the route named Route07, and then passes the result to the current cmdlet, which updates the table to reflect your changes.</span></span>

### <span data-ttu-id="f3ddd-112">Beispiel 2: Ändern der Routentabelle</span><span class="sxs-lookup"><span data-stu-id="f3ddd-112">Example 2: Modify route table</span></span>

```
PS C:\> $rt = Get-AzRouteTable -ResourceGroupName "rgName" -Name "rtName"
PS C:\> $rt.DisableBgpRoutePropagation
False
PS C:\> $rt.DisableBgpRoutePropagation = $true
PS C:\> Set-AzRouteTable -RouteTable $rt
PS C:\> $rt = Get-AzRouteTable -ResourceGroupName "rgName" -Name "rtName"
PS C:\> $rt.DisableBgpRoutePropagation
True
```

<span data-ttu-id="f3ddd-113">Der erste Befehl ruft die Routentabelle mit dem Namen "rtName" ab und speichert sie in $rt Variablen.</span><span class="sxs-lookup"><span data-stu-id="f3ddd-113">The first command gets the route table named rtName and stores it in the $rt variable.</span></span>
<span data-ttu-id="f3ddd-114">Der zweite Befehl zeigt den Wert DisableBgpRoutePropagation an.</span><span class="sxs-lookup"><span data-stu-id="f3ddd-114">The second command displays the value of DisableBgpRoutePropagation.</span></span>
<span data-ttu-id="f3ddd-115">Der dritte Befehl aktualisiert den Wert von DisableBgpRoutePropagation.</span><span class="sxs-lookup"><span data-stu-id="f3ddd-115">The third command updates value of DisableBgpRoutePropagation.</span></span>
<span data-ttu-id="f3ddd-116">Der vierte Befehl aktualisiert die Routentabelle auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="f3ddd-116">The fourth command updates route table on the server.</span></span>
<span data-ttu-id="f3ddd-117">Der fünfte Befehl wird aktualisiert und in der Variablen $rt gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f3ddd-117">The fifth command gets updated route table and stores it in the $rt variable.</span></span>
<span data-ttu-id="f3ddd-118">Der sechste Befehl zeigt den Wert DisableBgpRoutePropagation an.</span><span class="sxs-lookup"><span data-stu-id="f3ddd-118">The sixth command displays the value of DisableBgpRoutePropagation.</span></span>

## <span data-ttu-id="f3ddd-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f3ddd-119">PARAMETERS</span></span>

### <span data-ttu-id="f3ddd-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3ddd-120">-AsJob</span></span>
<span data-ttu-id="f3ddd-121">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f3ddd-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f3ddd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3ddd-122">-DefaultProfile</span></span>
<span data-ttu-id="f3ddd-123">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3ddd-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3ddd-124">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="f3ddd-124">-RouteTable</span></span>
<span data-ttu-id="f3ddd-125">Gibt ein Routentabelle-Objekt an, das den Zustand darstellt, auf den die Routentabelle festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f3ddd-125">Specifies a route table object representing the state to which the route table should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ddd-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f3ddd-126">-Confirm</span></span>
<span data-ttu-id="f3ddd-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f3ddd-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3ddd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3ddd-128">-WhatIf</span></span>
<span data-ttu-id="f3ddd-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f3ddd-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3ddd-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f3ddd-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3ddd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3ddd-131">CommonParameters</span></span>
<span data-ttu-id="f3ddd-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3ddd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3ddd-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3ddd-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3ddd-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f3ddd-134">INPUTS</span></span>

### <span data-ttu-id="f3ddd-135">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="f3ddd-135">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="f3ddd-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f3ddd-136">OUTPUTS</span></span>

### <span data-ttu-id="f3ddd-137">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="f3ddd-137">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="f3ddd-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f3ddd-138">NOTES</span></span>

## <span data-ttu-id="f3ddd-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f3ddd-139">RELATED LINKS</span></span>

[<span data-ttu-id="f3ddd-140">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f3ddd-140">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="f3ddd-141">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="f3ddd-141">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="f3ddd-142">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="f3ddd-142">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="f3ddd-143">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="f3ddd-143">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)


