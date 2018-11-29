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
ms.openlocfilehash: afa83a6258e57e961576b328e67fad634704dddf
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/29/2018
ms.locfileid: "52587736"
---
# <a name="azure-stack-module-150"></a><span data-ttu-id="42ed9-103">Azure Stack-Modul 1.5.0</span><span class="sxs-lookup"><span data-stu-id="42ed9-103">Azure Stack Module 1.5.0</span></span>

## <a name="requirements"></a><span data-ttu-id="42ed9-104">Anforderungen:</span><span class="sxs-lookup"><span data-stu-id="42ed9-104">Requirements:</span></span>
<span data-ttu-id="42ed9-105">Die niedrigste unterstützte Azure Stack-Version ist 1808.</span><span class="sxs-lookup"><span data-stu-id="42ed9-105">Minimum supported Azure Stack version is 1808.</span></span>

<span data-ttu-id="42ed9-106">Hinweis: Falls Sie eine niedrigere Version verwenden, sollten Sie Version 1.4.0 installieren.</span><span class="sxs-lookup"><span data-stu-id="42ed9-106">Note: If you are using an earlier version install version 1.4.0</span></span>

## <a name="known-issues"></a><span data-ttu-id="42ed9-107">Bekannte Probleme:</span><span class="sxs-lookup"><span data-stu-id="42ed9-107">Known issues:</span></span>

- <span data-ttu-id="42ed9-108">Mit „New-AzsOffer“ können keine öffentlichen Angebote erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="42ed9-108">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="42ed9-109">Das Cmdlet „Set-AzsOffer“ muss hinterher aufgerufen werden, um den Zustand zu ändern.</span><span class="sxs-lookup"><span data-stu-id="42ed9-109">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="42ed9-110">Ein IP-Pool kann nicht ohne erneute Bereitstellung entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="42ed9-110">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="install"></a><span data-ttu-id="42ed9-111">Installieren</span><span class="sxs-lookup"><span data-stu-id="42ed9-111">Install</span></span>
```
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.5.0
```

## <a name="release-notes"></a><span data-ttu-id="42ed9-112">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="42ed9-112">Release Notes</span></span>
* <span data-ttu-id="42ed9-113">Alle Azure Stack-Module mit Administratorrechten werden auf eine Version aktualisiert, die höher oder gleich der Abhängigkeit vom AzureRm.Profile-Modul sind</span><span class="sxs-lookup"><span data-stu-id="42ed9-113">All the Azure Stack Admin modules are updated for greater than or equal to dependency on the AzureRm.Profile module</span></span>
* <span data-ttu-id="42ed9-114">Unterstützung für die Verarbeitung von geschachtelten Ressourcennamen in allen Modulen</span><span class="sxs-lookup"><span data-stu-id="42ed9-114">Support for handling nested resource names in all the modules</span></span>
* <span data-ttu-id="42ed9-115">Fehlerbehebung in allen Modulen, in denen „ErrorActionPreference“ außer Kraft gesetzt wird und „Stop“ lautet</span><span class="sxs-lookup"><span data-stu-id="42ed9-115">Bug fix in all the modules where ErrorActionPreference is being overridden to be Stop</span></span>
* <span data-ttu-id="42ed9-116">Azs.Compute.Admin-Modul</span><span class="sxs-lookup"><span data-stu-id="42ed9-116">Azs.Compute.Admin Module</span></span>
    * <span data-ttu-id="42ed9-117">Neue Kontingenteigenschaften für die Unterstützung eines verwalteten Datenträgers hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="42ed9-117">New quota properties added for the support of manged disk</span></span>
    * <span data-ttu-id="42ed9-118">Cmdlets für Datenträgermigration hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="42ed9-118">Addition of disk migration related cmdlets</span></span>
    * <span data-ttu-id="42ed9-119">Zusätzliche Eigenschaften in Plattformimage und VM-Erweiterungsobjekten</span><span class="sxs-lookup"><span data-stu-id="42ed9-119">Additional properties in the Platform Image and VM extesnion objects</span></span>
