---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 204ecf05f0781649f441399c7a9b6acfbfbd8cdd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467440"
---
# <span data-ttu-id="b02ca-101">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b02ca-101">Add-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="b02ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b02ca-102">SYNOPSIS</span></span>
<span data-ttu-id="b02ca-103">Fügt einem Routenfilter eine Routenfilterregel hinzu.</span><span class="sxs-lookup"><span data-stu-id="b02ca-103">Adds a route filter rule to a route filter.</span></span>

## <span data-ttu-id="b02ca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b02ca-104">SYNTAX</span></span>

```
Add-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b02ca-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b02ca-105">DESCRIPTION</span></span>
<span data-ttu-id="b02ca-106">Das Add-AzRouteFilterRuleConfig fügt einem Azure-Routenfilter eine Routenfilterregel hinzu.</span><span class="sxs-lookup"><span data-stu-id="b02ca-106">The Add-AzRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="b02ca-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b02ca-107">EXAMPLES</span></span>

### <span data-ttu-id="b02ca-108">Beispiel 1: Hinzufügen einer Routenfilterregel zu einem Routenfilter</span><span class="sxs-lookup"><span data-stu-id="b02ca-108">Example 1: Add a route filter rule to a route filter</span></span>
```
PS C:\>$RouteFilter = Get-AzRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="b02ca-109">Der erste Befehl ruft einen Routenfilter namens "routefilter01" mithilfe des Get-AzRouteFilter cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="b02ca-109">The first command gets a route filter named routefilter01 by using the Get-AzRouteFilter cmdlet.</span></span>
<span data-ttu-id="b02ca-110">Der Befehl speichert den Filter in der $RouteFilter Variable.</span><span class="sxs-lookup"><span data-stu-id="b02ca-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="b02ca-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b02ca-111">PARAMETERS</span></span>

### <span data-ttu-id="b02ca-112">-Access</span><span class="sxs-lookup"><span data-stu-id="b02ca-112">-Access</span></span>
<span data-ttu-id="b02ca-113">Gibt den Zugriff auf die Routenfilterregel an: Gültige Werte sind "Verweigern" oder "Zulassen".</span><span class="sxs-lookup"><span data-stu-id="b02ca-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02ca-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="b02ca-114">-CommunityList</span></span>
<span data-ttu-id="b02ca-115">Die Liste des Communitywerts, nach dem der Routenfilter gefiltert wird</span><span class="sxs-lookup"><span data-stu-id="b02ca-115">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02ca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b02ca-116">-DefaultProfile</span></span>
<span data-ttu-id="b02ca-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b02ca-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b02ca-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b02ca-118">-Force</span></span>
<span data-ttu-id="b02ca-119">Bestätigen Sie nicht, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="b02ca-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b02ca-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b02ca-120">-Name</span></span>
<span data-ttu-id="b02ca-121">Gibt einen Namen der Routenfilterregel an, die dem Routenfilter hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b02ca-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02ca-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="b02ca-122">-RouteFilter</span></span>
<span data-ttu-id="b02ca-123">Gibt den Routenfilter an, dem dieses Cmdlet eine Routenfilterregel hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="b02ca-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b02ca-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="b02ca-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="b02ca-125">Gibt den Typ der Routenfilterregel an.</span><span class="sxs-lookup"><span data-stu-id="b02ca-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="b02ca-126">Gültige Werte sind: Community</span><span class="sxs-lookup"><span data-stu-id="b02ca-126">Valid values are: Community</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b02ca-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b02ca-127">-Confirm</span></span>
<span data-ttu-id="b02ca-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b02ca-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b02ca-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b02ca-129">-WhatIf</span></span>
<span data-ttu-id="b02ca-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b02ca-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b02ca-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b02ca-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b02ca-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b02ca-132">CommonParameters</span></span>
<span data-ttu-id="b02ca-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b02ca-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b02ca-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b02ca-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b02ca-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b02ca-135">INPUTS</span></span>

### <span data-ttu-id="b02ca-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b02ca-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="b02ca-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b02ca-137">OUTPUTS</span></span>

### <span data-ttu-id="b02ca-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b02ca-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="b02ca-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b02ca-139">NOTES</span></span>
<span data-ttu-id="b02ca-140">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="b02ca-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="b02ca-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b02ca-141">RELATED LINKS</span></span>

[<span data-ttu-id="b02ca-142">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b02ca-142">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b02ca-143">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b02ca-143">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b02ca-144">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b02ca-144">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b02ca-145">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b02ca-145">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b02ca-146">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b02ca-146">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="b02ca-147">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b02ca-147">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="b02ca-148">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b02ca-148">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="b02ca-149">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b02ca-149">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
