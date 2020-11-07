---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
ms.openlocfilehash: dc3beb041a143ed151c19e0623f5db7f5f6d61e3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847479"
---
# <span data-ttu-id="8fc90-101">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="8fc90-101">New-AzSupportTicket</span></span>

## <span data-ttu-id="8fc90-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8fc90-102">SYNOPSIS</span></span>
<span data-ttu-id="8fc90-103">Erstellt ein Support Ticket.</span><span class="sxs-lookup"><span data-stu-id="8fc90-103">Creates a support ticket.</span></span>

## <span data-ttu-id="8fc90-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8fc90-104">SYNTAX</span></span>

### <span data-ttu-id="8fc90-105">CreateSupportTicketWithContactDetailParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8fc90-105">CreateSupportTicketWithContactDetailParameterSet (Default)</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fc90-106">CreateSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fc90-106">CreateSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fc90-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fc90-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fc90-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fc90-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fc90-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fc90-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fc90-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fc90-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fc90-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8fc90-111">DESCRIPTION</span></span>
<span data-ttu-id="8fc90-112">Dieses Cmdlet kann verwendet werden, um ein Support Ticket für Abrechnungs-, Abonnement Verwaltungs-, Kontingents-oder technische Probleme zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8fc90-112">This cmdlet can be used to create a support ticket for Billing, Subscription Management, Quota or Technical issues.</span></span> <span data-ttu-id="8fc90-113">Verwenden Sie Get-AzSupportService-und Get-AzSupportProblemClassification-Cmdlets, um den Azure-Dienst und die entsprechenden Problem Klassifikationen zu identifizieren, für die Sie Support anfordern möchten.</span><span class="sxs-lookup"><span data-stu-id="8fc90-113">Use Get-AzSupportService and Get-AzSupportProblemClassification cmdlets to identify the Azure service and it's corresponding problem classifications respectively for which you want to request support.</span></span> <span data-ttu-id="8fc90-114">Sie müssen die folgenden Parameter angeben:</span><span class="sxs-lookup"><span data-stu-id="8fc90-114">You must specify the following parameters:</span></span> 

    • Title
    • Description
    • Severity level
    • ProblemClassificationId
    • CustomerContactDetail (or individual customer contact parameters)

<span data-ttu-id="8fc90-115">Sie können New-AzSupportContactProfileObject Hilfsprogramm-Cmdlet verwenden, um CustomerContactDetail-Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8fc90-115">You can use New-AzSupportContactProfileObject helper cmdlet to create CustomerContactDetail object.</span></span>

<span data-ttu-id="8fc90-116">Anbieter von Cloud-Lösungen können ein Support-Ticket für die Abonnements Ihres Kunden erstellen, indem Sie sich beim Mandanten des Kunden anmelden und seine Home-Mandanten-ID mithilfe des *CSPHomeTenantId* -Parameters angeben.</span><span class="sxs-lookup"><span data-stu-id="8fc90-116">Cloud Solution Providers can create a support ticket for their customer's subscriptions by logging into their customer's tenant and specifying their home tenant id using *CSPHomeTenantId* parameter.</span></span>

<span data-ttu-id="8fc90-117">__Für technische Tickets:__</span><span class="sxs-lookup"><span data-stu-id="8fc90-117">__For technical tickets:__</span></span>

<span data-ttu-id="8fc90-118">Um den Ressourcennamen anzugeben, geben Sie die Arm-Ressourcen-ID der Ressource mithilfe des *TechnicalTicketResourceId* -Parameters an.</span><span class="sxs-lookup"><span data-stu-id="8fc90-118">To specify the resource name, specify the ARM resource ID of the resource by using *TechnicalTicketResourceId* parameter.</span></span> <span data-ttu-id="8fc90-119">Sehen Sie sich ein Beispiel unten an.</span><span class="sxs-lookup"><span data-stu-id="8fc90-119">See an example below.</span></span> 