* <span data-ttu-id="42ed9-120">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="42ed9-120">Azs.Fabric.Admin</span></span> 
    * <span data-ttu-id="42ed9-121">Neues Cmdlet zum Hinzufügen eines Skalierungseinheitknotens</span><span class="sxs-lookup"><span data-stu-id="42ed9-121">New cmdlet for adding scale unit node</span></span>
* <span data-ttu-id="42ed9-122">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="42ed9-122">Azs.Backup.Admin</span></span>
    * <span data-ttu-id="42ed9-123">Set-AzsBackupShare ist ein Alias, jetzt Cmdlet Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="42ed9-123">Set-AzsBackupShare is an alias now to the cmdlet Set-AzsBackupConfiguration</span></span>
    * <span data-ttu-id="42ed9-124">Get-AzsBackupLocation ist ein Alias, jetzt Cmdlet Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="42ed9-124">Get-AzsBackupLocation is an alias now to the cmdlet Get-AzsBackupConfiguration</span></span>
    * <span data-ttu-id="42ed9-125">Set-AzsBackupConfiguration, Parameter „BackupShare“ ist jetzt ein Alias für den Parameterpfad</span><span class="sxs-lookup"><span data-stu-id="42ed9-125">Set-AzsBackupConfiguration, the parameter BackupShare is an alias now for the parameter path</span></span>
* <span data-ttu-id="42ed9-126">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="42ed9-126">Azs.Subscriptions</span></span>
    * <span data-ttu-id="42ed9-127">Get-AzsDelegatedProviderOffer, Parameter „OfferName“ ist jetzt ein Alias für „Offer“</span><span class="sxs-lookup"><span data-stu-id="42ed9-127">Get-AzsDelegatedProviderOffer, the parameter OfferName is now an alias for Offer</span></span>
* <span data-ttu-id="42ed9-128">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="42ed9-128">Azs.Subscriptions.Admin</span></span>
    * <span data-ttu-id="42ed9-129">Get-AzsDelegatedProviderOffer, Parameter „OfferName“ ist jetzt ein Alias für „Offer“</span><span class="sxs-lookup"><span data-stu-id="42ed9-129">Get-AzsDelegatedProviderOffer, the parameter OfferName is now an alias for Offer</span></span>

