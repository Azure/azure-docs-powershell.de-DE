---
title: Versionshinweise zu Azure PowerShell
description: Hier erfahren Sie mehr über die aktuellen Updates für die Azure PowerShell-Module.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: 83e6039153bcc2b8ccb7ceddfa91609f0d6c7b3f
ms.sourcegitcommit: b4ee3fbaaa2a329ea28308bd1902ae83a34db698
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2019
ms.locfileid: "72380197"
---
## <a name="280---october-2019"></a><span data-ttu-id="fb2da-103">2.8.0: Oktober 2019</span><span class="sxs-lookup"><span data-stu-id="fb2da-103">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="fb2da-104">Allgemein</span><span class="sxs-lookup"><span data-stu-id="fb2da-104">General</span></span>
* <span data-ttu-id="fb2da-105">Az.HealthcareApis-Release 1.0.0</span><span class="sxs-lookup"><span data-stu-id="fb2da-105">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="fb2da-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fb2da-106">Az.Accounts</span></span>
* <span data-ttu-id="fb2da-107">Telemetriedaten und URL-Umschreibung für generierte Module aktualisiert, Windows-Komponententests korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-107">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="fb2da-108">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fb2da-108">Az.ApiManagement</span></span>
* <span data-ttu-id="fb2da-109">**Set-AzApiManagementApi**: Unterstützung für die Aktualisierung der API in „ApiVersionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-109">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="fb2da-110">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="fb2da-110">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fb2da-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fb2da-111">Az.Automation</span></span>
* <span data-ttu-id="fb2da-112">Cmdlet „New-AzureAutomationSoftwareUpdateConfiguration“ für den Parameter für die Linux-Neustarteinstellung korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-112">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="fb2da-113">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="fb2da-113">Az.Batch</span></span>
* <span data-ttu-id="fb2da-114">**Get-AzBatchNodeAgentSku** ist veraltet und wird in Version 2.0.0 durch **Get-AzBatchSupportImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="fb2da-114">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fb2da-115">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fb2da-115">Az.Compute</span></span>
* <span data-ttu-id="fb2da-116">Parameter „Priority“, „EvictionPolicy“ und „MaxPrice“ zu den Cmdlets „“New-AzVM“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-116">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="fb2da-117">Warnmeldung und Hilfedokument für die Cmdlets „Add-AzVMAdditionalUnattendContent“ und „Add-AzVMSshPublicKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-117">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="fb2da-118">Ausnahme „-skipVmBackup“ Linux-VMs mit verwalteten Datenträgern für „Set-AzVMDiskEncryptionExtension“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-118">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="fb2da-119">Fehler beim Aktualisieren von Verschlüsselungseinstellungen in „Set-AzVMDiskEncryptionExtension“ korrigiert (zweistufiges Szenario)</span><span class="sxs-lookup"><span data-stu-id="fb2da-119">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fb2da-120">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fb2da-120">Az.DataFactory</span></span>
* <span data-ttu-id="fb2da-121">CRUD-Befehle für ADF V2-Datenfluss hinzugefügt: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow und Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="fb2da-121">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="fb2da-122">Aktionsbefehle für Debugsitzung für ADF V2-Datenfluss hinzugefügt: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand und Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="fb2da-122">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="fb2da-123">Version des ADF .NET SDK auf 4.2.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-123">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fb2da-124">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fb2da-124">Az.DataLakeStore</span></span>
* <span data-ttu-id="fb2da-125">Kontoüberprüfung korrigiert, sodass Konten mit „-“ ohne Domäne übermittelt werden können</span><span class="sxs-lookup"><span data-stu-id="fb2da-125">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="fb2da-126">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="fb2da-126">Az.HealthcareApis</span></span>
* <span data-ttu-id="fb2da-127">PowerShell-Version auf 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-127">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="fb2da-128">SDK-Version auf 1.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-128">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="fb2da-129">Aktualisierung in Tests, um auf neue SDK-Version zu verweisen</span><span class="sxs-lookup"><span data-stu-id="fb2da-129">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="fb2da-130">Ausgabestruktur von geschachtelt in vereinfacht geändert</span><span class="sxs-lookup"><span data-stu-id="fb2da-130">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="fb2da-131">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="fb2da-131">Az.IotHub</span></span>
* <span data-ttu-id="fb2da-132">Neue Routingquelle hinzugefügt: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="fb2da-132">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="fb2da-133">Kleinere Fehlerbehebung: „Get-AzIothub“ gibt „subscriptionId“ nicht zurück.</span><span class="sxs-lookup"><span data-stu-id="fb2da-133">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="fb2da-134">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fb2da-134">Az.Monitor</span></span>
* <span data-ttu-id="fb2da-135">Neue Aktionsgruppenempfänger für Aktionsgruppe hinzugefügt:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="fb2da-135">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="fb2da-136">Verwendung des allgemeinen Warnungsschemas für Empfänger aktiviert.</span><span class="sxs-lookup"><span data-stu-id="fb2da-136">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="fb2da-137">Dies gilt nicht für SMS, Azure App-Pushbenachrichtigungen, ITSM und Sprachempfänger.</span><span class="sxs-lookup"><span data-stu-id="fb2da-137">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="fb2da-138">Webhooks unterstützen nun die Azure Active Directory-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="fb2da-138">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fb2da-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fb2da-139">Az.Network</span></span>
* <span data-ttu-id="fb2da-140">Neues Cmdlet „Get-AzAvailableServiceAlias“ hinzugefügt, das zum Abrufen der Aliase aufgerufen werden kann, die für Dienstendpunktrichtlinien verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="fb2da-140">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="fb2da-141">Unterstützung für das Hinzufügen von Verbindungen von Datenverkehrsselektoren zu Virtual Network-Gatewayverbindungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-141">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="fb2da-142">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="fb2da-142">New cmdlets added:</span></span>
        - <span data-ttu-id="fb2da-143">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="fb2da-143">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="fb2da-144">Cmdlets mit optionalen Parametern aktualisiert: -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="fb2da-144">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="fb2da-145">Unterstützung für ESP- und AH-Protokolle in Konfigurationen von Netzwerksicherheitsregeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-145">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="fb2da-146">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="fb2da-146">Updated cmdlets:</span></span>
        - <span data-ttu-id="fb2da-147">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fb2da-147">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="fb2da-148">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fb2da-148">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="fb2da-149">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fb2da-149">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="fb2da-150">Verbesserte Behandlung von Ausnahmen in Cortex-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="fb2da-150">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="fb2da-151">Neue Generationen und SKUs für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="fb2da-151">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="fb2da-152">Einführung neuer Generationen für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="fb2da-152">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="fb2da-153">Einführung neuer SKUs mit höherem Durchsatz für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="fb2da-153">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="fb2da-154">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="fb2da-154">Az.RedisCache</span></span>
* <span data-ttu-id="fb2da-155">Referenzdokumentation zu „Set-AzRedisCache“ aktualisiert, um fehlende Werte für den Parameter „-Size“ aufzunehmen</span><span class="sxs-lookup"><span data-stu-id="fb2da-155">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="fb2da-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fb2da-156">Az.Sql</span></span>
* <span data-ttu-id="fb2da-157">Unterstützung für das Festlegen des Active Directory-Administrators für verwaltete Instanz hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-157">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fb2da-158">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fb2da-158">Az.Storage</span></span>
* <span data-ttu-id="fb2da-159">Storage-Clientbibliothek auf 11.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-159">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="fb2da-160">Auflisten von Containern mit der API der Verwaltungsebene, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="fb2da-160">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="fb2da-161">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fb2da-161">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="fb2da-162">Auflisten von Storage-Konten aus Abonnements, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="fb2da-162">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="fb2da-163">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fb2da-163">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="fb2da-164">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="fb2da-164">Az.StorageSync</span></span>
* <span data-ttu-id="fb2da-165">Problem 9810 in „Reset-AzStorageSyncServerCertificate“ behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-165">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fb2da-166">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fb2da-166">Az.Websites</span></span>
* <span data-ttu-id="fb2da-167">Fehler beim Aktualisieren von ASP einer App mit „Set-AzWebApp“</span><span class="sxs-lookup"><span data-stu-id="fb2da-167">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="fb2da-168">2.7.0: September 2019</span><span class="sxs-lookup"><span data-stu-id="fb2da-168">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="fb2da-169">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fb2da-169">Az.ApiManagement</span></span>
* <span data-ttu-id="fb2da-170">Beschreibung des Parameters „-Format“ in der Referenzdokumentation für „Set-AzApiManagementPolicy“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-170">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="fb2da-171">Verweise des veralteten Cmdlets „Update-AzApiManagementDeployment“ aus Referenzdokumentation entfernt.</span><span class="sxs-lookup"><span data-stu-id="fb2da-171">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="fb2da-172">Verwenden Sie stattdessen „Set-AzApiManagement“.</span><span class="sxs-lookup"><span data-stu-id="fb2da-172">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fb2da-173">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fb2da-173">Az.Automation</span></span>
* <span data-ttu-id="fb2da-174">Tippfehler im Beispiel in der Referenzdokumentation für „Register-AzAutomationDscNode“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-174">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="fb2da-175">Erläuterung zur Betriebssystemeinschränkung zu „Register-AzAutomationDSCNode“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-175">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="fb2da-176">Nullverweisausnahme des Cmdlets „Start-AzAutomationRunbook“ für die Option „-Wait“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="fb2da-176">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fb2da-177">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fb2da-177">Az.Compute</span></span>
* <span data-ttu-id="fb2da-178">Parameter „UploadSizeInBytes“ zu „New-AzDiskConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-178">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="fb2da-179">Inkrementeller Parameter zu „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-179">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="fb2da-180">Feature für VM mit niedriger Priorität hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="fb2da-180">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="fb2da-181">Parameter „MaxPrice“, „EvictionPolicy“ und „Priority“ zu New-AzVMConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-181">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="fb2da-182">Parameter „MaxPrice“ zu den Cmdlets „New-AzVmssConfig“, „Update-AzVM“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-182">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="fb2da-183">Fehlerbehebung für VM-Verweis für das Cmdlet „Get-AzAvailabilitySet“, wenn alle Verfügbarkeitsgruppen im Abonnement aufgelistet werden</span><span class="sxs-lookup"><span data-stu-id="fb2da-183">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="fb2da-184">Nullausnahme für „Get-AzRemoteDesktopFile“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-184">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="fb2da-185">VHD-Suchmethode für Position relativ zum Ende korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-185">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="fb2da-186">Problem mit UltraSSD für „New-AzVM“ und „Update-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-186">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fb2da-187">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fb2da-187">Az.DataFactory</span></span>
* <span data-ttu-id="fb2da-188">Drei neue Befehle für ADF V2 hinzugefügt: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription und Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="fb2da-188">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="fb2da-189">Version des ADF .NET SDK auf 4.1.3 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-189">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="fb2da-190">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="fb2da-190">Az.HDInsight</span></span>
* <span data-ttu-id="fb2da-191">Hinweis auf Breaking Changes hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-191">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="fb2da-192">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="fb2da-192">Az.IotHub</span></span>
* <span data-ttu-id="fb2da-193">Unterstützung zum Aufrufen eines Failovers für einen IoT-Hub zur geografisch gekoppelten Notfallwiederherstellungsregion hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-193">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="fb2da-194">Unterstützung zum Verwalten der Nachrichtenanreicherung für einen IoT-Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-194">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="fb2da-195">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="fb2da-195">New cmdlets are:</span></span>
    - <span data-ttu-id="fb2da-196">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="fb2da-196">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="fb2da-197">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="fb2da-197">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="fb2da-198">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="fb2da-198">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="fb2da-199">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="fb2da-199">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="fb2da-200">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fb2da-200">Az.Monitor</span></span>
* <span data-ttu-id="fb2da-201">Verweis auf das aktuelle Monitor SDK, d. h. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="fb2da-201">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="fb2da-202">Geringfügige Änderungen an den Metrik-Cmdlets vorgenommen, d. h. die Einheitenenumeration unterstützt verschiedene neue Werte.</span><span class="sxs-lookup"><span data-stu-id="fb2da-202">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="fb2da-203">Dabei handelt es sich um schreibgeschützte Cmdlets, sodass keine Änderungen an der Eingabe der Cmdlets erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="fb2da-203">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="fb2da-204">Die API-Version der **ActionGroups**-Anforderungen lautet jetzt **2019-06-01** (zuvor **2018-03-01**).</span><span class="sxs-lookup"><span data-stu-id="fb2da-204">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="fb2da-205">Die Szenariotests wurden aktualisiert, um diese Änderung zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="fb2da-205">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="fb2da-206">Die Konstruktoren für die Klassen **EmailReceiver** und **WebhookReceiver** haben ein neues obligatorisches Argument hinzugefügt, d. h. einen booleschen Wert namens **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="fb2da-206">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="fb2da-207">Derzeit ist der Wert auf **false** festgelegt, damit sich dieser Breaking Change nicht auf die Cmdlets auswirkt.</span><span class="sxs-lookup"><span data-stu-id="fb2da-207">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="fb2da-208">**HINWEIS:** Dies ist eine vorübergehende Änderung, die vom Team für Warnungen validiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="fb2da-208">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="fb2da-209">Die Reihenfolge der Argumente für den Konstruktor der Klasse **Source** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="fb2da-209">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="fb2da-210">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="fb2da-210">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="fb2da-211">Die Reihenfolge der Argumente für den Konstruktor der Klasse **AlertingAction** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="fb2da-211">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="fb2da-212">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="fb2da-212">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="fb2da-213">Unterstützung von Kriterien für dynamische Schwellwerte für Metrikwarnung v2</span><span class="sxs-lookup"><span data-stu-id="fb2da-213">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="fb2da-214">New-AzMetricAlertRuleV2Criteria: Erstellt nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="fb2da-214">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="fb2da-215">Add-AzMetricAlertRuleV2: Akzeptiert nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="fb2da-215">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="fb2da-216">Verbesserungen an den Cmdlets für geplante Abfrageregeln (Scheduled Query Rule, SQR)</span><span class="sxs-lookup"><span data-stu-id="fb2da-216">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="fb2da-217">Cmdlets akzeptieren den Parameter „Location“ in zwei Formaten: entweder den Standort (z. B. „eastus“) oder den Anzeigenamen des Standorts (z. B. „USA, Osten“)</span><span class="sxs-lookup"><span data-stu-id="fb2da-217">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="fb2da-218">Parameter „Enabled“ in Hilfedateien ordnungsgemäß dargestellt</span><span class="sxs-lookup"><span data-stu-id="fb2da-218">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="fb2da-219">Beispiele für optionalen Parameter „ActionGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-219">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="fb2da-220">Hilfedateien insgesamt verbessert</span><span class="sxs-lookup"><span data-stu-id="fb2da-220">Overall improved help files</span></span>
* <span data-ttu-id="fb2da-221">Fehler beim Bestimmen des Bereichstyps für „Set-AzActionRule“ behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-221">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fb2da-222">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fb2da-222">Az.Network</span></span>
* <span data-ttu-id="fb2da-223">Fehlerhaftes Beispiel in der Referenzdokumentation zu „New-AzApplicationGateway“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-223">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="fb2da-224">Hinweis in der Referenzdokumentation zu „Get-AzNetworkWatcherPacketCapture“ zum Abrufen aller Eigenschaften für eine Paketerfassung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-224">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="fb2da-225">Beispiel in der Referenzdokumentation zu „Test-AzNetworkWatcherIPFlow“ korrigiert, um die Netzwerkadapter ordnungsgemäß aufzulisten</span><span class="sxs-lookup"><span data-stu-id="fb2da-225">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="fb2da-226">Cloudausnahmeanalyse verbessert, um ggf. zusätzliche Details anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="fb2da-226">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="fb2da-227">Cloudausnahmeanalyse verbessert, um zusätzlichen Typ der SDK-Ausnahme zu verarbeiten</span><span class="sxs-lookup"><span data-stu-id="fb2da-227">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="fb2da-228">Falsche Zuordnung der Sicherheitsregelmodelle korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-228">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="fb2da-229">Eigenschaften zur Netzwerkschnittstelle für das Feature für die private IP-Adresse hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-229">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="fb2da-230">Eigenschaft „PrivateEndpoint“ als Typ „PSResourceId“ zu „PSNetworkInterface“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-230">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="fb2da-231">Eigenschaft „PrivateLinkConnectionProperties“ als Typ „PSIpConfigurationConnectivityInformation“ zu „PSNetworkInterfaceIPConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-231">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="fb2da-232">Neue Modellklasse „PSIpConfigurationConnectivityInformation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-232">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="fb2da-233">Neues ApplicationRuleProtocolType-Element „mssql“ für Azure Firewall-Ressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-233">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="fb2da-234">Unterstützung von Mehrfachverbindungen in Virtual WAN</span><span class="sxs-lookup"><span data-stu-id="fb2da-234">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="fb2da-235">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="fb2da-235">New cmdlets</span></span>
        - <span data-ttu-id="fb2da-236">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="fb2da-236">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="fb2da-237">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="fb2da-237">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="fb2da-238">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="fb2da-238">Updated cmdlet:</span></span>
        - <span data-ttu-id="fb2da-239">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="fb2da-239">New-VpnSite</span></span>
        - <span data-ttu-id="fb2da-240">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="fb2da-240">Update-VpnSite</span></span>
        - <span data-ttu-id="fb2da-241">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="fb2da-241">New-VpnConnection</span></span>
        - <span data-ttu-id="fb2da-242">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="fb2da-242">Update-VpnConnection</span></span>
