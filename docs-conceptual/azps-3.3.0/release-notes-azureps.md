---
title: Versionshinweise zu Azure PowerShell
description: Hier erfahren Sie mehr über die aktuellen Updates für die Azure PowerShell-Module.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: fb934ed0f8bef5e2aff715debe5d406d54abf24f
ms.sourcegitcommit: 2d0c3ffaa5246f680784fa7e15b0d2536c27ff80
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2020
ms.locfileid: "75718983"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="98bd2-103">Versionshinweise zu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="98bd2-103">Azure PowerShell release notes</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="98bd2-104">3.3.0 – Januar 2020</span><span class="sxs-lookup"><span data-stu-id="98bd2-104">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="98bd2-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="98bd2-105">Az.Accounts</span></span>
* <span data-ttu-id="98bd2-106">„Add-AzEnvironment“ und „Set-AzEnvironment“ wurden so aktualisiert, dass sie jetzt die Parameter „AzureAttestationServiceEndpointResourceId“ und „AzureAttestationServiceEndpointSuffix“ akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="98bd2-106">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="98bd2-107">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="98bd2-107">Az.Cdn</span></span>
* <span data-ttu-id="98bd2-108">Anzeigen von Fehlerantwortdetails im Cmdlet „New-AzCdnEndpoint“</span><span class="sxs-lookup"><span data-stu-id="98bd2-108">Display error response deatil in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="98bd2-109">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="98bd2-109">Az.Compute</span></span>
* <span data-ttu-id="98bd2-110">Cmdlet „Set-AzVMCustomScriptExtension“ für eine VM mit verwaltetem Betriebssystemdatenträger ohne Betriebssystemprofil wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="98bd2-110">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="98bd2-111">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="98bd2-111">Az.ContainerInstance</span></span>
* <span data-ttu-id="98bd2-112">Im Beispiel von „New-AzContainerGroup“ verwendete Parameternamen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="98bd2-112">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="98bd2-113">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="98bd2-113">Az.DataBoxEdge</span></span>
* <span data-ttu-id="98bd2-114">Cmdlet „Get-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-114">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="98bd2-115">Edge-Speichercontainer abrufen</span><span class="sxs-lookup"><span data-stu-id="98bd2-115">Get the Edge Stroage Container</span></span>
* <span data-ttu-id="98bd2-116">Cmdlet „New-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-116">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="98bd2-117">Neuen Edge-Speichercontainer erstellen</span><span class="sxs-lookup"><span data-stu-id="98bd2-117">Create new Edge Stroage Container</span></span>
* <span data-ttu-id="98bd2-118">Cmdlet „Remove-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-118">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="98bd2-119">Edge-Speichercontainer entfernen</span><span class="sxs-lookup"><span data-stu-id="98bd2-119">Remove the Edge Stroage Container</span></span>
* <span data-ttu-id="98bd2-120">Cmdlet „Invoke-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-120">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="98bd2-121">Aktion zum Aktualisieren von Daten in Edge-Speichercontainer aufrufen</span><span class="sxs-lookup"><span data-stu-id="98bd2-121">Invoke action to refresh data on Edge Stroage Container</span></span>
* <span data-ttu-id="98bd2-122">Cmdlet „Get-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-122">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="98bd2-123">Edge-Speicherkonto abrufen</span><span class="sxs-lookup"><span data-stu-id="98bd2-123">Get the Edge Stroage Account</span></span>
* <span data-ttu-id="98bd2-124">Cmdlet „New-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-124">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="98bd2-125">Neues Edge-Speicherkonto erstellen</span><span class="sxs-lookup"><span data-stu-id="98bd2-125">Create new Edge Stroage Account</span></span>
* <span data-ttu-id="98bd2-126">Cmdlet „Remove-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-126">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="98bd2-127">Edge-Speicherkonto entfernen</span><span class="sxs-lookup"><span data-stu-id="98bd2-127">Remove the Edge Stroage Account</span></span>
* <span data-ttu-id="98bd2-128">Cmdlet „Invoke-AzDataBoxEdgeShare“ aufrufen</span><span class="sxs-lookup"><span data-stu-id="98bd2-128">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="98bd2-129">Aktion zum Aktualisieren von Daten auf Freigabe aufrufen</span><span class="sxs-lookup"><span data-stu-id="98bd2-129">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="98bd2-130">Cmdlet „Set-AzDataBoxEdgeStorageAccountCredential“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-130">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="98bd2-131">Festlegen der Speicherkonto-Anmeldeinformationen für „az databoxedge“</span><span class="sxs-lookup"><span data-stu-id="98bd2-131">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="98bd2-132">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="98bd2-132">Az.DataFactory</span></span>
* <span data-ttu-id="98bd2-133">Eigenschaften „AutoUpdateETA“, „LatestVersion“, „PushedVersion“, „TaskQueueId“ und „VersionStatus“ für Befehl „Get-AzDataFactoryV2IntegrationRuntime“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-133">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="98bd2-134">Version des ADF .NET SDK auf 4.6.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-134">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="98bd2-135">Parameter „PublicIPs“ wurde für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um das Erstellen der Azure-SSIS Integration Runtime mit statischen öffentlichen IP-Adressen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="98bd2-135">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="98bd2-136">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="98bd2-136">Az.DevTestLabs</span></span>
* <span data-ttu-id="98bd2-137">Fehlerhafter Link in „Get-AzDtlAllowedVMSizesPolicy.md“ entfernt</span><span class="sxs-lookup"><span data-stu-id="98bd2-137">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="98bd2-138">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="98bd2-138">Az.EventHub</span></span>
* <span data-ttu-id="98bd2-139">Behebung des Problems 10634: Verweis auf NULL-Objekt für „remove eventhubnamespace“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-139">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="98bd2-140">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="98bd2-140">Az.HDInsight</span></span>
* <span data-ttu-id="98bd2-141">Fehler in „Invoke-AzHDInsightHiveJob.md“ wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="98bd2-141">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="98bd2-142">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="98bd2-142">Az.MachineLearning</span></span>
* <span data-ttu-id="98bd2-143">Die folgenden Cmdlets wurden entfernt, da „MachineLearningCompute“ nicht mehr verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="98bd2-143">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="98bd2-144">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="98bd2-144">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="98bd2-145">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="98bd2-145">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="98bd2-146">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="98bd2-146">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="98bd2-147">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="98bd2-147">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="98bd2-148">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="98bd2-148">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="98bd2-149">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="98bd2-149">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="98bd2-150">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="98bd2-150">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="98bd2-151">Az.Network</span><span class="sxs-lookup"><span data-stu-id="98bd2-151">Az.Network</span></span>
* <span data-ttu-id="98bd2-152">Upgrade der Abhängigkeit von „Microsoft.Azure.Management.Sql“ von „1.36-preview“ auf „1.37-preview“</span><span class="sxs-lookup"><span data-stu-id="98bd2-152">Upgrade dependancy of Microsoft.Azure.Management.Sql from 1.36-preivew to 1.37-preivew</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="98bd2-153">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="98bd2-153">Az.RecoveryServices</span></span>
* <span data-ttu-id="98bd2-154">Änderung der Azure Site Recovery-Unterstützung für virtuelle Computer mit verwalteten Datenträgern, die im Ruhezustand mit von Kunden verwalteten Schlüsseln für Azure-zu-Azure-Anbieter verschlüsselt sind</span><span class="sxs-lookup"><span data-stu-id="98bd2-154">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed leys for Azure to Azure provider.</span></span>
* <span data-ttu-id="98bd2-155">Azure Site Recovery-Unterstützung für die Eingabe der ID des Datenträgerverschlüsselungssatzes als optionale Eingabe beim Aktivieren des Schutzes für VMware in Azure</span><span class="sxs-lookup"><span data-stu-id="98bd2-155">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="98bd2-156">Azure Site Recovery-Unterstützung für die Eingabe der ID des Datenträgerverschlüsselungssatzes als optionale Eingabe auf Datenträgerebene beim Aktivieren des Schutzes für VMware in Azure</span><span class="sxs-lookup"><span data-stu-id="98bd2-156">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="98bd2-157">Azure Site Recovery-Unterstützung zum Aktualisieren eines replikationsgeschützten Elements mit der Zuordnung eines Datenträgerverschlüsselungssatzes für HyperV in Azure</span><span class="sxs-lookup"><span data-stu-id="98bd2-157">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="98bd2-158">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="98bd2-158">Az.Resources</span></span>
* <span data-ttu-id="98bd2-159">Fehler in Hilfedokument zu „Remove-AzTag“ behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-159">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="98bd2-160">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="98bd2-160">Az.Sql</span></span>
* <span data-ttu-id="98bd2-161">Funktionalität der Baseline-Cmdlets für einen Sicherheitsrisikobewertungssatz korrigiert, sodass sie auf der Master-Datenbank für Azure Database funktionieren und sie auf Systemdatenbanken von verwalteten Instanzen einschränken.</span><span class="sxs-lookup"><span data-stu-id="98bd2-161">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="98bd2-162">Fehler beim Erstellen einer SQL-Instanzfailovergruppe behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-162">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="98bd2-163">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="98bd2-163">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="98bd2-164">DR als neuer gültiger Lizenztyp hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-164">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="98bd2-165">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="98bd2-165">Az.Storage</span></span>
* <span data-ttu-id="98bd2-166">Warnmeldung für Breaking Change hinzugefügt: Wertänderung für „DefaultAction“ in einer zukünftigen Version</span><span class="sxs-lookup"><span data-stu-id="98bd2-166">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="98bd2-167">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="98bd2-167">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="98bd2-168">Unterstützung für das Abrufen der letzten Synchronisierungszeit des Speicherkontos durch Ausführen von „get-AzureRMStorageAccount“ mit Parameter „-IncludeGeoReplicationStats“</span><span class="sxs-lookup"><span data-stu-id="98bd2-168">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span> 
    - <span data-ttu-id="98bd2-169">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="98bd2-169">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="98bd2-170">3.2.0: Dezember 2019</span><span class="sxs-lookup"><span data-stu-id="98bd2-170">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="98bd2-171">Allgemein</span><span class="sxs-lookup"><span data-stu-id="98bd2-171">General</span></span>
* <span data-ttu-id="98bd2-172">Verweise in „.psd1“ zur Verwendung des relativen Pfads für alle Module aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-172">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="98bd2-173">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="98bd2-173">Az.Accounts</span></span>
* <span data-ttu-id="98bd2-174">Richtiges UserAgent-Element für clientseitige Telemetrie für Az 4.0-Vorschauversion festgelegt</span><span class="sxs-lookup"><span data-stu-id="98bd2-174">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="98bd2-175">Anzeigen benutzerfreundlicher Fehlermeldungen, wenn der Kontext in der Az 4.0-Vorschauversion NULL ist</span><span class="sxs-lookup"><span data-stu-id="98bd2-175">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="98bd2-176">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="98bd2-176">Az.Batch</span></span>
* <span data-ttu-id="98bd2-177">Problem [#10602](https://github.com/Azure/azure-powershell/issues/10602) behoben, aufgrund dessen „VirtualMachineConfiguration.ContainerConfiguration“ oder „VirtualMachineConfiguration.DataDisks“ von **New-AzBatchPool** nicht ordnungsgemäß an den Server gesendet wurde</span><span class="sxs-lookup"><span data-stu-id="98bd2-177">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="98bd2-178">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="98bd2-178">Az.DataFactory</span></span>
* <span data-ttu-id="98bd2-179">Version des ADF .NET SDK auf 4.5.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-179">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="98bd2-180">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="98bd2-180">Az.FrontDoor</span></span>
* <span data-ttu-id="98bd2-181">Unterstützung für den Ausschluss verwalteter WAF-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-181">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="98bd2-182">SocketAddr zur automatischen Vervollständigung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-182">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="98bd2-183">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="98bd2-183">Az.HealthcareApis</span></span>
* <span data-ttu-id="98bd2-184">Ausnahmebehandlung</span><span class="sxs-lookup"><span data-stu-id="98bd2-184">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="98bd2-185">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="98bd2-185">Az.KeyVault</span></span>
* <span data-ttu-id="98bd2-186">Fehler im Zusammenhang mit dem Zugriff auf einen möglicherweise nicht festgelegten Wert behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-186">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="98bd2-187">Zertifikatverwaltung für Kryptografie für elliptische Kurve</span><span class="sxs-lookup"><span data-stu-id="98bd2-187">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="98bd2-188">Unterstützung zum Angeben der Kurve für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-188">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="98bd2-189">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="98bd2-189">Az.Monitor</span></span>
* <span data-ttu-id="98bd2-190">Optionales Argument zum Befehl „Diagnoseeinstellungen hinzufügen“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-190">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="98bd2-191">Ein Optionsargument, das angibt, dass der Export in Log Analytics ein festes Schema sein muss (auch bekannt als</span><span class="sxs-lookup"><span data-stu-id="98bd2-191">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="98bd2-192">dedizierter Datentyp)</span><span class="sxs-lookup"><span data-stu-id="98bd2-192">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="98bd2-193">Az.Network</span><span class="sxs-lookup"><span data-stu-id="98bd2-193">Az.Network</span></span>
* <span data-ttu-id="98bd2-194">Unterstützung für IpGroups in der AzureFirewall-Anwendung sowie in NAT- und Netzwerkregeln</span><span class="sxs-lookup"><span data-stu-id="98bd2-194">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="98bd2-195">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="98bd2-195">Az.Resources</span></span>
* <span data-ttu-id="98bd2-196">Problem behoben, aufgrund dessen die Vorlagenbereitstellung einen Vorlagenparameter nicht lesen kann, wenn der Name einen Konflikt mit einem integrierten Parameternamen verursacht</span><span class="sxs-lookup"><span data-stu-id="98bd2-196">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="98bd2-197">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-09-01 aktualisiert, die Gruppierungsunterstützung in Richtliniensatzdefinitionen einführt</span><span class="sxs-lookup"><span data-stu-id="98bd2-197">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="98bd2-198">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="98bd2-198">Az.Sql</span></span>
* <span data-ttu-id="98bd2-199">Speichererstellung in automatischer Aktivierung der Sicherheitsrisikobewertung auf StorageV2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-199">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="98bd2-200">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="98bd2-200">Az.Storage</span></span>
* <span data-ttu-id="98bd2-201">Unterstützung der Generierung blob-/containeridentitätsbasierter SAS-Token mit Speicherkontext auf der Grundlage der OAuth-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="98bd2-201">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="98bd2-202">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="98bd2-202">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="98bd2-203">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="98bd2-203">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="98bd2-204">Unterstützung für das Widerrufen von Schlüsseln für die Speicherkonto-Benutzerdelegierung hinzugefügt, sodass alle SAS-Identitätstoken widerrufen werden</span><span class="sxs-lookup"><span data-stu-id="98bd2-204">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="98bd2-205">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="98bd2-205">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="98bd2-206">Upgrade auf Microsoft.Azure.Management.Storage 14.2.0, um die neue API-Version 2019-06-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="98bd2-206">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="98bd2-207">Unterstützung von QuotaGiB (Freigabekontingent in Gibibyte) für Werte über 5120 in der Verwaltungsebene von Dateifreigabe-Cmdlets und Parameteralias „Quota“ zum Parameter „QuotaGiB“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-207">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span> 
    - <span data-ttu-id="98bd2-208">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="98bd2-208">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="98bd2-209">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="98bd2-209">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="98bd2-210">Parameteralias „QuotaGiB“ zum Parameter „Quota“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-210">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="98bd2-211">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="98bd2-211">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="98bd2-212">Problem behoben, dass „Set-AzStorageContainerAcl“ die gespeicherte Zugriffsrichtlinie bereinigen kann</span><span class="sxs-lookup"><span data-stu-id="98bd2-212">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="98bd2-213">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="98bd2-213">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="98bd2-214">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="98bd2-214">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="98bd2-215">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="98bd2-215">Highlights since the last major release</span></span>
* <span data-ttu-id="98bd2-216">Az.DataBoxEdge 1.0.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="98bd2-216">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="98bd2-217">Az.SqlVirtualMachine 1.0.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="98bd2-217">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="98bd2-218">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="98bd2-218">Az.Compute</span></span>
* <span data-ttu-id="98bd2-219">Funktion zum erneuten Anwenden von VMs</span><span class="sxs-lookup"><span data-stu-id="98bd2-219">VM Reapply feature</span></span>
    - <span data-ttu-id="98bd2-220">Parameter für erneutes Anwenden zu Cmdlet „Set-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-220">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="98bd2-221">AutomaticRepairs-Funktion für VM-Skalierungsgruppe:</span><span class="sxs-lookup"><span data-stu-id="98bd2-221">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="98bd2-222">Parameter „EnableAutomaticRepair“, „AutomaticRepairGracePeriod“ und „AutomaticRepairMaxInstanceRepairsPercent“ zu folgenden Cmdlets hinzugefügt:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="98bd2-222">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="98bd2-223">Mandantenübergreifende Unterstützung von Katalogimages für „New-AzVM“</span><span class="sxs-lookup"><span data-stu-id="98bd2-223">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="98bd2-224">„Spot“ zu Argumentvervollständigung des Priority-Parameters in Cmdlets „New-AzVM“, „New-AzVMConfig“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-224">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="98bd2-225">Parameter „DiskIOPSReadWrite“ und „DiskMBpsReadWrite“ zu Cmdlet „Add-AzVmssDataDisk“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-225">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="98bd2-226">Parameter „SourceImageId“ von Cmdlet „New-AzGalleryImageVersion“ in optional geändert</span><span class="sxs-lookup"><span data-stu-id="98bd2-226">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="98bd2-227">Parameter „OSDiskImage“ und „DataDiskImage“ zu Cmdlet „New-AzGalleryImageVersion“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-227">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="98bd2-228">Parameter „HyperVGeneration“ zu Cmdlet „New-AzGalleryImageDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-228">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="98bd2-229">Parameter „SkipExtensionsOnOverprovisionedVMs“ zu Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-229">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="98bd2-230">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="98bd2-230">Az.DataBoxEdge</span></span>
* <span data-ttu-id="98bd2-231">Cmdlet `Get-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-231">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="98bd2-232">Bestellung abrufen</span><span class="sxs-lookup"><span data-stu-id="98bd2-232">Get the Order</span></span>
* <span data-ttu-id="98bd2-233">Cmdlet `New-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-233">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="98bd2-234">Neue Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="98bd2-234">Create new Order</span></span>
* <span data-ttu-id="98bd2-235">Cmdlet `Remove-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-235">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="98bd2-236">Bestellung entfernen</span><span class="sxs-lookup"><span data-stu-id="98bd2-236">Remove the Order</span></span>
* <span data-ttu-id="98bd2-237">Änderung im Cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="98bd2-237">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="98bd2-238">Erstellt jetzt eine lokale Freigabe</span><span class="sxs-lookup"><span data-stu-id="98bd2-238">Now creates Local Share</span></span>
* <span data-ttu-id="98bd2-239">Cmdlet `Set-AzDataBoxEdgeRole` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-239">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="98bd2-240">„IotRole“ kann jetzt einer Freigabe zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="98bd2-240">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="98bd2-241">Cmdlet `Invoke-AzDataBoxEdgeDevice` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-241">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="98bd2-242">Scanupdate aufrufen, Update herunterladen, Updates auf dem Gerät installieren</span><span class="sxs-lookup"><span data-stu-id="98bd2-242">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="98bd2-243">Cmdlet `Get-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-243">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="98bd2-244">Ruft die Informationen zu Auslösern ab</span><span class="sxs-lookup"><span data-stu-id="98bd2-244">Gets the information about Triggers</span></span>
* <span data-ttu-id="98bd2-245">Cmdlet `New-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-245">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="98bd2-246">Neue Auslöser erstellen</span><span class="sxs-lookup"><span data-stu-id="98bd2-246">Create new Triggers</span></span>
* <span data-ttu-id="98bd2-247">Cmdlet `Remove-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-247">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="98bd2-248">Auslöser entfernen</span><span class="sxs-lookup"><span data-stu-id="98bd2-248">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="98bd2-249">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="98bd2-249">Az.DataFactory</span></span>
* <span data-ttu-id="98bd2-250">Version des ADF .NET SDK auf 4.4.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-250">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="98bd2-251">Parameter „ExpressCustomSetup“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um Setupkonfigurationen und Drittanbieterkomponenten ohne benutzerdefiniertes Setupskript zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="98bd2-251">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="98bd2-252">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="98bd2-252">Az.DataLakeStore</span></span>
* <span data-ttu-id="98bd2-253">Dokumentation von „Get-AzDataLakeStoreDeletedItem“ und „Restore-AzDataLakeStoreDeletedItem“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-253">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="98bd2-254">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="98bd2-254">Az.EventHub</span></span>
* <span data-ttu-id="98bd2-255">Behebung des Problems 10301: Datumsformat von SAS-Token korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-255">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="98bd2-256">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="98bd2-256">Az.FrontDoor</span></span>
* <span data-ttu-id="98bd2-257">Parameter „MinimumTlsVersion“ zu „Enable-AzFrontDoorCustomDomainHttps“ und „New-AzFrontDoorFrontendEndpointObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-257">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="98bd2-258">Parameter „HealthProbeMethod“ und „EnabledState“ zu „New-AzFrontDoorHealthProbeSettingObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-258">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="98bd2-259">Neues Cmdlet zum Erstellen von BackendPoolsSettings-Objekten für die Übergabe in Erstellung/Update von Front Door hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-259">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="98bd2-260">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="98bd2-260">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="98bd2-261">Az.Network</span><span class="sxs-lookup"><span data-stu-id="98bd2-261">Az.Network</span></span>
* <span data-ttu-id="98bd2-262">FilterData-Optionsbeispiele „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ geändert.</span><span class="sxs-lookup"><span data-stu-id="98bd2-262">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="98bd2-263">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="98bd2-263">Az.PrivateDns</span></span>
* <span data-ttu-id="98bd2-264">PrivateDns.net-SDK auf Version 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-264">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="98bd2-265">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="98bd2-265">Az.RecoveryServices</span></span>
* <span data-ttu-id="98bd2-266">Azure Site Recovery-Unterstützung zum Auswählen des Datenträgertyps beim Aktivieren des Schutzes.</span><span class="sxs-lookup"><span data-stu-id="98bd2-266">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="98bd2-267">Fehlerbehebung bei Bearbeitungsaktion für Azure Site Recovery-Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="98bd2-267">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="98bd2-268">SQL-Wiederherstellungsunterstützung für Azure Backup zum Akzeptieren von Filestream-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="98bd2-268">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="98bd2-269">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="98bd2-269">Az.RedisCache</span></span>
* <span data-ttu-id="98bd2-270">Parameter „MinimumTlsVersion“ in Cmdlets „New-AzRedisCache“ und „Set-AzRedisCache“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-270">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="98bd2-271">Außerdem „MinimumTlsVersion“ in Ausgabe von Cmdlet „Get-AzRedisCache“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-271">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="98bd2-272">Validierung von Parameter „-Size“ für Cmdlets „Set-AzRedisCache“ und „New-AzRedisCache“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-272">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="98bd2-273">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="98bd2-273">Az.Resources</span></span>
- <span data-ttu-id="98bd2-274">Richtlinien-Cmdlets aktualisiert, um die neue API-Version 2019-06-01 mit der neuen EnforcementMode-Eigenschaft bei der Richtlinienzuweisung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="98bd2-274">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="98bd2-275">Hilfebeispiel zum Erstellen von Richtliniendefinitionen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-275">Updated create policy definition help example</span></span>
- <span data-ttu-id="98bd2-276">Fehlerkorrektur: „Remove-AZADServicePrincipal -ServicePrincipalName“ gibt Nullverweis aus, wenn Dienstprinzipalname nicht gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="98bd2-276">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="98bd2-277">Fehlerkorrektur: „New-AZADServicePrincipal“ gibt Nullverweis aus, wenn Mandant kein Abonnement hat.</span><span class="sxs-lookup"><span data-stu-id="98bd2-277">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="98bd2-278">„New-AzAdServicePrincipal“ geändert, um Anmeldeinformation nur zu zugeordneter Anwendung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="98bd2-278">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="98bd2-279">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="98bd2-279">Az.Sql</span></span>
* <span data-ttu-id="98bd2-280">Unterstützung von „ReadReplicaCount“ für Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-280">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="98bd2-281">Korrektur von „Set-AzSqlDatabase“, wenn Zonenredundanz nicht festgelegt</span><span class="sxs-lookup"><span data-stu-id="98bd2-281">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="98bd2-282">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="98bd2-282">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="98bd2-283">Allgemein</span><span class="sxs-lookup"><span data-stu-id="98bd2-283">General</span></span>
* <span data-ttu-id="98bd2-284">Az.PrivateDns 1.0.0 veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="98bd2-284">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="98bd2-285">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="98bd2-285">Az.Accounts</span></span>
* <span data-ttu-id="98bd2-286">Hinweis zur Veraltung des Alias „Resolve-Error“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-286">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="98bd2-287">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="98bd2-287">Az.Advisor</span></span>
* <span data-ttu-id="98bd2-288">Neue Kategorie „Operational Excellence“ für Cmdlet „Get-AzAdvisorRecommendation“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-288">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="98bd2-289">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="98bd2-289">Az.Batch</span></span>
* <span data-ttu-id="98bd2-290">`CoreQuota` für `BatchAccountContext` in `DedicatedCoreQuota` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-290">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="98bd2-291">Außerdem wurde das neue Element `LowPriorityCoreQuota` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-291">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="98bd2-292">Dies wirkt sich auf **Get-AzBatchAccount** aus.</span><span class="sxs-lookup"><span data-stu-id="98bd2-292">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="98bd2-293">Für Parameter `-ResourceFile` von **New-AzBatchTask** wird jetzt eine Sammlung mit `PSResourceFile`-Objekten verwendet, und für die Erstellung kann das Cmdlet **New-AzBatchResourceFile** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="98bd2-293">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="98bd2-294">Neues Cmdlet **New-AzBatchResourceFile** als Hilfe für die Erstellung von `PSResourceFile`-Objekten.</span><span class="sxs-lookup"><span data-stu-id="98bd2-294">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="98bd2-295">Diese können für **New-AzBatchTask** über den Parameter `-ResourceFile` bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="98bd2-295">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="98bd2-296">Hierbei werden zusätzlich zum Ansatz mit `HttpUrl` zwei neue Arten von Ressourcendateien unterstützt:</span><span class="sxs-lookup"><span data-stu-id="98bd2-296">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="98bd2-297">Mit Ressourcendateien, die auf `AutoStorageContainerName` basieren, wird ein gesamter Container für die automatische Speicherung auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="98bd2-297">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="98bd2-298">Für Ressourcendateien, die auf `StorageContainerUrl` basieren, wird der in der URL angegebene Container auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="98bd2-298">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="98bd2-299">`ApplicationPackages`-Eigenschaft von `PSApplication` entfernt, die von **Get-AzBatchApplication** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="98bd2-299">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="98bd2-300">Die spezifischen Pakete in einer Anwendung können jetzt mit **Get-AzBatchApplicationPackage** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="98bd2-300">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="98bd2-301">Beispiel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="98bd2-301">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="98bd2-302">`ApplicationId` für **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** und **Set-AzBatchApplication** in `ApplicationName` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-302">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="98bd2-303">`ApplicationId` ist jetzt ein Alias von `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="98bd2-303">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="98bd2-304">Neue `PSWindowsUserConfiguration`-Eigenschaft zu `PSUserAccount` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-304">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="98bd2-305">`Version` für `PSApplicationPackage` in `Name` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-305">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="98bd2-306">`BlobSource` für `PSResourceFile` in `HttpUrl` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-306">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="98bd2-307">`OSDisk`-Eigenschaft aus `PSVirtualMachineConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-307">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="98bd2-308">**Set-AzBatchPoolOSVersion** entfernt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-308">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="98bd2-309">Dieser Vorgang wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-309">This operation is no longer supported.</span></span>
* <span data-ttu-id="98bd2-310">`TargetOSVersion` aus `PSCloudServiceConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-310">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="98bd2-311">`CurrentOSVersion` für `PSCloudServiceConfiguration` in `OSVersion` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-311">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="98bd2-312">`DataEgressGiB` und `DataIngressGiB` aus `PSPoolUsageMetrics` entfernt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-312">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="98bd2-313">**Get-AzBatchNodeAgentSku** entfernt und durch **Get-AzBatchSupportedImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-313">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="98bd2-314">**Get-AzBatchSupportedImage** gibt die gleichen Daten wie **Get-AzBatchNodeAgentSku** zurück, aber in einem benutzerfreundlicheren Format.</span><span class="sxs-lookup"><span data-stu-id="98bd2-314">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="98bd2-315">Neue nicht verifizierte Images werden nun ebenfalls zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="98bd2-315">New non-verified images are also now returned.</span></span> <span data-ttu-id="98bd2-316">Zusätzlich sind weitere Informationen zu `Capabilities` und `BatchSupportEndOfLife` für jedes Image vorhanden.</span><span class="sxs-lookup"><span data-stu-id="98bd2-316">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="98bd2-317">Möglichkeit zum Bereitstellen von Remotedateisystemen auf jedem Knoten eines Pools über den neuen Parameter `MountConfiguration` von **New-AzBatchPool** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-317">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="98bd2-318">Es ist jetzt Unterstützung für Sicherheitsregeln vorhanden, die den Netzwerkzugriff auf einen Pool basierend auf dem Quellport des Datenverkehrs blockieren.</span><span class="sxs-lookup"><span data-stu-id="98bd2-318">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="98bd2-319">Dies erfolgt über die `SourcePortRanges`-Eigenschaft unter `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="98bd2-319">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="98bd2-320">Bei der Ausführung eines Containers unterstützt Batch jetzt die Ausführung der Aufgabe im Arbeitsverzeichnis des Containers bzw. im Arbeitsverzeichnis der Batch-Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="98bd2-320">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="98bd2-321">Dies wird mit der `WorkingDirectory`-Eigenschaft unter `PSTaskContainerSettings` gesteuert.</span><span class="sxs-lookup"><span data-stu-id="98bd2-321">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="98bd2-322">Möglichkeit zum Angeben einer Sammlung mit öffentlichen IP-Adressen für `PSNetworkConfiguration` über die neue `PublicIPs`-Eigenschaft hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-322">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="98bd2-323">So wird sichergestellt, dass Knoten im Pool über eine IP-Adresse aus der Liste mit den von Benutzern bereitgestellten IP-Adressen verfügen.</span><span class="sxs-lookup"><span data-stu-id="98bd2-323">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="98bd2-324">Wenn kein Wert angegeben wird, lautet der Standardwert von `WaitForSuccess` unter `PSSTartTask` jetzt `$True` (bisher `$False`).</span><span class="sxs-lookup"><span data-stu-id="98bd2-324">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="98bd2-325">Wenn kein Wert angegeben wird, lautet der Standardwert von `Scope` unter `PSAutoUserSpecification` jetzt `Pool` (bisher `Task` unter Windows und `Pool` unter Linux).</span><span class="sxs-lookup"><span data-stu-id="98bd2-325">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="98bd2-326">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="98bd2-326">Az.Cdn</span></span>
* <span data-ttu-id="98bd2-327">„UrlRewriteAction“ und „CacheKeyQueryStringAction“ für „RulesEngine“ eingeführt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-327">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="98bd2-328">Mehrere Fehler behoben, z. B. fehlende „Selector“-Eingabe im Cmdlet „New-AzDeliveryRuleCondition“.</span><span class="sxs-lookup"><span data-stu-id="98bd2-328">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="98bd2-329">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="98bd2-329">Az.Compute</span></span>
* <span data-ttu-id="98bd2-330">Feature „Datenträgerverschlüsselungssatz“</span><span class="sxs-lookup"><span data-stu-id="98bd2-330">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="98bd2-331">Neue Cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="98bd2-331">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="98bd2-332">Parameter „DiskEncryptionSetId“ wurde den folgenden Cmdlets hinzugefügt: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="98bd2-332">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="98bd2-333">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="98bd2-333">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="98bd2-334">Die Parameter „DiskEncryptionSetId“ und „EncryptionType“ wurden den folgenden Cmdlets hinzugefügt:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="98bd2-334">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="98bd2-335">Parameter „PublicIPAddressVersion“ wurde „New-AzVmssIPConfig“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-335">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="98bd2-336">„FileUris“ für benutzerdefinierte Skripterweiterung von öffentlicher Einstellung auf geschützte Einstellung umgestellt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-336">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="98bd2-337">„ScaleInPolicy“ wurde den Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-337">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="98bd2-338">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="98bd2-338">Breaking changes</span></span>
    - <span data-ttu-id="98bd2-339">Parameter „UploadSizeInBytes“ wird anstelle von „DiskSizeGB“ für „New-AzDiskConfig“ verwendet, wenn „CreateOption“ auf „Upload“ festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="98bd2-339">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="98bd2-340">Im „GalleryImageVersion“-Objekt wurde „objectPublishingProfile.Source.ManagedImage.Id“ durch „StorageProfile.Source.Id“ ersetzt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-340">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="98bd2-341">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="98bd2-341">Az.DataFactory</span></span>
* <span data-ttu-id="98bd2-342">Version des ADF .NET SDK auf 4.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="98bd2-342">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="98bd2-343">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="98bd2-343">Az.DataLakeStore</span></span>
* <span data-ttu-id="98bd2-344">Update für ADLS SDK-Version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) mit den folgenden Fehlerbehebungen durchgeführt:</span><span class="sxs-lookup"><span data-stu-id="98bd2-344">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="98bd2-345">Vermeidung der Auslösung einer Ausnahme, während die Deserialisierung des „creationtime“-Elements des Papierkorb- oder Verzeichniseintrags nicht durchgeführt werden kann</span><span class="sxs-lookup"><span data-stu-id="98bd2-345">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="98bd2-346">Verfügbarmachung der Einstellung pro Anforderungszeitlimit in „adlsclient“</span><span class="sxs-lookup"><span data-stu-id="98bd2-346">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="98bd2-347">Fehlerbehebung für Übergabe des ursprünglichen „syncflag“-Elements für badoffset-Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="98bd2-347">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="98bd2-348">Fehlerbehebung für „EnumerateDirectory“ zum Abrufen des Fortsetzungstokens nach der Überprüfung der Antwort</span><span class="sxs-lookup"><span data-stu-id="98bd2-348">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="98bd2-349">Behebung eines Verkettungsfehlers</span><span class="sxs-lookup"><span data-stu-id="98bd2-349">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="98bd2-350">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="98bd2-350">Az.FrontDoor</span></span>
* <span data-ttu-id="98bd2-351">Verschiedene Tippfehler im Modul korrigiert.</span><span class="sxs-lookup"><span data-stu-id="98bd2-351">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="98bd2-352">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="98bd2-352">Az.HDInsight</span></span>
* <span data-ttu-id="98bd2-353">Fehler behoben, bei dem Kunden die Meldung „Keine gültige Base64-Zeichenfolge“ erhalten haben, wenn sie „Get-AzHDInsightCluster“ zum Abrufen des Clusters mit ADLSGen1-Speicher verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="98bd2-353">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="98bd2-354">Parameter mit dem Namen „ApplicationId“ den drei Cmdlets „Add-AzHDInsightClusterIdentity“, „New-AzHDInsightClusterConfig“ und „New-AzHDInsightCluster“ hinzugefügt, damit der Kunde die Dienstprinzipal-Anwendungs-ID für den Zugriff auf Azure Data Lake bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="98bd2-354">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="98bd2-355">Microsoft.Azure.Management.HDInsight von 2.1.0 in 5.1.0 geändert.</span><span class="sxs-lookup"><span data-stu-id="98bd2-355">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="98bd2-356">Fünf Cmdlets wurden entfernt:</span><span class="sxs-lookup"><span data-stu-id="98bd2-356">Removed five cmdlets:</span></span>
    - <span data-ttu-id="98bd2-357">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="98bd2-357">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="98bd2-358">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="98bd2-358">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="98bd2-359">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="98bd2-359">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="98bd2-360">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="98bd2-360">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="98bd2-361">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="98bd2-361">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="98bd2-362">Drei Cmdlets wurden hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="98bd2-362">Added three cmdlets:</span></span>
    - <span data-ttu-id="98bd2-363">„Get-AzHDInsightMonitoring“ als Ersatz für „Get-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="98bd2-363">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="98bd2-364">„Enable-AzHDInsightMonitoring“ als Ersatz für „Enable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="98bd2-364">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="98bd2-365">„Disable-AzHDInsightMonitoring“ als Ersatz für „Disable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="98bd2-365">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="98bd2-366">Fehler für Cmdlet „Get-AzHDInsightProperties“ behoben, um Unterstützung für das Abrufen von Funktionsinformationen von einem bestimmten Ort bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="98bd2-366">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="98bd2-367">Parametersätze („Spark1“, „Spark2“) aus „Add-AzHDInsightConfigValue“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-367">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="98bd2-368">Beispiele den Hilfedokumenten des Cmdlets „Add-AzHDInsightSecurityProfile“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-368">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="98bd2-369">Der Ausgabetyp der folgenden Cmdlets wurde geändert:</span><span class="sxs-lookup"><span data-stu-id="98bd2-369">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="98bd2-370">Ausgabetyp für „Get-AzHDInsightProperties“ von „CapabilitiesResponse“ in „AzureHDInsightCapabilities“ geändert.</span><span class="sxs-lookup"><span data-stu-id="98bd2-370">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="98bd2-371">Ausgabetyp für „Remove-AzHDInsightCluster“ von „ClusterGetResponse“ in „bool“ geändert.</span><span class="sxs-lookup"><span data-stu-id="98bd2-371">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="98bd2-372">Ausgabetyp für „Set-AzHDInsightGatewaySettings“ von „HttpConnectivitySettings“ in „GatewaySettings“ geändert.</span><span class="sxs-lookup"><span data-stu-id="98bd2-372">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="98bd2-373">Einige Testfälle für Szenarien wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-373">Added some scenario test cases.</span></span>
