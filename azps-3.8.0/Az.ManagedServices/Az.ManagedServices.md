---
Module Name: Az.ManagedServices
Module Guid: d2a8f744-8dcb-4a13-ba80-eb181ff365ad
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.managedservices
Help Version: 0.0.1
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 41d7b3afa19de95b677ff5db18ca38294b8559af
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004408"
---
# <span data-ttu-id="d6c7e-101">AZ. ManagedServices-Modul</span><span class="sxs-lookup"><span data-stu-id="d6c7e-101">Az.ManagedServices Module</span></span>
## <span data-ttu-id="d6c7e-102">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d6c7e-102">Description</span></span>
<span data-ttu-id="d6c7e-103">Dieses Feature wird von Kunden von Managed Service Providers (MSPs) verwendet.</span><span class="sxs-lookup"><span data-stu-id="d6c7e-103">This feature is used by customers of Managed Service Providers (MSPs).</span></span> <span data-ttu-id="d6c7e-104">Kunden geben msp die Möglichkeit, Ihr Abonnement zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="d6c7e-104">Customers give an MSP the ability to manage their subscription.</span></span> <span data-ttu-id="d6c7e-105">Neben der Gewährung des Zugriffs kann der Kunde auch den Zugriff entfernen oder vorhandene Access-Delegierungen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="d6c7e-105">In addition to granting access, the customer can also remove access or view existing access delegations.</span></span> <span data-ttu-id="d6c7e-106">MSPs können die Liste der Kunden anzeigen, die Ihnen den Zugriff auf Abonnements gewährt haben.</span><span class="sxs-lookup"><span data-stu-id="d6c7e-106">MSPs are able to view the list of customers who have granted them access to subscriptions.</span></span> <span data-ttu-id="d6c7e-107">Es gibt zwei Objekte, die an diesem Prozess beteiligt sind: eine Registrierungs Definition, die das MSP und die Rollendefinitionen identifiziert, die dem MSP gewährt werden.</span><span class="sxs-lookup"><span data-stu-id="d6c7e-107">There are two objects involved in this process: A registration definition which identifies the MSP and the role definitions granted to the MSP.</span></span> <span data-ttu-id="d6c7e-108">Das MSP kann dieses Objekt optional mithilfe eines Managed Services Marketplace definieren, der Zugriffs Aufgaben bietet, die ein Abonnement mit der Definition verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="d6c7e-108">The MSP can optionally define this object using a Managed Services marketplace offering Access assignments which associate a subscription with the definition.</span></span>

## <span data-ttu-id="d6c7e-109">AZ. ManagedServices-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="d6c7e-109">Az.ManagedServices Cmdlets</span></span>
### [<span data-ttu-id="d6c7e-110">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="d6c7e-110">Get-AzManagedServicesAssignment</span></span>](Get-AzManagedServicesAssignment.md)
<span data-ttu-id="d6c7e-111">Ruft eine Liste der Registrierungsaufgaben ab.</span><span class="sxs-lookup"><span data-stu-id="d6c7e-111">Gets a list of the registration assignments.</span></span>

### [<span data-ttu-id="d6c7e-112">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="d6c7e-112">Get-AzManagedServicesDefinition</span></span>](Get-AzManagedServicesDefinition.md)
<span data-ttu-id="d6c7e-113">Ruft eine Liste der Registrierungs Definitionen ab.</span><span class="sxs-lookup"><span data-stu-id="d6c7e-113">Gets a list of the registration definitions.</span></span>

### [<span data-ttu-id="d6c7e-114">Neu – AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="d6c7e-114">New-AzManagedServicesAssignment</span></span>](New-AzManagedServicesAssignment.md)
<span data-ttu-id="d6c7e-115">Erstellt eine Registrierungs Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="d6c7e-115">Creates a registration assignment.</span></span>

### [<span data-ttu-id="d6c7e-116">Neu – AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="d6c7e-116">New-AzManagedServicesDefinition</span></span>](New-AzManagedServicesDefinition.md)
<span data-ttu-id="d6c7e-117">Erstellt eine Registrierungs Definition.</span><span class="sxs-lookup"><span data-stu-id="d6c7e-117">Creates a registration definition.</span></span>

### [<span data-ttu-id="d6c7e-118">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="d6c7e-118">Remove-AzManagedServicesAssignment</span></span>](Remove-AzManagedServicesAssignment.md)
<span data-ttu-id="d6c7e-119">Löscht die Registrierungs Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="d6c7e-119">Deletes the registration assignment.</span></span>

### [<span data-ttu-id="d6c7e-120">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="d6c7e-120">Remove-AzManagedServicesDefinition</span></span>](Remove-AzManagedServicesDefinition.md)
<span data-ttu-id="d6c7e-121">Löscht die Registrierungs Definition.</span><span class="sxs-lookup"><span data-stu-id="d6c7e-121">Deletes the registration definition.</span></span>

