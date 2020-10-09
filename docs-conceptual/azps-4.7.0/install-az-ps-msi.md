---
title: Installieren von Azure PowerShell mit einer MSI
description: Installieren von Azure PowerShell ohne PowerShellGet per MSI
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 193e8c5d14f1bf2fe9c84a9da2defac50be97ec7
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "91833269"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a><span data-ttu-id="f62c5-103">Installieren von Azure PowerShell unter Windows per MSI</span><span class="sxs-lookup"><span data-stu-id="f62c5-103">Install Azure PowerShell on Windows with MSI</span></span>

<span data-ttu-id="f62c5-104">In diesem Artikel erfahren Sie, wie Sie Azure PowerShell unter Windows mit einem MSI-Installationsprogramm installieren.</span><span class="sxs-lookup"><span data-stu-id="f62c5-104">This article explains how to install Azure PowerShell on Windows using an MSI installer.</span></span> <span data-ttu-id="f62c5-105">Das MSI-Installationsprogramm wird für Umgebungen bereitgestellt, in denen der PowerShell-Katalog unter Umständen durch eine Firewall blockiert oder in denen ein Offlineinstallationsprogramm benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="f62c5-105">The MSI installer is provided for environments where the PowerShell Gallery may be blocked by a firewall, or an offline installer is needed.</span></span> <span data-ttu-id="f62c5-106">Die empfohlene Vorgehensweise zum Installieren von Azure PowerShell ist die Verwendung von PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="f62c5-106">The recommended way to install Azure PowerShell is with PowerShellGet.</span></span> <span data-ttu-id="f62c5-107">Eine Anleitung für die Installation von Azure PowerShell unter Verwendung von PowerShellGet finden Sie unter [Installieren von Azure PowerShell mit PowerShellGet](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="f62c5-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-az-ps.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f62c5-108">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="f62c5-108">Requirements</span></span>

<span data-ttu-id="f62c5-109">Das MSI-Installationsprogramm unter Windows ist nur für die Installation von Azure PowerShell für PowerShell 5.1 konzipiert.</span><span class="sxs-lookup"><span data-stu-id="f62c5-109">The MSI installer on Windows is designed to install Azure PowerShell for PowerShell 5.1 only.</span></span> <span data-ttu-id="f62c5-110">Verwenden Sie zur Installation auf Nicht-Windows-Plattformen oder unter höheren Versionen von PowerShell [PowerShellGet](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="f62c5-110">For installation on non-Windows platforms or later versions of PowerShell, [Install with PowerShellGet](install-az-ps.md).</span></span> <span data-ttu-id="f62c5-111">Führen Sie den Befehl aus, um Ihre PowerShell-Version zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="f62c5-111">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="f62c5-112">Für die Verwendung von Azure PowerShell in PowerShell 5.1 ist Folgendes erforderlich:</span><span class="sxs-lookup"><span data-stu-id="f62c5-112">To use Azure PowerShell in PowerShell 5.1, you need to:</span></span>

1. <span data-ttu-id="f62c5-113">Führen Sie bei Bedarf ein Update auf [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell) aus.</span><span class="sxs-lookup"><span data-stu-id="f62c5-113">Update to [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="f62c5-114">Unter Windows 10 ist PowerShell 5.1 bereits installiert.</span><span class="sxs-lookup"><span data-stu-id="f62c5-114">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="f62c5-115">Installieren Sie [.NET Framework 4.7.2 oder höher](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="f62c5-115">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="f62c5-116">Installieren oder Aktualisieren unter Windows mithilfe des MSI-Pakets</span><span class="sxs-lookup"><span data-stu-id="f62c5-116">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="f62c5-117">Das MSI-Paket für Azure PowerShell ist auf [GitHub](https://github.com/Azure/azure-powershell/releases) verfügbar:</span><span class="sxs-lookup"><span data-stu-id="f62c5-117">The MSI package for Azure PowerShell is available from [GitHub](https://github.com/Azure/azure-powershell/releases):</span></span>

1. <span data-ttu-id="f62c5-118">Gehe zu https://github.com/Azure/azure-powershell/releases.</span><span class="sxs-lookup"><span data-stu-id="f62c5-118">Go to https://github.com/Azure/azure-powershell/releases.</span></span>
2. <span data-ttu-id="f62c5-119">Suchen Sie nach dem aktuellen Katalogmodul für Azure PowerShell (diese sind chronologisch aufgelistet und in der Regel nur als Releaseversion ohne Namen, z. B. „4.7.0“).</span><span class="sxs-lookup"><span data-stu-id="f62c5-119">Look for the most recent Gallery Module for Azure PowerShell (these are listed chronologically and are typically just a release version with no name like "4.7.0").</span></span>
3. <span data-ttu-id="f62c5-120">Scrollen Sie zum unteren Rand der Patchnotizen, und klicken Sie auf den Pfeil neben „Ressourcen“, um die MSI-Optionen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f62c5-120">Scroll down to the bottom of the patch notes and click on the arrow next to "Assets" to reveal the MSI options.</span></span>
4. <span data-ttu-id="f62c5-121">Klicken Sie auf die MSI-Datei der Az-Cmdlets Ihrer Wahl, um den Download zu starten.</span><span class="sxs-lookup"><span data-stu-id="f62c5-121">Click on the Az-Cmdlets MSI of your choice to start the download.</span></span>

<span data-ttu-id="f62c5-122">Ältere per MSI installierte Versionen von Azure PowerShell werden vom Installationsprogramm automatisch entfernt.</span><span class="sxs-lookup"><span data-stu-id="f62c5-122">If you have installed earlier versions of Azure PowerShell using the MSI, the installer automatically removes them.</span></span> <span data-ttu-id="f62c5-123">Mit dem MSI-Paket werden Module unter `${env:ProgramFiles}\WindowsPowerShell\Modules` installiert.</span><span class="sxs-lookup"><span data-stu-id="f62c5-123">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span>

<span data-ttu-id="f62c5-124">Melden Sie sich mit Ihren Azure-Anmeldeinformationen an, um Azure PowerShell zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f62c5-124">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzAccount
```

> [!NOTE]
> <span data-ttu-id="f62c5-125">Wenn Sie das automatische Laden von Modulen deaktiviert haben, müssen Sie das Modul manuell mit `Import-Module Az` importieren.</span><span class="sxs-lookup"><span data-stu-id="f62c5-125">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="f62c5-126">Aufgrund der Modulstruktur kann dieser Vorgang bis zu einer Minute dauern.</span><span class="sxs-lookup"><span data-stu-id="f62c5-126">Because of the way the module is structured, this can take up to a minute.</span></span>

<span data-ttu-id="f62c5-127">Sie müssen diesen Schritt für jede neue PowerShell-Sitzung wiederholen, die Sie starten.</span><span class="sxs-lookup"><span data-stu-id="f62c5-127">You'll need to repeat this step for every new PowerShell session you start.</span></span> <span data-ttu-id="f62c5-128">Informationen zum sitzungsübergreifenden Speichern der Azure-Anmeldung in PowerShell finden Sie unter [Speichern von Benutzeranmeldeinformationen zwischen PowerShell-Sitzungen](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="f62c5-128">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="f62c5-129">Feedback geben</span><span class="sxs-lookup"><span data-stu-id="f62c5-129">Provide feedback</span></span>

<span data-ttu-id="f62c5-130">[Melden Sie auf GitHub ein Problem](https://github.com/Azure/azure-powershell/issues), wenn Sie in Azure PowerShell einen Fehler finden.</span><span class="sxs-lookup"><span data-stu-id="f62c5-130">If you find a bug in Azure PowerShell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="f62c5-131">Verwenden Sie das [Send-Feedback](/powershell/module/az.accounts/send-feedback)-Cmdlet, um über die Befehlszeile Feedback zu senden.</span><span class="sxs-lookup"><span data-stu-id="f62c5-131">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="f62c5-132">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="f62c5-132">Next Steps</span></span>

<span data-ttu-id="f62c5-133">Weitere Informationen zu Azure PowerShell-Modulen und den zugehörigen Features finden Sie unter [Erste Schritte mit Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="f62c5-133">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span> <span data-ttu-id="f62c5-134">Falls Sie mit Azure PowerShell vertraut sind und die Migration aus AzureRM durchführen möchten, hilft Ihnen der Artikel [Migrieren von AzureRM zum Az-Modul von Azure PowerShell](migrate-from-azurerm-to-az.md) weiter.</span><span class="sxs-lookup"><span data-stu-id="f62c5-134">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
