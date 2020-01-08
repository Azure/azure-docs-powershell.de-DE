---
title: Installieren von Azure PowerShell unter Windows mit PowerShellGet
description: Anleitung für die Installation von Azure PowerShell mit PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/15/2018
ms.openlocfilehash: 5a4ccd67433fe3716df42075a4e2fd035a12af2b
ms.sourcegitcommit: 2d0c3ffaa5246f680784fa7e15b0d2536c27ff80
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2020
ms.locfileid: "75722440"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="25e3b-103">Installieren von Azure PowerShell unter Windows mit PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="25e3b-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="25e3b-104">In diesem Artikel erfahren Sie, wie Sie die Azure PowerShell-Module für PowerShell 5.x für Windows mit PowerShellGet installieren.</span><span class="sxs-lookup"><span data-stu-id="25e3b-104">This article explains the steps to install the Azure PowerShell modules for PowerShell 5.x for Windows using PowerShellGet.</span></span> <span data-ttu-id="25e3b-105">PowerShellGet und die Modulverwaltung stellen die bevorzugte Installationsmethode für Azure PowerShell dar. Sie können aber auch den Webplattform-Installer oder das MSI-Paket verwenden. Entsprechende Informationen finden Sie unter [Andere Installationsmethoden](other-install.md).</span><span class="sxs-lookup"><span data-stu-id="25e3b-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="25e3b-106">Das klassische Azure-Bereitstellungsmodell wird von dieser Version von Azure PowerShell nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="25e3b-106">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="25e3b-107">Befolgen Sie die Anleitung unter [Installieren des Azure PowerShell-Dienstverwaltungsmoduls](/powershell/azure/servicemanagement/install-azure-ps), um Unterstützung zu klassischen Bereitstellungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="25e3b-107">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="25e3b-108">Das AzureRM-Modul wird für macOS oder Linux nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="25e3b-108">The AzureRM module is not supported for macOS or Linux.</span></span> <span data-ttu-id="25e3b-109">Wenn Sie Azure PowerShell-Cmdlets auf diesen Plattformen verwenden möchten, [installieren Sie das Az-Modul](/powershell/azure/install-az-ps).</span><span class="sxs-lookup"><span data-stu-id="25e3b-109">To use Azure PowerShell cmdlets on these platforms, [Install the Az module](/powershell/azure/install-az-ps).</span></span>

## <a name="requirements"></a><span data-ttu-id="25e3b-110">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="25e3b-110">Requirements</span></span>

<span data-ttu-id="25e3b-111">Für die Installation von Azure PowerShell benötigen Sie PowerShellGet Version 1.1.2.0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="25e3b-111">To install Azure PowerShell, you need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="25e3b-112">Führen Sie den folgenden Befehl aus, um zu prüfen, ob diese Version unter Ihrem System verfügbar ist:</span><span class="sxs-lookup"><span data-stu-id="25e3b-112">To check if it is available on your system, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name PowerShellGet -AllVersions | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="25e3b-113">Etwa folgende Ausgabe sollte angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="25e3b-113">You should see something similar to the following output:</span></span>

