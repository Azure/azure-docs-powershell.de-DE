---
title: Andere Installationsmöglichkeiten für Azure PowerShell | Microsoft-Dokumentation
description: Hier erfahren Sie, wie Sie Azure PowerShell mithilfe des MSI-Pakets oder des Webplattform-Installers installieren.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/06/2017
ms.openlocfilehash: 7e59a5188dee3801a1305a693b2df8af63425eb5
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2018
ms.locfileid: "51211637"
---
# <a name="other-installation-methods"></a><span data-ttu-id="4d3a0-103">Andere Installationsmethoden</span><span class="sxs-lookup"><span data-stu-id="4d3a0-103">Other installation methods</span></span>

<span data-ttu-id="4d3a0-104">Für Azure PowerShell stehen unterschiedliche Installationsmethoden zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="4d3a0-104">Azure PowerShell has multiple installation methods.</span></span> <span data-ttu-id="4d3a0-105">Bevorzugt wird die Kombination aus „PowerShellGet“ und PowerShell-Katalog.</span><span class="sxs-lookup"><span data-stu-id="4d3a0-105">Using PowerShellGet with the PowerShell Gallery is the preferred method.</span></span> <span data-ttu-id="4d3a0-106">Azure PowerShell kann mithilfe des Webplattform-Installers (WebPI) oder unter Verwendung der bei GitHub verfügbaren MSI-Datei unter Windows installiert werden.</span><span class="sxs-lookup"><span data-stu-id="4d3a0-106">Azure PowerShell can be installed on Windows using the Web Platform Installer (WebPI) or by using the MSI file available from GitHub.</span></span>
 
