---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: a662b6b405296b515d1b69c846775e5209a253dd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150076"
---
# Az.Support-Modul
## Beschreibung
Die Themen in diesem Abschnitt dokumentieren die Azure PowerShell-Cmdlets zum Erstellen und Verwalten von Azure-Supporttickets im Azure Resource Manager (ARM)-Framework. Die Cmdlets sind im Namespace "Microsoft.Azure.Commands.Support" vorhanden.

## Az.Support-Cmdlets
### [Get-AzSupportService](Get-AzSupportService.md)
Ruft die aktuelle Liste der Azure-Dienste ab, für die Support verfügbar ist. Jeder Azure Service verfügt über einen eigenen Satz von Kategorien, die als Problemklassifizierung bezeichnet werden. Hier finden Sie die aktuelle Liste der Problemklassifizierung für einen Dienst mit "Get-AzSupportProblemClassification". Sie können die GUID für Dienst- und Problemklassifizierung verwenden, um mithilfe von "New-AzSupportTicket" ein neues Supportticket zu erstellen.

### [Get-AzSupportProblemClassification](Get-AzSupportProblemClassification.md)
Ruft die aktuelle Liste der Problemklassifizierung für einen Azure-Dienst ab. Sie können die GUID für Dienst- und Problemklassifizierung verwenden, um mithilfe von "New-AzSupportTicket" ein neues Supportticket zu erstellen. 

### [New-AzSupportContactProfileObject](New-AzSupportContactProfileObject.md)
Hilfs-Cmdlet zum Erstellen eines Supportkontaktprofilobjekts. Sie können dieses Objekt für New-AzSupportTicket verwenden.

### [New-AzSupportTicket](New-AzSupportTicket.md)
Erstellt ein neues Azure-Supportticket. Dieser Vorgang wird auf dem Verhalten der Seite "Supportanfrage für neue Azure- [und Azure-Plattform" modelliert.](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)

### [Get-AzSupportTicket](Get-AzSupportTicket.md)
Ruft die Liste der Supporttickets ab. Sie können vollständige Details zu Supporttickets nach Ticketname erhalten oder die Supporttickets nach *"Status"* oder *"CreatedDate" filtern.*

### [Update-AzSupportTicket](Update-AzSupportTicket.md)
Aktualisieren Sie den Schweregrad, den Status oder die Details von Kundenkontakten für ein Supportticket.

### [Get-AzSupportTicketCommunication](Get-AzSupportTicketCommunication.md)
Ruft Kommunikationen für ein Supportticket ab. Sie können die Kommunikation von Supporttickets auch nach *CreatedDate oder* *CommunicationType filtern.* 

### [New-AzSupportTicketCommunication](New-AzSupportTicketCommunication.md)
Fügt einem Supportticket für Azure eine neue Kundenkommunikation hinzu. 



