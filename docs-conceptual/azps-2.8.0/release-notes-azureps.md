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
ms.sourcegitcommit: f9445d1525eac8c165637e1a80fbc92b1ab005c2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/16/2019
ms.locfileid: "75035760"
---
## <a name="280---october-2019"></a><span data-ttu-id="2fb44-103">2.8.0: Oktober 2019</span><span class="sxs-lookup"><span data-stu-id="2fb44-103">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="2fb44-104">Allgemein</span><span class="sxs-lookup"><span data-stu-id="2fb44-104">General</span></span>
* <span data-ttu-id="2fb44-105">Az.HealthcareApis-Release 1.0.0</span><span class="sxs-lookup"><span data-stu-id="2fb44-105">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2fb44-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2fb44-106">Az.Accounts</span></span>
* <span data-ttu-id="2fb44-107">Telemetriedaten und URL-Umschreibung für generierte Module aktualisiert, Windows-Komponententests korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-107">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2fb44-108">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2fb44-108">Az.ApiManagement</span></span>
* <span data-ttu-id="2fb44-109">**Set-AzApiManagementApi**: Unterstützung für die Aktualisierung der API in „ApiVersionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-109">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="2fb44-110">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="2fb44-110">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2fb44-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2fb44-111">Az.Automation</span></span>
* <span data-ttu-id="2fb44-112">Cmdlet „New-AzureAutomationSoftwareUpdateConfiguration“ für den Parameter für die Linux-Neustarteinstellung korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-112">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="2fb44-113">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2fb44-113">Az.Batch</span></span>
* <span data-ttu-id="2fb44-114">**Get-AzBatchNodeAgentSku** ist veraltet und wird in Version 2.0.0 durch **Get-AzBatchSupportImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="2fb44-114">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2fb44-115">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2fb44-115">Az.Compute</span></span>
* <span data-ttu-id="2fb44-116">Parameter „Priority“, „EvictionPolicy“ und „MaxPrice“ zu den Cmdlets „“New-AzVM“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-116">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="2fb44-117">Warnmeldung und Hilfedokument für die Cmdlets „Add-AzVMAdditionalUnattendContent“ und „Add-AzVMSshPublicKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-117">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="2fb44-118">Ausnahme „-skipVmBackup“ Linux-VMs mit verwalteten Datenträgern für „Set-AzVMDiskEncryptionExtension“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-118">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="2fb44-119">Fehler beim Aktualisieren von Verschlüsselungseinstellungen in „Set-AzVMDiskEncryptionExtension“ korrigiert (zweistufiges Szenario)</span><span class="sxs-lookup"><span data-stu-id="2fb44-119">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2fb44-120">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2fb44-120">Az.DataFactory</span></span>
* <span data-ttu-id="2fb44-121">CRUD-Befehle für ADF V2-Datenfluss hinzugefügt: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow und Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="2fb44-121">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="2fb44-122">Aktionsbefehle für Debugsitzung für ADF V2-Datenfluss hinzugefügt: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand und Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="2fb44-122">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="2fb44-123">Version des ADF .NET SDK auf 4.2.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-123">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2fb44-124">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2fb44-124">Az.DataLakeStore</span></span>
* <span data-ttu-id="2fb44-125">Kontoüberprüfung korrigiert, sodass Konten mit „-“ ohne Domäne übermittelt werden können</span><span class="sxs-lookup"><span data-stu-id="2fb44-125">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="2fb44-126">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="2fb44-126">Az.HealthcareApis</span></span>
* <span data-ttu-id="2fb44-127">PowerShell-Version auf 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-127">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="2fb44-128">SDK-Version auf 1.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-128">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="2fb44-129">Aktualisierung in Tests, um auf neue SDK-Version zu verweisen</span><span class="sxs-lookup"><span data-stu-id="2fb44-129">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="2fb44-130">Ausgabestruktur von geschachtelt in vereinfacht geändert</span><span class="sxs-lookup"><span data-stu-id="2fb44-130">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2fb44-131">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2fb44-131">Az.IotHub</span></span>
* <span data-ttu-id="2fb44-132">Neue Routingquelle hinzugefügt: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="2fb44-132">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="2fb44-133">Kleinere Fehlerbehebung: „Get-AzIothub“ gibt „subscriptionId“ nicht zurück.</span><span class="sxs-lookup"><span data-stu-id="2fb44-133">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="2fb44-134">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2fb44-134">Az.Monitor</span></span>
* <span data-ttu-id="2fb44-135">Neue Aktionsgruppenempfänger für „New-AzActionGroupReceiver“ hinzugefügt:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="2fb44-135">New action group receivers added for New-AzActionGroupReceiver:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="2fb44-136">Verwendung des allgemeinen Warnungsschemas für Empfänger aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2fb44-136">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="2fb44-137">Dies gilt nicht für SMS, Azure App-Pushbenachrichtigungen, ITSM und Sprachempfänger.</span><span class="sxs-lookup"><span data-stu-id="2fb44-137">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="2fb44-138">Webhooks unterstützen nun die Azure Active Directory-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="2fb44-138">Webhooks now supports Azure active directory authentication.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2fb44-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2fb44-139">Az.Network</span></span>
* <span data-ttu-id="2fb44-140">Neues Cmdlet „Get-AzAvailableServiceAlias“ hinzugefügt, das zum Abrufen der Aliase aufgerufen werden kann, die für Dienstendpunktrichtlinien verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="2fb44-140">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="2fb44-141">Unterstützung für das Hinzufügen von Verbindungen von Datenverkehrsselektoren zu Virtual Network-Gatewayverbindungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-141">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="2fb44-142">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="2fb44-142">New cmdlets added:</span></span>
        - <span data-ttu-id="2fb44-143">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="2fb44-143">New-AzIpsecTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="2fb44-144">Cmdlets mit optionalem Parameter „-TrafficSelectorPolicies“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-144">Cmdlets updated with optional parameter -TrafficSelectorPolicies</span></span>
        - <span data-ttu-id="2fb44-145">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2fb44-145">New-AzVirtualNetworkGatewayConnection</span></span>
        - <span data-ttu-id="2fb44-146">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2fb44-146">Set-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="2fb44-147">Unterstützung für ESP- und AH-Protokolle in Konfigurationen von Netzwerksicherheitsregeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-147">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="2fb44-148">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="2fb44-148">Updated cmdlets:</span></span>
        - <span data-ttu-id="2fb44-149">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2fb44-149">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="2fb44-150">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2fb44-150">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="2fb44-151">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2fb44-151">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="2fb44-152">Verbesserte Behandlung von Ausnahmen in Cortex-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2fb44-152">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="2fb44-153">Neue Generationen und SKUs für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="2fb44-153">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="2fb44-154">Einführung neuer Generationen für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="2fb44-154">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="2fb44-155">Einführung neuer SKUs mit höherem Durchsatz für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="2fb44-155">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="2fb44-156">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2fb44-156">Az.RedisCache</span></span>
* <span data-ttu-id="2fb44-157">Referenzdokumentation zu „Set-AzRedisCache“ aktualisiert, um fehlende Werte für den Parameter „-Size“ aufzunehmen</span><span class="sxs-lookup"><span data-stu-id="2fb44-157">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="2fb44-158">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2fb44-158">Az.Sql</span></span>
* <span data-ttu-id="2fb44-159">Unterstützung für das Festlegen des Active Directory-Administrators für verwaltete Instanz hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-159">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2fb44-160">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2fb44-160">Az.Storage</span></span>
* <span data-ttu-id="2fb44-161">Storage-Clientbibliothek auf 11.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-161">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="2fb44-162">Auflisten von Containern mit der API der Verwaltungsebene, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="2fb44-162">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="2fb44-163">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2fb44-163">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="2fb44-164">Auflisten von Storage-Konten aus Abonnements, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="2fb44-164">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="2fb44-165">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2fb44-165">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="2fb44-166">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="2fb44-166">Az.StorageSync</span></span>
* <span data-ttu-id="2fb44-167">Problem 9810 in „Reset-AzStorageSyncServerCertificate“ behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-167">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2fb44-168">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2fb44-168">Az.Websites</span></span>
* <span data-ttu-id="2fb44-169">Fehler beim Aktualisieren von ASP einer App mit „Set-AzWebApp“</span><span class="sxs-lookup"><span data-stu-id="2fb44-169">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="2fb44-170">2.7.0: September 2019</span><span class="sxs-lookup"><span data-stu-id="2fb44-170">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="2fb44-171">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2fb44-171">Az.ApiManagement</span></span>
* <span data-ttu-id="2fb44-172">Beschreibung des Parameters „-Format“ in der Referenzdokumentation für „Set-AzApiManagementPolicy“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-172">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="2fb44-173">Verweise des veralteten Cmdlets „Update-AzApiManagementDeployment“ aus Referenzdokumentation entfernt.</span><span class="sxs-lookup"><span data-stu-id="2fb44-173">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="2fb44-174">Verwenden Sie stattdessen „Set-AzApiManagement“.</span><span class="sxs-lookup"><span data-stu-id="2fb44-174">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2fb44-175">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2fb44-175">Az.Automation</span></span>
* <span data-ttu-id="2fb44-176">Tippfehler im Beispiel in der Referenzdokumentation für „Register-AzAutomationDscNode“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-176">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="2fb44-177">Erläuterung zur Betriebssystemeinschränkung zu „Register-AzAutomationDSCNode“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-177">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="2fb44-178">Nullverweisausnahme des Cmdlets „Start-AzAutomationRunbook“ für die Option „-Wait“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="2fb44-178">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2fb44-179">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2fb44-179">Az.Compute</span></span>
* <span data-ttu-id="2fb44-180">Parameter „UploadSizeInBytes“ zu „New-AzDiskConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-180">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="2fb44-181">Inkrementeller Parameter zu „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-181">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="2fb44-182">Feature für VM mit niedriger Priorität hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="2fb44-182">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="2fb44-183">Parameter „MaxPrice“, „EvictionPolicy“ und „Priority“ zu New-AzVMConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-183">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="2fb44-184">Parameter „MaxPrice“ zu den Cmdlets „New-AzVmssConfig“, „Update-AzVM“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-184">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="2fb44-185">Fehlerbehebung für VM-Verweis für das Cmdlet „Get-AzAvailabilitySet“, wenn alle Verfügbarkeitsgruppen im Abonnement aufgelistet werden</span><span class="sxs-lookup"><span data-stu-id="2fb44-185">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="2fb44-186">Nullausnahme für „Get-AzRemoteDesktopFile“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-186">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="2fb44-187">VHD-Suchmethode für Position relativ zum Ende korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-187">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="2fb44-188">Problem mit UltraSSD für „New-AzVM“ und „Update-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-188">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2fb44-189">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2fb44-189">Az.DataFactory</span></span>
* <span data-ttu-id="2fb44-190">Drei neue Befehle für ADF V2 hinzugefügt: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription und Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="2fb44-190">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="2fb44-191">Version des ADF .NET SDK auf 4.1.3 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-191">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2fb44-192">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2fb44-192">Az.HDInsight</span></span>
* <span data-ttu-id="2fb44-193">Hinweis auf Breaking Changes hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-193">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2fb44-194">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2fb44-194">Az.IotHub</span></span>
* <span data-ttu-id="2fb44-195">Unterstützung zum Aufrufen eines Failovers für einen IoT-Hub zur geografisch gekoppelten Notfallwiederherstellungsregion hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-195">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="2fb44-196">Unterstützung zum Verwalten der Nachrichtenanreicherung für einen IoT-Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-196">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="2fb44-197">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="2fb44-197">New cmdlets are:</span></span>
    - <span data-ttu-id="2fb44-198">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="2fb44-198">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="2fb44-199">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="2fb44-199">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="2fb44-200">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="2fb44-200">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="2fb44-201">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="2fb44-201">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2fb44-202">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2fb44-202">Az.Monitor</span></span>
* <span data-ttu-id="2fb44-203">Verweis auf das aktuelle Monitor SDK, d. h. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="2fb44-203">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="2fb44-204">Geringfügige Änderungen an den Metrik-Cmdlets vorgenommen, d. h. die Einheitenenumeration unterstützt verschiedene neue Werte.</span><span class="sxs-lookup"><span data-stu-id="2fb44-204">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="2fb44-205">Dabei handelt es sich um schreibgeschützte Cmdlets, sodass keine Änderungen an der Eingabe der Cmdlets erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="2fb44-205">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="2fb44-206">Die API-Version der **ActionGroups**-Anforderungen lautet jetzt **2019-06-01** (zuvor **2018-03-01**).</span><span class="sxs-lookup"><span data-stu-id="2fb44-206">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="2fb44-207">Die Szenariotests wurden aktualisiert, um diese Änderung zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="2fb44-207">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="2fb44-208">Die Konstruktoren für die Klassen **EmailReceiver** und **WebhookReceiver** haben ein neues obligatorisches Argument hinzugefügt, d. h. einen booleschen Wert namens **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="2fb44-208">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="2fb44-209">Derzeit ist der Wert auf **false** festgelegt, damit sich dieser Breaking Change nicht auf die Cmdlets auswirkt.</span><span class="sxs-lookup"><span data-stu-id="2fb44-209">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="2fb44-210">**HINWEIS:** Dies ist eine vorübergehende Änderung, die vom Team für Warnungen validiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="2fb44-210">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="2fb44-211">Die Reihenfolge der Argumente für den Konstruktor der Klasse **Source** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="2fb44-211">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="2fb44-212">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="2fb44-212">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="2fb44-213">Die Reihenfolge der Argumente für den Konstruktor der Klasse **AlertingAction** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="2fb44-213">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="2fb44-214">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="2fb44-214">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="2fb44-215">Unterstützung von Kriterien für dynamische Schwellwerte für Metrikwarnung v2</span><span class="sxs-lookup"><span data-stu-id="2fb44-215">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="2fb44-216">New-AzMetricAlertRuleV2Criteria: Erstellt nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="2fb44-216">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="2fb44-217">Add-AzMetricAlertRuleV2: Akzeptiert nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="2fb44-217">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="2fb44-218">Verbesserungen an den Cmdlets für geplante Abfrageregeln (Scheduled Query Rule, SQR)</span><span class="sxs-lookup"><span data-stu-id="2fb44-218">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="2fb44-219">Cmdlets akzeptieren den Parameter „Location“ in zwei Formaten: entweder den Standort (z. B. „eastus“) oder den Anzeigenamen des Standorts (z. B. „USA, Osten“)</span><span class="sxs-lookup"><span data-stu-id="2fb44-219">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="2fb44-220">Parameter „Enabled“ in Hilfedateien ordnungsgemäß dargestellt</span><span class="sxs-lookup"><span data-stu-id="2fb44-220">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="2fb44-221">Beispiele für optionalen Parameter „ActionGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-221">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="2fb44-222">Hilfedateien insgesamt verbessert</span><span class="sxs-lookup"><span data-stu-id="2fb44-222">Overall improved help files</span></span>
* <span data-ttu-id="2fb44-223">Fehler beim Bestimmen des Bereichstyps für „Set-AzActionRule“ behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-223">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2fb44-224">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2fb44-224">Az.Network</span></span>
* <span data-ttu-id="2fb44-225">Fehlerhaftes Beispiel in der Referenzdokumentation zu „New-AzApplicationGateway“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-225">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="2fb44-226">Hinweis in der Referenzdokumentation zu „Get-AzNetworkWatcherPacketCapture“ zum Abrufen aller Eigenschaften für eine Paketerfassung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-226">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="2fb44-227">Beispiel in der Referenzdokumentation zu „Test-AzNetworkWatcherIPFlow“ korrigiert, um die Netzwerkadapter ordnungsgemäß aufzulisten</span><span class="sxs-lookup"><span data-stu-id="2fb44-227">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="2fb44-228">Cloudausnahmeanalyse verbessert, um ggf. zusätzliche Details anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="2fb44-228">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="2fb44-229">Cloudausnahmeanalyse verbessert, um zusätzlichen Typ der SDK-Ausnahme zu verarbeiten</span><span class="sxs-lookup"><span data-stu-id="2fb44-229">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="2fb44-230">Falsche Zuordnung der Sicherheitsregelmodelle korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-230">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="2fb44-231">Eigenschaften zur Netzwerkschnittstelle für das Feature für die private IP-Adresse hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-231">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="2fb44-232">Eigenschaft „PrivateEndpoint“ als Typ „PSResourceId“ zu „PSNetworkInterface“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-232">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="2fb44-233">Eigenschaft „PrivateLinkConnectionProperties“ als Typ „PSIpConfigurationConnectivityInformation“ zu „PSNetworkInterfaceIPConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-233">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="2fb44-234">Neue Modellklasse „PSIpConfigurationConnectivityInformation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-234">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="2fb44-235">Neues ApplicationRuleProtocolType-Element „mssql“ für Azure Firewall-Ressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-235">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="2fb44-236">Unterstützung von Mehrfachverbindungen in Virtual WAN</span><span class="sxs-lookup"><span data-stu-id="2fb44-236">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="2fb44-237">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2fb44-237">New cmdlets</span></span>
        - <span data-ttu-id="2fb44-238">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="2fb44-238">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="2fb44-239">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="2fb44-239">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="2fb44-240">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2fb44-240">Updated cmdlet:</span></span>
        - <span data-ttu-id="2fb44-241">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="2fb44-241">New-VpnSite</span></span>
        - <span data-ttu-id="2fb44-242">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="2fb44-242">Update-VpnSite</span></span>
        - <span data-ttu-id="2fb44-243">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="2fb44-243">New-VpnConnection</span></span>
        - <span data-ttu-id="2fb44-244">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="2fb44-244">Update-VpnConnection</span></span>