```output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="25e3b-114">Führen Sie den folgenden Befehl aus, wenn Sie Ihre Installation von PowerShellGet aktualisieren müssen:</span><span class="sxs-lookup"><span data-stu-id="25e3b-114">If you need to update your installation of PowerShellGet, run the following command:</span></span>

```powershell-interactive
Install-Module PowerShellGet -Force
```

<span data-ttu-id="25e3b-115">Befolgen Sie die Anleitung unten in der Tabelle, falls Sie PowerShellGet nicht installiert haben.</span><span class="sxs-lookup"><span data-stu-id="25e3b-115">If you don't have PowerShellGet installed, follow the instructions in the table below for your system.</span></span>

|<span data-ttu-id="25e3b-116">Szenario</span><span class="sxs-lookup"><span data-stu-id="25e3b-116">Scenario</span></span>|<span data-ttu-id="25e3b-117">Installationsanleitung</span><span class="sxs-lookup"><span data-stu-id="25e3b-117">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="25e3b-118">Windows 10</span><span class="sxs-lookup"><span data-stu-id="25e3b-118">Windows 10</span></span><br/><span data-ttu-id="25e3b-119">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="25e3b-119">Windows Server 2016</span></span>|<span data-ttu-id="25e3b-120">In Windows Management Framework (WMF) 5.0 integriert (im Betriebssystem enthalten)</span><span class="sxs-lookup"><span data-stu-id="25e3b-120">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="25e3b-121">Upgrade auf PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="25e3b-121">Upgrade to PowerShell 5</span></span>| <ol><li>[<span data-ttu-id="25e3b-122">Installieren Sie die aktuelle Version von WMF.</span><span class="sxs-lookup"><span data-stu-id="25e3b-122">Install the latest version of WMF</span></span>](https://www.microsoft.com/download/details.aspx?id=54616)</li><li><span data-ttu-id="25e3b-123">Führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="25e3b-123">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|
|<span data-ttu-id="25e3b-124">Windows mit PowerShell 3 oder PowerShell 4</span><span class="sxs-lookup"><span data-stu-id="25e3b-124">Windows with PowerShell 3 or PowerShell 4</span></span>|<ol><span data-ttu-id="25e3b-125"><il>[Laden Sie die PackageManagement-Module herunter.](https://go.microsoft.com/fwlink/?LinkID=746217)</il></span><span class="sxs-lookup"><span data-stu-id="25e3b-125"><il>[Get the PackageManagement modules](https://go.microsoft.com/fwlink/?LinkID=746217)</il></span></span><li><span data-ttu-id="25e3b-126">Führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="25e3b-126">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|

> [!NOTE]
> <span data-ttu-id="25e3b-127">Für die Verwendung von PowerShellGet ist eine Ausführungsrichtlinie erforderlich, die die Ausführung von Skripts ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="25e3b-127">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="25e3b-128">Weitere Informationen zur Ausführungsrichtlinie von PowerShell finden Sie unter [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies) (Informationen zu Ausführungsrichtlinien).</span><span class="sxs-lookup"><span data-stu-id="25e3b-128">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>
>
> [!IMPORTANT]
> <span data-ttu-id="25e3b-129">Das in diesem Dokument beschriebene Modul „AzureRM“ verwendet .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="25e3b-129">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="25e3b-130">Dadurch ist es nicht mit PowerShell 6.0 kompatibel, das .NET Core verwendet.</span><span class="sxs-lookup"><span data-stu-id="25e3b-130">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="25e3b-131">Wenn Sie PowerShell 6.0 verwenden, befolgen Sie die [Installationsanweisungen für macOS und Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="25e3b-131">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="25e3b-132">Installieren des Azure PowerShell-Moduls</span><span class="sxs-lookup"><span data-stu-id="25e3b-132">Install the Azure PowerShell module</span></span>

<span data-ttu-id="25e3b-133">Sie benötigen erhöhte Rechte, um Module aus dem PowerShell-Katalog installieren zu können.</span><span class="sxs-lookup"><span data-stu-id="25e3b-133">You need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="25e3b-134">Führen Sie den folgenden Befehl in einer Sitzung mit erhöhten Rechten aus, um Azure PowerShell zu installieren:</span><span class="sxs-lookup"><span data-stu-id="25e3b-134">To install Azure PowerShell, run the following command in an elevated session:</span></span>

```powershell-interactive
Install-Module -Name AzureRM
```

> [!NOTE]
> <span data-ttu-id="25e3b-135">Wenn Sie eine ältere NuGet-Version als 2.8.5.201 haben, werden Sie aufgefordert, die aktuelle NuGet-Version herunterzuladen und zu installieren.</span><span class="sxs-lookup"><span data-stu-id="25e3b-135">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="25e3b-136">Standardmäßig ist der PowerShell-Katalog nicht als vertrauenswürdiges Repository für PowerShellGet konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="25e3b-136">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="25e3b-137">Bei der ersten Verwendung des PowerShell-Katalogs wird die folgende Meldung angezeigt:</span><span class="sxs-lookup"><span data-stu-id="25e3b-137">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="25e3b-138">Antworten Sie mit `Yes` oder `Yes to All`, um die Installation fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="25e3b-138">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="25e3b-139">Das Modul `AzureRM` ist ein Rollupmodul für die Azure PowerShell-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="25e3b-139">The `AzureRM` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="25e3b-140">Wenn Sie es installieren, werden alle verfügbaren Azure Resource Manager-Module heruntergeladen und die zugehörigen Cmdlets für die Nutzung zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="25e3b-140">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="25e3b-141">Anmelden</span><span class="sxs-lookup"><span data-stu-id="25e3b-141">Sign in</span></span>

<span data-ttu-id="25e3b-142">Damit Sie Azure PowerShell verwenden können, müssen Sie `AzureRM` mit dem [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module)-Cmdlet in Ihre aktuelle PowerShell-Sitzung laden und sich dann mit Ihren Azure-Anmeldeinformationen anmelden.</span><span class="sxs-lookup"><span data-stu-id="25e3b-142">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="25e3b-143">Sie müssen diese Schritte für jede neue PowerShell-Sitzung wiederholen, die Sie starten.</span><span class="sxs-lookup"><span data-stu-id="25e3b-143">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="25e3b-144">Für den automatischen Import des Moduls `AzureRM` muss ein PowerShell-Profil eingerichtet werden. Informationen hierzu finden Sie unter [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles) (Informationen zu Profilen).</span><span class="sxs-lookup"><span data-stu-id="25e3b-144">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="25e3b-145">Informationen zum sitzungsübergreifenden Speichern der Azure-Anmeldung finden Sie unter [Persisting user credentials across PowerShell sessions](context-persistence.md) (Speichern von Benutzeranmeldeinformationen zwischen PowerShell-Sitzungen).</span><span class="sxs-lookup"><span data-stu-id="25e3b-145">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="25e3b-146">Aktualisieren des Azure PowerShell-Moduls</span><span class="sxs-lookup"><span data-stu-id="25e3b-146">Update the Azure PowerShell module</span></span>

<span data-ttu-id="25e3b-147">Sie können Ihre Azure PowerShell-Installation aktualisieren, indem Sie [Update-Module](/powershell/module/powershellget/update-module) ausführen.</span><span class="sxs-lookup"><span data-stu-id="25e3b-147">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="25e3b-148">Mit diesem Befehl werden __keine__ früheren Versionen deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="25e3b-148">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name AzureRM
```

