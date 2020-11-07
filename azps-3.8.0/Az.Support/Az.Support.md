---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: a662b6b405296b515d1b69c846775e5209a253dd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846340"
---
# AZ. Support Modul
## Beschreibung
In den Themen in diesem Abschnitt werden die Azure PowerShell-Cmdlets zum Erstellen und Verwalten von Azure-Support Tickets im Azure Resource Manager (Arm)-Framework dokumentiert. Die Cmdlets sind im Microsoft. Azure. Commands. Support-Namespace vorhanden

## AZ. Support-Cmdlets
### [Get-AzSupportService](Get-AzSupportService.md)
Ruft die aktuelle Liste der Azure-Dienste ab, für die Unterstützung verfügbar ist. Jeder Azure-Dienst verfügt über einen eigenen Satz von Kategorien, die so genannte Problem Klassifikation. Rufen Sie die aktuelle Liste der Problemklassifizierung für einen Dienst mithilfe von Get-AzSupportProblemClassification ab. Sie können die GUID des Diensts und der Problemklassifizierung verwenden, um ein neues Support Ticket mithilfe von New-AzSupportTicket zu erstellen.

### [Get-AzSupportProblemClassification](Get-AzSupportProblemClassification.md)
Ruft die aktuelle Liste der Problemklassifizierung für einen Azure-Dienst ab. Sie können die GUID des Diensts und der Problemklassifizierung verwenden, um ein neues Support Ticket mithilfe von New-AzSupportTicket zu erstellen. 

### [Neu – AzSupportContactProfileObject](New-AzSupportContactProfileObject.md)
Hilfsprogramm-Cmdlet zum Erstellen eines Support-Kontakt Profilobjekts. Sie können dieses Objekt für New-AzSupportTicket-Cmdlet verwenden.

### [Neu – AzSupportTicket](New-AzSupportTicket.md)
Erstellt ein neues Azure-Support Ticket. Dieser Vorgang wird anhand des Verhaltens der neuen Azure- [Support Anforderungsseite](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)modelliert.

### [Get-AzSupportTicket](Get-AzSupportTicket.md)
Ruft die Liste der Support Tickets ab. Sie können die vollständigen Support-Ticket Informationen nach dem Ticket Namen abrufen oder die Support-Tickets nach *Status* oder *"CreatedDate"* filtern.

### [Update-AzSupportTicket](Update-AzSupportTicket.md)
Aktualisieren des Schweregrads, des Status oder der Kundenkontakt Details eines Support Tickets

### [Get-AzSupportTicketCommunication](Get-AzSupportTicketCommunication.md)
Ruft die Kommunikation für ein Support Ticket ab. Sie können auch die Support-Ticket Kommunikation nach *"CreatedDate"*   oder *CommunicationType* filtern. 

### [Neu – AzSupportTicketCommunication](New-AzSupportTicketCommunication.md)
Fügt eine neue Kundenkommunikation zu einem Azure Support-Ticket hinzu. 



