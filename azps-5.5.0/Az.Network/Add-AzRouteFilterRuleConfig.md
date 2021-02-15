---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 204ecf05f0781649f441399c7a9b6acfbfbd8cdd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159252"
---
# <span data-ttu-id="1e9b9-101">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1e9b9-101">Add-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="1e9b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e9b9-102">SYNOPSIS</span></span>
<span data-ttu-id="1e9b9-103">Fügt einem Routenfilter eine Routenfilterregel hinzu.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-103">Adds a route filter rule to a route filter.</span></span>

## <span data-ttu-id="1e9b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1e9b9-104">SYNTAX</span></span>

```
Add-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e9b9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1e9b9-105">DESCRIPTION</span></span>
<span data-ttu-id="1e9b9-106">Das Add-AzRouteFilterRuleConfig fügt einem Azure-Routenfilter eine Routenfilterregel hinzu.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-106">The Add-AzRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="1e9b9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1e9b9-107">EXAMPLES</span></span>

### <span data-ttu-id="1e9b9-108">Beispiel 1: Hinzufügen einer Routenfilterregel zu einem Routenfilter</span><span class="sxs-lookup"><span data-stu-id="1e9b9-108">Example 1: Add a route filter rule to a route filter</span></span>
```
PS C:\>$RouteFilter = Get-AzRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="1e9b9-109">Der erste Befehl ruft einen Routenfilter namens "routefilter01" mithilfe des Get-AzRouteFilter cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-109">The first command gets a route filter named routefilter01 by using the Get-AzRouteFilter cmdlet.</span></span>
<span data-ttu-id="1e9b9-110">Der Befehl speichert den Filter in der $RouteFilter Variable.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="1e9b9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e9b9-111">PARAMETERS</span></span>

### <span data-ttu-id="1e9b9-112">-Access</span><span class="sxs-lookup"><span data-stu-id="1e9b9-112">-Access</span></span>
<span data-ttu-id="1e9b9-113">Gibt den Zugriff auf die Routenfilterregel an: Gültige Werte sind "Verweigern" oder "Zulassen".</span><span class="sxs-lookup"><span data-stu-id="1e9b9-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

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

### <span data-ttu-id="1e9b9-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="1e9b9-114">-CommunityList</span></span>
<span data-ttu-id="1e9b9-115">Die Liste des Communitywerts, nach dem der Routenfilter gefiltert wird</span><span class="sxs-lookup"><span data-stu-id="1e9b9-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="1e9b9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e9b9-116">-DefaultProfile</span></span>
<span data-ttu-id="1e9b9-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e9b9-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1e9b9-118">-Force</span></span>
<span data-ttu-id="1e9b9-119">Bestätigen Sie nicht, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="1e9b9-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="1e9b9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1e9b9-120">-Name</span></span>
<span data-ttu-id="1e9b9-121">Gibt einen Namen der Routenfilterregel an, die dem Routenfilter hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

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

### <span data-ttu-id="1e9b9-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="1e9b9-122">-RouteFilter</span></span>
<span data-ttu-id="1e9b9-123">Gibt den Routenfilter an, dem dieses Cmdlet eine Routenfilterregel hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

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

### <span data-ttu-id="1e9b9-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="1e9b9-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="1e9b9-125">Gibt den Typ der Routenfilterregel an.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="1e9b9-126">Gültige Werte sind: Community</span><span class="sxs-lookup"><span data-stu-id="1e9b9-126">Valid values are: Community</span></span>

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

### <span data-ttu-id="1e9b9-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e9b9-127">-Confirm</span></span>
<span data-ttu-id="1e9b9-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e9b9-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1e9b9-129">-WhatIf</span></span>
<span data-ttu-id="1e9b9-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1e9b9-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e9b9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e9b9-132">CommonParameters</span></span>
<span data-ttu-id="1e9b9-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e9b9-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e9b9-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e9b9-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1e9b9-135">INPUTS</span></span>

### <span data-ttu-id="1e9b9-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1e9b9-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="1e9b9-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1e9b9-137">OUTPUTS</span></span>

### <span data-ttu-id="1e9b9-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1e9b9-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="1e9b9-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1e9b9-139">NOTES</span></span>
<span data-ttu-id="1e9b9-140">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="1e9b9-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="1e9b9-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1e9b9-141">RELATED LINKS</span></span>

[<span data-ttu-id="1e9b9-142">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1e9b9-142">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1e9b9-143">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1e9b9-143">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1e9b9-144">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1e9b9-144">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1e9b9-145">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1e9b9-145">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1e9b9-146">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1e9b9-146">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="1e9b9-147">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1e9b9-147">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="1e9b9-148">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1e9b9-148">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="1e9b9-149">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1e9b9-149">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
