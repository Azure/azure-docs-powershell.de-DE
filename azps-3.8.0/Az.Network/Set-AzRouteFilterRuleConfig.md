---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
ms.openlocfilehash: eb8de50aac1b68928d5cebe8118665b9a24e8fbf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003291"
---
# <span data-ttu-id="ebf51-101">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ebf51-101">Set-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="ebf51-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ebf51-102">SYNOPSIS</span></span>
<span data-ttu-id="ebf51-103">Ändert die Routenfilter Regel eines Routen Filters.</span><span class="sxs-lookup"><span data-stu-id="ebf51-103">Modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="ebf51-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ebf51-104">SYNTAX</span></span>

```
Set-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebf51-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ebf51-105">DESCRIPTION</span></span>
<span data-ttu-id="ebf51-106">Das Cmdlet " **Satz-AzRouteFilterRuleConfig** " ändert die Routenfilter Regel eines Routen Filters.</span><span class="sxs-lookup"><span data-stu-id="ebf51-106">The **Set-AzRouteFilterRuleConfig** cmdlet modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="ebf51-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ebf51-107">EXAMPLES</span></span>

### <span data-ttu-id="ebf51-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ebf51-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> $rf = Set-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01" -Access Deny -RouteFilterRuleType Community -CommunityList "12076:5010","12076:5040"
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="ebf51-109">Der erste Befehl ruft den Routenfilter mit dem Namen RouteFilter01 ab und speichert ihn in der $RF Variablen.</span><span class="sxs-lookup"><span data-stu-id="ebf51-109">The first command gets the route filter named RouteFilter01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="ebf51-110">Der zweite Befehl ändert die Routenfilter Regel mit dem Namen Rule01 und speichert den aktualisierten Routenfilter in der $RF Variablen.</span><span class="sxs-lookup"><span data-stu-id="ebf51-110">The second command modifies the route filter rule named Rule01 and stores updated route filter in the $rf variable.</span></span>
<span data-ttu-id="ebf51-111">Der dritte Befehl speichert aktualisierten Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="ebf51-111">The third command saves updated route filter.</span></span>

## <span data-ttu-id="ebf51-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ebf51-112">PARAMETERS</span></span>

### <span data-ttu-id="ebf51-113">-Access</span><span class="sxs-lookup"><span data-stu-id="ebf51-113">-Access</span></span>
<span data-ttu-id="ebf51-114">Der Zugriffstyp der Regel.</span><span class="sxs-lookup"><span data-stu-id="ebf51-114">The access type of the rule.</span></span>
<span data-ttu-id="ebf51-115">Mögliche Werte sind: "zulassen", "verweigern"</span><span class="sxs-lookup"><span data-stu-id="ebf51-115">Possible values are: 'Allow', 'Deny'</span></span>

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

### <span data-ttu-id="ebf51-116">-Communityliste</span><span class="sxs-lookup"><span data-stu-id="ebf51-116">-CommunityList</span></span>
<span data-ttu-id="ebf51-117">Die Liste des Community-Werts, nach dem der Routenfilter gefiltert wird</span><span class="sxs-lookup"><span data-stu-id="ebf51-117">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="ebf51-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebf51-118">-DefaultProfile</span></span>
<span data-ttu-id="ebf51-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ebf51-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebf51-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ebf51-120">-Force</span></span>
<span data-ttu-id="ebf51-121">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="ebf51-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="ebf51-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ebf51-122">-Name</span></span>
<span data-ttu-id="ebf51-123">Der Name der Routenfilter Regel</span><span class="sxs-lookup"><span data-stu-id="ebf51-123">The name of the route filter rule</span></span>

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

### <span data-ttu-id="ebf51-124">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="ebf51-124">-RouteFilter</span></span>
<span data-ttu-id="ebf51-125">Die RouteFilter</span><span class="sxs-lookup"><span data-stu-id="ebf51-125">The RouteFilter</span></span>

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

### <span data-ttu-id="ebf51-126">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="ebf51-126">-RouteFilterRuleType</span></span>
<span data-ttu-id="ebf51-127">Der Typ der Regel für den Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="ebf51-127">The route filter rule type of the rule.</span></span>
<span data-ttu-id="ebf51-128">Mögliche Werte sind: "Community"</span><span class="sxs-lookup"><span data-stu-id="ebf51-128">Possible values are: 'Community'</span></span>

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

### <span data-ttu-id="ebf51-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ebf51-129">-Confirm</span></span>
<span data-ttu-id="ebf51-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ebf51-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebf51-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebf51-131">-WhatIf</span></span>
<span data-ttu-id="ebf51-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ebf51-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ebf51-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ebf51-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebf51-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebf51-134">CommonParameters</span></span>
<span data-ttu-id="ebf51-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebf51-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebf51-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebf51-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebf51-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ebf51-137">INPUTS</span></span>

### <span data-ttu-id="ebf51-138">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ebf51-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="ebf51-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ebf51-139">OUTPUTS</span></span>

### <span data-ttu-id="ebf51-140">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ebf51-140">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="ebf51-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="ebf51-141">NOTES</span></span>

## <span data-ttu-id="ebf51-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ebf51-142">RELATED LINKS</span></span>

[<span data-ttu-id="ebf51-143">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ebf51-143">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ebf51-144">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ebf51-144">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ebf51-145">Neu – AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ebf51-145">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ebf51-146">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ebf51-146">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ebf51-147">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ebf51-147">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="ebf51-148">Neu – AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ebf51-148">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="ebf51-149">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ebf51-149">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="ebf51-150">Satz-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ebf51-150">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
