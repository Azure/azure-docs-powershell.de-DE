---
title: Migrieren von Azure PowerShell-Skripts von AzureRM zu Az
description: Hier lernen Sie die Schritte und Tools kennen, mit denen Sie Skripts vom AzureRM-Modul zum neuen Az-Modul migrieren können.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/10/2019
ms.openlocfilehash: 0b0b951d540ed91e15472853bba46e4f302921bc
ms.sourcegitcommit: 10ec909100a70acec94d42f6084e7bf0342c6854
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2020
ms.locfileid: "83631097"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a>Migrieren von Azure PowerShell von AzureRM zum Az-Modul

Das Az-Modul bietet die gleichen Features wie AzureRM, verwendet aber kürzere und konsistentere Cmdlet-Namen.
Für die AzureRM-Cmdlets geschriebene Skripts funktionieren nicht automatisch auch mit dem neuen Modul. Zur Vereinfachung des Übergangs bietet Az Tools, die es Ihnen ermöglichen, Ihre bereits vorhandenen Skripts mit AzureRM auszuführen. Eine Migration zu einem neuen Befehlssatz ist immer unangenehm. Dieser Artikel hilft Ihnen jedoch dabei, den Umstieg auf das neue Modul in die Wege zu leiten.

Die vollständige Liste mit grundlegenden Änderungen zwischen AzureRM und Az finden Sie unter [Vollständige Änderungen von AzureRM zu Az](migrate-az-1.0.0.md).

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a>Vergewissern, dass vorhandene Skripts mit der neuesten AzureRM-Version funktionieren

Überprüfen Sie, welche Versionen von AzureRM auf Ihrem System installiert sind, bevor Sie Migrationsschritte ausführen. So können Sie sicherstellen, dass für Skripts bereits das aktuelle Release verwendet wird, und Sie können ermitteln, welche Versionen von AzureRM deinstalliert werden müssen.

Führen Sie den folgenden Befehl aus, um zu überprüfen, welche Versionen von AzureRM bei Ihnen installiert sind:

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

Die __aktuellste__ verfügbare Version von AzureRM ist __6.13.1__. Wenn diese Version nicht installiert ist, müssen Ihre vorhandenen Skripts möglicherweise zusätzlich geändert werden, um mit dem Az-Modul über das hinaus zu arbeiten, was hier und in der [Breaking Changes-Liste](migrate-az-1.0.0.md) beschrieben ist.

Wenn Ihre Skripts nicht mit AzureRM 6.13.1 funktionieren, aktualisieren Sie sie gemäß dem [Leitfaden zur Migration von AzureRM 5.x zu 6.x](/powershell/azure/azurerm/migration-guide.6.0.0).
Wenn Sie eine frühere Version des AzureRM-Moduls verwenden, gibt es für jede Hauptversion Migrationsleitfäden.

## <a name="uninstall-azurerm"></a>Deinstallieren von AzureRM

Es wird nicht garantiert, dass das Az-Modul mit allen bestehenden AzureRM-Installationen in PowerShell 5.1 für Windows kompatibel ist. Bevor Sie das Az-Modul installieren, deinstallieren Sie [AzureRM](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module).

