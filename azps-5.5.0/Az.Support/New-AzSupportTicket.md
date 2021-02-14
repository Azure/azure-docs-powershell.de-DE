---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
ms.openlocfilehash: 31e529ce30be608c5bd3167044b82f8094c1d248
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150052"
---
# <span data-ttu-id="b9a59-101">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="b9a59-101">New-AzSupportTicket</span></span>

## <span data-ttu-id="b9a59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9a59-102">SYNOPSIS</span></span>
<span data-ttu-id="b9a59-103">Erstellt ein Supportticket.</span><span class="sxs-lookup"><span data-stu-id="b9a59-103">Creates a support ticket.</span></span>

## <span data-ttu-id="b9a59-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9a59-104">SYNTAX</span></span>

### <span data-ttu-id="b9a59-105">CreateSupportTicketWithContactDetailParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b9a59-105">CreateSupportTicketWithContactDetailParameterSet (Default)</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9a59-106">CreateSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9a59-106">CreateSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9a59-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9a59-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9a59-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9a59-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9a59-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9a59-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9a59-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9a59-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9a59-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b9a59-111">DESCRIPTION</span></span>
<span data-ttu-id="b9a59-112">Dieses Cmdlet kann verwendet werden, um ein Supportticket für Abrechnungs-, Abonnementverwaltungs-, Kontingent- oder technische Probleme zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b9a59-112">This cmdlet can be used to create a support ticket for Billing, Subscription Management, Quota or Technical issues.</span></span> <span data-ttu-id="b9a59-113">Verwenden Get-AzSupportService und Get-AzSupportProblemClassification cmdlets zum Identifizieren des Azure-Diensts bzw. der zugehörigen Problemklassifizierungen, für die Sie Support anfordern möchten.</span><span class="sxs-lookup"><span data-stu-id="b9a59-113">Use Get-AzSupportService and Get-AzSupportProblemClassification cmdlets to identify the Azure service and it's corresponding problem classifications respectively for which you want to request support.</span></span> <span data-ttu-id="b9a59-114">Sie müssen die folgenden Parameter angeben:</span><span class="sxs-lookup"><span data-stu-id="b9a59-114">You must specify the following parameters:</span></span> 

    • Title
    • Description
    • Severity level
    • ProblemClassificationId
    • CustomerContactDetail (or individual customer contact parameters)

<span data-ttu-id="b9a59-115">Sie können das New-AzSupportContactProfileObject zum Erstellen des CustomerContactDetail-Objekts verwenden.</span><span class="sxs-lookup"><span data-stu-id="b9a59-115">You can use New-AzSupportContactProfileObject helper cmdlet to create CustomerContactDetail object.</span></span>

<span data-ttu-id="b9a59-116">Cloudlösungsanbieter können ein Supportticket für die Abonnements ihres Kunden erstellen, indem sie sich beim Mandanten des Kunden anmelden und seine Home Tenant-ID mithilfe des Parameters *"CSPHomeTenantId"* angeben.</span><span class="sxs-lookup"><span data-stu-id="b9a59-116">Cloud Solution Providers can create a support ticket for their customer's subscriptions by logging into their customer's tenant and specifying their home tenant id using *CSPHomeTenantId* parameter.</span></span>

<span data-ttu-id="b9a59-117">__Für technische Tickets:__</span><span class="sxs-lookup"><span data-stu-id="b9a59-117">__For technical tickets:__</span></span>

<span data-ttu-id="b9a59-118">Um den Ressourcennamen anzugeben, geben ARM Ressourcen-ID der Ressource mit dem Parameter *"TechnicalTicketResourceId"* an.</span><span class="sxs-lookup"><span data-stu-id="b9a59-118">To specify the resource name, specify the ARM resource ID of the resource by using *TechnicalTicketResourceId* parameter.</span></span> <span data-ttu-id="b9a59-119">Sehen Sie sich ein Beispiel unten an.</span><span class="sxs-lookup"><span data-stu-id="b9a59-119">See an example below.</span></span> 

