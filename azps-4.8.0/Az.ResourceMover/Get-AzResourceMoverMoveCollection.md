---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 73bb67577a9160440c2e42e1e5b3259ad8435c5c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173104"
---
# <span data-ttu-id="44cc2-101">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="44cc2-101">Get-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="44cc2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="44cc2-102">SYNOPSIS</span></span>
<span data-ttu-id="44cc2-103">Ruft die Move-Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="44cc2-103">Gets the move collection.</span></span>

## <span data-ttu-id="44cc2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="44cc2-104">SYNTAX</span></span>

### <span data-ttu-id="44cc2-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="44cc2-105">List (Default)</span></span>
```
Get-AzResourceMoverMoveCollection [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="44cc2-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="44cc2-106">Get</span></span>
```
Get-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="44cc2-107">List1</span><span class="sxs-lookup"><span data-stu-id="44cc2-107">List1</span></span>
```
Get-AzResourceMoverMoveCollection -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="44cc2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="44cc2-108">DESCRIPTION</span></span>
<span data-ttu-id="44cc2-109">Ruft die Move-Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="44cc2-109">Gets the move collection.</span></span>

## <span data-ttu-id="44cc2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="44cc2-110">EXAMPLES</span></span>

### <span data-ttu-id="44cc2-111">Beispiel 1: Abrufen von Details zu allen Move-Auflistungen im Abonnement</span><span class="sxs-lookup"><span data-stu-id="44cc2-111">Example 1:  Get details of all the Move collections in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection  -SubscriptionId e80eb9fa-c996-4435-aa32-5af6f3d3077c

Location    Name                                            Type
--------    ----                                            ----
eastus2     mvcolle2e07001                                  Microsoft.Migrate/moveCollections
eastus2     mvcolle2e34745                                  Microsoft.Migrate/moveCollections
eastus2     mvcolle2e56720                                  Microsoft.Migrate/moveCollections


```

<span data-ttu-id="44cc2-112">Hier erhalten Sie Informationen zu allen Move-Auflistungen im Abonnement.</span><span class="sxs-lookup"><span data-stu-id="44cc2-112">Get details of all the Move collections in the subscription.</span></span>

### <span data-ttu-id="44cc2-113">Beispiel 2: Abrufen von Details zur Move-Sammlung mit einem angegebenen Move-Sammlungsnamen im Abonnement</span><span class="sxs-lookup"><span data-stu-id="44cc2-113">Example 2: Get details of the Move collection with a specified move collection name in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection -ResourceGroupName RG-MoveCollection-demoRM -Name PS-centralus-westcentralus-demoRM

Location    Name                              Type
--------    ----                              ----
eastus2     PS-centralus-westcentralus-demoRM Microsoft.Migrate/moveCollections

```

<span data-ttu-id="44cc2-114">Abrufen von Details zur Move-Sammlung mit dem angegebenen Move-Sammlungsnamen im Abonnement.</span><span class="sxs-lookup"><span data-stu-id="44cc2-114">Get details of the Move collection with a specified move collection name in the subscription.</span></span>

### <span data-ttu-id="44cc2-115">Beispiel 3: Abrufen von Details zur Move-Sammlung mit einem angegebenen Ressourcengruppennamen im Abonnement</span><span class="sxs-lookup"><span data-stu-id="44cc2-115">Example 3: Get details of the Move collection with a specified resource group name in the subscription</span></span>
```powershell
PS C:\> Get-AzResourceMoverMoveCollection -ResourceGroupName RG-MoveCollection-demoRM 

Location    Name                               Type
--------    ----                               ----
eastus2     PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
eastus2euap PS-centralus-westcentralus-demoRM2 Microsoft.Migrate/moveCollections


```

<span data-ttu-id="44cc2-116">Abrufen von Details zur Move-Sammlung mit einem angegebenen Ressourcengruppennamen im Abonnement.</span><span class="sxs-lookup"><span data-stu-id="44cc2-116">Get details of the Move Collection with a specified resource group name in the subscription.</span></span>

## <span data-ttu-id="44cc2-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="44cc2-117">PARAMETERS</span></span>

### <span data-ttu-id="44cc2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44cc2-118">-DefaultProfile</span></span>
<span data-ttu-id="44cc2-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="44cc2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44cc2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="44cc2-120">-Name</span></span>
<span data-ttu-id="44cc2-121">Der Name der verschieben-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="44cc2-121">The Move Collection Name.</span></span>

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

### <span data-ttu-id="44cc2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44cc2-122">-ResourceGroupName</span></span>
<span data-ttu-id="44cc2-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="44cc2-123">The Resource Group Name.</span></span>

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

### <span data-ttu-id="44cc2-124">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="44cc2-124">-SubscriptionId</span></span>
<span data-ttu-id="44cc2-125">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="44cc2-125">The Subscription ID.</span></span>

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

### <span data-ttu-id="44cc2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44cc2-126">CommonParameters</span></span>
<span data-ttu-id="44cc2-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44cc2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44cc2-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44cc2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44cc2-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="44cc2-129">INPUTS</span></span>

## <span data-ttu-id="44cc2-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="44cc2-130">OUTPUTS</span></span>

### <span data-ttu-id="44cc2-131">Microsoft. Azure. PowerShell. Cmdlets. ResourceMover. Models. Api20191001Preview. IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="44cc2-131">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span></span>

## <span data-ttu-id="44cc2-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="44cc2-132">NOTES</span></span>

<span data-ttu-id="44cc2-133">Aliase</span><span class="sxs-lookup"><span data-stu-id="44cc2-133">ALIASES</span></span>

## <span data-ttu-id="44cc2-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="44cc2-134">RELATED LINKS</span></span>

