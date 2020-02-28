---
title: Versionshinweise zu Azure PowerShell
description: Hier erfahren Sie mehr über die aktuellen Updates für die Azure PowerShell-Module.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/09/2020
ms.openlocfilehash: 81afcd63e5ca7a776965849de9090b833f49acc7
ms.sourcegitcommit: a321ef9d134c684fa24ababcbd898f86b00d9364
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "77477232"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="31e1b-103">Versionshinweise zu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="31e1b-103">Azure PowerShell release notes</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="31e1b-104">3.5.0: Februar 2020</span><span class="sxs-lookup"><span data-stu-id="31e1b-104">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="31e1b-105">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="31e1b-105">Highlights since the last major release</span></span>
* <span data-ttu-id="31e1b-106">Clientseitige Telemetrie aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-106">Updated client side telemetry.</span></span>
* <span data-ttu-id="31e1b-107">Cmdlets zur Unterstützung der Geräteverwaltung in Az.IotHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-107">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="31e1b-108">Cmdlets für Verfügbarkeitsgruppenlistener in Az.SqlVirtualMachine hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-108">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="31e1b-109">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="31e1b-109">Az.Accounts</span></span>
* <span data-ttu-id="31e1b-110">Abonnement-ID, Mandanten-ID und Ausführungszeit in clientseitigen Telemetriedaten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-110">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="31e1b-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="31e1b-111">Az.Automation</span></span>
* <span data-ttu-id="31e1b-112">Tippfehler in Beispiel 1 in der Referenzdokumentation für „New-AzAutomationSoftwareUpdateConfiguration“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-112">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="31e1b-113">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="31e1b-113">Az.CognitiveServices</span></span>
* <span data-ttu-id="31e1b-114">SDK auf 7.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-114">Updated SDK to 7.0</span></span>
* <span data-ttu-id="31e1b-115">Verbesserte Fehlermeldung, wenn der Server mit leerem Text antwortet</span><span class="sxs-lookup"><span data-stu-id="31e1b-115">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31e1b-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31e1b-116">Az.Compute</span></span>
* <span data-ttu-id="31e1b-117">Zulässiger leerer Wert für „ProximityPlacementGroupId“ während des Updates</span><span class="sxs-lookup"><span data-stu-id="31e1b-117">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="31e1b-118">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="31e1b-118">Az.FrontDoor</span></span>
* <span data-ttu-id="31e1b-119">Cmdlet zum Abrufen verwalteter Regeldefinitionen hinzugefügt, die in WAF verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="31e1b-119">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="31e1b-120">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="31e1b-120">Az.IotHub</span></span>
* <span data-ttu-id="31e1b-121">Unterstützung für die Verwaltung von Geräten in IoT Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-121">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="31e1b-122">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="31e1b-122">New Cmdlets are:</span></span>
    - <span data-ttu-id="31e1b-123">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="31e1b-123">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="31e1b-124">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="31e1b-124">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="31e1b-125">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="31e1b-125">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="31e1b-126">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="31e1b-126">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="31e1b-127">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="31e1b-127">Az.KeyVault</span></span>
* <span data-ttu-id="31e1b-128">Duplizierter Text für „Add-AzKeyVaultKey.md“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-128">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="31e1b-129">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="31e1b-129">Az.Monitor</span></span>
* <span data-ttu-id="31e1b-130">Beschreibung des Cmdlets „Get-AzLog cmdlet“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-130">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="31e1b-131">Dem Befehl „New-AzMetricAlertRuleV2“ wurde ein Parameter namens „ActionGroupId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-131">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="31e1b-132">Der Benutzer kann entweder „ActionGroupId(string)“ oder „ActionGorup(ActivityLogAlertActionGroup)“ angeben.</span><span class="sxs-lookup"><span data-stu-id="31e1b-132">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31e1b-133">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31e1b-133">Az.Network</span></span>
* <span data-ttu-id="31e1b-134">Zusätzlicher Parameterhinweis für den Parameter „-EnableProxyProtocol“ für das Cmdlet „New-AzPrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-134">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="31e1b-135">FilterData-Beispiel in „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-135">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="31e1b-136">Paketerfassungsbeispiel für die Erfassung aller inneren und äußeren Pakete in „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-136">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="31e1b-137">Unterstützte Azure Firewall-Richtlinie für VNET-Firewalls</span><span class="sxs-lookup"><span data-stu-id="31e1b-137">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="31e1b-138">Keine neuen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-138">No new cmdlets are added.</span></span> <span data-ttu-id="31e1b-139">Die Einschränkung für die Firewallrichtlinie für VNET-Firewalls wurde gelockert.</span><span class="sxs-lookup"><span data-stu-id="31e1b-139">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="31e1b-140">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="31e1b-140">Az.RecoveryServices</span></span>
* <span data-ttu-id="31e1b-141">Unterstützung für „Als Dateien wiederherstellen“ für SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-141">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="31e1b-142">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31e1b-142">Az.Resources</span></span>
* <span data-ttu-id="31e1b-143">Cmdlets für die Vorlagenbereitstellung umgestaltet</span><span class="sxs-lookup"><span data-stu-id="31e1b-143">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="31e1b-144">Neue Cmdlets zur Verwaltung von Bereitstellungen in der Verwaltungsgruppe hinzugefügt: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="31e1b-144">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="31e1b-145">Neue Cmdlets zur Verwaltung von Bereitstellungen im Mandantenbereich hinzugefügt: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="31e1b-145">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="31e1b-146">Cmdlets vom Typ „\*-AzDeployment“ für den speziellen Einsatz im Abonnementbereich umgestaltet</span><span class="sxs-lookup"><span data-stu-id="31e1b-146">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="31e1b-147">Aliase vom Typ „*-AzSubscriptionDeployment“ für Cmdlets vom Typ „*-AzDeployment“ erstellt</span><span class="sxs-lookup"><span data-stu-id="31e1b-147">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="31e1b-148">„Update-AzADApplication“ korrigiert, wenn der Parameter „AvailableToOtherTenants“ nicht festgelegt wird</span><span class="sxs-lookup"><span data-stu-id="31e1b-148">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="31e1b-149">„ApplicationObjectWithoutCredentialParameterSet“ entfernt, um „AmbiguousParameterSetException“ zu vermeiden</span><span class="sxs-lookup"><span data-stu-id="31e1b-149">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="31e1b-150">Hilfedateien erneut generiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-150">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="31e1b-151">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31e1b-151">Az.Sql</span></span>
* <span data-ttu-id="31e1b-152">Unterstützung für abonnementübergreifende Point-in-Time-Wiederherstellung für verwaltete Instanzen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-152">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="31e1b-153">Unterstützung für die Änderung der Hardwaregeneration von vorhandenen verwalteten SQL-Instanzen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-153">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="31e1b-154">Hilfebeispiele für „Update-AzSqlServerVulnerabilityAssessmentSetting“ korrigiert: parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="31e1b-154">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="31e1b-155">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="31e1b-155">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="31e1b-156">Cmdlets für Verfügbarkeitsgruppenlistener hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-156">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="31e1b-157">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="31e1b-157">Az.StorageSync</span></span>
* <span data-ttu-id="31e1b-158">Unterstützte Zeichensätze in „Invoke-AzStorageSyncCompatibilityCheck“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-158">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="31e1b-159">3.4.0: Februar 2020</span><span class="sxs-lookup"><span data-stu-id="31e1b-159">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="31e1b-160">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="31e1b-160">Highlights since the last major release</span></span>
* <span data-ttu-id="31e1b-161">Az.CosmosDB: erste Version 0.1.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="31e1b-161">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="31e1b-162">Unterstützung für Az.Network ConnectionMonitor V2 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-162">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="31e1b-163">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="31e1b-163">Az.Accounts</span></span>
* <span data-ttu-id="31e1b-164">Deaktivieren der automatischen Kontextspeicherung, wenn „AzureRmContext.json“ nicht verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="31e1b-164">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="31e1b-165">Aktualisieren des Verweises auf Azure Powershell Common auf 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="31e1b-165">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="31e1b-166">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="31e1b-166">Az.ApiManagement</span></span>
* <span data-ttu-id="31e1b-167">**Get-AzApiManagementApiSchema** Fehler beim Abrufen des einer API zugeordneten Open-Api-Schemas behoben   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="31e1b-167">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="31e1b-168">**New-AzApiManagementProduct**\* und **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="31e1b-168">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="31e1b-169">Dokumentation korrigiert für https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="31e1b-169">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="31e1b-170">**Set-AzApiManagementApi** Beispiel hinzugefügt, das das Aktualisieren von ServiceUrl mithilfe des Cmdlets veranschaulicht</span><span class="sxs-lookup"><span data-stu-id="31e1b-170">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31e1b-171">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31e1b-171">Az.Compute</span></span>
* <span data-ttu-id="31e1b-172">Anzahl des VM-Status auf 100 beschränkt, um die Drosselung zu vermeiden, wenn „Get-AzVM -Status“ ohne VM-Name ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="31e1b-172">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="31e1b-173">Cmdlet „Update-AzDiskEncryptionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-173">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="31e1b-174">Die Parameter „EncryptionType“ und „DiskEncryptionSetId“ wurden den folgenden Cmdlets hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="31e1b-174">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="31e1b-175">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="31e1b-175">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="31e1b-176">Parameter „ColocationStatus“ zum Cmdlet „Get-AzProximityPlacementGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-176">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="31e1b-177">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="31e1b-177">Az.DataFactory</span></span>
* <span data-ttu-id="31e1b-178">Version des ADF .NET SDK auf 4.7.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-178">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="31e1b-179">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="31e1b-179">Az.DeploymentManager</span></span>
* <span data-ttu-id="31e1b-180">LIST-Vorgänge für Ressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-180">Adds LIST operations for resources</span></span>
* <span data-ttu-id="31e1b-181">Funktionen zum Ausführen von Vorgängen für Integritätsprüfungsschritte hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-181">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="31e1b-182">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="31e1b-182">Az.HDInsight</span></span>
* <span data-ttu-id="31e1b-183">Dokumentationsfehler für „New-AzHDInsightCluster“ behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-183">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="31e1b-184">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="31e1b-184">Az.KeyVault</span></span>
* <span data-ttu-id="31e1b-185">Namensalias zum VaultName-Attribut hinzugefügt, um „Remove-AzureKeyVault“ mit „New-AzureKeyVault“ konsistent zu machen</span><span class="sxs-lookup"><span data-stu-id="31e1b-185">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31e1b-186">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31e1b-186">Az.Network</span></span>
* <span data-ttu-id="31e1b-187">Neues Beispiel zu „Set-AzNetworkWatcherConfigFlowLog.md“ hinzugefügt, um das Szenario zur Traffic Analytics-Deaktivierung zu veranschaulichen</span><span class="sxs-lookup"><span data-stu-id="31e1b-187">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="31e1b-188">Unterstützung für die Zuweisung der IP-Verwaltungskonfiguration zu Azure Firewall hinzugefügt: ein dediziertes Subnetz und eine öffentliche IP-Adresse, die von der Firewall für den Verwaltungsdatenverkehr verwendet werden</span><span class="sxs-lookup"><span data-stu-id="31e1b-188">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="31e1b-189">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="31e1b-189">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="31e1b-190">Parameter „-ManagementPublicIpAddress“ (nicht obligatorisch) hinzugefügt, der ein Objekt für die öffentliche IP-Adresse akzeptiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-190">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="31e1b-191">Methode „SetManagementIpConfiguration“ für Firewallobjekt hinzugefügt. Erfordert ein Subnetz und eine öffentliche IP-Adresse als Eingabe, und der Subnetzname muss „AzureFirewallManagementSubnet“ lauten.</span><span class="sxs-lookup"><span data-stu-id="31e1b-191">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="31e1b-192">Beispiele für „Get-AzNetworkSecurityGroup“ korrigiert, um Beispiele für Netzwerksicherheitsgruppen und nicht für Netzwerkschnittstellen anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="31e1b-192">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="31e1b-193">Tippfehler im Befehl „New-AzVpnSite“ korrigiert, der dazu führte, dass die Vervollständigung für die Ressourcen-ID einen Parameter nicht vervollständigen konnte</span><span class="sxs-lookup"><span data-stu-id="31e1b-193">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="31e1b-194">Unterstützung für die URL-Konfiguration im Aktionssatz für Neuschreibungsregeln in Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-194">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="31e1b-195">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="31e1b-195">New cmdlets added:</span></span>
        - <span data-ttu-id="31e1b-196">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="31e1b-196">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="31e1b-197">Cmdlets mit optionalem Parameter aktualisiert: UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="31e1b-197">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="31e1b-198">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="31e1b-198">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="31e1b-199">Unterstützung für Ressourcen der Version 2 von NetworkWatcher ConnectionMonitor hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-199">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="31e1b-200">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="31e1b-200">Az.PolicyInsights</span></span>
* <span data-ttu-id="31e1b-201">Unterstützung der Konformitätsbewertung vor der Ermittlung der zu korrigierenden Ressourcen</span><span class="sxs-lookup"><span data-stu-id="31e1b-201">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="31e1b-202">Parameter „-ResourceDiscoverMode“ zu „Start-AzPolicyRemediation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-202">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="31e1b-203">Cmdlet „Get-AzPolicyMetadata“ zum Abrufen der Ressourcen für Richtlinienmetadaten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-203">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="31e1b-204">„Get-AzPolicyState“ und „Get-AzPolicyStateSummary“ für API-Version 2019-10-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-204">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="31e1b-205">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="31e1b-205">Az.RecoveryServices</span></span>
* <span data-ttu-id="31e1b-206">Azure Site Recovery-Unterstützung für das Entfernen eines replizierten Datenträgers</span><span class="sxs-lookup"><span data-stu-id="31e1b-206">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="31e1b-207">In Azure Backup wurde Unterstützung zum Hinzufügen von Tags bei der Erstellung eines Recovery Services-Tresors hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-207">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="31e1b-208">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31e1b-208">Az.Resources</span></span>
* <span data-ttu-id="31e1b-209">„-Scope“ in Cmdlets vom Typ „\*-AzPolicyAssignment“ nun optional (standardmäßig auf Abonnementkontext festgelegt)</span><span class="sxs-lookup"><span data-stu-id="31e1b-209">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="31e1b-210">Beispiele zum Erstellen von „ADServicePrincipal“ mit Kennwort und Schlüsselanmeldeinformation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-210">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="31e1b-211">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31e1b-211">Az.Sql</span></span>
<span data-ttu-id="31e1b-212">Cmdlet „New-AzSqlDatabaseSecondary“ korrigiert, um auf die Existenz von „PartnerDatabaseName“ anstelle von „DatabaseName“ zu prüfen</span><span class="sxs-lookup"><span data-stu-id="31e1b-212">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="31e1b-213">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="31e1b-213">Az.Storage</span></span>
* <span data-ttu-id="31e1b-214">Unterstützung für das Festlegen des Schlüsseltyps für die Tabellen-/Warteschlangenverschlüsselung beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="31e1b-214">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="31e1b-215">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="31e1b-215">New-AzStorageAccount</span></span>
* <span data-ttu-id="31e1b-216">Anzeigen der Anforderungs-ID (RequestId), wenn für „StorageException“ keine erweiterten Fehlerinformationen (ExtendedErrorInformation) vorliegen</span><span class="sxs-lookup"><span data-stu-id="31e1b-216">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="31e1b-217">Beispiel 6 des Cmdlets „Start-AzStorageBlobCopy“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-217">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="31e1b-218">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="31e1b-218">Az.Websites</span></span>
* <span data-ttu-id="31e1b-219">„Set-AzWebapp“ und „Set-AzWebappSlot“ unterstützen die Eigenschaften „AlwaysOn“, „MinTls“ und „FtpsState“.</span><span class="sxs-lookup"><span data-stu-id="31e1b-219">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="31e1b-220">Problem behoben, das dazu führte, dass beim Festlegen von „HttpsOnly“ bei gleichzeitiger Änderung von „AppservicePlan“ mit dem einzelnen Befehl „Set-AzWebApp“ „HttpsOnly“ auf den Standardwert zurückgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="31e1b-220">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="31e1b-221">3.3.0 – Januar 2020</span><span class="sxs-lookup"><span data-stu-id="31e1b-221">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="31e1b-222">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="31e1b-222">Az.Accounts</span></span>
* <span data-ttu-id="31e1b-223">„Add-AzEnvironment“ und „Set-AzEnvironment“ wurden so aktualisiert, dass sie jetzt die Parameter „AzureAttestationServiceEndpointResourceId“ und „AzureAttestationServiceEndpointSuffix“ akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="31e1b-223">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="31e1b-224">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="31e1b-224">Az.Cdn</span></span>
* <span data-ttu-id="31e1b-225">Anzeigen von Fehlerantwortdetails im Cmdlet „New-AzCdnEndpoint“</span><span class="sxs-lookup"><span data-stu-id="31e1b-225">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31e1b-226">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31e1b-226">Az.Compute</span></span>
* <span data-ttu-id="31e1b-227">Cmdlet „Set-AzVMCustomScriptExtension“ für eine VM mit verwaltetem Betriebssystemdatenträger ohne Betriebssystemprofil wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="31e1b-227">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="31e1b-228">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="31e1b-228">Az.ContainerInstance</span></span>
* <span data-ttu-id="31e1b-229">Im Beispiel von „New-AzContainerGroup“ verwendete Parameternamen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="31e1b-229">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="31e1b-230">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="31e1b-230">Az.DataBoxEdge</span></span>
* <span data-ttu-id="31e1b-231">Cmdlet „Get-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-231">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="31e1b-232">Edge-Speichercontainer abrufen</span><span class="sxs-lookup"><span data-stu-id="31e1b-232">Get the Edge Storage Container</span></span>
* <span data-ttu-id="31e1b-233">Cmdlet „New-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-233">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="31e1b-234">Neuen Edge-Speichercontainer erstellen</span><span class="sxs-lookup"><span data-stu-id="31e1b-234">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="31e1b-235">Cmdlet „Remove-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-235">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="31e1b-236">Edge-Speichercontainer entfernen</span><span class="sxs-lookup"><span data-stu-id="31e1b-236">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="31e1b-237">Cmdlet „Invoke-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-237">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="31e1b-238">Aktion zum Aktualisieren von Daten in Edge-Speichercontainer aufrufen</span><span class="sxs-lookup"><span data-stu-id="31e1b-238">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="31e1b-239">Cmdlet „Get-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-239">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="31e1b-240">Edge-Speicherkonto abrufen</span><span class="sxs-lookup"><span data-stu-id="31e1b-240">Get the Edge Storage Account</span></span>
* <span data-ttu-id="31e1b-241">Cmdlet „New-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-241">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="31e1b-242">Neues Edge-Speicherkonto erstellen</span><span class="sxs-lookup"><span data-stu-id="31e1b-242">Create new Edge Storage Account</span></span>
* <span data-ttu-id="31e1b-243">Cmdlet „Remove-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-243">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="31e1b-244">Edge-Speicherkonto entfernen</span><span class="sxs-lookup"><span data-stu-id="31e1b-244">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="31e1b-245">Cmdlet „Invoke-AzDataBoxEdgeShare“ aufrufen</span><span class="sxs-lookup"><span data-stu-id="31e1b-245">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="31e1b-246">Aktion zum Aktualisieren von Daten auf Freigabe aufrufen</span><span class="sxs-lookup"><span data-stu-id="31e1b-246">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="31e1b-247">Cmdlet „Set-AzDataBoxEdgeStorageAccountCredential“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-247">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="31e1b-248">Festlegen der Speicherkonto-Anmeldeinformationen für „az databoxedge“</span><span class="sxs-lookup"><span data-stu-id="31e1b-248">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="31e1b-249">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="31e1b-249">Az.DataFactory</span></span>
* <span data-ttu-id="31e1b-250">Eigenschaften „AutoUpdateETA“, „LatestVersion“, „PushedVersion“, „TaskQueueId“ und „VersionStatus“ für Befehl „Get-AzDataFactoryV2IntegrationRuntime“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-250">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="31e1b-251">Version des ADF .NET SDK auf 4.6.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-251">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="31e1b-252">Parameter „PublicIPs“ wurde für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um das Erstellen der Azure-SSIS Integration Runtime mit statischen öffentlichen IP-Adressen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="31e1b-252">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="31e1b-253">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="31e1b-253">Az.DevTestLabs</span></span>
* <span data-ttu-id="31e1b-254">Fehlerhafter Link in „Get-AzDtlAllowedVMSizesPolicy.md“ entfernt</span><span class="sxs-lookup"><span data-stu-id="31e1b-254">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="31e1b-255">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="31e1b-255">Az.EventHub</span></span>
* <span data-ttu-id="31e1b-256">Behebung des Problems 10634: Verweis auf NULL-Objekt für „remove eventhubnamespace“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-256">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="31e1b-257">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="31e1b-257">Az.HDInsight</span></span>
* <span data-ttu-id="31e1b-258">Fehler in „Invoke-AzHDInsightHiveJob.md“ wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="31e1b-258">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="31e1b-259">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="31e1b-259">Az.MachineLearning</span></span>
* <span data-ttu-id="31e1b-260">Die folgenden Cmdlets wurden entfernt, da „MachineLearningCompute“ nicht mehr verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="31e1b-260">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="31e1b-261">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="31e1b-261">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="31e1b-262">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="31e1b-262">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="31e1b-263">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="31e1b-263">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="31e1b-264">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="31e1b-264">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="31e1b-265">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="31e1b-265">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="31e1b-266">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="31e1b-266">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="31e1b-267">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="31e1b-267">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31e1b-268">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31e1b-268">Az.Network</span></span>
* <span data-ttu-id="31e1b-269">Upgrade der Abhängigkeit von „Microsoft.Azure.Management.Sql“ von „1.36-preview“ auf „1.37-preview“</span><span class="sxs-lookup"><span data-stu-id="31e1b-269">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="31e1b-270">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="31e1b-270">Az.RecoveryServices</span></span>
* <span data-ttu-id="31e1b-271">Änderung der Azure Site Recovery-Unterstützung für virtuelle Computer mit verwalteten Datenträgern, die im Ruhezustand mit kundenseitig verwalteten Schlüsseln für Azure-zu-Azure-Anbieter verschlüsselt sind</span><span class="sxs-lookup"><span data-stu-id="31e1b-271">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="31e1b-272">Azure Site Recovery-Unterstützung für die Eingabe der ID des Datenträgerverschlüsselungssatzes als optionale Eingabe beim Aktivieren des Schutzes für VMware in Azure</span><span class="sxs-lookup"><span data-stu-id="31e1b-272">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="31e1b-273">Azure Site Recovery-Unterstützung für die Eingabe der ID des Datenträgerverschlüsselungssatzes als optionale Eingabe auf Datenträgerebene beim Aktivieren des Schutzes für VMware in Azure</span><span class="sxs-lookup"><span data-stu-id="31e1b-273">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="31e1b-274">Azure Site Recovery-Unterstützung zum Aktualisieren eines replikationsgeschützten Elements mit der Zuordnung eines Datenträgerverschlüsselungssatzes für HyperV in Azure</span><span class="sxs-lookup"><span data-stu-id="31e1b-274">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="31e1b-275">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31e1b-275">Az.Resources</span></span>
* <span data-ttu-id="31e1b-276">Fehler in Hilfedokument zu „Remove-AzTag“ behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-276">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="31e1b-277">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31e1b-277">Az.Sql</span></span>
* <span data-ttu-id="31e1b-278">Funktionalität der Baseline-Cmdlets für einen Sicherheitsrisikobewertungssatz korrigiert, sodass sie auf der Master-Datenbank für Azure Database funktionieren und sie auf Systemdatenbanken von verwalteten Instanzen einschränken.</span><span class="sxs-lookup"><span data-stu-id="31e1b-278">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="31e1b-279">Fehler beim Erstellen einer SQL-Instanzfailovergruppe behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-279">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="31e1b-280">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="31e1b-280">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="31e1b-281">DR als neuer gültiger Lizenztyp hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-281">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="31e1b-282">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="31e1b-282">Az.Storage</span></span>
* <span data-ttu-id="31e1b-283">Warnmeldung für Breaking Change hinzugefügt: Wertänderung für „DefaultAction“ in einer zukünftigen Version</span><span class="sxs-lookup"><span data-stu-id="31e1b-283">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="31e1b-284">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="31e1b-284">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="31e1b-285">Unterstützung für das Abrufen der letzten Synchronisierungszeit des Speicherkontos durch Ausführen von „get-AzureRMStorageAccount“ mit Parameter „-IncludeGeoReplicationStats“</span><span class="sxs-lookup"><span data-stu-id="31e1b-285">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span> 
    - <span data-ttu-id="31e1b-286">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="31e1b-286">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="31e1b-287">3.2.0: Dezember 2019</span><span class="sxs-lookup"><span data-stu-id="31e1b-287">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="31e1b-288">Allgemein</span><span class="sxs-lookup"><span data-stu-id="31e1b-288">General</span></span>
