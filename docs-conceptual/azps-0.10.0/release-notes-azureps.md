---
title: Versionshinweise zu Azure PowerShell
description: Hier erfahren Sie mehr über die aktuellen Updates für die Azure PowerShell-Module.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 2e824dbbf593e0da9a2a8735aaa094b1944e306c
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2020
ms.locfileid: "93408869"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="7ad68-103">Versionshinweise zu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="7ad68-103">Azure PowerShell release notes</span></span>
## <a name="0100-preview---april-2020"></a><span data-ttu-id="7ad68-104">0.10.0-preview: April 2020</span><span class="sxs-lookup"><span data-stu-id="7ad68-104">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="7ad68-105">Allgemein</span><span class="sxs-lookup"><span data-stu-id="7ad68-105">General</span></span>
* <span data-ttu-id="7ad68-106">Az-Module sind nun als Vorschauversionen in Azure Stack Hub verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7ad68-106">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="7ad68-107">Dies ermöglicht eine plattformübergreifende Kompatibilität mit Linux und macOs.</span><span class="sxs-lookup"><span data-stu-id="7ad68-107">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="7ad68-108">Azure Stack Hub unterstützt jetzt PowerShell Core mit den Az-Modulen. Weitere Informationen finden Sie [hier](https://aka.ms/az4AzureStack).</span><span class="sxs-lookup"><span data-stu-id="7ad68-108">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="7ad68-109">Az-Module unterstützen das Supportprofil 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="7ad68-109">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="7ad68-110">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="7ad68-110">Az.Billing</span></span>
  - <span data-ttu-id="7ad68-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ad68-111">Az.Compute</span></span>
  - <span data-ttu-id="7ad68-112">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="7ad68-112">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="7ad68-113">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7ad68-113">Az.EventHub</span></span>
  - <span data-ttu-id="7ad68-114">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7ad68-114">Az.IotHub</span></span>
  - <span data-ttu-id="7ad68-115">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7ad68-115">Az.KeyVault</span></span>
  - <span data-ttu-id="7ad68-116">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7ad68-116">Az.Monitor</span></span>
  - <span data-ttu-id="7ad68-117">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ad68-117">Az.Network</span></span>
  - <span data-ttu-id="7ad68-118">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ad68-118">Az.Resources</span></span>
  - <span data-ttu-id="7ad68-119">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ad68-119">Az.Storage</span></span>
  - <span data-ttu-id="7ad68-120">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ad68-120">Az.Websites</span></span>
