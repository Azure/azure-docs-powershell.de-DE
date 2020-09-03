---
title: Übersicht über Azure Stack PowerShell | Microsoft-Dokumentation
description: Enthält eine Übersicht über Azure Stack PowerShell und eine Anleitung zur Installation und Konfiguration.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 4b72bbd1bda93767251e0ba3d488f798575d9115
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "89244312"
---
# <a name="azurerm-module-250"></a><span data-ttu-id="ee3af-103">AzureRM-Modul 2.5.0</span><span class="sxs-lookup"><span data-stu-id="ee3af-103">AzureRM Module 2.5.0</span></span>

## <a name="requirements"></a><span data-ttu-id="ee3af-104">Anforderungen:</span><span class="sxs-lookup"><span data-stu-id="ee3af-104">Requirements:</span></span>
<span data-ttu-id="ee3af-105">Die niedrigste unterstützte Azure Stack-Version ist 1904.</span><span class="sxs-lookup"><span data-stu-id="ee3af-105">Minimum supported Azure Stack version is 1904.</span></span>

<span data-ttu-id="ee3af-106">Hinweis: Falls Sie eine niedrigere Version verwenden, installieren Sie die Version 1.2.11.</span><span class="sxs-lookup"><span data-stu-id="ee3af-106">Note: If you are using an earlier version install version 1.2.11</span></span>


## <a name="install"></a><span data-ttu-id="ee3af-107">Installieren</span><span class="sxs-lookup"><span data-stu-id="ee3af-107">Install</span></span>
```powershell-interactive
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module -Name AzureRM -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force -ErrorAction Continue
Uninstall-Module AzureRM.AzureStackStorage -Force -ErrorAction Continue
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force
Get-Module Azure.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

```

## <a name="release-notes"></a><span data-ttu-id="ee3af-108">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="ee3af-108">Release Notes</span></span>
* <span data-ttu-id="ee3af-109">AzureRm.Resources</span><span class="sxs-lookup"><span data-stu-id="ee3af-109">AzureRm.Resources</span></span>
    * <span data-ttu-id="ee3af-110">Neues Ressourcenmodul, das die API-Version 2018-05-01 mit dem Hybridprofil „2019-03-01-hybrid“ unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ee3af-110">New Resources module supporting 2018-05-01 api version with 2019-03-01-hybrid profile</span></span>
    * <span data-ttu-id="ee3af-111">Für die Vorgänge „PolicyDefinition(2016-12-01)“ und „PolicyAssignment(2017-06-01-preview)“ gelten weiterhin die alten API-Versionen.</span><span class="sxs-lookup"><span data-stu-id="ee3af-111">PolicyDefinition(2016-12-01) and PolicyAssisgment(2017-06-01-preview) operations are still with old api versions</span></span>
* <span data-ttu-id="ee3af-112">AzureRm.Compute</span><span class="sxs-lookup"><span data-stu-id="ee3af-112">AzureRm.Compute</span></span>
    * <span data-ttu-id="ee3af-113">Neues Computemodul, das die API-Version 2017-12-01 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ee3af-113">New compute module supporting 2017-12-01 api version.'</span></span>


* <span data-ttu-id="ee3af-114">Dieses Release entspricht dem Azure Stack-spezifischen API-Profil „2019-03-01-hybrid“.</span><span class="sxs-lookup"><span data-stu-id="ee3af-114">This release corresponds to the azurestack specific api profile 2019-03-01-hybrid</span></span>
* <span data-ttu-id="ee3af-115">Alle Module sind mindestens vom AzureRm.Profile-Modul abhängig.</span><span class="sxs-lookup"><span data-stu-id="ee3af-115">All the modules are taking greater than or equal to dependency on the AzureRm.Profile module.</span></span>
* <span data-ttu-id="ee3af-116">Die von den einzelnen Modulen unterstützten API-Versionen werden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ee3af-116">Api version suppoerted by  each of the modules are updated.</span></span> 
    * <span data-ttu-id="ee3af-117">Compute – 2017-12-30</span><span class="sxs-lookup"><span data-stu-id="ee3af-117">Compute - 2017-12-30</span></span>
    * <span data-ttu-id="ee3af-118">Netzwerk – 2017-10-01</span><span class="sxs-lookup"><span data-stu-id="ee3af-118">Network - 2017-10-01</span></span>
    * <span data-ttu-id="ee3af-119">Storage – 2016-01-01</span><span class="sxs-lookup"><span data-stu-id="ee3af-119">Storage - 2016-01-01</span></span>
    * <span data-ttu-id="ee3af-120">Ressourcen – 2018-02-01</span><span class="sxs-lookup"><span data-stu-id="ee3af-120">Resources - 2018-02-01</span></span>
    * <span data-ttu-id="ee3af-121">Key Vault – 2016-10-01</span><span class="sxs-lookup"><span data-stu-id="ee3af-121">Keyvault - 2016-10-01</span></span>
    * <span data-ttu-id="ee3af-122">DNS – 2016-04-01</span><span class="sxs-lookup"><span data-stu-id="ee3af-122">Dns - 2016-04-01</span></span>
