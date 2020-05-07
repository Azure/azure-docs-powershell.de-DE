---
title: Versionshinweise zu Azure PowerShell
description: Hier erfahren Sie mehr über die aktuellen Updates für die Azure PowerShell-Module.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: 98a24c805fbf43dd899119d43301b4261c1f60dc
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2020
ms.locfileid: "75035760"
---
## <a name="280---october-2019"></a><span data-ttu-id="e9783-103">2.8.0: Oktober 2019</span><span class="sxs-lookup"><span data-stu-id="e9783-103">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="e9783-104">Allgemein</span><span class="sxs-lookup"><span data-stu-id="e9783-104">General</span></span>
* <span data-ttu-id="e9783-105">Az.HealthcareApis-Release 1.0.0</span><span class="sxs-lookup"><span data-stu-id="e9783-105">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e9783-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e9783-106">Az.Accounts</span></span>
* <span data-ttu-id="e9783-107">Telemetriedaten und URL-Umschreibung für generierte Module aktualisiert, Windows-Komponententests korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-107">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e9783-108">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e9783-108">Az.ApiManagement</span></span>
* <span data-ttu-id="e9783-109">**Set-AzApiManagementApi**: Unterstützung für die Aktualisierung der API in „ApiVersionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-109">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="e9783-110">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="e9783-110">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e9783-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e9783-111">Az.Automation</span></span>
* <span data-ttu-id="e9783-112">Cmdlet „New-AzureAutomationSoftwareUpdateConfiguration“ für den Parameter für die Linux-Neustarteinstellung korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-112">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="e9783-113">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e9783-113">Az.Batch</span></span>
* <span data-ttu-id="e9783-114">**Get-AzBatchNodeAgentSku** ist veraltet und wird in Version 2.0.0 durch **Get-AzBatchSupportImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="e9783-114">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9783-115">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9783-115">Az.Compute</span></span>
* <span data-ttu-id="e9783-116">Parameter „Priority“, „EvictionPolicy“ und „MaxPrice“ zu den Cmdlets „“New-AzVM“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-116">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="e9783-117">Warnmeldung und Hilfedokument für die Cmdlets „Add-AzVMAdditionalUnattendContent“ und „Add-AzVMSshPublicKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-117">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="e9783-118">Ausnahme „-skipVmBackup“ Linux-VMs mit verwalteten Datenträgern für „Set-AzVMDiskEncryptionExtension“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-118">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="e9783-119">Fehler beim Aktualisieren von Verschlüsselungseinstellungen in „Set-AzVMDiskEncryptionExtension“ korrigiert (zweistufiges Szenario)</span><span class="sxs-lookup"><span data-stu-id="e9783-119">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e9783-120">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e9783-120">Az.DataFactory</span></span>
* <span data-ttu-id="e9783-121">CRUD-Befehle für ADF V2-Datenfluss hinzugefügt: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow und Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="e9783-121">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="e9783-122">Aktionsbefehle für Debugsitzung für ADF V2-Datenfluss hinzugefügt: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand und Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="e9783-122">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="e9783-123">Version des ADF .NET SDK auf 4.2.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-123">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e9783-124">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e9783-124">Az.DataLakeStore</span></span>
* <span data-ttu-id="e9783-125">Kontoüberprüfung korrigiert, sodass Konten mit „-“ ohne Domäne übermittelt werden können</span><span class="sxs-lookup"><span data-stu-id="e9783-125">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="e9783-126">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="e9783-126">Az.HealthcareApis</span></span>
* <span data-ttu-id="e9783-127">PowerShell-Version auf 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-127">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="e9783-128">SDK-Version auf 1.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-128">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="e9783-129">Aktualisierung in Tests, um auf neue SDK-Version zu verweisen</span><span class="sxs-lookup"><span data-stu-id="e9783-129">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="e9783-130">Ausgabestruktur von geschachtelt in vereinfacht geändert</span><span class="sxs-lookup"><span data-stu-id="e9783-130">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e9783-131">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e9783-131">Az.IotHub</span></span>
* <span data-ttu-id="e9783-132">Neue Routingquelle hinzugefügt: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="e9783-132">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="e9783-133">Kleinere Fehlerbehebung: „Get-AzIothub“ gibt „subscriptionId“ nicht zurück.</span><span class="sxs-lookup"><span data-stu-id="e9783-133">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="e9783-134">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e9783-134">Az.Monitor</span></span>
* <span data-ttu-id="e9783-135">Neue Aktionsgruppenempfänger für „New-AzActionGroupReceiver“ hinzugefügt:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="e9783-135">New action group receivers added for New-AzActionGroupReceiver:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="e9783-136">Verwendung des allgemeinen Warnungsschemas für Empfänger aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e9783-136">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="e9783-137">Dies gilt nicht für SMS, Azure App-Pushbenachrichtigungen, ITSM und Sprachempfänger.</span><span class="sxs-lookup"><span data-stu-id="e9783-137">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="e9783-138">Webhooks unterstützen nun die Azure Active Directory-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="e9783-138">Webhooks now supports Azure active directory authentication.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e9783-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9783-139">Az.Network</span></span>
* <span data-ttu-id="e9783-140">Neues Cmdlet „Get-AzAvailableServiceAlias“ hinzugefügt, das zum Abrufen der Aliase aufgerufen werden kann, die für Dienstendpunktrichtlinien verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="e9783-140">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="e9783-141">Unterstützung für das Hinzufügen von Verbindungen von Datenverkehrsselektoren zu Virtual Network-Gatewayverbindungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-141">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="e9783-142">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="e9783-142">New cmdlets added:</span></span>
        - <span data-ttu-id="e9783-143">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="e9783-143">New-AzIpsecTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="e9783-144">Cmdlets mit optionalem Parameter „-TrafficSelectorPolicies“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-144">Cmdlets updated with optional parameter -TrafficSelectorPolicies</span></span>
        - <span data-ttu-id="e9783-145">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e9783-145">New-AzVirtualNetworkGatewayConnection</span></span>
        - <span data-ttu-id="e9783-146">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e9783-146">Set-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="e9783-147">Unterstützung für ESP- und AH-Protokolle in Konfigurationen von Netzwerksicherheitsregeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-147">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="e9783-148">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="e9783-148">Updated cmdlets:</span></span>
        - <span data-ttu-id="e9783-149">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e9783-149">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e9783-150">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e9783-150">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e9783-151">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e9783-151">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="e9783-152">Verbesserte Behandlung von Ausnahmen in Cortex-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="e9783-152">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="e9783-153">Neue Generationen und SKUs für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="e9783-153">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="e9783-154">Einführung neuer Generationen für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="e9783-154">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="e9783-155">Einführung neuer SKUs mit höherem Durchsatz für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="e9783-155">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e9783-156">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e9783-156">Az.RedisCache</span></span>
* <span data-ttu-id="e9783-157">Referenzdokumentation zu „Set-AzRedisCache“ aktualisiert, um fehlende Werte für den Parameter „-Size“ aufzunehmen</span><span class="sxs-lookup"><span data-stu-id="e9783-157">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="e9783-158">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9783-158">Az.Sql</span></span>
* <span data-ttu-id="e9783-159">Unterstützung für das Festlegen des Active Directory-Administrators für verwaltete Instanz hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-159">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e9783-160">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e9783-160">Az.Storage</span></span>
* <span data-ttu-id="e9783-161">Storage-Clientbibliothek auf 11.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-161">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="e9783-162">Auflisten von Containern mit der API der Verwaltungsebene, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="e9783-162">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="e9783-163">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e9783-163">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="e9783-164">Auflisten von Storage-Konten aus Abonnements, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="e9783-164">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="e9783-165">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e9783-165">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="e9783-166">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="e9783-166">Az.StorageSync</span></span>
* <span data-ttu-id="e9783-167">Problem 9810 in „Reset-AzStorageSyncServerCertificate“ behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-167">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e9783-168">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e9783-168">Az.Websites</span></span>
* <span data-ttu-id="e9783-169">Fehler beim Aktualisieren von ASP einer App mit „Set-AzWebApp“</span><span class="sxs-lookup"><span data-stu-id="e9783-169">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="e9783-170">2.7.0: September 2019</span><span class="sxs-lookup"><span data-stu-id="e9783-170">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="e9783-171">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e9783-171">Az.ApiManagement</span></span>
* <span data-ttu-id="e9783-172">Beschreibung des Parameters „-Format“ in der Referenzdokumentation für „Set-AzApiManagementPolicy“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-172">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="e9783-173">Verweise des veralteten Cmdlets „Update-AzApiManagementDeployment“ aus Referenzdokumentation entfernt.</span><span class="sxs-lookup"><span data-stu-id="e9783-173">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="e9783-174">Verwenden Sie stattdessen „Set-AzApiManagement“.</span><span class="sxs-lookup"><span data-stu-id="e9783-174">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e9783-175">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e9783-175">Az.Automation</span></span>
* <span data-ttu-id="e9783-176">Tippfehler im Beispiel in der Referenzdokumentation für „Register-AzAutomationDscNode“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-176">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="e9783-177">Erläuterung zur Betriebssystemeinschränkung zu „Register-AzAutomationDSCNode“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-177">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="e9783-178">Nullverweisausnahme des Cmdlets „Start-AzAutomationRunbook“ für die Option „-Wait“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="e9783-178">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9783-179">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9783-179">Az.Compute</span></span>
* <span data-ttu-id="e9783-180">Parameter „UploadSizeInBytes“ zu „New-AzDiskConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-180">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="e9783-181">Inkrementeller Parameter zu „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-181">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="e9783-182">Feature für VM mit niedriger Priorität hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="e9783-182">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="e9783-183">Parameter „MaxPrice“, „EvictionPolicy“ und „Priority“ zu New-AzVMConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-183">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="e9783-184">Parameter „MaxPrice“ zu den Cmdlets „New-AzVmssConfig“, „Update-AzVM“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-184">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="e9783-185">Fehlerbehebung für VM-Verweis für das Cmdlet „Get-AzAvailabilitySet“, wenn alle Verfügbarkeitsgruppen im Abonnement aufgelistet werden</span><span class="sxs-lookup"><span data-stu-id="e9783-185">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="e9783-186">Nullausnahme für „Get-AzRemoteDesktopFile“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-186">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="e9783-187">VHD-Suchmethode für Position relativ zum Ende korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-187">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="e9783-188">Problem mit UltraSSD für „New-AzVM“ und „Update-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-188">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e9783-189">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e9783-189">Az.DataFactory</span></span>
* <span data-ttu-id="e9783-190">Drei neue Befehle für ADF V2 hinzugefügt: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription und Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="e9783-190">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="e9783-191">Version des ADF .NET SDK auf 4.1.3 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-191">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e9783-192">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e9783-192">Az.HDInsight</span></span>
* <span data-ttu-id="e9783-193">Hinweis auf Breaking Changes hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-193">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e9783-194">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e9783-194">Az.IotHub</span></span>
* <span data-ttu-id="e9783-195">Unterstützung zum Aufrufen eines Failovers für einen IoT-Hub zur geografisch gekoppelten Notfallwiederherstellungsregion hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-195">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="e9783-196">Unterstützung zum Verwalten der Nachrichtenanreicherung für einen IoT-Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-196">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="e9783-197">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="e9783-197">New cmdlets are:</span></span>
    - <span data-ttu-id="e9783-198">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e9783-198">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="e9783-199">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e9783-199">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="e9783-200">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e9783-200">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="e9783-201">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e9783-201">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e9783-202">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e9783-202">Az.Monitor</span></span>
* <span data-ttu-id="e9783-203">Verweis auf das aktuelle Monitor SDK, d. h. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="e9783-203">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="e9783-204">Geringfügige Änderungen an den Metrik-Cmdlets vorgenommen, d. h. die Einheitenenumeration unterstützt verschiedene neue Werte.</span><span class="sxs-lookup"><span data-stu-id="e9783-204">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="e9783-205">Dabei handelt es sich um schreibgeschützte Cmdlets, sodass keine Änderungen an der Eingabe der Cmdlets erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="e9783-205">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="e9783-206">Die API-Version der **ActionGroups**-Anforderungen lautet jetzt **2019-06-01** (zuvor **2018-03-01**).</span><span class="sxs-lookup"><span data-stu-id="e9783-206">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="e9783-207">Die Szenariotests wurden aktualisiert, um diese Änderung zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="e9783-207">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="e9783-208">Die Konstruktoren für die Klassen **EmailReceiver** und **WebhookReceiver** haben ein neues obligatorisches Argument hinzugefügt, d. h. einen booleschen Wert namens **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="e9783-208">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="e9783-209">Derzeit ist der Wert auf **false** festgelegt, damit sich dieser Breaking Change nicht auf die Cmdlets auswirkt.</span><span class="sxs-lookup"><span data-stu-id="e9783-209">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="e9783-210">**HINWEIS:** Dies ist eine vorübergehende Änderung, die vom Team für Warnungen validiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="e9783-210">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="e9783-211">Die Reihenfolge der Argumente für den Konstruktor der Klasse **Source** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="e9783-211">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="e9783-212">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="e9783-212">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="e9783-213">Die Reihenfolge der Argumente für den Konstruktor der Klasse **AlertingAction** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="e9783-213">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="e9783-214">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="e9783-214">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="e9783-215">Unterstützung von Kriterien für dynamische Schwellwerte für Metrikwarnung v2</span><span class="sxs-lookup"><span data-stu-id="e9783-215">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="e9783-216">New-AzMetricAlertRuleV2Criteria: Erstellt nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="e9783-216">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="e9783-217">Add-AzMetricAlertRuleV2: Akzeptiert nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="e9783-217">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="e9783-218">Verbesserungen an den Cmdlets für geplante Abfrageregeln (Scheduled Query Rule, SQR)</span><span class="sxs-lookup"><span data-stu-id="e9783-218">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="e9783-219">Cmdlets akzeptieren den Parameter „Location“ in zwei Formaten: entweder den Standort (z. B. „eastus“) oder den Anzeigenamen des Standorts (z. B. „USA, Osten“)</span><span class="sxs-lookup"><span data-stu-id="e9783-219">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="e9783-220">Parameter „Enabled“ in Hilfedateien ordnungsgemäß dargestellt</span><span class="sxs-lookup"><span data-stu-id="e9783-220">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="e9783-221">Beispiele für optionalen Parameter „ActionGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-221">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="e9783-222">Hilfedateien insgesamt verbessert</span><span class="sxs-lookup"><span data-stu-id="e9783-222">Overall improved help files</span></span>
* <span data-ttu-id="e9783-223">Fehler beim Bestimmen des Bereichstyps für „Set-AzActionRule“ behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-223">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e9783-224">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9783-224">Az.Network</span></span>
* <span data-ttu-id="e9783-225">Fehlerhaftes Beispiel in der Referenzdokumentation zu „New-AzApplicationGateway“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-225">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="e9783-226">Hinweis in der Referenzdokumentation zu „Get-AzNetworkWatcherPacketCapture“ zum Abrufen aller Eigenschaften für eine Paketerfassung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-226">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="e9783-227">Beispiel in der Referenzdokumentation zu „Test-AzNetworkWatcherIPFlow“ korrigiert, um die Netzwerkadapter ordnungsgemäß aufzulisten</span><span class="sxs-lookup"><span data-stu-id="e9783-227">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="e9783-228">Cloudausnahmeanalyse verbessert, um ggf. zusätzliche Details anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="e9783-228">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="e9783-229">Cloudausnahmeanalyse verbessert, um zusätzlichen Typ der SDK-Ausnahme zu verarbeiten</span><span class="sxs-lookup"><span data-stu-id="e9783-229">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="e9783-230">Falsche Zuordnung der Sicherheitsregelmodelle korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-230">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="e9783-231">Eigenschaften zur Netzwerkschnittstelle für das Feature für die private IP-Adresse hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-231">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="e9783-232">Eigenschaft „PrivateEndpoint“ als Typ „PSResourceId“ zu „PSNetworkInterface“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-232">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="e9783-233">Eigenschaft „PrivateLinkConnectionProperties“ als Typ „PSIpConfigurationConnectivityInformation“ zu „PSNetworkInterfaceIPConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-233">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="e9783-234">Neue Modellklasse „PSIpConfigurationConnectivityInformation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-234">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="e9783-235">Neues ApplicationRuleProtocolType-Element „mssql“ für Azure Firewall-Ressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-235">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="e9783-236">Unterstützung von Mehrfachverbindungen in Virtual WAN</span><span class="sxs-lookup"><span data-stu-id="e9783-236">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="e9783-237">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="e9783-237">New cmdlets</span></span>
        - <span data-ttu-id="e9783-238">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="e9783-238">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="e9783-239">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="e9783-239">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="e9783-240">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e9783-240">Updated cmdlet:</span></span>
        - <span data-ttu-id="e9783-241">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="e9783-241">New-VpnSite</span></span>
        - <span data-ttu-id="e9783-242">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="e9783-242">Update-VpnSite</span></span>
        - <span data-ttu-id="e9783-243">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="e9783-243">New-VpnConnection</span></span>
        - <span data-ttu-id="e9783-244">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="e9783-244">Update-VpnConnection</span></span>
