---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
ms.openlocfilehash: a58a6216d49539d4fc40f9c9131a335f7a31b87f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938528"
---
# <span data-ttu-id="1104a-101">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1104a-101">Set-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="1104a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1104a-102">SYNOPSIS</span></span>
<span data-ttu-id="1104a-103">Ändert die Routenfilterregel eines Routenfilters.</span><span class="sxs-lookup"><span data-stu-id="1104a-103">Modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="1104a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1104a-104">SYNTAX</span></span>

```
Set-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1104a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1104a-105">DESCRIPTION</span></span>
<span data-ttu-id="1104a-106">Das **Cmdlet Set-AzRouteFilterRuleConfig** ändert die Routenfilterregel eines Routenfilters.</span><span class="sxs-lookup"><span data-stu-id="1104a-106">The **Set-AzRouteFilterRuleConfig** cmdlet modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="1104a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1104a-107">EXAMPLES</span></span>

### <span data-ttu-id="1104a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1104a-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> $rf = Set-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01" -Access Deny -RouteFilterRuleType Community -CommunityList "12076:5010","12076:5040"
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="1104a-109">Der erste Befehl ruft den Routenfilter mit dem Namen RouteFilter01 ab und speichert ihn in der $rf Variablen.</span><span class="sxs-lookup"><span data-stu-id="1104a-109">The first command gets the route filter named RouteFilter01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="1104a-110">Der zweite Befehl ändert die Routenfilterregel mit dem Namen Regel01 und speichert den aktualisierten Routenfilter in $rf Variablen.</span><span class="sxs-lookup"><span data-stu-id="1104a-110">The second command modifies the route filter rule named Rule01 and stores updated route filter in the $rf variable.</span></span>
<span data-ttu-id="1104a-111">Der dritte Befehl speichert den aktualisierten Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="1104a-111">The third command saves updated route filter.</span></span>

## <span data-ttu-id="1104a-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1104a-112">PARAMETERS</span></span>

### <span data-ttu-id="1104a-113">-Access</span><span class="sxs-lookup"><span data-stu-id="1104a-113">-Access</span></span>
<span data-ttu-id="1104a-114">Der Zugriffstyp der Regel.</span><span class="sxs-lookup"><span data-stu-id="1104a-114">The access type of the rule.</span></span>
<span data-ttu-id="1104a-115">Mögliche Werte sind: "Zulassen", "Verweigern"</span><span class="sxs-lookup"><span data-stu-id="1104a-115">Possible values are: 'Allow', 'Deny'</span></span>

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

### <span data-ttu-id="1104a-116">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="1104a-116">-CommunityList</span></span>
<span data-ttu-id="1104a-117">Die Liste des Communitywerts, nach dem der Routenfilter gefiltert wird</span><span class="sxs-lookup"><span data-stu-id="1104a-117">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="1104a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1104a-118">-DefaultProfile</span></span>
<span data-ttu-id="1104a-119">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1104a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1104a-120">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="1104a-120">-Force</span></span>
<span data-ttu-id="1104a-121">Bitten Sie nicht um Bestätigung, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="1104a-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="1104a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1104a-122">-Name</span></span>
<span data-ttu-id="1104a-123">Der Name der Routenfilterregel</span><span class="sxs-lookup"><span data-stu-id="1104a-123">The name of the route filter rule</span></span>

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

### <span data-ttu-id="1104a-124">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="1104a-124">-RouteFilter</span></span>
<span data-ttu-id="1104a-125">Der RouteFilter</span><span class="sxs-lookup"><span data-stu-id="1104a-125">The RouteFilter</span></span>

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

### <span data-ttu-id="1104a-126">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="1104a-126">-RouteFilterRuleType</span></span>
<span data-ttu-id="1104a-127">Der Typ der Routefilterregel der Regel.</span><span class="sxs-lookup"><span data-stu-id="1104a-127">The route filter rule type of the rule.</span></span>
<span data-ttu-id="1104a-128">Mögliche Werte sind: "Community"</span><span class="sxs-lookup"><span data-stu-id="1104a-128">Possible values are: 'Community'</span></span>

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

### <span data-ttu-id="1104a-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1104a-129">-Confirm</span></span>
<span data-ttu-id="1104a-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1104a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1104a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1104a-131">-WhatIf</span></span>
<span data-ttu-id="1104a-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1104a-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1104a-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1104a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1104a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1104a-134">CommonParameters</span></span>
<span data-ttu-id="1104a-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1104a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1104a-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1104a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1104a-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1104a-137">INPUTS</span></span>

### <span data-ttu-id="1104a-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1104a-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="1104a-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1104a-139">OUTPUTS</span></span>

### <span data-ttu-id="1104a-140">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1104a-140">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="1104a-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1104a-141">NOTES</span></span>

## <span data-ttu-id="1104a-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1104a-142">RELATED LINKS</span></span>

[<span data-ttu-id="1104a-143">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1104a-143">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1104a-144">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1104a-144">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1104a-145">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1104a-145">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1104a-146">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1104a-146">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="1104a-147">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1104a-147">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="1104a-148">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1104a-148">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="1104a-149">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1104a-149">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="1104a-150">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1104a-150">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
