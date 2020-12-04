---
title: Migrieren von Azure PowerShell-Skripts von AzureRM zu Az
description: Hier werden die Schritte und Tools zum Migrieren von Azure PowerShell-Skripts von AzureRM zum neuen Az PowerShell-Modul beschrieben.
ms.devlang: powershell
ms.service: azure-powershell
ms.topic: conceptual
ms.date: 12/1/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: bc37d0b73db0e6df226788795730730c077fcefa
ms.sourcegitcommit: cd243c8f6dc02dbd6234e764b065643dfd31dd8b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/02/2020
ms.locfileid: "96502588"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a>Migrieren von Azure PowerShell von AzureRM zum Az-Modul

Alle Versionen des AzureRM PowerShell-Moduls sind veraltet. Für die Interaktion mit Azure wird nun das [Az PowerShell-Modul](install-az-ps.md) empfohlen.

## <a name="why-a-new-module"></a>Gründe für ein neues Modul

Die größte und wichtigste Änderung ist, dass die [PowerShell](/powershell/scripting/overview)-Befehlsshell, die auf der .NET Standard-Bibliothek basiert, seit ihrer Einführung ein plattformübergreifendes Produkt ist.

Wie auch bei der PowerShell-Sprache haben wir es uns zur Aufgabe gemacht, Azure auf allen Plattformen zu unterstützen. Dies bedeutete, dass die Azure PowerShell-Module zur Verwendung von .NET Standard aktualisiert werden und mit PowerShell Core kompatibel sein mussten. Anstatt das bestehende AzureRM-Modul zu ändern und komplexe Änderungen vorzunehmen, um diese Unterstützung zu implementieren, wurde das Az-Modul erstellt.

Die Erstellung eines neuen Moduls ermöglichte es unseren Technikern auch, das Design sowie die Benennung von Cmdlets und Modulen zu vereinheitlichen. Alle Module beginnen jetzt mit dem Präfix `Az.`, und alle Cmdlets folgen der Namenskonvention `Verb-AzNoun`. Zuvor waren Cmdlet-Namen länger und inkonsistent.

Auch die Anzahl von Modulen wurde verringert: Einige Module, die dieselben Dienste nutzten, wurden zusammengeführt. Cmdlets auf Verwaltungs- und Datenebene für denselben Dienst sind jetzt in einem einzelnen Modul zusammengefasst. Für diejenigen, die Abhängigkeiten und Importvorgänge manuell verwalten, stellt diese Konsolidierung eine erhebliche Vereinfachung dar.

Bei diesen wichtigen Änderungen bestand das Ziel des Teams darin, die Verwendung von Azure mit PowerShell-Cmdlets einfacher denn je zu gestalten und auf mehr Plattformen als bisher zu ermöglichen.

## <a name="upgrading-to-az-powershell"></a>Aktualisieren auf Az PowerShell

