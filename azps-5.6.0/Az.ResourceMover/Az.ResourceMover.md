---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: 0f43535baa284dbe9f7c69aee5a688443172089a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943606"
---
# <span data-ttu-id="977e5-101">Az.ResourceMover-Modul</span><span class="sxs-lookup"><span data-stu-id="977e5-101">Az.ResourceMover Module</span></span>
## <span data-ttu-id="977e5-102">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="977e5-102">Description</span></span>
<span data-ttu-id="977e5-103">Microsoft Azure PowerShell: ResourceMover-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="977e5-103">Microsoft Azure PowerShell: ResourceMover cmdlets</span></span>

## <span data-ttu-id="977e5-104">Az.ResourceMover-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="977e5-104">Az.ResourceMover Cmdlets</span></span>
### [<span data-ttu-id="977e5-105">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="977e5-105">Add-AzResourceMoverMoveResource</span></span>](Add-AzResourceMoverMoveResource.md)
<span data-ttu-id="977e5-106">Erstellt oder aktualisiert eine Ressource verschieben in der Move-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="977e5-106">Creates or updates a Move Resource in the move collection.</span></span>

### [<span data-ttu-id="977e5-107">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="977e5-107">Get-AzResourceMoverMoveCollection</span></span>](Get-AzResourceMoverMoveCollection.md)
<span data-ttu-id="977e5-108">Ruft die Move-Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="977e5-108">Gets the move collection.</span></span>

### [<span data-ttu-id="977e5-109">Get-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="977e5-109">Get-AzResourceMoverMoveResource</span></span>](Get-AzResourceMoverMoveResource.md)
<span data-ttu-id="977e5-110">Ruft die Ressource verschieben ab.</span><span class="sxs-lookup"><span data-stu-id="977e5-110">Gets the Move Resource.</span></span>

### [<span data-ttu-id="977e5-111">Get-AzResourceMoverRequiredForResources</span><span class="sxs-lookup"><span data-stu-id="977e5-111">Get-AzResourceMoverRequiredForResources</span></span>](Get-AzResourceMoverRequiredForResources.md)
<span data-ttu-id="977e5-112">Liste der Verschieberessourcen, für die eine Armressource erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="977e5-112">List of the move resources for which an arm resource is required for.</span></span>

### [<span data-ttu-id="977e5-113">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="977e5-113">Get-AzResourceMoverUnresolvedDependency</span></span>](Get-AzResourceMoverUnresolvedDependency.md)
<span data-ttu-id="977e5-114">Ruft eine Liste der nicht aufgelösten Abhängigkeiten ab.</span><span class="sxs-lookup"><span data-stu-id="977e5-114">Gets a list of unresolved dependencies.</span></span>

