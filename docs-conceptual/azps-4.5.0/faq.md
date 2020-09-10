---
title: Häufig gestellte Fragen
description: Häufig gestellte Fragen zu Azure PowerShell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: b436f00ccef779464a555cd787a9ab0adcc970ce
ms.sourcegitcommit: 2f1e3c275626fba1c4275cae8ef1d13b11f55735
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/04/2020
ms.locfileid: "89449941"
---
# <a name="frequently-asked-questions-about-azure-powershell"></a><span data-ttu-id="bac0f-103">Häufig gestellte Fragen zu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="bac0f-103">Frequently asked questions about Azure PowerShell</span></span>

## <a name="what-is-azure-powershell"></a><span data-ttu-id="bac0f-104">Was ist Azure PowerShell?</span><span class="sxs-lookup"><span data-stu-id="bac0f-104">What is Azure PowerShell?</span></span>

<span data-ttu-id="bac0f-105">Azure PowerShell ist ein Satz von Cmdlets, die das direkte Verwalten von Azure-Ressourcen mit PowerShell ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="bac0f-105">Azure PowerShell is a set of cmdlets that allows you to manage Azure resources directly with PowerShell.</span></span> <span data-ttu-id="bac0f-106">Seit Dezember 2018 ist das Az PowerShell-Modul allgemein verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bac0f-106">In December 2018, the Az PowerShell module became generally available.</span></span> <span data-ttu-id="bac0f-107">Dieses PowerShell-Modul wird jetzt für die Interaktion mit Azure empfohlen.</span><span class="sxs-lookup"><span data-stu-id="bac0f-107">It's now the recommended PowerShell module for interacting with Azure.</span></span> <span data-ttu-id="bac0f-108">Weitere Informationen zum Az PowerShell-Modul finden Sie unter [Einführung in das neue Azure PowerShell Az-Modul](/powershell/azure/new-azureps-module-az).</span><span class="sxs-lookup"><span data-stu-id="bac0f-108">To learn more about the Az PowerShell module, see [Introducing the new Azure PowerShell Az module](/powershell/azure/new-azureps-module-az).</span></span>

## <a name="how-do-i-disable-breaking-change-warning-messages-in-azure-powershell"></a><span data-ttu-id="bac0f-109">Wie deaktiviere ich Warnmeldungen zu Breaking Changes in Azure PowerShell?</span><span class="sxs-lookup"><span data-stu-id="bac0f-109">How do I disable breaking change warning messages in Azure PowerShell?</span></span>

<span data-ttu-id="bac0f-110">Zum Unterdrücken der Warnmeldungen zu Breaking Changes in Azure PowerShell müssen Sie die Umgebungsvariable `SuppressAzurePowerShellBreakingChangeWarnings` auf `true` festlegen.</span><span class="sxs-lookup"><span data-stu-id="bac0f-110">To suppress the breaking change warning messages in Azure PowerShell, you'll need to set the environment variable `SuppressAzurePowerShellBreakingChangeWarnings` to `true`.</span></span>

```azurepowershell
Set-Item -Path Env:\SuppressAzurePowerShellBreakingChangeWarnings -Value $true
```
