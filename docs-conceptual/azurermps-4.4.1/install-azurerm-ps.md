---
title: Installieren und Konfigurieren von Azure PowerShell | Microsoft-Dokumentation
description: Hier erfahren Sie, wie Sie Azure PowerShell für die erste Verwendung installieren und konfigurieren.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/27/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 3f4b05352ef5e5c7f32495d002a78aadd3e056e1
ms.sourcegitcommit: 038cb42a3bd8c009bc57c8c1c252e66fa170c84b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2020
ms.locfileid: "92523290"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="6f44f-103">Installieren von Azure PowerShell unter Windows mit PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="6f44f-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="6f44f-104">In diesem Artikel erfahren Sie, wie Sie die Azure PowerShell-Module für PowerShell 5.x für Windows mit PowerShellGet installieren.</span><span class="sxs-lookup"><span data-stu-id="6f44f-104">This article explains the steps to install the Azure PowerShell modules for PowerShell 5.x for Windows using PowerShellGet.</span></span> <span data-ttu-id="6f44f-105">PowerShellGet und die Modulverwaltung stellen die bevorzugte Installationsmethode für Azure PowerShell dar. Sie können aber auch den Webplattform-Installer oder das MSI-Paket verwenden. Entsprechende Informationen finden Sie unter [Andere Installationsmethoden](other-install.md).</span><span class="sxs-lookup"><span data-stu-id="6f44f-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="6f44f-106">Das klassische Azure-Bereitstellungsmodell wird von dieser Version von Azure PowerShell nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6f44f-106">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="6f44f-107">Befolgen Sie die Anleitung unter [Installieren des Azure PowerShell-Dienstverwaltungsmoduls](/powershell/azure/servicemanagement/install-azure-ps), um Unterstützung zu klassischen Bereitstellungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6f44f-107">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6f44f-108">Das AzureRM-Modul wird für macOS oder Linux nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6f44f-108">The AzureRM module is not supported for macOS or Linux.</span></span> <span data-ttu-id="6f44f-109">Wenn Sie Azure PowerShell-Cmdlets auf diesen Plattformen verwenden möchten, [installieren Sie das Az-Modul](/powershell/azure/install-az-ps).</span><span class="sxs-lookup"><span data-stu-id="6f44f-109">To use Azure PowerShell cmdlets on these platforms, [Install the Az module](/powershell/azure/install-az-ps).</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="6f44f-110">Schritt 1: Installieren von PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="6f44f-110">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="6f44f-111">Für die Installation von Komponenten aus dem PowerShell-Katalog ist das PowerShellGet-Modul erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6f44f-111">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="6f44f-112">Stellen Sie sicher, dass Sie über die entsprechende Version von PowerShellGet verfügen und alle anderen Systemanforderungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="6f44f-112">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="6f44f-113">Führen Sie den folgenden Befehl aus, um zu ermitteln, ob PowerShellGet auf Ihrem System installiert ist.</span><span class="sxs-lookup"><span data-stu-id="6f44f-113">Run the following command to see if you have PowerShellGet installed on your system.</span></span>


```powershell-interactive
Get-InstalledModule -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="6f44f-114">Etwa folgende Ausgabe sollte angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="6f44f-114">You should see something similar to the following output:</span></span>

```Output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="6f44f-115">Sie benötigen mindestens die PowerShellGet-Version 1.1.2.0.</span><span class="sxs-lookup"><span data-stu-id="6f44f-115">You need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="6f44f-116">Verwenden Sie zum Aktualisieren von PowerShellGet den folgenden Befehl:</span><span class="sxs-lookup"><span data-stu-id="6f44f-116">To update PowerShellGet, use the following command:</span></span>

```powershell-interactive
Install-Module PowerShellGet -Force
```

