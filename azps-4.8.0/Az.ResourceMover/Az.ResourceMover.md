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
# AZ. ResourceMover-Modul
## Beschreibung
Microsoft Azure PowerShell: ResourceMover-Cmdlets

## AZ. ResourceMover-Cmdlets
### [Add-AzResourceMoverMoveResource](Add-AzResourceMoverMoveResource.md)
Erstellt oder aktualisiert eine Verschiebungs Ressource in der Move-Sammlung.

### [Get-AzResourceMoverMoveCollection](Get-AzResourceMoverMoveCollection.md)
Ruft die Move-Sammlung ab.

### [Get-AzResourceMoverMoveResource](Get-AzResourceMoverMoveResource.md)
Ruft die Verschiebungs Ressource ab.

### [Get-AzResourceMoverUnresolvedDependency](Get-AzResourceMoverUnresolvedDependency.md)
Ruft eine Liste der nicht aufgelösten Abhängigkeiten ab.

### [Invoke-AzResourceMoverCommit](Invoke-AzResourceMoverCommit.md)
Übergibt den Satz von Ressourcen, die im Anforderungstext enthalten sind.
Der Commit-Vorgang wird für den moveResources im moveState "CommitPending" oder "CommitFailed" ausgelöst, wenn der moveResource erfolgreich abgeschlossen wird und der moveState einen Übergang zu Committed durchführen.
Um dem Benutzer die Voraussetzungen für den Vorgang zu erleichtern, kann der Client den Vorgang aufrufen, wobei die validateOnly-Eigenschaft auf true festgelegt ist.

### [Invoke-AzResourceMoverDiscard](Invoke-AzResourceMoverDiscard.md)
Verwirft den Satz von Ressourcen, die im Anforderungstext enthalten sind.
Der verwerfen-Vorgang wird auf der moveResources im moveState "CommitPending" oder "DiscardFailed" ausgelöst, bei einem erfolgreichen Abschluss der moveResource moveState einen Übergang zu MovePending.
Um dem Benutzer die Voraussetzungen für den Vorgang zu erleichtern, kann der Client den Vorgang aufrufen, wobei die validateOnly-Eigenschaft auf true festgelegt ist.

### [Invoke-AzResourceMoverInitiateMove](Invoke-AzResourceMoverInitiateMove.md)
Verschiebt die im Anforderungstext enthaltene Ressourcengruppe.
Der Verschiebevorgang wird ausgelöst, nachdem sich die moveResources im moveState "MovePending" oder "MoveFailed" befinden, bei einem erfolgreichen Abschluss der moveResource moveState einen Übergang zu CommitPending durchführen.
Um dem Benutzer die Voraussetzungen für den Vorgang zu erleichtern, kann der Client den Vorgang aufrufen, wobei die validateOnly-Eigenschaft auf true festgelegt ist.

### [Invoke-AzResourceMoverPrepare](Invoke-AzResourceMoverPrepare.md)
Initiiert vorbereiten für die Gruppe von Ressourcen, die im Anforderungstext enthalten sind.
Der Prepare-Vorgang befindet sich auf der moveResources, die sich im moveState "PreparePending" oder "PrepareFailed" befinden, bei einem erfolgreichen Abschluss der moveResource moveState einen Übergang zu MovePending.
Um dem Benutzer die Voraussetzungen für den Vorgang zu erleichtern, kann der Client den Vorgang aufrufen, wobei die validateOnly-Eigenschaft auf true festgelegt ist.

### [Neu – AzResourceMoverMoveCollection](New-AzResourceMoverMoveCollection.md)
Erstellt oder aktualisiert eine Move-Sammlung.

### [Remove-AzResourceMoverMoveCollection](Remove-AzResourceMoverMoveCollection.md)
Löscht eine Move-Sammlung.

### [Remove-AzResourceMoverMoveResource](Remove-AzResourceMoverMoveResource.md)
Löscht eine Verschiebungs Ressource aus der Move-Sammlung.

### [Resolve-AzResourceMoverMoveCollectionDependency](Resolve-AzResourceMoverMoveCollectionDependency.md)
Berechnet, löst und überprüft die Abhängigkeiten von moveResources in der Move-Sammlung.