## <a name="content"></a><span data-ttu-id="42ed9-130">Inhalt:</span><span class="sxs-lookup"><span data-stu-id="42ed9-130">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="42ed9-131">Azure-Bridge</span><span class="sxs-lookup"><span data-stu-id="42ed9-131">Azure Bridge</span></span>
<span data-ttu-id="42ed9-132">Vorschauversion des AzureBridge-Administratormoduls von Azure Stack, mit dem Sie Images aus Azure syndizieren können.</span><span class="sxs-lookup"><span data-stu-id="42ed9-132">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="42ed9-133">Backup</span><span class="sxs-lookup"><span data-stu-id="42ed9-133">Backup</span></span>
<span data-ttu-id="42ed9-134">Vorschauversion des Backup-Administratormoduls, das Administratoren Folgendes ermöglicht:</span><span class="sxs-lookup"><span data-stu-id="42ed9-134">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="42ed9-135">Konfigurieren des Speicherorts von Sicherungen</span><span class="sxs-lookup"><span data-stu-id="42ed9-135">Configure where backups are stored</span></span>
- <span data-ttu-id="42ed9-136">Durchführen von Sicherungen</span><span class="sxs-lookup"><span data-stu-id="42ed9-136">Perform backups</span></span>
- <span data-ttu-id="42ed9-137">Auflisten und Wiederherstellen abgeschlossener Sicherungen</span><span class="sxs-lookup"><span data-stu-id="42ed9-137">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="42ed9-138">Commerce</span><span class="sxs-lookup"><span data-stu-id="42ed9-138">Commerce</span></span>
<span data-ttu-id="42ed9-139">Vorschauversion des Commerce-Administratormoduls von Azure Stack, mit dem die aggregierte Datennutzung für das gesamte Azure Stack-System angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="42ed9-139">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="42ed9-140">Compute</span><span class="sxs-lookup"><span data-stu-id="42ed9-140">Compute</span></span>
<span data-ttu-id="42ed9-141">Vorschauversion des Compute-Administratormoduls von Azure Stack mit Funktionen zur Verwaltung von Computekontingenten, Plattformimages, verwalteten Datenträgern und VM-Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="42ed9-141">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="42ed9-142">Fabric</span><span class="sxs-lookup"><span data-stu-id="42ed9-142">Fabric</span></span>
<span data-ttu-id="42ed9-143">Vorschauversion des Fabric-Administratormoduls von Azure Stack, mit dem Administratoren Infrastrukturkomponenten anzeigen und verwalten können:</span><span class="sxs-lookup"><span data-stu-id="42ed9-143">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="42ed9-144">Beenden, Starten und Herunterfahren von Skalierungseinheitknoten</span><span class="sxs-lookup"><span data-stu-id="42ed9-144">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="42ed9-145">Entladen und Fortsetzen von Skalierungseinheitknoten für FRU-bezogene Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="42ed9-145">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="42ed9-146">Reparieren von Skalierungseinheitknoten</span><span class="sxs-lookup"><span data-stu-id="42ed9-146">Repair of scale unit nodes</span></span>
- <span data-ttu-id="42ed9-147">Neustarten der Infrastrukturrolle</span><span class="sxs-lookup"><span data-stu-id="42ed9-147">Restart of Infrastructure role</span></span>
- <span data-ttu-id="42ed9-148">Beenden, Starten und Herunterfahren von Instanzen der Infrastrukturrolle</span><span class="sxs-lookup"><span data-stu-id="42ed9-148">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="42ed9-149">Erstellen neuer IP-Pools</span><span class="sxs-lookup"><span data-stu-id="42ed9-149">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="42ed9-150">Gallery</span><span class="sxs-lookup"><span data-stu-id="42ed9-150">Gallery</span></span>
<span data-ttu-id="42ed9-151">Vorschauversion des Gallery-Administratormoduls von Azure Stack mit Funktionen zum Verwalten von Katalogelementen im Azure Stack-Marketplace.</span><span class="sxs-lookup"><span data-stu-id="42ed9-151">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="42ed9-152">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="42ed9-152">Infrastructure Insights</span></span>
<span data-ttu-id="42ed9-153">Vorschauversion des Infrastructure Insights-Administratormoduls, das Administratoren Folgendes ermöglicht:</span><span class="sxs-lookup"><span data-stu-id="42ed9-153">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="42ed9-154">Anzeigen der Integrität ihrer Azure Stack-Stempelressourcen</span><span class="sxs-lookup"><span data-stu-id="42ed9-154">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="42ed9-155">Anzeigen und Verwalten von Warnungen</span><span class="sxs-lookup"><span data-stu-id="42ed9-155">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="42ed9-156">KeyVault</span><span class="sxs-lookup"><span data-stu-id="42ed9-156">KeyVault</span></span>
<span data-ttu-id="42ed9-157">Vorschauversion des KeyVault-Administratormoduls von Azure Stack, mit dem Administratoren KeyVault-Kontingente anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="42ed9-157">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="42ed9-158">Netzwerk</span><span class="sxs-lookup"><span data-stu-id="42ed9-158">Network</span></span>
<span data-ttu-id="42ed9-159">Vorschauversion des Network-Administratormoduls, das Folgendes ermöglicht:</span><span class="sxs-lookup"><span data-stu-id="42ed9-159">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="42ed9-160">Verwalten von Netzwerkkontingenten</span><span class="sxs-lookup"><span data-stu-id="42ed9-160">Management of network quotas</span></span>
- <span data-ttu-id="42ed9-161">Anzeigen zugeordneter Netzwerkressourcen (beispielsweise öffentliche IP-Adressen, virtuelle Netzwerke oder Lastenausgleichsmodule)</span><span class="sxs-lookup"><span data-stu-id="42ed9-161">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="42ed9-162">Stellt ein Cmdlet zum Anzeigen einer Administratorübersicht bereit.</span><span class="sxs-lookup"><span data-stu-id="42ed9-162">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="42ed9-163">Speicher</span><span class="sxs-lookup"><span data-stu-id="42ed9-163">Storage</span></span>
<span data-ttu-id="42ed9-164">Vorschauversion des Storage-Administratormoduls von Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="42ed9-164">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="42ed9-165">Dieses Release bietet Funktionen für Folgendes:</span><span class="sxs-lookup"><span data-stu-id="42ed9-165">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="42ed9-166">Verwalten von Speicherkontingenten</span><span class="sxs-lookup"><span data-stu-id="42ed9-166">Manage storage quotas</span></span>
- <span data-ttu-id="42ed9-167">Durchführen der Garbage Collection für gelöschte Speicherressourcen</span><span class="sxs-lookup"><span data-stu-id="42ed9-167">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="42ed9-168">Wiederherstellen gelöschter Speicherkonten</span><span class="sxs-lookup"><span data-stu-id="42ed9-168">Restore deleted storage accounts</span></span>
- <span data-ttu-id="42ed9-169">Migrieren von Containern zwischen Freigaben</span><span class="sxs-lookup"><span data-stu-id="42ed9-169">Migrate containers from one share to another</span></span>
- <span data-ttu-id="42ed9-170">Anzeigen von Informationen zu den einzelnen Speicherkomponenten</span><span class="sxs-lookup"><span data-stu-id="42ed9-170">View information about the individual storage components</span></span>
- <span data-ttu-id="42ed9-171">Anzeigen von Nutzungs- und Leistungsinformationen</span><span class="sxs-lookup"><span data-stu-id="42ed9-171">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="42ed9-172">Abonnementadministrator</span><span class="sxs-lookup"><span data-stu-id="42ed9-172">Subscription Admin</span></span>
<span data-ttu-id="42ed9-173">Vorschauversion des Subscription-Administratormoduls von Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="42ed9-173">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="42ed9-174">Dieses Modul bietet Administratorfunktionen für Folgendes:</span><span class="sxs-lookup"><span data-stu-id="42ed9-174">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="42ed9-175">Verwalten von Plänen und Angeboten</span><span class="sxs-lookup"><span data-stu-id="42ed9-175">Manage plans and offers</span></span>
- <span data-ttu-id="42ed9-176">Anzeigen von Nutzungs- und Leistungsinformationen</span><span class="sxs-lookup"><span data-stu-id="42ed9-176">View usage and performance information</span></span>
- <span data-ttu-id="42ed9-177">Verwalten der RBAC</span><span class="sxs-lookup"><span data-stu-id="42ed9-177">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="42ed9-178">Abonnement</span><span class="sxs-lookup"><span data-stu-id="42ed9-178">Subscription</span></span>
<span data-ttu-id="42ed9-179">Vorschauversion des Subscription-Moduls von Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="42ed9-179">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="42ed9-180">Dieses Modul bietet Benutzerfunktionen für Folgendes:</span><span class="sxs-lookup"><span data-stu-id="42ed9-180">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="42ed9-181">Erstellen, Löschen und Aktualisieren von Abonnements</span><span class="sxs-lookup"><span data-stu-id="42ed9-181">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="42ed9-182">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="42ed9-182">Update</span></span>
<span data-ttu-id="42ed9-183">Vorschauversion des Update-Administratormoduls von Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="42ed9-183">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="42ed9-184">Dieses Modul ermöglicht Administratoren Folgendes:</span><span class="sxs-lookup"><span data-stu-id="42ed9-184">In this module administrators can:</span></span>
- <span data-ttu-id="42ed9-185">Auflisten und Installieren verfügbarer Updates</span><span class="sxs-lookup"><span data-stu-id="42ed9-185">List and install available updates</span></span>
- <span data-ttu-id="42ed9-186">Fortsetzen unterbrochener Updates</span><span class="sxs-lookup"><span data-stu-id="42ed9-186">Resume interrupted updates</span></span>
- <span data-ttu-id="42ed9-187">Anzeigen installierter Updates</span><span class="sxs-lookup"><span data-stu-id="42ed9-187">View installed updates</span></span>