* <span data-ttu-id="31e1b-289">Verweise in „.psd1“ zur Verwendung des relativen Pfads für alle Module aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-289">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="31e1b-290">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="31e1b-290">Az.Accounts</span></span>
* <span data-ttu-id="31e1b-291">Richtiges UserAgent-Element für clientseitige Telemetrie für Az 4.0-Vorschauversion festgelegt</span><span class="sxs-lookup"><span data-stu-id="31e1b-291">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="31e1b-292">Anzeigen benutzerfreundlicher Fehlermeldungen, wenn der Kontext in der Az 4.0-Vorschauversion NULL ist</span><span class="sxs-lookup"><span data-stu-id="31e1b-292">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="31e1b-293">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="31e1b-293">Az.Batch</span></span>
* <span data-ttu-id="31e1b-294">Problem [#10602](https://github.com/Azure/azure-powershell/issues/10602) behoben, aufgrund dessen „VirtualMachineConfiguration.ContainerConfiguration“ oder „VirtualMachineConfiguration.DataDisks“ von **New-AzBatchPool** nicht ordnungsgemäß an den Server gesendet wurde</span><span class="sxs-lookup"><span data-stu-id="31e1b-294">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="31e1b-295">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="31e1b-295">Az.DataFactory</span></span>
* <span data-ttu-id="31e1b-296">Version des ADF .NET SDK auf 4.5.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-296">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="31e1b-297">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="31e1b-297">Az.FrontDoor</span></span>
* <span data-ttu-id="31e1b-298">Unterstützung für den Ausschluss verwalteter WAF-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-298">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="31e1b-299">SocketAddr zur automatischen Vervollständigung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-299">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="31e1b-300">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="31e1b-300">Az.HealthcareApis</span></span>
* <span data-ttu-id="31e1b-301">Ausnahmebehandlung</span><span class="sxs-lookup"><span data-stu-id="31e1b-301">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="31e1b-302">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="31e1b-302">Az.KeyVault</span></span>
* <span data-ttu-id="31e1b-303">Fehler im Zusammenhang mit dem Zugriff auf einen möglicherweise nicht festgelegten Wert behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-303">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="31e1b-304">Zertifikatverwaltung für Kryptografie für elliptische Kurve</span><span class="sxs-lookup"><span data-stu-id="31e1b-304">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="31e1b-305">Unterstützung zum Angeben der Kurve für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-305">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="31e1b-306">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="31e1b-306">Az.Monitor</span></span>
* <span data-ttu-id="31e1b-307">Optionales Argument zum Befehl „Diagnoseeinstellungen hinzufügen“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-307">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="31e1b-308">Ein Optionsargument, das angibt, dass der Export in Log Analytics ein festes Schema sein muss (auch bekannt als</span><span class="sxs-lookup"><span data-stu-id="31e1b-308">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="31e1b-309">dedizierter Datentyp)</span><span class="sxs-lookup"><span data-stu-id="31e1b-309">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31e1b-310">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31e1b-310">Az.Network</span></span>
* <span data-ttu-id="31e1b-311">Unterstützung für IpGroups in der AzureFirewall-Anwendung sowie in NAT- und Netzwerkregeln</span><span class="sxs-lookup"><span data-stu-id="31e1b-311">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="31e1b-312">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31e1b-312">Az.Resources</span></span>
* <span data-ttu-id="31e1b-313">Problem behoben, aufgrund dessen die Vorlagenbereitstellung einen Vorlagenparameter nicht lesen kann, wenn der Name einen Konflikt mit einem integrierten Parameternamen verursacht</span><span class="sxs-lookup"><span data-stu-id="31e1b-313">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="31e1b-314">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-09-01 aktualisiert, die Gruppierungsunterstützung in Richtliniensatzdefinitionen einführt</span><span class="sxs-lookup"><span data-stu-id="31e1b-314">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="31e1b-315">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31e1b-315">Az.Sql</span></span>
* <span data-ttu-id="31e1b-316">Speichererstellung in automatischer Aktivierung der Sicherheitsrisikobewertung auf StorageV2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-316">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="31e1b-317">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="31e1b-317">Az.Storage</span></span>
* <span data-ttu-id="31e1b-318">Unterstützung der Generierung blob-/containeridentitätsbasierter SAS-Token mit Speicherkontext auf der Grundlage der OAuth-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="31e1b-318">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="31e1b-319">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="31e1b-319">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="31e1b-320">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="31e1b-320">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="31e1b-321">Unterstützung für das Widerrufen von Schlüsseln für die Speicherkonto-Benutzerdelegierung hinzugefügt, sodass alle SAS-Identitätstoken widerrufen werden</span><span class="sxs-lookup"><span data-stu-id="31e1b-321">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="31e1b-322">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="31e1b-322">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="31e1b-323">Upgrade auf Microsoft.Azure.Management.Storage 14.2.0, um die neue API-Version 2019-06-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="31e1b-323">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="31e1b-324">Unterstützung von QuotaGiB (Freigabekontingent in Gibibyte) für Werte über 5120 in der Verwaltungsebene von Dateifreigabe-Cmdlets und Parameteralias „Quota“ zum Parameter „QuotaGiB“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-324">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span> 
    - <span data-ttu-id="31e1b-325">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="31e1b-325">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="31e1b-326">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="31e1b-326">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="31e1b-327">Parameteralias „QuotaGiB“ zum Parameter „Quota“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-327">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="31e1b-328">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="31e1b-328">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="31e1b-329">Problem behoben, dass „Set-AzStorageContainerAcl“ die gespeicherte Zugriffsrichtlinie bereinigen kann</span><span class="sxs-lookup"><span data-stu-id="31e1b-329">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="31e1b-330">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="31e1b-330">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="31e1b-331">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="31e1b-331">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="31e1b-332">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="31e1b-332">Highlights since the last major release</span></span>
* <span data-ttu-id="31e1b-333">Az.DataBoxEdge 1.0.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="31e1b-333">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="31e1b-334">Az.SqlVirtualMachine 1.0.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="31e1b-334">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31e1b-335">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31e1b-335">Az.Compute</span></span>
* <span data-ttu-id="31e1b-336">Funktion zum erneuten Anwenden von VMs</span><span class="sxs-lookup"><span data-stu-id="31e1b-336">VM Reapply feature</span></span>
    - <span data-ttu-id="31e1b-337">Parameter für erneutes Anwenden zu Cmdlet „Set-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-337">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="31e1b-338">AutomaticRepairs-Funktion für VM-Skalierungsgruppe:</span><span class="sxs-lookup"><span data-stu-id="31e1b-338">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="31e1b-339">Parameter „EnableAutomaticRepair“, „AutomaticRepairGracePeriod“ und „AutomaticRepairMaxInstanceRepairsPercent“ zu folgenden Cmdlets hinzugefügt:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="31e1b-339">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="31e1b-340">Mandantenübergreifende Unterstützung von Katalogimages für „New-AzVM“</span><span class="sxs-lookup"><span data-stu-id="31e1b-340">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="31e1b-341">„Spot“ zu Argumentvervollständigung des Priority-Parameters in Cmdlets „New-AzVM“, „New-AzVMConfig“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-341">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="31e1b-342">Parameter „DiskIOPSReadWrite“ und „DiskMBpsReadWrite“ zu Cmdlet „Add-AzVmssDataDisk“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-342">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="31e1b-343">Parameter „SourceImageId“ von Cmdlet „New-AzGalleryImageVersion“ in optional geändert</span><span class="sxs-lookup"><span data-stu-id="31e1b-343">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="31e1b-344">Parameter „OSDiskImage“ und „DataDiskImage“ zu Cmdlet „New-AzGalleryImageVersion“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-344">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="31e1b-345">Parameter „HyperVGeneration“ zu Cmdlet „New-AzGalleryImageDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-345">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="31e1b-346">Parameter „SkipExtensionsOnOverprovisionedVMs“ zu Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-346">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="31e1b-347">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="31e1b-347">Az.DataBoxEdge</span></span>
* <span data-ttu-id="31e1b-348">Cmdlet `Get-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-348">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="31e1b-349">Bestellung abrufen</span><span class="sxs-lookup"><span data-stu-id="31e1b-349">Get the Order</span></span>
* <span data-ttu-id="31e1b-350">Cmdlet `New-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-350">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="31e1b-351">Neue Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="31e1b-351">Create new Order</span></span>
* <span data-ttu-id="31e1b-352">Cmdlet `Remove-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-352">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="31e1b-353">Bestellung entfernen</span><span class="sxs-lookup"><span data-stu-id="31e1b-353">Remove the Order</span></span>
* <span data-ttu-id="31e1b-354">Änderung im Cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="31e1b-354">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="31e1b-355">Erstellt jetzt eine lokale Freigabe</span><span class="sxs-lookup"><span data-stu-id="31e1b-355">Now creates Local Share</span></span>
* <span data-ttu-id="31e1b-356">Cmdlet `Set-AzDataBoxEdgeRole` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-356">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="31e1b-357">„IotRole“ kann jetzt einer Freigabe zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="31e1b-357">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="31e1b-358">Cmdlet `Invoke-AzDataBoxEdgeDevice` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-358">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="31e1b-359">Scanupdate aufrufen, Update herunterladen, Updates auf dem Gerät installieren</span><span class="sxs-lookup"><span data-stu-id="31e1b-359">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="31e1b-360">Cmdlet `Get-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-360">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="31e1b-361">Ruft die Informationen zu Auslösern ab</span><span class="sxs-lookup"><span data-stu-id="31e1b-361">Gets the information about Triggers</span></span>
* <span data-ttu-id="31e1b-362">Cmdlet `New-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-362">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="31e1b-363">Neue Auslöser erstellen</span><span class="sxs-lookup"><span data-stu-id="31e1b-363">Create new Triggers</span></span>
* <span data-ttu-id="31e1b-364">Cmdlet `Remove-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-364">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="31e1b-365">Auslöser entfernen</span><span class="sxs-lookup"><span data-stu-id="31e1b-365">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="31e1b-366">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="31e1b-366">Az.DataFactory</span></span>
* <span data-ttu-id="31e1b-367">Version des ADF .NET SDK auf 4.4.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-367">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="31e1b-368">Parameter „ExpressCustomSetup“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um Setupkonfigurationen und Drittanbieterkomponenten ohne benutzerdefiniertes Setupskript zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="31e1b-368">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="31e1b-369">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="31e1b-369">Az.DataLakeStore</span></span>
* <span data-ttu-id="31e1b-370">Dokumentation von „Get-AzDataLakeStoreDeletedItem“ und „Restore-AzDataLakeStoreDeletedItem“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-370">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="31e1b-371">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="31e1b-371">Az.EventHub</span></span>
* <span data-ttu-id="31e1b-372">Behebung des Problems 10301: Datumsformat von SAS-Token korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-372">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="31e1b-373">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="31e1b-373">Az.FrontDoor</span></span>
* <span data-ttu-id="31e1b-374">Parameter „MinimumTlsVersion“ zu „Enable-AzFrontDoorCustomDomainHttps“ und „New-AzFrontDoorFrontendEndpointObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-374">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="31e1b-375">Parameter „HealthProbeMethod“ und „EnabledState“ zu „New-AzFrontDoorHealthProbeSettingObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-375">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="31e1b-376">Neues Cmdlet zum Erstellen von BackendPoolsSettings-Objekten für die Übergabe in Erstellung/Update von Front Door hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-376">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="31e1b-377">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="31e1b-377">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31e1b-378">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31e1b-378">Az.Network</span></span>
* <span data-ttu-id="31e1b-379">FilterData-Optionsbeispiele „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ geändert.</span><span class="sxs-lookup"><span data-stu-id="31e1b-379">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="31e1b-380">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="31e1b-380">Az.PrivateDns</span></span>
* <span data-ttu-id="31e1b-381">PrivateDns.net-SDK auf Version 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-381">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="31e1b-382">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="31e1b-382">Az.RecoveryServices</span></span>
* <span data-ttu-id="31e1b-383">Azure Site Recovery-Unterstützung zum Auswählen des Datenträgertyps beim Aktivieren des Schutzes.</span><span class="sxs-lookup"><span data-stu-id="31e1b-383">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="31e1b-384">Fehlerbehebung bei Bearbeitungsaktion für Azure Site Recovery-Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="31e1b-384">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="31e1b-385">SQL-Wiederherstellungsunterstützung für Azure Backup zum Akzeptieren von Filestream-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="31e1b-385">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="31e1b-386">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="31e1b-386">Az.RedisCache</span></span>
* <span data-ttu-id="31e1b-387">Parameter „MinimumTlsVersion“ in Cmdlets „New-AzRedisCache“ und „Set-AzRedisCache“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-387">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="31e1b-388">Außerdem „MinimumTlsVersion“ in Ausgabe von Cmdlet „Get-AzRedisCache“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-388">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="31e1b-389">Validierung von Parameter „-Size“ für Cmdlets „Set-AzRedisCache“ und „New-AzRedisCache“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-389">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="31e1b-390">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31e1b-390">Az.Resources</span></span>
- <span data-ttu-id="31e1b-391">Richtlinien-Cmdlets aktualisiert, um die neue API-Version 2019-06-01 mit der neuen EnforcementMode-Eigenschaft bei der Richtlinienzuweisung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="31e1b-391">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="31e1b-392">Hilfebeispiel zum Erstellen von Richtliniendefinitionen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-392">Updated create policy definition help example</span></span>
- <span data-ttu-id="31e1b-393">Fehlerkorrektur: „Remove-AZADServicePrincipal -ServicePrincipalName“ gibt Nullverweis aus, wenn Dienstprinzipalname nicht gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="31e1b-393">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="31e1b-394">Fehlerkorrektur: „New-AZADServicePrincipal“ gibt Nullverweis aus, wenn Mandant kein Abonnement hat.</span><span class="sxs-lookup"><span data-stu-id="31e1b-394">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="31e1b-395">„New-AzAdServicePrincipal“ geändert, um Anmeldeinformation nur zu zugeordneter Anwendung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="31e1b-395">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="31e1b-396">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31e1b-396">Az.Sql</span></span>
* <span data-ttu-id="31e1b-397">Unterstützung von „ReadReplicaCount“ für Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-397">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="31e1b-398">Korrektur von „Set-AzSqlDatabase“, wenn Zonenredundanz nicht festgelegt</span><span class="sxs-lookup"><span data-stu-id="31e1b-398">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="31e1b-399">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="31e1b-399">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="31e1b-400">Allgemein</span><span class="sxs-lookup"><span data-stu-id="31e1b-400">General</span></span>
* <span data-ttu-id="31e1b-401">Az.PrivateDns 1.0.0 veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="31e1b-401">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="31e1b-402">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="31e1b-402">Az.Accounts</span></span>
* <span data-ttu-id="31e1b-403">Hinweis zur Veraltung des Alias „Resolve-Error“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-403">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="31e1b-404">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="31e1b-404">Az.Advisor</span></span>
* <span data-ttu-id="31e1b-405">Neue Kategorie „Operational Excellence“ für Cmdlet „Get-AzAdvisorRecommendation“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-405">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="31e1b-406">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="31e1b-406">Az.Batch</span></span>
* <span data-ttu-id="31e1b-407">`CoreQuota` für `BatchAccountContext` in `DedicatedCoreQuota` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-407">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="31e1b-408">Außerdem wurde das neue Element `LowPriorityCoreQuota` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-408">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="31e1b-409">Dies wirkt sich auf **Get-AzBatchAccount** aus.</span><span class="sxs-lookup"><span data-stu-id="31e1b-409">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="31e1b-410">Für Parameter `-ResourceFile` von **New-AzBatchTask** wird jetzt eine Sammlung mit `PSResourceFile`-Objekten verwendet, und für die Erstellung kann das Cmdlet **New-AzBatchResourceFile** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="31e1b-410">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="31e1b-411">Neues Cmdlet **New-AzBatchResourceFile** als Hilfe für die Erstellung von `PSResourceFile`-Objekten.</span><span class="sxs-lookup"><span data-stu-id="31e1b-411">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="31e1b-412">Diese können für **New-AzBatchTask** über den Parameter `-ResourceFile` bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="31e1b-412">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="31e1b-413">Hierbei werden zusätzlich zum Ansatz mit `HttpUrl` zwei neue Arten von Ressourcendateien unterstützt:</span><span class="sxs-lookup"><span data-stu-id="31e1b-413">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="31e1b-414">Mit Ressourcendateien, die auf `AutoStorageContainerName` basieren, wird ein gesamter Container für die automatische Speicherung auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="31e1b-414">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="31e1b-415">Für Ressourcendateien, die auf `StorageContainerUrl` basieren, wird der in der URL angegebene Container auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="31e1b-415">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="31e1b-416">`ApplicationPackages`-Eigenschaft von `PSApplication` entfernt, die von **Get-AzBatchApplication** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="31e1b-416">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="31e1b-417">Die spezifischen Pakete in einer Anwendung können jetzt mit **Get-AzBatchApplicationPackage** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="31e1b-417">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="31e1b-418">Beispiel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="31e1b-418">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="31e1b-419">`ApplicationId` für **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** und **Set-AzBatchApplication** in `ApplicationName` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-419">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="31e1b-420">`ApplicationId` ist jetzt ein Alias von `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="31e1b-420">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="31e1b-421">Neue `PSWindowsUserConfiguration`-Eigenschaft zu `PSUserAccount` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-421">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="31e1b-422">`Version` für `PSApplicationPackage` in `Name` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-422">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="31e1b-423">`BlobSource` für `PSResourceFile` in `HttpUrl` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-423">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="31e1b-424">`OSDisk`-Eigenschaft aus `PSVirtualMachineConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-424">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="31e1b-425">**Set-AzBatchPoolOSVersion** entfernt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-425">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="31e1b-426">Dieser Vorgang wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-426">This operation is no longer supported.</span></span>
* <span data-ttu-id="31e1b-427">`TargetOSVersion` aus `PSCloudServiceConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-427">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="31e1b-428">`CurrentOSVersion` für `PSCloudServiceConfiguration` in `OSVersion` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-428">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="31e1b-429">`DataEgressGiB` und `DataIngressGiB` aus `PSPoolUsageMetrics` entfernt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-429">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="31e1b-430">**Get-AzBatchNodeAgentSku** entfernt und durch **Get-AzBatchSupportedImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-430">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="31e1b-431">**Get-AzBatchSupportedImage** gibt die gleichen Daten wie **Get-AzBatchNodeAgentSku** zurück, aber in einem benutzerfreundlicheren Format.</span><span class="sxs-lookup"><span data-stu-id="31e1b-431">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="31e1b-432">Neue nicht verifizierte Images werden nun ebenfalls zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="31e1b-432">New non-verified images are also now returned.</span></span> <span data-ttu-id="31e1b-433">Zusätzlich sind weitere Informationen zu `Capabilities` und `BatchSupportEndOfLife` für jedes Image vorhanden.</span><span class="sxs-lookup"><span data-stu-id="31e1b-433">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="31e1b-434">Möglichkeit zum Bereitstellen von Remotedateisystemen auf jedem Knoten eines Pools über den neuen Parameter `MountConfiguration` von **New-AzBatchPool** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-434">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="31e1b-435">Es ist jetzt Unterstützung für Sicherheitsregeln vorhanden, die den Netzwerkzugriff auf einen Pool basierend auf dem Quellport des Datenverkehrs blockieren.</span><span class="sxs-lookup"><span data-stu-id="31e1b-435">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="31e1b-436">Dies erfolgt über die `SourcePortRanges`-Eigenschaft unter `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="31e1b-436">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="31e1b-437">Bei der Ausführung eines Containers unterstützt Batch jetzt die Ausführung der Aufgabe im Arbeitsverzeichnis des Containers bzw. im Arbeitsverzeichnis der Batch-Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="31e1b-437">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="31e1b-438">Dies wird mit der `WorkingDirectory`-Eigenschaft unter `PSTaskContainerSettings` gesteuert.</span><span class="sxs-lookup"><span data-stu-id="31e1b-438">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="31e1b-439">Möglichkeit zum Angeben einer Sammlung mit öffentlichen IP-Adressen für `PSNetworkConfiguration` über die neue `PublicIPs`-Eigenschaft hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-439">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="31e1b-440">So wird sichergestellt, dass Knoten im Pool über eine IP-Adresse aus der Liste mit den von Benutzern bereitgestellten IP-Adressen verfügen.</span><span class="sxs-lookup"><span data-stu-id="31e1b-440">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="31e1b-441">Wenn kein Wert angegeben wird, lautet der Standardwert von `WaitForSuccess` unter `PSSTartTask` jetzt `$True` (bisher `$False`).</span><span class="sxs-lookup"><span data-stu-id="31e1b-441">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="31e1b-442">Wenn kein Wert angegeben wird, lautet der Standardwert von `Scope` unter `PSAutoUserSpecification` jetzt `Pool` (bisher `Task` unter Windows und `Pool` unter Linux).</span><span class="sxs-lookup"><span data-stu-id="31e1b-442">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="31e1b-443">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="31e1b-443">Az.Cdn</span></span>
* <span data-ttu-id="31e1b-444">„UrlRewriteAction“ und „CacheKeyQueryStringAction“ für „RulesEngine“ eingeführt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-444">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="31e1b-445">Mehrere Fehler behoben, z. B. fehlende „Selector“-Eingabe im Cmdlet „New-AzDeliveryRuleCondition“.</span><span class="sxs-lookup"><span data-stu-id="31e1b-445">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31e1b-446">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31e1b-446">Az.Compute</span></span>
* <span data-ttu-id="31e1b-447">Feature „Datenträgerverschlüsselungssatz“</span><span class="sxs-lookup"><span data-stu-id="31e1b-447">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="31e1b-448">Neue Cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="31e1b-448">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="31e1b-449">Parameter „DiskEncryptionSetId“ wurde den folgenden Cmdlets hinzugefügt: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="31e1b-449">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="31e1b-450">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="31e1b-450">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="31e1b-451">Die Parameter „DiskEncryptionSetId“ und „EncryptionType“ wurden den folgenden Cmdlets hinzugefügt:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="31e1b-451">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="31e1b-452">Parameter „PublicIPAddressVersion“ wurde „New-AzVmssIPConfig“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-452">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="31e1b-453">„FileUris“ für benutzerdefinierte Skripterweiterung von öffentlicher Einstellung auf geschützte Einstellung umgestellt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-453">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="31e1b-454">„ScaleInPolicy“ wurde den Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-454">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="31e1b-455">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="31e1b-455">Breaking changes</span></span>
    - <span data-ttu-id="31e1b-456">Parameter „UploadSizeInBytes“ wird anstelle von „DiskSizeGB“ für „New-AzDiskConfig“ verwendet, wenn „CreateOption“ auf „Upload“ festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="31e1b-456">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="31e1b-457">Im „GalleryImageVersion“-Objekt wurde „objectPublishingProfile.Source.ManagedImage.Id“ durch „StorageProfile.Source.Id“ ersetzt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-457">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="31e1b-458">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="31e1b-458">Az.DataFactory</span></span>
* <span data-ttu-id="31e1b-459">Version des ADF .NET SDK auf 4.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="31e1b-459">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="31e1b-460">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="31e1b-460">Az.DataLakeStore</span></span>
* <span data-ttu-id="31e1b-461">Update für ADLS SDK-Version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) mit den folgenden Fehlerbehebungen durchgeführt:</span><span class="sxs-lookup"><span data-stu-id="31e1b-461">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="31e1b-462">Vermeidung der Auslösung einer Ausnahme, während die Deserialisierung des „creationtime“-Elements des Papierkorb- oder Verzeichniseintrags nicht durchgeführt werden kann</span><span class="sxs-lookup"><span data-stu-id="31e1b-462">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="31e1b-463">Verfügbarmachung der Einstellung pro Anforderungszeitlimit in „adlsclient“</span><span class="sxs-lookup"><span data-stu-id="31e1b-463">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="31e1b-464">Fehlerbehebung für Übergabe des ursprünglichen „syncflag“-Elements für badoffset-Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="31e1b-464">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="31e1b-465">Fehlerbehebung für „EnumerateDirectory“ zum Abrufen des Fortsetzungstokens nach der Überprüfung der Antwort</span><span class="sxs-lookup"><span data-stu-id="31e1b-465">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="31e1b-466">Behebung eines Verkettungsfehlers</span><span class="sxs-lookup"><span data-stu-id="31e1b-466">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="31e1b-467">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="31e1b-467">Az.FrontDoor</span></span>
* <span data-ttu-id="31e1b-468">Verschiedene Tippfehler im Modul korrigiert.</span><span class="sxs-lookup"><span data-stu-id="31e1b-468">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="31e1b-469">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="31e1b-469">Az.HDInsight</span></span>
* <span data-ttu-id="31e1b-470">Fehler behoben, bei dem Kunden die Meldung „Keine gültige Base64-Zeichenfolge“ erhalten haben, wenn sie „Get-AzHDInsightCluster“ zum Abrufen des Clusters mit ADLSGen1-Speicher verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="31e1b-470">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="31e1b-471">Parameter mit dem Namen „ApplicationId“ den drei Cmdlets „Add-AzHDInsightClusterIdentity“, „New-AzHDInsightClusterConfig“ und „New-AzHDInsightCluster“ hinzugefügt, damit der Kunde die Dienstprinzipal-Anwendungs-ID für den Zugriff auf Azure Data Lake bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="31e1b-471">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="31e1b-472">Microsoft.Azure.Management.HDInsight von 2.1.0 in 5.1.0 geändert.</span><span class="sxs-lookup"><span data-stu-id="31e1b-472">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="31e1b-473">Fünf Cmdlets wurden entfernt:</span><span class="sxs-lookup"><span data-stu-id="31e1b-473">Removed five cmdlets:</span></span>
    - <span data-ttu-id="31e1b-474">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="31e1b-474">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="31e1b-475">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="31e1b-475">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="31e1b-476">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="31e1b-476">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="31e1b-477">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="31e1b-477">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="31e1b-478">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="31e1b-478">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="31e1b-479">Drei Cmdlets wurden hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="31e1b-479">Added three cmdlets:</span></span>
    - <span data-ttu-id="31e1b-480">„Get-AzHDInsightMonitoring“ als Ersatz für „Get-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="31e1b-480">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="31e1b-481">„Enable-AzHDInsightMonitoring“ als Ersatz für „Enable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="31e1b-481">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="31e1b-482">„Disable-AzHDInsightMonitoring“ als Ersatz für „Disable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="31e1b-482">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="31e1b-483">Fehler für Cmdlet „Get-AzHDInsightProperties“ behoben, um Unterstützung für das Abrufen von Funktionsinformationen von einem bestimmten Ort bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="31e1b-483">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="31e1b-484">Parametersätze („Spark1“, „Spark2“) aus „Add-AzHDInsightConfigValue“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-484">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="31e1b-485">Beispiele den Hilfedokumenten des Cmdlets „Add-AzHDInsightSecurityProfile“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-485">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="31e1b-486">Der Ausgabetyp der folgenden Cmdlets wurde geändert:</span><span class="sxs-lookup"><span data-stu-id="31e1b-486">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="31e1b-487">Ausgabetyp für „Get-AzHDInsightProperties“ von „CapabilitiesResponse“ in „AzureHDInsightCapabilities“ geändert.</span><span class="sxs-lookup"><span data-stu-id="31e1b-487">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="31e1b-488">Ausgabetyp für „Remove-AzHDInsightCluster“ von „ClusterGetResponse“ in „bool“ geändert.</span><span class="sxs-lookup"><span data-stu-id="31e1b-488">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="31e1b-489">Ausgabetyp für „Set-AzHDInsightGatewaySettings“ von „HttpConnectivitySettings“ in „GatewaySettings“ geändert.</span><span class="sxs-lookup"><span data-stu-id="31e1b-489">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="31e1b-490">Einige Testfälle für Szenarien wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-490">Added some scenario test cases.</span></span>
* <span data-ttu-id="31e1b-491">Aliase wurden entfernt: „Add-AzHDInsightConfigValues“, „Get-AzHDInsightProperties“.</span><span class="sxs-lookup"><span data-stu-id="31e1b-491">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="31e1b-492">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="31e1b-492">Az.IotHub</span></span>
* <span data-ttu-id="31e1b-493">Wichtige Änderungen:</span><span class="sxs-lookup"><span data-stu-id="31e1b-493">Breaking changes:</span></span>
    - <span data-ttu-id="31e1b-494">Das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="31e1b-494">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="31e1b-495">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-495">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="31e1b-496">Das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="31e1b-496">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="31e1b-497">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-497">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="31e1b-498">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-498">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="31e1b-499">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-499">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="31e1b-500">Das Cmdlet „New-AzIotHubExportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubExportDevices“.</span><span class="sxs-lookup"><span data-stu-id="31e1b-500">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="31e1b-501">Das Cmdlet „New-AzIotHubImportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubImportDevices“.</span><span class="sxs-lookup"><span data-stu-id="31e1b-501">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="31e1b-502">Das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="31e1b-502">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="31e1b-503">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-503">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="31e1b-504">Das Cmdlet „Set-AzIotHub“ unterstützt den Parameter „OperationsMonitoringProperties“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="31e1b-504">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="31e1b-505">Der Parametersatz „UpdateOperationsMonitoringProperties“ für das Cmdlet „Set-AzIotHub“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-505">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="31e1b-506">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="31e1b-506">Az.RecoveryServices</span></span>
