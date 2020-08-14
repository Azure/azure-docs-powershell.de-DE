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
ms.openlocfilehash: e314374eff433d1869378bdaa9a0370c3fd3d8d1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "88022937"
---
# <a name="azure-stack-module-182"></a><span data-ttu-id="dccf1-103">Azure Stack-Modul 1.8.2</span><span class="sxs-lookup"><span data-stu-id="dccf1-103">Azure Stack Module 1.8.2</span></span>

## <a name="requirements"></a><span data-ttu-id="dccf1-104">Anforderungen:</span><span class="sxs-lookup"><span data-stu-id="dccf1-104">Requirements:</span></span>

<span data-ttu-id="dccf1-105">Die niedrigste unterstützte Azure Stack-Version ist 1910.</span><span class="sxs-lookup"><span data-stu-id="dccf1-105">Minimum supported Azure Stack version is 1910.</span></span>

<span data-ttu-id="dccf1-106">Hinweis: Informationen zur Installation älterer Azure Stack-Versionen finden Sie unter [Installieren von PowerShell für Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell).</span><span class="sxs-lookup"><span data-stu-id="dccf1-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="dccf1-107">Installieren</span><span class="sxs-lookup"><span data-stu-id="dccf1-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.2
```

## <a name="release-notes"></a><span data-ttu-id="dccf1-108">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="dccf1-108">Release Notes</span></span>

* <span data-ttu-id="dccf1-109">Wird mit dem 1910-Update unterstützt</span><span class="sxs-lookup"><span data-stu-id="dccf1-109">Supported with 1910 update</span></span>
