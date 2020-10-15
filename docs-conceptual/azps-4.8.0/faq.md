---
title: Häufig gestellte Fragen
description: Häufig gestellte Fragen zu Azure PowerShell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: b436f00ccef779464a555cd787a9ab0adcc970ce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "92001997"
---
# <a name="frequently-asked-questions-about-azure-powershell"></a>Häufig gestellte Fragen zu Azure PowerShell

## <a name="what-is-azure-powershell"></a>Was ist Azure PowerShell?

Azure PowerShell ist ein Satz von Cmdlets, die das direkte Verwalten von Azure-Ressourcen mit PowerShell ermöglichen. Seit Dezember 2018 ist das Az PowerShell-Modul allgemein verfügbar. Dieses PowerShell-Modul wird jetzt für die Interaktion mit Azure empfohlen. Weitere Informationen zum Az PowerShell-Modul finden Sie unter [Einführung in das neue Azure PowerShell Az-Modul](/powershell/azure/new-azureps-module-az).

## <a name="how-do-i-disable-breaking-change-warning-messages-in-azure-powershell"></a>Wie deaktiviere ich Warnmeldungen zu Breaking Changes in Azure PowerShell?

Zum Unterdrücken der Warnmeldungen zu Breaking Changes in Azure PowerShell müssen Sie die Umgebungsvariable `SuppressAzurePowerShellBreakingChangeWarnings` auf `true` festlegen.

```azurepowershell
Set-Item -Path Env:\SuppressAzurePowerShellBreakingChangeWarnings -Value $true
```
