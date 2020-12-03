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
ms.openlocfilehash: e19fea440025e7a00a037e360ac95ff8e0e62129
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/01/2020
ms.locfileid: "96428009"
---
# <a name="azure-stack-module-180"></a><span data-ttu-id="09f42-103">Azure Stack-Modul 1.8.0</span><span class="sxs-lookup"><span data-stu-id="09f42-103">Azure Stack Module 1.8.0</span></span>

## <a name="requirements"></a><span data-ttu-id="09f42-104">Anforderungen:</span><span class="sxs-lookup"><span data-stu-id="09f42-104">Requirements:</span></span>

<span data-ttu-id="09f42-105">Die niedrigste unterstützte Azure Stack-Version ist 1910.</span><span class="sxs-lookup"><span data-stu-id="09f42-105">Minimum supported Azure Stack version is 1910.</span></span>

<span data-ttu-id="09f42-106">Hinweis: Informationen zur Installation älterer Azure Stack-Versionen finden Sie unter [Installieren von PowerShell für Azure Stack](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell).</span><span class="sxs-lookup"><span data-stu-id="09f42-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="09f42-107">Installieren</span><span class="sxs-lookup"><span data-stu-id="09f42-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.0
```

## <a name="release-notes"></a><span data-ttu-id="09f42-108">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="09f42-108">Release Notes</span></span>

* <span data-ttu-id="09f42-109">Wird mit dem 1910-Update unterstützt</span><span class="sxs-lookup"><span data-stu-id="09f42-109">Supported with 1910 update</span></span>
* <span data-ttu-id="09f42-110">Die Änderungen umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="09f42-110">Changes include:</span></span>

    - <span data-ttu-id="09f42-111">**Neues DRP-Administratormodul:** Der Bereitstellungsressourcenanbieter (Deployment Resource Provider, DRP) ermöglicht orchestrierte Bereitstellungen von Ressourcenanbietern in Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="09f42-111">**New DRP Admin module**: The Deployment Resource Provider (DRP) enables orchestrated deployments of resource providers to Azure Stack Hub.</span></span> <span data-ttu-id="09f42-112">Diese Befehle interagieren mit der Azure Resource Manager-Ebene, um mit DRP zu interagieren.</span><span class="sxs-lookup"><span data-stu-id="09f42-112">These commands interact with the Azure Resource Manager layer to interact with DRP.</span></span>

    - <span data-ttu-id="09f42-113">**BRP:**</span><span class="sxs-lookup"><span data-stu-id="09f42-113">**BRP**:</span></span>
        - <span data-ttu-id="09f42-114">Unterstützung der Wiederherstellung einzelner Rollen für die Sicherung der Azure Stack-Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="09f42-114">Support single role restore for Azures stack infrastructure backup.</span></span>
        - <span data-ttu-id="09f42-115">Hinzufügung des Parameters `RoleName` zum Cmdlet R`estore-AzsBackup`</span><span class="sxs-lookup"><span data-stu-id="09f42-115">Add parameter `RoleName` to cmdlet R`estore-AzsBackup`.</span></span>

    - <span data-ttu-id="09f42-116">**FRP:** Breaking Changes für Ressourcen vom Typ **Laufwerk** und **Volume** mit der API-Version 2019-05-01.</span><span class="sxs-lookup"><span data-stu-id="09f42-116">**FRP**: Breaking changes for **Drive** and **Volume** resources with API version 2019-05-01.</span></span> <span data-ttu-id="09f42-117">Die Features werden ab Azure Stack Hub 1910 unterstützt:</span><span class="sxs-lookup"><span data-stu-id="09f42-117">The features are supported by Azure Stack Hub 1910 and later:</span></span>
        - <span data-ttu-id="09f42-118">Der Wert von ID, `Name`, `HealthStatus` und `OperationalStatus` wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="09f42-118">The value of ID, `Name`, `HealthStatus`, and `OperationalStatus` have been changed.</span></span>
        - <span data-ttu-id="09f42-119">Unterstützte neue Eigenschaften `FirmwareVersion`, `IsIndicationEnabled`, `Manufacturer` und `StoragePool` für Ressourcen vom Typ **Laufwerk**</span><span class="sxs-lookup"><span data-stu-id="09f42-119">Supported new properties `FirmwareVersion`, `IsIndicationEnabled`, `Manufacturer`, and `StoragePool` for **Drive** resources.</span></span>
        - <span data-ttu-id="09f42-120">Die Eigenschaften `CanPool` und `CannotPoolReason` von Ressourcen des Typs **Laufwerk** sind veraltet. Verwenden Sie stattdessen `OperationalStatus`.</span><span class="sxs-lookup"><span data-stu-id="09f42-120">The properties `CanPool` and `CannotPoolReason` of **Drive** resources have been deprecated; use `OperationalStatus` instead.</span></span>