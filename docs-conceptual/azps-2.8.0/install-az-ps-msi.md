---
title: Installieren von Azure PowerShell mit einer MSI
description: Installieren von Azure PowerShell ohne PowerShellGet per MSI
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/22/2019
ms.openlocfilehash: 0c1576d669daa63becb0197c29e623a0a26960be
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2020
ms.locfileid: "83386900"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a><span data-ttu-id="d2186-103">Installieren von Azure PowerShell unter Windows per MSI</span><span class="sxs-lookup"><span data-stu-id="d2186-103">Install Azure PowerShell on Windows with MSI</span></span>

<span data-ttu-id="d2186-104">In diesem Artikel erfahren Sie, wie Sie Azure PowerShell unter Windows mit einem MSI-Installationsprogramm installieren.</span><span class="sxs-lookup"><span data-stu-id="d2186-104">This article explains how to install Azure PowerShell on Windows using an MSI installer.</span></span> <span data-ttu-id="d2186-105">Das MSI-Installationsprogramm wird für Umgebungen bereitgestellt, in denen der PowerShell-Katalog unter Umständen durch eine Firewall blockiert oder in denen ein Offlineinstallationsprogramm benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="d2186-105">The MSI installer is provided for environments where the PowerShell Gallery may be blocked by a firewall, or an offline installer is needed.</span></span> <span data-ttu-id="d2186-106">Die empfohlene Vorgehensweise zum Installieren von Azure PowerShell ist die Verwendung von PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="d2186-106">The recommended way to install Azure PowerShell is with PowerShellGet.</span></span> <span data-ttu-id="d2186-107">Eine Anleitung für die Installation von Azure PowerShell unter Verwendung von PowerShellGet finden Sie unter [Installieren von Azure PowerShell mit PowerShellGet](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="d2186-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-az-ps.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d2186-108">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="d2186-108">Requirements</span></span>

<span data-ttu-id="d2186-109">Das MSI-Installationsprogramm für Azure PowerShell funktioniert __nur__ für PowerShell 5.1 unter Windows.</span><span class="sxs-lookup"><span data-stu-id="d2186-109">The MSI installer for Azure PowerShell works __only__ for PowerShell 5.1 on Windows.</span></span> <span data-ttu-id="d2186-110">Verwenden Sie zur Installation auf Nicht-Windows-Plattformen oder unter höheren Versionen von PowerShell [PowerShellGet](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="d2186-110">For installation on non-Windows platforms or later versions of powershell, [Install with PowerShellGet](install-az-ps.md).</span></span>
<span data-ttu-id="d2186-111">Führen Sie den Befehl aus, um Ihre PowerShell-Version zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="d2186-111">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="d2186-112">Für die Verwendung von Azure PowerShell in PowerShell 5.1 ist Folgendes erforderlich:</span><span class="sxs-lookup"><span data-stu-id="d2186-112">To use Azure PowerShell in PowerShell 5.1, you need to:</span></span>

1. <span data-ttu-id="d2186-113">Führen Sie bei Bedarf ein Update auf [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) aus.</span><span class="sxs-lookup"><span data-stu-id="d2186-113">Update to [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="d2186-114">Unter Windows 10 ist PowerShell 5.1 bereits installiert.</span><span class="sxs-lookup"><span data-stu-id="d2186-114">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="d2186-115">Installieren Sie [.NET Framework 4.7.2 oder höher](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="d2186-115">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="d2186-116">Installieren oder Aktualisieren unter Windows mithilfe des MSI-Pakets</span><span class="sxs-lookup"><span data-stu-id="d2186-116">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="d2186-117">Azure PowerShell für Windows wird mithilfe der auf [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v2.8.0-October2019) verfügbaren MSI-Datei installiert.</span><span class="sxs-lookup"><span data-stu-id="d2186-117">Azure PowerShell for Windows is installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v2.8.0-October2019).</span></span> <span data-ttu-id="d2186-118">Ältere per MSI installierte Versionen von Azure-Modulen werden vom Installationsprogramm automatisch entfernt.</span><span class="sxs-lookup"><span data-stu-id="d2186-118">If you have installed earlier versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="d2186-119">Mit dem MSI-Paket werden Module unter `${env:ProgramFiles}\WindowsPowerShell\Modules` installiert.</span><span class="sxs-lookup"><span data-stu-id="d2186-119">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span>

<span data-ttu-id="d2186-120">Melden Sie sich mit Ihren Azure-Anmeldeinformationen an, um Azure PowerShell zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d2186-120">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="d2186-121">Wenn Sie das automatische Laden von Modulen deaktiviert haben, müssen Sie das Modul manuell mit `Import-Module Az` importieren.</span><span class="sxs-lookup"><span data-stu-id="d2186-121">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="d2186-122">Aufgrund der Modulstruktur kann dieser Vorgang bis zu einer Minute dauern.</span><span class="sxs-lookup"><span data-stu-id="d2186-122">Because of the way the module is structured, this can take up to a minute.</span></span>

<span data-ttu-id="d2186-123">Sie müssen diesen Schritt für jede neue PowerShell-Sitzung wiederholen, die Sie starten.</span><span class="sxs-lookup"><span data-stu-id="d2186-123">You'll need to repeat this step for every new PowerShell session you start.</span></span> <span data-ttu-id="d2186-124">Informationen zum sitzungsübergreifenden Speichern der Azure-Anmeldung in PowerShell finden Sie unter [Speichern von Benutzeranmeldeinformationen zwischen PowerShell-Sitzungen](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="d2186-124">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="d2186-125">Feedback geben</span><span class="sxs-lookup"><span data-stu-id="d2186-125">Provide feedback</span></span>

<span data-ttu-id="d2186-126">[Melden Sie auf GitHub ein Problem](https://github.com/Azure/azure-powershell/issues), wenn Sie in Azure PowerShell einen Fehler finden.</span><span class="sxs-lookup"><span data-stu-id="d2186-126">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="d2186-127">Verwenden Sie das [Send-Feedback](/powershell/module/az.accounts/send-feedback)-Cmdlet, um über die Befehlszeile Feedback zu senden.</span><span class="sxs-lookup"><span data-stu-id="d2186-127">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d2186-128">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="d2186-128">Next Steps</span></span>

<span data-ttu-id="d2186-129">Weitere Informationen zu Azure PowerShell-Modulen und den zugehörigen Features finden Sie unter [Erste Schritte mit Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="d2186-129">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="d2186-130">Falls Sie mit Azure PowerShell vertraut sind und die Migration aus AzureRM durchführen möchten, hilft Ihnen der Artikel [Migrieren von AzureRM zum Az-Modul von Azure PowerShell](migrate-from-azurerm-to-az.md) weiter.</span><span class="sxs-lookup"><span data-stu-id="d2186-130">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
