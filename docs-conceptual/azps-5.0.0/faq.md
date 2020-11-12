---
title: Häufig gestellte Fragen
description: Häufig gestellte Fragen zu Azure PowerShell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 10ed859f04fa29d866530af71c32819b256c882a
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2020
ms.locfileid: "93407509"
---
# <a name="frequently-asked-questions-about-azure-powershell"></a>Häufig gestellte Fragen zu Azure PowerShell

## <a name="what-is-azure-powershell"></a>Was ist Azure PowerShell?

Azure PowerShell ist ein Satz von Cmdlets, die das direkte Verwalten von Azure-Ressourcen mit PowerShell ermöglichen. Seit Dezember 2018 ist das Az PowerShell-Modul allgemein verfügbar. Dieses PowerShell-Modul wird jetzt für die Interaktion mit Azure empfohlen. Weitere Informationen zum Az PowerShell-Modul finden Sie unter [Einführung in das neue Azure PowerShell Az-Modul](/powershell/azure/new-azureps-module-az).

## <a name="how-do-i-disable-breaking-change-warning-messages-in-azure-powershell"></a>Wie deaktiviere ich Warnmeldungen zu Breaking Changes in Azure PowerShell?

Zum Unterdrücken der Warnmeldungen zu Breaking Changes in Azure PowerShell müssen Sie die Umgebungsvariable `SuppressAzurePowerShellBreakingChangeWarnings` auf `true` festlegen.

```azurepowershell
Set-Item -Path Env:\SuppressAzurePowerShellBreakingChangeWarnings -Value $true
```
