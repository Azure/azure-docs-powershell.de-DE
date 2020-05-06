---
title: Andere Installationsmöglichkeiten für Azure PowerShell
description: Installieren von Azure PowerShell ohne PowerShellGet per MSI
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: 82375cc4267f468f562d138c4cdec6131e34ae32
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2020
ms.locfileid: "65534516"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a><span data-ttu-id="1dc55-103">Installieren von Azure PowerShell unter Windows per MSI</span><span class="sxs-lookup"><span data-stu-id="1dc55-103">Install Azure PowerShell on Windows with MSI</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="1dc55-104">In diesem Artikel erfahren Sie, wie Sie Azure PowerShell unter Windows mit einem MSI-Installationsprogramm installieren.</span><span class="sxs-lookup"><span data-stu-id="1dc55-104">This article explains how to install Azure PowerShell on Windows using an MSI installer.</span></span>  
<span data-ttu-id="1dc55-105">Verwenden Sie diese Installationsmethoden nur, wenn sie für Ihr System erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="1dc55-105">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="1dc55-106">Die empfohlene Vorgehensweise zum Installieren von Azure PowerShell unter Windows ist die Verwendung von PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="1dc55-106">The recommended way to install Azure PowerShell on Windows is with PowerShellGet.</span></span> <span data-ttu-id="1dc55-107">Eine Anleitung für die Installation von Azure PowerShell unter Verwendung von PowerShellGet finden Sie unter [Installieren von Azure PowerShell mit PowerShellGet](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="1dc55-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

> [!NOTE]
> <span data-ttu-id="1dc55-108">Die Vorgehensweise mit dem Webplattform-Installer für die Installation ist für die Versionen Azure PowerShell 6.x und höher nicht mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1dc55-108">The Web Platform Installer method of installation is no longer available for versions of Azure PowerShell 6.x and higher.</span></span> <span data-ttu-id="1dc55-109">Falls Sie den Webplattform-Installer benötigen, können Sie stattdessen die Nutzung des MSI-Installationsprogramms erwägen, oder Sie können eine frühere Version von Azure PowerShell installieren.</span><span class="sxs-lookup"><span data-stu-id="1dc55-109">If you require use of the Web Platform Installer please consider using the MSI instead, or you can install an earlier version of Azure PowerShell.</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="1dc55-110">Installieren oder Aktualisieren unter Windows mithilfe des MSI-Pakets</span><span class="sxs-lookup"><span data-stu-id="1dc55-110">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="1dc55-111">Azure PowerShell für Windows PowerShell 5.x kann mithilfe der bei [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018) verfügbaren MSI-Datei installiert werden.</span><span class="sxs-lookup"><span data-stu-id="1dc55-111">Azure PowerShell for Windows PowerShell 5.x can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span></span> <span data-ttu-id="1dc55-112">Ältere per MSI installierte Versionen von Azure-Modulen werden vom Installationsprogramm automatisch entfernt.</span><span class="sxs-lookup"><span data-stu-id="1dc55-112">If you have installed previous versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="1dc55-113">Mit dem MSI-Paket werden Module unter `${env:ProgramFiles}\WindowsPowerShell\Modules` installiert.</span><span class="sxs-lookup"><span data-stu-id="1dc55-113">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="1dc55-114">Sowohl das Modul `AzureRM` als auch das Modul `Azure` werden installiert.</span><span class="sxs-lookup"><span data-stu-id="1dc55-114">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="1dc55-115">Verwenden Sie das Modul `Azure` nur, wenn Sie mit dem klassischen Azure-Bereitstellungsmodell arbeiten.</span><span class="sxs-lookup"><span data-stu-id="1dc55-115">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="1dc55-116">Melden Sie sich mit Ihren Azure-Anmeldeinformationen an, um Azure PowerShell zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1dc55-116">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
>
> <span data-ttu-id="1dc55-117">Wenn Sie das automatische Laden von Modulen deaktiviert haben, müssen Sie das Modul manuell mit `Import-Module AzureRM` importieren.</span><span class="sxs-lookup"><span data-stu-id="1dc55-117">If you've disabled module autoloading, you need to manually import the module with `Import-Module AzureRM`.</span></span> <span data-ttu-id="1dc55-118">Aufgrund der Modulstruktur kann dieser Vorgang einige Sekunden dauern.</span><span class="sxs-lookup"><span data-stu-id="1dc55-118">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="1dc55-119">Sie müssen diesen Schritt für jede neue PowerShell-Sitzung wiederholen, die Sie starten.</span><span class="sxs-lookup"><span data-stu-id="1dc55-119">You'll need to repeat this step for every new PowerShell session you start.</span></span> <span data-ttu-id="1dc55-120">Informationen zum sitzungsübergreifenden Speichern der Azure-Anmeldung in PowerShell finden Sie unter [Speichern von Benutzeranmeldeinformationen zwischen PowerShell-Sitzungen](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="1dc55-120">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>
