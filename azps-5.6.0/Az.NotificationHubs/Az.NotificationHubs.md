---
Module Name: Az.NotificationHubs
Module Guid: f875725d-8ce4-423f-a6af-ea880bc63f13
Download Help Link: https://docs.microsoft.com/powershell/module/az.notificationhubs
Help Version: 4.1.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
ms.openlocfilehash: f82f5ec814159bd71a83594a501df3561b747aee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918328"
---
# <span data-ttu-id="bf8dc-101">Az.NotificationHubs-Modul</span><span class="sxs-lookup"><span data-stu-id="bf8dc-101">Az.NotificationHubs Module</span></span>
## <span data-ttu-id="bf8dc-102">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf8dc-102">Description</span></span>
<span data-ttu-id="bf8dc-103">In diesem Thema werden Hilfethemen für die Azure Notification Hub-Cmdlets angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bf8dc-103">This topic displays help topics for the Azure Notification Hub cmdlets.</span></span> <span data-ttu-id="bf8dc-104">Benachrichtigungshubs werden verwendet, um Pushbenachrichtigungen an mehrere Clients zu senden, unabhängig von der Plattform (iOS, Android, Windows Phone 8, Windows Store usw.), die von diesen Clients verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bf8dc-104">Notification hubs are used to send push notifications to multiple clients regardless of the platform (iOS, Android, Windows Phone 8, Windows Store, etc.) used by those clients.</span></span> <span data-ttu-id="bf8dc-105">Diese Hubs sind in etwa mit einzelnen Apps vergleichbar: Jede Ihrer Apps hat in der Regel einen eigenen Benachrichtigungshub.</span><span class="sxs-lookup"><span data-stu-id="bf8dc-105">These hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span> <span data-ttu-id="bf8dc-106">Benachrichtigungshubs sind in logischen Containern organisiert, die als Namespaces bezeichnet werden, und Sas-Autorisierungsregeln (Shared Access Signature) werden verwendet, um den Zugriff auf Hubs und Namespaces zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="bf8dc-106">Notification hubs are organized within logical containers known as namespaces, and Shared Access Signature (SAS) authorization rules are used to manage access to hubs and namespaces.</span></span> <span data-ttu-id="bf8dc-107">Alle diese Elemente können mithilfe der Notification Hub-Cmdlets verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="bf8dc-107">All of these elements can be administered by using the Notification Hub cmdlets.</span></span>

## <span data-ttu-id="bf8dc-108">Az.NotificationHubs-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bf8dc-108">Az.NotificationHubs Cmdlets</span></span>
### [<span data-ttu-id="bf8dc-109">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="bf8dc-109">Get-AzNotificationHub</span></span>](Get-AzNotificationHub.md)
<span data-ttu-id="bf8dc-110">Ruft Informationen zu Ihren Benachrichtigungshubs ab.</span><span class="sxs-lookup"><span data-stu-id="bf8dc-110">Gets information about your notification hubs.</span></span>

### [<span data-ttu-id="bf8dc-111">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bf8dc-111">Get-AzNotificationHubAuthorizationRule</span></span>](Get-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="bf8dc-112">Ruft Informationen zu den Autorisierungsregeln ab, die einem Benachrichtigungshub zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="bf8dc-112">Gets information about the authorization rules associated with a notification hub.</span></span>

### [<span data-ttu-id="bf8dc-113">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="bf8dc-113">Get-AzNotificationHubListKey</span></span>](Get-AzNotificationHubListKey.md)
<span data-ttu-id="bf8dc-114">Ruft die primären und sekundären Verbindungszeichenfolgen ab, die einer Benachrichtigungshubautorisierungsregel zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="bf8dc-114">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

### [<span data-ttu-id="bf8dc-115">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="bf8dc-115">Get-AzNotificationHubPNSCredential</span></span>](Get-AzNotificationHubPNSCredential.md)
<span data-ttu-id="bf8dc-116">Ruft die PNS-Anmeldeinformationen für einen Benachrichtigungshub ab.</span><span class="sxs-lookup"><span data-stu-id="bf8dc-116">Gets the PNS credentials for a notification hub.</span></span>

### [<span data-ttu-id="bf8dc-117">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="bf8dc-117">Get-AzNotificationHubsNamespace</span></span>](Get-AzNotificationHubsNamespace.md)
<span data-ttu-id="bf8dc-118">Ruft Informationen zu einem Benachrichtigungshubnamespace ab.</span><span class="sxs-lookup"><span data-stu-id="bf8dc-118">Gets information about a notification hub namespace.</span></span>

### [<span data-ttu-id="bf8dc-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bf8dc-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Get-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="bf8dc-120">Ruft Informationen zu den Autorisierungsregeln ab, die einem Benachrichtigungshubnamespace zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="bf8dc-120">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

### [<span data-ttu-id="bf8dc-121">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="bf8dc-121">Get-AzNotificationHubsNamespaceListKey</span></span>](Get-AzNotificationHubsNamespaceListKey.md)
<span data-ttu-id="bf8dc-122">Ruft die primären und sekundären Verbindungszeichenfolgen ab, die einer Benachrichtigungshub-Namespaceautorisierungsregel zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="bf8dc-122">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

