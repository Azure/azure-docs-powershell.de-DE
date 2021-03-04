---
title: Azure-Kontexte und -Anmeldeinformationen
description: Hier erfahren Sie, wie Sie Azure-Anmeldeinformationen und andere Informationen in mehreren PowerShell-Sitzungen wiederverwenden.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: be9113ab1ad6a359832634ae2c21fd177b09318f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101872308"
---
# <a name="azure-powershell-context-objects"></a><span data-ttu-id="441ff-103">Azure PowerShell-Kontextobjekte</span><span class="sxs-lookup"><span data-stu-id="441ff-103">Azure PowerShell context objects</span></span>

<span data-ttu-id="441ff-104">Azure PowerShell verwendet _Azure PowerShell-Kontextobjekte_ (Azure-Kontexte), um Abonnement- und Authentifizierungsinformationen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="441ff-104">Azure PowerShell uses _Azure PowerShell context objects_ (Azure contexts) to hold subscription and authentication information.</span></span> <span data-ttu-id="441ff-105">Besitzer mehrerer Abonnements können mithilfe von Azure-Kontexten das Abonnement auswählen, für das Azure PowerShell-Cmdlets ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="441ff-105">If you have more than one subscription, Azure contexts let you select the subscription to run Azure PowerShell cmdlets on.</span></span> <span data-ttu-id="441ff-106">Azure-Kontexte werden auch verwendet, um Anmeldeinformationen über mehrere PowerShell-Sitzungen hinweg zu speichern und Hintergrundaufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="441ff-106">Azure contexts are also used to store sign-in information across multiple PowerShell sessions and run background tasks.</span></span>

<span data-ttu-id="441ff-107">In diesem Artikel wird die Verwaltung von Azure-Kontexten behandelt, nicht die Verwaltung von Abonnements oder Konten.</span><span class="sxs-lookup"><span data-stu-id="441ff-107">This article covers managing Azure contexts, not the management of subscriptions or accounts.</span></span> <span data-ttu-id="441ff-108">Informationen zur Verwaltung von Benutzern, Abonnements, Mandanten und anderen Kontoinformationen finden Sie in der [Dokumentation zu Azure Active Directory](/azure/active-directory).</span><span class="sxs-lookup"><span data-stu-id="441ff-108">If you're looking to manage users, subscriptions, tenants, or other account information, see the [Azure Active Directory](/azure/active-directory) documentation.</span></span> <span data-ttu-id="441ff-109">Informationen zur Verwendung von Kontexten für die Ausführung von Hintergrundaufgaben oder parallelen Aufgaben finden Sie unter [Ausführen von Azure PowerShell-Cmdlets in PowerShell-Aufträgen](using-psjobs.md). Machen Sie sich jedoch zuvor mit Azure-Kontexten vertraut.</span><span class="sxs-lookup"><span data-stu-id="441ff-109">To learn about using contexts for running background or parallel tasks, see [Use Azure PowerShell cmdlets in PowerShell jobs](using-psjobs.md) after becoming familiar with Azure contexts.</span></span>

## <a name="overview-of-azure-context-objects"></a><span data-ttu-id="441ff-110">Übersicht über Azure-Kontextobjekte</span><span class="sxs-lookup"><span data-stu-id="441ff-110">Overview of Azure context objects</span></span>

<span data-ttu-id="441ff-111">Bei Azure-Kontexten handelt es sich um PowerShell-Objekte, die Ihr aktives Abonnement, für das Befehle ausgeführt werden sollen, sowie die Authentifizierungsinformationen darstellen, die zum Herstellen einer Verbindung mit einer Azure-Cloud erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="441ff-111">Azure contexts are PowerShell objects representing your active subscription to run commands against, and the authentication information needed to connect to an Azure cloud.</span></span> <span data-ttu-id="441ff-112">Mit Azure-Kontexten muss Azure PowerShell Ihr Konto nicht bei jedem Abonnementwechsel erneut authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="441ff-112">With Azure contexts, Azure PowerShell doesn't need to reauthenticate your account each time you switch subscriptions.</span></span> <span data-ttu-id="441ff-113">Ein Azure-Kontext umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="441ff-113">An Azure context consists of:</span></span>