<span data-ttu-id="25e3b-149">Wenn Sie ältere Versionen von Azure PowerShell von Ihrem System entfernen möchten, helfen Ihnen die Informationen unter [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md) (Deinstallieren des Azure PowerShell-Moduls) weiter.</span><span class="sxs-lookup"><span data-stu-id="25e3b-149">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="25e3b-150">Verwenden von mehreren Versionen von Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="25e3b-150">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="25e3b-151">Es ist möglich, mehrere Versionen von Azure PowerShell zu installieren.</span><span class="sxs-lookup"><span data-stu-id="25e3b-151">It's possible to install multiple versions of Azure PowerShell.</span></span> <span data-ttu-id="25e3b-152">Unter Umständen benötigen Sie mehr als eine Version, wenn Sie mit lokalen Azure Stack-Ressourcen arbeiten, eine ältere Version von Windows ausführen, die nicht auf PowerShell 5.0 aktualisiert werden kann, oder das klassische Azure-Bereitstellungsmodell nutzen.</span><span class="sxs-lookup"><span data-stu-id="25e3b-152">You might need more than one version if you work with on-premises Azure Stack resources, run an older version of Windows that you can't update to PowerShell 5.0, or use the Azure classic deployment model.</span></span> <span data-ttu-id="25e3b-153">Geben Sie beim Installieren das Argument `-RequiredVersion` an, um eine ältere Version zu installieren.</span><span class="sxs-lookup"><span data-stu-id="25e3b-153">To install an older version, provide the `-RequiredVersion` argument when installing.</span></span>

```powershell-interactive
# Install version 2.3.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

<span data-ttu-id="25e3b-154">Beim Laden des Azure PowerShell-Moduls wird standardmäßig die aktuelle Version geladen.</span><span class="sxs-lookup"><span data-stu-id="25e3b-154">When loading the Azure PowerShell module the latest version is loaded by default.</span></span> <span data-ttu-id="25e3b-155">Geben Sie das Argument `-RequiredVersion` an, um eine andere Version zu laden.</span><span class="sxs-lookup"><span data-stu-id="25e3b-155">To load a different version, provide the `-RequiredVersion` argument.</span></span>

```powershell-interactive
# Load version 2.3.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

## <a name="provide-feedback"></a><span data-ttu-id="25e3b-156">Feedback geben</span><span class="sxs-lookup"><span data-stu-id="25e3b-156">Provide feedback</span></span>

<span data-ttu-id="25e3b-157">Bitte [melden Sie auf GitHub ein Problem](https://github.com/Azure/azure-powershell/issues), wenn Sie bei der Nutzung von Azure PowerShell einen Fehler finden.</span><span class="sxs-lookup"><span data-stu-id="25e3b-157">If you find a bug when using Azure Powershell, please [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="25e3b-158">Verwenden Sie das [Send-Feedback](/powershell/module/azurerm.profile/send-feedback)-Cmdlet, um über die Befehlszeile Feedback zu senden.</span><span class="sxs-lookup"><span data-stu-id="25e3b-158">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="25e3b-159">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="25e3b-159">Next Steps</span></span>

<span data-ttu-id="25e3b-160">Weitere Informationen zum Modul und zu den zugehörigen Features als Einstieg in die Nutzung von Azure PowerShell finden Sie unter [Get started with Azure PowerShell](get-started-azureps.md) (Erste Schritte mit Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="25e3b-160">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>