### [<span data-ttu-id="bf8dc-123">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="bf8dc-123">New-AzNotificationHub</span></span>](New-AzNotificationHub.md)
<span data-ttu-id="bf8dc-124">Erstellt einen Benachrichtigungshub.</span><span class="sxs-lookup"><span data-stu-id="bf8dc-124">Creates a notification hub.</span></span>

### [<span data-ttu-id="bf8dc-125">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bf8dc-125">New-AzNotificationHubAuthorizationRule</span></span>](New-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="bf8dc-126">Erstellt eine Autorisierungsregel und weist die Regel einem Benachrichtigungshub zu.</span><span class="sxs-lookup"><span data-stu-id="bf8dc-126">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

### [<span data-ttu-id="bf8dc-127">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="bf8dc-127">New-AzNotificationHubKey</span></span>](New-AzNotificationHubKey.md)
<span data-ttu-id="bf8dc-128">Regenerieren Sie den Autorisierungsregelschlüssel für einen NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="bf8dc-128">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

### [<span data-ttu-id="bf8dc-129">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="bf8dc-129">New-AzNotificationHubsNamespace</span></span>](New-AzNotificationHubsNamespace.md)
<span data-ttu-id="bf8dc-130">Erstellt einen Benachrichtigungshubnamespace.</span><span class="sxs-lookup"><span data-stu-id="bf8dc-130">Creates a notification hub namespace.</span></span>

### [<span data-ttu-id="bf8dc-131">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bf8dc-131">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](New-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="bf8dc-132">Erstellt eine Autorisierungsregel und weist diese Regel einem Benachrichtigungshubnamespace zu.</span><span class="sxs-lookup"><span data-stu-id="bf8dc-132">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

### [<span data-ttu-id="bf8dc-133">New-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="bf8dc-133">New-AzNotificationHubsNamespaceKey</span></span>](New-AzNotificationHubsNamespaceKey.md)
<span data-ttu-id="bf8dc-134">Regenerieren Sie den Autorisierungsregelschlüssel für einen Namespace.</span><span class="sxs-lookup"><span data-stu-id="bf8dc-134">Regenerate the Authorization Rule Key for a Namespace.</span></span>

### [<span data-ttu-id="bf8dc-135">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="bf8dc-135">Remove-AzNotificationHub</span></span>](Remove-AzNotificationHub.md)
<span data-ttu-id="bf8dc-136">Entfernt einen vorhandenen Benachrichtigungshub.</span><span class="sxs-lookup"><span data-stu-id="bf8dc-136">Removes an existing notification hub.</span></span>

### [<span data-ttu-id="bf8dc-137">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bf8dc-137">Remove-AzNotificationHubAuthorizationRule</span></span>](Remove-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="bf8dc-138">Entfernt eine Autorisierungsregel von einem Benachrichtigungshub.</span><span class="sxs-lookup"><span data-stu-id="bf8dc-138">Removes an authorization rule from a notification hub.</span></span>

### [<span data-ttu-id="bf8dc-139">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="bf8dc-139">Remove-AzNotificationHubsNamespace</span></span>](Remove-AzNotificationHubsNamespace.md)
<span data-ttu-id="bf8dc-140">Entfernt einen Benachrichtigungshubnamespace.</span><span class="sxs-lookup"><span data-stu-id="bf8dc-140">Removes a notification hub namespace.</span></span>

### [<span data-ttu-id="bf8dc-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bf8dc-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Remove-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="bf8dc-142">Entfernt eine Autorisierungsregel aus einem Benachrichtigungshubnamespace.</span><span class="sxs-lookup"><span data-stu-id="bf8dc-142">Removes an authorization rule from a notification hub namespace.</span></span>

### [<span data-ttu-id="bf8dc-143">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="bf8dc-143">Set-AzNotificationHub</span></span>](Set-AzNotificationHub.md)
<span data-ttu-id="bf8dc-144">Legt Eigenschaftswerte für einen Benachrichtigungshub fest.</span><span class="sxs-lookup"><span data-stu-id="bf8dc-144">Sets property values for a notification hub.</span></span>

### [<span data-ttu-id="bf8dc-145">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bf8dc-145">Set-AzNotificationHubAuthorizationRule</span></span>](Set-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="bf8dc-146">Legt Autorisierungsregeln für einen Benachrichtigungshub fest.</span><span class="sxs-lookup"><span data-stu-id="bf8dc-146">Sets authorization rules for a notification hub.</span></span>

### [<span data-ttu-id="bf8dc-147">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="bf8dc-147">Set-AzNotificationHubsNamespace</span></span>](Set-AzNotificationHubsNamespace.md)
<span data-ttu-id="bf8dc-148">Legt Eigenschaftswerte für einen Benachrichtigungshubnamespace fest.</span><span class="sxs-lookup"><span data-stu-id="bf8dc-148">Sets property values for a notification hub namespace.</span></span>

### [<span data-ttu-id="bf8dc-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bf8dc-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Set-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="bf8dc-150">Legt Autorisierungsregeln für einen Benachrichtigungshubnamespace fest.</span><span class="sxs-lookup"><span data-stu-id="bf8dc-150">Sets authorization rules for a notification hub namespace.</span></span>

