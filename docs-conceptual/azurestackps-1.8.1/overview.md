---
title: Übersicht über Azure Stack PowerShell mit Administratorrechten | Microsoft-Dokumentation
description: Enthält eine Übersicht über Azure Stack PowerShell mit Administratorrechten und eine Anleitung zur Installation und Konfiguration.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 03/04/2020
ms.openlocfilehash: ef034424c72d88b3ceb28956da9ca56e4a7f3941
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "79402713"
---
# <a name="azure-stack-module-181"></a><span data-ttu-id="c3100-103">Azure Stack-Modul 1.8.1</span><span class="sxs-lookup"><span data-stu-id="c3100-103">Azure Stack Module 1.8.1</span></span>

## <a name="requirements"></a><span data-ttu-id="c3100-104">Anforderungen:</span><span class="sxs-lookup"><span data-stu-id="c3100-104">Requirements:</span></span>

<span data-ttu-id="c3100-105">Die niedrigste unterstützte Azure Stack-Version ist 1910.</span><span class="sxs-lookup"><span data-stu-id="c3100-105">Minimum supported Azure Stack version is 1910.</span></span>

<span data-ttu-id="c3100-106">Hinweis: Informationen zur Installation älterer Azure Stack-Versionen finden Sie unter [Installieren von PowerShell für Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell).</span><span class="sxs-lookup"><span data-stu-id="c3100-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="c3100-107">Installieren</span><span class="sxs-lookup"><span data-stu-id="c3100-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.1
```

## <a name="release-notes"></a><span data-ttu-id="c3100-108">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="c3100-108">Release Notes</span></span>

* <span data-ttu-id="c3100-109">Wird mit dem 1910-Update unterstützt</span><span class="sxs-lookup"><span data-stu-id="c3100-109">Supported with 1910 update</span></span>
