---
title: Versionshinweise zu Azure PowerShell
description: Hier erfahren Sie mehr über die aktuellen Updates für die Azure PowerShell-Module.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: 9e60e76206127922902804112e0b3f837cf03d76
ms.sourcegitcommit: eeb720e053939a68873ae3973bc81d5826358c9f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2020
ms.locfileid: "80440502"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="86269-103">Versionshinweise zu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="86269-103">Azure PowerShell release notes</span></span>
## <a name="370---march-2020"></a><span data-ttu-id="86269-104">3.7.0: März 2020</span><span class="sxs-lookup"><span data-stu-id="86269-104">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="86269-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86269-105">Az.Accounts</span></span>
* <span data-ttu-id="86269-106">„Get-AzTenant“/„Get-AzDefault“/„Set-AzDefault“: Bei fehlender Anmeldung ausgelöste Ausnahme „NullReferenceException“ korrigiert [Nr. 10292]</span><span class="sxs-lookup"><span data-stu-id="86269-106">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86269-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86269-107">Az.Compute</span></span>
* <span data-ttu-id="86269-108">Folgende Parameter zum Cmdlet „New-AzDiskConfig“ hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="86269-108">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span> 
    - <span data-ttu-id="86269-109">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="86269-109">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="86269-110">Verschlüsselungseigenschaft für Zielparameter des Cmdlets „New-AzGalleryImageVersion“ zugelassen</span><span class="sxs-lookup"><span data-stu-id="86269-110">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="86269-111">Problem „tempDisk“ für Cmdlets „Set-AzVmss' -Reimage“ und „Invoke-AzVMReimage“ behoben</span><span class="sxs-lookup"><span data-stu-id="86269-111">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="86269-112">[Nr. 11354]</span><span class="sxs-lookup"><span data-stu-id="86269-112">[#11354]</span></span>
* <span data-ttu-id="86269-113">Unterstützung für die folgenden Cmdlets für die neue SAP-Erweiterung hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="86269-113">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="86269-114">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="86269-114">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="86269-115">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="86269-115">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="86269-116">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="86269-116">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="86269-117">Update-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="86269-117">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="86269-118">Fehler in Beispielen im Hilfedokument korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-118">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="86269-119">Der genaue Zeichenfolgenwert für den VM-Energiezustand (PowerState) wurde im Tabellenformat angezeigt.</span><span class="sxs-lookup"><span data-stu-id="86269-119">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="86269-120">New-AzVmssConfig: Serialisierung der Eigenschaft „AutomaticRepairs“ korrigiert, wenn „SinglePlacementGroup“d deaktiviert ist</span><span class="sxs-lookup"><span data-stu-id="86269-120">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="86269-121">[Nr. 11257]</span><span class="sxs-lookup"><span data-stu-id="86269-121">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="86269-122">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="86269-122">Az.DataFactory</span></span>
* <span data-ttu-id="86269-123">Version des ADF .NET SDK auf 4.8.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-123">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="86269-124">Optionale Parameter zum Befehl „Invoke-AzDataFactoryV2Pipeline“ zur Unterstützung der erneuten Ausführung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-124">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="86269-125">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="86269-125">Az.DataLakeStore</span></span>
* <span data-ttu-id="86269-126">Breaking Change-Beschreibung für „Export-AzDataLakeStoreItem“ und „Import-AzDataLakeStoreItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-126">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="86269-127">Option zur Bytecodierung für „New-AzDataLakeStoreItem“, „Add-AzDAtaLakeStoreItemContent“ und „Get-AzDAtaLakeStoreItemContent“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-127">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="86269-128">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="86269-128">Az.HDInsight</span></span>
* <span data-ttu-id="86269-129">Angabe der mindestens unterstützten TLS-Version bei Clustererstellung unterstützt</span><span class="sxs-lookup"><span data-stu-id="86269-129">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="86269-130">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="86269-130">Az.IotHub</span></span>
* <span data-ttu-id="86269-131">Unterstützung für die Verwaltung verteilter Einstellungen pro Gerät hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-131">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="86269-132">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="86269-132">New Cmdlets are:</span></span>
    - <span data-ttu-id="86269-133">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="86269-133">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="86269-134">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="86269-134">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="86269-135">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="86269-135">Az.KeyVault</span></span>