* <span data-ttu-id="98bd2-374">Aliase wurden entfernt: „Add-AzHDInsightConfigValues“, „Get-AzHDInsightProperties“.</span><span class="sxs-lookup"><span data-stu-id="98bd2-374">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="98bd2-375">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="98bd2-375">Az.IotHub</span></span>
* <span data-ttu-id="98bd2-376">Wichtige Änderungen:</span><span class="sxs-lookup"><span data-stu-id="98bd2-376">Breaking changes:</span></span>
    - <span data-ttu-id="98bd2-377">Das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="98bd2-377">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="98bd2-378">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-378">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="98bd2-379">Das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="98bd2-379">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="98bd2-380">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-380">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="98bd2-381">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-381">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="98bd2-382">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-382">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="98bd2-383">Das Cmdlet „New-AzIotHubExportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubExportDevices“.</span><span class="sxs-lookup"><span data-stu-id="98bd2-383">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="98bd2-384">Das Cmdlet „New-AzIotHubImportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubImportDevices“.</span><span class="sxs-lookup"><span data-stu-id="98bd2-384">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="98bd2-385">Das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="98bd2-385">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="98bd2-386">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-386">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="98bd2-387">Das Cmdlet „Set-AzIotHub“ unterstützt den Parameter „OperationsMonitoringProperties“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="98bd2-387">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="98bd2-388">Der Parametersatz „UpdateOperationsMonitoringProperties“ für das Cmdlet „Set-AzIotHub“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-388">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="98bd2-389">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="98bd2-389">Az.RecoveryServices</span></span>
* <span data-ttu-id="98bd2-390">Azure wurde die Azure Site Recovery-Unterstützung zum Konfigurieren von Netzwerkressourcen, z. B. NSG, öffentliche IP-Adresse und interner Load Balancer für Azure, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-390">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="98bd2-391">Azure Site Recovery-Unterstützung zum Schreiben auf verwaltete Datenträger für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-391">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="98bd2-392">Azure Site Recovery-Unterstützung für NIC-Reduzierung für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-392">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="98bd2-393">Azure wurde Azure Site Recovery-Unterstützung für beschleunigten Netzwerkbetrieb für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-393">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="98bd2-394">Azure wurde Azure Site Recovery-Unterstützung für automatische Agent-Updates für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-394">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="98bd2-395">Azure wurde Azure Site Recovery-Unterstützung für SSD Standard für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-395">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="98bd2-396">Azure wurde Azure Site Recovery-Unterstützung für das zweistufige Azure Disk Encryption-Verfahren für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-396">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="98bd2-397">Azure wurde Azure Site Recovery-Unterstützung für das Schützen von neu hinzugefügten Datenträgern für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-397">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="98bd2-398">Feature „Vorläufiges Löschen“ (SoftDelete) für VM und zugehörige Tests hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-398">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="98bd2-399">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="98bd2-399">Az.Resources</span></span>
* <span data-ttu-id="98bd2-400">Abhängigkeitsassembly „Microsoft.Extensions.Caching.Memory“ von 1.1.1 auf 2.2 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="98bd2-400">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="98bd2-401">Az.Network</span><span class="sxs-lookup"><span data-stu-id="98bd2-401">Az.Network</span></span>
* <span data-ttu-id="98bd2-402">Alle Cmdlets für „PrivateEndpointConnection“ geändert, um Unterstützung für generischen Dienstanbieter bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="98bd2-402">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="98bd2-403">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="98bd2-403">Updated cmdlet:</span></span>
        - <span data-ttu-id="98bd2-404">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="98bd2-404">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="98bd2-405">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="98bd2-405">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="98bd2-406">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="98bd2-406">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="98bd2-407">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="98bd2-407">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="98bd2-408">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="98bd2-408">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="98bd2-409">Neues Cmdlet für „PrivateLinkResource“ hinzugefügt, einschließlich Unterstützung des generischen Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="98bd2-409">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="98bd2-410">Neues Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="98bd2-410">New cmdlet:</span></span>
        - <span data-ttu-id="98bd2-411">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="98bd2-411">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="98bd2-412">Neue Felder und Parameter für das Feature „Proxyprotokoll V2“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-412">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="98bd2-413">„EnableProxyProtocol“-Eigenschaft in „PrivateLinkService“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-413">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="98bd2-414">„LinkIdentifier“-Eigenschaft in „PrivateEndpointConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-414">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="98bd2-415">„New-AzPrivateLinkService“ aktualisiert, um den neuen optionalen Parameter „EnableProxyProtocol“ hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="98bd2-415">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="98bd2-416">Fehlerhafte Parameterbeschreibung in Referenzdokumentation von „New-AzApplicationGatewaySku“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="98bd2-416">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="98bd2-417">Neue Cmdlets zur Unterstützung der Azure-Firewallrichtlinie hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-417">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="98bd2-418">Unterstützung für untergeordnete Ressource „RouteTables“ von VirtualHub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-418">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="98bd2-419">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="98bd2-419">New cmdlets added:</span></span>
        - <span data-ttu-id="98bd2-420">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="98bd2-420">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="98bd2-421">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="98bd2-421">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="98bd2-422">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="98bd2-422">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="98bd2-423">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="98bd2-423">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="98bd2-424">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="98bd2-424">Set-AzVirtualHub</span></span>
* <span data-ttu-id="98bd2-425">Unterstützung für die neuen Eigenschaften „Sku“ von VirtualHub und „VirtualWANType“ von VirtualWan hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-425">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="98bd2-426">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="98bd2-426">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="98bd2-427">New-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-427">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="98bd2-428">Update-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-428">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="98bd2-429">New-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-429">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="98bd2-430">Update-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-430">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="98bd2-431">Unterstützung für „EnableInternetSecurity“-Eigenschaft für „HubVnetConnection“, „VpnConnection“ und „ExpressRouteConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-431">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="98bd2-432">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="98bd2-432">New cmdlets added:</span></span>
        - <span data-ttu-id="98bd2-433">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="98bd2-433">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="98bd2-434">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="98bd2-434">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="98bd2-435">New-AzureRmVirtualHubVnetConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-435">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="98bd2-436">New-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-436">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="98bd2-437">Update-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-437">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="98bd2-438">New-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-438">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="98bd2-439">Set-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-439">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="98bd2-440">Unterstützung für die Konfiguration der „WebApplicationFirewall“-Richtlinie der obersten Ebene hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-440">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="98bd2-441">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="98bd2-441">New cmdlets added:</span></span>
        - <span data-ttu-id="98bd2-442">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="98bd2-442">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="98bd2-443">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="98bd2-443">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="98bd2-444">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="98bd2-444">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="98bd2-445">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="98bd2-445">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="98bd2-446">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="98bd2-446">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="98bd2-447">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="98bd2-447">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="98bd2-448">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="98bd2-448">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="98bd2-449">New-AzApplicationGatewayFirewallPolicy: Parameter „PolicySetting“, „ManagedRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-449">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="98bd2-450">Unterstützung für Operator „Geo-Match“ unter „CustomRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-450">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="98bd2-451">„GeoMatch“ zum Operator von „FirewallCondition“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-451">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="98bd2-452">Unterstützung für Firewallrichtlinien „perListener“ und „perSite“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-452">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="98bd2-453">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="98bd2-453">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="98bd2-454">New-AzApplicationGatewayHttpListener: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-454">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="98bd2-455">New-AzApplicationGatewayPathRuleConfig: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-455">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="98bd2-456">Fehlerbehebung: Nichtbeachtung der Groß-/Kleinschreibung für erforderliches Subnetz mit dem Namen „AzureBastionSubnet“ in „PSBastion“ ist jetzt möglich.</span><span class="sxs-lookup"><span data-stu-id="98bd2-456">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="98bd2-457">Unterstützung für Ziel-FQDNs in Netzwerkregeln und Übersetzung von FQDN in NAT-Regeln für Azure Firewall hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-457">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="98bd2-458">Unterstützung für Ressource „RouteTables“ der obersten Ebene von „IpGroup“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-458">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="98bd2-459">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="98bd2-459">New cmdlets added:</span></span>
        - <span data-ttu-id="98bd2-460">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="98bd2-460">New-AzIpGroup</span></span>
        - <span data-ttu-id="98bd2-461">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="98bd2-461">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="98bd2-462">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="98bd2-462">Get-AzIpGroup</span></span>
        - <span data-ttu-id="98bd2-463">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="98bd2-463">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="98bd2-464">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="98bd2-464">Az.ServiceFabric</span></span>