* <span data-ttu-id="ee3af-123">Die vollständige Zuordnung aller API-Versionen für die einzelnen Ressourcentypen finden Sie unter https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json.</span><span class="sxs-lookup"><span data-stu-id="ee3af-123">The complete api version map for each of the resource types can be found at https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span></span>

## <a name="content"></a><span data-ttu-id="ee3af-124">Inhalt:</span><span class="sxs-lookup"><span data-stu-id="ee3af-124">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="ee3af-125">Azure-Bridge</span><span class="sxs-lookup"><span data-stu-id="ee3af-125">Azure Bridge</span></span>
<span data-ttu-id="ee3af-126">Vorschauversion des AzureBridge-Administratormoduls von Azure Stack, mit dem Sie Images aus Azure syndizieren können.</span><span class="sxs-lookup"><span data-stu-id="ee3af-126">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="ee3af-127">Backup</span><span class="sxs-lookup"><span data-stu-id="ee3af-127">Backup</span></span>
<span data-ttu-id="ee3af-128">Vorschauversion des Backup-Administratormoduls, das Administratoren Folgendes ermöglicht:</span><span class="sxs-lookup"><span data-stu-id="ee3af-128">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="ee3af-129">Konfigurieren des Speicherorts von Sicherungen</span><span class="sxs-lookup"><span data-stu-id="ee3af-129">Configure where backups are stored</span></span>
- <span data-ttu-id="ee3af-130">Durchführen von Sicherungen</span><span class="sxs-lookup"><span data-stu-id="ee3af-130">Perform backups</span></span>
- <span data-ttu-id="ee3af-131">Auflisten und Wiederherstellen abgeschlossener Sicherungen</span><span class="sxs-lookup"><span data-stu-id="ee3af-131">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="ee3af-132">Commerce</span><span class="sxs-lookup"><span data-stu-id="ee3af-132">Commerce</span></span>
<span data-ttu-id="ee3af-133">Vorschauversion des Commerce-Administratormoduls von Azure Stack, mit dem die aggregierte Datennutzung für das gesamte Azure Stack-System angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ee3af-133">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="ee3af-134">Compute</span><span class="sxs-lookup"><span data-stu-id="ee3af-134">Compute</span></span>
<span data-ttu-id="ee3af-135">Vorschauversion des Compute-Administratormoduls von Azure Stack mit Funktionen zur Verwaltung von Computekontingenten, Plattformimages, verwalteten Datenträgern und VM-Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="ee3af-135">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="ee3af-136">Fabric</span><span class="sxs-lookup"><span data-stu-id="ee3af-136">Fabric</span></span>
<span data-ttu-id="ee3af-137">Vorschauversion des Fabric-Administratormoduls von Azure Stack, mit dem Administratoren Infrastrukturkomponenten anzeigen und verwalten können:</span><span class="sxs-lookup"><span data-stu-id="ee3af-137">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="ee3af-138">Beenden, Starten und Herunterfahren von Skalierungseinheitknoten</span><span class="sxs-lookup"><span data-stu-id="ee3af-138">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="ee3af-139">Entladen und Fortsetzen von Skalierungseinheitknoten für FRU-bezogene Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="ee3af-139">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="ee3af-140">Reparieren von Skalierungseinheitknoten</span><span class="sxs-lookup"><span data-stu-id="ee3af-140">Repair of scale unit nodes</span></span>
- <span data-ttu-id="ee3af-141">Neustarten der Infrastrukturrolle</span><span class="sxs-lookup"><span data-stu-id="ee3af-141">Restart of Infrastructure role</span></span>
- <span data-ttu-id="ee3af-142">Beenden, Starten und Herunterfahren von Instanzen der Infrastrukturrolle</span><span class="sxs-lookup"><span data-stu-id="ee3af-142">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="ee3af-143">Erstellen neuer IP-Pools</span><span class="sxs-lookup"><span data-stu-id="ee3af-143">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="ee3af-144">Galerie</span><span class="sxs-lookup"><span data-stu-id="ee3af-144">Gallery</span></span>
<span data-ttu-id="ee3af-145">Vorschauversion des Gallery-Administratormoduls von Azure Stack mit Funktionen zum Verwalten von Katalogelementen im Azure Stack-Marketplace.</span><span class="sxs-lookup"><span data-stu-id="ee3af-145">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="ee3af-146">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="ee3af-146">Infrastructure Insights</span></span>
<span data-ttu-id="ee3af-147">Vorschauversion des Infrastructure Insights-Administratormoduls, das Administratoren Folgendes ermöglicht:</span><span class="sxs-lookup"><span data-stu-id="ee3af-147">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="ee3af-148">Anzeigen der Integrität ihrer Azure Stack-Stempelressourcen</span><span class="sxs-lookup"><span data-stu-id="ee3af-148">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="ee3af-149">Anzeigen und Verwalten von Warnungen</span><span class="sxs-lookup"><span data-stu-id="ee3af-149">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="ee3af-150">KeyVault</span><span class="sxs-lookup"><span data-stu-id="ee3af-150">KeyVault</span></span>
<span data-ttu-id="ee3af-151">Vorschauversion des KeyVault-Administratormoduls von Azure Stack, mit dem Administratoren KeyVault-Kontingente anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="ee3af-151">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="ee3af-152">Netzwerk</span><span class="sxs-lookup"><span data-stu-id="ee3af-152">Network</span></span>
<span data-ttu-id="ee3af-153">Vorschauversion des Network-Administratormoduls, das Folgendes ermöglicht:</span><span class="sxs-lookup"><span data-stu-id="ee3af-153">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="ee3af-154">Verwalten von Netzwerkkontingenten</span><span class="sxs-lookup"><span data-stu-id="ee3af-154">Management of network quotas</span></span>
- <span data-ttu-id="ee3af-155">Anzeigen zugeordneter Netzwerkressourcen (beispielsweise öffentliche IP-Adressen, virtuelle Netzwerke oder Lastenausgleichsmodule)</span><span class="sxs-lookup"><span data-stu-id="ee3af-155">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="ee3af-156">Stellt ein Cmdlet zum Anzeigen einer Administratorübersicht bereit.</span><span class="sxs-lookup"><span data-stu-id="ee3af-156">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="ee3af-157">Storage</span><span class="sxs-lookup"><span data-stu-id="ee3af-157">Storage</span></span>
<span data-ttu-id="ee3af-158">Vorschauversion des Storage-Administratormoduls von Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="ee3af-158">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="ee3af-159">Dieses Release bietet Funktionen für Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ee3af-159">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="ee3af-160">Verwalten von Speicherkontingenten</span><span class="sxs-lookup"><span data-stu-id="ee3af-160">Manage storage quotas</span></span>
- <span data-ttu-id="ee3af-161">Durchführen der Garbage Collection für gelöschte Speicherressourcen</span><span class="sxs-lookup"><span data-stu-id="ee3af-161">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="ee3af-162">Wiederherstellen gelöschter Speicherkonten</span><span class="sxs-lookup"><span data-stu-id="ee3af-162">Restore deleted storage accounts</span></span>
- <span data-ttu-id="ee3af-163">Migrieren von Containern zwischen Freigaben</span><span class="sxs-lookup"><span data-stu-id="ee3af-163">Migrate containers from one share to another</span></span>
- <span data-ttu-id="ee3af-164">Anzeigen von Informationen zu den einzelnen Speicherkomponenten</span><span class="sxs-lookup"><span data-stu-id="ee3af-164">View information about the individual storage components</span></span>
- <span data-ttu-id="ee3af-165">Anzeigen von Nutzungs- und Leistungsinformationen</span><span class="sxs-lookup"><span data-stu-id="ee3af-165">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="ee3af-166">Abonnementadministrator</span><span class="sxs-lookup"><span data-stu-id="ee3af-166">Subscription Admin</span></span>
<span data-ttu-id="ee3af-167">Vorschauversion des Subscription-Administratormoduls von Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="ee3af-167">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="ee3af-168">Dieses Modul bietet Administratorfunktionen für Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ee3af-168">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="ee3af-169">Verwalten von Plänen und Angeboten</span><span class="sxs-lookup"><span data-stu-id="ee3af-169">Manage plans and offers</span></span>
- <span data-ttu-id="ee3af-170">Anzeigen von Nutzungs- und Leistungsinformationen</span><span class="sxs-lookup"><span data-stu-id="ee3af-170">View usage and performance information</span></span>
- <span data-ttu-id="ee3af-171">Verwalten der RBAC</span><span class="sxs-lookup"><span data-stu-id="ee3af-171">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="ee3af-172">Subscription</span><span class="sxs-lookup"><span data-stu-id="ee3af-172">Subscription</span></span>
<span data-ttu-id="ee3af-173">Vorschauversion des Subscription-Moduls von Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="ee3af-173">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="ee3af-174">Dieses Modul bietet Benutzerfunktionen für Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ee3af-174">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="ee3af-175">Erstellen, Löschen und Aktualisieren von Abonnements</span><span class="sxs-lookup"><span data-stu-id="ee3af-175">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="ee3af-176">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="ee3af-176">Update</span></span>
<span data-ttu-id="ee3af-177">Vorschauversion des Update-Administratormoduls von Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="ee3af-177">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="ee3af-178">Dieses Modul ermöglicht Administratoren Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ee3af-178">In this module administrators can:</span></span>
- <span data-ttu-id="ee3af-179">Auflisten und Installieren verfügbarer Updates</span><span class="sxs-lookup"><span data-stu-id="ee3af-179">List and install available updates</span></span>
- <span data-ttu-id="ee3af-180">Fortsetzen unterbrochener Updates</span><span class="sxs-lookup"><span data-stu-id="ee3af-180">Resume interrupted updates</span></span>
- <span data-ttu-id="ee3af-181">Anzeigen installierter Updates</span><span class="sxs-lookup"><span data-stu-id="ee3af-181">View installed updates</span></span>
