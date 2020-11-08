---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: b634b4e547b1e483037cec8efe5772b5460ee1b5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166650"
---
# <span data-ttu-id="18e77-101">AZ. ResourceMover-Modul</span><span class="sxs-lookup"><span data-stu-id="18e77-101">Az.ResourceMover Module</span></span>
## <span data-ttu-id="18e77-102">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="18e77-102">Description</span></span>
<span data-ttu-id="18e77-103">Microsoft Azure PowerShell: ResourceMover-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="18e77-103">Microsoft Azure PowerShell: ResourceMover cmdlets</span></span>

## <span data-ttu-id="18e77-104">AZ. ResourceMover-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="18e77-104">Az.ResourceMover Cmdlets</span></span>
### [<span data-ttu-id="18e77-105">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="18e77-105">Add-AzResourceMoverMoveResource</span></span>](Add-AzResourceMoverMoveResource.md)
<span data-ttu-id="18e77-106">Erstellt oder aktualisiert eine Verschiebungs Ressource in der Move-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="18e77-106">Creates or updates a Move Resource in the move collection.</span></span>

### [<span data-ttu-id="18e77-107">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="18e77-107">Get-AzResourceMoverMoveCollection</span></span>](Get-AzResourceMoverMoveCollection.md)
<span data-ttu-id="18e77-108">Ruft die Move-Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="18e77-108">Gets the move collection.</span></span>

### [<span data-ttu-id="18e77-109">Get-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="18e77-109">Get-AzResourceMoverMoveResource</span></span>](Get-AzResourceMoverMoveResource.md)
<span data-ttu-id="18e77-110">Ruft die Verschiebungs Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="18e77-110">Gets the Move Resource.</span></span>

### [<span data-ttu-id="18e77-111">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="18e77-111">Get-AzResourceMoverUnresolvedDependency</span></span>](Get-AzResourceMoverUnresolvedDependency.md)
<span data-ttu-id="18e77-112">Ruft eine Liste der nicht aufgelösten Abhängigkeiten ab.</span><span class="sxs-lookup"><span data-stu-id="18e77-112">Gets a list of unresolved dependencies.</span></span>

### [<span data-ttu-id="18e77-113">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="18e77-113">Invoke-AzResourceMoverCommit</span></span>](Invoke-AzResourceMoverCommit.md)
<span data-ttu-id="18e77-114">Übergibt den Satz von Ressourcen, die im Anforderungstext enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="18e77-114">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="18e77-115">Der Commit-Vorgang wird für den moveResources im moveState "CommitPending" oder "CommitFailed" ausgelöst, wenn der moveResource erfolgreich abgeschlossen wird und der moveState einen Übergang zu Committed durchführen.</span><span class="sxs-lookup"><span data-stu-id="18e77-115">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="18e77-116">Um dem Benutzer die Voraussetzungen für den Vorgang zu erleichtern, kann der Client den Vorgang aufrufen, wobei die validateOnly-Eigenschaft auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="18e77-116">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="18e77-117">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="18e77-117">Invoke-AzResourceMoverDiscard</span></span>](Invoke-AzResourceMoverDiscard.md)
<span data-ttu-id="18e77-118">Verwirft den Satz von Ressourcen, die im Anforderungstext enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="18e77-118">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="18e77-119">Der verwerfen-Vorgang wird auf der moveResources im moveState "CommitPending" oder "DiscardFailed" ausgelöst, bei einem erfolgreichen Abschluss der moveResource moveState einen Übergang zu MovePending.</span><span class="sxs-lookup"><span data-stu-id="18e77-119">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="18e77-120">Um dem Benutzer die Voraussetzungen für den Vorgang zu erleichtern, kann der Client den Vorgang aufrufen, wobei die validateOnly-Eigenschaft auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="18e77-120">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="18e77-121">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="18e77-121">Invoke-AzResourceMoverInitiateMove</span></span>](Invoke-AzResourceMoverInitiateMove.md)
<span data-ttu-id="18e77-122">Verschiebt die im Anforderungstext enthaltene Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="18e77-122">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="18e77-123">Der Verschiebevorgang wird ausgelöst, nachdem sich die moveResources im moveState "MovePending" oder "MoveFailed" befinden, bei einem erfolgreichen Abschluss der moveResource moveState einen Übergang zu CommitPending durchführen.</span><span class="sxs-lookup"><span data-stu-id="18e77-123">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="18e77-124">Um dem Benutzer die Voraussetzungen für den Vorgang zu erleichtern, kann der Client den Vorgang aufrufen, wobei die validateOnly-Eigenschaft auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="18e77-124">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="18e77-125">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="18e77-125">Invoke-AzResourceMoverPrepare</span></span>](Invoke-AzResourceMoverPrepare.md)
<span data-ttu-id="18e77-126">Initiiert vorbereiten für die Gruppe von Ressourcen, die im Anforderungstext enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="18e77-126">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="18e77-127">Der Prepare-Vorgang befindet sich auf der moveResources, die sich im moveState "PreparePending" oder "PrepareFailed" befinden, bei einem erfolgreichen Abschluss der moveResource moveState einen Übergang zu MovePending.</span><span class="sxs-lookup"><span data-stu-id="18e77-127">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="18e77-128">Um dem Benutzer die Voraussetzungen für den Vorgang zu erleichtern, kann der Client den Vorgang aufrufen, wobei die validateOnly-Eigenschaft auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="18e77-128">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="18e77-129">Neu – AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="18e77-129">New-AzResourceMoverMoveCollection</span></span>](New-AzResourceMoverMoveCollection.md)
<span data-ttu-id="18e77-130">Erstellt oder aktualisiert eine Move-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="18e77-130">Creates or updates a move collection.</span></span>

### [<span data-ttu-id="18e77-131">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="18e77-131">Remove-AzResourceMoverMoveCollection</span></span>](Remove-AzResourceMoverMoveCollection.md)
<span data-ttu-id="18e77-132">Löscht eine Move-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="18e77-132">Deletes a move collection.</span></span>

### [<span data-ttu-id="18e77-133">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="18e77-133">Remove-AzResourceMoverMoveResource</span></span>](Remove-AzResourceMoverMoveResource.md)
<span data-ttu-id="18e77-134">Löscht eine Verschiebungs Ressource aus der Move-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="18e77-134">Deletes a Move Resource from the move collection.</span></span>

### [<span data-ttu-id="18e77-135">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="18e77-135">Resolve-AzResourceMoverMoveCollectionDependency</span></span>](Resolve-AzResourceMoverMoveCollectionDependency.md)
<span data-ttu-id="18e77-136">Berechnet, löst und überprüft die Abhängigkeiten von moveResources in der Move-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="18e77-136">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

