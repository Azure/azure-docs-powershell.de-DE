---
title: Einführung in das Azure Az PowerShell-Modul
description: Hier erhalten Sie eine Einführung in das Az PowerShell-Modul, das für die Interaktion mit Azure empfohlen wird und das AzureRM PowerShell-Modul ersetzt.
ms.date: 02/12/2021
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: b52b6995fb50a6ce502d42e7df588ca72340a1e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101872362"
---
# <a name="introducing-the-azure-az-powershell-module"></a>Einführung in das Azure Az PowerShell-Modul

## <a name="overview"></a>Übersicht

Beim Az PowerShell-Modul handelt es sich um einen Satz von Cmdlets zum direkten Verwalten von Azure-Ressourcen über PowerShell. PowerShell bietet leistungsstarke Features für die Automatisierung, die Sie zum Verwalten Ihrer Azure-Ressourcen nutzen können, beispielsweise im Rahmen einer CI/CD-Pipeline.

Das Az PowerShell-Modul ersetzt AzureRM und ist die empfohlene Version für die Interaktion mit Azure.

Zur Verwendung des Az PowerShell-Moduls stehen Ihnen die folgenden Methoden zur Auswahl:

* [Installieren des Az PowerShell-Moduls über PowerShellGet](install-az-ps.md) (empfohlene Option)
* [Installieren des Az PowerShell-Moduls mit MSI](install-az-ps-msi.md)
* [Verwenden von Azure Cloud Shell](/azure/cloud-shell/overview)
* [Verwenden des Az PowerShell-Docker-Containers](azureps-in-docker.md)

## <a name="features"></a>Features

Das Az PowerShell-Modul bietet die folgenden Vorteile:

* Sicherheit und Stabilität
  * Verschlüsselung des Tokencaches
  * Verhindern von Man-in-the-Middle-Angriffen
  * Unterstützen der Authentifizierung mit ADFS 2019
  * Benutzernamen- und Kennwortauthentifizierung in PowerShell 7
  * Unterstützung für Features wie die fortlaufende Zugriffsevaluierung (wird 2021 eingeführt)
* Unterstützung für alle Azure-Dienste
  * Alle allgemein verfügbaren Azure-Dienste verfügen über ein entsprechendes unterstütztes PowerShell-Modul.
  * Mehrere Fehlerbehebungen und API-Versionsupgrades seit AzureRM
* Neue Funktionen
  * Unterstützung in Cloud Shell und plattformübergreifend
  * Abrufen und Verwenden von Zugriffstoken für den Zugriff auf Azure-Ressourcen
  * Cmdlet für erweiterte REST-Vorgänge mit Azure-Ressourcen verfügbar

> [!NOTE]
> PowerShell 7 und höher ist auf allen Plattformen die empfohlene Version für die Verwendung mit dem Az PowerShell-Modul.

Das neue Az PowerShell-Modul basiert auf der .NET Standard-Bibliothek und funktioniert mit PowerShell 7 und höher auf allen Plattformen, einschließlich Windows, macOS und Linux. Es ist auch mit Windows PowerShell 5.1 kompatibel.

Unser Ziel ist es, Azure auf allen Plattformen zu unterstützen, und alle Az PowerShell-Module sind plattformübergreifend.

## <a name="upgrade-your-environment-to-az"></a>Aktualisieren Ihrer Umgebung auf Az

Damit Sie hinsichtlich der neuesten Azure-Features in PowerShell auf dem Laufenden bleiben, sollten Sie zum Az-Modul migrieren. Wenn Sie nicht bereit sind, das Az-Modul als Ersatz für AzureRM zu installieren, stehen Ihnen einige Optionen zur Verfügung, um mit Az zu experimentieren:

