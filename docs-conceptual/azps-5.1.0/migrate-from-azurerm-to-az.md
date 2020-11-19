---
title: Migrieren von Azure PowerShell-Skripts von AzureRM zu Az
description: Hier lernen Sie die Schritte und Tools kennen, mit denen Sie Skripts vom AzureRM-Modul zum neuen Az-Modul migrieren können.
ms.devlang: powershell
ms.service: azure-powershell
ms.topic: conceptual
ms.date: 10/12/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2f3b6a55b3c674a6030a1d3568e57cdb15c43b02
ms.sourcegitcommit: d81c3b0f0f7289104be03869eb675128b61db7d3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "94715381"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a>Migrieren von Azure PowerShell von AzureRM zum Az-Modul

Alle Versionen des AzureRM PowerShell-Moduls sind veraltet, werden aber weiterhin unterstützt. Für die Interaktion mit Azure wird nun das [Az PowerShell-Modul](install-az-ps.md) empfohlen.

Für die AzureRM-Cmdlets geschriebene Skripts funktionieren nicht automatisch auch mit dem neuen Modul. Um den Umstieg zu vereinfachen, wurde das [Toolkit für die Migration von AzureRM zu Az](https://github.com/Azure/azure-powershell-migration) entwickelt. Eine Migration zu einem neuen Befehlssatz ist immer unangenehm. Dieser Artikel hilft Ihnen jedoch dabei, den Umstieg auf das Az PowerShell-Modul in die Wege zu leiten. Weitere Informationen zu den Gründen für die Entwicklung des Az PowerShell-Moduls finden Sie unter [Einführung in das neue Azure PowerShell Az-Modul](new-azureps-module-az.md).

Die vollständige Liste mit grundlegenden Änderungen zwischen AzureRM und Az finden Sie unter [Vollständige Änderungen von AzureRM zu Az](migrate-az-1.0.0.md).

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a>Vergewissern, dass vorhandene Skripts mit der neuesten AzureRM-Version funktionieren

Überprüfen Sie, welche Versionen von AzureRM auf Ihrem System installiert sind, bevor Sie Migrationsschritte ausführen.
So können Sie sicherstellen, dass für Skripts bereits das aktuelle Release verwendet wird, und Sie können ermitteln, welche Versionen von AzureRM deinstalliert werden müssen.

Führen Sie das folgende Beispiel aus, um zu überprüfen, welche Versionen von AzureRM bei Ihnen installiert sind:

```azurepowershell
Get-Module -Name AzureRM -ListAvailable -All
```

Die **aktuellste** verfügbare Version von AzureRM ist **6.13.1**. Sollte diese Version nicht installiert sein, sind für die Verwendung des Az-Moduls möglicherweise zusätzliche Änderungen für Ihre vorhandenen Skripts erforderlich, die über die Beschreibungen in diesem Artikel und in der [Breaking Changes-Liste](migrate-az-1.0.0.md) hinausgehen.

Wenn Ihre Skripts nicht mit AzureRM 6.13.1 funktionieren, aktualisieren Sie sie gemäß dem [Leitfaden zur Migration von AzureRM 5.x zu 6.x](/powershell/azure/azurerm/migration-guide.6.0.0). Wenn Sie eine frühere Version des AzureRM-Moduls verwenden, gibt es für jede Hauptversion Migrationsleitfäden.

## <a name="install-the-azurerm-to-az-migration-toolkit"></a>Installieren des Toolkits für die Migration von AzureRM zu Az

```azurepowershell
Install-Module -Name Az.Tools.Migration
```

## <a name="automatically-migrate-your-powershell-scripts"></a>Automatisches Migrieren Ihrer PowerShell-Skripts

Mit dem Toolkit für die Migration von AzureRM zu Az können Sie einen Plan generieren, um zu ermitteln, welche Änderungen für Ihre Skripts vorgenommen werden, bevor Sie tatsächlich Änderungen vornehmen und das Az PowerShell-Modul installieren.

In der Schnellstartanleitung [Automatisches Migrieren von PowerShell-Skripts von AzureRM zum Az PowerShell-Modul](quickstart-migrate-azurerm-to-az-automatically.md) werden die einzelnen Schritte für die automatische Aktualisierung Ihrer PowerShell-Skripts von AzureRM auf das Az PowerShell-Modul beschrieben.

## <a name="next-steps"></a>Nächste Schritte

[Installieren von Azure PowerShell](install-az-ps.md)
[Deinstallieren von AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module)