* <span data-ttu-id="2fb44-245">Dokumente für einige PowerShell-Beispiele korrigiert, sodass Az-Cmdlets anstelle von AzureRM-Cmdlets verwendet werden</span><span class="sxs-lookup"><span data-stu-id="2fb44-245">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2fb44-246">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2fb44-246">Az.RecoveryServices</span></span>
* <span data-ttu-id="2fb44-247">AzureVMpolicy-Objekt mit ProtectedItemsCount-Attribut aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-247">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="2fb44-248">Tests für VM-Richtlinie und Wiederherstellung des ursprünglichen Speicherkontos hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-248">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="2fb44-249">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2fb44-249">Az.Resources</span></span>
* <span data-ttu-id="2fb44-250">Fehler behoben, aufgrund dessen „New-AzRoleAssignment“ nicht ohne den Parameter „Scope“ aufgerufen werden konnte</span><span class="sxs-lookup"><span data-stu-id="2fb44-250">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2fb44-251">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2fb44-251">Az.ServiceFabric</span></span>
* <span data-ttu-id="2fb44-252">Tippfehler im Beispiel für die Referenzdokumentation „Update-AzServiceFabricReliability“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-252">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="2fb44-253">Neue Cmdlets zum Verwalten von Anwendung und Diensten hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="2fb44-253">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="2fb44-254">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="2fb44-254">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="2fb44-255">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="2fb44-255">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="2fb44-256">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="2fb44-256">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="2fb44-257">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="2fb44-257">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="2fb44-258">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="2fb44-258">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="2fb44-259">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="2fb44-259">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="2fb44-260">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="2fb44-260">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="2fb44-261">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="2fb44-261">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="2fb44-262">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="2fb44-262">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="2fb44-263">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="2fb44-263">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="2fb44-264">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="2fb44-264">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="2fb44-265">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="2fb44-265">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="2fb44-266">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="2fb44-266">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="2fb44-267">Service Fabric SDK auf Version 1.2.0 aktualisiert, die API-Version 2019-03-01 des Service Fabric-Ressourcenanbieters verwendet</span><span class="sxs-lookup"><span data-stu-id="2fb44-267">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="2fb44-268">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="2fb44-268">Az.SignalR</span></span>
* <span data-ttu-id="2fb44-269">Cmdlets „Update“, „Restart“, „CheckNameAvailability“ und „GetUsage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-269">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="2fb44-270">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2fb44-270">Az.Sql</span></span>
* <span data-ttu-id="2fb44-271">Beispiel in der Referenzdokumentation für „Get-AzSqlElasticPool“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-271">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="2fb44-272">V-Kern-Beispiel zum Erstellen eines Pools für elastische Datenbanken hinzugefügt (New-AzSqlElasticPool)</span><span class="sxs-lookup"><span data-stu-id="2fb44-272">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="2fb44-273">Überprüfung von „EmailAddresses“ sowie Validierung, dass „EmailAdmins“ nicht auf „false“ festgelegt ist, in „Set-AzSqlServerAdvancedThreatProtectionPolicy“ und „Set-AzSqlDatabaseAdvancedThreatProtectionPolicy“ entfernt, wenn „EmailAddresses“ leer ist</span><span class="sxs-lookup"><span data-stu-id="2fb44-273">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="2fb44-274">Entfernen der Einstellungen für Server-/Datenbanküberwachung aktiviert, wenn mehrere Diagnoseeinstellungen vorhanden sind, die eine Überwachungskategorie ermöglichen</span><span class="sxs-lookup"><span data-stu-id="2fb44-274">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="2fb44-275">Überprüfung von E-Mail-Adressen in mehreren Cmdlets für die SQL-Sicherheitsrisikobewertung korrigiert (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting und Update-AzSqlInstanceVulnerabilityAssessmentSetting)</span><span class="sxs-lookup"><span data-stu-id="2fb44-275">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2fb44-276">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2fb44-276">Az.Storage</span></span>
* <span data-ttu-id="2fb44-277">Beispiel in der Referenzdokumentation für „Get-AzStorageAccountKey“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-277">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="2fb44-278">Beim Upload/Download von Azure-Dateien wird das Beibehalten der SMB-Eigenschaften der Quelldateien (Dateiattribute, Zeitpunkt der Dateierstellung, letzter Schreibzugriff für die Datei) in der Zieldatei unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2fb44-278">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="2fb44-279">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2fb44-279">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="2fb44-280">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2fb44-280">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="2fb44-281">Fehler beim Hochladen von Blockblobs mit Eigenschaften/Metadaten für das für einen Container aktivierte ImmutabilityPolicy-Element behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-281">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="2fb44-282">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2fb44-282">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="2fb44-283">Unterstützung für die Verwaltung von Azure-Dateifreigaben mit der API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="2fb44-283">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="2fb44-284">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2fb44-284">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="2fb44-285">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2fb44-285">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="2fb44-286">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2fb44-286">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="2fb44-287">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2fb44-287">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2fb44-288">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2fb44-288">Az.Websites</span></span>
* <span data-ttu-id="2fb44-289">Problem behoben, aufgrund dessen Web-App-Tags beim Migrieren der App zum neuen ASP gelöscht wurden</span><span class="sxs-lookup"><span data-stu-id="2fb44-289">Fixing issue where webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="2fb44-290">„Publish-AzureWebapp“ für die Verwendung unter Linux und Windows korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-290">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="2fb44-291">Beispiel in Referenzdokumentation „Get-AzWebAppPublishingProfile“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-291">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="2fb44-292">2.6.0: August 2019</span><span class="sxs-lookup"><span data-stu-id="2fb44-292">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="2fb44-293">Allgemein</span><span class="sxs-lookup"><span data-stu-id="2fb44-293">General</span></span>
* <span data-ttu-id="2fb44-294">Verschiedene Tippfehler in zahlreichen Modulen korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-294">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2fb44-295">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2fb44-295">Az.Accounts</span></span>
* <span data-ttu-id="2fb44-296">Unterstützung der benutzerseitig zugewiesenen MSI in Azure Functions-Authentifizierung (#9479)</span><span class="sxs-lookup"><span data-stu-id="2fb44-296">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="2fb44-297">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="2fb44-297">Az.Aks</span></span>
* <span data-ttu-id="2fb44-298">Problem mit der Ausgabe für „Get-AzAks“ behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-298">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="2fb44-299">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="2fb44-299">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2fb44-300">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2fb44-300">Az.ApiManagement</span></span>
* <span data-ttu-id="2fb44-301">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="2fb44-301">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="2fb44-302">.NET-NuGet-Version aktualisiert, die keine Einschränkungen für „productId“, „apiId“, „groupId“ und „userId“ erzwingt</span><span class="sxs-lookup"><span data-stu-id="2fb44-302">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="2fb44-303">**Get-AzApiManagementProduct:** Unterstützung für das Abfragen von Produkten mithilfe der API hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-303">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="2fb44-304">**New-AzApiManagementApiRevision:** Problem behoben, aufgrund dessen „ApiRevisionDescription“ beim Erstellen einer neuen API-Revision nicht festgelegt wurde https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="2fb44-304">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="2fb44-305">Tippfehler im Modell „PsApiManagementOAuth2AuthrozationServer“ korrigiert: PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="2fb44-305">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="2fb44-306">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2fb44-306">Az.Batch</span></span>
* <span data-ttu-id="2fb44-307">Tippfehler in Hilfemeldung und Dokumentation korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="2fb44-307">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2fb44-308">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2fb44-308">Az.Cdn</span></span>
* <span data-ttu-id="2fb44-309">Tippfehler im Hilfsprogramm für die CDN-Modulkonvertierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-309">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2fb44-310">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2fb44-310">Az.Compute</span></span>
* <span data-ttu-id="2fb44-311">VmssId zum Cmdlet „New-AzVMConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-311">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="2fb44-312">Parameter „TerminateScheduledEvents“ und „TerminateScheduledEventNotBeforeTimeoutInMinutes“ zu „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-312">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="2fb44-313">HyperVGeneration-Eigenschaft zu VM-Imageobjekt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-313">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="2fb44-314">Host- und HostGroup-Features hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-314">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="2fb44-315">Neue Cmdlets:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="2fb44-315">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="2fb44-316">Parameter „HostId“ zu „New-AzVMConfig“ und „New-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-316">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="2fb44-317">Beispiel in der Dokumentation zu „Invoke-AzVMRunCommand“ zur Verwendung des richtigen Parameternamens aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-317">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="2fb44-318">Beschreibung für „-VolumeType“ in der Referenzdokumentation zu „Set-AzVMDiskEncryptionExtension“ und „Set-AzVmssDiskEncryptionExtension“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-318">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2fb44-319">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2fb44-319">Az.DataFactory</span></span>
* <span data-ttu-id="2fb44-320">Tippfehler in der Dokumentation zu „New-AzDataFactoryEncryptValue“ korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="2fb44-320">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="2fb44-321">Version des ADF .NET SDK auf 4.1.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-321">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="2fb44-322">Parameter „DataProxyIntegrationRuntimeName“, „DataProxyStagingLinkedServiceName“ und „DataProxyStagingPath“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um die Einrichtung der selbstgehosteten Integration Runtime als Proxy für die SSIS Integration Runtime zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="2fb44-322">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="2fb44-323">„PSTriggerRun“ zum Anzeigen der ausgelösten Pipelines, Meldungen und Eigenschaften und „PSActivityRun“ zum Anzeigen des Aktivitätstyps aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-323">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2fb44-324">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2fb44-324">Az.DataLakeStore</span></span>
* <span data-ttu-id="2fb44-325">Hängen von „Get-DataLakeStoreDeletedItem“ aufgrund von Fehlern oder Remoteausnahmen behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-325">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2fb44-326">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2fb44-326">Az.EventHub</span></span>
* <span data-ttu-id="2fb44-327">Behebung des Problems #9658: Tippfehler im Parameter „VirtualNteworkRule“ in „Set-AzEventHubNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="2fb44-327">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="2fb44-328">Behebung des Problems #9558: „Set-AzEventHubNamespace“ verwendet PATCH anstelle von PUT.</span><span class="sxs-lookup"><span data-stu-id="2fb44-328">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="2fb44-329">Parameter „EnableKafka“ zum Cmdlet „Set-AzEventHubNamespace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-329">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="2fb44-330">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="2fb44-330">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="2fb44-331">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="2fb44-331">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="2fb44-332">Tippfehler („Azure“ in Kleinbuchstaben) in der Dokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-332">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2fb44-333">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2fb44-333">Az.Monitor</span></span>
* <span data-ttu-id="2fb44-334">Falscher Parametername in der Hilfedokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-334">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2fb44-335">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2fb44-335">Az.Network</span></span>
* <span data-ttu-id="2fb44-336">„New-AzPrivateLinkServiceIpConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-336">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="2fb44-337">Parameter „PublicIpAddress“ ausgemustert, da er auf Serverseite nie verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="2fb44-337">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="2fb44-338">Optionaler Parameter „Primary“ hinzugefügt, der angibt, ob die aktuelle IP-Konfiguration die primäre ist oder nicht</span><span class="sxs-lookup"><span data-stu-id="2fb44-338">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="2fb44-339">Verbesserte Verarbeitung der Anforderungsfehlerausnahme aus dem SDK: Behebt das Problem, dass vorherige SDK-Ausnahmen nicht richtig behandelt wurden, was dazu führt, dass Schlüsselfehlerdetails nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2fb44-339">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="2fb44-340">Validierungslogik für Ipv6-IP-Präfix angepasst, damit auf die richtige IPv6-Präfixlänge geprüft wird</span><span class="sxs-lookup"><span data-stu-id="2fb44-340">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="2fb44-341">„Get-AzVirtualNetworkSubnetConfig“ aktualisiert: Parametersatz zum Abrufen nach Subnetzressourcen-ID hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-341">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="2fb44-342">Aktualisierte Beschreibung des Location-Parameters für „AzNetworkServiceTag“</span><span class="sxs-lookup"><span data-stu-id="2fb44-342">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2fb44-343">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2fb44-343">Az.OperationalInsights</span></span>
* <span data-ttu-id="2fb44-344">Aktualisierte Dokumentation für „New-AzOperationalInsightsLinuxSyslogDataSource“</span><span class="sxs-lookup"><span data-stu-id="2fb44-344">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="2fb44-345">Beispiel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-345">Added example</span></span>
    - <span data-ttu-id="2fb44-346">Beschreibung für den Parameter „-Name“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-346">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="2fb44-347">Beispiel für „New-AzOperationalInsightsWindowsEventDataSource“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-347">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="2fb44-348">Beschreibung des Parameters „-Name“ für „New-AzOperationalInsightsWindowsEventDataSource“ geändert</span><span class="sxs-lookup"><span data-stu-id="2fb44-348">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2fb44-349">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2fb44-349">Az.RecoveryServices</span></span>
* <span data-ttu-id="2fb44-350">„Get-AzRecoveryServicesBackupJobDetail.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-350">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="2fb44-351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2fb44-351">Az.Resources</span></span>
* <span data-ttu-id="2fb44-352">Unterstützung für die neue API-Version 2019-05-10 für Microsoft.Resource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-352">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="2fb44-353">Unterstützung für „copy.count = 0“ für Variablen, Ressourcen und Eigenschaften hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-353">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="2fb44-354">Ressourcen mit „condition = false“ oder „copy.count = 0“ werden im vollständigen Modus gelöscht.</span><span class="sxs-lookup"><span data-stu-id="2fb44-354">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="2fb44-355">Beispiel zum Hinzufügen einer Richtlinie auf Abonnementebene zur Hilfedokumentation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-355">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2fb44-356">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2fb44-356">Az.ServiceBus</span></span>
* <span data-ttu-id="2fb44-357">Behebung des Problems #9658: Tippfehler für Parameter „VirtualNetworkRule“ in „Set-AzServiceBusNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="2fb44-357">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="2fb44-358">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="2fb44-358">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="2fb44-359">Neuer Befehl „Test-AzServiceBusNameAvailability“ zum Überprüfen der Verfügbarkeit des Namens für Warteschlange und Thema hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-359">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="2fb44-360">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2fb44-360">Az.ServiceFabric</span></span>
* <span data-ttu-id="2fb44-361">Fehler bei Cmdlets zum Hinzufügen des Knotentyps korrigiert:</span><span class="sxs-lookup"><span data-stu-id="2fb44-361">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="2fb44-362">Fehler „NullReferenceException“, wenn die Ressourcengruppe andere VMSS enthielt, die nicht mit dem Service Fabric-Cluster in Zusammenhang stehen</span><span class="sxs-lookup"><span data-stu-id="2fb44-362">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="2fb44-363">Problembehebung: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="2fb44-363">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="2fb44-364">Fehler behoben, aufgrund dessen bei einem Cmdlet ein Fehler auftrat, wenn sich „virtualNetwork“ in einer anderen Ressourcengruppe befand als der Cluster</span><span class="sxs-lookup"><span data-stu-id="2fb44-364">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="2fb44-365">Problembehebung: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="2fb44-365">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="2fb44-366">Cmdlet „Add-AzServiceFabricApplicationCertificate“ ausgemustert</span><span class="sxs-lookup"><span data-stu-id="2fb44-366">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="2fb44-367">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2fb44-367">Az.Sql</span></span>
* <span data-ttu-id="2fb44-368">Dokumentation alter Überwachungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-368">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2fb44-369">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2fb44-369">Az.Storage</span></span>
* <span data-ttu-id="2fb44-370">Hilfe für „Get/Close-AzStorageFileHandle“ aktualisiert (weitere Szenarien zu Cmdlet-Beispielen hinzugefügt und Parameterbeschreibungen aktualisiert)</span><span class="sxs-lookup"><span data-stu-id="2fb44-370">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="2fb44-371">Unterstützung von „StandardBlobTier“ in Uploadblobs und Kopierblobs</span><span class="sxs-lookup"><span data-stu-id="2fb44-371">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="2fb44-372">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2fb44-372">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="2fb44-373">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2fb44-373">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="2fb44-374">Unterstützung der Aktivierungspriorität im Kopierblob</span><span class="sxs-lookup"><span data-stu-id="2fb44-374">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="2fb44-375">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2fb44-375">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2fb44-376">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2fb44-376">Az.Websites</span></span>
* <span data-ttu-id="2fb44-377">Hinzufügen von Erläuterungen zum Parameter „-AppSettings“ in „Set-AzWebApp“ und „Set-AzWebAppSlot“</span><span class="sxs-lookup"><span data-stu-id="2fb44-377">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="2fb44-378">2.5.0: Juli 2019</span><span class="sxs-lookup"><span data-stu-id="2fb44-378">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2fb44-379">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2fb44-379">Az.Accounts</span></span>
* <span data-ttu-id="2fb44-380">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="2fb44-380">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="2fb44-381">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="2fb44-381">Az.ApplicationInsights</span></span>
* <span data-ttu-id="2fb44-382">Tippfehler im Beispiel in der Dokumentation zu „Remove-AzApplicationInsightsApiKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-382">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="2fb44-383">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2fb44-383">Az.Automation</span></span>
* <span data-ttu-id="2fb44-384">Tippfehler in der Ressourcenzeichenfolge korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-384">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="2fb44-385">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2fb44-385">Az.CognitiveServices</span></span>
* <span data-ttu-id="2fb44-386">Unterstützung für NetworkRuleSet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-386">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2fb44-387">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2fb44-387">Az.Compute</span></span>
* <span data-ttu-id="2fb44-388">Fehlende Eigenschaften (ComputerName, OsName, OsVersion und HyperVGeneration) des Objekts für die VM-Instanzenansicht hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-388">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="2fb44-389">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2fb44-389">Az.ContainerRegistry</span></span>
* <span data-ttu-id="2fb44-390">Tippfehler in „Remove-AzContainerRegistryReplication“ für den Replikationsparameter korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-390">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="2fb44-391">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="2fb44-391">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2fb44-392">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2fb44-392">Az.DataFactory</span></span>
* <span data-ttu-id="2fb44-393">Version des ADF .NET SDK auf 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-393">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="2fb44-394">Tippfehler in der Dokumentation für „Get-AzDataFactoryV2PipelineRun“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-394">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2fb44-395">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2fb44-395">Az.EventHub</span></span>
* <span data-ttu-id="2fb44-396">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="2fb44-396">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="2fb44-397">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="2fb44-397">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2fb44-398">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2fb44-398">Az.KeyVault</span></span>
* <span data-ttu-id="2fb44-399">Unterstützung zum Angeben von KeySize für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-399">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2fb44-400">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2fb44-400">Az.LogicApp</span></span>
* <span data-ttu-id="2fb44-401">Korrektur für „Get-AzIntegrationAccountMap“ zum Auflisten aller Zuordnungstypen</span><span class="sxs-lookup"><span data-stu-id="2fb44-401">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="2fb44-402">Neuer MapType-Parameter für Filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-402">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="2fb44-403">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="2fb44-403">Az.ManagedServices</span></span>
* <span data-ttu-id="2fb44-404">Unterstützung für API-Version 2019-06-01 (GA) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-404">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2fb44-405">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2fb44-405">Az.Network</span></span>
* <span data-ttu-id="2fb44-406">Unterstützung für privaten Endpunkt und privaten Verknüpfungsdienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-406">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="2fb44-407">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2fb44-407">New cmdlets</span></span>
        - <span data-ttu-id="2fb44-408">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2fb44-408">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2fb44-409">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2fb44-409">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="2fb44-410">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2fb44-410">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2fb44-411">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2fb44-411">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2fb44-412">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2fb44-412">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2fb44-413">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2fb44-413">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2fb44-414">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="2fb44-414">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="2fb44-415">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2fb44-415">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="2fb44-416">Folgende Befehle für das Feature aktualisiert: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies für Subnetz in VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2fb44-416">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="2fb44-417">„New-AzVirtualNetworkSubnetConfig“, „Set-AzVirtualNetworkSubnetConfig“ und „Add-AzVirtualNetworkSubnetConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-417">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="2fb44-418">Optionaler Parameter „-PrivateEndpointNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den privaten Endpunkt in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="2fb44-418">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="2fb44-419">Optionaler Parameter „-PrivateLinkServiceNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den Privat Link-Dienst in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="2fb44-419">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="2fb44-420">Der Cmdlet-Parameter „ServiceName“ von AzPrivateLinkService wurde aus Gründen der Abwärtskompatibilität in „Name“ mit dem Alias „ServiceName“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="2fb44-420">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="2fb44-421">ICMP-Protokoll für Konfigurationen von Netzwerksicherheitsregeln aktiviert</span><span class="sxs-lookup"><span data-stu-id="2fb44-421">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="2fb44-422">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2fb44-422">Updated cmdlets</span></span>
        - <span data-ttu-id="2fb44-423">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2fb44-423">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="2fb44-424">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2fb44-424">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="2fb44-425">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2fb44-425">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="2fb44-426">ConnectionProtocolType (Ikev1/Ikev2) als konfigurierbarer Parameter für „New-AzVirtualNetworkGatewayConnection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-426">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="2fb44-427">PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-427">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="2fb44-428">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2fb44-428">Updated cmdlet:</span></span>
        - <span data-ttu-id="2fb44-429">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2fb44-429">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="2fb44-430">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2fb44-430">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="2fb44-431">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2fb44-431">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="2fb44-432">Application Gateway-Befehl „New-AzApplicationGatewayProbeConfig“ zur Unterstützung des benutzerdefinierten Ports im Test aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-432">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="2fb44-433">„New-AzApplicationGatewayProbeConfig“ aktualisiert: Optionaler Parameter „Port“ hinzugefügt, der zum Testen des Back-End-Servers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2fb44-433">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="2fb44-434">Dieser Parameter gilt für Standard_V2 und WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="2fb44-434">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2fb44-435">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2fb44-435">Az.OperationalInsights</span></span>
* <span data-ttu-id="2fb44-436">Standardversion für gespeicherte Suchvorgänge auf 1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-436">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="2fb44-437">Verarbeitung des regulären NULL-Ausdrucks in benutzerdefinierten Protokollen korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-437">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2fb44-438">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2fb44-438">Az.RecoveryServices</span></span>
* <span data-ttu-id="2fb44-439">„Get-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-439">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="2fb44-440">„Get-AzRecoveryServicesBackupContainer.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-440">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="2fb44-441">„Get-AzRecoveryServicesVault.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-441">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="2fb44-442">„Wait-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-442">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="2fb44-443">„Set-AzRecoveryServicesVaultContext.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-443">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="2fb44-444">„Get-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-444">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="2fb44-445">„Get-AzRecoveryServicesBackupRecoveryPoint.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-445">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="2fb44-446">„Restore-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-446">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="2fb44-447">Dienstaufruf zum Aufheben der Containerregistrierung für Azure-Dateifreigabe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-447">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="2fb44-448">„Set-AzRecoveryServicesAsrAlertSetting.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-448">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="2fb44-449">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2fb44-449">Az.Resources</span></span>
- <span data-ttu-id="2fb44-450">Fehlendes Cmdlet entfernt, auf das in der Dokumentation zu „New-AzResourceGroupDeployment“ verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="2fb44-450">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="2fb44-451">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-451">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2fb44-452">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2fb44-452">Az.ServiceBus</span></span>
* <span data-ttu-id="2fb44-453">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="2fb44-453">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="2fb44-454">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="2fb44-454">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="2fb44-455">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2fb44-455">Az.Sql</span></span>
* <span data-ttu-id="2fb44-456">Fehlende Beispiele für Cmdlet „Set-AzSqlDatabaseSecondary“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-456">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="2fb44-457">Festlegen wiederkehrender Überprüfungen der Sicherheitsrisikobewertung ohne Angabe von E-Mail-Adressen korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-457">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="2fb44-458">Tippfehler in einer Warnmeldung korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-458">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2fb44-459">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2fb44-459">Az.Storage</span></span>
* <span data-ttu-id="2fb44-460">Beispiel in Referenzdokumentation für „Get-AzStorageAccount“ aktualisiert, sodass der richtige Parametername verwendet wird</span><span class="sxs-lookup"><span data-stu-id="2fb44-460">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="2fb44-461">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="2fb44-461">Az.StorageSync</span></span>
* <span data-ttu-id="2fb44-462">Cmdlet „Invoke-AzStorageSyncChangeDetection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-462">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="2fb44-463">Problem 9551 zur Berücksichtigung von „TierFilesOlderThanDays“ behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-463">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2fb44-464">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2fb44-464">Az.Websites</span></span>
* <span data-ttu-id="2fb44-465">Problem behoben, aufgrund dessen einige SiteConfig-Eigenschaften von „Get-AzWebApp“ und „Set-AzWebApp“ nicht zurückgegeben wurden</span><span class="sxs-lookup"><span data-stu-id="2fb44-465">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="2fb44-466">Neuer Standortparameter zu „Get-AzDeletedWebApp“ und „Restore-AzDeletedWebApp“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-466">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="2fb44-467">Fehler beim Klonen von Web-App-Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-467">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="2fb44-468">2.4.0 – Juli 2019</span><span class="sxs-lookup"><span data-stu-id="2fb44-468">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2fb44-469">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2fb44-469">Az.Accounts</span></span>
* <span data-ttu-id="2fb44-470">Unterstützung für Profil-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-470">Add support for profile cmdlets</span></span>
* <span data-ttu-id="2fb44-471">Unterstützung für Umgebungen und Datenebenen in generierten Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-471">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="2fb44-472">Korrektur eines Fehlers, bei dem in einigen Fällen ein falscher Endpunkt für Datenebenen-Cmdlets in Windows PowerShell verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="2fb44-472">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="2fb44-473">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="2fb44-473">Az.Advisor</span></span>
* <span data-ttu-id="2fb44-474">Allgemein verfügbares Release von Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="2fb44-474">GA release of Az.Advisor</span></span>
* <span data-ttu-id="2fb44-475">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="2fb44-475">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2fb44-476">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2fb44-476">Az.ApiManagement</span></span>
* <span data-ttu-id="2fb44-477">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="2fb44-477">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="2fb44-478">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="2fb44-478">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="2fb44-479">Unterstützung für Abfragen von Abonnements nach Benutzer und Produkt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-479">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="2fb44-480">Unterstützung für Abfragen anhand des Umfangs hinzugefügt, „/“, „/apis“, „/apis/echo-api“</span><span class="sxs-lookup"><span data-stu-id="2fb44-480">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="2fb44-481">Behebung von Problem https://github.com/Azure/azure-powershell/issues/9307 und https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="2fb44-481">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="2fb44-482">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="2fb44-482">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="2fb44-483">Unterstützung für die Angabe von „ApiVersion“ und „ApiVersionSetId“ beim Importieren von APIs hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-483">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2fb44-484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2fb44-484">Az.Automation</span></span>
* <span data-ttu-id="2fb44-485">Fehler beim Cmdlet „Set-AzAutomationConnectionFieldValue“ für die Verarbeitung des Zeichenfolgewerts behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-485">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2fb44-486">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2fb44-486">Az.Compute</span></span>
* <span data-ttu-id="2fb44-487">Parameter „HyperVGeneration“ zu New-AzImageConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-487">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2fb44-488">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2fb44-488">Az.DataFactory</span></span>
* <span data-ttu-id="2fb44-489">Aktualisierung der Ausgabe von ADF-Cmdlets für das Abrufen von Aktivitäts-, Pipeline- und Auslöserausführungen, um die Pipe „Select-Object“ zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="2fb44-489">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2fb44-490">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2fb44-490">Az.EventGrid</span></span>
* <span data-ttu-id="2fb44-491">Tippfehler in Dokumentation zu 'New-AzEventGridSubscription' behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-491">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2fb44-492">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2fb44-492">Az.IotHub</span></span>
* <span data-ttu-id="2fb44-493">Unterstützung für das erneute Generieren von Autorisierungsrichtlinienschlüsseln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-493">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2fb44-494">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2fb44-494">Az.Network</span></span>
* <span data-ttu-id="2fb44-495">„RoutingPreference“ zu öffentlichen IP-Tags hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-495">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="2fb44-496">Beispiele für Referenzdokumentation zu „Get-AzNetworkServiceTag“ verbessert</span><span class="sxs-lookup"><span data-stu-id="2fb44-496">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2fb44-497">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2fb44-497">Az.PolicyInsights</span></span>
* <span data-ttu-id="2fb44-498">Fehlerbehebung für Nullverweis in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="2fb44-498">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="2fb44-499">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="2fb44-499">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2fb44-500">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2fb44-500">Az.OperationalInsights</span></span>
* <span data-ttu-id="2fb44-501">Zurückgegebenes CustomLog-Datenquellenmodell in Get-AzOperationalInsightsDataSource korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-501">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2fb44-502">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2fb44-502">Az.RecoveryServices</span></span>
* <span data-ttu-id="2fb44-503">Fehlerbehebung für Befehl „get-policy“ IaaSVMs</span><span class="sxs-lookup"><span data-stu-id="2fb44-503">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="2fb44-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2fb44-504">Az.Resources</span></span>
    - <span data-ttu-id="2fb44-505">Hilfetext für Parameter „-Top“ von „Get-AzPolicyState“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-505">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="2fb44-506">Clientseitige Unterstützung von Paginierung für „Get-AzPolicyAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-506">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="2fb44-507">Neue Parameter für „Set-AzPolicyAssignment“, „-PolicyParameters“ und „-PolicyParametersObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-507">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="2fb44-508">Einige Aktualisierungen von Dokumentationen und Beispielen für Policy-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2fb44-508">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2fb44-509">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2fb44-509">Az.ServiceBus</span></span>
* <span data-ttu-id="2fb44-510">Korrektur für Problem Nr. 4938: „New-AzureRmServiceBusQueue“ gibt beim Festlegen von „MaxSizeInMegabytes“ „BadRequest“ zurück</span><span class="sxs-lookup"><span data-stu-id="2fb44-510">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="2fb44-511">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2fb44-511">Az.Sql</span></span>
* <span data-ttu-id="2fb44-512">Instanzfailovergruppen-Cmdlets aus Vorschauversion in öffentliche Version hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-512">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="2fb44-513">Unterstützung von Azure SQL Server\Datenbanküberwachung mit neuen Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2fb44-513">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="2fb44-514">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="2fb44-514">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="2fb44-515">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="2fb44-515">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="2fb44-516">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="2fb44-516">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="2fb44-517">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="2fb44-517">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="2fb44-518">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="2fb44-518">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="2fb44-519">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="2fb44-519">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="2fb44-520">E-Mail-Einschränkungen aus Einstellungen der Sicherheitsrisikobewertung entfernt</span><span class="sxs-lookup"><span data-stu-id="2fb44-520">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2fb44-521">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2fb44-521">Az.Storage</span></span>
* <span data-ttu-id="2fb44-522">Zwei Parameter („-IndexDocument“ und „-ErrorDocument404Path“) in folgendem Cmdlet von erforderlich in optional geändert:</span><span class="sxs-lookup"><span data-stu-id="2fb44-522">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="2fb44-523">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="2fb44-523">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="2fb44-524">Hilfe zu „Get-AzStorageBlobContent“ mit neuem Beispiel ergänzt</span><span class="sxs-lookup"><span data-stu-id="2fb44-524">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="2fb44-525">Anzeige von mehr Fehlerinformationen beim Fehlschlagen eines Cmdlets mit „StorageException“</span><span class="sxs-lookup"><span data-stu-id="2fb44-525">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="2fb44-526">Unterstützung für das Erstellen oder Aktualisieren von Speicherkonten mit Azure Files AAD-DS-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="2fb44-526">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="2fb44-527">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2fb44-527">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="2fb44-528">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2fb44-528">Set-AzStorageAccount</span></span>
* <span data-ttu-id="2fb44-529">Unterstützung für das Auflisten oder Schließen von Dateihandles einer Dateifreigabe, eines Dateiverzeichnisses oder einer Datei</span><span class="sxs-lookup"><span data-stu-id="2fb44-529">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="2fb44-530">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="2fb44-530">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="2fb44-531">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="2fb44-531">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="2fb44-532">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="2fb44-532">Az.StorageSync</span></span>
* <span data-ttu-id="2fb44-533">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="2fb44-533">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="2fb44-534">2.3.2 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="2fb44-534">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2fb44-535">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2fb44-535">Az.Accounts</span></span>
* <span data-ttu-id="2fb44-536">Fehler behoben, aufgrund dessen in manchen Fällen eine falsche URL für Funktionsaufrufe verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="2fb44-536">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="2fb44-537">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="2fb44-537">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="2fb44-538">Problem mit Aliasen zwischen AzureRM und Azure-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-538">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="2fb44-539">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="2fb44-539">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="2fb44-540">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="2fb44-540">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2fb44-541">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2fb44-541">Az.Compute</span></span>
* <span data-ttu-id="2fb44-542">Die einfachen Parametersätze „New-AzVm“ und „New-AzVmss“ akzeptieren jetzt den Parameter „ProximityPlacementGroup“.</span><span class="sxs-lookup"><span data-stu-id="2fb44-542">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="2fb44-543">Tippfehler in der Referenzdokumentation für „New-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-543">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="2fb44-544">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="2fb44-544">Az.Dns</span></span>
* <span data-ttu-id="2fb44-545">Tippfehler in den Hilfebeispielen zu „Set-AzDnsZone“ behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-545">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2fb44-546">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2fb44-546">Az.EventGrid</span></span>
* <span data-ttu-id="2fb44-547">Zur Verwendung der API-Version 2019-06-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-547">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="2fb44-548">Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="2fb44-548">New cmdlets:</span></span>
    - <span data-ttu-id="2fb44-549">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="2fb44-549">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="2fb44-550">Erstellt eine neue Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="2fb44-550">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="2fb44-551">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="2fb44-551">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="2fb44-552">Ruft die Details einer Event Grid-Domäne oder eine Liste aller Event Grid-Domänen im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="2fb44-552">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="2fb44-553">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="2fb44-553">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="2fb44-554">Entfernt eine Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="2fb44-554">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="2fb44-555">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="2fb44-555">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="2fb44-556">Generiert den freigegebenen Zugriffsschlüssel für eine Azure Event Grid-Domäne erneut.</span><span class="sxs-lookup"><span data-stu-id="2fb44-556">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="2fb44-557">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="2fb44-557">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="2fb44-558">Ruft die freigegebenen Zugriffsschlüssel ab, die zum Veröffentlichen von Ereignissen in einer Event Grid-Domäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2fb44-558">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="2fb44-559">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="2fb44-559">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="2fb44-560">Erstellt ein neues Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="2fb44-560">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="2fb44-561">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="2fb44-561">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="2fb44-562">Ruft die Details eines Event Grid-Domänenthemas oder eine Liste aller Event Grid-Domänenthemen unter der jeweiligen Event Grid-Domäne im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="2fb44-562">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="2fb44-563">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="2fb44-563">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="2fb44-564">Entfernt ein vorhandenes Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="2fb44-564">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="2fb44-565">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="2fb44-565">Updated cmdlets:</span></span>
    - <span data-ttu-id="2fb44-566">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="2fb44-566">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="2fb44-567">Neue erforderliche Parameter zur Unterstützung des Pipings für die neue Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="2fb44-567">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="2fb44-568">Neue erforderliche Parameter zum Angeben des neuen Event Grid-Domänennamens und/oder Namens des Event Grid-Domänenthemas hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="2fb44-568">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="2fb44-569">Neue Parametersätze für Domänen und Domänenthemen hinzugefügt, um die Wiederverwendung vorhandener Parameter zuzulassen (‚z. B. „EndPointType“, „SubjectBeginsWith“ usw.)</span><span class="sxs-lookup"><span data-stu-id="2fb44-569">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="2fb44-570">Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="2fb44-570">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="2fb44-571">Ablaufdatum des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="2fb44-571">Event subscription expiration date,</span></span>
            - <span data-ttu-id="2fb44-572">Erweiterte Filterparameter</span><span class="sxs-lookup"><span data-stu-id="2fb44-572">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="2fb44-573">Neue Enumeration für „servicebusqueue“ als Ziel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-573">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="2fb44-574">Verwendung der Option „All“ in „-IncludedEventType“ gesperrt und wie folgt ersetzt</span><span class="sxs-lookup"><span data-stu-id="2fb44-574">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="2fb44-575">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="2fb44-575">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="2fb44-576">Neue optionale Parameter („Top“, „ODataQuery“ und „NextLink“) zur Unterstützung der Ergebnispaginierung und -filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-576">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="2fb44-577">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="2fb44-577">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="2fb44-578">Neue erforderliche Parameter zur Unterstützung des Pipings für die Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Entfernen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="2fb44-578">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="2fb44-579">Neue erforderliche Parameter zum Angeben des Event Grid-Domänennamens und/oder Event Grid-Domänenthemanamens hinzugefügt, um das Entfernen vorhandener Ereignisabonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="2fb44-579">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2fb44-580">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2fb44-580">Az.FrontDoor</span></span>
* <span data-ttu-id="2fb44-581">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="2fb44-581">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="2fb44-582">Unterstützung von Transformationen und neuen Wert für den Operator zum automatischen Vervollständigen (RegEx) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-582">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="2fb44-583">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="2fb44-583">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="2fb44-584">Neue Werte für automatisches Vervollständigen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-584">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2fb44-585">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2fb44-585">Az.Network</span></span>
* <span data-ttu-id="2fb44-586">Unterstützung für Virtual Network-Gatewayressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-586">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="2fb44-587">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2fb44-587">New cmdlets</span></span>
        - <span data-ttu-id="2fb44-588">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="2fb44-588">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="2fb44-589">AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="2fb44-589">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="2fb44-590">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2fb44-590">New cmdlets</span></span> 
        - <span data-ttu-id="2fb44-591">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="2fb44-591">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="2fb44-592">„PrivatePrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-592">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="2fb44-593">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2fb44-593">New cmdlets</span></span> 
        - <span data-ttu-id="2fb44-594">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2fb44-594">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="2fb44-595">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2fb44-595">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="2fb44-596">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2fb44-596">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="2fb44-597">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2fb44-597">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="2fb44-598">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2fb44-598">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="2fb44-599">„PrivateEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-599">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="2fb44-600">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2fb44-600">New cmdlets</span></span>
        - <span data-ttu-id="2fb44-601">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2fb44-601">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2fb44-602">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2fb44-602">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2fb44-603">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2fb44-603">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2fb44-604">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="2fb44-604">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="2fb44-605">Folgende Befehle für das Feature aktualisiert: UseLocalAzureIpAddress-Flag für „VpnConnection“</span><span class="sxs-lookup"><span data-stu-id="2fb44-605">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="2fb44-606">„New-AzVpnConnection§ „ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="2fb44-606">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="2fb44-607">„Set-AzVpnConnection“ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="2fb44-607">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="2fb44-608">Schreibgeschütztes Feld „PeeredConnections“ beim ExpressRoute-Peering hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-608">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="2fb44-609">Schreibgeschütztes Feld „GlobalReachEnabled“ in ExpressRoute hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-609">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="2fb44-610">Breaking Change-Attribut hinzugefügt, um auf das veraltete Feld „AllowGlobalReach“ im ExpressRouteCircuit-Modell hinzuweisen</span><span class="sxs-lookup"><span data-stu-id="2fb44-610">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="2fb44-611">Fehler 8756 bei der Verwendung von „TargetListenerID“ mit AzApplicationGatewayRedirectConfiguration-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-611">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="2fb44-612">Fehler in „New-AzApplicationGatewayPathRuleConfig“ behoben, aufgrund dessen der Regelsatz für erneutes Generieren nicht festgelegt werden konnte</span><span class="sxs-lookup"><span data-stu-id="2fb44-612">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="2fb44-613">Fehler bei der Anzeige von „VirtualNetworkTaps“ in „NetworkInterfaceIpConfiguration“ behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-613">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="2fb44-614">Cortex-Get-Cmdlets zum Auflisten aller Komponenten korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-614">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="2fb44-615">Problem beim Erstellen des festen VirtualHub-Verweises für ExpressRouteGateways behoben (VpnGateway)</span><span class="sxs-lookup"><span data-stu-id="2fb44-615">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="2fb44-616">Unterstützung für Verfügbarkeitszonen in AzureFirewall und NatGateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-616">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="2fb44-617">Cmdlet „Get-AzNetworkServiceTag“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-617">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="2fb44-618">Unterstützung für mehrere öffentliche IP-Adressen für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-618">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="2fb44-619">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="2fb44-619">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="2fb44-620">Parameter „-PublicIpAddress“ hinzugefügt, der ein oder mehre öffentliche IP-Adressobjekte akzeptiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-620">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="2fb44-621">Parameter „- VirtualNetwork“ hinzugefügt, der ein Virtual Network-Objekt akzeptiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-621">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="2fb44-622">Methoden „AddPublicIpAddress“ und „RemovePublicIpAddress“ für Firewallobjekte hinzugefügt (akzeptieren ein öffentliches IP-Adressobjekt als Eingabe)</span><span class="sxs-lookup"><span data-stu-id="2fb44-622">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="2fb44-623">Parameter „-PublicIpName“ und „-VirtualNetworkName“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-623">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="2fb44-624">Folgende Befehle für das Feature aktualisiert: VpnClient-AAD-Authentifizierungsoptionen auf die Gatewayressource des virtuellen Netzwerkgateways festgelegt</span><span class="sxs-lookup"><span data-stu-id="2fb44-624">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="2fb44-625">„New-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-625">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="2fb44-626">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2fb44-626">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="2fb44-627">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionaler Switch-Parameter „RemoveAadAuthentication“ zum Entfernen von VpnClient-AAD-Authentifizierungsoptionen aus dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-627">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2fb44-628">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2fb44-628">Az.OperationalInsights</span></span>
* <span data-ttu-id="2fb44-629">Tarif **pergb2018** im Befehl „New-AzureRmOperationalInsightsWorkspace“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="2fb44-629">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="2fb44-630">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2fb44-630">Az.Resources</span></span>
* <span data-ttu-id="2fb44-631">Unterstützung für zusätzliche Optionen zum Exportieren von Vorlagen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-631">Support for additional Template Export options</span></span>
    - <span data-ttu-id="2fb44-632">Parameter „-SkipResourceNameParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-632">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="2fb44-633">Parameter -SkipAllParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-633">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="2fb44-634">Parameter „-Resource“ zu „Export-AzResourceGroup“ hinzugefügt, um das Filtern exportierter Ressourcen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="2fb44-634">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2fb44-635">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2fb44-635">Az.ServiceFabric</span></span>
* <span data-ttu-id="2fb44-636">Problem beim Hinzufügen des Zertifikats mit „ByExistingKeyVault“ behoben (Abruf des falschen Fingerabdrucks in manchen Fällen)</span><span class="sxs-lookup"><span data-stu-id="2fb44-636">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="2fb44-637">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2fb44-637">Az.Sql</span></span>
* <span data-ttu-id="2fb44-638">Suffix des Advanced Threat Protection-Endpunkts korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-638">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="2fb44-639">Durch Advanced Data Security ermöglichte Außerkraftsetzungen der Advanced Threat Protection-Richtlinie korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-639">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="2fb44-640">Neue Cmdlets für „Management.Sql“ ermöglichen Kunden das Hinzufügen von TDE-Schlüsseln und Festlegen der TDE-Schutzvorrichtung für verwaltete Instanzen.</span><span class="sxs-lookup"><span data-stu-id="2fb44-640">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="2fb44-641">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2fb44-641">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="2fb44-642">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2fb44-642">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="2fb44-643">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2fb44-643">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="2fb44-644">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="2fb44-644">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="2fb44-645">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="2fb44-645">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2fb44-646">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2fb44-646">Az.Storage</span></span>
* <span data-ttu-id="2fb44-647">Unterstützung von „FileStorage“ und „SkuName Premium_ZRS“ beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="2fb44-647">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="2fb44-648">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2fb44-648">New-AzStorageAccount</span></span>
* <span data-ttu-id="2fb44-649">Überarbeitete Beschreibung des Cmdlets für die Unveränderlichkeit von Blobs</span><span class="sxs-lookup"><span data-stu-id="2fb44-649">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="2fb44-650">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="2fb44-650">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2fb44-651">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2fb44-651">Az.Websites</span></span>
* <span data-ttu-id="2fb44-652">Optimiert „Get-AzWebAppCertificate“, um nach der Ressourcengruppe auf dem Server zu filtern (nicht auf dem Client)</span><span class="sxs-lookup"><span data-stu-id="2fb44-652">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="2fb44-653">Switch-Parameter „-UseDisasterRecovery“ für „Get-AzWebAppSnapshot“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-653">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="2fb44-654">2.2.0 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="2fb44-654">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="2fb44-655">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2fb44-655">Az.Cdn</span></span>
* <span data-ttu-id="2fb44-656">Es wurden Cmdlets aktualisiert, um das rulesEngine-Feature basierend auf der API-Version 2019-04-15 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2fb44-656">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2fb44-657">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2fb44-657">Az.Compute</span></span>
* <span data-ttu-id="2fb44-658">Der Parameter `NoWait` wurde hinzugefügt, der den Vorgang startet und sofort zurückkehrt, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="2fb44-658">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="2fb44-659">Aktualisierte Cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="2fb44-659">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2fb44-660">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2fb44-660">Az.EventHub</span></span>
* <span data-ttu-id="2fb44-661">Fehlerbehebung für #9231 – Get-AzEventHubNamespace gibt keine Tags zurück</span><span class="sxs-lookup"><span data-stu-id="2fb44-661">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="2fb44-662">Fehlerbehebung für #9230 – Get-AzEventHubNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="2fb44-662">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2fb44-663">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2fb44-663">Az.Network</span></span>
* <span data-ttu-id="2fb44-664">ResourceId und InputObject wurden für NAT Gateway aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-664">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="2fb44-665">Es wurde ein Alias für ResourceId und InputObjectr hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-665">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2fb44-666">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2fb44-666">Az.PolicyInsights</span></span>
* <span data-ttu-id="2fb44-667">Fehlerbehebung für Nullverweis in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="2fb44-667">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2fb44-668">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2fb44-668">Az.RecoveryServices</span></span>
* <span data-ttu-id="2fb44-669">Minimale Aufbewahrung in Tagen für IaaSVM-Richtlinie wurde von 1 in 7 geändert</span><span class="sxs-lookup"><span data-stu-id="2fb44-669">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2fb44-670">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2fb44-670">Az.ServiceBus</span></span>
* <span data-ttu-id="2fb44-671">Fehlerbehebung für #9182 – Get-AzServiceBusNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="2fb44-671">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2fb44-672">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2fb44-672">Az.ServiceFabric</span></span>
* <span data-ttu-id="2fb44-673">Tippfehler in Fehlermeldung für Update-AzServiceFabricReliability wurde behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-673">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="2fb44-674">Fehlendes Zeichen in Service Fabric-Befehlszeilen wurde behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-674">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="2fb44-675">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2fb44-675">Az.Sql</span></span>
* <span data-ttu-id="2fb44-676">Der DnsZonePartner-Parameter für das Cmdlet New-AzureSqlInstance wurde hinzugefügt, um AutoDr für verwaltete Instanzen zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="2fb44-676">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="2fb44-677">Das Cmdlet Get-AzSqlDatabaseSecureConnectionPolicy wird eingestellt</span><span class="sxs-lookup"><span data-stu-id="2fb44-677">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="2fb44-678">Cmdlets zum Schutz vor Bedrohungen werden in „Advanced Threat Protection“ (Erweiterter Schutz vor Bedrohungen) umbenannt</span><span class="sxs-lookup"><span data-stu-id="2fb44-678">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="2fb44-679">New-AzSqlInstance – Die Parameter StorageSizeInGB und LicenseType sind jetzt optional</span><span class="sxs-lookup"><span data-stu-id="2fb44-679">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2fb44-680">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2fb44-680">Az.Websites</span></span>
* <span data-ttu-id="2fb44-681">Das Problem, bei dem die Verwendung von Set-AzWebApp und Set-AzWebAppSlot mit der -WebApp-Eigenschaft die Tags entfernt hat, wurde behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-681">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="2fb44-682">2.1.0 – Mai 2019</span><span class="sxs-lookup"><span data-stu-id="2fb44-682">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="2fb44-683">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2fb44-683">Az.ApiManagement</span></span>
* <span data-ttu-id="2fb44-684">Es wurden neue Cmdlets zum Verwalten der Diagnose im globalen sowie im API-Bereich erstellt</span><span class="sxs-lookup"><span data-stu-id="2fb44-684">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="2fb44-685">**Get-AzApiManagementDiagnostic**: Abrufen der Diagnose, die im globalen oder im API-Bereich konfiguriert wurde</span><span class="sxs-lookup"><span data-stu-id="2fb44-685">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="2fb44-686">**New-AzApiManagementDiagnostic**: Erstellen neuer Diagnosen im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="2fb44-686">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="2fb44-687">**New-AzApiManagementHttpMessageDiagnostic**: Erstellen einer Diagnoseeinstellung für die zu protokollierenden Kopfzeilen und für die Größe der Bytes für den Text</span><span class="sxs-lookup"><span data-stu-id="2fb44-687">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="2fb44-688">**New-AzApiManagementPipelineDiagnosticSetting**: Erstellen von Diagnoseeinstellungen für ein-/ausgehende HTTP-Nachrichten für das Gateway</span><span class="sxs-lookup"><span data-stu-id="2fb44-688">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="2fb44-689">**New-AzApiManagementSamplingSetting**: Erstellen der Einstellung „Sampling“ für die Anforderungen/Antworten für eine Diagnose</span><span class="sxs-lookup"><span data-stu-id="2fb44-689">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="2fb44-690">**Remove-AzApiManagementDiagnostic**: Entfernen einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="2fb44-690">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="2fb44-691">**Set-AzApiManagementDiagnostic**: Aktualisieren einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="2fb44-691">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="2fb44-692">Es wurden neue Cmdlets für die Cacheverwaltung im ApiManagement-Dienst erstellt</span><span class="sxs-lookup"><span data-stu-id="2fb44-692">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="2fb44-693">**Get-AzApiManagementCache**: Abrufen der Details des durch den Bezeichner angegebenen Caches oder aller Caches</span><span class="sxs-lookup"><span data-stu-id="2fb44-693">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="2fb44-694">**New-AzApiManagementCache**: Erstellen eines neuen „standardmäßigen“ Caches oder eines Caches in einer bestimmten „Region“ von Azure</span><span class="sxs-lookup"><span data-stu-id="2fb44-694">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="2fb44-695">**Remove-AzApiManagementCache**: Entfernen eines Caches</span><span class="sxs-lookup"><span data-stu-id="2fb44-695">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="2fb44-696">**Update-AzApiManagementCache**: Aktualisieren eines Caches</span><span class="sxs-lookup"><span data-stu-id="2fb44-696">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="2fb44-697">Es wurden neue Cmdlets zur Verwaltung von API-Schemas erstellt</span><span class="sxs-lookup"><span data-stu-id="2fb44-697">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="2fb44-698">**New-AzApiManagementSchema**: Erstellen eines neuen Schemas für eine API</span><span class="sxs-lookup"><span data-stu-id="2fb44-698">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="2fb44-699">**Get-AzApiManagementSchema**: Abrufen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="2fb44-699">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="2fb44-700">**Remove-AzApiManagementSchema**: Entfernen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="2fb44-700">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="2fb44-701">**Set-AzApiManagementSchema**: Aktualisieren des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="2fb44-701">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="2fb44-702">Es wurde ein neues Cmdlet zum Generieren eines Benutzertokens erstellt</span><span class="sxs-lookup"><span data-stu-id="2fb44-702">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="2fb44-703">**New-AzApiManagementUserToken**: Generieren eines neuen Benutzertokens, das standardmäßig für acht Stunden gültig ist. Mit diesem Cmdlet kann das Token für den „GIT“-Benutzer generiert werden./</span><span class="sxs-lookup"><span data-stu-id="2fb44-703">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="2fb44-704">Es wurde ein neues Cmdlet zum Abrufen des Netzwerkstatus erstellt</span><span class="sxs-lookup"><span data-stu-id="2fb44-704">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="2fb44-705">**Get-AzApiManagementNetworkStatus**: Abrufen der Netzwerkstatuskonnektivität von Ressourcen, von denen der API Management-Dienst abhängig ist</span><span class="sxs-lookup"><span data-stu-id="2fb44-705">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="2fb44-706">Dies ist hilfreich, wenn Sie den ApiManagement-Dienst in einem virtuellen Netzwerk bereitstellen und überprüfen, ob eine der Abhängigkeiten fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="2fb44-706">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="2fb44-707">Das Cmdlet **New-AzApiManagement** wurde zum Verwalten des ApiManagement-Diensts aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-707">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="2fb44-708">Die Unterstützung für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-708">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="2fb44-709">Die Unterstützung zum Aktivieren des Flags „EnableClientCertificate“ für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-709">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="2fb44-710">Das neue Cmdlet **New-AzApiManagementSslSetting** ermöglicht die Konfiguration der „TLS/SSL“-Einstellung für „Back-End“ und „Front-End“</span><span class="sxs-lookup"><span data-stu-id="2fb44-710">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="2fb44-711">Dies kann auch dazu verwendet werden, um „Verschlüsselungen“ wie „3DES“ und „ServerProtokolle“ wie „Http2“ für das „Front-End“ eines ApiManagement-Diensts zu konfigurieren</span><span class="sxs-lookup"><span data-stu-id="2fb44-711">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="2fb44-712">Die Unterstützung für die Konfiguration des Hostnamens „DeveloperPortal“ wurde zum ApiManagement-Dienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-712">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="2fb44-713">Die **Get-AzApiManagementSsoToken**-Cmdlets wurden aktualisiert, um das Objekt „PsApiManagement“ als Eingabe zu übernehmen</span><span class="sxs-lookup"><span data-stu-id="2fb44-713">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="2fb44-714">Das Cmdlet wurde aktualisiert, um Fehlermeldungen inline anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="2fb44-714">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="2fb44-715">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Fehlercode: ValidationError-Fehlermeldung: Mindestens ein Feld enthält ungültige Werte: Fehlerdetails: [Code=ValidationError, Message=Fehler in Element 'log-to-eventhub' in Zeile 3, Spalte 10: Protokollierungstool nicht gefunden, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="2fb44-715">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="2fb44-716">Cmdlet **Export-AzApiManagementApi** wurde für den Export von APIs im Format „OpenApi 3.0“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-716">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="2fb44-717">Cmdlet **Import-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-717">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="2fb44-718">Zum Importieren der API aus der „OpenApi 3.0“-Dokumentspezifikation</span><span class="sxs-lookup"><span data-stu-id="2fb44-718">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="2fb44-719">Zur Außerkraftsetzung der „PsApiManagementSchema“-Eigenschaft, die in einem beliebigen Dokument („Swagger“, „Wadl“, „Wsdl“, „OpenApi“) angegeben ist</span><span class="sxs-lookup"><span data-stu-id="2fb44-719">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="2fb44-720">Zur Außerkraftsetzung der „ServiceUrl“-Eigenschaft, die in einem beliebigen Dokument angegeben ist</span><span class="sxs-lookup"><span data-stu-id="2fb44-720">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="2fb44-721">Cmdlet **Get-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="2fb44-721">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="2fb44-722">Cmdlet **Set-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ und im Format mit XML-Escapezeichen mit „xml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="2fb44-722">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="2fb44-723">Cmdlet **New-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-723">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="2fb44-724">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="2fb44-724">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="2fb44-725">Zum Erstellen einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="2fb44-725">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="2fb44-726">Zum Klonen einer API mithilfe von „SourceApiId“ und „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="2fb44-726">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="2fb44-727">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="2fb44-727">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="2fb44-728">Cmdlet **Set-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-728">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="2fb44-729">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="2fb44-729">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="2fb44-730">Zum Aktualisieren einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="2fb44-730">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="2fb44-731">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="2fb44-731">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="2fb44-732">Cmdlet **New-AzApiManagementRevision** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-732">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="2fb44-733">Zum Klonen (Kopiertags, Produkte, Vorgänge und Richtlinien) einer vorhandenen Version mithilfe von „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="2fb44-733">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="2fb44-734">Die neue Version übernimmt die „ApiId“ des übergeordneten Elements</span><span class="sxs-lookup"><span data-stu-id="2fb44-734">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="2fb44-735">Zum Bereitstellen einer „ApiRevisionDescription“</span><span class="sxs-lookup"><span data-stu-id="2fb44-735">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="2fb44-736">Zur Außerkraftsetzung der „ServiceUrl“ beim Klonen einer API</span><span class="sxs-lookup"><span data-stu-id="2fb44-736">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="2fb44-737">Cmdlet **New-AzApiManagementIdentityProvider** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-737">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="2fb44-738">Zum Konfigurieren von „AAD“ oder „AADB2C“ mit einer „Authority“</span><span class="sxs-lookup"><span data-stu-id="2fb44-738">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="2fb44-739">Zum Einrichten von „SignupPolicy“, „SigninPolicy“, „ProfileEditingPolicy“ und „PasswordResetPolicy“</span><span class="sxs-lookup"><span data-stu-id="2fb44-739">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="2fb44-740">Cmdlet **New-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-740">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="2fb44-741">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="2fb44-741">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="2fb44-742">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="2fb44-742">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="2fb44-743">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-743">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="2fb44-744">Cmdlet **Set-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-744">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="2fb44-745">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="2fb44-745">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="2fb44-746">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="2fb44-746">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="2fb44-747">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-747">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="2fb44-748">Folgende Cmdlets wurden aktualisiert, um „ResourceId“ als Eingabe zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="2fb44-748">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="2fb44-749">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="2fb44-749">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="2fb44-750">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="2fb44-750">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="2fb44-751">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="2fb44-751">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="2fb44-752">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="2fb44-752">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="2fb44-753">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="2fb44-753">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="2fb44-754">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="2fb44-754">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="2fb44-755">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="2fb44-755">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="2fb44-756">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="2fb44-756">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="2fb44-757">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="2fb44-757">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="2fb44-758">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="2fb44-758">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="2fb44-759">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="2fb44-759">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="2fb44-760">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="2fb44-760">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2fb44-761">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2fb44-761">Az.Automation</span></span>
* <span data-ttu-id="2fb44-762">Get-AzAutomationJobOutputRecord wurde aktualisiert, um JSON- und Textdatensatzwerte zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="2fb44-762">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="2fb44-763">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="2fb44-763">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="2fb44-764">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="2fb44-764">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="2fb44-765">Das Verhalten von Start-AzAutomationDscCompilationJob wurde geändert, um den Auftrag einfach zu starten, anstatt auf dessen Abschluss zu warten</span><span class="sxs-lookup"><span data-stu-id="2fb44-765">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="2fb44-766">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="2fb44-766">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="2fb44-767">Fehlerbehebung für Get-AzAutomationDscNode, wenn die Verwendung von „-Name“ alle Knoten zurückgibt</span><span class="sxs-lookup"><span data-stu-id="2fb44-767">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="2fb44-768">Jetzt wird nur der übereinstimmende Knoten zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="2fb44-768">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2fb44-769">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2fb44-769">Az.Compute</span></span>
* <span data-ttu-id="2fb44-770">Parameter „ProtectFromScaleIn“ und „ProtectFromScaleSetAction“ wurden zum Cmdlet „Update-AzVmssVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-770">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="2fb44-771">Der jetzt festgelegte wimple-Parameter „New-AzVM“ verwendet standardmäßig einen verfügbaren Standort, wenn „East US“ (USA, Osten) nicht unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="2fb44-771">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2fb44-772">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2fb44-772">Az.DataLakeStore</span></span>
* <span data-ttu-id="2fb44-773">Das ADLS-SDK wurde aktualisiert, um „HttpClient“ zu verwenden und Datenebenentests wurden mit dem Azure-Framework integriert</span><span class="sxs-lookup"><span data-stu-id="2fb44-773">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2fb44-774">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2fb44-774">Az.Monitor</span></span>
* <span data-ttu-id="2fb44-775">Fehlerbehebung bei falschen Parameternamen in Hilfebeispielen</span><span class="sxs-lookup"><span data-stu-id="2fb44-775">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2fb44-776">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2fb44-776">Az.Network</span></span>
* <span data-ttu-id="2fb44-777">DisableBgpRoutePropagation-Flag wurde zur Ausgabe der effektiven Routentabelle hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-777">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="2fb44-778">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2fb44-778">Updated cmdlet:</span></span>
        - <span data-ttu-id="2fb44-779">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="2fb44-779">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="2fb44-780">Fehlerbehebung von doppeltem Bindestrich in Dokumentation von New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2fb44-780">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="2fb44-781">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2fb44-781">Az.Resources</span></span>
* <span data-ttu-id="2fb44-782">Neues Cmdlet „Get-AzureRmDenyAssignment“ zum Abrufen von Ablehnungszuweisungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-782">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="2fb44-783">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2fb44-783">Az.Sql</span></span>
* <span data-ttu-id="2fb44-784">„Advanced Threat Protection“-Cmdlets in „Advanced Data Security“ umbenennen und Sicherheitsrisikobewertung standardmäßig aktivieren</span><span class="sxs-lookup"><span data-stu-id="2fb44-784">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="2fb44-785">2.0.0: Mai 2019</span><span class="sxs-lookup"><span data-stu-id="2fb44-785">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2fb44-786">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2fb44-786">Az.Accounts</span></span>
* <span data-ttu-id="2fb44-787">Authentifizierungsbibliothek aktualisiert, um ADFS-Probleme mit der Authentifizierung per Benutzername/Kennwort zu beheben</span><span class="sxs-lookup"><span data-stu-id="2fb44-787">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2fb44-788">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2fb44-788">Az.CognitiveServices</span></span>
* <span data-ttu-id="2fb44-789">Ausschließliche Anzeige des Bing-Haftungsausschlusses für Bing-Suchdienste</span><span class="sxs-lookup"><span data-stu-id="2fb44-789">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="2fb44-790">Fehler behoben, der zu einem Fehler bei der Kontoerstellung führte</span><span class="sxs-lookup"><span data-stu-id="2fb44-790">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2fb44-791">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2fb44-791">Az.Compute</span></span>
* <span data-ttu-id="2fb44-792">Feature für die Näherungsplatzierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="2fb44-792">Proximity placement group feature.</span></span>
    - <span data-ttu-id="2fb44-793">Die folgenden neuen Cmdlets wurden hinzugefügt:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="2fb44-793">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="2fb44-794">Der neue Parameter „ProximityPlacementGroupId“ wurde zu den folgenden Cmdlets hinzugefügt:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="2fb44-794">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="2fb44-795">Der Parameter „StorageAccountType“ wurde zu „New-AzGalleryImageVersion“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2fb44-795">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="2fb44-796">„TargetRegion“ von „New-AzGalleryImageVersion“ kann „StorageAccountType“ enthalten.</span><span class="sxs-lookup"><span data-stu-id="2fb44-796">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="2fb44-797">Switch-Parameter „SkipShutdown“ wurde zu „Stop-AzVM“ und „Stop-AzVmss“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2fb44-797">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="2fb44-798">Wichtige Änderungen</span><span class="sxs-lookup"><span data-stu-id="2fb44-798">Breaking changes</span></span>
    - <span data-ttu-id="2fb44-799">„Set-AzVMBootDiagnostics“ in „Set-AzVMBootDiagnostic“ geändert</span><span class="sxs-lookup"><span data-stu-id="2fb44-799">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="2fb44-800">„Export-AzLogAnalyticThrottledRequests“ in „Export-AzLogAnalyticThrottledRequests“ geändert</span><span class="sxs-lookup"><span data-stu-id="2fb44-800">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="2fb44-801">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="2fb44-801">Az.DeploymentManager</span></span>
* <span data-ttu-id="2fb44-802">Erste allgemein verfügbare Version der Azure-Bereitstellungs-Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2fb44-802">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="2fb44-803">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="2fb44-803">Az.Dns</span></span>
* <span data-ttu-id="2fb44-804">Automatische Delegierung des DNS-Namenservers</span><span class="sxs-lookup"><span data-stu-id="2fb44-804">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="2fb44-805">Das Cmdlet zum Erstellen einer DNS-Zone akzeptiert den übergeordneten Zonennamen als zusätzlichen optionalen Parameter.</span><span class="sxs-lookup"><span data-stu-id="2fb44-805">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="2fb44-806">NS-Einträge in der übergeordneten Zone für neu erstellte untergeordnete Zone hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-806">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2fb44-807">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2fb44-807">Az.FrontDoor</span></span>
* <span data-ttu-id="2fb44-808">Erste allgemein verfügbare Version der Azure Frontdoor-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2fb44-808">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="2fb44-809">WAF-Cmdlets so umbenannt, dass sie „Waf“ enthalten</span><span class="sxs-lookup"><span data-stu-id="2fb44-809">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="2fb44-810">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2fb44-810">Az.HDInsight</span></span>
* <span data-ttu-id="2fb44-811">Zwei Cmdlets entfernt:</span><span class="sxs-lookup"><span data-stu-id="2fb44-811">Removed two cmdlets:</span></span>
    - <span data-ttu-id="2fb44-812">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2fb44-812">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="2fb44-813">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2fb44-813">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="2fb44-814">Neues Cmdlet „Set-AzHDInsightGatewayCredential“ hinzugefügt, um „Grant-AzHDInsightHttpServicesAccess“ zu ersetzen</span><span class="sxs-lookup"><span data-stu-id="2fb44-814">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="2fb44-815">Cmdlet „Get-AzHDInsightJobOutput“ aktualisiert, um zwischen Leserrolle und HDInsight-Bedienerrolle zu unterscheiden:</span><span class="sxs-lookup"><span data-stu-id="2fb44-815">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="2fb44-816">Benutzer mit der Rolle „Leser“ müssen den Parameter „DefaultStorageAccountKey“ explizit angeben, andernfalls treten Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="2fb44-816">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="2fb44-817">Benutzer mit der Rolle des HDInsight-Bedieners sind nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="2fb44-817">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2fb44-818">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2fb44-818">Az.Monitor</span></span>
* <span data-ttu-id="2fb44-819">Neue Cmdlets für SQR-API (Scheduled Query Rule, geplante Abfrageregel)</span><span class="sxs-lookup"><span data-stu-id="2fb44-819">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="2fb44-820">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="2fb44-820">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="2fb44-821">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="2fb44-821">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="2fb44-822">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="2fb44-822">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="2fb44-823">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="2fb44-823">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="2fb44-824">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="2fb44-824">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="2fb44-825">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="2fb44-825">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="2fb44-826">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2fb44-826">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2fb44-827">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2fb44-827">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2fb44-828">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2fb44-828">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2fb44-829">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2fb44-829">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2fb44-830">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2fb44-830">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2fb44-831">[Weitere Informationen](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) zur SQR-API</span><span class="sxs-lookup"><span data-stu-id="2fb44-831">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="2fb44-832">„Az.Monitor.md“ aktualisiert, um Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch) einzuschließen</span><span class="sxs-lookup"><span data-stu-id="2fb44-832">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2fb44-833">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2fb44-833">Az.Network</span></span>
* <span data-ttu-id="2fb44-834">Unterstützung für NAT-Gatewayressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-834">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="2fb44-835">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2fb44-835">New cmdlets</span></span>
        - <span data-ttu-id="2fb44-836">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2fb44-836">New-AzNatGateway</span></span>
        - <span data-ttu-id="2fb44-837">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2fb44-837">Get-AzNatGateway</span></span>
        - <span data-ttu-id="2fb44-838">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2fb44-838">Set-AzNatGateway</span></span>
        - <span data-ttu-id="2fb44-839">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2fb44-839">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="2fb44-840">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2fb44-840">Updated cmdlets</span></span>
        - <span data-ttu-id="2fb44-841">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="2fb44-841">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="2fb44-842">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="2fb44-842">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="2fb44-843">Folgende Befehle für das Feature aktualisiert: Benutzerdefinierte Routen für Brooklyn-Gateway festgelegt/entfernt</span><span class="sxs-lookup"><span data-stu-id="2fb44-843">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="2fb44-844">„New-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="2fb44-844">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="2fb44-845">„Set-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="2fb44-845">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2fb44-846">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2fb44-846">Az.PolicyInsights</span></span>
* <span data-ttu-id="2fb44-847">Unterstützung für die Abfrage von Richtlinienauswertungsdetails</span><span class="sxs-lookup"><span data-stu-id="2fb44-847">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="2fb44-848">Parameter „-Expand“ zu „Get-AzPolicyState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-848">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="2fb44-849">Unterstützung für „-Expand PolicyEvaluationDetails“</span><span class="sxs-lookup"><span data-stu-id="2fb44-849">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2fb44-850">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2fb44-850">Az.RecoveryServices</span></span>
* <span data-ttu-id="2fb44-851">Unterstützung für abonnementübergreifende Azure-zu-Azure-Sitewiederherstellung</span><span class="sxs-lookup"><span data-stu-id="2fb44-851">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="2fb44-852">Markierung anstehender wichtiger Änderungen für Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="2fb44-852">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="2fb44-853">Fehlerbehebung für Azure Site Recovery-Wiederherstellungsplan und -Aktionsplan</span><span class="sxs-lookup"><span data-stu-id="2fb44-853">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="2fb44-854">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Netzwerkzuordnung für Azure zu Azure</span><span class="sxs-lookup"><span data-stu-id="2fb44-854">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="2fb44-855">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Schutzrichtung für Azure zu Azure für verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="2fb44-855">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="2fb44-856">Weitere kleinere Korrekturen</span><span class="sxs-lookup"><span data-stu-id="2fb44-856">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="2fb44-857">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="2fb44-857">Az.Relay</span></span>
* <span data-ttu-id="2fb44-858">Korrektur von Tippfehlern in Kundennachrichten</span><span class="sxs-lookup"><span data-stu-id="2fb44-858">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2fb44-859">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2fb44-859">Az.ServiceBus</span></span>
* <span data-ttu-id="2fb44-860">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-860">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2fb44-861">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2fb44-861">Az.Storage</span></span>
* <span data-ttu-id="2fb44-862">Upgrade auf Speicherclientbibliothek 10.0.1 (Namespace aller Objekte von diesem SDK von „Microsoft.WindowsAzure.Storage. *“ in „Microsoft.Azure.Storage.* “ geändert)</span><span class="sxs-lookup"><span data-stu-id="2fb44-862">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="2fb44-863">Upgrade auf Microsoft.Azure.Management.Storage 11.0.0, um die neue API-Version 2019-04-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="2fb44-863">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="2fb44-864">Art des Standardspeicherkontos bei der Speicherkontoerstellung von „Storage“ in „StorageV2“ geändert</span><span class="sxs-lookup"><span data-stu-id="2fb44-864">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="2fb44-865">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2fb44-865">New-AzStorageAccount</span></span>
* <span data-ttu-id="2fb44-866">Vom Speicherkonto-Cmdlet ausgegebener SKU-Name (Sku.Name) durch Hinzufügen eines Unterstrichs an SKU-Eingabename angepasst (Beispiel: „StandardLRS“ > „Standard_LRS“).</span><span class="sxs-lookup"><span data-stu-id="2fb44-866">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="2fb44-867">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2fb44-867">New-AzStorageAccount</span></span>
    - <span data-ttu-id="2fb44-868">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2fb44-868">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="2fb44-869">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2fb44-869">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2fb44-870">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2fb44-870">Az.Websites</span></span>
* <span data-ttu-id="2fb44-871">Die Eigenschaft „Kind“ wird nun für PSSite-Objekte festgelegt, die von „Get-AzWebApp“ zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2fb44-871">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="2fb44-872">„Get-AzWebApp\*Metrics“ und „Get-AzAppServicePlanMetrics“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-872">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="2fb44-873">1.8.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="2fb44-873">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2fb44-874">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="2fb44-874">Highlights since the last major release</span></span>
* <span data-ttu-id="2fb44-875">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="2fb44-875">General availability of `Az` module</span></span>
* <span data-ttu-id="2fb44-876">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="2fb44-876">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="2fb44-877">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="2fb44-877">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="2fb44-878">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-878">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="2fb44-879">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-879">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2fb44-880">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-880">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="2fb44-881">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="2fb44-881">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2fb44-882">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2fb44-882">Az.Accounts</span></span>
* <span data-ttu-id="2fb44-883">„Uninstall-AzureRm“ aktualisiert, um Module unter Mac ordnungsgemäß zu löschen</span><span class="sxs-lookup"><span data-stu-id="2fb44-883">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="2fb44-884">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2fb44-884">Az.Batch</span></span>
* <span data-ttu-id="2fb44-885">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2fb44-885">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2fb44-886">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2fb44-886">Az.Cdn</span></span>
* <span data-ttu-id="2fb44-887">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2fb44-887">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2fb44-888">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2fb44-888">Az.CognitiveServices</span></span>
* <span data-ttu-id="2fb44-889">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2fb44-889">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2fb44-890">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2fb44-890">Az.Compute</span></span>
* <span data-ttu-id="2fb44-891">Problem mit der AEM-Installation behoben, wenn die Ressourcen-IDs von Datenträgern Ressourcengruppen in Kleinbuchstaben enthielten</span><span class="sxs-lookup"><span data-stu-id="2fb44-891">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="2fb44-892">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2fb44-892">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2fb44-893">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-893">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2fb44-894">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2fb44-894">Az.DataFactory</span></span>
* <span data-ttu-id="2fb44-895">„SsisProperties“ hinzugefügt, falls „NodeCount“ für verwaltete Integration Runtime nicht NULL ist</span><span class="sxs-lookup"><span data-stu-id="2fb44-895">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2fb44-896">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2fb44-896">Az.DataLakeStore</span></span>
* <span data-ttu-id="2fb44-897">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2fb44-897">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2fb44-898">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2fb44-898">Az.EventGrid</span></span>
* <span data-ttu-id="2fb44-899">Hilfetext für Endpunkt aktualisiert, um anzugeben, dass Ressourcen erstellt werden müssen, bevor die Cmdlets zum Erstellen/Aktualisieren von Ereignisabonnements verwendet werden</span><span class="sxs-lookup"><span data-stu-id="2fb44-899">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2fb44-900">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2fb44-900">Az.EventHub</span></span>
* <span data-ttu-id="2fb44-901">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-901">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="2fb44-902">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2fb44-902">Az.HDInsight</span></span>
* <span data-ttu-id="2fb44-903">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2fb44-903">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2fb44-904">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2fb44-904">Az.IotHub</span></span>
* <span data-ttu-id="2fb44-905">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2fb44-905">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2fb44-906">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2fb44-906">Az.KeyVault</span></span>
* <span data-ttu-id="2fb44-907">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2fb44-907">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2fb44-908">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-908">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="2fb44-909">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="2fb44-909">Az.MachineLearning</span></span>
* <span data-ttu-id="2fb44-910">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2fb44-910">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="2fb44-911">Az.Media</span><span class="sxs-lookup"><span data-stu-id="2fb44-911">Az.Media</span></span>
* <span data-ttu-id="2fb44-912">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2fb44-912">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2fb44-913">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2fb44-913">Az.Monitor</span></span>
  * <span data-ttu-id="2fb44-914">Neue Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch)</span><span class="sxs-lookup"><span data-stu-id="2fb44-914">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="2fb44-915">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="2fb44-915">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="2fb44-916">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="2fb44-916">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="2fb44-917">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="2fb44-917">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="2fb44-918">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="2fb44-918">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="2fb44-919">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="2fb44-919">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="2fb44-920">Monitor SDK auf Version 0.22.0-preview aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-920">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2fb44-921">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2fb44-921">Az.Network</span></span>
