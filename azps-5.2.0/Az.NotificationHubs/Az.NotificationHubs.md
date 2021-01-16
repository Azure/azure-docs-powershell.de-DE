---
Module Name: Az.NotificationHubs
Module Guid: f875725d-8ce4-423f-a6af-ea880bc63f13
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs
Help Version: 4.1.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
ms.openlocfilehash: dd39a8f87120ea7aaddb4570276e1e3060873e2f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295912"
---
# <span data-ttu-id="1cb23-101">Az.NotificationHubs-Modul</span><span class="sxs-lookup"><span data-stu-id="1cb23-101">Az.NotificationHubs Module</span></span>
## <span data-ttu-id="1cb23-102">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1cb23-102">Description</span></span>
<span data-ttu-id="1cb23-103">In diesem Thema werden Hilfethemen für die Azure Notification Hub-Cmdlets angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1cb23-103">This topic displays help topics for the Azure Notification Hub cmdlets.</span></span> <span data-ttu-id="1cb23-104">Benachrichtigungshubs werden verwendet, um Pushbenachrichtigungen unabhängig von der von diesen Clients verwendeten Plattform (iOS, Android, Windows Phone 8, Windows Store usw.) an mehrere Clients zu senden.</span><span class="sxs-lookup"><span data-stu-id="1cb23-104">Notification hubs are used to send push notifications to multiple clients regardless of the platform (iOS, Android, Windows Phone 8, Windows Store, etc.) used by those clients.</span></span> <span data-ttu-id="1cb23-105">Diese Hubs sind in etwa gleichbedeutend mit einzelnen Apps: Jede Ihrer Apps hat in der Regel einen eigenen Benachrichtigungshub.</span><span class="sxs-lookup"><span data-stu-id="1cb23-105">These hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span> <span data-ttu-id="1cb23-106">Benachrichtigungshubs sind in logischen Containern organisiert, die als Namespaces bezeichnet werden, und SAS (Shared Access Signature)-Autorisierungsregeln werden verwendet, um den Zugriff auf Hubs und Namespaces zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="1cb23-106">Notification hubs are organized within logical containers known as namespaces, and Shared Access Signature (SAS) authorization rules are used to manage access to hubs and namespaces.</span></span> <span data-ttu-id="1cb23-107">Alle diese Elemente können mithilfe der Cmdlets für den Benachrichtigungshub verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="1cb23-107">All of these elements can be administered by using the Notification Hub cmdlets.</span></span>

## <span data-ttu-id="1cb23-108">Az.NotificationHubs-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="1cb23-108">Az.NotificationHubs Cmdlets</span></span>
### [<span data-ttu-id="1cb23-109">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="1cb23-109">Get-AzNotificationHub</span></span>](Get-AzNotificationHub.md)
<span data-ttu-id="1cb23-110">Ruft Informationen zu Ihren Benachrichtigungshubs ab.</span><span class="sxs-lookup"><span data-stu-id="1cb23-110">Gets information about your notification hubs.</span></span>

### [<span data-ttu-id="1cb23-111">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1cb23-111">Get-AzNotificationHubAuthorizationRule</span></span>](Get-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="1cb23-112">Ruft Informationen zu den Autorisierungsregeln ab, die einem Benachrichtigungshub zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1cb23-112">Gets information about the authorization rules associated with a notification hub.</span></span>

### [<span data-ttu-id="1cb23-113">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="1cb23-113">Get-AzNotificationHubListKey</span></span>](Get-AzNotificationHubListKey.md)
<span data-ttu-id="1cb23-114">Ruft die primären und sekundären Verbindungszeichenfolgen ab, die einer Benachrichtigungshubautorisierungsregel zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1cb23-114">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

### [<span data-ttu-id="1cb23-115">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="1cb23-115">Get-AzNotificationHubPNSCredential</span></span>](Get-AzNotificationHubPNSCredential.md)
<span data-ttu-id="1cb23-116">Ruft die PNS-Anmeldeinformationen für einen Benachrichtigungshub ab.</span><span class="sxs-lookup"><span data-stu-id="1cb23-116">Gets the PNS credentials for a notification hub.</span></span>

### [<span data-ttu-id="1cb23-117">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1cb23-117">Get-AzNotificationHubsNamespace</span></span>](Get-AzNotificationHubsNamespace.md)
<span data-ttu-id="1cb23-118">Ruft Informationen zu einem Benachrichtigungshub-Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="1cb23-118">Gets information about a notification hub namespace.</span></span>

### [<span data-ttu-id="1cb23-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1cb23-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Get-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="1cb23-120">Ruft Informationen zu den Autorisierungsregeln ab, die einem Benachrichtigungshub-Namespace zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1cb23-120">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

### [<span data-ttu-id="1cb23-121">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="1cb23-121">Get-AzNotificationHubsNamespaceListKey</span></span>](Get-AzNotificationHubsNamespaceListKey.md)
<span data-ttu-id="1cb23-122">Ruft die primären und sekundären Verbindungszeichenfolgen ab, die einer Autorisierungsregel für den Benachrichtigungshubnamespace zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1cb23-122">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

