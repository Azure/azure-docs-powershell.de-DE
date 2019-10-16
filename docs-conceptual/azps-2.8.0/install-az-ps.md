---
title: Installieren von Azure PowerShell mit PowerShellGet
description: Anleitung für die Installation von Azure PowerShell mit PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: e302e49d95b6bc15750366c9eb960a6fec80c1a4
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/15/2019
ms.locfileid: "72370338"
---
# <a name="install-the-azure-powershell-module"></a><span data-ttu-id="059df-103">Installieren des Azure PowerShell-Moduls</span><span class="sxs-lookup"><span data-stu-id="059df-103">Install the Azure PowerShell module</span></span>

<span data-ttu-id="059df-104">In diesem Artikel erfahren Sie, wie Sie mithilfe von „PowerShellGet“ die Azure PowerShell-Module installieren.</span><span class="sxs-lookup"><span data-stu-id="059df-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="059df-105">Diese Anweisungen können für Windows-, macOS- und Linux-Plattformen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="059df-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="059df-106">Für das Az-Modul werden derzeit keine anderen Installationsmethoden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="059df-106">For the Az module, currently no other installation methods are supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="059df-107">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="059df-107">Requirements</span></span>

<span data-ttu-id="059df-108">Azure PowerShell kann mit PowerShell 5.1 oder höher unter Windows oder mit PowerShell Core 6.x und höher auf allen Plattformen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="059df-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell Core 6.x and later on all platforms.</span></span> <span data-ttu-id="059df-109">Wenn Sie sich nicht sicher sind, ob Sie über PowerShell verfügen oder unter MacOS oder Linux arbeiten, [installieren Sie die neueste Version von PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span><span class="sxs-lookup"><span data-stu-id="059df-109">If you aren't sure if you have PowerShell, or are on macOS or Linux, [install the latest version of PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span></span>