<span data-ttu-id="8fc90-120">__Für Kontingent Tickets:__</span><span class="sxs-lookup"><span data-stu-id="8fc90-120">__For quota tickets:__</span></span>

<span data-ttu-id="8fc90-121">Wenn Sie eine Kontingenterhöhung für **Compute-VM-Cores** , **Batch** , **SQL-Datenbank** und **SQL Data Warehouse** anfordern möchten, geben Sie unter *QuotaTicketDetail* -Objekt zusätzliche Details an.</span><span class="sxs-lookup"><span data-stu-id="8fc90-121">To request for quota increase for **Compute VM Cores** , **Batch** , **SQL Database** and **SQL Data Warehouse** , provide additional details under *QuotaTicketDetail* object.</span></span> <span data-ttu-id="8fc90-122">Das QuotaTicketDetail-Objekt besteht aus drei Eigenschaften, wie nachstehend beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8fc90-122">QuotaTicketDetail object consists of 3 properties as described below.</span></span> <span data-ttu-id="8fc90-123">Eine detaillierte Dokumentation finden [Sie hier.](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="8fc90-123">For detailed documentation, please [click here.](https://aka.ms/supportrpquotarequestpayload)</span></span>

    • QuotaChangeRequestSubType

        This is required for certain quota types when there is a sub type that you are requesting quota increase for. Example: Batch, SQL Database and SQL Data Warehouse have a sub type.

    • QuotaChangeRequestVersion

        This is required and indicates the version of the quota change request payload.

    • QuotaChangeRequests

        This is required and is a list of PSQuotaChangeRequest objects. PSQuotaChangeRequest object has 2 required properties.

        ○ Region

            This is the Azure location or region for which you are requesting quota increase. This is the Location property of Get-AzLocation cmdlet.
        
        ○ Payload

            This is where you specify the new limits for the selected quota type.


