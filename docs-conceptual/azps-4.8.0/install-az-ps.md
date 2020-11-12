---
title: Installieren von Azure PowerShell mit PowerShellGet
description: Anleitung für die Installation von Azure PowerShell mit PowerShellGet
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/14/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: f7a1658cdcafd1e8d6cba51ead26f9ddaa8c4c56
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2020
ms.locfileid: "93407384"
---
# <a name="install-azure-powershell"></a><span data-ttu-id="7ba8f-103">Installieren von Azure Powershell</span><span class="sxs-lookup"><span data-stu-id="7ba8f-103">Install Azure PowerShell</span></span>

<span data-ttu-id="7ba8f-104">In diesem Artikel wird erläutert, wie Sie mithilfe von [PowerShellGet](/powershell/scripting/gallery/installing-psget) die Azure PowerShell-Module installieren.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-104">This article explains how to install the Azure PowerShell modules using [PowerShellGet](/powershell/scripting/gallery/installing-psget).</span></span> <span data-ttu-id="7ba8f-105">Diese Anweisungen können für Windows-, macOS- und Linux-Plattformen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-105">These instructions work on Windows, macOS, and Linux platforms.</span></span>

<span data-ttu-id="7ba8f-106">Azure PowerShell ist auch in Azure [Cloud Shell](/azure/cloud-shell/overview) verfügbar und nun in [Docker-Images](azureps-in-docker.md) vorinstalliert.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-106">Azure PowerShell is also available in Azure [Cloud Shell](/azure/cloud-shell/overview) and is now preinstalled in [Docker images](azureps-in-docker.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7ba8f-107">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="7ba8f-107">Requirements</span></span>

> [!NOTE]
> <span data-ttu-id="7ba8f-108">PowerShell 7.x und höher ist die für die Verwendung mit Azure PowerShell auf allen Plattformen empfohlene PowerShell-Version.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-108">PowerShell 7.x and later is the recommended version of PowerShell for use with Azure PowerShell on all platforms.</span></span>

<span data-ttu-id="7ba8f-109">Azure PowerShell funktioniert mit PowerShell 6.2.4 und höher auf allen Plattformen.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-109">Azure PowerShell works with PowerShell 6.2.4 and later on all platforms.</span></span> <span data-ttu-id="7ba8f-110">Es wird auch mit PowerShell 5.1 unter Windows unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-110">It is also supported with PowerShell 5.1 on Windows.</span></span> <span data-ttu-id="7ba8f-111">Installieren Sie die [aktuelle PowerShell-Version](/powershell/scripting/install/installing-powershell) für Ihr Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-111">Install the [latest version of PowerShell](/powershell/scripting/install/installing-powershell) available for your operating system.</span></span> <span data-ttu-id="7ba8f-112">Bei der Ausführung in PowerShell 6.2.4 und höher gibt es keine zusätzlichen Anforderungen an Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-112">Azure PowerShell has no additional requirements when run on PowerShell 6.2.4 and later.</span></span>

<span data-ttu-id="7ba8f-113">Führen Sie den Befehl aus, um Ihre PowerShell-Version zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="7ba8f-113">To check your PowerShell version, run the command:</span></span>

```azurepowershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="7ba8f-114">So verwenden Sie Azure PowerShell in PowerShell 5.1 unter Windows:</span><span class="sxs-lookup"><span data-stu-id="7ba8f-114">To use Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="7ba8f-115">Führen Sie ein Update auf [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell) aus.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-115">Update to [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span></span>
   <span data-ttu-id="7ba8f-116">Unter Windows 10, Version 1607 oder höher, ist PowerShell 5.1 bereits installiert.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-116">If you're on Windows 10 version 1607 or higher, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="7ba8f-117">Installieren Sie [.NET Framework 4.7.2 oder höher](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="7ba8f-117">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>
3. <span data-ttu-id="7ba8f-118">Vergewissern Sie sich, dass die aktuelle Version von PowerShellGet installiert ist.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-118">Make sure you have the latest version of PowerShellGet.</span></span> <span data-ttu-id="7ba8f-119">Führen Sie `Install-Module -Name PowerShellGet -Force` aus.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-119">Run `Install-Module -Name PowerShellGet -Force`.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="7ba8f-120">Installieren des Azure PowerShell-Moduls</span><span class="sxs-lookup"><span data-stu-id="7ba8f-120">Install the Azure PowerShell module</span></span>

> [!WARNING]
> <span data-ttu-id="7ba8f-121">Die Module AzureRM und Az können für PowerShell 5.1 unter Windows nicht gleichzeitig installiert sein.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-121">We do not support having both the AzureRM and Az modules installed for PowerShell 5.1 on Windows at the same time.</span></span> <span data-ttu-id="7ba8f-122">Wenn AzureRM weiterhin auf Ihrem System verfügbar sein soll, installieren Sie das Az-Modul für PowerShell 6.2.4 oder höher.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-122">If you need to keep AzureRM available on your system, install the Az module for PowerShell 6.2.4 or later.</span></span>

<span data-ttu-id="7ba8f-123">Die Verwendung der PowerShellGet-Cmdlets ist die bevorzugte Installationsmethode.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-123">Using the PowerShellGet cmdlets is the preferred installation method.</span></span> <span data-ttu-id="7ba8f-124">Installieren Sie das Az-Modul nur für den aktuellen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-124">Install the Az module for the current user only.</span></span> <span data-ttu-id="7ba8f-125">Dies ist der empfohlene Installationsbereich.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-125">This is the recommended installation scope.</span></span> <span data-ttu-id="7ba8f-126">Die Funktionsweise dieser Methode ist auf Windows-, macOS- und Linux-Plattformen gleich.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-126">This method works the same on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="7ba8f-127">Führen Sie den folgenden Befehl in einer PowerShell-Sitzung aus:</span><span class="sxs-lookup"><span data-stu-id="7ba8f-127">Run the following command from a PowerShell session:</span></span>

```powershell-interactive
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope CurrentUser
}
```

<span data-ttu-id="7ba8f-128">Standardmäßig ist der PowerShell-Katalog nicht als vertrauenswürdiges Repository für PowerShellGet konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-128">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="7ba8f-129">Bei der ersten Verwendung des PowerShell-Katalogs wird die folgende Meldung angezeigt:</span><span class="sxs-lookup"><span data-stu-id="7ba8f-129">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the `Set-PSRepository` cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="7ba8f-130">Antworten Sie mit `Yes` oder `Yes to All`, um die Installation fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-130">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="7ba8f-131">Zum Installieren des Moduls für alle Benutzer in einem System sind erhöhte Rechte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-131">Installing the module for all users on a system requires elevated privileges.</span></span> <span data-ttu-id="7ba8f-132">Starten Sie unter Windows die PowerShell-Sitzung mithilfe der Option **Als Administrator ausführen**. Verwenden Sie unter macOS oder Linux den Befehl `sudo`:</span><span class="sxs-lookup"><span data-stu-id="7ba8f-132">Start the PowerShell session using **Run as administrator** in Windows or use the `sudo` command on macOS or Linux:</span></span>

```powershell-interactive
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope AllUsers
}
```

<span data-ttu-id="7ba8f-133">Das Az-Modul ist ein Rollupmodul für die Azure PowerShell-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-133">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="7ba8f-134">Wenn Sie es installieren, werden alle verfügbaren Azure PowerShell-Module heruntergeladen und die zugehörigen Cmdlets für die Nutzung zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-134">Installing it downloads all of the generally available Az PowerShell modules, and makes their cmdlets available for use.</span></span>

## <a name="install-offline"></a><span data-ttu-id="7ba8f-135">Offlineinstallation</span><span class="sxs-lookup"><span data-stu-id="7ba8f-135">Install offline</span></span>

<span data-ttu-id="7ba8f-136">In einigen Umgebungen ist es nicht möglich, eine Verbindung mit dem PowerShell-Katalog herzustellen.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-136">In some environments, it's not possible to connect to the PowerShell Gallery.</span></span> <span data-ttu-id="7ba8f-137">In diesen Fällen können Sie die Installation mithilfe einer der folgenden Methoden weiterhin offline durchführen:</span><span class="sxs-lookup"><span data-stu-id="7ba8f-137">In those situations, you can still install offline using one of these methods:</span></span>

* <span data-ttu-id="7ba8f-138">Laden Sie die Module an einen anderen Speicherort in Ihrem Netzwerk herunter, und verwenden Sie diesen als Installationsquelle.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-138">Download the modules to another location in your network and use that as an installation source.</span></span>
  <span data-ttu-id="7ba8f-139">Dieses Verfahren ermöglicht die Zwischenspeicherung von PowerShell-Modulen, die mithilfe von PowerShellGet auf Systemen ohne Verbindung bereitgestellt werden sollen, auf einem einzelnen Server oder in einer einzelnen Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-139">This method allows you to cache PowerShell modules on a single server or file share to be deployed with PowerShellGet to any disconnected systems.</span></span> <span data-ttu-id="7ba8f-140">Unter [Arbeiten mit lokalen PowerShellGet-Repositorys](/powershell/scripting/gallery/how-to/working-with-local-psrepositories) erfahren Sie, wie Sie ein lokales Repository einrichten und die Installation auf getrennten Systemen ausführen.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-140">Learn how to set up a local repository and install on disconnected systems with [Working with local PowerShellGet repositories](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span></span>
* <span data-ttu-id="7ba8f-141">[Laden Sie die Azure PowerShell MSI](install-az-ps-msi.md) auf einen mit dem Netzwerk verbundenen Computer herunter, und kopieren Sie anschließend das Installationsprogramm auf Systeme ohne Zugriff auf den PowerShell-Katalog.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-141">[Download the Azure PowerShell MSI](install-az-ps-msi.md) to a machine connected to the network, and then copy the installer to systems without access to PowerShell Gallery.</span></span> <span data-ttu-id="7ba8f-142">Beachten Sie, dass das MSI-Installationsprogramm nur für PowerShell 5.1 unter Windows verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-142">Keep in mind that the MSI installer only works for PowerShell 5.1 on Windows.</span></span>
* <span data-ttu-id="7ba8f-143">Speichern Sie das Modul mit [Save-Module](/powershell/module/PowershellGet/Save-Module) auf einer Dateifreigabe oder einer anderen Quelle, und kopieren Sie es manuell auf andere Computer:</span><span class="sxs-lookup"><span data-stu-id="7ba8f-143">Save the module with [Save-Module](/powershell/module/PowershellGet/Save-Module) to a file share, or save it to another source and manually copy it to other machines:</span></span>

  ```powershell-interactive
  Save-Module -Name Az -Path '\\server\share\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a><span data-ttu-id="7ba8f-144">Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="7ba8f-144">Troubleshooting</span></span>