* <span data-ttu-id="7ad68-121">Für Az wurden neue PowerShell-Module (Az.Databox, Az.IotHub und Az.EventHub) eingeführt, die mit Azure Stack Hub verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="7ad68-121">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="7ad68-122">Die Befehle bleiben ungefähr gleich und enthalten nur minimale Änderungen. Beispielsweise wird „AzureRM“ in „Az“ geändert.</span><span class="sxs-lookup"><span data-stu-id="7ad68-122">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="7ad68-123">Den aktualisierten Link zur PowerShell-Dokumentation für Azure Stack Hub finden Sie [hier](https://aka.ms/InstallASHPowerShell).</span><span class="sxs-lookup"><span data-stu-id="7ad68-123">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7ad68-124">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ad68-124">Az.Accounts</span></span>
* <span data-ttu-id="7ad68-125">Upgrade von ADAL auf MSAL</span><span class="sxs-lookup"><span data-stu-id="7ad68-125">Upgrade from ADAL to MSAL</span></span>


## <a name="370---march-2020"></a><span data-ttu-id="7ad68-126">3.7.0: März 2020</span><span class="sxs-lookup"><span data-stu-id="7ad68-126">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7ad68-127">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ad68-127">Az.Accounts</span></span>
* <span data-ttu-id="7ad68-128">„Get-AzTenant“/„Get-AzDefault“/„Set-AzDefault“: Bei fehlender Anmeldung ausgelöste Ausnahme „NullReferenceException“ korrigiert [Nr. 10292]</span><span class="sxs-lookup"><span data-stu-id="7ad68-128">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ad68-129">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ad68-129">Az.Compute</span></span>
* <span data-ttu-id="7ad68-130">Folgende Parameter zum Cmdlet „New-AzDiskConfig“ hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="7ad68-130">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="7ad68-131">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="7ad68-131">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="7ad68-132">Verschlüsselungseigenschaft für Zielparameter des Cmdlets „New-AzGalleryImageVersion“ zugelassen</span><span class="sxs-lookup"><span data-stu-id="7ad68-132">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="7ad68-133">Problem „tempDisk“ für Cmdlets „Set-AzVmss' -Reimage“ und „Invoke-AzVMReimage“ behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-133">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="7ad68-134">[Nr. 11354]</span><span class="sxs-lookup"><span data-stu-id="7ad68-134">[#11354]</span></span>
* <span data-ttu-id="7ad68-135">Unterstützung für die folgenden Cmdlets für die neue SAP-Erweiterung hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="7ad68-135">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="7ad68-136">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="7ad68-136">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="7ad68-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="7ad68-137">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="7ad68-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="7ad68-138">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="7ad68-139">Update-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="7ad68-139">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="7ad68-140">Fehler in Beispielen im Hilfedokument korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-140">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="7ad68-141">Der genaue Zeichenfolgenwert für den VM-Energiezustand (PowerState) wurde im Tabellenformat angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-141">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="7ad68-142">New-AzVmssConfig: Serialisierung der Eigenschaft „AutomaticRepairs“ korrigiert, wenn „SinglePlacementGroup“d deaktiviert ist</span><span class="sxs-lookup"><span data-stu-id="7ad68-142">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="7ad68-143">[Nr. 11257]</span><span class="sxs-lookup"><span data-stu-id="7ad68-143">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7ad68-144">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7ad68-144">Az.DataFactory</span></span>
* <span data-ttu-id="7ad68-145">Version des ADF .NET SDK auf 4.8.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-145">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="7ad68-146">Optionale Parameter zum Befehl „Invoke-AzDataFactoryV2Pipeline“ zur Unterstützung der erneuten Ausführung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-146">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7ad68-147">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7ad68-147">Az.DataLakeStore</span></span>
* <span data-ttu-id="7ad68-148">Breaking Change-Beschreibung für „Export-AzDataLakeStoreItem“ und „Import-AzDataLakeStoreItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-148">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="7ad68-149">Option zur Bytecodierung für „New-AzDataLakeStoreItem“, „Add-AzDAtaLakeStoreItemContent“ und „Get-AzDAtaLakeStoreItemContent“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-149">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7ad68-150">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7ad68-150">Az.HDInsight</span></span>
* <span data-ttu-id="7ad68-151">Angabe der mindestens unterstützten TLS-Version bei Clustererstellung unterstützt</span><span class="sxs-lookup"><span data-stu-id="7ad68-151">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7ad68-152">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7ad68-152">Az.IotHub</span></span>
* <span data-ttu-id="7ad68-153">Unterstützung für die Verwaltung verteilter Einstellungen pro Gerät hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-153">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="7ad68-154">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="7ad68-154">New Cmdlets are:</span></span>
    - <span data-ttu-id="7ad68-155">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="7ad68-155">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="7ad68-156">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="7ad68-156">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7ad68-157">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7ad68-157">Az.KeyVault</span></span>
* <span data-ttu-id="7ad68-158">Breaking Change-Attribute zu „New-AzKeyVault“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-158">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7ad68-159">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7ad68-159">Az.Monitor</span></span>
* <span data-ttu-id="7ad68-160">Dokumentation für „New-AzScheduledQueryRuleLogMetricTrigger“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-160">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ad68-161">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ad68-161">Az.Network</span></span>
* <span data-ttu-id="7ad68-162">Cmdlets aktualisiert, um mandantenübergreifende VNET-Verbindungen virtueller Hubs (VirtualHubVnetConnections) zuzulassen</span><span class="sxs-lookup"><span data-stu-id="7ad68-162">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="7ad68-163">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="7ad68-163">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="7ad68-164">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="7ad68-164">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="7ad68-165">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="7ad68-165">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="7ad68-166">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="7ad68-166">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="7ad68-167">Abhängigkeit vom SQL Management SDK entfernt</span><span class="sxs-lookup"><span data-stu-id="7ad68-167">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7ad68-168">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7ad68-168">Az.PolicyInsights</span></span>
* <span data-ttu-id="7ad68-169">Verbesserte Fehlermeldungen</span><span class="sxs-lookup"><span data-stu-id="7ad68-169">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7ad68-170">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7ad68-170">Az.RecoveryServices</span></span>
* <span data-ttu-id="7ad68-171">Azure Site Recovery: Unterstützung für erneutes Schützen hinzugefügt und VM-Eigenschaften für VMs mit Azure-Datenträgerverschlüsselung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-171">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="7ad68-172">Überwachung der Notfallwiederherstellung für VmwareToAzure-Eigenschaften von Azure Site Recovery hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-172">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="7ad68-173">Azure Backup: Unterstützung für die Wiederholung des Richtlinienupdates für fehlerhafte Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-173">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="7ad68-174">Azure Backup: Unterstützung für Einstellungen für den Ausschluss von Datenträgern während der Sicherung und Wiederherstellung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-174">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="7ad68-175">Azure Backup: Unterstützung für die Wiederherstellung mehrerer Dateien/Ordner in AzureFileShare hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-175">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="7ad68-176">Azure Backup: Unterstützung für vom Benutzer angegebene Ressourcengruppe beim Aktualisieren der IaasVM-Richtlinie hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-176">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ad68-177">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ad68-177">Az.Resources</span></span>
* <span data-ttu-id="7ad68-178">„Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType“ korrigiert, sodass die tatsächliche API-Version (apiVersion) von Ressourcen anstelle der API-Standardversion verwendet wird [Nr. 11267]</span><span class="sxs-lookup"><span data-stu-id="7ad68-178">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="7ad68-179">Protokollierung von „correlationId“ für Fehlerszenarien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-179">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="7ad68-180">Kleine Änderung an der Dokumentation für „Get-AzResourceLock“</span><span class="sxs-lookup"><span data-stu-id="7ad68-180">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="7ad68-181">Beispiel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-181">Added example.</span></span>
* <span data-ttu-id="7ad68-182">Einfaches Anführungszeichen im Parameterwert „Get-AzADUser“ mit Escapezeichen versehen [Nr. 11317]</span><span class="sxs-lookup"><span data-stu-id="7ad68-182">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="7ad68-183">Neue Cmdlets für Bereitstellungsskripts (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-183">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ad68-184">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ad68-184">Az.Sql</span></span>
* <span data-ttu-id="7ad68-185">Lesbarer sekundärer Parameter zu „Invoke-AzSqlDatabaseFailover“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-185">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="7ad68-186">Cmdlet „Disable-AzSqlServerActiveDirectoryOnlyAuthentication“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-186">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="7ad68-187">Vertraulichkeitsrang beim Klassifizieren von Spalten in der Datenbank gespeichert</span><span class="sxs-lookup"><span data-stu-id="7ad68-187">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="7ad68-188">Az.Support</span><span class="sxs-lookup"><span data-stu-id="7ad68-188">Az.Support</span></span>
* <span data-ttu-id="7ad68-189">Allgemeine Verfügbarkeit des Moduls „Az.Support“</span><span class="sxs-lookup"><span data-stu-id="7ad68-189">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7ad68-190">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ad68-190">Az.Websites</span></span>
* <span data-ttu-id="7ad68-191">Unterstützung für das Arbeiten mit Datenverkehrs-Routingregeln für Web-Apps über die folgenden neuen Cmdlets hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="7ad68-191">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="7ad68-192">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="7ad68-192">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="7ad68-193">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="7ad68-193">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="7ad68-194">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="7ad68-194">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="7ad68-195">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="7ad68-195">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="7ad68-196">3.6.1 – März 2020</span><span class="sxs-lookup"><span data-stu-id="7ad68-196">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7ad68-197">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ad68-197">Az.Accounts</span></span>
* <span data-ttu-id="7ad68-198">Öffnen der Azure PowerShell-Umfrageseite in „Send-Feedback“ [#11020]</span><span class="sxs-lookup"><span data-stu-id="7ad68-198">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="7ad68-199">Anzeigen der Azure PowerShell-Umfrage-URL in „Resolve-Error“ [#11021]</span><span class="sxs-lookup"><span data-stu-id="7ad68-199">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="7ad68-200">Az-Version in UserAgent hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-200">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7ad68-201">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7ad68-201">Az.ApiManagement</span></span>
* <span data-ttu-id="7ad68-202">Unterstützung für das Abrufen und Konfigurieren einer benutzerdefinierten Domäne auf dem DeveloperPortal-Endpunkt hinzugefügt [#11007]</span><span class="sxs-lookup"><span data-stu-id="7ad68-202">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="7ad68-203">„Export-AzApiManagementApi“: Unterstützung für das Herunterladen der API-Definition im JSON-Format hinzugefügt [#9987]</span><span class="sxs-lookup"><span data-stu-id="7ad68-203">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="7ad68-204">„Import-AzApiManagementApi“: Unterstützung für das Importieren der OpenApi 3.0-Definition aus JSON-Dokument hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-204">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="7ad68-205">„New-AzApiManagementIdentityProvider“ und „Set-AzApiManagementIdentityProvider“: Unterstützung für das Konfigurieren des Anmeldemandanten für AAD B2C-Anbieter hinzugefügt [#9784]</span><span class="sxs-lookup"><span data-stu-id="7ad68-205">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7ad68-206">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7ad68-206">Az.DataLakeStore</span></span>
* <span data-ttu-id="7ad68-207">Verweis auf System.Buffers in csproj und psd1 explizit hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-207">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7ad68-208">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7ad68-208">Az.IotHub</span></span>
* <span data-ttu-id="7ad68-209">Unterstützung für die Verwaltung von Geräten in IoT Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-209">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="7ad68-210">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="7ad68-210">New Cmdlets are:</span></span>
    - <span data-ttu-id="7ad68-211">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="7ad68-211">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="7ad68-212">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="7ad68-212">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="7ad68-213">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="7ad68-213">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="7ad68-214">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="7ad68-214">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="7ad68-215">Unterstützung für die Verwaltung von Modulen auf einem IoT-Zielgerät in einem IoT-Hub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-215">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="7ad68-216">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="7ad68-216">New Cmdlets are:</span></span>
    - <span data-ttu-id="7ad68-217">„Add-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="7ad68-217">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="7ad68-218">„Get-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="7ad68-218">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="7ad68-219">„Remove-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="7ad68-219">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="7ad68-220">„Set-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="7ad68-220">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="7ad68-221">Cmdlet zum Abrufen der Verbindungszeichenfolge eines IoT-Zielgeräts in einem IoT-Hub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-221">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="7ad68-222">Cmdlet zum Abrufen der Verbindungszeichenfolge eines Moduls auf einem IoT-Zielgerät in einem IoT-Hub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-222">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="7ad68-223">Unterstützung für das Abrufen/Festlegen des übergeordneten Geräts eines IoT-Geräts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-223">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="7ad68-224">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="7ad68-224">New Cmdlets are:</span></span>
    - <span data-ttu-id="7ad68-225">„Get-AzIotHubDeviceParent“</span><span class="sxs-lookup"><span data-stu-id="7ad68-225">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="7ad68-226">„Set-AzIotHubDeviceParent“</span><span class="sxs-lookup"><span data-stu-id="7ad68-226">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="7ad68-227">Unterstützung für die Verwaltung der Beziehung zwischen über- und untergeordneten Geräten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-227">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7ad68-228">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7ad68-228">Az.Monitor</span></span>
* <span data-ttu-id="7ad68-229">Ausgabewert für „Get-AzMetricDefinition“ korrigiert [#9714]</span><span class="sxs-lookup"><span data-stu-id="7ad68-229">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ad68-230">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ad68-230">Az.Network</span></span>
* <span data-ttu-id="7ad68-231">SQL Management SDK aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7ad68-231">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="7ad68-232">Es wurde ein Problem mit dem Namensunterschied in der PrivateLinkServiceConnectionState-Klasse behoben.</span><span class="sxs-lookup"><span data-stu-id="7ad68-232">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="7ad68-233">Zuordnung des Felds „ActionsRequired“ zu „ActionRequired“.</span><span class="sxs-lookup"><span data-stu-id="7ad68-233">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="7ad68-234">PublicNetworkAccess zu „New-AzSqlServer“ und „Set-AzSqlServer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-234">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ad68-235">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ad68-235">Az.Resources</span></span>
* <span data-ttu-id="7ad68-236">Für Nullverweisfehler in „Get-AzRoleAssignment“ behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-236">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="7ad68-237">Switch „-Force“ und „-PassThru“ in „Remove-AzADGroup“ als optional gekennzeichnet [#10849]</span><span class="sxs-lookup"><span data-stu-id="7ad68-237">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="7ad68-238">Problem behoben, dass „MailNickname“ nicht zurückgegeben wird, in „Remove-AzADGroup“ behoben [#11167]</span><span class="sxs-lookup"><span data-stu-id="7ad68-238">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="7ad68-239">Problem behoben, dass Pipe-Vorgang „Remove-AzADGroup“ nicht funktioniert [#11171]</span><span class="sxs-lookup"><span data-stu-id="7ad68-239">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="7ad68-240">Für Nullverweisfehler in GetAzureRoleAssignmentCommand behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-240">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="7ad68-241">Breaking Change-Attribute für bevorstehende Änderungen an Richtlinien-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-241">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="7ad68-242">„Get-AzResourceGroup“ aktualisiert, sodass jetzt serverseitig nach Ressourcengruppentags gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="7ad68-242">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="7ad68-243">Tag-Cmdlets so erweitert, dass „-ResourceId“ akzeptiert wird</span><span class="sxs-lookup"><span data-stu-id="7ad68-243">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="7ad68-244">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ad68-244">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="7ad68-245">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ad68-245">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="7ad68-246">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ad68-246">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="7ad68-247">Neues Tag-Cmdlet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-247">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="7ad68-248">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ad68-248">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="7ad68-249">ScopedDeployment aus SDK 3.3.0 übernommen</span><span class="sxs-lookup"><span data-stu-id="7ad68-249">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ad68-250">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ad68-250">Az.Sql</span></span>
* <span data-ttu-id="7ad68-251">Publicnetworkaccess wurde "New-azsqlserver" und "Set-azsqlserver" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-251">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="7ad68-252">Unterstützung für die Konfiguration der Sicherung der Langzeitaufbewahrung für verwaltete Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-252">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="7ad68-253">Einrichten/Festlegen der LTR-Richtlinie für eine verwaltete Datenbank</span><span class="sxs-lookup"><span data-stu-id="7ad68-253">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="7ad68-254">Abrufen von Sicherungen nach verwalteter Datenbank, verwalteter Instanz oder nach Speicherort</span><span class="sxs-lookup"><span data-stu-id="7ad68-254">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="7ad68-255">Entfernen einer LTR-Sicherung</span><span class="sxs-lookup"><span data-stu-id="7ad68-255">Remove an LTR backup</span></span>
    - <span data-ttu-id="7ad68-256">Wiederherstellen einer LTR-Sicherung zum Erstellen einer neuen verwalteten Datenbank</span><span class="sxs-lookup"><span data-stu-id="7ad68-256">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="7ad68-257">MinimalTlsVersion wurde zu New-AzSqlServer und Set-AzSqlServer hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-257">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="7ad68-258">MinimalTlsVersion wurde zu New-AzSqlInstance und Set-AzSqlInstance hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-258">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="7ad68-259">SQL SDK-Version für Az.Network festgelegt</span><span class="sxs-lookup"><span data-stu-id="7ad68-259">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7ad68-260">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ad68-260">Az.Storage</span></span>
* <span data-ttu-id="7ad68-261">Unterstützung von AllowProtectedAppendWrite in ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="7ad68-261">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="7ad68-262">„Set-AzRmStorageContainerImmutabilityPolicy“</span><span class="sxs-lookup"><span data-stu-id="7ad68-262">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="7ad68-263">Warnmeldung für Breaking Change hinzugefügt: Typänderung für „AzureStorageTable“ in einer zukünftigen Version</span><span class="sxs-lookup"><span data-stu-id="7ad68-263">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="7ad68-264">„New-AzStorageTable“</span><span class="sxs-lookup"><span data-stu-id="7ad68-264">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="7ad68-265">„Get-AzStorageTable“</span><span class="sxs-lookup"><span data-stu-id="7ad68-265">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7ad68-266">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ad68-266">Az.Websites</span></span>
* <span data-ttu-id="7ad68-267">Tag-Parameter für „New-AzAppServicePlan“ und „Set-AzAppServicePlan“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-267">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="7ad68-268">Beenden der Cmdlet-Ausführung, wenn beim Hinzufügen einer benutzerdefinierten Domäne zu einer Website eine Ausnahme ausgelöst wird</span><span class="sxs-lookup"><span data-stu-id="7ad68-268">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="7ad68-269">Unterstützung zur Durchführung von Vorgängen für App Services hinzugefügt, die sich nicht in der gleichen Ressourcengruppe wie der App Service-Plan befinden</span><span class="sxs-lookup"><span data-stu-id="7ad68-269">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="7ad68-270">Zugriffseinschränkung auf WebApp/Funktion in verschiedenen Ressourcengruppen angewendet</span><span class="sxs-lookup"><span data-stu-id="7ad68-270">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="7ad68-271">Problem beim Festlegen von benutzerdefinierten Hostnamen für WebAppSlots behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-271">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="7ad68-272">3.5.0: Februar 2020</span><span class="sxs-lookup"><span data-stu-id="7ad68-272">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7ad68-273">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="7ad68-273">Highlights since the last major release</span></span>
* <span data-ttu-id="7ad68-274">Clientseitige Telemetrie aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-274">Updated client side telemetry.</span></span>
* <span data-ttu-id="7ad68-275">Cmdlets zur Unterstützung der Geräteverwaltung in Az.IotHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-275">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="7ad68-276">Cmdlets für Verfügbarkeitsgruppenlistener in Az.SqlVirtualMachine hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-276">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7ad68-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ad68-277">Az.Accounts</span></span>
* <span data-ttu-id="7ad68-278">Abonnement-ID, Mandanten-ID und Ausführungszeit in clientseitigen Telemetriedaten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-278">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7ad68-279">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7ad68-279">Az.Automation</span></span>
* <span data-ttu-id="7ad68-280">Tippfehler in Beispiel 1 in der Referenzdokumentation für „New-AzAutomationSoftwareUpdateConfiguration“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-280">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7ad68-281">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7ad68-281">Az.CognitiveServices</span></span>
* <span data-ttu-id="7ad68-282">SDK auf 7.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-282">Updated SDK to 7.0</span></span>
* <span data-ttu-id="7ad68-283">Verbesserte Fehlermeldung, wenn der Server mit leerem Text antwortet</span><span class="sxs-lookup"><span data-stu-id="7ad68-283">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ad68-284">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ad68-284">Az.Compute</span></span>
* <span data-ttu-id="7ad68-285">Zulässiger leerer Wert für „ProximityPlacementGroupId“ während des Updates</span><span class="sxs-lookup"><span data-stu-id="7ad68-285">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7ad68-286">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7ad68-286">Az.FrontDoor</span></span>
* <span data-ttu-id="7ad68-287">Cmdlet zum Abrufen verwalteter Regeldefinitionen hinzugefügt, die in WAF verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="7ad68-287">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7ad68-288">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7ad68-288">Az.IotHub</span></span>
* <span data-ttu-id="7ad68-289">Unterstützung für die Verwaltung von Geräten in IoT Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-289">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="7ad68-290">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="7ad68-290">New Cmdlets are:</span></span>
    - <span data-ttu-id="7ad68-291">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="7ad68-291">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="7ad68-292">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="7ad68-292">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="7ad68-293">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="7ad68-293">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="7ad68-294">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="7ad68-294">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7ad68-295">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7ad68-295">Az.KeyVault</span></span>
* <span data-ttu-id="7ad68-296">Duplizierter Text für „Add-AzKeyVaultKey.md“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-296">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7ad68-297">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7ad68-297">Az.Monitor</span></span>
* <span data-ttu-id="7ad68-298">Beschreibung des Cmdlets „Get-AzLog cmdlet“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-298">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="7ad68-299">Dem Befehl „New-AzMetricAlertRuleV2“ wurde ein Parameter namens „ActionGroupId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-299">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="7ad68-300">Der Benutzer kann entweder „ActionGroupId(string)“ oder „ActionGorup(ActivityLogAlertActionGroup)“ angeben.</span><span class="sxs-lookup"><span data-stu-id="7ad68-300">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ad68-301">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ad68-301">Az.Network</span></span>
* <span data-ttu-id="7ad68-302">Zusätzlicher Parameterhinweis für den Parameter „-EnableProxyProtocol“ für das Cmdlet „New-AzPrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-302">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="7ad68-303">FilterData-Beispiel in „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-303">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="7ad68-304">Paketerfassungsbeispiel für die Erfassung aller inneren und äußeren Pakete in „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-304">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="7ad68-305">Unterstützte Azure Firewall-Richtlinie für VNET-Firewalls</span><span class="sxs-lookup"><span data-stu-id="7ad68-305">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="7ad68-306">Keine neuen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-306">No new cmdlets are added.</span></span> <span data-ttu-id="7ad68-307">Die Einschränkung für die Firewallrichtlinie für VNET-Firewalls wurde gelockert.</span><span class="sxs-lookup"><span data-stu-id="7ad68-307">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7ad68-308">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7ad68-308">Az.RecoveryServices</span></span>
* <span data-ttu-id="7ad68-309">Unterstützung für „Als Dateien wiederherstellen“ für SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-309">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ad68-310">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ad68-310">Az.Resources</span></span>
* <span data-ttu-id="7ad68-311">Cmdlets für die Vorlagenbereitstellung umgestaltet</span><span class="sxs-lookup"><span data-stu-id="7ad68-311">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="7ad68-312">Neue Cmdlets zur Verwaltung von Bereitstellungen in der Verwaltungsgruppe hinzugefügt: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7ad68-312">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="7ad68-313">Neue Cmdlets zur Verwaltung von Bereitstellungen im Mandantenbereich hinzugefügt: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="7ad68-313">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="7ad68-314">Cmdlets vom Typ „\*-AzDeployment“ für den speziellen Einsatz im Abonnementbereich umgestaltet</span><span class="sxs-lookup"><span data-stu-id="7ad68-314">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="7ad68-315">Aliase vom Typ „*-AzSubscriptionDeployment“ für Cmdlets vom Typ „*-AzDeployment“ erstellt</span><span class="sxs-lookup"><span data-stu-id="7ad68-315">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="7ad68-316">„Update-AzADApplication“ korrigiert, wenn der Parameter „AvailableToOtherTenants“ nicht festgelegt wird</span><span class="sxs-lookup"><span data-stu-id="7ad68-316">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="7ad68-317">„ApplicationObjectWithoutCredentialParameterSet“ entfernt, um „AmbiguousParameterSetException“ zu vermeiden</span><span class="sxs-lookup"><span data-stu-id="7ad68-317">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="7ad68-318">Hilfedateien erneut generiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-318">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ad68-319">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ad68-319">Az.Sql</span></span>
* <span data-ttu-id="7ad68-320">Unterstützung für abonnementübergreifende Point-in-Time-Wiederherstellung für verwaltete Instanzen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-320">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="7ad68-321">Unterstützung für die Änderung der Hardwaregeneration von vorhandenen verwalteten SQL-Instanzen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-321">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="7ad68-322">Hilfebeispiele für „Update-AzSqlServerVulnerabilityAssessmentSetting“ korrigiert: parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="7ad68-322">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="7ad68-323">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7ad68-323">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="7ad68-324">Cmdlets für Verfügbarkeitsgruppenlistener hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-324">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7ad68-325">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7ad68-325">Az.StorageSync</span></span>
* <span data-ttu-id="7ad68-326">Unterstützte Zeichensätze in „Invoke-AzStorageSyncCompatibilityCheck“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-326">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="7ad68-327">3.4.0: Februar 2020</span><span class="sxs-lookup"><span data-stu-id="7ad68-327">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7ad68-328">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="7ad68-328">Highlights since the last major release</span></span>
* <span data-ttu-id="7ad68-329">Az.CosmosDB: erste Version 0.1.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="7ad68-329">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="7ad68-330">Unterstützung für Az.Network ConnectionMonitor V2 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-330">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7ad68-331">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ad68-331">Az.Accounts</span></span>
* <span data-ttu-id="7ad68-332">Deaktivieren der automatischen Kontextspeicherung, wenn „AzureRmContext.json“ nicht verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="7ad68-332">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="7ad68-333">Aktualisieren des Verweises auf Azure Powershell Common auf 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="7ad68-333">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7ad68-334">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7ad68-334">Az.ApiManagement</span></span>
* <span data-ttu-id="7ad68-335">**Get-AzApiManagementApiSchema** Fehler beim Abrufen des einer API zugeordneten Open-Api-Schemas behoben   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="7ad68-335">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="7ad68-336">**New-AzApiManagementProduct** _ und _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="7ad68-336">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="7ad68-337">Dokumentation korrigiert für https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="7ad68-337">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="7ad68-338">**Set-AzApiManagementApi** Beispiel hinzugefügt, das das Aktualisieren von ServiceUrl mithilfe des Cmdlets veranschaulicht</span><span class="sxs-lookup"><span data-stu-id="7ad68-338">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ad68-339">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ad68-339">Az.Compute</span></span>
* <span data-ttu-id="7ad68-340">Anzahl des VM-Status auf 100 beschränkt, um die Drosselung zu vermeiden, wenn „Get-AzVM -Status“ ohne VM-Name ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="7ad68-340">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="7ad68-341">Cmdlet „Update-AzDiskEncryptionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-341">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="7ad68-342">Die Parameter „EncryptionType“ und „DiskEncryptionSetId“ wurden den folgenden Cmdlets hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="7ad68-342">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="7ad68-343">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="7ad68-343">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="7ad68-344">Parameter „ColocationStatus“ zum Cmdlet „Get-AzProximityPlacementGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-344">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7ad68-345">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7ad68-345">Az.DataFactory</span></span>
* <span data-ttu-id="7ad68-346">Version des ADF .NET SDK auf 4.7.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-346">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="7ad68-347">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="7ad68-347">Az.DeploymentManager</span></span>
* <span data-ttu-id="7ad68-348">LIST-Vorgänge für Ressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-348">Adds LIST operations for resources</span></span>
* <span data-ttu-id="7ad68-349">Funktionen zum Ausführen von Vorgängen für Integritätsprüfungsschritte hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-349">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7ad68-350">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7ad68-350">Az.HDInsight</span></span>
* <span data-ttu-id="7ad68-351">Dokumentationsfehler für „New-AzHDInsightCluster“ behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-351">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7ad68-352">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7ad68-352">Az.KeyVault</span></span>
* <span data-ttu-id="7ad68-353">Namensalias zum VaultName-Attribut hinzugefügt, um „Remove-AzureKeyVault“ mit „New-AzureKeyVault“ konsistent zu machen</span><span class="sxs-lookup"><span data-stu-id="7ad68-353">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ad68-354">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ad68-354">Az.Network</span></span>
* <span data-ttu-id="7ad68-355">Neues Beispiel zu „Set-AzNetworkWatcherConfigFlowLog.md“ hinzugefügt, um das Szenario zur Traffic Analytics-Deaktivierung zu veranschaulichen</span><span class="sxs-lookup"><span data-stu-id="7ad68-355">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="7ad68-356">Unterstützung für die Zuweisung der IP-Verwaltungskonfiguration zu Azure Firewall hinzugefügt: ein dediziertes Subnetz und eine öffentliche IP-Adresse, die von der Firewall für den Verwaltungsdatenverkehr verwendet werden</span><span class="sxs-lookup"><span data-stu-id="7ad68-356">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="7ad68-357">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="7ad68-357">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="7ad68-358">Parameter „-ManagementPublicIpAddress“ (nicht obligatorisch) hinzugefügt, der ein Objekt für die öffentliche IP-Adresse akzeptiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-358">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="7ad68-359">Methode „SetManagementIpConfiguration“ für Firewallobjekt hinzugefügt. Erfordert ein Subnetz und eine öffentliche IP-Adresse als Eingabe, und der Subnetzname muss „AzureFirewallManagementSubnet“ lauten.</span><span class="sxs-lookup"><span data-stu-id="7ad68-359">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="7ad68-360">Beispiele für „Get-AzNetworkSecurityGroup“ korrigiert, um Beispiele für Netzwerksicherheitsgruppen und nicht für Netzwerkschnittstellen anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="7ad68-360">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="7ad68-361">Tippfehler im Befehl „New-AzVpnSite“ korrigiert, der dazu führte, dass die Vervollständigung für die Ressourcen-ID einen Parameter nicht vervollständigen konnte</span><span class="sxs-lookup"><span data-stu-id="7ad68-361">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="7ad68-362">Unterstützung für die URL-Konfiguration im Aktionssatz für Neuschreibungsregeln in Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-362">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="7ad68-363">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7ad68-363">New cmdlets added:</span></span>
        - <span data-ttu-id="7ad68-364">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ad68-364">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="7ad68-365">Cmdlets mit optionalem Parameter aktualisiert: UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ad68-365">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="7ad68-366">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="7ad68-366">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="7ad68-367">Unterstützung für Ressourcen der Version 2 von NetworkWatcher ConnectionMonitor hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-367">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7ad68-368">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7ad68-368">Az.PolicyInsights</span></span>
* <span data-ttu-id="7ad68-369">Unterstützung der Konformitätsbewertung vor der Ermittlung der zu korrigierenden Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7ad68-369">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="7ad68-370">Parameter „-ResourceDiscoverMode“ zu „Start-AzPolicyRemediation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-370">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="7ad68-371">Cmdlet „Get-AzPolicyMetadata“ zum Abrufen der Ressourcen für Richtlinienmetadaten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-371">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="7ad68-372">„Get-AzPolicyState“ und „Get-AzPolicyStateSummary“ für API-Version 2019-10-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-372">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7ad68-373">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7ad68-373">Az.RecoveryServices</span></span>
* <span data-ttu-id="7ad68-374">Azure Site Recovery-Unterstützung für das Entfernen eines replizierten Datenträgers</span><span class="sxs-lookup"><span data-stu-id="7ad68-374">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="7ad68-375">In Azure Backup wurde Unterstützung zum Hinzufügen von Tags bei der Erstellung eines Recovery Services-Tresors hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-375">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ad68-376">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ad68-376">Az.Resources</span></span>
* <span data-ttu-id="7ad68-377">„-Scope“ in Cmdlets vom Typ „\*-AzPolicyAssignment“ nun optional (standardmäßig auf Abonnementkontext festgelegt)</span><span class="sxs-lookup"><span data-stu-id="7ad68-377">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="7ad68-378">Beispiele zum Erstellen von „ADServicePrincipal“ mit Kennwort und Schlüsselanmeldeinformation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-378">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ad68-379">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ad68-379">Az.Sql</span></span>
<span data-ttu-id="7ad68-380">Cmdlet „New-AzSqlDatabaseSecondary“ korrigiert, um auf die Existenz von „PartnerDatabaseName“ anstelle von „DatabaseName“ zu prüfen</span><span class="sxs-lookup"><span data-stu-id="7ad68-380">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7ad68-381">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ad68-381">Az.Storage</span></span>
* <span data-ttu-id="7ad68-382">Unterstützung für das Festlegen des Schlüsseltyps für die Tabellen-/Warteschlangenverschlüsselung beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="7ad68-382">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="7ad68-383">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ad68-383">New-AzStorageAccount</span></span>
* <span data-ttu-id="7ad68-384">Anzeigen der Anforderungs-ID (RequestId), wenn für „StorageException“ keine erweiterten Fehlerinformationen (ExtendedErrorInformation) vorliegen</span><span class="sxs-lookup"><span data-stu-id="7ad68-384">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="7ad68-385">Beispiel 6 des Cmdlets „Start-AzStorageBlobCopy“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-385">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7ad68-386">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ad68-386">Az.Websites</span></span>
* <span data-ttu-id="7ad68-387">„Set-AzWebapp“ und „Set-AzWebappSlot“ unterstützen die Eigenschaften „AlwaysOn“, „MinTls“ und „FtpsState“.</span><span class="sxs-lookup"><span data-stu-id="7ad68-387">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="7ad68-388">Problem behoben, das dazu führte, dass beim Festlegen von „HttpsOnly“ bei gleichzeitiger Änderung von „AppservicePlan“ mit dem einzelnen Befehl „Set-AzWebApp“ „HttpsOnly“ auf den Standardwert zurückgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="7ad68-388">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="7ad68-389">3.3.0 – Januar 2020</span><span class="sxs-lookup"><span data-stu-id="7ad68-389">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7ad68-390">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ad68-390">Az.Accounts</span></span>
* <span data-ttu-id="7ad68-391">„Add-AzEnvironment“ und „Set-AzEnvironment“ wurden so aktualisiert, dass sie jetzt die Parameter „AzureAttestationServiceEndpointResourceId“ und „AzureAttestationServiceEndpointSuffix“ akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="7ad68-391">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7ad68-392">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7ad68-392">Az.Cdn</span></span>
* <span data-ttu-id="7ad68-393">Anzeigen von Fehlerantwortdetails im Cmdlet „New-AzCdnEndpoint“</span><span class="sxs-lookup"><span data-stu-id="7ad68-393">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ad68-394">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ad68-394">Az.Compute</span></span>
* <span data-ttu-id="7ad68-395">Cmdlet „Set-AzVMCustomScriptExtension“ für eine VM mit verwaltetem Betriebssystemdatenträger ohne Betriebssystemprofil wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="7ad68-395">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="7ad68-396">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7ad68-396">Az.ContainerInstance</span></span>
* <span data-ttu-id="7ad68-397">Im Beispiel von „New-AzContainerGroup“ verwendete Parameternamen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="7ad68-397">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="7ad68-398">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="7ad68-398">Az.DataBoxEdge</span></span>
* <span data-ttu-id="7ad68-399">Cmdlet „Get-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-399">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="7ad68-400">Edge-Speichercontainer abrufen</span><span class="sxs-lookup"><span data-stu-id="7ad68-400">Get the Edge Storage Container</span></span>
* <span data-ttu-id="7ad68-401">Cmdlet „New-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-401">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="7ad68-402">Neuen Edge-Speichercontainer erstellen</span><span class="sxs-lookup"><span data-stu-id="7ad68-402">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="7ad68-403">Cmdlet „Remove-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-403">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="7ad68-404">Edge-Speichercontainer entfernen</span><span class="sxs-lookup"><span data-stu-id="7ad68-404">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="7ad68-405">Cmdlet „Invoke-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-405">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="7ad68-406">Aktion zum Aktualisieren von Daten in Edge-Speichercontainer aufrufen</span><span class="sxs-lookup"><span data-stu-id="7ad68-406">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="7ad68-407">Cmdlet „Get-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-407">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="7ad68-408">Edge-Speicherkonto abrufen</span><span class="sxs-lookup"><span data-stu-id="7ad68-408">Get the Edge Storage Account</span></span>
* <span data-ttu-id="7ad68-409">Cmdlet „New-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-409">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="7ad68-410">Neues Edge-Speicherkonto erstellen</span><span class="sxs-lookup"><span data-stu-id="7ad68-410">Create new Edge Storage Account</span></span>
* <span data-ttu-id="7ad68-411">Cmdlet „Remove-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-411">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="7ad68-412">Edge-Speicherkonto entfernen</span><span class="sxs-lookup"><span data-stu-id="7ad68-412">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="7ad68-413">Cmdlet „Invoke-AzDataBoxEdgeShare“ aufrufen</span><span class="sxs-lookup"><span data-stu-id="7ad68-413">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="7ad68-414">Aktion zum Aktualisieren von Daten auf Freigabe aufrufen</span><span class="sxs-lookup"><span data-stu-id="7ad68-414">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="7ad68-415">Cmdlet „Set-AzDataBoxEdgeStorageAccountCredential“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-415">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="7ad68-416">Festlegen der Speicherkonto-Anmeldeinformationen für „az databoxedge“</span><span class="sxs-lookup"><span data-stu-id="7ad68-416">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7ad68-417">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7ad68-417">Az.DataFactory</span></span>
* <span data-ttu-id="7ad68-418">Eigenschaften „AutoUpdateETA“, „LatestVersion“, „PushedVersion“, „TaskQueueId“ und „VersionStatus“ für Befehl „Get-AzDataFactoryV2IntegrationRuntime“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-418">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="7ad68-419">Version des ADF .NET SDK auf 4.6.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-419">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="7ad68-420">Parameter „PublicIPs“ wurde für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um das Erstellen der Azure-SSIS Integration Runtime mit statischen öffentlichen IP-Adressen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="7ad68-420">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="7ad68-421">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="7ad68-421">Az.DevTestLabs</span></span>
* <span data-ttu-id="7ad68-422">Fehlerhafter Link in „Get-AzDtlAllowedVMSizesPolicy.md“ entfernt</span><span class="sxs-lookup"><span data-stu-id="7ad68-422">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7ad68-423">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7ad68-423">Az.EventHub</span></span>
* <span data-ttu-id="7ad68-424">Behebung des Problems 10634: Verweis auf NULL-Objekt für „remove eventhubnamespace“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-424">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7ad68-425">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7ad68-425">Az.HDInsight</span></span>
* <span data-ttu-id="7ad68-426">Fehler in „Invoke-AzHDInsightHiveJob.md“ wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="7ad68-426">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="7ad68-427">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7ad68-427">Az.MachineLearning</span></span>
* <span data-ttu-id="7ad68-428">Die folgenden Cmdlets wurden entfernt, da „MachineLearningCompute“ nicht mehr verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="7ad68-428">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="7ad68-429">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="7ad68-429">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="7ad68-430">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="7ad68-430">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="7ad68-431">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="7ad68-431">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="7ad68-432">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="7ad68-432">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="7ad68-433">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="7ad68-433">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="7ad68-434">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="7ad68-434">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="7ad68-435">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="7ad68-435">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ad68-436">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ad68-436">Az.Network</span></span>
* <span data-ttu-id="7ad68-437">Upgrade der Abhängigkeit von „Microsoft.Azure.Management.Sql“ von „1.36-preview“ auf „1.37-preview“</span><span class="sxs-lookup"><span data-stu-id="7ad68-437">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7ad68-438">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7ad68-438">Az.RecoveryServices</span></span>
* <span data-ttu-id="7ad68-439">Änderung der Azure Site Recovery-Unterstützung für virtuelle Computer mit verwalteten Datenträgern, die im Ruhezustand mit kundenseitig verwalteten Schlüsseln für Azure-zu-Azure-Anbieter verschlüsselt sind</span><span class="sxs-lookup"><span data-stu-id="7ad68-439">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="7ad68-440">Azure Site Recovery-Unterstützung für die Eingabe der ID des Datenträgerverschlüsselungssatzes als optionale Eingabe beim Aktivieren des Schutzes für VMware in Azure</span><span class="sxs-lookup"><span data-stu-id="7ad68-440">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="7ad68-441">Azure Site Recovery-Unterstützung für die Eingabe der ID des Datenträgerverschlüsselungssatzes als optionale Eingabe auf Datenträgerebene beim Aktivieren des Schutzes für VMware in Azure</span><span class="sxs-lookup"><span data-stu-id="7ad68-441">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="7ad68-442">Azure Site Recovery-Unterstützung zum Aktualisieren eines replikationsgeschützten Elements mit der Zuordnung eines Datenträgerverschlüsselungssatzes für HyperV in Azure</span><span class="sxs-lookup"><span data-stu-id="7ad68-442">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ad68-443">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ad68-443">Az.Resources</span></span>
* <span data-ttu-id="7ad68-444">Fehler in Hilfedokument zu „Remove-AzTag“ behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-444">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ad68-445">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ad68-445">Az.Sql</span></span>
* <span data-ttu-id="7ad68-446">Funktionalität der Baseline-Cmdlets für einen Sicherheitsrisikobewertungssatz korrigiert, sodass sie auf der Master-Datenbank für Azure Database funktionieren und sie auf Systemdatenbanken von verwalteten Instanzen einschränken.</span><span class="sxs-lookup"><span data-stu-id="7ad68-446">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="7ad68-447">Fehler beim Erstellen einer SQL-Instanzfailovergruppe behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-447">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="7ad68-448">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7ad68-448">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="7ad68-449">DR als neuer gültiger Lizenztyp hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-449">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7ad68-450">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ad68-450">Az.Storage</span></span>
* <span data-ttu-id="7ad68-451">Warnmeldung für Breaking Change hinzugefügt: Wertänderung für „DefaultAction“ in einer zukünftigen Version</span><span class="sxs-lookup"><span data-stu-id="7ad68-451">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="7ad68-452">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="7ad68-452">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="7ad68-453">Unterstützung für das Abrufen der letzten Synchronisierungszeit des Speicherkontos durch Ausführen von „get-AzureRMStorageAccount“ mit Parameter „-IncludeGeoReplicationStats“</span><span class="sxs-lookup"><span data-stu-id="7ad68-453">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="7ad68-454">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ad68-454">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="7ad68-455">3.2.0: Dezember 2019</span><span class="sxs-lookup"><span data-stu-id="7ad68-455">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="7ad68-456">Allgemein</span><span class="sxs-lookup"><span data-stu-id="7ad68-456">General</span></span>
* <span data-ttu-id="7ad68-457">Verweise in „.psd1“ zur Verwendung des relativen Pfads für alle Module aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-457">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7ad68-458">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ad68-458">Az.Accounts</span></span>
* <span data-ttu-id="7ad68-459">Richtiges UserAgent-Element für clientseitige Telemetrie für Az 4.0-Vorschauversion festgelegt</span><span class="sxs-lookup"><span data-stu-id="7ad68-459">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="7ad68-460">Anzeigen benutzerfreundlicher Fehlermeldungen, wenn der Kontext in der Az 4.0-Vorschauversion NULL ist</span><span class="sxs-lookup"><span data-stu-id="7ad68-460">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7ad68-461">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7ad68-461">Az.Batch</span></span>
* <span data-ttu-id="7ad68-462">Problem [#10602](https://github.com/Azure/azure-powershell/issues/10602) behoben, aufgrund dessen „VirtualMachineConfiguration.ContainerConfiguration“ oder „VirtualMachineConfiguration.DataDisks“ von **New-AzBatchPool** nicht ordnungsgemäß an den Server gesendet wurde</span><span class="sxs-lookup"><span data-stu-id="7ad68-462">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7ad68-463">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7ad68-463">Az.DataFactory</span></span>
* <span data-ttu-id="7ad68-464">Version des ADF .NET SDK auf 4.5.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-464">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7ad68-465">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7ad68-465">Az.FrontDoor</span></span>
* <span data-ttu-id="7ad68-466">Unterstützung für den Ausschluss verwalteter WAF-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-466">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="7ad68-467">SocketAddr zur automatischen Vervollständigung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-467">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="7ad68-468">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="7ad68-468">Az.HealthcareApis</span></span>
* <span data-ttu-id="7ad68-469">Ausnahmebehandlung</span><span class="sxs-lookup"><span data-stu-id="7ad68-469">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7ad68-470">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7ad68-470">Az.KeyVault</span></span>
* <span data-ttu-id="7ad68-471">Fehler im Zusammenhang mit dem Zugriff auf einen möglicherweise nicht festgelegten Wert behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-471">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="7ad68-472">Zertifikatverwaltung für Kryptografie für elliptische Kurve</span><span class="sxs-lookup"><span data-stu-id="7ad68-472">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="7ad68-473">Unterstützung zum Angeben der Kurve für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-473">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7ad68-474">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7ad68-474">Az.Monitor</span></span>
* <span data-ttu-id="7ad68-475">Optionales Argument zum Befehl „Diagnoseeinstellungen hinzufügen“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-475">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="7ad68-476">Ein Optionsargument, das angibt, dass der Export in Log Analytics ein festes Schema sein muss (auch bekannt als</span><span class="sxs-lookup"><span data-stu-id="7ad68-476">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="7ad68-477">dedizierter Datentyp)</span><span class="sxs-lookup"><span data-stu-id="7ad68-477">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ad68-478">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ad68-478">Az.Network</span></span>
* <span data-ttu-id="7ad68-479">Unterstützung für IpGroups in der AzureFirewall-Anwendung sowie in NAT- und Netzwerkregeln</span><span class="sxs-lookup"><span data-stu-id="7ad68-479">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ad68-480">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ad68-480">Az.Resources</span></span>
* <span data-ttu-id="7ad68-481">Problem behoben, aufgrund dessen die Vorlagenbereitstellung einen Vorlagenparameter nicht lesen kann, wenn der Name einen Konflikt mit einem integrierten Parameternamen verursacht</span><span class="sxs-lookup"><span data-stu-id="7ad68-481">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="7ad68-482">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-09-01 aktualisiert, die Gruppierungsunterstützung in Richtliniensatzdefinitionen einführt</span><span class="sxs-lookup"><span data-stu-id="7ad68-482">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ad68-483">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ad68-483">Az.Sql</span></span>
* <span data-ttu-id="7ad68-484">Speichererstellung in automatischer Aktivierung der Sicherheitsrisikobewertung auf StorageV2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-484">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7ad68-485">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ad68-485">Az.Storage</span></span>
* <span data-ttu-id="7ad68-486">Unterstützung der Generierung blob-/containeridentitätsbasierter SAS-Token mit Speicherkontext auf der Grundlage der OAuth-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="7ad68-486">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="7ad68-487">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="7ad68-487">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="7ad68-488">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="7ad68-488">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="7ad68-489">Unterstützung für das Widerrufen von Schlüsseln für die Speicherkonto-Benutzerdelegierung hinzugefügt, sodass alle SAS-Identitätstoken widerrufen werden</span><span class="sxs-lookup"><span data-stu-id="7ad68-489">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="7ad68-490">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="7ad68-490">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="7ad68-491">Upgrade auf Microsoft.Azure.Management.Storage 14.2.0, um die neue API-Version 2019-06-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="7ad68-491">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="7ad68-492">Unterstützung von QuotaGiB (Freigabekontingent in Gibibyte) für Werte über 5120 in der Verwaltungsebene von Dateifreigabe-Cmdlets und Parameteralias „Quota“ zum Parameter „QuotaGiB“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-492">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="7ad68-493">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7ad68-493">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="7ad68-494">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7ad68-494">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="7ad68-495">Parameteralias „QuotaGiB“ zum Parameter „Quota“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-495">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="7ad68-496">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="7ad68-496">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="7ad68-497">Problem behoben, dass „Set-AzStorageContainerAcl“ die gespeicherte Zugriffsrichtlinie bereinigen kann</span><span class="sxs-lookup"><span data-stu-id="7ad68-497">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="7ad68-498">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="7ad68-498">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="7ad68-499">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="7ad68-499">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7ad68-500">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="7ad68-500">Highlights since the last major release</span></span>
* <span data-ttu-id="7ad68-501">Az.DataBoxEdge 1.0.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="7ad68-501">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="7ad68-502">Az.SqlVirtualMachine 1.0.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="7ad68-502">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ad68-503">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ad68-503">Az.Compute</span></span>
* <span data-ttu-id="7ad68-504">Funktion zum erneuten Anwenden von VMs</span><span class="sxs-lookup"><span data-stu-id="7ad68-504">VM Reapply feature</span></span>
    - <span data-ttu-id="7ad68-505">Parameter für erneutes Anwenden zu Cmdlet „Set-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-505">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="7ad68-506">AutomaticRepairs-Funktion für VM-Skalierungsgruppe:</span><span class="sxs-lookup"><span data-stu-id="7ad68-506">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="7ad68-507">Parameter „EnableAutomaticRepair“, „AutomaticRepairGracePeriod“ und „AutomaticRepairMaxInstanceRepairsPercent“ zu folgenden Cmdlets hinzugefügt:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7ad68-507">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="7ad68-508">Mandantenübergreifende Unterstützung von Katalogimages für „New-AzVM“</span><span class="sxs-lookup"><span data-stu-id="7ad68-508">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="7ad68-509">„Spot“ zu Argumentvervollständigung des Priority-Parameters in Cmdlets „New-AzVM“, „New-AzVMConfig“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-509">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="7ad68-510">Parameter „DiskIOPSReadWrite“ und „DiskMBpsReadWrite“ zu Cmdlet „Add-AzVmssDataDisk“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-510">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="7ad68-511">Parameter „SourceImageId“ von Cmdlet „New-AzGalleryImageVersion“ in optional geändert</span><span class="sxs-lookup"><span data-stu-id="7ad68-511">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="7ad68-512">Parameter „OSDiskImage“ und „DataDiskImage“ zu Cmdlet „New-AzGalleryImageVersion“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-512">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="7ad68-513">Parameter „HyperVGeneration“ zu Cmdlet „New-AzGalleryImageDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-513">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="7ad68-514">Parameter „SkipExtensionsOnOverprovisionedVMs“ zu Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-514">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="7ad68-515">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="7ad68-515">Az.DataBoxEdge</span></span>
* <span data-ttu-id="7ad68-516">Cmdlet `Get-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-516">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="7ad68-517">Bestellung abrufen</span><span class="sxs-lookup"><span data-stu-id="7ad68-517">Get the Order</span></span>
* <span data-ttu-id="7ad68-518">Cmdlet `New-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-518">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="7ad68-519">Neue Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="7ad68-519">Create new Order</span></span>
* <span data-ttu-id="7ad68-520">Cmdlet `Remove-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-520">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="7ad68-521">Bestellung entfernen</span><span class="sxs-lookup"><span data-stu-id="7ad68-521">Remove the Order</span></span>
* <span data-ttu-id="7ad68-522">Änderung im Cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="7ad68-522">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="7ad68-523">Erstellt jetzt eine lokale Freigabe</span><span class="sxs-lookup"><span data-stu-id="7ad68-523">Now creates Local Share</span></span>
* <span data-ttu-id="7ad68-524">Cmdlet `Set-AzDataBoxEdgeRole` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-524">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="7ad68-525">„IotRole“ kann jetzt einer Freigabe zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="7ad68-525">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="7ad68-526">Cmdlet `Invoke-AzDataBoxEdgeDevice` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-526">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="7ad68-527">Scanupdate aufrufen, Update herunterladen, Updates auf dem Gerät installieren</span><span class="sxs-lookup"><span data-stu-id="7ad68-527">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="7ad68-528">Cmdlet `Get-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-528">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="7ad68-529">Ruft die Informationen zu Auslösern ab</span><span class="sxs-lookup"><span data-stu-id="7ad68-529">Gets the information about Triggers</span></span>
* <span data-ttu-id="7ad68-530">Cmdlet `New-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-530">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="7ad68-531">Neue Auslöser erstellen</span><span class="sxs-lookup"><span data-stu-id="7ad68-531">Create new Triggers</span></span>
* <span data-ttu-id="7ad68-532">Cmdlet `Remove-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-532">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="7ad68-533">Auslöser entfernen</span><span class="sxs-lookup"><span data-stu-id="7ad68-533">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7ad68-534">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7ad68-534">Az.DataFactory</span></span>
* <span data-ttu-id="7ad68-535">Version des ADF .NET SDK auf 4.4.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-535">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="7ad68-536">Parameter „ExpressCustomSetup“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um Setupkonfigurationen und Drittanbieterkomponenten ohne benutzerdefiniertes Setupskript zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="7ad68-536">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7ad68-537">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7ad68-537">Az.DataLakeStore</span></span>
* <span data-ttu-id="7ad68-538">Dokumentation von „Get-AzDataLakeStoreDeletedItem“ und „Restore-AzDataLakeStoreDeletedItem“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-538">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7ad68-539">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7ad68-539">Az.EventHub</span></span>
* <span data-ttu-id="7ad68-540">Behebung des Problems 10301: Datumsformat von SAS-Token korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-540">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7ad68-541">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7ad68-541">Az.FrontDoor</span></span>
* <span data-ttu-id="7ad68-542">Parameter „MinimumTlsVersion“ zu „Enable-AzFrontDoorCustomDomainHttps“ und „New-AzFrontDoorFrontendEndpointObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-542">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="7ad68-543">Parameter „HealthProbeMethod“ und „EnabledState“ zu „New-AzFrontDoorHealthProbeSettingObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-543">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="7ad68-544">Neues Cmdlet zum Erstellen von BackendPoolsSettings-Objekten für die Übergabe in Erstellung/Update von Front Door hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-544">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="7ad68-545">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="7ad68-545">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ad68-546">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ad68-546">Az.Network</span></span>
* <span data-ttu-id="7ad68-547">FilterData-Optionsbeispiele „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ geändert.</span><span class="sxs-lookup"><span data-stu-id="7ad68-547">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="7ad68-548">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="7ad68-548">Az.PrivateDns</span></span>
* <span data-ttu-id="7ad68-549">PrivateDns.net-SDK auf Version 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-549">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7ad68-550">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7ad68-550">Az.RecoveryServices</span></span>
* <span data-ttu-id="7ad68-551">Azure Site Recovery-Unterstützung zum Auswählen des Datenträgertyps beim Aktivieren des Schutzes.</span><span class="sxs-lookup"><span data-stu-id="7ad68-551">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="7ad68-552">Fehlerbehebung bei Bearbeitungsaktion für Azure Site Recovery-Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="7ad68-552">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="7ad68-553">SQL-Wiederherstellungsunterstützung für Azure Backup zum Akzeptieren von Filestream-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="7ad68-553">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7ad68-554">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7ad68-554">Az.RedisCache</span></span>
* <span data-ttu-id="7ad68-555">Parameter „MinimumTlsVersion“ in Cmdlets „New-AzRedisCache“ und „Set-AzRedisCache“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-555">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="7ad68-556">Außerdem „MinimumTlsVersion“ in Ausgabe von Cmdlet „Get-AzRedisCache“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-556">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="7ad68-557">Validierung von Parameter „-Size“ für Cmdlets „Set-AzRedisCache“ und „New-AzRedisCache“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-557">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ad68-558">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ad68-558">Az.Resources</span></span>
- <span data-ttu-id="7ad68-559">Richtlinien-Cmdlets aktualisiert, um die neue API-Version 2019-06-01 mit der neuen EnforcementMode-Eigenschaft bei der Richtlinienzuweisung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7ad68-559">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="7ad68-560">Hilfebeispiel zum Erstellen von Richtliniendefinitionen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-560">Updated create policy definition help example</span></span>
- <span data-ttu-id="7ad68-561">Fehlerkorrektur: „Remove-AZADServicePrincipal -ServicePrincipalName“ gibt Nullverweis aus, wenn Dienstprinzipalname nicht gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="7ad68-561">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="7ad68-562">Fehlerkorrektur: „New-AZADServicePrincipal“ gibt Nullverweis aus, wenn Mandant kein Abonnement hat.</span><span class="sxs-lookup"><span data-stu-id="7ad68-562">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="7ad68-563">„New-AzAdServicePrincipal“ geändert, um Anmeldeinformation nur zu zugeordneter Anwendung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="7ad68-563">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ad68-564">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ad68-564">Az.Sql</span></span>
* <span data-ttu-id="7ad68-565">Unterstützung von „ReadReplicaCount“ für Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-565">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="7ad68-566">Korrektur von „Set-AzSqlDatabase“, wenn Zonenredundanz nicht festgelegt</span><span class="sxs-lookup"><span data-stu-id="7ad68-566">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="7ad68-567">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="7ad68-567">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="7ad68-568">Allgemein</span><span class="sxs-lookup"><span data-stu-id="7ad68-568">General</span></span>
* <span data-ttu-id="7ad68-569">Az.PrivateDns 1.0.0 veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="7ad68-569">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7ad68-570">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ad68-570">Az.Accounts</span></span>
* <span data-ttu-id="7ad68-571">Hinweis zur Veraltung des Alias „Resolve-Error“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-571">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="7ad68-572">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="7ad68-572">Az.Advisor</span></span>
* <span data-ttu-id="7ad68-573">Neue Kategorie „Operational Excellence“ für Cmdlet „Get-AzAdvisorRecommendation“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-573">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7ad68-574">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7ad68-574">Az.Batch</span></span>
* <span data-ttu-id="7ad68-575">`CoreQuota` für `BatchAccountContext` in `DedicatedCoreQuota` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-575">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="7ad68-576">Außerdem wurde das neue Element `LowPriorityCoreQuota` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-576">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="7ad68-577">Dies wirkt sich auf **Get-AzBatchAccount** aus.</span><span class="sxs-lookup"><span data-stu-id="7ad68-577">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="7ad68-578">Für Parameter `-ResourceFile` von **New-AzBatchTask** wird jetzt eine Sammlung mit `PSResourceFile`-Objekten verwendet, und für die Erstellung kann das Cmdlet **New-AzBatchResourceFile** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7ad68-578">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="7ad68-579">Neues Cmdlet **New-AzBatchResourceFile** als Hilfe für die Erstellung von `PSResourceFile`-Objekten.</span><span class="sxs-lookup"><span data-stu-id="7ad68-579">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="7ad68-580">Diese können für **New-AzBatchTask** über den Parameter `-ResourceFile` bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="7ad68-580">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="7ad68-581">Hierbei werden zusätzlich zum Ansatz mit `HttpUrl` zwei neue Arten von Ressourcendateien unterstützt:</span><span class="sxs-lookup"><span data-stu-id="7ad68-581">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="7ad68-582">Mit Ressourcendateien, die auf `AutoStorageContainerName` basieren, wird ein gesamter Container für die automatische Speicherung auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="7ad68-582">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="7ad68-583">Für Ressourcendateien, die auf `StorageContainerUrl` basieren, wird der in der URL angegebene Container auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="7ad68-583">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="7ad68-584">`ApplicationPackages`-Eigenschaft von `PSApplication` entfernt, die von **Get-AzBatchApplication** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7ad68-584">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="7ad68-585">Die spezifischen Pakete in einer Anwendung können jetzt mit **Get-AzBatchApplicationPackage** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7ad68-585">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="7ad68-586">Beispiel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="7ad68-586">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="7ad68-587">`ApplicationId` für **Get-AzBatchApplicationPackage** , **New-AzBatchApplicationPackage** , **Remove-AzBatchApplicationPackage** , **Get-AzBatchApplication** , **New-AzBatchApplication** , **Remove-AzBatchApplication** und **Set-AzBatchApplication** in `ApplicationName` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-587">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage** , **New-AzBatchApplicationPackage** , **Remove-AzBatchApplicationPackage** , **Get-AzBatchApplication** , **New-AzBatchApplication** , **Remove-AzBatchApplication** , and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="7ad68-588">`ApplicationId` ist jetzt ein Alias von `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="7ad68-588">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="7ad68-589">Neue `PSWindowsUserConfiguration`-Eigenschaft zu `PSUserAccount` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-589">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="7ad68-590">`Version` für `PSApplicationPackage` in `Name` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-590">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="7ad68-591">`BlobSource` für `PSResourceFile` in `HttpUrl` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-591">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="7ad68-592">`OSDisk`-Eigenschaft aus `PSVirtualMachineConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-592">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="7ad68-593">**Set-AzBatchPoolOSVersion** entfernt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-593">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="7ad68-594">Dieser Vorgang wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-594">This operation is no longer supported.</span></span>
* <span data-ttu-id="7ad68-595">`TargetOSVersion` aus `PSCloudServiceConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-595">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="7ad68-596">`CurrentOSVersion` für `PSCloudServiceConfiguration` in `OSVersion` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-596">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="7ad68-597">`DataEgressGiB` und `DataIngressGiB` aus `PSPoolUsageMetrics` entfernt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-597">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="7ad68-598">**Get-AzBatchNodeAgentSku** entfernt und durch **Get-AzBatchSupportedImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-598">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="7ad68-599">**Get-AzBatchSupportedImage** gibt die gleichen Daten wie **Get-AzBatchNodeAgentSku** zurück, aber in einem benutzerfreundlicheren Format.</span><span class="sxs-lookup"><span data-stu-id="7ad68-599">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="7ad68-600">Neue nicht verifizierte Images werden nun ebenfalls zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7ad68-600">New non-verified images are also now returned.</span></span> <span data-ttu-id="7ad68-601">Zusätzlich sind weitere Informationen zu `Capabilities` und `BatchSupportEndOfLife` für jedes Image vorhanden.</span><span class="sxs-lookup"><span data-stu-id="7ad68-601">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="7ad68-602">Möglichkeit zum Bereitstellen von Remotedateisystemen auf jedem Knoten eines Pools über den neuen Parameter `MountConfiguration` von **New-AzBatchPool** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-602">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="7ad68-603">Es ist jetzt Unterstützung für Sicherheitsregeln vorhanden, die den Netzwerkzugriff auf einen Pool basierend auf dem Quellport des Datenverkehrs blockieren.</span><span class="sxs-lookup"><span data-stu-id="7ad68-603">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="7ad68-604">Dies erfolgt über die `SourcePortRanges`-Eigenschaft unter `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="7ad68-604">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="7ad68-605">Bei der Ausführung eines Containers unterstützt Batch jetzt die Ausführung der Aufgabe im Arbeitsverzeichnis des Containers bzw. im Arbeitsverzeichnis der Batch-Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="7ad68-605">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="7ad68-606">Dies wird mit der `WorkingDirectory`-Eigenschaft unter `PSTaskContainerSettings` gesteuert.</span><span class="sxs-lookup"><span data-stu-id="7ad68-606">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="7ad68-607">Möglichkeit zum Angeben einer Sammlung mit öffentlichen IP-Adressen für `PSNetworkConfiguration` über die neue `PublicIPs`-Eigenschaft hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-607">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="7ad68-608">So wird sichergestellt, dass Knoten im Pool über eine IP-Adresse aus der Liste mit den von Benutzern bereitgestellten IP-Adressen verfügen.</span><span class="sxs-lookup"><span data-stu-id="7ad68-608">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="7ad68-609">Wenn kein Wert angegeben wird, lautet der Standardwert von `WaitForSuccess` unter `PSSTartTask` jetzt `$True` (bisher `$False`).</span><span class="sxs-lookup"><span data-stu-id="7ad68-609">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="7ad68-610">Wenn kein Wert angegeben wird, lautet der Standardwert von `Scope` unter `PSAutoUserSpecification` jetzt `Pool` (bisher `Task` unter Windows und `Pool` unter Linux).</span><span class="sxs-lookup"><span data-stu-id="7ad68-610">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7ad68-611">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7ad68-611">Az.Cdn</span></span>
* <span data-ttu-id="7ad68-612">„UrlRewriteAction“ und „CacheKeyQueryStringAction“ für „RulesEngine“ eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-612">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="7ad68-613">Mehrere Fehler behoben, z. B. fehlende „Selector“-Eingabe im Cmdlet „New-AzDeliveryRuleCondition“.</span><span class="sxs-lookup"><span data-stu-id="7ad68-613">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ad68-614">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ad68-614">Az.Compute</span></span>
* <span data-ttu-id="7ad68-615">Feature „Datenträgerverschlüsselungssatz“</span><span class="sxs-lookup"><span data-stu-id="7ad68-615">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="7ad68-616">Neue Cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="7ad68-616">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="7ad68-617">Parameter „DiskEncryptionSetId“ wurde den folgenden Cmdlets hinzugefügt:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="7ad68-617">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="7ad68-618">Die Parameter „DiskEncryptionSetId“ und „EncryptionType“ wurden den folgenden Cmdlets hinzugefügt:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="7ad68-618">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="7ad68-619">Parameter „PublicIPAddressVersion“ wurde „New-AzVmssIPConfig“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-619">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="7ad68-620">„FileUris“ für benutzerdefinierte Skripterweiterung von öffentlicher Einstellung auf geschützte Einstellung umgestellt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-620">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="7ad68-621">„ScaleInPolicy“ wurde den Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-621">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="7ad68-622">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="7ad68-622">Breaking changes</span></span>
    - <span data-ttu-id="7ad68-623">Parameter „UploadSizeInBytes“ wird anstelle von „DiskSizeGB“ für „New-AzDiskConfig“ verwendet, wenn „CreateOption“ auf „Upload“ festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7ad68-623">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="7ad68-624">Im „GalleryImageVersion“-Objekt wurde „objectPublishingProfile.Source.ManagedImage.Id“ durch „StorageProfile.Source.Id“ ersetzt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-624">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7ad68-625">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7ad68-625">Az.DataFactory</span></span>
* <span data-ttu-id="7ad68-626">Version des ADF .NET SDK auf 4.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7ad68-626">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7ad68-627">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7ad68-627">Az.DataLakeStore</span></span>
* <span data-ttu-id="7ad68-628">Update für ADLS SDK-Version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) mit den folgenden Fehlerbehebungen durchgeführt:</span><span class="sxs-lookup"><span data-stu-id="7ad68-628">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="7ad68-629">Vermeidung der Auslösung einer Ausnahme, während die Deserialisierung des „creationtime“-Elements des Papierkorb- oder Verzeichniseintrags nicht durchgeführt werden kann</span><span class="sxs-lookup"><span data-stu-id="7ad68-629">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="7ad68-630">Verfügbarmachung der Einstellung pro Anforderungszeitlimit in „adlsclient“</span><span class="sxs-lookup"><span data-stu-id="7ad68-630">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="7ad68-631">Fehlerbehebung für Übergabe des ursprünglichen „syncflag“-Elements für badoffset-Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="7ad68-631">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="7ad68-632">Fehlerbehebung für „EnumerateDirectory“ zum Abrufen des Fortsetzungstokens nach der Überprüfung der Antwort</span><span class="sxs-lookup"><span data-stu-id="7ad68-632">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="7ad68-633">Behebung eines Verkettungsfehlers</span><span class="sxs-lookup"><span data-stu-id="7ad68-633">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7ad68-634">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7ad68-634">Az.FrontDoor</span></span>
* <span data-ttu-id="7ad68-635">Verschiedene Tippfehler im Modul korrigiert.</span><span class="sxs-lookup"><span data-stu-id="7ad68-635">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7ad68-636">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7ad68-636">Az.HDInsight</span></span>
* <span data-ttu-id="7ad68-637">Fehler behoben, bei dem Kunden die Meldung „Keine gültige Base64-Zeichenfolge“ erhalten haben, wenn sie „Get-AzHDInsightCluster“ zum Abrufen des Clusters mit ADLSGen1-Speicher verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="7ad68-637">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="7ad68-638">Parameter mit dem Namen „ApplicationId“ den drei Cmdlets „Add-AzHDInsightClusterIdentity“, „New-AzHDInsightClusterConfig“ und „New-AzHDInsightCluster“ hinzugefügt, damit der Kunde die Dienstprinzipal-Anwendungs-ID für den Zugriff auf Azure Data Lake bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="7ad68-638">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="7ad68-639">Microsoft.Azure.Management.HDInsight von 2.1.0 in 5.1.0 geändert.</span><span class="sxs-lookup"><span data-stu-id="7ad68-639">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="7ad68-640">Fünf Cmdlets wurden entfernt:</span><span class="sxs-lookup"><span data-stu-id="7ad68-640">Removed five cmdlets:</span></span>
    - <span data-ttu-id="7ad68-641">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="7ad68-641">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="7ad68-642">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="7ad68-642">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="7ad68-643">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="7ad68-643">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="7ad68-644">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7ad68-644">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="7ad68-645">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7ad68-645">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="7ad68-646">Drei Cmdlets wurden hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="7ad68-646">Added three cmdlets:</span></span>
    - <span data-ttu-id="7ad68-647">„Get-AzHDInsightMonitoring“ als Ersatz für „Get-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="7ad68-647">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="7ad68-648">„Enable-AzHDInsightMonitoring“ als Ersatz für „Enable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="7ad68-648">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="7ad68-649">„Disable-AzHDInsightMonitoring“ als Ersatz für „Disable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="7ad68-649">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="7ad68-650">Fehler für Cmdlet „Get-AzHDInsightProperties“ behoben, um Unterstützung für das Abrufen von Funktionsinformationen von einem bestimmten Ort bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7ad68-650">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="7ad68-651">Parametersätze („Spark1“, „Spark2“) aus „Add-AzHDInsightConfigValue“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-651">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="7ad68-652">Beispiele den Hilfedokumenten des Cmdlets „Add-AzHDInsightSecurityProfile“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-652">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="7ad68-653">Der Ausgabetyp der folgenden Cmdlets wurde geändert:</span><span class="sxs-lookup"><span data-stu-id="7ad68-653">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="7ad68-654">Ausgabetyp für „Get-AzHDInsightProperties“ von „CapabilitiesResponse“ in „AzureHDInsightCapabilities“ geändert.</span><span class="sxs-lookup"><span data-stu-id="7ad68-654">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="7ad68-655">Ausgabetyp für „Remove-AzHDInsightCluster“ von „ClusterGetResponse“ in „bool“ geändert.</span><span class="sxs-lookup"><span data-stu-id="7ad68-655">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="7ad68-656">Ausgabetyp für „Set-AzHDInsightGatewaySettings“ von „HttpConnectivitySettings“ in „GatewaySettings“ geändert.</span><span class="sxs-lookup"><span data-stu-id="7ad68-656">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="7ad68-657">Einige Testfälle für Szenarien wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-657">Added some scenario test cases.</span></span>
* <span data-ttu-id="7ad68-658">Aliase wurden entfernt: „Add-AzHDInsightConfigValues“, „Get-AzHDInsightProperties“.</span><span class="sxs-lookup"><span data-stu-id="7ad68-658">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7ad68-659">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7ad68-659">Az.IotHub</span></span>
* <span data-ttu-id="7ad68-660">Wichtige Änderungen:</span><span class="sxs-lookup"><span data-stu-id="7ad68-660">Breaking changes:</span></span>
    - <span data-ttu-id="7ad68-661">Das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="7ad68-661">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="7ad68-662">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-662">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="7ad68-663">Das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="7ad68-663">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="7ad68-664">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-664">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="7ad68-665">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-665">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="7ad68-666">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-666">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="7ad68-667">Das Cmdlet „New-AzIotHubExportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubExportDevices“.</span><span class="sxs-lookup"><span data-stu-id="7ad68-667">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="7ad68-668">Das Cmdlet „New-AzIotHubImportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubImportDevices“.</span><span class="sxs-lookup"><span data-stu-id="7ad68-668">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="7ad68-669">Das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="7ad68-669">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="7ad68-670">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-670">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="7ad68-671">Das Cmdlet „Set-AzIotHub“ unterstützt den Parameter „OperationsMonitoringProperties“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="7ad68-671">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="7ad68-672">Der Parametersatz „UpdateOperationsMonitoringProperties“ für das Cmdlet „Set-AzIotHub“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-672">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7ad68-673">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7ad68-673">Az.RecoveryServices</span></span>
* <span data-ttu-id="7ad68-674">Azure wurde die Azure Site Recovery-Unterstützung zum Konfigurieren von Netzwerkressourcen, z. B. NSG, öffentliche IP-Adresse und interner Load Balancer für Azure, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-674">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="7ad68-675">Azure Site Recovery-Unterstützung zum Schreiben auf verwaltete Datenträger für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-675">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="7ad68-676">Azure Site Recovery-Unterstützung für NIC-Reduzierung für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-676">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="7ad68-677">Azure wurde Azure Site Recovery-Unterstützung für beschleunigten Netzwerkbetrieb für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-677">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="7ad68-678">Azure wurde Azure Site Recovery-Unterstützung für automatische Agent-Updates für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-678">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="7ad68-679">Azure wurde Azure Site Recovery-Unterstützung für SSD Standard für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-679">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="7ad68-680">Azure wurde Azure Site Recovery-Unterstützung für das zweistufige Azure Disk Encryption-Verfahren für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-680">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="7ad68-681">Azure wurde Azure Site Recovery-Unterstützung für das Schützen von neu hinzugefügten Datenträgern für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-681">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="7ad68-682">Feature „Vorläufiges Löschen“ (SoftDelete) für VM und zugehörige Tests hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-682">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ad68-683">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ad68-683">Az.Resources</span></span>
* <span data-ttu-id="7ad68-684">Abhängigkeitsassembly „Microsoft.Extensions.Caching.Memory“ von 1.1.1 auf 2.2 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7ad68-684">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ad68-685">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ad68-685">Az.Network</span></span>
* <span data-ttu-id="7ad68-686">Alle Cmdlets für „PrivateEndpointConnection“ geändert, um Unterstützung für generischen Dienstanbieter bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7ad68-686">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="7ad68-687">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7ad68-687">Updated cmdlet:</span></span>
        - <span data-ttu-id="7ad68-688">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7ad68-688">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7ad68-689">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7ad68-689">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7ad68-690">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7ad68-690">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7ad68-691">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7ad68-691">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7ad68-692">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7ad68-692">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="7ad68-693">Neues Cmdlet für „PrivateLinkResource“ hinzugefügt, einschließlich Unterstützung des generischen Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="7ad68-693">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="7ad68-694">Neues Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7ad68-694">New cmdlet:</span></span>
        - <span data-ttu-id="7ad68-695">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="7ad68-695">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="7ad68-696">Neue Felder und Parameter für das Feature „Proxyprotokoll V2“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-696">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="7ad68-697">„EnableProxyProtocol“-Eigenschaft in „PrivateLinkService“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-697">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="7ad68-698">„LinkIdentifier“-Eigenschaft in „PrivateEndpointConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-698">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="7ad68-699">„New-AzPrivateLinkService“ aktualisiert, um den neuen optionalen Parameter „EnableProxyProtocol“ hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="7ad68-699">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="7ad68-700">Fehlerhafte Parameterbeschreibung in Referenzdokumentation von „New-AzApplicationGatewaySku“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="7ad68-700">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="7ad68-701">Neue Cmdlets zur Unterstützung der Azure-Firewallrichtlinie hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-701">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="7ad68-702">Unterstützung für untergeordnete Ressource „RouteTables“ von VirtualHub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-702">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="7ad68-703">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7ad68-703">New cmdlets added:</span></span>
        - <span data-ttu-id="7ad68-704">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="7ad68-704">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="7ad68-705">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7ad68-705">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="7ad68-706">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7ad68-706">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="7ad68-707">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7ad68-707">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="7ad68-708">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="7ad68-708">Set-AzVirtualHub</span></span>
* <span data-ttu-id="7ad68-709">Unterstützung für die neuen Eigenschaften „Sku“ von VirtualHub und „VirtualWANType“ von VirtualWan hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-709">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="7ad68-710">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7ad68-710">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="7ad68-711">New-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-711">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="7ad68-712">Update-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-712">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="7ad68-713">New-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-713">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="7ad68-714">Update-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-714">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="7ad68-715">Unterstützung für „EnableInternetSecurity“-Eigenschaft für „HubVnetConnection“, „VpnConnection“ und „ExpressRouteConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-715">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="7ad68-716">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7ad68-716">New cmdlets added:</span></span>
        - <span data-ttu-id="7ad68-717">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="7ad68-717">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="7ad68-718">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7ad68-718">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="7ad68-719">New-AzureRmVirtualHubVnetConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-719">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="7ad68-720">New-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-720">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="7ad68-721">Update-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-721">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="7ad68-722">New-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-722">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="7ad68-723">Set-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-723">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="7ad68-724">Unterstützung für die Konfiguration der „WebApplicationFirewall“-Richtlinie der obersten Ebene hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-724">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="7ad68-725">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7ad68-725">New cmdlets added:</span></span>
        - <span data-ttu-id="7ad68-726">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="7ad68-726">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="7ad68-727">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="7ad68-727">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="7ad68-728">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="7ad68-728">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="7ad68-729">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="7ad68-729">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="7ad68-730">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="7ad68-730">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="7ad68-731">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="7ad68-731">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="7ad68-732">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7ad68-732">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="7ad68-733">New-AzApplicationGatewayFirewallPolicy: Parameter „PolicySetting“, „ManagedRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-733">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="7ad68-734">Unterstützung für Operator „Geo-Match“ unter „CustomRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-734">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="7ad68-735">„GeoMatch“ zum Operator von „FirewallCondition“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-735">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="7ad68-736">Unterstützung für Firewallrichtlinien „perListener“ und „perSite“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-736">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="7ad68-737">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7ad68-737">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="7ad68-738">New-AzApplicationGatewayHttpListener: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-738">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="7ad68-739">New-AzApplicationGatewayPathRuleConfig: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-739">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="7ad68-740">Fehlerbehebung: Nichtbeachtung der Groß-/Kleinschreibung für erforderliches Subnetz mit dem Namen „AzureBastionSubnet“ in „PSBastion“ ist jetzt möglich.</span><span class="sxs-lookup"><span data-stu-id="7ad68-740">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="7ad68-741">Unterstützung für Ziel-FQDNs in Netzwerkregeln und Übersetzung von FQDN in NAT-Regeln für Azure Firewall hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-741">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="7ad68-742">Unterstützung für Ressource „RouteTables“ der obersten Ebene von „IpGroup“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-742">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="7ad68-743">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7ad68-743">New cmdlets added:</span></span>
        - <span data-ttu-id="7ad68-744">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7ad68-744">New-AzIpGroup</span></span>
        - <span data-ttu-id="7ad68-745">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7ad68-745">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="7ad68-746">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7ad68-746">Get-AzIpGroup</span></span>
        - <span data-ttu-id="7ad68-747">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7ad68-747">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7ad68-748">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7ad68-748">Az.ServiceFabric</span></span>
* <span data-ttu-id="7ad68-749">Cmdlet „Add-AzServiceFabricApplicationCertificate“ entfernt, da dieses Szenario durch „Add-AzVmssSecret“ abgedeckt ist.</span><span class="sxs-lookup"><span data-stu-id="7ad68-749">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ad68-750">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ad68-750">Az.Sql</span></span>
* <span data-ttu-id="7ad68-751">Unterstützung für die Wiederherstellung von gelöschten Datenbanken auf verwalteten Instanzen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-751">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="7ad68-752">Veraltete Cmdlets für die Überprüfung aus Code ausgesondert.</span><span class="sxs-lookup"><span data-stu-id="7ad68-752">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="7ad68-753">Veraltete Aliase entfernt:</span><span class="sxs-lookup"><span data-stu-id="7ad68-753">Removed deprecated aliases:</span></span>
* <span data-ttu-id="7ad68-754">Get-AzSqlDatabaseIndexRecommendations (stattdessen „Get-AzSqlDatabaseIndexRecommendation“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="7ad68-754">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="7ad68-755">Get-AzSqlDatabaseRestorePoints (stattdessen „Get-AzSqlDatabaseRestorePoint“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="7ad68-755">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="7ad68-756">Cmdlet „Get-AzSqlDatabaseSecureConnectionPolicy“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-756">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="7ad68-757">Aliase für veraltete Cmdlets für Einstellungen zur Sicherheitsrisikobewertung wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-757">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="7ad68-758">Cmdlets für Einstellungen für die erweiterte Bedrohungserkennung wurden als veraltet eingestuft.</span><span class="sxs-lookup"><span data-stu-id="7ad68-758">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="7ad68-759">Cmdlets zum Deaktivieren und Aktivieren von Vertraulichkeitsempfehlungen in Spalten einer Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-759">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7ad68-760">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ad68-760">Az.Storage</span></span>
* <span data-ttu-id="7ad68-761">Unterstützung für große Dateifreigaben beim Erstellen oder Aktualisieren eines Speicherkontos hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-761">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="7ad68-762">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ad68-762">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="7ad68-763">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ad68-763">Set-AzStorageAccount</span></span>
* <span data-ttu-id="7ad68-764">Beim Schließen/Abrufen des Dateihandles wird die Überprüfung des Eingabepfads auf Dateiverzeichnis oder Datei übersprungen, um einen Fehler für das Objekt im Status „DeletePending“ zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="7ad68-764">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="7ad68-765">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7ad68-765">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="7ad68-766">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7ad68-766">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="7ad68-767">2.8.0: Oktober 2019</span><span class="sxs-lookup"><span data-stu-id="7ad68-767">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="7ad68-768">Allgemein</span><span class="sxs-lookup"><span data-stu-id="7ad68-768">General</span></span>
* <span data-ttu-id="7ad68-769">Az.HealthcareApis-Release 1.0.0</span><span class="sxs-lookup"><span data-stu-id="7ad68-769">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7ad68-770">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ad68-770">Az.Accounts</span></span>
* <span data-ttu-id="7ad68-771">Telemetriedaten und URL-Umschreibung für generierte Module aktualisiert, Windows-Komponententests korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-771">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7ad68-772">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7ad68-772">Az.ApiManagement</span></span>
* <span data-ttu-id="7ad68-773">**Set-AzApiManagementApi** : Unterstützung für die Aktualisierung der API in „ApiVersionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-773">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="7ad68-774">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="7ad68-774">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7ad68-775">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7ad68-775">Az.Automation</span></span>
* <span data-ttu-id="7ad68-776">Cmdlet „New-AzureAutomationSoftwareUpdateConfiguration“ für den Parameter für die Linux-Neustarteinstellung korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-776">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7ad68-777">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7ad68-777">Az.Batch</span></span>
* <span data-ttu-id="7ad68-778">**Get-AzBatchNodeAgentSku** ist veraltet und wird in Version 2.0.0 durch **Get-AzBatchSupportImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-778">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ad68-779">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ad68-779">Az.Compute</span></span>
* <span data-ttu-id="7ad68-780">Parameter „Priority“, „EvictionPolicy“ und „MaxPrice“ zu den Cmdlets „“New-AzVM“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-780">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="7ad68-781">Warnmeldung und Hilfedokument für die Cmdlets „Add-AzVMAdditionalUnattendContent“ und „Add-AzVMSshPublicKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-781">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="7ad68-782">Ausnahme „-skipVmBackup“ Linux-VMs mit verwalteten Datenträgern für „Set-AzVMDiskEncryptionExtension“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-782">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="7ad68-783">Fehler beim Aktualisieren von Verschlüsselungseinstellungen in „Set-AzVMDiskEncryptionExtension“ korrigiert (zweistufiges Szenario)</span><span class="sxs-lookup"><span data-stu-id="7ad68-783">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7ad68-784">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7ad68-784">Az.DataFactory</span></span>
* <span data-ttu-id="7ad68-785">CRUD-Befehle für ADF V2-Datenfluss hinzugefügt: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow und Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="7ad68-785">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="7ad68-786">Aktionsbefehle für Debugsitzung für ADF V2-Datenfluss hinzugefügt: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand und Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="7ad68-786">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="7ad68-787">Version des ADF .NET SDK auf 4.2.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-787">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7ad68-788">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7ad68-788">Az.DataLakeStore</span></span>
* <span data-ttu-id="7ad68-789">Kontoüberprüfung korrigiert, sodass Konten mit „-“ ohne Domäne übermittelt werden können</span><span class="sxs-lookup"><span data-stu-id="7ad68-789">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="7ad68-790">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="7ad68-790">Az.HealthcareApis</span></span>
* <span data-ttu-id="7ad68-791">PowerShell-Version auf 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-791">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="7ad68-792">SDK-Version auf 1.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-792">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="7ad68-793">Aktualisierung in Tests, um auf neue SDK-Version zu verweisen</span><span class="sxs-lookup"><span data-stu-id="7ad68-793">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="7ad68-794">Ausgabestruktur von geschachtelt in vereinfacht geändert</span><span class="sxs-lookup"><span data-stu-id="7ad68-794">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7ad68-795">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7ad68-795">Az.IotHub</span></span>
* <span data-ttu-id="7ad68-796">Neue Routingquelle hinzugefügt: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="7ad68-796">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="7ad68-797">Kleinere Fehlerbehebung: „Get-AzIothub“ gibt „subscriptionId“ nicht zurück.</span><span class="sxs-lookup"><span data-stu-id="7ad68-797">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7ad68-798">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7ad68-798">Az.Monitor</span></span>
* <span data-ttu-id="7ad68-799">Neue Aktionsgruppenempfänger für Aktionsgruppe hinzugefügt:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="7ad68-799">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="7ad68-800">Verwendung des allgemeinen Warnungsschemas für Empfänger aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7ad68-800">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="7ad68-801">Dies gilt nicht für SMS, Azure App-Pushbenachrichtigungen, ITSM und Sprachempfänger.</span><span class="sxs-lookup"><span data-stu-id="7ad68-801">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="7ad68-802">Webhooks unterstützen nun die Azure Active Directory-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="7ad68-802">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ad68-803">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ad68-803">Az.Network</span></span>
* <span data-ttu-id="7ad68-804">Neues Cmdlet „Get-AzAvailableServiceAlias“ hinzugefügt, das zum Abrufen der Aliase aufgerufen werden kann, die für Dienstendpunktrichtlinien verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="7ad68-804">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="7ad68-805">Unterstützung für das Hinzufügen von Verbindungen von Datenverkehrsselektoren zu Virtual Network-Gatewayverbindungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-805">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="7ad68-806">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7ad68-806">New cmdlets added:</span></span>
        - <span data-ttu-id="7ad68-807">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="7ad68-807">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="7ad68-808">Cmdlets mit optionalen Parametern aktualisiert: -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7ad68-808">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="7ad68-809">Unterstützung für ESP- und AH-Protokolle in Konfigurationen von Netzwerksicherheitsregeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-809">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="7ad68-810">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7ad68-810">Updated cmdlets:</span></span>
        - <span data-ttu-id="7ad68-811">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7ad68-811">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7ad68-812">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7ad68-812">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7ad68-813">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7ad68-813">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="7ad68-814">Verbesserte Behandlung von Ausnahmen in Cortex-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7ad68-814">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="7ad68-815">Neue Generationen und SKUs für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="7ad68-815">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="7ad68-816">Einführung neuer Generationen für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="7ad68-816">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="7ad68-817">Einführung neuer SKUs mit höherem Durchsatz für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="7ad68-817">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7ad68-818">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7ad68-818">Az.RedisCache</span></span>
* <span data-ttu-id="7ad68-819">Referenzdokumentation zu „Set-AzRedisCache“ aktualisiert, um fehlende Werte für den Parameter „-Size“ aufzunehmen</span><span class="sxs-lookup"><span data-stu-id="7ad68-819">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ad68-820">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ad68-820">Az.Sql</span></span>
* <span data-ttu-id="7ad68-821">Unterstützung für das Festlegen des Active Directory-Administrators für verwaltete Instanz hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-821">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7ad68-822">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ad68-822">Az.Storage</span></span>
* <span data-ttu-id="7ad68-823">Storage-Clientbibliothek auf 11.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-823">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="7ad68-824">Auflisten von Containern mit der API der Verwaltungsebene, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="7ad68-824">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="7ad68-825">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7ad68-825">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="7ad68-826">Auflisten von Storage-Konten aus Abonnements, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="7ad68-826">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="7ad68-827">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ad68-827">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7ad68-828">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7ad68-828">Az.StorageSync</span></span>
* <span data-ttu-id="7ad68-829">Problem 9810 in „Reset-AzStorageSyncServerCertificate“ behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-829">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7ad68-830">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ad68-830">Az.Websites</span></span>
* <span data-ttu-id="7ad68-831">Fehler beim Aktualisieren von ASP einer App mit „Set-AzWebApp“</span><span class="sxs-lookup"><span data-stu-id="7ad68-831">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="7ad68-832">2.7.0: September 2019</span><span class="sxs-lookup"><span data-stu-id="7ad68-832">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="7ad68-833">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7ad68-833">Az.ApiManagement</span></span>
* <span data-ttu-id="7ad68-834">Beschreibung des Parameters „-Format“ in der Referenzdokumentation für „Set-AzApiManagementPolicy“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-834">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="7ad68-835">Verweise des veralteten Cmdlets „Update-AzApiManagementDeployment“ aus Referenzdokumentation entfernt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-835">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="7ad68-836">Verwenden Sie stattdessen „Set-AzApiManagement“.</span><span class="sxs-lookup"><span data-stu-id="7ad68-836">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7ad68-837">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7ad68-837">Az.Automation</span></span>
* <span data-ttu-id="7ad68-838">Tippfehler im Beispiel in der Referenzdokumentation für „Register-AzAutomationDscNode“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-838">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="7ad68-839">Erläuterung zur Betriebssystemeinschränkung zu „Register-AzAutomationDSCNode“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-839">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="7ad68-840">Nullverweisausnahme des Cmdlets „Start-AzAutomationRunbook“ für die Option „-Wait“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="7ad68-840">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ad68-841">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ad68-841">Az.Compute</span></span>
* <span data-ttu-id="7ad68-842">Parameter „UploadSizeInBytes“ zu „New-AzDiskConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-842">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="7ad68-843">Inkrementeller Parameter zu „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-843">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="7ad68-844">Feature für VM mit niedriger Priorität hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="7ad68-844">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="7ad68-845">Parameter „MaxPrice“, „EvictionPolicy“ und „Priority“ zu New-AzVMConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-845">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="7ad68-846">Parameter „MaxPrice“ zu den Cmdlets „New-AzVmssConfig“, „Update-AzVM“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-846">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="7ad68-847">Fehlerbehebung für VM-Verweis für das Cmdlet „Get-AzAvailabilitySet“, wenn alle Verfügbarkeitsgruppen im Abonnement aufgelistet werden</span><span class="sxs-lookup"><span data-stu-id="7ad68-847">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="7ad68-848">Nullausnahme für „Get-AzRemoteDesktopFile“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-848">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="7ad68-849">VHD-Suchmethode für Position relativ zum Ende korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-849">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="7ad68-850">Problem mit UltraSSD für „New-AzVM“ und „Update-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-850">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7ad68-851">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7ad68-851">Az.DataFactory</span></span>
* <span data-ttu-id="7ad68-852">Drei neue Befehle für ADF V2 hinzugefügt: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription und Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="7ad68-852">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="7ad68-853">Version des ADF .NET SDK auf 4.1.3 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-853">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7ad68-854">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7ad68-854">Az.HDInsight</span></span>
* <span data-ttu-id="7ad68-855">Hinweis auf Breaking Changes hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-855">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7ad68-856">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7ad68-856">Az.IotHub</span></span>
* <span data-ttu-id="7ad68-857">Unterstützung zum Aufrufen eines Failovers für einen IoT-Hub zur geografisch gekoppelten Notfallwiederherstellungsregion hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-857">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="7ad68-858">Unterstützung zum Verwalten der Nachrichtenanreicherung für einen IoT-Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-858">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="7ad68-859">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="7ad68-859">New cmdlets are:</span></span>
    - <span data-ttu-id="7ad68-860">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="7ad68-860">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="7ad68-861">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="7ad68-861">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="7ad68-862">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="7ad68-862">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="7ad68-863">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="7ad68-863">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7ad68-864">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7ad68-864">Az.Monitor</span></span>
* <span data-ttu-id="7ad68-865">Verweis auf das aktuelle Monitor SDK, d. h. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="7ad68-865">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="7ad68-866">Geringfügige Änderungen an den Metrik-Cmdlets vorgenommen, d. h. die Einheitenenumeration unterstützt verschiedene neue Werte.</span><span class="sxs-lookup"><span data-stu-id="7ad68-866">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="7ad68-867">Dabei handelt es sich um schreibgeschützte Cmdlets, sodass keine Änderungen an der Eingabe der Cmdlets erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="7ad68-867">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="7ad68-868">Die API-Version der **ActionGroups** -Anforderungen lautet jetzt **2019-06-01** (zuvor **2018-03-01** ).</span><span class="sxs-lookup"><span data-stu-id="7ad68-868">The api-version of the **ActionGroups** requests is now **2019-06-01** , before it was **2018-03-01**.</span></span> <span data-ttu-id="7ad68-869">Die Szenariotests wurden aktualisiert, um diese Änderung zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="7ad68-869">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="7ad68-870">Die Konstruktoren für die Klassen **EmailReceiver** und **WebhookReceiver** haben ein neues obligatorisches Argument hinzugefügt, d. h. einen booleschen Wert namens **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="7ad68-870">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="7ad68-871">Derzeit ist der Wert auf **false** festgelegt, damit sich dieser Breaking Change nicht auf die Cmdlets auswirkt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-871">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="7ad68-872">**HINWEIS:** Dies ist eine vorübergehende Änderung, die vom Team für Warnungen validiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="7ad68-872">**NOTE** : this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="7ad68-873">Die Reihenfolge der Argumente für den Konstruktor der Klasse **Source** (in Bezug auf die Klasse **ScheduledQueryRuleSource** ) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="7ad68-873">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="7ad68-874">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="7ad68-874">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="7ad68-875">Die Reihenfolge der Argumente für den Konstruktor der Klasse **AlertingAction** (in Bezug auf die Klasse **ScheduledQueryRuleSource** ) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="7ad68-875">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="7ad68-876">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="7ad68-876">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="7ad68-877">Unterstützung von Kriterien für dynamische Schwellwerte für Metrikwarnung v2</span><span class="sxs-lookup"><span data-stu-id="7ad68-877">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="7ad68-878">New-AzMetricAlertRuleV2Criteria: Erstellt nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="7ad68-878">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="7ad68-879">Add-AzMetricAlertRuleV2: Akzeptiert nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="7ad68-879">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="7ad68-880">Verbesserungen an den Cmdlets für geplante Abfrageregeln (Scheduled Query Rule, SQR)</span><span class="sxs-lookup"><span data-stu-id="7ad68-880">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="7ad68-881">Cmdlets akzeptieren den Parameter „Location“ in zwei Formaten: entweder den Standort (z. B. „eastus“) oder den Anzeigenamen des Standorts (z. B. „USA, Osten“)</span><span class="sxs-lookup"><span data-stu-id="7ad68-881">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="7ad68-882">Parameter „Enabled“ in Hilfedateien ordnungsgemäß dargestellt</span><span class="sxs-lookup"><span data-stu-id="7ad68-882">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="7ad68-883">Beispiele für optionalen Parameter „ActionGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-883">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="7ad68-884">Hilfedateien insgesamt verbessert</span><span class="sxs-lookup"><span data-stu-id="7ad68-884">Overall improved help files</span></span>
* <span data-ttu-id="7ad68-885">Fehler beim Bestimmen des Bereichstyps für „Set-AzActionRule“ behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-885">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ad68-886">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ad68-886">Az.Network</span></span>
* <span data-ttu-id="7ad68-887">Fehlerhaftes Beispiel in der Referenzdokumentation zu „New-AzApplicationGateway“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-887">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="7ad68-888">Hinweis in der Referenzdokumentation zu „Get-AzNetworkWatcherPacketCapture“ zum Abrufen aller Eigenschaften für eine Paketerfassung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-888">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="7ad68-889">Beispiel in der Referenzdokumentation zu „Test-AzNetworkWatcherIPFlow“ korrigiert, um die Netzwerkadapter ordnungsgemäß aufzulisten</span><span class="sxs-lookup"><span data-stu-id="7ad68-889">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="7ad68-890">Cloudausnahmeanalyse verbessert, um ggf. zusätzliche Details anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="7ad68-890">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="7ad68-891">Cloudausnahmeanalyse verbessert, um zusätzlichen Typ der SDK-Ausnahme zu verarbeiten</span><span class="sxs-lookup"><span data-stu-id="7ad68-891">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="7ad68-892">Falsche Zuordnung der Sicherheitsregelmodelle korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-892">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="7ad68-893">Eigenschaften zur Netzwerkschnittstelle für das Feature für die private IP-Adresse hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-893">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="7ad68-894">Eigenschaft „PrivateEndpoint“ als Typ „PSResourceId“ zu „PSNetworkInterface“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-894">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="7ad68-895">Eigenschaft „PrivateLinkConnectionProperties“ als Typ „PSIpConfigurationConnectivityInformation“ zu „PSNetworkInterfaceIPConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-895">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="7ad68-896">Neue Modellklasse „PSIpConfigurationConnectivityInformation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-896">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="7ad68-897">Neues ApplicationRuleProtocolType-Element „mssql“ für Azure Firewall-Ressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-897">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="7ad68-898">Unterstützung von Mehrfachverbindungen in Virtual WAN</span><span class="sxs-lookup"><span data-stu-id="7ad68-898">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="7ad68-899">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7ad68-899">New cmdlets</span></span>
        - <span data-ttu-id="7ad68-900">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="7ad68-900">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="7ad68-901">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="7ad68-901">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="7ad68-902">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7ad68-902">Updated cmdlet:</span></span>
        - <span data-ttu-id="7ad68-903">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="7ad68-903">New-VpnSite</span></span>
        - <span data-ttu-id="7ad68-904">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="7ad68-904">Update-VpnSite</span></span>
        - <span data-ttu-id="7ad68-905">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="7ad68-905">New-VpnConnection</span></span>
        - <span data-ttu-id="7ad68-906">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="7ad68-906">Update-VpnConnection</span></span>
* <span data-ttu-id="7ad68-907">Dokumente für einige PowerShell-Beispiele korrigiert, sodass Az-Cmdlets anstelle von AzureRM-Cmdlets verwendet werden</span><span class="sxs-lookup"><span data-stu-id="7ad68-907">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7ad68-908">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7ad68-908">Az.RecoveryServices</span></span>
* <span data-ttu-id="7ad68-909">AzureVMpolicy-Objekt mit ProtectedItemsCount-Attribut aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-909">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="7ad68-910">Tests für VM-Richtlinie und Wiederherstellung des ursprünglichen Speicherkontos hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-910">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ad68-911">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ad68-911">Az.Resources</span></span>
* <span data-ttu-id="7ad68-912">Fehler behoben, aufgrund dessen „New-AzRoleAssignment“ nicht ohne den Parameter „Scope“ aufgerufen werden konnte</span><span class="sxs-lookup"><span data-stu-id="7ad68-912">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7ad68-913">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7ad68-913">Az.ServiceFabric</span></span>
* <span data-ttu-id="7ad68-914">Tippfehler im Beispiel für die Referenzdokumentation „Update-AzServiceFabricReliability“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-914">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="7ad68-915">Neue Cmdlets zum Verwalten von Anwendung und Diensten hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="7ad68-915">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="7ad68-916">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="7ad68-916">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="7ad68-917">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="7ad68-917">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="7ad68-918">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="7ad68-918">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="7ad68-919">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="7ad68-919">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="7ad68-920">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="7ad68-920">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="7ad68-921">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="7ad68-921">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="7ad68-922">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="7ad68-922">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="7ad68-923">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="7ad68-923">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="7ad68-924">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="7ad68-924">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="7ad68-925">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="7ad68-925">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="7ad68-926">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="7ad68-926">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="7ad68-927">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="7ad68-927">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="7ad68-928">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="7ad68-928">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="7ad68-929">Service Fabric SDK auf Version 1.2.0 aktualisiert, die API-Version 2019-03-01 des Service Fabric-Ressourcenanbieters verwendet</span><span class="sxs-lookup"><span data-stu-id="7ad68-929">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7ad68-930">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7ad68-930">Az.SignalR</span></span>
* <span data-ttu-id="7ad68-931">Cmdlets „Update“, „Restart“, „CheckNameAvailability“ und „GetUsage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-931">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ad68-932">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ad68-932">Az.Sql</span></span>
* <span data-ttu-id="7ad68-933">Beispiel in der Referenzdokumentation für „Get-AzSqlElasticPool“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-933">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="7ad68-934">V-Kern-Beispiel zum Erstellen eines Pools für elastische Datenbanken hinzugefügt (New-AzSqlElasticPool)</span><span class="sxs-lookup"><span data-stu-id="7ad68-934">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="7ad68-935">Überprüfung von „EmailAddresses“ sowie Validierung, dass „EmailAdmins“ nicht auf „false“ festgelegt ist, in „Set-AzSqlServerAdvancedThreatProtectionPolicy“ und „Set-AzSqlDatabaseAdvancedThreatProtectionPolicy“ entfernt, wenn „EmailAddresses“ leer ist</span><span class="sxs-lookup"><span data-stu-id="7ad68-935">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="7ad68-936">Entfernen der Einstellungen für Server-/Datenbanküberwachung aktiviert, wenn mehrere Diagnoseeinstellungen vorhanden sind, die eine Überwachungskategorie ermöglichen</span><span class="sxs-lookup"><span data-stu-id="7ad68-936">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="7ad68-937">Überprüfung von E-Mail-Adressen in mehreren Cmdlets für die SQL-Sicherheitsrisikobewertung korrigiert (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting und Update-AzSqlInstanceVulnerabilityAssessmentSetting)</span><span class="sxs-lookup"><span data-stu-id="7ad68-937">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7ad68-938">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ad68-938">Az.Storage</span></span>
* <span data-ttu-id="7ad68-939">Beispiel in der Referenzdokumentation für „Get-AzStorageAccountKey“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-939">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="7ad68-940">Beim Upload/Download von Azure-Dateien wird das Beibehalten der SMB-Eigenschaften der Quelldateien (Dateiattribute, Zeitpunkt der Dateierstellung, letzter Schreibzugriff für die Datei) in der Zieldatei unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-940">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="7ad68-941">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7ad68-941">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="7ad68-942">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7ad68-942">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="7ad68-943">Fehler beim Hochladen von Blockblobs mit Eigenschaften/Metadaten für das für einen Container aktivierte ImmutabilityPolicy-Element behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-943">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="7ad68-944">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7ad68-944">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="7ad68-945">Unterstützung für die Verwaltung von Azure-Dateifreigaben mit der API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="7ad68-945">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="7ad68-946">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7ad68-946">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="7ad68-947">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7ad68-947">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="7ad68-948">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7ad68-948">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="7ad68-949">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7ad68-949">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7ad68-950">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ad68-950">Az.Websites</span></span>
* <span data-ttu-id="7ad68-951">Problem behoben, aufgrund dessen webapp-Tags beim Migrieren der App zu neuem ASP gelöscht wurden</span><span class="sxs-lookup"><span data-stu-id="7ad68-951">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="7ad68-952">„Publish-AzureWebapp“ für die Verwendung unter Linux und Windows korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-952">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="7ad68-953">Beispiel in Referenzdokumentation „Get-AzWebAppPublishingProfile“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-953">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="7ad68-954">2.6.0: August 2019</span><span class="sxs-lookup"><span data-stu-id="7ad68-954">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="7ad68-955">Allgemein</span><span class="sxs-lookup"><span data-stu-id="7ad68-955">General</span></span>
* <span data-ttu-id="7ad68-956">Verschiedene Tippfehler in zahlreichen Modulen korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-956">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7ad68-957">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ad68-957">Az.Accounts</span></span>
* <span data-ttu-id="7ad68-958">Unterstützung der benutzerseitig zugewiesenen MSI in Azure Functions-Authentifizierung (#9479)</span><span class="sxs-lookup"><span data-stu-id="7ad68-958">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="7ad68-959">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="7ad68-959">Az.Aks</span></span>
* <span data-ttu-id="7ad68-960">Problem mit der Ausgabe für „Get-AzAks“ behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-960">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="7ad68-961">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="7ad68-961">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7ad68-962">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7ad68-962">Az.ApiManagement</span></span>
* <span data-ttu-id="7ad68-963">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="7ad68-963">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="7ad68-964">.NET-NuGet-Version aktualisiert, die keine Einschränkungen für „productId“, „apiId“, „groupId“ und „userId“ erzwingt</span><span class="sxs-lookup"><span data-stu-id="7ad68-964">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="7ad68-965">**Get-AzApiManagementProduct:** Unterstützung für das Abfragen von Produkten mithilfe der API hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-965">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="7ad68-966">**New-AzApiManagementApiRevision:** Problem behoben, aufgrund dessen „ApiRevisionDescription“ beim Erstellen einer neuen API-Revision nicht festgelegt wurde https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="7ad68-966">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="7ad68-967">Tippfehler im Modell „PsApiManagementOAuth2AuthrozationServer“ korrigiert: PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7ad68-967">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7ad68-968">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7ad68-968">Az.Batch</span></span>
* <span data-ttu-id="7ad68-969">Tippfehler in Hilfemeldung und Dokumentation korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="7ad68-969">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7ad68-970">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7ad68-970">Az.Cdn</span></span>
* <span data-ttu-id="7ad68-971">Tippfehler im Hilfsprogramm für die CDN-Modulkonvertierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-971">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ad68-972">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ad68-972">Az.Compute</span></span>
* <span data-ttu-id="7ad68-973">VmssId zum Cmdlet „New-AzVMConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-973">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="7ad68-974">Parameter „TerminateScheduledEvents“ und „TerminateScheduledEventNotBeforeTimeoutInMinutes“ zu „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-974">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="7ad68-975">HyperVGeneration-Eigenschaft zu VM-Imageobjekt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-975">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="7ad68-976">Host- und HostGroup-Features hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-976">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="7ad68-977">Neue Cmdlets:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="7ad68-977">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="7ad68-978">Parameter „HostId“ zu „New-AzVMConfig“ und „New-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-978">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="7ad68-979">Beispiel in der Dokumentation zu „Invoke-AzVMRunCommand“ zur Verwendung des richtigen Parameternamens aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-979">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="7ad68-980">Beschreibung für „-VolumeType“ in der Referenzdokumentation zu „Set-AzVMDiskEncryptionExtension“ und „Set-AzVmssDiskEncryptionExtension“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-980">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7ad68-981">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7ad68-981">Az.DataFactory</span></span>
* <span data-ttu-id="7ad68-982">Tippfehler in der Dokumentation zu „New-AzDataFactoryEncryptValue“ korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="7ad68-982">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="7ad68-983">Version des ADF .NET SDK auf 4.1.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-983">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="7ad68-984">Parameter „DataProxyIntegrationRuntimeName“, „DataProxyStagingLinkedServiceName“ und „DataProxyStagingPath“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um die Einrichtung der selbstgehosteten Integration Runtime als Proxy für die SSIS Integration Runtime zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="7ad68-984">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="7ad68-985">„PSTriggerRun“ zum Anzeigen der ausgelösten Pipelines, Meldungen und Eigenschaften und „PSActivityRun“ zum Anzeigen des Aktivitätstyps aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-985">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7ad68-986">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7ad68-986">Az.DataLakeStore</span></span>
* <span data-ttu-id="7ad68-987">Hängen von „Get-DataLakeStoreDeletedItem“ aufgrund von Fehlern oder Remoteausnahmen behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-987">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7ad68-988">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7ad68-988">Az.EventHub</span></span>
* <span data-ttu-id="7ad68-989">Behebung des Problems #9658: Tippfehler im Parameter „VirtualNteworkRule“ in „Set-AzEventHubNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="7ad68-989">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="7ad68-990">Behebung des Problems #9558: „Set-AzEventHubNamespace“ verwendet PATCH anstelle von PUT.</span><span class="sxs-lookup"><span data-stu-id="7ad68-990">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="7ad68-991">Parameter „EnableKafka“ zum Cmdlet „Set-AzEventHubNamespace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-991">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="7ad68-992">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="7ad68-992">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="7ad68-993">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="7ad68-993">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="7ad68-994">Tippfehler („Azure“ in Kleinbuchstaben) in der Dokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-994">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7ad68-995">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7ad68-995">Az.Monitor</span></span>
* <span data-ttu-id="7ad68-996">Falscher Parametername in der Hilfedokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-996">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ad68-997">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ad68-997">Az.Network</span></span>
* <span data-ttu-id="7ad68-998">„New-AzPrivateLinkServiceIpConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-998">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="7ad68-999">Parameter „PublicIpAddress“ ausgemustert, da er auf Serverseite nie verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="7ad68-999">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="7ad68-1000">Optionaler Parameter „Primary“ hinzugefügt, der angibt, ob die aktuelle IP-Konfiguration die primäre ist oder nicht</span><span class="sxs-lookup"><span data-stu-id="7ad68-1000">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="7ad68-1001">Verbesserte Verarbeitung der Anforderungsfehlerausnahme aus dem SDK: Behebt das Problem, dass vorherige SDK-Ausnahmen nicht richtig behandelt wurden, was dazu führt, dass Schlüsselfehlerdetails nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1001">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="7ad68-1002">Validierungslogik für Ipv6-IP-Präfix angepasst, damit auf die richtige IPv6-Präfixlänge geprüft wird</span><span class="sxs-lookup"><span data-stu-id="7ad68-1002">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="7ad68-1003">„Get-AzVirtualNetworkSubnetConfig“ aktualisiert: Parametersatz zum Abrufen nach Subnetzressourcen-ID hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1003">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="7ad68-1004">Aktualisierte Beschreibung des Location-Parameters für „AzNetworkServiceTag“</span><span class="sxs-lookup"><span data-stu-id="7ad68-1004">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7ad68-1005">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7ad68-1005">Az.OperationalInsights</span></span>
* <span data-ttu-id="7ad68-1006">Aktualisierte Dokumentation für „New-AzOperationalInsightsLinuxSyslogDataSource“</span><span class="sxs-lookup"><span data-stu-id="7ad68-1006">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="7ad68-1007">Beispiel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1007">Added example</span></span>
    - <span data-ttu-id="7ad68-1008">Beschreibung für den Parameter „-Name“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1008">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="7ad68-1009">Beispiel für „New-AzOperationalInsightsWindowsEventDataSource“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1009">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="7ad68-1010">Beschreibung des Parameters „-Name“ für „New-AzOperationalInsightsWindowsEventDataSource“ geändert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1010">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7ad68-1011">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7ad68-1011">Az.RecoveryServices</span></span>
* <span data-ttu-id="7ad68-1012">„Get-AzRecoveryServicesBackupJobDetail.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1012">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ad68-1013">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ad68-1013">Az.Resources</span></span>
* <span data-ttu-id="7ad68-1014">Unterstützung für die neue API-Version 2019-05-10 für Microsoft.Resource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1014">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="7ad68-1015">Unterstützung für „copy.count = 0“ für Variablen, Ressourcen und Eigenschaften hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1015">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="7ad68-1016">Ressourcen mit „condition = false“ oder „copy.count = 0“ werden im vollständigen Modus gelöscht.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1016">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="7ad68-1017">Beispiel zum Hinzufügen einer Richtlinie auf Abonnementebene zur Hilfedokumentation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1017">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7ad68-1018">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7ad68-1018">Az.ServiceBus</span></span>
* <span data-ttu-id="7ad68-1019">Behebung des Problems #9658: Tippfehler für Parameter „VirtualNetworkRule“ in „Set-AzServiceBusNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="7ad68-1019">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="7ad68-1020">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="7ad68-1020">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="7ad68-1021">Neuer Befehl „Test-AzServiceBusNameAvailability“ zum Überprüfen der Verfügbarkeit des Namens für Warteschlange und Thema hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1021">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7ad68-1022">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7ad68-1022">Az.ServiceFabric</span></span>
* <span data-ttu-id="7ad68-1023">Fehler bei Cmdlets zum Hinzufügen des Knotentyps korrigiert:</span><span class="sxs-lookup"><span data-stu-id="7ad68-1023">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="7ad68-1024">Fehler „NullReferenceException“, wenn die Ressourcengruppe andere VMSS enthielt, die nicht mit dem Service Fabric-Cluster in Zusammenhang stehen</span><span class="sxs-lookup"><span data-stu-id="7ad68-1024">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="7ad68-1025">Problembehebung: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="7ad68-1025">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="7ad68-1026">Fehler behoben, aufgrund dessen bei einem Cmdlet ein Fehler auftrat, wenn sich „virtualNetwork“ in einer anderen Ressourcengruppe befand als der Cluster</span><span class="sxs-lookup"><span data-stu-id="7ad68-1026">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="7ad68-1027">Problembehebung: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="7ad68-1027">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="7ad68-1028">Cmdlet „Add-AzServiceFabricApplicationCertificate“ ausgemustert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1028">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ad68-1029">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ad68-1029">Az.Sql</span></span>
* <span data-ttu-id="7ad68-1030">Dokumentation alter Überwachungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1030">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7ad68-1031">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ad68-1031">Az.Storage</span></span>
* <span data-ttu-id="7ad68-1032">Hilfe für „Get/Close-AzStorageFileHandle“ aktualisiert (weitere Szenarien zu Cmdlet-Beispielen hinzugefügt und Parameterbeschreibungen aktualisiert)</span><span class="sxs-lookup"><span data-stu-id="7ad68-1032">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="7ad68-1033">Unterstützung von „StandardBlobTier“ in Uploadblobs und Kopierblobs</span><span class="sxs-lookup"><span data-stu-id="7ad68-1033">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="7ad68-1034">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7ad68-1034">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="7ad68-1035">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7ad68-1035">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="7ad68-1036">Unterstützung der Aktivierungspriorität im Kopierblob</span><span class="sxs-lookup"><span data-stu-id="7ad68-1036">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="7ad68-1037">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7ad68-1037">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7ad68-1038">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ad68-1038">Az.Websites</span></span>
* <span data-ttu-id="7ad68-1039">Hinzufügen von Erläuterungen zum Parameter „-AppSettings“ in „Set-AzWebApp“ und „Set-AzWebAppSlot“</span><span class="sxs-lookup"><span data-stu-id="7ad68-1039">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="7ad68-1040">2.5.0: Juli 2019</span><span class="sxs-lookup"><span data-stu-id="7ad68-1040">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7ad68-1041">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ad68-1041">Az.Accounts</span></span>
* <span data-ttu-id="7ad68-1042">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="7ad68-1042">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="7ad68-1043">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="7ad68-1043">Az.ApplicationInsights</span></span>
* <span data-ttu-id="7ad68-1044">Tippfehler im Beispiel in der Dokumentation zu „Remove-AzApplicationInsightsApiKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1044">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7ad68-1045">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7ad68-1045">Az.Automation</span></span>
* <span data-ttu-id="7ad68-1046">Tippfehler in der Ressourcenzeichenfolge korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1046">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7ad68-1047">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7ad68-1047">Az.CognitiveServices</span></span>
* <span data-ttu-id="7ad68-1048">Unterstützung für NetworkRuleSet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1048">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ad68-1049">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ad68-1049">Az.Compute</span></span>
* <span data-ttu-id="7ad68-1050">Fehlende Eigenschaften (ComputerName, OsName, OsVersion und HyperVGeneration) des Objekts für die VM-Instanzenansicht hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1050">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="7ad68-1051">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7ad68-1051">Az.ContainerRegistry</span></span>
* <span data-ttu-id="7ad68-1052">Tippfehler in „Remove-AzContainerRegistryReplication“ für den Replikationsparameter korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1052">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="7ad68-1053">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1053">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7ad68-1054">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7ad68-1054">Az.DataFactory</span></span>
* <span data-ttu-id="7ad68-1055">Version des ADF .NET SDK auf 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1055">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="7ad68-1056">Tippfehler in der Dokumentation für „Get-AzDataFactoryV2PipelineRun“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1056">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7ad68-1057">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7ad68-1057">Az.EventHub</span></span>
* <span data-ttu-id="7ad68-1058">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="7ad68-1058">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="7ad68-1059">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="7ad68-1059">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7ad68-1060">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7ad68-1060">Az.KeyVault</span></span>
* <span data-ttu-id="7ad68-1061">Unterstützung zum Angeben von KeySize für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1061">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7ad68-1062">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7ad68-1062">Az.LogicApp</span></span>
* <span data-ttu-id="7ad68-1063">Korrektur für „Get-AzIntegrationAccountMap“ zum Auflisten aller Zuordnungstypen</span><span class="sxs-lookup"><span data-stu-id="7ad68-1063">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="7ad68-1064">Neuer MapType-Parameter für Filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1064">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="7ad68-1065">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="7ad68-1065">Az.ManagedServices</span></span>
* <span data-ttu-id="7ad68-1066">Unterstützung für API-Version 2019-06-01 (GA) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1066">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ad68-1067">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ad68-1067">Az.Network</span></span>
* <span data-ttu-id="7ad68-1068">Unterstützung für privaten Endpunkt und privaten Verknüpfungsdienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1068">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="7ad68-1069">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7ad68-1069">New cmdlets</span></span>
        - <span data-ttu-id="7ad68-1070">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7ad68-1070">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7ad68-1071">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7ad68-1071">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="7ad68-1072">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7ad68-1072">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7ad68-1073">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7ad68-1073">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7ad68-1074">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7ad68-1074">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7ad68-1075">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7ad68-1075">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7ad68-1076">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="7ad68-1076">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="7ad68-1077">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7ad68-1077">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="7ad68-1078">Folgende Befehle für das Feature aktualisiert: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies für Subnetz in VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7ad68-1078">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="7ad68-1079">„New-AzVirtualNetworkSubnetConfig“, „Set-AzVirtualNetworkSubnetConfig“ und „Add-AzVirtualNetworkSubnetConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1079">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="7ad68-1080">Optionaler Parameter „-PrivateEndpointNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den privaten Endpunkt in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="7ad68-1080">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="7ad68-1081">Optionaler Parameter „-PrivateLinkServiceNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den Privat Link-Dienst in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="7ad68-1081">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="7ad68-1082">Der Cmdlet-Parameter „ServiceName“ von AzPrivateLinkService wurde aus Gründen der Abwärtskompatibilität in „Name“ mit dem Alias „ServiceName“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1082">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="7ad68-1083">ICMP-Protokoll für Konfigurationen von Netzwerksicherheitsregeln aktiviert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1083">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="7ad68-1084">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7ad68-1084">Updated cmdlets</span></span>
        - <span data-ttu-id="7ad68-1085">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7ad68-1085">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7ad68-1086">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7ad68-1086">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7ad68-1087">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7ad68-1087">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="7ad68-1088">ConnectionProtocolType (Ikev1/Ikev2) als konfigurierbarer Parameter für „New-AzVirtualNetworkGatewayConnection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1088">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="7ad68-1089">PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1089">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="7ad68-1090">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7ad68-1090">Updated cmdlet:</span></span>
        - <span data-ttu-id="7ad68-1091">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7ad68-1091">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="7ad68-1092">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7ad68-1092">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="7ad68-1093">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7ad68-1093">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="7ad68-1094">Application Gateway-Befehl „New-AzApplicationGatewayProbeConfig“ zur Unterstützung des benutzerdefinierten Ports im Test aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1094">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="7ad68-1095">„New-AzApplicationGatewayProbeConfig“ aktualisiert: Optionaler Parameter „Port“ hinzugefügt, der zum Testen des Back-End-Servers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1095">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="7ad68-1096">Dieser Parameter gilt für Standard_V2 und WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1096">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7ad68-1097">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7ad68-1097">Az.OperationalInsights</span></span>
* <span data-ttu-id="7ad68-1098">Standardversion für gespeicherte Suchvorgänge auf 1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1098">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="7ad68-1099">Verarbeitung des regulären NULL-Ausdrucks in benutzerdefinierten Protokollen korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1099">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7ad68-1100">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7ad68-1100">Az.RecoveryServices</span></span>
* <span data-ttu-id="7ad68-1101">„Get-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1101">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="7ad68-1102">„Get-AzRecoveryServicesBackupContainer.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1102">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="7ad68-1103">„Get-AzRecoveryServicesVault.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1103">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="7ad68-1104">„Wait-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1104">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="7ad68-1105">„Set-AzRecoveryServicesVaultContext.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1105">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="7ad68-1106">„Get-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1106">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="7ad68-1107">„Get-AzRecoveryServicesBackupRecoveryPoint.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1107">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="7ad68-1108">„Restore-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1108">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="7ad68-1109">Dienstaufruf zum Aufheben der Containerregistrierung für Azure-Dateifreigabe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1109">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="7ad68-1110">„Set-AzRecoveryServicesAsrAlertSetting.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1110">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ad68-1111">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ad68-1111">Az.Resources</span></span>
- <span data-ttu-id="7ad68-1112">Fehlendes Cmdlet entfernt, auf das in der Dokumentation zu „New-AzResourceGroupDeployment“ verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="7ad68-1112">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="7ad68-1113">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1113">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7ad68-1114">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7ad68-1114">Az.ServiceBus</span></span>
* <span data-ttu-id="7ad68-1115">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="7ad68-1115">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="7ad68-1116">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="7ad68-1116">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ad68-1117">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ad68-1117">Az.Sql</span></span>
* <span data-ttu-id="7ad68-1118">Fehlende Beispiele für Cmdlet „Set-AzSqlDatabaseSecondary“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1118">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="7ad68-1119">Festlegen wiederkehrender Überprüfungen der Sicherheitsrisikobewertung ohne Angabe von E-Mail-Adressen korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1119">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="7ad68-1120">Tippfehler in einer Warnmeldung korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1120">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7ad68-1121">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ad68-1121">Az.Storage</span></span>
* <span data-ttu-id="7ad68-1122">Beispiel in Referenzdokumentation für „Get-AzStorageAccount“ aktualisiert, sodass der richtige Parametername verwendet wird</span><span class="sxs-lookup"><span data-stu-id="7ad68-1122">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7ad68-1123">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7ad68-1123">Az.StorageSync</span></span>
* <span data-ttu-id="7ad68-1124">Cmdlet „Invoke-AzStorageSyncChangeDetection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1124">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="7ad68-1125">Problem 9551 zur Berücksichtigung von „TierFilesOlderThanDays“ behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-1125">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7ad68-1126">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ad68-1126">Az.Websites</span></span>
* <span data-ttu-id="7ad68-1127">Problem behoben, aufgrund dessen einige SiteConfig-Eigenschaften von „Get-AzWebApp“ und „Set-AzWebApp“ nicht zurückgegeben wurden</span><span class="sxs-lookup"><span data-stu-id="7ad68-1127">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="7ad68-1128">Neuer Standortparameter zu „Get-AzDeletedWebApp“ und „Restore-AzDeletedWebApp“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1128">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="7ad68-1129">Fehler beim Klonen von Web-App-Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-1129">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="7ad68-1130">2.4.0 – Juli 2019</span><span class="sxs-lookup"><span data-stu-id="7ad68-1130">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7ad68-1131">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ad68-1131">Az.Accounts</span></span>
* <span data-ttu-id="7ad68-1132">Unterstützung für Profil-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1132">Add support for profile cmdlets</span></span>
* <span data-ttu-id="7ad68-1133">Unterstützung für Umgebungen und Datenebenen in generierten Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1133">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="7ad68-1134">Korrektur eines Fehlers, bei dem in einigen Fällen ein falscher Endpunkt für Datenebenen-Cmdlets in Windows PowerShell verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="7ad68-1134">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="7ad68-1135">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="7ad68-1135">Az.Advisor</span></span>
* <span data-ttu-id="7ad68-1136">Allgemein verfügbares Release von Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="7ad68-1136">GA release of Az.Advisor</span></span>
* <span data-ttu-id="7ad68-1137">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1137">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7ad68-1138">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7ad68-1138">Az.ApiManagement</span></span>
* <span data-ttu-id="7ad68-1139">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="7ad68-1139">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="7ad68-1140">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="7ad68-1140">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="7ad68-1141">Unterstützung für Abfragen von Abonnements nach Benutzer und Produkt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1141">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="7ad68-1142">Unterstützung für Abfragen anhand des Umfangs hinzugefügt, „/“, „/apis“, „/apis/echo-api“</span><span class="sxs-lookup"><span data-stu-id="7ad68-1142">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="7ad68-1143">Behebung von Problem https://github.com/Azure/azure-powershell/issues/9307 und https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="7ad68-1143">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="7ad68-1144">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="7ad68-1144">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="7ad68-1145">Unterstützung für die Angabe von „ApiVersion“ und „ApiVersionSetId“ beim Importieren von APIs hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1145">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7ad68-1146">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7ad68-1146">Az.Automation</span></span>
* <span data-ttu-id="7ad68-1147">Fehler beim Cmdlet „Set-AzAutomationConnectionFieldValue“ für die Verarbeitung des Zeichenfolgewerts behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-1147">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ad68-1148">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ad68-1148">Az.Compute</span></span>
* <span data-ttu-id="7ad68-1149">Parameter „HyperVGeneration“ zu New-AzImageConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1149">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7ad68-1150">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7ad68-1150">Az.DataFactory</span></span>
* <span data-ttu-id="7ad68-1151">Aktualisierung der Ausgabe von ADF-Cmdlets für das Abrufen von Aktivitäts-, Pipeline- und Auslöserausführungen, um die Pipe „Select-Object“ zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="7ad68-1151">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7ad68-1152">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7ad68-1152">Az.EventGrid</span></span>
* <span data-ttu-id="7ad68-1153">Tippfehler in Dokumentation zu 'New-AzEventGridSubscription' behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-1153">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7ad68-1154">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7ad68-1154">Az.IotHub</span></span>
* <span data-ttu-id="7ad68-1155">Unterstützung für das erneute Generieren von Autorisierungsrichtlinienschlüsseln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1155">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ad68-1156">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ad68-1156">Az.Network</span></span>
* <span data-ttu-id="7ad68-1157">„RoutingPreference“ zu öffentlichen IP-Tags hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1157">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="7ad68-1158">Beispiele für Referenzdokumentation zu „Get-AzNetworkServiceTag“ verbessert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1158">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7ad68-1159">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7ad68-1159">Az.PolicyInsights</span></span>
* <span data-ttu-id="7ad68-1160">Fehlerbehebung für Nullverweis in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="7ad68-1160">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="7ad68-1161">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="7ad68-1161">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7ad68-1162">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7ad68-1162">Az.OperationalInsights</span></span>
* <span data-ttu-id="7ad68-1163">Zurückgegebenes CustomLog-Datenquellenmodell in Get-AzOperationalInsightsDataSource korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1163">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7ad68-1164">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7ad68-1164">Az.RecoveryServices</span></span>
* <span data-ttu-id="7ad68-1165">Fehlerbehebung für Befehl „get-policy“ IaaSVMs</span><span class="sxs-lookup"><span data-stu-id="7ad68-1165">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ad68-1166">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ad68-1166">Az.Resources</span></span>
    - <span data-ttu-id="7ad68-1167">Hilfetext für Parameter „-Top“ von „Get-AzPolicyState“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1167">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="7ad68-1168">Clientseitige Unterstützung von Paginierung für „Get-AzPolicyAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1168">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="7ad68-1169">Neue Parameter für „Set-AzPolicyAssignment“, „-PolicyParameters“ und „-PolicyParametersObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1169">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="7ad68-1170">Einige Aktualisierungen von Dokumentationen und Beispielen für Policy-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7ad68-1170">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7ad68-1171">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7ad68-1171">Az.ServiceBus</span></span>
* <span data-ttu-id="7ad68-1172">Korrektur für Problem Nr. 4938: „New-AzureRmServiceBusQueue“ gibt beim Festlegen von „MaxSizeInMegabytes“ „BadRequest“ zurück</span><span class="sxs-lookup"><span data-stu-id="7ad68-1172">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ad68-1173">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ad68-1173">Az.Sql</span></span>
* <span data-ttu-id="7ad68-1174">Instanzfailovergruppen-Cmdlets aus Vorschauversion in öffentliche Version hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1174">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="7ad68-1175">Unterstützung von Azure SQL Server\Datenbanküberwachung mit neuen Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7ad68-1175">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="7ad68-1176">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="7ad68-1176">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="7ad68-1177">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="7ad68-1177">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="7ad68-1178">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="7ad68-1178">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="7ad68-1179">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="7ad68-1179">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="7ad68-1180">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="7ad68-1180">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="7ad68-1181">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="7ad68-1181">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="7ad68-1182">E-Mail-Einschränkungen aus Einstellungen der Sicherheitsrisikobewertung entfernt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1182">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7ad68-1183">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ad68-1183">Az.Storage</span></span>
* <span data-ttu-id="7ad68-1184">Zwei Parameter („-IndexDocument“ und „-ErrorDocument404Path“) in folgendem Cmdlet von erforderlich in optional geändert:</span><span class="sxs-lookup"><span data-stu-id="7ad68-1184">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="7ad68-1185">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7ad68-1185">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="7ad68-1186">Hilfe zu „Get-AzStorageBlobContent“ mit neuem Beispiel ergänzt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1186">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="7ad68-1187">Anzeige von mehr Fehlerinformationen beim Fehlschlagen eines Cmdlets mit „StorageException“</span><span class="sxs-lookup"><span data-stu-id="7ad68-1187">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="7ad68-1188">Unterstützung für das Erstellen oder Aktualisieren von Speicherkonten mit Azure Files AAD-DS-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="7ad68-1188">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="7ad68-1189">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ad68-1189">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="7ad68-1190">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ad68-1190">Set-AzStorageAccount</span></span>
* <span data-ttu-id="7ad68-1191">Unterstützung für das Auflisten oder Schließen von Dateihandles einer Dateifreigabe, eines Dateiverzeichnisses oder einer Datei</span><span class="sxs-lookup"><span data-stu-id="7ad68-1191">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="7ad68-1192">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7ad68-1192">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="7ad68-1193">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7ad68-1193">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7ad68-1194">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7ad68-1194">Az.StorageSync</span></span>
* <span data-ttu-id="7ad68-1195">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1195">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="7ad68-1196">2.3.2 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="7ad68-1196">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7ad68-1197">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ad68-1197">Az.Accounts</span></span>
* <span data-ttu-id="7ad68-1198">Fehler behoben, aufgrund dessen in manchen Fällen eine falsche URL für Funktionsaufrufe verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="7ad68-1198">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="7ad68-1199">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="7ad68-1199">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="7ad68-1200">Problem mit Aliasen zwischen AzureRM und Azure-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-1200">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="7ad68-1201">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="7ad68-1201">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="7ad68-1202">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="7ad68-1202">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ad68-1203">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ad68-1203">Az.Compute</span></span>
* <span data-ttu-id="7ad68-1204">Die einfachen Parametersätze „New-AzVm“ und „New-AzVmss“ akzeptieren jetzt den Parameter „ProximityPlacementGroup“.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1204">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="7ad68-1205">Tippfehler in der Referenzdokumentation für „New-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-1205">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="7ad68-1206">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="7ad68-1206">Az.Dns</span></span>
* <span data-ttu-id="7ad68-1207">Tippfehler in den Hilfebeispielen zu „Set-AzDnsZone“ behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-1207">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7ad68-1208">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7ad68-1208">Az.EventGrid</span></span>
* <span data-ttu-id="7ad68-1209">Zur Verwendung der API-Version 2019-06-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1209">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="7ad68-1210">Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7ad68-1210">New cmdlets:</span></span>
    - <span data-ttu-id="7ad68-1211">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="7ad68-1211">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="7ad68-1212">Erstellt eine neue Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1212">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="7ad68-1213">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="7ad68-1213">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="7ad68-1214">Ruft die Details einer Event Grid-Domäne oder eine Liste aller Event Grid-Domänen im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1214">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="7ad68-1215">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="7ad68-1215">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="7ad68-1216">Entfernt eine Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1216">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="7ad68-1217">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="7ad68-1217">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="7ad68-1218">Generiert den freigegebenen Zugriffsschlüssel für eine Azure Event Grid-Domäne erneut.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1218">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="7ad68-1219">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="7ad68-1219">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="7ad68-1220">Ruft die freigegebenen Zugriffsschlüssel ab, die zum Veröffentlichen von Ereignissen in einer Event Grid-Domäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1220">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="7ad68-1221">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="7ad68-1221">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="7ad68-1222">Erstellt ein neues Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1222">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="7ad68-1223">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="7ad68-1223">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="7ad68-1224">Ruft die Details eines Event Grid-Domänenthemas oder eine Liste aller Event Grid-Domänenthemen unter der jeweiligen Event Grid-Domäne im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1224">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="7ad68-1225">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="7ad68-1225">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="7ad68-1226">Entfernt ein vorhandenes Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1226">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="7ad68-1227">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7ad68-1227">Updated cmdlets:</span></span>
    - <span data-ttu-id="7ad68-1228">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="7ad68-1228">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="7ad68-1229">Neue erforderliche Parameter zur Unterstützung des Pipings für die neue Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="7ad68-1229">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="7ad68-1230">Neue erforderliche Parameter zum Angeben des neuen Event Grid-Domänennamens und/oder Namens des Event Grid-Domänenthemas hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="7ad68-1230">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="7ad68-1231">Neue Parametersätze für Domänen und Domänenthemen hinzugefügt, um die Wiederverwendung vorhandener Parameter zuzulassen (‚z. B. „EndPointType“, „SubjectBeginsWith“ usw.)</span><span class="sxs-lookup"><span data-stu-id="7ad68-1231">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="7ad68-1232">Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="7ad68-1232">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="7ad68-1233">Ablaufdatum des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="7ad68-1233">Event subscription expiration date,</span></span>
            - <span data-ttu-id="7ad68-1234">Erweiterte Filterparameter</span><span class="sxs-lookup"><span data-stu-id="7ad68-1234">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="7ad68-1235">Neue Enumeration für „servicebusqueue“ als Ziel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1235">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="7ad68-1236">Verwendung der Option „All“ in „-IncludedEventType“ gesperrt und wie folgt ersetzt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1236">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="7ad68-1237">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="7ad68-1237">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="7ad68-1238">Neue optionale Parameter („Top“, „ODataQuery“ und „NextLink“) zur Unterstützung der Ergebnispaginierung und -filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1238">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="7ad68-1239">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="7ad68-1239">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="7ad68-1240">Neue erforderliche Parameter zur Unterstützung des Pipings für die Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Entfernen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="7ad68-1240">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="7ad68-1241">Neue erforderliche Parameter zum Angeben des Event Grid-Domänennamens und/oder Event Grid-Domänenthemanamens hinzugefügt, um das Entfernen vorhandener Ereignisabonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="7ad68-1241">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7ad68-1242">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7ad68-1242">Az.FrontDoor</span></span>
* <span data-ttu-id="7ad68-1243">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="7ad68-1243">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="7ad68-1244">Unterstützung von Transformationen und neuen Wert für den Operator zum automatischen Vervollständigen (RegEx) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1244">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="7ad68-1245">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="7ad68-1245">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="7ad68-1246">Neue Werte für automatisches Vervollständigen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1246">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ad68-1247">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ad68-1247">Az.Network</span></span>
* <span data-ttu-id="7ad68-1248">Unterstützung für Virtual Network-Gatewayressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1248">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="7ad68-1249">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7ad68-1249">New cmdlets</span></span>
        - <span data-ttu-id="7ad68-1250">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="7ad68-1250">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="7ad68-1251">AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="7ad68-1251">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="7ad68-1252">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7ad68-1252">New cmdlets</span></span>
        - <span data-ttu-id="7ad68-1253">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="7ad68-1253">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="7ad68-1254">„PrivatePrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1254">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="7ad68-1255">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7ad68-1255">New cmdlets</span></span>
        - <span data-ttu-id="7ad68-1256">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7ad68-1256">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="7ad68-1257">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7ad68-1257">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="7ad68-1258">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7ad68-1258">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="7ad68-1259">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7ad68-1259">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="7ad68-1260">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7ad68-1260">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="7ad68-1261">„PrivateEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1261">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="7ad68-1262">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7ad68-1262">New cmdlets</span></span>
        - <span data-ttu-id="7ad68-1263">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7ad68-1263">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7ad68-1264">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7ad68-1264">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7ad68-1265">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7ad68-1265">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7ad68-1266">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="7ad68-1266">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="7ad68-1267">Folgende Befehle für das Feature aktualisiert: UseLocalAzureIpAddress-Flag für „VpnConnection“</span><span class="sxs-lookup"><span data-stu-id="7ad68-1267">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="7ad68-1268">„New-AzVpnConnection§ „ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="7ad68-1268">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="7ad68-1269">„Set-AzVpnConnection“ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="7ad68-1269">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="7ad68-1270">Schreibgeschütztes Feld „PeeredConnections“ beim ExpressRoute-Peering hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1270">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="7ad68-1271">Schreibgeschütztes Feld „GlobalReachEnabled“ in ExpressRoute hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1271">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="7ad68-1272">Breaking Change-Attribut hinzugefügt, um auf das veraltete Feld „AllowGlobalReach“ im ExpressRouteCircuit-Modell hinzuweisen</span><span class="sxs-lookup"><span data-stu-id="7ad68-1272">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="7ad68-1273">Fehler 8756 bei der Verwendung von „TargetListenerID“ mit AzApplicationGatewayRedirectConfiguration-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-1273">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="7ad68-1274">Fehler in „New-AzApplicationGatewayPathRuleConfig“ behoben, aufgrund dessen der Regelsatz für erneutes Generieren nicht festgelegt werden konnte</span><span class="sxs-lookup"><span data-stu-id="7ad68-1274">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="7ad68-1275">Fehler bei der Anzeige von „VirtualNetworkTaps“ in „NetworkInterfaceIpConfiguration“ behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-1275">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="7ad68-1276">Cortex-Get-Cmdlets zum Auflisten aller Komponenten korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1276">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="7ad68-1277">Problem beim Erstellen des festen VirtualHub-Verweises für ExpressRouteGateways behoben (VpnGateway)</span><span class="sxs-lookup"><span data-stu-id="7ad68-1277">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="7ad68-1278">Unterstützung für Verfügbarkeitszonen in AzureFirewall und NatGateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1278">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="7ad68-1279">Cmdlet „Get-AzNetworkServiceTag“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1279">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="7ad68-1280">Unterstützung für mehrere öffentliche IP-Adressen für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1280">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="7ad68-1281">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="7ad68-1281">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="7ad68-1282">Parameter „-PublicIpAddress“ hinzugefügt, der ein oder mehre öffentliche IP-Adressobjekte akzeptiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1282">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="7ad68-1283">Parameter „- VirtualNetwork“ hinzugefügt, der ein Virtual Network-Objekt akzeptiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1283">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="7ad68-1284">Methoden „AddPublicIpAddress“ und „RemovePublicIpAddress“ für Firewallobjekte hinzugefügt (akzeptieren ein öffentliches IP-Adressobjekt als Eingabe)</span><span class="sxs-lookup"><span data-stu-id="7ad68-1284">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="7ad68-1285">Parameter „-PublicIpName“ und „-VirtualNetworkName“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1285">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="7ad68-1286">Folgende Befehle für das Feature aktualisiert: VpnClient-AAD-Authentifizierungsoptionen auf die Gatewayressource des virtuellen Netzwerkgateways festgelegt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1286">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="7ad68-1287">„New-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1287">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="7ad68-1288">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1288">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="7ad68-1289">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionaler Switch-Parameter „RemoveAadAuthentication“ zum Entfernen von VpnClient-AAD-Authentifizierungsoptionen aus dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1289">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7ad68-1290">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7ad68-1290">Az.OperationalInsights</span></span>
* <span data-ttu-id="7ad68-1291">Tarif **pergb2018** im Befehl „New-AzureRmOperationalInsightsWorkspace“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="7ad68-1291">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ad68-1292">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ad68-1292">Az.Resources</span></span>
* <span data-ttu-id="7ad68-1293">Unterstützung für zusätzliche Optionen zum Exportieren von Vorlagen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1293">Support for additional Template Export options</span></span>
    - <span data-ttu-id="7ad68-1294">Parameter „-SkipResourceNameParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1294">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="7ad68-1295">Parameter -SkipAllParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1295">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="7ad68-1296">Parameter „-Resource“ zu „Export-AzResourceGroup“ hinzugefügt, um das Filtern exportierter Ressourcen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="7ad68-1296">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7ad68-1297">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7ad68-1297">Az.ServiceFabric</span></span>
* <span data-ttu-id="7ad68-1298">Problem beim Hinzufügen des Zertifikats mit „ByExistingKeyVault“ behoben (Abruf des falschen Fingerabdrucks in manchen Fällen)</span><span class="sxs-lookup"><span data-stu-id="7ad68-1298">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ad68-1299">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ad68-1299">Az.Sql</span></span>
* <span data-ttu-id="7ad68-1300">Suffix des Advanced Threat Protection-Endpunkts korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1300">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="7ad68-1301">Durch Advanced Data Security ermöglichte Außerkraftsetzungen der Advanced Threat Protection-Richtlinie korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1301">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="7ad68-1302">Neue Cmdlets für „Management.Sql“ ermöglichen Kunden das Hinzufügen von TDE-Schlüsseln und Festlegen der TDE-Schutzvorrichtung für verwaltete Instanzen.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1302">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="7ad68-1303">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7ad68-1303">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="7ad68-1304">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7ad68-1304">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="7ad68-1305">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7ad68-1305">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="7ad68-1306">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="7ad68-1306">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="7ad68-1307">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="7ad68-1307">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7ad68-1308">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ad68-1308">Az.Storage</span></span>
* <span data-ttu-id="7ad68-1309">Unterstützung von „FileStorage“ und „SkuName Premium_ZRS“ beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="7ad68-1309">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="7ad68-1310">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ad68-1310">New-AzStorageAccount</span></span>
* <span data-ttu-id="7ad68-1311">Überarbeitete Beschreibung des Cmdlets für die Unveränderlichkeit von Blobs</span><span class="sxs-lookup"><span data-stu-id="7ad68-1311">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="7ad68-1312">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="7ad68-1312">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7ad68-1313">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ad68-1313">Az.Websites</span></span>
* <span data-ttu-id="7ad68-1314">Optimiert „Get-AzWebAppCertificate“, um nach der Ressourcengruppe auf dem Server zu filtern (nicht auf dem Client)</span><span class="sxs-lookup"><span data-stu-id="7ad68-1314">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="7ad68-1315">Switch-Parameter „-UseDisasterRecovery“ für „Get-AzWebAppSnapshot“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1315">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="7ad68-1316">2.2.0 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="7ad68-1316">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="7ad68-1317">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7ad68-1317">Az.Cdn</span></span>
* <span data-ttu-id="7ad68-1318">Es wurden Cmdlets aktualisiert, um das rulesEngine-Feature basierend auf der API-Version 2019-04-15 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1318">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ad68-1319">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ad68-1319">Az.Compute</span></span>
* <span data-ttu-id="7ad68-1320">Der Parameter `NoWait` wurde hinzugefügt, der den Vorgang startet und sofort zurückkehrt, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1320">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="7ad68-1321">Aktualisierte Cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="7ad68-1321">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7ad68-1322">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7ad68-1322">Az.EventHub</span></span>
* <span data-ttu-id="7ad68-1323">Fehlerbehebung für #9231 – Get-AzEventHubNamespace gibt keine Tags zurück</span><span class="sxs-lookup"><span data-stu-id="7ad68-1323">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="7ad68-1324">Fehlerbehebung für #9230 – Get-AzEventHubNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="7ad68-1324">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ad68-1325">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ad68-1325">Az.Network</span></span>
* <span data-ttu-id="7ad68-1326">ResourceId und InputObject wurden für NAT Gateway aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1326">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="7ad68-1327">Es wurde ein Alias für ResourceId und InputObjectr hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1327">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7ad68-1328">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7ad68-1328">Az.PolicyInsights</span></span>
* <span data-ttu-id="7ad68-1329">Fehlerbehebung für Nullverweis in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="7ad68-1329">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7ad68-1330">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7ad68-1330">Az.RecoveryServices</span></span>
* <span data-ttu-id="7ad68-1331">Minimale Aufbewahrung in Tagen für IaaSVM-Richtlinie wurde von 1 in 7 geändert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1331">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7ad68-1332">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7ad68-1332">Az.ServiceBus</span></span>
* <span data-ttu-id="7ad68-1333">Fehlerbehebung für #9182 – Get-AzServiceBusNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="7ad68-1333">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7ad68-1334">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7ad68-1334">Az.ServiceFabric</span></span>
* <span data-ttu-id="7ad68-1335">Tippfehler in Fehlermeldung für Update-AzServiceFabricReliability wurde behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-1335">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="7ad68-1336">Fehlendes Zeichen in Service Fabric-Befehlszeilen wurde behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-1336">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ad68-1337">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ad68-1337">Az.Sql</span></span>
* <span data-ttu-id="7ad68-1338">Der DnsZonePartner-Parameter für das Cmdlet New-AzureSqlInstance wurde hinzugefügt, um AutoDr für verwaltete Instanzen zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="7ad68-1338">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="7ad68-1339">Das Cmdlet Get-AzSqlDatabaseSecureConnectionPolicy wird eingestellt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1339">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="7ad68-1340">Cmdlets zum Schutz vor Bedrohungen werden in „Advanced Threat Protection“ (Erweiterter Schutz vor Bedrohungen) umbenannt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1340">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="7ad68-1341">New-AzSqlInstance – Die Parameter StorageSizeInGB und LicenseType sind jetzt optional</span><span class="sxs-lookup"><span data-stu-id="7ad68-1341">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7ad68-1342">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ad68-1342">Az.Websites</span></span>
* <span data-ttu-id="7ad68-1343">Das Problem, bei dem die Verwendung von Set-AzWebApp und Set-AzWebAppSlot mit der -WebApp-Eigenschaft die Tags entfernt hat, wurde behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-1343">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="7ad68-1344">2.1.0 – Mai 2019</span><span class="sxs-lookup"><span data-stu-id="7ad68-1344">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="7ad68-1345">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7ad68-1345">Az.ApiManagement</span></span>
* <span data-ttu-id="7ad68-1346">Es wurden neue Cmdlets zum Verwalten der Diagnose im globalen sowie im API-Bereich erstellt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1346">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="7ad68-1347">**Get-AzApiManagementDiagnostic** : Abrufen der Diagnose, die im globalen oder im API-Bereich konfiguriert wurde</span><span class="sxs-lookup"><span data-stu-id="7ad68-1347">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="7ad68-1348">**New-AzApiManagementDiagnostic** : Erstellen neuer Diagnosen im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="7ad68-1348">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="7ad68-1349">**New-AzApiManagementHttpMessageDiagnostic** : Erstellen einer Diagnoseeinstellung für die zu protokollierenden Kopfzeilen und für die Größe der Bytes für den Text</span><span class="sxs-lookup"><span data-stu-id="7ad68-1349">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="7ad68-1350">**New-AzApiManagementPipelineDiagnosticSetting** : Erstellen von Diagnoseeinstellungen für ein-/ausgehende HTTP-Nachrichten für das Gateway</span><span class="sxs-lookup"><span data-stu-id="7ad68-1350">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="7ad68-1351">**New-AzApiManagementSamplingSetting** : Erstellen der Einstellung „Sampling“ für die Anforderungen/Antworten für eine Diagnose</span><span class="sxs-lookup"><span data-stu-id="7ad68-1351">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="7ad68-1352">**Remove-AzApiManagementDiagnostic** : Entfernen einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="7ad68-1352">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="7ad68-1353">**Set-AzApiManagementDiagnostic** : Aktualisieren einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="7ad68-1353">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="7ad68-1354">Es wurden neue Cmdlets für die Cacheverwaltung im ApiManagement-Dienst erstellt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1354">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="7ad68-1355">**Get-AzApiManagementCache** : Abrufen der Details des durch den Bezeichner angegebenen Caches oder aller Caches</span><span class="sxs-lookup"><span data-stu-id="7ad68-1355">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="7ad68-1356">**New-AzApiManagementCache** : Erstellen eines neuen „standardmäßigen“ Caches oder eines Caches in einer bestimmten „Region“ von Azure</span><span class="sxs-lookup"><span data-stu-id="7ad68-1356">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="7ad68-1357">**Remove-AzApiManagementCache** : Entfernen eines Caches</span><span class="sxs-lookup"><span data-stu-id="7ad68-1357">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="7ad68-1358">**Update-AzApiManagementCache** : Aktualisieren eines Caches</span><span class="sxs-lookup"><span data-stu-id="7ad68-1358">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="7ad68-1359">Es wurden neue Cmdlets zur Verwaltung von API-Schemas erstellt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1359">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="7ad68-1360">**New-AzApiManagementSchema** : Erstellen eines neuen Schemas für eine API</span><span class="sxs-lookup"><span data-stu-id="7ad68-1360">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="7ad68-1361">**Get-AzApiManagementSchema** : Abrufen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="7ad68-1361">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="7ad68-1362">**Remove-AzApiManagementSchema** : Entfernen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="7ad68-1362">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="7ad68-1363">**Set-AzApiManagementSchema** : Aktualisieren des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="7ad68-1363">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="7ad68-1364">Es wurde ein neues Cmdlet zum Generieren eines Benutzertokens erstellt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1364">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="7ad68-1365">**New-AzApiManagementUserToken** : Generieren eines neuen Benutzertokens, das standardmäßig für acht Stunden gültig ist. Mit diesem Cmdlet kann das Token für den „GIT“-Benutzer generiert werden./</span><span class="sxs-lookup"><span data-stu-id="7ad68-1365">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="7ad68-1366">Es wurde ein neues Cmdlet zum Abrufen des Netzwerkstatus erstellt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1366">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="7ad68-1367">**Get-AzApiManagementNetworkStatus** : Abrufen der Netzwerkstatuskonnektivität von Ressourcen, von denen der API Management-Dienst abhängig ist</span><span class="sxs-lookup"><span data-stu-id="7ad68-1367">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="7ad68-1368">Dies ist hilfreich, wenn Sie den ApiManagement-Dienst in einem virtuellen Netzwerk bereitstellen und überprüfen, ob eine der Abhängigkeiten fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1368">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="7ad68-1369">Das Cmdlet **New-AzApiManagement** wurde zum Verwalten des ApiManagement-Diensts aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1369">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="7ad68-1370">Die Unterstützung für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1370">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="7ad68-1371">Die Unterstützung zum Aktivieren des Flags „EnableClientCertificate“ für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1371">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="7ad68-1372">Das neue Cmdlet **New-AzApiManagementSslSetting** ermöglicht die Konfiguration der „TLS/SSL“-Einstellung für „Back-End“ und „Front-End“</span><span class="sxs-lookup"><span data-stu-id="7ad68-1372">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="7ad68-1373">Dies kann auch dazu verwendet werden, um „Verschlüsselungen“ wie „3DES“ und „ServerProtokolle“ wie „Http2“ für das „Front-End“ eines ApiManagement-Diensts zu konfigurieren</span><span class="sxs-lookup"><span data-stu-id="7ad68-1373">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="7ad68-1374">Die Unterstützung für die Konfiguration des Hostnamens „DeveloperPortal“ wurde zum ApiManagement-Dienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1374">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="7ad68-1375">Die **Get-AzApiManagementSsoToken** -Cmdlets wurden aktualisiert, um das Objekt „PsApiManagement“ als Eingabe zu übernehmen</span><span class="sxs-lookup"><span data-stu-id="7ad68-1375">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="7ad68-1376">Das Cmdlet wurde aktualisiert, um Fehlermeldungen inline anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="7ad68-1376">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="7ad68-1377">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Fehlercode: ValidationError-Fehlermeldung: Mindestens ein Feld enthält ungültige Werte: Fehlerdetails: [Code=ValidationError, Message=Fehler in Element 'log-to-eventhub' in Zeile 3, Spalte 10: Protokollierungstool nicht gefunden, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="7ad68-1377">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="7ad68-1378">Cmdlet **Export-AzApiManagementApi** wurde für den Export von APIs im Format „OpenApi 3.0“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1378">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="7ad68-1379">Cmdlet **Import-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1379">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="7ad68-1380">Zum Importieren der API aus der „OpenApi 3.0“-Dokumentspezifikation</span><span class="sxs-lookup"><span data-stu-id="7ad68-1380">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="7ad68-1381">Zur Außerkraftsetzung der „PsApiManagementSchema“-Eigenschaft, die in einem beliebigen Dokument („Swagger“, „Wadl“, „Wsdl“, „OpenApi“) angegeben ist</span><span class="sxs-lookup"><span data-stu-id="7ad68-1381">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="7ad68-1382">Zur Außerkraftsetzung der „ServiceUrl“-Eigenschaft, die in einem beliebigen Dokument angegeben ist</span><span class="sxs-lookup"><span data-stu-id="7ad68-1382">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="7ad68-1383">Cmdlet **Get-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="7ad68-1383">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="7ad68-1384">Cmdlet **Set-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ und im Format mit XML-Escapezeichen mit „xml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="7ad68-1384">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="7ad68-1385">Cmdlet **New-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1385">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="7ad68-1386">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="7ad68-1386">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="7ad68-1387">Zum Erstellen einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="7ad68-1387">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="7ad68-1388">Zum Klonen einer API mithilfe von „SourceApiId“ und „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="7ad68-1388">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="7ad68-1389">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="7ad68-1389">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="7ad68-1390">Cmdlet **Set-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1390">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="7ad68-1391">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="7ad68-1391">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="7ad68-1392">Zum Aktualisieren einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="7ad68-1392">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="7ad68-1393">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="7ad68-1393">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="7ad68-1394">Cmdlet **New-AzApiManagementRevision** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1394">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="7ad68-1395">Zum Klonen (Kopiertags, Produkte, Vorgänge und Richtlinien) einer vorhandenen Version mithilfe von „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="7ad68-1395">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="7ad68-1396">Die neue Version übernimmt die „ApiId“ des übergeordneten Elements</span><span class="sxs-lookup"><span data-stu-id="7ad68-1396">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="7ad68-1397">Zum Bereitstellen einer „ApiRevisionDescription“</span><span class="sxs-lookup"><span data-stu-id="7ad68-1397">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="7ad68-1398">Zur Außerkraftsetzung der „ServiceUrl“ beim Klonen einer API</span><span class="sxs-lookup"><span data-stu-id="7ad68-1398">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="7ad68-1399">Cmdlet **New-AzApiManagementIdentityProvider** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1399">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="7ad68-1400">Zum Konfigurieren von „AAD“ oder „AADB2C“ mit einer „Authority“</span><span class="sxs-lookup"><span data-stu-id="7ad68-1400">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="7ad68-1401">Zum Einrichten von „SignupPolicy“, „SigninPolicy“, „ProfileEditingPolicy“ und „PasswordResetPolicy“</span><span class="sxs-lookup"><span data-stu-id="7ad68-1401">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="7ad68-1402">Cmdlet **New-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1402">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="7ad68-1403">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="7ad68-1403">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="7ad68-1404">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="7ad68-1404">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="7ad68-1405">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1405">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="7ad68-1406">Cmdlet **Set-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1406">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="7ad68-1407">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="7ad68-1407">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="7ad68-1408">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="7ad68-1408">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="7ad68-1409">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1409">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="7ad68-1410">Folgende Cmdlets wurden aktualisiert, um „ResourceId“ als Eingabe zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="7ad68-1410">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="7ad68-1411">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="7ad68-1411">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="7ad68-1412">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="7ad68-1412">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="7ad68-1413">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="7ad68-1413">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="7ad68-1414">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="7ad68-1414">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="7ad68-1415">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="7ad68-1415">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="7ad68-1416">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="7ad68-1416">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="7ad68-1417">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="7ad68-1417">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="7ad68-1418">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="7ad68-1418">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="7ad68-1419">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="7ad68-1419">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="7ad68-1420">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="7ad68-1420">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="7ad68-1421">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="7ad68-1421">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="7ad68-1422">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="7ad68-1422">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7ad68-1423">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7ad68-1423">Az.Automation</span></span>
* <span data-ttu-id="7ad68-1424">Get-AzAutomationJobOutputRecord wurde aktualisiert, um JSON- und Textdatensatzwerte zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1424">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="7ad68-1425">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="7ad68-1425">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="7ad68-1426">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="7ad68-1426">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="7ad68-1427">Das Verhalten von Start-AzAutomationDscCompilationJob wurde geändert, um den Auftrag einfach zu starten, anstatt auf dessen Abschluss zu warten</span><span class="sxs-lookup"><span data-stu-id="7ad68-1427">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="7ad68-1428">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="7ad68-1428">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="7ad68-1429">Fehlerbehebung für Get-AzAutomationDscNode, wenn die Verwendung von „-Name“ alle Knoten zurückgibt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1429">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="7ad68-1430">Jetzt wird nur der übereinstimmende Knoten zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="7ad68-1430">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ad68-1431">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ad68-1431">Az.Compute</span></span>
* <span data-ttu-id="7ad68-1432">Parameter „ProtectFromScaleIn“ und „ProtectFromScaleSetAction“ wurden zum Cmdlet „Update-AzVmssVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1432">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="7ad68-1433">Der jetzt festgelegte wimple-Parameter „New-AzVM“ verwendet standardmäßig einen verfügbaren Standort, wenn „East US“ (USA, Osten) nicht unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="7ad68-1433">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7ad68-1434">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7ad68-1434">Az.DataLakeStore</span></span>
* <span data-ttu-id="7ad68-1435">Das ADLS-SDK wurde aktualisiert, um „HttpClient“ zu verwenden und Datenebenentests wurden mit dem Azure-Framework integriert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1435">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7ad68-1436">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7ad68-1436">Az.Monitor</span></span>
* <span data-ttu-id="7ad68-1437">Fehlerbehebung bei falschen Parameternamen in Hilfebeispielen</span><span class="sxs-lookup"><span data-stu-id="7ad68-1437">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ad68-1438">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ad68-1438">Az.Network</span></span>
* <span data-ttu-id="7ad68-1439">DisableBgpRoutePropagation-Flag wurde zur Ausgabe der effektiven Routentabelle hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1439">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="7ad68-1440">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7ad68-1440">Updated cmdlet:</span></span>
        - <span data-ttu-id="7ad68-1441">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="7ad68-1441">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="7ad68-1442">Fehlerbehebung von doppeltem Bindestrich in Dokumentation von New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7ad68-1442">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ad68-1443">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ad68-1443">Az.Resources</span></span>
* <span data-ttu-id="7ad68-1444">Neues Cmdlet „Get-AzureRmDenyAssignment“ zum Abrufen von Ablehnungszuweisungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1444">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ad68-1445">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ad68-1445">Az.Sql</span></span>
* <span data-ttu-id="7ad68-1446">„Advanced Threat Protection“-Cmdlets in „Advanced Data Security“ umbenennen und Sicherheitsrisikobewertung standardmäßig aktivieren</span><span class="sxs-lookup"><span data-stu-id="7ad68-1446">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="7ad68-1447">2.0.0: Mai 2019</span><span class="sxs-lookup"><span data-stu-id="7ad68-1447">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7ad68-1448">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ad68-1448">Az.Accounts</span></span>
* <span data-ttu-id="7ad68-1449">Authentifizierungsbibliothek aktualisiert, um ADFS-Probleme mit der Authentifizierung per Benutzername/Kennwort zu beheben</span><span class="sxs-lookup"><span data-stu-id="7ad68-1449">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7ad68-1450">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7ad68-1450">Az.CognitiveServices</span></span>
* <span data-ttu-id="7ad68-1451">Ausschließliche Anzeige des Bing-Haftungsausschlusses für Bing-Suchdienste</span><span class="sxs-lookup"><span data-stu-id="7ad68-1451">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="7ad68-1452">Fehler behoben, der zu einem Fehler bei der Kontoerstellung führte</span><span class="sxs-lookup"><span data-stu-id="7ad68-1452">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ad68-1453">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ad68-1453">Az.Compute</span></span>
* <span data-ttu-id="7ad68-1454">Feature für die Näherungsplatzierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="7ad68-1454">Proximity placement group feature.</span></span>
    - <span data-ttu-id="7ad68-1455">Die folgenden neuen Cmdlets wurden hinzugefügt:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="7ad68-1455">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="7ad68-1456">Der neue Parameter „ProximityPlacementGroupId“ wurde zu den folgenden Cmdlets hinzugefügt:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="7ad68-1456">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="7ad68-1457">Der Parameter „StorageAccountType“ wurde zu „New-AzGalleryImageVersion“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1457">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="7ad68-1458">„TargetRegion“ von „New-AzGalleryImageVersion“ kann „StorageAccountType“ enthalten.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1458">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="7ad68-1459">Switch-Parameter „SkipShutdown“ wurde zu „Stop-AzVM“ und „Stop-AzVmss“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1459">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="7ad68-1460">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="7ad68-1460">Breaking changes</span></span>
    - <span data-ttu-id="7ad68-1461">„Set-AzVMBootDiagnostics“ in „Set-AzVMBootDiagnostic“ geändert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1461">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="7ad68-1462">„Export-AzLogAnalyticThrottledRequests“ in „Export-AzLogAnalyticThrottledRequests“ geändert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1462">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="7ad68-1463">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="7ad68-1463">Az.DeploymentManager</span></span>
* <span data-ttu-id="7ad68-1464">Erste allgemein verfügbare Version der Azure-Bereitstellungs-Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7ad68-1464">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="7ad68-1465">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="7ad68-1465">Az.Dns</span></span>
* <span data-ttu-id="7ad68-1466">Automatische Delegierung des DNS-Namenservers</span><span class="sxs-lookup"><span data-stu-id="7ad68-1466">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="7ad68-1467">Das Cmdlet zum Erstellen einer DNS-Zone akzeptiert den übergeordneten Zonennamen als zusätzlichen optionalen Parameter.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1467">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="7ad68-1468">NS-Einträge in der übergeordneten Zone für neu erstellte untergeordnete Zone hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1468">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7ad68-1469">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7ad68-1469">Az.FrontDoor</span></span>
* <span data-ttu-id="7ad68-1470">Erste allgemein verfügbare Version der Azure Frontdoor-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7ad68-1470">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="7ad68-1471">WAF-Cmdlets so umbenannt, dass sie „Waf“ enthalten</span><span class="sxs-lookup"><span data-stu-id="7ad68-1471">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="7ad68-1472">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7ad68-1472">Az.HDInsight</span></span>
* <span data-ttu-id="7ad68-1473">Zwei Cmdlets entfernt:</span><span class="sxs-lookup"><span data-stu-id="7ad68-1473">Removed two cmdlets:</span></span>
    - <span data-ttu-id="7ad68-1474">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7ad68-1474">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="7ad68-1475">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7ad68-1475">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="7ad68-1476">Neues Cmdlet „Set-AzHDInsightGatewayCredential“ hinzugefügt, um „Grant-AzHDInsightHttpServicesAccess“ zu ersetzen</span><span class="sxs-lookup"><span data-stu-id="7ad68-1476">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="7ad68-1477">Cmdlet „Get-AzHDInsightJobOutput“ aktualisiert, um zwischen Leserrolle und HDInsight-Bedienerrolle zu unterscheiden:</span><span class="sxs-lookup"><span data-stu-id="7ad68-1477">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="7ad68-1478">Benutzer mit der Rolle „Leser“ müssen den Parameter „DefaultStorageAccountKey“ explizit angeben, andernfalls treten Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1478">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="7ad68-1479">Benutzer mit der Rolle des HDInsight-Bedieners sind nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1479">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7ad68-1480">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7ad68-1480">Az.Monitor</span></span>
* <span data-ttu-id="7ad68-1481">Neue Cmdlets für SQR-API (Scheduled Query Rule, geplante Abfrageregel)</span><span class="sxs-lookup"><span data-stu-id="7ad68-1481">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="7ad68-1482">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="7ad68-1482">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="7ad68-1483">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="7ad68-1483">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="7ad68-1484">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="7ad68-1484">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="7ad68-1485">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="7ad68-1485">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="7ad68-1486">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="7ad68-1486">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="7ad68-1487">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="7ad68-1487">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="7ad68-1488">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7ad68-1488">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7ad68-1489">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7ad68-1489">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7ad68-1490">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7ad68-1490">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7ad68-1491">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7ad68-1491">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7ad68-1492">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7ad68-1492">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7ad68-1493">[Weitere Informationen](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) zur SQR-API</span><span class="sxs-lookup"><span data-stu-id="7ad68-1493">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="7ad68-1494">„Az.Monitor.md“ aktualisiert, um Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch) einzuschließen</span><span class="sxs-lookup"><span data-stu-id="7ad68-1494">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ad68-1495">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ad68-1495">Az.Network</span></span>
* <span data-ttu-id="7ad68-1496">Unterstützung für NAT-Gatewayressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1496">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="7ad68-1497">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7ad68-1497">New cmdlets</span></span>
        - <span data-ttu-id="7ad68-1498">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7ad68-1498">New-AzNatGateway</span></span>
        - <span data-ttu-id="7ad68-1499">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7ad68-1499">Get-AzNatGateway</span></span>
        - <span data-ttu-id="7ad68-1500">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7ad68-1500">Set-AzNatGateway</span></span>
        - <span data-ttu-id="7ad68-1501">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7ad68-1501">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="7ad68-1502">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7ad68-1502">Updated cmdlets</span></span>
        - <span data-ttu-id="7ad68-1503">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="7ad68-1503">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="7ad68-1504">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="7ad68-1504">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="7ad68-1505">Folgende Befehle für das Feature aktualisiert: Benutzerdefinierte Routen für Brooklyn-Gateway festgelegt/entfernt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1505">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="7ad68-1506">„New-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1506">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="7ad68-1507">„Set-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1507">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7ad68-1508">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7ad68-1508">Az.PolicyInsights</span></span>
* <span data-ttu-id="7ad68-1509">Unterstützung für die Abfrage von Richtlinienauswertungsdetails</span><span class="sxs-lookup"><span data-stu-id="7ad68-1509">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="7ad68-1510">Parameter „-Expand“ zu „Get-AzPolicyState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1510">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="7ad68-1511">Unterstützung für „-Expand PolicyEvaluationDetails“</span><span class="sxs-lookup"><span data-stu-id="7ad68-1511">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7ad68-1512">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7ad68-1512">Az.RecoveryServices</span></span>
* <span data-ttu-id="7ad68-1513">Unterstützung für abonnementübergreifende Azure-zu-Azure-Sitewiederherstellung</span><span class="sxs-lookup"><span data-stu-id="7ad68-1513">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="7ad68-1514">Markierung anstehender wichtiger Änderungen für Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="7ad68-1514">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="7ad68-1515">Fehlerbehebung für Azure Site Recovery-Wiederherstellungsplan und -Aktionsplan</span><span class="sxs-lookup"><span data-stu-id="7ad68-1515">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="7ad68-1516">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Netzwerkzuordnung für Azure zu Azure</span><span class="sxs-lookup"><span data-stu-id="7ad68-1516">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="7ad68-1517">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Schutzrichtung für Azure zu Azure für verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="7ad68-1517">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="7ad68-1518">Weitere kleinere Korrekturen</span><span class="sxs-lookup"><span data-stu-id="7ad68-1518">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="7ad68-1519">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="7ad68-1519">Az.Relay</span></span>
* <span data-ttu-id="7ad68-1520">Korrektur von Tippfehlern in Kundennachrichten</span><span class="sxs-lookup"><span data-stu-id="7ad68-1520">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7ad68-1521">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7ad68-1521">Az.ServiceBus</span></span>
* <span data-ttu-id="7ad68-1522">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1522">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7ad68-1523">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ad68-1523">Az.Storage</span></span>
* <span data-ttu-id="7ad68-1524">Upgrade auf Speicherclientbibliothek 10.0.1 (Namespace aller Objekte von diesem SDK von „Microsoft.WindowsAzure.Storage. *“ in „Microsoft.Azure.Storage.* “ geändert)</span><span class="sxs-lookup"><span data-stu-id="7ad68-1524">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage. *' to 'Microsoft.Azure.Storage.* ')</span></span>
* <span data-ttu-id="7ad68-1525">Upgrade auf Microsoft.Azure.Management.Storage 11.0.0, um die neue API-Version 2019-04-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="7ad68-1525">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="7ad68-1526">Art des Standardspeicherkontos bei der Speicherkontoerstellung von „Storage“ in „StorageV2“ geändert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1526">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="7ad68-1527">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ad68-1527">New-AzStorageAccount</span></span>
* <span data-ttu-id="7ad68-1528">Vom Speicherkonto-Cmdlet ausgegebener SKU-Name (Sku.Name) durch Hinzufügen eines Unterstrichs an SKU-Eingabename angepasst (Beispiel: „StandardLRS“ > „Standard_LRS“).</span><span class="sxs-lookup"><span data-stu-id="7ad68-1528">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="7ad68-1529">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ad68-1529">New-AzStorageAccount</span></span>
    - <span data-ttu-id="7ad68-1530">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ad68-1530">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="7ad68-1531">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ad68-1531">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7ad68-1532">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ad68-1532">Az.Websites</span></span>
* <span data-ttu-id="7ad68-1533">Die Eigenschaft „Kind“ wird nun für PSSite-Objekte festgelegt, die von „Get-AzWebApp“ zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1533">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="7ad68-1534">„Get-AzWebApp\*Metrics“ und „Get-AzAppServicePlanMetrics“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1534">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="7ad68-1535">1.8.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="7ad68-1535">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7ad68-1536">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="7ad68-1536">Highlights since the last major release</span></span>
* <span data-ttu-id="7ad68-1537">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="7ad68-1537">General availability of `Az` module</span></span>
* <span data-ttu-id="7ad68-1538">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1538">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7ad68-1539">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1539">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7ad68-1540">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1540">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7ad68-1541">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1541">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7ad68-1542">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1542">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7ad68-1543">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="7ad68-1543">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7ad68-1544">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ad68-1544">Az.Accounts</span></span>
* <span data-ttu-id="7ad68-1545">„Uninstall-AzureRm“ aktualisiert, um Module unter Mac ordnungsgemäß zu löschen</span><span class="sxs-lookup"><span data-stu-id="7ad68-1545">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7ad68-1546">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7ad68-1546">Az.Batch</span></span>
* <span data-ttu-id="7ad68-1547">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1547">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7ad68-1548">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7ad68-1548">Az.Cdn</span></span>
* <span data-ttu-id="7ad68-1549">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1549">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7ad68-1550">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7ad68-1550">Az.CognitiveServices</span></span>
* <span data-ttu-id="7ad68-1551">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1551">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ad68-1552">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ad68-1552">Az.Compute</span></span>
* <span data-ttu-id="7ad68-1553">Problem mit der AEM-Installation behoben, wenn die Ressourcen-IDs von Datenträgern Ressourcengruppen in Kleinbuchstaben enthielten</span><span class="sxs-lookup"><span data-stu-id="7ad68-1553">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="7ad68-1554">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1554">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7ad68-1555">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1555">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7ad68-1556">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7ad68-1556">Az.DataFactory</span></span>
* <span data-ttu-id="7ad68-1557">„SsisProperties“ hinzugefügt, falls „NodeCount“ für verwaltete Integration Runtime nicht NULL ist</span><span class="sxs-lookup"><span data-stu-id="7ad68-1557">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7ad68-1558">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7ad68-1558">Az.DataLakeStore</span></span>
* <span data-ttu-id="7ad68-1559">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1559">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7ad68-1560">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7ad68-1560">Az.EventGrid</span></span>
* <span data-ttu-id="7ad68-1561">Hilfetext für Endpunkt aktualisiert, um anzugeben, dass Ressourcen erstellt werden müssen, bevor die Cmdlets zum Erstellen/Aktualisieren von Ereignisabonnements verwendet werden</span><span class="sxs-lookup"><span data-stu-id="7ad68-1561">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7ad68-1562">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7ad68-1562">Az.EventHub</span></span>
* <span data-ttu-id="7ad68-1563">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1563">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7ad68-1564">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7ad68-1564">Az.HDInsight</span></span>
* <span data-ttu-id="7ad68-1565">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1565">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7ad68-1566">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7ad68-1566">Az.IotHub</span></span>
* <span data-ttu-id="7ad68-1567">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1567">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7ad68-1568">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7ad68-1568">Az.KeyVault</span></span>
* <span data-ttu-id="7ad68-1569">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1569">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7ad68-1570">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1570">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="7ad68-1571">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7ad68-1571">Az.MachineLearning</span></span>
* <span data-ttu-id="7ad68-1572">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1572">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="7ad68-1573">Az.Media</span><span class="sxs-lookup"><span data-stu-id="7ad68-1573">Az.Media</span></span>
* <span data-ttu-id="7ad68-1574">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1574">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7ad68-1575">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7ad68-1575">Az.Monitor</span></span>
  * <span data-ttu-id="7ad68-1576">Neue Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch)</span><span class="sxs-lookup"><span data-stu-id="7ad68-1576">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="7ad68-1577">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="7ad68-1577">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="7ad68-1578">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="7ad68-1578">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="7ad68-1579">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7ad68-1579">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="7ad68-1580">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7ad68-1580">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="7ad68-1581">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7ad68-1581">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="7ad68-1582">Monitor SDK auf Version 0.22.0-preview aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1582">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ad68-1583">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ad68-1583">Az.Network</span></span>
* <span data-ttu-id="7ad68-1584">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1584">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7ad68-1585">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1585">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="7ad68-1586">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="7ad68-1586">Az.NotificationHubs</span></span>
* <span data-ttu-id="7ad68-1587">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1587">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7ad68-1588">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7ad68-1588">Az.OperationalInsights</span></span>
* <span data-ttu-id="7ad68-1589">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1589">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="7ad68-1590">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="7ad68-1590">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="7ad68-1591">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1591">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7ad68-1592">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7ad68-1592">Az.RecoveryServices</span></span>
* <span data-ttu-id="7ad68-1593">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1593">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7ad68-1594">Tabellenformat für SQL auf Azure-VM aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1594">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="7ad68-1595">Alternative Methode zum Abrufen des Speicherorts in „AzureFileShare“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1595">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="7ad68-1596">„ScheduleRunDays“ in SchedulePolicy-Objekt gemäß Zeitzone aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1596">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7ad68-1597">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7ad68-1597">Az.RedisCache</span></span>
* <span data-ttu-id="7ad68-1598">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1598">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ad68-1599">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ad68-1599">Az.Resources</span></span>
* <span data-ttu-id="7ad68-1600">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1600">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ad68-1601">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ad68-1601">Az.Sql</span></span>
* <span data-ttu-id="7ad68-1602">Abhängigkeit vom Monitor SDK durch allgemeinen Code ersetzt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1602">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="7ad68-1603">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1603">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7ad68-1604">Verbesserter Prozess für Klassifizierung mehrerer Spalten</span><span class="sxs-lookup"><span data-stu-id="7ad68-1604">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="7ad68-1605">SKU-Eigenschaften (SKU-Name, Familie, Kapazität) in Antwort von „Get-AzSqlServerServiceObjective“ aufgenommen und standardmäßig als Tabelle formatiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1605">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="7ad68-1606">Möglichkeit zum Ausführen von „Get-AzSqlServerServiceObjective“ nach Standort, ohne dass bereits ein Server in der Region vorhanden sein muss</span><span class="sxs-lookup"><span data-stu-id="7ad68-1606">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="7ad68-1607">Unterstützung für Zeitzonenparameter bei der Erstellung einer verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="7ad68-1607">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="7ad68-1608">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1608">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7ad68-1609">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ad68-1609">Az.Websites</span></span>
* <span data-ttu-id="7ad68-1610">„Set-AzWebApp“ und „Set-AzWebAppSlot“ korrigiert, sodass die Tags bei der Ausführung nicht entfernt werden</span><span class="sxs-lookup"><span data-stu-id="7ad68-1610">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="7ad68-1611">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1611">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7ad68-1612">WebSites SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1612">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="7ad68-1613">AdminSiteName-Eigenschaft aus „PSAppServicePlan“ entfernt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1613">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="7ad68-1614">1.7.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="7ad68-1614">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7ad68-1615">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="7ad68-1615">Highlights since the last major release</span></span>
* <span data-ttu-id="7ad68-1616">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="7ad68-1616">General availability of `Az` module</span></span>
* <span data-ttu-id="7ad68-1617">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1617">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7ad68-1618">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1618">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7ad68-1619">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1619">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7ad68-1620">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1620">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7ad68-1621">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1621">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7ad68-1622">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="7ad68-1622">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7ad68-1623">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ad68-1623">Az.Accounts</span></span>
* <span data-ttu-id="7ad68-1624">„Add-AzEnvironment“ und „Set-AzEnvironment“ aktualisiert, um den Parameter „AzureAnalysisServicesEndpointResourceId“ zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="7ad68-1624">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7ad68-1625">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7ad68-1625">Az.AnalysisServices</span></span>
* <span data-ttu-id="7ad68-1626">ServiceClient wird in Cmdlets für die Datenebene verwendet, und die ursprüngliche Authentifizierungslogik wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1626">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="7ad68-1627">„Add-AzureASAccount“ wird als Wrapper von „Connect-AzAccount“ festgelegt, um einen Breaking Change zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1627">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7ad68-1628">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7ad68-1628">Az.Automation</span></span>
* <span data-ttu-id="7ad68-1629">Fehler des Cmdlets „Fixed New-AzAutomationSoftwareUpdateConfiguration“ für Einschlüsse behoben.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1629">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="7ad68-1630">Die Parameter „IncludedKbNumber“ und „IncludedPackageNameMask“ sollten nun funktionieren.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1630">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="7ad68-1631">Fehlerbehebung für eine dynamische Gruppe der Azure Automation-Updateverwaltung</span><span class="sxs-lookup"><span data-stu-id="7ad68-1631">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ad68-1632">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ad68-1632">Az.Compute</span></span>
* <span data-ttu-id="7ad68-1633">Parameter „HyperVGeneration“ zu „New-AzDiskConfig“ und „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1633">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="7ad68-1634">Zulassen der VM-Erstellung mit einem Katalogimage aus anderen Mandanten</span><span class="sxs-lookup"><span data-stu-id="7ad68-1634">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="7ad68-1635">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7ad68-1635">Az.ContainerInstance</span></span>
* <span data-ttu-id="7ad68-1636">Problem im Parameter „-Command“ von „New-AzContainerGroup“ behoben, das dazu führte, dass ein nachgestelltes leeres Argument hinzugefügt wurde</span><span class="sxs-lookup"><span data-stu-id="7ad68-1636">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7ad68-1637">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7ad68-1637">Az.DataFactory</span></span>
* <span data-ttu-id="7ad68-1638">Version des ADF .NET SDK auf 3.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1638">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="7ad68-1639">Cmdlet „Set-AzDataFactoryV2“ mit zusätzlichen Parametern für RepoConfiguration-Einstellungen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1639">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ad68-1640">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ad68-1640">Az.Resources</span></span>
* <span data-ttu-id="7ad68-1641">Verarbeitung von Anbietern für „Get-AzResource“ bei der Angabe der Parameter „-ResourceId“ oder „-ResourceGroupName“, „-Name“ und „-ResourceType“ verbessert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1641">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="7ad68-1642">Fehlerbehandlung für „Test-AzDeployment“ und „Test-AzResourceGroupDeployment“ verbessert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1642">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="7ad68-1643">Behandlung von außerhalb der Bereitstellungsüberprüfung aufgetretenen Fehlern und stattdessen Aufnahme in die Ausgabe des Befehls</span><span class="sxs-lookup"><span data-stu-id="7ad68-1643">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="7ad68-1644">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="7ad68-1644">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="7ad68-1645">Switch-Parameter „-IgnoreDynamicParameters“ zu Bereitstellungs-Cmdlets hinzugefügt, um Aufforderung in Skript- und Auftragsszenarien zu überspringen</span><span class="sxs-lookup"><span data-stu-id="7ad68-1645">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="7ad68-1646">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="7ad68-1646">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ad68-1647">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ad68-1647">Az.Sql</span></span>
* <span data-ttu-id="7ad68-1648">Unterstützung für Klassifizierung von Datenbankdaten</span><span class="sxs-lookup"><span data-stu-id="7ad68-1648">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7ad68-1649">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ad68-1649">Az.Storage</span></span>
* <span data-ttu-id="7ad68-1650">Melden eines ausführlichen Fehlers beim Erstellen des Storage-Kontexts mit dem Parameter „-UseConnectedAccount“, aber ohne Azure-Anmeldekonto</span><span class="sxs-lookup"><span data-stu-id="7ad68-1650">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="7ad68-1651">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7ad68-1651">New-AzStorageContext</span></span>
* <span data-ttu-id="7ad68-1652">Unterstützung für das Verwalten von Blobdiensteigenschaften eines bestimmten Storage-Kontos mit einer API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="7ad68-1652">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="7ad68-1653">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="7ad68-1653">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="7ad68-1654">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="7ad68-1654">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="7ad68-1655">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7ad68-1655">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="7ad68-1656">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7ad68-1656">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="7ad68-1657">Unterstützung von „-AsJob“ für Cmdlets für den Upload und Download von Blobs und Dateien</span><span class="sxs-lookup"><span data-stu-id="7ad68-1657">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="7ad68-1658">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7ad68-1658">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="7ad68-1659">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7ad68-1659">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="7ad68-1660">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7ad68-1660">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="7ad68-1661">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7ad68-1661">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="7ad68-1662">1.6.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="7ad68-1662">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7ad68-1663">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="7ad68-1663">Highlights since the last major release</span></span>
* <span data-ttu-id="7ad68-1664">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="7ad68-1664">General availability of `Az` module</span></span>
* <span data-ttu-id="7ad68-1665">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1665">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7ad68-1666">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1666">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7ad68-1667">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1667">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7ad68-1668">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1668">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7ad68-1669">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1669">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7ad68-1670">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="7ad68-1670">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7ad68-1671">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7ad68-1671">Az.Automation</span></span>
* <span data-ttu-id="7ad68-1672">Änderung an der Azure Automation-Updateverwaltung, um die folgenden neuen Features zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="7ad68-1672">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="7ad68-1673">Dynamische Gruppierung</span><span class="sxs-lookup"><span data-stu-id="7ad68-1673">Dynamic grouping</span></span>
    * <span data-ttu-id="7ad68-1674">Pre-/Post-Skripts</span><span class="sxs-lookup"><span data-stu-id="7ad68-1674">Pre-Post script</span></span>
    * <span data-ttu-id="7ad68-1675">Neustarteinstellung</span><span class="sxs-lookup"><span data-stu-id="7ad68-1675">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ad68-1676">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ad68-1676">Az.Compute</span></span>
* <span data-ttu-id="7ad68-1677">Problem mit der Pfadauflösung in „Get-AzVmBootDiagnosticsData“ behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-1677">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="7ad68-1678">Computeclientbibliothek auf 25.0.0. aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1678">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7ad68-1679">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7ad68-1679">Az.KeyVault</span></span>
* <span data-ttu-id="7ad68-1680">Unterstützung für Platzhalterzeichen zu KeyVault-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1680">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ad68-1681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ad68-1681">Az.Network</span></span>
* <span data-ttu-id="7ad68-1682">Threat Intelligence-Unterstützung für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1682">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="7ad68-1683">Ressource der obersten Ebene für Application Gateway-Firewallrichtlinie und benutzerdefinierte Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1683">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7ad68-1684">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7ad68-1684">Az.RecoveryServices</span></span>
* <span data-ttu-id="7ad68-1685">SnapshotRetentionInDays in Azure-VM-Richtlinie hinzugefügt, um sofortigen Wiederherstellungspunkt zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="7ad68-1685">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="7ad68-1686">Pipe-Unterstützung für das Aufheben der Registrierung eines Containers hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1686">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ad68-1687">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ad68-1687">Az.Resources</span></span>
* <span data-ttu-id="7ad68-1688">Unterstützung für Platzhalterzeichen für Get-AzResource und Get-AzResourceGroup aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1688">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="7ad68-1689">Anmeldeinformationen aktualisiert, die beim Senden generischer Aufrufe an ARM verwendet werden</span><span class="sxs-lookup"><span data-stu-id="7ad68-1689">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ad68-1690">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ad68-1690">Az.Sql</span></span>
* <span data-ttu-id="7ad68-1691">Der Cmdlet-Parameter der Bedrohungserkennung (ExcludeDetectionType) wurde von „DetectionType“ in „string[]“ geändert, um ihn zukunftssicher zu machen, wenn neue DetectionTypes-Elemente hinzugefügt werden, und um AutoVervollständigen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1691">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7ad68-1692">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ad68-1692">Az.Storage</span></span>
* <span data-ttu-id="7ad68-1693">Unterstützung von Get-/Set-/Remove-Verwaltungsrichtlinien für Speicherkonto hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1693">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="7ad68-1694">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7ad68-1694">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7ad68-1695">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7ad68-1695">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7ad68-1696">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7ad68-1696">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7ad68-1697">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="7ad68-1697">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="7ad68-1698">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="7ad68-1698">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="7ad68-1699">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="7ad68-1699">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7ad68-1700">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ad68-1700">Az.Websites</span></span>
* <span data-ttu-id="7ad68-1701">ARM-Vorlagenfehler behoben, der zu einem Problem beim Klonen aller Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ führte</span><span class="sxs-lookup"><span data-stu-id="7ad68-1701">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="7ad68-1702">1.5.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="7ad68-1702">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7ad68-1703">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ad68-1703">Az.Accounts</span></span>
* <span data-ttu-id="7ad68-1704">Der Befehl „Register-AzModule“ wurde hinzugefügt, um von AutoRest generierte Cmdlets zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1704">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="7ad68-1705">Beispiele für „Connect-AzAccount“ wurden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1705">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7ad68-1706">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7ad68-1706">Az.Automation</span></span>
* <span data-ttu-id="7ad68-1707">Problem behoben, das beim Abrufen bestimmter monatlicher Zeitpläne in verschiedenen Azure Automation-Cmdlets auftrat</span><span class="sxs-lookup"><span data-stu-id="7ad68-1707">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="7ad68-1708">„Get-AzAutomationDscNode“ wurde korrigiert, da nur die 20 obersten Knoten zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1708">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="7ad68-1709">Jetzt werden alle Knoten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1709">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7ad68-1710">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7ad68-1710">Az.Cdn</span></span>
* <span data-ttu-id="7ad68-1711">Neue Powershell-Cmdlets zum Aktivieren/Deaktivieren von HTTPS für benutzerdefinierte Domänen hinzugefügt und alte Cmdlets außer Betrieb genommen</span><span class="sxs-lookup"><span data-stu-id="7ad68-1711">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ad68-1712">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ad68-1712">Az.Compute</span></span>
* <span data-ttu-id="7ad68-1713">Unterstützung für Platzhalterzeichen zu Get-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1713">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7ad68-1714">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7ad68-1714">Az.DataFactory</span></span>
* <span data-ttu-id="7ad68-1715">Version des ADF .NET SDK auf 3.0.1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1715">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7ad68-1716">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7ad68-1716">Az.LogicApp</span></span>
* <span data-ttu-id="7ad68-1717">„ListWorkflows“ wurde korrigiert, da nur die erste Seite mit Ergebnissen abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1717">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ad68-1718">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ad68-1718">Az.Network</span></span>
* <span data-ttu-id="7ad68-1719">Unterstützung für Platzhalterzeichen zu Network-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1719">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7ad68-1720">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7ad68-1720">Az.RecoveryServices</span></span>
* <span data-ttu-id="7ad68-1721">SQL Server jetzt in Azure-VM-Support enthalten</span><span class="sxs-lookup"><span data-stu-id="7ad68-1721">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="7ad68-1722">SDK-Update</span><span class="sxs-lookup"><span data-stu-id="7ad68-1722">SDK Update</span></span>
* <span data-ttu-id="7ad68-1723">VMappContainer-Überprüfung in „Get-ProtectableItem“ entfernt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1723">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="7ad68-1724">„Name“ und „ServerName“ als Parameter für „Get-ProtectableItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1724">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ad68-1725">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ad68-1725">Az.Resources</span></span>
* <span data-ttu-id="7ad68-1726">Parameter `-TemplateObject` zu Bereitstellungs-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1726">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="7ad68-1727">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="7ad68-1727">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="7ad68-1728">Problem beim Piping des Ergebnisses von `Get-AzResource` an `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-1728">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="7ad68-1729">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="7ad68-1729">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="7ad68-1730">Problem mit JSON-Datentypänderung beim Ausführen von `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-1730">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="7ad68-1731">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="7ad68-1731">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ad68-1732">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ad68-1732">Az.Sql</span></span>
* <span data-ttu-id="7ad68-1733">„AuditingEndpointsCommunicator“ wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1733">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="7ad68-1734">Das Verhalten eines Grenzfalls beim Erstellen neuer Diagnoseeinstellungen wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1734">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7ad68-1735">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ad68-1735">Az.Storage</span></span>
* <span data-ttu-id="7ad68-1736">Unterstützung von „Kind BlockBlobStorage“ beim Erstellen eines Speicherkontos: New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ad68-1736">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="7ad68-1737">1.4.0 – Februar 2019</span><span class="sxs-lookup"><span data-stu-id="7ad68-1737">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="7ad68-1738">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7ad68-1738">Az.AnalysisServices</span></span>
* <span data-ttu-id="7ad68-1739">Cmdlet „AddAzureASAccount“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1739">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7ad68-1740">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7ad68-1740">Az.Automation</span></span>
* <span data-ttu-id="7ad68-1741">Hilfe für „Import-AzAutomationDscNodeConfiguration“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1741">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="7ad68-1742">Überprüfung des Konfigurationsnamens zu Cmdlet „Import-AzAutomationDscConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1742">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="7ad68-1743">Fehlerbehandlung für Cmdlet „Import-AzAutomationDscConfiguration“ verbessert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1743">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7ad68-1744">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7ad68-1744">Az.CognitiveServices</span></span>
* <span data-ttu-id="7ad68-1745">„CustomSubdomainName“ als neuer optionaler Parameter für Cmdlet „New-AzCognitiveServicesAccount“ hinzugefügt, das zum Angeben der Unterdomäne für die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1745">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ad68-1746">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ad68-1746">Az.Compute</span></span>
* <span data-ttu-id="7ad68-1747">Problem mit ID-Parametersätzen behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-1747">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="7ad68-1748">„Get-AzVMExtension“ aktualisiert, sodass alle installierten Erweiterungen aufgelistet werden, wenn der Name-Parameter nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="7ad68-1748">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="7ad68-1749">Parameter „Tag“ und „ResourceId“ zum Cmdlet „Update-AzImage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1749">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="7ad68-1750">„Get-AzVmssVM“ ohne Instanz-ID und mit „InstanceView“ können virtuelle VMSS-Computer mit Instanzansicht auflisten.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1750">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7ad68-1751">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7ad68-1751">Az.DataLakeStore</span></span>
* <span data-ttu-id="7ad68-1752">Cmdlets zum Auflisten und Wiederherstellen gelöschter ADL-Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1752">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7ad68-1753">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7ad68-1753">Az.EventHub</span></span>
* <span data-ttu-id="7ad68-1754">Neue boolesche Eigenschaft „SkipEmptyArchives“ zum Überspringen leerer Archive in Klasse „CaptureDescription“ von EventHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1754">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7ad68-1755">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7ad68-1755">Az.KeyVault</span></span>
* <span data-ttu-id="7ad68-1756">Kennzeichnung in „Set-AzKeyVaultSecret“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1756">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7ad68-1757">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7ad68-1757">Az.LogicApp</span></span>
* <span data-ttu-id="7ad68-1758">SKU „Basic“ für Integrationskonten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1758">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="7ad68-1759">XSLT 2.0, XSLT 3.0 und Liquid-Zuordnungstypen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1759">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="7ad68-1760">Neue Cmdlets für Integrationskonto-Assemblys</span><span class="sxs-lookup"><span data-stu-id="7ad68-1760">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="7ad68-1761">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7ad68-1761">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7ad68-1762">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7ad68-1762">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7ad68-1763">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7ad68-1763">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7ad68-1764">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7ad68-1764">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="7ad68-1765">Neue Cmdlets für Integrationskonto-Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="7ad68-1765">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="7ad68-1766">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ad68-1766">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7ad68-1767">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ad68-1767">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7ad68-1768">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ad68-1768">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7ad68-1769">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ad68-1769">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="7ad68-1770">Logik-App-SDK auf Version 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1770">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7ad68-1771">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7ad68-1771">Az.Monitor</span></span>
* <span data-ttu-id="7ad68-1772">Hilfe für „Get-AzMetric“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1772">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ad68-1773">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ad68-1773">Az.Network</span></span>
* <span data-ttu-id="7ad68-1774">Hilfebeispiel für „Add-AzApplicationGatewayCustomError“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1774">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7ad68-1775">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7ad68-1775">Az.OperationalInsights</span></span>
* <span data-ttu-id="7ad68-1776">Zusätzliche Unterstützung für Datenquelle von „New-ApplicationInsights“ und „Get-ApplicationInsights“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1776">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="7ad68-1777">Neue Art von „ApplicationInsights“ zum Abrufen von bestimmten und von allen ApplicationInsights-Datenquellen für einen Workspace hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1777">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="7ad68-1778">Cmdlet „New-AzOperationalInsightsApplicationInsightsDataSource“ zum Erstellen einer Datenquelle anhand des angegebenen Ressourcenparameters für „Application-Insights“ hinzugefügt: „subscriptionId“, „resourceGroupName“ und „name“.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1778">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ad68-1779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ad68-1779">Az.Resources</span></span>
* <span data-ttu-id="7ad68-1780">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="7ad68-1780">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="7ad68-1781">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="7ad68-1781">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="7ad68-1782">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="7ad68-1782">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="7ad68-1783">Fehler korrigiert, der die wiederholte Erstellung von „KeyCredentials“ verhindert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1783">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ad68-1784">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ad68-1784">Az.Sql</span></span>
* <span data-ttu-id="7ad68-1785">Unterstützung für SQL DB Hyperscale-Tarif hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1785">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="7ad68-1786">Fehler korrigiert, aufgrund dessen die Wiederherstellung wegen der Festlegung unnötiger Eigenschaften in der Wiederherstellungsanforderung fehlschlagen konnte</span><span class="sxs-lookup"><span data-stu-id="7ad68-1786">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7ad68-1787">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ad68-1787">Az.Websites</span></span>
* <span data-ttu-id="7ad68-1788">Beispiel in „Get-AzWebAppSlotMetrics“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1788">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="7ad68-1789">1.3.0: Februar 2019</span><span class="sxs-lookup"><span data-stu-id="7ad68-1789">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7ad68-1790">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ad68-1790">Az.Accounts</span></span>
* <span data-ttu-id="7ad68-1791">Update auf die aktuelle Version von ClientRuntime durchgeführt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1791">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7ad68-1792">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7ad68-1792">Az.AnalysisServices</span></span>
<span data-ttu-id="7ad68-1793">Allgemeine Verfügbarkeit für Az.AnalysisServices-Modul</span><span class="sxs-lookup"><span data-stu-id="7ad68-1793">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ad68-1794">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ad68-1794">Az.Compute</span></span>
* <span data-ttu-id="7ad68-1795">AEM-Erweiterung: Unterstützung für UltraSSD und P60-, P70- und P80-Datenträger hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1795">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="7ad68-1796">Hilfebeschreibung für „Set-AzVMBootDiagnostics“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1796">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="7ad68-1797">Hilfebeschreibung und Beispiel für „Update-AzImage“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1797">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7ad68-1798">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7ad68-1798">Az.RecoveryServices</span></span>
<span data-ttu-id="7ad68-1799">Allgemeine Verfügbarkeit für Az.RecoveryServices-Modul.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1799">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ad68-1800">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ad68-1800">Az.Resources</span></span>
* <span data-ttu-id="7ad68-1801">Kennzeichnung für Ressourcengruppen korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1801">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="7ad68-1802">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="7ad68-1802">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="7ad68-1803">Problem behoben, bei dem „-ErrorAction“ von `Get-AzureRmRoleAssignment` nicht berücksichtigt wird</span><span class="sxs-lookup"><span data-stu-id="7ad68-1803">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="7ad68-1804">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="7ad68-1804">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ad68-1805">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ad68-1805">Az.Sql</span></span>
* <span data-ttu-id="7ad68-1806">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1806">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="7ad68-1807">Problem behoben, bei dem eine fehlende Anmeldung am Azure-Konto bei der Ausführung von SQL-Cmdlets zu einer nullref-Ausnahme führt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1807">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="7ad68-1808">nullref-Ausnahme in Get-AzSqlCapability korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1808">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="7ad68-1809">1.2.1: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="7ad68-1809">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7ad68-1810">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ad68-1810">Az.Accounts</span></span>
* <span data-ttu-id="7ad68-1811">Release mit richtiger Version der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="7ad68-1811">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7ad68-1812">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7ad68-1812">Az.AnalysisServices</span></span>
* <span data-ttu-id="7ad68-1813">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="7ad68-1813">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7ad68-1814">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7ad68-1814">Az.RecoveryServices</span></span>
* <span data-ttu-id="7ad68-1815">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="7ad68-1815">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="7ad68-1816">1.2.0: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="7ad68-1816">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7ad68-1817">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ad68-1817">Az.Accounts</span></span>
* <span data-ttu-id="7ad68-1818">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1818">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7ad68-1819">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1819">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7ad68-1820">Warnmeldung in PS Core für „Uninstall-AzureRm“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1820">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="7ad68-1821">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="7ad68-1821">Az.Aks</span></span>
* <span data-ttu-id="7ad68-1822">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1822">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7ad68-1823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7ad68-1823">Az.Automation</span></span>
* <span data-ttu-id="7ad68-1824">Unterstützung für Python 2-Runbooks hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1824">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="7ad68-1825">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1825">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7ad68-1826">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7ad68-1826">Az.Cdn</span></span>
* <span data-ttu-id="7ad68-1827">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1827">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ad68-1828">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ad68-1828">Az.Compute</span></span>
* <span data-ttu-id="7ad68-1829">Cmdlet „Invoke-AzVMReimage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1829">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="7ad68-1830">Parameter „TempDisk“ zu „Set-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1830">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="7ad68-1831">Warnmeldung von „New-AzVM“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1831">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="7ad68-1832">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7ad68-1832">Az.ContainerRegistry</span></span>
* <span data-ttu-id="7ad68-1833">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1833">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7ad68-1834">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7ad68-1834">Az.DataFactory</span></span>
* <span data-ttu-id="7ad68-1835">Version des ADF .NET SDK auf 3.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1835">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7ad68-1836">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7ad68-1836">Az.DataLakeStore</span></span>
* <span data-ttu-id="7ad68-1837">Problem mit ADLS-Endpunkt bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-1837">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="7ad68-1838">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="7ad68-1838">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="7ad68-1839">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1839">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7ad68-1840">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7ad68-1840">Az.IotHub</span></span>
* <span data-ttu-id="7ad68-1841">Codierungsformat zu Cmdlet „Add-IotHubRoutingEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1841">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7ad68-1842">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7ad68-1842">Az.KeyVault</span></span>
* <span data-ttu-id="7ad68-1843">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1843">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ad68-1844">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ad68-1844">Az.Network</span></span>
* <span data-ttu-id="7ad68-1845">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1845">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ad68-1846">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ad68-1846">Az.Resources</span></span>
* <span data-ttu-id="7ad68-1847">Fehlerhafte Beispiele in Referenzdokumentation zu „New-AzADAppCredential“ und „New-AzADSpCredential“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1847">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="7ad68-1848">Problem behoben, bei dem der Pfad für den Parameter „-TemplateFile“ nicht aufgelöst wurde, bevor Cmdlets für die Bereitstellung von Ressourcengruppen ausgeführt wurden</span><span class="sxs-lookup"><span data-stu-id="7ad68-1848">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="7ad68-1849">Az.Resources: Richtige Dokumentation für Standardwert von „New-AzureRmPolicyDefinition -Mode“ bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1849">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="7ad68-1850">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="7ad68-1850">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="7ad68-1851">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="7ad68-1851">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="7ad68-1852">Formatierungsproblem für Objekt „PSResourceGroupDeployment“ behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-1852">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="7ad68-1853">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="7ad68-1853">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7ad68-1854">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7ad68-1854">Az.ServiceFabric</span></span>
* <span data-ttu-id="7ad68-1855">Rollback beim Hinzufügen eines Zertifikats zum VMSS-Modell, Auslösung einer Ausnahme. Fehlerbehebung: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="7ad68-1855">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="7ad68-1856">Einige Fehlermeldungen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1856">Fix some error messages.</span></span>
* <span data-ttu-id="7ad68-1857">Fehler bei Clustererstellung mit ARM-Standardvorlage für „New-AzServiceFabriCluster“ behoben, bei dem die Migration zu Az nicht funktioniert hat.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1857">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="7ad68-1858">Fehler behoben beim Hinzufügen eines Cluster-/Anwendungszertifikats ausschließlich zu VM Scale Sets, die zum Cluster gehören, indem die Cluster-ID in der Erweiterung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1858">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7ad68-1859">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7ad68-1859">Az.SignalR</span></span>
* <span data-ttu-id="7ad68-1860">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1860">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ad68-1861">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ad68-1861">Az.Sql</span></span>
* <span data-ttu-id="7ad68-1862">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1862">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7ad68-1863">Parameterbeschreibung für den Parameter „LicenseType“ mit möglichen Werten aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1863">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="7ad68-1864">Fehler behoben, bei dem die Aktualisierung der Identität der verwalteten Instanz nicht funktioniert hat, wenn es sich um die einzige aktualisierte Eigenschaft gehandelt hat</span><span class="sxs-lookup"><span data-stu-id="7ad68-1864">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="7ad68-1865">Unterstützung für die benutzerdefinierte Sortierung auf verwalteter Instanz</span><span class="sxs-lookup"><span data-stu-id="7ad68-1865">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7ad68-1866">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ad68-1866">Az.Storage</span></span>
* <span data-ttu-id="7ad68-1867">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1867">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7ad68-1868">Ausführliche Fehlermeldung beim Abrufen/Festlegen der klassischen Protokollierung bzw. Metriken für Storage Premium-Konto, da für das Storage Premium-Konto die klassische Protokollierung bzw. Metriken nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1868">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="7ad68-1869">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="7ad68-1869">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="7ad68-1870">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="7ad68-1870">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="7ad68-1871">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="7ad68-1871">Az.TrafficManager</span></span>
* <span data-ttu-id="7ad68-1872">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1872">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7ad68-1873">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ad68-1873">Az.Websites</span></span>
* <span data-ttu-id="7ad68-1874">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1874">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7ad68-1875">„New-AzWebAppSSLBinding“ korrigiert, damit das Zertifikat in die richtige Ressourcengruppe bzw. an den richtigen Speicherort hochgeladen wird, wenn die App in einer ASE gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1875">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="7ad68-1876">„New-AzWebAppSSLBinding“ korrigiert, damit die Tags beim Binden eines SSL-Zertifikats an eine App nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1876">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="7ad68-1877">1.1.0 – Januar 2019</span><span class="sxs-lookup"><span data-stu-id="7ad68-1877">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7ad68-1878">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ad68-1878">Az.Accounts</span></span>
* <span data-ttu-id="7ad68-1879">Bereich „Local“ zu „Enable-AzureRmAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1879">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ad68-1880">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ad68-1880">Az.Compute</span></span>
* <span data-ttu-id="7ad68-1881">Name ist jetzt optional im ID-Parametersatz für „Restart/Start/Stop/Remove/Set-AzVM“ und „Save-AzVMImage“</span><span class="sxs-lookup"><span data-stu-id="7ad68-1881">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="7ad68-1882">Beschreibung der ID in Hilfedateien aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1882">Updated the description of ID in help files</span></span>
* <span data-ttu-id="7ad68-1883">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-1883">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7ad68-1884">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7ad68-1884">Az.DataLakeStore</span></span>
* <span data-ttu-id="7ad68-1885">Aktualisierung der SDK-Version der Datenebene auf 1.1.14 für SDK-Fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1885">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="7ad68-1886">Behandlung von negativen acesstime- and modificationtime-Werten für „getfilestatus“ und „liststatus“ korrigiert, asynchrones Abbruchtoken korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1886">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7ad68-1887">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7ad68-1887">Az.EventGrid</span></span>
* <span data-ttu-id="7ad68-1888">Zur Verwendung der API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1888">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="7ad68-1889">Aktualisierung der folgenden Cmdlets zur Unterstützung des neuen Szenarios in der API-Version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="7ad68-1889">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="7ad68-1890">New-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="7ad68-1890">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="7ad68-1891">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="7ad68-1891">Event Time-To-Live,</span></span>
        - <span data-ttu-id="7ad68-1892">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="7ad68-1892">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="7ad68-1893">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="7ad68-1893">Dead letter endpoint.</span></span>
    - <span data-ttu-id="7ad68-1894">Update-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="7ad68-1894">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="7ad68-1895">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="7ad68-1895">Event Time-To-Live,</span></span>
        - <span data-ttu-id="7ad68-1896">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="7ad68-1896">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="7ad68-1897">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="7ad68-1897">Dead letter endpoint.</span></span>
* <span data-ttu-id="7ad68-1898">Neue Enumerationswerte („storageQueue“ und „hybridConnection“) für die EndpointType-Option in den Cmdlets „New-AzureRmEventGridSubscription“ und „Update-AzureRmEventGridSubscription“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1898">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="7ad68-1899">Anzeige einer Warnmeldung, wenn das Erstellen oder Aktualisieren des Ereignisabonnements voraussichtlich eine manuelle Aktion des Benutzers zur Folge hat</span><span class="sxs-lookup"><span data-stu-id="7ad68-1899">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7ad68-1900">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7ad68-1900">Az.IotHub</span></span>
* <span data-ttu-id="7ad68-1901">Auf die aktuelle Version des Iot Hub SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1901">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7ad68-1902">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7ad68-1902">Az.LogicApp</span></span>
* <span data-ttu-id="7ad68-1903">„Get-AzLogicApp“ listet alle Apps ohne angegebenen Namen auf</span><span class="sxs-lookup"><span data-stu-id="7ad68-1903">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ad68-1904">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ad68-1904">Az.Resources</span></span>
* <span data-ttu-id="7ad68-1905">Problem mit dem Parametersatz bei Angabe der Parameter „-ODataQuery“ und „-ResourceId“ für „Get-AzResource“ behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-1905">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="7ad68-1906">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="7ad68-1906">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="7ad68-1907">Behandlung des Parameters „-Custom“ in „New/Set-AzPolicyDefinition“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1907">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="7ad68-1908">Tippfehler in der Dokumentation für „New-AzDeployment“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1908">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="7ad68-1909">Parameter „-MailNickname“ als obligatorisch festgelegt für „New-AzADUser“</span><span class="sxs-lookup"><span data-stu-id="7ad68-1909">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="7ad68-1910">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="7ad68-1910">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7ad68-1911">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7ad68-1911">Az.SignalR</span></span>
* <span data-ttu-id="7ad68-1912">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-1912">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ad68-1913">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ad68-1913">Az.Sql</span></span>
* <span data-ttu-id="7ad68-1914">Abhängigkeit des Speicherverwaltungsclients zur allgemeinen SDK-Implementierung konvertiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1914">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7ad68-1915">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ad68-1915">Az.Storage</span></span>
* <span data-ttu-id="7ad68-1916">Festlegung des „StorageAccountName“ des Speicherkontexts als tatsächlichen Namen des Speicherkontos, wenn dieser mit „SAS-Token“, „OAuth“ oder „Anonym“ erstellt wird</span><span class="sxs-lookup"><span data-stu-id="7ad68-1916">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="7ad68-1917">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7ad68-1917">New-AzStorageContext</span></span>
* <span data-ttu-id="7ad68-1918">Erstellen von SAS-Token des Blob-Momentaufnahmeobjekts mit dem Parameter „-FullUri“, Festlegung des zurückgegebenen URI als Momentaufnahme-URI</span><span class="sxs-lookup"><span data-stu-id="7ad68-1918">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="7ad68-1919">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="7ad68-1919">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7ad68-1920">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ad68-1920">Az.Websites</span></span>
* <span data-ttu-id="7ad68-1921">Fehler bei der Datumsanalyse in „Get-AzDeletedWebApp“ behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-1921">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="7ad68-1922">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-1922">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="7ad68-1923">1.0.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="7ad68-1923">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="7ad68-1924">Allgemein</span><span class="sxs-lookup"><span data-stu-id="7ad68-1924">General</span></span>

- <span data-ttu-id="7ad68-1925">Allgemeine Verfügbarkeit des Az-Moduls</span><span class="sxs-lookup"><span data-stu-id="7ad68-1925">General Availability of Az Module</span></span>
- <span data-ttu-id="7ad68-1926">Onlinehilfe für jedes Modul</span><span class="sxs-lookup"><span data-stu-id="7ad68-1926">Online help for each module</span></span>
- <span data-ttu-id="7ad68-1927">Ausführlichere Informationen und eine Roadmap finden Sie auf der [Seite mit der Ankündigung zu Az](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="7ad68-1927">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="7ad68-1928">Informationen zur Migration aus AzureRM finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="7ad68-1928">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="7ad68-1929">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7ad68-1929">Az.Accounts</span></span>
- <span data-ttu-id="7ad68-1930">Geändert von Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7ad68-1930">Changed from Az.Profile</span></span>
- <span data-ttu-id="7ad68-1931">Feste Tabellenformate für Profil- und Kontexttypen</span><span class="sxs-lookup"><span data-stu-id="7ad68-1931">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="7ad68-1932">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7ad68-1932">Az.ApiManagement</span></span>
- <span data-ttu-id="7ad68-1933">Korrekturen für #7002</span><span class="sxs-lookup"><span data-stu-id="7ad68-1933">Fixes for #7002</span></span>
- <span data-ttu-id="7ad68-1934">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="7ad68-1934">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="7ad68-1935">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7ad68-1935">Az.Batch</span></span>
- <span data-ttu-id="7ad68-1936">Möglichkeit zum Anzeigen der ausgeführten Version des Azure Batch-Knoten-Agents auf den VMs eines Pools mit der neuen `NodeAgentInformation`-Eigenschaft für `PSComputeNode` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1936">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="7ad68-1937">Der `Caching`-Standardwert für `PSDataDisk` lautet jetzt nicht mehr `None`, sondern `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1937">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="7ad68-1938">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="7ad68-1938">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="7ad68-1939">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="7ad68-1939">Az.Billing</span></span>
- <span data-ttu-id="7ad68-1940">Kombination von Billing-, Consumption- und UsageAggregates-Cmdlets. Ausführliche Informationen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="7ad68-1940">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="7ad68-1941">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="7ad68-1941">Az.CognitivServices</span></span>
- <span data-ttu-id="7ad68-1942">Vervollständigungen für SkuName und Typem für den Vorgang New-AzureRmCognitiveServicesAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1942">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="7ad68-1943">GetSkusWithAccountParamSetName-Parametersatz aus Get-AzCognitiveServicesAccountSkus entfernt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1943">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="7ad68-1944">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7ad68-1944">Az.ContainerInstance</span></span>
- <span data-ttu-id="7ad68-1945">ManagedIdentity-Unterstützung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1945">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="7ad68-1946">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="7ad68-1946">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="7ad68-1947">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="7ad68-1947">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="7ad68-1948">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7ad68-1948">Az.DataLakeStore</span></span>
- <span data-ttu-id="7ad68-1949">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="7ad68-1949">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="7ad68-1950">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7ad68-1950">Az.Monitor</span></span>
- <span data-ttu-id="7ad68-1951">Az.Insights in Az.Monitor umbenannt und weitere weniger wichtige grundlegende Änderungen durchgeführt. Informationen hierzu finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="7ad68-1951">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="7ad68-1952">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7ad68-1952">Az.KeyVault</span></span>
- <span data-ttu-id="7ad68-1953">Veraltete PurgeDisabled-Eigenschaft aus Ausgabetypen entfernt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1953">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="7ad68-1954">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7ad68-1954">Az.MachineLearning</span></span>
- <span data-ttu-id="7ad68-1955">Cmdlets des Az.MachineLearningCompute-Moduls eingebunden</span><span class="sxs-lookup"><span data-stu-id="7ad68-1955">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="7ad68-1956">Az.Media</span><span class="sxs-lookup"><span data-stu-id="7ad68-1956">Az.Media</span></span>
- <span data-ttu-id="7ad68-1957">Veralteten -Tags-Alias aus New-AzMediaService entfernt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1957">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="7ad68-1958">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ad68-1958">Az.Network</span></span>
<span data-ttu-id="7ad68-1959">Unterstützung für das Konfigurieren von RewriteRuleSets im Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1959">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="7ad68-1960">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7ad68-1960">New cmdlets added:</span></span>
        - <span data-ttu-id="7ad68-1961">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7ad68-1961">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7ad68-1962">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7ad68-1962">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7ad68-1963">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7ad68-1963">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7ad68-1964">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7ad68-1964">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7ad68-1965">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7ad68-1965">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7ad68-1966">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="7ad68-1966">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="7ad68-1967">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="7ad68-1967">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="7ad68-1968">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ad68-1968">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="7ad68-1969">Cmdlets mit optionalem Parameter -RewriteRuleSet aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1969">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="7ad68-1970">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ad68-1970">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="7ad68-1971">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7ad68-1971">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="7ad68-1972">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7ad68-1972">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="7ad68-1973">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7ad68-1973">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="7ad68-1974">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7ad68-1974">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="7ad68-1975">New-AzureRmApplicationGatewayUrlPathMapConfig: KeyVault-Unterstützung mithilfe von Identität zum Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-1975">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="7ad68-1976">Cmdlets mit optionalem Parameter aktualisiert: -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7ad68-1976">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="7ad68-1977">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7ad68-1977">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="7ad68-1978">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7ad68-1978">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="7ad68-1979">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7ad68-1979">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="7ad68-1980">Cmdlet New-AzApplicationGateway mit optionalem Parameter -UserAssignedIdentity aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1980">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="7ad68-1981">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="7ad68-1981">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="7ad68-1982">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7ad68-1982">Az.OperationalInsights</span></span>
- <span data-ttu-id="7ad68-1983">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="7ad68-1983">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="7ad68-1984">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7ad68-1984">Az.Profile</span></span>
- <span data-ttu-id="7ad68-1985">Modulnamen in Az.Accounts geändert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1985">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="7ad68-1986">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7ad68-1986">Az.RecoveryServices</span></span>
- <span data-ttu-id="7ad68-1987">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="7ad68-1987">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="7ad68-1988">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ad68-1988">Az.Resources</span></span>
- <span data-ttu-id="7ad68-1989">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="7ad68-1989">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="7ad68-1990">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7ad68-1990">Az.ServiceFabric</span></span>
- <span data-ttu-id="7ad68-1991">Unterstützung für das Angeben des Zertifikats anhand des allgemeinen Namens und Fingerabdrucks</span><span class="sxs-lookup"><span data-stu-id="7ad68-1991">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="7ad68-1992">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="7ad68-1992">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="7ad68-1993">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="7ad68-1993">Az.SIgnalR</span></span>
- <span data-ttu-id="7ad68-1994">Allgemeine Verfügbarkeit für PowerShell-Cmdlets für SIgnalR</span><span class="sxs-lookup"><span data-stu-id="7ad68-1994">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="7ad68-1995">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ad68-1995">Az.Sql</span></span>
- <span data-ttu-id="7ad68-1996">Neue Erkennungstypen Data_Exfiltration und Unsafe_Action zu Cmdlets für Bedrohungserkennung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-1996">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="7ad68-1997">Dokumentationsbeispiele für Cmdlets für SQL-Überwachung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-1997">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="7ad68-1998">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="7ad68-1998">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="7ad68-1999">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ad68-1999">Az.Storage</span></span>
- <span data-ttu-id="7ad68-2000">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="7ad68-2000">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="7ad68-2001">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ad68-2001">Az.Websites</span></span>
- <span data-ttu-id="7ad68-2002">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="7ad68-2002">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="7ad68-2003">0.7.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="7ad68-2003">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="7ad68-2004">Allgemein</span><span class="sxs-lookup"><span data-stu-id="7ad68-2004">General</span></span>

* <span data-ttu-id="7ad68-2005">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="7ad68-2005">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="7ad68-2006">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ad68-2006">Az.Compute</span></span>

* <span data-ttu-id="7ad68-2007">Unterstützung für UltraSSD und Katalogimages in einfachen Parametersätzen für `New-AzVm(ss)`-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-2007">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="7ad68-2008">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7ad68-2008">Az.DataLakeStore</span></span>

* <span data-ttu-id="7ad68-2009">Nachgestellten Schrägstrich für die Domäne des ADLS-Kontos korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-2009">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="7ad68-2010">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7ad68-2010">Az.FrontDoor</span></span>

* <span data-ttu-id="7ad68-2011">Einige fehlerhafte Links behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-2011">Fixed some broken links</span></span>
    - <span data-ttu-id="7ad68-2012">In den Artikeln zu New-AzureRmFrontDoor und Set-AzureRmFrontDoor den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorHealthProbeSettingObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="7ad68-2012">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="7ad68-2013">Im Artikel zu New-AzureRmFrontDoorManagedRuleObject den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorRuleGroupOverrideObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="7ad68-2013">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="7ad68-2014">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7ad68-2014">Az.RecoveryServices</span></span>

* <span data-ttu-id="7ad68-2015">Clientseitige Validierungen für Wiederherstellungsvorgänge von Azure-Dateifreigaben hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-2015">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="7ad68-2016">storageAccountName und storageAccountResourceGroupName für AFS-Wiederherstellung optional gemacht.</span><span class="sxs-lookup"><span data-stu-id="7ad68-2016">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="7ad68-2017">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ad68-2017">Az.Resources</span></span>

* <span data-ttu-id="7ad68-2018">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="7ad68-2018">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="7ad68-2019">Get-AzureRmRoleAssignment für die Verwendung des Abonnementbereichs aktualisiert, wenn dieser beim Anfordern von klassischen Administratoren angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7ad68-2019">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="7ad68-2020">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ad68-2020">Az.Sql</span></span>

* <span data-ttu-id="7ad68-2021">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="7ad68-2021">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="7ad68-2022">Problem mit der Verwendung von Get-AzureRmSqlDatabaseVulnerabilityAssessment mit .NET Core behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-2022">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="7ad68-2023">Dokumentation mit Hilfemeldungen zu Cmdlets für die SQL-Überwachung geändert.</span><span class="sxs-lookup"><span data-stu-id="7ad68-2023">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="7ad68-2024">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7ad68-2024">Az.Storage</span></span>

* <span data-ttu-id="7ad68-2025">-EnableHierarchicalNamespace zu New-AzureRmStorageAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-2025">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="7ad68-2026">Problem behoben, bei dem für das Copy File-Cmdlet am Ziel kein Quellkontext wiederverwendet werden kann, wenn -DestContext nicht eingegeben wird</span><span class="sxs-lookup"><span data-stu-id="7ad68-2026">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="7ad68-2027">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="7ad68-2027">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="7ad68-2028">Unterstützung der Konfiguration von statischen Websites</span><span class="sxs-lookup"><span data-stu-id="7ad68-2028">Support Static Website configuration</span></span>
    - <span data-ttu-id="7ad68-2029">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7ad68-2029">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="7ad68-2030">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7ad68-2030">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="7ad68-2031">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ad68-2031">Az.Websites</span></span>

* <span data-ttu-id="7ad68-2032">Set-AzureRmWebApp und Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7ad68-2032">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="7ad68-2033">Neuen Parameter (-AzureStoragePath) zum Angeben von Azure Storage-Pfaden hinzugefügt, die in Windows- und Linux-Container-Apps bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7ad68-2033">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="7ad68-2034">Verwenden Sie die Ausgabe des neuen Cmdlets New-AzureRmWebAppAzureStoragePath als Parameter zum Festlegen der Azure Storage-Pfade.</span><span class="sxs-lookup"><span data-stu-id="7ad68-2034">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="7ad68-2035">0.6.1 – November 2018</span><span class="sxs-lookup"><span data-stu-id="7ad68-2035">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="7ad68-2036">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7ad68-2036">Az.ApiManagement</span></span>
* <span data-ttu-id="7ad68-2037">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-2037">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="7ad68-2038">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7ad68-2038">Az.Automation</span></span>
* <span data-ttu-id="7ad68-2039">Swagger-basierte Azure Automation-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7ad68-2039">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="7ad68-2040">Cmdlets zur Updateverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-2040">Added Update Management cmdlets</span></span>
* <span data-ttu-id="7ad68-2041">Cmdlets zur Quellcodeverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-2041">Added Source Control cmdlets</span></span>
* <span data-ttu-id="7ad68-2042">Cmdlet „Remove-AzureRmAutomationHybridWorkerGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-2042">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="7ad68-2043">DSC-Befehl für die Knotenregistrierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-2043">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="7ad68-2044">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ad68-2044">Az.Compute</span></span>
* <span data-ttu-id="7ad68-2045">Identitätsproblem für SystemAssigned-Identität korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-2045">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="7ad68-2046">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-2046">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="7ad68-2047">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7ad68-2047">Az.ContainerInstance</span></span>
* <span data-ttu-id="7ad68-2048">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-2048">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="7ad68-2049">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="7ad68-2049">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="7ad68-2050">Beschreibung der Beispiele für Marketplace-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-2050">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="7ad68-2051">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ad68-2051">Az.Network</span></span>
* <span data-ttu-id="7ad68-2052">Folgende Cmdlets hinzugefügt: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="7ad68-2052">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="7ad68-2053">ICMP wieder unterstützten AzureFirewall-Netzwerkprotokollen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-2053">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="7ad68-2054">Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert und Überprüfung für Ziel-ID, Adresse und Port hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-2054">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="7ad68-2055">Probleme mit Arbeitsspeicherauslastung in der VirtualNetwork-Zuordnung behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-2055">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="7ad68-2056">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="7ad68-2056">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="7ad68-2057">Problem beim Ändern der Richtlinie für eine geschützte Dateifreigabe behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-2057">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="7ad68-2058">Richtlinienzeitzone in Großschreibung geändert</span><span class="sxs-lookup"><span data-stu-id="7ad68-2058">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="7ad68-2059">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="7ad68-2059">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="7ad68-2060">Korrigiertes Beispiel in „New-AzureRmRecoveryServicesAsrProtectableItem“</span><span class="sxs-lookup"><span data-stu-id="7ad68-2060">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="7ad68-2061">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-2061">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="7ad68-2062">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="7ad68-2062">Az.Relay</span></span>
* <span data-ttu-id="7ad68-2063">Optionaler Parameter „-KeyValue“ zu Cmdlet „New-AzureRmRelayKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht</span><span class="sxs-lookup"><span data-stu-id="7ad68-2063">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="7ad68-2064">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ad68-2064">Az.Resources</span></span>
* <span data-ttu-id="7ad68-2065">Hilfedokumentation für ressourcenidentitätsbezogene Parameter in `New-AzureRmPolicyAssignment` und `Set-AzureRmPolicyAssignment` aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-2065">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="7ad68-2066">Beispiel für „New-AzureRmPolicyDefinition“ hinzugefügt, das „-Metadata“ nutzt</span><span class="sxs-lookup"><span data-stu-id="7ad68-2066">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="7ad68-2067">Korrektur, um Beibehaltung von Groß-/Kleinschreibung in Tagschlüsseln in „NetStandard“ zu ermöglichen: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="7ad68-2067">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="7ad68-2068">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7ad68-2068">Az.ServiceFabric</span></span>
* <span data-ttu-id="7ad68-2069">Benachrichtigung über veraltete Elemente für anstehende wichtige Änderungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-2069">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="7ad68-2070">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ad68-2070">Az.Sql</span></span>
* <span data-ttu-id="7ad68-2071">Neue Cmdlets für CRUD-Vorgänge in verwalteten Azure SQL-Datenbank-Instanzen und verwalteten Azure SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-2071">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="7ad68-2072">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7ad68-2072">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7ad68-2073">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7ad68-2073">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7ad68-2074">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7ad68-2074">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7ad68-2075">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7ad68-2075">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7ad68-2076">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7ad68-2076">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7ad68-2077">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7ad68-2077">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7ad68-2078">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7ad68-2078">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7ad68-2079">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7ad68-2079">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="7ad68-2080">Erweiterte Verwaltung von Überwachungsrichtlinien auf einem Server oder in einer Datenbank aktiviert</span><span class="sxs-lookup"><span data-stu-id="7ad68-2080">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="7ad68-2081">Neuer Parameter (PredicateExpression) hinzugefügt, um die Filterung von Überwachungsprotokollen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="7ad68-2081">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="7ad68-2082">Cmdlets wurden angepasst, sodass sie SQL-Clients anstelle von Legacyclients verwenden.</span><span class="sxs-lookup"><span data-stu-id="7ad68-2082">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="7ad68-2083">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="7ad68-2083">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="7ad68-2084">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="7ad68-2084">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="7ad68-2085">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="7ad68-2085">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="7ad68-2086">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="7ad68-2086">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="7ad68-2087">Problem bei Verwendung von „Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings“ mit festgelegtem Parameter für den Speicherkontonamen behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-2087">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="7ad68-2088">0.5.0 – November 2018</span><span class="sxs-lookup"><span data-stu-id="7ad68-2088">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="7ad68-2089">Allgemein</span><span class="sxs-lookup"><span data-stu-id="7ad68-2089">General</span></span>
* <span data-ttu-id="7ad68-2090">Ressourcenvervollständigungen für viele Kern-Cmdlets hinzugefügt (diese ermöglichen das Durchlaufen von vorhandenen Ressourcennamen per TAB-TASTE, wenn Cmdlets interaktiv aufgerufen werden)</span><span class="sxs-lookup"><span data-stu-id="7ad68-2090">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="7ad68-2091">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7ad68-2091">Az.Profile</span></span>
* <span data-ttu-id="7ad68-2092">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="7ad68-2092">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="7ad68-2093">Parameter „TenantId“ im Cmdlet „Connect-AzAccount“ in „Tenant“ umbenannt und Alias für „TenantId“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-2093">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="7ad68-2094">Beschreibung von „TenantId“ für „Connect-AzAccount“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-2094">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="7ad68-2095">Fehlermeldung für fehlgeschlagene Anmeldung bei Angabe der Mandantendomäne korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-2095">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="7ad68-2096">Problem in Bezug auf Kontextnamenskonflikt für Konten ohne Abonnements im Mandanten behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-2096">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="7ad68-2097">Problem mit DataLake-Endpunkten bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-2097">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="7ad68-2098">Problem behoben, das zur Auslösung von „Disconnect-AzAccount“ führte, wenn keine Verbindung bestand</span><span class="sxs-lookup"><span data-stu-id="7ad68-2098">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="7ad68-2099">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7ad68-2099">Az.CognitiveServices</span></span>
* <span data-ttu-id="7ad68-2100">Vorgang „Get-AzCognitiveServicesAccountSkus“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-2100">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ad68-2101">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ad68-2101">Az.Compute</span></span>
* <span data-ttu-id="7ad68-2102">Cmdlets Add-AzVmssVMDataDisk und Remove-AzVmssVMDataDisk hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-2102">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="7ad68-2103">„Get-AzVMImage“ zeigt „AutomaticOSUpgradeProperties“ an</span><span class="sxs-lookup"><span data-stu-id="7ad68-2103">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="7ad68-2104">Problem behoben, aufgrund dessen die Optionswerte „SetAzVMChefExtension -BootstrapOptions“ und „-JsonAttribute“ nicht im JSON-Format festgelegt wurden</span><span class="sxs-lookup"><span data-stu-id="7ad68-2104">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7ad68-2105">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7ad68-2105">Az.DataLakeStore</span></span>
* <span data-ttu-id="7ad68-2106">Aktualisierung des DataLake-Pakets auf 1.1.10</span><span class="sxs-lookup"><span data-stu-id="7ad68-2106">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="7ad68-2107">Standardmäßige Parallelität zu Multithreadvorgängen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-2107">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="7ad68-2108">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="7ad68-2108">Az.Insights</span></span>
* <span data-ttu-id="7ad68-2109">Problem Nr. 7267 behoben (Bereich für automatische Skalierung)</span><span class="sxs-lookup"><span data-stu-id="7ad68-2109">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="7ad68-2110">Probleme beim Erstellen einer neuen Regel für die automatische Skalierung, aufgrund derer die aufgelisteten Parameter nicht richtig festgelegt wurden (Es wurde stets der Standardwert festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="7ad68-2110">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="7ad68-2111">Problem Nr. 7513 behoben [Insights] „Set-AzDiagnosticSetting“ erfordert die explizite Angabe von Kategorien während der Erstellung der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="7ad68-2111">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="7ad68-2112">Nun erfordert das Cmdlet nicht die explizite Angabe der Kategorien, die während der Erstellung aktiviert werden sollen. Das bedeutet, es funktioniert wie dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="7ad68-2112">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ad68-2113">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ad68-2113">Az.Network</span></span>
* <span data-ttu-id="7ad68-2114">„PeeringType“ wurde geändert und ist nun ein erforderlicher Parameter für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7ad68-2114">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="7ad68-2115">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="7ad68-2115">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="7ad68-2116">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="7ad68-2116">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="7ad68-2117">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7ad68-2117">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="7ad68-2118">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="7ad68-2118">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="7ad68-2119">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="7ad68-2119">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="7ad68-2120">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7ad68-2120">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7ad68-2121">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7ad68-2121">Az.PolicyInsights</span></span>
* <span data-ttu-id="7ad68-2122">Cmdlets für Richtlinienwartung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-2122">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ad68-2123">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ad68-2123">Az.Resources</span></span>
* <span data-ttu-id="7ad68-2124">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="7ad68-2124">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="7ad68-2125">Zulassen der Auflistung von Ressourcen mithilfe des Parameters „-ResourceId“ für „Get-AzResource“</span><span class="sxs-lookup"><span data-stu-id="7ad68-2125">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7ad68-2126">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7ad68-2126">Az.ServiceBus</span></span>
* <span data-ttu-id="7ad68-2127">Schreibgeschützte Eigenschaft „MigrationState“ zu „PSServiceBusMigrationConfigurationAttributes“ hinzugefügt, was das Ermitteln des Migrationsstatus ermöglicht</span><span class="sxs-lookup"><span data-stu-id="7ad68-2127">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7ad68-2128">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7ad68-2128">Az.ServiceFabric</span></span>
* <span data-ttu-id="7ad68-2129">Hinzufügen des Zertifikats zu Linux VMSS korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-2129">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="7ad68-2130">„Add-AzServiceFabricClusterCertificate“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="7ad68-2130">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="7ad68-2131">Verwenden des richtigen Fingerabdrucks aus dem neuen Zertifikat (Azure/service-fabric-issues#932)</span><span class="sxs-lookup"><span data-stu-id="7ad68-2131">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="7ad68-2132">Richtige Anzeige von Ausnahmen (Azure/service-fabric-issues#1054)</span><span class="sxs-lookup"><span data-stu-id="7ad68-2132">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="7ad68-2133">„Update-AzServiceFabricDurability“ korrigiert, um die Clusterkonfiguration zu aktualisieren, bevor der VMSS-Vorgang „CreateOrUpdate“ gestartet wird</span><span class="sxs-lookup"><span data-stu-id="7ad68-2133">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="7ad68-2134">0.4.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="7ad68-2134">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="7ad68-2135">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7ad68-2135">Az.Profile</span></span>
* <span data-ttu-id="7ad68-2136">Problem mit „Get-AzSubscription“ in Cloud Shell behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-2136">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="7ad68-2137">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="7ad68-2137">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ad68-2138">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ad68-2138">Az.Compute</span></span>
* <span data-ttu-id="7ad68-2139">Neue Größen zur Whitelist von VM-Größen hinzugefügt, für die bei Verwendung des einfachen Parametersatzes für „New-AzVm“ der beschleunigte Netzwerkbetrieb aktiviert wird</span><span class="sxs-lookup"><span data-stu-id="7ad68-2139">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="7ad68-2140">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-2140">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7ad68-2141">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7ad68-2141">Az.DataLakeStore</span></span>
* <span data-ttu-id="7ad68-2142">Unterstützung für VNET-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-2142">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="7ad68-2143">Get-AzDataLakeStoreVirtualNetworkRule: Dient zum Abrufen oder Auflisten der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="7ad68-2143">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="7ad68-2144">Add-AzDataLakeStoreVirtualNetworkRule: Fügt dem angegebenen Data Lake Store-Konto eine Regel für das virtuelle Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="7ad68-2144">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="7ad68-2145">Set-AzDataLakeStoreVirtualNetworkRule: Ändert die angegebene Regel für das virtuelle Netzwerk in das angegebene Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="7ad68-2145">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="7ad68-2146">Remove-AzDataLakeStoreVirtualNetworkRule: Dient zum Löschen der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="7ad68-2146">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ad68-2147">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ad68-2147">Az.Network</span></span>
* <span data-ttu-id="7ad68-2148">Cmdlet „Test-AzNetworkWatcherConnectivity“ aktualisiert, Protokollwert wird jetzt an Back-End übergeben.</span><span class="sxs-lookup"><span data-stu-id="7ad68-2148">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="7ad68-2149">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-2149">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ad68-2150">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ad68-2150">Az.Resources</span></span>
* <span data-ttu-id="7ad68-2151">Problem behoben, aufgrund dessen „Get-AzRoleDefinition“ eine unverständliche Ausnahme auslöst (wenn das Standardprofil kein Abonnement enthält und kein Bereich festgelegt ist), indem im Szenario eine aussagekräftige Ausnahme hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="7ad68-2151">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="7ad68-2152">Außerdem wurde der Standardparametersatz auf „RoleDefinitionNameParameterSet“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-2152">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="7ad68-2153">0.3.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="7ad68-2153">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="7ad68-2154">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="7ad68-2154">Azure.Storage</span></span>
* <span data-ttu-id="7ad68-2155">Fehler beim Kopieren von Blobs/Dateien behoben, aufgrund dessen bei einem Metadatenproblem des Ziels keine Metadaten kopiert wurden</span><span class="sxs-lookup"><span data-stu-id="7ad68-2155">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="7ad68-2156">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7ad68-2156">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="7ad68-2157">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="7ad68-2157">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="7ad68-2158">Der Abruf der Speicherressourcennutzung eines bestimmten Standorts wird jetzt unterstützt, und das Hinzufügen einer Warnmeldung für den Abruf der globalen Speicherressourcennutzung ist überflüssig.</span><span class="sxs-lookup"><span data-stu-id="7ad68-2158">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="7ad68-2159">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="7ad68-2159">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7ad68-2160">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7ad68-2160">Az.CognitiveServices</span></span>
* <span data-ttu-id="7ad68-2161">„Get-AzCognitiveServicesAccountSkus“ wird ohne vorhandenes Konto unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-2161">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7ad68-2162">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7ad68-2162">Az.Compute</span></span>
* <span data-ttu-id="7ad68-2163">Korrektur von „Get-AzVM -ResourceGroupName <rg>“, sodass ggf. mehr als 50 Ergebnisse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="7ad68-2163">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="7ad68-2164">Der Cmdlet-Hilfe zu „New-AzVmss“ wurde ein Beispiel für „SimpleParameterSet“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-2164">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="7ad68-2165">Tippfehler in der Azure Disk Encryption-Statusmeldung behoben</span><span class="sxs-lookup"><span data-stu-id="7ad68-2165">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="7ad68-2166">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="7ad68-2166">Az.DataFactoryV2</span></span>
* <span data-ttu-id="7ad68-2167">Die Version des ADF .Net-SDK wurde auf 2.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7ad68-2167">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7ad68-2168">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7ad68-2168">Az.Network</span></span>
* <span data-ttu-id="7ad68-2169">NetworkProfile-Funktionalität wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ad68-2169">Added NetworkProfile functionality.</span></span> <span data-ttu-id="7ad68-2170">Neue Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-2170">new cmdlets added</span></span>
    - <span data-ttu-id="7ad68-2171">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7ad68-2171">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="7ad68-2172">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7ad68-2172">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="7ad68-2173">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7ad68-2173">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="7ad68-2174">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7ad68-2174">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="7ad68-2175">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="7ad68-2175">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="7ad68-2176">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="7ad68-2176">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="7ad68-2177">Dienstzuordnungslink in Subnetzmodell hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-2177">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="7ad68-2178">Cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-2178">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="7ad68-2179">Cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-2179">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7ad68-2180">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7ad68-2180">Az.RedisCache</span></span>
* <span data-ttu-id="7ad68-2181">Künftig sind beliebige Zeichenfolgen als Größenparameter zulässig.</span><span class="sxs-lookup"><span data-stu-id="7ad68-2181">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="7ad68-2182">P5 in Popup „PSArgumentCompleter“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-2182">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="7ad68-2183">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7ad68-2183">Az.Resources</span></span>
* <span data-ttu-id="7ad68-2184">Fehlender Parameter „-Mode“ zu „Set-AzPolicyDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="7ad68-2184">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="7ad68-2185">Cmdlet-Fehler bei „Get-AzProviderOperation“ für Vorgänge mit Ursprung behoben, der den Benutzer enthält</span><span class="sxs-lookup"><span data-stu-id="7ad68-2185">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="7ad68-2186">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7ad68-2186">Az.Sql</span></span>
* <span data-ttu-id="7ad68-2187">Problem behoben, aufgrund dessen einige Sicherungs-Cmdlets das aktuelle Azure-Abonnements nicht erkannt haben</span><span class="sxs-lookup"><span data-stu-id="7ad68-2187">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7ad68-2188">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7ad68-2188">Az.Websites</span></span>
* <span data-ttu-id="7ad68-2189">Neues Cmdlet „Get-AzWebAppContainerContinuousDeploymentUrl“ zum Abrufen der Webhook-URL von Continuous Deployment für Container</span><span class="sxs-lookup"><span data-stu-id="7ad68-2189">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="7ad68-2190">Neue Cmdlets „New-AzWebAppContainerPSSession“ und „Enter-WebAppContainerPSSession“ zum Initiieren einer PowerShell-Remotesitzung in einer Windows-Container-App</span><span class="sxs-lookup"><span data-stu-id="7ad68-2190">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="7ad68-2191">0.2.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="7ad68-2191">0.2.0 - September 2018</span></span>
 <span data-ttu-id="7ad68-2192">Erstrelease</span><span class="sxs-lookup"><span data-stu-id="7ad68-2192">Initial Release</span></span>
