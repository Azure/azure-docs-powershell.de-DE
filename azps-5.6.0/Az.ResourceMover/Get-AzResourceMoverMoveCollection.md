---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/get-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
ms.openlocfilehash: a10ac77515b225c5e5ef06335f9cee1e99ecd3b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943601"
---
# <span data-ttu-id="03f38-101">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="03f38-101">Get-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="03f38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03f38-102">SYNOPSIS</span></span>
<span data-ttu-id="03f38-103">Ruft die Move-Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="03f38-103">Gets the move collection.</span></span>

## <span data-ttu-id="03f38-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="03f38-104">SYNTAX</span></span>

### <span data-ttu-id="03f38-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="03f38-105">List (Default)</span></span>
```
Get-AzResourceMoverMoveCollection [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="03f38-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="03f38-106">Get</span></span>
```
Get-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="03f38-107">Liste1</span><span class="sxs-lookup"><span data-stu-id="03f38-107">List1</span></span>
```
Get-AzResourceMoverMoveCollection -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="03f38-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="03f38-108">DESCRIPTION</span></span>
<span data-ttu-id="03f38-109">Ruft die Move-Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="03f38-109">Gets the move collection.</span></span>

## <span data-ttu-id="03f38-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="03f38-110">EXAMPLES</span></span>

### <span data-ttu-id="03f38-111">Beispiel 1: Details zu allen Sammlungen im Abonnement verschieben</span><span class="sxs-lookup"><span data-stu-id="03f38-111">Example 1:  Get details of all the Move collections in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection  -SubscriptionId "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Etag                                   Location      Name                                Type                             
----                                   --------      ----                                ----                             
"270119e0-0000-0c00-0000-5f5c94940000" centraluseuap PS-centralus-westcentralus-demoRMS  Microsoft.Migrate/moveCollections
"39015ed4-0000-0c00-0000-5f5ce2760000" centraluseuap PS-centralus-westcentralus-demo2RMS Microsoft.Migrate/moveCollections
"1000b505-0000-0c00-0000-5f69db6e0000" centraluseuap MoveCollection-cus-eus-ccy         Microsoft.Migrate/moveCollections


```

<span data-ttu-id="03f38-112">Hier erhalten Sie Details zu allen "Verschieben"-Sammlungen im Abonnement.</span><span class="sxs-lookup"><span data-stu-id="03f38-112">Get details of all the Move collections in the subscription.</span></span>

### <span data-ttu-id="03f38-113">Beispiel 2: Anzeigen von Details zur Move-Sammlung mit einem angegebenen Namen für die Umzugssammlung im Abonnement</span><span class="sxs-lookup"><span data-stu-id="03f38-113">Example 2: Get details of the Move collection with a specified move collection name in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRMS" -Name "PS-centralus-westcentralus-demoRMS"

Etag                                   Location      Name                               Type                             
----                                   --------      ----                               ----                             
"22006609-0000-3300-0000-602169590000" centraluseuap PS-centralus-westcentralus-demoRMS Microsoft.Migrate/moveCollections

```

<span data-ttu-id="03f38-114">Hier erhalten Sie Details zur Sammlung Verschieben mit einem angegebenen Namen für die Umzugssammlung im Abonnement.</span><span class="sxs-lookup"><span data-stu-id="03f38-114">Get details of the Move collection with a specified move collection name in the subscription.</span></span>

### <span data-ttu-id="03f38-115">Beispiel 3: Erhalten von Details zur Sammlung Verschieben mit einem angegebenen Ressourcengruppennamen im Abonnement</span><span class="sxs-lookup"><span data-stu-id="03f38-115">Example 3: Get details of the Move collection with a specified resource group name in the subscription</span></span>
```powershell
PS C:\> Get-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRMS" 

Location    Name                               Type
--------    ----                               ----
eastus2     PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
Etag                                   Location      Name                                Type                             
----                                   --------      ----                                ----                             
"22006609-0000-3300-0000-602169590000" centraluseuap PS-centralus-westcentralus-demoRMS  Microsoft.Migrate/moveCollections
"4e02b0a9-0000-0c00-0000-5fd101cc0000" centraluseuap PS-centralus-westcentralus-demo2RMS Microsoft.Migrate/moveCollections

```

<span data-ttu-id="03f38-116">Hier erhalten Sie Details zur Sammlung verschieben mit einem angegebenen Ressourcengruppennamen im Abonnement.</span><span class="sxs-lookup"><span data-stu-id="03f38-116">Get details of the Move Collection with a specified resource group name in the subscription.</span></span>

## <span data-ttu-id="03f38-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="03f38-117">PARAMETERS</span></span>

### <span data-ttu-id="03f38-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03f38-118">-DefaultProfile</span></span>
<span data-ttu-id="03f38-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="03f38-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03f38-120">-Name</span><span class="sxs-lookup"><span data-stu-id="03f38-120">-Name</span></span>
<span data-ttu-id="03f38-121">Der Name der Sammlung verschieben.</span><span class="sxs-lookup"><span data-stu-id="03f38-121">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MoveCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03f38-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03f38-122">-ResourceGroupName</span></span>
<span data-ttu-id="03f38-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="03f38-123">The Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03f38-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="03f38-124">-SubscriptionId</span></span>
<span data-ttu-id="03f38-125">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="03f38-125">The Subscription ID.</span></span>

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

### <span data-ttu-id="03f38-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03f38-126">CommonParameters</span></span>
<span data-ttu-id="03f38-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03f38-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03f38-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03f38-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03f38-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="03f38-129">INPUTS</span></span>

## <span data-ttu-id="03f38-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="03f38-130">OUTPUTS</span></span>

### <span data-ttu-id="03f38-131">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="03f38-131">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IMoveCollection</span></span>

## <span data-ttu-id="03f38-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="03f38-132">NOTES</span></span>

<span data-ttu-id="03f38-133">ALIASE</span><span class="sxs-lookup"><span data-stu-id="03f38-133">ALIASES</span></span>

## <span data-ttu-id="03f38-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="03f38-134">RELATED LINKS</span></span>