* <span data-ttu-id="98bd2-465">Cmdlet „Add-AzServiceFabricApplicationCertificate“ entfernt, da dieses Szenario durch „Add-AzVmssSecret“ abgedeckt ist.</span><span class="sxs-lookup"><span data-stu-id="98bd2-465">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="98bd2-466">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="98bd2-466">Az.Sql</span></span>
* <span data-ttu-id="98bd2-467">Unterstützung für die Wiederherstellung von gelöschten Datenbanken auf verwalteten Instanzen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-467">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="98bd2-468">Veraltete Cmdlets für die Überprüfung aus Code ausgesondert.</span><span class="sxs-lookup"><span data-stu-id="98bd2-468">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="98bd2-469">Veraltete Aliase entfernt:</span><span class="sxs-lookup"><span data-stu-id="98bd2-469">Removed deprecated aliases:</span></span>
* <span data-ttu-id="98bd2-470">Get-AzSqlDatabaseIndexRecommendations (stattdessen „Get-AzSqlDatabaseIndexRecommendation“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="98bd2-470">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="98bd2-471">Get-AzSqlDatabaseRestorePoints (stattdessen „Get-AzSqlDatabaseRestorePoint“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="98bd2-471">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="98bd2-472">Cmdlet „Get-AzSqlDatabaseSecureConnectionPolicy“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-472">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="98bd2-473">Aliase für veraltete Cmdlets für Einstellungen zur Sicherheitsrisikobewertung wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-473">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="98bd2-474">Cmdlets für Einstellungen für die erweiterte Bedrohungserkennung wurden als veraltet eingestuft.</span><span class="sxs-lookup"><span data-stu-id="98bd2-474">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="98bd2-475">Cmdlets zum Deaktivieren und Aktivieren von Vertraulichkeitsempfehlungen in Spalten einer Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-475">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="98bd2-476">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="98bd2-476">Az.Storage</span></span>
* <span data-ttu-id="98bd2-477">Unterstützung für große Dateifreigaben beim Erstellen oder Aktualisieren eines Speicherkontos hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-477">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="98bd2-478">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="98bd2-478">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="98bd2-479">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="98bd2-479">Set-AzStorageAccount</span></span>
* <span data-ttu-id="98bd2-480">Beim Schließen/Abrufen des Dateihandles wird die Überprüfung des Eingabepfads auf Dateiverzeichnis oder Datei übersprungen, um einen Fehler für das Objekt im Status „DeletePending“ zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="98bd2-480">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="98bd2-481">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="98bd2-481">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="98bd2-482">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="98bd2-482">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="98bd2-483">2.8.0: Oktober 2019</span><span class="sxs-lookup"><span data-stu-id="98bd2-483">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="98bd2-484">Allgemein</span><span class="sxs-lookup"><span data-stu-id="98bd2-484">General</span></span>
* <span data-ttu-id="98bd2-485">Az.HealthcareApis-Release 1.0.0</span><span class="sxs-lookup"><span data-stu-id="98bd2-485">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="98bd2-486">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="98bd2-486">Az.Accounts</span></span>
* <span data-ttu-id="98bd2-487">Telemetriedaten und URL-Umschreibung für generierte Module aktualisiert, Windows-Komponententests korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-487">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="98bd2-488">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="98bd2-488">Az.ApiManagement</span></span>
* <span data-ttu-id="98bd2-489">**Set-AzApiManagementApi**: Unterstützung für die Aktualisierung der API in „ApiVersionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-489">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="98bd2-490">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="98bd2-490">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="98bd2-491">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="98bd2-491">Az.Automation</span></span>
* <span data-ttu-id="98bd2-492">Cmdlet „New-AzureAutomationSoftwareUpdateConfiguration“ für den Parameter für die Linux-Neustarteinstellung korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-492">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="98bd2-493">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="98bd2-493">Az.Batch</span></span>
* <span data-ttu-id="98bd2-494">**Get-AzBatchNodeAgentSku** ist veraltet und wird in Version 2.0.0 durch **Get-AzBatchSupportImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-494">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="98bd2-495">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="98bd2-495">Az.Compute</span></span>
* <span data-ttu-id="98bd2-496">Parameter „Priority“, „EvictionPolicy“ und „MaxPrice“ zu den Cmdlets „“New-AzVM“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-496">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="98bd2-497">Warnmeldung und Hilfedokument für die Cmdlets „Add-AzVMAdditionalUnattendContent“ und „Add-AzVMSshPublicKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-497">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="98bd2-498">Ausnahme „-skipVmBackup“ Linux-VMs mit verwalteten Datenträgern für „Set-AzVMDiskEncryptionExtension“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-498">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="98bd2-499">Fehler beim Aktualisieren von Verschlüsselungseinstellungen in „Set-AzVMDiskEncryptionExtension“ korrigiert (zweistufiges Szenario)</span><span class="sxs-lookup"><span data-stu-id="98bd2-499">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="98bd2-500">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="98bd2-500">Az.DataFactory</span></span>
* <span data-ttu-id="98bd2-501">CRUD-Befehle für ADF V2-Datenfluss hinzugefügt: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow und Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="98bd2-501">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="98bd2-502">Aktionsbefehle für Debugsitzung für ADF V2-Datenfluss hinzugefügt: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand und Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="98bd2-502">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="98bd2-503">Version des ADF .NET SDK auf 4.2.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-503">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="98bd2-504">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="98bd2-504">Az.DataLakeStore</span></span>
* <span data-ttu-id="98bd2-505">Kontoüberprüfung korrigiert, sodass Konten mit „-“ ohne Domäne übermittelt werden können</span><span class="sxs-lookup"><span data-stu-id="98bd2-505">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="98bd2-506">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="98bd2-506">Az.HealthcareApis</span></span>
* <span data-ttu-id="98bd2-507">PowerShell-Version auf 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-507">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="98bd2-508">SDK-Version auf 1.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-508">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="98bd2-509">Aktualisierung in Tests, um auf neue SDK-Version zu verweisen</span><span class="sxs-lookup"><span data-stu-id="98bd2-509">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="98bd2-510">Ausgabestruktur von geschachtelt in vereinfacht geändert</span><span class="sxs-lookup"><span data-stu-id="98bd2-510">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="98bd2-511">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="98bd2-511">Az.IotHub</span></span>
* <span data-ttu-id="98bd2-512">Neue Routingquelle hinzugefügt: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="98bd2-512">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="98bd2-513">Kleinere Fehlerbehebung: „Get-AzIothub“ gibt „subscriptionId“ nicht zurück.</span><span class="sxs-lookup"><span data-stu-id="98bd2-513">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="98bd2-514">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="98bd2-514">Az.Monitor</span></span>
* <span data-ttu-id="98bd2-515">Neue Aktionsgruppenempfänger für Aktionsgruppe hinzugefügt:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="98bd2-515">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="98bd2-516">Verwendung des allgemeinen Warnungsschemas für Empfänger aktiviert.</span><span class="sxs-lookup"><span data-stu-id="98bd2-516">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="98bd2-517">Dies gilt nicht für SMS, Azure App-Pushbenachrichtigungen, ITSM und Sprachempfänger.</span><span class="sxs-lookup"><span data-stu-id="98bd2-517">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="98bd2-518">Webhooks unterstützen nun die Azure Active Directory-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="98bd2-518">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="98bd2-519">Az.Network</span><span class="sxs-lookup"><span data-stu-id="98bd2-519">Az.Network</span></span>
* <span data-ttu-id="98bd2-520">Neues Cmdlet „Get-AzAvailableServiceAlias“ hinzugefügt, das zum Abrufen der Aliase aufgerufen werden kann, die für Dienstendpunktrichtlinien verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="98bd2-520">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="98bd2-521">Unterstützung für das Hinzufügen von Verbindungen von Datenverkehrsselektoren zu Virtual Network-Gatewayverbindungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-521">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="98bd2-522">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="98bd2-522">New cmdlets added:</span></span>
        - <span data-ttu-id="98bd2-523">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="98bd2-523">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="98bd2-524">Cmdlets mit optionalen Parametern aktualisiert: -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="98bd2-524">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="98bd2-525">Unterstützung für ESP- und AH-Protokolle in Konfigurationen von Netzwerksicherheitsregeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-525">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="98bd2-526">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="98bd2-526">Updated cmdlets:</span></span>
        - <span data-ttu-id="98bd2-527">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="98bd2-527">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="98bd2-528">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="98bd2-528">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="98bd2-529">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="98bd2-529">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="98bd2-530">Verbesserte Behandlung von Ausnahmen in Cortex-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="98bd2-530">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="98bd2-531">Neue Generationen und SKUs für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="98bd2-531">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="98bd2-532">Einführung neuer Generationen für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="98bd2-532">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="98bd2-533">Einführung neuer SKUs mit höherem Durchsatz für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="98bd2-533">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="98bd2-534">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="98bd2-534">Az.RedisCache</span></span>
* <span data-ttu-id="98bd2-535">Referenzdokumentation zu „Set-AzRedisCache“ aktualisiert, um fehlende Werte für den Parameter „-Size“ aufzunehmen</span><span class="sxs-lookup"><span data-stu-id="98bd2-535">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="98bd2-536">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="98bd2-536">Az.Sql</span></span>
* <span data-ttu-id="98bd2-537">Unterstützung für das Festlegen des Active Directory-Administrators für verwaltete Instanz hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-537">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="98bd2-538">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="98bd2-538">Az.Storage</span></span>
* <span data-ttu-id="98bd2-539">Storage-Clientbibliothek auf 11.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-539">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="98bd2-540">Auflisten von Containern mit der API der Verwaltungsebene, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="98bd2-540">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="98bd2-541">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="98bd2-541">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="98bd2-542">Auflisten von Storage-Konten aus Abonnements, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="98bd2-542">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="98bd2-543">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="98bd2-543">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="98bd2-544">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="98bd2-544">Az.StorageSync</span></span>
* <span data-ttu-id="98bd2-545">Problem 9810 in „Reset-AzStorageSyncServerCertificate“ behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-545">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="98bd2-546">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="98bd2-546">Az.Websites</span></span>
* <span data-ttu-id="98bd2-547">Fehler beim Aktualisieren von ASP einer App mit „Set-AzWebApp“</span><span class="sxs-lookup"><span data-stu-id="98bd2-547">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="98bd2-548">2.7.0: September 2019</span><span class="sxs-lookup"><span data-stu-id="98bd2-548">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="98bd2-549">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="98bd2-549">Az.ApiManagement</span></span>
* <span data-ttu-id="98bd2-550">Beschreibung des Parameters „-Format“ in der Referenzdokumentation für „Set-AzApiManagementPolicy“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-550">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="98bd2-551">Verweise des veralteten Cmdlets „Update-AzApiManagementDeployment“ aus Referenzdokumentation entfernt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-551">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="98bd2-552">Verwenden Sie stattdessen „Set-AzApiManagement“.</span><span class="sxs-lookup"><span data-stu-id="98bd2-552">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="98bd2-553">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="98bd2-553">Az.Automation</span></span>
* <span data-ttu-id="98bd2-554">Tippfehler im Beispiel in der Referenzdokumentation für „Register-AzAutomationDscNode“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-554">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="98bd2-555">Erläuterung zur Betriebssystemeinschränkung zu „Register-AzAutomationDSCNode“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-555">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="98bd2-556">Nullverweisausnahme des Cmdlets „Start-AzAutomationRunbook“ für die Option „-Wait“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="98bd2-556">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="98bd2-557">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="98bd2-557">Az.Compute</span></span>
* <span data-ttu-id="98bd2-558">Parameter „UploadSizeInBytes“ zu „New-AzDiskConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-558">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="98bd2-559">Inkrementeller Parameter zu „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-559">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="98bd2-560">Feature für VM mit niedriger Priorität hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="98bd2-560">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="98bd2-561">Parameter „MaxPrice“, „EvictionPolicy“ und „Priority“ zu New-AzVMConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-561">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="98bd2-562">Parameter „MaxPrice“ zu den Cmdlets „New-AzVmssConfig“, „Update-AzVM“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-562">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="98bd2-563">Fehlerbehebung für VM-Verweis für das Cmdlet „Get-AzAvailabilitySet“, wenn alle Verfügbarkeitsgruppen im Abonnement aufgelistet werden</span><span class="sxs-lookup"><span data-stu-id="98bd2-563">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="98bd2-564">Nullausnahme für „Get-AzRemoteDesktopFile“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-564">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="98bd2-565">VHD-Suchmethode für Position relativ zum Ende korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-565">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="98bd2-566">Problem mit UltraSSD für „New-AzVM“ und „Update-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-566">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="98bd2-567">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="98bd2-567">Az.DataFactory</span></span>
* <span data-ttu-id="98bd2-568">Drei neue Befehle für ADF V2 hinzugefügt: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription und Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="98bd2-568">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="98bd2-569">Version des ADF .NET SDK auf 4.1.3 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-569">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="98bd2-570">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="98bd2-570">Az.HDInsight</span></span>
* <span data-ttu-id="98bd2-571">Hinweis auf Breaking Changes hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-571">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="98bd2-572">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="98bd2-572">Az.IotHub</span></span>
* <span data-ttu-id="98bd2-573">Unterstützung zum Aufrufen eines Failovers für einen IoT-Hub zur geografisch gekoppelten Notfallwiederherstellungsregion hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-573">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="98bd2-574">Unterstützung zum Verwalten der Nachrichtenanreicherung für einen IoT-Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-574">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="98bd2-575">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="98bd2-575">New cmdlets are:</span></span>
    - <span data-ttu-id="98bd2-576">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="98bd2-576">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="98bd2-577">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="98bd2-577">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="98bd2-578">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="98bd2-578">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="98bd2-579">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="98bd2-579">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="98bd2-580">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="98bd2-580">Az.Monitor</span></span>
* <span data-ttu-id="98bd2-581">Verweis auf das aktuelle Monitor SDK, d. h. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="98bd2-581">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="98bd2-582">Geringfügige Änderungen an den Metrik-Cmdlets vorgenommen, d. h. die Einheitenenumeration unterstützt verschiedene neue Werte.</span><span class="sxs-lookup"><span data-stu-id="98bd2-582">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="98bd2-583">Dabei handelt es sich um schreibgeschützte Cmdlets, sodass keine Änderungen an der Eingabe der Cmdlets erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="98bd2-583">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="98bd2-584">Die API-Version der **ActionGroups**-Anforderungen lautet jetzt **2019-06-01** (zuvor **2018-03-01**).</span><span class="sxs-lookup"><span data-stu-id="98bd2-584">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="98bd2-585">Die Szenariotests wurden aktualisiert, um diese Änderung zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="98bd2-585">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="98bd2-586">Die Konstruktoren für die Klassen **EmailReceiver** und **WebhookReceiver** haben ein neues obligatorisches Argument hinzugefügt, d. h. einen booleschen Wert namens **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="98bd2-586">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="98bd2-587">Derzeit ist der Wert auf **false** festgelegt, damit sich dieser Breaking Change nicht auf die Cmdlets auswirkt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-587">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="98bd2-588">**HINWEIS:** Dies ist eine vorübergehende Änderung, die vom Team für Warnungen validiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="98bd2-588">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="98bd2-589">Die Reihenfolge der Argumente für den Konstruktor der Klasse **Source** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="98bd2-589">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="98bd2-590">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="98bd2-590">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="98bd2-591">Die Reihenfolge der Argumente für den Konstruktor der Klasse **AlertingAction** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="98bd2-591">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="98bd2-592">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="98bd2-592">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="98bd2-593">Unterstützung von Kriterien für dynamische Schwellwerte für Metrikwarnung v2</span><span class="sxs-lookup"><span data-stu-id="98bd2-593">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="98bd2-594">New-AzMetricAlertRuleV2Criteria: Erstellt nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="98bd2-594">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="98bd2-595">Add-AzMetricAlertRuleV2: Akzeptiert nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="98bd2-595">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="98bd2-596">Verbesserungen an den Cmdlets für geplante Abfrageregeln (Scheduled Query Rule, SQR)</span><span class="sxs-lookup"><span data-stu-id="98bd2-596">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="98bd2-597">Cmdlets akzeptieren den Parameter „Location“ in zwei Formaten: entweder den Standort (z. B. „eastus“) oder den Anzeigenamen des Standorts (z. B. „USA, Osten“)</span><span class="sxs-lookup"><span data-stu-id="98bd2-597">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="98bd2-598">Parameter „Enabled“ in Hilfedateien ordnungsgemäß dargestellt</span><span class="sxs-lookup"><span data-stu-id="98bd2-598">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="98bd2-599">Beispiele für optionalen Parameter „ActionGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-599">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="98bd2-600">Hilfedateien insgesamt verbessert</span><span class="sxs-lookup"><span data-stu-id="98bd2-600">Overall improved help files</span></span>
* <span data-ttu-id="98bd2-601">Fehler beim Bestimmen des Bereichstyps für „Set-AzActionRule“ behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-601">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="98bd2-602">Az.Network</span><span class="sxs-lookup"><span data-stu-id="98bd2-602">Az.Network</span></span>
* <span data-ttu-id="98bd2-603">Fehlerhaftes Beispiel in der Referenzdokumentation zu „New-AzApplicationGateway“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-603">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="98bd2-604">Hinweis in der Referenzdokumentation zu „Get-AzNetworkWatcherPacketCapture“ zum Abrufen aller Eigenschaften für eine Paketerfassung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-604">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="98bd2-605">Beispiel in der Referenzdokumentation zu „Test-AzNetworkWatcherIPFlow“ korrigiert, um die Netzwerkadapter ordnungsgemäß aufzulisten</span><span class="sxs-lookup"><span data-stu-id="98bd2-605">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="98bd2-606">Cloudausnahmeanalyse verbessert, um ggf. zusätzliche Details anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="98bd2-606">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="98bd2-607">Cloudausnahmeanalyse verbessert, um zusätzlichen Typ der SDK-Ausnahme zu verarbeiten</span><span class="sxs-lookup"><span data-stu-id="98bd2-607">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="98bd2-608">Falsche Zuordnung der Sicherheitsregelmodelle korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-608">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="98bd2-609">Eigenschaften zur Netzwerkschnittstelle für das Feature für die private IP-Adresse hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-609">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="98bd2-610">Eigenschaft „PrivateEndpoint“ als Typ „PSResourceId“ zu „PSNetworkInterface“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-610">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="98bd2-611">Eigenschaft „PrivateLinkConnectionProperties“ als Typ „PSIpConfigurationConnectivityInformation“ zu „PSNetworkInterfaceIPConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-611">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="98bd2-612">Neue Modellklasse „PSIpConfigurationConnectivityInformation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-612">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="98bd2-613">Neues ApplicationRuleProtocolType-Element „mssql“ für Azure Firewall-Ressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-613">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="98bd2-614">Unterstützung von Mehrfachverbindungen in Virtual WAN</span><span class="sxs-lookup"><span data-stu-id="98bd2-614">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="98bd2-615">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="98bd2-615">New cmdlets</span></span>
        - <span data-ttu-id="98bd2-616">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="98bd2-616">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="98bd2-617">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="98bd2-617">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="98bd2-618">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="98bd2-618">Updated cmdlet:</span></span>
        - <span data-ttu-id="98bd2-619">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="98bd2-619">New-VpnSite</span></span>
        - <span data-ttu-id="98bd2-620">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="98bd2-620">Update-VpnSite</span></span>
        - <span data-ttu-id="98bd2-621">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="98bd2-621">New-VpnConnection</span></span>
        - <span data-ttu-id="98bd2-622">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="98bd2-622">Update-VpnConnection</span></span>
* <span data-ttu-id="98bd2-623">Dokumente für einige PowerShell-Beispiele korrigiert, sodass Az-Cmdlets anstelle von AzureRM-Cmdlets verwendet werden</span><span class="sxs-lookup"><span data-stu-id="98bd2-623">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="98bd2-624">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="98bd2-624">Az.RecoveryServices</span></span>
* <span data-ttu-id="98bd2-625">AzureVMpolicy-Objekt mit ProtectedItemsCount-Attribut aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-625">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="98bd2-626">Tests für VM-Richtlinie und Wiederherstellung des ursprünglichen Speicherkontos hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-626">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="98bd2-627">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="98bd2-627">Az.Resources</span></span>
* <span data-ttu-id="98bd2-628">Fehler behoben, aufgrund dessen „New-AzRoleAssignment“ nicht ohne den Parameter „Scope“ aufgerufen werden konnte</span><span class="sxs-lookup"><span data-stu-id="98bd2-628">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="98bd2-629">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="98bd2-629">Az.ServiceFabric</span></span>
* <span data-ttu-id="98bd2-630">Tippfehler im Beispiel für die Referenzdokumentation „Update-AzServiceFabricReliability“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-630">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="98bd2-631">Neue Cmdlets zum Verwalten von Anwendung und Diensten hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="98bd2-631">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="98bd2-632">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="98bd2-632">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="98bd2-633">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="98bd2-633">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="98bd2-634">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="98bd2-634">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="98bd2-635">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="98bd2-635">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="98bd2-636">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="98bd2-636">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="98bd2-637">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="98bd2-637">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="98bd2-638">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="98bd2-638">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="98bd2-639">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="98bd2-639">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="98bd2-640">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="98bd2-640">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="98bd2-641">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="98bd2-641">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="98bd2-642">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="98bd2-642">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="98bd2-643">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="98bd2-643">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="98bd2-644">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="98bd2-644">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="98bd2-645">Service Fabric SDK auf Version 1.2.0 aktualisiert, die API-Version 2019-03-01 des Service Fabric-Ressourcenanbieters verwendet</span><span class="sxs-lookup"><span data-stu-id="98bd2-645">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="98bd2-646">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="98bd2-646">Az.SignalR</span></span>
* <span data-ttu-id="98bd2-647">Cmdlets „Update“, „Restart“, „CheckNameAvailability“ und „GetUsage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-647">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="98bd2-648">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="98bd2-648">Az.Sql</span></span>
* <span data-ttu-id="98bd2-649">Beispiel in der Referenzdokumentation für „Get-AzSqlElasticPool“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-649">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="98bd2-650">V-Kern-Beispiel zum Erstellen eines Pools für elastische Datenbanken hinzugefügt (New-AzSqlElasticPool)</span><span class="sxs-lookup"><span data-stu-id="98bd2-650">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="98bd2-651">Überprüfung von „EmailAddresses“ sowie Validierung, dass „EmailAdmins“ nicht auf „false“ festgelegt ist, in „Set-AzSqlServerAdvancedThreatProtectionPolicy“ und „Set-AzSqlDatabaseAdvancedThreatProtectionPolicy“ entfernt, wenn „EmailAddresses“ leer ist</span><span class="sxs-lookup"><span data-stu-id="98bd2-651">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="98bd2-652">Entfernen der Einstellungen für Server-/Datenbanküberwachung aktiviert, wenn mehrere Diagnoseeinstellungen vorhanden sind, die eine Überwachungskategorie ermöglichen</span><span class="sxs-lookup"><span data-stu-id="98bd2-652">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="98bd2-653">Überprüfung von E-Mail-Adressen in mehreren Cmdlets für die SQL-Sicherheitsrisikobewertung korrigiert (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting und Update-AzSqlInstanceVulnerabilityAssessmentSetting)</span><span class="sxs-lookup"><span data-stu-id="98bd2-653">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="98bd2-654">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="98bd2-654">Az.Storage</span></span>
* <span data-ttu-id="98bd2-655">Beispiel in der Referenzdokumentation für „Get-AzStorageAccountKey“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-655">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="98bd2-656">Beim Upload/Download von Azure-Dateien wird das Beibehalten der SMB-Eigenschaften der Quelldateien (Dateiattribute, Zeitpunkt der Dateierstellung, letzter Schreibzugriff für die Datei) in der Zieldatei unterstützt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-656">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="98bd2-657">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="98bd2-657">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="98bd2-658">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="98bd2-658">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="98bd2-659">Fehler beim Hochladen von Blockblobs mit Eigenschaften/Metadaten für das für einen Container aktivierte ImmutabilityPolicy-Element behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-659">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="98bd2-660">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="98bd2-660">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="98bd2-661">Unterstützung für die Verwaltung von Azure-Dateifreigaben mit der API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="98bd2-661">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="98bd2-662">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="98bd2-662">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="98bd2-663">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="98bd2-663">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="98bd2-664">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="98bd2-664">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="98bd2-665">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="98bd2-665">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="98bd2-666">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="98bd2-666">Az.Websites</span></span>
* <span data-ttu-id="98bd2-667">Problem behoben, aufgrund dessen webapp-Tags beim Migrieren der App zu neuem ASP gelöscht wurden</span><span class="sxs-lookup"><span data-stu-id="98bd2-667">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="98bd2-668">„Publish-AzureWebapp“ für die Verwendung unter Linux und Windows korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-668">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="98bd2-669">Beispiel in Referenzdokumentation „Get-AzWebAppPublishingProfile“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-669">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="98bd2-670">2.6.0: August 2019</span><span class="sxs-lookup"><span data-stu-id="98bd2-670">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="98bd2-671">Allgemein</span><span class="sxs-lookup"><span data-stu-id="98bd2-671">General</span></span>
* <span data-ttu-id="98bd2-672">Verschiedene Tippfehler in zahlreichen Modulen korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-672">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="98bd2-673">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="98bd2-673">Az.Accounts</span></span>
* <span data-ttu-id="98bd2-674">Unterstützung der benutzerseitig zugewiesenen MSI in Azure Functions-Authentifizierung (#9479)</span><span class="sxs-lookup"><span data-stu-id="98bd2-674">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="98bd2-675">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="98bd2-675">Az.Aks</span></span>
* <span data-ttu-id="98bd2-676">Problem mit der Ausgabe für „Get-AzAks“ behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-676">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="98bd2-677">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="98bd2-677">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="98bd2-678">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="98bd2-678">Az.ApiManagement</span></span>
* <span data-ttu-id="98bd2-679">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="98bd2-679">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="98bd2-680">.NET-NuGet-Version aktualisiert, die keine Einschränkungen für „productId“, „apiId“, „groupId“ und „userId“ erzwingt</span><span class="sxs-lookup"><span data-stu-id="98bd2-680">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="98bd2-681">**Get-AzApiManagementProduct:** Unterstützung für das Abfragen von Produkten mithilfe der API hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-681">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="98bd2-682">**New-AzApiManagementApiRevision:** Problem behoben, aufgrund dessen „ApiRevisionDescription“ beim Erstellen einer neuen API-Revision nicht festgelegt wurde https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="98bd2-682">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="98bd2-683">Tippfehler im Modell „PsApiManagementOAuth2AuthrozationServer“ korrigiert: PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="98bd2-683">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="98bd2-684">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="98bd2-684">Az.Batch</span></span>
* <span data-ttu-id="98bd2-685">Tippfehler in Hilfemeldung und Dokumentation korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="98bd2-685">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="98bd2-686">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="98bd2-686">Az.Cdn</span></span>
* <span data-ttu-id="98bd2-687">Tippfehler im Hilfsprogramm für die CDN-Modulkonvertierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-687">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="98bd2-688">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="98bd2-688">Az.Compute</span></span>
* <span data-ttu-id="98bd2-689">VmssId zum Cmdlet „New-AzVMConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-689">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="98bd2-690">Parameter „TerminateScheduledEvents“ und „TerminateScheduledEventNotBeforeTimeoutInMinutes“ zu „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-690">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="98bd2-691">HyperVGeneration-Eigenschaft zu VM-Imageobjekt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-691">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="98bd2-692">Host- und HostGroup-Features hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-692">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="98bd2-693">Neue Cmdlets:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="98bd2-693">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="98bd2-694">Parameter „HostId“ zu „New-AzVMConfig“ und „New-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-694">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="98bd2-695">Beispiel in der Dokumentation zu „Invoke-AzVMRunCommand“ zur Verwendung des richtigen Parameternamens aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-695">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="98bd2-696">Beschreibung für „-VolumeType“ in der Referenzdokumentation zu „Set-AzVMDiskEncryptionExtension“ und „Set-AzVmssDiskEncryptionExtension“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-696">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="98bd2-697">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="98bd2-697">Az.DataFactory</span></span>
* <span data-ttu-id="98bd2-698">Tippfehler in der Dokumentation zu „New-AzDataFactoryEncryptValue“ korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="98bd2-698">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="98bd2-699">Version des ADF .NET SDK auf 4.1.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-699">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="98bd2-700">Parameter „DataProxyIntegrationRuntimeName“, „DataProxyStagingLinkedServiceName“ und „DataProxyStagingPath“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um die Einrichtung der selbstgehosteten Integration Runtime als Proxy für die SSIS Integration Runtime zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="98bd2-700">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="98bd2-701">„PSTriggerRun“ zum Anzeigen der ausgelösten Pipelines, Meldungen und Eigenschaften und „PSActivityRun“ zum Anzeigen des Aktivitätstyps aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-701">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="98bd2-702">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="98bd2-702">Az.DataLakeStore</span></span>
* <span data-ttu-id="98bd2-703">Hängen von „Get-DataLakeStoreDeletedItem“ aufgrund von Fehlern oder Remoteausnahmen behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-703">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="98bd2-704">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="98bd2-704">Az.EventHub</span></span>
* <span data-ttu-id="98bd2-705">Behebung des Problems #9658: Tippfehler im Parameter „VirtualNteworkRule“ in „Set-AzEventHubNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="98bd2-705">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="98bd2-706">Behebung des Problems #9558: „Set-AzEventHubNamespace“ verwendet PATCH anstelle von PUT.</span><span class="sxs-lookup"><span data-stu-id="98bd2-706">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="98bd2-707">Parameter „EnableKafka“ zum Cmdlet „Set-AzEventHubNamespace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-707">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="98bd2-708">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="98bd2-708">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="98bd2-709">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="98bd2-709">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="98bd2-710">Tippfehler („Azure“ in Kleinbuchstaben) in der Dokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-710">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="98bd2-711">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="98bd2-711">Az.Monitor</span></span>
* <span data-ttu-id="98bd2-712">Falscher Parametername in der Hilfedokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-712">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="98bd2-713">Az.Network</span><span class="sxs-lookup"><span data-stu-id="98bd2-713">Az.Network</span></span>
* <span data-ttu-id="98bd2-714">„New-AzPrivateLinkServiceIpConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-714">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="98bd2-715">Parameter „PublicIpAddress“ ausgemustert, da er auf Serverseite nie verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="98bd2-715">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="98bd2-716">Optionaler Parameter „Primary“ hinzugefügt, der angibt, ob die aktuelle IP-Konfiguration die primäre ist oder nicht</span><span class="sxs-lookup"><span data-stu-id="98bd2-716">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="98bd2-717">Verbesserte Verarbeitung der Anforderungsfehlerausnahme aus dem SDK: Behebt das Problem, dass vorherige SDK-Ausnahmen nicht richtig behandelt wurden, was dazu führt, dass Schlüsselfehlerdetails nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="98bd2-717">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="98bd2-718">Validierungslogik für Ipv6-IP-Präfix angepasst, damit auf die richtige IPv6-Präfixlänge geprüft wird</span><span class="sxs-lookup"><span data-stu-id="98bd2-718">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="98bd2-719">„Get-AzVirtualNetworkSubnetConfig“ aktualisiert: Parametersatz zum Abrufen nach Subnetzressourcen-ID hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-719">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="98bd2-720">Aktualisierte Beschreibung des Location-Parameters für „AzNetworkServiceTag“</span><span class="sxs-lookup"><span data-stu-id="98bd2-720">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="98bd2-721">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="98bd2-721">Az.OperationalInsights</span></span>
* <span data-ttu-id="98bd2-722">Aktualisierte Dokumentation für „New-AzOperationalInsightsLinuxSyslogDataSource“</span><span class="sxs-lookup"><span data-stu-id="98bd2-722">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="98bd2-723">Beispiel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-723">Added example</span></span>
    - <span data-ttu-id="98bd2-724">Beschreibung für den Parameter „-Name“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-724">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="98bd2-725">Beispiel für „New-AzOperationalInsightsWindowsEventDataSource“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-725">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="98bd2-726">Beschreibung des Parameters „-Name“ für „New-AzOperationalInsightsWindowsEventDataSource“ geändert</span><span class="sxs-lookup"><span data-stu-id="98bd2-726">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="98bd2-727">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="98bd2-727">Az.RecoveryServices</span></span>
* <span data-ttu-id="98bd2-728">„Get-AzRecoveryServicesBackupJobDetail.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-728">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="98bd2-729">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="98bd2-729">Az.Resources</span></span>
* <span data-ttu-id="98bd2-730">Unterstützung für die neue API-Version 2019-05-10 für Microsoft.Resource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-730">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="98bd2-731">Unterstützung für „copy.count = 0“ für Variablen, Ressourcen und Eigenschaften hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-731">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="98bd2-732">Ressourcen mit „condition = false“ oder „copy.count = 0“ werden im vollständigen Modus gelöscht.</span><span class="sxs-lookup"><span data-stu-id="98bd2-732">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="98bd2-733">Beispiel zum Hinzufügen einer Richtlinie auf Abonnementebene zur Hilfedokumentation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-733">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="98bd2-734">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="98bd2-734">Az.ServiceBus</span></span>
* <span data-ttu-id="98bd2-735">Behebung des Problems #9658: Tippfehler für Parameter „VirtualNetworkRule“ in „Set-AzServiceBusNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="98bd2-735">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="98bd2-736">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="98bd2-736">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="98bd2-737">Neuer Befehl „Test-AzServiceBusNameAvailability“ zum Überprüfen der Verfügbarkeit des Namens für Warteschlange und Thema hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-737">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="98bd2-738">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="98bd2-738">Az.ServiceFabric</span></span>
* <span data-ttu-id="98bd2-739">Fehler bei Cmdlets zum Hinzufügen des Knotentyps korrigiert:</span><span class="sxs-lookup"><span data-stu-id="98bd2-739">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="98bd2-740">Fehler „NullReferenceException“, wenn die Ressourcengruppe andere VMSS enthielt, die nicht mit dem Service Fabric-Cluster in Zusammenhang stehen</span><span class="sxs-lookup"><span data-stu-id="98bd2-740">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="98bd2-741">Problembehebung: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="98bd2-741">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="98bd2-742">Fehler behoben, aufgrund dessen bei einem Cmdlet ein Fehler auftrat, wenn sich „virtualNetwork“ in einer anderen Ressourcengruppe befand als der Cluster</span><span class="sxs-lookup"><span data-stu-id="98bd2-742">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="98bd2-743">Problembehebung: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="98bd2-743">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="98bd2-744">Cmdlet „Add-AzServiceFabricApplicationCertificate“ ausgemustert</span><span class="sxs-lookup"><span data-stu-id="98bd2-744">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="98bd2-745">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="98bd2-745">Az.Sql</span></span>
* <span data-ttu-id="98bd2-746">Dokumentation alter Überwachungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-746">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="98bd2-747">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="98bd2-747">Az.Storage</span></span>
* <span data-ttu-id="98bd2-748">Hilfe für „Get/Close-AzStorageFileHandle“ aktualisiert (weitere Szenarien zu Cmdlet-Beispielen hinzugefügt und Parameterbeschreibungen aktualisiert)</span><span class="sxs-lookup"><span data-stu-id="98bd2-748">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="98bd2-749">Unterstützung von „StandardBlobTier“ in Uploadblobs und Kopierblobs</span><span class="sxs-lookup"><span data-stu-id="98bd2-749">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="98bd2-750">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="98bd2-750">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="98bd2-751">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="98bd2-751">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="98bd2-752">Unterstützung der Aktivierungspriorität im Kopierblob</span><span class="sxs-lookup"><span data-stu-id="98bd2-752">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="98bd2-753">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="98bd2-753">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="98bd2-754">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="98bd2-754">Az.Websites</span></span>
* <span data-ttu-id="98bd2-755">Hinzufügen von Erläuterungen zum Parameter „-AppSettings“ in „Set-AzWebApp“ und „Set-AzWebAppSlot“</span><span class="sxs-lookup"><span data-stu-id="98bd2-755">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="98bd2-756">2.5.0: Juli 2019</span><span class="sxs-lookup"><span data-stu-id="98bd2-756">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="98bd2-757">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="98bd2-757">Az.Accounts</span></span>
* <span data-ttu-id="98bd2-758">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="98bd2-758">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="98bd2-759">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="98bd2-759">Az.ApplicationInsights</span></span>
* <span data-ttu-id="98bd2-760">Tippfehler im Beispiel in der Dokumentation zu „Remove-AzApplicationInsightsApiKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-760">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="98bd2-761">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="98bd2-761">Az.Automation</span></span>
* <span data-ttu-id="98bd2-762">Tippfehler in der Ressourcenzeichenfolge korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-762">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="98bd2-763">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="98bd2-763">Az.CognitiveServices</span></span>
* <span data-ttu-id="98bd2-764">Unterstützung für NetworkRuleSet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-764">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="98bd2-765">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="98bd2-765">Az.Compute</span></span>
* <span data-ttu-id="98bd2-766">Fehlende Eigenschaften (ComputerName, OsName, OsVersion und HyperVGeneration) des Objekts für die VM-Instanzenansicht hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-766">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="98bd2-767">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="98bd2-767">Az.ContainerRegistry</span></span>
* <span data-ttu-id="98bd2-768">Tippfehler in „Remove-AzContainerRegistryReplication“ für den Replikationsparameter korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-768">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="98bd2-769">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="98bd2-769">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="98bd2-770">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="98bd2-770">Az.DataFactory</span></span>
* <span data-ttu-id="98bd2-771">Version des ADF .NET SDK auf 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-771">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="98bd2-772">Tippfehler in der Dokumentation für „Get-AzDataFactoryV2PipelineRun“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-772">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="98bd2-773">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="98bd2-773">Az.EventHub</span></span>
* <span data-ttu-id="98bd2-774">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="98bd2-774">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="98bd2-775">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="98bd2-775">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="98bd2-776">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="98bd2-776">Az.KeyVault</span></span>
* <span data-ttu-id="98bd2-777">Unterstützung zum Angeben von KeySize für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-777">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="98bd2-778">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="98bd2-778">Az.LogicApp</span></span>
* <span data-ttu-id="98bd2-779">Korrektur für „Get-AzIntegrationAccountMap“ zum Auflisten aller Zuordnungstypen</span><span class="sxs-lookup"><span data-stu-id="98bd2-779">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="98bd2-780">Neuer MapType-Parameter für Filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-780">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="98bd2-781">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="98bd2-781">Az.ManagedServices</span></span>
* <span data-ttu-id="98bd2-782">Unterstützung für API-Version 2019-06-01 (GA) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-782">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="98bd2-783">Az.Network</span><span class="sxs-lookup"><span data-stu-id="98bd2-783">Az.Network</span></span>
* <span data-ttu-id="98bd2-784">Unterstützung für privaten Endpunkt und privaten Verknüpfungsdienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-784">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="98bd2-785">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="98bd2-785">New cmdlets</span></span>
        - <span data-ttu-id="98bd2-786">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="98bd2-786">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="98bd2-787">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="98bd2-787">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="98bd2-788">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="98bd2-788">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="98bd2-789">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="98bd2-789">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="98bd2-790">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="98bd2-790">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="98bd2-791">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="98bd2-791">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="98bd2-792">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="98bd2-792">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="98bd2-793">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="98bd2-793">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="98bd2-794">Folgende Befehle für das Feature aktualisiert: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies für Subnetz in VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="98bd2-794">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="98bd2-795">„New-AzVirtualNetworkSubnetConfig“, „Set-AzVirtualNetworkSubnetConfig“ und „Add-AzVirtualNetworkSubnetConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-795">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="98bd2-796">Optionaler Parameter „-PrivateEndpointNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den privaten Endpunkt in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="98bd2-796">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="98bd2-797">Optionaler Parameter „-PrivateLinkServiceNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den Privat Link-Dienst in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="98bd2-797">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="98bd2-798">Der Cmdlet-Parameter „ServiceName“ von AzPrivateLinkService wurde aus Gründen der Abwärtskompatibilität in „Name“ mit dem Alias „ServiceName“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-798">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="98bd2-799">ICMP-Protokoll für Konfigurationen von Netzwerksicherheitsregeln aktiviert</span><span class="sxs-lookup"><span data-stu-id="98bd2-799">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="98bd2-800">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="98bd2-800">Updated cmdlets</span></span>
        - <span data-ttu-id="98bd2-801">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="98bd2-801">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="98bd2-802">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="98bd2-802">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="98bd2-803">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="98bd2-803">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="98bd2-804">ConnectionProtocolType (Ikev1/Ikev2) als konfigurierbarer Parameter für „New-AzVirtualNetworkGatewayConnection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-804">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="98bd2-805">PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-805">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="98bd2-806">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="98bd2-806">Updated cmdlet:</span></span>
        - <span data-ttu-id="98bd2-807">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="98bd2-807">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="98bd2-808">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="98bd2-808">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="98bd2-809">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="98bd2-809">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="98bd2-810">Application Gateway-Befehl „New-AzApplicationGatewayProbeConfig“ zur Unterstützung des benutzerdefinierten Ports im Test aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-810">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="98bd2-811">„New-AzApplicationGatewayProbeConfig“ aktualisiert: Optionaler Parameter „Port“ hinzugefügt, der zum Testen des Back-End-Servers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="98bd2-811">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="98bd2-812">Dieser Parameter gilt für Standard_V2 und WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="98bd2-812">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="98bd2-813">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="98bd2-813">Az.OperationalInsights</span></span>
* <span data-ttu-id="98bd2-814">Standardversion für gespeicherte Suchvorgänge auf 1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-814">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="98bd2-815">Verarbeitung des regulären NULL-Ausdrucks in benutzerdefinierten Protokollen korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-815">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="98bd2-816">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="98bd2-816">Az.RecoveryServices</span></span>
* <span data-ttu-id="98bd2-817">„Get-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-817">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="98bd2-818">„Get-AzRecoveryServicesBackupContainer.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-818">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="98bd2-819">„Get-AzRecoveryServicesVault.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-819">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="98bd2-820">„Wait-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-820">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="98bd2-821">„Set-AzRecoveryServicesVaultContext.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-821">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="98bd2-822">„Get-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-822">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="98bd2-823">„Get-AzRecoveryServicesBackupRecoveryPoint.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-823">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="98bd2-824">„Restore-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-824">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="98bd2-825">Dienstaufruf zum Aufheben der Containerregistrierung für Azure-Dateifreigabe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-825">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="98bd2-826">„Set-AzRecoveryServicesAsrAlertSetting.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-826">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="98bd2-827">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="98bd2-827">Az.Resources</span></span>
- <span data-ttu-id="98bd2-828">Fehlendes Cmdlet entfernt, auf das in der Dokumentation zu „New-AzResourceGroupDeployment“ verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="98bd2-828">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="98bd2-829">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-829">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="98bd2-830">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="98bd2-830">Az.ServiceBus</span></span>
* <span data-ttu-id="98bd2-831">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="98bd2-831">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="98bd2-832">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="98bd2-832">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="98bd2-833">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="98bd2-833">Az.Sql</span></span>
* <span data-ttu-id="98bd2-834">Fehlende Beispiele für Cmdlet „Set-AzSqlDatabaseSecondary“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-834">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="98bd2-835">Festlegen wiederkehrender Überprüfungen der Sicherheitsrisikobewertung ohne Angabe von E-Mail-Adressen korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-835">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="98bd2-836">Tippfehler in einer Warnmeldung korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-836">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="98bd2-837">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="98bd2-837">Az.Storage</span></span>
* <span data-ttu-id="98bd2-838">Beispiel in Referenzdokumentation für „Get-AzStorageAccount“ aktualisiert, sodass der richtige Parametername verwendet wird</span><span class="sxs-lookup"><span data-stu-id="98bd2-838">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="98bd2-839">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="98bd2-839">Az.StorageSync</span></span>
* <span data-ttu-id="98bd2-840">Cmdlet „Invoke-AzStorageSyncChangeDetection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-840">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="98bd2-841">Problem 9551 zur Berücksichtigung von „TierFilesOlderThanDays“ behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-841">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="98bd2-842">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="98bd2-842">Az.Websites</span></span>
* <span data-ttu-id="98bd2-843">Problem behoben, aufgrund dessen einige SiteConfig-Eigenschaften von „Get-AzWebApp“ und „Set-AzWebApp“ nicht zurückgegeben wurden</span><span class="sxs-lookup"><span data-stu-id="98bd2-843">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="98bd2-844">Neuer Standortparameter zu „Get-AzDeletedWebApp“ und „Restore-AzDeletedWebApp“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-844">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="98bd2-845">Fehler beim Klonen von Web-App-Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-845">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="98bd2-846">2.4.0 – Juli 2019</span><span class="sxs-lookup"><span data-stu-id="98bd2-846">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="98bd2-847">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="98bd2-847">Az.Accounts</span></span>
* <span data-ttu-id="98bd2-848">Unterstützung für Profil-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-848">Add support for profile cmdlets</span></span>
* <span data-ttu-id="98bd2-849">Unterstützung für Umgebungen und Datenebenen in generierten Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-849">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="98bd2-850">Korrektur eines Fehlers, bei dem in einigen Fällen ein falscher Endpunkt für Datenebenen-Cmdlets in Windows PowerShell verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="98bd2-850">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="98bd2-851">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="98bd2-851">Az.Advisor</span></span>
* <span data-ttu-id="98bd2-852">Allgemein verfügbares Release von Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="98bd2-852">GA release of Az.Advisor</span></span>
* <span data-ttu-id="98bd2-853">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="98bd2-853">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="98bd2-854">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="98bd2-854">Az.ApiManagement</span></span>
* <span data-ttu-id="98bd2-855">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="98bd2-855">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="98bd2-856">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="98bd2-856">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="98bd2-857">Unterstützung für Abfragen von Abonnements nach Benutzer und Produkt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-857">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="98bd2-858">Unterstützung für Abfragen anhand des Umfangs hinzugefügt, „/“, „/apis“, „/apis/echo-api“</span><span class="sxs-lookup"><span data-stu-id="98bd2-858">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="98bd2-859">Behebung von Problem https://github.com/Azure/azure-powershell/issues/9307 und https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="98bd2-859">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="98bd2-860">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="98bd2-860">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="98bd2-861">Unterstützung für die Angabe von „ApiVersion“ und „ApiVersionSetId“ beim Importieren von APIs hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-861">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="98bd2-862">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="98bd2-862">Az.Automation</span></span>
* <span data-ttu-id="98bd2-863">Fehler beim Cmdlet „Set-AzAutomationConnectionFieldValue“ für die Verarbeitung des Zeichenfolgewerts behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-863">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="98bd2-864">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="98bd2-864">Az.Compute</span></span>
* <span data-ttu-id="98bd2-865">Parameter „HyperVGeneration“ zu New-AzImageConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-865">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="98bd2-866">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="98bd2-866">Az.DataFactory</span></span>
* <span data-ttu-id="98bd2-867">Aktualisierung der Ausgabe von ADF-Cmdlets für das Abrufen von Aktivitäts-, Pipeline- und Auslöserausführungen, um die Pipe „Select-Object“ zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="98bd2-867">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="98bd2-868">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="98bd2-868">Az.EventGrid</span></span>
* <span data-ttu-id="98bd2-869">Tippfehler in Dokumentation zu 'New-AzEventGridSubscription' behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-869">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="98bd2-870">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="98bd2-870">Az.IotHub</span></span>
* <span data-ttu-id="98bd2-871">Unterstützung für das erneute Generieren von Autorisierungsrichtlinienschlüsseln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-871">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="98bd2-872">Az.Network</span><span class="sxs-lookup"><span data-stu-id="98bd2-872">Az.Network</span></span>
* <span data-ttu-id="98bd2-873">„RoutingPreference“ zu öffentlichen IP-Tags hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-873">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="98bd2-874">Beispiele für Referenzdokumentation zu „Get-AzNetworkServiceTag“ verbessert</span><span class="sxs-lookup"><span data-stu-id="98bd2-874">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="98bd2-875">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="98bd2-875">Az.PolicyInsights</span></span>
* <span data-ttu-id="98bd2-876">Fehlerbehebung für Nullverweis in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="98bd2-876">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="98bd2-877">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="98bd2-877">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="98bd2-878">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="98bd2-878">Az.OperationalInsights</span></span>
* <span data-ttu-id="98bd2-879">Zurückgegebenes CustomLog-Datenquellenmodell in Get-AzOperationalInsightsDataSource korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-879">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="98bd2-880">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="98bd2-880">Az.RecoveryServices</span></span>
* <span data-ttu-id="98bd2-881">Fehlerbehebung für Befehl „get-policy“ IaaSVMs</span><span class="sxs-lookup"><span data-stu-id="98bd2-881">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="98bd2-882">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="98bd2-882">Az.Resources</span></span>
    - <span data-ttu-id="98bd2-883">Hilfetext für Parameter „-Top“ von „Get-AzPolicyState“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-883">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="98bd2-884">Clientseitige Unterstützung von Paginierung für „Get-AzPolicyAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-884">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="98bd2-885">Neue Parameter für „Set-AzPolicyAssignment“, „-PolicyParameters“ und „-PolicyParametersObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-885">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="98bd2-886">Einige Aktualisierungen von Dokumentationen und Beispielen für Policy-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="98bd2-886">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="98bd2-887">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="98bd2-887">Az.ServiceBus</span></span>
* <span data-ttu-id="98bd2-888">Korrektur für Problem Nr. 4938: „New-AzureRmServiceBusQueue“ gibt beim Festlegen von „MaxSizeInMegabytes“ „BadRequest“ zurück</span><span class="sxs-lookup"><span data-stu-id="98bd2-888">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="98bd2-889">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="98bd2-889">Az.Sql</span></span>
* <span data-ttu-id="98bd2-890">Instanzfailovergruppen-Cmdlets aus Vorschauversion in öffentliche Version hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-890">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="98bd2-891">Unterstützung von Azure SQL Server\Datenbanküberwachung mit neuen Cmdlets</span><span class="sxs-lookup"><span data-stu-id="98bd2-891">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="98bd2-892">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="98bd2-892">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="98bd2-893">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="98bd2-893">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="98bd2-894">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="98bd2-894">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="98bd2-895">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="98bd2-895">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="98bd2-896">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="98bd2-896">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="98bd2-897">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="98bd2-897">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="98bd2-898">E-Mail-Einschränkungen aus Einstellungen der Sicherheitsrisikobewertung entfernt</span><span class="sxs-lookup"><span data-stu-id="98bd2-898">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="98bd2-899">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="98bd2-899">Az.Storage</span></span>
* <span data-ttu-id="98bd2-900">Zwei Parameter („-IndexDocument“ und „-ErrorDocument404Path“) in folgendem Cmdlet von erforderlich in optional geändert:</span><span class="sxs-lookup"><span data-stu-id="98bd2-900">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="98bd2-901">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="98bd2-901">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="98bd2-902">Hilfe zu „Get-AzStorageBlobContent“ mit neuem Beispiel ergänzt</span><span class="sxs-lookup"><span data-stu-id="98bd2-902">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="98bd2-903">Anzeige von mehr Fehlerinformationen beim Fehlschlagen eines Cmdlets mit „StorageException“</span><span class="sxs-lookup"><span data-stu-id="98bd2-903">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="98bd2-904">Unterstützung für das Erstellen oder Aktualisieren von Speicherkonten mit Azure Files AAD-DS-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="98bd2-904">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="98bd2-905">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="98bd2-905">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="98bd2-906">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="98bd2-906">Set-AzStorageAccount</span></span>
* <span data-ttu-id="98bd2-907">Unterstützung für das Auflisten oder Schließen von Dateihandles einer Dateifreigabe, eines Dateiverzeichnisses oder einer Datei</span><span class="sxs-lookup"><span data-stu-id="98bd2-907">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="98bd2-908">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="98bd2-908">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="98bd2-909">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="98bd2-909">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="98bd2-910">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="98bd2-910">Az.StorageSync</span></span>
* <span data-ttu-id="98bd2-911">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="98bd2-911">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="98bd2-912">2.3.2 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="98bd2-912">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="98bd2-913">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="98bd2-913">Az.Accounts</span></span>
* <span data-ttu-id="98bd2-914">Fehler behoben, aufgrund dessen in manchen Fällen eine falsche URL für Funktionsaufrufe verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="98bd2-914">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="98bd2-915">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="98bd2-915">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="98bd2-916">Problem mit Aliasen zwischen AzureRM und Azure-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-916">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="98bd2-917">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="98bd2-917">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="98bd2-918">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="98bd2-918">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="98bd2-919">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="98bd2-919">Az.Compute</span></span>
* <span data-ttu-id="98bd2-920">Die einfachen Parametersätze „New-AzVm“ und „New-AzVmss“ akzeptieren jetzt den Parameter „ProximityPlacementGroup“.</span><span class="sxs-lookup"><span data-stu-id="98bd2-920">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="98bd2-921">Tippfehler in der Referenzdokumentation für „New-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-921">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="98bd2-922">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="98bd2-922">Az.Dns</span></span>
* <span data-ttu-id="98bd2-923">Tippfehler in den Hilfebeispielen zu „Set-AzDnsZone“ behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-923">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="98bd2-924">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="98bd2-924">Az.EventGrid</span></span>
* <span data-ttu-id="98bd2-925">Zur Verwendung der API-Version 2019-06-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-925">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="98bd2-926">Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="98bd2-926">New cmdlets:</span></span>
    - <span data-ttu-id="98bd2-927">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="98bd2-927">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="98bd2-928">Erstellt eine neue Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="98bd2-928">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="98bd2-929">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="98bd2-929">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="98bd2-930">Ruft die Details einer Event Grid-Domäne oder eine Liste aller Event Grid-Domänen im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="98bd2-930">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="98bd2-931">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="98bd2-931">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="98bd2-932">Entfernt eine Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="98bd2-932">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="98bd2-933">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="98bd2-933">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="98bd2-934">Generiert den freigegebenen Zugriffsschlüssel für eine Azure Event Grid-Domäne erneut.</span><span class="sxs-lookup"><span data-stu-id="98bd2-934">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="98bd2-935">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="98bd2-935">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="98bd2-936">Ruft die freigegebenen Zugriffsschlüssel ab, die zum Veröffentlichen von Ereignissen in einer Event Grid-Domäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="98bd2-936">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="98bd2-937">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="98bd2-937">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="98bd2-938">Erstellt ein neues Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="98bd2-938">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="98bd2-939">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="98bd2-939">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="98bd2-940">Ruft die Details eines Event Grid-Domänenthemas oder eine Liste aller Event Grid-Domänenthemen unter der jeweiligen Event Grid-Domäne im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="98bd2-940">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="98bd2-941">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="98bd2-941">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="98bd2-942">Entfernt ein vorhandenes Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="98bd2-942">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="98bd2-943">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="98bd2-943">Updated cmdlets:</span></span>
    - <span data-ttu-id="98bd2-944">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="98bd2-944">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="98bd2-945">Neue erforderliche Parameter zur Unterstützung des Pipings für die neue Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="98bd2-945">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="98bd2-946">Neue erforderliche Parameter zum Angeben des neuen Event Grid-Domänennamens und/oder Namens des Event Grid-Domänenthemas hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="98bd2-946">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="98bd2-947">Neue Parametersätze für Domänen und Domänenthemen hinzugefügt, um die Wiederverwendung vorhandener Parameter zuzulassen (‚z. B. „EndPointType“, „SubjectBeginsWith“ usw.)</span><span class="sxs-lookup"><span data-stu-id="98bd2-947">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="98bd2-948">Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="98bd2-948">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="98bd2-949">Ablaufdatum des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="98bd2-949">Event subscription expiration date,</span></span>
            - <span data-ttu-id="98bd2-950">Erweiterte Filterparameter</span><span class="sxs-lookup"><span data-stu-id="98bd2-950">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="98bd2-951">Neue Enumeration für „servicebusqueue“ als Ziel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-951">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="98bd2-952">Verwendung der Option „All“ in „-IncludedEventType“ gesperrt und wie folgt ersetzt</span><span class="sxs-lookup"><span data-stu-id="98bd2-952">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="98bd2-953">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="98bd2-953">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="98bd2-954">Neue optionale Parameter („Top“, „ODataQuery“ und „NextLink“) zur Unterstützung der Ergebnispaginierung und -filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-954">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="98bd2-955">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="98bd2-955">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="98bd2-956">Neue erforderliche Parameter zur Unterstützung des Pipings für die Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Entfernen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="98bd2-956">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="98bd2-957">Neue erforderliche Parameter zum Angeben des Event Grid-Domänennamens und/oder Event Grid-Domänenthemanamens hinzugefügt, um das Entfernen vorhandener Ereignisabonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="98bd2-957">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="98bd2-958">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="98bd2-958">Az.FrontDoor</span></span>
* <span data-ttu-id="98bd2-959">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="98bd2-959">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="98bd2-960">Unterstützung von Transformationen und neuen Wert für den Operator zum automatischen Vervollständigen (RegEx) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-960">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="98bd2-961">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="98bd2-961">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="98bd2-962">Neue Werte für automatisches Vervollständigen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-962">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="98bd2-963">Az.Network</span><span class="sxs-lookup"><span data-stu-id="98bd2-963">Az.Network</span></span>
* <span data-ttu-id="98bd2-964">Unterstützung für Virtual Network-Gatewayressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-964">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="98bd2-965">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="98bd2-965">New cmdlets</span></span>
        - <span data-ttu-id="98bd2-966">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="98bd2-966">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="98bd2-967">AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="98bd2-967">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="98bd2-968">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="98bd2-968">New cmdlets</span></span> 
        - <span data-ttu-id="98bd2-969">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="98bd2-969">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="98bd2-970">„PrivatePrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-970">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="98bd2-971">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="98bd2-971">New cmdlets</span></span> 
        - <span data-ttu-id="98bd2-972">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="98bd2-972">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="98bd2-973">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="98bd2-973">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="98bd2-974">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="98bd2-974">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="98bd2-975">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="98bd2-975">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="98bd2-976">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="98bd2-976">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="98bd2-977">„PrivateEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-977">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="98bd2-978">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="98bd2-978">New cmdlets</span></span>
        - <span data-ttu-id="98bd2-979">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="98bd2-979">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="98bd2-980">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="98bd2-980">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="98bd2-981">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="98bd2-981">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="98bd2-982">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="98bd2-982">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="98bd2-983">Folgende Befehle für das Feature aktualisiert: UseLocalAzureIpAddress-Flag für „VpnConnection“</span><span class="sxs-lookup"><span data-stu-id="98bd2-983">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="98bd2-984">„New-AzVpnConnection§ „ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="98bd2-984">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="98bd2-985">„Set-AzVpnConnection“ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="98bd2-985">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="98bd2-986">Schreibgeschütztes Feld „PeeredConnections“ beim ExpressRoute-Peering hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-986">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="98bd2-987">Schreibgeschütztes Feld „GlobalReachEnabled“ in ExpressRoute hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-987">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="98bd2-988">Breaking Change-Attribut hinzugefügt, um auf das veraltete Feld „AllowGlobalReach“ im ExpressRouteCircuit-Modell hinzuweisen</span><span class="sxs-lookup"><span data-stu-id="98bd2-988">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="98bd2-989">Fehler 8756 bei der Verwendung von „TargetListenerID“ mit AzApplicationGatewayRedirectConfiguration-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-989">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="98bd2-990">Fehler in „New-AzApplicationGatewayPathRuleConfig“ behoben, aufgrund dessen der Regelsatz für erneutes Generieren nicht festgelegt werden konnte</span><span class="sxs-lookup"><span data-stu-id="98bd2-990">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="98bd2-991">Fehler bei der Anzeige von „VirtualNetworkTaps“ in „NetworkInterfaceIpConfiguration“ behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-991">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="98bd2-992">Cortex-Get-Cmdlets zum Auflisten aller Komponenten korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-992">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="98bd2-993">Problem beim Erstellen des festen VirtualHub-Verweises für ExpressRouteGateways behoben (VpnGateway)</span><span class="sxs-lookup"><span data-stu-id="98bd2-993">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="98bd2-994">Unterstützung für Verfügbarkeitszonen in AzureFirewall und NatGateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-994">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="98bd2-995">Cmdlet „Get-AzNetworkServiceTag“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-995">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="98bd2-996">Unterstützung für mehrere öffentliche IP-Adressen für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-996">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="98bd2-997">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="98bd2-997">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="98bd2-998">Parameter „-PublicIpAddress“ hinzugefügt, der ein oder mehre öffentliche IP-Adressobjekte akzeptiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-998">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="98bd2-999">Parameter „- VirtualNetwork“ hinzugefügt, der ein Virtual Network-Objekt akzeptiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-999">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="98bd2-1000">Methoden „AddPublicIpAddress“ und „RemovePublicIpAddress“ für Firewallobjekte hinzugefügt (akzeptieren ein öffentliches IP-Adressobjekt als Eingabe)</span><span class="sxs-lookup"><span data-stu-id="98bd2-1000">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="98bd2-1001">Parameter „-PublicIpName“ und „-VirtualNetworkName“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1001">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="98bd2-1002">Folgende Befehle für das Feature aktualisiert: VpnClient-AAD-Authentifizierungsoptionen auf die Gatewayressource des virtuellen Netzwerkgateways festgelegt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1002">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="98bd2-1003">„New-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1003">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="98bd2-1004">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1004">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="98bd2-1005">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionaler Switch-Parameter „RemoveAadAuthentication“ zum Entfernen von VpnClient-AAD-Authentifizierungsoptionen aus dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1005">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="98bd2-1006">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="98bd2-1006">Az.OperationalInsights</span></span>
* <span data-ttu-id="98bd2-1007">Tarif **pergb2018** im Befehl „New-AzureRmOperationalInsightsWorkspace“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="98bd2-1007">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="98bd2-1008">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="98bd2-1008">Az.Resources</span></span>
* <span data-ttu-id="98bd2-1009">Unterstützung für zusätzliche Optionen zum Exportieren von Vorlagen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1009">Support for additional Template Export options</span></span>
    - <span data-ttu-id="98bd2-1010">Parameter „-SkipResourceNameParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1010">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="98bd2-1011">Parameter -SkipAllParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1011">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="98bd2-1012">Parameter „-Resource“ zu „Export-AzResourceGroup“ hinzugefügt, um das Filtern exportierter Ressourcen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="98bd2-1012">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="98bd2-1013">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="98bd2-1013">Az.ServiceFabric</span></span>
* <span data-ttu-id="98bd2-1014">Problem beim Hinzufügen des Zertifikats mit „ByExistingKeyVault“ behoben (Abruf des falschen Fingerabdrucks in manchen Fällen)</span><span class="sxs-lookup"><span data-stu-id="98bd2-1014">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="98bd2-1015">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="98bd2-1015">Az.Sql</span></span>
* <span data-ttu-id="98bd2-1016">Suffix des Advanced Threat Protection-Endpunkts korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1016">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="98bd2-1017">Durch Advanced Data Security ermöglichte Außerkraftsetzungen der Advanced Threat Protection-Richtlinie korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1017">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="98bd2-1018">Neue Cmdlets für „Management.Sql“ ermöglichen Kunden das Hinzufügen von TDE-Schlüsseln und Festlegen der TDE-Schutzvorrichtung für verwaltete Instanzen.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1018">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="98bd2-1019">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="98bd2-1019">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="98bd2-1020">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="98bd2-1020">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="98bd2-1021">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="98bd2-1021">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="98bd2-1022">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="98bd2-1022">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="98bd2-1023">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="98bd2-1023">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="98bd2-1024">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="98bd2-1024">Az.Storage</span></span>
* <span data-ttu-id="98bd2-1025">Unterstützung von „FileStorage“ und „SkuName Premium_ZRS“ beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="98bd2-1025">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="98bd2-1026">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="98bd2-1026">New-AzStorageAccount</span></span>
* <span data-ttu-id="98bd2-1027">Überarbeitete Beschreibung des Cmdlets für die Unveränderlichkeit von Blobs</span><span class="sxs-lookup"><span data-stu-id="98bd2-1027">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="98bd2-1028">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="98bd2-1028">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="98bd2-1029">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="98bd2-1029">Az.Websites</span></span>
* <span data-ttu-id="98bd2-1030">Optimiert „Get-AzWebAppCertificate“, um nach der Ressourcengruppe auf dem Server zu filtern (nicht auf dem Client)</span><span class="sxs-lookup"><span data-stu-id="98bd2-1030">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="98bd2-1031">Switch-Parameter „-UseDisasterRecovery“ für „Get-AzWebAppSnapshot“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1031">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="98bd2-1032">2.2.0 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="98bd2-1032">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="98bd2-1033">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="98bd2-1033">Az.Cdn</span></span>
* <span data-ttu-id="98bd2-1034">Es wurden Cmdlets aktualisiert, um das rulesEngine-Feature basierend auf der API-Version 2019-04-15 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1034">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="98bd2-1035">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="98bd2-1035">Az.Compute</span></span>
* <span data-ttu-id="98bd2-1036">Der Parameter `NoWait` wurde hinzugefügt, der den Vorgang startet und sofort zurückkehrt, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1036">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="98bd2-1037">Aktualisierte Cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="98bd2-1037">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="98bd2-1038">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="98bd2-1038">Az.EventHub</span></span>
* <span data-ttu-id="98bd2-1039">Fehlerbehebung für #9231 – Get-AzEventHubNamespace gibt keine Tags zurück</span><span class="sxs-lookup"><span data-stu-id="98bd2-1039">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="98bd2-1040">Fehlerbehebung für #9230 – Get-AzEventHubNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="98bd2-1040">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="98bd2-1041">Az.Network</span><span class="sxs-lookup"><span data-stu-id="98bd2-1041">Az.Network</span></span>
* <span data-ttu-id="98bd2-1042">ResourceId und InputObject wurden für NAT Gateway aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1042">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="98bd2-1043">Es wurde ein Alias für ResourceId und InputObjectr hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1043">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="98bd2-1044">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="98bd2-1044">Az.PolicyInsights</span></span>
* <span data-ttu-id="98bd2-1045">Fehlerbehebung für Nullverweis in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="98bd2-1045">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="98bd2-1046">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="98bd2-1046">Az.RecoveryServices</span></span>
* <span data-ttu-id="98bd2-1047">Minimale Aufbewahrung in Tagen für IaaSVM-Richtlinie wurde von 1 in 7 geändert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1047">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="98bd2-1048">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="98bd2-1048">Az.ServiceBus</span></span>
* <span data-ttu-id="98bd2-1049">Fehlerbehebung für #9182 – Get-AzServiceBusNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="98bd2-1049">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="98bd2-1050">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="98bd2-1050">Az.ServiceFabric</span></span>
* <span data-ttu-id="98bd2-1051">Tippfehler in Fehlermeldung für Update-AzServiceFabricReliability wurde behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-1051">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="98bd2-1052">Fehlendes Zeichen in Service Fabric-Befehlszeilen wurde behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-1052">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="98bd2-1053">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="98bd2-1053">Az.Sql</span></span>
* <span data-ttu-id="98bd2-1054">Der DnsZonePartner-Parameter für das Cmdlet New-AzureSqlInstance wurde hinzugefügt, um AutoDr für verwaltete Instanzen zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="98bd2-1054">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="98bd2-1055">Das Cmdlet Get-AzSqlDatabaseSecureConnectionPolicy wird eingestellt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1055">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="98bd2-1056">Cmdlets zum Schutz vor Bedrohungen werden in „Advanced Threat Protection“ (Erweiterter Schutz vor Bedrohungen) umbenannt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1056">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="98bd2-1057">New-AzSqlInstance – Die Parameter StorageSizeInGB und LicenseType sind jetzt optional</span><span class="sxs-lookup"><span data-stu-id="98bd2-1057">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="98bd2-1058">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="98bd2-1058">Az.Websites</span></span>
* <span data-ttu-id="98bd2-1059">Das Problem, bei dem die Verwendung von Set-AzWebApp und Set-AzWebAppSlot mit der -WebApp-Eigenschaft die Tags entfernt hat, wurde behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-1059">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="98bd2-1060">2.1.0 – Mai 2019</span><span class="sxs-lookup"><span data-stu-id="98bd2-1060">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="98bd2-1061">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="98bd2-1061">Az.ApiManagement</span></span>
* <span data-ttu-id="98bd2-1062">Es wurden neue Cmdlets zum Verwalten der Diagnose im globalen sowie im API-Bereich erstellt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1062">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="98bd2-1063">**Get-AzApiManagementDiagnostic**: Abrufen der Diagnose, die im globalen oder im API-Bereich konfiguriert wurde</span><span class="sxs-lookup"><span data-stu-id="98bd2-1063">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="98bd2-1064">**New-AzApiManagementDiagnostic**: Erstellen neuer Diagnosen im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="98bd2-1064">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="98bd2-1065">**New-AzApiManagementHttpMessageDiagnostic**: Erstellen einer Diagnoseeinstellung für die zu protokollierenden Kopfzeilen und für die Größe der Bytes für den Text</span><span class="sxs-lookup"><span data-stu-id="98bd2-1065">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="98bd2-1066">**New-AzApiManagementPipelineDiagnosticSetting**: Erstellen von Diagnoseeinstellungen für ein-/ausgehende HTTP-Nachrichten für das Gateway</span><span class="sxs-lookup"><span data-stu-id="98bd2-1066">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="98bd2-1067">**New-AzApiManagementSamplingSetting**: Erstellen der Einstellung „Sampling“ für die Anforderungen/Antworten für eine Diagnose</span><span class="sxs-lookup"><span data-stu-id="98bd2-1067">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="98bd2-1068">**Remove-AzApiManagementDiagnostic**: Entfernen einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="98bd2-1068">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="98bd2-1069">**Set-AzApiManagementDiagnostic**: Aktualisieren einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="98bd2-1069">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="98bd2-1070">Es wurden neue Cmdlets für die Cacheverwaltung im ApiManagement-Dienst erstellt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1070">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="98bd2-1071">**Get-AzApiManagementCache**: Abrufen der Details des durch den Bezeichner angegebenen Caches oder aller Caches</span><span class="sxs-lookup"><span data-stu-id="98bd2-1071">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="98bd2-1072">**New-AzApiManagementCache**: Erstellen eines neuen „standardmäßigen“ Caches oder eines Caches in einer bestimmten „Region“ von Azure</span><span class="sxs-lookup"><span data-stu-id="98bd2-1072">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="98bd2-1073">**Remove-AzApiManagementCache**: Entfernen eines Caches</span><span class="sxs-lookup"><span data-stu-id="98bd2-1073">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="98bd2-1074">**Update-AzApiManagementCache**: Aktualisieren eines Caches</span><span class="sxs-lookup"><span data-stu-id="98bd2-1074">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="98bd2-1075">Es wurden neue Cmdlets zur Verwaltung von API-Schemas erstellt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1075">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="98bd2-1076">**New-AzApiManagementSchema**: Erstellen eines neuen Schemas für eine API</span><span class="sxs-lookup"><span data-stu-id="98bd2-1076">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="98bd2-1077">**Get-AzApiManagementSchema**: Abrufen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="98bd2-1077">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="98bd2-1078">**Remove-AzApiManagementSchema**: Entfernen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="98bd2-1078">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="98bd2-1079">**Set-AzApiManagementSchema**: Aktualisieren des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="98bd2-1079">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="98bd2-1080">Es wurde ein neues Cmdlet zum Generieren eines Benutzertokens erstellt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1080">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="98bd2-1081">**New-AzApiManagementUserToken**: Generieren eines neuen Benutzertokens, das standardmäßig für acht Stunden gültig ist. Mit diesem Cmdlet kann das Token für den „GIT“-Benutzer generiert werden./</span><span class="sxs-lookup"><span data-stu-id="98bd2-1081">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="98bd2-1082">Es wurde ein neues Cmdlet zum Abrufen des Netzwerkstatus erstellt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1082">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="98bd2-1083">**Get-AzApiManagementNetworkStatus**: Abrufen der Netzwerkstatuskonnektivität von Ressourcen, von denen der API Management-Dienst abhängig ist</span><span class="sxs-lookup"><span data-stu-id="98bd2-1083">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="98bd2-1084">Dies ist hilfreich, wenn Sie den ApiManagement-Dienst in einem virtuellen Netzwerk bereitstellen und überprüfen, ob eine der Abhängigkeiten fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1084">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="98bd2-1085">Das Cmdlet **New-AzApiManagement** wurde zum Verwalten des ApiManagement-Diensts aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1085">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="98bd2-1086">Die Unterstützung für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1086">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="98bd2-1087">Die Unterstützung zum Aktivieren des Flags „EnableClientCertificate“ für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1087">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="98bd2-1088">Das neue Cmdlet **New-AzApiManagementSslSetting** ermöglicht die Konfiguration der „TLS/SSL“-Einstellung für „Back-End“ und „Front-End“</span><span class="sxs-lookup"><span data-stu-id="98bd2-1088">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="98bd2-1089">Dies kann auch dazu verwendet werden, um „Verschlüsselungen“ wie „3DES“ und „ServerProtokolle“ wie „Http2“ für das „Front-End“ eines ApiManagement-Diensts zu konfigurieren</span><span class="sxs-lookup"><span data-stu-id="98bd2-1089">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="98bd2-1090">Die Unterstützung für die Konfiguration des Hostnamens „DeveloperPortal“ wurde zum ApiManagement-Dienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1090">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="98bd2-1091">Die **Get-AzApiManagementSsoToken**-Cmdlets wurden aktualisiert, um das Objekt „PsApiManagement“ als Eingabe zu übernehmen</span><span class="sxs-lookup"><span data-stu-id="98bd2-1091">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="98bd2-1092">Das Cmdlet wurde aktualisiert, um Fehlermeldungen inline anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="98bd2-1092">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="98bd2-1093">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Fehlercode: ValidationError-Fehlermeldung: Mindestens ein Feld enthält ungültige Werte: Fehlerdetails: [Code=ValidationError, Message=Fehler in Element 'log-to-eventhub' in Zeile 3, Spalte 10: Protokollierungstool nicht gefunden, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="98bd2-1093">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="98bd2-1094">Cmdlet **Export-AzApiManagementApi** wurde für den Export von APIs im Format „OpenApi 3.0“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1094">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="98bd2-1095">Cmdlet **Import-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1095">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="98bd2-1096">Zum Importieren der API aus der „OpenApi 3.0“-Dokumentspezifikation</span><span class="sxs-lookup"><span data-stu-id="98bd2-1096">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="98bd2-1097">Zur Außerkraftsetzung der „PsApiManagementSchema“-Eigenschaft, die in einem beliebigen Dokument („Swagger“, „Wadl“, „Wsdl“, „OpenApi“) angegeben ist</span><span class="sxs-lookup"><span data-stu-id="98bd2-1097">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="98bd2-1098">Zur Außerkraftsetzung der „ServiceUrl“-Eigenschaft, die in einem beliebigen Dokument angegeben ist</span><span class="sxs-lookup"><span data-stu-id="98bd2-1098">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="98bd2-1099">Cmdlet **Get-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="98bd2-1099">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="98bd2-1100">Cmdlet **Set-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ und im Format mit XML-Escapezeichen mit „xml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="98bd2-1100">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="98bd2-1101">Cmdlet **New-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1101">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="98bd2-1102">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="98bd2-1102">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="98bd2-1103">Zum Erstellen einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="98bd2-1103">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="98bd2-1104">Zum Klonen einer API mithilfe von „SourceApiId“ und „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="98bd2-1104">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="98bd2-1105">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="98bd2-1105">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="98bd2-1106">Cmdlet **Set-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1106">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="98bd2-1107">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="98bd2-1107">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="98bd2-1108">Zum Aktualisieren einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="98bd2-1108">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="98bd2-1109">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="98bd2-1109">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="98bd2-1110">Cmdlet **New-AzApiManagementRevision** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1110">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="98bd2-1111">Zum Klonen (Kopiertags, Produkte, Vorgänge und Richtlinien) einer vorhandenen Version mithilfe von „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="98bd2-1111">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="98bd2-1112">Die neue Version übernimmt die „ApiId“ des übergeordneten Elements</span><span class="sxs-lookup"><span data-stu-id="98bd2-1112">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="98bd2-1113">Zum Bereitstellen einer „ApiRevisionDescription“</span><span class="sxs-lookup"><span data-stu-id="98bd2-1113">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="98bd2-1114">Zur Außerkraftsetzung der „ServiceUrl“ beim Klonen einer API</span><span class="sxs-lookup"><span data-stu-id="98bd2-1114">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="98bd2-1115">Cmdlet **New-AzApiManagementIdentityProvider** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1115">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="98bd2-1116">Zum Konfigurieren von „AAD“ oder „AADB2C“ mit einer „Authority“</span><span class="sxs-lookup"><span data-stu-id="98bd2-1116">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="98bd2-1117">Zum Einrichten von „SignupPolicy“, „SigninPolicy“, „ProfileEditingPolicy“ und „PasswordResetPolicy“</span><span class="sxs-lookup"><span data-stu-id="98bd2-1117">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="98bd2-1118">Cmdlet **New-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1118">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="98bd2-1119">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="98bd2-1119">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="98bd2-1120">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="98bd2-1120">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="98bd2-1121">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1121">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="98bd2-1122">Cmdlet **Set-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1122">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="98bd2-1123">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="98bd2-1123">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="98bd2-1124">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="98bd2-1124">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="98bd2-1125">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1125">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="98bd2-1126">Folgende Cmdlets wurden aktualisiert, um „ResourceId“ als Eingabe zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="98bd2-1126">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="98bd2-1127">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="98bd2-1127">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="98bd2-1128">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="98bd2-1128">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="98bd2-1129">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="98bd2-1129">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="98bd2-1130">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="98bd2-1130">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="98bd2-1131">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="98bd2-1131">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="98bd2-1132">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="98bd2-1132">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="98bd2-1133">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="98bd2-1133">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="98bd2-1134">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="98bd2-1134">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="98bd2-1135">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="98bd2-1135">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="98bd2-1136">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="98bd2-1136">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="98bd2-1137">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="98bd2-1137">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="98bd2-1138">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="98bd2-1138">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="98bd2-1139">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="98bd2-1139">Az.Automation</span></span>
* <span data-ttu-id="98bd2-1140">Get-AzAutomationJobOutputRecord wurde aktualisiert, um JSON- und Textdatensatzwerte zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1140">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="98bd2-1141">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="98bd2-1141">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="98bd2-1142">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="98bd2-1142">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="98bd2-1143">Das Verhalten von Start-AzAutomationDscCompilationJob wurde geändert, um den Auftrag einfach zu starten, anstatt auf dessen Abschluss zu warten</span><span class="sxs-lookup"><span data-stu-id="98bd2-1143">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="98bd2-1144">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="98bd2-1144">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="98bd2-1145">Fehlerbehebung für Get-AzAutomationDscNode, wenn die Verwendung von „-Name“ alle Knoten zurückgibt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1145">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="98bd2-1146">Jetzt wird nur der übereinstimmende Knoten zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="98bd2-1146">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="98bd2-1147">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="98bd2-1147">Az.Compute</span></span>
* <span data-ttu-id="98bd2-1148">Parameter „ProtectFromScaleIn“ und „ProtectFromScaleSetAction“ wurden zum Cmdlet „Update-AzVmssVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1148">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="98bd2-1149">Der jetzt festgelegte wimple-Parameter „New-AzVM“ verwendet standardmäßig einen verfügbaren Standort, wenn „East US“ (USA, Osten) nicht unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="98bd2-1149">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="98bd2-1150">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="98bd2-1150">Az.DataLakeStore</span></span>
* <span data-ttu-id="98bd2-1151">Das ADLS-SDK wurde aktualisiert, um „HttpClient“ zu verwenden und Datenebenentests wurden mit dem Azure-Framework integriert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1151">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="98bd2-1152">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="98bd2-1152">Az.Monitor</span></span>
* <span data-ttu-id="98bd2-1153">Fehlerbehebung bei falschen Parameternamen in Hilfebeispielen</span><span class="sxs-lookup"><span data-stu-id="98bd2-1153">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="98bd2-1154">Az.Network</span><span class="sxs-lookup"><span data-stu-id="98bd2-1154">Az.Network</span></span>
* <span data-ttu-id="98bd2-1155">DisableBgpRoutePropagation-Flag wurde zur Ausgabe der effektiven Routentabelle hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1155">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="98bd2-1156">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="98bd2-1156">Updated cmdlet:</span></span>
        - <span data-ttu-id="98bd2-1157">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="98bd2-1157">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="98bd2-1158">Fehlerbehebung von doppeltem Bindestrich in Dokumentation von New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="98bd2-1158">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="98bd2-1159">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="98bd2-1159">Az.Resources</span></span>
* <span data-ttu-id="98bd2-1160">Neues Cmdlet „Get-AzureRmDenyAssignment“ zum Abrufen von Ablehnungszuweisungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1160">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="98bd2-1161">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="98bd2-1161">Az.Sql</span></span>
* <span data-ttu-id="98bd2-1162">„Advanced Threat Protection“-Cmdlets in „Advanced Data Security“ umbenennen und Sicherheitsrisikobewertung standardmäßig aktivieren</span><span class="sxs-lookup"><span data-stu-id="98bd2-1162">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="98bd2-1163">2.0.0: Mai 2019</span><span class="sxs-lookup"><span data-stu-id="98bd2-1163">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="98bd2-1164">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="98bd2-1164">Az.Accounts</span></span>
* <span data-ttu-id="98bd2-1165">Authentifizierungsbibliothek aktualisiert, um ADFS-Probleme mit der Authentifizierung per Benutzername/Kennwort zu beheben</span><span class="sxs-lookup"><span data-stu-id="98bd2-1165">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="98bd2-1166">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="98bd2-1166">Az.CognitiveServices</span></span>
* <span data-ttu-id="98bd2-1167">Ausschließliche Anzeige des Bing-Haftungsausschlusses für Bing-Suchdienste</span><span class="sxs-lookup"><span data-stu-id="98bd2-1167">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="98bd2-1168">Fehler behoben, der zu einem Fehler bei der Kontoerstellung führte</span><span class="sxs-lookup"><span data-stu-id="98bd2-1168">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="98bd2-1169">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="98bd2-1169">Az.Compute</span></span>
* <span data-ttu-id="98bd2-1170">Feature für die Näherungsplatzierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="98bd2-1170">Proximity placement group feature.</span></span>
    - <span data-ttu-id="98bd2-1171">Die folgenden neuen Cmdlets wurden hinzugefügt:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="98bd2-1171">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="98bd2-1172">Der neue Parameter „ProximityPlacementGroupId“ wurde zu den folgenden Cmdlets hinzugefügt:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="98bd2-1172">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="98bd2-1173">Der Parameter „StorageAccountType“ wurde zu „New-AzGalleryImageVersion“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1173">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="98bd2-1174">„TargetRegion“ von „New-AzGalleryImageVersion“ kann „StorageAccountType“ enthalten.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1174">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="98bd2-1175">Switch-Parameter „SkipShutdown“ wurde zu „Stop-AzVM“ und „Stop-AzVmss“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1175">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="98bd2-1176">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="98bd2-1176">Breaking changes</span></span>
    - <span data-ttu-id="98bd2-1177">„Set-AzVMBootDiagnostics“ in „Set-AzVMBootDiagnostic“ geändert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1177">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="98bd2-1178">„Export-AzLogAnalyticThrottledRequests“ in „Export-AzLogAnalyticThrottledRequests“ geändert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1178">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="98bd2-1179">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="98bd2-1179">Az.DeploymentManager</span></span>
* <span data-ttu-id="98bd2-1180">Erste allgemein verfügbare Version der Azure-Bereitstellungs-Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="98bd2-1180">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="98bd2-1181">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="98bd2-1181">Az.Dns</span></span>
* <span data-ttu-id="98bd2-1182">Automatische Delegierung des DNS-Namenservers</span><span class="sxs-lookup"><span data-stu-id="98bd2-1182">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="98bd2-1183">Das Cmdlet zum Erstellen einer DNS-Zone akzeptiert den übergeordneten Zonennamen als zusätzlichen optionalen Parameter.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1183">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="98bd2-1184">NS-Einträge in der übergeordneten Zone für neu erstellte untergeordnete Zone hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1184">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="98bd2-1185">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="98bd2-1185">Az.FrontDoor</span></span>
* <span data-ttu-id="98bd2-1186">Erste allgemein verfügbare Version der Azure Frontdoor-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="98bd2-1186">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="98bd2-1187">WAF-Cmdlets so umbenannt, dass sie „Waf“ enthalten</span><span class="sxs-lookup"><span data-stu-id="98bd2-1187">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="98bd2-1188">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="98bd2-1188">Az.HDInsight</span></span>
* <span data-ttu-id="98bd2-1189">Zwei Cmdlets entfernt:</span><span class="sxs-lookup"><span data-stu-id="98bd2-1189">Removed two cmdlets:</span></span>
    - <span data-ttu-id="98bd2-1190">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="98bd2-1190">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="98bd2-1191">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="98bd2-1191">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="98bd2-1192">Neues Cmdlet „Set-AzHDInsightGatewayCredential“ hinzugefügt, um „Grant-AzHDInsightHttpServicesAccess“ zu ersetzen</span><span class="sxs-lookup"><span data-stu-id="98bd2-1192">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="98bd2-1193">Cmdlet „Get-AzHDInsightJobOutput“ aktualisiert, um zwischen Leserrolle und HDInsight-Bedienerrolle zu unterscheiden:</span><span class="sxs-lookup"><span data-stu-id="98bd2-1193">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="98bd2-1194">Benutzer mit der Rolle „Leser“ müssen den Parameter „DefaultStorageAccountKey“ explizit angeben, andernfalls treten Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1194">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="98bd2-1195">Benutzer mit der Rolle des HDInsight-Bedieners sind nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1195">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="98bd2-1196">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="98bd2-1196">Az.Monitor</span></span>
* <span data-ttu-id="98bd2-1197">Neue Cmdlets für SQR-API (Scheduled Query Rule, geplante Abfrageregel)</span><span class="sxs-lookup"><span data-stu-id="98bd2-1197">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="98bd2-1198">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="98bd2-1198">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="98bd2-1199">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="98bd2-1199">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="98bd2-1200">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="98bd2-1200">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="98bd2-1201">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="98bd2-1201">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="98bd2-1202">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="98bd2-1202">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="98bd2-1203">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="98bd2-1203">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="98bd2-1204">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="98bd2-1204">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="98bd2-1205">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="98bd2-1205">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="98bd2-1206">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="98bd2-1206">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="98bd2-1207">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="98bd2-1207">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="98bd2-1208">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="98bd2-1208">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="98bd2-1209">[Weitere Informationen](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) zur SQR-API</span><span class="sxs-lookup"><span data-stu-id="98bd2-1209">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="98bd2-1210">„Az.Monitor.md“ aktualisiert, um Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch) einzuschließen</span><span class="sxs-lookup"><span data-stu-id="98bd2-1210">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="98bd2-1211">Az.Network</span><span class="sxs-lookup"><span data-stu-id="98bd2-1211">Az.Network</span></span>
* <span data-ttu-id="98bd2-1212">Unterstützung für NAT-Gatewayressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1212">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="98bd2-1213">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="98bd2-1213">New cmdlets</span></span>
        - <span data-ttu-id="98bd2-1214">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="98bd2-1214">New-AzNatGateway</span></span>
        - <span data-ttu-id="98bd2-1215">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="98bd2-1215">Get-AzNatGateway</span></span>
        - <span data-ttu-id="98bd2-1216">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="98bd2-1216">Set-AzNatGateway</span></span>
        - <span data-ttu-id="98bd2-1217">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="98bd2-1217">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="98bd2-1218">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="98bd2-1218">Updated cmdlets</span></span>
        - <span data-ttu-id="98bd2-1219">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="98bd2-1219">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="98bd2-1220">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="98bd2-1220">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="98bd2-1221">Folgende Befehle für das Feature aktualisiert: Benutzerdefinierte Routen für Brooklyn-Gateway festgelegt/entfernt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1221">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="98bd2-1222">„New-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1222">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="98bd2-1223">„Set-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1223">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="98bd2-1224">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="98bd2-1224">Az.PolicyInsights</span></span>
* <span data-ttu-id="98bd2-1225">Unterstützung für die Abfrage von Richtlinienauswertungsdetails</span><span class="sxs-lookup"><span data-stu-id="98bd2-1225">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="98bd2-1226">Parameter „-Expand“ zu „Get-AzPolicyState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1226">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="98bd2-1227">Unterstützung für „-Expand PolicyEvaluationDetails“</span><span class="sxs-lookup"><span data-stu-id="98bd2-1227">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="98bd2-1228">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="98bd2-1228">Az.RecoveryServices</span></span>
* <span data-ttu-id="98bd2-1229">Unterstützung für abonnementübergreifende Azure-zu-Azure-Sitewiederherstellung</span><span class="sxs-lookup"><span data-stu-id="98bd2-1229">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="98bd2-1230">Markierung anstehender wichtiger Änderungen für Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="98bd2-1230">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="98bd2-1231">Fehlerbehebung für Azure Site Recovery-Wiederherstellungsplan und -Aktionsplan</span><span class="sxs-lookup"><span data-stu-id="98bd2-1231">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="98bd2-1232">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Netzwerkzuordnung für Azure zu Azure</span><span class="sxs-lookup"><span data-stu-id="98bd2-1232">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="98bd2-1233">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Schutzrichtung für Azure zu Azure für verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="98bd2-1233">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="98bd2-1234">Weitere kleinere Korrekturen</span><span class="sxs-lookup"><span data-stu-id="98bd2-1234">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="98bd2-1235">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="98bd2-1235">Az.Relay</span></span>
* <span data-ttu-id="98bd2-1236">Korrektur von Tippfehlern in Kundennachrichten</span><span class="sxs-lookup"><span data-stu-id="98bd2-1236">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="98bd2-1237">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="98bd2-1237">Az.ServiceBus</span></span>
* <span data-ttu-id="98bd2-1238">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1238">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="98bd2-1239">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="98bd2-1239">Az.Storage</span></span>
* <span data-ttu-id="98bd2-1240">Upgrade auf Speicherclientbibliothek 10.0.1 (Namespace aller Objekte von diesem SDK von „Microsoft.WindowsAzure.Storage. *“ in „Microsoft.Azure.Storage.* “ geändert)</span><span class="sxs-lookup"><span data-stu-id="98bd2-1240">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="98bd2-1241">Upgrade auf Microsoft.Azure.Management.Storage 11.0.0, um die neue API-Version 2019-04-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="98bd2-1241">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="98bd2-1242">Art des Standardspeicherkontos bei der Speicherkontoerstellung von „Storage“ in „StorageV2“ geändert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1242">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="98bd2-1243">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="98bd2-1243">New-AzStorageAccount</span></span>
* <span data-ttu-id="98bd2-1244">Vom Speicherkonto-Cmdlet ausgegebener SKU-Name (Sku.Name) durch Hinzufügen eines Unterstrichs an SKU-Eingabename angepasst (Beispiel: „StandardLRS“ > „Standard_LRS“).</span><span class="sxs-lookup"><span data-stu-id="98bd2-1244">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="98bd2-1245">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="98bd2-1245">New-AzStorageAccount</span></span>
    - <span data-ttu-id="98bd2-1246">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="98bd2-1246">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="98bd2-1247">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="98bd2-1247">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="98bd2-1248">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="98bd2-1248">Az.Websites</span></span>
* <span data-ttu-id="98bd2-1249">Die Eigenschaft „Kind“ wird nun für PSSite-Objekte festgelegt, die von „Get-AzWebApp“ zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1249">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="98bd2-1250">„Get-AzWebApp\*Metrics“ und „Get-AzAppServicePlanMetrics“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1250">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="98bd2-1251">1.8.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="98bd2-1251">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="98bd2-1252">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="98bd2-1252">Highlights since the last major release</span></span>
* <span data-ttu-id="98bd2-1253">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="98bd2-1253">General availability of `Az` module</span></span>
* <span data-ttu-id="98bd2-1254">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1254">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="98bd2-1255">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1255">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="98bd2-1256">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1256">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="98bd2-1257">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1257">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="98bd2-1258">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1258">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="98bd2-1259">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="98bd2-1259">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="98bd2-1260">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="98bd2-1260">Az.Accounts</span></span>
* <span data-ttu-id="98bd2-1261">„Uninstall-AzureRm“ aktualisiert, um Module unter Mac ordnungsgemäß zu löschen</span><span class="sxs-lookup"><span data-stu-id="98bd2-1261">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="98bd2-1262">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="98bd2-1262">Az.Batch</span></span>
* <span data-ttu-id="98bd2-1263">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1263">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="98bd2-1264">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="98bd2-1264">Az.Cdn</span></span>
* <span data-ttu-id="98bd2-1265">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1265">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="98bd2-1266">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="98bd2-1266">Az.CognitiveServices</span></span>
* <span data-ttu-id="98bd2-1267">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1267">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="98bd2-1268">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="98bd2-1268">Az.Compute</span></span>
* <span data-ttu-id="98bd2-1269">Problem mit der AEM-Installation behoben, wenn die Ressourcen-IDs von Datenträgern Ressourcengruppen in Kleinbuchstaben enthielten</span><span class="sxs-lookup"><span data-stu-id="98bd2-1269">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="98bd2-1270">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1270">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="98bd2-1271">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1271">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="98bd2-1272">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="98bd2-1272">Az.DataFactory</span></span>
* <span data-ttu-id="98bd2-1273">„SsisProperties“ hinzugefügt, falls „NodeCount“ für verwaltete Integration Runtime nicht NULL ist</span><span class="sxs-lookup"><span data-stu-id="98bd2-1273">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="98bd2-1274">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="98bd2-1274">Az.DataLakeStore</span></span>
* <span data-ttu-id="98bd2-1275">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1275">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="98bd2-1276">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="98bd2-1276">Az.EventGrid</span></span>
* <span data-ttu-id="98bd2-1277">Hilfetext für Endpunkt aktualisiert, um anzugeben, dass Ressourcen erstellt werden müssen, bevor die Cmdlets zum Erstellen/Aktualisieren von Ereignisabonnements verwendet werden</span><span class="sxs-lookup"><span data-stu-id="98bd2-1277">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="98bd2-1278">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="98bd2-1278">Az.EventHub</span></span>
* <span data-ttu-id="98bd2-1279">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1279">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="98bd2-1280">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="98bd2-1280">Az.HDInsight</span></span>
* <span data-ttu-id="98bd2-1281">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1281">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="98bd2-1282">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="98bd2-1282">Az.IotHub</span></span>
* <span data-ttu-id="98bd2-1283">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1283">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="98bd2-1284">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="98bd2-1284">Az.KeyVault</span></span>
* <span data-ttu-id="98bd2-1285">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1285">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="98bd2-1286">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1286">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="98bd2-1287">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="98bd2-1287">Az.MachineLearning</span></span>
* <span data-ttu-id="98bd2-1288">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1288">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="98bd2-1289">Az.Media</span><span class="sxs-lookup"><span data-stu-id="98bd2-1289">Az.Media</span></span>
* <span data-ttu-id="98bd2-1290">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1290">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="98bd2-1291">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="98bd2-1291">Az.Monitor</span></span>
  * <span data-ttu-id="98bd2-1292">Neue Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch)</span><span class="sxs-lookup"><span data-stu-id="98bd2-1292">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="98bd2-1293">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="98bd2-1293">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="98bd2-1294">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="98bd2-1294">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="98bd2-1295">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="98bd2-1295">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="98bd2-1296">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="98bd2-1296">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="98bd2-1297">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="98bd2-1297">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="98bd2-1298">Monitor SDK auf Version 0.22.0-preview aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1298">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="98bd2-1299">Az.Network</span><span class="sxs-lookup"><span data-stu-id="98bd2-1299">Az.Network</span></span>
* <span data-ttu-id="98bd2-1300">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1300">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="98bd2-1301">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1301">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="98bd2-1302">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="98bd2-1302">Az.NotificationHubs</span></span>
* <span data-ttu-id="98bd2-1303">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1303">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="98bd2-1304">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="98bd2-1304">Az.OperationalInsights</span></span>
* <span data-ttu-id="98bd2-1305">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1305">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="98bd2-1306">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="98bd2-1306">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="98bd2-1307">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1307">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="98bd2-1308">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="98bd2-1308">Az.RecoveryServices</span></span>
* <span data-ttu-id="98bd2-1309">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1309">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="98bd2-1310">Tabellenformat für SQL auf Azure-VM aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1310">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="98bd2-1311">Alternative Methode zum Abrufen des Speicherorts in „AzureFileShare“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1311">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="98bd2-1312">„ScheduleRunDays“ in SchedulePolicy-Objekt gemäß Zeitzone aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1312">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="98bd2-1313">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="98bd2-1313">Az.RedisCache</span></span>
* <span data-ttu-id="98bd2-1314">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1314">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="98bd2-1315">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="98bd2-1315">Az.Resources</span></span>
* <span data-ttu-id="98bd2-1316">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1316">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="98bd2-1317">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="98bd2-1317">Az.Sql</span></span>
* <span data-ttu-id="98bd2-1318">Abhängigkeit vom Monitor SDK durch allgemeinen Code ersetzt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1318">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="98bd2-1319">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1319">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="98bd2-1320">Verbesserter Prozess für Klassifizierung mehrerer Spalten</span><span class="sxs-lookup"><span data-stu-id="98bd2-1320">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="98bd2-1321">SKU-Eigenschaften (SKU-Name, Familie, Kapazität) in Antwort von „Get-AzSqlServerServiceObjective“ aufgenommen und standardmäßig als Tabelle formatiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1321">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="98bd2-1322">Möglichkeit zum Ausführen von „Get-AzSqlServerServiceObjective“ nach Standort, ohne dass bereits ein Server in der Region vorhanden sein muss</span><span class="sxs-lookup"><span data-stu-id="98bd2-1322">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="98bd2-1323">Unterstützung für Zeitzonenparameter bei der Erstellung einer verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="98bd2-1323">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="98bd2-1324">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1324">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="98bd2-1325">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="98bd2-1325">Az.Websites</span></span>
* <span data-ttu-id="98bd2-1326">„Set-AzWebApp“ und „Set-AzWebAppSlot“ korrigiert, sodass die Tags bei der Ausführung nicht entfernt werden</span><span class="sxs-lookup"><span data-stu-id="98bd2-1326">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="98bd2-1327">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1327">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="98bd2-1328">WebSites SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1328">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="98bd2-1329">AdminSiteName-Eigenschaft aus „PSAppServicePlan“ entfernt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1329">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="98bd2-1330">1.7.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="98bd2-1330">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="98bd2-1331">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="98bd2-1331">Highlights since the last major release</span></span>
* <span data-ttu-id="98bd2-1332">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="98bd2-1332">General availability of `Az` module</span></span>
* <span data-ttu-id="98bd2-1333">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1333">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="98bd2-1334">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1334">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="98bd2-1335">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1335">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="98bd2-1336">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1336">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="98bd2-1337">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1337">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="98bd2-1338">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="98bd2-1338">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="98bd2-1339">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="98bd2-1339">Az.Accounts</span></span>
* <span data-ttu-id="98bd2-1340">„Add-AzEnvironment“ und „Set-AzEnvironment“ aktualisiert, um den Parameter „AzureAnalysisServicesEndpointResourceId“ zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="98bd2-1340">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="98bd2-1341">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="98bd2-1341">Az.AnalysisServices</span></span>
* <span data-ttu-id="98bd2-1342">ServiceClient wird in Cmdlets für die Datenebene verwendet, und die ursprüngliche Authentifizierungslogik wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1342">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="98bd2-1343">„Add-AzureASAccount“ wird als Wrapper von „Connect-AzAccount“ festgelegt, um einen Breaking Change zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1343">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="98bd2-1344">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="98bd2-1344">Az.Automation</span></span>
* <span data-ttu-id="98bd2-1345">Fehler des Cmdlets „Fixed New-AzAutomationSoftwareUpdateConfiguration“ für Einschlüsse behoben.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1345">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="98bd2-1346">Die Parameter „IncludedKbNumber“ und „IncludedPackageNameMask“ sollten nun funktionieren.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1346">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="98bd2-1347">Fehlerbehebung für eine dynamische Gruppe der Azure Automation-Updateverwaltung</span><span class="sxs-lookup"><span data-stu-id="98bd2-1347">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="98bd2-1348">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="98bd2-1348">Az.Compute</span></span>
* <span data-ttu-id="98bd2-1349">Parameter „HyperVGeneration“ zu „New-AzDiskConfig“ und „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1349">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="98bd2-1350">Zulassen der VM-Erstellung mit einem Katalogimage aus anderen Mandanten</span><span class="sxs-lookup"><span data-stu-id="98bd2-1350">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="98bd2-1351">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="98bd2-1351">Az.ContainerInstance</span></span>
* <span data-ttu-id="98bd2-1352">Problem im Parameter „-Command“ von „New-AzContainerGroup“ behoben, das dazu führte, dass ein nachgestelltes leeres Argument hinzugefügt wurde</span><span class="sxs-lookup"><span data-stu-id="98bd2-1352">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="98bd2-1353">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="98bd2-1353">Az.DataFactory</span></span>
* <span data-ttu-id="98bd2-1354">Version des ADF .NET SDK auf 3.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1354">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="98bd2-1355">Cmdlet „Set-AzDataFactoryV2“ mit zusätzlichen Parametern für RepoConfiguration-Einstellungen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1355">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="98bd2-1356">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="98bd2-1356">Az.Resources</span></span>
* <span data-ttu-id="98bd2-1357">Verarbeitung von Anbietern für „Get-AzResource“ bei der Angabe der Parameter „-ResourceId“ oder „-ResourceGroupName“, „-Name“ und „-ResourceType“ verbessert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1357">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="98bd2-1358">Fehlerbehandlung für „Test-AzDeployment“ und „Test-AzResourceGroupDeployment“ verbessert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1358">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="98bd2-1359">Behandlung von außerhalb der Bereitstellungsüberprüfung aufgetretenen Fehlern und stattdessen Aufnahme in die Ausgabe des Befehls</span><span class="sxs-lookup"><span data-stu-id="98bd2-1359">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="98bd2-1360">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="98bd2-1360">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="98bd2-1361">Switch-Parameter „-IgnoreDynamicParameters“ zu Bereitstellungs-Cmdlets hinzugefügt, um Aufforderung in Skript- und Auftragsszenarien zu überspringen</span><span class="sxs-lookup"><span data-stu-id="98bd2-1361">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="98bd2-1362">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="98bd2-1362">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="98bd2-1363">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="98bd2-1363">Az.Sql</span></span>
* <span data-ttu-id="98bd2-1364">Unterstützung für Klassifizierung von Datenbankdaten</span><span class="sxs-lookup"><span data-stu-id="98bd2-1364">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="98bd2-1365">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="98bd2-1365">Az.Storage</span></span>
* <span data-ttu-id="98bd2-1366">Melden eines ausführlichen Fehlers beim Erstellen des Storage-Kontexts mit dem Parameter „-UseConnectedAccount“, aber ohne Azure-Anmeldekonto</span><span class="sxs-lookup"><span data-stu-id="98bd2-1366">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="98bd2-1367">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="98bd2-1367">New-AzStorageContext</span></span>
* <span data-ttu-id="98bd2-1368">Unterstützung für das Verwalten von Blobdiensteigenschaften eines bestimmten Storage-Kontos mit einer API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="98bd2-1368">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="98bd2-1369">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="98bd2-1369">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="98bd2-1370">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="98bd2-1370">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="98bd2-1371">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="98bd2-1371">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="98bd2-1372">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="98bd2-1372">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="98bd2-1373">Unterstützung von „-AsJob“ für Cmdlets für den Upload und Download von Blobs und Dateien</span><span class="sxs-lookup"><span data-stu-id="98bd2-1373">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="98bd2-1374">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="98bd2-1374">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="98bd2-1375">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="98bd2-1375">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="98bd2-1376">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="98bd2-1376">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="98bd2-1377">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="98bd2-1377">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="98bd2-1378">1.6.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="98bd2-1378">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="98bd2-1379">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="98bd2-1379">Highlights since the last major release</span></span>
* <span data-ttu-id="98bd2-1380">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="98bd2-1380">General availability of `Az` module</span></span>
* <span data-ttu-id="98bd2-1381">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1381">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="98bd2-1382">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1382">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="98bd2-1383">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1383">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="98bd2-1384">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1384">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="98bd2-1385">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1385">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="98bd2-1386">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="98bd2-1386">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="98bd2-1387">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="98bd2-1387">Az.Automation</span></span>
* <span data-ttu-id="98bd2-1388">Änderung an der Azure Automation-Updateverwaltung, um die folgenden neuen Features zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="98bd2-1388">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="98bd2-1389">Dynamische Gruppierung</span><span class="sxs-lookup"><span data-stu-id="98bd2-1389">Dynamic grouping</span></span>
    * <span data-ttu-id="98bd2-1390">Pre-/Post-Skripts</span><span class="sxs-lookup"><span data-stu-id="98bd2-1390">Pre-Post script</span></span>
    * <span data-ttu-id="98bd2-1391">Neustarteinstellung</span><span class="sxs-lookup"><span data-stu-id="98bd2-1391">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="98bd2-1392">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="98bd2-1392">Az.Compute</span></span>
* <span data-ttu-id="98bd2-1393">Problem mit der Pfadauflösung in „Get-AzVmBootDiagnosticsData“ behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-1393">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="98bd2-1394">Computeclientbibliothek auf 25.0.0. aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1394">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="98bd2-1395">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="98bd2-1395">Az.KeyVault</span></span>
* <span data-ttu-id="98bd2-1396">Unterstützung für Platzhalterzeichen zu KeyVault-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1396">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="98bd2-1397">Az.Network</span><span class="sxs-lookup"><span data-stu-id="98bd2-1397">Az.Network</span></span>
* <span data-ttu-id="98bd2-1398">Threat Intelligence-Unterstützung für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1398">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="98bd2-1399">Ressource der obersten Ebene für Application Gateway-Firewallrichtlinie und benutzerdefinierte Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1399">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="98bd2-1400">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="98bd2-1400">Az.RecoveryServices</span></span>
* <span data-ttu-id="98bd2-1401">SnapshotRetentionInDays in Azure-VM-Richtlinie hinzugefügt, um sofortigen Wiederherstellungspunkt zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="98bd2-1401">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="98bd2-1402">Pipe-Unterstützung für das Aufheben der Registrierung eines Containers hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1402">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="98bd2-1403">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="98bd2-1403">Az.Resources</span></span>
* <span data-ttu-id="98bd2-1404">Unterstützung für Platzhalterzeichen für Get-AzResource und Get-AzResourceGroup aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1404">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="98bd2-1405">Anmeldeinformationen aktualisiert, die beim Senden generischer Aufrufe an ARM verwendet werden</span><span class="sxs-lookup"><span data-stu-id="98bd2-1405">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="98bd2-1406">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="98bd2-1406">Az.Sql</span></span>
* <span data-ttu-id="98bd2-1407">Der Cmdlet-Parameter der Bedrohungserkennung (ExcludeDetectionType) wurde von „DetectionType“ in „string[]“ geändert, um ihn zukunftssicher zu machen, wenn neue DetectionTypes-Elemente hinzugefügt werden, und um AutoVervollständigen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1407">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="98bd2-1408">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="98bd2-1408">Az.Storage</span></span>
* <span data-ttu-id="98bd2-1409">Unterstützung von Get-/Set-/Remove-Verwaltungsrichtlinien für Speicherkonto hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1409">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="98bd2-1410">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="98bd2-1410">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="98bd2-1411">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="98bd2-1411">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="98bd2-1412">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="98bd2-1412">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="98bd2-1413">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="98bd2-1413">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="98bd2-1414">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="98bd2-1414">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="98bd2-1415">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="98bd2-1415">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="98bd2-1416">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="98bd2-1416">Az.Websites</span></span>
* <span data-ttu-id="98bd2-1417">ARM-Vorlagenfehler behoben, der zu einem Problem beim Klonen aller Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ führte</span><span class="sxs-lookup"><span data-stu-id="98bd2-1417">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="98bd2-1418">1.5.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="98bd2-1418">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="98bd2-1419">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="98bd2-1419">Az.Accounts</span></span>
* <span data-ttu-id="98bd2-1420">Der Befehl „Register-AzModule“ wurde hinzugefügt, um von AutoRest generierte Cmdlets zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1420">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="98bd2-1421">Beispiele für „Connect-AzAccount“ wurden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1421">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="98bd2-1422">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="98bd2-1422">Az.Automation</span></span>
* <span data-ttu-id="98bd2-1423">Problem behoben, das beim Abrufen bestimmter monatlicher Zeitpläne in verschiedenen Azure Automation-Cmdlets auftrat</span><span class="sxs-lookup"><span data-stu-id="98bd2-1423">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="98bd2-1424">„Get-AzAutomationDscNode“ wurde korrigiert, da nur die 20 obersten Knoten zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1424">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="98bd2-1425">Jetzt werden alle Knoten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1425">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="98bd2-1426">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="98bd2-1426">Az.Cdn</span></span>
* <span data-ttu-id="98bd2-1427">Neue Powershell-Cmdlets zum Aktivieren/Deaktivieren von HTTPS für benutzerdefinierte Domänen hinzugefügt und alte Cmdlets außer Betrieb genommen</span><span class="sxs-lookup"><span data-stu-id="98bd2-1427">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="98bd2-1428">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="98bd2-1428">Az.Compute</span></span>
* <span data-ttu-id="98bd2-1429">Unterstützung für Platzhalterzeichen zu Get-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1429">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="98bd2-1430">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="98bd2-1430">Az.DataFactory</span></span>
* <span data-ttu-id="98bd2-1431">Version des ADF .NET SDK auf 3.0.1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1431">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="98bd2-1432">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="98bd2-1432">Az.LogicApp</span></span>
* <span data-ttu-id="98bd2-1433">„ListWorkflows“ wurde korrigiert, da nur die erste Seite mit Ergebnissen abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1433">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="98bd2-1434">Az.Network</span><span class="sxs-lookup"><span data-stu-id="98bd2-1434">Az.Network</span></span>
* <span data-ttu-id="98bd2-1435">Unterstützung für Platzhalterzeichen zu Network-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1435">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="98bd2-1436">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="98bd2-1436">Az.RecoveryServices</span></span>
* <span data-ttu-id="98bd2-1437">SQL Server jetzt in Azure-VM-Support enthalten</span><span class="sxs-lookup"><span data-stu-id="98bd2-1437">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="98bd2-1438">SDK-Update</span><span class="sxs-lookup"><span data-stu-id="98bd2-1438">SDK Update</span></span>
* <span data-ttu-id="98bd2-1439">VMappContainer-Überprüfung in „Get-ProtectableItem“ entfernt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1439">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="98bd2-1440">„Name“ und „ServerName“ als Parameter für „Get-ProtectableItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1440">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="98bd2-1441">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="98bd2-1441">Az.Resources</span></span>
* <span data-ttu-id="98bd2-1442">Parameter `-TemplateObject` zu Bereitstellungs-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1442">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="98bd2-1443">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="98bd2-1443">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="98bd2-1444">Problem beim Piping des Ergebnisses von `Get-AzResource` an `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-1444">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="98bd2-1445">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="98bd2-1445">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="98bd2-1446">Problem mit JSON-Datentypänderung beim Ausführen von `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-1446">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="98bd2-1447">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="98bd2-1447">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="98bd2-1448">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="98bd2-1448">Az.Sql</span></span>
* <span data-ttu-id="98bd2-1449">„AuditingEndpointsCommunicator“ wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1449">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="98bd2-1450">Das Verhalten eines Grenzfalls beim Erstellen neuer Diagnoseeinstellungen wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1450">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="98bd2-1451">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="98bd2-1451">Az.Storage</span></span>
* <span data-ttu-id="98bd2-1452">Unterstützung von „Kind BlockBlobStorage“ beim Erstellen eines Speicherkontos: New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="98bd2-1452">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="98bd2-1453">1.4.0 – Februar 2019</span><span class="sxs-lookup"><span data-stu-id="98bd2-1453">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="98bd2-1454">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="98bd2-1454">Az.AnalysisServices</span></span>
* <span data-ttu-id="98bd2-1455">Cmdlet „AddAzureASAccount“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1455">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="98bd2-1456">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="98bd2-1456">Az.Automation</span></span>
* <span data-ttu-id="98bd2-1457">Hilfe für „Import-AzAutomationDscNodeConfiguration“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1457">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="98bd2-1458">Überprüfung des Konfigurationsnamens zu Cmdlet „Import-AzAutomationDscConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1458">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="98bd2-1459">Fehlerbehandlung für Cmdlet „Import-AzAutomationDscConfiguration“ verbessert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1459">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="98bd2-1460">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="98bd2-1460">Az.CognitiveServices</span></span>
* <span data-ttu-id="98bd2-1461">„CustomSubdomainName“ als neuer optionaler Parameter für Cmdlet „New-AzCognitiveServicesAccount“ hinzugefügt, das zum Angeben der Unterdomäne für die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1461">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="98bd2-1462">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="98bd2-1462">Az.Compute</span></span>
* <span data-ttu-id="98bd2-1463">Problem mit ID-Parametersätzen behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-1463">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="98bd2-1464">„Get-AzVMExtension“ aktualisiert, sodass alle installierten Erweiterungen aufgelistet werden, wenn der Name-Parameter nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="98bd2-1464">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="98bd2-1465">Parameter „Tag“ und „ResourceId“ zum Cmdlet „Update-AzImage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1465">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="98bd2-1466">„Get-AzVmssVM“ ohne Instanz-ID und mit „InstanceView“ können virtuelle VMSS-Computer mit Instanzansicht auflisten.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1466">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="98bd2-1467">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="98bd2-1467">Az.DataLakeStore</span></span>
* <span data-ttu-id="98bd2-1468">Cmdlets zum Auflisten und Wiederherstellen gelöschter ADL-Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1468">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="98bd2-1469">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="98bd2-1469">Az.EventHub</span></span>
* <span data-ttu-id="98bd2-1470">Neue boolesche Eigenschaft „SkipEmptyArchives“ zum Überspringen leerer Archive in Klasse „CaptureDescription“ von EventHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1470">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="98bd2-1471">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="98bd2-1471">Az.KeyVault</span></span>
* <span data-ttu-id="98bd2-1472">Kennzeichnung in „Set-AzKeyVaultSecret“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1472">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="98bd2-1473">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="98bd2-1473">Az.LogicApp</span></span>
* <span data-ttu-id="98bd2-1474">SKU „Basic“ für Integrationskonten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1474">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="98bd2-1475">XSLT 2.0, XSLT 3.0 und Liquid-Zuordnungstypen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1475">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="98bd2-1476">Neue Cmdlets für Integrationskonto-Assemblys</span><span class="sxs-lookup"><span data-stu-id="98bd2-1476">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="98bd2-1477">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="98bd2-1477">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="98bd2-1478">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="98bd2-1478">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="98bd2-1479">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="98bd2-1479">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="98bd2-1480">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="98bd2-1480">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="98bd2-1481">Neue Cmdlets für Integrationskonto-Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="98bd2-1481">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="98bd2-1482">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="98bd2-1482">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="98bd2-1483">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="98bd2-1483">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="98bd2-1484">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="98bd2-1484">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="98bd2-1485">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="98bd2-1485">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="98bd2-1486">Logik-App-SDK auf Version 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1486">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="98bd2-1487">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="98bd2-1487">Az.Monitor</span></span>
* <span data-ttu-id="98bd2-1488">Hilfe für „Get-AzMetric“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1488">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="98bd2-1489">Az.Network</span><span class="sxs-lookup"><span data-stu-id="98bd2-1489">Az.Network</span></span>
* <span data-ttu-id="98bd2-1490">Hilfebeispiel für „Add-AzApplicationGatewayCustomError“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1490">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="98bd2-1491">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="98bd2-1491">Az.OperationalInsights</span></span>
* <span data-ttu-id="98bd2-1492">Zusätzliche Unterstützung für Datenquelle von „New-ApplicationInsights“ und „Get-ApplicationInsights“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1492">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="98bd2-1493">Neue Art von „ApplicationInsights“ zum Abrufen von bestimmten und von allen ApplicationInsights-Datenquellen für einen Workspace hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1493">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="98bd2-1494">Cmdlet „New-AzOperationalInsightsApplicationInsightsDataSource“ zum Erstellen einer Datenquelle anhand des angegebenen Ressourcenparameters für „Application-Insights“ hinzugefügt: „subscriptionId“, „resourceGroupName“ und „name“.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1494">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="98bd2-1495">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="98bd2-1495">Az.Resources</span></span>
* <span data-ttu-id="98bd2-1496">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="98bd2-1496">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="98bd2-1497">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="98bd2-1497">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="98bd2-1498">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="98bd2-1498">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="98bd2-1499">Fehler korrigiert, der die wiederholte Erstellung von „KeyCredentials“ verhindert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1499">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="98bd2-1500">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="98bd2-1500">Az.Sql</span></span>
* <span data-ttu-id="98bd2-1501">Unterstützung für SQL DB Hyperscale-Tarif hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1501">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="98bd2-1502">Fehler korrigiert, aufgrund dessen die Wiederherstellung wegen der Festlegung unnötiger Eigenschaften in der Wiederherstellungsanforderung fehlschlagen konnte</span><span class="sxs-lookup"><span data-stu-id="98bd2-1502">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="98bd2-1503">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="98bd2-1503">Az.Websites</span></span>
* <span data-ttu-id="98bd2-1504">Beispiel in „Get-AzWebAppSlotMetrics“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1504">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="98bd2-1505">1.3.0: Februar 2019</span><span class="sxs-lookup"><span data-stu-id="98bd2-1505">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="98bd2-1506">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="98bd2-1506">Az.Accounts</span></span>
* <span data-ttu-id="98bd2-1507">Update auf die aktuelle Version von ClientRuntime durchgeführt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1507">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="98bd2-1508">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="98bd2-1508">Az.AnalysisServices</span></span>
<span data-ttu-id="98bd2-1509">Allgemeine Verfügbarkeit für Az.AnalysisServices-Modul</span><span class="sxs-lookup"><span data-stu-id="98bd2-1509">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="98bd2-1510">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="98bd2-1510">Az.Compute</span></span>
* <span data-ttu-id="98bd2-1511">AEM-Erweiterung: Unterstützung für UltraSSD und P60-, P70- und P80-Datenträger hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1511">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="98bd2-1512">Hilfebeschreibung für „Set-AzVMBootDiagnostics“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1512">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="98bd2-1513">Hilfebeschreibung und Beispiel für „Update-AzImage“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1513">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="98bd2-1514">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="98bd2-1514">Az.RecoveryServices</span></span>
<span data-ttu-id="98bd2-1515">Allgemeine Verfügbarkeit für Az.RecoveryServices-Modul.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1515">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="98bd2-1516">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="98bd2-1516">Az.Resources</span></span>
* <span data-ttu-id="98bd2-1517">Kennzeichnung für Ressourcengruppen korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1517">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="98bd2-1518">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="98bd2-1518">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="98bd2-1519">Problem behoben, bei dem „-ErrorAction“ von `Get-AzureRmRoleAssignment` nicht berücksichtigt wird</span><span class="sxs-lookup"><span data-stu-id="98bd2-1519">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="98bd2-1520">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="98bd2-1520">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="98bd2-1521">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="98bd2-1521">Az.Sql</span></span>
* <span data-ttu-id="98bd2-1522">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1522">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="98bd2-1523">Problem behoben, bei dem eine fehlende Anmeldung am Azure-Konto bei der Ausführung von SQL-Cmdlets zu einer nullref-Ausnahme führt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1523">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="98bd2-1524">nullref-Ausnahme in Get-AzSqlCapability korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1524">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="98bd2-1525">1.2.1: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="98bd2-1525">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="98bd2-1526">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="98bd2-1526">Az.Accounts</span></span>
* <span data-ttu-id="98bd2-1527">Release mit richtiger Version der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="98bd2-1527">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="98bd2-1528">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="98bd2-1528">Az.AnalysisServices</span></span>
* <span data-ttu-id="98bd2-1529">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="98bd2-1529">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="98bd2-1530">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="98bd2-1530">Az.RecoveryServices</span></span>
* <span data-ttu-id="98bd2-1531">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="98bd2-1531">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="98bd2-1532">1.2.0: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="98bd2-1532">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="98bd2-1533">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="98bd2-1533">Az.Accounts</span></span>
* <span data-ttu-id="98bd2-1534">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1534">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="98bd2-1535">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1535">Update incorrect online help URLs</span></span>
* <span data-ttu-id="98bd2-1536">Warnmeldung in PS Core für „Uninstall-AzureRm“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1536">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="98bd2-1537">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="98bd2-1537">Az.Aks</span></span>
* <span data-ttu-id="98bd2-1538">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1538">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="98bd2-1539">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="98bd2-1539">Az.Automation</span></span>
* <span data-ttu-id="98bd2-1540">Unterstützung für Python 2-Runbooks hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1540">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="98bd2-1541">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1541">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="98bd2-1542">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="98bd2-1542">Az.Cdn</span></span>
* <span data-ttu-id="98bd2-1543">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1543">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="98bd2-1544">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="98bd2-1544">Az.Compute</span></span>
* <span data-ttu-id="98bd2-1545">Cmdlet „Invoke-AzVMReimage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1545">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="98bd2-1546">Parameter „TempDisk“ zu „Set-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1546">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="98bd2-1547">Warnmeldung von „New-AzVM“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1547">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="98bd2-1548">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="98bd2-1548">Az.ContainerRegistry</span></span>
* <span data-ttu-id="98bd2-1549">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1549">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="98bd2-1550">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="98bd2-1550">Az.DataFactory</span></span>
* <span data-ttu-id="98bd2-1551">Version des ADF .NET SDK auf 3.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1551">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="98bd2-1552">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="98bd2-1552">Az.DataLakeStore</span></span>
* <span data-ttu-id="98bd2-1553">Problem mit ADLS-Endpunkt bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-1553">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="98bd2-1554">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="98bd2-1554">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="98bd2-1555">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1555">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="98bd2-1556">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="98bd2-1556">Az.IotHub</span></span>
* <span data-ttu-id="98bd2-1557">Codierungsformat zu Cmdlet „Add-IotHubRoutingEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1557">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="98bd2-1558">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="98bd2-1558">Az.KeyVault</span></span>
* <span data-ttu-id="98bd2-1559">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1559">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="98bd2-1560">Az.Network</span><span class="sxs-lookup"><span data-stu-id="98bd2-1560">Az.Network</span></span>
* <span data-ttu-id="98bd2-1561">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1561">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="98bd2-1562">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="98bd2-1562">Az.Resources</span></span>
* <span data-ttu-id="98bd2-1563">Fehlerhafte Beispiele in Referenzdokumentation zu „New-AzADAppCredential“ und „New-AzADSpCredential“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1563">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="98bd2-1564">Problem behoben, bei dem der Pfad für den Parameter „-TemplateFile“ nicht aufgelöst wurde, bevor Cmdlets für die Bereitstellung von Ressourcengruppen ausgeführt wurden</span><span class="sxs-lookup"><span data-stu-id="98bd2-1564">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="98bd2-1565">Az.Resources: Richtige Dokumentation für Standardwert von „New-AzureRmPolicyDefinition -Mode“ bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1565">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="98bd2-1566">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="98bd2-1566">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="98bd2-1567">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="98bd2-1567">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="98bd2-1568">Formatierungsproblem für Objekt „PSResourceGroupDeployment“ behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-1568">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="98bd2-1569">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="98bd2-1569">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="98bd2-1570">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="98bd2-1570">Az.ServiceFabric</span></span>
* <span data-ttu-id="98bd2-1571">Rollback beim Hinzufügen eines Zertifikats zum VMSS-Modell, Auslösung einer Ausnahme. Fehlerbehebung: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="98bd2-1571">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="98bd2-1572">Einige Fehlermeldungen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1572">Fix some error messages.</span></span>
* <span data-ttu-id="98bd2-1573">Fehler bei Clustererstellung mit ARM-Standardvorlage für „New-AzServiceFabriCluster“ behoben, bei dem die Migration zu Az nicht funktioniert hat.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1573">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="98bd2-1574">Fehler behoben beim Hinzufügen eines Cluster-/Anwendungszertifikats ausschließlich zu VM Scale Sets, die zum Cluster gehören, indem die Cluster-ID in der Erweiterung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1574">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="98bd2-1575">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="98bd2-1575">Az.SignalR</span></span>
* <span data-ttu-id="98bd2-1576">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1576">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="98bd2-1577">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="98bd2-1577">Az.Sql</span></span>
* <span data-ttu-id="98bd2-1578">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1578">Update incorrect online help URLs</span></span>
* <span data-ttu-id="98bd2-1579">Parameterbeschreibung für den Parameter „LicenseType“ mit möglichen Werten aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1579">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="98bd2-1580">Fehler behoben, bei dem die Aktualisierung der Identität der verwalteten Instanz nicht funktioniert hat, wenn es sich um die einzige aktualisierte Eigenschaft gehandelt hat</span><span class="sxs-lookup"><span data-stu-id="98bd2-1580">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="98bd2-1581">Unterstützung für die benutzerdefinierte Sortierung auf verwalteter Instanz</span><span class="sxs-lookup"><span data-stu-id="98bd2-1581">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="98bd2-1582">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="98bd2-1582">Az.Storage</span></span>
* <span data-ttu-id="98bd2-1583">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1583">Update incorrect online help URLs</span></span>
* <span data-ttu-id="98bd2-1584">Ausführliche Fehlermeldung beim Abrufen/Festlegen der klassischen Protokollierung bzw. Metriken für Storage Premium-Konto, da für das Storage Premium-Konto die klassische Protokollierung bzw. Metriken nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1584">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="98bd2-1585">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="98bd2-1585">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="98bd2-1586">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="98bd2-1586">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="98bd2-1587">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="98bd2-1587">Az.TrafficManager</span></span>
* <span data-ttu-id="98bd2-1588">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1588">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="98bd2-1589">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="98bd2-1589">Az.Websites</span></span>
* <span data-ttu-id="98bd2-1590">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1590">Update incorrect online help URLs</span></span>
* <span data-ttu-id="98bd2-1591">„New-AzWebAppSSLBinding“ korrigiert, damit das Zertifikat in die richtige Ressourcengruppe bzw. an den richtigen Speicherort hochgeladen wird, wenn die App in einer ASE gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1591">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="98bd2-1592">„New-AzWebAppSSLBinding“ korrigiert, damit die Tags beim Binden eines SSL-Zertifikats an eine App nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1592">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="98bd2-1593">1.1.0 – Januar 2019</span><span class="sxs-lookup"><span data-stu-id="98bd2-1593">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="98bd2-1594">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="98bd2-1594">Az.Accounts</span></span>
* <span data-ttu-id="98bd2-1595">Bereich „Local“ zu „Enable-AzureRmAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1595">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="98bd2-1596">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="98bd2-1596">Az.Compute</span></span>
* <span data-ttu-id="98bd2-1597">Name ist jetzt optional im ID-Parametersatz für „Restart/Start/Stop/Remove/Set-AzVM“ und „Save-AzVMImage“</span><span class="sxs-lookup"><span data-stu-id="98bd2-1597">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="98bd2-1598">Beschreibung der ID in Hilfedateien aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1598">Updated the description of ID in help files</span></span>
* <span data-ttu-id="98bd2-1599">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-1599">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="98bd2-1600">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="98bd2-1600">Az.DataLakeStore</span></span>
* <span data-ttu-id="98bd2-1601">Aktualisierung der SDK-Version der Datenebene auf 1.1.14 für SDK-Fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1601">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="98bd2-1602">Behandlung von negativen acesstime- and modificationtime-Werten für „getfilestatus“ und „liststatus“ korrigiert, asynchrones Abbruchtoken korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1602">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="98bd2-1603">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="98bd2-1603">Az.EventGrid</span></span>
* <span data-ttu-id="98bd2-1604">Zur Verwendung der API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1604">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="98bd2-1605">Aktualisierung der folgenden Cmdlets zur Unterstützung des neuen Szenarios in der API-Version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="98bd2-1605">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="98bd2-1606">New-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="98bd2-1606">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="98bd2-1607">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="98bd2-1607">Event Time-To-Live,</span></span>
        - <span data-ttu-id="98bd2-1608">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="98bd2-1608">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="98bd2-1609">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="98bd2-1609">Dead letter endpoint.</span></span>
    - <span data-ttu-id="98bd2-1610">Update-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="98bd2-1610">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="98bd2-1611">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="98bd2-1611">Event Time-To-Live,</span></span>
        - <span data-ttu-id="98bd2-1612">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="98bd2-1612">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="98bd2-1613">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="98bd2-1613">Dead letter endpoint.</span></span>
* <span data-ttu-id="98bd2-1614">Neue Enumerationswerte („storageQueue“ und „hybridConnection“) für die EndpointType-Option in den Cmdlets „New-AzureRmEventGridSubscription“ und „Update-AzureRmEventGridSubscription“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1614">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="98bd2-1615">Anzeige einer Warnmeldung, wenn das Erstellen oder Aktualisieren des Ereignisabonnements voraussichtlich eine manuelle Aktion des Benutzers zur Folge hat</span><span class="sxs-lookup"><span data-stu-id="98bd2-1615">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="98bd2-1616">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="98bd2-1616">Az.IotHub</span></span>
* <span data-ttu-id="98bd2-1617">Auf die aktuelle Version des Iot Hub SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1617">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="98bd2-1618">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="98bd2-1618">Az.LogicApp</span></span>
* <span data-ttu-id="98bd2-1619">„Get-AzLogicApp“ listet alle Apps ohne angegebenen Namen auf</span><span class="sxs-lookup"><span data-stu-id="98bd2-1619">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="98bd2-1620">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="98bd2-1620">Az.Resources</span></span>
* <span data-ttu-id="98bd2-1621">Problem mit dem Parametersatz bei Angabe der Parameter „-ODataQuery“ und „-ResourceId“ für „Get-AzResource“ behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-1621">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="98bd2-1622">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="98bd2-1622">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="98bd2-1623">Behandlung des Parameters „-Custom“ in „New/Set-AzPolicyDefinition“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1623">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="98bd2-1624">Tippfehler in der Dokumentation für „New-AzDeployment“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1624">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="98bd2-1625">Parameter „-MailNickname“ als obligatorisch festgelegt für „New-AzADUser“</span><span class="sxs-lookup"><span data-stu-id="98bd2-1625">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="98bd2-1626">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="98bd2-1626">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="98bd2-1627">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="98bd2-1627">Az.SignalR</span></span>
* <span data-ttu-id="98bd2-1628">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-1628">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="98bd2-1629">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="98bd2-1629">Az.Sql</span></span>
* <span data-ttu-id="98bd2-1630">Abhängigkeit des Speicherverwaltungsclients zur allgemeinen SDK-Implementierung konvertiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1630">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="98bd2-1631">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="98bd2-1631">Az.Storage</span></span>
* <span data-ttu-id="98bd2-1632">Festlegung des „StorageAccountName“ des Speicherkontexts als tatsächlichen Namen des Speicherkontos, wenn dieser mit „SAS-Token“, „OAuth“ oder „Anonym“ erstellt wird</span><span class="sxs-lookup"><span data-stu-id="98bd2-1632">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="98bd2-1633">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="98bd2-1633">New-AzStorageContext</span></span>
* <span data-ttu-id="98bd2-1634">Erstellen von SAS-Token des Blob-Momentaufnahmeobjekts mit dem Parameter „-FullUri“, Festlegung des zurückgegebenen URI als Momentaufnahme-URI</span><span class="sxs-lookup"><span data-stu-id="98bd2-1634">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="98bd2-1635">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="98bd2-1635">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="98bd2-1636">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="98bd2-1636">Az.Websites</span></span>
* <span data-ttu-id="98bd2-1637">Fehler bei der Datumsanalyse in „Get-AzDeletedWebApp“ behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-1637">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="98bd2-1638">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-1638">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="98bd2-1639">1.0.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="98bd2-1639">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="98bd2-1640">Allgemein</span><span class="sxs-lookup"><span data-stu-id="98bd2-1640">General</span></span>

- <span data-ttu-id="98bd2-1641">Allgemeine Verfügbarkeit des Az-Moduls</span><span class="sxs-lookup"><span data-stu-id="98bd2-1641">General Availability of Az Module</span></span>
- <span data-ttu-id="98bd2-1642">Onlinehilfe für jedes Modul</span><span class="sxs-lookup"><span data-stu-id="98bd2-1642">Online help for each module</span></span>
- <span data-ttu-id="98bd2-1643">Ausführlichere Informationen und eine Roadmap finden Sie auf der [Seite mit der Ankündigung zu Az](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="98bd2-1643">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="98bd2-1644">Informationen zur Migration aus AzureRM finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="98bd2-1644">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="98bd2-1645">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="98bd2-1645">Az.Accounts</span></span>
- <span data-ttu-id="98bd2-1646">Geändert von Az.Profile</span><span class="sxs-lookup"><span data-stu-id="98bd2-1646">Changed from Az.Profile</span></span>
- <span data-ttu-id="98bd2-1647">Feste Tabellenformate für Profil- und Kontexttypen</span><span class="sxs-lookup"><span data-stu-id="98bd2-1647">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="98bd2-1648">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="98bd2-1648">Az.ApiManagement</span></span>
- <span data-ttu-id="98bd2-1649">Korrekturen für #7002</span><span class="sxs-lookup"><span data-stu-id="98bd2-1649">Fixes for #7002</span></span>
- <span data-ttu-id="98bd2-1650">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="98bd2-1650">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="98bd2-1651">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="98bd2-1651">Az.Batch</span></span>
- <span data-ttu-id="98bd2-1652">Möglichkeit zum Anzeigen der ausgeführten Version des Azure Batch-Knoten-Agents auf den VMs eines Pools mit der neuen `NodeAgentInformation`-Eigenschaft für `PSComputeNode` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1652">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="98bd2-1653">Der `Caching`-Standardwert für `PSDataDisk` lautet jetzt nicht mehr `None`, sondern `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1653">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="98bd2-1654">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="98bd2-1654">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="98bd2-1655">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="98bd2-1655">Az.Billing</span></span>
- <span data-ttu-id="98bd2-1656">Kombination von Billing-, Consumption- und UsageAggregates-Cmdlets. Ausführliche Informationen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="98bd2-1656">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="98bd2-1657">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="98bd2-1657">Az.CognitivServices</span></span>
- <span data-ttu-id="98bd2-1658">Vervollständigungen für SkuName und Typem für den Vorgang New-AzureRmCognitiveServicesAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1658">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="98bd2-1659">GetSkusWithAccountParamSetName-Parametersatz aus Get-AzCognitiveServicesAccountSkus entfernt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1659">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="98bd2-1660">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="98bd2-1660">Az.ContainerInstance</span></span>
- <span data-ttu-id="98bd2-1661">ManagedIdentity-Unterstützung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1661">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="98bd2-1662">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="98bd2-1662">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="98bd2-1663">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="98bd2-1663">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="98bd2-1664">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="98bd2-1664">Az.DataLakeStore</span></span>
- <span data-ttu-id="98bd2-1665">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="98bd2-1665">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="98bd2-1666">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="98bd2-1666">Az.Monitor</span></span>
- <span data-ttu-id="98bd2-1667">Az.Insights in Az.Monitor umbenannt und weitere weniger wichtige grundlegende Änderungen durchgeführt. Informationen hierzu finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="98bd2-1667">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="98bd2-1668">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="98bd2-1668">Az.KeyVault</span></span>
- <span data-ttu-id="98bd2-1669">Veraltete PurgeDisabled-Eigenschaft aus Ausgabetypen entfernt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1669">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="98bd2-1670">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="98bd2-1670">Az.MachineLearning</span></span>
- <span data-ttu-id="98bd2-1671">Cmdlets des Az.MachineLearningCompute-Moduls eingebunden</span><span class="sxs-lookup"><span data-stu-id="98bd2-1671">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="98bd2-1672">Az.Media</span><span class="sxs-lookup"><span data-stu-id="98bd2-1672">Az.Media</span></span>
- <span data-ttu-id="98bd2-1673">Veralteten -Tags-Alias aus New-AzMediaService entfernt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1673">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="98bd2-1674">Az.Network</span><span class="sxs-lookup"><span data-stu-id="98bd2-1674">Az.Network</span></span>
<span data-ttu-id="98bd2-1675">Unterstützung für das Konfigurieren von RewriteRuleSets im Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1675">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="98bd2-1676">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="98bd2-1676">New cmdlets added:</span></span>
        - <span data-ttu-id="98bd2-1677">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="98bd2-1677">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="98bd2-1678">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="98bd2-1678">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="98bd2-1679">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="98bd2-1679">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="98bd2-1680">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="98bd2-1680">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="98bd2-1681">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="98bd2-1681">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="98bd2-1682">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="98bd2-1682">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="98bd2-1683">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="98bd2-1683">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="98bd2-1684">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="98bd2-1684">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="98bd2-1685">Cmdlets mit optionalem Parameter -RewriteRuleSet aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1685">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="98bd2-1686">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="98bd2-1686">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="98bd2-1687">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="98bd2-1687">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="98bd2-1688">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="98bd2-1688">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="98bd2-1689">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="98bd2-1689">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="98bd2-1690">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="98bd2-1690">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="98bd2-1691">New-AzureRmApplicationGatewayUrlPathMapConfig: KeyVault-Unterstützung mithilfe von Identität zum Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1691">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="98bd2-1692">Cmdlets mit optionalem Parameter aktualisiert: -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="98bd2-1692">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="98bd2-1693">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="98bd2-1693">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="98bd2-1694">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="98bd2-1694">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="98bd2-1695">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="98bd2-1695">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="98bd2-1696">Cmdlet New-AzApplicationGateway mit optionalem Parameter -UserAssignedIdentity aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1696">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="98bd2-1697">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="98bd2-1697">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="98bd2-1698">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="98bd2-1698">Az.OperationalInsights</span></span>
- <span data-ttu-id="98bd2-1699">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="98bd2-1699">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="98bd2-1700">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="98bd2-1700">Az.Profile</span></span>
- <span data-ttu-id="98bd2-1701">Modulnamen in Az.Accounts geändert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1701">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="98bd2-1702">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="98bd2-1702">Az.RecoveryServices</span></span>
- <span data-ttu-id="98bd2-1703">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="98bd2-1703">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="98bd2-1704">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="98bd2-1704">Az.Resources</span></span>
- <span data-ttu-id="98bd2-1705">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="98bd2-1705">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="98bd2-1706">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="98bd2-1706">Az.ServiceFabric</span></span>
- <span data-ttu-id="98bd2-1707">Unterstützung für das Angeben des Zertifikats anhand des allgemeinen Namens und Fingerabdrucks</span><span class="sxs-lookup"><span data-stu-id="98bd2-1707">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="98bd2-1708">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="98bd2-1708">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="98bd2-1709">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="98bd2-1709">Az.SIgnalR</span></span>
- <span data-ttu-id="98bd2-1710">Allgemeine Verfügbarkeit für PowerShell-Cmdlets für SIgnalR</span><span class="sxs-lookup"><span data-stu-id="98bd2-1710">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="98bd2-1711">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="98bd2-1711">Az.Sql</span></span>
- <span data-ttu-id="98bd2-1712">Neue Erkennungstypen Data_Exfiltration und Unsafe_Action zu Cmdlets für Bedrohungserkennung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1712">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="98bd2-1713">Dokumentationsbeispiele für Cmdlets für SQL-Überwachung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1713">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="98bd2-1714">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="98bd2-1714">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="98bd2-1715">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="98bd2-1715">Az.Storage</span></span>
- <span data-ttu-id="98bd2-1716">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="98bd2-1716">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="98bd2-1717">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="98bd2-1717">Az.Websites</span></span>
- <span data-ttu-id="98bd2-1718">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="98bd2-1718">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="98bd2-1719">0.7.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="98bd2-1719">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="98bd2-1720">Allgemein</span><span class="sxs-lookup"><span data-stu-id="98bd2-1720">General</span></span>

* <span data-ttu-id="98bd2-1721">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="98bd2-1721">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="98bd2-1722">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="98bd2-1722">Az.Compute</span></span>

* <span data-ttu-id="98bd2-1723">Unterstützung für UltraSSD und Katalogimages in einfachen Parametersätzen für `New-AzVm(ss)`-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1723">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="98bd2-1724">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="98bd2-1724">Az.DataLakeStore</span></span>

* <span data-ttu-id="98bd2-1725">Nachgestellten Schrägstrich für die Domäne des ADLS-Kontos korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1725">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="98bd2-1726">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="98bd2-1726">Az.FrontDoor</span></span>

* <span data-ttu-id="98bd2-1727">Einige fehlerhafte Links behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-1727">Fixed some broken links</span></span>
    - <span data-ttu-id="98bd2-1728">In den Artikeln zu New-AzureRmFrontDoor und Set-AzureRmFrontDoor den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorHealthProbeSettingObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1728">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="98bd2-1729">Im Artikel zu New-AzureRmFrontDoorManagedRuleObject den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorRuleGroupOverrideObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1729">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="98bd2-1730">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="98bd2-1730">Az.RecoveryServices</span></span>

* <span data-ttu-id="98bd2-1731">Clientseitige Validierungen für Wiederherstellungsvorgänge von Azure-Dateifreigaben hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1731">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="98bd2-1732">storageAccountName und storageAccountResourceGroupName für AFS-Wiederherstellung optional gemacht.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1732">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="98bd2-1733">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="98bd2-1733">Az.Resources</span></span>

* <span data-ttu-id="98bd2-1734">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="98bd2-1734">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="98bd2-1735">Get-AzureRmRoleAssignment für die Verwendung des Abonnementbereichs aktualisiert, wenn dieser beim Anfordern von klassischen Administratoren angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1735">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="98bd2-1736">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="98bd2-1736">Az.Sql</span></span>

* <span data-ttu-id="98bd2-1737">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="98bd2-1737">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="98bd2-1738">Problem mit der Verwendung von Get-AzureRmSqlDatabaseVulnerabilityAssessment mit .NET Core behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-1738">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="98bd2-1739">Dokumentation mit Hilfemeldungen zu Cmdlets für die SQL-Überwachung geändert.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1739">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="98bd2-1740">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="98bd2-1740">Az.Storage</span></span>

* <span data-ttu-id="98bd2-1741">-EnableHierarchicalNamespace zu New-AzureRmStorageAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1741">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="98bd2-1742">Problem behoben, bei dem für das Copy File-Cmdlet am Ziel kein Quellkontext wiederverwendet werden kann, wenn -DestContext nicht eingegeben wird</span><span class="sxs-lookup"><span data-stu-id="98bd2-1742">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="98bd2-1743">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="98bd2-1743">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="98bd2-1744">Unterstützung der Konfiguration von statischen Websites</span><span class="sxs-lookup"><span data-stu-id="98bd2-1744">Support Static Website configuration</span></span>
    - <span data-ttu-id="98bd2-1745">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="98bd2-1745">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="98bd2-1746">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="98bd2-1746">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="98bd2-1747">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="98bd2-1747">Az.Websites</span></span>

* <span data-ttu-id="98bd2-1748">Set-AzureRmWebApp und Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="98bd2-1748">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="98bd2-1749">Neuen Parameter (-AzureStoragePath) zum Angeben von Azure Storage-Pfaden hinzugefügt, die in Windows- und Linux-Container-Apps bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1749">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="98bd2-1750">Verwenden Sie die Ausgabe des neuen Cmdlets New-AzureRmWebAppAzureStoragePath als Parameter zum Festlegen der Azure Storage-Pfade.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1750">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="98bd2-1751">0.6.1 – November 2018</span><span class="sxs-lookup"><span data-stu-id="98bd2-1751">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="98bd2-1752">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="98bd2-1752">Az.ApiManagement</span></span>
* <span data-ttu-id="98bd2-1753">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1753">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="98bd2-1754">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="98bd2-1754">Az.Automation</span></span>
* <span data-ttu-id="98bd2-1755">Swagger-basierte Azure Automation-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="98bd2-1755">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="98bd2-1756">Cmdlets zur Updateverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1756">Added Update Management cmdlets</span></span>
* <span data-ttu-id="98bd2-1757">Cmdlets zur Quellcodeverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1757">Added Source Control cmdlets</span></span>
* <span data-ttu-id="98bd2-1758">Cmdlet „Remove-AzureRmAutomationHybridWorkerGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1758">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="98bd2-1759">DSC-Befehl für die Knotenregistrierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1759">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="98bd2-1760">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="98bd2-1760">Az.Compute</span></span>
* <span data-ttu-id="98bd2-1761">Identitätsproblem für SystemAssigned-Identität korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1761">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="98bd2-1762">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1762">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="98bd2-1763">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="98bd2-1763">Az.ContainerInstance</span></span>
* <span data-ttu-id="98bd2-1764">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1764">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="98bd2-1765">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="98bd2-1765">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="98bd2-1766">Beschreibung der Beispiele für Marketplace-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1766">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="98bd2-1767">Az.Network</span><span class="sxs-lookup"><span data-stu-id="98bd2-1767">Az.Network</span></span>
* <span data-ttu-id="98bd2-1768">Folgende Cmdlets hinzugefügt: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="98bd2-1768">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="98bd2-1769">ICMP wieder unterstützten AzureFirewall-Netzwerkprotokollen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1769">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="98bd2-1770">Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert und Überprüfung für Ziel-ID, Adresse und Port hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1770">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="98bd2-1771">Probleme mit Arbeitsspeicherauslastung in der VirtualNetwork-Zuordnung behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-1771">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="98bd2-1772">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="98bd2-1772">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="98bd2-1773">Problem beim Ändern der Richtlinie für eine geschützte Dateifreigabe behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-1773">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="98bd2-1774">Richtlinienzeitzone in Großschreibung geändert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1774">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="98bd2-1775">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="98bd2-1775">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="98bd2-1776">Korrigiertes Beispiel in „New-AzureRmRecoveryServicesAsrProtectableItem“</span><span class="sxs-lookup"><span data-stu-id="98bd2-1776">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="98bd2-1777">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1777">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="98bd2-1778">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="98bd2-1778">Az.Relay</span></span>
* <span data-ttu-id="98bd2-1779">Optionaler Parameter „-KeyValue“ zu Cmdlet „New-AzureRmRelayKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht</span><span class="sxs-lookup"><span data-stu-id="98bd2-1779">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="98bd2-1780">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="98bd2-1780">Az.Resources</span></span>
* <span data-ttu-id="98bd2-1781">Hilfedokumentation für ressourcenidentitätsbezogene Parameter in `New-AzureRmPolicyAssignment` und `Set-AzureRmPolicyAssignment` aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1781">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="98bd2-1782">Beispiel für „New-AzureRmPolicyDefinition“ hinzugefügt, das „-Metadata“ nutzt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1782">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="98bd2-1783">Korrektur, um Beibehaltung von Groß-/Kleinschreibung in Tagschlüsseln in „NetStandard“ zu ermöglichen: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="98bd2-1783">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="98bd2-1784">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="98bd2-1784">Az.ServiceFabric</span></span>
* <span data-ttu-id="98bd2-1785">Benachrichtigung über veraltete Elemente für anstehende wichtige Änderungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1785">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="98bd2-1786">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="98bd2-1786">Az.Sql</span></span>
* <span data-ttu-id="98bd2-1787">Neue Cmdlets für CRUD-Vorgänge in verwalteten Azure SQL-Datenbank-Instanzen und verwalteten Azure SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1787">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="98bd2-1788">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="98bd2-1788">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="98bd2-1789">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="98bd2-1789">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="98bd2-1790">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="98bd2-1790">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="98bd2-1791">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="98bd2-1791">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="98bd2-1792">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="98bd2-1792">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="98bd2-1793">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="98bd2-1793">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="98bd2-1794">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="98bd2-1794">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="98bd2-1795">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="98bd2-1795">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="98bd2-1796">Erweiterte Verwaltung von Überwachungsrichtlinien auf einem Server oder in einer Datenbank aktiviert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1796">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="98bd2-1797">Neuer Parameter (PredicateExpression) hinzugefügt, um die Filterung von Überwachungsprotokollen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="98bd2-1797">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="98bd2-1798">Cmdlets wurden angepasst, sodass sie SQL-Clients anstelle von Legacyclients verwenden.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1798">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="98bd2-1799">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="98bd2-1799">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="98bd2-1800">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="98bd2-1800">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="98bd2-1801">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="98bd2-1801">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="98bd2-1802">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="98bd2-1802">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="98bd2-1803">Problem bei Verwendung von „Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings“ mit festgelegtem Parameter für den Speicherkontonamen behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-1803">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="98bd2-1804">0.5.0 – November 2018</span><span class="sxs-lookup"><span data-stu-id="98bd2-1804">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="98bd2-1805">Allgemein</span><span class="sxs-lookup"><span data-stu-id="98bd2-1805">General</span></span>
* <span data-ttu-id="98bd2-1806">Ressourcenvervollständigungen für viele Kern-Cmdlets hinzugefügt (diese ermöglichen das Durchlaufen von vorhandenen Ressourcennamen per TAB-TASTE, wenn Cmdlets interaktiv aufgerufen werden)</span><span class="sxs-lookup"><span data-stu-id="98bd2-1806">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="98bd2-1807">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="98bd2-1807">Az.Profile</span></span>
* <span data-ttu-id="98bd2-1808">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="98bd2-1808">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="98bd2-1809">Parameter „TenantId“ im Cmdlet „Connect-AzAccount“ in „Tenant“ umbenannt und Alias für „TenantId“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1809">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="98bd2-1810">Beschreibung von „TenantId“ für „Connect-AzAccount“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1810">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="98bd2-1811">Fehlermeldung für fehlgeschlagene Anmeldung bei Angabe der Mandantendomäne korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1811">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="98bd2-1812">Problem in Bezug auf Kontextnamenskonflikt für Konten ohne Abonnements im Mandanten behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-1812">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="98bd2-1813">Problem mit DataLake-Endpunkten bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-1813">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="98bd2-1814">Problem behoben, das zur Auslösung von „Disconnect-AzAccount“ führte, wenn keine Verbindung bestand</span><span class="sxs-lookup"><span data-stu-id="98bd2-1814">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="98bd2-1815">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="98bd2-1815">Az.CognitiveServices</span></span>
* <span data-ttu-id="98bd2-1816">Vorgang „Get-AzCognitiveServicesAccountSkus“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1816">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="98bd2-1817">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="98bd2-1817">Az.Compute</span></span>
* <span data-ttu-id="98bd2-1818">Cmdlets Add-AzVmssVMDataDisk und Remove-AzVmssVMDataDisk hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1818">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="98bd2-1819">„Get-AzVMImage“ zeigt „AutomaticOSUpgradeProperties“ an</span><span class="sxs-lookup"><span data-stu-id="98bd2-1819">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="98bd2-1820">Problem behoben, aufgrund dessen die Optionswerte „SetAzVMChefExtension -BootstrapOptions“ und „-JsonAttribute“ nicht im JSON-Format festgelegt wurden</span><span class="sxs-lookup"><span data-stu-id="98bd2-1820">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="98bd2-1821">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="98bd2-1821">Az.DataLakeStore</span></span>
* <span data-ttu-id="98bd2-1822">Aktualisierung des DataLake-Pakets auf 1.1.10</span><span class="sxs-lookup"><span data-stu-id="98bd2-1822">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="98bd2-1823">Standardmäßige Parallelität zu Multithreadvorgängen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1823">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="98bd2-1824">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="98bd2-1824">Az.Insights</span></span>
* <span data-ttu-id="98bd2-1825">Problem Nr. 7267 behoben (Bereich für automatische Skalierung)</span><span class="sxs-lookup"><span data-stu-id="98bd2-1825">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="98bd2-1826">Probleme beim Erstellen einer neuen Regel für die automatische Skalierung, aufgrund derer die aufgelisteten Parameter nicht richtig festgelegt wurden (Es wurde stets der Standardwert festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="98bd2-1826">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="98bd2-1827">Problem Nr. 7513 behoben [Insights] „Set-AzDiagnosticSetting“ erfordert die explizite Angabe von Kategorien während der Erstellung der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1827">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="98bd2-1828">Nun erfordert das Cmdlet nicht die explizite Angabe der Kategorien, die während der Erstellung aktiviert werden sollen. Das bedeutet, es funktioniert wie dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1828">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="98bd2-1829">Az.Network</span><span class="sxs-lookup"><span data-stu-id="98bd2-1829">Az.Network</span></span>
* <span data-ttu-id="98bd2-1830">„PeeringType“ wurde geändert und ist nun ein erforderlicher Parameter für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="98bd2-1830">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="98bd2-1831">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="98bd2-1831">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="98bd2-1832">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="98bd2-1832">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="98bd2-1833">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="98bd2-1833">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="98bd2-1834">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="98bd2-1834">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="98bd2-1835">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="98bd2-1835">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="98bd2-1836">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="98bd2-1836">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="98bd2-1837">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="98bd2-1837">Az.PolicyInsights</span></span>
* <span data-ttu-id="98bd2-1838">Cmdlets für Richtlinienwartung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1838">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="98bd2-1839">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="98bd2-1839">Az.Resources</span></span>
* <span data-ttu-id="98bd2-1840">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="98bd2-1840">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="98bd2-1841">Zulassen der Auflistung von Ressourcen mithilfe des Parameters „-ResourceId“ für „Get-AzResource“</span><span class="sxs-lookup"><span data-stu-id="98bd2-1841">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="98bd2-1842">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="98bd2-1842">Az.ServiceBus</span></span>
* <span data-ttu-id="98bd2-1843">Schreibgeschützte Eigenschaft „MigrationState“ zu „PSServiceBusMigrationConfigurationAttributes“ hinzugefügt, was das Ermitteln des Migrationsstatus ermöglicht</span><span class="sxs-lookup"><span data-stu-id="98bd2-1843">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="98bd2-1844">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="98bd2-1844">Az.ServiceFabric</span></span>
* <span data-ttu-id="98bd2-1845">Hinzufügen des Zertifikats zu Linux VMSS korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1845">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="98bd2-1846">„Add-AzServiceFabricClusterCertificate“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="98bd2-1846">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="98bd2-1847">Verwenden des richtigen Fingerabdrucks aus dem neuen Zertifikat (Azure/service-fabric-issues#932)</span><span class="sxs-lookup"><span data-stu-id="98bd2-1847">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="98bd2-1848">Richtige Anzeige von Ausnahmen (Azure/service-fabric-issues#1054)</span><span class="sxs-lookup"><span data-stu-id="98bd2-1848">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="98bd2-1849">„Update-AzServiceFabricDurability“ korrigiert, um die Clusterkonfiguration zu aktualisieren, bevor der VMSS-Vorgang „CreateOrUpdate“ gestartet wird</span><span class="sxs-lookup"><span data-stu-id="98bd2-1849">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="98bd2-1850">0.4.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="98bd2-1850">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="98bd2-1851">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="98bd2-1851">Az.Profile</span></span>
* <span data-ttu-id="98bd2-1852">Problem mit „Get-AzSubscription“ in Cloud Shell behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-1852">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="98bd2-1853">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="98bd2-1853">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="98bd2-1854">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="98bd2-1854">Az.Compute</span></span>
* <span data-ttu-id="98bd2-1855">Neue Größen zur Whitelist von VM-Größen hinzugefügt, für die bei Verwendung des einfachen Parametersatzes für „New-AzVm“ der beschleunigte Netzwerkbetrieb aktiviert wird</span><span class="sxs-lookup"><span data-stu-id="98bd2-1855">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="98bd2-1856">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1856">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="98bd2-1857">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="98bd2-1857">Az.DataLakeStore</span></span>
* <span data-ttu-id="98bd2-1858">Unterstützung für VNET-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1858">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="98bd2-1859">Get-AzDataLakeStoreVirtualNetworkRule: Dient zum Abrufen oder Auflisten der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1859">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="98bd2-1860">Add-AzDataLakeStoreVirtualNetworkRule: Fügt dem angegebenen Data Lake Store-Konto eine Regel für das virtuelle Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1860">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="98bd2-1861">Set-AzDataLakeStoreVirtualNetworkRule: Ändert die angegebene Regel für das virtuelle Netzwerk in das angegebene Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1861">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="98bd2-1862">Remove-AzDataLakeStoreVirtualNetworkRule: Dient zum Löschen der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1862">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="98bd2-1863">Az.Network</span><span class="sxs-lookup"><span data-stu-id="98bd2-1863">Az.Network</span></span>
* <span data-ttu-id="98bd2-1864">Cmdlet „Test-AzNetworkWatcherConnectivity“ aktualisiert, Protokollwert wird jetzt an Back-End übergeben.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1864">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="98bd2-1865">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1865">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="98bd2-1866">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="98bd2-1866">Az.Resources</span></span>
* <span data-ttu-id="98bd2-1867">Problem behoben, aufgrund dessen „Get-AzRoleDefinition“ eine unverständliche Ausnahme auslöst (wenn das Standardprofil kein Abonnement enthält und kein Bereich festgelegt ist), indem im Szenario eine aussagekräftige Ausnahme hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1867">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="98bd2-1868">Außerdem wurde der Standardparametersatz auf „RoleDefinitionNameParameterSet“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1868">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="98bd2-1869">0.3.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="98bd2-1869">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="98bd2-1870">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="98bd2-1870">Azure.Storage</span></span>
* <span data-ttu-id="98bd2-1871">Fehler beim Kopieren von Blobs/Dateien behoben, aufgrund dessen bei einem Metadatenproblem des Ziels keine Metadaten kopiert wurden</span><span class="sxs-lookup"><span data-stu-id="98bd2-1871">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="98bd2-1872">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="98bd2-1872">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="98bd2-1873">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="98bd2-1873">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="98bd2-1874">Der Abruf der Speicherressourcennutzung eines bestimmten Standorts wird jetzt unterstützt, und das Hinzufügen einer Warnmeldung für den Abruf der globalen Speicherressourcennutzung ist überflüssig.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1874">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="98bd2-1875">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="98bd2-1875">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="98bd2-1876">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="98bd2-1876">Az.CognitiveServices</span></span>
* <span data-ttu-id="98bd2-1877">„Get-AzCognitiveServicesAccountSkus“ wird ohne vorhandenes Konto unterstützt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1877">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="98bd2-1878">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="98bd2-1878">Az.Compute</span></span>
* <span data-ttu-id="98bd2-1879">Korrektur von „Get-AzVM -ResourceGroupName <rg>“, sodass ggf. mehr als 50 Ergebnisse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="98bd2-1879">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="98bd2-1880">Der Cmdlet-Hilfe zu „New-AzVmss“ wurde ein Beispiel für „SimpleParameterSet“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1880">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="98bd2-1881">Tippfehler in der Azure Disk Encryption-Statusmeldung behoben</span><span class="sxs-lookup"><span data-stu-id="98bd2-1881">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="98bd2-1882">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="98bd2-1882">Az.DataFactoryV2</span></span>
* <span data-ttu-id="98bd2-1883">Die Version des ADF .Net-SDK wurde auf 2.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1883">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="98bd2-1884">Az.Network</span><span class="sxs-lookup"><span data-stu-id="98bd2-1884">Az.Network</span></span>
* <span data-ttu-id="98bd2-1885">NetworkProfile-Funktionalität wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1885">Added NetworkProfile functionality.</span></span> <span data-ttu-id="98bd2-1886">Neue Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1886">new cmdlets added</span></span>
    - <span data-ttu-id="98bd2-1887">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="98bd2-1887">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="98bd2-1888">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="98bd2-1888">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="98bd2-1889">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="98bd2-1889">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="98bd2-1890">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="98bd2-1890">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="98bd2-1891">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="98bd2-1891">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="98bd2-1892">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="98bd2-1892">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="98bd2-1893">Dienstzuordnungslink in Subnetzmodell hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1893">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="98bd2-1894">Cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1894">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="98bd2-1895">Cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1895">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="98bd2-1896">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="98bd2-1896">Az.RedisCache</span></span>
* <span data-ttu-id="98bd2-1897">Künftig sind beliebige Zeichenfolgen als Größenparameter zulässig.</span><span class="sxs-lookup"><span data-stu-id="98bd2-1897">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="98bd2-1898">P5 in Popup „PSArgumentCompleter“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1898">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="98bd2-1899">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="98bd2-1899">Az.Resources</span></span>
* <span data-ttu-id="98bd2-1900">Fehlender Parameter „-Mode“ zu „Set-AzPolicyDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="98bd2-1900">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="98bd2-1901">Cmdlet-Fehler bei „Get-AzProviderOperation“ für Vorgänge mit Ursprung behoben, der den Benutzer enthält</span><span class="sxs-lookup"><span data-stu-id="98bd2-1901">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="98bd2-1902">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="98bd2-1902">Az.Sql</span></span>
* <span data-ttu-id="98bd2-1903">Problem behoben, aufgrund dessen einige Sicherungs-Cmdlets das aktuelle Azure-Abonnements nicht erkannt haben</span><span class="sxs-lookup"><span data-stu-id="98bd2-1903">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="98bd2-1904">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="98bd2-1904">Az.Websites</span></span>
* <span data-ttu-id="98bd2-1905">Neues Cmdlet „Get-AzWebAppContainerContinuousDeploymentUrl“ zum Abrufen der Webhook-URL von Continuous Deployment für Container</span><span class="sxs-lookup"><span data-stu-id="98bd2-1905">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="98bd2-1906">Neue Cmdlets „New-AzWebAppContainerPSSession“ und „Enter-WebAppContainerPSSession“ zum Initiieren einer PowerShell-Remotesitzung in einer Windows-Container-App</span><span class="sxs-lookup"><span data-stu-id="98bd2-1906">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="98bd2-1907">0.2.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="98bd2-1907">0.2.0 - September 2018</span></span>
 <span data-ttu-id="98bd2-1908">Erstrelease</span><span class="sxs-lookup"><span data-stu-id="98bd2-1908">Initial Release</span></span>
