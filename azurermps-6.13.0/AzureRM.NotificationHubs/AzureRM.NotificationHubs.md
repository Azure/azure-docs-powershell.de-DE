---
Module Name: AzureRM.NotificationHubs
Module Guid: f875725d-8ce4-423f-a6af-ea880bc63f13
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/AzureRM.NotificationHubs.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/AzureRM.NotificationHubs.md
ms.openlocfilehash: e9f6fce095bd7ea4c494cf778587c3853f347c38
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "93650004"
---
# <span data-ttu-id="a0b1c-101">AzureRM. NotificationHubs-Modul</span><span class="sxs-lookup"><span data-stu-id="a0b1c-101">AzureRM.NotificationHubs Module</span></span>
## <span data-ttu-id="a0b1c-102">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0b1c-102">Description</span></span>
<span data-ttu-id="a0b1c-103">In diesem Thema werden Hilfethemen für die Azure-Benachrichtigungs-Hub-Cmdlets angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a0b1c-103">This topic displays help topics for the Azure Notification Hub cmdlets.</span></span> <span data-ttu-id="a0b1c-104">Benachrichtigungshubs werden verwendet, um Push-Benachrichtigungen an mehrere Clients zu senden, und zwar unabhängig von der Plattform (Ios, Android, Windows Phone 8, Windows Store usw.), die von diesen Clients verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a0b1c-104">Notification hubs are used to send push notifications to multiple clients regardless of the platform (iOS, Android, Windows Phone 8, Windows Store, etc.) used by those clients.</span></span> <span data-ttu-id="a0b1c-105">Diese Hubs sind in etwa mit einzelnen apps vergleichbar: jede Ihrer Apps verfügt in der Regel über einen eigenen Benachrichtigungs-Hub.</span><span class="sxs-lookup"><span data-stu-id="a0b1c-105">These hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span> <span data-ttu-id="a0b1c-106">Benachrichtigungshubs sind in logischen Containern organisiert, die als Namespaces bezeichnet werden, und die Autorisierungsregeln für Shared Access-Signaturen (SAS) werden verwendet, um den Zugriff auf Hubs und Namespaces zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="a0b1c-106">Notification hubs are organized within logical containers known as namespaces, and Shared Access Signature (SAS) authorization rules are used to manage access to hubs and namespaces.</span></span> <span data-ttu-id="a0b1c-107">Alle diese Elemente können mithilfe der Notification Hub-Cmdlets verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="a0b1c-107">All of these elements can be administered by using the Notification Hub cmdlets.</span></span>

## <span data-ttu-id="a0b1c-108">AzureRM. NotificationHubs-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a0b1c-108">AzureRM.NotificationHubs Cmdlets</span></span>
### [<span data-ttu-id="a0b1c-109">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a0b1c-109">Get-AzureRmNotificationHub</span></span>](Get-AzureRmNotificationHub.md)
<span data-ttu-id="a0b1c-110">Ruft Informationen zu ihren benachrichtigungshubs ab.</span><span class="sxs-lookup"><span data-stu-id="a0b1c-110">Gets information about your notification hubs.</span></span>

### [<span data-ttu-id="a0b1c-111">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="a0b1c-111">Get-AzureRmNotificationHubAuthorizationRules</span></span>](Get-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="a0b1c-112">Ruft Informationen zu den Autorisierungsregeln ab, die einem Benachrichtigungs-Hub zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a0b1c-112">Gets information about the authorization rules associated with a notification hub.</span></span>

### [<span data-ttu-id="a0b1c-113">Get-AzureRmNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="a0b1c-113">Get-AzureRmNotificationHubListKeys</span></span>](Get-AzureRmNotificationHubListKeys.md)
<span data-ttu-id="a0b1c-114">Ruft die primären und sekundären Verbindungszeichenfolgen ab, die einer Benachrichtigungs-Hub-Autorisierungsregel zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a0b1c-114">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

### [<span data-ttu-id="a0b1c-115">Get-AzureRmNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="a0b1c-115">Get-AzureRmNotificationHubPNSCredentials</span></span>](Get-AzureRmNotificationHubPNSCredentials.md)
<span data-ttu-id="a0b1c-116">Ruft die PNS-Anmeldeinformationen für einen Benachrichtigungs-Hub ab.</span><span class="sxs-lookup"><span data-stu-id="a0b1c-116">Gets the PNS credentials for a notification hub.</span></span>

### [<span data-ttu-id="a0b1c-117">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="a0b1c-117">Get-AzureRmNotificationHubsNamespace</span></span>](Get-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="a0b1c-118">Ruft Informationen zu einem Notification Hub-Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="a0b1c-118">Gets information about a notification hub namespace.</span></span>

### [<span data-ttu-id="a0b1c-119">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="a0b1c-119">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="a0b1c-120">Ruft Informationen zu den Autorisierungsregeln ab, die einem Notification Hub-Namespace zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a0b1c-120">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

### [<span data-ttu-id="a0b1c-121">Get-AzureRmNotificationHubsNamespaceListKeys</span><span class="sxs-lookup"><span data-stu-id="a0b1c-121">Get-AzureRmNotificationHubsNamespaceListKeys</span></span>](Get-AzureRmNotificationHubsNamespaceListKeys.md)
<span data-ttu-id="a0b1c-122">Ruft die primären und sekundären Verbindungszeichenfolgen ab, die einer Benachrichtigungs-Hub-Namespace Autorisierungsregel zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a0b1c-122">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

