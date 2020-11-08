---
Module Name: Az.NotificationHubs
Module Guid: f875725d-8ce4-423f-a6af-ea880bc63f13
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs
Help Version: 4.1.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
ms.openlocfilehash: dd39a8f87120ea7aaddb4570276e1e3060873e2f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997041"
---
# <span data-ttu-id="d9573-101">AZ. NotificationHubs-Modul</span><span class="sxs-lookup"><span data-stu-id="d9573-101">Az.NotificationHubs Module</span></span>
## <span data-ttu-id="d9573-102">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9573-102">Description</span></span>
<span data-ttu-id="d9573-103">In diesem Thema werden Hilfethemen für die Azure-Benachrichtigungs-Hub-Cmdlets angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d9573-103">This topic displays help topics for the Azure Notification Hub cmdlets.</span></span> <span data-ttu-id="d9573-104">Benachrichtigungshubs werden verwendet, um Push-Benachrichtigungen an mehrere Clients zu senden, und zwar unabhängig von der Plattform (Ios, Android, Windows Phone 8, Windows Store usw.), die von diesen Clients verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d9573-104">Notification hubs are used to send push notifications to multiple clients regardless of the platform (iOS, Android, Windows Phone 8, Windows Store, etc.) used by those clients.</span></span> <span data-ttu-id="d9573-105">Diese Hubs sind in etwa mit einzelnen apps vergleichbar: jede Ihrer Apps verfügt in der Regel über einen eigenen Benachrichtigungs-Hub.</span><span class="sxs-lookup"><span data-stu-id="d9573-105">These hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span> <span data-ttu-id="d9573-106">Benachrichtigungshubs sind in logischen Containern organisiert, die als Namespaces bezeichnet werden, und die Autorisierungsregeln für Shared Access-Signaturen (SAS) werden verwendet, um den Zugriff auf Hubs und Namespaces zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="d9573-106">Notification hubs are organized within logical containers known as namespaces, and Shared Access Signature (SAS) authorization rules are used to manage access to hubs and namespaces.</span></span> <span data-ttu-id="d9573-107">Alle diese Elemente können mithilfe der Notification Hub-Cmdlets verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="d9573-107">All of these elements can be administered by using the Notification Hub cmdlets.</span></span>

## <span data-ttu-id="d9573-108">AZ. NotificationHubs-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="d9573-108">Az.NotificationHubs Cmdlets</span></span>
### [<span data-ttu-id="d9573-109">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="d9573-109">Get-AzNotificationHub</span></span>](Get-AzNotificationHub.md)
<span data-ttu-id="d9573-110">Ruft Informationen zu ihren benachrichtigungshubs ab.</span><span class="sxs-lookup"><span data-stu-id="d9573-110">Gets information about your notification hubs.</span></span>

### [<span data-ttu-id="d9573-111">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d9573-111">Get-AzNotificationHubAuthorizationRule</span></span>](Get-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="d9573-112">Ruft Informationen zu den Autorisierungsregeln ab, die einem Benachrichtigungs-Hub zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d9573-112">Gets information about the authorization rules associated with a notification hub.</span></span>

### [<span data-ttu-id="d9573-113">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="d9573-113">Get-AzNotificationHubListKey</span></span>](Get-AzNotificationHubListKey.md)
<span data-ttu-id="d9573-114">Ruft die primären und sekundären Verbindungszeichenfolgen ab, die einer Benachrichtigungs-Hub-Autorisierungsregel zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d9573-114">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

### [<span data-ttu-id="d9573-115">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="d9573-115">Get-AzNotificationHubPNSCredential</span></span>](Get-AzNotificationHubPNSCredential.md)
<span data-ttu-id="d9573-116">Ruft die PNS-Anmeldeinformationen für einen Benachrichtigungs-Hub ab.</span><span class="sxs-lookup"><span data-stu-id="d9573-116">Gets the PNS credentials for a notification hub.</span></span>

### [<span data-ttu-id="d9573-117">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="d9573-117">Get-AzNotificationHubsNamespace</span></span>](Get-AzNotificationHubsNamespace.md)
<span data-ttu-id="d9573-118">Ruft Informationen zu einem Notification Hub-Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="d9573-118">Gets information about a notification hub namespace.</span></span>

### [<span data-ttu-id="d9573-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d9573-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Get-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="d9573-120">Ruft Informationen zu den Autorisierungsregeln ab, die einem Notification Hub-Namespace zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d9573-120">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

### [<span data-ttu-id="d9573-121">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="d9573-121">Get-AzNotificationHubsNamespaceListKey</span></span>](Get-AzNotificationHubsNamespaceListKey.md)
<span data-ttu-id="d9573-122">Ruft die primären und sekundären Verbindungszeichenfolgen ab, die einer Benachrichtigungs-Hub-Namespace Autorisierungsregel zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d9573-122">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

