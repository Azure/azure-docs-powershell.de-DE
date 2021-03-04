---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 2212ffb43f646e49a4552713b6408091dd985aae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941507"
---
# <span data-ttu-id="a7e0a-101">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a7e0a-101">Remove-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="a7e0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7e0a-102">SYNOPSIS</span></span>
<span data-ttu-id="a7e0a-103">Entfernt eine Routenfilterregel aus einem Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="a7e0a-103">Removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="a7e0a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a7e0a-104">SYNTAX</span></span>

```
Remove-AzRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7e0a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a7e0a-105">DESCRIPTION</span></span>
<span data-ttu-id="a7e0a-106">Das **Cmdlet Remove-AzRouteFilterRuleConfig** entfernt eine Routenfilterregel aus einem Routenfilter.</span><span class="sxs-lookup"><span data-stu-id="a7e0a-106">The **Remove-AzRouteFilterRuleConfig** cmdlet removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="a7e0a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a7e0a-107">EXAMPLES</span></span>

### <span data-ttu-id="a7e0a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a7e0a-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
```

<span data-ttu-id="a7e0a-109">Der erste Befehl ruft einen Routenfilter mit dem Namen RouteFilter01 ab, der zur Ressourcengruppe "ResourceGroup01" gehört und ihn in der $rf speichert.</span><span class="sxs-lookup"><span data-stu-id="a7e0a-109">The first command gets a route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="a7e0a-110">Mit dem zweiten Befehl wird die Routenfilterregel mit dem Namen Regel01 aus dem routenfilter entfernt, der in $rf.</span><span class="sxs-lookup"><span data-stu-id="a7e0a-110">The second command removes the route filter rule named Rule01 from the route filter stored in $rf.</span></span>

## <span data-ttu-id="a7e0a-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a7e0a-111">PARAMETERS</span></span>

### <span data-ttu-id="a7e0a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7e0a-112">-DefaultProfile</span></span>
<span data-ttu-id="a7e0a-113">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a7e0a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7e0a-114">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="a7e0a-114">-Force</span></span>
<span data-ttu-id="a7e0a-115">Bitten Sie nicht um Bestätigung, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="a7e0a-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a7e0a-116">-Name</span><span class="sxs-lookup"><span data-stu-id="a7e0a-116">-Name</span></span>
<span data-ttu-id="a7e0a-117">Der Name der Routenfilterregel</span><span class="sxs-lookup"><span data-stu-id="a7e0a-117">The name of the route filter rule</span></span>

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

### <span data-ttu-id="a7e0a-118">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="a7e0a-118">-RouteFilter</span></span>
<span data-ttu-id="a7e0a-119">Der RouteFilter</span><span class="sxs-lookup"><span data-stu-id="a7e0a-119">The RouteFilter</span></span>

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

### <span data-ttu-id="a7e0a-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a7e0a-120">-Confirm</span></span>
<span data-ttu-id="a7e0a-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a7e0a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7e0a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7e0a-122">-WhatIf</span></span>
<span data-ttu-id="a7e0a-123">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a7e0a-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a7e0a-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a7e0a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7e0a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7e0a-125">CommonParameters</span></span>
<span data-ttu-id="a7e0a-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7e0a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7e0a-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7e0a-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7e0a-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a7e0a-128">INPUTS</span></span>

### <span data-ttu-id="a7e0a-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a7e0a-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="a7e0a-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a7e0a-130">OUTPUTS</span></span>

### <span data-ttu-id="a7e0a-131">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="a7e0a-131">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="a7e0a-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a7e0a-132">NOTES</span></span>

## <span data-ttu-id="a7e0a-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a7e0a-133">RELATED LINKS</span></span>

[<span data-ttu-id="a7e0a-134">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a7e0a-134">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="a7e0a-135">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a7e0a-135">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="a7e0a-136">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a7e0a-136">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="a7e0a-137">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a7e0a-137">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="a7e0a-138">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a7e0a-138">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="a7e0a-139">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a7e0a-139">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="a7e0a-140">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a7e0a-140">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="a7e0a-141">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a7e0a-141">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
