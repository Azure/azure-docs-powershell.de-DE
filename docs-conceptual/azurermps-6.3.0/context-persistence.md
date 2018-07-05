---
title: Speichern von Benutzeranmeldeinformationen zwischen PowerShell-Sitzungen
description: Hier erfahren Sie, wie Sie Azure-Anmeldeinformationen und andere Informationen in mehreren PowerShell-Sitzungen wiederverwenden.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/31/2017
ms.openlocfilehash: aa374c6e93124fb4b428aa8c4854f7424f494bff
ms.sourcegitcommit: 4c775721461210431bd913f28d1f1e6f1976880a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/28/2018
ms.locfileid: "37091349"
---
# <a name="persisting-user-credentials-across-powershell-sessions"></a><span data-ttu-id="5f0f2-103">Speichern von Benutzeranmeldeinformationen zwischen PowerShell-Sitzungen</span><span class="sxs-lookup"><span data-stu-id="5f0f2-103">Persisting user credentials across PowerShell sessions</span></span>

<span data-ttu-id="5f0f2-104">In der Azure PowerShell-Version vom September 2017 wird für Azure Resource Manager-Cmdlets ein neues Feature eingeführt: die **automatische Speicherung des Azure-Kontexts**.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-104">In the September 2017 release of Azure PowerShell, Azure Resource Manager cmdlets introduce a new feature, **Azure Context Autosave**.</span></span> <span data-ttu-id="5f0f2-105">Dieses Feature kann beispielsweise für folgende neue Benutzerszenarien verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="5f0f2-105">This feature enables several new user scenarios, including:</span></span>

- <span data-ttu-id="5f0f2-106">Speicherung von Anmeldeinformationen zur Wiederverwendung in neuen PowerShell-Sitzungen</span><span class="sxs-lookup"><span data-stu-id="5f0f2-106">Retention of login information for reuse in new PowerShell sessions.</span></span>
- <span data-ttu-id="5f0f2-107">Einfachere Verwendung von Hintergrundaufgaben für die Ausführung von Cmdlets mit langer Ausführungszeit</span><span class="sxs-lookup"><span data-stu-id="5f0f2-107">Easier use of background tasks for executing long-running cmdlets.</span></span>
- <span data-ttu-id="5f0f2-108">Wechsel zwischen Konten, Abonnements und Umgebungen ohne separate Anmeldung</span><span class="sxs-lookup"><span data-stu-id="5f0f2-108">Switch between accounts, subscriptions, and environments without a separate login.</span></span>
- <span data-ttu-id="5f0f2-109">Gleichzeitige Ausführung von Aufgaben mit unterschiedlichen Anmeldeinformationen und Abonnements über die gleiche PowerShell-Sitzung</span><span class="sxs-lookup"><span data-stu-id="5f0f2-109">Execution of tasks using different credentials and subscriptions, simultaneously, from the same PowerShell session.</span></span>

## <a name="azure-contexts-defined"></a><span data-ttu-id="5f0f2-110">Definition von Azure-Kontexten</span><span class="sxs-lookup"><span data-stu-id="5f0f2-110">Azure contexts defined</span></span>

<span data-ttu-id="5f0f2-111">Bei einem *Azure-Kontext* handelt es sich um einen Satz von Informationen, die das Ziel von Azure PowerShell-Cmdlets definieren.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-111">An *Azure context* is a set of information that defines the target of Azure PowerShell cmdlets.</span></span> <span data-ttu-id="5f0f2-112">Der Kontext setzt sich aus fünf Teilen zusammen:</span><span class="sxs-lookup"><span data-stu-id="5f0f2-112">The context consists of five parts:</span></span>

- <span data-ttu-id="5f0f2-113">Ein *Konto*: Der Benutzername oder Dienstprinzipal, der verwendet wird, um die Kommunikation mit Azure zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-113">An *Account* - the UserName or Service Principal used to authenticate communications with Azure</span></span>
- <span data-ttu-id="5f0f2-114">Ein *Abonnement*: Das Azure-Abonnement mit den Ressourcen, für die eine Aktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-114">A *Subscription* - The Azure Subscription containing the Resources being acted upon.</span></span>
- <span data-ttu-id="5f0f2-115">Ein *Mandant*: Der Azure Active Directory-Mandant mit Ihrem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-115">A *Tenant* - The Azure Active Directory tenant that contains your subscription.</span></span> <span data-ttu-id="5f0f2-116">Mandanten sind eher für die Dienstprinzipalauthentifizierung relevant.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-116">Tenants are more important to ServicePrincipal authentication.</span></span>
- <span data-ttu-id="5f0f2-117">Eine *Umgebung*: Die spezielle Azure-Cloud, die als Ziel fungiert (in der Regel die globale Azure-Cloud).</span><span class="sxs-lookup"><span data-stu-id="5f0f2-117">An *Environment* - The particular Azure Cloud being targeted, usually the Azure global Cloud.</span></span>
  <span data-ttu-id="5f0f2-118">Über die Umgebungseinstellung können Sie jedoch auch nationale Clouds, Government Clouds und lokale Clouds (Azure Stack) als Ziel festlegen.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-118">However, the environment setting allows you to target National, Government, and on-premises (Azure Stack) clouds as well.</span></span>
