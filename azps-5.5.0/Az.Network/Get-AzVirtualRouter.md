---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
ms.openlocfilehash: e99df2f29781281ee0293f4cf52715153ff0d0cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151844"
---
# <span data-ttu-id="58d40-101">Get-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="58d40-101">Get-AzVirtualRouter</span></span>

## <span data-ttu-id="58d40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58d40-102">SYNOPSIS</span></span>
<span data-ttu-id="58d40-103">Azure VirtualRouter erhalten</span><span class="sxs-lookup"><span data-stu-id="58d40-103">Get an Azure VirtualRouter</span></span>

## <span data-ttu-id="58d40-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58d40-104">SYNTAX</span></span>

### <span data-ttu-id="58d40-105">VirtualRouterSubscriptionIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="58d40-105">VirtualRouterSubscriptionIdParameterSet (Default)</span></span>
```
Get-AzVirtualRouter [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58d40-106">VirtualRouterNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="58d40-106">VirtualRouterNameParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceGroupName <String> [-RouterName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58d40-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="58d40-107">VirtualRouterResourceIdParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58d40-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="58d40-108">DESCRIPTION</span></span>
<span data-ttu-id="58d40-109">Das **Get-AzVirtualRouter-Cmdlet** ruft einen Azure VirtualRouter ab.</span><span class="sxs-lookup"><span data-stu-id="58d40-109">The **Get-AzVirtualRouter** cmdlet gets an Azure VirtualRouter</span></span>

## <span data-ttu-id="58d40-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="58d40-110">EXAMPLES</span></span>

### <span data-ttu-id="58d40-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="58d40-111">Example 1</span></span>
```powershell
Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="58d40-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="58d40-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Get-AzVirtualRouter -ResourceId $virtualRouterId
```

## <span data-ttu-id="58d40-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58d40-113">PARAMETERS</span></span>

### <span data-ttu-id="58d40-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58d40-114">-DefaultProfile</span></span>
<span data-ttu-id="58d40-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="58d40-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58d40-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58d40-116">-ResourceGroupName</span></span>
<span data-ttu-id="58d40-117">Der Ressourcengruppenname des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="58d40-117">The resource group name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58d40-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58d40-118">-ResourceId</span></span>
<span data-ttu-id="58d40-119">ResourceId des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="58d40-119">ResourceId of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58d40-120">-RouterName</span><span class="sxs-lookup"><span data-stu-id="58d40-120">-RouterName</span></span>
<span data-ttu-id="58d40-121">Der Name des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="58d40-121">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58d40-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58d40-122">CommonParameters</span></span>
<span data-ttu-id="58d40-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58d40-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58d40-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58d40-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58d40-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="58d40-125">INPUTS</span></span>

### <span data-ttu-id="58d40-126">System.String</span><span class="sxs-lookup"><span data-stu-id="58d40-126">System.String</span></span>

## <span data-ttu-id="58d40-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="58d40-127">OUTPUTS</span></span>

### <span data-ttu-id="58d40-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="58d40-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="58d40-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="58d40-129">NOTES</span></span>

## <span data-ttu-id="58d40-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="58d40-130">RELATED LINKS</span></span>
