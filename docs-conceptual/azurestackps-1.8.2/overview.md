---
title: Übersicht über Azure Stack PowerShell mit Administratorrechten | Microsoft-Dokumentation
description: Enthält eine Übersicht über Azure Stack PowerShell mit Administratorrechten und eine Anleitung zur Installation und Konfiguration.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 08/06/2020
ms.openlocfilehash: 5e30e1b4a21f62c00419cfa77e1d875e110eebec
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427991"
---
# <a name="azure-stack-module-182"></a>Azure Stack-Modul 1.8.2

## <a name="requirements"></a>Anforderungen:

Die niedrigste unterstützte Azure Stack-Version ist 1910.

Hinweis: Informationen zur Installation älterer Azure Stack-Versionen finden Sie unter [Installieren von PowerShell für Azure Stack](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell).

## <a name="install"></a>Installieren

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.2
```

## <a name="release-notes"></a>Versionsinformationen

* Wird mit dem 1910-Update unterstützt