---
title: Einführung in das Az-Modul von Azure PowerShell
description: Hier finden Sie eine Einführung in das neue Az-Modul von Azure PowerShell, das das AzureRM-Modul ersetzt.
ms.date: 05/20/2020
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 1626bb4bee775ac173d078cf67934ee5a22632c4
ms.sourcegitcommit: 9f5c7d231b069ad501729bf015a829f3fe89bc6a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2020
ms.locfileid: "84122142"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a>Einführung in das neue Azure PowerShell Az-Modul

Seit Dezember 2018 ist das Az-Modul von Azure PowerShell allgemein verfügbar und jetzt das beabsichtigte PowerShell-Modul für die Interaktion mit Azure. Az verfügt über kürzere Befehle, verbesserte Stabilität und plattformübergreifende Unterstützung. Az bietet darüber hinaus die gleichen Features wie AzureRM und damit einen einfachen Migrationspfad.

> [!NOTE]
> PowerShell 7.x und höher ist die für die Verwendung mit Azure PowerShell auf allen Plattformen empfohlene PowerShell-Version.

Mit dem neuesten Az-Modul funktioniert Azure PowerShell mit PowerShell 6.x und höher auf allen Plattformen, einschließlich Windows, macOS und Linux. Es ist ebenfalls mit PowerShell 5.1 unter Windows kompatibel.

Da es sich bei Az um ein neues Modul handelt, wurde die Version auf 1.0.0 zurückgesetzt.

## <a name="why-a-new-module"></a>Gründe für ein neues Modul

Größere Updates können umständlich sein, daher ist es wichtig, dass Sie erfahren, warum die Entscheidung getroffen wurde, einen neuen Satz von Modulen mit neuen Cmdlets für die Interaktion zwischen Azure und PowerShell einzuführen.

Die größte und wichtigste Änderung ist, dass PowerShell seit der Einführung von [PowerShell](/powershell/scripting/overview) auf Basis der .NET Standard-Bibliothek ein plattformübergreifendes Produkt ist.
Wir sind bestrebt, den Azure-Support auf allen Plattformen bereitzustellen. Dies bedeutet, dass die Azure PowerShell-Module aktualisiert werden müssen, um .NET Standard zu verwenden und mit PowerShell Core kompatibel zu sein. Anstatt das bestehende AzureRM-Modul zu verwenden und komplexe Änderungen vorzunehmen, um diese Unterstützung zu implementieren, wurde das Az-Modul erstellt.

Die Erstellung eines neuen Moduls ermöglichte es unseren Technikern, auch das Design und die Benennung von Cmdlets und Modulen zu vereinheitlichen. Alle Module beginnen jetzt mit dem Präfix `Az.` und Cmdlets verwenden alle die Form _Verb_-`Az`_Nomen_. Früher waren Cmdlet-Namen nicht nur länger, sondern es gab auch Inkonsistenzen bei Cmdlet-Namen.

Auch die Anzahl der Module wurde verringert: Einige Module, die dieselben Diensten verwendet haben, wurden zusammengeführt. Cmdlets auf Verwaltungs- und Datenebene sind jetzt in einzelnen Modulen für ihre Dienste zusammengefasst. Für diejenigen, die Abhängigkeiten und Importvorgänge manuell verwalten, vereinfacht dies die Situation erheblich.

Mit diesen wichtigen Änderungen, die zur Entwicklung eines neuen Azure PowerShell-Moduls führten, war das Team bestrebt, die Verwendung von Azure mit PowerShell-Cmdlets einfacher denn je zu gestalten und sie auf mehr Plattformen als bisher bereitzustellen.

## <a name="upgrade-to-az"></a>Upgraden auf Az

Damit Sie hinsichtlich der neuesten Azure-Features in PowerShell auf dem Laufenden bleiben, sollten Sie so schnell wie möglich zum Az-Modul migrieren. Wenn Sie nicht bereit sind, das Az-Modul als Ersatz für AzureRM zu installieren, stehen Ihnen einige Optionen zur Verfügung, um mit Az zu experimentieren:

