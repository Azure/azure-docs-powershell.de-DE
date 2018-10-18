---
title: Speichern von Benutzeranmeldeinformationen zwischen PowerShell-Sitzungen
description: Hier erfahren Sie, wie Sie Azure-Anmeldeinformationen und andere Informationen in mehreren PowerShell-Sitzungen wiederverwenden.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 9867efc991f4a9efe880c0f449d9d2be1cddf8ef
ms.sourcegitcommit: f6f5e256143aa6c097de3e57e930d8badea49f30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2018
ms.locfileid: "49399993"
---
# <a name="persist-user-credentials-across-powershell-sessions"></a><span data-ttu-id="4e78b-103">Speichern von Benutzeranmeldeinformationen zwischen PowerShell-Sitzungen</span><span class="sxs-lookup"><span data-stu-id="4e78b-103">Persist user credentials across PowerShell sessions</span></span>

<span data-ttu-id="4e78b-104">Azure PowerShell bietet ein Feature namens **Azure Context Autosave** mit den folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="4e78b-104">Azure PowerShell offers a feature called **Azure Context Autosave**, which gives the following features:</span></span>

- <span data-ttu-id="4e78b-105">Speicherung von Anmeldeinformationen zur Wiederverwendung in neuen PowerShell-Sitzungen</span><span class="sxs-lookup"><span data-stu-id="4e78b-105">Retention of sign-in information for reuse in new PowerShell sessions.</span></span>
- <span data-ttu-id="4e78b-106">Einfachere Verwendung von Hintergrundaufgaben für die Ausführung von Cmdlets mit langer Ausführungszeit</span><span class="sxs-lookup"><span data-stu-id="4e78b-106">Easier use of background tasks for executing long-running cmdlets.</span></span>
- <span data-ttu-id="4e78b-107">Wechsel zwischen Konten, Abonnements und Umgebungen ohne separate Anmeldung</span><span class="sxs-lookup"><span data-stu-id="4e78b-107">Switch between accounts, subscriptions, and environments without a separate sign-in.</span></span>
- <span data-ttu-id="4e78b-108">Gleichzeitige Ausführung von Aufgaben mit unterschiedlichen Anmeldeinformationen und Abonnements über die gleiche PowerShell-Sitzung</span><span class="sxs-lookup"><span data-stu-id="4e78b-108">Execution of tasks using different credentials and subscriptions, simultaneously, from the same PowerShell session.</span></span>

## <a name="azure-contexts-defined"></a><span data-ttu-id="4e78b-109">Definition von Azure-Kontexten</span><span class="sxs-lookup"><span data-stu-id="4e78b-109">Azure contexts defined</span></span>

<span data-ttu-id="4e78b-110">Bei einem *Azure-Kontext* handelt es sich um einen Satz von Informationen, die das Ziel von Azure PowerShell-Cmdlets definieren.</span><span class="sxs-lookup"><span data-stu-id="4e78b-110">An *Azure context* is a set of information that defines the target of Azure PowerShell cmdlets.</span></span> <span data-ttu-id="4e78b-111">Der Kontext setzt sich aus fünf Teilen zusammen:</span><span class="sxs-lookup"><span data-stu-id="4e78b-111">The context consists of five parts:</span></span>

