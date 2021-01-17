---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemoverunresolveddependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
ms.openlocfilehash: 261ca79618f6d0568647f9126e0fddeaeb8db540
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365293"
---
# <span data-ttu-id="7829c-101">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="7829c-101">Get-AzResourceMoverUnresolvedDependency</span></span>

## <span data-ttu-id="7829c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7829c-102">SYNOPSIS</span></span>
<span data-ttu-id="7829c-103">Ruft eine Liste der nicht aufgelösten Abhängigkeiten ab.</span><span class="sxs-lookup"><span data-stu-id="7829c-103">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="7829c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7829c-104">SYNTAX</span></span>

```
Get-AzResourceMoverUnresolvedDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7829c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7829c-105">DESCRIPTION</span></span>
<span data-ttu-id="7829c-106">Ruft eine Liste der nicht aufgelösten Abhängigkeiten ab.</span><span class="sxs-lookup"><span data-stu-id="7829c-106">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="7829c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7829c-107">EXAMPLES</span></span>

### <span data-ttu-id="7829c-108">Beispiel 1: Erhalten einer Liste der nicht aufgelösten abhängigen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7829c-108">Example 1: Get list of unresolved dependent resources</span></span>
```powershell
PS C:\> Get-AzResourceMoverUnresolvedDependency -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM
Count Id
----- --
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/publicipaddresses/psdemovm-ip
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/virtualnetworks/psdemorm-vnet
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg
```

<span data-ttu-id="7829c-109">Hier erhalten Sie eine Liste der nicht aufgelösten abhängigen Ressourcen für eine Move-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="7829c-109">Get list of unresolved dependent resources for a Move collection.</span></span>

## <span data-ttu-id="7829c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7829c-110">PARAMETERS</span></span>

### <span data-ttu-id="7829c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7829c-111">-DefaultProfile</span></span>
<span data-ttu-id="7829c-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7829c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7829c-113">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="7829c-113">-MoveCollectionName</span></span>
<span data-ttu-id="7829c-114">Der Name der Sammlung "Verschieben".</span><span class="sxs-lookup"><span data-stu-id="7829c-114">The Move Collection Name.</span></span>

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

### <span data-ttu-id="7829c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7829c-115">-ResourceGroupName</span></span>
<span data-ttu-id="7829c-116">Der Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="7829c-116">The Resource Group Name.</span></span>

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

### <span data-ttu-id="7829c-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7829c-117">-SubscriptionId</span></span>
<span data-ttu-id="7829c-118">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="7829c-118">The Subscription ID.</span></span>

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

### <span data-ttu-id="7829c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7829c-119">CommonParameters</span></span>
<span data-ttu-id="7829c-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7829c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7829c-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7829c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7829c-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7829c-122">INPUTS</span></span>

## <span data-ttu-id="7829c-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7829c-123">OUTPUTS</span></span>

### <span data-ttu-id="7829c-124">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IUnresolvedDependencyCollection</span><span class="sxs-lookup"><span data-stu-id="7829c-124">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IUnresolvedDependencyCollection</span></span>

## <span data-ttu-id="7829c-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7829c-125">NOTES</span></span>

<span data-ttu-id="7829c-126">ALIASE</span><span class="sxs-lookup"><span data-stu-id="7829c-126">ALIASES</span></span>

## <span data-ttu-id="7829c-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7829c-127">RELATED LINKS</span></span>