<span data-ttu-id="7ba8f-145">In diesem Abschnitt finden Sie einige allgemeine Probleme, die bei der Installation des Azure PowerShell-Moduls auftreten können.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-145">Here are some common problems seen when installing the Azure PowerShell module.</span></span> <span data-ttu-id="7ba8f-146">Falls ein Problem auftritt, das hier nicht aufgeführt ist, [melden Sie es auf GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="7ba8f-146">If you experience a problem not listed here, [file an issue on GitHub](https://github.com/azure/azure-powershell/issues).</span></span>

### <a name="proxy-blocks-connection"></a><span data-ttu-id="7ba8f-147">Der Proxy blockiert die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-147">Proxy blocks connection</span></span>

<span data-ttu-id="7ba8f-148">Wenn Sie von `Install-Module` Fehler erhalten, die anzeigen, dass der PowerShell-Katalog nicht erreichbar ist, befinden Sie sich möglicherweise hinter einem Proxy.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-148">If you get errors from `Install-Module` that indicate the PowerShell Gallery is unreachable, you may be behind a proxy.</span></span> <span data-ttu-id="7ba8f-149">Verschiedene Betriebssysteme und Netzwerkumgebungen haben unterschiedliche Anforderungen an die Konfiguration eines systemweiten Proxys.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-149">Different operating systems and network environment have different requirements for configuring a system-wide proxy.</span></span> <span data-ttu-id="7ba8f-150">Wenden Sie sich an Ihren Systemadministrator, um Ihre Proxyeinstellungen zu erhalten und zu erfahren, wie Sie sie für Ihre Umgebung konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-150">Contact your system administrator for your proxy settings and how to configure them for your environment.</span></span>

<span data-ttu-id="7ba8f-151">PowerShell selbst ist möglicherweise nicht so konfiguriert, dass es diesen Proxy automatisch verwendet.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-151">PowerShell itself may not be configured to use this proxy automatically.</span></span> <span data-ttu-id="7ba8f-152">Konfigurieren Sie bei PowerShell 5.1 und höher die PowerShell-Sitzung mit den folgenden Befehlen so, dass ein Proxy verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="7ba8f-152">With PowerShell 5.1 and later, configure the PowerShell session to use a proxy using the following commands:</span></span>

```powershell
$webClient = New-Object System.Net.WebClient
$webClient.Proxy.Credentials = [System.Net.CredentialCache]::DefaultNetworkCredentials
```