### [<span data-ttu-id="a0b1c-123">Neu – AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a0b1c-123">New-AzureRmNotificationHub</span></span>](New-AzureRmNotificationHub.md)
<span data-ttu-id="a0b1c-124">Erstellt einen Benachrichtigungs-Hub.</span><span class="sxs-lookup"><span data-stu-id="a0b1c-124">Creates a notification hub.</span></span>

### [<span data-ttu-id="a0b1c-125">Neu – AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="a0b1c-125">New-AzureRmNotificationHubAuthorizationRules</span></span>](New-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="a0b1c-126">Erstellt eine Autorisierungsregel und weist die Regel einem Benachrichtigungs-Hub zu.</span><span class="sxs-lookup"><span data-stu-id="a0b1c-126">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

### [<span data-ttu-id="a0b1c-127">Neu – AzureRmNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="a0b1c-127">New-AzureRmNotificationHubKey</span></span>](New-AzureRmNotificationHubKey.md)
<span data-ttu-id="a0b1c-128">Generieren Sie den Autorisierungsregel Schlüssel für eine NotificationHub erneut.</span><span class="sxs-lookup"><span data-stu-id="a0b1c-128">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

### [<span data-ttu-id="a0b1c-129">Neu – AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="a0b1c-129">New-AzureRmNotificationHubsNamespace</span></span>](New-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="a0b1c-130">Erstellt einen Benachrichtigungs-Hub-Namespace.</span><span class="sxs-lookup"><span data-stu-id="a0b1c-130">Creates a notification hub namespace.</span></span>

### [<span data-ttu-id="a0b1c-131">Neu – AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="a0b1c-131">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](New-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="a0b1c-132">Erstellt eine Autorisierungsregel und weist diese Regel einem Benachrichtigungs-Hub-Namespace zu.</span><span class="sxs-lookup"><span data-stu-id="a0b1c-132">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

### [<span data-ttu-id="a0b1c-133">Neu – AzureRmNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="a0b1c-133">New-AzureRmNotificationHubsNamespaceKey</span></span>](New-AzureRmNotificationHubsNamespaceKey.md)
<span data-ttu-id="a0b1c-134">Generieren Sie den Autorisierungsregel Schlüssel für einen Namespace erneut.</span><span class="sxs-lookup"><span data-stu-id="a0b1c-134">Regenerate the Authorization Rule Key for a Namespace.</span></span>

### [<span data-ttu-id="a0b1c-135">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a0b1c-135">Remove-AzureRmNotificationHub</span></span>](Remove-AzureRmNotificationHub.md)
<span data-ttu-id="a0b1c-136">Entfernt einen vorhandenen Benachrichtigungs-Hub.</span><span class="sxs-lookup"><span data-stu-id="a0b1c-136">Removes an existing notification hub.</span></span>

### [<span data-ttu-id="a0b1c-137">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="a0b1c-137">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](Remove-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="a0b1c-138">Entfernt eine Autorisierungsregel aus einem Benachrichtigungs-Hub.</span><span class="sxs-lookup"><span data-stu-id="a0b1c-138">Removes an authorization rule from a notification hub.</span></span>

### [<span data-ttu-id="a0b1c-139">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="a0b1c-139">Remove-AzureRmNotificationHubsNamespace</span></span>](Remove-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="a0b1c-140">Entfernt einen Benachrichtigungs-Hub-Namespace.</span><span class="sxs-lookup"><span data-stu-id="a0b1c-140">Removes a notification hub namespace.</span></span>

### [<span data-ttu-id="a0b1c-141">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="a0b1c-141">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="a0b1c-142">Entfernt eine Autorisierungsregel aus einem Notification Hub-Namespace.</span><span class="sxs-lookup"><span data-stu-id="a0b1c-142">Removes an authorization rule from a notification hub namespace.</span></span>

### [<span data-ttu-id="a0b1c-143">Satz-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a0b1c-143">Set-AzureRmNotificationHub</span></span>](Set-AzureRmNotificationHub.md)
<span data-ttu-id="a0b1c-144">Legt Eigenschaftswerte für einen Benachrichtigungs-Hub fest.</span><span class="sxs-lookup"><span data-stu-id="a0b1c-144">Sets property values for a notification hub.</span></span>

### [<span data-ttu-id="a0b1c-145">Satz-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="a0b1c-145">Set-AzureRmNotificationHubAuthorizationRules</span></span>](Set-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="a0b1c-146">Legt Autorisierungsregeln für einen Benachrichtigungs-Hub fest.</span><span class="sxs-lookup"><span data-stu-id="a0b1c-146">Sets authorization rules for a notification hub.</span></span>

### [<span data-ttu-id="a0b1c-147">Satz-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="a0b1c-147">Set-AzureRmNotificationHubsNamespace</span></span>](Set-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="a0b1c-148">Legt Eigenschaftswerte für einen Notification Hub-Namespace fest.</span><span class="sxs-lookup"><span data-stu-id="a0b1c-148">Sets property values for a notification hub namespace.</span></span>

### [<span data-ttu-id="a0b1c-149">Satz-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="a0b1c-149">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="a0b1c-150">Legt Autorisierungsregeln für einen Benachrichtigungs-Hub-Namespace fest.</span><span class="sxs-lookup"><span data-stu-id="a0b1c-150">Sets authorization rules for a notification hub namespace.</span></span>

