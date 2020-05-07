---
title: Übersicht über Azure Stack PowerShell mit Administratorrechten | Microsoft-Dokumentation
description: Enthält eine Übersicht über Azure Stack PowerShell mit Administratorrechten und eine Anleitung zur Installation und Konfiguration.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 02/24/2020
ms.openlocfilehash: ec406c80de6b457f7e340a23fe8caf2ab83be46a
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2020
ms.locfileid: "78264409"
---
# <a name="azure-stack-module-180"></a>Azure Stack-Modul 1.8.0

## <a name="requirements"></a>Anforderungen:

Die niedrigste unterstützte Azure Stack-Version ist 1910.

Hinweis: Informationen zur Installation älterer Azure Stack-Versionen finden Sie unter [Installieren von PowerShell für Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell).

## <a name="install"></a>Installieren

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.0
```

## <a name="release-notes"></a>Versionsinformationen

* Wird mit dem 1910-Update unterstützt
* Die Änderungen umfassen Folgendes:

    - **Neues DRP-Administratormodul:** Der Bereitstellungsressourcenanbieter (Deployment Resource Provider, DRP) ermöglicht orchestrierte Bereitstellungen von Ressourcenanbietern in Azure Stack Hub. Diese Befehle interagieren mit der Azure Resource Manager-Ebene, um mit DRP zu interagieren.

    - **BRP:**
        - Unterstützung der Wiederherstellung einzelner Rollen für die Sicherung der Azure Stack-Infrastruktur
        - Hinzufügung des Parameters `RoleName` zum Cmdlet R`estore-AzsBackup`

    - **FRP:** Breaking Changes für Ressourcen vom Typ **Laufwerk** und **Volume** mit der API-Version 2019-05-01. Die Features werden ab Azure Stack Hub 1910 unterstützt:
        - Der Wert von ID, `Name`, `HealthStatus` und `OperationalStatus` wurde geändert.
        - Unterstützte neue Eigenschaften `FirmwareVersion`, `IsIndicationEnabled`, `Manufacturer` und `StoragePool` für Ressourcen vom Typ **Laufwerk**
        - Die Eigenschaften `CanPool` und `CannotPoolReason` von Ressourcen des Typs **Laufwerk** sind veraltet. Verwenden Sie stattdessen `OperationalStatus`.
