---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
ms.openlocfilehash: 26fb3e9a7b4b097e79fdb328d79a82fc423ac675
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822279"
---
# <span data-ttu-id="0c308-101">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0c308-101">Get-AzRouteFilter</span></span>

## <span data-ttu-id="0c308-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0c308-102">SYNOPSIS</span></span>
<span data-ttu-id="0c308-103">Ruft einen Routenfilter ab.</span><span class="sxs-lookup"><span data-stu-id="0c308-103">Gets a route filter.</span></span>

## <span data-ttu-id="0c308-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c308-104">SYNTAX</span></span>

### <span data-ttu-id="0c308-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="0c308-105">NoExpand</span></span>
```
Get-AzRouteFilter [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0c308-106">Erweitern</span><span class="sxs-lookup"><span data-stu-id="0c308-106">Expand</span></span>
```
Get-AzRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c308-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c308-107">DESCRIPTION</span></span>
<span data-ttu-id="0c308-108">Das Cmdlet " **Get-AzRouteFilter** " Ruft einen Routenfilter ab.</span><span class="sxs-lookup"><span data-stu-id="0c308-108">The **Get-AzRouteFilter** cmdlet gets a route filter.</span></span>

## <span data-ttu-id="0c308-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0c308-109">EXAMPLES</span></span>

### <span data-ttu-id="0c308-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0c308-110">Example 1</span></span>
```powershell
PS C:\> Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"

Name              : RouteFilter01
ResourceGroupName : ResourceGroup01
Location          : westus
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsof
                    t.Network/routeFilters/RouteFilter01
Etag              : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState : Succeeded
Tags              :
Rules             : []
Peerings          : []
```

<span data-ttu-id="0c308-111">Dieser Befehl ruft den Routenfilter mit dem Namen RouteFilter01 ab, der zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört.</span><span class="sxs-lookup"><span data-stu-id="0c308-111">This command gets the route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="0c308-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0c308-112">Example 2</span></span>
```powershell
PS C:\> Get-AzRouteFilter -Name "RouteFilter*"

Name              : RouteFilter01
ResourceGroupName : ResourceGroup01
Location          : westus
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsof
                    t.Network/routeFilters/RouteFilter01
Etag              : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState : Succeeded
Tags              :
Rules             : []
Peerings          : []

Name              : RouteFilter02
ResourceGroupName : ResourceGroup01
Location          : westus
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsof
                    t.Network/routeFilters/RouteFilter02
Etag              : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState : Succeeded
Tags              :
Rules             : []
Peerings          : []
```

<span data-ttu-id="0c308-113">Dieser Befehl ruft alle Routenfilter ab, die mit "RouteFilter" beginnen.</span><span class="sxs-lookup"><span data-stu-id="0c308-113">This command gets all route filters that start with "RouteFilter".</span></span>

## <span data-ttu-id="0c308-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c308-114">PARAMETERS</span></span>

### <span data-ttu-id="0c308-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c308-115">-DefaultProfile</span></span>
<span data-ttu-id="0c308-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0c308-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c308-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="0c308-117">-ExpandResource</span></span>
<span data-ttu-id="0c308-118">Der Ressourcenverweis, der erweitert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0c308-118">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c308-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0c308-119">-Name</span></span>
<span data-ttu-id="0c308-120">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="0c308-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="0c308-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c308-121">-ResourceGroupName</span></span>
<span data-ttu-id="0c308-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0c308-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="0c308-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c308-123">CommonParameters</span></span>
<span data-ttu-id="0c308-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c308-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c308-125">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c308-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c308-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0c308-126">INPUTS</span></span>

### <span data-ttu-id="0c308-127">System. String</span><span class="sxs-lookup"><span data-stu-id="0c308-127">System.String</span></span>

## <span data-ttu-id="0c308-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0c308-128">OUTPUTS</span></span>

### <span data-ttu-id="0c308-129">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0c308-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="0c308-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="0c308-130">NOTES</span></span>

## <span data-ttu-id="0c308-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0c308-131">RELATED LINKS</span></span>

[<span data-ttu-id="0c308-132">Neu – AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0c308-132">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="0c308-133">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0c308-133">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="0c308-134">Satz-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0c308-134">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="0c308-135">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0c308-135">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0c308-136">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0c308-136">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0c308-137">Neu – AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0c308-137">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0c308-138">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0c308-138">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0c308-139">Satz-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0c308-139">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