* <span data-ttu-id="fb2da-243">Dokumente für einige PowerShell-Beispiele korrigiert, sodass Az-Cmdlets anstelle von AzureRM-Cmdlets verwendet werden</span><span class="sxs-lookup"><span data-stu-id="fb2da-243">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fb2da-244">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fb2da-244">Az.RecoveryServices</span></span>
* <span data-ttu-id="fb2da-245">AzureVMpolicy-Objekt mit ProtectedItemsCount-Attribut aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-245">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="fb2da-246">Tests für VM-Richtlinie und Wiederherstellung des ursprünglichen Speicherkontos hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-246">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="fb2da-247">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fb2da-247">Az.Resources</span></span>
* <span data-ttu-id="fb2da-248">Fehler behoben, aufgrund dessen „New-AzRoleAssignment“ nicht ohne den Parameter „Scope“ aufgerufen werden konnte</span><span class="sxs-lookup"><span data-stu-id="fb2da-248">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="fb2da-249">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fb2da-249">Az.ServiceFabric</span></span>
* <span data-ttu-id="fb2da-250">Tippfehler im Beispiel für die Referenzdokumentation „Update-AzServiceFabricReliability“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-250">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="fb2da-251">Neue Cmdlets zum Verwalten von Anwendung und Diensten hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="fb2da-251">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="fb2da-252">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="fb2da-252">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="fb2da-253">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="fb2da-253">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="fb2da-254">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="fb2da-254">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="fb2da-255">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="fb2da-255">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="fb2da-256">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="fb2da-256">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="fb2da-257">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="fb2da-257">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="fb2da-258">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="fb2da-258">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="fb2da-259">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="fb2da-259">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="fb2da-260">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="fb2da-260">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="fb2da-261">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="fb2da-261">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="fb2da-262">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="fb2da-262">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="fb2da-263">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="fb2da-263">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="fb2da-264">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="fb2da-264">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="fb2da-265">Service Fabric SDK auf Version 1.2.0 aktualisiert, die API-Version 2019-03-01 des Service Fabric-Ressourcenanbieters verwendet</span><span class="sxs-lookup"><span data-stu-id="fb2da-265">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="fb2da-266">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="fb2da-266">Az.SignalR</span></span>
* <span data-ttu-id="fb2da-267">Cmdlets „Update“, „Restart“, „CheckNameAvailability“ und „GetUsage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-267">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="fb2da-268">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fb2da-268">Az.Sql</span></span>
* <span data-ttu-id="fb2da-269">Beispiel in der Referenzdokumentation für „Get-AzSqlElasticPool“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-269">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="fb2da-270">V-Kern-Beispiel zum Erstellen eines Pools für elastische Datenbanken hinzugefügt (New-AzSqlElasticPool)</span><span class="sxs-lookup"><span data-stu-id="fb2da-270">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="fb2da-271">Überprüfung von „EmailAddresses“ sowie Validierung, dass „EmailAdmins“ nicht auf „false“ festgelegt ist, in „Set-AzSqlServerAdvancedThreatProtectionPolicy“ und „Set-AzSqlDatabaseAdvancedThreatProtectionPolicy“ entfernt, wenn „EmailAddresses“ leer ist</span><span class="sxs-lookup"><span data-stu-id="fb2da-271">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="fb2da-272">Entfernen der Einstellungen für Server-/Datenbanküberwachung aktiviert, wenn mehrere Diagnoseeinstellungen vorhanden sind, die eine Überwachungskategorie ermöglichen</span><span class="sxs-lookup"><span data-stu-id="fb2da-272">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="fb2da-273">Überprüfung von E-Mail-Adressen in mehreren Cmdlets für die SQL-Sicherheitsrisikobewertung korrigiert (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting und Update-AzSqlInstanceVulnerabilityAssessmentSetting)</span><span class="sxs-lookup"><span data-stu-id="fb2da-273">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fb2da-274">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fb2da-274">Az.Storage</span></span>
* <span data-ttu-id="fb2da-275">Beispiel in der Referenzdokumentation für „Get-AzStorageAccountKey“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-275">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="fb2da-276">Beim Upload/Download von Azure-Dateien wird das Beibehalten der SMB-Eigenschaften der Quelldateien (Dateiattribute, Zeitpunkt der Dateierstellung, letzter Schreibzugriff für die Datei) in der Zieldatei unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fb2da-276">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="fb2da-277">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="fb2da-277">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="fb2da-278">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="fb2da-278">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="fb2da-279">Fehler beim Hochladen von Blockblobs mit Eigenschaften/Metadaten für das für einen Container aktivierte ImmutabilityPolicy-Element behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-279">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="fb2da-280">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="fb2da-280">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="fb2da-281">Unterstützung für die Verwaltung von Azure-Dateifreigaben mit der API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="fb2da-281">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="fb2da-282">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="fb2da-282">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="fb2da-283">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="fb2da-283">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="fb2da-284">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="fb2da-284">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="fb2da-285">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="fb2da-285">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fb2da-286">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fb2da-286">Az.Websites</span></span>
* <span data-ttu-id="fb2da-287">Problem behoben, aufgrund dessen webapp-Tags beim Migrieren der App zu neuem ASP gelöscht wurden</span><span class="sxs-lookup"><span data-stu-id="fb2da-287">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="fb2da-288">„Publish-AzureWebapp“ für die Verwendung unter Linux und Windows korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-288">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="fb2da-289">Beispiel in Referenzdokumentation „Get-AzWebAppPublishingProfile“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-289">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="fb2da-290">2.6.0: August 2019</span><span class="sxs-lookup"><span data-stu-id="fb2da-290">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="fb2da-291">Allgemein</span><span class="sxs-lookup"><span data-stu-id="fb2da-291">General</span></span>
* <span data-ttu-id="fb2da-292">Verschiedene Tippfehler in zahlreichen Modulen korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-292">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="fb2da-293">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fb2da-293">Az.Accounts</span></span>
* <span data-ttu-id="fb2da-294">Unterstützung der benutzerseitig zugewiesenen MSI in Azure Functions-Authentifizierung (#9479)</span><span class="sxs-lookup"><span data-stu-id="fb2da-294">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="fb2da-295">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="fb2da-295">Az.Aks</span></span>
* <span data-ttu-id="fb2da-296">Problem mit der Ausgabe für „Get-AzAks“ behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-296">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="fb2da-297">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="fb2da-297">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="fb2da-298">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fb2da-298">Az.ApiManagement</span></span>
* <span data-ttu-id="fb2da-299">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="fb2da-299">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="fb2da-300">.NET-NuGet-Version aktualisiert, die keine Einschränkungen für „productId“, „apiId“, „groupId“ und „userId“ erzwingt</span><span class="sxs-lookup"><span data-stu-id="fb2da-300">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="fb2da-301">**Get-AzApiManagementProduct:** Unterstützung für das Abfragen von Produkten mithilfe der API hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-301">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="fb2da-302">**New-AzApiManagementApiRevision:** Problem behoben, aufgrund dessen „ApiRevisionDescription“ beim Erstellen einer neuen API-Revision nicht festgelegt wurde https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="fb2da-302">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="fb2da-303">Tippfehler im Modell „PsApiManagementOAuth2AuthrozationServer“ korrigiert: PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="fb2da-303">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="fb2da-304">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="fb2da-304">Az.Batch</span></span>
* <span data-ttu-id="fb2da-305">Tippfehler in Hilfemeldung und Dokumentation korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="fb2da-305">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="fb2da-306">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="fb2da-306">Az.Cdn</span></span>
* <span data-ttu-id="fb2da-307">Tippfehler im Hilfsprogramm für die CDN-Modulkonvertierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-307">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fb2da-308">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fb2da-308">Az.Compute</span></span>
* <span data-ttu-id="fb2da-309">VmssId zum Cmdlet „New-AzVMConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-309">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="fb2da-310">Parameter „TerminateScheduledEvents“ und „TerminateScheduledEventNotBeforeTimeoutInMinutes“ zu „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-310">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="fb2da-311">HyperVGeneration-Eigenschaft zu VM-Imageobjekt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-311">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="fb2da-312">Host- und HostGroup-Features hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-312">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="fb2da-313">Neue Cmdlets:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="fb2da-313">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="fb2da-314">Parameter „HostId“ zu „New-AzVMConfig“ und „New-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-314">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="fb2da-315">Beispiel in der Dokumentation zu „Invoke-AzVMRunCommand“ zur Verwendung des richtigen Parameternamens aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-315">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="fb2da-316">Beschreibung für „-VolumeType“ in der Referenzdokumentation zu „Set-AzVMDiskEncryptionExtension“ und „Set-AzVmssDiskEncryptionExtension“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-316">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fb2da-317">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fb2da-317">Az.DataFactory</span></span>
* <span data-ttu-id="fb2da-318">Tippfehler in der Dokumentation zu „New-AzDataFactoryEncryptValue“ korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="fb2da-318">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="fb2da-319">Version des ADF .NET SDK auf 4.1.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-319">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="fb2da-320">Parameter „DataProxyIntegrationRuntimeName“, „DataProxyStagingLinkedServiceName“ und „DataProxyStagingPath“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um die Einrichtung der selbstgehosteten Integration Runtime als Proxy für die SSIS Integration Runtime zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="fb2da-320">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="fb2da-321">„PSTriggerRun“ zum Anzeigen der ausgelösten Pipelines, Meldungen und Eigenschaften und „PSActivityRun“ zum Anzeigen des Aktivitätstyps aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-321">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fb2da-322">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fb2da-322">Az.DataLakeStore</span></span>
* <span data-ttu-id="fb2da-323">Hängen von „Get-DataLakeStoreDeletedItem“ aufgrund von Fehlern oder Remoteausnahmen behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-323">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="fb2da-324">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="fb2da-324">Az.EventHub</span></span>
* <span data-ttu-id="fb2da-325">Behebung des Problems #9658: Tippfehler im Parameter „VirtualNteworkRule“ in „Set-AzEventHubNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="fb2da-325">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="fb2da-326">Behebung des Problems #9558: „Set-AzEventHubNamespace“ verwendet PATCH anstelle von PUT.</span><span class="sxs-lookup"><span data-stu-id="fb2da-326">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="fb2da-327">Parameter „EnableKafka“ zum Cmdlet „Set-AzEventHubNamespace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-327">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="fb2da-328">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="fb2da-328">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="fb2da-329">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="fb2da-329">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="fb2da-330">Tippfehler („Azure“ in Kleinbuchstaben) in der Dokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-330">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="fb2da-331">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fb2da-331">Az.Monitor</span></span>
* <span data-ttu-id="fb2da-332">Falscher Parametername in der Hilfedokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-332">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fb2da-333">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fb2da-333">Az.Network</span></span>
* <span data-ttu-id="fb2da-334">„New-AzPrivateLinkServiceIpConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-334">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="fb2da-335">Parameter „PublicIpAddress“ ausgemustert, da er auf Serverseite nie verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="fb2da-335">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="fb2da-336">Optionaler Parameter „Primary“ hinzugefügt, der angibt, ob die aktuelle IP-Konfiguration die primäre ist oder nicht</span><span class="sxs-lookup"><span data-stu-id="fb2da-336">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="fb2da-337">Verbesserte Verarbeitung der Anforderungsfehlerausnahme aus dem SDK: Behebt das Problem, dass vorherige SDK-Ausnahmen nicht richtig behandelt wurden, was dazu führt, dass Schlüsselfehlerdetails nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="fb2da-337">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="fb2da-338">Validierungslogik für Ipv6-IP-Präfix angepasst, damit auf die richtige IPv6-Präfixlänge geprüft wird</span><span class="sxs-lookup"><span data-stu-id="fb2da-338">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="fb2da-339">„Get-AzVirtualNetworkSubnetConfig“ aktualisiert: Parametersatz zum Abrufen nach Subnetzressourcen-ID hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-339">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="fb2da-340">Aktualisierte Beschreibung des Location-Parameters für „AzNetworkServiceTag“</span><span class="sxs-lookup"><span data-stu-id="fb2da-340">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="fb2da-341">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fb2da-341">Az.OperationalInsights</span></span>
* <span data-ttu-id="fb2da-342">Aktualisierte Dokumentation für „New-AzOperationalInsightsLinuxSyslogDataSource“</span><span class="sxs-lookup"><span data-stu-id="fb2da-342">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="fb2da-343">Beispiel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-343">Added example</span></span>
    - <span data-ttu-id="fb2da-344">Beschreibung für den Parameter „-Name“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-344">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="fb2da-345">Beispiel für „New-AzOperationalInsightsWindowsEventDataSource“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-345">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="fb2da-346">Beschreibung des Parameters „-Name“ für „New-AzOperationalInsightsWindowsEventDataSource“ geändert</span><span class="sxs-lookup"><span data-stu-id="fb2da-346">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fb2da-347">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fb2da-347">Az.RecoveryServices</span></span>
* <span data-ttu-id="fb2da-348">„Get-AzRecoveryServicesBackupJobDetail.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-348">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="fb2da-349">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fb2da-349">Az.Resources</span></span>
* <span data-ttu-id="fb2da-350">Unterstützung für die neue API-Version 2019-05-10 für Microsoft.Resource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-350">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="fb2da-351">Unterstützung für „copy.count = 0“ für Variablen, Ressourcen und Eigenschaften hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-351">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="fb2da-352">Ressourcen mit „condition = false“ oder „copy.count = 0“ werden im vollständigen Modus gelöscht.</span><span class="sxs-lookup"><span data-stu-id="fb2da-352">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="fb2da-353">Beispiel zum Hinzufügen einer Richtlinie auf Abonnementebene zur Hilfedokumentation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-353">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="fb2da-354">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fb2da-354">Az.ServiceBus</span></span>
* <span data-ttu-id="fb2da-355">Behebung des Problems #9658: Tippfehler für Parameter „VirtualNetworkRule“ in „Set-AzServiceBusNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="fb2da-355">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="fb2da-356">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="fb2da-356">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="fb2da-357">Neuer Befehl „Test-AzServiceBusNameAvailability“ zum Überprüfen der Verfügbarkeit des Namens für Warteschlange und Thema hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-357">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="fb2da-358">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fb2da-358">Az.ServiceFabric</span></span>
* <span data-ttu-id="fb2da-359">Fehler bei Cmdlets zum Hinzufügen des Knotentyps korrigiert:</span><span class="sxs-lookup"><span data-stu-id="fb2da-359">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="fb2da-360">Fehler „NullReferenceException“, wenn die Ressourcengruppe andere VMSS enthielt, die nicht mit dem Service Fabric-Cluster in Zusammenhang stehen</span><span class="sxs-lookup"><span data-stu-id="fb2da-360">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="fb2da-361">Problembehebung: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="fb2da-361">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="fb2da-362">Fehler behoben, aufgrund dessen bei einem Cmdlet ein Fehler auftrat, wenn sich „virtualNetwork“ in einer anderen Ressourcengruppe befand als der Cluster</span><span class="sxs-lookup"><span data-stu-id="fb2da-362">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="fb2da-363">Problembehebung: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="fb2da-363">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="fb2da-364">Cmdlet „Add-AzServiceFabricApplicationCertificate“ ausgemustert</span><span class="sxs-lookup"><span data-stu-id="fb2da-364">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="fb2da-365">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fb2da-365">Az.Sql</span></span>
* <span data-ttu-id="fb2da-366">Dokumentation alter Überwachungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-366">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fb2da-367">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fb2da-367">Az.Storage</span></span>
* <span data-ttu-id="fb2da-368">Hilfe für „Get/Close-AzStorageFileHandle“ aktualisiert (weitere Szenarien zu Cmdlet-Beispielen hinzugefügt und Parameterbeschreibungen aktualisiert)</span><span class="sxs-lookup"><span data-stu-id="fb2da-368">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="fb2da-369">Unterstützung von „StandardBlobTier“ in Uploadblobs und Kopierblobs</span><span class="sxs-lookup"><span data-stu-id="fb2da-369">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="fb2da-370">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="fb2da-370">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="fb2da-371">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="fb2da-371">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="fb2da-372">Unterstützung der Aktivierungspriorität im Kopierblob</span><span class="sxs-lookup"><span data-stu-id="fb2da-372">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="fb2da-373">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="fb2da-373">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fb2da-374">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fb2da-374">Az.Websites</span></span>
* <span data-ttu-id="fb2da-375">Hinzufügen von Erläuterungen zum Parameter „-AppSettings“ in „Set-AzWebApp“ und „Set-AzWebAppSlot“</span><span class="sxs-lookup"><span data-stu-id="fb2da-375">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="fb2da-376">2.5.0: Juli 2019</span><span class="sxs-lookup"><span data-stu-id="fb2da-376">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fb2da-377">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fb2da-377">Az.Accounts</span></span>
* <span data-ttu-id="fb2da-378">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="fb2da-378">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="fb2da-379">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="fb2da-379">Az.ApplicationInsights</span></span>
* <span data-ttu-id="fb2da-380">Tippfehler im Beispiel in der Dokumentation zu „Remove-AzApplicationInsightsApiKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-380">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="fb2da-381">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fb2da-381">Az.Automation</span></span>
* <span data-ttu-id="fb2da-382">Tippfehler in der Ressourcenzeichenfolge korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-382">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="fb2da-383">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fb2da-383">Az.CognitiveServices</span></span>
* <span data-ttu-id="fb2da-384">Unterstützung für NetworkRuleSet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-384">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fb2da-385">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fb2da-385">Az.Compute</span></span>
* <span data-ttu-id="fb2da-386">Fehlende Eigenschaften (ComputerName, OsName, OsVersion und HyperVGeneration) des Objekts für die VM-Instanzenansicht hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-386">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="fb2da-387">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fb2da-387">Az.ContainerRegistry</span></span>
* <span data-ttu-id="fb2da-388">Tippfehler in „Remove-AzContainerRegistryReplication“ für den Replikationsparameter korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-388">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="fb2da-389">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="fb2da-389">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fb2da-390">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fb2da-390">Az.DataFactory</span></span>
* <span data-ttu-id="fb2da-391">Version des ADF .NET SDK auf 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-391">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="fb2da-392">Tippfehler in der Dokumentation für „Get-AzDataFactoryV2PipelineRun“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-392">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="fb2da-393">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="fb2da-393">Az.EventHub</span></span>
* <span data-ttu-id="fb2da-394">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="fb2da-394">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="fb2da-395">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="fb2da-395">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="fb2da-396">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fb2da-396">Az.KeyVault</span></span>
* <span data-ttu-id="fb2da-397">Unterstützung zum Angeben von KeySize für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-397">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="fb2da-398">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="fb2da-398">Az.LogicApp</span></span>
* <span data-ttu-id="fb2da-399">Korrektur für „Get-AzIntegrationAccountMap“ zum Auflisten aller Zuordnungstypen</span><span class="sxs-lookup"><span data-stu-id="fb2da-399">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="fb2da-400">Neuer MapType-Parameter für Filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-400">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="fb2da-401">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="fb2da-401">Az.ManagedServices</span></span>
* <span data-ttu-id="fb2da-402">Unterstützung für API-Version 2019-06-01 (GA) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-402">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fb2da-403">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fb2da-403">Az.Network</span></span>
* <span data-ttu-id="fb2da-404">Unterstützung für privaten Endpunkt und privaten Verknüpfungsdienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-404">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="fb2da-405">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="fb2da-405">New cmdlets</span></span>
        - <span data-ttu-id="fb2da-406">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="fb2da-406">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="fb2da-407">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="fb2da-407">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="fb2da-408">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="fb2da-408">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="fb2da-409">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="fb2da-409">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="fb2da-410">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="fb2da-410">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="fb2da-411">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="fb2da-411">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="fb2da-412">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="fb2da-412">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="fb2da-413">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="fb2da-413">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="fb2da-414">Folgende Befehle für das Feature aktualisiert: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies für Subnetz in VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fb2da-414">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="fb2da-415">„New-AzVirtualNetworkSubnetConfig“, „Set-AzVirtualNetworkSubnetConfig“ und „Add-AzVirtualNetworkSubnetConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-415">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="fb2da-416">Optionaler Parameter „-PrivateEndpointNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den privaten Endpunkt in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="fb2da-416">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="fb2da-417">Optionaler Parameter „-PrivateLinkServiceNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den Privat Link-Dienst in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="fb2da-417">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="fb2da-418">Der Cmdlet-Parameter „ServiceName“ von AzPrivateLinkService wurde aus Gründen der Abwärtskompatibilität in „Name“ mit dem Alias „ServiceName“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="fb2da-418">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="fb2da-419">ICMP-Protokoll für Konfigurationen von Netzwerksicherheitsregeln aktiviert</span><span class="sxs-lookup"><span data-stu-id="fb2da-419">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="fb2da-420">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="fb2da-420">Updated cmdlets</span></span>
        - <span data-ttu-id="fb2da-421">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fb2da-421">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="fb2da-422">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fb2da-422">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="fb2da-423">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fb2da-423">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="fb2da-424">ConnectionProtocolType (Ikev1/Ikev2) als konfigurierbarer Parameter für „New-AzVirtualNetworkGatewayConnection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-424">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="fb2da-425">PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-425">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="fb2da-426">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="fb2da-426">Updated cmdlet:</span></span>
        - <span data-ttu-id="fb2da-427">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="fb2da-427">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="fb2da-428">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="fb2da-428">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="fb2da-429">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="fb2da-429">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="fb2da-430">Application Gateway-Befehl „New-AzApplicationGatewayProbeConfig“ zur Unterstützung des benutzerdefinierten Ports im Test aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-430">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="fb2da-431">„New-AzApplicationGatewayProbeConfig“ aktualisiert: Optionaler Parameter „Port“ hinzugefügt, der zum Testen des Back-End-Servers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fb2da-431">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="fb2da-432">Dieser Parameter gilt für Standard_V2 und WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="fb2da-432">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="fb2da-433">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fb2da-433">Az.OperationalInsights</span></span>
* <span data-ttu-id="fb2da-434">Standardversion für gespeicherte Suchvorgänge auf 1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-434">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="fb2da-435">Verarbeitung des regulären NULL-Ausdrucks in benutzerdefinierten Protokollen korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-435">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fb2da-436">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fb2da-436">Az.RecoveryServices</span></span>
* <span data-ttu-id="fb2da-437">„Get-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-437">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="fb2da-438">„Get-AzRecoveryServicesBackupContainer.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-438">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="fb2da-439">„Get-AzRecoveryServicesVault.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-439">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="fb2da-440">„Wait-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-440">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="fb2da-441">„Set-AzRecoveryServicesVaultContext.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-441">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="fb2da-442">„Get-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-442">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="fb2da-443">„Get-AzRecoveryServicesBackupRecoveryPoint.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-443">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="fb2da-444">„Restore-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-444">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="fb2da-445">Dienstaufruf zum Aufheben der Containerregistrierung für Azure-Dateifreigabe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-445">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="fb2da-446">„Set-AzRecoveryServicesAsrAlertSetting.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-446">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="fb2da-447">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fb2da-447">Az.Resources</span></span>
- <span data-ttu-id="fb2da-448">Fehlendes Cmdlet entfernt, auf das in der Dokumentation zu „New-AzResourceGroupDeployment“ verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="fb2da-448">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="fb2da-449">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-449">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="fb2da-450">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fb2da-450">Az.ServiceBus</span></span>
* <span data-ttu-id="fb2da-451">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="fb2da-451">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="fb2da-452">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="fb2da-452">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="fb2da-453">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fb2da-453">Az.Sql</span></span>
* <span data-ttu-id="fb2da-454">Fehlende Beispiele für Cmdlet „Set-AzSqlDatabaseSecondary“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-454">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="fb2da-455">Festlegen wiederkehrender Überprüfungen der Sicherheitsrisikobewertung ohne Angabe von E-Mail-Adressen korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-455">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="fb2da-456">Tippfehler in einer Warnmeldung korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-456">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fb2da-457">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fb2da-457">Az.Storage</span></span>
* <span data-ttu-id="fb2da-458">Beispiel in Referenzdokumentation für „Get-AzStorageAccount“ aktualisiert, sodass der richtige Parametername verwendet wird</span><span class="sxs-lookup"><span data-stu-id="fb2da-458">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="fb2da-459">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="fb2da-459">Az.StorageSync</span></span>
* <span data-ttu-id="fb2da-460">Cmdlet „Invoke-AzStorageSyncChangeDetection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-460">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="fb2da-461">Problem 9551 zur Berücksichtigung von „TierFilesOlderThanDays“ behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-461">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fb2da-462">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fb2da-462">Az.Websites</span></span>
* <span data-ttu-id="fb2da-463">Problem behoben, aufgrund dessen einige SiteConfig-Eigenschaften von „Get-AzWebApp“ und „Set-AzWebApp“ nicht zurückgegeben wurden</span><span class="sxs-lookup"><span data-stu-id="fb2da-463">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="fb2da-464">Neuer Standortparameter zu „Get-AzDeletedWebApp“ und „Restore-AzDeletedWebApp“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-464">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="fb2da-465">Fehler beim Klonen von Web-App-Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-465">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="fb2da-466">2.4.0 – Juli 2019</span><span class="sxs-lookup"><span data-stu-id="fb2da-466">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fb2da-467">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fb2da-467">Az.Accounts</span></span>
* <span data-ttu-id="fb2da-468">Unterstützung für Profil-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-468">Add support for profile cmdlets</span></span>
* <span data-ttu-id="fb2da-469">Unterstützung für Umgebungen und Datenebenen in generierten Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-469">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="fb2da-470">Korrektur eines Fehlers, bei dem in einigen Fällen ein falscher Endpunkt für Datenebenen-Cmdlets in Windows PowerShell verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="fb2da-470">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="fb2da-471">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="fb2da-471">Az.Advisor</span></span>
* <span data-ttu-id="fb2da-472">Allgemein verfügbares Release von Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="fb2da-472">GA release of Az.Advisor</span></span>
* <span data-ttu-id="fb2da-473">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="fb2da-473">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="fb2da-474">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fb2da-474">Az.ApiManagement</span></span>
* <span data-ttu-id="fb2da-475">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="fb2da-475">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="fb2da-476">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="fb2da-476">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="fb2da-477">Unterstützung für Abfragen von Abonnements nach Benutzer und Produkt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-477">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="fb2da-478">Unterstützung für Abfragen anhand des Umfangs hinzugefügt, „/“, „/apis“, „/apis/echo-api“</span><span class="sxs-lookup"><span data-stu-id="fb2da-478">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="fb2da-479">Behebung von Problem https://github.com/Azure/azure-powershell/issues/9307 und https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="fb2da-479">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="fb2da-480">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="fb2da-480">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="fb2da-481">Unterstützung für die Angabe von „ApiVersion“ und „ApiVersionSetId“ beim Importieren von APIs hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-481">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fb2da-482">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fb2da-482">Az.Automation</span></span>
* <span data-ttu-id="fb2da-483">Fehler beim Cmdlet „Set-AzAutomationConnectionFieldValue“ für die Verarbeitung des Zeichenfolgewerts behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-483">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fb2da-484">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fb2da-484">Az.Compute</span></span>
* <span data-ttu-id="fb2da-485">Parameter „HyperVGeneration“ zu New-AzImageConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-485">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fb2da-486">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fb2da-486">Az.DataFactory</span></span>
* <span data-ttu-id="fb2da-487">Aktualisierung der Ausgabe von ADF-Cmdlets für das Abrufen von Aktivitäts-, Pipeline- und Auslöserausführungen, um die Pipe „Select-Object“ zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="fb2da-487">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="fb2da-488">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="fb2da-488">Az.EventGrid</span></span>
* <span data-ttu-id="fb2da-489">Tippfehler in Dokumentation zu 'New-AzEventGridSubscription' behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-489">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="fb2da-490">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="fb2da-490">Az.IotHub</span></span>
* <span data-ttu-id="fb2da-491">Unterstützung für das erneute Generieren von Autorisierungsrichtlinienschlüsseln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-491">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fb2da-492">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fb2da-492">Az.Network</span></span>
* <span data-ttu-id="fb2da-493">„RoutingPreference“ zu öffentlichen IP-Tags hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-493">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="fb2da-494">Beispiele für Referenzdokumentation zu „Get-AzNetworkServiceTag“ verbessert</span><span class="sxs-lookup"><span data-stu-id="fb2da-494">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="fb2da-495">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="fb2da-495">Az.PolicyInsights</span></span>
* <span data-ttu-id="fb2da-496">Fehlerbehebung für Nullverweis in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="fb2da-496">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="fb2da-497">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="fb2da-497">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="fb2da-498">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fb2da-498">Az.OperationalInsights</span></span>
* <span data-ttu-id="fb2da-499">Zurückgegebenes CustomLog-Datenquellenmodell in Get-AzOperationalInsightsDataSource korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-499">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fb2da-500">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fb2da-500">Az.RecoveryServices</span></span>
* <span data-ttu-id="fb2da-501">Fehlerbehebung für Befehl „get-policy“ IaaSVMs</span><span class="sxs-lookup"><span data-stu-id="fb2da-501">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="fb2da-502">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fb2da-502">Az.Resources</span></span>
    - <span data-ttu-id="fb2da-503">Hilfetext für Parameter „-Top“ von „Get-AzPolicyState“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-503">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="fb2da-504">Clientseitige Unterstützung von Paginierung für „Get-AzPolicyAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-504">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="fb2da-505">Neue Parameter für „Set-AzPolicyAssignment“, „-PolicyParameters“ und „-PolicyParametersObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-505">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="fb2da-506">Einige Aktualisierungen von Dokumentationen und Beispielen für Policy-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="fb2da-506">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="fb2da-507">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fb2da-507">Az.ServiceBus</span></span>
* <span data-ttu-id="fb2da-508">Korrektur für Problem Nr. 4938: „New-AzureRmServiceBusQueue“ gibt beim Festlegen von „MaxSizeInMegabytes“ „BadRequest“ zurück</span><span class="sxs-lookup"><span data-stu-id="fb2da-508">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="fb2da-509">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fb2da-509">Az.Sql</span></span>
* <span data-ttu-id="fb2da-510">Instanzfailovergruppen-Cmdlets aus Vorschauversion in öffentliche Version hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-510">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="fb2da-511">Unterstützung von Azure SQL Server\Datenbanküberwachung mit neuen Cmdlets</span><span class="sxs-lookup"><span data-stu-id="fb2da-511">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="fb2da-512">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="fb2da-512">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="fb2da-513">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="fb2da-513">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="fb2da-514">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="fb2da-514">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="fb2da-515">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="fb2da-515">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="fb2da-516">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="fb2da-516">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="fb2da-517">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="fb2da-517">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="fb2da-518">E-Mail-Einschränkungen aus Einstellungen der Sicherheitsrisikobewertung entfernt</span><span class="sxs-lookup"><span data-stu-id="fb2da-518">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fb2da-519">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fb2da-519">Az.Storage</span></span>
* <span data-ttu-id="fb2da-520">Zwei Parameter („-IndexDocument“ und „-ErrorDocument404Path“) in folgendem Cmdlet von erforderlich in optional geändert:</span><span class="sxs-lookup"><span data-stu-id="fb2da-520">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="fb2da-521">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="fb2da-521">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="fb2da-522">Hilfe zu „Get-AzStorageBlobContent“ mit neuem Beispiel ergänzt</span><span class="sxs-lookup"><span data-stu-id="fb2da-522">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="fb2da-523">Anzeige von mehr Fehlerinformationen beim Fehlschlagen eines Cmdlets mit „StorageException“</span><span class="sxs-lookup"><span data-stu-id="fb2da-523">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="fb2da-524">Unterstützung für das Erstellen oder Aktualisieren von Speicherkonten mit Azure Files AAD-DS-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="fb2da-524">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="fb2da-525">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fb2da-525">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="fb2da-526">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fb2da-526">Set-AzStorageAccount</span></span>
* <span data-ttu-id="fb2da-527">Unterstützung für das Auflisten oder Schließen von Dateihandles einer Dateifreigabe, eines Dateiverzeichnisses oder einer Datei</span><span class="sxs-lookup"><span data-stu-id="fb2da-527">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="fb2da-528">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="fb2da-528">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="fb2da-529">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="fb2da-529">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="fb2da-530">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="fb2da-530">Az.StorageSync</span></span>
* <span data-ttu-id="fb2da-531">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="fb2da-531">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="fb2da-532">2.3.2 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="fb2da-532">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fb2da-533">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fb2da-533">Az.Accounts</span></span>
* <span data-ttu-id="fb2da-534">Fehler behoben, aufgrund dessen in manchen Fällen eine falsche URL für Funktionsaufrufe verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="fb2da-534">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="fb2da-535">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="fb2da-535">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="fb2da-536">Problem mit Aliasen zwischen AzureRM und Azure-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-536">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="fb2da-537">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="fb2da-537">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="fb2da-538">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="fb2da-538">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fb2da-539">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fb2da-539">Az.Compute</span></span>
* <span data-ttu-id="fb2da-540">Die einfachen Parametersätze „New-AzVm“ und „New-AzVmss“ akzeptieren jetzt den Parameter „ProximityPlacementGroup“.</span><span class="sxs-lookup"><span data-stu-id="fb2da-540">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="fb2da-541">Tippfehler in der Referenzdokumentation für „New-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-541">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="fb2da-542">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="fb2da-542">Az.Dns</span></span>
* <span data-ttu-id="fb2da-543">Tippfehler in den Hilfebeispielen zu „Set-AzDnsZone“ behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-543">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="fb2da-544">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="fb2da-544">Az.EventGrid</span></span>
* <span data-ttu-id="fb2da-545">Zur Verwendung der API-Version 2019-06-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-545">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="fb2da-546">Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="fb2da-546">New cmdlets:</span></span>
    - <span data-ttu-id="fb2da-547">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="fb2da-547">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="fb2da-548">Erstellt eine neue Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="fb2da-548">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="fb2da-549">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="fb2da-549">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="fb2da-550">Ruft die Details einer Event Grid-Domäne oder eine Liste aller Event Grid-Domänen im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="fb2da-550">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="fb2da-551">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="fb2da-551">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="fb2da-552">Entfernt eine Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="fb2da-552">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="fb2da-553">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="fb2da-553">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="fb2da-554">Generiert den freigegebenen Zugriffsschlüssel für eine Azure Event Grid-Domäne erneut.</span><span class="sxs-lookup"><span data-stu-id="fb2da-554">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="fb2da-555">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="fb2da-555">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="fb2da-556">Ruft die freigegebenen Zugriffsschlüssel ab, die zum Veröffentlichen von Ereignissen in einer Event Grid-Domäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fb2da-556">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="fb2da-557">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="fb2da-557">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="fb2da-558">Erstellt ein neues Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="fb2da-558">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="fb2da-559">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="fb2da-559">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="fb2da-560">Ruft die Details eines Event Grid-Domänenthemas oder eine Liste aller Event Grid-Domänenthemen unter der jeweiligen Event Grid-Domäne im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="fb2da-560">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="fb2da-561">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="fb2da-561">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="fb2da-562">Entfernt ein vorhandenes Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="fb2da-562">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="fb2da-563">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="fb2da-563">Updated cmdlets:</span></span>
    - <span data-ttu-id="fb2da-564">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="fb2da-564">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="fb2da-565">Neue erforderliche Parameter zur Unterstützung des Pipings für die neue Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="fb2da-565">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="fb2da-566">Neue erforderliche Parameter zum Angeben des neuen Event Grid-Domänennamens und/oder Namens des Event Grid-Domänenthemas hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="fb2da-566">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="fb2da-567">Neue Parametersätze für Domänen und Domänenthemen hinzugefügt, um die Wiederverwendung vorhandener Parameter zuzulassen (‚z. B. „EndPointType“, „SubjectBeginsWith“ usw.)</span><span class="sxs-lookup"><span data-stu-id="fb2da-567">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="fb2da-568">Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="fb2da-568">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="fb2da-569">Ablaufdatum des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="fb2da-569">Event subscription expiration date,</span></span>
            - <span data-ttu-id="fb2da-570">Erweiterte Filterparameter</span><span class="sxs-lookup"><span data-stu-id="fb2da-570">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="fb2da-571">Neue Enumeration für „servicebusqueue“ als Ziel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-571">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="fb2da-572">Verwendung der Option „All“ in „-IncludedEventType“ gesperrt und wie folgt ersetzt</span><span class="sxs-lookup"><span data-stu-id="fb2da-572">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="fb2da-573">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="fb2da-573">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="fb2da-574">Neue optionale Parameter („Top“, „ODataQuery“ und „NextLink“) zur Unterstützung der Ergebnispaginierung und -filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-574">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="fb2da-575">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="fb2da-575">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="fb2da-576">Neue erforderliche Parameter zur Unterstützung des Pipings für die Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Entfernen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="fb2da-576">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="fb2da-577">Neue erforderliche Parameter zum Angeben des Event Grid-Domänennamens und/oder Event Grid-Domänenthemanamens hinzugefügt, um das Entfernen vorhandener Ereignisabonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="fb2da-577">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="fb2da-578">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="fb2da-578">Az.FrontDoor</span></span>
* <span data-ttu-id="fb2da-579">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="fb2da-579">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="fb2da-580">Unterstützung von Transformationen und neuen Wert für den Operator zum automatischen Vervollständigen (RegEx) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-580">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="fb2da-581">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="fb2da-581">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="fb2da-582">Neue Werte für automatisches Vervollständigen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-582">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fb2da-583">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fb2da-583">Az.Network</span></span>
* <span data-ttu-id="fb2da-584">Unterstützung für Virtual Network-Gatewayressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-584">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="fb2da-585">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="fb2da-585">New cmdlets</span></span>
        - <span data-ttu-id="fb2da-586">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="fb2da-586">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="fb2da-587">AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="fb2da-587">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="fb2da-588">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="fb2da-588">New cmdlets</span></span> 
        - <span data-ttu-id="fb2da-589">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="fb2da-589">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="fb2da-590">„PrivatePrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-590">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="fb2da-591">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="fb2da-591">New cmdlets</span></span> 
        - <span data-ttu-id="fb2da-592">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="fb2da-592">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="fb2da-593">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="fb2da-593">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="fb2da-594">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="fb2da-594">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="fb2da-595">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="fb2da-595">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="fb2da-596">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="fb2da-596">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="fb2da-597">„PrivateEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-597">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="fb2da-598">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="fb2da-598">New cmdlets</span></span>
        - <span data-ttu-id="fb2da-599">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="fb2da-599">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="fb2da-600">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="fb2da-600">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="fb2da-601">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="fb2da-601">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="fb2da-602">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="fb2da-602">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="fb2da-603">Folgende Befehle für das Feature aktualisiert: UseLocalAzureIpAddress-Flag für „VpnConnection“</span><span class="sxs-lookup"><span data-stu-id="fb2da-603">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="fb2da-604">„New-AzVpnConnection§ „ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="fb2da-604">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="fb2da-605">„Set-AzVpnConnection“ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="fb2da-605">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="fb2da-606">Schreibgeschütztes Feld „PeeredConnections“ beim ExpressRoute-Peering hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-606">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="fb2da-607">Schreibgeschütztes Feld „GlobalReachEnabled“ in ExpressRoute hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-607">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="fb2da-608">Breaking Change-Attribut hinzugefügt, um auf das veraltete Feld „AllowGlobalReach“ im ExpressRouteCircuit-Modell hinzuweisen</span><span class="sxs-lookup"><span data-stu-id="fb2da-608">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="fb2da-609">Fehler 8756 bei der Verwendung von „TargetListenerID“ mit AzApplicationGatewayRedirectConfiguration-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-609">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="fb2da-610">Fehler in „New-AzApplicationGatewayPathRuleConfig“ behoben, aufgrund dessen der Regelsatz für erneutes Generieren nicht festgelegt werden konnte</span><span class="sxs-lookup"><span data-stu-id="fb2da-610">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="fb2da-611">Fehler bei der Anzeige von „VirtualNetworkTaps“ in „NetworkInterfaceIpConfiguration“ behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-611">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="fb2da-612">Cortex-Get-Cmdlets zum Auflisten aller Komponenten korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-612">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="fb2da-613">Problem beim Erstellen des festen VirtualHub-Verweises für ExpressRouteGateways behoben (VpnGateway)</span><span class="sxs-lookup"><span data-stu-id="fb2da-613">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="fb2da-614">Unterstützung für Verfügbarkeitszonen in AzureFirewall und NatGateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-614">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="fb2da-615">Cmdlet „Get-AzNetworkServiceTag“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-615">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="fb2da-616">Unterstützung für mehrere öffentliche IP-Adressen für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-616">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="fb2da-617">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="fb2da-617">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="fb2da-618">Parameter „-PublicIpAddress“ hinzugefügt, der ein oder mehre öffentliche IP-Adressobjekte akzeptiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-618">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="fb2da-619">Parameter „- VirtualNetwork“ hinzugefügt, der ein Virtual Network-Objekt akzeptiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-619">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="fb2da-620">Methoden „AddPublicIpAddress“ und „RemovePublicIpAddress“ für Firewallobjekte hinzugefügt (akzeptieren ein öffentliches IP-Adressobjekt als Eingabe)</span><span class="sxs-lookup"><span data-stu-id="fb2da-620">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="fb2da-621">Parameter „-PublicIpName“ und „-VirtualNetworkName“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-621">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="fb2da-622">Folgende Befehle für das Feature aktualisiert: VpnClient-AAD-Authentifizierungsoptionen auf die Gatewayressource des virtuellen Netzwerkgateways festgelegt</span><span class="sxs-lookup"><span data-stu-id="fb2da-622">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="fb2da-623">„New-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-623">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="fb2da-624">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fb2da-624">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="fb2da-625">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionaler Switch-Parameter „RemoveAadAuthentication“ zum Entfernen von VpnClient-AAD-Authentifizierungsoptionen aus dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-625">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="fb2da-626">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fb2da-626">Az.OperationalInsights</span></span>
* <span data-ttu-id="fb2da-627">Tarif **pergb2018** im Befehl „New-AzureRmOperationalInsightsWorkspace“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="fb2da-627">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="fb2da-628">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fb2da-628">Az.Resources</span></span>
* <span data-ttu-id="fb2da-629">Unterstützung für zusätzliche Optionen zum Exportieren von Vorlagen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-629">Support for additional Template Export options</span></span>
    - <span data-ttu-id="fb2da-630">Parameter „-SkipResourceNameParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-630">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="fb2da-631">Parameter -SkipAllParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-631">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="fb2da-632">Parameter „-Resource“ zu „Export-AzResourceGroup“ hinzugefügt, um das Filtern exportierter Ressourcen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="fb2da-632">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="fb2da-633">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fb2da-633">Az.ServiceFabric</span></span>
* <span data-ttu-id="fb2da-634">Problem beim Hinzufügen des Zertifikats mit „ByExistingKeyVault“ behoben (Abruf des falschen Fingerabdrucks in manchen Fällen)</span><span class="sxs-lookup"><span data-stu-id="fb2da-634">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="fb2da-635">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fb2da-635">Az.Sql</span></span>
* <span data-ttu-id="fb2da-636">Suffix des Advanced Threat Protection-Endpunkts korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-636">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="fb2da-637">Durch Advanced Data Security ermöglichte Außerkraftsetzungen der Advanced Threat Protection-Richtlinie korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-637">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="fb2da-638">Neue Cmdlets für „Management.Sql“ ermöglichen Kunden das Hinzufügen von TDE-Schlüsseln und Festlegen der TDE-Schutzvorrichtung für verwaltete Instanzen.</span><span class="sxs-lookup"><span data-stu-id="fb2da-638">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="fb2da-639">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fb2da-639">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="fb2da-640">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fb2da-640">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="fb2da-641">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fb2da-641">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="fb2da-642">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="fb2da-642">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="fb2da-643">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="fb2da-643">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fb2da-644">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fb2da-644">Az.Storage</span></span>
* <span data-ttu-id="fb2da-645">Unterstützung von „FileStorage“ und „SkuName Premium_ZRS“ beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="fb2da-645">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="fb2da-646">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fb2da-646">New-AzStorageAccount</span></span>
* <span data-ttu-id="fb2da-647">Überarbeitete Beschreibung des Cmdlets für die Unveränderlichkeit von Blobs</span><span class="sxs-lookup"><span data-stu-id="fb2da-647">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="fb2da-648">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="fb2da-648">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fb2da-649">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fb2da-649">Az.Websites</span></span>
* <span data-ttu-id="fb2da-650">Optimiert „Get-AzWebAppCertificate“, um nach der Ressourcengruppe auf dem Server zu filtern (nicht auf dem Client)</span><span class="sxs-lookup"><span data-stu-id="fb2da-650">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="fb2da-651">Switch-Parameter „-UseDisasterRecovery“ für „Get-AzWebAppSnapshot“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-651">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="fb2da-652">2.2.0 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="fb2da-652">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="fb2da-653">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="fb2da-653">Az.Cdn</span></span>
* <span data-ttu-id="fb2da-654">Es wurden Cmdlets aktualisiert, um das rulesEngine-Feature basierend auf der API-Version 2019-04-15 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="fb2da-654">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fb2da-655">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fb2da-655">Az.Compute</span></span>
* <span data-ttu-id="fb2da-656">Der Parameter `NoWait` wurde hinzugefügt, der den Vorgang startet und sofort zurückkehrt, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="fb2da-656">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="fb2da-657">Aktualisierte Cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="fb2da-657">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="fb2da-658">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="fb2da-658">Az.EventHub</span></span>
* <span data-ttu-id="fb2da-659">Fehlerbehebung für #9231 – Get-AzEventHubNamespace gibt keine Tags zurück</span><span class="sxs-lookup"><span data-stu-id="fb2da-659">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="fb2da-660">Fehlerbehebung für #9230 – Get-AzEventHubNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="fb2da-660">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fb2da-661">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fb2da-661">Az.Network</span></span>
* <span data-ttu-id="fb2da-662">ResourceId und InputObject wurden für NAT Gateway aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-662">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="fb2da-663">Es wurde ein Alias für ResourceId und InputObjectr hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-663">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="fb2da-664">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="fb2da-664">Az.PolicyInsights</span></span>
* <span data-ttu-id="fb2da-665">Fehlerbehebung für Nullverweis in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="fb2da-665">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fb2da-666">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fb2da-666">Az.RecoveryServices</span></span>
* <span data-ttu-id="fb2da-667">Minimale Aufbewahrung in Tagen für IaaSVM-Richtlinie wurde von 1 in 7 geändert</span><span class="sxs-lookup"><span data-stu-id="fb2da-667">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="fb2da-668">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fb2da-668">Az.ServiceBus</span></span>
* <span data-ttu-id="fb2da-669">Fehlerbehebung für #9182 – Get-AzServiceBusNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="fb2da-669">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="fb2da-670">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fb2da-670">Az.ServiceFabric</span></span>
* <span data-ttu-id="fb2da-671">Tippfehler in Fehlermeldung für Update-AzServiceFabricReliability wurde behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-671">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="fb2da-672">Fehlendes Zeichen in Service Fabric-Befehlszeilen wurde behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-672">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="fb2da-673">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fb2da-673">Az.Sql</span></span>
* <span data-ttu-id="fb2da-674">Der DnsZonePartner-Parameter für das Cmdlet New-AzureSqlInstance wurde hinzugefügt, um AutoDr für verwaltete Instanzen zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="fb2da-674">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="fb2da-675">Das Cmdlet Get-AzSqlDatabaseSecureConnectionPolicy wird eingestellt</span><span class="sxs-lookup"><span data-stu-id="fb2da-675">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="fb2da-676">Cmdlets zum Schutz vor Bedrohungen werden in „Advanced Threat Protection“ (Erweiterter Schutz vor Bedrohungen) umbenannt</span><span class="sxs-lookup"><span data-stu-id="fb2da-676">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="fb2da-677">New-AzSqlInstance – Die Parameter StorageSizeInGB und LicenseType sind jetzt optional</span><span class="sxs-lookup"><span data-stu-id="fb2da-677">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fb2da-678">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fb2da-678">Az.Websites</span></span>
* <span data-ttu-id="fb2da-679">Das Problem, bei dem die Verwendung von Set-AzWebApp und Set-AzWebAppSlot mit der -WebApp-Eigenschaft die Tags entfernt hat, wurde behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-679">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="fb2da-680">2.1.0 – Mai 2019</span><span class="sxs-lookup"><span data-stu-id="fb2da-680">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="fb2da-681">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fb2da-681">Az.ApiManagement</span></span>
* <span data-ttu-id="fb2da-682">Es wurden neue Cmdlets zum Verwalten der Diagnose im globalen sowie im API-Bereich erstellt</span><span class="sxs-lookup"><span data-stu-id="fb2da-682">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="fb2da-683">**Get-AzApiManagementDiagnostic**: Abrufen der Diagnose, die im globalen oder im API-Bereich konfiguriert wurde</span><span class="sxs-lookup"><span data-stu-id="fb2da-683">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="fb2da-684">**New-AzApiManagementDiagnostic**: Erstellen neuer Diagnosen im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="fb2da-684">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="fb2da-685">**New-AzApiManagementHttpMessageDiagnostic**: Erstellen einer Diagnoseeinstellung für die zu protokollierenden Kopfzeilen und für die Größe der Bytes für den Text</span><span class="sxs-lookup"><span data-stu-id="fb2da-685">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="fb2da-686">**New-AzApiManagementPipelineDiagnosticSetting**: Erstellen von Diagnoseeinstellungen für ein-/ausgehende HTTP-Nachrichten für das Gateway</span><span class="sxs-lookup"><span data-stu-id="fb2da-686">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="fb2da-687">**New-AzApiManagementSamplingSetting**: Erstellen der Einstellung „Sampling“ für die Anforderungen/Antworten für eine Diagnose</span><span class="sxs-lookup"><span data-stu-id="fb2da-687">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="fb2da-688">**Remove-AzApiManagementDiagnostic**: Entfernen einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="fb2da-688">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="fb2da-689">**Set-AzApiManagementDiagnostic**: Aktualisieren einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="fb2da-689">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="fb2da-690">Es wurden neue Cmdlets für die Cacheverwaltung im ApiManagement-Dienst erstellt</span><span class="sxs-lookup"><span data-stu-id="fb2da-690">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="fb2da-691">**Get-AzApiManagementCache**: Abrufen der Details des durch den Bezeichner angegebenen Caches oder aller Caches</span><span class="sxs-lookup"><span data-stu-id="fb2da-691">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="fb2da-692">**New-AzApiManagementCache**: Erstellen eines neuen „standardmäßigen“ Caches oder eines Caches in einer bestimmten „Region“ von Azure</span><span class="sxs-lookup"><span data-stu-id="fb2da-692">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="fb2da-693">**Remove-AzApiManagementCache**: Entfernen eines Caches</span><span class="sxs-lookup"><span data-stu-id="fb2da-693">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="fb2da-694">**Update-AzApiManagementCache**: Aktualisieren eines Caches</span><span class="sxs-lookup"><span data-stu-id="fb2da-694">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="fb2da-695">Es wurden neue Cmdlets zur Verwaltung von API-Schemas erstellt</span><span class="sxs-lookup"><span data-stu-id="fb2da-695">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="fb2da-696">**New-AzApiManagementSchema**: Erstellen eines neuen Schemas für eine API</span><span class="sxs-lookup"><span data-stu-id="fb2da-696">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="fb2da-697">**Get-AzApiManagementSchema**: Abrufen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="fb2da-697">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="fb2da-698">**Remove-AzApiManagementSchema**: Entfernen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="fb2da-698">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="fb2da-699">**Set-AzApiManagementSchema**: Aktualisieren des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="fb2da-699">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="fb2da-700">Es wurde ein neues Cmdlet zum Generieren eines Benutzertokens erstellt</span><span class="sxs-lookup"><span data-stu-id="fb2da-700">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="fb2da-701">**New-AzApiManagementUserToken**: Generieren eines neuen Benutzertokens, das standardmäßig für acht Stunden gültig ist. Mit diesem Cmdlet kann das Token für den „GIT“-Benutzer generiert werden./</span><span class="sxs-lookup"><span data-stu-id="fb2da-701">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="fb2da-702">Es wurde ein neues Cmdlet zum Abrufen des Netzwerkstatus erstellt</span><span class="sxs-lookup"><span data-stu-id="fb2da-702">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="fb2da-703">**Get-AzApiManagementNetworkStatus**: Abrufen der Netzwerkstatuskonnektivität von Ressourcen, von denen der API Management-Dienst abhängig ist</span><span class="sxs-lookup"><span data-stu-id="fb2da-703">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="fb2da-704">Dies ist hilfreich, wenn Sie den ApiManagement-Dienst in einem virtuellen Netzwerk bereitstellen und überprüfen, ob eine der Abhängigkeiten fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="fb2da-704">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="fb2da-705">Das Cmdlet **New-AzApiManagement** wurde zum Verwalten des ApiManagement-Diensts aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-705">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="fb2da-706">Die Unterstützung für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-706">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="fb2da-707">Die Unterstützung zum Aktivieren des Flags „EnableClientCertificate“ für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-707">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="fb2da-708">Das neue Cmdlet **New-AzApiManagementSslSetting** ermöglicht die Konfiguration der „TLS/SSL“-Einstellung für „Back-End“ und „Front-End“</span><span class="sxs-lookup"><span data-stu-id="fb2da-708">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="fb2da-709">Dies kann auch dazu verwendet werden, um „Verschlüsselungen“ wie „3DES“ und „ServerProtokolle“ wie „Http2“ für das „Front-End“ eines ApiManagement-Diensts zu konfigurieren</span><span class="sxs-lookup"><span data-stu-id="fb2da-709">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="fb2da-710">Die Unterstützung für die Konfiguration des Hostnamens „DeveloperPortal“ wurde zum ApiManagement-Dienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-710">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="fb2da-711">Die **Get-AzApiManagementSsoToken**-Cmdlets wurden aktualisiert, um das Objekt „PsApiManagement“ als Eingabe zu übernehmen</span><span class="sxs-lookup"><span data-stu-id="fb2da-711">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="fb2da-712">Das Cmdlet wurde aktualisiert, um Fehlermeldungen inline anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="fb2da-712">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="fb2da-713">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Fehlercode: ValidationError-Fehlermeldung: Mindestens ein Feld enthält ungültige Werte: Fehlerdetails: [Code=ValidationError, Message=Fehler in Element 'log-to-eventhub' in Zeile 3, Spalte 10: Protokollierungstool nicht gefunden, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="fb2da-713">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="fb2da-714">Cmdlet **Export-AzApiManagementApi** wurde für den Export von APIs im Format „OpenApi 3.0“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-714">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="fb2da-715">Cmdlet **Import-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-715">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="fb2da-716">Zum Importieren der API aus der „OpenApi 3.0“-Dokumentspezifikation</span><span class="sxs-lookup"><span data-stu-id="fb2da-716">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="fb2da-717">Zur Außerkraftsetzung der „PsApiManagementSchema“-Eigenschaft, die in einem beliebigen Dokument („Swagger“, „Wadl“, „Wsdl“, „OpenApi“) angegeben ist</span><span class="sxs-lookup"><span data-stu-id="fb2da-717">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="fb2da-718">Zur Außerkraftsetzung der „ServiceUrl“-Eigenschaft, die in einem beliebigen Dokument angegeben ist</span><span class="sxs-lookup"><span data-stu-id="fb2da-718">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="fb2da-719">Cmdlet **Get-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="fb2da-719">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="fb2da-720">Cmdlet **Set-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ und im Format mit XML-Escapezeichen mit „xml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="fb2da-720">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="fb2da-721">Cmdlet **New-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-721">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="fb2da-722">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="fb2da-722">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="fb2da-723">Zum Erstellen einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="fb2da-723">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="fb2da-724">Zum Klonen einer API mithilfe von „SourceApiId“ und „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="fb2da-724">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="fb2da-725">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="fb2da-725">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="fb2da-726">Cmdlet **Set-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-726">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="fb2da-727">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="fb2da-727">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="fb2da-728">Zum Aktualisieren einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="fb2da-728">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="fb2da-729">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="fb2da-729">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="fb2da-730">Cmdlet **New-AzApiManagementRevision** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-730">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="fb2da-731">Zum Klonen (Kopiertags, Produkte, Vorgänge und Richtlinien) einer vorhandenen Version mithilfe von „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="fb2da-731">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="fb2da-732">Die neue Version übernimmt die „ApiId“ des übergeordneten Elements</span><span class="sxs-lookup"><span data-stu-id="fb2da-732">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="fb2da-733">Zum Bereitstellen einer „ApiRevisionDescription“</span><span class="sxs-lookup"><span data-stu-id="fb2da-733">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="fb2da-734">Zur Außerkraftsetzung der „ServiceUrl“ beim Klonen einer API</span><span class="sxs-lookup"><span data-stu-id="fb2da-734">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="fb2da-735">Cmdlet **New-AzApiManagementIdentityProvider** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-735">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="fb2da-736">Zum Konfigurieren von „AAD“ oder „AADB2C“ mit einer „Authority“</span><span class="sxs-lookup"><span data-stu-id="fb2da-736">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="fb2da-737">Zum Einrichten von „SignupPolicy“, „SigninPolicy“, „ProfileEditingPolicy“ und „PasswordResetPolicy“</span><span class="sxs-lookup"><span data-stu-id="fb2da-737">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="fb2da-738">Cmdlet **New-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-738">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="fb2da-739">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="fb2da-739">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="fb2da-740">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="fb2da-740">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="fb2da-741">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-741">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="fb2da-742">Cmdlet **Set-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-742">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="fb2da-743">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="fb2da-743">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="fb2da-744">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="fb2da-744">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="fb2da-745">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-745">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="fb2da-746">Folgende Cmdlets wurden aktualisiert, um „ResourceId“ als Eingabe zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="fb2da-746">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="fb2da-747">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="fb2da-747">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="fb2da-748">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="fb2da-748">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="fb2da-749">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="fb2da-749">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="fb2da-750">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="fb2da-750">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="fb2da-751">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="fb2da-751">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="fb2da-752">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="fb2da-752">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="fb2da-753">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="fb2da-753">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="fb2da-754">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="fb2da-754">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="fb2da-755">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="fb2da-755">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="fb2da-756">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="fb2da-756">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="fb2da-757">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="fb2da-757">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="fb2da-758">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="fb2da-758">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fb2da-759">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fb2da-759">Az.Automation</span></span>
* <span data-ttu-id="fb2da-760">Get-AzAutomationJobOutputRecord wurde aktualisiert, um JSON- und Textdatensatzwerte zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="fb2da-760">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="fb2da-761">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="fb2da-761">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="fb2da-762">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="fb2da-762">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="fb2da-763">Das Verhalten von Start-AzAutomationDscCompilationJob wurde geändert, um den Auftrag einfach zu starten, anstatt auf dessen Abschluss zu warten</span><span class="sxs-lookup"><span data-stu-id="fb2da-763">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="fb2da-764">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="fb2da-764">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="fb2da-765">Fehlerbehebung für Get-AzAutomationDscNode, wenn die Verwendung von „-Name“ alle Knoten zurückgibt</span><span class="sxs-lookup"><span data-stu-id="fb2da-765">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="fb2da-766">Jetzt wird nur der übereinstimmende Knoten zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="fb2da-766">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fb2da-767">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fb2da-767">Az.Compute</span></span>
* <span data-ttu-id="fb2da-768">Parameter „ProtectFromScaleIn“ und „ProtectFromScaleSetAction“ wurden zum Cmdlet „Update-AzVmssVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-768">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="fb2da-769">Der jetzt festgelegte wimple-Parameter „New-AzVM“ verwendet standardmäßig einen verfügbaren Standort, wenn „East US“ (USA, Osten) nicht unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="fb2da-769">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fb2da-770">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fb2da-770">Az.DataLakeStore</span></span>
* <span data-ttu-id="fb2da-771">Das ADLS-SDK wurde aktualisiert, um „HttpClient“ zu verwenden und Datenebenentests wurden mit dem Azure-Framework integriert</span><span class="sxs-lookup"><span data-stu-id="fb2da-771">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="fb2da-772">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fb2da-772">Az.Monitor</span></span>
* <span data-ttu-id="fb2da-773">Fehlerbehebung bei falschen Parameternamen in Hilfebeispielen</span><span class="sxs-lookup"><span data-stu-id="fb2da-773">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fb2da-774">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fb2da-774">Az.Network</span></span>
* <span data-ttu-id="fb2da-775">DisableBgpRoutePropagation-Flag wurde zur Ausgabe der effektiven Routentabelle hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-775">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="fb2da-776">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="fb2da-776">Updated cmdlet:</span></span>
        - <span data-ttu-id="fb2da-777">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="fb2da-777">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="fb2da-778">Fehlerbehebung von doppeltem Bindestrich in Dokumentation von New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fb2da-778">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="fb2da-779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fb2da-779">Az.Resources</span></span>
* <span data-ttu-id="fb2da-780">Neues Cmdlet „Get-AzureRmDenyAssignment“ zum Abrufen von Ablehnungszuweisungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-780">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="fb2da-781">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fb2da-781">Az.Sql</span></span>
* <span data-ttu-id="fb2da-782">„Advanced Threat Protection“-Cmdlets in „Advanced Data Security“ umbenennen und Sicherheitsrisikobewertung standardmäßig aktivieren</span><span class="sxs-lookup"><span data-stu-id="fb2da-782">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="fb2da-783">2.0.0: Mai 2019</span><span class="sxs-lookup"><span data-stu-id="fb2da-783">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fb2da-784">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fb2da-784">Az.Accounts</span></span>
* <span data-ttu-id="fb2da-785">Authentifizierungsbibliothek aktualisiert, um ADFS-Probleme mit der Authentifizierung per Benutzername/Kennwort zu beheben</span><span class="sxs-lookup"><span data-stu-id="fb2da-785">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="fb2da-786">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fb2da-786">Az.CognitiveServices</span></span>
* <span data-ttu-id="fb2da-787">Ausschließliche Anzeige des Bing-Haftungsausschlusses für Bing-Suchdienste</span><span class="sxs-lookup"><span data-stu-id="fb2da-787">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="fb2da-788">Fehler behoben, der zu einem Fehler bei der Kontoerstellung führte</span><span class="sxs-lookup"><span data-stu-id="fb2da-788">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fb2da-789">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fb2da-789">Az.Compute</span></span>
* <span data-ttu-id="fb2da-790">Feature für die Näherungsplatzierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="fb2da-790">Proximity placement group feature.</span></span>
    - <span data-ttu-id="fb2da-791">Die folgenden neuen Cmdlets wurden hinzugefügt:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="fb2da-791">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="fb2da-792">Der neue Parameter „ProximityPlacementGroupId“ wurde zu den folgenden Cmdlets hinzugefügt:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="fb2da-792">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="fb2da-793">Der Parameter „StorageAccountType“ wurde zu „New-AzGalleryImageVersion“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fb2da-793">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="fb2da-794">„TargetRegion“ von „New-AzGalleryImageVersion“ kann „StorageAccountType“ enthalten.</span><span class="sxs-lookup"><span data-stu-id="fb2da-794">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="fb2da-795">Switch-Parameter „SkipShutdown“ wurde zu „Stop-AzVM“ und „Stop-AzVmss“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fb2da-795">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="fb2da-796">Wichtige Änderungen</span><span class="sxs-lookup"><span data-stu-id="fb2da-796">Breaking changes</span></span>
    - <span data-ttu-id="fb2da-797">„Set-AzVMBootDiagnostics“ in „Set-AzVMBootDiagnostic“ geändert</span><span class="sxs-lookup"><span data-stu-id="fb2da-797">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="fb2da-798">„Export-AzLogAnalyticThrottledRequests“ in „Export-AzLogAnalyticThrottledRequests“ geändert</span><span class="sxs-lookup"><span data-stu-id="fb2da-798">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="fb2da-799">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="fb2da-799">Az.DeploymentManager</span></span>
* <span data-ttu-id="fb2da-800">Erste allgemein verfügbare Version der Azure-Bereitstellungs-Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="fb2da-800">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="fb2da-801">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="fb2da-801">Az.Dns</span></span>
* <span data-ttu-id="fb2da-802">Automatische Delegierung des DNS-Namenservers</span><span class="sxs-lookup"><span data-stu-id="fb2da-802">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="fb2da-803">Das Cmdlet zum Erstellen einer DNS-Zone akzeptiert den übergeordneten Zonennamen als zusätzlichen optionalen Parameter.</span><span class="sxs-lookup"><span data-stu-id="fb2da-803">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="fb2da-804">NS-Einträge in der übergeordneten Zone für neu erstellte untergeordnete Zone hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-804">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="fb2da-805">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="fb2da-805">Az.FrontDoor</span></span>
* <span data-ttu-id="fb2da-806">Erste allgemein verfügbare Version der Azure Frontdoor-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="fb2da-806">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="fb2da-807">WAF-Cmdlets so umbenannt, dass sie „Waf“ enthalten</span><span class="sxs-lookup"><span data-stu-id="fb2da-807">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="fb2da-808">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="fb2da-808">Az.HDInsight</span></span>
* <span data-ttu-id="fb2da-809">Zwei Cmdlets entfernt:</span><span class="sxs-lookup"><span data-stu-id="fb2da-809">Removed two cmdlets:</span></span>
    - <span data-ttu-id="fb2da-810">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="fb2da-810">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="fb2da-811">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="fb2da-811">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="fb2da-812">Neues Cmdlet „Set-AzHDInsightGatewayCredential“ hinzugefügt, um „Grant-AzHDInsightHttpServicesAccess“ zu ersetzen</span><span class="sxs-lookup"><span data-stu-id="fb2da-812">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="fb2da-813">Cmdlet „Get-AzHDInsightJobOutput“ aktualisiert, um zwischen Leserrolle und HDInsight-Bedienerrolle zu unterscheiden:</span><span class="sxs-lookup"><span data-stu-id="fb2da-813">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="fb2da-814">Benutzer mit der Rolle „Leser“ müssen den Parameter „DefaultStorageAccountKey“ explizit angeben, andernfalls treten Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="fb2da-814">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="fb2da-815">Benutzer mit der Rolle des HDInsight-Bedieners sind nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="fb2da-815">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="fb2da-816">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fb2da-816">Az.Monitor</span></span>
* <span data-ttu-id="fb2da-817">Neue Cmdlets für SQR-API (Scheduled Query Rule, geplante Abfrageregel)</span><span class="sxs-lookup"><span data-stu-id="fb2da-817">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="fb2da-818">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="fb2da-818">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="fb2da-819">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="fb2da-819">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="fb2da-820">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="fb2da-820">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="fb2da-821">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="fb2da-821">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="fb2da-822">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="fb2da-822">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="fb2da-823">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="fb2da-823">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="fb2da-824">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="fb2da-824">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="fb2da-825">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="fb2da-825">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="fb2da-826">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="fb2da-826">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="fb2da-827">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="fb2da-827">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="fb2da-828">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="fb2da-828">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="fb2da-829">[Weitere Informationen](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) zur SQR-API</span><span class="sxs-lookup"><span data-stu-id="fb2da-829">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="fb2da-830">„Az.Monitor.md“ aktualisiert, um Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch) einzuschließen</span><span class="sxs-lookup"><span data-stu-id="fb2da-830">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fb2da-831">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fb2da-831">Az.Network</span></span>
* <span data-ttu-id="fb2da-832">Unterstützung für NAT-Gatewayressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-832">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="fb2da-833">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="fb2da-833">New cmdlets</span></span>
        - <span data-ttu-id="fb2da-834">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="fb2da-834">New-AzNatGateway</span></span>
        - <span data-ttu-id="fb2da-835">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="fb2da-835">Get-AzNatGateway</span></span>
        - <span data-ttu-id="fb2da-836">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="fb2da-836">Set-AzNatGateway</span></span>
        - <span data-ttu-id="fb2da-837">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="fb2da-837">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="fb2da-838">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="fb2da-838">Updated cmdlets</span></span>
        - <span data-ttu-id="fb2da-839">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="fb2da-839">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="fb2da-840">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="fb2da-840">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="fb2da-841">Folgende Befehle für das Feature aktualisiert: Benutzerdefinierte Routen für Brooklyn-Gateway festgelegt/entfernt</span><span class="sxs-lookup"><span data-stu-id="fb2da-841">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="fb2da-842">„New-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="fb2da-842">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="fb2da-843">„Set-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="fb2da-843">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="fb2da-844">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="fb2da-844">Az.PolicyInsights</span></span>
* <span data-ttu-id="fb2da-845">Unterstützung für die Abfrage von Richtlinienauswertungsdetails</span><span class="sxs-lookup"><span data-stu-id="fb2da-845">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="fb2da-846">Parameter „-Expand“ zu „Get-AzPolicyState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-846">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="fb2da-847">Unterstützung für „-Expand PolicyEvaluationDetails“</span><span class="sxs-lookup"><span data-stu-id="fb2da-847">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fb2da-848">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fb2da-848">Az.RecoveryServices</span></span>
* <span data-ttu-id="fb2da-849">Unterstützung für abonnementübergreifende Azure-zu-Azure-Sitewiederherstellung</span><span class="sxs-lookup"><span data-stu-id="fb2da-849">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="fb2da-850">Markierung anstehender wichtiger Änderungen für Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="fb2da-850">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="fb2da-851">Fehlerbehebung für Azure Site Recovery-Wiederherstellungsplan und -Aktionsplan</span><span class="sxs-lookup"><span data-stu-id="fb2da-851">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="fb2da-852">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Netzwerkzuordnung für Azure zu Azure</span><span class="sxs-lookup"><span data-stu-id="fb2da-852">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="fb2da-853">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Schutzrichtung für Azure zu Azure für verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="fb2da-853">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="fb2da-854">Weitere kleinere Korrekturen</span><span class="sxs-lookup"><span data-stu-id="fb2da-854">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="fb2da-855">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="fb2da-855">Az.Relay</span></span>
* <span data-ttu-id="fb2da-856">Korrektur von Tippfehlern in Kundennachrichten</span><span class="sxs-lookup"><span data-stu-id="fb2da-856">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="fb2da-857">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fb2da-857">Az.ServiceBus</span></span>
* <span data-ttu-id="fb2da-858">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-858">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fb2da-859">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fb2da-859">Az.Storage</span></span>
* <span data-ttu-id="fb2da-860">Upgrade auf Speicherclientbibliothek 10.0.1 (Namespace aller Objekte von diesem SDK von „Microsoft.WindowsAzure.Storage. *“ in „Microsoft.Azure.Storage.* “ geändert)</span><span class="sxs-lookup"><span data-stu-id="fb2da-860">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="fb2da-861">Upgrade auf Microsoft.Azure.Management.Storage 11.0.0, um die neue API-Version 2019-04-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="fb2da-861">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="fb2da-862">Art des Standardspeicherkontos bei der Speicherkontoerstellung von „Storage“ in „StorageV2“ geändert</span><span class="sxs-lookup"><span data-stu-id="fb2da-862">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="fb2da-863">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fb2da-863">New-AzStorageAccount</span></span>
* <span data-ttu-id="fb2da-864">Vom Speicherkonto-Cmdlet ausgegebener SKU-Name (Sku.Name) durch Hinzufügen eines Unterstrichs an SKU-Eingabename angepasst (Beispiel: „StandardLRS“ > „Standard_LRS“).</span><span class="sxs-lookup"><span data-stu-id="fb2da-864">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="fb2da-865">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fb2da-865">New-AzStorageAccount</span></span>
    - <span data-ttu-id="fb2da-866">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fb2da-866">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="fb2da-867">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fb2da-867">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fb2da-868">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fb2da-868">Az.Websites</span></span>
* <span data-ttu-id="fb2da-869">Die Eigenschaft „Kind“ wird nun für PSSite-Objekte festgelegt, die von „Get-AzWebApp“ zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fb2da-869">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="fb2da-870">„Get-AzWebApp\*Metrics“ und „Get-AzAppServicePlanMetrics“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-870">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="fb2da-871">1.8.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="fb2da-871">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="fb2da-872">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="fb2da-872">Highlights since the last major release</span></span>
* <span data-ttu-id="fb2da-873">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="fb2da-873">General availability of `Az` module</span></span>
* <span data-ttu-id="fb2da-874">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="fb2da-874">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="fb2da-875">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="fb2da-875">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="fb2da-876">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-876">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="fb2da-877">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-877">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="fb2da-878">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-878">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="fb2da-879">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="fb2da-879">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="fb2da-880">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fb2da-880">Az.Accounts</span></span>
* <span data-ttu-id="fb2da-881">„Uninstall-AzureRm“ aktualisiert, um Module unter Mac ordnungsgemäß zu löschen</span><span class="sxs-lookup"><span data-stu-id="fb2da-881">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="fb2da-882">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="fb2da-882">Az.Batch</span></span>
* <span data-ttu-id="fb2da-883">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="fb2da-883">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="fb2da-884">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="fb2da-884">Az.Cdn</span></span>
* <span data-ttu-id="fb2da-885">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="fb2da-885">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="fb2da-886">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fb2da-886">Az.CognitiveServices</span></span>
* <span data-ttu-id="fb2da-887">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="fb2da-887">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fb2da-888">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fb2da-888">Az.Compute</span></span>
* <span data-ttu-id="fb2da-889">Problem mit der AEM-Installation behoben, wenn die Ressourcen-IDs von Datenträgern Ressourcengruppen in Kleinbuchstaben enthielten</span><span class="sxs-lookup"><span data-stu-id="fb2da-889">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="fb2da-890">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="fb2da-890">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="fb2da-891">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-891">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fb2da-892">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fb2da-892">Az.DataFactory</span></span>
* <span data-ttu-id="fb2da-893">„SsisProperties“ hinzugefügt, falls „NodeCount“ für verwaltete Integration Runtime nicht NULL ist</span><span class="sxs-lookup"><span data-stu-id="fb2da-893">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fb2da-894">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fb2da-894">Az.DataLakeStore</span></span>
* <span data-ttu-id="fb2da-895">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="fb2da-895">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="fb2da-896">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="fb2da-896">Az.EventGrid</span></span>
* <span data-ttu-id="fb2da-897">Hilfetext für Endpunkt aktualisiert, um anzugeben, dass Ressourcen erstellt werden müssen, bevor die Cmdlets zum Erstellen/Aktualisieren von Ereignisabonnements verwendet werden</span><span class="sxs-lookup"><span data-stu-id="fb2da-897">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="fb2da-898">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="fb2da-898">Az.EventHub</span></span>
* <span data-ttu-id="fb2da-899">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-899">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="fb2da-900">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="fb2da-900">Az.HDInsight</span></span>
* <span data-ttu-id="fb2da-901">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="fb2da-901">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="fb2da-902">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="fb2da-902">Az.IotHub</span></span>
* <span data-ttu-id="fb2da-903">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="fb2da-903">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="fb2da-904">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fb2da-904">Az.KeyVault</span></span>
* <span data-ttu-id="fb2da-905">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="fb2da-905">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="fb2da-906">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-906">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="fb2da-907">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="fb2da-907">Az.MachineLearning</span></span>
* <span data-ttu-id="fb2da-908">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="fb2da-908">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="fb2da-909">Az.Media</span><span class="sxs-lookup"><span data-stu-id="fb2da-909">Az.Media</span></span>
* <span data-ttu-id="fb2da-910">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="fb2da-910">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="fb2da-911">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fb2da-911">Az.Monitor</span></span>
  * <span data-ttu-id="fb2da-912">Neue Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch)</span><span class="sxs-lookup"><span data-stu-id="fb2da-912">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="fb2da-913">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="fb2da-913">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="fb2da-914">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="fb2da-914">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="fb2da-915">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="fb2da-915">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="fb2da-916">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="fb2da-916">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="fb2da-917">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="fb2da-917">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="fb2da-918">Monitor SDK auf Version 0.22.0-preview aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-918">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fb2da-919">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fb2da-919">Az.Network</span></span>