* <span data-ttu-id="e9783-245">Dokumente für einige PowerShell-Beispiele korrigiert, sodass Az-Cmdlets anstelle von AzureRM-Cmdlets verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e9783-245">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e9783-246">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e9783-246">Az.RecoveryServices</span></span>
* <span data-ttu-id="e9783-247">AzureVMpolicy-Objekt mit ProtectedItemsCount-Attribut aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-247">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="e9783-248">Tests für VM-Richtlinie und Wiederherstellung des ursprünglichen Speicherkontos hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-248">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="e9783-249">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9783-249">Az.Resources</span></span>
* <span data-ttu-id="e9783-250">Fehler behoben, aufgrund dessen „New-AzRoleAssignment“ nicht ohne den Parameter „Scope“ aufgerufen werden konnte</span><span class="sxs-lookup"><span data-stu-id="e9783-250">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e9783-251">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e9783-251">Az.ServiceFabric</span></span>
* <span data-ttu-id="e9783-252">Tippfehler im Beispiel für die Referenzdokumentation „Update-AzServiceFabricReliability“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-252">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="e9783-253">Neue Cmdlets zum Verwalten von Anwendung und Diensten hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="e9783-253">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="e9783-254">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e9783-254">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="e9783-255">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="e9783-255">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="e9783-256">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e9783-256">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="e9783-257">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="e9783-257">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="e9783-258">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e9783-258">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="e9783-259">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e9783-259">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="e9783-260">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="e9783-260">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="e9783-261">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e9783-261">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="e9783-262">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="e9783-262">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="e9783-263">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e9783-263">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="e9783-264">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="e9783-264">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="e9783-265">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e9783-265">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="e9783-266">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="e9783-266">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="e9783-267">Service Fabric SDK auf Version 1.2.0 aktualisiert, die API-Version 2019-03-01 des Service Fabric-Ressourcenanbieters verwendet</span><span class="sxs-lookup"><span data-stu-id="e9783-267">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e9783-268">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e9783-268">Az.SignalR</span></span>
* <span data-ttu-id="e9783-269">Cmdlets „Update“, „Restart“, „CheckNameAvailability“ und „GetUsage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-269">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="e9783-270">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9783-270">Az.Sql</span></span>
* <span data-ttu-id="e9783-271">Beispiel in der Referenzdokumentation für „Get-AzSqlElasticPool“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-271">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="e9783-272">V-Kern-Beispiel zum Erstellen eines Pools für elastische Datenbanken hinzugefügt (New-AzSqlElasticPool)</span><span class="sxs-lookup"><span data-stu-id="e9783-272">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="e9783-273">Überprüfung von „EmailAddresses“ sowie Validierung, dass „EmailAdmins“ nicht auf „false“ festgelegt ist, in „Set-AzSqlServerAdvancedThreatProtectionPolicy“ und „Set-AzSqlDatabaseAdvancedThreatProtectionPolicy“ entfernt, wenn „EmailAddresses“ leer ist</span><span class="sxs-lookup"><span data-stu-id="e9783-273">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="e9783-274">Entfernen der Einstellungen für Server-/Datenbanküberwachung aktiviert, wenn mehrere Diagnoseeinstellungen vorhanden sind, die eine Überwachungskategorie ermöglichen</span><span class="sxs-lookup"><span data-stu-id="e9783-274">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="e9783-275">Überprüfung von E-Mail-Adressen in mehreren Cmdlets für die SQL-Sicherheitsrisikobewertung korrigiert (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting und Update-AzSqlInstanceVulnerabilityAssessmentSetting)</span><span class="sxs-lookup"><span data-stu-id="e9783-275">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e9783-276">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e9783-276">Az.Storage</span></span>
* <span data-ttu-id="e9783-277">Beispiel in der Referenzdokumentation für „Get-AzStorageAccountKey“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-277">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="e9783-278">Beim Upload/Download von Azure-Dateien wird das Beibehalten der SMB-Eigenschaften der Quelldateien (Dateiattribute, Zeitpunkt der Dateierstellung, letzter Schreibzugriff für die Datei) in der Zieldatei unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e9783-278">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="e9783-279">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e9783-279">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="e9783-280">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e9783-280">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="e9783-281">Fehler beim Hochladen von Blockblobs mit Eigenschaften/Metadaten für das für einen Container aktivierte ImmutabilityPolicy-Element behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-281">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="e9783-282">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e9783-282">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="e9783-283">Unterstützung für die Verwaltung von Azure-Dateifreigaben mit der API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="e9783-283">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="e9783-284">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e9783-284">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="e9783-285">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e9783-285">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="e9783-286">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e9783-286">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="e9783-287">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e9783-287">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e9783-288">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e9783-288">Az.Websites</span></span>
* <span data-ttu-id="e9783-289">Problem behoben, aufgrund dessen Web-App-Tags beim Migrieren der App zum neuen ASP gelöscht wurden</span><span class="sxs-lookup"><span data-stu-id="e9783-289">Fixing issue where webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="e9783-290">„Publish-AzureWebapp“ für die Verwendung unter Linux und Windows korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-290">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="e9783-291">Beispiel in Referenzdokumentation „Get-AzWebAppPublishingProfile“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-291">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="e9783-292">2.6.0: August 2019</span><span class="sxs-lookup"><span data-stu-id="e9783-292">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="e9783-293">Allgemein</span><span class="sxs-lookup"><span data-stu-id="e9783-293">General</span></span>
* <span data-ttu-id="e9783-294">Verschiedene Tippfehler in zahlreichen Modulen korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-294">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e9783-295">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e9783-295">Az.Accounts</span></span>
* <span data-ttu-id="e9783-296">Unterstützung der benutzerseitig zugewiesenen MSI in Azure Functions-Authentifizierung (#9479)</span><span class="sxs-lookup"><span data-stu-id="e9783-296">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="e9783-297">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e9783-297">Az.Aks</span></span>
* <span data-ttu-id="e9783-298">Problem mit der Ausgabe für „Get-AzAks“ behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-298">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="e9783-299">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="e9783-299">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e9783-300">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e9783-300">Az.ApiManagement</span></span>
* <span data-ttu-id="e9783-301">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="e9783-301">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="e9783-302">.NET-NuGet-Version aktualisiert, die keine Einschränkungen für „productId“, „apiId“, „groupId“ und „userId“ erzwingt</span><span class="sxs-lookup"><span data-stu-id="e9783-302">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="e9783-303">**Get-AzApiManagementProduct:** Unterstützung für das Abfragen von Produkten mithilfe der API hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-303">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="e9783-304">**New-AzApiManagementApiRevision:** Problem behoben, aufgrund dessen „ApiRevisionDescription“ beim Erstellen einer neuen API-Revision nicht festgelegt wurde https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="e9783-304">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="e9783-305">Tippfehler im Modell „PsApiManagementOAuth2AuthrozationServer“ korrigiert: PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="e9783-305">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e9783-306">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e9783-306">Az.Batch</span></span>
* <span data-ttu-id="e9783-307">Tippfehler in Hilfemeldung und Dokumentation korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="e9783-307">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e9783-308">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e9783-308">Az.Cdn</span></span>
* <span data-ttu-id="e9783-309">Tippfehler im Hilfsprogramm für die CDN-Modulkonvertierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-309">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9783-310">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9783-310">Az.Compute</span></span>
* <span data-ttu-id="e9783-311">VmssId zum Cmdlet „New-AzVMConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-311">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="e9783-312">Parameter „TerminateScheduledEvents“ und „TerminateScheduledEventNotBeforeTimeoutInMinutes“ zu „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-312">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="e9783-313">HyperVGeneration-Eigenschaft zu VM-Imageobjekt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-313">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="e9783-314">Host- und HostGroup-Features hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-314">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="e9783-315">Neue Cmdlets:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="e9783-315">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="e9783-316">Parameter „HostId“ zu „New-AzVMConfig“ und „New-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-316">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="e9783-317">Beispiel in der Dokumentation zu „Invoke-AzVMRunCommand“ zur Verwendung des richtigen Parameternamens aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-317">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="e9783-318">Beschreibung für „-VolumeType“ in der Referenzdokumentation zu „Set-AzVMDiskEncryptionExtension“ und „Set-AzVmssDiskEncryptionExtension“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-318">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e9783-319">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e9783-319">Az.DataFactory</span></span>
* <span data-ttu-id="e9783-320">Tippfehler in der Dokumentation zu „New-AzDataFactoryEncryptValue“ korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="e9783-320">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="e9783-321">Version des ADF .NET SDK auf 4.1.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-321">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="e9783-322">Parameter „DataProxyIntegrationRuntimeName“, „DataProxyStagingLinkedServiceName“ und „DataProxyStagingPath“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um die Einrichtung der selbstgehosteten Integration Runtime als Proxy für die SSIS Integration Runtime zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="e9783-322">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="e9783-323">„PSTriggerRun“ zum Anzeigen der ausgelösten Pipelines, Meldungen und Eigenschaften und „PSActivityRun“ zum Anzeigen des Aktivitätstyps aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-323">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e9783-324">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e9783-324">Az.DataLakeStore</span></span>
* <span data-ttu-id="e9783-325">Hängen von „Get-DataLakeStoreDeletedItem“ aufgrund von Fehlern oder Remoteausnahmen behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-325">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e9783-326">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e9783-326">Az.EventHub</span></span>
* <span data-ttu-id="e9783-327">Behebung des Problems #9658: Tippfehler im Parameter „VirtualNteworkRule“ in „Set-AzEventHubNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="e9783-327">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="e9783-328">Behebung des Problems #9558: „Set-AzEventHubNamespace“ verwendet PATCH anstelle von PUT.</span><span class="sxs-lookup"><span data-stu-id="e9783-328">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="e9783-329">Parameter „EnableKafka“ zum Cmdlet „Set-AzEventHubNamespace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-329">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="e9783-330">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="e9783-330">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="e9783-331">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="e9783-331">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="e9783-332">Tippfehler („Azure“ in Kleinbuchstaben) in der Dokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-332">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e9783-333">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e9783-333">Az.Monitor</span></span>
* <span data-ttu-id="e9783-334">Falscher Parametername in der Hilfedokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-334">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e9783-335">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9783-335">Az.Network</span></span>
* <span data-ttu-id="e9783-336">„New-AzPrivateLinkServiceIpConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-336">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="e9783-337">Parameter „PublicIpAddress“ ausgemustert, da er auf Serverseite nie verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="e9783-337">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="e9783-338">Optionaler Parameter „Primary“ hinzugefügt, der angibt, ob die aktuelle IP-Konfiguration die primäre ist oder nicht</span><span class="sxs-lookup"><span data-stu-id="e9783-338">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="e9783-339">Verbesserte Verarbeitung der Anforderungsfehlerausnahme aus dem SDK: Behebt das Problem, dass vorherige SDK-Ausnahmen nicht richtig behandelt wurden, was dazu führt, dass Schlüsselfehlerdetails nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e9783-339">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="e9783-340">Validierungslogik für Ipv6-IP-Präfix angepasst, damit auf die richtige IPv6-Präfixlänge geprüft wird</span><span class="sxs-lookup"><span data-stu-id="e9783-340">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="e9783-341">„Get-AzVirtualNetworkSubnetConfig“ aktualisiert: Parametersatz zum Abrufen nach Subnetzressourcen-ID hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-341">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="e9783-342">Aktualisierte Beschreibung des Location-Parameters für „AzNetworkServiceTag“</span><span class="sxs-lookup"><span data-stu-id="e9783-342">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e9783-343">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e9783-343">Az.OperationalInsights</span></span>
* <span data-ttu-id="e9783-344">Aktualisierte Dokumentation für „New-AzOperationalInsightsLinuxSyslogDataSource“</span><span class="sxs-lookup"><span data-stu-id="e9783-344">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="e9783-345">Beispiel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-345">Added example</span></span>
    - <span data-ttu-id="e9783-346">Beschreibung für den Parameter „-Name“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-346">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="e9783-347">Beispiel für „New-AzOperationalInsightsWindowsEventDataSource“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-347">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="e9783-348">Beschreibung des Parameters „-Name“ für „New-AzOperationalInsightsWindowsEventDataSource“ geändert</span><span class="sxs-lookup"><span data-stu-id="e9783-348">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e9783-349">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e9783-349">Az.RecoveryServices</span></span>
* <span data-ttu-id="e9783-350">„Get-AzRecoveryServicesBackupJobDetail.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-350">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="e9783-351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9783-351">Az.Resources</span></span>
* <span data-ttu-id="e9783-352">Unterstützung für die neue API-Version 2019-05-10 für Microsoft.Resource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-352">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="e9783-353">Unterstützung für „copy.count = 0“ für Variablen, Ressourcen und Eigenschaften hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-353">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="e9783-354">Ressourcen mit „condition = false“ oder „copy.count = 0“ werden im vollständigen Modus gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e9783-354">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="e9783-355">Beispiel zum Hinzufügen einer Richtlinie auf Abonnementebene zur Hilfedokumentation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-355">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e9783-356">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e9783-356">Az.ServiceBus</span></span>
* <span data-ttu-id="e9783-357">Behebung des Problems #9658: Tippfehler für Parameter „VirtualNetworkRule“ in „Set-AzServiceBusNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="e9783-357">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="e9783-358">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="e9783-358">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="e9783-359">Neuer Befehl „Test-AzServiceBusNameAvailability“ zum Überprüfen der Verfügbarkeit des Namens für Warteschlange und Thema hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-359">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="e9783-360">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e9783-360">Az.ServiceFabric</span></span>
* <span data-ttu-id="e9783-361">Fehler bei Cmdlets zum Hinzufügen des Knotentyps korrigiert:</span><span class="sxs-lookup"><span data-stu-id="e9783-361">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="e9783-362">Fehler „NullReferenceException“, wenn die Ressourcengruppe andere VMSS enthielt, die nicht mit dem Service Fabric-Cluster in Zusammenhang stehen</span><span class="sxs-lookup"><span data-stu-id="e9783-362">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="e9783-363">Problembehebung: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="e9783-363">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="e9783-364">Fehler behoben, aufgrund dessen bei einem Cmdlet ein Fehler auftrat, wenn sich „virtualNetwork“ in einer anderen Ressourcengruppe befand als der Cluster</span><span class="sxs-lookup"><span data-stu-id="e9783-364">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="e9783-365">Problembehebung: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="e9783-365">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="e9783-366">Cmdlet „Add-AzServiceFabricApplicationCertificate“ ausgemustert</span><span class="sxs-lookup"><span data-stu-id="e9783-366">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="e9783-367">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9783-367">Az.Sql</span></span>
* <span data-ttu-id="e9783-368">Dokumentation alter Überwachungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-368">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e9783-369">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e9783-369">Az.Storage</span></span>
* <span data-ttu-id="e9783-370">Hilfe für „Get/Close-AzStorageFileHandle“ aktualisiert (weitere Szenarien zu Cmdlet-Beispielen hinzugefügt und Parameterbeschreibungen aktualisiert)</span><span class="sxs-lookup"><span data-stu-id="e9783-370">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="e9783-371">Unterstützung von „StandardBlobTier“ in Uploadblobs und Kopierblobs</span><span class="sxs-lookup"><span data-stu-id="e9783-371">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="e9783-372">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e9783-372">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="e9783-373">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e9783-373">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="e9783-374">Unterstützung der Aktivierungspriorität im Kopierblob</span><span class="sxs-lookup"><span data-stu-id="e9783-374">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="e9783-375">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e9783-375">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e9783-376">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e9783-376">Az.Websites</span></span>
* <span data-ttu-id="e9783-377">Hinzufügen von Erläuterungen zum Parameter „-AppSettings“ in „Set-AzWebApp“ und „Set-AzWebAppSlot“</span><span class="sxs-lookup"><span data-stu-id="e9783-377">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="e9783-378">2.5.0: Juli 2019</span><span class="sxs-lookup"><span data-stu-id="e9783-378">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e9783-379">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e9783-379">Az.Accounts</span></span>
* <span data-ttu-id="e9783-380">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="e9783-380">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="e9783-381">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="e9783-381">Az.ApplicationInsights</span></span>
* <span data-ttu-id="e9783-382">Tippfehler im Beispiel in der Dokumentation zu „Remove-AzApplicationInsightsApiKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-382">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="e9783-383">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e9783-383">Az.Automation</span></span>
* <span data-ttu-id="e9783-384">Tippfehler in der Ressourcenzeichenfolge korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-384">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="e9783-385">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e9783-385">Az.CognitiveServices</span></span>
* <span data-ttu-id="e9783-386">Unterstützung für NetworkRuleSet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-386">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9783-387">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9783-387">Az.Compute</span></span>
* <span data-ttu-id="e9783-388">Fehlende Eigenschaften (ComputerName, OsName, OsVersion und HyperVGeneration) des Objekts für die VM-Instanzenansicht hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-388">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="e9783-389">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e9783-389">Az.ContainerRegistry</span></span>
* <span data-ttu-id="e9783-390">Tippfehler in „Remove-AzContainerRegistryReplication“ für den Replikationsparameter korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-390">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="e9783-391">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="e9783-391">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e9783-392">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e9783-392">Az.DataFactory</span></span>
* <span data-ttu-id="e9783-393">Version des ADF .NET SDK auf 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-393">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="e9783-394">Tippfehler in der Dokumentation für „Get-AzDataFactoryV2PipelineRun“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-394">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e9783-395">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e9783-395">Az.EventHub</span></span>
* <span data-ttu-id="e9783-396">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="e9783-396">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="e9783-397">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="e9783-397">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e9783-398">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e9783-398">Az.KeyVault</span></span>
* <span data-ttu-id="e9783-399">Unterstützung zum Angeben von KeySize für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-399">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e9783-400">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e9783-400">Az.LogicApp</span></span>
* <span data-ttu-id="e9783-401">Korrektur für „Get-AzIntegrationAccountMap“ zum Auflisten aller Zuordnungstypen</span><span class="sxs-lookup"><span data-stu-id="e9783-401">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="e9783-402">Neuer MapType-Parameter für Filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-402">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="e9783-403">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="e9783-403">Az.ManagedServices</span></span>
* <span data-ttu-id="e9783-404">Unterstützung für API-Version 2019-06-01 (GA) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-404">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e9783-405">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9783-405">Az.Network</span></span>
* <span data-ttu-id="e9783-406">Unterstützung für privaten Endpunkt und privaten Verknüpfungsdienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-406">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="e9783-407">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="e9783-407">New cmdlets</span></span>
        - <span data-ttu-id="e9783-408">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e9783-408">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e9783-409">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e9783-409">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="e9783-410">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e9783-410">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e9783-411">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e9783-411">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e9783-412">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e9783-412">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e9783-413">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e9783-413">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e9783-414">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="e9783-414">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="e9783-415">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e9783-415">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="e9783-416">Folgende Befehle für das Feature aktualisiert: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies für Subnetz in VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e9783-416">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="e9783-417">„New-AzVirtualNetworkSubnetConfig“, „Set-AzVirtualNetworkSubnetConfig“ und „Add-AzVirtualNetworkSubnetConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-417">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="e9783-418">Optionaler Parameter „-PrivateEndpointNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den privaten Endpunkt in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="e9783-418">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="e9783-419">Optionaler Parameter „-PrivateLinkServiceNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den Privat Link-Dienst in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="e9783-419">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="e9783-420">Der Cmdlet-Parameter „ServiceName“ von AzPrivateLinkService wurde aus Gründen der Abwärtskompatibilität in „Name“ mit dem Alias „ServiceName“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="e9783-420">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="e9783-421">ICMP-Protokoll für Konfigurationen von Netzwerksicherheitsregeln aktiviert</span><span class="sxs-lookup"><span data-stu-id="e9783-421">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="e9783-422">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="e9783-422">Updated cmdlets</span></span>
        - <span data-ttu-id="e9783-423">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e9783-423">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e9783-424">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e9783-424">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e9783-425">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e9783-425">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="e9783-426">ConnectionProtocolType (Ikev1/Ikev2) als konfigurierbarer Parameter für „New-AzVirtualNetworkGatewayConnection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-426">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="e9783-427">PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-427">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="e9783-428">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e9783-428">Updated cmdlet:</span></span>
        - <span data-ttu-id="e9783-429">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e9783-429">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="e9783-430">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e9783-430">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="e9783-431">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e9783-431">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="e9783-432">Application Gateway-Befehl „New-AzApplicationGatewayProbeConfig“ zur Unterstützung des benutzerdefinierten Ports im Test aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-432">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="e9783-433">„New-AzApplicationGatewayProbeConfig“ aktualisiert: Optionaler Parameter „Port“ hinzugefügt, der zum Testen des Back-End-Servers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e9783-433">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="e9783-434">Dieser Parameter gilt für Standard_V2 und WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="e9783-434">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e9783-435">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e9783-435">Az.OperationalInsights</span></span>
* <span data-ttu-id="e9783-436">Standardversion für gespeicherte Suchvorgänge auf 1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-436">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="e9783-437">Verarbeitung des regulären NULL-Ausdrucks in benutzerdefinierten Protokollen korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-437">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e9783-438">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e9783-438">Az.RecoveryServices</span></span>
* <span data-ttu-id="e9783-439">„Get-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-439">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="e9783-440">„Get-AzRecoveryServicesBackupContainer.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-440">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="e9783-441">„Get-AzRecoveryServicesVault.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-441">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="e9783-442">„Wait-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-442">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="e9783-443">„Set-AzRecoveryServicesVaultContext.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-443">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="e9783-444">„Get-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-444">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="e9783-445">„Get-AzRecoveryServicesBackupRecoveryPoint.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-445">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="e9783-446">„Restore-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-446">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="e9783-447">Dienstaufruf zum Aufheben der Containerregistrierung für Azure-Dateifreigabe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-447">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="e9783-448">„Set-AzRecoveryServicesAsrAlertSetting.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-448">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="e9783-449">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9783-449">Az.Resources</span></span>
- <span data-ttu-id="e9783-450">Fehlendes Cmdlet entfernt, auf das in der Dokumentation zu „New-AzResourceGroupDeployment“ verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="e9783-450">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="e9783-451">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-451">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e9783-452">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e9783-452">Az.ServiceBus</span></span>
* <span data-ttu-id="e9783-453">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="e9783-453">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="e9783-454">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="e9783-454">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="e9783-455">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9783-455">Az.Sql</span></span>
* <span data-ttu-id="e9783-456">Fehlende Beispiele für Cmdlet „Set-AzSqlDatabaseSecondary“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-456">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="e9783-457">Festlegen wiederkehrender Überprüfungen der Sicherheitsrisikobewertung ohne Angabe von E-Mail-Adressen korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-457">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="e9783-458">Tippfehler in einer Warnmeldung korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-458">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e9783-459">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e9783-459">Az.Storage</span></span>
* <span data-ttu-id="e9783-460">Beispiel in Referenzdokumentation für „Get-AzStorageAccount“ aktualisiert, sodass der richtige Parametername verwendet wird</span><span class="sxs-lookup"><span data-stu-id="e9783-460">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="e9783-461">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="e9783-461">Az.StorageSync</span></span>
* <span data-ttu-id="e9783-462">Cmdlet „Invoke-AzStorageSyncChangeDetection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-462">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="e9783-463">Problem 9551 zur Berücksichtigung von „TierFilesOlderThanDays“ behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-463">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e9783-464">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e9783-464">Az.Websites</span></span>
* <span data-ttu-id="e9783-465">Problem behoben, aufgrund dessen einige SiteConfig-Eigenschaften von „Get-AzWebApp“ und „Set-AzWebApp“ nicht zurückgegeben wurden</span><span class="sxs-lookup"><span data-stu-id="e9783-465">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="e9783-466">Neuer Standortparameter zu „Get-AzDeletedWebApp“ und „Restore-AzDeletedWebApp“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-466">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="e9783-467">Fehler beim Klonen von Web-App-Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-467">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="e9783-468">2.4.0 – Juli 2019</span><span class="sxs-lookup"><span data-stu-id="e9783-468">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e9783-469">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e9783-469">Az.Accounts</span></span>
* <span data-ttu-id="e9783-470">Unterstützung für Profil-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-470">Add support for profile cmdlets</span></span>
* <span data-ttu-id="e9783-471">Unterstützung für Umgebungen und Datenebenen in generierten Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-471">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="e9783-472">Korrektur eines Fehlers, bei dem in einigen Fällen ein falscher Endpunkt für Datenebenen-Cmdlets in Windows PowerShell verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="e9783-472">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="e9783-473">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="e9783-473">Az.Advisor</span></span>
* <span data-ttu-id="e9783-474">Allgemein verfügbares Release von Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="e9783-474">GA release of Az.Advisor</span></span>
* <span data-ttu-id="e9783-475">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="e9783-475">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e9783-476">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e9783-476">Az.ApiManagement</span></span>
* <span data-ttu-id="e9783-477">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="e9783-477">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="e9783-478">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="e9783-478">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="e9783-479">Unterstützung für Abfragen von Abonnements nach Benutzer und Produkt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-479">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="e9783-480">Unterstützung für Abfragen anhand des Umfangs hinzugefügt, „/“, „/apis“, „/apis/echo-api“</span><span class="sxs-lookup"><span data-stu-id="e9783-480">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="e9783-481">Behebung von Problem https://github.com/Azure/azure-powershell/issues/9307 und https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="e9783-481">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="e9783-482">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="e9783-482">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="e9783-483">Unterstützung für die Angabe von „ApiVersion“ und „ApiVersionSetId“ beim Importieren von APIs hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-483">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e9783-484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e9783-484">Az.Automation</span></span>
* <span data-ttu-id="e9783-485">Fehler beim Cmdlet „Set-AzAutomationConnectionFieldValue“ für die Verarbeitung des Zeichenfolgewerts behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-485">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9783-486">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9783-486">Az.Compute</span></span>
* <span data-ttu-id="e9783-487">Parameter „HyperVGeneration“ zu New-AzImageConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-487">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e9783-488">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e9783-488">Az.DataFactory</span></span>
* <span data-ttu-id="e9783-489">Aktualisierung der Ausgabe von ADF-Cmdlets für das Abrufen von Aktivitäts-, Pipeline- und Auslöserausführungen, um die Pipe „Select-Object“ zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="e9783-489">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e9783-490">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e9783-490">Az.EventGrid</span></span>
* <span data-ttu-id="e9783-491">Tippfehler in Dokumentation zu 'New-AzEventGridSubscription' behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-491">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e9783-492">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e9783-492">Az.IotHub</span></span>
* <span data-ttu-id="e9783-493">Unterstützung für das erneute Generieren von Autorisierungsrichtlinienschlüsseln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-493">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e9783-494">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9783-494">Az.Network</span></span>
* <span data-ttu-id="e9783-495">„RoutingPreference“ zu öffentlichen IP-Tags hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-495">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="e9783-496">Beispiele für Referenzdokumentation zu „Get-AzNetworkServiceTag“ verbessert</span><span class="sxs-lookup"><span data-stu-id="e9783-496">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e9783-497">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e9783-497">Az.PolicyInsights</span></span>
* <span data-ttu-id="e9783-498">Fehlerbehebung für Nullverweis in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="e9783-498">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="e9783-499">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="e9783-499">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e9783-500">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e9783-500">Az.OperationalInsights</span></span>
* <span data-ttu-id="e9783-501">Zurückgegebenes CustomLog-Datenquellenmodell in Get-AzOperationalInsightsDataSource korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-501">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e9783-502">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e9783-502">Az.RecoveryServices</span></span>
* <span data-ttu-id="e9783-503">Fehlerbehebung für Befehl „get-policy“ IaaSVMs</span><span class="sxs-lookup"><span data-stu-id="e9783-503">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="e9783-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9783-504">Az.Resources</span></span>
    - <span data-ttu-id="e9783-505">Hilfetext für Parameter „-Top“ von „Get-AzPolicyState“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-505">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="e9783-506">Clientseitige Unterstützung von Paginierung für „Get-AzPolicyAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-506">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="e9783-507">Neue Parameter für „Set-AzPolicyAssignment“, „-PolicyParameters“ und „-PolicyParametersObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-507">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="e9783-508">Einige Aktualisierungen von Dokumentationen und Beispielen für Policy-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="e9783-508">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e9783-509">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e9783-509">Az.ServiceBus</span></span>
* <span data-ttu-id="e9783-510">Korrektur für Problem Nr. 4938: „New-AzureRmServiceBusQueue“ gibt beim Festlegen von „MaxSizeInMegabytes“ „BadRequest“ zurück</span><span class="sxs-lookup"><span data-stu-id="e9783-510">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="e9783-511">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9783-511">Az.Sql</span></span>
* <span data-ttu-id="e9783-512">Instanzfailovergruppen-Cmdlets aus Vorschauversion in öffentliche Version hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-512">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="e9783-513">Unterstützung von Azure SQL Server\Datenbanküberwachung mit neuen Cmdlets</span><span class="sxs-lookup"><span data-stu-id="e9783-513">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="e9783-514">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="e9783-514">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="e9783-515">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="e9783-515">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="e9783-516">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="e9783-516">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="e9783-517">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="e9783-517">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="e9783-518">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="e9783-518">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="e9783-519">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="e9783-519">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="e9783-520">E-Mail-Einschränkungen aus Einstellungen der Sicherheitsrisikobewertung entfernt</span><span class="sxs-lookup"><span data-stu-id="e9783-520">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e9783-521">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e9783-521">Az.Storage</span></span>
* <span data-ttu-id="e9783-522">Zwei Parameter („-IndexDocument“ und „-ErrorDocument404Path“) in folgendem Cmdlet von erforderlich in optional geändert:</span><span class="sxs-lookup"><span data-stu-id="e9783-522">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="e9783-523">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e9783-523">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="e9783-524">Hilfe zu „Get-AzStorageBlobContent“ mit neuem Beispiel ergänzt</span><span class="sxs-lookup"><span data-stu-id="e9783-524">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="e9783-525">Anzeige von mehr Fehlerinformationen beim Fehlschlagen eines Cmdlets mit „StorageException“</span><span class="sxs-lookup"><span data-stu-id="e9783-525">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="e9783-526">Unterstützung für das Erstellen oder Aktualisieren von Speicherkonten mit Azure Files AAD-DS-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="e9783-526">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="e9783-527">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e9783-527">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="e9783-528">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e9783-528">Set-AzStorageAccount</span></span>
* <span data-ttu-id="e9783-529">Unterstützung für das Auflisten oder Schließen von Dateihandles einer Dateifreigabe, eines Dateiverzeichnisses oder einer Datei</span><span class="sxs-lookup"><span data-stu-id="e9783-529">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="e9783-530">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="e9783-530">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="e9783-531">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="e9783-531">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="e9783-532">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="e9783-532">Az.StorageSync</span></span>
* <span data-ttu-id="e9783-533">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="e9783-533">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="e9783-534">2.3.2 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="e9783-534">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e9783-535">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e9783-535">Az.Accounts</span></span>
* <span data-ttu-id="e9783-536">Fehler behoben, aufgrund dessen in manchen Fällen eine falsche URL für Funktionsaufrufe verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="e9783-536">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="e9783-537">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="e9783-537">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="e9783-538">Problem mit Aliasen zwischen AzureRM und Azure-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-538">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="e9783-539">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e9783-539">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="e9783-540">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="e9783-540">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9783-541">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9783-541">Az.Compute</span></span>
* <span data-ttu-id="e9783-542">Die einfachen Parametersätze „New-AzVm“ und „New-AzVmss“ akzeptieren jetzt den Parameter „ProximityPlacementGroup“.</span><span class="sxs-lookup"><span data-stu-id="e9783-542">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="e9783-543">Tippfehler in der Referenzdokumentation für „New-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-543">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="e9783-544">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="e9783-544">Az.Dns</span></span>
* <span data-ttu-id="e9783-545">Tippfehler in den Hilfebeispielen zu „Set-AzDnsZone“ behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-545">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e9783-546">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e9783-546">Az.EventGrid</span></span>
* <span data-ttu-id="e9783-547">Zur Verwendung der API-Version 2019-06-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-547">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="e9783-548">Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="e9783-548">New cmdlets:</span></span>
    - <span data-ttu-id="e9783-549">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e9783-549">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="e9783-550">Erstellt eine neue Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="e9783-550">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="e9783-551">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e9783-551">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="e9783-552">Ruft die Details einer Event Grid-Domäne oder eine Liste aller Event Grid-Domänen im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="e9783-552">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="e9783-553">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e9783-553">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="e9783-554">Entfernt eine Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="e9783-554">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="e9783-555">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="e9783-555">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="e9783-556">Generiert den freigegebenen Zugriffsschlüssel für eine Azure Event Grid-Domäne erneut.</span><span class="sxs-lookup"><span data-stu-id="e9783-556">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="e9783-557">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="e9783-557">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="e9783-558">Ruft die freigegebenen Zugriffsschlüssel ab, die zum Veröffentlichen von Ereignissen in einer Event Grid-Domäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e9783-558">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="e9783-559">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="e9783-559">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="e9783-560">Erstellt ein neues Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="e9783-560">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="e9783-561">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="e9783-561">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="e9783-562">Ruft die Details eines Event Grid-Domänenthemas oder eine Liste aller Event Grid-Domänenthemen unter der jeweiligen Event Grid-Domäne im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="e9783-562">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="e9783-563">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="e9783-563">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="e9783-564">Entfernt ein vorhandenes Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="e9783-564">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="e9783-565">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="e9783-565">Updated cmdlets:</span></span>
    - <span data-ttu-id="e9783-566">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="e9783-566">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="e9783-567">Neue erforderliche Parameter zur Unterstützung des Pipings für die neue Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="e9783-567">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="e9783-568">Neue erforderliche Parameter zum Angeben des neuen Event Grid-Domänennamens und/oder Namens des Event Grid-Domänenthemas hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="e9783-568">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="e9783-569">Neue Parametersätze für Domänen und Domänenthemen hinzugefügt, um die Wiederverwendung vorhandener Parameter zuzulassen (‚z. B. „EndPointType“, „SubjectBeginsWith“ usw.)</span><span class="sxs-lookup"><span data-stu-id="e9783-569">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="e9783-570">Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="e9783-570">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="e9783-571">Ablaufdatum des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="e9783-571">Event subscription expiration date,</span></span>
            - <span data-ttu-id="e9783-572">Erweiterte Filterparameter</span><span class="sxs-lookup"><span data-stu-id="e9783-572">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="e9783-573">Neue Enumeration für „servicebusqueue“ als Ziel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-573">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="e9783-574">Verwendung der Option „All“ in „-IncludedEventType“ gesperrt und wie folgt ersetzt</span><span class="sxs-lookup"><span data-stu-id="e9783-574">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="e9783-575">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="e9783-575">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="e9783-576">Neue optionale Parameter („Top“, „ODataQuery“ und „NextLink“) zur Unterstützung der Ergebnispaginierung und -filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-576">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="e9783-577">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="e9783-577">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="e9783-578">Neue erforderliche Parameter zur Unterstützung des Pipings für die Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Entfernen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="e9783-578">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="e9783-579">Neue erforderliche Parameter zum Angeben des Event Grid-Domänennamens und/oder Event Grid-Domänenthemanamens hinzugefügt, um das Entfernen vorhandener Ereignisabonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="e9783-579">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e9783-580">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e9783-580">Az.FrontDoor</span></span>
* <span data-ttu-id="e9783-581">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="e9783-581">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="e9783-582">Unterstützung von Transformationen und neuen Wert für den Operator zum automatischen Vervollständigen (RegEx) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-582">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="e9783-583">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="e9783-583">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="e9783-584">Neue Werte für automatisches Vervollständigen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-584">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e9783-585">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9783-585">Az.Network</span></span>
* <span data-ttu-id="e9783-586">Unterstützung für Virtual Network-Gatewayressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-586">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="e9783-587">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="e9783-587">New cmdlets</span></span>
        - <span data-ttu-id="e9783-588">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="e9783-588">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="e9783-589">AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="e9783-589">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="e9783-590">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="e9783-590">New cmdlets</span></span> 
        - <span data-ttu-id="e9783-591">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="e9783-591">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="e9783-592">„PrivatePrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-592">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="e9783-593">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="e9783-593">New cmdlets</span></span> 
        - <span data-ttu-id="e9783-594">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e9783-594">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="e9783-595">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e9783-595">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="e9783-596">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e9783-596">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="e9783-597">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e9783-597">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="e9783-598">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e9783-598">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="e9783-599">„PrivateEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-599">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="e9783-600">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="e9783-600">New cmdlets</span></span>
        - <span data-ttu-id="e9783-601">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e9783-601">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e9783-602">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e9783-602">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e9783-603">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e9783-603">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e9783-604">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="e9783-604">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="e9783-605">Folgende Befehle für das Feature aktualisiert: UseLocalAzureIpAddress-Flag für „VpnConnection“</span><span class="sxs-lookup"><span data-stu-id="e9783-605">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="e9783-606">„New-AzVpnConnection§ „ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="e9783-606">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="e9783-607">„Set-AzVpnConnection“ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="e9783-607">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="e9783-608">Schreibgeschütztes Feld „PeeredConnections“ beim ExpressRoute-Peering hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-608">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="e9783-609">Schreibgeschütztes Feld „GlobalReachEnabled“ in ExpressRoute hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-609">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="e9783-610">Breaking Change-Attribut hinzugefügt, um auf das veraltete Feld „AllowGlobalReach“ im ExpressRouteCircuit-Modell hinzuweisen</span><span class="sxs-lookup"><span data-stu-id="e9783-610">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="e9783-611">Fehler 8756 bei der Verwendung von „TargetListenerID“ mit AzApplicationGatewayRedirectConfiguration-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-611">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="e9783-612">Fehler in „New-AzApplicationGatewayPathRuleConfig“ behoben, aufgrund dessen der Regelsatz für erneutes Generieren nicht festgelegt werden konnte</span><span class="sxs-lookup"><span data-stu-id="e9783-612">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="e9783-613">Fehler bei der Anzeige von „VirtualNetworkTaps“ in „NetworkInterfaceIpConfiguration“ behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-613">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="e9783-614">Cortex-Get-Cmdlets zum Auflisten aller Komponenten korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-614">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="e9783-615">Problem beim Erstellen des festen VirtualHub-Verweises für ExpressRouteGateways behoben (VpnGateway)</span><span class="sxs-lookup"><span data-stu-id="e9783-615">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="e9783-616">Unterstützung für Verfügbarkeitszonen in AzureFirewall und NatGateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-616">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="e9783-617">Cmdlet „Get-AzNetworkServiceTag“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-617">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="e9783-618">Unterstützung für mehrere öffentliche IP-Adressen für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-618">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="e9783-619">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="e9783-619">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="e9783-620">Parameter „-PublicIpAddress“ hinzugefügt, der ein oder mehre öffentliche IP-Adressobjekte akzeptiert</span><span class="sxs-lookup"><span data-stu-id="e9783-620">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="e9783-621">Parameter „- VirtualNetwork“ hinzugefügt, der ein Virtual Network-Objekt akzeptiert</span><span class="sxs-lookup"><span data-stu-id="e9783-621">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="e9783-622">Methoden „AddPublicIpAddress“ und „RemovePublicIpAddress“ für Firewallobjekte hinzugefügt (akzeptieren ein öffentliches IP-Adressobjekt als Eingabe)</span><span class="sxs-lookup"><span data-stu-id="e9783-622">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="e9783-623">Parameter „-PublicIpName“ und „-VirtualNetworkName“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="e9783-623">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="e9783-624">Folgende Befehle für das Feature aktualisiert: VpnClient-AAD-Authentifizierungsoptionen auf die Gatewayressource des virtuellen Netzwerkgateways festgelegt</span><span class="sxs-lookup"><span data-stu-id="e9783-624">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="e9783-625">„New-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-625">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="e9783-626">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e9783-626">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="e9783-627">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionaler Switch-Parameter „RemoveAadAuthentication“ zum Entfernen von VpnClient-AAD-Authentifizierungsoptionen aus dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-627">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e9783-628">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e9783-628">Az.OperationalInsights</span></span>
* <span data-ttu-id="e9783-629">Tarif **pergb2018** im Befehl „New-AzureRmOperationalInsightsWorkspace“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="e9783-629">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="e9783-630">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9783-630">Az.Resources</span></span>
* <span data-ttu-id="e9783-631">Unterstützung für zusätzliche Optionen zum Exportieren von Vorlagen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-631">Support for additional Template Export options</span></span>
    - <span data-ttu-id="e9783-632">Parameter „-SkipResourceNameParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-632">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="e9783-633">Parameter -SkipAllParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-633">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="e9783-634">Parameter „-Resource“ zu „Export-AzResourceGroup“ hinzugefügt, um das Filtern exportierter Ressourcen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="e9783-634">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e9783-635">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e9783-635">Az.ServiceFabric</span></span>
* <span data-ttu-id="e9783-636">Problem beim Hinzufügen des Zertifikats mit „ByExistingKeyVault“ behoben (Abruf des falschen Fingerabdrucks in manchen Fällen)</span><span class="sxs-lookup"><span data-stu-id="e9783-636">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="e9783-637">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9783-637">Az.Sql</span></span>
* <span data-ttu-id="e9783-638">Suffix des Advanced Threat Protection-Endpunkts korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-638">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="e9783-639">Durch Advanced Data Security ermöglichte Außerkraftsetzungen der Advanced Threat Protection-Richtlinie korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-639">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="e9783-640">Neue Cmdlets für „Management.Sql“ ermöglichen Kunden das Hinzufügen von TDE-Schlüsseln und Festlegen der TDE-Schutzvorrichtung für verwaltete Instanzen.</span><span class="sxs-lookup"><span data-stu-id="e9783-640">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="e9783-641">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e9783-641">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="e9783-642">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e9783-642">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="e9783-643">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e9783-643">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="e9783-644">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="e9783-644">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="e9783-645">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="e9783-645">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e9783-646">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e9783-646">Az.Storage</span></span>
* <span data-ttu-id="e9783-647">Unterstützung von „FileStorage“ und „SkuName Premium_ZRS“ beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="e9783-647">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="e9783-648">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e9783-648">New-AzStorageAccount</span></span>
* <span data-ttu-id="e9783-649">Überarbeitete Beschreibung des Cmdlets für die Unveränderlichkeit von Blobs</span><span class="sxs-lookup"><span data-stu-id="e9783-649">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="e9783-650">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="e9783-650">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e9783-651">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e9783-651">Az.Websites</span></span>
* <span data-ttu-id="e9783-652">Optimiert „Get-AzWebAppCertificate“, um nach der Ressourcengruppe auf dem Server zu filtern (nicht auf dem Client)</span><span class="sxs-lookup"><span data-stu-id="e9783-652">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="e9783-653">Switch-Parameter „-UseDisasterRecovery“ für „Get-AzWebAppSnapshot“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-653">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="e9783-654">2.2.0 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="e9783-654">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="e9783-655">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e9783-655">Az.Cdn</span></span>
* <span data-ttu-id="e9783-656">Es wurden Cmdlets aktualisiert, um das rulesEngine-Feature basierend auf der API-Version 2019-04-15 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e9783-656">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9783-657">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9783-657">Az.Compute</span></span>
* <span data-ttu-id="e9783-658">Der Parameter `NoWait` wurde hinzugefügt, der den Vorgang startet und sofort zurückkehrt, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="e9783-658">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="e9783-659">Aktualisierte Cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="e9783-659">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e9783-660">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e9783-660">Az.EventHub</span></span>
* <span data-ttu-id="e9783-661">Fehlerbehebung für #9231 – Get-AzEventHubNamespace gibt keine Tags zurück</span><span class="sxs-lookup"><span data-stu-id="e9783-661">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="e9783-662">Fehlerbehebung für #9230 – Get-AzEventHubNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="e9783-662">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e9783-663">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9783-663">Az.Network</span></span>
* <span data-ttu-id="e9783-664">ResourceId und InputObject wurden für NAT Gateway aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-664">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="e9783-665">Es wurde ein Alias für ResourceId und InputObjectr hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-665">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e9783-666">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e9783-666">Az.PolicyInsights</span></span>
* <span data-ttu-id="e9783-667">Fehlerbehebung für Nullverweis in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="e9783-667">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e9783-668">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e9783-668">Az.RecoveryServices</span></span>
* <span data-ttu-id="e9783-669">Minimale Aufbewahrung in Tagen für IaaSVM-Richtlinie wurde von 1 in 7 geändert</span><span class="sxs-lookup"><span data-stu-id="e9783-669">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e9783-670">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e9783-670">Az.ServiceBus</span></span>
* <span data-ttu-id="e9783-671">Fehlerbehebung für #9182 – Get-AzServiceBusNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="e9783-671">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e9783-672">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e9783-672">Az.ServiceFabric</span></span>
* <span data-ttu-id="e9783-673">Tippfehler in Fehlermeldung für Update-AzServiceFabricReliability wurde behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-673">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="e9783-674">Fehlendes Zeichen in Service Fabric-Befehlszeilen wurde behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-674">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="e9783-675">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9783-675">Az.Sql</span></span>
* <span data-ttu-id="e9783-676">Der DnsZonePartner-Parameter für das Cmdlet New-AzureSqlInstance wurde hinzugefügt, um AutoDr für verwaltete Instanzen zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="e9783-676">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="e9783-677">Das Cmdlet Get-AzSqlDatabaseSecureConnectionPolicy wird eingestellt</span><span class="sxs-lookup"><span data-stu-id="e9783-677">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="e9783-678">Cmdlets zum Schutz vor Bedrohungen werden in „Advanced Threat Protection“ (Erweiterter Schutz vor Bedrohungen) umbenannt</span><span class="sxs-lookup"><span data-stu-id="e9783-678">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="e9783-679">New-AzSqlInstance – Die Parameter StorageSizeInGB und LicenseType sind jetzt optional</span><span class="sxs-lookup"><span data-stu-id="e9783-679">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e9783-680">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e9783-680">Az.Websites</span></span>
* <span data-ttu-id="e9783-681">Das Problem, bei dem die Verwendung von Set-AzWebApp und Set-AzWebAppSlot mit der -WebApp-Eigenschaft die Tags entfernt hat, wurde behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-681">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="e9783-682">2.1.0 – Mai 2019</span><span class="sxs-lookup"><span data-stu-id="e9783-682">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="e9783-683">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e9783-683">Az.ApiManagement</span></span>
* <span data-ttu-id="e9783-684">Es wurden neue Cmdlets zum Verwalten der Diagnose im globalen sowie im API-Bereich erstellt</span><span class="sxs-lookup"><span data-stu-id="e9783-684">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="e9783-685">**Get-AzApiManagementDiagnostic**: Abrufen der Diagnose, die im globalen oder im API-Bereich konfiguriert wurde</span><span class="sxs-lookup"><span data-stu-id="e9783-685">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="e9783-686">**New-AzApiManagementDiagnostic**: Erstellen neuer Diagnosen im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="e9783-686">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="e9783-687">**New-AzApiManagementHttpMessageDiagnostic**: Erstellen einer Diagnoseeinstellung für die zu protokollierenden Kopfzeilen und für die Größe der Bytes für den Text</span><span class="sxs-lookup"><span data-stu-id="e9783-687">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="e9783-688">**New-AzApiManagementPipelineDiagnosticSetting**: Erstellen von Diagnoseeinstellungen für ein-/ausgehende HTTP-Nachrichten für das Gateway</span><span class="sxs-lookup"><span data-stu-id="e9783-688">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="e9783-689">**New-AzApiManagementSamplingSetting**: Erstellen der Einstellung „Sampling“ für die Anforderungen/Antworten für eine Diagnose</span><span class="sxs-lookup"><span data-stu-id="e9783-689">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="e9783-690">**Remove-AzApiManagementDiagnostic**: Entfernen einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="e9783-690">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="e9783-691">**Set-AzApiManagementDiagnostic**: Aktualisieren einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="e9783-691">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="e9783-692">Es wurden neue Cmdlets für die Cacheverwaltung im ApiManagement-Dienst erstellt</span><span class="sxs-lookup"><span data-stu-id="e9783-692">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="e9783-693">**Get-AzApiManagementCache**: Abrufen der Details des durch den Bezeichner angegebenen Caches oder aller Caches</span><span class="sxs-lookup"><span data-stu-id="e9783-693">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="e9783-694">**New-AzApiManagementCache**: Erstellen eines neuen „standardmäßigen“ Caches oder eines Caches in einer bestimmten „Region“ von Azure</span><span class="sxs-lookup"><span data-stu-id="e9783-694">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="e9783-695">**Remove-AzApiManagementCache**: Entfernen eines Caches</span><span class="sxs-lookup"><span data-stu-id="e9783-695">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="e9783-696">**Update-AzApiManagementCache**: Aktualisieren eines Caches</span><span class="sxs-lookup"><span data-stu-id="e9783-696">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="e9783-697">Es wurden neue Cmdlets zur Verwaltung von API-Schemas erstellt</span><span class="sxs-lookup"><span data-stu-id="e9783-697">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="e9783-698">**New-AzApiManagementSchema**: Erstellen eines neuen Schemas für eine API</span><span class="sxs-lookup"><span data-stu-id="e9783-698">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="e9783-699">**Get-AzApiManagementSchema**: Abrufen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="e9783-699">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="e9783-700">**Remove-AzApiManagementSchema**: Entfernen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="e9783-700">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="e9783-701">**Set-AzApiManagementSchema**: Aktualisieren des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="e9783-701">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="e9783-702">Es wurde ein neues Cmdlet zum Generieren eines Benutzertokens erstellt</span><span class="sxs-lookup"><span data-stu-id="e9783-702">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="e9783-703">**New-AzApiManagementUserToken**: Generieren eines neuen Benutzertokens, das standardmäßig für acht Stunden gültig ist. Mit diesem Cmdlet kann das Token für den „GIT“-Benutzer generiert werden./</span><span class="sxs-lookup"><span data-stu-id="e9783-703">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="e9783-704">Es wurde ein neues Cmdlet zum Abrufen des Netzwerkstatus erstellt</span><span class="sxs-lookup"><span data-stu-id="e9783-704">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="e9783-705">**Get-AzApiManagementNetworkStatus**: Abrufen der Netzwerkstatuskonnektivität von Ressourcen, von denen der API Management-Dienst abhängig ist</span><span class="sxs-lookup"><span data-stu-id="e9783-705">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="e9783-706">Dies ist hilfreich, wenn Sie den ApiManagement-Dienst in einem virtuellen Netzwerk bereitstellen und überprüfen, ob eine der Abhängigkeiten fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="e9783-706">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="e9783-707">Das Cmdlet **New-AzApiManagement** wurde zum Verwalten des ApiManagement-Diensts aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-707">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="e9783-708">Die Unterstützung für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-708">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="e9783-709">Die Unterstützung zum Aktivieren des Flags „EnableClientCertificate“ für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-709">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="e9783-710">Das neue Cmdlet **New-AzApiManagementSslSetting** ermöglicht die Konfiguration der „TLS/SSL“-Einstellung für „Back-End“ und „Front-End“</span><span class="sxs-lookup"><span data-stu-id="e9783-710">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="e9783-711">Dies kann auch dazu verwendet werden, um „Verschlüsselungen“ wie „3DES“ und „ServerProtokolle“ wie „Http2“ für das „Front-End“ eines ApiManagement-Diensts zu konfigurieren</span><span class="sxs-lookup"><span data-stu-id="e9783-711">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="e9783-712">Die Unterstützung für die Konfiguration des Hostnamens „DeveloperPortal“ wurde zum ApiManagement-Dienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-712">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="e9783-713">Die **Get-AzApiManagementSsoToken**-Cmdlets wurden aktualisiert, um das Objekt „PsApiManagement“ als Eingabe zu übernehmen</span><span class="sxs-lookup"><span data-stu-id="e9783-713">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="e9783-714">Das Cmdlet wurde aktualisiert, um Fehlermeldungen inline anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="e9783-714">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="e9783-715">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Fehlercode: ValidationError-Fehlermeldung: Mindestens ein Feld enthält ungültige Werte: Fehlerdetails: [Code=ValidationError, Message=Fehler in Element 'log-to-eventhub' in Zeile 3, Spalte 10: Protokollierungstool nicht gefunden, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="e9783-715">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="e9783-716">Cmdlet **Export-AzApiManagementApi** wurde für den Export von APIs im Format „OpenApi 3.0“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-716">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="e9783-717">Cmdlet **Import-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-717">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="e9783-718">Zum Importieren der API aus der „OpenApi 3.0“-Dokumentspezifikation</span><span class="sxs-lookup"><span data-stu-id="e9783-718">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="e9783-719">Zur Außerkraftsetzung der „PsApiManagementSchema“-Eigenschaft, die in einem beliebigen Dokument („Swagger“, „Wadl“, „Wsdl“, „OpenApi“) angegeben ist</span><span class="sxs-lookup"><span data-stu-id="e9783-719">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="e9783-720">Zur Außerkraftsetzung der „ServiceUrl“-Eigenschaft, die in einem beliebigen Dokument angegeben ist</span><span class="sxs-lookup"><span data-stu-id="e9783-720">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="e9783-721">Cmdlet **Get-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="e9783-721">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="e9783-722">Cmdlet **Set-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ und im Format mit XML-Escapezeichen mit „xml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="e9783-722">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="e9783-723">Cmdlet **New-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-723">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="e9783-724">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="e9783-724">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="e9783-725">Zum Erstellen einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="e9783-725">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="e9783-726">Zum Klonen einer API mithilfe von „SourceApiId“ und „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="e9783-726">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="e9783-727">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="e9783-727">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="e9783-728">Cmdlet **Set-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-728">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="e9783-729">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="e9783-729">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="e9783-730">Zum Aktualisieren einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="e9783-730">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="e9783-731">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="e9783-731">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="e9783-732">Cmdlet **New-AzApiManagementRevision** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-732">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="e9783-733">Zum Klonen (Kopiertags, Produkte, Vorgänge und Richtlinien) einer vorhandenen Version mithilfe von „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="e9783-733">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="e9783-734">Die neue Version übernimmt die „ApiId“ des übergeordneten Elements</span><span class="sxs-lookup"><span data-stu-id="e9783-734">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="e9783-735">Zum Bereitstellen einer „ApiRevisionDescription“</span><span class="sxs-lookup"><span data-stu-id="e9783-735">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="e9783-736">Zur Außerkraftsetzung der „ServiceUrl“ beim Klonen einer API</span><span class="sxs-lookup"><span data-stu-id="e9783-736">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="e9783-737">Cmdlet **New-AzApiManagementIdentityProvider** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-737">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="e9783-738">Zum Konfigurieren von „AAD“ oder „AADB2C“ mit einer „Authority“</span><span class="sxs-lookup"><span data-stu-id="e9783-738">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="e9783-739">Zum Einrichten von „SignupPolicy“, „SigninPolicy“, „ProfileEditingPolicy“ und „PasswordResetPolicy“</span><span class="sxs-lookup"><span data-stu-id="e9783-739">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="e9783-740">Cmdlet **New-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-740">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="e9783-741">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="e9783-741">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="e9783-742">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="e9783-742">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="e9783-743">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-743">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="e9783-744">Cmdlet **Set-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-744">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="e9783-745">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="e9783-745">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="e9783-746">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="e9783-746">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="e9783-747">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-747">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="e9783-748">Folgende Cmdlets wurden aktualisiert, um „ResourceId“ als Eingabe zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="e9783-748">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="e9783-749">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="e9783-749">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="e9783-750">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="e9783-750">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="e9783-751">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="e9783-751">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="e9783-752">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="e9783-752">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="e9783-753">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="e9783-753">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="e9783-754">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="e9783-754">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="e9783-755">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="e9783-755">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="e9783-756">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="e9783-756">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="e9783-757">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="e9783-757">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="e9783-758">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="e9783-758">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="e9783-759">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="e9783-759">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="e9783-760">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="e9783-760">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e9783-761">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e9783-761">Az.Automation</span></span>
* <span data-ttu-id="e9783-762">Get-AzAutomationJobOutputRecord wurde aktualisiert, um JSON- und Textdatensatzwerte zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="e9783-762">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="e9783-763">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="e9783-763">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="e9783-764">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="e9783-764">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="e9783-765">Das Verhalten von Start-AzAutomationDscCompilationJob wurde geändert, um den Auftrag einfach zu starten, anstatt auf dessen Abschluss zu warten</span><span class="sxs-lookup"><span data-stu-id="e9783-765">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="e9783-766">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="e9783-766">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="e9783-767">Fehlerbehebung für Get-AzAutomationDscNode, wenn die Verwendung von „-Name“ alle Knoten zurückgibt</span><span class="sxs-lookup"><span data-stu-id="e9783-767">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="e9783-768">Jetzt wird nur der übereinstimmende Knoten zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="e9783-768">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9783-769">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9783-769">Az.Compute</span></span>
* <span data-ttu-id="e9783-770">Parameter „ProtectFromScaleIn“ und „ProtectFromScaleSetAction“ wurden zum Cmdlet „Update-AzVmssVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-770">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="e9783-771">Der jetzt festgelegte wimple-Parameter „New-AzVM“ verwendet standardmäßig einen verfügbaren Standort, wenn „East US“ (USA, Osten) nicht unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="e9783-771">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e9783-772">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e9783-772">Az.DataLakeStore</span></span>
* <span data-ttu-id="e9783-773">Das ADLS-SDK wurde aktualisiert, um „HttpClient“ zu verwenden und Datenebenentests wurden mit dem Azure-Framework integriert</span><span class="sxs-lookup"><span data-stu-id="e9783-773">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e9783-774">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e9783-774">Az.Monitor</span></span>
* <span data-ttu-id="e9783-775">Fehlerbehebung bei falschen Parameternamen in Hilfebeispielen</span><span class="sxs-lookup"><span data-stu-id="e9783-775">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e9783-776">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9783-776">Az.Network</span></span>
* <span data-ttu-id="e9783-777">DisableBgpRoutePropagation-Flag wurde zur Ausgabe der effektiven Routentabelle hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-777">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="e9783-778">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e9783-778">Updated cmdlet:</span></span>
        - <span data-ttu-id="e9783-779">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="e9783-779">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="e9783-780">Fehlerbehebung von doppeltem Bindestrich in Dokumentation von New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e9783-780">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="e9783-781">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9783-781">Az.Resources</span></span>
* <span data-ttu-id="e9783-782">Neues Cmdlet „Get-AzureRmDenyAssignment“ zum Abrufen von Ablehnungszuweisungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-782">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="e9783-783">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9783-783">Az.Sql</span></span>
* <span data-ttu-id="e9783-784">„Advanced Threat Protection“-Cmdlets in „Advanced Data Security“ umbenennen und Sicherheitsrisikobewertung standardmäßig aktivieren</span><span class="sxs-lookup"><span data-stu-id="e9783-784">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="e9783-785">2.0.0: Mai 2019</span><span class="sxs-lookup"><span data-stu-id="e9783-785">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e9783-786">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e9783-786">Az.Accounts</span></span>
* <span data-ttu-id="e9783-787">Authentifizierungsbibliothek aktualisiert, um ADFS-Probleme mit der Authentifizierung per Benutzername/Kennwort zu beheben</span><span class="sxs-lookup"><span data-stu-id="e9783-787">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e9783-788">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e9783-788">Az.CognitiveServices</span></span>
* <span data-ttu-id="e9783-789">Ausschließliche Anzeige des Bing-Haftungsausschlusses für Bing-Suchdienste</span><span class="sxs-lookup"><span data-stu-id="e9783-789">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="e9783-790">Fehler behoben, der zu einem Fehler bei der Kontoerstellung führte</span><span class="sxs-lookup"><span data-stu-id="e9783-790">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9783-791">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9783-791">Az.Compute</span></span>
* <span data-ttu-id="e9783-792">Feature für die Näherungsplatzierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="e9783-792">Proximity placement group feature.</span></span>
    - <span data-ttu-id="e9783-793">Die folgenden neuen Cmdlets wurden hinzugefügt:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="e9783-793">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="e9783-794">Der neue Parameter „ProximityPlacementGroupId“ wurde zu den folgenden Cmdlets hinzugefügt:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="e9783-794">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="e9783-795">Der Parameter „StorageAccountType“ wurde zu „New-AzGalleryImageVersion“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e9783-795">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="e9783-796">„TargetRegion“ von „New-AzGalleryImageVersion“ kann „StorageAccountType“ enthalten.</span><span class="sxs-lookup"><span data-stu-id="e9783-796">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="e9783-797">Switch-Parameter „SkipShutdown“ wurde zu „Stop-AzVM“ und „Stop-AzVmss“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e9783-797">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="e9783-798">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="e9783-798">Breaking changes</span></span>
    - <span data-ttu-id="e9783-799">„Set-AzVMBootDiagnostics“ in „Set-AzVMBootDiagnostic“ geändert</span><span class="sxs-lookup"><span data-stu-id="e9783-799">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="e9783-800">„Export-AzLogAnalyticThrottledRequests“ in „Export-AzLogAnalyticThrottledRequests“ geändert</span><span class="sxs-lookup"><span data-stu-id="e9783-800">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="e9783-801">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="e9783-801">Az.DeploymentManager</span></span>
* <span data-ttu-id="e9783-802">Erste allgemein verfügbare Version der Azure-Bereitstellungs-Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="e9783-802">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="e9783-803">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="e9783-803">Az.Dns</span></span>
* <span data-ttu-id="e9783-804">Automatische Delegierung des DNS-Namenservers</span><span class="sxs-lookup"><span data-stu-id="e9783-804">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="e9783-805">Das Cmdlet zum Erstellen einer DNS-Zone akzeptiert den übergeordneten Zonennamen als zusätzlichen optionalen Parameter.</span><span class="sxs-lookup"><span data-stu-id="e9783-805">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="e9783-806">NS-Einträge in der übergeordneten Zone für neu erstellte untergeordnete Zone hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-806">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e9783-807">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e9783-807">Az.FrontDoor</span></span>
* <span data-ttu-id="e9783-808">Erste allgemein verfügbare Version der Azure Frontdoor-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="e9783-808">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="e9783-809">WAF-Cmdlets so umbenannt, dass sie „Waf“ enthalten</span><span class="sxs-lookup"><span data-stu-id="e9783-809">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="e9783-810">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e9783-810">Az.HDInsight</span></span>
* <span data-ttu-id="e9783-811">Zwei Cmdlets entfernt:</span><span class="sxs-lookup"><span data-stu-id="e9783-811">Removed two cmdlets:</span></span>
    - <span data-ttu-id="e9783-812">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e9783-812">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="e9783-813">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e9783-813">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="e9783-814">Neues Cmdlet „Set-AzHDInsightGatewayCredential“ hinzugefügt, um „Grant-AzHDInsightHttpServicesAccess“ zu ersetzen</span><span class="sxs-lookup"><span data-stu-id="e9783-814">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="e9783-815">Cmdlet „Get-AzHDInsightJobOutput“ aktualisiert, um zwischen Leserrolle und HDInsight-Bedienerrolle zu unterscheiden:</span><span class="sxs-lookup"><span data-stu-id="e9783-815">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="e9783-816">Benutzer mit der Rolle „Leser“ müssen den Parameter „DefaultStorageAccountKey“ explizit angeben, andernfalls treten Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="e9783-816">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="e9783-817">Benutzer mit der Rolle des HDInsight-Bedieners sind nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="e9783-817">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e9783-818">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e9783-818">Az.Monitor</span></span>
* <span data-ttu-id="e9783-819">Neue Cmdlets für SQR-API (Scheduled Query Rule, geplante Abfrageregel)</span><span class="sxs-lookup"><span data-stu-id="e9783-819">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="e9783-820">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="e9783-820">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="e9783-821">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="e9783-821">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="e9783-822">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="e9783-822">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="e9783-823">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="e9783-823">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="e9783-824">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="e9783-824">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="e9783-825">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="e9783-825">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="e9783-826">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e9783-826">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e9783-827">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e9783-827">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e9783-828">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e9783-828">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e9783-829">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e9783-829">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e9783-830">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e9783-830">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e9783-831">[Weitere Informationen](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) zur SQR-API</span><span class="sxs-lookup"><span data-stu-id="e9783-831">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="e9783-832">„Az.Monitor.md“ aktualisiert, um Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch) einzuschließen</span><span class="sxs-lookup"><span data-stu-id="e9783-832">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e9783-833">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9783-833">Az.Network</span></span>
* <span data-ttu-id="e9783-834">Unterstützung für NAT-Gatewayressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-834">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="e9783-835">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="e9783-835">New cmdlets</span></span>
        - <span data-ttu-id="e9783-836">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e9783-836">New-AzNatGateway</span></span>
        - <span data-ttu-id="e9783-837">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e9783-837">Get-AzNatGateway</span></span>
        - <span data-ttu-id="e9783-838">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e9783-838">Set-AzNatGateway</span></span>
        - <span data-ttu-id="e9783-839">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e9783-839">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="e9783-840">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="e9783-840">Updated cmdlets</span></span>
        - <span data-ttu-id="e9783-841">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="e9783-841">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="e9783-842">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="e9783-842">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="e9783-843">Folgende Befehle für das Feature aktualisiert: Benutzerdefinierte Routen für Brooklyn-Gateway festgelegt/entfernt</span><span class="sxs-lookup"><span data-stu-id="e9783-843">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="e9783-844">„New-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="e9783-844">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="e9783-845">„Set-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="e9783-845">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e9783-846">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e9783-846">Az.PolicyInsights</span></span>
* <span data-ttu-id="e9783-847">Unterstützung für die Abfrage von Richtlinienauswertungsdetails</span><span class="sxs-lookup"><span data-stu-id="e9783-847">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="e9783-848">Parameter „-Expand“ zu „Get-AzPolicyState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-848">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="e9783-849">Unterstützung für „-Expand PolicyEvaluationDetails“</span><span class="sxs-lookup"><span data-stu-id="e9783-849">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e9783-850">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e9783-850">Az.RecoveryServices</span></span>
* <span data-ttu-id="e9783-851">Unterstützung für abonnementübergreifende Azure-zu-Azure-Sitewiederherstellung</span><span class="sxs-lookup"><span data-stu-id="e9783-851">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="e9783-852">Markierung anstehender wichtiger Änderungen für Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="e9783-852">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="e9783-853">Fehlerbehebung für Azure Site Recovery-Wiederherstellungsplan und -Aktionsplan</span><span class="sxs-lookup"><span data-stu-id="e9783-853">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="e9783-854">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Netzwerkzuordnung für Azure zu Azure</span><span class="sxs-lookup"><span data-stu-id="e9783-854">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="e9783-855">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Schutzrichtung für Azure zu Azure für verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="e9783-855">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="e9783-856">Weitere kleinere Korrekturen</span><span class="sxs-lookup"><span data-stu-id="e9783-856">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="e9783-857">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="e9783-857">Az.Relay</span></span>
* <span data-ttu-id="e9783-858">Korrektur von Tippfehlern in Kundennachrichten</span><span class="sxs-lookup"><span data-stu-id="e9783-858">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e9783-859">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e9783-859">Az.ServiceBus</span></span>
* <span data-ttu-id="e9783-860">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-860">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e9783-861">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e9783-861">Az.Storage</span></span>
* <span data-ttu-id="e9783-862">Upgrade auf Speicherclientbibliothek 10.0.1 (Namespace aller Objekte von diesem SDK von „Microsoft.WindowsAzure.Storage. *“ in „Microsoft.Azure.Storage.* “ geändert)</span><span class="sxs-lookup"><span data-stu-id="e9783-862">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="e9783-863">Upgrade auf Microsoft.Azure.Management.Storage 11.0.0, um die neue API-Version 2019-04-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="e9783-863">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="e9783-864">Art des Standardspeicherkontos bei der Speicherkontoerstellung von „Storage“ in „StorageV2“ geändert</span><span class="sxs-lookup"><span data-stu-id="e9783-864">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="e9783-865">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e9783-865">New-AzStorageAccount</span></span>
* <span data-ttu-id="e9783-866">Vom Speicherkonto-Cmdlet ausgegebener SKU-Name (Sku.Name) durch Hinzufügen eines Unterstrichs an SKU-Eingabename angepasst (Beispiel: „StandardLRS“ > „Standard_LRS“).</span><span class="sxs-lookup"><span data-stu-id="e9783-866">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="e9783-867">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e9783-867">New-AzStorageAccount</span></span>
    - <span data-ttu-id="e9783-868">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e9783-868">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="e9783-869">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e9783-869">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e9783-870">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e9783-870">Az.Websites</span></span>
* <span data-ttu-id="e9783-871">Die Eigenschaft „Kind“ wird nun für PSSite-Objekte festgelegt, die von „Get-AzWebApp“ zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e9783-871">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="e9783-872">„Get-AzWebApp\*Metrics“ und „Get-AzAppServicePlanMetrics“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="e9783-872">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="e9783-873">1.8.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="e9783-873">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e9783-874">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="e9783-874">Highlights since the last major release</span></span>
* <span data-ttu-id="e9783-875">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="e9783-875">General availability of `Az` module</span></span>
* <span data-ttu-id="e9783-876">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="e9783-876">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e9783-877">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="e9783-877">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e9783-878">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-878">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e9783-879">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-879">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e9783-880">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-880">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e9783-881">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="e9783-881">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e9783-882">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e9783-882">Az.Accounts</span></span>
* <span data-ttu-id="e9783-883">„Uninstall-AzureRm“ aktualisiert, um Module unter Mac ordnungsgemäß zu löschen</span><span class="sxs-lookup"><span data-stu-id="e9783-883">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e9783-884">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e9783-884">Az.Batch</span></span>
* <span data-ttu-id="e9783-885">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="e9783-885">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e9783-886">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e9783-886">Az.Cdn</span></span>
* <span data-ttu-id="e9783-887">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="e9783-887">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e9783-888">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e9783-888">Az.CognitiveServices</span></span>
* <span data-ttu-id="e9783-889">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="e9783-889">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9783-890">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9783-890">Az.Compute</span></span>
* <span data-ttu-id="e9783-891">Problem mit der AEM-Installation behoben, wenn die Ressourcen-IDs von Datenträgern Ressourcengruppen in Kleinbuchstaben enthielten</span><span class="sxs-lookup"><span data-stu-id="e9783-891">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="e9783-892">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="e9783-892">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e9783-893">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-893">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e9783-894">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e9783-894">Az.DataFactory</span></span>
* <span data-ttu-id="e9783-895">„SsisProperties“ hinzugefügt, falls „NodeCount“ für verwaltete Integration Runtime nicht NULL ist</span><span class="sxs-lookup"><span data-stu-id="e9783-895">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e9783-896">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e9783-896">Az.DataLakeStore</span></span>
* <span data-ttu-id="e9783-897">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="e9783-897">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e9783-898">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e9783-898">Az.EventGrid</span></span>
* <span data-ttu-id="e9783-899">Hilfetext für Endpunkt aktualisiert, um anzugeben, dass Ressourcen erstellt werden müssen, bevor die Cmdlets zum Erstellen/Aktualisieren von Ereignisabonnements verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e9783-899">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e9783-900">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e9783-900">Az.EventHub</span></span>
* <span data-ttu-id="e9783-901">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-901">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="e9783-902">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e9783-902">Az.HDInsight</span></span>
* <span data-ttu-id="e9783-903">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="e9783-903">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e9783-904">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e9783-904">Az.IotHub</span></span>
* <span data-ttu-id="e9783-905">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="e9783-905">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e9783-906">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e9783-906">Az.KeyVault</span></span>
* <span data-ttu-id="e9783-907">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="e9783-907">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e9783-908">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-908">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="e9783-909">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e9783-909">Az.MachineLearning</span></span>
* <span data-ttu-id="e9783-910">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="e9783-910">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="e9783-911">Az.Media</span><span class="sxs-lookup"><span data-stu-id="e9783-911">Az.Media</span></span>
* <span data-ttu-id="e9783-912">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="e9783-912">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e9783-913">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e9783-913">Az.Monitor</span></span>
  * <span data-ttu-id="e9783-914">Neue Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch)</span><span class="sxs-lookup"><span data-stu-id="e9783-914">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="e9783-915">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="e9783-915">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="e9783-916">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="e9783-916">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="e9783-917">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e9783-917">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="e9783-918">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e9783-918">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="e9783-919">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e9783-919">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="e9783-920">Monitor SDK auf Version 0.22.0-preview aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-920">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e9783-921">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9783-921">Az.Network</span></span>