* <span data-ttu-id="86269-136">Breaking Change-Attribute zu „New-AzKeyVault“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-136">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="86269-137">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="86269-137">Az.Monitor</span></span>
* <span data-ttu-id="86269-138">Dokumentation für „New-AzScheduledQueryRuleLogMetricTrigger“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-138">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86269-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86269-139">Az.Network</span></span>
* <span data-ttu-id="86269-140">Cmdlets aktualisiert, um mandantenübergreifende VNET-Verbindungen virtueller Hubs (VirtualHubVnetConnections) zuzulassen</span><span class="sxs-lookup"><span data-stu-id="86269-140">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="86269-141">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="86269-141">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="86269-142">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="86269-142">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="86269-143">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="86269-143">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="86269-144">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="86269-144">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="86269-145">Abhängigkeit vom SQL Management SDK entfernt</span><span class="sxs-lookup"><span data-stu-id="86269-145">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="86269-146">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="86269-146">Az.PolicyInsights</span></span>
* <span data-ttu-id="86269-147">Verbesserte Fehlermeldungen</span><span class="sxs-lookup"><span data-stu-id="86269-147">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="86269-148">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="86269-148">Az.RecoveryServices</span></span>
* <span data-ttu-id="86269-149">Azure Site Recovery: Unterstützung für erneutes Schützen hinzugefügt und VM-Eigenschaften für VMs mit Azure-Datenträgerverschlüsselung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-149">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="86269-150">Überwachung der Notfallwiederherstellung für VmwareToAzure-Eigenschaften von Azure Site Recovery hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-150">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="86269-151">Azure Backup: Unterstützung für die Wiederholung des Richtlinienupdates für fehlerhafte Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-151">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="86269-152">Azure Backup: Unterstützung für Einstellungen für den Ausschluss von Datenträgern während der Sicherung und Wiederherstellung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-152">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="86269-153">Azure Backup: Unterstützung für die Wiederherstellung mehrerer Dateien/Ordner in AzureFileShare hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-153">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="86269-154">Azure Backup: Unterstützung für vom Benutzer angegebene Ressourcengruppe beim Aktualisieren der IaasVM-Richtlinie hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-154">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="86269-155">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86269-155">Az.Resources</span></span>
* <span data-ttu-id="86269-156">„Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType“ korrigiert, sodass die tatsächliche API-Version (apiVersion) von Ressourcen anstelle der API-Standardversion verwendet wird [Nr. 11267]</span><span class="sxs-lookup"><span data-stu-id="86269-156">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="86269-157">Protokollierung von „correlationId“ für Fehlerszenarien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-157">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="86269-158">Kleine Änderung an der Dokumentation für „Get-AzResourceLock“</span><span class="sxs-lookup"><span data-stu-id="86269-158">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="86269-159">Beispiel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-159">Added example.</span></span>
* <span data-ttu-id="86269-160">Einfaches Anführungszeichen im Parameterwert „Get-AzADUser“ mit Escapezeichen versehen [Nr. 11317]</span><span class="sxs-lookup"><span data-stu-id="86269-160">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="86269-161">Neue Cmdlets für Bereitstellungsskripts (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-161">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="86269-162">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86269-162">Az.Sql</span></span>
* <span data-ttu-id="86269-163">Lesbarer sekundärer Parameter zu „Invoke-AzSqlDatabaseFailover“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-163">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="86269-164">Cmdlet „Disable-AzSqlServerActiveDirectoryOnlyAuthentication“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-164">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="86269-165">Vertraulichkeitsrang beim Klassifizieren von Spalten in der Datenbank gespeichert</span><span class="sxs-lookup"><span data-stu-id="86269-165">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="86269-166">Az.Support</span><span class="sxs-lookup"><span data-stu-id="86269-166">Az.Support</span></span>
* <span data-ttu-id="86269-167">Allgemeine Verfügbarkeit des Moduls „Az.Support“</span><span class="sxs-lookup"><span data-stu-id="86269-167">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="86269-168">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="86269-168">Az.Websites</span></span>
* <span data-ttu-id="86269-169">Unterstützung für das Arbeiten mit Datenverkehrs-Routingregeln für Web-Apps über die folgenden neuen Cmdlets hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="86269-169">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="86269-170">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="86269-170">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="86269-171">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="86269-171">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="86269-172">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="86269-172">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="86269-173">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="86269-173">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="86269-174">3.6.1 – März 2020</span><span class="sxs-lookup"><span data-stu-id="86269-174">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="86269-175">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86269-175">Az.Accounts</span></span>
* <span data-ttu-id="86269-176">Öffnen der Azure PowerShell-Umfrageseite in „Send-Feedback“ [#11020]</span><span class="sxs-lookup"><span data-stu-id="86269-176">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="86269-177">Anzeigen der Azure PowerShell-Umfrage-URL in „Resolve-Error“ [#11021]</span><span class="sxs-lookup"><span data-stu-id="86269-177">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="86269-178">Az-Version in UserAgent hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-178">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="86269-179">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="86269-179">Az.ApiManagement</span></span>
* <span data-ttu-id="86269-180">Unterstützung für das Abrufen und Konfigurieren einer benutzerdefinierten Domäne auf dem DeveloperPortal-Endpunkt hinzugefügt [#11007]</span><span class="sxs-lookup"><span data-stu-id="86269-180">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="86269-181">„Export-AzApiManagementApi“: Unterstützung für das Herunterladen der API-Definition im JSON-Format hinzugefügt [#9987]</span><span class="sxs-lookup"><span data-stu-id="86269-181">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="86269-182">„Import-AzApiManagementApi“: Unterstützung für das Importieren der OpenApi 3.0-Definition aus JSON-Dokument hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-182">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="86269-183">„New-AzApiManagementIdentityProvider“ und „Set-AzApiManagementIdentityProvider“: Unterstützung für das Konfigurieren des Anmeldemandanten für AAD B2C-Anbieter hinzugefügt [#9784]</span><span class="sxs-lookup"><span data-stu-id="86269-183">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="86269-184">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="86269-184">Az.DataLakeStore</span></span>
* <span data-ttu-id="86269-185">Verweis auf System.Buffers in csproj und psd1 explizit hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-185">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="86269-186">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="86269-186">Az.IotHub</span></span>
* <span data-ttu-id="86269-187">Unterstützung für die Verwaltung von Geräten in IoT Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-187">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="86269-188">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="86269-188">New Cmdlets are:</span></span>
    - <span data-ttu-id="86269-189">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="86269-189">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="86269-190">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="86269-190">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="86269-191">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="86269-191">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="86269-192">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="86269-192">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="86269-193">Unterstützung für die Verwaltung von Modulen auf einem IoT-Zielgerät in einem IoT-Hub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-193">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="86269-194">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="86269-194">New Cmdlets are:</span></span>
    - <span data-ttu-id="86269-195">„Add-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="86269-195">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="86269-196">„Get-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="86269-196">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="86269-197">„Remove-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="86269-197">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="86269-198">„Set-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="86269-198">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="86269-199">Cmdlet zum Abrufen der Verbindungszeichenfolge eines IoT-Zielgeräts in einem IoT-Hub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-199">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="86269-200">Cmdlet zum Abrufen der Verbindungszeichenfolge eines Moduls auf einem IoT-Zielgerät in einem IoT-Hub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-200">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="86269-201">Unterstützung für das Abrufen/Festlegen des übergeordneten Geräts eines IoT-Geräts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-201">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="86269-202">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="86269-202">New Cmdlets are:</span></span>
    - <span data-ttu-id="86269-203">„Get-AzIotHubDeviceParent“</span><span class="sxs-lookup"><span data-stu-id="86269-203">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="86269-204">„Set-AzIotHubDeviceParent“</span><span class="sxs-lookup"><span data-stu-id="86269-204">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="86269-205">Unterstützung für die Verwaltung der Beziehung zwischen über- und untergeordneten Geräten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-205">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="86269-206">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="86269-206">Az.Monitor</span></span>
* <span data-ttu-id="86269-207">Ausgabewert für „Get-AzMetricDefinition“ korrigiert [#9714]</span><span class="sxs-lookup"><span data-stu-id="86269-207">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86269-208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86269-208">Az.Network</span></span>
* <span data-ttu-id="86269-209">SQL Management SDK aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="86269-209">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="86269-210">Es wurde ein Problem mit dem Namensunterschied in der PrivateLinkServiceConnectionState-Klasse behoben.</span><span class="sxs-lookup"><span data-stu-id="86269-210">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="86269-211">Zuordnung des Felds „ActionsRequired“ zu „ActionRequired“.</span><span class="sxs-lookup"><span data-stu-id="86269-211">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="86269-212">PublicNetworkAccess zu „New-AzSqlServer“ und „Set-AzSqlServer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-212">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="86269-213">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86269-213">Az.Resources</span></span>
* <span data-ttu-id="86269-214">Für Nullverweisfehler in „Get-AzRoleAssignment“ behoben</span><span class="sxs-lookup"><span data-stu-id="86269-214">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="86269-215">Switch „-Force“ und „-PassThru“ in „Remove-AzADGroup“ als optional gekennzeichnet [#10849]</span><span class="sxs-lookup"><span data-stu-id="86269-215">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="86269-216">Problem behoben, dass „MailNickname“ nicht zurückgegeben wird, in „Remove-AzADGroup“ behoben [#11167]</span><span class="sxs-lookup"><span data-stu-id="86269-216">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="86269-217">Problem behoben, dass Pipe-Vorgang „Remove-AzADGroup“ nicht funktioniert [#11171]</span><span class="sxs-lookup"><span data-stu-id="86269-217">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="86269-218">Für Nullverweisfehler in GetAzureRoleAssignmentCommand behoben</span><span class="sxs-lookup"><span data-stu-id="86269-218">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="86269-219">Breaking Change-Attribute für bevorstehende Änderungen an Richtlinien-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-219">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="86269-220">„Get-AzResourceGroup“ aktualisiert, sodass jetzt serverseitig nach Ressourcengruppentags gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="86269-220">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="86269-221">Tag-Cmdlets so erweitert, dass „-ResourceId“ akzeptiert wird</span><span class="sxs-lookup"><span data-stu-id="86269-221">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="86269-222">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="86269-222">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="86269-223">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="86269-223">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="86269-224">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="86269-224">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="86269-225">Neues Tag-Cmdlet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-225">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="86269-226">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="86269-226">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="86269-227">ScopedDeployment aus SDK 3.3.0 übernommen</span><span class="sxs-lookup"><span data-stu-id="86269-227">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="86269-228">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86269-228">Az.Sql</span></span>
* <span data-ttu-id="86269-229">Publicnetworkaccess wurde "New-azsqlserver" und "Set-azsqlserver" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-229">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="86269-230">Unterstützung für die Konfiguration der Sicherung der Langzeitaufbewahrung für verwaltete Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-230">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="86269-231">Einrichten/Festlegen der LTR-Richtlinie für eine verwaltete Datenbank</span><span class="sxs-lookup"><span data-stu-id="86269-231">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="86269-232">Abrufen von Sicherungen nach verwalteter Datenbank, verwalteter Instanz oder nach Speicherort</span><span class="sxs-lookup"><span data-stu-id="86269-232">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="86269-233">Entfernen einer LTR-Sicherung</span><span class="sxs-lookup"><span data-stu-id="86269-233">Remove an LTR backup</span></span>
    - <span data-ttu-id="86269-234">Wiederherstellen einer LTR-Sicherung zum Erstellen einer neuen verwalteten Datenbank</span><span class="sxs-lookup"><span data-stu-id="86269-234">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="86269-235">MinimalTlsVersion wurde zu New-AzSqlServer und Set-AzSqlServer hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-235">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="86269-236">MinimalTlsVersion wurde zu New-AzSqlInstance und Set-AzSqlInstance hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-236">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="86269-237">SQL SDK-Version für Az.Network festgelegt</span><span class="sxs-lookup"><span data-stu-id="86269-237">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="86269-238">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86269-238">Az.Storage</span></span>
* <span data-ttu-id="86269-239">Unterstützung von AllowProtectedAppendWrite in ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="86269-239">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="86269-240">„Set-AzRmStorageContainerImmutabilityPolicy“</span><span class="sxs-lookup"><span data-stu-id="86269-240">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="86269-241">Warnmeldung für Breaking Change hinzugefügt: Typänderung für „AzureStorageTable“ in einer zukünftigen Version</span><span class="sxs-lookup"><span data-stu-id="86269-241">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="86269-242">„New-AzStorageTable“</span><span class="sxs-lookup"><span data-stu-id="86269-242">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="86269-243">„Get-AzStorageTable“</span><span class="sxs-lookup"><span data-stu-id="86269-243">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="86269-244">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="86269-244">Az.Websites</span></span>
* <span data-ttu-id="86269-245">Tag-Parameter für „New-AzAppServicePlan“ und „Set-AzAppServicePlan“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-245">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="86269-246">Beenden der Cmdlet-Ausführung, wenn beim Hinzufügen einer benutzerdefinierten Domäne zu einer Website eine Ausnahme ausgelöst wird</span><span class="sxs-lookup"><span data-stu-id="86269-246">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="86269-247">Unterstützung zur Durchführung von Vorgängen für App Services hinzugefügt, die sich nicht in der gleichen Ressourcengruppe wie der App Service-Plan befinden</span><span class="sxs-lookup"><span data-stu-id="86269-247">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="86269-248">Zugriffseinschränkung auf WebApp/Funktion in verschiedenen Ressourcengruppen angewendet</span><span class="sxs-lookup"><span data-stu-id="86269-248">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="86269-249">Problem beim Festlegen von benutzerdefinierten Hostnamen für WebAppSlots behoben</span><span class="sxs-lookup"><span data-stu-id="86269-249">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="86269-250">3.5.0: Februar 2020</span><span class="sxs-lookup"><span data-stu-id="86269-250">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="86269-251">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="86269-251">Highlights since the last major release</span></span>
* <span data-ttu-id="86269-252">Clientseitige Telemetrie aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-252">Updated client side telemetry.</span></span>
* <span data-ttu-id="86269-253">Cmdlets zur Unterstützung der Geräteverwaltung in Az.IotHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-253">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="86269-254">Cmdlets für Verfügbarkeitsgruppenlistener in Az.SqlVirtualMachine hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-254">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="86269-255">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86269-255">Az.Accounts</span></span>
* <span data-ttu-id="86269-256">Abonnement-ID, Mandanten-ID und Ausführungszeit in clientseitigen Telemetriedaten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-256">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="86269-257">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="86269-257">Az.Automation</span></span>
* <span data-ttu-id="86269-258">Tippfehler in Beispiel 1 in der Referenzdokumentation für „New-AzAutomationSoftwareUpdateConfiguration“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-258">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="86269-259">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="86269-259">Az.CognitiveServices</span></span>
* <span data-ttu-id="86269-260">SDK auf 7.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-260">Updated SDK to 7.0</span></span>
* <span data-ttu-id="86269-261">Verbesserte Fehlermeldung, wenn der Server mit leerem Text antwortet</span><span class="sxs-lookup"><span data-stu-id="86269-261">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86269-262">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86269-262">Az.Compute</span></span>
* <span data-ttu-id="86269-263">Zulässiger leerer Wert für „ProximityPlacementGroupId“ während des Updates</span><span class="sxs-lookup"><span data-stu-id="86269-263">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="86269-264">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="86269-264">Az.FrontDoor</span></span>
* <span data-ttu-id="86269-265">Cmdlet zum Abrufen verwalteter Regeldefinitionen hinzugefügt, die in WAF verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="86269-265">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="86269-266">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="86269-266">Az.IotHub</span></span>
* <span data-ttu-id="86269-267">Unterstützung für die Verwaltung von Geräten in IoT Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-267">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="86269-268">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="86269-268">New Cmdlets are:</span></span>
    - <span data-ttu-id="86269-269">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="86269-269">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="86269-270">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="86269-270">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="86269-271">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="86269-271">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="86269-272">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="86269-272">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="86269-273">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="86269-273">Az.KeyVault</span></span>
* <span data-ttu-id="86269-274">Duplizierter Text für „Add-AzKeyVaultKey.md“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-274">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="86269-275">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="86269-275">Az.Monitor</span></span>
* <span data-ttu-id="86269-276">Beschreibung des Cmdlets „Get-AzLog cmdlet“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-276">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="86269-277">Dem Befehl „New-AzMetricAlertRuleV2“ wurde ein Parameter namens „ActionGroupId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-277">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="86269-278">Der Benutzer kann entweder „ActionGroupId(string)“ oder „ActionGorup(ActivityLogAlertActionGroup)“ angeben.</span><span class="sxs-lookup"><span data-stu-id="86269-278">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86269-279">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86269-279">Az.Network</span></span>
* <span data-ttu-id="86269-280">Zusätzlicher Parameterhinweis für den Parameter „-EnableProxyProtocol“ für das Cmdlet „New-AzPrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-280">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="86269-281">FilterData-Beispiel in „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-281">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="86269-282">Paketerfassungsbeispiel für die Erfassung aller inneren und äußeren Pakete in „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-282">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="86269-283">Unterstützte Azure Firewall-Richtlinie für VNET-Firewalls</span><span class="sxs-lookup"><span data-stu-id="86269-283">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="86269-284">Keine neuen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-284">No new cmdlets are added.</span></span> <span data-ttu-id="86269-285">Die Einschränkung für die Firewallrichtlinie für VNET-Firewalls wurde gelockert.</span><span class="sxs-lookup"><span data-stu-id="86269-285">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="86269-286">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="86269-286">Az.RecoveryServices</span></span>
* <span data-ttu-id="86269-287">Unterstützung für „Als Dateien wiederherstellen“ für SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-287">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="86269-288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86269-288">Az.Resources</span></span>
* <span data-ttu-id="86269-289">Cmdlets für die Vorlagenbereitstellung umgestaltet</span><span class="sxs-lookup"><span data-stu-id="86269-289">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="86269-290">Neue Cmdlets zur Verwaltung von Bereitstellungen in der Verwaltungsgruppe hinzugefügt: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="86269-290">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="86269-291">Neue Cmdlets zur Verwaltung von Bereitstellungen im Mandantenbereich hinzugefügt: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="86269-291">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="86269-292">Cmdlets vom Typ „\*-AzDeployment“ für den speziellen Einsatz im Abonnementbereich umgestaltet</span><span class="sxs-lookup"><span data-stu-id="86269-292">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="86269-293">Aliase vom Typ „*-AzSubscriptionDeployment“ für Cmdlets vom Typ „*-AzDeployment“ erstellt</span><span class="sxs-lookup"><span data-stu-id="86269-293">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="86269-294">„Update-AzADApplication“ korrigiert, wenn der Parameter „AvailableToOtherTenants“ nicht festgelegt wird</span><span class="sxs-lookup"><span data-stu-id="86269-294">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="86269-295">„ApplicationObjectWithoutCredentialParameterSet“ entfernt, um „AmbiguousParameterSetException“ zu vermeiden</span><span class="sxs-lookup"><span data-stu-id="86269-295">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="86269-296">Hilfedateien erneut generiert</span><span class="sxs-lookup"><span data-stu-id="86269-296">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="86269-297">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86269-297">Az.Sql</span></span>
* <span data-ttu-id="86269-298">Unterstützung für abonnementübergreifende Point-in-Time-Wiederherstellung für verwaltete Instanzen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-298">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="86269-299">Unterstützung für die Änderung der Hardwaregeneration von vorhandenen verwalteten SQL-Instanzen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-299">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="86269-300">Hilfebeispiele für „Update-AzSqlServerVulnerabilityAssessmentSetting“ korrigiert: parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="86269-300">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="86269-301">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="86269-301">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="86269-302">Cmdlets für Verfügbarkeitsgruppenlistener hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-302">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="86269-303">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="86269-303">Az.StorageSync</span></span>
* <span data-ttu-id="86269-304">Unterstützte Zeichensätze in „Invoke-AzStorageSyncCompatibilityCheck“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-304">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="86269-305">3.4.0: Februar 2020</span><span class="sxs-lookup"><span data-stu-id="86269-305">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="86269-306">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="86269-306">Highlights since the last major release</span></span>
* <span data-ttu-id="86269-307">Az.CosmosDB: erste Version 0.1.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="86269-307">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="86269-308">Unterstützung für Az.Network ConnectionMonitor V2 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-308">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="86269-309">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86269-309">Az.Accounts</span></span>
* <span data-ttu-id="86269-310">Deaktivieren der automatischen Kontextspeicherung, wenn „AzureRmContext.json“ nicht verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="86269-310">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="86269-311">Aktualisieren des Verweises auf Azure Powershell Common auf 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="86269-311">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="86269-312">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="86269-312">Az.ApiManagement</span></span>
* <span data-ttu-id="86269-313">**Get-AzApiManagementApiSchema** Fehler beim Abrufen des einer API zugeordneten Open-Api-Schemas behoben   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="86269-313">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="86269-314">**New-AzApiManagementProduct**\* und **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="86269-314">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="86269-315">Dokumentation korrigiert für https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="86269-315">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="86269-316">**Set-AzApiManagementApi** Beispiel hinzugefügt, das das Aktualisieren von ServiceUrl mithilfe des Cmdlets veranschaulicht</span><span class="sxs-lookup"><span data-stu-id="86269-316">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86269-317">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86269-317">Az.Compute</span></span>
* <span data-ttu-id="86269-318">Anzahl des VM-Status auf 100 beschränkt, um die Drosselung zu vermeiden, wenn „Get-AzVM -Status“ ohne VM-Name ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="86269-318">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="86269-319">Cmdlet „Update-AzDiskEncryptionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-319">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="86269-320">Die Parameter „EncryptionType“ und „DiskEncryptionSetId“ wurden den folgenden Cmdlets hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="86269-320">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="86269-321">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="86269-321">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="86269-322">Parameter „ColocationStatus“ zum Cmdlet „Get-AzProximityPlacementGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-322">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="86269-323">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="86269-323">Az.DataFactory</span></span>
* <span data-ttu-id="86269-324">Version des ADF .NET SDK auf 4.7.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-324">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="86269-325">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="86269-325">Az.DeploymentManager</span></span>
* <span data-ttu-id="86269-326">LIST-Vorgänge für Ressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-326">Adds LIST operations for resources</span></span>
* <span data-ttu-id="86269-327">Funktionen zum Ausführen von Vorgängen für Integritätsprüfungsschritte hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-327">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="86269-328">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="86269-328">Az.HDInsight</span></span>
* <span data-ttu-id="86269-329">Dokumentationsfehler für „New-AzHDInsightCluster“ behoben</span><span class="sxs-lookup"><span data-stu-id="86269-329">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="86269-330">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="86269-330">Az.KeyVault</span></span>
* <span data-ttu-id="86269-331">Namensalias zum VaultName-Attribut hinzugefügt, um „Remove-AzureKeyVault“ mit „New-AzureKeyVault“ konsistent zu machen</span><span class="sxs-lookup"><span data-stu-id="86269-331">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86269-332">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86269-332">Az.Network</span></span>
* <span data-ttu-id="86269-333">Neues Beispiel zu „Set-AzNetworkWatcherConfigFlowLog.md“ hinzugefügt, um das Szenario zur Traffic Analytics-Deaktivierung zu veranschaulichen</span><span class="sxs-lookup"><span data-stu-id="86269-333">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="86269-334">Unterstützung für die Zuweisung der IP-Verwaltungskonfiguration zu Azure Firewall hinzugefügt: ein dediziertes Subnetz und eine öffentliche IP-Adresse, die von der Firewall für den Verwaltungsdatenverkehr verwendet werden</span><span class="sxs-lookup"><span data-stu-id="86269-334">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="86269-335">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="86269-335">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="86269-336">Parameter „-ManagementPublicIpAddress“ (nicht obligatorisch) hinzugefügt, der ein Objekt für die öffentliche IP-Adresse akzeptiert</span><span class="sxs-lookup"><span data-stu-id="86269-336">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="86269-337">Methode „SetManagementIpConfiguration“ für Firewallobjekt hinzugefügt. Erfordert ein Subnetz und eine öffentliche IP-Adresse als Eingabe, und der Subnetzname muss „AzureFirewallManagementSubnet“ lauten.</span><span class="sxs-lookup"><span data-stu-id="86269-337">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="86269-338">Beispiele für „Get-AzNetworkSecurityGroup“ korrigiert, um Beispiele für Netzwerksicherheitsgruppen und nicht für Netzwerkschnittstellen anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="86269-338">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="86269-339">Tippfehler im Befehl „New-AzVpnSite“ korrigiert, der dazu führte, dass die Vervollständigung für die Ressourcen-ID einen Parameter nicht vervollständigen konnte</span><span class="sxs-lookup"><span data-stu-id="86269-339">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="86269-340">Unterstützung für die URL-Konfiguration im Aktionssatz für Neuschreibungsregeln in Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-340">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="86269-341">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="86269-341">New cmdlets added:</span></span>
        - <span data-ttu-id="86269-342">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="86269-342">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="86269-343">Cmdlets mit optionalem Parameter aktualisiert: UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="86269-343">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="86269-344">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="86269-344">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="86269-345">Unterstützung für Ressourcen der Version 2 von NetworkWatcher ConnectionMonitor hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-345">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="86269-346">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="86269-346">Az.PolicyInsights</span></span>
* <span data-ttu-id="86269-347">Unterstützung der Konformitätsbewertung vor der Ermittlung der zu korrigierenden Ressourcen</span><span class="sxs-lookup"><span data-stu-id="86269-347">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="86269-348">Parameter „-ResourceDiscoverMode“ zu „Start-AzPolicyRemediation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-348">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="86269-349">Cmdlet „Get-AzPolicyMetadata“ zum Abrufen der Ressourcen für Richtlinienmetadaten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-349">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="86269-350">„Get-AzPolicyState“ und „Get-AzPolicyStateSummary“ für API-Version 2019-10-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-350">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="86269-351">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="86269-351">Az.RecoveryServices</span></span>
* <span data-ttu-id="86269-352">Azure Site Recovery-Unterstützung für das Entfernen eines replizierten Datenträgers</span><span class="sxs-lookup"><span data-stu-id="86269-352">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="86269-353">In Azure Backup wurde Unterstützung zum Hinzufügen von Tags bei der Erstellung eines Recovery Services-Tresors hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-353">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="86269-354">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86269-354">Az.Resources</span></span>
* <span data-ttu-id="86269-355">„-Scope“ in Cmdlets vom Typ „\*-AzPolicyAssignment“ nun optional (standardmäßig auf Abonnementkontext festgelegt)</span><span class="sxs-lookup"><span data-stu-id="86269-355">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="86269-356">Beispiele zum Erstellen von „ADServicePrincipal“ mit Kennwort und Schlüsselanmeldeinformation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-356">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="86269-357">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86269-357">Az.Sql</span></span>
<span data-ttu-id="86269-358">Cmdlet „New-AzSqlDatabaseSecondary“ korrigiert, um auf die Existenz von „PartnerDatabaseName“ anstelle von „DatabaseName“ zu prüfen</span><span class="sxs-lookup"><span data-stu-id="86269-358">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="86269-359">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86269-359">Az.Storage</span></span>
* <span data-ttu-id="86269-360">Unterstützung für das Festlegen des Schlüsseltyps für die Tabellen-/Warteschlangenverschlüsselung beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="86269-360">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="86269-361">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="86269-361">New-AzStorageAccount</span></span>
* <span data-ttu-id="86269-362">Anzeigen der Anforderungs-ID (RequestId), wenn für „StorageException“ keine erweiterten Fehlerinformationen (ExtendedErrorInformation) vorliegen</span><span class="sxs-lookup"><span data-stu-id="86269-362">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="86269-363">Beispiel 6 des Cmdlets „Start-AzStorageBlobCopy“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-363">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="86269-364">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="86269-364">Az.Websites</span></span>
* <span data-ttu-id="86269-365">„Set-AzWebapp“ und „Set-AzWebappSlot“ unterstützen die Eigenschaften „AlwaysOn“, „MinTls“ und „FtpsState“.</span><span class="sxs-lookup"><span data-stu-id="86269-365">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="86269-366">Problem behoben, das dazu führte, dass beim Festlegen von „HttpsOnly“ bei gleichzeitiger Änderung von „AppservicePlan“ mit dem einzelnen Befehl „Set-AzWebApp“ „HttpsOnly“ auf den Standardwert zurückgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="86269-366">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="86269-367">3.3.0 – Januar 2020</span><span class="sxs-lookup"><span data-stu-id="86269-367">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="86269-368">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86269-368">Az.Accounts</span></span>
* <span data-ttu-id="86269-369">„Add-AzEnvironment“ und „Set-AzEnvironment“ wurden so aktualisiert, dass sie jetzt die Parameter „AzureAttestationServiceEndpointResourceId“ und „AzureAttestationServiceEndpointSuffix“ akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="86269-369">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="86269-370">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="86269-370">Az.Cdn</span></span>
* <span data-ttu-id="86269-371">Anzeigen von Fehlerantwortdetails im Cmdlet „New-AzCdnEndpoint“</span><span class="sxs-lookup"><span data-stu-id="86269-371">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86269-372">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86269-372">Az.Compute</span></span>
* <span data-ttu-id="86269-373">Cmdlet „Set-AzVMCustomScriptExtension“ für eine VM mit verwaltetem Betriebssystemdatenträger ohne Betriebssystemprofil wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="86269-373">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="86269-374">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="86269-374">Az.ContainerInstance</span></span>
* <span data-ttu-id="86269-375">Im Beispiel von „New-AzContainerGroup“ verwendete Parameternamen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="86269-375">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="86269-376">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="86269-376">Az.DataBoxEdge</span></span>
* <span data-ttu-id="86269-377">Cmdlet „Get-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-377">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="86269-378">Edge-Speichercontainer abrufen</span><span class="sxs-lookup"><span data-stu-id="86269-378">Get the Edge Storage Container</span></span>
* <span data-ttu-id="86269-379">Cmdlet „New-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-379">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="86269-380">Neuen Edge-Speichercontainer erstellen</span><span class="sxs-lookup"><span data-stu-id="86269-380">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="86269-381">Cmdlet „Remove-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-381">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="86269-382">Edge-Speichercontainer entfernen</span><span class="sxs-lookup"><span data-stu-id="86269-382">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="86269-383">Cmdlet „Invoke-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-383">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="86269-384">Aktion zum Aktualisieren von Daten in Edge-Speichercontainer aufrufen</span><span class="sxs-lookup"><span data-stu-id="86269-384">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="86269-385">Cmdlet „Get-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-385">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="86269-386">Edge-Speicherkonto abrufen</span><span class="sxs-lookup"><span data-stu-id="86269-386">Get the Edge Storage Account</span></span>
* <span data-ttu-id="86269-387">Cmdlet „New-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-387">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="86269-388">Neues Edge-Speicherkonto erstellen</span><span class="sxs-lookup"><span data-stu-id="86269-388">Create new Edge Storage Account</span></span>
* <span data-ttu-id="86269-389">Cmdlet „Remove-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-389">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="86269-390">Edge-Speicherkonto entfernen</span><span class="sxs-lookup"><span data-stu-id="86269-390">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="86269-391">Cmdlet „Invoke-AzDataBoxEdgeShare“ aufrufen</span><span class="sxs-lookup"><span data-stu-id="86269-391">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="86269-392">Aktion zum Aktualisieren von Daten auf Freigabe aufrufen</span><span class="sxs-lookup"><span data-stu-id="86269-392">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="86269-393">Cmdlet „Set-AzDataBoxEdgeStorageAccountCredential“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-393">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="86269-394">Festlegen der Speicherkonto-Anmeldeinformationen für „az databoxedge“</span><span class="sxs-lookup"><span data-stu-id="86269-394">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="86269-395">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="86269-395">Az.DataFactory</span></span>
* <span data-ttu-id="86269-396">Eigenschaften „AutoUpdateETA“, „LatestVersion“, „PushedVersion“, „TaskQueueId“ und „VersionStatus“ für Befehl „Get-AzDataFactoryV2IntegrationRuntime“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-396">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="86269-397">Version des ADF .NET SDK auf 4.6.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-397">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="86269-398">Parameter „PublicIPs“ wurde für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um das Erstellen der Azure-SSIS Integration Runtime mit statischen öffentlichen IP-Adressen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="86269-398">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="86269-399">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="86269-399">Az.DevTestLabs</span></span>
* <span data-ttu-id="86269-400">Fehlerhafter Link in „Get-AzDtlAllowedVMSizesPolicy.md“ entfernt</span><span class="sxs-lookup"><span data-stu-id="86269-400">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="86269-401">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="86269-401">Az.EventHub</span></span>
* <span data-ttu-id="86269-402">Behebung des Problems 10634: Verweis auf NULL-Objekt für „remove eventhubnamespace“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-402">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="86269-403">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="86269-403">Az.HDInsight</span></span>
* <span data-ttu-id="86269-404">Fehler in „Invoke-AzHDInsightHiveJob.md“ wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="86269-404">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="86269-405">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="86269-405">Az.MachineLearning</span></span>
* <span data-ttu-id="86269-406">Die folgenden Cmdlets wurden entfernt, da „MachineLearningCompute“ nicht mehr verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="86269-406">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="86269-407">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="86269-407">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="86269-408">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="86269-408">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="86269-409">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="86269-409">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="86269-410">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="86269-410">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="86269-411">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="86269-411">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="86269-412">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="86269-412">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="86269-413">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="86269-413">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86269-414">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86269-414">Az.Network</span></span>
* <span data-ttu-id="86269-415">Upgrade der Abhängigkeit von „Microsoft.Azure.Management.Sql“ von „1.36-preview“ auf „1.37-preview“</span><span class="sxs-lookup"><span data-stu-id="86269-415">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="86269-416">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="86269-416">Az.RecoveryServices</span></span>
* <span data-ttu-id="86269-417">Änderung der Azure Site Recovery-Unterstützung für virtuelle Computer mit verwalteten Datenträgern, die im Ruhezustand mit kundenseitig verwalteten Schlüsseln für Azure-zu-Azure-Anbieter verschlüsselt sind</span><span class="sxs-lookup"><span data-stu-id="86269-417">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="86269-418">Azure Site Recovery-Unterstützung für die Eingabe der ID des Datenträgerverschlüsselungssatzes als optionale Eingabe beim Aktivieren des Schutzes für VMware in Azure</span><span class="sxs-lookup"><span data-stu-id="86269-418">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="86269-419">Azure Site Recovery-Unterstützung für die Eingabe der ID des Datenträgerverschlüsselungssatzes als optionale Eingabe auf Datenträgerebene beim Aktivieren des Schutzes für VMware in Azure</span><span class="sxs-lookup"><span data-stu-id="86269-419">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="86269-420">Azure Site Recovery-Unterstützung zum Aktualisieren eines replikationsgeschützten Elements mit der Zuordnung eines Datenträgerverschlüsselungssatzes für HyperV in Azure</span><span class="sxs-lookup"><span data-stu-id="86269-420">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="86269-421">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86269-421">Az.Resources</span></span>
* <span data-ttu-id="86269-422">Fehler in Hilfedokument zu „Remove-AzTag“ behoben</span><span class="sxs-lookup"><span data-stu-id="86269-422">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="86269-423">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86269-423">Az.Sql</span></span>
* <span data-ttu-id="86269-424">Funktionalität der Baseline-Cmdlets für einen Sicherheitsrisikobewertungssatz korrigiert, sodass sie auf der Master-Datenbank für Azure Database funktionieren und sie auf Systemdatenbanken von verwalteten Instanzen einschränken.</span><span class="sxs-lookup"><span data-stu-id="86269-424">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="86269-425">Fehler beim Erstellen einer SQL-Instanzfailovergruppe behoben</span><span class="sxs-lookup"><span data-stu-id="86269-425">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="86269-426">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="86269-426">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="86269-427">DR als neuer gültiger Lizenztyp hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-427">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="86269-428">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86269-428">Az.Storage</span></span>
* <span data-ttu-id="86269-429">Warnmeldung für Breaking Change hinzugefügt: Wertänderung für „DefaultAction“ in einer zukünftigen Version</span><span class="sxs-lookup"><span data-stu-id="86269-429">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="86269-430">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="86269-430">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="86269-431">Unterstützung für das Abrufen der letzten Synchronisierungszeit des Speicherkontos durch Ausführen von „get-AzureRMStorageAccount“ mit Parameter „-IncludeGeoReplicationStats“</span><span class="sxs-lookup"><span data-stu-id="86269-431">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="86269-432">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="86269-432">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="86269-433">3.2.0: Dezember 2019</span><span class="sxs-lookup"><span data-stu-id="86269-433">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="86269-434">Allgemein</span><span class="sxs-lookup"><span data-stu-id="86269-434">General</span></span>
* <span data-ttu-id="86269-435">Verweise in „.psd1“ zur Verwendung des relativen Pfads für alle Module aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-435">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="86269-436">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86269-436">Az.Accounts</span></span>
* <span data-ttu-id="86269-437">Richtiges UserAgent-Element für clientseitige Telemetrie für Az 4.0-Vorschauversion festgelegt</span><span class="sxs-lookup"><span data-stu-id="86269-437">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="86269-438">Anzeigen benutzerfreundlicher Fehlermeldungen, wenn der Kontext in der Az 4.0-Vorschauversion NULL ist</span><span class="sxs-lookup"><span data-stu-id="86269-438">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="86269-439">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="86269-439">Az.Batch</span></span>
* <span data-ttu-id="86269-440">Problem [#10602](https://github.com/Azure/azure-powershell/issues/10602) behoben, aufgrund dessen „VirtualMachineConfiguration.ContainerConfiguration“ oder „VirtualMachineConfiguration.DataDisks“ von **New-AzBatchPool** nicht ordnungsgemäß an den Server gesendet wurde</span><span class="sxs-lookup"><span data-stu-id="86269-440">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="86269-441">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="86269-441">Az.DataFactory</span></span>
* <span data-ttu-id="86269-442">Version des ADF .NET SDK auf 4.5.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-442">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="86269-443">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="86269-443">Az.FrontDoor</span></span>
* <span data-ttu-id="86269-444">Unterstützung für den Ausschluss verwalteter WAF-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-444">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="86269-445">SocketAddr zur automatischen Vervollständigung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-445">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="86269-446">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="86269-446">Az.HealthcareApis</span></span>
* <span data-ttu-id="86269-447">Ausnahmebehandlung</span><span class="sxs-lookup"><span data-stu-id="86269-447">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="86269-448">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="86269-448">Az.KeyVault</span></span>
* <span data-ttu-id="86269-449">Fehler im Zusammenhang mit dem Zugriff auf einen möglicherweise nicht festgelegten Wert behoben</span><span class="sxs-lookup"><span data-stu-id="86269-449">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="86269-450">Zertifikatverwaltung für Kryptografie für elliptische Kurve</span><span class="sxs-lookup"><span data-stu-id="86269-450">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="86269-451">Unterstützung zum Angeben der Kurve für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-451">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="86269-452">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="86269-452">Az.Monitor</span></span>
* <span data-ttu-id="86269-453">Optionales Argument zum Befehl „Diagnoseeinstellungen hinzufügen“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-453">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="86269-454">Ein Optionsargument, das angibt, dass der Export in Log Analytics ein festes Schema sein muss (auch bekannt als</span><span class="sxs-lookup"><span data-stu-id="86269-454">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="86269-455">dedizierter Datentyp)</span><span class="sxs-lookup"><span data-stu-id="86269-455">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86269-456">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86269-456">Az.Network</span></span>
* <span data-ttu-id="86269-457">Unterstützung für IpGroups in der AzureFirewall-Anwendung sowie in NAT- und Netzwerkregeln</span><span class="sxs-lookup"><span data-stu-id="86269-457">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="86269-458">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86269-458">Az.Resources</span></span>
* <span data-ttu-id="86269-459">Problem behoben, aufgrund dessen die Vorlagenbereitstellung einen Vorlagenparameter nicht lesen kann, wenn der Name einen Konflikt mit einem integrierten Parameternamen verursacht</span><span class="sxs-lookup"><span data-stu-id="86269-459">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="86269-460">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-09-01 aktualisiert, die Gruppierungsunterstützung in Richtliniensatzdefinitionen einführt</span><span class="sxs-lookup"><span data-stu-id="86269-460">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="86269-461">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86269-461">Az.Sql</span></span>
* <span data-ttu-id="86269-462">Speichererstellung in automatischer Aktivierung der Sicherheitsrisikobewertung auf StorageV2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-462">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="86269-463">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86269-463">Az.Storage</span></span>
* <span data-ttu-id="86269-464">Unterstützung der Generierung blob-/containeridentitätsbasierter SAS-Token mit Speicherkontext auf der Grundlage der OAuth-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="86269-464">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="86269-465">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="86269-465">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="86269-466">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="86269-466">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="86269-467">Unterstützung für das Widerrufen von Schlüsseln für die Speicherkonto-Benutzerdelegierung hinzugefügt, sodass alle SAS-Identitätstoken widerrufen werden</span><span class="sxs-lookup"><span data-stu-id="86269-467">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="86269-468">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="86269-468">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="86269-469">Upgrade auf Microsoft.Azure.Management.Storage 14.2.0, um die neue API-Version 2019-06-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="86269-469">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="86269-470">Unterstützung von QuotaGiB (Freigabekontingent in Gibibyte) für Werte über 5120 in der Verwaltungsebene von Dateifreigabe-Cmdlets und Parameteralias „Quota“ zum Parameter „QuotaGiB“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-470">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="86269-471">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="86269-471">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="86269-472">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="86269-472">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="86269-473">Parameteralias „QuotaGiB“ zum Parameter „Quota“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-473">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="86269-474">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="86269-474">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="86269-475">Problem behoben, dass „Set-AzStorageContainerAcl“ die gespeicherte Zugriffsrichtlinie bereinigen kann</span><span class="sxs-lookup"><span data-stu-id="86269-475">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="86269-476">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="86269-476">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="86269-477">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="86269-477">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="86269-478">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="86269-478">Highlights since the last major release</span></span>
* <span data-ttu-id="86269-479">Az.DataBoxEdge 1.0.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="86269-479">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="86269-480">Az.SqlVirtualMachine 1.0.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="86269-480">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86269-481">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86269-481">Az.Compute</span></span>
* <span data-ttu-id="86269-482">Funktion zum erneuten Anwenden von VMs</span><span class="sxs-lookup"><span data-stu-id="86269-482">VM Reapply feature</span></span>
    - <span data-ttu-id="86269-483">Parameter für erneutes Anwenden zu Cmdlet „Set-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-483">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="86269-484">AutomaticRepairs-Funktion für VM-Skalierungsgruppe:</span><span class="sxs-lookup"><span data-stu-id="86269-484">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="86269-485">Parameter „EnableAutomaticRepair“, „AutomaticRepairGracePeriod“ und „AutomaticRepairMaxInstanceRepairsPercent“ zu folgenden Cmdlets hinzugefügt:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="86269-485">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="86269-486">Mandantenübergreifende Unterstützung von Katalogimages für „New-AzVM“</span><span class="sxs-lookup"><span data-stu-id="86269-486">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="86269-487">„Spot“ zu Argumentvervollständigung des Priority-Parameters in Cmdlets „New-AzVM“, „New-AzVMConfig“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-487">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="86269-488">Parameter „DiskIOPSReadWrite“ und „DiskMBpsReadWrite“ zu Cmdlet „Add-AzVmssDataDisk“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-488">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="86269-489">Parameter „SourceImageId“ von Cmdlet „New-AzGalleryImageVersion“ in optional geändert</span><span class="sxs-lookup"><span data-stu-id="86269-489">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="86269-490">Parameter „OSDiskImage“ und „DataDiskImage“ zu Cmdlet „New-AzGalleryImageVersion“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-490">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="86269-491">Parameter „HyperVGeneration“ zu Cmdlet „New-AzGalleryImageDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-491">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="86269-492">Parameter „SkipExtensionsOnOverprovisionedVMs“ zu Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-492">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="86269-493">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="86269-493">Az.DataBoxEdge</span></span>
* <span data-ttu-id="86269-494">Cmdlet `Get-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-494">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="86269-495">Bestellung abrufen</span><span class="sxs-lookup"><span data-stu-id="86269-495">Get the Order</span></span>
* <span data-ttu-id="86269-496">Cmdlet `New-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-496">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="86269-497">Neue Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="86269-497">Create new Order</span></span>
* <span data-ttu-id="86269-498">Cmdlet `Remove-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-498">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="86269-499">Bestellung entfernen</span><span class="sxs-lookup"><span data-stu-id="86269-499">Remove the Order</span></span>
* <span data-ttu-id="86269-500">Änderung im Cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="86269-500">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="86269-501">Erstellt jetzt eine lokale Freigabe</span><span class="sxs-lookup"><span data-stu-id="86269-501">Now creates Local Share</span></span>
* <span data-ttu-id="86269-502">Cmdlet `Set-AzDataBoxEdgeRole` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-502">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="86269-503">„IotRole“ kann jetzt einer Freigabe zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="86269-503">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="86269-504">Cmdlet `Invoke-AzDataBoxEdgeDevice` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-504">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="86269-505">Scanupdate aufrufen, Update herunterladen, Updates auf dem Gerät installieren</span><span class="sxs-lookup"><span data-stu-id="86269-505">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="86269-506">Cmdlet `Get-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-506">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="86269-507">Ruft die Informationen zu Auslösern ab</span><span class="sxs-lookup"><span data-stu-id="86269-507">Gets the information about Triggers</span></span>
* <span data-ttu-id="86269-508">Cmdlet `New-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-508">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="86269-509">Neue Auslöser erstellen</span><span class="sxs-lookup"><span data-stu-id="86269-509">Create new Triggers</span></span>
* <span data-ttu-id="86269-510">Cmdlet `Remove-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-510">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="86269-511">Auslöser entfernen</span><span class="sxs-lookup"><span data-stu-id="86269-511">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="86269-512">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="86269-512">Az.DataFactory</span></span>
* <span data-ttu-id="86269-513">Version des ADF .NET SDK auf 4.4.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-513">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="86269-514">Parameter „ExpressCustomSetup“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um Setupkonfigurationen und Drittanbieterkomponenten ohne benutzerdefiniertes Setupskript zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="86269-514">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="86269-515">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="86269-515">Az.DataLakeStore</span></span>
* <span data-ttu-id="86269-516">Dokumentation von „Get-AzDataLakeStoreDeletedItem“ und „Restore-AzDataLakeStoreDeletedItem“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-516">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="86269-517">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="86269-517">Az.EventHub</span></span>
* <span data-ttu-id="86269-518">Behebung des Problems 10301: Datumsformat von SAS-Token korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-518">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="86269-519">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="86269-519">Az.FrontDoor</span></span>
* <span data-ttu-id="86269-520">Parameter „MinimumTlsVersion“ zu „Enable-AzFrontDoorCustomDomainHttps“ und „New-AzFrontDoorFrontendEndpointObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-520">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="86269-521">Parameter „HealthProbeMethod“ und „EnabledState“ zu „New-AzFrontDoorHealthProbeSettingObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-521">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="86269-522">Neues Cmdlet zum Erstellen von BackendPoolsSettings-Objekten für die Übergabe in Erstellung/Update von Front Door hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-522">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="86269-523">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="86269-523">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86269-524">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86269-524">Az.Network</span></span>
* <span data-ttu-id="86269-525">FilterData-Optionsbeispiele „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ geändert.</span><span class="sxs-lookup"><span data-stu-id="86269-525">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="86269-526">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="86269-526">Az.PrivateDns</span></span>
* <span data-ttu-id="86269-527">PrivateDns.net-SDK auf Version 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-527">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="86269-528">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="86269-528">Az.RecoveryServices</span></span>
* <span data-ttu-id="86269-529">Azure Site Recovery-Unterstützung zum Auswählen des Datenträgertyps beim Aktivieren des Schutzes.</span><span class="sxs-lookup"><span data-stu-id="86269-529">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="86269-530">Fehlerbehebung bei Bearbeitungsaktion für Azure Site Recovery-Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="86269-530">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="86269-531">SQL-Wiederherstellungsunterstützung für Azure Backup zum Akzeptieren von Filestream-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="86269-531">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="86269-532">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="86269-532">Az.RedisCache</span></span>
* <span data-ttu-id="86269-533">Parameter „MinimumTlsVersion“ in Cmdlets „New-AzRedisCache“ und „Set-AzRedisCache“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-533">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="86269-534">Außerdem „MinimumTlsVersion“ in Ausgabe von Cmdlet „Get-AzRedisCache“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-534">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="86269-535">Validierung von Parameter „-Size“ für Cmdlets „Set-AzRedisCache“ und „New-AzRedisCache“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-535">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="86269-536">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86269-536">Az.Resources</span></span>
- <span data-ttu-id="86269-537">Richtlinien-Cmdlets aktualisiert, um die neue API-Version 2019-06-01 mit der neuen EnforcementMode-Eigenschaft bei der Richtlinienzuweisung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="86269-537">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="86269-538">Hilfebeispiel zum Erstellen von Richtliniendefinitionen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-538">Updated create policy definition help example</span></span>
- <span data-ttu-id="86269-539">Fehlerkorrektur: „Remove-AZADServicePrincipal -ServicePrincipalName“ gibt Nullverweis aus, wenn Dienstprinzipalname nicht gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="86269-539">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="86269-540">Fehlerkorrektur: „New-AZADServicePrincipal“ gibt Nullverweis aus, wenn Mandant kein Abonnement hat.</span><span class="sxs-lookup"><span data-stu-id="86269-540">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="86269-541">„New-AzAdServicePrincipal“ geändert, um Anmeldeinformation nur zu zugeordneter Anwendung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="86269-541">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="86269-542">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86269-542">Az.Sql</span></span>
* <span data-ttu-id="86269-543">Unterstützung von „ReadReplicaCount“ für Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-543">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="86269-544">Korrektur von „Set-AzSqlDatabase“, wenn Zonenredundanz nicht festgelegt</span><span class="sxs-lookup"><span data-stu-id="86269-544">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="86269-545">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="86269-545">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="86269-546">Allgemein</span><span class="sxs-lookup"><span data-stu-id="86269-546">General</span></span>
* <span data-ttu-id="86269-547">Az.PrivateDns 1.0.0 veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="86269-547">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="86269-548">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86269-548">Az.Accounts</span></span>
* <span data-ttu-id="86269-549">Hinweis zur Veraltung des Alias „Resolve-Error“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-549">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="86269-550">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="86269-550">Az.Advisor</span></span>
* <span data-ttu-id="86269-551">Neue Kategorie „Operational Excellence“ für Cmdlet „Get-AzAdvisorRecommendation“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-551">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="86269-552">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="86269-552">Az.Batch</span></span>
* <span data-ttu-id="86269-553">`CoreQuota` für `BatchAccountContext` in `DedicatedCoreQuota` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="86269-553">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="86269-554">Außerdem wurde das neue Element `LowPriorityCoreQuota` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-554">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="86269-555">Dies wirkt sich auf **Get-AzBatchAccount** aus.</span><span class="sxs-lookup"><span data-stu-id="86269-555">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="86269-556">Für Parameter `-ResourceFile` von **New-AzBatchTask** wird jetzt eine Sammlung mit `PSResourceFile`-Objekten verwendet, und für die Erstellung kann das Cmdlet **New-AzBatchResourceFile** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="86269-556">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="86269-557">Neues Cmdlet **New-AzBatchResourceFile** als Hilfe für die Erstellung von `PSResourceFile`-Objekten.</span><span class="sxs-lookup"><span data-stu-id="86269-557">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="86269-558">Diese können für **New-AzBatchTask** über den Parameter `-ResourceFile` bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="86269-558">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="86269-559">Hierbei werden zusätzlich zum Ansatz mit `HttpUrl` zwei neue Arten von Ressourcendateien unterstützt:</span><span class="sxs-lookup"><span data-stu-id="86269-559">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="86269-560">Mit Ressourcendateien, die auf `AutoStorageContainerName` basieren, wird ein gesamter Container für die automatische Speicherung auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="86269-560">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="86269-561">Für Ressourcendateien, die auf `StorageContainerUrl` basieren, wird der in der URL angegebene Container auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="86269-561">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="86269-562">`ApplicationPackages`-Eigenschaft von `PSApplication` entfernt, die von **Get-AzBatchApplication** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="86269-562">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="86269-563">Die spezifischen Pakete in einer Anwendung können jetzt mit **Get-AzBatchApplicationPackage** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="86269-563">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="86269-564">Beispiel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="86269-564">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="86269-565">`ApplicationId` für **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** und **Set-AzBatchApplication** in `ApplicationName` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="86269-565">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="86269-566">`ApplicationId` ist jetzt ein Alias von `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="86269-566">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="86269-567">Neue `PSWindowsUserConfiguration`-Eigenschaft zu `PSUserAccount` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-567">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="86269-568">`Version` für `PSApplicationPackage` in `Name` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="86269-568">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="86269-569">`BlobSource` für `PSResourceFile` in `HttpUrl` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="86269-569">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="86269-570">`OSDisk`-Eigenschaft aus `PSVirtualMachineConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="86269-570">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="86269-571">**Set-AzBatchPoolOSVersion** entfernt.</span><span class="sxs-lookup"><span data-stu-id="86269-571">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="86269-572">Dieser Vorgang wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="86269-572">This operation is no longer supported.</span></span>
* <span data-ttu-id="86269-573">`TargetOSVersion` aus `PSCloudServiceConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="86269-573">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="86269-574">`CurrentOSVersion` für `PSCloudServiceConfiguration` in `OSVersion` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="86269-574">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="86269-575">`DataEgressGiB` und `DataIngressGiB` aus `PSPoolUsageMetrics` entfernt.</span><span class="sxs-lookup"><span data-stu-id="86269-575">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="86269-576">**Get-AzBatchNodeAgentSku** entfernt und durch **Get-AzBatchSupportedImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="86269-576">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="86269-577">**Get-AzBatchSupportedImage** gibt die gleichen Daten wie **Get-AzBatchNodeAgentSku** zurück, aber in einem benutzerfreundlicheren Format.</span><span class="sxs-lookup"><span data-stu-id="86269-577">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="86269-578">Neue nicht verifizierte Images werden nun ebenfalls zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="86269-578">New non-verified images are also now returned.</span></span> <span data-ttu-id="86269-579">Zusätzlich sind weitere Informationen zu `Capabilities` und `BatchSupportEndOfLife` für jedes Image vorhanden.</span><span class="sxs-lookup"><span data-stu-id="86269-579">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="86269-580">Möglichkeit zum Bereitstellen von Remotedateisystemen auf jedem Knoten eines Pools über den neuen Parameter `MountConfiguration` von **New-AzBatchPool** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-580">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="86269-581">Es ist jetzt Unterstützung für Sicherheitsregeln vorhanden, die den Netzwerkzugriff auf einen Pool basierend auf dem Quellport des Datenverkehrs blockieren.</span><span class="sxs-lookup"><span data-stu-id="86269-581">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="86269-582">Dies erfolgt über die `SourcePortRanges`-Eigenschaft unter `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="86269-582">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="86269-583">Bei der Ausführung eines Containers unterstützt Batch jetzt die Ausführung der Aufgabe im Arbeitsverzeichnis des Containers bzw. im Arbeitsverzeichnis der Batch-Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="86269-583">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="86269-584">Dies wird mit der `WorkingDirectory`-Eigenschaft unter `PSTaskContainerSettings` gesteuert.</span><span class="sxs-lookup"><span data-stu-id="86269-584">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="86269-585">Möglichkeit zum Angeben einer Sammlung mit öffentlichen IP-Adressen für `PSNetworkConfiguration` über die neue `PublicIPs`-Eigenschaft hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-585">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="86269-586">So wird sichergestellt, dass Knoten im Pool über eine IP-Adresse aus der Liste mit den von Benutzern bereitgestellten IP-Adressen verfügen.</span><span class="sxs-lookup"><span data-stu-id="86269-586">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="86269-587">Wenn kein Wert angegeben wird, lautet der Standardwert von `WaitForSuccess` unter `PSSTartTask` jetzt `$True` (bisher `$False`).</span><span class="sxs-lookup"><span data-stu-id="86269-587">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="86269-588">Wenn kein Wert angegeben wird, lautet der Standardwert von `Scope` unter `PSAutoUserSpecification` jetzt `Pool` (bisher `Task` unter Windows und `Pool` unter Linux).</span><span class="sxs-lookup"><span data-stu-id="86269-588">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="86269-589">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="86269-589">Az.Cdn</span></span>
* <span data-ttu-id="86269-590">„UrlRewriteAction“ und „CacheKeyQueryStringAction“ für „RulesEngine“ eingeführt.</span><span class="sxs-lookup"><span data-stu-id="86269-590">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="86269-591">Mehrere Fehler behoben, z. B. fehlende „Selector“-Eingabe im Cmdlet „New-AzDeliveryRuleCondition“.</span><span class="sxs-lookup"><span data-stu-id="86269-591">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86269-592">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86269-592">Az.Compute</span></span>
* <span data-ttu-id="86269-593">Feature „Datenträgerverschlüsselungssatz“</span><span class="sxs-lookup"><span data-stu-id="86269-593">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="86269-594">Neue Cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="86269-594">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="86269-595">Parameter „DiskEncryptionSetId“ wurde den folgenden Cmdlets hinzugefügt:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="86269-595">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="86269-596">Die Parameter „DiskEncryptionSetId“ und „EncryptionType“ wurden den folgenden Cmdlets hinzugefügt:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="86269-596">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="86269-597">Parameter „PublicIPAddressVersion“ wurde „New-AzVmssIPConfig“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-597">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="86269-598">„FileUris“ für benutzerdefinierte Skripterweiterung von öffentlicher Einstellung auf geschützte Einstellung umgestellt.</span><span class="sxs-lookup"><span data-stu-id="86269-598">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="86269-599">„ScaleInPolicy“ wurde den Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-599">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="86269-600">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="86269-600">Breaking changes</span></span>
    - <span data-ttu-id="86269-601">Parameter „UploadSizeInBytes“ wird anstelle von „DiskSizeGB“ für „New-AzDiskConfig“ verwendet, wenn „CreateOption“ auf „Upload“ festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="86269-601">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="86269-602">Im „GalleryImageVersion“-Objekt wurde „objectPublishingProfile.Source.ManagedImage.Id“ durch „StorageProfile.Source.Id“ ersetzt.</span><span class="sxs-lookup"><span data-stu-id="86269-602">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="86269-603">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="86269-603">Az.DataFactory</span></span>
* <span data-ttu-id="86269-604">Version des ADF .NET SDK auf 4.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="86269-604">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="86269-605">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="86269-605">Az.DataLakeStore</span></span>
* <span data-ttu-id="86269-606">Update für ADLS SDK-Version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) mit den folgenden Fehlerbehebungen durchgeführt:</span><span class="sxs-lookup"><span data-stu-id="86269-606">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="86269-607">Vermeidung der Auslösung einer Ausnahme, während die Deserialisierung des „creationtime“-Elements des Papierkorb- oder Verzeichniseintrags nicht durchgeführt werden kann</span><span class="sxs-lookup"><span data-stu-id="86269-607">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="86269-608">Verfügbarmachung der Einstellung pro Anforderungszeitlimit in „adlsclient“</span><span class="sxs-lookup"><span data-stu-id="86269-608">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="86269-609">Fehlerbehebung für Übergabe des ursprünglichen „syncflag“-Elements für badoffset-Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="86269-609">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="86269-610">Fehlerbehebung für „EnumerateDirectory“ zum Abrufen des Fortsetzungstokens nach der Überprüfung der Antwort</span><span class="sxs-lookup"><span data-stu-id="86269-610">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="86269-611">Behebung eines Verkettungsfehlers</span><span class="sxs-lookup"><span data-stu-id="86269-611">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="86269-612">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="86269-612">Az.FrontDoor</span></span>
* <span data-ttu-id="86269-613">Verschiedene Tippfehler im Modul korrigiert.</span><span class="sxs-lookup"><span data-stu-id="86269-613">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="86269-614">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="86269-614">Az.HDInsight</span></span>
* <span data-ttu-id="86269-615">Fehler behoben, bei dem Kunden die Meldung „Keine gültige Base64-Zeichenfolge“ erhalten haben, wenn sie „Get-AzHDInsightCluster“ zum Abrufen des Clusters mit ADLSGen1-Speicher verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="86269-615">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="86269-616">Parameter mit dem Namen „ApplicationId“ den drei Cmdlets „Add-AzHDInsightClusterIdentity“, „New-AzHDInsightClusterConfig“ und „New-AzHDInsightCluster“ hinzugefügt, damit der Kunde die Dienstprinzipal-Anwendungs-ID für den Zugriff auf Azure Data Lake bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="86269-616">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="86269-617">Microsoft.Azure.Management.HDInsight von 2.1.0 in 5.1.0 geändert.</span><span class="sxs-lookup"><span data-stu-id="86269-617">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="86269-618">Fünf Cmdlets wurden entfernt:</span><span class="sxs-lookup"><span data-stu-id="86269-618">Removed five cmdlets:</span></span>
    - <span data-ttu-id="86269-619">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="86269-619">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="86269-620">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="86269-620">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="86269-621">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="86269-621">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="86269-622">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="86269-622">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="86269-623">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="86269-623">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="86269-624">Drei Cmdlets wurden hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="86269-624">Added three cmdlets:</span></span>
    - <span data-ttu-id="86269-625">„Get-AzHDInsightMonitoring“ als Ersatz für „Get-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="86269-625">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="86269-626">„Enable-AzHDInsightMonitoring“ als Ersatz für „Enable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="86269-626">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="86269-627">„Disable-AzHDInsightMonitoring“ als Ersatz für „Disable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="86269-627">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="86269-628">Fehler für Cmdlet „Get-AzHDInsightProperties“ behoben, um Unterstützung für das Abrufen von Funktionsinformationen von einem bestimmten Ort bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="86269-628">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="86269-629">Parametersätze („Spark1“, „Spark2“) aus „Add-AzHDInsightConfigValue“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="86269-629">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="86269-630">Beispiele den Hilfedokumenten des Cmdlets „Add-AzHDInsightSecurityProfile“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-630">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="86269-631">Der Ausgabetyp der folgenden Cmdlets wurde geändert:</span><span class="sxs-lookup"><span data-stu-id="86269-631">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="86269-632">Ausgabetyp für „Get-AzHDInsightProperties“ von „CapabilitiesResponse“ in „AzureHDInsightCapabilities“ geändert.</span><span class="sxs-lookup"><span data-stu-id="86269-632">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="86269-633">Ausgabetyp für „Remove-AzHDInsightCluster“ von „ClusterGetResponse“ in „bool“ geändert.</span><span class="sxs-lookup"><span data-stu-id="86269-633">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="86269-634">Ausgabetyp für „Set-AzHDInsightGatewaySettings“ von „HttpConnectivitySettings“ in „GatewaySettings“ geändert.</span><span class="sxs-lookup"><span data-stu-id="86269-634">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="86269-635">Einige Testfälle für Szenarien wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-635">Added some scenario test cases.</span></span>
* <span data-ttu-id="86269-636">Aliase wurden entfernt: „Add-AzHDInsightConfigValues“, „Get-AzHDInsightProperties“.</span><span class="sxs-lookup"><span data-stu-id="86269-636">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="86269-637">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="86269-637">Az.IotHub</span></span>
* <span data-ttu-id="86269-638">Wichtige Änderungen:</span><span class="sxs-lookup"><span data-stu-id="86269-638">Breaking changes:</span></span>
    - <span data-ttu-id="86269-639">Das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="86269-639">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="86269-640">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="86269-640">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="86269-641">Das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="86269-641">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="86269-642">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="86269-642">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="86269-643">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="86269-643">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="86269-644">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="86269-644">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="86269-645">Das Cmdlet „New-AzIotHubExportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubExportDevices“.</span><span class="sxs-lookup"><span data-stu-id="86269-645">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="86269-646">Das Cmdlet „New-AzIotHubImportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubImportDevices“.</span><span class="sxs-lookup"><span data-stu-id="86269-646">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="86269-647">Das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="86269-647">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="86269-648">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="86269-648">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="86269-649">Das Cmdlet „Set-AzIotHub“ unterstützt den Parameter „OperationsMonitoringProperties“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="86269-649">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="86269-650">Der Parametersatz „UpdateOperationsMonitoringProperties“ für das Cmdlet „Set-AzIotHub“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="86269-650">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="86269-651">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="86269-651">Az.RecoveryServices</span></span>
* <span data-ttu-id="86269-652">Azure wurde die Azure Site Recovery-Unterstützung zum Konfigurieren von Netzwerkressourcen, z. B. NSG, öffentliche IP-Adresse und interner Load Balancer für Azure, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-652">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="86269-653">Azure Site Recovery-Unterstützung zum Schreiben auf verwaltete Datenträger für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-653">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="86269-654">Azure Site Recovery-Unterstützung für NIC-Reduzierung für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-654">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="86269-655">Azure wurde Azure Site Recovery-Unterstützung für beschleunigten Netzwerkbetrieb für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-655">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="86269-656">Azure wurde Azure Site Recovery-Unterstützung für automatische Agent-Updates für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-656">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="86269-657">Azure wurde Azure Site Recovery-Unterstützung für SSD Standard für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-657">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="86269-658">Azure wurde Azure Site Recovery-Unterstützung für das zweistufige Azure Disk Encryption-Verfahren für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-658">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="86269-659">Azure wurde Azure Site Recovery-Unterstützung für das Schützen von neu hinzugefügten Datenträgern für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-659">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="86269-660">Feature „Vorläufiges Löschen“ (SoftDelete) für VM und zugehörige Tests hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-660">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="86269-661">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86269-661">Az.Resources</span></span>
* <span data-ttu-id="86269-662">Abhängigkeitsassembly „Microsoft.Extensions.Caching.Memory“ von 1.1.1 auf 2.2 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="86269-662">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86269-663">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86269-663">Az.Network</span></span>
* <span data-ttu-id="86269-664">Alle Cmdlets für „PrivateEndpointConnection“ geändert, um Unterstützung für generischen Dienstanbieter bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="86269-664">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="86269-665">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="86269-665">Updated cmdlet:</span></span>
        - <span data-ttu-id="86269-666">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="86269-666">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="86269-667">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="86269-667">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="86269-668">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="86269-668">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="86269-669">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="86269-669">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="86269-670">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="86269-670">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="86269-671">Neues Cmdlet für „PrivateLinkResource“ hinzugefügt, einschließlich Unterstützung des generischen Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="86269-671">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="86269-672">Neues Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="86269-672">New cmdlet:</span></span>
        - <span data-ttu-id="86269-673">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="86269-673">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="86269-674">Neue Felder und Parameter für das Feature „Proxyprotokoll V2“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-674">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="86269-675">„EnableProxyProtocol“-Eigenschaft in „PrivateLinkService“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-675">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="86269-676">„LinkIdentifier“-Eigenschaft in „PrivateEndpointConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-676">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="86269-677">„New-AzPrivateLinkService“ aktualisiert, um den neuen optionalen Parameter „EnableProxyProtocol“ hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="86269-677">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="86269-678">Fehlerhafte Parameterbeschreibung in Referenzdokumentation von „New-AzApplicationGatewaySku“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="86269-678">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="86269-679">Neue Cmdlets zur Unterstützung der Azure-Firewallrichtlinie hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-679">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="86269-680">Unterstützung für untergeordnete Ressource „RouteTables“ von VirtualHub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-680">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="86269-681">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="86269-681">New cmdlets added:</span></span>
        - <span data-ttu-id="86269-682">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="86269-682">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="86269-683">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="86269-683">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="86269-684">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="86269-684">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="86269-685">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="86269-685">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="86269-686">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="86269-686">Set-AzVirtualHub</span></span>
* <span data-ttu-id="86269-687">Unterstützung für die neuen Eigenschaften „Sku“ von VirtualHub und „VirtualWANType“ von VirtualWan hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-687">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="86269-688">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="86269-688">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="86269-689">New-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-689">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="86269-690">Update-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-690">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="86269-691">New-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-691">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="86269-692">Update-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-692">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="86269-693">Unterstützung für „EnableInternetSecurity“-Eigenschaft für „HubVnetConnection“, „VpnConnection“ und „ExpressRouteConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-693">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="86269-694">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="86269-694">New cmdlets added:</span></span>
        - <span data-ttu-id="86269-695">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="86269-695">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="86269-696">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="86269-696">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="86269-697">New-AzureRmVirtualHubVnetConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-697">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="86269-698">New-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-698">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="86269-699">Update-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-699">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="86269-700">New-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-700">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="86269-701">Set-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-701">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="86269-702">Unterstützung für die Konfiguration der „WebApplicationFirewall“-Richtlinie der obersten Ebene hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-702">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="86269-703">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="86269-703">New cmdlets added:</span></span>
        - <span data-ttu-id="86269-704">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="86269-704">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="86269-705">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="86269-705">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="86269-706">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="86269-706">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="86269-707">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="86269-707">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="86269-708">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="86269-708">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="86269-709">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="86269-709">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="86269-710">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="86269-710">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="86269-711">New-AzApplicationGatewayFirewallPolicy: Parameter „PolicySetting“, „ManagedRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-711">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="86269-712">Unterstützung für Operator „Geo-Match“ unter „CustomRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-712">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="86269-713">„GeoMatch“ zum Operator von „FirewallCondition“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-713">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="86269-714">Unterstützung für Firewallrichtlinien „perListener“ und „perSite“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-714">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="86269-715">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="86269-715">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="86269-716">New-AzApplicationGatewayHttpListener: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-716">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="86269-717">New-AzApplicationGatewayPathRuleConfig: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-717">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="86269-718">Fehlerbehebung: Nichtbeachtung der Groß-/Kleinschreibung für erforderliches Subnetz mit dem Namen „AzureBastionSubnet“ in „PSBastion“ ist jetzt möglich.</span><span class="sxs-lookup"><span data-stu-id="86269-718">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="86269-719">Unterstützung für Ziel-FQDNs in Netzwerkregeln und Übersetzung von FQDN in NAT-Regeln für Azure Firewall hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-719">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="86269-720">Unterstützung für Ressource „RouteTables“ der obersten Ebene von „IpGroup“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-720">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="86269-721">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="86269-721">New cmdlets added:</span></span>
        - <span data-ttu-id="86269-722">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="86269-722">New-AzIpGroup</span></span>
        - <span data-ttu-id="86269-723">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="86269-723">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="86269-724">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="86269-724">Get-AzIpGroup</span></span>
        - <span data-ttu-id="86269-725">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="86269-725">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="86269-726">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="86269-726">Az.ServiceFabric</span></span>
* <span data-ttu-id="86269-727">Cmdlet „Add-AzServiceFabricApplicationCertificate“ entfernt, da dieses Szenario durch „Add-AzVmssSecret“ abgedeckt ist.</span><span class="sxs-lookup"><span data-stu-id="86269-727">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="86269-728">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86269-728">Az.Sql</span></span>
* <span data-ttu-id="86269-729">Unterstützung für die Wiederherstellung von gelöschten Datenbanken auf verwalteten Instanzen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-729">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="86269-730">Veraltete Cmdlets für die Überprüfung aus Code ausgesondert.</span><span class="sxs-lookup"><span data-stu-id="86269-730">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="86269-731">Veraltete Aliase entfernt:</span><span class="sxs-lookup"><span data-stu-id="86269-731">Removed deprecated aliases:</span></span>
* <span data-ttu-id="86269-732">Get-AzSqlDatabaseIndexRecommendations (stattdessen „Get-AzSqlDatabaseIndexRecommendation“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="86269-732">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="86269-733">Get-AzSqlDatabaseRestorePoints (stattdessen „Get-AzSqlDatabaseRestorePoint“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="86269-733">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="86269-734">Cmdlet „Get-AzSqlDatabaseSecureConnectionPolicy“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="86269-734">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="86269-735">Aliase für veraltete Cmdlets für Einstellungen zur Sicherheitsrisikobewertung wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="86269-735">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="86269-736">Cmdlets für Einstellungen für die erweiterte Bedrohungserkennung wurden als veraltet eingestuft.</span><span class="sxs-lookup"><span data-stu-id="86269-736">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="86269-737">Cmdlets zum Deaktivieren und Aktivieren von Vertraulichkeitsempfehlungen in Spalten einer Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-737">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="86269-738">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86269-738">Az.Storage</span></span>
* <span data-ttu-id="86269-739">Unterstützung für große Dateifreigaben beim Erstellen oder Aktualisieren eines Speicherkontos hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-739">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="86269-740">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="86269-740">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="86269-741">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="86269-741">Set-AzStorageAccount</span></span>
* <span data-ttu-id="86269-742">Beim Schließen/Abrufen des Dateihandles wird die Überprüfung des Eingabepfads auf Dateiverzeichnis oder Datei übersprungen, um einen Fehler für das Objekt im Status „DeletePending“ zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="86269-742">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="86269-743">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="86269-743">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="86269-744">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="86269-744">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="86269-745">2.8.0: Oktober 2019</span><span class="sxs-lookup"><span data-stu-id="86269-745">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="86269-746">Allgemein</span><span class="sxs-lookup"><span data-stu-id="86269-746">General</span></span>
* <span data-ttu-id="86269-747">Az.HealthcareApis-Release 1.0.0</span><span class="sxs-lookup"><span data-stu-id="86269-747">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="86269-748">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86269-748">Az.Accounts</span></span>
* <span data-ttu-id="86269-749">Telemetriedaten und URL-Umschreibung für generierte Module aktualisiert, Windows-Komponententests korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-749">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="86269-750">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="86269-750">Az.ApiManagement</span></span>
* <span data-ttu-id="86269-751">**Set-AzApiManagementApi**: Unterstützung für die Aktualisierung der API in „ApiVersionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-751">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="86269-752">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="86269-752">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="86269-753">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="86269-753">Az.Automation</span></span>
* <span data-ttu-id="86269-754">Cmdlet „New-AzureAutomationSoftwareUpdateConfiguration“ für den Parameter für die Linux-Neustarteinstellung korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-754">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="86269-755">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="86269-755">Az.Batch</span></span>
* <span data-ttu-id="86269-756">**Get-AzBatchNodeAgentSku** ist veraltet und wird in Version 2.0.0 durch **Get-AzBatchSupportImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="86269-756">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86269-757">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86269-757">Az.Compute</span></span>
* <span data-ttu-id="86269-758">Parameter „Priority“, „EvictionPolicy“ und „MaxPrice“ zu den Cmdlets „“New-AzVM“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-758">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="86269-759">Warnmeldung und Hilfedokument für die Cmdlets „Add-AzVMAdditionalUnattendContent“ und „Add-AzVMSshPublicKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-759">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="86269-760">Ausnahme „-skipVmBackup“ Linux-VMs mit verwalteten Datenträgern für „Set-AzVMDiskEncryptionExtension“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-760">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="86269-761">Fehler beim Aktualisieren von Verschlüsselungseinstellungen in „Set-AzVMDiskEncryptionExtension“ korrigiert (zweistufiges Szenario)</span><span class="sxs-lookup"><span data-stu-id="86269-761">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="86269-762">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="86269-762">Az.DataFactory</span></span>
* <span data-ttu-id="86269-763">CRUD-Befehle für ADF V2-Datenfluss hinzugefügt: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow und Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="86269-763">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="86269-764">Aktionsbefehle für Debugsitzung für ADF V2-Datenfluss hinzugefügt: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand und Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="86269-764">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="86269-765">Version des ADF .NET SDK auf 4.2.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-765">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="86269-766">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="86269-766">Az.DataLakeStore</span></span>
* <span data-ttu-id="86269-767">Kontoüberprüfung korrigiert, sodass Konten mit „-“ ohne Domäne übermittelt werden können</span><span class="sxs-lookup"><span data-stu-id="86269-767">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="86269-768">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="86269-768">Az.HealthcareApis</span></span>
* <span data-ttu-id="86269-769">PowerShell-Version auf 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-769">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="86269-770">SDK-Version auf 1.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-770">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="86269-771">Aktualisierung in Tests, um auf neue SDK-Version zu verweisen</span><span class="sxs-lookup"><span data-stu-id="86269-771">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="86269-772">Ausgabestruktur von geschachtelt in vereinfacht geändert</span><span class="sxs-lookup"><span data-stu-id="86269-772">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="86269-773">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="86269-773">Az.IotHub</span></span>
* <span data-ttu-id="86269-774">Neue Routingquelle hinzugefügt: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="86269-774">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="86269-775">Kleinere Fehlerbehebung: „Get-AzIothub“ gibt „subscriptionId“ nicht zurück.</span><span class="sxs-lookup"><span data-stu-id="86269-775">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="86269-776">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="86269-776">Az.Monitor</span></span>
* <span data-ttu-id="86269-777">Neue Aktionsgruppenempfänger für Aktionsgruppe hinzugefügt:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="86269-777">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="86269-778">Verwendung des allgemeinen Warnungsschemas für Empfänger aktiviert.</span><span class="sxs-lookup"><span data-stu-id="86269-778">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="86269-779">Dies gilt nicht für SMS, Azure App-Pushbenachrichtigungen, ITSM und Sprachempfänger.</span><span class="sxs-lookup"><span data-stu-id="86269-779">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="86269-780">Webhooks unterstützen nun die Azure Active Directory-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="86269-780">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86269-781">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86269-781">Az.Network</span></span>
* <span data-ttu-id="86269-782">Neues Cmdlet „Get-AzAvailableServiceAlias“ hinzugefügt, das zum Abrufen der Aliase aufgerufen werden kann, die für Dienstendpunktrichtlinien verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="86269-782">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="86269-783">Unterstützung für das Hinzufügen von Verbindungen von Datenverkehrsselektoren zu Virtual Network-Gatewayverbindungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-783">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="86269-784">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="86269-784">New cmdlets added:</span></span>
        - <span data-ttu-id="86269-785">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="86269-785">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="86269-786">Cmdlets mit optionalen Parametern aktualisiert: -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="86269-786">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="86269-787">Unterstützung für ESP- und AH-Protokolle in Konfigurationen von Netzwerksicherheitsregeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-787">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="86269-788">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="86269-788">Updated cmdlets:</span></span>
        - <span data-ttu-id="86269-789">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="86269-789">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="86269-790">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="86269-790">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="86269-791">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="86269-791">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="86269-792">Verbesserte Behandlung von Ausnahmen in Cortex-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="86269-792">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="86269-793">Neue Generationen und SKUs für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="86269-793">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="86269-794">Einführung neuer Generationen für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="86269-794">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="86269-795">Einführung neuer SKUs mit höherem Durchsatz für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="86269-795">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="86269-796">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="86269-796">Az.RedisCache</span></span>
* <span data-ttu-id="86269-797">Referenzdokumentation zu „Set-AzRedisCache“ aktualisiert, um fehlende Werte für den Parameter „-Size“ aufzunehmen</span><span class="sxs-lookup"><span data-stu-id="86269-797">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="86269-798">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86269-798">Az.Sql</span></span>
* <span data-ttu-id="86269-799">Unterstützung für das Festlegen des Active Directory-Administrators für verwaltete Instanz hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-799">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="86269-800">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86269-800">Az.Storage</span></span>
* <span data-ttu-id="86269-801">Storage-Clientbibliothek auf 11.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-801">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="86269-802">Auflisten von Containern mit der API der Verwaltungsebene, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="86269-802">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="86269-803">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="86269-803">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="86269-804">Auflisten von Storage-Konten aus Abonnements, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="86269-804">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="86269-805">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="86269-805">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="86269-806">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="86269-806">Az.StorageSync</span></span>
* <span data-ttu-id="86269-807">Problem 9810 in „Reset-AzStorageSyncServerCertificate“ behoben</span><span class="sxs-lookup"><span data-stu-id="86269-807">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="86269-808">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="86269-808">Az.Websites</span></span>
* <span data-ttu-id="86269-809">Fehler beim Aktualisieren von ASP einer App mit „Set-AzWebApp“</span><span class="sxs-lookup"><span data-stu-id="86269-809">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="86269-810">2.7.0: September 2019</span><span class="sxs-lookup"><span data-stu-id="86269-810">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="86269-811">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="86269-811">Az.ApiManagement</span></span>
* <span data-ttu-id="86269-812">Beschreibung des Parameters „-Format“ in der Referenzdokumentation für „Set-AzApiManagementPolicy“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-812">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="86269-813">Verweise des veralteten Cmdlets „Update-AzApiManagementDeployment“ aus Referenzdokumentation entfernt.</span><span class="sxs-lookup"><span data-stu-id="86269-813">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="86269-814">Verwenden Sie stattdessen „Set-AzApiManagement“.</span><span class="sxs-lookup"><span data-stu-id="86269-814">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="86269-815">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="86269-815">Az.Automation</span></span>
* <span data-ttu-id="86269-816">Tippfehler im Beispiel in der Referenzdokumentation für „Register-AzAutomationDscNode“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-816">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="86269-817">Erläuterung zur Betriebssystemeinschränkung zu „Register-AzAutomationDSCNode“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-817">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="86269-818">Nullverweisausnahme des Cmdlets „Start-AzAutomationRunbook“ für die Option „-Wait“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="86269-818">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86269-819">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86269-819">Az.Compute</span></span>
* <span data-ttu-id="86269-820">Parameter „UploadSizeInBytes“ zu „New-AzDiskConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-820">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="86269-821">Inkrementeller Parameter zu „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-821">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="86269-822">Feature für VM mit niedriger Priorität hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="86269-822">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="86269-823">Parameter „MaxPrice“, „EvictionPolicy“ und „Priority“ zu New-AzVMConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-823">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="86269-824">Parameter „MaxPrice“ zu den Cmdlets „New-AzVmssConfig“, „Update-AzVM“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-824">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="86269-825">Fehlerbehebung für VM-Verweis für das Cmdlet „Get-AzAvailabilitySet“, wenn alle Verfügbarkeitsgruppen im Abonnement aufgelistet werden</span><span class="sxs-lookup"><span data-stu-id="86269-825">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="86269-826">Nullausnahme für „Get-AzRemoteDesktopFile“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-826">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="86269-827">VHD-Suchmethode für Position relativ zum Ende korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-827">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="86269-828">Problem mit UltraSSD für „New-AzVM“ und „Update-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="86269-828">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="86269-829">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="86269-829">Az.DataFactory</span></span>
* <span data-ttu-id="86269-830">Drei neue Befehle für ADF V2 hinzugefügt: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription und Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="86269-830">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="86269-831">Version des ADF .NET SDK auf 4.1.3 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-831">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="86269-832">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="86269-832">Az.HDInsight</span></span>
* <span data-ttu-id="86269-833">Hinweis auf Breaking Changes hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-833">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="86269-834">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="86269-834">Az.IotHub</span></span>
* <span data-ttu-id="86269-835">Unterstützung zum Aufrufen eines Failovers für einen IoT-Hub zur geografisch gekoppelten Notfallwiederherstellungsregion hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-835">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="86269-836">Unterstützung zum Verwalten der Nachrichtenanreicherung für einen IoT-Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-836">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="86269-837">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="86269-837">New cmdlets are:</span></span>
    - <span data-ttu-id="86269-838">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="86269-838">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="86269-839">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="86269-839">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="86269-840">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="86269-840">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="86269-841">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="86269-841">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="86269-842">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="86269-842">Az.Monitor</span></span>
* <span data-ttu-id="86269-843">Verweis auf das aktuelle Monitor SDK, d. h. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="86269-843">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="86269-844">Geringfügige Änderungen an den Metrik-Cmdlets vorgenommen, d. h. die Einheitenenumeration unterstützt verschiedene neue Werte.</span><span class="sxs-lookup"><span data-stu-id="86269-844">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="86269-845">Dabei handelt es sich um schreibgeschützte Cmdlets, sodass keine Änderungen an der Eingabe der Cmdlets erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="86269-845">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="86269-846">Die API-Version der **ActionGroups**-Anforderungen lautet jetzt **2019-06-01** (zuvor **2018-03-01**).</span><span class="sxs-lookup"><span data-stu-id="86269-846">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="86269-847">Die Szenariotests wurden aktualisiert, um diese Änderung zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="86269-847">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="86269-848">Die Konstruktoren für die Klassen **EmailReceiver** und **WebhookReceiver** haben ein neues obligatorisches Argument hinzugefügt, d. h. einen booleschen Wert namens **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="86269-848">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="86269-849">Derzeit ist der Wert auf **false** festgelegt, damit sich dieser Breaking Change nicht auf die Cmdlets auswirkt.</span><span class="sxs-lookup"><span data-stu-id="86269-849">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="86269-850">**HINWEIS:** Dies ist eine vorübergehende Änderung, die vom Team für Warnungen validiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="86269-850">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="86269-851">Die Reihenfolge der Argumente für den Konstruktor der Klasse **Source** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="86269-851">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="86269-852">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="86269-852">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="86269-853">Die Reihenfolge der Argumente für den Konstruktor der Klasse **AlertingAction** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="86269-853">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="86269-854">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="86269-854">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="86269-855">Unterstützung von Kriterien für dynamische Schwellwerte für Metrikwarnung v2</span><span class="sxs-lookup"><span data-stu-id="86269-855">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="86269-856">New-AzMetricAlertRuleV2Criteria: Erstellt nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="86269-856">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="86269-857">Add-AzMetricAlertRuleV2: Akzeptiert nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="86269-857">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="86269-858">Verbesserungen an den Cmdlets für geplante Abfrageregeln (Scheduled Query Rule, SQR)</span><span class="sxs-lookup"><span data-stu-id="86269-858">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="86269-859">Cmdlets akzeptieren den Parameter „Location“ in zwei Formaten: entweder den Standort (z. B. „eastus“) oder den Anzeigenamen des Standorts (z. B. „USA, Osten“)</span><span class="sxs-lookup"><span data-stu-id="86269-859">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="86269-860">Parameter „Enabled“ in Hilfedateien ordnungsgemäß dargestellt</span><span class="sxs-lookup"><span data-stu-id="86269-860">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="86269-861">Beispiele für optionalen Parameter „ActionGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-861">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="86269-862">Hilfedateien insgesamt verbessert</span><span class="sxs-lookup"><span data-stu-id="86269-862">Overall improved help files</span></span>
* <span data-ttu-id="86269-863">Fehler beim Bestimmen des Bereichstyps für „Set-AzActionRule“ behoben</span><span class="sxs-lookup"><span data-stu-id="86269-863">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86269-864">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86269-864">Az.Network</span></span>
* <span data-ttu-id="86269-865">Fehlerhaftes Beispiel in der Referenzdokumentation zu „New-AzApplicationGateway“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-865">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="86269-866">Hinweis in der Referenzdokumentation zu „Get-AzNetworkWatcherPacketCapture“ zum Abrufen aller Eigenschaften für eine Paketerfassung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-866">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="86269-867">Beispiel in der Referenzdokumentation zu „Test-AzNetworkWatcherIPFlow“ korrigiert, um die Netzwerkadapter ordnungsgemäß aufzulisten</span><span class="sxs-lookup"><span data-stu-id="86269-867">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="86269-868">Cloudausnahmeanalyse verbessert, um ggf. zusätzliche Details anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="86269-868">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="86269-869">Cloudausnahmeanalyse verbessert, um zusätzlichen Typ der SDK-Ausnahme zu verarbeiten</span><span class="sxs-lookup"><span data-stu-id="86269-869">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="86269-870">Falsche Zuordnung der Sicherheitsregelmodelle korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-870">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="86269-871">Eigenschaften zur Netzwerkschnittstelle für das Feature für die private IP-Adresse hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-871">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="86269-872">Eigenschaft „PrivateEndpoint“ als Typ „PSResourceId“ zu „PSNetworkInterface“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-872">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="86269-873">Eigenschaft „PrivateLinkConnectionProperties“ als Typ „PSIpConfigurationConnectivityInformation“ zu „PSNetworkInterfaceIPConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-873">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="86269-874">Neue Modellklasse „PSIpConfigurationConnectivityInformation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-874">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="86269-875">Neues ApplicationRuleProtocolType-Element „mssql“ für Azure Firewall-Ressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-875">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="86269-876">Unterstützung von Mehrfachverbindungen in Virtual WAN</span><span class="sxs-lookup"><span data-stu-id="86269-876">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="86269-877">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="86269-877">New cmdlets</span></span>
        - <span data-ttu-id="86269-878">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="86269-878">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="86269-879">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="86269-879">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="86269-880">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="86269-880">Updated cmdlet:</span></span>
        - <span data-ttu-id="86269-881">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="86269-881">New-VpnSite</span></span>
        - <span data-ttu-id="86269-882">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="86269-882">Update-VpnSite</span></span>
        - <span data-ttu-id="86269-883">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="86269-883">New-VpnConnection</span></span>
        - <span data-ttu-id="86269-884">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="86269-884">Update-VpnConnection</span></span>
* <span data-ttu-id="86269-885">Dokumente für einige PowerShell-Beispiele korrigiert, sodass Az-Cmdlets anstelle von AzureRM-Cmdlets verwendet werden</span><span class="sxs-lookup"><span data-stu-id="86269-885">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="86269-886">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="86269-886">Az.RecoveryServices</span></span>
* <span data-ttu-id="86269-887">AzureVMpolicy-Objekt mit ProtectedItemsCount-Attribut aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-887">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="86269-888">Tests für VM-Richtlinie und Wiederherstellung des ursprünglichen Speicherkontos hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-888">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="86269-889">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86269-889">Az.Resources</span></span>
* <span data-ttu-id="86269-890">Fehler behoben, aufgrund dessen „New-AzRoleAssignment“ nicht ohne den Parameter „Scope“ aufgerufen werden konnte</span><span class="sxs-lookup"><span data-stu-id="86269-890">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="86269-891">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="86269-891">Az.ServiceFabric</span></span>
* <span data-ttu-id="86269-892">Tippfehler im Beispiel für die Referenzdokumentation „Update-AzServiceFabricReliability“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-892">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="86269-893">Neue Cmdlets zum Verwalten von Anwendung und Diensten hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="86269-893">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="86269-894">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="86269-894">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="86269-895">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="86269-895">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="86269-896">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="86269-896">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="86269-897">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="86269-897">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="86269-898">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="86269-898">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="86269-899">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="86269-899">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="86269-900">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="86269-900">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="86269-901">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="86269-901">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="86269-902">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="86269-902">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="86269-903">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="86269-903">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="86269-904">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="86269-904">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="86269-905">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="86269-905">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="86269-906">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="86269-906">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="86269-907">Service Fabric SDK auf Version 1.2.0 aktualisiert, die API-Version 2019-03-01 des Service Fabric-Ressourcenanbieters verwendet</span><span class="sxs-lookup"><span data-stu-id="86269-907">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="86269-908">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="86269-908">Az.SignalR</span></span>
* <span data-ttu-id="86269-909">Cmdlets „Update“, „Restart“, „CheckNameAvailability“ und „GetUsage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-909">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="86269-910">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86269-910">Az.Sql</span></span>
* <span data-ttu-id="86269-911">Beispiel in der Referenzdokumentation für „Get-AzSqlElasticPool“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-911">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="86269-912">V-Kern-Beispiel zum Erstellen eines Pools für elastische Datenbanken hinzugefügt (New-AzSqlElasticPool)</span><span class="sxs-lookup"><span data-stu-id="86269-912">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="86269-913">Überprüfung von „EmailAddresses“ sowie Validierung, dass „EmailAdmins“ nicht auf „false“ festgelegt ist, in „Set-AzSqlServerAdvancedThreatProtectionPolicy“ und „Set-AzSqlDatabaseAdvancedThreatProtectionPolicy“ entfernt, wenn „EmailAddresses“ leer ist</span><span class="sxs-lookup"><span data-stu-id="86269-913">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="86269-914">Entfernen der Einstellungen für Server-/Datenbanküberwachung aktiviert, wenn mehrere Diagnoseeinstellungen vorhanden sind, die eine Überwachungskategorie ermöglichen</span><span class="sxs-lookup"><span data-stu-id="86269-914">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="86269-915">Überprüfung von E-Mail-Adressen in mehreren Cmdlets für die SQL-Sicherheitsrisikobewertung korrigiert (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting und Update-AzSqlInstanceVulnerabilityAssessmentSetting)</span><span class="sxs-lookup"><span data-stu-id="86269-915">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="86269-916">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86269-916">Az.Storage</span></span>
* <span data-ttu-id="86269-917">Beispiel in der Referenzdokumentation für „Get-AzStorageAccountKey“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-917">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="86269-918">Beim Upload/Download von Azure-Dateien wird das Beibehalten der SMB-Eigenschaften der Quelldateien (Dateiattribute, Zeitpunkt der Dateierstellung, letzter Schreibzugriff für die Datei) in der Zieldatei unterstützt.</span><span class="sxs-lookup"><span data-stu-id="86269-918">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="86269-919">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="86269-919">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="86269-920">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="86269-920">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="86269-921">Fehler beim Hochladen von Blockblobs mit Eigenschaften/Metadaten für das für einen Container aktivierte ImmutabilityPolicy-Element behoben</span><span class="sxs-lookup"><span data-stu-id="86269-921">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="86269-922">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="86269-922">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="86269-923">Unterstützung für die Verwaltung von Azure-Dateifreigaben mit der API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="86269-923">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="86269-924">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="86269-924">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="86269-925">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="86269-925">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="86269-926">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="86269-926">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="86269-927">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="86269-927">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="86269-928">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="86269-928">Az.Websites</span></span>
* <span data-ttu-id="86269-929">Problem behoben, aufgrund dessen webapp-Tags beim Migrieren der App zu neuem ASP gelöscht wurden</span><span class="sxs-lookup"><span data-stu-id="86269-929">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="86269-930">„Publish-AzureWebapp“ für die Verwendung unter Linux und Windows korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-930">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="86269-931">Beispiel in Referenzdokumentation „Get-AzWebAppPublishingProfile“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-931">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="86269-932">2.6.0: August 2019</span><span class="sxs-lookup"><span data-stu-id="86269-932">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="86269-933">Allgemein</span><span class="sxs-lookup"><span data-stu-id="86269-933">General</span></span>
* <span data-ttu-id="86269-934">Verschiedene Tippfehler in zahlreichen Modulen korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-934">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="86269-935">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86269-935">Az.Accounts</span></span>
* <span data-ttu-id="86269-936">Unterstützung der benutzerseitig zugewiesenen MSI in Azure Functions-Authentifizierung (#9479)</span><span class="sxs-lookup"><span data-stu-id="86269-936">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="86269-937">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="86269-937">Az.Aks</span></span>
* <span data-ttu-id="86269-938">Problem mit der Ausgabe für „Get-AzAks“ behoben</span><span class="sxs-lookup"><span data-stu-id="86269-938">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="86269-939">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="86269-939">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="86269-940">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="86269-940">Az.ApiManagement</span></span>
* <span data-ttu-id="86269-941">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="86269-941">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="86269-942">.NET-NuGet-Version aktualisiert, die keine Einschränkungen für „productId“, „apiId“, „groupId“ und „userId“ erzwingt</span><span class="sxs-lookup"><span data-stu-id="86269-942">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="86269-943">**Get-AzApiManagementProduct:** Unterstützung für das Abfragen von Produkten mithilfe der API hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-943">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="86269-944">**New-AzApiManagementApiRevision:** Problem behoben, aufgrund dessen „ApiRevisionDescription“ beim Erstellen einer neuen API-Revision nicht festgelegt wurde https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="86269-944">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="86269-945">Tippfehler im Modell „PsApiManagementOAuth2AuthrozationServer“ korrigiert: PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="86269-945">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="86269-946">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="86269-946">Az.Batch</span></span>
* <span data-ttu-id="86269-947">Tippfehler in Hilfemeldung und Dokumentation korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="86269-947">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="86269-948">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="86269-948">Az.Cdn</span></span>
* <span data-ttu-id="86269-949">Tippfehler im Hilfsprogramm für die CDN-Modulkonvertierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-949">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86269-950">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86269-950">Az.Compute</span></span>
* <span data-ttu-id="86269-951">VmssId zum Cmdlet „New-AzVMConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-951">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="86269-952">Parameter „TerminateScheduledEvents“ und „TerminateScheduledEventNotBeforeTimeoutInMinutes“ zu „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-952">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="86269-953">HyperVGeneration-Eigenschaft zu VM-Imageobjekt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-953">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="86269-954">Host- und HostGroup-Features hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-954">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="86269-955">Neue Cmdlets:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="86269-955">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="86269-956">Parameter „HostId“ zu „New-AzVMConfig“ und „New-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-956">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="86269-957">Beispiel in der Dokumentation zu „Invoke-AzVMRunCommand“ zur Verwendung des richtigen Parameternamens aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-957">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="86269-958">Beschreibung für „-VolumeType“ in der Referenzdokumentation zu „Set-AzVMDiskEncryptionExtension“ und „Set-AzVmssDiskEncryptionExtension“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-958">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="86269-959">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="86269-959">Az.DataFactory</span></span>
* <span data-ttu-id="86269-960">Tippfehler in der Dokumentation zu „New-AzDataFactoryEncryptValue“ korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="86269-960">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="86269-961">Version des ADF .NET SDK auf 4.1.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-961">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="86269-962">Parameter „DataProxyIntegrationRuntimeName“, „DataProxyStagingLinkedServiceName“ und „DataProxyStagingPath“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um die Einrichtung der selbstgehosteten Integration Runtime als Proxy für die SSIS Integration Runtime zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="86269-962">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="86269-963">„PSTriggerRun“ zum Anzeigen der ausgelösten Pipelines, Meldungen und Eigenschaften und „PSActivityRun“ zum Anzeigen des Aktivitätstyps aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-963">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="86269-964">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="86269-964">Az.DataLakeStore</span></span>
* <span data-ttu-id="86269-965">Hängen von „Get-DataLakeStoreDeletedItem“ aufgrund von Fehlern oder Remoteausnahmen behoben</span><span class="sxs-lookup"><span data-stu-id="86269-965">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="86269-966">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="86269-966">Az.EventHub</span></span>
* <span data-ttu-id="86269-967">Behebung des Problems #9658: Tippfehler im Parameter „VirtualNteworkRule“ in „Set-AzEventHubNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="86269-967">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="86269-968">Behebung des Problems #9558: „Set-AzEventHubNamespace“ verwendet PATCH anstelle von PUT.</span><span class="sxs-lookup"><span data-stu-id="86269-968">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="86269-969">Parameter „EnableKafka“ zum Cmdlet „Set-AzEventHubNamespace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-969">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="86269-970">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="86269-970">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="86269-971">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="86269-971">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="86269-972">Tippfehler („Azure“ in Kleinbuchstaben) in der Dokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-972">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="86269-973">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="86269-973">Az.Monitor</span></span>
* <span data-ttu-id="86269-974">Falscher Parametername in der Hilfedokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-974">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86269-975">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86269-975">Az.Network</span></span>
* <span data-ttu-id="86269-976">„New-AzPrivateLinkServiceIpConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-976">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="86269-977">Parameter „PublicIpAddress“ ausgemustert, da er auf Serverseite nie verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="86269-977">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="86269-978">Optionaler Parameter „Primary“ hinzugefügt, der angibt, ob die aktuelle IP-Konfiguration die primäre ist oder nicht</span><span class="sxs-lookup"><span data-stu-id="86269-978">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="86269-979">Verbesserte Verarbeitung der Anforderungsfehlerausnahme aus dem SDK: Behebt das Problem, dass vorherige SDK-Ausnahmen nicht richtig behandelt wurden, was dazu führt, dass Schlüsselfehlerdetails nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="86269-979">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="86269-980">Validierungslogik für Ipv6-IP-Präfix angepasst, damit auf die richtige IPv6-Präfixlänge geprüft wird</span><span class="sxs-lookup"><span data-stu-id="86269-980">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="86269-981">„Get-AzVirtualNetworkSubnetConfig“ aktualisiert: Parametersatz zum Abrufen nach Subnetzressourcen-ID hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-981">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="86269-982">Aktualisierte Beschreibung des Location-Parameters für „AzNetworkServiceTag“</span><span class="sxs-lookup"><span data-stu-id="86269-982">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="86269-983">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="86269-983">Az.OperationalInsights</span></span>
* <span data-ttu-id="86269-984">Aktualisierte Dokumentation für „New-AzOperationalInsightsLinuxSyslogDataSource“</span><span class="sxs-lookup"><span data-stu-id="86269-984">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="86269-985">Beispiel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-985">Added example</span></span>
    - <span data-ttu-id="86269-986">Beschreibung für den Parameter „-Name“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-986">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="86269-987">Beispiel für „New-AzOperationalInsightsWindowsEventDataSource“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-987">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="86269-988">Beschreibung des Parameters „-Name“ für „New-AzOperationalInsightsWindowsEventDataSource“ geändert</span><span class="sxs-lookup"><span data-stu-id="86269-988">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="86269-989">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="86269-989">Az.RecoveryServices</span></span>
* <span data-ttu-id="86269-990">„Get-AzRecoveryServicesBackupJobDetail.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-990">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="86269-991">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86269-991">Az.Resources</span></span>
* <span data-ttu-id="86269-992">Unterstützung für die neue API-Version 2019-05-10 für Microsoft.Resource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-992">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="86269-993">Unterstützung für „copy.count = 0“ für Variablen, Ressourcen und Eigenschaften hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-993">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="86269-994">Ressourcen mit „condition = false“ oder „copy.count = 0“ werden im vollständigen Modus gelöscht.</span><span class="sxs-lookup"><span data-stu-id="86269-994">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="86269-995">Beispiel zum Hinzufügen einer Richtlinie auf Abonnementebene zur Hilfedokumentation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-995">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="86269-996">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="86269-996">Az.ServiceBus</span></span>
* <span data-ttu-id="86269-997">Behebung des Problems #9658: Tippfehler für Parameter „VirtualNetworkRule“ in „Set-AzServiceBusNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="86269-997">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="86269-998">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="86269-998">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="86269-999">Neuer Befehl „Test-AzServiceBusNameAvailability“ zum Überprüfen der Verfügbarkeit des Namens für Warteschlange und Thema hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-999">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="86269-1000">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="86269-1000">Az.ServiceFabric</span></span>
* <span data-ttu-id="86269-1001">Fehler bei Cmdlets zum Hinzufügen des Knotentyps korrigiert:</span><span class="sxs-lookup"><span data-stu-id="86269-1001">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="86269-1002">Fehler „NullReferenceException“, wenn die Ressourcengruppe andere VMSS enthielt, die nicht mit dem Service Fabric-Cluster in Zusammenhang stehen</span><span class="sxs-lookup"><span data-stu-id="86269-1002">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="86269-1003">Problembehebung: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="86269-1003">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="86269-1004">Fehler behoben, aufgrund dessen bei einem Cmdlet ein Fehler auftrat, wenn sich „virtualNetwork“ in einer anderen Ressourcengruppe befand als der Cluster</span><span class="sxs-lookup"><span data-stu-id="86269-1004">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="86269-1005">Problembehebung: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="86269-1005">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="86269-1006">Cmdlet „Add-AzServiceFabricApplicationCertificate“ ausgemustert</span><span class="sxs-lookup"><span data-stu-id="86269-1006">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="86269-1007">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86269-1007">Az.Sql</span></span>
* <span data-ttu-id="86269-1008">Dokumentation alter Überwachungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1008">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="86269-1009">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86269-1009">Az.Storage</span></span>
* <span data-ttu-id="86269-1010">Hilfe für „Get/Close-AzStorageFileHandle“ aktualisiert (weitere Szenarien zu Cmdlet-Beispielen hinzugefügt und Parameterbeschreibungen aktualisiert)</span><span class="sxs-lookup"><span data-stu-id="86269-1010">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="86269-1011">Unterstützung von „StandardBlobTier“ in Uploadblobs und Kopierblobs</span><span class="sxs-lookup"><span data-stu-id="86269-1011">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="86269-1012">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="86269-1012">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="86269-1013">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="86269-1013">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="86269-1014">Unterstützung der Aktivierungspriorität im Kopierblob</span><span class="sxs-lookup"><span data-stu-id="86269-1014">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="86269-1015">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="86269-1015">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="86269-1016">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="86269-1016">Az.Websites</span></span>
* <span data-ttu-id="86269-1017">Hinzufügen von Erläuterungen zum Parameter „-AppSettings“ in „Set-AzWebApp“ und „Set-AzWebAppSlot“</span><span class="sxs-lookup"><span data-stu-id="86269-1017">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="86269-1018">2.5.0: Juli 2019</span><span class="sxs-lookup"><span data-stu-id="86269-1018">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="86269-1019">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86269-1019">Az.Accounts</span></span>
* <span data-ttu-id="86269-1020">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="86269-1020">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="86269-1021">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="86269-1021">Az.ApplicationInsights</span></span>
* <span data-ttu-id="86269-1022">Tippfehler im Beispiel in der Dokumentation zu „Remove-AzApplicationInsightsApiKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-1022">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="86269-1023">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="86269-1023">Az.Automation</span></span>
* <span data-ttu-id="86269-1024">Tippfehler in der Ressourcenzeichenfolge korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-1024">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="86269-1025">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="86269-1025">Az.CognitiveServices</span></span>
* <span data-ttu-id="86269-1026">Unterstützung für NetworkRuleSet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1026">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86269-1027">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86269-1027">Az.Compute</span></span>
* <span data-ttu-id="86269-1028">Fehlende Eigenschaften (ComputerName, OsName, OsVersion und HyperVGeneration) des Objekts für die VM-Instanzenansicht hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1028">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="86269-1029">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="86269-1029">Az.ContainerRegistry</span></span>
* <span data-ttu-id="86269-1030">Tippfehler in „Remove-AzContainerRegistryReplication“ für den Replikationsparameter korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-1030">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="86269-1031">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="86269-1031">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="86269-1032">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="86269-1032">Az.DataFactory</span></span>
* <span data-ttu-id="86269-1033">Version des ADF .NET SDK auf 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1033">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="86269-1034">Tippfehler in der Dokumentation für „Get-AzDataFactoryV2PipelineRun“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-1034">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="86269-1035">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="86269-1035">Az.EventHub</span></span>
* <span data-ttu-id="86269-1036">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="86269-1036">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="86269-1037">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="86269-1037">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="86269-1038">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="86269-1038">Az.KeyVault</span></span>
* <span data-ttu-id="86269-1039">Unterstützung zum Angeben von KeySize für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1039">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="86269-1040">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="86269-1040">Az.LogicApp</span></span>
* <span data-ttu-id="86269-1041">Korrektur für „Get-AzIntegrationAccountMap“ zum Auflisten aller Zuordnungstypen</span><span class="sxs-lookup"><span data-stu-id="86269-1041">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="86269-1042">Neuer MapType-Parameter für Filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1042">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="86269-1043">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="86269-1043">Az.ManagedServices</span></span>
* <span data-ttu-id="86269-1044">Unterstützung für API-Version 2019-06-01 (GA) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1044">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86269-1045">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86269-1045">Az.Network</span></span>
* <span data-ttu-id="86269-1046">Unterstützung für privaten Endpunkt und privaten Verknüpfungsdienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1046">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="86269-1047">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="86269-1047">New cmdlets</span></span>
        - <span data-ttu-id="86269-1048">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="86269-1048">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="86269-1049">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="86269-1049">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="86269-1050">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="86269-1050">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="86269-1051">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="86269-1051">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="86269-1052">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="86269-1052">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="86269-1053">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="86269-1053">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="86269-1054">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="86269-1054">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="86269-1055">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="86269-1055">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="86269-1056">Folgende Befehle für das Feature aktualisiert: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies für Subnetz in VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="86269-1056">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="86269-1057">„New-AzVirtualNetworkSubnetConfig“, „Set-AzVirtualNetworkSubnetConfig“ und „Add-AzVirtualNetworkSubnetConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1057">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="86269-1058">Optionaler Parameter „-PrivateEndpointNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den privaten Endpunkt in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="86269-1058">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="86269-1059">Optionaler Parameter „-PrivateLinkServiceNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den Privat Link-Dienst in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="86269-1059">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="86269-1060">Der Cmdlet-Parameter „ServiceName“ von AzPrivateLinkService wurde aus Gründen der Abwärtskompatibilität in „Name“ mit dem Alias „ServiceName“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="86269-1060">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="86269-1061">ICMP-Protokoll für Konfigurationen von Netzwerksicherheitsregeln aktiviert</span><span class="sxs-lookup"><span data-stu-id="86269-1061">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="86269-1062">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="86269-1062">Updated cmdlets</span></span>
        - <span data-ttu-id="86269-1063">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="86269-1063">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="86269-1064">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="86269-1064">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="86269-1065">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="86269-1065">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="86269-1066">ConnectionProtocolType (Ikev1/Ikev2) als konfigurierbarer Parameter für „New-AzVirtualNetworkGatewayConnection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1066">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="86269-1067">PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1067">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="86269-1068">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="86269-1068">Updated cmdlet:</span></span>
        - <span data-ttu-id="86269-1069">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="86269-1069">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="86269-1070">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="86269-1070">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="86269-1071">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="86269-1071">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="86269-1072">Application Gateway-Befehl „New-AzApplicationGatewayProbeConfig“ zur Unterstützung des benutzerdefinierten Ports im Test aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1072">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="86269-1073">„New-AzApplicationGatewayProbeConfig“ aktualisiert: Optionaler Parameter „Port“ hinzugefügt, der zum Testen des Back-End-Servers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="86269-1073">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="86269-1074">Dieser Parameter gilt für Standard_V2 und WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="86269-1074">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="86269-1075">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="86269-1075">Az.OperationalInsights</span></span>
* <span data-ttu-id="86269-1076">Standardversion für gespeicherte Suchvorgänge auf 1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1076">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="86269-1077">Verarbeitung des regulären NULL-Ausdrucks in benutzerdefinierten Protokollen korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-1077">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="86269-1078">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="86269-1078">Az.RecoveryServices</span></span>
* <span data-ttu-id="86269-1079">„Get-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1079">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="86269-1080">„Get-AzRecoveryServicesBackupContainer.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1080">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="86269-1081">„Get-AzRecoveryServicesVault.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1081">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="86269-1082">„Wait-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1082">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="86269-1083">„Set-AzRecoveryServicesVaultContext.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1083">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="86269-1084">„Get-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1084">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="86269-1085">„Get-AzRecoveryServicesBackupRecoveryPoint.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1085">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="86269-1086">„Restore-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1086">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="86269-1087">Dienstaufruf zum Aufheben der Containerregistrierung für Azure-Dateifreigabe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1087">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="86269-1088">„Set-AzRecoveryServicesAsrAlertSetting.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1088">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="86269-1089">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86269-1089">Az.Resources</span></span>
- <span data-ttu-id="86269-1090">Fehlendes Cmdlet entfernt, auf das in der Dokumentation zu „New-AzResourceGroupDeployment“ verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="86269-1090">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="86269-1091">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1091">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="86269-1092">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="86269-1092">Az.ServiceBus</span></span>
* <span data-ttu-id="86269-1093">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="86269-1093">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="86269-1094">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="86269-1094">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="86269-1095">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86269-1095">Az.Sql</span></span>
* <span data-ttu-id="86269-1096">Fehlende Beispiele für Cmdlet „Set-AzSqlDatabaseSecondary“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-1096">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="86269-1097">Festlegen wiederkehrender Überprüfungen der Sicherheitsrisikobewertung ohne Angabe von E-Mail-Adressen korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-1097">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="86269-1098">Tippfehler in einer Warnmeldung korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-1098">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="86269-1099">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86269-1099">Az.Storage</span></span>
* <span data-ttu-id="86269-1100">Beispiel in Referenzdokumentation für „Get-AzStorageAccount“ aktualisiert, sodass der richtige Parametername verwendet wird</span><span class="sxs-lookup"><span data-stu-id="86269-1100">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="86269-1101">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="86269-1101">Az.StorageSync</span></span>
* <span data-ttu-id="86269-1102">Cmdlet „Invoke-AzStorageSyncChangeDetection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1102">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="86269-1103">Problem 9551 zur Berücksichtigung von „TierFilesOlderThanDays“ behoben</span><span class="sxs-lookup"><span data-stu-id="86269-1103">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="86269-1104">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="86269-1104">Az.Websites</span></span>
* <span data-ttu-id="86269-1105">Problem behoben, aufgrund dessen einige SiteConfig-Eigenschaften von „Get-AzWebApp“ und „Set-AzWebApp“ nicht zurückgegeben wurden</span><span class="sxs-lookup"><span data-stu-id="86269-1105">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="86269-1106">Neuer Standortparameter zu „Get-AzDeletedWebApp“ und „Restore-AzDeletedWebApp“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1106">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="86269-1107">Fehler beim Klonen von Web-App-Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ behoben</span><span class="sxs-lookup"><span data-stu-id="86269-1107">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="86269-1108">2.4.0 – Juli 2019</span><span class="sxs-lookup"><span data-stu-id="86269-1108">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="86269-1109">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86269-1109">Az.Accounts</span></span>
* <span data-ttu-id="86269-1110">Unterstützung für Profil-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1110">Add support for profile cmdlets</span></span>
* <span data-ttu-id="86269-1111">Unterstützung für Umgebungen und Datenebenen in generierten Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1111">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="86269-1112">Korrektur eines Fehlers, bei dem in einigen Fällen ein falscher Endpunkt für Datenebenen-Cmdlets in Windows PowerShell verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="86269-1112">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="86269-1113">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="86269-1113">Az.Advisor</span></span>
* <span data-ttu-id="86269-1114">Allgemein verfügbares Release von Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="86269-1114">GA release of Az.Advisor</span></span>
* <span data-ttu-id="86269-1115">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="86269-1115">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="86269-1116">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="86269-1116">Az.ApiManagement</span></span>
* <span data-ttu-id="86269-1117">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="86269-1117">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="86269-1118">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="86269-1118">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="86269-1119">Unterstützung für Abfragen von Abonnements nach Benutzer und Produkt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1119">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="86269-1120">Unterstützung für Abfragen anhand des Umfangs hinzugefügt, „/“, „/apis“, „/apis/echo-api“</span><span class="sxs-lookup"><span data-stu-id="86269-1120">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="86269-1121">Behebung von Problem https://github.com/Azure/azure-powershell/issues/9307 und https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="86269-1121">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="86269-1122">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="86269-1122">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="86269-1123">Unterstützung für die Angabe von „ApiVersion“ und „ApiVersionSetId“ beim Importieren von APIs hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1123">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="86269-1124">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="86269-1124">Az.Automation</span></span>
* <span data-ttu-id="86269-1125">Fehler beim Cmdlet „Set-AzAutomationConnectionFieldValue“ für die Verarbeitung des Zeichenfolgewerts behoben</span><span class="sxs-lookup"><span data-stu-id="86269-1125">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86269-1126">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86269-1126">Az.Compute</span></span>
* <span data-ttu-id="86269-1127">Parameter „HyperVGeneration“ zu New-AzImageConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1127">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="86269-1128">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="86269-1128">Az.DataFactory</span></span>
* <span data-ttu-id="86269-1129">Aktualisierung der Ausgabe von ADF-Cmdlets für das Abrufen von Aktivitäts-, Pipeline- und Auslöserausführungen, um die Pipe „Select-Object“ zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="86269-1129">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="86269-1130">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="86269-1130">Az.EventGrid</span></span>
* <span data-ttu-id="86269-1131">Tippfehler in Dokumentation zu 'New-AzEventGridSubscription' behoben</span><span class="sxs-lookup"><span data-stu-id="86269-1131">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="86269-1132">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="86269-1132">Az.IotHub</span></span>
* <span data-ttu-id="86269-1133">Unterstützung für das erneute Generieren von Autorisierungsrichtlinienschlüsseln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1133">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86269-1134">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86269-1134">Az.Network</span></span>
* <span data-ttu-id="86269-1135">„RoutingPreference“ zu öffentlichen IP-Tags hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1135">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="86269-1136">Beispiele für Referenzdokumentation zu „Get-AzNetworkServiceTag“ verbessert</span><span class="sxs-lookup"><span data-stu-id="86269-1136">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="86269-1137">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="86269-1137">Az.PolicyInsights</span></span>
* <span data-ttu-id="86269-1138">Fehlerbehebung für Nullverweis in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="86269-1138">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="86269-1139">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="86269-1139">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="86269-1140">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="86269-1140">Az.OperationalInsights</span></span>
* <span data-ttu-id="86269-1141">Zurückgegebenes CustomLog-Datenquellenmodell in Get-AzOperationalInsightsDataSource korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-1141">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="86269-1142">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="86269-1142">Az.RecoveryServices</span></span>
* <span data-ttu-id="86269-1143">Fehlerbehebung für Befehl „get-policy“ IaaSVMs</span><span class="sxs-lookup"><span data-stu-id="86269-1143">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="86269-1144">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86269-1144">Az.Resources</span></span>
    - <span data-ttu-id="86269-1145">Hilfetext für Parameter „-Top“ von „Get-AzPolicyState“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-1145">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="86269-1146">Clientseitige Unterstützung von Paginierung für „Get-AzPolicyAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1146">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="86269-1147">Neue Parameter für „Set-AzPolicyAssignment“, „-PolicyParameters“ und „-PolicyParametersObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1147">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="86269-1148">Einige Aktualisierungen von Dokumentationen und Beispielen für Policy-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="86269-1148">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="86269-1149">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="86269-1149">Az.ServiceBus</span></span>
* <span data-ttu-id="86269-1150">Korrektur für Problem Nr. 4938: „New-AzureRmServiceBusQueue“ gibt beim Festlegen von „MaxSizeInMegabytes“ „BadRequest“ zurück</span><span class="sxs-lookup"><span data-stu-id="86269-1150">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="86269-1151">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86269-1151">Az.Sql</span></span>
* <span data-ttu-id="86269-1152">Instanzfailovergruppen-Cmdlets aus Vorschauversion in öffentliche Version hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1152">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="86269-1153">Unterstützung von Azure SQL Server\Datenbanküberwachung mit neuen Cmdlets</span><span class="sxs-lookup"><span data-stu-id="86269-1153">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="86269-1154">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="86269-1154">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="86269-1155">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="86269-1155">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="86269-1156">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="86269-1156">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="86269-1157">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="86269-1157">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="86269-1158">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="86269-1158">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="86269-1159">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="86269-1159">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="86269-1160">E-Mail-Einschränkungen aus Einstellungen der Sicherheitsrisikobewertung entfernt</span><span class="sxs-lookup"><span data-stu-id="86269-1160">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="86269-1161">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86269-1161">Az.Storage</span></span>
* <span data-ttu-id="86269-1162">Zwei Parameter („-IndexDocument“ und „-ErrorDocument404Path“) in folgendem Cmdlet von erforderlich in optional geändert:</span><span class="sxs-lookup"><span data-stu-id="86269-1162">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="86269-1163">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="86269-1163">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="86269-1164">Hilfe zu „Get-AzStorageBlobContent“ mit neuem Beispiel ergänzt</span><span class="sxs-lookup"><span data-stu-id="86269-1164">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="86269-1165">Anzeige von mehr Fehlerinformationen beim Fehlschlagen eines Cmdlets mit „StorageException“</span><span class="sxs-lookup"><span data-stu-id="86269-1165">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="86269-1166">Unterstützung für das Erstellen oder Aktualisieren von Speicherkonten mit Azure Files AAD-DS-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="86269-1166">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="86269-1167">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="86269-1167">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="86269-1168">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="86269-1168">Set-AzStorageAccount</span></span>
* <span data-ttu-id="86269-1169">Unterstützung für das Auflisten oder Schließen von Dateihandles einer Dateifreigabe, eines Dateiverzeichnisses oder einer Datei</span><span class="sxs-lookup"><span data-stu-id="86269-1169">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="86269-1170">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="86269-1170">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="86269-1171">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="86269-1171">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="86269-1172">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="86269-1172">Az.StorageSync</span></span>
* <span data-ttu-id="86269-1173">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="86269-1173">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="86269-1174">2.3.2 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="86269-1174">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="86269-1175">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86269-1175">Az.Accounts</span></span>
* <span data-ttu-id="86269-1176">Fehler behoben, aufgrund dessen in manchen Fällen eine falsche URL für Funktionsaufrufe verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="86269-1176">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="86269-1177">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="86269-1177">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="86269-1178">Problem mit Aliasen zwischen AzureRM und Azure-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="86269-1178">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="86269-1179">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="86269-1179">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="86269-1180">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="86269-1180">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86269-1181">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86269-1181">Az.Compute</span></span>
* <span data-ttu-id="86269-1182">Die einfachen Parametersätze „New-AzVm“ und „New-AzVmss“ akzeptieren jetzt den Parameter „ProximityPlacementGroup“.</span><span class="sxs-lookup"><span data-stu-id="86269-1182">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="86269-1183">Tippfehler in der Referenzdokumentation für „New-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="86269-1183">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="86269-1184">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="86269-1184">Az.Dns</span></span>
* <span data-ttu-id="86269-1185">Tippfehler in den Hilfebeispielen zu „Set-AzDnsZone“ behoben</span><span class="sxs-lookup"><span data-stu-id="86269-1185">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="86269-1186">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="86269-1186">Az.EventGrid</span></span>
* <span data-ttu-id="86269-1187">Zur Verwendung der API-Version 2019-06-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1187">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="86269-1188">Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="86269-1188">New cmdlets:</span></span>
    - <span data-ttu-id="86269-1189">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="86269-1189">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="86269-1190">Erstellt eine neue Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="86269-1190">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="86269-1191">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="86269-1191">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="86269-1192">Ruft die Details einer Event Grid-Domäne oder eine Liste aller Event Grid-Domänen im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="86269-1192">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="86269-1193">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="86269-1193">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="86269-1194">Entfernt eine Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="86269-1194">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="86269-1195">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="86269-1195">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="86269-1196">Generiert den freigegebenen Zugriffsschlüssel für eine Azure Event Grid-Domäne erneut.</span><span class="sxs-lookup"><span data-stu-id="86269-1196">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="86269-1197">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="86269-1197">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="86269-1198">Ruft die freigegebenen Zugriffsschlüssel ab, die zum Veröffentlichen von Ereignissen in einer Event Grid-Domäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="86269-1198">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="86269-1199">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="86269-1199">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="86269-1200">Erstellt ein neues Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="86269-1200">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="86269-1201">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="86269-1201">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="86269-1202">Ruft die Details eines Event Grid-Domänenthemas oder eine Liste aller Event Grid-Domänenthemen unter der jeweiligen Event Grid-Domäne im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="86269-1202">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="86269-1203">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="86269-1203">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="86269-1204">Entfernt ein vorhandenes Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="86269-1204">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="86269-1205">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="86269-1205">Updated cmdlets:</span></span>
    - <span data-ttu-id="86269-1206">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="86269-1206">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="86269-1207">Neue erforderliche Parameter zur Unterstützung des Pipings für die neue Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="86269-1207">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="86269-1208">Neue erforderliche Parameter zum Angeben des neuen Event Grid-Domänennamens und/oder Namens des Event Grid-Domänenthemas hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="86269-1208">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="86269-1209">Neue Parametersätze für Domänen und Domänenthemen hinzugefügt, um die Wiederverwendung vorhandener Parameter zuzulassen (‚z. B. „EndPointType“, „SubjectBeginsWith“ usw.)</span><span class="sxs-lookup"><span data-stu-id="86269-1209">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="86269-1210">Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="86269-1210">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="86269-1211">Ablaufdatum des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="86269-1211">Event subscription expiration date,</span></span>
            - <span data-ttu-id="86269-1212">Erweiterte Filterparameter</span><span class="sxs-lookup"><span data-stu-id="86269-1212">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="86269-1213">Neue Enumeration für „servicebusqueue“ als Ziel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1213">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="86269-1214">Verwendung der Option „All“ in „-IncludedEventType“ gesperrt und wie folgt ersetzt</span><span class="sxs-lookup"><span data-stu-id="86269-1214">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="86269-1215">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="86269-1215">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="86269-1216">Neue optionale Parameter („Top“, „ODataQuery“ und „NextLink“) zur Unterstützung der Ergebnispaginierung und -filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1216">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="86269-1217">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="86269-1217">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="86269-1218">Neue erforderliche Parameter zur Unterstützung des Pipings für die Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Entfernen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="86269-1218">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="86269-1219">Neue erforderliche Parameter zum Angeben des Event Grid-Domänennamens und/oder Event Grid-Domänenthemanamens hinzugefügt, um das Entfernen vorhandener Ereignisabonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="86269-1219">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="86269-1220">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="86269-1220">Az.FrontDoor</span></span>
* <span data-ttu-id="86269-1221">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="86269-1221">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="86269-1222">Unterstützung von Transformationen und neuen Wert für den Operator zum automatischen Vervollständigen (RegEx) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1222">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="86269-1223">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="86269-1223">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="86269-1224">Neue Werte für automatisches Vervollständigen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1224">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86269-1225">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86269-1225">Az.Network</span></span>
* <span data-ttu-id="86269-1226">Unterstützung für Virtual Network-Gatewayressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1226">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="86269-1227">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="86269-1227">New cmdlets</span></span>
        - <span data-ttu-id="86269-1228">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="86269-1228">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="86269-1229">AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="86269-1229">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="86269-1230">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="86269-1230">New cmdlets</span></span>
        - <span data-ttu-id="86269-1231">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="86269-1231">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="86269-1232">„PrivatePrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1232">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="86269-1233">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="86269-1233">New cmdlets</span></span>
        - <span data-ttu-id="86269-1234">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="86269-1234">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="86269-1235">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="86269-1235">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="86269-1236">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="86269-1236">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="86269-1237">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="86269-1237">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="86269-1238">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="86269-1238">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="86269-1239">„PrivateEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1239">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="86269-1240">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="86269-1240">New cmdlets</span></span>
        - <span data-ttu-id="86269-1241">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="86269-1241">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="86269-1242">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="86269-1242">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="86269-1243">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="86269-1243">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="86269-1244">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="86269-1244">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="86269-1245">Folgende Befehle für das Feature aktualisiert: UseLocalAzureIpAddress-Flag für „VpnConnection“</span><span class="sxs-lookup"><span data-stu-id="86269-1245">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="86269-1246">„New-AzVpnConnection§ „ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="86269-1246">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="86269-1247">„Set-AzVpnConnection“ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="86269-1247">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="86269-1248">Schreibgeschütztes Feld „PeeredConnections“ beim ExpressRoute-Peering hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1248">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="86269-1249">Schreibgeschütztes Feld „GlobalReachEnabled“ in ExpressRoute hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1249">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="86269-1250">Breaking Change-Attribut hinzugefügt, um auf das veraltete Feld „AllowGlobalReach“ im ExpressRouteCircuit-Modell hinzuweisen</span><span class="sxs-lookup"><span data-stu-id="86269-1250">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="86269-1251">Fehler 8756 bei der Verwendung von „TargetListenerID“ mit AzApplicationGatewayRedirectConfiguration-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="86269-1251">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="86269-1252">Fehler in „New-AzApplicationGatewayPathRuleConfig“ behoben, aufgrund dessen der Regelsatz für erneutes Generieren nicht festgelegt werden konnte</span><span class="sxs-lookup"><span data-stu-id="86269-1252">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="86269-1253">Fehler bei der Anzeige von „VirtualNetworkTaps“ in „NetworkInterfaceIpConfiguration“ behoben</span><span class="sxs-lookup"><span data-stu-id="86269-1253">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="86269-1254">Cortex-Get-Cmdlets zum Auflisten aller Komponenten korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-1254">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="86269-1255">Problem beim Erstellen des festen VirtualHub-Verweises für ExpressRouteGateways behoben (VpnGateway)</span><span class="sxs-lookup"><span data-stu-id="86269-1255">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="86269-1256">Unterstützung für Verfügbarkeitszonen in AzureFirewall und NatGateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1256">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="86269-1257">Cmdlet „Get-AzNetworkServiceTag“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1257">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="86269-1258">Unterstützung für mehrere öffentliche IP-Adressen für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1258">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="86269-1259">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="86269-1259">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="86269-1260">Parameter „-PublicIpAddress“ hinzugefügt, der ein oder mehre öffentliche IP-Adressobjekte akzeptiert</span><span class="sxs-lookup"><span data-stu-id="86269-1260">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="86269-1261">Parameter „- VirtualNetwork“ hinzugefügt, der ein Virtual Network-Objekt akzeptiert</span><span class="sxs-lookup"><span data-stu-id="86269-1261">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="86269-1262">Methoden „AddPublicIpAddress“ und „RemovePublicIpAddress“ für Firewallobjekte hinzugefügt (akzeptieren ein öffentliches IP-Adressobjekt als Eingabe)</span><span class="sxs-lookup"><span data-stu-id="86269-1262">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="86269-1263">Parameter „-PublicIpName“ und „-VirtualNetworkName“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="86269-1263">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="86269-1264">Folgende Befehle für das Feature aktualisiert: VpnClient-AAD-Authentifizierungsoptionen auf die Gatewayressource des virtuellen Netzwerkgateways festgelegt</span><span class="sxs-lookup"><span data-stu-id="86269-1264">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="86269-1265">„New-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1265">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="86269-1266">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-1266">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="86269-1267">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionaler Switch-Parameter „RemoveAadAuthentication“ zum Entfernen von VpnClient-AAD-Authentifizierungsoptionen aus dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1267">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="86269-1268">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="86269-1268">Az.OperationalInsights</span></span>
* <span data-ttu-id="86269-1269">Tarif **pergb2018** im Befehl „New-AzureRmOperationalInsightsWorkspace“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="86269-1269">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="86269-1270">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86269-1270">Az.Resources</span></span>
* <span data-ttu-id="86269-1271">Unterstützung für zusätzliche Optionen zum Exportieren von Vorlagen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1271">Support for additional Template Export options</span></span>
    - <span data-ttu-id="86269-1272">Parameter „-SkipResourceNameParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1272">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="86269-1273">Parameter -SkipAllParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1273">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="86269-1274">Parameter „-Resource“ zu „Export-AzResourceGroup“ hinzugefügt, um das Filtern exportierter Ressourcen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="86269-1274">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="86269-1275">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="86269-1275">Az.ServiceFabric</span></span>
* <span data-ttu-id="86269-1276">Problem beim Hinzufügen des Zertifikats mit „ByExistingKeyVault“ behoben (Abruf des falschen Fingerabdrucks in manchen Fällen)</span><span class="sxs-lookup"><span data-stu-id="86269-1276">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="86269-1277">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86269-1277">Az.Sql</span></span>
* <span data-ttu-id="86269-1278">Suffix des Advanced Threat Protection-Endpunkts korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-1278">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="86269-1279">Durch Advanced Data Security ermöglichte Außerkraftsetzungen der Advanced Threat Protection-Richtlinie korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-1279">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="86269-1280">Neue Cmdlets für „Management.Sql“ ermöglichen Kunden das Hinzufügen von TDE-Schlüsseln und Festlegen der TDE-Schutzvorrichtung für verwaltete Instanzen.</span><span class="sxs-lookup"><span data-stu-id="86269-1280">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="86269-1281">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="86269-1281">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="86269-1282">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="86269-1282">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="86269-1283">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="86269-1283">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="86269-1284">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="86269-1284">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="86269-1285">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="86269-1285">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="86269-1286">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86269-1286">Az.Storage</span></span>
* <span data-ttu-id="86269-1287">Unterstützung von „FileStorage“ und „SkuName Premium_ZRS“ beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="86269-1287">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="86269-1288">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="86269-1288">New-AzStorageAccount</span></span>
* <span data-ttu-id="86269-1289">Überarbeitete Beschreibung des Cmdlets für die Unveränderlichkeit von Blobs</span><span class="sxs-lookup"><span data-stu-id="86269-1289">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="86269-1290">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="86269-1290">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="86269-1291">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="86269-1291">Az.Websites</span></span>
* <span data-ttu-id="86269-1292">Optimiert „Get-AzWebAppCertificate“, um nach der Ressourcengruppe auf dem Server zu filtern (nicht auf dem Client)</span><span class="sxs-lookup"><span data-stu-id="86269-1292">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="86269-1293">Switch-Parameter „-UseDisasterRecovery“ für „Get-AzWebAppSnapshot“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1293">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="86269-1294">2.2.0 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="86269-1294">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="86269-1295">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="86269-1295">Az.Cdn</span></span>
* <span data-ttu-id="86269-1296">Es wurden Cmdlets aktualisiert, um das rulesEngine-Feature basierend auf der API-Version 2019-04-15 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="86269-1296">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86269-1297">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86269-1297">Az.Compute</span></span>
* <span data-ttu-id="86269-1298">Der Parameter `NoWait` wurde hinzugefügt, der den Vorgang startet und sofort zurückkehrt, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="86269-1298">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="86269-1299">Aktualisierte Cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="86269-1299">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="86269-1300">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="86269-1300">Az.EventHub</span></span>
* <span data-ttu-id="86269-1301">Fehlerbehebung für #9231 – Get-AzEventHubNamespace gibt keine Tags zurück</span><span class="sxs-lookup"><span data-stu-id="86269-1301">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="86269-1302">Fehlerbehebung für #9230 – Get-AzEventHubNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="86269-1302">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86269-1303">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86269-1303">Az.Network</span></span>
* <span data-ttu-id="86269-1304">ResourceId und InputObject wurden für NAT Gateway aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1304">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="86269-1305">Es wurde ein Alias für ResourceId und InputObjectr hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1305">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="86269-1306">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="86269-1306">Az.PolicyInsights</span></span>
* <span data-ttu-id="86269-1307">Fehlerbehebung für Nullverweis in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="86269-1307">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="86269-1308">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="86269-1308">Az.RecoveryServices</span></span>
* <span data-ttu-id="86269-1309">Minimale Aufbewahrung in Tagen für IaaSVM-Richtlinie wurde von 1 in 7 geändert</span><span class="sxs-lookup"><span data-stu-id="86269-1309">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="86269-1310">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="86269-1310">Az.ServiceBus</span></span>
* <span data-ttu-id="86269-1311">Fehlerbehebung für #9182 – Get-AzServiceBusNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="86269-1311">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="86269-1312">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="86269-1312">Az.ServiceFabric</span></span>
* <span data-ttu-id="86269-1313">Tippfehler in Fehlermeldung für Update-AzServiceFabricReliability wurde behoben</span><span class="sxs-lookup"><span data-stu-id="86269-1313">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="86269-1314">Fehlendes Zeichen in Service Fabric-Befehlszeilen wurde behoben</span><span class="sxs-lookup"><span data-stu-id="86269-1314">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="86269-1315">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86269-1315">Az.Sql</span></span>
* <span data-ttu-id="86269-1316">Der DnsZonePartner-Parameter für das Cmdlet New-AzureSqlInstance wurde hinzugefügt, um AutoDr für verwaltete Instanzen zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="86269-1316">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="86269-1317">Das Cmdlet Get-AzSqlDatabaseSecureConnectionPolicy wird eingestellt</span><span class="sxs-lookup"><span data-stu-id="86269-1317">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="86269-1318">Cmdlets zum Schutz vor Bedrohungen werden in „Advanced Threat Protection“ (Erweiterter Schutz vor Bedrohungen) umbenannt</span><span class="sxs-lookup"><span data-stu-id="86269-1318">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="86269-1319">New-AzSqlInstance – Die Parameter StorageSizeInGB und LicenseType sind jetzt optional</span><span class="sxs-lookup"><span data-stu-id="86269-1319">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="86269-1320">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="86269-1320">Az.Websites</span></span>
* <span data-ttu-id="86269-1321">Das Problem, bei dem die Verwendung von Set-AzWebApp und Set-AzWebAppSlot mit der -WebApp-Eigenschaft die Tags entfernt hat, wurde behoben</span><span class="sxs-lookup"><span data-stu-id="86269-1321">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="86269-1322">2.1.0 – Mai 2019</span><span class="sxs-lookup"><span data-stu-id="86269-1322">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="86269-1323">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="86269-1323">Az.ApiManagement</span></span>
* <span data-ttu-id="86269-1324">Es wurden neue Cmdlets zum Verwalten der Diagnose im globalen sowie im API-Bereich erstellt</span><span class="sxs-lookup"><span data-stu-id="86269-1324">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="86269-1325">**Get-AzApiManagementDiagnostic**: Abrufen der Diagnose, die im globalen oder im API-Bereich konfiguriert wurde</span><span class="sxs-lookup"><span data-stu-id="86269-1325">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="86269-1326">**New-AzApiManagementDiagnostic**: Erstellen neuer Diagnosen im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="86269-1326">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="86269-1327">**New-AzApiManagementHttpMessageDiagnostic**: Erstellen einer Diagnoseeinstellung für die zu protokollierenden Kopfzeilen und für die Größe der Bytes für den Text</span><span class="sxs-lookup"><span data-stu-id="86269-1327">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="86269-1328">**New-AzApiManagementPipelineDiagnosticSetting**: Erstellen von Diagnoseeinstellungen für ein-/ausgehende HTTP-Nachrichten für das Gateway</span><span class="sxs-lookup"><span data-stu-id="86269-1328">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="86269-1329">**New-AzApiManagementSamplingSetting**: Erstellen der Einstellung „Sampling“ für die Anforderungen/Antworten für eine Diagnose</span><span class="sxs-lookup"><span data-stu-id="86269-1329">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="86269-1330">**Remove-AzApiManagementDiagnostic**: Entfernen einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="86269-1330">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="86269-1331">**Set-AzApiManagementDiagnostic**: Aktualisieren einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="86269-1331">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="86269-1332">Es wurden neue Cmdlets für die Cacheverwaltung im ApiManagement-Dienst erstellt</span><span class="sxs-lookup"><span data-stu-id="86269-1332">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="86269-1333">**Get-AzApiManagementCache**: Abrufen der Details des durch den Bezeichner angegebenen Caches oder aller Caches</span><span class="sxs-lookup"><span data-stu-id="86269-1333">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="86269-1334">**New-AzApiManagementCache**: Erstellen eines neuen „standardmäßigen“ Caches oder eines Caches in einer bestimmten „Region“ von Azure</span><span class="sxs-lookup"><span data-stu-id="86269-1334">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="86269-1335">**Remove-AzApiManagementCache**: Entfernen eines Caches</span><span class="sxs-lookup"><span data-stu-id="86269-1335">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="86269-1336">**Update-AzApiManagementCache**: Aktualisieren eines Caches</span><span class="sxs-lookup"><span data-stu-id="86269-1336">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="86269-1337">Es wurden neue Cmdlets zur Verwaltung von API-Schemas erstellt</span><span class="sxs-lookup"><span data-stu-id="86269-1337">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="86269-1338">**New-AzApiManagementSchema**: Erstellen eines neuen Schemas für eine API</span><span class="sxs-lookup"><span data-stu-id="86269-1338">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="86269-1339">**Get-AzApiManagementSchema**: Abrufen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="86269-1339">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="86269-1340">**Remove-AzApiManagementSchema**: Entfernen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="86269-1340">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="86269-1341">**Set-AzApiManagementSchema**: Aktualisieren des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="86269-1341">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="86269-1342">Es wurde ein neues Cmdlet zum Generieren eines Benutzertokens erstellt</span><span class="sxs-lookup"><span data-stu-id="86269-1342">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="86269-1343">**New-AzApiManagementUserToken**: Generieren eines neuen Benutzertokens, das standardmäßig für acht Stunden gültig ist. Mit diesem Cmdlet kann das Token für den „GIT“-Benutzer generiert werden./</span><span class="sxs-lookup"><span data-stu-id="86269-1343">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="86269-1344">Es wurde ein neues Cmdlet zum Abrufen des Netzwerkstatus erstellt</span><span class="sxs-lookup"><span data-stu-id="86269-1344">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="86269-1345">**Get-AzApiManagementNetworkStatus**: Abrufen der Netzwerkstatuskonnektivität von Ressourcen, von denen der API Management-Dienst abhängig ist</span><span class="sxs-lookup"><span data-stu-id="86269-1345">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="86269-1346">Dies ist hilfreich, wenn Sie den ApiManagement-Dienst in einem virtuellen Netzwerk bereitstellen und überprüfen, ob eine der Abhängigkeiten fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="86269-1346">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="86269-1347">Das Cmdlet **New-AzApiManagement** wurde zum Verwalten des ApiManagement-Diensts aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1347">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="86269-1348">Die Unterstützung für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1348">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="86269-1349">Die Unterstützung zum Aktivieren des Flags „EnableClientCertificate“ für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1349">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="86269-1350">Das neue Cmdlet **New-AzApiManagementSslSetting** ermöglicht die Konfiguration der „TLS/SSL“-Einstellung für „Back-End“ und „Front-End“</span><span class="sxs-lookup"><span data-stu-id="86269-1350">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="86269-1351">Dies kann auch dazu verwendet werden, um „Verschlüsselungen“ wie „3DES“ und „ServerProtokolle“ wie „Http2“ für das „Front-End“ eines ApiManagement-Diensts zu konfigurieren</span><span class="sxs-lookup"><span data-stu-id="86269-1351">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="86269-1352">Die Unterstützung für die Konfiguration des Hostnamens „DeveloperPortal“ wurde zum ApiManagement-Dienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1352">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="86269-1353">Die **Get-AzApiManagementSsoToken**-Cmdlets wurden aktualisiert, um das Objekt „PsApiManagement“ als Eingabe zu übernehmen</span><span class="sxs-lookup"><span data-stu-id="86269-1353">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="86269-1354">Das Cmdlet wurde aktualisiert, um Fehlermeldungen inline anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="86269-1354">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="86269-1355">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Fehlercode: ValidationError-Fehlermeldung: Mindestens ein Feld enthält ungültige Werte: Fehlerdetails: [Code=ValidationError, Message=Fehler in Element 'log-to-eventhub' in Zeile 3, Spalte 10: Protokollierungstool nicht gefunden, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="86269-1355">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="86269-1356">Cmdlet **Export-AzApiManagementApi** wurde für den Export von APIs im Format „OpenApi 3.0“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1356">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="86269-1357">Cmdlet **Import-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1357">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="86269-1358">Zum Importieren der API aus der „OpenApi 3.0“-Dokumentspezifikation</span><span class="sxs-lookup"><span data-stu-id="86269-1358">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="86269-1359">Zur Außerkraftsetzung der „PsApiManagementSchema“-Eigenschaft, die in einem beliebigen Dokument („Swagger“, „Wadl“, „Wsdl“, „OpenApi“) angegeben ist</span><span class="sxs-lookup"><span data-stu-id="86269-1359">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="86269-1360">Zur Außerkraftsetzung der „ServiceUrl“-Eigenschaft, die in einem beliebigen Dokument angegeben ist</span><span class="sxs-lookup"><span data-stu-id="86269-1360">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="86269-1361">Cmdlet **Get-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="86269-1361">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="86269-1362">Cmdlet **Set-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ und im Format mit XML-Escapezeichen mit „xml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="86269-1362">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="86269-1363">Cmdlet **New-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1363">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="86269-1364">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="86269-1364">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="86269-1365">Zum Erstellen einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="86269-1365">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="86269-1366">Zum Klonen einer API mithilfe von „SourceApiId“ und „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="86269-1366">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="86269-1367">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="86269-1367">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="86269-1368">Cmdlet **Set-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1368">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="86269-1369">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="86269-1369">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="86269-1370">Zum Aktualisieren einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="86269-1370">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="86269-1371">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="86269-1371">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="86269-1372">Cmdlet **New-AzApiManagementRevision** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1372">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="86269-1373">Zum Klonen (Kopiertags, Produkte, Vorgänge und Richtlinien) einer vorhandenen Version mithilfe von „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="86269-1373">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="86269-1374">Die neue Version übernimmt die „ApiId“ des übergeordneten Elements</span><span class="sxs-lookup"><span data-stu-id="86269-1374">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="86269-1375">Zum Bereitstellen einer „ApiRevisionDescription“</span><span class="sxs-lookup"><span data-stu-id="86269-1375">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="86269-1376">Zur Außerkraftsetzung der „ServiceUrl“ beim Klonen einer API</span><span class="sxs-lookup"><span data-stu-id="86269-1376">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="86269-1377">Cmdlet **New-AzApiManagementIdentityProvider** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1377">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="86269-1378">Zum Konfigurieren von „AAD“ oder „AADB2C“ mit einer „Authority“</span><span class="sxs-lookup"><span data-stu-id="86269-1378">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="86269-1379">Zum Einrichten von „SignupPolicy“, „SigninPolicy“, „ProfileEditingPolicy“ und „PasswordResetPolicy“</span><span class="sxs-lookup"><span data-stu-id="86269-1379">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="86269-1380">Cmdlet **New-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1380">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="86269-1381">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="86269-1381">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="86269-1382">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="86269-1382">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="86269-1383">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1383">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="86269-1384">Cmdlet **Set-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1384">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="86269-1385">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="86269-1385">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="86269-1386">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="86269-1386">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="86269-1387">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1387">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="86269-1388">Folgende Cmdlets wurden aktualisiert, um „ResourceId“ als Eingabe zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="86269-1388">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="86269-1389">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="86269-1389">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="86269-1390">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="86269-1390">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="86269-1391">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="86269-1391">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="86269-1392">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="86269-1392">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="86269-1393">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="86269-1393">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="86269-1394">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="86269-1394">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="86269-1395">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="86269-1395">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="86269-1396">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="86269-1396">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="86269-1397">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="86269-1397">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="86269-1398">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="86269-1398">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="86269-1399">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="86269-1399">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="86269-1400">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="86269-1400">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="86269-1401">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="86269-1401">Az.Automation</span></span>
* <span data-ttu-id="86269-1402">Get-AzAutomationJobOutputRecord wurde aktualisiert, um JSON- und Textdatensatzwerte zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="86269-1402">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="86269-1403">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="86269-1403">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="86269-1404">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="86269-1404">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="86269-1405">Das Verhalten von Start-AzAutomationDscCompilationJob wurde geändert, um den Auftrag einfach zu starten, anstatt auf dessen Abschluss zu warten</span><span class="sxs-lookup"><span data-stu-id="86269-1405">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="86269-1406">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="86269-1406">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="86269-1407">Fehlerbehebung für Get-AzAutomationDscNode, wenn die Verwendung von „-Name“ alle Knoten zurückgibt</span><span class="sxs-lookup"><span data-stu-id="86269-1407">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="86269-1408">Jetzt wird nur der übereinstimmende Knoten zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="86269-1408">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86269-1409">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86269-1409">Az.Compute</span></span>
* <span data-ttu-id="86269-1410">Parameter „ProtectFromScaleIn“ und „ProtectFromScaleSetAction“ wurden zum Cmdlet „Update-AzVmssVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1410">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="86269-1411">Der jetzt festgelegte wimple-Parameter „New-AzVM“ verwendet standardmäßig einen verfügbaren Standort, wenn „East US“ (USA, Osten) nicht unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="86269-1411">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="86269-1412">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="86269-1412">Az.DataLakeStore</span></span>
* <span data-ttu-id="86269-1413">Das ADLS-SDK wurde aktualisiert, um „HttpClient“ zu verwenden und Datenebenentests wurden mit dem Azure-Framework integriert</span><span class="sxs-lookup"><span data-stu-id="86269-1413">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="86269-1414">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="86269-1414">Az.Monitor</span></span>
* <span data-ttu-id="86269-1415">Fehlerbehebung bei falschen Parameternamen in Hilfebeispielen</span><span class="sxs-lookup"><span data-stu-id="86269-1415">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86269-1416">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86269-1416">Az.Network</span></span>
* <span data-ttu-id="86269-1417">DisableBgpRoutePropagation-Flag wurde zur Ausgabe der effektiven Routentabelle hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1417">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="86269-1418">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="86269-1418">Updated cmdlet:</span></span>
        - <span data-ttu-id="86269-1419">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="86269-1419">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="86269-1420">Fehlerbehebung von doppeltem Bindestrich in Dokumentation von New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="86269-1420">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="86269-1421">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86269-1421">Az.Resources</span></span>
* <span data-ttu-id="86269-1422">Neues Cmdlet „Get-AzureRmDenyAssignment“ zum Abrufen von Ablehnungszuweisungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1422">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="86269-1423">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86269-1423">Az.Sql</span></span>
* <span data-ttu-id="86269-1424">„Advanced Threat Protection“-Cmdlets in „Advanced Data Security“ umbenennen und Sicherheitsrisikobewertung standardmäßig aktivieren</span><span class="sxs-lookup"><span data-stu-id="86269-1424">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="86269-1425">2.0.0: Mai 2019</span><span class="sxs-lookup"><span data-stu-id="86269-1425">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="86269-1426">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86269-1426">Az.Accounts</span></span>
* <span data-ttu-id="86269-1427">Authentifizierungsbibliothek aktualisiert, um ADFS-Probleme mit der Authentifizierung per Benutzername/Kennwort zu beheben</span><span class="sxs-lookup"><span data-stu-id="86269-1427">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="86269-1428">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="86269-1428">Az.CognitiveServices</span></span>
* <span data-ttu-id="86269-1429">Ausschließliche Anzeige des Bing-Haftungsausschlusses für Bing-Suchdienste</span><span class="sxs-lookup"><span data-stu-id="86269-1429">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="86269-1430">Fehler behoben, der zu einem Fehler bei der Kontoerstellung führte</span><span class="sxs-lookup"><span data-stu-id="86269-1430">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86269-1431">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86269-1431">Az.Compute</span></span>
* <span data-ttu-id="86269-1432">Feature für die Näherungsplatzierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="86269-1432">Proximity placement group feature.</span></span>
    - <span data-ttu-id="86269-1433">Die folgenden neuen Cmdlets wurden hinzugefügt:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="86269-1433">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="86269-1434">Der neue Parameter „ProximityPlacementGroupId“ wurde zu den folgenden Cmdlets hinzugefügt:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="86269-1434">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="86269-1435">Der Parameter „StorageAccountType“ wurde zu „New-AzGalleryImageVersion“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-1435">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="86269-1436">„TargetRegion“ von „New-AzGalleryImageVersion“ kann „StorageAccountType“ enthalten.</span><span class="sxs-lookup"><span data-stu-id="86269-1436">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="86269-1437">Switch-Parameter „SkipShutdown“ wurde zu „Stop-AzVM“ und „Stop-AzVmss“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-1437">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="86269-1438">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="86269-1438">Breaking changes</span></span>
    - <span data-ttu-id="86269-1439">„Set-AzVMBootDiagnostics“ in „Set-AzVMBootDiagnostic“ geändert</span><span class="sxs-lookup"><span data-stu-id="86269-1439">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="86269-1440">„Export-AzLogAnalyticThrottledRequests“ in „Export-AzLogAnalyticThrottledRequests“ geändert</span><span class="sxs-lookup"><span data-stu-id="86269-1440">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="86269-1441">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="86269-1441">Az.DeploymentManager</span></span>
* <span data-ttu-id="86269-1442">Erste allgemein verfügbare Version der Azure-Bereitstellungs-Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="86269-1442">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="86269-1443">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="86269-1443">Az.Dns</span></span>
* <span data-ttu-id="86269-1444">Automatische Delegierung des DNS-Namenservers</span><span class="sxs-lookup"><span data-stu-id="86269-1444">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="86269-1445">Das Cmdlet zum Erstellen einer DNS-Zone akzeptiert den übergeordneten Zonennamen als zusätzlichen optionalen Parameter.</span><span class="sxs-lookup"><span data-stu-id="86269-1445">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="86269-1446">NS-Einträge in der übergeordneten Zone für neu erstellte untergeordnete Zone hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1446">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="86269-1447">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="86269-1447">Az.FrontDoor</span></span>
* <span data-ttu-id="86269-1448">Erste allgemein verfügbare Version der Azure Frontdoor-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="86269-1448">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="86269-1449">WAF-Cmdlets so umbenannt, dass sie „Waf“ enthalten</span><span class="sxs-lookup"><span data-stu-id="86269-1449">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="86269-1450">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="86269-1450">Az.HDInsight</span></span>
* <span data-ttu-id="86269-1451">Zwei Cmdlets entfernt:</span><span class="sxs-lookup"><span data-stu-id="86269-1451">Removed two cmdlets:</span></span>
    - <span data-ttu-id="86269-1452">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="86269-1452">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="86269-1453">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="86269-1453">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="86269-1454">Neues Cmdlet „Set-AzHDInsightGatewayCredential“ hinzugefügt, um „Grant-AzHDInsightHttpServicesAccess“ zu ersetzen</span><span class="sxs-lookup"><span data-stu-id="86269-1454">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="86269-1455">Cmdlet „Get-AzHDInsightJobOutput“ aktualisiert, um zwischen Leserrolle und HDInsight-Bedienerrolle zu unterscheiden:</span><span class="sxs-lookup"><span data-stu-id="86269-1455">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="86269-1456">Benutzer mit der Rolle „Leser“ müssen den Parameter „DefaultStorageAccountKey“ explizit angeben, andernfalls treten Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="86269-1456">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="86269-1457">Benutzer mit der Rolle des HDInsight-Bedieners sind nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="86269-1457">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="86269-1458">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="86269-1458">Az.Monitor</span></span>
* <span data-ttu-id="86269-1459">Neue Cmdlets für SQR-API (Scheduled Query Rule, geplante Abfrageregel)</span><span class="sxs-lookup"><span data-stu-id="86269-1459">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="86269-1460">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="86269-1460">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="86269-1461">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="86269-1461">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="86269-1462">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="86269-1462">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="86269-1463">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="86269-1463">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="86269-1464">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="86269-1464">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="86269-1465">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="86269-1465">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="86269-1466">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="86269-1466">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="86269-1467">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="86269-1467">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="86269-1468">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="86269-1468">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="86269-1469">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="86269-1469">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="86269-1470">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="86269-1470">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="86269-1471">[Weitere Informationen](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) zur SQR-API</span><span class="sxs-lookup"><span data-stu-id="86269-1471">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="86269-1472">„Az.Monitor.md“ aktualisiert, um Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch) einzuschließen</span><span class="sxs-lookup"><span data-stu-id="86269-1472">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86269-1473">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86269-1473">Az.Network</span></span>
* <span data-ttu-id="86269-1474">Unterstützung für NAT-Gatewayressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1474">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="86269-1475">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="86269-1475">New cmdlets</span></span>
        - <span data-ttu-id="86269-1476">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="86269-1476">New-AzNatGateway</span></span>
        - <span data-ttu-id="86269-1477">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="86269-1477">Get-AzNatGateway</span></span>
        - <span data-ttu-id="86269-1478">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="86269-1478">Set-AzNatGateway</span></span>
        - <span data-ttu-id="86269-1479">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="86269-1479">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="86269-1480">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="86269-1480">Updated cmdlets</span></span>
        - <span data-ttu-id="86269-1481">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="86269-1481">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="86269-1482">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="86269-1482">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="86269-1483">Folgende Befehle für das Feature aktualisiert: Benutzerdefinierte Routen für Brooklyn-Gateway festgelegt/entfernt</span><span class="sxs-lookup"><span data-stu-id="86269-1483">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="86269-1484">„New-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="86269-1484">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="86269-1485">„Set-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="86269-1485">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="86269-1486">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="86269-1486">Az.PolicyInsights</span></span>
* <span data-ttu-id="86269-1487">Unterstützung für die Abfrage von Richtlinienauswertungsdetails</span><span class="sxs-lookup"><span data-stu-id="86269-1487">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="86269-1488">Parameter „-Expand“ zu „Get-AzPolicyState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1488">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="86269-1489">Unterstützung für „-Expand PolicyEvaluationDetails“</span><span class="sxs-lookup"><span data-stu-id="86269-1489">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="86269-1490">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="86269-1490">Az.RecoveryServices</span></span>
* <span data-ttu-id="86269-1491">Unterstützung für abonnementübergreifende Azure-zu-Azure-Sitewiederherstellung</span><span class="sxs-lookup"><span data-stu-id="86269-1491">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="86269-1492">Markierung anstehender wichtiger Änderungen für Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="86269-1492">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="86269-1493">Fehlerbehebung für Azure Site Recovery-Wiederherstellungsplan und -Aktionsplan</span><span class="sxs-lookup"><span data-stu-id="86269-1493">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="86269-1494">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Netzwerkzuordnung für Azure zu Azure</span><span class="sxs-lookup"><span data-stu-id="86269-1494">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="86269-1495">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Schutzrichtung für Azure zu Azure für verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="86269-1495">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="86269-1496">Weitere kleinere Korrekturen</span><span class="sxs-lookup"><span data-stu-id="86269-1496">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="86269-1497">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="86269-1497">Az.Relay</span></span>
* <span data-ttu-id="86269-1498">Korrektur von Tippfehlern in Kundennachrichten</span><span class="sxs-lookup"><span data-stu-id="86269-1498">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="86269-1499">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="86269-1499">Az.ServiceBus</span></span>
* <span data-ttu-id="86269-1500">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1500">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="86269-1501">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86269-1501">Az.Storage</span></span>
* <span data-ttu-id="86269-1502">Upgrade auf Speicherclientbibliothek 10.0.1 (Namespace aller Objekte von diesem SDK von „Microsoft.WindowsAzure.Storage. *“ in „Microsoft.Azure.Storage.* “ geändert)</span><span class="sxs-lookup"><span data-stu-id="86269-1502">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="86269-1503">Upgrade auf Microsoft.Azure.Management.Storage 11.0.0, um die neue API-Version 2019-04-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="86269-1503">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="86269-1504">Art des Standardspeicherkontos bei der Speicherkontoerstellung von „Storage“ in „StorageV2“ geändert</span><span class="sxs-lookup"><span data-stu-id="86269-1504">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="86269-1505">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="86269-1505">New-AzStorageAccount</span></span>
* <span data-ttu-id="86269-1506">Vom Speicherkonto-Cmdlet ausgegebener SKU-Name (Sku.Name) durch Hinzufügen eines Unterstrichs an SKU-Eingabename angepasst (Beispiel: „StandardLRS“ > „Standard_LRS“).</span><span class="sxs-lookup"><span data-stu-id="86269-1506">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="86269-1507">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="86269-1507">New-AzStorageAccount</span></span>
    - <span data-ttu-id="86269-1508">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="86269-1508">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="86269-1509">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="86269-1509">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="86269-1510">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="86269-1510">Az.Websites</span></span>
* <span data-ttu-id="86269-1511">Die Eigenschaft „Kind“ wird nun für PSSite-Objekte festgelegt, die von „Get-AzWebApp“ zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="86269-1511">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="86269-1512">„Get-AzWebApp\*Metrics“ und „Get-AzAppServicePlanMetrics“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="86269-1512">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="86269-1513">1.8.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="86269-1513">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="86269-1514">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="86269-1514">Highlights since the last major release</span></span>
* <span data-ttu-id="86269-1515">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="86269-1515">General availability of `Az` module</span></span>
* <span data-ttu-id="86269-1516">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="86269-1516">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="86269-1517">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="86269-1517">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="86269-1518">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1518">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="86269-1519">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1519">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="86269-1520">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1520">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="86269-1521">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="86269-1521">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="86269-1522">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86269-1522">Az.Accounts</span></span>
* <span data-ttu-id="86269-1523">„Uninstall-AzureRm“ aktualisiert, um Module unter Mac ordnungsgemäß zu löschen</span><span class="sxs-lookup"><span data-stu-id="86269-1523">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="86269-1524">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="86269-1524">Az.Batch</span></span>
* <span data-ttu-id="86269-1525">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="86269-1525">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="86269-1526">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="86269-1526">Az.Cdn</span></span>
* <span data-ttu-id="86269-1527">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="86269-1527">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="86269-1528">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="86269-1528">Az.CognitiveServices</span></span>
* <span data-ttu-id="86269-1529">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="86269-1529">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86269-1530">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86269-1530">Az.Compute</span></span>
* <span data-ttu-id="86269-1531">Problem mit der AEM-Installation behoben, wenn die Ressourcen-IDs von Datenträgern Ressourcengruppen in Kleinbuchstaben enthielten</span><span class="sxs-lookup"><span data-stu-id="86269-1531">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="86269-1532">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="86269-1532">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="86269-1533">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-1533">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="86269-1534">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="86269-1534">Az.DataFactory</span></span>
* <span data-ttu-id="86269-1535">„SsisProperties“ hinzugefügt, falls „NodeCount“ für verwaltete Integration Runtime nicht NULL ist</span><span class="sxs-lookup"><span data-stu-id="86269-1535">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="86269-1536">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="86269-1536">Az.DataLakeStore</span></span>
* <span data-ttu-id="86269-1537">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="86269-1537">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="86269-1538">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="86269-1538">Az.EventGrid</span></span>
* <span data-ttu-id="86269-1539">Hilfetext für Endpunkt aktualisiert, um anzugeben, dass Ressourcen erstellt werden müssen, bevor die Cmdlets zum Erstellen/Aktualisieren von Ereignisabonnements verwendet werden</span><span class="sxs-lookup"><span data-stu-id="86269-1539">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="86269-1540">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="86269-1540">Az.EventHub</span></span>
* <span data-ttu-id="86269-1541">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1541">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="86269-1542">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="86269-1542">Az.HDInsight</span></span>
* <span data-ttu-id="86269-1543">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="86269-1543">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="86269-1544">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="86269-1544">Az.IotHub</span></span>
* <span data-ttu-id="86269-1545">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="86269-1545">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="86269-1546">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="86269-1546">Az.KeyVault</span></span>
* <span data-ttu-id="86269-1547">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="86269-1547">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="86269-1548">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-1548">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="86269-1549">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="86269-1549">Az.MachineLearning</span></span>
* <span data-ttu-id="86269-1550">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="86269-1550">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="86269-1551">Az.Media</span><span class="sxs-lookup"><span data-stu-id="86269-1551">Az.Media</span></span>
* <span data-ttu-id="86269-1552">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="86269-1552">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="86269-1553">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="86269-1553">Az.Monitor</span></span>
  * <span data-ttu-id="86269-1554">Neue Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch)</span><span class="sxs-lookup"><span data-stu-id="86269-1554">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="86269-1555">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="86269-1555">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="86269-1556">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="86269-1556">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="86269-1557">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="86269-1557">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="86269-1558">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="86269-1558">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="86269-1559">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="86269-1559">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="86269-1560">Monitor SDK auf Version 0.22.0-preview aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1560">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86269-1561">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86269-1561">Az.Network</span></span>
* <span data-ttu-id="86269-1562">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="86269-1562">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="86269-1563">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-1563">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="86269-1564">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="86269-1564">Az.NotificationHubs</span></span>
* <span data-ttu-id="86269-1565">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="86269-1565">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="86269-1566">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="86269-1566">Az.OperationalInsights</span></span>
* <span data-ttu-id="86269-1567">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="86269-1567">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="86269-1568">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="86269-1568">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="86269-1569">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="86269-1569">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="86269-1570">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="86269-1570">Az.RecoveryServices</span></span>
* <span data-ttu-id="86269-1571">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="86269-1571">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="86269-1572">Tabellenformat für SQL auf Azure-VM aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1572">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="86269-1573">Alternative Methode zum Abrufen des Speicherorts in „AzureFileShare“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1573">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="86269-1574">„ScheduleRunDays“ in SchedulePolicy-Objekt gemäß Zeitzone aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1574">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="86269-1575">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="86269-1575">Az.RedisCache</span></span>
* <span data-ttu-id="86269-1576">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="86269-1576">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="86269-1577">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86269-1577">Az.Resources</span></span>
* <span data-ttu-id="86269-1578">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-1578">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="86269-1579">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86269-1579">Az.Sql</span></span>
* <span data-ttu-id="86269-1580">Abhängigkeit vom Monitor SDK durch allgemeinen Code ersetzt</span><span class="sxs-lookup"><span data-stu-id="86269-1580">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="86269-1581">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="86269-1581">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="86269-1582">Verbesserter Prozess für Klassifizierung mehrerer Spalten</span><span class="sxs-lookup"><span data-stu-id="86269-1582">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="86269-1583">SKU-Eigenschaften (SKU-Name, Familie, Kapazität) in Antwort von „Get-AzSqlServerServiceObjective“ aufgenommen und standardmäßig als Tabelle formatiert</span><span class="sxs-lookup"><span data-stu-id="86269-1583">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="86269-1584">Möglichkeit zum Ausführen von „Get-AzSqlServerServiceObjective“ nach Standort, ohne dass bereits ein Server in der Region vorhanden sein muss</span><span class="sxs-lookup"><span data-stu-id="86269-1584">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="86269-1585">Unterstützung für Zeitzonenparameter bei der Erstellung einer verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="86269-1585">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="86269-1586">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-1586">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="86269-1587">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="86269-1587">Az.Websites</span></span>
* <span data-ttu-id="86269-1588">„Set-AzWebApp“ und „Set-AzWebAppSlot“ korrigiert, sodass die Tags bei der Ausführung nicht entfernt werden</span><span class="sxs-lookup"><span data-stu-id="86269-1588">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="86269-1589">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="86269-1589">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="86269-1590">WebSites SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1590">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="86269-1591">AdminSiteName-Eigenschaft aus „PSAppServicePlan“ entfernt</span><span class="sxs-lookup"><span data-stu-id="86269-1591">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="86269-1592">1.7.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="86269-1592">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="86269-1593">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="86269-1593">Highlights since the last major release</span></span>
* <span data-ttu-id="86269-1594">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="86269-1594">General availability of `Az` module</span></span>
* <span data-ttu-id="86269-1595">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="86269-1595">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="86269-1596">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="86269-1596">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="86269-1597">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1597">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="86269-1598">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1598">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="86269-1599">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1599">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="86269-1600">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="86269-1600">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="86269-1601">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86269-1601">Az.Accounts</span></span>
* <span data-ttu-id="86269-1602">„Add-AzEnvironment“ und „Set-AzEnvironment“ aktualisiert, um den Parameter „AzureAnalysisServicesEndpointResourceId“ zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="86269-1602">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="86269-1603">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="86269-1603">Az.AnalysisServices</span></span>
* <span data-ttu-id="86269-1604">ServiceClient wird in Cmdlets für die Datenebene verwendet, und die ursprüngliche Authentifizierungslogik wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="86269-1604">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="86269-1605">„Add-AzureASAccount“ wird als Wrapper von „Connect-AzAccount“ festgelegt, um einen Breaking Change zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="86269-1605">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="86269-1606">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="86269-1606">Az.Automation</span></span>
* <span data-ttu-id="86269-1607">Fehler des Cmdlets „Fixed New-AzAutomationSoftwareUpdateConfiguration“ für Einschlüsse behoben.</span><span class="sxs-lookup"><span data-stu-id="86269-1607">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="86269-1608">Die Parameter „IncludedKbNumber“ und „IncludedPackageNameMask“ sollten nun funktionieren.</span><span class="sxs-lookup"><span data-stu-id="86269-1608">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="86269-1609">Fehlerbehebung für eine dynamische Gruppe der Azure Automation-Updateverwaltung</span><span class="sxs-lookup"><span data-stu-id="86269-1609">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86269-1610">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86269-1610">Az.Compute</span></span>
* <span data-ttu-id="86269-1611">Parameter „HyperVGeneration“ zu „New-AzDiskConfig“ und „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1611">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="86269-1612">Zulassen der VM-Erstellung mit einem Katalogimage aus anderen Mandanten</span><span class="sxs-lookup"><span data-stu-id="86269-1612">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="86269-1613">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="86269-1613">Az.ContainerInstance</span></span>
* <span data-ttu-id="86269-1614">Problem im Parameter „-Command“ von „New-AzContainerGroup“ behoben, das dazu führte, dass ein nachgestelltes leeres Argument hinzugefügt wurde</span><span class="sxs-lookup"><span data-stu-id="86269-1614">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="86269-1615">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="86269-1615">Az.DataFactory</span></span>
* <span data-ttu-id="86269-1616">Version des ADF .NET SDK auf 3.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1616">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="86269-1617">Cmdlet „Set-AzDataFactoryV2“ mit zusätzlichen Parametern für RepoConfiguration-Einstellungen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1617">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="86269-1618">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86269-1618">Az.Resources</span></span>
* <span data-ttu-id="86269-1619">Verarbeitung von Anbietern für „Get-AzResource“ bei der Angabe der Parameter „-ResourceId“ oder „-ResourceGroupName“, „-Name“ und „-ResourceType“ verbessert</span><span class="sxs-lookup"><span data-stu-id="86269-1619">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="86269-1620">Fehlerbehandlung für „Test-AzDeployment“ und „Test-AzResourceGroupDeployment“ verbessert</span><span class="sxs-lookup"><span data-stu-id="86269-1620">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="86269-1621">Behandlung von außerhalb der Bereitstellungsüberprüfung aufgetretenen Fehlern und stattdessen Aufnahme in die Ausgabe des Befehls</span><span class="sxs-lookup"><span data-stu-id="86269-1621">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="86269-1622">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="86269-1622">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="86269-1623">Switch-Parameter „-IgnoreDynamicParameters“ zu Bereitstellungs-Cmdlets hinzugefügt, um Aufforderung in Skript- und Auftragsszenarien zu überspringen</span><span class="sxs-lookup"><span data-stu-id="86269-1623">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="86269-1624">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="86269-1624">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="86269-1625">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86269-1625">Az.Sql</span></span>
* <span data-ttu-id="86269-1626">Unterstützung für Klassifizierung von Datenbankdaten</span><span class="sxs-lookup"><span data-stu-id="86269-1626">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="86269-1627">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86269-1627">Az.Storage</span></span>
* <span data-ttu-id="86269-1628">Melden eines ausführlichen Fehlers beim Erstellen des Storage-Kontexts mit dem Parameter „-UseConnectedAccount“, aber ohne Azure-Anmeldekonto</span><span class="sxs-lookup"><span data-stu-id="86269-1628">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="86269-1629">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="86269-1629">New-AzStorageContext</span></span>
* <span data-ttu-id="86269-1630">Unterstützung für das Verwalten von Blobdiensteigenschaften eines bestimmten Storage-Kontos mit einer API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="86269-1630">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="86269-1631">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="86269-1631">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="86269-1632">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="86269-1632">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="86269-1633">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="86269-1633">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="86269-1634">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="86269-1634">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="86269-1635">Unterstützung von „-AsJob“ für Cmdlets für den Upload und Download von Blobs und Dateien</span><span class="sxs-lookup"><span data-stu-id="86269-1635">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="86269-1636">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="86269-1636">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="86269-1637">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="86269-1637">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="86269-1638">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="86269-1638">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="86269-1639">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="86269-1639">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="86269-1640">1.6.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="86269-1640">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="86269-1641">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="86269-1641">Highlights since the last major release</span></span>
* <span data-ttu-id="86269-1642">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="86269-1642">General availability of `Az` module</span></span>
* <span data-ttu-id="86269-1643">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="86269-1643">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="86269-1644">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="86269-1644">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="86269-1645">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1645">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="86269-1646">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1646">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="86269-1647">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1647">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="86269-1648">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="86269-1648">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="86269-1649">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="86269-1649">Az.Automation</span></span>
* <span data-ttu-id="86269-1650">Änderung an der Azure Automation-Updateverwaltung, um die folgenden neuen Features zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="86269-1650">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="86269-1651">Dynamische Gruppierung</span><span class="sxs-lookup"><span data-stu-id="86269-1651">Dynamic grouping</span></span>
    * <span data-ttu-id="86269-1652">Pre-/Post-Skripts</span><span class="sxs-lookup"><span data-stu-id="86269-1652">Pre-Post script</span></span>
    * <span data-ttu-id="86269-1653">Neustarteinstellung</span><span class="sxs-lookup"><span data-stu-id="86269-1653">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86269-1654">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86269-1654">Az.Compute</span></span>
* <span data-ttu-id="86269-1655">Problem mit der Pfadauflösung in „Get-AzVmBootDiagnosticsData“ behoben</span><span class="sxs-lookup"><span data-stu-id="86269-1655">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="86269-1656">Computeclientbibliothek auf 25.0.0. aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1656">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="86269-1657">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="86269-1657">Az.KeyVault</span></span>
* <span data-ttu-id="86269-1658">Unterstützung für Platzhalterzeichen zu KeyVault-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1658">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86269-1659">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86269-1659">Az.Network</span></span>
* <span data-ttu-id="86269-1660">Threat Intelligence-Unterstützung für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1660">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="86269-1661">Ressource der obersten Ebene für Application Gateway-Firewallrichtlinie und benutzerdefinierte Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1661">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="86269-1662">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="86269-1662">Az.RecoveryServices</span></span>
* <span data-ttu-id="86269-1663">SnapshotRetentionInDays in Azure-VM-Richtlinie hinzugefügt, um sofortigen Wiederherstellungspunkt zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="86269-1663">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="86269-1664">Pipe-Unterstützung für das Aufheben der Registrierung eines Containers hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1664">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="86269-1665">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86269-1665">Az.Resources</span></span>
* <span data-ttu-id="86269-1666">Unterstützung für Platzhalterzeichen für Get-AzResource und Get-AzResourceGroup aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1666">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="86269-1667">Anmeldeinformationen aktualisiert, die beim Senden generischer Aufrufe an ARM verwendet werden</span><span class="sxs-lookup"><span data-stu-id="86269-1667">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="86269-1668">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86269-1668">Az.Sql</span></span>
* <span data-ttu-id="86269-1669">Der Cmdlet-Parameter der Bedrohungserkennung (ExcludeDetectionType) wurde von „DetectionType“ in „string[]“ geändert, um ihn zukunftssicher zu machen, wenn neue DetectionTypes-Elemente hinzugefügt werden, und um AutoVervollständigen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="86269-1669">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="86269-1670">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86269-1670">Az.Storage</span></span>
* <span data-ttu-id="86269-1671">Unterstützung von Get-/Set-/Remove-Verwaltungsrichtlinien für Speicherkonto hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1671">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="86269-1672">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="86269-1672">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="86269-1673">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="86269-1673">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="86269-1674">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="86269-1674">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="86269-1675">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="86269-1675">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="86269-1676">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="86269-1676">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="86269-1677">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="86269-1677">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="86269-1678">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="86269-1678">Az.Websites</span></span>
* <span data-ttu-id="86269-1679">ARM-Vorlagenfehler behoben, der zu einem Problem beim Klonen aller Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ führte</span><span class="sxs-lookup"><span data-stu-id="86269-1679">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="86269-1680">1.5.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="86269-1680">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="86269-1681">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86269-1681">Az.Accounts</span></span>
* <span data-ttu-id="86269-1682">Der Befehl „Register-AzModule“ wurde hinzugefügt, um von AutoRest generierte Cmdlets zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="86269-1682">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="86269-1683">Beispiele für „Connect-AzAccount“ wurden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="86269-1683">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="86269-1684">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="86269-1684">Az.Automation</span></span>
* <span data-ttu-id="86269-1685">Problem behoben, das beim Abrufen bestimmter monatlicher Zeitpläne in verschiedenen Azure Automation-Cmdlets auftrat</span><span class="sxs-lookup"><span data-stu-id="86269-1685">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="86269-1686">„Get-AzAutomationDscNode“ wurde korrigiert, da nur die 20 obersten Knoten zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="86269-1686">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="86269-1687">Jetzt werden alle Knoten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="86269-1687">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="86269-1688">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="86269-1688">Az.Cdn</span></span>
* <span data-ttu-id="86269-1689">Neue Powershell-Cmdlets zum Aktivieren/Deaktivieren von HTTPS für benutzerdefinierte Domänen hinzugefügt und alte Cmdlets außer Betrieb genommen</span><span class="sxs-lookup"><span data-stu-id="86269-1689">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86269-1690">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86269-1690">Az.Compute</span></span>
* <span data-ttu-id="86269-1691">Unterstützung für Platzhalterzeichen zu Get-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1691">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="86269-1692">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="86269-1692">Az.DataFactory</span></span>
* <span data-ttu-id="86269-1693">Version des ADF .NET SDK auf 3.0.1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1693">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="86269-1694">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="86269-1694">Az.LogicApp</span></span>
* <span data-ttu-id="86269-1695">„ListWorkflows“ wurde korrigiert, da nur die erste Seite mit Ergebnissen abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="86269-1695">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86269-1696">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86269-1696">Az.Network</span></span>
* <span data-ttu-id="86269-1697">Unterstützung für Platzhalterzeichen zu Network-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1697">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="86269-1698">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="86269-1698">Az.RecoveryServices</span></span>
* <span data-ttu-id="86269-1699">SQL Server jetzt in Azure-VM-Support enthalten</span><span class="sxs-lookup"><span data-stu-id="86269-1699">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="86269-1700">SDK-Update</span><span class="sxs-lookup"><span data-stu-id="86269-1700">SDK Update</span></span>
* <span data-ttu-id="86269-1701">VMappContainer-Überprüfung in „Get-ProtectableItem“ entfernt</span><span class="sxs-lookup"><span data-stu-id="86269-1701">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="86269-1702">„Name“ und „ServerName“ als Parameter für „Get-ProtectableItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1702">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="86269-1703">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86269-1703">Az.Resources</span></span>
* <span data-ttu-id="86269-1704">Parameter `-TemplateObject` zu Bereitstellungs-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1704">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="86269-1705">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="86269-1705">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="86269-1706">Problem beim Piping des Ergebnisses von `Get-AzResource` an `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="86269-1706">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="86269-1707">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="86269-1707">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="86269-1708">Problem mit JSON-Datentypänderung beim Ausführen von `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="86269-1708">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="86269-1709">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="86269-1709">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="86269-1710">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86269-1710">Az.Sql</span></span>
* <span data-ttu-id="86269-1711">„AuditingEndpointsCommunicator“ wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="86269-1711">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="86269-1712">Das Verhalten eines Grenzfalls beim Erstellen neuer Diagnoseeinstellungen wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="86269-1712">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="86269-1713">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86269-1713">Az.Storage</span></span>
* <span data-ttu-id="86269-1714">Unterstützung von „Kind BlockBlobStorage“ beim Erstellen eines Speicherkontos: New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="86269-1714">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="86269-1715">1.4.0 – Februar 2019</span><span class="sxs-lookup"><span data-stu-id="86269-1715">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="86269-1716">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="86269-1716">Az.AnalysisServices</span></span>
* <span data-ttu-id="86269-1717">Cmdlet „AddAzureASAccount“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="86269-1717">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="86269-1718">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="86269-1718">Az.Automation</span></span>
* <span data-ttu-id="86269-1719">Hilfe für „Import-AzAutomationDscNodeConfiguration“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1719">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="86269-1720">Überprüfung des Konfigurationsnamens zu Cmdlet „Import-AzAutomationDscConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1720">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="86269-1721">Fehlerbehandlung für Cmdlet „Import-AzAutomationDscConfiguration“ verbessert</span><span class="sxs-lookup"><span data-stu-id="86269-1721">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="86269-1722">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="86269-1722">Az.CognitiveServices</span></span>
* <span data-ttu-id="86269-1723">„CustomSubdomainName“ als neuer optionaler Parameter für Cmdlet „New-AzCognitiveServicesAccount“ hinzugefügt, das zum Angeben der Unterdomäne für die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="86269-1723">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86269-1724">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86269-1724">Az.Compute</span></span>
* <span data-ttu-id="86269-1725">Problem mit ID-Parametersätzen behoben</span><span class="sxs-lookup"><span data-stu-id="86269-1725">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="86269-1726">„Get-AzVMExtension“ aktualisiert, sodass alle installierten Erweiterungen aufgelistet werden, wenn der Name-Parameter nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="86269-1726">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="86269-1727">Parameter „Tag“ und „ResourceId“ zum Cmdlet „Update-AzImage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1727">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="86269-1728">„Get-AzVmssVM“ ohne Instanz-ID und mit „InstanceView“ können virtuelle VMSS-Computer mit Instanzansicht auflisten.</span><span class="sxs-lookup"><span data-stu-id="86269-1728">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="86269-1729">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="86269-1729">Az.DataLakeStore</span></span>
* <span data-ttu-id="86269-1730">Cmdlets zum Auflisten und Wiederherstellen gelöschter ADL-Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1730">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="86269-1731">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="86269-1731">Az.EventHub</span></span>
* <span data-ttu-id="86269-1732">Neue boolesche Eigenschaft „SkipEmptyArchives“ zum Überspringen leerer Archive in Klasse „CaptureDescription“ von EventHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1732">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="86269-1733">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="86269-1733">Az.KeyVault</span></span>
* <span data-ttu-id="86269-1734">Kennzeichnung in „Set-AzKeyVaultSecret“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-1734">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="86269-1735">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="86269-1735">Az.LogicApp</span></span>
* <span data-ttu-id="86269-1736">SKU „Basic“ für Integrationskonten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1736">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="86269-1737">XSLT 2.0, XSLT 3.0 und Liquid-Zuordnungstypen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1737">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="86269-1738">Neue Cmdlets für Integrationskonto-Assemblys</span><span class="sxs-lookup"><span data-stu-id="86269-1738">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="86269-1739">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="86269-1739">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="86269-1740">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="86269-1740">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="86269-1741">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="86269-1741">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="86269-1742">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="86269-1742">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="86269-1743">Neue Cmdlets für Integrationskonto-Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="86269-1743">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="86269-1744">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="86269-1744">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="86269-1745">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="86269-1745">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="86269-1746">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="86269-1746">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="86269-1747">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="86269-1747">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="86269-1748">Logik-App-SDK auf Version 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1748">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="86269-1749">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="86269-1749">Az.Monitor</span></span>
* <span data-ttu-id="86269-1750">Hilfe für „Get-AzMetric“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1750">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86269-1751">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86269-1751">Az.Network</span></span>
* <span data-ttu-id="86269-1752">Hilfebeispiel für „Add-AzApplicationGatewayCustomError“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1752">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="86269-1753">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="86269-1753">Az.OperationalInsights</span></span>
* <span data-ttu-id="86269-1754">Zusätzliche Unterstützung für Datenquelle von „New-ApplicationInsights“ und „Get-ApplicationInsights“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-1754">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="86269-1755">Neue Art von „ApplicationInsights“ zum Abrufen von bestimmten und von allen ApplicationInsights-Datenquellen für einen Workspace hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-1755">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="86269-1756">Cmdlet „New-AzOperationalInsightsApplicationInsightsDataSource“ zum Erstellen einer Datenquelle anhand des angegebenen Ressourcenparameters für „Application-Insights“ hinzugefügt: „subscriptionId“, „resourceGroupName“ und „name“.</span><span class="sxs-lookup"><span data-stu-id="86269-1756">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="86269-1757">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86269-1757">Az.Resources</span></span>
* <span data-ttu-id="86269-1758">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="86269-1758">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="86269-1759">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="86269-1759">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="86269-1760">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="86269-1760">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="86269-1761">Fehler korrigiert, der die wiederholte Erstellung von „KeyCredentials“ verhindert</span><span class="sxs-lookup"><span data-stu-id="86269-1761">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="86269-1762">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86269-1762">Az.Sql</span></span>
* <span data-ttu-id="86269-1763">Unterstützung für SQL DB Hyperscale-Tarif hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1763">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="86269-1764">Fehler korrigiert, aufgrund dessen die Wiederherstellung wegen der Festlegung unnötiger Eigenschaften in der Wiederherstellungsanforderung fehlschlagen konnte</span><span class="sxs-lookup"><span data-stu-id="86269-1764">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="86269-1765">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="86269-1765">Az.Websites</span></span>
* <span data-ttu-id="86269-1766">Beispiel in „Get-AzWebAppSlotMetrics“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-1766">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="86269-1767">1.3.0: Februar 2019</span><span class="sxs-lookup"><span data-stu-id="86269-1767">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="86269-1768">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86269-1768">Az.Accounts</span></span>
* <span data-ttu-id="86269-1769">Update auf die aktuelle Version von ClientRuntime durchgeführt</span><span class="sxs-lookup"><span data-stu-id="86269-1769">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="86269-1770">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="86269-1770">Az.AnalysisServices</span></span>
<span data-ttu-id="86269-1771">Allgemeine Verfügbarkeit für Az.AnalysisServices-Modul</span><span class="sxs-lookup"><span data-stu-id="86269-1771">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86269-1772">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86269-1772">Az.Compute</span></span>
* <span data-ttu-id="86269-1773">AEM-Erweiterung: Unterstützung für UltraSSD und P60-, P70- und P80-Datenträger hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1773">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="86269-1774">Hilfebeschreibung für „Set-AzVMBootDiagnostics“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1774">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="86269-1775">Hilfebeschreibung und Beispiel für „Update-AzImage“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1775">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="86269-1776">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="86269-1776">Az.RecoveryServices</span></span>
<span data-ttu-id="86269-1777">Allgemeine Verfügbarkeit für Az.RecoveryServices-Modul.</span><span class="sxs-lookup"><span data-stu-id="86269-1777">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="86269-1778">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86269-1778">Az.Resources</span></span>
* <span data-ttu-id="86269-1779">Kennzeichnung für Ressourcengruppen korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-1779">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="86269-1780">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="86269-1780">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="86269-1781">Problem behoben, bei dem „-ErrorAction“ von `Get-AzureRmRoleAssignment` nicht berücksichtigt wird</span><span class="sxs-lookup"><span data-stu-id="86269-1781">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="86269-1782">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="86269-1782">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="86269-1783">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86269-1783">Az.Sql</span></span>
* <span data-ttu-id="86269-1784">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1784">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="86269-1785">Problem behoben, bei dem eine fehlende Anmeldung am Azure-Konto bei der Ausführung von SQL-Cmdlets zu einer nullref-Ausnahme führt</span><span class="sxs-lookup"><span data-stu-id="86269-1785">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="86269-1786">nullref-Ausnahme in Get-AzSqlCapability korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-1786">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="86269-1787">1.2.1: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="86269-1787">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="86269-1788">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86269-1788">Az.Accounts</span></span>
* <span data-ttu-id="86269-1789">Release mit richtiger Version der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="86269-1789">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="86269-1790">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="86269-1790">Az.AnalysisServices</span></span>
* <span data-ttu-id="86269-1791">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="86269-1791">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="86269-1792">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="86269-1792">Az.RecoveryServices</span></span>
* <span data-ttu-id="86269-1793">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="86269-1793">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="86269-1794">1.2.0: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="86269-1794">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="86269-1795">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86269-1795">Az.Accounts</span></span>
* <span data-ttu-id="86269-1796">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1796">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="86269-1797">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1797">Update incorrect online help URLs</span></span>
* <span data-ttu-id="86269-1798">Warnmeldung in PS Core für „Uninstall-AzureRm“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1798">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="86269-1799">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="86269-1799">Az.Aks</span></span>
* <span data-ttu-id="86269-1800">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1800">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="86269-1801">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="86269-1801">Az.Automation</span></span>
* <span data-ttu-id="86269-1802">Unterstützung für Python 2-Runbooks hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1802">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="86269-1803">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1803">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="86269-1804">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="86269-1804">Az.Cdn</span></span>
* <span data-ttu-id="86269-1805">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1805">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86269-1806">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86269-1806">Az.Compute</span></span>
* <span data-ttu-id="86269-1807">Cmdlet „Invoke-AzVMReimage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1807">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="86269-1808">Parameter „TempDisk“ zu „Set-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1808">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="86269-1809">Warnmeldung von „New-AzVM“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-1809">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="86269-1810">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="86269-1810">Az.ContainerRegistry</span></span>
* <span data-ttu-id="86269-1811">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1811">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="86269-1812">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="86269-1812">Az.DataFactory</span></span>
* <span data-ttu-id="86269-1813">Version des ADF .NET SDK auf 3.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1813">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="86269-1814">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="86269-1814">Az.DataLakeStore</span></span>
* <span data-ttu-id="86269-1815">Problem mit ADLS-Endpunkt bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="86269-1815">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="86269-1816">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="86269-1816">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="86269-1817">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1817">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="86269-1818">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="86269-1818">Az.IotHub</span></span>
* <span data-ttu-id="86269-1819">Codierungsformat zu Cmdlet „Add-IotHubRoutingEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1819">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="86269-1820">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="86269-1820">Az.KeyVault</span></span>
* <span data-ttu-id="86269-1821">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1821">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86269-1822">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86269-1822">Az.Network</span></span>
* <span data-ttu-id="86269-1823">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1823">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="86269-1824">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86269-1824">Az.Resources</span></span>
* <span data-ttu-id="86269-1825">Fehlerhafte Beispiele in Referenzdokumentation zu „New-AzADAppCredential“ und „New-AzADSpCredential“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-1825">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="86269-1826">Problem behoben, bei dem der Pfad für den Parameter „-TemplateFile“ nicht aufgelöst wurde, bevor Cmdlets für die Bereitstellung von Ressourcengruppen ausgeführt wurden</span><span class="sxs-lookup"><span data-stu-id="86269-1826">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="86269-1827">Az.Resources: Richtige Dokumentation für Standardwert von „New-AzureRmPolicyDefinition -Mode“ bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="86269-1827">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="86269-1828">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="86269-1828">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="86269-1829">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="86269-1829">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="86269-1830">Formatierungsproblem für Objekt „PSResourceGroupDeployment“ behoben</span><span class="sxs-lookup"><span data-stu-id="86269-1830">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="86269-1831">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="86269-1831">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="86269-1832">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="86269-1832">Az.ServiceFabric</span></span>
* <span data-ttu-id="86269-1833">Rollback beim Hinzufügen eines Zertifikats zum VMSS-Modell, Auslösung einer Ausnahme. Fehlerbehebung: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="86269-1833">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="86269-1834">Einige Fehlermeldungen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="86269-1834">Fix some error messages.</span></span>
* <span data-ttu-id="86269-1835">Fehler bei Clustererstellung mit ARM-Standardvorlage für „New-AzServiceFabriCluster“ behoben, bei dem die Migration zu Az nicht funktioniert hat.</span><span class="sxs-lookup"><span data-stu-id="86269-1835">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="86269-1836">Fehler behoben beim Hinzufügen eines Cluster-/Anwendungszertifikats ausschließlich zu VM Scale Sets, die zum Cluster gehören, indem die Cluster-ID in der Erweiterung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="86269-1836">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="86269-1837">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="86269-1837">Az.SignalR</span></span>
* <span data-ttu-id="86269-1838">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1838">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="86269-1839">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86269-1839">Az.Sql</span></span>
* <span data-ttu-id="86269-1840">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1840">Update incorrect online help URLs</span></span>
* <span data-ttu-id="86269-1841">Parameterbeschreibung für den Parameter „LicenseType“ mit möglichen Werten aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1841">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="86269-1842">Fehler behoben, bei dem die Aktualisierung der Identität der verwalteten Instanz nicht funktioniert hat, wenn es sich um die einzige aktualisierte Eigenschaft gehandelt hat</span><span class="sxs-lookup"><span data-stu-id="86269-1842">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="86269-1843">Unterstützung für die benutzerdefinierte Sortierung auf verwalteter Instanz</span><span class="sxs-lookup"><span data-stu-id="86269-1843">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="86269-1844">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86269-1844">Az.Storage</span></span>
* <span data-ttu-id="86269-1845">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1845">Update incorrect online help URLs</span></span>
* <span data-ttu-id="86269-1846">Ausführliche Fehlermeldung beim Abrufen/Festlegen der klassischen Protokollierung bzw. Metriken für Storage Premium-Konto, da für das Storage Premium-Konto die klassische Protokollierung bzw. Metriken nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="86269-1846">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="86269-1847">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="86269-1847">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="86269-1848">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="86269-1848">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="86269-1849">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="86269-1849">Az.TrafficManager</span></span>
* <span data-ttu-id="86269-1850">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1850">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="86269-1851">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="86269-1851">Az.Websites</span></span>
* <span data-ttu-id="86269-1852">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1852">Update incorrect online help URLs</span></span>
* <span data-ttu-id="86269-1853">„New-AzWebAppSSLBinding“ korrigiert, damit das Zertifikat in die richtige Ressourcengruppe bzw. an den richtigen Speicherort hochgeladen wird, wenn die App in einer ASE gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="86269-1853">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="86269-1854">„New-AzWebAppSSLBinding“ korrigiert, damit die Tags beim Binden eines SSL-Zertifikats an eine App nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="86269-1854">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="86269-1855">1.1.0 – Januar 2019</span><span class="sxs-lookup"><span data-stu-id="86269-1855">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="86269-1856">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86269-1856">Az.Accounts</span></span>
* <span data-ttu-id="86269-1857">Bereich „Local“ zu „Enable-AzureRmAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1857">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86269-1858">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86269-1858">Az.Compute</span></span>
* <span data-ttu-id="86269-1859">Name ist jetzt optional im ID-Parametersatz für „Restart/Start/Stop/Remove/Set-AzVM“ und „Save-AzVMImage“</span><span class="sxs-lookup"><span data-stu-id="86269-1859">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="86269-1860">Beschreibung der ID in Hilfedateien aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1860">Updated the description of ID in help files</span></span>
* <span data-ttu-id="86269-1861">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="86269-1861">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="86269-1862">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="86269-1862">Az.DataLakeStore</span></span>
* <span data-ttu-id="86269-1863">Aktualisierung der SDK-Version der Datenebene auf 1.1.14 für SDK-Fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="86269-1863">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="86269-1864">Behandlung von negativen acesstime- and modificationtime-Werten für „getfilestatus“ und „liststatus“ korrigiert, asynchrones Abbruchtoken korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-1864">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="86269-1865">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="86269-1865">Az.EventGrid</span></span>
* <span data-ttu-id="86269-1866">Zur Verwendung der API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1866">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="86269-1867">Aktualisierung der folgenden Cmdlets zur Unterstützung des neuen Szenarios in der API-Version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="86269-1867">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="86269-1868">New-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="86269-1868">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="86269-1869">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="86269-1869">Event Time-To-Live,</span></span>
        - <span data-ttu-id="86269-1870">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="86269-1870">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="86269-1871">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="86269-1871">Dead letter endpoint.</span></span>
    - <span data-ttu-id="86269-1872">Update-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="86269-1872">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="86269-1873">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="86269-1873">Event Time-To-Live,</span></span>
        - <span data-ttu-id="86269-1874">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="86269-1874">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="86269-1875">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="86269-1875">Dead letter endpoint.</span></span>
* <span data-ttu-id="86269-1876">Neue Enumerationswerte („storageQueue“ und „hybridConnection“) für die EndpointType-Option in den Cmdlets „New-AzureRmEventGridSubscription“ und „Update-AzureRmEventGridSubscription“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1876">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="86269-1877">Anzeige einer Warnmeldung, wenn das Erstellen oder Aktualisieren des Ereignisabonnements voraussichtlich eine manuelle Aktion des Benutzers zur Folge hat</span><span class="sxs-lookup"><span data-stu-id="86269-1877">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="86269-1878">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="86269-1878">Az.IotHub</span></span>
* <span data-ttu-id="86269-1879">Auf die aktuelle Version des Iot Hub SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1879">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="86269-1880">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="86269-1880">Az.LogicApp</span></span>
* <span data-ttu-id="86269-1881">„Get-AzLogicApp“ listet alle Apps ohne angegebenen Namen auf</span><span class="sxs-lookup"><span data-stu-id="86269-1881">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="86269-1882">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86269-1882">Az.Resources</span></span>
* <span data-ttu-id="86269-1883">Problem mit dem Parametersatz bei Angabe der Parameter „-ODataQuery“ und „-ResourceId“ für „Get-AzResource“ behoben</span><span class="sxs-lookup"><span data-stu-id="86269-1883">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="86269-1884">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="86269-1884">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="86269-1885">Behandlung des Parameters „-Custom“ in „New/Set-AzPolicyDefinition“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-1885">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="86269-1886">Tippfehler in der Dokumentation für „New-AzDeployment“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-1886">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="86269-1887">Parameter „-MailNickname“ als obligatorisch festgelegt für „New-AzADUser“</span><span class="sxs-lookup"><span data-stu-id="86269-1887">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="86269-1888">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="86269-1888">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="86269-1889">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="86269-1889">Az.SignalR</span></span>
* <span data-ttu-id="86269-1890">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="86269-1890">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="86269-1891">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86269-1891">Az.Sql</span></span>
* <span data-ttu-id="86269-1892">Abhängigkeit des Speicherverwaltungsclients zur allgemeinen SDK-Implementierung konvertiert</span><span class="sxs-lookup"><span data-stu-id="86269-1892">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="86269-1893">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86269-1893">Az.Storage</span></span>
* <span data-ttu-id="86269-1894">Festlegung des „StorageAccountName“ des Speicherkontexts als tatsächlichen Namen des Speicherkontos, wenn dieser mit „SAS-Token“, „OAuth“ oder „Anonym“ erstellt wird</span><span class="sxs-lookup"><span data-stu-id="86269-1894">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="86269-1895">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="86269-1895">New-AzStorageContext</span></span>
* <span data-ttu-id="86269-1896">Erstellen von SAS-Token des Blob-Momentaufnahmeobjekts mit dem Parameter „-FullUri“, Festlegung des zurückgegebenen URI als Momentaufnahme-URI</span><span class="sxs-lookup"><span data-stu-id="86269-1896">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="86269-1897">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="86269-1897">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="86269-1898">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="86269-1898">Az.Websites</span></span>
* <span data-ttu-id="86269-1899">Fehler bei der Datumsanalyse in „Get-AzDeletedWebApp“ behoben</span><span class="sxs-lookup"><span data-stu-id="86269-1899">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="86269-1900">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="86269-1900">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="86269-1901">1.0.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="86269-1901">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="86269-1902">Allgemein</span><span class="sxs-lookup"><span data-stu-id="86269-1902">General</span></span>

- <span data-ttu-id="86269-1903">Allgemeine Verfügbarkeit des Az-Moduls</span><span class="sxs-lookup"><span data-stu-id="86269-1903">General Availability of Az Module</span></span>
- <span data-ttu-id="86269-1904">Onlinehilfe für jedes Modul</span><span class="sxs-lookup"><span data-stu-id="86269-1904">Online help for each module</span></span>
- <span data-ttu-id="86269-1905">Ausführlichere Informationen und eine Roadmap finden Sie auf der [Seite mit der Ankündigung zu Az](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="86269-1905">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="86269-1906">Informationen zur Migration aus AzureRM finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="86269-1906">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="86269-1907">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="86269-1907">Az.Accounts</span></span>
- <span data-ttu-id="86269-1908">Geändert von Az.Profile</span><span class="sxs-lookup"><span data-stu-id="86269-1908">Changed from Az.Profile</span></span>
- <span data-ttu-id="86269-1909">Feste Tabellenformate für Profil- und Kontexttypen</span><span class="sxs-lookup"><span data-stu-id="86269-1909">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="86269-1910">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="86269-1910">Az.ApiManagement</span></span>
- <span data-ttu-id="86269-1911">Korrekturen für #7002</span><span class="sxs-lookup"><span data-stu-id="86269-1911">Fixes for #7002</span></span>
- <span data-ttu-id="86269-1912">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="86269-1912">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="86269-1913">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="86269-1913">Az.Batch</span></span>
- <span data-ttu-id="86269-1914">Möglichkeit zum Anzeigen der ausgeführten Version des Azure Batch-Knoten-Agents auf den VMs eines Pools mit der neuen `NodeAgentInformation`-Eigenschaft für `PSComputeNode` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-1914">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="86269-1915">Der `Caching`-Standardwert für `PSDataDisk` lautet jetzt nicht mehr `None`, sondern `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="86269-1915">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="86269-1916">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="86269-1916">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="86269-1917">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="86269-1917">Az.Billing</span></span>
- <span data-ttu-id="86269-1918">Kombination von Billing-, Consumption- und UsageAggregates-Cmdlets. Ausführliche Informationen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="86269-1918">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="86269-1919">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="86269-1919">Az.CognitivServices</span></span>
- <span data-ttu-id="86269-1920">Vervollständigungen für SkuName und Typem für den Vorgang New-AzureRmCognitiveServicesAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1920">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="86269-1921">GetSkusWithAccountParamSetName-Parametersatz aus Get-AzCognitiveServicesAccountSkus entfernt</span><span class="sxs-lookup"><span data-stu-id="86269-1921">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="86269-1922">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="86269-1922">Az.ContainerInstance</span></span>
- <span data-ttu-id="86269-1923">ManagedIdentity-Unterstützung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1923">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="86269-1924">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="86269-1924">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="86269-1925">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="86269-1925">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="86269-1926">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="86269-1926">Az.DataLakeStore</span></span>
- <span data-ttu-id="86269-1927">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="86269-1927">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="86269-1928">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="86269-1928">Az.Monitor</span></span>
- <span data-ttu-id="86269-1929">Az.Insights in Az.Monitor umbenannt und weitere weniger wichtige grundlegende Änderungen durchgeführt. Informationen hierzu finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="86269-1929">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="86269-1930">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="86269-1930">Az.KeyVault</span></span>
- <span data-ttu-id="86269-1931">Veraltete PurgeDisabled-Eigenschaft aus Ausgabetypen entfernt</span><span class="sxs-lookup"><span data-stu-id="86269-1931">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="86269-1932">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="86269-1932">Az.MachineLearning</span></span>
- <span data-ttu-id="86269-1933">Cmdlets des Az.MachineLearningCompute-Moduls eingebunden</span><span class="sxs-lookup"><span data-stu-id="86269-1933">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="86269-1934">Az.Media</span><span class="sxs-lookup"><span data-stu-id="86269-1934">Az.Media</span></span>
- <span data-ttu-id="86269-1935">Veralteten -Tags-Alias aus New-AzMediaService entfernt</span><span class="sxs-lookup"><span data-stu-id="86269-1935">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="86269-1936">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86269-1936">Az.Network</span></span>
<span data-ttu-id="86269-1937">Unterstützung für das Konfigurieren von RewriteRuleSets im Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1937">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="86269-1938">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="86269-1938">New cmdlets added:</span></span>
        - <span data-ttu-id="86269-1939">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="86269-1939">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="86269-1940">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="86269-1940">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="86269-1941">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="86269-1941">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="86269-1942">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="86269-1942">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="86269-1943">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="86269-1943">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="86269-1944">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="86269-1944">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="86269-1945">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="86269-1945">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="86269-1946">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="86269-1946">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="86269-1947">Cmdlets mit optionalem Parameter -RewriteRuleSet aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1947">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="86269-1948">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="86269-1948">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="86269-1949">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="86269-1949">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="86269-1950">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="86269-1950">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="86269-1951">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="86269-1951">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="86269-1952">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="86269-1952">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="86269-1953">New-AzureRmApplicationGatewayUrlPathMapConfig: KeyVault-Unterstützung mithilfe von Identität zum Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-1953">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="86269-1954">Cmdlets mit optionalem Parameter aktualisiert: -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="86269-1954">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="86269-1955">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="86269-1955">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="86269-1956">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="86269-1956">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="86269-1957">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="86269-1957">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="86269-1958">Cmdlet New-AzApplicationGateway mit optionalem Parameter -UserAssignedIdentity aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1958">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="86269-1959">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="86269-1959">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="86269-1960">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="86269-1960">Az.OperationalInsights</span></span>
- <span data-ttu-id="86269-1961">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="86269-1961">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="86269-1962">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="86269-1962">Az.Profile</span></span>
- <span data-ttu-id="86269-1963">Modulnamen in Az.Accounts geändert</span><span class="sxs-lookup"><span data-stu-id="86269-1963">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="86269-1964">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="86269-1964">Az.RecoveryServices</span></span>
- <span data-ttu-id="86269-1965">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="86269-1965">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="86269-1966">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86269-1966">Az.Resources</span></span>
- <span data-ttu-id="86269-1967">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="86269-1967">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="86269-1968">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="86269-1968">Az.ServiceFabric</span></span>
- <span data-ttu-id="86269-1969">Unterstützung für das Angeben des Zertifikats anhand des allgemeinen Namens und Fingerabdrucks</span><span class="sxs-lookup"><span data-stu-id="86269-1969">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="86269-1970">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="86269-1970">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="86269-1971">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="86269-1971">Az.SIgnalR</span></span>
- <span data-ttu-id="86269-1972">Allgemeine Verfügbarkeit für PowerShell-Cmdlets für SIgnalR</span><span class="sxs-lookup"><span data-stu-id="86269-1972">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="86269-1973">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86269-1973">Az.Sql</span></span>
- <span data-ttu-id="86269-1974">Neue Erkennungstypen Data_Exfiltration und Unsafe_Action zu Cmdlets für Bedrohungserkennung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-1974">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="86269-1975">Dokumentationsbeispiele für Cmdlets für SQL-Überwachung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-1975">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="86269-1976">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="86269-1976">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="86269-1977">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86269-1977">Az.Storage</span></span>
- <span data-ttu-id="86269-1978">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="86269-1978">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="86269-1979">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="86269-1979">Az.Websites</span></span>
- <span data-ttu-id="86269-1980">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="86269-1980">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="86269-1981">0.7.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="86269-1981">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="86269-1982">Allgemein</span><span class="sxs-lookup"><span data-stu-id="86269-1982">General</span></span>

* <span data-ttu-id="86269-1983">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="86269-1983">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="86269-1984">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86269-1984">Az.Compute</span></span>

* <span data-ttu-id="86269-1985">Unterstützung für UltraSSD und Katalogimages in einfachen Parametersätzen für `New-AzVm(ss)`-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-1985">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="86269-1986">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="86269-1986">Az.DataLakeStore</span></span>

* <span data-ttu-id="86269-1987">Nachgestellten Schrägstrich für die Domäne des ADLS-Kontos korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-1987">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="86269-1988">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="86269-1988">Az.FrontDoor</span></span>

* <span data-ttu-id="86269-1989">Einige fehlerhafte Links behoben</span><span class="sxs-lookup"><span data-stu-id="86269-1989">Fixed some broken links</span></span>
    - <span data-ttu-id="86269-1990">In den Artikeln zu New-AzureRmFrontDoor und Set-AzureRmFrontDoor den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorHealthProbeSettingObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="86269-1990">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="86269-1991">Im Artikel zu New-AzureRmFrontDoorManagedRuleObject den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorRuleGroupOverrideObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="86269-1991">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="86269-1992">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="86269-1992">Az.RecoveryServices</span></span>

* <span data-ttu-id="86269-1993">Clientseitige Validierungen für Wiederherstellungsvorgänge von Azure-Dateifreigaben hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-1993">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="86269-1994">storageAccountName und storageAccountResourceGroupName für AFS-Wiederherstellung optional gemacht.</span><span class="sxs-lookup"><span data-stu-id="86269-1994">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="86269-1995">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86269-1995">Az.Resources</span></span>

* <span data-ttu-id="86269-1996">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="86269-1996">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="86269-1997">Get-AzureRmRoleAssignment für die Verwendung des Abonnementbereichs aktualisiert, wenn dieser beim Anfordern von klassischen Administratoren angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="86269-1997">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="86269-1998">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86269-1998">Az.Sql</span></span>

* <span data-ttu-id="86269-1999">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="86269-1999">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="86269-2000">Problem mit der Verwendung von Get-AzureRmSqlDatabaseVulnerabilityAssessment mit .NET Core behoben</span><span class="sxs-lookup"><span data-stu-id="86269-2000">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="86269-2001">Dokumentation mit Hilfemeldungen zu Cmdlets für die SQL-Überwachung geändert.</span><span class="sxs-lookup"><span data-stu-id="86269-2001">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="86269-2002">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="86269-2002">Az.Storage</span></span>

* <span data-ttu-id="86269-2003">-EnableHierarchicalNamespace zu New-AzureRmStorageAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-2003">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="86269-2004">Problem behoben, bei dem für das Copy File-Cmdlet am Ziel kein Quellkontext wiederverwendet werden kann, wenn -DestContext nicht eingegeben wird</span><span class="sxs-lookup"><span data-stu-id="86269-2004">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="86269-2005">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="86269-2005">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="86269-2006">Unterstützung der Konfiguration von statischen Websites</span><span class="sxs-lookup"><span data-stu-id="86269-2006">Support Static Website configuration</span></span>
    - <span data-ttu-id="86269-2007">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="86269-2007">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="86269-2008">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="86269-2008">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="86269-2009">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="86269-2009">Az.Websites</span></span>

* <span data-ttu-id="86269-2010">Set-AzureRmWebApp und Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="86269-2010">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="86269-2011">Neuen Parameter (-AzureStoragePath) zum Angeben von Azure Storage-Pfaden hinzugefügt, die in Windows- und Linux-Container-Apps bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="86269-2011">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="86269-2012">Verwenden Sie die Ausgabe des neuen Cmdlets New-AzureRmWebAppAzureStoragePath als Parameter zum Festlegen der Azure Storage-Pfade.</span><span class="sxs-lookup"><span data-stu-id="86269-2012">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="86269-2013">0.6.1 – November 2018</span><span class="sxs-lookup"><span data-stu-id="86269-2013">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="86269-2014">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="86269-2014">Az.ApiManagement</span></span>
* <span data-ttu-id="86269-2015">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-2015">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="86269-2016">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="86269-2016">Az.Automation</span></span>
* <span data-ttu-id="86269-2017">Swagger-basierte Azure Automation-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="86269-2017">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="86269-2018">Cmdlets zur Updateverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-2018">Added Update Management cmdlets</span></span>
* <span data-ttu-id="86269-2019">Cmdlets zur Quellcodeverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-2019">Added Source Control cmdlets</span></span>
* <span data-ttu-id="86269-2020">Cmdlet „Remove-AzureRmAutomationHybridWorkerGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-2020">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="86269-2021">DSC-Befehl für die Knotenregistrierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-2021">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="86269-2022">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86269-2022">Az.Compute</span></span>
* <span data-ttu-id="86269-2023">Identitätsproblem für SystemAssigned-Identität korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-2023">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="86269-2024">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-2024">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="86269-2025">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="86269-2025">Az.ContainerInstance</span></span>
* <span data-ttu-id="86269-2026">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-2026">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="86269-2027">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="86269-2027">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="86269-2028">Beschreibung der Beispiele für Marketplace-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-2028">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="86269-2029">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86269-2029">Az.Network</span></span>
* <span data-ttu-id="86269-2030">Folgende Cmdlets hinzugefügt: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="86269-2030">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="86269-2031">ICMP wieder unterstützten AzureFirewall-Netzwerkprotokollen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-2031">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="86269-2032">Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert und Überprüfung für Ziel-ID, Adresse und Port hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-2032">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="86269-2033">Probleme mit Arbeitsspeicherauslastung in der VirtualNetwork-Zuordnung behoben</span><span class="sxs-lookup"><span data-stu-id="86269-2033">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="86269-2034">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="86269-2034">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="86269-2035">Problem beim Ändern der Richtlinie für eine geschützte Dateifreigabe behoben</span><span class="sxs-lookup"><span data-stu-id="86269-2035">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="86269-2036">Richtlinienzeitzone in Großschreibung geändert</span><span class="sxs-lookup"><span data-stu-id="86269-2036">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="86269-2037">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="86269-2037">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="86269-2038">Korrigiertes Beispiel in „New-AzureRmRecoveryServicesAsrProtectableItem“</span><span class="sxs-lookup"><span data-stu-id="86269-2038">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="86269-2039">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-2039">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="86269-2040">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="86269-2040">Az.Relay</span></span>
* <span data-ttu-id="86269-2041">Optionaler Parameter „-KeyValue“ zu Cmdlet „New-AzureRmRelayKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht</span><span class="sxs-lookup"><span data-stu-id="86269-2041">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="86269-2042">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86269-2042">Az.Resources</span></span>
* <span data-ttu-id="86269-2043">Hilfedokumentation für ressourcenidentitätsbezogene Parameter in `New-AzureRmPolicyAssignment` und `Set-AzureRmPolicyAssignment` aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-2043">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="86269-2044">Beispiel für „New-AzureRmPolicyDefinition“ hinzugefügt, das „-Metadata“ nutzt</span><span class="sxs-lookup"><span data-stu-id="86269-2044">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="86269-2045">Korrektur, um Beibehaltung von Groß-/Kleinschreibung in Tagschlüsseln in „NetStandard“ zu ermöglichen: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="86269-2045">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="86269-2046">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="86269-2046">Az.ServiceFabric</span></span>
* <span data-ttu-id="86269-2047">Benachrichtigung über veraltete Elemente für anstehende wichtige Änderungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-2047">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="86269-2048">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86269-2048">Az.Sql</span></span>
* <span data-ttu-id="86269-2049">Neue Cmdlets für CRUD-Vorgänge in verwalteten Azure SQL-Datenbank-Instanzen und verwalteten Azure SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-2049">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="86269-2050">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="86269-2050">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="86269-2051">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="86269-2051">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="86269-2052">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="86269-2052">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="86269-2053">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="86269-2053">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="86269-2054">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="86269-2054">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="86269-2055">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="86269-2055">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="86269-2056">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="86269-2056">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="86269-2057">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="86269-2057">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="86269-2058">Erweiterte Verwaltung von Überwachungsrichtlinien auf einem Server oder in einer Datenbank aktiviert</span><span class="sxs-lookup"><span data-stu-id="86269-2058">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="86269-2059">Neuer Parameter (PredicateExpression) hinzugefügt, um die Filterung von Überwachungsprotokollen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="86269-2059">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="86269-2060">Cmdlets wurden angepasst, sodass sie SQL-Clients anstelle von Legacyclients verwenden.</span><span class="sxs-lookup"><span data-stu-id="86269-2060">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="86269-2061">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="86269-2061">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="86269-2062">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="86269-2062">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="86269-2063">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="86269-2063">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="86269-2064">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="86269-2064">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="86269-2065">Problem bei Verwendung von „Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings“ mit festgelegtem Parameter für den Speicherkontonamen behoben</span><span class="sxs-lookup"><span data-stu-id="86269-2065">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="86269-2066">0.5.0 – November 2018</span><span class="sxs-lookup"><span data-stu-id="86269-2066">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="86269-2067">Allgemein</span><span class="sxs-lookup"><span data-stu-id="86269-2067">General</span></span>
* <span data-ttu-id="86269-2068">Ressourcenvervollständigungen für viele Kern-Cmdlets hinzugefügt (diese ermöglichen das Durchlaufen von vorhandenen Ressourcennamen per TAB-TASTE, wenn Cmdlets interaktiv aufgerufen werden)</span><span class="sxs-lookup"><span data-stu-id="86269-2068">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="86269-2069">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="86269-2069">Az.Profile</span></span>
* <span data-ttu-id="86269-2070">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="86269-2070">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="86269-2071">Parameter „TenantId“ im Cmdlet „Connect-AzAccount“ in „Tenant“ umbenannt und Alias für „TenantId“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-2071">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="86269-2072">Beschreibung von „TenantId“ für „Connect-AzAccount“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="86269-2072">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="86269-2073">Fehlermeldung für fehlgeschlagene Anmeldung bei Angabe der Mandantendomäne korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-2073">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="86269-2074">Problem in Bezug auf Kontextnamenskonflikt für Konten ohne Abonnements im Mandanten behoben</span><span class="sxs-lookup"><span data-stu-id="86269-2074">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="86269-2075">Problem mit DataLake-Endpunkten bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="86269-2075">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="86269-2076">Problem behoben, das zur Auslösung von „Disconnect-AzAccount“ führte, wenn keine Verbindung bestand</span><span class="sxs-lookup"><span data-stu-id="86269-2076">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="86269-2077">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="86269-2077">Az.CognitiveServices</span></span>
* <span data-ttu-id="86269-2078">Vorgang „Get-AzCognitiveServicesAccountSkus“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-2078">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86269-2079">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86269-2079">Az.Compute</span></span>
* <span data-ttu-id="86269-2080">Cmdlets Add-AzVmssVMDataDisk und Remove-AzVmssVMDataDisk hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-2080">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="86269-2081">„Get-AzVMImage“ zeigt „AutomaticOSUpgradeProperties“ an</span><span class="sxs-lookup"><span data-stu-id="86269-2081">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="86269-2082">Problem behoben, aufgrund dessen die Optionswerte „SetAzVMChefExtension -BootstrapOptions“ und „-JsonAttribute“ nicht im JSON-Format festgelegt wurden</span><span class="sxs-lookup"><span data-stu-id="86269-2082">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="86269-2083">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="86269-2083">Az.DataLakeStore</span></span>
* <span data-ttu-id="86269-2084">Aktualisierung des DataLake-Pakets auf 1.1.10</span><span class="sxs-lookup"><span data-stu-id="86269-2084">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="86269-2085">Standardmäßige Parallelität zu Multithreadvorgängen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-2085">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="86269-2086">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="86269-2086">Az.Insights</span></span>
* <span data-ttu-id="86269-2087">Problem Nr. 7267 behoben (Bereich für automatische Skalierung)</span><span class="sxs-lookup"><span data-stu-id="86269-2087">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="86269-2088">Probleme beim Erstellen einer neuen Regel für die automatische Skalierung, aufgrund derer die aufgelisteten Parameter nicht richtig festgelegt wurden (Es wurde stets der Standardwert festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="86269-2088">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="86269-2089">Problem Nr. 7513 behoben [Insights] „Set-AzDiagnosticSetting“ erfordert die explizite Angabe von Kategorien während der Erstellung der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="86269-2089">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="86269-2090">Nun erfordert das Cmdlet nicht die explizite Angabe der Kategorien, die während der Erstellung aktiviert werden sollen. Das bedeutet, es funktioniert wie dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="86269-2090">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86269-2091">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86269-2091">Az.Network</span></span>
* <span data-ttu-id="86269-2092">„PeeringType“ wurde geändert und ist nun ein erforderlicher Parameter für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="86269-2092">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="86269-2093">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="86269-2093">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="86269-2094">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="86269-2094">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="86269-2095">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="86269-2095">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="86269-2096">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="86269-2096">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="86269-2097">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="86269-2097">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="86269-2098">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="86269-2098">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="86269-2099">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="86269-2099">Az.PolicyInsights</span></span>
* <span data-ttu-id="86269-2100">Cmdlets für Richtlinienwartung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-2100">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="86269-2101">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86269-2101">Az.Resources</span></span>
* <span data-ttu-id="86269-2102">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="86269-2102">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="86269-2103">Zulassen der Auflistung von Ressourcen mithilfe des Parameters „-ResourceId“ für „Get-AzResource“</span><span class="sxs-lookup"><span data-stu-id="86269-2103">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="86269-2104">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="86269-2104">Az.ServiceBus</span></span>
* <span data-ttu-id="86269-2105">Schreibgeschützte Eigenschaft „MigrationState“ zu „PSServiceBusMigrationConfigurationAttributes“ hinzugefügt, was das Ermitteln des Migrationsstatus ermöglicht</span><span class="sxs-lookup"><span data-stu-id="86269-2105">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="86269-2106">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="86269-2106">Az.ServiceFabric</span></span>
* <span data-ttu-id="86269-2107">Hinzufügen des Zertifikats zu Linux VMSS korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-2107">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="86269-2108">„Add-AzServiceFabricClusterCertificate“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="86269-2108">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="86269-2109">Verwenden des richtigen Fingerabdrucks aus dem neuen Zertifikat (Azure/service-fabric-issues#932)</span><span class="sxs-lookup"><span data-stu-id="86269-2109">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="86269-2110">Richtige Anzeige von Ausnahmen (Azure/service-fabric-issues#1054)</span><span class="sxs-lookup"><span data-stu-id="86269-2110">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="86269-2111">„Update-AzServiceFabricDurability“ korrigiert, um die Clusterkonfiguration zu aktualisieren, bevor der VMSS-Vorgang „CreateOrUpdate“ gestartet wird</span><span class="sxs-lookup"><span data-stu-id="86269-2111">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="86269-2112">0.4.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="86269-2112">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="86269-2113">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="86269-2113">Az.Profile</span></span>
* <span data-ttu-id="86269-2114">Problem mit „Get-AzSubscription“ in Cloud Shell behoben</span><span class="sxs-lookup"><span data-stu-id="86269-2114">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="86269-2115">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="86269-2115">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86269-2116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86269-2116">Az.Compute</span></span>
* <span data-ttu-id="86269-2117">Neue Größen zur Whitelist von VM-Größen hinzugefügt, für die bei Verwendung des einfachen Parametersatzes für „New-AzVm“ der beschleunigte Netzwerkbetrieb aktiviert wird</span><span class="sxs-lookup"><span data-stu-id="86269-2117">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="86269-2118">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-2118">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="86269-2119">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="86269-2119">Az.DataLakeStore</span></span>
* <span data-ttu-id="86269-2120">Unterstützung für VNET-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-2120">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="86269-2121">Get-AzDataLakeStoreVirtualNetworkRule: Dient zum Abrufen oder Auflisten der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="86269-2121">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="86269-2122">Add-AzDataLakeStoreVirtualNetworkRule: Fügt dem angegebenen Data Lake Store-Konto eine Regel für das virtuelle Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="86269-2122">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="86269-2123">Set-AzDataLakeStoreVirtualNetworkRule: Ändert die angegebene Regel für das virtuelle Netzwerk in das angegebene Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="86269-2123">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="86269-2124">Remove-AzDataLakeStoreVirtualNetworkRule: Dient zum Löschen der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="86269-2124">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86269-2125">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86269-2125">Az.Network</span></span>
* <span data-ttu-id="86269-2126">Cmdlet „Test-AzNetworkWatcherConnectivity“ aktualisiert, Protokollwert wird jetzt an Back-End übergeben.</span><span class="sxs-lookup"><span data-stu-id="86269-2126">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="86269-2127">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-2127">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="86269-2128">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86269-2128">Az.Resources</span></span>
* <span data-ttu-id="86269-2129">Problem behoben, aufgrund dessen „Get-AzRoleDefinition“ eine unverständliche Ausnahme auslöst (wenn das Standardprofil kein Abonnement enthält und kein Bereich festgelegt ist), indem im Szenario eine aussagekräftige Ausnahme hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="86269-2129">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="86269-2130">Außerdem wurde der Standardparametersatz auf „RoleDefinitionNameParameterSet“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="86269-2130">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="86269-2131">0.3.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="86269-2131">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="86269-2132">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="86269-2132">Azure.Storage</span></span>
* <span data-ttu-id="86269-2133">Fehler beim Kopieren von Blobs/Dateien behoben, aufgrund dessen bei einem Metadatenproblem des Ziels keine Metadaten kopiert wurden</span><span class="sxs-lookup"><span data-stu-id="86269-2133">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="86269-2134">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="86269-2134">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="86269-2135">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="86269-2135">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="86269-2136">Der Abruf der Speicherressourcennutzung eines bestimmten Standorts wird jetzt unterstützt, und das Hinzufügen einer Warnmeldung für den Abruf der globalen Speicherressourcennutzung ist überflüssig.</span><span class="sxs-lookup"><span data-stu-id="86269-2136">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="86269-2137">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="86269-2137">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="86269-2138">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="86269-2138">Az.CognitiveServices</span></span>
* <span data-ttu-id="86269-2139">„Get-AzCognitiveServicesAccountSkus“ wird ohne vorhandenes Konto unterstützt.</span><span class="sxs-lookup"><span data-stu-id="86269-2139">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="86269-2140">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="86269-2140">Az.Compute</span></span>
* <span data-ttu-id="86269-2141">Korrektur von „Get-AzVM -ResourceGroupName <rg>“, sodass ggf. mehr als 50 Ergebnisse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="86269-2141">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="86269-2142">Der Cmdlet-Hilfe zu „New-AzVmss“ wurde ein Beispiel für „SimpleParameterSet“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-2142">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="86269-2143">Tippfehler in der Azure Disk Encryption-Statusmeldung behoben</span><span class="sxs-lookup"><span data-stu-id="86269-2143">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="86269-2144">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="86269-2144">Az.DataFactoryV2</span></span>
* <span data-ttu-id="86269-2145">Die Version des ADF .Net-SDK wurde auf 2.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="86269-2145">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="86269-2146">Az.Network</span><span class="sxs-lookup"><span data-stu-id="86269-2146">Az.Network</span></span>
* <span data-ttu-id="86269-2147">NetworkProfile-Funktionalität wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="86269-2147">Added NetworkProfile functionality.</span></span> <span data-ttu-id="86269-2148">Neue Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-2148">new cmdlets added</span></span>
    - <span data-ttu-id="86269-2149">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="86269-2149">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="86269-2150">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="86269-2150">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="86269-2151">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="86269-2151">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="86269-2152">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="86269-2152">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="86269-2153">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="86269-2153">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="86269-2154">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="86269-2154">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="86269-2155">Dienstzuordnungslink in Subnetzmodell hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-2155">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="86269-2156">Cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-2156">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="86269-2157">Cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-2157">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="86269-2158">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="86269-2158">Az.RedisCache</span></span>
* <span data-ttu-id="86269-2159">Künftig sind beliebige Zeichenfolgen als Größenparameter zulässig.</span><span class="sxs-lookup"><span data-stu-id="86269-2159">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="86269-2160">P5 in Popup „PSArgumentCompleter“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-2160">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="86269-2161">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="86269-2161">Az.Resources</span></span>
* <span data-ttu-id="86269-2162">Fehlender Parameter „-Mode“ zu „Set-AzPolicyDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="86269-2162">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="86269-2163">Cmdlet-Fehler bei „Get-AzProviderOperation“ für Vorgänge mit Ursprung behoben, der den Benutzer enthält</span><span class="sxs-lookup"><span data-stu-id="86269-2163">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="86269-2164">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="86269-2164">Az.Sql</span></span>
* <span data-ttu-id="86269-2165">Problem behoben, aufgrund dessen einige Sicherungs-Cmdlets das aktuelle Azure-Abonnements nicht erkannt haben</span><span class="sxs-lookup"><span data-stu-id="86269-2165">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="86269-2166">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="86269-2166">Az.Websites</span></span>
* <span data-ttu-id="86269-2167">Neues Cmdlet „Get-AzWebAppContainerContinuousDeploymentUrl“ zum Abrufen der Webhook-URL von Continuous Deployment für Container</span><span class="sxs-lookup"><span data-stu-id="86269-2167">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="86269-2168">Neue Cmdlets „New-AzWebAppContainerPSSession“ und „Enter-WebAppContainerPSSession“ zum Initiieren einer PowerShell-Remotesitzung in einer Windows-Container-App</span><span class="sxs-lookup"><span data-stu-id="86269-2168">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="86269-2169">0.2.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="86269-2169">0.2.0 - September 2018</span></span>
 <span data-ttu-id="86269-2170">Erstrelease</span><span class="sxs-lookup"><span data-stu-id="86269-2170">Initial Release</span></span>