<span data-ttu-id="059df-110">Führen Sie den Befehl aus, um Ihre PowerShell-Version zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="059df-110">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="059df-111">So führen Sie Azure PowerShell in PowerShell 5.1 unter Windows aus</span><span class="sxs-lookup"><span data-stu-id="059df-111">To run Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="059df-112">Führen Sie bei Bedarf ein Update auf [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) aus.</span><span class="sxs-lookup"><span data-stu-id="059df-112">Update to [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="059df-113">Unter Windows 10 ist PowerShell 5.1 bereits installiert.</span><span class="sxs-lookup"><span data-stu-id="059df-113">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="059df-114">Installieren Sie [.NET Framework 4.7.2 oder höher](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="059df-114">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

<span data-ttu-id="059df-115">Bei Verwendung von PowerShell Core gibt es keine zusätzlichen Anforderungen an Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="059df-115">There are no additional requirements for Azure PowerShell when using PowerShell Core.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="059df-116">Installieren des Azure PowerShell-Moduls</span><span class="sxs-lookup"><span data-stu-id="059df-116">Install the Azure PowerShell module</span></span>

> [!WARNING]
> <span data-ttu-id="059df-117">Die Module AzureRM und Az können für PowerShell 5.1 für Windows __nicht__ gleichzeitig installiert sein.</span><span class="sxs-lookup"><span data-stu-id="059df-117">You __can't__ have both the AzureRM and Az modules installed for PowerShell 5.1 for Windows at the same time.</span></span> <span data-ttu-id="059df-118">Wenn AzureRM weiterhin auf Ihrem System verfügbar sein soll, installieren Sie das Az-Modul für PowerShell Core 6.x oder höher.</span><span class="sxs-lookup"><span data-stu-id="059df-118">If you need to keep AzureRM available on your system, install the Az module for PowerShell Core 6.x or later.</span></span> <span data-ttu-id="059df-119">Installieren Sie dazu [PowerShell Core 6.x oder höher](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows), und befolgen Sie dann diese Anweisungen in einem PowerShell Core-Terminal.</span><span class="sxs-lookup"><span data-stu-id="059df-119">To do this, [install PowerShell Core 6.x or later](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows) and then follow these instructions in a PowerShell Core terminal.</span></span>

<span data-ttu-id="059df-120">Es wird empfohlen, die Installation nur für den aktiven Benutzer auszuführen:</span><span class="sxs-lookup"><span data-stu-id="059df-120">The recommended install method is to only install for the active user:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="059df-121">Für die Installation für alle Benutzer in einem System sind Administratorberechtigungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="059df-121">If you want to install for all users on a system, this requires administrator privileges.</span></span> <span data-ttu-id="059df-122">Führen Sie unter macOS oder Linux Folgendes in einer PowerShell-Sitzung mit erhöhten Rechten aus (entweder als Administrator oder mithilfe des Befehls `sudo`):</span><span class="sxs-lookup"><span data-stu-id="059df-122">From an elevated PowerShell session either run as administrator or with the `sudo` command on macOS or Linux:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope AllUsers
```

<span data-ttu-id="059df-123">Standardmäßig ist der PowerShell-Katalog nicht als vertrauenswürdiges Repository für PowerShellGet konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="059df-123">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="059df-124">Bei der ersten Verwendung des PowerShell-Katalogs wird die folgende Meldung angezeigt:</span><span class="sxs-lookup"><span data-stu-id="059df-124">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="059df-125">Antworten Sie mit `Yes` oder `Yes to All`, um die Installation fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="059df-125">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="059df-126">Das Az-Modul ist ein Rollupmodul für die Azure PowerShell-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="059df-126">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="059df-127">Wenn Sie es installieren, werden alle verfügbaren Azure Resource Manager-Module heruntergeladen und die zugehörigen Cmdlets für die Nutzung zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="059df-127">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="059df-128">Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="059df-128">Troubleshooting</span></span>

<span data-ttu-id="059df-129">In diesem Abschnitt finden Sie einige allgemeine Probleme, die bei der Installation des Azure PowerShell-Moduls auftreten können.</span><span class="sxs-lookup"><span data-stu-id="059df-129">Here are some common problems seen when installing the Azure PowerShell module.</span></span> <span data-ttu-id="059df-130">Falls ein Problem auftritt, das hier nicht aufgeführt ist, [melden Sie es auf GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="059df-130">If you experience a problem not listed here, please [file an issue on GitHub](https://github.com/azure/azure-powershell/issues).</span></span>

### <a name="proxy-blocks-connection"></a><span data-ttu-id="059df-131">Der Proxy blockiert die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="059df-131">Proxy blocks connection</span></span>

<span data-ttu-id="059df-132">Wenn Sie von `Install-Module` Fehler erhalten, die anzeigen, dass der PowerShell-Katalog nicht erreichbar ist, befinden Sie sich möglicherweise hinter einem Proxy.</span><span class="sxs-lookup"><span data-stu-id="059df-132">If you get errors from `Install-Module` that indicate the PowerShell Gallery is unreachable, you may be behind a proxy.</span></span> <span data-ttu-id="059df-133">Verschiedene Betriebssysteme haben unterschiedliche Anforderungen an die Konfiguration eines systemweiten Proxys, die hier nicht ausführlich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="059df-133">Different operating systems will have different requirements for configuring a system-wide proxy, which are not covered in detail here.</span></span> <span data-ttu-id="059df-134">Wenden Sie sich an Ihren Systemadministrator, um Ihre Proxyeinstellungen zu erhalten und zu erfahren, wie Sie sie für Ihr Betriebssystem konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="059df-134">Contact your system administrator for your proxy settings and how to configure them for your OS.</span></span>

<span data-ttu-id="059df-135">PowerShell selbst ist möglicherweise nicht so konfiguriert, dass es diesen Proxy automatisch verwendet.</span><span class="sxs-lookup"><span data-stu-id="059df-135">PowerShell itself may not be configured to use this proxy automatically.</span></span> <span data-ttu-id="059df-136">Konfigurieren Sie den Proxy für PowerShell 5.1 und höher mit dem folgenden Befehl so, dass er eine PowerShell-Sitzung verwendet:</span><span class="sxs-lookup"><span data-stu-id="059df-136">With PowerShell 5.1 and later, configure the proxy to use for a PowerShell session with the following command:</span></span>

```powershell
(New-Object System.Net.WebClient).Proxy.Credentials = `
  [System.Net.CredentialCache]::DefaultNetworkCredentials
```

<span data-ttu-id="059df-137">Wenn die Anmeldeinformationen Ihres Betriebssystems ordnungsgemäß konfiguriert sind, werden PowerShell-Anforderungen über den Proxy weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="059df-137">If your operating system credentials are configured correctly, this will route PowerShell requests through the proxy.</span></span>
<span data-ttu-id="059df-138">Damit diese Einstellung auch zwischen den Sitzungen erhalten bleibt, fügen Sie den Befehl zu einem [PowerShell-Profil](/powershell/module/microsoft.powershell.core/about/about_profiles) hinzu.</span><span class="sxs-lookup"><span data-stu-id="059df-138">In order to have this setting persist between sessions, add the command to a [PowerShell profile](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>

<span data-ttu-id="059df-139">Ihr Proxy muss HTTPS-Verbindungen zu der folgenden Adresse zulassen, damit das Paket installiert werden kann:</span><span class="sxs-lookup"><span data-stu-id="059df-139">In order to install the package, your proxy needs to allow HTTPS connections to the following address:</span></span>

* `https://www.powershellgallery.com`

## <a name="sign-in"></a><span data-ttu-id="059df-140">Anmelden</span><span class="sxs-lookup"><span data-stu-id="059df-140">Sign in</span></span>

<span data-ttu-id="059df-141">Melden Sie sich mit Ihren Azure-Anmeldeinformationen an, um Azure PowerShell zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="059df-141">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="059df-142">Wenn Sie das automatische Laden von Modulen deaktiviert haben, importieren Sie das Modul manuell mit `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="059df-142">If you've disabled module autoloading, manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="059df-143">Aufgrund der Modulstruktur kann dieser Vorgang einige Sekunden dauern.</span><span class="sxs-lookup"><span data-stu-id="059df-143">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="059df-144">Sie müssen diese Schritte für jede neue PowerShell-Sitzung wiederholen, die Sie starten.</span><span class="sxs-lookup"><span data-stu-id="059df-144">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="059df-145">Informationen zum sitzungsübergreifenden Speichern der Azure-Anmeldung in PowerShell finden Sie unter [Speichern von Benutzeranmeldeinformationen zwischen PowerShell-Sitzungen](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="059df-145">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="059df-146">Aktualisieren des Azure PowerShell-Moduls</span><span class="sxs-lookup"><span data-stu-id="059df-146">Update the Azure PowerShell module</span></span>

<span data-ttu-id="059df-147">Aufgrund der Art und Weise, wie das Az-Modul gepackt ist, aktualisiert der Befehl [Update-Module](/powershell/module/powershellget/update-module) Ihre Installation nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="059df-147">Because of how the Az module is packaged, the [Update-Module](/powershell/module/powershellget/update-module) command won't update your installation correctly.</span></span> <span data-ttu-id="059df-148">Bei der Installation des Az-Moduls werden alle abhängigen Submodule gesammelt und installiert und dadurch die Cmdlets für jeden Dienst bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="059df-148">When you install the Az module, it actually collects and installs all of its dependent submodules, and which provide the cmdlets for each service.</span></span>
<span data-ttu-id="059df-149">Das bedeutet, dass zum Aktualisieren des Azure PowerShell-Moduls eine __Neuinstallation__ und keine __Aktualisierung__ erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="059df-149">That means that to update the Azure PowerShell module, you will need to __reinstall__, rather than just __update__.</span></span> <span data-ttu-id="059df-150">Dies erfolgt auf dieselbe Weise wie bei der Installation, aber Sie müssen möglicherweise das Argument `-Force` hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="059df-150">This is done in the same way as installing, but you may need to add the `-Force` argument:</span></span>

```powershell
Install-Module -Name Az -AllowClobber -Force
```

<span data-ttu-id="059df-151">Obwohl dadurch installierte Module überschrieben werden können, verbleiben möglicherweise noch ältere Versionen auf Ihrem System.</span><span class="sxs-lookup"><span data-stu-id="059df-151">Although this can overwrite installed modules, you may still have older versions left on your system.</span></span>
<span data-ttu-id="059df-152">Wenn Sie frühere Versionen von Azure PowerShell von Ihrem System entfernen möchten, helfen Ihnen die Informationen unter [Deinstallieren des Azure PowerShell-Moduls](uninstall-az-ps.md) weiter.</span><span class="sxs-lookup"><span data-stu-id="059df-152">To learn how to remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="059df-153">Verwenden von mehreren Versionen von Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="059df-153">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="059df-154">Es ist möglich, mehr als eine Version von Azure PowerShell zu installieren.</span><span class="sxs-lookup"><span data-stu-id="059df-154">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="059df-155">Verwenden Sie den folgenden Befehl zum Überprüfen, ob Sie mehrere Versionen von Azure PowerShell installiert haben:</span><span class="sxs-lookup"><span data-stu-id="059df-155">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="059df-156">Anweisungen zum Entfernen einer Version von Azure PowerShell finden Sie unter [Deinstallieren des Azure PowerShell-Moduls](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="059df-156">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="059df-157">Wenn Sie eine bestimmte Version des `Az`-Moduls installieren oder laden möchten, können Sie das Argument `-RequiredVersion` verwenden:</span><span class="sxs-lookup"><span data-stu-id="059df-157">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` argument:</span></span>

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

<span data-ttu-id="059df-158">Sind mehrere Versionen des Moduls installiert, wird mit der Funktion zum automatischen Laden von Modulen und mit `Import-Module` standardmäßig die neueste Version geladen.</span><span class="sxs-lookup"><span data-stu-id="059df-158">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="059df-159">Feedback geben</span><span class="sxs-lookup"><span data-stu-id="059df-159">Provide feedback</span></span>

<span data-ttu-id="059df-160">[Melden Sie auf GitHub ein Problem](https://github.com/Azure/azure-powershell/issues), wenn Sie in Azure PowerShell einen Fehler finden.</span><span class="sxs-lookup"><span data-stu-id="059df-160">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="059df-161">Verwenden Sie das [Send-Feedback](/powershell/module/az.accounts/send-feedback)-Cmdlet, um über die Befehlszeile Feedback zu senden.</span><span class="sxs-lookup"><span data-stu-id="059df-161">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="059df-162">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="059df-162">Next Steps</span></span>

<span data-ttu-id="059df-163">Weitere Informationen zu Azure PowerShell-Modulen und den zugehörigen Features finden Sie unter [Erste Schritte mit Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="059df-163">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="059df-164">Falls Sie mit Azure PowerShell vertraut sind und die Migration aus AzureRM durchführen möchten, hilft Ihnen der Artikel [Migrieren von AzureRM zum Az-Modul von Azure PowerShell](migrate-from-azurerm-to-az.md) weiter.</span><span class="sxs-lookup"><span data-stu-id="059df-164">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