* <span data-ttu-id="2fb44-922">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2fb44-922">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2fb44-923">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-923">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="2fb44-924">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="2fb44-924">Az.NotificationHubs</span></span>
* <span data-ttu-id="2fb44-925">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2fb44-925">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2fb44-926">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2fb44-926">Az.OperationalInsights</span></span>
* <span data-ttu-id="2fb44-927">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2fb44-927">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="2fb44-928">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="2fb44-928">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="2fb44-929">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2fb44-929">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2fb44-930">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2fb44-930">Az.RecoveryServices</span></span>
* <span data-ttu-id="2fb44-931">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2fb44-931">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2fb44-932">Tabellenformat für SQL auf Azure-VM aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-932">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="2fb44-933">Alternative Methode zum Abrufen des Speicherorts in „AzureFileShare“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-933">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="2fb44-934">„ScheduleRunDays“ in SchedulePolicy-Objekt gemäß Zeitzone aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-934">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="2fb44-935">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2fb44-935">Az.RedisCache</span></span>
* <span data-ttu-id="2fb44-936">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2fb44-936">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2fb44-937">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2fb44-937">Az.Resources</span></span>
* <span data-ttu-id="2fb44-938">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-938">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="2fb44-939">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2fb44-939">Az.Sql</span></span>
* <span data-ttu-id="2fb44-940">Abhängigkeit vom Monitor SDK durch allgemeinen Code ersetzt</span><span class="sxs-lookup"><span data-stu-id="2fb44-940">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="2fb44-941">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2fb44-941">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2fb44-942">Verbesserter Prozess für Klassifizierung mehrerer Spalten</span><span class="sxs-lookup"><span data-stu-id="2fb44-942">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="2fb44-943">SKU-Eigenschaften (SKU-Name, Familie, Kapazität) in Antwort von „Get-AzSqlServerServiceObjective“ aufgenommen und standardmäßig als Tabelle formatiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-943">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="2fb44-944">Möglichkeit zum Ausführen von „Get-AzSqlServerServiceObjective“ nach Standort, ohne dass bereits ein Server in der Region vorhanden sein muss</span><span class="sxs-lookup"><span data-stu-id="2fb44-944">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="2fb44-945">Unterstützung für Zeitzonenparameter bei der Erstellung einer verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="2fb44-945">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="2fb44-946">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-946">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2fb44-947">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2fb44-947">Az.Websites</span></span>
* <span data-ttu-id="2fb44-948">„Set-AzWebApp“ und „Set-AzWebAppSlot“ korrigiert, sodass die Tags bei der Ausführung nicht entfernt werden</span><span class="sxs-lookup"><span data-stu-id="2fb44-948">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="2fb44-949">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2fb44-949">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2fb44-950">WebSites SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-950">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="2fb44-951">AdminSiteName-Eigenschaft aus „PSAppServicePlan“ entfernt</span><span class="sxs-lookup"><span data-stu-id="2fb44-951">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="2fb44-952">1.7.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="2fb44-952">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2fb44-953">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="2fb44-953">Highlights since the last major release</span></span>
* <span data-ttu-id="2fb44-954">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="2fb44-954">General availability of `Az` module</span></span>
* <span data-ttu-id="2fb44-955">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="2fb44-955">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="2fb44-956">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="2fb44-956">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="2fb44-957">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-957">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="2fb44-958">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-958">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2fb44-959">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-959">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="2fb44-960">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="2fb44-960">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2fb44-961">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2fb44-961">Az.Accounts</span></span>
* <span data-ttu-id="2fb44-962">„Add-AzEnvironment“ und „Set-AzEnvironment“ aktualisiert, um den Parameter „AzureAnalysisServicesEndpointResourceId“ zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="2fb44-962">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="2fb44-963">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2fb44-963">Az.AnalysisServices</span></span>
* <span data-ttu-id="2fb44-964">ServiceClient wird in Cmdlets für die Datenebene verwendet, und die ursprüngliche Authentifizierungslogik wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="2fb44-964">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="2fb44-965">„Add-AzureASAccount“ wird als Wrapper von „Connect-AzAccount“ festgelegt, um einen Breaking Change zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="2fb44-965">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2fb44-966">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2fb44-966">Az.Automation</span></span>
* <span data-ttu-id="2fb44-967">Fehler des Cmdlets „Fixed New-AzAutomationSoftwareUpdateConfiguration“ für Einschlüsse behoben.</span><span class="sxs-lookup"><span data-stu-id="2fb44-967">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="2fb44-968">Die Parameter „IncludedKbNumber“ und „IncludedPackageNameMask“ sollten nun funktionieren.</span><span class="sxs-lookup"><span data-stu-id="2fb44-968">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="2fb44-969">Fehlerbehebung für eine dynamische Gruppe der Azure Automation-Updateverwaltung</span><span class="sxs-lookup"><span data-stu-id="2fb44-969">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2fb44-970">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2fb44-970">Az.Compute</span></span>
* <span data-ttu-id="2fb44-971">Parameter „HyperVGeneration“ zu „New-AzDiskConfig“ und „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-971">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="2fb44-972">Zulassen der VM-Erstellung mit einem Katalogimage aus anderen Mandanten</span><span class="sxs-lookup"><span data-stu-id="2fb44-972">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="2fb44-973">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2fb44-973">Az.ContainerInstance</span></span>
* <span data-ttu-id="2fb44-974">Problem im Parameter „-Command“ von „New-AzContainerGroup“ behoben, das dazu führte, dass ein nachgestelltes leeres Argument hinzugefügt wurde</span><span class="sxs-lookup"><span data-stu-id="2fb44-974">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2fb44-975">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2fb44-975">Az.DataFactory</span></span>
* <span data-ttu-id="2fb44-976">Version des ADF .NET SDK auf 3.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-976">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="2fb44-977">Cmdlet „Set-AzDataFactoryV2“ mit zusätzlichen Parametern für RepoConfiguration-Einstellungen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-977">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2fb44-978">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2fb44-978">Az.Resources</span></span>
* <span data-ttu-id="2fb44-979">Verarbeitung von Anbietern für „Get-AzResource“ bei der Angabe der Parameter „-ResourceId“ oder „-ResourceGroupName“, „-Name“ und „-ResourceType“ verbessert</span><span class="sxs-lookup"><span data-stu-id="2fb44-979">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="2fb44-980">Fehlerbehandlung für „Test-AzDeployment“ und „Test-AzResourceGroupDeployment“ verbessert</span><span class="sxs-lookup"><span data-stu-id="2fb44-980">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="2fb44-981">Behandlung von außerhalb der Bereitstellungsüberprüfung aufgetretenen Fehlern und stattdessen Aufnahme in die Ausgabe des Befehls</span><span class="sxs-lookup"><span data-stu-id="2fb44-981">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="2fb44-982">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="2fb44-982">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="2fb44-983">Switch-Parameter „-IgnoreDynamicParameters“ zu Bereitstellungs-Cmdlets hinzugefügt, um Aufforderung in Skript- und Auftragsszenarien zu überspringen</span><span class="sxs-lookup"><span data-stu-id="2fb44-983">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="2fb44-984">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="2fb44-984">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="2fb44-985">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2fb44-985">Az.Sql</span></span>
* <span data-ttu-id="2fb44-986">Unterstützung für Klassifizierung von Datenbankdaten</span><span class="sxs-lookup"><span data-stu-id="2fb44-986">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2fb44-987">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2fb44-987">Az.Storage</span></span>
* <span data-ttu-id="2fb44-988">Melden eines ausführlichen Fehlers beim Erstellen des Storage-Kontexts mit dem Parameter „-UseConnectedAccount“, aber ohne Azure-Anmeldekonto</span><span class="sxs-lookup"><span data-stu-id="2fb44-988">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="2fb44-989">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="2fb44-989">New-AzStorageContext</span></span>
* <span data-ttu-id="2fb44-990">Unterstützung für das Verwalten von Blobdiensteigenschaften eines bestimmten Storage-Kontos mit einer API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="2fb44-990">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="2fb44-991">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="2fb44-991">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="2fb44-992">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="2fb44-992">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="2fb44-993">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2fb44-993">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="2fb44-994">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2fb44-994">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="2fb44-995">Unterstützung von „-AsJob“ für Cmdlets für den Upload und Download von Blobs und Dateien</span><span class="sxs-lookup"><span data-stu-id="2fb44-995">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="2fb44-996">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2fb44-996">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="2fb44-997">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2fb44-997">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="2fb44-998">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2fb44-998">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="2fb44-999">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2fb44-999">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="2fb44-1000">1.6.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="2fb44-1000">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2fb44-1001">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="2fb44-1001">Highlights since the last major release</span></span>
* <span data-ttu-id="2fb44-1002">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="2fb44-1002">General availability of `Az` module</span></span>
* <span data-ttu-id="2fb44-1003">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1003">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="2fb44-1004">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1004">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="2fb44-1005">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1005">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="2fb44-1006">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1006">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2fb44-1007">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1007">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="2fb44-1008">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="2fb44-1008">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2fb44-1009">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2fb44-1009">Az.Automation</span></span>
* <span data-ttu-id="2fb44-1010">Änderung an der Azure Automation-Updateverwaltung, um die folgenden neuen Features zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="2fb44-1010">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="2fb44-1011">Dynamische Gruppierung</span><span class="sxs-lookup"><span data-stu-id="2fb44-1011">Dynamic grouping</span></span>
    * <span data-ttu-id="2fb44-1012">Pre-/Post-Skripts</span><span class="sxs-lookup"><span data-stu-id="2fb44-1012">Pre-Post script</span></span>
    * <span data-ttu-id="2fb44-1013">Neustarteinstellung</span><span class="sxs-lookup"><span data-stu-id="2fb44-1013">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2fb44-1014">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2fb44-1014">Az.Compute</span></span>