<span data-ttu-id="6f44f-117">Falls PowerShellGet nicht installiert ist, lesen Sie die Informationen im Abschnitt [Installieren von PowerShellGet](#how-to-get-powershellget) dieses Artikels.</span><span class="sxs-lookup"><span data-stu-id="6f44f-117">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget) section of this article.</span></span>

> [!NOTE]
> <span data-ttu-id="6f44f-118">Für die Verwendung von PowerShellGet ist eine Ausführungsrichtlinie erforderlich, die die Ausführung von Skripts ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="6f44f-118">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="6f44f-119">Weitere Informationen zur Ausführungsrichtlinie von PowerShell finden Sie unter [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies) (Informationen zu Ausführungsrichtlinien).</span><span class="sxs-lookup"><span data-stu-id="6f44f-119">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>
>
> [!IMPORTANT]
> <span data-ttu-id="6f44f-120">Das in diesem Dokument beschriebene Modul „AzureRM“ verwendet .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="6f44f-120">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="6f44f-121">Dadurch ist es nicht mit PowerShell 6.0 kompatibel, das .NET Core verwendet.</span><span class="sxs-lookup"><span data-stu-id="6f44f-121">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="6f44f-122">Wenn Sie PowerShell 6.0 verwenden, befolgen Sie die [Installationsanweisungen für macOS und Linux](/powershell/azure/install-az-ps).</span><span class="sxs-lookup"><span data-stu-id="6f44f-122">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](/powershell/azure/install-az-ps).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="6f44f-123">Schritt 2: Installieren von Azure Powershell</span><span class="sxs-lookup"><span data-stu-id="6f44f-123">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="6f44f-124">Für die Installation von Azure PowerShell aus dem PowerShell-Katalog sind erhöhte Rechte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6f44f-124">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="6f44f-125">Führen Sie den folgenden Befehl in einer PowerShell-Sitzung mit erhöhten Rechten aus:</span><span class="sxs-lookup"><span data-stu-id="6f44f-125">Run the following command from an elevated PowerShell session:</span></span>

```powershell-interactive
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="6f44f-126">Standardmäßig ist der PowerShell-Katalog nicht als vertrauenswürdiges Repository für PowerShellGet konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="6f44f-126">By default, the PowerShell gallery is not configured as a Trusted repository for PowerShellGet.</span></span> <span data-ttu-id="6f44f-127">Bei der ersten Verwendung des PowerShell-Katalogs wird die folgende Meldung angezeigt:</span><span class="sxs-lookup"><span data-stu-id="6f44f-127">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

<span data-ttu-id="6f44f-128">Antworten Sie mit „Ja“ oder „Ja zu allen“, um die Installation fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="6f44f-128">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="6f44f-129">Wenn Sie eine ältere NuGet-Version als 2.8.5.201 haben, werden Sie aufgefordert, die aktuelle NuGet-Version herunterzuladen und zu installieren.</span><span class="sxs-lookup"><span data-stu-id="6f44f-129">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="6f44f-130">Das AzureRM-Modul ist ein Rollupmodul für die Azure Resource Manager-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="6f44f-130">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="6f44f-131">Bei der Installation des AzureRM-Moduls werden alle noch nicht installierten Azure PowerShell-Module aus dem PowerShell-Katalog heruntergeladen und installiert.</span><span class="sxs-lookup"><span data-stu-id="6f44f-131">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded and from the PowerShell Gallery.</span></span>

<span data-ttu-id="6f44f-132">Wenn eine frühere Version von Azure PowerShell installiert ist, erhalten Sie möglicherweise eine Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="6f44f-132">If you have a previous version of Azure PowerShell installed you may receive an error.</span></span> <span data-ttu-id="6f44f-133">Informationen zum Beheben dieses Problem finden Sie im Abschnitt [Aktualisieren auf eine neue Version von Azure PowerShell](#update-azps) dieses Artikels.</span><span class="sxs-lookup"><span data-stu-id="6f44f-133">To resolve this issue, see the [Updating to a new version of Azure PowerShell](#update-azps) section of this article.</span></span>

## <a name="step-3-load-the-azurerm-module"></a><span data-ttu-id="6f44f-134">Schritt 3: Laden des AzureRM-Moduls</span><span class="sxs-lookup"><span data-stu-id="6f44f-134">Step 3: Load the AzureRM module</span></span>

<span data-ttu-id="6f44f-135">Nach der Installation des Moduls müssen Sie das Modul in der PowerShell-Sitzung laden.</span><span class="sxs-lookup"><span data-stu-id="6f44f-135">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="6f44f-136">Dies muss in einer normalen PowerShell-Sitzung (ohne erhöhte Rechte) erfolgen.</span><span class="sxs-lookup"><span data-stu-id="6f44f-136">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="6f44f-137">Module werden wie folgt mit dem Cmdlet `Import-Module` geladen:</span><span class="sxs-lookup"><span data-stu-id="6f44f-137">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell-interactive
Import-Module -Name AzureRM
```

## <a name="next-steps"></a><span data-ttu-id="6f44f-138">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="6f44f-138">Next Steps</span></span>

