---
title: Verwenden experimenteller Azure PowerShell-Module
description: Grundlegendes zur Philosophie und Verwendung experimenteller Azure PowerShell-Module.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: ae2fecf73271a34a08ac66de03962a7a529e353b
ms.sourcegitcommit: 6c0d296bfec7c1c35a1d15074ca5eacda6684ea4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/30/2019
ms.locfileid: "68657585"
---
# <a name="use-experimental-azure-powershell-modules"></a>Verwenden von experimentellen Azure PowerShell-Modulen

Das Azure PowerShell-Team experimentiert mit zahlreichen Verbesserungen für Azure PowerShell und konzentriert sich dabei auf Azure-Entwicklertools. In diesem Artikel wird beschrieben, wie Sie sich an Experimenten mit Azure PowerShell beteiligen und Feedback an das Entwicklungsteam senden können.

## <a name="experimentation-methodology"></a>Experimentiermethodik

Zur Vereinfachung der Experimente erstellen wir neue Azure PowerShell-Module, die vorhandene Azure SDK-Funktionen auf neue, benutzerfreundlichere Weise implementieren. In den meisten Fällen sind die Cmdlets mit bereits vorhandenen Cmdlets identisch. Die experimentellen Cmdlets bieten jedoch eine Kurzschreibweise und intelligentere Standardwerte, die die Erstellung und Verwaltung von Azure-Ressourcen erleichtern.

Diese Module können parallel zu bereits vorhandenen Azure PowerShell-Modulen installiert werden. Die Cmdlet-Namen wurden verkürzt, um die Angabe kürzerer Namen zu ermöglichen und Namenskonflikte mit bereits vorhandenen, nicht experimentellen Cmdlets zu vermeiden.

Für die experimentellen Module wird folgende Benennungskonvention verwendet: `Az.*.Experiments`. Diese Benennungskonvention kommt so ähnlich auch bei der Benennung von Vorschaumodulen zur Anwendung: `Az.*.Preview`. Vorschaumodule unterscheiden sich von experimentellen Modulen. Vorschaumodule implementieren neue Funktionen von Azure-Diensten, die nur als Vorschauversion angeboten werden. Vorschaumodule ersetzen vorhandene Azure PowerShell-Module und verwenden die gleichen Cmdlet- und Parameternamen.

## <a name="how-to-install-an-experimental-module"></a>Installieren eines experimentellen Moduls

Experimentelle Module werden genau wie vorhandene Azure PowerShell-Module im PowerShell-Katalog veröffentlicht. Führen Sie zum Anzeigen einer Liste der experimentellen Module den folgenden Befehl aus:

```azurepowershell-interactive
Find-Module Az.*.Experiments
```

Verwenden Sie zum Installieren eines experimentellen Moduls das Cmdlet `Install-Module`.

### <a name="documentation-and-support"></a>Dokumentation und Support

Die Dokumentation ist im Installationspaket enthalten und kann über das Cmdlet `Get-Help` aufgerufen werden. Für experimentelle Module wird keine offizielle Dokumentation veröffentlicht.

Wir ermutigen Sie dazu, diese Module zu testen. Ihr Feedback hilft uns dabei, die Benutzerfreundlichkeit zu verbessern und noch besser auf Ihre Anforderungen einzugehen. Da es sich hierbei jedoch um experimentelle Modul handelt, ist der Support dafür eingeschränkt. Fragen oder Problemberichte können durch Erstellen eines [Problems](https://github.com/Azure/azure-powershell/issues) im GitHub-Repository übermittelt werden.

## <a name="experiments-and-areas-of-improvement"></a>Experimente und Verbesserungsbereiche

Diese Verbesserungen wurden auf der Grundlage wichtiger Alleinstellungsmerkmale in Konkurrenzprodukten ausgewählt. Bei der Azure CLI basieren Befehle beispielsweise ganz bewusst auf _Szenarien_ und nicht auf der _API-Oberfläche_.
Die Azure CLI verwendet einige intelligente Standardwerte, die Endbenutzern den Einstieg erleichtern.

### <a name="core-improvements"></a>Zentrale Verbesserungen

Die zentralen Verbesserungen gelten als naheliegend, und zur Implementierung dieser Updates sind nicht viele Experimente erforderlich.

- Szenariobasierte Cmdlets: *Alle* Cmdlets sollten für Szenarien und nicht für den Azure REST-Dienst entwickelt werden.

- Kürzere Namen: Gilt für die Namen von Cmdlets und Parametern.
  Verwenden Sie Aliase, um die Kompatibilität mit älteren Cmdlets zu gewährleisten. Geben Sie _abwärtskompatible_ Parametersätze an.

- Intelligente Standardwerte: Erstellen Sie intelligente Standardwerte zum Ausfüllen erforderlicher Informationen. Beispiel:
  - Ressourcengruppe
  - Location
  - Abhängige Ressourcen

### <a name="experimental-improvements"></a>Experimentelle Verbesserungen

Die experimentellen Verbesserungen stellen eine wesentliche Änderung dar, die das Team im Rahmen von Experimenten überprüfen möchte.

- Einfache Typen: Erstellungsszenarien sollten weniger komplexe Typen und Konfigurationsobjekte verwenden. Vereinfachen Sie die Konfiguration auf maximal zwei Parameter.

- Intelligente Erstellung: In Erstellungsszenarien mit intelligenter Erstellung gibt es _keine_ erforderlichen Parameter. Alle benötigten Informationen werden automatisch von Azure PowerShell ausgewählt.

- „Graue“ Parameter: In vielen Fällen sind einige Parameter unter Umständen „grau“ oder nicht wirklich optimal. Wurde der Parameter nicht angegeben, wird der Benutzer gefragt, ob der Parameter automatisch generiert werden soll. Bei grauen Parametern ist es auch sinnvoll, einen Wert mit Zustimmung des Benutzers vom Kontext abzuleiten.
  So kann es beispielsweise sinnvoll sein, wenn der graue Parameter den zuletzt verwendeten Wert vorschlägt.

- Schalter `-Auto`: Mit dem Schalter `-Auto` können Benutzer entscheiden, ob sie _für alles Standardwerte verwenden_ und dabei gleichzeitig die Integrität der erforderlichen Parameter im Hauptpfad bewahren möchten.

### <a name="feature-specific-switches"></a>Featurespezifische Schalter

Im Szenario „Web-App erstellen“ sind beispielsweise Schalter wie `-Git` oder `-AddRemote` denkbar, durch die einem vorhandenen Git-Repository automatisch eine Azure-Remotefunktion hinzugefügt wird.

- Festlegbare Standardwerte: Benutzer sollten die Möglichkeit haben, allgemeine Parameter wie `-ResourceGroupName` und `-Location` auf Standardwerte festzulegen.

- Standardgrößen: Ressourcengrößen können für Benutzer verwirrend sein, da viele Ressourcenanbieter unterschiedliche Namen verwenden (etwa „Standard\_DS1\_v2“ oder „S1“). Die meisten Benutzer machen sich jedoch eher Gedanken über die Kosten. Daher ist es sinnvoll, auf Grundlage eines Preisplans universelle Größen zu definieren. Benutzer können sich für eine bestimmte Größe entscheiden oder Azure PowerShell die Wahl der _besten Option_ für die Ressource und das Budget überlassen.

- Ausgabeformat: Azure PowerShell gibt derzeit `PSObject`-Objekte zurück und nur wenig über die Konsole aus. Azure PowerShell muss dem Benutzer ggf. Informationen zu den verwendeten intelligenten Standardwerten anzeigen.