* <span data-ttu-id="2fb44-1015">Problem mit der Pfadauflösung in „Get-AzVmBootDiagnosticsData“ behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-1015">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="2fb44-1016">Computeclientbibliothek auf 25.0.0. aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1016">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2fb44-1017">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2fb44-1017">Az.KeyVault</span></span>
* <span data-ttu-id="2fb44-1018">Unterstützung für Platzhalterzeichen zu KeyVault-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1018">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2fb44-1019">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2fb44-1019">Az.Network</span></span>
* <span data-ttu-id="2fb44-1020">Threat Intelligence-Unterstützung für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1020">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="2fb44-1021">Ressource der obersten Ebene für Application Gateway-Firewallrichtlinie und benutzerdefinierte Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1021">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2fb44-1022">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2fb44-1022">Az.RecoveryServices</span></span>
* <span data-ttu-id="2fb44-1023">SnapshotRetentionInDays in Azure-VM-Richtlinie hinzugefügt, um sofortigen Wiederherstellungspunkt zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="2fb44-1023">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="2fb44-1024">Pipe-Unterstützung für das Aufheben der Registrierung eines Containers hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1024">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="2fb44-1025">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2fb44-1025">Az.Resources</span></span>
* <span data-ttu-id="2fb44-1026">Unterstützung für Platzhalterzeichen für Get-AzResource und Get-AzResourceGroup aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1026">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="2fb44-1027">Anmeldeinformationen aktualisiert, die beim Senden generischer Aufrufe an ARM verwendet werden</span><span class="sxs-lookup"><span data-stu-id="2fb44-1027">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="2fb44-1028">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2fb44-1028">Az.Sql</span></span>
* <span data-ttu-id="2fb44-1029">Der Cmdlet-Parameter der Bedrohungserkennung (ExcludeDetectionType) wurde von „DetectionType“ in „string[]“ geändert, um ihn zukunftssicher zu machen, wenn neue DetectionTypes-Elemente hinzugefügt werden, und um AutoVervollständigen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1029">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2fb44-1030">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2fb44-1030">Az.Storage</span></span>
* <span data-ttu-id="2fb44-1031">Unterstützung von Get-/Set-/Remove-Verwaltungsrichtlinien für Speicherkonto hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1031">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="2fb44-1032">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2fb44-1032">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="2fb44-1033">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2fb44-1033">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="2fb44-1034">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2fb44-1034">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="2fb44-1035">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="2fb44-1035">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="2fb44-1036">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="2fb44-1036">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="2fb44-1037">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="2fb44-1037">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2fb44-1038">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2fb44-1038">Az.Websites</span></span>
* <span data-ttu-id="2fb44-1039">ARM-Vorlagenfehler behoben, der zu einem Problem beim Klonen aller Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ führte</span><span class="sxs-lookup"><span data-stu-id="2fb44-1039">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="2fb44-1040">1.5.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="2fb44-1040">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2fb44-1041">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2fb44-1041">Az.Accounts</span></span>
* <span data-ttu-id="2fb44-1042">Der Befehl „Register-AzModule“ wurde hinzugefügt, um von AutoRest generierte Cmdlets zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1042">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="2fb44-1043">Beispiele für „Connect-AzAccount“ wurden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1043">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2fb44-1044">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2fb44-1044">Az.Automation</span></span>
* <span data-ttu-id="2fb44-1045">Problem behoben, das beim Abrufen bestimmter monatlicher Zeitpläne in verschiedenen Azure Automation-Cmdlets auftrat</span><span class="sxs-lookup"><span data-stu-id="2fb44-1045">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="2fb44-1046">„Get-AzAutomationDscNode“ wurde korrigiert, da nur die 20 obersten Knoten zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1046">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="2fb44-1047">Jetzt werden alle Knoten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1047">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2fb44-1048">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2fb44-1048">Az.Cdn</span></span>
* <span data-ttu-id="2fb44-1049">Neue Powershell-Cmdlets zum Aktivieren/Deaktivieren von HTTPS für benutzerdefinierte Domänen hinzugefügt und alte Cmdlets außer Betrieb genommen</span><span class="sxs-lookup"><span data-stu-id="2fb44-1049">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2fb44-1050">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2fb44-1050">Az.Compute</span></span>
* <span data-ttu-id="2fb44-1051">Unterstützung für Platzhalterzeichen zu Get-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1051">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2fb44-1052">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2fb44-1052">Az.DataFactory</span></span>
* <span data-ttu-id="2fb44-1053">Version des ADF .NET SDK auf 3.0.1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1053">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2fb44-1054">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2fb44-1054">Az.LogicApp</span></span>
* <span data-ttu-id="2fb44-1055">„ListWorkflows“ wurde korrigiert, da nur die erste Seite mit Ergebnissen abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1055">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2fb44-1056">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2fb44-1056">Az.Network</span></span>
* <span data-ttu-id="2fb44-1057">Unterstützung für Platzhalterzeichen zu Network-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1057">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2fb44-1058">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2fb44-1058">Az.RecoveryServices</span></span>
* <span data-ttu-id="2fb44-1059">SQL Server jetzt in Azure-VM-Support enthalten</span><span class="sxs-lookup"><span data-stu-id="2fb44-1059">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="2fb44-1060">SDK-Update</span><span class="sxs-lookup"><span data-stu-id="2fb44-1060">SDK Update</span></span>
* <span data-ttu-id="2fb44-1061">VMappContainer-Überprüfung in „Get-ProtectableItem“ entfernt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1061">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="2fb44-1062">„Name“ und „ServerName“ als Parameter für „Get-ProtectableItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1062">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="2fb44-1063">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2fb44-1063">Az.Resources</span></span>
* <span data-ttu-id="2fb44-1064">Parameter `-TemplateObject` zu Bereitstellungs-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1064">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="2fb44-1065">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="2fb44-1065">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="2fb44-1066">Problem beim Piping des Ergebnisses von `Get-AzResource` an `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-1066">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="2fb44-1067">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="2fb44-1067">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="2fb44-1068">Problem mit JSON-Datentypänderung beim Ausführen von `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-1068">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="2fb44-1069">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="2fb44-1069">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="2fb44-1070">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2fb44-1070">Az.Sql</span></span>
* <span data-ttu-id="2fb44-1071">„AuditingEndpointsCommunicator“ wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1071">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="2fb44-1072">Das Verhalten eines Grenzfalls beim Erstellen neuer Diagnoseeinstellungen wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1072">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2fb44-1073">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2fb44-1073">Az.Storage</span></span>
* <span data-ttu-id="2fb44-1074">Unterstützung von „Kind BlockBlobStorage“ beim Erstellen eines Speicherkontos: New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2fb44-1074">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="2fb44-1075">1.4.0 – Februar 2019</span><span class="sxs-lookup"><span data-stu-id="2fb44-1075">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="2fb44-1076">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2fb44-1076">Az.AnalysisServices</span></span>
* <span data-ttu-id="2fb44-1077">Cmdlet „AddAzureASAccount“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1077">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2fb44-1078">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2fb44-1078">Az.Automation</span></span>
* <span data-ttu-id="2fb44-1079">Hilfe für „Import-AzAutomationDscNodeConfiguration“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1079">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="2fb44-1080">Überprüfung des Konfigurationsnamens zu Cmdlet „Import-AzAutomationDscConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1080">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="2fb44-1081">Fehlerbehandlung für Cmdlet „Import-AzAutomationDscConfiguration“ verbessert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1081">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2fb44-1082">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2fb44-1082">Az.CognitiveServices</span></span>
* <span data-ttu-id="2fb44-1083">„CustomSubdomainName“ als neuer optionaler Parameter für Cmdlet „New-AzCognitiveServicesAccount“ hinzugefügt, das zum Angeben der Unterdomäne für die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1083">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2fb44-1084">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2fb44-1084">Az.Compute</span></span>
* <span data-ttu-id="2fb44-1085">Problem mit ID-Parametersätzen behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-1085">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="2fb44-1086">„Get-AzVMExtension“ aktualisiert, sodass alle installierten Erweiterungen aufgelistet werden, wenn der Name-Parameter nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="2fb44-1086">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="2fb44-1087">Parameter „Tag“ und „ResourceId“ zum Cmdlet „Update-AzImage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1087">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="2fb44-1088">„Get-AzVmssVM“ ohne Instanz-ID und mit „InstanceView“ können virtuelle VMSS-Computer mit Instanzansicht auflisten.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1088">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2fb44-1089">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2fb44-1089">Az.DataLakeStore</span></span>
* <span data-ttu-id="2fb44-1090">Cmdlets zum Auflisten und Wiederherstellen gelöschter ADL-Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1090">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2fb44-1091">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2fb44-1091">Az.EventHub</span></span>
* <span data-ttu-id="2fb44-1092">Neue boolesche Eigenschaft „SkipEmptyArchives“ zum Überspringen leerer Archive in Klasse „CaptureDescription“ von EventHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1092">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="2fb44-1093">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2fb44-1093">Az.KeyVault</span></span>
* <span data-ttu-id="2fb44-1094">Kennzeichnung in „Set-AzKeyVaultSecret“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1094">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2fb44-1095">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2fb44-1095">Az.LogicApp</span></span>
* <span data-ttu-id="2fb44-1096">SKU „Basic“ für Integrationskonten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1096">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="2fb44-1097">XSLT 2.0, XSLT 3.0 und Liquid-Zuordnungstypen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1097">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="2fb44-1098">Neue Cmdlets für Integrationskonto-Assemblys</span><span class="sxs-lookup"><span data-stu-id="2fb44-1098">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="2fb44-1099">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2fb44-1099">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="2fb44-1100">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2fb44-1100">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="2fb44-1101">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2fb44-1101">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="2fb44-1102">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2fb44-1102">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="2fb44-1103">Neue Cmdlets für Integrationskonto-Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="2fb44-1103">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="2fb44-1104">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fb44-1104">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="2fb44-1105">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fb44-1105">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="2fb44-1106">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fb44-1106">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="2fb44-1107">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fb44-1107">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="2fb44-1108">Logik-App-SDK auf Version 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1108">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2fb44-1109">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2fb44-1109">Az.Monitor</span></span>
* <span data-ttu-id="2fb44-1110">Hilfe für „Get-AzMetric“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1110">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2fb44-1111">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2fb44-1111">Az.Network</span></span>
* <span data-ttu-id="2fb44-1112">Hilfebeispiel für „Add-AzApplicationGatewayCustomError“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1112">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2fb44-1113">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2fb44-1113">Az.OperationalInsights</span></span>
* <span data-ttu-id="2fb44-1114">Zusätzliche Unterstützung für Datenquelle von „New-ApplicationInsights“ und „Get-ApplicationInsights“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1114">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="2fb44-1115">Neue Art von „ApplicationInsights“ zum Abrufen von bestimmten und von allen ApplicationInsights-Datenquellen für einen Workspace hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1115">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="2fb44-1116">Cmdlet „New-AzOperationalInsightsApplicationInsightsDataSource“ zum Erstellen einer Datenquelle anhand des angegebenen Ressourcenparameters für „Application-Insights“ hinzugefügt: „subscriptionId“, „resourceGroupName“ und „name“.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1116">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="2fb44-1117">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2fb44-1117">Az.Resources</span></span>
* <span data-ttu-id="2fb44-1118">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="2fb44-1118">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="2fb44-1119">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="2fb44-1119">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="2fb44-1120">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="2fb44-1120">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="2fb44-1121">Fehler korrigiert, der die wiederholte Erstellung von „KeyCredentials“ verhindert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1121">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="2fb44-1122">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2fb44-1122">Az.Sql</span></span>
* <span data-ttu-id="2fb44-1123">Unterstützung für SQL DB Hyperscale-Tarif hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1123">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="2fb44-1124">Fehler korrigiert, aufgrund dessen die Wiederherstellung wegen der Festlegung unnötiger Eigenschaften in der Wiederherstellungsanforderung fehlschlagen konnte</span><span class="sxs-lookup"><span data-stu-id="2fb44-1124">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2fb44-1125">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2fb44-1125">Az.Websites</span></span>
* <span data-ttu-id="2fb44-1126">Beispiel in „Get-AzWebAppSlotMetrics“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1126">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="2fb44-1127">1.3.0: Februar 2019</span><span class="sxs-lookup"><span data-stu-id="2fb44-1127">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2fb44-1128">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2fb44-1128">Az.Accounts</span></span>
* <span data-ttu-id="2fb44-1129">Update auf die aktuelle Version von ClientRuntime durchgeführt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1129">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="2fb44-1130">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2fb44-1130">Az.AnalysisServices</span></span>
<span data-ttu-id="2fb44-1131">Allgemeine Verfügbarkeit für Az.AnalysisServices-Modul</span><span class="sxs-lookup"><span data-stu-id="2fb44-1131">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2fb44-1132">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2fb44-1132">Az.Compute</span></span>
* <span data-ttu-id="2fb44-1133">AEM-Erweiterung: Unterstützung für UltraSSD und P60-, P70- und P80-Datenträger hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1133">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="2fb44-1134">Hilfebeschreibung für „Set-AzVMBootDiagnostics“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1134">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="2fb44-1135">Hilfebeschreibung und Beispiel für „Update-AzImage“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1135">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2fb44-1136">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2fb44-1136">Az.RecoveryServices</span></span>
<span data-ttu-id="2fb44-1137">Allgemeine Verfügbarkeit für Az.RecoveryServices-Modul.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1137">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2fb44-1138">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2fb44-1138">Az.Resources</span></span>
* <span data-ttu-id="2fb44-1139">Kennzeichnung für Ressourcengruppen korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1139">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="2fb44-1140">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="2fb44-1140">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="2fb44-1141">Problem behoben, bei dem „-ErrorAction“ von `Get-AzureRmRoleAssignment` nicht berücksichtigt wird</span><span class="sxs-lookup"><span data-stu-id="2fb44-1141">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="2fb44-1142">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="2fb44-1142">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="2fb44-1143">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2fb44-1143">Az.Sql</span></span>
* <span data-ttu-id="2fb44-1144">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1144">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="2fb44-1145">Problem behoben, bei dem eine fehlende Anmeldung am Azure-Konto bei der Ausführung von SQL-Cmdlets zu einer nullref-Ausnahme führt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1145">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="2fb44-1146">nullref-Ausnahme in Get-AzSqlCapability korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1146">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="2fb44-1147">1.2.1: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="2fb44-1147">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2fb44-1148">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2fb44-1148">Az.Accounts</span></span>
* <span data-ttu-id="2fb44-1149">Release mit richtiger Version der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="2fb44-1149">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="2fb44-1150">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2fb44-1150">Az.AnalysisServices</span></span>
* <span data-ttu-id="2fb44-1151">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="2fb44-1151">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2fb44-1152">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2fb44-1152">Az.RecoveryServices</span></span>
* <span data-ttu-id="2fb44-1153">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="2fb44-1153">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="2fb44-1154">1.2.0: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="2fb44-1154">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2fb44-1155">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2fb44-1155">Az.Accounts</span></span>
* <span data-ttu-id="2fb44-1156">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1156">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2fb44-1157">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1157">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2fb44-1158">Warnmeldung in PS Core für „Uninstall-AzureRm“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1158">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="2fb44-1159">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="2fb44-1159">Az.Aks</span></span>
* <span data-ttu-id="2fb44-1160">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1160">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2fb44-1161">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2fb44-1161">Az.Automation</span></span>
* <span data-ttu-id="2fb44-1162">Unterstützung für Python 2-Runbooks hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1162">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="2fb44-1163">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1163">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2fb44-1164">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2fb44-1164">Az.Cdn</span></span>
* <span data-ttu-id="2fb44-1165">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1165">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2fb44-1166">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2fb44-1166">Az.Compute</span></span>
* <span data-ttu-id="2fb44-1167">Cmdlet „Invoke-AzVMReimage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1167">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="2fb44-1168">Parameter „TempDisk“ zu „Set-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1168">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="2fb44-1169">Warnmeldung von „New-AzVM“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1169">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="2fb44-1170">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2fb44-1170">Az.ContainerRegistry</span></span>
* <span data-ttu-id="2fb44-1171">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1171">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2fb44-1172">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2fb44-1172">Az.DataFactory</span></span>
* <span data-ttu-id="2fb44-1173">Version des ADF .NET SDK auf 3.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1173">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2fb44-1174">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2fb44-1174">Az.DataLakeStore</span></span>
* <span data-ttu-id="2fb44-1175">Problem mit ADLS-Endpunkt bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-1175">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="2fb44-1176">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="2fb44-1176">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="2fb44-1177">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1177">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2fb44-1178">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2fb44-1178">Az.IotHub</span></span>
* <span data-ttu-id="2fb44-1179">Codierungsformat zu Cmdlet „Add-IotHubRoutingEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1179">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2fb44-1180">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2fb44-1180">Az.KeyVault</span></span>
* <span data-ttu-id="2fb44-1181">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1181">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2fb44-1182">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2fb44-1182">Az.Network</span></span>
* <span data-ttu-id="2fb44-1183">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1183">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="2fb44-1184">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2fb44-1184">Az.Resources</span></span>
* <span data-ttu-id="2fb44-1185">Fehlerhafte Beispiele in Referenzdokumentation zu „New-AzADAppCredential“ und „New-AzADSpCredential“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1185">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="2fb44-1186">Problem behoben, bei dem der Pfad für den Parameter „-TemplateFile“ nicht aufgelöst wurde, bevor Cmdlets für die Bereitstellung von Ressourcengruppen ausgeführt wurden</span><span class="sxs-lookup"><span data-stu-id="2fb44-1186">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="2fb44-1187">Az.Resources: Richtige Dokumentation für Standardwert von „New-AzureRmPolicyDefinition -Mode“ bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1187">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="2fb44-1188">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="2fb44-1188">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="2fb44-1189">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="2fb44-1189">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="2fb44-1190">Formatierungsproblem für Objekt „PSResourceGroupDeployment“ behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-1190">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="2fb44-1191">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="2fb44-1191">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2fb44-1192">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2fb44-1192">Az.ServiceFabric</span></span>
* <span data-ttu-id="2fb44-1193">Rollback beim Hinzufügen eines Zertifikats zum VMSS-Modell, Auslösung einer Ausnahme. Fehlerbehebung: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="2fb44-1193">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="2fb44-1194">Einige Fehlermeldungen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1194">Fix some error messages.</span></span>
* <span data-ttu-id="2fb44-1195">Fehler bei Clustererstellung mit ARM-Standardvorlage für „New-AzServiceFabriCluster“ behoben, bei dem die Migration zu Az nicht funktioniert hat.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1195">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="2fb44-1196">Fehler behoben beim Hinzufügen eines Cluster-/Anwendungszertifikats ausschließlich zu VM Scale Sets, die zum Cluster gehören, indem die Cluster-ID in der Erweiterung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1196">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="2fb44-1197">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="2fb44-1197">Az.SignalR</span></span>
* <span data-ttu-id="2fb44-1198">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1198">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="2fb44-1199">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2fb44-1199">Az.Sql</span></span>
* <span data-ttu-id="2fb44-1200">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1200">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2fb44-1201">Parameterbeschreibung für den Parameter „LicenseType“ mit möglichen Werten aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1201">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="2fb44-1202">Fehler behoben, bei dem die Aktualisierung der Identität der verwalteten Instanz nicht funktioniert hat, wenn es sich um die einzige aktualisierte Eigenschaft gehandelt hat</span><span class="sxs-lookup"><span data-stu-id="2fb44-1202">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="2fb44-1203">Unterstützung für die benutzerdefinierte Sortierung auf verwalteter Instanz</span><span class="sxs-lookup"><span data-stu-id="2fb44-1203">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2fb44-1204">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2fb44-1204">Az.Storage</span></span>
* <span data-ttu-id="2fb44-1205">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1205">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2fb44-1206">Ausführliche Fehlermeldung beim Abrufen/Festlegen der klassischen Protokollierung bzw. Metriken für Storage Premium-Konto, da für das Storage Premium-Konto die klassische Protokollierung bzw. Metriken nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1206">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="2fb44-1207">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="2fb44-1207">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="2fb44-1208">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="2fb44-1208">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="2fb44-1209">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="2fb44-1209">Az.TrafficManager</span></span>
* <span data-ttu-id="2fb44-1210">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1210">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2fb44-1211">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2fb44-1211">Az.Websites</span></span>
* <span data-ttu-id="2fb44-1212">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1212">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2fb44-1213">„New-AzWebAppSSLBinding“ korrigiert, damit das Zertifikat in die richtige Ressourcengruppe bzw. an den richtigen Speicherort hochgeladen wird, wenn die App in einer ASE gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1213">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="2fb44-1214">„New-AzWebAppSSLBinding“ korrigiert, damit die Tags beim Binden eines SSL-Zertifikats an eine App nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1214">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="2fb44-1215">1.1.0 – Januar 2019</span><span class="sxs-lookup"><span data-stu-id="2fb44-1215">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2fb44-1216">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2fb44-1216">Az.Accounts</span></span>
* <span data-ttu-id="2fb44-1217">Bereich „Local“ zu „Enable-AzureRmAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1217">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2fb44-1218">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2fb44-1218">Az.Compute</span></span>
* <span data-ttu-id="2fb44-1219">Name ist jetzt optional im ID-Parametersatz für „Restart/Start/Stop/Remove/Set-AzVM“ und „Save-AzVMImage“</span><span class="sxs-lookup"><span data-stu-id="2fb44-1219">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="2fb44-1220">Beschreibung der ID in Hilfedateien aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1220">Updated the description of ID in help files</span></span>
* <span data-ttu-id="2fb44-1221">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-1221">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2fb44-1222">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2fb44-1222">Az.DataLakeStore</span></span>
* <span data-ttu-id="2fb44-1223">Aktualisierung der SDK-Version der Datenebene auf 1.1.14 für SDK-Fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1223">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="2fb44-1224">Behandlung von negativen acesstime- and modificationtime-Werten für „getfilestatus“ und „liststatus“ korrigiert, asynchrones Abbruchtoken korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1224">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2fb44-1225">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2fb44-1225">Az.EventGrid</span></span>
* <span data-ttu-id="2fb44-1226">Zur Verwendung der API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1226">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="2fb44-1227">Aktualisierung der folgenden Cmdlets zur Unterstützung des neuen Szenarios in der API-Version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="2fb44-1227">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="2fb44-1228">New-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="2fb44-1228">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="2fb44-1229">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="2fb44-1229">Event Time-To-Live,</span></span>
        - <span data-ttu-id="2fb44-1230">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="2fb44-1230">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="2fb44-1231">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="2fb44-1231">Dead letter endpoint.</span></span>
    - <span data-ttu-id="2fb44-1232">Update-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="2fb44-1232">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="2fb44-1233">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="2fb44-1233">Event Time-To-Live,</span></span>
        - <span data-ttu-id="2fb44-1234">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="2fb44-1234">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="2fb44-1235">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="2fb44-1235">Dead letter endpoint.</span></span>
* <span data-ttu-id="2fb44-1236">Neue Enumerationswerte („storageQueue“ und „hybridConnection“) für die EndpointType-Option in den Cmdlets „New-AzureRmEventGridSubscription“ und „Update-AzureRmEventGridSubscription“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1236">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="2fb44-1237">Anzeige einer Warnmeldung, wenn das Erstellen oder Aktualisieren des Ereignisabonnements voraussichtlich eine manuelle Aktion des Benutzers zur Folge hat</span><span class="sxs-lookup"><span data-stu-id="2fb44-1237">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2fb44-1238">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2fb44-1238">Az.IotHub</span></span>
* <span data-ttu-id="2fb44-1239">Auf die aktuelle Version des Iot Hub SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1239">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2fb44-1240">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2fb44-1240">Az.LogicApp</span></span>
* <span data-ttu-id="2fb44-1241">„Get-AzLogicApp“ listet alle Apps ohne angegebenen Namen auf</span><span class="sxs-lookup"><span data-stu-id="2fb44-1241">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="2fb44-1242">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2fb44-1242">Az.Resources</span></span>
* <span data-ttu-id="2fb44-1243">Problem mit dem Parametersatz bei Angabe der Parameter „-ODataQuery“ und „-ResourceId“ für „Get-AzResource“ behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-1243">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="2fb44-1244">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="2fb44-1244">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="2fb44-1245">Behandlung des Parameters „-Custom“ in „New/Set-AzPolicyDefinition“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1245">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="2fb44-1246">Tippfehler in der Dokumentation für „New-AzDeployment“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1246">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="2fb44-1247">Parameter „-MailNickname“ als obligatorisch festgelegt für „New-AzADUser“</span><span class="sxs-lookup"><span data-stu-id="2fb44-1247">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="2fb44-1248">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="2fb44-1248">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="2fb44-1249">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="2fb44-1249">Az.SignalR</span></span>
* <span data-ttu-id="2fb44-1250">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-1250">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="2fb44-1251">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2fb44-1251">Az.Sql</span></span>
* <span data-ttu-id="2fb44-1252">Abhängigkeit des Speicherverwaltungsclients zur allgemeinen SDK-Implementierung konvertiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1252">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2fb44-1253">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2fb44-1253">Az.Storage</span></span>
* <span data-ttu-id="2fb44-1254">Festlegung des „StorageAccountName“ des Speicherkontexts als tatsächlichen Namen des Speicherkontos, wenn dieser mit „SAS-Token“, „OAuth“ oder „Anonym“ erstellt wird</span><span class="sxs-lookup"><span data-stu-id="2fb44-1254">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="2fb44-1255">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="2fb44-1255">New-AzStorageContext</span></span>
* <span data-ttu-id="2fb44-1256">Erstellen von SAS-Token des Blob-Momentaufnahmeobjekts mit dem Parameter „-FullUri“, Festlegung des zurückgegebenen URI als Momentaufnahme-URI</span><span class="sxs-lookup"><span data-stu-id="2fb44-1256">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="2fb44-1257">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="2fb44-1257">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2fb44-1258">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2fb44-1258">Az.Websites</span></span>
* <span data-ttu-id="2fb44-1259">Fehler bei der Datumsanalyse in „Get-AzDeletedWebApp“ behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-1259">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="2fb44-1260">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-1260">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="2fb44-1261">1.0.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="2fb44-1261">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="2fb44-1262">Allgemein</span><span class="sxs-lookup"><span data-stu-id="2fb44-1262">General</span></span>

- <span data-ttu-id="2fb44-1263">Allgemeine Verfügbarkeit des Az-Moduls</span><span class="sxs-lookup"><span data-stu-id="2fb44-1263">General Availability of Az Module</span></span>
- <span data-ttu-id="2fb44-1264">Onlinehilfe für jedes Modul</span><span class="sxs-lookup"><span data-stu-id="2fb44-1264">Online help for each module</span></span>
- <span data-ttu-id="2fb44-1265">Ausführlichere Informationen und eine Roadmap finden Sie auf der [Seite mit der Ankündigung zu Az](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="2fb44-1265">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="2fb44-1266">Informationen zur Migration aus AzureRM finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="2fb44-1266">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="2fb44-1267">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2fb44-1267">Az.Accounts</span></span>
- <span data-ttu-id="2fb44-1268">Geändert von Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2fb44-1268">Changed from Az.Profile</span></span>
- <span data-ttu-id="2fb44-1269">Feste Tabellenformate für Profil- und Kontexttypen</span><span class="sxs-lookup"><span data-stu-id="2fb44-1269">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="2fb44-1270">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2fb44-1270">Az.ApiManagement</span></span>
- <span data-ttu-id="2fb44-1271">Korrekturen für #7002</span><span class="sxs-lookup"><span data-stu-id="2fb44-1271">Fixes for #7002</span></span>
- <span data-ttu-id="2fb44-1272">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="2fb44-1272">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="2fb44-1273">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2fb44-1273">Az.Batch</span></span>
- <span data-ttu-id="2fb44-1274">Möglichkeit zum Anzeigen der ausgeführten Version des Azure Batch-Knoten-Agents auf den VMs eines Pools mit der neuen `NodeAgentInformation`-Eigenschaft für `PSComputeNode` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1274">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="2fb44-1275">Der `Caching`-Standardwert für `PSDataDisk` lautet jetzt nicht mehr `None`, sondern `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1275">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="2fb44-1276">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="2fb44-1276">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="2fb44-1277">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="2fb44-1277">Az.Billing</span></span>
- <span data-ttu-id="2fb44-1278">Kombination von Billing-, Consumption- und UsageAggregates-Cmdlets. Ausführliche Informationen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="2fb44-1278">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="2fb44-1279">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="2fb44-1279">Az.CognitivServices</span></span>
- <span data-ttu-id="2fb44-1280">Vervollständigungen für SkuName und Typem für den Vorgang New-AzureRmCognitiveServicesAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1280">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="2fb44-1281">GetSkusWithAccountParamSetName-Parametersatz aus Get-AzCognitiveServicesAccountSkus entfernt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1281">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="2fb44-1282">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2fb44-1282">Az.ContainerInstance</span></span>
- <span data-ttu-id="2fb44-1283">ManagedIdentity-Unterstützung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1283">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="2fb44-1284">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="2fb44-1284">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="2fb44-1285">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="2fb44-1285">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="2fb44-1286">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2fb44-1286">Az.DataLakeStore</span></span>
- <span data-ttu-id="2fb44-1287">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="2fb44-1287">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="2fb44-1288">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2fb44-1288">Az.Monitor</span></span>
- <span data-ttu-id="2fb44-1289">Az.Insights in Az.Monitor umbenannt und weitere weniger wichtige grundlegende Änderungen durchgeführt. Informationen hierzu finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="2fb44-1289">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="2fb44-1290">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2fb44-1290">Az.KeyVault</span></span>
- <span data-ttu-id="2fb44-1291">Veraltete PurgeDisabled-Eigenschaft aus Ausgabetypen entfernt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1291">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="2fb44-1292">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="2fb44-1292">Az.MachineLearning</span></span>
- <span data-ttu-id="2fb44-1293">Cmdlets des Az.MachineLearningCompute-Moduls eingebunden</span><span class="sxs-lookup"><span data-stu-id="2fb44-1293">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="2fb44-1294">Az.Media</span><span class="sxs-lookup"><span data-stu-id="2fb44-1294">Az.Media</span></span>
- <span data-ttu-id="2fb44-1295">Veralteten -Tags-Alias aus New-AzMediaService entfernt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1295">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="2fb44-1296">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2fb44-1296">Az.Network</span></span>
<span data-ttu-id="2fb44-1297">Unterstützung für das Konfigurieren von RewriteRuleSets im Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1297">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="2fb44-1298">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="2fb44-1298">New cmdlets added:</span></span>
        - <span data-ttu-id="2fb44-1299">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2fb44-1299">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2fb44-1300">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2fb44-1300">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2fb44-1301">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2fb44-1301">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2fb44-1302">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2fb44-1302">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2fb44-1303">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2fb44-1303">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2fb44-1304">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="2fb44-1304">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="2fb44-1305">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="2fb44-1305">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="2fb44-1306">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fb44-1306">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="2fb44-1307">Cmdlets mit optionalem Parameter -RewriteRuleSet aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1307">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="2fb44-1308">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2fb44-1308">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="2fb44-1309">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2fb44-1309">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="2fb44-1310">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2fb44-1310">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="2fb44-1311">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2fb44-1311">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="2fb44-1312">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2fb44-1312">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="2fb44-1313">New-AzureRmApplicationGatewayUrlPathMapConfig: KeyVault-Unterstützung mithilfe von Identität zum Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1313">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="2fb44-1314">Cmdlets mit optionalem Parameter aktualisiert: -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2fb44-1314">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="2fb44-1315">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2fb44-1315">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="2fb44-1316">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2fb44-1316">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="2fb44-1317">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2fb44-1317">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="2fb44-1318">Cmdlet New-AzApplicationGateway mit optionalem Parameter -UserAssignedIdentity aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1318">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="2fb44-1319">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="2fb44-1319">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="2fb44-1320">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2fb44-1320">Az.OperationalInsights</span></span>