<span data-ttu-id="7ba8f-153">Wenn die Anmeldeinformationen Ihres Betriebssystems ordnungsgemäß konfiguriert sind, leitet diese Konfiguration PowerShell-Anforderungen über den Proxy weiter.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-153">If your operating system credentials are configured correctly, this configuration routes PowerShell requests through the proxy.</span></span> <span data-ttu-id="7ba8f-154">Damit diese Einstellung auch zwischen den Sitzungen erhalten bleibt, fügen Sie die Befehle zu Ihrem [PowerShell-Profil](/powershell/module/microsoft.powershell.core/about/about_profiles) hinzu.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-154">To have this setting persist between sessions, add the commands to your [PowerShell profile](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>

<span data-ttu-id="7ba8f-155">Ihr Proxy muss HTTPS-Verbindungen mit der folgenden Adresse zulassen, damit das Paket installiert werden kann:</span><span class="sxs-lookup"><span data-stu-id="7ba8f-155">To install the package, your proxy needs to allow HTTPS connections to the following address:</span></span>

* `https://www.powershellgallery.com`

## <a name="sign-in"></a><span data-ttu-id="7ba8f-156">Anmelden</span><span class="sxs-lookup"><span data-stu-id="7ba8f-156">Sign in</span></span>

<span data-ttu-id="7ba8f-157">Melden Sie sich mit Ihren Azure-Anmeldeinformationen an, um Azure PowerShell zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-157">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
> <span data-ttu-id="7ba8f-158">Wenn Sie das automatische Laden von Modulen deaktiviert haben, importieren Sie das Modul manuell mit `Import-Module -Name Az`.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-158">If you've disabled module autoloading, manually import the module with `Import-Module -Name Az`.</span></span>
> <span data-ttu-id="7ba8f-159">Aufgrund der Modulstruktur kann dieser Vorgang einige Sekunden dauern.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-159">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="7ba8f-160">Sie müssen diese Schritte für jede neue PowerShell-Sitzung wiederholen, die Sie starten.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-160">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="7ba8f-161">Informationen zum sitzungsübergreifenden Speichern der Azure-Anmeldung in PowerShell finden Sie unter [Speichern von Benutzeranmeldeinformationen zwischen PowerShell-Sitzungen](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="7ba8f-161">To learn how to persist your Azure sign in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="7ba8f-162">Aktualisieren des Azure PowerShell-Moduls</span><span class="sxs-lookup"><span data-stu-id="7ba8f-162">Update the Azure PowerShell module</span></span>

<span data-ttu-id="7ba8f-163">Zum Aktualisieren eines beliebigen PowerShell-Moduls müssen Sie dieselbe Methode verwenden, die zum Installieren des Moduls verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-163">To update any PowerShell module, you should use the same method used to install the module.</span></span> <span data-ttu-id="7ba8f-164">Wenn Sie beispielsweise ursprünglich `Install-Module` verwendet haben, müssen Sie [Update-Module](/powershell/module/powershellget/update-module) verwenden, um die neueste Version zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-164">For example, if you originally used `Install-Module`, then you should use [Update-Module](/powershell/module/powershellget/update-module) to get the latest version.</span></span> <span data-ttu-id="7ba8f-165">Wenn Sie ursprünglich das MSI-Paket verwendet haben, müssen Sie das neue MSI-Paket herunterladen und installieren.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-165">If you originally used the MSI package then you should download and install the new MSI package.</span></span>

<span data-ttu-id="7ba8f-166">Die PowerShellGet-Cmdlets können keine Module aktualisieren, die über ein MSI-Paket installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-166">The PowerShellGet cmdlets cannot update modules that were installed from an MSI package.</span></span> <span data-ttu-id="7ba8f-167">Mit MSI-Paketen werden keine Module aktualisiert, die mithilfe von PowerShellGet installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-167">MSI packages do not update modules that were installed using PowerShellGet.</span></span> <span data-ttu-id="7ba8f-168">Wenn bei der Aktualisierung mithilfe von PowerShellGet Probleme auftreten, sollten Sie eine **Neuinstallation** anstelle eines **Updates** durchführen.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-168">If you have any issues updating using PowershellGet, then you should **reinstall** , rather than **update**.</span></span> <span data-ttu-id="7ba8f-169">Die Neuinstallation erfolgt auf dieselbe Weise wie die Installation, Sie müssen jedoch den Parameter `-Force` hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="7ba8f-169">Reinstalling is done the same way as installing, but you need to add the `-Force` parameter:</span></span>

```powershell
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Force
}
```

<span data-ttu-id="7ba8f-170">Im Gegensatz zu MSI-basierten Installationen werden bei der Installation oder Aktualisierung mithilfe von PowerShellGet frühere Versionen nicht entfernt, die unter Umständen auf Ihrem System vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-170">Unlike MSI-based installations, installing or updating using PowerShellGet does not remove older versions that may exist on your system.</span></span> <span data-ttu-id="7ba8f-171">Wenn Sie frühere Versionen von Azure PowerShell von Ihrem System entfernen möchten, helfen Ihnen die Informationen unter [Deinstallieren des Azure PowerShell-Moduls](uninstall-az-ps.md) weiter.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-171">To remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span> <span data-ttu-id="7ba8f-172">Weitere Informationen zu MSI-basierten Installationen finden Sie unter [Installieren von Azure PowerShell mit einer MSI](install-az-ps-msi.md).</span><span class="sxs-lookup"><span data-stu-id="7ba8f-172">For more information about MSI-based installations, see [Install Azure PowerShell with an MSI](install-az-ps-msi.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="7ba8f-173">Verwenden von mehreren Versionen von Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="7ba8f-173">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="7ba8f-174">Es ist möglich, mehr als eine Version von Azure PowerShell zu installieren.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-174">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="7ba8f-175">Verwenden Sie den folgenden Befehl zum Überprüfen, ob Sie mehrere Versionen von Azure PowerShell installiert haben:</span><span class="sxs-lookup"><span data-stu-id="7ba8f-175">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | Select-Object -Property Name, Version
```

<span data-ttu-id="7ba8f-176">Anweisungen zum Entfernen einer Version von Azure PowerShell finden Sie unter [Deinstallieren des Azure PowerShell-Moduls](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="7ba8f-176">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="7ba8f-177">Sind mehrere Versionen des Moduls installiert, wird mit der Funktion zum automatischen Laden von Modulen und mit `Import-Module` standardmäßig die neueste Version geladen.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-177">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

<span data-ttu-id="7ba8f-178">Sie können eine bestimmte Version des `Az`-Moduls mithilfe des Parameters `-RequiredVersion` installieren oder laden:</span><span class="sxs-lookup"><span data-stu-id="7ba8f-178">You can install or load a specific version of the `Az` module using the `-RequiredVersion` parameter:</span></span>

```powershell-interactive
# Install Az version 3.6.1
Install-Module -Name Az -RequiredVersion 3.6.1
# Load Az version 3.6.1
Import-Module -Name Az -RequiredVersion 3.6.1
```

## <a name="use-multiple-repositories-with-powershellget"></a><span data-ttu-id="7ba8f-179">Verwenden mehrerer Repositorys mit PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="7ba8f-179">Use multiple repositories with PowerShellGet</span></span>

<span data-ttu-id="7ba8f-180">Der Parameter **Repository** ist erforderlich, wenn Sie PowerShellGet auf Ihrem System zusätzliche Repositorys hinzugefügt haben und das Az-Modul in mehr als einem davon vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-180">The **Repository** parameter is required if you have added additional repositories to PowerShellGet on your system and the Az module can be found in more than one of them.</span></span>

```powershell-interactive
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message 'Az module not installed. Having both the AzureRM and Az modules installed at the same time is not supported.'
} else {
    Install-Module -Name Az -Repository PSGallery -AllowClobber -Force
}
```

## <a name="provide-feedback"></a><span data-ttu-id="7ba8f-181">Feedback geben</span><span class="sxs-lookup"><span data-stu-id="7ba8f-181">Provide feedback</span></span>

<span data-ttu-id="7ba8f-182">[Melden Sie auf GitHub ein Problem](https://github.com/Azure/azure-powershell/issues), wenn Sie in Azure PowerShell einen Fehler finden.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-182">If you find a bug in Azure PowerShell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="7ba8f-183">Verwenden Sie das [Send-Feedback](/powershell/module/az.accounts/send-feedback)-Cmdlet, um über die Befehlszeile Feedback zu senden.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-183">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="7ba8f-184">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="7ba8f-184">Next Steps</span></span>

<span data-ttu-id="7ba8f-185">Weitere Informationen zu Azure PowerShell-Modulen und den zugehörigen Features finden Sie unter [Erste Schritte mit Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="7ba8f-185">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span> <span data-ttu-id="7ba8f-186">Falls Sie mit Azure PowerShell vertraut sind und die Migration aus AzureRM durchführen möchten, hilft Ihnen der Artikel [Migrieren von AzureRM zum Az-Modul von Azure PowerShell](migrate-from-azurerm-to-az.md) weiter.</span><span class="sxs-lookup"><span data-stu-id="7ba8f-186">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
