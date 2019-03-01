---
title: Verwalten von Azure-Abonnements mit Azure PowerShell
description: Verwalten von Azure-Abonnements mit Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/04/2019
ms.openlocfilehash: 29d7c84d0ca9ae8d3e4e22f407b007d2d582f8bc
ms.sourcegitcommit: 5630030c5cfa9828c3c024b69de59248263ef17f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "56837638"
---
# <a name="use-multiple-azure-subscriptions"></a><span data-ttu-id="44f20-103">Verwenden mehrerer Azure-Abonnements</span><span class="sxs-lookup"><span data-stu-id="44f20-103">Use multiple Azure subscriptions</span></span>

<span data-ttu-id="44f20-104">Die meisten Azure-Benutzer verwenden nur ein einzelnes Abonnement.</span><span class="sxs-lookup"><span data-stu-id="44f20-104">Most Azure users will only ever have a single subscription.</span></span> <span data-ttu-id="44f20-105">Wenn Sie allerdings mehreren Organisationen angehören oder Ihre Organisation den Zugriff auf bestimmte Ressourcen über Gruppierungen aufgeteilt hat, besitzen Sie möglicherweise mehrere Abonnements in Azure.</span><span class="sxs-lookup"><span data-stu-id="44f20-105">However, if you are part of more than one organization or your organization has divided up access to certain resources across groupings, you may have multiple subscriptions within Azure.</span></span> <span data-ttu-id="44f20-106">Die CLI unterstützt sowohl die globale Auswahl eines Abonnements als auch die Auswahl per Befehl.</span><span class="sxs-lookup"><span data-stu-id="44f20-106">The CLI supports selecting a subscription both globally and per command.</span></span>

## <a name="tenants-users-and-subscriptions"></a><span data-ttu-id="44f20-107">Mandanten, Benutzer und Abonnements</span><span class="sxs-lookup"><span data-stu-id="44f20-107">Tenants, users, and subscriptions</span></span>

<span data-ttu-id="44f20-108">Möglicherweise sind Sie sich nicht ganz über den Unterschied zwischen Mandanten, Benutzern und Abonnements in Azure im Klaren.</span><span class="sxs-lookup"><span data-stu-id="44f20-108">You might have some confusion over the difference between tenants, users, and subscriptions within Azure.</span></span> <span data-ttu-id="44f20-109">Ein _Mandant_ ist die Azure Active Directory-Entität, die eine gesamte Organisation umfasst.</span><span class="sxs-lookup"><span data-stu-id="44f20-109">A _tenant_ is the Azure Active Directory entity that encompasses a whole organization.</span></span> <span data-ttu-id="44f20-110">Dieser Mandant hat mindestens ein _Abonnement_ und einen _Benutzer_.</span><span class="sxs-lookup"><span data-stu-id="44f20-110">This tenant has at least one _subscription_ and _user_.</span></span> <span data-ttu-id="44f20-111">Ein Benutzer ist eine Person und nur einem einzelnen Mandanten zugeordnet: der Organisation, der er angehört.</span><span class="sxs-lookup"><span data-stu-id="44f20-111">A user is an individual and is associated with only one tenant, the organization that they belong to.</span></span> <span data-ttu-id="44f20-112">Benutzer sind Konten, die sich bei Azure anmelden, um Ressourcen zu erstellen, zu verwalten und zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="44f20-112">Users are those accounts that sign in to Azure to create, manage, and use resources.</span></span>
<span data-ttu-id="44f20-113">Ein Benutzer hat möglicherweise Zugriff auf mehrere _Abonnements_. Hierbei handelt es sich um die Vereinbarungen mit Microsoft, die die Verwendung von Clouddiensten wie Azure regeln.</span><span class="sxs-lookup"><span data-stu-id="44f20-113">A user may have access to multiple _subscriptions_, which are the agreements with Microsoft to use cloud services, including Azure.</span></span> <span data-ttu-id="44f20-114">Jede Ressource ist einem Abonnement zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="44f20-114">Every resource is associated with a subscription.</span></span>