### [<span data-ttu-id="1cb23-123">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="1cb23-123">New-AzNotificationHub</span></span>](New-AzNotificationHub.md)
<span data-ttu-id="1cb23-124">Erstellt einen Benachrichtigungshub.</span><span class="sxs-lookup"><span data-stu-id="1cb23-124">Creates a notification hub.</span></span>

### [<span data-ttu-id="1cb23-125">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1cb23-125">New-AzNotificationHubAuthorizationRule</span></span>](New-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="1cb23-126">Erstellt eine Autorisierungsregel und weist die Regel einem Benachrichtigungshub zu.</span><span class="sxs-lookup"><span data-stu-id="1cb23-126">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

### [<span data-ttu-id="1cb23-127">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="1cb23-127">New-AzNotificationHubKey</span></span>](New-AzNotificationHubKey.md)
<span data-ttu-id="1cb23-128">Erstellen Sie den Autorisierungsregelschlüssel für einen NotificationHub erneut.</span><span class="sxs-lookup"><span data-stu-id="1cb23-128">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

### [<span data-ttu-id="1cb23-129">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1cb23-129">New-AzNotificationHubsNamespace</span></span>](New-AzNotificationHubsNamespace.md)
<span data-ttu-id="1cb23-130">Erstellt einen Benachrichtigungshub-Namespace.</span><span class="sxs-lookup"><span data-stu-id="1cb23-130">Creates a notification hub namespace.</span></span>

### [<span data-ttu-id="1cb23-131">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1cb23-131">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](New-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="1cb23-132">Erstellt eine Autorisierungsregel und weist diese Regel einem Benachrichtigungshub-Namespace zu.</span><span class="sxs-lookup"><span data-stu-id="1cb23-132">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

### [<span data-ttu-id="1cb23-133">New-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="1cb23-133">New-AzNotificationHubsNamespaceKey</span></span>](New-AzNotificationHubsNamespaceKey.md)
<span data-ttu-id="1cb23-134">Erstellen Sie den Autorisierungsregelschlüssel für einen Namespace erneut.</span><span class="sxs-lookup"><span data-stu-id="1cb23-134">Regenerate the Authorization Rule Key for a Namespace.</span></span>

### [<span data-ttu-id="1cb23-135">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="1cb23-135">Remove-AzNotificationHub</span></span>](Remove-AzNotificationHub.md)
<span data-ttu-id="1cb23-136">Entfernt einen vorhandenen Benachrichtigungshub.</span><span class="sxs-lookup"><span data-stu-id="1cb23-136">Removes an existing notification hub.</span></span>

### [<span data-ttu-id="1cb23-137">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1cb23-137">Remove-AzNotificationHubAuthorizationRule</span></span>](Remove-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="1cb23-138">Entfernt eine Autorisierungsregel von einem Benachrichtigungshub.</span><span class="sxs-lookup"><span data-stu-id="1cb23-138">Removes an authorization rule from a notification hub.</span></span>

### [<span data-ttu-id="1cb23-139">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1cb23-139">Remove-AzNotificationHubsNamespace</span></span>](Remove-AzNotificationHubsNamespace.md)
<span data-ttu-id="1cb23-140">Entfernt einen Benachrichtigungshub-Namespace.</span><span class="sxs-lookup"><span data-stu-id="1cb23-140">Removes a notification hub namespace.</span></span>

### [<span data-ttu-id="1cb23-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1cb23-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Remove-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="1cb23-142">Entfernt eine Autorisierungsregel aus einem Benachrichtigungshub-Namespace.</span><span class="sxs-lookup"><span data-stu-id="1cb23-142">Removes an authorization rule from a notification hub namespace.</span></span>

### [<span data-ttu-id="1cb23-143">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="1cb23-143">Set-AzNotificationHub</span></span>](Set-AzNotificationHub.md)
<span data-ttu-id="1cb23-144">Legt Eigenschaftswerte für einen Benachrichtigungshub fest.</span><span class="sxs-lookup"><span data-stu-id="1cb23-144">Sets property values for a notification hub.</span></span>

### [<span data-ttu-id="1cb23-145">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1cb23-145">Set-AzNotificationHubAuthorizationRule</span></span>](Set-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="1cb23-146">Legt Autorisierungsregeln für einen Benachrichtigungshub fest.</span><span class="sxs-lookup"><span data-stu-id="1cb23-146">Sets authorization rules for a notification hub.</span></span>

### [<span data-ttu-id="1cb23-147">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1cb23-147">Set-AzNotificationHubsNamespace</span></span>](Set-AzNotificationHubsNamespace.md)
<span data-ttu-id="1cb23-148">Legt Eigenschaftswerte für einen Benachrichtigungshub-Namespace fest.</span><span class="sxs-lookup"><span data-stu-id="1cb23-148">Sets property values for a notification hub namespace.</span></span>

### [<span data-ttu-id="1cb23-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1cb23-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Set-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="1cb23-150">Legt Autorisierungsregeln für einen Benachrichtigungshub-Namespace fest.</span><span class="sxs-lookup"><span data-stu-id="1cb23-150">Sets authorization rules for a notification hub namespace.</span></span>

