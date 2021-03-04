---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/get-azresourcemoverunresolveddependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
ms.openlocfilehash: 34cae1bcc6020e2e0c2a8b2f6b70e302c8576f2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943583"
---
# <span data-ttu-id="2d3b8-101">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="2d3b8-101">Get-AzResourceMoverUnresolvedDependency</span></span>

## <span data-ttu-id="2d3b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d3b8-102">SYNOPSIS</span></span>
<span data-ttu-id="2d3b8-103">Ruft eine Liste der nicht aufgelösten Abhängigkeiten ab.</span><span class="sxs-lookup"><span data-stu-id="2d3b8-103">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="2d3b8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d3b8-104">SYNTAX</span></span>

```
Get-AzResourceMoverUnresolvedDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DependencyLevel <DependencyLevel>] [-Filter <String>] [-Orderby <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2d3b8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d3b8-105">DESCRIPTION</span></span>
<span data-ttu-id="2d3b8-106">Ruft eine Liste der nicht aufgelösten Abhängigkeiten ab.</span><span class="sxs-lookup"><span data-stu-id="2d3b8-106">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="2d3b8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2d3b8-107">EXAMPLES</span></span>

### <span data-ttu-id="2d3b8-108">Beispiel 1: Liste der nicht aufgelösten abhängigen Ressourcen für eine Sammlung verschieben.</span><span class="sxs-lookup"><span data-stu-id="2d3b8-108">Example 1: Get list of unresolved dependent resources for a Move Collection.</span></span>
```powershell
PS C:\> Get-AzResourceMoverUnresolvedDependency -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -ResourceGroupName "RG-MoveCollection-demoRMS" -DependencyLevel Descendant
Count Id                                                                                                                                        
----- --                                                                                                                                        
    1 /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networkinterfaces/psdemovm111   
    1 /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/psdemorm/providers/Microsoft.Network/virtualNetworks/psdemorm-vnet     
    1 /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg
    3 /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm
```

<span data-ttu-id="2d3b8-109">Hier erhalten Sie eine Liste der nicht aufgelösten abhängigen Ressourcen für eine Sammlung verschieben.</span><span class="sxs-lookup"><span data-stu-id="2d3b8-109">Get a list of unresolved dependent resources for a Move Collection.</span></span>

## <span data-ttu-id="2d3b8-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2d3b8-110">PARAMETERS</span></span>

### <span data-ttu-id="2d3b8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d3b8-111">-DefaultProfile</span></span>
<span data-ttu-id="2d3b8-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2d3b8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d3b8-113">-DependencyLevel</span><span class="sxs-lookup"><span data-stu-id="2d3b8-113">-DependencyLevel</span></span>
<span data-ttu-id="2d3b8-114">Definiert die Abhängigkeitsebene.</span><span class="sxs-lookup"><span data-stu-id="2d3b8-114">Defines the dependency level.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.DependencyLevel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d3b8-115">-Filter</span><span class="sxs-lookup"><span data-stu-id="2d3b8-115">-Filter</span></span>
<span data-ttu-id="2d3b8-116">Der Filter, der für den Vorgang angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2d3b8-116">The filter to apply on the operation.</span></span>
<span data-ttu-id="2d3b8-117">Beispiel: $apply=filter(Anzahl gleich 2).</span><span class="sxs-lookup"><span data-stu-id="2d3b8-117">For example, $apply=filter(count eq 2).</span></span>

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

### <span data-ttu-id="2d3b8-118">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="2d3b8-118">-MoveCollectionName</span></span>
<span data-ttu-id="2d3b8-119">Der Name der Sammlung verschieben.</span><span class="sxs-lookup"><span data-stu-id="2d3b8-119">The Move Collection Name.</span></span>

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

### <span data-ttu-id="2d3b8-120">-Orderby</span><span class="sxs-lookup"><span data-stu-id="2d3b8-120">-Orderby</span></span>
<span data-ttu-id="2d3b8-121">OData-Reihenfolge nach Abfrageoption.</span><span class="sxs-lookup"><span data-stu-id="2d3b8-121">OData order by query option.</span></span>
<span data-ttu-id="2d3b8-122">Sie können z. B. $orderby=Anzahl desc verwenden.</span><span class="sxs-lookup"><span data-stu-id="2d3b8-122">For example, you can use $orderby=Count desc.</span></span>

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

### <span data-ttu-id="2d3b8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d3b8-123">-ResourceGroupName</span></span>
<span data-ttu-id="2d3b8-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2d3b8-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="2d3b8-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2d3b8-125">-SubscriptionId</span></span>
<span data-ttu-id="2d3b8-126">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="2d3b8-126">The Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d3b8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d3b8-127">CommonParameters</span></span>
<span data-ttu-id="2d3b8-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d3b8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d3b8-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d3b8-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d3b8-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2d3b8-130">INPUTS</span></span>

## <span data-ttu-id="2d3b8-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2d3b8-131">OUTPUTS</span></span>

### <span data-ttu-id="2d3b8-132">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="2d3b8-132">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IUnresolvedDependency</span></span>

## <span data-ttu-id="2d3b8-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2d3b8-133">NOTES</span></span>

<span data-ttu-id="2d3b8-134">ALIASE</span><span class="sxs-lookup"><span data-stu-id="2d3b8-134">ALIASES</span></span>

## <span data-ttu-id="2d3b8-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2d3b8-135">RELATED LINKS</span></span>