- <span data-ttu-id="2fb44-1321">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="2fb44-1321">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="2fb44-1322">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2fb44-1322">Az.Profile</span></span>
- <span data-ttu-id="2fb44-1323">Modulnamen in Az.Accounts geändert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1323">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="2fb44-1324">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2fb44-1324">Az.RecoveryServices</span></span>
- <span data-ttu-id="2fb44-1325">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="2fb44-1325">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="2fb44-1326">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2fb44-1326">Az.Resources</span></span>
- <span data-ttu-id="2fb44-1327">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="2fb44-1327">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="2fb44-1328">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2fb44-1328">Az.ServiceFabric</span></span>
- <span data-ttu-id="2fb44-1329">Unterstützung für das Angeben des Zertifikats anhand des allgemeinen Namens und Fingerabdrucks</span><span class="sxs-lookup"><span data-stu-id="2fb44-1329">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="2fb44-1330">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="2fb44-1330">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="2fb44-1331">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="2fb44-1331">Az.SIgnalR</span></span>
- <span data-ttu-id="2fb44-1332">Allgemeine Verfügbarkeit für PowerShell-Cmdlets für SIgnalR</span><span class="sxs-lookup"><span data-stu-id="2fb44-1332">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="2fb44-1333">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2fb44-1333">Az.Sql</span></span>
- <span data-ttu-id="2fb44-1334">Neue Erkennungstypen Data_Exfiltration und Unsafe_Action zu Cmdlets für Bedrohungserkennung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1334">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="2fb44-1335">Dokumentationsbeispiele für Cmdlets für SQL-Überwachung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1335">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="2fb44-1336">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="2fb44-1336">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="2fb44-1337">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2fb44-1337">Az.Storage</span></span>
- <span data-ttu-id="2fb44-1338">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="2fb44-1338">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="2fb44-1339">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2fb44-1339">Az.Websites</span></span>
- <span data-ttu-id="2fb44-1340">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="2fb44-1340">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="2fb44-1341">0.7.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="2fb44-1341">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="2fb44-1342">Allgemein</span><span class="sxs-lookup"><span data-stu-id="2fb44-1342">General</span></span>

