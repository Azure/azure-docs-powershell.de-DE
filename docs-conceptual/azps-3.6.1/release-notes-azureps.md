---
title: Versionshinweise zu Azure PowerShell
description: Hier erfahren Sie mehr über die aktuellen Updates für die Azure PowerShell-Module.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/09/2020
ms.openlocfilehash: 4c7ea19a225d63307ecf4a6fe5ebfa14ccd78d7e
ms.sourcegitcommit: f6fa6543be1e0f6330b1598f01528b2928cc426c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2020
ms.locfileid: "79036160"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="936ed-103">Versionshinweise zu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="936ed-103">Azure PowerShell release notes</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="936ed-104">3.6.1 – März 2020</span><span class="sxs-lookup"><span data-stu-id="936ed-104">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="936ed-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="936ed-105">Az.Accounts</span></span>
* <span data-ttu-id="936ed-106">Öffnen der Azure PowerShell-Umfrageseite in „Send-Feedback“ [#11020]</span><span class="sxs-lookup"><span data-stu-id="936ed-106">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="936ed-107">Anzeigen der Azure PowerShell-Umfrage-URL in „Resolve-Error“ [#11021]</span><span class="sxs-lookup"><span data-stu-id="936ed-107">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="936ed-108">Az-Version in UserAgent hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-108">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="936ed-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="936ed-109">Az.ApiManagement</span></span>
* <span data-ttu-id="936ed-110">Unterstützung für das Abrufen und Konfigurieren einer benutzerdefinierten Domäne auf dem DeveloperPortal-Endpunkt hinzugefügt [#11007]</span><span class="sxs-lookup"><span data-stu-id="936ed-110">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="936ed-111">„Export-AzApiManagementApi“: Unterstützung für das Herunterladen der API-Definition im JSON-Format hinzugefügt [#9987]</span><span class="sxs-lookup"><span data-stu-id="936ed-111">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="936ed-112">„Import-AzApiManagementApi“: Unterstützung für das Importieren der OpenApi 3.0-Definition aus JSON-Dokument hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-112">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="936ed-113">„New-AzApiManagementIdentityProvider“ und „Set-AzApiManagementIdentityProvider“: Unterstützung für das Konfigurieren des Anmeldemandanten für AAD B2C-Anbieter hinzugefügt [#9784]</span><span class="sxs-lookup"><span data-stu-id="936ed-113">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="936ed-114">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="936ed-114">Az.DataLakeStore</span></span>
* <span data-ttu-id="936ed-115">Verweis auf System.Buffers in csproj und psd1 explizit hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-115">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="936ed-116">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="936ed-116">Az.IotHub</span></span>
* <span data-ttu-id="936ed-117">Unterstützung für die Verwaltung von Geräten in IoT Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-117">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="936ed-118">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="936ed-118">New Cmdlets are:</span></span>
    - <span data-ttu-id="936ed-119">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="936ed-119">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="936ed-120">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="936ed-120">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="936ed-121">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="936ed-121">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="936ed-122">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="936ed-122">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="936ed-123">Unterstützung für die Verwaltung von Modulen auf einem IoT-Zielgerät in einem IoT-Hub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-123">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="936ed-124">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="936ed-124">New Cmdlets are:</span></span>
    - <span data-ttu-id="936ed-125">„Add-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="936ed-125">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="936ed-126">„Get-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="936ed-126">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="936ed-127">„Remove-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="936ed-127">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="936ed-128">„Set-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="936ed-128">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="936ed-129">Cmdlet zum Abrufen der Verbindungszeichenfolge eines IoT-Zielgeräts in einem IoT-Hub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-129">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="936ed-130">Cmdlet zum Abrufen der Verbindungszeichenfolge eines Moduls auf einem IoT-Zielgerät in einem IoT-Hub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-130">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="936ed-131">Unterstützung für das Abrufen/Festlegen des übergeordneten Geräts eines IoT-Geräts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-131">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="936ed-132">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="936ed-132">New Cmdlets are:</span></span>
    - <span data-ttu-id="936ed-133">„Get-AzIotHubDeviceParent“</span><span class="sxs-lookup"><span data-stu-id="936ed-133">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="936ed-134">„Set-AzIotHubDeviceParent“</span><span class="sxs-lookup"><span data-stu-id="936ed-134">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="936ed-135">Unterstützung für die Verwaltung der Beziehung zwischen über- und untergeordneten Geräten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-135">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="936ed-136">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="936ed-136">Az.Monitor</span></span>
* <span data-ttu-id="936ed-137">Ausgabewert für „Get-AzMetricDefinition“ korrigiert [#9714]</span><span class="sxs-lookup"><span data-stu-id="936ed-137">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="936ed-138">Az.Network</span><span class="sxs-lookup"><span data-stu-id="936ed-138">Az.Network</span></span>
* <span data-ttu-id="936ed-139">SQL Management SDK aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="936ed-139">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="936ed-140">Es wurde ein Problem mit dem Namensunterschied in der PrivateLinkServiceConnectionState-Klasse behoben.</span><span class="sxs-lookup"><span data-stu-id="936ed-140">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="936ed-141">Zuordnung des Felds „ActionsRequired“ zu „ActionRequired“.</span><span class="sxs-lookup"><span data-stu-id="936ed-141">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="936ed-142">PublicNetworkAccess zu „New-AzSqlServer“ und „Set-AzSqlServer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-142">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="936ed-143">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="936ed-143">Az.Resources</span></span>
* <span data-ttu-id="936ed-144">Für Nullverweisfehler in „Get-AzRoleAssignment“ behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-144">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="936ed-145">Switch „-Force“ und „-PassThru“ in „Remove-AzADGroup“ als optional gekennzeichnet [#10849]</span><span class="sxs-lookup"><span data-stu-id="936ed-145">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="936ed-146">Problem behoben, dass „MailNickname“ nicht zurückgegeben wird, in „Remove-AzADGroup“ behoben [#11167]</span><span class="sxs-lookup"><span data-stu-id="936ed-146">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="936ed-147">Problem behoben, dass Pipe-Vorgang „Remove-AzADGroup“ nicht funktioniert [#11171]</span><span class="sxs-lookup"><span data-stu-id="936ed-147">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="936ed-148">Für Nullverweisfehler in GetAzureRoleAssignmentCommand behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-148">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="936ed-149">Breaking Change-Attribute für bevorstehende Änderungen an Richtlinien-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-149">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="936ed-150">„Get-AzResourceGroup“ aktualisiert, sodass jetzt serverseitig nach Ressourcengruppentags gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="936ed-150">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="936ed-151">Tag-Cmdlets so erweitert, dass „-ResourceId“ akzeptiert wird</span><span class="sxs-lookup"><span data-stu-id="936ed-151">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="936ed-152">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="936ed-152">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="936ed-153">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="936ed-153">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="936ed-154">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="936ed-154">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="936ed-155">Neues Tag-Cmdlet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-155">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="936ed-156">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="936ed-156">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="936ed-157">ScopedDeployment aus SDK 3.3.0 übernommen</span><span class="sxs-lookup"><span data-stu-id="936ed-157">Brought ScopedDeployment from SDK 3.3.0</span></span> 

#### <a name="azsql"></a><span data-ttu-id="936ed-158">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="936ed-158">Az.Sql</span></span>
* <span data-ttu-id="936ed-159">Publicnetworkaccess wurde "New-azsqlserver" und "Set-azsqlserver" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-159">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="936ed-160">Unterstützung für die Konfiguration der Sicherung der Langzeitaufbewahrung für verwaltete Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-160">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="936ed-161">Einrichten/Festlegen der LTR-Richtlinie für eine verwaltete Datenbank</span><span class="sxs-lookup"><span data-stu-id="936ed-161">Get/Set LTR policy on a managed database</span></span> 
    - <span data-ttu-id="936ed-162">Abrufen von Sicherungen nach verwalteter Datenbank, verwalteter Instanz oder nach Speicherort</span><span class="sxs-lookup"><span data-stu-id="936ed-162">Get LTR backup(s) by managed database, managed instance, or by location</span></span> 
    - <span data-ttu-id="936ed-163">Entfernen einer LTR-Sicherung</span><span class="sxs-lookup"><span data-stu-id="936ed-163">Remove an LTR backup</span></span> 
    - <span data-ttu-id="936ed-164">Wiederherstellen einer LTR-Sicherung zum Erstellen einer neuen verwalteten Datenbank</span><span class="sxs-lookup"><span data-stu-id="936ed-164">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="936ed-165">MinimalTlsVersion wurde zu New-AzSqlServer und Set-AzSqlServer hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-165">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="936ed-166">MinimalTlsVersion wurde zu New-AzSqlInstance und Set-AzSqlInstance hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-166">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="936ed-167">SQL SDK-Version für Az.Network festgelegt</span><span class="sxs-lookup"><span data-stu-id="936ed-167">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="936ed-168">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="936ed-168">Az.Storage</span></span>
* <span data-ttu-id="936ed-169">Unterstützung von AllowProtectedAppendWrite in ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="936ed-169">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="936ed-170">„Set-AzRmStorageContainerImmutabilityPolicy“</span><span class="sxs-lookup"><span data-stu-id="936ed-170">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="936ed-171">Warnmeldung für Breaking Change hinzugefügt: Typänderung für „AzureStorageTable“ in einer zukünftigen Version</span><span class="sxs-lookup"><span data-stu-id="936ed-171">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="936ed-172">„New-AzStorageTable“</span><span class="sxs-lookup"><span data-stu-id="936ed-172">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="936ed-173">„Get-AzStorageTable“</span><span class="sxs-lookup"><span data-stu-id="936ed-173">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="936ed-174">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="936ed-174">Az.Websites</span></span>
* <span data-ttu-id="936ed-175">Tag-Parameter für „New-AzAppServicePlan“ und „Set-AzAppServicePlan“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-175">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="936ed-176">Beenden der Cmdlet-Ausführung, wenn beim Hinzufügen einer benutzerdefinierten Domäne zu einer Website eine Ausnahme ausgelöst wird</span><span class="sxs-lookup"><span data-stu-id="936ed-176">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="936ed-177">Unterstützung zur Durchführung von Vorgängen für App Services hinzugefügt, die sich nicht in der gleichen Ressourcengruppe wie der App Service-Plan befinden</span><span class="sxs-lookup"><span data-stu-id="936ed-177">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="936ed-178">Zugriffseinschränkung auf WebApp/Funktion in verschiedenen Ressourcengruppen angewendet</span><span class="sxs-lookup"><span data-stu-id="936ed-178">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="936ed-179">Problem beim Festlegen von benutzerdefinierten Hostnamen für WebAppSlots behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-179">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="936ed-180">3.5.0: Februar 2020</span><span class="sxs-lookup"><span data-stu-id="936ed-180">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="936ed-181">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="936ed-181">Highlights since the last major release</span></span>
* <span data-ttu-id="936ed-182">Clientseitige Telemetrie aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-182">Updated client side telemetry.</span></span>
* <span data-ttu-id="936ed-183">Cmdlets zur Unterstützung der Geräteverwaltung in Az.IotHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-183">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="936ed-184">Cmdlets für Verfügbarkeitsgruppenlistener in Az.SqlVirtualMachine hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-184">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="936ed-185">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="936ed-185">Az.Accounts</span></span>
* <span data-ttu-id="936ed-186">Abonnement-ID, Mandanten-ID und Ausführungszeit in clientseitigen Telemetriedaten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-186">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="936ed-187">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="936ed-187">Az.Automation</span></span>
* <span data-ttu-id="936ed-188">Tippfehler in Beispiel 1 in der Referenzdokumentation für „New-AzAutomationSoftwareUpdateConfiguration“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-188">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="936ed-189">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="936ed-189">Az.CognitiveServices</span></span>
* <span data-ttu-id="936ed-190">SDK auf 7.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-190">Updated SDK to 7.0</span></span>
* <span data-ttu-id="936ed-191">Verbesserte Fehlermeldung, wenn der Server mit leerem Text antwortet</span><span class="sxs-lookup"><span data-stu-id="936ed-191">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="936ed-192">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="936ed-192">Az.Compute</span></span>
* <span data-ttu-id="936ed-193">Zulässiger leerer Wert für „ProximityPlacementGroupId“ während des Updates</span><span class="sxs-lookup"><span data-stu-id="936ed-193">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="936ed-194">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="936ed-194">Az.FrontDoor</span></span>
* <span data-ttu-id="936ed-195">Cmdlet zum Abrufen verwalteter Regeldefinitionen hinzugefügt, die in WAF verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="936ed-195">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="936ed-196">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="936ed-196">Az.IotHub</span></span>
* <span data-ttu-id="936ed-197">Unterstützung für die Verwaltung von Geräten in IoT Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-197">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="936ed-198">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="936ed-198">New Cmdlets are:</span></span>
    - <span data-ttu-id="936ed-199">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="936ed-199">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="936ed-200">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="936ed-200">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="936ed-201">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="936ed-201">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="936ed-202">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="936ed-202">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="936ed-203">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="936ed-203">Az.KeyVault</span></span>
* <span data-ttu-id="936ed-204">Duplizierter Text für „Add-AzKeyVaultKey.md“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-204">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="936ed-205">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="936ed-205">Az.Monitor</span></span>
* <span data-ttu-id="936ed-206">Beschreibung des Cmdlets „Get-AzLog cmdlet“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-206">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="936ed-207">Dem Befehl „New-AzMetricAlertRuleV2“ wurde ein Parameter namens „ActionGroupId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-207">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="936ed-208">Der Benutzer kann entweder „ActionGroupId(string)“ oder „ActionGorup(ActivityLogAlertActionGroup)“ angeben.</span><span class="sxs-lookup"><span data-stu-id="936ed-208">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="936ed-209">Az.Network</span><span class="sxs-lookup"><span data-stu-id="936ed-209">Az.Network</span></span>
* <span data-ttu-id="936ed-210">Zusätzlicher Parameterhinweis für den Parameter „-EnableProxyProtocol“ für das Cmdlet „New-AzPrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-210">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="936ed-211">FilterData-Beispiel in „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-211">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="936ed-212">Paketerfassungsbeispiel für die Erfassung aller inneren und äußeren Pakete in „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-212">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="936ed-213">Unterstützte Azure Firewall-Richtlinie für VNET-Firewalls</span><span class="sxs-lookup"><span data-stu-id="936ed-213">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="936ed-214">Keine neuen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-214">No new cmdlets are added.</span></span> <span data-ttu-id="936ed-215">Die Einschränkung für die Firewallrichtlinie für VNET-Firewalls wurde gelockert.</span><span class="sxs-lookup"><span data-stu-id="936ed-215">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="936ed-216">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="936ed-216">Az.RecoveryServices</span></span>
* <span data-ttu-id="936ed-217">Unterstützung für „Als Dateien wiederherstellen“ für SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-217">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="936ed-218">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="936ed-218">Az.Resources</span></span>
* <span data-ttu-id="936ed-219">Cmdlets für die Vorlagenbereitstellung umgestaltet</span><span class="sxs-lookup"><span data-stu-id="936ed-219">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="936ed-220">Neue Cmdlets zur Verwaltung von Bereitstellungen in der Verwaltungsgruppe hinzugefügt: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="936ed-220">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="936ed-221">Neue Cmdlets zur Verwaltung von Bereitstellungen im Mandantenbereich hinzugefügt: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="936ed-221">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="936ed-222">Cmdlets vom Typ „\*-AzDeployment“ für den speziellen Einsatz im Abonnementbereich umgestaltet</span><span class="sxs-lookup"><span data-stu-id="936ed-222">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="936ed-223">Aliase vom Typ „*-AzSubscriptionDeployment“ für Cmdlets vom Typ „*-AzDeployment“ erstellt</span><span class="sxs-lookup"><span data-stu-id="936ed-223">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="936ed-224">„Update-AzADApplication“ korrigiert, wenn der Parameter „AvailableToOtherTenants“ nicht festgelegt wird</span><span class="sxs-lookup"><span data-stu-id="936ed-224">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="936ed-225">„ApplicationObjectWithoutCredentialParameterSet“ entfernt, um „AmbiguousParameterSetException“ zu vermeiden</span><span class="sxs-lookup"><span data-stu-id="936ed-225">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="936ed-226">Hilfedateien erneut generiert</span><span class="sxs-lookup"><span data-stu-id="936ed-226">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="936ed-227">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="936ed-227">Az.Sql</span></span>
* <span data-ttu-id="936ed-228">Unterstützung für abonnementübergreifende Point-in-Time-Wiederherstellung für verwaltete Instanzen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-228">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="936ed-229">Unterstützung für die Änderung der Hardwaregeneration von vorhandenen verwalteten SQL-Instanzen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-229">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="936ed-230">Hilfebeispiele für „Update-AzSqlServerVulnerabilityAssessmentSetting“ korrigiert: parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="936ed-230">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="936ed-231">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="936ed-231">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="936ed-232">Cmdlets für Verfügbarkeitsgruppenlistener hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-232">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="936ed-233">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="936ed-233">Az.StorageSync</span></span>
* <span data-ttu-id="936ed-234">Unterstützte Zeichensätze in „Invoke-AzStorageSyncCompatibilityCheck“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-234">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="936ed-235">3.4.0: Februar 2020</span><span class="sxs-lookup"><span data-stu-id="936ed-235">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="936ed-236">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="936ed-236">Highlights since the last major release</span></span>
* <span data-ttu-id="936ed-237">Az.CosmosDB: erste Version 0.1.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="936ed-237">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="936ed-238">Unterstützung für Az.Network ConnectionMonitor V2 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-238">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="936ed-239">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="936ed-239">Az.Accounts</span></span>
* <span data-ttu-id="936ed-240">Deaktivieren der automatischen Kontextspeicherung, wenn „AzureRmContext.json“ nicht verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="936ed-240">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="936ed-241">Aktualisieren des Verweises auf Azure Powershell Common auf 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="936ed-241">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="936ed-242">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="936ed-242">Az.ApiManagement</span></span>
* <span data-ttu-id="936ed-243">**Get-AzApiManagementApiSchema** Fehler beim Abrufen des einer API zugeordneten Open-Api-Schemas behoben   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="936ed-243">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="936ed-244">**New-AzApiManagementProduct**\* und **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="936ed-244">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="936ed-245">Dokumentation korrigiert für https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="936ed-245">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="936ed-246">**Set-AzApiManagementApi** Beispiel hinzugefügt, das das Aktualisieren von ServiceUrl mithilfe des Cmdlets veranschaulicht</span><span class="sxs-lookup"><span data-stu-id="936ed-246">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="936ed-247">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="936ed-247">Az.Compute</span></span>
* <span data-ttu-id="936ed-248">Anzahl des VM-Status auf 100 beschränkt, um die Drosselung zu vermeiden, wenn „Get-AzVM -Status“ ohne VM-Name ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="936ed-248">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="936ed-249">Cmdlet „Update-AzDiskEncryptionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-249">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="936ed-250">Die Parameter „EncryptionType“ und „DiskEncryptionSetId“ wurden den folgenden Cmdlets hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="936ed-250">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="936ed-251">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="936ed-251">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="936ed-252">Parameter „ColocationStatus“ zum Cmdlet „Get-AzProximityPlacementGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-252">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="936ed-253">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="936ed-253">Az.DataFactory</span></span>
* <span data-ttu-id="936ed-254">Version des ADF .NET SDK auf 4.7.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-254">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="936ed-255">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="936ed-255">Az.DeploymentManager</span></span>
* <span data-ttu-id="936ed-256">LIST-Vorgänge für Ressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-256">Adds LIST operations for resources</span></span>
* <span data-ttu-id="936ed-257">Funktionen zum Ausführen von Vorgängen für Integritätsprüfungsschritte hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-257">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="936ed-258">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="936ed-258">Az.HDInsight</span></span>
* <span data-ttu-id="936ed-259">Dokumentationsfehler für „New-AzHDInsightCluster“ behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-259">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="936ed-260">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="936ed-260">Az.KeyVault</span></span>
* <span data-ttu-id="936ed-261">Namensalias zum VaultName-Attribut hinzugefügt, um „Remove-AzureKeyVault“ mit „New-AzureKeyVault“ konsistent zu machen</span><span class="sxs-lookup"><span data-stu-id="936ed-261">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="936ed-262">Az.Network</span><span class="sxs-lookup"><span data-stu-id="936ed-262">Az.Network</span></span>
* <span data-ttu-id="936ed-263">Neues Beispiel zu „Set-AzNetworkWatcherConfigFlowLog.md“ hinzugefügt, um das Szenario zur Traffic Analytics-Deaktivierung zu veranschaulichen</span><span class="sxs-lookup"><span data-stu-id="936ed-263">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="936ed-264">Unterstützung für die Zuweisung der IP-Verwaltungskonfiguration zu Azure Firewall hinzugefügt: ein dediziertes Subnetz und eine öffentliche IP-Adresse, die von der Firewall für den Verwaltungsdatenverkehr verwendet werden</span><span class="sxs-lookup"><span data-stu-id="936ed-264">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="936ed-265">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="936ed-265">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="936ed-266">Parameter „-ManagementPublicIpAddress“ (nicht obligatorisch) hinzugefügt, der ein Objekt für die öffentliche IP-Adresse akzeptiert</span><span class="sxs-lookup"><span data-stu-id="936ed-266">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="936ed-267">Methode „SetManagementIpConfiguration“ für Firewallobjekt hinzugefügt. Erfordert ein Subnetz und eine öffentliche IP-Adresse als Eingabe, und der Subnetzname muss „AzureFirewallManagementSubnet“ lauten.</span><span class="sxs-lookup"><span data-stu-id="936ed-267">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="936ed-268">Beispiele für „Get-AzNetworkSecurityGroup“ korrigiert, um Beispiele für Netzwerksicherheitsgruppen und nicht für Netzwerkschnittstellen anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="936ed-268">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="936ed-269">Tippfehler im Befehl „New-AzVpnSite“ korrigiert, der dazu führte, dass die Vervollständigung für die Ressourcen-ID einen Parameter nicht vervollständigen konnte</span><span class="sxs-lookup"><span data-stu-id="936ed-269">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="936ed-270">Unterstützung für die URL-Konfiguration im Aktionssatz für Neuschreibungsregeln in Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-270">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="936ed-271">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="936ed-271">New cmdlets added:</span></span>
        - <span data-ttu-id="936ed-272">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="936ed-272">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="936ed-273">Cmdlets mit optionalem Parameter aktualisiert: UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="936ed-273">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="936ed-274">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="936ed-274">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="936ed-275">Unterstützung für Ressourcen der Version 2 von NetworkWatcher ConnectionMonitor hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-275">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="936ed-276">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="936ed-276">Az.PolicyInsights</span></span>
* <span data-ttu-id="936ed-277">Unterstützung der Konformitätsbewertung vor der Ermittlung der zu korrigierenden Ressourcen</span><span class="sxs-lookup"><span data-stu-id="936ed-277">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="936ed-278">Parameter „-ResourceDiscoverMode“ zu „Start-AzPolicyRemediation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-278">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="936ed-279">Cmdlet „Get-AzPolicyMetadata“ zum Abrufen der Ressourcen für Richtlinienmetadaten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-279">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="936ed-280">„Get-AzPolicyState“ und „Get-AzPolicyStateSummary“ für API-Version 2019-10-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-280">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="936ed-281">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="936ed-281">Az.RecoveryServices</span></span>
* <span data-ttu-id="936ed-282">Azure Site Recovery-Unterstützung für das Entfernen eines replizierten Datenträgers</span><span class="sxs-lookup"><span data-stu-id="936ed-282">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="936ed-283">In Azure Backup wurde Unterstützung zum Hinzufügen von Tags bei der Erstellung eines Recovery Services-Tresors hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-283">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="936ed-284">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="936ed-284">Az.Resources</span></span>
* <span data-ttu-id="936ed-285">„-Scope“ in Cmdlets vom Typ „\*-AzPolicyAssignment“ nun optional (standardmäßig auf Abonnementkontext festgelegt)</span><span class="sxs-lookup"><span data-stu-id="936ed-285">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="936ed-286">Beispiele zum Erstellen von „ADServicePrincipal“ mit Kennwort und Schlüsselanmeldeinformation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-286">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="936ed-287">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="936ed-287">Az.Sql</span></span>
<span data-ttu-id="936ed-288">Cmdlet „New-AzSqlDatabaseSecondary“ korrigiert, um auf die Existenz von „PartnerDatabaseName“ anstelle von „DatabaseName“ zu prüfen</span><span class="sxs-lookup"><span data-stu-id="936ed-288">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="936ed-289">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="936ed-289">Az.Storage</span></span>
* <span data-ttu-id="936ed-290">Unterstützung für das Festlegen des Schlüsseltyps für die Tabellen-/Warteschlangenverschlüsselung beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="936ed-290">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="936ed-291">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="936ed-291">New-AzStorageAccount</span></span>
* <span data-ttu-id="936ed-292">Anzeigen der Anforderungs-ID (RequestId), wenn für „StorageException“ keine erweiterten Fehlerinformationen (ExtendedErrorInformation) vorliegen</span><span class="sxs-lookup"><span data-stu-id="936ed-292">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="936ed-293">Beispiel 6 des Cmdlets „Start-AzStorageBlobCopy“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-293">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="936ed-294">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="936ed-294">Az.Websites</span></span>
* <span data-ttu-id="936ed-295">„Set-AzWebapp“ und „Set-AzWebappSlot“ unterstützen die Eigenschaften „AlwaysOn“, „MinTls“ und „FtpsState“.</span><span class="sxs-lookup"><span data-stu-id="936ed-295">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="936ed-296">Problem behoben, das dazu führte, dass beim Festlegen von „HttpsOnly“ bei gleichzeitiger Änderung von „AppservicePlan“ mit dem einzelnen Befehl „Set-AzWebApp“ „HttpsOnly“ auf den Standardwert zurückgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="936ed-296">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="936ed-297">3.3.0 – Januar 2020</span><span class="sxs-lookup"><span data-stu-id="936ed-297">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="936ed-298">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="936ed-298">Az.Accounts</span></span>
* <span data-ttu-id="936ed-299">„Add-AzEnvironment“ und „Set-AzEnvironment“ wurden so aktualisiert, dass sie jetzt die Parameter „AzureAttestationServiceEndpointResourceId“ und „AzureAttestationServiceEndpointSuffix“ akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="936ed-299">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="936ed-300">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="936ed-300">Az.Cdn</span></span>
* <span data-ttu-id="936ed-301">Anzeigen von Fehlerantwortdetails im Cmdlet „New-AzCdnEndpoint“</span><span class="sxs-lookup"><span data-stu-id="936ed-301">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="936ed-302">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="936ed-302">Az.Compute</span></span>
* <span data-ttu-id="936ed-303">Cmdlet „Set-AzVMCustomScriptExtension“ für eine VM mit verwaltetem Betriebssystemdatenträger ohne Betriebssystemprofil wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="936ed-303">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="936ed-304">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="936ed-304">Az.ContainerInstance</span></span>
* <span data-ttu-id="936ed-305">Im Beispiel von „New-AzContainerGroup“ verwendete Parameternamen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="936ed-305">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="936ed-306">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="936ed-306">Az.DataBoxEdge</span></span>
* <span data-ttu-id="936ed-307">Cmdlet „Get-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-307">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="936ed-308">Edge-Speichercontainer abrufen</span><span class="sxs-lookup"><span data-stu-id="936ed-308">Get the Edge Storage Container</span></span>
* <span data-ttu-id="936ed-309">Cmdlet „New-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-309">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="936ed-310">Neuen Edge-Speichercontainer erstellen</span><span class="sxs-lookup"><span data-stu-id="936ed-310">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="936ed-311">Cmdlet „Remove-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-311">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="936ed-312">Edge-Speichercontainer entfernen</span><span class="sxs-lookup"><span data-stu-id="936ed-312">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="936ed-313">Cmdlet „Invoke-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-313">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="936ed-314">Aktion zum Aktualisieren von Daten in Edge-Speichercontainer aufrufen</span><span class="sxs-lookup"><span data-stu-id="936ed-314">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="936ed-315">Cmdlet „Get-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-315">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="936ed-316">Edge-Speicherkonto abrufen</span><span class="sxs-lookup"><span data-stu-id="936ed-316">Get the Edge Storage Account</span></span>
* <span data-ttu-id="936ed-317">Cmdlet „New-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-317">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="936ed-318">Neues Edge-Speicherkonto erstellen</span><span class="sxs-lookup"><span data-stu-id="936ed-318">Create new Edge Storage Account</span></span>
* <span data-ttu-id="936ed-319">Cmdlet „Remove-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-319">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="936ed-320">Edge-Speicherkonto entfernen</span><span class="sxs-lookup"><span data-stu-id="936ed-320">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="936ed-321">Cmdlet „Invoke-AzDataBoxEdgeShare“ aufrufen</span><span class="sxs-lookup"><span data-stu-id="936ed-321">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="936ed-322">Aktion zum Aktualisieren von Daten auf Freigabe aufrufen</span><span class="sxs-lookup"><span data-stu-id="936ed-322">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="936ed-323">Cmdlet „Set-AzDataBoxEdgeStorageAccountCredential“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-323">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="936ed-324">Festlegen der Speicherkonto-Anmeldeinformationen für „az databoxedge“</span><span class="sxs-lookup"><span data-stu-id="936ed-324">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="936ed-325">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="936ed-325">Az.DataFactory</span></span>
* <span data-ttu-id="936ed-326">Eigenschaften „AutoUpdateETA“, „LatestVersion“, „PushedVersion“, „TaskQueueId“ und „VersionStatus“ für Befehl „Get-AzDataFactoryV2IntegrationRuntime“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-326">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="936ed-327">Version des ADF .NET SDK auf 4.6.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-327">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="936ed-328">Parameter „PublicIPs“ wurde für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um das Erstellen der Azure-SSIS Integration Runtime mit statischen öffentlichen IP-Adressen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="936ed-328">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="936ed-329">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="936ed-329">Az.DevTestLabs</span></span>
* <span data-ttu-id="936ed-330">Fehlerhafter Link in „Get-AzDtlAllowedVMSizesPolicy.md“ entfernt</span><span class="sxs-lookup"><span data-stu-id="936ed-330">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="936ed-331">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="936ed-331">Az.EventHub</span></span>
* <span data-ttu-id="936ed-332">Behebung des Problems 10634: Verweis auf NULL-Objekt für „remove eventhubnamespace“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-332">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="936ed-333">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="936ed-333">Az.HDInsight</span></span>
* <span data-ttu-id="936ed-334">Fehler in „Invoke-AzHDInsightHiveJob.md“ wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="936ed-334">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="936ed-335">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="936ed-335">Az.MachineLearning</span></span>
* <span data-ttu-id="936ed-336">Die folgenden Cmdlets wurden entfernt, da „MachineLearningCompute“ nicht mehr verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="936ed-336">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="936ed-337">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="936ed-337">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="936ed-338">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="936ed-338">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="936ed-339">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="936ed-339">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="936ed-340">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="936ed-340">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="936ed-341">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="936ed-341">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="936ed-342">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="936ed-342">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="936ed-343">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="936ed-343">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="936ed-344">Az.Network</span><span class="sxs-lookup"><span data-stu-id="936ed-344">Az.Network</span></span>
* <span data-ttu-id="936ed-345">Upgrade der Abhängigkeit von „Microsoft.Azure.Management.Sql“ von „1.36-preview“ auf „1.37-preview“</span><span class="sxs-lookup"><span data-stu-id="936ed-345">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="936ed-346">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="936ed-346">Az.RecoveryServices</span></span>
* <span data-ttu-id="936ed-347">Änderung der Azure Site Recovery-Unterstützung für virtuelle Computer mit verwalteten Datenträgern, die im Ruhezustand mit kundenseitig verwalteten Schlüsseln für Azure-zu-Azure-Anbieter verschlüsselt sind</span><span class="sxs-lookup"><span data-stu-id="936ed-347">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="936ed-348">Azure Site Recovery-Unterstützung für die Eingabe der ID des Datenträgerverschlüsselungssatzes als optionale Eingabe beim Aktivieren des Schutzes für VMware in Azure</span><span class="sxs-lookup"><span data-stu-id="936ed-348">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="936ed-349">Azure Site Recovery-Unterstützung für die Eingabe der ID des Datenträgerverschlüsselungssatzes als optionale Eingabe auf Datenträgerebene beim Aktivieren des Schutzes für VMware in Azure</span><span class="sxs-lookup"><span data-stu-id="936ed-349">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="936ed-350">Azure Site Recovery-Unterstützung zum Aktualisieren eines replikationsgeschützten Elements mit der Zuordnung eines Datenträgerverschlüsselungssatzes für HyperV in Azure</span><span class="sxs-lookup"><span data-stu-id="936ed-350">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="936ed-351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="936ed-351">Az.Resources</span></span>
* <span data-ttu-id="936ed-352">Fehler in Hilfedokument zu „Remove-AzTag“ behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-352">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="936ed-353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="936ed-353">Az.Sql</span></span>
* <span data-ttu-id="936ed-354">Funktionalität der Baseline-Cmdlets für einen Sicherheitsrisikobewertungssatz korrigiert, sodass sie auf der Master-Datenbank für Azure Database funktionieren und sie auf Systemdatenbanken von verwalteten Instanzen einschränken.</span><span class="sxs-lookup"><span data-stu-id="936ed-354">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="936ed-355">Fehler beim Erstellen einer SQL-Instanzfailovergruppe behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-355">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="936ed-356">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="936ed-356">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="936ed-357">DR als neuer gültiger Lizenztyp hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-357">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="936ed-358">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="936ed-358">Az.Storage</span></span>
* <span data-ttu-id="936ed-359">Warnmeldung für Breaking Change hinzugefügt: Wertänderung für „DefaultAction“ in einer zukünftigen Version</span><span class="sxs-lookup"><span data-stu-id="936ed-359">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="936ed-360">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="936ed-360">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="936ed-361">Unterstützung für das Abrufen der letzten Synchronisierungszeit des Speicherkontos durch Ausführen von „get-AzureRMStorageAccount“ mit Parameter „-IncludeGeoReplicationStats“</span><span class="sxs-lookup"><span data-stu-id="936ed-361">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span> 
    - <span data-ttu-id="936ed-362">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="936ed-362">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="936ed-363">3.2.0: Dezember 2019</span><span class="sxs-lookup"><span data-stu-id="936ed-363">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="936ed-364">Allgemein</span><span class="sxs-lookup"><span data-stu-id="936ed-364">General</span></span>
* <span data-ttu-id="936ed-365">Verweise in „.psd1“ zur Verwendung des relativen Pfads für alle Module aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-365">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="936ed-366">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="936ed-366">Az.Accounts</span></span>
* <span data-ttu-id="936ed-367">Richtiges UserAgent-Element für clientseitige Telemetrie für Az 4.0-Vorschauversion festgelegt</span><span class="sxs-lookup"><span data-stu-id="936ed-367">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="936ed-368">Anzeigen benutzerfreundlicher Fehlermeldungen, wenn der Kontext in der Az 4.0-Vorschauversion NULL ist</span><span class="sxs-lookup"><span data-stu-id="936ed-368">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="936ed-369">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="936ed-369">Az.Batch</span></span>
* <span data-ttu-id="936ed-370">Problem [#10602](https://github.com/Azure/azure-powershell/issues/10602) behoben, aufgrund dessen „VirtualMachineConfiguration.ContainerConfiguration“ oder „VirtualMachineConfiguration.DataDisks“ von **New-AzBatchPool** nicht ordnungsgemäß an den Server gesendet wurde</span><span class="sxs-lookup"><span data-stu-id="936ed-370">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="936ed-371">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="936ed-371">Az.DataFactory</span></span>
* <span data-ttu-id="936ed-372">Version des ADF .NET SDK auf 4.5.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-372">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="936ed-373">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="936ed-373">Az.FrontDoor</span></span>
* <span data-ttu-id="936ed-374">Unterstützung für den Ausschluss verwalteter WAF-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-374">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="936ed-375">SocketAddr zur automatischen Vervollständigung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-375">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="936ed-376">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="936ed-376">Az.HealthcareApis</span></span>
* <span data-ttu-id="936ed-377">Ausnahmebehandlung</span><span class="sxs-lookup"><span data-stu-id="936ed-377">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="936ed-378">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="936ed-378">Az.KeyVault</span></span>
* <span data-ttu-id="936ed-379">Fehler im Zusammenhang mit dem Zugriff auf einen möglicherweise nicht festgelegten Wert behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-379">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="936ed-380">Zertifikatverwaltung für Kryptografie für elliptische Kurve</span><span class="sxs-lookup"><span data-stu-id="936ed-380">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="936ed-381">Unterstützung zum Angeben der Kurve für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-381">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="936ed-382">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="936ed-382">Az.Monitor</span></span>
* <span data-ttu-id="936ed-383">Optionales Argument zum Befehl „Diagnoseeinstellungen hinzufügen“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-383">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="936ed-384">Ein Optionsargument, das angibt, dass der Export in Log Analytics ein festes Schema sein muss (auch bekannt als</span><span class="sxs-lookup"><span data-stu-id="936ed-384">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="936ed-385">dedizierter Datentyp)</span><span class="sxs-lookup"><span data-stu-id="936ed-385">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="936ed-386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="936ed-386">Az.Network</span></span>
* <span data-ttu-id="936ed-387">Unterstützung für IpGroups in der AzureFirewall-Anwendung sowie in NAT- und Netzwerkregeln</span><span class="sxs-lookup"><span data-stu-id="936ed-387">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="936ed-388">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="936ed-388">Az.Resources</span></span>
* <span data-ttu-id="936ed-389">Problem behoben, aufgrund dessen die Vorlagenbereitstellung einen Vorlagenparameter nicht lesen kann, wenn der Name einen Konflikt mit einem integrierten Parameternamen verursacht</span><span class="sxs-lookup"><span data-stu-id="936ed-389">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="936ed-390">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-09-01 aktualisiert, die Gruppierungsunterstützung in Richtliniensatzdefinitionen einführt</span><span class="sxs-lookup"><span data-stu-id="936ed-390">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="936ed-391">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="936ed-391">Az.Sql</span></span>
* <span data-ttu-id="936ed-392">Speichererstellung in automatischer Aktivierung der Sicherheitsrisikobewertung auf StorageV2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-392">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="936ed-393">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="936ed-393">Az.Storage</span></span>
* <span data-ttu-id="936ed-394">Unterstützung der Generierung blob-/containeridentitätsbasierter SAS-Token mit Speicherkontext auf der Grundlage der OAuth-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="936ed-394">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="936ed-395">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="936ed-395">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="936ed-396">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="936ed-396">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="936ed-397">Unterstützung für das Widerrufen von Schlüsseln für die Speicherkonto-Benutzerdelegierung hinzugefügt, sodass alle SAS-Identitätstoken widerrufen werden</span><span class="sxs-lookup"><span data-stu-id="936ed-397">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="936ed-398">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="936ed-398">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="936ed-399">Upgrade auf Microsoft.Azure.Management.Storage 14.2.0, um die neue API-Version 2019-06-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="936ed-399">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="936ed-400">Unterstützung von QuotaGiB (Freigabekontingent in Gibibyte) für Werte über 5120 in der Verwaltungsebene von Dateifreigabe-Cmdlets und Parameteralias „Quota“ zum Parameter „QuotaGiB“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-400">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span> 
    - <span data-ttu-id="936ed-401">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="936ed-401">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="936ed-402">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="936ed-402">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="936ed-403">Parameteralias „QuotaGiB“ zum Parameter „Quota“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-403">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="936ed-404">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="936ed-404">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="936ed-405">Problem behoben, dass „Set-AzStorageContainerAcl“ die gespeicherte Zugriffsrichtlinie bereinigen kann</span><span class="sxs-lookup"><span data-stu-id="936ed-405">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="936ed-406">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="936ed-406">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="936ed-407">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="936ed-407">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="936ed-408">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="936ed-408">Highlights since the last major release</span></span>
* <span data-ttu-id="936ed-409">Az.DataBoxEdge 1.0.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="936ed-409">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="936ed-410">Az.SqlVirtualMachine 1.0.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="936ed-410">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="936ed-411">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="936ed-411">Az.Compute</span></span>
* <span data-ttu-id="936ed-412">Funktion zum erneuten Anwenden von VMs</span><span class="sxs-lookup"><span data-stu-id="936ed-412">VM Reapply feature</span></span>
    - <span data-ttu-id="936ed-413">Parameter für erneutes Anwenden zu Cmdlet „Set-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-413">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="936ed-414">AutomaticRepairs-Funktion für VM-Skalierungsgruppe:</span><span class="sxs-lookup"><span data-stu-id="936ed-414">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="936ed-415">Parameter „EnableAutomaticRepair“, „AutomaticRepairGracePeriod“ und „AutomaticRepairMaxInstanceRepairsPercent“ zu folgenden Cmdlets hinzugefügt:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="936ed-415">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="936ed-416">Mandantenübergreifende Unterstützung von Katalogimages für „New-AzVM“</span><span class="sxs-lookup"><span data-stu-id="936ed-416">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="936ed-417">„Spot“ zu Argumentvervollständigung des Priority-Parameters in Cmdlets „New-AzVM“, „New-AzVMConfig“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-417">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="936ed-418">Parameter „DiskIOPSReadWrite“ und „DiskMBpsReadWrite“ zu Cmdlet „Add-AzVmssDataDisk“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-418">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="936ed-419">Parameter „SourceImageId“ von Cmdlet „New-AzGalleryImageVersion“ in optional geändert</span><span class="sxs-lookup"><span data-stu-id="936ed-419">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="936ed-420">Parameter „OSDiskImage“ und „DataDiskImage“ zu Cmdlet „New-AzGalleryImageVersion“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-420">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="936ed-421">Parameter „HyperVGeneration“ zu Cmdlet „New-AzGalleryImageDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-421">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="936ed-422">Parameter „SkipExtensionsOnOverprovisionedVMs“ zu Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-422">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="936ed-423">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="936ed-423">Az.DataBoxEdge</span></span>
* <span data-ttu-id="936ed-424">Cmdlet `Get-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-424">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="936ed-425">Bestellung abrufen</span><span class="sxs-lookup"><span data-stu-id="936ed-425">Get the Order</span></span>
* <span data-ttu-id="936ed-426">Cmdlet `New-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-426">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="936ed-427">Neue Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="936ed-427">Create new Order</span></span>
* <span data-ttu-id="936ed-428">Cmdlet `Remove-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-428">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="936ed-429">Bestellung entfernen</span><span class="sxs-lookup"><span data-stu-id="936ed-429">Remove the Order</span></span>
* <span data-ttu-id="936ed-430">Änderung im Cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="936ed-430">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="936ed-431">Erstellt jetzt eine lokale Freigabe</span><span class="sxs-lookup"><span data-stu-id="936ed-431">Now creates Local Share</span></span>
* <span data-ttu-id="936ed-432">Cmdlet `Set-AzDataBoxEdgeRole` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-432">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="936ed-433">„IotRole“ kann jetzt einer Freigabe zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="936ed-433">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="936ed-434">Cmdlet `Invoke-AzDataBoxEdgeDevice` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-434">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="936ed-435">Scanupdate aufrufen, Update herunterladen, Updates auf dem Gerät installieren</span><span class="sxs-lookup"><span data-stu-id="936ed-435">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="936ed-436">Cmdlet `Get-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-436">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="936ed-437">Ruft die Informationen zu Auslösern ab</span><span class="sxs-lookup"><span data-stu-id="936ed-437">Gets the information about Triggers</span></span>
* <span data-ttu-id="936ed-438">Cmdlet `New-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-438">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="936ed-439">Neue Auslöser erstellen</span><span class="sxs-lookup"><span data-stu-id="936ed-439">Create new Triggers</span></span>
* <span data-ttu-id="936ed-440">Cmdlet `Remove-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-440">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="936ed-441">Auslöser entfernen</span><span class="sxs-lookup"><span data-stu-id="936ed-441">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="936ed-442">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="936ed-442">Az.DataFactory</span></span>
* <span data-ttu-id="936ed-443">Version des ADF .NET SDK auf 4.4.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-443">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="936ed-444">Parameter „ExpressCustomSetup“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um Setupkonfigurationen und Drittanbieterkomponenten ohne benutzerdefiniertes Setupskript zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="936ed-444">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="936ed-445">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="936ed-445">Az.DataLakeStore</span></span>
* <span data-ttu-id="936ed-446">Dokumentation von „Get-AzDataLakeStoreDeletedItem“ und „Restore-AzDataLakeStoreDeletedItem“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-446">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="936ed-447">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="936ed-447">Az.EventHub</span></span>
* <span data-ttu-id="936ed-448">Behebung des Problems 10301: Datumsformat von SAS-Token korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-448">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="936ed-449">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="936ed-449">Az.FrontDoor</span></span>
* <span data-ttu-id="936ed-450">Parameter „MinimumTlsVersion“ zu „Enable-AzFrontDoorCustomDomainHttps“ und „New-AzFrontDoorFrontendEndpointObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-450">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="936ed-451">Parameter „HealthProbeMethod“ und „EnabledState“ zu „New-AzFrontDoorHealthProbeSettingObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-451">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="936ed-452">Neues Cmdlet zum Erstellen von BackendPoolsSettings-Objekten für die Übergabe in Erstellung/Update von Front Door hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-452">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="936ed-453">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="936ed-453">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="936ed-454">Az.Network</span><span class="sxs-lookup"><span data-stu-id="936ed-454">Az.Network</span></span>
* <span data-ttu-id="936ed-455">FilterData-Optionsbeispiele „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ geändert.</span><span class="sxs-lookup"><span data-stu-id="936ed-455">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="936ed-456">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="936ed-456">Az.PrivateDns</span></span>
* <span data-ttu-id="936ed-457">PrivateDns.net-SDK auf Version 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-457">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="936ed-458">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="936ed-458">Az.RecoveryServices</span></span>
* <span data-ttu-id="936ed-459">Azure Site Recovery-Unterstützung zum Auswählen des Datenträgertyps beim Aktivieren des Schutzes.</span><span class="sxs-lookup"><span data-stu-id="936ed-459">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="936ed-460">Fehlerbehebung bei Bearbeitungsaktion für Azure Site Recovery-Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="936ed-460">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="936ed-461">SQL-Wiederherstellungsunterstützung für Azure Backup zum Akzeptieren von Filestream-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="936ed-461">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="936ed-462">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="936ed-462">Az.RedisCache</span></span>
* <span data-ttu-id="936ed-463">Parameter „MinimumTlsVersion“ in Cmdlets „New-AzRedisCache“ und „Set-AzRedisCache“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-463">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="936ed-464">Außerdem „MinimumTlsVersion“ in Ausgabe von Cmdlet „Get-AzRedisCache“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-464">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="936ed-465">Validierung von Parameter „-Size“ für Cmdlets „Set-AzRedisCache“ und „New-AzRedisCache“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-465">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="936ed-466">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="936ed-466">Az.Resources</span></span>
- <span data-ttu-id="936ed-467">Richtlinien-Cmdlets aktualisiert, um die neue API-Version 2019-06-01 mit der neuen EnforcementMode-Eigenschaft bei der Richtlinienzuweisung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="936ed-467">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="936ed-468">Hilfebeispiel zum Erstellen von Richtliniendefinitionen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-468">Updated create policy definition help example</span></span>
- <span data-ttu-id="936ed-469">Fehlerkorrektur: „Remove-AZADServicePrincipal -ServicePrincipalName“ gibt Nullverweis aus, wenn Dienstprinzipalname nicht gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="936ed-469">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="936ed-470">Fehlerkorrektur: „New-AZADServicePrincipal“ gibt Nullverweis aus, wenn Mandant kein Abonnement hat.</span><span class="sxs-lookup"><span data-stu-id="936ed-470">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="936ed-471">„New-AzAdServicePrincipal“ geändert, um Anmeldeinformation nur zu zugeordneter Anwendung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="936ed-471">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="936ed-472">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="936ed-472">Az.Sql</span></span>
* <span data-ttu-id="936ed-473">Unterstützung von „ReadReplicaCount“ für Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-473">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="936ed-474">Korrektur von „Set-AzSqlDatabase“, wenn Zonenredundanz nicht festgelegt</span><span class="sxs-lookup"><span data-stu-id="936ed-474">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="936ed-475">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="936ed-475">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="936ed-476">Allgemein</span><span class="sxs-lookup"><span data-stu-id="936ed-476">General</span></span>
* <span data-ttu-id="936ed-477">Az.PrivateDns 1.0.0 veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="936ed-477">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="936ed-478">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="936ed-478">Az.Accounts</span></span>
* <span data-ttu-id="936ed-479">Hinweis zur Veraltung des Alias „Resolve-Error“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-479">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="936ed-480">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="936ed-480">Az.Advisor</span></span>
* <span data-ttu-id="936ed-481">Neue Kategorie „Operational Excellence“ für Cmdlet „Get-AzAdvisorRecommendation“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-481">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="936ed-482">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="936ed-482">Az.Batch</span></span>
* <span data-ttu-id="936ed-483">`CoreQuota` für `BatchAccountContext` in `DedicatedCoreQuota` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="936ed-483">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="936ed-484">Außerdem wurde das neue Element `LowPriorityCoreQuota` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-484">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="936ed-485">Dies wirkt sich auf **Get-AzBatchAccount** aus.</span><span class="sxs-lookup"><span data-stu-id="936ed-485">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="936ed-486">Für Parameter `-ResourceFile` von **New-AzBatchTask** wird jetzt eine Sammlung mit `PSResourceFile`-Objekten verwendet, und für die Erstellung kann das Cmdlet **New-AzBatchResourceFile** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="936ed-486">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="936ed-487">Neues Cmdlet **New-AzBatchResourceFile** als Hilfe für die Erstellung von `PSResourceFile`-Objekten.</span><span class="sxs-lookup"><span data-stu-id="936ed-487">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="936ed-488">Diese können für **New-AzBatchTask** über den Parameter `-ResourceFile` bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="936ed-488">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="936ed-489">Hierbei werden zusätzlich zum Ansatz mit `HttpUrl` zwei neue Arten von Ressourcendateien unterstützt:</span><span class="sxs-lookup"><span data-stu-id="936ed-489">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="936ed-490">Mit Ressourcendateien, die auf `AutoStorageContainerName` basieren, wird ein gesamter Container für die automatische Speicherung auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="936ed-490">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="936ed-491">Für Ressourcendateien, die auf `StorageContainerUrl` basieren, wird der in der URL angegebene Container auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="936ed-491">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="936ed-492">`ApplicationPackages`-Eigenschaft von `PSApplication` entfernt, die von **Get-AzBatchApplication** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="936ed-492">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="936ed-493">Die spezifischen Pakete in einer Anwendung können jetzt mit **Get-AzBatchApplicationPackage** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="936ed-493">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="936ed-494">Beispiel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="936ed-494">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="936ed-495">`ApplicationId` für **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** und **Set-AzBatchApplication** in `ApplicationName` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="936ed-495">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="936ed-496">`ApplicationId` ist jetzt ein Alias von `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="936ed-496">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="936ed-497">Neue `PSWindowsUserConfiguration`-Eigenschaft zu `PSUserAccount` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-497">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="936ed-498">`Version` für `PSApplicationPackage` in `Name` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="936ed-498">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="936ed-499">`BlobSource` für `PSResourceFile` in `HttpUrl` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="936ed-499">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="936ed-500">`OSDisk`-Eigenschaft aus `PSVirtualMachineConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="936ed-500">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="936ed-501">**Set-AzBatchPoolOSVersion** entfernt.</span><span class="sxs-lookup"><span data-stu-id="936ed-501">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="936ed-502">Dieser Vorgang wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="936ed-502">This operation is no longer supported.</span></span>
* <span data-ttu-id="936ed-503">`TargetOSVersion` aus `PSCloudServiceConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="936ed-503">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="936ed-504">`CurrentOSVersion` für `PSCloudServiceConfiguration` in `OSVersion` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="936ed-504">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="936ed-505">`DataEgressGiB` und `DataIngressGiB` aus `PSPoolUsageMetrics` entfernt.</span><span class="sxs-lookup"><span data-stu-id="936ed-505">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="936ed-506">**Get-AzBatchNodeAgentSku** entfernt und durch **Get-AzBatchSupportedImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="936ed-506">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="936ed-507">**Get-AzBatchSupportedImage** gibt die gleichen Daten wie **Get-AzBatchNodeAgentSku** zurück, aber in einem benutzerfreundlicheren Format.</span><span class="sxs-lookup"><span data-stu-id="936ed-507">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="936ed-508">Neue nicht verifizierte Images werden nun ebenfalls zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="936ed-508">New non-verified images are also now returned.</span></span> <span data-ttu-id="936ed-509">Zusätzlich sind weitere Informationen zu `Capabilities` und `BatchSupportEndOfLife` für jedes Image vorhanden.</span><span class="sxs-lookup"><span data-stu-id="936ed-509">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="936ed-510">Möglichkeit zum Bereitstellen von Remotedateisystemen auf jedem Knoten eines Pools über den neuen Parameter `MountConfiguration` von **New-AzBatchPool** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-510">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="936ed-511">Es ist jetzt Unterstützung für Sicherheitsregeln vorhanden, die den Netzwerkzugriff auf einen Pool basierend auf dem Quellport des Datenverkehrs blockieren.</span><span class="sxs-lookup"><span data-stu-id="936ed-511">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="936ed-512">Dies erfolgt über die `SourcePortRanges`-Eigenschaft unter `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="936ed-512">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="936ed-513">Bei der Ausführung eines Containers unterstützt Batch jetzt die Ausführung der Aufgabe im Arbeitsverzeichnis des Containers bzw. im Arbeitsverzeichnis der Batch-Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="936ed-513">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="936ed-514">Dies wird mit der `WorkingDirectory`-Eigenschaft unter `PSTaskContainerSettings` gesteuert.</span><span class="sxs-lookup"><span data-stu-id="936ed-514">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="936ed-515">Möglichkeit zum Angeben einer Sammlung mit öffentlichen IP-Adressen für `PSNetworkConfiguration` über die neue `PublicIPs`-Eigenschaft hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-515">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="936ed-516">So wird sichergestellt, dass Knoten im Pool über eine IP-Adresse aus der Liste mit den von Benutzern bereitgestellten IP-Adressen verfügen.</span><span class="sxs-lookup"><span data-stu-id="936ed-516">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="936ed-517">Wenn kein Wert angegeben wird, lautet der Standardwert von `WaitForSuccess` unter `PSSTartTask` jetzt `$True` (bisher `$False`).</span><span class="sxs-lookup"><span data-stu-id="936ed-517">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="936ed-518">Wenn kein Wert angegeben wird, lautet der Standardwert von `Scope` unter `PSAutoUserSpecification` jetzt `Pool` (bisher `Task` unter Windows und `Pool` unter Linux).</span><span class="sxs-lookup"><span data-stu-id="936ed-518">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="936ed-519">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="936ed-519">Az.Cdn</span></span>
* <span data-ttu-id="936ed-520">„UrlRewriteAction“ und „CacheKeyQueryStringAction“ für „RulesEngine“ eingeführt.</span><span class="sxs-lookup"><span data-stu-id="936ed-520">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="936ed-521">Mehrere Fehler behoben, z. B. fehlende „Selector“-Eingabe im Cmdlet „New-AzDeliveryRuleCondition“.</span><span class="sxs-lookup"><span data-stu-id="936ed-521">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="936ed-522">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="936ed-522">Az.Compute</span></span>
* <span data-ttu-id="936ed-523">Feature „Datenträgerverschlüsselungssatz“</span><span class="sxs-lookup"><span data-stu-id="936ed-523">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="936ed-524">Neue Cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="936ed-524">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="936ed-525">Parameter „DiskEncryptionSetId“ wurde den folgenden Cmdlets hinzugefügt: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="936ed-525">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="936ed-526">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="936ed-526">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="936ed-527">Die Parameter „DiskEncryptionSetId“ und „EncryptionType“ wurden den folgenden Cmdlets hinzugefügt:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="936ed-527">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="936ed-528">Parameter „PublicIPAddressVersion“ wurde „New-AzVmssIPConfig“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-528">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="936ed-529">„FileUris“ für benutzerdefinierte Skripterweiterung von öffentlicher Einstellung auf geschützte Einstellung umgestellt.</span><span class="sxs-lookup"><span data-stu-id="936ed-529">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="936ed-530">„ScaleInPolicy“ wurde den Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-530">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="936ed-531">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="936ed-531">Breaking changes</span></span>
    - <span data-ttu-id="936ed-532">Parameter „UploadSizeInBytes“ wird anstelle von „DiskSizeGB“ für „New-AzDiskConfig“ verwendet, wenn „CreateOption“ auf „Upload“ festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="936ed-532">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="936ed-533">Im „GalleryImageVersion“-Objekt wurde „objectPublishingProfile.Source.ManagedImage.Id“ durch „StorageProfile.Source.Id“ ersetzt.</span><span class="sxs-lookup"><span data-stu-id="936ed-533">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="936ed-534">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="936ed-534">Az.DataFactory</span></span>
* <span data-ttu-id="936ed-535">Version des ADF .NET SDK auf 4.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="936ed-535">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="936ed-536">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="936ed-536">Az.DataLakeStore</span></span>
* <span data-ttu-id="936ed-537">Update für ADLS SDK-Version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) mit den folgenden Fehlerbehebungen durchgeführt:</span><span class="sxs-lookup"><span data-stu-id="936ed-537">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="936ed-538">Vermeidung der Auslösung einer Ausnahme, während die Deserialisierung des „creationtime“-Elements des Papierkorb- oder Verzeichniseintrags nicht durchgeführt werden kann</span><span class="sxs-lookup"><span data-stu-id="936ed-538">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="936ed-539">Verfügbarmachung der Einstellung pro Anforderungszeitlimit in „adlsclient“</span><span class="sxs-lookup"><span data-stu-id="936ed-539">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="936ed-540">Fehlerbehebung für Übergabe des ursprünglichen „syncflag“-Elements für badoffset-Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="936ed-540">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="936ed-541">Fehlerbehebung für „EnumerateDirectory“ zum Abrufen des Fortsetzungstokens nach der Überprüfung der Antwort</span><span class="sxs-lookup"><span data-stu-id="936ed-541">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="936ed-542">Behebung eines Verkettungsfehlers</span><span class="sxs-lookup"><span data-stu-id="936ed-542">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="936ed-543">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="936ed-543">Az.FrontDoor</span></span>
* <span data-ttu-id="936ed-544">Verschiedene Tippfehler im Modul korrigiert.</span><span class="sxs-lookup"><span data-stu-id="936ed-544">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="936ed-545">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="936ed-545">Az.HDInsight</span></span>
* <span data-ttu-id="936ed-546">Fehler behoben, bei dem Kunden die Meldung „Keine gültige Base64-Zeichenfolge“ erhalten haben, wenn sie „Get-AzHDInsightCluster“ zum Abrufen des Clusters mit ADLSGen1-Speicher verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="936ed-546">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="936ed-547">Parameter mit dem Namen „ApplicationId“ den drei Cmdlets „Add-AzHDInsightClusterIdentity“, „New-AzHDInsightClusterConfig“ und „New-AzHDInsightCluster“ hinzugefügt, damit der Kunde die Dienstprinzipal-Anwendungs-ID für den Zugriff auf Azure Data Lake bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="936ed-547">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="936ed-548">Microsoft.Azure.Management.HDInsight von 2.1.0 in 5.1.0 geändert.</span><span class="sxs-lookup"><span data-stu-id="936ed-548">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="936ed-549">Fünf Cmdlets wurden entfernt:</span><span class="sxs-lookup"><span data-stu-id="936ed-549">Removed five cmdlets:</span></span>
    - <span data-ttu-id="936ed-550">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="936ed-550">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="936ed-551">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="936ed-551">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="936ed-552">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="936ed-552">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="936ed-553">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="936ed-553">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="936ed-554">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="936ed-554">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="936ed-555">Drei Cmdlets wurden hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="936ed-555">Added three cmdlets:</span></span>
    - <span data-ttu-id="936ed-556">„Get-AzHDInsightMonitoring“ als Ersatz für „Get-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="936ed-556">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="936ed-557">„Enable-AzHDInsightMonitoring“ als Ersatz für „Enable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="936ed-557">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="936ed-558">„Disable-AzHDInsightMonitoring“ als Ersatz für „Disable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="936ed-558">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="936ed-559">Fehler für Cmdlet „Get-AzHDInsightProperties“ behoben, um Unterstützung für das Abrufen von Funktionsinformationen von einem bestimmten Ort bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="936ed-559">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="936ed-560">Parametersätze („Spark1“, „Spark2“) aus „Add-AzHDInsightConfigValue“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="936ed-560">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="936ed-561">Beispiele den Hilfedokumenten des Cmdlets „Add-AzHDInsightSecurityProfile“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-561">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="936ed-562">Der Ausgabetyp der folgenden Cmdlets wurde geändert:</span><span class="sxs-lookup"><span data-stu-id="936ed-562">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="936ed-563">Ausgabetyp für „Get-AzHDInsightProperties“ von „CapabilitiesResponse“ in „AzureHDInsightCapabilities“ geändert.</span><span class="sxs-lookup"><span data-stu-id="936ed-563">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="936ed-564">Ausgabetyp für „Remove-AzHDInsightCluster“ von „ClusterGetResponse“ in „bool“ geändert.</span><span class="sxs-lookup"><span data-stu-id="936ed-564">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="936ed-565">Ausgabetyp für „Set-AzHDInsightGatewaySettings“ von „HttpConnectivitySettings“ in „GatewaySettings“ geändert.</span><span class="sxs-lookup"><span data-stu-id="936ed-565">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="936ed-566">Einige Testfälle für Szenarien wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-566">Added some scenario test cases.</span></span>
* <span data-ttu-id="936ed-567">Aliase wurden entfernt: „Add-AzHDInsightConfigValues“, „Get-AzHDInsightProperties“.</span><span class="sxs-lookup"><span data-stu-id="936ed-567">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="936ed-568">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="936ed-568">Az.IotHub</span></span>
* <span data-ttu-id="936ed-569">Wichtige Änderungen:</span><span class="sxs-lookup"><span data-stu-id="936ed-569">Breaking changes:</span></span>
    - <span data-ttu-id="936ed-570">Das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="936ed-570">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="936ed-571">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="936ed-571">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="936ed-572">Das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="936ed-572">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="936ed-573">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="936ed-573">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="936ed-574">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="936ed-574">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="936ed-575">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="936ed-575">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="936ed-576">Das Cmdlet „New-AzIotHubExportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubExportDevices“.</span><span class="sxs-lookup"><span data-stu-id="936ed-576">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="936ed-577">Das Cmdlet „New-AzIotHubImportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubImportDevices“.</span><span class="sxs-lookup"><span data-stu-id="936ed-577">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="936ed-578">Das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="936ed-578">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="936ed-579">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="936ed-579">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="936ed-580">Das Cmdlet „Set-AzIotHub“ unterstützt den Parameter „OperationsMonitoringProperties“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="936ed-580">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="936ed-581">Der Parametersatz „UpdateOperationsMonitoringProperties“ für das Cmdlet „Set-AzIotHub“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="936ed-581">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="936ed-582">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="936ed-582">Az.RecoveryServices</span></span>
* <span data-ttu-id="936ed-583">Azure wurde die Azure Site Recovery-Unterstützung zum Konfigurieren von Netzwerkressourcen, z. B. NSG, öffentliche IP-Adresse und interner Load Balancer für Azure, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-583">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="936ed-584">Azure Site Recovery-Unterstützung zum Schreiben auf verwaltete Datenträger für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-584">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="936ed-585">Azure Site Recovery-Unterstützung für NIC-Reduzierung für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-585">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="936ed-586">Azure wurde Azure Site Recovery-Unterstützung für beschleunigten Netzwerkbetrieb für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-586">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="936ed-587">Azure wurde Azure Site Recovery-Unterstützung für automatische Agent-Updates für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-587">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="936ed-588">Azure wurde Azure Site Recovery-Unterstützung für SSD Standard für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-588">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="936ed-589">Azure wurde Azure Site Recovery-Unterstützung für das zweistufige Azure Disk Encryption-Verfahren für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-589">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="936ed-590">Azure wurde Azure Site Recovery-Unterstützung für das Schützen von neu hinzugefügten Datenträgern für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-590">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="936ed-591">Feature „Vorläufiges Löschen“ (SoftDelete) für VM und zugehörige Tests hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-591">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="936ed-592">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="936ed-592">Az.Resources</span></span>
* <span data-ttu-id="936ed-593">Abhängigkeitsassembly „Microsoft.Extensions.Caching.Memory“ von 1.1.1 auf 2.2 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="936ed-593">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="936ed-594">Az.Network</span><span class="sxs-lookup"><span data-stu-id="936ed-594">Az.Network</span></span>
* <span data-ttu-id="936ed-595">Alle Cmdlets für „PrivateEndpointConnection“ geändert, um Unterstützung für generischen Dienstanbieter bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="936ed-595">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="936ed-596">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="936ed-596">Updated cmdlet:</span></span>
        - <span data-ttu-id="936ed-597">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="936ed-597">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="936ed-598">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="936ed-598">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="936ed-599">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="936ed-599">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="936ed-600">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="936ed-600">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="936ed-601">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="936ed-601">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="936ed-602">Neues Cmdlet für „PrivateLinkResource“ hinzugefügt, einschließlich Unterstützung des generischen Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="936ed-602">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="936ed-603">Neues Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="936ed-603">New cmdlet:</span></span>
        - <span data-ttu-id="936ed-604">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="936ed-604">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="936ed-605">Neue Felder und Parameter für das Feature „Proxyprotokoll V2“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-605">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="936ed-606">„EnableProxyProtocol“-Eigenschaft in „PrivateLinkService“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-606">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="936ed-607">„LinkIdentifier“-Eigenschaft in „PrivateEndpointConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-607">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="936ed-608">„New-AzPrivateLinkService“ aktualisiert, um den neuen optionalen Parameter „EnableProxyProtocol“ hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="936ed-608">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="936ed-609">Fehlerhafte Parameterbeschreibung in Referenzdokumentation von „New-AzApplicationGatewaySku“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="936ed-609">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="936ed-610">Neue Cmdlets zur Unterstützung der Azure-Firewallrichtlinie hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-610">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="936ed-611">Unterstützung für untergeordnete Ressource „RouteTables“ von VirtualHub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-611">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="936ed-612">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="936ed-612">New cmdlets added:</span></span>
        - <span data-ttu-id="936ed-613">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="936ed-613">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="936ed-614">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="936ed-614">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="936ed-615">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="936ed-615">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="936ed-616">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="936ed-616">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="936ed-617">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="936ed-617">Set-AzVirtualHub</span></span>
* <span data-ttu-id="936ed-618">Unterstützung für die neuen Eigenschaften „Sku“ von VirtualHub und „VirtualWANType“ von VirtualWan hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-618">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="936ed-619">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="936ed-619">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="936ed-620">New-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-620">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="936ed-621">Update-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-621">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="936ed-622">New-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-622">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="936ed-623">Update-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-623">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="936ed-624">Unterstützung für „EnableInternetSecurity“-Eigenschaft für „HubVnetConnection“, „VpnConnection“ und „ExpressRouteConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-624">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="936ed-625">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="936ed-625">New cmdlets added:</span></span>
        - <span data-ttu-id="936ed-626">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="936ed-626">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="936ed-627">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="936ed-627">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="936ed-628">New-AzureRmVirtualHubVnetConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-628">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="936ed-629">New-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-629">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="936ed-630">Update-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-630">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="936ed-631">New-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-631">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="936ed-632">Set-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-632">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="936ed-633">Unterstützung für die Konfiguration der „WebApplicationFirewall“-Richtlinie der obersten Ebene hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-633">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="936ed-634">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="936ed-634">New cmdlets added:</span></span>
        - <span data-ttu-id="936ed-635">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="936ed-635">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="936ed-636">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="936ed-636">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="936ed-637">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="936ed-637">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="936ed-638">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="936ed-638">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="936ed-639">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="936ed-639">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="936ed-640">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="936ed-640">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="936ed-641">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="936ed-641">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="936ed-642">New-AzApplicationGatewayFirewallPolicy: Parameter „PolicySetting“, „ManagedRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-642">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="936ed-643">Unterstützung für Operator „Geo-Match“ unter „CustomRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-643">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="936ed-644">„GeoMatch“ zum Operator von „FirewallCondition“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-644">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="936ed-645">Unterstützung für Firewallrichtlinien „perListener“ und „perSite“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-645">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="936ed-646">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="936ed-646">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="936ed-647">New-AzApplicationGatewayHttpListener: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-647">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="936ed-648">New-AzApplicationGatewayPathRuleConfig: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-648">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="936ed-649">Fehlerbehebung: Nichtbeachtung der Groß-/Kleinschreibung für erforderliches Subnetz mit dem Namen „AzureBastionSubnet“ in „PSBastion“ ist jetzt möglich.</span><span class="sxs-lookup"><span data-stu-id="936ed-649">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="936ed-650">Unterstützung für Ziel-FQDNs in Netzwerkregeln und Übersetzung von FQDN in NAT-Regeln für Azure Firewall hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-650">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="936ed-651">Unterstützung für Ressource „RouteTables“ der obersten Ebene von „IpGroup“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-651">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="936ed-652">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="936ed-652">New cmdlets added:</span></span>
        - <span data-ttu-id="936ed-653">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="936ed-653">New-AzIpGroup</span></span>
        - <span data-ttu-id="936ed-654">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="936ed-654">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="936ed-655">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="936ed-655">Get-AzIpGroup</span></span>
        - <span data-ttu-id="936ed-656">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="936ed-656">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="936ed-657">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="936ed-657">Az.ServiceFabric</span></span>
* <span data-ttu-id="936ed-658">Cmdlet „Add-AzServiceFabricApplicationCertificate“ entfernt, da dieses Szenario durch „Add-AzVmssSecret“ abgedeckt ist.</span><span class="sxs-lookup"><span data-stu-id="936ed-658">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="936ed-659">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="936ed-659">Az.Sql</span></span>
* <span data-ttu-id="936ed-660">Unterstützung für die Wiederherstellung von gelöschten Datenbanken auf verwalteten Instanzen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-660">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="936ed-661">Veraltete Cmdlets für die Überprüfung aus Code ausgesondert.</span><span class="sxs-lookup"><span data-stu-id="936ed-661">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="936ed-662">Veraltete Aliase entfernt:</span><span class="sxs-lookup"><span data-stu-id="936ed-662">Removed deprecated aliases:</span></span>
* <span data-ttu-id="936ed-663">Get-AzSqlDatabaseIndexRecommendations (stattdessen „Get-AzSqlDatabaseIndexRecommendation“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="936ed-663">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="936ed-664">Get-AzSqlDatabaseRestorePoints (stattdessen „Get-AzSqlDatabaseRestorePoint“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="936ed-664">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="936ed-665">Cmdlet „Get-AzSqlDatabaseSecureConnectionPolicy“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="936ed-665">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="936ed-666">Aliase für veraltete Cmdlets für Einstellungen zur Sicherheitsrisikobewertung wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="936ed-666">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="936ed-667">Cmdlets für Einstellungen für die erweiterte Bedrohungserkennung wurden als veraltet eingestuft.</span><span class="sxs-lookup"><span data-stu-id="936ed-667">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="936ed-668">Cmdlets zum Deaktivieren und Aktivieren von Vertraulichkeitsempfehlungen in Spalten einer Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-668">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="936ed-669">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="936ed-669">Az.Storage</span></span>
* <span data-ttu-id="936ed-670">Unterstützung für große Dateifreigaben beim Erstellen oder Aktualisieren eines Speicherkontos hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-670">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="936ed-671">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="936ed-671">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="936ed-672">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="936ed-672">Set-AzStorageAccount</span></span>
* <span data-ttu-id="936ed-673">Beim Schließen/Abrufen des Dateihandles wird die Überprüfung des Eingabepfads auf Dateiverzeichnis oder Datei übersprungen, um einen Fehler für das Objekt im Status „DeletePending“ zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="936ed-673">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="936ed-674">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="936ed-674">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="936ed-675">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="936ed-675">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="936ed-676">2.8.0: Oktober 2019</span><span class="sxs-lookup"><span data-stu-id="936ed-676">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="936ed-677">Allgemein</span><span class="sxs-lookup"><span data-stu-id="936ed-677">General</span></span>
* <span data-ttu-id="936ed-678">Az.HealthcareApis-Release 1.0.0</span><span class="sxs-lookup"><span data-stu-id="936ed-678">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="936ed-679">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="936ed-679">Az.Accounts</span></span>
* <span data-ttu-id="936ed-680">Telemetriedaten und URL-Umschreibung für generierte Module aktualisiert, Windows-Komponententests korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-680">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="936ed-681">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="936ed-681">Az.ApiManagement</span></span>
* <span data-ttu-id="936ed-682">**Set-AzApiManagementApi**: Unterstützung für die Aktualisierung der API in „ApiVersionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-682">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="936ed-683">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="936ed-683">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="936ed-684">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="936ed-684">Az.Automation</span></span>
* <span data-ttu-id="936ed-685">Cmdlet „New-AzureAutomationSoftwareUpdateConfiguration“ für den Parameter für die Linux-Neustarteinstellung korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-685">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="936ed-686">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="936ed-686">Az.Batch</span></span>
* <span data-ttu-id="936ed-687">**Get-AzBatchNodeAgentSku** ist veraltet und wird in Version 2.0.0 durch **Get-AzBatchSupportImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="936ed-687">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="936ed-688">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="936ed-688">Az.Compute</span></span>
* <span data-ttu-id="936ed-689">Parameter „Priority“, „EvictionPolicy“ und „MaxPrice“ zu den Cmdlets „“New-AzVM“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-689">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="936ed-690">Warnmeldung und Hilfedokument für die Cmdlets „Add-AzVMAdditionalUnattendContent“ und „Add-AzVMSshPublicKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-690">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="936ed-691">Ausnahme „-skipVmBackup“ Linux-VMs mit verwalteten Datenträgern für „Set-AzVMDiskEncryptionExtension“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-691">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="936ed-692">Fehler beim Aktualisieren von Verschlüsselungseinstellungen in „Set-AzVMDiskEncryptionExtension“ korrigiert (zweistufiges Szenario)</span><span class="sxs-lookup"><span data-stu-id="936ed-692">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="936ed-693">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="936ed-693">Az.DataFactory</span></span>
* <span data-ttu-id="936ed-694">CRUD-Befehle für ADF V2-Datenfluss hinzugefügt: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow und Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="936ed-694">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="936ed-695">Aktionsbefehle für Debugsitzung für ADF V2-Datenfluss hinzugefügt: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand und Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="936ed-695">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="936ed-696">Version des ADF .NET SDK auf 4.2.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-696">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="936ed-697">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="936ed-697">Az.DataLakeStore</span></span>
* <span data-ttu-id="936ed-698">Kontoüberprüfung korrigiert, sodass Konten mit „-“ ohne Domäne übermittelt werden können</span><span class="sxs-lookup"><span data-stu-id="936ed-698">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="936ed-699">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="936ed-699">Az.HealthcareApis</span></span>
* <span data-ttu-id="936ed-700">PowerShell-Version auf 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-700">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="936ed-701">SDK-Version auf 1.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-701">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="936ed-702">Aktualisierung in Tests, um auf neue SDK-Version zu verweisen</span><span class="sxs-lookup"><span data-stu-id="936ed-702">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="936ed-703">Ausgabestruktur von geschachtelt in vereinfacht geändert</span><span class="sxs-lookup"><span data-stu-id="936ed-703">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="936ed-704">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="936ed-704">Az.IotHub</span></span>
* <span data-ttu-id="936ed-705">Neue Routingquelle hinzugefügt: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="936ed-705">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="936ed-706">Kleinere Fehlerbehebung: „Get-AzIothub“ gibt „subscriptionId“ nicht zurück.</span><span class="sxs-lookup"><span data-stu-id="936ed-706">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="936ed-707">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="936ed-707">Az.Monitor</span></span>
* <span data-ttu-id="936ed-708">Neue Aktionsgruppenempfänger für Aktionsgruppe hinzugefügt:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="936ed-708">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="936ed-709">Verwendung des allgemeinen Warnungsschemas für Empfänger aktiviert.</span><span class="sxs-lookup"><span data-stu-id="936ed-709">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="936ed-710">Dies gilt nicht für SMS, Azure App-Pushbenachrichtigungen, ITSM und Sprachempfänger.</span><span class="sxs-lookup"><span data-stu-id="936ed-710">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="936ed-711">Webhooks unterstützen nun die Azure Active Directory-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="936ed-711">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="936ed-712">Az.Network</span><span class="sxs-lookup"><span data-stu-id="936ed-712">Az.Network</span></span>
* <span data-ttu-id="936ed-713">Neues Cmdlet „Get-AzAvailableServiceAlias“ hinzugefügt, das zum Abrufen der Aliase aufgerufen werden kann, die für Dienstendpunktrichtlinien verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="936ed-713">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="936ed-714">Unterstützung für das Hinzufügen von Verbindungen von Datenverkehrsselektoren zu Virtual Network-Gatewayverbindungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-714">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="936ed-715">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="936ed-715">New cmdlets added:</span></span>
        - <span data-ttu-id="936ed-716">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="936ed-716">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="936ed-717">Cmdlets mit optionalen Parametern aktualisiert: -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="936ed-717">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="936ed-718">Unterstützung für ESP- und AH-Protokolle in Konfigurationen von Netzwerksicherheitsregeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-718">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="936ed-719">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="936ed-719">Updated cmdlets:</span></span>
        - <span data-ttu-id="936ed-720">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="936ed-720">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="936ed-721">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="936ed-721">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="936ed-722">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="936ed-722">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="936ed-723">Verbesserte Behandlung von Ausnahmen in Cortex-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="936ed-723">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="936ed-724">Neue Generationen und SKUs für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="936ed-724">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="936ed-725">Einführung neuer Generationen für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="936ed-725">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="936ed-726">Einführung neuer SKUs mit höherem Durchsatz für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="936ed-726">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="936ed-727">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="936ed-727">Az.RedisCache</span></span>
* <span data-ttu-id="936ed-728">Referenzdokumentation zu „Set-AzRedisCache“ aktualisiert, um fehlende Werte für den Parameter „-Size“ aufzunehmen</span><span class="sxs-lookup"><span data-stu-id="936ed-728">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="936ed-729">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="936ed-729">Az.Sql</span></span>
* <span data-ttu-id="936ed-730">Unterstützung für das Festlegen des Active Directory-Administrators für verwaltete Instanz hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-730">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="936ed-731">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="936ed-731">Az.Storage</span></span>
* <span data-ttu-id="936ed-732">Storage-Clientbibliothek auf 11.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-732">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="936ed-733">Auflisten von Containern mit der API der Verwaltungsebene, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="936ed-733">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="936ed-734">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="936ed-734">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="936ed-735">Auflisten von Storage-Konten aus Abonnements, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="936ed-735">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="936ed-736">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="936ed-736">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="936ed-737">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="936ed-737">Az.StorageSync</span></span>
* <span data-ttu-id="936ed-738">Problem 9810 in „Reset-AzStorageSyncServerCertificate“ behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-738">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="936ed-739">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="936ed-739">Az.Websites</span></span>
* <span data-ttu-id="936ed-740">Fehler beim Aktualisieren von ASP einer App mit „Set-AzWebApp“</span><span class="sxs-lookup"><span data-stu-id="936ed-740">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="936ed-741">2.7.0: September 2019</span><span class="sxs-lookup"><span data-stu-id="936ed-741">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="936ed-742">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="936ed-742">Az.ApiManagement</span></span>
* <span data-ttu-id="936ed-743">Beschreibung des Parameters „-Format“ in der Referenzdokumentation für „Set-AzApiManagementPolicy“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-743">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="936ed-744">Verweise des veralteten Cmdlets „Update-AzApiManagementDeployment“ aus Referenzdokumentation entfernt.</span><span class="sxs-lookup"><span data-stu-id="936ed-744">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="936ed-745">Verwenden Sie stattdessen „Set-AzApiManagement“.</span><span class="sxs-lookup"><span data-stu-id="936ed-745">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="936ed-746">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="936ed-746">Az.Automation</span></span>
* <span data-ttu-id="936ed-747">Tippfehler im Beispiel in der Referenzdokumentation für „Register-AzAutomationDscNode“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-747">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="936ed-748">Erläuterung zur Betriebssystemeinschränkung zu „Register-AzAutomationDSCNode“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-748">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="936ed-749">Nullverweisausnahme des Cmdlets „Start-AzAutomationRunbook“ für die Option „-Wait“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="936ed-749">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="936ed-750">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="936ed-750">Az.Compute</span></span>
* <span data-ttu-id="936ed-751">Parameter „UploadSizeInBytes“ zu „New-AzDiskConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-751">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="936ed-752">Inkrementeller Parameter zu „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-752">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="936ed-753">Feature für VM mit niedriger Priorität hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="936ed-753">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="936ed-754">Parameter „MaxPrice“, „EvictionPolicy“ und „Priority“ zu New-AzVMConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-754">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="936ed-755">Parameter „MaxPrice“ zu den Cmdlets „New-AzVmssConfig“, „Update-AzVM“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-755">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="936ed-756">Fehlerbehebung für VM-Verweis für das Cmdlet „Get-AzAvailabilitySet“, wenn alle Verfügbarkeitsgruppen im Abonnement aufgelistet werden</span><span class="sxs-lookup"><span data-stu-id="936ed-756">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="936ed-757">Nullausnahme für „Get-AzRemoteDesktopFile“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-757">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="936ed-758">VHD-Suchmethode für Position relativ zum Ende korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-758">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="936ed-759">Problem mit UltraSSD für „New-AzVM“ und „Update-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-759">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="936ed-760">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="936ed-760">Az.DataFactory</span></span>
* <span data-ttu-id="936ed-761">Drei neue Befehle für ADF V2 hinzugefügt: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription und Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="936ed-761">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="936ed-762">Version des ADF .NET SDK auf 4.1.3 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-762">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="936ed-763">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="936ed-763">Az.HDInsight</span></span>
* <span data-ttu-id="936ed-764">Hinweis auf Breaking Changes hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-764">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="936ed-765">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="936ed-765">Az.IotHub</span></span>
* <span data-ttu-id="936ed-766">Unterstützung zum Aufrufen eines Failovers für einen IoT-Hub zur geografisch gekoppelten Notfallwiederherstellungsregion hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-766">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="936ed-767">Unterstützung zum Verwalten der Nachrichtenanreicherung für einen IoT-Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-767">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="936ed-768">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="936ed-768">New cmdlets are:</span></span>
    - <span data-ttu-id="936ed-769">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="936ed-769">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="936ed-770">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="936ed-770">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="936ed-771">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="936ed-771">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="936ed-772">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="936ed-772">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="936ed-773">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="936ed-773">Az.Monitor</span></span>
* <span data-ttu-id="936ed-774">Verweis auf das aktuelle Monitor SDK, d. h. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="936ed-774">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="936ed-775">Geringfügige Änderungen an den Metrik-Cmdlets vorgenommen, d. h. die Einheitenenumeration unterstützt verschiedene neue Werte.</span><span class="sxs-lookup"><span data-stu-id="936ed-775">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="936ed-776">Dabei handelt es sich um schreibgeschützte Cmdlets, sodass keine Änderungen an der Eingabe der Cmdlets erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="936ed-776">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="936ed-777">Die API-Version der **ActionGroups**-Anforderungen lautet jetzt **2019-06-01** (zuvor **2018-03-01**).</span><span class="sxs-lookup"><span data-stu-id="936ed-777">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="936ed-778">Die Szenariotests wurden aktualisiert, um diese Änderung zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="936ed-778">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="936ed-779">Die Konstruktoren für die Klassen **EmailReceiver** und **WebhookReceiver** haben ein neues obligatorisches Argument hinzugefügt, d. h. einen booleschen Wert namens **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="936ed-779">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="936ed-780">Derzeit ist der Wert auf **false** festgelegt, damit sich dieser Breaking Change nicht auf die Cmdlets auswirkt.</span><span class="sxs-lookup"><span data-stu-id="936ed-780">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="936ed-781">**HINWEIS:** Dies ist eine vorübergehende Änderung, die vom Team für Warnungen validiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="936ed-781">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="936ed-782">Die Reihenfolge der Argumente für den Konstruktor der Klasse **Source** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="936ed-782">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="936ed-783">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="936ed-783">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="936ed-784">Die Reihenfolge der Argumente für den Konstruktor der Klasse **AlertingAction** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="936ed-784">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="936ed-785">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="936ed-785">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="936ed-786">Unterstützung von Kriterien für dynamische Schwellwerte für Metrikwarnung v2</span><span class="sxs-lookup"><span data-stu-id="936ed-786">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="936ed-787">New-AzMetricAlertRuleV2Criteria: Erstellt nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="936ed-787">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="936ed-788">Add-AzMetricAlertRuleV2: Akzeptiert nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="936ed-788">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="936ed-789">Verbesserungen an den Cmdlets für geplante Abfrageregeln (Scheduled Query Rule, SQR)</span><span class="sxs-lookup"><span data-stu-id="936ed-789">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="936ed-790">Cmdlets akzeptieren den Parameter „Location“ in zwei Formaten: entweder den Standort (z. B. „eastus“) oder den Anzeigenamen des Standorts (z. B. „USA, Osten“)</span><span class="sxs-lookup"><span data-stu-id="936ed-790">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="936ed-791">Parameter „Enabled“ in Hilfedateien ordnungsgemäß dargestellt</span><span class="sxs-lookup"><span data-stu-id="936ed-791">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="936ed-792">Beispiele für optionalen Parameter „ActionGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-792">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="936ed-793">Hilfedateien insgesamt verbessert</span><span class="sxs-lookup"><span data-stu-id="936ed-793">Overall improved help files</span></span>
* <span data-ttu-id="936ed-794">Fehler beim Bestimmen des Bereichstyps für „Set-AzActionRule“ behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-794">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="936ed-795">Az.Network</span><span class="sxs-lookup"><span data-stu-id="936ed-795">Az.Network</span></span>
* <span data-ttu-id="936ed-796">Fehlerhaftes Beispiel in der Referenzdokumentation zu „New-AzApplicationGateway“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-796">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="936ed-797">Hinweis in der Referenzdokumentation zu „Get-AzNetworkWatcherPacketCapture“ zum Abrufen aller Eigenschaften für eine Paketerfassung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-797">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="936ed-798">Beispiel in der Referenzdokumentation zu „Test-AzNetworkWatcherIPFlow“ korrigiert, um die Netzwerkadapter ordnungsgemäß aufzulisten</span><span class="sxs-lookup"><span data-stu-id="936ed-798">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="936ed-799">Cloudausnahmeanalyse verbessert, um ggf. zusätzliche Details anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="936ed-799">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="936ed-800">Cloudausnahmeanalyse verbessert, um zusätzlichen Typ der SDK-Ausnahme zu verarbeiten</span><span class="sxs-lookup"><span data-stu-id="936ed-800">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="936ed-801">Falsche Zuordnung der Sicherheitsregelmodelle korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-801">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="936ed-802">Eigenschaften zur Netzwerkschnittstelle für das Feature für die private IP-Adresse hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-802">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="936ed-803">Eigenschaft „PrivateEndpoint“ als Typ „PSResourceId“ zu „PSNetworkInterface“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-803">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="936ed-804">Eigenschaft „PrivateLinkConnectionProperties“ als Typ „PSIpConfigurationConnectivityInformation“ zu „PSNetworkInterfaceIPConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-804">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="936ed-805">Neue Modellklasse „PSIpConfigurationConnectivityInformation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-805">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="936ed-806">Neues ApplicationRuleProtocolType-Element „mssql“ für Azure Firewall-Ressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-806">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="936ed-807">Unterstützung von Mehrfachverbindungen in Virtual WAN</span><span class="sxs-lookup"><span data-stu-id="936ed-807">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="936ed-808">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="936ed-808">New cmdlets</span></span>
        - <span data-ttu-id="936ed-809">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="936ed-809">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="936ed-810">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="936ed-810">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="936ed-811">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="936ed-811">Updated cmdlet:</span></span>
        - <span data-ttu-id="936ed-812">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="936ed-812">New-VpnSite</span></span>
        - <span data-ttu-id="936ed-813">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="936ed-813">Update-VpnSite</span></span>
        - <span data-ttu-id="936ed-814">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="936ed-814">New-VpnConnection</span></span>
        - <span data-ttu-id="936ed-815">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="936ed-815">Update-VpnConnection</span></span>
* <span data-ttu-id="936ed-816">Dokumente für einige PowerShell-Beispiele korrigiert, sodass Az-Cmdlets anstelle von AzureRM-Cmdlets verwendet werden</span><span class="sxs-lookup"><span data-stu-id="936ed-816">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="936ed-817">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="936ed-817">Az.RecoveryServices</span></span>
* <span data-ttu-id="936ed-818">AzureVMpolicy-Objekt mit ProtectedItemsCount-Attribut aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-818">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="936ed-819">Tests für VM-Richtlinie und Wiederherstellung des ursprünglichen Speicherkontos hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-819">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="936ed-820">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="936ed-820">Az.Resources</span></span>
* <span data-ttu-id="936ed-821">Fehler behoben, aufgrund dessen „New-AzRoleAssignment“ nicht ohne den Parameter „Scope“ aufgerufen werden konnte</span><span class="sxs-lookup"><span data-stu-id="936ed-821">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="936ed-822">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="936ed-822">Az.ServiceFabric</span></span>
* <span data-ttu-id="936ed-823">Tippfehler im Beispiel für die Referenzdokumentation „Update-AzServiceFabricReliability“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-823">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="936ed-824">Neue Cmdlets zum Verwalten von Anwendung und Diensten hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="936ed-824">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="936ed-825">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="936ed-825">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="936ed-826">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="936ed-826">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="936ed-827">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="936ed-827">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="936ed-828">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="936ed-828">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="936ed-829">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="936ed-829">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="936ed-830">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="936ed-830">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="936ed-831">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="936ed-831">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="936ed-832">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="936ed-832">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="936ed-833">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="936ed-833">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="936ed-834">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="936ed-834">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="936ed-835">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="936ed-835">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="936ed-836">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="936ed-836">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="936ed-837">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="936ed-837">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="936ed-838">Service Fabric SDK auf Version 1.2.0 aktualisiert, die API-Version 2019-03-01 des Service Fabric-Ressourcenanbieters verwendet</span><span class="sxs-lookup"><span data-stu-id="936ed-838">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="936ed-839">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="936ed-839">Az.SignalR</span></span>
* <span data-ttu-id="936ed-840">Cmdlets „Update“, „Restart“, „CheckNameAvailability“ und „GetUsage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-840">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="936ed-841">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="936ed-841">Az.Sql</span></span>
* <span data-ttu-id="936ed-842">Beispiel in der Referenzdokumentation für „Get-AzSqlElasticPool“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-842">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="936ed-843">V-Kern-Beispiel zum Erstellen eines Pools für elastische Datenbanken hinzugefügt (New-AzSqlElasticPool)</span><span class="sxs-lookup"><span data-stu-id="936ed-843">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="936ed-844">Überprüfung von „EmailAddresses“ sowie Validierung, dass „EmailAdmins“ nicht auf „false“ festgelegt ist, in „Set-AzSqlServerAdvancedThreatProtectionPolicy“ und „Set-AzSqlDatabaseAdvancedThreatProtectionPolicy“ entfernt, wenn „EmailAddresses“ leer ist</span><span class="sxs-lookup"><span data-stu-id="936ed-844">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="936ed-845">Entfernen der Einstellungen für Server-/Datenbanküberwachung aktiviert, wenn mehrere Diagnoseeinstellungen vorhanden sind, die eine Überwachungskategorie ermöglichen</span><span class="sxs-lookup"><span data-stu-id="936ed-845">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="936ed-846">Überprüfung von E-Mail-Adressen in mehreren Cmdlets für die SQL-Sicherheitsrisikobewertung korrigiert (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting und Update-AzSqlInstanceVulnerabilityAssessmentSetting)</span><span class="sxs-lookup"><span data-stu-id="936ed-846">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="936ed-847">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="936ed-847">Az.Storage</span></span>
* <span data-ttu-id="936ed-848">Beispiel in der Referenzdokumentation für „Get-AzStorageAccountKey“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-848">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="936ed-849">Beim Upload/Download von Azure-Dateien wird das Beibehalten der SMB-Eigenschaften der Quelldateien (Dateiattribute, Zeitpunkt der Dateierstellung, letzter Schreibzugriff für die Datei) in der Zieldatei unterstützt.</span><span class="sxs-lookup"><span data-stu-id="936ed-849">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="936ed-850">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="936ed-850">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="936ed-851">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="936ed-851">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="936ed-852">Fehler beim Hochladen von Blockblobs mit Eigenschaften/Metadaten für das für einen Container aktivierte ImmutabilityPolicy-Element behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-852">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="936ed-853">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="936ed-853">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="936ed-854">Unterstützung für die Verwaltung von Azure-Dateifreigaben mit der API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="936ed-854">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="936ed-855">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="936ed-855">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="936ed-856">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="936ed-856">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="936ed-857">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="936ed-857">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="936ed-858">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="936ed-858">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="936ed-859">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="936ed-859">Az.Websites</span></span>
* <span data-ttu-id="936ed-860">Problem behoben, aufgrund dessen webapp-Tags beim Migrieren der App zu neuem ASP gelöscht wurden</span><span class="sxs-lookup"><span data-stu-id="936ed-860">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="936ed-861">„Publish-AzureWebapp“ für die Verwendung unter Linux und Windows korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-861">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="936ed-862">Beispiel in Referenzdokumentation „Get-AzWebAppPublishingProfile“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-862">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="936ed-863">2.6.0: August 2019</span><span class="sxs-lookup"><span data-stu-id="936ed-863">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="936ed-864">Allgemein</span><span class="sxs-lookup"><span data-stu-id="936ed-864">General</span></span>
* <span data-ttu-id="936ed-865">Verschiedene Tippfehler in zahlreichen Modulen korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-865">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="936ed-866">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="936ed-866">Az.Accounts</span></span>
* <span data-ttu-id="936ed-867">Unterstützung der benutzerseitig zugewiesenen MSI in Azure Functions-Authentifizierung (#9479)</span><span class="sxs-lookup"><span data-stu-id="936ed-867">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="936ed-868">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="936ed-868">Az.Aks</span></span>
* <span data-ttu-id="936ed-869">Problem mit der Ausgabe für „Get-AzAks“ behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-869">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="936ed-870">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="936ed-870">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="936ed-871">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="936ed-871">Az.ApiManagement</span></span>
* <span data-ttu-id="936ed-872">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="936ed-872">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="936ed-873">.NET-NuGet-Version aktualisiert, die keine Einschränkungen für „productId“, „apiId“, „groupId“ und „userId“ erzwingt</span><span class="sxs-lookup"><span data-stu-id="936ed-873">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="936ed-874">**Get-AzApiManagementProduct:** Unterstützung für das Abfragen von Produkten mithilfe der API hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-874">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="936ed-875">**New-AzApiManagementApiRevision:** Problem behoben, aufgrund dessen „ApiRevisionDescription“ beim Erstellen einer neuen API-Revision nicht festgelegt wurde https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="936ed-875">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="936ed-876">Tippfehler im Modell „PsApiManagementOAuth2AuthrozationServer“ korrigiert: PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="936ed-876">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="936ed-877">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="936ed-877">Az.Batch</span></span>
* <span data-ttu-id="936ed-878">Tippfehler in Hilfemeldung und Dokumentation korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="936ed-878">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="936ed-879">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="936ed-879">Az.Cdn</span></span>
* <span data-ttu-id="936ed-880">Tippfehler im Hilfsprogramm für die CDN-Modulkonvertierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-880">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="936ed-881">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="936ed-881">Az.Compute</span></span>
* <span data-ttu-id="936ed-882">VmssId zum Cmdlet „New-AzVMConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-882">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="936ed-883">Parameter „TerminateScheduledEvents“ und „TerminateScheduledEventNotBeforeTimeoutInMinutes“ zu „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-883">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="936ed-884">HyperVGeneration-Eigenschaft zu VM-Imageobjekt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-884">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="936ed-885">Host- und HostGroup-Features hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-885">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="936ed-886">Neue Cmdlets:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="936ed-886">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="936ed-887">Parameter „HostId“ zu „New-AzVMConfig“ und „New-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-887">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="936ed-888">Beispiel in der Dokumentation zu „Invoke-AzVMRunCommand“ zur Verwendung des richtigen Parameternamens aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-888">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="936ed-889">Beschreibung für „-VolumeType“ in der Referenzdokumentation zu „Set-AzVMDiskEncryptionExtension“ und „Set-AzVmssDiskEncryptionExtension“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-889">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="936ed-890">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="936ed-890">Az.DataFactory</span></span>
* <span data-ttu-id="936ed-891">Tippfehler in der Dokumentation zu „New-AzDataFactoryEncryptValue“ korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="936ed-891">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="936ed-892">Version des ADF .NET SDK auf 4.1.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-892">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="936ed-893">Parameter „DataProxyIntegrationRuntimeName“, „DataProxyStagingLinkedServiceName“ und „DataProxyStagingPath“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um die Einrichtung der selbstgehosteten Integration Runtime als Proxy für die SSIS Integration Runtime zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="936ed-893">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="936ed-894">„PSTriggerRun“ zum Anzeigen der ausgelösten Pipelines, Meldungen und Eigenschaften und „PSActivityRun“ zum Anzeigen des Aktivitätstyps aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-894">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="936ed-895">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="936ed-895">Az.DataLakeStore</span></span>
* <span data-ttu-id="936ed-896">Hängen von „Get-DataLakeStoreDeletedItem“ aufgrund von Fehlern oder Remoteausnahmen behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-896">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="936ed-897">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="936ed-897">Az.EventHub</span></span>
* <span data-ttu-id="936ed-898">Behebung des Problems #9658: Tippfehler im Parameter „VirtualNteworkRule“ in „Set-AzEventHubNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="936ed-898">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="936ed-899">Behebung des Problems #9558: „Set-AzEventHubNamespace“ verwendet PATCH anstelle von PUT.</span><span class="sxs-lookup"><span data-stu-id="936ed-899">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="936ed-900">Parameter „EnableKafka“ zum Cmdlet „Set-AzEventHubNamespace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-900">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="936ed-901">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="936ed-901">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="936ed-902">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="936ed-902">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="936ed-903">Tippfehler („Azure“ in Kleinbuchstaben) in der Dokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-903">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="936ed-904">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="936ed-904">Az.Monitor</span></span>
* <span data-ttu-id="936ed-905">Falscher Parametername in der Hilfedokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-905">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="936ed-906">Az.Network</span><span class="sxs-lookup"><span data-stu-id="936ed-906">Az.Network</span></span>
* <span data-ttu-id="936ed-907">„New-AzPrivateLinkServiceIpConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-907">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="936ed-908">Parameter „PublicIpAddress“ ausgemustert, da er auf Serverseite nie verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="936ed-908">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="936ed-909">Optionaler Parameter „Primary“ hinzugefügt, der angibt, ob die aktuelle IP-Konfiguration die primäre ist oder nicht</span><span class="sxs-lookup"><span data-stu-id="936ed-909">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="936ed-910">Verbesserte Verarbeitung der Anforderungsfehlerausnahme aus dem SDK: Behebt das Problem, dass vorherige SDK-Ausnahmen nicht richtig behandelt wurden, was dazu führt, dass Schlüsselfehlerdetails nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="936ed-910">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="936ed-911">Validierungslogik für Ipv6-IP-Präfix angepasst, damit auf die richtige IPv6-Präfixlänge geprüft wird</span><span class="sxs-lookup"><span data-stu-id="936ed-911">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="936ed-912">„Get-AzVirtualNetworkSubnetConfig“ aktualisiert: Parametersatz zum Abrufen nach Subnetzressourcen-ID hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-912">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="936ed-913">Aktualisierte Beschreibung des Location-Parameters für „AzNetworkServiceTag“</span><span class="sxs-lookup"><span data-stu-id="936ed-913">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="936ed-914">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="936ed-914">Az.OperationalInsights</span></span>
* <span data-ttu-id="936ed-915">Aktualisierte Dokumentation für „New-AzOperationalInsightsLinuxSyslogDataSource“</span><span class="sxs-lookup"><span data-stu-id="936ed-915">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="936ed-916">Beispiel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-916">Added example</span></span>
    - <span data-ttu-id="936ed-917">Beschreibung für den Parameter „-Name“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-917">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="936ed-918">Beispiel für „New-AzOperationalInsightsWindowsEventDataSource“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-918">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="936ed-919">Beschreibung des Parameters „-Name“ für „New-AzOperationalInsightsWindowsEventDataSource“ geändert</span><span class="sxs-lookup"><span data-stu-id="936ed-919">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="936ed-920">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="936ed-920">Az.RecoveryServices</span></span>
* <span data-ttu-id="936ed-921">„Get-AzRecoveryServicesBackupJobDetail.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-921">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="936ed-922">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="936ed-922">Az.Resources</span></span>
* <span data-ttu-id="936ed-923">Unterstützung für die neue API-Version 2019-05-10 für Microsoft.Resource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-923">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="936ed-924">Unterstützung für „copy.count = 0“ für Variablen, Ressourcen und Eigenschaften hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-924">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="936ed-925">Ressourcen mit „condition = false“ oder „copy.count = 0“ werden im vollständigen Modus gelöscht.</span><span class="sxs-lookup"><span data-stu-id="936ed-925">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="936ed-926">Beispiel zum Hinzufügen einer Richtlinie auf Abonnementebene zur Hilfedokumentation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-926">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="936ed-927">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="936ed-927">Az.ServiceBus</span></span>
* <span data-ttu-id="936ed-928">Behebung des Problems #9658: Tippfehler für Parameter „VirtualNetworkRule“ in „Set-AzServiceBusNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="936ed-928">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="936ed-929">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="936ed-929">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="936ed-930">Neuer Befehl „Test-AzServiceBusNameAvailability“ zum Überprüfen der Verfügbarkeit des Namens für Warteschlange und Thema hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-930">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="936ed-931">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="936ed-931">Az.ServiceFabric</span></span>
* <span data-ttu-id="936ed-932">Fehler bei Cmdlets zum Hinzufügen des Knotentyps korrigiert:</span><span class="sxs-lookup"><span data-stu-id="936ed-932">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="936ed-933">Fehler „NullReferenceException“, wenn die Ressourcengruppe andere VMSS enthielt, die nicht mit dem Service Fabric-Cluster in Zusammenhang stehen</span><span class="sxs-lookup"><span data-stu-id="936ed-933">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="936ed-934">Problembehebung: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="936ed-934">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="936ed-935">Fehler behoben, aufgrund dessen bei einem Cmdlet ein Fehler auftrat, wenn sich „virtualNetwork“ in einer anderen Ressourcengruppe befand als der Cluster</span><span class="sxs-lookup"><span data-stu-id="936ed-935">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="936ed-936">Problembehebung: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="936ed-936">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="936ed-937">Cmdlet „Add-AzServiceFabricApplicationCertificate“ ausgemustert</span><span class="sxs-lookup"><span data-stu-id="936ed-937">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="936ed-938">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="936ed-938">Az.Sql</span></span>
* <span data-ttu-id="936ed-939">Dokumentation alter Überwachungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-939">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="936ed-940">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="936ed-940">Az.Storage</span></span>
* <span data-ttu-id="936ed-941">Hilfe für „Get/Close-AzStorageFileHandle“ aktualisiert (weitere Szenarien zu Cmdlet-Beispielen hinzugefügt und Parameterbeschreibungen aktualisiert)</span><span class="sxs-lookup"><span data-stu-id="936ed-941">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="936ed-942">Unterstützung von „StandardBlobTier“ in Uploadblobs und Kopierblobs</span><span class="sxs-lookup"><span data-stu-id="936ed-942">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="936ed-943">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="936ed-943">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="936ed-944">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="936ed-944">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="936ed-945">Unterstützung der Aktivierungspriorität im Kopierblob</span><span class="sxs-lookup"><span data-stu-id="936ed-945">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="936ed-946">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="936ed-946">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="936ed-947">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="936ed-947">Az.Websites</span></span>
* <span data-ttu-id="936ed-948">Hinzufügen von Erläuterungen zum Parameter „-AppSettings“ in „Set-AzWebApp“ und „Set-AzWebAppSlot“</span><span class="sxs-lookup"><span data-stu-id="936ed-948">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="936ed-949">2.5.0: Juli 2019</span><span class="sxs-lookup"><span data-stu-id="936ed-949">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="936ed-950">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="936ed-950">Az.Accounts</span></span>
* <span data-ttu-id="936ed-951">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="936ed-951">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="936ed-952">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="936ed-952">Az.ApplicationInsights</span></span>
* <span data-ttu-id="936ed-953">Tippfehler im Beispiel in der Dokumentation zu „Remove-AzApplicationInsightsApiKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-953">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="936ed-954">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="936ed-954">Az.Automation</span></span>
* <span data-ttu-id="936ed-955">Tippfehler in der Ressourcenzeichenfolge korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-955">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="936ed-956">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="936ed-956">Az.CognitiveServices</span></span>
* <span data-ttu-id="936ed-957">Unterstützung für NetworkRuleSet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-957">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="936ed-958">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="936ed-958">Az.Compute</span></span>
* <span data-ttu-id="936ed-959">Fehlende Eigenschaften (ComputerName, OsName, OsVersion und HyperVGeneration) des Objekts für die VM-Instanzenansicht hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-959">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="936ed-960">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="936ed-960">Az.ContainerRegistry</span></span>
* <span data-ttu-id="936ed-961">Tippfehler in „Remove-AzContainerRegistryReplication“ für den Replikationsparameter korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-961">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="936ed-962">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="936ed-962">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="936ed-963">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="936ed-963">Az.DataFactory</span></span>
* <span data-ttu-id="936ed-964">Version des ADF .NET SDK auf 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-964">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="936ed-965">Tippfehler in der Dokumentation für „Get-AzDataFactoryV2PipelineRun“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-965">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="936ed-966">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="936ed-966">Az.EventHub</span></span>
* <span data-ttu-id="936ed-967">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="936ed-967">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="936ed-968">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="936ed-968">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="936ed-969">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="936ed-969">Az.KeyVault</span></span>
* <span data-ttu-id="936ed-970">Unterstützung zum Angeben von KeySize für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-970">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="936ed-971">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="936ed-971">Az.LogicApp</span></span>
* <span data-ttu-id="936ed-972">Korrektur für „Get-AzIntegrationAccountMap“ zum Auflisten aller Zuordnungstypen</span><span class="sxs-lookup"><span data-stu-id="936ed-972">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="936ed-973">Neuer MapType-Parameter für Filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-973">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="936ed-974">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="936ed-974">Az.ManagedServices</span></span>
* <span data-ttu-id="936ed-975">Unterstützung für API-Version 2019-06-01 (GA) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-975">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="936ed-976">Az.Network</span><span class="sxs-lookup"><span data-stu-id="936ed-976">Az.Network</span></span>
* <span data-ttu-id="936ed-977">Unterstützung für privaten Endpunkt und privaten Verknüpfungsdienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-977">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="936ed-978">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="936ed-978">New cmdlets</span></span>
        - <span data-ttu-id="936ed-979">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="936ed-979">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="936ed-980">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="936ed-980">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="936ed-981">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="936ed-981">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="936ed-982">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="936ed-982">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="936ed-983">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="936ed-983">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="936ed-984">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="936ed-984">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="936ed-985">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="936ed-985">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="936ed-986">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="936ed-986">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="936ed-987">Folgende Befehle für das Feature aktualisiert: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies für Subnetz in VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="936ed-987">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="936ed-988">„New-AzVirtualNetworkSubnetConfig“, „Set-AzVirtualNetworkSubnetConfig“ und „Add-AzVirtualNetworkSubnetConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-988">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="936ed-989">Optionaler Parameter „-PrivateEndpointNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den privaten Endpunkt in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="936ed-989">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="936ed-990">Optionaler Parameter „-PrivateLinkServiceNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den Privat Link-Dienst in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="936ed-990">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="936ed-991">Der Cmdlet-Parameter „ServiceName“ von AzPrivateLinkService wurde aus Gründen der Abwärtskompatibilität in „Name“ mit dem Alias „ServiceName“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="936ed-991">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="936ed-992">ICMP-Protokoll für Konfigurationen von Netzwerksicherheitsregeln aktiviert</span><span class="sxs-lookup"><span data-stu-id="936ed-992">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="936ed-993">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="936ed-993">Updated cmdlets</span></span>
        - <span data-ttu-id="936ed-994">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="936ed-994">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="936ed-995">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="936ed-995">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="936ed-996">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="936ed-996">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="936ed-997">ConnectionProtocolType (Ikev1/Ikev2) als konfigurierbarer Parameter für „New-AzVirtualNetworkGatewayConnection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-997">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="936ed-998">PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-998">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="936ed-999">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="936ed-999">Updated cmdlet:</span></span>
        - <span data-ttu-id="936ed-1000">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="936ed-1000">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="936ed-1001">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="936ed-1001">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="936ed-1002">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="936ed-1002">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="936ed-1003">Application Gateway-Befehl „New-AzApplicationGatewayProbeConfig“ zur Unterstützung des benutzerdefinierten Ports im Test aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1003">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="936ed-1004">„New-AzApplicationGatewayProbeConfig“ aktualisiert: Optionaler Parameter „Port“ hinzugefügt, der zum Testen des Back-End-Servers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="936ed-1004">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="936ed-1005">Dieser Parameter gilt für Standard_V2 und WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="936ed-1005">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="936ed-1006">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="936ed-1006">Az.OperationalInsights</span></span>
* <span data-ttu-id="936ed-1007">Standardversion für gespeicherte Suchvorgänge auf 1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1007">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="936ed-1008">Verarbeitung des regulären NULL-Ausdrucks in benutzerdefinierten Protokollen korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1008">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="936ed-1009">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="936ed-1009">Az.RecoveryServices</span></span>
* <span data-ttu-id="936ed-1010">„Get-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1010">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="936ed-1011">„Get-AzRecoveryServicesBackupContainer.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1011">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="936ed-1012">„Get-AzRecoveryServicesVault.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1012">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="936ed-1013">„Wait-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1013">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="936ed-1014">„Set-AzRecoveryServicesVaultContext.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1014">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="936ed-1015">„Get-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1015">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="936ed-1016">„Get-AzRecoveryServicesBackupRecoveryPoint.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1016">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="936ed-1017">„Restore-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1017">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="936ed-1018">Dienstaufruf zum Aufheben der Containerregistrierung für Azure-Dateifreigabe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1018">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="936ed-1019">„Set-AzRecoveryServicesAsrAlertSetting.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1019">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="936ed-1020">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="936ed-1020">Az.Resources</span></span>
- <span data-ttu-id="936ed-1021">Fehlendes Cmdlet entfernt, auf das in der Dokumentation zu „New-AzResourceGroupDeployment“ verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="936ed-1021">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="936ed-1022">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1022">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="936ed-1023">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="936ed-1023">Az.ServiceBus</span></span>
* <span data-ttu-id="936ed-1024">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="936ed-1024">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="936ed-1025">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="936ed-1025">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="936ed-1026">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="936ed-1026">Az.Sql</span></span>
* <span data-ttu-id="936ed-1027">Fehlende Beispiele für Cmdlet „Set-AzSqlDatabaseSecondary“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1027">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="936ed-1028">Festlegen wiederkehrender Überprüfungen der Sicherheitsrisikobewertung ohne Angabe von E-Mail-Adressen korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1028">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="936ed-1029">Tippfehler in einer Warnmeldung korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1029">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="936ed-1030">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="936ed-1030">Az.Storage</span></span>
* <span data-ttu-id="936ed-1031">Beispiel in Referenzdokumentation für „Get-AzStorageAccount“ aktualisiert, sodass der richtige Parametername verwendet wird</span><span class="sxs-lookup"><span data-stu-id="936ed-1031">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="936ed-1032">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="936ed-1032">Az.StorageSync</span></span>
* <span data-ttu-id="936ed-1033">Cmdlet „Invoke-AzStorageSyncChangeDetection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1033">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="936ed-1034">Problem 9551 zur Berücksichtigung von „TierFilesOlderThanDays“ behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-1034">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="936ed-1035">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="936ed-1035">Az.Websites</span></span>
* <span data-ttu-id="936ed-1036">Problem behoben, aufgrund dessen einige SiteConfig-Eigenschaften von „Get-AzWebApp“ und „Set-AzWebApp“ nicht zurückgegeben wurden</span><span class="sxs-lookup"><span data-stu-id="936ed-1036">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="936ed-1037">Neuer Standortparameter zu „Get-AzDeletedWebApp“ und „Restore-AzDeletedWebApp“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1037">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="936ed-1038">Fehler beim Klonen von Web-App-Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-1038">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="936ed-1039">2.4.0 – Juli 2019</span><span class="sxs-lookup"><span data-stu-id="936ed-1039">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="936ed-1040">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="936ed-1040">Az.Accounts</span></span>
* <span data-ttu-id="936ed-1041">Unterstützung für Profil-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1041">Add support for profile cmdlets</span></span>
* <span data-ttu-id="936ed-1042">Unterstützung für Umgebungen und Datenebenen in generierten Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1042">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="936ed-1043">Korrektur eines Fehlers, bei dem in einigen Fällen ein falscher Endpunkt für Datenebenen-Cmdlets in Windows PowerShell verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="936ed-1043">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="936ed-1044">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="936ed-1044">Az.Advisor</span></span>
* <span data-ttu-id="936ed-1045">Allgemein verfügbares Release von Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="936ed-1045">GA release of Az.Advisor</span></span>
* <span data-ttu-id="936ed-1046">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="936ed-1046">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="936ed-1047">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="936ed-1047">Az.ApiManagement</span></span>
* <span data-ttu-id="936ed-1048">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="936ed-1048">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="936ed-1049">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="936ed-1049">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="936ed-1050">Unterstützung für Abfragen von Abonnements nach Benutzer und Produkt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1050">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="936ed-1051">Unterstützung für Abfragen anhand des Umfangs hinzugefügt, „/“, „/apis“, „/apis/echo-api“</span><span class="sxs-lookup"><span data-stu-id="936ed-1051">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="936ed-1052">Behebung von Problem https://github.com/Azure/azure-powershell/issues/9307 und https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="936ed-1052">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="936ed-1053">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="936ed-1053">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="936ed-1054">Unterstützung für die Angabe von „ApiVersion“ und „ApiVersionSetId“ beim Importieren von APIs hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1054">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="936ed-1055">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="936ed-1055">Az.Automation</span></span>
* <span data-ttu-id="936ed-1056">Fehler beim Cmdlet „Set-AzAutomationConnectionFieldValue“ für die Verarbeitung des Zeichenfolgewerts behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-1056">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="936ed-1057">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="936ed-1057">Az.Compute</span></span>
* <span data-ttu-id="936ed-1058">Parameter „HyperVGeneration“ zu New-AzImageConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1058">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="936ed-1059">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="936ed-1059">Az.DataFactory</span></span>
* <span data-ttu-id="936ed-1060">Aktualisierung der Ausgabe von ADF-Cmdlets für das Abrufen von Aktivitäts-, Pipeline- und Auslöserausführungen, um die Pipe „Select-Object“ zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="936ed-1060">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="936ed-1061">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="936ed-1061">Az.EventGrid</span></span>
* <span data-ttu-id="936ed-1062">Tippfehler in Dokumentation zu 'New-AzEventGridSubscription' behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-1062">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="936ed-1063">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="936ed-1063">Az.IotHub</span></span>
* <span data-ttu-id="936ed-1064">Unterstützung für das erneute Generieren von Autorisierungsrichtlinienschlüsseln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1064">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="936ed-1065">Az.Network</span><span class="sxs-lookup"><span data-stu-id="936ed-1065">Az.Network</span></span>
* <span data-ttu-id="936ed-1066">„RoutingPreference“ zu öffentlichen IP-Tags hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1066">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="936ed-1067">Beispiele für Referenzdokumentation zu „Get-AzNetworkServiceTag“ verbessert</span><span class="sxs-lookup"><span data-stu-id="936ed-1067">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="936ed-1068">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="936ed-1068">Az.PolicyInsights</span></span>
* <span data-ttu-id="936ed-1069">Fehlerbehebung für Nullverweis in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="936ed-1069">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="936ed-1070">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="936ed-1070">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="936ed-1071">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="936ed-1071">Az.OperationalInsights</span></span>
* <span data-ttu-id="936ed-1072">Zurückgegebenes CustomLog-Datenquellenmodell in Get-AzOperationalInsightsDataSource korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1072">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="936ed-1073">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="936ed-1073">Az.RecoveryServices</span></span>
* <span data-ttu-id="936ed-1074">Fehlerbehebung für Befehl „get-policy“ IaaSVMs</span><span class="sxs-lookup"><span data-stu-id="936ed-1074">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="936ed-1075">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="936ed-1075">Az.Resources</span></span>
    - <span data-ttu-id="936ed-1076">Hilfetext für Parameter „-Top“ von „Get-AzPolicyState“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1076">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="936ed-1077">Clientseitige Unterstützung von Paginierung für „Get-AzPolicyAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1077">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="936ed-1078">Neue Parameter für „Set-AzPolicyAssignment“, „-PolicyParameters“ und „-PolicyParametersObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1078">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="936ed-1079">Einige Aktualisierungen von Dokumentationen und Beispielen für Policy-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="936ed-1079">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="936ed-1080">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="936ed-1080">Az.ServiceBus</span></span>
* <span data-ttu-id="936ed-1081">Korrektur für Problem Nr. 4938: „New-AzureRmServiceBusQueue“ gibt beim Festlegen von „MaxSizeInMegabytes“ „BadRequest“ zurück</span><span class="sxs-lookup"><span data-stu-id="936ed-1081">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="936ed-1082">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="936ed-1082">Az.Sql</span></span>
* <span data-ttu-id="936ed-1083">Instanzfailovergruppen-Cmdlets aus Vorschauversion in öffentliche Version hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1083">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="936ed-1084">Unterstützung von Azure SQL Server\Datenbanküberwachung mit neuen Cmdlets</span><span class="sxs-lookup"><span data-stu-id="936ed-1084">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="936ed-1085">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="936ed-1085">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="936ed-1086">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="936ed-1086">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="936ed-1087">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="936ed-1087">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="936ed-1088">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="936ed-1088">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="936ed-1089">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="936ed-1089">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="936ed-1090">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="936ed-1090">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="936ed-1091">E-Mail-Einschränkungen aus Einstellungen der Sicherheitsrisikobewertung entfernt</span><span class="sxs-lookup"><span data-stu-id="936ed-1091">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="936ed-1092">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="936ed-1092">Az.Storage</span></span>
* <span data-ttu-id="936ed-1093">Zwei Parameter („-IndexDocument“ und „-ErrorDocument404Path“) in folgendem Cmdlet von erforderlich in optional geändert:</span><span class="sxs-lookup"><span data-stu-id="936ed-1093">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="936ed-1094">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="936ed-1094">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="936ed-1095">Hilfe zu „Get-AzStorageBlobContent“ mit neuem Beispiel ergänzt</span><span class="sxs-lookup"><span data-stu-id="936ed-1095">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="936ed-1096">Anzeige von mehr Fehlerinformationen beim Fehlschlagen eines Cmdlets mit „StorageException“</span><span class="sxs-lookup"><span data-stu-id="936ed-1096">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="936ed-1097">Unterstützung für das Erstellen oder Aktualisieren von Speicherkonten mit Azure Files AAD-DS-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="936ed-1097">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="936ed-1098">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="936ed-1098">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="936ed-1099">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="936ed-1099">Set-AzStorageAccount</span></span>
* <span data-ttu-id="936ed-1100">Unterstützung für das Auflisten oder Schließen von Dateihandles einer Dateifreigabe, eines Dateiverzeichnisses oder einer Datei</span><span class="sxs-lookup"><span data-stu-id="936ed-1100">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="936ed-1101">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="936ed-1101">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="936ed-1102">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="936ed-1102">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="936ed-1103">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="936ed-1103">Az.StorageSync</span></span>
* <span data-ttu-id="936ed-1104">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="936ed-1104">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="936ed-1105">2.3.2 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="936ed-1105">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="936ed-1106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="936ed-1106">Az.Accounts</span></span>
* <span data-ttu-id="936ed-1107">Fehler behoben, aufgrund dessen in manchen Fällen eine falsche URL für Funktionsaufrufe verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="936ed-1107">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="936ed-1108">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="936ed-1108">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="936ed-1109">Problem mit Aliasen zwischen AzureRM und Azure-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-1109">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="936ed-1110">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="936ed-1110">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="936ed-1111">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="936ed-1111">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="936ed-1112">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="936ed-1112">Az.Compute</span></span>
* <span data-ttu-id="936ed-1113">Die einfachen Parametersätze „New-AzVm“ und „New-AzVmss“ akzeptieren jetzt den Parameter „ProximityPlacementGroup“.</span><span class="sxs-lookup"><span data-stu-id="936ed-1113">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="936ed-1114">Tippfehler in der Referenzdokumentation für „New-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-1114">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="936ed-1115">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="936ed-1115">Az.Dns</span></span>
* <span data-ttu-id="936ed-1116">Tippfehler in den Hilfebeispielen zu „Set-AzDnsZone“ behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-1116">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="936ed-1117">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="936ed-1117">Az.EventGrid</span></span>
* <span data-ttu-id="936ed-1118">Zur Verwendung der API-Version 2019-06-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1118">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="936ed-1119">Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="936ed-1119">New cmdlets:</span></span>
    - <span data-ttu-id="936ed-1120">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="936ed-1120">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="936ed-1121">Erstellt eine neue Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="936ed-1121">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="936ed-1122">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="936ed-1122">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="936ed-1123">Ruft die Details einer Event Grid-Domäne oder eine Liste aller Event Grid-Domänen im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="936ed-1123">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="936ed-1124">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="936ed-1124">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="936ed-1125">Entfernt eine Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="936ed-1125">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="936ed-1126">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="936ed-1126">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="936ed-1127">Generiert den freigegebenen Zugriffsschlüssel für eine Azure Event Grid-Domäne erneut.</span><span class="sxs-lookup"><span data-stu-id="936ed-1127">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="936ed-1128">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="936ed-1128">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="936ed-1129">Ruft die freigegebenen Zugriffsschlüssel ab, die zum Veröffentlichen von Ereignissen in einer Event Grid-Domäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="936ed-1129">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="936ed-1130">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="936ed-1130">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="936ed-1131">Erstellt ein neues Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="936ed-1131">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="936ed-1132">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="936ed-1132">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="936ed-1133">Ruft die Details eines Event Grid-Domänenthemas oder eine Liste aller Event Grid-Domänenthemen unter der jeweiligen Event Grid-Domäne im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="936ed-1133">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="936ed-1134">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="936ed-1134">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="936ed-1135">Entfernt ein vorhandenes Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="936ed-1135">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="936ed-1136">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="936ed-1136">Updated cmdlets:</span></span>
    - <span data-ttu-id="936ed-1137">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="936ed-1137">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="936ed-1138">Neue erforderliche Parameter zur Unterstützung des Pipings für die neue Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="936ed-1138">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="936ed-1139">Neue erforderliche Parameter zum Angeben des neuen Event Grid-Domänennamens und/oder Namens des Event Grid-Domänenthemas hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="936ed-1139">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="936ed-1140">Neue Parametersätze für Domänen und Domänenthemen hinzugefügt, um die Wiederverwendung vorhandener Parameter zuzulassen (‚z. B. „EndPointType“, „SubjectBeginsWith“ usw.)</span><span class="sxs-lookup"><span data-stu-id="936ed-1140">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="936ed-1141">Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="936ed-1141">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="936ed-1142">Ablaufdatum des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="936ed-1142">Event subscription expiration date,</span></span>
            - <span data-ttu-id="936ed-1143">Erweiterte Filterparameter</span><span class="sxs-lookup"><span data-stu-id="936ed-1143">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="936ed-1144">Neue Enumeration für „servicebusqueue“ als Ziel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1144">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="936ed-1145">Verwendung der Option „All“ in „-IncludedEventType“ gesperrt und wie folgt ersetzt</span><span class="sxs-lookup"><span data-stu-id="936ed-1145">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="936ed-1146">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="936ed-1146">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="936ed-1147">Neue optionale Parameter („Top“, „ODataQuery“ und „NextLink“) zur Unterstützung der Ergebnispaginierung und -filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1147">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="936ed-1148">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="936ed-1148">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="936ed-1149">Neue erforderliche Parameter zur Unterstützung des Pipings für die Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Entfernen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="936ed-1149">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="936ed-1150">Neue erforderliche Parameter zum Angeben des Event Grid-Domänennamens und/oder Event Grid-Domänenthemanamens hinzugefügt, um das Entfernen vorhandener Ereignisabonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="936ed-1150">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="936ed-1151">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="936ed-1151">Az.FrontDoor</span></span>
* <span data-ttu-id="936ed-1152">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="936ed-1152">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="936ed-1153">Unterstützung von Transformationen und neuen Wert für den Operator zum automatischen Vervollständigen (RegEx) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1153">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="936ed-1154">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="936ed-1154">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="936ed-1155">Neue Werte für automatisches Vervollständigen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1155">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="936ed-1156">Az.Network</span><span class="sxs-lookup"><span data-stu-id="936ed-1156">Az.Network</span></span>
* <span data-ttu-id="936ed-1157">Unterstützung für Virtual Network-Gatewayressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1157">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="936ed-1158">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="936ed-1158">New cmdlets</span></span>
        - <span data-ttu-id="936ed-1159">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="936ed-1159">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="936ed-1160">AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="936ed-1160">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="936ed-1161">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="936ed-1161">New cmdlets</span></span> 
        - <span data-ttu-id="936ed-1162">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="936ed-1162">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="936ed-1163">„PrivatePrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1163">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="936ed-1164">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="936ed-1164">New cmdlets</span></span> 
        - <span data-ttu-id="936ed-1165">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="936ed-1165">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="936ed-1166">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="936ed-1166">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="936ed-1167">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="936ed-1167">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="936ed-1168">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="936ed-1168">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="936ed-1169">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="936ed-1169">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="936ed-1170">„PrivateEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1170">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="936ed-1171">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="936ed-1171">New cmdlets</span></span>
        - <span data-ttu-id="936ed-1172">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="936ed-1172">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="936ed-1173">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="936ed-1173">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="936ed-1174">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="936ed-1174">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="936ed-1175">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="936ed-1175">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="936ed-1176">Folgende Befehle für das Feature aktualisiert: UseLocalAzureIpAddress-Flag für „VpnConnection“</span><span class="sxs-lookup"><span data-stu-id="936ed-1176">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="936ed-1177">„New-AzVpnConnection§ „ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="936ed-1177">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="936ed-1178">„Set-AzVpnConnection“ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="936ed-1178">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="936ed-1179">Schreibgeschütztes Feld „PeeredConnections“ beim ExpressRoute-Peering hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1179">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="936ed-1180">Schreibgeschütztes Feld „GlobalReachEnabled“ in ExpressRoute hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1180">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="936ed-1181">Breaking Change-Attribut hinzugefügt, um auf das veraltete Feld „AllowGlobalReach“ im ExpressRouteCircuit-Modell hinzuweisen</span><span class="sxs-lookup"><span data-stu-id="936ed-1181">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="936ed-1182">Fehler 8756 bei der Verwendung von „TargetListenerID“ mit AzApplicationGatewayRedirectConfiguration-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-1182">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="936ed-1183">Fehler in „New-AzApplicationGatewayPathRuleConfig“ behoben, aufgrund dessen der Regelsatz für erneutes Generieren nicht festgelegt werden konnte</span><span class="sxs-lookup"><span data-stu-id="936ed-1183">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="936ed-1184">Fehler bei der Anzeige von „VirtualNetworkTaps“ in „NetworkInterfaceIpConfiguration“ behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-1184">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="936ed-1185">Cortex-Get-Cmdlets zum Auflisten aller Komponenten korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1185">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="936ed-1186">Problem beim Erstellen des festen VirtualHub-Verweises für ExpressRouteGateways behoben (VpnGateway)</span><span class="sxs-lookup"><span data-stu-id="936ed-1186">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="936ed-1187">Unterstützung für Verfügbarkeitszonen in AzureFirewall und NatGateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1187">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="936ed-1188">Cmdlet „Get-AzNetworkServiceTag“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1188">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="936ed-1189">Unterstützung für mehrere öffentliche IP-Adressen für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1189">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="936ed-1190">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="936ed-1190">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="936ed-1191">Parameter „-PublicIpAddress“ hinzugefügt, der ein oder mehre öffentliche IP-Adressobjekte akzeptiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1191">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="936ed-1192">Parameter „- VirtualNetwork“ hinzugefügt, der ein Virtual Network-Objekt akzeptiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1192">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="936ed-1193">Methoden „AddPublicIpAddress“ und „RemovePublicIpAddress“ für Firewallobjekte hinzugefügt (akzeptieren ein öffentliches IP-Adressobjekt als Eingabe)</span><span class="sxs-lookup"><span data-stu-id="936ed-1193">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="936ed-1194">Parameter „-PublicIpName“ und „-VirtualNetworkName“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1194">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="936ed-1195">Folgende Befehle für das Feature aktualisiert: VpnClient-AAD-Authentifizierungsoptionen auf die Gatewayressource des virtuellen Netzwerkgateways festgelegt</span><span class="sxs-lookup"><span data-stu-id="936ed-1195">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="936ed-1196">„New-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1196">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="936ed-1197">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-1197">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="936ed-1198">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionaler Switch-Parameter „RemoveAadAuthentication“ zum Entfernen von VpnClient-AAD-Authentifizierungsoptionen aus dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1198">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="936ed-1199">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="936ed-1199">Az.OperationalInsights</span></span>
* <span data-ttu-id="936ed-1200">Tarif **pergb2018** im Befehl „New-AzureRmOperationalInsightsWorkspace“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="936ed-1200">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="936ed-1201">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="936ed-1201">Az.Resources</span></span>
* <span data-ttu-id="936ed-1202">Unterstützung für zusätzliche Optionen zum Exportieren von Vorlagen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1202">Support for additional Template Export options</span></span>
    - <span data-ttu-id="936ed-1203">Parameter „-SkipResourceNameParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1203">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="936ed-1204">Parameter -SkipAllParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1204">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="936ed-1205">Parameter „-Resource“ zu „Export-AzResourceGroup“ hinzugefügt, um das Filtern exportierter Ressourcen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="936ed-1205">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="936ed-1206">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="936ed-1206">Az.ServiceFabric</span></span>
* <span data-ttu-id="936ed-1207">Problem beim Hinzufügen des Zertifikats mit „ByExistingKeyVault“ behoben (Abruf des falschen Fingerabdrucks in manchen Fällen)</span><span class="sxs-lookup"><span data-stu-id="936ed-1207">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="936ed-1208">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="936ed-1208">Az.Sql</span></span>
* <span data-ttu-id="936ed-1209">Suffix des Advanced Threat Protection-Endpunkts korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1209">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="936ed-1210">Durch Advanced Data Security ermöglichte Außerkraftsetzungen der Advanced Threat Protection-Richtlinie korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1210">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="936ed-1211">Neue Cmdlets für „Management.Sql“ ermöglichen Kunden das Hinzufügen von TDE-Schlüsseln und Festlegen der TDE-Schutzvorrichtung für verwaltete Instanzen.</span><span class="sxs-lookup"><span data-stu-id="936ed-1211">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="936ed-1212">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="936ed-1212">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="936ed-1213">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="936ed-1213">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="936ed-1214">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="936ed-1214">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="936ed-1215">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="936ed-1215">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="936ed-1216">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="936ed-1216">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="936ed-1217">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="936ed-1217">Az.Storage</span></span>
* <span data-ttu-id="936ed-1218">Unterstützung von „FileStorage“ und „SkuName Premium_ZRS“ beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="936ed-1218">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="936ed-1219">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="936ed-1219">New-AzStorageAccount</span></span>
* <span data-ttu-id="936ed-1220">Überarbeitete Beschreibung des Cmdlets für die Unveränderlichkeit von Blobs</span><span class="sxs-lookup"><span data-stu-id="936ed-1220">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="936ed-1221">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="936ed-1221">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="936ed-1222">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="936ed-1222">Az.Websites</span></span>
* <span data-ttu-id="936ed-1223">Optimiert „Get-AzWebAppCertificate“, um nach der Ressourcengruppe auf dem Server zu filtern (nicht auf dem Client)</span><span class="sxs-lookup"><span data-stu-id="936ed-1223">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="936ed-1224">Switch-Parameter „-UseDisasterRecovery“ für „Get-AzWebAppSnapshot“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1224">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="936ed-1225">2.2.0 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="936ed-1225">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="936ed-1226">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="936ed-1226">Az.Cdn</span></span>
* <span data-ttu-id="936ed-1227">Es wurden Cmdlets aktualisiert, um das rulesEngine-Feature basierend auf der API-Version 2019-04-15 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="936ed-1227">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="936ed-1228">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="936ed-1228">Az.Compute</span></span>
* <span data-ttu-id="936ed-1229">Der Parameter `NoWait` wurde hinzugefügt, der den Vorgang startet und sofort zurückkehrt, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="936ed-1229">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="936ed-1230">Aktualisierte Cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="936ed-1230">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="936ed-1231">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="936ed-1231">Az.EventHub</span></span>
* <span data-ttu-id="936ed-1232">Fehlerbehebung für #9231 – Get-AzEventHubNamespace gibt keine Tags zurück</span><span class="sxs-lookup"><span data-stu-id="936ed-1232">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="936ed-1233">Fehlerbehebung für #9230 – Get-AzEventHubNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="936ed-1233">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="936ed-1234">Az.Network</span><span class="sxs-lookup"><span data-stu-id="936ed-1234">Az.Network</span></span>
* <span data-ttu-id="936ed-1235">ResourceId und InputObject wurden für NAT Gateway aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1235">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="936ed-1236">Es wurde ein Alias für ResourceId und InputObjectr hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1236">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="936ed-1237">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="936ed-1237">Az.PolicyInsights</span></span>
* <span data-ttu-id="936ed-1238">Fehlerbehebung für Nullverweis in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="936ed-1238">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="936ed-1239">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="936ed-1239">Az.RecoveryServices</span></span>
* <span data-ttu-id="936ed-1240">Minimale Aufbewahrung in Tagen für IaaSVM-Richtlinie wurde von 1 in 7 geändert</span><span class="sxs-lookup"><span data-stu-id="936ed-1240">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="936ed-1241">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="936ed-1241">Az.ServiceBus</span></span>
* <span data-ttu-id="936ed-1242">Fehlerbehebung für #9182 – Get-AzServiceBusNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="936ed-1242">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="936ed-1243">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="936ed-1243">Az.ServiceFabric</span></span>
* <span data-ttu-id="936ed-1244">Tippfehler in Fehlermeldung für Update-AzServiceFabricReliability wurde behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-1244">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="936ed-1245">Fehlendes Zeichen in Service Fabric-Befehlszeilen wurde behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-1245">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="936ed-1246">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="936ed-1246">Az.Sql</span></span>
* <span data-ttu-id="936ed-1247">Der DnsZonePartner-Parameter für das Cmdlet New-AzureSqlInstance wurde hinzugefügt, um AutoDr für verwaltete Instanzen zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="936ed-1247">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="936ed-1248">Das Cmdlet Get-AzSqlDatabaseSecureConnectionPolicy wird eingestellt</span><span class="sxs-lookup"><span data-stu-id="936ed-1248">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="936ed-1249">Cmdlets zum Schutz vor Bedrohungen werden in „Advanced Threat Protection“ (Erweiterter Schutz vor Bedrohungen) umbenannt</span><span class="sxs-lookup"><span data-stu-id="936ed-1249">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="936ed-1250">New-AzSqlInstance – Die Parameter StorageSizeInGB und LicenseType sind jetzt optional</span><span class="sxs-lookup"><span data-stu-id="936ed-1250">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="936ed-1251">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="936ed-1251">Az.Websites</span></span>
* <span data-ttu-id="936ed-1252">Das Problem, bei dem die Verwendung von Set-AzWebApp und Set-AzWebAppSlot mit der -WebApp-Eigenschaft die Tags entfernt hat, wurde behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-1252">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="936ed-1253">2.1.0 – Mai 2019</span><span class="sxs-lookup"><span data-stu-id="936ed-1253">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="936ed-1254">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="936ed-1254">Az.ApiManagement</span></span>
* <span data-ttu-id="936ed-1255">Es wurden neue Cmdlets zum Verwalten der Diagnose im globalen sowie im API-Bereich erstellt</span><span class="sxs-lookup"><span data-stu-id="936ed-1255">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="936ed-1256">**Get-AzApiManagementDiagnostic**: Abrufen der Diagnose, die im globalen oder im API-Bereich konfiguriert wurde</span><span class="sxs-lookup"><span data-stu-id="936ed-1256">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="936ed-1257">**New-AzApiManagementDiagnostic**: Erstellen neuer Diagnosen im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="936ed-1257">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="936ed-1258">**New-AzApiManagementHttpMessageDiagnostic**: Erstellen einer Diagnoseeinstellung für die zu protokollierenden Kopfzeilen und für die Größe der Bytes für den Text</span><span class="sxs-lookup"><span data-stu-id="936ed-1258">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="936ed-1259">**New-AzApiManagementPipelineDiagnosticSetting**: Erstellen von Diagnoseeinstellungen für ein-/ausgehende HTTP-Nachrichten für das Gateway</span><span class="sxs-lookup"><span data-stu-id="936ed-1259">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="936ed-1260">**New-AzApiManagementSamplingSetting**: Erstellen der Einstellung „Sampling“ für die Anforderungen/Antworten für eine Diagnose</span><span class="sxs-lookup"><span data-stu-id="936ed-1260">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="936ed-1261">**Remove-AzApiManagementDiagnostic**: Entfernen einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="936ed-1261">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="936ed-1262">**Set-AzApiManagementDiagnostic**: Aktualisieren einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="936ed-1262">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="936ed-1263">Es wurden neue Cmdlets für die Cacheverwaltung im ApiManagement-Dienst erstellt</span><span class="sxs-lookup"><span data-stu-id="936ed-1263">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="936ed-1264">**Get-AzApiManagementCache**: Abrufen der Details des durch den Bezeichner angegebenen Caches oder aller Caches</span><span class="sxs-lookup"><span data-stu-id="936ed-1264">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="936ed-1265">**New-AzApiManagementCache**: Erstellen eines neuen „standardmäßigen“ Caches oder eines Caches in einer bestimmten „Region“ von Azure</span><span class="sxs-lookup"><span data-stu-id="936ed-1265">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="936ed-1266">**Remove-AzApiManagementCache**: Entfernen eines Caches</span><span class="sxs-lookup"><span data-stu-id="936ed-1266">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="936ed-1267">**Update-AzApiManagementCache**: Aktualisieren eines Caches</span><span class="sxs-lookup"><span data-stu-id="936ed-1267">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="936ed-1268">Es wurden neue Cmdlets zur Verwaltung von API-Schemas erstellt</span><span class="sxs-lookup"><span data-stu-id="936ed-1268">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="936ed-1269">**New-AzApiManagementSchema**: Erstellen eines neuen Schemas für eine API</span><span class="sxs-lookup"><span data-stu-id="936ed-1269">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="936ed-1270">**Get-AzApiManagementSchema**: Abrufen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="936ed-1270">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="936ed-1271">**Remove-AzApiManagementSchema**: Entfernen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="936ed-1271">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="936ed-1272">**Set-AzApiManagementSchema**: Aktualisieren des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="936ed-1272">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="936ed-1273">Es wurde ein neues Cmdlet zum Generieren eines Benutzertokens erstellt</span><span class="sxs-lookup"><span data-stu-id="936ed-1273">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="936ed-1274">**New-AzApiManagementUserToken**: Generieren eines neuen Benutzertokens, das standardmäßig für acht Stunden gültig ist. Mit diesem Cmdlet kann das Token für den „GIT“-Benutzer generiert werden./</span><span class="sxs-lookup"><span data-stu-id="936ed-1274">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="936ed-1275">Es wurde ein neues Cmdlet zum Abrufen des Netzwerkstatus erstellt</span><span class="sxs-lookup"><span data-stu-id="936ed-1275">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="936ed-1276">**Get-AzApiManagementNetworkStatus**: Abrufen der Netzwerkstatuskonnektivität von Ressourcen, von denen der API Management-Dienst abhängig ist</span><span class="sxs-lookup"><span data-stu-id="936ed-1276">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="936ed-1277">Dies ist hilfreich, wenn Sie den ApiManagement-Dienst in einem virtuellen Netzwerk bereitstellen und überprüfen, ob eine der Abhängigkeiten fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="936ed-1277">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="936ed-1278">Das Cmdlet **New-AzApiManagement** wurde zum Verwalten des ApiManagement-Diensts aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1278">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="936ed-1279">Die Unterstützung für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1279">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="936ed-1280">Die Unterstützung zum Aktivieren des Flags „EnableClientCertificate“ für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1280">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="936ed-1281">Das neue Cmdlet **New-AzApiManagementSslSetting** ermöglicht die Konfiguration der „TLS/SSL“-Einstellung für „Back-End“ und „Front-End“</span><span class="sxs-lookup"><span data-stu-id="936ed-1281">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="936ed-1282">Dies kann auch dazu verwendet werden, um „Verschlüsselungen“ wie „3DES“ und „ServerProtokolle“ wie „Http2“ für das „Front-End“ eines ApiManagement-Diensts zu konfigurieren</span><span class="sxs-lookup"><span data-stu-id="936ed-1282">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="936ed-1283">Die Unterstützung für die Konfiguration des Hostnamens „DeveloperPortal“ wurde zum ApiManagement-Dienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1283">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="936ed-1284">Die **Get-AzApiManagementSsoToken**-Cmdlets wurden aktualisiert, um das Objekt „PsApiManagement“ als Eingabe zu übernehmen</span><span class="sxs-lookup"><span data-stu-id="936ed-1284">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="936ed-1285">Das Cmdlet wurde aktualisiert, um Fehlermeldungen inline anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="936ed-1285">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="936ed-1286">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Fehlercode: ValidationError-Fehlermeldung: Mindestens ein Feld enthält ungültige Werte: Fehlerdetails: [Code=ValidationError, Message=Fehler in Element 'log-to-eventhub' in Zeile 3, Spalte 10: Protokollierungstool nicht gefunden, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="936ed-1286">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="936ed-1287">Cmdlet **Export-AzApiManagementApi** wurde für den Export von APIs im Format „OpenApi 3.0“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1287">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="936ed-1288">Cmdlet **Import-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1288">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="936ed-1289">Zum Importieren der API aus der „OpenApi 3.0“-Dokumentspezifikation</span><span class="sxs-lookup"><span data-stu-id="936ed-1289">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="936ed-1290">Zur Außerkraftsetzung der „PsApiManagementSchema“-Eigenschaft, die in einem beliebigen Dokument („Swagger“, „Wadl“, „Wsdl“, „OpenApi“) angegeben ist</span><span class="sxs-lookup"><span data-stu-id="936ed-1290">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="936ed-1291">Zur Außerkraftsetzung der „ServiceUrl“-Eigenschaft, die in einem beliebigen Dokument angegeben ist</span><span class="sxs-lookup"><span data-stu-id="936ed-1291">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="936ed-1292">Cmdlet **Get-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="936ed-1292">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="936ed-1293">Cmdlet **Set-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ und im Format mit XML-Escapezeichen mit „xml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="936ed-1293">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="936ed-1294">Cmdlet **New-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1294">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="936ed-1295">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="936ed-1295">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="936ed-1296">Zum Erstellen einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="936ed-1296">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="936ed-1297">Zum Klonen einer API mithilfe von „SourceApiId“ und „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="936ed-1297">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="936ed-1298">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="936ed-1298">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="936ed-1299">Cmdlet **Set-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1299">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="936ed-1300">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="936ed-1300">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="936ed-1301">Zum Aktualisieren einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="936ed-1301">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="936ed-1302">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="936ed-1302">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="936ed-1303">Cmdlet **New-AzApiManagementRevision** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1303">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="936ed-1304">Zum Klonen (Kopiertags, Produkte, Vorgänge und Richtlinien) einer vorhandenen Version mithilfe von „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="936ed-1304">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="936ed-1305">Die neue Version übernimmt die „ApiId“ des übergeordneten Elements</span><span class="sxs-lookup"><span data-stu-id="936ed-1305">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="936ed-1306">Zum Bereitstellen einer „ApiRevisionDescription“</span><span class="sxs-lookup"><span data-stu-id="936ed-1306">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="936ed-1307">Zur Außerkraftsetzung der „ServiceUrl“ beim Klonen einer API</span><span class="sxs-lookup"><span data-stu-id="936ed-1307">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="936ed-1308">Cmdlet **New-AzApiManagementIdentityProvider** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1308">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="936ed-1309">Zum Konfigurieren von „AAD“ oder „AADB2C“ mit einer „Authority“</span><span class="sxs-lookup"><span data-stu-id="936ed-1309">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="936ed-1310">Zum Einrichten von „SignupPolicy“, „SigninPolicy“, „ProfileEditingPolicy“ und „PasswordResetPolicy“</span><span class="sxs-lookup"><span data-stu-id="936ed-1310">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="936ed-1311">Cmdlet **New-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1311">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="936ed-1312">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="936ed-1312">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="936ed-1313">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="936ed-1313">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="936ed-1314">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1314">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="936ed-1315">Cmdlet **Set-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1315">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="936ed-1316">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="936ed-1316">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="936ed-1317">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="936ed-1317">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="936ed-1318">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1318">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="936ed-1319">Folgende Cmdlets wurden aktualisiert, um „ResourceId“ als Eingabe zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="936ed-1319">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="936ed-1320">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="936ed-1320">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="936ed-1321">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="936ed-1321">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="936ed-1322">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="936ed-1322">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="936ed-1323">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="936ed-1323">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="936ed-1324">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="936ed-1324">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="936ed-1325">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="936ed-1325">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="936ed-1326">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="936ed-1326">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="936ed-1327">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="936ed-1327">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="936ed-1328">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="936ed-1328">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="936ed-1329">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="936ed-1329">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="936ed-1330">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="936ed-1330">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="936ed-1331">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="936ed-1331">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="936ed-1332">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="936ed-1332">Az.Automation</span></span>
* <span data-ttu-id="936ed-1333">Get-AzAutomationJobOutputRecord wurde aktualisiert, um JSON- und Textdatensatzwerte zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="936ed-1333">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="936ed-1334">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="936ed-1334">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="936ed-1335">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="936ed-1335">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="936ed-1336">Das Verhalten von Start-AzAutomationDscCompilationJob wurde geändert, um den Auftrag einfach zu starten, anstatt auf dessen Abschluss zu warten</span><span class="sxs-lookup"><span data-stu-id="936ed-1336">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="936ed-1337">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="936ed-1337">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="936ed-1338">Fehlerbehebung für Get-AzAutomationDscNode, wenn die Verwendung von „-Name“ alle Knoten zurückgibt</span><span class="sxs-lookup"><span data-stu-id="936ed-1338">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="936ed-1339">Jetzt wird nur der übereinstimmende Knoten zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="936ed-1339">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="936ed-1340">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="936ed-1340">Az.Compute</span></span>
* <span data-ttu-id="936ed-1341">Parameter „ProtectFromScaleIn“ und „ProtectFromScaleSetAction“ wurden zum Cmdlet „Update-AzVmssVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1341">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="936ed-1342">Der jetzt festgelegte wimple-Parameter „New-AzVM“ verwendet standardmäßig einen verfügbaren Standort, wenn „East US“ (USA, Osten) nicht unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="936ed-1342">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="936ed-1343">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="936ed-1343">Az.DataLakeStore</span></span>
* <span data-ttu-id="936ed-1344">Das ADLS-SDK wurde aktualisiert, um „HttpClient“ zu verwenden und Datenebenentests wurden mit dem Azure-Framework integriert</span><span class="sxs-lookup"><span data-stu-id="936ed-1344">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="936ed-1345">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="936ed-1345">Az.Monitor</span></span>
* <span data-ttu-id="936ed-1346">Fehlerbehebung bei falschen Parameternamen in Hilfebeispielen</span><span class="sxs-lookup"><span data-stu-id="936ed-1346">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="936ed-1347">Az.Network</span><span class="sxs-lookup"><span data-stu-id="936ed-1347">Az.Network</span></span>
* <span data-ttu-id="936ed-1348">DisableBgpRoutePropagation-Flag wurde zur Ausgabe der effektiven Routentabelle hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1348">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="936ed-1349">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="936ed-1349">Updated cmdlet:</span></span>
        - <span data-ttu-id="936ed-1350">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="936ed-1350">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="936ed-1351">Fehlerbehebung von doppeltem Bindestrich in Dokumentation von New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="936ed-1351">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="936ed-1352">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="936ed-1352">Az.Resources</span></span>
* <span data-ttu-id="936ed-1353">Neues Cmdlet „Get-AzureRmDenyAssignment“ zum Abrufen von Ablehnungszuweisungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1353">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="936ed-1354">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="936ed-1354">Az.Sql</span></span>
* <span data-ttu-id="936ed-1355">„Advanced Threat Protection“-Cmdlets in „Advanced Data Security“ umbenennen und Sicherheitsrisikobewertung standardmäßig aktivieren</span><span class="sxs-lookup"><span data-stu-id="936ed-1355">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="936ed-1356">2.0.0: Mai 2019</span><span class="sxs-lookup"><span data-stu-id="936ed-1356">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="936ed-1357">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="936ed-1357">Az.Accounts</span></span>
* <span data-ttu-id="936ed-1358">Authentifizierungsbibliothek aktualisiert, um ADFS-Probleme mit der Authentifizierung per Benutzername/Kennwort zu beheben</span><span class="sxs-lookup"><span data-stu-id="936ed-1358">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="936ed-1359">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="936ed-1359">Az.CognitiveServices</span></span>
* <span data-ttu-id="936ed-1360">Ausschließliche Anzeige des Bing-Haftungsausschlusses für Bing-Suchdienste</span><span class="sxs-lookup"><span data-stu-id="936ed-1360">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="936ed-1361">Fehler behoben, der zu einem Fehler bei der Kontoerstellung führte</span><span class="sxs-lookup"><span data-stu-id="936ed-1361">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="936ed-1362">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="936ed-1362">Az.Compute</span></span>
* <span data-ttu-id="936ed-1363">Feature für die Näherungsplatzierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="936ed-1363">Proximity placement group feature.</span></span>
    - <span data-ttu-id="936ed-1364">Die folgenden neuen Cmdlets wurden hinzugefügt:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="936ed-1364">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="936ed-1365">Der neue Parameter „ProximityPlacementGroupId“ wurde zu den folgenden Cmdlets hinzugefügt:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="936ed-1365">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="936ed-1366">Der Parameter „StorageAccountType“ wurde zu „New-AzGalleryImageVersion“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-1366">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="936ed-1367">„TargetRegion“ von „New-AzGalleryImageVersion“ kann „StorageAccountType“ enthalten.</span><span class="sxs-lookup"><span data-stu-id="936ed-1367">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="936ed-1368">Switch-Parameter „SkipShutdown“ wurde zu „Stop-AzVM“ und „Stop-AzVmss“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-1368">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="936ed-1369">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="936ed-1369">Breaking changes</span></span>
    - <span data-ttu-id="936ed-1370">„Set-AzVMBootDiagnostics“ in „Set-AzVMBootDiagnostic“ geändert</span><span class="sxs-lookup"><span data-stu-id="936ed-1370">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="936ed-1371">„Export-AzLogAnalyticThrottledRequests“ in „Export-AzLogAnalyticThrottledRequests“ geändert</span><span class="sxs-lookup"><span data-stu-id="936ed-1371">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="936ed-1372">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="936ed-1372">Az.DeploymentManager</span></span>
* <span data-ttu-id="936ed-1373">Erste allgemein verfügbare Version der Azure-Bereitstellungs-Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="936ed-1373">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="936ed-1374">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="936ed-1374">Az.Dns</span></span>
* <span data-ttu-id="936ed-1375">Automatische Delegierung des DNS-Namenservers</span><span class="sxs-lookup"><span data-stu-id="936ed-1375">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="936ed-1376">Das Cmdlet zum Erstellen einer DNS-Zone akzeptiert den übergeordneten Zonennamen als zusätzlichen optionalen Parameter.</span><span class="sxs-lookup"><span data-stu-id="936ed-1376">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="936ed-1377">NS-Einträge in der übergeordneten Zone für neu erstellte untergeordnete Zone hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1377">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="936ed-1378">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="936ed-1378">Az.FrontDoor</span></span>
* <span data-ttu-id="936ed-1379">Erste allgemein verfügbare Version der Azure Frontdoor-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="936ed-1379">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="936ed-1380">WAF-Cmdlets so umbenannt, dass sie „Waf“ enthalten</span><span class="sxs-lookup"><span data-stu-id="936ed-1380">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="936ed-1381">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="936ed-1381">Az.HDInsight</span></span>
* <span data-ttu-id="936ed-1382">Zwei Cmdlets entfernt:</span><span class="sxs-lookup"><span data-stu-id="936ed-1382">Removed two cmdlets:</span></span>
    - <span data-ttu-id="936ed-1383">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="936ed-1383">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="936ed-1384">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="936ed-1384">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="936ed-1385">Neues Cmdlet „Set-AzHDInsightGatewayCredential“ hinzugefügt, um „Grant-AzHDInsightHttpServicesAccess“ zu ersetzen</span><span class="sxs-lookup"><span data-stu-id="936ed-1385">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="936ed-1386">Cmdlet „Get-AzHDInsightJobOutput“ aktualisiert, um zwischen Leserrolle und HDInsight-Bedienerrolle zu unterscheiden:</span><span class="sxs-lookup"><span data-stu-id="936ed-1386">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="936ed-1387">Benutzer mit der Rolle „Leser“ müssen den Parameter „DefaultStorageAccountKey“ explizit angeben, andernfalls treten Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="936ed-1387">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="936ed-1388">Benutzer mit der Rolle des HDInsight-Bedieners sind nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="936ed-1388">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="936ed-1389">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="936ed-1389">Az.Monitor</span></span>
* <span data-ttu-id="936ed-1390">Neue Cmdlets für SQR-API (Scheduled Query Rule, geplante Abfrageregel)</span><span class="sxs-lookup"><span data-stu-id="936ed-1390">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="936ed-1391">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="936ed-1391">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="936ed-1392">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="936ed-1392">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="936ed-1393">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="936ed-1393">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="936ed-1394">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="936ed-1394">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="936ed-1395">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="936ed-1395">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="936ed-1396">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="936ed-1396">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="936ed-1397">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="936ed-1397">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="936ed-1398">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="936ed-1398">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="936ed-1399">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="936ed-1399">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="936ed-1400">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="936ed-1400">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="936ed-1401">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="936ed-1401">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="936ed-1402">[Weitere Informationen](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) zur SQR-API</span><span class="sxs-lookup"><span data-stu-id="936ed-1402">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="936ed-1403">„Az.Monitor.md“ aktualisiert, um Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch) einzuschließen</span><span class="sxs-lookup"><span data-stu-id="936ed-1403">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="936ed-1404">Az.Network</span><span class="sxs-lookup"><span data-stu-id="936ed-1404">Az.Network</span></span>
* <span data-ttu-id="936ed-1405">Unterstützung für NAT-Gatewayressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1405">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="936ed-1406">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="936ed-1406">New cmdlets</span></span>
        - <span data-ttu-id="936ed-1407">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="936ed-1407">New-AzNatGateway</span></span>
        - <span data-ttu-id="936ed-1408">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="936ed-1408">Get-AzNatGateway</span></span>
        - <span data-ttu-id="936ed-1409">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="936ed-1409">Set-AzNatGateway</span></span>
        - <span data-ttu-id="936ed-1410">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="936ed-1410">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="936ed-1411">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="936ed-1411">Updated cmdlets</span></span>
        - <span data-ttu-id="936ed-1412">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="936ed-1412">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="936ed-1413">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="936ed-1413">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="936ed-1414">Folgende Befehle für das Feature aktualisiert: Benutzerdefinierte Routen für Brooklyn-Gateway festgelegt/entfernt</span><span class="sxs-lookup"><span data-stu-id="936ed-1414">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="936ed-1415">„New-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="936ed-1415">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="936ed-1416">„Set-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="936ed-1416">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="936ed-1417">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="936ed-1417">Az.PolicyInsights</span></span>
* <span data-ttu-id="936ed-1418">Unterstützung für die Abfrage von Richtlinienauswertungsdetails</span><span class="sxs-lookup"><span data-stu-id="936ed-1418">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="936ed-1419">Parameter „-Expand“ zu „Get-AzPolicyState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1419">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="936ed-1420">Unterstützung für „-Expand PolicyEvaluationDetails“</span><span class="sxs-lookup"><span data-stu-id="936ed-1420">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="936ed-1421">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="936ed-1421">Az.RecoveryServices</span></span>
* <span data-ttu-id="936ed-1422">Unterstützung für abonnementübergreifende Azure-zu-Azure-Sitewiederherstellung</span><span class="sxs-lookup"><span data-stu-id="936ed-1422">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="936ed-1423">Markierung anstehender wichtiger Änderungen für Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="936ed-1423">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="936ed-1424">Fehlerbehebung für Azure Site Recovery-Wiederherstellungsplan und -Aktionsplan</span><span class="sxs-lookup"><span data-stu-id="936ed-1424">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="936ed-1425">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Netzwerkzuordnung für Azure zu Azure</span><span class="sxs-lookup"><span data-stu-id="936ed-1425">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="936ed-1426">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Schutzrichtung für Azure zu Azure für verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="936ed-1426">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="936ed-1427">Weitere kleinere Korrekturen</span><span class="sxs-lookup"><span data-stu-id="936ed-1427">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="936ed-1428">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="936ed-1428">Az.Relay</span></span>
* <span data-ttu-id="936ed-1429">Korrektur von Tippfehlern in Kundennachrichten</span><span class="sxs-lookup"><span data-stu-id="936ed-1429">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="936ed-1430">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="936ed-1430">Az.ServiceBus</span></span>
* <span data-ttu-id="936ed-1431">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1431">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="936ed-1432">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="936ed-1432">Az.Storage</span></span>
* <span data-ttu-id="936ed-1433">Upgrade auf Speicherclientbibliothek 10.0.1 (Namespace aller Objekte von diesem SDK von „Microsoft.WindowsAzure.Storage. *“ in „Microsoft.Azure.Storage.* “ geändert)</span><span class="sxs-lookup"><span data-stu-id="936ed-1433">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="936ed-1434">Upgrade auf Microsoft.Azure.Management.Storage 11.0.0, um die neue API-Version 2019-04-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="936ed-1434">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="936ed-1435">Art des Standardspeicherkontos bei der Speicherkontoerstellung von „Storage“ in „StorageV2“ geändert</span><span class="sxs-lookup"><span data-stu-id="936ed-1435">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="936ed-1436">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="936ed-1436">New-AzStorageAccount</span></span>
* <span data-ttu-id="936ed-1437">Vom Speicherkonto-Cmdlet ausgegebener SKU-Name (Sku.Name) durch Hinzufügen eines Unterstrichs an SKU-Eingabename angepasst (Beispiel: „StandardLRS“ > „Standard_LRS“).</span><span class="sxs-lookup"><span data-stu-id="936ed-1437">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="936ed-1438">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="936ed-1438">New-AzStorageAccount</span></span>
    - <span data-ttu-id="936ed-1439">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="936ed-1439">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="936ed-1440">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="936ed-1440">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="936ed-1441">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="936ed-1441">Az.Websites</span></span>
* <span data-ttu-id="936ed-1442">Die Eigenschaft „Kind“ wird nun für PSSite-Objekte festgelegt, die von „Get-AzWebApp“ zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="936ed-1442">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="936ed-1443">„Get-AzWebApp\*Metrics“ und „Get-AzAppServicePlanMetrics“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1443">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="936ed-1444">1.8.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="936ed-1444">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="936ed-1445">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="936ed-1445">Highlights since the last major release</span></span>
* <span data-ttu-id="936ed-1446">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="936ed-1446">General availability of `Az` module</span></span>
* <span data-ttu-id="936ed-1447">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="936ed-1447">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="936ed-1448">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="936ed-1448">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="936ed-1449">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1449">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="936ed-1450">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1450">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="936ed-1451">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1451">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="936ed-1452">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="936ed-1452">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="936ed-1453">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="936ed-1453">Az.Accounts</span></span>
* <span data-ttu-id="936ed-1454">„Uninstall-AzureRm“ aktualisiert, um Module unter Mac ordnungsgemäß zu löschen</span><span class="sxs-lookup"><span data-stu-id="936ed-1454">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="936ed-1455">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="936ed-1455">Az.Batch</span></span>
* <span data-ttu-id="936ed-1456">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="936ed-1456">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="936ed-1457">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="936ed-1457">Az.Cdn</span></span>
* <span data-ttu-id="936ed-1458">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="936ed-1458">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="936ed-1459">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="936ed-1459">Az.CognitiveServices</span></span>
* <span data-ttu-id="936ed-1460">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="936ed-1460">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="936ed-1461">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="936ed-1461">Az.Compute</span></span>
* <span data-ttu-id="936ed-1462">Problem mit der AEM-Installation behoben, wenn die Ressourcen-IDs von Datenträgern Ressourcengruppen in Kleinbuchstaben enthielten</span><span class="sxs-lookup"><span data-stu-id="936ed-1462">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="936ed-1463">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="936ed-1463">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="936ed-1464">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1464">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="936ed-1465">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="936ed-1465">Az.DataFactory</span></span>
* <span data-ttu-id="936ed-1466">„SsisProperties“ hinzugefügt, falls „NodeCount“ für verwaltete Integration Runtime nicht NULL ist</span><span class="sxs-lookup"><span data-stu-id="936ed-1466">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="936ed-1467">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="936ed-1467">Az.DataLakeStore</span></span>
* <span data-ttu-id="936ed-1468">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="936ed-1468">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="936ed-1469">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="936ed-1469">Az.EventGrid</span></span>
* <span data-ttu-id="936ed-1470">Hilfetext für Endpunkt aktualisiert, um anzugeben, dass Ressourcen erstellt werden müssen, bevor die Cmdlets zum Erstellen/Aktualisieren von Ereignisabonnements verwendet werden</span><span class="sxs-lookup"><span data-stu-id="936ed-1470">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="936ed-1471">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="936ed-1471">Az.EventHub</span></span>
* <span data-ttu-id="936ed-1472">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1472">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="936ed-1473">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="936ed-1473">Az.HDInsight</span></span>
* <span data-ttu-id="936ed-1474">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="936ed-1474">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="936ed-1475">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="936ed-1475">Az.IotHub</span></span>
* <span data-ttu-id="936ed-1476">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="936ed-1476">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="936ed-1477">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="936ed-1477">Az.KeyVault</span></span>
* <span data-ttu-id="936ed-1478">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="936ed-1478">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="936ed-1479">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1479">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="936ed-1480">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="936ed-1480">Az.MachineLearning</span></span>
* <span data-ttu-id="936ed-1481">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="936ed-1481">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="936ed-1482">Az.Media</span><span class="sxs-lookup"><span data-stu-id="936ed-1482">Az.Media</span></span>
* <span data-ttu-id="936ed-1483">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="936ed-1483">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="936ed-1484">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="936ed-1484">Az.Monitor</span></span>
  * <span data-ttu-id="936ed-1485">Neue Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch)</span><span class="sxs-lookup"><span data-stu-id="936ed-1485">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="936ed-1486">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="936ed-1486">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="936ed-1487">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="936ed-1487">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="936ed-1488">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="936ed-1488">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="936ed-1489">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="936ed-1489">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="936ed-1490">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="936ed-1490">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="936ed-1491">Monitor SDK auf Version 0.22.0-preview aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1491">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="936ed-1492">Az.Network</span><span class="sxs-lookup"><span data-stu-id="936ed-1492">Az.Network</span></span>
* <span data-ttu-id="936ed-1493">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="936ed-1493">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="936ed-1494">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1494">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="936ed-1495">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="936ed-1495">Az.NotificationHubs</span></span>
* <span data-ttu-id="936ed-1496">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="936ed-1496">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="936ed-1497">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="936ed-1497">Az.OperationalInsights</span></span>
* <span data-ttu-id="936ed-1498">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="936ed-1498">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="936ed-1499">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="936ed-1499">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="936ed-1500">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="936ed-1500">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="936ed-1501">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="936ed-1501">Az.RecoveryServices</span></span>
* <span data-ttu-id="936ed-1502">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="936ed-1502">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="936ed-1503">Tabellenformat für SQL auf Azure-VM aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1503">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="936ed-1504">Alternative Methode zum Abrufen des Speicherorts in „AzureFileShare“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1504">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="936ed-1505">„ScheduleRunDays“ in SchedulePolicy-Objekt gemäß Zeitzone aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1505">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="936ed-1506">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="936ed-1506">Az.RedisCache</span></span>
* <span data-ttu-id="936ed-1507">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="936ed-1507">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="936ed-1508">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="936ed-1508">Az.Resources</span></span>
* <span data-ttu-id="936ed-1509">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1509">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="936ed-1510">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="936ed-1510">Az.Sql</span></span>
* <span data-ttu-id="936ed-1511">Abhängigkeit vom Monitor SDK durch allgemeinen Code ersetzt</span><span class="sxs-lookup"><span data-stu-id="936ed-1511">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="936ed-1512">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="936ed-1512">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="936ed-1513">Verbesserter Prozess für Klassifizierung mehrerer Spalten</span><span class="sxs-lookup"><span data-stu-id="936ed-1513">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="936ed-1514">SKU-Eigenschaften (SKU-Name, Familie, Kapazität) in Antwort von „Get-AzSqlServerServiceObjective“ aufgenommen und standardmäßig als Tabelle formatiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1514">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="936ed-1515">Möglichkeit zum Ausführen von „Get-AzSqlServerServiceObjective“ nach Standort, ohne dass bereits ein Server in der Region vorhanden sein muss</span><span class="sxs-lookup"><span data-stu-id="936ed-1515">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="936ed-1516">Unterstützung für Zeitzonenparameter bei der Erstellung einer verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="936ed-1516">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="936ed-1517">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1517">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="936ed-1518">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="936ed-1518">Az.Websites</span></span>
* <span data-ttu-id="936ed-1519">„Set-AzWebApp“ und „Set-AzWebAppSlot“ korrigiert, sodass die Tags bei der Ausführung nicht entfernt werden</span><span class="sxs-lookup"><span data-stu-id="936ed-1519">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="936ed-1520">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="936ed-1520">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="936ed-1521">WebSites SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1521">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="936ed-1522">AdminSiteName-Eigenschaft aus „PSAppServicePlan“ entfernt</span><span class="sxs-lookup"><span data-stu-id="936ed-1522">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="936ed-1523">1.7.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="936ed-1523">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="936ed-1524">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="936ed-1524">Highlights since the last major release</span></span>
* <span data-ttu-id="936ed-1525">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="936ed-1525">General availability of `Az` module</span></span>
* <span data-ttu-id="936ed-1526">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="936ed-1526">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="936ed-1527">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="936ed-1527">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="936ed-1528">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1528">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="936ed-1529">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1529">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="936ed-1530">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1530">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="936ed-1531">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="936ed-1531">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="936ed-1532">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="936ed-1532">Az.Accounts</span></span>
* <span data-ttu-id="936ed-1533">„Add-AzEnvironment“ und „Set-AzEnvironment“ aktualisiert, um den Parameter „AzureAnalysisServicesEndpointResourceId“ zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="936ed-1533">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="936ed-1534">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="936ed-1534">Az.AnalysisServices</span></span>
* <span data-ttu-id="936ed-1535">ServiceClient wird in Cmdlets für die Datenebene verwendet, und die ursprüngliche Authentifizierungslogik wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="936ed-1535">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="936ed-1536">„Add-AzureASAccount“ wird als Wrapper von „Connect-AzAccount“ festgelegt, um einen Breaking Change zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="936ed-1536">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="936ed-1537">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="936ed-1537">Az.Automation</span></span>
* <span data-ttu-id="936ed-1538">Fehler des Cmdlets „Fixed New-AzAutomationSoftwareUpdateConfiguration“ für Einschlüsse behoben.</span><span class="sxs-lookup"><span data-stu-id="936ed-1538">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="936ed-1539">Die Parameter „IncludedKbNumber“ und „IncludedPackageNameMask“ sollten nun funktionieren.</span><span class="sxs-lookup"><span data-stu-id="936ed-1539">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="936ed-1540">Fehlerbehebung für eine dynamische Gruppe der Azure Automation-Updateverwaltung</span><span class="sxs-lookup"><span data-stu-id="936ed-1540">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="936ed-1541">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="936ed-1541">Az.Compute</span></span>
* <span data-ttu-id="936ed-1542">Parameter „HyperVGeneration“ zu „New-AzDiskConfig“ und „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1542">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="936ed-1543">Zulassen der VM-Erstellung mit einem Katalogimage aus anderen Mandanten</span><span class="sxs-lookup"><span data-stu-id="936ed-1543">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="936ed-1544">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="936ed-1544">Az.ContainerInstance</span></span>
* <span data-ttu-id="936ed-1545">Problem im Parameter „-Command“ von „New-AzContainerGroup“ behoben, das dazu führte, dass ein nachgestelltes leeres Argument hinzugefügt wurde</span><span class="sxs-lookup"><span data-stu-id="936ed-1545">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="936ed-1546">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="936ed-1546">Az.DataFactory</span></span>
* <span data-ttu-id="936ed-1547">Version des ADF .NET SDK auf 3.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1547">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="936ed-1548">Cmdlet „Set-AzDataFactoryV2“ mit zusätzlichen Parametern für RepoConfiguration-Einstellungen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1548">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="936ed-1549">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="936ed-1549">Az.Resources</span></span>
* <span data-ttu-id="936ed-1550">Verarbeitung von Anbietern für „Get-AzResource“ bei der Angabe der Parameter „-ResourceId“ oder „-ResourceGroupName“, „-Name“ und „-ResourceType“ verbessert</span><span class="sxs-lookup"><span data-stu-id="936ed-1550">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="936ed-1551">Fehlerbehandlung für „Test-AzDeployment“ und „Test-AzResourceGroupDeployment“ verbessert</span><span class="sxs-lookup"><span data-stu-id="936ed-1551">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="936ed-1552">Behandlung von außerhalb der Bereitstellungsüberprüfung aufgetretenen Fehlern und stattdessen Aufnahme in die Ausgabe des Befehls</span><span class="sxs-lookup"><span data-stu-id="936ed-1552">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="936ed-1553">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="936ed-1553">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="936ed-1554">Switch-Parameter „-IgnoreDynamicParameters“ zu Bereitstellungs-Cmdlets hinzugefügt, um Aufforderung in Skript- und Auftragsszenarien zu überspringen</span><span class="sxs-lookup"><span data-stu-id="936ed-1554">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="936ed-1555">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="936ed-1555">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="936ed-1556">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="936ed-1556">Az.Sql</span></span>
* <span data-ttu-id="936ed-1557">Unterstützung für Klassifizierung von Datenbankdaten</span><span class="sxs-lookup"><span data-stu-id="936ed-1557">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="936ed-1558">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="936ed-1558">Az.Storage</span></span>
* <span data-ttu-id="936ed-1559">Melden eines ausführlichen Fehlers beim Erstellen des Storage-Kontexts mit dem Parameter „-UseConnectedAccount“, aber ohne Azure-Anmeldekonto</span><span class="sxs-lookup"><span data-stu-id="936ed-1559">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="936ed-1560">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="936ed-1560">New-AzStorageContext</span></span>
* <span data-ttu-id="936ed-1561">Unterstützung für das Verwalten von Blobdiensteigenschaften eines bestimmten Storage-Kontos mit einer API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="936ed-1561">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="936ed-1562">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="936ed-1562">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="936ed-1563">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="936ed-1563">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="936ed-1564">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="936ed-1564">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="936ed-1565">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="936ed-1565">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="936ed-1566">Unterstützung von „-AsJob“ für Cmdlets für den Upload und Download von Blobs und Dateien</span><span class="sxs-lookup"><span data-stu-id="936ed-1566">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="936ed-1567">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="936ed-1567">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="936ed-1568">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="936ed-1568">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="936ed-1569">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="936ed-1569">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="936ed-1570">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="936ed-1570">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="936ed-1571">1.6.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="936ed-1571">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="936ed-1572">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="936ed-1572">Highlights since the last major release</span></span>
* <span data-ttu-id="936ed-1573">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="936ed-1573">General availability of `Az` module</span></span>
* <span data-ttu-id="936ed-1574">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="936ed-1574">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="936ed-1575">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="936ed-1575">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="936ed-1576">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1576">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="936ed-1577">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1577">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="936ed-1578">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1578">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="936ed-1579">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="936ed-1579">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="936ed-1580">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="936ed-1580">Az.Automation</span></span>
* <span data-ttu-id="936ed-1581">Änderung an der Azure Automation-Updateverwaltung, um die folgenden neuen Features zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="936ed-1581">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="936ed-1582">Dynamische Gruppierung</span><span class="sxs-lookup"><span data-stu-id="936ed-1582">Dynamic grouping</span></span>
    * <span data-ttu-id="936ed-1583">Pre-/Post-Skripts</span><span class="sxs-lookup"><span data-stu-id="936ed-1583">Pre-Post script</span></span>
    * <span data-ttu-id="936ed-1584">Neustarteinstellung</span><span class="sxs-lookup"><span data-stu-id="936ed-1584">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="936ed-1585">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="936ed-1585">Az.Compute</span></span>
* <span data-ttu-id="936ed-1586">Problem mit der Pfadauflösung in „Get-AzVmBootDiagnosticsData“ behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-1586">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="936ed-1587">Computeclientbibliothek auf 25.0.0. aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1587">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="936ed-1588">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="936ed-1588">Az.KeyVault</span></span>
* <span data-ttu-id="936ed-1589">Unterstützung für Platzhalterzeichen zu KeyVault-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1589">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="936ed-1590">Az.Network</span><span class="sxs-lookup"><span data-stu-id="936ed-1590">Az.Network</span></span>
* <span data-ttu-id="936ed-1591">Threat Intelligence-Unterstützung für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1591">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="936ed-1592">Ressource der obersten Ebene für Application Gateway-Firewallrichtlinie und benutzerdefinierte Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1592">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="936ed-1593">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="936ed-1593">Az.RecoveryServices</span></span>
* <span data-ttu-id="936ed-1594">SnapshotRetentionInDays in Azure-VM-Richtlinie hinzugefügt, um sofortigen Wiederherstellungspunkt zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="936ed-1594">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="936ed-1595">Pipe-Unterstützung für das Aufheben der Registrierung eines Containers hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1595">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="936ed-1596">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="936ed-1596">Az.Resources</span></span>
* <span data-ttu-id="936ed-1597">Unterstützung für Platzhalterzeichen für Get-AzResource und Get-AzResourceGroup aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1597">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="936ed-1598">Anmeldeinformationen aktualisiert, die beim Senden generischer Aufrufe an ARM verwendet werden</span><span class="sxs-lookup"><span data-stu-id="936ed-1598">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="936ed-1599">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="936ed-1599">Az.Sql</span></span>
* <span data-ttu-id="936ed-1600">Der Cmdlet-Parameter der Bedrohungserkennung (ExcludeDetectionType) wurde von „DetectionType“ in „string[]“ geändert, um ihn zukunftssicher zu machen, wenn neue DetectionTypes-Elemente hinzugefügt werden, und um AutoVervollständigen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="936ed-1600">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="936ed-1601">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="936ed-1601">Az.Storage</span></span>
* <span data-ttu-id="936ed-1602">Unterstützung von Get-/Set-/Remove-Verwaltungsrichtlinien für Speicherkonto hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1602">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="936ed-1603">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="936ed-1603">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="936ed-1604">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="936ed-1604">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="936ed-1605">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="936ed-1605">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="936ed-1606">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="936ed-1606">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="936ed-1607">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="936ed-1607">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="936ed-1608">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="936ed-1608">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="936ed-1609">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="936ed-1609">Az.Websites</span></span>
* <span data-ttu-id="936ed-1610">ARM-Vorlagenfehler behoben, der zu einem Problem beim Klonen aller Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ führte</span><span class="sxs-lookup"><span data-stu-id="936ed-1610">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="936ed-1611">1.5.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="936ed-1611">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="936ed-1612">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="936ed-1612">Az.Accounts</span></span>
* <span data-ttu-id="936ed-1613">Der Befehl „Register-AzModule“ wurde hinzugefügt, um von AutoRest generierte Cmdlets zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="936ed-1613">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="936ed-1614">Beispiele für „Connect-AzAccount“ wurden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="936ed-1614">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="936ed-1615">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="936ed-1615">Az.Automation</span></span>
* <span data-ttu-id="936ed-1616">Problem behoben, das beim Abrufen bestimmter monatlicher Zeitpläne in verschiedenen Azure Automation-Cmdlets auftrat</span><span class="sxs-lookup"><span data-stu-id="936ed-1616">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="936ed-1617">„Get-AzAutomationDscNode“ wurde korrigiert, da nur die 20 obersten Knoten zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="936ed-1617">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="936ed-1618">Jetzt werden alle Knoten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="936ed-1618">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="936ed-1619">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="936ed-1619">Az.Cdn</span></span>
* <span data-ttu-id="936ed-1620">Neue Powershell-Cmdlets zum Aktivieren/Deaktivieren von HTTPS für benutzerdefinierte Domänen hinzugefügt und alte Cmdlets außer Betrieb genommen</span><span class="sxs-lookup"><span data-stu-id="936ed-1620">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="936ed-1621">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="936ed-1621">Az.Compute</span></span>
* <span data-ttu-id="936ed-1622">Unterstützung für Platzhalterzeichen zu Get-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1622">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="936ed-1623">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="936ed-1623">Az.DataFactory</span></span>
* <span data-ttu-id="936ed-1624">Version des ADF .NET SDK auf 3.0.1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1624">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="936ed-1625">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="936ed-1625">Az.LogicApp</span></span>
* <span data-ttu-id="936ed-1626">„ListWorkflows“ wurde korrigiert, da nur die erste Seite mit Ergebnissen abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="936ed-1626">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="936ed-1627">Az.Network</span><span class="sxs-lookup"><span data-stu-id="936ed-1627">Az.Network</span></span>
* <span data-ttu-id="936ed-1628">Unterstützung für Platzhalterzeichen zu Network-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1628">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="936ed-1629">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="936ed-1629">Az.RecoveryServices</span></span>
* <span data-ttu-id="936ed-1630">SQL Server jetzt in Azure-VM-Support enthalten</span><span class="sxs-lookup"><span data-stu-id="936ed-1630">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="936ed-1631">SDK-Update</span><span class="sxs-lookup"><span data-stu-id="936ed-1631">SDK Update</span></span>
* <span data-ttu-id="936ed-1632">VMappContainer-Überprüfung in „Get-ProtectableItem“ entfernt</span><span class="sxs-lookup"><span data-stu-id="936ed-1632">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="936ed-1633">„Name“ und „ServerName“ als Parameter für „Get-ProtectableItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1633">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="936ed-1634">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="936ed-1634">Az.Resources</span></span>
* <span data-ttu-id="936ed-1635">Parameter `-TemplateObject` zu Bereitstellungs-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1635">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="936ed-1636">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="936ed-1636">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="936ed-1637">Problem beim Piping des Ergebnisses von `Get-AzResource` an `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-1637">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="936ed-1638">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="936ed-1638">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="936ed-1639">Problem mit JSON-Datentypänderung beim Ausführen von `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-1639">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="936ed-1640">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="936ed-1640">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="936ed-1641">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="936ed-1641">Az.Sql</span></span>
* <span data-ttu-id="936ed-1642">„AuditingEndpointsCommunicator“ wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="936ed-1642">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="936ed-1643">Das Verhalten eines Grenzfalls beim Erstellen neuer Diagnoseeinstellungen wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="936ed-1643">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="936ed-1644">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="936ed-1644">Az.Storage</span></span>
* <span data-ttu-id="936ed-1645">Unterstützung von „Kind BlockBlobStorage“ beim Erstellen eines Speicherkontos: New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="936ed-1645">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="936ed-1646">1.4.0 – Februar 2019</span><span class="sxs-lookup"><span data-stu-id="936ed-1646">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="936ed-1647">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="936ed-1647">Az.AnalysisServices</span></span>
* <span data-ttu-id="936ed-1648">Cmdlet „AddAzureASAccount“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1648">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="936ed-1649">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="936ed-1649">Az.Automation</span></span>
* <span data-ttu-id="936ed-1650">Hilfe für „Import-AzAutomationDscNodeConfiguration“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1650">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="936ed-1651">Überprüfung des Konfigurationsnamens zu Cmdlet „Import-AzAutomationDscConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1651">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="936ed-1652">Fehlerbehandlung für Cmdlet „Import-AzAutomationDscConfiguration“ verbessert</span><span class="sxs-lookup"><span data-stu-id="936ed-1652">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="936ed-1653">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="936ed-1653">Az.CognitiveServices</span></span>
* <span data-ttu-id="936ed-1654">„CustomSubdomainName“ als neuer optionaler Parameter für Cmdlet „New-AzCognitiveServicesAccount“ hinzugefügt, das zum Angeben der Unterdomäne für die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="936ed-1654">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="936ed-1655">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="936ed-1655">Az.Compute</span></span>
* <span data-ttu-id="936ed-1656">Problem mit ID-Parametersätzen behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-1656">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="936ed-1657">„Get-AzVMExtension“ aktualisiert, sodass alle installierten Erweiterungen aufgelistet werden, wenn der Name-Parameter nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="936ed-1657">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="936ed-1658">Parameter „Tag“ und „ResourceId“ zum Cmdlet „Update-AzImage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1658">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="936ed-1659">„Get-AzVmssVM“ ohne Instanz-ID und mit „InstanceView“ können virtuelle VMSS-Computer mit Instanzansicht auflisten.</span><span class="sxs-lookup"><span data-stu-id="936ed-1659">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="936ed-1660">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="936ed-1660">Az.DataLakeStore</span></span>
* <span data-ttu-id="936ed-1661">Cmdlets zum Auflisten und Wiederherstellen gelöschter ADL-Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1661">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="936ed-1662">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="936ed-1662">Az.EventHub</span></span>
* <span data-ttu-id="936ed-1663">Neue boolesche Eigenschaft „SkipEmptyArchives“ zum Überspringen leerer Archive in Klasse „CaptureDescription“ von EventHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1663">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="936ed-1664">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="936ed-1664">Az.KeyVault</span></span>
* <span data-ttu-id="936ed-1665">Kennzeichnung in „Set-AzKeyVaultSecret“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1665">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="936ed-1666">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="936ed-1666">Az.LogicApp</span></span>
* <span data-ttu-id="936ed-1667">SKU „Basic“ für Integrationskonten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1667">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="936ed-1668">XSLT 2.0, XSLT 3.0 und Liquid-Zuordnungstypen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1668">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="936ed-1669">Neue Cmdlets für Integrationskonto-Assemblys</span><span class="sxs-lookup"><span data-stu-id="936ed-1669">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="936ed-1670">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="936ed-1670">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="936ed-1671">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="936ed-1671">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="936ed-1672">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="936ed-1672">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="936ed-1673">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="936ed-1673">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="936ed-1674">Neue Cmdlets für Integrationskonto-Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="936ed-1674">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="936ed-1675">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="936ed-1675">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="936ed-1676">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="936ed-1676">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="936ed-1677">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="936ed-1677">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="936ed-1678">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="936ed-1678">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="936ed-1679">Logik-App-SDK auf Version 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1679">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="936ed-1680">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="936ed-1680">Az.Monitor</span></span>
* <span data-ttu-id="936ed-1681">Hilfe für „Get-AzMetric“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1681">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="936ed-1682">Az.Network</span><span class="sxs-lookup"><span data-stu-id="936ed-1682">Az.Network</span></span>
* <span data-ttu-id="936ed-1683">Hilfebeispiel für „Add-AzApplicationGatewayCustomError“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1683">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="936ed-1684">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="936ed-1684">Az.OperationalInsights</span></span>
* <span data-ttu-id="936ed-1685">Zusätzliche Unterstützung für Datenquelle von „New-ApplicationInsights“ und „Get-ApplicationInsights“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-1685">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="936ed-1686">Neue Art von „ApplicationInsights“ zum Abrufen von bestimmten und von allen ApplicationInsights-Datenquellen für einen Workspace hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-1686">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="936ed-1687">Cmdlet „New-AzOperationalInsightsApplicationInsightsDataSource“ zum Erstellen einer Datenquelle anhand des angegebenen Ressourcenparameters für „Application-Insights“ hinzugefügt: „subscriptionId“, „resourceGroupName“ und „name“.</span><span class="sxs-lookup"><span data-stu-id="936ed-1687">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="936ed-1688">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="936ed-1688">Az.Resources</span></span>
* <span data-ttu-id="936ed-1689">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="936ed-1689">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="936ed-1690">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="936ed-1690">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="936ed-1691">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="936ed-1691">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="936ed-1692">Fehler korrigiert, der die wiederholte Erstellung von „KeyCredentials“ verhindert</span><span class="sxs-lookup"><span data-stu-id="936ed-1692">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="936ed-1693">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="936ed-1693">Az.Sql</span></span>
* <span data-ttu-id="936ed-1694">Unterstützung für SQL DB Hyperscale-Tarif hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1694">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="936ed-1695">Fehler korrigiert, aufgrund dessen die Wiederherstellung wegen der Festlegung unnötiger Eigenschaften in der Wiederherstellungsanforderung fehlschlagen konnte</span><span class="sxs-lookup"><span data-stu-id="936ed-1695">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="936ed-1696">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="936ed-1696">Az.Websites</span></span>
* <span data-ttu-id="936ed-1697">Beispiel in „Get-AzWebAppSlotMetrics“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1697">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="936ed-1698">1.3.0: Februar 2019</span><span class="sxs-lookup"><span data-stu-id="936ed-1698">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="936ed-1699">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="936ed-1699">Az.Accounts</span></span>
* <span data-ttu-id="936ed-1700">Update auf die aktuelle Version von ClientRuntime durchgeführt</span><span class="sxs-lookup"><span data-stu-id="936ed-1700">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="936ed-1701">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="936ed-1701">Az.AnalysisServices</span></span>
<span data-ttu-id="936ed-1702">Allgemeine Verfügbarkeit für Az.AnalysisServices-Modul</span><span class="sxs-lookup"><span data-stu-id="936ed-1702">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="936ed-1703">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="936ed-1703">Az.Compute</span></span>
* <span data-ttu-id="936ed-1704">AEM-Erweiterung: Unterstützung für UltraSSD und P60-, P70- und P80-Datenträger hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1704">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="936ed-1705">Hilfebeschreibung für „Set-AzVMBootDiagnostics“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1705">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="936ed-1706">Hilfebeschreibung und Beispiel für „Update-AzImage“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1706">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="936ed-1707">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="936ed-1707">Az.RecoveryServices</span></span>
<span data-ttu-id="936ed-1708">Allgemeine Verfügbarkeit für Az.RecoveryServices-Modul.</span><span class="sxs-lookup"><span data-stu-id="936ed-1708">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="936ed-1709">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="936ed-1709">Az.Resources</span></span>
* <span data-ttu-id="936ed-1710">Kennzeichnung für Ressourcengruppen korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1710">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="936ed-1711">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="936ed-1711">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="936ed-1712">Problem behoben, bei dem „-ErrorAction“ von `Get-AzureRmRoleAssignment` nicht berücksichtigt wird</span><span class="sxs-lookup"><span data-stu-id="936ed-1712">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="936ed-1713">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="936ed-1713">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="936ed-1714">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="936ed-1714">Az.Sql</span></span>
* <span data-ttu-id="936ed-1715">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1715">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="936ed-1716">Problem behoben, bei dem eine fehlende Anmeldung am Azure-Konto bei der Ausführung von SQL-Cmdlets zu einer nullref-Ausnahme führt</span><span class="sxs-lookup"><span data-stu-id="936ed-1716">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="936ed-1717">nullref-Ausnahme in Get-AzSqlCapability korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1717">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="936ed-1718">1.2.1: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="936ed-1718">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="936ed-1719">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="936ed-1719">Az.Accounts</span></span>
* <span data-ttu-id="936ed-1720">Release mit richtiger Version der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="936ed-1720">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="936ed-1721">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="936ed-1721">Az.AnalysisServices</span></span>
* <span data-ttu-id="936ed-1722">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="936ed-1722">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="936ed-1723">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="936ed-1723">Az.RecoveryServices</span></span>
* <span data-ttu-id="936ed-1724">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="936ed-1724">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="936ed-1725">1.2.0: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="936ed-1725">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="936ed-1726">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="936ed-1726">Az.Accounts</span></span>
* <span data-ttu-id="936ed-1727">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1727">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="936ed-1728">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1728">Update incorrect online help URLs</span></span>
* <span data-ttu-id="936ed-1729">Warnmeldung in PS Core für „Uninstall-AzureRm“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1729">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="936ed-1730">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="936ed-1730">Az.Aks</span></span>
* <span data-ttu-id="936ed-1731">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1731">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="936ed-1732">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="936ed-1732">Az.Automation</span></span>
* <span data-ttu-id="936ed-1733">Unterstützung für Python 2-Runbooks hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1733">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="936ed-1734">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1734">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="936ed-1735">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="936ed-1735">Az.Cdn</span></span>
* <span data-ttu-id="936ed-1736">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1736">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="936ed-1737">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="936ed-1737">Az.Compute</span></span>
* <span data-ttu-id="936ed-1738">Cmdlet „Invoke-AzVMReimage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1738">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="936ed-1739">Parameter „TempDisk“ zu „Set-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1739">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="936ed-1740">Warnmeldung von „New-AzVM“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1740">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="936ed-1741">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="936ed-1741">Az.ContainerRegistry</span></span>
* <span data-ttu-id="936ed-1742">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1742">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="936ed-1743">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="936ed-1743">Az.DataFactory</span></span>
* <span data-ttu-id="936ed-1744">Version des ADF .NET SDK auf 3.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1744">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="936ed-1745">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="936ed-1745">Az.DataLakeStore</span></span>
* <span data-ttu-id="936ed-1746">Problem mit ADLS-Endpunkt bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-1746">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="936ed-1747">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="936ed-1747">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="936ed-1748">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1748">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="936ed-1749">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="936ed-1749">Az.IotHub</span></span>
* <span data-ttu-id="936ed-1750">Codierungsformat zu Cmdlet „Add-IotHubRoutingEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1750">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="936ed-1751">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="936ed-1751">Az.KeyVault</span></span>
* <span data-ttu-id="936ed-1752">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1752">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="936ed-1753">Az.Network</span><span class="sxs-lookup"><span data-stu-id="936ed-1753">Az.Network</span></span>
* <span data-ttu-id="936ed-1754">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1754">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="936ed-1755">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="936ed-1755">Az.Resources</span></span>
* <span data-ttu-id="936ed-1756">Fehlerhafte Beispiele in Referenzdokumentation zu „New-AzADAppCredential“ und „New-AzADSpCredential“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1756">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="936ed-1757">Problem behoben, bei dem der Pfad für den Parameter „-TemplateFile“ nicht aufgelöst wurde, bevor Cmdlets für die Bereitstellung von Ressourcengruppen ausgeführt wurden</span><span class="sxs-lookup"><span data-stu-id="936ed-1757">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="936ed-1758">Az.Resources: Richtige Dokumentation für Standardwert von „New-AzureRmPolicyDefinition -Mode“ bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="936ed-1758">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="936ed-1759">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="936ed-1759">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="936ed-1760">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="936ed-1760">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="936ed-1761">Formatierungsproblem für Objekt „PSResourceGroupDeployment“ behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-1761">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="936ed-1762">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="936ed-1762">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="936ed-1763">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="936ed-1763">Az.ServiceFabric</span></span>
* <span data-ttu-id="936ed-1764">Rollback beim Hinzufügen eines Zertifikats zum VMSS-Modell, Auslösung einer Ausnahme. Fehlerbehebung: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="936ed-1764">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="936ed-1765">Einige Fehlermeldungen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="936ed-1765">Fix some error messages.</span></span>
* <span data-ttu-id="936ed-1766">Fehler bei Clustererstellung mit ARM-Standardvorlage für „New-AzServiceFabriCluster“ behoben, bei dem die Migration zu Az nicht funktioniert hat.</span><span class="sxs-lookup"><span data-stu-id="936ed-1766">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="936ed-1767">Fehler behoben beim Hinzufügen eines Cluster-/Anwendungszertifikats ausschließlich zu VM Scale Sets, die zum Cluster gehören, indem die Cluster-ID in der Erweiterung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="936ed-1767">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="936ed-1768">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="936ed-1768">Az.SignalR</span></span>
* <span data-ttu-id="936ed-1769">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1769">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="936ed-1770">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="936ed-1770">Az.Sql</span></span>
* <span data-ttu-id="936ed-1771">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1771">Update incorrect online help URLs</span></span>
* <span data-ttu-id="936ed-1772">Parameterbeschreibung für den Parameter „LicenseType“ mit möglichen Werten aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1772">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="936ed-1773">Fehler behoben, bei dem die Aktualisierung der Identität der verwalteten Instanz nicht funktioniert hat, wenn es sich um die einzige aktualisierte Eigenschaft gehandelt hat</span><span class="sxs-lookup"><span data-stu-id="936ed-1773">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="936ed-1774">Unterstützung für die benutzerdefinierte Sortierung auf verwalteter Instanz</span><span class="sxs-lookup"><span data-stu-id="936ed-1774">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="936ed-1775">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="936ed-1775">Az.Storage</span></span>
* <span data-ttu-id="936ed-1776">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1776">Update incorrect online help URLs</span></span>
* <span data-ttu-id="936ed-1777">Ausführliche Fehlermeldung beim Abrufen/Festlegen der klassischen Protokollierung bzw. Metriken für Storage Premium-Konto, da für das Storage Premium-Konto die klassische Protokollierung bzw. Metriken nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="936ed-1777">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="936ed-1778">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="936ed-1778">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="936ed-1779">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="936ed-1779">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="936ed-1780">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="936ed-1780">Az.TrafficManager</span></span>
* <span data-ttu-id="936ed-1781">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1781">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="936ed-1782">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="936ed-1782">Az.Websites</span></span>
* <span data-ttu-id="936ed-1783">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1783">Update incorrect online help URLs</span></span>
* <span data-ttu-id="936ed-1784">„New-AzWebAppSSLBinding“ korrigiert, damit das Zertifikat in die richtige Ressourcengruppe bzw. an den richtigen Speicherort hochgeladen wird, wenn die App in einer ASE gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="936ed-1784">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="936ed-1785">„New-AzWebAppSSLBinding“ korrigiert, damit die Tags beim Binden eines SSL-Zertifikats an eine App nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="936ed-1785">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="936ed-1786">1.1.0 – Januar 2019</span><span class="sxs-lookup"><span data-stu-id="936ed-1786">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="936ed-1787">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="936ed-1787">Az.Accounts</span></span>
* <span data-ttu-id="936ed-1788">Bereich „Local“ zu „Enable-AzureRmAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1788">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="936ed-1789">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="936ed-1789">Az.Compute</span></span>
* <span data-ttu-id="936ed-1790">Name ist jetzt optional im ID-Parametersatz für „Restart/Start/Stop/Remove/Set-AzVM“ und „Save-AzVMImage“</span><span class="sxs-lookup"><span data-stu-id="936ed-1790">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="936ed-1791">Beschreibung der ID in Hilfedateien aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1791">Updated the description of ID in help files</span></span>
* <span data-ttu-id="936ed-1792">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-1792">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="936ed-1793">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="936ed-1793">Az.DataLakeStore</span></span>
* <span data-ttu-id="936ed-1794">Aktualisierung der SDK-Version der Datenebene auf 1.1.14 für SDK-Fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="936ed-1794">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="936ed-1795">Behandlung von negativen acesstime- and modificationtime-Werten für „getfilestatus“ und „liststatus“ korrigiert, asynchrones Abbruchtoken korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1795">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="936ed-1796">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="936ed-1796">Az.EventGrid</span></span>
* <span data-ttu-id="936ed-1797">Zur Verwendung der API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1797">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="936ed-1798">Aktualisierung der folgenden Cmdlets zur Unterstützung des neuen Szenarios in der API-Version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="936ed-1798">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="936ed-1799">New-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="936ed-1799">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="936ed-1800">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="936ed-1800">Event Time-To-Live,</span></span>
        - <span data-ttu-id="936ed-1801">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="936ed-1801">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="936ed-1802">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="936ed-1802">Dead letter endpoint.</span></span>
    - <span data-ttu-id="936ed-1803">Update-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="936ed-1803">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="936ed-1804">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="936ed-1804">Event Time-To-Live,</span></span>
        - <span data-ttu-id="936ed-1805">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="936ed-1805">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="936ed-1806">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="936ed-1806">Dead letter endpoint.</span></span>
* <span data-ttu-id="936ed-1807">Neue Enumerationswerte („storageQueue“ und „hybridConnection“) für die EndpointType-Option in den Cmdlets „New-AzureRmEventGridSubscription“ und „Update-AzureRmEventGridSubscription“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1807">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="936ed-1808">Anzeige einer Warnmeldung, wenn das Erstellen oder Aktualisieren des Ereignisabonnements voraussichtlich eine manuelle Aktion des Benutzers zur Folge hat</span><span class="sxs-lookup"><span data-stu-id="936ed-1808">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="936ed-1809">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="936ed-1809">Az.IotHub</span></span>
* <span data-ttu-id="936ed-1810">Auf die aktuelle Version des Iot Hub SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1810">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="936ed-1811">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="936ed-1811">Az.LogicApp</span></span>
* <span data-ttu-id="936ed-1812">„Get-AzLogicApp“ listet alle Apps ohne angegebenen Namen auf</span><span class="sxs-lookup"><span data-stu-id="936ed-1812">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="936ed-1813">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="936ed-1813">Az.Resources</span></span>
* <span data-ttu-id="936ed-1814">Problem mit dem Parametersatz bei Angabe der Parameter „-ODataQuery“ und „-ResourceId“ für „Get-AzResource“ behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-1814">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="936ed-1815">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="936ed-1815">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="936ed-1816">Behandlung des Parameters „-Custom“ in „New/Set-AzPolicyDefinition“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1816">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="936ed-1817">Tippfehler in der Dokumentation für „New-AzDeployment“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1817">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="936ed-1818">Parameter „-MailNickname“ als obligatorisch festgelegt für „New-AzADUser“</span><span class="sxs-lookup"><span data-stu-id="936ed-1818">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="936ed-1819">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="936ed-1819">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="936ed-1820">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="936ed-1820">Az.SignalR</span></span>
* <span data-ttu-id="936ed-1821">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-1821">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="936ed-1822">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="936ed-1822">Az.Sql</span></span>
* <span data-ttu-id="936ed-1823">Abhängigkeit des Speicherverwaltungsclients zur allgemeinen SDK-Implementierung konvertiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1823">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="936ed-1824">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="936ed-1824">Az.Storage</span></span>
* <span data-ttu-id="936ed-1825">Festlegung des „StorageAccountName“ des Speicherkontexts als tatsächlichen Namen des Speicherkontos, wenn dieser mit „SAS-Token“, „OAuth“ oder „Anonym“ erstellt wird</span><span class="sxs-lookup"><span data-stu-id="936ed-1825">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="936ed-1826">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="936ed-1826">New-AzStorageContext</span></span>
* <span data-ttu-id="936ed-1827">Erstellen von SAS-Token des Blob-Momentaufnahmeobjekts mit dem Parameter „-FullUri“, Festlegung des zurückgegebenen URI als Momentaufnahme-URI</span><span class="sxs-lookup"><span data-stu-id="936ed-1827">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="936ed-1828">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="936ed-1828">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="936ed-1829">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="936ed-1829">Az.Websites</span></span>
* <span data-ttu-id="936ed-1830">Fehler bei der Datumsanalyse in „Get-AzDeletedWebApp“ behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-1830">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="936ed-1831">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-1831">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="936ed-1832">1.0.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="936ed-1832">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="936ed-1833">Allgemein</span><span class="sxs-lookup"><span data-stu-id="936ed-1833">General</span></span>

- <span data-ttu-id="936ed-1834">Allgemeine Verfügbarkeit des Az-Moduls</span><span class="sxs-lookup"><span data-stu-id="936ed-1834">General Availability of Az Module</span></span>
- <span data-ttu-id="936ed-1835">Onlinehilfe für jedes Modul</span><span class="sxs-lookup"><span data-stu-id="936ed-1835">Online help for each module</span></span>
- <span data-ttu-id="936ed-1836">Ausführlichere Informationen und eine Roadmap finden Sie auf der [Seite mit der Ankündigung zu Az](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="936ed-1836">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="936ed-1837">Informationen zur Migration aus AzureRM finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="936ed-1837">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="936ed-1838">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="936ed-1838">Az.Accounts</span></span>
- <span data-ttu-id="936ed-1839">Geändert von Az.Profile</span><span class="sxs-lookup"><span data-stu-id="936ed-1839">Changed from Az.Profile</span></span>
- <span data-ttu-id="936ed-1840">Feste Tabellenformate für Profil- und Kontexttypen</span><span class="sxs-lookup"><span data-stu-id="936ed-1840">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="936ed-1841">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="936ed-1841">Az.ApiManagement</span></span>
- <span data-ttu-id="936ed-1842">Korrekturen für #7002</span><span class="sxs-lookup"><span data-stu-id="936ed-1842">Fixes for #7002</span></span>
- <span data-ttu-id="936ed-1843">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="936ed-1843">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="936ed-1844">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="936ed-1844">Az.Batch</span></span>
- <span data-ttu-id="936ed-1845">Möglichkeit zum Anzeigen der ausgeführten Version des Azure Batch-Knoten-Agents auf den VMs eines Pools mit der neuen `NodeAgentInformation`-Eigenschaft für `PSComputeNode` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-1845">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="936ed-1846">Der `Caching`-Standardwert für `PSDataDisk` lautet jetzt nicht mehr `None`, sondern `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="936ed-1846">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="936ed-1847">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="936ed-1847">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="936ed-1848">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="936ed-1848">Az.Billing</span></span>
- <span data-ttu-id="936ed-1849">Kombination von Billing-, Consumption- und UsageAggregates-Cmdlets. Ausführliche Informationen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="936ed-1849">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="936ed-1850">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="936ed-1850">Az.CognitivServices</span></span>
- <span data-ttu-id="936ed-1851">Vervollständigungen für SkuName und Typem für den Vorgang New-AzureRmCognitiveServicesAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1851">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="936ed-1852">GetSkusWithAccountParamSetName-Parametersatz aus Get-AzCognitiveServicesAccountSkus entfernt</span><span class="sxs-lookup"><span data-stu-id="936ed-1852">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="936ed-1853">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="936ed-1853">Az.ContainerInstance</span></span>
- <span data-ttu-id="936ed-1854">ManagedIdentity-Unterstützung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1854">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="936ed-1855">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="936ed-1855">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="936ed-1856">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="936ed-1856">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="936ed-1857">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="936ed-1857">Az.DataLakeStore</span></span>
- <span data-ttu-id="936ed-1858">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="936ed-1858">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="936ed-1859">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="936ed-1859">Az.Monitor</span></span>
- <span data-ttu-id="936ed-1860">Az.Insights in Az.Monitor umbenannt und weitere weniger wichtige grundlegende Änderungen durchgeführt. Informationen hierzu finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="936ed-1860">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="936ed-1861">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="936ed-1861">Az.KeyVault</span></span>
- <span data-ttu-id="936ed-1862">Veraltete PurgeDisabled-Eigenschaft aus Ausgabetypen entfernt</span><span class="sxs-lookup"><span data-stu-id="936ed-1862">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="936ed-1863">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="936ed-1863">Az.MachineLearning</span></span>
- <span data-ttu-id="936ed-1864">Cmdlets des Az.MachineLearningCompute-Moduls eingebunden</span><span class="sxs-lookup"><span data-stu-id="936ed-1864">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="936ed-1865">Az.Media</span><span class="sxs-lookup"><span data-stu-id="936ed-1865">Az.Media</span></span>
- <span data-ttu-id="936ed-1866">Veralteten -Tags-Alias aus New-AzMediaService entfernt</span><span class="sxs-lookup"><span data-stu-id="936ed-1866">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="936ed-1867">Az.Network</span><span class="sxs-lookup"><span data-stu-id="936ed-1867">Az.Network</span></span>
<span data-ttu-id="936ed-1868">Unterstützung für das Konfigurieren von RewriteRuleSets im Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1868">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="936ed-1869">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="936ed-1869">New cmdlets added:</span></span>
        - <span data-ttu-id="936ed-1870">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="936ed-1870">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="936ed-1871">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="936ed-1871">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="936ed-1872">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="936ed-1872">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="936ed-1873">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="936ed-1873">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="936ed-1874">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="936ed-1874">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="936ed-1875">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="936ed-1875">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="936ed-1876">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="936ed-1876">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="936ed-1877">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="936ed-1877">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="936ed-1878">Cmdlets mit optionalem Parameter -RewriteRuleSet aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1878">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="936ed-1879">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="936ed-1879">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="936ed-1880">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="936ed-1880">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="936ed-1881">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="936ed-1881">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="936ed-1882">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="936ed-1882">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="936ed-1883">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="936ed-1883">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="936ed-1884">New-AzureRmApplicationGatewayUrlPathMapConfig: KeyVault-Unterstützung mithilfe von Identität zum Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-1884">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="936ed-1885">Cmdlets mit optionalem Parameter aktualisiert: -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="936ed-1885">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="936ed-1886">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="936ed-1886">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="936ed-1887">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="936ed-1887">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="936ed-1888">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="936ed-1888">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="936ed-1889">Cmdlet New-AzApplicationGateway mit optionalem Parameter -UserAssignedIdentity aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1889">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="936ed-1890">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="936ed-1890">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="936ed-1891">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="936ed-1891">Az.OperationalInsights</span></span>
- <span data-ttu-id="936ed-1892">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="936ed-1892">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="936ed-1893">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="936ed-1893">Az.Profile</span></span>
- <span data-ttu-id="936ed-1894">Modulnamen in Az.Accounts geändert</span><span class="sxs-lookup"><span data-stu-id="936ed-1894">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="936ed-1895">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="936ed-1895">Az.RecoveryServices</span></span>
- <span data-ttu-id="936ed-1896">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="936ed-1896">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="936ed-1897">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="936ed-1897">Az.Resources</span></span>
- <span data-ttu-id="936ed-1898">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="936ed-1898">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="936ed-1899">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="936ed-1899">Az.ServiceFabric</span></span>
- <span data-ttu-id="936ed-1900">Unterstützung für das Angeben des Zertifikats anhand des allgemeinen Namens und Fingerabdrucks</span><span class="sxs-lookup"><span data-stu-id="936ed-1900">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="936ed-1901">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="936ed-1901">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="936ed-1902">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="936ed-1902">Az.SIgnalR</span></span>
- <span data-ttu-id="936ed-1903">Allgemeine Verfügbarkeit für PowerShell-Cmdlets für SIgnalR</span><span class="sxs-lookup"><span data-stu-id="936ed-1903">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="936ed-1904">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="936ed-1904">Az.Sql</span></span>
- <span data-ttu-id="936ed-1905">Neue Erkennungstypen Data_Exfiltration und Unsafe_Action zu Cmdlets für Bedrohungserkennung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1905">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="936ed-1906">Dokumentationsbeispiele für Cmdlets für SQL-Überwachung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1906">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="936ed-1907">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="936ed-1907">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="936ed-1908">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="936ed-1908">Az.Storage</span></span>
- <span data-ttu-id="936ed-1909">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="936ed-1909">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="936ed-1910">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="936ed-1910">Az.Websites</span></span>
- <span data-ttu-id="936ed-1911">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="936ed-1911">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="936ed-1912">0.7.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="936ed-1912">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="936ed-1913">Allgemein</span><span class="sxs-lookup"><span data-stu-id="936ed-1913">General</span></span>

* <span data-ttu-id="936ed-1914">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="936ed-1914">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="936ed-1915">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="936ed-1915">Az.Compute</span></span>

* <span data-ttu-id="936ed-1916">Unterstützung für UltraSSD und Katalogimages in einfachen Parametersätzen für `New-AzVm(ss)`-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-1916">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="936ed-1917">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="936ed-1917">Az.DataLakeStore</span></span>

* <span data-ttu-id="936ed-1918">Nachgestellten Schrägstrich für die Domäne des ADLS-Kontos korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1918">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="936ed-1919">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="936ed-1919">Az.FrontDoor</span></span>

* <span data-ttu-id="936ed-1920">Einige fehlerhafte Links behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-1920">Fixed some broken links</span></span>
    - <span data-ttu-id="936ed-1921">In den Artikeln zu New-AzureRmFrontDoor und Set-AzureRmFrontDoor den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorHealthProbeSettingObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="936ed-1921">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="936ed-1922">Im Artikel zu New-AzureRmFrontDoorManagedRuleObject den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorRuleGroupOverrideObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="936ed-1922">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="936ed-1923">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="936ed-1923">Az.RecoveryServices</span></span>

* <span data-ttu-id="936ed-1924">Clientseitige Validierungen für Wiederherstellungsvorgänge von Azure-Dateifreigaben hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-1924">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="936ed-1925">storageAccountName und storageAccountResourceGroupName für AFS-Wiederherstellung optional gemacht.</span><span class="sxs-lookup"><span data-stu-id="936ed-1925">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="936ed-1926">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="936ed-1926">Az.Resources</span></span>

* <span data-ttu-id="936ed-1927">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="936ed-1927">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="936ed-1928">Get-AzureRmRoleAssignment für die Verwendung des Abonnementbereichs aktualisiert, wenn dieser beim Anfordern von klassischen Administratoren angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="936ed-1928">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="936ed-1929">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="936ed-1929">Az.Sql</span></span>

* <span data-ttu-id="936ed-1930">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="936ed-1930">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="936ed-1931">Problem mit der Verwendung von Get-AzureRmSqlDatabaseVulnerabilityAssessment mit .NET Core behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-1931">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="936ed-1932">Dokumentation mit Hilfemeldungen zu Cmdlets für die SQL-Überwachung geändert.</span><span class="sxs-lookup"><span data-stu-id="936ed-1932">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="936ed-1933">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="936ed-1933">Az.Storage</span></span>

* <span data-ttu-id="936ed-1934">-EnableHierarchicalNamespace zu New-AzureRmStorageAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1934">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="936ed-1935">Problem behoben, bei dem für das Copy File-Cmdlet am Ziel kein Quellkontext wiederverwendet werden kann, wenn -DestContext nicht eingegeben wird</span><span class="sxs-lookup"><span data-stu-id="936ed-1935">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="936ed-1936">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="936ed-1936">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="936ed-1937">Unterstützung der Konfiguration von statischen Websites</span><span class="sxs-lookup"><span data-stu-id="936ed-1937">Support Static Website configuration</span></span>
    - <span data-ttu-id="936ed-1938">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="936ed-1938">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="936ed-1939">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="936ed-1939">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="936ed-1940">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="936ed-1940">Az.Websites</span></span>

* <span data-ttu-id="936ed-1941">Set-AzureRmWebApp und Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="936ed-1941">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="936ed-1942">Neuen Parameter (-AzureStoragePath) zum Angeben von Azure Storage-Pfaden hinzugefügt, die in Windows- und Linux-Container-Apps bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="936ed-1942">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="936ed-1943">Verwenden Sie die Ausgabe des neuen Cmdlets New-AzureRmWebAppAzureStoragePath als Parameter zum Festlegen der Azure Storage-Pfade.</span><span class="sxs-lookup"><span data-stu-id="936ed-1943">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="936ed-1944">0.6.1 – November 2018</span><span class="sxs-lookup"><span data-stu-id="936ed-1944">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="936ed-1945">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="936ed-1945">Az.ApiManagement</span></span>
* <span data-ttu-id="936ed-1946">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1946">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="936ed-1947">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="936ed-1947">Az.Automation</span></span>
* <span data-ttu-id="936ed-1948">Swagger-basierte Azure Automation-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="936ed-1948">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="936ed-1949">Cmdlets zur Updateverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1949">Added Update Management cmdlets</span></span>
* <span data-ttu-id="936ed-1950">Cmdlets zur Quellcodeverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1950">Added Source Control cmdlets</span></span>
* <span data-ttu-id="936ed-1951">Cmdlet „Remove-AzureRmAutomationHybridWorkerGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1951">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="936ed-1952">DSC-Befehl für die Knotenregistrierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1952">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="936ed-1953">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="936ed-1953">Az.Compute</span></span>
* <span data-ttu-id="936ed-1954">Identitätsproblem für SystemAssigned-Identität korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1954">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="936ed-1955">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1955">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="936ed-1956">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="936ed-1956">Az.ContainerInstance</span></span>
* <span data-ttu-id="936ed-1957">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1957">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="936ed-1958">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="936ed-1958">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="936ed-1959">Beschreibung der Beispiele für Marketplace-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1959">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="936ed-1960">Az.Network</span><span class="sxs-lookup"><span data-stu-id="936ed-1960">Az.Network</span></span>
* <span data-ttu-id="936ed-1961">Folgende Cmdlets hinzugefügt: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="936ed-1961">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="936ed-1962">ICMP wieder unterstützten AzureFirewall-Netzwerkprotokollen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1962">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="936ed-1963">Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert und Überprüfung für Ziel-ID, Adresse und Port hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1963">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="936ed-1964">Probleme mit Arbeitsspeicherauslastung in der VirtualNetwork-Zuordnung behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-1964">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="936ed-1965">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="936ed-1965">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="936ed-1966">Problem beim Ändern der Richtlinie für eine geschützte Dateifreigabe behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-1966">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="936ed-1967">Richtlinienzeitzone in Großschreibung geändert</span><span class="sxs-lookup"><span data-stu-id="936ed-1967">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="936ed-1968">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="936ed-1968">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="936ed-1969">Korrigiertes Beispiel in „New-AzureRmRecoveryServicesAsrProtectableItem“</span><span class="sxs-lookup"><span data-stu-id="936ed-1969">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="936ed-1970">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1970">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="936ed-1971">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="936ed-1971">Az.Relay</span></span>
* <span data-ttu-id="936ed-1972">Optionaler Parameter „-KeyValue“ zu Cmdlet „New-AzureRmRelayKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht</span><span class="sxs-lookup"><span data-stu-id="936ed-1972">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="936ed-1973">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="936ed-1973">Az.Resources</span></span>
* <span data-ttu-id="936ed-1974">Hilfedokumentation für ressourcenidentitätsbezogene Parameter in `New-AzureRmPolicyAssignment` und `Set-AzureRmPolicyAssignment` aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-1974">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="936ed-1975">Beispiel für „New-AzureRmPolicyDefinition“ hinzugefügt, das „-Metadata“ nutzt</span><span class="sxs-lookup"><span data-stu-id="936ed-1975">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="936ed-1976">Korrektur, um Beibehaltung von Groß-/Kleinschreibung in Tagschlüsseln in „NetStandard“ zu ermöglichen: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="936ed-1976">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="936ed-1977">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="936ed-1977">Az.ServiceFabric</span></span>
* <span data-ttu-id="936ed-1978">Benachrichtigung über veraltete Elemente für anstehende wichtige Änderungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1978">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="936ed-1979">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="936ed-1979">Az.Sql</span></span>
* <span data-ttu-id="936ed-1980">Neue Cmdlets für CRUD-Vorgänge in verwalteten Azure SQL-Datenbank-Instanzen und verwalteten Azure SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-1980">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="936ed-1981">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="936ed-1981">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="936ed-1982">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="936ed-1982">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="936ed-1983">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="936ed-1983">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="936ed-1984">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="936ed-1984">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="936ed-1985">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="936ed-1985">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="936ed-1986">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="936ed-1986">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="936ed-1987">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="936ed-1987">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="936ed-1988">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="936ed-1988">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="936ed-1989">Erweiterte Verwaltung von Überwachungsrichtlinien auf einem Server oder in einer Datenbank aktiviert</span><span class="sxs-lookup"><span data-stu-id="936ed-1989">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="936ed-1990">Neuer Parameter (PredicateExpression) hinzugefügt, um die Filterung von Überwachungsprotokollen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="936ed-1990">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="936ed-1991">Cmdlets wurden angepasst, sodass sie SQL-Clients anstelle von Legacyclients verwenden.</span><span class="sxs-lookup"><span data-stu-id="936ed-1991">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="936ed-1992">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="936ed-1992">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="936ed-1993">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="936ed-1993">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="936ed-1994">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="936ed-1994">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="936ed-1995">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="936ed-1995">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="936ed-1996">Problem bei Verwendung von „Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings“ mit festgelegtem Parameter für den Speicherkontonamen behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-1996">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="936ed-1997">0.5.0 – November 2018</span><span class="sxs-lookup"><span data-stu-id="936ed-1997">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="936ed-1998">Allgemein</span><span class="sxs-lookup"><span data-stu-id="936ed-1998">General</span></span>
* <span data-ttu-id="936ed-1999">Ressourcenvervollständigungen für viele Kern-Cmdlets hinzugefügt (diese ermöglichen das Durchlaufen von vorhandenen Ressourcennamen per TAB-TASTE, wenn Cmdlets interaktiv aufgerufen werden)</span><span class="sxs-lookup"><span data-stu-id="936ed-1999">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="936ed-2000">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="936ed-2000">Az.Profile</span></span>
* <span data-ttu-id="936ed-2001">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="936ed-2001">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="936ed-2002">Parameter „TenantId“ im Cmdlet „Connect-AzAccount“ in „Tenant“ umbenannt und Alias für „TenantId“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-2002">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="936ed-2003">Beschreibung von „TenantId“ für „Connect-AzAccount“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="936ed-2003">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="936ed-2004">Fehlermeldung für fehlgeschlagene Anmeldung bei Angabe der Mandantendomäne korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-2004">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="936ed-2005">Problem in Bezug auf Kontextnamenskonflikt für Konten ohne Abonnements im Mandanten behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-2005">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="936ed-2006">Problem mit DataLake-Endpunkten bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-2006">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="936ed-2007">Problem behoben, das zur Auslösung von „Disconnect-AzAccount“ führte, wenn keine Verbindung bestand</span><span class="sxs-lookup"><span data-stu-id="936ed-2007">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="936ed-2008">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="936ed-2008">Az.CognitiveServices</span></span>
* <span data-ttu-id="936ed-2009">Vorgang „Get-AzCognitiveServicesAccountSkus“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-2009">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="936ed-2010">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="936ed-2010">Az.Compute</span></span>
* <span data-ttu-id="936ed-2011">Cmdlets Add-AzVmssVMDataDisk und Remove-AzVmssVMDataDisk hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-2011">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="936ed-2012">„Get-AzVMImage“ zeigt „AutomaticOSUpgradeProperties“ an</span><span class="sxs-lookup"><span data-stu-id="936ed-2012">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="936ed-2013">Problem behoben, aufgrund dessen die Optionswerte „SetAzVMChefExtension -BootstrapOptions“ und „-JsonAttribute“ nicht im JSON-Format festgelegt wurden</span><span class="sxs-lookup"><span data-stu-id="936ed-2013">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="936ed-2014">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="936ed-2014">Az.DataLakeStore</span></span>
* <span data-ttu-id="936ed-2015">Aktualisierung des DataLake-Pakets auf 1.1.10</span><span class="sxs-lookup"><span data-stu-id="936ed-2015">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="936ed-2016">Standardmäßige Parallelität zu Multithreadvorgängen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-2016">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="936ed-2017">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="936ed-2017">Az.Insights</span></span>
* <span data-ttu-id="936ed-2018">Problem Nr. 7267 behoben (Bereich für automatische Skalierung)</span><span class="sxs-lookup"><span data-stu-id="936ed-2018">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="936ed-2019">Probleme beim Erstellen einer neuen Regel für die automatische Skalierung, aufgrund derer die aufgelisteten Parameter nicht richtig festgelegt wurden (Es wurde stets der Standardwert festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="936ed-2019">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="936ed-2020">Problem Nr. 7513 behoben [Insights] „Set-AzDiagnosticSetting“ erfordert die explizite Angabe von Kategorien während der Erstellung der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="936ed-2020">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="936ed-2021">Nun erfordert das Cmdlet nicht die explizite Angabe der Kategorien, die während der Erstellung aktiviert werden sollen. Das bedeutet, es funktioniert wie dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="936ed-2021">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="936ed-2022">Az.Network</span><span class="sxs-lookup"><span data-stu-id="936ed-2022">Az.Network</span></span>
* <span data-ttu-id="936ed-2023">„PeeringType“ wurde geändert und ist nun ein erforderlicher Parameter für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="936ed-2023">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="936ed-2024">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="936ed-2024">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="936ed-2025">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="936ed-2025">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="936ed-2026">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="936ed-2026">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="936ed-2027">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="936ed-2027">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="936ed-2028">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="936ed-2028">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="936ed-2029">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="936ed-2029">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="936ed-2030">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="936ed-2030">Az.PolicyInsights</span></span>
* <span data-ttu-id="936ed-2031">Cmdlets für Richtlinienwartung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-2031">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="936ed-2032">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="936ed-2032">Az.Resources</span></span>
* <span data-ttu-id="936ed-2033">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="936ed-2033">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="936ed-2034">Zulassen der Auflistung von Ressourcen mithilfe des Parameters „-ResourceId“ für „Get-AzResource“</span><span class="sxs-lookup"><span data-stu-id="936ed-2034">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="936ed-2035">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="936ed-2035">Az.ServiceBus</span></span>
* <span data-ttu-id="936ed-2036">Schreibgeschützte Eigenschaft „MigrationState“ zu „PSServiceBusMigrationConfigurationAttributes“ hinzugefügt, was das Ermitteln des Migrationsstatus ermöglicht</span><span class="sxs-lookup"><span data-stu-id="936ed-2036">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="936ed-2037">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="936ed-2037">Az.ServiceFabric</span></span>
* <span data-ttu-id="936ed-2038">Hinzufügen des Zertifikats zu Linux VMSS korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-2038">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="936ed-2039">„Add-AzServiceFabricClusterCertificate“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="936ed-2039">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="936ed-2040">Verwenden des richtigen Fingerabdrucks aus dem neuen Zertifikat (Azure/service-fabric-issues#932)</span><span class="sxs-lookup"><span data-stu-id="936ed-2040">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="936ed-2041">Richtige Anzeige von Ausnahmen (Azure/service-fabric-issues#1054)</span><span class="sxs-lookup"><span data-stu-id="936ed-2041">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="936ed-2042">„Update-AzServiceFabricDurability“ korrigiert, um die Clusterkonfiguration zu aktualisieren, bevor der VMSS-Vorgang „CreateOrUpdate“ gestartet wird</span><span class="sxs-lookup"><span data-stu-id="936ed-2042">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="936ed-2043">0.4.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="936ed-2043">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="936ed-2044">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="936ed-2044">Az.Profile</span></span>
* <span data-ttu-id="936ed-2045">Problem mit „Get-AzSubscription“ in Cloud Shell behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-2045">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="936ed-2046">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="936ed-2046">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="936ed-2047">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="936ed-2047">Az.Compute</span></span>
* <span data-ttu-id="936ed-2048">Neue Größen zur Whitelist von VM-Größen hinzugefügt, für die bei Verwendung des einfachen Parametersatzes für „New-AzVm“ der beschleunigte Netzwerkbetrieb aktiviert wird</span><span class="sxs-lookup"><span data-stu-id="936ed-2048">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="936ed-2049">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-2049">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="936ed-2050">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="936ed-2050">Az.DataLakeStore</span></span>
* <span data-ttu-id="936ed-2051">Unterstützung für VNET-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-2051">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="936ed-2052">Get-AzDataLakeStoreVirtualNetworkRule: Dient zum Abrufen oder Auflisten der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="936ed-2052">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="936ed-2053">Add-AzDataLakeStoreVirtualNetworkRule: Fügt dem angegebenen Data Lake Store-Konto eine Regel für das virtuelle Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="936ed-2053">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="936ed-2054">Set-AzDataLakeStoreVirtualNetworkRule: Ändert die angegebene Regel für das virtuelle Netzwerk in das angegebene Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="936ed-2054">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="936ed-2055">Remove-AzDataLakeStoreVirtualNetworkRule: Dient zum Löschen der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="936ed-2055">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="936ed-2056">Az.Network</span><span class="sxs-lookup"><span data-stu-id="936ed-2056">Az.Network</span></span>
* <span data-ttu-id="936ed-2057">Cmdlet „Test-AzNetworkWatcherConnectivity“ aktualisiert, Protokollwert wird jetzt an Back-End übergeben.</span><span class="sxs-lookup"><span data-stu-id="936ed-2057">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="936ed-2058">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-2058">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="936ed-2059">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="936ed-2059">Az.Resources</span></span>
* <span data-ttu-id="936ed-2060">Problem behoben, aufgrund dessen „Get-AzRoleDefinition“ eine unverständliche Ausnahme auslöst (wenn das Standardprofil kein Abonnement enthält und kein Bereich festgelegt ist), indem im Szenario eine aussagekräftige Ausnahme hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="936ed-2060">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="936ed-2061">Außerdem wurde der Standardparametersatz auf „RoleDefinitionNameParameterSet“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="936ed-2061">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="936ed-2062">0.3.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="936ed-2062">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="936ed-2063">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="936ed-2063">Azure.Storage</span></span>
* <span data-ttu-id="936ed-2064">Fehler beim Kopieren von Blobs/Dateien behoben, aufgrund dessen bei einem Metadatenproblem des Ziels keine Metadaten kopiert wurden</span><span class="sxs-lookup"><span data-stu-id="936ed-2064">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="936ed-2065">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="936ed-2065">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="936ed-2066">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="936ed-2066">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="936ed-2067">Der Abruf der Speicherressourcennutzung eines bestimmten Standorts wird jetzt unterstützt, und das Hinzufügen einer Warnmeldung für den Abruf der globalen Speicherressourcennutzung ist überflüssig.</span><span class="sxs-lookup"><span data-stu-id="936ed-2067">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="936ed-2068">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="936ed-2068">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="936ed-2069">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="936ed-2069">Az.CognitiveServices</span></span>
* <span data-ttu-id="936ed-2070">„Get-AzCognitiveServicesAccountSkus“ wird ohne vorhandenes Konto unterstützt.</span><span class="sxs-lookup"><span data-stu-id="936ed-2070">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="936ed-2071">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="936ed-2071">Az.Compute</span></span>
* <span data-ttu-id="936ed-2072">Korrektur von „Get-AzVM -ResourceGroupName <rg>“, sodass ggf. mehr als 50 Ergebnisse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="936ed-2072">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="936ed-2073">Der Cmdlet-Hilfe zu „New-AzVmss“ wurde ein Beispiel für „SimpleParameterSet“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-2073">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="936ed-2074">Tippfehler in der Azure Disk Encryption-Statusmeldung behoben</span><span class="sxs-lookup"><span data-stu-id="936ed-2074">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="936ed-2075">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="936ed-2075">Az.DataFactoryV2</span></span>
* <span data-ttu-id="936ed-2076">Die Version des ADF .Net-SDK wurde auf 2.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="936ed-2076">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="936ed-2077">Az.Network</span><span class="sxs-lookup"><span data-stu-id="936ed-2077">Az.Network</span></span>
* <span data-ttu-id="936ed-2078">NetworkProfile-Funktionalität wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="936ed-2078">Added NetworkProfile functionality.</span></span> <span data-ttu-id="936ed-2079">Neue Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-2079">new cmdlets added</span></span>
    - <span data-ttu-id="936ed-2080">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="936ed-2080">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="936ed-2081">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="936ed-2081">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="936ed-2082">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="936ed-2082">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="936ed-2083">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="936ed-2083">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="936ed-2084">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="936ed-2084">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="936ed-2085">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="936ed-2085">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="936ed-2086">Dienstzuordnungslink in Subnetzmodell hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-2086">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="936ed-2087">Cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-2087">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="936ed-2088">Cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-2088">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="936ed-2089">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="936ed-2089">Az.RedisCache</span></span>
* <span data-ttu-id="936ed-2090">Künftig sind beliebige Zeichenfolgen als Größenparameter zulässig.</span><span class="sxs-lookup"><span data-stu-id="936ed-2090">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="936ed-2091">P5 in Popup „PSArgumentCompleter“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-2091">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="936ed-2092">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="936ed-2092">Az.Resources</span></span>
* <span data-ttu-id="936ed-2093">Fehlender Parameter „-Mode“ zu „Set-AzPolicyDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="936ed-2093">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="936ed-2094">Cmdlet-Fehler bei „Get-AzProviderOperation“ für Vorgänge mit Ursprung behoben, der den Benutzer enthält</span><span class="sxs-lookup"><span data-stu-id="936ed-2094">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="936ed-2095">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="936ed-2095">Az.Sql</span></span>
* <span data-ttu-id="936ed-2096">Problem behoben, aufgrund dessen einige Sicherungs-Cmdlets das aktuelle Azure-Abonnements nicht erkannt haben</span><span class="sxs-lookup"><span data-stu-id="936ed-2096">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="936ed-2097">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="936ed-2097">Az.Websites</span></span>
* <span data-ttu-id="936ed-2098">Neues Cmdlet „Get-AzWebAppContainerContinuousDeploymentUrl“ zum Abrufen der Webhook-URL von Continuous Deployment für Container</span><span class="sxs-lookup"><span data-stu-id="936ed-2098">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="936ed-2099">Neue Cmdlets „New-AzWebAppContainerPSSession“ und „Enter-WebAppContainerPSSession“ zum Initiieren einer PowerShell-Remotesitzung in einer Windows-Container-App</span><span class="sxs-lookup"><span data-stu-id="936ed-2099">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="936ed-2100">0.2.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="936ed-2100">0.2.0 - September 2018</span></span>
 <span data-ttu-id="936ed-2101">Erstrelease</span><span class="sxs-lookup"><span data-stu-id="936ed-2101">Initial Release</span></span>
