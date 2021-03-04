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
# Az.ResourceMover-Modul
## Beschreibung
Microsoft Azure PowerShell: ResourceMover-Cmdlets

## Az.ResourceMover-Cmdlets
### [Add-AzResourceMoverMoveResource](Add-AzResourceMoverMoveResource.md)
Erstellt oder aktualisiert eine Ressource verschieben in der Move-Sammlung.

### [Get-AzResourceMoverMoveCollection](Get-AzResourceMoverMoveCollection.md)
Ruft die Move-Sammlung ab.

### [Get-AzResourceMoverMoveResource](Get-AzResourceMoverMoveResource.md)
Ruft die Ressource verschieben ab.

### [Get-AzResourceMoverRequiredForResources](Get-AzResourceMoverRequiredForResources.md)
Liste der Verschieberessourcen, für die eine Armressource erforderlich ist.

### [Get-AzResourceMoverUnresolvedDependency](Get-AzResourceMoverUnresolvedDependency.md)
Ruft eine Liste der nicht aufgelösten Abhängigkeiten ab.

### [Invoke-AzResourceMoverBulkRemove](Invoke-AzResourceMoverBulkRemove.md)
Entfernt den Satz der im Anforderungstext enthaltenen Verschieberessourcen aus der Move-Auflistung.
Die Orchestrierung erfolgt nach Dienst.
Um dem Benutzer die Voraussetzung für den Vorgang zu erfüllen, kann der Client den Vorgang aufrufen, bei dem die Eigenschaft validateOnly auf true festgelegt ist.

### [Invoke-AzResourceMoverCommit](Invoke-AzResourceMoverCommit.md)
Über commits the set of resources included in the request body.
Der Commitvorgang wird für die moveResources im moveState "CommitPending" oder "CommitFailed" ausgelöst, bei einem erfolgreichen Abschluss übergeht moveResource moveState einen Übergang zu Committed.
Um dem Benutzer die Voraussetzung für den Vorgang zu erfüllen, kann der Client den Vorgang aufrufen, bei dem die Eigenschaft validateOnly auf true festgelegt ist.

### [Invoke-AzResourceMoverDiscard](Invoke-AzResourceMoverDiscard.md)
Verwirft die im Anforderungstext enthaltenen Ressourcen.
Der verwerfende Vorgang wird für die moveResources im moveState "CommitPending" oder "DiscardFailed" ausgelöst, bei einem erfolgreichen Abschluss übergeht moveResource moveState einen Übergang zu MovePending.
Um dem Benutzer die Voraussetzung für den Vorgang zu erfüllen, kann der Client den Vorgang aufrufen, bei dem die Eigenschaft validateOnly auf true festgelegt ist.

### [Invoke-AzResourceMoverInitiateMove](Invoke-AzResourceMoverInitiateMove.md)
Verschiebt den Satz von Ressourcen, die im Anforderungstext enthalten sind.
Der Verschiebenvorgang wird ausgelöst, nachdem sich die moveResources im moveState "MovePending" oder "MoveFailed" befinden. Bei erfolgreichem Abschluss übergeht moveResource moveState einen Übergang zu CommitPending.
Um dem Benutzer die Voraussetzung für den Vorgang zu erfüllen, kann der Client den Vorgang aufrufen, bei dem die Eigenschaft validateOnly auf true festgelegt ist.

### [Invoke-AzResourceMoverPrepare](Invoke-AzResourceMoverPrepare.md)
Initiiert die Vorbereitung für den Satz von Ressourcen, die im Anforderungstext enthalten sind.
Der Vorbereitungsvorgang befindet sich auf den moveResources, die sich im moveState "PreparePending" oder "PrepareFailed" befinden, nach einem erfolgreichen Abschluss über die moveResource moveState einen Übergang zu MovePending.
Um dem Benutzer die Voraussetzung für den Vorgang zu erfüllen, kann der Client den Vorgang aufrufen, bei dem die Eigenschaft validateOnly auf true festgelegt ist.

### [New-AzResourceMoverMoveCollection](New-AzResourceMoverMoveCollection.md)
Erstellt oder aktualisiert eine Verschiebesammlung.

### [Remove-AzResourceMoverMoveCollection](Remove-AzResourceMoverMoveCollection.md)
Löscht eine Verschiebesammlung.

### [Remove-AzResourceMoverMoveResource](Remove-AzResourceMoverMoveResource.md)
Löscht eine Ressource verschieben aus der Sammlung verschieben.

### [Resolve-AzResourceMoverMoveCollectionDependency](Resolve-AzResourceMoverMoveCollectionDependency.md)
Berechnet, löst und überprüft die Abhängigkeiten der moveResources in der Move-Auflistung.

