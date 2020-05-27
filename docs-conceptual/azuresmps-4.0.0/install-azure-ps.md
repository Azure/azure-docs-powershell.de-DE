---
title: Installieren und Konfigurieren des Azure PowerShell-Dienstverwaltungsmoduls | Microsoft-Dokumentation
description: Hier erfahren Sie, wie Sie Azure PowerShell für die erste Verwendung installieren und konfigurieren.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/06/2017
ms.openlocfilehash: 8a04684e644fedf12613341bec99ab3a27900d7e
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "83384758"
---
# <a name="installing-the-azure-powershell-service-management-module"></a><span data-ttu-id="2b2a5-103">Installieren des Azure PowerShell-Dienstverwaltungsmoduls</span><span class="sxs-lookup"><span data-stu-id="2b2a5-103">Installing the Azure PowerShell Service Management module</span></span>

<span data-ttu-id="2b2a5-104">Die Installation von Azure PowerShell aus dem [PowerShell-Katalog](https://www.powershellgallery.com/) ist die bevorzugte Installationsmethode.</span><span class="sxs-lookup"><span data-stu-id="2b2a5-104">Installing Azure PowerShell from the [PowerShell Gallery](https://www.powershellgallery.com/) is the preferred method of installation.</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="2b2a5-105">Schritt 1: Installieren von PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="2b2a5-105">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="2b2a5-106">Für die Installation von Komponenten aus dem PowerShell-Katalog ist das PowerShellGet-Modul erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2b2a5-106">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="2b2a5-107">Stellen Sie sicher, dass Sie über die entsprechende Version von PowerShellGet verfügen und alle anderen Systemanforderungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="2b2a5-107">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="2b2a5-108">Führen Sie den folgenden Befehl aus, um zu ermitteln, ob PowerShellGet auf Ihrem System installiert ist.</span><span class="sxs-lookup"><span data-stu-id="2b2a5-108">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell
Get-InstalledModule PowerShellGet -AllVersions | Select-Object Name,Version,Path
```

<span data-ttu-id="2b2a5-109">Etwa folgende Ausgabe sollte angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="2b2a5-109">You should see something similar to the following output:</span></span>

```output
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="2b2a5-110">Falls PowerShellGet nicht installiert ist, lesen Sie [Installieren von PowerShellGet](#how-to-get-powershellget).</span><span class="sxs-lookup"><span data-stu-id="2b2a5-110">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="2b2a5-111">Schritt 2: Installieren von Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="2b2a5-111">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="2b2a5-112">Führen Sie über die Windows PowerShell-Konsole den folgenden Befehl als Administrator aus:</span><span class="sxs-lookup"><span data-stu-id="2b2a5-112">Run the following command from the Windows PowerShell console running as Administrator:</span></span>

```powershell
Install-Module Azure
```

<span data-ttu-id="2b2a5-113">Das Azure-Modul ist ein Rollupmodul für die Azure Resource Manager-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="2b2a5-113">The Azure module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="2b2a5-114">Bei der Installation des AzureRM-Moduls werden alle noch nicht installierten Azure-Module aus dem PowerShell-Katalog heruntergeladen und installiert.</span><span class="sxs-lookup"><span data-stu-id="2b2a5-114">When you install the AzureRM module, any other Azure modules that have not previously been installed will be downloaded and installed from the PowerShell Gallery.</span></span>

<span data-ttu-id="2b2a5-115">Das Azure-Dienstverwaltungsmodul nutzt zum Teil die gleichen Abhängigkeiten wie die Azure PowerShell Resource Manager-Module.</span><span class="sxs-lookup"><span data-stu-id="2b2a5-115">The Azure Service Management module shares dependencies with the Azure PowerShell Resource Manager modules.</span></span> <span data-ttu-id="2b2a5-116">Wenn Sie die Azure PowerShell Resource Manager-Module installiert haben, müssen Sie dem Installationsbefehl den Parameter `-AllowClobber` hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2b2a5-116">If you have installed the Azure PowerShell Resource Manager modules, you will need to add the `-AllowClobber` parameter to the install command.</span></span> <span data-ttu-id="2b2a5-117">So können diese gemeinsam genutzten Abhängigkeiten aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="2b2a5-117">This allows this existing shared dependencies to be updated.</span></span> <span data-ttu-id="2b2a5-118">Ohne den Parameter ist die Installation des Moduls nicht erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="2b2a5-118">Without this parameter, installation of the module fails.</span></span>

```powershell
Install-Module Azure -AllowClobber
```

<span data-ttu-id="2b2a5-119">Nach der Installation können Sie das Modul mithilfe des folgenden Befehls importieren:</span><span class="sxs-lookup"><span data-stu-id="2b2a5-119">After you install this module, you can import the module by running the following command:</span></span>

```powershell
Import-Module Azure
```

## <a name="to-use-the-cmdlets"></a><span data-ttu-id="2b2a5-120">So verwenden Sie die Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2b2a5-120">To use the cmdlets</span></span>

<span data-ttu-id="2b2a5-121">Melden Sie sich zunächst bei Ihrem Azure-Konto an, bevor Sie die Cmdlets der Azure-Dienstverwaltung verwenden.</span><span class="sxs-lookup"><span data-stu-id="2b2a5-121">To start working with the Azure Service Management cmdlets, first log on to your Azure account.</span></span> <span data-ttu-id="2b2a5-122">Führen Sie dazu den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="2b2a5-122">To log on to your account, run the following command:</span></span>

```powershell
Add-AzureAccount
```

<span data-ttu-id="2b2a5-123">Nach der Anmeldung bei Azure erstellt Azure PowerShell einen Kontext für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="2b2a5-123">After logging into Azure, Azure PowerShell creates a context for the given session.</span></span> <span data-ttu-id="2b2a5-124">Dieser Kontext enthält die Azure PowerShell-Umgebung, das Konto, den Mandanten und das Abonnement für alle Cmdlets innerhalb dieser Sitzung.</span><span class="sxs-lookup"><span data-stu-id="2b2a5-124">That context contains the Azure PowerShell environment, account, tenant, and subscription that will be used for all cmdlets within that session.</span></span> <span data-ttu-id="2b2a5-125">Nun können Sie die folgenden Module verwenden.</span><span class="sxs-lookup"><span data-stu-id="2b2a5-125">Now you are ready to use the modules below.</span></span>

## <a name="azure-service-management-cmdlets"></a><span data-ttu-id="2b2a5-126">Cmdlets der Azure-Dienstverwaltung</span><span class="sxs-lookup"><span data-stu-id="2b2a5-126">Azure Service Management cmdlets</span></span>

<span data-ttu-id="2b2a5-127">Azure PowerShell-Module werden regelmäßig aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2b2a5-127">Azure PowerShell modules are updated frequently.</span></span> <span data-ttu-id="2b2a5-128">Sollten Sie feststellen, dass die Cmdlet-Onlinehilfe Cmdlets oder Parameter enthält, die in Ihrem Modul nicht vorhanden sind, laden Sie die neueste Version des Moduls herunter, und installieren Sie sie.</span><span class="sxs-lookup"><span data-stu-id="2b2a5-128">If you notice that the online cmdlet help includes cmdlets or parameters that are not in your module, download and install the latest version of the module.</span></span> <span data-ttu-id="2b2a5-129">Geben Sie Folgendes ein, um die Version Ihres Moduls zu ermitteln: `(Get-InstalledModule Azure).Version`.</span><span class="sxs-lookup"><span data-stu-id="2b2a5-129">To find the version of your module, type: `(Get-InstalledModule Azure).Version`.</span></span>

<span data-ttu-id="2b2a5-130">Beispielskripts zur Automatisierung einiger allgemeiner Aufgaben in Azure finden Sie im [Azure Script Center](http://www.windowsazure.com/documentation/scripts/).</span><span class="sxs-lookup"><span data-stu-id="2b2a5-130">For sample scripts that can help you automate some of the common tasks in Azure, see the [Windows Azure Script Center](http://www.windowsazure.com/documentation/scripts/).</span></span>

<span data-ttu-id="2b2a5-131">Allgemeine Informationen zum Installieren, Kennenlernen, Verwenden und Anpassen von Windows PowerShell finden Sie unter [Skripterstellung mit Windows PowerShell](https://go.microsoft.com/fwlink/p/?linkid=320210).</span><span class="sxs-lookup"><span data-stu-id="2b2a5-131">For general information about installing, learning, using, and customizing Windows PowerShell, see [Scripting with Windows PowerShell](https://go.microsoft.com/fwlink/p/?linkid=320210).</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="2b2a5-132">Installieren von PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="2b2a5-132">How to get PowerShellGet</span></span>

|<span data-ttu-id="2b2a5-133">Betriebssystemversion</span><span class="sxs-lookup"><span data-stu-id="2b2a5-133">OS Version</span></span>|<span data-ttu-id="2b2a5-134">Installationsanleitung</span><span class="sxs-lookup"><span data-stu-id="2b2a5-134">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="2b2a5-135">Ich besitze Windows 10 oder Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="2b2a5-135">I have Windows 10 or Windows Server 2016</span></span>|<span data-ttu-id="2b2a5-136">In Windows Management Framework (WMF) 5.0 integriert (im Betriebssystem enthalten)</span><span class="sxs-lookup"><span data-stu-id="2b2a5-136">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="2b2a5-137">Ich möchte auf PowerShell 5 aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="2b2a5-137">I want to upgrade to PowerShell 5</span></span>|[<span data-ttu-id="2b2a5-138">Installieren Sie die aktuelle Version von WMF.</span><span class="sxs-lookup"><span data-stu-id="2b2a5-138">Install the latest version of WMF</span></span>](https://www.microsoft.com/download/details.aspx?id=54616)|
|<span data-ttu-id="2b2a5-139">Ich nutze eine Windows-Version mit PowerShell 3 oder PowerShell 4.</span><span class="sxs-lookup"><span data-stu-id="2b2a5-139">I am running on a version of Windows with PowerShell 3 or PowerShell 4</span></span>|[<span data-ttu-id="2b2a5-140">Laden Sie die PackageManagement-Module herunter.</span><span class="sxs-lookup"><span data-stu-id="2b2a5-140">Get the PackageManagement modules</span></span>](https://go.microsoft.com/fwlink/?LinkID=746217)|

<div id="helpmechoose"/>

### <a name="checking-the-version-of-azure-powershell"></a><span data-ttu-id="2b2a5-141">Überprüfen der Azure PowerShell-Version</span><span class="sxs-lookup"><span data-stu-id="2b2a5-141">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="2b2a5-142">Obwohl empfohlen wird, möglichst bald ein Upgrade auf die neueste Version auszuführen, werden verschiedene Azure PowerShell-Versionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2b2a5-142">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are support.</span></span> <span data-ttu-id="2b2a5-143">Führen Sie zum Ermitteln der installierten Azure PowerShell-Version `Get-InstalledModule Azure` in der Befehlszeile aus:</span><span class="sxs-lookup"><span data-stu-id="2b2a5-143">To determine the version of Azure PowerShell you have installed, run `Get-InstalledModule Azure` from your command line.</span></span>

```powershell
Get-InstalledModule Azure -AllVersions | Select-Object Name,Version,Path
```