- <span data-ttu-id="5f0f2-119">*Anmeldeinformationen*: Die Informationen, die von Azure verwendet werden, um Ihre Identität zu überprüfen und die Autorisierung des Zugriffs auf Ressourcen in Azure zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-119">*Credentials* - The information used by Azure to verify your identity and ensure your authorization to access resources in Azure</span></span>

<span data-ttu-id="5f0f2-120">In früheren Versionen musste der Azure-Kontext bei jedem Öffnen einer neuen PowerShell-Sitzung erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-120">In previous releases, your Azure Context had to be created each time you opened a new PowerShell session.</span></span> <span data-ttu-id="5f0f2-121">Ab Azure PowerShell 4.4.0 können Sie die automatische Speicherung und Wiederverwendung von Azure-Kontexten beim Öffnen einer neuen PowerShell-Sitzung aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-121">Beginning with Azure PowerShell v4.4.0, you can enable the automatic saving and reuse of Azure Contexts whenever you open a new PowerShell session.</span></span>

## <a name="automatically-saving-the-context-for-the-next-login"></a><span data-ttu-id="5f0f2-122">Automatisches Speichern des Kontexts für die nächste Anmeldung</span><span class="sxs-lookup"><span data-stu-id="5f0f2-122">Automatically saving the context for the next login</span></span>

<span data-ttu-id="5f0f2-123">Standardmäßig verwirft Azure PowerShell Ihre Kontextinformationen, sobald Sie die PowerShell-Sitzung beenden.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-123">By default, Azure PowerShell discards your context information whenever you close the PowerShell session.</span></span>

<span data-ttu-id="5f0f2-124">Mit `Enable-AzureRmContextAutosave` können Sie es Azure PowerShell ermöglichen, den Kontext über das Sitzungsende hinaus zu speichern.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-124">To allow Azure PowerShell to remember your context after the PowerShell session is closed, use `Enable-AzureRmContextAutosave`.</span></span> <span data-ttu-id="5f0f2-125">Kontext und Anmeldeinformationen werden automatisch in einem speziellen ausgeblendeten Ordner in Ihrem Benutzerverzeichnis (`%AppData%\Roaming\Windows Azure PowerShell`) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-125">Context and credential information are automatically saved in a special hidden folder in your user directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span>
<span data-ttu-id="5f0f2-126">Anschließend verwendet jede neue PowerShell-Sitzung den Kontext aus Ihrer letzten Sitzung als Ziel.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-126">Subsequently, each new PowerShell session targets the context used in your last session.</span></span>

<span data-ttu-id="5f0f2-127">Wenn PowerShell den Kontext und die Anmeldeinformationen verwerfen soll, verwenden Sie `Disable-AzureRmContextAutoSave`.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-127">To set PowerShell to forget your context and credentials, use `Disable-AzureRmContextAutoSave`.</span></span> <span data-ttu-id="5f0f2-128">Daraufhin müssen Sie sich jedes Mal anmelden, wenn Sie eine PowerShell-Sitzung öffnen.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-128">You will need to log in to Azure every time you open a PowerShell session.</span></span>