* <span data-ttu-id="e9783-922">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="e9783-922">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e9783-923">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-923">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="e9783-924">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="e9783-924">Az.NotificationHubs</span></span>
* <span data-ttu-id="e9783-925">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="e9783-925">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e9783-926">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e9783-926">Az.OperationalInsights</span></span>
* <span data-ttu-id="e9783-927">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="e9783-927">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="e9783-928">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="e9783-928">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="e9783-929">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="e9783-929">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e9783-930">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e9783-930">Az.RecoveryServices</span></span>
* <span data-ttu-id="e9783-931">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="e9783-931">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e9783-932">Tabellenformat für SQL auf Azure-VM aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-932">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="e9783-933">Alternative Methode zum Abrufen des Speicherorts in „AzureFileShare“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-933">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="e9783-934">„ScheduleRunDays“ in SchedulePolicy-Objekt gemäß Zeitzone aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-934">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e9783-935">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e9783-935">Az.RedisCache</span></span>
* <span data-ttu-id="e9783-936">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="e9783-936">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e9783-937">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9783-937">Az.Resources</span></span>
* <span data-ttu-id="e9783-938">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-938">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="e9783-939">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9783-939">Az.Sql</span></span>
* <span data-ttu-id="e9783-940">Abhängigkeit vom Monitor SDK durch allgemeinen Code ersetzt</span><span class="sxs-lookup"><span data-stu-id="e9783-940">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="e9783-941">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="e9783-941">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e9783-942">Verbesserter Prozess für Klassifizierung mehrerer Spalten</span><span class="sxs-lookup"><span data-stu-id="e9783-942">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="e9783-943">SKU-Eigenschaften (SKU-Name, Familie, Kapazität) in Antwort von „Get-AzSqlServerServiceObjective“ aufgenommen und standardmäßig als Tabelle formatiert</span><span class="sxs-lookup"><span data-stu-id="e9783-943">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="e9783-944">Möglichkeit zum Ausführen von „Get-AzSqlServerServiceObjective“ nach Standort, ohne dass bereits ein Server in der Region vorhanden sein muss</span><span class="sxs-lookup"><span data-stu-id="e9783-944">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="e9783-945">Unterstützung für Zeitzonenparameter bei der Erstellung einer verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="e9783-945">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="e9783-946">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-946">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e9783-947">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e9783-947">Az.Websites</span></span>
* <span data-ttu-id="e9783-948">„Set-AzWebApp“ und „Set-AzWebAppSlot“ korrigiert, sodass die Tags bei der Ausführung nicht entfernt werden</span><span class="sxs-lookup"><span data-stu-id="e9783-948">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="e9783-949">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="e9783-949">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e9783-950">WebSites SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-950">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="e9783-951">AdminSiteName-Eigenschaft aus „PSAppServicePlan“ entfernt</span><span class="sxs-lookup"><span data-stu-id="e9783-951">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="e9783-952">1.7.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="e9783-952">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e9783-953">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="e9783-953">Highlights since the last major release</span></span>
* <span data-ttu-id="e9783-954">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="e9783-954">General availability of `Az` module</span></span>
* <span data-ttu-id="e9783-955">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="e9783-955">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e9783-956">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="e9783-956">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e9783-957">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-957">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e9783-958">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-958">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e9783-959">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-959">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e9783-960">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="e9783-960">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e9783-961">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e9783-961">Az.Accounts</span></span>
* <span data-ttu-id="e9783-962">„Add-AzEnvironment“ und „Set-AzEnvironment“ aktualisiert, um den Parameter „AzureAnalysisServicesEndpointResourceId“ zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="e9783-962">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e9783-963">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e9783-963">Az.AnalysisServices</span></span>
* <span data-ttu-id="e9783-964">ServiceClient wird in Cmdlets für die Datenebene verwendet, und die ursprüngliche Authentifizierungslogik wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="e9783-964">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="e9783-965">„Add-AzureASAccount“ wird als Wrapper von „Connect-AzAccount“ festgelegt, um einen Breaking Change zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="e9783-965">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e9783-966">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e9783-966">Az.Automation</span></span>
* <span data-ttu-id="e9783-967">Fehler des Cmdlets „Fixed New-AzAutomationSoftwareUpdateConfiguration“ für Einschlüsse behoben.</span><span class="sxs-lookup"><span data-stu-id="e9783-967">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="e9783-968">Die Parameter „IncludedKbNumber“ und „IncludedPackageNameMask“ sollten nun funktionieren.</span><span class="sxs-lookup"><span data-stu-id="e9783-968">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="e9783-969">Fehlerbehebung für eine dynamische Gruppe der Azure Automation-Updateverwaltung</span><span class="sxs-lookup"><span data-stu-id="e9783-969">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9783-970">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9783-970">Az.Compute</span></span>
* <span data-ttu-id="e9783-971">Parameter „HyperVGeneration“ zu „New-AzDiskConfig“ und „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-971">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="e9783-972">Zulassen der VM-Erstellung mit einem Katalogimage aus anderen Mandanten</span><span class="sxs-lookup"><span data-stu-id="e9783-972">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="e9783-973">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e9783-973">Az.ContainerInstance</span></span>
* <span data-ttu-id="e9783-974">Problem im Parameter „-Command“ von „New-AzContainerGroup“ behoben, das dazu führte, dass ein nachgestelltes leeres Argument hinzugefügt wurde</span><span class="sxs-lookup"><span data-stu-id="e9783-974">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e9783-975">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e9783-975">Az.DataFactory</span></span>
* <span data-ttu-id="e9783-976">Version des ADF .NET SDK auf 3.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-976">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="e9783-977">Cmdlet „Set-AzDataFactoryV2“ mit zusätzlichen Parametern für RepoConfiguration-Einstellungen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-977">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e9783-978">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9783-978">Az.Resources</span></span>
* <span data-ttu-id="e9783-979">Verarbeitung von Anbietern für „Get-AzResource“ bei der Angabe der Parameter „-ResourceId“ oder „-ResourceGroupName“, „-Name“ und „-ResourceType“ verbessert</span><span class="sxs-lookup"><span data-stu-id="e9783-979">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="e9783-980">Fehlerbehandlung für „Test-AzDeployment“ und „Test-AzResourceGroupDeployment“ verbessert</span><span class="sxs-lookup"><span data-stu-id="e9783-980">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="e9783-981">Behandlung von außerhalb der Bereitstellungsüberprüfung aufgetretenen Fehlern und stattdessen Aufnahme in die Ausgabe des Befehls</span><span class="sxs-lookup"><span data-stu-id="e9783-981">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="e9783-982">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="e9783-982">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="e9783-983">Switch-Parameter „-IgnoreDynamicParameters“ zu Bereitstellungs-Cmdlets hinzugefügt, um Aufforderung in Skript- und Auftragsszenarien zu überspringen</span><span class="sxs-lookup"><span data-stu-id="e9783-983">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="e9783-984">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="e9783-984">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="e9783-985">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9783-985">Az.Sql</span></span>
* <span data-ttu-id="e9783-986">Unterstützung für Klassifizierung von Datenbankdaten</span><span class="sxs-lookup"><span data-stu-id="e9783-986">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e9783-987">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e9783-987">Az.Storage</span></span>
* <span data-ttu-id="e9783-988">Melden eines ausführlichen Fehlers beim Erstellen des Storage-Kontexts mit dem Parameter „-UseConnectedAccount“, aber ohne Azure-Anmeldekonto</span><span class="sxs-lookup"><span data-stu-id="e9783-988">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="e9783-989">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e9783-989">New-AzStorageContext</span></span>
* <span data-ttu-id="e9783-990">Unterstützung für das Verwalten von Blobdiensteigenschaften eines bestimmten Storage-Kontos mit einer API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="e9783-990">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="e9783-991">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="e9783-991">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="e9783-992">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="e9783-992">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="e9783-993">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e9783-993">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="e9783-994">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e9783-994">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="e9783-995">Unterstützung von „-AsJob“ für Cmdlets für den Upload und Download von Blobs und Dateien</span><span class="sxs-lookup"><span data-stu-id="e9783-995">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="e9783-996">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e9783-996">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="e9783-997">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e9783-997">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="e9783-998">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e9783-998">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="e9783-999">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e9783-999">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="e9783-1000">1.6.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="e9783-1000">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e9783-1001">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="e9783-1001">Highlights since the last major release</span></span>
* <span data-ttu-id="e9783-1002">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="e9783-1002">General availability of `Az` module</span></span>
* <span data-ttu-id="e9783-1003">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="e9783-1003">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e9783-1004">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="e9783-1004">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e9783-1005">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1005">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e9783-1006">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1006">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e9783-1007">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1007">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e9783-1008">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="e9783-1008">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e9783-1009">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e9783-1009">Az.Automation</span></span>
* <span data-ttu-id="e9783-1010">Änderung an der Azure Automation-Updateverwaltung, um die folgenden neuen Features zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="e9783-1010">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="e9783-1011">Dynamische Gruppierung</span><span class="sxs-lookup"><span data-stu-id="e9783-1011">Dynamic grouping</span></span>
    * <span data-ttu-id="e9783-1012">Pre-/Post-Skripts</span><span class="sxs-lookup"><span data-stu-id="e9783-1012">Pre-Post script</span></span>
    * <span data-ttu-id="e9783-1013">Neustarteinstellung</span><span class="sxs-lookup"><span data-stu-id="e9783-1013">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9783-1014">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9783-1014">Az.Compute</span></span>
