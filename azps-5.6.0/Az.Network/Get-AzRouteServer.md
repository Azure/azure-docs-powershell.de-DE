---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServer.md
ms.openlocfilehash: ef5609a34104ca8502b8e4ce96fe294a4714366d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919648"
---
# <span data-ttu-id="2034d-101">Get-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="2034d-101">Get-AzRouteServer</span></span>

## <span data-ttu-id="2034d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2034d-102">SYNOPSIS</span></span>
<span data-ttu-id="2034d-103">Herunterladen eines Azure RouteServers</span><span class="sxs-lookup"><span data-stu-id="2034d-103">Get an Azure RouteServer</span></span>

## <span data-ttu-id="2034d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2034d-104">SYNTAX</span></span>

### <span data-ttu-id="2034d-105">RouteServerSubscriptionIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2034d-105">RouteServerSubscriptionIdParameterSet (Default)</span></span>
```
Get-AzRouteServer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2034d-106">RouteServerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2034d-106">RouteServerNameParameterSet</span></span>
```
Get-AzRouteServer -ResourceGroupName <String> [-RouteServerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2034d-107">RouteServerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2034d-107">RouteServerResourceIdParameterSet</span></span>
```
Get-AzRouteServer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2034d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2034d-108">DESCRIPTION</span></span>
<span data-ttu-id="2034d-109">Das **Get-AzRouteServer-Cmdlet** ruft einen Azure RouteServer ab.</span><span class="sxs-lookup"><span data-stu-id="2034d-109">The **Get-AzRouteServer** cmdlet gets an Azure RouteServer</span></span>

## <span data-ttu-id="2034d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2034d-110">EXAMPLES</span></span>

### <span data-ttu-id="2034d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2034d-111">Example 1</span></span>
```powershell
Get-AzRouteServer -ResourceGroupName routeServerRG -RouteServerName routeServer
```

### <span data-ttu-id="2034d-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2034d-112">Example 2</span></span>
```powershell
$routeServerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer'
Get-AzRouteServer -ResourceId $routeServerId
```
## <span data-ttu-id="2034d-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2034d-113">PARAMETERS</span></span>

### <span data-ttu-id="2034d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2034d-114">-DefaultProfile</span></span>
<span data-ttu-id="2034d-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2034d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2034d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2034d-116">-ResourceGroupName</span></span>
<span data-ttu-id="2034d-117">Der Ressourcengruppenname des Routenservers.</span><span class="sxs-lookup"><span data-stu-id="2034d-117">The resource group name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2034d-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2034d-118">-ResourceId</span></span>
<span data-ttu-id="2034d-119">ResourceId des Routenservers.</span><span class="sxs-lookup"><span data-stu-id="2034d-119">ResourceId of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2034d-120">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="2034d-120">-RouteServerName</span></span>
<span data-ttu-id="2034d-121">Der Name des Routenservers.</span><span class="sxs-lookup"><span data-stu-id="2034d-121">The name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2034d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2034d-122">CommonParameters</span></span>
<span data-ttu-id="2034d-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2034d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2034d-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2034d-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2034d-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2034d-125">INPUTS</span></span>

### <span data-ttu-id="2034d-126">System.String</span><span class="sxs-lookup"><span data-stu-id="2034d-126">System.String</span></span>

## <span data-ttu-id="2034d-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2034d-127">OUTPUTS</span></span>

### <span data-ttu-id="2034d-128">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="2034d-128">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="2034d-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2034d-129">NOTES</span></span>

## <span data-ttu-id="2034d-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2034d-130">RELATED LINKS</span></span>