* <span data-ttu-id="441ff-114">Das _Konto_, das für die Anmeldung bei Azure mit [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="441ff-114">The _account_ that was used to sign in to Azure with [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span></span> <span data-ttu-id="441ff-115">In Azure-Kontexten werden Benutzer, Anwendungs-IDs und Dienstprinzipale aus Kontosicht gleich behandelt.</span><span class="sxs-lookup"><span data-stu-id="441ff-115">Azure contexts treat users, application IDs, and service principals the same from an account perspective.</span></span>
* <span data-ttu-id="441ff-116">Das aktive _Abonnement_ – ein Servicevertrag mit Microsoft für die Erstellung und Ausführung von Azure-Ressourcen, die einem _Mandanten_ zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="441ff-116">The active _subscription_, a service agreement with Microsoft to create and run Azure resources, which are associated with a _tenant_.</span></span> <span data-ttu-id="441ff-117">Mandanten werden in der Dokumentation oder im Zusammenhang mit Active Directory häufig als _Organisationen_ bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="441ff-117">Tenants are often referred to as _organizations_ in documentation or when working with Active Directory.</span></span>
* <span data-ttu-id="441ff-118">Ein Verweis auf einen _Tokencache_ – ein gespeichertes Authentifizierungstoken für den Zugriff auf eine Azure-Cloud.</span><span class="sxs-lookup"><span data-stu-id="441ff-118">A reference to a _token cache_, a stored authentication token for accessing an Azure cloud.</span></span> <span data-ttu-id="441ff-119">Speicherort und Aufbewahrungsdauer dieses Tokens hängen von den [Einstellungen für die automatische Kontextspeicherung](#save-azure-contexts-across-powershell-sessions) ab.</span><span class="sxs-lookup"><span data-stu-id="441ff-119">Where this token is stored and how long it persists for is determined by the [context autosave settings](#save-azure-contexts-across-powershell-sessions).</span></span>

<span data-ttu-id="441ff-120">Weitere Informationen zu diesen Begriffen finden Sie [hier](/azure/active-directory/fundamentals/active-directory-whatis#terminology).</span><span class="sxs-lookup"><span data-stu-id="441ff-120">For more information on these terms, see [Azure Active Directory Terminology](/azure/active-directory/fundamentals/active-directory-whatis#terminology).</span></span> <span data-ttu-id="441ff-121">Von Azure-Kontexten verwendete Authentifizierungstoken unterscheiden sich nicht von anderen gespeicherten Token einer beständigen Sitzung.</span><span class="sxs-lookup"><span data-stu-id="441ff-121">Authentication tokens used by Azure contexts are the same as other stored tokens that are part of a persistent session.</span></span>

<span data-ttu-id="441ff-122">Wenn Sie sich mit `Connect-AzAccount` anmelden, wird mindestens ein Azure-Kontext für Ihr Standardabonnement erstellt.</span><span class="sxs-lookup"><span data-stu-id="441ff-122">When you sign in with `Connect-AzAccount`, at least one Azure context is created for your default subscription.</span></span> <span data-ttu-id="441ff-123">Bei dem von `Connect-AzAccount` zurückgegebenen Objekt handelt es sich um den Azure-Standardkontext, der für die restliche PowerShell-Sitzung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="441ff-123">The object returned by `Connect-AzAccount` is the default Azure context used for the rest of the PowerShell session.</span></span>

## <a name="get-azure-contexts"></a><span data-ttu-id="441ff-124">Abrufen von Azure-Kontexten</span><span class="sxs-lookup"><span data-stu-id="441ff-124">Get Azure contexts</span></span>

<span data-ttu-id="441ff-125">Verfügbare Azure-Kontexte werden mithilfe des Cmdlets [Get-AzContext](/powershell/module/az.accounts/get-azcontext) abgerufen.</span><span class="sxs-lookup"><span data-stu-id="441ff-125">Available Azure contexts are retrieved with the [Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet.</span></span> <span data-ttu-id="441ff-126">Verwenden Sie `-ListAvailable`, um alle verfügbaren Kontexte aufzulisten:</span><span class="sxs-lookup"><span data-stu-id="441ff-126">List all of the available contexts with `-ListAvailable`:</span></span>

```azurepowershell-interactive
Get-AzContext -ListAvailable
```

<span data-ttu-id="441ff-127">Oder rufen Sie einen Kontext anhand des Namens ab:</span><span class="sxs-lookup"><span data-stu-id="441ff-127">Or get a context by name:</span></span>

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
```

<span data-ttu-id="441ff-128">Kontextnamen können sich vom Namen des zugeordneten Abonnements unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="441ff-128">Context names may be different from the name of the associated subscription.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="441ff-129">Bei den verfügbaren Azure-Kontexten handelt es sich __nicht__ immer um Ihre verfügbaren Abonnements.</span><span class="sxs-lookup"><span data-stu-id="441ff-129">The available Azure contexts __aren't__ always your available subscriptions.</span></span> <span data-ttu-id="441ff-130">Azure-Kontexte stellen nur lokal gespeicherte Informationen dar.</span><span class="sxs-lookup"><span data-stu-id="441ff-130">Azure contexts only represent locally-stored information.</span></span> <span data-ttu-id="441ff-131">Ihre Abonnements können Sie mithilfe des Cmdlets [Get-AzSubscription](/powershell/module/Az.Accounts/Get-AzSubscription) abrufen.</span><span class="sxs-lookup"><span data-stu-id="441ff-131">You can get your subscriptions with the [Get-AzSubscription](/powershell/module/Az.Accounts/Get-AzSubscription) cmdlet.</span></span>

## <a name="create-a-new-azure-context-from-subscription-information"></a><span data-ttu-id="441ff-132">Erstellen eines neuen Azure-Kontexts auf der Grundlage von Abonnementinformationen</span><span class="sxs-lookup"><span data-stu-id="441ff-132">Create a new Azure context from subscription information</span></span>

<span data-ttu-id="441ff-133">Mit dem Cmdlet [Set-AzContext](/powershell/module/Az.Accounts/Set-AzContext) können Sie neue Azure-Kontexte erstellen und sie als aktiven Kontext festlegen.</span><span class="sxs-lookup"><span data-stu-id="441ff-133">The [Set-AzContext](/powershell/module/Az.Accounts/Set-AzContext) cmdlet is used to both create new Azure contexts and set them as the active context.</span></span>
<span data-ttu-id="441ff-134">Am einfachsten lässt sich ein neuer Azure-Kontext auf der Grundlage vorhandener Abonnementinformationen erstellen.</span><span class="sxs-lookup"><span data-stu-id="441ff-134">The easiest way to create a new Azure context is to use existing subscription information.</span></span> <span data-ttu-id="441ff-135">Das Cmdlet akzeptiert das Ausgabeobjekt von `Get-AzSubscription` als weitergeleiteten Wert und konfiguriert einen neuen Azure-Kontext:</span><span class="sxs-lookup"><span data-stu-id="441ff-135">The cmdlet is designed to take the output object from `Get-AzSubscription` as a piped value and configure a new Azure context:</span></span>

```azurepowershell-interactive
Get-AzSubscription -SubscriptionName 'MySubscriptionName' | Set-AzContext -Name 'MyContextName'
```

<span data-ttu-id="441ff-136">Bei Bedarf können alternativ auch der Name oder die ID des Abonnements und die Mandanten-ID angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="441ff-136">Or give the subscription name or ID and the tenant ID if necessary:</span></span>

```azurepowershell-interactive
Set-AzContext -Name 'MyContextName' -Subscription 'MySubscriptionName' -Tenant '.......'
```

<span data-ttu-id="441ff-137">Ohne Angabe des Arguments `-Name` werden Name und ID des Abonnements als Kontextname im Format `Subscription Name (subscription-id)` verwendet.</span><span class="sxs-lookup"><span data-stu-id="441ff-137">If the `-Name` argument is omitted, then the subscription's name and ID are used as the context name in the format `Subscription Name (subscription-id)`.</span></span>

## <a name="change-the-active-azure-context"></a><span data-ttu-id="441ff-138">Ändern des aktiven Azure-Kontexts</span><span class="sxs-lookup"><span data-stu-id="441ff-138">Change the active Azure context</span></span>

<span data-ttu-id="441ff-139">Der aktive Azure-Kontext kann sowohl mit `Set-AzContext` als auch mit [Select-AzContext](/powershell/module/az.accounts/set-azcontext) geändert werden.</span><span class="sxs-lookup"><span data-stu-id="441ff-139">Both `Set-AzContext` and [Select-AzContext](/powershell/module/az.accounts/set-azcontext) can be used to change the active Azure context.</span></span> <span data-ttu-id="441ff-140">`Set-AzContext` erstellt wie unter [Erstellen eines neuen Azure-Kontexts auf der Grundlage von Abonnementinformationen](#create-a-new-azure-context-from-subscription-information) beschrieben einen neuen Azure-Kontext für ein Abonnement, sofern noch keiner vorhanden ist, und verwendet diesen dann als aktiven Kontext.</span><span class="sxs-lookup"><span data-stu-id="441ff-140">As described in [Create a new Azure context](#create-a-new-azure-context-from-subscription-information), `Set-AzContext` creates a new Azure context for a subscription if one doesn't exist, and then switches to use that context as the active one.</span></span>

<span data-ttu-id="441ff-141">`Select-AzContext` ist nur für die Verwendung mit vorhandenen Azure-Kontexten vorgesehen und funktioniert ähnlich wie `Set-AzContext -Context`, ist aber für die Verwendung mit Piping konzipiert:</span><span class="sxs-lookup"><span data-stu-id="441ff-141">`Select-AzContext` is meant to be used with existing Azure contexts only and works similarly to using `Set-AzContext -Context`, but is designed for use with piping:</span></span>

```azurepowershell-interactive
Set-AzContext -Context $(Get-AzContext -Name "mycontext") # Set a context with an inline Azure context object
Get-AzContext -Name "mycontext" | Select-AzContext # Set a context with a piped Azure context object
```

<span data-ttu-id="441ff-142">Genau wie viele andere Konto- und Kontextverwaltungsbefehle in Azure PowerShell unterstützen auch `Set-AzContext` und `Select-AzContext` das Argument `-Scope` zum Steuern der Aktivitätsdauer des Kontexts.</span><span class="sxs-lookup"><span data-stu-id="441ff-142">Like many other account and context management commands in Azure PowerShell, `Set-AzContext` and `Select-AzContext` support the `-Scope` argument so that you can control how long the context is active.</span></span> <span data-ttu-id="441ff-143">Mithilfe von `-Scope` können Sie den aktiven Kontext einer einzelnen Sitzung ändern, ohne den Standardkontext zu ändern:</span><span class="sxs-lookup"><span data-stu-id="441ff-143">`-Scope` lets you change a single session's active context without changing the default:</span></span>

```azurepowershell-interactive
Get-AzContext -Name "mycontext" | Select-AzContext -Scope Process
```

<span data-ttu-id="441ff-144">Zur Vermeidung des Kontextwechsels für eine gesamte PowerShell-Sitzung können alle Azure PowerShell-Befehle mithilfe des Arguments `-AzContext` für einen bestimmten Kontext ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="441ff-144">To avoid switching contexts for a whole PowerShell session, all Azure PowerShell commands can be run against a given context with the `-AzContext` argument:</span></span>

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
New-AzVM -Name ExampleVM -AzContext $context
```

<span data-ttu-id="441ff-145">Der andere Hauptzweck von Kontexten mit Azure PowerShell-Cmdlets ist das Ausführen von Hintergrundbefehlen.</span><span class="sxs-lookup"><span data-stu-id="441ff-145">The other main use of contexts with Azure PowerShell cmdlets is to run background commands.</span></span> <span data-ttu-id="441ff-146">Weitere Informationen zum Ausführen von PowerShell-Aufträgen mit Azure PowerShell finden Sie unter [Ausführen von Azure PowerShell-Cmdlets in PowerShell-Aufträgen](using-psjobs.md).</span><span class="sxs-lookup"><span data-stu-id="441ff-146">To learn more about running PowerShell Jobs using Azure PowerShell, see [Run Azure PowerShell cmdlets in PowerShell Jobs](using-psjobs.md).</span></span>

## <a name="save-azure-contexts-across-powershell-sessions"></a><span data-ttu-id="441ff-147">Speichern von Azure-Kontexten zwischen PowerShell-Sitzungen</span><span class="sxs-lookup"><span data-stu-id="441ff-147">Save Azure contexts across PowerShell sessions</span></span>

<span data-ttu-id="441ff-148">Azure-Kontexte werden standardmäßig für die Verwendung zwischen PowerShell-Sitzungen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="441ff-148">By default, Azure contexts are saved for use between PowerShell sessions.</span></span> <span data-ttu-id="441ff-149">Dieses Verhalten kann wie folgt geändert werden:</span><span class="sxs-lookup"><span data-stu-id="441ff-149">You change this behavior in the following ways:</span></span>

* <span data-ttu-id="441ff-150">Melden Sie sich mithilfe von `Connect-AzAccount` unter Verwendung von `-Scope Process` an.</span><span class="sxs-lookup"><span data-stu-id="441ff-150">Sign in using `-Scope Process` with `Connect-AzAccount`.</span></span>

  ```azurepowershell
  Connect-AzAccount -Scope Process
  ```

  <span data-ttu-id="441ff-151">Der im Rahmen dieser Anmeldung zurückgegebene Azure-Kontext ist _ausschließlich_ für die aktuelle Sitzung gültig und wird unabhängig von der Einstellung für die automatische Azure PowerShell-Kontextspeicherung nicht automatisch gespeichert.</span><span class="sxs-lookup"><span data-stu-id="441ff-151">The Azure context returned as part of this sign in is valid for the current session _only_ and will not be automatically saved, regardless of the Azure PowerShell context autosave setting.</span></span>
* <span data-ttu-id="441ff-152">Die automatische Kontextspeicherung von Azure PowerShell kann mithilfe des Cmdlets [Disable-AzContextAutosave](/powershell/module/az.accounts/disable-azcontextautosave) deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="441ff-152">Disable AzurePowershell's context autosave with the [Disable-AzContextAutosave](/powershell/module/az.accounts/disable-azcontextautosave) cmdlet.</span></span>
  <span data-ttu-id="441ff-153">Gespeicherte Token werden durch die Deaktivierung der automatischen Kontextspeicherung __nicht__ gelöscht.</span><span class="sxs-lookup"><span data-stu-id="441ff-153">Disabling context autosave __doesn't__ clear any stored tokens.</span></span> <span data-ttu-id="441ff-154">Informationen zum Löschen gespeicherter Azure-Kontextinformationen finden Sie unter [Entfernen von Azure-Kontexten und gespeicherten Anmeldeinformationen](#remove-azure-contexts-and-stored-credentials).</span><span class="sxs-lookup"><span data-stu-id="441ff-154">To learn how to clear stored Azure context information, see [Remove Azure contexts and credentials](#remove-azure-contexts-and-stored-credentials).</span></span>
* <span data-ttu-id="441ff-155">Die automatische Speicherung von Azure-Kontexten kann mithilfe des Cmdlets [Enable-AzContextAutosave](/powershell/module/az.accounts/enable-azcontextautosave) explizit aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="441ff-155">Explicitly enable Azure context autosave can be enabled with the [Enable-AzContextAutosave](/powershell/module/az.accounts/enable-azcontextautosave) cmdlet.</span></span> <span data-ttu-id="441ff-156">Bei aktivierter automatischer Speicherung werden alle Kontexte eines Benutzers lokal für spätere PowerShell-Sitzungen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="441ff-156">With autosave enabled, all of a user's contexts are stored locally for later PowerShell sessions.</span></span>
* <span data-ttu-id="441ff-157">Mithilfe von [Save-AzContext](/powershell/module/az.accounts/save-azcontext) können Kontexte manuell gespeichert und mithilfe von [Import-AzContext](/powershell/module/az.accounts/import-azcontext) in späteren PowerShell-Sitzungen geladen werden:</span><span class="sxs-lookup"><span data-stu-id="441ff-157">Manually save contexts with [Save-AzContext](/powershell/module/az.accounts/save-azcontext) to be used in future PowerShell sessions, where they can be loaded with [Import-AzContext](/powershell/module/az.accounts/import-azcontext):</span></span>

  ```azurepowershell
  Save-AzContext -Path current-context.json # Save the current context
  Save-AzContext -Profile $profileObject -Path other-context.json # Save a context object
  Import-AzContext -Path other-context.json # Load the context from a file and set it to the current context
  ```

> [!WARNING]
> <span data-ttu-id="441ff-158">Wenn Sie die automatische Kontextspeicherung deaktivieren, werden __keine__ gespeicherten Kontextinformationen gelöscht.</span><span class="sxs-lookup"><span data-stu-id="441ff-158">Disabling context autosave __doesn't__ clear any stored context information that was saved.</span></span> <span data-ttu-id="441ff-159">Zum Entfernen gespeicherter Informationen muss das Cmdlet [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="441ff-159">To remove stored information, use the [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext) cmdlet.</span></span> <span data-ttu-id="441ff-160">Weitere Informationen zum Entfernen gespeicherter Kontexte finden Sie unter [Entfernen von Azure-Kontexten und gespeicherten Anmeldeinformationen](#remove-azure-contexts-and-stored-credentials).</span><span class="sxs-lookup"><span data-stu-id="441ff-160">For more on removing saved contexts, see [Remove contexts and credentials](#remove-azure-contexts-and-stored-credentials).</span></span>

<span data-ttu-id="441ff-161">Jeder dieser Befehle unterstützt den Parameter `-Scope`. Dieser kann auf den Wert `Process` festgelegt werden, damit der Befehl nur für den aktuell ausgeführten Prozess gilt.</span><span class="sxs-lookup"><span data-stu-id="441ff-161">Each of these commands supports the `-Scope` parameter, which can take a value of `Process` to only apply to the current running process.</span></span> <span data-ttu-id="441ff-162">Wenn Sie also beispielsweise sicherstellen möchten, dass neu erstellte Kontexte nach dem Verlassen einer PowerShell-Sitzung nicht gespeichert werden, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="441ff-162">For example, to ensure that newly created contexts aren't saved after exiting a PowerShell session:</span></span>

```azurepowershell-interactive
Disable-AzContextAutosave -Scope Process
$context2 = Set-AzContext -Subscription "sub-id" -Tenant "other-tenant"
```

<span data-ttu-id="441ff-163">Kontextinformationen und Token werden unter Windows im Verzeichnis `$env:USERPROFILE\.Azure` und auf anderen Plattformen unter `$HOME/.Azure` gespeichert.</span><span class="sxs-lookup"><span data-stu-id="441ff-163">Context information and tokens are stored in the `$env:USERPROFILE\.Azure` directory on Windows, and on `$HOME/.Azure` on other platforms.</span></span> <span data-ttu-id="441ff-164">Es kann vorkommen, dass sensible Informationen wie Abonnement- und Mandanten-IDs in gespeicherten Informationen über Protokolle oder gespeicherte Kontexte offengelegt werden.</span><span class="sxs-lookup"><span data-stu-id="441ff-164">Sensitive information such as subscription IDs and tenant IDs may still be exposed in stored information, through logs or saved contexts.</span></span> <span data-ttu-id="441ff-165">Informationen zum Löschen gespeicherter Informationen finden Sie im Abschnitt [Entfernen von Azure-Kontexten und gespeicherten Anmeldeinformationen](#remove-azure-contexts-and-stored-credentials).</span><span class="sxs-lookup"><span data-stu-id="441ff-165">To learn how to clear stored information, see the [Remove contexts and credentials](#remove-azure-contexts-and-stored-credentials) section.</span></span>

## <a name="remove-azure-contexts-and-stored-credentials"></a><span data-ttu-id="441ff-166">Entfernen von Azure-Kontexten und gespeicherten Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="441ff-166">Remove Azure contexts and stored credentials</span></span>

<span data-ttu-id="441ff-167">So löschen Sie Azure-Kontexte und -Anmeldeinformationen:</span><span class="sxs-lookup"><span data-stu-id="441ff-167">To clear Azure contexts and credentials:</span></span>

* <span data-ttu-id="441ff-168">Melden Sie sich mithilfe von [Disconnect-AzAccount](/powershell/module/az.accounts/disconnect-azaccount) von einem Konto ab.</span><span class="sxs-lookup"><span data-stu-id="441ff-168">Sign out of an account with [Disconnect-AzAccount](/powershell/module/az.accounts/disconnect-azaccount).</span></span>
  <span data-ttu-id="441ff-169">Zur Abmeldung können Sie entweder das Konto oder den Kontext verwenden:</span><span class="sxs-lookup"><span data-stu-id="441ff-169">You can sign out of any account either by account or context:</span></span>

  ```azurepowershell-interactive
  Disconnect-AzAccount # Disconnect active account
  Disconnect-AzAccount -Username "user@contoso.com" # Disconnect by account name

  Disconnect-AzAccount -ContextName "subscription2" # Disconnect by context name
  Disconnect-AzAccount -AzureContext $contextObject # Disconnect using context object information
  ```

  <span data-ttu-id="441ff-170">Beim Trennen der Verbindung werden gespeicherte Authentifizierungstoken entfernt und gespeicherte Kontexte gelöscht, die dem getrennten Benutzer oder Kontext zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="441ff-170">Disconnecting always removes stored authentication tokens and clears saved contexts associated with the disconnected user or context.</span></span>
* <span data-ttu-id="441ff-171">Verwenden Sie [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext).</span><span class="sxs-lookup"><span data-stu-id="441ff-171">Use [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext).</span></span> <span data-ttu-id="441ff-172">Dieses Cmdlet entfernt zuverlässig gespeicherte Kontexte und Authentifizierungstoken und meldet Sie außerdem ab.</span><span class="sxs-lookup"><span data-stu-id="441ff-172">This cmdlet is guaranteed to always remove stored contexts and authentication tokens, and will also sign you out.</span></span>
* <span data-ttu-id="441ff-173">Verwenden Sie zum Entfernen eines Kontexts das Cmdlet [Remove-AzContext](/powershell/module/az.accounts/remove-azcontext):</span><span class="sxs-lookup"><span data-stu-id="441ff-173">Remove a context with [Remove-AzContext](/powershell/module/az.accounts/remove-azcontext):</span></span>

  ```azurepowershell-interactive
  Remove-AzContext -Name "mycontext" # Remove by name
  Get-AzContext -Name "mycontext" | Remove-AzContext # Remove by piping Azure context object
  ```

  <span data-ttu-id="441ff-174">Wenn Sie den aktiven Kontext entfernen, wird die Verbindung mit Azure getrennt, und Sie müssen sich mithilfe von `Connect-AzAccount` erneut authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="441ff-174">If you remove the active context, you will be disconnected from Azure and need to reauthenticate with `Connect-AzAccount`.</span></span>

## <a name="see-also"></a><span data-ttu-id="441ff-175">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="441ff-175">See also</span></span>

* [<span data-ttu-id="441ff-176">Ausführen von Azure PowerShell-Cmdlets in PowerShell-Aufträgen</span><span class="sxs-lookup"><span data-stu-id="441ff-176">Run Azure PowerShell cmdlets in PowerShell Jobs</span></span>](using-psjobs.md)
* [<span data-ttu-id="441ff-177">Azure Active Directory-Terminologie</span><span class="sxs-lookup"><span data-stu-id="441ff-177">Azure Active Directory Terminology</span></span>](/azure/active-directory/fundamentals/active-directory-whatis#terminology)
* [<span data-ttu-id="441ff-178">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="441ff-178">Az.Accounts reference</span></span>](/powershell/module/az.accounts)