* <span data-ttu-id="e9783-1015">Problem mit der Pfadauflösung in „Get-AzVmBootDiagnosticsData“ behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-1015">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="e9783-1016">Computeclientbibliothek auf 25.0.0. aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1016">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e9783-1017">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e9783-1017">Az.KeyVault</span></span>
* <span data-ttu-id="e9783-1018">Unterstützung für Platzhalterzeichen zu KeyVault-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1018">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e9783-1019">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9783-1019">Az.Network</span></span>
* <span data-ttu-id="e9783-1020">Threat Intelligence-Unterstützung für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1020">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="e9783-1021">Ressource der obersten Ebene für Application Gateway-Firewallrichtlinie und benutzerdefinierte Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1021">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e9783-1022">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e9783-1022">Az.RecoveryServices</span></span>
* <span data-ttu-id="e9783-1023">SnapshotRetentionInDays in Azure-VM-Richtlinie hinzugefügt, um sofortigen Wiederherstellungspunkt zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="e9783-1023">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="e9783-1024">Pipe-Unterstützung für das Aufheben der Registrierung eines Containers hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1024">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="e9783-1025">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9783-1025">Az.Resources</span></span>
* <span data-ttu-id="e9783-1026">Unterstützung für Platzhalterzeichen für Get-AzResource und Get-AzResourceGroup aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1026">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="e9783-1027">Anmeldeinformationen aktualisiert, die beim Senden generischer Aufrufe an ARM verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e9783-1027">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="e9783-1028">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9783-1028">Az.Sql</span></span>
* <span data-ttu-id="e9783-1029">Der Cmdlet-Parameter der Bedrohungserkennung (ExcludeDetectionType) wurde von „DetectionType“ in „string[]“ geändert, um ihn zukunftssicher zu machen, wenn neue DetectionTypes-Elemente hinzugefügt werden, und um AutoVervollständigen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e9783-1029">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e9783-1030">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e9783-1030">Az.Storage</span></span>
* <span data-ttu-id="e9783-1031">Unterstützung von Get-/Set-/Remove-Verwaltungsrichtlinien für Speicherkonto hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1031">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="e9783-1032">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e9783-1032">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e9783-1033">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e9783-1033">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e9783-1034">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e9783-1034">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e9783-1035">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="e9783-1035">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="e9783-1036">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="e9783-1036">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="e9783-1037">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="e9783-1037">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e9783-1038">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e9783-1038">Az.Websites</span></span>
* <span data-ttu-id="e9783-1039">ARM-Vorlagenfehler behoben, der zu einem Problem beim Klonen aller Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ führte</span><span class="sxs-lookup"><span data-stu-id="e9783-1039">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="e9783-1040">1.5.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="e9783-1040">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e9783-1041">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e9783-1041">Az.Accounts</span></span>
* <span data-ttu-id="e9783-1042">Der Befehl „Register-AzModule“ wurde hinzugefügt, um von AutoRest generierte Cmdlets zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e9783-1042">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="e9783-1043">Beispiele für „Connect-AzAccount“ wurden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="e9783-1043">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e9783-1044">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e9783-1044">Az.Automation</span></span>
* <span data-ttu-id="e9783-1045">Problem behoben, das beim Abrufen bestimmter monatlicher Zeitpläne in verschiedenen Azure Automation-Cmdlets auftrat</span><span class="sxs-lookup"><span data-stu-id="e9783-1045">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="e9783-1046">„Get-AzAutomationDscNode“ wurde korrigiert, da nur die 20 obersten Knoten zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="e9783-1046">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="e9783-1047">Jetzt werden alle Knoten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e9783-1047">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e9783-1048">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e9783-1048">Az.Cdn</span></span>
* <span data-ttu-id="e9783-1049">Neue Powershell-Cmdlets zum Aktivieren/Deaktivieren von HTTPS für benutzerdefinierte Domänen hinzugefügt und alte Cmdlets außer Betrieb genommen</span><span class="sxs-lookup"><span data-stu-id="e9783-1049">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9783-1050">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9783-1050">Az.Compute</span></span>
* <span data-ttu-id="e9783-1051">Unterstützung für Platzhalterzeichen zu Get-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1051">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e9783-1052">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e9783-1052">Az.DataFactory</span></span>
* <span data-ttu-id="e9783-1053">Version des ADF .NET SDK auf 3.0.1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1053">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e9783-1054">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e9783-1054">Az.LogicApp</span></span>
* <span data-ttu-id="e9783-1055">„ListWorkflows“ wurde korrigiert, da nur die erste Seite mit Ergebnissen abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="e9783-1055">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e9783-1056">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9783-1056">Az.Network</span></span>
* <span data-ttu-id="e9783-1057">Unterstützung für Platzhalterzeichen zu Network-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1057">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e9783-1058">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e9783-1058">Az.RecoveryServices</span></span>
* <span data-ttu-id="e9783-1059">SQL Server jetzt in Azure-VM-Support enthalten</span><span class="sxs-lookup"><span data-stu-id="e9783-1059">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="e9783-1060">SDK-Update</span><span class="sxs-lookup"><span data-stu-id="e9783-1060">SDK Update</span></span>
* <span data-ttu-id="e9783-1061">VMappContainer-Überprüfung in „Get-ProtectableItem“ entfernt</span><span class="sxs-lookup"><span data-stu-id="e9783-1061">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="e9783-1062">„Name“ und „ServerName“ als Parameter für „Get-ProtectableItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1062">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="e9783-1063">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9783-1063">Az.Resources</span></span>
* <span data-ttu-id="e9783-1064">Parameter `-TemplateObject` zu Bereitstellungs-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1064">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="e9783-1065">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="e9783-1065">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="e9783-1066">Problem beim Piping des Ergebnisses von `Get-AzResource` an `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-1066">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="e9783-1067">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="e9783-1067">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="e9783-1068">Problem mit JSON-Datentypänderung beim Ausführen von `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-1068">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="e9783-1069">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="e9783-1069">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="e9783-1070">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9783-1070">Az.Sql</span></span>
* <span data-ttu-id="e9783-1071">„AuditingEndpointsCommunicator“ wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="e9783-1071">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="e9783-1072">Das Verhalten eines Grenzfalls beim Erstellen neuer Diagnoseeinstellungen wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="e9783-1072">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e9783-1073">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e9783-1073">Az.Storage</span></span>
* <span data-ttu-id="e9783-1074">Unterstützung von „Kind BlockBlobStorage“ beim Erstellen eines Speicherkontos: New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e9783-1074">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="e9783-1075">1.4.0 – Februar 2019</span><span class="sxs-lookup"><span data-stu-id="e9783-1075">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="e9783-1076">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e9783-1076">Az.AnalysisServices</span></span>
* <span data-ttu-id="e9783-1077">Cmdlet „AddAzureASAccount“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1077">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e9783-1078">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e9783-1078">Az.Automation</span></span>
* <span data-ttu-id="e9783-1079">Hilfe für „Import-AzAutomationDscNodeConfiguration“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1079">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="e9783-1080">Überprüfung des Konfigurationsnamens zu Cmdlet „Import-AzAutomationDscConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1080">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="e9783-1081">Fehlerbehandlung für Cmdlet „Import-AzAutomationDscConfiguration“ verbessert</span><span class="sxs-lookup"><span data-stu-id="e9783-1081">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e9783-1082">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e9783-1082">Az.CognitiveServices</span></span>
* <span data-ttu-id="e9783-1083">„CustomSubdomainName“ als neuer optionaler Parameter für Cmdlet „New-AzCognitiveServicesAccount“ hinzugefügt, das zum Angeben der Unterdomäne für die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e9783-1083">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9783-1084">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9783-1084">Az.Compute</span></span>
* <span data-ttu-id="e9783-1085">Problem mit ID-Parametersätzen behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-1085">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="e9783-1086">„Get-AzVMExtension“ aktualisiert, sodass alle installierten Erweiterungen aufgelistet werden, wenn der Name-Parameter nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="e9783-1086">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="e9783-1087">Parameter „Tag“ und „ResourceId“ zum Cmdlet „Update-AzImage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1087">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="e9783-1088">„Get-AzVmssVM“ ohne Instanz-ID und mit „InstanceView“ können virtuelle VMSS-Computer mit Instanzansicht auflisten.</span><span class="sxs-lookup"><span data-stu-id="e9783-1088">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e9783-1089">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e9783-1089">Az.DataLakeStore</span></span>
* <span data-ttu-id="e9783-1090">Cmdlets zum Auflisten und Wiederherstellen gelöschter ADL-Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1090">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e9783-1091">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e9783-1091">Az.EventHub</span></span>
* <span data-ttu-id="e9783-1092">Neue boolesche Eigenschaft „SkipEmptyArchives“ zum Überspringen leerer Archive in Klasse „CaptureDescription“ von EventHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1092">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="e9783-1093">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e9783-1093">Az.KeyVault</span></span>
* <span data-ttu-id="e9783-1094">Kennzeichnung in „Set-AzKeyVaultSecret“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1094">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e9783-1095">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e9783-1095">Az.LogicApp</span></span>
* <span data-ttu-id="e9783-1096">SKU „Basic“ für Integrationskonten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1096">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="e9783-1097">XSLT 2.0, XSLT 3.0 und Liquid-Zuordnungstypen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1097">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="e9783-1098">Neue Cmdlets für Integrationskonto-Assemblys</span><span class="sxs-lookup"><span data-stu-id="e9783-1098">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="e9783-1099">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e9783-1099">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e9783-1100">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e9783-1100">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e9783-1101">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e9783-1101">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e9783-1102">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e9783-1102">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="e9783-1103">Neue Cmdlets für Integrationskonto-Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="e9783-1103">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="e9783-1104">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9783-1104">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e9783-1105">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9783-1105">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e9783-1106">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9783-1106">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e9783-1107">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9783-1107">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="e9783-1108">Logik-App-SDK auf Version 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1108">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e9783-1109">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e9783-1109">Az.Monitor</span></span>
* <span data-ttu-id="e9783-1110">Hilfe für „Get-AzMetric“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1110">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e9783-1111">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9783-1111">Az.Network</span></span>
* <span data-ttu-id="e9783-1112">Hilfebeispiel für „Add-AzApplicationGatewayCustomError“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1112">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e9783-1113">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e9783-1113">Az.OperationalInsights</span></span>
* <span data-ttu-id="e9783-1114">Zusätzliche Unterstützung für Datenquelle von „New-ApplicationInsights“ und „Get-ApplicationInsights“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e9783-1114">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="e9783-1115">Neue Art von „ApplicationInsights“ zum Abrufen von bestimmten und von allen ApplicationInsights-Datenquellen für einen Workspace hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e9783-1115">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="e9783-1116">Cmdlet „New-AzOperationalInsightsApplicationInsightsDataSource“ zum Erstellen einer Datenquelle anhand des angegebenen Ressourcenparameters für „Application-Insights“ hinzugefügt: „subscriptionId“, „resourceGroupName“ und „name“.</span><span class="sxs-lookup"><span data-stu-id="e9783-1116">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="e9783-1117">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9783-1117">Az.Resources</span></span>
* <span data-ttu-id="e9783-1118">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="e9783-1118">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="e9783-1119">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="e9783-1119">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="e9783-1120">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="e9783-1120">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="e9783-1121">Fehler korrigiert, der die wiederholte Erstellung von „KeyCredentials“ verhindert</span><span class="sxs-lookup"><span data-stu-id="e9783-1121">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="e9783-1122">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9783-1122">Az.Sql</span></span>
* <span data-ttu-id="e9783-1123">Unterstützung für SQL DB Hyperscale-Tarif hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1123">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="e9783-1124">Fehler korrigiert, aufgrund dessen die Wiederherstellung wegen der Festlegung unnötiger Eigenschaften in der Wiederherstellungsanforderung fehlschlagen konnte</span><span class="sxs-lookup"><span data-stu-id="e9783-1124">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e9783-1125">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e9783-1125">Az.Websites</span></span>
* <span data-ttu-id="e9783-1126">Beispiel in „Get-AzWebAppSlotMetrics“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1126">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="e9783-1127">1.3.0: Februar 2019</span><span class="sxs-lookup"><span data-stu-id="e9783-1127">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e9783-1128">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e9783-1128">Az.Accounts</span></span>
* <span data-ttu-id="e9783-1129">Update auf die aktuelle Version von ClientRuntime durchgeführt</span><span class="sxs-lookup"><span data-stu-id="e9783-1129">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e9783-1130">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e9783-1130">Az.AnalysisServices</span></span>
<span data-ttu-id="e9783-1131">Allgemeine Verfügbarkeit für Az.AnalysisServices-Modul</span><span class="sxs-lookup"><span data-stu-id="e9783-1131">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9783-1132">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9783-1132">Az.Compute</span></span>
* <span data-ttu-id="e9783-1133">AEM-Erweiterung: Unterstützung für UltraSSD und P60-, P70- und P80-Datenträger hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1133">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="e9783-1134">Hilfebeschreibung für „Set-AzVMBootDiagnostics“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1134">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="e9783-1135">Hilfebeschreibung und Beispiel für „Update-AzImage“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1135">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e9783-1136">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e9783-1136">Az.RecoveryServices</span></span>
<span data-ttu-id="e9783-1137">Allgemeine Verfügbarkeit für Az.RecoveryServices-Modul.</span><span class="sxs-lookup"><span data-stu-id="e9783-1137">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e9783-1138">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9783-1138">Az.Resources</span></span>
* <span data-ttu-id="e9783-1139">Kennzeichnung für Ressourcengruppen korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1139">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="e9783-1140">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="e9783-1140">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="e9783-1141">Problem behoben, bei dem „-ErrorAction“ von `Get-AzureRmRoleAssignment` nicht berücksichtigt wird</span><span class="sxs-lookup"><span data-stu-id="e9783-1141">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="e9783-1142">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="e9783-1142">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="e9783-1143">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9783-1143">Az.Sql</span></span>
* <span data-ttu-id="e9783-1144">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1144">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="e9783-1145">Problem behoben, bei dem eine fehlende Anmeldung am Azure-Konto bei der Ausführung von SQL-Cmdlets zu einer nullref-Ausnahme führt</span><span class="sxs-lookup"><span data-stu-id="e9783-1145">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="e9783-1146">nullref-Ausnahme in Get-AzSqlCapability korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1146">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="e9783-1147">1.2.1: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="e9783-1147">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e9783-1148">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e9783-1148">Az.Accounts</span></span>
* <span data-ttu-id="e9783-1149">Release mit richtiger Version der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="e9783-1149">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e9783-1150">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e9783-1150">Az.AnalysisServices</span></span>
* <span data-ttu-id="e9783-1151">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="e9783-1151">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e9783-1152">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e9783-1152">Az.RecoveryServices</span></span>
* <span data-ttu-id="e9783-1153">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="e9783-1153">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="e9783-1154">1.2.0: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="e9783-1154">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e9783-1155">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e9783-1155">Az.Accounts</span></span>
* <span data-ttu-id="e9783-1156">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1156">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e9783-1157">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1157">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e9783-1158">Warnmeldung in PS Core für „Uninstall-AzureRm“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1158">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="e9783-1159">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e9783-1159">Az.Aks</span></span>
* <span data-ttu-id="e9783-1160">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1160">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e9783-1161">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e9783-1161">Az.Automation</span></span>
* <span data-ttu-id="e9783-1162">Unterstützung für Python 2-Runbooks hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1162">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="e9783-1163">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1163">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e9783-1164">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e9783-1164">Az.Cdn</span></span>
* <span data-ttu-id="e9783-1165">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1165">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9783-1166">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9783-1166">Az.Compute</span></span>
* <span data-ttu-id="e9783-1167">Cmdlet „Invoke-AzVMReimage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1167">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="e9783-1168">Parameter „TempDisk“ zu „Set-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1168">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="e9783-1169">Warnmeldung von „New-AzVM“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1169">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="e9783-1170">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e9783-1170">Az.ContainerRegistry</span></span>
* <span data-ttu-id="e9783-1171">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1171">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e9783-1172">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e9783-1172">Az.DataFactory</span></span>
* <span data-ttu-id="e9783-1173">Version des ADF .NET SDK auf 3.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1173">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e9783-1174">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e9783-1174">Az.DataLakeStore</span></span>
* <span data-ttu-id="e9783-1175">Problem mit ADLS-Endpunkt bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-1175">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="e9783-1176">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="e9783-1176">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="e9783-1177">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1177">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e9783-1178">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e9783-1178">Az.IotHub</span></span>
* <span data-ttu-id="e9783-1179">Codierungsformat zu Cmdlet „Add-IotHubRoutingEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1179">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e9783-1180">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e9783-1180">Az.KeyVault</span></span>
* <span data-ttu-id="e9783-1181">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1181">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e9783-1182">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9783-1182">Az.Network</span></span>
* <span data-ttu-id="e9783-1183">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1183">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="e9783-1184">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9783-1184">Az.Resources</span></span>
* <span data-ttu-id="e9783-1185">Fehlerhafte Beispiele in Referenzdokumentation zu „New-AzADAppCredential“ und „New-AzADSpCredential“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1185">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="e9783-1186">Problem behoben, bei dem der Pfad für den Parameter „-TemplateFile“ nicht aufgelöst wurde, bevor Cmdlets für die Bereitstellung von Ressourcengruppen ausgeführt wurden</span><span class="sxs-lookup"><span data-stu-id="e9783-1186">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="e9783-1187">Az.Resources: Richtige Dokumentation für Standardwert von „New-AzureRmPolicyDefinition -Mode“ bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="e9783-1187">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="e9783-1188">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="e9783-1188">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="e9783-1189">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="e9783-1189">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="e9783-1190">Formatierungsproblem für Objekt „PSResourceGroupDeployment“ behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-1190">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="e9783-1191">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="e9783-1191">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e9783-1192">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e9783-1192">Az.ServiceFabric</span></span>
* <span data-ttu-id="e9783-1193">Rollback beim Hinzufügen eines Zertifikats zum VMSS-Modell, Auslösung einer Ausnahme. Fehlerbehebung: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="e9783-1193">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="e9783-1194">Einige Fehlermeldungen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="e9783-1194">Fix some error messages.</span></span>
* <span data-ttu-id="e9783-1195">Fehler bei Clustererstellung mit ARM-Standardvorlage für „New-AzServiceFabriCluster“ behoben, bei dem die Migration zu Az nicht funktioniert hat.</span><span class="sxs-lookup"><span data-stu-id="e9783-1195">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="e9783-1196">Fehler behoben beim Hinzufügen eines Cluster-/Anwendungszertifikats ausschließlich zu VM Scale Sets, die zum Cluster gehören, indem die Cluster-ID in der Erweiterung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="e9783-1196">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e9783-1197">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e9783-1197">Az.SignalR</span></span>
* <span data-ttu-id="e9783-1198">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1198">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="e9783-1199">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9783-1199">Az.Sql</span></span>
* <span data-ttu-id="e9783-1200">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1200">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e9783-1201">Parameterbeschreibung für den Parameter „LicenseType“ mit möglichen Werten aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1201">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="e9783-1202">Fehler behoben, bei dem die Aktualisierung der Identität der verwalteten Instanz nicht funktioniert hat, wenn es sich um die einzige aktualisierte Eigenschaft gehandelt hat</span><span class="sxs-lookup"><span data-stu-id="e9783-1202">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="e9783-1203">Unterstützung für die benutzerdefinierte Sortierung auf verwalteter Instanz</span><span class="sxs-lookup"><span data-stu-id="e9783-1203">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e9783-1204">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e9783-1204">Az.Storage</span></span>
* <span data-ttu-id="e9783-1205">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1205">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e9783-1206">Ausführliche Fehlermeldung beim Abrufen/Festlegen der klassischen Protokollierung bzw. Metriken für Storage Premium-Konto, da für das Storage Premium-Konto die klassische Protokollierung bzw. Metriken nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e9783-1206">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="e9783-1207">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="e9783-1207">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="e9783-1208">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="e9783-1208">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="e9783-1209">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="e9783-1209">Az.TrafficManager</span></span>
* <span data-ttu-id="e9783-1210">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1210">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e9783-1211">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e9783-1211">Az.Websites</span></span>
* <span data-ttu-id="e9783-1212">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1212">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e9783-1213">„New-AzWebAppSSLBinding“ korrigiert, damit das Zertifikat in die richtige Ressourcengruppe bzw. an den richtigen Speicherort hochgeladen wird, wenn die App in einer ASE gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="e9783-1213">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="e9783-1214">„New-AzWebAppSSLBinding“ korrigiert, damit die Tags beim Binden eines SSL-Zertifikats an eine App nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e9783-1214">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="e9783-1215">1.1.0 – Januar 2019</span><span class="sxs-lookup"><span data-stu-id="e9783-1215">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e9783-1216">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e9783-1216">Az.Accounts</span></span>
* <span data-ttu-id="e9783-1217">Bereich „Local“ zu „Enable-AzureRmAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1217">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9783-1218">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9783-1218">Az.Compute</span></span>
* <span data-ttu-id="e9783-1219">Name ist jetzt optional im ID-Parametersatz für „Restart/Start/Stop/Remove/Set-AzVM“ und „Save-AzVMImage“</span><span class="sxs-lookup"><span data-stu-id="e9783-1219">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="e9783-1220">Beschreibung der ID in Hilfedateien aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1220">Updated the description of ID in help files</span></span>
* <span data-ttu-id="e9783-1221">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-1221">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e9783-1222">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e9783-1222">Az.DataLakeStore</span></span>
* <span data-ttu-id="e9783-1223">Aktualisierung der SDK-Version der Datenebene auf 1.1.14 für SDK-Fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="e9783-1223">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="e9783-1224">Behandlung von negativen acesstime- and modificationtime-Werten für „getfilestatus“ und „liststatus“ korrigiert, asynchrones Abbruchtoken korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1224">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e9783-1225">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e9783-1225">Az.EventGrid</span></span>
* <span data-ttu-id="e9783-1226">Zur Verwendung der API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1226">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="e9783-1227">Aktualisierung der folgenden Cmdlets zur Unterstützung des neuen Szenarios in der API-Version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="e9783-1227">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="e9783-1228">New-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="e9783-1228">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="e9783-1229">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="e9783-1229">Event Time-To-Live,</span></span>
        - <span data-ttu-id="e9783-1230">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="e9783-1230">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="e9783-1231">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="e9783-1231">Dead letter endpoint.</span></span>
    - <span data-ttu-id="e9783-1232">Update-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="e9783-1232">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="e9783-1233">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="e9783-1233">Event Time-To-Live,</span></span>
        - <span data-ttu-id="e9783-1234">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="e9783-1234">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="e9783-1235">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="e9783-1235">Dead letter endpoint.</span></span>
* <span data-ttu-id="e9783-1236">Neue Enumerationswerte („storageQueue“ und „hybridConnection“) für die EndpointType-Option in den Cmdlets „New-AzureRmEventGridSubscription“ und „Update-AzureRmEventGridSubscription“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1236">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="e9783-1237">Anzeige einer Warnmeldung, wenn das Erstellen oder Aktualisieren des Ereignisabonnements voraussichtlich eine manuelle Aktion des Benutzers zur Folge hat</span><span class="sxs-lookup"><span data-stu-id="e9783-1237">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e9783-1238">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e9783-1238">Az.IotHub</span></span>
* <span data-ttu-id="e9783-1239">Auf die aktuelle Version des Iot Hub SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1239">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e9783-1240">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e9783-1240">Az.LogicApp</span></span>
* <span data-ttu-id="e9783-1241">„Get-AzLogicApp“ listet alle Apps ohne angegebenen Namen auf</span><span class="sxs-lookup"><span data-stu-id="e9783-1241">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="e9783-1242">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9783-1242">Az.Resources</span></span>
* <span data-ttu-id="e9783-1243">Problem mit dem Parametersatz bei Angabe der Parameter „-ODataQuery“ und „-ResourceId“ für „Get-AzResource“ behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-1243">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="e9783-1244">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="e9783-1244">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="e9783-1245">Behandlung des Parameters „-Custom“ in „New/Set-AzPolicyDefinition“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1245">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="e9783-1246">Tippfehler in der Dokumentation für „New-AzDeployment“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1246">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="e9783-1247">Parameter „-MailNickname“ als obligatorisch festgelegt für „New-AzADUser“</span><span class="sxs-lookup"><span data-stu-id="e9783-1247">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="e9783-1248">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="e9783-1248">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e9783-1249">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e9783-1249">Az.SignalR</span></span>
* <span data-ttu-id="e9783-1250">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-1250">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="e9783-1251">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9783-1251">Az.Sql</span></span>
* <span data-ttu-id="e9783-1252">Abhängigkeit des Speicherverwaltungsclients zur allgemeinen SDK-Implementierung konvertiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1252">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e9783-1253">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e9783-1253">Az.Storage</span></span>
* <span data-ttu-id="e9783-1254">Festlegung des „StorageAccountName“ des Speicherkontexts als tatsächlichen Namen des Speicherkontos, wenn dieser mit „SAS-Token“, „OAuth“ oder „Anonym“ erstellt wird</span><span class="sxs-lookup"><span data-stu-id="e9783-1254">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="e9783-1255">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e9783-1255">New-AzStorageContext</span></span>
* <span data-ttu-id="e9783-1256">Erstellen von SAS-Token des Blob-Momentaufnahmeobjekts mit dem Parameter „-FullUri“, Festlegung des zurückgegebenen URI als Momentaufnahme-URI</span><span class="sxs-lookup"><span data-stu-id="e9783-1256">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="e9783-1257">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="e9783-1257">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e9783-1258">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e9783-1258">Az.Websites</span></span>
* <span data-ttu-id="e9783-1259">Fehler bei der Datumsanalyse in „Get-AzDeletedWebApp“ behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-1259">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="e9783-1260">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-1260">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="e9783-1261">1.0.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="e9783-1261">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="e9783-1262">Allgemein</span><span class="sxs-lookup"><span data-stu-id="e9783-1262">General</span></span>

- <span data-ttu-id="e9783-1263">Allgemeine Verfügbarkeit des Az-Moduls</span><span class="sxs-lookup"><span data-stu-id="e9783-1263">General Availability of Az Module</span></span>
- <span data-ttu-id="e9783-1264">Onlinehilfe für jedes Modul</span><span class="sxs-lookup"><span data-stu-id="e9783-1264">Online help for each module</span></span>
- <span data-ttu-id="e9783-1265">Ausführlichere Informationen und eine Roadmap finden Sie auf der [Seite mit der Ankündigung zu Az](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="e9783-1265">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="e9783-1266">Informationen zur Migration aus AzureRM finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="e9783-1266">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="e9783-1267">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e9783-1267">Az.Accounts</span></span>
- <span data-ttu-id="e9783-1268">Geändert von Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e9783-1268">Changed from Az.Profile</span></span>
- <span data-ttu-id="e9783-1269">Feste Tabellenformate für Profil- und Kontexttypen</span><span class="sxs-lookup"><span data-stu-id="e9783-1269">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="e9783-1270">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e9783-1270">Az.ApiManagement</span></span>
- <span data-ttu-id="e9783-1271">Korrekturen für #7002</span><span class="sxs-lookup"><span data-stu-id="e9783-1271">Fixes for #7002</span></span>
- <span data-ttu-id="e9783-1272">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="e9783-1272">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="e9783-1273">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e9783-1273">Az.Batch</span></span>
- <span data-ttu-id="e9783-1274">Möglichkeit zum Anzeigen der ausgeführten Version des Azure Batch-Knoten-Agents auf den VMs eines Pools mit der neuen `NodeAgentInformation`-Eigenschaft für `PSComputeNode` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e9783-1274">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="e9783-1275">Der `Caching`-Standardwert für `PSDataDisk` lautet jetzt nicht mehr `None`, sondern `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="e9783-1275">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="e9783-1276">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="e9783-1276">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="e9783-1277">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="e9783-1277">Az.Billing</span></span>
- <span data-ttu-id="e9783-1278">Kombination von Billing-, Consumption- und UsageAggregates-Cmdlets. Ausführliche Informationen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="e9783-1278">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="e9783-1279">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="e9783-1279">Az.CognitivServices</span></span>
- <span data-ttu-id="e9783-1280">Vervollständigungen für SkuName und Typem für den Vorgang New-AzureRmCognitiveServicesAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1280">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="e9783-1281">GetSkusWithAccountParamSetName-Parametersatz aus Get-AzCognitiveServicesAccountSkus entfernt</span><span class="sxs-lookup"><span data-stu-id="e9783-1281">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="e9783-1282">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e9783-1282">Az.ContainerInstance</span></span>
- <span data-ttu-id="e9783-1283">ManagedIdentity-Unterstützung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1283">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="e9783-1284">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="e9783-1284">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="e9783-1285">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="e9783-1285">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="e9783-1286">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e9783-1286">Az.DataLakeStore</span></span>
- <span data-ttu-id="e9783-1287">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="e9783-1287">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="e9783-1288">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e9783-1288">Az.Monitor</span></span>
- <span data-ttu-id="e9783-1289">Az.Insights in Az.Monitor umbenannt und weitere weniger wichtige grundlegende Änderungen durchgeführt. Informationen hierzu finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="e9783-1289">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="e9783-1290">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e9783-1290">Az.KeyVault</span></span>
- <span data-ttu-id="e9783-1291">Veraltete PurgeDisabled-Eigenschaft aus Ausgabetypen entfernt</span><span class="sxs-lookup"><span data-stu-id="e9783-1291">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="e9783-1292">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e9783-1292">Az.MachineLearning</span></span>
- <span data-ttu-id="e9783-1293">Cmdlets des Az.MachineLearningCompute-Moduls eingebunden</span><span class="sxs-lookup"><span data-stu-id="e9783-1293">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="e9783-1294">Az.Media</span><span class="sxs-lookup"><span data-stu-id="e9783-1294">Az.Media</span></span>
- <span data-ttu-id="e9783-1295">Veralteten -Tags-Alias aus New-AzMediaService entfernt</span><span class="sxs-lookup"><span data-stu-id="e9783-1295">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="e9783-1296">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9783-1296">Az.Network</span></span>
<span data-ttu-id="e9783-1297">Unterstützung für das Konfigurieren von RewriteRuleSets im Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1297">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="e9783-1298">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="e9783-1298">New cmdlets added:</span></span>
        - <span data-ttu-id="e9783-1299">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e9783-1299">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e9783-1300">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e9783-1300">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e9783-1301">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e9783-1301">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e9783-1302">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e9783-1302">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e9783-1303">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e9783-1303">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e9783-1304">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="e9783-1304">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="e9783-1305">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="e9783-1305">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="e9783-1306">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9783-1306">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="e9783-1307">Cmdlets mit optionalem Parameter -RewriteRuleSet aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1307">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="e9783-1308">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e9783-1308">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="e9783-1309">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e9783-1309">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="e9783-1310">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e9783-1310">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="e9783-1311">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e9783-1311">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="e9783-1312">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e9783-1312">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="e9783-1313">New-AzureRmApplicationGatewayUrlPathMapConfig: KeyVault-Unterstützung mithilfe von Identität zum Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e9783-1313">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="e9783-1314">Cmdlets mit optionalem Parameter aktualisiert: -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e9783-1314">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="e9783-1315">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e9783-1315">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="e9783-1316">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e9783-1316">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="e9783-1317">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e9783-1317">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="e9783-1318">Cmdlet New-AzApplicationGateway mit optionalem Parameter -UserAssignedIdentity aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1318">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="e9783-1319">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="e9783-1319">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="e9783-1320">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e9783-1320">Az.OperationalInsights</span></span>