* <span data-ttu-id="31e1b-507">Azure wurde die Azure Site Recovery-Unterstützung zum Konfigurieren von Netzwerkressourcen, z. B. NSG, öffentliche IP-Adresse und interner Load Balancer für Azure, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-507">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="31e1b-508">Azure Site Recovery-Unterstützung zum Schreiben auf verwaltete Datenträger für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-508">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="31e1b-509">Azure Site Recovery-Unterstützung für NIC-Reduzierung für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-509">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="31e1b-510">Azure wurde Azure Site Recovery-Unterstützung für beschleunigten Netzwerkbetrieb für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-510">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="31e1b-511">Azure wurde Azure Site Recovery-Unterstützung für automatische Agent-Updates für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-511">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="31e1b-512">Azure wurde Azure Site Recovery-Unterstützung für SSD Standard für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-512">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="31e1b-513">Azure wurde Azure Site Recovery-Unterstützung für das zweistufige Azure Disk Encryption-Verfahren für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-513">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="31e1b-514">Azure wurde Azure Site Recovery-Unterstützung für das Schützen von neu hinzugefügten Datenträgern für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-514">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="31e1b-515">Feature „Vorläufiges Löschen“ (SoftDelete) für VM und zugehörige Tests hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-515">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="31e1b-516">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31e1b-516">Az.Resources</span></span>
* <span data-ttu-id="31e1b-517">Abhängigkeitsassembly „Microsoft.Extensions.Caching.Memory“ von 1.1.1 auf 2.2 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="31e1b-517">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31e1b-518">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31e1b-518">Az.Network</span></span>
* <span data-ttu-id="31e1b-519">Alle Cmdlets für „PrivateEndpointConnection“ geändert, um Unterstützung für generischen Dienstanbieter bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="31e1b-519">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="31e1b-520">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="31e1b-520">Updated cmdlet:</span></span>
        - <span data-ttu-id="31e1b-521">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="31e1b-521">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="31e1b-522">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="31e1b-522">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="31e1b-523">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="31e1b-523">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="31e1b-524">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="31e1b-524">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="31e1b-525">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="31e1b-525">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="31e1b-526">Neues Cmdlet für „PrivateLinkResource“ hinzugefügt, einschließlich Unterstützung des generischen Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="31e1b-526">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="31e1b-527">Neues Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="31e1b-527">New cmdlet:</span></span>
        - <span data-ttu-id="31e1b-528">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="31e1b-528">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="31e1b-529">Neue Felder und Parameter für das Feature „Proxyprotokoll V2“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-529">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="31e1b-530">„EnableProxyProtocol“-Eigenschaft in „PrivateLinkService“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-530">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="31e1b-531">„LinkIdentifier“-Eigenschaft in „PrivateEndpointConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-531">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="31e1b-532">„New-AzPrivateLinkService“ aktualisiert, um den neuen optionalen Parameter „EnableProxyProtocol“ hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="31e1b-532">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="31e1b-533">Fehlerhafte Parameterbeschreibung in Referenzdokumentation von „New-AzApplicationGatewaySku“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="31e1b-533">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="31e1b-534">Neue Cmdlets zur Unterstützung der Azure-Firewallrichtlinie hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-534">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="31e1b-535">Unterstützung für untergeordnete Ressource „RouteTables“ von VirtualHub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-535">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="31e1b-536">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="31e1b-536">New cmdlets added:</span></span>
        - <span data-ttu-id="31e1b-537">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="31e1b-537">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="31e1b-538">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="31e1b-538">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="31e1b-539">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="31e1b-539">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="31e1b-540">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="31e1b-540">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="31e1b-541">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="31e1b-541">Set-AzVirtualHub</span></span>
* <span data-ttu-id="31e1b-542">Unterstützung für die neuen Eigenschaften „Sku“ von VirtualHub und „VirtualWANType“ von VirtualWan hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-542">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="31e1b-543">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="31e1b-543">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="31e1b-544">New-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-544">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="31e1b-545">Update-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-545">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="31e1b-546">New-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-546">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="31e1b-547">Update-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-547">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="31e1b-548">Unterstützung für „EnableInternetSecurity“-Eigenschaft für „HubVnetConnection“, „VpnConnection“ und „ExpressRouteConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-548">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="31e1b-549">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="31e1b-549">New cmdlets added:</span></span>
        - <span data-ttu-id="31e1b-550">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="31e1b-550">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="31e1b-551">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="31e1b-551">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="31e1b-552">New-AzureRmVirtualHubVnetConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-552">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="31e1b-553">New-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-553">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="31e1b-554">Update-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-554">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="31e1b-555">New-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-555">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="31e1b-556">Set-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-556">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="31e1b-557">Unterstützung für die Konfiguration der „WebApplicationFirewall“-Richtlinie der obersten Ebene hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-557">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="31e1b-558">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="31e1b-558">New cmdlets added:</span></span>
        - <span data-ttu-id="31e1b-559">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="31e1b-559">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="31e1b-560">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="31e1b-560">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="31e1b-561">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="31e1b-561">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="31e1b-562">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="31e1b-562">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="31e1b-563">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="31e1b-563">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="31e1b-564">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="31e1b-564">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="31e1b-565">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="31e1b-565">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="31e1b-566">New-AzApplicationGatewayFirewallPolicy: Parameter „PolicySetting“, „ManagedRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-566">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="31e1b-567">Unterstützung für Operator „Geo-Match“ unter „CustomRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-567">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="31e1b-568">„GeoMatch“ zum Operator von „FirewallCondition“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-568">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="31e1b-569">Unterstützung für Firewallrichtlinien „perListener“ und „perSite“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-569">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="31e1b-570">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="31e1b-570">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="31e1b-571">New-AzApplicationGatewayHttpListener: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-571">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="31e1b-572">New-AzApplicationGatewayPathRuleConfig: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-572">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="31e1b-573">Fehlerbehebung: Nichtbeachtung der Groß-/Kleinschreibung für erforderliches Subnetz mit dem Namen „AzureBastionSubnet“ in „PSBastion“ ist jetzt möglich.</span><span class="sxs-lookup"><span data-stu-id="31e1b-573">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="31e1b-574">Unterstützung für Ziel-FQDNs in Netzwerkregeln und Übersetzung von FQDN in NAT-Regeln für Azure Firewall hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-574">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="31e1b-575">Unterstützung für Ressource „RouteTables“ der obersten Ebene von „IpGroup“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-575">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="31e1b-576">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="31e1b-576">New cmdlets added:</span></span>
        - <span data-ttu-id="31e1b-577">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="31e1b-577">New-AzIpGroup</span></span>
        - <span data-ttu-id="31e1b-578">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="31e1b-578">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="31e1b-579">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="31e1b-579">Get-AzIpGroup</span></span>
        - <span data-ttu-id="31e1b-580">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="31e1b-580">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="31e1b-581">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="31e1b-581">Az.ServiceFabric</span></span>
