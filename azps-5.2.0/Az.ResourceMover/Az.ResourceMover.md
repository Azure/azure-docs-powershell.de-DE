---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: b634b4e547b1e483037cec8efe5772b5460ee1b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358782"
---
# <span data-ttu-id="48b8c-101">Az.ResourceMover-Modul</span><span class="sxs-lookup"><span data-stu-id="48b8c-101">Az.ResourceMover Module</span></span>
## <span data-ttu-id="48b8c-102">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48b8c-102">Description</span></span>
<span data-ttu-id="48b8c-103">Microsoft Azure PowerShell: ResourceMover-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="48b8c-103">Microsoft Azure PowerShell: ResourceMover cmdlets</span></span>

## <span data-ttu-id="48b8c-104">Az.ResourceMover-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="48b8c-104">Az.ResourceMover Cmdlets</span></span>
### [<span data-ttu-id="48b8c-105">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="48b8c-105">Add-AzResourceMoverMoveResource</span></span>](Add-AzResourceMoverMoveResource.md)
<span data-ttu-id="48b8c-106">Erstellt oder aktualisiert eine "Verschieben"-Ressource in der Sammlung "Verschieben".</span><span class="sxs-lookup"><span data-stu-id="48b8c-106">Creates or updates a Move Resource in the move collection.</span></span>

### [<span data-ttu-id="48b8c-107">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="48b8c-107">Get-AzResourceMoverMoveCollection</span></span>](Get-AzResourceMoverMoveCollection.md)
<span data-ttu-id="48b8c-108">Ruft die Sammlung zum Verschieben ab.</span><span class="sxs-lookup"><span data-stu-id="48b8c-108">Gets the move collection.</span></span>

### [<span data-ttu-id="48b8c-109">Get-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="48b8c-109">Get-AzResourceMoverMoveResource</span></span>](Get-AzResourceMoverMoveResource.md)
<span data-ttu-id="48b8c-110">Ruft die "Verschieben"-Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="48b8c-110">Gets the Move Resource.</span></span>

### [<span data-ttu-id="48b8c-111">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="48b8c-111">Get-AzResourceMoverUnresolvedDependency</span></span>](Get-AzResourceMoverUnresolvedDependency.md)
<span data-ttu-id="48b8c-112">Ruft eine Liste der nicht aufgelösten Abhängigkeiten ab.</span><span class="sxs-lookup"><span data-stu-id="48b8c-112">Gets a list of unresolved dependencies.</span></span>

### [<span data-ttu-id="48b8c-113">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="48b8c-113">Invoke-AzResourceMoverCommit</span></span>](Invoke-AzResourceMoverCommit.md)
<span data-ttu-id="48b8c-114">Über committ die Gruppe von Ressourcen, die im Anforderungstext enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="48b8c-114">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="48b8c-115">Der Commitvorgang wird für die moveResources im moveState-Element "CommitPending" oder "CommitFailed" ausgelöst, und bei einem erfolgreichen Abschluss übergeht "moveResource moveState" zu "Committed".</span><span class="sxs-lookup"><span data-stu-id="48b8c-115">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="48b8c-116">Um dem Benutzer die Voraussetzung für den Vorgang zu erfüllen, kann der Client den Vorgang aufrufen, bei dem die "validateOnly"-Eigenschaft auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="48b8c-116">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="48b8c-117">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="48b8c-117">Invoke-AzResourceMoverDiscard</span></span>](Invoke-AzResourceMoverDiscard.md)
<span data-ttu-id="48b8c-118">Verwirft die Gruppe von Ressourcen, die im Anforderungstext enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="48b8c-118">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="48b8c-119">Der Verwerfenvorgang wird für die moveResources im moveState-Element "CommitPending" oder "DiscardFailed" ausgelöst. Bei einem erfolgreichen Abschluss übertäft moveResource moveState einen Übergang zu "MovePending".</span><span class="sxs-lookup"><span data-stu-id="48b8c-119">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="48b8c-120">Um dem Benutzer die Voraussetzung für den Vorgang zu erfüllen, kann der Client den Vorgang aufrufen, bei dem die "validateOnly"-Eigenschaft auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="48b8c-120">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="48b8c-121">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="48b8c-121">Invoke-AzResourceMoverInitiateMove</span></span>](Invoke-AzResourceMoverInitiateMove.md)
<span data-ttu-id="48b8c-122">Verschiebt die Gruppe von Ressourcen, die im Anforderungstext enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="48b8c-122">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="48b8c-123">Der Verschiebevorgang wird ausgelöst, nachdem sich "moveResources" im moveState-Element "MovePending" oder "MoveFailed" befindet. Bei einem erfolgreichen Abschluss übergeht moveResource moveState einen Übergang zu "CommitPending".</span><span class="sxs-lookup"><span data-stu-id="48b8c-123">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="48b8c-124">Um dem Benutzer die Voraussetzung für den Vorgang zu erfüllen, kann der Client den Vorgang aufrufen, bei dem die "validateOnly"-Eigenschaft auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="48b8c-124">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="48b8c-125">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="48b8c-125">Invoke-AzResourceMoverPrepare</span></span>](Invoke-AzResourceMoverPrepare.md)
<span data-ttu-id="48b8c-126">Initiieren bereiten die Gruppe von Ressourcen vor, die im Anforderungstext enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="48b8c-126">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="48b8c-127">Der Vorbereitungsvorgang befindet sich in den moveResources, die sich im moveState-Element "PreparePending" oder "PrepareFailed" befinden, und nach einem erfolgreichen Abschluss über die moveResource moveState einen Übergang zu "MovePending".</span><span class="sxs-lookup"><span data-stu-id="48b8c-127">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="48b8c-128">Um dem Benutzer die Voraussetzung für den Vorgang zu erfüllen, kann der Client den Vorgang aufrufen, bei dem die "validateOnly"-Eigenschaft auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="48b8c-128">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="48b8c-129">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="48b8c-129">New-AzResourceMoverMoveCollection</span></span>](New-AzResourceMoverMoveCollection.md)
<span data-ttu-id="48b8c-130">Erstellt oder aktualisiert eine Sammlung zum Verschieben.</span><span class="sxs-lookup"><span data-stu-id="48b8c-130">Creates or updates a move collection.</span></span>

### [<span data-ttu-id="48b8c-131">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="48b8c-131">Remove-AzResourceMoverMoveCollection</span></span>](Remove-AzResourceMoverMoveCollection.md)
<span data-ttu-id="48b8c-132">Löscht eine Sammlung zum Verschieben.</span><span class="sxs-lookup"><span data-stu-id="48b8c-132">Deletes a move collection.</span></span>

### [<span data-ttu-id="48b8c-133">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="48b8c-133">Remove-AzResourceMoverMoveResource</span></span>](Remove-AzResourceMoverMoveResource.md)
<span data-ttu-id="48b8c-134">Löscht eine "Verschieben"-Ressource aus der Sammlung "Verschieben".</span><span class="sxs-lookup"><span data-stu-id="48b8c-134">Deletes a Move Resource from the move collection.</span></span>

### [<span data-ttu-id="48b8c-135">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="48b8c-135">Resolve-AzResourceMoverMoveCollectionDependency</span></span>](Resolve-AzResourceMoverMoveCollectionDependency.md)
<span data-ttu-id="48b8c-136">Berechnet, aufgelöst und überprüft die Abhängigkeiten der moveResources in der Move-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="48b8c-136">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