- <span data-ttu-id="e9783-1321">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="e9783-1321">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="e9783-1322">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e9783-1322">Az.Profile</span></span>
- <span data-ttu-id="e9783-1323">Modulnamen in Az.Accounts geändert</span><span class="sxs-lookup"><span data-stu-id="e9783-1323">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="e9783-1324">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e9783-1324">Az.RecoveryServices</span></span>
- <span data-ttu-id="e9783-1325">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="e9783-1325">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="e9783-1326">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9783-1326">Az.Resources</span></span>
- <span data-ttu-id="e9783-1327">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="e9783-1327">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="e9783-1328">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e9783-1328">Az.ServiceFabric</span></span>
- <span data-ttu-id="e9783-1329">Unterstützung für das Angeben des Zertifikats anhand des allgemeinen Namens und Fingerabdrucks</span><span class="sxs-lookup"><span data-stu-id="e9783-1329">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="e9783-1330">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="e9783-1330">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="e9783-1331">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="e9783-1331">Az.SIgnalR</span></span>
- <span data-ttu-id="e9783-1332">Allgemeine Verfügbarkeit für PowerShell-Cmdlets für SIgnalR</span><span class="sxs-lookup"><span data-stu-id="e9783-1332">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="e9783-1333">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9783-1333">Az.Sql</span></span>
- <span data-ttu-id="e9783-1334">Neue Erkennungstypen Data_Exfiltration und Unsafe_Action zu Cmdlets für Bedrohungserkennung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1334">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="e9783-1335">Dokumentationsbeispiele für Cmdlets für SQL-Überwachung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1335">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="e9783-1336">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="e9783-1336">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="e9783-1337">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e9783-1337">Az.Storage</span></span>
- <span data-ttu-id="e9783-1338">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="e9783-1338">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="e9783-1339">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e9783-1339">Az.Websites</span></span>
- <span data-ttu-id="e9783-1340">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="e9783-1340">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="e9783-1341">0.7.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="e9783-1341">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="e9783-1342">Allgemein</span><span class="sxs-lookup"><span data-stu-id="e9783-1342">General</span></span>

