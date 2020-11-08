---
Module Name: Az.ManagedServices
Module Guid: fe0ae00c-c482-4e5f-a837-fbc342fdc7e0
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.managedservices
Help Version: 0.0.2
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 4b3d901b606e9ee8127d0ef47ea7847338a69a4c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177898"
---
# <span data-ttu-id="3ac30-101">AZ. ManagedServices-Modul</span><span class="sxs-lookup"><span data-stu-id="3ac30-101">Az.ManagedServices Module</span></span>
## <span data-ttu-id="3ac30-102">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3ac30-102">Description</span></span>
<span data-ttu-id="3ac30-103">Dieses Feature wird von Kunden von Managed Service Providers (MSPs) verwendet.</span><span class="sxs-lookup"><span data-stu-id="3ac30-103">This feature is used by customers of Managed Service Providers (MSPs).</span></span> <span data-ttu-id="3ac30-104">Kunden geben einem msp die Möglichkeit, das Abonnement oder die Ressourcengruppe zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="3ac30-104">Customers give an MSP the ability to manage their subscription or resource group.</span></span> <span data-ttu-id="3ac30-105">Neben der Gewährung des Zugriffs kann der Kunde auch den Zugriff entfernen oder den vorhandenen Zugriff anzeigen.</span><span class="sxs-lookup"><span data-stu-id="3ac30-105">In addition to granting access, the customer can also remove access or view existing access.</span></span> <span data-ttu-id="3ac30-106">MSPs können die Liste der Kunden anzeigen, die Ihnen den Zugriff auf Abonnements gewährt haben.</span><span class="sxs-lookup"><span data-stu-id="3ac30-106">MSPs are able to view the list of customers who have granted them access to subscriptions.</span></span> <span data-ttu-id="3ac30-107">Es gibt zwei Objekte, die an diesem Prozess beteiligt sind: eine Registrierungs Definition, die das MSP und die Rollendefinitionen identifiziert, die den MSP-Benutzern gewährt wurden.</span><span class="sxs-lookup"><span data-stu-id="3ac30-107">There are two objects involved in this process: A registration definition which identifies the MSP and the role definitions granted to the MSP users.</span></span> <span data-ttu-id="3ac30-108">Das MSP kann dieses Objekt optional mithilfe eines Managed Services Marketplace definieren, der Zugriffs Aufgaben bietet, die ein Abonnement mit der Definition verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="3ac30-108">The MSP can optionally define this object using a Managed Services marketplace offering Access assignments which associate a subscription with the definition.</span></span>

## <span data-ttu-id="3ac30-109">AZ. ManagedServices-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="3ac30-109">Az.ManagedServices Cmdlets</span></span>
### [<span data-ttu-id="3ac30-110">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="3ac30-110">Get-AzManagedServicesAssignment</span></span>](Get-AzManagedServicesAssignment.md)
<span data-ttu-id="3ac30-111">Ruft eine bestimmte Registrierungs Aufgabe oder eine Liste der Registrierungsaufgaben ab.</span><span class="sxs-lookup"><span data-stu-id="3ac30-111">Gets a specific registration assignment or a list of the registration assignments.</span></span>

### [<span data-ttu-id="3ac30-112">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="3ac30-112">Get-AzManagedServicesDefinition</span></span>](Get-AzManagedServicesDefinition.md)
<span data-ttu-id="3ac30-113">Ruft eine bestimmte Registrierungs Definition oder eine Liste der Registrierungs Definitionen ab.</span><span class="sxs-lookup"><span data-stu-id="3ac30-113">Gets a specific registration definition or a list of the registration definitions.</span></span>

### [<span data-ttu-id="3ac30-114">Neu – AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="3ac30-114">New-AzManagedServicesAssignment</span></span>](New-AzManagedServicesAssignment.md)
<span data-ttu-id="3ac30-115">Erstellt eine Registrierungs Aufgabe oder aktualisiert sie.</span><span class="sxs-lookup"><span data-stu-id="3ac30-115">Creates or updates a registration assignment.</span></span>

### [<span data-ttu-id="3ac30-116">Neu – AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="3ac30-116">New-AzManagedServicesDefinition</span></span>](New-AzManagedServicesDefinition.md)
<span data-ttu-id="3ac30-117">Erstellt eine Registrierungs Definition oder aktualisiert sie.</span><span class="sxs-lookup"><span data-stu-id="3ac30-117">Creates or updates a registration definition.</span></span>

### [<span data-ttu-id="3ac30-118">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="3ac30-118">Remove-AzManagedServicesAssignment</span></span>](Remove-AzManagedServicesAssignment.md)
<span data-ttu-id="3ac30-119">Entfernt eine Registrierungs Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="3ac30-119">Removes a registration assignment.</span></span>

### [<span data-ttu-id="3ac30-120">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="3ac30-120">Remove-AzManagedServicesDefinition</span></span>](Remove-AzManagedServicesDefinition.md)
<span data-ttu-id="3ac30-121">Entfernt eine Registrierungs Definition.</span><span class="sxs-lookup"><span data-stu-id="3ac30-121">Removes a registration definition.</span></span>
