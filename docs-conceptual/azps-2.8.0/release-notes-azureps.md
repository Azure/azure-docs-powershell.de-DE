---
title: Versionshinweise zu Azure PowerShell
description: Hier erfahren Sie mehr über die aktuellen Updates für die Azure PowerShell-Module.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 656e61e7f208367fc7fae28f73d1b6f289831d77
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427733"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="8b12a-103">Versionshinweise zu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="8b12a-103">Azure PowerShell release notes</span></span>
## <a name="280---october-2019"></a><span data-ttu-id="8b12a-104">2.8.0: Oktober 2019</span><span class="sxs-lookup"><span data-stu-id="8b12a-104">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="8b12a-105">Allgemein</span><span class="sxs-lookup"><span data-stu-id="8b12a-105">General</span></span>
* <span data-ttu-id="8b12a-106">Az.HealthcareApis-Release 1.0.0</span><span class="sxs-lookup"><span data-stu-id="8b12a-106">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8b12a-107">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8b12a-107">Az.Accounts</span></span>
* <span data-ttu-id="8b12a-108">Telemetriedaten und URL-Umschreibung für generierte Module aktualisiert, Windows-Komponententests korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-108">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8b12a-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8b12a-109">Az.ApiManagement</span></span>
* <span data-ttu-id="8b12a-110">**Set-AzApiManagementApi**: Unterstützung für die Aktualisierung der API in „ApiVersionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-110">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="8b12a-111">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="8b12a-111">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8b12a-112">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8b12a-112">Az.Automation</span></span>
* <span data-ttu-id="8b12a-113">Cmdlet „New-AzureAutomationSoftwareUpdateConfiguration“ für den Parameter für die Linux-Neustarteinstellung korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-113">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8b12a-114">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8b12a-114">Az.Batch</span></span>
* <span data-ttu-id="8b12a-115">**Get-AzBatchNodeAgentSku** ist veraltet und wird in Version 2.0.0 durch **Get-AzBatchSupportImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="8b12a-115">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8b12a-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8b12a-116">Az.Compute</span></span>
* <span data-ttu-id="8b12a-117">Parameter „Priority“, „EvictionPolicy“ und „MaxPrice“ zu den Cmdlets „“New-AzVM“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-117">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="8b12a-118">Warnmeldung und Hilfedokument für die Cmdlets „Add-AzVMAdditionalUnattendContent“ und „Add-AzVMSshPublicKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-118">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="8b12a-119">Ausnahme „-skipVmBackup“ Linux-VMs mit verwalteten Datenträgern für „Set-AzVMDiskEncryptionExtension“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-119">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="8b12a-120">Fehler beim Aktualisieren von Verschlüsselungseinstellungen in „Set-AzVMDiskEncryptionExtension“ korrigiert (zweistufiges Szenario)</span><span class="sxs-lookup"><span data-stu-id="8b12a-120">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8b12a-121">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8b12a-121">Az.DataFactory</span></span>
* <span data-ttu-id="8b12a-122">CRUD-Befehle für ADF V2-Datenfluss hinzugefügt: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow und Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="8b12a-122">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="8b12a-123">Aktionsbefehle für Debugsitzung für ADF V2-Datenfluss hinzugefügt: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand und Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="8b12a-123">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="8b12a-124">Version des ADF .NET SDK auf 4.2.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-124">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8b12a-125">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8b12a-125">Az.DataLakeStore</span></span>
* <span data-ttu-id="8b12a-126">Kontoüberprüfung korrigiert, sodass Konten mit „-“ ohne Domäne übermittelt werden können</span><span class="sxs-lookup"><span data-stu-id="8b12a-126">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="8b12a-127">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="8b12a-127">Az.HealthcareApis</span></span>
* <span data-ttu-id="8b12a-128">PowerShell-Version auf 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-128">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="8b12a-129">SDK-Version auf 1.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-129">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="8b12a-130">Aktualisierung in Tests, um auf neue SDK-Version zu verweisen</span><span class="sxs-lookup"><span data-stu-id="8b12a-130">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="8b12a-131">Ausgabestruktur von geschachtelt in vereinfacht geändert</span><span class="sxs-lookup"><span data-stu-id="8b12a-131">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8b12a-132">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8b12a-132">Az.IotHub</span></span>
* <span data-ttu-id="8b12a-133">Neue Routingquelle hinzugefügt: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="8b12a-133">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="8b12a-134">Kleinere Fehlerbehebung: „Get-AzIothub“ gibt „subscriptionId“ nicht zurück.</span><span class="sxs-lookup"><span data-stu-id="8b12a-134">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8b12a-135">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8b12a-135">Az.Monitor</span></span>
* <span data-ttu-id="8b12a-136">Neue Aktionsgruppenempfänger für „New-AzActionGroupReceiver“ hinzugefügt:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="8b12a-136">New action group receivers added for New-AzActionGroupReceiver:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="8b12a-137">Verwendung des allgemeinen Warnungsschemas für Empfänger aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8b12a-137">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="8b12a-138">Dies gilt nicht für SMS, Azure App-Pushbenachrichtigungen, ITSM und Sprachempfänger.</span><span class="sxs-lookup"><span data-stu-id="8b12a-138">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="8b12a-139">Webhooks unterstützen nun die Azure Active Directory-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="8b12a-139">Webhooks now supports Azure active directory authentication.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8b12a-140">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8b12a-140">Az.Network</span></span>
* <span data-ttu-id="8b12a-141">Neues Cmdlet „Get-AzAvailableServiceAlias“ hinzugefügt, das zum Abrufen der Aliase aufgerufen werden kann, die für Dienstendpunktrichtlinien verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="8b12a-141">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="8b12a-142">Unterstützung für das Hinzufügen von Verbindungen von Datenverkehrsselektoren zu Virtual Network-Gatewayverbindungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-142">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="8b12a-143">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="8b12a-143">New cmdlets added:</span></span>
        - <span data-ttu-id="8b12a-144">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="8b12a-144">New-AzIpsecTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="8b12a-145">Cmdlets mit optionalem Parameter „-TrafficSelectorPolicies“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-145">Cmdlets updated with optional parameter -TrafficSelectorPolicies</span></span>
        - <span data-ttu-id="8b12a-146">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8b12a-146">New-AzVirtualNetworkGatewayConnection</span></span>
        - <span data-ttu-id="8b12a-147">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8b12a-147">Set-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="8b12a-148">Unterstützung für ESP- und AH-Protokolle in Konfigurationen von Netzwerksicherheitsregeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-148">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="8b12a-149">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="8b12a-149">Updated cmdlets:</span></span>
        - <span data-ttu-id="8b12a-150">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8b12a-150">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8b12a-151">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8b12a-151">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8b12a-152">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8b12a-152">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="8b12a-153">Verbesserte Behandlung von Ausnahmen in Cortex-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8b12a-153">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="8b12a-154">Neue Generationen und SKUs für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="8b12a-154">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="8b12a-155">Einführung neuer Generationen für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="8b12a-155">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="8b12a-156">Einführung neuer SKUs mit höherem Durchsatz für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="8b12a-156">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8b12a-157">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8b12a-157">Az.RedisCache</span></span>
* <span data-ttu-id="8b12a-158">Referenzdokumentation zu „Set-AzRedisCache“ aktualisiert, um fehlende Werte für den Parameter „-Size“ aufzunehmen</span><span class="sxs-lookup"><span data-stu-id="8b12a-158">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="8b12a-159">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8b12a-159">Az.Sql</span></span>
* <span data-ttu-id="8b12a-160">Unterstützung für das Festlegen des Active Directory-Administrators für verwaltete Instanz hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-160">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8b12a-161">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8b12a-161">Az.Storage</span></span>
* <span data-ttu-id="8b12a-162">Storage-Clientbibliothek auf 11.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-162">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="8b12a-163">Auflisten von Containern mit der API der Verwaltungsebene, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="8b12a-163">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="8b12a-164">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="8b12a-164">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="8b12a-165">Auflisten von Storage-Konten aus Abonnements, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="8b12a-165">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="8b12a-166">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8b12a-166">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="8b12a-167">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="8b12a-167">Az.StorageSync</span></span>
* <span data-ttu-id="8b12a-168">Problem 9810 in „Reset-AzStorageSyncServerCertificate“ behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-168">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8b12a-169">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8b12a-169">Az.Websites</span></span>
* <span data-ttu-id="8b12a-170">Fehler beim Aktualisieren von ASP einer App mit „Set-AzWebApp“</span><span class="sxs-lookup"><span data-stu-id="8b12a-170">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="8b12a-171">2.7.0: September 2019</span><span class="sxs-lookup"><span data-stu-id="8b12a-171">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="8b12a-172">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8b12a-172">Az.ApiManagement</span></span>
* <span data-ttu-id="8b12a-173">Beschreibung des Parameters „-Format“ in der Referenzdokumentation für „Set-AzApiManagementPolicy“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-173">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="8b12a-174">Verweise des veralteten Cmdlets „Update-AzApiManagementDeployment“ aus Referenzdokumentation entfernt.</span><span class="sxs-lookup"><span data-stu-id="8b12a-174">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="8b12a-175">Verwenden Sie stattdessen „Set-AzApiManagement“.</span><span class="sxs-lookup"><span data-stu-id="8b12a-175">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8b12a-176">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8b12a-176">Az.Automation</span></span>
* <span data-ttu-id="8b12a-177">Tippfehler im Beispiel in der Referenzdokumentation für „Register-AzAutomationDscNode“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-177">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="8b12a-178">Erläuterung zur Betriebssystemeinschränkung zu „Register-AzAutomationDSCNode“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-178">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="8b12a-179">Nullverweisausnahme des Cmdlets „Start-AzAutomationRunbook“ für die Option „-Wait“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="8b12a-179">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8b12a-180">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8b12a-180">Az.Compute</span></span>
* <span data-ttu-id="8b12a-181">Parameter „UploadSizeInBytes“ zu „New-AzDiskConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-181">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="8b12a-182">Inkrementeller Parameter zu „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-182">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="8b12a-183">Feature für VM mit niedriger Priorität hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="8b12a-183">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="8b12a-184">Parameter „MaxPrice“, „EvictionPolicy“ und „Priority“ zu New-AzVMConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-184">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="8b12a-185">Parameter „MaxPrice“ zu den Cmdlets „New-AzVmssConfig“, „Update-AzVM“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-185">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="8b12a-186">Fehlerbehebung für VM-Verweis für das Cmdlet „Get-AzAvailabilitySet“, wenn alle Verfügbarkeitsgruppen im Abonnement aufgelistet werden</span><span class="sxs-lookup"><span data-stu-id="8b12a-186">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="8b12a-187">Nullausnahme für „Get-AzRemoteDesktopFile“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-187">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="8b12a-188">VHD-Suchmethode für Position relativ zum Ende korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-188">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="8b12a-189">Problem mit UltraSSD für „New-AzVM“ und „Update-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-189">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8b12a-190">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8b12a-190">Az.DataFactory</span></span>
* <span data-ttu-id="8b12a-191">Drei neue Befehle für ADF V2 hinzugefügt: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription und Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="8b12a-191">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="8b12a-192">Version des ADF .NET SDK auf 4.1.3 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-192">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8b12a-193">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8b12a-193">Az.HDInsight</span></span>
* <span data-ttu-id="8b12a-194">Hinweis auf Breaking Changes hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-194">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8b12a-195">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8b12a-195">Az.IotHub</span></span>
* <span data-ttu-id="8b12a-196">Unterstützung zum Aufrufen eines Failovers für einen IoT-Hub zur geografisch gekoppelten Notfallwiederherstellungsregion hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-196">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="8b12a-197">Unterstützung zum Verwalten der Nachrichtenanreicherung für einen IoT-Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-197">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="8b12a-198">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="8b12a-198">New cmdlets are:</span></span>
    - <span data-ttu-id="8b12a-199">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="8b12a-199">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="8b12a-200">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="8b12a-200">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="8b12a-201">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="8b12a-201">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="8b12a-202">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="8b12a-202">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8b12a-203">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8b12a-203">Az.Monitor</span></span>
* <span data-ttu-id="8b12a-204">Verweis auf das aktuelle Monitor SDK, d. h. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="8b12a-204">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="8b12a-205">Geringfügige Änderungen an den Metrik-Cmdlets vorgenommen, d. h. die Einheitenenumeration unterstützt verschiedene neue Werte.</span><span class="sxs-lookup"><span data-stu-id="8b12a-205">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="8b12a-206">Dabei handelt es sich um schreibgeschützte Cmdlets, sodass keine Änderungen an der Eingabe der Cmdlets erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="8b12a-206">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="8b12a-207">Die API-Version der **ActionGroups**-Anforderungen lautet jetzt **2019-06-01** (zuvor **2018-03-01**).</span><span class="sxs-lookup"><span data-stu-id="8b12a-207">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="8b12a-208">Die Szenariotests wurden aktualisiert, um diese Änderung zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="8b12a-208">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="8b12a-209">Die Konstruktoren für die Klassen **EmailReceiver** und **WebhookReceiver** haben ein neues obligatorisches Argument hinzugefügt, d. h. einen booleschen Wert namens **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="8b12a-209">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="8b12a-210">Derzeit ist der Wert auf **false** festgelegt, damit sich dieser Breaking Change nicht auf die Cmdlets auswirkt.</span><span class="sxs-lookup"><span data-stu-id="8b12a-210">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="8b12a-211">**HINWEIS:** Dies ist eine vorübergehende Änderung, die vom Team für Warnungen validiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="8b12a-211">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="8b12a-212">Die Reihenfolge der Argumente für den Konstruktor der Klasse **Source** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="8b12a-212">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="8b12a-213">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="8b12a-213">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="8b12a-214">Die Reihenfolge der Argumente für den Konstruktor der Klasse **AlertingAction** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="8b12a-214">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="8b12a-215">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="8b12a-215">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="8b12a-216">Unterstützung von Kriterien für dynamische Schwellwerte für Metrikwarnung v2</span><span class="sxs-lookup"><span data-stu-id="8b12a-216">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="8b12a-217">New-AzMetricAlertRuleV2Criteria: Erstellt nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="8b12a-217">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="8b12a-218">Add-AzMetricAlertRuleV2: Akzeptiert nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="8b12a-218">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="8b12a-219">Verbesserungen an den Cmdlets für geplante Abfrageregeln (Scheduled Query Rule, SQR)</span><span class="sxs-lookup"><span data-stu-id="8b12a-219">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="8b12a-220">Cmdlets akzeptieren den Parameter „Location“ in zwei Formaten: entweder den Standort (z. B. „eastus“) oder den Anzeigenamen des Standorts (z. B. „USA, Osten“)</span><span class="sxs-lookup"><span data-stu-id="8b12a-220">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="8b12a-221">Parameter „Enabled“ in Hilfedateien ordnungsgemäß dargestellt</span><span class="sxs-lookup"><span data-stu-id="8b12a-221">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="8b12a-222">Beispiele für optionalen Parameter „ActionGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-222">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="8b12a-223">Hilfedateien insgesamt verbessert</span><span class="sxs-lookup"><span data-stu-id="8b12a-223">Overall improved help files</span></span>
* <span data-ttu-id="8b12a-224">Fehler beim Bestimmen des Bereichstyps für „Set-AzActionRule“ behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-224">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8b12a-225">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8b12a-225">Az.Network</span></span>
* <span data-ttu-id="8b12a-226">Fehlerhaftes Beispiel in der Referenzdokumentation zu „New-AzApplicationGateway“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-226">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="8b12a-227">Hinweis in der Referenzdokumentation zu „Get-AzNetworkWatcherPacketCapture“ zum Abrufen aller Eigenschaften für eine Paketerfassung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-227">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="8b12a-228">Beispiel in der Referenzdokumentation zu „Test-AzNetworkWatcherIPFlow“ korrigiert, um die Netzwerkadapter ordnungsgemäß aufzulisten</span><span class="sxs-lookup"><span data-stu-id="8b12a-228">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="8b12a-229">Cloudausnahmeanalyse verbessert, um ggf. zusätzliche Details anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="8b12a-229">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="8b12a-230">Cloudausnahmeanalyse verbessert, um zusätzlichen Typ der SDK-Ausnahme zu verarbeiten</span><span class="sxs-lookup"><span data-stu-id="8b12a-230">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="8b12a-231">Falsche Zuordnung der Sicherheitsregelmodelle korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-231">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="8b12a-232">Eigenschaften zur Netzwerkschnittstelle für das Feature für die private IP-Adresse hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-232">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="8b12a-233">Eigenschaft „PrivateEndpoint“ als Typ „PSResourceId“ zu „PSNetworkInterface“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-233">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="8b12a-234">Eigenschaft „PrivateLinkConnectionProperties“ als Typ „PSIpConfigurationConnectivityInformation“ zu „PSNetworkInterfaceIPConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-234">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="8b12a-235">Neue Modellklasse „PSIpConfigurationConnectivityInformation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-235">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="8b12a-236">Neues ApplicationRuleProtocolType-Element „mssql“ für Azure Firewall-Ressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-236">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="8b12a-237">Unterstützung von Mehrfachverbindungen in Virtual WAN</span><span class="sxs-lookup"><span data-stu-id="8b12a-237">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="8b12a-238">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8b12a-238">New cmdlets</span></span>
        - <span data-ttu-id="8b12a-239">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="8b12a-239">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="8b12a-240">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="8b12a-240">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="8b12a-241">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8b12a-241">Updated cmdlet:</span></span>
        - <span data-ttu-id="8b12a-242">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="8b12a-242">New-VpnSite</span></span>
        - <span data-ttu-id="8b12a-243">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="8b12a-243">Update-VpnSite</span></span>
        - <span data-ttu-id="8b12a-244">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="8b12a-244">New-VpnConnection</span></span>
        - <span data-ttu-id="8b12a-245">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="8b12a-245">Update-VpnConnection</span></span>