* <span data-ttu-id="fb2da-920">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="fb2da-920">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="fb2da-921">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-921">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="fb2da-922">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="fb2da-922">Az.NotificationHubs</span></span>
* <span data-ttu-id="fb2da-923">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="fb2da-923">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="fb2da-924">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fb2da-924">Az.OperationalInsights</span></span>
* <span data-ttu-id="fb2da-925">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="fb2da-925">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="fb2da-926">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="fb2da-926">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="fb2da-927">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="fb2da-927">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fb2da-928">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fb2da-928">Az.RecoveryServices</span></span>
* <span data-ttu-id="fb2da-929">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="fb2da-929">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="fb2da-930">Tabellenformat für SQL auf Azure-VM aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-930">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="fb2da-931">Alternative Methode zum Abrufen des Speicherorts in „AzureFileShare“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-931">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="fb2da-932">„ScheduleRunDays“ in SchedulePolicy-Objekt gemäß Zeitzone aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-932">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="fb2da-933">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="fb2da-933">Az.RedisCache</span></span>
* <span data-ttu-id="fb2da-934">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="fb2da-934">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="fb2da-935">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fb2da-935">Az.Resources</span></span>
* <span data-ttu-id="fb2da-936">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-936">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="fb2da-937">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fb2da-937">Az.Sql</span></span>
* <span data-ttu-id="fb2da-938">Abhängigkeit vom Monitor SDK durch allgemeinen Code ersetzt</span><span class="sxs-lookup"><span data-stu-id="fb2da-938">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="fb2da-939">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="fb2da-939">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="fb2da-940">Verbesserter Prozess für Klassifizierung mehrerer Spalten</span><span class="sxs-lookup"><span data-stu-id="fb2da-940">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="fb2da-941">SKU-Eigenschaften (SKU-Name, Familie, Kapazität) in Antwort von „Get-AzSqlServerServiceObjective“ aufgenommen und standardmäßig als Tabelle formatiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-941">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="fb2da-942">Möglichkeit zum Ausführen von „Get-AzSqlServerServiceObjective“ nach Standort, ohne dass bereits ein Server in der Region vorhanden sein muss</span><span class="sxs-lookup"><span data-stu-id="fb2da-942">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="fb2da-943">Unterstützung für Zeitzonenparameter bei der Erstellung einer verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="fb2da-943">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="fb2da-944">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-944">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fb2da-945">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fb2da-945">Az.Websites</span></span>
* <span data-ttu-id="fb2da-946">„Set-AzWebApp“ und „Set-AzWebAppSlot“ korrigiert, sodass die Tags bei der Ausführung nicht entfernt werden</span><span class="sxs-lookup"><span data-stu-id="fb2da-946">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="fb2da-947">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="fb2da-947">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="fb2da-948">WebSites SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-948">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="fb2da-949">AdminSiteName-Eigenschaft aus „PSAppServicePlan“ entfernt</span><span class="sxs-lookup"><span data-stu-id="fb2da-949">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="fb2da-950">1.7.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="fb2da-950">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="fb2da-951">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="fb2da-951">Highlights since the last major release</span></span>
* <span data-ttu-id="fb2da-952">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="fb2da-952">General availability of `Az` module</span></span>
* <span data-ttu-id="fb2da-953">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="fb2da-953">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="fb2da-954">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="fb2da-954">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="fb2da-955">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-955">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="fb2da-956">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-956">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="fb2da-957">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-957">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="fb2da-958">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="fb2da-958">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="fb2da-959">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fb2da-959">Az.Accounts</span></span>
* <span data-ttu-id="fb2da-960">„Add-AzEnvironment“ und „Set-AzEnvironment“ aktualisiert, um den Parameter „AzureAnalysisServicesEndpointResourceId“ zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="fb2da-960">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="fb2da-961">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fb2da-961">Az.AnalysisServices</span></span>
* <span data-ttu-id="fb2da-962">ServiceClient wird in Cmdlets für die Datenebene verwendet, und die ursprüngliche Authentifizierungslogik wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="fb2da-962">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="fb2da-963">„Add-AzureASAccount“ wird als Wrapper von „Connect-AzAccount“ festgelegt, um einen Breaking Change zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="fb2da-963">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fb2da-964">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fb2da-964">Az.Automation</span></span>
* <span data-ttu-id="fb2da-965">Fehler des Cmdlets „Fixed New-AzAutomationSoftwareUpdateConfiguration“ für Einschlüsse behoben.</span><span class="sxs-lookup"><span data-stu-id="fb2da-965">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="fb2da-966">Die Parameter „IncludedKbNumber“ und „IncludedPackageNameMask“ sollten nun funktionieren.</span><span class="sxs-lookup"><span data-stu-id="fb2da-966">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="fb2da-967">Fehlerbehebung für eine dynamische Gruppe der Azure Automation-Updateverwaltung</span><span class="sxs-lookup"><span data-stu-id="fb2da-967">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fb2da-968">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fb2da-968">Az.Compute</span></span>
* <span data-ttu-id="fb2da-969">Parameter „HyperVGeneration“ zu „New-AzDiskConfig“ und „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-969">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="fb2da-970">Zulassen der VM-Erstellung mit einem Katalogimage aus anderen Mandanten</span><span class="sxs-lookup"><span data-stu-id="fb2da-970">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="fb2da-971">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="fb2da-971">Az.ContainerInstance</span></span>
* <span data-ttu-id="fb2da-972">Problem im Parameter „-Command“ von „New-AzContainerGroup“ behoben, das dazu führte, dass ein nachgestelltes leeres Argument hinzugefügt wurde</span><span class="sxs-lookup"><span data-stu-id="fb2da-972">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fb2da-973">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fb2da-973">Az.DataFactory</span></span>
* <span data-ttu-id="fb2da-974">Version des ADF .NET SDK auf 3.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-974">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="fb2da-975">Cmdlet „Set-AzDataFactoryV2“ mit zusätzlichen Parametern für RepoConfiguration-Einstellungen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-975">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="fb2da-976">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fb2da-976">Az.Resources</span></span>
* <span data-ttu-id="fb2da-977">Verarbeitung von Anbietern für „Get-AzResource“ bei der Angabe der Parameter „-ResourceId“ oder „-ResourceGroupName“, „-Name“ und „-ResourceType“ verbessert</span><span class="sxs-lookup"><span data-stu-id="fb2da-977">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="fb2da-978">Fehlerbehandlung für „Test-AzDeployment“ und „Test-AzResourceGroupDeployment“ verbessert</span><span class="sxs-lookup"><span data-stu-id="fb2da-978">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="fb2da-979">Behandlung von außerhalb der Bereitstellungsüberprüfung aufgetretenen Fehlern und stattdessen Aufnahme in die Ausgabe des Befehls</span><span class="sxs-lookup"><span data-stu-id="fb2da-979">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="fb2da-980">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="fb2da-980">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="fb2da-981">Switch-Parameter „-IgnoreDynamicParameters“ zu Bereitstellungs-Cmdlets hinzugefügt, um Aufforderung in Skript- und Auftragsszenarien zu überspringen</span><span class="sxs-lookup"><span data-stu-id="fb2da-981">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="fb2da-982">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="fb2da-982">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="fb2da-983">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fb2da-983">Az.Sql</span></span>
* <span data-ttu-id="fb2da-984">Unterstützung für Klassifizierung von Datenbankdaten</span><span class="sxs-lookup"><span data-stu-id="fb2da-984">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fb2da-985">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fb2da-985">Az.Storage</span></span>
* <span data-ttu-id="fb2da-986">Melden eines ausführlichen Fehlers beim Erstellen des Storage-Kontexts mit dem Parameter „-UseConnectedAccount“, aber ohne Azure-Anmeldekonto</span><span class="sxs-lookup"><span data-stu-id="fb2da-986">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="fb2da-987">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="fb2da-987">New-AzStorageContext</span></span>
* <span data-ttu-id="fb2da-988">Unterstützung für das Verwalten von Blobdiensteigenschaften eines bestimmten Storage-Kontos mit einer API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="fb2da-988">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="fb2da-989">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="fb2da-989">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="fb2da-990">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="fb2da-990">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="fb2da-991">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="fb2da-991">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="fb2da-992">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="fb2da-992">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="fb2da-993">Unterstützung von „-AsJob“ für Cmdlets für den Upload und Download von Blobs und Dateien</span><span class="sxs-lookup"><span data-stu-id="fb2da-993">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="fb2da-994">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="fb2da-994">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="fb2da-995">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="fb2da-995">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="fb2da-996">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="fb2da-996">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="fb2da-997">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="fb2da-997">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="fb2da-998">1.6.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="fb2da-998">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="fb2da-999">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="fb2da-999">Highlights since the last major release</span></span>
* <span data-ttu-id="fb2da-1000">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="fb2da-1000">General availability of `Az` module</span></span>
* <span data-ttu-id="fb2da-1001">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1001">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="fb2da-1002">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1002">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="fb2da-1003">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1003">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="fb2da-1004">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1004">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="fb2da-1005">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1005">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="fb2da-1006">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="fb2da-1006">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fb2da-1007">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fb2da-1007">Az.Automation</span></span>
* <span data-ttu-id="fb2da-1008">Änderung an der Azure Automation-Updateverwaltung, um die folgenden neuen Features zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="fb2da-1008">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="fb2da-1009">Dynamische Gruppierung</span><span class="sxs-lookup"><span data-stu-id="fb2da-1009">Dynamic grouping</span></span>
    * <span data-ttu-id="fb2da-1010">Pre-/Post-Skripts</span><span class="sxs-lookup"><span data-stu-id="fb2da-1010">Pre-Post script</span></span>
    * <span data-ttu-id="fb2da-1011">Neustarteinstellung</span><span class="sxs-lookup"><span data-stu-id="fb2da-1011">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fb2da-1012">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fb2da-1012">Az.Compute</span></span>
