---
title: Installieren von Azure PowerShell unter Windows mit PowerShellGet
description: Anleitung für die Installation von Azure PowerShell mit PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: 616a9e14c3944e3151676d89b8a22e35d8f9d406
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/29/2018
ms.locfileid: "52586427"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="ae98b-103">Installieren von Azure PowerShell unter Windows mit PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="ae98b-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

<span data-ttu-id="ae98b-104">In diesem Artikel erfahren Sie, wie Sie die Azure PowerShell-Module in einer Windows-Umgebung unter Verwendung von PowerShellGet installieren.</span><span class="sxs-lookup"><span data-stu-id="ae98b-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment using PowerShellGet.</span></span> <span data-ttu-id="ae98b-105">PowerShellGet und die Modulverwaltung stellen die bevorzugte Installationsmethode für Azure PowerShell dar. Sie können aber auch den Webplattform-Installer oder das MSI-Paket verwenden. Entsprechende Informationen finden Sie unter [Andere Installationsmethoden](other-install.md).</span><span class="sxs-lookup"><span data-stu-id="ae98b-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="ae98b-106">Eine Anleitung zum Installieren von Azure PowerShell auf anderen Plattformen finden Sie unter [Installieren und Konfigurieren von Azure PowerShell unter macOS und Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="ae98b-106">For instructions to install Azure PowerShell on other platforms, see [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

<span data-ttu-id="ae98b-107">Das klassische Azure-Bereitstellungsmodell wird von dieser Version von Azure PowerShell nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ae98b-107">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="ae98b-108">Befolgen Sie die Anleitung unter [Installieren des Azure PowerShell-Dienstverwaltungsmoduls](/powershell/azure/servicemanagement/install-azure-ps), um Unterstützung zu klassischen Bereitstellungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ae98b-108">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

[!INCLUDE[az-replacing-azurerm](../includes/az-replacing-azurerm.md)]

## <a name="requirements"></a><span data-ttu-id="ae98b-109">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ae98b-109">Requirements</span></span>

<span data-ttu-id="ae98b-110">Ab Version 6.0 erfordert Azure PowerShell die PowerShell-Version 5.0.</span><span class="sxs-lookup"><span data-stu-id="ae98b-110">Starting with Azure PowerShell version 6.0, Azure PowerShell requires PowerShell version 5.0.</span></span> <span data-ttu-id="ae98b-111">Führen Sie den folgenden Befehl aus, um die Version von PowerShell zu prüfen, die auf Ihrem Computer ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="ae98b-111">To check the version of PowerShell running on your machine, run the following command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="ae98b-112">Falls Sie über eine veraltete Version verfügen, helfen Ihnen die Informationen unter [Aktualisieren einer vorhandenen Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell) weiter.</span><span class="sxs-lookup"><span data-stu-id="ae98b-112">If you have an outdated version, see [Upgrading existing Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ae98b-113">Das in diesem Dokument beschriebene Modul „AzureRM“ verwendet .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="ae98b-113">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="ae98b-114">Dadurch ist es nicht mit PowerShell 6.0 kompatibel, das .NET Core verwendet.</span><span class="sxs-lookup"><span data-stu-id="ae98b-114">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="ae98b-115">Wenn Sie PowerShell 6.0 verwenden, befolgen Sie die [Installationsanweisungen für macOS und Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="ae98b-115">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="ae98b-116">Installieren des Azure PowerShell-Moduls</span><span class="sxs-lookup"><span data-stu-id="ae98b-116">Install the Azure PowerShell module</span></span>

<span data-ttu-id="ae98b-117">Sie benötigen erhöhte Rechte, um Module aus dem PowerShell-Katalog installieren zu können.</span><span class="sxs-lookup"><span data-stu-id="ae98b-117">You need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="ae98b-118">Führen Sie den folgenden Befehl in einer Sitzung mit erhöhten Rechten aus, um Azure PowerShell zu installieren:</span><span class="sxs-lookup"><span data-stu-id="ae98b-118">To install Azure PowerShell, run the following command in an elevated session:</span></span>

```powershell-interactive
Install-Module -Name AzureRM -AllowClobber
```

> [!NOTE]
> <span data-ttu-id="ae98b-119">Wenn Sie eine ältere NuGet-Version als 2.8.5.201 haben, werden Sie aufgefordert, die aktuelle NuGet-Version herunterzuladen und zu installieren.</span><span class="sxs-lookup"><span data-stu-id="ae98b-119">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="ae98b-120">Standardmäßig ist der PowerShell-Katalog nicht als vertrauenswürdiges Repository für PowerShellGet konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="ae98b-120">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="ae98b-121">Bei der ersten Verwendung des PowerShell-Katalogs wird die folgende Meldung angezeigt:</span><span class="sxs-lookup"><span data-stu-id="ae98b-121">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="ae98b-122">Antworten Sie mit `Yes` oder `Yes to All`, um die Installation fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="ae98b-122">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="ae98b-123">Das Modul `AzureRM` ist ein Rollupmodul für die Azure PowerShell-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="ae98b-123">The `AzureRM` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="ae98b-124">Wenn Sie es installieren, werden alle verfügbaren Azure Resource Manager-Module heruntergeladen und die zugehörigen Cmdlets für die Nutzung zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="ae98b-124">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="ae98b-125">Anmelden</span><span class="sxs-lookup"><span data-stu-id="ae98b-125">Sign in</span></span>

<span data-ttu-id="ae98b-126">Melden Sie sich mit Ihren Azure-Anmeldeinformationen an, um Azure PowerShell zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ae98b-126">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
>
> <span data-ttu-id="ae98b-127">Wenn Sie das automatische Laden von Modulen deaktiviert haben, müssen Sie das Modul manuell mit `Import-Module AzureRM` importieren.</span><span class="sxs-lookup"><span data-stu-id="ae98b-127">If you've disabled module autoloading, you need to manually import the module with `Import-Module AzureRM`.</span></span> <span data-ttu-id="ae98b-128">Aufgrund der Modulstruktur kann dieser Vorgang einige Sekunden dauern.</span><span class="sxs-lookup"><span data-stu-id="ae98b-128">Because of the way the module is structured, this can take a few seconds.</span></span>


<span data-ttu-id="ae98b-129">Sie müssen diese Schritte für jede neue PowerShell-Sitzung wiederholen, die Sie starten.</span><span class="sxs-lookup"><span data-stu-id="ae98b-129">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="ae98b-130">Informationen zum sitzungsübergreifenden Speichern der Azure-Anmeldung in PowerShell finden Sie unter [Speichern von Benutzeranmeldeinformationen zwischen PowerShell-Sitzungen](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="ae98b-130">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="ae98b-131">Aktualisieren des Azure PowerShell-Moduls</span><span class="sxs-lookup"><span data-stu-id="ae98b-131">Update the Azure PowerShell module</span></span>

<span data-ttu-id="ae98b-132">Sie können Ihre Azure PowerShell-Installation aktualisieren, indem Sie [Update-Module](/powershell/module/powershellget/update-module) ausführen.</span><span class="sxs-lookup"><span data-stu-id="ae98b-132">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="ae98b-133">Mit diesem Befehl werden __keine__ früheren Versionen deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="ae98b-133">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name AzureRM
```

<span data-ttu-id="ae98b-134">Wenn Sie ältere Versionen von Azure PowerShell von Ihrem System entfernen möchten, helfen Ihnen die Informationen unter [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md) (Deinstallieren des Azure PowerShell-Moduls) weiter.</span><span class="sxs-lookup"><span data-stu-id="ae98b-134">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="ae98b-135">Verwenden von mehreren Versionen von Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ae98b-135">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="ae98b-136">Es ist möglich, mehr als eine Version von Azure PowerShell zu installieren.</span><span class="sxs-lookup"><span data-stu-id="ae98b-136">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="ae98b-137">Verwenden Sie den folgenden Befehl zum Überprüfen, ob Sie mehrere Versionen von Azure PowerShell installiert haben:</span><span class="sxs-lookup"><span data-stu-id="ae98b-137">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-Module -Name AzureRM -List | select Name,Version
```

<span data-ttu-id="ae98b-138">Anweisungen zum Entfernen einer Version von Azure PowerShell finden Sie unter [Deinstallieren des Azure PowerShell-Moduls](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="ae98b-138">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="ae98b-139">Unter Umständen benötigen Sie mehr als eine Version, wenn Sie mit lokalen Azure Stack-Ressourcen arbeiten, eine ältere Version von Windows ausführen oder das klassische Azure-Bereitstellungsmodell nutzen.</span><span class="sxs-lookup"><span data-stu-id="ae98b-139">You might need more than one version if you work with on-premises Azure Stack resources, run an older version of Windows, or use the Azure classic deployment model.</span></span> <span data-ttu-id="ae98b-140">Geben Sie beim Installieren das Argument `-RequiredVersion` an, um eine ältere Version zu installieren.</span><span class="sxs-lookup"><span data-stu-id="ae98b-140">To install an older version, provide the `-RequiredVersion` argument when installing.</span></span>

```powershell-interactive
# Install version 2.3.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

<span data-ttu-id="ae98b-141">Beim Laden des Azure PowerShell-Moduls wird standardmäßig die aktuelle Version geladen.</span><span class="sxs-lookup"><span data-stu-id="ae98b-141">When loading the Azure PowerShell module the latest version is loaded by default.</span></span> <span data-ttu-id="ae98b-142">Geben Sie das Argument `-RequiredVersion` an, um eine andere Version zu laden.</span><span class="sxs-lookup"><span data-stu-id="ae98b-142">To load a different version, provide the `-RequiredVersion` argument.</span></span>

```powershell-interactive
# Load version 2.3.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

## <a name="provide-feedback"></a><span data-ttu-id="ae98b-143">Feedback geben</span><span class="sxs-lookup"><span data-stu-id="ae98b-143">Provide feedback</span></span>

<span data-ttu-id="ae98b-144">[Melden Sie auf GitHub ein Problem](https://github.com/Azure/azure-powershell/issues), wenn Sie bei der Nutzung von Azure PowerShell einen Fehler finden.</span><span class="sxs-lookup"><span data-stu-id="ae98b-144">If you find a bug when using Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="ae98b-145">Verwenden Sie das [Send-Feedback](/powershell/module/azurerm.profile/send-feedback)-Cmdlet, um über die Befehlszeile Feedback zu senden.</span><span class="sxs-lookup"><span data-stu-id="ae98b-145">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ae98b-146">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="ae98b-146">Next Steps</span></span>

<span data-ttu-id="ae98b-147">Weitere Informationen zum Modul und zu den zugehörigen Features als Einstieg in die Nutzung von Azure PowerShell finden Sie unter [Get started with Azure PowerShell](get-started-azureps.md) (Erste Schritte mit Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="ae98b-147">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>