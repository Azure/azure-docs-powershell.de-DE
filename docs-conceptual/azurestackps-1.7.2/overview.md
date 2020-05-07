---
title: Übersicht über Azure Stack PowerShell mit Administratorrechten | Microsoft-Dokumentation
description: Enthält eine Übersicht über Azure Stack PowerShell mit Administratorrechten und eine Anleitung zur Installation und Konfiguration.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 02/06/2019
ms.openlocfilehash: 1b3d707e862dd0c21e9e6b0a89f429ff21b1a99d
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2020
ms.locfileid: "68861347"
---
# <a name="azure-stack-module-172"></a><span data-ttu-id="cb689-103">Azure Stack-Modul 1.7.2</span><span class="sxs-lookup"><span data-stu-id="cb689-103">Azure Stack Module 1.7.2</span></span>

## <a name="requirements"></a><span data-ttu-id="cb689-104">Anforderungen:</span><span class="sxs-lookup"><span data-stu-id="cb689-104">Requirements:</span></span>

<span data-ttu-id="cb689-105">Die niedrigste unterstützte Azure Stack-Version ist 1904.</span><span class="sxs-lookup"><span data-stu-id="cb689-105">Minimum supported Azure Stack version is 1904.</span></span>

<span data-ttu-id="cb689-106">Hinweis: Informationen zur Installation älterer Azure Stack-Versionen finden Sie unter [Installieren von PowerShell für Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell).</span><span class="sxs-lookup"><span data-stu-id="cb689-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="cb689-107">Installieren</span><span class="sxs-lookup"><span data-stu-id="cb689-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.5.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

## <a name="release-notes"></a><span data-ttu-id="cb689-108">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="cb689-108">Release Notes</span></span>

* <span data-ttu-id="cb689-109">Wird mit dem 1904-Update unterstützt</span><span class="sxs-lookup"><span data-stu-id="cb689-109">Supported with 1904 update</span></span>
* <span data-ttu-id="cb689-110">Hierbei handelt es sich um eine Version mit grundlegenden Änderungen (Breaking Changes).</span><span class="sxs-lookup"><span data-stu-id="cb689-110">This a breaking change release.</span></span> <span data-ttu-id="cb689-111">Details zu Breaking Changes finden Sie unter <https://aka.ms/azspshmigration170>.</span><span class="sxs-lookup"><span data-stu-id="cb689-111">For details on the breaking changes, refer to <https://aka.ms/azspshmigration170></span></span>
* <span data-ttu-id="cb689-112">Wichtige Änderung: Änderungen am zertifikatbasierten Verschlüsselungsmodus werden gesichert.</span><span class="sxs-lookup"><span data-stu-id="cb689-112">Breaking change: Backup changes to cert-based encryption mode.</span></span> <span data-ttu-id="cb689-113">Unterstützung für symmetrische Schlüssel ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="cb689-113">Support for symmetric keys is deprecated.</span></span>
* <span data-ttu-id="cb689-114">Details zu Breaking Changes finden Sie unter https://aka.ms/azspshmigration170.</span><span class="sxs-lookup"><span data-stu-id="cb689-114">For details on the breaking changes, refer to https://aka.ms/azspshmigration170</span></span>
* <span data-ttu-id="cb689-115">Azs.Storage.Admin Module</span><span class="sxs-lookup"><span data-stu-id="cb689-115">Azs.Storage.Admin Module</span></span> 
* <span data-ttu-id="cb689-116">Fehlerbehebung: Neues Speicherplatzkontingent verwendet Standardwerte, wenn keine angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cb689-116">Bug fix - New Storage Quota uses defaults if none provided.</span></span>