- Verwenden Sie eine `PowerShell`-Umgebung mit [Azure Cloud Shell](https://docs.microsoft.com/azure/cloud-shell/overview). Azure Cloud Shell ist eine browserbasierte Shellumgebung, die mit installiertem Az-Modul und aktivierten `Enable-AzureRM`-Kompatibilitätsaliasen bereitgestellt wird.
- Lassen Sie das AzureRM-Modul mit PowerShell 5.1 für Windows installiert, installieren Sie aber das Az-Modul für PowerShell 6.x oder höher. PowerShell 5.1 für Windows und PowerShell 6.x und höher verwenden separate Modulsammlungen. Befolgen Sie die Anweisungen zum Installieren der [aktuellen PowerShell-Version](/powershell/scripting/install/installing-powershell), und [installieren Sie dann das Az-Modul](install-az-ps.md) über PowerShell 6.x oder höher.

So führen Sie ein Upgrade von einer bestehenden AzureRM-Installation durch

1. [Deinstallieren Sie das AzureRM-Modul von Azure PowerShell.](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)
2. [Installieren Sie das Az-Modul von Azure PowerShell.](install-az-ps.md)
3. **OPTIONAL**: Aktivieren Sie den Kompatibilitätsmodus, um Aliase für AzureRM-Cmdlets mit [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias) hinzuzufügen, während Sie sich mit den neuen Befehlen vertraut machen. Weitere Informationen finden Sie im nächsten Abschnitt oder unter [Starten der Migration von AzureRM zu Az](migrate-from-azurerm-to-az.md).

## <a name="migrate-existing-scripts-to-az"></a>Migrieren bereits vorhandener Skripts zu Az

Die neuen Cmdlet-Namen sind ganz einfach zu lernen. Verwenden Sie in Cmdlet-Namen nicht mehr `AzureRm` oder `Azure`, sondern `Az`. Der alte Befehl `New-AzureRMVm` lautet nun also beispielsweise `New-AzVm`.
Die Migration umfasst mehr als sich nur mit den neuen Cmdlet-Namen vertraut zu machen: Es gibt umbenannte Module, Parameter und andere wichtige Änderungen.

Um Sie bei der Migration von AzureRM zu Az zu unterstützen, haben wir einige Ressourcen zur Verfügung gestellt:

- [Erste Schritte bei der Migration von AzureRM zu Azure](migrate-from-azurerm-to-az.md)
- [Vollständige Liste der Breaking Changes von AzureRM zu Az 1.0.0.0](migrate-az-1.0.0.md)
- Das Cmdlet [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias)

Das Az-Modul verfügt über einen Kompatibilitätsmodus, der Ihnen die Verwendung bereits vorhandener Skripts ermöglicht, während Sie das Update auf die neue Syntax durchführen. Das Cmdlet [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) ermöglicht einen Kompatibilitätsmodus durch Aliase, damit Sie vorhandene Skripts mit minimalen Änderungen verwenden können, während Sie an der vollständigen Migration zu Az arbeiten. Standardmäßig aktiviert `Enable-AzureRmAlias` nur Kompatibilitätsaliase für die aktuelle PowerShell-Sitzung. Verwenden Sie den Parameter `Scope`, um Kompatibilitätsaliase über PowerShell-Sitzungen hinweg beizubehalten. Weitere Informationen finden Sie in der [Referenzdokumentation zu Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias).

> [!IMPORTANT]
> Auch wenn die Cmdlet-Namen mit Aliasen versehen sind, kann es dennoch neue (oder umbenannte) Parameter oder geänderte Rückgabewerte für die Az-Cmdlets geben. Erwarten Sie nicht, dass die Aktivierung von Aliasen die Migration für Sie übernimmt! Weitere Informationen zu möglicherweise erforderlichen Änderungen an Ihren Skripts finden Sie in der [Vollständigen Liste der Breaking Changes](migrate-az-1.0.0.md).

## <a name="continued-support-for-azurerm"></a>Fortgesetzte Unterstützung für AzureRM

Für AzureRM werden keine neuen Cmdlets oder Features mehr bereitgestellt. Das AzureRM-Modul wird bis Dezember 2020 aber weiterhin offiziell gepflegt und mit Fehlerbehebungen versehen.
