---
title: Installieren und Konfigurieren von Azure PowerShell unter macOS und Linux | Microsoft-Dokumentation
description: Hier erfahren Sie, wie Sie Azure PowerShell für die erste Verwendung unter macOS und Linux installieren und konfigurieren.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/12/2018
ms.openlocfilehash: 9e4c727c9adc378b9f1a65d3cb3dda7af05c33f5
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/23/2018
---
# <a name="install-and-configure-azure-powershell-on-macos-and-linux"></a>Installieren und Konfigurieren von Azure PowerShell unter macOS und Linux

PowerShell Core v6 und Azure PowerShell können jetzt auf Windows-fremden Plattformen installiert werden.
Die Installation von Azure PowerShell unter macOS und Linux unterscheidet sich nicht sehr von der Installation unter Windows, allerdings müssen Sie zuerst PowerShell Core v6 installieren.

> [!NOTE]

> PowerShell Core v6 und Azure PowerShell für .NET Core befinden sich derzeit noch in der Betaphase.
> Der Support für diese Produkte ist eingeschränkt. Wenn Sie Probleme haben oder Fehler erkennen, melden Sie dies bitte in GitHub.
>
> * [Probleme mit PowerShell Core v6](https://github.com/PowerShell/PowerShell/issues)
> * [Probleme mit Azure PowerShell](https://github.com/azure/azure-docs-powershell/issues)

## <a name="step-1-install-powershell-core-v6"></a>Schritt 1: Installieren von PowerShell Core v6

Die Installation von PowerShell Core v6 variiert je nach Betriebssystem.
PowerShell Core v6 kann zwar auch unter Windows installiert werden, in diesem Artikel wird jedoch die Installation unter macOS und Linux behandelt. Wenn Sie Azure PowerShell unter Windows verwenden möchten, lesen Sie den Artikel [Installieren und Konfigurieren von Azure PowerShell](./install-azurerm-ps.md) für Windows.

Die Installation von **PowerShell Core v6** unter Linux oder macOS variiert je nach Linux-Distribution und Betriebssystemversion.
Eine ausführliche Anleitung finden Sie im folgenden Artikel:

- [Installieren von PowerShell Core unter macOS und Linux](/powershell/scripting/setup/installing-powershell-core-on-macos-and-linux)

## <a name="step-2-install-azure-powershell-for-net-core"></a>Schritt 2: Installieren von Azure PowerShell für .NET Core

In PowerShell Core v6 ist das PowerShellGet-Modul bereits vorinstalliert. Dies vereinfacht die Installation eines beliebigen, im PowerShell-Katalog veröffentlichten Moduls. Um Azure PowerShell zu installieren, öffnen Sie eine neue PowerShell-Sitzung, und führen Sie den folgenden Befehl aus:

```powershell
Install-Module AzureRM.NetCore
```

## <a name="step-3-load-the-azurermnetcore-module"></a>Schritt 3: Laden des AzureRM.Netcore-Moduls

Nach der Installation des Moduls müssen Sie das Modul in der PowerShell-Sitzung laden. Module werden wie folgt mit dem Cmdlet `Import-Module` geladen:

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

Nach Abschluss des Imports können Sie das neu installierte Modul testen, indem Sie versuchen, sich mithilfe des folgenden Befehls bei Azure anzumelden:

```powershell
Login-AzureRMAccount
```

Der obige Befehl sollte Sie auffordern, zu `https://aka.ms/devicelogin` zu wechseln und den bereitgestellten Code einzugeben.

## <a name="available-cmdlets"></a>Verfügbare Cmdlets

Die Azure PowerShell-Module für .NET Standard sind immer noch in der Entwicklungsphase. Diese Module bieten nicht den vollständigen Satz der Cmdlets, die für die Windows-Version der Module verfügbar sind. Die folgenden Funktionen werden in AzureRM.Netcore-Module implementiert:

* Kontenverwaltung
  - Melden Sie sich mit dem Microsoft-Konto, Unternehmenskonto oder einem Dienstprinzipal über Microsoft Azure Active Directory an.
  - Speichern Sie die Anmeldeinformationen mit Save-AzureRmContext auf einem Datenträger, und laden Sie gespeicherte Anmeldeinformationen mit Import-AzureRmContext.
* Environment
  - Abrufen der verschiedenen vorkonfigurierten Microsoft Azure-Umgebungen
  - Hinzufügen/Einrichten/Entfernen angepasster Umgebungen (z.B. Ihrer Azure Stack- oder Windows Azure Pack-Umgebungen)
* Cmdlets auf Verwaltungsebene für Azure-Dienste, die Resource Manager- und Service Management-Schnittstellen nutzen.
  - Virtual Machine
  - App Service (Websites)
  - SQL-Datenbank
  - Speicher
  - Netzwerk

## <a name="next-steps"></a>Nächste Schritte

Weitere Informationen zur Verwendung von Azure PowerShell finden Sie im Artikel [Erste Schritte mit Azure PowerShell](get-started-azureps.md).