* <span data-ttu-id="fb2da-1013">Problem mit der Pfadauflösung in „Get-AzVmBootDiagnosticsData“ behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-1013">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="fb2da-1014">Computeclientbibliothek auf 25.0.0. aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1014">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="fb2da-1015">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fb2da-1015">Az.KeyVault</span></span>
* <span data-ttu-id="fb2da-1016">Unterstützung für Platzhalterzeichen zu KeyVault-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1016">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fb2da-1017">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fb2da-1017">Az.Network</span></span>
* <span data-ttu-id="fb2da-1018">Threat Intelligence-Unterstützung für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1018">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="fb2da-1019">Ressource der obersten Ebene für Application Gateway-Firewallrichtlinie und benutzerdefinierte Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1019">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fb2da-1020">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fb2da-1020">Az.RecoveryServices</span></span>
* <span data-ttu-id="fb2da-1021">SnapshotRetentionInDays in Azure-VM-Richtlinie hinzugefügt, um sofortigen Wiederherstellungspunkt zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="fb2da-1021">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="fb2da-1022">Pipe-Unterstützung für das Aufheben der Registrierung eines Containers hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1022">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="fb2da-1023">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fb2da-1023">Az.Resources</span></span>
* <span data-ttu-id="fb2da-1024">Unterstützung für Platzhalterzeichen für Get-AzResource und Get-AzResourceGroup aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1024">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="fb2da-1025">Anmeldeinformationen aktualisiert, die beim Senden generischer Aufrufe an ARM verwendet werden</span><span class="sxs-lookup"><span data-stu-id="fb2da-1025">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="fb2da-1026">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fb2da-1026">Az.Sql</span></span>
* <span data-ttu-id="fb2da-1027">Der Cmdlet-Parameter der Bedrohungserkennung (ExcludeDetectionType) wurde von „DetectionType“ in „string[]“ geändert, um ihn zukunftssicher zu machen, wenn neue DetectionTypes-Elemente hinzugefügt werden, und um AutoVervollständigen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1027">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fb2da-1028">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fb2da-1028">Az.Storage</span></span>
* <span data-ttu-id="fb2da-1029">Unterstützung von Get-/Set-/Remove-Verwaltungsrichtlinien für Speicherkonto hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1029">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="fb2da-1030">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="fb2da-1030">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="fb2da-1031">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="fb2da-1031">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="fb2da-1032">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="fb2da-1032">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="fb2da-1033">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="fb2da-1033">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="fb2da-1034">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="fb2da-1034">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="fb2da-1035">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="fb2da-1035">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fb2da-1036">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fb2da-1036">Az.Websites</span></span>
* <span data-ttu-id="fb2da-1037">ARM-Vorlagenfehler behoben, der zu einem Problem beim Klonen aller Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ führte</span><span class="sxs-lookup"><span data-stu-id="fb2da-1037">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="fb2da-1038">1.5.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="fb2da-1038">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fb2da-1039">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fb2da-1039">Az.Accounts</span></span>
* <span data-ttu-id="fb2da-1040">Der Befehl „Register-AzModule“ wurde hinzugefügt, um von AutoRest generierte Cmdlets zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1040">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="fb2da-1041">Beispiele für „Connect-AzAccount“ wurden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1041">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fb2da-1042">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fb2da-1042">Az.Automation</span></span>
* <span data-ttu-id="fb2da-1043">Problem behoben, das beim Abrufen bestimmter monatlicher Zeitpläne in verschiedenen Azure Automation-Cmdlets auftrat</span><span class="sxs-lookup"><span data-stu-id="fb2da-1043">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="fb2da-1044">„Get-AzAutomationDscNode“ wurde korrigiert, da nur die 20 obersten Knoten zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1044">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="fb2da-1045">Jetzt werden alle Knoten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1045">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="fb2da-1046">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="fb2da-1046">Az.Cdn</span></span>
* <span data-ttu-id="fb2da-1047">Neue Powershell-Cmdlets zum Aktivieren/Deaktivieren von HTTPS für benutzerdefinierte Domänen hinzugefügt und alte Cmdlets außer Betrieb genommen</span><span class="sxs-lookup"><span data-stu-id="fb2da-1047">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fb2da-1048">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fb2da-1048">Az.Compute</span></span>
* <span data-ttu-id="fb2da-1049">Unterstützung für Platzhalterzeichen zu Get-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1049">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fb2da-1050">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fb2da-1050">Az.DataFactory</span></span>
* <span data-ttu-id="fb2da-1051">Version des ADF .NET SDK auf 3.0.1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1051">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="fb2da-1052">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="fb2da-1052">Az.LogicApp</span></span>
* <span data-ttu-id="fb2da-1053">„ListWorkflows“ wurde korrigiert, da nur die erste Seite mit Ergebnissen abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1053">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fb2da-1054">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fb2da-1054">Az.Network</span></span>
* <span data-ttu-id="fb2da-1055">Unterstützung für Platzhalterzeichen zu Network-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1055">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fb2da-1056">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fb2da-1056">Az.RecoveryServices</span></span>
* <span data-ttu-id="fb2da-1057">SQL Server jetzt in Azure-VM-Support enthalten</span><span class="sxs-lookup"><span data-stu-id="fb2da-1057">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="fb2da-1058">SDK-Update</span><span class="sxs-lookup"><span data-stu-id="fb2da-1058">SDK Update</span></span>
* <span data-ttu-id="fb2da-1059">VMappContainer-Überprüfung in „Get-ProtectableItem“ entfernt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1059">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="fb2da-1060">„Name“ und „ServerName“ als Parameter für „Get-ProtectableItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1060">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="fb2da-1061">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fb2da-1061">Az.Resources</span></span>
* <span data-ttu-id="fb2da-1062">Parameter `-TemplateObject` zu Bereitstellungs-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1062">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="fb2da-1063">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="fb2da-1063">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="fb2da-1064">Problem beim Piping des Ergebnisses von `Get-AzResource` an `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-1064">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="fb2da-1065">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="fb2da-1065">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="fb2da-1066">Problem mit JSON-Datentypänderung beim Ausführen von `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-1066">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="fb2da-1067">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="fb2da-1067">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="fb2da-1068">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fb2da-1068">Az.Sql</span></span>
* <span data-ttu-id="fb2da-1069">„AuditingEndpointsCommunicator“ wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1069">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="fb2da-1070">Das Verhalten eines Grenzfalls beim Erstellen neuer Diagnoseeinstellungen wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1070">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fb2da-1071">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fb2da-1071">Az.Storage</span></span>
* <span data-ttu-id="fb2da-1072">Unterstützung von „Kind BlockBlobStorage“ beim Erstellen eines Speicherkontos: New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fb2da-1072">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="fb2da-1073">1.4.0 – Februar 2019</span><span class="sxs-lookup"><span data-stu-id="fb2da-1073">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="fb2da-1074">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fb2da-1074">Az.AnalysisServices</span></span>
* <span data-ttu-id="fb2da-1075">Cmdlet „AddAzureASAccount“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1075">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fb2da-1076">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fb2da-1076">Az.Automation</span></span>
* <span data-ttu-id="fb2da-1077">Hilfe für „Import-AzAutomationDscNodeConfiguration“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1077">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="fb2da-1078">Überprüfung des Konfigurationsnamens zu Cmdlet „Import-AzAutomationDscConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1078">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="fb2da-1079">Fehlerbehandlung für Cmdlet „Import-AzAutomationDscConfiguration“ verbessert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1079">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="fb2da-1080">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fb2da-1080">Az.CognitiveServices</span></span>
* <span data-ttu-id="fb2da-1081">„CustomSubdomainName“ als neuer optionaler Parameter für Cmdlet „New-AzCognitiveServicesAccount“ hinzugefügt, das zum Angeben der Unterdomäne für die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1081">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fb2da-1082">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fb2da-1082">Az.Compute</span></span>
* <span data-ttu-id="fb2da-1083">Problem mit ID-Parametersätzen behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-1083">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="fb2da-1084">„Get-AzVMExtension“ aktualisiert, sodass alle installierten Erweiterungen aufgelistet werden, wenn der Name-Parameter nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="fb2da-1084">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="fb2da-1085">Parameter „Tag“ und „ResourceId“ zum Cmdlet „Update-AzImage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1085">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="fb2da-1086">„Get-AzVmssVM“ ohne Instanz-ID und mit „InstanceView“ können virtuelle VMSS-Computer mit Instanzansicht auflisten.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1086">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fb2da-1087">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fb2da-1087">Az.DataLakeStore</span></span>
* <span data-ttu-id="fb2da-1088">Cmdlets zum Auflisten und Wiederherstellen gelöschter ADL-Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1088">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="fb2da-1089">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="fb2da-1089">Az.EventHub</span></span>
* <span data-ttu-id="fb2da-1090">Neue boolesche Eigenschaft „SkipEmptyArchives“ zum Überspringen leerer Archive in Klasse „CaptureDescription“ von EventHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1090">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="fb2da-1091">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fb2da-1091">Az.KeyVault</span></span>
* <span data-ttu-id="fb2da-1092">Kennzeichnung in „Set-AzKeyVaultSecret“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1092">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="fb2da-1093">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="fb2da-1093">Az.LogicApp</span></span>
* <span data-ttu-id="fb2da-1094">SKU „Basic“ für Integrationskonten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1094">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="fb2da-1095">XSLT 2.0, XSLT 3.0 und Liquid-Zuordnungstypen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1095">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="fb2da-1096">Neue Cmdlets für Integrationskonto-Assemblys</span><span class="sxs-lookup"><span data-stu-id="fb2da-1096">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="fb2da-1097">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="fb2da-1097">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="fb2da-1098">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="fb2da-1098">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="fb2da-1099">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="fb2da-1099">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="fb2da-1100">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="fb2da-1100">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="fb2da-1101">Neue Cmdlets für Integrationskonto-Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="fb2da-1101">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="fb2da-1102">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb2da-1102">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="fb2da-1103">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb2da-1103">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="fb2da-1104">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb2da-1104">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="fb2da-1105">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb2da-1105">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="fb2da-1106">Logik-App-SDK auf Version 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1106">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="fb2da-1107">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fb2da-1107">Az.Monitor</span></span>
* <span data-ttu-id="fb2da-1108">Hilfe für „Get-AzMetric“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1108">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fb2da-1109">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fb2da-1109">Az.Network</span></span>
* <span data-ttu-id="fb2da-1110">Hilfebeispiel für „Add-AzApplicationGatewayCustomError“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1110">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="fb2da-1111">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fb2da-1111">Az.OperationalInsights</span></span>
* <span data-ttu-id="fb2da-1112">Zusätzliche Unterstützung für Datenquelle von „New-ApplicationInsights“ und „Get-ApplicationInsights“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1112">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="fb2da-1113">Neue Art von „ApplicationInsights“ zum Abrufen von bestimmten und von allen ApplicationInsights-Datenquellen für einen Workspace hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1113">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="fb2da-1114">Cmdlet „New-AzOperationalInsightsApplicationInsightsDataSource“ zum Erstellen einer Datenquelle anhand des angegebenen Ressourcenparameters für „Application-Insights“ hinzugefügt: „subscriptionId“, „resourceGroupName“ und „name“.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1114">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="fb2da-1115">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fb2da-1115">Az.Resources</span></span>
* <span data-ttu-id="fb2da-1116">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="fb2da-1116">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="fb2da-1117">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="fb2da-1117">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="fb2da-1118">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="fb2da-1118">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="fb2da-1119">Fehler korrigiert, der die wiederholte Erstellung von „KeyCredentials“ verhindert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1119">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="fb2da-1120">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fb2da-1120">Az.Sql</span></span>
* <span data-ttu-id="fb2da-1121">Unterstützung für SQL DB Hyperscale-Tarif hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1121">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="fb2da-1122">Fehler korrigiert, aufgrund dessen die Wiederherstellung wegen der Festlegung unnötiger Eigenschaften in der Wiederherstellungsanforderung fehlschlagen konnte</span><span class="sxs-lookup"><span data-stu-id="fb2da-1122">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fb2da-1123">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fb2da-1123">Az.Websites</span></span>
* <span data-ttu-id="fb2da-1124">Beispiel in „Get-AzWebAppSlotMetrics“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1124">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="fb2da-1125">1.3.0: Februar 2019</span><span class="sxs-lookup"><span data-stu-id="fb2da-1125">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fb2da-1126">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fb2da-1126">Az.Accounts</span></span>
* <span data-ttu-id="fb2da-1127">Update auf die aktuelle Version von ClientRuntime durchgeführt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1127">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="fb2da-1128">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fb2da-1128">Az.AnalysisServices</span></span>
<span data-ttu-id="fb2da-1129">Allgemeine Verfügbarkeit für Az.AnalysisServices-Modul</span><span class="sxs-lookup"><span data-stu-id="fb2da-1129">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fb2da-1130">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fb2da-1130">Az.Compute</span></span>
* <span data-ttu-id="fb2da-1131">AEM-Erweiterung: Unterstützung für UltraSSD und P60-, P70- und P80-Datenträger hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1131">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="fb2da-1132">Hilfebeschreibung für „Set-AzVMBootDiagnostics“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1132">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="fb2da-1133">Hilfebeschreibung und Beispiel für „Update-AzImage“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1133">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fb2da-1134">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fb2da-1134">Az.RecoveryServices</span></span>
<span data-ttu-id="fb2da-1135">Allgemeine Verfügbarkeit für Az.RecoveryServices-Modul.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1135">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="fb2da-1136">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fb2da-1136">Az.Resources</span></span>
* <span data-ttu-id="fb2da-1137">Kennzeichnung für Ressourcengruppen korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1137">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="fb2da-1138">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="fb2da-1138">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="fb2da-1139">Problem behoben, bei dem „-ErrorAction“ von `Get-AzureRmRoleAssignment` nicht berücksichtigt wird</span><span class="sxs-lookup"><span data-stu-id="fb2da-1139">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="fb2da-1140">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="fb2da-1140">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="fb2da-1141">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fb2da-1141">Az.Sql</span></span>
* <span data-ttu-id="fb2da-1142">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1142">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="fb2da-1143">Problem behoben, bei dem eine fehlende Anmeldung am Azure-Konto bei der Ausführung von SQL-Cmdlets zu einer nullref-Ausnahme führt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1143">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="fb2da-1144">nullref-Ausnahme in Get-AzSqlCapability korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1144">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="fb2da-1145">1.2.1: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="fb2da-1145">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fb2da-1146">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fb2da-1146">Az.Accounts</span></span>
* <span data-ttu-id="fb2da-1147">Release mit richtiger Version der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="fb2da-1147">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="fb2da-1148">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fb2da-1148">Az.AnalysisServices</span></span>
* <span data-ttu-id="fb2da-1149">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="fb2da-1149">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fb2da-1150">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fb2da-1150">Az.RecoveryServices</span></span>
* <span data-ttu-id="fb2da-1151">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="fb2da-1151">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="fb2da-1152">1.2.0: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="fb2da-1152">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fb2da-1153">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fb2da-1153">Az.Accounts</span></span>
* <span data-ttu-id="fb2da-1154">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1154">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="fb2da-1155">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1155">Update incorrect online help URLs</span></span>
* <span data-ttu-id="fb2da-1156">Warnmeldung in PS Core für „Uninstall-AzureRm“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1156">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="fb2da-1157">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="fb2da-1157">Az.Aks</span></span>
* <span data-ttu-id="fb2da-1158">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1158">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fb2da-1159">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fb2da-1159">Az.Automation</span></span>
* <span data-ttu-id="fb2da-1160">Unterstützung für Python 2-Runbooks hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1160">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="fb2da-1161">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1161">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="fb2da-1162">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="fb2da-1162">Az.Cdn</span></span>
* <span data-ttu-id="fb2da-1163">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1163">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fb2da-1164">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fb2da-1164">Az.Compute</span></span>
* <span data-ttu-id="fb2da-1165">Cmdlet „Invoke-AzVMReimage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1165">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="fb2da-1166">Parameter „TempDisk“ zu „Set-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1166">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="fb2da-1167">Warnmeldung von „New-AzVM“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1167">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="fb2da-1168">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fb2da-1168">Az.ContainerRegistry</span></span>
* <span data-ttu-id="fb2da-1169">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1169">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fb2da-1170">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fb2da-1170">Az.DataFactory</span></span>
* <span data-ttu-id="fb2da-1171">Version des ADF .NET SDK auf 3.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1171">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fb2da-1172">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fb2da-1172">Az.DataLakeStore</span></span>
* <span data-ttu-id="fb2da-1173">Problem mit ADLS-Endpunkt bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-1173">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="fb2da-1174">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="fb2da-1174">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="fb2da-1175">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1175">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="fb2da-1176">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="fb2da-1176">Az.IotHub</span></span>
* <span data-ttu-id="fb2da-1177">Codierungsformat zu Cmdlet „Add-IotHubRoutingEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1177">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="fb2da-1178">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fb2da-1178">Az.KeyVault</span></span>
* <span data-ttu-id="fb2da-1179">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1179">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fb2da-1180">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fb2da-1180">Az.Network</span></span>
* <span data-ttu-id="fb2da-1181">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1181">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="fb2da-1182">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fb2da-1182">Az.Resources</span></span>
* <span data-ttu-id="fb2da-1183">Fehlerhafte Beispiele in Referenzdokumentation zu „New-AzADAppCredential“ und „New-AzADSpCredential“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1183">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="fb2da-1184">Problem behoben, bei dem der Pfad für den Parameter „-TemplateFile“ nicht aufgelöst wurde, bevor Cmdlets für die Bereitstellung von Ressourcengruppen ausgeführt wurden</span><span class="sxs-lookup"><span data-stu-id="fb2da-1184">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="fb2da-1185">Az.Resources: Richtige Dokumentation für Standardwert von „New-AzureRmPolicyDefinition -Mode“ bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1185">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="fb2da-1186">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="fb2da-1186">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="fb2da-1187">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="fb2da-1187">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="fb2da-1188">Formatierungsproblem für Objekt „PSResourceGroupDeployment“ behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-1188">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="fb2da-1189">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="fb2da-1189">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="fb2da-1190">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fb2da-1190">Az.ServiceFabric</span></span>
* <span data-ttu-id="fb2da-1191">Rollback beim Hinzufügen eines Zertifikats zum VMSS-Modell, Auslösung einer Ausnahme. Fehlerbehebung: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="fb2da-1191">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="fb2da-1192">Einige Fehlermeldungen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1192">Fix some error messages.</span></span>
* <span data-ttu-id="fb2da-1193">Fehler bei Clustererstellung mit ARM-Standardvorlage für „New-AzServiceFabriCluster“ behoben, bei dem die Migration zu Az nicht funktioniert hat.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1193">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="fb2da-1194">Fehler behoben beim Hinzufügen eines Cluster-/Anwendungszertifikats ausschließlich zu VM Scale Sets, die zum Cluster gehören, indem die Cluster-ID in der Erweiterung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1194">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="fb2da-1195">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="fb2da-1195">Az.SignalR</span></span>
* <span data-ttu-id="fb2da-1196">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1196">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="fb2da-1197">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fb2da-1197">Az.Sql</span></span>
* <span data-ttu-id="fb2da-1198">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1198">Update incorrect online help URLs</span></span>
* <span data-ttu-id="fb2da-1199">Parameterbeschreibung für den Parameter „LicenseType“ mit möglichen Werten aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1199">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="fb2da-1200">Fehler behoben, bei dem die Aktualisierung der Identität der verwalteten Instanz nicht funktioniert hat, wenn es sich um die einzige aktualisierte Eigenschaft gehandelt hat</span><span class="sxs-lookup"><span data-stu-id="fb2da-1200">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="fb2da-1201">Unterstützung für die benutzerdefinierte Sortierung auf verwalteter Instanz</span><span class="sxs-lookup"><span data-stu-id="fb2da-1201">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fb2da-1202">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fb2da-1202">Az.Storage</span></span>
* <span data-ttu-id="fb2da-1203">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1203">Update incorrect online help URLs</span></span>
* <span data-ttu-id="fb2da-1204">Ausführliche Fehlermeldung beim Abrufen/Festlegen der klassischen Protokollierung bzw. Metriken für Storage Premium-Konto, da für das Storage Premium-Konto die klassische Protokollierung bzw. Metriken nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1204">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="fb2da-1205">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="fb2da-1205">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="fb2da-1206">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="fb2da-1206">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="fb2da-1207">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="fb2da-1207">Az.TrafficManager</span></span>
* <span data-ttu-id="fb2da-1208">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1208">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fb2da-1209">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fb2da-1209">Az.Websites</span></span>
* <span data-ttu-id="fb2da-1210">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1210">Update incorrect online help URLs</span></span>
* <span data-ttu-id="fb2da-1211">„New-AzWebAppSSLBinding“ korrigiert, damit das Zertifikat in die richtige Ressourcengruppe bzw. an den richtigen Speicherort hochgeladen wird, wenn die App in einer ASE gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1211">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="fb2da-1212">„New-AzWebAppSSLBinding“ korrigiert, damit die Tags beim Binden eines SSL-Zertifikats an eine App nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1212">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="fb2da-1213">1.1.0 – Januar 2019</span><span class="sxs-lookup"><span data-stu-id="fb2da-1213">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fb2da-1214">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fb2da-1214">Az.Accounts</span></span>
* <span data-ttu-id="fb2da-1215">Bereich „Local“ zu „Enable-AzureRmAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1215">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fb2da-1216">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fb2da-1216">Az.Compute</span></span>
* <span data-ttu-id="fb2da-1217">Name ist jetzt optional im ID-Parametersatz für „Restart/Start/Stop/Remove/Set-AzVM“ und „Save-AzVMImage“</span><span class="sxs-lookup"><span data-stu-id="fb2da-1217">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="fb2da-1218">Beschreibung der ID in Hilfedateien aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1218">Updated the description of ID in help files</span></span>
* <span data-ttu-id="fb2da-1219">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-1219">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fb2da-1220">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fb2da-1220">Az.DataLakeStore</span></span>
* <span data-ttu-id="fb2da-1221">Aktualisierung der SDK-Version der Datenebene auf 1.1.14 für SDK-Fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1221">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="fb2da-1222">Behandlung von negativen acesstime- and modificationtime-Werten für „getfilestatus“ und „liststatus“ korrigiert, asynchrones Abbruchtoken korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1222">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="fb2da-1223">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="fb2da-1223">Az.EventGrid</span></span>
* <span data-ttu-id="fb2da-1224">Zur Verwendung der API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1224">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="fb2da-1225">Aktualisierung der folgenden Cmdlets zur Unterstützung des neuen Szenarios in der API-Version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="fb2da-1225">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="fb2da-1226">New-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="fb2da-1226">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="fb2da-1227">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="fb2da-1227">Event Time-To-Live,</span></span>
        - <span data-ttu-id="fb2da-1228">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="fb2da-1228">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="fb2da-1229">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="fb2da-1229">Dead letter endpoint.</span></span>
    - <span data-ttu-id="fb2da-1230">Update-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="fb2da-1230">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="fb2da-1231">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="fb2da-1231">Event Time-To-Live,</span></span>
        - <span data-ttu-id="fb2da-1232">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="fb2da-1232">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="fb2da-1233">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="fb2da-1233">Dead letter endpoint.</span></span>
* <span data-ttu-id="fb2da-1234">Neue Enumerationswerte („storageQueue“ und „hybridConnection“) für die EndpointType-Option in den Cmdlets „New-AzureRmEventGridSubscription“ und „Update-AzureRmEventGridSubscription“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1234">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="fb2da-1235">Anzeige einer Warnmeldung, wenn das Erstellen oder Aktualisieren des Ereignisabonnements voraussichtlich eine manuelle Aktion des Benutzers zur Folge hat</span><span class="sxs-lookup"><span data-stu-id="fb2da-1235">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="fb2da-1236">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="fb2da-1236">Az.IotHub</span></span>
* <span data-ttu-id="fb2da-1237">Auf die aktuelle Version des Iot Hub SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1237">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="fb2da-1238">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="fb2da-1238">Az.LogicApp</span></span>
* <span data-ttu-id="fb2da-1239">„Get-AzLogicApp“ listet alle Apps ohne angegebenen Namen auf</span><span class="sxs-lookup"><span data-stu-id="fb2da-1239">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="fb2da-1240">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fb2da-1240">Az.Resources</span></span>
* <span data-ttu-id="fb2da-1241">Problem mit dem Parametersatz bei Angabe der Parameter „-ODataQuery“ und „-ResourceId“ für „Get-AzResource“ behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-1241">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="fb2da-1242">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="fb2da-1242">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="fb2da-1243">Behandlung des Parameters „-Custom“ in „New/Set-AzPolicyDefinition“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1243">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="fb2da-1244">Tippfehler in der Dokumentation für „New-AzDeployment“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1244">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="fb2da-1245">Parameter „-MailNickname“ als obligatorisch festgelegt für „New-AzADUser“</span><span class="sxs-lookup"><span data-stu-id="fb2da-1245">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="fb2da-1246">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="fb2da-1246">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="fb2da-1247">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="fb2da-1247">Az.SignalR</span></span>
* <span data-ttu-id="fb2da-1248">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-1248">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="fb2da-1249">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fb2da-1249">Az.Sql</span></span>
* <span data-ttu-id="fb2da-1250">Abhängigkeit des Speicherverwaltungsclients zur allgemeinen SDK-Implementierung konvertiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1250">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fb2da-1251">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fb2da-1251">Az.Storage</span></span>
* <span data-ttu-id="fb2da-1252">Festlegung des „StorageAccountName“ des Speicherkontexts als tatsächlichen Namen des Speicherkontos, wenn dieser mit „SAS-Token“, „OAuth“ oder „Anonym“ erstellt wird</span><span class="sxs-lookup"><span data-stu-id="fb2da-1252">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="fb2da-1253">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="fb2da-1253">New-AzStorageContext</span></span>
* <span data-ttu-id="fb2da-1254">Erstellen von SAS-Token des Blob-Momentaufnahmeobjekts mit dem Parameter „-FullUri“, Festlegung des zurückgegebenen URI als Momentaufnahme-URI</span><span class="sxs-lookup"><span data-stu-id="fb2da-1254">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="fb2da-1255">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="fb2da-1255">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fb2da-1256">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fb2da-1256">Az.Websites</span></span>
* <span data-ttu-id="fb2da-1257">Fehler bei der Datumsanalyse in „Get-AzDeletedWebApp“ behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-1257">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="fb2da-1258">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-1258">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="fb2da-1259">1.0.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="fb2da-1259">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="fb2da-1260">Allgemein</span><span class="sxs-lookup"><span data-stu-id="fb2da-1260">General</span></span>

- <span data-ttu-id="fb2da-1261">Allgemeine Verfügbarkeit des Az-Moduls</span><span class="sxs-lookup"><span data-stu-id="fb2da-1261">General Availability of Az Module</span></span>
- <span data-ttu-id="fb2da-1262">Onlinehilfe für jedes Modul</span><span class="sxs-lookup"><span data-stu-id="fb2da-1262">Online help for each module</span></span>
- <span data-ttu-id="fb2da-1263">Ausführlichere Informationen und eine Roadmap finden Sie auf der [Seite mit der Ankündigung zu Az](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="fb2da-1263">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="fb2da-1264">Informationen zur Migration aus AzureRM finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fb2da-1264">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="fb2da-1265">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fb2da-1265">Az.Accounts</span></span>
- <span data-ttu-id="fb2da-1266">Geändert von Az.Profile</span><span class="sxs-lookup"><span data-stu-id="fb2da-1266">Changed from Az.Profile</span></span>
- <span data-ttu-id="fb2da-1267">Feste Tabellenformate für Profil- und Kontexttypen</span><span class="sxs-lookup"><span data-stu-id="fb2da-1267">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="fb2da-1268">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fb2da-1268">Az.ApiManagement</span></span>
- <span data-ttu-id="fb2da-1269">Korrekturen für #7002</span><span class="sxs-lookup"><span data-stu-id="fb2da-1269">Fixes for #7002</span></span>
- <span data-ttu-id="fb2da-1270">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fb2da-1270">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="fb2da-1271">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="fb2da-1271">Az.Batch</span></span>
- <span data-ttu-id="fb2da-1272">Möglichkeit zum Anzeigen der ausgeführten Version des Azure Batch-Knoten-Agents auf den VMs eines Pools mit der neuen `NodeAgentInformation`-Eigenschaft für `PSComputeNode` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1272">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="fb2da-1273">Der `Caching`-Standardwert für `PSDataDisk` lautet jetzt nicht mehr `None`, sondern `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1273">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="fb2da-1274">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fb2da-1274">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="fb2da-1275">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="fb2da-1275">Az.Billing</span></span>
- <span data-ttu-id="fb2da-1276">Kombination von Billing-, Consumption- und UsageAggregates-Cmdlets. Ausführliche Informationen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fb2da-1276">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="fb2da-1277">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="fb2da-1277">Az.CognitivServices</span></span>
- <span data-ttu-id="fb2da-1278">Vervollständigungen für SkuName und Typem für den Vorgang New-AzureRmCognitiveServicesAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1278">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="fb2da-1279">GetSkusWithAccountParamSetName-Parametersatz aus Get-AzCognitiveServicesAccountSkus entfernt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1279">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="fb2da-1280">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="fb2da-1280">Az.ContainerInstance</span></span>
- <span data-ttu-id="fb2da-1281">ManagedIdentity-Unterstützung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1281">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="fb2da-1282">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="fb2da-1282">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="fb2da-1283">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fb2da-1283">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="fb2da-1284">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fb2da-1284">Az.DataLakeStore</span></span>
- <span data-ttu-id="fb2da-1285">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fb2da-1285">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="fb2da-1286">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fb2da-1286">Az.Monitor</span></span>
- <span data-ttu-id="fb2da-1287">Az.Insights in Az.Monitor umbenannt und weitere weniger wichtige grundlegende Änderungen durchgeführt. Informationen hierzu finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fb2da-1287">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="fb2da-1288">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fb2da-1288">Az.KeyVault</span></span>
- <span data-ttu-id="fb2da-1289">Veraltete PurgeDisabled-Eigenschaft aus Ausgabetypen entfernt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1289">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="fb2da-1290">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="fb2da-1290">Az.MachineLearning</span></span>
- <span data-ttu-id="fb2da-1291">Cmdlets des Az.MachineLearningCompute-Moduls eingebunden</span><span class="sxs-lookup"><span data-stu-id="fb2da-1291">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="fb2da-1292">Az.Media</span><span class="sxs-lookup"><span data-stu-id="fb2da-1292">Az.Media</span></span>
- <span data-ttu-id="fb2da-1293">Veralteten -Tags-Alias aus New-AzMediaService entfernt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1293">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="fb2da-1294">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fb2da-1294">Az.Network</span></span>
<span data-ttu-id="fb2da-1295">Unterstützung für das Konfigurieren von RewriteRuleSets im Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1295">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="fb2da-1296">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="fb2da-1296">New cmdlets added:</span></span>
        - <span data-ttu-id="fb2da-1297">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fb2da-1297">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="fb2da-1298">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fb2da-1298">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="fb2da-1299">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fb2da-1299">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="fb2da-1300">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fb2da-1300">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="fb2da-1301">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fb2da-1301">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="fb2da-1302">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="fb2da-1302">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="fb2da-1303">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="fb2da-1303">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="fb2da-1304">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb2da-1304">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="fb2da-1305">Cmdlets mit optionalem Parameter -RewriteRuleSet aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1305">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="fb2da-1306">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fb2da-1306">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="fb2da-1307">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="fb2da-1307">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="fb2da-1308">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="fb2da-1308">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="fb2da-1309">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fb2da-1309">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="fb2da-1310">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="fb2da-1310">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="fb2da-1311">New-AzureRmApplicationGatewayUrlPathMapConfig: KeyVault-Unterstützung mithilfe von Identität zum Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1311">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="fb2da-1312">Cmdlets mit optionalem Parameter aktualisiert: -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="fb2da-1312">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="fb2da-1313">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="fb2da-1313">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="fb2da-1314">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="fb2da-1314">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="fb2da-1315">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="fb2da-1315">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="fb2da-1316">Cmdlet New-AzApplicationGateway mit optionalem Parameter -UserAssignedIdentity aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1316">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="fb2da-1317">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fb2da-1317">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="fb2da-1318">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fb2da-1318">Az.OperationalInsights</span></span>