- <span data-ttu-id="4e78b-112">Ein *Konto*: Der Benutzername oder Dienstprinzipal, der verwendet wird, um die Kommunikation mit Azure zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="4e78b-112">An *Account* - the UserName or Service Principal used to authenticate communications with Azure</span></span>
- <span data-ttu-id="4e78b-113">Ein *Abonnement*: Das Azure-Abonnement mit den Ressourcen, für die eine Aktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4e78b-113">A *Subscription* - The Azure Subscription with the Resources being acted upon.</span></span>
- <span data-ttu-id="4e78b-114">Ein *Mandant*: Der Azure Active Directory-Mandant mit Ihrem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4e78b-114">A *Tenant* - The Azure Active Directory tenant that contains your subscription.</span></span> <span data-ttu-id="4e78b-115">Mandanten sind eher für die Dienstprinzipalauthentifizierung relevant.</span><span class="sxs-lookup"><span data-stu-id="4e78b-115">Tenants are more important to ServicePrincipal authentication.</span></span>
- <span data-ttu-id="4e78b-116">Eine *Umgebung*: Die spezielle Azure-Cloud, die als Ziel fungiert (in der Regel die globale Azure-Cloud).</span><span class="sxs-lookup"><span data-stu-id="4e78b-116">An *Environment* - The particular Azure Cloud being targeted, usually the Azure global Cloud.</span></span>
  <span data-ttu-id="4e78b-117">Über die Umgebungseinstellung können Sie jedoch auch nationale Clouds, Government Clouds und lokale Clouds (Azure Stack) als Ziel festlegen.</span><span class="sxs-lookup"><span data-stu-id="4e78b-117">However, the environment setting allows you to target National, Government, and on-premises (Azure Stack) clouds as well.</span></span>
- <span data-ttu-id="4e78b-118">*Anmeldeinformationen*: Die Informationen, die von Azure verwendet werden, um Ihre Identität zu überprüfen und die Autorisierung des Zugriffs auf Ressourcen in Azure zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="4e78b-118">*Credentials* - The information used by Azure to verify your identity and confirm your authorization to access resources in Azure</span></span>

<span data-ttu-id="4e78b-119">In früheren Versionen musste bei jedem Öffnen einer neuen PowerShell-Sitzung ein Azure-Kontext erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4e78b-119">In previous releases, an Azure Context had to be created each time you opened a new PowerShell session.</span></span> <span data-ttu-id="4e78b-120">Ab Azure PowerShell 4.4.0 können Azure-Kontexte jeweils automatisch gespeichert werden, wenn eine neue PowerShell-Sitzung geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="4e78b-120">Beginning with Azure PowerShell v4.4.0, Azure Contexts can automatically be saved whenever opening a new PowerShell session.</span></span>

## <a name="automatically-save-the-context-for-the-next-sign-in"></a><span data-ttu-id="4e78b-121">Automatisches Speichern des Kontexts für die nächste Anmeldung</span><span class="sxs-lookup"><span data-stu-id="4e78b-121">Automatically save the context for the next sign-in</span></span>

<span data-ttu-id="4e78b-122">In den Versionen 6.3.0 und höher behält Azure PowerShell Ihre Kontextinformationen zwischen Sitzungen automatisch bei.</span><span class="sxs-lookup"><span data-stu-id="4e78b-122">In versions 6.3.0 and later, Azure PowerShell retains your context information automatically between sessions.</span></span> <span data-ttu-id="4e78b-123">Wenn PowerShell den Kontext und die Anmeldeinformationen verwerfen soll, verwenden Sie `Disable-AzureRmContextAutoSave`.</span><span class="sxs-lookup"><span data-stu-id="4e78b-123">To set PowerShell to forget your context and credentials, use `Disable-AzureRmContextAutoSave`.</span></span> <span data-ttu-id="4e78b-124">Sie müssen sich jedes Mal an Azure anmelden, wenn Sie eine PowerShell-Sitzung öffnen.</span><span class="sxs-lookup"><span data-stu-id="4e78b-124">You'll need to sign in to Azure every time you open a PowerShell session.</span></span>

<span data-ttu-id="4e78b-125">Mit `Enable-AzureRmContextAutosave` können Sie es Azure PowerShell ermöglichen, den Kontext über das Sitzungsende hinaus zu speichern.</span><span class="sxs-lookup"><span data-stu-id="4e78b-125">To allow Azure PowerShell to remember your context after the PowerShell session is closed, use `Enable-AzureRmContextAutosave`.</span></span> <span data-ttu-id="4e78b-126">Kontext und Anmeldeinformationen werden automatisch in einem speziellen ausgeblendeten Ordner in Ihrem Benutzerverzeichnis (`%AppData%\Roaming\Windows Azure PowerShell`) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4e78b-126">Context and credential information are automatically saved in a special hidden folder in your user directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span>
<span data-ttu-id="4e78b-127">Jede neue PowerShell-Sitzung verwendet den Kontext aus Ihrer letzten Sitzung als Ziel.</span><span class="sxs-lookup"><span data-stu-id="4e78b-127">Each new PowerShell session targets the context used in your last session.</span></span>