Für die AzureRM-Cmdlets geschriebene Skripts funktionieren nicht automatisch mit dem Az-Modul. Um den Umstieg zu vereinfachen, wurde das [Toolkit für die Migration von AzureRM zu Az](https://github.com/Azure/azure-powershell-migration) entwickelt. Eine Migration zu einem neuen Befehlssatz ist immer unangenehm. Dieser Artikel hilft Ihnen jedoch dabei, den Umstieg auf das Az PowerShell-Modul in die Wege zu leiten. Weitere Informationen zu den Gründen für die Entwicklung des Az PowerShell-Moduls finden Sie unter [Einführung in das neue Azure PowerShell Az-Modul](new-azureps-module-az.md).

Die neuen Cmdlet-Namen sind ganz einfach zu lernen. Verwenden Sie in Cmdlet-Namen nicht mehr `AzureRm` oder `Azure`, sondern `Az`. Das alte Cmdlet `New-AzureRMVm` heißt jetzt beispielsweise `New-AzVm`.
Die Migration umfasst jedoch mehr, als sich nur mit den neuen Cmdlet-Namen vertraut zu machen. Es gibt umbenannte Module, Parameter und andere wichtige Änderungen.

Die vollständige Liste mit grundlegenden Änderungen zwischen AzureRM und Az finden Sie unter [Vollständige Änderungen von AzureRM zu Az](migrate-az-1.0.0.md).

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a>Vergewissern, dass vorhandene Skripts mit der neuesten AzureRM-Version funktionieren

Überprüfen Sie, welche Versionen von AzureRM auf Ihrem System installiert sind, bevor Sie Migrationsschritte ausführen.
So können Sie sicherstellen, dass für Skripts bereits das aktuelle Release verwendet wird, und ermitteln, welche Versionen von AzureRM deinstalliert werden müssen.

Führen Sie das folgende Beispiel aus, um zu überprüfen, welche Versionen von AzureRM bei Ihnen installiert sind:

```azurepowershell
Get-Module -Name AzureRM -ListAvailable -All
```

Die **aktuellste** verfügbare Version von AzureRM ist **6.13.1**. Sollte diese Version nicht installiert sein, sind zur Verwendung des Az-Moduls möglicherweise zusätzliche Änderungen für Ihre vorhandenen Skripts erforderlich, die nicht in diesem Artikel und der [Breaking Changes-Liste](migrate-az-1.0.0.md) beschrieben werden.

Wenn Ihre Skripts nicht mit AzureRM 6.13.1 funktionieren, aktualisieren Sie sie gemäß dem [Leitfaden zur Migration von AzureRM 5.x zu 6.x](/powershell/azure/azurerm/migration-guide.6.0.0). Wenn Sie eine frühere Version des AzureRM-Moduls verwenden, gibt es für jede Hauptversion Migrationsleitfäden.

## <a name="option-1-recommended-automatically-migrate-your-powershell-scripts"></a>Option 1 (empfohlen): Automatisches Migrieren Ihrer PowerShell-Skripts

Die empfohlene Option minimiert den erforderlichen Aufwand für die Migration von AzureRM-Skripts zu Az.

### <a name="install-the-azurerm-to-az-migration-toolkit"></a>Installieren des Toolkits für die Migration von AzureRM zu Az

```azurepowershell
Install-Module -Name Az.Tools.Migration
```

### <a name="convert-your-scripts-automatically"></a>Automatisches Konvertieren Ihrer Skripts

Mit dem Toolkit für die Migration von AzureRM zu Az können Sie einen Plan generieren, um zu ermitteln, welche Änderungen für Ihre Skripts vorgenommen werden, bevor Sie tatsächlich Änderungen vornehmen und das Az PowerShell-Modul installieren.

In der Schnellstartanleitung [Automatisches Migrieren von PowerShell-Skripts von AzureRM zum Az PowerShell-Modul](quickstart-migrate-azurerm-to-az-automatically.md) werden die einzelnen Schritte für die automatische Aktualisierung Ihrer PowerShell-Skripts von AzureRM auf das Az PowerShell-Modul beschrieben.

## <a name="option-2-use-compatibility-mode-with-enable-azurermalias"></a>Option 2: Verwenden des Kompatibilitätsmodus mit „Enable-AzureRmAlias“

Das Az-Modul verfügt über einen Kompatibilitätsmodus, der Ihnen die Verwendung bereits vorhandener Skripts ermöglicht, während Sie das Update auf die neue Syntax durchführen. Mit dem Cmdlet [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) können Sie über Aliase einen Kompatibilitätsmodus nutzen. Dieser Modus ermöglicht es Ihnen, vorhandene Skripts mit minimalen Änderungen zu verwenden, während Sie an der vollständigen Migration zu Az arbeiten. Standardmäßig aktiviert `Enable-AzureRmAlias` nur Kompatibilitätsaliase für die aktuelle PowerShell-Sitzung. Verwenden Sie den Parameter `Scope`, um Kompatibilitätsaliase über PowerShell-Sitzungen hinweg beizubehalten. Weitere Informationen finden Sie in der [Referenzdokumentation zu Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias).

> [!IMPORTANT]
> Auch wenn die Cmdlet-Namen mit Aliasen versehen sind, kann es dennoch neue (oder umbenannte) Parameter oder geänderte Rückgabewerte für die Az-Cmdlets geben. Erwarten Sie nicht, dass die Aktivierung von Aliasen die Migration für Sie übernimmt! Weitere Informationen zu möglicherweise erforderlichen Änderungen an Ihren Skripts finden Sie in der [Vollständigen Liste der Breaking Changes](migrate-az-1.0.0.md).

## <a name="option-3-migrate-your-scripts-in-visual-studio-code-with-the-azure-powershell-extension"></a>Option 3: Migrieren Ihrer Skripts in Visual Studio Code mit der Azure PowerShell-Erweiterung

### <a name="install-the-azure-powershell-extension-for-visual-studio-code"></a>Installieren der Azure PowerShell-Erweiterung für Visual Studio Code

Installieren Sie die [Azure PowerShell-Erweiterung für VSCode](https://marketplace.visualstudio.com/items?itemName=azps-tools.azps-tools).

### <a name="convert-your-scripts-manually"></a>Manuelles Konvertieren Ihrer Skripts

1. Laden Sie Ihr AzureRM-Skript in VSCode.
2. Starten Sie die Migration, indem Sie die Befehlspalette mit `Ctrl+Shift+P` öffnen und dann `Migrate Azure PowerShell script` auswählen.
3. Wählen Sie `AzureRM` als Quellversion aus.
4. Führen Sie die empfohlenen Aktionen für jeden unterstrichenen Befehl oder Parameter aus.

## <a name="next-steps"></a>Nächste Schritte

[Deinstallieren von AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module)
[Installieren von Azure PowerShell](install-az-ps.md)