- <span data-ttu-id="fb2da-1319">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fb2da-1319">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="fb2da-1320">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="fb2da-1320">Az.Profile</span></span>
- <span data-ttu-id="fb2da-1321">Modulnamen in Az.Accounts geändert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1321">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="fb2da-1322">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fb2da-1322">Az.RecoveryServices</span></span>
- <span data-ttu-id="fb2da-1323">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fb2da-1323">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="fb2da-1324">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fb2da-1324">Az.Resources</span></span>
- <span data-ttu-id="fb2da-1325">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fb2da-1325">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="fb2da-1326">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fb2da-1326">Az.ServiceFabric</span></span>
- <span data-ttu-id="fb2da-1327">Unterstützung für das Angeben des Zertifikats anhand des allgemeinen Namens und Fingerabdrucks</span><span class="sxs-lookup"><span data-stu-id="fb2da-1327">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="fb2da-1328">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fb2da-1328">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="fb2da-1329">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="fb2da-1329">Az.SIgnalR</span></span>
- <span data-ttu-id="fb2da-1330">Allgemeine Verfügbarkeit für PowerShell-Cmdlets für SIgnalR</span><span class="sxs-lookup"><span data-stu-id="fb2da-1330">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="fb2da-1331">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fb2da-1331">Az.Sql</span></span>
- <span data-ttu-id="fb2da-1332">Neue Erkennungstypen Data_Exfiltration und Unsafe_Action zu Cmdlets für Bedrohungserkennung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1332">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="fb2da-1333">Dokumentationsbeispiele für Cmdlets für SQL-Überwachung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1333">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="fb2da-1334">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fb2da-1334">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="fb2da-1335">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fb2da-1335">Az.Storage</span></span>
- <span data-ttu-id="fb2da-1336">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fb2da-1336">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="fb2da-1337">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fb2da-1337">Az.Websites</span></span>
- <span data-ttu-id="fb2da-1338">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fb2da-1338">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="fb2da-1339">0.7.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="fb2da-1339">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="fb2da-1340">Allgemein</span><span class="sxs-lookup"><span data-stu-id="fb2da-1340">General</span></span>