* <span data-ttu-id="e9783-1343">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="e9783-1343">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="e9783-1344">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9783-1344">Az.Compute</span></span>

* <span data-ttu-id="e9783-1345">Unterstützung für UltraSSD und Katalogimages in einfachen Parametersätzen für `New-AzVm(ss)`-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e9783-1345">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="e9783-1346">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e9783-1346">Az.DataLakeStore</span></span>

* <span data-ttu-id="e9783-1347">Nachgestellten Schrägstrich für die Domäne des ADLS-Kontos korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1347">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="e9783-1348">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e9783-1348">Az.FrontDoor</span></span>

* <span data-ttu-id="e9783-1349">Einige fehlerhafte Links behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-1349">Fixed some broken links</span></span>
    - <span data-ttu-id="e9783-1350">In den Artikeln zu New-AzureRmFrontDoor und Set-AzureRmFrontDoor den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorHealthProbeSettingObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="e9783-1350">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="e9783-1351">Im Artikel zu New-AzureRmFrontDoorManagedRuleObject den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorRuleGroupOverrideObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="e9783-1351">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="e9783-1352">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e9783-1352">Az.RecoveryServices</span></span>

* <span data-ttu-id="e9783-1353">Clientseitige Validierungen für Wiederherstellungsvorgänge von Azure-Dateifreigaben hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e9783-1353">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="e9783-1354">storageAccountName und storageAccountResourceGroupName für AFS-Wiederherstellung optional gemacht.</span><span class="sxs-lookup"><span data-stu-id="e9783-1354">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="e9783-1355">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9783-1355">Az.Resources</span></span>