* Verwenden Sie eine `PowerShell`-Umgebung mit [Azure Cloud Shell](/azure/cloud-shell/overview). Azure Cloud Shell ist eine browserbasierte Shellumgebung, die mit installiertem Az-Modul und aktivierten `Enable-AzureRM`-Kompatibilitätsaliasen bereitgestellt wird.
* Lassen Sie das AzureRM-Modul in Windows PowerShell 5.1 installiert, und installieren Sie das Az-Modul in PowerShell 7 oder höher. Windows PowerShell 5.1 sowie PowerShell 7 und höher verwenden separate Modulsammlungen. Befolgen Sie die Anweisungen zum Installieren der [aktuellen PowerShell-Version](/powershell/scripting/install/installing-powershell), und [installieren Sie das Az-Modul](install-az-ps.md) dann über PowerShell 7 oder höher.

So führen Sie ein Upgrade von einer bestehenden AzureRM-Installation durch

1. [Deinstallieren Sie das AzureRM-Modul von Azure PowerShell.](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)
1. [Installieren Sie das Az-Modul von Azure PowerShell.](install-az-ps.md)
1. **OPTIONAL**: Aktivieren Sie den Kompatibilitätsmodus, um Aliase für AzureRM-Cmdlets mit [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias) hinzuzufügen, während Sie sich mit den neuen Befehlen vertraut machen. Weitere Informationen finden Sie im nächsten Abschnitt oder unter [Migrieren von Azure PowerShell von AzureRM zum Az-Modul](migrate-from-azurerm-to-az.md).

## <a name="migrate-existing-scripts-from-azurerm-to-az"></a>Migrieren vorhandener Skripts von AzureRM zu Az

Wenn Ihre Skripts noch auf dem AzureRM-Modul basieren, stehen Ihnen verschiedene Ressourcen zur Verfügung, die Sie bei der Migration unterstützen:

* [Erste Schritte bei der Migration von AzureRM zu Azure](migrate-from-azurerm-to-az.md)
* [Vollständige Liste der Breaking Changes von AzureRM zu Az 1.0.0.0](migrate-az-1.0.0.md)
* Das Cmdlet [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias)

## <a name="supportability"></a>Support-Fähigkeit

Az ist das aktuellste PowerShell-Modul für Azure. Wenn Sie Probleme melden oder Featureanfragen senden möchten, können Sie diese direkt im [GitHub-Repository](https://github.com/Azure/azure-powershell) eingeben, oder sich an den Microsoft-Support wenden, falls Sie über einen Supportvertrag verfügen. Featureanfragen werden in der aktuellen Version von Az implementiert. Behebungen kritischer Probleme werden in der aktuellen Version von Az implementiert.

Die Az PowerShell-Module bieten nun die gleichen Funktionen wie AzureRM PowerShell-Module und weitere Funktionen, daher werden die AzureRM PowerShell-Module am 29 Februar 2024 ausgemustert.

Um Dienstunterbrechungen zu vermeiden, müssen Sie bis zum 29. Februar 2024 die [Skripts aktualisieren](https://aka.ms/azpsmigrate), die AzureRM PowerShell-Module verwenden. Befolgen Sie zum automatischen Aktualisieren Ihrer Skripts die [Schnellstartanleitung](/powershell/azure/quickstart-migrate-azurerm-to-az-automatically).

## <a name="data-collection"></a>Datensammlung

Azure PowerShell sammelt standardmäßig Telemetriedaten. Microsoft aggregiert gesammelte Daten, um Verwendungsmuster zu identifizieren, allgemeine Probleme zu ermitteln und die Benutzerfreundlichkeit von Azure PowerShell zu verbessern.
Microsoft Azure PowerShell sammelt keine privaten oder personenbezogenen Daten. Die Nutzungsdaten tragen beispielsweise dazu bei, Probleme zu identifizieren (z. B. Cmdlets mit mäßigem Erfolg) und unsere Arbeit zu priorisieren.

Wir schätzen die Erkenntnisse, die uns diese Daten liefern, wissen aber auch, dass nicht jeder Nutzungsdaten senden möchte. Sie können die Datensammlung mit dem Cmdlet [`Disable-AzDataCollection`](/powershell/module/az.accounts/disable-azdatacollection) deaktivieren. Weitere Informationen finden Sie bei Bedarf auch in unseren [Datenschutzbestimmungen](https://privacy.microsoft.com/privacystatement).