* <span data-ttu-id="fb2da-1341">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="fb2da-1341">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="fb2da-1342">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fb2da-1342">Az.Compute</span></span>

* <span data-ttu-id="fb2da-1343">Unterstützung für UltraSSD und Katalogimages in einfachen Parametersätzen für `New-AzVm(ss)`-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1343">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="fb2da-1344">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fb2da-1344">Az.DataLakeStore</span></span>

* <span data-ttu-id="fb2da-1345">Nachgestellten Schrägstrich für die Domäne des ADLS-Kontos korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1345">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="fb2da-1346">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="fb2da-1346">Az.FrontDoor</span></span>

* <span data-ttu-id="fb2da-1347">Einige fehlerhafte Links behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-1347">Fixed some broken links</span></span>
    - <span data-ttu-id="fb2da-1348">In den Artikeln zu New-AzureRmFrontDoor und Set-AzureRmFrontDoor den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorHealthProbeSettingObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1348">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="fb2da-1349">Im Artikel zu New-AzureRmFrontDoorManagedRuleObject den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorRuleGroupOverrideObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1349">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="fb2da-1350">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fb2da-1350">Az.RecoveryServices</span></span>

* <span data-ttu-id="fb2da-1351">Clientseitige Validierungen für Wiederherstellungsvorgänge von Azure-Dateifreigaben hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1351">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="fb2da-1352">storageAccountName und storageAccountResourceGroupName für AFS-Wiederherstellung optional gemacht.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1352">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="fb2da-1353">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fb2da-1353">Az.Resources</span></span>