* <span data-ttu-id="e9783-1356">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="e9783-1356">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="e9783-1357">Get-AzureRmRoleAssignment für die Verwendung des Abonnementbereichs aktualisiert, wenn dieser beim Anfordern von klassischen Administratoren angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e9783-1357">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="e9783-1358">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9783-1358">Az.Sql</span></span>

* <span data-ttu-id="e9783-1359">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="e9783-1359">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="e9783-1360">Problem mit der Verwendung von Get-AzureRmSqlDatabaseVulnerabilityAssessment mit .NET Core behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-1360">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="e9783-1361">Dokumentation mit Hilfemeldungen zu Cmdlets für die SQL-Überwachung geändert.</span><span class="sxs-lookup"><span data-stu-id="e9783-1361">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="e9783-1362">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e9783-1362">Az.Storage</span></span>

* <span data-ttu-id="e9783-1363">-EnableHierarchicalNamespace zu New-AzureRmStorageAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1363">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="e9783-1364">Problem behoben, bei dem für das Copy File-Cmdlet am Ziel kein Quellkontext wiederverwendet werden kann, wenn -DestContext nicht eingegeben wird</span><span class="sxs-lookup"><span data-stu-id="e9783-1364">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="e9783-1365">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e9783-1365">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="e9783-1366">Unterstützung der Konfiguration von statischen Websites</span><span class="sxs-lookup"><span data-stu-id="e9783-1366">Support Static Website configuration</span></span>
    - <span data-ttu-id="e9783-1367">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e9783-1367">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="e9783-1368">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e9783-1368">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="e9783-1369">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e9783-1369">Az.Websites</span></span>