### [<span data-ttu-id="977e5-115">Invoke-AzResourceMoverBulkRemove</span><span class="sxs-lookup"><span data-stu-id="977e5-115">Invoke-AzResourceMoverBulkRemove</span></span>](Invoke-AzResourceMoverBulkRemove.md)
<span data-ttu-id="977e5-116">Entfernt den Satz der im Anforderungstext enthaltenen Verschieberessourcen aus der Move-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="977e5-116">Removes the set of move resources included in the request body from move collection.</span></span>
<span data-ttu-id="977e5-117">Die Orchestrierung erfolgt nach Dienst.</span><span class="sxs-lookup"><span data-stu-id="977e5-117">The orchestration is done by service.</span></span>
<span data-ttu-id="977e5-118">Um dem Benutzer die Voraussetzung für den Vorgang zu erfüllen, kann der Client den Vorgang aufrufen, bei dem die Eigenschaft validateOnly auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="977e5-118">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="977e5-119">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="977e5-119">Invoke-AzResourceMoverCommit</span></span>](Invoke-AzResourceMoverCommit.md)
<span data-ttu-id="977e5-120">Über commits the set of resources included in the request body.</span><span class="sxs-lookup"><span data-stu-id="977e5-120">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="977e5-121">Der Commitvorgang wird für die moveResources im moveState "CommitPending" oder "CommitFailed" ausgelöst, bei einem erfolgreichen Abschluss übergeht moveResource moveState einen Übergang zu Committed.</span><span class="sxs-lookup"><span data-stu-id="977e5-121">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="977e5-122">Um dem Benutzer die Voraussetzung für den Vorgang zu erfüllen, kann der Client den Vorgang aufrufen, bei dem die Eigenschaft validateOnly auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="977e5-122">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="977e5-123">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="977e5-123">Invoke-AzResourceMoverDiscard</span></span>](Invoke-AzResourceMoverDiscard.md)
<span data-ttu-id="977e5-124">Verwirft die im Anforderungstext enthaltenen Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="977e5-124">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="977e5-125">Der verwerfende Vorgang wird für die moveResources im moveState "CommitPending" oder "DiscardFailed" ausgelöst, bei einem erfolgreichen Abschluss übergeht moveResource moveState einen Übergang zu MovePending.</span><span class="sxs-lookup"><span data-stu-id="977e5-125">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="977e5-126">Um dem Benutzer die Voraussetzung für den Vorgang zu erfüllen, kann der Client den Vorgang aufrufen, bei dem die Eigenschaft validateOnly auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="977e5-126">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="977e5-127">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="977e5-127">Invoke-AzResourceMoverInitiateMove</span></span>](Invoke-AzResourceMoverInitiateMove.md)
<span data-ttu-id="977e5-128">Verschiebt den Satz von Ressourcen, die im Anforderungstext enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="977e5-128">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="977e5-129">Der Verschiebenvorgang wird ausgelöst, nachdem sich die moveResources im moveState "MovePending" oder "MoveFailed" befinden. Bei erfolgreichem Abschluss übergeht moveResource moveState einen Übergang zu CommitPending.</span><span class="sxs-lookup"><span data-stu-id="977e5-129">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="977e5-130">Um dem Benutzer die Voraussetzung für den Vorgang zu erfüllen, kann der Client den Vorgang aufrufen, bei dem die Eigenschaft validateOnly auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="977e5-130">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="977e5-131">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="977e5-131">Invoke-AzResourceMoverPrepare</span></span>](Invoke-AzResourceMoverPrepare.md)
<span data-ttu-id="977e5-132">Initiiert die Vorbereitung für den Satz von Ressourcen, die im Anforderungstext enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="977e5-132">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="977e5-133">Der Vorbereitungsvorgang befindet sich auf den moveResources, die sich im moveState "PreparePending" oder "PrepareFailed" befinden, nach einem erfolgreichen Abschluss über die moveResource moveState einen Übergang zu MovePending.</span><span class="sxs-lookup"><span data-stu-id="977e5-133">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="977e5-134">Um dem Benutzer die Voraussetzung für den Vorgang zu erfüllen, kann der Client den Vorgang aufrufen, bei dem die Eigenschaft validateOnly auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="977e5-134">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="977e5-135">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="977e5-135">New-AzResourceMoverMoveCollection</span></span>](New-AzResourceMoverMoveCollection.md)
<span data-ttu-id="977e5-136">Erstellt oder aktualisiert eine Verschiebesammlung.</span><span class="sxs-lookup"><span data-stu-id="977e5-136">Creates or updates a move collection.</span></span>

### [<span data-ttu-id="977e5-137">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="977e5-137">Remove-AzResourceMoverMoveCollection</span></span>](Remove-AzResourceMoverMoveCollection.md)
<span data-ttu-id="977e5-138">Löscht eine Verschiebesammlung.</span><span class="sxs-lookup"><span data-stu-id="977e5-138">Deletes a move collection.</span></span>

### [<span data-ttu-id="977e5-139">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="977e5-139">Remove-AzResourceMoverMoveResource</span></span>](Remove-AzResourceMoverMoveResource.md)
<span data-ttu-id="977e5-140">Löscht eine Ressource verschieben aus der Sammlung verschieben.</span><span class="sxs-lookup"><span data-stu-id="977e5-140">Deletes a Move Resource from the move collection.</span></span>

### [<span data-ttu-id="977e5-141">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="977e5-141">Resolve-AzResourceMoverMoveCollectionDependency</span></span>](Resolve-AzResourceMoverMoveCollectionDependency.md)
<span data-ttu-id="977e5-142">Berechnet, löst und überprüft die Abhängigkeiten der moveResources in der Move-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="977e5-142">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

