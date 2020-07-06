---
title: Übersicht über Azure Stack Hub PowerShell mit Administratorrechten | Microsoft-Dokumentation
description: Hier finden Sie eine Übersicht über Azure Stack Hub PowerShell mit Administratorrechten und eine Anleitung zur Installation und Konfiguration.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 06/22/2020
ms.openlocfilehash: 860a32d120e203093038130a535e8b6801e2bce2
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "85306559"
---
# <a name="azure-stack-hub-module-201"></a><span data-ttu-id="d8ca3-103">Azure Stack Hub-Modul 2.0.1</span><span class="sxs-lookup"><span data-stu-id="d8ca3-103">Azure Stack Hub Module 2.0.1</span></span>

## <a name="requirements"></a><span data-ttu-id="d8ca3-104">Anforderungen:</span><span class="sxs-lookup"><span data-stu-id="d8ca3-104">Requirements:</span></span>

<span data-ttu-id="d8ca3-105">Die niedrigste unterstützte Azure Stack Hub-Version ist 2002.</span><span class="sxs-lookup"><span data-stu-id="d8ca3-105">Minimum supported Azure Stack Hub version is 2002.</span></span>

<span data-ttu-id="d8ca3-106">Hinweis: Informationen zur Installation älterer Azure Stack-Versionen finden Sie unter [Installieren von PowerShell für Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell).</span><span class="sxs-lookup"><span data-stu-id="d8ca3-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="d8ca3-107">Installieren</span><span class="sxs-lookup"><span data-stu-id="d8ca3-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Az.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue

Install-Module -Name Az.BootStrapper -Force -AllowPrerelease

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 2.0.1-preview -AllowPrerelease
```


## <a name="release-notes"></a><span data-ttu-id="d8ca3-108">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="d8ca3-108">Release Notes</span></span>

* <span data-ttu-id="d8ca3-109">Wird mit dem 2002-Update unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d8ca3-109">Supported with 2002 update.</span></span>  

  <span data-ttu-id="d8ca3-110">Azure Stack Hub 2.0.0 ist ein Breaking Change.</span><span class="sxs-lookup"><span data-stu-id="d8ca3-110">The Azure Stack Hub 2.0.0 is a breaking change.</span></span> <span data-ttu-id="d8ca3-111">Das Modul verwendet das Az-Modul anstelle des AzureRM-Moduls.</span><span class="sxs-lookup"><span data-stu-id="d8ca3-111">The module uses the Az module rather than the AzureRM module.</span></span> <span data-ttu-id="d8ca3-112">Einen Migrationsleitfaden und eine Liste der Breaking Changes finden Sie unter [Migrieren von AzureRM zu Azure PowerShell Az in Azure Stack Hub](https://aka.ms/AA7qsji).</span><span class="sxs-lookup"><span data-stu-id="d8ca3-112">You can find a migration guide and a list of breaking changes in [Migrate from AzureRM to Azure PowerShell Az in Azure Stack Hub](https://aka.ms/AA7qsji).</span></span>
