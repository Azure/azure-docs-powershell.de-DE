---
title: Übersicht über Azure Stack PowerShell mit Administratorrechten | Microsoft-Dokumentation
description: Enthält eine Übersicht über Azure Stack PowerShell mit Administratorrechten und eine Anleitung zur Installation und Konfiguration.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: b0e85bec82b9b7c876b2bbf337b603c8d68cf6a3
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2020
ms.locfileid: "63053314"
---
# <a name="azure-stack-module-160"></a>Azure Stack-Modul 1.6.0

## <a name="requirements"></a>Anforderungen:
Die niedrigste unterstützte Azure Stack-Version ist 1811.

Hinweis: Falls Sie eine niedrigere Version verwenden, sollten Sie Version 1.6.0 installieren.

## <a name="install"></a>Installieren
```
# Remove previous versions of AzureStack and AzureRM modules
Uninstall-Module -Name AzureRM -Force
Uninstall-Module -Name Azure.Storage -Force
Uninstall-Module -Name AzureStack -Force
Get-Module -Name "Azs*" -ListAvailable | Uninstall-Module  -Force 
Get-Module -Name "AzureRm*" -ListAvailable | Uninstall-Module  -Force

# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.6.0
```

## <a name="release-notes"></a>Versionsinformationen
* Wird mit dem 1811-Update unterstützt
* Azs.Compute.Admin-Modul
    * Fehlen des Azs-Präfix für „New-DataDiskObject“ korrigiert und Alias mit Warnung zur bevorstehenden Einstellung hinzugefügt
* Azs.Update.Admin-Modul
    * Warnung hinzugefügt, um die Ausführung von „Test-AzureStack“ vor „Install-AzsUpdate“ zu empfehlen
* Azs.Fabric.Admin
    * Neues Cmdlet (die Funktionen werden von Azure Stack 1811 und höher unterstützt)
        * Get-AzsDrive
        * Get-AzsVolume
        * Get-AzsStorageSubSystem
    * Eingestellte Unterstützung
        * „Get-AzsInfrastructureVolume“ ist jetzt ein Alias für das Cmdlet „Get-AzsVolume“
* Azs.InfrastructureInsights.Admin
    *  Neues Cmdlet „Repair-AzsAlert“ hinzugefügt
* Azs.Storage.Admin
    * Fehler behoben, aufgrund dessen Standardkontingentwerte nicht verwendet wurden
* Azs.Subscriptions.Admin-Modul
    * Fehlen des Azs-Präfix für „New-AddonPlanDefinitionObject“ korrigiert und Alias mit Warnung zur bevorstehenden Einstellung hinzugefügt