> [!IMPORTANT]
>
> Wenn Sie nicht bereit sind, das AzureRM-Modul aus Ihrem System zu entfernen, können Sie stattdessen das Az-Modul für [PowerShell Core](/powershell/scripting/install/installing-powershell-core-on-windows) 6.x oder höher installieren. PowerShell Core und PowerShell 5.1 für Windows verwenden unterschiedliche Modulbibliotheken, sodass keine Konflikte auftreten. Sie können in PowerShell Core weiterhin [Aliase](#enable-azurerm-compatibility-aliases) aktivieren.

## <a name="install-the-azure-powershell-az-module"></a>Installieren des Az-Moduls von Azure PowerShell

Der erste Schritt besteht darin, das Az-Modul auf Ihrer Plattform zu installieren. Wenn Sie Az installieren, ist es ratsam, AzureRM zu deinstallieren. In den folgenden Schritten erfahren Sie, wie Sie Ihre bereits vorhandenen Skripts weiterhin ausführen und die Kompatibilität mit älteren Cmdlet-Namen sicherstellen können.

Befolgen Sie zur Installation des Az-Moduls von Azure PowerShell die Anweisungen unter [Installieren des Az-Moduls](install-az-ps.md).

> [!NOTE]
> An dieser Stelle sollten Sie vielleicht das im Az-Modul bereitgestellte Cmdlet [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) ausführen, nur um sicherzustellen, dass alle Versionen von AzureRM deinstalliert wurden und somit keine Konflikte verursachen.

## <a name="enable-azurerm-compatibility-aliases"></a>Aktivieren von AzureRM-Kompatibilitätsaliasen

Wenn Sie AzureRM deinstalliert haben und Ihre Skripts mit der neuesten Version von AzureRM funktionieren, ist der nächste Schritt das Aktivieren des Kompatibilitätsmodus für das Az-Modul. Die Kompatibilität wird mithilfe des folgenden Befehls aktiviert:

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

Aliase ermöglichen die Verwendung alter Cmdlet-Namen bei installiertem Az-Modul. Diese Aliase werden in das Profil für den ausgewählten Bereich geschrieben. Sollte kein Profil vorhanden sein, wird eines erstellt.
Wenn Sie einen `-Scope` verwenden, der umfangreicher als `CurrentUser` ist, sind die entsprechenden Berechtigungen erforderlich, um die entsprechende Profildatei zu erstellen oder zu aktualisieren.

> [!IMPORTANT]
> __Nur__ Cmdlet-Namen werden mit einem Alias versehen – dies gilt nicht für Modulnamen! Wenn Sie `#Requires`, `Import-Module`, Abhängigkeitslisten in einer `.psd1` oder vollqualifizierte Cmdlet-Namen verwenden, stellen Sie sicher, dass Sie diese an dieser Stelle migrieren, indem Sie dem in der [Breaking Changes-Liste](migrate-az-1.0.0.md) zu Modulnamen beschriebenen Prozess folgen.

> [!WARNING]
>
> Sie können für diesen Befehl zwar einen anderen Bereich (`-Scope`) verwenden, aber dies wird nicht empfohlen. Da Aliase in das Benutzerprofil für den ausgewählten Bereich geschrieben werden, empfiehlt es sich, sie auf einen möglichst kleinen Bereich zu beschränken. Eine systemweite Aktivierung von Aliasen kann zu Problemen für andere Benutzer führen, die AzureRM in ihrem lokalen Bereich installiert haben.

Führen Sie Ihre Skripts nach der Aktivierung des Aliasmodus erneut aus, um sich zu vergewissern, dass sie weiterhin wie erwartet funktionieren.
Einige Parameternamen wurden geändert, hinzugefügt oder für das Az-Modul vorgeschrieben. Die Ausgabetypen von Cmdlets wurden möglicherweise ebenfalls geändert. Diese Änderungen werden in der [Breaking Changes-Liste](migrate-az-1.0.0.md) beschrieben.

## <a name="update-cmdlets-modules-and-parameters"></a>Aktualisieren von Cmdlets, Modulen und Parametern

Wenn Skripts aktualisiert wurden und mit Aliasen ausgeführt werden, können Sie sich die Zeit nehmen, sie zu aktualisieren, um die neuen Cmdlets zu verwenden und andere Änderungen zu nutzen, z. B. neue Features. Für die meisten Skripts müssen Sie nur die Cmdlet-Namen gemäß dem [neuen Cmdlet-Namensschema in Az](migrate-az-1.0.0.md#cmdlet-noun-prefix-changes) aktualisieren. Es gibt möglicherweise auch einige andere vorzunehmende Änderungen, damit die Skripts gemäß ihrer Aufgabe und der verwendeten Azure PowerShell-Features funktionieren.

So wurden z. B. die [Blob Storage-Cmdlets](migrate-az-1.0.0.md#azstorage-previously-azurestorage-and-azurermstorage) vollständig überarbeitet, um ein neues asynchrones Modell zu verwenden, sodass die Skripts, die diese Cmdlets verwenden, einen höheren Aufwand für die Aktualisierung erfordern als solche, bei denen die einzigen relevanten Änderungen die Cmdlet-Namen darstellen.

Auch wenn Sie bis zu diesem Zeitpunkt nur kleine, einfache Änderungen an Ihren Skripts vornehmen mussten – oder sie sogar ohne zusätzliche Änderungen funktionieren, wenn Aliase aktiviert sind – lesen Sie die [vollständige Liste der Breaking Changes in Az 1.0.0](migrate-az-1.0.0.md), um sicherzustellen, dass Sie sich nicht auf ein „transparentes“ Verhalten der Aliase verlassen, das verschwinden könnte, nachdem Sie Cmdlet-Namen geändert und Aliase deaktiviert haben.

## <a name="disable-aliases"></a>Deaktivieren von Aliasen

Sobald Sie die Migration abgeschlossen haben und nicht mehr auf das Aliasverhalten angewiesen sind, wird empfohlen, Aliase zu deaktivieren. Dies erfolgt mit dem Cmdlet [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).

> [!IMPORTANT]
> Wenn Sie dieses Cmdlet ausführen, __stellen Sie sicher__, dass Sie es für jeden `-Scope` aufrufen, für den `Enable-AzureRmAlias` aufgerufen wurde, ansonsten kann es auf Ihrem System noch Skripts geben, die sich auf das Aliasverhalten verlassen.
