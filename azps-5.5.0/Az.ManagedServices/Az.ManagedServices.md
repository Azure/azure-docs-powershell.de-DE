---
Module Name: Az.ManagedServices
Module Guid: fe0ae00c-c482-4e5f-a837-fbc342fdc7e0
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.managedservices
Help Version: 0.0.2
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 4b3d901b606e9ee8127d0ef47ea7847338a69a4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154724"
---
# Az.ManagedServices-Modul
## Beschreibung
Dieses Feature wird von Kunden verwalteter Dienstanbieter (Managed Service Providers, MSPs) verwendet. Kunden geben einem MSP die Möglichkeit, sein Abonnement oder seine Ressourcengruppe zu verwalten. Zusätzlich zum Gewähren des Zugriffs kann der Kunde auch den Zugriff entfernen oder vorhandenen Zugriff anzeigen. MSPs können die Liste der Kunden anzeigen, die ihnen den Zugriff auf Abonnements gewährt haben. An diesem Prozess sind zwei Objekte beteiligt: eine Registrierungsdefinition, die den MSP und die Rollendefinitionen identifiziert, die den Benutzer des MSP gewährt werden. Der MSP kann dieses Objekt optional mithilfe eines Marketplace für verwaltete Dienste definieren, der Access-Zuweisungen bietet, die der Definition ein Abonnement zuordnen.

## Az.ManagedServices-Cmdlets
### [Get-AzManagedServicesAssignment](Get-AzManagedServicesAssignment.md)
Ruft eine bestimmte Registrierungszuweisung oder eine Liste der Registrierungszuweisungen ab.

### [Get-AzManagedServicesDefinition](Get-AzManagedServicesDefinition.md)
Ruft eine bestimmte Registrierungsdefinition oder eine Liste der Registrierungsdefinitionen ab.

### [New-AzManagedServicesAssignment](New-AzManagedServicesAssignment.md)
Erstellt oder aktualisiert eine Registrierungszuweisung.

### [New-AzManagedServicesDefinition](New-AzManagedServicesDefinition.md)
Erstellt oder aktualisiert eine Registrierungsdefinition.

### [Remove-AzManagedServicesAssignment](Remove-AzManagedServicesAssignment.md)
Entfernt eine Registrierungszuweisung.

### [Remove-AzManagedServicesDefinition](Remove-AzManagedServicesDefinition.md)
Entfernt eine Registrierungsdefinition.
