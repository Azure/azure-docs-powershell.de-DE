---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: a662b6b405296b515d1b69c846775e5209a253dd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165943"
---
# <span data-ttu-id="50d79-101">AZ. Support Modul</span><span class="sxs-lookup"><span data-stu-id="50d79-101">Az.Support Module</span></span>
## <span data-ttu-id="50d79-102">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="50d79-102">Description</span></span>
<span data-ttu-id="50d79-103">In den Themen in diesem Abschnitt werden die Azure PowerShell-Cmdlets zum Erstellen und Verwalten von Azure-Support Tickets im Azure Resource Manager (Arm)-Framework dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="50d79-103">The topics in this section document the Azure PowerShell cmdlets for creating and managing Azure support tickets in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="50d79-104">Die Cmdlets sind im Microsoft. Azure. Commands. Support-Namespace vorhanden</span><span class="sxs-lookup"><span data-stu-id="50d79-104">The cmdlets exist in the Microsoft.Azure.Commands.Support namespace</span></span>

## <span data-ttu-id="50d79-105">AZ. Support-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="50d79-105">Az.Support Cmdlets</span></span>
### [<span data-ttu-id="50d79-106">Get-AzSupportService</span><span class="sxs-lookup"><span data-stu-id="50d79-106">Get-AzSupportService</span></span>](Get-AzSupportService.md)
<span data-ttu-id="50d79-107">Ruft die aktuelle Liste der Azure-Dienste ab, für die Unterstützung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="50d79-107">Gets the current list of Azure services for which support is available.</span></span> <span data-ttu-id="50d79-108">Jeder Azure-Dienst verfügt über einen eigenen Satz von Kategorien, die so genannte Problem Klassifikation.</span><span class="sxs-lookup"><span data-stu-id="50d79-108">Each Azure service has its own set of categories called problem classification.</span></span> <span data-ttu-id="50d79-109">Rufen Sie die aktuelle Liste der Problemklassifizierung für einen Dienst mithilfe von Get-AzSupportProblemClassification ab.</span><span class="sxs-lookup"><span data-stu-id="50d79-109">Get the current list of problem classification for a service using Get-AzSupportProblemClassification.</span></span> <span data-ttu-id="50d79-110">Sie können die GUID des Diensts und der Problemklassifizierung verwenden, um ein neues Support Ticket mithilfe von New-AzSupportTicket zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="50d79-110">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

### [<span data-ttu-id="50d79-111">Get-AzSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="50d79-111">Get-AzSupportProblemClassification</span></span>](Get-AzSupportProblemClassification.md)
<span data-ttu-id="50d79-112">Ruft die aktuelle Liste der Problemklassifizierung für einen Azure-Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="50d79-112">Gets the current list of problem classification for an Azure service.</span></span> <span data-ttu-id="50d79-113">Sie können die GUID des Diensts und der Problemklassifizierung verwenden, um ein neues Support Ticket mithilfe von New-AzSupportTicket zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="50d79-113">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span> 

### [<span data-ttu-id="50d79-114">Neu – AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="50d79-114">New-AzSupportContactProfileObject</span></span>](New-AzSupportContactProfileObject.md)
<span data-ttu-id="50d79-115">Hilfsprogramm-Cmdlet zum Erstellen eines Support-Kontakt Profilobjekts.</span><span class="sxs-lookup"><span data-stu-id="50d79-115">Helper cmdlet to create a support contact profile object.</span></span> <span data-ttu-id="50d79-116">Sie können dieses Objekt für New-AzSupportTicket-Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="50d79-116">You can use this object for New-AzSupportTicket cmdlet.</span></span>

### [<span data-ttu-id="50d79-117">Neu – AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="50d79-117">New-AzSupportTicket</span></span>](New-AzSupportTicket.md)
<span data-ttu-id="50d79-118">Erstellt ein neues Azure-Support Ticket.</span><span class="sxs-lookup"><span data-stu-id="50d79-118">Creates a new Azure support ticket.</span></span> <span data-ttu-id="50d79-119">Dieser Vorgang wird anhand des Verhaltens der neuen Azure- [Support Anforderungsseite](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)modelliert.</span><span class="sxs-lookup"><span data-stu-id="50d79-119">This operation is modeled on the behavior of the Azure [New support request page](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview).</span></span>

### [<span data-ttu-id="50d79-120">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="50d79-120">Get-AzSupportTicket</span></span>](Get-AzSupportTicket.md)
<span data-ttu-id="50d79-121">Ruft die Liste der Support Tickets ab.</span><span class="sxs-lookup"><span data-stu-id="50d79-121">Gets the list of support tickets.</span></span> <span data-ttu-id="50d79-122">Sie können die vollständigen Support-Ticket Informationen nach dem Ticket Namen abrufen oder die Support-Tickets nach *Status* oder *"CreatedDate"* filtern.</span><span class="sxs-lookup"><span data-stu-id="50d79-122">You can get full support ticket details by ticket name or filter the support tickets by *Status* or *CreatedDate*.</span></span>

### [<span data-ttu-id="50d79-123">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="50d79-123">Update-AzSupportTicket</span></span>](Update-AzSupportTicket.md)
<span data-ttu-id="50d79-124">Aktualisieren des Schweregrads, des Status oder der Kundenkontakt Details eines Support Tickets</span><span class="sxs-lookup"><span data-stu-id="50d79-124">Update a support ticket's severity, status or customer contact details.</span></span>

### [<span data-ttu-id="50d79-125">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="50d79-125">Get-AzSupportTicketCommunication</span></span>](Get-AzSupportTicketCommunication.md)
<span data-ttu-id="50d79-126">Ruft die Kommunikation für ein Support Ticket ab.</span><span class="sxs-lookup"><span data-stu-id="50d79-126">Gets communications for a support ticket.</span></span> <span data-ttu-id="50d79-127">Sie können auch die Support-Ticket Kommunikation nach *"CreatedDate"*   oder *CommunicationType* filtern.</span><span class="sxs-lookup"><span data-stu-id="50d79-127">You can also filter support ticket communications by *CreatedDate* or *CommunicationType*.</span></span> 

### [<span data-ttu-id="50d79-128">Neu – AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="50d79-128">New-AzSupportTicketCommunication</span></span>](New-AzSupportTicketCommunication.md)
<span data-ttu-id="50d79-129">Fügt eine neue Kundenkommunikation zu einem Azure Support-Ticket hinzu.</span><span class="sxs-lookup"><span data-stu-id="50d79-129">Adds a new customer communication to an Azure support ticket.</span></span> 



