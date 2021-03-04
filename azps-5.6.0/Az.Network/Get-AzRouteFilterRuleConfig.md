---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 0ed7233cda87c376707e0a5b5682a61a179550d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919656"
---
# <span data-ttu-id="91b1a-101">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="91b1a-101">Get-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="91b1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91b1a-102">SYNOPSIS</span></span>
<span data-ttu-id="91b1a-103">Ruft eine Routenfilterregel in einem Routenfilter ab.</span><span class="sxs-lookup"><span data-stu-id="91b1a-103">Gets a route filter rule in a route filter.</span></span>

## <span data-ttu-id="91b1a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91b1a-104">SYNTAX</span></span>

```
Get-AzRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91b1a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="91b1a-105">DESCRIPTION</span></span>
<span data-ttu-id="91b1a-106">Das **Get-AzRouteFilterRuleConfig-Cmdlet** ruft eine Routenfilterregel oder eine Liste der Routenfilterregeln in einem Routenfilter ab.</span><span class="sxs-lookup"><span data-stu-id="91b1a-106">The **Get-AzRouteFilterRuleConfig** cmdlet gets a route filter rule or a list of route filter rules in a route filter.</span></span>

## <span data-ttu-id="91b1a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="91b1a-107">EXAMPLES</span></span>

### <span data-ttu-id="91b1a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="91b1a-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf
```

<span data-ttu-id="91b1a-109">Der erste Befehl ruft den Routenfilter mit dem Namen MyRouteFilter ab und speichert ihn dann in der variablen $rf.</span><span class="sxs-lookup"><span data-stu-id="91b1a-109">The first command gets the route filter named MyRouteFilter, and then stores it in the variable $rf.</span></span>
<span data-ttu-id="91b1a-110">Der zweite Befehl ruft die dem Routenfilter zugeordnete Routenfilterregel "Regel01" ab.</span><span class="sxs-lookup"><span data-stu-id="91b1a-110">The second command gets the route filter rule named Rule01 associated with that route filter.</span></span>
<span data-ttu-id="91b1a-111">Der dritte Befehl ruft eine Liste der Routenfilterregeln ab, die diesem Routenfilter zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="91b1a-111">The third command gets a list of route filter rules associated with that route filter.</span></span>

## <span data-ttu-id="91b1a-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="91b1a-112">PARAMETERS</span></span>

### <span data-ttu-id="91b1a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91b1a-113">-DefaultProfile</span></span>
<span data-ttu-id="91b1a-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="91b1a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91b1a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="91b1a-115">-Name</span></span>
<span data-ttu-id="91b1a-116">Der Name der Routenfilterregel</span><span class="sxs-lookup"><span data-stu-id="91b1a-116">The name of the route filter rule</span></span>

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

### <span data-ttu-id="91b1a-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="91b1a-117">-RouteFilter</span></span>
<span data-ttu-id="91b1a-118">Der RouteFilter</span><span class="sxs-lookup"><span data-stu-id="91b1a-118">The RouteFilter</span></span>

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

### <span data-ttu-id="91b1a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91b1a-119">CommonParameters</span></span>
<span data-ttu-id="91b1a-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91b1a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91b1a-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91b1a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91b1a-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="91b1a-122">INPUTS</span></span>

### <span data-ttu-id="91b1a-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="91b1a-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="91b1a-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="91b1a-124">OUTPUTS</span></span>

### <span data-ttu-id="91b1a-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="91b1a-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="91b1a-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="91b1a-126">NOTES</span></span>

## <span data-ttu-id="91b1a-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="91b1a-127">RELATED LINKS</span></span>

[<span data-ttu-id="91b1a-128">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="91b1a-128">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="91b1a-129">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="91b1a-129">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="91b1a-130">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="91b1a-130">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="91b1a-131">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="91b1a-131">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="91b1a-132">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="91b1a-132">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="91b1a-133">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="91b1a-133">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="91b1a-134">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="91b1a-134">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="91b1a-135">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="91b1a-135">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