<span data-ttu-id="4e78b-128">Die Cmdlets zum Verwalten von Azure-Kontexten ermöglichen eine präzise Steuerung.</span><span class="sxs-lookup"><span data-stu-id="4e78b-128">The cmdlets that allow you to manage Azure contexts also allow you fine grained control.</span></span> <span data-ttu-id="4e78b-129">So können Sie festlegen, ob Änderungen nur für die aktuelle PowerShell-Sitzung (`Process`-Bereich) oder für jede PowerShell-Sitzung (`CurrentUser`-Bereich) gelten sollen.</span><span class="sxs-lookup"><span data-stu-id="4e78b-129">If you want changes to apply only to the current PowerShell session (`Process` scope) or every PowerShell session (`CurrentUser` scope).</span></span> <span data-ttu-id="4e78b-130">Ausführlichere Informationen zu diesen Optionen finden Sie unter [Verwenden von Kontextbereichen](#Using-Context-Scopes).</span><span class="sxs-lookup"><span data-stu-id="4e78b-130">These options are discussed in mode detail in [Using Context Scopes](#Using-Context-Scopes).</span></span>

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a><span data-ttu-id="4e78b-131">Ausführen von Azure PowerShell-Cmdlets als Hintergrundaufträge</span><span class="sxs-lookup"><span data-stu-id="4e78b-131">Running Azure PowerShell cmdlets as background jobs</span></span>

<span data-ttu-id="4e78b-132">Dank der**automatischen Speicherung des Azure-Kontexts können** Sie Ihren Kontext auch für PowerShell-Hintergrundaufträge freigeben.</span><span class="sxs-lookup"><span data-stu-id="4e78b-132">The **Azure Context Autosave** feature also allows you to share you context with PowerShell background jobs.</span></span> <span data-ttu-id="4e78b-133">Mit PowerShell können Sie Aufgaben mit langer Ausführungszeit als Hintergrundaufträge starten und überwachen, ohne auf den Abschluss der Aufgaben warten zu müssen.</span><span class="sxs-lookup"><span data-stu-id="4e78b-133">PowerShell allows you to start and monitor long-executing tasks as background jobs without having to wait for the tasks to complete.</span></span> <span data-ttu-id="4e78b-134">Sie können Anmeldeinformationen auf zwei Arten an Hintergrundaufträge weitergeben:</span><span class="sxs-lookup"><span data-stu-id="4e78b-134">You can share credentials with background jobs in two different ways:</span></span>

- <span data-ttu-id="4e78b-135">Übergeben des Kontexts als Argument</span><span class="sxs-lookup"><span data-stu-id="4e78b-135">Passing the context as an argument</span></span>

  <span data-ttu-id="4e78b-136">Bei den meisten AzureRM-Cmdlets kann der Kontext als Parameter an das Cmdlet übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="4e78b-136">Most AzureRM cmdlets allow you to pass the context as a parameter to the cmdlet.</span></span> <span data-ttu-id="4e78b-137">Das folgende Beispiel veranschaulicht das Übergeben eines Kontexts an einen Hintergrundauftrag:</span><span class="sxs-lookup"><span data-stu-id="4e78b-137">You can pass a context to a background job as shown in the following example:</span></span>

  ```powershell
  PS C:\> $job = Start-Job { param ($ctx) New-AzureRmVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzureRmContext)
  ```

- <span data-ttu-id="4e78b-138">Verwenden des Standardkontexts bei aktivierter automatischer Speicherung</span><span class="sxs-lookup"><span data-stu-id="4e78b-138">Using the default context with Autosave enabled</span></span>

  <span data-ttu-id="4e78b-139">Wenn Sie die **automatische Speicherung des Kontexts** aktiviert haben, wird von Hintergrundaufträgen automatisch der gespeicherte Standardkontext verwendet.</span><span class="sxs-lookup"><span data-stu-id="4e78b-139">If you have enabled **Context Autosave**, background jobs automatically use the default saved context.</span></span>

  ```powershell
  PS C:\> $job = Start-Job { New-AzureRmVm [... Additional parameters ...]}
  ```

<span data-ttu-id="4e78b-140">Falls Sie das Ergebnis des Hintergrundauftrags ermitteln möchten, können Sie mit `Get-Job` den Auftragsstatus prüfen und mit `Wait-Job` auf den Abschluss des Auftrags warten.</span><span class="sxs-lookup"><span data-stu-id="4e78b-140">When you need to know the outcome of the background task, use `Get-Job` to check the job status and `Wait-Job` to wait for the Job to complete.</span></span> <span data-ttu-id="4e78b-141">Mit `Receive-Job` können Sie die Ausgabe des Hintergrundauftrags erfassen oder anzeigen.</span><span class="sxs-lookup"><span data-stu-id="4e78b-141">Use `Receive-Job` to capture or display the output of the background job.</span></span> <span data-ttu-id="4e78b-142">Weitere Informationen finden Sie unter [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="4e78b-142">For more information, see [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="creating-selecting-renaming-and-removing-contexts"></a><span data-ttu-id="4e78b-143">Erstellen, Auswählen, Umbenennen und Entfernen von Kontexten</span><span class="sxs-lookup"><span data-stu-id="4e78b-143">Creating, selecting, renaming, and removing contexts</span></span>

<span data-ttu-id="4e78b-144">Für die Kontexterstellung müssen Sie bei Azure angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="4e78b-144">To create a context, you must be signed in to Azure.</span></span> <span data-ttu-id="4e78b-145">Das Cmdlet `Connect-AzureRmAccount` (oder dessen Alias `Login-AzureRmAccount`) legt den von Azure PowerShell-Cmdlets verwendeten Standardkontext fest und ermöglicht den Zugriff auf beliebige Mandanten oder Abonnements, die im Rahmen Ihrer Anmeldeinformationen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="4e78b-145">The `Connect-AzureRmAccount` cmdlet (or its alias, `Login-AzureRmAccount`) sets the default context used by Azure PowerShell cmdlets, and allows you to access any tenants or subscriptions allowed by your credentials.</span></span>

<span data-ttu-id="4e78b-146">Verwenden Sie `Set-AzureRmContext` (oder dessen Alias `Select-AzureRmSubscription`), um nach der Anmeldung einen neuen Kontext hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4e78b-146">To add a new context after sign-in, use `Set-AzureRmContext` (or its alias, `Select-AzureRmSubscription`).</span></span>

```azurepowershell-interactive
PS C:\> Set-AzureRMContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

<span data-ttu-id="4e78b-147">Im vorherigen Beispiel wird ein neuer Kontext mit dem Ziel „Contoso Subscription 1“ und Ihren aktuellen Anmeldeinformationen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4e78b-147">The previous example adds a new context targeting 'Contoso Subscription 1' using your current credentials.</span></span> <span data-ttu-id="4e78b-148">Der neue Kontext heißt „Contoso1“.</span><span class="sxs-lookup"><span data-stu-id="4e78b-148">The new context is named 'Contoso1'.</span></span> <span data-ttu-id="4e78b-149">Falls Sie keinen Namen für den Kontext angeben, wird ein Standardname aus Konto-ID und Abonnement-ID verwendet.</span><span class="sxs-lookup"><span data-stu-id="4e78b-149">If you don't provide a name for the context, a default name, using the account ID and subscription ID is used.</span></span>

<span data-ttu-id="4e78b-150">Einen vorhandenen Kontext können Sie mithilfe des Cmdlets `Rename-AzureRmContext` umbenennen.</span><span class="sxs-lookup"><span data-stu-id="4e78b-150">To rename an existing context, use the `Rename-AzureRmContext` cmdlet.</span></span> <span data-ttu-id="4e78b-151">Beispiel: </span><span class="sxs-lookup"><span data-stu-id="4e78b-151">For example:</span></span>

```azurepowershell-interactive
PS C:\> Rename-AzureRmContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

<span data-ttu-id="4e78b-152">In diesem Beispiel wird der Kontext mit dem automatisch vergebenen Namen `[user1@contoso.org; 123456-7890-1234-564321]` in den einfachen Namen „Contoso2“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="4e78b-152">This example renames the context with automatic name `[user1@contoso.org; 123456-7890-1234-564321]` to the simple name 'Contoso2'.</span></span> <span data-ttu-id="4e78b-153">Dank Vervollständigung mit der TAB-TASTE können Sie in Kontextverwaltungs-Cmdlets schnell einen Kontext auswählen.</span><span class="sxs-lookup"><span data-stu-id="4e78b-153">Cmdlets that manage contexts also use tab completion, allowing you to quickly select the context.</span></span>

<span data-ttu-id="4e78b-154">Zum Entfernen eines Kontexts steht das Cmdlet `Remove-AzureRmContext` zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="4e78b-154">Finally, to remove a context, use the `Remove-AzureRmContext` cmdlet.</span></span>  <span data-ttu-id="4e78b-155">Beispiel: </span><span class="sxs-lookup"><span data-stu-id="4e78b-155">For example:</span></span>

```azurepowershell-interactive
PS C:\> Remove-AzureRmContext Contoso2
```

<span data-ttu-id="4e78b-156">Verwirft den Kontext namens „Contoso2“.</span><span class="sxs-lookup"><span data-stu-id="4e78b-156">Forgets the context that was named 'Contoso2'.</span></span> <span data-ttu-id="4e78b-157">Sie können diesen Kontext neu erstellen, indem Sie `Set-AzureRmContext` verwenden.</span><span class="sxs-lookup"><span data-stu-id="4e78b-157">You can recreate this context using `Set-AzureRmContext`</span></span>

## <a name="removing-credentials"></a><span data-ttu-id="4e78b-158">Entfernen von Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="4e78b-158">Removing credentials</span></span>

<span data-ttu-id="4e78b-159">Mit `Disconnect-AzureRmAccount` (auch bekannt als `Logout-AzureRmAccount`) können Sie alle Anmeldeinformationen und zugeordneten Kontexte für einen Benutzer oder Dienstprinzipal entfernen.</span><span class="sxs-lookup"><span data-stu-id="4e78b-159">You can remove all credentials and associated contexts for a user or service principal using `Disconnect-AzureRmAccount` (also known as `Logout-AzureRmAccount`).</span></span> <span data-ttu-id="4e78b-160">Wenn das Cmdlet `Disconnect-AzureRmAccount` ohne Parameter ausgeführt wird, entfernt es alle Anmeldeinformationen und Kontexte, die dem Benutzer oder Dienstprinzipal im aktuellen Kontext zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="4e78b-160">When executed without parameters, the `Disconnect-AzureRmAccount` cmdlet removes all credentials and contexts associated with the User or Service Principal in the current context.</span></span> <span data-ttu-id="4e78b-161">Wenn Sie einen bestimmten Prinzipal als Ziel verwenden möchten, können Sie einen Benutzernamen, Dienstprinzipalnamen oder Kontext übergeben.</span><span class="sxs-lookup"><span data-stu-id="4e78b-161">You may pass in a Username, Service Principal Name, or context to target a particular principal.</span></span>

```azurepowershell-interactive
Disconnect-AzureRmAccount user1@contoso.org
```

## <a name="using-context-scopes"></a><span data-ttu-id="4e78b-162">Verwenden von Kontextbereichen</span><span class="sxs-lookup"><span data-stu-id="4e78b-162">Using context scopes</span></span>

<span data-ttu-id="4e78b-163">Manchmal möchten Sie unter Umständen einen Kontext in einer PowerShell-Sitzung auswählen, ändern oder entfernen, ohne dass sich das auf andere Sitzungen auswirkt.</span><span class="sxs-lookup"><span data-stu-id="4e78b-163">Occasionally, you may want to select, change, or remove a context in a PowerShell session without impacting other sessions.</span></span> <span data-ttu-id="4e78b-164">Das Standardverhalten von Kontext-Cmdlets kann mithilfe des Parameters `Scope`geändert werden.</span><span class="sxs-lookup"><span data-stu-id="4e78b-164">To change the default behavior of context cmdlets, use the `Scope` parameter.</span></span> <span data-ttu-id="4e78b-165">Der Bereich `Process` überschreibt das Standardverhalten, indem er die Gültigkeit auf die aktuelle Sitzung beschränkt.</span><span class="sxs-lookup"><span data-stu-id="4e78b-165">The `Process` scope overrides the default behavior by making it apply only for the current session.</span></span> <span data-ttu-id="4e78b-166">Im Gegensatz dazu ändert der Bereich `CurrentUser` den Kontext nicht nur in der aktuellen Sitzung, sondern in allen Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="4e78b-166">Conversely `CurrentUser` scope changes the context in all sessions, instead of just the current session.</span></span>

<span data-ttu-id="4e78b-167">Verwenden Sie beispielsweise Folgendes, um den Standardkontext in der aktuellen PowerShell-Sitzung zu ändern, ohne andere Fenster oder den Kontext zu beeinflussen, der beim nächsten Öffnen einer Sitzung verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="4e78b-167">As an example, to change the default context in the current PowerShell session without impacting other windows, or the context used the next time a session is opened, use:</span></span>

```azurepowershell-interactive
PS C:\> Select-AzureRmContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a><span data-ttu-id="4e78b-168">Speicherung der Einstellung für die automatische Speicherung des Kontexts</span><span class="sxs-lookup"><span data-stu-id="4e78b-168">How the context autosave setting is remembered</span></span>

<span data-ttu-id="4e78b-169">Die Einstellung für die automatische Speicherung des Kontexts wird im Azure PowerShell-Verzeichnis des Benutzers (`%AppData%\Roaming\Windows Azure PowerShell`) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4e78b-169">The context AutoSave setting is saved to the user Azure PowerShell directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span> <span data-ttu-id="4e78b-170">Manche Computerkonten haben möglicherweise keinen Zugriff auf dieses Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="4e78b-170">Some kinds of computer accounts may not have access to this directory.</span></span> <span data-ttu-id="4e78b-171">In solchen Fällen können Sie die Umgebungsvariable verwenden.</span><span class="sxs-lookup"><span data-stu-id="4e78b-171">For such scenarios, you can use the environment variable</span></span>

```azurepowershell-interactive
$env:AzureRmContextAutoSave="true" | "false"
```

<span data-ttu-id="4e78b-172">Bei Verwendung von „true“ wird der Kontext automatisch gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4e78b-172">When set to 'true', the context is automatically saved.</span></span> <span data-ttu-id="4e78b-173">Bei Verwendung von „false“ wird der Kontext nicht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4e78b-173">If set to 'false', the context isn't saved.</span></span>

## <a name="changes-to-the-azurermprofile-module"></a><span data-ttu-id="4e78b-174">Änderungen am Modul „AzureRM.Profile“</span><span class="sxs-lookup"><span data-stu-id="4e78b-174">Changes to the AzureRM.Profile module</span></span>

<span data-ttu-id="4e78b-175">Neue Cmdlets für die Kontextverwaltung</span><span class="sxs-lookup"><span data-stu-id="4e78b-175">New cmdlets for managing context</span></span>

- <span data-ttu-id="4e78b-176">[Enable-AzureRmContextAutosave][enable]: Ermöglicht das Speichern des Kontexts zwischen PowerShell-Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="4e78b-176">[Enable-AzureRmContextAutosave][enable] - Allow saving the context between powershell sessions.</span></span>
  <span data-ttu-id="4e78b-177">Änderungen wirken sich auf den globalen Kontext aus.</span><span class="sxs-lookup"><span data-stu-id="4e78b-177">Any changes alter the global context.</span></span>
- <span data-ttu-id="4e78b-178">[Disable-AzureRmContextAutosave][disable]: Deaktiviert die automatische Speicherung des Kontexts.</span><span class="sxs-lookup"><span data-stu-id="4e78b-178">[Disable-AzureRmContextAutosave][disable] - Turn off autosaving the context.</span></span> <span data-ttu-id="4e78b-179">Bei jeder neuen PowerShell-Sitzung ist eine erneute Anmeldung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4e78b-179">Each new PowerShell session is required to sign in again.</span></span>
- <span data-ttu-id="4e78b-180">[Select-AzureRmContext][select]: Ermöglicht das Auswählen eines Standardkontexts.</span><span class="sxs-lookup"><span data-stu-id="4e78b-180">[Select-AzureRmContext][select] - Select a context as the default.</span></span> <span data-ttu-id="4e78b-181">Alle Cmdlets verwenden die Anmeldeinformationen aus diesem Kontext für die Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="4e78b-181">All cmdlets use the credentials in this context for authentication.</span></span>
- <span data-ttu-id="4e78b-182">[Disconnect-AzureRmAccount][remove-cred]: Dient zum Entfernen aller einem Konto zugeordneten Anmeldeinformationen und Kontexte.</span><span class="sxs-lookup"><span data-stu-id="4e78b-182">[Disconnect-AzureRmAccount][remove-cred] - Remove all credentials and contexts associated with an account.</span></span>
- <span data-ttu-id="4e78b-183">[Remove-AzureRmContext][remove-context]: Dient zum Entfernen eines benannten Kontexts.</span><span class="sxs-lookup"><span data-stu-id="4e78b-183">[Remove-AzureRmContext][remove-context] - Remove a named context.</span></span>
- <span data-ttu-id="4e78b-184">[Rename-AzureRmContext][rename]: Dient zum Umbenennen eines vorhandenen Kontexts.</span><span class="sxs-lookup"><span data-stu-id="4e78b-184">[Rename-AzureRmContext][rename] - Rename an existing context.</span></span>

<span data-ttu-id="4e78b-185">Änderungen an vorhandenen Profil-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="4e78b-185">Changes to existing profile cmdlets</span></span>

- <span data-ttu-id="4e78b-186">[Add-AzureRmAccount][login]: Ermöglicht es, den Gültigkeitsbereich der Anmeldung auf den Prozess oder auf den aktuellen Benutzer festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4e78b-186">[Add-AzureRmAccount][login] - Allow scoping of the sign-in to the process or the current user.</span></span>
  <span data-ttu-id="4e78b-187">Ermöglicht die Benennung des Standardkontexts nach der Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="4e78b-187">Allow naming the default context after authentication.</span></span>
- <span data-ttu-id="4e78b-188">[Import-AzureRmContext][import]: Ermöglicht es, den Gültigkeitsbereich der Anmeldung auf den Prozess oder auf den aktuellen Benutzer festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4e78b-188">[Import-AzureRmContext][import] - Allow scoping of the sign-in to the process or the current user.</span></span>
- <span data-ttu-id="4e78b-189">[Set-AzureRmContext][set-context]: Ermöglicht die Wahl vorhandener benannter Kontexte sowie die Festlegung, ob Änderungen auf den Prozess oder auf den aktuellen Benutzer angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4e78b-189">[Set-AzureRmContext][set-context] - Allow selection of existing named contexts, and scope changes to the process or current user.</span></span>

<!-- Hyperlinks -->
[enable]: /powershell/module/azurerm.profile/Enable-AzureRmContextAutosave
[disable]: /powershell/module/azurerm.profile/Disable-AzureRmContextAutosave
[select]: /powershell/module/azurerm.profile/Select-AzureRmContext
[remove-cred]: /powershell/module/azurerm.profile/Disconnect-AzureRmAccount
[remove-context]: /powershell/module/azurerm.profile/Remove-AzureRmContext
[rename]: /powershell/module/azurerm.profile/Rename-AzureRmContext

<!-- Updated cmdlets -->
[login]: /powershell/module/azurerm.profile/Connect-AzureRmAccount
[import]:  /powershell/module/azurerm.profile/Import-AzureRmContext
[set-context]: /powershell/module/azurerm.profile/Set-AzureRmContext
