---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
ms.openlocfilehash: e596ea3092cd5fda045c20f80c9208015b57a42d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295043"
---
# <span data-ttu-id="9f669-101">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9f669-101">Remove-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="9f669-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f669-102">SYNOPSIS</span></span>
<span data-ttu-id="9f669-103">Entfernt eine Routenfilterregel aus einem Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="9f669-103">Removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="9f669-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f669-104">SYNTAX</span></span>

```
Remove-AzRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f669-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9f669-105">DESCRIPTION</span></span>
<span data-ttu-id="9f669-106">Das **Cmdlet "Remove-AzRouteFilterRuleConfig"** entfernt eine Routenfilterregel aus einem Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="9f669-106">The **Remove-AzRouteFilterRuleConfig** cmdlet removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="9f669-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9f669-107">EXAMPLES</span></span>

### <span data-ttu-id="9f669-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9f669-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
```

<span data-ttu-id="9f669-109">Der erste Befehl ruft einen Routenfilter namens "RouteFilter01" ab, der zur Ressourcengruppe "ResourceGroup01" gehört, und speichert ihn in der $rf Variable.</span><span class="sxs-lookup"><span data-stu-id="9f669-109">The first command gets a route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="9f669-110">Mit dem zweiten Befehl wird die Routenfilterregel mit dem Namen "Regel01" aus dem in der Liste gespeicherten $rf.</span><span class="sxs-lookup"><span data-stu-id="9f669-110">The second command removes the route filter rule named Rule01 from the route filter stored in $rf.</span></span>

## <span data-ttu-id="9f669-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f669-111">PARAMETERS</span></span>

### <span data-ttu-id="9f669-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f669-112">-DefaultProfile</span></span>
<span data-ttu-id="9f669-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9f669-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f669-114">-Force</span><span class="sxs-lookup"><span data-stu-id="9f669-114">-Force</span></span>
<span data-ttu-id="9f669-115">Bestätigen Sie nicht, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="9f669-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="9f669-116">-Name</span><span class="sxs-lookup"><span data-stu-id="9f669-116">-Name</span></span>
<span data-ttu-id="9f669-117">Der Name der Routenfilterregel</span><span class="sxs-lookup"><span data-stu-id="9f669-117">The name of the route filter rule</span></span>

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

### <span data-ttu-id="9f669-118">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="9f669-118">-RouteFilter</span></span>
<span data-ttu-id="9f669-119">Der RouteFilter</span><span class="sxs-lookup"><span data-stu-id="9f669-119">The RouteFilter</span></span>

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

### <span data-ttu-id="9f669-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f669-120">-Confirm</span></span>
<span data-ttu-id="9f669-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9f669-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f669-122">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9f669-122">-WhatIf</span></span>
<span data-ttu-id="9f669-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9f669-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9f669-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9f669-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f669-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f669-125">CommonParameters</span></span>
<span data-ttu-id="9f669-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f669-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f669-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f669-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f669-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9f669-128">INPUTS</span></span>

### <span data-ttu-id="9f669-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9f669-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="9f669-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9f669-130">OUTPUTS</span></span>

### <span data-ttu-id="9f669-131">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="9f669-131">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="9f669-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9f669-132">NOTES</span></span>

## <span data-ttu-id="9f669-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9f669-133">RELATED LINKS</span></span>

[<span data-ttu-id="9f669-134">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9f669-134">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="9f669-135">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9f669-135">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="9f669-136">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9f669-136">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="9f669-137">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9f669-137">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="9f669-138">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9f669-138">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="9f669-139">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9f669-139">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="9f669-140">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9f669-140">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="9f669-141">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9f669-141">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