* <span data-ttu-id="fb2da-1354">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="fb2da-1354">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="fb2da-1355">Get-AzureRmRoleAssignment für die Verwendung des Abonnementbereichs aktualisiert, wenn dieser beim Anfordern von klassischen Administratoren angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1355">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="fb2da-1356">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fb2da-1356">Az.Sql</span></span>

* <span data-ttu-id="fb2da-1357">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="fb2da-1357">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="fb2da-1358">Problem mit der Verwendung von Get-AzureRmSqlDatabaseVulnerabilityAssessment mit .NET Core behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-1358">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="fb2da-1359">Dokumentation mit Hilfemeldungen zu Cmdlets für die SQL-Überwachung geändert.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1359">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="fb2da-1360">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fb2da-1360">Az.Storage</span></span>

* <span data-ttu-id="fb2da-1361">-EnableHierarchicalNamespace zu New-AzureRmStorageAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1361">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="fb2da-1362">Problem behoben, bei dem für das Copy File-Cmdlet am Ziel kein Quellkontext wiederverwendet werden kann, wenn -DestContext nicht eingegeben wird</span><span class="sxs-lookup"><span data-stu-id="fb2da-1362">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="fb2da-1363">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="fb2da-1363">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="fb2da-1364">Unterstützung der Konfiguration von statischen Websites</span><span class="sxs-lookup"><span data-stu-id="fb2da-1364">Support Static Website configuration</span></span>
    - <span data-ttu-id="fb2da-1365">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="fb2da-1365">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="fb2da-1366">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="fb2da-1366">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="fb2da-1367">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fb2da-1367">Az.Websites</span></span>

