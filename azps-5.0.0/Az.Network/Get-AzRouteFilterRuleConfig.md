---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
ms.openlocfilehash: d55c16f7fa4f45ac3b1249f4e2e8b41dfb529d4c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179898"
---
# <span data-ttu-id="0ba3a-101">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0ba3a-101">Get-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="0ba3a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0ba3a-102">SYNOPSIS</span></span>
<span data-ttu-id="0ba3a-103">Ruft eine Routenfilter Regel in einem Routenfilter ab.</span><span class="sxs-lookup"><span data-stu-id="0ba3a-103">Gets a route filter rule in a route filter.</span></span>

## <span data-ttu-id="0ba3a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ba3a-104">SYNTAX</span></span>

```
Get-AzRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ba3a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ba3a-105">DESCRIPTION</span></span>
<span data-ttu-id="0ba3a-106">Das Cmdlet " **Get-AzRouteFilterRuleConfig** " Ruft eine Routenfilter Regel oder eine Liste von Routenfilter Regeln in einem Routenfilter ab.</span><span class="sxs-lookup"><span data-stu-id="0ba3a-106">The **Get-AzRouteFilterRuleConfig** cmdlet gets a route filter rule or a list of route filter rules in a route filter.</span></span>

## <span data-ttu-id="0ba3a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0ba3a-107">EXAMPLES</span></span>

### <span data-ttu-id="0ba3a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0ba3a-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf
```

<span data-ttu-id="0ba3a-109">Der erste Befehl ruft den Routenfilter mit dem Namen MyRouteFilter ab und speichert ihn dann in der Variablen $RF.</span><span class="sxs-lookup"><span data-stu-id="0ba3a-109">The first command gets the route filter named MyRouteFilter, and then stores it in the variable $rf.</span></span>
<span data-ttu-id="0ba3a-110">Der zweite Befehl ruft die Routenfilter Regel mit dem Namen Rule01 ab, die diesem Routenfilter zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0ba3a-110">The second command gets the route filter rule named Rule01 associated with that route filter.</span></span>
<span data-ttu-id="0ba3a-111">Der dritte Befehl ruft eine Liste der Routenfilter Regeln ab, die diesem Routenfilter zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0ba3a-111">The third command gets a list of route filter rules associated with that route filter.</span></span>

## <span data-ttu-id="0ba3a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ba3a-112">PARAMETERS</span></span>

### <span data-ttu-id="0ba3a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ba3a-113">-DefaultProfile</span></span>
<span data-ttu-id="0ba3a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0ba3a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ba3a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0ba3a-115">-Name</span></span>
<span data-ttu-id="0ba3a-116">Der Name der Routenfilter Regel</span><span class="sxs-lookup"><span data-stu-id="0ba3a-116">The name of the route filter rule</span></span>

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

### <span data-ttu-id="0ba3a-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="0ba3a-117">-RouteFilter</span></span>
<span data-ttu-id="0ba3a-118">Die RouteFilter</span><span class="sxs-lookup"><span data-stu-id="0ba3a-118">The RouteFilter</span></span>

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

### <span data-ttu-id="0ba3a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ba3a-119">CommonParameters</span></span>
<span data-ttu-id="0ba3a-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ba3a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ba3a-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ba3a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ba3a-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0ba3a-122">INPUTS</span></span>

### <span data-ttu-id="0ba3a-123">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0ba3a-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="0ba3a-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0ba3a-124">OUTPUTS</span></span>

### <span data-ttu-id="0ba3a-125">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="0ba3a-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="0ba3a-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="0ba3a-126">NOTES</span></span>

## <span data-ttu-id="0ba3a-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0ba3a-127">RELATED LINKS</span></span>

[<span data-ttu-id="0ba3a-128">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0ba3a-128">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0ba3a-129">Neu – AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0ba3a-129">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0ba3a-130">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0ba3a-130">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0ba3a-131">Satz-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0ba3a-131">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0ba3a-132">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0ba3a-132">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="0ba3a-133">Neu – AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0ba3a-133">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="0ba3a-134">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0ba3a-134">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="0ba3a-135">Satz-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0ba3a-135">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
