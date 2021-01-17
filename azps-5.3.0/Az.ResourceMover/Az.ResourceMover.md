---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: b634b4e547b1e483037cec8efe5772b5460ee1b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377892"
---
# Az.ResourceMover-Modul
## Beschreibung
Microsoft Azure PowerShell: ResourceMover-Cmdlets

## Az.ResourceMover-Cmdlets
### [Add-AzResourceMoverMoveResource](Add-AzResourceMoverMoveResource.md)
Erstellt oder aktualisiert eine "Verschieben"-Ressource in der Sammlung "Verschieben".

### [Get-AzResourceMoverMoveCollection](Get-AzResourceMoverMoveCollection.md)
Ruft die Sammlung zum Verschieben ab.

### [Get-AzResourceMoverMoveResource](Get-AzResourceMoverMoveResource.md)
Ruft die "Verschieben"-Ressource ab.

### [Get-AzResourceMoverUnresolvedDependency](Get-AzResourceMoverUnresolvedDependency.md)
Ruft eine Liste der nicht aufgelösten Abhängigkeiten ab.

### [Invoke-AzResourceMoverCommit](Invoke-AzResourceMoverCommit.md)
Über committ die Gruppe von Ressourcen, die im Anforderungstext enthalten sind.
Der Commitvorgang wird für die moveResources im moveState-Element "CommitPending" oder "CommitFailed" ausgelöst, und bei einem erfolgreichen Abschluss übergeht "moveResource moveState" zu "Committed".
Um dem Benutzer die Voraussetzung für den Vorgang zu erfüllen, kann der Client den Vorgang aufrufen, bei dem die "validateOnly"-Eigenschaft auf "true" festgelegt ist.

### [Invoke-AzResourceMoverDiscard](Invoke-AzResourceMoverDiscard.md)
Verwirft die Gruppe von Ressourcen, die im Anforderungstext enthalten sind.
Der Verwerfenvorgang wird für die moveResources im moveState-Element "CommitPending" oder "DiscardFailed" ausgelöst. Bei einem erfolgreichen Abschluss übertäft moveResource moveState einen Übergang zu "MovePending".
Um dem Benutzer die Voraussetzung für den Vorgang zu erfüllen, kann der Client den Vorgang aufrufen, bei dem die "validateOnly"-Eigenschaft auf "true" festgelegt ist.

### [Invoke-AzResourceMoverInitiateMove](Invoke-AzResourceMoverInitiateMove.md)
Verschiebt die Gruppe von Ressourcen, die im Anforderungstext enthalten sind.
Der Verschiebevorgang wird ausgelöst, nachdem sich "moveResources" im moveState-Element "MovePending" oder "MoveFailed" befindet. Bei einem erfolgreichen Abschluss übertähnt moveResource moveState einen Übergang zu "CommitPending".
Um dem Benutzer die Voraussetzung für den Vorgang zu erfüllen, kann der Client den Vorgang aufrufen, bei dem die "validateOnly"-Eigenschaft auf "true" festgelegt ist.

### [Invoke-AzResourceMoverPrepare](Invoke-AzResourceMoverPrepare.md)
Initiieren bereiten die Gruppe von Ressourcen vor, die im Anforderungstext enthalten sind.
Der Vorbereitungsvorgang befindet sich in den moveResources, die sich im moveState-Element "PreparePending" oder "PrepareFailed" befinden. Bei einem erfolgreichen Abschluss übertähnt moveResource moveState einen Übergang zu "MovePending".
Um dem Benutzer die Voraussetzung für den Vorgang zu erfüllen, kann der Client den Vorgang aufrufen, bei dem die "validateOnly"-Eigenschaft auf "true" festgelegt ist.

### [New-AzResourceMoverMoveCollection](New-AzResourceMoverMoveCollection.md)
Erstellt oder aktualisiert eine Sammlung zum Verschieben.

### [Remove-AzResourceMoverMoveCollection](Remove-AzResourceMoverMoveCollection.md)
Löscht eine Sammlung zum Verschieben.

### [Remove-AzResourceMoverMoveResource](Remove-AzResourceMoverMoveResource.md)
Löscht eine "Verschieben"-Ressource aus der Sammlung "Verschieben".

### [Resolve-AzResourceMoverMoveCollectionDependency](Resolve-AzResourceMoverMoveCollectionDependency.md)
Berechnet, aufgelöst und überprüft die Abhängigkeiten der moveResources in der Move-Auflistung.