* <span data-ttu-id="8b12a-246">Dokumente für einige PowerShell-Beispiele korrigiert, sodass Az-Cmdlets anstelle von AzureRM-Cmdlets verwendet werden</span><span class="sxs-lookup"><span data-stu-id="8b12a-246">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8b12a-247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8b12a-247">Az.RecoveryServices</span></span>
* <span data-ttu-id="8b12a-248">AzureVMpolicy-Objekt mit ProtectedItemsCount-Attribut aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-248">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="8b12a-249">Tests für VM-Richtlinie und Wiederherstellung des ursprünglichen Speicherkontos hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-249">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="8b12a-250">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8b12a-250">Az.Resources</span></span>
* <span data-ttu-id="8b12a-251">Fehler behoben, aufgrund dessen „New-AzRoleAssignment“ nicht ohne den Parameter „Scope“ aufgerufen werden konnte</span><span class="sxs-lookup"><span data-stu-id="8b12a-251">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8b12a-252">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8b12a-252">Az.ServiceFabric</span></span>
* <span data-ttu-id="8b12a-253">Tippfehler im Beispiel für die Referenzdokumentation „Update-AzServiceFabricReliability“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-253">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="8b12a-254">Neue Cmdlets zum Verwalten von Anwendung und Diensten hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="8b12a-254">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="8b12a-255">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="8b12a-255">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="8b12a-256">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="8b12a-256">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="8b12a-257">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="8b12a-257">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="8b12a-258">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="8b12a-258">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="8b12a-259">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="8b12a-259">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="8b12a-260">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="8b12a-260">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="8b12a-261">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="8b12a-261">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="8b12a-262">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="8b12a-262">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="8b12a-263">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="8b12a-263">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="8b12a-264">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="8b12a-264">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="8b12a-265">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="8b12a-265">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="8b12a-266">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="8b12a-266">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="8b12a-267">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="8b12a-267">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="8b12a-268">Service Fabric SDK auf Version 1.2.0 aktualisiert, die API-Version 2019-03-01 des Service Fabric-Ressourcenanbieters verwendet</span><span class="sxs-lookup"><span data-stu-id="8b12a-268">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8b12a-269">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8b12a-269">Az.SignalR</span></span>
* <span data-ttu-id="8b12a-270">Cmdlets „Update“, „Restart“, „CheckNameAvailability“ und „GetUsage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-270">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="8b12a-271">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8b12a-271">Az.Sql</span></span>
* <span data-ttu-id="8b12a-272">Beispiel in der Referenzdokumentation für „Get-AzSqlElasticPool“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-272">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="8b12a-273">V-Kern-Beispiel zum Erstellen eines Pools für elastische Datenbanken hinzugefügt (New-AzSqlElasticPool)</span><span class="sxs-lookup"><span data-stu-id="8b12a-273">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="8b12a-274">Überprüfung von „EmailAddresses“ sowie Validierung, dass „EmailAdmins“ nicht auf „false“ festgelegt ist, in „Set-AzSqlServerAdvancedThreatProtectionPolicy“ und „Set-AzSqlDatabaseAdvancedThreatProtectionPolicy“ entfernt, wenn „EmailAddresses“ leer ist</span><span class="sxs-lookup"><span data-stu-id="8b12a-274">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="8b12a-275">Entfernen der Einstellungen für Server-/Datenbanküberwachung aktiviert, wenn mehrere Diagnoseeinstellungen vorhanden sind, die eine Überwachungskategorie ermöglichen</span><span class="sxs-lookup"><span data-stu-id="8b12a-275">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="8b12a-276">Überprüfung von E-Mail-Adressen in mehreren Cmdlets für die SQL-Sicherheitsrisikobewertung korrigiert (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting und Update-AzSqlInstanceVulnerabilityAssessmentSetting)</span><span class="sxs-lookup"><span data-stu-id="8b12a-276">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8b12a-277">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8b12a-277">Az.Storage</span></span>
* <span data-ttu-id="8b12a-278">Beispiel in der Referenzdokumentation für „Get-AzStorageAccountKey“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-278">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="8b12a-279">Beim Upload/Download von Azure-Dateien wird das Beibehalten der SMB-Eigenschaften der Quelldateien (Dateiattribute, Zeitpunkt der Dateierstellung, letzter Schreibzugriff für die Datei) in der Zieldatei unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8b12a-279">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="8b12a-280">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8b12a-280">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="8b12a-281">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8b12a-281">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="8b12a-282">Fehler beim Hochladen von Blockblobs mit Eigenschaften/Metadaten für das für einen Container aktivierte ImmutabilityPolicy-Element behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-282">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="8b12a-283">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8b12a-283">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="8b12a-284">Unterstützung für die Verwaltung von Azure-Dateifreigaben mit der API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="8b12a-284">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="8b12a-285">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8b12a-285">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="8b12a-286">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8b12a-286">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="8b12a-287">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8b12a-287">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="8b12a-288">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8b12a-288">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8b12a-289">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8b12a-289">Az.Websites</span></span>
* <span data-ttu-id="8b12a-290">Problem behoben, aufgrund dessen Web-App-Tags beim Migrieren der App zum neuen ASP gelöscht wurden</span><span class="sxs-lookup"><span data-stu-id="8b12a-290">Fixing issue where webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="8b12a-291">„Publish-AzureWebapp“ für die Verwendung unter Linux und Windows korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-291">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="8b12a-292">Beispiel in Referenzdokumentation „Get-AzWebAppPublishingProfile“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-292">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="8b12a-293">2.6.0: August 2019</span><span class="sxs-lookup"><span data-stu-id="8b12a-293">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="8b12a-294">Allgemein</span><span class="sxs-lookup"><span data-stu-id="8b12a-294">General</span></span>
* <span data-ttu-id="8b12a-295">Verschiedene Tippfehler in zahlreichen Modulen korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-295">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8b12a-296">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8b12a-296">Az.Accounts</span></span>
* <span data-ttu-id="8b12a-297">Unterstützung der benutzerseitig zugewiesenen MSI in Azure Functions-Authentifizierung (#9479)</span><span class="sxs-lookup"><span data-stu-id="8b12a-297">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="8b12a-298">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8b12a-298">Az.Aks</span></span>
* <span data-ttu-id="8b12a-299">Problem mit der Ausgabe für „Get-AzAks“ behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-299">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="8b12a-300">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="8b12a-300">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8b12a-301">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8b12a-301">Az.ApiManagement</span></span>
* <span data-ttu-id="8b12a-302">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="8b12a-302">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="8b12a-303">.NET-NuGet-Version aktualisiert, die keine Einschränkungen für „productId“, „apiId“, „groupId“ und „userId“ erzwingt</span><span class="sxs-lookup"><span data-stu-id="8b12a-303">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="8b12a-304">**Get-AzApiManagementProduct:** Unterstützung für das Abfragen von Produkten mithilfe der API hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-304">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="8b12a-305">**New-AzApiManagementApiRevision:** Problem behoben, aufgrund dessen „ApiRevisionDescription“ beim Erstellen einer neuen API-Revision nicht festgelegt wurde https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="8b12a-305">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="8b12a-306">Tippfehler im Modell „PsApiManagementOAuth2AuthrozationServer“ korrigiert: PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="8b12a-306">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8b12a-307">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8b12a-307">Az.Batch</span></span>
* <span data-ttu-id="8b12a-308">Tippfehler in Hilfemeldung und Dokumentation korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="8b12a-308">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8b12a-309">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8b12a-309">Az.Cdn</span></span>
* <span data-ttu-id="8b12a-310">Tippfehler im Hilfsprogramm für die CDN-Modulkonvertierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-310">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8b12a-311">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8b12a-311">Az.Compute</span></span>
* <span data-ttu-id="8b12a-312">VmssId zum Cmdlet „New-AzVMConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-312">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="8b12a-313">Parameter „TerminateScheduledEvents“ und „TerminateScheduledEventNotBeforeTimeoutInMinutes“ zu „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-313">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="8b12a-314">HyperVGeneration-Eigenschaft zu VM-Imageobjekt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-314">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="8b12a-315">Host- und HostGroup-Features hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-315">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="8b12a-316">Neue Cmdlets:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="8b12a-316">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="8b12a-317">Parameter „HostId“ zu „New-AzVMConfig“ und „New-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-317">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="8b12a-318">Beispiel in der Dokumentation zu „Invoke-AzVMRunCommand“ zur Verwendung des richtigen Parameternamens aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-318">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="8b12a-319">Beschreibung für „-VolumeType“ in der Referenzdokumentation zu „Set-AzVMDiskEncryptionExtension“ und „Set-AzVmssDiskEncryptionExtension“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-319">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8b12a-320">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8b12a-320">Az.DataFactory</span></span>
* <span data-ttu-id="8b12a-321">Tippfehler in der Dokumentation zu „New-AzDataFactoryEncryptValue“ korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="8b12a-321">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="8b12a-322">Version des ADF .NET SDK auf 4.1.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-322">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="8b12a-323">Parameter „DataProxyIntegrationRuntimeName“, „DataProxyStagingLinkedServiceName“ und „DataProxyStagingPath“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um die Einrichtung der selbstgehosteten Integration Runtime als Proxy für die SSIS Integration Runtime zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="8b12a-323">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="8b12a-324">„PSTriggerRun“ zum Anzeigen der ausgelösten Pipelines, Meldungen und Eigenschaften und „PSActivityRun“ zum Anzeigen des Aktivitätstyps aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-324">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8b12a-325">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8b12a-325">Az.DataLakeStore</span></span>
* <span data-ttu-id="8b12a-326">Hängen von „Get-DataLakeStoreDeletedItem“ aufgrund von Fehlern oder Remoteausnahmen behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-326">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8b12a-327">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8b12a-327">Az.EventHub</span></span>
* <span data-ttu-id="8b12a-328">Behebung des Problems #9658: Tippfehler im Parameter „VirtualNteworkRule“ in „Set-AzEventHubNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="8b12a-328">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="8b12a-329">Behebung des Problems #9558: „Set-AzEventHubNamespace“ verwendet PATCH anstelle von PUT.</span><span class="sxs-lookup"><span data-stu-id="8b12a-329">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="8b12a-330">Parameter „EnableKafka“ zum Cmdlet „Set-AzEventHubNamespace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-330">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="8b12a-331">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="8b12a-331">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="8b12a-332">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="8b12a-332">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="8b12a-333">Tippfehler („Azure“ in Kleinbuchstaben) in der Dokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-333">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8b12a-334">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8b12a-334">Az.Monitor</span></span>
* <span data-ttu-id="8b12a-335">Falscher Parametername in der Hilfedokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-335">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8b12a-336">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8b12a-336">Az.Network</span></span>
* <span data-ttu-id="8b12a-337">„New-AzPrivateLinkServiceIpConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-337">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="8b12a-338">Parameter „PublicIpAddress“ ausgemustert, da er auf Serverseite nie verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="8b12a-338">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="8b12a-339">Optionaler Parameter „Primary“ hinzugefügt, der angibt, ob die aktuelle IP-Konfiguration die primäre ist oder nicht</span><span class="sxs-lookup"><span data-stu-id="8b12a-339">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="8b12a-340">Verbesserte Verarbeitung der Anforderungsfehlerausnahme aus dem SDK: Behebt das Problem, dass vorherige SDK-Ausnahmen nicht richtig behandelt wurden, was dazu führt, dass Schlüsselfehlerdetails nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8b12a-340">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="8b12a-341">Validierungslogik für Ipv6-IP-Präfix angepasst, damit auf die richtige IPv6-Präfixlänge geprüft wird</span><span class="sxs-lookup"><span data-stu-id="8b12a-341">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="8b12a-342">„Get-AzVirtualNetworkSubnetConfig“ aktualisiert: Parametersatz zum Abrufen nach Subnetzressourcen-ID hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-342">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="8b12a-343">Aktualisierte Beschreibung des Location-Parameters für „AzNetworkServiceTag“</span><span class="sxs-lookup"><span data-stu-id="8b12a-343">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8b12a-344">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8b12a-344">Az.OperationalInsights</span></span>
* <span data-ttu-id="8b12a-345">Aktualisierte Dokumentation für „New-AzOperationalInsightsLinuxSyslogDataSource“</span><span class="sxs-lookup"><span data-stu-id="8b12a-345">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="8b12a-346">Beispiel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-346">Added example</span></span>
    - <span data-ttu-id="8b12a-347">Beschreibung für den Parameter „-Name“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-347">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="8b12a-348">Beispiel für „New-AzOperationalInsightsWindowsEventDataSource“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-348">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="8b12a-349">Beschreibung des Parameters „-Name“ für „New-AzOperationalInsightsWindowsEventDataSource“ geändert</span><span class="sxs-lookup"><span data-stu-id="8b12a-349">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8b12a-350">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8b12a-350">Az.RecoveryServices</span></span>
* <span data-ttu-id="8b12a-351">„Get-AzRecoveryServicesBackupJobDetail.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-351">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="8b12a-352">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8b12a-352">Az.Resources</span></span>
* <span data-ttu-id="8b12a-353">Unterstützung für die neue API-Version 2019-05-10 für Microsoft.Resource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-353">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="8b12a-354">Unterstützung für „copy.count = 0“ für Variablen, Ressourcen und Eigenschaften hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-354">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="8b12a-355">Ressourcen mit „condition = false“ oder „copy.count = 0“ werden im vollständigen Modus gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8b12a-355">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="8b12a-356">Beispiel zum Hinzufügen einer Richtlinie auf Abonnementebene zur Hilfedokumentation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-356">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8b12a-357">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8b12a-357">Az.ServiceBus</span></span>
* <span data-ttu-id="8b12a-358">Behebung des Problems #9658: Tippfehler für Parameter „VirtualNetworkRule“ in „Set-AzServiceBusNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="8b12a-358">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="8b12a-359">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="8b12a-359">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="8b12a-360">Neuer Befehl „Test-AzServiceBusNameAvailability“ zum Überprüfen der Verfügbarkeit des Namens für Warteschlange und Thema hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-360">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8b12a-361">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8b12a-361">Az.ServiceFabric</span></span>
* <span data-ttu-id="8b12a-362">Fehler bei Cmdlets zum Hinzufügen des Knotentyps korrigiert:</span><span class="sxs-lookup"><span data-stu-id="8b12a-362">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="8b12a-363">Fehler „NullReferenceException“, wenn die Ressourcengruppe andere VMSS enthielt, die nicht mit dem Service Fabric-Cluster in Zusammenhang stehen</span><span class="sxs-lookup"><span data-stu-id="8b12a-363">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="8b12a-364">Problembehebung: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="8b12a-364">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="8b12a-365">Fehler behoben, aufgrund dessen bei einem Cmdlet ein Fehler auftrat, wenn sich „virtualNetwork“ in einer anderen Ressourcengruppe befand als der Cluster</span><span class="sxs-lookup"><span data-stu-id="8b12a-365">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="8b12a-366">Problembehebung: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="8b12a-366">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="8b12a-367">Cmdlet „Add-AzServiceFabricApplicationCertificate“ ausgemustert</span><span class="sxs-lookup"><span data-stu-id="8b12a-367">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="8b12a-368">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8b12a-368">Az.Sql</span></span>
* <span data-ttu-id="8b12a-369">Dokumentation alter Überwachungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-369">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8b12a-370">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8b12a-370">Az.Storage</span></span>
* <span data-ttu-id="8b12a-371">Hilfe für „Get/Close-AzStorageFileHandle“ aktualisiert (weitere Szenarien zu Cmdlet-Beispielen hinzugefügt und Parameterbeschreibungen aktualisiert)</span><span class="sxs-lookup"><span data-stu-id="8b12a-371">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="8b12a-372">Unterstützung von „StandardBlobTier“ in Uploadblobs und Kopierblobs</span><span class="sxs-lookup"><span data-stu-id="8b12a-372">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="8b12a-373">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8b12a-373">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="8b12a-374">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8b12a-374">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="8b12a-375">Unterstützung der Aktivierungspriorität im Kopierblob</span><span class="sxs-lookup"><span data-stu-id="8b12a-375">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="8b12a-376">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8b12a-376">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8b12a-377">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8b12a-377">Az.Websites</span></span>
* <span data-ttu-id="8b12a-378">Hinzufügen von Erläuterungen zum Parameter „-AppSettings“ in „Set-AzWebApp“ und „Set-AzWebAppSlot“</span><span class="sxs-lookup"><span data-stu-id="8b12a-378">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="8b12a-379">2.5.0: Juli 2019</span><span class="sxs-lookup"><span data-stu-id="8b12a-379">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8b12a-380">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8b12a-380">Az.Accounts</span></span>
* <span data-ttu-id="8b12a-381">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="8b12a-381">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="8b12a-382">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="8b12a-382">Az.ApplicationInsights</span></span>
* <span data-ttu-id="8b12a-383">Tippfehler im Beispiel in der Dokumentation zu „Remove-AzApplicationInsightsApiKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-383">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8b12a-384">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8b12a-384">Az.Automation</span></span>
* <span data-ttu-id="8b12a-385">Tippfehler in der Ressourcenzeichenfolge korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-385">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8b12a-386">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8b12a-386">Az.CognitiveServices</span></span>
* <span data-ttu-id="8b12a-387">Unterstützung für NetworkRuleSet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-387">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8b12a-388">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8b12a-388">Az.Compute</span></span>
* <span data-ttu-id="8b12a-389">Fehlende Eigenschaften (ComputerName, OsName, OsVersion und HyperVGeneration) des Objekts für die VM-Instanzenansicht hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-389">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="8b12a-390">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8b12a-390">Az.ContainerRegistry</span></span>
* <span data-ttu-id="8b12a-391">Tippfehler in „Remove-AzContainerRegistryReplication“ für den Replikationsparameter korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-391">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="8b12a-392">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="8b12a-392">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8b12a-393">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8b12a-393">Az.DataFactory</span></span>
* <span data-ttu-id="8b12a-394">Version des ADF .NET SDK auf 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-394">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="8b12a-395">Tippfehler in der Dokumentation für „Get-AzDataFactoryV2PipelineRun“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-395">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8b12a-396">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8b12a-396">Az.EventHub</span></span>
* <span data-ttu-id="8b12a-397">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="8b12a-397">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="8b12a-398">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="8b12a-398">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8b12a-399">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8b12a-399">Az.KeyVault</span></span>
* <span data-ttu-id="8b12a-400">Unterstützung zum Angeben von KeySize für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-400">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8b12a-401">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8b12a-401">Az.LogicApp</span></span>
* <span data-ttu-id="8b12a-402">Korrektur für „Get-AzIntegrationAccountMap“ zum Auflisten aller Zuordnungstypen</span><span class="sxs-lookup"><span data-stu-id="8b12a-402">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="8b12a-403">Neuer MapType-Parameter für Filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-403">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="8b12a-404">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="8b12a-404">Az.ManagedServices</span></span>
* <span data-ttu-id="8b12a-405">Unterstützung für API-Version 2019-06-01 (GA) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-405">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8b12a-406">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8b12a-406">Az.Network</span></span>
* <span data-ttu-id="8b12a-407">Unterstützung für privaten Endpunkt und privaten Verknüpfungsdienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-407">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="8b12a-408">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8b12a-408">New cmdlets</span></span>
        - <span data-ttu-id="8b12a-409">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8b12a-409">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8b12a-410">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8b12a-410">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8b12a-411">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8b12a-411">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8b12a-412">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8b12a-412">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8b12a-413">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8b12a-413">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8b12a-414">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8b12a-414">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8b12a-415">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="8b12a-415">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="8b12a-416">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8b12a-416">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="8b12a-417">Folgende Befehle für das Feature aktualisiert: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies für Subnetz in VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8b12a-417">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="8b12a-418">„New-AzVirtualNetworkSubnetConfig“, „Set-AzVirtualNetworkSubnetConfig“ und „Add-AzVirtualNetworkSubnetConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-418">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="8b12a-419">Optionaler Parameter „-PrivateEndpointNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den privaten Endpunkt in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="8b12a-419">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="8b12a-420">Optionaler Parameter „-PrivateLinkServiceNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den Privat Link-Dienst in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="8b12a-420">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="8b12a-421">Der Cmdlet-Parameter „ServiceName“ von AzPrivateLinkService wurde aus Gründen der Abwärtskompatibilität in „Name“ mit dem Alias „ServiceName“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="8b12a-421">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="8b12a-422">ICMP-Protokoll für Konfigurationen von Netzwerksicherheitsregeln aktiviert</span><span class="sxs-lookup"><span data-stu-id="8b12a-422">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="8b12a-423">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8b12a-423">Updated cmdlets</span></span>
        - <span data-ttu-id="8b12a-424">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8b12a-424">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8b12a-425">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8b12a-425">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8b12a-426">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8b12a-426">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="8b12a-427">ConnectionProtocolType (Ikev1/Ikev2) als konfigurierbarer Parameter für „New-AzVirtualNetworkGatewayConnection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-427">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="8b12a-428">PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-428">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="8b12a-429">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8b12a-429">Updated cmdlet:</span></span>
        - <span data-ttu-id="8b12a-430">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8b12a-430">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="8b12a-431">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8b12a-431">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="8b12a-432">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8b12a-432">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="8b12a-433">Application Gateway-Befehl „New-AzApplicationGatewayProbeConfig“ zur Unterstützung des benutzerdefinierten Ports im Test aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-433">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="8b12a-434">„New-AzApplicationGatewayProbeConfig“ aktualisiert: Optionaler Parameter „Port“ hinzugefügt, der zum Testen des Back-End-Servers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8b12a-434">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="8b12a-435">Dieser Parameter gilt für Standard_V2 und WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="8b12a-435">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8b12a-436">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8b12a-436">Az.OperationalInsights</span></span>
* <span data-ttu-id="8b12a-437">Standardversion für gespeicherte Suchvorgänge auf 1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-437">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="8b12a-438">Verarbeitung des regulären NULL-Ausdrucks in benutzerdefinierten Protokollen korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-438">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8b12a-439">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8b12a-439">Az.RecoveryServices</span></span>
* <span data-ttu-id="8b12a-440">„Get-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-440">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="8b12a-441">„Get-AzRecoveryServicesBackupContainer.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-441">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="8b12a-442">„Get-AzRecoveryServicesVault.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-442">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="8b12a-443">„Wait-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-443">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="8b12a-444">„Set-AzRecoveryServicesVaultContext.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-444">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="8b12a-445">„Get-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-445">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="8b12a-446">„Get-AzRecoveryServicesBackupRecoveryPoint.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-446">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="8b12a-447">„Restore-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-447">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="8b12a-448">Dienstaufruf zum Aufheben der Containerregistrierung für Azure-Dateifreigabe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-448">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="8b12a-449">„Set-AzRecoveryServicesAsrAlertSetting.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-449">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="8b12a-450">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8b12a-450">Az.Resources</span></span>
- <span data-ttu-id="8b12a-451">Fehlendes Cmdlet entfernt, auf das in der Dokumentation zu „New-AzResourceGroupDeployment“ verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="8b12a-451">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="8b12a-452">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-452">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8b12a-453">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8b12a-453">Az.ServiceBus</span></span>
* <span data-ttu-id="8b12a-454">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="8b12a-454">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="8b12a-455">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="8b12a-455">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="8b12a-456">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8b12a-456">Az.Sql</span></span>
* <span data-ttu-id="8b12a-457">Fehlende Beispiele für Cmdlet „Set-AzSqlDatabaseSecondary“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-457">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="8b12a-458">Festlegen wiederkehrender Überprüfungen der Sicherheitsrisikobewertung ohne Angabe von E-Mail-Adressen korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-458">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="8b12a-459">Tippfehler in einer Warnmeldung korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-459">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8b12a-460">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8b12a-460">Az.Storage</span></span>
* <span data-ttu-id="8b12a-461">Beispiel in Referenzdokumentation für „Get-AzStorageAccount“ aktualisiert, sodass der richtige Parametername verwendet wird</span><span class="sxs-lookup"><span data-stu-id="8b12a-461">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="8b12a-462">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="8b12a-462">Az.StorageSync</span></span>
* <span data-ttu-id="8b12a-463">Cmdlet „Invoke-AzStorageSyncChangeDetection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-463">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="8b12a-464">Problem 9551 zur Berücksichtigung von „TierFilesOlderThanDays“ behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-464">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8b12a-465">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8b12a-465">Az.Websites</span></span>
* <span data-ttu-id="8b12a-466">Problem behoben, aufgrund dessen einige SiteConfig-Eigenschaften von „Get-AzWebApp“ und „Set-AzWebApp“ nicht zurückgegeben wurden</span><span class="sxs-lookup"><span data-stu-id="8b12a-466">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="8b12a-467">Neuer Standortparameter zu „Get-AzDeletedWebApp“ und „Restore-AzDeletedWebApp“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-467">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="8b12a-468">Fehler beim Klonen von Web-App-Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-468">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="8b12a-469">2.4.0 – Juli 2019</span><span class="sxs-lookup"><span data-stu-id="8b12a-469">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8b12a-470">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8b12a-470">Az.Accounts</span></span>
* <span data-ttu-id="8b12a-471">Unterstützung für Profil-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-471">Add support for profile cmdlets</span></span>
* <span data-ttu-id="8b12a-472">Unterstützung für Umgebungen und Datenebenen in generierten Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-472">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="8b12a-473">Korrektur eines Fehlers, bei dem in einigen Fällen ein falscher Endpunkt für Datenebenen-Cmdlets in Windows PowerShell verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="8b12a-473">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="8b12a-474">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="8b12a-474">Az.Advisor</span></span>
* <span data-ttu-id="8b12a-475">Allgemein verfügbares Release von Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="8b12a-475">GA release of Az.Advisor</span></span>
* <span data-ttu-id="8b12a-476">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="8b12a-476">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8b12a-477">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8b12a-477">Az.ApiManagement</span></span>
* <span data-ttu-id="8b12a-478">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="8b12a-478">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="8b12a-479">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="8b12a-479">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="8b12a-480">Unterstützung für Abfragen von Abonnements nach Benutzer und Produkt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-480">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="8b12a-481">Unterstützung für Abfragen anhand des Umfangs hinzugefügt, „/“, „/apis“, „/apis/echo-api“</span><span class="sxs-lookup"><span data-stu-id="8b12a-481">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="8b12a-482">Behebung von Problem https://github.com/Azure/azure-powershell/issues/9307 und https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="8b12a-482">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="8b12a-483">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="8b12a-483">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="8b12a-484">Unterstützung für die Angabe von „ApiVersion“ und „ApiVersionSetId“ beim Importieren von APIs hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-484">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8b12a-485">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8b12a-485">Az.Automation</span></span>
* <span data-ttu-id="8b12a-486">Fehler beim Cmdlet „Set-AzAutomationConnectionFieldValue“ für die Verarbeitung des Zeichenfolgewerts behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-486">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8b12a-487">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8b12a-487">Az.Compute</span></span>
* <span data-ttu-id="8b12a-488">Parameter „HyperVGeneration“ zu New-AzImageConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-488">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8b12a-489">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8b12a-489">Az.DataFactory</span></span>
* <span data-ttu-id="8b12a-490">Aktualisierung der Ausgabe von ADF-Cmdlets für das Abrufen von Aktivitäts-, Pipeline- und Auslöserausführungen, um die Pipe „Select-Object“ zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="8b12a-490">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8b12a-491">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8b12a-491">Az.EventGrid</span></span>
* <span data-ttu-id="8b12a-492">Tippfehler in Dokumentation zu 'New-AzEventGridSubscription' behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-492">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8b12a-493">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8b12a-493">Az.IotHub</span></span>
* <span data-ttu-id="8b12a-494">Unterstützung für das erneute Generieren von Autorisierungsrichtlinienschlüsseln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-494">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8b12a-495">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8b12a-495">Az.Network</span></span>
* <span data-ttu-id="8b12a-496">„RoutingPreference“ zu öffentlichen IP-Tags hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-496">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="8b12a-497">Beispiele für Referenzdokumentation zu „Get-AzNetworkServiceTag“ verbessert</span><span class="sxs-lookup"><span data-stu-id="8b12a-497">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8b12a-498">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8b12a-498">Az.PolicyInsights</span></span>
* <span data-ttu-id="8b12a-499">Fehlerbehebung für Nullverweis in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="8b12a-499">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="8b12a-500">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="8b12a-500">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8b12a-501">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8b12a-501">Az.OperationalInsights</span></span>
* <span data-ttu-id="8b12a-502">Zurückgegebenes CustomLog-Datenquellenmodell in Get-AzOperationalInsightsDataSource korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-502">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8b12a-503">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8b12a-503">Az.RecoveryServices</span></span>
* <span data-ttu-id="8b12a-504">Fehlerbehebung für Befehl „get-policy“ IaaSVMs</span><span class="sxs-lookup"><span data-stu-id="8b12a-504">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="8b12a-505">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8b12a-505">Az.Resources</span></span>
    - <span data-ttu-id="8b12a-506">Hilfetext für Parameter „-Top“ von „Get-AzPolicyState“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-506">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="8b12a-507">Clientseitige Unterstützung von Paginierung für „Get-AzPolicyAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-507">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="8b12a-508">Neue Parameter für „Set-AzPolicyAssignment“, „-PolicyParameters“ und „-PolicyParametersObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-508">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="8b12a-509">Einige Aktualisierungen von Dokumentationen und Beispielen für Policy-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8b12a-509">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8b12a-510">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8b12a-510">Az.ServiceBus</span></span>
* <span data-ttu-id="8b12a-511">Korrektur für Problem Nr. 4938: „New-AzureRmServiceBusQueue“ gibt beim Festlegen von „MaxSizeInMegabytes“ „BadRequest“ zurück</span><span class="sxs-lookup"><span data-stu-id="8b12a-511">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="8b12a-512">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8b12a-512">Az.Sql</span></span>
* <span data-ttu-id="8b12a-513">Instanzfailovergruppen-Cmdlets aus Vorschauversion in öffentliche Version hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-513">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="8b12a-514">Unterstützung von Azure SQL Server\Datenbanküberwachung mit neuen Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8b12a-514">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="8b12a-515">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="8b12a-515">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="8b12a-516">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="8b12a-516">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="8b12a-517">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="8b12a-517">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="8b12a-518">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="8b12a-518">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="8b12a-519">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="8b12a-519">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="8b12a-520">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="8b12a-520">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="8b12a-521">E-Mail-Einschränkungen aus Einstellungen der Sicherheitsrisikobewertung entfernt</span><span class="sxs-lookup"><span data-stu-id="8b12a-521">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8b12a-522">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8b12a-522">Az.Storage</span></span>
* <span data-ttu-id="8b12a-523">Zwei Parameter („-IndexDocument“ und „-ErrorDocument404Path“) in folgendem Cmdlet von erforderlich in optional geändert:</span><span class="sxs-lookup"><span data-stu-id="8b12a-523">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="8b12a-524">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8b12a-524">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="8b12a-525">Hilfe zu „Get-AzStorageBlobContent“ mit neuem Beispiel ergänzt</span><span class="sxs-lookup"><span data-stu-id="8b12a-525">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="8b12a-526">Anzeige von mehr Fehlerinformationen beim Fehlschlagen eines Cmdlets mit „StorageException“</span><span class="sxs-lookup"><span data-stu-id="8b12a-526">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="8b12a-527">Unterstützung für das Erstellen oder Aktualisieren von Speicherkonten mit Azure Files AAD-DS-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="8b12a-527">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="8b12a-528">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8b12a-528">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="8b12a-529">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8b12a-529">Set-AzStorageAccount</span></span>
* <span data-ttu-id="8b12a-530">Unterstützung für das Auflisten oder Schließen von Dateihandles einer Dateifreigabe, eines Dateiverzeichnisses oder einer Datei</span><span class="sxs-lookup"><span data-stu-id="8b12a-530">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="8b12a-531">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="8b12a-531">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="8b12a-532">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="8b12a-532">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="8b12a-533">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="8b12a-533">Az.StorageSync</span></span>
* <span data-ttu-id="8b12a-534">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="8b12a-534">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="8b12a-535">2.3.2 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="8b12a-535">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8b12a-536">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8b12a-536">Az.Accounts</span></span>
* <span data-ttu-id="8b12a-537">Fehler behoben, aufgrund dessen in manchen Fällen eine falsche URL für Funktionsaufrufe verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="8b12a-537">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="8b12a-538">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="8b12a-538">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="8b12a-539">Problem mit Aliasen zwischen AzureRM und Azure-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-539">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="8b12a-540">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8b12a-540">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="8b12a-541">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="8b12a-541">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8b12a-542">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8b12a-542">Az.Compute</span></span>
* <span data-ttu-id="8b12a-543">Die einfachen Parametersätze „New-AzVm“ und „New-AzVmss“ akzeptieren jetzt den Parameter „ProximityPlacementGroup“.</span><span class="sxs-lookup"><span data-stu-id="8b12a-543">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="8b12a-544">Tippfehler in der Referenzdokumentation für „New-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-544">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="8b12a-545">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="8b12a-545">Az.Dns</span></span>
* <span data-ttu-id="8b12a-546">Tippfehler in den Hilfebeispielen zu „Set-AzDnsZone“ behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-546">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8b12a-547">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8b12a-547">Az.EventGrid</span></span>
* <span data-ttu-id="8b12a-548">Zur Verwendung der API-Version 2019-06-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-548">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="8b12a-549">Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="8b12a-549">New cmdlets:</span></span>
    - <span data-ttu-id="8b12a-550">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="8b12a-550">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="8b12a-551">Erstellt eine neue Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="8b12a-551">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="8b12a-552">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="8b12a-552">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="8b12a-553">Ruft die Details einer Event Grid-Domäne oder eine Liste aller Event Grid-Domänen im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="8b12a-553">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="8b12a-554">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="8b12a-554">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="8b12a-555">Entfernt eine Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="8b12a-555">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="8b12a-556">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="8b12a-556">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="8b12a-557">Generiert den freigegebenen Zugriffsschlüssel für eine Azure Event Grid-Domäne erneut.</span><span class="sxs-lookup"><span data-stu-id="8b12a-557">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="8b12a-558">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="8b12a-558">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="8b12a-559">Ruft die freigegebenen Zugriffsschlüssel ab, die zum Veröffentlichen von Ereignissen in einer Event Grid-Domäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8b12a-559">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="8b12a-560">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="8b12a-560">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="8b12a-561">Erstellt ein neues Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="8b12a-561">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="8b12a-562">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="8b12a-562">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="8b12a-563">Ruft die Details eines Event Grid-Domänenthemas oder eine Liste aller Event Grid-Domänenthemen unter der jeweiligen Event Grid-Domäne im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="8b12a-563">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="8b12a-564">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="8b12a-564">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="8b12a-565">Entfernt ein vorhandenes Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="8b12a-565">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="8b12a-566">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="8b12a-566">Updated cmdlets:</span></span>
    - <span data-ttu-id="8b12a-567">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="8b12a-567">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="8b12a-568">Neue erforderliche Parameter zur Unterstützung des Pipings für die neue Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="8b12a-568">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="8b12a-569">Neue erforderliche Parameter zum Angeben des neuen Event Grid-Domänennamens und/oder Namens des Event Grid-Domänenthemas hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="8b12a-569">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="8b12a-570">Neue Parametersätze für Domänen und Domänenthemen hinzugefügt, um die Wiederverwendung vorhandener Parameter zuzulassen (‚z. B. „EndPointType“, „SubjectBeginsWith“ usw.)</span><span class="sxs-lookup"><span data-stu-id="8b12a-570">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="8b12a-571">Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="8b12a-571">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="8b12a-572">Ablaufdatum des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="8b12a-572">Event subscription expiration date,</span></span>
            - <span data-ttu-id="8b12a-573">Erweiterte Filterparameter</span><span class="sxs-lookup"><span data-stu-id="8b12a-573">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="8b12a-574">Neue Enumeration für „servicebusqueue“ als Ziel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-574">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="8b12a-575">Verwendung der Option „All“ in „-IncludedEventType“ gesperrt und wie folgt ersetzt</span><span class="sxs-lookup"><span data-stu-id="8b12a-575">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="8b12a-576">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="8b12a-576">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="8b12a-577">Neue optionale Parameter („Top“, „ODataQuery“ und „NextLink“) zur Unterstützung der Ergebnispaginierung und -filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-577">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="8b12a-578">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="8b12a-578">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="8b12a-579">Neue erforderliche Parameter zur Unterstützung des Pipings für die Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Entfernen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="8b12a-579">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="8b12a-580">Neue erforderliche Parameter zum Angeben des Event Grid-Domänennamens und/oder Event Grid-Domänenthemanamens hinzugefügt, um das Entfernen vorhandener Ereignisabonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="8b12a-580">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8b12a-581">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8b12a-581">Az.FrontDoor</span></span>
* <span data-ttu-id="8b12a-582">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="8b12a-582">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="8b12a-583">Unterstützung von Transformationen und neuen Wert für den Operator zum automatischen Vervollständigen (RegEx) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-583">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="8b12a-584">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="8b12a-584">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="8b12a-585">Neue Werte für automatisches Vervollständigen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-585">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8b12a-586">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8b12a-586">Az.Network</span></span>
* <span data-ttu-id="8b12a-587">Unterstützung für Virtual Network-Gatewayressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-587">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="8b12a-588">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8b12a-588">New cmdlets</span></span>
        - <span data-ttu-id="8b12a-589">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="8b12a-589">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="8b12a-590">AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="8b12a-590">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="8b12a-591">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8b12a-591">New cmdlets</span></span>
        - <span data-ttu-id="8b12a-592">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="8b12a-592">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="8b12a-593">„PrivatePrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-593">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="8b12a-594">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8b12a-594">New cmdlets</span></span>
        - <span data-ttu-id="8b12a-595">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8b12a-595">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8b12a-596">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8b12a-596">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8b12a-597">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8b12a-597">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8b12a-598">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8b12a-598">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="8b12a-599">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8b12a-599">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="8b12a-600">„PrivateEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-600">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="8b12a-601">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8b12a-601">New cmdlets</span></span>
        - <span data-ttu-id="8b12a-602">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8b12a-602">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8b12a-603">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8b12a-603">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8b12a-604">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8b12a-604">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8b12a-605">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="8b12a-605">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="8b12a-606">Folgende Befehle für das Feature aktualisiert: UseLocalAzureIpAddress-Flag für „VpnConnection“</span><span class="sxs-lookup"><span data-stu-id="8b12a-606">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="8b12a-607">„New-AzVpnConnection§ „ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="8b12a-607">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="8b12a-608">„Set-AzVpnConnection“ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="8b12a-608">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="8b12a-609">Schreibgeschütztes Feld „PeeredConnections“ beim ExpressRoute-Peering hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-609">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="8b12a-610">Schreibgeschütztes Feld „GlobalReachEnabled“ in ExpressRoute hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-610">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="8b12a-611">Breaking Change-Attribut hinzugefügt, um auf das veraltete Feld „AllowGlobalReach“ im ExpressRouteCircuit-Modell hinzuweisen</span><span class="sxs-lookup"><span data-stu-id="8b12a-611">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="8b12a-612">Fehler 8756 bei der Verwendung von „TargetListenerID“ mit AzApplicationGatewayRedirectConfiguration-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-612">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="8b12a-613">Fehler in „New-AzApplicationGatewayPathRuleConfig“ behoben, aufgrund dessen der Regelsatz für erneutes Generieren nicht festgelegt werden konnte</span><span class="sxs-lookup"><span data-stu-id="8b12a-613">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="8b12a-614">Fehler bei der Anzeige von „VirtualNetworkTaps“ in „NetworkInterfaceIpConfiguration“ behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-614">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="8b12a-615">Cortex-Get-Cmdlets zum Auflisten aller Komponenten korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-615">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="8b12a-616">Problem beim Erstellen des festen VirtualHub-Verweises für ExpressRouteGateways behoben (VpnGateway)</span><span class="sxs-lookup"><span data-stu-id="8b12a-616">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="8b12a-617">Unterstützung für Verfügbarkeitszonen in AzureFirewall und NatGateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-617">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="8b12a-618">Cmdlet „Get-AzNetworkServiceTag“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-618">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="8b12a-619">Unterstützung für mehrere öffentliche IP-Adressen für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-619">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="8b12a-620">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="8b12a-620">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="8b12a-621">Parameter „-PublicIpAddress“ hinzugefügt, der ein oder mehre öffentliche IP-Adressobjekte akzeptiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-621">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="8b12a-622">Parameter „- VirtualNetwork“ hinzugefügt, der ein Virtual Network-Objekt akzeptiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-622">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="8b12a-623">Methoden „AddPublicIpAddress“ und „RemovePublicIpAddress“ für Firewallobjekte hinzugefügt (akzeptieren ein öffentliches IP-Adressobjekt als Eingabe)</span><span class="sxs-lookup"><span data-stu-id="8b12a-623">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="8b12a-624">Parameter „-PublicIpName“ und „-VirtualNetworkName“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-624">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="8b12a-625">Folgende Befehle für das Feature aktualisiert: VpnClient-AAD-Authentifizierungsoptionen auf die Gatewayressource des virtuellen Netzwerkgateways festgelegt</span><span class="sxs-lookup"><span data-stu-id="8b12a-625">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="8b12a-626">„New-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-626">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="8b12a-627">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8b12a-627">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="8b12a-628">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionaler Switch-Parameter „RemoveAadAuthentication“ zum Entfernen von VpnClient-AAD-Authentifizierungsoptionen aus dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-628">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8b12a-629">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8b12a-629">Az.OperationalInsights</span></span>
* <span data-ttu-id="8b12a-630">Tarif **pergb2018** im Befehl „New-AzureRmOperationalInsightsWorkspace“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="8b12a-630">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="8b12a-631">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8b12a-631">Az.Resources</span></span>
* <span data-ttu-id="8b12a-632">Unterstützung für zusätzliche Optionen zum Exportieren von Vorlagen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-632">Support for additional Template Export options</span></span>
    - <span data-ttu-id="8b12a-633">Parameter „-SkipResourceNameParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-633">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="8b12a-634">Parameter -SkipAllParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-634">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="8b12a-635">Parameter „-Resource“ zu „Export-AzResourceGroup“ hinzugefügt, um das Filtern exportierter Ressourcen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="8b12a-635">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8b12a-636">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8b12a-636">Az.ServiceFabric</span></span>
* <span data-ttu-id="8b12a-637">Problem beim Hinzufügen des Zertifikats mit „ByExistingKeyVault“ behoben (Abruf des falschen Fingerabdrucks in manchen Fällen)</span><span class="sxs-lookup"><span data-stu-id="8b12a-637">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="8b12a-638">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8b12a-638">Az.Sql</span></span>
* <span data-ttu-id="8b12a-639">Suffix des Advanced Threat Protection-Endpunkts korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-639">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="8b12a-640">Durch Advanced Data Security ermöglichte Außerkraftsetzungen der Advanced Threat Protection-Richtlinie korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-640">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="8b12a-641">Neue Cmdlets für „Management.Sql“ ermöglichen Kunden das Hinzufügen von TDE-Schlüsseln und Festlegen der TDE-Schutzvorrichtung für verwaltete Instanzen.</span><span class="sxs-lookup"><span data-stu-id="8b12a-641">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="8b12a-642">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8b12a-642">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="8b12a-643">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8b12a-643">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="8b12a-644">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8b12a-644">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="8b12a-645">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="8b12a-645">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="8b12a-646">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="8b12a-646">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8b12a-647">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8b12a-647">Az.Storage</span></span>
* <span data-ttu-id="8b12a-648">Unterstützung von „FileStorage“ und „SkuName Premium_ZRS“ beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="8b12a-648">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="8b12a-649">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8b12a-649">New-AzStorageAccount</span></span>
* <span data-ttu-id="8b12a-650">Überarbeitete Beschreibung des Cmdlets für die Unveränderlichkeit von Blobs</span><span class="sxs-lookup"><span data-stu-id="8b12a-650">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="8b12a-651">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8b12a-651">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8b12a-652">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8b12a-652">Az.Websites</span></span>
* <span data-ttu-id="8b12a-653">Optimiert „Get-AzWebAppCertificate“, um nach der Ressourcengruppe auf dem Server zu filtern (nicht auf dem Client)</span><span class="sxs-lookup"><span data-stu-id="8b12a-653">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="8b12a-654">Switch-Parameter „-UseDisasterRecovery“ für „Get-AzWebAppSnapshot“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-654">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="8b12a-655">2.2.0 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="8b12a-655">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="8b12a-656">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8b12a-656">Az.Cdn</span></span>
* <span data-ttu-id="8b12a-657">Es wurden Cmdlets aktualisiert, um das rulesEngine-Feature basierend auf der API-Version 2019-04-15 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8b12a-657">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8b12a-658">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8b12a-658">Az.Compute</span></span>
* <span data-ttu-id="8b12a-659">Der Parameter `NoWait` wurde hinzugefügt, der den Vorgang startet und sofort zurückkehrt, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="8b12a-659">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="8b12a-660">Aktualisierte Cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="8b12a-660">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8b12a-661">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8b12a-661">Az.EventHub</span></span>
* <span data-ttu-id="8b12a-662">Fehlerbehebung für #9231 – Get-AzEventHubNamespace gibt keine Tags zurück</span><span class="sxs-lookup"><span data-stu-id="8b12a-662">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="8b12a-663">Fehlerbehebung für #9230 – Get-AzEventHubNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="8b12a-663">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8b12a-664">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8b12a-664">Az.Network</span></span>
* <span data-ttu-id="8b12a-665">ResourceId und InputObject wurden für NAT Gateway aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-665">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="8b12a-666">Es wurde ein Alias für ResourceId und InputObjectr hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-666">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8b12a-667">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8b12a-667">Az.PolicyInsights</span></span>
* <span data-ttu-id="8b12a-668">Fehlerbehebung für Nullverweis in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="8b12a-668">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8b12a-669">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8b12a-669">Az.RecoveryServices</span></span>
* <span data-ttu-id="8b12a-670">Minimale Aufbewahrung in Tagen für IaaSVM-Richtlinie wurde von 1 in 7 geändert</span><span class="sxs-lookup"><span data-stu-id="8b12a-670">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8b12a-671">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8b12a-671">Az.ServiceBus</span></span>
* <span data-ttu-id="8b12a-672">Fehlerbehebung für #9182 – Get-AzServiceBusNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="8b12a-672">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8b12a-673">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8b12a-673">Az.ServiceFabric</span></span>
* <span data-ttu-id="8b12a-674">Tippfehler in Fehlermeldung für Update-AzServiceFabricReliability wurde behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-674">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="8b12a-675">Fehlendes Zeichen in Service Fabric-Befehlszeilen wurde behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-675">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="8b12a-676">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8b12a-676">Az.Sql</span></span>
* <span data-ttu-id="8b12a-677">Der DnsZonePartner-Parameter für das Cmdlet New-AzureSqlInstance wurde hinzugefügt, um AutoDr für verwaltete Instanzen zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="8b12a-677">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="8b12a-678">Das Cmdlet Get-AzSqlDatabaseSecureConnectionPolicy wird eingestellt</span><span class="sxs-lookup"><span data-stu-id="8b12a-678">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="8b12a-679">Cmdlets zum Schutz vor Bedrohungen werden in „Advanced Threat Protection“ (Erweiterter Schutz vor Bedrohungen) umbenannt</span><span class="sxs-lookup"><span data-stu-id="8b12a-679">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="8b12a-680">New-AzSqlInstance – Die Parameter StorageSizeInGB und LicenseType sind jetzt optional</span><span class="sxs-lookup"><span data-stu-id="8b12a-680">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8b12a-681">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8b12a-681">Az.Websites</span></span>
* <span data-ttu-id="8b12a-682">Das Problem, bei dem die Verwendung von Set-AzWebApp und Set-AzWebAppSlot mit der -WebApp-Eigenschaft die Tags entfernt hat, wurde behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-682">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="8b12a-683">2.1.0 – Mai 2019</span><span class="sxs-lookup"><span data-stu-id="8b12a-683">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="8b12a-684">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8b12a-684">Az.ApiManagement</span></span>
* <span data-ttu-id="8b12a-685">Es wurden neue Cmdlets zum Verwalten der Diagnose im globalen sowie im API-Bereich erstellt</span><span class="sxs-lookup"><span data-stu-id="8b12a-685">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="8b12a-686">**Get-AzApiManagementDiagnostic**: Abrufen der Diagnose, die im globalen oder im API-Bereich konfiguriert wurde</span><span class="sxs-lookup"><span data-stu-id="8b12a-686">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="8b12a-687">**New-AzApiManagementDiagnostic**: Erstellen neuer Diagnosen im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="8b12a-687">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="8b12a-688">**New-AzApiManagementHttpMessageDiagnostic**: Erstellen einer Diagnoseeinstellung für die zu protokollierenden Kopfzeilen und für die Größe der Bytes für den Text</span><span class="sxs-lookup"><span data-stu-id="8b12a-688">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="8b12a-689">**New-AzApiManagementPipelineDiagnosticSetting**: Erstellen von Diagnoseeinstellungen für ein-/ausgehende HTTP-Nachrichten für das Gateway</span><span class="sxs-lookup"><span data-stu-id="8b12a-689">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="8b12a-690">**New-AzApiManagementSamplingSetting**: Erstellen der Einstellung „Sampling“ für die Anforderungen/Antworten für eine Diagnose</span><span class="sxs-lookup"><span data-stu-id="8b12a-690">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="8b12a-691">**Remove-AzApiManagementDiagnostic**: Entfernen einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="8b12a-691">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="8b12a-692">**Set-AzApiManagementDiagnostic**: Aktualisieren einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="8b12a-692">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="8b12a-693">Es wurden neue Cmdlets für die Cacheverwaltung im ApiManagement-Dienst erstellt</span><span class="sxs-lookup"><span data-stu-id="8b12a-693">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="8b12a-694">**Get-AzApiManagementCache**: Abrufen der Details des durch den Bezeichner angegebenen Caches oder aller Caches</span><span class="sxs-lookup"><span data-stu-id="8b12a-694">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="8b12a-695">**New-AzApiManagementCache**: Erstellen eines neuen „standardmäßigen“ Caches oder eines Caches in einer bestimmten „Region“ von Azure</span><span class="sxs-lookup"><span data-stu-id="8b12a-695">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="8b12a-696">**Remove-AzApiManagementCache**: Entfernen eines Caches</span><span class="sxs-lookup"><span data-stu-id="8b12a-696">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="8b12a-697">**Update-AzApiManagementCache**: Aktualisieren eines Caches</span><span class="sxs-lookup"><span data-stu-id="8b12a-697">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="8b12a-698">Es wurden neue Cmdlets zur Verwaltung von API-Schemas erstellt</span><span class="sxs-lookup"><span data-stu-id="8b12a-698">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="8b12a-699">**New-AzApiManagementSchema**: Erstellen eines neuen Schemas für eine API</span><span class="sxs-lookup"><span data-stu-id="8b12a-699">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="8b12a-700">**Get-AzApiManagementSchema**: Abrufen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="8b12a-700">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="8b12a-701">**Remove-AzApiManagementSchema**: Entfernen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="8b12a-701">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="8b12a-702">**Set-AzApiManagementSchema**: Aktualisieren des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="8b12a-702">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="8b12a-703">Es wurde ein neues Cmdlet zum Generieren eines Benutzertokens erstellt</span><span class="sxs-lookup"><span data-stu-id="8b12a-703">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="8b12a-704">**New-AzApiManagementUserToken**: Generieren eines neuen Benutzertokens, das standardmäßig für acht Stunden gültig ist. Mit diesem Cmdlet kann das Token für den „GIT“-Benutzer generiert werden./</span><span class="sxs-lookup"><span data-stu-id="8b12a-704">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="8b12a-705">Es wurde ein neues Cmdlet zum Abrufen des Netzwerkstatus erstellt</span><span class="sxs-lookup"><span data-stu-id="8b12a-705">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="8b12a-706">**Get-AzApiManagementNetworkStatus**: Abrufen der Netzwerkstatuskonnektivität von Ressourcen, von denen der API Management-Dienst abhängig ist</span><span class="sxs-lookup"><span data-stu-id="8b12a-706">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="8b12a-707">Dies ist hilfreich, wenn Sie den ApiManagement-Dienst in einem virtuellen Netzwerk bereitstellen und überprüfen, ob eine der Abhängigkeiten fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="8b12a-707">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="8b12a-708">Das Cmdlet **New-AzApiManagement** wurde zum Verwalten des ApiManagement-Diensts aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-708">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="8b12a-709">Die Unterstützung für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-709">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="8b12a-710">Die Unterstützung zum Aktivieren des Flags „EnableClientCertificate“ für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-710">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="8b12a-711">Das neue Cmdlet **New-AzApiManagementSslSetting** ermöglicht die Konfiguration der „TLS/SSL“-Einstellung für „Back-End“ und „Front-End“</span><span class="sxs-lookup"><span data-stu-id="8b12a-711">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="8b12a-712">Dies kann auch dazu verwendet werden, um „Verschlüsselungen“ wie „3DES“ und „ServerProtokolle“ wie „Http2“ für das „Front-End“ eines ApiManagement-Diensts zu konfigurieren</span><span class="sxs-lookup"><span data-stu-id="8b12a-712">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="8b12a-713">Die Unterstützung für die Konfiguration des Hostnamens „DeveloperPortal“ wurde zum ApiManagement-Dienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-713">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="8b12a-714">Die **Get-AzApiManagementSsoToken**-Cmdlets wurden aktualisiert, um das Objekt „PsApiManagement“ als Eingabe zu übernehmen</span><span class="sxs-lookup"><span data-stu-id="8b12a-714">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="8b12a-715">Das Cmdlet wurde aktualisiert, um Fehlermeldungen inline anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="8b12a-715">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="8b12a-716">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Fehlercode: ValidationError-Fehlermeldung: Mindestens ein Feld enthält ungültige Werte: Fehlerdetails: [Code=ValidationError, Message=Fehler in Element 'log-to-eventhub' in Zeile 3, Spalte 10: Protokollierungstool nicht gefunden, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="8b12a-716">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="8b12a-717">Cmdlet **Export-AzApiManagementApi** wurde für den Export von APIs im Format „OpenApi 3.0“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-717">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="8b12a-718">Cmdlet **Import-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-718">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="8b12a-719">Zum Importieren der API aus der „OpenApi 3.0“-Dokumentspezifikation</span><span class="sxs-lookup"><span data-stu-id="8b12a-719">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="8b12a-720">Zur Außerkraftsetzung der „PsApiManagementSchema“-Eigenschaft, die in einem beliebigen Dokument („Swagger“, „Wadl“, „Wsdl“, „OpenApi“) angegeben ist</span><span class="sxs-lookup"><span data-stu-id="8b12a-720">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="8b12a-721">Zur Außerkraftsetzung der „ServiceUrl“-Eigenschaft, die in einem beliebigen Dokument angegeben ist</span><span class="sxs-lookup"><span data-stu-id="8b12a-721">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="8b12a-722">Cmdlet **Get-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="8b12a-722">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="8b12a-723">Cmdlet **Set-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ und im Format mit XML-Escapezeichen mit „xml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="8b12a-723">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="8b12a-724">Cmdlet **New-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-724">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="8b12a-725">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="8b12a-725">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="8b12a-726">Zum Erstellen einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="8b12a-726">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="8b12a-727">Zum Klonen einer API mithilfe von „SourceApiId“ und „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="8b12a-727">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="8b12a-728">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="8b12a-728">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="8b12a-729">Cmdlet **Set-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-729">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="8b12a-730">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="8b12a-730">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="8b12a-731">Zum Aktualisieren einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="8b12a-731">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="8b12a-732">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="8b12a-732">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="8b12a-733">Cmdlet **New-AzApiManagementRevision** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-733">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="8b12a-734">Zum Klonen (Kopiertags, Produkte, Vorgänge und Richtlinien) einer vorhandenen Version mithilfe von „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="8b12a-734">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="8b12a-735">Die neue Version übernimmt die „ApiId“ des übergeordneten Elements</span><span class="sxs-lookup"><span data-stu-id="8b12a-735">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="8b12a-736">Zum Bereitstellen einer „ApiRevisionDescription“</span><span class="sxs-lookup"><span data-stu-id="8b12a-736">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="8b12a-737">Zur Außerkraftsetzung der „ServiceUrl“ beim Klonen einer API</span><span class="sxs-lookup"><span data-stu-id="8b12a-737">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="8b12a-738">Cmdlet **New-AzApiManagementIdentityProvider** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-738">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="8b12a-739">Zum Konfigurieren von „AAD“ oder „AADB2C“ mit einer „Authority“</span><span class="sxs-lookup"><span data-stu-id="8b12a-739">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="8b12a-740">Zum Einrichten von „SignupPolicy“, „SigninPolicy“, „ProfileEditingPolicy“ und „PasswordResetPolicy“</span><span class="sxs-lookup"><span data-stu-id="8b12a-740">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="8b12a-741">Cmdlet **New-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-741">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="8b12a-742">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="8b12a-742">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="8b12a-743">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="8b12a-743">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="8b12a-744">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-744">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="8b12a-745">Cmdlet **Set-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-745">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="8b12a-746">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="8b12a-746">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="8b12a-747">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="8b12a-747">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="8b12a-748">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-748">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="8b12a-749">Folgende Cmdlets wurden aktualisiert, um „ResourceId“ als Eingabe zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="8b12a-749">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="8b12a-750">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="8b12a-750">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="8b12a-751">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="8b12a-751">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="8b12a-752">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="8b12a-752">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="8b12a-753">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="8b12a-753">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="8b12a-754">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="8b12a-754">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="8b12a-755">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="8b12a-755">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="8b12a-756">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="8b12a-756">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="8b12a-757">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="8b12a-757">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="8b12a-758">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="8b12a-758">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="8b12a-759">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="8b12a-759">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="8b12a-760">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="8b12a-760">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="8b12a-761">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="8b12a-761">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8b12a-762">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8b12a-762">Az.Automation</span></span>
* <span data-ttu-id="8b12a-763">Get-AzAutomationJobOutputRecord wurde aktualisiert, um JSON- und Textdatensatzwerte zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="8b12a-763">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="8b12a-764">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="8b12a-764">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="8b12a-765">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="8b12a-765">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="8b12a-766">Das Verhalten von Start-AzAutomationDscCompilationJob wurde geändert, um den Auftrag einfach zu starten, anstatt auf dessen Abschluss zu warten</span><span class="sxs-lookup"><span data-stu-id="8b12a-766">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="8b12a-767">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="8b12a-767">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="8b12a-768">Fehlerbehebung für Get-AzAutomationDscNode, wenn die Verwendung von „-Name“ alle Knoten zurückgibt</span><span class="sxs-lookup"><span data-stu-id="8b12a-768">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="8b12a-769">Jetzt wird nur der übereinstimmende Knoten zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="8b12a-769">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8b12a-770">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8b12a-770">Az.Compute</span></span>
* <span data-ttu-id="8b12a-771">Parameter „ProtectFromScaleIn“ und „ProtectFromScaleSetAction“ wurden zum Cmdlet „Update-AzVmssVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-771">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="8b12a-772">Der jetzt festgelegte wimple-Parameter „New-AzVM“ verwendet standardmäßig einen verfügbaren Standort, wenn „East US“ (USA, Osten) nicht unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="8b12a-772">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8b12a-773">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8b12a-773">Az.DataLakeStore</span></span>
* <span data-ttu-id="8b12a-774">Das ADLS-SDK wurde aktualisiert, um „HttpClient“ zu verwenden und Datenebenentests wurden mit dem Azure-Framework integriert</span><span class="sxs-lookup"><span data-stu-id="8b12a-774">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8b12a-775">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8b12a-775">Az.Monitor</span></span>
* <span data-ttu-id="8b12a-776">Fehlerbehebung bei falschen Parameternamen in Hilfebeispielen</span><span class="sxs-lookup"><span data-stu-id="8b12a-776">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8b12a-777">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8b12a-777">Az.Network</span></span>
* <span data-ttu-id="8b12a-778">DisableBgpRoutePropagation-Flag wurde zur Ausgabe der effektiven Routentabelle hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-778">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="8b12a-779">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8b12a-779">Updated cmdlet:</span></span>
        - <span data-ttu-id="8b12a-780">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="8b12a-780">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="8b12a-781">Fehlerbehebung von doppeltem Bindestrich in Dokumentation von New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8b12a-781">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="8b12a-782">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8b12a-782">Az.Resources</span></span>
* <span data-ttu-id="8b12a-783">Neues Cmdlet „Get-AzureRmDenyAssignment“ zum Abrufen von Ablehnungszuweisungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-783">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="8b12a-784">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8b12a-784">Az.Sql</span></span>
* <span data-ttu-id="8b12a-785">„Advanced Threat Protection“-Cmdlets in „Advanced Data Security“ umbenennen und Sicherheitsrisikobewertung standardmäßig aktivieren</span><span class="sxs-lookup"><span data-stu-id="8b12a-785">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="8b12a-786">2.0.0: Mai 2019</span><span class="sxs-lookup"><span data-stu-id="8b12a-786">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8b12a-787">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8b12a-787">Az.Accounts</span></span>
* <span data-ttu-id="8b12a-788">Authentifizierungsbibliothek aktualisiert, um ADFS-Probleme mit der Authentifizierung per Benutzername/Kennwort zu beheben</span><span class="sxs-lookup"><span data-stu-id="8b12a-788">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8b12a-789">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8b12a-789">Az.CognitiveServices</span></span>
* <span data-ttu-id="8b12a-790">Ausschließliche Anzeige des Bing-Haftungsausschlusses für Bing-Suchdienste</span><span class="sxs-lookup"><span data-stu-id="8b12a-790">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="8b12a-791">Fehler behoben, der zu einem Fehler bei der Kontoerstellung führte</span><span class="sxs-lookup"><span data-stu-id="8b12a-791">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8b12a-792">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8b12a-792">Az.Compute</span></span>
* <span data-ttu-id="8b12a-793">Feature für die Näherungsplatzierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="8b12a-793">Proximity placement group feature.</span></span>
    - <span data-ttu-id="8b12a-794">Die folgenden neuen Cmdlets wurden hinzugefügt:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="8b12a-794">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="8b12a-795">Der neue Parameter „ProximityPlacementGroupId“ wurde zu den folgenden Cmdlets hinzugefügt:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="8b12a-795">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="8b12a-796">Der Parameter „StorageAccountType“ wurde zu „New-AzGalleryImageVersion“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8b12a-796">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="8b12a-797">„TargetRegion“ von „New-AzGalleryImageVersion“ kann „StorageAccountType“ enthalten.</span><span class="sxs-lookup"><span data-stu-id="8b12a-797">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="8b12a-798">Switch-Parameter „SkipShutdown“ wurde zu „Stop-AzVM“ und „Stop-AzVmss“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8b12a-798">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="8b12a-799">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="8b12a-799">Breaking changes</span></span>
    - <span data-ttu-id="8b12a-800">„Set-AzVMBootDiagnostics“ in „Set-AzVMBootDiagnostic“ geändert</span><span class="sxs-lookup"><span data-stu-id="8b12a-800">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="8b12a-801">„Export-AzLogAnalyticThrottledRequests“ in „Export-AzLogAnalyticThrottledRequests“ geändert</span><span class="sxs-lookup"><span data-stu-id="8b12a-801">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="8b12a-802">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="8b12a-802">Az.DeploymentManager</span></span>
* <span data-ttu-id="8b12a-803">Erste allgemein verfügbare Version der Azure-Bereitstellungs-Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8b12a-803">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="8b12a-804">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="8b12a-804">Az.Dns</span></span>
* <span data-ttu-id="8b12a-805">Automatische Delegierung des DNS-Namenservers</span><span class="sxs-lookup"><span data-stu-id="8b12a-805">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="8b12a-806">Das Cmdlet zum Erstellen einer DNS-Zone akzeptiert den übergeordneten Zonennamen als zusätzlichen optionalen Parameter.</span><span class="sxs-lookup"><span data-stu-id="8b12a-806">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="8b12a-807">NS-Einträge in der übergeordneten Zone für neu erstellte untergeordnete Zone hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-807">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8b12a-808">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8b12a-808">Az.FrontDoor</span></span>
* <span data-ttu-id="8b12a-809">Erste allgemein verfügbare Version der Azure Frontdoor-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8b12a-809">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="8b12a-810">WAF-Cmdlets so umbenannt, dass sie „Waf“ enthalten</span><span class="sxs-lookup"><span data-stu-id="8b12a-810">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="8b12a-811">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8b12a-811">Az.HDInsight</span></span>
* <span data-ttu-id="8b12a-812">Zwei Cmdlets entfernt:</span><span class="sxs-lookup"><span data-stu-id="8b12a-812">Removed two cmdlets:</span></span>
    - <span data-ttu-id="8b12a-813">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8b12a-813">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="8b12a-814">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8b12a-814">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="8b12a-815">Neues Cmdlet „Set-AzHDInsightGatewayCredential“ hinzugefügt, um „Grant-AzHDInsightHttpServicesAccess“ zu ersetzen</span><span class="sxs-lookup"><span data-stu-id="8b12a-815">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="8b12a-816">Cmdlet „Get-AzHDInsightJobOutput“ aktualisiert, um zwischen Leserrolle und HDInsight-Bedienerrolle zu unterscheiden:</span><span class="sxs-lookup"><span data-stu-id="8b12a-816">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="8b12a-817">Benutzer mit der Rolle „Leser“ müssen den Parameter „DefaultStorageAccountKey“ explizit angeben, andernfalls treten Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="8b12a-817">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="8b12a-818">Benutzer mit der Rolle des HDInsight-Bedieners sind nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="8b12a-818">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8b12a-819">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8b12a-819">Az.Monitor</span></span>
* <span data-ttu-id="8b12a-820">Neue Cmdlets für SQR-API (Scheduled Query Rule, geplante Abfrageregel)</span><span class="sxs-lookup"><span data-stu-id="8b12a-820">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="8b12a-821">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="8b12a-821">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="8b12a-822">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="8b12a-822">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="8b12a-823">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="8b12a-823">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="8b12a-824">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="8b12a-824">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="8b12a-825">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="8b12a-825">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="8b12a-826">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="8b12a-826">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="8b12a-827">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8b12a-827">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8b12a-828">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8b12a-828">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8b12a-829">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8b12a-829">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8b12a-830">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8b12a-830">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8b12a-831">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8b12a-831">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8b12a-832">[Weitere Informationen](/rest/api/monitor/scheduledqueryrules) zur SQR-API</span><span class="sxs-lookup"><span data-stu-id="8b12a-832">[More](/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="8b12a-833">„Az.Monitor.md“ aktualisiert, um Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch) einzuschließen</span><span class="sxs-lookup"><span data-stu-id="8b12a-833">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8b12a-834">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8b12a-834">Az.Network</span></span>
* <span data-ttu-id="8b12a-835">Unterstützung für NAT-Gatewayressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-835">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="8b12a-836">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8b12a-836">New cmdlets</span></span>
        - <span data-ttu-id="8b12a-837">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8b12a-837">New-AzNatGateway</span></span>
        - <span data-ttu-id="8b12a-838">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8b12a-838">Get-AzNatGateway</span></span>
        - <span data-ttu-id="8b12a-839">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8b12a-839">Set-AzNatGateway</span></span>
        - <span data-ttu-id="8b12a-840">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8b12a-840">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="8b12a-841">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8b12a-841">Updated cmdlets</span></span>
        - <span data-ttu-id="8b12a-842">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="8b12a-842">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="8b12a-843">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="8b12a-843">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="8b12a-844">Folgende Befehle für das Feature aktualisiert: Benutzerdefinierte Routen für Brooklyn-Gateway festgelegt/entfernt</span><span class="sxs-lookup"><span data-stu-id="8b12a-844">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="8b12a-845">„New-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="8b12a-845">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="8b12a-846">„Set-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="8b12a-846">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8b12a-847">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8b12a-847">Az.PolicyInsights</span></span>
* <span data-ttu-id="8b12a-848">Unterstützung für die Abfrage von Richtlinienauswertungsdetails</span><span class="sxs-lookup"><span data-stu-id="8b12a-848">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="8b12a-849">Parameter „-Expand“ zu „Get-AzPolicyState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-849">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="8b12a-850">Unterstützung für „-Expand PolicyEvaluationDetails“</span><span class="sxs-lookup"><span data-stu-id="8b12a-850">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8b12a-851">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8b12a-851">Az.RecoveryServices</span></span>
* <span data-ttu-id="8b12a-852">Unterstützung für abonnementübergreifende Azure-zu-Azure-Sitewiederherstellung</span><span class="sxs-lookup"><span data-stu-id="8b12a-852">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="8b12a-853">Markierung anstehender wichtiger Änderungen für Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="8b12a-853">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="8b12a-854">Fehlerbehebung für Azure Site Recovery-Wiederherstellungsplan und -Aktionsplan</span><span class="sxs-lookup"><span data-stu-id="8b12a-854">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="8b12a-855">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Netzwerkzuordnung für Azure zu Azure</span><span class="sxs-lookup"><span data-stu-id="8b12a-855">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="8b12a-856">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Schutzrichtung für Azure zu Azure für verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="8b12a-856">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="8b12a-857">Weitere kleinere Korrekturen</span><span class="sxs-lookup"><span data-stu-id="8b12a-857">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="8b12a-858">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="8b12a-858">Az.Relay</span></span>
* <span data-ttu-id="8b12a-859">Korrektur von Tippfehlern in Kundennachrichten</span><span class="sxs-lookup"><span data-stu-id="8b12a-859">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8b12a-860">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8b12a-860">Az.ServiceBus</span></span>
* <span data-ttu-id="8b12a-861">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-861">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8b12a-862">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8b12a-862">Az.Storage</span></span>
* <span data-ttu-id="8b12a-863">Upgrade auf Speicherclientbibliothek 10.0.1 (Namespace aller Objekte von diesem SDK von „Microsoft.WindowsAzure.Storage. *“ in „Microsoft.Azure.Storage.* “ geändert)</span><span class="sxs-lookup"><span data-stu-id="8b12a-863">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="8b12a-864">Upgrade auf Microsoft.Azure.Management.Storage 11.0.0, um die neue API-Version 2019-04-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="8b12a-864">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="8b12a-865">Art des Standardspeicherkontos bei der Speicherkontoerstellung von „Storage“ in „StorageV2“ geändert</span><span class="sxs-lookup"><span data-stu-id="8b12a-865">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="8b12a-866">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8b12a-866">New-AzStorageAccount</span></span>
* <span data-ttu-id="8b12a-867">Vom Speicherkonto-Cmdlet ausgegebener SKU-Name (Sku.Name) durch Hinzufügen eines Unterstrichs an SKU-Eingabename angepasst (Beispiel: „StandardLRS“ > „Standard_LRS“).</span><span class="sxs-lookup"><span data-stu-id="8b12a-867">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="8b12a-868">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8b12a-868">New-AzStorageAccount</span></span>
    - <span data-ttu-id="8b12a-869">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8b12a-869">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="8b12a-870">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8b12a-870">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8b12a-871">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8b12a-871">Az.Websites</span></span>
* <span data-ttu-id="8b12a-872">Die Eigenschaft „Kind“ wird nun für PSSite-Objekte festgelegt, die von „Get-AzWebApp“ zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8b12a-872">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="8b12a-873">„Get-AzWebApp\*Metrics“ und „Get-AzAppServicePlanMetrics“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-873">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="8b12a-874">1.8.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="8b12a-874">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8b12a-875">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="8b12a-875">Highlights since the last major release</span></span>
* <span data-ttu-id="8b12a-876">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="8b12a-876">General availability of `Az` module</span></span>
* <span data-ttu-id="8b12a-877">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="8b12a-877">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8b12a-878">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="8b12a-878">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8b12a-879">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-879">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8b12a-880">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-880">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8b12a-881">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-881">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8b12a-882">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="8b12a-882">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8b12a-883">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8b12a-883">Az.Accounts</span></span>
* <span data-ttu-id="8b12a-884">„Uninstall-AzureRm“ aktualisiert, um Module unter Mac ordnungsgemäß zu löschen</span><span class="sxs-lookup"><span data-stu-id="8b12a-884">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8b12a-885">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8b12a-885">Az.Batch</span></span>
* <span data-ttu-id="8b12a-886">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="8b12a-886">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8b12a-887">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8b12a-887">Az.Cdn</span></span>
* <span data-ttu-id="8b12a-888">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="8b12a-888">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8b12a-889">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8b12a-889">Az.CognitiveServices</span></span>
* <span data-ttu-id="8b12a-890">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="8b12a-890">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8b12a-891">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8b12a-891">Az.Compute</span></span>
* <span data-ttu-id="8b12a-892">Problem mit der AEM-Installation behoben, wenn die Ressourcen-IDs von Datenträgern Ressourcengruppen in Kleinbuchstaben enthielten</span><span class="sxs-lookup"><span data-stu-id="8b12a-892">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="8b12a-893">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="8b12a-893">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8b12a-894">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-894">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8b12a-895">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8b12a-895">Az.DataFactory</span></span>
* <span data-ttu-id="8b12a-896">„SsisProperties“ hinzugefügt, falls „NodeCount“ für verwaltete Integration Runtime nicht NULL ist</span><span class="sxs-lookup"><span data-stu-id="8b12a-896">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8b12a-897">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8b12a-897">Az.DataLakeStore</span></span>
* <span data-ttu-id="8b12a-898">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="8b12a-898">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8b12a-899">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8b12a-899">Az.EventGrid</span></span>
* <span data-ttu-id="8b12a-900">Hilfetext für Endpunkt aktualisiert, um anzugeben, dass Ressourcen erstellt werden müssen, bevor die Cmdlets zum Erstellen/Aktualisieren von Ereignisabonnements verwendet werden</span><span class="sxs-lookup"><span data-stu-id="8b12a-900">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8b12a-901">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8b12a-901">Az.EventHub</span></span>
* <span data-ttu-id="8b12a-902">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-902">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8b12a-903">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8b12a-903">Az.HDInsight</span></span>
* <span data-ttu-id="8b12a-904">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="8b12a-904">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8b12a-905">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8b12a-905">Az.IotHub</span></span>
* <span data-ttu-id="8b12a-906">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="8b12a-906">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8b12a-907">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8b12a-907">Az.KeyVault</span></span>
* <span data-ttu-id="8b12a-908">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="8b12a-908">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8b12a-909">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-909">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="8b12a-910">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="8b12a-910">Az.MachineLearning</span></span>
* <span data-ttu-id="8b12a-911">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="8b12a-911">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="8b12a-912">Az.Media</span><span class="sxs-lookup"><span data-stu-id="8b12a-912">Az.Media</span></span>
* <span data-ttu-id="8b12a-913">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="8b12a-913">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8b12a-914">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8b12a-914">Az.Monitor</span></span>
  * <span data-ttu-id="8b12a-915">Neue Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch)</span><span class="sxs-lookup"><span data-stu-id="8b12a-915">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="8b12a-916">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="8b12a-916">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="8b12a-917">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="8b12a-917">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="8b12a-918">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8b12a-918">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="8b12a-919">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8b12a-919">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="8b12a-920">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8b12a-920">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="8b12a-921">Monitor SDK auf Version 0.22.0-preview aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-921">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8b12a-922">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8b12a-922">Az.Network</span></span>
* <span data-ttu-id="8b12a-923">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="8b12a-923">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8b12a-924">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-924">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="8b12a-925">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="8b12a-925">Az.NotificationHubs</span></span>
* <span data-ttu-id="8b12a-926">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="8b12a-926">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8b12a-927">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8b12a-927">Az.OperationalInsights</span></span>
* <span data-ttu-id="8b12a-928">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="8b12a-928">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="8b12a-929">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="8b12a-929">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="8b12a-930">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="8b12a-930">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8b12a-931">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8b12a-931">Az.RecoveryServices</span></span>
* <span data-ttu-id="8b12a-932">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="8b12a-932">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8b12a-933">Tabellenformat für SQL auf Azure-VM aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-933">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="8b12a-934">Alternative Methode zum Abrufen des Speicherorts in „AzureFileShare“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-934">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="8b12a-935">„ScheduleRunDays“ in SchedulePolicy-Objekt gemäß Zeitzone aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-935">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8b12a-936">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8b12a-936">Az.RedisCache</span></span>
* <span data-ttu-id="8b12a-937">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="8b12a-937">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8b12a-938">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8b12a-938">Az.Resources</span></span>
* <span data-ttu-id="8b12a-939">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-939">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="8b12a-940">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8b12a-940">Az.Sql</span></span>
* <span data-ttu-id="8b12a-941">Abhängigkeit vom Monitor SDK durch allgemeinen Code ersetzt</span><span class="sxs-lookup"><span data-stu-id="8b12a-941">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="8b12a-942">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="8b12a-942">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8b12a-943">Verbesserter Prozess für Klassifizierung mehrerer Spalten</span><span class="sxs-lookup"><span data-stu-id="8b12a-943">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="8b12a-944">SKU-Eigenschaften (SKU-Name, Familie, Kapazität) in Antwort von „Get-AzSqlServerServiceObjective“ aufgenommen und standardmäßig als Tabelle formatiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-944">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="8b12a-945">Möglichkeit zum Ausführen von „Get-AzSqlServerServiceObjective“ nach Standort, ohne dass bereits ein Server in der Region vorhanden sein muss</span><span class="sxs-lookup"><span data-stu-id="8b12a-945">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="8b12a-946">Unterstützung für Zeitzonenparameter bei der Erstellung einer verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="8b12a-946">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="8b12a-947">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-947">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8b12a-948">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8b12a-948">Az.Websites</span></span>
* <span data-ttu-id="8b12a-949">„Set-AzWebApp“ und „Set-AzWebAppSlot“ korrigiert, sodass die Tags bei der Ausführung nicht entfernt werden</span><span class="sxs-lookup"><span data-stu-id="8b12a-949">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="8b12a-950">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="8b12a-950">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8b12a-951">WebSites SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-951">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="8b12a-952">AdminSiteName-Eigenschaft aus „PSAppServicePlan“ entfernt</span><span class="sxs-lookup"><span data-stu-id="8b12a-952">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="8b12a-953">1.7.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="8b12a-953">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8b12a-954">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="8b12a-954">Highlights since the last major release</span></span>
* <span data-ttu-id="8b12a-955">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="8b12a-955">General availability of `Az` module</span></span>
* <span data-ttu-id="8b12a-956">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="8b12a-956">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8b12a-957">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="8b12a-957">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8b12a-958">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-958">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8b12a-959">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-959">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8b12a-960">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-960">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8b12a-961">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="8b12a-961">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8b12a-962">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8b12a-962">Az.Accounts</span></span>
* <span data-ttu-id="8b12a-963">„Add-AzEnvironment“ und „Set-AzEnvironment“ aktualisiert, um den Parameter „AzureAnalysisServicesEndpointResourceId“ zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="8b12a-963">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8b12a-964">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8b12a-964">Az.AnalysisServices</span></span>
* <span data-ttu-id="8b12a-965">ServiceClient wird in Cmdlets für die Datenebene verwendet, und die ursprüngliche Authentifizierungslogik wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="8b12a-965">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="8b12a-966">„Add-AzureASAccount“ wird als Wrapper von „Connect-AzAccount“ festgelegt, um einen Breaking Change zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="8b12a-966">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8b12a-967">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8b12a-967">Az.Automation</span></span>
* <span data-ttu-id="8b12a-968">Fehler des Cmdlets „Fixed New-AzAutomationSoftwareUpdateConfiguration“ für Einschlüsse behoben.</span><span class="sxs-lookup"><span data-stu-id="8b12a-968">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="8b12a-969">Die Parameter „IncludedKbNumber“ und „IncludedPackageNameMask“ sollten nun funktionieren.</span><span class="sxs-lookup"><span data-stu-id="8b12a-969">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="8b12a-970">Fehlerbehebung für eine dynamische Gruppe der Azure Automation-Updateverwaltung</span><span class="sxs-lookup"><span data-stu-id="8b12a-970">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8b12a-971">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8b12a-971">Az.Compute</span></span>
* <span data-ttu-id="8b12a-972">Parameter „HyperVGeneration“ zu „New-AzDiskConfig“ und „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-972">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="8b12a-973">Zulassen der VM-Erstellung mit einem Katalogimage aus anderen Mandanten</span><span class="sxs-lookup"><span data-stu-id="8b12a-973">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="8b12a-974">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8b12a-974">Az.ContainerInstance</span></span>
* <span data-ttu-id="8b12a-975">Problem im Parameter „-Command“ von „New-AzContainerGroup“ behoben, das dazu führte, dass ein nachgestelltes leeres Argument hinzugefügt wurde</span><span class="sxs-lookup"><span data-stu-id="8b12a-975">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8b12a-976">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8b12a-976">Az.DataFactory</span></span>
* <span data-ttu-id="8b12a-977">Version des ADF .NET SDK auf 3.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-977">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="8b12a-978">Cmdlet „Set-AzDataFactoryV2“ mit zusätzlichen Parametern für RepoConfiguration-Einstellungen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-978">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8b12a-979">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8b12a-979">Az.Resources</span></span>
* <span data-ttu-id="8b12a-980">Verarbeitung von Anbietern für „Get-AzResource“ bei der Angabe der Parameter „-ResourceId“ oder „-ResourceGroupName“, „-Name“ und „-ResourceType“ verbessert</span><span class="sxs-lookup"><span data-stu-id="8b12a-980">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="8b12a-981">Fehlerbehandlung für „Test-AzDeployment“ und „Test-AzResourceGroupDeployment“ verbessert</span><span class="sxs-lookup"><span data-stu-id="8b12a-981">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="8b12a-982">Behandlung von außerhalb der Bereitstellungsüberprüfung aufgetretenen Fehlern und stattdessen Aufnahme in die Ausgabe des Befehls</span><span class="sxs-lookup"><span data-stu-id="8b12a-982">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="8b12a-983">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="8b12a-983">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="8b12a-984">Switch-Parameter „-IgnoreDynamicParameters“ zu Bereitstellungs-Cmdlets hinzugefügt, um Aufforderung in Skript- und Auftragsszenarien zu überspringen</span><span class="sxs-lookup"><span data-stu-id="8b12a-984">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="8b12a-985">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="8b12a-985">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="8b12a-986">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8b12a-986">Az.Sql</span></span>
* <span data-ttu-id="8b12a-987">Unterstützung für Klassifizierung von Datenbankdaten</span><span class="sxs-lookup"><span data-stu-id="8b12a-987">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8b12a-988">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8b12a-988">Az.Storage</span></span>
* <span data-ttu-id="8b12a-989">Melden eines ausführlichen Fehlers beim Erstellen des Storage-Kontexts mit dem Parameter „-UseConnectedAccount“, aber ohne Azure-Anmeldekonto</span><span class="sxs-lookup"><span data-stu-id="8b12a-989">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="8b12a-990">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8b12a-990">New-AzStorageContext</span></span>
* <span data-ttu-id="8b12a-991">Unterstützung für das Verwalten von Blobdiensteigenschaften eines bestimmten Storage-Kontos mit einer API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="8b12a-991">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="8b12a-992">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="8b12a-992">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="8b12a-993">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="8b12a-993">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="8b12a-994">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8b12a-994">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="8b12a-995">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8b12a-995">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="8b12a-996">Unterstützung von „-AsJob“ für Cmdlets für den Upload und Download von Blobs und Dateien</span><span class="sxs-lookup"><span data-stu-id="8b12a-996">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="8b12a-997">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8b12a-997">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="8b12a-998">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8b12a-998">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="8b12a-999">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8b12a-999">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="8b12a-1000">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8b12a-1000">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="8b12a-1001">1.6.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="8b12a-1001">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8b12a-1002">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="8b12a-1002">Highlights since the last major release</span></span>
* <span data-ttu-id="8b12a-1003">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="8b12a-1003">General availability of `Az` module</span></span>
* <span data-ttu-id="8b12a-1004">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1004">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8b12a-1005">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1005">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8b12a-1006">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1006">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8b12a-1007">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1007">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8b12a-1008">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1008">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8b12a-1009">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="8b12a-1009">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8b12a-1010">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8b12a-1010">Az.Automation</span></span>
* <span data-ttu-id="8b12a-1011">Änderung an der Azure Automation-Updateverwaltung, um die folgenden neuen Features zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="8b12a-1011">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="8b12a-1012">Dynamische Gruppierung</span><span class="sxs-lookup"><span data-stu-id="8b12a-1012">Dynamic grouping</span></span>
    * <span data-ttu-id="8b12a-1013">Pre-/Post-Skripts</span><span class="sxs-lookup"><span data-stu-id="8b12a-1013">Pre-Post script</span></span>
    * <span data-ttu-id="8b12a-1014">Neustarteinstellung</span><span class="sxs-lookup"><span data-stu-id="8b12a-1014">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8b12a-1015">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8b12a-1015">Az.Compute</span></span>
* <span data-ttu-id="8b12a-1016">Problem mit der Pfadauflösung in „Get-AzVmBootDiagnosticsData“ behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-1016">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="8b12a-1017">Computeclientbibliothek auf 25.0.0. aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1017">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8b12a-1018">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8b12a-1018">Az.KeyVault</span></span>
* <span data-ttu-id="8b12a-1019">Unterstützung für Platzhalterzeichen zu KeyVault-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1019">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8b12a-1020">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8b12a-1020">Az.Network</span></span>
* <span data-ttu-id="8b12a-1021">Threat Intelligence-Unterstützung für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1021">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="8b12a-1022">Ressource der obersten Ebene für Application Gateway-Firewallrichtlinie und benutzerdefinierte Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1022">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8b12a-1023">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8b12a-1023">Az.RecoveryServices</span></span>
* <span data-ttu-id="8b12a-1024">SnapshotRetentionInDays in Azure-VM-Richtlinie hinzugefügt, um sofortigen Wiederherstellungspunkt zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="8b12a-1024">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="8b12a-1025">Pipe-Unterstützung für das Aufheben der Registrierung eines Containers hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1025">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="8b12a-1026">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8b12a-1026">Az.Resources</span></span>
* <span data-ttu-id="8b12a-1027">Unterstützung für Platzhalterzeichen für Get-AzResource und Get-AzResourceGroup aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1027">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="8b12a-1028">Anmeldeinformationen aktualisiert, die beim Senden generischer Aufrufe an ARM verwendet werden</span><span class="sxs-lookup"><span data-stu-id="8b12a-1028">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="8b12a-1029">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8b12a-1029">Az.Sql</span></span>
* <span data-ttu-id="8b12a-1030">Der Cmdlet-Parameter der Bedrohungserkennung (ExcludeDetectionType) wurde von „DetectionType“ in „string[]“ geändert, um ihn zukunftssicher zu machen, wenn neue DetectionTypes-Elemente hinzugefügt werden, und um AutoVervollständigen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1030">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8b12a-1031">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8b12a-1031">Az.Storage</span></span>
* <span data-ttu-id="8b12a-1032">Unterstützung von Get-/Set-/Remove-Verwaltungsrichtlinien für Speicherkonto hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1032">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="8b12a-1033">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8b12a-1033">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8b12a-1034">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8b12a-1034">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8b12a-1035">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8b12a-1035">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8b12a-1036">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="8b12a-1036">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="8b12a-1037">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="8b12a-1037">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="8b12a-1038">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="8b12a-1038">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8b12a-1039">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8b12a-1039">Az.Websites</span></span>
* <span data-ttu-id="8b12a-1040">ARM-Vorlagenfehler behoben, der zu einem Problem beim Klonen aller Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ führte</span><span class="sxs-lookup"><span data-stu-id="8b12a-1040">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="8b12a-1041">1.5.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="8b12a-1041">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8b12a-1042">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8b12a-1042">Az.Accounts</span></span>
* <span data-ttu-id="8b12a-1043">Der Befehl „Register-AzModule“ wurde hinzugefügt, um von AutoRest generierte Cmdlets zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1043">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="8b12a-1044">Beispiele für „Connect-AzAccount“ wurden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1044">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8b12a-1045">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8b12a-1045">Az.Automation</span></span>
* <span data-ttu-id="8b12a-1046">Problem behoben, das beim Abrufen bestimmter monatlicher Zeitpläne in verschiedenen Azure Automation-Cmdlets auftrat</span><span class="sxs-lookup"><span data-stu-id="8b12a-1046">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="8b12a-1047">„Get-AzAutomationDscNode“ wurde korrigiert, da nur die 20 obersten Knoten zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1047">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="8b12a-1048">Jetzt werden alle Knoten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1048">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8b12a-1049">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8b12a-1049">Az.Cdn</span></span>
* <span data-ttu-id="8b12a-1050">Neue Powershell-Cmdlets zum Aktivieren/Deaktivieren von HTTPS für benutzerdefinierte Domänen hinzugefügt und alte Cmdlets außer Betrieb genommen</span><span class="sxs-lookup"><span data-stu-id="8b12a-1050">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8b12a-1051">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8b12a-1051">Az.Compute</span></span>
* <span data-ttu-id="8b12a-1052">Unterstützung für Platzhalterzeichen zu Get-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1052">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8b12a-1053">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8b12a-1053">Az.DataFactory</span></span>
* <span data-ttu-id="8b12a-1054">Version des ADF .NET SDK auf 3.0.1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1054">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8b12a-1055">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8b12a-1055">Az.LogicApp</span></span>
* <span data-ttu-id="8b12a-1056">„ListWorkflows“ wurde korrigiert, da nur die erste Seite mit Ergebnissen abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1056">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8b12a-1057">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8b12a-1057">Az.Network</span></span>
* <span data-ttu-id="8b12a-1058">Unterstützung für Platzhalterzeichen zu Network-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1058">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8b12a-1059">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8b12a-1059">Az.RecoveryServices</span></span>
* <span data-ttu-id="8b12a-1060">SQL Server jetzt in Azure-VM-Support enthalten</span><span class="sxs-lookup"><span data-stu-id="8b12a-1060">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="8b12a-1061">SDK-Update</span><span class="sxs-lookup"><span data-stu-id="8b12a-1061">SDK Update</span></span>
* <span data-ttu-id="8b12a-1062">VMappContainer-Überprüfung in „Get-ProtectableItem“ entfernt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1062">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="8b12a-1063">„Name“ und „ServerName“ als Parameter für „Get-ProtectableItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1063">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="8b12a-1064">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8b12a-1064">Az.Resources</span></span>
* <span data-ttu-id="8b12a-1065">Parameter `-TemplateObject` zu Bereitstellungs-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1065">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="8b12a-1066">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="8b12a-1066">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="8b12a-1067">Problem beim Piping des Ergebnisses von `Get-AzResource` an `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-1067">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="8b12a-1068">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="8b12a-1068">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="8b12a-1069">Problem mit JSON-Datentypänderung beim Ausführen von `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-1069">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="8b12a-1070">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="8b12a-1070">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="8b12a-1071">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8b12a-1071">Az.Sql</span></span>
* <span data-ttu-id="8b12a-1072">„AuditingEndpointsCommunicator“ wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1072">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="8b12a-1073">Das Verhalten eines Grenzfalls beim Erstellen neuer Diagnoseeinstellungen wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1073">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8b12a-1074">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8b12a-1074">Az.Storage</span></span>
* <span data-ttu-id="8b12a-1075">Unterstützung von „Kind BlockBlobStorage“ beim Erstellen eines Speicherkontos: New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8b12a-1075">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="8b12a-1076">1.4.0 – Februar 2019</span><span class="sxs-lookup"><span data-stu-id="8b12a-1076">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="8b12a-1077">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8b12a-1077">Az.AnalysisServices</span></span>
* <span data-ttu-id="8b12a-1078">Cmdlet „AddAzureASAccount“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1078">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8b12a-1079">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8b12a-1079">Az.Automation</span></span>
* <span data-ttu-id="8b12a-1080">Hilfe für „Import-AzAutomationDscNodeConfiguration“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1080">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="8b12a-1081">Überprüfung des Konfigurationsnamens zu Cmdlet „Import-AzAutomationDscConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1081">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="8b12a-1082">Fehlerbehandlung für Cmdlet „Import-AzAutomationDscConfiguration“ verbessert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1082">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8b12a-1083">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8b12a-1083">Az.CognitiveServices</span></span>
* <span data-ttu-id="8b12a-1084">„CustomSubdomainName“ als neuer optionaler Parameter für Cmdlet „New-AzCognitiveServicesAccount“ hinzugefügt, das zum Angeben der Unterdomäne für die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1084">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8b12a-1085">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8b12a-1085">Az.Compute</span></span>
* <span data-ttu-id="8b12a-1086">Problem mit ID-Parametersätzen behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-1086">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="8b12a-1087">„Get-AzVMExtension“ aktualisiert, sodass alle installierten Erweiterungen aufgelistet werden, wenn der Name-Parameter nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="8b12a-1087">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="8b12a-1088">Parameter „Tag“ und „ResourceId“ zum Cmdlet „Update-AzImage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1088">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="8b12a-1089">„Get-AzVmssVM“ ohne Instanz-ID und mit „InstanceView“ können virtuelle VMSS-Computer mit Instanzansicht auflisten.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1089">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8b12a-1090">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8b12a-1090">Az.DataLakeStore</span></span>
* <span data-ttu-id="8b12a-1091">Cmdlets zum Auflisten und Wiederherstellen gelöschter ADL-Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1091">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8b12a-1092">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8b12a-1092">Az.EventHub</span></span>
* <span data-ttu-id="8b12a-1093">Neue boolesche Eigenschaft „SkipEmptyArchives“ zum Überspringen leerer Archive in Klasse „CaptureDescription“ von EventHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1093">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8b12a-1094">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8b12a-1094">Az.KeyVault</span></span>
* <span data-ttu-id="8b12a-1095">Kennzeichnung in „Set-AzKeyVaultSecret“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1095">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8b12a-1096">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8b12a-1096">Az.LogicApp</span></span>
* <span data-ttu-id="8b12a-1097">SKU „Basic“ für Integrationskonten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1097">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="8b12a-1098">XSLT 2.0, XSLT 3.0 und Liquid-Zuordnungstypen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1098">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="8b12a-1099">Neue Cmdlets für Integrationskonto-Assemblys</span><span class="sxs-lookup"><span data-stu-id="8b12a-1099">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="8b12a-1100">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8b12a-1100">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8b12a-1101">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8b12a-1101">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8b12a-1102">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8b12a-1102">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8b12a-1103">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8b12a-1103">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="8b12a-1104">Neue Cmdlets für Integrationskonto-Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="8b12a-1104">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="8b12a-1105">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b12a-1105">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8b12a-1106">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b12a-1106">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8b12a-1107">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b12a-1107">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8b12a-1108">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b12a-1108">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="8b12a-1109">Logik-App-SDK auf Version 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1109">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8b12a-1110">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8b12a-1110">Az.Monitor</span></span>
* <span data-ttu-id="8b12a-1111">Hilfe für „Get-AzMetric“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1111">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8b12a-1112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8b12a-1112">Az.Network</span></span>
* <span data-ttu-id="8b12a-1113">Hilfebeispiel für „Add-AzApplicationGatewayCustomError“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1113">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8b12a-1114">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8b12a-1114">Az.OperationalInsights</span></span>
* <span data-ttu-id="8b12a-1115">Zusätzliche Unterstützung für Datenquelle von „New-ApplicationInsights“ und „Get-ApplicationInsights“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1115">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="8b12a-1116">Neue Art von „ApplicationInsights“ zum Abrufen von bestimmten und von allen ApplicationInsights-Datenquellen für einen Workspace hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1116">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="8b12a-1117">Cmdlet „New-AzOperationalInsightsApplicationInsightsDataSource“ zum Erstellen einer Datenquelle anhand des angegebenen Ressourcenparameters für „Application-Insights“ hinzugefügt: „subscriptionId“, „resourceGroupName“ und „name“.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1117">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8b12a-1118">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8b12a-1118">Az.Resources</span></span>
* <span data-ttu-id="8b12a-1119">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="8b12a-1119">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="8b12a-1120">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="8b12a-1120">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="8b12a-1121">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="8b12a-1121">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="8b12a-1122">Fehler korrigiert, der die wiederholte Erstellung von „KeyCredentials“ verhindert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1122">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="8b12a-1123">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8b12a-1123">Az.Sql</span></span>
* <span data-ttu-id="8b12a-1124">Unterstützung für SQL DB Hyperscale-Tarif hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1124">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="8b12a-1125">Fehler korrigiert, aufgrund dessen die Wiederherstellung wegen der Festlegung unnötiger Eigenschaften in der Wiederherstellungsanforderung fehlschlagen konnte</span><span class="sxs-lookup"><span data-stu-id="8b12a-1125">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8b12a-1126">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8b12a-1126">Az.Websites</span></span>
* <span data-ttu-id="8b12a-1127">Beispiel in „Get-AzWebAppSlotMetrics“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1127">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="8b12a-1128">1.3.0: Februar 2019</span><span class="sxs-lookup"><span data-stu-id="8b12a-1128">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8b12a-1129">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8b12a-1129">Az.Accounts</span></span>
* <span data-ttu-id="8b12a-1130">Update auf die aktuelle Version von ClientRuntime durchgeführt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1130">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8b12a-1131">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8b12a-1131">Az.AnalysisServices</span></span>
<span data-ttu-id="8b12a-1132">Allgemeine Verfügbarkeit für Az.AnalysisServices-Modul</span><span class="sxs-lookup"><span data-stu-id="8b12a-1132">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8b12a-1133">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8b12a-1133">Az.Compute</span></span>
* <span data-ttu-id="8b12a-1134">AEM-Erweiterung: Unterstützung für UltraSSD und P60-, P70- und P80-Datenträger hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1134">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="8b12a-1135">Hilfebeschreibung für „Set-AzVMBootDiagnostics“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1135">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="8b12a-1136">Hilfebeschreibung und Beispiel für „Update-AzImage“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1136">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8b12a-1137">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8b12a-1137">Az.RecoveryServices</span></span>
<span data-ttu-id="8b12a-1138">Allgemeine Verfügbarkeit für Az.RecoveryServices-Modul.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1138">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8b12a-1139">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8b12a-1139">Az.Resources</span></span>
* <span data-ttu-id="8b12a-1140">Kennzeichnung für Ressourcengruppen korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1140">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="8b12a-1141">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="8b12a-1141">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="8b12a-1142">Problem behoben, bei dem „-ErrorAction“ von `Get-AzureRmRoleAssignment` nicht berücksichtigt wird</span><span class="sxs-lookup"><span data-stu-id="8b12a-1142">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="8b12a-1143">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="8b12a-1143">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="8b12a-1144">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8b12a-1144">Az.Sql</span></span>
* <span data-ttu-id="8b12a-1145">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1145">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="8b12a-1146">Problem behoben, bei dem eine fehlende Anmeldung am Azure-Konto bei der Ausführung von SQL-Cmdlets zu einer nullref-Ausnahme führt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1146">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="8b12a-1147">nullref-Ausnahme in Get-AzSqlCapability korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1147">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="8b12a-1148">1.2.1: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="8b12a-1148">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8b12a-1149">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8b12a-1149">Az.Accounts</span></span>
* <span data-ttu-id="8b12a-1150">Release mit richtiger Version der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="8b12a-1150">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8b12a-1151">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8b12a-1151">Az.AnalysisServices</span></span>
* <span data-ttu-id="8b12a-1152">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="8b12a-1152">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8b12a-1153">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8b12a-1153">Az.RecoveryServices</span></span>
* <span data-ttu-id="8b12a-1154">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="8b12a-1154">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="8b12a-1155">1.2.0: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="8b12a-1155">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8b12a-1156">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8b12a-1156">Az.Accounts</span></span>
* <span data-ttu-id="8b12a-1157">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1157">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8b12a-1158">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1158">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8b12a-1159">Warnmeldung in PS Core für „Uninstall-AzureRm“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1159">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="8b12a-1160">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8b12a-1160">Az.Aks</span></span>
* <span data-ttu-id="8b12a-1161">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1161">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8b12a-1162">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8b12a-1162">Az.Automation</span></span>
* <span data-ttu-id="8b12a-1163">Unterstützung für Python 2-Runbooks hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1163">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="8b12a-1164">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1164">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8b12a-1165">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8b12a-1165">Az.Cdn</span></span>
* <span data-ttu-id="8b12a-1166">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1166">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8b12a-1167">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8b12a-1167">Az.Compute</span></span>
* <span data-ttu-id="8b12a-1168">Cmdlet „Invoke-AzVMReimage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1168">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="8b12a-1169">Parameter „TempDisk“ zu „Set-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1169">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="8b12a-1170">Warnmeldung von „New-AzVM“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1170">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="8b12a-1171">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8b12a-1171">Az.ContainerRegistry</span></span>
* <span data-ttu-id="8b12a-1172">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1172">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8b12a-1173">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8b12a-1173">Az.DataFactory</span></span>
* <span data-ttu-id="8b12a-1174">Version des ADF .NET SDK auf 3.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1174">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8b12a-1175">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8b12a-1175">Az.DataLakeStore</span></span>
* <span data-ttu-id="8b12a-1176">Problem mit ADLS-Endpunkt bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-1176">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="8b12a-1177">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="8b12a-1177">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="8b12a-1178">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1178">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8b12a-1179">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8b12a-1179">Az.IotHub</span></span>
* <span data-ttu-id="8b12a-1180">Codierungsformat zu Cmdlet „Add-IotHubRoutingEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1180">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8b12a-1181">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8b12a-1181">Az.KeyVault</span></span>
* <span data-ttu-id="8b12a-1182">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1182">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8b12a-1183">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8b12a-1183">Az.Network</span></span>
* <span data-ttu-id="8b12a-1184">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1184">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="8b12a-1185">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8b12a-1185">Az.Resources</span></span>
* <span data-ttu-id="8b12a-1186">Fehlerhafte Beispiele in Referenzdokumentation zu „New-AzADAppCredential“ und „New-AzADSpCredential“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1186">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="8b12a-1187">Problem behoben, bei dem der Pfad für den Parameter „-TemplateFile“ nicht aufgelöst wurde, bevor Cmdlets für die Bereitstellung von Ressourcengruppen ausgeführt wurden</span><span class="sxs-lookup"><span data-stu-id="8b12a-1187">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="8b12a-1188">Az.Resources: Richtige Dokumentation für Standardwert von „New-AzureRmPolicyDefinition -Mode“ bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1188">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="8b12a-1189">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="8b12a-1189">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="8b12a-1190">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="8b12a-1190">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="8b12a-1191">Formatierungsproblem für Objekt „PSResourceGroupDeployment“ behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-1191">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="8b12a-1192">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="8b12a-1192">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8b12a-1193">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8b12a-1193">Az.ServiceFabric</span></span>
* <span data-ttu-id="8b12a-1194">Rollback beim Hinzufügen eines Zertifikats zum VMSS-Modell, Auslösung einer Ausnahme. Fehlerbehebung: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="8b12a-1194">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="8b12a-1195">Einige Fehlermeldungen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1195">Fix some error messages.</span></span>
* <span data-ttu-id="8b12a-1196">Fehler bei Clustererstellung mit ARM-Standardvorlage für „New-AzServiceFabriCluster“ behoben, bei dem die Migration zu Az nicht funktioniert hat.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1196">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="8b12a-1197">Fehler behoben beim Hinzufügen eines Cluster-/Anwendungszertifikats ausschließlich zu VM Scale Sets, die zum Cluster gehören, indem die Cluster-ID in der Erweiterung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1197">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8b12a-1198">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8b12a-1198">Az.SignalR</span></span>
* <span data-ttu-id="8b12a-1199">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1199">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="8b12a-1200">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8b12a-1200">Az.Sql</span></span>
* <span data-ttu-id="8b12a-1201">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1201">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8b12a-1202">Parameterbeschreibung für den Parameter „LicenseType“ mit möglichen Werten aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1202">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="8b12a-1203">Fehler behoben, bei dem die Aktualisierung der Identität der verwalteten Instanz nicht funktioniert hat, wenn es sich um die einzige aktualisierte Eigenschaft gehandelt hat</span><span class="sxs-lookup"><span data-stu-id="8b12a-1203">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="8b12a-1204">Unterstützung für die benutzerdefinierte Sortierung auf verwalteter Instanz</span><span class="sxs-lookup"><span data-stu-id="8b12a-1204">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8b12a-1205">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8b12a-1205">Az.Storage</span></span>
* <span data-ttu-id="8b12a-1206">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1206">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8b12a-1207">Ausführliche Fehlermeldung beim Abrufen/Festlegen der klassischen Protokollierung bzw. Metriken für Storage Premium-Konto, da für das Storage Premium-Konto die klassische Protokollierung bzw. Metriken nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1207">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="8b12a-1208">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="8b12a-1208">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="8b12a-1209">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="8b12a-1209">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="8b12a-1210">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8b12a-1210">Az.TrafficManager</span></span>
* <span data-ttu-id="8b12a-1211">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1211">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8b12a-1212">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8b12a-1212">Az.Websites</span></span>
* <span data-ttu-id="8b12a-1213">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1213">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8b12a-1214">„New-AzWebAppSSLBinding“ korrigiert, damit das Zertifikat in die richtige Ressourcengruppe bzw. an den richtigen Speicherort hochgeladen wird, wenn die App in einer ASE gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1214">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="8b12a-1215">„New-AzWebAppSSLBinding“ korrigiert, damit die Tags beim Binden eines SSL-Zertifikats an eine App nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1215">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="8b12a-1216">1.1.0 – Januar 2019</span><span class="sxs-lookup"><span data-stu-id="8b12a-1216">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8b12a-1217">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8b12a-1217">Az.Accounts</span></span>
* <span data-ttu-id="8b12a-1218">Bereich „Local“ zu „Enable-AzureRmAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1218">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8b12a-1219">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8b12a-1219">Az.Compute</span></span>
* <span data-ttu-id="8b12a-1220">Name ist jetzt optional im ID-Parametersatz für „Restart/Start/Stop/Remove/Set-AzVM“ und „Save-AzVMImage“</span><span class="sxs-lookup"><span data-stu-id="8b12a-1220">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="8b12a-1221">Beschreibung der ID in Hilfedateien aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1221">Updated the description of ID in help files</span></span>
* <span data-ttu-id="8b12a-1222">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-1222">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8b12a-1223">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8b12a-1223">Az.DataLakeStore</span></span>
* <span data-ttu-id="8b12a-1224">Aktualisierung der SDK-Version der Datenebene auf 1.1.14 für SDK-Fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1224">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="8b12a-1225">Behandlung von negativen acesstime- and modificationtime-Werten für „getfilestatus“ und „liststatus“ korrigiert, asynchrones Abbruchtoken korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1225">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8b12a-1226">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8b12a-1226">Az.EventGrid</span></span>
* <span data-ttu-id="8b12a-1227">Zur Verwendung der API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1227">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="8b12a-1228">Aktualisierung der folgenden Cmdlets zur Unterstützung des neuen Szenarios in der API-Version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="8b12a-1228">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="8b12a-1229">New-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="8b12a-1229">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="8b12a-1230">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="8b12a-1230">Event Time-To-Live,</span></span>
        - <span data-ttu-id="8b12a-1231">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="8b12a-1231">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="8b12a-1232">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="8b12a-1232">Dead letter endpoint.</span></span>
    - <span data-ttu-id="8b12a-1233">Update-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="8b12a-1233">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="8b12a-1234">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="8b12a-1234">Event Time-To-Live,</span></span>
        - <span data-ttu-id="8b12a-1235">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="8b12a-1235">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="8b12a-1236">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="8b12a-1236">Dead letter endpoint.</span></span>
* <span data-ttu-id="8b12a-1237">Neue Enumerationswerte („storageQueue“ und „hybridConnection“) für die EndpointType-Option in den Cmdlets „New-AzureRmEventGridSubscription“ und „Update-AzureRmEventGridSubscription“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1237">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="8b12a-1238">Anzeige einer Warnmeldung, wenn das Erstellen oder Aktualisieren des Ereignisabonnements voraussichtlich eine manuelle Aktion des Benutzers zur Folge hat</span><span class="sxs-lookup"><span data-stu-id="8b12a-1238">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8b12a-1239">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8b12a-1239">Az.IotHub</span></span>
* <span data-ttu-id="8b12a-1240">Auf die aktuelle Version des Iot Hub SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1240">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8b12a-1241">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8b12a-1241">Az.LogicApp</span></span>
* <span data-ttu-id="8b12a-1242">„Get-AzLogicApp“ listet alle Apps ohne angegebenen Namen auf</span><span class="sxs-lookup"><span data-stu-id="8b12a-1242">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="8b12a-1243">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8b12a-1243">Az.Resources</span></span>
* <span data-ttu-id="8b12a-1244">Problem mit dem Parametersatz bei Angabe der Parameter „-ODataQuery“ und „-ResourceId“ für „Get-AzResource“ behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-1244">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="8b12a-1245">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="8b12a-1245">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="8b12a-1246">Behandlung des Parameters „-Custom“ in „New/Set-AzPolicyDefinition“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1246">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="8b12a-1247">Tippfehler in der Dokumentation für „New-AzDeployment“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1247">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="8b12a-1248">Parameter „-MailNickname“ als obligatorisch festgelegt für „New-AzADUser“</span><span class="sxs-lookup"><span data-stu-id="8b12a-1248">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="8b12a-1249">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="8b12a-1249">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8b12a-1250">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8b12a-1250">Az.SignalR</span></span>
* <span data-ttu-id="8b12a-1251">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-1251">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="8b12a-1252">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8b12a-1252">Az.Sql</span></span>
* <span data-ttu-id="8b12a-1253">Abhängigkeit des Speicherverwaltungsclients zur allgemeinen SDK-Implementierung konvertiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1253">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8b12a-1254">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8b12a-1254">Az.Storage</span></span>
* <span data-ttu-id="8b12a-1255">Festlegung des „StorageAccountName“ des Speicherkontexts als tatsächlichen Namen des Speicherkontos, wenn dieser mit „SAS-Token“, „OAuth“ oder „Anonym“ erstellt wird</span><span class="sxs-lookup"><span data-stu-id="8b12a-1255">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="8b12a-1256">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8b12a-1256">New-AzStorageContext</span></span>
* <span data-ttu-id="8b12a-1257">Erstellen von SAS-Token des Blob-Momentaufnahmeobjekts mit dem Parameter „-FullUri“, Festlegung des zurückgegebenen URI als Momentaufnahme-URI</span><span class="sxs-lookup"><span data-stu-id="8b12a-1257">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="8b12a-1258">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="8b12a-1258">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8b12a-1259">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8b12a-1259">Az.Websites</span></span>
* <span data-ttu-id="8b12a-1260">Fehler bei der Datumsanalyse in „Get-AzDeletedWebApp“ behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-1260">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="8b12a-1261">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-1261">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="8b12a-1262">1.0.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="8b12a-1262">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="8b12a-1263">Allgemein</span><span class="sxs-lookup"><span data-stu-id="8b12a-1263">General</span></span>

- <span data-ttu-id="8b12a-1264">Allgemeine Verfügbarkeit des Az-Moduls</span><span class="sxs-lookup"><span data-stu-id="8b12a-1264">General Availability of Az Module</span></span>
- <span data-ttu-id="8b12a-1265">Onlinehilfe für jedes Modul</span><span class="sxs-lookup"><span data-stu-id="8b12a-1265">Online help for each module</span></span>
- <span data-ttu-id="8b12a-1266">Ausführlichere Informationen und eine Roadmap finden Sie auf der [Seite mit der Ankündigung zu Az](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="8b12a-1266">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="8b12a-1267">Informationen zur Migration aus AzureRM finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="8b12a-1267">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="8b12a-1268">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8b12a-1268">Az.Accounts</span></span>
- <span data-ttu-id="8b12a-1269">Geändert von Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8b12a-1269">Changed from Az.Profile</span></span>
- <span data-ttu-id="8b12a-1270">Feste Tabellenformate für Profil- und Kontexttypen</span><span class="sxs-lookup"><span data-stu-id="8b12a-1270">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="8b12a-1271">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8b12a-1271">Az.ApiManagement</span></span>
- <span data-ttu-id="8b12a-1272">Korrekturen für #7002</span><span class="sxs-lookup"><span data-stu-id="8b12a-1272">Fixes for #7002</span></span>
- <span data-ttu-id="8b12a-1273">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="8b12a-1273">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="8b12a-1274">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8b12a-1274">Az.Batch</span></span>
- <span data-ttu-id="8b12a-1275">Möglichkeit zum Anzeigen der ausgeführten Version des Azure Batch-Knoten-Agents auf den VMs eines Pools mit der neuen `NodeAgentInformation`-Eigenschaft für `PSComputeNode` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1275">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="8b12a-1276">Der `Caching`-Standardwert für `PSDataDisk` lautet jetzt nicht mehr `None`, sondern `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1276">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="8b12a-1277">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="8b12a-1277">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="8b12a-1278">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="8b12a-1278">Az.Billing</span></span>
- <span data-ttu-id="8b12a-1279">Kombination von Billing-, Consumption- und UsageAggregates-Cmdlets. Ausführliche Informationen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="8b12a-1279">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="8b12a-1280">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="8b12a-1280">Az.CognitivServices</span></span>
- <span data-ttu-id="8b12a-1281">Vervollständigungen für SkuName und Typem für den Vorgang New-AzureRmCognitiveServicesAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1281">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="8b12a-1282">GetSkusWithAccountParamSetName-Parametersatz aus Get-AzCognitiveServicesAccountSkus entfernt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1282">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="8b12a-1283">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8b12a-1283">Az.ContainerInstance</span></span>
- <span data-ttu-id="8b12a-1284">ManagedIdentity-Unterstützung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1284">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="8b12a-1285">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="8b12a-1285">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="8b12a-1286">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="8b12a-1286">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="8b12a-1287">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8b12a-1287">Az.DataLakeStore</span></span>
- <span data-ttu-id="8b12a-1288">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="8b12a-1288">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="8b12a-1289">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8b12a-1289">Az.Monitor</span></span>
- <span data-ttu-id="8b12a-1290">Az.Insights in Az.Monitor umbenannt und weitere weniger wichtige grundlegende Änderungen durchgeführt. Informationen hierzu finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="8b12a-1290">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="8b12a-1291">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8b12a-1291">Az.KeyVault</span></span>
- <span data-ttu-id="8b12a-1292">Veraltete PurgeDisabled-Eigenschaft aus Ausgabetypen entfernt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1292">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="8b12a-1293">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="8b12a-1293">Az.MachineLearning</span></span>
- <span data-ttu-id="8b12a-1294">Cmdlets des Az.MachineLearningCompute-Moduls eingebunden</span><span class="sxs-lookup"><span data-stu-id="8b12a-1294">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="8b12a-1295">Az.Media</span><span class="sxs-lookup"><span data-stu-id="8b12a-1295">Az.Media</span></span>
- <span data-ttu-id="8b12a-1296">Veralteten -Tags-Alias aus New-AzMediaService entfernt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1296">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="8b12a-1297">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8b12a-1297">Az.Network</span></span>
<span data-ttu-id="8b12a-1298">Unterstützung für das Konfigurieren von RewriteRuleSets im Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1298">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="8b12a-1299">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="8b12a-1299">New cmdlets added:</span></span>
        - <span data-ttu-id="8b12a-1300">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8b12a-1300">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8b12a-1301">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8b12a-1301">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8b12a-1302">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8b12a-1302">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8b12a-1303">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8b12a-1303">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8b12a-1304">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8b12a-1304">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8b12a-1305">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="8b12a-1305">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="8b12a-1306">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="8b12a-1306">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="8b12a-1307">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b12a-1307">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="8b12a-1308">Cmdlets mit optionalem Parameter -RewriteRuleSet aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1308">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="8b12a-1309">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8b12a-1309">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="8b12a-1310">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8b12a-1310">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="8b12a-1311">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8b12a-1311">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="8b12a-1312">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8b12a-1312">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="8b12a-1313">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8b12a-1313">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="8b12a-1314">New-AzureRmApplicationGatewayUrlPathMapConfig: KeyVault-Unterstützung mithilfe von Identität zum Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1314">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="8b12a-1315">Cmdlets mit optionalem Parameter aktualisiert: -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8b12a-1315">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="8b12a-1316">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8b12a-1316">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="8b12a-1317">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8b12a-1317">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="8b12a-1318">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8b12a-1318">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="8b12a-1319">Cmdlet New-AzApplicationGateway mit optionalem Parameter -UserAssignedIdentity aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1319">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="8b12a-1320">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="8b12a-1320">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="8b12a-1321">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8b12a-1321">Az.OperationalInsights</span></span>
- <span data-ttu-id="8b12a-1322">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="8b12a-1322">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="8b12a-1323">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8b12a-1323">Az.Profile</span></span>
- <span data-ttu-id="8b12a-1324">Modulnamen in Az.Accounts geändert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1324">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="8b12a-1325">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8b12a-1325">Az.RecoveryServices</span></span>
- <span data-ttu-id="8b12a-1326">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="8b12a-1326">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="8b12a-1327">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8b12a-1327">Az.Resources</span></span>
- <span data-ttu-id="8b12a-1328">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="8b12a-1328">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="8b12a-1329">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8b12a-1329">Az.ServiceFabric</span></span>
- <span data-ttu-id="8b12a-1330">Unterstützung für das Angeben des Zertifikats anhand des allgemeinen Namens und Fingerabdrucks</span><span class="sxs-lookup"><span data-stu-id="8b12a-1330">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="8b12a-1331">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="8b12a-1331">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="8b12a-1332">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="8b12a-1332">Az.SIgnalR</span></span>
- <span data-ttu-id="8b12a-1333">Allgemeine Verfügbarkeit für PowerShell-Cmdlets für SIgnalR</span><span class="sxs-lookup"><span data-stu-id="8b12a-1333">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="8b12a-1334">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8b12a-1334">Az.Sql</span></span>
- <span data-ttu-id="8b12a-1335">Neue Erkennungstypen Data_Exfiltration und Unsafe_Action zu Cmdlets für Bedrohungserkennung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1335">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="8b12a-1336">Dokumentationsbeispiele für Cmdlets für SQL-Überwachung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1336">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="8b12a-1337">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="8b12a-1337">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="8b12a-1338">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8b12a-1338">Az.Storage</span></span>
- <span data-ttu-id="8b12a-1339">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="8b12a-1339">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="8b12a-1340">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8b12a-1340">Az.Websites</span></span>
- <span data-ttu-id="8b12a-1341">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="8b12a-1341">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="8b12a-1342">0.7.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="8b12a-1342">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="8b12a-1343">Allgemein</span><span class="sxs-lookup"><span data-stu-id="8b12a-1343">General</span></span>

* <span data-ttu-id="8b12a-1344">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="8b12a-1344">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="8b12a-1345">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8b12a-1345">Az.Compute</span></span>

* <span data-ttu-id="8b12a-1346">Unterstützung für UltraSSD und Katalogimages in einfachen Parametersätzen für `New-AzVm(ss)`-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1346">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="8b12a-1347">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8b12a-1347">Az.DataLakeStore</span></span>

* <span data-ttu-id="8b12a-1348">Nachgestellten Schrägstrich für die Domäne des ADLS-Kontos korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1348">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="8b12a-1349">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8b12a-1349">Az.FrontDoor</span></span>

* <span data-ttu-id="8b12a-1350">Einige fehlerhafte Links behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-1350">Fixed some broken links</span></span>
    - <span data-ttu-id="8b12a-1351">In den Artikeln zu New-AzureRmFrontDoor und Set-AzureRmFrontDoor den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorHealthProbeSettingObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1351">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="8b12a-1352">Im Artikel zu New-AzureRmFrontDoorManagedRuleObject den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorRuleGroupOverrideObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1352">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="8b12a-1353">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8b12a-1353">Az.RecoveryServices</span></span>

* <span data-ttu-id="8b12a-1354">Clientseitige Validierungen für Wiederherstellungsvorgänge von Azure-Dateifreigaben hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1354">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="8b12a-1355">storageAccountName und storageAccountResourceGroupName für AFS-Wiederherstellung optional gemacht.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1355">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="8b12a-1356">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8b12a-1356">Az.Resources</span></span>

* <span data-ttu-id="8b12a-1357">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="8b12a-1357">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="8b12a-1358">Get-AzureRmRoleAssignment für die Verwendung des Abonnementbereichs aktualisiert, wenn dieser beim Anfordern von klassischen Administratoren angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1358">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="8b12a-1359">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8b12a-1359">Az.Sql</span></span>

* <span data-ttu-id="8b12a-1360">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="8b12a-1360">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="8b12a-1361">Problem mit der Verwendung von Get-AzureRmSqlDatabaseVulnerabilityAssessment mit .NET Core behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-1361">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="8b12a-1362">Dokumentation mit Hilfemeldungen zu Cmdlets für die SQL-Überwachung geändert.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1362">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="8b12a-1363">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8b12a-1363">Az.Storage</span></span>

* <span data-ttu-id="8b12a-1364">-EnableHierarchicalNamespace zu New-AzureRmStorageAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1364">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="8b12a-1365">Problem behoben, bei dem für das Copy File-Cmdlet am Ziel kein Quellkontext wiederverwendet werden kann, wenn -DestContext nicht eingegeben wird</span><span class="sxs-lookup"><span data-stu-id="8b12a-1365">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="8b12a-1366">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="8b12a-1366">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="8b12a-1367">Unterstützung der Konfiguration von statischen Websites</span><span class="sxs-lookup"><span data-stu-id="8b12a-1367">Support Static Website configuration</span></span>
    - <span data-ttu-id="8b12a-1368">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8b12a-1368">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="8b12a-1369">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8b12a-1369">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="8b12a-1370">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8b12a-1370">Az.Websites</span></span>

* <span data-ttu-id="8b12a-1371">Set-AzureRmWebApp und Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8b12a-1371">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="8b12a-1372">Neuen Parameter (-AzureStoragePath) zum Angeben von Azure Storage-Pfaden hinzugefügt, die in Windows- und Linux-Container-Apps bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1372">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="8b12a-1373">Verwenden Sie die Ausgabe des neuen Cmdlets New-AzureRmWebAppAzureStoragePath als Parameter zum Festlegen der Azure Storage-Pfade.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1373">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="8b12a-1374">0.6.1 – November 2018</span><span class="sxs-lookup"><span data-stu-id="8b12a-1374">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="8b12a-1375">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8b12a-1375">Az.ApiManagement</span></span>
* <span data-ttu-id="8b12a-1376">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1376">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="8b12a-1377">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8b12a-1377">Az.Automation</span></span>
* <span data-ttu-id="8b12a-1378">Swagger-basierte Azure Automation-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8b12a-1378">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="8b12a-1379">Cmdlets zur Updateverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1379">Added Update Management cmdlets</span></span>
* <span data-ttu-id="8b12a-1380">Cmdlets zur Quellcodeverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1380">Added Source Control cmdlets</span></span>
* <span data-ttu-id="8b12a-1381">Cmdlet „Remove-AzureRmAutomationHybridWorkerGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1381">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="8b12a-1382">DSC-Befehl für die Knotenregistrierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1382">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="8b12a-1383">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8b12a-1383">Az.Compute</span></span>
* <span data-ttu-id="8b12a-1384">Identitätsproblem für SystemAssigned-Identität korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1384">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="8b12a-1385">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1385">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="8b12a-1386">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8b12a-1386">Az.ContainerInstance</span></span>
* <span data-ttu-id="8b12a-1387">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1387">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="8b12a-1388">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="8b12a-1388">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="8b12a-1389">Beschreibung der Beispiele für Marketplace-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1389">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="8b12a-1390">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8b12a-1390">Az.Network</span></span>
* <span data-ttu-id="8b12a-1391">Folgende Cmdlets hinzugefügt: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="8b12a-1391">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="8b12a-1392">ICMP wieder unterstützten AzureFirewall-Netzwerkprotokollen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1392">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="8b12a-1393">Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert und Überprüfung für Ziel-ID, Adresse und Port hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1393">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="8b12a-1394">Probleme mit Arbeitsspeicherauslastung in der VirtualNetwork-Zuordnung behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-1394">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="8b12a-1395">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="8b12a-1395">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="8b12a-1396">Problem beim Ändern der Richtlinie für eine geschützte Dateifreigabe behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-1396">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="8b12a-1397">Richtlinienzeitzone in Großschreibung geändert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1397">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="8b12a-1398">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="8b12a-1398">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="8b12a-1399">Korrigiertes Beispiel in „New-AzureRmRecoveryServicesAsrProtectableItem“</span><span class="sxs-lookup"><span data-stu-id="8b12a-1399">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="8b12a-1400">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1400">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="8b12a-1401">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="8b12a-1401">Az.Relay</span></span>
* <span data-ttu-id="8b12a-1402">Optionaler Parameter „-KeyValue“ zu Cmdlet „New-AzureRmRelayKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht</span><span class="sxs-lookup"><span data-stu-id="8b12a-1402">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="8b12a-1403">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8b12a-1403">Az.Resources</span></span>
* <span data-ttu-id="8b12a-1404">Hilfedokumentation für ressourcenidentitätsbezogene Parameter in `New-AzureRmPolicyAssignment` und `Set-AzureRmPolicyAssignment` aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1404">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="8b12a-1405">Beispiel für „New-AzureRmPolicyDefinition“ hinzugefügt, das „-Metadata“ nutzt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1405">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="8b12a-1406">Korrektur, um Beibehaltung von Groß-/Kleinschreibung in Tagschlüsseln in „NetStandard“ zu ermöglichen: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="8b12a-1406">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="8b12a-1407">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8b12a-1407">Az.ServiceFabric</span></span>
* <span data-ttu-id="8b12a-1408">Benachrichtigung über veraltete Elemente für anstehende wichtige Änderungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1408">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="8b12a-1409">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8b12a-1409">Az.Sql</span></span>
* <span data-ttu-id="8b12a-1410">Neue Cmdlets für CRUD-Vorgänge in verwalteten Azure SQL-Datenbank-Instanzen und verwalteten Azure SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1410">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="8b12a-1411">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8b12a-1411">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8b12a-1412">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8b12a-1412">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8b12a-1413">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8b12a-1413">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8b12a-1414">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8b12a-1414">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8b12a-1415">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8b12a-1415">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8b12a-1416">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8b12a-1416">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8b12a-1417">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8b12a-1417">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8b12a-1418">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8b12a-1418">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="8b12a-1419">Erweiterte Verwaltung von Überwachungsrichtlinien auf einem Server oder in einer Datenbank aktiviert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1419">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="8b12a-1420">Neuer Parameter (PredicateExpression) hinzugefügt, um die Filterung von Überwachungsprotokollen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="8b12a-1420">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="8b12a-1421">Cmdlets wurden angepasst, sodass sie SQL-Clients anstelle von Legacyclients verwenden.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1421">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="8b12a-1422">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="8b12a-1422">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="8b12a-1423">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="8b12a-1423">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="8b12a-1424">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="8b12a-1424">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="8b12a-1425">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="8b12a-1425">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="8b12a-1426">Problem bei Verwendung von „Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings“ mit festgelegtem Parameter für den Speicherkontonamen behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-1426">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="8b12a-1427">0.5.0 – November 2018</span><span class="sxs-lookup"><span data-stu-id="8b12a-1427">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="8b12a-1428">Allgemein</span><span class="sxs-lookup"><span data-stu-id="8b12a-1428">General</span></span>
* <span data-ttu-id="8b12a-1429">Ressourcenvervollständigungen für viele Kern-Cmdlets hinzugefügt (diese ermöglichen das Durchlaufen von vorhandenen Ressourcennamen per TAB-TASTE, wenn Cmdlets interaktiv aufgerufen werden)</span><span class="sxs-lookup"><span data-stu-id="8b12a-1429">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="8b12a-1430">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8b12a-1430">Az.Profile</span></span>
* <span data-ttu-id="8b12a-1431">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="8b12a-1431">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="8b12a-1432">Parameter „TenantId“ im Cmdlet „Connect-AzAccount“ in „Tenant“ umbenannt und Alias für „TenantId“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1432">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="8b12a-1433">Beschreibung von „TenantId“ für „Connect-AzAccount“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1433">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="8b12a-1434">Fehlermeldung für fehlgeschlagene Anmeldung bei Angabe der Mandantendomäne korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1434">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="8b12a-1435">Problem in Bezug auf Kontextnamenskonflikt für Konten ohne Abonnements im Mandanten behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-1435">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="8b12a-1436">Problem mit DataLake-Endpunkten bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-1436">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="8b12a-1437">Problem behoben, das zur Auslösung von „Disconnect-AzAccount“ führte, wenn keine Verbindung bestand</span><span class="sxs-lookup"><span data-stu-id="8b12a-1437">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="8b12a-1438">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8b12a-1438">Az.CognitiveServices</span></span>
* <span data-ttu-id="8b12a-1439">Vorgang „Get-AzCognitiveServicesAccountSkus“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1439">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8b12a-1440">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8b12a-1440">Az.Compute</span></span>
* <span data-ttu-id="8b12a-1441">Cmdlets Add-AzVmssVMDataDisk und Remove-AzVmssVMDataDisk hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1441">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="8b12a-1442">„Get-AzVMImage“ zeigt „AutomaticOSUpgradeProperties“ an</span><span class="sxs-lookup"><span data-stu-id="8b12a-1442">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="8b12a-1443">Problem behoben, aufgrund dessen die Optionswerte „SetAzVMChefExtension -BootstrapOptions“ und „-JsonAttribute“ nicht im JSON-Format festgelegt wurden</span><span class="sxs-lookup"><span data-stu-id="8b12a-1443">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8b12a-1444">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8b12a-1444">Az.DataLakeStore</span></span>
* <span data-ttu-id="8b12a-1445">Aktualisierung des DataLake-Pakets auf 1.1.10</span><span class="sxs-lookup"><span data-stu-id="8b12a-1445">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="8b12a-1446">Standardmäßige Parallelität zu Multithreadvorgängen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1446">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="8b12a-1447">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="8b12a-1447">Az.Insights</span></span>
* <span data-ttu-id="8b12a-1448">Problem Nr. 7267 behoben (Bereich für automatische Skalierung)</span><span class="sxs-lookup"><span data-stu-id="8b12a-1448">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="8b12a-1449">Probleme beim Erstellen einer neuen Regel für die automatische Skalierung, aufgrund derer die aufgelisteten Parameter nicht richtig festgelegt wurden (Es wurde stets der Standardwert festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="8b12a-1449">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="8b12a-1450">Problem Nr. 7513 behoben [Insights] „Set-AzDiagnosticSetting“ erfordert die explizite Angabe von Kategorien während der Erstellung der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1450">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="8b12a-1451">Nun erfordert das Cmdlet nicht die explizite Angabe der Kategorien, die während der Erstellung aktiviert werden sollen. Das bedeutet, es funktioniert wie dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1451">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8b12a-1452">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8b12a-1452">Az.Network</span></span>
* <span data-ttu-id="8b12a-1453">„PeeringType“ wurde geändert und ist nun ein erforderlicher Parameter für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="8b12a-1453">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="8b12a-1454">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="8b12a-1454">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="8b12a-1455">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="8b12a-1455">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="8b12a-1456">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8b12a-1456">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="8b12a-1457">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="8b12a-1457">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="8b12a-1458">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="8b12a-1458">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="8b12a-1459">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8b12a-1459">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8b12a-1460">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8b12a-1460">Az.PolicyInsights</span></span>
* <span data-ttu-id="8b12a-1461">Cmdlets für Richtlinienwartung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1461">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="8b12a-1462">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8b12a-1462">Az.Resources</span></span>
* <span data-ttu-id="8b12a-1463">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="8b12a-1463">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="8b12a-1464">Zulassen der Auflistung von Ressourcen mithilfe des Parameters „-ResourceId“ für „Get-AzResource“</span><span class="sxs-lookup"><span data-stu-id="8b12a-1464">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8b12a-1465">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8b12a-1465">Az.ServiceBus</span></span>
* <span data-ttu-id="8b12a-1466">Schreibgeschützte Eigenschaft „MigrationState“ zu „PSServiceBusMigrationConfigurationAttributes“ hinzugefügt, was das Ermitteln des Migrationsstatus ermöglicht</span><span class="sxs-lookup"><span data-stu-id="8b12a-1466">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8b12a-1467">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8b12a-1467">Az.ServiceFabric</span></span>
* <span data-ttu-id="8b12a-1468">Hinzufügen des Zertifikats zu Linux VMSS korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1468">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="8b12a-1469">„Add-AzServiceFabricClusterCertificate“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="8b12a-1469">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="8b12a-1470">Verwenden des richtigen Fingerabdrucks aus dem neuen Zertifikat (Azure/service-fabric-issues#932)</span><span class="sxs-lookup"><span data-stu-id="8b12a-1470">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="8b12a-1471">Richtige Anzeige von Ausnahmen (Azure/service-fabric-issues#1054)</span><span class="sxs-lookup"><span data-stu-id="8b12a-1471">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="8b12a-1472">„Update-AzServiceFabricDurability“ korrigiert, um die Clusterkonfiguration zu aktualisieren, bevor der VMSS-Vorgang „CreateOrUpdate“ gestartet wird</span><span class="sxs-lookup"><span data-stu-id="8b12a-1472">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="8b12a-1473">0.4.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="8b12a-1473">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="8b12a-1474">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8b12a-1474">Az.Profile</span></span>
* <span data-ttu-id="8b12a-1475">Problem mit „Get-AzSubscription“ in Cloud Shell behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-1475">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="8b12a-1476">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="8b12a-1476">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8b12a-1477">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8b12a-1477">Az.Compute</span></span>
* <span data-ttu-id="8b12a-1478">Neue Größen zur Whitelist von VM-Größen hinzugefügt, für die bei Verwendung des einfachen Parametersatzes für „New-AzVm“ der beschleunigte Netzwerkbetrieb aktiviert wird</span><span class="sxs-lookup"><span data-stu-id="8b12a-1478">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="8b12a-1479">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1479">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8b12a-1480">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8b12a-1480">Az.DataLakeStore</span></span>
* <span data-ttu-id="8b12a-1481">Unterstützung für VNET-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1481">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="8b12a-1482">Get-AzDataLakeStoreVirtualNetworkRule: Dient zum Abrufen oder Auflisten der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1482">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="8b12a-1483">Add-AzDataLakeStoreVirtualNetworkRule: Fügt dem angegebenen Data Lake Store-Konto eine Regel für das virtuelle Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1483">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="8b12a-1484">Set-AzDataLakeStoreVirtualNetworkRule: Ändert die angegebene Regel für das virtuelle Netzwerk in das angegebene Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1484">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="8b12a-1485">Remove-AzDataLakeStoreVirtualNetworkRule: Dient zum Löschen der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1485">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8b12a-1486">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8b12a-1486">Az.Network</span></span>
* <span data-ttu-id="8b12a-1487">Cmdlet „Test-AzNetworkWatcherConnectivity“ aktualisiert, Protokollwert wird jetzt an Back-End übergeben.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1487">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="8b12a-1488">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1488">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8b12a-1489">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8b12a-1489">Az.Resources</span></span>
* <span data-ttu-id="8b12a-1490">Problem behoben, aufgrund dessen „Get-AzRoleDefinition“ eine unverständliche Ausnahme auslöst (wenn das Standardprofil kein Abonnement enthält und kein Bereich festgelegt ist), indem im Szenario eine aussagekräftige Ausnahme hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1490">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="8b12a-1491">Außerdem wurde der Standardparametersatz auf „RoleDefinitionNameParameterSet“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1491">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="8b12a-1492">0.3.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="8b12a-1492">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="8b12a-1493">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="8b12a-1493">Azure.Storage</span></span>
* <span data-ttu-id="8b12a-1494">Fehler beim Kopieren von Blobs/Dateien behoben, aufgrund dessen bei einem Metadatenproblem des Ziels keine Metadaten kopiert wurden</span><span class="sxs-lookup"><span data-stu-id="8b12a-1494">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="8b12a-1495">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8b12a-1495">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="8b12a-1496">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="8b12a-1496">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="8b12a-1497">Der Abruf der Speicherressourcennutzung eines bestimmten Standorts wird jetzt unterstützt, und das Hinzufügen einer Warnmeldung für den Abruf der globalen Speicherressourcennutzung ist überflüssig.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1497">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="8b12a-1498">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="8b12a-1498">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8b12a-1499">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8b12a-1499">Az.CognitiveServices</span></span>
* <span data-ttu-id="8b12a-1500">„Get-AzCognitiveServicesAccountSkus“ wird ohne vorhandenes Konto unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1500">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8b12a-1501">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8b12a-1501">Az.Compute</span></span>
* <span data-ttu-id="8b12a-1502">Korrektur von „Get-AzVM -ResourceGroupName <rg>“, sodass ggf. mehr als 50 Ergebnisse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="8b12a-1502">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="8b12a-1503">Der Cmdlet-Hilfe zu „New-AzVmss“ wurde ein Beispiel für „SimpleParameterSet“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1503">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="8b12a-1504">Tippfehler in der Azure Disk Encryption-Statusmeldung behoben</span><span class="sxs-lookup"><span data-stu-id="8b12a-1504">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="8b12a-1505">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8b12a-1505">Az.DataFactoryV2</span></span>
* <span data-ttu-id="8b12a-1506">Die Version des ADF .Net-SDK wurde auf 2.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1506">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8b12a-1507">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8b12a-1507">Az.Network</span></span>
* <span data-ttu-id="8b12a-1508">NetworkProfile-Funktionalität wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1508">Added NetworkProfile functionality.</span></span> <span data-ttu-id="8b12a-1509">Neue Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1509">new cmdlets added</span></span>
    - <span data-ttu-id="8b12a-1510">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8b12a-1510">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="8b12a-1511">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8b12a-1511">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="8b12a-1512">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8b12a-1512">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="8b12a-1513">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8b12a-1513">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="8b12a-1514">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="8b12a-1514">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="8b12a-1515">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="8b12a-1515">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="8b12a-1516">Dienstzuordnungslink in Subnetzmodell hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1516">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="8b12a-1517">Cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1517">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="8b12a-1518">Cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1518">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8b12a-1519">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8b12a-1519">Az.RedisCache</span></span>
* <span data-ttu-id="8b12a-1520">Künftig sind beliebige Zeichenfolgen als Größenparameter zulässig.</span><span class="sxs-lookup"><span data-stu-id="8b12a-1520">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="8b12a-1521">P5 in Popup „PSArgumentCompleter“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1521">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="8b12a-1522">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8b12a-1522">Az.Resources</span></span>
* <span data-ttu-id="8b12a-1523">Fehlender Parameter „-Mode“ zu „Set-AzPolicyDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="8b12a-1523">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="8b12a-1524">Cmdlet-Fehler bei „Get-AzProviderOperation“ für Vorgänge mit Ursprung behoben, der den Benutzer enthält</span><span class="sxs-lookup"><span data-stu-id="8b12a-1524">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="8b12a-1525">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8b12a-1525">Az.Sql</span></span>
* <span data-ttu-id="8b12a-1526">Problem behoben, aufgrund dessen einige Sicherungs-Cmdlets das aktuelle Azure-Abonnements nicht erkannt haben</span><span class="sxs-lookup"><span data-stu-id="8b12a-1526">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8b12a-1527">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8b12a-1527">Az.Websites</span></span>
* <span data-ttu-id="8b12a-1528">Neues Cmdlet „Get-AzWebAppContainerContinuousDeploymentUrl“ zum Abrufen der Webhook-URL von Continuous Deployment für Container</span><span class="sxs-lookup"><span data-stu-id="8b12a-1528">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="8b12a-1529">Neue Cmdlets „New-AzWebAppContainerPSSession“ und „Enter-WebAppContainerPSSession“ zum Initiieren einer PowerShell-Remotesitzung in einer Windows-Container-App</span><span class="sxs-lookup"><span data-stu-id="8b12a-1529">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="8b12a-1530">0.2.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="8b12a-1530">0.2.0 - September 2018</span></span>
 <span data-ttu-id="8b12a-1531">Erstrelease</span><span class="sxs-lookup"><span data-stu-id="8b12a-1531">Initial Release</span></span>