---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: b02401044f3b01a73954ac199cc15457cddb795a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932171"
---
# Az.Support-Modul
## Beschreibung
Die Themen in diesem Abschnitt dokumentieren die Azure PowerShell-Cmdlets zum Erstellen und Verwalten von Azure-Supporttickets im Azure Resource Manager (ARM)-Framework. Die Cmdlets sind im Microsoft.Azure.Commands.Support-Namespace vorhanden.

## Az.Support-Cmdlets
### [Get-AzSupportService](Get-AzSupportService.md)
Ruft die aktuelle Liste der Azure-Dienste ab, für die Support verfügbar ist. Jeder Azure-Dienst verfügt über einen eigenen Satz von Kategorien, die als Problemklassifizierung bezeichnet werden. Hier erhalten Sie die aktuelle Liste der Problemklassifizierung für einen Dienst mit Get-AzSupportProblemClassification. Sie können die GUID für Dienst- und Problemklassifizierung verwenden, um ein neues Supportticket mit New-AzSupportTicket zu erstellen.

### [Get-AzSupportProblemClassification](Get-AzSupportProblemClassification.md)
Ruft die aktuelle Liste der Problemklassifizierung für einen Azure-Dienst ab. Sie können die GUID für Dienst- und Problemklassifizierung verwenden, um ein neues Supportticket mit New-AzSupportTicket zu erstellen. 

### [New-AzSupportContactProfileObject](New-AzSupportContactProfileObject.md)
Hilfs-Cmdlet zum Erstellen eines Supportkontaktprofilobjekts. Sie können dieses Objekt für das cmdlet New-AzSupportTicket verwenden.

### [New-AzSupportTicket](New-AzSupportTicket.md)
Erstellt ein neues Azure-Supportticket. Dieser Vorgang wird nach dem Verhalten der Azure [New-Supportanforderungsseite modelliert.](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)

### [Get-AzSupportTicket](Get-AzSupportTicket.md)
Ruft die Liste der Supporttickets ab. Sie können vollständige Supportticketdetails nach Ticketname erhalten oder die Supporttickets nach *Status oder* *CreatedDate filtern.*

### [Update-AzSupportTicket](Update-AzSupportTicket.md)
Aktualisieren Sie den Schweregrad, den Status oder die Kontaktdetails eines Supporttickets.

### [Get-AzSupportTicketCommunication](Get-AzSupportTicketCommunication.md)
Ruft Kommunikationen für ein Supportticket ab. Sie können auch die Kommunikation mit Supporttickets nach *CreatedDate oder* *CommunicationType filtern.* 

### [New-AzSupportTicketCommunication](New-AzSupportTicketCommunication.md)
Fügt einem Azure-Supportticket eine neue Kundenkommunikation hinzu. 