* <span data-ttu-id="fb2da-1368">Set-AzureRmWebApp und Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fb2da-1368">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="fb2da-1369">Neuen Parameter (-AzureStoragePath) zum Angeben von Azure Storage-Pfaden hinzugefügt, die in Windows- und Linux-Container-Apps bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1369">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="fb2da-1370">Verwenden Sie die Ausgabe des neuen Cmdlets New-AzureRmWebAppAzureStoragePath als Parameter zum Festlegen der Azure Storage-Pfade.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1370">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="fb2da-1371">0.6.1 – November 2018</span><span class="sxs-lookup"><span data-stu-id="fb2da-1371">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="fb2da-1372">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fb2da-1372">Az.ApiManagement</span></span>
* <span data-ttu-id="fb2da-1373">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1373">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="fb2da-1374">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fb2da-1374">Az.Automation</span></span>
* <span data-ttu-id="fb2da-1375">Swagger-basierte Azure Automation-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="fb2da-1375">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="fb2da-1376">Cmdlets zur Updateverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1376">Added Update Management cmdlets</span></span>
* <span data-ttu-id="fb2da-1377">Cmdlets zur Quellcodeverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1377">Added Source Control cmdlets</span></span>
* <span data-ttu-id="fb2da-1378">Cmdlet „Remove-AzureRmAutomationHybridWorkerGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1378">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="fb2da-1379">DSC-Befehl für die Knotenregistrierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1379">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="fb2da-1380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fb2da-1380">Az.Compute</span></span>
* <span data-ttu-id="fb2da-1381">Identitätsproblem für SystemAssigned-Identität korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1381">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="fb2da-1382">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1382">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="fb2da-1383">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="fb2da-1383">Az.ContainerInstance</span></span>
* <span data-ttu-id="fb2da-1384">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1384">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="fb2da-1385">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="fb2da-1385">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="fb2da-1386">Beschreibung der Beispiele für Marketplace-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1386">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="fb2da-1387">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fb2da-1387">Az.Network</span></span>
* <span data-ttu-id="fb2da-1388">Folgende Cmdlets hinzugefügt: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="fb2da-1388">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="fb2da-1389">ICMP wieder unterstützten AzureFirewall-Netzwerkprotokollen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1389">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="fb2da-1390">Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert und Überprüfung für Ziel-ID, Adresse und Port hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1390">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="fb2da-1391">Probleme mit Arbeitsspeicherauslastung in der VirtualNetwork-Zuordnung behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-1391">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="fb2da-1392">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="fb2da-1392">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="fb2da-1393">Problem beim Ändern der Richtlinie für eine geschützte Dateifreigabe behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-1393">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="fb2da-1394">Richtlinienzeitzone in Großschreibung geändert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1394">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="fb2da-1395">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="fb2da-1395">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="fb2da-1396">Korrigiertes Beispiel in „New-AzureRmRecoveryServicesAsrProtectableItem“</span><span class="sxs-lookup"><span data-stu-id="fb2da-1396">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="fb2da-1397">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1397">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="fb2da-1398">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="fb2da-1398">Az.Relay</span></span>
* <span data-ttu-id="fb2da-1399">Optionaler Parameter „-KeyValue“ zu Cmdlet „New-AzureRmRelayKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht</span><span class="sxs-lookup"><span data-stu-id="fb2da-1399">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="fb2da-1400">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fb2da-1400">Az.Resources</span></span>
* <span data-ttu-id="fb2da-1401">Hilfedokumentation für ressourcenidentitätsbezogene Parameter in `New-AzureRmPolicyAssignment` und `Set-AzureRmPolicyAssignment` aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1401">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="fb2da-1402">Beispiel für „New-AzureRmPolicyDefinition“ hinzugefügt, das „-Metadata“ nutzt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1402">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="fb2da-1403">Korrektur, um Beibehaltung von Groß-/Kleinschreibung in Tagschlüsseln in „NetStandard“ zu ermöglichen: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="fb2da-1403">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="fb2da-1404">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fb2da-1404">Az.ServiceFabric</span></span>
* <span data-ttu-id="fb2da-1405">Benachrichtigung über veraltete Elemente für anstehende wichtige Änderungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1405">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="fb2da-1406">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fb2da-1406">Az.Sql</span></span>
* <span data-ttu-id="fb2da-1407">Neue Cmdlets für CRUD-Vorgänge in verwalteten Azure SQL-Datenbank-Instanzen und verwalteten Azure SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1407">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="fb2da-1408">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="fb2da-1408">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="fb2da-1409">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="fb2da-1409">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="fb2da-1410">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="fb2da-1410">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="fb2da-1411">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="fb2da-1411">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="fb2da-1412">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="fb2da-1412">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="fb2da-1413">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="fb2da-1413">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="fb2da-1414">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="fb2da-1414">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="fb2da-1415">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="fb2da-1415">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="fb2da-1416">Erweiterte Verwaltung von Überwachungsrichtlinien auf einem Server oder in einer Datenbank aktiviert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1416">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="fb2da-1417">Neuer Parameter (PredicateExpression) hinzugefügt, um die Filterung von Überwachungsprotokollen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="fb2da-1417">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="fb2da-1418">Cmdlets wurden angepasst, sodass sie SQL-Clients anstelle von Legacyclients verwenden.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1418">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="fb2da-1419">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="fb2da-1419">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="fb2da-1420">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="fb2da-1420">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="fb2da-1421">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="fb2da-1421">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="fb2da-1422">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="fb2da-1422">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="fb2da-1423">Problem bei Verwendung von „Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings“ mit festgelegtem Parameter für den Speicherkontonamen behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-1423">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="fb2da-1424">0.5.0 – November 2018</span><span class="sxs-lookup"><span data-stu-id="fb2da-1424">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="fb2da-1425">Allgemein</span><span class="sxs-lookup"><span data-stu-id="fb2da-1425">General</span></span>
* <span data-ttu-id="fb2da-1426">Ressourcenvervollständigungen für viele Kern-Cmdlets hinzugefügt (diese ermöglichen das Durchlaufen von vorhandenen Ressourcennamen per TAB-TASTE, wenn Cmdlets interaktiv aufgerufen werden)</span><span class="sxs-lookup"><span data-stu-id="fb2da-1426">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="fb2da-1427">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="fb2da-1427">Az.Profile</span></span>
* <span data-ttu-id="fb2da-1428">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="fb2da-1428">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="fb2da-1429">Parameter „TenantId“ im Cmdlet „Connect-AzAccount“ in „Tenant“ umbenannt und Alias für „TenantId“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1429">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="fb2da-1430">Beschreibung von „TenantId“ für „Connect-AzAccount“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1430">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="fb2da-1431">Fehlermeldung für fehlgeschlagene Anmeldung bei Angabe der Mandantendomäne korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1431">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="fb2da-1432">Problem in Bezug auf Kontextnamenskonflikt für Konten ohne Abonnements im Mandanten behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-1432">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="fb2da-1433">Problem mit DataLake-Endpunkten bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-1433">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="fb2da-1434">Problem behoben, das zur Auslösung von „Disconnect-AzAccount“ führte, wenn keine Verbindung bestand</span><span class="sxs-lookup"><span data-stu-id="fb2da-1434">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="fb2da-1435">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fb2da-1435">Az.CognitiveServices</span></span>
* <span data-ttu-id="fb2da-1436">Vorgang „Get-AzCognitiveServicesAccountSkus“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1436">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fb2da-1437">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fb2da-1437">Az.Compute</span></span>
* <span data-ttu-id="fb2da-1438">Cmdlets Add-AzVmssVMDataDisk und Remove-AzVmssVMDataDisk hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1438">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="fb2da-1439">„Get-AzVMImage“ zeigt „AutomaticOSUpgradeProperties“ an</span><span class="sxs-lookup"><span data-stu-id="fb2da-1439">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="fb2da-1440">Problem behoben, aufgrund dessen die Optionswerte „SetAzVMChefExtension -BootstrapOptions“ und „-JsonAttribute“ nicht im JSON-Format festgelegt wurden</span><span class="sxs-lookup"><span data-stu-id="fb2da-1440">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fb2da-1441">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fb2da-1441">Az.DataLakeStore</span></span>
* <span data-ttu-id="fb2da-1442">Aktualisierung des DataLake-Pakets auf 1.1.10</span><span class="sxs-lookup"><span data-stu-id="fb2da-1442">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="fb2da-1443">Standardmäßige Parallelität zu Multithreadvorgängen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1443">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="fb2da-1444">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="fb2da-1444">Az.Insights</span></span>
* <span data-ttu-id="fb2da-1445">Problem Nr. 7267 behoben (Bereich für automatische Skalierung)</span><span class="sxs-lookup"><span data-stu-id="fb2da-1445">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="fb2da-1446">Probleme beim Erstellen einer neuen Regel für die automatische Skalierung, aufgrund derer die aufgelisteten Parameter nicht richtig festgelegt wurden (Es wurde stets der Standardwert festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="fb2da-1446">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="fb2da-1447">Problem Nr. 7513 behoben [Insights] „Set-AzDiagnosticSetting“ erfordert die explizite Angabe von Kategorien während der Erstellung der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1447">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="fb2da-1448">Nun erfordert das Cmdlet nicht die explizite Angabe der Kategorien, die während der Erstellung aktiviert werden sollen. Das bedeutet, es funktioniert wie dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1448">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fb2da-1449">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fb2da-1449">Az.Network</span></span>
* <span data-ttu-id="fb2da-1450">„PeeringType“ wurde geändert und ist nun ein erforderlicher Parameter für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="fb2da-1450">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="fb2da-1451">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="fb2da-1451">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="fb2da-1452">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="fb2da-1452">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="fb2da-1453">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="fb2da-1453">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="fb2da-1454">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="fb2da-1454">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="fb2da-1455">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="fb2da-1455">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="fb2da-1456">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="fb2da-1456">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="fb2da-1457">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="fb2da-1457">Az.PolicyInsights</span></span>
* <span data-ttu-id="fb2da-1458">Cmdlets für Richtlinienwartung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1458">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="fb2da-1459">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fb2da-1459">Az.Resources</span></span>
* <span data-ttu-id="fb2da-1460">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="fb2da-1460">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="fb2da-1461">Zulassen der Auflistung von Ressourcen mithilfe des Parameters „-ResourceId“ für „Get-AzResource“</span><span class="sxs-lookup"><span data-stu-id="fb2da-1461">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="fb2da-1462">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fb2da-1462">Az.ServiceBus</span></span>
* <span data-ttu-id="fb2da-1463">Schreibgeschützte Eigenschaft „MigrationState“ zu „PSServiceBusMigrationConfigurationAttributes“ hinzugefügt, was das Ermitteln des Migrationsstatus ermöglicht</span><span class="sxs-lookup"><span data-stu-id="fb2da-1463">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="fb2da-1464">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fb2da-1464">Az.ServiceFabric</span></span>
* <span data-ttu-id="fb2da-1465">Hinzufügen des Zertifikats zu Linux VMSS korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1465">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="fb2da-1466">„Add-AzServiceFabricClusterCertificate“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="fb2da-1466">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="fb2da-1467">Verwenden des richtigen Fingerabdrucks aus dem neuen Zertifikat (Azure/service-fabric-issues#932)</span><span class="sxs-lookup"><span data-stu-id="fb2da-1467">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="fb2da-1468">Richtige Anzeige von Ausnahmen (Azure/service-fabric-issues#1054)</span><span class="sxs-lookup"><span data-stu-id="fb2da-1468">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="fb2da-1469">„Update-AzServiceFabricDurability“ korrigiert, um die Clusterkonfiguration zu aktualisieren, bevor der VMSS-Vorgang „CreateOrUpdate“ gestartet wird</span><span class="sxs-lookup"><span data-stu-id="fb2da-1469">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="fb2da-1470">0.4.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="fb2da-1470">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="fb2da-1471">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="fb2da-1471">Az.Profile</span></span>
* <span data-ttu-id="fb2da-1472">Problem mit „Get-AzSubscription“ in Cloud Shell behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-1472">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="fb2da-1473">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="fb2da-1473">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fb2da-1474">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fb2da-1474">Az.Compute</span></span>
* <span data-ttu-id="fb2da-1475">Neue Größen zur Whitelist von VM-Größen hinzugefügt, für die bei Verwendung des einfachen Parametersatzes für „New-AzVm“ der beschleunigte Netzwerkbetrieb aktiviert wird</span><span class="sxs-lookup"><span data-stu-id="fb2da-1475">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="fb2da-1476">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1476">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fb2da-1477">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fb2da-1477">Az.DataLakeStore</span></span>
* <span data-ttu-id="fb2da-1478">Unterstützung für VNET-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1478">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="fb2da-1479">Get-AzDataLakeStoreVirtualNetworkRule: Dient zum Abrufen oder Auflisten der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1479">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="fb2da-1480">Add-AzDataLakeStoreVirtualNetworkRule: Fügt dem angegebenen Data Lake Store-Konto eine Regel für das virtuelle Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1480">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="fb2da-1481">Set-AzDataLakeStoreVirtualNetworkRule: Ändert die angegebene Regel für das virtuelle Netzwerk in das angegebene Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1481">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="fb2da-1482">Remove-AzDataLakeStoreVirtualNetworkRule: Dient zum Löschen der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1482">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fb2da-1483">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fb2da-1483">Az.Network</span></span>
* <span data-ttu-id="fb2da-1484">Cmdlet „Test-AzNetworkWatcherConnectivity“ aktualisiert, Protokollwert wird jetzt an Back-End übergeben.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1484">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="fb2da-1485">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1485">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="fb2da-1486">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fb2da-1486">Az.Resources</span></span>
* <span data-ttu-id="fb2da-1487">Problem behoben, aufgrund dessen „Get-AzRoleDefinition“ eine unverständliche Ausnahme auslöst (wenn das Standardprofil kein Abonnement enthält und kein Bereich festgelegt ist), indem im Szenario eine aussagekräftige Ausnahme hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1487">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="fb2da-1488">Außerdem wurde der Standardparametersatz auf „RoleDefinitionNameParameterSet“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1488">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="fb2da-1489">0.3.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="fb2da-1489">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="fb2da-1490">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="fb2da-1490">Azure.Storage</span></span>
* <span data-ttu-id="fb2da-1491">Fehler beim Kopieren von Blobs/Dateien behoben, aufgrund dessen bei einem Metadatenproblem des Ziels keine Metadaten kopiert wurden</span><span class="sxs-lookup"><span data-stu-id="fb2da-1491">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="fb2da-1492">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="fb2da-1492">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="fb2da-1493">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="fb2da-1493">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="fb2da-1494">Der Abruf der Speicherressourcennutzung eines bestimmten Standorts wird jetzt unterstützt, und das Hinzufügen einer Warnmeldung für den Abruf der globalen Speicherressourcennutzung ist überflüssig.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1494">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="fb2da-1495">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="fb2da-1495">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="fb2da-1496">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fb2da-1496">Az.CognitiveServices</span></span>
* <span data-ttu-id="fb2da-1497">„Get-AzCognitiveServicesAccountSkus“ wird ohne vorhandenes Konto unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1497">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fb2da-1498">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fb2da-1498">Az.Compute</span></span>
* <span data-ttu-id="fb2da-1499">Korrektur von „Get-AzVM -ResourceGroupName <rg>“, sodass ggf. mehr als 50 Ergebnisse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="fb2da-1499">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="fb2da-1500">Der Cmdlet-Hilfe zu „New-AzVmss“ wurde ein Beispiel für „SimpleParameterSet“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1500">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="fb2da-1501">Tippfehler in der Azure Disk Encryption-Statusmeldung behoben</span><span class="sxs-lookup"><span data-stu-id="fb2da-1501">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="fb2da-1502">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="fb2da-1502">Az.DataFactoryV2</span></span>
* <span data-ttu-id="fb2da-1503">Die Version des ADF .Net-SDK wurde auf 2.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1503">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fb2da-1504">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fb2da-1504">Az.Network</span></span>
* <span data-ttu-id="fb2da-1505">NetworkProfile-Funktionalität wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1505">Added NetworkProfile functionality.</span></span> <span data-ttu-id="fb2da-1506">Neue Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1506">new cmdlets added</span></span>
    - <span data-ttu-id="fb2da-1507">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fb2da-1507">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="fb2da-1508">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fb2da-1508">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="fb2da-1509">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fb2da-1509">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="fb2da-1510">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fb2da-1510">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="fb2da-1511">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="fb2da-1511">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="fb2da-1512">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="fb2da-1512">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="fb2da-1513">Dienstzuordnungslink in Subnetzmodell hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1513">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="fb2da-1514">Cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1514">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="fb2da-1515">Cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1515">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="fb2da-1516">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="fb2da-1516">Az.RedisCache</span></span>
* <span data-ttu-id="fb2da-1517">Künftig sind beliebige Zeichenfolgen als Größenparameter zulässig.</span><span class="sxs-lookup"><span data-stu-id="fb2da-1517">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="fb2da-1518">P5 in Popup „PSArgumentCompleter“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1518">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="fb2da-1519">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fb2da-1519">Az.Resources</span></span>
* <span data-ttu-id="fb2da-1520">Fehlender Parameter „-Mode“ zu „Set-AzPolicyDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="fb2da-1520">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="fb2da-1521">Cmdlet-Fehler bei „Get-AzProviderOperation“ für Vorgänge mit Ursprung behoben, der den Benutzer enthält</span><span class="sxs-lookup"><span data-stu-id="fb2da-1521">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="fb2da-1522">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fb2da-1522">Az.Sql</span></span>
* <span data-ttu-id="fb2da-1523">Problem behoben, aufgrund dessen einige Sicherungs-Cmdlets das aktuelle Azure-Abonnements nicht erkannt haben</span><span class="sxs-lookup"><span data-stu-id="fb2da-1523">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fb2da-1524">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fb2da-1524">Az.Websites</span></span>
* <span data-ttu-id="fb2da-1525">Neues Cmdlet „Get-AzWebAppContainerContinuousDeploymentUrl“ zum Abrufen der Webhook-URL von Continuous Deployment für Container</span><span class="sxs-lookup"><span data-stu-id="fb2da-1525">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="fb2da-1526">Neue Cmdlets „New-AzWebAppContainerPSSession“ und „Enter-WebAppContainerPSSession“ zum Initiieren einer PowerShell-Remotesitzung in einer Windows-Container-App</span><span class="sxs-lookup"><span data-stu-id="fb2da-1526">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="fb2da-1527">0.2.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="fb2da-1527">0.2.0 - September 2018</span></span>
 <span data-ttu-id="fb2da-1528">Erste Version</span><span class="sxs-lookup"><span data-stu-id="fb2da-1528">Initial Release</span></span>