* <span data-ttu-id="e9783-1370">Set-AzureRmWebApp und Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e9783-1370">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="e9783-1371">Neuen Parameter (-AzureStoragePath) zum Angeben von Azure Storage-Pfaden hinzugefügt, die in Windows- und Linux-Container-Apps bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e9783-1371">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="e9783-1372">Verwenden Sie die Ausgabe des neuen Cmdlets New-AzureRmWebAppAzureStoragePath als Parameter zum Festlegen der Azure Storage-Pfade.</span><span class="sxs-lookup"><span data-stu-id="e9783-1372">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="e9783-1373">0.6.1 – November 2018</span><span class="sxs-lookup"><span data-stu-id="e9783-1373">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="e9783-1374">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e9783-1374">Az.ApiManagement</span></span>
* <span data-ttu-id="e9783-1375">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1375">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="e9783-1376">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e9783-1376">Az.Automation</span></span>
* <span data-ttu-id="e9783-1377">Swagger-basierte Azure Automation-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="e9783-1377">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="e9783-1378">Cmdlets zur Updateverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1378">Added Update Management cmdlets</span></span>
* <span data-ttu-id="e9783-1379">Cmdlets zur Quellcodeverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1379">Added Source Control cmdlets</span></span>
* <span data-ttu-id="e9783-1380">Cmdlet „Remove-AzureRmAutomationHybridWorkerGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1380">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="e9783-1381">DSC-Befehl für die Knotenregistrierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1381">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="e9783-1382">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9783-1382">Az.Compute</span></span>
* <span data-ttu-id="e9783-1383">Identitätsproblem für SystemAssigned-Identität korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1383">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="e9783-1384">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1384">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="e9783-1385">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e9783-1385">Az.ContainerInstance</span></span>
* <span data-ttu-id="e9783-1386">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1386">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="e9783-1387">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="e9783-1387">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="e9783-1388">Beschreibung der Beispiele für Marketplace-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1388">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="e9783-1389">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9783-1389">Az.Network</span></span>
* <span data-ttu-id="e9783-1390">Folgende Cmdlets hinzugefügt: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="e9783-1390">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="e9783-1391">ICMP wieder unterstützten AzureFirewall-Netzwerkprotokollen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1391">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="e9783-1392">Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert und Überprüfung für Ziel-ID, Adresse und Port hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1392">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="e9783-1393">Probleme mit Arbeitsspeicherauslastung in der VirtualNetwork-Zuordnung behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-1393">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="e9783-1394">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="e9783-1394">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="e9783-1395">Problem beim Ändern der Richtlinie für eine geschützte Dateifreigabe behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-1395">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="e9783-1396">Richtlinienzeitzone in Großschreibung geändert</span><span class="sxs-lookup"><span data-stu-id="e9783-1396">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="e9783-1397">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="e9783-1397">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="e9783-1398">Korrigiertes Beispiel in „New-AzureRmRecoveryServicesAsrProtectableItem“</span><span class="sxs-lookup"><span data-stu-id="e9783-1398">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="e9783-1399">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1399">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="e9783-1400">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="e9783-1400">Az.Relay</span></span>
* <span data-ttu-id="e9783-1401">Optionaler Parameter „-KeyValue“ zu Cmdlet „New-AzureRmRelayKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht</span><span class="sxs-lookup"><span data-stu-id="e9783-1401">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="e9783-1402">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9783-1402">Az.Resources</span></span>
* <span data-ttu-id="e9783-1403">Hilfedokumentation für ressourcenidentitätsbezogene Parameter in `New-AzureRmPolicyAssignment` und `Set-AzureRmPolicyAssignment` aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1403">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="e9783-1404">Beispiel für „New-AzureRmPolicyDefinition“ hinzugefügt, das „-Metadata“ nutzt</span><span class="sxs-lookup"><span data-stu-id="e9783-1404">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="e9783-1405">Korrektur, um Beibehaltung von Groß-/Kleinschreibung in Tagschlüsseln in „NetStandard“ zu ermöglichen: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="e9783-1405">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="e9783-1406">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e9783-1406">Az.ServiceFabric</span></span>
* <span data-ttu-id="e9783-1407">Benachrichtigung über veraltete Elemente für anstehende wichtige Änderungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1407">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="e9783-1408">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9783-1408">Az.Sql</span></span>
* <span data-ttu-id="e9783-1409">Neue Cmdlets für CRUD-Vorgänge in verwalteten Azure SQL-Datenbank-Instanzen und verwalteten Azure SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1409">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="e9783-1410">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e9783-1410">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e9783-1411">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e9783-1411">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e9783-1412">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e9783-1412">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e9783-1413">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e9783-1413">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e9783-1414">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e9783-1414">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e9783-1415">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e9783-1415">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e9783-1416">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e9783-1416">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e9783-1417">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e9783-1417">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="e9783-1418">Erweiterte Verwaltung von Überwachungsrichtlinien auf einem Server oder in einer Datenbank aktiviert</span><span class="sxs-lookup"><span data-stu-id="e9783-1418">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="e9783-1419">Neuer Parameter (PredicateExpression) hinzugefügt, um die Filterung von Überwachungsprotokollen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="e9783-1419">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="e9783-1420">Cmdlets wurden angepasst, sodass sie SQL-Clients anstelle von Legacyclients verwenden.</span><span class="sxs-lookup"><span data-stu-id="e9783-1420">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="e9783-1421">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="e9783-1421">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="e9783-1422">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="e9783-1422">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="e9783-1423">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="e9783-1423">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="e9783-1424">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="e9783-1424">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="e9783-1425">Problem bei Verwendung von „Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings“ mit festgelegtem Parameter für den Speicherkontonamen behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-1425">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="e9783-1426">0.5.0 – November 2018</span><span class="sxs-lookup"><span data-stu-id="e9783-1426">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="e9783-1427">Allgemein</span><span class="sxs-lookup"><span data-stu-id="e9783-1427">General</span></span>
* <span data-ttu-id="e9783-1428">Ressourcenvervollständigungen für viele Kern-Cmdlets hinzugefügt (diese ermöglichen das Durchlaufen von vorhandenen Ressourcennamen per TAB-TASTE, wenn Cmdlets interaktiv aufgerufen werden)</span><span class="sxs-lookup"><span data-stu-id="e9783-1428">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="e9783-1429">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e9783-1429">Az.Profile</span></span>
* <span data-ttu-id="e9783-1430">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="e9783-1430">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="e9783-1431">Parameter „TenantId“ im Cmdlet „Connect-AzAccount“ in „Tenant“ umbenannt und Alias für „TenantId“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1431">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="e9783-1432">Beschreibung von „TenantId“ für „Connect-AzAccount“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1432">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="e9783-1433">Fehlermeldung für fehlgeschlagene Anmeldung bei Angabe der Mandantendomäne korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1433">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="e9783-1434">Problem in Bezug auf Kontextnamenskonflikt für Konten ohne Abonnements im Mandanten behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-1434">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="e9783-1435">Problem mit DataLake-Endpunkten bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-1435">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="e9783-1436">Problem behoben, das zur Auslösung von „Disconnect-AzAccount“ führte, wenn keine Verbindung bestand</span><span class="sxs-lookup"><span data-stu-id="e9783-1436">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="e9783-1437">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e9783-1437">Az.CognitiveServices</span></span>
* <span data-ttu-id="e9783-1438">Vorgang „Get-AzCognitiveServicesAccountSkus“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1438">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9783-1439">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9783-1439">Az.Compute</span></span>
* <span data-ttu-id="e9783-1440">Cmdlets Add-AzVmssVMDataDisk und Remove-AzVmssVMDataDisk hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1440">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="e9783-1441">„Get-AzVMImage“ zeigt „AutomaticOSUpgradeProperties“ an</span><span class="sxs-lookup"><span data-stu-id="e9783-1441">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="e9783-1442">Problem behoben, aufgrund dessen die Optionswerte „SetAzVMChefExtension -BootstrapOptions“ und „-JsonAttribute“ nicht im JSON-Format festgelegt wurden</span><span class="sxs-lookup"><span data-stu-id="e9783-1442">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e9783-1443">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e9783-1443">Az.DataLakeStore</span></span>
* <span data-ttu-id="e9783-1444">Aktualisierung des DataLake-Pakets auf 1.1.10</span><span class="sxs-lookup"><span data-stu-id="e9783-1444">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="e9783-1445">Standardmäßige Parallelität zu Multithreadvorgängen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1445">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="e9783-1446">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="e9783-1446">Az.Insights</span></span>
* <span data-ttu-id="e9783-1447">Problem Nr. 7267 behoben (Bereich für automatische Skalierung)</span><span class="sxs-lookup"><span data-stu-id="e9783-1447">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="e9783-1448">Probleme beim Erstellen einer neuen Regel für die automatische Skalierung, aufgrund derer die aufgelisteten Parameter nicht richtig festgelegt wurden (Es wurde stets der Standardwert festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="e9783-1448">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="e9783-1449">Problem Nr. 7513 behoben [Insights] „Set-AzDiagnosticSetting“ erfordert die explizite Angabe von Kategorien während der Erstellung der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="e9783-1449">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="e9783-1450">Nun erfordert das Cmdlet nicht die explizite Angabe der Kategorien, die während der Erstellung aktiviert werden sollen. Das bedeutet, es funktioniert wie dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="e9783-1450">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e9783-1451">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9783-1451">Az.Network</span></span>
* <span data-ttu-id="e9783-1452">„PeeringType“ wurde geändert und ist nun ein erforderlicher Parameter für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="e9783-1452">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="e9783-1453">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="e9783-1453">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="e9783-1454">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="e9783-1454">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="e9783-1455">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e9783-1455">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="e9783-1456">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="e9783-1456">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="e9783-1457">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="e9783-1457">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="e9783-1458">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e9783-1458">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e9783-1459">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e9783-1459">Az.PolicyInsights</span></span>
* <span data-ttu-id="e9783-1460">Cmdlets für Richtlinienwartung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1460">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="e9783-1461">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9783-1461">Az.Resources</span></span>
* <span data-ttu-id="e9783-1462">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="e9783-1462">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="e9783-1463">Zulassen der Auflistung von Ressourcen mithilfe des Parameters „-ResourceId“ für „Get-AzResource“</span><span class="sxs-lookup"><span data-stu-id="e9783-1463">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e9783-1464">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e9783-1464">Az.ServiceBus</span></span>
* <span data-ttu-id="e9783-1465">Schreibgeschützte Eigenschaft „MigrationState“ zu „PSServiceBusMigrationConfigurationAttributes“ hinzugefügt, was das Ermitteln des Migrationsstatus ermöglicht</span><span class="sxs-lookup"><span data-stu-id="e9783-1465">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e9783-1466">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e9783-1466">Az.ServiceFabric</span></span>
* <span data-ttu-id="e9783-1467">Hinzufügen des Zertifikats zu Linux VMSS korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1467">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="e9783-1468">„Add-AzServiceFabricClusterCertificate“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="e9783-1468">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="e9783-1469">Verwenden des richtigen Fingerabdrucks aus dem neuen Zertifikat (Azure/service-fabric-issues#932)</span><span class="sxs-lookup"><span data-stu-id="e9783-1469">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="e9783-1470">Richtige Anzeige von Ausnahmen (Azure/service-fabric-issues#1054)</span><span class="sxs-lookup"><span data-stu-id="e9783-1470">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="e9783-1471">„Update-AzServiceFabricDurability“ korrigiert, um die Clusterkonfiguration zu aktualisieren, bevor der VMSS-Vorgang „CreateOrUpdate“ gestartet wird</span><span class="sxs-lookup"><span data-stu-id="e9783-1471">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="e9783-1472">0.4.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="e9783-1472">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="e9783-1473">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e9783-1473">Az.Profile</span></span>
* <span data-ttu-id="e9783-1474">Problem mit „Get-AzSubscription“ in Cloud Shell behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-1474">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="e9783-1475">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="e9783-1475">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9783-1476">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9783-1476">Az.Compute</span></span>
* <span data-ttu-id="e9783-1477">Neue Größen zur Whitelist von VM-Größen hinzugefügt, für die bei Verwendung des einfachen Parametersatzes für „New-AzVm“ der beschleunigte Netzwerkbetrieb aktiviert wird</span><span class="sxs-lookup"><span data-stu-id="e9783-1477">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="e9783-1478">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e9783-1478">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e9783-1479">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e9783-1479">Az.DataLakeStore</span></span>
* <span data-ttu-id="e9783-1480">Unterstützung für VNET-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1480">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="e9783-1481">Get-AzDataLakeStoreVirtualNetworkRule: Dient zum Abrufen oder Auflisten der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="e9783-1481">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="e9783-1482">Add-AzDataLakeStoreVirtualNetworkRule: Fügt dem angegebenen Data Lake Store-Konto eine Regel für das virtuelle Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="e9783-1482">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e9783-1483">Set-AzDataLakeStoreVirtualNetworkRule: Ändert die angegebene Regel für das virtuelle Netzwerk in das angegebene Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="e9783-1483">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e9783-1484">Remove-AzDataLakeStoreVirtualNetworkRule: Dient zum Löschen der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="e9783-1484">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e9783-1485">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9783-1485">Az.Network</span></span>
* <span data-ttu-id="e9783-1486">Cmdlet „Test-AzNetworkWatcherConnectivity“ aktualisiert, Protokollwert wird jetzt an Back-End übergeben.</span><span class="sxs-lookup"><span data-stu-id="e9783-1486">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="e9783-1487">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e9783-1487">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e9783-1488">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9783-1488">Az.Resources</span></span>
* <span data-ttu-id="e9783-1489">Problem behoben, aufgrund dessen „Get-AzRoleDefinition“ eine unverständliche Ausnahme auslöst (wenn das Standardprofil kein Abonnement enthält und kein Bereich festgelegt ist), indem im Szenario eine aussagekräftige Ausnahme hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="e9783-1489">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="e9783-1490">Außerdem wurde der Standardparametersatz auf „RoleDefinitionNameParameterSet“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e9783-1490">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="e9783-1491">0.3.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="e9783-1491">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="e9783-1492">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="e9783-1492">Azure.Storage</span></span>
* <span data-ttu-id="e9783-1493">Fehler beim Kopieren von Blobs/Dateien behoben, aufgrund dessen bei einem Metadatenproblem des Ziels keine Metadaten kopiert wurden</span><span class="sxs-lookup"><span data-stu-id="e9783-1493">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="e9783-1494">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e9783-1494">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="e9783-1495">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e9783-1495">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="e9783-1496">Der Abruf der Speicherressourcennutzung eines bestimmten Standorts wird jetzt unterstützt, und das Hinzufügen einer Warnmeldung für den Abruf der globalen Speicherressourcennutzung ist überflüssig.</span><span class="sxs-lookup"><span data-stu-id="e9783-1496">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="e9783-1497">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="e9783-1497">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="e9783-1498">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e9783-1498">Az.CognitiveServices</span></span>
* <span data-ttu-id="e9783-1499">„Get-AzCognitiveServicesAccountSkus“ wird ohne vorhandenes Konto unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e9783-1499">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e9783-1500">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e9783-1500">Az.Compute</span></span>
* <span data-ttu-id="e9783-1501">Korrektur von „Get-AzVM -ResourceGroupName <rg>“, sodass ggf. mehr als 50 Ergebnisse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="e9783-1501">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="e9783-1502">Der Cmdlet-Hilfe zu „New-AzVmss“ wurde ein Beispiel für „SimpleParameterSet“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e9783-1502">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="e9783-1503">Tippfehler in der Azure Disk Encryption-Statusmeldung behoben</span><span class="sxs-lookup"><span data-stu-id="e9783-1503">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="e9783-1504">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e9783-1504">Az.DataFactoryV2</span></span>
* <span data-ttu-id="e9783-1505">Die Version des ADF .Net-SDK wurde auf 2.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="e9783-1505">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e9783-1506">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e9783-1506">Az.Network</span></span>
* <span data-ttu-id="e9783-1507">NetworkProfile-Funktionalität wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e9783-1507">Added NetworkProfile functionality.</span></span> <span data-ttu-id="e9783-1508">Neue Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1508">new cmdlets added</span></span>
    - <span data-ttu-id="e9783-1509">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e9783-1509">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="e9783-1510">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e9783-1510">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="e9783-1511">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e9783-1511">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="e9783-1512">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e9783-1512">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="e9783-1513">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="e9783-1513">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="e9783-1514">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="e9783-1514">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="e9783-1515">Dienstzuordnungslink in Subnetzmodell hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1515">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="e9783-1516">Cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1516">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="e9783-1517">Cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1517">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e9783-1518">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e9783-1518">Az.RedisCache</span></span>
* <span data-ttu-id="e9783-1519">Künftig sind beliebige Zeichenfolgen als Größenparameter zulässig.</span><span class="sxs-lookup"><span data-stu-id="e9783-1519">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="e9783-1520">P5 in Popup „PSArgumentCompleter“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1520">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="e9783-1521">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e9783-1521">Az.Resources</span></span>
* <span data-ttu-id="e9783-1522">Fehlender Parameter „-Mode“ zu „Set-AzPolicyDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="e9783-1522">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="e9783-1523">Cmdlet-Fehler bei „Get-AzProviderOperation“ für Vorgänge mit Ursprung behoben, der den Benutzer enthält</span><span class="sxs-lookup"><span data-stu-id="e9783-1523">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="e9783-1524">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e9783-1524">Az.Sql</span></span>
* <span data-ttu-id="e9783-1525">Problem behoben, aufgrund dessen einige Sicherungs-Cmdlets das aktuelle Azure-Abonnements nicht erkannt haben</span><span class="sxs-lookup"><span data-stu-id="e9783-1525">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e9783-1526">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e9783-1526">Az.Websites</span></span>
* <span data-ttu-id="e9783-1527">Neues Cmdlet „Get-AzWebAppContainerContinuousDeploymentUrl“ zum Abrufen der Webhook-URL von Continuous Deployment für Container</span><span class="sxs-lookup"><span data-stu-id="e9783-1527">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="e9783-1528">Neue Cmdlets „New-AzWebAppContainerPSSession“ und „Enter-WebAppContainerPSSession“ zum Initiieren einer PowerShell-Remotesitzung in einer Windows-Container-App</span><span class="sxs-lookup"><span data-stu-id="e9783-1528">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="e9783-1529">0.2.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="e9783-1529">0.2.0 - September 2018</span></span>
 <span data-ttu-id="e9783-1530">Erstrelease</span><span class="sxs-lookup"><span data-stu-id="e9783-1530">Initial Release</span></span>