* <span data-ttu-id="2fb44-1343">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="2fb44-1343">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="2fb44-1344">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2fb44-1344">Az.Compute</span></span>

* <span data-ttu-id="2fb44-1345">Unterstützung für UltraSSD und Katalogimages in einfachen Parametersätzen für `New-AzVm(ss)`-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1345">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="2fb44-1346">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2fb44-1346">Az.DataLakeStore</span></span>

* <span data-ttu-id="2fb44-1347">Nachgestellten Schrägstrich für die Domäne des ADLS-Kontos korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1347">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="2fb44-1348">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2fb44-1348">Az.FrontDoor</span></span>

* <span data-ttu-id="2fb44-1349">Einige fehlerhafte Links behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-1349">Fixed some broken links</span></span>
    - <span data-ttu-id="2fb44-1350">In den Artikeln zu New-AzureRmFrontDoor und Set-AzureRmFrontDoor den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorHealthProbeSettingObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1350">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="2fb44-1351">Im Artikel zu New-AzureRmFrontDoorManagedRuleObject den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorRuleGroupOverrideObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1351">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="2fb44-1352">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2fb44-1352">Az.RecoveryServices</span></span>

* <span data-ttu-id="2fb44-1353">Clientseitige Validierungen für Wiederherstellungsvorgänge von Azure-Dateifreigaben hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1353">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="2fb44-1354">storageAccountName und storageAccountResourceGroupName für AFS-Wiederherstellung optional gemacht.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1354">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="2fb44-1355">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2fb44-1355">Az.Resources</span></span>