<span data-ttu-id="b9a59-120">__Für Kontingenttickets:__</span><span class="sxs-lookup"><span data-stu-id="b9a59-120">__For quota tickets:__</span></span>

<span data-ttu-id="b9a59-121">Geben Sie zum Anfordern einer Kontingenterhöhung für **Compute VM Cores,** **Batch,** **SQL Database** und SQL **Data Warehouse** zusätzliche Details unter dem *"QuotaTicketDetail"-Objekt* an.</span><span class="sxs-lookup"><span data-stu-id="b9a59-121">To request for quota increase for **Compute VM Cores**, **Batch**, **SQL Database** and **SQL Data Warehouse**, provide additional details under *QuotaTicketDetail* object.</span></span> <span data-ttu-id="b9a59-122">Das Objekt "QuotaTicketDetail" besteht aus drei Eigenschaften, wie unten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b9a59-122">QuotaTicketDetail object consists of 3 properties as described below.</span></span> <span data-ttu-id="b9a59-123">Klicken Sie hier, um ausführliche [Informationen zu erhalten.](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="b9a59-123">For detailed documentation, please [click here.](https://aka.ms/supportrpquotarequestpayload)</span></span>

    • QuotaChangeRequestSubType

        This is required for certain quota types when there is a sub type that you are requesting quota increase for. Example: Batch, SQL Database and SQL Data Warehouse have a sub type.

    • QuotaChangeRequestVersion

        This is required and indicates the version of the quota change request payload.

    • QuotaChangeRequests

        This is required and is a list of PSQuotaChangeRequest objects. PSQuotaChangeRequest object has 2 required properties.

        ○ Region

            This is the Azure location or region for which you are requesting quota increase. This is the Location property of Get-AzLocation cmdlet.
        
        ○ Payload

            This is where you specify the new limits for the selected quota type.