<span data-ttu-id="6f44f-139">Weitere Informationen zur Verwendung von Azure PowerShell finden Sie in den folgenden Artikeln:</span><span class="sxs-lookup"><span data-stu-id="6f44f-139">For more information about using Azure PowerShell, see the following articles:</span></span>

* [<span data-ttu-id="6f44f-140">Erste Schritte mit Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="6f44f-140">Get started with Azure PowerShell</span></span>](get-started-azureps.md)

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="6f44f-141">Melden von Problemen und Bereitstellen von Feedback</span><span class="sxs-lookup"><span data-stu-id="6f44f-141">Reporting issues and feedback</span></span>

<span data-ttu-id="6f44f-142">Wenn mit dem Tool Fehler auftreten, legen Sie einen Eintrag im Bereich [Probleme](https://github.com/Azure/azure-powershell/issues) unseres GitHub Repositorys an.</span><span class="sxs-lookup"><span data-stu-id="6f44f-142">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-powershell/issues) section of our GitHub repo.</span></span> <span data-ttu-id="6f44f-143">Zum Senden von Feedback zur Befehlszeile verwenden Sie das Cmdlet `Send-Feedback`.</span><span class="sxs-lookup"><span data-stu-id="6f44f-143">To provide feedback from the command line, use the `Send-Feedback` cmdlet.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="6f44f-144">Häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="6f44f-144">Frequently asked questions</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="6f44f-145">Installieren von PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="6f44f-145">How to get PowerShellGet</span></span>

|<span data-ttu-id="6f44f-146">Betriebssystemversion</span><span class="sxs-lookup"><span data-stu-id="6f44f-146">OS Version</span></span>|<span data-ttu-id="6f44f-147">Installationsanleitung</span><span class="sxs-lookup"><span data-stu-id="6f44f-147">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="6f44f-148">Ich besitze Windows 10 oder Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="6f44f-148">I have Windows 10 or Windows Server 2016</span></span>|<span data-ttu-id="6f44f-149">In Windows Management Framework (WMF) 5.0 integriert (im Betriebssystem enthalten)</span><span class="sxs-lookup"><span data-stu-id="6f44f-149">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="6f44f-150">Ich möchte auf PowerShell 5 aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="6f44f-150">I want to upgrade to PowerShell 5</span></span>|[<span data-ttu-id="6f44f-151">Installieren Sie die aktuelle Version von WMF.</span><span class="sxs-lookup"><span data-stu-id="6f44f-151">Install the latest version of WMF</span></span>](https://www.microsoft.com/download/details.aspx?id=54616)|

### <a name="div-idhelpmechoosechecking-the-version-of-azure-powershell"></a><div id="helpmechoose"/><span data-ttu-id="6f44f-152">Überprüfen der Azure PowerShell-Version</span><span class="sxs-lookup"><span data-stu-id="6f44f-152">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="6f44f-153">Obwohl empfohlen wird, möglichst bald ein Upgrade auf die neueste Version auszuführen, werden verschiedene Azure PowerShell-Versionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6f44f-153">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are supported.</span></span> <span data-ttu-id="6f44f-154">Führen Sie zum Ermitteln der installierten Azure PowerShell-Version `Get-InstalledModule AzureRM` in der Befehlszeile aus:</span><span class="sxs-lookup"><span data-stu-id="6f44f-154">To determine the version of Azure PowerShell you have installed, run `Get-InstalledModule AzureRM` from your command line.</span></span>

```powershell-interactive
Get-InstalledModule AzureRM -AllVersions | Select-Object -Property Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a><span data-ttu-id="6f44f-155">Unterstützung für klassische Bereitstellungsmethoden</span><span class="sxs-lookup"><span data-stu-id="6f44f-155">Support for classic deployment methods</span></span>

<span data-ttu-id="6f44f-156">Bei Bereitstellungen mit dem klassischen Bereitstellungsmodell können Sie die Dienstverwaltungsversion von Azure PowerShell installieren.</span><span class="sxs-lookup"><span data-stu-id="6f44f-156">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="6f44f-157">Weitere Informationen finden Sie unter [Installing the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps) (Installieren des Azure PowerShell-Dienstverwaltungsmoduls).</span><span class="sxs-lookup"><span data-stu-id="6f44f-157">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="6f44f-158">Das Azure- und das AzureRM-Modul nutzen gemeinsame Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="6f44f-158">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="6f44f-159">Wenn Sie sowohl die Azure- als auch die AzureRM-Module verwenden, müssen Sie die gleiche Version der einzelnen Pakete installieren.</span><span class="sxs-lookup"><span data-stu-id="6f44f-159">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a name="div-idupdate-azpsupdating-to-a-new-version-of-azure-powershell"></a><div id="update-azps"/><span data-ttu-id="6f44f-160">Aktualisieren auf eine neue Version von Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="6f44f-160">Updating to a new version of Azure PowerShell</span></span>

<span data-ttu-id="6f44f-161">Wenn Sie eine frühere Version von Azure PowerShell installiert haben, die das Dienstverwaltungsmodul enthält, kann die folgende Fehlermeldung angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="6f44f-161">If you have a previous version of Azure PowerShell installed that includes the Service Management module, you may receive the following error:</span></span>

```Output
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

<span data-ttu-id="6f44f-162">Wie in der Fehlermeldung angegeben, müssen Sie den Parameter „-AllowClobber“ zum Installieren des Moduls verwenden.</span><span class="sxs-lookup"><span data-stu-id="6f44f-162">As the error message states, you need to use the -AllowClobber parameter to install the module.</span></span> <span data-ttu-id="6f44f-163">Verwenden Sie den folgenden Befehl:</span><span class="sxs-lookup"><span data-stu-id="6f44f-163">Use the following command:</span></span>

```powershell-interactive
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="6f44f-164">Weitere Informationen finden Sie im Hilfethema zu [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span><span class="sxs-lookup"><span data-stu-id="6f44f-164">For more information, see the help topic for [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span></span>

### <a name="installing-module-versions-side-by-side"></a><span data-ttu-id="6f44f-165">Parallele Installation von Modulversionen</span><span class="sxs-lookup"><span data-stu-id="6f44f-165">Installing module versions side by side</span></span>

<span data-ttu-id="6f44f-166">Die PowerShellGet-Installationsmethode ist die einzige Methode, die die Installation mehrerer Versionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6f44f-166">The PowerShellGet method of installation is the only method that supports the installation of multiple versions.</span></span> <span data-ttu-id="6f44f-167">Beispiel: Sie besitzen Skripts, die mit einer vorherigen Version von Azure PowerShell geschrieben wurden, für deren Aktualisierung keine Zeit ist bzw. keine Ressourcen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="6f44f-167">For example, you may have scripts written using a previous version of Azure PowerShell that you don't have the time or resources to updated.</span></span> <span data-ttu-id="6f44f-168">Die folgenden Befehle veranschaulichen, wie mehrere Versionen von Azure PowerShell installiert werden:</span><span class="sxs-lookup"><span data-stu-id="6f44f-168">The following commands illustrate how to install multiple versions of Azure PowerShell:</span></span>

```powershell-interactive
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

<span data-ttu-id="6f44f-169">Nur eine Version des Moduls kann in einer PowerShell-Sitzung geladen werden.</span><span class="sxs-lookup"><span data-stu-id="6f44f-169">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="6f44f-170">Sie müssen ein neues PowerShell-Fenster öffnen und `Import-Module` verwenden, um eine bestimmte Version der AzureRM-Cmdlets zu importieren:</span><span class="sxs-lookup"><span data-stu-id="6f44f-170">You must open a new PowerShell window and use `Import-Module` to import a specific version of the AzureRM cmdlets:</span></span>

```powershell-interactive
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

> [!NOTE]
> <span data-ttu-id="6f44f-171">Version 2.1.0 und Version 1.2.6 sind die ersten Modulversionen, die parallel installiert und genutzt werden können.</span><span class="sxs-lookup"><span data-stu-id="6f44f-171">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="6f44f-172">Beim Laden einer früheren Version von Azure PowerShell werden inkompatible Versionen des **AzureRM.Profile** -Moduls geladen.</span><span class="sxs-lookup"><span data-stu-id="6f44f-172">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="6f44f-173">Dies führt dazu, dass Sie, immer wenn Sie ein Cmdlet ausführen, zum Anmelden aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="6f44f-173">This results in the cmdlets prompting you to sign in whenever you execute a cmdlet.</span></span>

### <a name="other-installation-methods"></a><span data-ttu-id="6f44f-174">Andere Installationsmethoden</span><span class="sxs-lookup"><span data-stu-id="6f44f-174">Other installation methods</span></span>

<span data-ttu-id="6f44f-175">Information zum Installieren des Webplattform-Installers oder des MSI-Pakets finden Sie unter [Other installation methods](other-install.md) (Andere Installationsmethoden).</span><span class="sxs-lookup"><span data-stu-id="6f44f-175">For information about installing using the Web Platform Installer or the MSI Package, see [Other installation methods](other-install.md)</span></span>