* <span data-ttu-id="2fb44-1356">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="2fb44-1356">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="2fb44-1357">Get-AzureRmRoleAssignment für die Verwendung des Abonnementbereichs aktualisiert, wenn dieser beim Anfordern von klassischen Administratoren angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1357">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="2fb44-1358">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2fb44-1358">Az.Sql</span></span>

* <span data-ttu-id="2fb44-1359">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="2fb44-1359">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="2fb44-1360">Problem mit der Verwendung von Get-AzureRmSqlDatabaseVulnerabilityAssessment mit .NET Core behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-1360">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="2fb44-1361">Dokumentation mit Hilfemeldungen zu Cmdlets für die SQL-Überwachung geändert.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1361">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="2fb44-1362">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2fb44-1362">Az.Storage</span></span>

* <span data-ttu-id="2fb44-1363">-EnableHierarchicalNamespace zu New-AzureRmStorageAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1363">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="2fb44-1364">Problem behoben, bei dem für das Copy File-Cmdlet am Ziel kein Quellkontext wiederverwendet werden kann, wenn -DestContext nicht eingegeben wird</span><span class="sxs-lookup"><span data-stu-id="2fb44-1364">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="2fb44-1365">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="2fb44-1365">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="2fb44-1366">Unterstützung der Konfiguration von statischen Websites</span><span class="sxs-lookup"><span data-stu-id="2fb44-1366">Support Static Website configuration</span></span>
    - <span data-ttu-id="2fb44-1367">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="2fb44-1367">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="2fb44-1368">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="2fb44-1368">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="2fb44-1369">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2fb44-1369">Az.Websites</span></span>

