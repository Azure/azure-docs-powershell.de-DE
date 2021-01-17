---
Module Name: Az.ManagedServices
Module Guid: fe0ae00c-c482-4e5f-a837-fbc342fdc7e0
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.managedservices
Help Version: 0.0.2
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 4b3d901b606e9ee8127d0ef47ea7847338a69a4c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470434"
---
# <span data-ttu-id="29909-101">Az.ManagedServices-Modul</span><span class="sxs-lookup"><span data-stu-id="29909-101">Az.ManagedServices Module</span></span>
## <span data-ttu-id="29909-102">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29909-102">Description</span></span>
<span data-ttu-id="29909-103">Dieses Feature wird von Kunden verwalteter Dienstanbieter (Managed Service Providers, MSPs) verwendet.</span><span class="sxs-lookup"><span data-stu-id="29909-103">This feature is used by customers of Managed Service Providers (MSPs).</span></span> <span data-ttu-id="29909-104">Kunden geben einem MSP die Möglichkeit, sein Abonnement oder seine Ressourcengruppe zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="29909-104">Customers give an MSP the ability to manage their subscription or resource group.</span></span> <span data-ttu-id="29909-105">Zusätzlich zum Gewähren des Zugriffs kann der Kunde auch den Zugriff entfernen oder vorhandenen Zugriff anzeigen.</span><span class="sxs-lookup"><span data-stu-id="29909-105">In addition to granting access, the customer can also remove access or view existing access.</span></span> <span data-ttu-id="29909-106">MSPs können die Liste der Kunden anzeigen, die ihnen den Zugriff auf Abonnements gewährt haben.</span><span class="sxs-lookup"><span data-stu-id="29909-106">MSPs are able to view the list of customers who have granted them access to subscriptions.</span></span> <span data-ttu-id="29909-107">An diesem Prozess sind zwei Objekte beteiligt: eine Registrierungsdefinition, die den MSP und die Rollendefinitionen identifiziert, die den Benutzer des MSP gewährt werden.</span><span class="sxs-lookup"><span data-stu-id="29909-107">There are two objects involved in this process: A registration definition which identifies the MSP and the role definitions granted to the MSP users.</span></span> <span data-ttu-id="29909-108">Der MSP kann dieses Objekt optional mithilfe eines Marketplace für verwaltete Dienste definieren, der Access-Zuweisungen bietet, die der Definition ein Abonnement zuordnen.</span><span class="sxs-lookup"><span data-stu-id="29909-108">The MSP can optionally define this object using a Managed Services marketplace offering Access assignments which associate a subscription with the definition.</span></span>

## <span data-ttu-id="29909-109">Az.ManagedServices-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="29909-109">Az.ManagedServices Cmdlets</span></span>
### [<span data-ttu-id="29909-110">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="29909-110">Get-AzManagedServicesAssignment</span></span>](Get-AzManagedServicesAssignment.md)
<span data-ttu-id="29909-111">Ruft eine bestimmte Registrierungszuweisung oder eine Liste der Registrierungszuweisungen ab.</span><span class="sxs-lookup"><span data-stu-id="29909-111">Gets a specific registration assignment or a list of the registration assignments.</span></span>

### [<span data-ttu-id="29909-112">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="29909-112">Get-AzManagedServicesDefinition</span></span>](Get-AzManagedServicesDefinition.md)
<span data-ttu-id="29909-113">Ruft eine bestimmte Registrierungsdefinition oder eine Liste der Registrierungsdefinitionen ab.</span><span class="sxs-lookup"><span data-stu-id="29909-113">Gets a specific registration definition or a list of the registration definitions.</span></span>

### [<span data-ttu-id="29909-114">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="29909-114">New-AzManagedServicesAssignment</span></span>](New-AzManagedServicesAssignment.md)
<span data-ttu-id="29909-115">Erstellt oder aktualisiert eine Registrierungszuweisung.</span><span class="sxs-lookup"><span data-stu-id="29909-115">Creates or updates a registration assignment.</span></span>

### [<span data-ttu-id="29909-116">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="29909-116">New-AzManagedServicesDefinition</span></span>](New-AzManagedServicesDefinition.md)
<span data-ttu-id="29909-117">Erstellt oder aktualisiert eine Registrierungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="29909-117">Creates or updates a registration definition.</span></span>

### [<span data-ttu-id="29909-118">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="29909-118">Remove-AzManagedServicesAssignment</span></span>](Remove-AzManagedServicesAssignment.md)
<span data-ttu-id="29909-119">Entfernt eine Registrierungszuweisung.</span><span class="sxs-lookup"><span data-stu-id="29909-119">Removes a registration assignment.</span></span>

### [<span data-ttu-id="29909-120">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="29909-120">Remove-AzManagedServicesDefinition</span></span>](Remove-AzManagedServicesDefinition.md)
<span data-ttu-id="29909-121">Entfernt eine Registrierungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="29909-121">Removes a registration definition.</span></span>
