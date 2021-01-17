---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: a662b6b405296b515d1b69c846775e5209a253dd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460071"
---
# <span data-ttu-id="46005-101">Az.Support-Modul</span><span class="sxs-lookup"><span data-stu-id="46005-101">Az.Support Module</span></span>
## <span data-ttu-id="46005-102">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46005-102">Description</span></span>
<span data-ttu-id="46005-103">Die Themen in diesem Abschnitt dokumentieren die Azure PowerShell-Cmdlets zum Erstellen und Verwalten von Azure-Supporttickets im Azure Resource Manager (ARM)-Framework.</span><span class="sxs-lookup"><span data-stu-id="46005-103">The topics in this section document the Azure PowerShell cmdlets for creating and managing Azure support tickets in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="46005-104">Die Cmdlets sind im Namespace "Microsoft.Azure.Commands.Support" vorhanden.</span><span class="sxs-lookup"><span data-stu-id="46005-104">The cmdlets exist in the Microsoft.Azure.Commands.Support namespace</span></span>

## <span data-ttu-id="46005-105">Az.Support-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="46005-105">Az.Support Cmdlets</span></span>
### [<span data-ttu-id="46005-106">Get-AzSupportService</span><span class="sxs-lookup"><span data-stu-id="46005-106">Get-AzSupportService</span></span>](Get-AzSupportService.md)
<span data-ttu-id="46005-107">Ruft die aktuelle Liste der Azure-Dienste ab, für die Support verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="46005-107">Gets the current list of Azure services for which support is available.</span></span> <span data-ttu-id="46005-108">Jeder Azure Service verfügt über einen eigenen Satz von Kategorien, die als Problemklassifizierung bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="46005-108">Each Azure service has its own set of categories called problem classification.</span></span> <span data-ttu-id="46005-109">Hier finden Sie die aktuelle Liste der Problemklassifizierung für einen Dienst mit "Get-AzSupportProblemClassification".</span><span class="sxs-lookup"><span data-stu-id="46005-109">Get the current list of problem classification for a service using Get-AzSupportProblemClassification.</span></span> <span data-ttu-id="46005-110">Sie können die GUID für Dienst- und Problemklassifizierung verwenden, um ein neues Supportticket mit "New-AzSupportTicket" zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="46005-110">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

### [<span data-ttu-id="46005-111">Get-AzSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="46005-111">Get-AzSupportProblemClassification</span></span>](Get-AzSupportProblemClassification.md)
<span data-ttu-id="46005-112">Ruft die aktuelle Liste der Problemklassifizierung für einen Azure-Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="46005-112">Gets the current list of problem classification for an Azure service.</span></span> <span data-ttu-id="46005-113">Sie können die GUID für Dienst- und Problemklassifizierung verwenden, um ein neues Supportticket mit "New-AzSupportTicket" zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="46005-113">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span> 

### [<span data-ttu-id="46005-114">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="46005-114">New-AzSupportContactProfileObject</span></span>](New-AzSupportContactProfileObject.md)
<span data-ttu-id="46005-115">Hilfs-Cmdlet zum Erstellen eines Supportkontaktprofilobjekts.</span><span class="sxs-lookup"><span data-stu-id="46005-115">Helper cmdlet to create a support contact profile object.</span></span> <span data-ttu-id="46005-116">Sie können dieses Objekt für New-AzSupportTicket verwenden.</span><span class="sxs-lookup"><span data-stu-id="46005-116">You can use this object for New-AzSupportTicket cmdlet.</span></span>

### [<span data-ttu-id="46005-117">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="46005-117">New-AzSupportTicket</span></span>](New-AzSupportTicket.md)
<span data-ttu-id="46005-118">Erstellt ein neues Azure-Supportticket.</span><span class="sxs-lookup"><span data-stu-id="46005-118">Creates a new Azure support ticket.</span></span> <span data-ttu-id="46005-119">Dieser Vorgang wird auf dem Verhalten der Seite "Supportanfrage für neue Azure- [und Azure-Plattform" modelliert.](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)</span><span class="sxs-lookup"><span data-stu-id="46005-119">This operation is modeled on the behavior of the Azure [New support request page](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview).</span></span>

### [<span data-ttu-id="46005-120">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="46005-120">Get-AzSupportTicket</span></span>](Get-AzSupportTicket.md)
<span data-ttu-id="46005-121">Ruft die Liste der Supporttickets ab.</span><span class="sxs-lookup"><span data-stu-id="46005-121">Gets the list of support tickets.</span></span> <span data-ttu-id="46005-122">Sie können vollständige Details zu Supporttickets nach Ticketname erhalten oder die Supporttickets nach *Status oder* *CreatedDate filtern.*</span><span class="sxs-lookup"><span data-stu-id="46005-122">You can get full support ticket details by ticket name or filter the support tickets by *Status* or *CreatedDate*.</span></span>

### [<span data-ttu-id="46005-123">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="46005-123">Update-AzSupportTicket</span></span>](Update-AzSupportTicket.md)
<span data-ttu-id="46005-124">Aktualisieren Sie den Schweregrad, den Status oder die Details von Kundenkontakten für ein Supportticket.</span><span class="sxs-lookup"><span data-stu-id="46005-124">Update a support ticket's severity, status or customer contact details.</span></span>

### [<span data-ttu-id="46005-125">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="46005-125">Get-AzSupportTicketCommunication</span></span>](Get-AzSupportTicketCommunication.md)
<span data-ttu-id="46005-126">Ruft Kommunikationen für ein Supportticket ab.</span><span class="sxs-lookup"><span data-stu-id="46005-126">Gets communications for a support ticket.</span></span> <span data-ttu-id="46005-127">Sie können die Kommunikation von Supporttickets auch nach *CreatedDate oder* *CommunicationType filtern.*</span><span class="sxs-lookup"><span data-stu-id="46005-127">You can also filter support ticket communications by *CreatedDate* or *CommunicationType*.</span></span> 

### [<span data-ttu-id="46005-128">New-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="46005-128">New-AzSupportTicketCommunication</span></span>](New-AzSupportTicketCommunication.md)
<span data-ttu-id="46005-129">Fügt einem Supportticket für Azure eine neue Kundenkommunikation hinzu.</span><span class="sxs-lookup"><span data-stu-id="46005-129">Adds a new customer communication to an Azure support ticket.</span></span> 