* <span data-ttu-id="31e1b-582">Cmdlet „Add-AzServiceFabricApplicationCertificate“ entfernt, da dieses Szenario durch „Add-AzVmssSecret“ abgedeckt ist.</span><span class="sxs-lookup"><span data-stu-id="31e1b-582">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="31e1b-583">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31e1b-583">Az.Sql</span></span>
* <span data-ttu-id="31e1b-584">Unterstützung für die Wiederherstellung von gelöschten Datenbanken auf verwalteten Instanzen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-584">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="31e1b-585">Veraltete Cmdlets für die Überprüfung aus Code ausgesondert.</span><span class="sxs-lookup"><span data-stu-id="31e1b-585">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="31e1b-586">Veraltete Aliase entfernt:</span><span class="sxs-lookup"><span data-stu-id="31e1b-586">Removed deprecated aliases:</span></span>
* <span data-ttu-id="31e1b-587">Get-AzSqlDatabaseIndexRecommendations (stattdessen „Get-AzSqlDatabaseIndexRecommendation“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="31e1b-587">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="31e1b-588">Get-AzSqlDatabaseRestorePoints (stattdessen „Get-AzSqlDatabaseRestorePoint“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="31e1b-588">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="31e1b-589">Cmdlet „Get-AzSqlDatabaseSecureConnectionPolicy“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-589">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="31e1b-590">Aliase für veraltete Cmdlets für Einstellungen zur Sicherheitsrisikobewertung wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-590">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="31e1b-591">Cmdlets für Einstellungen für die erweiterte Bedrohungserkennung wurden als veraltet eingestuft.</span><span class="sxs-lookup"><span data-stu-id="31e1b-591">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="31e1b-592">Cmdlets zum Deaktivieren und Aktivieren von Vertraulichkeitsempfehlungen in Spalten einer Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-592">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="31e1b-593">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="31e1b-593">Az.Storage</span></span>
* <span data-ttu-id="31e1b-594">Unterstützung für große Dateifreigaben beim Erstellen oder Aktualisieren eines Speicherkontos hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-594">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="31e1b-595">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="31e1b-595">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="31e1b-596">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="31e1b-596">Set-AzStorageAccount</span></span>
* <span data-ttu-id="31e1b-597">Beim Schließen/Abrufen des Dateihandles wird die Überprüfung des Eingabepfads auf Dateiverzeichnis oder Datei übersprungen, um einen Fehler für das Objekt im Status „DeletePending“ zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="31e1b-597">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="31e1b-598">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="31e1b-598">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="31e1b-599">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="31e1b-599">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="31e1b-600">2.8.0: Oktober 2019</span><span class="sxs-lookup"><span data-stu-id="31e1b-600">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="31e1b-601">Allgemein</span><span class="sxs-lookup"><span data-stu-id="31e1b-601">General</span></span>
* <span data-ttu-id="31e1b-602">Az.HealthcareApis-Release 1.0.0</span><span class="sxs-lookup"><span data-stu-id="31e1b-602">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="31e1b-603">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="31e1b-603">Az.Accounts</span></span>
* <span data-ttu-id="31e1b-604">Telemetriedaten und URL-Umschreibung für generierte Module aktualisiert, Windows-Komponententests korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-604">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="31e1b-605">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="31e1b-605">Az.ApiManagement</span></span>
* <span data-ttu-id="31e1b-606">**Set-AzApiManagementApi**: Unterstützung für die Aktualisierung der API in „ApiVersionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-606">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="31e1b-607">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="31e1b-607">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="31e1b-608">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="31e1b-608">Az.Automation</span></span>
* <span data-ttu-id="31e1b-609">Cmdlet „New-AzureAutomationSoftwareUpdateConfiguration“ für den Parameter für die Linux-Neustarteinstellung korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-609">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="31e1b-610">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="31e1b-610">Az.Batch</span></span>
* <span data-ttu-id="31e1b-611">**Get-AzBatchNodeAgentSku** ist veraltet und wird in Version 2.0.0 durch **Get-AzBatchSupportImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-611">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31e1b-612">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31e1b-612">Az.Compute</span></span>
* <span data-ttu-id="31e1b-613">Parameter „Priority“, „EvictionPolicy“ und „MaxPrice“ zu den Cmdlets „“New-AzVM“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-613">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="31e1b-614">Warnmeldung und Hilfedokument für die Cmdlets „Add-AzVMAdditionalUnattendContent“ und „Add-AzVMSshPublicKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-614">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="31e1b-615">Ausnahme „-skipVmBackup“ Linux-VMs mit verwalteten Datenträgern für „Set-AzVMDiskEncryptionExtension“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-615">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="31e1b-616">Fehler beim Aktualisieren von Verschlüsselungseinstellungen in „Set-AzVMDiskEncryptionExtension“ korrigiert (zweistufiges Szenario)</span><span class="sxs-lookup"><span data-stu-id="31e1b-616">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="31e1b-617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="31e1b-617">Az.DataFactory</span></span>
* <span data-ttu-id="31e1b-618">CRUD-Befehle für ADF V2-Datenfluss hinzugefügt: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow und Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="31e1b-618">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="31e1b-619">Aktionsbefehle für Debugsitzung für ADF V2-Datenfluss hinzugefügt: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand und Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="31e1b-619">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="31e1b-620">Version des ADF .NET SDK auf 4.2.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-620">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="31e1b-621">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="31e1b-621">Az.DataLakeStore</span></span>
* <span data-ttu-id="31e1b-622">Kontoüberprüfung korrigiert, sodass Konten mit „-“ ohne Domäne übermittelt werden können</span><span class="sxs-lookup"><span data-stu-id="31e1b-622">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="31e1b-623">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="31e1b-623">Az.HealthcareApis</span></span>
* <span data-ttu-id="31e1b-624">PowerShell-Version auf 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-624">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="31e1b-625">SDK-Version auf 1.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-625">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="31e1b-626">Aktualisierung in Tests, um auf neue SDK-Version zu verweisen</span><span class="sxs-lookup"><span data-stu-id="31e1b-626">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="31e1b-627">Ausgabestruktur von geschachtelt in vereinfacht geändert</span><span class="sxs-lookup"><span data-stu-id="31e1b-627">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="31e1b-628">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="31e1b-628">Az.IotHub</span></span>
* <span data-ttu-id="31e1b-629">Neue Routingquelle hinzugefügt: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="31e1b-629">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="31e1b-630">Kleinere Fehlerbehebung: „Get-AzIothub“ gibt „subscriptionId“ nicht zurück.</span><span class="sxs-lookup"><span data-stu-id="31e1b-630">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="31e1b-631">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="31e1b-631">Az.Monitor</span></span>
* <span data-ttu-id="31e1b-632">Neue Aktionsgruppenempfänger für Aktionsgruppe hinzugefügt:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="31e1b-632">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="31e1b-633">Verwendung des allgemeinen Warnungsschemas für Empfänger aktiviert.</span><span class="sxs-lookup"><span data-stu-id="31e1b-633">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="31e1b-634">Dies gilt nicht für SMS, Azure App-Pushbenachrichtigungen, ITSM und Sprachempfänger.</span><span class="sxs-lookup"><span data-stu-id="31e1b-634">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="31e1b-635">Webhooks unterstützen nun die Azure Active Directory-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="31e1b-635">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31e1b-636">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31e1b-636">Az.Network</span></span>
* <span data-ttu-id="31e1b-637">Neues Cmdlet „Get-AzAvailableServiceAlias“ hinzugefügt, das zum Abrufen der Aliase aufgerufen werden kann, die für Dienstendpunktrichtlinien verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="31e1b-637">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="31e1b-638">Unterstützung für das Hinzufügen von Verbindungen von Datenverkehrsselektoren zu Virtual Network-Gatewayverbindungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-638">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="31e1b-639">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="31e1b-639">New cmdlets added:</span></span>
        - <span data-ttu-id="31e1b-640">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="31e1b-640">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="31e1b-641">Cmdlets mit optionalen Parametern aktualisiert: -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="31e1b-641">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="31e1b-642">Unterstützung für ESP- und AH-Protokolle in Konfigurationen von Netzwerksicherheitsregeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-642">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="31e1b-643">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="31e1b-643">Updated cmdlets:</span></span>
        - <span data-ttu-id="31e1b-644">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="31e1b-644">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="31e1b-645">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="31e1b-645">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="31e1b-646">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="31e1b-646">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="31e1b-647">Verbesserte Behandlung von Ausnahmen in Cortex-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="31e1b-647">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="31e1b-648">Neue Generationen und SKUs für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="31e1b-648">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="31e1b-649">Einführung neuer Generationen für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="31e1b-649">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="31e1b-650">Einführung neuer SKUs mit höherem Durchsatz für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="31e1b-650">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="31e1b-651">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="31e1b-651">Az.RedisCache</span></span>
* <span data-ttu-id="31e1b-652">Referenzdokumentation zu „Set-AzRedisCache“ aktualisiert, um fehlende Werte für den Parameter „-Size“ aufzunehmen</span><span class="sxs-lookup"><span data-stu-id="31e1b-652">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="31e1b-653">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31e1b-653">Az.Sql</span></span>
* <span data-ttu-id="31e1b-654">Unterstützung für das Festlegen des Active Directory-Administrators für verwaltete Instanz hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-654">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="31e1b-655">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="31e1b-655">Az.Storage</span></span>
* <span data-ttu-id="31e1b-656">Storage-Clientbibliothek auf 11.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-656">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="31e1b-657">Auflisten von Containern mit der API der Verwaltungsebene, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="31e1b-657">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="31e1b-658">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="31e1b-658">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="31e1b-659">Auflisten von Storage-Konten aus Abonnements, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="31e1b-659">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="31e1b-660">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="31e1b-660">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="31e1b-661">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="31e1b-661">Az.StorageSync</span></span>
* <span data-ttu-id="31e1b-662">Problem 9810 in „Reset-AzStorageSyncServerCertificate“ behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-662">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="31e1b-663">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="31e1b-663">Az.Websites</span></span>
* <span data-ttu-id="31e1b-664">Fehler beim Aktualisieren von ASP einer App mit „Set-AzWebApp“</span><span class="sxs-lookup"><span data-stu-id="31e1b-664">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="31e1b-665">2.7.0: September 2019</span><span class="sxs-lookup"><span data-stu-id="31e1b-665">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="31e1b-666">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="31e1b-666">Az.ApiManagement</span></span>
* <span data-ttu-id="31e1b-667">Beschreibung des Parameters „-Format“ in der Referenzdokumentation für „Set-AzApiManagementPolicy“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-667">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="31e1b-668">Verweise des veralteten Cmdlets „Update-AzApiManagementDeployment“ aus Referenzdokumentation entfernt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-668">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="31e1b-669">Verwenden Sie stattdessen „Set-AzApiManagement“.</span><span class="sxs-lookup"><span data-stu-id="31e1b-669">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="31e1b-670">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="31e1b-670">Az.Automation</span></span>
* <span data-ttu-id="31e1b-671">Tippfehler im Beispiel in der Referenzdokumentation für „Register-AzAutomationDscNode“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-671">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="31e1b-672">Erläuterung zur Betriebssystemeinschränkung zu „Register-AzAutomationDSCNode“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-672">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="31e1b-673">Nullverweisausnahme des Cmdlets „Start-AzAutomationRunbook“ für die Option „-Wait“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="31e1b-673">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31e1b-674">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31e1b-674">Az.Compute</span></span>
* <span data-ttu-id="31e1b-675">Parameter „UploadSizeInBytes“ zu „New-AzDiskConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-675">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="31e1b-676">Inkrementeller Parameter zu „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-676">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="31e1b-677">Feature für VM mit niedriger Priorität hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="31e1b-677">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="31e1b-678">Parameter „MaxPrice“, „EvictionPolicy“ und „Priority“ zu New-AzVMConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-678">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="31e1b-679">Parameter „MaxPrice“ zu den Cmdlets „New-AzVmssConfig“, „Update-AzVM“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-679">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="31e1b-680">Fehlerbehebung für VM-Verweis für das Cmdlet „Get-AzAvailabilitySet“, wenn alle Verfügbarkeitsgruppen im Abonnement aufgelistet werden</span><span class="sxs-lookup"><span data-stu-id="31e1b-680">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="31e1b-681">Nullausnahme für „Get-AzRemoteDesktopFile“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-681">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="31e1b-682">VHD-Suchmethode für Position relativ zum Ende korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-682">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="31e1b-683">Problem mit UltraSSD für „New-AzVM“ und „Update-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-683">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="31e1b-684">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="31e1b-684">Az.DataFactory</span></span>
* <span data-ttu-id="31e1b-685">Drei neue Befehle für ADF V2 hinzugefügt: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription und Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="31e1b-685">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="31e1b-686">Version des ADF .NET SDK auf 4.1.3 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-686">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="31e1b-687">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="31e1b-687">Az.HDInsight</span></span>
* <span data-ttu-id="31e1b-688">Hinweis auf Breaking Changes hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-688">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="31e1b-689">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="31e1b-689">Az.IotHub</span></span>
* <span data-ttu-id="31e1b-690">Unterstützung zum Aufrufen eines Failovers für einen IoT-Hub zur geografisch gekoppelten Notfallwiederherstellungsregion hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-690">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="31e1b-691">Unterstützung zum Verwalten der Nachrichtenanreicherung für einen IoT-Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-691">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="31e1b-692">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="31e1b-692">New cmdlets are:</span></span>
    - <span data-ttu-id="31e1b-693">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="31e1b-693">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="31e1b-694">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="31e1b-694">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="31e1b-695">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="31e1b-695">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="31e1b-696">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="31e1b-696">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="31e1b-697">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="31e1b-697">Az.Monitor</span></span>
* <span data-ttu-id="31e1b-698">Verweis auf das aktuelle Monitor SDK, d. h. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="31e1b-698">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="31e1b-699">Geringfügige Änderungen an den Metrik-Cmdlets vorgenommen, d. h. die Einheitenenumeration unterstützt verschiedene neue Werte.</span><span class="sxs-lookup"><span data-stu-id="31e1b-699">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="31e1b-700">Dabei handelt es sich um schreibgeschützte Cmdlets, sodass keine Änderungen an der Eingabe der Cmdlets erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="31e1b-700">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="31e1b-701">Die API-Version der **ActionGroups**-Anforderungen lautet jetzt **2019-06-01** (zuvor **2018-03-01**).</span><span class="sxs-lookup"><span data-stu-id="31e1b-701">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="31e1b-702">Die Szenariotests wurden aktualisiert, um diese Änderung zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="31e1b-702">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="31e1b-703">Die Konstruktoren für die Klassen **EmailReceiver** und **WebhookReceiver** haben ein neues obligatorisches Argument hinzugefügt, d. h. einen booleschen Wert namens **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="31e1b-703">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="31e1b-704">Derzeit ist der Wert auf **false** festgelegt, damit sich dieser Breaking Change nicht auf die Cmdlets auswirkt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-704">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="31e1b-705">**HINWEIS:** Dies ist eine vorübergehende Änderung, die vom Team für Warnungen validiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="31e1b-705">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="31e1b-706">Die Reihenfolge der Argumente für den Konstruktor der Klasse **Source** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="31e1b-706">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="31e1b-707">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="31e1b-707">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="31e1b-708">Die Reihenfolge der Argumente für den Konstruktor der Klasse **AlertingAction** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="31e1b-708">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="31e1b-709">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="31e1b-709">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="31e1b-710">Unterstützung von Kriterien für dynamische Schwellwerte für Metrikwarnung v2</span><span class="sxs-lookup"><span data-stu-id="31e1b-710">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="31e1b-711">New-AzMetricAlertRuleV2Criteria: Erstellt nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="31e1b-711">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="31e1b-712">Add-AzMetricAlertRuleV2: Akzeptiert nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="31e1b-712">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="31e1b-713">Verbesserungen an den Cmdlets für geplante Abfrageregeln (Scheduled Query Rule, SQR)</span><span class="sxs-lookup"><span data-stu-id="31e1b-713">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="31e1b-714">Cmdlets akzeptieren den Parameter „Location“ in zwei Formaten: entweder den Standort (z. B. „eastus“) oder den Anzeigenamen des Standorts (z. B. „USA, Osten“)</span><span class="sxs-lookup"><span data-stu-id="31e1b-714">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="31e1b-715">Parameter „Enabled“ in Hilfedateien ordnungsgemäß dargestellt</span><span class="sxs-lookup"><span data-stu-id="31e1b-715">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="31e1b-716">Beispiele für optionalen Parameter „ActionGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-716">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="31e1b-717">Hilfedateien insgesamt verbessert</span><span class="sxs-lookup"><span data-stu-id="31e1b-717">Overall improved help files</span></span>
* <span data-ttu-id="31e1b-718">Fehler beim Bestimmen des Bereichstyps für „Set-AzActionRule“ behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-718">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31e1b-719">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31e1b-719">Az.Network</span></span>
* <span data-ttu-id="31e1b-720">Fehlerhaftes Beispiel in der Referenzdokumentation zu „New-AzApplicationGateway“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-720">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="31e1b-721">Hinweis in der Referenzdokumentation zu „Get-AzNetworkWatcherPacketCapture“ zum Abrufen aller Eigenschaften für eine Paketerfassung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-721">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="31e1b-722">Beispiel in der Referenzdokumentation zu „Test-AzNetworkWatcherIPFlow“ korrigiert, um die Netzwerkadapter ordnungsgemäß aufzulisten</span><span class="sxs-lookup"><span data-stu-id="31e1b-722">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="31e1b-723">Cloudausnahmeanalyse verbessert, um ggf. zusätzliche Details anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="31e1b-723">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="31e1b-724">Cloudausnahmeanalyse verbessert, um zusätzlichen Typ der SDK-Ausnahme zu verarbeiten</span><span class="sxs-lookup"><span data-stu-id="31e1b-724">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="31e1b-725">Falsche Zuordnung der Sicherheitsregelmodelle korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-725">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="31e1b-726">Eigenschaften zur Netzwerkschnittstelle für das Feature für die private IP-Adresse hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-726">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="31e1b-727">Eigenschaft „PrivateEndpoint“ als Typ „PSResourceId“ zu „PSNetworkInterface“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-727">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="31e1b-728">Eigenschaft „PrivateLinkConnectionProperties“ als Typ „PSIpConfigurationConnectivityInformation“ zu „PSNetworkInterfaceIPConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-728">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="31e1b-729">Neue Modellklasse „PSIpConfigurationConnectivityInformation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-729">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="31e1b-730">Neues ApplicationRuleProtocolType-Element „mssql“ für Azure Firewall-Ressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-730">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="31e1b-731">Unterstützung von Mehrfachverbindungen in Virtual WAN</span><span class="sxs-lookup"><span data-stu-id="31e1b-731">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="31e1b-732">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="31e1b-732">New cmdlets</span></span>
        - <span data-ttu-id="31e1b-733">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="31e1b-733">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="31e1b-734">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="31e1b-734">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="31e1b-735">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="31e1b-735">Updated cmdlet:</span></span>
        - <span data-ttu-id="31e1b-736">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="31e1b-736">New-VpnSite</span></span>
        - <span data-ttu-id="31e1b-737">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="31e1b-737">Update-VpnSite</span></span>
        - <span data-ttu-id="31e1b-738">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="31e1b-738">New-VpnConnection</span></span>
        - <span data-ttu-id="31e1b-739">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="31e1b-739">Update-VpnConnection</span></span>
* <span data-ttu-id="31e1b-740">Dokumente für einige PowerShell-Beispiele korrigiert, sodass Az-Cmdlets anstelle von AzureRM-Cmdlets verwendet werden</span><span class="sxs-lookup"><span data-stu-id="31e1b-740">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="31e1b-741">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="31e1b-741">Az.RecoveryServices</span></span>
* <span data-ttu-id="31e1b-742">AzureVMpolicy-Objekt mit ProtectedItemsCount-Attribut aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-742">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="31e1b-743">Tests für VM-Richtlinie und Wiederherstellung des ursprünglichen Speicherkontos hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-743">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="31e1b-744">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31e1b-744">Az.Resources</span></span>
* <span data-ttu-id="31e1b-745">Fehler behoben, aufgrund dessen „New-AzRoleAssignment“ nicht ohne den Parameter „Scope“ aufgerufen werden konnte</span><span class="sxs-lookup"><span data-stu-id="31e1b-745">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="31e1b-746">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="31e1b-746">Az.ServiceFabric</span></span>
* <span data-ttu-id="31e1b-747">Tippfehler im Beispiel für die Referenzdokumentation „Update-AzServiceFabricReliability“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-747">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="31e1b-748">Neue Cmdlets zum Verwalten von Anwendung und Diensten hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="31e1b-748">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="31e1b-749">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="31e1b-749">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="31e1b-750">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="31e1b-750">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="31e1b-751">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="31e1b-751">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="31e1b-752">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="31e1b-752">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="31e1b-753">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="31e1b-753">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="31e1b-754">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="31e1b-754">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="31e1b-755">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="31e1b-755">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="31e1b-756">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="31e1b-756">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="31e1b-757">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="31e1b-757">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="31e1b-758">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="31e1b-758">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="31e1b-759">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="31e1b-759">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="31e1b-760">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="31e1b-760">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="31e1b-761">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="31e1b-761">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="31e1b-762">Service Fabric SDK auf Version 1.2.0 aktualisiert, die API-Version 2019-03-01 des Service Fabric-Ressourcenanbieters verwendet</span><span class="sxs-lookup"><span data-stu-id="31e1b-762">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="31e1b-763">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="31e1b-763">Az.SignalR</span></span>
* <span data-ttu-id="31e1b-764">Cmdlets „Update“, „Restart“, „CheckNameAvailability“ und „GetUsage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-764">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="31e1b-765">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31e1b-765">Az.Sql</span></span>
* <span data-ttu-id="31e1b-766">Beispiel in der Referenzdokumentation für „Get-AzSqlElasticPool“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-766">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="31e1b-767">V-Kern-Beispiel zum Erstellen eines Pools für elastische Datenbanken hinzugefügt (New-AzSqlElasticPool)</span><span class="sxs-lookup"><span data-stu-id="31e1b-767">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="31e1b-768">Überprüfung von „EmailAddresses“ sowie Validierung, dass „EmailAdmins“ nicht auf „false“ festgelegt ist, in „Set-AzSqlServerAdvancedThreatProtectionPolicy“ und „Set-AzSqlDatabaseAdvancedThreatProtectionPolicy“ entfernt, wenn „EmailAddresses“ leer ist</span><span class="sxs-lookup"><span data-stu-id="31e1b-768">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="31e1b-769">Entfernen der Einstellungen für Server-/Datenbanküberwachung aktiviert, wenn mehrere Diagnoseeinstellungen vorhanden sind, die eine Überwachungskategorie ermöglichen</span><span class="sxs-lookup"><span data-stu-id="31e1b-769">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="31e1b-770">Überprüfung von E-Mail-Adressen in mehreren Cmdlets für die SQL-Sicherheitsrisikobewertung korrigiert (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting und Update-AzSqlInstanceVulnerabilityAssessmentSetting)</span><span class="sxs-lookup"><span data-stu-id="31e1b-770">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="31e1b-771">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="31e1b-771">Az.Storage</span></span>
* <span data-ttu-id="31e1b-772">Beispiel in der Referenzdokumentation für „Get-AzStorageAccountKey“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-772">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="31e1b-773">Beim Upload/Download von Azure-Dateien wird das Beibehalten der SMB-Eigenschaften der Quelldateien (Dateiattribute, Zeitpunkt der Dateierstellung, letzter Schreibzugriff für die Datei) in der Zieldatei unterstützt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-773">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="31e1b-774">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="31e1b-774">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="31e1b-775">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="31e1b-775">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="31e1b-776">Fehler beim Hochladen von Blockblobs mit Eigenschaften/Metadaten für das für einen Container aktivierte ImmutabilityPolicy-Element behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-776">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="31e1b-777">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="31e1b-777">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="31e1b-778">Unterstützung für die Verwaltung von Azure-Dateifreigaben mit der API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="31e1b-778">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="31e1b-779">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="31e1b-779">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="31e1b-780">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="31e1b-780">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="31e1b-781">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="31e1b-781">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="31e1b-782">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="31e1b-782">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="31e1b-783">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="31e1b-783">Az.Websites</span></span>
* <span data-ttu-id="31e1b-784">Problem behoben, aufgrund dessen webapp-Tags beim Migrieren der App zu neuem ASP gelöscht wurden</span><span class="sxs-lookup"><span data-stu-id="31e1b-784">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="31e1b-785">„Publish-AzureWebapp“ für die Verwendung unter Linux und Windows korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-785">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="31e1b-786">Beispiel in Referenzdokumentation „Get-AzWebAppPublishingProfile“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-786">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="31e1b-787">2.6.0: August 2019</span><span class="sxs-lookup"><span data-stu-id="31e1b-787">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="31e1b-788">Allgemein</span><span class="sxs-lookup"><span data-stu-id="31e1b-788">General</span></span>
* <span data-ttu-id="31e1b-789">Verschiedene Tippfehler in zahlreichen Modulen korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-789">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="31e1b-790">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="31e1b-790">Az.Accounts</span></span>
* <span data-ttu-id="31e1b-791">Unterstützung der benutzerseitig zugewiesenen MSI in Azure Functions-Authentifizierung (#9479)</span><span class="sxs-lookup"><span data-stu-id="31e1b-791">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="31e1b-792">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="31e1b-792">Az.Aks</span></span>
* <span data-ttu-id="31e1b-793">Problem mit der Ausgabe für „Get-AzAks“ behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-793">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="31e1b-794">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="31e1b-794">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="31e1b-795">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="31e1b-795">Az.ApiManagement</span></span>
* <span data-ttu-id="31e1b-796">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="31e1b-796">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="31e1b-797">.NET-NuGet-Version aktualisiert, die keine Einschränkungen für „productId“, „apiId“, „groupId“ und „userId“ erzwingt</span><span class="sxs-lookup"><span data-stu-id="31e1b-797">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="31e1b-798">**Get-AzApiManagementProduct:** Unterstützung für das Abfragen von Produkten mithilfe der API hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-798">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="31e1b-799">**New-AzApiManagementApiRevision:** Problem behoben, aufgrund dessen „ApiRevisionDescription“ beim Erstellen einer neuen API-Revision nicht festgelegt wurde https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="31e1b-799">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="31e1b-800">Tippfehler im Modell „PsApiManagementOAuth2AuthrozationServer“ korrigiert: PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="31e1b-800">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="31e1b-801">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="31e1b-801">Az.Batch</span></span>
* <span data-ttu-id="31e1b-802">Tippfehler in Hilfemeldung und Dokumentation korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="31e1b-802">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="31e1b-803">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="31e1b-803">Az.Cdn</span></span>
* <span data-ttu-id="31e1b-804">Tippfehler im Hilfsprogramm für die CDN-Modulkonvertierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-804">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31e1b-805">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31e1b-805">Az.Compute</span></span>
* <span data-ttu-id="31e1b-806">VmssId zum Cmdlet „New-AzVMConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-806">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="31e1b-807">Parameter „TerminateScheduledEvents“ und „TerminateScheduledEventNotBeforeTimeoutInMinutes“ zu „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-807">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="31e1b-808">HyperVGeneration-Eigenschaft zu VM-Imageobjekt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-808">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="31e1b-809">Host- und HostGroup-Features hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-809">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="31e1b-810">Neue Cmdlets:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="31e1b-810">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="31e1b-811">Parameter „HostId“ zu „New-AzVMConfig“ und „New-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-811">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="31e1b-812">Beispiel in der Dokumentation zu „Invoke-AzVMRunCommand“ zur Verwendung des richtigen Parameternamens aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-812">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="31e1b-813">Beschreibung für „-VolumeType“ in der Referenzdokumentation zu „Set-AzVMDiskEncryptionExtension“ und „Set-AzVmssDiskEncryptionExtension“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-813">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="31e1b-814">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="31e1b-814">Az.DataFactory</span></span>
* <span data-ttu-id="31e1b-815">Tippfehler in der Dokumentation zu „New-AzDataFactoryEncryptValue“ korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="31e1b-815">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="31e1b-816">Version des ADF .NET SDK auf 4.1.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-816">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="31e1b-817">Parameter „DataProxyIntegrationRuntimeName“, „DataProxyStagingLinkedServiceName“ und „DataProxyStagingPath“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um die Einrichtung der selbstgehosteten Integration Runtime als Proxy für die SSIS Integration Runtime zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="31e1b-817">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="31e1b-818">„PSTriggerRun“ zum Anzeigen der ausgelösten Pipelines, Meldungen und Eigenschaften und „PSActivityRun“ zum Anzeigen des Aktivitätstyps aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-818">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="31e1b-819">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="31e1b-819">Az.DataLakeStore</span></span>
* <span data-ttu-id="31e1b-820">Hängen von „Get-DataLakeStoreDeletedItem“ aufgrund von Fehlern oder Remoteausnahmen behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-820">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="31e1b-821">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="31e1b-821">Az.EventHub</span></span>
* <span data-ttu-id="31e1b-822">Behebung des Problems #9658: Tippfehler im Parameter „VirtualNteworkRule“ in „Set-AzEventHubNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="31e1b-822">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="31e1b-823">Behebung des Problems #9558: „Set-AzEventHubNamespace“ verwendet PATCH anstelle von PUT.</span><span class="sxs-lookup"><span data-stu-id="31e1b-823">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="31e1b-824">Parameter „EnableKafka“ zum Cmdlet „Set-AzEventHubNamespace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-824">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="31e1b-825">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="31e1b-825">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="31e1b-826">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="31e1b-826">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="31e1b-827">Tippfehler („Azure“ in Kleinbuchstaben) in der Dokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-827">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="31e1b-828">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="31e1b-828">Az.Monitor</span></span>
* <span data-ttu-id="31e1b-829">Falscher Parametername in der Hilfedokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-829">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31e1b-830">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31e1b-830">Az.Network</span></span>
* <span data-ttu-id="31e1b-831">„New-AzPrivateLinkServiceIpConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-831">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="31e1b-832">Parameter „PublicIpAddress“ ausgemustert, da er auf Serverseite nie verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="31e1b-832">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="31e1b-833">Optionaler Parameter „Primary“ hinzugefügt, der angibt, ob die aktuelle IP-Konfiguration die primäre ist oder nicht</span><span class="sxs-lookup"><span data-stu-id="31e1b-833">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="31e1b-834">Verbesserte Verarbeitung der Anforderungsfehlerausnahme aus dem SDK: Behebt das Problem, dass vorherige SDK-Ausnahmen nicht richtig behandelt wurden, was dazu führt, dass Schlüsselfehlerdetails nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="31e1b-834">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="31e1b-835">Validierungslogik für Ipv6-IP-Präfix angepasst, damit auf die richtige IPv6-Präfixlänge geprüft wird</span><span class="sxs-lookup"><span data-stu-id="31e1b-835">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="31e1b-836">„Get-AzVirtualNetworkSubnetConfig“ aktualisiert: Parametersatz zum Abrufen nach Subnetzressourcen-ID hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-836">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="31e1b-837">Aktualisierte Beschreibung des Location-Parameters für „AzNetworkServiceTag“</span><span class="sxs-lookup"><span data-stu-id="31e1b-837">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="31e1b-838">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="31e1b-838">Az.OperationalInsights</span></span>
* <span data-ttu-id="31e1b-839">Aktualisierte Dokumentation für „New-AzOperationalInsightsLinuxSyslogDataSource“</span><span class="sxs-lookup"><span data-stu-id="31e1b-839">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="31e1b-840">Beispiel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-840">Added example</span></span>
    - <span data-ttu-id="31e1b-841">Beschreibung für den Parameter „-Name“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-841">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="31e1b-842">Beispiel für „New-AzOperationalInsightsWindowsEventDataSource“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-842">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="31e1b-843">Beschreibung des Parameters „-Name“ für „New-AzOperationalInsightsWindowsEventDataSource“ geändert</span><span class="sxs-lookup"><span data-stu-id="31e1b-843">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="31e1b-844">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="31e1b-844">Az.RecoveryServices</span></span>
* <span data-ttu-id="31e1b-845">„Get-AzRecoveryServicesBackupJobDetail.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-845">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="31e1b-846">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31e1b-846">Az.Resources</span></span>
* <span data-ttu-id="31e1b-847">Unterstützung für die neue API-Version 2019-05-10 für Microsoft.Resource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-847">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="31e1b-848">Unterstützung für „copy.count = 0“ für Variablen, Ressourcen und Eigenschaften hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-848">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="31e1b-849">Ressourcen mit „condition = false“ oder „copy.count = 0“ werden im vollständigen Modus gelöscht.</span><span class="sxs-lookup"><span data-stu-id="31e1b-849">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="31e1b-850">Beispiel zum Hinzufügen einer Richtlinie auf Abonnementebene zur Hilfedokumentation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-850">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="31e1b-851">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="31e1b-851">Az.ServiceBus</span></span>
* <span data-ttu-id="31e1b-852">Behebung des Problems #9658: Tippfehler für Parameter „VirtualNetworkRule“ in „Set-AzServiceBusNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="31e1b-852">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="31e1b-853">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="31e1b-853">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="31e1b-854">Neuer Befehl „Test-AzServiceBusNameAvailability“ zum Überprüfen der Verfügbarkeit des Namens für Warteschlange und Thema hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-854">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="31e1b-855">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="31e1b-855">Az.ServiceFabric</span></span>
* <span data-ttu-id="31e1b-856">Fehler bei Cmdlets zum Hinzufügen des Knotentyps korrigiert:</span><span class="sxs-lookup"><span data-stu-id="31e1b-856">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="31e1b-857">Fehler „NullReferenceException“, wenn die Ressourcengruppe andere VMSS enthielt, die nicht mit dem Service Fabric-Cluster in Zusammenhang stehen</span><span class="sxs-lookup"><span data-stu-id="31e1b-857">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="31e1b-858">Problembehebung: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="31e1b-858">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="31e1b-859">Fehler behoben, aufgrund dessen bei einem Cmdlet ein Fehler auftrat, wenn sich „virtualNetwork“ in einer anderen Ressourcengruppe befand als der Cluster</span><span class="sxs-lookup"><span data-stu-id="31e1b-859">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="31e1b-860">Problembehebung: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="31e1b-860">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="31e1b-861">Cmdlet „Add-AzServiceFabricApplicationCertificate“ ausgemustert</span><span class="sxs-lookup"><span data-stu-id="31e1b-861">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="31e1b-862">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31e1b-862">Az.Sql</span></span>
* <span data-ttu-id="31e1b-863">Dokumentation alter Überwachungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-863">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="31e1b-864">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="31e1b-864">Az.Storage</span></span>
* <span data-ttu-id="31e1b-865">Hilfe für „Get/Close-AzStorageFileHandle“ aktualisiert (weitere Szenarien zu Cmdlet-Beispielen hinzugefügt und Parameterbeschreibungen aktualisiert)</span><span class="sxs-lookup"><span data-stu-id="31e1b-865">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="31e1b-866">Unterstützung von „StandardBlobTier“ in Uploadblobs und Kopierblobs</span><span class="sxs-lookup"><span data-stu-id="31e1b-866">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="31e1b-867">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="31e1b-867">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="31e1b-868">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="31e1b-868">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="31e1b-869">Unterstützung der Aktivierungspriorität im Kopierblob</span><span class="sxs-lookup"><span data-stu-id="31e1b-869">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="31e1b-870">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="31e1b-870">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="31e1b-871">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="31e1b-871">Az.Websites</span></span>
* <span data-ttu-id="31e1b-872">Hinzufügen von Erläuterungen zum Parameter „-AppSettings“ in „Set-AzWebApp“ und „Set-AzWebAppSlot“</span><span class="sxs-lookup"><span data-stu-id="31e1b-872">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="31e1b-873">2.5.0: Juli 2019</span><span class="sxs-lookup"><span data-stu-id="31e1b-873">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="31e1b-874">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="31e1b-874">Az.Accounts</span></span>
* <span data-ttu-id="31e1b-875">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="31e1b-875">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="31e1b-876">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="31e1b-876">Az.ApplicationInsights</span></span>
* <span data-ttu-id="31e1b-877">Tippfehler im Beispiel in der Dokumentation zu „Remove-AzApplicationInsightsApiKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-877">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="31e1b-878">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="31e1b-878">Az.Automation</span></span>
* <span data-ttu-id="31e1b-879">Tippfehler in der Ressourcenzeichenfolge korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-879">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="31e1b-880">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="31e1b-880">Az.CognitiveServices</span></span>
* <span data-ttu-id="31e1b-881">Unterstützung für NetworkRuleSet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-881">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31e1b-882">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31e1b-882">Az.Compute</span></span>
* <span data-ttu-id="31e1b-883">Fehlende Eigenschaften (ComputerName, OsName, OsVersion und HyperVGeneration) des Objekts für die VM-Instanzenansicht hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-883">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="31e1b-884">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="31e1b-884">Az.ContainerRegistry</span></span>
* <span data-ttu-id="31e1b-885">Tippfehler in „Remove-AzContainerRegistryReplication“ für den Replikationsparameter korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-885">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="31e1b-886">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="31e1b-886">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="31e1b-887">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="31e1b-887">Az.DataFactory</span></span>
* <span data-ttu-id="31e1b-888">Version des ADF .NET SDK auf 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-888">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="31e1b-889">Tippfehler in der Dokumentation für „Get-AzDataFactoryV2PipelineRun“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-889">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="31e1b-890">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="31e1b-890">Az.EventHub</span></span>
* <span data-ttu-id="31e1b-891">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="31e1b-891">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="31e1b-892">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="31e1b-892">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="31e1b-893">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="31e1b-893">Az.KeyVault</span></span>
* <span data-ttu-id="31e1b-894">Unterstützung zum Angeben von KeySize für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-894">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="31e1b-895">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="31e1b-895">Az.LogicApp</span></span>
* <span data-ttu-id="31e1b-896">Korrektur für „Get-AzIntegrationAccountMap“ zum Auflisten aller Zuordnungstypen</span><span class="sxs-lookup"><span data-stu-id="31e1b-896">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="31e1b-897">Neuer MapType-Parameter für Filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-897">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="31e1b-898">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="31e1b-898">Az.ManagedServices</span></span>
* <span data-ttu-id="31e1b-899">Unterstützung für API-Version 2019-06-01 (GA) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-899">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31e1b-900">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31e1b-900">Az.Network</span></span>
* <span data-ttu-id="31e1b-901">Unterstützung für privaten Endpunkt und privaten Verknüpfungsdienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-901">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="31e1b-902">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="31e1b-902">New cmdlets</span></span>
        - <span data-ttu-id="31e1b-903">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="31e1b-903">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="31e1b-904">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="31e1b-904">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="31e1b-905">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="31e1b-905">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="31e1b-906">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="31e1b-906">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="31e1b-907">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="31e1b-907">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="31e1b-908">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="31e1b-908">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="31e1b-909">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="31e1b-909">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="31e1b-910">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="31e1b-910">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="31e1b-911">Folgende Befehle für das Feature aktualisiert: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies für Subnetz in VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="31e1b-911">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="31e1b-912">„New-AzVirtualNetworkSubnetConfig“, „Set-AzVirtualNetworkSubnetConfig“ und „Add-AzVirtualNetworkSubnetConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-912">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="31e1b-913">Optionaler Parameter „-PrivateEndpointNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den privaten Endpunkt in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="31e1b-913">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="31e1b-914">Optionaler Parameter „-PrivateLinkServiceNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den Privat Link-Dienst in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="31e1b-914">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="31e1b-915">Der Cmdlet-Parameter „ServiceName“ von AzPrivateLinkService wurde aus Gründen der Abwärtskompatibilität in „Name“ mit dem Alias „ServiceName“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-915">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="31e1b-916">ICMP-Protokoll für Konfigurationen von Netzwerksicherheitsregeln aktiviert</span><span class="sxs-lookup"><span data-stu-id="31e1b-916">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="31e1b-917">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="31e1b-917">Updated cmdlets</span></span>
        - <span data-ttu-id="31e1b-918">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="31e1b-918">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="31e1b-919">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="31e1b-919">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="31e1b-920">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="31e1b-920">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="31e1b-921">ConnectionProtocolType (Ikev1/Ikev2) als konfigurierbarer Parameter für „New-AzVirtualNetworkGatewayConnection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-921">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="31e1b-922">PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-922">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="31e1b-923">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="31e1b-923">Updated cmdlet:</span></span>
        - <span data-ttu-id="31e1b-924">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="31e1b-924">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="31e1b-925">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="31e1b-925">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="31e1b-926">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="31e1b-926">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="31e1b-927">Application Gateway-Befehl „New-AzApplicationGatewayProbeConfig“ zur Unterstützung des benutzerdefinierten Ports im Test aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-927">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="31e1b-928">„New-AzApplicationGatewayProbeConfig“ aktualisiert: Optionaler Parameter „Port“ hinzugefügt, der zum Testen des Back-End-Servers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="31e1b-928">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="31e1b-929">Dieser Parameter gilt für Standard_V2 und WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="31e1b-929">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="31e1b-930">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="31e1b-930">Az.OperationalInsights</span></span>
* <span data-ttu-id="31e1b-931">Standardversion für gespeicherte Suchvorgänge auf 1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-931">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="31e1b-932">Verarbeitung des regulären NULL-Ausdrucks in benutzerdefinierten Protokollen korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-932">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="31e1b-933">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="31e1b-933">Az.RecoveryServices</span></span>
* <span data-ttu-id="31e1b-934">„Get-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-934">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="31e1b-935">„Get-AzRecoveryServicesBackupContainer.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-935">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="31e1b-936">„Get-AzRecoveryServicesVault.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-936">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="31e1b-937">„Wait-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-937">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="31e1b-938">„Set-AzRecoveryServicesVaultContext.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-938">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="31e1b-939">„Get-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-939">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="31e1b-940">„Get-AzRecoveryServicesBackupRecoveryPoint.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-940">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="31e1b-941">„Restore-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-941">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="31e1b-942">Dienstaufruf zum Aufheben der Containerregistrierung für Azure-Dateifreigabe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-942">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="31e1b-943">„Set-AzRecoveryServicesAsrAlertSetting.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-943">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="31e1b-944">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31e1b-944">Az.Resources</span></span>
- <span data-ttu-id="31e1b-945">Fehlendes Cmdlet entfernt, auf das in der Dokumentation zu „New-AzResourceGroupDeployment“ verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="31e1b-945">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="31e1b-946">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-946">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="31e1b-947">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="31e1b-947">Az.ServiceBus</span></span>
* <span data-ttu-id="31e1b-948">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="31e1b-948">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="31e1b-949">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="31e1b-949">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="31e1b-950">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31e1b-950">Az.Sql</span></span>
* <span data-ttu-id="31e1b-951">Fehlende Beispiele für Cmdlet „Set-AzSqlDatabaseSecondary“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-951">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="31e1b-952">Festlegen wiederkehrender Überprüfungen der Sicherheitsrisikobewertung ohne Angabe von E-Mail-Adressen korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-952">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="31e1b-953">Tippfehler in einer Warnmeldung korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-953">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="31e1b-954">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="31e1b-954">Az.Storage</span></span>
* <span data-ttu-id="31e1b-955">Beispiel in Referenzdokumentation für „Get-AzStorageAccount“ aktualisiert, sodass der richtige Parametername verwendet wird</span><span class="sxs-lookup"><span data-stu-id="31e1b-955">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="31e1b-956">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="31e1b-956">Az.StorageSync</span></span>
* <span data-ttu-id="31e1b-957">Cmdlet „Invoke-AzStorageSyncChangeDetection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-957">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="31e1b-958">Problem 9551 zur Berücksichtigung von „TierFilesOlderThanDays“ behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-958">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="31e1b-959">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="31e1b-959">Az.Websites</span></span>
* <span data-ttu-id="31e1b-960">Problem behoben, aufgrund dessen einige SiteConfig-Eigenschaften von „Get-AzWebApp“ und „Set-AzWebApp“ nicht zurückgegeben wurden</span><span class="sxs-lookup"><span data-stu-id="31e1b-960">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="31e1b-961">Neuer Standortparameter zu „Get-AzDeletedWebApp“ und „Restore-AzDeletedWebApp“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-961">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="31e1b-962">Fehler beim Klonen von Web-App-Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-962">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="31e1b-963">2.4.0 – Juli 2019</span><span class="sxs-lookup"><span data-stu-id="31e1b-963">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="31e1b-964">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="31e1b-964">Az.Accounts</span></span>
* <span data-ttu-id="31e1b-965">Unterstützung für Profil-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-965">Add support for profile cmdlets</span></span>
* <span data-ttu-id="31e1b-966">Unterstützung für Umgebungen und Datenebenen in generierten Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-966">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="31e1b-967">Korrektur eines Fehlers, bei dem in einigen Fällen ein falscher Endpunkt für Datenebenen-Cmdlets in Windows PowerShell verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="31e1b-967">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="31e1b-968">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="31e1b-968">Az.Advisor</span></span>
* <span data-ttu-id="31e1b-969">Allgemein verfügbares Release von Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="31e1b-969">GA release of Az.Advisor</span></span>
* <span data-ttu-id="31e1b-970">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="31e1b-970">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="31e1b-971">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="31e1b-971">Az.ApiManagement</span></span>
* <span data-ttu-id="31e1b-972">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="31e1b-972">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="31e1b-973">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="31e1b-973">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="31e1b-974">Unterstützung für Abfragen von Abonnements nach Benutzer und Produkt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-974">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="31e1b-975">Unterstützung für Abfragen anhand des Umfangs hinzugefügt, „/“, „/apis“, „/apis/echo-api“</span><span class="sxs-lookup"><span data-stu-id="31e1b-975">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="31e1b-976">Behebung von Problem https://github.com/Azure/azure-powershell/issues/9307 und https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="31e1b-976">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="31e1b-977">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="31e1b-977">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="31e1b-978">Unterstützung für die Angabe von „ApiVersion“ und „ApiVersionSetId“ beim Importieren von APIs hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-978">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="31e1b-979">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="31e1b-979">Az.Automation</span></span>
* <span data-ttu-id="31e1b-980">Fehler beim Cmdlet „Set-AzAutomationConnectionFieldValue“ für die Verarbeitung des Zeichenfolgewerts behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-980">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31e1b-981">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31e1b-981">Az.Compute</span></span>
* <span data-ttu-id="31e1b-982">Parameter „HyperVGeneration“ zu New-AzImageConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-982">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="31e1b-983">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="31e1b-983">Az.DataFactory</span></span>
* <span data-ttu-id="31e1b-984">Aktualisierung der Ausgabe von ADF-Cmdlets für das Abrufen von Aktivitäts-, Pipeline- und Auslöserausführungen, um die Pipe „Select-Object“ zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="31e1b-984">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="31e1b-985">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="31e1b-985">Az.EventGrid</span></span>
* <span data-ttu-id="31e1b-986">Tippfehler in Dokumentation zu 'New-AzEventGridSubscription' behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-986">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="31e1b-987">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="31e1b-987">Az.IotHub</span></span>
* <span data-ttu-id="31e1b-988">Unterstützung für das erneute Generieren von Autorisierungsrichtlinienschlüsseln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-988">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31e1b-989">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31e1b-989">Az.Network</span></span>
* <span data-ttu-id="31e1b-990">„RoutingPreference“ zu öffentlichen IP-Tags hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-990">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="31e1b-991">Beispiele für Referenzdokumentation zu „Get-AzNetworkServiceTag“ verbessert</span><span class="sxs-lookup"><span data-stu-id="31e1b-991">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="31e1b-992">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="31e1b-992">Az.PolicyInsights</span></span>
* <span data-ttu-id="31e1b-993">Fehlerbehebung für Nullverweis in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="31e1b-993">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="31e1b-994">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="31e1b-994">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="31e1b-995">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="31e1b-995">Az.OperationalInsights</span></span>
* <span data-ttu-id="31e1b-996">Zurückgegebenes CustomLog-Datenquellenmodell in Get-AzOperationalInsightsDataSource korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-996">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="31e1b-997">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="31e1b-997">Az.RecoveryServices</span></span>
* <span data-ttu-id="31e1b-998">Fehlerbehebung für Befehl „get-policy“ IaaSVMs</span><span class="sxs-lookup"><span data-stu-id="31e1b-998">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="31e1b-999">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31e1b-999">Az.Resources</span></span>
    - <span data-ttu-id="31e1b-1000">Hilfetext für Parameter „-Top“ von „Get-AzPolicyState“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1000">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="31e1b-1001">Clientseitige Unterstützung von Paginierung für „Get-AzPolicyAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1001">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="31e1b-1002">Neue Parameter für „Set-AzPolicyAssignment“, „-PolicyParameters“ und „-PolicyParametersObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1002">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="31e1b-1003">Einige Aktualisierungen von Dokumentationen und Beispielen für Policy-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="31e1b-1003">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="31e1b-1004">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="31e1b-1004">Az.ServiceBus</span></span>
* <span data-ttu-id="31e1b-1005">Korrektur für Problem Nr. 4938: „New-AzureRmServiceBusQueue“ gibt beim Festlegen von „MaxSizeInMegabytes“ „BadRequest“ zurück</span><span class="sxs-lookup"><span data-stu-id="31e1b-1005">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="31e1b-1006">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31e1b-1006">Az.Sql</span></span>
* <span data-ttu-id="31e1b-1007">Instanzfailovergruppen-Cmdlets aus Vorschauversion in öffentliche Version hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1007">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="31e1b-1008">Unterstützung von Azure SQL Server\Datenbanküberwachung mit neuen Cmdlets</span><span class="sxs-lookup"><span data-stu-id="31e1b-1008">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="31e1b-1009">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="31e1b-1009">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="31e1b-1010">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="31e1b-1010">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="31e1b-1011">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="31e1b-1011">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="31e1b-1012">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="31e1b-1012">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="31e1b-1013">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="31e1b-1013">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="31e1b-1014">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="31e1b-1014">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="31e1b-1015">E-Mail-Einschränkungen aus Einstellungen der Sicherheitsrisikobewertung entfernt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1015">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="31e1b-1016">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="31e1b-1016">Az.Storage</span></span>
* <span data-ttu-id="31e1b-1017">Zwei Parameter („-IndexDocument“ und „-ErrorDocument404Path“) in folgendem Cmdlet von erforderlich in optional geändert:</span><span class="sxs-lookup"><span data-stu-id="31e1b-1017">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="31e1b-1018">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="31e1b-1018">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="31e1b-1019">Hilfe zu „Get-AzStorageBlobContent“ mit neuem Beispiel ergänzt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1019">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="31e1b-1020">Anzeige von mehr Fehlerinformationen beim Fehlschlagen eines Cmdlets mit „StorageException“</span><span class="sxs-lookup"><span data-stu-id="31e1b-1020">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="31e1b-1021">Unterstützung für das Erstellen oder Aktualisieren von Speicherkonten mit Azure Files AAD-DS-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="31e1b-1021">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="31e1b-1022">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="31e1b-1022">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="31e1b-1023">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="31e1b-1023">Set-AzStorageAccount</span></span>
* <span data-ttu-id="31e1b-1024">Unterstützung für das Auflisten oder Schließen von Dateihandles einer Dateifreigabe, eines Dateiverzeichnisses oder einer Datei</span><span class="sxs-lookup"><span data-stu-id="31e1b-1024">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="31e1b-1025">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="31e1b-1025">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="31e1b-1026">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="31e1b-1026">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="31e1b-1027">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="31e1b-1027">Az.StorageSync</span></span>
* <span data-ttu-id="31e1b-1028">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1028">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="31e1b-1029">2.3.2 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="31e1b-1029">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="31e1b-1030">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="31e1b-1030">Az.Accounts</span></span>
* <span data-ttu-id="31e1b-1031">Fehler behoben, aufgrund dessen in manchen Fällen eine falsche URL für Funktionsaufrufe verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="31e1b-1031">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="31e1b-1032">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="31e1b-1032">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="31e1b-1033">Problem mit Aliasen zwischen AzureRM und Azure-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-1033">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="31e1b-1034">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="31e1b-1034">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="31e1b-1035">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="31e1b-1035">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31e1b-1036">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31e1b-1036">Az.Compute</span></span>
* <span data-ttu-id="31e1b-1037">Die einfachen Parametersätze „New-AzVm“ und „New-AzVmss“ akzeptieren jetzt den Parameter „ProximityPlacementGroup“.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1037">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="31e1b-1038">Tippfehler in der Referenzdokumentation für „New-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-1038">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="31e1b-1039">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="31e1b-1039">Az.Dns</span></span>
* <span data-ttu-id="31e1b-1040">Tippfehler in den Hilfebeispielen zu „Set-AzDnsZone“ behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-1040">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="31e1b-1041">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="31e1b-1041">Az.EventGrid</span></span>
* <span data-ttu-id="31e1b-1042">Zur Verwendung der API-Version 2019-06-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1042">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="31e1b-1043">Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="31e1b-1043">New cmdlets:</span></span>
    - <span data-ttu-id="31e1b-1044">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="31e1b-1044">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="31e1b-1045">Erstellt eine neue Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1045">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="31e1b-1046">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="31e1b-1046">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="31e1b-1047">Ruft die Details einer Event Grid-Domäne oder eine Liste aller Event Grid-Domänen im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1047">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="31e1b-1048">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="31e1b-1048">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="31e1b-1049">Entfernt eine Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1049">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="31e1b-1050">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="31e1b-1050">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="31e1b-1051">Generiert den freigegebenen Zugriffsschlüssel für eine Azure Event Grid-Domäne erneut.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1051">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="31e1b-1052">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="31e1b-1052">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="31e1b-1053">Ruft die freigegebenen Zugriffsschlüssel ab, die zum Veröffentlichen von Ereignissen in einer Event Grid-Domäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1053">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="31e1b-1054">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="31e1b-1054">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="31e1b-1055">Erstellt ein neues Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1055">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="31e1b-1056">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="31e1b-1056">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="31e1b-1057">Ruft die Details eines Event Grid-Domänenthemas oder eine Liste aller Event Grid-Domänenthemen unter der jeweiligen Event Grid-Domäne im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1057">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="31e1b-1058">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="31e1b-1058">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="31e1b-1059">Entfernt ein vorhandenes Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1059">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="31e1b-1060">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="31e1b-1060">Updated cmdlets:</span></span>
    - <span data-ttu-id="31e1b-1061">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="31e1b-1061">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="31e1b-1062">Neue erforderliche Parameter zur Unterstützung des Pipings für die neue Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="31e1b-1062">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="31e1b-1063">Neue erforderliche Parameter zum Angeben des neuen Event Grid-Domänennamens und/oder Namens des Event Grid-Domänenthemas hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="31e1b-1063">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="31e1b-1064">Neue Parametersätze für Domänen und Domänenthemen hinzugefügt, um die Wiederverwendung vorhandener Parameter zuzulassen (‚z. B. „EndPointType“, „SubjectBeginsWith“ usw.)</span><span class="sxs-lookup"><span data-stu-id="31e1b-1064">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="31e1b-1065">Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="31e1b-1065">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="31e1b-1066">Ablaufdatum des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="31e1b-1066">Event subscription expiration date,</span></span>
            - <span data-ttu-id="31e1b-1067">Erweiterte Filterparameter</span><span class="sxs-lookup"><span data-stu-id="31e1b-1067">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="31e1b-1068">Neue Enumeration für „servicebusqueue“ als Ziel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1068">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="31e1b-1069">Verwendung der Option „All“ in „-IncludedEventType“ gesperrt und wie folgt ersetzt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1069">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="31e1b-1070">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="31e1b-1070">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="31e1b-1071">Neue optionale Parameter („Top“, „ODataQuery“ und „NextLink“) zur Unterstützung der Ergebnispaginierung und -filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1071">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="31e1b-1072">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="31e1b-1072">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="31e1b-1073">Neue erforderliche Parameter zur Unterstützung des Pipings für die Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Entfernen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="31e1b-1073">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="31e1b-1074">Neue erforderliche Parameter zum Angeben des Event Grid-Domänennamens und/oder Event Grid-Domänenthemanamens hinzugefügt, um das Entfernen vorhandener Ereignisabonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="31e1b-1074">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="31e1b-1075">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="31e1b-1075">Az.FrontDoor</span></span>
* <span data-ttu-id="31e1b-1076">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="31e1b-1076">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="31e1b-1077">Unterstützung von Transformationen und neuen Wert für den Operator zum automatischen Vervollständigen (RegEx) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1077">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="31e1b-1078">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="31e1b-1078">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="31e1b-1079">Neue Werte für automatisches Vervollständigen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1079">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31e1b-1080">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31e1b-1080">Az.Network</span></span>
* <span data-ttu-id="31e1b-1081">Unterstützung für Virtual Network-Gatewayressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1081">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="31e1b-1082">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="31e1b-1082">New cmdlets</span></span>
        - <span data-ttu-id="31e1b-1083">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="31e1b-1083">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="31e1b-1084">AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="31e1b-1084">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="31e1b-1085">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="31e1b-1085">New cmdlets</span></span> 
        - <span data-ttu-id="31e1b-1086">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="31e1b-1086">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="31e1b-1087">„PrivatePrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1087">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="31e1b-1088">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="31e1b-1088">New cmdlets</span></span> 
        - <span data-ttu-id="31e1b-1089">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="31e1b-1089">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="31e1b-1090">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="31e1b-1090">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="31e1b-1091">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="31e1b-1091">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="31e1b-1092">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="31e1b-1092">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="31e1b-1093">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="31e1b-1093">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="31e1b-1094">„PrivateEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1094">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="31e1b-1095">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="31e1b-1095">New cmdlets</span></span>
        - <span data-ttu-id="31e1b-1096">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="31e1b-1096">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="31e1b-1097">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="31e1b-1097">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="31e1b-1098">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="31e1b-1098">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="31e1b-1099">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="31e1b-1099">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="31e1b-1100">Folgende Befehle für das Feature aktualisiert: UseLocalAzureIpAddress-Flag für „VpnConnection“</span><span class="sxs-lookup"><span data-stu-id="31e1b-1100">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="31e1b-1101">„New-AzVpnConnection§ „ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="31e1b-1101">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="31e1b-1102">„Set-AzVpnConnection“ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="31e1b-1102">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="31e1b-1103">Schreibgeschütztes Feld „PeeredConnections“ beim ExpressRoute-Peering hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1103">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="31e1b-1104">Schreibgeschütztes Feld „GlobalReachEnabled“ in ExpressRoute hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1104">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="31e1b-1105">Breaking Change-Attribut hinzugefügt, um auf das veraltete Feld „AllowGlobalReach“ im ExpressRouteCircuit-Modell hinzuweisen</span><span class="sxs-lookup"><span data-stu-id="31e1b-1105">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="31e1b-1106">Fehler 8756 bei der Verwendung von „TargetListenerID“ mit AzApplicationGatewayRedirectConfiguration-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-1106">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="31e1b-1107">Fehler in „New-AzApplicationGatewayPathRuleConfig“ behoben, aufgrund dessen der Regelsatz für erneutes Generieren nicht festgelegt werden konnte</span><span class="sxs-lookup"><span data-stu-id="31e1b-1107">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="31e1b-1108">Fehler bei der Anzeige von „VirtualNetworkTaps“ in „NetworkInterfaceIpConfiguration“ behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-1108">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="31e1b-1109">Cortex-Get-Cmdlets zum Auflisten aller Komponenten korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1109">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="31e1b-1110">Problem beim Erstellen des festen VirtualHub-Verweises für ExpressRouteGateways behoben (VpnGateway)</span><span class="sxs-lookup"><span data-stu-id="31e1b-1110">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="31e1b-1111">Unterstützung für Verfügbarkeitszonen in AzureFirewall und NatGateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1111">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="31e1b-1112">Cmdlet „Get-AzNetworkServiceTag“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1112">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="31e1b-1113">Unterstützung für mehrere öffentliche IP-Adressen für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1113">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="31e1b-1114">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="31e1b-1114">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="31e1b-1115">Parameter „-PublicIpAddress“ hinzugefügt, der ein oder mehre öffentliche IP-Adressobjekte akzeptiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1115">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="31e1b-1116">Parameter „- VirtualNetwork“ hinzugefügt, der ein Virtual Network-Objekt akzeptiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1116">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="31e1b-1117">Methoden „AddPublicIpAddress“ und „RemovePublicIpAddress“ für Firewallobjekte hinzugefügt (akzeptieren ein öffentliches IP-Adressobjekt als Eingabe)</span><span class="sxs-lookup"><span data-stu-id="31e1b-1117">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="31e1b-1118">Parameter „-PublicIpName“ und „-VirtualNetworkName“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1118">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="31e1b-1119">Folgende Befehle für das Feature aktualisiert: VpnClient-AAD-Authentifizierungsoptionen auf die Gatewayressource des virtuellen Netzwerkgateways festgelegt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1119">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="31e1b-1120">„New-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1120">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="31e1b-1121">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1121">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="31e1b-1122">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionaler Switch-Parameter „RemoveAadAuthentication“ zum Entfernen von VpnClient-AAD-Authentifizierungsoptionen aus dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1122">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="31e1b-1123">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="31e1b-1123">Az.OperationalInsights</span></span>
* <span data-ttu-id="31e1b-1124">Tarif **pergb2018** im Befehl „New-AzureRmOperationalInsightsWorkspace“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="31e1b-1124">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="31e1b-1125">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31e1b-1125">Az.Resources</span></span>
* <span data-ttu-id="31e1b-1126">Unterstützung für zusätzliche Optionen zum Exportieren von Vorlagen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1126">Support for additional Template Export options</span></span>
    - <span data-ttu-id="31e1b-1127">Parameter „-SkipResourceNameParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1127">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="31e1b-1128">Parameter -SkipAllParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1128">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="31e1b-1129">Parameter „-Resource“ zu „Export-AzResourceGroup“ hinzugefügt, um das Filtern exportierter Ressourcen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="31e1b-1129">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="31e1b-1130">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="31e1b-1130">Az.ServiceFabric</span></span>
* <span data-ttu-id="31e1b-1131">Problem beim Hinzufügen des Zertifikats mit „ByExistingKeyVault“ behoben (Abruf des falschen Fingerabdrucks in manchen Fällen)</span><span class="sxs-lookup"><span data-stu-id="31e1b-1131">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="31e1b-1132">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31e1b-1132">Az.Sql</span></span>
* <span data-ttu-id="31e1b-1133">Suffix des Advanced Threat Protection-Endpunkts korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1133">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="31e1b-1134">Durch Advanced Data Security ermöglichte Außerkraftsetzungen der Advanced Threat Protection-Richtlinie korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1134">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="31e1b-1135">Neue Cmdlets für „Management.Sql“ ermöglichen Kunden das Hinzufügen von TDE-Schlüsseln und Festlegen der TDE-Schutzvorrichtung für verwaltete Instanzen.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1135">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="31e1b-1136">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="31e1b-1136">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="31e1b-1137">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="31e1b-1137">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="31e1b-1138">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="31e1b-1138">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="31e1b-1139">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="31e1b-1139">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="31e1b-1140">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="31e1b-1140">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="31e1b-1141">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="31e1b-1141">Az.Storage</span></span>
* <span data-ttu-id="31e1b-1142">Unterstützung von „FileStorage“ und „SkuName Premium_ZRS“ beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="31e1b-1142">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="31e1b-1143">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="31e1b-1143">New-AzStorageAccount</span></span>
* <span data-ttu-id="31e1b-1144">Überarbeitete Beschreibung des Cmdlets für die Unveränderlichkeit von Blobs</span><span class="sxs-lookup"><span data-stu-id="31e1b-1144">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="31e1b-1145">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="31e1b-1145">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="31e1b-1146">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="31e1b-1146">Az.Websites</span></span>
* <span data-ttu-id="31e1b-1147">Optimiert „Get-AzWebAppCertificate“, um nach der Ressourcengruppe auf dem Server zu filtern (nicht auf dem Client)</span><span class="sxs-lookup"><span data-stu-id="31e1b-1147">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="31e1b-1148">Switch-Parameter „-UseDisasterRecovery“ für „Get-AzWebAppSnapshot“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1148">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="31e1b-1149">2.2.0 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="31e1b-1149">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="31e1b-1150">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="31e1b-1150">Az.Cdn</span></span>
* <span data-ttu-id="31e1b-1151">Es wurden Cmdlets aktualisiert, um das rulesEngine-Feature basierend auf der API-Version 2019-04-15 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1151">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31e1b-1152">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31e1b-1152">Az.Compute</span></span>
* <span data-ttu-id="31e1b-1153">Der Parameter `NoWait` wurde hinzugefügt, der den Vorgang startet und sofort zurückkehrt, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1153">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="31e1b-1154">Aktualisierte Cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="31e1b-1154">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="31e1b-1155">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="31e1b-1155">Az.EventHub</span></span>
* <span data-ttu-id="31e1b-1156">Fehlerbehebung für #9231 – Get-AzEventHubNamespace gibt keine Tags zurück</span><span class="sxs-lookup"><span data-stu-id="31e1b-1156">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="31e1b-1157">Fehlerbehebung für #9230 – Get-AzEventHubNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="31e1b-1157">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31e1b-1158">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31e1b-1158">Az.Network</span></span>
* <span data-ttu-id="31e1b-1159">ResourceId und InputObject wurden für NAT Gateway aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1159">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="31e1b-1160">Es wurde ein Alias für ResourceId und InputObjectr hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1160">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="31e1b-1161">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="31e1b-1161">Az.PolicyInsights</span></span>
* <span data-ttu-id="31e1b-1162">Fehlerbehebung für Nullverweis in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="31e1b-1162">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="31e1b-1163">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="31e1b-1163">Az.RecoveryServices</span></span>
* <span data-ttu-id="31e1b-1164">Minimale Aufbewahrung in Tagen für IaaSVM-Richtlinie wurde von 1 in 7 geändert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1164">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="31e1b-1165">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="31e1b-1165">Az.ServiceBus</span></span>
* <span data-ttu-id="31e1b-1166">Fehlerbehebung für #9182 – Get-AzServiceBusNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="31e1b-1166">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="31e1b-1167">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="31e1b-1167">Az.ServiceFabric</span></span>
* <span data-ttu-id="31e1b-1168">Tippfehler in Fehlermeldung für Update-AzServiceFabricReliability wurde behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-1168">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="31e1b-1169">Fehlendes Zeichen in Service Fabric-Befehlszeilen wurde behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-1169">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="31e1b-1170">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31e1b-1170">Az.Sql</span></span>
* <span data-ttu-id="31e1b-1171">Der DnsZonePartner-Parameter für das Cmdlet New-AzureSqlInstance wurde hinzugefügt, um AutoDr für verwaltete Instanzen zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="31e1b-1171">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="31e1b-1172">Das Cmdlet Get-AzSqlDatabaseSecureConnectionPolicy wird eingestellt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1172">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="31e1b-1173">Cmdlets zum Schutz vor Bedrohungen werden in „Advanced Threat Protection“ (Erweiterter Schutz vor Bedrohungen) umbenannt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1173">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="31e1b-1174">New-AzSqlInstance – Die Parameter StorageSizeInGB und LicenseType sind jetzt optional</span><span class="sxs-lookup"><span data-stu-id="31e1b-1174">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="31e1b-1175">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="31e1b-1175">Az.Websites</span></span>
* <span data-ttu-id="31e1b-1176">Das Problem, bei dem die Verwendung von Set-AzWebApp und Set-AzWebAppSlot mit der -WebApp-Eigenschaft die Tags entfernt hat, wurde behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-1176">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="31e1b-1177">2.1.0 – Mai 2019</span><span class="sxs-lookup"><span data-stu-id="31e1b-1177">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="31e1b-1178">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="31e1b-1178">Az.ApiManagement</span></span>
* <span data-ttu-id="31e1b-1179">Es wurden neue Cmdlets zum Verwalten der Diagnose im globalen sowie im API-Bereich erstellt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1179">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="31e1b-1180">**Get-AzApiManagementDiagnostic**: Abrufen der Diagnose, die im globalen oder im API-Bereich konfiguriert wurde</span><span class="sxs-lookup"><span data-stu-id="31e1b-1180">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="31e1b-1181">**New-AzApiManagementDiagnostic**: Erstellen neuer Diagnosen im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="31e1b-1181">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="31e1b-1182">**New-AzApiManagementHttpMessageDiagnostic**: Erstellen einer Diagnoseeinstellung für die zu protokollierenden Kopfzeilen und für die Größe der Bytes für den Text</span><span class="sxs-lookup"><span data-stu-id="31e1b-1182">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="31e1b-1183">**New-AzApiManagementPipelineDiagnosticSetting**: Erstellen von Diagnoseeinstellungen für ein-/ausgehende HTTP-Nachrichten für das Gateway</span><span class="sxs-lookup"><span data-stu-id="31e1b-1183">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="31e1b-1184">**New-AzApiManagementSamplingSetting**: Erstellen der Einstellung „Sampling“ für die Anforderungen/Antworten für eine Diagnose</span><span class="sxs-lookup"><span data-stu-id="31e1b-1184">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="31e1b-1185">**Remove-AzApiManagementDiagnostic**: Entfernen einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="31e1b-1185">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="31e1b-1186">**Set-AzApiManagementDiagnostic**: Aktualisieren einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="31e1b-1186">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="31e1b-1187">Es wurden neue Cmdlets für die Cacheverwaltung im ApiManagement-Dienst erstellt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1187">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="31e1b-1188">**Get-AzApiManagementCache**: Abrufen der Details des durch den Bezeichner angegebenen Caches oder aller Caches</span><span class="sxs-lookup"><span data-stu-id="31e1b-1188">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="31e1b-1189">**New-AzApiManagementCache**: Erstellen eines neuen „standardmäßigen“ Caches oder eines Caches in einer bestimmten „Region“ von Azure</span><span class="sxs-lookup"><span data-stu-id="31e1b-1189">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="31e1b-1190">**Remove-AzApiManagementCache**: Entfernen eines Caches</span><span class="sxs-lookup"><span data-stu-id="31e1b-1190">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="31e1b-1191">**Update-AzApiManagementCache**: Aktualisieren eines Caches</span><span class="sxs-lookup"><span data-stu-id="31e1b-1191">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="31e1b-1192">Es wurden neue Cmdlets zur Verwaltung von API-Schemas erstellt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1192">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="31e1b-1193">**New-AzApiManagementSchema**: Erstellen eines neuen Schemas für eine API</span><span class="sxs-lookup"><span data-stu-id="31e1b-1193">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="31e1b-1194">**Get-AzApiManagementSchema**: Abrufen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="31e1b-1194">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="31e1b-1195">**Remove-AzApiManagementSchema**: Entfernen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="31e1b-1195">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="31e1b-1196">**Set-AzApiManagementSchema**: Aktualisieren des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="31e1b-1196">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="31e1b-1197">Es wurde ein neues Cmdlet zum Generieren eines Benutzertokens erstellt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1197">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="31e1b-1198">**New-AzApiManagementUserToken**: Generieren eines neuen Benutzertokens, das standardmäßig für acht Stunden gültig ist. Mit diesem Cmdlet kann das Token für den „GIT“-Benutzer generiert werden./</span><span class="sxs-lookup"><span data-stu-id="31e1b-1198">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="31e1b-1199">Es wurde ein neues Cmdlet zum Abrufen des Netzwerkstatus erstellt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1199">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="31e1b-1200">**Get-AzApiManagementNetworkStatus**: Abrufen der Netzwerkstatuskonnektivität von Ressourcen, von denen der API Management-Dienst abhängig ist</span><span class="sxs-lookup"><span data-stu-id="31e1b-1200">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="31e1b-1201">Dies ist hilfreich, wenn Sie den ApiManagement-Dienst in einem virtuellen Netzwerk bereitstellen und überprüfen, ob eine der Abhängigkeiten fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1201">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="31e1b-1202">Das Cmdlet **New-AzApiManagement** wurde zum Verwalten des ApiManagement-Diensts aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1202">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="31e1b-1203">Die Unterstützung für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1203">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="31e1b-1204">Die Unterstützung zum Aktivieren des Flags „EnableClientCertificate“ für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1204">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="31e1b-1205">Das neue Cmdlet **New-AzApiManagementSslSetting** ermöglicht die Konfiguration der „TLS/SSL“-Einstellung für „Back-End“ und „Front-End“</span><span class="sxs-lookup"><span data-stu-id="31e1b-1205">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="31e1b-1206">Dies kann auch dazu verwendet werden, um „Verschlüsselungen“ wie „3DES“ und „ServerProtokolle“ wie „Http2“ für das „Front-End“ eines ApiManagement-Diensts zu konfigurieren</span><span class="sxs-lookup"><span data-stu-id="31e1b-1206">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="31e1b-1207">Die Unterstützung für die Konfiguration des Hostnamens „DeveloperPortal“ wurde zum ApiManagement-Dienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1207">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="31e1b-1208">Die **Get-AzApiManagementSsoToken**-Cmdlets wurden aktualisiert, um das Objekt „PsApiManagement“ als Eingabe zu übernehmen</span><span class="sxs-lookup"><span data-stu-id="31e1b-1208">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="31e1b-1209">Das Cmdlet wurde aktualisiert, um Fehlermeldungen inline anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="31e1b-1209">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="31e1b-1210">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Fehlercode: ValidationError-Fehlermeldung: Mindestens ein Feld enthält ungültige Werte: Fehlerdetails: [Code=ValidationError, Message=Fehler in Element 'log-to-eventhub' in Zeile 3, Spalte 10: Protokollierungstool nicht gefunden, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="31e1b-1210">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="31e1b-1211">Cmdlet **Export-AzApiManagementApi** wurde für den Export von APIs im Format „OpenApi 3.0“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1211">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="31e1b-1212">Cmdlet **Import-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1212">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="31e1b-1213">Zum Importieren der API aus der „OpenApi 3.0“-Dokumentspezifikation</span><span class="sxs-lookup"><span data-stu-id="31e1b-1213">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="31e1b-1214">Zur Außerkraftsetzung der „PsApiManagementSchema“-Eigenschaft, die in einem beliebigen Dokument („Swagger“, „Wadl“, „Wsdl“, „OpenApi“) angegeben ist</span><span class="sxs-lookup"><span data-stu-id="31e1b-1214">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="31e1b-1215">Zur Außerkraftsetzung der „ServiceUrl“-Eigenschaft, die in einem beliebigen Dokument angegeben ist</span><span class="sxs-lookup"><span data-stu-id="31e1b-1215">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="31e1b-1216">Cmdlet **Get-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="31e1b-1216">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="31e1b-1217">Cmdlet **Set-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ und im Format mit XML-Escapezeichen mit „xml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="31e1b-1217">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="31e1b-1218">Cmdlet **New-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1218">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="31e1b-1219">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="31e1b-1219">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="31e1b-1220">Zum Erstellen einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="31e1b-1220">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="31e1b-1221">Zum Klonen einer API mithilfe von „SourceApiId“ und „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="31e1b-1221">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="31e1b-1222">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="31e1b-1222">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="31e1b-1223">Cmdlet **Set-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1223">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="31e1b-1224">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="31e1b-1224">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="31e1b-1225">Zum Aktualisieren einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="31e1b-1225">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="31e1b-1226">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="31e1b-1226">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="31e1b-1227">Cmdlet **New-AzApiManagementRevision** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1227">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="31e1b-1228">Zum Klonen (Kopiertags, Produkte, Vorgänge und Richtlinien) einer vorhandenen Version mithilfe von „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="31e1b-1228">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="31e1b-1229">Die neue Version übernimmt die „ApiId“ des übergeordneten Elements</span><span class="sxs-lookup"><span data-stu-id="31e1b-1229">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="31e1b-1230">Zum Bereitstellen einer „ApiRevisionDescription“</span><span class="sxs-lookup"><span data-stu-id="31e1b-1230">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="31e1b-1231">Zur Außerkraftsetzung der „ServiceUrl“ beim Klonen einer API</span><span class="sxs-lookup"><span data-stu-id="31e1b-1231">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="31e1b-1232">Cmdlet **New-AzApiManagementIdentityProvider** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1232">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="31e1b-1233">Zum Konfigurieren von „AAD“ oder „AADB2C“ mit einer „Authority“</span><span class="sxs-lookup"><span data-stu-id="31e1b-1233">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="31e1b-1234">Zum Einrichten von „SignupPolicy“, „SigninPolicy“, „ProfileEditingPolicy“ und „PasswordResetPolicy“</span><span class="sxs-lookup"><span data-stu-id="31e1b-1234">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="31e1b-1235">Cmdlet **New-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1235">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="31e1b-1236">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="31e1b-1236">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="31e1b-1237">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="31e1b-1237">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="31e1b-1238">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1238">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="31e1b-1239">Cmdlet **Set-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1239">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="31e1b-1240">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="31e1b-1240">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="31e1b-1241">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="31e1b-1241">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="31e1b-1242">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1242">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="31e1b-1243">Folgende Cmdlets wurden aktualisiert, um „ResourceId“ als Eingabe zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="31e1b-1243">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="31e1b-1244">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="31e1b-1244">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="31e1b-1245">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="31e1b-1245">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="31e1b-1246">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="31e1b-1246">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="31e1b-1247">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="31e1b-1247">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="31e1b-1248">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="31e1b-1248">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="31e1b-1249">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="31e1b-1249">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="31e1b-1250">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="31e1b-1250">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="31e1b-1251">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="31e1b-1251">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="31e1b-1252">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="31e1b-1252">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="31e1b-1253">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="31e1b-1253">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="31e1b-1254">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="31e1b-1254">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="31e1b-1255">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="31e1b-1255">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="31e1b-1256">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="31e1b-1256">Az.Automation</span></span>
* <span data-ttu-id="31e1b-1257">Get-AzAutomationJobOutputRecord wurde aktualisiert, um JSON- und Textdatensatzwerte zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1257">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="31e1b-1258">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="31e1b-1258">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="31e1b-1259">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="31e1b-1259">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="31e1b-1260">Das Verhalten von Start-AzAutomationDscCompilationJob wurde geändert, um den Auftrag einfach zu starten, anstatt auf dessen Abschluss zu warten</span><span class="sxs-lookup"><span data-stu-id="31e1b-1260">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="31e1b-1261">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="31e1b-1261">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="31e1b-1262">Fehlerbehebung für Get-AzAutomationDscNode, wenn die Verwendung von „-Name“ alle Knoten zurückgibt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1262">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="31e1b-1263">Jetzt wird nur der übereinstimmende Knoten zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="31e1b-1263">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31e1b-1264">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31e1b-1264">Az.Compute</span></span>
* <span data-ttu-id="31e1b-1265">Parameter „ProtectFromScaleIn“ und „ProtectFromScaleSetAction“ wurden zum Cmdlet „Update-AzVmssVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1265">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="31e1b-1266">Der jetzt festgelegte wimple-Parameter „New-AzVM“ verwendet standardmäßig einen verfügbaren Standort, wenn „East US“ (USA, Osten) nicht unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="31e1b-1266">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="31e1b-1267">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="31e1b-1267">Az.DataLakeStore</span></span>
* <span data-ttu-id="31e1b-1268">Das ADLS-SDK wurde aktualisiert, um „HttpClient“ zu verwenden und Datenebenentests wurden mit dem Azure-Framework integriert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1268">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="31e1b-1269">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="31e1b-1269">Az.Monitor</span></span>
* <span data-ttu-id="31e1b-1270">Fehlerbehebung bei falschen Parameternamen in Hilfebeispielen</span><span class="sxs-lookup"><span data-stu-id="31e1b-1270">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31e1b-1271">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31e1b-1271">Az.Network</span></span>
* <span data-ttu-id="31e1b-1272">DisableBgpRoutePropagation-Flag wurde zur Ausgabe der effektiven Routentabelle hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1272">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="31e1b-1273">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="31e1b-1273">Updated cmdlet:</span></span>
        - <span data-ttu-id="31e1b-1274">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="31e1b-1274">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="31e1b-1275">Fehlerbehebung von doppeltem Bindestrich in Dokumentation von New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="31e1b-1275">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="31e1b-1276">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31e1b-1276">Az.Resources</span></span>
* <span data-ttu-id="31e1b-1277">Neues Cmdlet „Get-AzureRmDenyAssignment“ zum Abrufen von Ablehnungszuweisungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1277">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="31e1b-1278">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31e1b-1278">Az.Sql</span></span>
* <span data-ttu-id="31e1b-1279">„Advanced Threat Protection“-Cmdlets in „Advanced Data Security“ umbenennen und Sicherheitsrisikobewertung standardmäßig aktivieren</span><span class="sxs-lookup"><span data-stu-id="31e1b-1279">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="31e1b-1280">2.0.0: Mai 2019</span><span class="sxs-lookup"><span data-stu-id="31e1b-1280">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="31e1b-1281">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="31e1b-1281">Az.Accounts</span></span>
* <span data-ttu-id="31e1b-1282">Authentifizierungsbibliothek aktualisiert, um ADFS-Probleme mit der Authentifizierung per Benutzername/Kennwort zu beheben</span><span class="sxs-lookup"><span data-stu-id="31e1b-1282">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="31e1b-1283">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="31e1b-1283">Az.CognitiveServices</span></span>
* <span data-ttu-id="31e1b-1284">Ausschließliche Anzeige des Bing-Haftungsausschlusses für Bing-Suchdienste</span><span class="sxs-lookup"><span data-stu-id="31e1b-1284">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="31e1b-1285">Fehler behoben, der zu einem Fehler bei der Kontoerstellung führte</span><span class="sxs-lookup"><span data-stu-id="31e1b-1285">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31e1b-1286">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31e1b-1286">Az.Compute</span></span>
* <span data-ttu-id="31e1b-1287">Feature für die Näherungsplatzierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="31e1b-1287">Proximity placement group feature.</span></span>
    - <span data-ttu-id="31e1b-1288">Die folgenden neuen Cmdlets wurden hinzugefügt:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="31e1b-1288">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="31e1b-1289">Der neue Parameter „ProximityPlacementGroupId“ wurde zu den folgenden Cmdlets hinzugefügt:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="31e1b-1289">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="31e1b-1290">Der Parameter „StorageAccountType“ wurde zu „New-AzGalleryImageVersion“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1290">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="31e1b-1291">„TargetRegion“ von „New-AzGalleryImageVersion“ kann „StorageAccountType“ enthalten.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1291">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="31e1b-1292">Switch-Parameter „SkipShutdown“ wurde zu „Stop-AzVM“ und „Stop-AzVmss“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1292">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="31e1b-1293">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="31e1b-1293">Breaking changes</span></span>
    - <span data-ttu-id="31e1b-1294">„Set-AzVMBootDiagnostics“ in „Set-AzVMBootDiagnostic“ geändert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1294">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="31e1b-1295">„Export-AzLogAnalyticThrottledRequests“ in „Export-AzLogAnalyticThrottledRequests“ geändert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1295">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="31e1b-1296">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="31e1b-1296">Az.DeploymentManager</span></span>
* <span data-ttu-id="31e1b-1297">Erste allgemein verfügbare Version der Azure-Bereitstellungs-Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="31e1b-1297">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="31e1b-1298">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="31e1b-1298">Az.Dns</span></span>
* <span data-ttu-id="31e1b-1299">Automatische Delegierung des DNS-Namenservers</span><span class="sxs-lookup"><span data-stu-id="31e1b-1299">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="31e1b-1300">Das Cmdlet zum Erstellen einer DNS-Zone akzeptiert den übergeordneten Zonennamen als zusätzlichen optionalen Parameter.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1300">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="31e1b-1301">NS-Einträge in der übergeordneten Zone für neu erstellte untergeordnete Zone hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1301">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="31e1b-1302">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="31e1b-1302">Az.FrontDoor</span></span>
* <span data-ttu-id="31e1b-1303">Erste allgemein verfügbare Version der Azure Frontdoor-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="31e1b-1303">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="31e1b-1304">WAF-Cmdlets so umbenannt, dass sie „Waf“ enthalten</span><span class="sxs-lookup"><span data-stu-id="31e1b-1304">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="31e1b-1305">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="31e1b-1305">Az.HDInsight</span></span>
* <span data-ttu-id="31e1b-1306">Zwei Cmdlets entfernt:</span><span class="sxs-lookup"><span data-stu-id="31e1b-1306">Removed two cmdlets:</span></span>
    - <span data-ttu-id="31e1b-1307">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="31e1b-1307">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="31e1b-1308">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="31e1b-1308">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="31e1b-1309">Neues Cmdlet „Set-AzHDInsightGatewayCredential“ hinzugefügt, um „Grant-AzHDInsightHttpServicesAccess“ zu ersetzen</span><span class="sxs-lookup"><span data-stu-id="31e1b-1309">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="31e1b-1310">Cmdlet „Get-AzHDInsightJobOutput“ aktualisiert, um zwischen Leserrolle und HDInsight-Bedienerrolle zu unterscheiden:</span><span class="sxs-lookup"><span data-stu-id="31e1b-1310">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="31e1b-1311">Benutzer mit der Rolle „Leser“ müssen den Parameter „DefaultStorageAccountKey“ explizit angeben, andernfalls treten Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1311">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="31e1b-1312">Benutzer mit der Rolle des HDInsight-Bedieners sind nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1312">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="31e1b-1313">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="31e1b-1313">Az.Monitor</span></span>
* <span data-ttu-id="31e1b-1314">Neue Cmdlets für SQR-API (Scheduled Query Rule, geplante Abfrageregel)</span><span class="sxs-lookup"><span data-stu-id="31e1b-1314">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="31e1b-1315">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="31e1b-1315">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="31e1b-1316">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="31e1b-1316">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="31e1b-1317">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="31e1b-1317">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="31e1b-1318">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="31e1b-1318">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="31e1b-1319">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="31e1b-1319">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="31e1b-1320">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="31e1b-1320">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="31e1b-1321">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="31e1b-1321">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="31e1b-1322">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="31e1b-1322">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="31e1b-1323">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="31e1b-1323">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="31e1b-1324">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="31e1b-1324">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="31e1b-1325">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="31e1b-1325">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="31e1b-1326">[Weitere Informationen](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) zur SQR-API</span><span class="sxs-lookup"><span data-stu-id="31e1b-1326">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="31e1b-1327">„Az.Monitor.md“ aktualisiert, um Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch) einzuschließen</span><span class="sxs-lookup"><span data-stu-id="31e1b-1327">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31e1b-1328">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31e1b-1328">Az.Network</span></span>
* <span data-ttu-id="31e1b-1329">Unterstützung für NAT-Gatewayressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1329">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="31e1b-1330">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="31e1b-1330">New cmdlets</span></span>
        - <span data-ttu-id="31e1b-1331">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="31e1b-1331">New-AzNatGateway</span></span>
        - <span data-ttu-id="31e1b-1332">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="31e1b-1332">Get-AzNatGateway</span></span>
        - <span data-ttu-id="31e1b-1333">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="31e1b-1333">Set-AzNatGateway</span></span>
        - <span data-ttu-id="31e1b-1334">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="31e1b-1334">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="31e1b-1335">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="31e1b-1335">Updated cmdlets</span></span>
        - <span data-ttu-id="31e1b-1336">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="31e1b-1336">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="31e1b-1337">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="31e1b-1337">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="31e1b-1338">Folgende Befehle für das Feature aktualisiert: Benutzerdefinierte Routen für Brooklyn-Gateway festgelegt/entfernt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1338">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="31e1b-1339">„New-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1339">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="31e1b-1340">„Set-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1340">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="31e1b-1341">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="31e1b-1341">Az.PolicyInsights</span></span>
* <span data-ttu-id="31e1b-1342">Unterstützung für die Abfrage von Richtlinienauswertungsdetails</span><span class="sxs-lookup"><span data-stu-id="31e1b-1342">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="31e1b-1343">Parameter „-Expand“ zu „Get-AzPolicyState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1343">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="31e1b-1344">Unterstützung für „-Expand PolicyEvaluationDetails“</span><span class="sxs-lookup"><span data-stu-id="31e1b-1344">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="31e1b-1345">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="31e1b-1345">Az.RecoveryServices</span></span>
* <span data-ttu-id="31e1b-1346">Unterstützung für abonnementübergreifende Azure-zu-Azure-Sitewiederherstellung</span><span class="sxs-lookup"><span data-stu-id="31e1b-1346">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="31e1b-1347">Markierung anstehender wichtiger Änderungen für Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="31e1b-1347">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="31e1b-1348">Fehlerbehebung für Azure Site Recovery-Wiederherstellungsplan und -Aktionsplan</span><span class="sxs-lookup"><span data-stu-id="31e1b-1348">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="31e1b-1349">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Netzwerkzuordnung für Azure zu Azure</span><span class="sxs-lookup"><span data-stu-id="31e1b-1349">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="31e1b-1350">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Schutzrichtung für Azure zu Azure für verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="31e1b-1350">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="31e1b-1351">Weitere kleinere Korrekturen</span><span class="sxs-lookup"><span data-stu-id="31e1b-1351">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="31e1b-1352">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="31e1b-1352">Az.Relay</span></span>
* <span data-ttu-id="31e1b-1353">Korrektur von Tippfehlern in Kundennachrichten</span><span class="sxs-lookup"><span data-stu-id="31e1b-1353">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="31e1b-1354">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="31e1b-1354">Az.ServiceBus</span></span>
* <span data-ttu-id="31e1b-1355">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1355">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="31e1b-1356">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="31e1b-1356">Az.Storage</span></span>
* <span data-ttu-id="31e1b-1357">Upgrade auf Speicherclientbibliothek 10.0.1 (Namespace aller Objekte von diesem SDK von „Microsoft.WindowsAzure.Storage. *“ in „Microsoft.Azure.Storage.* “ geändert)</span><span class="sxs-lookup"><span data-stu-id="31e1b-1357">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="31e1b-1358">Upgrade auf Microsoft.Azure.Management.Storage 11.0.0, um die neue API-Version 2019-04-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="31e1b-1358">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="31e1b-1359">Art des Standardspeicherkontos bei der Speicherkontoerstellung von „Storage“ in „StorageV2“ geändert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1359">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="31e1b-1360">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="31e1b-1360">New-AzStorageAccount</span></span>
* <span data-ttu-id="31e1b-1361">Vom Speicherkonto-Cmdlet ausgegebener SKU-Name (Sku.Name) durch Hinzufügen eines Unterstrichs an SKU-Eingabename angepasst (Beispiel: „StandardLRS“ > „Standard_LRS“).</span><span class="sxs-lookup"><span data-stu-id="31e1b-1361">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="31e1b-1362">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="31e1b-1362">New-AzStorageAccount</span></span>
    - <span data-ttu-id="31e1b-1363">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="31e1b-1363">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="31e1b-1364">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="31e1b-1364">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="31e1b-1365">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="31e1b-1365">Az.Websites</span></span>
* <span data-ttu-id="31e1b-1366">Die Eigenschaft „Kind“ wird nun für PSSite-Objekte festgelegt, die von „Get-AzWebApp“ zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1366">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="31e1b-1367">„Get-AzWebApp\*Metrics“ und „Get-AzAppServicePlanMetrics“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1367">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="31e1b-1368">1.8.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="31e1b-1368">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="31e1b-1369">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="31e1b-1369">Highlights since the last major release</span></span>
* <span data-ttu-id="31e1b-1370">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="31e1b-1370">General availability of `Az` module</span></span>
* <span data-ttu-id="31e1b-1371">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1371">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="31e1b-1372">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1372">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="31e1b-1373">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1373">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="31e1b-1374">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1374">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="31e1b-1375">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1375">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="31e1b-1376">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="31e1b-1376">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="31e1b-1377">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="31e1b-1377">Az.Accounts</span></span>
* <span data-ttu-id="31e1b-1378">„Uninstall-AzureRm“ aktualisiert, um Module unter Mac ordnungsgemäß zu löschen</span><span class="sxs-lookup"><span data-stu-id="31e1b-1378">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="31e1b-1379">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="31e1b-1379">Az.Batch</span></span>
* <span data-ttu-id="31e1b-1380">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1380">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="31e1b-1381">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="31e1b-1381">Az.Cdn</span></span>
* <span data-ttu-id="31e1b-1382">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1382">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="31e1b-1383">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="31e1b-1383">Az.CognitiveServices</span></span>
* <span data-ttu-id="31e1b-1384">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1384">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31e1b-1385">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31e1b-1385">Az.Compute</span></span>
* <span data-ttu-id="31e1b-1386">Problem mit der AEM-Installation behoben, wenn die Ressourcen-IDs von Datenträgern Ressourcengruppen in Kleinbuchstaben enthielten</span><span class="sxs-lookup"><span data-stu-id="31e1b-1386">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="31e1b-1387">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1387">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="31e1b-1388">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1388">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="31e1b-1389">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="31e1b-1389">Az.DataFactory</span></span>
* <span data-ttu-id="31e1b-1390">„SsisProperties“ hinzugefügt, falls „NodeCount“ für verwaltete Integration Runtime nicht NULL ist</span><span class="sxs-lookup"><span data-stu-id="31e1b-1390">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="31e1b-1391">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="31e1b-1391">Az.DataLakeStore</span></span>
* <span data-ttu-id="31e1b-1392">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1392">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="31e1b-1393">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="31e1b-1393">Az.EventGrid</span></span>
* <span data-ttu-id="31e1b-1394">Hilfetext für Endpunkt aktualisiert, um anzugeben, dass Ressourcen erstellt werden müssen, bevor die Cmdlets zum Erstellen/Aktualisieren von Ereignisabonnements verwendet werden</span><span class="sxs-lookup"><span data-stu-id="31e1b-1394">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="31e1b-1395">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="31e1b-1395">Az.EventHub</span></span>
* <span data-ttu-id="31e1b-1396">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1396">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="31e1b-1397">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="31e1b-1397">Az.HDInsight</span></span>
* <span data-ttu-id="31e1b-1398">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1398">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="31e1b-1399">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="31e1b-1399">Az.IotHub</span></span>
* <span data-ttu-id="31e1b-1400">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1400">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="31e1b-1401">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="31e1b-1401">Az.KeyVault</span></span>
* <span data-ttu-id="31e1b-1402">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1402">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="31e1b-1403">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1403">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="31e1b-1404">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="31e1b-1404">Az.MachineLearning</span></span>
* <span data-ttu-id="31e1b-1405">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1405">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="31e1b-1406">Az.Media</span><span class="sxs-lookup"><span data-stu-id="31e1b-1406">Az.Media</span></span>
* <span data-ttu-id="31e1b-1407">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1407">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="31e1b-1408">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="31e1b-1408">Az.Monitor</span></span>
  * <span data-ttu-id="31e1b-1409">Neue Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch)</span><span class="sxs-lookup"><span data-stu-id="31e1b-1409">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="31e1b-1410">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="31e1b-1410">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="31e1b-1411">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="31e1b-1411">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="31e1b-1412">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="31e1b-1412">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="31e1b-1413">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="31e1b-1413">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="31e1b-1414">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="31e1b-1414">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="31e1b-1415">Monitor SDK auf Version 0.22.0-preview aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1415">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31e1b-1416">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31e1b-1416">Az.Network</span></span>
* <span data-ttu-id="31e1b-1417">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1417">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="31e1b-1418">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1418">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="31e1b-1419">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="31e1b-1419">Az.NotificationHubs</span></span>
* <span data-ttu-id="31e1b-1420">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1420">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="31e1b-1421">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="31e1b-1421">Az.OperationalInsights</span></span>
* <span data-ttu-id="31e1b-1422">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1422">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="31e1b-1423">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="31e1b-1423">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="31e1b-1424">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1424">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="31e1b-1425">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="31e1b-1425">Az.RecoveryServices</span></span>
* <span data-ttu-id="31e1b-1426">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1426">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="31e1b-1427">Tabellenformat für SQL auf Azure-VM aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1427">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="31e1b-1428">Alternative Methode zum Abrufen des Speicherorts in „AzureFileShare“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1428">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="31e1b-1429">„ScheduleRunDays“ in SchedulePolicy-Objekt gemäß Zeitzone aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1429">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="31e1b-1430">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="31e1b-1430">Az.RedisCache</span></span>
* <span data-ttu-id="31e1b-1431">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1431">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="31e1b-1432">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31e1b-1432">Az.Resources</span></span>
* <span data-ttu-id="31e1b-1433">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1433">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="31e1b-1434">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31e1b-1434">Az.Sql</span></span>
* <span data-ttu-id="31e1b-1435">Abhängigkeit vom Monitor SDK durch allgemeinen Code ersetzt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1435">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="31e1b-1436">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1436">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="31e1b-1437">Verbesserter Prozess für Klassifizierung mehrerer Spalten</span><span class="sxs-lookup"><span data-stu-id="31e1b-1437">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="31e1b-1438">SKU-Eigenschaften (SKU-Name, Familie, Kapazität) in Antwort von „Get-AzSqlServerServiceObjective“ aufgenommen und standardmäßig als Tabelle formatiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1438">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="31e1b-1439">Möglichkeit zum Ausführen von „Get-AzSqlServerServiceObjective“ nach Standort, ohne dass bereits ein Server in der Region vorhanden sein muss</span><span class="sxs-lookup"><span data-stu-id="31e1b-1439">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="31e1b-1440">Unterstützung für Zeitzonenparameter bei der Erstellung einer verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="31e1b-1440">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="31e1b-1441">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1441">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="31e1b-1442">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="31e1b-1442">Az.Websites</span></span>
* <span data-ttu-id="31e1b-1443">„Set-AzWebApp“ und „Set-AzWebAppSlot“ korrigiert, sodass die Tags bei der Ausführung nicht entfernt werden</span><span class="sxs-lookup"><span data-stu-id="31e1b-1443">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="31e1b-1444">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1444">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="31e1b-1445">WebSites SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1445">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="31e1b-1446">AdminSiteName-Eigenschaft aus „PSAppServicePlan“ entfernt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1446">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="31e1b-1447">1.7.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="31e1b-1447">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="31e1b-1448">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="31e1b-1448">Highlights since the last major release</span></span>
* <span data-ttu-id="31e1b-1449">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="31e1b-1449">General availability of `Az` module</span></span>
* <span data-ttu-id="31e1b-1450">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1450">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="31e1b-1451">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1451">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="31e1b-1452">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1452">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="31e1b-1453">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1453">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="31e1b-1454">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1454">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="31e1b-1455">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="31e1b-1455">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="31e1b-1456">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="31e1b-1456">Az.Accounts</span></span>
* <span data-ttu-id="31e1b-1457">„Add-AzEnvironment“ und „Set-AzEnvironment“ aktualisiert, um den Parameter „AzureAnalysisServicesEndpointResourceId“ zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="31e1b-1457">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="31e1b-1458">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="31e1b-1458">Az.AnalysisServices</span></span>
* <span data-ttu-id="31e1b-1459">ServiceClient wird in Cmdlets für die Datenebene verwendet, und die ursprüngliche Authentifizierungslogik wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1459">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="31e1b-1460">„Add-AzureASAccount“ wird als Wrapper von „Connect-AzAccount“ festgelegt, um einen Breaking Change zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1460">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="31e1b-1461">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="31e1b-1461">Az.Automation</span></span>
* <span data-ttu-id="31e1b-1462">Fehler des Cmdlets „Fixed New-AzAutomationSoftwareUpdateConfiguration“ für Einschlüsse behoben.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1462">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="31e1b-1463">Die Parameter „IncludedKbNumber“ und „IncludedPackageNameMask“ sollten nun funktionieren.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1463">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="31e1b-1464">Fehlerbehebung für eine dynamische Gruppe der Azure Automation-Updateverwaltung</span><span class="sxs-lookup"><span data-stu-id="31e1b-1464">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31e1b-1465">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31e1b-1465">Az.Compute</span></span>
* <span data-ttu-id="31e1b-1466">Parameter „HyperVGeneration“ zu „New-AzDiskConfig“ und „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1466">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="31e1b-1467">Zulassen der VM-Erstellung mit einem Katalogimage aus anderen Mandanten</span><span class="sxs-lookup"><span data-stu-id="31e1b-1467">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="31e1b-1468">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="31e1b-1468">Az.ContainerInstance</span></span>
* <span data-ttu-id="31e1b-1469">Problem im Parameter „-Command“ von „New-AzContainerGroup“ behoben, das dazu führte, dass ein nachgestelltes leeres Argument hinzugefügt wurde</span><span class="sxs-lookup"><span data-stu-id="31e1b-1469">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="31e1b-1470">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="31e1b-1470">Az.DataFactory</span></span>
* <span data-ttu-id="31e1b-1471">Version des ADF .NET SDK auf 3.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1471">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="31e1b-1472">Cmdlet „Set-AzDataFactoryV2“ mit zusätzlichen Parametern für RepoConfiguration-Einstellungen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1472">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="31e1b-1473">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31e1b-1473">Az.Resources</span></span>
* <span data-ttu-id="31e1b-1474">Verarbeitung von Anbietern für „Get-AzResource“ bei der Angabe der Parameter „-ResourceId“ oder „-ResourceGroupName“, „-Name“ und „-ResourceType“ verbessert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1474">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="31e1b-1475">Fehlerbehandlung für „Test-AzDeployment“ und „Test-AzResourceGroupDeployment“ verbessert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1475">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="31e1b-1476">Behandlung von außerhalb der Bereitstellungsüberprüfung aufgetretenen Fehlern und stattdessen Aufnahme in die Ausgabe des Befehls</span><span class="sxs-lookup"><span data-stu-id="31e1b-1476">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="31e1b-1477">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="31e1b-1477">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="31e1b-1478">Switch-Parameter „-IgnoreDynamicParameters“ zu Bereitstellungs-Cmdlets hinzugefügt, um Aufforderung in Skript- und Auftragsszenarien zu überspringen</span><span class="sxs-lookup"><span data-stu-id="31e1b-1478">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="31e1b-1479">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="31e1b-1479">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="31e1b-1480">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31e1b-1480">Az.Sql</span></span>
* <span data-ttu-id="31e1b-1481">Unterstützung für Klassifizierung von Datenbankdaten</span><span class="sxs-lookup"><span data-stu-id="31e1b-1481">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="31e1b-1482">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="31e1b-1482">Az.Storage</span></span>
* <span data-ttu-id="31e1b-1483">Melden eines ausführlichen Fehlers beim Erstellen des Storage-Kontexts mit dem Parameter „-UseConnectedAccount“, aber ohne Azure-Anmeldekonto</span><span class="sxs-lookup"><span data-stu-id="31e1b-1483">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="31e1b-1484">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="31e1b-1484">New-AzStorageContext</span></span>
* <span data-ttu-id="31e1b-1485">Unterstützung für das Verwalten von Blobdiensteigenschaften eines bestimmten Storage-Kontos mit einer API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="31e1b-1485">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="31e1b-1486">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="31e1b-1486">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="31e1b-1487">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="31e1b-1487">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="31e1b-1488">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="31e1b-1488">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="31e1b-1489">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="31e1b-1489">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="31e1b-1490">Unterstützung von „-AsJob“ für Cmdlets für den Upload und Download von Blobs und Dateien</span><span class="sxs-lookup"><span data-stu-id="31e1b-1490">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="31e1b-1491">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="31e1b-1491">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="31e1b-1492">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="31e1b-1492">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="31e1b-1493">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="31e1b-1493">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="31e1b-1494">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="31e1b-1494">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="31e1b-1495">1.6.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="31e1b-1495">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="31e1b-1496">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="31e1b-1496">Highlights since the last major release</span></span>
* <span data-ttu-id="31e1b-1497">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="31e1b-1497">General availability of `Az` module</span></span>
* <span data-ttu-id="31e1b-1498">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1498">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="31e1b-1499">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1499">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="31e1b-1500">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1500">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="31e1b-1501">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1501">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="31e1b-1502">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1502">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="31e1b-1503">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="31e1b-1503">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="31e1b-1504">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="31e1b-1504">Az.Automation</span></span>
* <span data-ttu-id="31e1b-1505">Änderung an der Azure Automation-Updateverwaltung, um die folgenden neuen Features zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="31e1b-1505">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="31e1b-1506">Dynamische Gruppierung</span><span class="sxs-lookup"><span data-stu-id="31e1b-1506">Dynamic grouping</span></span>
    * <span data-ttu-id="31e1b-1507">Pre-/Post-Skripts</span><span class="sxs-lookup"><span data-stu-id="31e1b-1507">Pre-Post script</span></span>
    * <span data-ttu-id="31e1b-1508">Neustarteinstellung</span><span class="sxs-lookup"><span data-stu-id="31e1b-1508">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31e1b-1509">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31e1b-1509">Az.Compute</span></span>
* <span data-ttu-id="31e1b-1510">Problem mit der Pfadauflösung in „Get-AzVmBootDiagnosticsData“ behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-1510">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="31e1b-1511">Computeclientbibliothek auf 25.0.0. aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1511">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="31e1b-1512">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="31e1b-1512">Az.KeyVault</span></span>
* <span data-ttu-id="31e1b-1513">Unterstützung für Platzhalterzeichen zu KeyVault-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1513">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31e1b-1514">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31e1b-1514">Az.Network</span></span>
* <span data-ttu-id="31e1b-1515">Threat Intelligence-Unterstützung für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1515">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="31e1b-1516">Ressource der obersten Ebene für Application Gateway-Firewallrichtlinie und benutzerdefinierte Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1516">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="31e1b-1517">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="31e1b-1517">Az.RecoveryServices</span></span>
* <span data-ttu-id="31e1b-1518">SnapshotRetentionInDays in Azure-VM-Richtlinie hinzugefügt, um sofortigen Wiederherstellungspunkt zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="31e1b-1518">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="31e1b-1519">Pipe-Unterstützung für das Aufheben der Registrierung eines Containers hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1519">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="31e1b-1520">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31e1b-1520">Az.Resources</span></span>
* <span data-ttu-id="31e1b-1521">Unterstützung für Platzhalterzeichen für Get-AzResource und Get-AzResourceGroup aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1521">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="31e1b-1522">Anmeldeinformationen aktualisiert, die beim Senden generischer Aufrufe an ARM verwendet werden</span><span class="sxs-lookup"><span data-stu-id="31e1b-1522">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="31e1b-1523">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31e1b-1523">Az.Sql</span></span>
* <span data-ttu-id="31e1b-1524">Der Cmdlet-Parameter der Bedrohungserkennung (ExcludeDetectionType) wurde von „DetectionType“ in „string[]“ geändert, um ihn zukunftssicher zu machen, wenn neue DetectionTypes-Elemente hinzugefügt werden, und um AutoVervollständigen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1524">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="31e1b-1525">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="31e1b-1525">Az.Storage</span></span>
* <span data-ttu-id="31e1b-1526">Unterstützung von Get-/Set-/Remove-Verwaltungsrichtlinien für Speicherkonto hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1526">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="31e1b-1527">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="31e1b-1527">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="31e1b-1528">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="31e1b-1528">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="31e1b-1529">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="31e1b-1529">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="31e1b-1530">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="31e1b-1530">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="31e1b-1531">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="31e1b-1531">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="31e1b-1532">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="31e1b-1532">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="31e1b-1533">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="31e1b-1533">Az.Websites</span></span>
* <span data-ttu-id="31e1b-1534">ARM-Vorlagenfehler behoben, der zu einem Problem beim Klonen aller Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ führte</span><span class="sxs-lookup"><span data-stu-id="31e1b-1534">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="31e1b-1535">1.5.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="31e1b-1535">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="31e1b-1536">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="31e1b-1536">Az.Accounts</span></span>
* <span data-ttu-id="31e1b-1537">Der Befehl „Register-AzModule“ wurde hinzugefügt, um von AutoRest generierte Cmdlets zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1537">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="31e1b-1538">Beispiele für „Connect-AzAccount“ wurden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1538">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="31e1b-1539">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="31e1b-1539">Az.Automation</span></span>
* <span data-ttu-id="31e1b-1540">Problem behoben, das beim Abrufen bestimmter monatlicher Zeitpläne in verschiedenen Azure Automation-Cmdlets auftrat</span><span class="sxs-lookup"><span data-stu-id="31e1b-1540">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="31e1b-1541">„Get-AzAutomationDscNode“ wurde korrigiert, da nur die 20 obersten Knoten zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1541">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="31e1b-1542">Jetzt werden alle Knoten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1542">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="31e1b-1543">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="31e1b-1543">Az.Cdn</span></span>
* <span data-ttu-id="31e1b-1544">Neue Powershell-Cmdlets zum Aktivieren/Deaktivieren von HTTPS für benutzerdefinierte Domänen hinzugefügt und alte Cmdlets außer Betrieb genommen</span><span class="sxs-lookup"><span data-stu-id="31e1b-1544">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31e1b-1545">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31e1b-1545">Az.Compute</span></span>
* <span data-ttu-id="31e1b-1546">Unterstützung für Platzhalterzeichen zu Get-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1546">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="31e1b-1547">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="31e1b-1547">Az.DataFactory</span></span>
* <span data-ttu-id="31e1b-1548">Version des ADF .NET SDK auf 3.0.1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1548">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="31e1b-1549">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="31e1b-1549">Az.LogicApp</span></span>
* <span data-ttu-id="31e1b-1550">„ListWorkflows“ wurde korrigiert, da nur die erste Seite mit Ergebnissen abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1550">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31e1b-1551">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31e1b-1551">Az.Network</span></span>
* <span data-ttu-id="31e1b-1552">Unterstützung für Platzhalterzeichen zu Network-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1552">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="31e1b-1553">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="31e1b-1553">Az.RecoveryServices</span></span>
* <span data-ttu-id="31e1b-1554">SQL Server jetzt in Azure-VM-Support enthalten</span><span class="sxs-lookup"><span data-stu-id="31e1b-1554">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="31e1b-1555">SDK-Update</span><span class="sxs-lookup"><span data-stu-id="31e1b-1555">SDK Update</span></span>
* <span data-ttu-id="31e1b-1556">VMappContainer-Überprüfung in „Get-ProtectableItem“ entfernt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1556">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="31e1b-1557">„Name“ und „ServerName“ als Parameter für „Get-ProtectableItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1557">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="31e1b-1558">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31e1b-1558">Az.Resources</span></span>
* <span data-ttu-id="31e1b-1559">Parameter `-TemplateObject` zu Bereitstellungs-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1559">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="31e1b-1560">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="31e1b-1560">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="31e1b-1561">Problem beim Piping des Ergebnisses von `Get-AzResource` an `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-1561">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="31e1b-1562">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="31e1b-1562">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="31e1b-1563">Problem mit JSON-Datentypänderung beim Ausführen von `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-1563">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="31e1b-1564">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="31e1b-1564">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="31e1b-1565">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31e1b-1565">Az.Sql</span></span>
* <span data-ttu-id="31e1b-1566">„AuditingEndpointsCommunicator“ wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1566">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="31e1b-1567">Das Verhalten eines Grenzfalls beim Erstellen neuer Diagnoseeinstellungen wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1567">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="31e1b-1568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="31e1b-1568">Az.Storage</span></span>
* <span data-ttu-id="31e1b-1569">Unterstützung von „Kind BlockBlobStorage“ beim Erstellen eines Speicherkontos: New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="31e1b-1569">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="31e1b-1570">1.4.0 – Februar 2019</span><span class="sxs-lookup"><span data-stu-id="31e1b-1570">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="31e1b-1571">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="31e1b-1571">Az.AnalysisServices</span></span>
* <span data-ttu-id="31e1b-1572">Cmdlet „AddAzureASAccount“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1572">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="31e1b-1573">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="31e1b-1573">Az.Automation</span></span>
* <span data-ttu-id="31e1b-1574">Hilfe für „Import-AzAutomationDscNodeConfiguration“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1574">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="31e1b-1575">Überprüfung des Konfigurationsnamens zu Cmdlet „Import-AzAutomationDscConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1575">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="31e1b-1576">Fehlerbehandlung für Cmdlet „Import-AzAutomationDscConfiguration“ verbessert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1576">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="31e1b-1577">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="31e1b-1577">Az.CognitiveServices</span></span>
* <span data-ttu-id="31e1b-1578">„CustomSubdomainName“ als neuer optionaler Parameter für Cmdlet „New-AzCognitiveServicesAccount“ hinzugefügt, das zum Angeben der Unterdomäne für die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1578">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31e1b-1579">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31e1b-1579">Az.Compute</span></span>
* <span data-ttu-id="31e1b-1580">Problem mit ID-Parametersätzen behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-1580">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="31e1b-1581">„Get-AzVMExtension“ aktualisiert, sodass alle installierten Erweiterungen aufgelistet werden, wenn der Name-Parameter nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="31e1b-1581">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="31e1b-1582">Parameter „Tag“ und „ResourceId“ zum Cmdlet „Update-AzImage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1582">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="31e1b-1583">„Get-AzVmssVM“ ohne Instanz-ID und mit „InstanceView“ können virtuelle VMSS-Computer mit Instanzansicht auflisten.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1583">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="31e1b-1584">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="31e1b-1584">Az.DataLakeStore</span></span>
* <span data-ttu-id="31e1b-1585">Cmdlets zum Auflisten und Wiederherstellen gelöschter ADL-Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1585">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="31e1b-1586">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="31e1b-1586">Az.EventHub</span></span>
* <span data-ttu-id="31e1b-1587">Neue boolesche Eigenschaft „SkipEmptyArchives“ zum Überspringen leerer Archive in Klasse „CaptureDescription“ von EventHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1587">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="31e1b-1588">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="31e1b-1588">Az.KeyVault</span></span>
* <span data-ttu-id="31e1b-1589">Kennzeichnung in „Set-AzKeyVaultSecret“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1589">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="31e1b-1590">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="31e1b-1590">Az.LogicApp</span></span>
* <span data-ttu-id="31e1b-1591">SKU „Basic“ für Integrationskonten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1591">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="31e1b-1592">XSLT 2.0, XSLT 3.0 und Liquid-Zuordnungstypen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1592">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="31e1b-1593">Neue Cmdlets für Integrationskonto-Assemblys</span><span class="sxs-lookup"><span data-stu-id="31e1b-1593">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="31e1b-1594">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="31e1b-1594">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="31e1b-1595">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="31e1b-1595">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="31e1b-1596">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="31e1b-1596">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="31e1b-1597">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="31e1b-1597">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="31e1b-1598">Neue Cmdlets für Integrationskonto-Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="31e1b-1598">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="31e1b-1599">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="31e1b-1599">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="31e1b-1600">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="31e1b-1600">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="31e1b-1601">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="31e1b-1601">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="31e1b-1602">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="31e1b-1602">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="31e1b-1603">Logik-App-SDK auf Version 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1603">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="31e1b-1604">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="31e1b-1604">Az.Monitor</span></span>
* <span data-ttu-id="31e1b-1605">Hilfe für „Get-AzMetric“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1605">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31e1b-1606">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31e1b-1606">Az.Network</span></span>
* <span data-ttu-id="31e1b-1607">Hilfebeispiel für „Add-AzApplicationGatewayCustomError“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1607">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="31e1b-1608">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="31e1b-1608">Az.OperationalInsights</span></span>
* <span data-ttu-id="31e1b-1609">Zusätzliche Unterstützung für Datenquelle von „New-ApplicationInsights“ und „Get-ApplicationInsights“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1609">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="31e1b-1610">Neue Art von „ApplicationInsights“ zum Abrufen von bestimmten und von allen ApplicationInsights-Datenquellen für einen Workspace hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1610">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="31e1b-1611">Cmdlet „New-AzOperationalInsightsApplicationInsightsDataSource“ zum Erstellen einer Datenquelle anhand des angegebenen Ressourcenparameters für „Application-Insights“ hinzugefügt: „subscriptionId“, „resourceGroupName“ und „name“.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1611">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="31e1b-1612">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31e1b-1612">Az.Resources</span></span>
* <span data-ttu-id="31e1b-1613">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="31e1b-1613">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="31e1b-1614">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="31e1b-1614">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="31e1b-1615">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="31e1b-1615">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="31e1b-1616">Fehler korrigiert, der die wiederholte Erstellung von „KeyCredentials“ verhindert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1616">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="31e1b-1617">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31e1b-1617">Az.Sql</span></span>
* <span data-ttu-id="31e1b-1618">Unterstützung für SQL DB Hyperscale-Tarif hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1618">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="31e1b-1619">Fehler korrigiert, aufgrund dessen die Wiederherstellung wegen der Festlegung unnötiger Eigenschaften in der Wiederherstellungsanforderung fehlschlagen konnte</span><span class="sxs-lookup"><span data-stu-id="31e1b-1619">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="31e1b-1620">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="31e1b-1620">Az.Websites</span></span>
* <span data-ttu-id="31e1b-1621">Beispiel in „Get-AzWebAppSlotMetrics“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1621">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="31e1b-1622">1.3.0: Februar 2019</span><span class="sxs-lookup"><span data-stu-id="31e1b-1622">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="31e1b-1623">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="31e1b-1623">Az.Accounts</span></span>
* <span data-ttu-id="31e1b-1624">Update auf die aktuelle Version von ClientRuntime durchgeführt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1624">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="31e1b-1625">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="31e1b-1625">Az.AnalysisServices</span></span>
<span data-ttu-id="31e1b-1626">Allgemeine Verfügbarkeit für Az.AnalysisServices-Modul</span><span class="sxs-lookup"><span data-stu-id="31e1b-1626">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31e1b-1627">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31e1b-1627">Az.Compute</span></span>
* <span data-ttu-id="31e1b-1628">AEM-Erweiterung: Unterstützung für UltraSSD und P60-, P70- und P80-Datenträger hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1628">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="31e1b-1629">Hilfebeschreibung für „Set-AzVMBootDiagnostics“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1629">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="31e1b-1630">Hilfebeschreibung und Beispiel für „Update-AzImage“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1630">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="31e1b-1631">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="31e1b-1631">Az.RecoveryServices</span></span>
<span data-ttu-id="31e1b-1632">Allgemeine Verfügbarkeit für Az.RecoveryServices-Modul.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1632">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="31e1b-1633">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31e1b-1633">Az.Resources</span></span>
* <span data-ttu-id="31e1b-1634">Kennzeichnung für Ressourcengruppen korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1634">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="31e1b-1635">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="31e1b-1635">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="31e1b-1636">Problem behoben, bei dem „-ErrorAction“ von `Get-AzureRmRoleAssignment` nicht berücksichtigt wird</span><span class="sxs-lookup"><span data-stu-id="31e1b-1636">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="31e1b-1637">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="31e1b-1637">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="31e1b-1638">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31e1b-1638">Az.Sql</span></span>
* <span data-ttu-id="31e1b-1639">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1639">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="31e1b-1640">Problem behoben, bei dem eine fehlende Anmeldung am Azure-Konto bei der Ausführung von SQL-Cmdlets zu einer nullref-Ausnahme führt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1640">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="31e1b-1641">nullref-Ausnahme in Get-AzSqlCapability korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1641">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="31e1b-1642">1.2.1: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="31e1b-1642">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="31e1b-1643">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="31e1b-1643">Az.Accounts</span></span>
* <span data-ttu-id="31e1b-1644">Release mit richtiger Version der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="31e1b-1644">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="31e1b-1645">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="31e1b-1645">Az.AnalysisServices</span></span>
* <span data-ttu-id="31e1b-1646">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="31e1b-1646">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="31e1b-1647">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="31e1b-1647">Az.RecoveryServices</span></span>
* <span data-ttu-id="31e1b-1648">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="31e1b-1648">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="31e1b-1649">1.2.0: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="31e1b-1649">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="31e1b-1650">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="31e1b-1650">Az.Accounts</span></span>
* <span data-ttu-id="31e1b-1651">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1651">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="31e1b-1652">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1652">Update incorrect online help URLs</span></span>
* <span data-ttu-id="31e1b-1653">Warnmeldung in PS Core für „Uninstall-AzureRm“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1653">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="31e1b-1654">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="31e1b-1654">Az.Aks</span></span>
* <span data-ttu-id="31e1b-1655">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1655">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="31e1b-1656">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="31e1b-1656">Az.Automation</span></span>
* <span data-ttu-id="31e1b-1657">Unterstützung für Python 2-Runbooks hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1657">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="31e1b-1658">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1658">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="31e1b-1659">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="31e1b-1659">Az.Cdn</span></span>
* <span data-ttu-id="31e1b-1660">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1660">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31e1b-1661">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31e1b-1661">Az.Compute</span></span>
* <span data-ttu-id="31e1b-1662">Cmdlet „Invoke-AzVMReimage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1662">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="31e1b-1663">Parameter „TempDisk“ zu „Set-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1663">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="31e1b-1664">Warnmeldung von „New-AzVM“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1664">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="31e1b-1665">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="31e1b-1665">Az.ContainerRegistry</span></span>
* <span data-ttu-id="31e1b-1666">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1666">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="31e1b-1667">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="31e1b-1667">Az.DataFactory</span></span>
* <span data-ttu-id="31e1b-1668">Version des ADF .NET SDK auf 3.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1668">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="31e1b-1669">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="31e1b-1669">Az.DataLakeStore</span></span>
* <span data-ttu-id="31e1b-1670">Problem mit ADLS-Endpunkt bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-1670">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="31e1b-1671">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="31e1b-1671">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="31e1b-1672">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1672">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="31e1b-1673">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="31e1b-1673">Az.IotHub</span></span>
* <span data-ttu-id="31e1b-1674">Codierungsformat zu Cmdlet „Add-IotHubRoutingEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1674">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="31e1b-1675">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="31e1b-1675">Az.KeyVault</span></span>
* <span data-ttu-id="31e1b-1676">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1676">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31e1b-1677">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31e1b-1677">Az.Network</span></span>
* <span data-ttu-id="31e1b-1678">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1678">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="31e1b-1679">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31e1b-1679">Az.Resources</span></span>
* <span data-ttu-id="31e1b-1680">Fehlerhafte Beispiele in Referenzdokumentation zu „New-AzADAppCredential“ und „New-AzADSpCredential“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1680">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="31e1b-1681">Problem behoben, bei dem der Pfad für den Parameter „-TemplateFile“ nicht aufgelöst wurde, bevor Cmdlets für die Bereitstellung von Ressourcengruppen ausgeführt wurden</span><span class="sxs-lookup"><span data-stu-id="31e1b-1681">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="31e1b-1682">Az.Resources: Richtige Dokumentation für Standardwert von „New-AzureRmPolicyDefinition -Mode“ bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1682">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="31e1b-1683">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="31e1b-1683">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="31e1b-1684">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="31e1b-1684">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="31e1b-1685">Formatierungsproblem für Objekt „PSResourceGroupDeployment“ behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-1685">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="31e1b-1686">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="31e1b-1686">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="31e1b-1687">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="31e1b-1687">Az.ServiceFabric</span></span>
* <span data-ttu-id="31e1b-1688">Rollback beim Hinzufügen eines Zertifikats zum VMSS-Modell, Auslösung einer Ausnahme. Fehlerbehebung: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="31e1b-1688">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="31e1b-1689">Einige Fehlermeldungen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1689">Fix some error messages.</span></span>
* <span data-ttu-id="31e1b-1690">Fehler bei Clustererstellung mit ARM-Standardvorlage für „New-AzServiceFabriCluster“ behoben, bei dem die Migration zu Az nicht funktioniert hat.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1690">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="31e1b-1691">Fehler behoben beim Hinzufügen eines Cluster-/Anwendungszertifikats ausschließlich zu VM Scale Sets, die zum Cluster gehören, indem die Cluster-ID in der Erweiterung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1691">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="31e1b-1692">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="31e1b-1692">Az.SignalR</span></span>
* <span data-ttu-id="31e1b-1693">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1693">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="31e1b-1694">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31e1b-1694">Az.Sql</span></span>
* <span data-ttu-id="31e1b-1695">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1695">Update incorrect online help URLs</span></span>
* <span data-ttu-id="31e1b-1696">Parameterbeschreibung für den Parameter „LicenseType“ mit möglichen Werten aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1696">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="31e1b-1697">Fehler behoben, bei dem die Aktualisierung der Identität der verwalteten Instanz nicht funktioniert hat, wenn es sich um die einzige aktualisierte Eigenschaft gehandelt hat</span><span class="sxs-lookup"><span data-stu-id="31e1b-1697">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="31e1b-1698">Unterstützung für die benutzerdefinierte Sortierung auf verwalteter Instanz</span><span class="sxs-lookup"><span data-stu-id="31e1b-1698">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="31e1b-1699">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="31e1b-1699">Az.Storage</span></span>
* <span data-ttu-id="31e1b-1700">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1700">Update incorrect online help URLs</span></span>
* <span data-ttu-id="31e1b-1701">Ausführliche Fehlermeldung beim Abrufen/Festlegen der klassischen Protokollierung bzw. Metriken für Storage Premium-Konto, da für das Storage Premium-Konto die klassische Protokollierung bzw. Metriken nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1701">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="31e1b-1702">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="31e1b-1702">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="31e1b-1703">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="31e1b-1703">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="31e1b-1704">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="31e1b-1704">Az.TrafficManager</span></span>
* <span data-ttu-id="31e1b-1705">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1705">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="31e1b-1706">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="31e1b-1706">Az.Websites</span></span>
* <span data-ttu-id="31e1b-1707">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1707">Update incorrect online help URLs</span></span>
* <span data-ttu-id="31e1b-1708">„New-AzWebAppSSLBinding“ korrigiert, damit das Zertifikat in die richtige Ressourcengruppe bzw. an den richtigen Speicherort hochgeladen wird, wenn die App in einer ASE gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1708">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="31e1b-1709">„New-AzWebAppSSLBinding“ korrigiert, damit die Tags beim Binden eines SSL-Zertifikats an eine App nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1709">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="31e1b-1710">1.1.0 – Januar 2019</span><span class="sxs-lookup"><span data-stu-id="31e1b-1710">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="31e1b-1711">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="31e1b-1711">Az.Accounts</span></span>
* <span data-ttu-id="31e1b-1712">Bereich „Local“ zu „Enable-AzureRmAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1712">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31e1b-1713">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31e1b-1713">Az.Compute</span></span>
* <span data-ttu-id="31e1b-1714">Name ist jetzt optional im ID-Parametersatz für „Restart/Start/Stop/Remove/Set-AzVM“ und „Save-AzVMImage“</span><span class="sxs-lookup"><span data-stu-id="31e1b-1714">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="31e1b-1715">Beschreibung der ID in Hilfedateien aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1715">Updated the description of ID in help files</span></span>
* <span data-ttu-id="31e1b-1716">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-1716">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="31e1b-1717">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="31e1b-1717">Az.DataLakeStore</span></span>
* <span data-ttu-id="31e1b-1718">Aktualisierung der SDK-Version der Datenebene auf 1.1.14 für SDK-Fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1718">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="31e1b-1719">Behandlung von negativen acesstime- and modificationtime-Werten für „getfilestatus“ und „liststatus“ korrigiert, asynchrones Abbruchtoken korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1719">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="31e1b-1720">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="31e1b-1720">Az.EventGrid</span></span>
* <span data-ttu-id="31e1b-1721">Zur Verwendung der API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1721">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="31e1b-1722">Aktualisierung der folgenden Cmdlets zur Unterstützung des neuen Szenarios in der API-Version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="31e1b-1722">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="31e1b-1723">New-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="31e1b-1723">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="31e1b-1724">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="31e1b-1724">Event Time-To-Live,</span></span>
        - <span data-ttu-id="31e1b-1725">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="31e1b-1725">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="31e1b-1726">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="31e1b-1726">Dead letter endpoint.</span></span>
    - <span data-ttu-id="31e1b-1727">Update-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="31e1b-1727">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="31e1b-1728">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="31e1b-1728">Event Time-To-Live,</span></span>
        - <span data-ttu-id="31e1b-1729">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="31e1b-1729">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="31e1b-1730">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="31e1b-1730">Dead letter endpoint.</span></span>
* <span data-ttu-id="31e1b-1731">Neue Enumerationswerte („storageQueue“ und „hybridConnection“) für die EndpointType-Option in den Cmdlets „New-AzureRmEventGridSubscription“ und „Update-AzureRmEventGridSubscription“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1731">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="31e1b-1732">Anzeige einer Warnmeldung, wenn das Erstellen oder Aktualisieren des Ereignisabonnements voraussichtlich eine manuelle Aktion des Benutzers zur Folge hat</span><span class="sxs-lookup"><span data-stu-id="31e1b-1732">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="31e1b-1733">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="31e1b-1733">Az.IotHub</span></span>
* <span data-ttu-id="31e1b-1734">Auf die aktuelle Version des Iot Hub SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1734">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="31e1b-1735">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="31e1b-1735">Az.LogicApp</span></span>
* <span data-ttu-id="31e1b-1736">„Get-AzLogicApp“ listet alle Apps ohne angegebenen Namen auf</span><span class="sxs-lookup"><span data-stu-id="31e1b-1736">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="31e1b-1737">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31e1b-1737">Az.Resources</span></span>
* <span data-ttu-id="31e1b-1738">Problem mit dem Parametersatz bei Angabe der Parameter „-ODataQuery“ und „-ResourceId“ für „Get-AzResource“ behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-1738">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="31e1b-1739">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="31e1b-1739">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="31e1b-1740">Behandlung des Parameters „-Custom“ in „New/Set-AzPolicyDefinition“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1740">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="31e1b-1741">Tippfehler in der Dokumentation für „New-AzDeployment“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1741">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="31e1b-1742">Parameter „-MailNickname“ als obligatorisch festgelegt für „New-AzADUser“</span><span class="sxs-lookup"><span data-stu-id="31e1b-1742">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="31e1b-1743">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="31e1b-1743">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="31e1b-1744">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="31e1b-1744">Az.SignalR</span></span>
* <span data-ttu-id="31e1b-1745">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-1745">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="31e1b-1746">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31e1b-1746">Az.Sql</span></span>
* <span data-ttu-id="31e1b-1747">Abhängigkeit des Speicherverwaltungsclients zur allgemeinen SDK-Implementierung konvertiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1747">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="31e1b-1748">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="31e1b-1748">Az.Storage</span></span>
* <span data-ttu-id="31e1b-1749">Festlegung des „StorageAccountName“ des Speicherkontexts als tatsächlichen Namen des Speicherkontos, wenn dieser mit „SAS-Token“, „OAuth“ oder „Anonym“ erstellt wird</span><span class="sxs-lookup"><span data-stu-id="31e1b-1749">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="31e1b-1750">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="31e1b-1750">New-AzStorageContext</span></span>
* <span data-ttu-id="31e1b-1751">Erstellen von SAS-Token des Blob-Momentaufnahmeobjekts mit dem Parameter „-FullUri“, Festlegung des zurückgegebenen URI als Momentaufnahme-URI</span><span class="sxs-lookup"><span data-stu-id="31e1b-1751">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="31e1b-1752">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="31e1b-1752">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="31e1b-1753">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="31e1b-1753">Az.Websites</span></span>
* <span data-ttu-id="31e1b-1754">Fehler bei der Datumsanalyse in „Get-AzDeletedWebApp“ behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-1754">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="31e1b-1755">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-1755">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="31e1b-1756">1.0.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="31e1b-1756">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="31e1b-1757">Allgemein</span><span class="sxs-lookup"><span data-stu-id="31e1b-1757">General</span></span>

- <span data-ttu-id="31e1b-1758">Allgemeine Verfügbarkeit des Az-Moduls</span><span class="sxs-lookup"><span data-stu-id="31e1b-1758">General Availability of Az Module</span></span>
- <span data-ttu-id="31e1b-1759">Onlinehilfe für jedes Modul</span><span class="sxs-lookup"><span data-stu-id="31e1b-1759">Online help for each module</span></span>
- <span data-ttu-id="31e1b-1760">Ausführlichere Informationen und eine Roadmap finden Sie auf der [Seite mit der Ankündigung zu Az](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="31e1b-1760">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="31e1b-1761">Informationen zur Migration aus AzureRM finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="31e1b-1761">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="31e1b-1762">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="31e1b-1762">Az.Accounts</span></span>
- <span data-ttu-id="31e1b-1763">Geändert von Az.Profile</span><span class="sxs-lookup"><span data-stu-id="31e1b-1763">Changed from Az.Profile</span></span>
- <span data-ttu-id="31e1b-1764">Feste Tabellenformate für Profil- und Kontexttypen</span><span class="sxs-lookup"><span data-stu-id="31e1b-1764">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="31e1b-1765">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="31e1b-1765">Az.ApiManagement</span></span>
- <span data-ttu-id="31e1b-1766">Korrekturen für #7002</span><span class="sxs-lookup"><span data-stu-id="31e1b-1766">Fixes for #7002</span></span>
- <span data-ttu-id="31e1b-1767">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="31e1b-1767">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="31e1b-1768">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="31e1b-1768">Az.Batch</span></span>
- <span data-ttu-id="31e1b-1769">Möglichkeit zum Anzeigen der ausgeführten Version des Azure Batch-Knoten-Agents auf den VMs eines Pools mit der neuen `NodeAgentInformation`-Eigenschaft für `PSComputeNode` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1769">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="31e1b-1770">Der `Caching`-Standardwert für `PSDataDisk` lautet jetzt nicht mehr `None`, sondern `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1770">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="31e1b-1771">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="31e1b-1771">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="31e1b-1772">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="31e1b-1772">Az.Billing</span></span>
- <span data-ttu-id="31e1b-1773">Kombination von Billing-, Consumption- und UsageAggregates-Cmdlets. Ausführliche Informationen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="31e1b-1773">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="31e1b-1774">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="31e1b-1774">Az.CognitivServices</span></span>
- <span data-ttu-id="31e1b-1775">Vervollständigungen für SkuName und Typem für den Vorgang New-AzureRmCognitiveServicesAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1775">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="31e1b-1776">GetSkusWithAccountParamSetName-Parametersatz aus Get-AzCognitiveServicesAccountSkus entfernt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1776">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="31e1b-1777">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="31e1b-1777">Az.ContainerInstance</span></span>
- <span data-ttu-id="31e1b-1778">ManagedIdentity-Unterstützung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1778">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="31e1b-1779">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="31e1b-1779">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="31e1b-1780">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="31e1b-1780">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="31e1b-1781">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="31e1b-1781">Az.DataLakeStore</span></span>
- <span data-ttu-id="31e1b-1782">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="31e1b-1782">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="31e1b-1783">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="31e1b-1783">Az.Monitor</span></span>
- <span data-ttu-id="31e1b-1784">Az.Insights in Az.Monitor umbenannt und weitere weniger wichtige grundlegende Änderungen durchgeführt. Informationen hierzu finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="31e1b-1784">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="31e1b-1785">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="31e1b-1785">Az.KeyVault</span></span>
- <span data-ttu-id="31e1b-1786">Veraltete PurgeDisabled-Eigenschaft aus Ausgabetypen entfernt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1786">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="31e1b-1787">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="31e1b-1787">Az.MachineLearning</span></span>
- <span data-ttu-id="31e1b-1788">Cmdlets des Az.MachineLearningCompute-Moduls eingebunden</span><span class="sxs-lookup"><span data-stu-id="31e1b-1788">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="31e1b-1789">Az.Media</span><span class="sxs-lookup"><span data-stu-id="31e1b-1789">Az.Media</span></span>
- <span data-ttu-id="31e1b-1790">Veralteten -Tags-Alias aus New-AzMediaService entfernt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1790">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="31e1b-1791">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31e1b-1791">Az.Network</span></span>
<span data-ttu-id="31e1b-1792">Unterstützung für das Konfigurieren von RewriteRuleSets im Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1792">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="31e1b-1793">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="31e1b-1793">New cmdlets added:</span></span>
        - <span data-ttu-id="31e1b-1794">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="31e1b-1794">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="31e1b-1795">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="31e1b-1795">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="31e1b-1796">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="31e1b-1796">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="31e1b-1797">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="31e1b-1797">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="31e1b-1798">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="31e1b-1798">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="31e1b-1799">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="31e1b-1799">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="31e1b-1800">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="31e1b-1800">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="31e1b-1801">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="31e1b-1801">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="31e1b-1802">Cmdlets mit optionalem Parameter -RewriteRuleSet aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1802">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="31e1b-1803">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="31e1b-1803">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="31e1b-1804">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="31e1b-1804">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="31e1b-1805">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="31e1b-1805">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="31e1b-1806">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="31e1b-1806">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="31e1b-1807">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="31e1b-1807">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="31e1b-1808">New-AzureRmApplicationGatewayUrlPathMapConfig: KeyVault-Unterstützung mithilfe von Identität zum Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1808">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="31e1b-1809">Cmdlets mit optionalem Parameter aktualisiert: -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="31e1b-1809">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="31e1b-1810">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="31e1b-1810">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="31e1b-1811">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="31e1b-1811">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="31e1b-1812">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="31e1b-1812">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="31e1b-1813">Cmdlet New-AzApplicationGateway mit optionalem Parameter -UserAssignedIdentity aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1813">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="31e1b-1814">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="31e1b-1814">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="31e1b-1815">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="31e1b-1815">Az.OperationalInsights</span></span>
- <span data-ttu-id="31e1b-1816">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="31e1b-1816">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="31e1b-1817">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="31e1b-1817">Az.Profile</span></span>
- <span data-ttu-id="31e1b-1818">Modulnamen in Az.Accounts geändert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1818">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="31e1b-1819">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="31e1b-1819">Az.RecoveryServices</span></span>
- <span data-ttu-id="31e1b-1820">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="31e1b-1820">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="31e1b-1821">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31e1b-1821">Az.Resources</span></span>
- <span data-ttu-id="31e1b-1822">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="31e1b-1822">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="31e1b-1823">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="31e1b-1823">Az.ServiceFabric</span></span>
- <span data-ttu-id="31e1b-1824">Unterstützung für das Angeben des Zertifikats anhand des allgemeinen Namens und Fingerabdrucks</span><span class="sxs-lookup"><span data-stu-id="31e1b-1824">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="31e1b-1825">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="31e1b-1825">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="31e1b-1826">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="31e1b-1826">Az.SIgnalR</span></span>
- <span data-ttu-id="31e1b-1827">Allgemeine Verfügbarkeit für PowerShell-Cmdlets für SIgnalR</span><span class="sxs-lookup"><span data-stu-id="31e1b-1827">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="31e1b-1828">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31e1b-1828">Az.Sql</span></span>
- <span data-ttu-id="31e1b-1829">Neue Erkennungstypen Data_Exfiltration und Unsafe_Action zu Cmdlets für Bedrohungserkennung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1829">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="31e1b-1830">Dokumentationsbeispiele für Cmdlets für SQL-Überwachung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1830">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="31e1b-1831">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="31e1b-1831">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="31e1b-1832">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="31e1b-1832">Az.Storage</span></span>
- <span data-ttu-id="31e1b-1833">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="31e1b-1833">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="31e1b-1834">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="31e1b-1834">Az.Websites</span></span>
- <span data-ttu-id="31e1b-1835">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="31e1b-1835">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="31e1b-1836">0.7.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="31e1b-1836">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="31e1b-1837">Allgemein</span><span class="sxs-lookup"><span data-stu-id="31e1b-1837">General</span></span>

* <span data-ttu-id="31e1b-1838">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="31e1b-1838">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="31e1b-1839">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31e1b-1839">Az.Compute</span></span>

* <span data-ttu-id="31e1b-1840">Unterstützung für UltraSSD und Katalogimages in einfachen Parametersätzen für `New-AzVm(ss)`-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1840">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="31e1b-1841">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="31e1b-1841">Az.DataLakeStore</span></span>

* <span data-ttu-id="31e1b-1842">Nachgestellten Schrägstrich für die Domäne des ADLS-Kontos korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1842">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="31e1b-1843">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="31e1b-1843">Az.FrontDoor</span></span>

* <span data-ttu-id="31e1b-1844">Einige fehlerhafte Links behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-1844">Fixed some broken links</span></span>
    - <span data-ttu-id="31e1b-1845">In den Artikeln zu New-AzureRmFrontDoor und Set-AzureRmFrontDoor den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorHealthProbeSettingObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1845">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="31e1b-1846">Im Artikel zu New-AzureRmFrontDoorManagedRuleObject den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorRuleGroupOverrideObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1846">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="31e1b-1847">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="31e1b-1847">Az.RecoveryServices</span></span>

* <span data-ttu-id="31e1b-1848">Clientseitige Validierungen für Wiederherstellungsvorgänge von Azure-Dateifreigaben hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1848">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="31e1b-1849">storageAccountName und storageAccountResourceGroupName für AFS-Wiederherstellung optional gemacht.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1849">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="31e1b-1850">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31e1b-1850">Az.Resources</span></span>

* <span data-ttu-id="31e1b-1851">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="31e1b-1851">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="31e1b-1852">Get-AzureRmRoleAssignment für die Verwendung des Abonnementbereichs aktualisiert, wenn dieser beim Anfordern von klassischen Administratoren angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1852">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="31e1b-1853">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31e1b-1853">Az.Sql</span></span>

* <span data-ttu-id="31e1b-1854">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="31e1b-1854">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="31e1b-1855">Problem mit der Verwendung von Get-AzureRmSqlDatabaseVulnerabilityAssessment mit .NET Core behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-1855">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="31e1b-1856">Dokumentation mit Hilfemeldungen zu Cmdlets für die SQL-Überwachung geändert.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1856">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="31e1b-1857">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="31e1b-1857">Az.Storage</span></span>

* <span data-ttu-id="31e1b-1858">-EnableHierarchicalNamespace zu New-AzureRmStorageAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1858">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="31e1b-1859">Problem behoben, bei dem für das Copy File-Cmdlet am Ziel kein Quellkontext wiederverwendet werden kann, wenn -DestContext nicht eingegeben wird</span><span class="sxs-lookup"><span data-stu-id="31e1b-1859">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="31e1b-1860">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="31e1b-1860">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="31e1b-1861">Unterstützung der Konfiguration von statischen Websites</span><span class="sxs-lookup"><span data-stu-id="31e1b-1861">Support Static Website configuration</span></span>
    - <span data-ttu-id="31e1b-1862">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="31e1b-1862">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="31e1b-1863">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="31e1b-1863">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="31e1b-1864">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="31e1b-1864">Az.Websites</span></span>

* <span data-ttu-id="31e1b-1865">Set-AzureRmWebApp und Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="31e1b-1865">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="31e1b-1866">Neuen Parameter (-AzureStoragePath) zum Angeben von Azure Storage-Pfaden hinzugefügt, die in Windows- und Linux-Container-Apps bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1866">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="31e1b-1867">Verwenden Sie die Ausgabe des neuen Cmdlets New-AzureRmWebAppAzureStoragePath als Parameter zum Festlegen der Azure Storage-Pfade.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1867">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="31e1b-1868">0.6.1 – November 2018</span><span class="sxs-lookup"><span data-stu-id="31e1b-1868">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="31e1b-1869">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="31e1b-1869">Az.ApiManagement</span></span>
* <span data-ttu-id="31e1b-1870">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1870">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="31e1b-1871">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="31e1b-1871">Az.Automation</span></span>
* <span data-ttu-id="31e1b-1872">Swagger-basierte Azure Automation-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="31e1b-1872">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="31e1b-1873">Cmdlets zur Updateverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1873">Added Update Management cmdlets</span></span>
* <span data-ttu-id="31e1b-1874">Cmdlets zur Quellcodeverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1874">Added Source Control cmdlets</span></span>
* <span data-ttu-id="31e1b-1875">Cmdlet „Remove-AzureRmAutomationHybridWorkerGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1875">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="31e1b-1876">DSC-Befehl für die Knotenregistrierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1876">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="31e1b-1877">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31e1b-1877">Az.Compute</span></span>
* <span data-ttu-id="31e1b-1878">Identitätsproblem für SystemAssigned-Identität korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1878">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="31e1b-1879">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1879">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="31e1b-1880">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="31e1b-1880">Az.ContainerInstance</span></span>
* <span data-ttu-id="31e1b-1881">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1881">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="31e1b-1882">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="31e1b-1882">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="31e1b-1883">Beschreibung der Beispiele für Marketplace-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1883">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="31e1b-1884">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31e1b-1884">Az.Network</span></span>
* <span data-ttu-id="31e1b-1885">Folgende Cmdlets hinzugefügt: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="31e1b-1885">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="31e1b-1886">ICMP wieder unterstützten AzureFirewall-Netzwerkprotokollen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1886">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="31e1b-1887">Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert und Überprüfung für Ziel-ID, Adresse und Port hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1887">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="31e1b-1888">Probleme mit Arbeitsspeicherauslastung in der VirtualNetwork-Zuordnung behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-1888">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="31e1b-1889">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="31e1b-1889">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="31e1b-1890">Problem beim Ändern der Richtlinie für eine geschützte Dateifreigabe behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-1890">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="31e1b-1891">Richtlinienzeitzone in Großschreibung geändert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1891">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="31e1b-1892">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="31e1b-1892">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="31e1b-1893">Korrigiertes Beispiel in „New-AzureRmRecoveryServicesAsrProtectableItem“</span><span class="sxs-lookup"><span data-stu-id="31e1b-1893">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="31e1b-1894">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1894">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="31e1b-1895">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="31e1b-1895">Az.Relay</span></span>
* <span data-ttu-id="31e1b-1896">Optionaler Parameter „-KeyValue“ zu Cmdlet „New-AzureRmRelayKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht</span><span class="sxs-lookup"><span data-stu-id="31e1b-1896">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="31e1b-1897">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31e1b-1897">Az.Resources</span></span>
* <span data-ttu-id="31e1b-1898">Hilfedokumentation für ressourcenidentitätsbezogene Parameter in `New-AzureRmPolicyAssignment` und `Set-AzureRmPolicyAssignment` aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1898">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="31e1b-1899">Beispiel für „New-AzureRmPolicyDefinition“ hinzugefügt, das „-Metadata“ nutzt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1899">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="31e1b-1900">Korrektur, um Beibehaltung von Groß-/Kleinschreibung in Tagschlüsseln in „NetStandard“ zu ermöglichen: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="31e1b-1900">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="31e1b-1901">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="31e1b-1901">Az.ServiceFabric</span></span>
* <span data-ttu-id="31e1b-1902">Benachrichtigung über veraltete Elemente für anstehende wichtige Änderungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1902">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="31e1b-1903">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31e1b-1903">Az.Sql</span></span>
* <span data-ttu-id="31e1b-1904">Neue Cmdlets für CRUD-Vorgänge in verwalteten Azure SQL-Datenbank-Instanzen und verwalteten Azure SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1904">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="31e1b-1905">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="31e1b-1905">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="31e1b-1906">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="31e1b-1906">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="31e1b-1907">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="31e1b-1907">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="31e1b-1908">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="31e1b-1908">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="31e1b-1909">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="31e1b-1909">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="31e1b-1910">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="31e1b-1910">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="31e1b-1911">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="31e1b-1911">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="31e1b-1912">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="31e1b-1912">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="31e1b-1913">Erweiterte Verwaltung von Überwachungsrichtlinien auf einem Server oder in einer Datenbank aktiviert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1913">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="31e1b-1914">Neuer Parameter (PredicateExpression) hinzugefügt, um die Filterung von Überwachungsprotokollen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="31e1b-1914">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="31e1b-1915">Cmdlets wurden angepasst, sodass sie SQL-Clients anstelle von Legacyclients verwenden.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1915">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="31e1b-1916">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="31e1b-1916">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="31e1b-1917">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="31e1b-1917">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="31e1b-1918">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="31e1b-1918">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="31e1b-1919">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="31e1b-1919">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="31e1b-1920">Problem bei Verwendung von „Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings“ mit festgelegtem Parameter für den Speicherkontonamen behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-1920">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="31e1b-1921">0.5.0 – November 2018</span><span class="sxs-lookup"><span data-stu-id="31e1b-1921">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="31e1b-1922">Allgemein</span><span class="sxs-lookup"><span data-stu-id="31e1b-1922">General</span></span>
* <span data-ttu-id="31e1b-1923">Ressourcenvervollständigungen für viele Kern-Cmdlets hinzugefügt (diese ermöglichen das Durchlaufen von vorhandenen Ressourcennamen per TAB-TASTE, wenn Cmdlets interaktiv aufgerufen werden)</span><span class="sxs-lookup"><span data-stu-id="31e1b-1923">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="31e1b-1924">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="31e1b-1924">Az.Profile</span></span>
* <span data-ttu-id="31e1b-1925">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="31e1b-1925">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="31e1b-1926">Parameter „TenantId“ im Cmdlet „Connect-AzAccount“ in „Tenant“ umbenannt und Alias für „TenantId“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1926">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="31e1b-1927">Beschreibung von „TenantId“ für „Connect-AzAccount“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1927">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="31e1b-1928">Fehlermeldung für fehlgeschlagene Anmeldung bei Angabe der Mandantendomäne korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1928">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="31e1b-1929">Problem in Bezug auf Kontextnamenskonflikt für Konten ohne Abonnements im Mandanten behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-1929">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="31e1b-1930">Problem mit DataLake-Endpunkten bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-1930">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="31e1b-1931">Problem behoben, das zur Auslösung von „Disconnect-AzAccount“ führte, wenn keine Verbindung bestand</span><span class="sxs-lookup"><span data-stu-id="31e1b-1931">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="31e1b-1932">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="31e1b-1932">Az.CognitiveServices</span></span>
* <span data-ttu-id="31e1b-1933">Vorgang „Get-AzCognitiveServicesAccountSkus“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1933">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31e1b-1934">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31e1b-1934">Az.Compute</span></span>
* <span data-ttu-id="31e1b-1935">Cmdlets Add-AzVmssVMDataDisk und Remove-AzVmssVMDataDisk hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1935">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="31e1b-1936">„Get-AzVMImage“ zeigt „AutomaticOSUpgradeProperties“ an</span><span class="sxs-lookup"><span data-stu-id="31e1b-1936">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="31e1b-1937">Problem behoben, aufgrund dessen die Optionswerte „SetAzVMChefExtension -BootstrapOptions“ und „-JsonAttribute“ nicht im JSON-Format festgelegt wurden</span><span class="sxs-lookup"><span data-stu-id="31e1b-1937">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="31e1b-1938">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="31e1b-1938">Az.DataLakeStore</span></span>
* <span data-ttu-id="31e1b-1939">Aktualisierung des DataLake-Pakets auf 1.1.10</span><span class="sxs-lookup"><span data-stu-id="31e1b-1939">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="31e1b-1940">Standardmäßige Parallelität zu Multithreadvorgängen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1940">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="31e1b-1941">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="31e1b-1941">Az.Insights</span></span>
* <span data-ttu-id="31e1b-1942">Problem Nr. 7267 behoben (Bereich für automatische Skalierung)</span><span class="sxs-lookup"><span data-stu-id="31e1b-1942">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="31e1b-1943">Probleme beim Erstellen einer neuen Regel für die automatische Skalierung, aufgrund derer die aufgelisteten Parameter nicht richtig festgelegt wurden (Es wurde stets der Standardwert festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="31e1b-1943">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="31e1b-1944">Problem Nr. 7513 behoben [Insights] „Set-AzDiagnosticSetting“ erfordert die explizite Angabe von Kategorien während der Erstellung der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1944">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="31e1b-1945">Nun erfordert das Cmdlet nicht die explizite Angabe der Kategorien, die während der Erstellung aktiviert werden sollen. Das bedeutet, es funktioniert wie dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1945">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31e1b-1946">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31e1b-1946">Az.Network</span></span>
* <span data-ttu-id="31e1b-1947">„PeeringType“ wurde geändert und ist nun ein erforderlicher Parameter für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="31e1b-1947">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="31e1b-1948">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="31e1b-1948">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="31e1b-1949">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="31e1b-1949">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="31e1b-1950">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="31e1b-1950">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="31e1b-1951">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="31e1b-1951">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="31e1b-1952">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="31e1b-1952">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="31e1b-1953">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="31e1b-1953">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="31e1b-1954">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="31e1b-1954">Az.PolicyInsights</span></span>
* <span data-ttu-id="31e1b-1955">Cmdlets für Richtlinienwartung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1955">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="31e1b-1956">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31e1b-1956">Az.Resources</span></span>
* <span data-ttu-id="31e1b-1957">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="31e1b-1957">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="31e1b-1958">Zulassen der Auflistung von Ressourcen mithilfe des Parameters „-ResourceId“ für „Get-AzResource“</span><span class="sxs-lookup"><span data-stu-id="31e1b-1958">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="31e1b-1959">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="31e1b-1959">Az.ServiceBus</span></span>
* <span data-ttu-id="31e1b-1960">Schreibgeschützte Eigenschaft „MigrationState“ zu „PSServiceBusMigrationConfigurationAttributes“ hinzugefügt, was das Ermitteln des Migrationsstatus ermöglicht</span><span class="sxs-lookup"><span data-stu-id="31e1b-1960">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="31e1b-1961">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="31e1b-1961">Az.ServiceFabric</span></span>
* <span data-ttu-id="31e1b-1962">Hinzufügen des Zertifikats zu Linux VMSS korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1962">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="31e1b-1963">„Add-AzServiceFabricClusterCertificate“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="31e1b-1963">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="31e1b-1964">Verwenden des richtigen Fingerabdrucks aus dem neuen Zertifikat (Azure/service-fabric-issues#932)</span><span class="sxs-lookup"><span data-stu-id="31e1b-1964">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="31e1b-1965">Richtige Anzeige von Ausnahmen (Azure/service-fabric-issues#1054)</span><span class="sxs-lookup"><span data-stu-id="31e1b-1965">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="31e1b-1966">„Update-AzServiceFabricDurability“ korrigiert, um die Clusterkonfiguration zu aktualisieren, bevor der VMSS-Vorgang „CreateOrUpdate“ gestartet wird</span><span class="sxs-lookup"><span data-stu-id="31e1b-1966">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="31e1b-1967">0.4.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="31e1b-1967">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="31e1b-1968">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="31e1b-1968">Az.Profile</span></span>
* <span data-ttu-id="31e1b-1969">Problem mit „Get-AzSubscription“ in Cloud Shell behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-1969">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="31e1b-1970">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="31e1b-1970">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31e1b-1971">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31e1b-1971">Az.Compute</span></span>
* <span data-ttu-id="31e1b-1972">Neue Größen zur Whitelist von VM-Größen hinzugefügt, für die bei Verwendung des einfachen Parametersatzes für „New-AzVm“ der beschleunigte Netzwerkbetrieb aktiviert wird</span><span class="sxs-lookup"><span data-stu-id="31e1b-1972">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="31e1b-1973">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1973">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="31e1b-1974">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="31e1b-1974">Az.DataLakeStore</span></span>
* <span data-ttu-id="31e1b-1975">Unterstützung für VNET-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-1975">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="31e1b-1976">Get-AzDataLakeStoreVirtualNetworkRule: Dient zum Abrufen oder Auflisten der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1976">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="31e1b-1977">Add-AzDataLakeStoreVirtualNetworkRule: Fügt dem angegebenen Data Lake Store-Konto eine Regel für das virtuelle Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1977">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="31e1b-1978">Set-AzDataLakeStoreVirtualNetworkRule: Ändert die angegebene Regel für das virtuelle Netzwerk in das angegebene Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1978">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="31e1b-1979">Remove-AzDataLakeStoreVirtualNetworkRule: Dient zum Löschen der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1979">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31e1b-1980">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31e1b-1980">Az.Network</span></span>
* <span data-ttu-id="31e1b-1981">Cmdlet „Test-AzNetworkWatcherConnectivity“ aktualisiert, Protokollwert wird jetzt an Back-End übergeben.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1981">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="31e1b-1982">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1982">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="31e1b-1983">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31e1b-1983">Az.Resources</span></span>
* <span data-ttu-id="31e1b-1984">Problem behoben, aufgrund dessen „Get-AzRoleDefinition“ eine unverständliche Ausnahme auslöst (wenn das Standardprofil kein Abonnement enthält und kein Bereich festgelegt ist), indem im Szenario eine aussagekräftige Ausnahme hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1984">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="31e1b-1985">Außerdem wurde der Standardparametersatz auf „RoleDefinitionNameParameterSet“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1985">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="31e1b-1986">0.3.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="31e1b-1986">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="31e1b-1987">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="31e1b-1987">Azure.Storage</span></span>
* <span data-ttu-id="31e1b-1988">Fehler beim Kopieren von Blobs/Dateien behoben, aufgrund dessen bei einem Metadatenproblem des Ziels keine Metadaten kopiert wurden</span><span class="sxs-lookup"><span data-stu-id="31e1b-1988">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="31e1b-1989">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="31e1b-1989">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="31e1b-1990">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="31e1b-1990">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="31e1b-1991">Der Abruf der Speicherressourcennutzung eines bestimmten Standorts wird jetzt unterstützt, und das Hinzufügen einer Warnmeldung für den Abruf der globalen Speicherressourcennutzung ist überflüssig.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1991">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="31e1b-1992">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="31e1b-1992">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="31e1b-1993">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="31e1b-1993">Az.CognitiveServices</span></span>
* <span data-ttu-id="31e1b-1994">„Get-AzCognitiveServicesAccountSkus“ wird ohne vorhandenes Konto unterstützt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1994">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31e1b-1995">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31e1b-1995">Az.Compute</span></span>
* <span data-ttu-id="31e1b-1996">Korrektur von „Get-AzVM -ResourceGroupName <rg>“, sodass ggf. mehr als 50 Ergebnisse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="31e1b-1996">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="31e1b-1997">Der Cmdlet-Hilfe zu „New-AzVmss“ wurde ein Beispiel für „SimpleParameterSet“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-1997">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="31e1b-1998">Tippfehler in der Azure Disk Encryption-Statusmeldung behoben</span><span class="sxs-lookup"><span data-stu-id="31e1b-1998">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="31e1b-1999">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="31e1b-1999">Az.DataFactoryV2</span></span>
* <span data-ttu-id="31e1b-2000">Die Version des ADF .Net-SDK wurde auf 2.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="31e1b-2000">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31e1b-2001">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31e1b-2001">Az.Network</span></span>
* <span data-ttu-id="31e1b-2002">NetworkProfile-Funktionalität wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31e1b-2002">Added NetworkProfile functionality.</span></span> <span data-ttu-id="31e1b-2003">Neue Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-2003">new cmdlets added</span></span>
    - <span data-ttu-id="31e1b-2004">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="31e1b-2004">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="31e1b-2005">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="31e1b-2005">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="31e1b-2006">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="31e1b-2006">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="31e1b-2007">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="31e1b-2007">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="31e1b-2008">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="31e1b-2008">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="31e1b-2009">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="31e1b-2009">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="31e1b-2010">Dienstzuordnungslink in Subnetzmodell hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-2010">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="31e1b-2011">Cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-2011">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="31e1b-2012">Cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-2012">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="31e1b-2013">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="31e1b-2013">Az.RedisCache</span></span>
* <span data-ttu-id="31e1b-2014">Künftig sind beliebige Zeichenfolgen als Größenparameter zulässig.</span><span class="sxs-lookup"><span data-stu-id="31e1b-2014">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="31e1b-2015">P5 in Popup „PSArgumentCompleter“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-2015">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="31e1b-2016">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31e1b-2016">Az.Resources</span></span>
* <span data-ttu-id="31e1b-2017">Fehlender Parameter „-Mode“ zu „Set-AzPolicyDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="31e1b-2017">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="31e1b-2018">Cmdlet-Fehler bei „Get-AzProviderOperation“ für Vorgänge mit Ursprung behoben, der den Benutzer enthält</span><span class="sxs-lookup"><span data-stu-id="31e1b-2018">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="31e1b-2019">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31e1b-2019">Az.Sql</span></span>
* <span data-ttu-id="31e1b-2020">Problem behoben, aufgrund dessen einige Sicherungs-Cmdlets das aktuelle Azure-Abonnements nicht erkannt haben</span><span class="sxs-lookup"><span data-stu-id="31e1b-2020">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="31e1b-2021">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="31e1b-2021">Az.Websites</span></span>
* <span data-ttu-id="31e1b-2022">Neues Cmdlet „Get-AzWebAppContainerContinuousDeploymentUrl“ zum Abrufen der Webhook-URL von Continuous Deployment für Container</span><span class="sxs-lookup"><span data-stu-id="31e1b-2022">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="31e1b-2023">Neue Cmdlets „New-AzWebAppContainerPSSession“ und „Enter-WebAppContainerPSSession“ zum Initiieren einer PowerShell-Remotesitzung in einer Windows-Container-App</span><span class="sxs-lookup"><span data-stu-id="31e1b-2023">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="31e1b-2024">0.2.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="31e1b-2024">0.2.0 - September 2018</span></span>
 <span data-ttu-id="31e1b-2025">Erstrelease</span><span class="sxs-lookup"><span data-stu-id="31e1b-2025">Initial Release</span></span>
