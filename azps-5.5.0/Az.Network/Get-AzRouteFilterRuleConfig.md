---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
ms.openlocfilehash: d55c16f7fa4f45ac3b1249f4e2e8b41dfb529d4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151908"
---
# <span data-ttu-id="3d373-101">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3d373-101">Get-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="3d373-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d373-102">SYNOPSIS</span></span>
<span data-ttu-id="3d373-103">Ruft eine Routenfilterregel in einem Routenfilter ab.</span><span class="sxs-lookup"><span data-stu-id="3d373-103">Gets a route filter rule in a route filter.</span></span>

## <span data-ttu-id="3d373-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d373-104">SYNTAX</span></span>

```
Get-AzRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d373-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3d373-105">DESCRIPTION</span></span>
<span data-ttu-id="3d373-106">Das **Cmdlet "Get-AzRouteFilterRuleConfig"** ruft eine Routenfilterregel oder eine Liste der Routenfilterregeln in einem Routenfilter ab.</span><span class="sxs-lookup"><span data-stu-id="3d373-106">The **Get-AzRouteFilterRuleConfig** cmdlet gets a route filter rule or a list of route filter rules in a route filter.</span></span>

## <span data-ttu-id="3d373-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3d373-107">EXAMPLES</span></span>

### <span data-ttu-id="3d373-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3d373-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf
```

<span data-ttu-id="3d373-109">Der erste Befehl ruft den Routenfilter namens "MyRouteFilter" ab und speichert ihn dann in der variablen $rf.</span><span class="sxs-lookup"><span data-stu-id="3d373-109">The first command gets the route filter named MyRouteFilter, and then stores it in the variable $rf.</span></span>
<span data-ttu-id="3d373-110">Der zweite Befehl ruft die diesem Routenfilter zugeordnete Routenfilterregel mit dem Namen "Rule01" ab.</span><span class="sxs-lookup"><span data-stu-id="3d373-110">The second command gets the route filter rule named Rule01 associated with that route filter.</span></span>
<span data-ttu-id="3d373-111">Der dritte Befehl ruft eine Liste der Routenfilterregeln ab, die diesem Routenfilter zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3d373-111">The third command gets a list of route filter rules associated with that route filter.</span></span>

## <span data-ttu-id="3d373-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d373-112">PARAMETERS</span></span>

### <span data-ttu-id="3d373-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d373-113">-DefaultProfile</span></span>
<span data-ttu-id="3d373-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3d373-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d373-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3d373-115">-Name</span></span>
<span data-ttu-id="3d373-116">Der Name der Routenfilterregel</span><span class="sxs-lookup"><span data-stu-id="3d373-116">The name of the route filter rule</span></span>

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

### <span data-ttu-id="3d373-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="3d373-117">-RouteFilter</span></span>
<span data-ttu-id="3d373-118">Der RouteFilter</span><span class="sxs-lookup"><span data-stu-id="3d373-118">The RouteFilter</span></span>

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

### <span data-ttu-id="3d373-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d373-119">CommonParameters</span></span>
<span data-ttu-id="3d373-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d373-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d373-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3d373-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d373-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3d373-122">INPUTS</span></span>

### <span data-ttu-id="3d373-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3d373-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="3d373-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3d373-124">OUTPUTS</span></span>

### <span data-ttu-id="3d373-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="3d373-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="3d373-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3d373-126">NOTES</span></span>

## <span data-ttu-id="3d373-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3d373-127">RELATED LINKS</span></span>

[<span data-ttu-id="3d373-128">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3d373-128">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="3d373-129">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3d373-129">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="3d373-130">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3d373-130">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="3d373-131">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3d373-131">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="3d373-132">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3d373-132">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="3d373-133">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3d373-133">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="3d373-134">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3d373-134">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="3d373-135">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3d373-135">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
