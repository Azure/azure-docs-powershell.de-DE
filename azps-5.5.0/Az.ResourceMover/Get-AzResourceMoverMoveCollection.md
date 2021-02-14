---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 73bb67577a9160440c2e42e1e5b3259ad8435c5c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174473"
---
# <span data-ttu-id="f2375-101">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="f2375-101">Get-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="f2375-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2375-102">SYNOPSIS</span></span>
<span data-ttu-id="f2375-103">Ruft die Sammlung zum Verschieben ab.</span><span class="sxs-lookup"><span data-stu-id="f2375-103">Gets the move collection.</span></span>

## <span data-ttu-id="f2375-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f2375-104">SYNTAX</span></span>

### <span data-ttu-id="f2375-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="f2375-105">List (Default)</span></span>
```
Get-AzResourceMoverMoveCollection [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2375-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="f2375-106">Get</span></span>
```
Get-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f2375-107">Liste1</span><span class="sxs-lookup"><span data-stu-id="f2375-107">List1</span></span>
```
Get-AzResourceMoverMoveCollection -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f2375-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2375-108">DESCRIPTION</span></span>
<span data-ttu-id="f2375-109">Ruft die Sammlung zum Verschieben ab.</span><span class="sxs-lookup"><span data-stu-id="f2375-109">Gets the move collection.</span></span>

## <span data-ttu-id="f2375-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f2375-110">EXAMPLES</span></span>

### <span data-ttu-id="f2375-111">Beispiel 1: Anzeigen von Details aller "Move"-Sammlungen im Abonnement</span><span class="sxs-lookup"><span data-stu-id="f2375-111">Example 1:  Get details of all the Move collections in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection  -SubscriptionId e80eb9fa-c996-4435-aa32-5af6f3d3077c

Location    Name                                            Type
--------    ----                                            ----
eastus2     mvcolle2e07001                                  Microsoft.Migrate/moveCollections
eastus2     mvcolle2e34745                                  Microsoft.Migrate/moveCollections
eastus2     mvcolle2e56720                                  Microsoft.Migrate/moveCollections


```

<span data-ttu-id="f2375-112">Hier erhalten Sie Details zu allen "Move"-Sammlungen im Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f2375-112">Get details of all the Move collections in the subscription.</span></span>

### <span data-ttu-id="f2375-113">Beispiel 2: Anzeigen von Details der Sammlung "Verschieben" mit einem angegebenen Namen für die Sammlung "Verschieben" im Abonnement</span><span class="sxs-lookup"><span data-stu-id="f2375-113">Example 2: Get details of the Move collection with a specified move collection name in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection -ResourceGroupName RG-MoveCollection-demoRM -Name PS-centralus-westcentralus-demoRM

Location    Name                              Type
--------    ----                              ----
eastus2     PS-centralus-westcentralus-demoRM Microsoft.Migrate/moveCollections

```

<span data-ttu-id="f2375-114">Erhalten Sie Details der Sammlung "Verschieben" mit einem angegebenen Namen für die Sammlung "Verschieben" im Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f2375-114">Get details of the Move collection with a specified move collection name in the subscription.</span></span>

### <span data-ttu-id="f2375-115">Beispiel 3: Anzeigen von Details der Sammlung "Verschieben" mit einem angegebenen Ressourcengruppennamen im Abonnement</span><span class="sxs-lookup"><span data-stu-id="f2375-115">Example 3: Get details of the Move collection with a specified resource group name in the subscription</span></span>
```powershell
PS C:\> Get-AzResourceMoverMoveCollection -ResourceGroupName RG-MoveCollection-demoRM 

Location    Name                               Type
--------    ----                               ----
eastus2     PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
eastus2euap PS-centralus-westcentralus-demoRM2 Microsoft.Migrate/moveCollections


```

<span data-ttu-id="f2375-116">Erhalten Sie Details der Sammlung "Sammlung verschieben" mit einem angegebenen Ressourcengruppennamen im Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f2375-116">Get details of the Move Collection with a specified resource group name in the subscription.</span></span>

## <span data-ttu-id="f2375-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2375-117">PARAMETERS</span></span>

### <span data-ttu-id="f2375-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2375-118">-DefaultProfile</span></span>
<span data-ttu-id="f2375-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f2375-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2375-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f2375-120">-Name</span></span>
<span data-ttu-id="f2375-121">Der Name der Sammlung "Verschieben".</span><span class="sxs-lookup"><span data-stu-id="f2375-121">The Move Collection Name.</span></span>

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

### <span data-ttu-id="f2375-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2375-122">-ResourceGroupName</span></span>
<span data-ttu-id="f2375-123">Der Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="f2375-123">The Resource Group Name.</span></span>

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

### <span data-ttu-id="f2375-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f2375-124">-SubscriptionId</span></span>
<span data-ttu-id="f2375-125">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="f2375-125">The Subscription ID.</span></span>

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

### <span data-ttu-id="f2375-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2375-126">CommonParameters</span></span>
<span data-ttu-id="f2375-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2375-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2375-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2375-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2375-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f2375-129">INPUTS</span></span>

## <span data-ttu-id="f2375-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f2375-130">OUTPUTS</span></span>

### <span data-ttu-id="f2375-131">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="f2375-131">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span></span>

## <span data-ttu-id="f2375-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f2375-132">NOTES</span></span>

<span data-ttu-id="f2375-133">ALIASE</span><span class="sxs-lookup"><span data-stu-id="f2375-133">ALIASES</span></span>

## <span data-ttu-id="f2375-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f2375-134">RELATED LINKS</span></span>