## <a name="install-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="4d3a0-107">Installieren unter Windows mit dem Webplattform-Installer</span><span class="sxs-lookup"><span data-stu-id="4d3a0-107">Install on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="4d3a0-108">Die Vorgehensweise zum Installieren der neuesten Azure PowerShell-Version über WebPI hat sich im Vergleich zu früheren Versionen nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="4d3a0-108">Installing the latest Azure PowerShell from WebPI is the same as it was for previous versions.</span></span>
<span data-ttu-id="4d3a0-109">Laden Sie das [Azure PowerShell-WebPI-Paket](http://aka.ms/webpi-azps) herunter, und starten Sie die Installation.</span><span class="sxs-lookup"><span data-stu-id="4d3a0-109">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span>

> [!NOTE]
> <span data-ttu-id="4d3a0-110">Wenn Sie bereits Azure-Module aus dem PowerShell-Katalog installiert haben, entfernt das Installationsprogramm diese automatisch.</span><span class="sxs-lookup"><span data-stu-id="4d3a0-110">If you have previously installed Azure modules from the PowerShell Gallery, the installer automatically removes them.</span></span> <span data-ttu-id="4d3a0-111">Dadurch wird sichergestellt, dass nur eine einzelne Version von Azure PowerShell installiert ist, was Ihre Umgebung vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="4d3a0-111">This simplifies your environment by ensuring that only one version of Azure PowerShell is installed.</span></span> <span data-ttu-id="4d3a0-112">Es gibt jedoch Szenarien, in denen mehrere gleichzeitig installierte Versionen benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="4d3a0-112">However, there are scenarios where you may need multiple versions installed at the same time.</span></span>
>
> <span data-ttu-id="4d3a0-113">PowerShell-Katalogmodule werden unter `$env:ProgramFiles\WindowsPowerShell\Modules` installiert.</span><span class="sxs-lookup"><span data-stu-id="4d3a0-113">PowerShell Gallery modules install modules in `$env:ProgramFiles\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="4d3a0-114">Der WebPI-Installer installiert Azure-Module dagegen unter `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span><span class="sxs-lookup"><span data-stu-id="4d3a0-114">In contrast, the WebPI installer installs the Azure modules in `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span></span>
>
> <span data-ttu-id="4d3a0-115">Im Falle eines Installationsfehlers können Sie die Azure\*-Ordner aus dem Ordner `$env:ProgramFiles\WindowsPowerShell\Modules` entfernen und die Installation wiederholen.</span><span class="sxs-lookup"><span data-stu-id="4d3a0-115">If an error occurs during install, you can manually remove the Azure\* folders in your `$env:ProgramFiles\WindowsPowerShell\Modules` folder, and try the installation again.</span></span>

<span data-ttu-id="4d3a0-116">Nach Abschluss der Installation sollte Ihre `$env:PSModulePath` -Einstellung die Verzeichnisse mit den Azure PowerShell-Cmdlets enthalten.</span><span class="sxs-lookup"><span data-stu-id="4d3a0-116">Once the installation completes, your `$env:PSModulePath` setting should include the directories containing the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="4d3a0-117">Mit dem folgenden Befehl können Sie überprüfen, ob Azure PowerShell ordnungsgemäß installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="4d3a0-117">The following command can be used to verify that the Azure PowerShell is installed properly.</span></span>

```powershell-interactive
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> <span data-ttu-id="4d3a0-118">Es gibt ein bekanntes Problem, das bei der Installation per WebPI auftreten kann.</span><span class="sxs-lookup"><span data-stu-id="4d3a0-118">There is a known issue that can occur when installing from WebPI.</span></span> <span data-ttu-id="4d3a0-119">Wenn Ihr Computer aufgrund von Systemupdates oder anderen Installationen neu gestartet werden muss, wird bei Updates für `$env:PSModulePath` unter Umständen der Installationspfad von Azure PowerShell nicht einbezogen.</span><span class="sxs-lookup"><span data-stu-id="4d3a0-119">If your computer requires a restart due to system updates or other installations, it may cause updates to `$env:PSModulePath` to fail to include the path where Azure PowerShell is installed.</span></span>

<span data-ttu-id="4d3a0-120">Nach der Installation wird beim Ladevorgang oder beim Ausführen von Cmdlets möglicherweise folgende Fehlermeldung angezeigt:</span><span class="sxs-lookup"><span data-stu-id="4d3a0-120">When attempting to load or execute cmdlets after installation, you can receive the following error message:</span></span>

```output
PS C:\> Login-AzureRmAccount
Login-AzureRmAccount : The term 'Login-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Login-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Login-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

<span data-ttu-id="4d3a0-121">Starten Sie zum Beheben dieses Fehlers den Computer neu, oder importieren Sie das Modul unter Verwendung des vollqualifizierten Pfads.</span><span class="sxs-lookup"><span data-stu-id="4d3a0-121">This error can be corrected by restarting the machine or importing the module using the fully qualified path.</span></span> <span data-ttu-id="4d3a0-122">Beispiel: </span><span class="sxs-lookup"><span data-stu-id="4d3a0-122">For example:</span></span>

```powershell-interactive
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-on-windows-using-the-msi-package"></a><span data-ttu-id="4d3a0-123">Installieren unter Windows mithilfe des MSI-Pakets</span><span class="sxs-lookup"><span data-stu-id="4d3a0-123">Install on Windows using the MSI Package</span></span>

<span data-ttu-id="4d3a0-124">Azure PowerShell kann mithilfe der bei [GitHub](https://github.com/Azure/azure-powershell/releases/latest) verfügbaren MSI-Datei installiert werden.</span><span class="sxs-lookup"><span data-stu-id="4d3a0-124">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span></span> <span data-ttu-id="4d3a0-125">Ältere installierte Versionen von Azure-Modulen werden vom Installationsprogramm automatisch entfernt.</span><span class="sxs-lookup"><span data-stu-id="4d3a0-125">If you have installed previous versions of Azure modules, the installer automatically removes them.</span></span> <span data-ttu-id="4d3a0-126">Das MSI-Paket installiert Module unter `$env:ProgramFiles\WindowsPowerShell\Modules`, erstellt aber keine versionsspezifischen Ordner.</span><span class="sxs-lookup"><span data-stu-id="4d3a0-126">The MSI package installs modules in `$env:ProgramFiles\WindowsPowerShell\Modules` but does not create version-specific folders.</span></span>