<span data-ttu-id="8fc90-124">Eine detaillierte Dokumentation zum Erstellen von Nutzlast für verschiedene Kontingenttypen finden [Sie hier](https://aka.ms/supportrpquotarequestpayload) .</span><span class="sxs-lookup"><span data-stu-id="8fc90-124">For detailed documentation on how to construct Payload for various quota types, please [click here](https://aka.ms/supportrpquotarequestpayload)</span></span>

## <span data-ttu-id="8fc90-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8fc90-125">EXAMPLES</span></span>

### <span data-ttu-id="8fc90-126">Beispiel 1: Erstellen eines Support Tickets für Abrechnungs-oder Abonnementverwaltung</span><span class="sxs-lookup"><span data-stu-id="8fc90-126">Example 1: Create a Billing or Subscription Management support ticket.</span></span> <span data-ttu-id="8fc90-127">Verwenden Sie Get-AzSupportService und Get-AzSupportProblemClassification, um korrekte GUIDs für die Abrechnungs-oder Abonnement Verwaltungsproblem Klassifizierung abzurufen, für die Sie Support anfordern möchten.</span><span class="sxs-lookup"><span data-stu-id="8fc90-127">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Billing or Subscription Management problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="8fc90-128">Beispiel 2: Erstellen eines Tickets für den technischen Support für Virtual Machine für Windows-Ressource.</span><span class="sxs-lookup"><span data-stu-id="8fc90-128">Example 2: Create a technical support ticket for Virtual Machine for Windows resource.</span></span> <span data-ttu-id="8fc90-129">Verwenden Sie Get-AzSupportService und Get-AzSupportProblemClassification, um korrekte GUIDs für die Problem Klassifikation von Virtual Machine für Windows abzurufen, für die Sie Support anfordern möchten.</span><span class="sxs-lookup"><span data-stu-id="8fc90-129">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Virtual Machine for Windows problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{vm_windows_service_guid}/problemClassifications/{problemClassification_guid}" -TechnicalTicketResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName              Status CreatedDate
----  ----- --------------- -------- ------------------              ------ -----------
test1 Test  150010521000317 Minimal  Virtual Machine running Windows Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="8fc90-130">Beispiel 3: Erstellen eines Kontingent Unterstützungs Tickets zur Erhöhung des Kontingents für virtuelle Maschinen Kerne für eine bestimmte VM-Familie.</span><span class="sxs-lookup"><span data-stu-id="8fc90-130">Example 3: Create a quota support ticket to increase quota for Virtual Machine Cores for a specific VM family.</span></span> <span data-ttu-id="8fc90-131">Verwenden Sie Get-AzSupportService und Get-AzSupportProblemClassification, um korrekte GUIDs für die Problemklassifizierung der Kontingent Berechnung für VM-Kerne abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8fc90-131">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Compute VM Cores problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{cores_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":350}"}, @{Region = "eastus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":516}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="8fc90-132">Beispiel 4: Erstellen eines Kontingent Unterstützungs Tickets, um das Kontingent für Kerne mit niedriger Priorität für ein Stapelverarbeitungs Konto zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="8fc90-132">Example 4: Create a quota support ticket to increase quota for Low-priority cores for a Batch account.</span></span> <span data-ttu-id="8fc90-133">Verwenden Sie Get-AzSupportService und Get-AzSupportProblemClassification, um korrekte GUIDs für die Kontingent Batch Problemklassifizierung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8fc90-133">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":200,`"Type`":`"LowPriority`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="8fc90-134">Beispiel 5: Erstellen eines Kontingent Unterstützungs Tickets zum Erhöhen des VM-Kern Kontingents für eine bestimmte VM-Familie für ein Stapelverarbeitungs Konto.</span><span class="sxs-lookup"><span data-stu-id="8fc90-134">Example 5: Create a quota support ticket to increase VM cores quota for a specific VM Family for a Batch account.</span></span> <span data-ttu-id="8fc90-135">Verwenden Sie Get-AzSupportService und Get-AzSupportProblemClassification, um korrekte GUIDs für die Kontingent Batch Problemklassifizierung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8fc90-135">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"VMFamily`":`"standardA0_A7Family`",`"NewLimit`":200,`"Type`":`"Dedicated`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="8fc90-136">Beispiel 6: Erstellen eines Kontingent Support Tickets zum Erhöhen der Kontingente für ein Batch Konto</span><span class="sxs-lookup"><span data-stu-id="8fc90-136">Example 6: Create a quota support ticket to increase Pools quota for a Batch account.</span></span> <span data-ttu-id="8fc90-137">Verwenden Sie Get-AzSupportService und Get-AzSupportProblemClassification, um korrekte GUIDs für die Kontingent Batch Problemklassifizierung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8fc90-137">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Pools`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="8fc90-138">Beispiel 7: Erstellen eines Kontingent Unterstützungs Tickets zum Erhöhen der aktiven Aufträge und des Kontingents für Auftragszeitpläne für ein Stapelverarbeitungs Konto.</span><span class="sxs-lookup"><span data-stu-id="8fc90-138">Example 7: Create a quota support ticket to increase active Jobs and job schedules quota for a Batch account.</span></span> <span data-ttu-id="8fc90-139">Verwenden Sie Get-AzSupportService und Get-AzSupportProblemClassification, um korrekte GUIDs für die Kontingent Batch Problemklassifizierung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8fc90-139">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Jobs`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="8fc90-140">Beispiel 8: Erstellen eines Kontingent Unterstützungs Tickets, um die Anzahl der Stapelverarbeitungs Konten für ein Abonnement zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="8fc90-140">Example 8: Create a quota support ticket to increase number of Batch accounts for a subscription.</span></span> <span data-ttu-id="8fc90-141">Verwenden Sie Get-AzSupportService und Get-AzSupportProblemClassification, um korrekte GUIDs für die Kontingent Batch Problemklassifizierung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8fc90-141">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Subscription" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":120,`"Type`":`"Account`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="8fc90-142">Beispiel 9: Erstellen eines Kontingent Unterstützungs Tickets zum Erhöhen des Kontingents für DTUs für SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="8fc90-142">Example 9: Create a quota support ticket to increase quota for DTUs for SQL Database.</span></span> <span data-ttu-id="8fc90-143">Verwenden Sie Get-AzSupportService und Get-AzSupportProblemClassification, um korrekte GUIDs für die Problemklassifizierung der Kontingent SQL-Datenbank abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8fc90-143">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="8fc90-144">Beispiel 10: Erstellen eines Kontingent Unterstützungs Tickets, um das Kontingent für Server für SQL-Datenbank zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="8fc90-144">Example 10: Create a quota support ticket to increase quota for Servers for SQL Database.</span></span> <span data-ttu-id="8fc90-145">Verwenden Sie Get-AzSupportService und Get-AzSupportProblemClassification, um korrekte GUIDs für die Problemklassifizierung der Kontingent SQL-Datenbank abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8fc90-145">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="8fc90-146">Beispiel 11: Erstellen eines Kontingent Support Tickets zum Erhöhen des Kontingents für DTUs für SQL Data Warehouse</span><span class="sxs-lookup"><span data-stu-id="8fc90-146">Example 11: Create a quota support ticket to increase quota for DTUs for SQL Data Warehouse.</span></span> <span data-ttu-id="8fc90-147">Verwenden Sie Get-AzSupportService und Get-AzSupportProblemClassification, um korrekte GUIDs für die Problemklassifizierung des Kontingents SQL-Datums Warehouse abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8fc90-147">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Date Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="8fc90-148">Beispiel 12: Erstellen eines Kontingent Unterstützungs Tickets, um das Kontingent für Server für SQL Data Warehouse zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="8fc90-148">Example 12: Create a quota support ticket to increase quota for Servers for SQL Data Warehouse.</span></span> <span data-ttu-id="8fc90-149">Verwenden Sie Get-AzSupportService und Get-AzSupportProblemClassification, um korrekte GUIDs für die Problemklassifizierung des Kontingents SQL-Data Warehouse abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8fc90-149">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Data Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="8fc90-150">Beispiel 13: Erstellen eines Kontingent Unterstützungs Tickets zur Erhöhung des Kontingents für Kerne mit niedriger Priorität für den maschinellen Lerndienst</span><span class="sxs-lookup"><span data-stu-id="8fc90-150">Example 13: Create a quota support ticket to increase quota for Low-priority cores for Machine Learning service.</span></span> <span data-ttu-id="8fc90-151">Verwenden Sie Get-AzSupportService und Get-AzSupportProblemClassification, um korrekte GUIDs für die Problem Klassifikation des Kontingent Computer lerndienstes abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8fc90-151">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"LowPriority`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="8fc90-152">Beispiel 14: Erstellen eines Kontingent Unterstützungs Tickets zum Erhöhen des VM-Kern Kontingents für eine bestimmte VM-Familie für den Computer Lerndienst</span><span class="sxs-lookup"><span data-stu-id="8fc90-152">Example 14: Create a quota support ticket to increase VM cores quota for a specific VM Family for Machine Learning service.</span></span> <span data-ttu-id="8fc90-153">Verwenden Sie Get-AzSupportService und Get-AzSupportProblemClassification, um korrekte GUIDs für die Problem Klassifikation des Kontingent Computer lerndienstes abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8fc90-153">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"standardDFamily`",`"NewLimit`":200,`"Type`":`"Dedicated`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="8fc90-154">Beispiel 15: Erstellen Sie ein Support Ticket, indem Sie einzelne Kundenkontakt Parameter anstelle des CustomerContactDetail-Objekts angeben.</span><span class="sxs-lookup"><span data-stu-id="8fc90-154">Example 15: Create a support ticket by specifying individual customer contact parameters instead of CustomerContactDetail object.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com"

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="8fc90-155">Beispiel 16: Erstellen eines Support Tickets mit der Anforderung einer Antwort von Azure auf 24 x 7.</span><span class="sxs-lookup"><span data-stu-id="8fc90-155">Example 16: Create a support ticket with request for 24 x 7 response from Azure.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "critical" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -Require24X7Response 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Critical  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="8fc90-156">Beispiel 17: Erstellen Sie im Auftrag Ihres Kunden ein Support Ticket, wenn Sie ein Anbieter von Cloud-Lösungen (CSP) sind.</span><span class="sxs-lookup"><span data-stu-id="8fc90-156">Example 17: Create a support ticket on behalf of your customer if you are a Cloud Solution Provider (CSP).</span></span> <span data-ttu-id="8fc90-157">CSP sollte sich zunächst bei seinem Mandanten anmelden und sich dann in den Mandanten des Kunden einloggen, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="8fc90-157">CSP should first login into their tenant, and then login into customer's tenant as shown in the example below.</span></span> <span data-ttu-id="8fc90-158">Sie müssen dann-CSPHomeTenantId-Parameter verwenden, um Ihre Home-Mandanten-ID zum Zeitpunkt der Erstellung eines Support-Tickets anzugeben.</span><span class="sxs-lookup"><span data-stu-id="8fc90-158">They must then use -CSPHomeTenantId parameter to specify their home tenant id at the time of creating a support ticket.</span></span>  
```powershell

PS C:\> Login-AzAccount

PS C:\> Login-AzAccount -TenantId {customer_tenant_id}

PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -CSPHomeTenantId {csp_home_tenant_id} 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="8fc90-159">Parameter</span><span class="sxs-lookup"><span data-stu-id="8fc90-159">PARAMETERS</span></span>

### <span data-ttu-id="8fc90-160">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="8fc90-160">-AdditionalEmailAddress</span></span>
<span data-ttu-id="8fc90-161">Weitere e-Mail-Adressen.</span><span class="sxs-lookup"><span data-stu-id="8fc90-161">Additional email addresses.</span></span>
<span data-ttu-id="8fc90-162">Die hier aufgelisteten e-Mail-Adressen werden auf jede Korrespondenz über das Support-Ticket kopiert.</span><span class="sxs-lookup"><span data-stu-id="8fc90-162">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

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

### <span data-ttu-id="8fc90-163">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8fc90-163">-AsJob</span></span>
<span data-ttu-id="8fc90-164">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="8fc90-164">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="8fc90-165">-CSPHomeTenantId</span><span class="sxs-lookup"><span data-stu-id="8fc90-165">-CSPHomeTenantId</span></span>
<span data-ttu-id="8fc90-166">Hierbei handelt es sich um die Home-Mandanten-ID des Cloud Solution Provider-Benutzers, der versucht, ein Support Ticket für seinen Kunden zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8fc90-166">This is the home tenant id of the Cloud Solution Provider user trying to create a support ticket for their customer.</span></span>

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

### <span data-ttu-id="8fc90-167">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="8fc90-167">-CustomerContactDetail</span></span>
<span data-ttu-id="8fc90-168">Mit der Supportticket-Ressource verknüpfte Kundenkontakt Details.</span><span class="sxs-lookup"><span data-stu-id="8fc90-168">Customer contact details associated with SupportTicket resource.</span></span>

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

### <span data-ttu-id="8fc90-169">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="8fc90-169">-CustomerCountry</span></span>
<span data-ttu-id="8fc90-170">Kunden Land.</span><span class="sxs-lookup"><span data-stu-id="8fc90-170">Customer country.</span></span>
<span data-ttu-id="8fc90-171">Dies muss eine gültige ISO-Alpha-3-Landesvorwahl (ISO 3166) sein.</span><span class="sxs-lookup"><span data-stu-id="8fc90-171">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="8fc90-172">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="8fc90-172">-CustomerFirstName</span></span>
<span data-ttu-id="8fc90-173">Name des Kunden Vornamens</span><span class="sxs-lookup"><span data-stu-id="8fc90-173">Customer first name.</span></span>

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

### <span data-ttu-id="8fc90-174">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="8fc90-174">-CustomerLastName</span></span>
<span data-ttu-id="8fc90-175">Nachname des Kunden</span><span class="sxs-lookup"><span data-stu-id="8fc90-175">Customer last name.</span></span>

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

### <span data-ttu-id="8fc90-176">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="8fc90-176">-CustomerPhoneNumber</span></span>
<span data-ttu-id="8fc90-177">Kundentelefonnummer.</span><span class="sxs-lookup"><span data-stu-id="8fc90-177">Customer phone number.</span></span>
<span data-ttu-id="8fc90-178">Dies ist erforderlich, wenn die bevorzugte Kontaktmethode Telefon ist.</span><span class="sxs-lookup"><span data-stu-id="8fc90-178">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="8fc90-179">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="8fc90-179">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="8fc90-180">Peferred-Sprache des benutzerdefinierten.</span><span class="sxs-lookup"><span data-stu-id="8fc90-180">Peferred language of the custom.</span></span>
<span data-ttu-id="8fc90-181">Hierbei muss es sich um einen gültigen sprach Fortsetzungs Code für eine der hier aufgeführten unterstützten Sprachen handeln https://azure.microsoft.com/en-us/support/faq/ .</span><span class="sxs-lookup"><span data-stu-id="8fc90-181">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/en-us/support/faq/.</span></span>

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

### <span data-ttu-id="8fc90-182">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="8fc90-182">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="8fc90-183">Bevorzugte Zeitzone des Kunden.</span><span class="sxs-lookup"><span data-stu-id="8fc90-183">Customer preferred time zone.</span></span>
<span data-ttu-id="8fc90-184">Dies muss ein gültiger System.TimeZoneInfo.ID-Wert sein.</span><span class="sxs-lookup"><span data-stu-id="8fc90-184">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="8fc90-185">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="8fc90-185">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="8fc90-186">Primäre e-Mail-Adresse des Kunden.</span><span class="sxs-lookup"><span data-stu-id="8fc90-186">Customer primary email address.</span></span>

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

### <span data-ttu-id="8fc90-187">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fc90-187">-DefaultProfile</span></span>
<span data-ttu-id="8fc90-188">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8fc90-188">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fc90-189">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8fc90-189">-Description</span></span>
<span data-ttu-id="8fc90-190">Detaillierte Beschreibung der Frage oder des Problems.</span><span class="sxs-lookup"><span data-stu-id="8fc90-190">Detailed description of the question or issue.</span></span>

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

### <span data-ttu-id="8fc90-191">-Name</span><span class="sxs-lookup"><span data-stu-id="8fc90-191">-Name</span></span>
<span data-ttu-id="8fc90-192">Name des Support Tickets, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8fc90-192">Name of support ticket that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8fc90-193">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="8fc90-193">-PreferredContactMethod</span></span>
<span data-ttu-id="8fc90-194">Bevorzugte Kontaktmethode.</span><span class="sxs-lookup"><span data-stu-id="8fc90-194">Preferred contact method.</span></span>

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

### <span data-ttu-id="8fc90-195">-ProblemClassificationId</span><span class="sxs-lookup"><span data-stu-id="8fc90-195">-ProblemClassificationId</span></span>
<span data-ttu-id="8fc90-196">Jeder Azure-Dienst verfügt über einen eigenen Satz der Problemkategorie, der dem Typ des aufgetretenen Problems entspricht.</span><span class="sxs-lookup"><span data-stu-id="8fc90-196">Each Azure service has its own set of issue category called problem classification that corresponds to the type of problem you're experiencing.</span></span>
<span data-ttu-id="8fc90-197">Dieser Parameter ist die Arm-Ressourcen-ID der ProblemClassification-Ressource.</span><span class="sxs-lookup"><span data-stu-id="8fc90-197">This parameter is the ARM resource id of ProblemClassification resource.</span></span>

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

### <span data-ttu-id="8fc90-198">-ProblemStartTime</span><span class="sxs-lookup"><span data-stu-id="8fc90-198">-ProblemStartTime</span></span>
<span data-ttu-id="8fc90-199">Datum und Uhrzeit des Starts des Problems.</span><span class="sxs-lookup"><span data-stu-id="8fc90-199">Date and time when the problem started.</span></span>

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

### <span data-ttu-id="8fc90-200">-QuotaTicketDetail</span><span class="sxs-lookup"><span data-stu-id="8fc90-200">-QuotaTicketDetail</span></span>
<span data-ttu-id="8fc90-201">Weitere Details zu einem Kontingent Support-Ticket.</span><span class="sxs-lookup"><span data-stu-id="8fc90-201">Additional details for a Quota support ticket.</span></span>

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

### <span data-ttu-id="8fc90-202">-Require24X7Response</span><span class="sxs-lookup"><span data-stu-id="8fc90-202">-Require24X7Response</span></span>
<span data-ttu-id="8fc90-203">Gibt an, ob für dieses Support Ticket eine 24X7-Antwort von Azure erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="8fc90-203">Indicates if this support ticket requires a 24x7 response from Azure.</span></span>

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

### <span data-ttu-id="8fc90-204">-Schweregrad</span><span class="sxs-lookup"><span data-stu-id="8fc90-204">-Severity</span></span>
<span data-ttu-id="8fc90-205">Schweregrad des Support Tickets.</span><span class="sxs-lookup"><span data-stu-id="8fc90-205">Severity of the support ticket.</span></span>
<span data-ttu-id="8fc90-206">Dies zeigt die Dringlichkeit des Falls an, die wiederum die Antwortzeit entsprechend der Vereinbarung zum Service Level des Technical Support-Plans festlegt, den Sie mit Azure haben.</span><span class="sxs-lookup"><span data-stu-id="8fc90-206">This indicates the urgency of the case, which in turn determines the response time according to the service level agreement of the technical support plan you have with Azure.</span></span>

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

### <span data-ttu-id="8fc90-207">-TechnicalTicketResourceId</span><span class="sxs-lookup"><span data-stu-id="8fc90-207">-TechnicalTicketResourceId</span></span>
<span data-ttu-id="8fc90-208">Hierbei handelt es sich um die Ressourcen-ID der Azure-Dienstressource (Beispiel: eine Ressource für einen virtuellen Computer oder eine HDInsight-Ressource), für die das Support Ticket erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8fc90-208">This is the resource id of the Azure service resource (For example: A virtual machine resource or an HDInsight resource) for which the support ticket is created.</span></span>

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

### <span data-ttu-id="8fc90-209">-Title</span><span class="sxs-lookup"><span data-stu-id="8fc90-209">-Title</span></span>
<span data-ttu-id="8fc90-210">Titel des Support Tickets.</span><span class="sxs-lookup"><span data-stu-id="8fc90-210">Title of support ticket.</span></span>

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

### <span data-ttu-id="8fc90-211">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8fc90-211">-Confirm</span></span>
<span data-ttu-id="8fc90-212">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8fc90-212">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fc90-213">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fc90-213">-WhatIf</span></span>
<span data-ttu-id="8fc90-214">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8fc90-214">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fc90-215">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8fc90-215">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fc90-216">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fc90-216">CommonParameters</span></span>
<span data-ttu-id="8fc90-217">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fc90-217">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fc90-218">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8fc90-218">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fc90-219">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8fc90-219">INPUTS</span></span>

### <span data-ttu-id="8fc90-220">Keine</span><span class="sxs-lookup"><span data-stu-id="8fc90-220">None</span></span>

## <span data-ttu-id="8fc90-221">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8fc90-221">OUTPUTS</span></span>

### <span data-ttu-id="8fc90-222">Microsoft. Azure. Commands. Support. Models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="8fc90-222">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="8fc90-223">Notizen</span><span class="sxs-lookup"><span data-stu-id="8fc90-223">NOTES</span></span>

## <span data-ttu-id="8fc90-224">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8fc90-224">RELATED LINKS</span></span>