<span data-ttu-id="b9a59-124">Eine ausführliche Dokumentation zum Erstellen der Nutzlast für verschiedene Kontingenttypen finden Sie [hier.](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="b9a59-124">For detailed documentation on how to construct Payload for various quota types, please [click here](https://aka.ms/supportrpquotarequestpayload)</span></span>

## <span data-ttu-id="b9a59-125">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b9a59-125">EXAMPLES</span></span>

### <span data-ttu-id="b9a59-126">Beispiel 1: Erstellen eines Supporttickets für die Abrechnungs- oder Abonnementverwaltung</span><span class="sxs-lookup"><span data-stu-id="b9a59-126">Example 1: Create a Billing or Subscription Management support ticket.</span></span> <span data-ttu-id="b9a59-127">Verwenden Get-AzSupportService und Get-AzSupportProblemClassification, um die richtigen GUIDs für die Problemklassifizierung der Abrechnung oder Abonnementverwaltung abzurufen, für die Sie Support anfordern möchten</span><span class="sxs-lookup"><span data-stu-id="b9a59-127">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Billing or Subscription Management problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b9a59-128">Beispiel 2: Erstellen eines Eintrittstickets für den technischen Support für eine Ressource des virtuellen Computers für Windows.</span><span class="sxs-lookup"><span data-stu-id="b9a59-128">Example 2: Create a technical support ticket for Virtual Machine for Windows resource.</span></span> <span data-ttu-id="b9a59-129">Verwenden Get-AzSupportService und Get-AzSupportProblemClassification zum Abrufen der korrekten GUIDs für die Problemklassifizierung von Virtual Machine für Windows, für die Sie Unterstützung anfordern möchten</span><span class="sxs-lookup"><span data-stu-id="b9a59-129">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Virtual Machine for Windows problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{vm_windows_service_guid}/problemClassifications/{problemClassification_guid}" -TechnicalTicketResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName              Status CreatedDate
----  ----- --------------- -------- ------------------              ------ -----------
test1 Test  150010521000317 Minimal  Virtual Machine running Windows Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b9a59-130">Beispiel 3: Erstellen eines Kontingentunterstützungstickets zum Erhöhen des Kontingents für Virtual Machine Cores für eine bestimmte VM-Familie.</span><span class="sxs-lookup"><span data-stu-id="b9a59-130">Example 3: Create a quota support ticket to increase quota for Virtual Machine Cores for a specific VM family.</span></span> <span data-ttu-id="b9a59-131">Verwenden Get-AzSupportService und Get-AzSupportProblemClassification, um die richtigen GUIDs für die Problemklassifizierung von Quota Compute VM Cores abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b9a59-131">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Compute VM Cores problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{cores_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":350}"}, @{Region = "eastus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":516}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b9a59-132">Beispiel 4: Erstellen eines Kontingentunterstützungstickets zum Erhöhen des Kontingents für Kerne mit niedriger Priorität für ein Batchkonto.</span><span class="sxs-lookup"><span data-stu-id="b9a59-132">Example 4: Create a quota support ticket to increase quota for Low-priority cores for a Batch account.</span></span> <span data-ttu-id="b9a59-133">Verwenden Get-AzSupportService und Get-AzSupportProblemClassification, um die richtigen GUIDs für die Problemklassifizierung des Kontingentbatches abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b9a59-133">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":200,`"Type`":`"LowPriority`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b9a59-134">Beispiel 5: Erstellen eines Kontingentunterstützungstickets zum Erhöhen des Kontingents für VM-Kerne für eine bestimmte VM-Familie für ein Batchkonto.</span><span class="sxs-lookup"><span data-stu-id="b9a59-134">Example 5: Create a quota support ticket to increase VM cores quota for a specific VM Family for a Batch account.</span></span> <span data-ttu-id="b9a59-135">Verwenden Get-AzSupportService und Get-AzSupportProblemClassification, um die richtigen GUIDs für die Problemklassifizierung des Kontingentbatches abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b9a59-135">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"VMFamily`":`"standardA0_A7Family`",`"NewLimit`":200,`"Type`":`"Dedicated`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b9a59-136">Beispiel 6: Erstellen eines Kontingentunterstützungstickets zum Erhöhen des Kontingents für ein Batchkonto.</span><span class="sxs-lookup"><span data-stu-id="b9a59-136">Example 6: Create a quota support ticket to increase Pools quota for a Batch account.</span></span> <span data-ttu-id="b9a59-137">Verwenden Get-AzSupportService und Get-AzSupportProblemClassification, um die richtigen GUIDs für die Problemklassifizierung des Kontingentbatches abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b9a59-137">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Pools`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b9a59-138">Beispiel 7: Erstellen eines Kontingentunterstützungstickets zum Erhöhen des Kontingents aktiver Aufträge und Stellenpläne für ein Batchkonto.</span><span class="sxs-lookup"><span data-stu-id="b9a59-138">Example 7: Create a quota support ticket to increase active Jobs and job schedules quota for a Batch account.</span></span> <span data-ttu-id="b9a59-139">Verwenden Get-AzSupportService und Get-AzSupportProblemClassification, um die richtigen GUIDs für die Problemklassifizierung des Kontingentbatches abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b9a59-139">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Jobs`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b9a59-140">Beispiel 8: Erstellen eines Kontingent-Supporttickets, um die Anzahl der Batchkonten für ein Abonnement zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="b9a59-140">Example 8: Create a quota support ticket to increase number of Batch accounts for a subscription.</span></span> <span data-ttu-id="b9a59-141">Verwenden Get-AzSupportService und Get-AzSupportProblemClassification, um die richtigen GUIDs für die Problemklassifizierung des Kontingentbatches abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b9a59-141">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Subscription" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":120,`"Type`":`"Account`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b9a59-142">Beispiel 9: Erstellen eines Kontingentunterstützungstickets zum Erhöhen des Kontingents für DTUs für SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="b9a59-142">Example 9: Create a quota support ticket to increase quota for DTUs for SQL Database.</span></span> <span data-ttu-id="b9a59-143">Verwenden Get-AzSupportService und Get-AzSupportProblemClassification, um die richtigen GUIDs für die Klassifizierung von Kontingenten und SQL Datenbankproblem abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b9a59-143">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b9a59-144">Beispiel 10: Erstellen eines Kontingentunterstützungstickets zum Erhöhen des Kontingents für Server SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="b9a59-144">Example 10: Create a quota support ticket to increase quota for Servers for SQL Database.</span></span> <span data-ttu-id="b9a59-145">Verwenden Get-AzSupportService und Get-AzSupportProblemClassification, um die richtigen GUIDs für die Klassifizierung von Kontingenten und SQL Datenbankproblem abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b9a59-145">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b9a59-146">Beispiel 11: Erstellen eines Kontingentunterstützungstickets zum Erhöhen des Kontingents für DTUs für SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="b9a59-146">Example 11: Create a quota support ticket to increase quota for DTUs for SQL Data Warehouse.</span></span> <span data-ttu-id="b9a59-147">Verwenden Get-AzSupportService und Get-AzSupportProblemClassification, um die richtigen GUIDs für "Quota" SQL Date Warehouse-Problemklassifizierung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b9a59-147">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Date Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b9a59-148">Beispiel 12: Erstellen eines Kontingentsupporttickets zum Erhöhen des Kontingents für Server für SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="b9a59-148">Example 12: Create a quota support ticket to increase quota for Servers for SQL Data Warehouse.</span></span> <span data-ttu-id="b9a59-149">Verwenden Get-AzSupportService und Get-AzSupportProblemClassification, um die richtigen GUIDs für das Kontingent SQL Data Warehouse-Problemklassifizierung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b9a59-149">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Data Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b9a59-150">Beispiel 13: Erstellen eines Kontingentunterstützungstickets zum Erhöhen des Kontingents für Kerne mit niedriger Priorität für den Machine Learning-Dienst.</span><span class="sxs-lookup"><span data-stu-id="b9a59-150">Example 13: Create a quota support ticket to increase quota for Low-priority cores for Machine Learning service.</span></span> <span data-ttu-id="b9a59-151">Verwenden Get-AzSupportService und Get-AzSupportProblemClassification, um die richtigen GUIDs für die Problemklassifizierung des Diensts Quota Machine Learning abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b9a59-151">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"LowPriority`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b9a59-152">Beispiel 14: Erstellen eines Kontingentunterstützungstickets zum Erhöhen des Kontingents für VM-Kerne für eine bestimmte VM Family für Machine Learning-Dienst.</span><span class="sxs-lookup"><span data-stu-id="b9a59-152">Example 14: Create a quota support ticket to increase VM cores quota for a specific VM Family for Machine Learning service.</span></span> <span data-ttu-id="b9a59-153">Verwenden Get-AzSupportService und Get-AzSupportProblemClassification, um die richtigen GUIDs für die Problemklassifizierung des Diensts Quota Machine Learning abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b9a59-153">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"standardDFamily`",`"NewLimit`":200,`"Type`":`"Dedicated`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b9a59-154">Beispiel 15: Erstellen eines Kontingentsupporttickets zum Erhöhen des Kontingents für Azure SQL Verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="b9a59-154">Example 15: Create a quota support ticket to increase quota for Azure SQL Managed Instance.</span></span> <span data-ttu-id="b9a59-155">Verwenden Get-AzSupportService und Get-AzSupportProblemClassification zum Abrufen der richtigen GUIDs für das Kontingent SQL Dienstproblemklassifizierung verwalteter Instanzen.</span><span class="sxs-lookup"><span data-stu-id="b9a59-155">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Managed Instance service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_managed_instance_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "SQLMI" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"vCore`" }"}, @{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"Subnet`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b9a59-156">Beispiel 16: Erstellen eines Supporttickets durch Angeben einzelner Kundenkontaktparameter anstelle des CustomerContactDetail-Objekts.</span><span class="sxs-lookup"><span data-stu-id="b9a59-156">Example 16: Create a support ticket by specifying individual customer contact parameters instead of CustomerContactDetail object.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com"

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b9a59-157">Beispiel 17: Erstellen eines Supporttickets mit der Anforderung einer 24 x 7-Antwort von Azure.</span><span class="sxs-lookup"><span data-stu-id="b9a59-157">Example 17: Create a support ticket with request for 24 x 7 response from Azure.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "critical" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -Require24X7Response 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Critical  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="b9a59-158">Beispiel 18: Erstellen eines Supporttickets für Ihren Kunden, wenn Sie Cloudlösungsanbieter (Cloud Solution Provider, CSP) sind.</span><span class="sxs-lookup"><span data-stu-id="b9a59-158">Example 18: Create a support ticket on behalf of your customer if you are a Cloud Solution Provider (CSP).</span></span> <span data-ttu-id="b9a59-159">CSP sollte sich zuerst bei ihrem Mandanten und dann wie im folgenden Beispiel gezeigt beim Mandanten des Kunden anmelden.</span><span class="sxs-lookup"><span data-stu-id="b9a59-159">CSP should first login into their tenant, and then login into customer's tenant as shown in the example below.</span></span> <span data-ttu-id="b9a59-160">Sie müssen dann den Parameter "-CSPHomeTenantId" verwenden, um ihre Home Tenant-ID zum Zeitpunkt der Erstellung eines Supporttickets anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b9a59-160">They must then use -CSPHomeTenantId parameter to specify their home tenant id at the time of creating a support ticket.</span></span>  
```powershell

PS C:\> Login-AzAccount

PS C:\> Login-AzAccount -TenantId {customer_tenant_id}

PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -CSPHomeTenantId {csp_home_tenant_id} 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="b9a59-161">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9a59-161">PARAMETERS</span></span>

### <span data-ttu-id="b9a59-162">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="b9a59-162">-AdditionalEmailAddress</span></span>
<span data-ttu-id="b9a59-163">Weitere E-Mail-Adressen.</span><span class="sxs-lookup"><span data-stu-id="b9a59-163">Additional email addresses.</span></span>
<span data-ttu-id="b9a59-164">Die hier aufgelisteten E-Mail-Adressen werden nach Übereinstimmung mit dem Supportticket kopiert.</span><span class="sxs-lookup"><span data-stu-id="b9a59-164">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a59-165">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9a59-165">-AsJob</span></span>
<span data-ttu-id="b9a59-166">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="b9a59-166">Run cmdlet in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a59-167">-CSPHomeTenantId</span><span class="sxs-lookup"><span data-stu-id="b9a59-167">-CSPHomeTenantId</span></span>
<span data-ttu-id="b9a59-168">Dies ist die Home-Mandanten-ID des Benutzers des Cloud-Lösungsanbieters, der versucht, ein Supportticket für seinen Kunden zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b9a59-168">This is the home tenant id of the Cloud Solution Provider user trying to create a support ticket for their customer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a59-169">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="b9a59-169">-CustomerContactDetail</span></span>
<span data-ttu-id="b9a59-170">Kundenkontaktdetails, die der Ressource "SupportTicket" zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b9a59-170">Customer contact details associated with SupportTicket resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSContactProfile
Parameter Sets: CreateSupportTicketWithContactObjectParameterSet, CreateTechnicalSupportTicketWithContactObjectParameterSet, CreateQuotaSupportTicketWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a59-171">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="b9a59-171">-CustomerCountry</span></span>
<span data-ttu-id="b9a59-172">Land des Kunden.</span><span class="sxs-lookup"><span data-stu-id="b9a59-172">Customer country.</span></span>
<span data-ttu-id="b9a59-173">Dies muss ein gültiger ISO Alpha-3-Ländercode (ISO 3166) sein.</span><span class="sxs-lookup"><span data-stu-id="b9a59-173">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a59-174">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="b9a59-174">-CustomerFirstName</span></span>
<span data-ttu-id="b9a59-175">Vorname des Kunden.</span><span class="sxs-lookup"><span data-stu-id="b9a59-175">Customer first name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a59-176">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="b9a59-176">-CustomerLastName</span></span>
<span data-ttu-id="b9a59-177">Nachname des Kunden.</span><span class="sxs-lookup"><span data-stu-id="b9a59-177">Customer last name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a59-178">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="b9a59-178">-CustomerPhoneNumber</span></span>
<span data-ttu-id="b9a59-179">Telefonnummer des Kunden.</span><span class="sxs-lookup"><span data-stu-id="b9a59-179">Customer phone number.</span></span>
<span data-ttu-id="b9a59-180">Dies ist erforderlich, wenn die bevorzugte Kontaktmethode "Telefon" ist.</span><span class="sxs-lookup"><span data-stu-id="b9a59-180">This is required if preferred contact method is phone.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a59-181">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="b9a59-181">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="b9a59-182">Verzögerte Sprache des Benutzerdefinierten.</span><span class="sxs-lookup"><span data-stu-id="b9a59-182">Peferred language of the custom.</span></span>
<span data-ttu-id="b9a59-183">Dies muss ein gültiger Code für andere Sprachen für eine der hier aufgeführten unterstützten Sprachen https://azure.microsoft.com/en-us/support/faq/ sein.</span><span class="sxs-lookup"><span data-stu-id="b9a59-183">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/en-us/support/faq/.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a59-184">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="b9a59-184">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="b9a59-185">Vom Kunden bevorzugte Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="b9a59-185">Customer preferred time zone.</span></span>
<span data-ttu-id="b9a59-186">Dies muss ein gültiger System.TimeZoneInfo.Id sein.</span><span class="sxs-lookup"><span data-stu-id="b9a59-186">This must be a valid System.TimeZoneInfo.Id value.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a59-187">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="b9a59-187">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="b9a59-188">Primäre E-Mail-Adresse des Kunden.</span><span class="sxs-lookup"><span data-stu-id="b9a59-188">Customer primary email address.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a59-189">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9a59-189">-DefaultProfile</span></span>
<span data-ttu-id="b9a59-190">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b9a59-190">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a59-191">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b9a59-191">-Description</span></span>
<span data-ttu-id="b9a59-192">Detaillierte Beschreibung der Frage oder des Problems.</span><span class="sxs-lookup"><span data-stu-id="b9a59-192">Detailed description of the question or issue.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a59-193">-Name</span><span class="sxs-lookup"><span data-stu-id="b9a59-193">-Name</span></span>
<span data-ttu-id="b9a59-194">Name des Supporttickets, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b9a59-194">Name of support ticket that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a59-195">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="b9a59-195">-PreferredContactMethod</span></span>
<span data-ttu-id="b9a59-196">Bevorzugte Kontaktmethode.</span><span class="sxs-lookup"><span data-stu-id="b9a59-196">Preferred contact method.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.ContactMethod
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:
Accepted values: Email, Phone

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a59-197">-ProblemClassificationId</span><span class="sxs-lookup"><span data-stu-id="b9a59-197">-ProblemClassificationId</span></span>
<span data-ttu-id="b9a59-198">Jeder Azure -Dienst verfügt über eine eigene Problemkategorie, die so genannte Problemklassifizierung, die dem Problemtyp entspricht, den Sie gerade haben.</span><span class="sxs-lookup"><span data-stu-id="b9a59-198">Each Azure service has its own set of issue category called problem classification that corresponds to the type of problem you're experiencing.</span></span>
<span data-ttu-id="b9a59-199">Dieser Parameter ist die ARM der ProblemClassification-Ressource.</span><span class="sxs-lookup"><span data-stu-id="b9a59-199">This parameter is the ARM resource id of ProblemClassification resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a59-200">-ProblemStartTime</span><span class="sxs-lookup"><span data-stu-id="b9a59-200">-ProblemStartTime</span></span>
<span data-ttu-id="b9a59-201">Datum und Uhrzeit, zu dem das Problem begonnen hat.</span><span class="sxs-lookup"><span data-stu-id="b9a59-201">Date and time when the problem started.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a59-202">-QuotaTicketDetail</span><span class="sxs-lookup"><span data-stu-id="b9a59-202">-QuotaTicketDetail</span></span>
<span data-ttu-id="b9a59-203">Weitere Details für ein Kontingent-Supportticket.</span><span class="sxs-lookup"><span data-stu-id="b9a59-203">Additional details for a Quota support ticket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSQuotaTicketDetail
Parameter Sets: CreateQuotaSupportTicketWithContactObjectParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a59-204">-Require24X7Response</span><span class="sxs-lookup"><span data-stu-id="b9a59-204">-Require24X7Response</span></span>
<span data-ttu-id="b9a59-205">Gibt an, ob für dieses Supportticket eine Rund-um-die-Uhr-Antwort von Azure erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b9a59-205">Indicates if this support ticket requires a 24x7 response from Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a59-206">-Schweregrad</span><span class="sxs-lookup"><span data-stu-id="b9a59-206">-Severity</span></span>
<span data-ttu-id="b9a59-207">Schweregrad des Supporttickets.</span><span class="sxs-lookup"><span data-stu-id="b9a59-207">Severity of the support ticket.</span></span>
<span data-ttu-id="b9a59-208">Dies gibt die Dringlichkeit des Falls an, die wiederum die Reaktionszeit gemäß dem Servicelevelvertrag des technischen Supportplans, den Sie mit Azure haben, bestimmt.</span><span class="sxs-lookup"><span data-stu-id="b9a59-208">This indicates the urgency of the case, which in turn determines the response time according to the service level agreement of the technical support plan you have with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.Severity
Parameter Sets: (All)
Aliases:
Accepted values: Minimal, Moderate, Critical, HighestCriticalImpact

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a59-209">-TechnicalTicketResourceId</span><span class="sxs-lookup"><span data-stu-id="b9a59-209">-TechnicalTicketResourceId</span></span>
<span data-ttu-id="b9a59-210">Dies ist die Ressourcen-ID der Azure-Dienstressource (z. B. eine Ressource des virtuellen Computers oder eine HDInsight-Ressource), für die das Supportticket erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b9a59-210">This is the resource id of the Azure service resource (For example: A virtual machine resource or an HDInsight resource) for which the support ticket is created.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTechnicalSupportTicketWithContactObjectParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a59-211">-Title</span><span class="sxs-lookup"><span data-stu-id="b9a59-211">-Title</span></span>
<span data-ttu-id="b9a59-212">Titel des Supporttickets.</span><span class="sxs-lookup"><span data-stu-id="b9a59-212">Title of support ticket.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a59-213">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9a59-213">-Confirm</span></span>
<span data-ttu-id="b9a59-214">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b9a59-214">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a59-215">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b9a59-215">-WhatIf</span></span>
<span data-ttu-id="b9a59-216">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b9a59-216">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9a59-217">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b9a59-217">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a59-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9a59-218">CommonParameters</span></span>
<span data-ttu-id="b9a59-219">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9a59-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9a59-220">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9a59-220">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9a59-221">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b9a59-221">INPUTS</span></span>

### <span data-ttu-id="b9a59-222">Keine</span><span class="sxs-lookup"><span data-stu-id="b9a59-222">None</span></span>

## <span data-ttu-id="b9a59-223">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b9a59-223">OUTPUTS</span></span>

### <span data-ttu-id="b9a59-224">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="b9a59-224">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="b9a59-225">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b9a59-225">NOTES</span></span>

## <span data-ttu-id="b9a59-226">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b9a59-226">RELATED LINKS</span></span>