<span data-ttu-id="44f20-115">Weitere Informationen zu den Unterschieden zwischen Mandanten, Benutzern und Abonnements finden Sie im [Microsoft Azure-Glossar](/azure/azure-glossary-cloud-terminology).</span><span class="sxs-lookup"><span data-stu-id="44f20-115">To learn more about the differences between tenants, users, and subscriptions, see the [Azure cloud terminology dictionary](/azure/azure-glossary-cloud-terminology).</span></span>  <span data-ttu-id="44f20-116">Informationen zum Hinzufügen eines neuen Abonnements zu Ihrem Azure Active Directory-Mandanten finden Sie unter [Hinzufügen eines Azure-Abonnements zu Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory).</span><span class="sxs-lookup"><span data-stu-id="44f20-116">To learn how to add a new subscription to your Azure Active Directory tenant, see [How to add an Azure subscription to Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory).</span></span>
<span data-ttu-id="44f20-117">Informationen zum Anmelden bei einem bestimmten Mandanten finden Sie unter [Anmelden mit Azure PowerShell](/powershell/azure/authenticate-azureps).</span><span class="sxs-lookup"><span data-stu-id="44f20-117">To learn how to sign in to a specific tenant, see [Sign in with Azure PowerShell](/powershell/azure/authenticate-azureps).</span></span>

## <a name="change-the-active-subscription"></a><span data-ttu-id="44f20-118">Ändern des aktiven Abonnements</span><span class="sxs-lookup"><span data-stu-id="44f20-118">Change the active subscription</span></span>

<span data-ttu-id="44f20-119">In Azure PowerShell ist für den Zugriff auf die Ressourcen für ein Abonnement eine Änderung des Abonnements erforderlich, das Ihrer aktuellen Azure-Sitzung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="44f20-119">In Azure PowerShell, accessing the resources for a subscription requires changing the subscription associated with your current Azure session.</span></span>
<span data-ttu-id="44f20-120">Hierfür wird der Kontext der aktiven Sitzung geändert. Dies sind die Informationen dazu, welcher Mandant, welches Abonnement und welche Benutzer-Cmdlets für die Ausführung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="44f20-120">This is done by modifying the active session context, the information about which tenant, subscription, and user cmdlets should be run against.</span></span>
<span data-ttu-id="44f20-121">Zum Ändern von Abonnements muss zuerst mit [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) ein Azure PowerShell-Kontextobjekt abgerufen und anschließend der aktuelle Kontext mit [Set-AzContext](/powershell/module/az.accounts/set-azcontext) geändert werden.</span><span class="sxs-lookup"><span data-stu-id="44f20-121">In order to change subscriptions, an Azure PowerShell Context object first needs to be retrieved with [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) and then the current context changed with [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span></span>

<span data-ttu-id="44f20-122">Im nächsten Beispiel wird veranschaulicht, wie Sie ein Abonnement im derzeit aktiven Mandanten abrufen und als aktive Sitzung festlegen:</span><span class="sxs-lookup"><span data-stu-id="44f20-122">The next example shows how to get a subscription in the currently active tenant, and set it as the active session:</span></span>

```powershell-interactive
$context = Get-AzSubscription -SubscriptionId ...
Set-AzContext $context
```

<span data-ttu-id="44f20-123">Weitere Informationen zu Azure PowerShell-Kontexten, z. B. zum Durchführen von Speichervorgängen und schnellen Wechseln zwischen Kontexten, um die Nutzung mehrerer Abonnements zu vereinfachen, finden Sie unter [Speichern von Benutzeranmeldeinformationen zwischen PowerShell-Sitzungen](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="44f20-123">To learn more about Azure PowerShell contexts, including how to save them and quickly switch between them for working with multiple subscriptions easily, see [Persist credentials with Azure PowerShell contexts](context-persistence.md).</span></span>
