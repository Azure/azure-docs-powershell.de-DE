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
# <a name="azure-stack-module-160"></a><span data-ttu-id="4c170-103">Azure Stack-Modul 1.6.0</span><span class="sxs-lookup"><span data-stu-id="4c170-103">Azure Stack Module 1.6.0</span></span>

## <a name="requirements"></a><span data-ttu-id="4c170-104">Anforderungen:</span><span class="sxs-lookup"><span data-stu-id="4c170-104">Requirements:</span></span>
<span data-ttu-id="4c170-105">Die niedrigste unterstützte Azure Stack-Version ist 1811.</span><span class="sxs-lookup"><span data-stu-id="4c170-105">Minimum supported Azure Stack version is 1811.</span></span>

<span data-ttu-id="4c170-106">Hinweis: Falls Sie eine niedrigere Version verwenden, sollten Sie Version 1.6.0 installieren.</span><span class="sxs-lookup"><span data-stu-id="4c170-106">Note: If you are using an earlier version install version 1.6.0</span></span>

## <a name="install"></a><span data-ttu-id="4c170-107">Installieren</span><span class="sxs-lookup"><span data-stu-id="4c170-107">Install</span></span>
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

## <a name="release-notes"></a><span data-ttu-id="4c170-108">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="4c170-108">Release Notes</span></span>
* <span data-ttu-id="4c170-109">Wird mit dem 1811-Update unterstützt</span><span class="sxs-lookup"><span data-stu-id="4c170-109">Supported with 1811 update</span></span>
* <span data-ttu-id="4c170-110">Azs.Compute.Admin-Modul</span><span class="sxs-lookup"><span data-stu-id="4c170-110">Azs.Compute.Admin Module</span></span>
    * <span data-ttu-id="4c170-111">Fehlen des Azs-Präfix für „New-DataDiskObject“ korrigiert und Alias mit Warnung zur bevorstehenden Einstellung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="4c170-111">Fixed missing Azs prefix for New-DataDiskObject and added alias with warning of future deprecation.</span></span>
* <span data-ttu-id="4c170-112">Azs.Update.Admin-Modul</span><span class="sxs-lookup"><span data-stu-id="4c170-112">Azs.Update.Admin Module</span></span>
    * <span data-ttu-id="4c170-113">Warnung hinzugefügt, um die Ausführung von „Test-AzureStack“ vor „Install-AzsUpdate“ zu empfehlen</span><span class="sxs-lookup"><span data-stu-id="4c170-113">Added a warning to recommend running Test-AzureStack before Install-AzsUpdate</span></span>
* <span data-ttu-id="4c170-114">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="4c170-114">Azs.Fabric.Admin</span></span>
    * <span data-ttu-id="4c170-115">Neues Cmdlet (die Funktionen werden von Azure Stack 1811 und höher unterstützt)</span><span class="sxs-lookup"><span data-stu-id="4c170-115">New cmdlet (The features are supported by Azure Stack 1811+)</span></span>
        * <span data-ttu-id="4c170-116">Get-AzsDrive</span><span class="sxs-lookup"><span data-stu-id="4c170-116">Get-AzsDrive</span></span>
        * <span data-ttu-id="4c170-117">Get-AzsVolume</span><span class="sxs-lookup"><span data-stu-id="4c170-117">Get-AzsVolume</span></span>
        * <span data-ttu-id="4c170-118">Get-AzsStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="4c170-118">Get-AzsStorageSubSystem</span></span>
    * <span data-ttu-id="4c170-119">Eingestellte Unterstützung</span><span class="sxs-lookup"><span data-stu-id="4c170-119">Deprecation</span></span>
        * <span data-ttu-id="4c170-120">„Get-AzsInfrastructureVolume“ ist jetzt ein Alias für das Cmdlet „Get-AzsVolume“</span><span class="sxs-lookup"><span data-stu-id="4c170-120">Get-AzsInfrastructureVolume is an alias now to the cmdlet Get-AzsVolume</span></span>
* <span data-ttu-id="4c170-121">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="4c170-121">Azs.InfrastructureInsights.Admin</span></span>
    *  <span data-ttu-id="4c170-122">Neues Cmdlet „Repair-AzsAlert“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="4c170-122">Added a new cmdlet Repair-AzsAlert</span></span>
* <span data-ttu-id="4c170-123">Azs.Storage.Admin</span><span class="sxs-lookup"><span data-stu-id="4c170-123">Azs.Storage.Admin</span></span>
    * <span data-ttu-id="4c170-124">Fehler behoben, aufgrund dessen Standardkontingentwerte nicht verwendet wurden</span><span class="sxs-lookup"><span data-stu-id="4c170-124">Bug fix where default quota values are not being used</span></span>
* <span data-ttu-id="4c170-125">Azs.Subscriptions.Admin-Modul</span><span class="sxs-lookup"><span data-stu-id="4c170-125">Azs.Subscriptions.Admin Module</span></span>
    * <span data-ttu-id="4c170-126">Fehlen des Azs-Präfix für „New-AddonPlanDefinitionObject“ korrigiert und Alias mit Warnung zur bevorstehenden Einstellung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="4c170-126">Fixed missing Azs prefix for New-AddonPlanDefinitionObject and added alias with warning of future deprecation.</span></span>
