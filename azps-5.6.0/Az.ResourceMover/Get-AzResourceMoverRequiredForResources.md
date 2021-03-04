---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/get-azresourcemoverrequiredforresources
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverRequiredForResources.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverRequiredForResources.md
ms.openlocfilehash: 9aa09de52a6b731fbf57b309fb605c0ba07325da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943589"
---
# <span data-ttu-id="4e42f-101">Get-AzResourceMoverRequiredForResources</span><span class="sxs-lookup"><span data-stu-id="4e42f-101">Get-AzResourceMoverRequiredForResources</span></span>

## <span data-ttu-id="4e42f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e42f-102">SYNOPSIS</span></span>
<span data-ttu-id="4e42f-103">Liste der Verschieberessourcen, für die eine Armressource erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="4e42f-103">List of the move resources for which an arm resource is required for.</span></span>

## <span data-ttu-id="4e42f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4e42f-104">SYNTAX</span></span>

```
Get-AzResourceMoverRequiredForResources -MoveCollectionName <String> -ResourceGroupName <String>
 -SourceId <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4e42f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4e42f-105">DESCRIPTION</span></span>
<span data-ttu-id="4e42f-106">Liste der Verschieberessourcen, für die eine Armressource erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="4e42f-106">List of the move resources for which an arm resource is required for.</span></span>

## <span data-ttu-id="4e42f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4e42f-107">EXAMPLES</span></span>

### <span data-ttu-id="4e42f-108">Beispiel 1: Hier erhalten Sie eine Liste der erforderlichen Ressourcen-ARMIDs, die hinzugefügt werden müssen, um die angegebene Ressource hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4e42f-108">Example 1: Get a list of required resource ARMIDs that are required to be added, to add the specified resource.</span></span>
```powershell
PS C:\> Get-AzResourceMoverRequiredForResources -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -ResourceGroupName "RG-MoveCollection-demoRMS" -SourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups"

/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachines/PSDemoVM
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networkinterfaces/psdemovm111
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/psdemorm/providers/Microsoft.Network/virtualNetworks/psdemorm-vnet
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg
```

<span data-ttu-id="4e42f-109">Hier erhalten Sie eine Liste der erforderlichen Ressourcen-ARMIDs, die hinzugefügt werden müssen, um die angegebene Ressource hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4e42f-109">Get a list of required resource ARMIDs that are required to be added, to add the specified resource.</span></span>

## <span data-ttu-id="4e42f-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4e42f-110">PARAMETERS</span></span>

### <span data-ttu-id="4e42f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e42f-111">-DefaultProfile</span></span>
<span data-ttu-id="4e42f-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4e42f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e42f-113">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="4e42f-113">-MoveCollectionName</span></span>
<span data-ttu-id="4e42f-114">Der Name der Sammlung verschieben.</span><span class="sxs-lookup"><span data-stu-id="4e42f-114">The Move Collection Name.</span></span>

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

### <span data-ttu-id="4e42f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e42f-115">-ResourceGroupName</span></span>
<span data-ttu-id="4e42f-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4e42f-116">The Resource Group Name.</span></span>

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

### <span data-ttu-id="4e42f-117">-SourceId</span><span class="sxs-lookup"><span data-stu-id="4e42f-117">-SourceId</span></span>
<span data-ttu-id="4e42f-118">Die sourceId, für die die Api aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4e42f-118">The sourceId for which the api is invoked.</span></span>

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

### <span data-ttu-id="4e42f-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4e42f-119">-SubscriptionId</span></span>
<span data-ttu-id="4e42f-120">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="4e42f-120">The Subscription ID.</span></span>

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

### <span data-ttu-id="4e42f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e42f-121">CommonParameters</span></span>
<span data-ttu-id="4e42f-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e42f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e42f-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e42f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e42f-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4e42f-124">INPUTS</span></span>

## <span data-ttu-id="4e42f-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4e42f-125">OUTPUTS</span></span>

### <span data-ttu-id="4e42f-126">System.String</span><span class="sxs-lookup"><span data-stu-id="4e42f-126">System.String</span></span>

## <span data-ttu-id="4e42f-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4e42f-127">NOTES</span></span>

<span data-ttu-id="4e42f-128">ALIASE</span><span class="sxs-lookup"><span data-stu-id="4e42f-128">ALIASES</span></span>

## <span data-ttu-id="4e42f-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4e42f-129">RELATED LINKS</span></span>

