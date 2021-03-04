---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
ms.openlocfilehash: 2cccbc06095f9ff71f4b16d40bca16d91e91dda0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942163"
---
# <span data-ttu-id="601ff-101">Get-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="601ff-101">Get-AzVirtualRouter</span></span>

## <span data-ttu-id="601ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="601ff-102">SYNOPSIS</span></span>
<span data-ttu-id="601ff-103">Azure VirtualRouter erhalten</span><span class="sxs-lookup"><span data-stu-id="601ff-103">Get an Azure VirtualRouter</span></span>

## <span data-ttu-id="601ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="601ff-104">SYNTAX</span></span>

### <span data-ttu-id="601ff-105">VirtualRouterSubscriptionIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="601ff-105">VirtualRouterSubscriptionIdParameterSet (Default)</span></span>
```
Get-AzVirtualRouter [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="601ff-106">VirtualRouterNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="601ff-106">VirtualRouterNameParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceGroupName <String> [-RouterName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="601ff-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="601ff-107">VirtualRouterResourceIdParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="601ff-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="601ff-108">DESCRIPTION</span></span>
<span data-ttu-id="601ff-109">Das **Get-AzVirtualRouter-Cmdlet** erhält einen Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="601ff-109">The **Get-AzVirtualRouter** cmdlet gets an Azure VirtualRouter</span></span>

## <span data-ttu-id="601ff-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="601ff-110">EXAMPLES</span></span>

### <span data-ttu-id="601ff-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="601ff-111">Example 1</span></span>
```powershell
Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="601ff-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="601ff-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Get-AzVirtualRouter -ResourceId $virtualRouterId
```

## <span data-ttu-id="601ff-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="601ff-113">PARAMETERS</span></span>

### <span data-ttu-id="601ff-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="601ff-114">-DefaultProfile</span></span>
<span data-ttu-id="601ff-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="601ff-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="601ff-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="601ff-116">-ResourceGroupName</span></span>
<span data-ttu-id="601ff-117">Der Ressourcengruppenname des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="601ff-117">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="601ff-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="601ff-118">-ResourceId</span></span>
<span data-ttu-id="601ff-119">ResourceId des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="601ff-119">ResourceId of the virtual router.</span></span>

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

### <span data-ttu-id="601ff-120">-RouterName</span><span class="sxs-lookup"><span data-stu-id="601ff-120">-RouterName</span></span>
<span data-ttu-id="601ff-121">Der Name des virtuellen Routers.</span><span class="sxs-lookup"><span data-stu-id="601ff-121">The name of the virtual router.</span></span>

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

### <span data-ttu-id="601ff-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="601ff-122">CommonParameters</span></span>
<span data-ttu-id="601ff-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="601ff-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="601ff-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="601ff-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="601ff-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="601ff-125">INPUTS</span></span>

### <span data-ttu-id="601ff-126">System.String</span><span class="sxs-lookup"><span data-stu-id="601ff-126">System.String</span></span>

## <span data-ttu-id="601ff-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="601ff-127">OUTPUTS</span></span>

### <span data-ttu-id="601ff-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="601ff-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="601ff-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="601ff-129">NOTES</span></span>

## <span data-ttu-id="601ff-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="601ff-130">RELATED LINKS</span></span>
