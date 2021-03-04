---
Module Name: Az.ManagedServices
Module Guid: fe0ae00c-c482-4e5f-a837-fbc342fdc7e0
Download Help Link: https://docs.microsoft.com/powershell/module/az.managedservices
Help Version: 0.0.2
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 33c6f65e258ee16b0ffb6a4616ffd1c7c5f16c77
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924067"
---
# Az.ManagedServices-Modul
## Beschreibung
Dieses Feature wird von Kunden von Managed Service Providers (MSPs) verwendet. Kunden geben einem MSP die Möglichkeit, sein Abonnement oder seine Ressourcengruppe zu verwalten. Zusätzlich zum Gewähren des Zugriffs kann der Kunde auch den Zugriff entfernen oder vorhandenen Zugriff anzeigen. MSPs können die Liste der Kunden anzeigen, die ihnen den Zugriff auf Abonnements gewährt haben. An diesem Prozess sind zwei Objekte beteiligt: eine Registrierungsdefinition, mit der der MSP und die Rollendefinitionen identifiziert werden, die den MSP-Benutzern gewährt werden. Der MSP kann dieses Objekt optional über einen Marketplace für verwaltete Dienste definieren, in dem Access-Zuweisungen angeboten werden, die der Definition ein Abonnement zuordnen.

## Az.ManagedServices-Cmdlets
### [Get-AzManagedServicesAssignment](Get-AzManagedServicesAssignment.md)
Ruft eine bestimmte Registrierungszuordnung oder eine Liste der Registrierungszuordnungen ab.

### [Get-AzManagedServicesDefinition](Get-AzManagedServicesDefinition.md)
Ruft eine bestimmte Registrierungsdefinition oder eine Liste der Registrierungsdefinitionen ab.

### [New-AzManagedServicesAssignment](New-AzManagedServicesAssignment.md)
Erstellt oder aktualisiert eine Registrierungszuordnung.

### [New-AzManagedServicesDefinition](New-AzManagedServicesDefinition.md)
Erstellt oder aktualisiert eine Registrierungsdefinition.

### [Remove-AzManagedServicesAssignment](Remove-AzManagedServicesAssignment.md)
Entfernt eine Registrierungszuordnung.

### [Remove-AzManagedServicesDefinition](Remove-AzManagedServicesDefinition.md)
Entfernt eine Registrierungsdefinition.
