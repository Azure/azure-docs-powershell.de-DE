---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteConfig.md
ms.openlocfilehash: e48da3a5f300d39051a9d1b07e9789855ed7dca1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941515"
---
# <span data-ttu-id="2fa53-101">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="2fa53-101">Remove-AzRouteConfig</span></span>

## <span data-ttu-id="2fa53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fa53-102">SYNOPSIS</span></span>
<span data-ttu-id="2fa53-103">Entfernt eine Route aus einer Routentabelle.</span><span class="sxs-lookup"><span data-stu-id="2fa53-103">Removes a route from a route table.</span></span>

## <span data-ttu-id="2fa53-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2fa53-104">SYNTAX</span></span>

```
Remove-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fa53-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2fa53-105">DESCRIPTION</span></span>
<span data-ttu-id="2fa53-106">Das **Cmdlet Remove-AzRouteConfig** entfernt eine Route aus einer Azure-Routentabelle.</span><span class="sxs-lookup"><span data-stu-id="2fa53-106">The **Remove-AzRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="2fa53-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2fa53-107">EXAMPLES</span></span>

### <span data-ttu-id="2fa53-108">Beispiel 1: Entfernen einer Route</span><span class="sxs-lookup"><span data-stu-id="2fa53-108">Example 1: Remove a route</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Remove-AzRouteConfig -Name "Route02" | Set-AzRouteTable
Name              : RouteTable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"47099b62-60ec-4bc1-b87b-fad56cb8bed1"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"47099b62-60ec-4bc1-b87b-fad56cb8bed1\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="2fa53-109">Dieser Befehl ruft die Routentabelle mit dem Namen RouteTable01 mithilfe des **Get-AzRouteTable-Cmdlets** ab.</span><span class="sxs-lookup"><span data-stu-id="2fa53-109">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="2fa53-110">Der Befehl übergibt diese Tabelle mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fa53-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2fa53-111">Das aktuelle Cmdlet entfernt die Route mit dem Namen Route02, und das -Cmdlet übergibt das Ergebnis an das **Set-AzRouteTable-Cmdlet,** das die Tabelle aktualisiert, um Ihre Änderungen widerspiegeln zu können.</span><span class="sxs-lookup"><span data-stu-id="2fa53-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="2fa53-112">Die Tabelle enthält nicht mehr die Route mit dem Namen Route02.</span><span class="sxs-lookup"><span data-stu-id="2fa53-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="2fa53-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2fa53-113">PARAMETERS</span></span>

### <span data-ttu-id="2fa53-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fa53-114">-DefaultProfile</span></span>
<span data-ttu-id="2fa53-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2fa53-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fa53-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2fa53-116">-Name</span></span>
<span data-ttu-id="2fa53-117">Gibt den Namen der Route an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="2fa53-117">Specifies the name of the route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2fa53-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="2fa53-118">-RouteTable</span></span>
<span data-ttu-id="2fa53-119">Gibt die Routentabelle an, die die Route enthält, die von diesem Cmdlet gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="2fa53-119">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2fa53-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2fa53-120">-Confirm</span></span>
<span data-ttu-id="2fa53-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2fa53-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fa53-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fa53-122">-WhatIf</span></span>
<span data-ttu-id="2fa53-123">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2fa53-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2fa53-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2fa53-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fa53-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fa53-125">CommonParameters</span></span>
<span data-ttu-id="2fa53-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fa53-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fa53-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fa53-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fa53-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2fa53-128">INPUTS</span></span>

### <span data-ttu-id="2fa53-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="2fa53-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="2fa53-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2fa53-130">OUTPUTS</span></span>

### <span data-ttu-id="2fa53-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="2fa53-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="2fa53-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2fa53-132">NOTES</span></span>

## <span data-ttu-id="2fa53-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2fa53-133">RELATED LINKS</span></span>

[<span data-ttu-id="2fa53-134">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="2fa53-134">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="2fa53-135">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="2fa53-135">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="2fa53-136">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="2fa53-136">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="2fa53-137">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="2fa53-137">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


