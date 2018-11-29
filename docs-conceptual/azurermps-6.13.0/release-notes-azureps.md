---
title: Azure PowerShell-Änderungsprotokoll | Microsoft-Dokumentation
description: Hierbei handelt es sich um einen Verlauf der Änderungen, die in der neuesten Version an Azure PowerShell vorgenommen wurden.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.openlocfilehash: 7f517f0b3768a2075557b131158ee1264ea9ab3f
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/29/2018
ms.locfileid: "52587838"
---
# <a name="release-notes"></a><span data-ttu-id="89de5-103">Versionshinweise</span><span class="sxs-lookup"><span data-stu-id="89de5-103">Release notes</span></span>

<span data-ttu-id="89de5-104">Hierbei handelt es sich um eine Liste der Änderungen, die in dieser Version an Azure PowerShell vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="89de5-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6130---november-2018"></a><span data-ttu-id="89de5-105">6.13.0: November 2018</span><span class="sxs-lookup"><span data-stu-id="89de5-105">6.13.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="89de5-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="89de5-106">AzureRM.Profile</span></span>
* <span data-ttu-id="89de5-107">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="89de5-107">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="89de5-108">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="89de5-108">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="89de5-109">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-109">Update dependencies for type mapping issue</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="89de5-110">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="89de5-110">AzureRM.Automation</span></span>
* <span data-ttu-id="89de5-111">Swagger-basierte Azure Automation-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="89de5-111">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="89de5-112">Cmdlets zur Updateverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-112">Added Update Management cmdlets</span></span>
* <span data-ttu-id="89de5-113">Cmdlets zur Quellcodeverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-113">Added Source Control cmdlets</span></span>
* <span data-ttu-id="89de5-114">Cmdlet „Remove-AzureRmAutomationHybridWorkerGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-114">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="89de5-115">DSC-Befehl für die Knotenregistrierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="89de5-115">Fixed the DSC Register Node command</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="89de5-116">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="89de5-116">AzureRM.Compute</span></span>
* <span data-ttu-id="89de5-117">Identitätsproblem für SystemAssigned-Identität korrigiert</span><span class="sxs-lookup"><span data-stu-id="89de5-117">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="89de5-118">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-118">Update dependencies for type mapping issue</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="89de5-119">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="89de5-119">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="89de5-120">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-120">Update dependencies for type mapping issue</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="89de5-121">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="89de5-121">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="89de5-122">Beschreibung der Beispiele für Marketplace-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-122">update the examples description for marketplace cmdlets</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="89de5-123">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="89de5-123">AzureRM.Network</span></span>
* <span data-ttu-id="89de5-124">Folgende Cmdlets hinzugefügt: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="89de5-124">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="89de5-125">ICMP wieder unterstützten AzureFirewall-Netzwerkprotokollen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-125">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="89de5-126">Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert und Überprüfung für Ziel-ID, Adresse und Port hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-126">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="89de5-127">Probleme mit Arbeitsspeicherauslastung in der VirtualNetwork-Zuordnung behoben</span><span class="sxs-lookup"><span data-stu-id="89de5-127">Fix issues with memory usage in VirtualNetwork map</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="89de5-128">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="89de5-128">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="89de5-129">Problem beim Ändern der Richtlinie für eine geschützte Dateifreigabe behoben</span><span class="sxs-lookup"><span data-stu-id="89de5-129">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="89de5-130">Richtlinienzeitzone in Großschreibung geändert</span><span class="sxs-lookup"><span data-stu-id="89de5-130">Converted policy timezone to uppercase.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="89de5-131">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="89de5-131">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="89de5-132">Korrigiertes Beispiel in „New-AzureRmRecoveryServicesAsrProtectableItem“</span><span class="sxs-lookup"><span data-stu-id="89de5-132">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="89de5-133">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-133">Update dependencies for type mapping issue</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="89de5-134">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="89de5-134">AzureRM.Relay</span></span>
* <span data-ttu-id="89de5-135">Optionaler Parameter „-KeyValue“ zu Cmdlet „New-AzureRmRelayKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht</span><span class="sxs-lookup"><span data-stu-id="89de5-135">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="89de5-136">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="89de5-136">AzureRM.Resources</span></span>
* <span data-ttu-id="89de5-137">Hilfedokumentation für ressourcenidentitätsbezogene Parameter in `New-AzureRmPolicyAssignment` und `Set-AzureRmPolicyAssignment` aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-137">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="89de5-138">Beispiel für „New-AzureRmPolicyDefinition“ hinzugefügt, das „-Metadata“ nutzt</span><span class="sxs-lookup"><span data-stu-id="89de5-138">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="89de5-139">Korrektur, um Beibehaltung von Groß-/Kleinschreibung in Tagschlüsseln in „NetStandard“ zu ermöglichen: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="89de5-139">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="89de5-140">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="89de5-140">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="89de5-141">Benachrichtigung über veraltete Elemente für anstehende wichtige Änderungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-141">Add deprecation messages for upcoming breaking changes</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="89de5-142">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="89de5-142">AzureRM.Sql</span></span>
* <span data-ttu-id="89de5-143">Neue Cmdlets für CRUD-Vorgänge in verwalteten Azure SQL-Datenbank-Instanzen und verwalteten Azure SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-143">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="89de5-144">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="89de5-144">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="89de5-145">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="89de5-145">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="89de5-146">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="89de5-146">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="89de5-147">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="89de5-147">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="89de5-148">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="89de5-148">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="89de5-149">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="89de5-149">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="89de5-150">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="89de5-150">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="89de5-151">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="89de5-151">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="89de5-152">Erweiterte Verwaltung von Überwachungsrichtlinien auf einem Server oder in einer Datenbank aktiviert</span><span class="sxs-lookup"><span data-stu-id="89de5-152">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="89de5-153">Neuer Parameter (PredicateExpression) hinzugefügt, um die Filterung von Überwachungsprotokollen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="89de5-153">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="89de5-154">Cmdlets wurden angepasst, sodass sie SQL-Clients anstelle von Legacyclients verwenden.</span><span class="sxs-lookup"><span data-stu-id="89de5-154">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="89de5-155">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="89de5-155">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="89de5-156">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="89de5-156">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="89de5-157">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="89de5-157">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="89de5-158">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="89de5-158">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="89de5-159">Problem bei Verwendung von „Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings“ mit festgelegtem Parameter für den Speicherkontonamen behoben</span><span class="sxs-lookup"><span data-stu-id="89de5-159">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="6120---november-2018"></a><span data-ttu-id="89de5-160">6.12.0: November 2018</span><span class="sxs-lookup"><span data-stu-id="89de5-160">6.12.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="89de5-161">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="89de5-161">AzureRM.Profile</span></span>
* <span data-ttu-id="89de5-162">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="89de5-162">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="89de5-163">Parameter „TenantId“ im Cmdlet „Connect-AzureRmAccount“ in „Tenant“ umbenannt und Alias für „TenantId“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-163">Rename param TenantId in cmdlet Connect-AzureRmAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="89de5-164">Beschreibung von „TenantId“ für „Connect-AzureRmAccount“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-164">Updated TenantId description for Connect-AzureRmAccount</span></span>
* <span data-ttu-id="89de5-165">Fehlermeldung für fehlgeschlagene Anmeldung bei Angabe der Mandantendomäne korrigiert</span><span class="sxs-lookup"><span data-stu-id="89de5-165">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="89de5-166">Problem in Bezug auf Kontextnamenskonflikt für Konten ohne Abonnements im Mandanten behoben</span><span class="sxs-lookup"><span data-stu-id="89de5-166">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="89de5-167">Problem mit DataLake-Endpunkten bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="89de5-167">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="89de5-168">Problem behoben, das zur Auslösung von „Disconnect-AzureRmAccount“ führte, wenn keine Verbindung bestand</span><span class="sxs-lookup"><span data-stu-id="89de5-168">Fix issue where 'Disconnect-AzureRmAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a><span data-ttu-id="89de5-169">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="89de5-169">AzureRM.Automation</span></span>
* <span data-ttu-id="89de5-170">DLL-Dateiname des Cmdlets in „Microsoft.Azure.Commands.Automation.dll“ umbenannt</span><span class="sxs-lookup"><span data-stu-id="89de5-170">Renamed cmdlet DLL filename to Microsoft.Azure.Commands.Automation.dll</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="89de5-171">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="89de5-171">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="89de5-172">Vorgang „Get-AzureRmCognitiveServicesAccountSkus“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-172">Add Get-AzureRmCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="89de5-173">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="89de5-173">AzureRM.Compute</span></span>
* <span data-ttu-id="89de5-174">Cmdlets „Add-AzureRmVmssVMDataDisk“ und „Remove-AzureRmVmssVMDataDisk“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-174">Add Add-AzureRmVmssVMDataDisk and Remove-AzureRmVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="89de5-175">„Get-AzureRmVMImage“ zeigt „AutomaticOSUpgradeProperties“ an.</span><span class="sxs-lookup"><span data-stu-id="89de5-175">Get-AzureRmVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="89de5-176">Problem behoben, aufgrund dessen die Optionswerte „SetAzureRmVMChefExtension -BootstrapOptions“ und „-JsonAttribute“ nicht im JSON-Format festgelegt wurden</span><span class="sxs-lookup"><span data-stu-id="89de5-176">Fixed SetAzureRmVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="89de5-177">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="89de5-177">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="89de5-178">Aktualisierung des DataLake-Pakets auf 1.1.10</span><span class="sxs-lookup"><span data-stu-id="89de5-178">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="89de5-179">Standardmäßige Parallelität zu Multithreadvorgängen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-179">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="89de5-180">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="89de5-180">AzureRM.Insights</span></span>
* <span data-ttu-id="89de5-181">Problem Nr. 7267 behoben (Bereich für automatische Skalierung)</span><span class="sxs-lookup"><span data-stu-id="89de5-181">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="89de5-182">Probleme beim Erstellen einer neuen Regel für die automatische Skalierung, aufgrund derer die aufgelisteten Parameter nicht richtig festgelegt wurden (Es wurde stets der Standardwert festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="89de5-182">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="89de5-183">Problem Nr. 7513 behoben [Insights] „Set-AzureRMDiagnosticSetting“ erfordert die explizite Angabe von Kategorien während der Erstellung der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="89de5-183">Fixed issue #7513 [Insights] Set-AzureRMDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="89de5-184">Nun erfordert das Cmdlet nicht die explizite Angabe der Kategorien, die während der Erstellung aktiviert werden sollen. Das bedeutet, es funktioniert wie dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="89de5-184">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="89de5-185">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="89de5-185">AzureRM.Network</span></span>
* <span data-ttu-id="89de5-186">„PeeringType“ wurde geändert und ist nun ein erforderlicher Parameter für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="89de5-186">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="89de5-187">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="89de5-187">Get-AzureRmExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="89de5-188">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="89de5-188">Get-AzureRmExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="89de5-189">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="89de5-189">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="89de5-190">Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="89de5-190">Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="89de5-191">Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="89de5-191">Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="89de5-192">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="89de5-192">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="89de5-193">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="89de5-193">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="89de5-194">Cmdlets für Richtlinienwartung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-194">Added policy remediation cmdlets</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="89de5-195">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="89de5-195">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="89de5-196">Unterstützung für Azure-Dateifreigaben in Wiederherstellungsdiensten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-196">Added support for azure file shares in recovery services.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="89de5-197">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="89de5-197">AzureRM.Resources</span></span>
* <span data-ttu-id="89de5-198">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="89de5-198">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="89de5-199">Zulassen der Auflistung von Ressourcen mithilfe des Parameters „-ResourceId“ für „Get-AzureRmResource“</span><span class="sxs-lookup"><span data-stu-id="89de5-199">Allow listing resources using the '-ResourceId' parameter for 'Get-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="89de5-200">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="89de5-200">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="89de5-201">Schreibgeschützte Eigenschaft „MigrationState“ zu „PSServiceBusMigrationConfigurationAttributes“ hinzugefügt, was das Ermitteln des Migrationsstatus ermöglicht</span><span class="sxs-lookup"><span data-stu-id="89de5-201">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="89de5-202">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="89de5-202">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="89de5-203">Hinzufügen des Zertifikats zu Linux VMSS korrigiert</span><span class="sxs-lookup"><span data-stu-id="89de5-203">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="89de5-204">„Add-AzureRmServiceFabricClusterCertificate“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="89de5-204">Fix 'Add-AzureRmServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="89de5-205">Verwenden des richtigen Fingerabdrucks aus dem neuen Zertifikat (Azure/service-fabric-issues#932)</span><span class="sxs-lookup"><span data-stu-id="89de5-205">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="89de5-206">Richtige Anzeige von Ausnahmen (Azure/service-fabric-issues#1054)</span><span class="sxs-lookup"><span data-stu-id="89de5-206">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="89de5-207">„Update-AzureRmServiceFabricDurability“ korrigiert, um die Clusterkonfiguration zu aktualisieren, bevor der VMSS-Vorgang „CreateOrUpdate“ gestartet wird</span><span class="sxs-lookup"><span data-stu-id="89de5-207">Fix 'Update-AzureRmServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="6110---october-2018"></a><span data-ttu-id="89de5-208">6.11.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="89de5-208">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="89de5-209">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="89de5-209">AzureRM.Profile</span></span>
* <span data-ttu-id="89de5-210">Problem mit „Get-AzureRmSubscription“ in CloudShell behoben</span><span class="sxs-lookup"><span data-stu-id="89de5-210">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="89de5-211">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="89de5-211">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="89de5-212">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="89de5-212">AzureRM.Backup</span></span>
* <span data-ttu-id="89de5-213">Azure Backup-Cmdlets als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="89de5-213">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="89de5-214">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="89de5-214">AzureRM.Compute</span></span>
* <span data-ttu-id="89de5-215">Neue Größen zur Whitelist von VM-Größen hinzugefügt, für die bei Verwendung des einfachen Parametersatzes für „New-AzureRmVm“ der beschleunigte Netzwerkbetrieb aktiviert wird</span><span class="sxs-lookup"><span data-stu-id="89de5-215">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="89de5-216">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="89de5-216">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="89de5-217">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="89de5-217">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="89de5-218">Unterstützung für Regeln für virtuelle Netzwerke hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-218">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="89de5-219">Get-AzureRmDataLakeStoreVirtualNetworkRule: Ruft Regel für virtuelles Azure Data Lake Store-Netzwerk ab oder listet sie auf.</span><span class="sxs-lookup"><span data-stu-id="89de5-219">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="89de5-220">Add-AzureRmDataLakeStoreVirtualNetworkRule: Fügt dem angegebenen Data Lake Store-Konto eine Regel für das virtuelle Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="89de5-220">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="89de5-221">Set-AzureRmDataLakeStoreVirtualNetworkRule: Ändert die angegebene Regel für das virtuelle Netzwerk im angegebenen Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="89de5-221">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="89de5-222">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Löscht eine Regel für das virtuelle Azure Data Lake Store-Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="89de5-222">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="89de5-223">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="89de5-223">AzureRM.Network</span></span>
* <span data-ttu-id="89de5-224">Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert, Protokollwert wird jetzt an Back-End übergeben.</span><span class="sxs-lookup"><span data-stu-id="89de5-224">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="89de5-225">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="89de5-225">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="89de5-226">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="89de5-226">AzureRM.Resources</span></span>
* <span data-ttu-id="89de5-227">Problem behoben, aufgrund dessen „Get-AzureRMRoleDefinition“ eine unverständliche Ausnahme auslöst (wenn das Standardprofil kein Abonnement enthält und kein Bereich festgelegt ist) indem im Szenario eine aussagekräftige Ausnahme hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="89de5-227">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="89de5-228">Außerdem wurde der Standardparametersatz auf „RoleDefinitionNameParameterSet“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="89de5-228">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="89de5-229">6.10.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="89de5-229">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="89de5-230">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="89de5-230">Azure.Storage</span></span>
* <span data-ttu-id="89de5-231">Fehler beim Kopieren von Blobs/Dateien behoben, aufgrund dessen bei einem Metadatenproblem des Ziels keine Metadaten kopiert wurden</span><span class="sxs-lookup"><span data-stu-id="89de5-231">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="89de5-232">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="89de5-232">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="89de5-233">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="89de5-233">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="89de5-234">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="89de5-234">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="89de5-235">„Get-AzureRmCognitiveServicesAccountSkus“ wird ohne vorhandenes Konto unterstützt.</span><span class="sxs-lookup"><span data-stu-id="89de5-235">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="89de5-236">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="89de5-236">AzureRM.Compute</span></span>
* <span data-ttu-id="89de5-237">Korrektur von „Get-AzureRmVM -ResourceGroupName <rg>“ sodass ggf. mehr als 50 Ergebnisse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="89de5-237">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="89de5-238">Der Cmdlet-Hilfe zu „New-AzureRmVmss“ wurde ein Beispiel für „SimpleParameterSet“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="89de5-238">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="89de5-239">Tippfehler in der Azure Disk Encryption-Statusmeldung behoben</span><span class="sxs-lookup"><span data-stu-id="89de5-239">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="89de5-240">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="89de5-240">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="89de5-241">Die Version des ADF .Net-SDK wurde auf 2.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="89de5-241">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="89de5-242">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="89de5-242">AzureRM.Network</span></span>
* <span data-ttu-id="89de5-243">NetworkProfile-Funktionalität wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="89de5-243">Added NetworkProfile functionality.</span></span> <span data-ttu-id="89de5-244">Neue Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-244">new cmdlets added</span></span>
    - <span data-ttu-id="89de5-245">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="89de5-245">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="89de5-246">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="89de5-246">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="89de5-247">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="89de5-247">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="89de5-248">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="89de5-248">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="89de5-249">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="89de5-249">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="89de5-250">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="89de5-250">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="89de5-251">Dienstzuordnungslink in Subnetzmodell hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-251">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="89de5-252">Cmdlets „New-AzureRmVirtualNetworkTap“, „Get-AzureRmVirtualNetworkTap“, „Set-AzureRmVirtualNetworkTap“, „Remove-AzureRmVirtualNetworkTap“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-252">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="89de5-253">Cmdlets „Set-AzureRmNEtworkInterfaceTapConfig“, „Get-AzureRmNEtworkInterfaceTapConfig“, „Remove-AzureRmNEtworkInterfaceTapConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-253">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="89de5-254">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="89de5-254">AzureRM.RedisCache</span></span>
* <span data-ttu-id="89de5-255">Künftig sind beliebige Zeichenfolgen als Größenparameter zulässig.</span><span class="sxs-lookup"><span data-stu-id="89de5-255">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="89de5-256">P5 in Popup „PSArgumentCompleter“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-256">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="89de5-257">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="89de5-257">AzureRM.Resources</span></span>
* <span data-ttu-id="89de5-258">Fehlender Parameter „-Mode“ zu „Set-AzureRmPolicyDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-258">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="89de5-259">Cmdlet-Fehler bei „Fix Get-AzureRmProviderOperation“ für Vorgänge mit Ursprung behoben, der den Benutzer enthält</span><span class="sxs-lookup"><span data-stu-id="89de5-259">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="89de5-260">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="89de5-260">AzureRM.Sql</span></span>
* <span data-ttu-id="89de5-261">Problem behoben, aufgrund dessen einige Sicherungs-Cmdlets das aktuelle Azure-Abonnements nicht erkannt haben</span><span class="sxs-lookup"><span data-stu-id="89de5-261">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="89de5-262">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="89de5-262">AzureRM.Storage</span></span>
* <span data-ttu-id="89de5-263">Der Abruf der Speicherressourcennutzung eines bestimmten Standorts wird jetzt unterstützt, und das Hinzufügen einer Warnmeldung für den Abruf der globalen Speicherressourcennutzung ist überflüssig.</span><span class="sxs-lookup"><span data-stu-id="89de5-263">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="89de5-264">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="89de5-264">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="89de5-265">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="89de5-265">AzureRM.Websites</span></span>
* <span data-ttu-id="89de5-266">Neues Cmdlet „Get-AzureRMWebAppContainerContinuousDeploymentUrl“ zum Abruf der Webhook-URL von Continuous Deployment für Container</span><span class="sxs-lookup"><span data-stu-id="89de5-266">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="89de5-267">Neue Cmdlets „New-AzureRMWebAppContainerPSSession“ und „Enter-WebAppContainerPSSession“ zum Initiieren einer PowerShell-Remotesitzung in einer Windows-Container-App</span><span class="sxs-lookup"><span data-stu-id="89de5-267">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="89de5-268">6.9.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="89de5-268">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="89de5-269">Allgemein</span><span class="sxs-lookup"><span data-stu-id="89de5-269">General</span></span>
* <span data-ttu-id="89de5-270">AzureRM.SignalR wurde dem Rollupmodul AzureRM hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-270">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="89de5-271">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="89de5-271">AzureRM.Profile</span></span>
* <span data-ttu-id="89de5-272">Kleinere Änderungen am allgemeinen Speichercode</span><span class="sxs-lookup"><span data-stu-id="89de5-272">Minor changes to the storage common code</span></span>
* <span data-ttu-id="89de5-273">Hilfedateien aktualisiert, um vollständige Parametertypen einzubinden.</span><span class="sxs-lookup"><span data-stu-id="89de5-273">Updated help files to include full parameter types.</span></span>
* <span data-ttu-id="89de5-274">„-ServicePrincipal“ im Parametersatz „ServicePrincipalCertificateWithSubscriptionId“ in nicht obligatorisch geändert</span><span class="sxs-lookup"><span data-stu-id="89de5-274">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="89de5-275">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="89de5-275">Azure.Storage</span></span>
* <span data-ttu-id="89de5-276">Unterstützung für die Erstellung des Speicherkontexts mit OAuth.</span><span class="sxs-lookup"><span data-stu-id="89de5-276">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="89de5-277">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="89de5-277">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="89de5-278">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="89de5-278">AzureRM.Cdn</span></span>
* <span data-ttu-id="89de5-279">Standard_Microsoft in SKU für CDN-Preise hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="89de5-279">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="89de5-280">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="89de5-280">AzureRM.Compute</span></span>
* <span data-ttu-id="89de5-281">Abhängigkeiten für Key Vault und Storage in allgemeine Abhängigkeiten verschieben</span><span class="sxs-lookup"><span data-stu-id="89de5-281">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="89de5-282">Unterstützung für weitere VM-Größen zu AEM-Cmdlets hinzufügen</span><span class="sxs-lookup"><span data-stu-id="89de5-282">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="89de5-283">Parameter „PublicIPPrefix“ zu „New-AzureRmVmssIpConfig“ hinzufügen</span><span class="sxs-lookup"><span data-stu-id="89de5-283">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="89de5-284">Parameter „ResourceId“ zu Cmdlet „Invoke-AzureRmVMRunCommand“ hinzufügen</span><span class="sxs-lookup"><span data-stu-id="89de5-284">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="89de5-285">Cmdlet „Invoke-AzureRmVmssVMRunCommand“ hinzufügen</span><span class="sxs-lookup"><span data-stu-id="89de5-285">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="89de5-286">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="89de5-286">AzureRM.Dns</span></span>
* <span data-ttu-id="89de5-287">Unterstützung für Aliaseintrag während der Erstellung des DNS-Eintrags hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-287">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="89de5-288">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="89de5-288">AzureRM.Insights</span></span>
* <span data-ttu-id="89de5-289">Probleme #6833 und #7102 behoben (Bereich „Diagnoseeinstellungen“)</span><span class="sxs-lookup"><span data-stu-id="89de5-289">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="89de5-290">Probleme mit dem Standardnamen, also „service“, beim Erstellen und Auflisten/Abrufen von Diagnoseeinstellungen</span><span class="sxs-lookup"><span data-stu-id="89de5-290">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="89de5-291">Probleme beim Erstellen von Diagnoseeinstellungen mit Kategorien</span><span class="sxs-lookup"><span data-stu-id="89de5-291">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="89de5-292">Meldung zur Einstellung der Unterstützung für Metrikaggregationsintervall-Parameter</span><span class="sxs-lookup"><span data-stu-id="89de5-292">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="89de5-293">Aggregationsintervall-Parameter werden weiterhin akzeptiert (Änderung ohne Funktionsbeeinträchtigung), aber sie werden auf dem Back-End ignoriert, da nur PT1M gültig ist</span><span class="sxs-lookup"><span data-stu-id="89de5-293">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="89de5-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="89de5-294">AzureRM.Network</span></span>
* <span data-ttu-id="89de5-295">Änderungen an LoadBalancer-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="89de5-295">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="89de5-296">LoadBalancerInboundNatPoolConfig: Parameter IdleTimeoutInMinutes, EnableFloatingIp und EnableTcpReset hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-296">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="89de5-297">LoadBalancerInboundNatRuleConfig: Parameter EnableTcpReset hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-297">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="89de5-298">LoadBalancerRuleConfig: Parameter EnableTcpReset hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-298">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="89de5-299">LoadBalancerProbeConfig: Unterstützung für Wert „Https“ für Parameter „Protocol“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-299">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="89de5-300">Neue Befehle für neue Unterressource „OutboundRule“ von LoadBalancer hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-300">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="89de5-301">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="89de5-301">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="89de5-302">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="89de5-302">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="89de5-303">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="89de5-303">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="89de5-304">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="89de5-304">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="89de5-305">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="89de5-305">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="89de5-306">Neue HostedWorkloads-Eigenschaft für PSNetworkInterface hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-306">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="89de5-307">Neue Cmdlets für Feature: Azure Firewall über ARM</span><span class="sxs-lookup"><span data-stu-id="89de5-307">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="89de5-308">Get-AzureRmFirewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-308">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="89de5-309">Set-AzureRmFirewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-309">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="89de5-310">New-AzureRmFirewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-310">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="89de5-311">Remove-AzureRmFirewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-311">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="89de5-312">New-AzureRmFirewallApplicationRuleCollection hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-312">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="89de5-313">New-AzureRmFirewallApplicationRule hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-313">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="89de5-314">New-AzureRmFirewallNatRuleCollection hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-314">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="89de5-315">New-AzureRmFirewallNatRule hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-315">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="89de5-316">New-AzureRmFirewallNetworkRuleCollection hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-316">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="89de5-317">New-AzureRmFirewallNetworkRule hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-317">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="89de5-318">Unterstützung für vertrauenswürdiges Stammzertifikat und Konfiguration der automatischen Skalierung in Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-318">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="89de5-319">Neue Cmdlets hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="89de5-319">New Cmdlets added:</span></span>
      - <span data-ttu-id="89de5-320">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="89de5-320">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="89de5-321">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="89de5-321">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="89de5-322">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="89de5-322">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="89de5-323">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="89de5-323">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="89de5-324">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="89de5-324">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="89de5-325">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="89de5-325">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="89de5-326">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="89de5-326">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="89de5-327">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="89de5-327">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="89de5-328">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="89de5-328">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="89de5-329">Cmdlets mit optionalem Parameter „-TrustedRootCertificate“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-329">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="89de5-330">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="89de5-330">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="89de5-331">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="89de5-331">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="89de5-332">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="89de5-332">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="89de5-333">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="89de5-333">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="89de5-334">Cmdlets mit optionalem Parameter „-AutoscaleConfiguration“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-334">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="89de5-335">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="89de5-335">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="89de5-336">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="89de5-336">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="89de5-337">Cmdlet für Schnittstellenendpunkt Get-AzureInterfaceEndpoint hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-337">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="89de5-338">Unterstützung für mehrere Adresspräfixe in einem Subnetz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="89de5-338">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="89de5-339">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="89de5-339">Updated cmdlets:</span></span>
  - <span data-ttu-id="89de5-340">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="89de5-340">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="89de5-341">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="89de5-341">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="89de5-342">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="89de5-342">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="89de5-343">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="89de5-343">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="89de5-344">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="89de5-344">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="89de5-345">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="89de5-345">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="89de5-346">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="89de5-346">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="89de5-347">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="89de5-347">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="89de5-348">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="89de5-348">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="89de5-349">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="89de5-349">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="89de5-350">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="89de5-350">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="89de5-351">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="89de5-351">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="89de5-352">New-AzureRmNetworkInterfaceIpConfig – Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="89de5-352">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="89de5-353">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="89de5-353">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="89de5-354">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="89de5-354">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="89de5-355">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="89de5-355">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="89de5-356">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="89de5-356">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="89de5-357">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="89de5-357">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="89de5-358">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="89de5-358">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="89de5-359">Cmdlets für die Subnetzdelegierung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="89de5-359">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="89de5-360">New-AzureRmDelegation: Erstellt eine neue Delegierung, die einem Subnetz hinzugefügt werden kann</span><span class="sxs-lookup"><span data-stu-id="89de5-360">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="89de5-361">Remove-AzureRmDelegation: Nutzt ein Subnetz und entfernt den bereitgestellten Delegierungsnamen aus diesem Subnetz</span><span class="sxs-lookup"><span data-stu-id="89de5-361">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="89de5-362">Add-AzureRmDelegation: Nutzt ein Subnetz und fügt den angegebenen Dienstnamen diesem Subnetz als Delegierung hinzu</span><span class="sxs-lookup"><span data-stu-id="89de5-362">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="89de5-363">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="89de5-363">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="89de5-364">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="89de5-364">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="89de5-365">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="89de5-365">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="89de5-366">Unterstützung für verwalteten Datenträger</span><span class="sxs-lookup"><span data-stu-id="89de5-366">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="89de5-367">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="89de5-367">AzureRM.RedisCache</span></span>
* <span data-ttu-id="89de5-368">Insights-Abhängigkeit aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="89de5-368">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="89de5-369">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="89de5-369">AzureRM.Resources</span></span>
* <span data-ttu-id="89de5-370">New-AzureRmResourceGroupDeployment mit neuem Parameter „RollbackAction“ aktualisieren</span><span class="sxs-lookup"><span data-stu-id="89de5-370">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="89de5-371">Unterstützung für OnErrorDeployment mit dem neuen Parameter hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="89de5-371">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="89de5-372">Unterstützung für verwaltete Identität in Richtlinienzuweisungen.</span><span class="sxs-lookup"><span data-stu-id="89de5-372">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="89de5-373">Parameter mit Standardwerten sind nicht mehr erforderlich, wenn eine Richtlinie mit „New-AzureRmPolicyAssignment“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="89de5-373">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="89de5-374">Neues Cmdlet „Get-AzureRmPolicyAlias“ zum Abrufen von Richtlinienaliasen hinzufügen</span><span class="sxs-lookup"><span data-stu-id="89de5-374">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="89de5-375">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="89de5-375">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="89de5-376">Problem #7161 behoben</span><span class="sxs-lookup"><span data-stu-id="89de5-376">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="89de5-377">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="89de5-377">AzureRM.SignalR</span></span>
* <span data-ttu-id="89de5-378">SKU-Namen auf Free_F1 und Standard_S1 aktualisieren</span><span class="sxs-lookup"><span data-stu-id="89de5-378">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="89de5-379">Versionsfeld zum PSSignalRResource-Objekt und Verbindungszeichenfolge zum PSSignalRKeys-Objekt hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="89de5-379">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="89de5-380">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="89de5-380">AzureRM.Storage</span></span>
* <span data-ttu-id="89de5-381">Unterstützung für Unveränderlichkeitsrichtlinie in AzureRm.Storage</span><span class="sxs-lookup"><span data-stu-id="89de5-381">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="89de5-382">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="89de5-382">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="89de5-383">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="89de5-383">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="89de5-384">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="89de5-384">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="89de5-385">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="89de5-385">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="89de5-386">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="89de5-386">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="89de5-387">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="89de5-387">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="89de5-388">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="89de5-388">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="89de5-389">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="89de5-389">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="89de5-390">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="89de5-390">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="89de5-391">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="89de5-391">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="89de5-392">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="89de5-392">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="89de5-393">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="89de5-393">AzureRM.Websites</span></span>
* <span data-ttu-id="89de5-394">Zwei neue Cmdlets hinzugefügt: Get-AzureRmDeletedWebApp und Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="89de5-394">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="89de5-395">New-AzureRmAppServicePlan -HyperV-Switch für „App Service-Plan erstellen“ mit Windows-Container hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-395">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="89de5-396">New-AzureRmWebApp/New-AzureRmWebAppSlot/Set-AzureRmWebApp/Set-AzureRmWebAppSlot: Neue Parameter (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) für die Erstellung und Verwaltung der Windows-Container-App hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-396">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="89de5-397">6.8.1: August 2018</span><span class="sxs-lookup"><span data-stu-id="89de5-397">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="89de5-398">Allgemein</span><span class="sxs-lookup"><span data-stu-id="89de5-398">General</span></span>
* <span data-ttu-id="89de5-399">Das Problem, dass Standardressourcengruppen nicht festgelegt wurden, wurde behoben.</span><span class="sxs-lookup"><span data-stu-id="89de5-399">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="89de5-400">Allgemeine Laufzeitassemblys aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-400">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="89de5-401">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="89de5-401">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="89de5-402">Das Problem, dass Standardressourcengruppen nicht festgelegt wurden, wurde behoben.</span><span class="sxs-lookup"><span data-stu-id="89de5-402">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="89de5-403">Problem https://github.com/Azure/azure-powershell/issues/6603 behoben</span><span class="sxs-lookup"><span data-stu-id="89de5-403">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="89de5-404">Die Cmdlets „Import-AzureRmApiManagementApi“ und „\*-AzureRmApiManagementCertificate“ können jetzt relative Pfade verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="89de5-404">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="89de5-405">Problem https://github.com/Azure/azure-powershell/issues/6879 behoben</span><span class="sxs-lookup"><span data-stu-id="89de5-405">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="89de5-406">„CertificateInformation“ ist eine festlegbare Eigenschaft, die die ordnungsgemäße Funktionsweise des Cmdlets „Set-AzureRmApiManagement“ ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="89de5-406">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="89de5-407">Behoben durch Upgrade auf NuGet-Paket „4.0.4-preview“</span><span class="sxs-lookup"><span data-stu-id="89de5-407">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="89de5-408">Problem https://github.com/Azure/azure-powershell/issues/6853 behoben</span><span class="sxs-lookup"><span data-stu-id="89de5-408">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="89de5-409">OData-Filter für die Suche anhand des Namens korrigiert (Produkt)</span><span class="sxs-lookup"><span data-stu-id="89de5-409">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="89de5-410">Problem https://github.com/Azure/azure-powershell/issues/6814 behoben</span><span class="sxs-lookup"><span data-stu-id="89de5-410">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="89de5-411">OData-Filter für die Suche anhand des Namens korrigiert (API)</span><span class="sxs-lookup"><span data-stu-id="89de5-411">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="89de5-412">Unterstützung für AzureMonitor-Protokollierung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-412">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="89de5-413">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="89de5-413">AzureRM.Compute</span></span>
* <span data-ttu-id="89de5-414">Problem des fehlenden Ziels in der Fehlerausgabe behoben</span><span class="sxs-lookup"><span data-stu-id="89de5-414">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="89de5-415">Problem mit dem Speicherkontotyp für den virtuellen Computer mit verwaltetem Datenträgern behoben</span><span class="sxs-lookup"><span data-stu-id="89de5-415">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="89de5-416">Das Problem, dass Standardressourcengruppen nicht festgelegt wurden, wurde behoben.</span><span class="sxs-lookup"><span data-stu-id="89de5-416">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="89de5-417">AEM-Erweiterungs-Cmdlets für andere Umgebungen (etwa Azure China) korrigiert</span><span class="sxs-lookup"><span data-stu-id="89de5-417">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="89de5-418">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="89de5-418">AzureRM.Network</span></span>
* <span data-ttu-id="89de5-419">Standarddarstellung der Cmdlet-Ausgabe in Tabellenansicht geändert</span><span class="sxs-lookup"><span data-stu-id="89de5-419">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="89de5-420">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="89de5-420">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="89de5-421">Fehler in „Update-AzureRmPowerBIEmbeddedCapacity“ beim Skalieren der angehaltenen Kapazität behoben</span><span class="sxs-lookup"><span data-stu-id="89de5-421">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="89de5-422">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="89de5-422">AzureRM.Resources</span></span>
* <span data-ttu-id="89de5-423">Problem beim Erstellen verwalteter Anwendungen über Marketplace behoben</span><span class="sxs-lookup"><span data-stu-id="89de5-423">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="89de5-424">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="89de5-424">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="89de5-425">Behobene Probleme</span><span class="sxs-lookup"><span data-stu-id="89de5-425">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="89de5-426">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="89de5-426">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="89de5-427">Unterstützung für Routingmethode „MultiValue“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-427">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="89de5-428">Neuer Parameter „MaxReturn“ für Routingtyp „MultiValue“</span><span class="sxs-lookup"><span data-stu-id="89de5-428">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="89de5-429">Unterstützung für Subnetzroutingmethode hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-429">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="89de5-430">Unterstützung für IP-Adressbereiche (Subnetze) in Endpunkten</span><span class="sxs-lookup"><span data-stu-id="89de5-430">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="89de5-431">Unterstützung für benutzerdefinierte Header in Profilen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-431">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="89de5-432">Unterstützung für erwartete Statuscodebereiche in Profilen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-432">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="89de5-433">Unterstützung für benutzerdefinierte Header in Endpunkten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-433">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="89de5-434">6.8.0: August 2018</span><span class="sxs-lookup"><span data-stu-id="89de5-434">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="89de5-435">Allgemein</span><span class="sxs-lookup"><span data-stu-id="89de5-435">General</span></span>
* <span data-ttu-id="89de5-436">Das Problem, dass Standardressourcengruppen nicht festgelegt wurden, wurde behoben.</span><span class="sxs-lookup"><span data-stu-id="89de5-436">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="89de5-437">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="89de5-437">AzureRM.Profile</span></span>
* <span data-ttu-id="89de5-438">Ablaufeigenschaft zu Token hinzugefügt, die während „Connect-AzureRmAccount“ zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="89de5-438">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="89de5-439">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="89de5-439">AzureRM.Compute</span></span>
* <span data-ttu-id="89de5-440">Problem des fehlenden Ziels in der Fehlerausgabe behoben</span><span class="sxs-lookup"><span data-stu-id="89de5-440">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="89de5-441">Problem mit dem Speicherkontotyp für den virtuellen Computer mit verwaltetem Datenträgern behoben</span><span class="sxs-lookup"><span data-stu-id="89de5-441">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="89de5-442">AEM-Erweiterungs-Cmdlets für andere Umgebungen (etwa Azure China) korrigiert</span><span class="sxs-lookup"><span data-stu-id="89de5-442">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="89de5-443">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="89de5-443">AzureRM.IotHub</span></span>
* <span data-ttu-id="89de5-444">Beispiele für „New-AzureRmIotHubExportDevices“ und „New-AzureRmIotHubImportDevices“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="89de5-444">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="89de5-445">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="89de5-445">AzureRM.Network</span></span>
* <span data-ttu-id="89de5-446">Standarddarstellung von Modellen in Tabellenansicht geändert</span><span class="sxs-lookup"><span data-stu-id="89de5-446">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="89de5-447">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="89de5-447">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="89de5-448">Fehler in „Update-AzureRmPowerBIEmbeddedCapacity“ beim Skalieren der angehaltenen Kapazität behoben</span><span class="sxs-lookup"><span data-stu-id="89de5-448">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="89de5-449">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="89de5-449">AzureRM.Resources</span></span>
* <span data-ttu-id="89de5-450">Problem beim Erstellen der verwalteten Anwendung über Marketplace behoben</span><span class="sxs-lookup"><span data-stu-id="89de5-450">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="89de5-451">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="89de5-451">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="89de5-452">Fehlerbehebung</span><span class="sxs-lookup"><span data-stu-id="89de5-452">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="89de5-453">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="89de5-453">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="89de5-454">Unterstützung für Routingmethode „MultiValue“</span><span class="sxs-lookup"><span data-stu-id="89de5-454">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="89de5-455">Neuer Parameter „MaxReturn“ für Routingtyp „MultiValue“</span><span class="sxs-lookup"><span data-stu-id="89de5-455">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="89de5-456">Unterstützung für Subnetzroutingmethode</span><span class="sxs-lookup"><span data-stu-id="89de5-456">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="89de5-457">Unterstützung für IP-Adressbereiche (Subnetze) in Endpunkten</span><span class="sxs-lookup"><span data-stu-id="89de5-457">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="89de5-458">Unterstützung für benutzerdefinierte Header in Profilen</span><span class="sxs-lookup"><span data-stu-id="89de5-458">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="89de5-459">Unterstützung für erwartete Statuscodebereiche in Profilen</span><span class="sxs-lookup"><span data-stu-id="89de5-459">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="89de5-460">Unterstützung für benutzerdefinierte Header in Endpunkten</span><span class="sxs-lookup"><span data-stu-id="89de5-460">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="89de5-461">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="89de5-461">AzureRM.Websites</span></span>
* <span data-ttu-id="89de5-462">Das Problem, dass die Standardressourcengruppe falsch festgelegt wurde, wurde behoben.</span><span class="sxs-lookup"><span data-stu-id="89de5-462">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="89de5-463">6.7.0: August 2018</span><span class="sxs-lookup"><span data-stu-id="89de5-463">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="89de5-464">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="89de5-464">AzureRM.Profile</span></span>
* <span data-ttu-id="89de5-465">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-465">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="89de5-466">Benutzer-ID zum Standardkontextnamen hinzugefügt, um Kontextkonflikte zu vermeiden</span><span class="sxs-lookup"><span data-stu-id="89de5-466">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="89de5-467">Probleme mit „Clear-AzureRmContext“ behoben, die Fehler beim Auswählen eines Kontexts verursacht haben (6398)</span><span class="sxs-lookup"><span data-stu-id="89de5-467">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="89de5-468">Ermöglicht, dass für „Connect-AzureRmAccount“ die Mandantendomäne an den Parameter „-TenantId“ übergeben wird</span><span class="sxs-lookup"><span data-stu-id="89de5-468">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="89de5-469">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="89de5-469">Azure.Storage</span></span>
* <span data-ttu-id="89de5-470">Begrenzung von 5 TB für das Kontingent der Azure-Dateifreigabe entfernt</span><span class="sxs-lookup"><span data-stu-id="89de5-470">Remove the 5TB limitation for Azure File Share quota</span></span>
* <span data-ttu-id="89de5-471">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="89de5-471">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="89de5-472">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="89de5-472">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="89de5-473">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-473">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="89de5-474">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="89de5-474">Azure.AnalysisServices</span></span>
* <span data-ttu-id="89de5-475">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-475">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="89de5-476">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="89de5-476">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="89de5-477">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-477">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="89de5-478">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="89de5-478">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="89de5-479">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-479">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="89de5-480">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="89de5-480">AzureRM.Automation</span></span>
* <span data-ttu-id="89de5-481">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-481">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="89de5-482">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="89de5-482">AzureRM.Backup</span></span>
* <span data-ttu-id="89de5-483">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="89de5-484">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="89de5-484">AzureRM.Batch</span></span>
* <span data-ttu-id="89de5-485">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="89de5-486">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="89de5-486">AzureRM.Billing</span></span>
* <span data-ttu-id="89de5-487">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-487">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="89de5-488">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="89de5-488">AzureRM.Cdn</span></span>
* <span data-ttu-id="89de5-489">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-489">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="89de5-490">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="89de5-490">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="89de5-491">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-491">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="89de5-492">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="89de5-492">AzureRM.Compute</span></span>
* <span data-ttu-id="89de5-493">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-493">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="89de5-494">EvictionPolicy-Parameter zu „New-AzureRmVmssConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-494">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="89de5-495">Standort in „DiskFileParameterSet“ von „New-AzureRmVm“ angeben, wenn kein Ort angegeben ist</span><span class="sxs-lookup"><span data-stu-id="89de5-495">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="89de5-496">Parameterbeschreibung in „Save-AzureRmVMImage“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="89de5-496">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="89de5-497">Cmdlet „Get-AzureRmVMDiskEncryptionStatus“ für bestimmte Szenarien im Zusammenhang mit einem Durchlauf korrigiert</span><span class="sxs-lookup"><span data-stu-id="89de5-497">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="89de5-498">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="89de5-498">AzureRM.Consumption</span></span>
* <span data-ttu-id="89de5-499">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-499">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="89de5-500">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="89de5-500">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="89de5-501">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-501">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="89de5-502">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="89de5-502">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="89de5-503">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-503">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="89de5-504">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="89de5-504">AzureRM.DataFactories</span></span>
* <span data-ttu-id="89de5-505">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-505">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="89de5-506">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="89de5-506">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="89de5-507">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-507">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="89de5-508">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="89de5-508">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="89de5-509">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-509">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="89de5-510">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="89de5-510">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="89de5-511">Debuggen korrigiert, wenn „DebugPreference“ über die PowerShell-Befehlszeile festgelegt wird</span><span class="sxs-lookup"><span data-stu-id="89de5-511">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="89de5-512">Beispiel für „Set-AzureRmDataLakeStoreItemAcl“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-512">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="89de5-513">Aktualisiert auf die aktuelle Version von Azure ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="89de5-513">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="89de5-514">Beispiel für „Set-AzureRmDataLakeStoreItemAclEntry“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-514">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="89de5-515">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="89de5-515">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="89de5-516">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-516">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="89de5-517">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="89de5-517">AzureRM.Dns</span></span>
* <span data-ttu-id="89de5-518">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-518">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="89de5-519">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="89de5-519">AzureRM.EventGrid</span></span>
* <span data-ttu-id="89de5-520">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-520">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="89de5-521">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="89de5-521">AzureRM.EventHub</span></span>
* <span data-ttu-id="89de5-522">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-522">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="89de5-523">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="89de5-523">AzureRM.HDInsight</span></span>
* <span data-ttu-id="89de5-524">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-524">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="89de5-525">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="89de5-525">AzureRM.Insights</span></span>
* <span data-ttu-id="89de5-526">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-526">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="89de5-527">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="89de5-527">AzureRM.IotHub</span></span>
* <span data-ttu-id="89de5-528">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-528">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="89de5-529">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="89de5-529">AzureRM.KeyVault</span></span>
* <span data-ttu-id="89de5-530">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-530">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="89de5-531">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="89de5-531">AzureRM.LogicApp</span></span>
* <span data-ttu-id="89de5-532">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-532">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="89de5-533">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="89de5-533">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="89de5-534">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-534">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="89de5-535">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="89de5-535">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="89de5-536">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-536">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="89de5-537">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="89de5-537">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="89de5-538">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-538">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="89de5-539">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="89de5-539">AzureRM.Media</span></span>
* <span data-ttu-id="89de5-540">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-540">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="89de5-541">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="89de5-541">AzureRM.Network</span></span>
* <span data-ttu-id="89de5-542">Beispiel für „Set-AzureRmLocalNetworkGateway“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-542">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="89de5-543">Beispiele und Beschreibungen für „Add-AzureRmVirtualNetworkGatewayIpConfig“, „Get-AzureRmVirtualNetworkGatewayConnectionSharedKey“ und „New-AzureRmVirtualNetworkGatewayConnection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-543">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="89de5-544">Beispiele für „Remove-AzureRmVirtualNetworkGatewayIpConfig“ und „Reset-AzureRmVirtualNetworkGateway“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-544">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="89de5-545">Beispiel für „Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-545">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="89de5-546">Beispiel für „Set-AzureRmVirtualNetworkGatewayConnectionSharedKey“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-546">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="89de5-547">Beispiel für „Set-AzureRmVirtualNetworkGatewayConnection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-547">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="89de5-548">Cmdlets für „ApplicationSecurityGroup“, „RouteTable“ und „Usage“ mithilfe des aktuellen Code-Generators erneut erstellt</span><span class="sxs-lookup"><span data-stu-id="89de5-548">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="89de5-549">Deutlichere Formulierung der Fehlermeldung für „Get-AzureRmVirtualNetworkSubnetConfig“, wenn ein nicht vorhandenes Subnetz abgerufen wird</span><span class="sxs-lookup"><span data-stu-id="89de5-549">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="89de5-550">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="89de5-550">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="89de5-551">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-551">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="89de5-552">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="89de5-552">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="89de5-553">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-553">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="89de5-554">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="89de5-554">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="89de5-555">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-555">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="89de5-556">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="89de5-556">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="89de5-557">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-557">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="89de5-558">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="89de5-558">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="89de5-559">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-559">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="89de5-560">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="89de5-560">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="89de5-561">Richtlinienfilter zum Cmdlet „Get-AzureRmRecoveryServicesBackItem“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="89de5-561">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="89de5-562">Der Befehl gibt die Liste der Sicherungselemente zurück, die durch die angegebene Richtlinien-ID geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="89de5-562">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="89de5-563">„Microsoft.Azure.Management.RecoveryServices.Backup“ auf Version 3.0.0-preview aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-563">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="89de5-564">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-564">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="89de5-565">TargetResourceGroupName-Parameter zu „Restore-AzureRmRecoveryServicesBackupItem“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="89de5-565">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="89de5-566">Die Ressourcengruppe, in der die verwalteten Datenträger wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="89de5-566">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="89de5-567">Gilt für die Sicherung des virtuellen Computers mit verwalteten Datenträgern.</span><span class="sxs-lookup"><span data-stu-id="89de5-567">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="89de5-568">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="89de5-568">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="89de5-569">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-569">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="89de5-570">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="89de5-570">AzureRM.RedisCache</span></span>
* <span data-ttu-id="89de5-571">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-571">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="89de5-572">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="89de5-572">AzureRM.Relay</span></span>
* <span data-ttu-id="89de5-573">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-573">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="89de5-574">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="89de5-574">AzureRM.Resources</span></span>
* <span data-ttu-id="89de5-575">Unterstützung der Vorlagenbereitstellung im Abonnementbereich.</span><span class="sxs-lookup"><span data-stu-id="89de5-575">Support template deployment at subscription scope.</span></span> <span data-ttu-id="89de5-576">Neue Cmdlets hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="89de5-576">Add new Cmdlets:</span></span>
    - <span data-ttu-id="89de5-577">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="89de5-577">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="89de5-578">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="89de5-578">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="89de5-579">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="89de5-579">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="89de5-580">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="89de5-580">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="89de5-581">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="89de5-581">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="89de5-582">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="89de5-582">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="89de5-583">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="89de5-583">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="89de5-584">Problem behoben, aufgrund dessen beim Übergeben eines Kontexts an „Set-AzureRmResource“ ein Fehler auftrat</span><span class="sxs-lookup"><span data-stu-id="89de5-584">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="89de5-585">Beispiel in „New-AzureRmResourceGroupDeployment“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="89de5-585">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="89de5-586">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-586">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="89de5-587">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="89de5-587">AzureRM.Scheduler</span></span>
* <span data-ttu-id="89de5-588">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-588">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="89de5-589">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="89de5-589">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="89de5-590">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-590">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="89de5-591">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="89de5-591">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="89de5-592">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-592">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="89de5-593">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="89de5-593">AzureRM.Sql</span></span>
* <span data-ttu-id="89de5-594">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-594">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="89de5-595">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="89de5-595">AzureRM.Storage</span></span>
* <span data-ttu-id="89de5-596">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-596">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="89de5-597">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="89de5-597">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="89de5-598">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-598">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="89de5-599">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="89de5-599">AzureRM.Tags</span></span>
* <span data-ttu-id="89de5-600">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-600">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="89de5-601">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="89de5-601">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="89de5-602">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-602">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="89de5-603">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="89de5-603">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="89de5-604">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-604">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="89de5-605">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="89de5-605">AzureRM.Websites</span></span>
* <span data-ttu-id="89de5-606">Auf die aktuelle Version von Azure ClientRuntime aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-606">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="89de5-607">6.6.0 – Juli 2018</span><span class="sxs-lookup"><span data-stu-id="89de5-607">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="89de5-608">Allgemein</span><span class="sxs-lookup"><span data-stu-id="89de5-608">General</span></span>
* <span data-ttu-id="89de5-609">Alle Hilfedateien aktualisiert, um vollständige Parametertypen und die richtigen Eingabe/Ausgabe-Typen einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="89de5-609">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="89de5-610">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="89de5-610">AzureRM.Profile</span></span>
* <span data-ttu-id="89de5-611">Bibliothek „Common.Strategy“ aktualisiert, um überprüfen zu können, ob die aktuelle Konfiguration für eine Ressource mit der Zielressource kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="89de5-611">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="89de5-612">ps1xml-Typen zu „Common.Storage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-612">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="89de5-613">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="89de5-613">Azure.Storage</span></span>
* <span data-ttu-id="89de5-614">Unterstützung zum Abrufen von Speicherkontext aus „DefaultProfile“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-614">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="89de5-615">„Ps1XmlAttribute“ zu Typeneigenschaften von Cmdlet-Ausgaben hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-615">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="89de5-616">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="89de5-616">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="89de5-617">Problem https://github.com/Azure/azure-powershell/issues/6370 behoben</span><span class="sxs-lookup"><span data-stu-id="89de5-617">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="89de5-618">Fehler in Automapper behoben, um „PsApiManagementApi“ in „ApiContract“ zu verschieben</span><span class="sxs-lookup"><span data-stu-id="89de5-618">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="89de5-619">Problem https://github.com/Azure/azure-powershell/issues/6515 behoben</span><span class="sxs-lookup"><span data-stu-id="89de5-619">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="89de5-620">Fehler in „File.Save“ behoben, um Überladung mit Codierungstyp zu vermeiden</span><span class="sxs-lookup"><span data-stu-id="89de5-620">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="89de5-621">Problem https://github.com/Azure/azure-powershell/issues/6560 behoben</span><span class="sxs-lookup"><span data-stu-id="89de5-621">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="89de5-622">Upgrade auf Nuget-Version 4.0.3 durchgeführt, in der Musterausnahme in „apiId“ behoben wurde</span><span class="sxs-lookup"><span data-stu-id="89de5-622">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="89de5-623">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="89de5-623">AzureRM.Compute</span></span>
* <span data-ttu-id="89de5-624">Das Problem, aufgrund dessen beim Erstellen eines virtuellen Computers mithilfe von „DiskFileParameterSet“ in „New-AzureRmVm“ wegen einer Umbenennung des Speicherkontotyps „PremiumLRS“ ein Fehler auftrat, wurde behoben.</span><span class="sxs-lookup"><span data-stu-id="89de5-624">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="89de5-625">Cmdlet „Invoke-AzureRmVMRunCommand“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="89de5-625">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="89de5-626">„Get-AzureRmAvailabilitySet“ aktualisiert, um die Auflistung aller Verfügbarkeitsgruppen in einem Abonnement zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="89de5-626">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="89de5-627">(ResouceGroupName-Parameter ist jetzt optional.)</span><span class="sxs-lookup"><span data-stu-id="89de5-627">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="89de5-628">„SimpleParameterSet“ von „New-AzureRmVm“ aktualisiert, um Accelerated Networking auf kompatiblen virtuellen Computern zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="89de5-628">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="89de5-629">Einfacher Parametersatz „New-AzureRmVmss“ aktualisiert, sodass das Erstellen der VMSS fehlschlägt, wenn bereits ein benutzerdefinierter LB vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="89de5-629">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="89de5-630">Beispiel für „New-AzureRmDisk“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-630">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="89de5-631">Beispiel für „New-AzureRmVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-631">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="89de5-632">Beschreibung für „Set-AzureRmVMOSDisk“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-632">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="89de5-633">Beispiel 1 für „Set-AzureRmVMBginfoExtension“ aktualisiert, um Rechtschreibung und Präfix zu korrigieren.</span><span class="sxs-lookup"><span data-stu-id="89de5-633">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="89de5-634">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="89de5-634">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="89de5-635">ADF .Net SDK-Version auf 1.1.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="89de5-635">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="89de5-636">Unterstützung der Freigabe der selbstgehosteten Integration Runtime über Data Factorys hinweg.</span><span class="sxs-lookup"><span data-stu-id="89de5-636">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="89de5-637">Neuer Parameter „-SharedIntegrationRuntimeResourceId“ zu Cmdlet „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="89de5-637">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="89de5-638">Neuer optionaler Parameter „-LinkedDataFactoryName“ zu Cmdlet „Remove-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="89de5-638">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="89de5-639">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="89de5-639">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="89de5-640">DataPlane SDK-Version (Microsoft.Azure.DataLake.Store) auf 1.1.9 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-640">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="89de5-641">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="89de5-641">AzureRM.EventHub</span></span>
* <span data-ttu-id="89de5-642">Piping für „InputObject“ und „ResourceId“ in Entfernungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-642">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="89de5-643">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="89de5-643">AzureRM.Insights</span></span>
* <span data-ttu-id="89de5-644">Formatierung von „OutputType“ in Hilfedateien korrigiert</span><span class="sxs-lookup"><span data-stu-id="89de5-644">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="89de5-645">Verwendung von Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="89de5-645">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="89de5-646">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="89de5-646">AzureRM.KeyVault</span></span>
* <span data-ttu-id="89de5-647">Piping-Problem in „Set-AzureRmKeyVaultAccessPolicy“ behoben</span><span class="sxs-lookup"><span data-stu-id="89de5-647">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="89de5-648">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="89de5-648">AzureRM.Network</span></span>
* <span data-ttu-id="89de5-649">Beispiele für LoadBalancerInboundNatPoolConfig-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="89de5-649">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="89de5-650">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="89de5-650">AzureRM.Resources</span></span>
* <span data-ttu-id="89de5-651">Problem beim Angeben sowohl des Tag-Namens als auch des Werts für „Get-AzureRmResource“ behoben</span><span class="sxs-lookup"><span data-stu-id="89de5-651">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="89de5-652">Piping-Szenario mit „Set-AzureRmResource“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="89de5-652">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="89de5-653">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="89de5-653">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="89de5-654">Piping für „InputObject“ und „ResourceId“ in Entfernungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-654">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="89de5-655">Einige Probleme behoben</span><span class="sxs-lookup"><span data-stu-id="89de5-655">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="89de5-656">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="89de5-656">AzureRM.Sql</span></span>
* <span data-ttu-id="89de5-657">Unterstützung für Advanced Threat Protection für Server bei folgenden Cmdlets hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="89de5-657">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="89de5-658">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="89de5-658">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="89de5-659">Unterstützung für Sicherheitsrisikobewertung bei folgenden Cmdlets hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="89de5-659">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="89de5-660">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="89de5-660">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="89de5-661">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="89de5-661">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="89de5-662">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="89de5-662">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="89de5-663">Beispiel in „Remove-AzureRmSqlServerFirewallRule“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="89de5-663">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="89de5-664">Falsche Verarbeitung von „datetime“ für nicht US-basierte Kultur in „Get-AzureSqlSyncGroupLog“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="89de5-664">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="89de5-665">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="89de5-665">AzureRM.Storage</span></span>
* <span data-ttu-id="89de5-666">„Ps1XmlAttribute“ zu Typeneigenschaften von Cmdlet-Ausgaben hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-666">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="89de5-667">Cmdlet-Ausgabe von „StorageAccount“ in Tabellenansicht anzeigen</span><span class="sxs-lookup"><span data-stu-id="89de5-667">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="89de5-668">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="89de5-668">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="89de5-669">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="89de5-669">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="89de5-670">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="89de5-670">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="89de5-671">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="89de5-671">AzureRM.Tags</span></span>
* <span data-ttu-id="89de5-672">Falsche Anweisung aus Tag-Cmdlet-Hilfe entfernt</span><span class="sxs-lookup"><span data-stu-id="89de5-672">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="89de5-673">6.5.0 – Juli 2018</span><span class="sxs-lookup"><span data-stu-id="89de5-673">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="89de5-674">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="89de5-674">AzureRM.Profile</span></span>
* <span data-ttu-id="89de5-675">Hilfe für „Get-AzureRmContextAutosaveSetting“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-675">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="89de5-676">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="89de5-676">Azure.Storage</span></span>
* <span data-ttu-id="89de5-677">Unterstützung des Blob- oder Dateiuploads mit lesegeschütztem SAS-Token</span><span class="sxs-lookup"><span data-stu-id="89de5-677">Support Upload Blob or File with write only Sas token</span></span>
* <span data-ttu-id="89de5-678">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="89de5-678">Set-AzureStorageBlobContent</span></span>
* <span data-ttu-id="89de5-679">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="89de5-679">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="89de5-680">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="89de5-680">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="89de5-681">Erforderliche Eigenschaft „ResourceGroupName“ zu AS hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="89de5-681">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="89de5-682">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="89de5-682">AzureRM.Automation</span></span>
* <span data-ttu-id="89de5-683">Hilfe aktualisiert und Beispiel für „New-AzureRMAutomationSchedule“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-683">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="89de5-684">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="89de5-684">AzureRM.Compute</span></span>
* <span data-ttu-id="89de5-685">Parameter „-Tag“ zu „Update/New-AzureRmAvailabilitySet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-685">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="89de5-686">Beispiel für „Add-AzureRmVmssExtension“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-686">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="89de5-687">Beispiele für „Remove-AzureRmVmssExtension“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-687">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="89de5-688">Hilfe für „Set-AzureRmVMAccessExtension“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-688">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="89de5-689">„SimpleParameterSet“ für „New-AzureRmVmss“ so aktualisiert, dass „SinglePlacementGroup“ standardmäßig auf „false“ festgelegt ist, und Switch-Parameter „SinglePlacementGroup“ hinzugefügt, der dem Benutzer das Erstellen der VMSS in einer einzelnen Platzierungsgruppe ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="89de5-689">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="89de5-690">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="89de5-690">AzureRM.EventHub</span></span>
* <span data-ttu-id="89de5-691">Schreibgeschützte Eigenschaft „PendingReplicationOperationsCount“ zur Klasse „PSEventHubDRConfigurationAttributes“ hinzugefügt, welche die Anzahl der ausstehenden Replikationsvorgänge während der Replikation angibt</span><span class="sxs-lookup"><span data-stu-id="89de5-691">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="89de5-692">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="89de5-692">AzureRM.KeyVault</span></span>
* <span data-ttu-id="89de5-693">Fehlermeldung für „Set-AzureRmKeyVaultAccessPolicy“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-693">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="89de5-694">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="89de5-694">AzureRM.LogicApp</span></span>
* <span data-ttu-id="89de5-695">Fehler „Parametersatz konnte nicht aufgelöst werden“ in „New-AzureRmLogicApp“behoben</span><span class="sxs-lookup"><span data-stu-id="89de5-695">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="89de5-696">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="89de5-696">AzureRM.Network</span></span>
* <span data-ttu-id="89de5-697">Peering über mehrere virtuelle Netzwerke in mehreren Mandanten für „Set/Add-AzureRmVirtualNetworkPeering“ aktiviert</span><span class="sxs-lookup"><span data-stu-id="89de5-697">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="89de5-698">Folgende Cmdlets für Application Gateway aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-698">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="89de5-699">New-AzureRmApplicationGateway: EnableFIPS-Flag und Zonenunterstützung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-699">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="89de5-700">New-AzureRmApplicationGatewaySku: Neue SKUs „Standard_v2“ und „WAF_v2“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-700">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="89de5-701">Set-AzureRmApplicationGatewaySku: Neue SKUs „Standard_v2“ und „WAF_v2“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-701">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="89de5-702">RouteTable-Cmdlets mit aktueller Generatorversion erneut generiert</span><span class="sxs-lookup"><span data-stu-id="89de5-702">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="89de5-703">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="89de5-703">AzureRM.Relay</span></span>
* <span data-ttu-id="89de5-704">Markdowndateien aktualisiert, Problem mit Parametername in Beispiel behoben</span><span class="sxs-lookup"><span data-stu-id="89de5-704">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="89de5-705">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="89de5-705">AzureRM.Resources</span></span>
* <span data-ttu-id="89de5-706">Roleassignment- und roledefinition-Cmdlets aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="89de5-706">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="89de5-707">Zusätzliche roledefinition-Aufrufe entfernt, die als Teil des Pagings durchgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="89de5-707">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="89de5-708">Get-AzureRmRoleAssignment-Cmdlet korrigiert</span><span class="sxs-lookup"><span data-stu-id="89de5-708">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="89de5-709">Befehlsparameterfunktion von „-ExpandPrincipalGroups“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="89de5-709">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="89de5-710">Problem mit „Get-AzureRmResource“ behoben, aufgrund dessen die Groß-/Kleinschreibung des Parameters „-ResourceType“ beachtet wurde</span><span class="sxs-lookup"><span data-stu-id="89de5-710">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="89de5-711">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="89de5-711">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="89de5-712">top- und skip-Parameter zu Listen-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-712">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="89de5-713">Cmdlets für die Migration von Standard- zu Premium-Namespace hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="89de5-713">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="89de5-714">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="89de5-714">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="89de5-715">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="89de5-715">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="89de5-716">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="89de5-716">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="89de5-717">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="89de5-717">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="89de5-718">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="89de5-718">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="89de5-719">Schreibgeschützte Eigenschaft „PendingReplicationOperationsCount“ zur Klasse „PSServiceBusDRConfigurationAttributes“ hinzugefügt, welche die Anzahl der ausstehenden Replikationsvorgänge während der Replikation angibt</span><span class="sxs-lookup"><span data-stu-id="89de5-719">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="89de5-720">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="89de5-720">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="89de5-721">Beispiel für „New-AzureRmServiceFabricCluster“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-721">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="89de5-722">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="89de5-722">AzureRM.Sql</span></span>
* <span data-ttu-id="89de5-723">Neue Cmdlets für „Management.Sql“ hinzugefügt, um Kunden das Hinzufügen des TDE-Zertifikats zu einer SQL Server-Instanz oder einer verwalteten Instanz zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="89de5-723">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="89de5-724">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="89de5-724">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="89de5-725">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="89de5-725">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="89de5-726">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="89de5-726">AzureRM.Websites</span></span>
* <span data-ttu-id="89de5-727">Wenn `Set-AzureRmWebApp -AssignIdentity` und `Set-AzureRmWebAppSlot -AssignIdentity` auf „false“ festgelegt sind, wird jetzt die Identity-Eigenschaft aus dem Websiteobjekt entfernt. Auch das Vorschau-Tag wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="89de5-727">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="89de5-728">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics`-Beispiel aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-728">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="89de5-729">Unterstützung von `Set-AzureRmWebApp -PhpVersion` als gültige PHP-Version eingestellt</span><span class="sxs-lookup"><span data-stu-id="89de5-729">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="89de5-730">6.4.0 – Juli 2018</span><span class="sxs-lookup"><span data-stu-id="89de5-730">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="89de5-731">Allgemein</span><span class="sxs-lookup"><span data-stu-id="89de5-731">General</span></span>
* <span data-ttu-id="89de5-732">Formatierung von OutputType in Hilfedateien für die meisten Module korrigiert</span><span class="sxs-lookup"><span data-stu-id="89de5-732">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="89de5-733">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="89de5-733">AzureRM.Profile</span></span>
* <span data-ttu-id="89de5-734">Attribut „Ps1Xml“ wurde den Standardausgabetypen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-734">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="89de5-735">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="89de5-735">AzureRM.Compute</span></span>
* <span data-ttu-id="89de5-736">IP-Tag-Funktion für VMSS</span><span class="sxs-lookup"><span data-stu-id="89de5-736">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="89de5-737">Cmdlet „New-AzureRmVmssIpTagConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-737">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="89de5-738">IpTag-Parameter zu „New-AzureRmVmssIpConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-738">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="89de5-739">Funktion für automatisches Betriebssystemrollback für VMSS</span><span class="sxs-lookup"><span data-stu-id="89de5-739">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="89de5-740">DisableAutoRollback-Parameter zu „New-AzureRmVmssConfig“ und „Update-AzureRmVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-740">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="89de5-741">Funktion für Upgradeverlauf des Betriebssystems für VMSS</span><span class="sxs-lookup"><span data-stu-id="89de5-741">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="89de5-742">Switch-Parameter „OSUpgradeHistory“ zu „Get-AzureRmVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-742">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="89de5-743">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="89de5-743">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="89de5-744">Unterstützung für Katalog-ACLs über die folgenden Befehle hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="89de5-744">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="89de5-745">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="89de5-745">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="89de5-746">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="89de5-746">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="89de5-747">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="89de5-747">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="89de5-748">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="89de5-748">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="89de5-749">Abbruchunterstützung und Nachverfolgung des Fortschritts für „Set-AzureRmDataLakeStoreItemAclEntry“, „Remove-AzureRmDataLakeStoreItemAclEntry“, „Set-AzureRmDataLakeStoreItemAcl“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-749">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="89de5-750">Abbruchunterstützung „Export-AzureRmDataLakeStoreChildItemProperties“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-750">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="89de5-751">Leerung von Debugmeldungen für Cmdlets korrigiert, die rekursive Vorgänge durchführt</span><span class="sxs-lookup"><span data-stu-id="89de5-751">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="89de5-752">Speicherort des Test von DataLake-Cmdlets korrigiert</span><span class="sxs-lookup"><span data-stu-id="89de5-752">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="89de5-753">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="89de5-753">AzureRM.EventHub</span></span>
* <span data-ttu-id="89de5-754">Optionaler Parameter „MaxCount“ zu Listenvorgangs-Cmdlets „Get-AzureRmEventHub“ und „Get-AzureRmEventHubConsumerGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-754">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="89de5-755">Problem in Cmdlet „New-AzureRmEventHub“ behoben, aufgrund dessen beim Erstellen einer neuen EventHub-Instanz mindestens ein Parameter benötigt wurde.</span><span class="sxs-lookup"><span data-stu-id="89de5-755">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="89de5-756">Standardparametersatz wurde bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="89de5-756">Provided Default Parameter set.</span></span>
* <span data-ttu-id="89de5-757">Optionaler Parameter“ -KeyValue“ zu Cmdlet „New-AzureRmEventHubKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="89de5-757">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="89de5-758">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="89de5-758">AzureRM.KeyVault</span></span>
* <span data-ttu-id="89de5-759">Problem behoben, aufgrund dessen von „Get-AzureRmKeyVault -Tag“ alle Ressourcen zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="89de5-759">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="89de5-760">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="89de5-760">AzureRM.Network</span></span>
* <span data-ttu-id="89de5-761">Neue SKUs für zonenredundante VirtualNetworkGateways-Instanzen verfügbar gemacht</span><span class="sxs-lookup"><span data-stu-id="89de5-761">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="89de5-762">Neue Befehle für Funktion hinzugefügt: ExpressRoute-Partner-APIs über ARM</span><span class="sxs-lookup"><span data-stu-id="89de5-762">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="89de5-763">Get-AzureRmExpressRouteCrossConnection hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-763">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="89de5-764">Set-AzureRmExpressRouteCrossConnection hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-764">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="89de5-765">Add-AzureRmExpressRouteCrossConnectionPeering hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-765">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="89de5-766">Get-AzureRmExpressRouteCrossConnectionPeering hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-766">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="89de5-767">Remove-AzureRmExpressRouteCrossConnectionPeering hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-767">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="89de5-768">Get-AzureRMExpressRouteCrossConnectionArpTable hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-768">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="89de5-769">Get-AzureRMExpressRouteCrossConnectionRouteTable hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-769">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="89de5-770">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-770">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="89de5-771">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="89de5-771">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="89de5-772">Cmdlet „Get-AzureRmRecoveryServicesBackupStatus“ wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="89de5-772">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="89de5-773">Dieses Cmdlet überprüft anhand der ID eines virtuellen Computers, ob dieser durch einen Tresor im Abonnement geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="89de5-773">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="89de5-774">Wenn ein solcher Tresor vorhanden ist, gibt das Cmdlet die Tresordetails aus.</span><span class="sxs-lookup"><span data-stu-id="89de5-774">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="89de5-775">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="89de5-775">AzureRM.Resources</span></span>
* <span data-ttu-id="89de5-776">Cmdlets vom Typ „Get-AzureRmPolicyAssignment“ aktualisieren:</span><span class="sxs-lookup"><span data-stu-id="89de5-776">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="89de5-777">Unterstützung für das Auflisten von „-Scope“-Werten auf Verwaltungsgruppenebene hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-777">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="89de5-778">Unterstützung für das Abrufen einzelner Arbeitsaufträge mit „-Scope“-Werten auf Verwaltungsgruppenebene hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-778">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="89de5-779">Switches „-Effective“ und „-All“ zu Steuerparameter hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-779">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="89de5-780">Cmdlets vom Typ Get/New/Remove/Set-AzureRmPolicyDefinition aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-780">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="89de5-781">Parameter „-ManagementGroupName“ hinzugefügt, um Vorgänge auf eine bestimmte Verwaltungsgruppe anzuwenden</span><span class="sxs-lookup"><span data-stu-id="89de5-781">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="89de5-782">Parameter „-SubscriptionId“ hinzugefügt, um Vorgänge auf ein bestimmtes Abonnement anzuwenden</span><span class="sxs-lookup"><span data-stu-id="89de5-782">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="89de5-783">Cmdlets vom Typ Get/New/Remove/Set-AzureRmPolicySetDefinition aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-783">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="89de5-784">Parameter „-ManagementGroupName“ hinzugefügt, um Vorgänge auf eine bestimmte Verwaltungsgruppe anzuwenden</span><span class="sxs-lookup"><span data-stu-id="89de5-784">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="89de5-785">Parameter „-SubscriptionId“ hinzugefügt, um Vorgänge auf ein bestimmtes Abonnement anzuwenden</span><span class="sxs-lookup"><span data-stu-id="89de5-785">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="89de5-786">Unterstützung für KeyVault-Geheimnisverweis in Parametern hinzugefügt, wenn „TemplateParameterObject“ in „New-AzureRmResourceGroupDeployment“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="89de5-786">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="89de5-787">Problem behoben, aufgrund dessen, der Parameter „-EndDate“ für „New-AzureRmADAppCredential“ ignoriert wurde</span><span class="sxs-lookup"><span data-stu-id="89de5-787">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="89de5-788">Problem behoben, aufgrund dessen „Add-AzureRmADGroupMember“ eine falsche URL für Anforderungen verwendete</span><span class="sxs-lookup"><span data-stu-id="89de5-788">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="89de5-789">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="89de5-789">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="89de5-790">Optionaler Parameter“ -KeyValue“ zu Cmdlet „New-AzureRmServiceBusKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="89de5-790">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="89de5-791">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="89de5-791">AzureRM.Sql</span></span>
* <span data-ttu-id="89de5-792">Benutzerdefinierte Wiederherstellungspunkte für SQLDW in Hilfe zu „New-AzureRmSqlDatabaseRestorePoint“ erläutert</span><span class="sxs-lookup"><span data-stu-id="89de5-792">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="89de5-793">Dokumentation von Parameter „-ComputeGeneration“ in mehreren Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-793">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="89de5-794">6.3.0: Juni 2018</span><span class="sxs-lookup"><span data-stu-id="89de5-794">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="89de5-795">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="89de5-795">AzureRM.Profile</span></span>
* <span data-ttu-id="89de5-796">Aktualisierte Fehlermeldungen für „Enable-AzureRmContextAutoSave“</span><span class="sxs-lookup"><span data-stu-id="89de5-796">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="89de5-797">Erstellen eines Kontexts für jedes Abonnement beim Ausführen von „Connect-AzureRmAccount“ ohne vorherigen Kontext</span><span class="sxs-lookup"><span data-stu-id="89de5-797">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="89de5-798">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="89de5-798">Azure.Storage</span></span>
* <span data-ttu-id="89de5-799">Zusätzliche Informationen zum Parameter „-Permissions“ in Hilfedateien</span><span class="sxs-lookup"><span data-stu-id="89de5-799">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="89de5-800">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="89de5-800">AzureRM.Compute</span></span>
* <span data-ttu-id="89de5-801">„Get-AzureRmVmDiskEncryptionStatus“ behebt ein Problem, das bei virtuellen Computern ohne Datenträger festgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="89de5-801">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="89de5-802">Version der Computeclientbibliothek aktualisiert, um folgende Cmdlets zu korrigieren:</span><span class="sxs-lookup"><span data-stu-id="89de5-802">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="89de5-803">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="89de5-803">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="89de5-804">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="89de5-804">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="89de5-805">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="89de5-805">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="89de5-806">Die folgenden Cmdlets wurden korrigiert, um die Vorgangs-ID und den Vorgangsstatus korrekt anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="89de5-806">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="89de5-807">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="89de5-807">Start-AzureRmVM</span></span>
    - <span data-ttu-id="89de5-808">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="89de5-808">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="89de5-809">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="89de5-809">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="89de5-810">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="89de5-810">Set-AzureRmVM</span></span>
    - <span data-ttu-id="89de5-811">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="89de5-811">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="89de5-812">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="89de5-812">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="89de5-813">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="89de5-813">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="89de5-814">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="89de5-814">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="89de5-815">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="89de5-815">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="89de5-816">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="89de5-816">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="89de5-817">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="89de5-817">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="89de5-818">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="89de5-818">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="89de5-819">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="89de5-819">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="89de5-820">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="89de5-820">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="89de5-821">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="89de5-821">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="89de5-822">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="89de5-822">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="89de5-823">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="89de5-823">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="89de5-824">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="89de5-824">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="89de5-825">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="89de5-825">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="89de5-826">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="89de5-826">AzureRM.EventGrid</span></span>
* <span data-ttu-id="89de5-827">ValidateNotNullOrEmpty-Überprüfungskonditionen für „SubjectBeginsWith“/„SubjectEndsWith“ im Cmdlet „Update-AzureRmEventGridSubscription“ wurden entfernt, um bei Bedarf die Änderung dieser Parameter in eine leere Zeichenfolge zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="89de5-827">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="89de5-828">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="89de5-828">AzureRM.KeyVault</span></span>
* <span data-ttu-id="89de5-829">Ein Problem wurde behoben, aufgrund dessen bei Ausführung von „Get-AzureRmKeyVault -Tag“ keine Tags zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="89de5-829">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="89de5-830">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="89de5-830">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="89de5-831">Offizielle Veröffentlichung von Policy Insights-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="89de5-831">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="89de5-832">Verwendung der API-Version 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="89de5-832">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="89de5-833">„PolicyDefinitionReferenceId“ zu den Ergebnissen von „Get-AzureRmPolicyStateSummary“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-833">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="89de5-834">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="89de5-834">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="89de5-835">Parameter „-Vault“ zu den RecoveryServices.Backup-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="89de5-835">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="89de5-836">Bei der Übergabe wird dadurch das Cmdlet „Set-AzureRmRecoveryServicesContext“ außer Kraft gesetzt.</span><span class="sxs-lookup"><span data-stu-id="89de5-836">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="89de5-837">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="89de5-837">AzureRM.Sql</span></span>
* <span data-ttu-id="89de5-838">Aktualisiertes Beispiel in der Hilfedatei für „Get-AzureRmSqlDatabaseExpanded“</span><span class="sxs-lookup"><span data-stu-id="89de5-838">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="89de5-839">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="89de5-839">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="89de5-840">Hilfedatei für „Add-AzureRmTrafficManagerEndpointConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="89de5-840">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="89de5-841">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="89de5-841">AzureRM.Websites</span></span>
* <span data-ttu-id="89de5-842">„Set-AzureRmWebApp“ wurde aktualisiert, damit „AppSettings“ bei der Verwendung von „-AssignIdentity“ nicht außer Kraft gesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="89de5-842">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="89de5-843">„New-AzureRmWebAppSlot“ wurde aktualisiert, um „AppServicePlan“ als optionalen Parameter anzuerkennen</span><span class="sxs-lookup"><span data-stu-id="89de5-843">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="89de5-844">6.2.1: Juni 2018</span><span class="sxs-lookup"><span data-stu-id="89de5-844">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="89de5-845">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="89de5-845">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="89de5-846">PSWorkspace-Modell aktualisiert, damit das Netzwerk „type“ als Parameter verwenden kann</span><span class="sxs-lookup"><span data-stu-id="89de5-846">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="89de5-847">6.2.0: Juni 2018</span><span class="sxs-lookup"><span data-stu-id="89de5-847">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="89de5-848">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="89de5-848">AzureRM.Profile</span></span>
* <span data-ttu-id="89de5-849">Beheben des Problems, aufgrund dessen Version 10.0.3 von Newtonsoft.Json beim Modulimport nicht geladen wurde</span><span class="sxs-lookup"><span data-stu-id="89de5-849">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="89de5-850">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="89de5-850">AzureRM.Compute</span></span>
* <span data-ttu-id="89de5-851">Feature zum Aktualisieren von virtuellen VMSS-Computern</span><span class="sxs-lookup"><span data-stu-id="89de5-851">VMSS VM Update feature</span></span>
    - <span data-ttu-id="89de5-852">Cmdlets „Update-AzureRmVmssVM“ und „New-AzureRmVMDataDisk“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-852">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="89de5-853">Fügen Sie den Parameter „VirtualMachineScaleSetVM“ zum Cmdlet „Add-AzureRmVMDataDisk“ hinzu, um das Hinzufügen eines Datenträgers zum virtuellen VMSS-Computer zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="89de5-853">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="89de5-854">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="89de5-854">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="89de5-855">Aktualisierung der ADF .Net SDK-Version auf 0.8.0-preview mit den folgenden Änderungen:</span><span class="sxs-lookup"><span data-stu-id="89de5-855">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="89de5-856">Vorgang zum Konfigurieren des Factoryrepositorys hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-856">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="89de5-857">Der verknüpfte QuickBooks-Dienst wurde aktualisiert, um die Eigenschaften „consumerKey“ und „consumerSecret“ verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="89de5-857">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="89de5-858">Aktualisierung verschiedener Modelltypen von „SecretBase“ auf „Object“</span><span class="sxs-lookup"><span data-stu-id="89de5-858">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="89de5-859">Blobereignisauslöser hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-859">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="89de5-860">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="89de5-860">AzureRM.KeyVault</span></span>
* <span data-ttu-id="89de5-861">Aktualisierung der Dokumentation mit Beispielausgabe</span><span class="sxs-lookup"><span data-stu-id="89de5-861">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="89de5-862">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="89de5-862">AzureRM.Network</span></span>
* <span data-ttu-id="89de5-863">Aktivierung der Traffic Analytics-Parameter für Network Watcher-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="89de5-863">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="89de5-864">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="89de5-864">AzureRM.Resources</span></span>
* <span data-ttu-id="89de5-865">Behebung des Problems mit der Eigenschaft „Properties“ von PSResource-Objekten, die von „Get-AzureRmResource“ zurückgegeben wurden</span><span class="sxs-lookup"><span data-stu-id="89de5-865">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="89de5-866">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="89de5-866">AzureRM.Scheduler</span></span>
* <span data-ttu-id="89de5-867">Behebung des Problems, dass beim Aktualisieren von „ServiceBusQueueJob“ keine neuen Authentifizierungswerte festgelegt wurden</span><span class="sxs-lookup"><span data-stu-id="89de5-867">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="89de5-868">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="89de5-868">AzureRM.Sql</span></span>
* <span data-ttu-id="89de5-869">Aktualisierung der folgenden Cmdlets mit dem optionalen LicenseType-Parameter</span><span class="sxs-lookup"><span data-stu-id="89de5-869">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="89de5-870">New-AzureRmSqlDatabase, Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="89de5-870">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="89de5-871">New-AzureRmSqlElasticPool, Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="89de5-871">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="89de5-872">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="89de5-872">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="89de5-873">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="89de5-873">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="89de5-874">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="89de5-874">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="89de5-875">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="89de5-875">AzureRM.Websites</span></span>
* <span data-ttu-id="89de5-876">„New-AzureRMWebApp“ aktualisiert, um allgemeine Algorithmen aus der Strategiebibliothek zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="89de5-876">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="89de5-877">6.1.0 – Mai 2018</span><span class="sxs-lookup"><span data-stu-id="89de5-877">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="89de5-878">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="89de5-878">AzureRM.Profile</span></span>
* <span data-ttu-id="89de5-879">Behebung eines Problems, durch das beim Ausführen von „Clear-AzureRmContext“ ein leerer Kontext mit dem Namen des vorherigen Standardkontexts beibehalten wurde und der Benutzer dadurch keinen neuen Kontext mit dem alten Namen erstellen konnte</span><span class="sxs-lookup"><span data-stu-id="89de5-879">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="89de5-880">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="89de5-880">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="89de5-881">Ermöglichung der Zuordnung von Gateways/Aufhebung der Gatewayzuordnung in AS</span><span class="sxs-lookup"><span data-stu-id="89de5-881">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="89de5-882">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="89de5-882">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="89de5-883">Unterstützung für „ApiVersions“, „ApiReleases“ und „ApiRevisions“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-883">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="89de5-884">Unterstützung für ServiceFabric-Back-End hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-884">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="89de5-885">Unterstützung für Application Insights-Protokollierung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-885">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="89de5-886">Unterstützung für die Erkennung von SKUs vom Typ „Basic“ als gültige SKU des API Management-Diensts hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-886">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="89de5-887">Unterstützung hinzugefügt, damit Zertifikate, die von der privaten Zertifizierungsstelle ausgestellt wurden, als Stamm- oder ZS-Zertifikate installiert werden können</span><span class="sxs-lookup"><span data-stu-id="89de5-887">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="89de5-888">Unterstützung für die Akzeptierung benutzerdefinierter SSL-Zertifikate über KeyVault und mehrere Proxyhostnamen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-888">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="89de5-889">Unterstützung für die verwaltete Dienstidentität hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-889">Added support for MSI identity</span></span>
* <span data-ttu-id="89de5-890">Unterstützung für die Annahme von Richtlinien über URL hinzugefügt; HINWEIS: Folgende Cmdlets werden in einem zukünftigen Release als veraltet gekennzeichnet:</span><span class="sxs-lookup"><span data-stu-id="89de5-890">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="89de5-891">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="89de5-891">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="89de5-892">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="89de5-892">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="89de5-893">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="89de5-893">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="89de5-894">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="89de5-894">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="89de5-895">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="89de5-895">AzureRM.Batch</span></span>
* <span data-ttu-id="89de5-896">Veröffentlichung des neuen Cmdlets „Get-AzureBatchPoolNodeCounts“</span><span class="sxs-lookup"><span data-stu-id="89de5-896">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="89de5-897">Veröffentlichung des neuen Cmdlets „Start-AzureBatchComputeNodeServiceLogUpload“</span><span class="sxs-lookup"><span data-stu-id="89de5-897">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="89de5-898">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="89de5-898">AzureRM.Consumption</span></span>
* <span data-ttu-id="89de5-899">Hinzufügung neuer Parameter („Expand“, „ResourceGroup“, „InstanceName“, „InstanceId“, „Tags“ und „Top“) für das Cmdlet „Get-AzureRmConsumptionUsageDetail“</span><span class="sxs-lookup"><span data-stu-id="89de5-899">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="89de5-900">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="89de5-900">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="89de5-901">Korrektur des Beispiels für „Export AzureRmDataLakeStoreChildItemProperties“</span><span class="sxs-lookup"><span data-stu-id="89de5-901">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="89de5-902">Korrektur der NULL-Parameterausnahme für rekursiven Fall in „Set-AzureRmDataLakeStoreItemAclEntry“</span><span class="sxs-lookup"><span data-stu-id="89de5-902">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="89de5-903">Korrektur der Hilfedateien für „Set-AzureRmDataLakeStoreItemAclEntry“, „Set-AzureRmDataLakeStoreItemAcl“ und „Remove-AzureRmDataLakeStoreItemAclEntry“</span><span class="sxs-lookup"><span data-stu-id="89de5-903">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="89de5-904">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="89de5-904">AzureRM.Network</span></span>
* <span data-ttu-id="89de5-905">Erhöhung der Network SDK-Version von 18.0.0-preview auf 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="89de5-905">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="89de5-906">Cmdlet zum Erstellen der Protokollkonfiguration hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-906">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="89de5-907">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="89de5-907">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="89de5-908">Cmdlet zum Hinzufügen einer neuen Leitungsverbindung zu einer vorhandenen ExpressRoute-Leitung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-908">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="89de5-909">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="89de5-909">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="89de5-910">Cmdlet zum Entfernen einer Leitungsverbindung aus einer vorhandenen ExpressRoute-Leitung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-910">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="89de5-911">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="89de5-911">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="89de5-912">Cmdlet zum Abrufen einer Leitungsverbindung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="89de5-912">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="89de5-913">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="89de5-913">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="89de5-914">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="89de5-914">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="89de5-915">Verwendung der Serverauthentifizierung mit generierten Zertifikaten korrigiert (Problemnr. 5998)</span><span class="sxs-lookup"><span data-stu-id="89de5-915">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="89de5-916">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="89de5-916">AzureRM.Sql</span></span>
* <span data-ttu-id="89de5-917">Überwachungscmdlets korrigiert, um das Entfernen von „AuditActions“ oder „AuditActionGroups“ zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="89de5-917">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="89de5-918">Problem mit „Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy“ behoben, das beim Festlegen einer neuen flexiblen Aufbewahrungsrichtlinie zu folgendem Fehler führte: „Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="89de5-918">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="89de5-919">Please submit request with the new flexible retention policy“ (Das Konfigurieren einer langfristigen Aufbewahrungsrichtlinie mit Azure Recovery Service-Tresor und -Richtlinie wird nicht mehr unterstützt. Übermitteln Sie eine Anforderung mit der neuen flexiblen Aufbewahrungsrichtlinie.)</span><span class="sxs-lookup"><span data-stu-id="89de5-919">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="89de5-920">Aktualisierung aller Cmdlets für Azure SQL-Datenbank, für die Erstellung von Pools für elastische Datenbanken und für die Aktualisierung, sodass sie die neue Datenbank-API verwenden. Diese unterstützt die Sku-Eigenschaft für skalierungs- und tarifbezogene Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="89de5-920">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="89de5-921">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="89de5-921">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="89de5-922">New-AzureRmSqlDatabase, Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="89de5-922">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="89de5-923">New-AzureRmSqlElasticPool, Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="89de5-923">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="89de5-924">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="89de5-924">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="89de5-925">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="89de5-925">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="89de5-926">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="89de5-926">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="89de5-927">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="89de5-927">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="89de5-928">Aktualisierung der Parameter für „Get-AzureRmTrafficManagerProfile“, sodass bei Verwendung des Parameters „-Name“ der Parameter „-ResourceGroupName“ erforderlich ist</span><span class="sxs-lookup"><span data-stu-id="89de5-928">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>