### [<span data-ttu-id="d9573-123">Neu – AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="d9573-123">New-AzNotificationHub</span></span>](New-AzNotificationHub.md)
<span data-ttu-id="d9573-124">Erstellt einen Benachrichtigungs-Hub.</span><span class="sxs-lookup"><span data-stu-id="d9573-124">Creates a notification hub.</span></span>

### [<span data-ttu-id="d9573-125">Neu – AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d9573-125">New-AzNotificationHubAuthorizationRule</span></span>](New-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="d9573-126">Erstellt eine Autorisierungsregel und weist die Regel einem Benachrichtigungs-Hub zu.</span><span class="sxs-lookup"><span data-stu-id="d9573-126">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

### [<span data-ttu-id="d9573-127">Neu – AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="d9573-127">New-AzNotificationHubKey</span></span>](New-AzNotificationHubKey.md)
<span data-ttu-id="d9573-128">Generieren Sie den Autorisierungsregel Schlüssel für eine NotificationHub erneut.</span><span class="sxs-lookup"><span data-stu-id="d9573-128">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

### [<span data-ttu-id="d9573-129">Neu – AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="d9573-129">New-AzNotificationHubsNamespace</span></span>](New-AzNotificationHubsNamespace.md)
<span data-ttu-id="d9573-130">Erstellt einen Benachrichtigungs-Hub-Namespace.</span><span class="sxs-lookup"><span data-stu-id="d9573-130">Creates a notification hub namespace.</span></span>

### [<span data-ttu-id="d9573-131">Neu – AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d9573-131">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](New-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="d9573-132">Erstellt eine Autorisierungsregel und weist diese Regel einem Benachrichtigungs-Hub-Namespace zu.</span><span class="sxs-lookup"><span data-stu-id="d9573-132">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

### [<span data-ttu-id="d9573-133">Neu – AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="d9573-133">New-AzNotificationHubsNamespaceKey</span></span>](New-AzNotificationHubsNamespaceKey.md)
<span data-ttu-id="d9573-134">Generieren Sie den Autorisierungsregel Schlüssel für einen Namespace erneut.</span><span class="sxs-lookup"><span data-stu-id="d9573-134">Regenerate the Authorization Rule Key for a Namespace.</span></span>

### [<span data-ttu-id="d9573-135">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="d9573-135">Remove-AzNotificationHub</span></span>](Remove-AzNotificationHub.md)
<span data-ttu-id="d9573-136">Entfernt einen vorhandenen Benachrichtigungs-Hub.</span><span class="sxs-lookup"><span data-stu-id="d9573-136">Removes an existing notification hub.</span></span>

### [<span data-ttu-id="d9573-137">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d9573-137">Remove-AzNotificationHubAuthorizationRule</span></span>](Remove-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="d9573-138">Entfernt eine Autorisierungsregel aus einem Benachrichtigungs-Hub.</span><span class="sxs-lookup"><span data-stu-id="d9573-138">Removes an authorization rule from a notification hub.</span></span>

### [<span data-ttu-id="d9573-139">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="d9573-139">Remove-AzNotificationHubsNamespace</span></span>](Remove-AzNotificationHubsNamespace.md)
<span data-ttu-id="d9573-140">Entfernt einen Benachrichtigungs-Hub-Namespace.</span><span class="sxs-lookup"><span data-stu-id="d9573-140">Removes a notification hub namespace.</span></span>

### [<span data-ttu-id="d9573-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d9573-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Remove-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="d9573-142">Entfernt eine Autorisierungsregel aus einem Notification Hub-Namespace.</span><span class="sxs-lookup"><span data-stu-id="d9573-142">Removes an authorization rule from a notification hub namespace.</span></span>

### [<span data-ttu-id="d9573-143">Satz-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="d9573-143">Set-AzNotificationHub</span></span>](Set-AzNotificationHub.md)
<span data-ttu-id="d9573-144">Legt Eigenschaftswerte für einen Benachrichtigungs-Hub fest.</span><span class="sxs-lookup"><span data-stu-id="d9573-144">Sets property values for a notification hub.</span></span>

### [<span data-ttu-id="d9573-145">Satz-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d9573-145">Set-AzNotificationHubAuthorizationRule</span></span>](Set-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="d9573-146">Legt Autorisierungsregeln für einen Benachrichtigungs-Hub fest.</span><span class="sxs-lookup"><span data-stu-id="d9573-146">Sets authorization rules for a notification hub.</span></span>

### [<span data-ttu-id="d9573-147">Satz-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="d9573-147">Set-AzNotificationHubsNamespace</span></span>](Set-AzNotificationHubsNamespace.md)
<span data-ttu-id="d9573-148">Legt Eigenschaftswerte für einen Notification Hub-Namespace fest.</span><span class="sxs-lookup"><span data-stu-id="d9573-148">Sets property values for a notification hub namespace.</span></span>

### [<span data-ttu-id="d9573-149">Satz-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d9573-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Set-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="d9573-150">Legt Autorisierungsregeln für einen Benachrichtigungs-Hub-Namespace fest.</span><span class="sxs-lookup"><span data-stu-id="d9573-150">Sets authorization rules for a notification hub namespace.</span></span>