* <span data-ttu-id="2fb44-1370">Set-AzureRmWebApp und Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2fb44-1370">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="2fb44-1371">Neuen Parameter (-AzureStoragePath) zum Angeben von Azure Storage-Pfaden hinzugefügt, die in Windows- und Linux-Container-Apps bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1371">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="2fb44-1372">Verwenden Sie die Ausgabe des neuen Cmdlets New-AzureRmWebAppAzureStoragePath als Parameter zum Festlegen der Azure Storage-Pfade.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1372">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="2fb44-1373">0.6.1 – November 2018</span><span class="sxs-lookup"><span data-stu-id="2fb44-1373">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="2fb44-1374">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2fb44-1374">Az.ApiManagement</span></span>
* <span data-ttu-id="2fb44-1375">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1375">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="2fb44-1376">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2fb44-1376">Az.Automation</span></span>
* <span data-ttu-id="2fb44-1377">Swagger-basierte Azure Automation-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2fb44-1377">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="2fb44-1378">Cmdlets zur Updateverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1378">Added Update Management cmdlets</span></span>
* <span data-ttu-id="2fb44-1379">Cmdlets zur Quellcodeverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1379">Added Source Control cmdlets</span></span>
* <span data-ttu-id="2fb44-1380">Cmdlet „Remove-AzureRmAutomationHybridWorkerGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1380">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="2fb44-1381">DSC-Befehl für die Knotenregistrierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1381">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="2fb44-1382">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2fb44-1382">Az.Compute</span></span>
* <span data-ttu-id="2fb44-1383">Identitätsproblem für SystemAssigned-Identität korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1383">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="2fb44-1384">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1384">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="2fb44-1385">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2fb44-1385">Az.ContainerInstance</span></span>
* <span data-ttu-id="2fb44-1386">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1386">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="2fb44-1387">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="2fb44-1387">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="2fb44-1388">Beschreibung der Beispiele für Marketplace-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1388">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="2fb44-1389">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2fb44-1389">Az.Network</span></span>
* <span data-ttu-id="2fb44-1390">Folgende Cmdlets hinzugefügt: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="2fb44-1390">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="2fb44-1391">ICMP wieder unterstützten AzureFirewall-Netzwerkprotokollen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1391">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="2fb44-1392">Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert und Überprüfung für Ziel-ID, Adresse und Port hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1392">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="2fb44-1393">Probleme mit Arbeitsspeicherauslastung in der VirtualNetwork-Zuordnung behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-1393">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="2fb44-1394">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="2fb44-1394">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="2fb44-1395">Problem beim Ändern der Richtlinie für eine geschützte Dateifreigabe behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-1395">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="2fb44-1396">Richtlinienzeitzone in Großschreibung geändert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1396">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="2fb44-1397">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="2fb44-1397">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="2fb44-1398">Korrigiertes Beispiel in „New-AzureRmRecoveryServicesAsrProtectableItem“</span><span class="sxs-lookup"><span data-stu-id="2fb44-1398">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="2fb44-1399">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1399">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="2fb44-1400">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="2fb44-1400">Az.Relay</span></span>
* <span data-ttu-id="2fb44-1401">Optionaler Parameter „-KeyValue“ zu Cmdlet „New-AzureRmRelayKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht</span><span class="sxs-lookup"><span data-stu-id="2fb44-1401">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="2fb44-1402">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2fb44-1402">Az.Resources</span></span>
* <span data-ttu-id="2fb44-1403">Hilfedokumentation für ressourcenidentitätsbezogene Parameter in `New-AzureRmPolicyAssignment` und `Set-AzureRmPolicyAssignment` aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1403">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="2fb44-1404">Beispiel für „New-AzureRmPolicyDefinition“ hinzugefügt, das „-Metadata“ nutzt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1404">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="2fb44-1405">Korrektur, um Beibehaltung von Groß-/Kleinschreibung in Tagschlüsseln in „NetStandard“ zu ermöglichen: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="2fb44-1405">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="2fb44-1406">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2fb44-1406">Az.ServiceFabric</span></span>
* <span data-ttu-id="2fb44-1407">Benachrichtigung über veraltete Elemente für anstehende wichtige Änderungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1407">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="2fb44-1408">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2fb44-1408">Az.Sql</span></span>
* <span data-ttu-id="2fb44-1409">Neue Cmdlets für CRUD-Vorgänge in verwalteten Azure SQL-Datenbank-Instanzen und verwalteten Azure SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1409">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="2fb44-1410">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2fb44-1410">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2fb44-1411">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2fb44-1411">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2fb44-1412">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2fb44-1412">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2fb44-1413">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2fb44-1413">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2fb44-1414">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="2fb44-1414">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="2fb44-1415">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="2fb44-1415">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="2fb44-1416">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="2fb44-1416">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="2fb44-1417">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="2fb44-1417">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="2fb44-1418">Erweiterte Verwaltung von Überwachungsrichtlinien auf einem Server oder in einer Datenbank aktiviert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1418">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="2fb44-1419">Neuer Parameter (PredicateExpression) hinzugefügt, um die Filterung von Überwachungsprotokollen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="2fb44-1419">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="2fb44-1420">Cmdlets wurden angepasst, sodass sie SQL-Clients anstelle von Legacyclients verwenden.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1420">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="2fb44-1421">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="2fb44-1421">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="2fb44-1422">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="2fb44-1422">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="2fb44-1423">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="2fb44-1423">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="2fb44-1424">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="2fb44-1424">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="2fb44-1425">Problem bei Verwendung von „Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings“ mit festgelegtem Parameter für den Speicherkontonamen behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-1425">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="2fb44-1426">0.5.0 – November 2018</span><span class="sxs-lookup"><span data-stu-id="2fb44-1426">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="2fb44-1427">Allgemein</span><span class="sxs-lookup"><span data-stu-id="2fb44-1427">General</span></span>
* <span data-ttu-id="2fb44-1428">Ressourcenvervollständigungen für viele Kern-Cmdlets hinzugefügt (diese ermöglichen das Durchlaufen von vorhandenen Ressourcennamen per TAB-TASTE, wenn Cmdlets interaktiv aufgerufen werden)</span><span class="sxs-lookup"><span data-stu-id="2fb44-1428">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="2fb44-1429">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2fb44-1429">Az.Profile</span></span>
* <span data-ttu-id="2fb44-1430">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="2fb44-1430">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="2fb44-1431">Parameter „TenantId“ im Cmdlet „Connect-AzAccount“ in „Tenant“ umbenannt und Alias für „TenantId“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1431">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="2fb44-1432">Beschreibung von „TenantId“ für „Connect-AzAccount“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1432">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="2fb44-1433">Fehlermeldung für fehlgeschlagene Anmeldung bei Angabe der Mandantendomäne korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1433">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="2fb44-1434">Problem in Bezug auf Kontextnamenskonflikt für Konten ohne Abonnements im Mandanten behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-1434">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="2fb44-1435">Problem mit DataLake-Endpunkten bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-1435">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="2fb44-1436">Problem behoben, das zur Auslösung von „Disconnect-AzAccount“ führte, wenn keine Verbindung bestand</span><span class="sxs-lookup"><span data-stu-id="2fb44-1436">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="2fb44-1437">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2fb44-1437">Az.CognitiveServices</span></span>
* <span data-ttu-id="2fb44-1438">Vorgang „Get-AzCognitiveServicesAccountSkus“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1438">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2fb44-1439">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2fb44-1439">Az.Compute</span></span>
* <span data-ttu-id="2fb44-1440">Cmdlets Add-AzVmssVMDataDisk und Remove-AzVmssVMDataDisk hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1440">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="2fb44-1441">„Get-AzVMImage“ zeigt „AutomaticOSUpgradeProperties“ an</span><span class="sxs-lookup"><span data-stu-id="2fb44-1441">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="2fb44-1442">Problem behoben, aufgrund dessen die Optionswerte „SetAzVMChefExtension -BootstrapOptions“ und „-JsonAttribute“ nicht im JSON-Format festgelegt wurden</span><span class="sxs-lookup"><span data-stu-id="2fb44-1442">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2fb44-1443">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2fb44-1443">Az.DataLakeStore</span></span>
* <span data-ttu-id="2fb44-1444">Aktualisierung des DataLake-Pakets auf 1.1.10</span><span class="sxs-lookup"><span data-stu-id="2fb44-1444">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="2fb44-1445">Standardmäßige Parallelität zu Multithreadvorgängen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1445">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="2fb44-1446">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="2fb44-1446">Az.Insights</span></span>
* <span data-ttu-id="2fb44-1447">Problem Nr. 7267 behoben (Bereich für automatische Skalierung)</span><span class="sxs-lookup"><span data-stu-id="2fb44-1447">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="2fb44-1448">Probleme beim Erstellen einer neuen Regel für die automatische Skalierung, aufgrund derer die aufgelisteten Parameter nicht richtig festgelegt wurden (Es wurde stets der Standardwert festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="2fb44-1448">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="2fb44-1449">Problem Nr. 7513 behoben [Insights] „Set-AzDiagnosticSetting“ erfordert die explizite Angabe von Kategorien während der Erstellung der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1449">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="2fb44-1450">Nun erfordert das Cmdlet nicht die explizite Angabe der Kategorien, die während der Erstellung aktiviert werden sollen. Das bedeutet, es funktioniert wie dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1450">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2fb44-1451">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2fb44-1451">Az.Network</span></span>
* <span data-ttu-id="2fb44-1452">„PeeringType“ wurde geändert und ist nun ein erforderlicher Parameter für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="2fb44-1452">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="2fb44-1453">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="2fb44-1453">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="2fb44-1454">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="2fb44-1454">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="2fb44-1455">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="2fb44-1455">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="2fb44-1456">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="2fb44-1456">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="2fb44-1457">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="2fb44-1457">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="2fb44-1458">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="2fb44-1458">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2fb44-1459">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2fb44-1459">Az.PolicyInsights</span></span>
* <span data-ttu-id="2fb44-1460">Cmdlets für Richtlinienwartung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1460">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="2fb44-1461">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2fb44-1461">Az.Resources</span></span>
* <span data-ttu-id="2fb44-1462">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="2fb44-1462">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="2fb44-1463">Zulassen der Auflistung von Ressourcen mithilfe des Parameters „-ResourceId“ für „Get-AzResource“</span><span class="sxs-lookup"><span data-stu-id="2fb44-1463">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2fb44-1464">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2fb44-1464">Az.ServiceBus</span></span>
* <span data-ttu-id="2fb44-1465">Schreibgeschützte Eigenschaft „MigrationState“ zu „PSServiceBusMigrationConfigurationAttributes“ hinzugefügt, was das Ermitteln des Migrationsstatus ermöglicht</span><span class="sxs-lookup"><span data-stu-id="2fb44-1465">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2fb44-1466">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2fb44-1466">Az.ServiceFabric</span></span>
* <span data-ttu-id="2fb44-1467">Hinzufügen des Zertifikats zu Linux VMSS korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1467">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="2fb44-1468">„Add-AzServiceFabricClusterCertificate“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="2fb44-1468">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="2fb44-1469">Verwenden des richtigen Fingerabdrucks aus dem neuen Zertifikat (Azure/service-fabric-issues#932)</span><span class="sxs-lookup"><span data-stu-id="2fb44-1469">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="2fb44-1470">Richtige Anzeige von Ausnahmen (Azure/service-fabric-issues#1054)</span><span class="sxs-lookup"><span data-stu-id="2fb44-1470">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="2fb44-1471">„Update-AzServiceFabricDurability“ korrigiert, um die Clusterkonfiguration zu aktualisieren, bevor der VMSS-Vorgang „CreateOrUpdate“ gestartet wird</span><span class="sxs-lookup"><span data-stu-id="2fb44-1471">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="2fb44-1472">0.4.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="2fb44-1472">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="2fb44-1473">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2fb44-1473">Az.Profile</span></span>
* <span data-ttu-id="2fb44-1474">Problem mit „Get-AzSubscription“ in Cloud Shell behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-1474">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="2fb44-1475">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="2fb44-1475">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2fb44-1476">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2fb44-1476">Az.Compute</span></span>
* <span data-ttu-id="2fb44-1477">Neue Größen zur Whitelist von VM-Größen hinzugefügt, für die bei Verwendung des einfachen Parametersatzes für „New-AzVm“ der beschleunigte Netzwerkbetrieb aktiviert wird</span><span class="sxs-lookup"><span data-stu-id="2fb44-1477">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="2fb44-1478">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1478">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2fb44-1479">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2fb44-1479">Az.DataLakeStore</span></span>
* <span data-ttu-id="2fb44-1480">Unterstützung für VNET-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1480">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="2fb44-1481">Get-AzDataLakeStoreVirtualNetworkRule: Dient zum Abrufen oder Auflisten der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1481">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="2fb44-1482">Add-AzDataLakeStoreVirtualNetworkRule: Fügt dem angegebenen Data Lake Store-Konto eine Regel für das virtuelle Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1482">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="2fb44-1483">Set-AzDataLakeStoreVirtualNetworkRule: Ändert die angegebene Regel für das virtuelle Netzwerk in das angegebene Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1483">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="2fb44-1484">Remove-AzDataLakeStoreVirtualNetworkRule: Dient zum Löschen der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1484">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2fb44-1485">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2fb44-1485">Az.Network</span></span>
* <span data-ttu-id="2fb44-1486">Cmdlet „Test-AzNetworkWatcherConnectivity“ aktualisiert, Protokollwert wird jetzt an Back-End übergeben.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1486">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="2fb44-1487">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1487">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2fb44-1488">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2fb44-1488">Az.Resources</span></span>
* <span data-ttu-id="2fb44-1489">Problem behoben, aufgrund dessen „Get-AzRoleDefinition“ eine unverständliche Ausnahme auslöst (wenn das Standardprofil kein Abonnement enthält und kein Bereich festgelegt ist), indem im Szenario eine aussagekräftige Ausnahme hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1489">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="2fb44-1490">Außerdem wurde der Standardparametersatz auf „RoleDefinitionNameParameterSet“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1490">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="2fb44-1491">0.3.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="2fb44-1491">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="2fb44-1492">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="2fb44-1492">Azure.Storage</span></span>
* <span data-ttu-id="2fb44-1493">Fehler beim Kopieren von Blobs/Dateien behoben, aufgrund dessen bei einem Metadatenproblem des Ziels keine Metadaten kopiert wurden</span><span class="sxs-lookup"><span data-stu-id="2fb44-1493">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="2fb44-1494">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2fb44-1494">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="2fb44-1495">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="2fb44-1495">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="2fb44-1496">Der Abruf der Speicherressourcennutzung eines bestimmten Standorts wird jetzt unterstützt, und das Hinzufügen einer Warnmeldung für den Abruf der globalen Speicherressourcennutzung ist überflüssig.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1496">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="2fb44-1497">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="2fb44-1497">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="2fb44-1498">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2fb44-1498">Az.CognitiveServices</span></span>
* <span data-ttu-id="2fb44-1499">„Get-AzCognitiveServicesAccountSkus“ wird ohne vorhandenes Konto unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1499">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2fb44-1500">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2fb44-1500">Az.Compute</span></span>
* <span data-ttu-id="2fb44-1501">Korrektur von „Get-AzVM -ResourceGroupName <rg>“, sodass ggf. mehr als 50 Ergebnisse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="2fb44-1501">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="2fb44-1502">Der Cmdlet-Hilfe zu „New-AzVmss“ wurde ein Beispiel für „SimpleParameterSet“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1502">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="2fb44-1503">Tippfehler in der Azure Disk Encryption-Statusmeldung behoben</span><span class="sxs-lookup"><span data-stu-id="2fb44-1503">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="2fb44-1504">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2fb44-1504">Az.DataFactoryV2</span></span>
* <span data-ttu-id="2fb44-1505">Die Version des ADF .Net-SDK wurde auf 2.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1505">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2fb44-1506">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2fb44-1506">Az.Network</span></span>
* <span data-ttu-id="2fb44-1507">NetworkProfile-Funktionalität wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1507">Added NetworkProfile functionality.</span></span> <span data-ttu-id="2fb44-1508">Neue Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1508">new cmdlets added</span></span>
    - <span data-ttu-id="2fb44-1509">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2fb44-1509">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="2fb44-1510">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2fb44-1510">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="2fb44-1511">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2fb44-1511">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="2fb44-1512">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2fb44-1512">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="2fb44-1513">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="2fb44-1513">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="2fb44-1514">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="2fb44-1514">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="2fb44-1515">Dienstzuordnungslink in Subnetzmodell hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1515">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="2fb44-1516">Cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1516">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="2fb44-1517">Cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1517">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="2fb44-1518">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2fb44-1518">Az.RedisCache</span></span>
* <span data-ttu-id="2fb44-1519">Künftig sind beliebige Zeichenfolgen als Größenparameter zulässig.</span><span class="sxs-lookup"><span data-stu-id="2fb44-1519">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="2fb44-1520">P5 in Popup „PSArgumentCompleter“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1520">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="2fb44-1521">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2fb44-1521">Az.Resources</span></span>
* <span data-ttu-id="2fb44-1522">Fehlender Parameter „-Mode“ zu „Set-AzPolicyDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="2fb44-1522">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="2fb44-1523">Cmdlet-Fehler bei „Get-AzProviderOperation“ für Vorgänge mit Ursprung behoben, der den Benutzer enthält</span><span class="sxs-lookup"><span data-stu-id="2fb44-1523">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="2fb44-1524">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2fb44-1524">Az.Sql</span></span>
* <span data-ttu-id="2fb44-1525">Problem behoben, aufgrund dessen einige Sicherungs-Cmdlets das aktuelle Azure-Abonnements nicht erkannt haben</span><span class="sxs-lookup"><span data-stu-id="2fb44-1525">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2fb44-1526">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2fb44-1526">Az.Websites</span></span>
* <span data-ttu-id="2fb44-1527">Neues Cmdlet „Get-AzWebAppContainerContinuousDeploymentUrl“ zum Abrufen der Webhook-URL von Continuous Deployment für Container</span><span class="sxs-lookup"><span data-stu-id="2fb44-1527">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="2fb44-1528">Neue Cmdlets „New-AzWebAppContainerPSSession“ und „Enter-WebAppContainerPSSession“ zum Initiieren einer PowerShell-Remotesitzung in einer Windows-Container-App</span><span class="sxs-lookup"><span data-stu-id="2fb44-1528">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="2fb44-1529">0.2.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="2fb44-1529">0.2.0 - September 2018</span></span>
 <span data-ttu-id="2fb44-1530">Erste Version</span><span class="sxs-lookup"><span data-stu-id="2fb44-1530">Initial Release</span></span>
