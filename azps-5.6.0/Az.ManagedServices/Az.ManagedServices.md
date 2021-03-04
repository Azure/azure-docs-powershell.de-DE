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
# <span data-ttu-id="f30f0-101">Az.ManagedServices-Modul</span><span class="sxs-lookup"><span data-stu-id="f30f0-101">Az.ManagedServices Module</span></span>
## <span data-ttu-id="f30f0-102">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f30f0-102">Description</span></span>
<span data-ttu-id="f30f0-103">Dieses Feature wird von Kunden von Managed Service Providers (MSPs) verwendet.</span><span class="sxs-lookup"><span data-stu-id="f30f0-103">This feature is used by customers of Managed Service Providers (MSPs).</span></span> <span data-ttu-id="f30f0-104">Kunden geben einem MSP die Möglichkeit, sein Abonnement oder seine Ressourcengruppe zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="f30f0-104">Customers give an MSP the ability to manage their subscription or resource group.</span></span> <span data-ttu-id="f30f0-105">Zusätzlich zum Gewähren des Zugriffs kann der Kunde auch den Zugriff entfernen oder vorhandenen Zugriff anzeigen.</span><span class="sxs-lookup"><span data-stu-id="f30f0-105">In addition to granting access, the customer can also remove access or view existing access.</span></span> <span data-ttu-id="f30f0-106">MSPs können die Liste der Kunden anzeigen, die ihnen den Zugriff auf Abonnements gewährt haben.</span><span class="sxs-lookup"><span data-stu-id="f30f0-106">MSPs are able to view the list of customers who have granted them access to subscriptions.</span></span> <span data-ttu-id="f30f0-107">An diesem Prozess sind zwei Objekte beteiligt: eine Registrierungsdefinition, mit der der MSP und die Rollendefinitionen identifiziert werden, die den MSP-Benutzern gewährt werden.</span><span class="sxs-lookup"><span data-stu-id="f30f0-107">There are two objects involved in this process: A registration definition which identifies the MSP and the role definitions granted to the MSP users.</span></span> <span data-ttu-id="f30f0-108">Der MSP kann dieses Objekt optional über einen Marketplace für verwaltete Dienste definieren, in dem Access-Zuweisungen angeboten werden, die der Definition ein Abonnement zuordnen.</span><span class="sxs-lookup"><span data-stu-id="f30f0-108">The MSP can optionally define this object using a Managed Services marketplace offering Access assignments which associate a subscription with the definition.</span></span>

## <span data-ttu-id="f30f0-109">Az.ManagedServices-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="f30f0-109">Az.ManagedServices Cmdlets</span></span>
### [<span data-ttu-id="f30f0-110">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="f30f0-110">Get-AzManagedServicesAssignment</span></span>](Get-AzManagedServicesAssignment.md)
<span data-ttu-id="f30f0-111">Ruft eine bestimmte Registrierungszuordnung oder eine Liste der Registrierungszuordnungen ab.</span><span class="sxs-lookup"><span data-stu-id="f30f0-111">Gets a specific registration assignment or a list of the registration assignments.</span></span>

### [<span data-ttu-id="f30f0-112">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="f30f0-112">Get-AzManagedServicesDefinition</span></span>](Get-AzManagedServicesDefinition.md)
<span data-ttu-id="f30f0-113">Ruft eine bestimmte Registrierungsdefinition oder eine Liste der Registrierungsdefinitionen ab.</span><span class="sxs-lookup"><span data-stu-id="f30f0-113">Gets a specific registration definition or a list of the registration definitions.</span></span>

### [<span data-ttu-id="f30f0-114">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="f30f0-114">New-AzManagedServicesAssignment</span></span>](New-AzManagedServicesAssignment.md)
<span data-ttu-id="f30f0-115">Erstellt oder aktualisiert eine Registrierungszuordnung.</span><span class="sxs-lookup"><span data-stu-id="f30f0-115">Creates or updates a registration assignment.</span></span>

### [<span data-ttu-id="f30f0-116">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="f30f0-116">New-AzManagedServicesDefinition</span></span>](New-AzManagedServicesDefinition.md)
<span data-ttu-id="f30f0-117">Erstellt oder aktualisiert eine Registrierungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="f30f0-117">Creates or updates a registration definition.</span></span>

### [<span data-ttu-id="f30f0-118">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="f30f0-118">Remove-AzManagedServicesAssignment</span></span>](Remove-AzManagedServicesAssignment.md)
<span data-ttu-id="f30f0-119">Entfernt eine Registrierungszuordnung.</span><span class="sxs-lookup"><span data-stu-id="f30f0-119">Removes a registration assignment.</span></span>

### [<span data-ttu-id="f30f0-120">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="f30f0-120">Remove-AzManagedServicesDefinition</span></span>](Remove-AzManagedServicesDefinition.md)
<span data-ttu-id="f30f0-121">Entfernt eine Registrierungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="f30f0-121">Removes a registration definition.</span></span>