<span data-ttu-id="5f0f2-129">Die Cmdlets zum Verwalten von Azure-Kontexten ermöglichen eine präzise Steuerung.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-129">The cmdlets that allow you to manage Azure contexts also allow you fine grained control.</span></span> <span data-ttu-id="5f0f2-130">So können Sie festlegen, ob Änderungen nur für die aktuelle PowerShell-Sitzung (`Process`-Bereich) oder für jede PowerShell-Sitzung (`CurrentUser`-Bereich) gelten sollen.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-130">If you want changes to apply only to the current PowerShell session (`Process` scope) or every PowerShell session (`CurrentUser` scope).</span></span> <span data-ttu-id="5f0f2-131">Ausführlichere Informationen zu diesen Optionen finden Sie unter [Verwenden von Kontextbereichen](#Using-Context-Scopes).</span><span class="sxs-lookup"><span data-stu-id="5f0f2-131">These options are discussed in mode detail in [Using Context Scopes](#Using-Context-Scopes).</span></span>

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a><span data-ttu-id="5f0f2-132">Ausführen von Azure PowerShell-Cmdlets als Hintergrundaufträge</span><span class="sxs-lookup"><span data-stu-id="5f0f2-132">Running Azure PowerShell cmdlets as background jobs</span></span>

<span data-ttu-id="5f0f2-133">Dank der**automatischen Speicherung des Azure-Kontexts** können Sie Ihren Kontext auch für PowerShell-Hintergrundaufträge freigeben.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-133">The **Azure Context Autosave** feature also allows you to share you context with PowerShell background jobs.</span></span> <span data-ttu-id="5f0f2-134">Mit PowerShell können Sie Aufgaben mit langer Ausführungszeit als Hintergrundaufträge starten und überwachen, ohne auf den Abschluss der Aufgaben warten zu müssen.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-134">PowerShell allows you to start and monitor long-executing tasks as background jobs without having to wait for the tasks to complete.</span></span> <span data-ttu-id="5f0f2-135">Sie können Anmeldeinformationen auf zwei Arten an Hintergrundaufträge weitergeben:</span><span class="sxs-lookup"><span data-stu-id="5f0f2-135">You can share credentials with background jobs in two different ways:</span></span>

- <span data-ttu-id="5f0f2-136">Übergeben des Kontexts als Argument</span><span class="sxs-lookup"><span data-stu-id="5f0f2-136">Passing the context as an argument</span></span>

  <span data-ttu-id="5f0f2-137">Bei den meisten AzureRM-Cmdlets kann der Kontext als Parameter an das Cmdlet übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-137">Most AzureRM cmdlets allow you to pass the context as a parameter to the cmdlet.</span></span> <span data-ttu-id="5f0f2-138">Das folgende Beispiel veranschaulicht das Übergeben eines Kontexts an einen Hintergrundauftrag:</span><span class="sxs-lookup"><span data-stu-id="5f0f2-138">You can pass a context to a background job as shown in the following example:</span></span>

  ```powershell
  PS C:\> $job = Start-Job { param ($ctx) New-AzureRmVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzureRmContext)
  ```

- <span data-ttu-id="5f0f2-139">Verwenden des Standardkontexts bei aktivierter automatischer Speicherung</span><span class="sxs-lookup"><span data-stu-id="5f0f2-139">Using the default context with Autosave enabled</span></span>

  <span data-ttu-id="5f0f2-140">Wenn Sie die **automatische Speicherung des Kontexts** aktiviert haben, wird von Hintergrundaufträgen automatisch der gespeicherte Standardkontext verwendet.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-140">If you have enabled **Context Autosave**, background jobs automatically use the default saved context.</span></span>

  ```powershell
  PS C:\> $job = Start-Job { New-AzureRmVm [... Additional parameters ...]}
  ```

<span data-ttu-id="5f0f2-141">Falls Sie das Ergebnis des Hintergrundauftrags ermitteln möchten, können Sie mit `Get-Job` den Auftragsstatus prüfen und mit `Wait-Job` auf den Abschluss des Auftrags warten.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-141">When you need to know the outcome of the background task, use `Get-Job` to check the job status and `Wait-Job` to wait for the Job to complete.</span></span> <span data-ttu-id="5f0f2-142">Mit `Receive-Job` können Sie die Ausgabe des Hintergrundauftrags erfassen oder anzeigen.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-142">Use `Receive-Job` to capture or display the output of the background job.</span></span> <span data-ttu-id="5f0f2-143">Weitere Informationen finden Sie unter [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="5f0f2-143">For more information, see [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="creating-selecting-renaming-and-removing-contexts"></a><span data-ttu-id="5f0f2-144">Erstellen, Auswählen, Umbenennen und Entfernen von Kontexten</span><span class="sxs-lookup"><span data-stu-id="5f0f2-144">Creating, selecting, renaming, and removing contexts</span></span>

<span data-ttu-id="5f0f2-145">Für die Kontexterstellung müssen Sie bei Azure angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-145">To create a context, you must be logged in to Azure.</span></span> <span data-ttu-id="5f0f2-146">Das Cmdlet `Connect-AzureRmAccount` (oder dessen Alias `Login-AzureRmAccount`) legt den von nachfolgenden Azure PowerShell-Cmdlets verwendeten Standardkontext fest und ermöglicht den Zugriff auf beliebige Mandanten oder Abonnements, die im Rahmen Ihrer Anmeldeinformationen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-146">The `Connect-AzureRmAccount` cmdlet (or its alias, `Login-AzureRmAccount`) sets the default context used by subsequent Azure PowerShell cmdlets, and allows you to access any tenants or subscriptions allowed by your login credentials.</span></span>

<span data-ttu-id="5f0f2-147">Verwenden Sie `Set-AzureRmContext` (oder dessen Alias `Select-AzureRmSubscription`), um nach der Anmeldung einen neuen Kontext hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-147">To add a new context after login, use `Set-AzureRmContext` (or its alias, `Select-AzureRmSubscription`).</span></span>

```azurepowershell-interactive
PS C:\> Set-AzureRMContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

<span data-ttu-id="5f0f2-148">Im vorherigen Beispiel wird ein neuer Kontext mit dem Ziel „Contoso Subscription 1“ und Ihren aktuellen Anmeldeinformationen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-148">The previous example adds a new context targeting 'Contoso Subscription 1' using your current credentials.</span></span> <span data-ttu-id="5f0f2-149">Der neue Kontext heißt „Contoso1“.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-149">The new context is named 'Contoso1'.</span></span> <span data-ttu-id="5f0f2-150">Falls Sie keinen Namen für den Kontext angeben, wird ein Standardname aus Konto-ID und Abonnement-ID verwendet.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-150">If you do not provide a name for the context, a default name, using the account ID and subscription ID is used.</span></span>

<span data-ttu-id="5f0f2-151">Einen vorhandenen Kontext können Sie mithilfe des Cmdlets `Rename-AzureRmContext` umbenennen.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-151">To rename an existing context, use the `Rename-AzureRmContext` cmdlet.</span></span> <span data-ttu-id="5f0f2-152">Beispiel: </span><span class="sxs-lookup"><span data-stu-id="5f0f2-152">For example:</span></span>

```azurepowershell-interactive
PS C:\> Rename-AzureRmContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

<span data-ttu-id="5f0f2-153">In diesem Beispiel wird der Kontext mit dem automatisch vergebenen Namen `[user1@contoso.org; 123456-7890-1234-564321]` in den einfachen Namen „Contoso2“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-153">This example renames the context with automatic name `[user1@contoso.org; 123456-7890-1234-564321]` to the simple name 'Contoso2'.</span></span> <span data-ttu-id="5f0f2-154">Dank Vervollständigung mit der TAB-TASTE können Sie in Kontextverwaltungs-Cmdlets schnell einen Kontext auswählen.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-154">Cmdlets that manage contexts also use tab completion, allowing you to quickly select the context.</span></span>

<span data-ttu-id="5f0f2-155">Zum Entfernen eines Kontexts steht das Cmdlet `Remove-AzureRmContext` zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-155">Finally, to remove a context, use the `Remove-AzureRmContext` cmdlet.</span></span>  <span data-ttu-id="5f0f2-156">Beispiel: </span><span class="sxs-lookup"><span data-stu-id="5f0f2-156">For example:</span></span>

```azurepowershell-interactive
PS C:\> Remove-AzureRmContext Contoso2
```

<span data-ttu-id="5f0f2-157">Verwirft den Kontext namens „Contoso2“.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-157">Forgets the context that was named 'Contoso2'.</span></span> <span data-ttu-id="5f0f2-158">Er kann anschließend mit `Set-AzureRmContext` erneut erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-158">You can recreate this context subsequently using `Set-AzureRmContext`</span></span>

## <a name="removing-credentials"></a><span data-ttu-id="5f0f2-159">Entfernen von Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="5f0f2-159">Removing credentials</span></span>

<span data-ttu-id="5f0f2-160">Mit `Disconnect-AzureRmAccount` (auch bekannt als `Logout-AzureRmAccount`) können Sie alle Anmeldeinformationen und zugeordneten Kontexte für einen Benutzer oder Dienstprinzipal entfernen.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-160">You can remove all credentials and associated contexts for a user or service principal using `Disconnect-AzureRmAccount` (also known as `Logout-AzureRmAccount`).</span></span> <span data-ttu-id="5f0f2-161">Wenn das Cmdlet `Disconnect-AzureRmAccount` ohne Parameter ausgeführt wird, entfernt es alle Anmeldeinformationen und Kontexte, die dem Benutzer oder Dienstprinzipal im aktuellen Kontext zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-161">When executed without parameters, the `Disconnect-AzureRmAccount` cmdlet removes all credentials and contexts associated with the User or Service Principal in the current context.</span></span> <span data-ttu-id="5f0f2-162">Wenn Sie einen bestimmten Prinzipal als Ziel verwenden möchten, können Sie einen Benutzernamen, Dienstprinzipalnamen oder Kontext übergeben.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-162">You may pass in a Username, Service Principal Name, or context to target a particular principal.</span></span>

```azurepowershell-interactive
Disconnect-AzureRmAccount user1@contoso.org
```

## <a name="using-context-scopes"></a><span data-ttu-id="5f0f2-163">Verwenden von Kontextbereichen</span><span class="sxs-lookup"><span data-stu-id="5f0f2-163">Using context scopes</span></span>

<span data-ttu-id="5f0f2-164">Manchmal möchten Sie unter Umständen einen Kontext in einer PowerShell-Sitzung auswählen, ändern oder entfernen, ohne dass sich das auf andere Sitzungen auswirkt.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-164">Occasionally, you may want to select, change, or remove a context in a PowerShell session without impacting other sessions.</span></span> <span data-ttu-id="5f0f2-165">Das Standardverhalten von Kontext-Cmdlets kann mithilfe des Parameters `Scope`geändert werden.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-165">To change the default behavior of context cmdlets, use the `Scope` parameter.</span></span> <span data-ttu-id="5f0f2-166">Der Bereich `Process` überschreibt das Standardverhalten, indem er die Gültigkeit auf die aktuelle Sitzung beschränkt.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-166">The `Process` scope overrides the default behavior by making it apply only for the current session.</span></span> <span data-ttu-id="5f0f2-167">Im Gegensatz dazu ändert der Bereich `CurrentUser` den Kontext nicht nur in der aktuellen Sitzung, sondern in allen Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-167">Conversely `CurrentUser` scope changes the context in all sessions, instead of just the current session.</span></span>

<span data-ttu-id="5f0f2-168">Verwenden Sie beispielsweise Folgendes, um den Standardkontext in der aktuellen PowerShell-Sitzung zu ändern, ohne andere Fenster oder den Kontext zu beeinflussen, der beim nächsten Öffnen einer Sitzung verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="5f0f2-168">As an example, to change the default context in the current PowerShell session without impacting other windows, or the context used the next time a session is opened, use:</span></span>

```azurepowershell-interactive
PS C:\> Select-AzureRmContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a><span data-ttu-id="5f0f2-169">Speicherung der Einstellung für die automatische Speicherung des Kontexts</span><span class="sxs-lookup"><span data-stu-id="5f0f2-169">How the context autosave setting is remembered</span></span>

<span data-ttu-id="5f0f2-170">Die Einstellung für die automatische Speicherung des Kontexts wird im Azure PowerShell-Verzeichnis des Benutzers (`%AppData%\Roaming\Windows Azure PowerShell`) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-170">The context AutoSave setting is saved to the user Azure PowerShell directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span> <span data-ttu-id="5f0f2-171">Manche Computerkonten haben möglicherweise keinen Zugriff auf dieses Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-171">Some kinds of computer accounts may not have access to this directory.</span></span> <span data-ttu-id="5f0f2-172">In solchen Fällen können Sie die Umgebungsvariable verwenden.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-172">For such scenarios, you can use the environment variable</span></span>

```azurepowershell-interactive
$env:AzureRmContextAutoSave="true" | "false"
```

<span data-ttu-id="5f0f2-173">Bei Verwendung von „true“ wird der Kontext automatisch gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-173">If set to 'true', the context is automatically saved.</span></span> <span data-ttu-id="5f0f2-174">Bei Verwendung von „false“ wird der Kontext nicht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-174">If set to 'false', the context is not saved.</span></span>

## <a name="changes-to-the-azurermprofile-module"></a><span data-ttu-id="5f0f2-175">Änderungen am Modul „AzureRM.Profile“</span><span class="sxs-lookup"><span data-stu-id="5f0f2-175">Changes to the AzureRM.Profile module</span></span>

<span data-ttu-id="5f0f2-176">Neue Cmdlets für die Kontextverwaltung</span><span class="sxs-lookup"><span data-stu-id="5f0f2-176">New cmdlets for managing context</span></span>

- <span data-ttu-id="5f0f2-177">[Enable-AzureRmContextAutosave][enable]: Ermöglicht das Speichern des Kontexts zwischen PowerShell-Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-177">[Enable-AzureRmContextAutosave][enable] - Allow saving the context between powershell sessions.</span></span>
  <span data-ttu-id="5f0f2-178">Änderungen wirken sich auf den globalen Kontext aus.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-178">Any changes alter the global context.</span></span>
- <span data-ttu-id="5f0f2-179">[Disable-AzureRmContextAutosave][disable]: Deaktiviert die automatische Speicherung des Kontexts.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-179">[Disable-AzureRmContextAutosave][disable] - Turn off autosaving the context.</span></span> <span data-ttu-id="5f0f2-180">Bei jeder neuen PowerShell-Sitzung ist eine erneute Anmeldung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-180">Each new PowerShell session is required to log in again.</span></span>
- <span data-ttu-id="5f0f2-181">[Select-AzureRmContext][select]: Ermöglicht das Auswählen eines Standardkontexts.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-181">[Select-AzureRmContext][select] - Select a context as the default.</span></span> <span data-ttu-id="5f0f2-182">Alle nachfolgenden Cmdlets verwenden die Anmeldeinformationen aus diesem Kontext für die Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-182">All subsequent cmdlets use the credentials in this context for authentication.</span></span>
- <span data-ttu-id="5f0f2-183">[Disconnect-AzureRmAccount][remove-cred]: Dient zum Entfernen aller einem Konto zugeordneten Anmeldeinformationen und Kontexte.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-183">[Disconnect-AzureRmAccount][remove-cred] - Remove all credentials and contexts associated with an account.</span></span>
- <span data-ttu-id="5f0f2-184">[Remove-AzureRmContext][remove-context]: Dient zum Entfernen eines benannten Kontexts.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-184">[Remove-AzureRmContext][remove-context] - Remove a named context.</span></span>
- <span data-ttu-id="5f0f2-185">[Rename-AzureRmContext][rename]: Dient zum Umbenennen eines vorhandenen Kontexts.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-185">[Rename-AzureRmContext][rename] - Rename an existing context.</span></span>

<span data-ttu-id="5f0f2-186">Änderungen an vorhandenen Profil-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="5f0f2-186">Changes to existing profile cmdlets</span></span>

- <span data-ttu-id="5f0f2-187">[Add-AzureRmAccount][login]: Ermöglicht es, den Gültigkeitsbereich der Anmeldung auf den Prozess oder auf den aktuellen Benutzer festzulegen.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-187">[Add-AzureRmAccount][login] - Allow scoping of the login to the process or the current user.</span></span>
  <span data-ttu-id="5f0f2-188">Ermöglicht die Benennung des Standardkontexts nach der Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-188">Allow naming the default context after login.</span></span>
- <span data-ttu-id="5f0f2-189">[Import-AzureRmContext][import]: Ermöglicht es, den Gültigkeitsbereich der Anmeldung auf den Prozess oder auf den aktuellen Benutzer festzulegen.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-189">[Import-AzureRmContext][import] - Allow scoping of the login to the process or the current user.</span></span>
- <span data-ttu-id="5f0f2-190">[Set-AzureRmContext][set-context]: Ermöglicht die Wahl vorhandener benannter Kontexte sowie die Festlegung, ob Änderungen auf den Prozess oder auf den aktuellen Benutzer angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5f0f2-190">[Set-AzureRmContext][set-context] - Allow selection of existing named contexts, and scope changes to the process or current user.</span></span>

<!-- Hyperlinks -->
[enable]: /powershell/module/azurerm.profile/Enable-AzureRmContextAutosave
[disable]: /powershell/module/azurerm.profile/Disable-AzureRmContextAutosave
[select]: /powershell/module/azurerm.profile/Select-AzureRmContext
[remove-cred]: /powershell/module/azurerm.profile/Disconnect-AzureRmAccount
[remove-context]: /powershell/module/azurerm.profile/Remove-AzureRmContext
[rename]: /powershell/module/azurerm.profile/Rename-AzureRmContext

<!-- Updated cmdlets -->
[login]: /powershell/module/azurerm.profile/Connect-AzureRmAccount
[import]: /powershell/module/azurerm.profile/Import-AzureRmAccount
[set-context]: /powershell/module/azurerm.profile/Import-AzureRmContext
